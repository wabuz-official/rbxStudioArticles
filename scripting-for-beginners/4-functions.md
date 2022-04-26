# Functions

## What are functions?

A function is a set of commands that can be runned multiple times in the script. Once it has been defined in the script, it can be executed as many times by calling the function.

For more information, check out [Functions](https://developer.roblox.com/en-us/articles/Function)

## Creating a function

Let's make a new **script** called **FunctionsTesting** and put it in **ServerScriptService**. There are few ways to create a **function**, but we're going to use the regular **function** object.

In our **script**, type the following code:

```lua
function MyFunction()
	print("This is my function")
end
```

as you can see, we have created a **function** that prints out **"This is my function"**. However, if we run this, you see nothing happens. That is because we haven't called the function, so lets do that now.

## Calling our function

To call our **function**, it is pretty easy, all we have to do is type the following line of code:
```lua
MyFunction()
```
> NOTE: If your **function** has a **different name**, put the **name** of the **function** in front of the **brackets**.

Now, let's say there is **specific** **data** that you want your **function** to use, to do that, we're going to use **Parameters**.

## Giving our **function** **parameters**.

To give our **function** **parameters**, it's pretty straight forward. Let's create a **variable** with the **variable name** being **Parameter** with the string value being "This is my parameter".

Next, **modify** the **function** to the following **code**:
```lua
function MyFunction(String)
	print(String)
end
```
As you can see, we **defined** the **parameter** with the **variable** name being called **"String"**.

Now, let's put the actual **String data** when we **call** the **function** by putting in the **Parameter** **variable** we made previously within the **brackets** like so:
```lua
MyFunction(Parameter)
```

Your final code should look something similiar to this:
```lua
local Parameter = "This is my parameter"

function MyFunction(String : string)
	print(String)
end

MyFunction(Parameter)
```

## Running our game

Lets run our **game** to see if it works.

![ezgif com-gif-maker (3)](https://user-images.githubusercontent.com/70015895/165327655-c06e8604-a0d3-42a2-8590-07492b1ae4b3.gif)

It works!

### And that concludes the fourth article on how to script in Roblox!
#### Next we will learn about **part values**!
