local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Robojini/Tuturial_UI_Library/main/UI_Template_1"))()

local Window = Library.CreateLib("TridentChack", "RJTheme5")

local Tab = Window:NewTab("AimBot")

local Section = Tab:NewSection("Aim")

Section:NewButton("AimBot", "Aim bot legit", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Exunys/Aimbot-V3/main/src/Aimbot.lua"))()
ExunysDeveloperAimbot()
end)

local Tab = Window:NewTab("Esp")

local Section = Tab:NewSection("ESP")

Section:NewToggle("Esp", "ToggleInfo", function(state)
    if state then
        while wait(0.5) do
    for i, childrik in ipairs(workspace:GetDescendants()) do
        if childrik:FindFirstChild("Humanoid") then
            if not childrik:FindFirstChild("EspBox") then
                if childrik ~= game.Players.LocalPlayer.Character then
                    local esp = Instance.new("BoxHandleAdornment",childrik)
                    esp.Adornee = childrik
                    esp.ZIndex = 0
                    esp.Size = Vector3.new(4, 5, 1)
                    esp.Transparency = 0.60
                    esp.Color3 = Color3.fromRGB(52,12,12)
                    esp.AlwaysOnTop = true
                    esp.Name = "EspBox"
                end
            end
        end
    end
end
    else
        EspBox:Destroy()
		esp:Destroy()
    end
end)
