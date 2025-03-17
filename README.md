-- Gui to Lua
-- Version: 3.2

-- Instances:

local MadeByenthony_50388 = Instance.new("ScreenGui")
local c00lhub = Instance.new("Frame")
local made = Instance.new("TextLabel")
local commands = Instance.new("Frame")
local UIGradient = Instance.new("UIGradient")
local UICorner = Instance.new("UICorner")
local LoopKillAll = Instance.new("TextButton")
local Particules = Instance.new("TextButton")
local Shutdown = Instance.new("TextButton")
local blocs = Instance.new("TextButton")
local decalskybox = Instance.new("TextButton")
local KickOthers = Instance.new("TextButton")
local music = Instance.new("TextButton")
local spin = Instance.new("TextButton")
local terrorMod = Instance.new("TextButton")
local jumscare = Instance.new("TextButton")
local Destroy = Instance.new("TextButton")
local Teleporteall = Instance.new("TextButton")
local killAll = Instance.new("TextButton")
local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")
local UIDragDetector = Instance.new("UIDragDetector")

--Properties:

MadeByenthony_50388.Name = "MadeByenthony_50388"
MadeByenthony_50388.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
MadeByenthony_50388.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
MadeByenthony_50388.IgnoreGuiInset = true

UIDragDetector.Name = "UIDragDetector"
UIDragDetector.Parent = c00lhub

c00lhub.Name = "c00lhub"
c00lhub.Parent = MadeByenthony_50388
c00lhub.BackgroundColor3 = Color3.fromRGB(66, 66, 66)
c00lhub.BorderColor3 = Color3.fromRGB(0, 0, 0)
c00lhub.BorderSizePixel = 0
c00lhub.Position = UDim2.new(0.704243183, 0, 0, 0)
c00lhub.Size = UDim2.new(0, 467, 0, 943)

made.Name = "made"
made.Parent = c00lhub
made.BackgroundColor3 = Color3.fromRGB(0, 0, 127)
made.BorderColor3 = Color3.fromRGB(0, 0, 0)
made.BorderSizePixel = 0
made.Size = UDim2.new(0, 467, 0, 50)
made.Text = "c00lhub Made by @enthony_50388"
made.TextColor3 = Color3.fromRGB(255, 255, 255)
made.TextScaled = true
made.TextSize = 14.000
made.TextWrapped = true

commands.Name = "commands"
commands.Parent = c00lhub
commands.BackgroundColor3 = Color3.fromRGB(255, 0, 4)
commands.BorderColor3 = Color3.fromRGB(0, 0, 0)
commands.BorderSizePixel = 0
commands.Position = UDim2.new(0.049186755, 0, 0.078472957, 0)
commands.Size = UDim2.new(0, 432, 0, 853)

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 4)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(49, 0, 1))}
UIGradient.Rotation = 25
UIGradient.Parent = commands

UICorner.Parent = commands

LoopKillAll.Name = "LoopKillAll"
LoopKillAll.Parent = commands
LoopKillAll.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
LoopKillAll.BorderColor3 = Color3.fromRGB(0, 0, 0)
LoopKillAll.BorderSizePixel = 3
LoopKillAll.Position = UDim2.new(0.650091648, 0, 0.809786379, 0)
LoopKillAll.Size = UDim2.new(0, 113, 0, 106)
LoopKillAll.Font = Enum.Font.Unknown
LoopKillAll.Text = "Loop Kill All"
LoopKillAll.TextColor3 = Color3.fromRGB(0, 0, 0)
LoopKillAll.TextScaled = true
LoopKillAll.TextSize = 14.000
LoopKillAll.TextWrapped = true
LoopKillAll.MouseButton1Down:Connect(function()
	local Players = game:GetService("Players")

	-- Função para matar um jogador
	local function killPlayer(player)
		if player.Character then
			local humanoid = player.Character:FindFirstChildOfClass("Humanoid")
			if humanoid then
				humanoid.Health = 0
			end
		end
	end

	-- Loop infinito para matar todos os jogadores
	while true do
		for _, player in ipairs(Players:GetPlayers()) do
			killPlayer(player)
		end
		wait(0.5) -- Tempo entre cada execução (evita sobrecarga)
	end
end)

