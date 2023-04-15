## Generics : locks the type -> when we want the return type of function to be same as that of the argument


```ts

//suppose we want a function that takes a number as input & gives number as output OR
//takes a string as input & gives a string as output
//in general we want a function that returns a value as the same type of the argument

function identityOne(val : number | string): number | string {
    return val
}


```

the above piece of code won't serve our need its because according to that code even if my argument is a number it can return a string & vice-versa.

<br>

```ts

function identityTwo(val : any) : any {
    return val
}


```
the above code will also not serve our need because it too can take arguments of any-datatype(i.e. number,sting,boolean etc) as input & will return a value of type any.

<br>

```ts

function identityThree(val: number | string | boolean) : number | string | boolean {
    if(typeof(val) === "number")
        //do some computation....
        return 1

    else if(typeof(val) === "string")
        //do some computation....
        return "1"

    else
        //do some computation....
        return true
}

```
the above code might solve our problem but imagine a situtation when we'll have more than just 3 datatypes, at that time we'll be having n number of if-else if 
statements for checking the types & performing the further calculations, that makes our code further lengthly & this isn't a good approach.

<br>

### Using generics

```ts

function identityFour<Type> (val : Type) : Type{
    return val
}

identityFour(1)
identityFour("1")
identityFour(true)


```

the above approach of using generic solves our problem, when we write  ``` <Type> ``` (Type in angular brackets), it locks that type, i.e. it locks the type of the 
agrument passed to the function & returns a value of the same type.

- another way of writing the same code

```ts

function identityFour<A> (val : A) : A{
    return val
}

identityFour(1)
identityFour("1")
identityFour(true)

```

- we can write any capital letter/word in place of Type.

## Generics of interface type

```ts

interface Phone{
    color: string
    model: number
}

function identity<Phone> (val : Phone): Phone {
    return val
}

identity({color:'blue',model: 7})


```

## Using Type parameters in Generic constraint

EXAMPLE 1

```ts


//it is taking a parameter of type Type as input and the another parameter is any of the keyof Type 
//So if our 1st parameter is an object then the 2nd parameter should be any of the key of that object
function getKey<Type, Key extends keyof Type> (obj : Type, key: Key){
    return obj[key]
}

let x = {'a': 1, 'b' : 2, 'c' : 3, 'd' : 4}
getKey(x,'a')


//it gives us squiggly lines, because the key is extending the keyof Type
//i.e. key is extending the keyof x, and in x we don't have any key as 'j'
getKey(x,'j')

```


EXAMPLE 2 

```ts

interface User{
    name: string
    age: number
}

function getIdentity<Type, newUser extends User>(val1: Type, val2: newUser): string {
    return "implementing type parameters in generic constraint"
}

getIdentity(4,{name:'s', age: 1})


```

## Generic class

```ts


interface book {
    name: string
    author : string
}

interface bottle{
    color: string
    capacity: number
}

//here the Type can be anything like it can be a book or a bottle
class sellAble<T> {
    public cart: T[] = []

    addToCart(product : T): void{
        this.cart.push(product);
        console.log("product added to cart!")
    }
}


```







