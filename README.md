-- Ella's Decompiler
-- Game: Race Around The World (8147712744)
-- Scripts: 400 passed, 7 failed

==================================================
-- Workspace.Lobby.LavaObby.Sensor.Spleef
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Lobby.LobSecret.Spleef
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Lobby.Center Piece..Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Portal.Cube.001.PortalScript
==================================================
local v_u_1 = game:GetService("RunService")
local v_u_2 = game:GetService("Workspace")
local v_u_3 = script.Parent
local v_u_4 = v_u_3.PortalGui.Portal
local v_u_5 = {}
local function v_u_7(p6) -- name: addLayer
	-- upvalues: (copy) v_u_5
	if p6:IsA("GuiObject") then
		v_u_5[p6] = {
			["position"] = p6.Position,
			["depth"] = p6:GetAttribute("ParallaxDepth") or 0
		}
	end
end
local function v_u_18() -- name: update
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_5
	local v8 = v_u_2.CurrentCamera
	local v9 = v_u_3.Size.Y / v_u_3.Size.X
	local v10 = (v_u_3.Position - v8.CFrame.Position).Unit
	local v11 = v_u_3.CFrame:VectorToObjectSpace(v10)
	local v12 = v11.X
	local v13 = v11.Y / v9
	local v14 = Vector3.new(v12, v13, 0)
	for v15, v16 in v_u_5 do
		local v17 = UDim2.fromScale(v14.X * v16.depth, v14.Y * v16.depth)
		v15.Position = v16.position + v17
	end
end
(function() -- name: initialize
	-- upvalues: (copy) v_u_4, (copy) v_u_7, (copy) v_u_1, (copy) v_u_18, (copy) v_u_5
	v_u_4.ChildAdded:Connect(v_u_7)
	v_u_1.RenderStepped:Connect(v_u_18)
	for _, v19 in v_u_4:GetChildren() do
		if v19:IsA("GuiObject") then
			v_u_5[v19] = {
				["position"] = v19.Position,
				["depth"] = v19:GetAttribute("ParallaxDepth") or 0
			}
		end
	end
end)()

==================================================
-- Workspace.Transport.Railway.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Railway.Trent.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Female3.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Female5.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Man1.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Man2.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Man3.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Man4.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Bus.Man5.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Railway.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Transport.Railway.Trent.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Papeete Cathedral.Checkpoint.Justin Thyme.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Papeete Cathedral.Checkpoint.Justin Thyme.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Bora Bora.TransportCharterBoat.Left
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Bora Bora.TransportCharterBoat.Right
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Bora Bora.TransportCharterBoat.CharterBoat1.Captain Nemo.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v3, v4 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserNoUpdateOnLoop")
end)
local v5, v6 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateScriptEmoteHook")
end)
local v_u_7 = script:FindFirstChild("ScaleDampeningPercent")
local v_u_8 = {}
local v_u_9 = {}
local v_u_10 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
math.randomseed(tick())
function findExistingAnimationInSet(p11, p12) -- name: findExistingAnimationInSet
	if p11 == nil or p12 == nil then
		return 0
	end
	for v13 = 1, p11.count do
		if p11[v13].anim.AnimationId == p12.AnimationId then
			return v13
		end
	end
	return 0
end
function configureAnimationSet(p_u_14, p_u_15) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_9, (copy) v_u_8, (copy) v_u_2
	if v_u_9[p_u_14] ~= nil then
		for _, v16 in pairs(v_u_9[p_u_14].connections) do
			v16:disconnect()
		end
	end
	v_u_9[p_u_14] = {}
	v_u_9[p_u_14].count = 0
	v_u_9[p_u_14].totalWeight = 0
	v_u_9[p_u_14].connections = {}
	local v_u_17 = true
	local v18, _ = pcall(function()
		-- upvalues: (ref) v_u_17
		v_u_17 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_17 = not v18 and true or v_u_17
	local v19 = script:FindFirstChild(p_u_14)
	if v_u_17 and v19 ~= nil then
		local v20 = v_u_9[p_u_14].connections
		local v21 = v19.ChildAdded
		table.insert(v20, v21:connect(function(_)
			-- upvalues: (copy) p_u_14, (copy) p_u_15
			configureAnimationSet(p_u_14, p_u_15)
		end))
		local v22 = v_u_9[p_u_14].connections
		local v23 = v19.ChildRemoved
		table.insert(v22, v23:connect(function(_)
			-- upvalues: (copy) p_u_14, (copy) p_u_15
			configureAnimationSet(p_u_14, p_u_15)
		end))
		for _, v24 in pairs(v19:GetChildren()) do
			if v24:IsA("Animation") then
				local v25 = v24:FindFirstChild("Weight")
				local v26 = v25 == nil and 1 or v25.Value
				v_u_9[p_u_14].count = v_u_9[p_u_14].count + 1
				local v27 = v_u_9[p_u_14].count
				v_u_9[p_u_14][v27] = {}
				v_u_9[p_u_14][v27].anim = v24
				v_u_9[p_u_14][v27].weight = v26
				v_u_9[p_u_14].totalWeight = v_u_9[p_u_14].totalWeight + v_u_9[p_u_14][v27].weight
				local v28 = v_u_9[p_u_14].connections
				local v29 = v24.Changed
				table.insert(v28, v29:connect(function(_)
					-- upvalues: (copy) p_u_14, (copy) p_u_15
					configureAnimationSet(p_u_14, p_u_15)
				end))
				local v30 = v_u_9[p_u_14].connections
				local v31 = v24.ChildAdded
				table.insert(v30, v31:connect(function(_)
					-- upvalues: (copy) p_u_14, (copy) p_u_15
					configureAnimationSet(p_u_14, p_u_15)
				end))
				local v32 = v_u_9[p_u_14].connections
				local v33 = v24.ChildRemoved
				table.insert(v32, v33:connect(function(_)
					-- upvalues: (copy) p_u_14, (copy) p_u_15
					configureAnimationSet(p_u_14, p_u_15)
				end))
			end
		end
	end
	if v_u_9[p_u_14].count <= 0 then
		for v34, v35 in pairs(p_u_15) do
			v_u_9[p_u_14][v34] = {}
			v_u_9[p_u_14][v34].anim = Instance.new("Animation")
			v_u_9[p_u_14][v34].anim.Name = p_u_14
			v_u_9[p_u_14][v34].anim.AnimationId = v35.id
			v_u_9[p_u_14][v34].weight = v35.weight
			v_u_9[p_u_14].count = v_u_9[p_u_14].count + 1
			v_u_9[p_u_14].totalWeight = v_u_9[p_u_14].totalWeight + v35.weight
		end
	end
	for _, v36 in pairs(v_u_9) do
		for v37 = 1, v36.count do
			if v_u_8[v36[v37].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v36[v37].anim)
				v_u_8[v36[v37].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_38, p_u_39) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_9, (copy) v_u_2
	if v_u_9[p_u_38] ~= nil then
		for _, v40 in pairs(v_u_9[p_u_38].connections) do
			v40:disconnect()
		end
	end
	v_u_9[p_u_38] = {}
	v_u_9[p_u_38].count = 0
	v_u_9[p_u_38].totalWeight = 0
	v_u_9[p_u_38].connections = {}
	local v_u_41 = true
	local v42, _ = pcall(function()
		-- upvalues: (ref) v_u_41
		v_u_41 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_41 = not v42 and true or v_u_41
	local v43 = script:FindFirstChild(p_u_38)
	if v_u_41 and v43 ~= nil then
		local v44 = v_u_9[p_u_38].connections
		local v45 = v43.ChildAdded
		table.insert(v44, v45:connect(function(_)
			-- upvalues: (copy) p_u_38, (copy) p_u_39
			configureAnimationSet(p_u_38, p_u_39)
		end))
		local v46 = v_u_9[p_u_38].connections
		local v47 = v43.ChildRemoved
		table.insert(v46, v47:connect(function(_)
			-- upvalues: (copy) p_u_38, (copy) p_u_39
			configureAnimationSet(p_u_38, p_u_39)
		end))
		local v48 = 1
		for _, v49 in pairs(v43:GetChildren()) do
			if v49:IsA("Animation") then
				local v50 = v_u_9[p_u_38].connections
				local v51 = v49.Changed
				table.insert(v50, v51:connect(function(_)
					-- upvalues: (copy) p_u_38, (copy) p_u_39
					configureAnimationSet(p_u_38, p_u_39)
				end))
				v_u_9[p_u_38][v48] = {}
				v_u_9[p_u_38][v48].anim = v49
				local v52 = v49:FindFirstChild("Weight")
				if v52 == nil then
					v_u_9[p_u_38][v48].weight = 1
				else
					v_u_9[p_u_38][v48].weight = v52.Value
				end
				v_u_9[p_u_38].count = v_u_9[p_u_38].count + 1
				v_u_9[p_u_38].totalWeight = v_u_9[p_u_38].totalWeight + v_u_9[p_u_38][v48].weight
				v48 = v48 + 1
			end
		end
	end
	if v_u_9[p_u_38].count <= 0 then
		for v53, v54 in pairs(p_u_39) do
			v_u_9[p_u_38][v53] = {}
			v_u_9[p_u_38][v53].anim = Instance.new("Animation")
			v_u_9[p_u_38][v53].anim.Name = p_u_38
			v_u_9[p_u_38][v53].anim.AnimationId = v54.id
			v_u_9[p_u_38][v53].weight = v54.weight
			v_u_9[p_u_38].count = v_u_9[p_u_38].count + 1
			v_u_9[p_u_38].totalWeight = v_u_9[p_u_38].totalWeight + v54.weight
		end
	end
	for _, v55 in pairs(v_u_9) do
		for v56 = 1, v55.count do
			v_u_2:LoadAnimation(v55[v56].anim)
		end
	end
end
function scriptChildModified(p57) -- name: scriptChildModified
	-- upvalues: (copy) v_u_10
	local v58 = v_u_10[p57.Name]
	if v58 ~= nil then
		configureAnimationSet(p57.Name, v58)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v_u_59 = "Standing"
local v_u_60 = ""
local v_u_61 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_62 = v5 and v6
local v_u_63 = nil
local v_u_64 = nil
local v_u_65 = nil
local v_u_66 = 1
local v_u_67 = v3 and v4
local v_u_68 = nil
local v_u_69 = nil
for v70, v71 in pairs(v_u_10) do
	configureAnimationSet(v70, v71)
end
local v_u_72 = "None"
local v_u_73 = 0
local v_u_74 = 0
local v_u_75 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_60, (copy) v_u_61, (copy) v_u_62, (ref) v_u_75, (ref) v_u_68, (ref) v_u_63, (ref) v_u_64, (ref) v_u_69, (ref) v_u_65
	local v76 = v_u_60
	local v77 = v_u_61[v76] ~= nil and v_u_61[v76] == false and "idle" or v76
	if v_u_62 and v_u_75 then
		v77 = "idle"
		v_u_75 = false
	end
	v_u_60 = ""
	v_u_68 = nil
	if v_u_63 ~= nil then
		v_u_63:disconnect()
	end
	if v_u_64 ~= nil then
		v_u_64:Stop()
		v_u_64:Destroy()
		v_u_64 = nil
	end
	if v_u_69 ~= nil then
		v_u_69:disconnect()
	end
	if v_u_65 ~= nil then
		v_u_65:Stop()
		v_u_65:Destroy()
		v_u_65 = nil
	end
	return v77
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (ref) v_u_7
	if not v_u_2 then
		return 1
	end
	if not v_u_2.AutomaticScalingEnabled then
		return 1
	end
	local v78 = v_u_2.HipHeight / 2
	if v_u_7 == nil then
		v_u_7 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_7 ~= nil then
		v78 = 1 + (v_u_2.HipHeight - 2) * v_u_7.Value / 2
	end
	return v78
end
function setRunSpeed(p79) -- name: setRunSpeed
	-- upvalues: (ref) v_u_66, (ref) v_u_64, (ref) v_u_65
	local v80 = p79 * 1.25 / getHeightScale()
	if v80 ~= v_u_66 then
		if v80 < 0.33 then
			v_u_64:AdjustWeight(1)
			v_u_65:AdjustWeight(0.0001)
		elseif v80 < 0.66 then
			local v81 = (v80 - 0.33) / 0.33
			v_u_64:AdjustWeight(1 - v81 + 0.0001)
			v_u_65:AdjustWeight(v81 + 0.0001)
		else
			v_u_64:AdjustWeight(0.0001)
			v_u_65:AdjustWeight(1)
		end
		v_u_66 = v80
		v_u_65:AdjustSpeed(v80)
		v_u_64:AdjustSpeed(v80)
	end
end
function setAnimationSpeed(p82) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_60, (ref) v_u_66, (ref) v_u_64
	if v_u_60 == "walk" then
		setRunSpeed(p82)
	elseif p82 ~= v_u_66 then
		v_u_66 = p82
		v_u_64:AdjustSpeed(v_u_66)
	end
end
function keyFrameReachedFunc(p83) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_60, (copy) v_u_67, (ref) v_u_65, (ref) v_u_64, (copy) v_u_61, (copy) v_u_62, (ref) v_u_75, (ref) v_u_66, (copy) v_u_2
	if p83 == "End" then
		if v_u_60 == "walk" then
			if v_u_67 ~= true then
				v_u_65.TimePosition = 0
				v_u_64.TimePosition = 0
				return
			end
			if v_u_65.Looped ~= true then
				v_u_65.TimePosition = 0
			end
			if v_u_64.Looped ~= true then
				v_u_64.TimePosition = 0
				return
			end
		else
			local v84 = v_u_60
			local v85 = v_u_61[v84] ~= nil and v_u_61[v84] == false and "idle" or v84
			if v_u_62 and v_u_75 then
				if v_u_64.Looped then
					return
				end
				v85 = "idle"
				v_u_75 = false
			end
			local v86 = v_u_66
			playAnimation(v85, 0.15, v_u_2)
			setAnimationSpeed(v86)
		end
	end
end
function rollAnimation(p87) -- name: rollAnimation
	-- upvalues: (copy) v_u_9
	local v88 = math.random(1, v_u_9[p87].totalWeight)
	local v89 = 1
	while v_u_9[p87][v89].weight < v88 do
		v88 = v88 - v_u_9[p87][v89].weight
		v89 = v89 + 1
	end
	return v89
end
local function v_u_95(p90, p91, p92, p93) -- name: switchToAnim
	-- upvalues: (ref) v_u_68, (ref) v_u_64, (ref) v_u_65, (copy) v_u_67, (ref) v_u_66, (ref) v_u_60, (ref) v_u_63, (copy) v_u_9, (ref) v_u_69
	if p90 ~= v_u_68 then
		if v_u_64 ~= nil then
			v_u_64:Stop(p92)
			v_u_64:Destroy()
		end
		if v_u_65 ~= nil then
			v_u_65:Stop(p92)
			v_u_65:Destroy()
			if v_u_67 == true then
				v_u_65 = nil
			end
		end
		v_u_66 = 1
		v_u_64 = p93:LoadAnimation(p90)
		v_u_64.Priority = Enum.AnimationPriority.Core
		v_u_64:Play(p92)
		v_u_60 = p91
		v_u_68 = p90
		if v_u_63 ~= nil then
			v_u_63:disconnect()
		end
		v_u_63 = v_u_64.KeyframeReached:connect(keyFrameReachedFunc)
		if p91 == "walk" then
			local v94 = rollAnimation("run")
			v_u_65 = p93:LoadAnimation(v_u_9.run[v94].anim)
			v_u_65.Priority = Enum.AnimationPriority.Core
			v_u_65:Play(p92)
			if v_u_69 ~= nil then
				v_u_69:disconnect()
			end
			v_u_69 = v_u_65.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p96, p97, p98) -- name: playAnimation
	-- upvalues: (copy) v_u_9, (copy) v_u_95, (ref) v_u_75
	local v99 = rollAnimation(p96)
	v_u_95(v_u_9[p96][v99].anim, p96, p97, p98)
	v_u_75 = false
end
function playEmote(p100, p101, p102) -- name: playEmote
	-- upvalues: (copy) v_u_95, (ref) v_u_75
	v_u_95(p100, p100.Name, p101, p102)
	v_u_75 = true
end
local v_u_103 = ""
local v_u_104 = nil
local v_u_105 = nil
local v_u_106 = nil
function toolKeyFrameReachedFunc(p107) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_103, (copy) v_u_2
	if p107 == "End" then
		playToolAnimation(v_u_103, 0, v_u_2)
	end
end
function playToolAnimation(p108, p109, p110, p111) -- name: playToolAnimation
	-- upvalues: (copy) v_u_9, (ref) v_u_105, (ref) v_u_104, (ref) v_u_103, (ref) v_u_106
	local v112 = rollAnimation(p108)
	local v113 = v_u_9[p108][v112].anim
	if v_u_105 ~= v113 then
		if v_u_104 ~= nil then
			v_u_104:Stop()
			v_u_104:Destroy()
			p109 = 0
		end
		v_u_104 = p110:LoadAnimation(v113)
		if p111 then
			v_u_104.Priority = p111
		end
		v_u_104:Play(p109)
		v_u_103 = p108
		v_u_105 = v113
		v_u_106 = v_u_104.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_103, (ref) v_u_106, (ref) v_u_105, (ref) v_u_104
	local v114 = v_u_103
	if v_u_106 ~= nil then
		v_u_106:disconnect()
	end
	v_u_103 = ""
	v_u_105 = nil
	if v_u_104 ~= nil then
		v_u_104:Stop()
		v_u_104:Destroy()
		v_u_104 = nil
	end
	return v114
end
function onRunning(p115) -- name: onRunning
	-- upvalues: (copy) v_u_2, (ref) v_u_59, (copy) v_u_61, (ref) v_u_60, (ref) v_u_75
	if p115 > 0.75 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p115 / 16)
		v_u_59 = "Running"
	elseif v_u_61[v_u_60] == nil and not v_u_75 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_59 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_59
	v_u_59 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_74, (ref) v_u_59
	playAnimation("jump", 0.1, v_u_2)
	v_u_74 = 0.31
	v_u_59 = "Jumping"
end
function onClimbing(p116) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_59
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(p116 / 5)
	v_u_59 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_59
	v_u_59 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_74, (copy) v_u_2, (ref) v_u_59
	if v_u_74 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_59 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_59
	v_u_59 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_59
	v_u_59 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_59
	v_u_59 = "PlatformStanding"
end
function onSwimming(p117) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_59
	if p117 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(p117 / 10)
		v_u_59 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_59 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_72, (copy) v_u_2
	if v_u_72 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_72 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_72 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p118) -- name: getToolAnim
	for _, v119 in ipairs(p118:GetChildren()) do
		if v119.Name == "toolanim" and v119.className == "StringValue" then
			return v119
		end
	end
	return nil
end
local v_u_120 = 0
function stepAnimate(p121) -- name: stepAnimate
	-- upvalues: (ref) v_u_120, (ref) v_u_74, (ref) v_u_59, (copy) v_u_2, (copy) v_u_1, (ref) v_u_72, (ref) v_u_73, (ref) v_u_105
	local v122 = p121 - v_u_120
	v_u_120 = p121
	if v_u_74 > 0 then
		v_u_74 = v_u_74 - v122
	end
	if v_u_59 == "FreeFall" and v_u_74 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_59 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_59 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_59 == "Dead" or (v_u_59 == "GettingUp" or (v_u_59 == "FallingDown" or (v_u_59 == "Seated" or v_u_59 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v123 = v_u_1:FindFirstChildOfClass("Tool")
	if v123 and v123:FindFirstChild("Handle") then
		local v124 = getToolAnim(v123)
		if v124 then
			v_u_72 = v124.Value
			v124.Parent = nil
			v_u_73 = p121 + 0.3
		end
		if v_u_73 < p121 then
			v_u_73 = 0
			v_u_72 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_72 = "None"
		v_u_105 = nil
		v_u_73 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
game:GetService("Players").LocalPlayer.Chatted:connect(function(p125)
	-- upvalues: (ref) v_u_59, (copy) v_u_61, (copy) v_u_2
	local v126 = ""
	if string.sub(p125, 1, 3) == "/e " then
		v126 = string.sub(p125, 4)
	elseif string.sub(p125, 1, 7) == "/emote " then
		v126 = string.sub(p125, 8)
	end
	if v_u_59 == "Standing" and v_u_61[v126] ~= nil then
		playAnimation(v126, 0.1, v_u_2)
	end
end)
if v_u_62 then
	script:WaitForChild("PlayEmote").OnInvoke = function(p127)
		-- upvalues: (ref) v_u_59, (copy) v_u_61, (copy) v_u_2
		if v_u_59 == "Standing" then
			if v_u_61[p127] ~= nil then
				playAnimation(p127, 0.1, v_u_2)
				return true
			end
			if typeof(p127) ~= "Instance" or not p127:IsA("Animation") then
				return false
			end
			playEmote(p127, 0.1, v_u_2)
			return true
		end
	end
end
playAnimation("idle", 0.1, v_u_2)
local _ = "Standing"
while v_u_1.Parent ~= nil do
	local _, v128 = wait(0.1)
	stepAnimate(v128)
end

==================================================
-- Workspace.Legs.Papeete.Bora Bora.TransportCharterBoat.CharterBoat1.Captain Nemo.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Bora Bora.TransportCharterBoat.CharterBoat2.Captain Nemo.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v3, v4 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserNoUpdateOnLoop")
end)
local v5, v6 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateScriptEmoteHook")
end)
local v_u_7 = script:FindFirstChild("ScaleDampeningPercent")
local v_u_8 = {}
local v_u_9 = {}
local v_u_10 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
math.randomseed(tick())
function findExistingAnimationInSet(p11, p12) -- name: findExistingAnimationInSet
	if p11 == nil or p12 == nil then
		return 0
	end
	for v13 = 1, p11.count do
		if p11[v13].anim.AnimationId == p12.AnimationId then
			return v13
		end
	end
	return 0
end
function configureAnimationSet(p_u_14, p_u_15) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_9, (copy) v_u_8, (copy) v_u_2
	if v_u_9[p_u_14] ~= nil then
		for _, v16 in pairs(v_u_9[p_u_14].connections) do
			v16:disconnect()
		end
	end
	v_u_9[p_u_14] = {}
	v_u_9[p_u_14].count = 0
	v_u_9[p_u_14].totalWeight = 0
	v_u_9[p_u_14].connections = {}
	local v_u_17 = true
	local v18, _ = pcall(function()
		-- upvalues: (ref) v_u_17
		v_u_17 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_17 = not v18 and true or v_u_17
	local v19 = script:FindFirstChild(p_u_14)
	if v_u_17 and v19 ~= nil then
		local v20 = v_u_9[p_u_14].connections
		local v21 = v19.ChildAdded
		table.insert(v20, v21:connect(function(_)
			-- upvalues: (copy) p_u_14, (copy) p_u_15
			configureAnimationSet(p_u_14, p_u_15)
		end))
		local v22 = v_u_9[p_u_14].connections
		local v23 = v19.ChildRemoved
		table.insert(v22, v23:connect(function(_)
			-- upvalues: (copy) p_u_14, (copy) p_u_15
			configureAnimationSet(p_u_14, p_u_15)
		end))
		for _, v24 in pairs(v19:GetChildren()) do
			if v24:IsA("Animation") then
				local v25 = v24:FindFirstChild("Weight")
				local v26 = v25 == nil and 1 or v25.Value
				v_u_9[p_u_14].count = v_u_9[p_u_14].count + 1
				local v27 = v_u_9[p_u_14].count
				v_u_9[p_u_14][v27] = {}
				v_u_9[p_u_14][v27].anim = v24
				v_u_9[p_u_14][v27].weight = v26
				v_u_9[p_u_14].totalWeight = v_u_9[p_u_14].totalWeight + v_u_9[p_u_14][v27].weight
				local v28 = v_u_9[p_u_14].connections
				local v29 = v24.Changed
				table.insert(v28, v29:connect(function(_)
					-- upvalues: (copy) p_u_14, (copy) p_u_15
					configureAnimationSet(p_u_14, p_u_15)
				end))
				local v30 = v_u_9[p_u_14].connections
				local v31 = v24.ChildAdded
				table.insert(v30, v31:connect(function(_)
					-- upvalues: (copy) p_u_14, (copy) p_u_15
					configureAnimationSet(p_u_14, p_u_15)
				end))
				local v32 = v_u_9[p_u_14].connections
				local v33 = v24.ChildRemoved
				table.insert(v32, v33:connect(function(_)
					-- upvalues: (copy) p_u_14, (copy) p_u_15
					configureAnimationSet(p_u_14, p_u_15)
				end))
			end
		end
	end
	if v_u_9[p_u_14].count <= 0 then
		for v34, v35 in pairs(p_u_15) do
			v_u_9[p_u_14][v34] = {}
			v_u_9[p_u_14][v34].anim = Instance.new("Animation")
			v_u_9[p_u_14][v34].anim.Name = p_u_14
			v_u_9[p_u_14][v34].anim.AnimationId = v35.id
			v_u_9[p_u_14][v34].weight = v35.weight
			v_u_9[p_u_14].count = v_u_9[p_u_14].count + 1
			v_u_9[p_u_14].totalWeight = v_u_9[p_u_14].totalWeight + v35.weight
		end
	end
	for _, v36 in pairs(v_u_9) do
		for v37 = 1, v36.count do
			if v_u_8[v36[v37].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v36[v37].anim)
				v_u_8[v36[v37].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_38, p_u_39) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_9, (copy) v_u_2
	if v_u_9[p_u_38] ~= nil then
		for _, v40 in pairs(v_u_9[p_u_38].connections) do
			v40:disconnect()
		end
	end
	v_u_9[p_u_38] = {}
	v_u_9[p_u_38].count = 0
	v_u_9[p_u_38].totalWeight = 0
	v_u_9[p_u_38].connections = {}
	local v_u_41 = true
	local v42, _ = pcall(function()
		-- upvalues: (ref) v_u_41
		v_u_41 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_41 = not v42 and true or v_u_41
	local v43 = script:FindFirstChild(p_u_38)
	if v_u_41 and v43 ~= nil then
		local v44 = v_u_9[p_u_38].connections
		local v45 = v43.ChildAdded
		table.insert(v44, v45:connect(function(_)
			-- upvalues: (copy) p_u_38, (copy) p_u_39
			configureAnimationSet(p_u_38, p_u_39)
		end))
		local v46 = v_u_9[p_u_38].connections
		local v47 = v43.ChildRemoved
		table.insert(v46, v47:connect(function(_)
			-- upvalues: (copy) p_u_38, (copy) p_u_39
			configureAnimationSet(p_u_38, p_u_39)
		end))
		local v48 = 1
		for _, v49 in pairs(v43:GetChildren()) do
			if v49:IsA("Animation") then
				local v50 = v_u_9[p_u_38].connections
				local v51 = v49.Changed
				table.insert(v50, v51:connect(function(_)
					-- upvalues: (copy) p_u_38, (copy) p_u_39
					configureAnimationSet(p_u_38, p_u_39)
				end))
				v_u_9[p_u_38][v48] = {}
				v_u_9[p_u_38][v48].anim = v49
				local v52 = v49:FindFirstChild("Weight")
				if v52 == nil then
					v_u_9[p_u_38][v48].weight = 1
				else
					v_u_9[p_u_38][v48].weight = v52.Value
				end
				v_u_9[p_u_38].count = v_u_9[p_u_38].count + 1
				v_u_9[p_u_38].totalWeight = v_u_9[p_u_38].totalWeight + v_u_9[p_u_38][v48].weight
				v48 = v48 + 1
			end
		end
	end
	if v_u_9[p_u_38].count <= 0 then
		for v53, v54 in pairs(p_u_39) do
			v_u_9[p_u_38][v53] = {}
			v_u_9[p_u_38][v53].anim = Instance.new("Animation")
			v_u_9[p_u_38][v53].anim.Name = p_u_38
			v_u_9[p_u_38][v53].anim.AnimationId = v54.id
			v_u_9[p_u_38][v53].weight = v54.weight
			v_u_9[p_u_38].count = v_u_9[p_u_38].count + 1
			v_u_9[p_u_38].totalWeight = v_u_9[p_u_38].totalWeight + v54.weight
		end
	end
	for _, v55 in pairs(v_u_9) do
		for v56 = 1, v55.count do
			v_u_2:LoadAnimation(v55[v56].anim)
		end
	end
end
function scriptChildModified(p57) -- name: scriptChildModified
	-- upvalues: (copy) v_u_10
	local v58 = v_u_10[p57.Name]
	if v58 ~= nil then
		configureAnimationSet(p57.Name, v58)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v_u_59 = 1
local v_u_60 = v3 and v4
local v_u_61 = "Standing"
local v_u_62 = nil
local v_u_63 = nil
local v_u_64 = nil
local v_u_65 = ""
local v_u_66 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_67 = v5 and v6
local v_u_68 = nil
local v_u_69 = nil
for v70, v71 in pairs(v_u_10) do
	configureAnimationSet(v70, v71)
end
local v_u_72 = "None"
local v_u_73 = 0
local v_u_74 = 0
local v_u_75 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_65, (copy) v_u_66, (copy) v_u_67, (ref) v_u_75, (ref) v_u_62, (ref) v_u_63, (ref) v_u_68, (ref) v_u_64, (ref) v_u_69
	local v76 = v_u_65
	local v77 = v_u_66[v76] ~= nil and v_u_66[v76] == false and "idle" or v76
	if v_u_67 and v_u_75 then
		v77 = "idle"
		v_u_75 = false
	end
	v_u_65 = ""
	v_u_62 = nil
	if v_u_63 ~= nil then
		v_u_63:disconnect()
	end
	if v_u_68 ~= nil then
		v_u_68:Stop()
		v_u_68:Destroy()
		v_u_68 = nil
	end
	if v_u_64 ~= nil then
		v_u_64:disconnect()
	end
	if v_u_69 ~= nil then
		v_u_69:Stop()
		v_u_69:Destroy()
		v_u_69 = nil
	end
	return v77
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (ref) v_u_7
	if not v_u_2 then
		return 1
	end
	if not v_u_2.AutomaticScalingEnabled then
		return 1
	end
	local v78 = v_u_2.HipHeight / 2
	if v_u_7 == nil then
		v_u_7 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_7 ~= nil then
		v78 = 1 + (v_u_2.HipHeight - 2) * v_u_7.Value / 2
	end
	return v78
end
function setRunSpeed(p79) -- name: setRunSpeed
	-- upvalues: (ref) v_u_59, (ref) v_u_68, (ref) v_u_69
	local v80 = p79 * 1.25 / getHeightScale()
	if v80 ~= v_u_59 then
		if v80 < 0.33 then
			v_u_68:AdjustWeight(1)
			v_u_69:AdjustWeight(0.0001)
		elseif v80 < 0.66 then
			local v81 = (v80 - 0.33) / 0.33
			v_u_68:AdjustWeight(1 - v81 + 0.0001)
			v_u_69:AdjustWeight(v81 + 0.0001)
		else
			v_u_68:AdjustWeight(0.0001)
			v_u_69:AdjustWeight(1)
		end
		v_u_59 = v80
		v_u_69:AdjustSpeed(v80)
		v_u_68:AdjustSpeed(v80)
	end
end
function setAnimationSpeed(p82) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_65, (ref) v_u_59, (ref) v_u_68
	if v_u_65 == "walk" then
		setRunSpeed(p82)
	elseif p82 ~= v_u_59 then
		v_u_59 = p82
		v_u_68:AdjustSpeed(v_u_59)
	end
end
function keyFrameReachedFunc(p83) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_65, (copy) v_u_60, (ref) v_u_69, (ref) v_u_68, (copy) v_u_66, (copy) v_u_67, (ref) v_u_75, (ref) v_u_59, (copy) v_u_2
	if p83 == "End" then
		if v_u_65 == "walk" then
			if v_u_60 ~= true then
				v_u_69.TimePosition = 0
				v_u_68.TimePosition = 0
				return
			end
			if v_u_69.Looped ~= true then
				v_u_69.TimePosition = 0
			end
			if v_u_68.Looped ~= true then
				v_u_68.TimePosition = 0
				return
			end
		else
			local v84 = v_u_65
			local v85 = v_u_66[v84] ~= nil and v_u_66[v84] == false and "idle" or v84
			if v_u_67 and v_u_75 then
				if v_u_68.Looped then
					return
				end
				v85 = "idle"
				v_u_75 = false
			end
			local v86 = v_u_59
			playAnimation(v85, 0.15, v_u_2)
			setAnimationSpeed(v86)
		end
	end
end
function rollAnimation(p87) -- name: rollAnimation
	-- upvalues: (copy) v_u_9
	local v88 = math.random(1, v_u_9[p87].totalWeight)
	local v89 = 1
	while v_u_9[p87][v89].weight < v88 do
		v88 = v88 - v_u_9[p87][v89].weight
		v89 = v89 + 1
	end
	return v89
end
local function v_u_95(p90, p91, p92, p93) -- name: switchToAnim
	-- upvalues: (ref) v_u_62, (ref) v_u_68, (ref) v_u_69, (copy) v_u_60, (ref) v_u_59, (ref) v_u_65, (ref) v_u_63, (copy) v_u_9, (ref) v_u_64
	if p90 ~= v_u_62 then
		if v_u_68 ~= nil then
			v_u_68:Stop(p92)
			v_u_68:Destroy()
		end
		if v_u_69 ~= nil then
			v_u_69:Stop(p92)
			v_u_69:Destroy()
			if v_u_60 == true then
				v_u_69 = nil
			end
		end
		v_u_59 = 1
		v_u_68 = p93:LoadAnimation(p90)
		v_u_68.Priority = Enum.AnimationPriority.Core
		v_u_68:Play(p92)
		v_u_65 = p91
		v_u_62 = p90
		if v_u_63 ~= nil then
			v_u_63:disconnect()
		end
		v_u_63 = v_u_68.KeyframeReached:connect(keyFrameReachedFunc)
		if p91 == "walk" then
			local v94 = rollAnimation("run")
			v_u_69 = p93:LoadAnimation(v_u_9.run[v94].anim)
			v_u_69.Priority = Enum.AnimationPriority.Core
			v_u_69:Play(p92)
			if v_u_64 ~= nil then
				v_u_64:disconnect()
			end
			v_u_64 = v_u_69.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p96, p97, p98) -- name: playAnimation
	-- upvalues: (copy) v_u_9, (copy) v_u_95, (ref) v_u_75
	local v99 = rollAnimation(p96)
	v_u_95(v_u_9[p96][v99].anim, p96, p97, p98)
	v_u_75 = false
end
function playEmote(p100, p101, p102) -- name: playEmote
	-- upvalues: (copy) v_u_95, (ref) v_u_75
	v_u_95(p100, p100.Name, p101, p102)
	v_u_75 = true
end
local v_u_103 = ""
local v_u_104 = nil
local v_u_105 = nil
local v_u_106 = nil
function toolKeyFrameReachedFunc(p107) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_103, (copy) v_u_2
	if p107 == "End" then
		playToolAnimation(v_u_103, 0, v_u_2)
	end
end
function playToolAnimation(p108, p109, p110, p111) -- name: playToolAnimation
	-- upvalues: (copy) v_u_9, (ref) v_u_105, (ref) v_u_104, (ref) v_u_103, (ref) v_u_106
	local v112 = rollAnimation(p108)
	local v113 = v_u_9[p108][v112].anim
	if v_u_105 ~= v113 then
		if v_u_104 ~= nil then
			v_u_104:Stop()
			v_u_104:Destroy()
			p109 = 0
		end
		v_u_104 = p110:LoadAnimation(v113)
		if p111 then
			v_u_104.Priority = p111
		end
		v_u_104:Play(p109)
		v_u_103 = p108
		v_u_105 = v113
		v_u_106 = v_u_104.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_103, (ref) v_u_106, (ref) v_u_105, (ref) v_u_104
	local v114 = v_u_103
	if v_u_106 ~= nil then
		v_u_106:disconnect()
	end
	v_u_103 = ""
	v_u_105 = nil
	if v_u_104 ~= nil then
		v_u_104:Stop()
		v_u_104:Destroy()
		v_u_104 = nil
	end
	return v114
end
function onRunning(p115) -- name: onRunning
	-- upvalues: (copy) v_u_2, (ref) v_u_61, (copy) v_u_66, (ref) v_u_65, (ref) v_u_75
	if p115 > 0.75 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p115 / 16)
		v_u_61 = "Running"
	elseif v_u_66[v_u_65] == nil and not v_u_75 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_61 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_61
	v_u_61 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_74, (ref) v_u_61
	playAnimation("jump", 0.1, v_u_2)
	v_u_74 = 0.31
	v_u_61 = "Jumping"
end
function onClimbing(p116) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_61
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(p116 / 5)
	v_u_61 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_61
	v_u_61 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_74, (copy) v_u_2, (ref) v_u_61
	if v_u_74 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_61 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_61
	v_u_61 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_61
	v_u_61 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_61
	v_u_61 = "PlatformStanding"
end
function onSwimming(p117) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_61
	if p117 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(p117 / 10)
		v_u_61 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_61 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_72, (copy) v_u_2
	if v_u_72 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_72 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_72 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p118) -- name: getToolAnim
	for _, v119 in ipairs(p118:GetChildren()) do
		if v119.Name == "toolanim" and v119.className == "StringValue" then
			return v119
		end
	end
	return nil
