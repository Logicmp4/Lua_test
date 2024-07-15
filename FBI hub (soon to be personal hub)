local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/ionlyusegithubformcmods/1-Line-Scripts/main/Mobile%20Friendly%20Orion')))()

local Window = OrionLib:MakeWindow({Name = "LOGIC'S FBI PANEL | Client Replication", HidePremium = true, IntroEnabled = false, SaveConfig = false, ConfigFolder = "OrionTest"})

local Tab = Window:MakeTab({
	Name = "Main",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
 Name = "Kill other",
 Callback = function()
        local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

  for _, player in ipairs(Players:GetPlayers()) do
    if player ~= LocalPlayer then
      player.Character.Humanoid.Health = 0
    end
  end
   end    
})

Tab:AddButton({
 Name = "Bring all",
 Callback = function()
        local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

  for _, player in ipairs(Players:GetPlayers()) do
    if player ~= LocalPlayer then
      player.Character.HumanoidRootPart.CFrame = LocalPlayer.Character.HumanoidRootPart.CFrame
    end
  end
   end    
})

Tab:AddButton({
 Name = "Delete all characters",
 Callback = function()
        local Players = game:GetService("Players")
  for _, player in ipairs(Players:GetPlayers()) do
  if player ~= Players.LocalPlayer then
      player.Character:Destroy()
  end
end
   end    
})

Tab:AddDropdown({
	Name = "Freeze all",
	Default = "1",
	Options = {"Freeze", "Unfreeze"},
	Callback = function(Value)
		if Value == "Freeze" then
		local Players = game:GetService("Players")
  for _, player in ipairs(Players:GetPlayers()) do
  if player ~= Players.LocalPlayer then
      player.Character.HumanoidRootPart.Anchored = true
  end
end
		elseif Value == "Unfreeze" then
		local Players = game:GetService("Players")
  for _, player in ipairs(Players:GetPlayers()) do
  if player ~= Players.LocalPlayer then
      player.Character.HumanoidRootPart.Anchored = false
  end
end
		end
	end    
})

Tab:AddToggle({
	Name = "Mute all sounds",
	Default = false,
	Callback = function(Value)
MuteS = Value
 while MuteS do
   task.wait()
for i,v in pairs(game:GetDescendants()) do
        if v:IsA("Sound") then
            v.Playing = false
        end
    end
end
	end    
})

Tab:AddToggle({
	Name = "Auto Load Character",
	Default = false,
	Callback = function(Value)
gytptr = Value
 local Player = game:GetService("Players").LocalPlayer
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local lastPosition = Player.Character.HumanoidRootPart.CFrame

while gytptr do
    wait(0.1)
    if Player.Character:FindFirstChildOfClass("Humanoid") then
        lastPosition = Player.Character.HumanoidRootPart.CFrame
    end
    
    if Player == game:GetService("Players").LocalPlayer then
        if not Player.Character or not Player.Character:FindFirstChildOfClass("Humanoid") then
            ReplicatedStorage.InstantRespawn:FireServer()
            repeat 
                wait() 
            until Player.Character:FindFirstChildOfClass("Humanoid")
            Player.Character.HumanoidRootPart.CFrame = lastPosition
        end
    end
end
	end    
})

Tab:AddToggle({
 Name = "Remove decals and workspace effects",
 Default = false,
 Callback = function(Value)
 guy = Value
        workspace = game:GetService("Workspace")

function deleteAllDecals()
  for _, child in ipairs(workspace:GetDescendants()) do
    if child:IsA("Decal") or child:IsA("ParticleEmitter") or child:IsA("Fire") or child:IsA("Smoke") or child:IsA("Explosion") or child:IsA("Trail") or child:IsA("Sparkles") or child:IsA("Beam") or child:IsA("PointLight") or child:IsA("SpotLight") or child:IsA("SurfaceLight") or child:IsA("SelectionBox") then
      child:Destroy()
    end
  end

for _, child in ipairs(game.Lighting:GetDescendants()) do
    if child:IsA("Sky") then
      child:Destroy()
    end
  end
  
end

while guy do
   task.wait()
deleteAllDecals()
end
   end    
})

Tab:AddToggle({
 Name = "Remove Messages",
 Default = false,
 Callback = function(Value)
 hyur = Value
        workspace = game:GetService("Workspace")

function deleteAllMessages()
  for _, child in ipairs(workspace:GetDescendants()) do
    if child:IsA("Message") or child:IsA("Hint") then
      child:Destroy()
    end
  end
end

while hyur do
   task.wait()
deleteAllMessages()
end
   end    
})

Tab:AddToggle({
	Name = "Remove BillboardsGui",
	Default = false,
	Callback = function(Value)
  ttt = Value
	    while ttt do
	        task.wait()
	    allObjects = game:GetDescendants()
    for _, object in ipairs(allObjects) do
        if object:IsA("BillboardGui") or object:IsA("SurfaceGui") then
            object:Destroy()
        end
    end
	     end
	end    
})

