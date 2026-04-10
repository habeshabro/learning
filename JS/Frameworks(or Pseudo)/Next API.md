put api route in routes,
(routes) are ignored in routes
put models and db in lib

```ts
import mongoose from "mongoose";
const mongo_uri = process.env.MONGO_URI || "mongodb://127.0.0.1:27017";
const connect = async() => {
    switch(mongoose.connection.readyState){
        case 1:
            console.log("Already Connected");
            break;
        case 2:
            console.log("connectig...");
            break;
        default:
            try{
                mongoose.connect(mongo_uri, {
                    dbName: 'nextDB',
                    bufferCommands: true

                })
                console.log("connected")
            } catch(err) {
                console.log("error",err);
            }
    }
}

export default connect;
```
 ```TS
import connect from "@/lib/db";
import User from "@/lib/models/user.model";
import { NextResponse } from "next/server";

export const GET = async () => {
    try {
        await connect();
        const users = await User.find();
        return new NextResponse(JSON.stringify(users), {status: 200})
    } catch(err){
        return new NextResponse("error in fetching", {status: 500} )
    }
}

export const POST = async (request: Request) => {
    try {
        const body = await request.json();
        await connect();
        const newUser = new User(body);
        await newUser.save();
        NextResponse(JSON.stringify(newUser), {status: 200})
    } catch(error:any) {}
}
```

```ts
const ObjectId = require("mongoose").Types.ObjectId;
import {Types} from "mongoose"

ObjectId.isValid(userId) //check valid
const updatedUser = await User.findOneAndUpdate({_id: new ObjectId(userId)}, {userName: userName}, {new: true})
```

```ts
	const {searchParams} = new URL(request.url);
	const userId = searchParams.get("userId")
	
```
```ts
user: {type: Schema.Types.ObjectId, ref: "User"}

new Category({title: title, user: new ObjectId(userId)})
```
square brackets "[]" make dynamic url

```ts
//let's say the url is /[category]
export const PATCH = async(request: Request, context: { params: any}) => {
const categoryId = context.params.category;
}
```
```ts
	const filter: any = {
		user: new ObjectId(userId),
		category: new ObjectId(categoryId)
	}
	filter.$or = [
		{
			title: {$regex: searchTerm, $options: 'i'}
		}
	]
	filter.createdAt = {
	$gte: new Date(), $lte: new Date()
	}
const cc = await Blog.find(filter).sort({
	createdAt: "asc"
}).skip(skip).limit(limit)
```

create middleware.ts

```ts
export const config = {
matcher: "/api/:path*",
}

export default function middleware(request: Request){
	const authResult = authMiddleWare(request);
	if(!authResult?.isValid){
		return new NextResponse(JSON.stringify({ meddage: "Unauthorized"}), {status: 401})
	}
	return NextResponse.next();
}
```

create middlewares file, 
name the middleware mstn like api/authMiddleware.ts
```ts
const validate = (token: any) => {
	const validToken = true;
	if(!validToken){
		return false;
	}
	return true;
}

export function authMiddleWare(req: Request) {
	const token = req.headers.get("authorization")?.splait(" ")[1];
	return { isVAlid: validate(token)}
}
```