local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local UIStroke = Instance.new("UIStroke")
local Title = Instance.new("TextLabel")
local Button = Instance.new("TextButton")
local TeleportService = game:GetService("TeleportService")
local placeId = game.PlaceId

-- Propriedades da ScreenGui
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Propriedades da Frame
Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
Frame.Position = UDim2.new(0.5, -100, 0.5, -150)
Frame.Size = UDim2.new(0, 200, 0, 150)
Frame.Active = true
Frame.Draggable = true

-- Adicionando cantos arredondados e borda à Frame
UICorner.CornerRadius = UDim.new(0, 50)
UICorner.Parent = Frame

UIStroke.Color = Color3.fromRGB(255, 255, 255)
UIStroke.Thickness = 2
UIStroke.Parent = Frame

-- Propriedades do Title
Title.Parent = Frame
Title.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
Title.Size = UDim2.new(1, 0, 0, 50)
Title.Font = Enum.Font.SourceSansBold
Title.Text = "tubergamer (beta) (1.1)"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextSize = 24

local titleCorner = Instance.new("UICorner")
titleCorner.CornerRadius = UDim.new(0, 50)
titleCorner.Parent = Title

-- Propriedades do Button
Button.Parent = Frame
Button.BackgroundColor3 = Color3.fromRGB(255, 140, 0)
Button.Position = UDim2.new(0.5, -75, 0.5, 10)
Button.Size = UDim2.new(0, 150, 0, 50)
Button.Text = "inf (risk ban)"
Button.TextColor3 = Color3.fromRGB(255, 255, 255)
Button.Font = Enum.Font.SourceSansBold
Button.TextSize = 20

local buttonCorner = Instance.new("UICorner")
buttonCorner.CornerRadius = UDim.new(0, 50)
buttonCorner.Parent = Button

-- Script do botão
Button.MouseButton1Click:Connect(function()
    game:GetService("ReplicatedStorage").RemoteEvents.AddFans:FireServer(9e999999)
    game:GetService("ReplicatedStorage").RemoteEvents.WinsGiver:FireServer(9e99999)
    game:GetService("ReplicatedStorage").RemoteEvents.GemsGiver:FireServer(9e99999)
    TeleportService:Teleport(placeId, game.Players.LocalPlayer)
end)