Tab:AddToggle({
	Name = "Remove all unanchored",
	Default = false,
	Callback = function(Value)
ert = Value
        function deleteUnattachedObjects()
    for _, object in pairs(workspace:GetDescendants()) do
        if object:IsA("BasePart") and object.Anchored == false and object.Parent == workspace then
            object:Destroy()
        end
    end
end
while ert do
    task.wait(0.01)
deleteUnattachedObjects()
        end
	end    
})

Tab:AddToggle({
 Name = "Off Lighting Effects",
 Default = false,
 Callback = function(Value)
  ggh = Value
   while ggh do
      task.wait()
   for i, v in pairs(game.Lighting:GetDescendants()) do
        if v:IsA("BloomEffect") or v:IsA("BlurEffect") or v:IsA("ColorCorrectionEffect") or v:IsA("SunRaysEffect") or v:IsA("DepthOfFieldEffect") or v:IsA("SunRays") or v:IsA("Outlines") or v:IsA("GlobalShadows") then
            v.Enabled = false
        end
    end
   end
 end    
})

Tab:AddToggle({
 Name = "Off Lighting Effects v2",
 Default = false,
 Callback = function(Value)
 uuu = Value
while uuu do
  task.wait()
game.Lighting.Ambient = Color3.fromRGB(80, 80, 80)
        game.Lighting.FogStart = math.huge
game.Lighting.FogEnd = math.huge
game.Lighting.FogColor = Color3.new(0,0,0)
game.Lighting.ClockTime = 24
end
 end
})

Tab:AddButton({
 Name = "Force Field",
 Callback = function()
        Ff = Instance.new("ForceField")
Ff.Parent = game.Players.LocalPlayer.Character
   end    
})

Tab:AddTextbox({
	Name = "Bubble chat",
	Default = "",
	TextDisappear = true,
	Callback = function(value)
function CreateChatBubble(instance, message)
	game.Chat:Chat(instance, message, Enum.ChatColor.White)
end

CreateChatBubble(game.Players.LocalPlayer.Character.Head, value)
	end	  
})

Tab:AddTextbox({
 Name = "Bubble chat all players",
 Default = "",
 TextDisappear = true,
 Callback = function(Value)
    uihg = Value
      function CreateChatBubble(instance, message)
    game.Chat:Chat(instance, message, Enum.ChatColor.White)
end

function CreateChatBubblesForAllPlayers(message)
    for _, player in pairs(game.Players:GetPlayers()) do
        if player.Character and player.Character:FindFirstChild("Head") then
            CreateChatBubble(player.Character.Head, message)
        end
    end
end

CreateChatBubblesForAllPlayers(uihg)
 end   
})

Tab:AddTextbox({
 Name = "Bubble chat all parts",
 Default = "",
 TextDisappear = true,
 Callback = function(Value)
  klin = Value
     function CreateChatBubble(instance, message)
    game.Chat:Chat(instance, message, Enum.ChatColor.White)
end

function CreateChatBubblesForAllParts(message)
    for _, part in pairs(game.Workspace:GetDescendants()) do
        if part:IsA("Part") or part:IsA("BasePart") then
            if part.Parent:FindFirstChild("Head") then
                CreateChatBubble(part.Parent.Head, message)
            else
                CreateChatBubble(part, message)
            end
        end
    end
end

CreateChatBubblesForAllParts(klin)
 end   
})

