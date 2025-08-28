# How to use
### All UI Elements need a unique Name


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

A  Icon/thumbnail can be added by using an image id in the second Argument(Set 1 here) but is not required
```lua
local Page = UI:addPage("Page Name",1)
```

## Creating a section

sections will hold the Interactable elements

```lua
local Section = Page:addSection("Section Name")
```

## Creating A Basic Button
Buttons will fire a function when clicked 
```lua
local Button = Section:addButton("Button Name, function()
  print("button was clicked")
end)
```

## Creating A Toggle Button
Toggles will fire a function when click and will pass the changed value

```lua
local Toggle = Section:addToggle("Toggle Name",function(Val)
  print(Val)
end)
```

## Creating a Text Box

Text Boxes will fire a function when ever there is a change to it(Clicking on it, Editing the text, Clicking off it) and pass the text at the time of the chnage 

Default Text can be anything as long as its made a string 

```lua
local TextBox = Section:addTextBox("Text Box Name","Default Text", function(text)
  print(text)
end)
```

## Creating A Slider
A Slider will have 3 Arguments 

Default Value

Min Value

Max Value. 

All three must be a number 

Just like the text box this will fire when ever the slider is changed and will pass the value the slider is at
```lua
local Slider = Section:addSlider("Slider Name", 1,1,100, function(Val)
  print(Val)
end)
```

## Creating A KeyBind 
Lets you set a custom key bind

Will Fire when the chosen key is pressed

```lua
local KeyBind = Section:addKeybind("Key Bind Name",Enum.KeyCode.A, function()
  print("Key Pressed)"
end)
```

## Crating Drop Down
A drop down will hold a Table for the list it will have  in its second argument 

will fire when an option is chosen from the list and pass the chosen option
```lua
local DropDown = Section:addDropdown("Drop Down Name"{"Option1","Option2",Option3",function(Selected}
  print(Selected)
end)
```

## Creating A color selector
allows for a custom color to be picked

will fire when ever the color is being changed and will pass the chosen color
```lua
local ColorPicker = Section:addColorPicker("Color Picker Name", Color3.fromRGB(255,255,255), function(Col)
  print(Col)
end)
```







