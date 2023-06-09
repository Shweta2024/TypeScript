## Interface

```ts

//INTERFACE
interface User {
    readonly dbId : number
    userId: number,
    email: string,
    googleId? : string,

    //functions
    startTrail() : string,
    getDiscount(coupon: number) : number
}

let newUser : User = {
    dbId: 1,
    userId: 20,
    email: 'abc@gmail.com',

    startTrail(){
        return "trail started"
    },

    getDiscount(coupon : 0){
        return 0;
    }
}

export {}


```


## we can add new properties to the same interface after declaring it - it is called Reopening of the iterface.


```ts

//INTERFACE
interface User {
    readonly dbId : number
    userId: number,
    email: string,
    googleId? : string,

    //functions
    startTrail() : string,
    getDiscount(coupon: number) : number
}

interface User{
    gitHubAc : string
}

let newUser : User = {
    dbId: 1,
    userId: 20,
    email: 'abc@gmail.com',

    startTrail(){
        return "trail started"
    },

    getDiscount(coupon : 0){
        return 0;
    },
    gitHubAc: 'githubbbb'
}

export {}

```

## Alows Inheritence : one interface can inherit another

```ts

//INTERFACE
interface User {
    readonly dbId : number
    userId: number,
    email: string,
    googleId? : string,

    //functions
    startTrail() : string,
    getDiscount(coupon: number) : number
}

//INHERITENCE
interface Admin extends User{
    role : "head" | "business admin"
}
let newUser : Admin = {
    dbId: 1,
    userId: 20,
    email: 'abc@gmail.com',
    role: "head",

    startTrail(){
        return "trail started"
    },

    getDiscount(coupon : 0){
        return 0;
    }
}

export {}

```

## Difference between Interface & type
- Interface can be re-opened i.e. can add new properties to it after it has been declared.
- Type can't be re-opened.