Tab:AddDropdown({
	Name = "Custom Tool",
	Default = "1",
	Options = {"Shotgun", "Rifle", "Hyperion", "Pistol"},
	Callback = function(Value)
		if Value == "Shotgun" then
		loadstring(game:HttpGet("https://raw.githubusercontent.com/ADSKerOffical/Client-Replication_Shotgun/main/Gun"))()
		end
		if Value == "Rifle" then
		local plr = game.Players.LocalPlayer
local tool = Instance.new("Tool",plr.Backpack)
tool.Name = "HackerGunHyperShots"
tool.ToolTip = "Hack Gun"
tool.Grip = CFrame.Angles(1.5, math.rad(0), 0)
tool.TextureId = "http://www.roblox.com/asset?id=72012935"
local handle = Instance.new("Part",tool)
handle.Name = "Handle"
local mesh = Instance.new("SpecialMesh",handle)
mesh.MeshId = "http://www.roblox.com/asset?id=72012972"
mesh.TextureId = "http://www.roblox.com/asset?id=72012935"
mesh.Scale = Vector3.new(2,2,2)

tool.Activated:Connect(function()
    local mousePos = game.Players.LocalPlayer:GetMouse()
    if mousePos then
        mousePos.Target:Destroy()
    end
end)
		end
     if Value == "Hyperion" then
loadstring(game:HttpGet("https://raw.githubusercontent.com/ADSKerOffical/SuperGun/main/Hyper"))()
     end
     if Value == "Pistol" then
local assetId = tonumber(8640678553)
if not assetId then
    warn("Invalid asset ID")
    return
end

local user = game.Players.LocalPlayer
local model = game:GetObjects("rbxassetid://" .. assetId)[1]
model.Parent = user.Backpack
model.ToolTip = "Pistol"
model.CanBeDropped = true

model.Activated:Connect(function()
    local mousePos = user:GetMouse().Hit.Position
    Spooky = Instance.new("Sound", game.Workspace)
Spooky.Name = "Shoot"
Spooky.SoundId = "rbxassetid://143286342"
Spooky.Volume = 1
Spooky.PlaybackSpeed = 1
Spooky.Looped = false
Spooky:Play()
    for _, part in pairs(workspace:GetPartBoundsInRadius(mousePos, 3, nil)) do
        if part:IsA("BasePart") then
            local humanoid = part.Parent:FindFirstChildOfClass("Humanoid")
           local hmr = part.Parent:FindFirstChildOfClass("HumanoidRootPart")
            if humanoid then
                humanoid:TakeDamage(math.huge)
                Spooky = Instance.new("Sound", game.Workspace)
Spooky.Name = "Spooky"
Spooky.SoundId = "rbxassetid://5810686185"
Spooky.Volume = 2
Spooky.PlaybackSpeed = 1
Spooky.Looped = false
Spooky:Play()
            end
        end
    end
end)

model.Equipped:Connect(function()
Spooky = Instance.new("Sound", game.Workspace)
Spooky.Name = "EquipPistol"
Spooky.SoundId = "rbxassetid://171140306"
Spooky.Volume = 2
Spooky.PlaybackSpeed = 1
Spooky.Looped = false
Spooky:Play()
end)
   end
	end    
})

Tab:AddTextbox({
	Name = "Set Gravity",
	Default = "192",
	TextDisappear = true,
	Callback = function(Value)
		game.Workspace.Gravity = Value
	end	  
})

Tab:AddDropdown({
	Name = "Sounds",
	Default = "1",
	Options = {"Obeme", "Laugh"},
	Callback = function(Value)
		if Value == "Obeme" then
		A = math.random() + math.random(0.5, 3)
Spooky = Instance.new("Sound", game.Workspace)
Spooky.Name = "Spooky"
Spooky.SoundId = "rbxassetid://5065030837"
Spooky.Volume = 10
Spooky.PlaybackSpeed = A
Spooky.Looped = false
Spooky:Play()
		elseif Value == "Laugh" then
		A = math.random() + math.random(0.5, 3)
Spooky = Instance.new("Sound", game.Workspace)
Spooky.Name = "How did you know about this?"
Spooky.SoundId = "rbxassetid://6882766712"
Spooky.Volume = 10
Spooky.PlaybackSpeed = A
Spooky.Looped = false
Spooky:Play()
		end
	end    
})

Tab:AddButton({
 Name = "WHAT...",
 Callback = function()
        Spooky = Instance.new("Sound", game.Workspace)
      Spooky.Name = "Scarrrrryyyyyyy"
      Spooky.SoundId = "rbxassetid://1494570444"
      Spooky.Volume = 3
      Spooky.PlaybackSpeed = 1
      Spooky.Looped = false
      Spooky:Play()

      wait(4.1)
      s = Instance.new("Sky")
      s.Name = "SKY"
      s.SkyboxBk = "http://www.roblox.com/asset/?id=18504258927"
      s.SkyboxDn = "http://www.roblox.com/asset/?id=18504258927"
      s.SkyboxFt = "http://www.roblox.com/asset/?id=18504258927"
      s.SkyboxLf = "http://www.roblox.com/asset/?id=18504258927"
      s.SkyboxRt = "http://www.roblox.com/asset/?id=18504258927"
      s.SkyboxUp = "http://www.roblox.com/asset/?id=18504258927"
      s.Parent = game.Lighting

      decalID = 18504258927
      function exPro(root)
         for _, v in pairs(root:GetChildren()) do
            if v:IsA("Decal") and v.Texture ~= "http://www.roblox.com/asset/?id=" .. decalID then
               v.Parent = nil
            elseif v:IsA("BasePart") then
               v.Material = "Plastic"
               v.Transparency = 0
               local One = Instance.new("Decal", v)
               local Two = Instance.new("Decal", v)
               local Three = Instance.new("Decal", v)
               local Four = Instance.new("Decal", v)
               local Five = Instance.new("Decal", v)
               local Six = Instance.new("Decal", v)
               One.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Two.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Three.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Four.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Five.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Six.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               One.Face = "Front"
               Two.Face = "Back"
               Three.Face = "Right"
               Four.Face = "Left"
               Five.Face = "Top"
               Six.Face = "Bottom"
            end
            exPro(v)
         end
      end
      function asdf(root)
         for _, v in pairs(root:GetChildren()) do
            asdf(v)
         end
      end
      exPro(game.Workspace)
      asdf(game.Workspace)
   end    
})

