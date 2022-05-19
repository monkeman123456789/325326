local funnyTable
for i,v in next, getgc(true) do 
if typeof(v)=="table" and table.find(v,"ABSURD") then
funnyTable = v
end
end

funnyTable[1] = "Ketone On Top!"
funnyTable[2] = "NotOreoz On Top!"
funnyTable[3] = "Colb Likes minors"
funnyTable[4] = "De Pride devs = monke"
funnyTable[5] = "e261 is cool"
funnyTable[6] = "V3rm is sexy"
funnyTable[7] = "/e Dance"
funnyTable[8] = "Vouch!"
funnyTable[9] = "Like"
funnyTable[10] = "Rep"
funnyTable[11] = "Bump"
funnyTable[12] = "L + Ratio"
funnyTable[13] = "Ketone#2640"
funnyTable[14] = "DM me on discord! Ketone#2640"
funnyTable[15] = "5000 alts later.."
funnyTable[16] = "Emo Bitches >"
funnyTable[17] = "De Pride Devs <"
funnyTable[18] = "How you die like that?"
funnyTable[19] = "Running out of ideas"
funnyTable[20] = "😘"
funnyTable[21] = "Join my discord!"
funnyTable[22] = "Bro dies while cheating 😹"
funnyTable[23] = "De pride = poopie"
funnyTable[24] = "NurseDads = 0"
funnyTable[25] = "Ketone on V3rm!"
funnyTable[26] = "Hope you are having fun!"
funnyTable[27] = "Remotes >"
funnyTable[28] = "Monkeys 🐒"

loadstring(game:HttpGet("https://pastebin.com/raw/tUUGAeaH", true))()

    spoof(game.Players.LocalPlayer.Character.Humanoid, "WalkSpeed", 16)
game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = 16

    spoof(game.Players.LocalPlayer.Character.Humanoid, "JumpPower", 35)
game:GetService("Players").LocalPlayer.Character.Humanoid.JumpPower = 35

local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "~De Pride Isle Sanatorium~", HidePremium = true, SaveConfig = false, ConfigFolder = "OrionTest"})

function player()
    local monke = {}
for _, Player in next, game.Players:GetChildren() do
if Player.Rank.Value >=50 then 
    table.insert(monke, Player.Name)
    else
       table.insert(monke, Player.Name) 
end
end
return monke
end

OrionLib:MakeNotification({
    Name = "Ketone",
    Content = "Thanks for using my script make sure to vouch!",
    Image = "rbxassetid://6833114846",
    Time = 5
})
 
local Tab = Window:MakeTab({
    Name = "LocalPlayer",
    Icon = "rbxassetid://80985",
    PremiumOnly = false
})
 
Tab:AddButton({
    Name = "No Blur",
    Callback = function()
for i,v in next, game.Lighting:GetDescendants() do
   if v:IsA('BlurEffect') or v.Name == "PanicBlur" then
       while wait() do
    v.Size = 0
   end
 end
end
for i,v in next, game.Lighting:GetDescendants() do
   if v.Name == "PanicColor"then
       while wait() do
    v.Brightness = 0
    v.Contrast = 0
    v.Saturation = 0
   end
 end
end

for i,v in next, game.Lighting:GetDescendants() do
   if v.Name == "PanicBlur" then
       while wait() do
    v.Size = 0
   end
   end
end

    end    
})
 
Tab:AddButton({
    Name = "No Ragdoll",
    Callback = function()
                OrionLib:MakeNotification({
    Name = "Ragdoll",
    Content = "Note, this will NOT work against the holy stick due to it being a SS remote on the staffs side not ours.",
    Image = "rbxassetid://6833114846",
    Time = 10
})
for i,v in next, game.Workspace[game.Players.LocalPlayer.Name]:GetDescendants() do
   if v:IsA('Folder') and v.Name == "Ragdoll" then
       v.Parent = game.Players.LocalPlayer.PlayerGui
       wait()
       v:Destroy()
   end
end

        local mt = getrawmetatable(game)
setreadonly(mt,false)
 
local old = mt.__namecall
 
mt.__namecall = function(...)
    local method= getnamecallmethod() or get_namecall_method()
    local args = {...}
    if method == "FireServer" and args[2] == "Ragdoll" then
          return nil
    end
    return old(...)
end
end
})
 
Tab:AddButton({
    Name = "No Fall Damage",
    Callback = function()
        local mt = getrawmetatable(game)
setreadonly(mt,false)
 
local old = mt.__namecall
 
mt.__namecall = function(...)
    local method= getnamecallmethod() or get_namecall_method()
    local args = {...}
    if method == "FireServer" and args[2] == "FallDamage2" then
          return nil
    end
    return old(...)
end
    end    
})
 
