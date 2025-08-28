# How to use

## requiring the UILib
Grabs the UI Library from this repository

```lua
local UILib = loadstring(game:HttpGet("https://raw.githubusercontent.com/MX6-RBX/UiLib/refs/heads/main/UiLib.lua"))()
```

## Creating a UI
Creates a new UI Frame with the given name assigned to it

```lua
local UI = UILib:New("Ui Name")
```

## Adding a page 
Multiple pages can be created
Pages need a unique name
Pages can hold multiple sections 

A  Icon/thumbnail can be added by using an image id in the second Argument(Set 1 here)
```lua
local Page = UI:addPage("Page Name",1)
```

## Creating a section
```lua
local Section = Page:addSection("Section Name")
```

## Creating A Basic Button
```lua
local Button = Section:addButton("Button Name, function()
  print("button was clicked")
end)
```

## Creating A Toggle Button
Value can be use to set a varables value ext

```lua
local Toggle = Section:addToggle("Toggle Name",function(Val)
  print(Val)
end)
```

## Creating a Text Box

Default Text can be any string you want
will fire the function any time the text box is changed in any way(click on it, adding text, removing text, clicking off it)

```lua
local TextBox = Section:addTextBox("Text Box Name","Default Text", function(text)
  print(text)
end)
```

## Creating A Slider
A Slider will have 3 Arguments 
Default Value 
Min Value
Max Value
All three must be a number 

Just like the text box this will fire when ever the slider is changed
```lua
local Slider = Section:addSlider("Slider Name", 1,1,100, function(Val)
  print(Val)
end)
```

## Creating A KeyBind 
Will Fire when the inputted key is pressed

```lua
local KeyBind = Section:addKeybind("Key Bind Name",Enum.KeyCode.A, function()
  print("Key Pressed)"
end)
```

## Crating Drop Down
A drop down will hold a Table for the list it will have 

This fire when an option is chosen 
```lua
local DropDown = Section:addDropdown("Drop Down Name"{"Option1","Option2",Option3",function(Selected}
  print(Selected)
end)
```

## Creating A color selector

```lua
local ColorPicker = Section:addColorPicker("Color Picker Name", Color3.fromRGB(255,255,255), function(Col)
  print(Col)
end)
```