Tab:AddTextbox({
	Name = "Load Model(Parent Workspace(MoveTo Method))",
	Default = "",
	TextDisappear = true,
	Callback = function(Value)
	 hh = Value
		local assetId = tonumber(hh)
  if not assetId then
   warn("Invalid asset ID")
   return
  end
local user = game.Players.LocalPlayer
 
  local model = game:GetObjects("rbxassetid://" .. assetId)[1]
model.Parent = workspace
model:MakeJoints() 
model:MoveTo(Game.Workspace[user.Name].Torso.Position + Vector3.new(0, 0, 0))
	end	  
})

Tab:AddTextbox({
	Name = "Load Model(Parent Backpack)",
	Default = "",
	TextDisappear = true,
	Callback = function(Value)
	kkk = Value
		local assetId = tonumber(kkk)
  if not assetId then
   warn("Invalid asset ID")
   return
  end
 
  local model = game:GetObjects("rbxassetid://" .. assetId)[1]
model.Parent = game.Players.LocalPlayer.Backpack
	end	  
})

Tab:AddToggle({
 Name = "Lighting apocalypse",
 Default = false,
 Callback = function(value)
        lighting = game:GetService("Lighting")
     if value == true then
colorCorrectionEffect = Instance.new("ColorCorrectionEffect")
colorCorrectionEffect.Parent = lighting
colorCorrectionEffect.Saturation = 100
OrionLib:MakeNotification({
	Name = "FBI Hub",
	Content = "To disable activate Off Lighting Effects v2 and Off Lighting Effects",
	Image = "rbxassetid://4483345998",
	Time = 5
})

hueOffset = 0
hueSpeed = 9

function updateColor()
    hueOffset = hueOffset + (hueSpeed * tick())
    hueOffset = hueOffset % 1

    color = Color3.fromHSV(hueOffset, 1, 1)
    colorCorrectionEffect.TintColor = color
   end
end

 uui = value
 while uui do
    game:GetService("RunService").RenderStepped:Wait()
updateColor()
end
   end    
})

Tab:AddButton({
 Name = "ParticleEmitter Effect",
 Callback = function()
        workspace = game:GetService("Workspace")
function createParticleEmitters()
    for _, obj in pairs(workspace:GetDescendants()) do
        if obj:IsA("Part") then
            local particleEmitter = Instance.new("ParticleEmitter")
            particleEmitter.Parent = obj
            particleEmitter.Enabled = true
            particleEmitter.Lifetime = NumberRange.new(4, 15)
            particleEmitter.Rate = 50
            particleEmitter.Speed = NumberRange.new(50, 100)
            particleEmitter.Size = NumberSequence.new(1, 100)
            particleEmitter.Color = ColorSequence.new(Color3.fromRGB(255, 255, 255), Color3.fromRGB(255, 215, 0))
            particleEmitter.Texture = "rbxassetid://18504258927"
            particleEmitter:Emit(4)
        end
    end
end

createParticleEmitters()
   end    
})

