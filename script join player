
-- Mohamed Hajjaj GUI V3
-- UI ONLY - Roblox LocalScript

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local PlayerGui = player:WaitForChild("PlayerGui")

-- Remove old GUI
local old = PlayerGui:FindFirstChild("MohamedHajjajV3")
if old then old:Destroy() end

-- Main GUI
local GUI = Instance.new("ScreenGui")
GUI.Name = "MohamedHajjajV3"
GUI.ResetOnSpawn = false
GUI.Parent = PlayerGui

-- Main Frame
local Main = Instance.new("Frame")
Main.Size = UDim2.new(0, 300, 0, 310)
Main.Position = UDim2.new(0.5, -150, 0.4, -155)
Main.BackgroundColor3 = Color3.fromRGB(15,15,15)
Main.BorderSizePixel = 0
Main.Active = true
Main.Draggable = true
Main.Parent = GUI

local MainCorner = Instance.new("UICorner")
MainCorner.CornerRadius = UDim.new(0,12)
MainCorner.Parent = Main

-- Header
local Header = Instance.new("Frame")
Header.Size = UDim2.new(1,0,0,40)
Header.BackgroundColor3 = Color3.fromRGB(25,25,25)
Header.BorderSizePixel = 0
Header.Parent = Main

local Title = Instance.new("TextLabel")
Title.Size = UDim2.new(1,-90,1,0)
Title.Position = UDim2.new(0,10,0,0)
Title.BackgroundTransparency = 1
Title.Text = "MOHAMED HAJJAJ"
Title.TextColor3 = Color3.new(1,1,1)
Title.Font = Enum.Font.GothamBold
Title.TextSize = 14
Title.TextXAlignment = Enum.TextXAlignment.Left
Title.Parent = Header

-- Minus Button (Collapse)
local Minus = Instance.new("TextButton")
Minus.Size = UDim2.new(0,30,0,28)
Minus.Position = UDim2.new(1,-65,0,6)
Minus.BackgroundColor3 = Color3.fromRGB(40,40,40)
Minus.Text = "-"
Minus.TextColor3 = Color3.new(1,1,1)
Minus.Font = Enum.Font.GothamBold
Minus.TextSize = 20
Minus.Parent = Header

local MC = Instance.new("UICorner")
MC.CornerRadius = UDim.new(0,6)
MC.Parent = Minus

-- Close Button
local Close = Instance.new("TextButton")
Close.Size = UDim2.new(0,25,0,28)
Close.Position = UDim2.new(1,-30,0,6)
Close.BackgroundColor3 = Color3.fromRGB(150,30,30)
Close.Text = "X"
Close.TextColor3 = Color3.new(1,1,1)
Close.Font = Enum.Font.GothamBold
Close.Parent = Header

local CC = Instance.new("UICorner")
CC.CornerRadius = UDim.new(0,6)
CC.Parent = Close

-- Content
local Content = Instance.new("Frame")
Content.Size = UDim2.new(1,-20,1,-50)
Content.Position = UDim2.new(0,10,0,45)
Content.BackgroundTransparency = 1
Content.Parent = Main

-- Section Creator
local function CreateSection(y, titleText, placeholder)
    local Section = Instance.new("Frame")
    Section.Size = UDim2.new(1,0,0,115)
    Section.Position = UDim2.new(0,0,0,y)
    Section.BackgroundColor3 = Color3.fromRGB(35,35,35)
    Section.BorderSizePixel = 0
    Section.Parent = Content

    local SC = Instance.new("UICorner")
    SC.CornerRadius = UDim.new(0,8)
    SC.Parent = Section

    local Label = Instance.new("TextLabel")
    Label.Size = UDim2.new(1,0,0,28)
    Label.BackgroundTransparency = 1
    Label.Text = titleText
    Label.TextColor3 = Color3.fromRGB(0,170,255)
    Label.Font = Enum.Font.GothamBold
    Label.TextSize = 13
    Label.Parent = Section

    local Input = Instance.new("TextBox")
    Input.Size = UDim2.new(1,-20,0,32)
    Input.Position = UDim2.new(0,10,0,32)
    Input.BackgroundColor3 = Color3.fromRGB(20,20,20)
    Input.PlaceholderText = placeholder
    Input.Text = ""
    Input.TextColor3 = Color3.new(1,1,1)
    Input.PlaceholderColor3 = Color3.fromRGB(150,150,150)
    Input.Font = Enum.Font.Gotham
    Input.TextSize = 13
    Input.Parent = Section

    local IC = Instance.new("UICorner")
    IC.CornerRadius = UDim.new(0,6)
    IC.Parent = Input

    local Join = Instance.new("TextButton")
    Join.Size = UDim2.new(1,-20,0,32)
    Join.Position = UDim2.new(0,10,0,73)
    Join.BackgroundColor3 = Color3.fromRGB(0,120,255)
    Join.Text = "JOIN"
    Join.TextColor3 = Color3.new(1,1,1)
    Join.Font = Enum.Font.GothamBold
    Join.TextSize = 13
    Join.Parent = Section

    local JC = Instance.new("UICorner")
    JC.CornerRadius = UDim.new(0,6)
    JC.Parent = Join

    return Input, Join
end

-- Section 1
local ServerInput, ServerJoin =
    CreateSection(0, "سيرفر الماب الحالية", "Username اللاعب")

-- Section 2
local AllMapsInput, AllMapsJoin =
    CreateSection(125, "بحث جميع المابات", "Username اللاعب")

-- Floating Icon
local Floating = Instance.new("TextButton")
Floating.Size = UDim2.new(0,65,0,65)
Floating.Position = UDim2.new(0.05,0,0.3,0)
Floating.BackgroundColor3 = Color3.fromRGB(5,5,5)
Floating.Text = "TO\nOPEN"
Floating.TextColor3 = Color3.new(1,1,1)
Floating.Font = Enum.Font.GothamBold
Floating.TextSize = 12
Floating.Active = true
Floating.Draggable = true
Floating.Parent = GUI

local FC = Instance.new("UICorner")
FC.CornerRadius = UDim.new(1,0)
FC.Parent = Floating

local FStroke = Instance.new("UIStroke")
FStroke.Color = Color3.fromRGB(0,120,255)
FStroke.Thickness = 2
FStroke.Parent = Floating

-- Collapse / Expand
local collapsed = false

Minus.MouseButton1Click:Connect(function()
    collapsed = true
    Content.Visible = false
    Main.Size = UDim2.new(0,300,0,40)
    Minus.Text = "+"
end)

Minus.MouseButton1Click:Connect(function()
    if collapsed then
        collapsed = false
        Content.Visible = true
        Main.Size = UDim2.new(0,300,0,310)
        Minus.Text = "-"
    end
end)

Floating.MouseButton1Click:Connect(function()
    Main.Visible = not Main.Visible
end)

Close.MouseButton1Click:Connect(function()
    Main.Visible = false
end)

-- Search buttons (UI placeholders)
ServerJoin.MouseButton1Click:Connect(function()
    ServerJoin.Text = "البحث غير مربوط"
    task.wait(2)
    ServerJoin.Text = "JOIN"
end)

AllMapsJoin.MouseButton1Click:Connect(function()
    AllMapsJoin.Text = "غير متاح عالميًا"
    task.wait(2)
    AllMapsJoin.Text = "JOIN"
end)
