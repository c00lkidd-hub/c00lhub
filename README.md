-- Gui to Lua
-- Version: 3.2

-- Instances:

local MadeByenthony_50388 = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local blocs = Instance.new("TextButton")
local spin = Instance.new("TextButton")
local terrorMod = Instance.new("TextButton")
local music = Instance.new("TextButton")
local Particules = Instance.new("TextButton")
local made = Instance.new("TextLabel")
local decalskybox = Instance.new("TextButton")
local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")

--Properties:

MadeByenthony_50388.Name = "MadeBy@enthony_50388"
MadeByenthony_50388.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
MadeByenthony_50388.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = MadeByenthony_50388
Frame.BackgroundColor3 = Color3.fromRGB(66, 66, 66)
Frame.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0.703609884, 0, 0.735001028, 0)
Frame.Size = UDim2.new(0, 468, 0, 250)

blocs.Name = "blocs"
blocs.Parent = Frame
blocs.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
blocs.BorderColor3 = Color3.fromRGB(0, 0, 0)
blocs.BorderSizePixel = 3
blocs.Position = UDim2.new(0.02991453, 0, 0.786811471, 0)
blocs.Size = UDim2.new(0, 200, 0, 50)
blocs.Font = Enum.Font.SourceSans
blocs.Text = "blocks"
blocs.TextColor3 = Color3.fromRGB(0, 0, 0)
blocs.TextSize = 14.000
blocs.MouseButton1Down:Connect(function()
	local spawnHeight = 1000  -- Altura onde os blocos aparecem
	local fallInterval = 0.1    -- Intervalo entre cada bloco cair (segundos)
	local spawnRange = 5000     -- Distância horizontal máxima para spawn
	local despawnTime = 10    -- Tempo até os blocos desaparecerem (segundos)

	function spawnBlock()
		local sizeFactor = math.random(10, 20) -- Aumenta o tamanho geral dos blocos
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

spin.Name = "spin"
spin.Parent = Frame
spin.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
spin.BorderColor3 = Color3.fromRGB(0, 0, 0)
spin.BorderSizePixel = 3
spin.Position = UDim2.new(0.552912235, 0, 0.786811471, 0)
spin.Size = UDim2.new(0, 200, 0, 50)
spin.Font = Enum.Font.SourceSans
spin.Text = "spin workspace"
spin.TextColor3 = Color3.fromRGB(0, 0, 0)
spin.TextSize = 14.000
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
terrorMod.Parent = Frame
terrorMod.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
terrorMod.BorderColor3 = Color3.fromRGB(0, 0, 0)
terrorMod.BorderSizePixel = 3
terrorMod.Position = UDim2.new(0.02991453, 0, 0.549504936, 0)
terrorMod.Size = UDim2.new(0, 200, 0, 50)
terrorMod.Font = Enum.Font.SourceSans
terrorMod.Text = "terrorMod"
terrorMod.TextColor3 = Color3.fromRGB(0, 0, 0)
terrorMod.TextSize = 14.000
terrorMod.MouseButton1Down:Connect(function()
	local lighting = game:GetService("Lighting")

	-- Remove qualquer Skybox existente
	for _, obj in pairs(lighting:GetChildren()) do
		if obj:IsA("Sky") then
			obj:Destroy()
		end
	end

	-- Criar uma nova Skybox sombria
	local sky = Instance.new("Sky")
	sky.SkyboxBk = "rbxassetid://510093024" -- Fundo escuro
	sky.SkyboxDn = "rbxassetid://510093024"
	sky.SkyboxFt = "rbxassetid://510093024"
	sky.SkyboxLf = "rbxassetid://510093024"
	sky.SkyboxRt = "rbxassetid://510093024"
	sky.SkyboxUp = "rbxassetid://510093024"
	sky.Parent = lighting

	-- Configuração de iluminação para terror
	lighting.Ambient = Color3.fromRGB(30, 0, 0) -- Luz avermelhada fraca
	lighting.OutdoorAmbient = Color3.fromRGB(10, 10, 10) -- Luz externa escura
	lighting.Brightness = 0.3 -- Reduz o brilho
	lighting.FogColor = Color3.fromRGB(10, 10, 10) -- Neblina escura
	lighting.FogStart = 10
	lighting.FogEnd = 100 -- Neblina densa para visibilidade baixa
	lighting.ClockTime = 0 -- Noite profunda
	lighting.GlobalShadows = true -- Sombras realistas
	lighting.Technology = Enum.Technology.Compatibility -- Efeito de sombra mais escuro

	-- Adicionar um efeito de névoa com Atmosphere
	local atmosphere = Instance.new("Atmosphere")
	atmosphere.Density = 0.5 -- Mais neblina
	atmosphere.Offset = 0
	atmosphere.Color = Color3.fromRGB(50, 50, 50) -- Cinza escuro
	atmosphere.Decay = Color3.fromRGB(10, 0, 0) -- Efeito avermelhado na distância
	atmosphere.Glare = 0
	atmosphere.Haze = 3
	atmosphere.Parent = lighting

	print("Modo terror ativado!")
end)

music.Name = "music"
music.Parent = Frame
music.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
music.BorderColor3 = Color3.fromRGB(0, 0, 0)
music.BorderSizePixel = 3
music.Position = UDim2.new(0.551282048, 0, 0.549504936, 0)
music.Size = UDim2.new(0, 200, 0, 50)
music.Font = Enum.Font.SourceSans
music.Text = "music"
music.TextColor3 = Color3.fromRGB(0, 0, 0)
music.TextSize = 14.000
music.MouseButton1Down:Connect(function()
	local soundId = "rbxassetid://142376088" -- ID da música (troque por outro se quiser)
	local volume = 1 -- Volume da música

	-- Função para remover todas as músicas existentes
	local function removeExistingMusic()
		for _, obj in pairs(game.Workspace:GetDescendants()) do
			if obj:IsA("Sound") then
				obj:Destroy()
			end
		end
	end

	-- Função para impedir novas músicas
	local function blockNewMusic()
		game.Workspace.DescendantAdded:Connect(function(obj)
			if obj:IsA("Sound") and obj.SoundId ~= "rbxassetid://142376088" .. soundId then
				obj:Destroy()
				warn("Uma música não autorizada foi removida!")
			end
		end)
	end

	-- Criar e tocar a música oficial
	local function playMainMusic()
		local sound = Instance.new("Sound")
		sound.SoundId = soundId
		sound.Looped = true
		sound.Volume = volume
		sound.Parent = game.Workspace
		sound:Play()
	end

	-- Executa as funções
	removeExistingMusic()
	blockNewMusic()
	playMainMusic()

	print("Música oficial adicionada e músicas não autorizadas bloqueadas!")
end)

Particules.Name = "Particules"
Particules.Parent = Frame
Particules.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
Particules.BorderColor3 = Color3.fromRGB(0, 0, 0)
Particules.BorderSizePixel = 3
Particules.Position = UDim2.new(0.02991453, 0, 0.296706796, 0)
Particules.Size = UDim2.new(0, 200, 0, 50)
Particules.Font = Enum.Font.SourceSans
Particules.Text = "particules"
Particules.TextColor3 = Color3.fromRGB(0, 0, 0)
Particules.TextSize = 14.000
Particules.MouseButton1Down:Connect(function()
	local function addParticlesToPart(part)
		-- Verifica se a peça já tem um ParticleEmitter para evitar duplicação
		if not part:FindFirstChild("ParticleEmitter") then
			local particle = Instance.new("ParticleEmitter")
			particle.Texture = "rbxassetid://258128463" -- ID da textura fornecida
			particle.Rate = 100 -- Quantidade de partículas emitidas por segundo
			particle.Lifetime = NumberRange.new(2, 2) -- Tempo de vida das partículas
			particle.Speed = NumberRange.new(5, 5) -- Velocidade das partículas
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

made.Name = "made"
made.Parent = Frame
made.BackgroundColor3 = Color3.fromRGB(0, 0, 127)
made.BorderColor3 = Color3.fromRGB(0, 0, 0)
made.BorderSizePixel = 0
made.Size = UDim2.new(0, 467, 0, 50)
made.Font = Enum.Font.Unknown
made.Text = "c00lhub Made by @enthony_50388"
made.TextColor3 = Color3.fromRGB(255, 255, 255)
made.TextScaled = true
made.TextSize = 14.000
made.TextWrapped = true

decalskybox.Name = "decal/skybox"
decalskybox.Parent = Frame
decalskybox.BackgroundColor3 = Color3.fromRGB(0, 85, 255)
decalskybox.BorderColor3 = Color3.fromRGB(0, 0, 0)
decalskybox.BorderSizePixel = 3
decalskybox.Position = UDim2.new(0.551282048, 0, 0.296706796, 0)
decalskybox.Size = UDim2.new(0, 200, 0, 50)
decalskybox.Font = Enum.Font.SourceSans
decalskybox.Text = "decal and skybox"
decalskybox.TextColor3 = Color3.fromRGB(0, 0, 0)
decalskybox.TextSize = 14.000
decalskybox.MouseButton1Down:Connect(function()
	local lighting = game:GetService("Lighting")
	local workspace = game:GetService("Workspace")

	-- Função para alterar a textura da Skybox
	local function changeSkyboxTexture()
		-- Verifica se já existe uma Skybox configurada
		if not lighting:FindFirstChild("Skybox") then
			-- Cria uma nova Skybox se não existir
			local skybox = Instance.new("Sky")
			skybox.Name = "Skybox"
			skybox.Parent = lighting
		end

		-- Altera a textura da Skybox para um ID desejado (substitua pelo ID que preferir)
		lighting.Sky.SkyboxId = "rbxassetid://158118263"  -- Substitua com o seu ID de textura

		-- Impede mudanças futuras na Skybox
		lighting:GetPropertyChangedSignal("Sky"):Connect(function()
			lighting.Sky.SkyboxId = "rbxassetid://158118263"  -- Restabelece a Skybox original
		end)
	end

	-- Função para criar o decal nas Parts
	local function createDecal(part)
		if part:IsA("Part") and not part:FindFirstChildOfClass("Decal") then
			local decal = Instance.new("Decal")
			decal.Name = "Decal"
			decal.Texture = "rbxassetid://158118263"  -- Substitua pelo ID da sua textura
			decal.Parent = part
		end
	end

	-- Cria Decals em todas as Parts existentes no Workspace
	for _, part in pairs(workspace:GetDescendants()) do
		createDecal(part)
	end

	-- Impede a criação ou modificação de Decals no futuro
	workspace.DescendantAdded:Connect(function(obj)
		if obj:IsA("Part") then
			-- Impede que novos Decals sejam criados
			obj.ChildAdded:Connect(function(child)
				if child:IsA("Decal") then
					child:Destroy()  -- Remove Decal assim que é criada
					warn("Tentativa de criar Decal removida!")
				end
			end)
		end
	end)

	-- Impede a modificação dos Decals existentes
	for _, part in pairs(workspace:GetDescendants()) do
		if part:IsA("Part") then
			local decal = part:FindFirstChildOfClass("Decal")
			if decal then
				decal:GetPropertyChangedSignal("Texture"):Connect(function()
					decal.Texture = "rbxassetid://158118263"  -- Restaura a textura original
				end)
			end
		end
	end

	-- Chama a função para mudar a textura da Skybox
	changeSkyboxTexture()

	print("Skybox alterada, Decals criadas e proteção contra alterações ativada!")
end)

UIAspectRatioConstraint.Parent = MadeByenthony_50388
UIAspectRatioConstraint.AspectRatio = 1.674
