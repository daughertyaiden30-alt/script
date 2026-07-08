-- EU Red | No Key | Cross Platform (Windows / Android / iOS)

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/violin-suzutsuki/LinoriaLib/main/Library.lua"))()
local ThemeManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/violin-suzutsuki/LinoriaLib/main/addons/ThemeManager.lua"))()

local Window = Library:CreateWindow({
    Title = "EU Red | Rivals",
    Center = true,
    AutoShow = true,
    Size = UDim2.fromOffset(680, 520),
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
Movement:AddToggle("FlyEnabled", {Text = "Fly", Default = false})
Movement:AddSlider("FlySpeed", {Text = "Fly Speed", Default = 60, Min = 10, Max = 300})

local Skins = Tabs.Character:AddRightGroupbox("Skins")
Skins:AddButton({Text = "Unlock All Skins", Func = function() 
    Library:Notify("Unlock All", "
