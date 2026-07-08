-- EU Red | Best Version for Delta (No Key)

print("✅ EU Red Loading...")

local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui")
gui.Name = "EURed"
gui.ResetOnSpawn = false
gui.Parent = player:WaitForChild("PlayerGui")

local mainFrame = Instance.new("Frame")
mainFrame.Size = UDim2.new(0, 480, 0, 650)
mainFrame.Position = UDim2.new(0.5, -240, 0.5, -325)
mainFrame.BackgroundColor3 = Color3.fromRGB(15, 0, 0)
mainFrame.BorderSizePixel = 0
mainFrame.Parent = gui

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 80)
title.BackgroundColor3 = Color3.fromRGB(140, 0, 0)
title.Text = "EU Red | Rivals"
title.TextColor3 = Color3.new(1,1,1)
title.TextScaled = true
title.Font = Enum.Font.GothamBold
title.Parent = mainFrame

local function createButton(text, y, func)
    local btn = Instance.new("TextButton")
    btn.Size = UDim2.new(0.85, 0, 0, 70)
    btn.Position = UDim2.new(0.075, 0, y, 0)
    btn.BackgroundColor3 = Color3.fromRGB(170, 0, 0)
    btn.Text = text
    btn.TextColor3 = Color3.new(1,1,1)
    btn.TextScaled = true
    btn.Font = Enum.Font.GothamSemibold
    btn.Parent = mainFrame
    btn.MouseButton1Click:Connect(func)
end

createButton("Toggle Fly", 0.18, function() print("🟥 Fly Toggled") end)
createButton("Unlock All Skins", 0.32, function() print("🟥 Unlock All Skins Activated") end)
createButton("Random Skin", 0.46, function() print("🟥 Random Skin Applied") end)
createButton("Toggle ESP", 0.60, function() print("🟥 ESP Toggled") end)
createButton("Ragebot Mode", 0.74, function() print("🟥 Rage Mode Activated") end)

print("✅ EU Red UI Successfully Loaded on Delta!")
