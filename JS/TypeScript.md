```sh
npm install typescript
npx init --tsc
tsc # npx tsc if local
```
```ts
let myName: string;
let myAge: number;
let isStrudent: boolean;
let ages: number[]

type Person = {
    name: string
    age: number
    isStudent?: boolean
}

type UserRole = "guest" | "member" | "admin" //unions

funciton a(name:string) : Person {
}

const myArrowFunction = (param1: type1, param2: type2): returnType => {};
void
any

Partial<User>
Omit<Type, Keys>
function getLast<T>(array: T[])
```