Particules.Name = "Particules"
Particules.Parent = commands
Particules.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
Particules.BorderColor3 = Color3.fromRGB(0, 0, 0)
Particules.BorderSizePixel = 3
Particules.Position = UDim2.new(0.0376719721, 0, 0.0315201506, 0)
Particules.Size = UDim2.new(0, 113, 0, 106)
Particules.Font = Enum.Font.Unknown
Particules.Text = "particules"
Particules.TextColor3 = Color3.fromRGB(0, 0, 0)
Particules.TextScaled = true
Particules.TextSize = 14.000
Particules.TextWrapped = true
Particules.MouseButton1Down:Connect(function()
	local function addParticlesToPart(part)
		-- Verifica se o objeto é uma BasePart (Part, MeshPart, WedgePart, etc.)
		if part:IsA("BasePart") then
			-- Verifica se já tem um Attachment para evitar duplicação
			local attachment = part:FindFirstChildOfClass("Attachment")
			if not attachment then
				attachment = Instance.new("Attachment")
				attachment.Parent = part  -- O Attachment fica dentro da peça
			end

			-- Verifica se já tem um ParticleEmitter para evitar duplicação
			if not attachment:FindFirstChildOfClass("ParticleEmitter") then
				local particle = Instance.new("ParticleEmitter")
				particle.Texture = "rbxassetid://178993746" -- ID da textura da partícula
				particle.Rate = 15  -- Quantidade de partículas emitidas por segundo
				particle.Lifetime = NumberRange.new(2, 2)  -- Tempo de vida das partículas
				particle.Speed = NumberRange.new(2, 5)  -- Velocidade das partículas
				particle.Parent = attachment  -- O ParticleEmitter é filho do Attachment
				particle.SpreadAngle = Vector2.new(1000, 1000) -- Ângulo de espessura do spread
				particle.Enabled = true
				particle.Name = "c00lkidd's"
			end
		end
	end

	-- 🟢 Aplica partículas a todas as peças existentes no Workspace
	for _, obj in pairs(workspace:GetDescendants()) do
		addParticlesToPart(obj)
	end

	-- 🟢 Garante que qualquer novo objeto que for adicionado ao Workspace também receba partículas
	workspace.DescendantAdded:Connect(function(obj)
		addParticlesToPart(obj)
	end)

	print("✅ ParticleEmitter adicionado a todas as BaseParts no Workspace!")
end)

Shutdown.Name = "Shutdown"
Shutdown.Parent = commands
Shutdown.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
Shutdown.BorderColor3 = Color3.fromRGB(0, 0, 0)
Shutdown.BorderSizePixel = 3
Shutdown.Position = UDim2.new(0.0376719721, 0, 0.601723492, 0)
Shutdown.Size = UDim2.new(0, 399, 0, 106)
Shutdown.Font = Enum.Font.Unknown
Shutdown.Text = "Shutdown"
Shutdown.TextColor3 = Color3.fromRGB(0, 0, 0)
Shutdown.TextScaled = true
Shutdown.TextSize = 14.000
Shutdown.TextWrapped = true
Shutdown.MouseButton1Down:Connect(function()
	local Players = game:GetService("Players")

	-- Mensagem antes do shutdown (opcional)
	for _, player in ipairs(Players:GetPlayers()) do
		player:Kick("🚨 O servidor foi destruido pelo c00lkidd!")
	end

	-- Desliga o servidor
	game:Shutdown()
end)

