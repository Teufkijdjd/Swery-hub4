_G.Hom = 150
TweeSpeed = 350
TP = function(Point)
local LocalPlayer = game.Players.LocalPlayer 
	repeat wait()
		TweenPlay = (Point.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if LocalPlayer.Character.Humanoid.Sit == true then 
			LocalPlayer.Character.Humanoid.Sit = false 
		end
		pcall(function() 
			tot = game:GetService("TweenService"):Create(LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(TweenPlay/TweeSpeed, Enum.EasingStyle.Linear),{CFrame = Point})
		end)
		tot:Play()
		if TweenPlay <= _G.Hom then
			tot:Cancel()
			LocalPlayer.Character.HumanoidRootPart.CFrame = Point
		end
		if _G.StopTween == true then
			tot:Cancel()
			_G.Clip = false
		end
		if not game:GetService("Workspace"):FindFirstChild("Part") then
			local Part = Instance.new("Part")
                Part.Name = "Part"
                Part.Parent = game.Workspace
                Part.Anchored = true
                Part.Transparency = 1
                Part.Size = Vector3.new(40, 0.5, 40)
            elseif game:GetService("Workspace"):FindFirstChild("Part") then
                game.Workspace["Part"].CFrame = CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
			else
           	 game:GetService("Workspace"):FindFirstChild("Part"):Destroy()
        	end
	until TweenPlay <= _G.Hom
end

function _G.StopTween(target)
    if not TP then
       _G.StopTween = true
       wait()
             TP(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
       wait()
        if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
           game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
        end
        _G.StopTween = false
        _G.Clip = false
    end
end

function TPPlayer(Pos)
	repeat wait()
		Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end
		pcall(function() tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/200, Enum.EasingStyle.Linear),{CFrame = Pos}) end)
		tween:Play()
		if Distance <= 350 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
		end
		if Distance >= 1200 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.Head:Destroy()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			wait(1)
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
		end
		if _G.StopTween == true then
			tween:Cancel()
			_G.Clip = false
		end
	until Distance <= 3000
end
-- tween 1
_G.Hom = 150
TweeSpeed = 350
topos = function(Point)
local LocalPlayer = game.Players.LocalPlayer 
	repeat wait()
		TweenPlay = (Point.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if LocalPlayer.Character.Humanoid.Sit == true then 
			LocalPlayer.Character.Humanoid.Sit = false 
		end
		pcall(function() 
			tot = game:GetService("TweenService"):Create(LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(TweenPlay/TweeSpeed, Enum.EasingStyle.Linear),{CFrame = Point})
		end)
		tot:Play()
		if TweenPlay <= _G.Hom then
			tot:Cancel()
			LocalPlayer.Character.HumanoidRootPart.CFrame = Point
		end
		if _G.StopTween == true then
			tot:Cancel()
			_G.Clip = false
		end
		if not game:GetService("Workspace"):FindFirstChild("Part") then
			local Part = Instance.new("Part")
                Part.Name = "Part"
                Part.Parent = game.Workspace
                Part.Anchored = true
                Part.Transparency = 1
                Part.Size = Vector3.new(40, 0.5, 40)
            elseif game:GetService("Workspace"):FindFirstChild("Part") then
                game.Workspace["Part"].CFrame = CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
			else
           	 game:GetService("Workspace"):FindFirstChild("Part"):Destroy()
        	end
	until TweenPlay <= _G.Hom
end

function _G.StopTween(target)
    if not topos then
       _G.StopTween = true
       wait()
             topos(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
       wait()
        if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
           game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
        end
        _G.StopTween = false
        _G.Clip = false
    end
end

function TPPlayer(Pos)
	repeat wait()
		Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
		if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end
		pcall(function() tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/200, Enum.EasingStyle.Linear),{CFrame = Pos}) end)
		tween:Play()
		if Distance <= 350 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
		end
		if Distance >= 1200 then
			tween:Cancel()
			game.Players.LocalPlayer.Character.Head:Destroy()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			wait(1)
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
		end
		if _G.StopTween == true then
			tween:Cancel()
			_G.Clip = false
		end
	until Distance <= 3000
end

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/lime"))()

local w = Library:Window("Swery hub")

