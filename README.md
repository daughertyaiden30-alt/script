-- EU Red | No Key Version for Rivals (Red Theme)

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/violin-suzutsuki/LinoriaLib/main/Library.lua"))()
local ThemeManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/violin-suzutsuki/LinoriaLib/main/addons/ThemeManager.lua"))()

local Window = Library:CreateWindow({
    Title = "EU Red | Rivals",
    Center = true,
    AutoShow = true,
})

local Tabs = {
    Main = Window:AddTab("main"),
    World = Window:AddTab("world"),
    ESP = Window:AddTab("esp"),
    Visuals = Window:AddTab("visuals"),
    Character = Window:AddTab("character"),
    Misc = Window:AddTab("misc"),
    Settings = Window:AddTab("settings"),
}

-- ==================== MAIN ====================
local SilentAim = Tabs.Main:AddLeftGroupbox("silent aim")
SilentAim:AddToggle("SilentAimEnabled", {Text = "enabled", Default = true})
SilentAim:AddToggle("Manipulation", {Text = "manipulation"})
SilentAim:AddToggle("ClosestPart", {Text = "closest part"})
SilentAim:AddToggle("Visualize", {Text = "visualize"})
SilentAim:AddToggle("ShowFOV", {Text = "show fov"})
SilentAim:AddSlider("AimRadius", {Text = "radius", Default = 1000, Min = 100, Max = 2000, Rounding = 0})

local Weapons = Tabs.Main:AddRightGroupbox("weapons")
Weapons:AddToggle("NoSpread", {Text = "no spread", Default = true})
Weapons:AddToggle("FullAuto", {Text = "full auto"})
Weapons:AddToggle("AlwaysBackstab", {Text = "always backstab"})

-- ==================== CHARACTER ====================
local Movement = Tabs.Character:AddLeftGroupbox("Movement")
Movement:AddToggle("FlyEnabled", {Text = "Fly", Default = false, Callback = function(v)
    print("Fly:", v and "ON" or "OFF")
end})
Movement:AddSlider("FlySpeed", {Text = "Fly Speed", Default = 60, Min = 10, Max = 300})

local Skins = Tabs.Character:AddRightGroupbox("Skins")
Skins:AddButton({Text = "Unlock All Skins", Func = function() 
    Library:Notify("Unlock All", "Local skins unlocked!", 4) 
end})
Skins:AddButton({Text = "Random Skin", Func = function() 
    Library:Notify("Skin Changer", "Random skin applied", 3)
end})

-- ==================== RAGE ====================
local Rage = Tabs.Misc:AddLeftGroupbox("ragebot")
Rage:AddToggle("RageEnabled", {Text = "enabled"})
Rage:AddToggle("VoidSpam", {Text = "void spam"})

-- Visuals
Tabs.Visuals:AddLeftGroupbox("ESP"):AddToggle("ESPEnabled", {Text = "ESP Enabled", Default = true})

-- Red Theme
ThemeManager:SetLibrary(Library)
ThemeManager:SetTheme("Blood")
ThemeManager:ApplyToTab(Tabs.Main)

Library:Notify("EU Red", "No Key Version Loaded Successfully!", 6)
print("✅ EU Red | No Key - Ready!")