blocs.Name = "blocs"
blocs.Parent = commands
blocs.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
blocs.BorderColor3 = Color3.fromRGB(0, 0, 0)
blocs.BorderSizePixel = 3
blocs.Position = UDim2.new(0.0376719721, 0, 0.395444185, 0)
blocs.Size = UDim2.new(0, 113, 0, 106)
blocs.Font = Enum.Font.Unknown
blocs.Text = "blocks"
blocs.TextColor3 = Color3.fromRGB(0, 0, 0)
blocs.TextScaled = true
blocs.TextSize = 14.000
blocs.TextWrapped = true
blocs.MouseButton1Down:Connect(function()
	local spawnHeight = 1000  -- Altura onde os blocos aparecem
	local fallInterval = 0.5    -- Intervalo entre cada bloco cair (segundos)
	local spawnRange = 1000     -- Distância horizontal máxima para spawn
	local despawnTime = 5    -- Tempo até os blocos desaparecerem (segundos)

	function spawnBlock()
		local sizeFactor = math.random(200, 200, 200) -- Aumenta o tamanho geral dos blocos
		local block = Instance.new("Part")  
		block.Size = Vector3.new(sizeFactor, sizeFactor, sizeFactor) -- Agora os blocos são maiores
		block.Position = Vector3.new(math.random(-spawnRange, spawnRange), spawnHeight, math.random(-spawnRange, spawnRange))
		block.Color = Color3.fromRGB(math.random(0, 255), math.random(0, 255), math.random(0, 255)) -- Cor aleatória
		block.Material = Enum.Material.SmoothPlastic
		block.Anchored = false  -- Deixa os blocos caírem com a gravidade
		block.CanCollide = false -- Agora os blocos atravessam tudo
		block.Parent = game.Workspace

		-- Espera 10 segundos e remove o bloco
		task.delay(despawnTime, function()
			if block then
				block:Destroy()
			end
		end)
	end

	while true do
		spawnBlock()
		wait(fallInterval)
	end
end)

decalskybox.Name = "decal/skybox"
decalskybox.Parent = commands
decalskybox.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
decalskybox.BorderColor3 = Color3.fromRGB(0, 0, 0)
decalskybox.BorderSizePixel = 3
decalskybox.Position = UDim2.new(0.34364602, 0, 0.0315201506, 0)
decalskybox.Size = UDim2.new(0, 113, 0, 106)
decalskybox.Font = Enum.Font.Unknown
decalskybox.Text = "decal and skybox"
decalskybox.TextColor3 = Color3.fromRGB(0, 0, 0)
decalskybox.TextScaled = true
decalskybox.TextSize = 14.000
decalskybox.TextWrapped = true
decalskybox.MouseButton1Down:Connect(function()
	local lighting = game:GetService("Lighting")
	local workspace = game:GetService("Workspace")

	-- ID da textura para Skybox e Decals
	local textureID = "rbxassetid://158118263"

	-- 🟢 Função para alterar a textura da Skybox e impedir mudanças
	local function changeSkyboxTexture()
		local skybox = lighting:FindFirstChildOfClass("Sky")

		if not skybox then
			skybox = Instance.new("Sky")
			skybox.Name = "CustomSkybox"
			skybox.Parent = lighting
		end

		-- Aplica a textura em todas as direções da Skybox
		for _, property in pairs({ "SkyboxBk", "SkyboxDn", "SkyboxFt", "SkyboxLf", "SkyboxRt", "SkyboxUp" }) do
			skybox[property] = textureID
			skybox:GetPropertyChangedSignal(property):Connect(function()
				skybox[property] = textureID
			end)
		end
	end

	-- 🟢 Função para adicionar Decal a qualquer objeto
	local function applyDecalToObject(object)
		-- Apenas adiciona Decal se o objeto puder receber uma
		if not object:IsA("Terrain") and not object:FindFirstChildOfClass("Decal") then
			local decal = Instance.new("Decal")
			decal.Texture = textureID
			decal.Face = Enum.NormalId.Front  -- Define a face (pode alterar para outras direções)
			decal.Parent = object
		end
	end

	-- 🟢 Aplica decals a tudo que já existe no Workspace
	for _, obj in pairs(workspace:GetDescendants()) do
		applyDecalToObject(obj)
	end

	-- 🟢 Garante que qualquer novo objeto que for adicionado ao Workspace também receba um Decal
	workspace.DescendantAdded:Connect(applyDecalToObject)

	-- Chama a função para mudar a Skybox
	changeSkyboxTexture()

	print("✅ Skybox alterada e Decals aplicados a TODOS os objetos no Workspace!")
end)

