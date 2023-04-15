## using ``` in ``` operator

```ts


//we want to check whether the account is of User or Admin type
///we'll be using the ```in``` operator for that

interface User {
    name: string
    age: number
    isUser: boolean
}

interface Admin{
    name: string
    department: string
    isAdmin: boolean
}

function typeOfAccount(account: User | Admin): string{
    if("isUser" in  account)
        return "it is a User"
    else
        return "it is an Admin"
}



```

- using ``` instanceof ```
- using type predicates
- using  discriminated union 
- using exhaustive checking
