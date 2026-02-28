local player = game.Players.LocalPlayer

-- Criar GUI
local screenGui = Instance.new("ScreenGui")
screenGui.Parent = player:WaitForChild("PlayerGui")

-- Painel principal
local frame = Instance.new("Frame")
frame.Parent = screenGui
frame.Size = UDim2.new(0, 400, 0, 300)
frame.Position = UDim2.new(0.5, -200, 0.5, -150)
frame.BackgroundColor3 = Color3.fromRGB(40, 0, 60)
frame.BorderSizePixel = 0

-- Cantos arredondados
local corner = Instance.new("UICorner")
corner.CornerRadius = UDim.new(0, 15)
corner.Parent = frame

-- Título
local title = Instance.new("TextLabel")
title.Parent = frame
title.Size = UDim2.new(1, 0, 0, 60)
title.Position = UDim2.new(0, 0, 0, 10)
title.BackgroundTransparency = 1
title.Text = "CRAZY TP ⚡️VIP\nCOLOQUE SUA KEY 👇🏻"
title.TextColor3 = Color3.fromRGB(255,255,255)
title.TextScaled = true
title.Font = Enum.Font.GothamBold

-- Caixa de texto (Key)
local keyBox = Instance.new("TextBox")
keyBox.Parent = frame
keyBox.Size = UDim2.new(0.8, 0, 0, 40)
keyBox.Position = UDim2.new(0.1, 0, 0.4, 0)
keyBox.PlaceholderText = "Digite sua key aqui..."
keyBox.Text = ""
keyBox.BackgroundColor3 = Color3.fromRGB(70, 0, 100)
keyBox.TextColor3 = Color3.fromRGB(255,255,255)
keyBox.Font = Enum.Font.Gotham
keyBox.TextScaled = true

local keyCorner = Instance.new("UICorner")
keyCorner.CornerRadius = UDim.new(0, 10)
keyCorner.Parent = keyBox

-- Texto pegar key
local infoText = Instance.new("TextLabel")
infoText.Parent = frame
infoText.Size = UDim2.new(1, 0, 0, 30)
infoText.Position = UDim2.new(0, 0, 0.6, 0)
infoText.BackgroundTransparency = 1
infoText.Text = "Se você não tem key pegue aqui 👇🏻"
infoText.TextColor3 = Color3.fromRGB(255,255,255)
infoText.TextScaled = true
infoText.Font = Enum.Font.Gotham

-- Botão Get Key
local getKeyButton = Instance.new("TextButton")
getKeyButton.Parent = frame
getKeyButton.Size = UDim2.new(0.6, 0, 0, 40)
getKeyButton.Position = UDim2.new(0.2, 0, 0.75, 0)
getKeyButton.Text = "GET KEY"
getKeyButton.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
getKeyButton.TextColor3 = Color3.fromRGB(255,255,255)
getKeyButton.Font = Enum.Font.GothamBold
getKeyButton.TextScaled = true

local btnCorner = Instance.new("UICorner")
btnCorner.CornerRadius = UDim.new(0, 10)
btnCorner.Parent = getKeyButton

-- Aviso
local aviso = Instance.new("TextLabel")
aviso.Parent = frame
aviso.Size = UDim2.new(1, 0, 0, 25)
aviso.Position = UDim2.new(0, 0, 0.9, 0)
aviso.BackgroundTransparency = 1
aviso.Text = ""
aviso.TextColor3 = Color3.fromRGB(0,255,0)
aviso.TextScaled = true
aviso.Font = Enum.Font.GothamBold

-- Função copiar link
getKeyButton.MouseButton1Click:Connect(function()
	local link = "https://link-target.net/1388004/Da9kbuUgS09R"
	
	if setclipboard then
		setclipboard(link)
		aviso.Text = "LINK COPIADO COM SUCESSO ✅"
	else
		aviso.Text = "Seu executor não suporta cópia ❌"
	end
	
	wait(3)
	aviso.Text = ""
end)