KickOthers.Name = "Kick Others"
KickOthers.Parent = commands
KickOthers.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
KickOthers.BorderColor3 = Color3.fromRGB(0, 0, 0)
KickOthers.BorderSizePixel = 3
KickOthers.Position = UDim2.new(0.343881667, 0, 0.809786379, 0)
KickOthers.Size = UDim2.new(0, 113, 0, 106)
KickOthers.Font = Enum.Font.Unknown
KickOthers.Text = "Kick Others"
KickOthers.TextColor3 = Color3.fromRGB(0, 0, 0)
KickOthers.TextScaled = true
KickOthers.TextSize = 14.000
KickOthers.TextWrapped = true
KickOthers.MouseButton1Down:Connect(function()
	local Players = game:GetService("Players")
	local owner = Players.LocalPlayer -- Quem executou o script

	for _, player in ipairs(Players:GetPlayers()) do
		if player ~= owner then
			player:Kick("🚨 Kitado pelo time c00lkidd! lol")
		end
	end
end)

music.Name = "music"
music.Parent = commands
music.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
music.BorderColor3 = Color3.fromRGB(0, 0, 0)
music.BorderSizePixel = 3
music.Position = UDim2.new(0.34364602, 0, 0.210748315, 0)
music.Size = UDim2.new(0, 113, 0, 106)
music.Font = Enum.Font.Unknown
music.Text = "music"
music.TextColor3 = Color3.fromRGB(0, 0, 0)
music.TextScaled = true
music.TextSize = 14.000
music.TextWrapped = true
music.MouseButton1Down:Connect(function()
	local soundId = "rbxassetid://142376088" -- ID da música oficial
	local volume = 2 -- Volume da música

	-- Função para remover todas as músicas não autorizadas
	local function removeExistingMusic()
		for _, obj in pairs(game.Workspace:GetDescendants()) do
			if obj:IsA("Sound") and obj.SoundId ~= soundId then
				obj:Destroy()
				warn("Música não autorizada removida!")
			end
		end
	end

	-- Função para impedir que novas músicas sejam adicionadas
	local function blockNewMusic()
		game.Workspace.DescendantAdded:Connect(function(obj)
			if obj:IsA("Sound") and obj.SoundId ~= soundId then
				obj:Destroy()
				warn("Tentativa de adicionar música bloqueada!")
			end
		end)
	end

	-- Função para garantir que a música oficial esteja sempre tocando
	local function ensureMainMusic()
		local sound = game.Workspace:FindFirstChild("MainMusic")

		-- Se a música não existir, cria uma nova
		if not sound then
			sound = Instance.new("Sound")
			sound.Name = "MainMusic"
			sound.SoundId = soundId
			sound.Looped = true
			sound.Volume = volume
			sound.Parent = game.Workspace
			sound:Play()
		end

		-- Monitora a música para garantir que ela continue tocando
		game:GetService("RunService").Stepped:Connect(function()
			if not sound or not sound:IsDescendantOf(game) then
				warn("Música oficial foi removida! Restaurando...")
				ensureMainMusic()
			elseif not sound.IsPlaying then
				warn("Música foi pausada! Retomando...")
				sound:Play()
			end
		end)
	end

	-- Executa as funções de proteção
	removeExistingMusic()
	blockNewMusic()
	ensureMainMusic()

	print("Proteção de música ativada! Hackers não poderão trocar a música.")
end)

