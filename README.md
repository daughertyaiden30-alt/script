-- EU Red | Delta Fixed + Simple UI (No Key)

print("✅ Loading EU Red...")

local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui")
gui.Name = "EURed"
gui.ResetOnSpawn = false
gui.Parent = player:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 450, 0, 600)
frame.Position = UDim2.new(0.5, -225, 0.5, -300)
frame.BackgroundColor3 = Color3.fromRGB(20, 0, 0)
frame.BorderSizePixel = 0
frame.Parent = gui

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 70)
title.BackgroundColor3 = Color3.fromRGB(170, 0, 0)
title.Text = "EU Red | Rivals"
title.TextColor3 = Color3.new(1,1,1)
title.TextScaled = true
title.Font = Enum.Font.GothamBold
title.Parent = frame

-- Buttons
local function createBtn(text, posY, callback)
    local btn = Instance.new("TextButton")
    btn.Size = UDim2.new(0.85, 0, 0, 60)
    btn.Position = UDim2.new(0.075, 0, posY, 0)
    btn.BackgroundColor3 = Color3.fromRGB(190, 0, 0)
    btn.Text = text
    btn.TextColor3 = Color3.new(1,1,1)
    btn.TextScaled = true
    btn.Font = Enum.Font.GothamSemibold
    btn.Parent = frame
    btn.MouseButton1Click:Connect(callback)
end

createBtn("Toggle Fly", 0.18, function()
    print("🟥 Fly Toggled")
end)

createBtn("Unlock All Skins", 0.32, function()
    print("🟥 Unlock All Activated")
end)

createBtn("Random Skin", 0.46, function()
    print("🟥 Random Skin Applied")
end)

createBtn("Toggle ESP", 0.60, function()
    print("🟥 ESP Toggled")
end)

print("✅ EU Red Loaded Successfully on Delta!")