end
local v_u_120 = 0
function stepAnimate(p121) -- name: stepAnimate
	-- upvalues: (ref) v_u_120, (ref) v_u_74, (ref) v_u_61, (copy) v_u_2, (copy) v_u_1, (ref) v_u_72, (ref) v_u_73, (ref) v_u_105
	local v122 = p121 - v_u_120
	v_u_120 = p121
	if v_u_74 > 0 then
		v_u_74 = v_u_74 - v122
	end
	if v_u_61 == "FreeFall" and v_u_74 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_61 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_61 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_61 == "Dead" or (v_u_61 == "GettingUp" or (v_u_61 == "FallingDown" or (v_u_61 == "Seated" or v_u_61 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v123 = v_u_1:FindFirstChildOfClass("Tool")
	if v123 and v123:FindFirstChild("Handle") then
		local v124 = getToolAnim(v123)
		if v124 then
			v_u_72 = v124.Value
			v124.Parent = nil
			v_u_73 = p121 + 0.3
		end
		if v_u_73 < p121 then
			v_u_73 = 0
			v_u_72 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_72 = "None"
		v_u_105 = nil
		v_u_73 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
game:GetService("Players").LocalPlayer.Chatted:connect(function(p125)
	-- upvalues: (ref) v_u_61, (copy) v_u_66, (copy) v_u_2
	local v126 = ""
	if string.sub(p125, 1, 3) == "/e " then
		v126 = string.sub(p125, 4)
	elseif string.sub(p125, 1, 7) == "/emote " then
		v126 = string.sub(p125, 8)
	end
	if v_u_61 == "Standing" and v_u_66[v126] ~= nil then
		playAnimation(v126, 0.1, v_u_2)
	end
end)
if v_u_67 then
	script:WaitForChild("PlayEmote").OnInvoke = function(p127)
		-- upvalues: (ref) v_u_61, (copy) v_u_66, (copy) v_u_2
		if v_u_61 == "Standing" then
			if v_u_66[p127] ~= nil then
				playAnimation(p127, 0.1, v_u_2)
				return true
			end
			if typeof(p127) ~= "Instance" or not p127:IsA("Animation") then
				return false
			end
			playEmote(p127, 0.1, v_u_2)
			return true
		end
	end
end
playAnimation("idle", 0.1, v_u_2)
local _ = "Standing"
while v_u_1.Parent ~= nil do
	local _, v128 = wait(0.1)
	stepAnimate(v128)
end

==================================================
-- Workspace.Legs.Papeete.Bora Bora.TransportCharterBoat.CharterBoat2.Captain Nemo.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane1.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane1.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane1.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane5.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane5.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane5.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane6.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane6.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane6.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane7.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane7.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane7.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane8.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane8.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane8.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane9.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane9.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane9.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane4.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane4.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane4.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane2.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane2.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane2.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane3.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane3.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Lanes.Lane3.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Talia.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Loto.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Legs.Papeete.Over.Loto.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Arrivals.Center Piece..Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Arrivals.Papeete.Water.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.iFlyFStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.InterAirlinesFStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.JambeAirwaysFStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.iFlyMStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.BloxJetMStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.InterAirlinesMStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.BloxJetFStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.JambeAirwaysMStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.YonderMStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Staff.YonderFStaff.Animate
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Airport.Center Piece..Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Ji18_123.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.Ji18_123.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Ji18_123.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_24
	v_u_89 = v_u_23
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_24
	v_u_89 = v_u_23
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_89, (copy) v_u_2, (ref) v_u_88, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_89 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_89.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_89.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_88.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.thatgirlvanssa1.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_24
	v_u_89 = v_u_23
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_24
	v_u_89 = v_u_23
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_89, (copy) v_u_2, (ref) v_u_88, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_89 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_89.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_89.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_88.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.thatgirlvanssa1.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.thatgirlvanssa1.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.Katy_862.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_23
	v_u_89 = v_u_24
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_23
	v_u_89 = v_u_24
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_88, (copy) v_u_2, (ref) v_u_89, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_88 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_88.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_88.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_89.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.Katy_862.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.Katy_862.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.vgvybrxbh.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_24
	v_u_89 = v_u_23
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_24
	v_u_89 = v_u_23
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_89, (copy) v_u_2, (ref) v_u_88, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_89 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_89.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_89.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_88.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.vgvybrxbh.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.vgvybrxbh.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.julija151119.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_24
	v_u_89 = v_u_23
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_24
	v_u_89 = v_u_23
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_89, (copy) v_u_2, (ref) v_u_88, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_89 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_89.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_89.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_88.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.julija151119.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.julija151119.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.a01z3.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_24
	v_u_89 = v_u_23
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_24
	v_u_89 = v_u_23
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_89, (copy) v_u_2, (ref) v_u_88, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_89 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_89.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_89.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_88.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.a01z3.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.a01z3.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.moe55112.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.moe55112.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.moe55112.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_24
	v_u_89 = v_u_23
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_24
	v_u_89 = v_u_23
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_89, (copy) v_u_2, (ref) v_u_88, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_89 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_89.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_89.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_88.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.olauvliver.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_24
	v_u_89 = v_u_23
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_24
	v_u_89 = v_u_23
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_89, (copy) v_u_2, (ref) v_u_88, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_89 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_89.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_89.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_88.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.olauvliver.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.olauvliver.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.0000El0000.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.0000El0000.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.0000El0000.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_24
	v_u_89 = v_u_23
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_24
	v_u_89 = v_u_23
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_89, (copy) v_u_2, (ref) v_u_88, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_89 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_89.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_89.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_88.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.0000El0000.Theater Sign.Script
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.maja110.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_24
	v_u_89 = v_u_23
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_24
	v_u_89 = v_u_23
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_89, (copy) v_u_2, (ref) v_u_88, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_89 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_89.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_89.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_88.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Workspace.maja110.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.maja110.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.turbobrutti.HoldItem
==================================================
local v1 = game.Players.LocalPlayer
local v_u_2 = {}
local v_u_3 = script:WaitForChild("HoldItem")
local v_u_4 = script:WaitForChild("HoldItem2")
local v_u_5 = script:WaitForChild("HoldSpade")
local v_u_6 = script:WaitForChild("HoldPizzaBox")
local v_u_7 = script:WaitForChild("ThrowBasketball")
local v_u_8 = script:WaitForChild("DigHole")
local v_u_9 = script:WaitForChild("ArmsUp")
local v_u_10 = script:WaitForChild("SwingDown")
local v_u_11 = script:WaitForChild("AboveHead")
local function v_u_13(p12) -- name: loadAnimations
	-- upvalues: (copy) v_u_2, (copy) v_u_3, (copy) v_u_4, (copy) v_u_5, (copy) v_u_6, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10, (copy) v_u_11
	v_u_2.holdtool = p12:LoadAnimation(v_u_3)
	v_u_2.holdtool2 = p12:LoadAnimation(v_u_4)
	v_u_2.holdspade = p12:LoadAnimation(v_u_5)
	v_u_2.holdPizzaBox = p12:LoadAnimation(v_u_6)
	v_u_2.throwbasketball = p12:LoadAnimation(v_u_7)
	v_u_2.dighole = p12:LoadAnimation(v_u_8)
	v_u_2.armsup = p12:LoadAnimation(v_u_9)
	v_u_2.swingdown = p12:LoadAnimation(v_u_10)
	v_u_2.abovehead = p12:LoadAnimation(v_u_11)
end
local v_u_14 = {
	["Bucket"] = true,
	["PenguinAntarctica"] = true
}
local v_u_15 = {
	["PizzaBox"] = true
}
local v_u_16 = {
	["Hay"] = true,
	["Surfboard"] = true
}
local v_u_17 = {
	["GlassBlower"] = true
}
local function v_u_21(p18) -- name: setupRightHand
	-- upvalues: (copy) v_u_14, (copy) v_u_2, (copy) v_u_16, (copy) v_u_15, (copy) v_u_17
	p18.ChildAdded:Connect(function(p19)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if p19:IsA("BasePart") or p19:IsA("Model") then
			if v_u_14[p19.Name] then
				v_u_2.holdtool2:Play()
				return
			end
			if v_u_16[p19.Name] then
				v_u_2.abovehead:Play()
				return
			end
			if v_u_15[p19.Name] then
				v_u_2.holdPizzaBox:Play()
				return
			end
			if not v_u_17[p19.Name] then
				v_u_2.holdtool:Play()
			end
		end
	end)
	p18.ChildRemoved:Connect(function(p20)
		-- upvalues: (ref) v_u_14, (ref) v_u_2, (ref) v_u_16, (ref) v_u_15, (ref) v_u_17
		if v_u_14[p20.Name] then
			v_u_2.holdtool2:Stop()
			return
		elseif v_u_16[p20.Name] then
			v_u_2.abovehead:Stop()
			return
		elseif v_u_15[p20.Name] then
			v_u_2.holdPizzaBox:Stop()
		elseif not v_u_17[p20.Name] then
			v_u_2.holdtool:Stop()
		end
	end)
end
local function v28(p_u_22) -- name: setupCharacter
	-- upvalues: (copy) v_u_13, (copy) v_u_21
	local v23 = p_u_22:WaitForChild("Humanoid")
	v_u_13((v23:WaitForChild("Animator")))
	p_u_22.ChildAdded:Connect(function(p24)
		-- upvalues: (copy) p_u_22, (ref) v_u_21
		local v25 = p24.Name == "RightHand" and p_u_22:FindFirstChild("RightHand")
		if v25 then
			v_u_21(v25)
		end
	end)
	local v26 = p_u_22:FindFirstChild("RightHand")
	if v26 then
		v_u_21(v26)
	end
	v23.ChildAdded:Connect(function(p27)
		-- upvalues: (ref) v_u_13
		if p27:IsA("Animator") then
			v_u_13(p27)
		end
	end)
end
v1.CharacterAdded:Connect(v28)
if v1.Character then
	v28(v1.Character)
end

==================================================
-- Workspace.turbobrutti.Health
==================================================
-- failed to get script bytecode

==================================================
-- Workspace.turbobrutti.Animate
==================================================
local v_u_1 = script.Parent
local v_u_2 = v_u_1:WaitForChild("Humanoid")
local v_u_3 = "Standing"
local function v_u_4() -- name: getRigScale
	-- upvalues: (copy) v_u_1
	return v_u_1:GetScale()
end
local v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
local v6, v7 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimateRemoveEmoteChatHook")
end)
local v8 = v6 and v7
local v_u_9 = ""
local v_u_10 = nil
local v_u_11 = nil
local v_u_12 = nil
local v_u_13 = 1
local v_u_14 = nil
local v_u_15 = nil
local v_u_16 = {}
local v_u_17 = {}
local v_u_18 = {
	["idle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507766666",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766951",
			["weight"] = 1
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507766388",
			["weight"] = 9
		}
	},
	["walk"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777826",
			["weight"] = 10
		}
	},
	["run"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767714",
			["weight"] = 10
		}
	},
	["swim"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507784897",
			["weight"] = 10
		}
	},
	["swimidle"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507785072",
			["weight"] = 10
		}
	},
	["jump"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765000",
			["weight"] = 10
		}
	},
	["fall"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507767968",
			["weight"] = 10
		}
	},
	["climb"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507765644",
			["weight"] = 10
		}
	},
	["sit"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=2506281703",
			["weight"] = 10
		}
	},
	["toolnone"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507768375",
			["weight"] = 10
		}
	},
	["toolslash"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522635514",
			["weight"] = 10
		}
	},
	["toollunge"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=522638767",
			["weight"] = 10
		}
	},
	["wave"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770239",
			["weight"] = 10
		}
	},
	["point"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770453",
			["weight"] = 10
		}
	},
	["dance"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507771019",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507771955",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507772104",
			["weight"] = 10
		}
	},
	["dance2"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507776043",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776720",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507776879",
			["weight"] = 10
		}
	},
	["dance3"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507777268",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777451",
			["weight"] = 10
		},
		{
			["id"] = "http://www.roblox.com/asset/?id=507777623",
			["weight"] = 10
		}
	},
	["laugh"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770818",
			["weight"] = 10
		}
	},
	["cheer"] = {
		{
			["id"] = "http://www.roblox.com/asset/?id=507770677",
			["weight"] = 10
		}
	}
}
local v_u_19 = {
	["wave"] = false,
	["point"] = false,
	["dance"] = true,
	["dance2"] = true,
	["dance3"] = true,
	["laugh"] = false,
	["cheer"] = false
}
local v_u_20 = nil
local v_u_21 = nil
local v_u_22 = nil
local v_u_23 = nil
local v_u_24 = nil
local v25, v26 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserAnimationAbilityManagerFixed")
end)
local v_u_27 = v25 and v26
function resetManagerListeners() -- name: resetManagerListeners
	-- upvalues: (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if v_u_20 then
		v_u_20:Disconnect()
		v_u_20 = nil
	end
	if v_u_21 then
		v_u_21:Disconnect()
		v_u_21 = nil
	end
	if v_u_22 then
		v_u_22:Disconnect()
		v_u_22 = nil
	end
end
function teardownManager() -- name: teardownManager
	-- upvalues: (ref) v_u_23, (ref) v_u_24
	resetManagerListeners()
	v_u_23 = nil
	v_u_24 = nil
end
function processIfManagerBelongsToCharacter(p_u_28) -- name: processIfManagerBelongsToCharacter
	-- upvalues: (copy) v_u_1, (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (ref) v_u_22
	if p_u_28.RootPart ~= v_u_1.PrimaryPart then
		return false
	end
	if v_u_24 ~= p_u_28 then
		resetManagerListeners()
		v_u_23 = p_u_28.GroundSensor
		v_u_20 = p_u_28:GetPropertyChangedSignal("GroundSensor"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_20
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_20:Disconnect()
				v_u_20 = nil
			end
		end)
		v_u_21 = p_u_28:GetPropertyChangedSignal("RootPart"):Connect(function()
			-- upvalues: (copy) p_u_28, (ref) v_u_21
			if processIfManagerBelongsToCharacter(p_u_28) then
				v_u_21:Disconnect()
				v_u_21 = nil
			end
		end)
		v_u_22 = p_u_28.AncestryChanged:Connect(function(_, p29)
			if p29 == nil then
				resetManagerListeners()
				lookForControllerManager()
			end
		end)
		v_u_24 = p_u_28
	end
	return true
end
function setupManager(p_u_30) -- name: setupManager
	-- upvalues: (ref) v_u_24, (ref) v_u_23, (ref) v_u_20, (ref) v_u_21, (copy) v_u_1, (ref) v_u_22
	v_u_24 = p_u_30
	v_u_23 = p_u_30.GroundSensor
	v_u_20 = p_u_30:GetPropertyChangedSignal("GroundSensor"):Connect(function()
		-- upvalues: (ref) v_u_23, (ref) v_u_24
		v_u_23 = v_u_24.GroundSensor
	end)
	v_u_21 = p_u_30:GetPropertyChangedSignal("RootPart"):Connect(function()
		-- upvalues: (copy) p_u_30, (ref) v_u_1
		if p_u_30.RootPart ~= v_u_1.PrimaryPart then
			teardownManager()
			lookForControllerManager()
		end
	end)
	v_u_22 = p_u_30.AncestryChanged:Connect(function(_, p31)
		if p31 == nil then
			teardownManager()
			lookForControllerManager()
		end
	end)
end
function lookForControllerManager() -- name: lookForControllerManager
	-- upvalues: (ref) v_u_27, (copy) v_u_1, (ref) v_u_23, (ref) v_u_24
	if v_u_27 then
		local v_u_32 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v_u_32 then
			if v_u_32.RootPart == v_u_1.PrimaryPart then
				setupManager(v_u_32)
			else
				local v_u_33 = nil
				v_u_33 = v_u_32:GetPropertyChangedSignal("RootPart"):Connect(function()
					-- upvalues: (copy) v_u_32, (ref) v_u_1, (ref) v_u_33
					if v_u_32.RootPart == v_u_1.PrimaryPart then
						v_u_33:Disconnect()
						setupManager(v_u_32)
					end
				end)
			end
		else
			local v_u_34 = nil
			v_u_34 = v_u_1.ChildAdded:Connect(function(p35)
				-- upvalues: (ref) v_u_34
				if p35:IsA("ControllerManager") then
					v_u_34:Disconnect()
					lookForControllerManager()
				end
			end)
			return
		end
	else
		v_u_23 = nil
		v_u_24 = nil
		local v36 = v_u_1:FindFirstChildOfClass("ControllerManager")
		if v36 then
			processIfManagerBelongsToCharacter(v36)
		end
		if v_u_24 == nil then
			local v_u_37 = nil
			v_u_37 = v_u_1.ChildAdded:Connect(function(p38)
				-- upvalues: (ref) v_u_37
				if p38:IsA("ControllerManager") and processIfManagerBelongsToCharacter(p38) then
					v_u_37:Disconnect()
					v_u_37 = nil
				end
			end)
		end
		return
	end
end
lookForControllerManager()
math.randomseed(tick())
function findExistingAnimationInSet(p39, p40) -- name: findExistingAnimationInSet
	if p39 == nil or p40 == nil then
		return 0
	end
	for v41 = 1, p39.count do
		if p39[v41].anim.AnimationId == p40.AnimationId then
			return v41
		end
	end
	return 0
end
function configureAnimationSet(p_u_42, p_u_43) -- name: configureAnimationSet
	-- upvalues: (copy) v_u_17, (copy) v_u_16, (copy) v_u_2
	if v_u_17[p_u_42] ~= nil then
		for _, v44 in pairs(v_u_17[p_u_42].connections) do
			v44:disconnect()
		end
	end
	v_u_17[p_u_42] = {}
	v_u_17[p_u_42].count = 0
	v_u_17[p_u_42].totalWeight = 0
	v_u_17[p_u_42].connections = {}
	local v_u_45 = true
	local v46, _ = pcall(function()
		-- upvalues: (ref) v_u_45
		v_u_45 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_45 = not v46 and true or v_u_45
	local v47 = script:FindFirstChild(p_u_42)
	if v_u_45 and v47 ~= nil then
		local v48 = v_u_17[p_u_42].connections
		local v49 = v47.ChildAdded
		table.insert(v48, v49:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		local v50 = v_u_17[p_u_42].connections
		local v51 = v47.ChildRemoved
		table.insert(v50, v51:connect(function(_)
			-- upvalues: (copy) p_u_42, (copy) p_u_43
			configureAnimationSet(p_u_42, p_u_43)
		end))
		for _, v52 in pairs(v47:GetChildren()) do
			if v52:IsA("Animation") then
				local v53 = v52:FindFirstChild("Weight")
				local v54 = v53 == nil and 1 or v53.Value
				v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
				local v55 = v_u_17[p_u_42].count
				v_u_17[p_u_42][v55] = {}
				v_u_17[p_u_42][v55].anim = v52
				v_u_17[p_u_42][v55].weight = v54
				v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v_u_17[p_u_42][v55].weight
				local v56 = v_u_17[p_u_42].connections
				local v57 = v52.Changed
				table.insert(v56, v57:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v58 = v_u_17[p_u_42].connections
				local v59 = v52.ChildAdded
				table.insert(v58, v59:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
				local v60 = v_u_17[p_u_42].connections
				local v61 = v52.ChildRemoved
				table.insert(v60, v61:connect(function(_)
					-- upvalues: (copy) p_u_42, (copy) p_u_43
					configureAnimationSet(p_u_42, p_u_43)
				end))
			end
		end
	end
	if v_u_17[p_u_42].count <= 0 then
		for v62, v63 in pairs(p_u_43) do
			v_u_17[p_u_42][v62] = {}
			v_u_17[p_u_42][v62].anim = Instance.new("Animation")
			v_u_17[p_u_42][v62].anim.Name = p_u_42
			v_u_17[p_u_42][v62].anim.AnimationId = v63.id
			v_u_17[p_u_42][v62].weight = v63.weight
			v_u_17[p_u_42].count = v_u_17[p_u_42].count + 1
			v_u_17[p_u_42].totalWeight = v_u_17[p_u_42].totalWeight + v63.weight
		end
	end
	for _, v64 in pairs(v_u_17) do
		for v65 = 1, v64.count do
			if v_u_16[v64[v65].anim.AnimationId] == nil then
				v_u_2:LoadAnimation(v64[v65].anim)
				v_u_16[v64[v65].anim.AnimationId] = true
			end
		end
	end
end
function configureAnimationSetOld(p_u_66, p_u_67) -- name: configureAnimationSetOld
	-- upvalues: (copy) v_u_17, (copy) v_u_2
	if v_u_17[p_u_66] ~= nil then
		for _, v68 in pairs(v_u_17[p_u_66].connections) do
			v68:disconnect()
		end
	end
	v_u_17[p_u_66] = {}
	v_u_17[p_u_66].count = 0
	v_u_17[p_u_66].totalWeight = 0
	v_u_17[p_u_66].connections = {}
	local v_u_69 = true
	local v70, _ = pcall(function()
		-- upvalues: (ref) v_u_69
		v_u_69 = game:GetService("StarterPlayer").AllowCustomAnimations
	end)
	v_u_69 = not v70 and true or v_u_69
	local v71 = script:FindFirstChild(p_u_66)
	if v_u_69 and v71 ~= nil then
		local v72 = v_u_17[p_u_66].connections
		local v73 = v71.ChildAdded
		table.insert(v72, v73:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v74 = v_u_17[p_u_66].connections
		local v75 = v71.ChildRemoved
		table.insert(v74, v75:connect(function(_)
			-- upvalues: (copy) p_u_66, (copy) p_u_67
			configureAnimationSet(p_u_66, p_u_67)
		end))
		local v76 = 1
		for _, v77 in pairs(v71:GetChildren()) do
			if v77:IsA("Animation") then
				local v78 = v_u_17[p_u_66].connections
				local v79 = v77.Changed
				table.insert(v78, v79:connect(function(_)
					-- upvalues: (copy) p_u_66, (copy) p_u_67
					configureAnimationSet(p_u_66, p_u_67)
				end))
				v_u_17[p_u_66][v76] = {}
				v_u_17[p_u_66][v76].anim = v77
				local v80 = v77:FindFirstChild("Weight")
				if v80 == nil then
					v_u_17[p_u_66][v76].weight = 1
				else
					v_u_17[p_u_66][v76].weight = v80.Value
				end
				v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
				v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v_u_17[p_u_66][v76].weight
				v76 = v76 + 1
			end
		end
	end
	if v_u_17[p_u_66].count <= 0 then
		for v81, v82 in pairs(p_u_67) do
			v_u_17[p_u_66][v81] = {}
			v_u_17[p_u_66][v81].anim = Instance.new("Animation")
			v_u_17[p_u_66][v81].anim.Name = p_u_66
			v_u_17[p_u_66][v81].anim.AnimationId = v82.id
			v_u_17[p_u_66][v81].weight = v82.weight
			v_u_17[p_u_66].count = v_u_17[p_u_66].count + 1
			v_u_17[p_u_66].totalWeight = v_u_17[p_u_66].totalWeight + v82.weight
		end
	end
	for _, v83 in pairs(v_u_17) do
		for v84 = 1, v83.count do
			v_u_2:LoadAnimation(v83[v84].anim)
		end
	end
end
function scriptChildModified(p85) -- name: scriptChildModified
	-- upvalues: (copy) v_u_18
	local v86 = v_u_18[p85.Name]
	if v86 ~= nil then
		configureAnimationSet(p85.Name, v86)
	end
end
script.ChildAdded:connect(scriptChildModified)
script.ChildRemoved:connect(scriptChildModified)
local v87
if v_u_2 then
	v87 = v_u_2:FindFirstChildOfClass("Animator")
else
	v87 = nil
end
local v_u_88, v_u_89
if v87 then
	local v90 = v87:GetPlayingAnimationTracks()
	v_u_88 = v_u_23
	v_u_89 = v_u_24
	for _, v91 in ipairs(v90) do
		v91:Stop(0)
		v91:Destroy()
	end
else
	v_u_88 = v_u_23
	v_u_89 = v_u_24
end
for v92, v93 in pairs(v_u_18) do
	configureAnimationSet(v92, v93)
end
local v_u_94 = "None"
local v_u_95 = 0
local v_u_96 = 0
local v_u_97 = false
function stopAllAnimations() -- name: stopAllAnimations
	-- upvalues: (ref) v_u_9, (copy) v_u_19, (ref) v_u_97, (ref) v_u_10, (ref) v_u_12, (ref) v_u_11, (ref) v_u_15, (ref) v_u_14
	local v98 = v_u_9
	local v99 = v_u_19[v98] ~= nil and v_u_19[v98] == false and "idle" or v98
	if v_u_97 then
		v99 = "idle"
		v_u_97 = false
	end
	v_u_9 = ""
	v_u_10 = nil
	if v_u_12 ~= nil then
		v_u_12:disconnect()
	end
	if v_u_11 ~= nil then
		v_u_11:Stop()
		v_u_11:Destroy()
		v_u_11 = nil
	end
	if v_u_15 ~= nil then
		v_u_15:disconnect()
	end
	if v_u_14 ~= nil then
		v_u_14:Stop()
		v_u_14:Destroy()
		v_u_14 = nil
	end
	return v99
end
function getHeightScale() -- name: getHeightScale
	-- upvalues: (copy) v_u_2, (copy) v_u_4, (ref) v_u_5
	if not v_u_2 then
		return v_u_4()
	end
	if not v_u_2.AutomaticScalingEnabled then
		return v_u_4()
	end
	local v100 = v_u_2.HipHeight / 2
	if v_u_5 == nil then
		v_u_5 = script:FindFirstChild("ScaleDampeningPercent")
	end
	if v_u_5 ~= nil then
		v100 = 1 + (v_u_2.HipHeight - 2) * v_u_5.Value / 2
	end
	return v100
end
local function v_u_106(p101) -- name: setRunSpeed
	-- upvalues: (ref) v_u_11, (ref) v_u_14
	local v102 = p101 * 1.25 / getHeightScale()
	local v103 = 0.0001
	local v104 = 0.0001
	local v105 = 1
	if v102 <= 0.5 then
		v105 = v102 / 0.5
		v103 = 1
	elseif v102 < 1 then
		v104 = (v102 - 0.5) / 0.5
		v103 = 1 - v104
	else
		v105 = v102 / 1
		v104 = 1
	end
	v_u_11:AdjustWeight(v103)
	v_u_14:AdjustWeight(v104)
	v_u_11:AdjustSpeed(v105)
	v_u_14:AdjustSpeed(v105)
end
function setAnimationSpeed(p107) -- name: setAnimationSpeed
	-- upvalues: (ref) v_u_9, (copy) v_u_106, (ref) v_u_13, (ref) v_u_11
	if v_u_9 == "walk" then
		v_u_106(p107)
	elseif p107 ~= v_u_13 then
		v_u_13 = p107
		v_u_11:AdjustSpeed(v_u_13)
	end
end
function keyFrameReachedFunc(p108) -- name: keyFrameReachedFunc
	-- upvalues: (ref) v_u_9, (ref) v_u_14, (ref) v_u_11, (copy) v_u_19, (ref) v_u_97, (ref) v_u_13, (copy) v_u_2
	if p108 == "End" then
		if v_u_9 == "walk" then
			if v_u_14.Looped ~= true then
				v_u_14.TimePosition = 0
			end
			if v_u_11.Looped ~= true then
				v_u_11.TimePosition = 0
				return
			end
		else
			local v109 = v_u_9
			local v110 = v_u_19[v109] ~= nil and v_u_19[v109] == false and "idle" or v109
			if v_u_97 then
				if v_u_11.Looped then
					return
				end
				v110 = "idle"
				v_u_97 = false
			end
			local v111 = v_u_13
			playAnimation(v110, 0.15, v_u_2)
			setAnimationSpeed(v111)
		end
	end
end
function rollAnimation(p112) -- name: rollAnimation
	-- upvalues: (copy) v_u_17
	local v113 = math.random(1, v_u_17[p112].totalWeight)
	local v114 = 1
	while v_u_17[p112][v114].weight < v113 do
		v113 = v113 - v_u_17[p112][v114].weight
		v114 = v114 + 1
	end
	return v114
end
local function v_u_120(p115, p116, p117, p118) -- name: switchToAnim
	-- upvalues: (ref) v_u_10, (ref) v_u_11, (ref) v_u_14, (ref) v_u_13, (ref) v_u_9, (ref) v_u_12, (copy) v_u_17, (ref) v_u_15
	if p115 ~= v_u_10 then
		if v_u_11 ~= nil then
			v_u_11:Stop(p117)
			v_u_11:Destroy()
		end
		if v_u_14 ~= nil then
			v_u_14:Stop(p117)
			v_u_14:Destroy()
			v_u_14 = nil
		end
		v_u_13 = 1
		v_u_11 = p118:LoadAnimation(p115)
		v_u_11.Priority = Enum.AnimationPriority.Core
		v_u_11:Play(p117)
		v_u_9 = p116
		v_u_10 = p115
		if v_u_12 ~= nil then
			v_u_12:disconnect()
		end
		v_u_12 = v_u_11.KeyframeReached:connect(keyFrameReachedFunc)
		if p116 == "walk" then
			local v119 = rollAnimation("run")
			v_u_14 = p118:LoadAnimation(v_u_17.run[v119].anim)
			v_u_14.Priority = Enum.AnimationPriority.Core
			v_u_14:Play(p117)
			if v_u_15 ~= nil then
				v_u_15:disconnect()
			end
			v_u_15 = v_u_14.KeyframeReached:connect(keyFrameReachedFunc)
		end
	end
end
function playAnimation(p121, p122, p123) -- name: playAnimation
	-- upvalues: (copy) v_u_17, (copy) v_u_120, (ref) v_u_97
	local v124 = rollAnimation(p121)
	v_u_120(v_u_17[p121][v124].anim, p121, p122, p123)
	v_u_97 = false
end
function playEmote(p125, p126, p127) -- name: playEmote
	-- upvalues: (copy) v_u_120, (ref) v_u_97
	v_u_120(p125, p125.Name, p126, p127)
	v_u_97 = true
end
local v_u_128 = ""
local v_u_129 = nil
local v_u_130 = nil
local v_u_131 = nil
function toolKeyFrameReachedFunc(p132) -- name: toolKeyFrameReachedFunc
	-- upvalues: (ref) v_u_128, (copy) v_u_2
	if p132 == "End" then
		playToolAnimation(v_u_128, 0, v_u_2)
	end
end
function playToolAnimation(p133, p134, p135, p136) -- name: playToolAnimation
	-- upvalues: (copy) v_u_17, (ref) v_u_130, (ref) v_u_129, (ref) v_u_128, (ref) v_u_131
	local v137 = rollAnimation(p133)
	local v138 = v_u_17[p133][v137].anim
	if v_u_130 ~= v138 then
		if v_u_129 ~= nil then
			v_u_129:Stop()
			v_u_129:Destroy()
			p134 = 0
		end
		v_u_129 = p135:LoadAnimation(v138)
		if p136 then
			v_u_129.Priority = p136
		end
		v_u_129:Play(p134)
		v_u_128 = p133
		v_u_130 = v138
		v_u_131 = v_u_129.KeyframeReached:connect(toolKeyFrameReachedFunc)
	end
end
function stopToolAnimations() -- name: stopToolAnimations
	-- upvalues: (ref) v_u_128, (ref) v_u_131, (ref) v_u_130, (ref) v_u_129
	local v139 = v_u_128
	if v_u_131 ~= nil then
		v_u_131:disconnect()
	end
	v_u_128 = ""
	v_u_130 = nil
	if v_u_129 ~= nil then
		v_u_129:Stop()
		v_u_129:Destroy()
		v_u_129 = nil
	end
	return v139
end
function onRunning(p140) -- name: onRunning
	-- upvalues: (ref) v_u_88, (copy) v_u_2, (ref) v_u_89, (ref) v_u_97, (ref) v_u_3, (copy) v_u_19, (ref) v_u_9
	local v141 = getHeightScale()
	if v_u_88 ~= nil and v_u_2.EvaluateStateMachine == false then
		local v142 = v_u_2.RootPart
		local v143 = v_u_88.SensedPart
		if v143 then
			local v144 = v143:GetVelocityAtPosition(v_u_88.HitFrame.Position)
			local v145 = v142.AssemblyLinearVelocity
			local v146 = v145.X - v144.X
			local v147 = v145.Z - v144.Z
			local v148 = Vector3.new(v146, 0, v147).Magnitude
			local v149 = v_u_89.MovingDirection.Magnitude
			if v149 < 0.1 then
				v148 = 0
				v149 = 0
			elseif v149 > 1 then
				v149 = 1
			end
			p140 = v148 * v149
		end
	end
	local v150 = v_u_97
	if v150 then
		v150 = v_u_2.MoveDirection == Vector3.new(0, 0, 0)
	end
	if (v150 and (v_u_2.WalkSpeed / v141 or 0.75) or 0.75) * v141 < p140 then
		playAnimation("walk", 0.2, v_u_2)
		setAnimationSpeed(p140 / 16)
		v_u_3 = "Running"
	elseif v_u_19[v_u_9] == nil and not v_u_97 then
		playAnimation("idle", 0.2, v_u_2)
		v_u_3 = "Standing"
	end
end
function onDied() -- name: onDied
	-- upvalues: (ref) v_u_3
	v_u_3 = "Dead"
end
function onJumping() -- name: onJumping
	-- upvalues: (copy) v_u_2, (ref) v_u_96, (ref) v_u_3
	playAnimation("jump", 0.1, v_u_2)
	v_u_96 = 0.31
	v_u_3 = "Jumping"
end
function onClimbing(p151) -- name: onClimbing
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v152 = p151 / getHeightScale()
	playAnimation("climb", 0.1, v_u_2)
	setAnimationSpeed(v152 / 5)
	v_u_3 = "Climbing"
end
function onGettingUp() -- name: onGettingUp
	-- upvalues: (ref) v_u_3
	v_u_3 = "GettingUp"
end
function onFreeFall() -- name: onFreeFall
	-- upvalues: (ref) v_u_96, (copy) v_u_2, (ref) v_u_3
	if v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	end
	v_u_3 = "FreeFall"
end
function onFallingDown() -- name: onFallingDown
	-- upvalues: (ref) v_u_3
	v_u_3 = "FallingDown"
end
function onSeated() -- name: onSeated
	-- upvalues: (ref) v_u_3
	v_u_3 = "Seated"
end
function onPlatformStanding() -- name: onPlatformStanding
	-- upvalues: (ref) v_u_3
	v_u_3 = "PlatformStanding"
end
function onSwimming(p153) -- name: onSwimming
	-- upvalues: (copy) v_u_2, (ref) v_u_3
	local v154 = p153 / getHeightScale()
	if v154 > 1 then
		playAnimation("swim", 0.4, v_u_2)
		setAnimationSpeed(v154 / 10)
		v_u_3 = "Swimming"
	else
		playAnimation("swimidle", 0.4, v_u_2)
		v_u_3 = "Standing"
	end
end
function animateTool() -- name: animateTool
	-- upvalues: (ref) v_u_94, (copy) v_u_2
	if v_u_94 == "None" then
		playToolAnimation("toolnone", 0.1, v_u_2, Enum.AnimationPriority.Idle)
		return
	elseif v_u_94 == "Slash" then
		playToolAnimation("toolslash", 0, v_u_2, Enum.AnimationPriority.Action)
		return
	elseif v_u_94 == "Lunge" then
		playToolAnimation("toollunge", 0, v_u_2, Enum.AnimationPriority.Action)
	end
end
function getToolAnim(p155) -- name: getToolAnim
	for _, v156 in ipairs(p155:GetChildren()) do
		if v156.Name == "toolanim" and v156.className == "StringValue" then
			return v156
		end
	end
	return nil
end
local v_u_157 = 0
function stepAnimate(p158) -- name: stepAnimate
	-- upvalues: (ref) v_u_157, (ref) v_u_96, (ref) v_u_3, (copy) v_u_2, (copy) v_u_1, (ref) v_u_94, (ref) v_u_95, (ref) v_u_130
	local v159 = p158 - v_u_157
	v_u_157 = p158
	if v_u_96 > 0 then
		v_u_96 = v_u_96 - v159
	end
	if v_u_3 == "FreeFall" and v_u_96 <= 0 then
		playAnimation("fall", 0.2, v_u_2)
	else
		if v_u_3 == "Seated" then
			playAnimation("sit", 0.5, v_u_2)
			return
		end
		if v_u_3 == "Running" then
			playAnimation("walk", 0.2, v_u_2)
		elseif v_u_3 == "Dead" or (v_u_3 == "GettingUp" or (v_u_3 == "FallingDown" or (v_u_3 == "Seated" or v_u_3 == "PlatformStanding"))) then
			stopAllAnimations()
		end
	end
	local v160 = v_u_1:FindFirstChildOfClass("Tool")
	if v160 and v160:FindFirstChild("Handle") then
		local v161 = getToolAnim(v160)
		if v161 then
			v_u_94 = v161.Value
			v161.Parent = nil
			v_u_95 = p158 + 0.3
		end
		if v_u_95 < p158 then
			v_u_95 = 0
			v_u_94 = "None"
		end
		animateTool()
	else
		stopToolAnimations()
		v_u_94 = "None"
		v_u_130 = nil
		v_u_95 = 0
	end
end
v_u_2.Died:connect(onDied)
v_u_2.Running:connect(onRunning)
v_u_2.Jumping:connect(onJumping)
v_u_2.Climbing:connect(onClimbing)
v_u_2.GettingUp:connect(onGettingUp)
v_u_2.FreeFalling:connect(onFreeFall)
v_u_2.FallingDown:connect(onFallingDown)
v_u_2.Seated:connect(onSeated)
v_u_2.PlatformStanding:connect(onPlatformStanding)
v_u_2.Swimming:connect(onSwimming)
if not v8 then
	game:GetService("Players").LocalPlayer.Chatted:connect(function(p162)
		-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2
		local v163 = ""
		if string.sub(p162, 1, 3) == "/e " then
			v163 = string.sub(p162, 4)
		elseif string.sub(p162, 1, 7) == "/emote " then
			v163 = string.sub(p162, 8)
		end
		if v_u_3 == "Standing" and v_u_19[v163] ~= nil then
			playAnimation(v163, 0.1, v_u_2)
		end
	end)
end
script:WaitForChild("PlayEmote").OnInvoke = function(p164)
	-- upvalues: (ref) v_u_3, (copy) v_u_19, (copy) v_u_2, (ref) v_u_11
	if v_u_3 == "Standing" then
		if v_u_19[p164] ~= nil then
			playAnimation(p164, 0.1, v_u_2)
			return true, v_u_11
		end
		if typeof(p164) ~= "Instance" or not p164:IsA("Animation") then
			return false
		end
		playEmote(p164, 0.1, v_u_2)
		return true, v_u_11
	end
end
if v_u_1.Parent ~= nil then
	playAnimation("idle", 0.1, v_u_2)
	local _ = "Standing"
end
while v_u_1.Parent ~= nil do
	local _, v165 = wait(0.1)
	stepAnimate(v165)
end

==================================================
-- Players.turbobrutti.PlayerScripts.AudioPlayer
==================================================
local v1 = game:GetService("ReplicatedStorage")
local v2 = game:GetService("SoundService")
local v3 = game:GetService("Players")
local v_u_4 = require(v1.ModuleScripts.AudioPlayer)
local v_u_5 = v2:WaitForChild("BackgroundMusic")
local v_u_6 = false
local v_u_7 = v3.LocalPlayer
local function v_u_10(p8) -- name: FadeMusic
	-- upvalues: (ref) v_u_6, (copy) v_u_7
	v_u_6 = true
	for v9 = 0.5, 0, -0.01 do
		if v_u_7:GetAttribute("Muted") ~= true then
			p8.Volume = v9
		end
		wait(0.025)
	end
	p8:Stop()
	if v_u_7:GetAttribute("Muted") ~= true then
		p8.Volume = 0.5
	end
	v_u_6 = false
	p8.TimePosition = 0
end
local function v12() -- name: UpdateBackgroundMusic
	-- upvalues: (copy) v_u_5, (ref) v_u_6, (copy) v_u_4, (copy) v_u_10
	local v11 = v_u_5:GetAttribute("Status")
	if v11 == "Play" then
		while v_u_6 == true do
			wait(0.025)
		end
		if v_u_5.IsPlaying == false then
			if v_u_5:GetAttribute("Country") == true then
				v_u_4.ChangeMusic(v_u_5:GetAttribute("Country"))
			end
			v_u_5:Play()
			return
		end
	else
		if v11 == "Fade" then
			v_u_10(v_u_5)
			return
		end
		v_u_5:Stop()
		v_u_5.TimePosition = 0
	end
end
local v_u_13 = v_u_6
local function v14() -- name: ChangeMusic
	-- upvalues: (copy) v_u_4, (copy) v_u_5
	v_u_4.ChangeMusic(v_u_5:GetAttribute("Country"))
end
for _, v_u_15 in pairs(v2:GetChildren()) do
	if v_u_15.Name ~= "BackgroundMusic" then
		v_u_15:GetAttributeChangedSignal("Status"):Connect(function()
			-- upvalues: (copy) v_u_15, (ref) v_u_13, (copy) v_u_10
			local v16 = v_u_15:GetAttribute("Status")
			if v16 == "Play" then
				while v_u_13 == true do
					wait(0.025)
				end
				if v_u_15.IsPlaying == false then
					v_u_15:Play()
					return
				end
			else
				if v16 == "Fade" then
					v_u_10(v_u_15)
					return
				end
				v_u_15:Stop()
				v_u_15.TimePosition = 0
			end
		end)
	end
end
if v_u_5:GetAttribute("Status") == "Play" then
	v_u_5:Play()
end
v_u_5:GetAttributeChangedSignal("Status"):Connect(v12)
v_u_5:GetAttributeChangedSignal("Country"):Connect(v14)

==================================================
-- Players.turbobrutti.PlayerScripts.UI
==================================================
local v_u_1 = game:GetService("StarterGui")
game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui"):SetTopbarTransparency(0)
v_u_1:SetCoreGuiEnabled(Enum.CoreGuiType.Backpack, false)
local v_u_2 = game:GetService("RunService");
(function(p3, ...) -- name: coreCall
	-- upvalues: (copy) v_u_1, (copy) v_u_2
	local v4 = {}
	for _ = 1, 8 do
		v4 = { pcall(v_u_1[p3], v_u_1, ...) }
		if v4[1] then
			break
		end
		v_u_2.Stepped:Wait()
	end
	return unpack(v4)
end)("SetCore", "ResetButtonCallback", false)

==================================================
-- Players.turbobrutti.PlayerScripts.DynamicScrolling
==================================================
local v1 = game:GetService("CollectionService")
local v_u_2 = workspace.CurrentCamera.ViewportSize.X
local function v_u_11(p3, _) -- name: resizeList
	-- upvalues: (ref) v_u_2
	if p3 and p3:FindFirstChildWhichIsA("UIListLayout") then
		if p3.Name == "Profile" then
			if v_u_2 >= 900 then
				p3.UIListLayout.Padding = UDim.new(0, 20)
			else
				p3.UIListLayout.Padding = UDim.new(0, 10)
				for _, v4 in pairs(p3:GetChildren()) do
					if v4:IsA("Frame") then
						v4.Size = UDim2.new(v4.Size.X.Scale, 0, 0, v4:GetAttribute("SmallSize"))
					end
				end
			end
		end
		if p3.Name == "Settings" then
			if v_u_2 >= 900 then
				p3.UIListLayout.Padding = UDim.new(0, 20)
				p3.BackgroundMusic.OnOff.UIStroke.Thickness = 5
				p3.BagEffects.OnOff.UIStroke.Thickness = 5
				p3.HideNames.OnOff.UIStroke.Thickness = 5
				p3.StreamingMusic.OnOff.UIStroke.Thickness = 5
			else
				p3.UIListLayout.Padding = UDim.new(0, 10)
				for _, v5 in pairs(p3:GetChildren()) do
					if v5:IsA("Frame") or (v5:IsA("TextLabel") or v5:IsA("TextButton")) then
						v5.Size = UDim2.new(v5.Size.X.Scale, 0, 0, v5:GetAttribute("SmallSize"))
					end
				end
				p3.BackgroundMusic.OnOff.UIStroke.Thickness = 2
				p3.BagEffects.OnOff.UIStroke.Thickness = 2
				p3.HideNames.OnOff.UIStroke.Thickness = 2
				p3.StreamingMusic.OnOff.UIStroke.Thickness = 2
			end
		end
		if p3.Name == "SortFilter" then
			if v_u_2 >= 900 then
				p3.UIListLayout.Padding = UDim.new(0, 10)
			else
				p3.UIListLayout.Padding = UDim.new(0, 5)
				for _, v6 in pairs(p3:GetChildren()) do
					if v6:IsA("TextButton") then
						v6.Size = UDim2.new(1, 0, 0, 12)
					elseif v6:IsA("TextLabel") then
						v6.Size = UDim2.new(1, 0, 0, 12)
					end
				end
			end
		end
		if p3.Name == "Stats" then
			if v_u_2 >= 900 then
				p3.UIListLayout.Padding = UDim.new(0, 10)
				p3.UIPadding.PaddingBottom = UDim.new(0, 10)
				p3.UIPadding.PaddingTop = UDim.new(0, 10)
				for _, v7 in pairs(p3:GetChildren()) do
					if v7:IsA("Frame") then
						v7.Size = UDim2.new(0.9, 0, 0, 36)
					end
				end
			else
				p3.UIListLayout.Padding = UDim.new(0, 5)
				p3.UIPadding.PaddingBottom = UDim.new(0, 5)
				p3.UIPadding.PaddingTop = UDim.new(0, 5)
				for _, v8 in pairs(p3:GetChildren()) do
					if v8:IsA("Frame") then
						v8.Size = UDim2.new(0.9, 0, 0, 18)
					end
				end
			end
		end
		if p3.Name == "Items" or p3.Name == "PassItems" then
			if v_u_2 >= 900 then
				p3.UIListLayout.Padding = UDim.new(0, 20)
			else
				p3.UIListLayout.Padding = UDim.new(0, 10)
				for _, v9 in pairs(p3:GetChildren()) do
					if v9:IsA("Frame") then
						if p3.Parent.Name == "TeamShop" then
							v9.Size = UDim2.new(0, 125, 0.75, 0)
						else
							v9.Size = UDim2.new(0, 125, 1, -15)
						end
					end
				end
			end
		end
		if p3.Name == "CountryList" then
			if v_u_2 >= 900 then
				p3.UIListLayout.Padding = UDim.new(0, 10)
				return
			end
			p3.UIListLayout.Padding = UDim.new(0, 5)
			for _, v10 in pairs(p3:GetChildren()) do
				if v10:IsA("TextButton") then
					v10.Size = UDim2.new(0.75, 0, 0, 25)
				end
			end
		end
	end
end
local function v_u_13(p12, _) -- name: resizeGrid
	-- upvalues: (ref) v_u_2
	if p12 and p12:FindFirstChildWhichIsA("UIGridLayout") then
		if p12.Name == "Teams" or p12.Name == "Colors" then
			if v_u_2 >= 900 then
				p12.UIGridLayout.CellSize = UDim2.new(0.2, 0, 0, 100)
			else
				p12.UIGridLayout.CellSize = UDim2.new(0.2, 0, 0, 50)
			end
		end
		if p12.Name == "BagInventory" or p12.Name == "TeamInventory" then
			if v_u_2 >= 900 then
				p12.UIGridLayout.CellPadding = UDim2.new(0.033, 0, 0, 10)
				return
			end
			p12.UIGridLayout.CellPadding = UDim2.new(0.033, 0, 0, 5)
			p12.UIGridLayout.CellSize = UDim2.new(0.3, 0, 0, 75)
		end
	end
end
local function v20(p_u_14) -- name: registerDynamicScrollingFrame
	-- upvalues: (ref) v_u_2, (copy) v_u_11, (copy) v_u_13
	local v_u_15 = p_u_14:FindFirstChildWhichIsA("UIGridStyleLayout")
	if v_u_15 == nil then
		v_u_15 = p_u_14:FindFirstChildWhichIsA("UIListLayout")
	end
	local v16 = v_u_15.AbsoluteContentSize
	if v_u_2 < 10 then
		while v_u_2 < 10 do
			v_u_2 = workspace.CurrentCamera.ViewportSize.X
			task.wait(0.25)
		end
	end
	if v_u_15 then
		if v_u_15:IsA("UIListLayout") then
			v_u_11(p_u_14, v16)
		else
			v_u_13(p_u_14, v16)
		end
		p_u_14.ChildAdded:Connect(function(_)
			-- upvalues: (ref) v_u_15, (ref) v_u_11, (copy) p_u_14, (ref) v_u_13
			local v17 = v_u_15.AbsoluteContentSize
			if v_u_15:IsA("UIListLayout") then
				v_u_11(p_u_14, v17)
			else
				v_u_13(p_u_14, v17)
			end
		end)
		p_u_14.ChildRemoved:Connect(function(_)
			-- upvalues: (ref) v_u_15, (ref) v_u_11, (copy) p_u_14, (ref) v_u_13
			local v18 = v_u_15.AbsoluteContentSize
			if v_u_15:IsA("UIListLayout") then
				v_u_11(p_u_14, v18)
			else
				v_u_13(p_u_14, v18)
			end
		end)
		p_u_14:GetPropertyChangedSignal("AbsoluteSize"):Connect(function()
			-- upvalues: (ref) v_u_15, (ref) v_u_11, (copy) p_u_14, (ref) v_u_13
			local v19 = v_u_15.AbsoluteContentSize
			if v_u_15:IsA("UIListLayout") then
				v_u_11(p_u_14, v19)
			else
				v_u_13(p_u_14, v19)
			end
		end)
	end
end
v1:GetInstanceAddedSignal("DynamicScrollingFrame"):Connect(v20)
for _, v21 in ipairs(v1:GetTagged("DynamicScrollingFrame")) do
	v20(v21)
end

==================================================
-- Players.turbobrutti.PlayerScripts.DayNight
==================================================
local v1 = game:GetService("ReplicatedStorage")
local v_u_2 = game:GetService("Lighting")
v1.PlayerEvents.DayNight.OnClientEvent:Connect(function(p3) -- name: CheckBeam
	-- upvalues: (copy) v_u_2
	if p3 == "Day" then
		v_u_2.ClockTime = 9
	else
		v_u_2.ClockTime = 22
	end
end)

==================================================
-- Players.turbobrutti.PlayerScripts.BeamDetector
==================================================
local v1 = game:GetService("Players")
local v2 = game:GetService("ReplicatedStorage")
local v_u_3 = v1.LocalPlayer
v2.PlayerEvents.Beam.OnClientEvent:Connect(function(p4) -- name: CheckBeam
	-- upvalues: (copy) v_u_3
	if v_u_3.Character and v_u_3.Character:FindFirstChild("HumanoidRootPart") then
		v_u_3.Character.HumanoidRootPart:FindFirstChildOfClass("Beam")
		local v5
		if p4 == "Cluebox" then
			v5 = v_u_3.Character.HumanoidRootPart:FindFirstChild("ClueboxBeam")
		else
			v5 = v_u_3.Character.HumanoidRootPart:FindFirstChildOfClass("Beam")
		end
		if v5 then
			v5.Enabled = true
		end
	end
end)

==================================================
-- Players.turbobrutti.PlayerScripts.PSControl
==================================================
local v1 = game:GetService("ReplicatedStorage")
local v2 = game:GetService("Players")
local v3 = v1.Data
local v4 = v1.PlayerEvents.PrivateServer
local v5 = v3.PrivateServer
local v_u_6 = v2.LocalPlayer
local v_u_7 = nil
local v_u_8 = nil
local v_u_9 = nil
local v_u_10 = nil
if v5.Value == true or table.find({ 72345597, 57245869, -1 }, v_u_6.UserId) then
	v4.OnClientEvent:Connect(function(p11)
		-- upvalues: (ref) v_u_8, (copy) v_u_6, (ref) v_u_9, (ref) v_u_10, (ref) v_u_7
		if not v_u_8 then
			v_u_8 = v_u_6.PlayerGui
		end
		if v_u_8 and v_u_8:FindFirstChild("UI") then
			v_u_9 = v_u_8.UI.PrivateServerOwnerMessage
			v_u_10 = v_u_8.UI.Commands
			v_u_10.CloseButton.Activated:Connect(function()
				-- upvalues: (ref) v_u_10
				if v_u_10 then
					v_u_10.Visible = false
				end
			end)
		end
		if v_u_10 and v_u_9 then
			if p11 == "Owner" then
				if v_u_9 then
					v_u_9:TweenSize(UDim2.new(0.75, 0, 0.1, 0), "In", "Linear", 0.5)
					return
				end
			elseif p11 == "Start" then
				if v_u_9 then
					v_u_9:TweenSize(UDim2.new(0, 0, 0.1, 0), "Out", "Linear", 0.5)
					return
				end
			elseif p11 == "Commands" then
				if v_u_10 then
					v_u_10.Visible = true
					return
				end
			elseif p11 == "Legs" then
				if not v_u_7 then
					v_u_7 = v_u_6.PlayerGui:FindFirstChild("Legs")
				end
				if v_u_7 then
					v_u_7.Frame.Visible = true
				end
			end
		end
	end)
end

==================================================
-- Players.turbobrutti.PlayerScripts.SettingsControl
==================================================
local v1 = game:GetService("Players")
local v_u_2 = game:GetService("SoundService")
local v_u_3 = game:GetService("CollectionService")
local v_u_4 = v1.LocalPlayer
local v_u_5 = false
local v_u_6 = false
local v_u_7 = true
local function v9(p8) -- name: SoundAdded
	-- upvalues: (ref) v_u_5
	if v_u_5 == true then
		p8.Volume = 0
	else
		p8.Volume = 0.5
	end
end
local function v10() -- name: UpdateMute
	-- upvalues: (ref) v_u_5, (copy) v_u_4, (copy) v_u_2
	v_u_5 = v_u_4:GetAttribute("Muted")
	if v_u_5 then
		v_u_2.BackgroundMusic.Volume = 0
		v_u_2.Elimination.Volume = 0
		v_u_2.NonElimination.Volume = 0
		v_u_2.FinishLine.Volume = 0
	else
		v_u_2.BackgroundMusic.Volume = 0.5
		v_u_2.Elimination.Volume = 0.5
		v_u_2.NonElimination.Volume = 0.5
		v_u_2.FinishLine.Volume = 0.5
	end
end
local function v14() -- name: UpdateHideNames
	-- upvalues: (ref) v_u_6, (copy) v_u_4, (copy) v_u_3
	v_u_6 = v_u_4:GetAttribute("HideNames")
	local v11 = v_u_3:GetTagged("NameBanners")
	if v_u_6 then
		for _, v12 in pairs(v11) do
			if v12 then
				v12.Enabled = false
			end
		end
	else
		for _, v13 in pairs(v11) do
			if v13 then
				v13.Enabled = true
			end
		end
	end
end
local function v16(p15) -- name: NewNameBanner
	-- upvalues: (ref) v_u_6
	if v_u_6 == true then
		p15.Enabled = false
	end
end
local function v22() -- name: UpdateBagEffects
	-- upvalues: (ref) v_u_7, (copy) v_u_4, (copy) v_u_3
	v_u_7 = v_u_4:GetAttribute("BagEffects")
	local v17 = v_u_3:GetTagged("BagEffects")
	if v_u_7 then
		for _, v18 in pairs(v17) do
			if v18 then
				for _, v19 in pairs(v18:GetDescendants()) do
					if v19:IsA("ParticleEmitter") then
						v19.Enabled = true
					elseif v19:IsA("Script") then
						v19.Disabled = false
					end
				end
			end
		end
	else
		for _, v20 in pairs(v17) do
			if v20 then
				for _, v21 in pairs(v20:GetDescendants()) do
					if v21:IsA("ParticleEmitter") then
						v21.Enabled = false
					elseif v21:IsA("Script") then
						v21.Disabled = true
					end
				end
			end
		end
	end
end
local function v25(p23) -- name: NewBagEffect
	-- upvalues: (ref) v_u_7
	if not v_u_7 then
		task.wait(5)
		if p23 then
			for _, v24 in pairs(p23:GetDescendants()) do
				if v24:IsA("ParticleEmitter") then
					v24.Enabled = false
				elseif v24:IsA("Script") then
					v24.Disabled = true
				end
			end
		end
	end
end
v_u_4:GetAttributeChangedSignal("Muted"):Connect(v10)
v_u_4:GetAttributeChangedSignal("HideNames"):Connect(v14)
v_u_4:GetAttributeChangedSignal("BagEffects"):Connect(v22)
v_u_2.ChildAdded:Connect(v9)
v_u_3:GetInstanceAddedSignal("NameBanners"):Connect(v16)
v_u_3:GetInstanceAddedSignal("BagEffects"):Connect(v25)

==================================================
-- Players.turbobrutti.PlayerScripts.Teleport
==================================================
local v1 = game:GetService("Players")
local v2 = game:GetService("ReplicatedStorage")
local v3 = v1.LocalPlayer
local v_u_4 = v2:WaitForChild("PlayerEvents"):WaitForChild("Teleport")
local v_u_5 = v3.Character or v3.CharacterAdded:Wait()
v3.CharacterAdded:Connect(function(p6)
	-- upvalues: (ref) v_u_5
	v_u_5 = p6
end)
v_u_4.OnClientEvent:Connect(function(p7, p8, p9)
	-- upvalues: (ref) v_u_5, (copy) v_u_4
	if p7 then
		if v_u_5 and v_u_5.Parent then
			local v10 = script.Parent:GetAttribute("Seat")
			if v10 and v10 ~= "" then
				return
			elseif v_u_5:FindFirstChild("HumanoidRootPart") or v_u_5.PrimaryPart then
				if p8 then
					v_u_5:SetPrimaryPartCFrame(p7 * p8)
				else
					v_u_5:SetPrimaryPartCFrame(p7)
				end
				v_u_4:FireServer(p9)
			end
		else
			return
		end
	else
		return
	end
end)

==================================================
-- Players.turbobrutti.PlayerScripts.Fly
==================================================
local v1 = game:GetService("Players")
local v_u_2 = game:GetService("TweenService")
local v3 = game:GetService("ReplicatedStorage")
local v4 = game:GetService("RunService")
game:GetService("TextChatService")
local v5 = v3.ModuleScripts
local v_u_6 = require(v5.ShiftLock)
local v_u_7 = v1.LocalPlayer
local v8 = v3.PlayerEvents
local v_u_9 = workspace:WaitForChild("Camera")
local v10 = v8.Fly
local v_u_11 = v3.Data.Loading
local v_u_12 = TweenInfo.new(5, Enum.EasingStyle.Linear, Enum.EasingDirection.Out, 0, false, 0)
local v_u_13 = TweenInfo.new(2.5, Enum.EasingStyle.Linear, Enum.EasingDirection.Out, 0, false, 0)
local v_u_14 = nil
local v_u_15 = 0
local v_u_16 = {
	["Las Vegas"] = true,
	["Rio de Janeiro"] = true,
	["Rovaniemi"] = true
}
local function v17() -- name: OnChanged
	-- upvalues: (ref) v_u_15, (ref) v_u_14, (copy) v_u_9
	if v_u_15 == 1 and v_u_14 ~= nil then
		v_u_9.CFrame = CFrame.new(v_u_14.Position) * CFrame.Angles(-1.5707963267948966, 0, -1.5707963267948966) + Vector3.new(0, 5, 0)
	end
end
v4.RenderStepped:Connect(v17)
v10.OnClientEvent:Connect(function(p18, p19)
	-- upvalues: (copy) v_u_11, (copy) v_u_6, (ref) v_u_15, (ref) v_u_14, (copy) v_u_9, (copy) v_u_2, (copy) v_u_12, (copy) v_u_13, (copy) v_u_16, (copy) v_u_7
	if p18 and p18 ~= "EndFlight" then
		v_u_11.Value = true
		task.wait(0.5)
		v_u_6.EnableDisable(false)
		v_u_15 = 1
		v_u_14 = p18
		v_u_9.CameraType = Enum.CameraType.Scriptable
		v_u_9.CameraSubject = p18
		local v20 = {
			["Position"] = nil,
			["Size"] = Vector3.new(1.2, 0.4, 1.6),
			["Position"] = p19.Position
		}
		local v21 = {
			["Position"] = nil,
			["Size"] = Vector3.new(0.05, 0.05, 0.05),
			["Position"] = p19.Position
		}
		v_u_11.Value = false
		task.wait(0.5)
		local v22 = v_u_2:Create(p18, v_u_12, v20)
		v22:Play()
		task.wait(2.5)
		v22:Pause()
		v_u_2:Create(p18, v_u_13, v21):Play()
	elseif p18 and p18 == "EndFlight" then
		v_u_11.Value = true
		task.wait(0.5)
		if v_u_16[p19] then
			game.Lighting.ClockTime = 22
		else
			game.Lighting.ClockTime = 9
		end
		v_u_15 = 0
		v_u_14 = nil
		v_u_9.CFrame = v_u_7.Character.HumanoidRootPart.CFrame
		v_u_9.CameraType = Enum.CameraType.Custom
		v_u_9.CameraSubject = v_u_7.Character.Humanoid
		v_u_11.Value = false
		v_u_6.EnableDisable(true)
	end
end)

==================================================
-- Players.turbobrutti.PlayerScripts.GuiControl
==================================================
local v1 = game:GetService("ReplicatedStorage")
local v2 = game:GetService("Players")
local v3 = v1.PlayerEvents
local v_u_4 = v1.Challenges
local v5 = v3.ChallengeSetUp
local v_u_6 = v2.LocalPlayer
v5.OnClientEvent:Connect(function(p7, p8, p9) -- name: SetUpChallenges
	-- upvalues: (copy) v_u_4, (copy) v_u_6
	if v_u_4:FindFirstChild(p8) then
		for _, v10 in pairs(p7) do
			local v11 = v_u_4[p8]:FindFirstChild(v10)
			if v11 then
				for _, v12 in pairs(v11:GetChildren()) do
					local v13 = v_u_6.PlayerGui.Challenges:FindFirstChild(v12.Name)
					if v13 and p9 == true then
						v13:Destroy()
					elseif p9 == false then
						v12:Clone().Parent = v_u_6.PlayerGui.Challenges
					end
				end
			end
		end
	end
end)

==================================================
-- Players.turbobrutti.PlayerScripts.Director
==================================================
local v_u_1 = game:GetService("TweenService")
local v2 = game:GetService("ReplicatedStorage")
local v3 = game:GetService("Players").LocalPlayer
local v4 = v2:WaitForChild("ModuleScripts")
local v_u_5 = require(v4:WaitForChild("ShiftLock"))
local v_u_6 = v2:WaitForChild("Cameras")
local v_u_7 = workspace:WaitForChild("Camera")
local v_u_8 = v2:WaitForChild("Data"):WaitForChild("Camera")
local v_u_9 = nil
local function v_u_13(p10, p11) -- name: cutscene
	-- upvalues: (copy) v_u_7, (copy) v_u_1
	local v12 = TweenInfo.new(5, Enum.EasingStyle.Sine, Enum.EasingDirection.Out, 0, false, 0)
	v_u_7.CameraType = Enum.CameraType.Scriptable
	v_u_7.CFrame = p10.CFrame
	v_u_1:Create(v_u_7, v12, {
		["CFrame"] = p11.CFrame
	}):Play()
end
local function v15() -- name: ChangeCamera
	-- upvalues: (copy) v_u_8, (copy) v_u_7, (copy) v_u_5, (ref) v_u_9, (copy) v_u_6, (copy) v_u_13
	local v14 = v_u_8.Value
	if v14 == "Reset" then
		v_u_7.CameraType = Enum.CameraType.Custom
		v_u_5.EnableDisable(true)
	else
		v_u_5.EnableDisable(false)
		v_u_9 = v_u_6:FindFirstChild(v14)
		if v_u_9 then
			v_u_13(v_u_9.Start, v_u_9.Finish)
		end
	end
end
local function v_u_18(p16, p17) -- name: PlayerSitting
	-- upvalues: (copy) v_u_5
	if p16 and p17 then
		script.Parent:SetAttribute("Seat", p17.Parent.Name)
		v_u_5.EnableDisable(false)
		print("Seated")
	else
		script.Parent:SetAttribute("Seat", "")
		v_u_5.EnableDisable(true)
		print("Not Seated")
	end
end
local function v20(p19) -- name: OnCharacterAdded
	-- upvalues: (copy) v_u_18
	p19:WaitForChild("Humanoid").Seated:Connect(v_u_18)
end
if v3.Character then
	v3.Character:WaitForChild("Humanoid").Seated:Connect(v_u_18)
end
v3.CharacterAdded:Connect(v20)
v_u_8:GetPropertyChangedSignal("Value"):Connect(v15)

==================================================
-- Players.turbobrutti.PlayerScripts.RbxCharacterSounds
==================================================
local v_u_1 = game:GetService("Players")
local v_u_2 = game:GetService("RunService")
local v_u_3 = game:GetService("SoundService")
local v4 = require(script:WaitForChild("AtomicBinding"))
local v_u_5 = "UserSoundsUseRelativeVelocity2"
local v6, v7 = pcall(function()
	-- upvalues: (copy) v_u_5
	return UserSettings():IsUserFeatureEnabled(v_u_5)
end)
local v_u_8 = v6 and v7
local v_u_9 = "UserNewCharacterSoundsApi3"
local v10, v11 = pcall(function()
	-- upvalues: (copy) v_u_9
	return UserSettings():IsUserFeatureEnabled(v_u_9)
end)
local v_u_12 = v10 and v11
local v_u_13 = "UserFixCharSoundsEmitters"
local v14, v15 = pcall(function()
	-- upvalues: (copy) v_u_13
	return UserSettings():IsUserFeatureEnabled(v_u_13)
end)
local v_u_16 = v14 and v15
local v_u_17 = "UserFixCharSoundsEmitterRootPart"
local v18, v19 = pcall(function()
	-- upvalues: (copy) v_u_17
	return UserSettings():IsUserFeatureEnabled(v_u_17)
end)
local v_u_20 = v18 and v19
local v_u_21 = {
	["Climbing"] = {
		["SoundId"] = "rbxasset://sounds/action_footsteps_plastic.mp3",
		["Looped"] = true
	},
	["Died"] = {
		["SoundId"] = "rbxasset://sounds/uuhhh.mp3"
	},
	["FreeFalling"] = {
		["SoundId"] = "rbxasset://sounds/action_falling.ogg",
		["Looped"] = true
	},
	["GettingUp"] = {
		["SoundId"] = "rbxasset://sounds/action_get_up.mp3"
	},
	["Jumping"] = {
		["SoundId"] = "rbxasset://sounds/action_jump.mp3"
	},
	["Landing"] = {
		["SoundId"] = "rbxasset://sounds/action_jump_land.mp3"
	},
	["Running"] = {
		["SoundId"] = "rbxasset://sounds/action_footsteps_plastic.mp3",
		["Looped"] = true,
		["Pitch"] = 1.85
	},
	["Splash"] = {
		["SoundId"] = "rbxasset://sounds/impact_water.mp3"
	},
	["Swimming"] = {
		["SoundId"] = "rbxasset://sounds/action_swim.mp3",
		["Looped"] = true,
		["Pitch"] = 1.6
	}
}
local v_u_22 = {
	["Climbing"] = {
		["AssetId"] = "rbxasset://sounds/action_footsteps_plastic.mp3",
		["Looping"] = true
	},
	["Died"] = {
		["AssetId"] = "rbxasset://sounds/uuhhh.mp3"
	},
	["FreeFalling"] = {
		["AssetId"] = "rbxasset://sounds/action_falling.ogg",
		["Looping"] = true
	},
	["GettingUp"] = {
		["AssetId"] = "rbxasset://sounds/action_get_up.mp3"
	},
	["Jumping"] = {
		["AssetId"] = "rbxasset://sounds/action_jump.mp3"
	},
	["Landing"] = {
		["AssetId"] = "rbxasset://sounds/action_jump_land.mp3"
	},
	["Running"] = {
		["AssetId"] = "rbxasset://sounds/action_footsteps_plastic.mp3",
		["Looping"] = true,
		["PlaybackSpeed"] = 1.85
	},
	["Splash"] = {
		["AssetId"] = "rbxasset://sounds/impact_water.mp3"
	},
	["Swimming"] = {
		["AssetId"] = "rbxasset://sounds/action_swim.mp3",
		["Looping"] = true,
		["PlaybackSpeed"] = 1.6
	}
}
local function v_u_26(p23, p24) -- name: getRelativeVelocity
	if p23 then
		local v25 = p23.ActiveController and (not (p23.ActiveController:IsA("GroundController") and p23.GroundSensor) and p23.ActiveController:IsA("ClimbController"))
		if v25 then
			v25 = p23.ClimbSensor
		end
		if v25 and v25.SensedPart then
			return p24 - v25.SensedPart:GetVelocityAtPosition(p23.RootPart.Position)
		else
			return p24
		end
	else
		return p24
	end
end
local v_u_103 = v4.new({
	["humanoid"] = "Humanoid",
	["rootPart"] = "HumanoidRootPart"
}, function(p27) -- name: initializeSoundSystem
	-- upvalues: (copy) v_u_8, (copy) v_u_12, (copy) v_u_3, (copy) v_u_16, (copy) v_u_20, (copy) v_u_1, (copy) v_u_22, (copy) v_u_21, (copy) v_u_26, (copy) v_u_2
	local v_u_28 = p27.humanoid
	local v_u_29 = p27.rootPart
	local v_u_30 = nil
	local v_u_31
	if v_u_8 then
		v_u_31 = v_u_28.Parent:FindFirstChild("ControllerManager")
	else
		v_u_31 = nil
	end
	local v_u_32 = {}
	if v_u_12 and v_u_3.CharacterSoundsUseNewApi == Enum.RolloutState.Enabled then
		local v33 = nil
		local v34 = nil
		if v_u_16 then
			if v_u_20 then
				v34 = v_u_28.RootPart or v_u_28.Parent
			else
				v34 = v_u_28.RootPart
			end
		else
			v33 = v_u_1.LocalPlayer.Character
		end
		local v35 = 5
		local v36 = {}
		while v35 < 150 do
			v36[v35] = 5 / v35
			v35 = v35 * 1.25
		end
		v36[150] = 0
		if v_u_16 then
			v_u_30 = Instance.new("AudioEmitter", v34)
		else
			v_u_30 = Instance.new("AudioEmitter", v33)
		end
		v_u_30.Name = "RbxCharacterSoundsEmitter"
		v_u_30:SetDistanceAttenuation(v36)
		for v37, v38 in pairs(v_u_22) do
			local v39 = Instance.new("AudioPlayer")
			local v40 = Instance.new("Wire")
			v39.Name = v37
			v40.Name = v37 .. "Wire"
			v39.Archivable = false
			v39.Volume = 0.65
			for v41, v42 in pairs(v38) do
				v39[v41] = v42
			end
			v39.Parent = v_u_29
			v40.Parent = v39
			v40.SourceInstance = v39
			v40.TargetInstance = v_u_30
			v_u_32[v37] = v39
		end
	else
		for v43, v44 in pairs(v_u_21) do
			local v45 = Instance.new("Sound")
			v45.Name = v43
			v45.Archivable = false
			v45.RollOffMinDistance = 5
			v45.RollOffMaxDistance = 150
			v45.Volume = 0.65
			for v46, v47 in pairs(v44) do
				v45[v46] = v47
			end
			v45.Parent = v_u_29
			v_u_32[v43] = v45
		end
	end
	local v_u_48 = {}
	local function v_u_57(p49) -- name: stopPlayingLoopedSounds
		-- upvalues: (copy) v_u_48, (ref) v_u_12
		local v50 = pairs
		local v51 = v_u_48
		local v52 = {}
		local v53 = p49 or nil
		for v54, v55 in pairs(v51) do
			v52[v54] = v55
		end
		for v56 in v50(v52) do
			if v56 ~= v53 then
				if v_u_12 and v56:IsA("AudioPlayer") then
					v56:Stop()
				else
					v56.Playing = false
				end
				v_u_48[v56] = nil
			end
		end
	end
	local v_u_78 = {
		[Enum.HumanoidStateType.FallingDown] = function()
			-- upvalues: (copy) v_u_57
			v_u_57()
		end,
		[Enum.HumanoidStateType.GettingUp] = function()
			-- upvalues: (copy) v_u_57, (copy) v_u_32, (ref) v_u_12
			v_u_57()
			local v58 = v_u_32.GettingUp
			v58.TimePosition = 0
			if v_u_12 and v58:IsA("AudioPlayer") then
				v58:Play()
			else
				v58.Playing = true
			end
		end,
		[Enum.HumanoidStateType.Jumping] = function()
			-- upvalues: (copy) v_u_57, (copy) v_u_32, (ref) v_u_12
			v_u_57()
			local v59 = v_u_32.Jumping
			v59.TimePosition = 0
			if v_u_12 and v59:IsA("AudioPlayer") then
				v59:Play()
			else
				v59.Playing = true
			end
		end,
		[Enum.HumanoidStateType.Swimming] = function()
			-- upvalues: (copy) v_u_29, (copy) v_u_32, (ref) v_u_12, (copy) v_u_57, (copy) v_u_48
			local v60 = v_u_29.AssemblyLinearVelocity.Y
			local v61 = math.abs(v60)
			if v61 > 0.1 then
				local v62 = v_u_32.Splash
				local v63 = (v61 - 100) * 0.72 / 250 + 0.28
				v62.Volume = math.clamp(v63, 0, 1)
				local v64 = v_u_32.Splash
				v64.TimePosition = 0
				if v_u_12 and v64:IsA("AudioPlayer") then
					v64:Play()
				else
					v64.Playing = true
				end
			end
			v_u_57(v_u_32.Swimming)
			local v65 = v_u_32.Swimming
			if v_u_12 and v65:IsA("AudioPlayer") then
				v65:Play()
			else
				v65.Playing = true
			end
			v_u_48[v_u_32.Swimming] = true
		end,
		[Enum.HumanoidStateType.Freefall] = function()
			-- upvalues: (copy) v_u_32, (copy) v_u_57, (ref) v_u_12, (copy) v_u_48
			v_u_32.FreeFalling.Volume = 0
			v_u_57(v_u_32.FreeFalling)
			local v66 = v_u_32.FreeFalling
			if v_u_12 and v66:IsA("AudioPlayer") then
				v66.Looping = true
			else
				v66.Looped = true
			end
			if v_u_32.FreeFalling:IsA("Sound") then
				v_u_32.FreeFalling.PlaybackRegionsEnabled = true
			end
			v_u_32.FreeFalling.LoopRegion = NumberRange.new(2, 9)
			local v67 = v_u_32.FreeFalling
			v67.TimePosition = 0
			if v_u_12 and v67:IsA("AudioPlayer") then
				v67:Play()
			else
				v67.Playing = true
			end
			v_u_48[v_u_32.FreeFalling] = true
		end,
		[Enum.HumanoidStateType.Landed] = function()
			-- upvalues: (copy) v_u_57, (copy) v_u_29, (copy) v_u_32, (ref) v_u_12
			v_u_57()
			local v68 = v_u_29.AssemblyLinearVelocity.Y
			local v69 = math.abs(v68)
			if v69 > 75 then
				local v70 = v_u_32.Landing
				local v71 = (v69 - 50) * 1 / 50 + 0
				v70.Volume = math.clamp(v71, 0, 1)
				local v72 = v_u_32.Landing
				v72.TimePosition = 0
				if v_u_12 and v72:IsA("AudioPlayer") then
					v72:Play()
					return
				end
				v72.Playing = true
			end
		end,
		[Enum.HumanoidStateType.Running] = function()
			-- upvalues: (copy) v_u_57, (copy) v_u_32, (ref) v_u_12, (copy) v_u_48
			v_u_57(v_u_32.Running)
			local v73 = v_u_32.Running
			if v_u_12 and v73:IsA("AudioPlayer") then
				v73:Play()
			else
				v73.Playing = true
			end
			v_u_48[v_u_32.Running] = true
		end,
		[Enum.HumanoidStateType.Climbing] = function()
			-- upvalues: (copy) v_u_32, (copy) v_u_29, (ref) v_u_8, (ref) v_u_26, (ref) v_u_31, (ref) v_u_12, (copy) v_u_57, (copy) v_u_48
			local v74 = v_u_32.Climbing
			local v75 = v_u_29.AssemblyLinearVelocity
			if v_u_8 then
				v75 = v_u_26(v_u_31, v75)
			end
			local v76 = v75.Y
			if math.abs(v76) > 0.1 then
				if v_u_12 and v74:IsA("AudioPlayer") then
					v74:Play()
				else
					v74.Playing = true
				end
				v_u_57(v74)
			else
				v_u_57()
			end
			v_u_48[v74] = true
		end,
		[Enum.HumanoidStateType.Seated] = function()
			-- upvalues: (copy) v_u_57
			v_u_57()
		end,
		[Enum.HumanoidStateType.Dead] = function()
			-- upvalues: (copy) v_u_57, (copy) v_u_32, (ref) v_u_12
			v_u_57()
			local v77 = v_u_32.Died
			v77.TimePosition = 0
			if v_u_12 and v77:IsA("AudioPlayer") then
				v77:Play()
			else
				v77.Playing = true
			end
		end
	}
	local v_u_89 = {
		[v_u_32.Climbing] = function(_, p79, p80)
			-- upvalues: (ref) v_u_8, (ref) v_u_26, (ref) v_u_31, (ref) v_u_12
			if v_u_8 then
				p80 = v_u_26(v_u_31, p80)
			end
			local v81 = p80.Magnitude > 0.1
			if v_u_12 and p79:IsA("AudioPlayer") then
				if p79.IsPlaying and not v81 then
					p79:Stop()
					return
				end
				if not p79.IsPlaying and v81 then
					p79:Play()
					return
				end
			else
				p79.Playing = v81
			end
		end,
		[v_u_32.FreeFalling] = function(p82, p83, p84)
			if p84.Magnitude > 75 then
				local v85 = p83.Volume + p82 * 0.9
				p83.Volume = math.clamp(v85, 0, 1)
			else
				p83.Volume = 0
			end
		end,
		[v_u_32.Running] = function(_, p86, p87)
			-- upvalues: (copy) v_u_28, (ref) v_u_12
			local v88
			if p87.Magnitude > 0.5 then
				v88 = v_u_28.MoveDirection.Magnitude > 0.5
			else
				v88 = false
			end
			if v_u_12 and p86:IsA("AudioPlayer") then
				if p86.IsPlaying and not v88 then
					p86:Stop()
					return
				end
				if not p86.IsPlaying and v88 then
					p86:Play()
					return
				end
			else
				p86.Playing = v88
			end
		end
	}
	local v_u_90 = {
		[Enum.HumanoidStateType.RunningNoPhysics] = Enum.HumanoidStateType.Running
	}
	local v_u_91 = v_u_90[v_u_28:GetState()] or v_u_28:GetState()
	local v92 = v_u_91
	local v93 = v_u_78[v92]
	if v93 then
		v93()
	end
	v_u_91 = v92
	local v_u_97 = v_u_28.StateChanged:Connect(function(_, p94)
		-- upvalues: (copy) v_u_90, (ref) v_u_91, (copy) v_u_78
		local v95 = v_u_90[p94] or p94
		if v95 ~= v_u_91 then
			local v96 = v_u_78[v95]
			if v96 then
				v96()
			end
			v_u_91 = v95
		end
	end)
	local v_u_101 = v_u_2.Stepped:Connect(function(_, p98)
		-- upvalues: (copy) v_u_48, (copy) v_u_89, (copy) v_u_29
		for v99 in pairs(v_u_48) do
			local v100 = v_u_89[v99]
			if v100 then
				v100(p98, v99, v_u_29.AssemblyLinearVelocity)
			end
		end
	end)
	return function() -- name: terminate
		-- upvalues: (copy) v_u_97, (copy) v_u_101, (ref) v_u_20, (ref) v_u_30, (copy) v_u_32
		v_u_97:Disconnect()
		v_u_101:Disconnect()
		if v_u_20 and v_u_30 then
			v_u_30:Destroy()
		end
		for _, v102 in pairs(v_u_32) do
			v102:Destroy()
		end
		table.clear(v_u_32)
	end
end)
local v_u_104 = {}
local function v_u_106(p105) -- name: characterAdded
	-- upvalues: (copy) v_u_103
	v_u_103:bindRoot(p105)
end
local function v_u_108(p107) -- name: characterRemoving
	-- upvalues: (copy) v_u_103
	v_u_103:unbindRoot(p107)
end
local function v115(p109) -- name: playerAdded
	-- upvalues: (copy) v_u_104, (copy) v_u_103, (copy) v_u_106, (copy) v_u_108
	local v110 = v_u_104[p109]
	if not v110 then
		v110 = {}
		v_u_104[p109] = v110
	end
	if p109.Character then
		v_u_103:bindRoot(p109.Character)
	end
	local v111 = p109.CharacterAdded
	local v112 = v_u_106
	table.insert(v110, v111:Connect(v112))
	local v113 = p109.CharacterRemoving
	local v114 = v_u_108
	table.insert(v110, v113:Connect(v114))
end
local function v119(p116) -- name: playerRemoving
	-- upvalues: (copy) v_u_104, (copy) v_u_103
	local v117 = v_u_104[p116]
	if v117 then
		for _, v118 in ipairs(v117) do
			v118:Disconnect()
		end
		v_u_104[p116] = nil
	end
	if p116.Character then
		v_u_103:unbindRoot(p116.Character)
	end
end
for _, v120 in ipairs(v_u_1:GetPlayers()) do
	task.spawn(v115, v120)
end
v_u_1.PlayerAdded:Connect(v115)
v_u_1.PlayerRemoving:Connect(v119)

==================================================
-- Players.turbobrutti.PlayerScripts.RbxCharacterSounds.AtomicBinding
==================================================
local function v_u_4(p1) -- name: parsePath
	local v2 = string.split(p1, "/")
	for v3 = #v2, 1, -1 do
		if v2[v3] == "" then
			table.remove(v2, v3)
		end
	end
	return v2
end
local function v_u_11(p5, p6) -- name: unbindNodeDescend
	-- upvalues: (copy) v_u_11
	if p5.instance ~= nil then
		p5.instance = nil
		local v7 = p5.connections
		if v7 then
			for _, v8 in ipairs(v7) do
				v8:Disconnect()
			end
			table.clear(v7)
		end
		if p6 and p5.alias then
			p6[p5.alias] = nil
		end
		local v9 = p5.children
		if v9 then
			for _, v10 in pairs(v9) do
				v_u_11(v10, p6)
			end
		end
	end
end
local v_u_12 = {}
v_u_12.__index = v_u_12
function v_u_12.new(p13, p14) -- name: new
	-- upvalues: (copy) v_u_4, (copy) v_u_12
	local v15 = {}
	local v16 = 1
	local v17 = {}
	local v18 = {}
	local v19 = {}
	local v20 = {}
	for v21, v22 in pairs(p13) do
		v15[v21] = v_u_4(v22)
		v16 = v16 + 1
	end
	local v23 = v_u_12
	return setmetatable({
		["_boundFn"] = p14,
		["_parsedManifest"] = v15,
		["_manifestSizeTarget"] = v16,
		["_dtorMap"] = v17,
		["_connections"] = v18,
		["_rootInstToRootNode"] = v19,
		["_rootInstToManifest"] = v20
	}, v23)
end
function v_u_12._startBoundFn(p24, p25, p26) -- name: _startBoundFn
	local v27 = p24._boundFn
	local v28 = p24._dtorMap
	local v29 = v28[p25]
	if v29 then
		v29()
		v28[p25] = nil
	end
	local v30 = v27(p26)
	if v30 then
		v28[p25] = v30
	end
end
function v_u_12._stopBoundFn(p31, p32) -- name: _stopBoundFn
	local v33 = p31._dtorMap
	local v34 = v33[p32]
	if v34 then
		v34()
		v33[p32] = nil
	end
end
function v_u_12.bindRoot(p_u_35, p_u_36) -- name: bindRoot
	-- upvalues: (copy) v_u_11
	debug.profilebegin("AtomicBinding:BindRoot")
	local v37 = p_u_35._parsedManifest
	local v38 = p_u_35._rootInstToRootNode
	local v39 = p_u_35._rootInstToManifest
	local v_u_40 = p_u_35._manifestSizeTarget
	local v41 = v39[p_u_36] == nil
	assert(v41)
	local v_u_42 = {}
	v39[p_u_36] = v_u_42
	debug.profilebegin("BuildTree")
	local v43 = {
		["alias"] = "root",
		["instance"] = p_u_36
	}
	if next(v37) then
		v43.children = {}
		v43.connections = {}
	end
	v38[p_u_36] = v43
	for v44, v45 in pairs(v37) do
		local v46 = v43
		for v47, v48 in ipairs(v45) do
			local v49 = v47 == #v45
			local v50 = v43.children[v48] or {}
			if v49 then
				if v50.alias ~= nil then
					error("Multiple aliases assigned to one instance")
				end
				v50.alias = v44
			else
				v50.children = v50.children or {}
				v50.connections = v50.connections or {}
			end
			v43.children[v48] = v50
			v43 = v50
		end
		v43 = v46
	end
	debug.profileend()
	local function v_u_77(p51) -- name: processNode
		-- upvalues: (copy) v_u_42, (copy) v_u_77, (copy) p_u_35, (copy) p_u_36, (ref) v_u_11, (copy) v_u_40
		local v52 = p51.instance
		local v_u_53 = assert(v52)
		local v_u_54 = p51.children
		local v55 = p51.alias
		local v56 = not v_u_54
		if v55 then
			v_u_42[v55] = v_u_53
		end
		if not v56 then
			local function v59(p57) -- name: processAddChild
				-- upvalues: (copy) v_u_54, (ref) v_u_77
				local v58 = v_u_54[p57.Name]
				if v58 and v58.instance == nil then
					v58.instance = p57
					v_u_77(v58)
				end
			end
			local function v66(p60) -- name: processDeleteChild
				-- upvalues: (copy) v_u_54, (ref) p_u_35, (ref) p_u_36, (ref) v_u_11, (ref) v_u_42, (copy) v_u_53, (ref) v_u_77
				local v61 = p60.Name
				local v62 = v_u_54[v61]
				if v62 then
					if v62.instance == p60 then
						p_u_35:_stopBoundFn(p_u_36)
						v_u_11(v62, v_u_42)
						local v63 = v62.instance == nil
						assert(v63)
						local v64 = v_u_53:FindFirstChild(v61)
						local v65 = v64 and v_u_54[v64.Name]
						if v65 then
							if v65.instance ~= nil then
								return
							end
							v65.instance = v64
							v_u_77(v65)
						end
					end
				else
					return
				end
			end
			for _, v67 in ipairs(v_u_53:GetChildren()) do
				local v68 = v_u_54[v67.Name]
				if v68 then
					if v68.instance == nil then
						v68.instance = v67
						v_u_77(v68)
					end
				end
			end
			local v69 = p51.connections
			local v70 = v_u_53.ChildAdded
			table.insert(v69, v70:Connect(v59))
			local v71 = p51.connections
			local v72 = v_u_53.ChildRemoved
			table.insert(v71, v72:Connect(v66))
		end
		if v56 then
			local v73 = v_u_42
			local v74 = v_u_40
			local v75 = 0
			for _ in pairs(v73) do
				v75 = v75 + 1
			end
			local v76 = v75 <= v74
			assert(v76, v75)
			if v75 == v74 then
				p_u_35:_startBoundFn(p_u_36, v_u_42)
			end
		end
	end
	debug.profilebegin("ResolveTree")
	v_u_77(v43)
	debug.profileend()
	debug.profileend()
end
function v_u_12.unbindRoot(p78, p79) -- name: unbindRoot
	-- upvalues: (copy) v_u_11
	local v80 = p78._rootInstToRootNode
	local v81 = p78._rootInstToManifest
	p78:_stopBoundFn(p79)
	local v82 = v80[p79]
	if v82 then
		local v83 = v81[p79]
		v_u_11(v82, (assert(v83)))
		v80[p79] = nil
	end
	v81[p79] = nil
end
function v_u_12.destroy(p84) -- name: destroy
	-- upvalues: (copy) v_u_11
	debug.profilebegin("AtomicBinding:destroy")
	for _, v85 in pairs(p84._dtorMap) do
		v85:destroy()
	end
	table.clear(p84._dtorMap)
	for _, v86 in ipairs(p84._connections) do
		v86:Disconnect()
	end
	table.clear(p84._connections)
	local v87 = p84._rootInstToManifest
	for v88, v89 in pairs(p84._rootInstToRootNode) do
		local v90 = v87[v88]
		v_u_11(v89, (assert(v90)))
	end
	table.clear(p84._rootInstToManifest)
	table.clear(p84._rootInstToRootNode)
	debug.profileend()
end
return v_u_12

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerScriptsLoader
==================================================
require(script.Parent:WaitForChild("PlayerModule"))

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule
==================================================
local v_u_1 = {}
v_u_1.__index = v_u_1
function v_u_1.new() -- name: new
	-- upvalues: (copy) v_u_1
	local v2 = v_u_1
	local v3 = setmetatable({}, v2)
	v3.cameras = require(script:WaitForChild("CameraModule"))
	v3.controls = require(script:WaitForChild("ControlModule"))
	return v3
end
function v_u_1.GetCameras(p4) -- name: GetCameras
	return p4.cameras
end
function v_u_1.GetControls(p5) -- name: GetControls
	return p5.controls
end
function v_u_1.GetClickToMoveController(p6) -- name: GetClickToMoveController
	return p6.controls:GetClickToMoveController()
end
return v_u_1.new()

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule
==================================================
local v_u_1 = {}
v_u_1.__index = v_u_1
local v_u_2 = {
	"CameraMinZoomDistance",
	"CameraMaxZoomDistance",
	"CameraMode",
	"DevCameraOcclusionMode",
	"DevComputerCameraMode",
	"DevTouchCameraMode",
	"DevComputerMovementMode",
	"DevTouchMovementMode",
	"DevEnableMouseLock"
}
local v_u_3 = {
	"ComputerCameraMovementMode",
	"ComputerMovementMode",
	"ControlMode",
	"GamepadCameraSensitivity",
	"MouseSensitivity",
	"RotationType",
	"TouchCameraMovementMode",
	"TouchMovementMode"
}
local v_u_4 = game:GetService("Players")
local v_u_5 = game:GetService("RunService")
local v_u_6 = game:GetService("UserInputService")
local v_u_7 = game:GetService("VRService")
local v_u_8 = UserSettings():GetService("UserGameSettings")
local v9 = script.Parent:WaitForChild("CommonUtils")
local v_u_10 = require(v9:WaitForChild("ConnectionUtil"))
local v11 = require(v9:WaitForChild("FlagUtil"))
local v_u_12 = require(script:WaitForChild("CameraUtils"))
local v_u_13 = require(script:WaitForChild("CameraInput"))
local v_u_14 = require(script:WaitForChild("ClassicCamera"))
local v_u_15 = require(script:WaitForChild("OrbitalCamera"))
local v_u_16 = require(script:WaitForChild("LegacyCamera"))
local v_u_17 = require(script:WaitForChild("VehicleCamera"))
local v_u_18 = require(script:WaitForChild("VRCamera"))
local v_u_19 = require(script:WaitForChild("VRVehicleCamera"))
local v_u_20 = require(script:WaitForChild("Invisicam"))
local v_u_21 = require(script:WaitForChild("Poppercam"))
local v_u_22 = require(script:WaitForChild("TransparencyController"))
local v_u_23 = require(script:WaitForChild("MouseLockController"))
local v_u_24 = {}
local v_u_25 = {}
if not v_u_4.LocalPlayer then
	return {}
end
local v26 = v_u_4.LocalPlayer
assert(v26, "Strict typing check")
local v27 = v_u_4.LocalPlayer:WaitForChild("PlayerScripts")
v27:RegisterTouchCameraMovementMode(Enum.TouchCameraMovementMode.Default)
v27:RegisterTouchCameraMovementMode(Enum.TouchCameraMovementMode.Follow)
v27:RegisterTouchCameraMovementMode(Enum.TouchCameraMovementMode.Classic)
v27:RegisterComputerCameraMovementMode(Enum.ComputerCameraMovementMode.Default)
v27:RegisterComputerCameraMovementMode(Enum.ComputerCameraMovementMode.Follow)
v27:RegisterComputerCameraMovementMode(Enum.ComputerCameraMovementMode.Classic)
v27:RegisterComputerCameraMovementMode(Enum.ComputerCameraMovementMode.CameraToggle)
local v_u_28 = v11.getUserFlag("UserPlayerConnectionMemoryLeak")
local v_u_29 = v11.getUserFlag("UserPSFixCameraControllerReset")
function v_u_1.new() -- name: new
	-- upvalues: (copy) v_u_22, (copy) v_u_28, (copy) v_u_10, (copy) v_u_1, (copy) v_u_4, (copy) v_u_23, (copy) v_u_5, (copy) v_u_2, (copy) v_u_3, (copy) v_u_8, (copy) v_u_6
	local v30 = {
		["activeTransparencyController"] = v_u_22.new()
	}
	local v31
	if v_u_28 then
		v31 = v_u_10.new()
	else
		v31 = nil
	end
	v30.connectionUtil = v31
	local v32 = v_u_1
	local v_u_33 = setmetatable(v30, v32)
	v_u_33.activeCameraController = nil
	v_u_33.activeOcclusionModule = nil
	v_u_33.activeMouseLockController = nil
	v_u_33.currentComputerCameraMovementMode = nil
	v_u_33.cameraSubjectChangedConn = nil
	v_u_33.cameraTypeChangedConn = nil
	for _, v34 in pairs(v_u_4:GetPlayers()) do
		v_u_33:OnPlayerAdded(v34)
	end
	v_u_4.PlayerAdded:Connect(function(p35)
		-- upvalues: (copy) v_u_33
		v_u_33:OnPlayerAdded(p35)
	end)
	if v_u_28 then
		v_u_4.PlayerRemoving:Connect(function(p36)
			-- upvalues: (copy) v_u_33
			v_u_33:OnPlayerRemoving(p36)
		end)
	end
	v_u_33.activeTransparencyController:Enable(true)
	v_u_33.activeMouseLockController = v_u_23.new()
	local v37 = v_u_33.activeMouseLockController
	assert(v37, "Strict typing check")
	local v38 = v_u_33.activeMouseLockController:GetBindableToggleEvent()
	if v38 then
		v38:Connect(function()
			-- upvalues: (copy) v_u_33
			v_u_33:OnMouseLockToggled()
		end)
	end
	v_u_33:ActivateCameraController()
	v_u_33:ActivateOcclusionModule(v_u_4.LocalPlayer.DevCameraOcclusionMode)
	v_u_33:OnCurrentCameraChanged()
	v_u_5:BindToRenderStep("cameraRenderUpdate", Enum.RenderPriority.Camera.Value, function(p39)
		-- upvalues: (copy) v_u_33
		v_u_33:Update(p39)
	end)
	for _, v_u_40 in pairs(v_u_2) do
		v_u_4.LocalPlayer:GetPropertyChangedSignal(v_u_40):Connect(function()
			-- upvalues: (copy) v_u_33, (copy) v_u_40
			v_u_33:OnLocalPlayerCameraPropertyChanged(v_u_40)
		end)
	end
	for _, v_u_41 in pairs(v_u_3) do
		v_u_8:GetPropertyChangedSignal(v_u_41):Connect(function()
			-- upvalues: (copy) v_u_33, (copy) v_u_41
			v_u_33:OnUserGameSettingsPropertyChanged(v_u_41)
		end)
	end
	game.Workspace:GetPropertyChangedSignal("CurrentCamera"):Connect(function()
		-- upvalues: (copy) v_u_33
		v_u_33:OnCurrentCameraChanged()
	end)
	v_u_6:GetPropertyChangedSignal("PreferredInput"):Connect(function()
		-- upvalues: (copy) v_u_33
		v_u_33:OnPreferredInputChanged()
	end)
	return v_u_33
end
function v_u_1.GetCameraMovementModeFromSettings(_) -- name: GetCameraMovementModeFromSettings
	-- upvalues: (copy) v_u_4, (copy) v_u_12, (copy) v_u_6, (copy) v_u_8
	if v_u_4.LocalPlayer.CameraMode == Enum.CameraMode.LockFirstPerson then
		return v_u_12.ConvertCameraModeEnumToStandard(Enum.ComputerCameraMovementMode.Classic)
	else
		local v42, v43
		if v_u_6.PreferredInput == Enum.PreferredInput.Touch then
			v42 = v_u_12.ConvertCameraModeEnumToStandard(v_u_4.LocalPlayer.DevTouchCameraMode)
			v43 = v_u_12.ConvertCameraModeEnumToStandard(v_u_8.TouchCameraMovementMode)
		else
			v42 = v_u_12.ConvertCameraModeEnumToStandard(v_u_4.LocalPlayer.DevComputerCameraMode)
			v43 = v_u_12.ConvertCameraModeEnumToStandard(v_u_8.ComputerCameraMovementMode)
		end
		if v42 == Enum.DevComputerCameraMovementMode.UserChoice then
			return v43
		else
			return v42
		end
	end
end
function v_u_1.ActivateOcclusionModule(p44, p45) -- name: ActivateOcclusionModule
	-- upvalues: (copy) v_u_21, (copy) v_u_20, (copy) v_u_25, (copy) v_u_4
	local v46
	if p45 == Enum.DevCameraOcclusionMode.Zoom then
		v46 = v_u_21
	else
		if p45 ~= Enum.DevCameraOcclusionMode.Invisicam then
			warn("CameraScript ActivateOcclusionModule called with unsupported mode")
			return
		end
		v46 = v_u_20
	end
	p44.occlusionMode = p45
	if p44.activeOcclusionModule and p44.activeOcclusionModule:GetOcclusionMode() == p45 then
		if not p44.activeOcclusionModule:GetEnabled() then
			p44.activeOcclusionModule:Enable(true)
		end
	else
		local v47 = p44.activeOcclusionModule
		p44.activeOcclusionModule = v_u_25[v46]
		if not p44.activeOcclusionModule then
			p44.activeOcclusionModule = v46.new()
			if p44.activeOcclusionModule then
				v_u_25[v46] = p44.activeOcclusionModule
			end
		end
		if p44.activeOcclusionModule then
			if p44.activeOcclusionModule:GetOcclusionMode() ~= p45 then
				warn("CameraScript ActivateOcclusionModule mismatch: ", p44.activeOcclusionModule:GetOcclusionMode(), "~=", p45)
			end
			if v47 then
				if v47 == p44.activeOcclusionModule then
					warn("CameraScript ActivateOcclusionModule failure to detect already running correct module")
				else
					v47:Enable(false)
				end
			end
			if p45 == Enum.DevCameraOcclusionMode.Invisicam then
				if v_u_4.LocalPlayer.Character then
					p44.activeOcclusionModule:CharacterAdded(v_u_4.LocalPlayer.Character, v_u_4.LocalPlayer)
				end
			else
				for _, v48 in pairs(v_u_4:GetPlayers()) do
					if v48 and v48.Character then
						p44.activeOcclusionModule:CharacterAdded(v48.Character, v48)
					end
				end
				p44.activeOcclusionModule:OnCameraSubjectChanged(game.Workspace.CurrentCamera.CameraSubject)
			end
			p44.activeOcclusionModule:Enable(true)
		end
	end
end
function v_u_1.ShouldUseVehicleCamera(p49) -- name: ShouldUseVehicleCamera
	local v50 = workspace.CurrentCamera
	if not v50 then
		return false
	end
	local v51 = v50.CameraType
	local v52 = v50.CameraSubject
	local v53 = v51 == Enum.CameraType.Custom and true or v51 == Enum.CameraType.Follow
	local v54 = v52 and v52:IsA("VehicleSeat") or false
	local v55 = p49.occlusionMode ~= Enum.DevCameraOcclusionMode.Invisicam
	if v54 then
		if not v53 then
			v55 = v53
		end
	else
		v55 = v54
	end
	return v55
end
function v_u_1.ActivateCameraController(p56) -- name: ActivateCameraController
	-- upvalues: (copy) v_u_16, (copy) v_u_7, (copy) v_u_18, (copy) v_u_14, (copy) v_u_15, (copy) v_u_19, (copy) v_u_17, (copy) v_u_24, (copy) v_u_29
	local v57 = workspace.CurrentCamera.CameraType
	local v58 = p56:GetCameraMovementModeFromSettings()
	local v59 = nil
	if v57 == Enum.CameraType.Scriptable then
		if p56.activeCameraController then
			p56.activeCameraController:Enable(false)
			p56.activeCameraController = nil
		end
	else
		if v57 == Enum.CameraType.Custom then
			v58 = p56:GetCameraMovementModeFromSettings()
		elseif v57 == Enum.CameraType.Track then
			v58 = Enum.ComputerCameraMovementMode.Classic
		elseif v57 == Enum.CameraType.Follow then
			v58 = Enum.ComputerCameraMovementMode.Follow
		elseif v57 == Enum.CameraType.Orbital then
			v58 = Enum.ComputerCameraMovementMode.Orbital
		elseif v57 == Enum.CameraType.Attach or (v57 == Enum.CameraType.Watch or v57 == Enum.CameraType.Fixed) then
			v59 = v_u_16
		else
			warn("CameraScript encountered an unhandled Camera.CameraType value: ", v57)
		end
		if not v59 then
			if v_u_7.VREnabled then
				v59 = v_u_18
			elseif v58 == Enum.ComputerCameraMovementMode.Classic or (v58 == Enum.ComputerCameraMovementMode.Follow or (v58 == Enum.ComputerCameraMovementMode.Default or v58 == Enum.ComputerCameraMovementMode.CameraToggle)) then
				v59 = v_u_14
			else
				if v58 ~= Enum.ComputerCameraMovementMode.Orbital then
					warn("ActivateCameraController did not select a module.")
					return
				end
				v59 = v_u_15
			end
		end
		if p56:ShouldUseVehicleCamera() then
			if v_u_7.VREnabled then
				v59 = v_u_19
			else
				v59 = v_u_17
			end
		end
		local v60
		if v_u_24[v59] then
			v60 = v_u_24[v59]
			if v_u_29 then
				if v60.Reset and p56.activeCameraController ~= v60 then
					v60:Reset()
				end
			elseif v60.Reset then
				v60:Reset()
			end
		else
			v60 = v59.new()
			v_u_24[v59] = v60
		end
		if p56.activeCameraController then
			if p56.activeCameraController == v60 then
				if not p56.activeCameraController:GetEnabled() then
					p56.activeCameraController:Enable(true)
				end
			else
				if v60.HandleSubjectDistance then
					v60:HandleSubjectDistance(p56.activeCameraController)
				end
				p56.activeCameraController:Enable(false)
				p56.activeCameraController = v60
				p56.activeCameraController:Enable(true)
			end
		elseif v60 ~= nil then
			p56.activeCameraController = v60
			local v61 = p56.activeCameraController
			assert(v61, "Strict typing check")
			p56.activeCameraController:Enable(true)
		end
		if p56.activeCameraController then
			p56.activeCameraController:SetCameraMovementMode(v58)
			p56.activeCameraController:SetCameraType(v57)
		end
	end
end
function v_u_1.OnCameraSubjectChanged(p62) -- name: OnCameraSubjectChanged
	local v63 = workspace.CurrentCamera
	local v64
	if v63 then
		v64 = v63.CameraSubject
	else
		v64 = nil
	end
	if p62.activeTransparencyController then
		p62.activeTransparencyController:SetSubject(v64)
	end
	if p62.activeOcclusionModule then
		p62.activeOcclusionModule:OnCameraSubjectChanged(v64)
	end
	p62:ActivateCameraController()
end
function v_u_1.OnCameraTypeChanged(p65, p66) -- name: OnCameraTypeChanged
	-- upvalues: (copy) v_u_6, (copy) v_u_12
	if p66 == Enum.CameraType.Scriptable and v_u_6.MouseBehavior == Enum.MouseBehavior.LockCenter then
		v_u_12.restoreMouseBehavior()
	end
	p65:ActivateCameraController()
end
function v_u_1.OnCurrentCameraChanged(p_u_67) -- name: OnCurrentCameraChanged
	local v_u_68 = game.Workspace.CurrentCamera
	if v_u_68 then
		if p_u_67.cameraSubjectChangedConn then
			p_u_67.cameraSubjectChangedConn:Disconnect()
		end
		if p_u_67.cameraTypeChangedConn then
			p_u_67.cameraTypeChangedConn:Disconnect()
		end
		p_u_67.cameraSubjectChangedConn = v_u_68:GetPropertyChangedSignal("CameraSubject"):Connect(function()
			-- upvalues: (copy) p_u_67
			p_u_67:OnCameraSubjectChanged()
		end)
		p_u_67.cameraTypeChangedConn = v_u_68:GetPropertyChangedSignal("CameraType"):Connect(function()
			-- upvalues: (copy) p_u_67, (copy) v_u_68
			p_u_67:OnCameraTypeChanged(v_u_68.CameraType)
		end)
		p_u_67:OnCameraSubjectChanged()
		p_u_67:OnCameraTypeChanged(v_u_68.CameraType)
	end
end
function v_u_1.OnLocalPlayerCameraPropertyChanged(p69, p70) -- name: OnLocalPlayerCameraPropertyChanged
	-- upvalues: (copy) v_u_4
	if p70 == "CameraMode" then
		if v_u_4.LocalPlayer.CameraMode ~= Enum.CameraMode.LockFirstPerson then
			if v_u_4.LocalPlayer.CameraMode == Enum.CameraMode.Classic then
				p69:ActivateCameraController()
			else
				warn("Unhandled value for property player.CameraMode: ", v_u_4.LocalPlayer.CameraMode)
			end
		end
		if not p69.activeCameraController or p69.activeCameraController:GetModuleName() ~= "ClassicCamera" then
			p69:ActivateCameraController()
		end
		if p69.activeCameraController then
			p69.activeCameraController:UpdateForDistancePropertyChange()
			return
		end
	else
		if p70 == "DevComputerCameraMode" or p70 == "DevTouchCameraMode" then
			p69:ActivateCameraController()
			return
		end
		if p70 == "DevCameraOcclusionMode" then
			p69:ActivateOcclusionModule(v_u_4.LocalPlayer.DevCameraOcclusionMode)
			return
		end
		if p70 == "CameraMinZoomDistance" or p70 == "CameraMaxZoomDistance" then
			if p69.activeCameraController then
				p69.activeCameraController:UpdateForDistancePropertyChange()
				return
			end
		else
			if p70 == "DevTouchMovementMode" then
				return
			end
			if p70 == "DevComputerMovementMode" then
				return
			end
			local _ = p70 == "DevEnableMouseLock"
		end
	end
end
function v_u_1.OnUserGameSettingsPropertyChanged(p71, p72) -- name: OnUserGameSettingsPropertyChanged
	if p72 == "ComputerCameraMovementMode" or p72 == "TouchCameraMovementMode" then
		p71:ActivateCameraController()
	end
end
function v_u_1.OnPreferredInputChanged(p73) -- name: OnPreferredInputChanged
	p73:ActivateCameraController()
end
function v_u_1.Update(p74, p75) -- name: Update
	-- upvalues: (copy) v_u_13
	if p74.activeCameraController then
		p74.activeCameraController:UpdateMouseBehavior()
		local v76, v77 = p74.activeCameraController:Update(p75)
		if p74.activeOcclusionModule and not p74.activeCameraController.skipOcclusion then
			v76, v77 = p74.activeOcclusionModule:Update(p75, v76, v77)
		end
		local v78 = game.Workspace.CurrentCamera
		v78.CFrame = v76
		v78.Focus = v77
		if p74.activeTransparencyController then
			p74.activeTransparencyController:Update(p75)
		end
		if v_u_13.getInputEnabled() then
			v_u_13.resetInputForFrameEnd()
		end
	end
end
function v_u_1.OnCharacterAdded(p79, p80, p81) -- name: OnCharacterAdded
	if p79.activeOcclusionModule then
		p79.activeOcclusionModule:CharacterAdded(p80, p81)
	end
end
function v_u_1.OnCharacterRemoving(p82, p83, p84) -- name: OnCharacterRemoving
	if p82.activeOcclusionModule then
		p82.activeOcclusionModule:CharacterRemoving(p83, p84)
	end
end
function v_u_1.OnPlayerAdded(p_u_85, p_u_86) -- name: OnPlayerAdded
	-- upvalues: (copy) v_u_28
	if v_u_28 then
		if p_u_85.connectionUtil then
			p_u_85.connectionUtil:trackConnection(("%*CharacterAdded"):format(p_u_86.UserId), p_u_86.CharacterAdded:Connect(function(p87)
				-- upvalues: (copy) p_u_85, (copy) p_u_86
				p_u_85:OnCharacterAdded(p87, p_u_86)
			end))
			p_u_85.connectionUtil:trackConnection(("%*CharacterRemoving"):format(p_u_86.UserId), p_u_86.CharacterRemoving:Connect(function(p88)
				-- upvalues: (copy) p_u_85, (copy) p_u_86
				p_u_85:OnCharacterRemoving(p88, p_u_86)
			end))
			return
		end
	else
		p_u_86.CharacterAdded:Connect(function(p89)
			-- upvalues: (copy) p_u_85, (copy) p_u_86
			p_u_85:OnCharacterAdded(p89, p_u_86)
		end)
		p_u_86.CharacterRemoving:Connect(function(p90)
			-- upvalues: (copy) p_u_85, (copy) p_u_86
			p_u_85:OnCharacterRemoving(p90, p_u_86)
		end)
	end
end
function v_u_1.OnPlayerRemoving(p91, p92) -- name: OnPlayerRemoving
	if p91.connectionUtil then
		p91.connectionUtil:disconnect((("%*CharacterAdded"):format(p92.UserId)))
		p91.connectionUtil:disconnect((("%*CharacterRemoving"):format(p92.UserId)))
	end
end
function v_u_1.OnMouseLockToggled(p93) -- name: OnMouseLockToggled
	if p93.activeMouseLockController then
		local v94 = p93.activeMouseLockController:GetIsMouseLocked()
		local v95 = p93.activeMouseLockController:GetMouseLockOffset()
		if p93.activeCameraController then
			p93.activeCameraController:SetIsMouseLocked(v94)
			p93.activeCameraController:SetMouseLockOffset(v95)
		end
	end
end
v_u_1.new()
return {}

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.VRCameraTeleportDetector.spec
==================================================
local v1 = game:GetService("CorePackages")
local v2 = require(v1.Packages.Dev.JestGlobals)
local v3 = v2.describe
local v_u_4 = v2.expect
local v_u_5 = v2.it
local v6 = require(script.Parent.VRCameraTeleportDetector)
local v_u_7 = v6.shouldRecenter
local v_u_8 = v6.JUMP_STUDS
local v_u_9 = v6.SETTLED_STUDS
local v_u_10 = v6.DEBOUNCE_SECONDS
v3("VRCameraTeleportDetector.shouldRecenter", function()
	-- upvalues: (copy) v_u_5, (copy) v_u_4, (copy) v_u_7, (copy) v_u_8, (copy) v_u_9, (copy) v_u_10
	v_u_5("fires on a discrete jump from rest (no prior step, never recentered)", function()
		-- upvalues: (ref) v_u_4, (ref) v_u_7, (ref) v_u_8
		v_u_4(v_u_7(nil, v_u_8 + 10, nil, 100)).toBe(true)
	end)
	v_u_5("fires on a discrete jump preceded by a near-still frame", function()
		-- upvalues: (ref) v_u_4, (ref) v_u_7, (ref) v_u_9, (ref) v_u_8
		v_u_4(v_u_7(v_u_9 - 0.5, v_u_8 + 10, nil, 100)).toBe(true)
	end)
	v_u_5("does not fire for sub-threshold motion", function()
		-- upvalues: (ref) v_u_4, (ref) v_u_7, (ref) v_u_8
		v_u_4(v_u_7(0, v_u_8 - 0.1, nil, 100)).toBe(false)
		v_u_4(v_u_7(0, 0, nil, 100)).toBe(false)
	end)
	v_u_5("does not fire when the previous frame was already moving (continuous motion)", function()
		-- upvalues: (ref) v_u_4, (ref) v_u_7, (ref) v_u_9, (ref) v_u_8
		v_u_4(v_u_7(v_u_9 + 0.1, v_u_8 + 10, nil, 100)).toBe(false)
	end)
	v_u_5("does not fire within the debounce interval", function()
		-- upvalues: (ref) v_u_4, (ref) v_u_7, (ref) v_u_8, (ref) v_u_10
		v_u_4(v_u_7(nil, v_u_8 + 10, 100, 100 + v_u_10 - 0.01)).toBe(false)
	end)
	v_u_5("fires again once the debounce interval has elapsed", function()
		-- upvalues: (ref) v_u_4, (ref) v_u_7, (ref) v_u_8, (ref) v_u_10
		v_u_4(v_u_7(nil, v_u_8 + 10, 100, 100 + v_u_10 + 0.01)).toBe(true)
	end)
	v_u_5("does not retrigger every frame under continuous per-frame CFrame writes (oscillation guard)", function()
		-- upvalues: (ref) v_u_8, (ref) v_u_7, (ref) v_u_4
		local v11 = v_u_8 + 10
		local v12 = nil
		local v13 = nil
		local v14 = 0
		local v15 = 0
		for _ = 1, 120 do
			if v_u_7(v12, v11, v13, v14) then
				v15 = v15 + 1
				v13 = v14
			end
			v14 = v14 + 0.016666666666666666
			v12 = v11
		end
		v_u_4(v15).toBe(1)
	end)
end)

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.VehicleCamera
==================================================
local v_u_1 = { 0, 15, 30 }
local v2 = game:GetService("Players")
local v3 = game:GetService("RunService")
local v_u_4 = require(script.Parent:WaitForChild("BaseCamera"))
local v_u_5 = require(script.Parent:WaitForChild("CameraInput"))
local v_u_6 = require(script.Parent:WaitForChild("CameraUtils"))
require(script.Parent:WaitForChild("ZoomController"))
local v_u_7 = require(script:WaitForChild("VehicleCameraCore"))
local v_u_8 = require(script:WaitForChild("VehicleCameraConfig"))
local v_u_9 = v2.LocalPlayer
local _ = v_u_6.map
local v_u_10 = v_u_6.Spring
local v_u_11 = v_u_6.mapClamp
local v_u_12 = v_u_6.sanitizeAngle
local v_u_13 = 0.016666666666666666
v3.Stepped:Connect(function(_, p14)
	-- upvalues: (ref) v_u_13
	v_u_13 = p14
end)
local v_u_15 = setmetatable({}, v_u_4)
v_u_15.__index = v_u_15
function v_u_15.new() -- name: new
	-- upvalues: (copy) v_u_4, (copy) v_u_15
	local v16 = v_u_4.new()
	local v17 = v_u_15
	local v18 = setmetatable(v16, v17)
	v18:Reset()
	return v18
end
function v_u_15.Reset(p19) -- name: Reset
	-- upvalues: (copy) v_u_7, (copy) v_u_10, (copy) v_u_8, (copy) v_u_6, (copy) v_u_1
	p19.vehicleCameraCore = v_u_7.new(p19:GetSubjectCFrame())
	local v20 = v_u_10.new
	local v21 = v_u_8.pitchBaseAngle
	p19.pitchSpring = v20(0, -math.rad(v21))
	p19.yawSpring = v_u_10.new(0, 0)
	p19.lastPanTick = 0
	local v22 = workspace.CurrentCamera
	local v23
	if v22 then
		v23 = v22.CameraSubject
	else
		v23 = v22
	end
	assert(v22)
	assert(v23)
	assert(v23:IsA("VehicleSeat"))
	local v24 = v23:GetConnectedParts(true)
	local v25, v26 = v_u_6.getLooseBoundingSphere(v24)
	p19.assemblyRadius = math.max(v26, 5)
	p19.assemblyOffset = v23.CFrame:Inverse() * v25
	p19.gamepadZoomLevels = {}
	for _, v27 in v_u_1 do
		local v28 = p19.gamepadZoomLevels
		local v29 = v27 * p19.assemblyRadius / 10
		table.insert(v28, v29)
	end
	p19:SetCameraToSubjectDistance(p19.gamepadZoomLevels[#p19.gamepadZoomLevels])
end
function v_u_15._StepRotation(p30, p31, p32) -- name: _StepRotation
	-- upvalues: (copy) v_u_5, (copy) v_u_12, (copy) v_u_8, (copy) v_u_11
	local v33 = p30.yawSpring
	local v34 = p30.pitchSpring
	local v35 = v_u_5.getRotation(p31, true)
	local v36 = -v35.X
	local v37 = -v35.Y
	v33.pos = v_u_12(v33.pos + v36)
	local v38 = v_u_12
	local v39 = v34.pos + v37
	v34.pos = v38((math.clamp(v39, -1.3962634015954636, 1.3962634015954636)))
	if v_u_5.getRotationActivated() then
		p30.lastPanTick = os.clock()
	end
	local v40 = v_u_8.pitchBaseAngle
	local v41 = -math.rad(v40)
	local v42 = v_u_8.pitchDeadzoneAngle
	local v43 = math.rad(v42)
	if os.clock() - p30.lastPanTick > v_u_8.autocorrectDelay then
		local v44 = v_u_11(p32, v_u_8.autocorrectMinCarSpeed, v_u_8.autocorrectMaxCarSpeed, 0, v_u_8.autocorrectResponse)
		v33.freq = v44
		v34.freq = v44
		if v33.freq < 0.001 then
			v33.vel = 0
		end
		if v34.freq < 0.001 then
			v34.vel = 0
		end
		local v45 = v_u_12(v41 - v34.pos)
		if math.abs(v45) <= v43 then
			v34.goal = v34.pos
		else
			v34.goal = v41
		end
	else
		v33.freq = 0
		v33.vel = 0
		v34.freq = 0
		v34.vel = 0
		v34.goal = v41
	end
	return CFrame.fromEulerAnglesYXZ(v34:step(p31), v33:step(p31), 0)
end
function v_u_15._GetThirdPersonLocalOffset(p46) -- name: _GetThirdPersonLocalOffset
	-- upvalues: (copy) v_u_8
	local v47 = p46.assemblyOffset
	local v48 = p46.assemblyRadius * v_u_8.verticalCenterOffset
	return v47 + Vector3.new(0, v48, 0)
end
function v_u_15._GetFirstPersonLocalOffset(p49, p50) -- name: _GetFirstPersonLocalOffset
	-- upvalues: (copy) v_u_9
	local v51 = v_u_9.Character
	if v51 and v51.Parent then
		local v52 = v51:FindFirstChild("Head")
		if v52 and v52:IsA("BasePart") then
			return p50:Inverse() * v52.Position
		end
	end
	return p49:_GetThirdPersonLocalOffset()
end
function v_u_15.Update(p53) -- name: Update
	-- upvalues: (ref) v_u_13, (copy) v_u_11
	local v54 = workspace.CurrentCamera
	local v55
	if v54 then
		v55 = v54.CameraSubject
	else
		v55 = v54
	end
	local v56 = p53.vehicleCameraCore
	assert(v54)
	assert(v55)
	assert(v55:IsA("VehicleSeat"))
	local v57 = v_u_13
	v_u_13 = 0
	local v58 = p53:GetSubjectCFrame()
	local v59 = p53:GetSubjectVelocity()
	local v60 = p53:GetSubjectRotVelocity()
	local v61 = v59:Dot(v58.ZVector)
	local v62 = math.abs(v61)
	local v63 = v58.YVector:Dot(v60)
	local v64 = math.abs(v63)
	local v65 = v58.XVector:Dot(v60)
	local v66 = math.abs(v65)
	local v67 = p53:StepZoom()
	local v68 = p53:_StepRotation(v57, v62)
	local v69 = v_u_11(v67, 0.5, p53.assemblyRadius, 1, 0)
	local v70 = p53:_GetThirdPersonLocalOffset():Lerp(p53:_GetFirstPersonLocalOffset(v58), v69)
	v56:setTransform(v58)
	local v71 = v56:step(v57, v66, v64, v69)
	local v72 = CFrame.new(v58 * v70) * v71 * v68
	return v72 * CFrame.new(0, 0, v67), v72
end
function v_u_15.ApplyVRTransform(_) -- name: ApplyVRTransform end
return v_u_15

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.VehicleCamera.VehicleCameraConfig
==================================================
return {
	["pitchStiffness"] = 0.5,
	["yawStiffness"] = 2.5,
	["autocorrectDelay"] = 1,
	["autocorrectMinCarSpeed"] = 16,
	["autocorrectMaxCarSpeed"] = 32,
	["autocorrectResponse"] = 0.5,
	["cutoffMinAngularVelYaw"] = 60,
	["cutoffMaxAngularVelYaw"] = 180,
	["cutoffMinAngularVelPitch"] = 15,
	["cutoffMaxAngularVelPitch"] = 60,
	["pitchBaseAngle"] = 18,
	["pitchDeadzoneAngle"] = 12,
	["firstPersonResponseMul"] = 10,
	["yawReponseDampingRising"] = 1,
	["yawResponseDampingFalling"] = 3,
	["pitchReponseDampingRising"] = 1,
	["pitchResponseDampingFalling"] = 3,
	["verticalCenterOffset"] = 0.33
}

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.VehicleCamera.VehicleCameraCore
==================================================
local v1 = require(script.Parent.Parent.CameraUtils)
local v_u_2 = require(script.Parent.VehicleCameraConfig)
local v_u_3 = v1.map
local v_u_4 = v1.mapClamp
local v_u_5 = v1.sanitizeAngle
local v_u_6 = {}
v_u_6.__index = v_u_6
function v_u_6.new(p7, p8, p9) -- name: new
	-- upvalues: (copy) v_u_6
	local v10 = {
		["fRising"] = p7,
		["fFalling"] = p8,
		["g"] = p9,
		["p"] = p9,
		["v"] = p9 * 0
	}
	local v11 = v_u_6
	return setmetatable(v10, v11)
end
function v_u_6.step(p12, p13) -- name: step
	local v14 = p12.fRising
	local v15 = p12.fFalling
	local v16 = p12.g
	local v17 = p12.p
	local v18 = p12.v
	local v19 = 6.283185307179586
	if v18 > 0 then
		v15 = v14 or v15
	end
	local v20 = v19 * v15
	local v21 = v17 - v16
	local v22 = -v20 * p13
	local v23 = math.exp(v22)
	local v24 = (v21 * (1 + v20 * p13) + v18 * p13) * v23 + v16
	local v25 = (v18 * (1 - v20 * p13) - v21 * (v20 * v20 * p13)) * v23
	p12.p = v24
	p12.v = v25
	return v24
end
local v_u_26 = {}
v_u_26.__index = v_u_26
function v_u_26.new(p27) -- name: new
	-- upvalues: (copy) v_u_5, (copy) v_u_6, (copy) v_u_2, (copy) v_u_26
	local v28 = typeof(p27) == "CFrame"
	assert(v28)
	local v29 = {
		["yawG"] = nil,
		["yawP"] = nil,
		["yawV"] = 0,
		["pitchG"] = nil,
		["pitchP"] = nil,
		["pitchV"] = 0,
		["fSpringYaw"] = nil,
		["fSpringPitch"] = nil
	}
	local _, v30 = p27:toEulerAnglesYXZ()
	v29.yawG = v_u_5(v30)
	local _, v31 = p27:toEulerAnglesYXZ()
	v29.yawP = v_u_5(v31)
	v29.pitchG = v_u_5((p27:toEulerAnglesYXZ()))
	v29.pitchP = v_u_5((p27:toEulerAnglesYXZ()))
	v29.fSpringYaw = v_u_6.new(v_u_2.yawReponseDampingRising, v_u_2.yawResponseDampingFalling, 0)
	v29.fSpringPitch = v_u_6.new(v_u_2.pitchReponseDampingRising, v_u_2.pitchResponseDampingFalling, 0)
	local v32 = v_u_26
	return setmetatable(v29, v32)
end
function v_u_26.setGoal(p33, p34) -- name: setGoal
	-- upvalues: (copy) v_u_5
	local v35 = typeof(p34) == "CFrame"
	assert(v35)
	local _, v36 = p34:toEulerAnglesYXZ()
	p33.yawG = v_u_5(v36)
	p33.pitchG = v_u_5((p34:toEulerAnglesYXZ()))
end
function v_u_26.getCFrame(p37) -- name: getCFrame
	return CFrame.fromEulerAnglesYXZ(p37.pitchP, p37.yawP, 0)
end
function v_u_26.step(p38, p39, p40, p41, p42) -- name: step
	-- upvalues: (copy) v_u_4, (copy) v_u_3, (copy) v_u_2, (copy) v_u_5
	local v43 = typeof(p39) == "number"
	assert(v43)
	local v44 = typeof(p41) == "number"
	assert(v44)
	local v45 = typeof(p40) == "number"
	assert(v45)
	local v46 = typeof(p42) == "number"
	assert(v46)
	local v47 = p38.fSpringYaw
	local v48 = p38.fSpringPitch
	local v49 = v_u_4
	local v50 = v_u_3(p42, 0, 1, p41, 0)
	local v51 = v_u_2.cutoffMinAngularVelYaw
	local v52 = math.rad(v51)
	local v53 = v_u_2.cutoffMaxAngularVelYaw
	v47.g = v49(v50, v52, math.rad(v53), 1, 0)
	local v54 = v_u_4
	local v55 = v_u_3(p42, 0, 1, p40, 0)
	local v56 = v_u_2.cutoffMinAngularVelPitch
	local v57 = math.rad(v56)
	local v58 = v_u_2.cutoffMaxAngularVelPitch
	v48.g = v54(v55, v57, math.rad(v58), 1, 0)
	local v59 = 6.283185307179586 * v_u_2.yawStiffness * v47:step(p39)
	local v60 = 6.283185307179586 * v_u_2.pitchStiffness * v48:step(p39) * v_u_3(p42, 0, 1, 1, v_u_2.firstPersonResponseMul)
	local v61 = v59 * v_u_3(p42, 0, 1, 1, v_u_2.firstPersonResponseMul)
	local v62 = p38.yawG
	local v63 = p38.yawP
	local v64 = p38.yawV
	local v65 = v_u_5(v63 - v62)
	local v66 = -v61 * p39
	local v67 = math.exp(v66)
	local v68 = v_u_5((v65 * (1 + v61 * p39) + v64 * p39) * v67 + v62)
	local v69 = (v64 * (1 - v61 * p39) - v65 * (v61 * v61 * p39)) * v67
	p38.yawP = v68
	p38.yawV = v69
	local v70 = p38.pitchG
	local v71 = p38.pitchP
	local v72 = p38.pitchV
	local v73 = v_u_5(v71 - v70)
	local v74 = -v60 * p39
	local v75 = math.exp(v74)
	local v76 = v_u_5((v73 * (1 + v60 * p39) + v72 * p39) * v75 + v70)
	local v77 = (v72 * (1 - v60 * p39) - v73 * (v60 * v60 * p39)) * v75
	p38.pitchP = v76
	p38.pitchV = v77
	return p38:getCFrame()
end
local v_u_78 = {}
v_u_78.__index = v_u_78
function v_u_78.new(p79) -- name: new
	-- upvalues: (copy) v_u_26, (copy) v_u_78
	local v80 = {
		["vrs"] = v_u_26.new(p79)
	}
	local v81 = v_u_78
	return setmetatable(v80, v81)
end
function v_u_78.step(p82, p83, p84, p85, p86) -- name: step
	return p82.vrs:step(p83, p84, p85, p86)
end
function v_u_78.setTransform(p87, p88) -- name: setTransform
	p87.vrs:setGoal(p88)
end
return v_u_78

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.VRBaseCamera
==================================================
local v1, v2 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserVRVehicleCameraOrbital")
end)
local v_u_3 = v1 and v2
local v_u_4 = game:GetService("VRService")
local v_u_5 = game:GetService("Players").LocalPlayer
local v_u_6 = game:GetService("Lighting")
local v_u_7 = game:GetService("RunService")
local v_u_8 = UserSettings():GetService("UserGameSettings")
local v_u_9 = require(script.Parent:WaitForChild("CameraInput"))
local v_u_10 = require(script.Parent:WaitForChild("ZoomController"))
local v11 = script.Parent.Parent:WaitForChild("CommonUtils")
local v_u_12 = require(v11:WaitForChild("FlagUtil")).getUserFlag("UserVRRemoveLuaEdgeBlur")
local v_u_13 = require(script.Parent:WaitForChild("BaseCamera"))
local v_u_14 = setmetatable({}, v_u_13)
v_u_14.__index = v_u_14
function v_u_14.new() -- name: new
	-- upvalues: (copy) v_u_13, (copy) v_u_14
	local v15 = v_u_13.new()
	local v16 = v_u_14
	local v17 = setmetatable(v15, v16)
	v17.gamepadZoomLevels = { 0, 7 }
	v17.headScale = 1
	v17:SetCameraToSubjectDistance(7)
	v17.VRFadeResetTimer = 0
	v17.VREdgeBlurTimer = 0
	v17.gamepadResetConnection = nil
	v17.needsReset = true
	v17.recentered = false
	v17:Reset()
	return v17
end
function v_u_14.Reset(p18) -- name: Reset
	p18.stepRotateTimeout = 0
end
function v_u_14.GetModuleName(_) -- name: GetModuleName
	return "VRBaseCamera"
end
function v_u_14.GamepadZoomPress(p19) -- name: GamepadZoomPress
	-- upvalues: (copy) v_u_13
	v_u_13.GamepadZoomPress(p19)
	p19:GamepadReset()
	p19:ResetZoom()
end
function v_u_14.GamepadReset(p20) -- name: GamepadReset
	p20.stepRotateTimeout = 0
	p20.needsReset = true
end
function v_u_14.ResetZoom(p21) -- name: ResetZoom
	-- upvalues: (copy) v_u_10
	v_u_10.SetZoomParameters(p21.currentSubjectDistance, 0)
	v_u_10.ReleaseSpring()
end
function v_u_14.OnEnabledChanged(p_u_22) -- name: OnEnabledChanged
	-- upvalues: (copy) v_u_13, (copy) v_u_9, (copy) v_u_4, (ref) v_u_3, (copy) v_u_12, (copy) v_u_5, (copy) v_u_6
	v_u_13.OnEnabledChanged(p_u_22)
	if p_u_22.enabled then
		p_u_22.gamepadResetConnection = v_u_9.gamepadReset:Connect(function()
			-- upvalues: (copy) p_u_22
			p_u_22:GamepadReset()
		end)
		p_u_22.thirdPersonOptionChanged = v_u_4:GetPropertyChangedSignal("ThirdPersonFollowCamEnabled"):Connect(function()
			-- upvalues: (ref) v_u_3, (copy) p_u_22
			if v_u_3 then
				p_u_22:Reset()
			elseif not p_u_22:IsInFirstPerson() then
				p_u_22:Reset()
			end
		end)
		p_u_22.vrRecentered = v_u_4.UserCFrameChanged:Connect(function(p23, _)
			-- upvalues: (copy) p_u_22
			if p23 == Enum.UserCFrame.Floor then
				p_u_22.recentered = true
			end
		end)
	else
		if p_u_22.inFirstPerson then
			p_u_22:GamepadZoomPress()
		end
		if p_u_22.thirdPersonOptionChanged then
			p_u_22.thirdPersonOptionChanged:Disconnect()
			p_u_22.thirdPersonOptionChanged = nil
		end
		if p_u_22.vrRecentered then
			p_u_22.vrRecentered:Disconnect()
			p_u_22.vrRecentered = nil
		end
		if p_u_22.cameraHeadScaleChangedConn then
			p_u_22.cameraHeadScaleChangedConn:Disconnect()
			p_u_22.cameraHeadScaleChangedConn = nil
		end
		if p_u_22.gamepadResetConnection then
			p_u_22.gamepadResetConnection:Disconnect()
			p_u_22.gamepadResetConnection = nil
		end
		if not v_u_12 then
			p_u_22.VREdgeBlurTimer = 0
			p_u_22:UpdateEdgeBlur(v_u_5, 1)
		end
		local v24 = v_u_6:FindFirstChild("VRFade")
		if v24 then
			v24.Brightness = 0
		end
	end
end
function v_u_14.OnCurrentCameraChanged(p_u_25) -- name: OnCurrentCameraChanged
	-- upvalues: (copy) v_u_13
	v_u_13.OnCurrentCameraChanged(p_u_25)
	if p_u_25.cameraHeadScaleChangedConn then
		p_u_25.cameraHeadScaleChangedConn:Disconnect()
		p_u_25.cameraHeadScaleChangedConn = nil
	end
	local v26 = workspace.CurrentCamera
	if v26 then
		p_u_25.cameraHeadScaleChangedConn = v26:GetPropertyChangedSignal("HeadScale"):Connect(function()
			-- upvalues: (copy) p_u_25
			p_u_25:OnHeadScaleChanged()
		end)
		p_u_25:OnHeadScaleChanged()
	end
end
function v_u_14.OnHeadScaleChanged(p27) -- name: OnHeadScaleChanged
	local v28 = workspace.CurrentCamera.HeadScale
	for v29, v30 in p27.gamepadZoomLevels do
		p27.gamepadZoomLevels[v29] = v30 * v28 / p27.headScale
	end
	p27:SetCameraToSubjectDistance(p27:GetCameraToSubjectDistance() * v28 / p27.headScale)
	p27.headScale = v28
end
function v_u_14.GetVRFocus(p31, p32, p33) -- name: GetVRFocus
	local v34 = p31.lastCameraFocus or p32
	local v35 = p31.cameraTranslationConstraints.x
	local v36 = p31.cameraTranslationConstraints.y + p33
	local v37 = math.min(1, v36)
	local v38 = p31.cameraTranslationConstraints.z
	p31.cameraTranslationConstraints = Vector3.new(v35, v37, v38)
	local v39 = p31:GetCameraHeight()
	local v40 = Vector3.new(0, v39, 0)
	local v41 = CFrame.new
	local v42 = p32.x
	local v43 = v34.y
	local v44 = p32.z
	return v41(Vector3.new(v42, v43, v44):Lerp(p32 + v40, p31.cameraTranslationConstraints.y))
end
function v_u_14.StartFadeFromBlack(p45) -- name: StartFadeFromBlack
	-- upvalues: (copy) v_u_8, (copy) v_u_6
	if v_u_8.VignetteEnabled ~= false then
		local v46 = v_u_6:FindFirstChild("VRFade")
		if not v46 then
			v46 = Instance.new("ColorCorrectionEffect")
			v46.Name = "VRFade"
			v46.Parent = v_u_6
		end
		v46.Brightness = -1
		p45.VRFadeResetTimer = 0.1
	end
end
function v_u_14.UpdateFadeFromBlack(p47, p48) -- name: UpdateFadeFromBlack
	-- upvalues: (copy) v_u_6
	local v49 = v_u_6:FindFirstChild("VRFade")
	if p47.VRFadeResetTimer > 0 then
		local v50 = p47.VRFadeResetTimer - p48
		p47.VRFadeResetTimer = math.max(v50, 0)
		local v51 = v_u_6:FindFirstChild("VRFade")
		if v51 and v51.Brightness < 0 then
			local v52 = v51.Brightness + p48 * 10
			v51.Brightness = math.min(v52, 0)
			return
		end
	elseif v49 then
		v49.Brightness = 0
	end
end
function v_u_14.StartVREdgeBlur(p53, p54, p55) -- name: StartVREdgeBlur
	-- upvalues: (copy) v_u_8, (copy) v_u_7, (copy) v_u_4
	if p55 or v_u_8.VignetteEnabled ~= false then
		local v56 = workspace.CurrentCamera:FindFirstChild("VRBlurPart")
		if not v56 then
			local v_u_57 = Instance.new("Part")
			v_u_57.Name = "VRBlurPart"
			v_u_57.Parent = workspace.CurrentCamera
			v_u_57.CanTouch = false
			v_u_57.CanCollide = false
			v_u_57.CanQuery = false
			v_u_57.Anchored = true
			v_u_57.Size = Vector3.new(0.44, 0.47, 1)
			v_u_57.Transparency = 1
			v_u_57.CastShadow = false
			v_u_7.RenderStepped:Connect(function(_)
				-- upvalues: (ref) v_u_4, (ref) v_u_57
				local v58 = v_u_4:GetUserCFrame(Enum.UserCFrame.Head)
				local v59 = workspace.CurrentCamera.CFrame * (CFrame.new(v58.p * workspace.CurrentCamera.HeadScale) * (v58 - v58.p))
				v_u_57.CFrame = v59 * CFrame.Angles(0, 3.141592653589793, 0) + v59.LookVector * (1.05 * workspace.CurrentCamera.HeadScale)
				v_u_57.Size = Vector3.new(0.44, 0.47, 1) * workspace.CurrentCamera.HeadScale
			end)
			v56 = v_u_57
		end
		local v60 = p54.PlayerGui:FindFirstChild("VRBlurScreen")
		local v61
		if v60 then
			v61 = v60:FindFirstChild("VRBlur")
		else
			v61 = nil
		end
		if not v61 then
			local v62 = v60 or (Instance.new("SurfaceGui") or Instance.new("ScreenGui"))
			v62.Name = "VRBlurScreen"
			v62.Parent = p54.PlayerGui
			v62.Adornee = v56
			v61 = Instance.new("ImageLabel")
			v61.Name = "VRBlur"
			v61.Parent = v62
			v61.Image = "rbxasset://textures/ui/VR/edgeBlur.png"
			v61.AnchorPoint = Vector2.new(0.5, 0.5)
			v61.Position = UDim2.new(0.5, 0, 0.5, 0)
			local v63 = workspace.CurrentCamera.ViewportSize.X * 2.3 / 512
			local v64 = workspace.CurrentCamera.ViewportSize.Y * 2.3 / 512
			v61.Size = UDim2.fromScale(v63, v64)
			v61.BackgroundTransparency = 1
			v61.Active = true
			v61.ScaleType = Enum.ScaleType.Stretch
		end
		v61.Visible = true
		v61.ImageTransparency = 0
		p53.VREdgeBlurTimer = 0.14
	end
end
function v_u_14.UpdateEdgeBlur(p65, p66, p67) -- name: UpdateEdgeBlur
	local v68 = p66.PlayerGui:FindFirstChild("VRBlurScreen")
	local v69
	if v68 then
		v69 = v68:FindFirstChild("VRBlur")
	else
		v69 = nil
	end
	if v69 then
		if p65.VREdgeBlurTimer > 0 then
			p65.VREdgeBlurTimer = p65.VREdgeBlurTimer - p67
			local v70 = p66.PlayerGui:FindFirstChild("VRBlurScreen")
			local v71 = v70 and v70:FindFirstChild("VRBlur")
			if v71 then
				local v72 = p65.VREdgeBlurTimer
				v71.ImageTransparency = 1 - math.clamp(v72, 0.01, 0.14) * 7.142857142857142
				return
			end
		else
			v69.Visible = false
		end
	end
end
function v_u_14.GetCameraHeight(p73) -- name: GetCameraHeight
	return p73.inFirstPerson and 0 or 0.25881904510252074 * p73.currentSubjectDistance
end
function v_u_14.GetSubjectCFrame(p74) -- name: GetSubjectCFrame
	-- upvalues: (copy) v_u_13
	local v75 = v_u_13.GetSubjectCFrame(p74)
	local v76 = workspace.CurrentCamera
	if v76 then
		v76 = v76.CameraSubject
	end
	if not v76 then
		return v75
	end
	if v76:IsA("Humanoid") and (v76:GetState() == Enum.HumanoidStateType.Dead and v76 == p74.lastSubject) then
		v75 = p74.lastSubjectCFrame
	end
	if v75 then
		p74.lastSubjectCFrame = v75
	end
	return v75
end
function v_u_14.GetSubjectPosition(p77) -- name: GetSubjectPosition
	-- upvalues: (copy) v_u_13
	local v78 = v_u_13.GetSubjectPosition(p77)
	local v79 = game.Workspace.CurrentCamera
	if v79 then
		v79 = v79.CameraSubject
	end
	if not v79 then
		return nil
	end
	if v79:IsA("Humanoid") then
		if v79:GetState() == Enum.HumanoidStateType.Dead and v79 == p77.lastSubject then
			v78 = p77.lastSubjectPosition
		end
	elseif v79:IsA("VehicleSeat") then
		v78 = v79.CFrame.p + v79.CFrame:vectorToWorldSpace(Vector3.new(0, 4, 0))
	end
	p77.lastSubjectPosition = v78
	return v78
end
function v_u_14.getRotation(p80, p81) -- name: getRotation
	-- upvalues: (copy) v_u_9, (copy) v_u_8
	local v82 = v_u_9.getRotation(p81)
	local v83 = 0
	if v_u_8.VRSmoothRotationEnabled then
		return v82.X
	end
	local v84 = v82.X
	if math.abs(v84) > 0.03 then
		if p80.stepRotateTimeout > 0 then
			p80.stepRotateTimeout = p80.stepRotateTimeout - p81
		end
		if p80.stepRotateTimeout <= 0 then
			local v85 = (v82.X < 0 and -1 or 1) * 0.5235987755982988
			p80:StartFadeFromBlack()
			p80.stepRotateTimeout = 0.25
			return v85
		end
	else
		local v86 = v82.X
		if math.abs(v86) < 0.02 then
			p80.stepRotateTimeout = 0
		end
	end
	return v83
end
function v_u_14.HandleSubjectDistance(p87, p88) -- name: HandleSubjectDistance
	-- upvalues: (ref) v_u_3
	if v_u_3 and (p88 and (p88.IsInFirstPerson and p88:IsInFirstPerson())) then
		p87:SetCameraToSubjectDistance(0)
	end
end
return v_u_14

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.ZoomController
==================================================
local v_u_1 = require(script:WaitForChild("Popper"))
local v_u_2 = math.clamp
local v_u_3 = math.exp
local v_u_4 = math.min
local v_u_5 = math.max
local v_u_6 = nil
local v_u_7 = nil
local v_u_8 = game:GetService("Players").LocalPlayer
assert(v_u_8)
local function v9() -- name: updateBounds
	-- upvalues: (ref) v_u_6, (copy) v_u_8, (ref) v_u_7
	v_u_6 = v_u_8.CameraMinZoomDistance
	v_u_7 = v_u_8.CameraMaxZoomDistance
end
v_u_6 = v_u_8.CameraMinZoomDistance
v_u_7 = v_u_8.CameraMaxZoomDistance
v_u_8:GetPropertyChangedSignal("CameraMinZoomDistance"):Connect(v9)
v_u_8:GetPropertyChangedSignal("CameraMaxZoomDistance"):Connect(v9)
local v_u_10 = {}
v_u_10.__index = v_u_10
function v_u_10.new(p11, p12, p13, p14) -- name: new
	-- upvalues: (copy) v_u_2, (copy) v_u_10
	local v15 = v_u_2(p12, p13, p14)
	local v16 = v_u_10
	return setmetatable({
		["freq"] = nil,
		["x"] = nil,
		["v"] = 0,
		["minValue"] = nil,
		["maxValue"] = nil,
		["goal"] = nil,
		["freq"] = p11,
		["x"] = v15,
		["minValue"] = p13,
		["maxValue"] = p14,
		["goal"] = v15
	}, v16)
end
function v_u_10.Step(p17, p18) -- name: Step
	-- upvalues: (copy) v_u_3
	local v19 = p17.freq * 2 * 3.141592653589793
	local v20 = p17.x
	local v21 = p17.v
	local v22 = p17.minValue
	local v23 = p17.maxValue
	local v24 = p17.goal
	local v25 = v24 - v20
	local v26 = v19 * p18
	local v27 = v_u_3(-v26)
	local v28 = v24 + (v21 * p18 - v25 * (v26 + 1)) * v27
	local v29 = ((v25 * v19 - v21) * v26 + v21) * v27
	if v28 < v22 then
		v23 = v22
		v29 = 0
	elseif v23 < v28 then
		v29 = 0
	else
		v23 = v28
	end
	p17.x = v23
	p17.v = v29
	return v23
end
local v_u_30 = v_u_10.new(4.5, 12.5, 0.5, v_u_7)
local v_u_31 = 0
return {
	["Update"] = function(p32, p33, p34) -- name: Update
		-- upvalues: (copy) v_u_30, (ref) v_u_31, (ref) v_u_6, (ref) v_u_7, (copy) v_u_2, (copy) v_u_5, (copy) v_u_1, (copy) v_u_4
		local v35
		if v_u_30.goal > 1 then
			local v36 = v_u_30.x
			local v37 = v_u_30.goal
			local v38 = v_u_31
			local v39 = v_u_6
			local v40 = v_u_7
			local v41 = v_u_2(v37 + v38 * (v37 * 0.0375 + 1), v39, v40)
			local v42 = v_u_5(v36, v41 < 1 and (v38 <= 0 and v39 and v39 or 1) or v41)
			v35 = v_u_1(p33 * CFrame.new(0, 0, 0.5), v42 - 0.5, p34) + 0.5
		else
			v35 = (1 / 0)
		end
		v_u_30.minValue = 0.5
		v_u_30.maxValue = v_u_4(v_u_7, v35)
		return v_u_30:Step(p32)
	end,
	["GetZoomRadius"] = function() -- name: GetZoomRadius
		-- upvalues: (copy) v_u_30
		return v_u_30.x
	end,
	["SetZoomParameters"] = function(p43, p44) -- name: SetZoomParameters
		-- upvalues: (copy) v_u_30, (ref) v_u_31
		v_u_30.goal = p43
		v_u_31 = p44
	end,
	["ReleaseSpring"] = function() -- name: ReleaseSpring
		-- upvalues: (copy) v_u_30
		v_u_30.x = v_u_30.goal
		v_u_30.v = 0
	end
}

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.ZoomController.Popper
==================================================
local v1 = game:GetService("Players")
local v2 = script.Parent.Parent.Parent:WaitForChild("CommonUtils")
local v3 = require(v2:WaitForChild("FlagUtil"))
local v4 = require(v2:WaitForChild("CameraWrapper"))
local v5 = require(v2:WaitForChild("ConnectionUtil"))
local v_u_6 = v3.getUserFlag("UserRaycastUpdateAPI2")
local v_u_7 = v3.getUserFlag("UserCurrentCameraUpdate2")
local v_u_8 = v3.getUserFlag("UserPlayerConnectionMemoryLeak")
local v_u_9
if v_u_7 then
	v_u_9 = v4.new()
else
	v_u_9 = nil
end
local v_u_10
if v_u_7 then
	v_u_10 = nil
else
	v_u_10 = game.Workspace.CurrentCamera
end
if v_u_7 then
	v_u_9:Enable()
end
local v_u_11 = math.min
local v_u_12 = math.tan
local v_u_13 = math.rad
local v_u_14 = Ray.new
local v_u_15 = RaycastParams.new()
v_u_15.IgnoreWater = true
v_u_15.FilterType = Enum.RaycastFilterType.Exclude
v_u_15.RespectCanCollide = true
local v_u_16 = RaycastParams.new()
v_u_16.IgnoreWater = true
v_u_16.FilterType = Enum.RaycastFilterType.Include
local v_u_17
if v_u_8 then
	v_u_17 = v5.new()
else
	v_u_17 = nil
end
local v_u_18 = nil
local v_u_19 = nil
local v_u_20, v_u_21, v_u_22
if v_u_7 then
	local function v27() -- name: updateProjection
		-- upvalues: (copy) v_u_9, (copy) v_u_13, (ref) v_u_19, (copy) v_u_12, (ref) v_u_18
		local v23 = v_u_9:getCamera()
		local v24 = v_u_13(v23.FieldOfView)
		local v25 = v23.ViewportSize
		local v26 = v25.X / v25.Y
		v_u_19 = v_u_12(v24 / 2) * 2
		v_u_18 = v26 * v_u_19
	end
	v_u_9:Connect("FieldOfView", v27)
	v_u_9:Connect("ViewportSize", v27)
	local v28 = v_u_9:getCamera()
	local v29 = v_u_13(v28.FieldOfView)
	local v30 = v28.ViewportSize
	local v31 = v30.X / v30.Y
	local v32 = v_u_12(v29 / 2) * 2
	local v33 = v31 * v32
	local v_u_34 = v_u_9:getCamera().NearPlaneZ
	v_u_9:Connect("NearPlaneZ", function()
		-- upvalues: (ref) v_u_34, (copy) v_u_9
		v_u_34 = v_u_9:getCamera().NearPlaneZ
	end)
	v_u_20 = v32
	v_u_21 = v33
	v_u_22 = v_u_34
else
	local function v38() -- name: updateProjection
		-- upvalues: (ref) v_u_10, (copy) v_u_13, (ref) v_u_19, (copy) v_u_12, (ref) v_u_18
		local v35 = v_u_13(v_u_10.FieldOfView)
		local v36 = v_u_10.ViewportSize
		local v37 = v36.X / v36.Y
		v_u_19 = v_u_12(v35 / 2) * 2
		v_u_18 = v37 * v_u_19
	end
	v_u_10:GetPropertyChangedSignal("FieldOfView"):Connect(v38)
	v_u_10:GetPropertyChangedSignal("ViewportSize"):Connect(v38)
	local v39 = v_u_13(v_u_10.FieldOfView)
	local v40 = v_u_10.ViewportSize
	local v41 = v40.X / v40.Y
	local v42 = v_u_12(v39 / 2) * 2
	local v43 = v41 * v42
	local v_u_44 = v_u_10.NearPlaneZ
	v_u_10:GetPropertyChangedSignal("NearPlaneZ"):Connect(function()
		-- upvalues: (ref) v_u_44, (ref) v_u_10
		v_u_44 = v_u_10.NearPlaneZ
	end)
	v_u_20 = v42
	v_u_21 = v43
	v_u_22 = v_u_44
end
local v_u_45 = {}
local v_u_46 = {}
local function v57(p_u_47) -- name: playerAdded
	-- upvalues: (copy) v_u_46, (ref) v_u_45, (copy) v_u_8, (copy) v_u_17
	local function v51(p48) -- name: characterAdded
		-- upvalues: (ref) v_u_46, (copy) p_u_47, (ref) v_u_45
		v_u_46[p_u_47] = p48
		local v49 = 1
		v_u_45 = {}
		for _, v50 in pairs(v_u_46) do
			v_u_45[v49] = v50
			v49 = v49 + 1
		end
	end
	local function v54() -- name: characterRemoving
		-- upvalues: (ref) v_u_46, (copy) p_u_47, (ref) v_u_45
		v_u_46[p_u_47] = nil
		local v52 = 1
		v_u_45 = {}
		for _, v53 in pairs(v_u_46) do
			v_u_45[v52] = v53
			v52 = v52 + 1
		end
	end
	if v_u_8 then
		v_u_17:trackConnection(("%*CharacterAdded"):format(p_u_47.UserId), p_u_47.CharacterAdded:Connect(v51))
		v_u_17:trackConnection(("%*CharacterRemoving"):format(p_u_47.UserId), p_u_47.CharacterRemoving:Connect(v54))
	else
		p_u_47.CharacterAdded:Connect(v51)
		p_u_47.CharacterRemoving:Connect(v54)
	end
	if p_u_47.Character then
		v_u_46[p_u_47] = p_u_47.Character
		local v55 = 1
		v_u_45 = {}
		for _, v56 in pairs(v_u_46) do
			v_u_45[v55] = v56
			v55 = v55 + 1
		end
	end
end
local function v61(p58) -- name: playerRemoving
	-- upvalues: (copy) v_u_46, (ref) v_u_45, (copy) v_u_8, (copy) v_u_17
	v_u_46[p58] = nil
	local v59 = 1
	v_u_45 = {}
	for _, v60 in pairs(v_u_46) do
		v_u_45[v59] = v60
		v59 = v59 + 1
	end
	if v_u_8 then
		v_u_17:disconnect((("%*CharacterAdded"):format(p58.UserId)))
		v_u_17:disconnect((("%*CharacterRemoving"):format(p58.UserId)))
	end
end
v1.PlayerAdded:Connect(v57)
v1.PlayerRemoving:Connect(v61)
for _, v62 in ipairs(v1:GetPlayers()) do
	v57(v62)
end
local v63 = 1
v_u_45 = {}
local v_u_64 = v_u_45
for _, v65 in pairs(v_u_46) do
	v_u_64[v63] = v65
	v63 = v63 + 1
end
local v_u_66 = nil
local v_u_67 = nil
if v_u_7 then
	v_u_9:Connect("CameraSubject", function()
		-- upvalues: (copy) v_u_9, (ref) v_u_67
		local v68 = v_u_9:getCamera().CameraSubject
		if v68 and v68:IsA("Humanoid") then
			v_u_67 = v68.RootPart
			return
		elseif v68 and v68:IsA("BasePart") then
			v_u_67 = v68
		else
			v_u_67 = nil
		end
	end)
else
	v_u_10:GetPropertyChangedSignal("CameraSubject"):Connect(function()
		-- upvalues: (ref) v_u_10, (ref) v_u_67
		local v69 = v_u_10.CameraSubject
		if v69:IsA("Humanoid") then
			v_u_67 = v69.RootPart
			return
		elseif v69:IsA("BasePart") then
			v_u_67 = v69
		else
			v_u_67 = nil
		end
	end)
end
local v_u_70 = {
	Vector2.new(0.4, 0),
	Vector2.new(-0.4, 0),
	Vector2.new(0, -0.4),
	Vector2.new(0, 0.4),
	Vector2.new(0, 0.2)
}
local function v_u_81(p71, p72) -- name: getCollisionPoint
	-- upvalues: (copy) v_u_6, (copy) v_u_15, (ref) v_u_64, (copy) v_u_14
	if v_u_6 then
		v_u_15.FilterDescendantsInstances = v_u_64
		local v73 = workspace:Raycast(p71, p72, v_u_15)
		if v73 then
			return v73.Position, true
		end
		::l4::
		return p71 + p72, false
	else
		local v74 = #v_u_64
		while true do
			local v75, v76 = workspace:FindPartOnRayWithIgnoreList(v_u_14(p71, p72), v_u_64, false, true)
			if v75 then
				if v75.CanCollide then
					local v77 = v_u_64
					for v78 = #v77, v74 + 1, -1 do
						v77[v78] = nil
					end
					return v76, true
				end
				v_u_64[#v_u_64 + 1] = v75
			end
			if not v75 then
				local v79 = v_u_64
				for v80 = #v79, v74 + 1, -1 do
					v79[v80] = nil
				end
				goto l4
			end
		end
	end
end
local function v_u_109(p82, p83, p84, p85) -- name: queryPoint
	-- upvalues: (ref) v_u_64, (ref) v_u_22, (copy) v_u_6, (copy) v_u_15, (ref) v_u_66, (copy) v_u_16, (copy) v_u_14
	debug.profilebegin("queryPoint")
	local v86 = #v_u_64
	local v87 = p84 + v_u_22
	local v88 = p82 + p83 * v87
	local v89 = (1 / 0)
	local v90 = (1 / 0)
	local v91 = 0
	local v92
	if v_u_6 then
		v_u_15.FilterDescendantsInstances = v_u_64
		local v93 = p82
		while true do
			local v94 = workspace:Raycast(p82, v88 - p82, v_u_15)
			if not v94 then
				v92 = v89
				break
			end
			v91 = v91 + 1
			local v95 = v94.Instance
			local v96 = v94.Position
			v92 = (v96 - v93).Magnitude
			if v91 >= 64 then
				v90 = v92
				v92 = v89
			else
				local v97 = 1 - (1 - v95.Transparency) * (1 - v95.LocalTransparencyModifier) < 0.25 and (v_u_6 or v95.CanCollide)
				if v97 then
					if v_u_66 == (v95:GetRootPart() or v95) then
						v97 = false
					else
						v97 = not v95:IsA("TrussPart")
					end
				end
				if v97 then
					v_u_16.FilterDescendantsInstances = { v95 }
					if workspace:Raycast(v88, v96 - v88, v_u_16) then
						local v98
						if p85 then
							v98 = workspace:Raycast(p85, v88 - p85, v_u_16) or workspace:Raycast(v88, p85 - v88, v_u_16)
						else
							v98 = false
						end
						if v98 then
							v90 = v92
							v92 = v89
						elseif v87 >= v89 then
							v92 = v89
						end
					else
						v90 = v92
						v92 = v89
					end
				else
					v92 = v89
				end
			end
			v_u_15:AddToFilter(v95)
			p82 = v96 - p83 * 0.001
			if v90 < (1 / 0) or not v95 then
				break
			end
			v89 = v92
		end
	else
		local v99 = p82
		while true do
			if true then
				local v100, v101 = workspace:FindPartOnRayWithIgnoreList(v_u_14(p82, v88 - p82), v_u_64, false, true)
				v91 = v91 + 1
				if v100 then
					local v102 = v91 >= 64
					local v103 = 1 - (1 - v100.Transparency) * (1 - v100.LocalTransparencyModifier) < 0.25 and (v_u_6 or v100.CanCollide)
					if v103 then
						if v_u_66 == (v100:GetRootPart() or v100) then
							v103 = false
						else
							v103 = not v100:IsA("TrussPart")
						end
					end
					if v103 or v102 then
						local v104 = { v100 }
						local v105 = workspace:FindPartOnRayWithWhitelist(v_u_14(v88, v101 - v88), v104, true)
						v92 = (v101 - v99).Magnitude
						if v105 and not v102 then
							local v106
							if p85 then
								v106 = workspace:FindPartOnRayWithWhitelist(v_u_14(p85, v88 - p85), v104, true) or workspace:FindPartOnRayWithWhitelist(v_u_14(v88, p85 - v88), v104, true)
							else
								v106 = false
							end
							if v106 then
								v90 = v92
								v92 = v89
							elseif v87 >= v89 then
								v92 = v89
							end
						else
							v90 = v92
							v92 = v89
						end
					else
						v92 = v89
					end
					v_u_64[#v_u_64 + 1] = v100
					p82 = v101 - p83 * 0.001
				else
					v92 = v89
				end
			end
			if v90 < (1 / 0) or not v100 then
				break
			end
			v89 = v92
		end
		local v107 = v_u_64
		for v108 = #v107, v86 + 1, -1 do
			v107[v108] = nil
		end
	end
	debug.profileend()
	return v92 - v_u_22, v90 - v_u_22
end
local function v_u_125(p110, p111) -- name: queryViewport
	-- upvalues: (ref) v_u_10, (copy) v_u_7, (copy) v_u_9, (ref) v_u_21, (ref) v_u_20, (ref) v_u_22, (copy) v_u_109
	debug.profilebegin("queryViewport")
	local v112 = p110.p
	local v113 = p110.rightVector
	local v114 = p110.upVector
	local v115 = -p110.lookVector
	local v116
	if v_u_7 then
		v116 = v_u_9:getCamera()
	else
		v116 = v_u_10
	end
	v_u_10 = v116
	local v117 = v_u_10.ViewportSize
	local v118 = (1 / 0)
	local v119 = (1 / 0)
	for v120 = 0, 1 do
		local v121 = v113 * ((v120 - 0.5) * v_u_21)
		for v122 = 0, 1 do
			local v123, v124 = v_u_109(v112 + v_u_22 * (v121 + v114 * ((v122 - 0.5) * v_u_20)), v115, p111, v_u_10:ViewportPointToRay(v117.x * v120, v117.y * v122).Origin)
			if v124 >= v119 then
				v124 = v119
			end
			if v123 < v118 then
				v119 = v124
				v118 = v123
			else
				v119 = v124
			end
		end
	end
	debug.profileend()
	return v118, v119
end
local function v_u_139(p126, p127, p128) -- name: testPromotion
	-- upvalues: (copy) v_u_81, (copy) v_u_11, (copy) v_u_109, (copy) v_u_70
	debug.profilebegin("testPromotion")
	local v129 = p126.p
	local v130 = p126.rightVector
	local v131 = p126.upVector
	local v132 = -p126.lookVector
	debug.profilebegin("extrapolate")
	local v133 = (v_u_81(v129, p128.posVelocity * 1.25) - v129).Magnitude
	local v134 = p128.posVelocity.magnitude
	for v135 = 0, v_u_11(1.25, p128.rotVelocity.magnitude + v133 / v134), 0.0625 do
		local v136 = p128.extrapolate(v135)
		if p127 <= v_u_109(v136.p, -v136.lookVector, p127) then
			return false
		end
	end
	debug.profileend()
	debug.profilebegin("testOffsets")
	for _, v137 in ipairs(v_u_70) do
		local v138 = v_u_81(v129, v130 * v137.x + v131 * v137.y)
		if v_u_109(v138, (v129 + v132 * p127 - v138).Unit, p127) == (1 / 0) then
			return false
		end
	end
	debug.profileend()
	debug.profileend()
	return true
end
return function(p140, p141, p142) -- name: Popper
	-- upvalues: (ref) v_u_66, (ref) v_u_67, (copy) v_u_125, (copy) v_u_139
	debug.profilebegin("popper")
	v_u_66 = v_u_67 and v_u_67:GetRootPart() or v_u_67
	local v143, v144 = v_u_125(p140, p141)
	if v144 >= p141 then
		v144 = p141
	end
	if v143 < v144 then
		if not v_u_139(p140, p141, p142) then
			v143 = v144
		end
	else
		v143 = v144
	end
	v_u_66 = nil
	debug.profileend()
	return v143
end

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.CameraToggleStateController
==================================================
game:GetService("Players")
game:GetService("UserInputService")
UserSettings():GetService("UserGameSettings")
local v_u_1 = require(script.Parent:WaitForChild("CameraInput"))
local v_u_2 = require(script.Parent:WaitForChild("CameraUI"))
local v_u_3 = require(script.Parent:WaitForChild("CameraUtils"))
local v_u_4 = false
local v_u_5 = tick()
local v_u_6 = false
local v_u_7 = false
local v_u_8 = false
v_u_2.setCameraModeToastEnabled(false)
return function(p9)
	-- upvalues: (copy) v_u_1, (ref) v_u_4, (ref) v_u_6, (ref) v_u_5, (copy) v_u_2, (ref) v_u_8, (ref) v_u_7, (copy) v_u_3
	local v10 = v_u_1.getTogglePan()
	if p9 and v10 ~= v_u_4 then
		v_u_6 = true
	end
	if v_u_4 ~= v10 or tick() - v_u_5 > 3 then
		local v11
		if v10 then
			v11 = tick() - v_u_5 < 3
		else
			v11 = v10
		end
		v_u_2.setCameraModeToastOpen(v11)
		if v10 then
			v_u_6 = false
		end
		v_u_5 = tick()
		v_u_4 = v10
	end
	if p9 ~= v_u_8 then
		if p9 then
			v_u_7 = v_u_1.getTogglePan()
			v_u_1.setTogglePan(true)
		elseif not v_u_6 then
			v_u_1.setTogglePan(v_u_7)
		end
	end
	if p9 then
		if v_u_1.getTogglePan() then
			v_u_3.setMouseIconOverride("rbxasset://textures/Cursors/CrossMouseIcon.png")
			v_u_3.setMouseBehaviorOverride(Enum.MouseBehavior.LockCenter)
			v_u_3.setRotationTypeOverride(Enum.RotationType.CameraRelative)
		else
			v_u_3.restoreMouseIcon()
			v_u_3.restoreMouseBehavior()
			v_u_3.setRotationTypeOverride(Enum.RotationType.CameraRelative)
		end
	elseif v_u_1.getTogglePan() then
		v_u_3.setMouseIconOverride("rbxasset://textures/Cursors/CrossMouseIcon.png")
		v_u_3.setMouseBehaviorOverride(Enum.MouseBehavior.LockCenter)
		v_u_3.setRotationTypeOverride(Enum.RotationType.MovementRelative)
	elseif v_u_1.getHoldPan() then
		v_u_3.restoreMouseIcon()
		v_u_3.setMouseBehaviorOverride(Enum.MouseBehavior.LockCurrentPosition)
		v_u_3.setRotationTypeOverride(Enum.RotationType.MovementRelative)
	else
		v_u_3.restoreMouseIcon()
		v_u_3.restoreMouseBehavior()
		v_u_3.restoreRotationType()
	end
	v_u_8 = p9
end

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.VRVehicleCameraDeprecated
==================================================
local v1, v2 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserVRVehicleCamera2")
end)
local v_u_3 = v1 and v2
local v_u_4 = { 0, 30 }
local v_u_5 = UserSettings():GetService("UserGameSettings")
local v_u_6 = require(script.Parent:WaitForChild("VRBaseCamera"))
local v_u_7 = require(script.Parent:WaitForChild("CameraInput"))
local v_u_8 = require(script.Parent:WaitForChild("CameraUtils"))
require(script.Parent:WaitForChild("VehicleCamera"))
local v_u_9 = require(script.Parent.VehicleCamera:FindFirstChild("VehicleCameraCore"))
local v_u_10 = require(script.Parent.VehicleCamera:FindFirstChild("VehicleCameraConfig"))
local v11 = game:GetService("Players")
local v_u_12 = game:GetService("RunService")
local v_u_13 = game:GetService("VRService")
local v_u_14 = v11.LocalPlayer
local v_u_15 = v_u_8.Spring
local v_u_16 = v_u_8.mapClamp
local v_u_17 = v_u_8.sanitizeAngle
local v_u_18 = 0.016666666666666666
local v_u_19 = setmetatable({}, v_u_6)
v_u_19.__index = v_u_19
function v_u_19.new() -- name: new
	-- upvalues: (copy) v_u_6, (copy) v_u_19, (copy) v_u_12, (ref) v_u_18
	local v20 = v_u_6.new()
	local v21 = v_u_19
	local v22 = setmetatable(v20, v21)
	v22:Reset()
	v_u_12.Stepped:Connect(function(_, p23)
		-- upvalues: (ref) v_u_18
		v_u_18 = p23
	end)
	return v22
end
function v_u_19.Reset(p24) -- name: Reset
	-- upvalues: (copy) v_u_9, (ref) v_u_3, (copy) v_u_15, (copy) v_u_10, (copy) v_u_8, (copy) v_u_4
	p24.vehicleCameraCore = v_u_9.new(p24:GetSubjectCFrame())
	if v_u_3 then
		p24.pitchSpring = v_u_15.new(0, 0)
	else
		local v25 = v_u_15.new
		local v26 = v_u_10.pitchBaseAngle
		p24.pitchSpring = v25(0, -math.rad(v26))
	end
	p24.yawSpring = v_u_15.new(0, 0)
	if v_u_3 then
		p24.lastPanTick = 0
		p24.currentDriftAngle = 0
		p24.needsReset = true
	end
	local v27 = workspace.CurrentCamera
	local v28
	if v27 then
		v28 = v27.CameraSubject
	else
		v28 = v27
	end
	assert(v27, "VRVehicleCamera initialization error")
	assert(v28)
	assert(v28:IsA("VehicleSeat"))
	local v29 = v28:GetConnectedParts(true)
	local v30, v31 = v_u_8.getLooseBoundingSphere(v29)
	p24.assemblyRadius = math.max(v31, 5)
	p24.assemblyOffset = v28.CFrame:Inverse() * v30
	p24.gamepadZoomLevels = {}
	for _, v32 in v_u_4 do
		local v33 = p24.gamepadZoomLevels
		local v34 = v32 * p24.headScale * p24.assemblyRadius / 10
		table.insert(v33, v34)
	end
	p24.lastCameraFocus = nil
	p24:SetCameraToSubjectDistance(p24.gamepadZoomLevels[#p24.gamepadZoomLevels])
end
function v_u_19._StepRotation(p35, p36, p37) -- name: _StepRotation
	-- upvalues: (copy) v_u_17, (copy) v_u_7, (copy) v_u_10, (copy) v_u_16
	local v38 = p35.yawSpring
	local v39 = p35.pitchSpring
	local v40 = -p35:getRotation(p36)
	v38.pos = v_u_17(v38.pos + v40)
	local v41 = v_u_17
	local v42 = v39.pos
	v39.pos = v41((math.clamp(v42, -1.3962634015954636, 1.3962634015954636)))
	if v_u_7.getRotationActivated() then
		p35.lastPanTick = os.clock()
	end
	local v43 = v_u_10.pitchDeadzoneAngle
	local v44 = math.rad(v43)
	if os.clock() - p35.lastPanTick > v_u_10.autocorrectDelay then
		local v45 = v_u_16(p37, v_u_10.autocorrectMinCarSpeed, v_u_10.autocorrectMaxCarSpeed, 0, v_u_10.autocorrectResponse)
		v38.freq = v45
		v39.freq = v45
		if v38.freq < 0.001 then
			v38.vel = 0
		end
		if v39.freq < 0.001 then
			v39.vel = 0
		end
		local v46 = v_u_17(0 - v39.pos)
		if math.abs(v46) <= v44 then
			v39.goal = v39.pos
		else
			v39.goal = 0
		end
	else
		v38.freq = 0
		v38.vel = 0
		v39.freq = 0
		v39.vel = 0
		v39.goal = 0
	end
	return CFrame.fromEulerAnglesYXZ(v39:step(p36), v38:step(p36), 0)
end
function v_u_19._GetThirdPersonLocalOffset(p47) -- name: _GetThirdPersonLocalOffset
	-- upvalues: (copy) v_u_10
	local v48 = p47.assemblyOffset
	local v49 = p47.assemblyRadius * v_u_10.verticalCenterOffset
	return v48 + Vector3.new(0, v49, 0)
end
function v_u_19._GetFirstPersonLocalOffset(p50, p51) -- name: _GetFirstPersonLocalOffset
	-- upvalues: (copy) v_u_14
	local v52 = v_u_14.Character
	if v52 and v52.Parent then
		local v53 = v52:FindFirstChild("Head")
		if v53 and v53:IsA("BasePart") then
			return p51:Inverse() * v53.Position
		end
	end
	return p50:_GetThirdPersonLocalOffset()
end
function v_u_19.Update(p54) -- name: Update
	-- upvalues: (ref) v_u_3, (ref) v_u_18, (copy) v_u_14, (copy) v_u_13
	if v_u_3 then
		local v55 = v_u_18
		v_u_18 = 0
		p54:UpdateFadeFromBlack(v55)
		p54:UpdateEdgeBlur(v_u_14, v55)
		if v_u_13.ThirdPersonFollowCamEnabled then
			local v56, v57 = p54:UpdateStepRotation(v55)
			return v56, v57
		else
			local v58, v59 = p54:UpdateComfortCamera(v55)
			return v58, v59
		end
	else
		return p54:UpdateComfortCamera()
	end
end
function v_u_19.addDrift(p60, p61, p62) -- name: addDrift
	-- upvalues: (copy) v_u_14, (copy) v_u_13
	local v63 = workspace.CurrentCamera
	local v64 = p60:GetCameraToSubjectDistance()
	local v65 = p60:GetSubjectVelocity()
	local v66 = p60:GetSubjectCFrame()
	require(v_u_14:WaitForChild("PlayerScripts").PlayerModule:WaitForChild("ControlModule"))
	if v65.Magnitude > 0.1 then
		local v67 = v_u_13:GetUserCFrame(Enum.UserCFrame.Head)
		local v68 = v67.Rotation + v67.Position * v63.HeadScale
		local v69 = v63.CFrame * v68
		local _, v70, _ = v69:ToEulerAnglesYXZ()
		local _, v71, _ = v66:ToEulerAnglesYXZ()
		local v72 = (v70 - p60.currentDriftAngle + 12.566370614359172) % 6.283185307179586
		if v72 > 3.141592653589793 then
			v72 = v72 - 6.283185307179586
		end
		local v73 = (v71 - p60.currentDriftAngle + 12.566370614359172) % 6.283185307179586
		if v73 > 3.141592653589793 then
			v73 = v73 - 6.283185307179586
		end
		local v74 = math.min(v73, v72)
		local v75 = math.max(v73, v72)
		local v76 = 0
		if v74 > 0 then
			v75 = v74
		elseif v75 >= 0 then
			v75 = v76
		end
		p60.currentDriftAngle = v75 + p60.currentDriftAngle
		local v77 = CFrame.fromEulerAnglesYXZ(0, p60.currentDriftAngle, 0).LookVector
		local v78 = v77.X
		local v79 = v77.Z
		local v80 = Vector3.new(v78, 0, v79).Unit * v64
		local v81 = p62.Position - v80
		p61 = p61:Lerp(CFrame.new(v63.CFrame.Position + v81 - v69.Position) * v63.CFrame.Rotation, 0.01)
	end
	return p61, p62
end
function v_u_19.UpdateRotationCamera(p82, p83) -- name: UpdateRotationCamera
	-- upvalues: (copy) v_u_16, (copy) v_u_14
	local v84 = workspace.CurrentCamera
	local v85
	if v84 then
		v85 = v84.CameraSubject
	else
		v85 = v84
	end
	local v86 = p82.vehicleCameraCore
	assert(v84)
	assert(v85)
	assert(v85:IsA("VehicleSeat"))
	local v87 = p82:GetSubjectCFrame()
	local v88 = p82:GetSubjectVelocity()
	local v89 = p82:GetSubjectRotVelocity()
	local v90 = v88:Dot(v87.ZVector)
	local v91 = math.abs(v90)
	local v92 = v87.YVector:Dot(v89)
	local v93 = math.abs(v92)
	local v94 = v87.XVector:Dot(v89)
	local v95 = math.abs(v94)
	local v96 = p82:GetCameraToSubjectDistance()
	local v97 = v_u_16(v96, 0.5, p82.assemblyRadius, 1, 0)
	local v98 = p82:_GetThirdPersonLocalOffset():Lerp(p82:_GetFirstPersonLocalOffset(v87), v97)
	v86:setTransform(v87)
	local v99 = v86:step(p83, v95, v93, v97)
	local v100 = p82:_StepRotation(p83, v91)
	local v101 = p82:GetVRFocus(v87 * v98, p83) * v99 * v100
	local v102 = v101 * CFrame.new(0, 0, v96)
	if v88.Magnitude > 0.1 then
		p82:StartVREdgeBlur(v_u_14)
	end
	return v102, v101
end
function v_u_19.UpdateStepRotation(p103, p104) -- name: UpdateStepRotation
	-- upvalues: (copy) v_u_16, (copy) v_u_5, (copy) v_u_13, (copy) v_u_14
	local v105 = workspace.CurrentCamera
	local v106 = p103.lastSubjectCFrame
	local v107 = p103:GetSubjectCFrame()
	local v108 = p103:GetSubjectVelocity()
	local v109 = p103:GetCameraToSubjectDistance()
	local v110 = v_u_16(v109, 0.5, p103.assemblyRadius, 1, 0)
	local v111 = p103:_GetThirdPersonLocalOffset():Lerp(p103:_GetFirstPersonLocalOffset(v107), v110)
	local v112 = p103:GetVRFocus(v107 * v111, p104)
	local v113, v114 = p103:addDrift(v112:ToWorldSpace(p103:GetVRFocus(v106 * v111, p104):ToObjectSpace(v105.CFrame)), v112)
	local v115 = p103:getRotation(p104)
	local v116
	if math.abs(v115) > 0 then
		local v117 = v114:ToObjectSpace(v113)
		v116 = v114 * CFrame.Angles(0, -v115, 0) * v117
		if not v_u_5.VRSmoothRotationEnabled then
			local v118 = v_u_13:GetUserCFrame(Enum.UserCFrame.Head)
			local v119 = v118.Rotation + v118.Position * v105.HeadScale
			local v120 = v114 * v107.Rotation
			local v121 = v120:ToObjectSpace(v113 * v119)
			local v122 = v121.X
			local v123 = v121.Z
			local v124 = Vector3.new(v122, 0, v123).Unit:Dot(Vector3.new(0, 0, 1))
			local v125 = math.acos(v124)
			local v126 = v120:ToObjectSpace(v116 * v119)
			local v127 = v126.X
			local v128 = v126.Z
			local v129 = Vector3.new(v127, 0, v128).Unit:Dot(Vector3.new(0, 0, 1))
			if math.acos(v129) < v125 then
				if v115 < 0 then
					v125 = v125 * -1
				end
				v116 = v114 * CFrame.Angles(0, -v125, 0) * v117
			end
		end
	else
		v116 = v113
	end
	if v108.Magnitude > 0.1 then
		p103:StartVREdgeBlur(v_u_14)
	end
	if p103.needsReset then
		p103.needsReset = false
		v_u_13:RecenterUserHeadCFrame()
		p103:StartFadeFromBlack()
		p103:ResetZoom()
	end
	if p103.recentered then
		v116 = v114 * v107.Rotation * CFrame.new(0, 0, v109)
		p103.recentered = false
	end
	return v116, v116 * CFrame.new(0, 0, -v109)
end
function v_u_19.UpdateComfortCamera(p130, p131) -- name: UpdateComfortCamera
	-- upvalues: (ref) v_u_3, (ref) v_u_18, (copy) v_u_16, (copy) v_u_14
	local v132 = workspace.CurrentCamera
	local v133
	if v132 then
		v133 = v132.CameraSubject
	else
		v133 = v132
	end
	local v134 = p130.vehicleCameraCore
	assert(v132)
	assert(v133)
	assert(v133:IsA("VehicleSeat"))
	if not v_u_3 then
		p131 = v_u_18
		v_u_18 = 0
	end
	local v135 = p130:GetSubjectCFrame()
	local v136 = p130:GetSubjectVelocity()
	local v137 = p130:GetSubjectRotVelocity()
	local v138 = v136:Dot(v135.ZVector)
	math.abs(v138)
	local v139 = v135.YVector:Dot(v137)
	local v140 = math.abs(v139)
	local v141 = v135.XVector:Dot(v137)
	local v142 = math.abs(v141)
	local v143 = p130:StepZoom()
	local v144 = v_u_16(v143, 0.5, p130.assemblyRadius, 1, 0)
	local v145 = p130:_GetThirdPersonLocalOffset():Lerp(p130:_GetFirstPersonLocalOffset(v135), v144)
	v134:setTransform(v135)
	local v146 = v134:step(p131, v142, v140, v144)
	if not v_u_3 then
		p130:UpdateFadeFromBlack(p131)
	end
	local v147, v148
	if p130:IsInFirstPerson() then
		local v149 = v146.LookVector.X
		local v150 = v146.LookVector.Z
		local v151 = Vector3.new(v149, 0, v150).Unit
		local v152 = CFrame.new(v146.Position, v151)
		v147 = CFrame.new(v135 * v145) * v152
		v148 = v147 * CFrame.new(0, 0, v143)
		if v_u_3 then
			if v136.Magnitude > 0.1 then
				p130:StartVREdgeBlur(v_u_14)
			end
		else
			p130:StartVREdgeBlur(v_u_14)
		end
	else
		v147 = CFrame.new(v135 * v145) * v146
		v148 = v147 * CFrame.new(0, 0, v143)
		if not p130.lastCameraFocus then
			p130.lastCameraFocus = v147
			p130.needsReset = true
		end
		local v153 = v147.Position - v132.CFrame.Position
		local v154 = v153.magnitude
		if v153.Unit:Dot(v132.CFrame.LookVector) > 0.56 and (v154 < 200 and not p130.needsReset) then
			v147 = p130.lastCameraFocus
			local v155 = v147.p
			local v156 = p130:GetCameraLookVector()
			local v157 = v156.X
			local v158 = v156.Z
			local v159 = p130:CalculateNewLookVectorFromArg(Vector3.new(v157, 0, v158).Unit, Vector2.new(0, 0))
			v148 = CFrame.new(v155 - v143 * v159, v155)
		else
			p130.lastCameraFocus = p130:GetVRFocus(v135.Position, p131)
			p130.needsReset = false
			p130:StartFadeFromBlack()
			p130:ResetZoom()
		end
		if not v_u_3 then
			p130:UpdateEdgeBlur(v_u_14, p131)
		end
	end
	return v148, v147
end
return v_u_19

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.OrbitalCamera
==================================================
local v1 = script.Parent.Parent:WaitForChild("CommonUtils")
local v_u_2 = require(v1:WaitForChild("FlagUtil")).getUserFlag("UserFixOrbitalCameraAzimuth")
local v_u_3 = require(script.Parent:WaitForChild("CameraUtils"))
local v_u_4 = require(script.Parent:WaitForChild("CameraInput"))
local v_u_5 = game:GetService("Players")
local v_u_6 = require(script.Parent:WaitForChild("BaseCamera"))
local v_u_7 = setmetatable({}, v_u_6)
v_u_7.__index = v_u_7
function v_u_7.new() -- name: new
	-- upvalues: (copy) v_u_6, (copy) v_u_7
	local v8 = v_u_6.new()
	local v9 = v_u_7
	local v10 = setmetatable(v8, v9)
	v10.lastUpdate = tick()
	v10.changedSignalConnections = {}
	v10.refAzimuthRad = nil
	v10.curAzimuthRad = nil
	v10.minAzimuthAbsoluteRad = nil
	v10.maxAzimuthAbsoluteRad = nil
	v10.useAzimuthLimits = nil
	v10.curElevationRad = nil
	v10.minElevationRad = nil
	v10.maxElevationRad = nil
	v10.curDistance = nil
	v10.minDistance = nil
	v10.maxDistance = nil
	v10.gamepadDollySpeedMultiplier = 1
	v10.lastUserPanCamera = tick()
	v10.externalProperties = {}
	v10.externalProperties.InitialDistance = 25
	v10.externalProperties.MinDistance = 10
	v10.externalProperties.MaxDistance = 100
	v10.externalProperties.InitialElevation = 35
	v10.externalProperties.MinElevation = 35
	v10.externalProperties.MaxElevation = 35
	v10.externalProperties.ReferenceAzimuth = -45
	v10.externalProperties.CWAzimuthTravel = 90
	v10.externalProperties.CCWAzimuthTravel = 90
	v10.externalProperties.UseAzimuthLimits = false
	v10:LoadNumberValueParameters()
	return v10
end
function v_u_7.LoadOrCreateNumberValueParameter(p_u_11, p_u_12, p13, p_u_14) -- name: LoadOrCreateNumberValueParameter
	local v15 = script:FindFirstChild(p_u_12)
	if v15 and v15:IsA(p13) then
		p_u_11.externalProperties[p_u_12] = v15.Value
	else
		if p_u_11.externalProperties[p_u_12] == nil then
			return
		end
		v15 = Instance.new(p13)
		v15.Name = p_u_12
		v15.Parent = script
		v15.Value = p_u_11.externalProperties[p_u_12]
	end
	if p_u_14 then
		if p_u_11.changedSignalConnections[p_u_12] then
			p_u_11.changedSignalConnections[p_u_12]:Disconnect()
		end
		p_u_11.changedSignalConnections[p_u_12] = v15.Changed:Connect(function(p16)
			-- upvalues: (copy) p_u_11, (copy) p_u_12, (copy) p_u_14
			p_u_11.externalProperties[p_u_12] = p16
			p_u_14(p_u_11)
		end)
	end
end
function v_u_7.SetAndBoundsCheckAzimuthValues(p17) -- name: SetAndBoundsCheckAzimuthValues
	local v18 = p17.externalProperties.ReferenceAzimuth
	local v19 = math.rad(v18)
	local v20 = p17.externalProperties.CWAzimuthTravel
	local v21 = math.rad(v20)
	p17.minAzimuthAbsoluteRad = v19 - math.abs(v21)
	local v22 = p17.externalProperties.ReferenceAzimuth
	local v23 = math.rad(v22)
	local v24 = p17.externalProperties.CCWAzimuthTravel
	local v25 = math.rad(v24)
	p17.maxAzimuthAbsoluteRad = v23 + math.abs(v25)
	p17.useAzimuthLimits = p17.externalProperties.UseAzimuthLimits
	if p17.useAzimuthLimits then
		local v26 = p17.curAzimuthRad
		local v27 = p17.minAzimuthAbsoluteRad
		p17.curAzimuthRad = math.max(v26, v27)
		local v28 = p17.curAzimuthRad
		local v29 = p17.maxAzimuthAbsoluteRad
		p17.curAzimuthRad = math.min(v28, v29)
	end
end
function v_u_7.SetAndBoundsCheckElevationValues(p30) -- name: SetAndBoundsCheckElevationValues
	local v31 = p30.externalProperties.MinElevation
	local v32 = math.max(v31, -80)
	local v33 = p30.externalProperties.MaxElevation
	local v34 = math.min(v33, 80)
	local v35 = math.min(v32, v34)
	p30.minElevationRad = math.rad(v35)
	local v36 = math.max(v32, v34)
	p30.maxElevationRad = math.rad(v36)
	local v37 = p30.curElevationRad
	local v38 = p30.minElevationRad
	p30.curElevationRad = math.max(v37, v38)
	local v39 = p30.curElevationRad
	local v40 = p30.maxElevationRad
	p30.curElevationRad = math.min(v39, v40)
end
function v_u_7.SetAndBoundsCheckDistanceValues(p41) -- name: SetAndBoundsCheckDistanceValues
	p41.minDistance = p41.externalProperties.MinDistance
	p41.maxDistance = p41.externalProperties.MaxDistance
	local v42 = p41.curDistance
	local v43 = p41.minDistance
	p41.curDistance = math.max(v42, v43)
	local v44 = p41.curDistance
	local v45 = p41.maxDistance
	p41.curDistance = math.min(v44, v45)
end
function v_u_7.LoadNumberValueParameters(p46) -- name: LoadNumberValueParameters
	-- upvalues: (copy) v_u_2
	p46:LoadOrCreateNumberValueParameter("InitialElevation", "NumberValue", nil)
	p46:LoadOrCreateNumberValueParameter("InitialDistance", "NumberValue", nil)
	local v47 = "ReferenceAzimuth"
	local v48 = "NumberValue"
	local v49
	if v_u_2 then
		v49 = p46.SetAndBoundsCheckAzimuthValues
	else
		v49 = p46.SetAndBoundsCheckAzimuthValue
	end
	p46:LoadOrCreateNumberValueParameter(v47, v48, v49)
	p46:LoadOrCreateNumberValueParameter("CWAzimuthTravel", "NumberValue", p46.SetAndBoundsCheckAzimuthValues)
	p46:LoadOrCreateNumberValueParameter("CCWAzimuthTravel", "NumberValue", p46.SetAndBoundsCheckAzimuthValues)
	p46:LoadOrCreateNumberValueParameter("MinElevation", "NumberValue", p46.SetAndBoundsCheckElevationValues)
	p46:LoadOrCreateNumberValueParameter("MaxElevation", "NumberValue", p46.SetAndBoundsCheckElevationValues)
	p46:LoadOrCreateNumberValueParameter("MinDistance", "NumberValue", p46.SetAndBoundsCheckDistanceValues)
	p46:LoadOrCreateNumberValueParameter("MaxDistance", "NumberValue", p46.SetAndBoundsCheckDistanceValues)
	p46:LoadOrCreateNumberValueParameter("UseAzimuthLimits", "BoolValue", p46.SetAndBoundsCheckAzimuthValues)
	local v50 = p46.externalProperties.ReferenceAzimuth
	p46.curAzimuthRad = math.rad(v50)
	local v51 = p46.externalProperties.InitialElevation
	p46.curElevationRad = math.rad(v51)
	p46.curDistance = p46.externalProperties.InitialDistance
	p46:SetAndBoundsCheckAzimuthValues()
	p46:SetAndBoundsCheckElevationValues()
	p46:SetAndBoundsCheckDistanceValues()
end
function v_u_7.GetModuleName(_) -- name: GetModuleName
	return "OrbitalCamera"
end
function v_u_7.SetInitialOrientation(p52, p53) -- name: SetInitialOrientation
	-- upvalues: (copy) v_u_3
	if p53 and p53.RootPart then
		local v54 = p53.RootPart
		assert(v54, "")
		local v55 = (p53.RootPart.CFrame.LookVector - Vector3.new(0, 0.23, 0)).Unit
		local v56 = v_u_3.GetAngleBetweenXZVectors(v55, p52:GetCameraLookVector())
		local v57 = p52:GetCameraLookVector().Y
		local v58 = math.asin(v57)
		local v59 = v55.Y
		local v60 = v58 - math.asin(v59)
		v_u_3.IsFinite(v56)
		v_u_3.IsFinite(v60)
	else
		warn("OrbitalCamera could not set initial orientation due to missing humanoid")
	end
end
function v_u_7.GetCameraToSubjectDistance(p61) -- name: GetCameraToSubjectDistance
	return p61.curDistance
end
function v_u_7.SetCameraToSubjectDistance(p62, p63) -- name: SetCameraToSubjectDistance
	-- upvalues: (copy) v_u_5
	if v_u_5.LocalPlayer then
		local v64 = p62.minDistance
		local v65 = p62.maxDistance
		p62.currentSubjectDistance = math.clamp(p63, v64, v65)
		local v66 = p62.currentSubjectDistance
		local v67 = p62.FIRST_PERSON_DISTANCE_THRESHOLD
		p62.currentSubjectDistance = math.max(v66, v67)
	end
	p62.inFirstPerson = false
	p62:UpdateMouseBehavior()
	return p62.currentSubjectDistance
end
function v_u_7.CalculateNewLookVector(p68, p69, p70) -- name: CalculateNewLookVector
	local v71 = p69 or p68:GetCameraLookVector()
	local v72 = v71.Y
	local v73 = math.asin(v72)
	local v74 = p70.Y
	local v75 = v73 - 1.3962634015954636
	local v76 = v73 - -1.3962634015954636
	local v77 = math.clamp(v74, v75, v76)
	local v78 = Vector2.new(p70.X, v77)
	local v79 = CFrame.new(Vector3.new(0, 0, 0), v71)
	return (CFrame.Angles(0, -v78.X, 0) * v79 * CFrame.Angles(-v78.Y, 0, 0)).LookVector
end
function v_u_7.Update(p80, p81) -- name: Update
	-- upvalues: (copy) v_u_4, (copy) v_u_5
	local v82 = tick()
	local v83 = v82 - p80.lastUpdate
	local v84 = v_u_4.getRotation(p81) ~= Vector2.new()
	local v85 = workspace.CurrentCamera
	local v86 = v85.CFrame
	local v87 = v85.Focus
	local v88 = v_u_5.LocalPlayer
	local v89
	if v85 then
		v89 = v85.CameraSubject
	else
		v89 = v85
	end
	local v90
	if v89 then
		v90 = v89:IsA("VehicleSeat")
	else
		v90 = v89
	end
	local v91
	if v89 then
		v91 = v89:IsA("SkateboardPlatform")
	else
		v91 = v89
	end
	if p80.lastUpdate == nil or v83 > 1 then
		p80.lastCameraTransform = nil
	end
	if v84 then
		p80.lastUserPanCamera = tick()
	end
	local v92 = p80:GetSubjectPosition()
	if v92 and (v88 and v85) then
		if p80.gamepadDollySpeedMultiplier ~= 1 then
			p80:SetCameraToSubjectDistance(p80.currentSubjectDistance * p80.gamepadDollySpeedMultiplier)
		end
		v87 = CFrame.new(v92)
		local v93 = v_u_4.getRotation(p81)
		p80.curAzimuthRad = p80.curAzimuthRad - v93.X
		if p80.useAzimuthLimits then
			local v94 = p80.curAzimuthRad
			local v95 = p80.minAzimuthAbsoluteRad
			local v96 = p80.maxAzimuthAbsoluteRad
			p80.curAzimuthRad = math.clamp(v94, v95, v96)
		else
			local v97
			if p80.curAzimuthRad == 0 then
				v97 = 0
			else
				local v98 = p80.curAzimuthRad
				local v99 = math.sign(v98)
				local v100 = p80.curAzimuthRad
				v97 = v99 * (math.abs(v100) % 6.283185307179586) or 0
			end
			p80.curAzimuthRad = v97
		end
		local v101 = p80.curElevationRad + v93.Y
		local v102 = p80.minElevationRad
		local v103 = p80.maxElevationRad
		p80.curElevationRad = math.clamp(v101, v102, v103)
		local v104 = v92 + p80.currentSubjectDistance * (CFrame.fromEulerAnglesYXZ(-p80.curElevationRad, p80.curAzimuthRad, 0) * Vector3.new(0, 0, 1))
		v86 = CFrame.new(v104, v92)
		p80.lastCameraTransform = v86
		p80.lastCameraFocus = v87
		if (v90 or v91) and v89:IsA("BasePart") then
			p80.lastSubjectCFrame = v89.CFrame
		else
			p80.lastSubjectCFrame = nil
		end
	end
	p80.lastUpdate = v82
	return v86, v87
end
return v_u_7

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.LegacyCamera
==================================================
Vector2.new()
require(script.Parent:WaitForChild("CameraUtils"))
local v_u_1 = require(script.Parent:WaitForChild("CameraInput"))
local v_u_2 = game:GetService("Players")
local v_u_3 = require(script.Parent:WaitForChild("BaseCamera"))
local v_u_4 = setmetatable({}, v_u_3)
v_u_4.__index = v_u_4
function v_u_4.new() -- name: new
	-- upvalues: (copy) v_u_3, (copy) v_u_4
	local v5 = v_u_3.new()
	local v6 = v_u_4
	local v7 = setmetatable(v5, v6)
	v7.cameraType = Enum.CameraType.Fixed
	v7.lastUpdate = tick()
	v7.lastDistanceToSubject = nil
	return v7
end
function v_u_4.GetModuleName(_) -- name: GetModuleName
	return "LegacyCamera"
end
function v_u_4.SetCameraToSubjectDistance(p8, p9) -- name: SetCameraToSubjectDistance
	-- upvalues: (copy) v_u_3
	return v_u_3.SetCameraToSubjectDistance(p8, p9)
end
function v_u_4.Update(p10, p11) -- name: Update
	-- upvalues: (copy) v_u_2, (copy) v_u_1
	if not p10.cameraType then
		return nil, nil
	end
	local v12 = tick()
	local v13 = v12 - p10.lastUpdate
	local v14 = workspace.CurrentCamera
	local v15 = v14.CFrame
	local v16 = v14.Focus
	local v17 = v_u_2.LocalPlayer
	local v18 = v_u_1.getRotation(p11)
	if p10.lastUpdate == nil or v13 > 1 then
		p10.lastDistanceToSubject = nil
	end
	local v19 = p10:GetSubjectPosition()
	if p10.cameraType == Enum.CameraType.Fixed then
		if v19 and (v17 and v14) then
			local v20 = p10:GetCameraToSubjectDistance()
			local v21 = p10:CalculateNewLookVectorFromArg(nil, v18)
			v16 = v14.Focus
			v15 = CFrame.new(v14.CFrame.p, v14.CFrame.p + v20 * v21)
		end
	elseif p10.cameraType == Enum.CameraType.Attach then
		local v22 = p10:GetSubjectCFrame()
		local v23 = v14.CFrame:ToEulerAnglesYXZ()
		local _, v24 = v22:ToEulerAnglesYXZ()
		local v25 = v23 - v18.Y
		local v26 = math.clamp(v25, -1.3962634015954636, 1.3962634015954636)
		v16 = CFrame.new(v22.p) * CFrame.fromEulerAnglesYXZ(v26, v24, 0)
		v15 = v16 * CFrame.new(0, 0, p10:StepZoom())
	else
		if p10.cameraType ~= Enum.CameraType.Watch then
			return v14.CFrame, v14.Focus
		end
		if v19 and (v17 and v14) then
			local v27 = nil
			if v19 == v14.CFrame.p then
				warn("Camera cannot watch subject in same position as itself")
				return v14.CFrame, v14.Focus
			end
			local v28 = p10:GetHumanoid()
			if v28 and v28.RootPart then
				local v29 = v19 - v14.CFrame.p
				v27 = v29.unit
				if p10.lastDistanceToSubject and p10.lastDistanceToSubject == p10:GetCameraToSubjectDistance() then
					p10:SetCameraToSubjectDistance(v29.magnitude)
				end
			end
			local v30 = p10:GetCameraToSubjectDistance()
			local v31 = p10:CalculateNewLookVectorFromArg(v27, v18)
			v16 = CFrame.new(v19)
			v15 = CFrame.new(v19 - v30 * v31, v19)
			p10.lastDistanceToSubject = v30
		end
	end
	p10.lastUpdate = v12
	return v15, v16
end
return v_u_4

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.VRVehicleCamera
==================================================
local v1, v2 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserVRVehicleCameraOrbital")
end)
local v_u_3 = v1 and v2
local v_u_4 = { 0, 30 }
local v_u_5 = require(script.Parent:WaitForChild("VRBaseCamera"))
local v_u_6 = require(script.Parent:WaitForChild("CameraUtils"))
local v_u_7 = require(script.Parent:WaitForChild("CameraInput"))
local v8 = game:GetService("Players")
local v_u_9 = game:GetService("RunService")
local v_u_10 = game:GetService("VRService")
local v_u_11 = game:GetService("Lighting")
local v_u_12 = v8.LocalPlayer
local v_u_13 = v_u_6.mapClamp
local v_u_14 = require(script.Parent:WaitForChild("VehicleCamera"):FindFirstChild("VehicleCameraConfig"))
local v_u_15 = RaycastParams.new()
v_u_15.FilterType = Enum.RaycastFilterType.Exclude
v_u_15.IgnoreWater = true
local function v_u_34(p16, p17, p18, p19) -- name: vrOccludeDisplace
	-- upvalues: (copy) v_u_12, (copy) v_u_15
	local v20 = p17.X
	local v21 = p17.Z
	local v22 = math.atan2(v20, v21)
	local v23 = CFrame.new(p16.Position + p17 * p18) * CFrame.Angles(0, v22, 0)
	local v24 = workspace.CurrentCamera
	if not v24 then
		return v23
	end
	local v25 = p16.Position
	local v26 = (v23.Position - v25) * Vector3.new(1, 0, 1)
	local v27 = v26.Magnitude
	if v27 < 0.5 then
		return v23
	end
	local v28 = { v24 }
	if p19 then
		table.insert(v28, p19)
	end
	local v29 = v_u_12
	if v29 then
		v29 = v_u_12.Character
	end
	if v29 then
		table.insert(v28, v29)
	end
	v_u_15.FilterDescendantsInstances = v28
	local v30 = v26.Unit
	local v31 = workspace:Raycast(v25, v26, v_u_15)
	if v31 and v31.Normal:Dot(v30) < 0 then
		local v32 = (v31.Position - v25).Magnitude - 0.5
		if v32 < v27 then
			local v33 = math.max(v32, 0.5)
			return CFrame.new(p16.Position + v30 * v33) * v23.Rotation
		end
	end
	return v23
end
local v_u_35 = OverlapParams.new()
v_u_35.FilterType = Enum.RaycastFilterType.Exclude
local function v_u_62(p36, p37, p38, p39) -- name: findObstructions
	-- upvalues: (copy) v_u_10, (copy) v_u_12, (copy) v_u_15, (copy) v_u_35
	local v40 = workspace.CurrentCamera
	if not v40 then
		return 0, {}
	end
	local v41 = p37.Position
	local v42 = v_u_10:GetUserCFrame(Enum.UserCFrame.Head)
	local v43 = v40.HeadScale
	local v44 = p36 * (CFrame.new(v42.Position * v43) * v42.Rotation)
	local v45 = v44.Position - v41
	local v46 = v45.Magnitude
	if v46 < 0.5 then
		return 0, {}
	end
	local v47 = { v40 }
	if p39 then
		table.insert(v47, p39)
	end
	local v48 = v_u_12
	if v48 then
		v48 = v_u_12.Character
	end
	if v48 then
		table.insert(v47, v48)
	end
	v_u_15.FilterDescendantsInstances = v47
	local v49 = workspace:Raycast(v41, v45, v_u_15)
	if v49 then
		local v50 = (v49.Position - v41).Magnitude
		if v50 < v46 then
			local v51 = v44.LookVector
			local v52 = (1 - -v45.Unit:Dot(v51)) / 0.1339745962155613
			local v53 = math.clamp(v52, 0, 1)
			local v54 = 1 - v50 / p38
			local v55 = math.max(v53, v54, 0.15)
			local v56 = v49.Position
			local v57 = v44.Position
			local v58 = (v56 + v57) / 2
			local v59 = (v57 - v56).Magnitude
			local v60 = Vector3.new(2, 2, v59)
			local v61 = CFrame.lookAt(v58, v57)
			v_u_35.FilterDescendantsInstances = v47
			return v55, workspace:GetPartBoundsInBox(v61, v60, v_u_35)
		end
	end
	return 0, {}
end
local v_u_63 = 0.016666666666666666
local v_u_64 = setmetatable({}, v_u_5)
v_u_64.__index = v_u_64
function v_u_64.new() -- name: new
	-- upvalues: (ref) v_u_3, (copy) v_u_5, (copy) v_u_64, (copy) v_u_9, (ref) v_u_63
	if not v_u_3 then
		return require(script.Parent:WaitForChild("VRVehicleCameraDeprecated")).new()
	end
	local v65 = v_u_5.new()
	local v66 = v_u_64
	local v67 = setmetatable(v65, v66)
	v67.skipOcclusion = true
	v67:Reset()
	if v67.thirdPersonOptionChanged then
		v67.thirdPersonOptionChanged:Disconnect()
		v67.thirdPersonOptionChanged = nil
	end
	v_u_9.Stepped:Connect(function(_, p68)
		-- upvalues: (ref) v_u_63
		v_u_63 = p68
	end)
	return v67
end
function v_u_64.Reset(p69) -- name: Reset
	-- upvalues: (copy) v_u_6, (copy) v_u_4
	local v70 = workspace.CurrentCamera
	local v71
	if v70 then
		v71 = v70.CameraSubject
	else
		v71 = v70
	end
	assert(v70, "VRVehicleCamera initialization error")
	assert(v71)
	assert(v71:IsA("VehicleSeat"))
	p69.lastOrbitalDir = nil
	p69.wasInFirstPerson = nil
	local v72 = v71:GetConnectedParts(true)
	table.insert(v72, v71)
	local v73, v74 = v_u_6.getLooseBoundingSphere(v72)
	p69.vehicleModel = v71:FindFirstAncestorOfClass("Model") or v71.Parent
	p69.assemblyRadius = math.max(v74, 5)
	p69.assemblyOffset = v71.CFrame:Inverse() * v73
	p69.gamepadZoomLevels = {}
	for _, v75 in v_u_4 do
		local v76 = p69.gamepadZoomLevels
		local v77 = v75 * p69.headScale * p69.assemblyRadius / 10
		table.insert(v76, v77)
	end
	p69.lastCameraFocus = nil
	if not p69:IsInFirstPerson() then
		p69:SetCameraToSubjectDistance(p69.gamepadZoomLevels[#p69.gamepadZoomLevels])
	end
	p69.needsReset = false
end
function v_u_64._getThirdPersonLocalOffset(p78) -- name: _getThirdPersonLocalOffset
	-- upvalues: (copy) v_u_14
	local v79 = p78.assemblyOffset
	local v80 = p78.assemblyRadius * v_u_14.verticalCenterOffset
	return v79 + Vector3.new(0, v80, 0)
end
function v_u_64._getFirstPersonLocalOffset(p81, p82) -- name: _getFirstPersonLocalOffset
	-- upvalues: (copy) v_u_12
	local v83 = v_u_12.Character
	if v83 and v83.Parent then
		local v84 = v83:FindFirstChild("Head")
		if v84 and v84:IsA("BasePart") then
			return p82:Inverse() * v84.Position
		end
	end
	return p81:_getThirdPersonLocalOffset()
end
function v_u_64._vrOccludeVignette(p85, p86, p87, p88) -- name: _vrOccludeVignette
	-- upvalues: (copy) v_u_62, (copy) v_u_11, (copy) v_u_12
	local v89 = p87.X
	local v90 = p87.Z
	local v91 = math.atan2(v89, v90)
	local v92 = CFrame.new(p86.Position + p87 * p88) * CFrame.Angles(0, v91, 0)
	local v93, v94 = v_u_62(v92, p86, p88, p85.vehicleModel)
	local v95 = v_u_11:FindFirstChild("VRFade")
	if not v95 then
		v95 = Instance.new("ColorCorrectionEffect")
		v95.Name = "VRFade"
		v95.Parent = v_u_11
	end
	v95.Brightness = -v93
	if p85.lastOccludedParts then
		for _, v96 in p85.lastOccludedParts do
			v96.LocalTransparencyModifier = 0
		end
	end
	if #v94 > 0 then
		for _, v97 in v94 do
			v97.LocalTransparencyModifier = 1
		end
		p85:StartVREdgeBlur(v_u_12, true)
	end
	p85.lastOccludedParts = v94
	return v92
end
function v_u_64.Update(p98) -- name: Update
	-- upvalues: (ref) v_u_63, (copy) v_u_12
	local v99 = v_u_63
	v_u_63 = 0
	p98:UpdateFadeFromBlack(v99)
	p98:UpdateEdgeBlur(v_u_12, v99)
	local v100, v101 = p98:_updateStepRotation(v99)
	return v100, v101
end
function v_u_64._updateStepRotation(p102, p103) -- name: _updateStepRotation
	-- upvalues: (copy) v_u_13, (copy) v_u_7, (copy) v_u_14, (copy) v_u_34
	local v104 = p102:GetSubjectCFrame()
	local v105 = p102:GetCameraToSubjectDistance()
	local v106 = v_u_13(v105, 0.5, p102.assemblyRadius, 1, 0)
	local v107 = v104 * p102:_getThirdPersonLocalOffset():Lerp(p102:_getFirstPersonLocalOffset(v104), v106)
	local v108 = CFrame.new
	local v109 = p102:GetCameraHeight()
	local v110 = v108(v107 + Vector3.new(0, v109, 0))
	if p102.needsReset or p102.recentered then
		p102.lastOrbitalDir = nil
		p102.needsReset = false
		p102.recentered = false
	end
	local v111 = p102.lastOrbitalDir
	if not v111 then
		v111 = (v104.LookVector * Vector3.new(-1, 0, -1)).Unit
		p102:StartFadeFromBlack()
	end
	local v112 = (p102:GetSubjectVelocity() * Vector3.new(1, 0, 1)).Magnitude > 2
	if v112 then
		v_u_7.getRotation(p103)
	else
		local v113 = p102:getRotation(p103)
		if math.abs(v113) > 0 then
			v111 = (CFrame.Angles(0, -v113, 0) * CFrame.new(v111)).Position.Unit
			p102.lastRotateTime = os.clock()
		end
	end
	local v114
	if p102:IsInFirstPerson() then
		if not p102.wasInFirstPerson or v112 then
			v111 = (v104.LookVector * Vector3.new(-1, 0, -1)).Unit
			p102.wasInFirstPerson = true
		end
		local v115 = -v104.LookVector.X
		local v116 = -v104.LookVector.Z
		local v117 = math.atan2(v115, v116)
		if p102.lastVehicleYaw then
			local v118 = (v117 - p102.lastVehicleYaw + 3.141592653589793) % 6.283185307179586 - 3.141592653589793
			if math.abs(v118) > 0.001 then
				v111 = (CFrame.Angles(0, v118, 0) * CFrame.new(v111)).Position.Unit
			end
		end
		p102.lastVehicleYaw = v117
		local v119 = v111.X
		local v120 = v111.Z
		local v121 = math.atan2(v119, v120)
		v114 = CFrame.new(v110.Position + v111 * v105) * CFrame.Angles(0, v121, 0)
	else
		p102.wasInFirstPerson = false
		p102.lastVehicleYaw = nil
		local v122 = p102.lastRotateTime
		if v122 then
			v122 = os.clock() - p102.lastRotateTime < v_u_14.autocorrectDelay
		end
		if v112 and not v122 then
			local v123 = (v104.LookVector * Vector3.new(-1, 0, -1)).Unit
			local v124 = v111:Dot(v123)
			local v125 = math.clamp(v124, -1, 1)
			local v126 = math.acos(v125)
			local v127 = p102:GetSubjectRotVelocity()
			local v128 = v104.YVector:Dot(v127)
			local v129 = math.abs(v128)
			local v130 = 0.01 + v126 / 3.141592653589793 * 0.05 + v129 * 0.02
			v111 = v111:Lerp(v123, (math.min(v130, 0.15)))
		end
		v114 = v_u_34(v110, v111, v105, p102.vehicleModel)
	end
	p102.lastOrbitalDir = v111
	return v114, v114 * CFrame.new(0, 0, -v105)
end
return v_u_64

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.VRCameraTeleportDetector
==================================================
local v_u_5 = {
	["JUMP_STUDS"] = 4,
	["SETTLED_STUDS"] = 1,
	["DEBOUNCE_SECONDS"] = 0.25,
	["shouldRecenter"] = function(p1, p2, p3, p4) -- name: shouldRecenter
		-- upvalues: (copy) v_u_5
		if p2 <= v_u_5.JUMP_STUDS then
			return false
		elseif p1 == nil or v_u_5.SETTLED_STUDS > p1 then
			return p3 == nil or p4 - p3 >= v_u_5.DEBOUNCE_SECONDS
		else
			return false
		end
	end
}
return v_u_5

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.ClassicCamera
==================================================
Vector2.new(0, 0)
local v_u_1 = 0
local v_u_2 = CFrame.fromOrientation(-0.2617993877991494, 0, 0)
local v3 = script.Parent.Parent:WaitForChild("CommonUtils")
local v_u_4 = require(v3:WaitForChild("FlagUtil")).getUserFlag("UserFixCameraFPError")
local v_u_5 = game:GetService("Players")
local v_u_6 = require(script.Parent:WaitForChild("CameraInput"))
local v_u_7 = require(script.Parent:WaitForChild("CameraUtils"))
local v_u_8 = require(script.Parent:WaitForChild("BaseCamera"))
local v_u_9 = setmetatable({}, v_u_8)
v_u_9.__index = v_u_9
function v_u_9.new() -- name: new
	-- upvalues: (copy) v_u_8, (copy) v_u_9, (copy) v_u_7
	local v10 = v_u_8.new()
	local v11 = v_u_9
	local v12 = setmetatable(v10, v11)
	v12.isFollowCamera = false
	v12.isCameraToggle = false
	v12.lastUpdate = tick()
	v12.cameraToggleSpring = v_u_7.Spring.new(5, 0)
	return v12
end
function v_u_9.GetCameraToggleOffset(p13, p14) -- name: GetCameraToggleOffset
	-- upvalues: (copy) v_u_6, (copy) v_u_7
	if not p13.isCameraToggle then
		return Vector3.new()
	end
	local v15 = p13.currentSubjectDistance
	if v_u_6.getTogglePan() then
		local v16 = p13.cameraToggleSpring
		local v17 = v_u_7.map(v15, 0.5, p13.FIRST_PERSON_DISTANCE_THRESHOLD, 0, 1)
		v16.goal = math.clamp(v17, 0, 1)
	else
		p13.cameraToggleSpring.goal = 0
	end
	local v18 = v_u_7.map(v15, 0.5, 64, 0, 1)
	local v19 = math.clamp(v18, 0, 1) + 1
	local v20 = p13.cameraToggleSpring:step(p14) * v19
	return Vector3.new(0, v20, 0)
end
function v_u_9.SetCameraMovementMode(p21, p22) -- name: SetCameraMovementMode
	-- upvalues: (copy) v_u_8
	v_u_8.SetCameraMovementMode(p21, p22)
	p21.isFollowCamera = p22 == Enum.ComputerCameraMovementMode.Follow
	p21.isCameraToggle = p22 == Enum.ComputerCameraMovementMode.CameraToggle
end
function v_u_9.Update(p23, p24) -- name: Update
	-- upvalues: (copy) v_u_2, (copy) v_u_5, (copy) v_u_6, (ref) v_u_1, (copy) v_u_7, (copy) v_u_4
	local v25 = tick()
	local v26 = workspace.CurrentCamera
	local v27 = v26.CFrame
	local v28 = v26.Focus
	local v29
	if p23.resetCameraAngle then
		local v30 = p23:GetHumanoidRootPart()
		if v30 then
			v29 = (v30.CFrame * v_u_2).lookVector
		else
			v29 = v_u_2.lookVector
		end
		p23.resetCameraAngle = false
	else
		v29 = nil
	end
	local v31 = v_u_5.LocalPlayer
	local v32 = p23:GetHumanoid()
	local v33 = v26.CameraSubject
	local v34
	if v33 then
		v34 = v33:IsA("VehicleSeat")
	else
		v34 = v33
	end
	local v35
	if v33 then
		v35 = v33:IsA("SkateboardPlatform")
	else
		v35 = v33
	end
	local v36
	if v32 then
		v36 = v32:GetState() == Enum.HumanoidStateType.Climbing
	else
		v36 = v32
	end
	if p23.lastUpdate == nil or p24 > 1 then
		p23.lastCameraTransform = nil
	end
	local v37 = v_u_6.getRotation(p24)
	p23:StepZoom()
	local v38 = p23:GetCameraHeight()
	if v37 ~= Vector2.new() then
		v_u_1 = 0
		p23.lastUserPanCamera = tick()
	end
	local v39 = v25 - p23.lastUserPanCamera < 2
	local v40 = p23:GetSubjectPosition()
	if v40 and (v31 and v26) then
		local v41 = p23:GetCameraToSubjectDistance()
		local v42 = v41 < 0.5 and 0.5 or v41
		if p23:GetIsMouseLocked() and not p23:IsInFirstPerson() then
			local v43 = p23:CalculateNewLookCFrameFromArg(v29, v37)
			local v44 = p23:GetMouseLockOffset()
			if v32 then
				v44 = v44 + v32.CameraOffset
			end
			local v45 = v44.X * v43.RightVector + v44.Y * v43.UpVector + v44.Z * v43.LookVector
			if v_u_7.IsFiniteVector3(v45) then
				v40 = v40 + v45
			end
		elseif v37 == Vector2.new() and p23.lastCameraTransform then
			local v46 = p23:IsInFirstPerson()
			if (v34 or (v35 or p23.isFollowCamera and v36)) and (p23.lastUpdate and (v32 and v32.Torso)) then
				if v46 then
					if p23.lastSubjectCFrame and (v34 or v35) and v33:IsA("BasePart") then
						local v47 = -v_u_7.GetAngleBetweenXZVectors(p23.lastSubjectCFrame.lookVector, v33.CFrame.lookVector)
						if v_u_7.IsFinite(v47) then
							v37 = v37 + Vector2.new(v47, 0)
						end
						v_u_1 = 0
					end
				elseif not v39 then
					local v48 = v32.Torso.CFrame.lookVector
					local v49 = v_u_1 + 3.839724354387525 * p24
					v_u_1 = math.clamp(v49, 0, 4.363323129985824)
					local v50 = v_u_1 * p24
					local v51 = math.clamp(v50, 0, 1)
					local v52 = p23:IsInFirstPerson() and not (p23.isFollowCamera and p23.isClimbing) and 1 or v51
					local v53 = v_u_7.GetAngleBetweenXZVectors(v48, p23:GetCameraLookVector())
					if v_u_7.IsFinite(v53) and math.abs(v53) > 0.0001 then
						v37 = v37 + Vector2.new(v53 * v52, 0)
					end
				end
			elseif p23.isFollowCamera and not (v46 or v39) then
				local v54 = -(p23.lastCameraTransform.p - v40)
				local v55 = v_u_7.GetAngleBetweenXZVectors(v54, p23:GetCameraLookVector())
				if v_u_7.IsFinite(v55) and (math.abs(v55) > 0.0001 and math.abs(v55) > 0.4 * p24) then
					v37 = v37 + Vector2.new(v55, 0)
				end
			end
		end
		local v56, v57
		if p23.isFollowCamera then
			local v58 = p23:CalculateNewLookVectorFromArg(v29, v37)
			v56 = CFrame.new(v40)
			if v_u_4 then
				v57 = CFrame.lookAlong(v56.p - v42 * v58, v58)
			else
				v57 = CFrame.new(v56.p - v42 * v58, v56.p) + Vector3.new(0, v38, 0)
			end
		else
			v56 = CFrame.new(v40)
			local v59 = v56.p
			local v60 = p23:CalculateNewLookVectorFromArg(v29, v37)
			if v_u_4 then
				v57 = CFrame.lookAlong(v59 - v42 * v60, v60)
			else
				v57 = CFrame.new(v59 - v42 * v60, v59)
			end
		end
		local v61 = p23:GetCameraToggleOffset(p24)
		v28 = v56 + v61
		v27 = v57 + v61
		p23.lastCameraTransform = v27
		p23.lastCameraFocus = v28
		if (v34 or v35) and v33:IsA("BasePart") then
			p23.lastSubjectCFrame = v33.CFrame
		else
			p23.lastSubjectCFrame = nil
		end
	end
	p23.lastUpdate = v25
	return v27, v28
end
return v_u_9

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.CameraUtils
==================================================
local v_u_1 = game:GetService("Players")
local v_u_2 = game:GetService("UserInputService")
local v_u_3 = UserSettings():GetService("UserGameSettings")
local v_u_4 = {}
local v_u_5 = {}
v_u_5.__index = v_u_5
function v_u_5.new(p6, p7) -- name: new
	-- upvalues: (copy) v_u_5
	local v8 = v_u_5
	return setmetatable({
		["freq"] = nil,
		["goal"] = nil,
		["pos"] = nil,
		["vel"] = 0,
		["freq"] = p6,
		["goal"] = p7,
		["pos"] = p7
	}, v8)
end
function v_u_5.step(p9, p10) -- name: step
	local v11 = p9.freq * 2 * 3.141592653589793
	local v12 = p9.goal
	local v13 = p9.pos
	local v14 = p9.vel
	local v15 = v13 - v12
	local v16 = -v11 * p10
	local v17 = math.exp(v16)
	local v18 = (v15 * (v11 * p10 + 1) + v14 * p10) * v17 + v12
	local v19 = (v14 * (1 - v11 * p10) - v15 * (v11 * v11 * p10)) * v17
	p9.pos = v18
	p9.vel = v19
	return v18
end
v_u_4.Spring = v_u_5
function v_u_4.map(p20, p21, p22, p23, p24) -- name: map
	return (p20 - p21) * (p24 - p23) / (p22 - p21) + p23
end
function v_u_4.mapClamp(p25, p26, p27, p28, p29) -- name: mapClamp
	local v30 = (p25 - p26) * (p29 - p28) / (p27 - p26) + p28
	local v31 = math.min(p28, p29)
	local v32 = math.max(p28, p29)
	return math.clamp(v30, v31, v32)
end
function v_u_4.getLooseBoundingSphere(p33) -- name: getLooseBoundingSphere
	local v34 = table.create(#p33)
	for v35, v36 in pairs(p33) do
		v34[v35] = v36.Position
	end
	local v37 = v34[1]
	local v38 = v37
	local v39 = 0
	for _, v40 in ipairs(v34) do
		local v41 = (v40 - v37).Magnitude
		if v39 < v41 then
			v38 = v40
			v39 = v41
		end
	end
	local v42 = v38
	local v43 = 0
	for _, v44 in ipairs(v34) do
		local v45 = (v44 - v38).Magnitude
		if v43 < v45 then
			v42 = v44
			v43 = v45
		end
	end
	local v46 = (v38 + v42) * 0.5
	local v47 = (v38 - v42).Magnitude * 0.5
	for _, v48 in ipairs(v34) do
		local v49 = (v48 - v46).Magnitude
		if v47 < v49 then
			v46 = v46 + (v49 - v47) * 0.5 * (v48 - v46).Unit
			v47 = (v49 + v47) * 0.5
		end
	end
	return v46, v47
end
function v_u_4.sanitizeAngle(p50) -- name: sanitizeAngle
	return (p50 + 3.141592653589793) % 6.283185307179586 - 3.141592653589793
end
function v_u_4.Round(p51, p52) -- name: Round
	local v53 = 10 ^ p52
	local v54 = p51 * v53 + 0.5
	return math.floor(v54) / v53
end
function v_u_4.IsFinite(p55) -- name: IsFinite
	local v56
	if p55 == p55 and p55 ~= (1 / 0) then
		v56 = p55 ~= (-1 / 0)
	else
		v56 = false
	end
	return v56
end
function v_u_4.IsFiniteVector3(p57) -- name: IsFiniteVector3
	-- upvalues: (copy) v_u_4
	local v58 = v_u_4.IsFinite(p57.X) and v_u_4.IsFinite(p57.Y)
	if v58 then
		v58 = v_u_4.IsFinite(p57.Z)
	end
	return v58
end
function v_u_4.GetAngleBetweenXZVectors(p59, p60) -- name: GetAngleBetweenXZVectors
	local v61 = p60.X * p59.Z - p60.Z * p59.X
	local v62 = p60.X * p59.X + p60.Z * p59.Z
	return math.atan2(v61, v62)
end
function v_u_4.RotateVectorByAngleAndRound(p63, p64, p65) -- name: RotateVectorByAngleAndRound
	if p63.Magnitude <= 0 then
		return 0
	end
	local v66 = p63.Unit
	local v67 = v66.Z
	local v68 = v66.X
	local v69 = math.atan2(v67, v68)
	local v70 = v66.Z
	local v71 = v66.X
	local v72 = (math.atan2(v70, v71) + p64) / p65 + 0.5
	return math.floor(v72) * p65 - v69
end
function v_u_4.GamepadLinearToCurve(p73) -- name: GamepadLinearToCurve
	local v74 = Vector2.new
	local v75 = p73.X
	local v76 = v75 < 0 and -1 or 1
	local v77 = math.abs(v75)
	local v78 = (math.abs(v77) * 2 - 1) * 1.1 - 0.1
	local v79 = math.clamp(v78, -1, 1)
	local v80
	if v79 >= 0 then
		v80 = v79 * 0.35 / (0.35 - v79 + 1)
	else
		v80 = -(-v79 * 0.8 / (v79 + 0.8 + 1))
	end
	local v81 = (v80 / 2 + 0.5) * v76
	local v82 = math.clamp(v81, -1, 1)
	local v83 = p73.Y
	local v84 = v83 < 0 and -1 or 1
	local v85 = math.abs(v83)
	local v86 = (math.abs(v85) * 2 - 1) * 1.1 - 0.1
	local v87 = math.clamp(v86, -1, 1)
	local v88
	if v87 >= 0 then
		v88 = v87 * 0.35 / (0.35 - v87 + 1)
	else
		v88 = -(-v87 * 0.8 / (v87 + 0.8 + 1))
	end
	local v89 = (v88 / 2 + 0.5) * v84
	return v74(v82, (math.clamp(v89, -1, 1)))
end
function v_u_4.ConvertCameraModeEnumToStandard(p90) -- name: ConvertCameraModeEnumToStandard
	if p90 == Enum.TouchCameraMovementMode.Default then
		return Enum.ComputerCameraMovementMode.Follow
	elseif p90 == Enum.ComputerCameraMovementMode.Default then
		return Enum.ComputerCameraMovementMode.Classic
	elseif p90 == Enum.TouchCameraMovementMode.Classic or (p90 == Enum.DevTouchCameraMovementMode.Classic or (p90 == Enum.DevComputerCameraMovementMode.Classic or p90 == Enum.ComputerCameraMovementMode.Classic)) then
		return Enum.ComputerCameraMovementMode.Classic
	elseif p90 == Enum.TouchCameraMovementMode.Follow or (p90 == Enum.DevTouchCameraMovementMode.Follow or (p90 == Enum.DevComputerCameraMovementMode.Follow or p90 == Enum.ComputerCameraMovementMode.Follow)) then
		return Enum.ComputerCameraMovementMode.Follow
	elseif p90 == Enum.TouchCameraMovementMode.Orbital or (p90 == Enum.DevTouchCameraMovementMode.Orbital or (p90 == Enum.DevComputerCameraMovementMode.Orbital or p90 == Enum.ComputerCameraMovementMode.Orbital)) then
		return Enum.ComputerCameraMovementMode.Orbital
	elseif p90 == Enum.ComputerCameraMovementMode.CameraToggle or p90 == Enum.DevComputerCameraMovementMode.CameraToggle then
		return Enum.ComputerCameraMovementMode.CameraToggle
	elseif p90 == Enum.DevTouchCameraMovementMode.UserChoice or p90 == Enum.DevComputerCameraMovementMode.UserChoice then
		return Enum.DevComputerCameraMovementMode.UserChoice
	else
		return Enum.ComputerCameraMovementMode.Classic
	end
end
local v_u_91 = ""
local v_u_92 = nil
function v_u_4.setMouseIconOverride(p93) -- name: setMouseIconOverride
	-- upvalues: (copy) v_u_1, (ref) v_u_92, (ref) v_u_91
	local v94 = v_u_1.LocalPlayer
	if not v94 then
		v_u_1:GetPropertyChangedSignal("LocalPlayer"):Wait()
		v94 = v_u_1.LocalPlayer
	end
	assert(v94)
	local v95 = v94:GetMouse()
	if v95.Icon ~= v_u_92 then
		v_u_91 = v95.Icon
	end
	v95.Icon = p93
	v_u_92 = p93
end
function v_u_4.restoreMouseIcon() -- name: restoreMouseIcon
	-- upvalues: (copy) v_u_1, (ref) v_u_92, (ref) v_u_91
	local v96 = v_u_1.LocalPlayer
	if not v96 then
		v_u_1:GetPropertyChangedSignal("LocalPlayer"):Wait()
		v96 = v_u_1.LocalPlayer
	end
	assert(v96)
	local v97 = v96:GetMouse()
	if v97.Icon == v_u_92 then
		v97.Icon = v_u_91
	end
	v_u_92 = nil
end
local v_u_98 = Enum.MouseBehavior.Default
local v_u_99 = nil
function v_u_4.setMouseBehaviorOverride(p100) -- name: setMouseBehaviorOverride
	-- upvalues: (copy) v_u_2, (ref) v_u_99, (ref) v_u_98
	if v_u_2.MouseBehavior ~= v_u_99 then
		v_u_98 = v_u_2.MouseBehavior
	end
	v_u_2.MouseBehavior = p100
	v_u_99 = p100
end
function v_u_4.restoreMouseBehavior() -- name: restoreMouseBehavior
	-- upvalues: (copy) v_u_2, (ref) v_u_99, (ref) v_u_98
	if v_u_2.MouseBehavior == v_u_99 then
		v_u_2.MouseBehavior = v_u_98
	end
	v_u_99 = nil
end
local v_u_101 = Enum.RotationType.MovementRelative
local v_u_102 = nil
function v_u_4.setRotationTypeOverride(p103) -- name: setRotationTypeOverride
	-- upvalues: (copy) v_u_3, (ref) v_u_102, (ref) v_u_101
	if v_u_3.RotationType ~= v_u_102 then
		v_u_101 = v_u_3.RotationType
	end
	v_u_3.RotationType = p103
	v_u_102 = p103
end
function v_u_4.restoreRotationType() -- name: restoreRotationType
	-- upvalues: (copy) v_u_3, (ref) v_u_102, (ref) v_u_101
	if v_u_3.RotationType == v_u_102 then
		v_u_3.RotationType = v_u_101
	end
	v_u_102 = nil
end
return v_u_4

==================================================
-- Players.turbobrutti.PlayerScripts.PlayerModule.CameraModule.TransparencyController
==================================================
local v_u_1 = game:GetService("VRService")
local v_u_2 = {
	"BasePart",
	"Decal",
	"Beam",
	"ParticleEmitter",
	"Trail",
	"Fire",
	"Smoke",
	"Sparkles",
	"Explosion"
}
local v_u_3 = require(script.Parent:WaitForChild("CameraUtils"))
local v4, v5 = pcall(function()
	return UserSettings():IsUserFeatureEnabled("UserHideCharacterParticlesInFirstPerson")
end)
local v_u_6 = v4 and v5
local v_u_7 = {}
v_u_7.__index = v_u_7
function v_u_7.new() -- name: new
	-- upvalues: (copy) v_u_7
	local v8 = v_u_7
	local v9 = setmetatable({}, v8)
	v9.transparencyDirty = false
	v9.enabled = false
	v9.lastTransparency = nil
	v9.descendantAddedConn = nil
	v9.descendantRemovingConn = nil
	v9.toolDescendantAddedConns = {}
	v9.toolDescendantRemovingConns = {}
	v9.cachedParts = {}
	return v9
end
function v_u_7.HasToolAncestor(p10, p11) -- name: HasToolAncestor
	if p11.Parent == nil then
		return false
	end
	local v12 = p11.Parent
	assert(v12, "")
	return p11.Parent:IsA("Tool") or p10:HasToolAncestor(p11.Parent)
end
function v_u_7.IsValidPartToModify(p13, p14) -- name: IsValidPartToModify
	-- upvalues: (ref) v_u_6, (copy) v_u_2
	if v_u_6 then
		for _, v15 in v_u_2 do
			if p14:IsA(v15) then
				return not p13:HasToolAncestor(p14)
			end
		end
	elseif p14:IsA("BasePart") or p14:IsA("Decal") then
		return not p13:HasToolAncestor(p14)
	end
	return false
end
function v_u_7.CachePartsRecursive(p16, p17) -- name: CachePartsRecursive
	if p17 then
		if p16:IsValidPartToModify(p17) then
			p16.cachedParts[p17] = true
			p16.transparencyDirty = true
		end
		for _, v18 in pairs(p17:GetChildren()) do
			p16:CachePartsRecursive(v18)
		end
	end
end
function v_u_7.TeardownTransparency(p19) -- name: TeardownTransparency
	for v20, _ in pairs(p19.cachedParts) do
		v20.LocalTransparencyModifier = 0
	end
	p19.cachedParts = {}
	p19.transparencyDirty = true
	p19.lastTransparency = nil
	if p19.descendantAddedConn then
		p19.descendantAddedConn:disconnect()
		p19.descendantAddedConn = nil
	end
	if p19.descendantRemovingConn then
		p19.descendantRemovingConn:disconnect()
		p19.descendantRemovingConn = nil
	end
	for v21, v22 in pairs(p19.toolDescendantAddedConns) do
		v22:Disconnect()
		p19.toolDescendantAddedConns[v21] = nil
	end
	for v23, v24 in pairs(p19.toolDescendantRemovingConns) do
		v24:Disconnect()
		p19.toolDescendantRemovingConns[v23] = nil
	end
end
function v_u_7.SetupTransparency(p_u_25, p_u_26) -- name: SetupTransparency
	p_u_25:TeardownTransparency()
	if p_u_25.descendantAddedConn then
		p_u_25.descendantAddedConn:disconnect()
	end
	p_u_25.descendantAddedConn = p_u_26.DescendantAdded:Connect(function(p27)
		-- upvalues: (copy) p_u_25, (copy) p_u_26
		if p_u_25:IsValidPartToModify(p27) then
			p_u_25.cachedParts[p27] = true
			p_u_25.transparencyDirty = true
		elseif p27:IsA("Tool") then
			if p_u_25.toolDescendantAddedConns[p27] then
				p_u_25.toolDescendantAddedConns[p27]:Disconnect()
			end
			p_u_25.toolDescendantAddedConns[p27] = p27.DescendantAdded:Connect(function(p28)
				-- upvalues: (ref) p_u_25
				p_u_25.cachedParts[p28] = nil
				if p28:IsA("BasePart") or p28:IsA("Decal") then
					p28.LocalTransparencyModifier = 0
				end
			end)
			if p_u_25.toolDescendantRemovingConns[p27] then
				p_u_25.toolDescendantRemovingConns[p27]:disconnect()
			end
			p_u_25.toolDescendantRemovingConns[p27] = p27.DescendantRemoving:Connect(function(p29)
				-- upvalues: (ref) p_u_26, (ref) p_u_25
				wait()
				if p_u_26 and (p29 and (p29:IsDescendantOf(p_u_26) and p_u_25:IsValidPartToModify(p29))) then
					p_u_25.cachedParts[p29] = true
					p_u_25.transparencyDirty = true
				end
			end)
		end
	end)
	if p_u_25.descendantRemovingConn then
		p_u_25.descendantRemovingConn:disconnect()
	end
	p_u_25.descendantRemovingConn = p_u_26.DescendantRemoving:connect(function(p30)
		-- upvalues: (copy) p_u_25
		if p_u_25.cachedParts[p30] then
			p_u_25.cachedParts[p30] = nil
			p30.LocalTransparencyModifier = 0
		end
	end)
	p_u_25:CachePartsRecursive(p_u_26)
end
function v_u_7.Enable(p31, p32) -- name: Enable
	if p31.enabled ~= p32 then
		p31.enabled = p32
	end
end
function v_u_7.SetSubject(p33, p34) -- name: SetSubject
	local v35
	if p34 and p34:IsA("Humanoid") then
		v35 = p34.Parent
	else
		v35 = nil
	end
	if p34 and (p34:IsA("VehicleSeat") and p34.Occupant) then
		v35 = p34.Occupant.Parent
	end
	if v35 then
		p33:SetupTransparency(v35)
	else
		p33:TeardownTransparency()
	end
end
function v_u_7.Update(p36, p37) -- name: Update
	-- upvalues: (copy) v_u_3, (copy) v_u_1
	local v38 = workspace.CurrentCamera
	if v38 and p36.enabled then
		local v39 = (v38.Focus.p - v38.CoordinateFrame.p).magnitude
		local v40 = v39 < 2 and 1 - (v39 - 0.5) / 1.5 or 0
		local v41 = v40 < 0.5 and 0 or v40
		if p36.lastTransparency and (v41 < 1 and p36.lastTransparency < 0.95) then
			local v42 = v41 - p36.lastTransparency
			local v43 = 2.8 * p37
			local v44 = -v43
			local v45 = math.clamp(v42, v44, v43)
			v41 = p36.lastTransparency + v45
		else
			p36.transparencyDirty = true
		end
		local v46 = v_u_3.Round(v41, 2)
		local v47 = math.clamp(v46, 0, 1)
		if p36.transparencyDirty or p36.lastTransparency ~= v47 then
			for v48, _ in pairs(p36.cachedParts) do
				if v_u_1.VREnabled and v_u_1.AvatarGestures then
					local v49 = {
						[Enum.AccessoryType.Hat] = true,
						[Enum.AccessoryType.Hair] = true,
						[Enum.AccessoryType.Face] = true,
						[Enum.AccessoryType.Eyebrow] = true,
						[Enum.AccessoryType.Eyelash] = true
					}
					if v48.Parent:IsA("Accessory") and v49[v48.Parent.AccessoryType] or v48.Name == "Head" then
						v48.LocalTransparencyModifier = v47
					else
						v48.LocalTransparencyModifier = 0
					end
				else
					v48.LocalTransparencyModifier = v47
				end
			end
			p36.transparencyDirty = false
			p36.lastTransparency = v47
		end
	end
end
return v_u_7
