## How do we write a class?

```ts

//classes

class User {
    name : string
    age : number
    email: string

    constructor(name: string, age: number, email: string){
        this.name = name
        this.age = age
        this.email = email
    }
}

let newUser = new User('shweta',20,'abc@gmail.com')

```

## Better way of writing the above code

```ts


class User {

    private id : number
    constructor(public name: string,
                public age: number){            
        this.name= name
        this.age= age
    }
}

let newUser = new User('shweta',20)


```


## Access Modifiers 
- public
- private
- protected


## getters & setters

- we don't mention any return typr for the setters not even void.

```ts


class User {

    //private access modifier
    private id : number

    constructor(public name: string,public age: number){            
        this.name= name
        this.age= age
    }

    //setter
    set setID(id: number){
        this.id = id
    }

    //getter
    get getID(): number {
        return this.id
    }
}

let newUser = new User('shweta',20)


```

