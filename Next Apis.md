In apps, create api directory. In api directory, set the route for your api aka create user file for /user

create a route.ts inside of the directory and

```ts
import { NextResponse } from "next/server";
export const GET = () => {
    return new NextResponse("Thsi is my first api")
}
```
folders with () are purely organizational and don't affect the url