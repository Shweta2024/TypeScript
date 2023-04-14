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
- public : can be accessed by anyone anywhere.
- private : can be accessed only within that class.
- protected : can be accessed within that class & by the derived classes.


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

## class implements interface

```ts


interface TakePhoto{
    cameraMode : string
    filter : string
}

interface story{
    count : number
}

class Instagram implements TakePhoto{
    constructor(
                public cameraMode: string,
                public filter: string,
                public story : string
                ){}

    showStory(): void{
        console.log("story displayed!")
    }
}

class youtube implements TakePhoto, story{
    constructor(
        public cameraMode: string,
        public filter: string,
        public count: number,
        public shorts: number
    ){}

    displayShorts(): number{
        return this.count;
    }
}


```

## Abstract class

- we don't implement any method inside it , we just declare the variables & the methods.
- The classes that extends it, overwrites the abstract method.
-  we can't create any objetcs for an abstract class.

```ts



abstract class TakePhoto{
    constructor(public cameraMode: string, public filter: string){}

    public abstract showPicture(): string
}

class Instagram extends TakePhoto{
    constructor(public cameraMode: string, public filter: string){
        super(cameraMode,filter);
    }

    public showPicture(): string {
        return "picture shown!";
    }
}


```