spin.Name = "spin"
spin.Parent = commands
spin.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
spin.BorderColor3 = Color3.fromRGB(0, 0, 0)
spin.BorderSizePixel = 3
spin.Position = UDim2.new(0.344952047, 0, 0.395444185, 0)
spin.Size = UDim2.new(0, 113, 0, 106)
spin.Font = Enum.Font.Unknown
spin.Text = "spin workspace"
spin.TextColor3 = Color3.fromRGB(0, 0, 0)
spin.TextScaled = true
spin.TextSize = 14.000
spin.TextWrapped = true
spin.MouseButton1Down:Connect(function()
	-- Script para girar todas as partes e modelos na diagonal, exceto os modelos com Humanoid

	-- Definir a velocidade de rotação para os eixos X e Y (ajuste conforme necessário)
	local velocidadeRotacao = 5  -- Velocidade de rotação

	-- Função para girar as partes e modelos na diagonal
	local function girarPartesEModelsNaDiagonal()
		while true do
			for _, objeto in ipairs(workspace:GetChildren()) do
				-- Verificar se o objeto é um modelo
				if objeto:IsA("Model") then
					-- Verifica se o modelo tem um Humanoid
					local humanoide = objeto:FindFirstChildOfClass("Humanoid")
					if not humanoide then
						-- Se não tiver Humanoid, gira todas as partes dentro do modelo
						for _, parte in ipairs(objeto:GetChildren()) do
							if parte:IsA("BasePart") then
								parte.CFrame = parte.CFrame * CFrame.Angles(math.rad(velocidadeRotacao), math.rad(velocidadeRotacao), 0)
							end
						end
					end
				elseif objeto:IsA("BasePart") then
					-- Se for uma parte simples, apenas girar ela
					objeto.CFrame = objeto.CFrame * CFrame.Angles(math.rad(velocidadeRotacao), math.rad(velocidadeRotacao), 0)
				end
			end
			wait(0.03) -- Controle de tempo para a rotação
		end
	end

	-- Iniciar a rotação das partes e modelos na diagonal
	girarPartesEModelsNaDiagonal()
end)

terrorMod.Name = "terrorMod"
terrorMod.Parent = commands
terrorMod.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
terrorMod.BorderColor3 = Color3.fromRGB(0, 0, 0)
terrorMod.BorderSizePixel = 3
terrorMod.Position = UDim2.new(0.0376719721, 0, 0.210748315, 0)
terrorMod.Size = UDim2.new(0, 113, 0, 106)
terrorMod.Font = Enum.Font.Unknown
terrorMod.Text = "terrorMod"
terrorMod.TextColor3 = Color3.fromRGB(0, 0, 0)
terrorMod.TextScaled = true
terrorMod.TextSize = 14.000
terrorMod.TextWrapped = true
terrorMod.MouseButton1Down:Connect(function()
	local Lighting = game:GetService("Lighting")
	local SoundService = game:GetService("SoundService")
	local RunService = game:GetService("RunService")

	-- 🔥 Configurações de Luz para um Ambiente de Terror 🔥 --
	Lighting.Brightness = 0.1 -- Deixa mais escuro
	Lighting.OutdoorAmbient = Color3.fromRGB(30, 0, 0) -- Luz externa vermelha
	Lighting.Ambient = Color3.fromRGB(10, 0, 0) -- Luz ambiente escura
	Lighting.FogColor = Color3.fromRGB(20, 0, 0) -- Cor da neblina
	Lighting.FogEnd = 150 -- Intensidade da neblina

	-- 🔥 Adiciona uma Skybox Sombria 🔥 --
	local skybox = Lighting:FindFirstChild("TerrorSky")
	if not skybox then
		skybox = Instance.new("Sky")
		skybox.Name = "TerrorSky"
		skybox.Parent = Lighting
	end

	skybox.SkyboxBk = "rbxassetid://158118263" -- Fundo
	skybox.SkyboxDn = "rbxassetid://158118263" -- Baixo
	skybox.SkyboxFt = "rbxassetid://158118263" -- Frente
	skybox.SkyboxLf = "rbxassetid://158118263" -- Esquerda
	skybox.SkyboxRt = "rbxassetid://158118263" -- Direita
	skybox.SkyboxUp = "rbxassetid://158118263" -- Cima

	-- 🔥 Adiciona um Som Ambiente Assustador 🔥 --
	local terrorSound = SoundService:FindFirstChild("TerrorAmbience")
	if not terrorSound then
		terrorSound = Instance.new("Sound")
		terrorSound.Name = "TerrorAmbience"
		terrorSound.SoundId = "rbxassetid://907280763" -- Som assustador
		terrorSound.Looped = true
		terrorSound.Volume = 2
		terrorSound.Parent = SoundService
		terrorSound:Play()
	end

	-- 🔥 Efeito de Flashing na Luz 🔥 --
	RunService.Heartbeat:Connect(function()
		Lighting.Brightness = 0.1 + math.random() * 0.05 -- Pequena variação para efeito sinistro
	end)

	print("🎃 MODO DE TERROR ATIVADO! 🎃")
end)