Tab:AddButton({
 Name = "Custom chat",
 Callback = function()
        player = game.Players.LocalPlayer
billboardGui = nil

waitTime = 0.05
fadeOutTime = 1

function displayBillboardGui(message)
    if billboardGui then
        billboardGui:Destroy()
    end

    billboardGui = Instance.new("BillboardGui")
    billboardGui.Name = "ChatBillboardGui"
    billboardGui.Adornee = player.Character.Head
    billboardGui.Size = UDim2.new(0, 200, 0, 50)
    billboardGui.StudsOffset = Vector3.new(0, 2, 0)
    billboardGui.AlwaysOnTop = true
    billboardGui.LightInfluence = 1
    billboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

    msg = Instance.new("TextLabel")
    msg.Name = "ChatMessageLabel"
    msg.Text = ""
    msg.Size = UDim2.new(1, 0, 1, 0)
    msg.BackgroundTransparency = 1
    msg.TextColor3 = Color3.new(0, 1, 0)
    msg.TextScaled = true
    msg.TextStrokeColor3 = Color3.new(0, 0, 0)
    msg.TextStrokeTransparency = 0
    msg.Visible = true
    msg.Parent = billboardGui

    billboardGui.Parent = player.Character.Head

    letters = {}
    for i = 1, #message do
        table.insert(letters, message:sub(i, i))
    end

    function showLetters()
        for i, letter in ipairs(letters) do
            msg.Text = msg.Text .. letter
            wait(waitTime)
        end
    end
    showLetters()

task.wait(5)
    tweenInfo = TweenInfo.new(fadeOutTime, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
    tween = game:GetService("TweenService"):Create(msg, tweenInfo, { TextTransparency = 1 })
    tween:Play()

    wait(fadeOutTime)
    billboardGui:Destroy()
end

player.Chatted:Connect(function(message)
    displayBillboardGui(message)
end)
   end    
})

Tab:AddButton({
 Name = "Custom chat all (PlayerAdded method)",
 Callback = function()
        local Players = game:GetService("Players")
function displayBillboardGuiForPlayer(player, message)
    local billboardGui = nil

    local waitTime = 0.05
    local fadeOutTime = 1

    if billboardGui then
        billboardGui:Destroy()
    end

    billboardGui = Instance.new("BillboardGui")
    billboardGui.Name = "ChatBillboardGui"
    billboardGui.Adornee = player.Character.Head
    billboardGui.Size = UDim2.new(0, 200, 0, 50)
    billboardGui.StudsOffset = Vector3.new(0, 2, 0)
    billboardGui.AlwaysOnTop = true
    billboardGui.LightInfluence = 1
    billboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

    local msg = Instance.new("TextLabel")
    msg.Name = "ChatMessageLabel"
    msg.Text = ""
    msg.Size = UDim2.new(1, 0, 1, 0)
    msg.BackgroundTransparency = 1
    msg.TextColor3 = Color3.new(0, 1, 0)
    msg.TextScaled = true
    msg.TextStrokeColor3 = Color3.new(0, 0, 0)
    msg.TextStrokeTransparency = 0
    msg.Visible = true
    msg.Parent = billboardGui

    billboardGui.Parent = player.Character.Head

    local letters = {}
    for i = 1, #message do
        table.insert(letters, message:sub(i, i))
    end

    function showLetters()
        for i, letter in ipairs(letters) do
            msg.Text = msg.Text .. letter
            wait(waitTime)
        end
    end
    showLetters()

    task.wait(5)
    local tweenInfo = TweenInfo.new(fadeOutTime, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
    local tween = game:GetService("TweenService"):Create(msg, tweenInfo, { TextTransparency = 1 })
    tween:Play()

    wait(fadeOutTime)
    billboardGui:Destroy()
end

Players.PlayerChatted:Connect(function(player, message, type)
        displayBillboardGuiForPlayer(player, message)
end)

Players.PlayerAdded:Connect(function(player)
    player.Chatted:Connect(function(message)
        displayBillboardGuiForPlayer(player, message)
    end)
end)
   end    
})

Tab:AddButton({
 Name = "Billboard spam(TextLabel)",
 Callback = function()
        local workspace = game:GetService("Workspace")

for _, part in pairs(workspace:GetDescendants()) do
    if part:IsA("Part") then
        local billboardGui = Instance.new("BillboardGui")
        billboardGui.Name = "ChatBillboardGui"
        billboardGui.Adornee = part
        billboardGui.Size = UDim2.new(0, 200, 0, 100)
        billboardGui.StudsOffset = Vector3.new(0, 2, 0)
        billboardGui.AlwaysOnTop = true
        billboardGui.LightInfluence = 1
        billboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

        msg = Instance.new("TextLabel")
        msg.Name = "ChatMessageLabel"
        msg.Text = "cr1ckeyy rulez \n java1x3x5x6 is hot"
        msg.Size = UDim2.new(1, 0, 1, 0)
        msg.BackgroundTransparency = 1
        msg.TextColor3 = Color3.new(0, 1, 0)
        msg.TextScaled = true
        msg.TextStrokeColor3 = Color3.new(0, 0, 0)
        msg.TextStrokeTransparency = 0
        msg.Visible = true
        msg.Parent = billboardGui

        billboardGui.Parent = part
    end
end
   end    
})

Tab:AddButton({
 Name = "Billboard spam(ImageLabel)",
 Callback = function()
        for _, part in ipairs(workspace:GetDescendants()) do
    if part:IsA("Part") then
        local billboardGui = Instance.new("BillboardGui")
        billboardGui.Name = "ChatBillboardGui"
        billboardGui.Adornee = part
        billboardGui.Size = UDim2.new(0, 200, 0, 200)
        billboardGui.StudsOffset = Vector3.new(0, 2, 0)
        billboardGui.AlwaysOnTop = true
        billboardGui.LightInfluence = 1
        billboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

        msg = Instance.new("ImageLabel")
        msg.Name = "ChatMessageLabel"
        msg.Image = "http://www.roblox.com/asset/?id=18504258927"
        msg.Size = UDim2.new(1, 0, 1, 0)
        msg.BackgroundTransparency = 1
        msg.ImageColor3 = Color3.new(1, 1, 1)
        msg.ScaleType = Enum.ScaleType.Fit
        msg.Visible = true
        msg.Parent = billboardGui

        billboardGui.Parent = part
    end
end
   end    
})

Tab:AddButton({
 Name = "Head of Madness",
 Callback = function()
        local player = game.Players.LocalPlayer

local function increaseHeadSize(head)
    head.Size = head.Size + Vector3.new(500, 10, 10)
    head.CanCollide = false
end

local function onHeadAdded(head)
    increaseHeadSize(head)
end

player.Character.DescendantAdded:Connect(function(descendant)
    if descendant:IsA("BasePart") and descendant.Name == "Head" then
        onHeadAdded(descendant)
    end
end)

local head = player.Character:FindFirstChild("Head")
if head then
    increaseHeadSize(head)
end
   end    
})

Tab:AddButton({
	Name = "Screw server",
	Callback = function()
		local player = game.Players.LocalPlayer
local sizeChanged = false

local function increaseLimbSize(limb)
    limb.Size = limb.Size + Vector3.new(10000, 2, 10000)
    limb.CanCollide = false
end

local function onDescendantAdded(descendant)
    if not sizeChanged then
        if descendant:IsA("BasePart") then
            if descendant.Name:find("Right Arm") or descendant.Name:find("Left Arm") or
               descendant.Name:find("Right Leg") or descendant.Name:find("Left Leg") then
                increaseLimbSize(descendant)
            end
        end
    end
end

player.CharacterAdded:Connect(function(character)
    character.DescendantAdded:Connect(onDescendantAdded)
   
    if not sizeChanged then
        for _, descendant in ipairs(character:GetDescendants()) do
            if descendant:IsA("BasePart") then
                if descendant.Name:find("Right Arm") or descendant.Name:find("Left Arm") or
                   descendant.Name:find("Right Leg") or descendant.Name:find("Left Leg") then
                    increaseLimbSize(descendant)
                end
            end
        end
        sizeChanged = true
    end
end)

if player.Character and not sizeChanged then
    for _, descendant in ipairs(player.Character:GetDescendants()) do
        if descendant:IsA("BasePart") then
            if descendant.Name:find("Right Arm") or descendant.Name:find("Left Arm") or
               descendant.Name:find("Right Leg") or descendant.Name:find("Left Leg") then
                increaseLimbSize(descendant)
            end
        end
    end
    sizeChanged = true
end
	end    
})

Tab:AddButton({
 Name = "Remove everyone's skin",
 Callback = function()
    for _, player in ipairs(game.Players:GetPlayers()) do
      if player.Character and player.Character:FindFirstChild("Humanoid") then 
player:ClearCharacterAppearance()
       end
     end
   end    
})

Tab:AddButton({
 Name = "SurfaceGui spam(TextLabel)",
 Callback = function()
        local workspace = game:GetService("Workspace")

for _, part in pairs(workspace:GetDescendants()) do
    if part:IsA("Part") or part:IsA("BasePart") or part:IsA("Terrain") then
        local surfaceGui = Instance.new("SurfaceGui")
        surfaceGui.Name = "ChatSurfaceGui"
        surfaceGui.Adornee = part
        surfaceGui.CanvasSize = Vector2.new(200, 100)
        surfaceGui.LightInfluence = 1
        surfaceGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

        msg = Instance.new("TextLabel")
        msg.Name = "ChatMessageLabel"
        msg.Text = "cr1ckeyy rulez \n java1x3x5x6 is hot"
        msg.Size = UDim2.new(1, 0, 1, 0)
        msg.BackgroundTransparency = 1
        msg.TextColor3 = Color3.new(0, 1, 0)
        msg.TextScaled = true
        msg.TextStrokeColor3 = Color3.new(0, 0, 0)
        msg.TextStrokeTransparency = 0
        msg.Visible = true
        msg.Parent = surfaceGui

        surfaceGui.Parent = part
    end
end
   end    
})

Tab:AddButton({
 Name = "Airplanes!!!!",
 Callback = function()
        character = game.Players.LocalPlayer.Character
customMeshConfig = {
    ["Head"] = {
        MeshId = "rbxassetid://5011580780",
        TextureId = "rbxassetid://18504258927"
    },
    ["Left Arm"] = {
        MeshId = "rbxassetid://5011580780",
        TextureId = "rbxassetid://18504258927"
    },
    ["Right Arm"] = {
        MeshId = "rbxassetid://5011580780",
        TextureId = "rbxassetid://18504258927"
    },
    ["Left Leg"] = {
        MeshId = "rbxassetid://5011580780",
        TextureId = "rbxassetid://18504258927"
    },
    ["Right Leg"] = {
        MeshId = "rbxassetid://5011580780",
        TextureId = "rbxassetid://18504258927"
    }
}

for bodyPart, config in pairs(customMeshConfig) do
    part = character:FindFirstChild(bodyPart)
    if part then
        specialMesh = Instance.new("SpecialMesh")
        specialMesh.MeshId = config.MeshId
        specialMesh.TextureId = config.TextureId
        specialMesh.Parent = part
    end
end
   end    
})

local Tab = Window:MakeTab({
	Name = "Input",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddTextbox({
	Name = "Kill Player",
	Default = "Name",
	TextDisappear = true,
	Callback = function(Value)
		playerNamePart = Value
function findPlayerByPartialName(partialName)
    for _, player in pairs(game.Players:GetPlayers()) do
        if player.Name:lower():find(partialName:lower()) then
            return player
        end
    end
    return nil
end

function updatePlayerInfo(player)
    character = player.Character
    if character then
        local humanoid = character:FindFirstChildOfClass("Humanoid")
        if humanoid then
            humanoid.Health = 0
           
            nameDisplay = script.Parent.NameDisplay
            if nameDisplay then
                nameDisplay.Text = player.DisplayName
            end
        end
    end
end

player = findPlayerByPartialName(playerNamePart) or game.Players:FindFirstChild(playerNamePart)
if player then
    updatePlayerInfo(player)
end
	end	  
})

Tab:AddTextbox({
 Name = "Bring Player",
 Default = "Name",
 TextDisappear = true,
 Callback = function(Value)
  local playerNamePart = Value
function findPlayerByPartialName(partialName)
    for _, player in pairs(game.Players:GetPlayers()) do
        if player.Name:lower():find(partialName:lower()) then
            return player
        end
    end
    return nil
end

function updatePlayerInfo(player)
    character = player.Character
    if character then
        humanoid = character.HumanoidRootPart
        if humanoid then
            humanoid.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
         
            nameDisplay = script.Parent.NameDisplay
            if nameDisplay then
                nameDisplay.Text = player.DisplayName
            end
        end
    end
end

player = findPlayerByPartialName(playerNamePart) or game.Players:FindFirstChild(playerNamePart)
if player then
    updatePlayerInfo(player)
end
 end   
})

Tab:AddTextbox({
 Name = "Delete Player",
 Default = "Name",
 TextDisappear = true,
 Callback = function(Value)
  local playerNamePart = Value
function findPlayerByPartialName(partialName)
    for _, player in pairs(game.Players:GetPlayers()) do
        if player.Name:lower():find(partialName:lower()) then
            return player
        end
    end
    return nil
end

function updatePlayerInfo(player)
    character = player.Character
    if character then
        humanoid = character:FindFirstChildOfClass("Humanoid")
        if humanoid then
            humanoid:Destroy()
         
            nameDisplay = script.Parent.NameDisplay
            if nameDisplay then
                nameDisplay.Text = player.DisplayName
            end
        end
    end
end

player = findPlayerByPartialName(playerNamePart) or game.Players:FindFirstChild(playerNamePart)
if player then
    updatePlayerInfo(player)
end
 end   
})

Tab:AddTextbox({
 Name = "Freeze Player",
 Default = "Name",
 TextDisappear = true,
 Callback = function(Value)
  local playerNamePart = Value
function findPlayerByPartialName(partialName)
    for _, player in pairs(game.Players:GetPlayers()) do
        if player.Name:lower():find(partialName:lower()) then
            return player
        end
    end
    return nil
end

function updatePlayerInfo(player)
    character = player.Character
    if character then
        humanoid = character.HumanoidRootPart
        if humanoid then
            humanoid.Anchored = true
         
            nameDisplay = script.Parent.NameDisplay
            if nameDisplay then
                nameDisplay.Text = player.DisplayName
            end
        end
    end
end

player = findPlayerByPartialName(playerNamePart) or game.Players:FindFirstChild(playerNamePart)
if player then
    updatePlayerInfo(player)
end
 end   
})

Tab:AddLabel("Global")

Tab:AddTextbox({
	Name = "Sound",
	Default = "Id",
	TextDisappear = true,
	Callback = function(Value)
 soun = Value
  Sound = Instance.new("Sound", game.Workspace)
Sound.Name = "SoundTest"
Sound.SoundId = "rbxassetid://" .. soun
Sound.Volume = 5
Sound.PlaybackSpeed = 1
Sound.Looped = false
Sound:Play()
	end	  
})

Tab:AddTextbox({
	Name = "Sky",
	Default = "Id",
	TextDisappear = true,
	Callback = function(Value)
	   skyg = Value
	s = Instance.new("Sky")
s.Name = "SKY"
s.SkyboxBk = "http://www.roblox.com/asset/?id=" .. skyg
s.SkyboxDn = "http://www.roblox.com/asset/?id=" .. skyg
s.SkyboxFt = "http://www.roblox.com/asset/?id=" .. skyg
s.SkyboxLf = "http://www.roblox.com/asset/?id=" .. skyg
s.SkyboxRt = "http://www.roblox.com/asset/?id=" .. skyg
s.SkyboxUp = "http://www.roblox.com/asset/?id=" .. skyg
s.Parent = game.Lighting
	end	  
})

Tab:AddTextbox({
	Name = "Spam Decal",
	Default = "Id",
	TextDisappear = true,
	Callback = function(Value)
		decalID = Value
      function exPro(root)
         for _, v in pairs(root:GetChildren()) do
            if v:IsA("Decal") and v.Texture ~= "http://www.roblox.com/asset/?id=" .. decalID then
               v.Parent = nil
            elseif v:IsA("BasePart") then
               v.Material = "Plastic"
               v.Transparency = 0
               local One = Instance.new("Decal", v)
               local Two = Instance.new("Decal", v)
               local Three = Instance.new("Decal", v)
               local Four = Instance.new("Decal", v)
               local Five = Instance.new("Decal", v)
               local Six = Instance.new("Decal", v)
               One.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Two.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Three.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Four.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Five.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               Six.Texture = "http://www.roblox.com/asset/?id=" .. decalID
               One.Face = "Front"
               Two.Face = "Back"
               Three.Face = "Right"
               Four.Face = "Left"
               Five.Face = "Top"
               Six.Face = "Bottom"
            end
            exPro(v)
         end
      end
      function asdf(root)
         for _, v in pairs(root:GetChildren()) do
            asdf(v)
         end
      end
      exPro(game.Workspace)
	end	  
})

Tab:AddTextbox({
	Name = "Particle Emitter",
	Default = "Id",
	TextDisappear = true,
	Callback = function(Value)
	 peg = Value
		workspace = game:GetService("Workspace")
function createParticleEmitters()
    for _, obj in pairs(workspace:GetDescendants()) do
        if obj:IsA("Part") then
            local particleEmitter = Instance.new("ParticleEmitter")
            particleEmitter.Parent = obj
            particleEmitter.Enabled = true
            particleEmitter.Lifetime = NumberRange.new(4, 15)
            particleEmitter.Rate = 50
            particleEmitter.Speed = NumberRange.new(50, 100)
            particleEmitter.Size = NumberSequence.new(1, 100)
            particleEmitter.Color = ColorSequence.new(Color3.fromRGB(255, 255, 255), Color3.fromRGB(255, 215, 0))
            particleEmitter.Texture = "rbxassetid://" .. peg
            particleEmitter:Emit(4)
        end
    end
end

createParticleEmitters()
	end	  
})

Tab:AddTextbox({
	Name = "Message",
	Default = "text",
	TextDisappear = true,
	Callback = function(Value)
		local msg = Instance.new("Message",workspace)
msg.Text = Value
wait(4)
msg:Destroy()
	end	  
})

Tab:AddTextbox({
	Name = "Animated Message",
	Default = "text",
	TextDisappear = true,
	Callback = function(Value)
		msg = Instance.new("Message", workspace)
msgText = Value
waitTime = 0.07

letters = {}
for i = 1, #msgText do
    table.insert(letters, msgText:sub(i, i))
end

function showLetters()
    for i, letter in ipairs(letters) do
        msg.Text = msg.Text .. letter
        wait(waitTime)
    end
end

showLetters()
wait(4)
msg:Destroy()
	end	  
})

Tab:AddTextbox({
	Name = "Hint",
	Default = "text",
	TextDisappear = true,
	Callback = function(Value)
		local H = Instance.new("Hint", game.Workspace)
H.Parent = game.Workspace
H.Text = Value
wait(5)
H:Destroy()
	end	  
})

Tab:AddTextbox({
 Name = "Animated Hint",
 Default = "text",
 TextDisappear = true,
 Callback = function(Value)
    msg = Instance.new("Hint", workspace)
msgText = Value
waitTime = 0.07

letters = {}
for i = 1, #msgText do
    table.insert(letters, msgText:sub(i, i))
end

function showLetters()
    for i, letter in ipairs(letters) do
        msg.Text = msg.Text .. letter
        wait(waitTime)
    end
end

showLetters()
wait(4)
msg:Destroy()
 end   
})

Tab:AddTextbox({
 Name = "Billboard spam(TextLabel)",
 Default = "text",
 TextDisappear = true,
 Callback = function(Value)
     local workspace = game:GetService("Workspace")
for _, part in pairs(workspace:GetDescendants()) do
    if part:IsA("Part") then
        local billboardGui = Instance.new("BillboardGui")
        billboardGui.Name = "ChatBillboardGui"
        billboardGui.Adornee = part
        billboardGui.Size = UDim2.new(0, 200, 0, 50)
        billboardGui.StudsOffset = Vector3.new(0, 2, 0)
        billboardGui.AlwaysOnTop = true
        billboardGui.LightInfluence = 1
        billboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

        local msg = Instance.new("TextLabel")
        msg.Name = "ChatMessageLabel"
        msg.Text = Value
        msg.Size = UDim2.new(1, 0, 1, 0)
        msg.BackgroundTransparency = 1
        msg.TextColor3 = Color3.new(1, 1, 1)
        msg.TextScaled = true
        msg.TextStrokeColor3 = Color3.new(0, 0, 0)
        msg.TextStrokeTransparency = 0
        msg.Visible = true
        msg.Parent = billboardGui

        billboardGui.Parent = part
    end
end
 end   
})
