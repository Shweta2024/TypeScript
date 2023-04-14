## Syntax

- ```  let variableName: type = value  ```

- There are many types in TS and they can be found [here](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html)

## Primitive types : number, string & boolean.

![image](https://user-images.githubusercontent.com/75883328/231978020-4eb6637d-17bf-4435-bca2-c0adefe93868.png)


## Type Inference
We are not required to each time write the type while declaring a variable like in the above picture we have declared num & initialised it the with value 2 at the same 
time, so typescrpit is smart enough to understand that its a number and we aren't required to write the types at those situations.

![image](https://user-images.githubusercontent.com/75883328/231980166-fd4792c9-cd2a-4e21-9145-e2c917302965.png)


## Any 
- When we don't specify the type of a variable & the complier fails to infer its type, then the compiler default it to ``` any```. 
- we use ``` any ``` when we don't wnat it to get type-checked.
- Using any is not a good practice. TRY TO AVOID USING ANY.


![image](https://user-images.githubusercontent.com/75883328/231981888-71a8572d-78ab-4529-bf28-1397e9e6c2bf.png)


## Objects
![image](https://user-images.githubusercontent.com/75883328/232025803-67a1ec7b-6a56-4720-a0c2-1a234079cd54.png)

## Type Alias

![image](https://user-images.githubusercontent.com/75883328/232028836-ae726434-837b-4dec-b98b-42144373dec9.png)