Tab:AddButton({
    Name = "Reset",
    Callback = function()
        local player = game:getService("Players").LocalPlayer
local lastPosition = player.Character.PrimaryPart.Position
player.Character:BreakJoints()
Player.CharacterAdded:connect(function(char)
if (lastPosition ~= nil) then
char:moveTo(lastPosition)
lastPosition = nil
end
end)
    end    
})
 
local Tab = Window:MakeTab({
    Name = "Movement",
    Icon = "rbxassetid://4799",
    PremiumOnly = false
})
 
Tab:AddButton({
    Name = "Noclip Fly",
    Callback = function()
                OrionLib:MakeNotification({
    Name = "Fly",
    Content = "(E) to toggle flight \nAlso Works as Noclip",
    Image = "rbxassetid://6833114846",
    Time = 5
})
        loadstring(game:HttpGet("https://raw.githubusercontent.com/LegitH3x0R/Roblox-Scripts/main/AEBypassing/CFrameFly.lua"))()
    end    
})
 
Tab:AddButton({
    Name = "No Stamina",
    Callback = function()
        local mt = getrawmetatable(game)
setreadonly(mt,false)
 
local old = mt.__namecall
 
mt.__namecall = function(...)
    local method= getnamecallmethod() or get_namecall_method()
    local args = {...}
    if method == "FireServer" and args[2] == "Vagour2" then
          return nil
    end
    return old(...)
end
 
    end    
})
 
Tab:AddButton({
    Name = "Inf Jump",
    Callback = function()
        while wait() do
        local Player = game:GetService'Players'.LocalPlayer;
local UIS = game:GetService'UserInputService';
 
_G.JumpHeight = game.Players.LocalPlayer.Character.Humanoid.JumpPower;
 
function Action(Object, Function) if Object ~= nil then Function(Object); end end
 
UIS.InputBegan:connect(function(UserInput)
    if UserInput.UserInputType == Enum.UserInputType.Keyboard and UserInput.KeyCode == Enum.KeyCode.Space then
        Action(Player.Character.Humanoid, function(self)
            if self:GetState() == Enum.HumanoidStateType.Jumping or self:GetState() == Enum.HumanoidStateType.Freefall then
                Action(self.Parent.HumanoidRootPart, function(self)
                    self.Velocity = Vector3.new(0, _G.JumpHeight, 0);
                end)
            end
        end)
    end
end)
        end    
  end
})

Tab:AddSlider({
    Name = "Walkspeed",
    Min = 16,
    Max = 200,
    Default = 16,
    Increment = 5,
    ValueName = "bananas",
    Callback = function(Value)
        spoof(game.Players.LocalPlayer.Character.Humanoid, "WalkSpeed", 16)
       game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = (Value)
    end    
})
 
Tab:AddSlider({
    Name = "JumpPower",
    Min = 35,
    Max = 200,
    Default = 35,
    Increment = 5,
    ValueName = "spinach",
    Callback = function(Value)
        spoof(game.Players.LocalPlayer.Character.Humanoid, "JumpPower", 35)
       game:GetService("Players").LocalPlayer.Character.Humanoid.JumpPower = (Value)
    end    
})
 
local Tab = Window:MakeTab({
    Name = "Players",
    Icon = "rbxassetid://7268",
    PremiumOnly = false
})
 
local dropdown = Tab:AddDropdown({
    Name = "Players",
    Default = "1",
    Options = {"1", "2"},
    Callback = function(Values)
        Valuess = Values
    end    
})
dropdown:Refresh(player{}, true)

Tab:AddButton({
    Name = "Go to Player",
    Callback = function()
          game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Valuess].Character.HumanoidRootPart.CFrame
      end    
})

Tab:AddButton({
    Name = "Give Cockroach",
    Callback = function()
      Cock = false
        for _,x in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
            if string.find(x.Name, "Cock") then
                Cock = true 
            end
        end
        for _,x in pairs(game.Workspace[game.Players.LocalPlayer.Name]:GetChildren()) do 
            if string.find(x.Name, "Cock") then
                Cock = true 
            end
        end
        if Cock == false then
        for _,v in pairs(game.Workspace.Givers:GetChildren()) do
        if v.Name == "Cockroach" then
            if v.Cockroach.Transparency == 0 then
            OldPos = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Cockroach.CFrame
            wait(1)
            fireclickdetector(v.Cockroach.ClickDetector)
            wait(0.5)
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = OldPos
            break
            end
        end
        end
        end

for i=1, 50 do

game.Players[Valuess].Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame

local args = {
    [1] = "GiveTool",
    [2] = game:GetService("Players")[Valuess],
    [3] = game:GetService("Players").LocalPlayer.Character.Cockroach
}

game:GetService("ReplicatedStorage").Events.Game:FireServer(unpack(args))
     
     end
end
})
 
