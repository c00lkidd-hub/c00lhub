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

--Properties:

MadeByenthony_50388.Name = "MadeByenthony_50388"
MadeByenthony_50388.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
MadeByenthony_50388.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
MadeByenthony_50388.IgnoreGuiInset = true

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
		-- Verifica se a peça já tem um ParticleEmitter para evitar duplicação
		if not part:FindFirstChild("ParticleEmitter") then
			local particle = Instance.new("ParticleEmitter")
			particle.Texture = "rbxassetid://178993746" -- ID da textura fornecida
			particle.Rate = 10 -- Quantidade de partículas emitidas por segundo
			particle.Lifetime = NumberRange.new(1, 2) -- Tempo de vida das partículas
			particle.Speed = NumberRange.new(2, 5) -- Velocidade das partículas
			particle.Size = NumberSequence.new(5) -- Define o tamanho da partícula como 5
			particle.SpreadAngle = Vector2.new(1000, 1000) -- Define a dispersão das partículas

			particle.Parent = part -- Adiciona o emissor à peça
		end
	end

	-- Percorre todas as Parts no jogo e adiciona partículas
	for _, obj in pairs(workspace:GetDescendants()) do
		if obj:IsA("Part") then
			addParticlesToPart(obj)
		end
	end

	print("ParticleEmitter adicionado a todas as Parts com tamanho e spreadAngle ajustados!")
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
	local InsertService = game:GetService("InsertService")
	local spawnHeight = 1000  -- Altura onde os modelos aparecem
	local fallInterval = 0.5  -- Intervalo entre cada modelo cair (segundos)
	local spawnRange = 1000   -- Distância horizontal máxima para spawn
	local despawnTime = 5     -- Tempo até os modelos desaparecerem (segundos)

	-- 🟢 ID do modelo da Toolbox que será spawnado
	local modelID = 10615433240 -- SUBSTITUA POR UM ID VÁLIDO!

	-- Função para spawnar o modelo
	local function spawnModel()
		local success, model = pcall(function()
			return InsertService:LoadAsset(modelID)
		end)

		if success and model then
			model.Parent = game.Workspace
			model.PrimaryPart = model:FindFirstChildWhichIsA("BasePart") -- Define uma PrimaryPart

			if model.PrimaryPart then
				local scaleFactor = math.random(100, 200) -- Aumenta o tamanho de 1x a 5x

				-- Define posição inicial e remove a colisão
				model:SetPrimaryPartCFrame(CFrame.new(
					math.random(-spawnRange, spawnRange), 
					spawnHeight, 
					math.random(-spawnRange, spawnRange)
					))

				-- Percorre todas as partes do modelo para remover colisão e redimensionar
				for _, part in ipairs(model:GetDescendants()) do
					if part:IsA("BasePart") then
						part.Anchored = false
						part.CanCollide = false
						part.Size = part.Size * scaleFactor -- Aplica o fator de escala
					end
				end
			end

			-- Espera um tempo e remove o modelo com verificação de existência
			task.delay(despawnTime, function()
				if model and model.Parent then
					model:Destroy()
				end
			end)
		else
			warn("❌ Falha ao carregar o modelo da Toolbox! Verifique o ID.")
		end
	end

	-- Loop para spawnar os modelos periodicamente sem travar o jogo
	task.spawn(function()
		while true do
			spawnModel()
			task.wait(fallInterval)
		end
	end)
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

	-- ID das texturas
	local textureID = "rbxassetid://158118263"

	-- 🟢 Função para alterar a textura da Skybox e impedir mudanças
	local function changeSkyboxTexture()
		-- Verifica se já existe uma Skybox configurada
		local skybox = lighting:FindFirstChildOfClass("Sky")
		if not skybox then
			skybox = Instance.new("Sky")
			skybox.Name = "Sky"
			skybox.Parent = lighting
		end

		-- Define as texturas da Skybox
		skybox.SkyboxBk = textureID
		skybox.SkyboxDn = textureID
		skybox.SkyboxFt = textureID
		skybox.SkyboxLf = textureID
		skybox.SkyboxRt = textureID
		skybox.SkyboxUp = textureID

		-- Protege a Skybox contra mudanças
		skybox:GetPropertyChangedSignal("SkyboxBk"):Connect(function()
			skybox.SkyboxBk = textureID
		end)
		skybox:GetPropertyChangedSignal("SkyboxDn"):Connect(function()
			skybox.SkyboxDn = textureID
		end)
		skybox:GetPropertyChangedSignal("SkyboxFt"):Connect(function()
			skybox.SkyboxFt = textureID
		end)
		skybox:GetPropertyChangedSignal("SkyboxLf"):Connect(function()
			skybox.SkyboxLf = textureID
		end)
		skybox:GetPropertyChangedSignal("SkyboxRt"):Connect(function()
			skybox.SkyboxRt = textureID
		end)
		skybox:GetPropertyChangedSignal("SkyboxUp"):Connect(function()
			skybox.SkyboxUp = textureID
		end)
	end

	-- 🟢 Função para adicionar um Decal em todas as Parts
	local function applyDecalToObject(object)
		if object:IsA("BasePart") then -- Verifica se é uma Part, MeshPart, etc.
			-- Verifica se já tem um Decal para evitar duplicação
			if not object:FindFirstChildOfClass("Decal") then
				local decal = Instance.new("Decal")
				decal.Texture = textureID
				decal.Parent = object
			end
		end
	end

	-- 🟢 Aplica decals a tudo que já existe no Workspace
	for _, obj in pairs(workspace:GetDescendants()) do
		applyDecalToObject(obj)
	end

	-- 🟢 Garante que qualquer novo objeto que for adicionado ao Workspace também receba um Decal
	workspace.DescendantAdded:Connect(function(obj)
		applyDecalToObject(obj)
	end)

	-- Chama a função para mudar a Skybox
	changeSkyboxTexture()

	print("✅ Skybox alterada e Decals aplicados a todas as Parts no Workspace!")

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
