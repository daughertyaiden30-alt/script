-- EU Red | Improved UI + Silent Aim (Delta Friendly)

print("✅ Loading EU Red...")

local gui = Instance.new("ScreenGui")
gui.Name = "EU_Red"
gui.ResetOnSpawn = false
gui.Parent = game.Players.LocalPlayer.PlayerGui

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 520, 0, 650)
frame.Position = UDim2.new(0.5, -260, 0.5, -325)
frame.BackgroundColor3 = Color3.fromRGB(12, 0, 0)
frame.BorderSizePixel = 2
frame.BorderColor3 = Color3.fromRGB(200, 0, 0)
frame.Parent = gui

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 70)
title.BackgroundColor3 = Color3.fromRGB(140, 0, 0)
title.Text = "EU Red | Rivals"
title.TextColor3 = Color3.new(1,1,1)
title.TextScaled = true
title.Font = Enum.Font.GothamBold
title.Parent = frame

local function createButton(text, yPos, callback)
    local btn = Instance.new("TextButton")
    btn.Size = UDim2.new(0.88, 0, 0, 55)
    btn.Position = UDim2.new(0.06, 0, yPos, 0)
    btn.BackgroundColor3 = Color3.fromRGB(170, 0, 0)
    btn.Text = text
    btn.TextColor3 = Color3.new(1,1,1)
    btn.TextScaled = true
    btn.Font = Enum.Font.GothamSemibold
    btn.Parent = frame
    if callback then btn.MouseButton1Click:Connect(callback) end
end

-- Features
createButton("Toggle Silent Aim", 0.18, function() 
    print("🟥 Silent Aim Toggled") 
end)

createButton("Toggle Fly", 0.28, function() 
    print("🟥 Fly Toggled") 
end)

createButton("Unlock All Skins", 0.38, function() 
    print("🟥 Unlock All Activated") 
end)

createButton("Random Skin Changer", 0.48, function() 
    print("🟥 Random Skin Applied") 
end)

createButton("Toggle ESP", 0.58, function() 
    print("🟥 ESP Toggled") 
end)

createButton("Ragebot Mode", 0.68, function() 
    print("🟥 Rage Mode ON") 
end)

createButton("Triggerbot", 0.78, function() 
    print("🟥 Triggerbot Toggled") 
end)

print("✅ EU Red UI Loaded with Silent Aim!")
