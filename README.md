print("Turtle Egg Screct - you stupid nigger - Don't Tell Anyone")
wait(0)
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Rank Controller [ HEHEHEHA ]", "Ocean")
local Tab = Window:NewTab("Player")
local Section = Tab:NewSection("Select Player!")
Plr = {}
for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(Plr,v.Name) 
end
local drop = Section:NewDropdown("Select Player!", "Click To Select", Plr, function(t)
   PlayerTP = t
end)
Section:NewButton("Click To Give", "", function()
local toolName = "Building Tools"

local player = game.Players.LocalPlayer
local backpack = player.Backpack
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

local tool = backpack:FindFirstChild(toolName) or character:FindFirstChild(toolName)

if tool then
    humanoid:EquipTool(tool)
else
    -- Create the message object
local message = Instance.new("Message")
message.Text = "YOU DON'T HAVE BUILDING TOOLS NIGGA GO FIND BUILDING TO OR ASK YOUR MOMMY FOR BUIILDING TOOLS"
message.Parent = game.Workspace

-- Wait for 3 seconds
wait(5)

-- Destroy the message object
message:Destroy()
end
wait(0)
local args = {
    [1] = "SyncMove",
    [2] = {
        [1] = {
            ["Part"] = workspace.RankGiverPads.Model.BlackCircle,
            ["CFrame"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
        },
        [2] = {
            ["Part"] = workspace.RankGiverPads.Model.TouchPart,
            ["CFrame"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
        },
        [3] = {
            ["Part"] = workspace.RankGiverPads.Model.BlueCircle,
            ["CFrame"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
        },
        [4] = {
            ["Pivot"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame,
            ["Model"] = workspace.RankGiverPads.Model
        }
    }
}

game:GetService("Players").LocalPlayer.Character:FindFirstChild("Building Tools").SyncAPI.ServerEndpoint:InvokeServer(unpack(args))
wait(0)
local args = {
    [1] = "SyncMove",
    [2] = {
        [1] = {
            ["Part"] = workspace.RankGiverPads.Model.BlackCircle,
            ["CFrame"] = CFrame.new(0, -1000000, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
        },
        [2] = {
            ["Part"] = workspace.RankGiverPads.Model.TouchPart,
            ["CFrame"] = CFrame.new(0, -1000000, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
        },
        [3] = {
            ["Part"] = workspace.RankGiverPads.Model.BlueCircle,
            ["CFrame"] = CFrame.new(0, -1000000, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
        },
        [4] = {
            ["Pivot"] = CFrame.new(0, -1000000, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),
            ["Model"] = workspace.RankGiverPads.Model
        }
    }
}

game:GetService("Players").LocalPlayer.Character:FindFirstChild("Building Tools").SyncAPI.ServerEndpoint:InvokeServer(unpack(args))
end)
Section:NewButton("Click To Remove", "", function()
local toolName = "Building Tools"

local player = game.Players.LocalPlayer
local backpack = player.Backpack
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

local tool = backpack:FindFirstChild(toolName) or character:FindFirstChild(toolName)

if tool then
    humanoid:EquipTool(tool)
else
    -- Create the message object
local message = Instance.new("Message")
message.Text = "YOU DON'T HAVE BUILDING TOOLS NIGGA GO FIND BUILDING TO OR ASK YOUR MOMMY FOR BUIILDING TOOLS"
message.Parent = game.Workspace

-- Wait for 3 seconds
wait(5)

-- Destroy the message object
message:Destroy()
end
wait(0)
local args = {
    [1] = "SyncMove",
    [2] = {
        [1] = {
            ["Part"] = workspace.RankRemoverPads.Model.BlackCircle,
            ["CFrame"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
        },
        [2] = {
            ["Part"] = workspace.RankRemoverPads.Model.TouchPart,
            ["CFrame"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
        },
        [3] = {
            ["Part"] = workspace.RankRemoverPads.Model.BlueCircle,
            ["CFrame"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
        },
        [4] = {
            ["Pivot"] = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame,
            ["Model"] = workspace.RankRemoverPads.Model
        }
    }
}

game:GetService("Players").LocalPlayer.Character:FindFirstChild("Building Tools").SyncAPI.ServerEndpoint:InvokeServer(unpack(args))
wait(0)
local args = {
    [1] = "SyncMove",
    [2] = {
        [1] = {
            ["Part"] = workspace.RankRemoverPads.Model.BlackCircle,
            ["CFrame"] = CFrame.new(0, -1000000, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
        },
        [2] = {
            ["Part"] = workspace.RankRemoverPads.Model.TouchPart,
            ["CFrame"] = CFrame.new(0, -1000000, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
        },
        [3] = {
            ["Part"] = workspace.RankRemoverPads.Model.BlueCircle,
            ["CFrame"] = CFrame.new(0, -1000000, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1)
        },
        [4] = {
            ["Pivot"] = CFrame.new(0, -1000000, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1),
            ["Model"] = workspace.RankRemoverPads.Model
        }
    }
}

game:GetService("Players").LocalPlayer.Character:FindFirstChild("Building Tools").SyncAPI.ServerEndpoint:InvokeServer(unpack(args))
end)


Section:NewButton("Btools","give btools", function()
local args = {
    [1] = ";btools"
}

game:GetService("ReplicatedStorage").HDAdminClient.Signals.RequestCommand:InvokeServer(unpack(args))
end)
