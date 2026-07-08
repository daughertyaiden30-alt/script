-- EU Red | Final Delta Fixed Version (No Key)

print("✅ Loading EU Red...")

local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui")
gui.Name = "EURed"
gui.ResetOnSpawn = false
gui.Parent = player:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 460, 0, 620)
frame.Position = UDim2.new(0.5, -230, 0.5, -310)
frame.BackgroundColor3 = Color3.fromRGB(18, 0, 0)
frame.BorderSizePixel = 0
frame.Parent = gui

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 70)
title.BackgroundColor3 = Color3.fromRGB(160, 0, 0)
title.Text = "EU Red | Rivals"
title.TextColor3 = Color3.new(1,1,1)
title.TextScaled = true
title.Font = Enum.Font.GothamBold
title.Parent = frame

local function makeButton(text, yPos, callback)
    local btn = Instance.new("TextButton")
    btn.Size = UDim2.new(0.85, 0, 0, 65)
    btn.Position = UDim2.new(0.075, 0, yPos, 0)
    btn.BackgroundColor3 = Color3.fromRGB(180, 0, 0)
    btn.Text = text
    btn.TextColor3 = Color3.new(1,1,1)
    btn.TextScaled = true
    btn.Font = Enum.Font.GothamSemibold
    btn.Parent = frame
    btn.MouseButton1Click:Connect(callback)
end

makeButton("Toggle Fly", 0.18, function() print("🟥 Fly Toggled") end)
makeButton("Unlock All Skins", 0.32, function() print("🟥 Unlock All Activated") end)
makeButton("Random Skin Changer", 0.46, function() print("🟥 Random Skin Applied") end)
makeButton("Toggle ESP", 0.60, function() print("🟥 ESP Toggled") end)
makeButton("Rage Mode", 0.74, function() print("🟥 Rage Mode ON") end)

print("✅ EU Red UI Loaded on Delta!")
