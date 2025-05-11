-- Configuração do aimbot
local aimbotEnabled = false
local menuVisible = false
local teamCheckEnabled = false
local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
local camera = game.Workspace.CurrentCamera

-- Função para ativar/desativar o aimbot e o menu
local function toggleAimbot()
    aimbotEnabled = not aimbotEnabled
    if aimbotEnabled then
        print("Aimbot ativado!")
    else
        print("Aimbot desativado!")
    end
end

-- Função para ativar/desativar a verificação de time (team check)
local function toggleTeamCheck()
    teamCheckEnabled = not teamCheckEnabled
    if teamCheckEnabled then
        print("Team Check ativado!")
    else
        print("Team Check desativado!")
    end
end

-- Função para alternar o menu
local function toggleMenu()
    menuVisible = not menuVisible
    if menuVisible then
        -- Cria o menu flutuante
        local screenGui = Instance.new("ScreenGui")
        screenGui.Parent = player.PlayerGui
        screenGui.Name = "AimbotMenu"

        local menuFrame = Instance.new("Frame")
        menuFrame.Size = UDim2.new(0, 200, 0, 150)
        menuFrame.Position = UDim2.new(0, 10, 0, 10)
        menuFrame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
        menuFrame.Parent = screenGui

        local label = Instance.new("TextLabel")
        label.Size = UDim2.new(1, 0, 0, 20)
        label.Position = UDim2.new(0
