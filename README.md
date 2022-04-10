local ToggleNOOB = Instance.new("ScreenGui")
local ToggleN = Instance.new("TextButton")
local UICorner = Instance.new("UICorner")

ToggleNOOB.Name = "ToggleNOOB"
ToggleNOOB.Parent = game.CoreGui
ToggleNOOB.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

ToggleN.Name = "ToggleN"
ToggleN.Parent = ToggleNOOB
ToggleN.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
ToggleN.Position = UDim2.new(0.104927011, 0, 0.168986082, 0)
ToggleN.Size = UDim2.new(0, 64, 0, 64)
ToggleN.Font = Enum.Font.SourceSans
ToggleN.Text = "Th"
ToggleN.TextColor3 = Color3.fromRGB(255, 0, 0)
ToggleN.TextSize = 50.000
ToggleN.MouseButton1Click:Connect(function() 
	game.CoreGui:FindFirstChild("UICopied").Enabled = not game.CoreGui:FindFirstChild("UICopied").Enabled 
end)
UICorner.Parent = ToggleN

local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Patskorn/GUI/main/Copy-SynapOver.lua"))()

local GUI = library:new("SynapOver","[ RightControl ]")
local Tab1 = GUI:Tap("Menu 1")
local Tab2 = GUI:Tap("Menu 2")

Tab1:Toggle("Toggle",nil,function(a)
    AutoFarm = a
end)

spawn(function()
while wait(0.1) do
if AutoFarm then
pcall(function()

local A_1 = "swingKatana"
local Event = game:GetService("Players").LocalPlayer.ninjaEvent
Event:FireServer(A_1)

end)
end
end
end)