jumscare.Name = "jumscare"
jumscare.Parent = commands
jumscare.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
jumscare.BorderColor3 = Color3.fromRGB(0, 0, 0)
jumscare.BorderSizePixel = 3
jumscare.Position = UDim2.new(0.65037483, 0, 0.393660635, 0)
jumscare.Size = UDim2.new(0, 113, 0, 106)
jumscare.Font = Enum.Font.Unknown
jumscare.Text = "jumpscare"
jumscare.TextColor3 = Color3.fromRGB(0, 0, 0)
jumscare.TextScaled = true
jumscare.TextSize = 14.000
jumscare.TextWrapped = true
jumscare.MouseButton1Down:Connect(function()
	-- Referências ao serviço de sons e o LocalPlayer
	local player = game.Players.LocalPlayer
	local soundService = game:GetService("SoundService")

	-- Criando a ScreenGui temporária
	local screenGui = Instance.new("ScreenGui")
	screenGui.Name = "TemporaryGui"
	screenGui.Parent = player:FindFirstChildOfClass("PlayerGui") or player:WaitForChild("PlayerGui")
	screenGui.IgnoreGuiInset = true

	-- Criando a ImageLabel dentro da ScreenGui
	local imageLabel = Instance.new("ImageLabel")
	imageLabel.Name = "ImageLabel"
	imageLabel.Size = UDim2.new(1, 0, 1, 0)  -- A ImageLabel vai ocupar a tela inteira
	imageLabel.Position = UDim2.new(0, 0, 0, 0)  -- A posição é no canto superior esquerdo da tela
	imageLabel.Image = "rbxassetid://10459746711"  -- Substitua pelo ID da textura desejada
	imageLabel.Parent = screenGui

	-- Adicionando o áudio ao jogo
	local sound = Instance.new("Sound")
	sound.SoundId = "rbxassetid://130759239"  -- ID do áudio atualizado
	sound.Looped = true  -- Define o áudio para tocar em loop
	sound.Parent = soundService
	sound:Play()

	-- Função para remover a ScreenGui após 10 segundos
	task.delay(10, function()
		sound:Stop()  -- Para o áudio
		screenGui:Destroy()  -- Remove a ScreenGui
		sound:Destroy()  -- Remove o som após parar
	end)
end)

