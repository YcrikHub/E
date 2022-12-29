local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Admin Players Hub", "DarkTheme")
local Tab = Window:NewTab("Player")
local Section = Tab:NewSection("Select Player!")
Plr = {}
for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(Plr,v.Name) 
end
local drop = Section:NewDropdown("Select Player!", "Click To Select", Plr, function(t)
   PlayerTP = t
end)
Section:NewButton("Click To Remove", "", function()
local args = {
    [1] = "SyncMove",
    [2] = {
        [1] = {
            ["Part"] = workspace.RankRemoverPads.Model.TouchPart,
            ["CFrame"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
        }
    }
}

game:GetService("Players").LocalPlayer.Character:FindFirstChild("Building Tools").SyncAPI.ServerEndpoint:InvokeServer(unpack(args))
end)
Section:NewButton("Click To Give", "", function()
local args = {
    [1] = "SyncMove",
    [2] = {
        [1] = {
            ["Part"] = workspace.RankGiverPads.Model.TouchPart,
            ["CFrame"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
        }
    }
}

game:GetService("Players").LocalPlayer.Character:FindFirstChild("Building Tools").SyncAPI.ServerEndpoint:InvokeServer(unpack(args))
end)

Section:NewButton("Refresh Dropdown","Refresh Dropdown", function()
  drop:Refresh(Plr)
end)