w:Button("นั่งเรือก่อนกดเปิดออโต้รันหาเกาะลับ", function(v)
 end) 
 
 w:Button("หยุดการ ทวีน รอ การวาป",function()
  topos(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
  _G.Clip = false
TP(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
_G.Clip = false
  end)
 
 w:Toggle("ออโต้หาเกาะลับ",function(v)
Farm = v
while Farm do wait()
game:GetService("VirtualInputManager"):SendKeyEvent(true,"W",false,game)
end
 end)

w:Toggle("ออโต้หาเกาะลับ [ย้ายเชิฟ]",function(value)
  _G.MirageHop = value
if game:GetService("Workspace").Map:FindFirstChild("MysticIsland") then
                           topos(game:GetService("Workspace").Map:FindFirstChild("MysticIsland").HumanoidRootPart.CFrame * CFrame.new(0,500,-100))
                    else
if _G.MirageHop then
hop()
end
end
  end)
  
w:Toggle("วาปไปหาเกียร์",function(value)
  TP(game:GetService("Workspace").Map.MysticIsland:FindFirstChildOfClass("MeshPart").CFrame)
  
end)

 w:Button("วาปไปที่ทำเผ่า",function(v)
 
 end)
 
 w:Button("วาปไปห้องทำเผ่าวี",function()
  Game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(28286.35546875, 14895.3017578125, 102.62469482421875)
    end)
    
w:Button("เทเลพอร์ตไปที่คันโยกดึง",function()
  topos(CFrame.new(28575.181640625, 14936.6279296875, 72.31636810302734))
end)

w:Button("เทเลพอร์ตไปยัง Ancient One (ต้องอยู่ใน Temple of Time!) กดที่นี่เพื่อวาป",function()
  topos(CFrame.new(28981.552734375, 14888.4267578125, -120.245849609375))
end) 

w:Toggle("เอมบอท1", function(v)
local player = game.Players.LocalPlayer
local character = player.Character 
local localroot = character.HumanoidRootPart
local Camera = workspace.CurrentCamera

local function closestPlayer()
    local target = nil
    local range = math.huge
    for _, v in pairs(game.Players:GetPlayers()) do
        if v ~= player and v.Character the
            local JN = v.Character:FindFirstChild("HumanoidRootPart")
            if JN then
                local distance = (localroot.Position - JN.Position).magnitude
                if distance < range then
                    range = distance
                    target = v
                end
            end
        end
    end
    return target
end

local aimbot = true

spawn(function()
    while aimbot do
        local Enemy = closestPlayer()
        if Enemy and Enemy.Character then
            local EnemyV = Enemy.Character:FindFirstChild("HumanoidRootPart")
            local EnemyK = Enemy.Character:FindFirstChild("Humanoid")
            if EnemyV and EnemyK and EnemyK.Health > 0 then
                Camera.CFrame = CFrame.new(Camera.CFrame.Position, EnemyV.Position)
            end
        end
        game:GetService("RunService").Heartbeat:Wait()
    end
end)

w:Toggle("เอมบอท2", function(v)
local player = game.Players.LocalPlayer
local character = player.Character
local localroot = character.HumanoidRootPart
local UIS = game:GetService("UserInputService")
local Camera = workspace.CurrentCamera

local function closestPlayer()
    local target = nil
    local range = math.huge
    for _, v in pairs(game.Players:GetPlayers()) do
        if v ~= player and v.Character then
            local JN = v.Character:FindFirstChild("HumanoidRootPart")
            if JN then
                local distance = (localroot.Position - JN.Position).magnitude
                if distance < range then
                    range = distance
                    target = v
                end
            end
        end
    end
    return target
end

local aimbot = false

UIS.InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.P then
        aimbot = not aimbot
        if aimbot then
            spawn(function()
                while aimbot == true d
                    if aimbot ~= true then return end
                    local Enemy = closestPlayer()
                    if Enemy and Enemy.Character then
                        local EnemyV = Enemy.Character:FindFirstChild("HumanoidRootPart")
                        local EnemyK = Enemy.Character:FindFirstChild("Humanoid")
                        if EnemyV and EnemyK and EnemyK.Health > 0 then
                            Camera.CFrame = CFrame.new(Camera.CFrame.Position, EnemyV.Position)
                        end
                    end
                    game:GetService("RunService").Heartbeat:Wait()
                end
            end)
        end
    elseif input.KeyCode == Enum.KeyCode.K then
        aimbot = false
    end
end)

w:Toggle("Esp", function(v)
local plr = game:GetService("Players").LocalPlayer
local Notification = require(game:GetService("ReplicatedStorage").Notification)
local Data = plr:WaitForChild("Data")
local EXPFunction = require(game.ReplicatedStorage:WaitForChild("EXPFunction"))
local LevelUp = require(game:GetService("ReplicatedStorage").Effect.Container.LevelUp)
local Sound = require(game:GetService("ReplicatedStorage").Util.Sound)
local LevelUpSound = game:GetService("ReplicatedStorage").Util.Sound.Storage.Other:FindFirstChild("LevelUp_Proxy") or game:GetService("ReplicatedStorage").Util.Sound.Storage.Other:FindFirstChild("LevelUp")
function v129(p15)
    local v130 = p15;
    while true do
        local v131, v132 = string.gsub(v130, "^(-?%d+)(%d%d%d)", "%1,%2");
        v130 = v131;
        if v132 == 0 then
            break;
        end;    
    end;
    return v130;
end;

Notification.new("<Color=White>Swery Hub<Color=/>"):Display()
Notification.new("<Color=blue>Thank you for using this script.<Color=/>"):Display()

_G.Color = Color3.fromRGB(0, 0, 255) -- Color UI
_G.Logo = 13990972098 -- ID Logo Your Hub

local normal = loadstring(game:HttpGet(('https://raw.githubusercontent.com/Lucifer4381/ui-normal-hub/main/scr')))()

local Win = library:Evil("Swery","Hub",_G.Logo )

local Tab = Win:CraftTab('Main') -- Name

local Page = Tab:CraftPage('Main',1) -- Name,1 or 2

Page:Toggle('Aim bot1',nil,function(a) -- Toggle,Def,callback
local player = game.Players.LocalPlayer
local character = player.Character
local localroot = character.HumanoidRootPart
local UIS = game:GetService("UserInputService")
local Camera = workspace.CurrentCamera

local function closestPlayer()
    local target = nil
    local range = math.huge
    for _, v in pairs(game.Players:GetPlayers()) do
        if v ~= player and v.Character then
            local JN = v.Character:FindFirstChild("HumanoidRootPart")
            if JN then
                local distance = (localroot.Position - JN.Position).magnitude
                if distance < range then
                    range = distance
                    target = v
                end
            end
        end
    end
    return target
end

local aimbot = false

UIS.InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.P then
        aimbot = not aimbot
        if aimbot then
            spawn(function()
                while aimbot == true d
                    if aimbot ~= true then return end
                    local Enemy = closestPlayer()
                    if Enemy and Enemy.Character then
                        local EnemyV = Enemy.Character:FindFirstChild("HumanoidRootPart")
                        local EnemyK = Enemy.Character:FindFirstChild("Humanoid")
                        if EnemyV and EnemyK and EnemyK.Health > 0 then
                            Camera.CFrame = CFrame.new(Camera.CFrame.Position, EnemyV.Position)
                        end
                    end
                    game:GetService("RunService").Heartbeat:Wait()
                end
            end)
        end
    elseif input.KeyCode == Enum.KeyCode.K then
        aimbot = false
    end
end)
    print(a)
end)

Page:Toggle('Aim bot2',nil,function(a) -- Toggle,Def,callback
local player = game.Players.LocalPlayer
local character = player.Character
local localroot = character.HumanoidRootPart
local UIS = game:GetService("UserInputService")
local Camera = workspace.CurrentCamera

local function closestPlayer()
    local target = nil
    local range = math.huge
    for _, v in pairs(game.Players:GetPlayers()) do
        if v ~= player and v.Character then
            local JN = v.Character:FindFirstChild("HumanoidRootPart")
            if JN then
                local distance = (localroot.Position - JN.Position).magnitude
                if distance < range then
                    range = distance
                    target = v
                end
            end
        end
    end
    return target
end

local aimbot = false

UIS.InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.P then
        aimbot = not aimbot
        if aimbot then
            spawn(function()
                while aimbot == true d
                    if aimbot ~= true then return end
                    local Enemy = closestPlayer()
                    if Enemy and Enemy.Character then
                        local EnemyV = Enemy.Character:FindFirstChild("HumanoidRootPart")
                        local EnemyK = Enemy.Character:FindFirstChild("Humanoid")
                        if EnemyV and EnemyK and EnemyK.Health > 0 then
                            Camera.CFrame = CFrame.new(Camera.CFrame.Position, EnemyV.Position)
                        end
                    end
                    game:GetService("RunService").Heartbeat:Wait()
                end
            end)
        end
    elseif input.KeyCode == Enum.KeyCode.K then
        aimbot = false
    end
end)
    print(a)
end)

Page:Toggle('Esp',nil,function(a) -- Toggle,Def,callback
while wait() do
     pcall(function()
       for i,v in pairs(game.Players:GetChildren()) do
            if not v.Character.Head:FindFirstChild("ESP") then
                local BillboardGui = Instance.new("BillboardGui")
                local TextLabel = Instance.new("TextLabel")
                BillboardGui.Parent = v.Character.Head
                BillboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
                BillboardGui.Active = true
                BillboardGui.Name = "ESP"
                BillboardGui.AlwaysOnTop = true
                BillboardGui.LightInfluence = 1.000
                BillboardGui.Size = UDim2.new(0, 200, 0, 50)
                BillboardGui.StudsOffset = Vector3.new(0, 2.5, 0)
                TextLabel.Parent = BillboardGui
                TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                TextLabel.BackgroundTransparency = 1.000
                TextLabel.Size = UDim2.new(0, 200, 0, 50)
                TextLabel.Font = Enum.Font.GothamBold
                TextLabel.Text = v.Name
                TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
                TextLabel.TextScaled = true
                TextLabel.TextSize = 14.000
                TextLabel.TextStrokeTransparency = 0.000
                TextLabel.TextWrapped = true
            end
        end
    end) 
end
    print(v)