local Tab = Window:MakeTab({
    Name = "Misc",
    Icon = "rbxassetid://44898",
    PremiumOnly = false
})

local CoolLabel = Tab:AddLabel("Time")

Tab:AddToggle({
Name = "Rain Toggle",
	Default = false,
	Callback = function(Value)
		game:GetService("ReplicatedStorage").Server.Rain.Value = Value
	end    
}) 

loadstring(game:HttpGet("https://pastebin.com/raw/06iG6YkU", true))()

Tab:AddToggle({
	Name = "Fullbright Toggle",
	Default = false,
	Callback = function(Value)
		loadstring(game:HttpGet("https://pastebin.com/raw/06iG6YkU", true))()
	end    
}) 

Tab:AddToggle({Name = "Monster",
Default = false,
Callback = function(Value) 
    if Value == true then 
        game.Players.LocalPlayer.Rank.XLevel.Value = 16669
    else
        game.Players.LocalPlayer.Rank.XLevel.Value = 0
    end
end}) 

Tab:AddToggle({Name = "Spider",
Default = false,
Callback = function(Value) 
    if Value == true then 
        game.Players.LocalPlayer.Rank.XLevel.Value = 16669
        game.Players.LocalPlayer.Transformed.TransformationLevel.Value = 3
    else
        game.Players.LocalPlayer.Rank.XLevel.Value = 0
        game.Players.LocalPlayer.Transformed.TransformationLevel.Value = 1
    end
end}) 

Tab:AddButton({
    Name = "No Barriers",
    Callback = function()
        for i,v in next, game:GetService("Workspace"):GetChildren() do
            if v:IsA('Folder') and v.Name == "RankBarriers" then
            v.Parent = StarterGui
            end
        end
    end    
})

Tab:AddButton({
    Name = "No Hunger",
    Callback = function()
local Anticheat = game:GetService("Players").LocalPlayer.Voracity
local GameMt = getrawmetatable(game)
local OldIndex = GameMt.__index
 
setreadonly(GameMt, false)
 
GameMt.__index = newcclosure(function(Self, Key)
   if not checkcaller() and Self == Anticheat and Key == "Value" then
       return math.huge
   end
 
   return OldIndex(Self, Key)
end)
 
setreadonly(GameMt, true)

        local mt = getrawmetatable(game)
setreadonly(mt,false)
 
local old = mt.__namecall
 
mt.__namecall = function(...)
    local method= getnamecallmethod() or get_namecall_method()
    local args = {...}
    if method == "FireServer" and args[2] == "Voracity2" then
          return nil
    end
    return old(...)
end

end  
})

Tab:AddButton({
    Name = "Get Cockroach",
    Callback = function()
        Cock = false
        for _,x in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
            if string.find(x.Name, "Cock") then
                Cock = true 
            end
        end
        for _,x in pairs(game.Workspace[game.Players.LocalPlayer.Name]:GetChildren()) do 
            if string.find(x.Name, "Cock") then
                Cock = true 
            end
        end
        if Cock == false then
        for _,v in pairs(game.Workspace.Givers:GetChildren()) do
        if v.Name == "Cockroach" then
            if v.Cockroach.Transparency == 0 then
            OldPos = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Cockroach.CFrame
            wait(1)
            fireclickdetector(v.Cockroach.ClickDetector)
            wait(0.5)
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = OldPos
            break
            end
        end
        end
        end
    end    
})
 
Tab:AddButton({
    Name = "ChatLogs",
    Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/Y8yW6Nas", true))()
    end    
})

local Tab = Window:MakeTab({
    Name = "Credits",
    Icon = "rbxassetid://44898",
    PremiumOnly = false
})
 
Tab:AddLabel("Developer: Ketone")
Tab:AddLabel("Developer: NotOreoz")

Tab:AddButton({
	Name = "Copy Discord",
	Callback = function()
	    OrionLib:MakeNotification({
	Name = "Discord",
	Content = "Discord copied to clipboard",
	Image = "rbxassetid://4483345998",
	Time = 5
})
      		Synapse:CopyString([[
https://discord.gg/KJA9CKJV5C
]])()
  	end    
})

spawn(function()
    while wait() do 
        CoolLabel:Set("Time: "..game.Lighting.TimeOfDay)
    end
end)

OrionLib:Init()
