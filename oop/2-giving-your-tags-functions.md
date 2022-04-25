# Giving your Tags Functions

Welcome back! In the previous article, I introduced you to **Object-oriented programming** and the **Tag Editor**.
Now, I'm going to show you how to script the tags to have an actual function!


First, in the **Explorer**, create a new **Server Script** in **ServerScriptService** called **'TagHandler'**

![image](https://user-images.githubusercontent.com/70015895/165090851-dee9a69c-8d7a-4f34-a0b2-6f7f5da70379.png)

Then, add a **Folder** in **ServerScriptService** called **TagModules**.
In the folder, create a new **Module Script** with the same name as your tag.

In the module script, type the following code:

```lua
local CollectionService = game:GetService("CollectionService")

local TagModule = {}

function TagModule:Start()
	for i, part in ipairs(workspace:GetDescendants()) do
		if CollectionService:HasTag(part, "YOUR_TAG_NAME") then
			TagModule:Init(part)
		end
	end
end

function TagModule:Init(instance : instance)
	
end

return TagModule
```
> Note: on line 7 (the if statement checking if a part has a tag called "YOUR_TAG_NAME"), make sure to put the name of your tag in the quotes, it is caps sensitive.

In the Init function, we will state what we want our part to do. I will make my part change from blue to yellow every second using the following code:

```lua
function TagModule:Init(instance : instance)
	if instance:IsA("BasePart") then
		while task.wait(1) do
			instance.BrickColor = BrickColor.new("Bright blue")
			task.wait(1)
			instance.BrickColor = BrickColor.new("New Yeller")
		end
	end
end
```


Back in our **TagHandler** script, type the following script:
```lua
local TagModules = game:GetService("ServerScriptService"):WaitForChild("TagModules")

for i, module in ipairs(TagModules:GetChildren()) do
	if module:IsA("ModuleScript") then
		local RequiredModule = require(TagModules:FindFirstChild(module.Name))
		if RequiredModule then
			print("called module", module.Name)
			RequiredModule:Start()
		else
			warn("attempted to fetched module. Failed.")
		end
	end
end
```

Now when I run the game, my part does this:

![ezgif com-gif-maker (1)](https://user-images.githubusercontent.com/70015895/165094667-eb8572f4-88d6-4d93-bcf5-a73b92cdb448.gif)

_**It works!**_

### And boom! We're done! Since this is object-oriented, you can create new tags with the **Tag Editor** as long as you make a module for the tag and you have the the **:Start()** and **:Init()** functions.
