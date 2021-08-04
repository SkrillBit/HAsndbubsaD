-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local Frame = Instance.new("Frame")
local UIGradient = Instance.new("UIGradient")
local BottomBar = Instance.new("Frame")
local UIGradient_2 = Instance.new("UIGradient")
local TextLabel = Instance.new("TextLabel")
local Imput = Instance.new("TextBox")
local Name = Instance.new("TextLabel")
local Submit = Instance.new("TextButton")
local UICorner = Instance.new("UICorner")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

MainFrame.Name = "MainFrame"
MainFrame.Parent = ScreenGui
MainFrame.AnchorPoint = Vector2.new(0.5, 0.5)
MainFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
MainFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
MainFrame.Size = UDim2.new(0, 326, 0, 292)

Frame.Parent = MainFrame
Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame.BorderColor3 = Color3.fromRGB(27, 42, 53)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0, 0, -0.0376712345, 0)
Frame.Size = UDim2.new(0, 326, 0, 11)

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(133, 255, 153)), ColorSequenceKeypoint.new(0.46, Color3.fromRGB(255, 82, 108)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(37, 215, 255))}
UIGradient.Parent = Frame

BottomBar.Name = "BottomBar"
BottomBar.Parent = MainFrame
BottomBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
BottomBar.BorderSizePixel = 0
BottomBar.Position = UDim2.new(0, 0, 1, 0)
BottomBar.Size = UDim2.new(0, 326, 0, 11)

UIGradient_2.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(133, 255, 153)), ColorSequenceKeypoint.new(0.46, Color3.fromRGB(255, 82, 108)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(37, 215, 255))}
UIGradient_2.Parent = BottomBar

TextLabel.Parent = MainFrame
TextLabel.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
TextLabel.BorderColor3 = Color3.fromRGB(25, 25, 25)
TextLabel.Position = UDim2.new(0.257668704, 0, 0.301369846, 0)
TextLabel.Size = UDim2.new(0, 158, 0, 30)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "Enter Key"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextSize = 31.000

Imput.Name = "Imput"
Imput.Parent = MainFrame
Imput.BackgroundColor3 = Color3.fromRGB(88, 88, 88)
Imput.Position = UDim2.new(0.257668704, 0, 0.527397275, 0)
Imput.Size = UDim2.new(0, 158, 0, 36)
Imput.Font = Enum.Font.SourceSans
Imput.Text = ""
Imput.TextColor3 = Color3.fromRGB(25, 25, 25)
Imput.TextSize = 16.000

Name.Name = "Name"
Name.Parent = MainFrame
Name.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
Name.BorderSizePixel = 0
Name.Position = UDim2.new(0.742331266, 0, 0.917808175, 0)
Name.Size = UDim2.new(0, 62, 0, 16)
Name.Font = Enum.Font.SourceSans
Name.Text = "Made By SkrillBit"
Name.TextColor3 = Color3.fromRGB(255, 255, 255)
Name.TextSize = 14.000

Submit.Name = "Submit"
Submit.Parent = MainFrame
Submit.BackgroundColor3 = Color3.fromRGB(97, 97, 97)
Submit.Position = UDim2.new(0.285276085, 0, 0.739726067, 0)
Submit.Size = UDim2.new(0, 139, 0, 36)
Submit.Font = Enum.Font.SourceSans
Submit.Text = "Submit"
Submit.TextColor3 = Color3.fromRGB(0, 0, 0)
Submit.TextSize = 22.000
Submit.MouseButton1Down:Connect(function()
    if Imput.Text == "E},N5mRS:2KD}@h" then
        MainFrame.Visible = false
        
        loadstring(game:HttpGet("https://pastebin.com/raw/nwhiKdkp"))()
        else game.Players.LocalPlayer:Kick("Invalid SkrillHub Key")
    end
end)
        
        

UICorner.Parent = Submit

-- Scripts:

local function KUMONZ_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	local RS = game:GetService("RunService")
	
	local rainbow = script.Parent 
	local grad = rainbow.UIGradient
	
	local counter = 0       
	local w = math.pi / 6 
	local CS = {}         
	local num = 15 			
	local frames = 0	
	
	local count = 0
	local cskCache = {}
	local gamepassid = 8782801
	local MarketplaceService = game:GetService("MarketplaceService")
	
	game.Players.PlayerAdded:Connect(function(player)
		if MarketplaceService:UserOwnsGamePassAsync(player.UserId, gamepassid) or player:GetRankInGroup(5330486) >= 200 then
			print("Rainbow nametag")
		else
			grad:Destroy()
		end
	end)
	
	while true do
		for i = 0, num do
			local c = Color3.fromRGB(127 * math.sin(w*i + counter) + 128, 127 * math.sin(w*i + 2 * math.pi/3 + counter) + 128, 127*math.sin(w*i + 4*math.pi/3 + counter) + 128)
			table.insert(CS, i+1, ColorSequenceKeypoint.new(i/num, c))
		end
		local newCS = ColorSequence.new(CS)
	
		if #cskCache > 0 then
			if newCS == cskCache[1] then
				CS = {}
				break
			end
		end
		table.insert(cskCache, newCS)
	
		CS = {}
	
		counter = counter + math.pi/40
		if (counter >= math.pi * 2) then counter = 0 end	
	end
	
	local finalCacheCt = #cskCache
	local rotation = 1
	
	RS.Heartbeat:Connect(function()	
		if math.fmod(frames, 2) == 0 then
			grad.Color = cskCache[rotation]			
			if rotation >= #cskCache then rotation = 0 end
			rotation = rotation + 1				
		end
		if frames >= 1000 then frames = 0 end
		frames = frames + 1
	end)
end
coroutine.wrap(KUMONZ_fake_script)()
local function IVGJE_fake_script() -- BottomBar.LocalScript 
	local script = Instance.new('LocalScript', BottomBar)

	local RS = game:GetService("RunService")
	
	local rainbow = script.Parent 
	local grad = rainbow.UIGradient
	
	local counter = 0       
	local w = math.pi / 6 
	local CS = {}         
	local num = 15 			
	local frames = 0	
	
	local count = 0
	local cskCache = {}
	local gamepassid = 8782801
	local MarketplaceService = game:GetService("MarketplaceService")
	
	game.Players.PlayerAdded:Connect(function(player)
		if MarketplaceService:UserOwnsGamePassAsync(player.UserId, gamepassid) or player:GetRankInGroup(5330486) >= 200 then
			print("Rainbow nametag")
		else
			grad:Destroy()
		end
	end)
	
	while true do
		for i = 0, num do
			local c = Color3.fromRGB(127 * math.sin(w*i + counter) + 128, 127 * math.sin(w*i + 2 * math.pi/3 + counter) + 128, 127*math.sin(w*i + 4*math.pi/3 + counter) + 128)
			table.insert(CS, i+1, ColorSequenceKeypoint.new(i/num, c))
		end
		local newCS = ColorSequence.new(CS)
	
		if #cskCache > 0 then
			if newCS == cskCache[1] then
				CS = {}
				break
			end
		end
		table.insert(cskCache, newCS)
	
		CS = {}
	
		counter = counter + math.pi/40
		if (counter >= math.pi * 2) then counter = 0 end	
	end
	
	local finalCacheCt = #cskCache
	local rotation = 1
	
	RS.Heartbeat:Connect(function()	
		if math.fmod(frames, 2) == 0 then
			grad.Color = cskCache[rotation]			
			if rotation >= #cskCache then rotation = 0 end
			rotation = rotation + 1				
		end
		if frames >= 1000 then frames = 0 end
		frames = frames + 1
	end)
end
coroutine.wrap(IVGJE_fake_script)()
