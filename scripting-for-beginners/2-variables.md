# Variables

## What are Variables?

A **variable** is data that can change, depending on conditions or information passed to the program. **Variables** can store **strings**, **numbers**, **integers**, **booleans**,
**objects** and many more **object types**!

Variables can be useful when scripting because it stores data that can be called multiple times instead of repeating the object type over and over.

For more information, see [Variable (computer science)](https://en.wikipedia.org/wiki/Variable_(computer_science))

## Creating a variable

Let's go back to our **Script** in **ServerScriptService** from our previous article. Delete all the code in the script and type the following:
```lua
local MyVariable = "This is my variable!"
```
This line of code creates a **variable** called **MyVariable** and has the string **"This is my variable!"** assigned to it.

However, if we run this, you see nothing prints in the console. This is because we haven't given the variable an actual use. So let's make it so that
it prints out our variable.

## Printing our Variable

To print a variable, we have to do someone slightly different.

Instead of doing:
```lua
print("MyVariable")
```

We do:
```lua
print(MyVariable)
```
Noticed what changed?

When printing a **variable**, we **do not** put the name of the **variable in quotations** due to **our string being assigned to the variable**. However **when printing something that isn't a variable**, you **have to put the text in quotations**.

Now when we **run our game**, the string should be printed out as shown below:
![image](https://user-images.githubusercontent.com/70015895/165128402-42c78a20-d42c-4067-b37e-ce23813490e4.png)

### And that concludes the second article on how to script in **Roblox!**
#### Next time we will learn about basic math in **Roblox!**