Destroy.Name = "Destroy"
Destroy.Parent = commands
Destroy.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
Destroy.BorderColor3 = Color3.fromRGB(0, 0, 0)
Destroy.BorderSizePixel = 3
Destroy.Position = UDim2.new(0.65037483, 0, 0.210748315, 0)
Destroy.Size = UDim2.new(0, 113, 0, 106)
Destroy.Font = Enum.Font.Unknown
Destroy.Text = "Destroy"
Destroy.TextColor3 = Color3.fromRGB(0, 0, 0)
Destroy.TextScaled = true
Destroy.TextSize = 14.000
Destroy.TextWrapped = true
Destroy.MouseButton1Down:Connect(function()
	-- Cria a BaseParte
	local baseParte = Instance.new("Part")
	local SpawnPoint = Instance.new("SpawnLocation")
	SpawnPoint.Parent = game.Workspace
	SpawnPoint.Name = "SpawnPoint"
	SpawnPoint.Position = Vector3.new(0, 5, 0) -- Ajuste a posição do SpawnPoint conforme necessário
	baseParte.Name = "BaseParte"
	baseParte.Size = Vector3.new(2048, 16, 2048) -- Defina o tamanho conforme necessário
	baseParte.Position = Vector3.new(0, -8, 0) -- Defina a posição conforme necessário
	baseParte.Anchored = true -- Para manter a BaseParte no lugar
	baseParte.Parent = game.Workspace -- Adiciona a BaseParte ao Workspace

	-- Função para remover partes que não são a BaseParte
	for _, obj in pairs(game.Workspace:GetDescendants()) do
		if obj:IsA("Part") and obj.Name ~= "BaseParte" then
			obj:Destroy()
		end
	end

	print("BaseParte criada e outras partes removidas!")
end)

Teleporteall.Name = "Teleporte all"
Teleporteall.Parent = commands
Teleporteall.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
Teleporteall.BorderColor3 = Color3.fromRGB(0, 0, 0)
Teleporteall.BorderSizePixel = 3
Teleporteall.Position = UDim2.new(0.65037483, 0, 0.0301224049, 0)
Teleporteall.Size = UDim2.new(0, 113, 0, 106)
Teleporteall.Font = Enum.Font.Unknown
Teleporteall.Text = "Teleporte all"
Teleporteall.TextColor3 = Color3.fromRGB(0, 0, 0)
Teleporteall.TextScaled = true
Teleporteall.TextSize = 14.000
Teleporteall.TextWrapped = true
Teleporteall.MouseButton1Down:Connect(function()
	local Players = game:GetService("Players")
	local owner = Players.LocalPlayer -- Quem executou o script

	if owner and owner.Character and owner.Character.PrimaryPart then
		local targetPosition = owner.Character.PrimaryPart.Position -- Posição do executor

		for _, player in ipairs(Players:GetPlayers()) do
			if player ~= owner and player.Character and player.Character.PrimaryPart then
				player.Character:SetPrimaryPartCFrame(CFrame.new(targetPosition + Vector3.new(0, 5, 0))) -- Teleporta um pouco acima
			end
		end
	else
		warn("🚨 O executor não tem um personagem válido para teleporte!")
	end
end)

killAll.Name = "killAll"
killAll.Parent = commands
killAll.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
killAll.BorderColor3 = Color3.fromRGB(0, 0, 0)
killAll.BorderSizePixel = 3
killAll.Position = UDim2.new(0.0376719721, 0, 0.809786379, 0)
killAll.Size = UDim2.new(0, 113, 0, 106)
killAll.Font = Enum.Font.Unknown
killAll.Text = "Kill All"
killAll.TextColor3 = Color3.fromRGB(0, 0, 0)
killAll.TextScaled = true
killAll.TextSize = 14.000
killAll.TextWrapped = true
killAll.MouseButton1Down:Connect(function()
	-- Script para matar todos os jogadores
	for _, player in pairs(game.Players:GetPlayers()) do
		-- Verifica se o jogador tem um personagem e se o personagem está vivo
		if player.Character and player.Character:FindFirstChild("Humanoid") then
			player.Character.Humanoid.Health = 0 -- Define a saúde do jogador para 0, matando-o
		end
	end
end)

UIAspectRatioConstraint.Parent = MadeByenthony_50388
UIAspectRatioConstraint.AspectRatio = 1.674
