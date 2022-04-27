# Changing Part Properties

## What are part properties?

Properties are data for an instance inside Roblox which is assigned to the object, for example, color can be changed.

## Creating a variable for our part

Let's create a new **Part** called **"OurPart"** in **workspace**.

Next, let's create a new **script** called **PropertiesChanger** in **ServerScriptService**.

## Changing Part Properties

Now, in the script, type the following code:
```lua
local Part = game.Workspace.OurPart
```
This line will reference our part in the script.

Next, let's unanchor our part in the script by typing the following line:
```lua
Part.Anchored = true
```

Now, if you the game, you can see our part is anchored.

Now, lets make it so that our part changes the color to blue like so:
```lua
Part.Color = BrickColor.new("Bright blue")
```
## Running our game

If you run the game now, you can see our part is anchored and the color has changed to blue.

### And that concludes the fifth article on how to script in Roblox!
Next we will learn about if statements and for loops!
