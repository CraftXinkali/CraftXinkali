local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Thanatos Universal GUI HUB /// " ..game.Name, "BloodTheme")

-- Main
local Main = Window:NewTab("Main")
local MainSection = Main:NewSection("Player")


MainSection:NewToggle("Super Human", "Toggles SuperHuman Mode", function(state)
    if state then
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 120
		game.Players.LocalPlayer.Character.Humanoid.JumpPower = 120
    	game.Players.LocalPlayer.Character.Humanoid.Health = 99999999
    else
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
		game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
		game.Players.LocalPlayer.Character.Humanoid.Health = 100
    end
end)


MainSection:NewSlider("WalkSpeed", "Changes Player Walkspeed", 500, 0, function(s)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)

MainSection:NewSlider("JumpPower", "Changes Player JumpPower", 500, 0, function(j)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = j
end)

MainSection:NewButton("Reset", "Resets Movement", function()
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
	game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
end)

MainSection:NewButton("Suicide", "Are you really gonna make me explain?", function()
	game.Players.LocalPlayer.Character.Humanoid.Health = 0
end)

-- Misc
local Misc = Window:NewTab("Misc")
local MiscSection = Misc:NewSection("Misc")

MiscSection:NewKeybind("GUI TOGGLE BUTTON", "Toggle GUI Button", Enum.KeyCode.RightControl, function()
	Library:ToggleUI()
end)

--- OtherScripts

local OtherScripts = Window:NewTab("Other")
local OtherSection = OtherScripts:NewSection("Scripts")


OtherSection:NewButton("Reviz Admin", "Reviz Admin Script", function()
    -- Creator: illremember#3799

-- Credits to infinite yield, harkinian, dex creators

prefix = ";"
wait(0.3)
Commands = {
	'[-] cmdbar is shown when ; is pressed.',
	'[1] kill [plr] -- You need a tool! Will kill the player, use rkill to kill you and player',
	'[2] bring [plr] -- You need a tool! Will bring player to you',
	'[3] spin [plr] -- You need a tool! Makes you and the player spin crazy',
	'[4] unspin -- Use after using spin cmd and dying, so you stop loop teleporting',
	'[5] attach [plr] -- You need a tool! Attaches you to player',
	'[6] unattach [plr] -- Attempts to unattach you from a player',
	'[7] follow [plr] -- Makes you follow behind the player',
	'[8] unfollow',
	'[9] freefall [plr] -- You need a tool! Teleports you and the player up into the air',
	'[10] trail [plr] -- The opposite of follow, you stay infront of player',
	'[11] untrail',
	'[12] orbit [plr] -- Makes you orbit the player',
	'[13] unorbit',
	'[14] fling [plr] -- Makes you fling the player',
	'[15] unfling',
	'[16] fecheck -- Checks if the game is FE or not',
	'[17] void [plr] -- Teleports player to the void',
	'[18] noclip -- Gives you noclip to walk through walls',
	'[19] clip -- Removes noclip',
	'[20] speed [num]/ws [num] -- Changes how fast you walk 16 is default',
	'[21] jumppower [num]/jp [num] -- Changes how high you jump 50 is default',
	'[22] hipheight [num]/hh [num] -- Changes how high you float 0 is default',
	'[23] default -- Changes your speed, jumppower and hipheight to default values',
	'[24] annoy [plr] -- Loop teleports you to the player',
	'[25] unannoy',
	'[26] headwalk [plr] -- Loop teleports you to the player head',
	'[27] unheadwalk',
	'[28] nolimbs -- Removes your arms and legs',
	'[29] god -- Gives you FE Godmode',
	'[30] drophats -- Drops your accessories',
	'[31] droptool -- Drops any tool you have equipped',
	'[32] loopdhats -- Loop drops your accessories',
	'[33] unloopdhats',
	'[34] loopdtool -- Loop drops any tools you have equipped',
	'[35] unloopdtool',
	'[36] invisible -- Gives you invisibility CREDIT TO TIMELESS',
	'[37] view [plr] -- Changes your camera to the player character',
	'[38] unview',
	'[39] goto [plr] -- Teleports you to player',
	'[40] fly -- Allows you to fly, credit to Infinite Yield',
	'[41] unfly',
	'[42] chat [msg] -- Makes you chat a message',
	'[43] spam [msg] -- Spams a message',
	'[44] unspam',
	'[45] spamwait [num] -- Changes delay of chatting a message for the spam command in seconds default is 1 second',
	'[46] pmspam [plr] -- Spams a player in private message',
	'[47] unpmspam',
	'[48] cfreeze [plr] -- Freezes a player on your client, they will only be frozen for you',
	'[49] uncfreeze [plr]',
	'[50] unlockws -- Unlocks the workspace',
	'[51] lockws -- Locks the workspace',
	'[52] btools -- Gives you btools that will only show to you useful for deleting certain blocks only for you',
	'[53] pstand -- Enables platform stand',
	'[54] unpstand -- Disables platform stand',
	'[55] blockhead -- Removes your head mesh',
	'[56] sit',
	'[57] bringobj [obj] -- Only shows on client, brings an object/part to you constantly, can be used to bring healing parts, weapons, money etc, type in exact name',
	'[58] wsvis [num] -- Changes visibility of workspace parts, num should be between 0 and 1, only shows client sided',
	'[59] hypertotal -- Loads in my FE GUI Hypertotal',
	'[60] cmds -- Prints all commands',
	'[61] rmeshhats/blockhats -- Removes the meshes of all your accessories aka block hats',
	'[62] rmeshtool/blocktool -- Removes the mesh of the tool you have equipped aka block tool',
	'[63] spinner -- Makes you spin',
	'[64] nospinner',
	'[65] reach [num] -- Gives you reach, mostly used for swords, say ;reachd for default and enter number after for custom',
	'[66] noreach -- Removes reach, must have tool equipped',
	'[67] rkill [plr] -- Kills you and the player, use kill to just kill the player without dying',
	'[68] tp me [plr] -- Alternative to goto',
	'[69] cbring [plr] -- Brings player infront of you, shows only on client, allows you to do damage to player',
	'[70] uncbring',
	'[71] swap [plr] -- You need a tool! Swaps players position with yours and your position with players',
	'[72] givetool [plr] -- Gives the tool you have equipped to the player',
	'[73] glitch [plr] -- Glitches you and the player, looks very cool',
	'[74] unglitch -- Unglitches you',
	'[75] grespawn -- Alternative to normal respawn and usually works best for when you want to reset with FE Godmode',
	'[76] explorer -- Loads up DEX',
	'[77] reset -- Resets your character.',
	'[78] anim [id] -- Applies an animation on you, must be created by ROBLOX',
	'[79] animgui -- Loads up Energize animations GUI',
	'[80] savepos -- Saves your current position',
	'[81] loadpos -- Teleports you to your saved position',
	'[82] bang [plr] -- 18+ will not work if you have FE Godmode on',
	'[83] unbang',
	'[84] delcmdbar -- Removes the command bar completely',
	'[85] bringmod [obj] -- Brings all the parts in a model, client only, comes from ;bringobj enter exact name of model',
	'[86] shutdown -- Uses harkinians script to shutdown server',
	'[87] respawn -- If grespawn doesnt work you can use respawn',
	'[88] delobj [obj] -- Deletes a certain brick in workspace, client sided',
	'[89] getplrs -- Prints all players in game',
	'[90] deldecal -- Deletes all decals client sided',
	'[91] opfinality -- Loads in my FE GUI Opfinality',
	'[92] remotes -- Prints all remotes in the game in the console when added',
	'[93] noremotes -- Stops printing remotes',
	'[94] tpdefault -- Stops all loop teleports to a player',
	'[95] stopsit -- Will not allow you to sit',
	'[96] gosit -- Allows you to sit',
	'[97] clicktp -- Enables click tp',
	'[98] noclicktp -- Disables click tp',
	'[99] toolson -- If any tools are dropped in the workspace you will automatically get them',
	'[100] toolsoff -- Stops ;toolson',
	'[101] version -- Gets the admin version',
	'[102] state [num] -- Changes your humanoid state, ;unstate to stop.',
	'[103] gravity [num] -- Changes workspace gravity default is 196.2',
	'[104] pgs -- Checks if the game has PGSPhysicsSolverEnabled enabled',
	'[105] clickdel -- Delete any block you press q on, client sided',
	'[106] noclickdel -- Stops clickdel',
	'[107] looprhats -- Loop removes mesh of your hats/loop block hats',
	'[108] unlooprhats -- Stops loop removing mesh',
	'[109] looprtool -- Loop removes mesh of your tool/loop block tools',
	'[110] unlooprtool -- Stops loop removing mesh',
	'[111] givealltools [plr] -- Gives all the tools you have in your backpack to the player',
	'[112] age [plr] -- Makes you chat the account age of the player',
	'[113] id [plr] -- Makes you chat the account ID of the player',
	'[114] .age [plr] -- Privately shows you the account age of the player',
	'[115] .id [plr] -- Privately shows you the account ID of the player',
	'[116] gameid -- Shows the game ID',
	'[117] removeinvis -- Removes all invisible walls/parts, client sided',
	'[118] removefog -- Removes fog, client sided',
	'[119] disable -- Disables your character by removing humanoid',
	'[120] enable -- Enables your character by adding humanoid',
	'[121] prefix [key] -- Changes the prefix used, default is ;',
	'[122] ;resetprefix -- Resets the prefix to ; incase you change it to an unusable prefix. Say exactly ";resetprefix" to do this command, no matter what your prefix is set to.',
	'[123] flyspeed [num] -- Change your fly speed, default is 1',
	'[124] carpet [plr] -- Makes you a carpet for a player, will not work if FE Godmode is on',
	'[125] uncarpet -- Stops carpet player',
	'[126] stare [plr] -- Turns your character to stare at another player',
	'[127] unstare -- Stops stare player',
	'[128] logchat -- Logs all chat (including /e and whispers) of all players',
	'[129] unlogchat -- Disables logchat',
	'[130] fixcam -- Fixes/resets your camera',
	'[131] unstate -- Stops changing state',
}
speedget = 1

lplayer = game:GetService("Players").LocalPlayer

lplayer.CharacterAdded:Connect(function(character)
	spin = false
	flying = false
	staring = false
	banpl = false
end)

function change()
	prefix = prefix
	speedfly = speedfly
end

function GetPlayer(String) -- Credit to Timeless/xFunnieuss
    local Found = {}
    local strl = String:lower()
    if strl == "all" then
        for i,v in pairs(game:GetService("Players"):GetPlayers()) do
            table.insert(Found,v)
        end
    elseif strl == "others" then
        for i,v in pairs(game:GetService("Players"):GetPlayers()) do
            if v.Name ~= lplayer.Name then
                table.insert(Found,v)
            end
        end   
	elseif strl == "me" then
        for i,v in pairs(game:GetService("Players"):GetPlayers()) do
            if v.Name == lplayer.Name then
                table.insert(Found,v)
            end
        end  
    else
        for i,v in pairs(game:GetService("Players"):GetPlayers()) do
            if v.Name:lower():sub(1, #String) == String:lower() then
                table.insert(Found,v)
            end
        end    
    end
    return Found    
end

local Mouse = lplayer:GetMouse()

spin = false
followed = false
traill = false
noclip = false
annoying = false
hwalk = false
droppinghats = false
droppingtools = false
flying = false
spamdelay = 1
spamming = false
spammingpm = false
cbringing = false
remotes = true
added = true
binds = false
stopsitting = false
clickgoto = false
gettingtools = false
removingmeshhats = false
removingmeshtool = false
clickdel = false
staring = false
chatlogs = false
banpl = false
changingstate = false
statechosen = 0

adminversion = "Reviz Admin by illremember, Version 2.0"

flying = false
speedfly = 1

function plrchat(plr, chat)
print(plr.Name..": "..tick().."\n"..chat)
end

for i,v in pairs(game:GetService("Players"):GetPlayers()) do
v.Chatted:connect(function(chat)
if chatlogs then
plrchat(v, chat)
end
end)
end
game:GetService("Players").PlayerAdded:connect(function(plr)
plr.Chatted:connect(function(chat)
if chatlogs then
plrchat(plr, chat)
end
end)
end)


local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local CMDBAR = Instance.new("TextBox")
ScreenGui.Parent = game:GetService("CoreGui")
Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.new(0.3, 0.1, 0.1)
Frame.BackgroundTransparency = 0.3
Frame.Position = UDim2.new(0.5, 0, 0, 10)
Frame.Size = UDim2.new(0, 200, 0, 40)
Frame.Active = true
Frame.Draggable = true
CMDBAR.Name = "CMDBAR"
CMDBAR.Parent = Frame
CMDBAR.BackgroundColor3 = Color3.new(0.105882, 0.164706, 0.207843)
CMDBAR.BackgroundTransparency = 0.20000000298023
CMDBAR.Size = UDim2.new(0, 180, 0, 20)
CMDBAR.Position = UDim2.new(0.05, 0, 0.25, 0)
CMDBAR.Font = Enum.Font.SourceSansLight
CMDBAR.FontSize = Enum.FontSize.Size14
CMDBAR.TextColor3 = Color3.new(0.945098, 0.945098, 0.945098)
CMDBAR.TextScaled = true
CMDBAR.TextSize = 14
CMDBAR.TextWrapped = true
CMDBAR.Text = "Press ; to type, Enter to execute"

local CMDS = Instance.new("ScreenGui")
local CMDSFRAME = Instance.new("Frame")
local ScrollingFrame = Instance.new("ScrollingFrame")
local TextLabel = Instance.new("TextLabel")
local closegui = Instance.new("TextButton")
CMDS.Name = "CMDS"
CMDS.Parent = game:GetService("CoreGui")
CMDSFRAME.Name = "CMDSFRAME"
CMDSFRAME.Parent = CMDS
CMDSFRAME.Active = true
CMDSFRAME.BackgroundColor3 = Color3.new(0.223529, 0.231373, 0.309804)
CMDSFRAME.BorderSizePixel = 0
CMDSFRAME.Draggable = true
CMDSFRAME.Position = UDim2.new(0, 315, 0, 100)
CMDSFRAME.Size = UDim2.new(0, 275, 0, 275)
CMDSFRAME.Visible = false
ScrollingFrame.Parent = CMDSFRAME
ScrollingFrame.BackgroundColor3 = Color3.new(0.160784, 0.160784, 0.203922)
ScrollingFrame.BorderSizePixel = 0
ScrollingFrame.Position = UDim2.new(0, 0, 0.0729999989, 0)
ScrollingFrame.Size = UDim2.new(1.04999995, 0, 0.92900002, 0)
ScrollingFrame.CanvasSize = UDim2.new(0, 0, 10, 0)
TextLabel.Parent = ScrollingFrame
TextLabel.BackgroundColor3 = Color3.new(1, 1, 1)
TextLabel.BackgroundTransparency = 1
TextLabel.Size = UDim2.new(0.930000007, 0, 1, 0)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.FontSize = Enum.FontSize.Size18
TextLabel.Text = "[-] cmdbar is shown when ; is pressed.,\n[1] kill [plr] -- You need a tool! Will kill the player, use rkill to kill you and player,\n[2] bring [plr] -- You need a tool! Will bring player to you,\n[3] spin [plr] -- You need a tool! Makes you and the player spin crazy,\n[4] unspin -- Use after using spin cmd and dying, so you stop loop teleporting,\n[5] attach [plr] -- You need a tool! Attaches you to player,\n[6] unattach [plr] -- Attempts to unattach you from a player,\n[7] follow [plr] -- Makes you follow behind the player,\n[8] unfollow,\n[9] freefall [plr] -- You need a tool! Teleports you and the player up into the air,\n[10] trail [plr] -- The opposite of follow, you stay infront of player,\n[11] untrail,\n[12] orbit [plr] -- Makes you orbit the player,\n[13] unorbit,\n[14] fling [plr] -- Makes you fling the player,\n[15] unfling,\n[16] fecheck -- Checks if the game is FE or not,\n[17] void [plr] -- Teleports player to the void,\n[18] noclip -- Gives you noclip to walk through walls,\n[19] clip -- Removes noclip,\n[20] speed [num]/ws [num] -- Changes how fast you walk 16 is default,\n[21] jumppower [num]/jp [num] -- Changes how high you jump 50 is default,\n[22] hipheight [num]/hh [num] -- Changes how high you float 0 is default,\n[23] default -- Changes your speed, jumppower and hipheight to default values,\n[24] annoy [plr] -- Loop teleports you to the player,\n[25] unannoy,\n[26] headwalk [plr] -- Loop teleports you to the player head,\n[27] unheadwalk,\n[28] nolimbs -- Removes your arms and legs,\n[29] god -- Gives you FE Godmode,\n[30] drophats -- Drops your accessories,\n[31] droptool -- Drops any tool you have equipped,\n[32] loopdhats -- Loop drops your accessories,\n[33] unloopdhats,\n[34] loopdtool -- Loop drops any tools you have equipped,\n[35] unloopdtool,\n[36] invisible -- Gives you invisibility CREDIT TO TIMELESS,\n[37] view [plr] -- Changes your camera to the player character,\n[38] unview,\n[39] goto [plr] -- Teleports you to player,\n[40] fly -- Allows you to fly,\n[41] unfly,\n[42] chat [msg] -- Makes you chat a message,\n[43] spam [msg] -- Spams a message,\n[44] unspam,\n[45] spamwait [num] -- Changes delay of chatting a message for the spam command in seconds default is 1 second,\n[46] pmspam [plr] -- Spams a player in private message,\n[47] unpmspam,\n[48] cfreeze [plr] -- Freezes a player on your client, they will only be frozen for you,\n[49] uncfreeze [plr],\n[50] unlockws -- Unlocks the workspace,\n[51] lockws -- Locks the workspace,\n[52] btools -- Gives you btools that will only show to you useful for deleting certain blocks only for you,\n[53] pstand -- Enables platform stand,\n[54] unpstand -- Disables platform stand,\n[55] blockhead -- Removes your head mesh,\n[56] sit,\n[57] bringobj [obj] -- Only shows on client, brings an object/part to you constantly, can be used to bring healing parts, weapons, money etc, type in exact name,\n[58] wsvis [num] -- Changes visibility of workspace parts, num should be between 0 and 1, only shows client sided,\n[59] hypertotal -- Loads in my FE GUI Hypertotal,\n[60] cmds -- Prints all commands,\n[61] rmeshhats/blockhats -- Removes the meshes of all your accessories aka block hats,\n[62] rmeshtool/blocktool -- Removes the mesh of the tool you have equipped aka block tool,\n[63] spinner -- Makes you spin,\n[64] nospinner,\n[65] reach [num] -- Gives you reach, mostly used for swords, say ;reachd for default and enter number after for custom,\n[66] noreach -- Removes reach, must have tool equipped,\n[67] rkill [plr] -- Kills you and the player, use kill to just kill the player without dying,\n[68] tp me [plr] -- Alternative to goto,\n[69] cbring [plr] -- Brings player infront of you, shows only on client, allows you to do damage to player,\n[70] uncbring,\n[71] swap [plr] -- You need a tool! Swaps players position with yours and your position with players,\n[72] givetool [plr] -- Gives the tool you have equipped to the player,\n[73] glitch [plr] -- Glitches you and the player, looks very cool,\n[74] unglitch -- Unglitches you,\n[75] grespawn -- Alternative to normal respawn and usually works best for when you want to reset with FE Godmode,\n[76] explorer -- Loads up DEX,\n[77] reset -- Resets your character.,\n[78] anim [id] -- Applies an animation on you, must be created by ROBLOX,\n[79] animgui -- Loads up Energize animations GUI,\n[80] savepos -- Saves your current position,\n[81] loadpos -- Teleports you to your saved position,\n[82] bang [plr] -- 18+,\n[83] unbang,\n[84] delcmdbar -- Removes the command bar completely,\n[85] bringmod [obj] -- Brings all the parts in a model, client only, comes from ;bringobj enter exact name of model,\n[86] shutdown -- Uses harkinians script to shutdown server,\n[87] respawn -- If grespawn doesnt work you can use respawn,\n[88] delobj [obj] -- Deletes a certain brick in workspace, client sided,\n[89] getplrs -- Prints all players in game,\n[90] deldecal -- Deletes all decals client sided,\n[91] opfinality -- Loads in my FE GUI Opfinality,\n[92] remotes -- Prints all remotes in the game in the console when added,\n[93] noremotes -- Stops printing remotes,\n[94] tpdefault -- Stops all loop teleports to a player,\n[95] stopsit -- Will not allow you to sit,\n[96] gosit -- Allows you to sit,\n[97] clicktp -- Enables click tp,\n[98] noclicktp -- Disables click tp,\n[99] toolson -- If any tools are dropped in the workspace you will automatically get them,\n[100] toolsoff -- Stops ;toolson,\n[101] version -- Gets the admin version, \n This list of commands is NOT showing everything, go to my thread in the pastebin link to see ALL commands."
TextLabel.TextColor3 = Color3.new(1, 1, 1)
TextLabel.TextSize = 15
TextLabel.TextWrapped = true
TextLabel.TextXAlignment = Enum.TextXAlignment.Left
TextLabel.TextYAlignment = Enum.TextYAlignment.Top
closegui.Name = "closegui"
closegui.Parent = CMDSFRAME
closegui.BackgroundColor3 = Color3.new(0.890196, 0.223529, 0.0588235)
closegui.BorderSizePixel = 0
closegui.Position = UDim2.new(0.995000005, 0, 0, 0)
closegui.Size = UDim2.new(0.0545952693, 0, 0.0728644878, 0)
closegui.Font = Enum.Font.SourceSansBold
closegui.FontSize = Enum.FontSize.Size24
closegui.Text = "X"
closegui.TextColor3 = Color3.new(1, 1, 1)
closegui.TextSize = 20

closegui.MouseButton1Click:connect(function()
	CMDSFRAME.Visible = false
end)

game:GetService('RunService').Stepped:connect(function()
	if spin then
		lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[spinplr.Name].Character.HumanoidRootPart.CFrame
	end
	if followed then
		lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[flwplr.Name].Character.HumanoidRootPart.CFrame + game:GetService("Players")[flwplr.Name].Character.HumanoidRootPart.CFrame.lookVector * -5
	end
	if traill then
		lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[trlplr.Name].Character.HumanoidRootPart.CFrame + game:GetService("Players")[trlplr.Name].Character.HumanoidRootPart.CFrame.lookVector * 5
	end
	if annoying then
		lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[annplr.Name].Character.HumanoidRootPart.CFrame
	end
	if hwalk then
		lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[hdwplr.Name].Character.HumanoidRootPart.CFrame + Vector3.new(0, 4, 0)
	end
	if staring then
		lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(lplayer.Character.Torso.Position, game:GetService("Players")[stareplr.Name].Character.Torso.Position)
	end
end)
game:GetService('RunService').Stepped:connect(function()
	if noclip then
		if lplayer.Character.Humanoid.RigType == Enum.HumanoidRigType.R6 then
			lplayer.Character.Head.CanCollide = false
			lplayer.Character.Torso.CanCollide = false
			lplayer.Character["Left Leg"].CanCollide = false
			lplayer.Character["Right Leg"].CanCollide = false
		else
			lplayer.Character.Humanoid:ChangeState(11)
		end
	end
	if changingstate then
		lplayer.Character.Humanoid:ChangeState(statechosen)
	end
end)
game:GetService('RunService').Stepped:connect(function()
	if droppinghats then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Accessory")) or (v:IsA("Hat")) then
				v.Parent = workspace
			end
		end
	end
	if droppingtools then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Tool")) then
				v.Parent = workspace
			end
		end
	end
	if removingmeshhats then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Accessory")) or (v:IsA("Hat")) then
				v.Handle.Mesh:Destroy()
			end
		end
	end
	if removingmeshtool then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Tool")) then
				v.Handle.Mesh:Destroy()
			end
		end
	end
end)
game:GetService('RunService').Stepped:connect(function()
	if banpl then
		lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[bplrr].Character.HumanoidRootPart.CFrame
	end
end)
game:GetService('RunService').Stepped:connect(function()
	if stopsitting then
		lplayer.Character.Humanoid.Sit = false
	end
end)

plr = lplayer 
hum = plr.Character.HumanoidRootPart
mouse = plr:GetMouse() 
mouse.KeyDown:connect(function(key) 
	if key == "e" then 
		if mouse.Target then 
			if clickgoto then
				hum.CFrame = CFrame.new(mouse.Hit.x, mouse.Hit.y + 5, mouse.Hit.z)
			elseif clickdel then
				mouse.Target:Destroy()
			end
		end 
	end
end)

game:GetService("Workspace").ChildAdded:connect(function(part)
	if gettingtools then
		if part:IsA("Tool") then
			part.Handle.CFrame = lplayer.Character.HumanoidRootPart.CFrame
		end
	end
end)

lplayer.Chatted:Connect(function(msg)
	if string.sub(msg, 1, 6) == (prefix.."kill ") then
		if string.sub(msg, 7) == "me" then
			lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(100000,0,100000)
		else
			for i,v in pairs(GetPlayer(string.sub(msg, 7)))do
				local NOW = lplayer.Character.HumanoidRootPart.CFrame
				lplayer.Character.Humanoid.Name = 1
				local l = lplayer.Character["1"]:Clone()
				l.Parent = lplayer.Character
				l.Name = "Humanoid"
				wait(0.1)
				lplayer.Character["1"]:Destroy()
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
				lplayer.Character.Animate.Disabled = true
				wait(0.1)
				lplayer.Character.Animate.Disabled = false
				lplayer.Character.Humanoid.DisplayDistanceType = "None"
				for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
				lplayer.Character.Humanoid:EquipTool(v)
				end
				local function tp(player,player2)
				local char1,char2=player.Character,player2.Character
				if char1 and char2 then
				char1:MoveTo(char2.Head.Position)
				end
				end
				wait(0.1)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.2)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.5)
				lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(-100000,10,-100000))
				wait(0.7)
				tp(lplayer,game:GetService("Players")[v.Name])
				wait(0.7)
				lplayer.Character.HumanoidRootPart.CFrame = NOW
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "Tools needed!";
				Text = "You need a tool in your backpack for this command!";
				})
			end
		end
	end
	if string.sub(msg, 1, 7) == (prefix.."bring ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 8)))do
			local NOW = lplayer.Character.HumanoidRootPart.CFrame
			lplayer.Character.Humanoid.Name = 1
			local l = lplayer.Character["1"]:Clone()
			l.Parent = lplayer.Character
			l.Name = "Humanoid"
			wait(0.1)
			lplayer.Character["1"]:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
			lplayer.Character.Animate.Disabled = true
			wait(0.1)
			lplayer.Character.Animate.Disabled = false
			lplayer.Character.Humanoid.DisplayDistanceType = "None"
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
			lplayer.Character.Humanoid:EquipTool(v)
			end
			local function tp(player,player2)
			local char1,char2=player.Character,player2.Character
			if char1 and char2 then
			char1.HumanoidRootPart.CFrame = char2.HumanoidRootPart.CFrame
			end
			end
			local function getout(player,player2)
			local char1,char2=player.Character,player2.Character
			if char1 and char2 then
			char1:MoveTo(char2.Head.Position)
			end
			end
			tp(game:GetService("Players")[v.Name], lplayer)
			wait(0.2)
			tp(game:GetService("Players")[v.Name], lplayer)
			wait(0.5)
			lplayer.Character.HumanoidRootPart.CFrame = NOW
			wait(0.5)
			getout(lplayer, game:GetService("Players")[v.Name])
			wait(0.3)
			lplayer.Character.HumanoidRootPart.CFrame = NOW
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools needed!";
			Text = "You need a tool in your backpack for this command!";
			})
		end
	end
	if string.sub(msg, 1, 6) == (prefix.."spin ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
			lplayer.Character.Humanoid.Name = 1
			local l = lplayer.Character["1"]:Clone()
			l.Parent = lplayer.Character
			l.Name = "Humanoid"
			wait(0.1)
			lplayer.Character["1"]:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
			lplayer.Character.Animate.Disabled = true
			wait(0.1)
			lplayer.Character.Animate.Disabled = false
			lplayer.Character.Humanoid.DisplayDistanceType = "None"
			lplayer.Character.Animate.Disabled = false
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
			lplayer.Character.Humanoid:EquipTool(v)
			end
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
			spinplr = v
			wait(0.5)
			spin = true
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools needed!";
			Text = "You need a tool in your backpack for this command!";
			})
		end
	end
	if string.sub(msg, 1, 7) == (prefix.."unspin") then
		spin = false
	end
	if string.sub(msg, 1, 8) == (prefix.."attach ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
			lplayer.Character.Humanoid.Name = 1
			local l = lplayer.Character["1"]:Clone()
			l.Parent = lplayer.Character
			l.Name = "Humanoid"
			wait(0.1)
			lplayer.Character["1"]:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
			lplayer.Character.Animate.Disabled = true
			wait(0.1)
			lplayer.Character.Animate.Disabled = false
			lplayer.Character.Humanoid.DisplayDistanceType = "None"
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
			lplayer.Character.Humanoid:EquipTool(v)
			end
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
			wait(0.3)
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
			attplr = v
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools needed!";
			Text = "You need a tool in your backpack for this command!";
			})
		end
	end
	if string.sub(msg, 1, 10) == (prefix.."unattach ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 11))) do
			local function getout(player,player2)
			local char1,char2=player.Character,player2.Character
			if char1 and char2 then
			char1:MoveTo(char2.Head.Position)
			end
			end
			getout(lplayer, game:GetService("Players")[v.Name])
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."follow ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
			followed = true
			flwplr = v
		end
	end
	if string.sub(msg, 1, 9) == (prefix.."unfollow") then
		followed = false
	end
	if string.sub(msg, 1, 10) == (prefix.."freefall ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 11))) do
			local NOW = lplayer.Character.HumanoidRootPart.CFrame
			lplayer.Character.Humanoid.Name = 1
			local l = lplayer.Character["1"]:Clone()
			l.Parent = lplayer.Character
			l.Name = "Humanoid"
			wait(0.1)
			lplayer.Character["1"]:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
			lplayer.Character.Animate.Disabled = true
			wait(0.1)
			lplayer.Character.Animate.Disabled = false
			lplayer.Character.Humanoid.DisplayDistanceType = "None"
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
			lplayer.Character.Humanoid:EquipTool(v)
			end
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			wait(0.2)
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			wait(0.6)
			lplayer.Character.HumanoidRootPart.CFrame = NOW
			wait(0.6)
			lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(0,50000,0)
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools needed!";
			Text = "You need a tool in your backpack for this command!";
			})
		end
	end
	if string.sub(msg, 1, 7) == (prefix.."trail ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
			traill = true
			trlplr = v
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."untrail") then
		traill = false
	end
	if string.sub(msg, 1, 7) == (prefix.."orbit ") then
		if string.sub(msg, 8) == "all" or string.sub(msg, 8) == "others" or string.sub(msg, 8) == "me" then
			lplayer.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame
		else
			for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
				local o = Instance.new("RocketPropulsion")
				o.Parent = lplayer.Character.HumanoidRootPart
				o.Name = "Orbit"
				o.Target = game:GetService("Players")[v.Name].Character.HumanoidRootPart
				o:Fire()
				noclip = true
			end
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."unorbit") then
		lplayer.Character.HumanoidRootPart.Orbit:Destroy()
		noclip = false
	end
	if string.sub(msg, 1, 7) == (prefix.."fling ") then
		if string.sub(msg, 8) == "all" or string.sub(msg, 8) == "others" or string.sub(msg, 8) == "me" then
			lplayer.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame
		else
			for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
				local y = Instance.new("RocketPropulsion")
				y.Parent = lplayer.Character.HumanoidRootPart
				y.CartoonFactor = 1
				y.MaxThrust = 800000
				y.MaxSpeed = 1000
				y.ThrustP = 200000
				y.Name = "Fling"
				game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Head
				y.Target = game:GetService("Players")[v.Name].Character.HumanoidRootPart
				y:Fire()
				noclip = true
			end
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."unfling") then
		noclip = false
		lplayer.Character.HumanoidRootPart.Fling:Destroy()
		game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Head
		wait(0.4)
		lplayer.Character.HumanoidRootPart.Fling:Destroy()
	end
	if string.sub(msg, 1, 8) == (prefix.."fecheck") then
		if game:GetService("Workspace").FilteringEnabled == true then
			warn("FE is Enabled (Filtering Enabled)")
			game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "FE is Enabled";
				Text = "Filtering Enabled. Enjoy using Reviz Admin!";
			})
		else
			warn("FE is Disabled (Filtering Disabled) Consider using a different admin script.")
			game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "FE is Disabled";
				Text = "Filtering Disabled. Consider using a different admin script.";
			})
		end
	end
	if string.sub(msg, 1, 6) == (prefix.."void ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
			lplayer.Character.Humanoid.Name = 1
			local l = lplayer.Character["1"]:Clone()
			l.Parent = lplayer.Character
			l.Name = "Humanoid"
			wait(0.1)
			lplayer.Character["1"]:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
			lplayer.Character.Animate.Disabled = true
			wait(0.1)
			lplayer.Character.Animate.Disabled = false
			lplayer.Character.Humanoid.DisplayDistanceType = "None"
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
			lplayer.Character.Humanoid:EquipTool(v)
			end
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			wait(0.2)
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			wait(0.6)
			lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(999999999999999,0,999999999999999)
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools needed!";
			Text = "You need a tool in your backpack for this command!";
			})
		end
	end
	if string.sub(msg, 1, 7) == (prefix.."noclip") then
		noclip = true
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Noclip enabled";
		Text = "Type ;clip to disable";
		})
	end
	if string.sub(msg, 1, 5) == (prefix.."clip") then
		noclip = false
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Noclip disabled";
		Text = "Type ;noclip to enable";
		})
	end
	if string.sub(msg, 1, 7) == (prefix.."speed ") then
		lplayer.Character.Humanoid.WalkSpeed = (string.sub(msg, 8))
	end
	if string.sub(msg, 1, 4) == (prefix.."ws ") then
		lplayer.Character.Humanoid.WalkSpeed = (string.sub(msg, 5))
	end
	if string.sub(msg, 1, 11) == (prefix.."hipheight ") then
		lplayer.Character.Humanoid.HipHeight = (string.sub(msg, 12))
	end
	if string.sub(msg, 1, 4) == (prefix.."hh ") then
		lplayer.Character.Humanoid.HipHeight = (string.sub(msg, 5))
	end
	if string.sub(msg, 1, 11) == (prefix.."jumppower ") then
		lplayer.Character.Humanoid.JumpPower = (string.sub(msg, 12))
	end
	if string.sub(msg, 1, 4) == (prefix.."jp ") then
		lplayer.Character.Humanoid.JumpPower = (string.sub(msg, 5))
	end
	if string.sub(msg, 1, 8) == (prefix.."default") then
		lplayer.Character.Humanoid.JumpPower = 50
		lplayer.Character.Humanoid.WalkSpeed = 16
		lplayer.Character.Humanoid.HipHeight = 0
	end
	if string.sub(msg, 1, 7) == (prefix.."annoy ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
			annoying = true
			annplr = v
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."unannoy") then
		annoying = false
	end
	if string.sub(msg, 1, 10) == (prefix.."headwalk ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 11))) do
			hwalk = true
			hdwplr = v
		end
	end
	if string.sub(msg, 1, 11) == (prefix.."unheadwalk") then
		hwalk = false
	end
	if string.sub(msg, 1, 8) == (prefix.."nolimbs") then
		lplayer.Character["Left Leg"]:Destroy()
		lplayer.Character["Left Arm"]:Destroy()
		lplayer.Character["Right Leg"]:Destroy()
		lplayer.Character["Right Arm"]:Destroy()
	end
	if string.sub(msg, 1, 4) == (prefix.."god") then
		lplayer.Character.Humanoid.Name = 1
		local l = lplayer.Character["1"]:Clone()
		l.Parent = lplayer.Character
		l.Name = "Humanoid"
		wait(0.1)
		lplayer.Character["1"]:Destroy()
		game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
		lplayer.Character.Animate.Disabled = true
		wait(0.1)
		lplayer.Character.Animate.Disabled = false
		lplayer.Character.Humanoid.DisplayDistanceType = "None"
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "FE Godmode enabled";
		Text = "Use ;grespawn or ;respawn to remove";
		})
	end
	if string.sub(msg, 1, 9) == (prefix.."drophats") then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Accessory")) or (v:IsA("Hat")) then
				v.Parent = workspace
			end
		end
	end
	if string.sub(msg, 1, 9) == (prefix.."droptool") then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Tool")) then
				v.Parent = workspace
			end
		end
	end
	if string.sub(msg, 1, 10) == (prefix.."loopdhats") then
		droppinghats = true
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Loop Drop Enabled";
		Text = "Type ;unloopdhats to disable";
		})
	end
	if string.sub(msg, 1, 12) == (prefix.."unloopdhats") then
		droppinghats = false
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Loop Drop Disabled";
		Text = "Type ;loopdhats to enable.";
		})
	end
	if string.sub(msg, 1, 10) == (prefix.."loopdtool") then
		droppingtools = true
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Loop Drop Enabled";
		Text = "Type ;unloopdtool to disable";
		})
	end
	if string.sub(msg, 1, 12) == (prefix.."unloopdtool") then
		droppingtools = false
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Loop Drop Disabled";
		Text = "Type ;loopdtool to enable.";
		})
	end
	if string.sub(msg, 1, 10) == (prefix.."invisible") then -- Credit to Timeless
		Local = game:GetService('Players').LocalPlayer
		Char  = Local.Character
		touched,tpdback = false, false
		box = Instance.new('Part',workspace)
		box.Anchored = true
		box.CanCollide = true
		box.Size = Vector3.new(10,1,10)
		box.Position = Vector3.new(0,10000,0)
		box.Touched:connect(function(part)
		    if (part.Parent.Name == Local.Name) then
		        if touched == false then
		            touched = true
		            function apply()
		                if script.Disabled ~= true then
		                    no = Char.HumanoidRootPart:Clone()
		                    wait(.25)
		                    Char.HumanoidRootPart:Destroy()
		                    no.Parent = Char
		                    Char:MoveTo(loc)
		                    touched = false
		                end end
		            if Char then
		                apply()
		            end
		        end
		    end
		end)
		repeat wait() until Char
		loc = Char.HumanoidRootPart.Position
		Char:MoveTo(box.Position + Vector3.new(0,.5,0))
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Invisibility enabled!";
		Text = "Reset or use ;respawn to remove.";
		})
	end
	if string.sub(msg, 1, 6) == (prefix.."view ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
			if game:GetService("Players")[v.Name].Character.Humanoid then
				game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Humanoid
			else
				game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Head
			end
		end
	end
	if string.sub(msg, 1, 7) == (prefix.."unview") then
		if lplayer.Character.Humanoid then
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Humanoid
		else
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Head
		end
	end
	if string.sub(msg, 1, 6) == (prefix.."goto ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
		end
	end
	if string.sub(msg, 1, 4) == (prefix.."fly") then
	repeat wait() until lplayer and lplayer.Character and lplayer.Character:FindFirstChild('HumanoidRootPart') and lplayer.Character:FindFirstChild('Humanoid')
	repeat wait() until Mouse
	
	local T = lplayer.Character.HumanoidRootPart
	local CONTROL = {F = 0, B = 0, L = 0, R = 0}
	local lCONTROL = {F = 0, B = 0, L = 0, R = 0}
	local SPEED = speedget
	
	local function fly()
		flying = true
		local BG = Instance.new('BodyGyro', T)
		local BV = Instance.new('BodyVelocity', T)
		BG.P = 9e4
		BG.maxTorque = Vector3.new(9e9, 9e9, 9e9)
		BG.cframe = T.CFrame
		BV.velocity = Vector3.new(0, 0.1, 0)
		BV.maxForce = Vector3.new(9e9, 9e9, 9e9)
		spawn(function()
		repeat wait()
		lplayer.Character.Humanoid.PlatformStand = true
		if CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0 then
		SPEED = 50
		elseif not (CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0) and SPEED ~= 0 then
		SPEED = 0
		end
		if (CONTROL.L + CONTROL.R) ~= 0 or (CONTROL.F + CONTROL.B) ~= 0 then
		BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (CONTROL.F + CONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(CONTROL.L + CONTROL.R, (CONTROL.F + CONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
		lCONTROL = {F = CONTROL.F, B = CONTROL.B, L = CONTROL.L, R = CONTROL.R}
		elseif (CONTROL.L + CONTROL.R) == 0 and (CONTROL.F + CONTROL.B) == 0 and SPEED ~= 0 then
		BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (lCONTROL.F + lCONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(lCONTROL.L + lCONTROL.R, (lCONTROL.F + lCONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
		else
		BV.velocity = Vector3.new(0, 0.1, 0)
		end
		BG.cframe = workspace.CurrentCamera.CoordinateFrame
				until not flying
				CONTROL = {F = 0, B = 0, L = 0, R = 0}
				lCONTROL = {F = 0, B = 0, L = 0, R = 0}
				SPEED = 0
				BG:destroy()
				BV:destroy()
				lplayer.Character.Humanoid.PlatformStand = false
			end)
		end
	Mouse.KeyDown:connect(function(KEY)
		if KEY:lower() == 'w' then
			CONTROL.F = speedfly
		elseif KEY:lower() == 's' then
			CONTROL.B = -speedfly
		elseif KEY:lower() == 'a' then
			CONTROL.L = -speedfly 
		elseif KEY:lower() == 'd' then 
			CONTROL.R = speedfly
		end
	end)
	Mouse.KeyUp:connect(function(KEY)
		if KEY:lower() == 'w' then
			CONTROL.F = 0
		elseif KEY:lower() == 's' then
			CONTROL.B = 0
		elseif KEY:lower() == 'a' then
			CONTROL.L = 0
		elseif KEY:lower() == 'd' then
			CONTROL.R = 0
		end
	end)
	fly()
	end
	if string.sub(msg, 1, 6) == (prefix.."unfly") then
		flying = false
		lplayer.Character.Humanoid.PlatformStand = false
	end
	if string.sub(msg, 1, 6) == (prefix.."chat ") then
		game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer((string.sub(msg, 7)), "All")
	end
	if string.sub(msg, 1, 6) == (prefix.."spam ") then
		spamtext = (string.sub(msg, 7))
		spamming = true
	end
	if string.sub(msg, 1, 7) == (prefix.."unspam") then
		spamming = false
	end
	if string.sub(msg, 1, 10) == (prefix.."spamwait ") then
		spamdelay = (string.sub(msg, 11))
	end
	if string.sub(msg, 1, 8) == (prefix.."pmspam ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
			pmspammed = v.Name
			spammingpm = true
		end
	end
	if string.sub(msg, 1, 9) == (prefix.."unpmspam") then
		spammingpm = false
	end
	if string.sub(msg, 1, 9) == (prefix.."cfreeze ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 10))) do
			v.Character["Left Leg"].Anchored = true
			v.Character["Left Arm"].Anchored = true
			v.Character["Right Leg"].Anchored = true
			v.Character["Right Arm"].Anchored = true
			v.Character.Torso.Anchored = true
			v.Character.Head.Anchored = true
		end
	end
	if string.sub(msg, 1, 11) == (prefix.."uncfreeze ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 12))) do
			v.Character["Left Leg"].Anchored = false
			v.Character["Left Arm"].Anchored = false
			v.Character["Right Leg"].Anchored = false
			v.Character["Right Arm"].Anchored = false
			v.Character.Torso.Anchored = false
			v.Character.Head.Anchored = false
		end
	end
	if string.sub(msg, 1, 9) == (prefix.."unlockws") then
		local a = game:GetService("Workspace"):getChildren()
		for i = 1, #a do
			if a[i].className == "Part" then
				a[i].Locked = false
			elseif a[i].className == "Model" then
				local r = a[i]:getChildren()
				for i = 1, #r do
					if r[i].className == "Part" then
					r[i].Locked = false
					end
				end
			end
		end
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Success!";
		Text = "Workspace unlocked. Use ;lockws to lock.";
		})
	end
	if string.sub(msg, 1, 7) == (prefix.."lockws") then
		local a = game:GetService("Workspace"):getChildren()
		for i = 1, #a do
			if a[i].className == "Part" then
				a[i].Locked = true
			elseif a[i].className == "Model" then
				local r = a[i]:getChildren()
				for i = 1, #r do
					if r[i].className == "Part" then
					r[i].Locked = true
					end
				end
			end
		end
	end
	if string.sub(msg, 1, 7) == (prefix.."btools") then
		local Clone_T = Instance.new("HopperBin",lplayer.Backpack)
		Clone_T.BinType = "Clone"
		local Destruct = Instance.new("HopperBin",lplayer.Backpack)
		Destruct.BinType = "Hammer"
		local Hold_T = Instance.new("HopperBin",lplayer.Backpack)
		Hold_T.BinType = "Grab"
	end
	if string.sub(msg, 1, 7) == (prefix.."pstand") then
		lplayer.Character.Humanoid.PlatformStand = true
	end
	if string.sub(msg, 1, 9) == (prefix.."unpstand") then
		lplayer.Character.Humanoid.PlatformStand = false
	end
	if string.sub(msg, 1, 10) == (prefix.."blockhead") then
		lplayer.Character.Head.Mesh:Destroy()
	end
	if string.sub(msg, 1, 4) == (prefix.."sit") then
		lplayer.Character.Humanoid.Sit = true
	end
	if string.sub(msg, 1, 10) == (prefix.."bringobj ") then
		local function bringobjw()
		for i,obj in ipairs(game:GetService("Workspace"):GetDescendants()) do
		if obj.Name == (string.sub(msg, 11)) then
		obj.CFrame = lplayer.Character.HumanoidRootPart.CFrame
		obj.CanCollide = false
		obj.Transparency = 0.7
		wait()
		obj.CFrame = lplayer.Character["Left Leg"].CFrame
		wait()
		obj.CFrame = lplayer.Character["Right Leg"].CFrame
		wait()
		obj.CFrame = lplayer.Character["Head"].CFrame
		end
		end
		end
		while wait() do
			bringobjw()
		end
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "BringObj";
		Text = "BringObj enabled.";
		})
	end
	if string.sub(msg, 1, 7) == (prefix.."wsvis ") then
		vis = (string.sub(msg, 8))
		local a = game:GetService("Workspace"):GetDescendants()
		for i = 1, #a do
			if a[i].className == "Part" then
				a[i].Transparency = vis
			elseif a[i].className == "Model" then
				local r = a[i]:getChildren()
				for i = 1, #r do
					if r[i].className == "Part" then
					r[i].Transparency = vis
					end
				end
			end
		end
	end
	if string.sub(msg, 1, 11) == (prefix.."hypertotal") then
		loadstring(game:GetObjects("rbxassetid://1255063809")[1].Source)()
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Success!";
		Text = "HyperTotal GUI Loaded!";
		})
	end
	if string.sub(msg, 1, 5) == (prefix.."cmds") then
		CMDSFRAME.Visible = true
	end
	if string.sub(msg, 1, 10) == (prefix.."rmeshhats") then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Accessory")) or (v:IsA("Hat")) then
				v.Handle.Mesh:Destroy()
			end
		end
	end
	if string.sub(msg, 1, 10) == (prefix.."blockhats") then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Accessory")) or (v:IsA("Hat")) then
				v.Handle.Mesh:Destroy()
			end
		end
	end
	if string.sub(msg, 1, 10) == (prefix.."rmeshtool") then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Tool")) then
				v.Handle.Mesh:Destroy()
			end
		end
	end
	if string.sub(msg, 1, 10) == (prefix.."blocktool") then
		for i,v in pairs(lplayer.Character:GetChildren()) do
			if (v:IsA("Tool")) then
				v.Handle.Mesh:Destroy()
			end
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."spinner") then
		local p = Instance.new("RocketPropulsion")
		p.Parent = lplayer.Character.HumanoidRootPart
		p.Name = "Spinner"
		p.Target = lplayer.Character["Left Arm"]
		p:Fire()
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Spinner enabled";
		Text = "Type ;nospinner to disable.";
		})
	end
	if string.sub(msg, 1, 10) == (prefix.."nospinner") then
		lplayer.Character.HumanoidRootPart.Spinner:Destroy()
	end
	if string.sub(msg, 1, 7) == (prefix.."reachd") then
		for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
			if v:isA("Tool") then
				local a = Instance.new("SelectionBox",v.Handle)
				a.Adornee = v.Handle
				v.Handle.Size = Vector3.new(0.5,0.5,60)
				v.GripPos = Vector3.new(0,0,0)
				lplayer.Character.Humanoid:UnequipTools()
			end
		end
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Reach applied!";
		Text = "Applied to equipped sword. Use ;noreach to disable.";
		})
	end
	if string.sub(msg, 1, 7) == (prefix.."reach ") then
		for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
			if v:isA("Tool") then
				handleSize = v.Handle.Size
				wait()
				local a = Instance.new("SelectionBox",v.Handle)
				a.Name = "a"
				a.Adornee = v.Handle
				v.Handle.Size = Vector3.new(0.5,0.5,(string.sub(msg, 8)))
				v.GripPos = Vector3.new(0,0,0)
				lplayer.Character.Humanoid:UnequipTools()
			end
		end
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Reach applied!";
		Text = "Applied to equipped sword. Use ;noreach to disable.";
		})
	end
	if string.sub(msg, 1, 8) == (prefix.."noreach") then
		for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
			if v:isA("Tool") then
				v.Handle.a:Destroy()
				v.Handle.Size = handleSize
			end
		end
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Reach removed!";
		Text = "Removed reach from equipped sword.";
		})
	end
	if string.sub(msg, 1, 7) == (prefix.."rkill ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 8)))do
			lplayer.Character.Humanoid.Name = 1
			local l = lplayer.Character["1"]:Clone()
			l.Parent = lplayer.Character
			l.Name = "Humanoid"
			wait(0.1)
			lplayer.Character["1"]:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
			lplayer.Character.Animate.Disabled = true
			wait(0.1)
			lplayer.Character.Animate.Disabled = false
			lplayer.Character.Humanoid.DisplayDistanceType = "None"
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
			lplayer.Character.Humanoid:EquipTool(v)
			end
			wait(0.1)
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			wait(0.2)
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			wait(0.5)
			lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(-100000,10,-100000))
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools needed!";
			Text = "You need a tool in your backpack for this command!";
			})
		end
	end
	if string.sub(msg, 1, 7) == (prefix.."tp me ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."cbring ") then
		if (string.sub(msg, 9)) == "all" or (string.sub(msg, 9)) == "All" or (string.sub(msg, 9)) == "ALL" then
			cbringall = true
		else
			for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
				brplr = v.Name
			end
		end
		cbring = true
	end
	if string.sub(msg, 1, 9) == (prefix.."uncbring") then
		cbring = false
		cbringall = false
	end
	if string.sub(msg, 1, 6) == (prefix.."swap ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
			local NOWPLR = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			local NOW = lplayer.Character.HumanoidRootPart.CFrame
			lplayer.Character.Humanoid.Name = 1
			local l = lplayer.Character["1"]:Clone()
			l.Parent = lplayer.Character
			l.Name = "Humanoid"
			wait(0.1)
			lplayer.Character["1"]:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
			lplayer.Character.Animate.Disabled = true
			wait(0.1)
			lplayer.Character.Animate.Disabled = false
			lplayer.Character.Humanoid.DisplayDistanceType = "None"
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
			lplayer.Character.Humanoid:EquipTool(v)
			end
			local function tp(player,player2)
			local char1,char2=player.Character,player2.Character
			if char1 and char2 then
			char1:MoveTo(char2.Head.Position)
			end
			end
			wait(0.1)
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			wait(0.2)
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			wait(0.5)
			lplayer.Character.HumanoidRootPart.CFrame = NOW
			wait(0.6)
			tp(lplayer, game:GetService("Players")[v.Name])
			wait(0.4)
			lplayer.Character.HumanoidRootPart.CFrame = NOWPLR
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools needed!";
			Text = "You need a tool in your backpack for this command!";
			})
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."glitch ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
			lplayer.Character.Humanoid.Name = 1
			local l = lplayer.Character["1"]:Clone()
			l.Parent = lplayer.Character
			l.Name = "Humanoid"
			wait(0.1)
			lplayer.Character["1"]:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
			lplayer.Character.Animate.Disabled = true
			wait(0.1)
			lplayer.Character.Animate.Disabled = false
			lplayer.Character.Humanoid.DisplayDistanceType = "None"
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
			lplayer.Character.Humanoid:EquipTool(v)
			end
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
			wait(0.3)
			lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
			wait(0.4)
			b = Instance.new("BodyForce")
			b.Parent = lplayer.Character.HumanoidRootPart
			b.Name = "Glitch"
			b.Force = Vector3.new(100000000,5000,0)
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools needed!";
			Text = "You need a tool in your backpack for this command!";
			})
		end
	end
	if string.sub(msg, 1, 9) == (prefix.."unglitch") then
		lplayer.Character.HumanoidRootPart.Glitch:Destroy()
		lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(10000,0,10000)
		b = Instance.new("BodyForce")
		b.Parent = lplayer.Character.HumanoidRootPart
		b.Name = "unGlitch"
		b.Force = Vector3.new(0,-5000000,0)
		wait(2)
		lplayer.Character.HumanoidRootPart.unGlitch:Destroy()
	end
	if string.sub(msg, 1, 9) == (prefix.."grespawn") then
		lplayer.Character.Humanoid.Health = 0
		wait(1)
		lplayer.Character.Head.CFrame = CFrame.new(1000000,0,1000000)
		lplayer.Character.Torso.CFrame = CFrame.new(1000000,0,1000000)
	end
	if string.sub(msg, 1, 9) == (prefix.."explorer") then
		loadstring(game:GetObjects("rbxassetid://492005721")[1].Source)()
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Success!";
		Text = "DEX Explorer has loaded.";
		})
	end
	if string.sub(msg, 1, 6) == (prefix.."anim ") then
		local Anim = Instance.new("Animation")
		Anim.AnimationId = "rbxassetid://"..(string.sub(msg, 7))
		local track = lplayer.Character.Humanoid:LoadAnimation(Anim)
		track:Play(.1, 1, 1)
	end
	if string.sub(msg, 1, 8) == (prefix.."animgui") then
		loadstring(game:GetObjects("rbxassetid://1202558084")[1].Source)()
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Success!";
		Text = "Energize Animations GUI has loaded.";
		})
	end
	if string.sub(msg, 1, 8) == (prefix.."savepos") then
		saved = lplayer.Character.HumanoidRootPart.CFrame
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Position Saved";
		Text = "Use ;loadpos to return to saved position.";
		})
	end
	if string.sub(msg, 1, 8) == (prefix.."loadpos") then
		lplayer.Character.HumanoidRootPart.CFrame = saved
	end
	if string.sub(msg, 1, 6) == (prefix.."bang ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
			local Anim2 = Instance.new("Animation")
			Anim2.AnimationId = "rbxassetid://148840371"
			local track2 = lplayer.Character.Humanoid:LoadAnimation(Anim2)
			track2:Play(.1, 1, 1)
			bplrr = v.Name
			banpl = true
		end
	end
	if string.sub(msg, 1, 7) == (prefix.."unbang") then
		banpl = false
	end
	if string.sub(msg, 1, 10) == (prefix.."bringmod ") then
		local function bringmodw()
		for i,obj in ipairs(game:GetService("Workspace"):GetDescendants()) do
		if obj.Name == (string.sub(msg, 11)) then
		for i,ch in pairs(obj:GetDescendants()) do
		if (ch:IsA("BasePart")) then
		ch.CFrame = lplayer.Character.HumanoidRootPart.CFrame
		ch.CanCollide = false
		ch.Transparency = 0.7
		wait()
		ch.CFrame = lplayer.Character["Left Leg"].CFrame
		wait()
		ch.CFrame = lplayer.Character["Right Leg"].CFrame
		wait()
		ch.CFrame = lplayer.Character["Head"].CFrame
		end
		end
		end
		end
		end
		while wait() do
			bringmodw()
		end
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "BringMod";
		Text = "BringMod enabled.";
		})
	end
	if string.sub(msg, 1, 8) == (prefix.."respawn") then
		local mod = Instance.new('Model', workspace) mod.Name = 're '..lplayer.Name
		local hum = Instance.new('Humanoid', mod)
		local ins = Instance.new('Part', mod) ins.Name = 'Torso' ins.CanCollide = false ins.Transparency = 1
		lplayer.Character = mod
	end
	if string.sub(msg, 1, 9) == (prefix.."shutdown") then
		game:GetService'RunService'.Stepped:Connect(function()
		pcall(function()
		    for i,v in pairs(game:GetService'Players':GetPlayers()) do
		        if v.Character ~= nil and v.Character:FindFirstChild'Head' then
		            for _,x in pairs(v.Character.Head:GetChildren()) do
		                if x:IsA'Sound' then x.Playing = true x.CharacterSoundEvent:FireServer(true, true) end
		            end
		        end
		    end
		end)
		end)
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Attempting Shutdown";
		Text = "Shutdown Attempt has begun.";
		})
	end
	if string.sub(msg, 1, 8) == (prefix.."delobj ") then
		objtodel = (string.sub(msg, 9))
		for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
			if v.Name == objtodel then
				v:Destroy()
			end
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."getplrs") then
		for i,v in pairs(game:GetService("Players"):GetPlayers())do
			print(v)
		end
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Printed";
		Text = "Players have been printed to console. (F9)";
		})
	end
	if string.sub(msg, 1, 9) == (prefix.."deldecal") then
		for i,v in pairs(game:GetService("Workspace"):GetDescendants())do
			if (v:IsA("Decal")) then
				v:Destroy()
			end
		end
	end
	if string.sub(msg, 1, 11) == (prefix.."opfinality") then
		loadstring(game:GetObjects("rbxassetid://1294358929")[1].Source)()
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Success!";
		Text = "OpFinality GUI has loaded.";
		})
	end
	if string.sub(msg, 1, 8) == (prefix.."remotes") then
		remotes = true
		added = true
		game.DescendantAdded:connect(function(rmt)
		if added == true then
		if remotes == true then 
		if rmt:IsA("RemoteEvent") then
		print("A RemoteEvent was added!")
		print(" game." .. rmt:GetFullName() .. " | RemoteEvent")
		print(" game." .. rmt:GetFullName() .. " | RemoteEvent", 247, 0, 0, true)
		end end end
		end)
		game.DescendantAdded:connect(function(rmtfnctn)
		if added == true then
		if remotes == true then 
		if rmtfnctn:IsA("RemoteFunction") then
		warn("A RemoteFunction was added!")
		warn(" game." .. rmtfnctn:GetFullName() .. " | RemoteFunction")
		print(" game." .. rmtfnctn:GetFullName() .. " | RemoteFunction", 5, 102, 198, true)
		end end end
		end)
		
		game.DescendantAdded:connect(function(bndfnctn)
		if added == true then
		if binds == true then 
		if bndfnctn:IsA("BindableFunction") then
		print("A BindableFunction was added!")
		print(" game." .. bndfnctn:GetFullName() .. " | BindableFunction")
		print(" game." .. bndfnctn:GetFullName() .. " | BindableFunction", 239, 247, 4, true)
		end end end
		end)
		
		game.DescendantAdded:connect(function(bnd)
		if added == true then
		if binds == true then 
		if bnd:IsA("BindableEvent") then
		warn("A BindableEvent was added!")
		warn(" game." .. bnd:GetFullName() .. " | BindableEvent")
		print(" game." .. bnd:GetFullName() .. " | BindableEvent", 13, 193, 22, true)
		end end end
		end)
		
		
		if binds == true then
		for i,v in pairs(game:GetDescendants()) do
		if v:IsA("BindableFunction") then
		print(" game." .. v:GetFullName() .. " | BindableFunction")
		print(" game." .. v:GetFullName() .. " | BindableFunction", 239, 247, 4, true)
		end end
		for i,v in pairs(game:GetDescendants()) do
		if v:IsA("BindableEvent") then
		warn(" game." .. v:GetFullName() .. " | BindableEvent")
		print(" game." .. v:GetFullName() .. " | BindableEvent", 13, 193, 22, true)
		end end
		else
		print("Off")
		end
		if remotes == true then
		for i,v in pairs(game:GetDescendants()) do
		if v:IsA("RemoteFunction") then
		warn(" game." .. v:GetFullName() .. " | RemoteFunction")
		print(" game." .. v:GetFullName() .. " | RemoteFunction", 5, 102, 198, true)
		end end
		wait()
		for i,v in pairs(game:GetDescendants()) do
		if v:IsA("RemoteEvent") then
		print(" game." .. v:GetFullName() .. " | RemoteEvent")
		print(" game." .. v:GetFullName() .. " | RemoteEvent", 247, 0, 0, true)
		end end
		else
		print("Off")
		end
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Printing Remotes";
		Text = "Type ;noremotes to disable.";
		})
	end
	if string.sub(msg, 1, 10) == (prefix.."noremotes") then
		remotes = false
		added = false
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Printing Remotes Disabled";
		Text = "Type ;remotes to enable.";
		})
	end
	if string.sub(msg, 1, 10) == (prefix.."tpdefault") then
		spin = false
		followed = false
		traill = false
		noclip = false
		annoying = false
		hwalk = false
		cbringing = false
	end
	if string.sub(msg, 1, 8) == (prefix.."stopsit") then
		stopsitting = true
	end
	if string.sub(msg, 1, 6) == (prefix.."gosit") then
		stopsitting = false
	end
	if string.sub(msg, 1, 8) == (prefix.."version") then
		print(adminversion)
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Version";
		Text = adminversion;
		})
	end
	if string.sub(msg, 1, 8) == (prefix.."clicktp") then
		clickgoto = true
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Click TP";
		Text = "Press E to teleport to mouse position, ;noclicktp to stop";
		})
	end
	if string.sub(msg, 1, 9) == (prefix.."clickdel") then
		clickdel = true
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Click Delete";
		Text = "Press E to delete part at mouse, ;noclickdel to stop";
		})
	end
	if string.sub(msg, 1, 11) == (prefix.."noclickdel") then
		clickdel = false
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Click Delete";
		Text = "Click delete has been disabled.";
		})
	end
	if string.sub(msg, 1, 10) == (prefix.."noclicktp") then
		clickgoto = false
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Click TP";
		Text = "Click TP has been disabled.";
		})
	end
	if string.sub(msg, 1, 8) == (prefix.."toolson") then
		gettingtools = true
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Tools Enabled";
		Text = "Automatically colleting tools dropped.";
		})
	end
	if string.sub(msg, 1, 9) == (prefix.."toolsoff") then
		gettingtools = false
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Tools Disabled";
		Text = "Click TP has been disabled.";
		})
	end
	if string.sub(msg, 1, 10) == (prefix.."delcmdbar") then
		ScreenGui:Destroy()
	end
	if string.sub(msg, 1, 6) == (prefix.."reset") then
		lplayer.Character.Head:Destroy()
	end
	if string.sub(msg, 1, 7) == (prefix.."state ") then
		statechosen = string.sub(msg, 8)
		changingstate = true
	end
	if string.sub(msg, 1, 9) == (prefix.."gravity ") then
		game:GetService("Workspace").Gravity = string.sub(msg, 10)
	end
	if string.sub(msg, 1, 10) == (prefix.."looprhats") then
		removingmeshhats = true
	end
	if string.sub(msg, 1, 12) == (prefix.."unlooprhats") then
		removingmeshhats = false
	end
	if string.sub(msg, 1, 10) == (prefix.."looprtool") then
		removingmeshtool = true
	end
	if string.sub(msg, 1, 12) == (prefix.."unlooprtool") then
		removingmeshtool = false
	end
	if string.sub(msg, 1, 10) == (prefix.."givetool ") then
		for i,v in pairs(game:GetService("Players").LocalPlayer.Character:GetDescendants()) do
			if v:IsA("Tool") then
				for i,player in pairs(GetPlayer(string.sub(msg, 11))) do
					v.Parent = player.Character
				end
			end
		end
	end
	if string.sub(msg, 1, 14) == (prefix.."givealltools ") then
		for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetDescendants()) do
			if v:IsA("Tool") then
				v.Parent = lplayer.Character
				wait()
				for i,player in pairs(GetPlayer(string.sub(msg, 15))) do
					v.Parent = player.Character
				end
			end
		end
	end
	if string.sub(msg, 1, 5) == (prefix.."age ") then
		for i,player in pairs(GetPlayer(string.sub(msg, 6))) do
			game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(player.Name.." Account Age: "..player.AccountAge.." days!", "All")
		end
	end
	if string.sub(msg, 1, 4) == (prefix.."id ") then
		for i,player in pairs(GetPlayer(string.sub(msg, 5))) do
			game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(player.Name.." Account ID: "..player.UserId, "All")
		end
	end
	if string.sub(msg, 1, 6) == (prefix..".age ") then
		for i,player in pairs(GetPlayer(string.sub(msg, 7))) do
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = player.AccountAge.." Days";
			Text = "Account age of "..player.Name;
			})
		end
	end
	if string.sub(msg, 1, 5) == (prefix..".id ") then
		for i,player in pairs(GetPlayer(string.sub(msg, 6))) do
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = player.UserId.." ID";
			Text = "Account ID of "..player.Name;
			})
		end
	end
	if string.sub(msg, 1, 7) == (prefix.."gameid") then
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Game ID";
		Text = "Game ID: ".. game.GameId;
		})
	end
	if string.sub(msg, 1, 4) == (prefix.."pgs") then
		local pgscheck = game:GetService("Workspace"):PGSIsEnabled()
		if pgscheck == true then
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "PGSPhysicsSolverEnabled";
			Text = "PGS is Enabled!";
			})
		else
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "PGSPhysicsSolverEnabled";
			Text = "PGS is Disabled!";
			})
		end
	end
	if string.sub(msg, 1, 12) == (prefix.."removeinvis") then
		for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
			if v:IsA("Part") then
				if v.Transparency == 1 then
					if v.Name ~= "HumanoidRootPart" then
						v:Destroy()
					end
				end
			end
		end
	end
	if string.sub(msg, 1, 10) == (prefix.."removefog") then
		game:GetService("Lighting").FogStart = 0
		game:GetService("Lighting").FogEnd = 9999999999999
	end
	if string.sub(msg, 1, 8) == (prefix.."disable") then
		lplayer.Character.Humanoid.Parent = lplayer
	end
	if string.sub(msg, 1, 7) == (prefix.."enable") then
		lplayer.Humanoid.Parent = lplayer.Character
	end
	if string.sub(msg, 1, 8) == (prefix.."prefix ") then
		prefix = (string.sub(msg, 9, 9))
		wait(0.1)
		change()
		wait(0.1)
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Prefix changed!";
		Text = "Prefix is now "..prefix..". Use ;resetprefix to reset to ;";
		})
	end
	if string.sub(msg, 1, 12) == (";resetprefix") then
		prefix = ";"
		wait(0.1)
		change()
		wait(0.1)
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "Prefix changed!";
		Text = "Prefix is now "..prefix..". Make sure it's one key!";
		})
	end
	if string.sub(msg, 1, 10) == (prefix.."flyspeed ") then
		speedfly = string.sub(msg, 11)
		wait()
		change()
	end
	if string.sub(msg, 1, 8) == (prefix.."carpet ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
			local Anim3 = Instance.new("Animation")
			Anim3.AnimationId = "rbxassetid://282574440"
			local track3 = lplayer.Character.Humanoid:LoadAnimation(Anim3)
			track3:Play(.1, 1, 1)
			bplrr = v.Name
			banpl = true
		end
	end
	if string.sub(msg, 1, 9) == (prefix.."uncarpet") then
		banpl = false
	end
	if string.sub(msg, 1, 7) == (prefix.."stare ") then
		for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
			staring = true
			stareplr = v
		end
	end
	if string.sub(msg, 1, 8) == (prefix.."unstare") then
		staring = false
	end
	if string.sub(msg, 1, 8) == (prefix.."logchat") then
		chatlogs = true
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "LogChat enabled";
		Text = "Now logging all player chat.";
		})
	end
	if string.sub(msg, 1, 10) == (prefix.."unlogchat") then
		chatlogs = false
		game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "LogChat disabled";
		Text = "Stopped logging all player chat.";
		})
	end
	if string.sub(msg, 1, 7) == (prefix.."fixcam") then
		game:GetService("Workspace").CurrentCamera:Destroy()
		wait(0.1)
		game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Humanoid
		game:GetService("Workspace").CurrentCamera.CameraType = "Custom"
		lplayer.CameraMinZoomDistance = 0.5
		lplayer.CameraMaxZoomDistance = 400
		lplayer.CameraMode = "Classic"
	end
	if string.sub(msg, 1, 8) == (prefix.."unstate") then
		changingstate = false
	end
end)

local function tp()
	for i, player in ipairs(game:GetService("Players"):GetPlayers()) do
		if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
			if player.Name == brplr then
				player.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame + lplayer.Character.HumanoidRootPart.CFrame.lookVector * 2
			end
		end
	end
end
local function tpall()
	for i, player in ipairs(game:GetService("Players"):GetPlayers()) do
		if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
			player.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame + lplayer.Character.HumanoidRootPart.CFrame.lookVector * 3
		end
	end
end
spawn(function()
	while wait(spamdelay) do
		if spamming == true then
			game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(spamtext, "All")
		end
	end
end)
spawn(function()
	while wait(spamdelay) do
		if spammingpm == true then
			game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("/w "..pmspammed.." @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@", "All")
		end
	end
end)
spawn(function()
	while wait() do
		if cbring == true then
			tp()
		end
	end
end)
spawn(function()
	while wait() do
		if cbringall == true then
			tpall()
		end
	end
end)

Mouse.KeyDown:connect(function(Key)
	if Key == prefix then
		CMDBAR:CaptureFocus()
	end
end)

CMDBAR.FocusLost:connect(function(enterPressed)
	if enterPressed then
		if string.sub(CMDBAR.Text, 1, 5) == ("kill ") then
			if string.sub(CMDBAR.Text, 6) == "me" then
				lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(100000,0,100000)
			else
				for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6)))do
					local NOW = lplayer.Character.HumanoidRootPart.CFrame
					lplayer.Character.Humanoid.Name = 1
					local l = lplayer.Character["1"]:Clone()
					l.Parent = lplayer.Character
					l.Name = "Humanoid"
					wait(0.1)
					lplayer.Character["1"]:Destroy()
					game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
					lplayer.Character.Animate.Disabled = true
					wait(0.1)
					lplayer.Character.Animate.Disabled = false
					lplayer.Character.Humanoid.DisplayDistanceType = "None"
					for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
					lplayer.Character.Humanoid:EquipTool(v)
					end
					local function tp(player,player2)
					local char1,char2=player.Character,player2.Character
					if char1 and char2 then
					char1:MoveTo(char2.Head.Position)
					end
					end
					wait(0.1)
					lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
					wait(0.2)
					lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
					wait(0.5)
					lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(-100000,10,-100000))
					wait(0.7)
					tp(lplayer,game:GetService("Players")[v.Name])
					wait(0.7)
					lplayer.Character.HumanoidRootPart.CFrame = NOW
					game:GetService("StarterGui"):SetCore("SendNotification", {
					Title = "Tools needed!";
					Text = "You need a tool in your backpack for this command!";
					})
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("bring ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7)))do
				local NOW = lplayer.Character.HumanoidRootPart.CFrame
				lplayer.Character.Humanoid.Name = 1
				local l = lplayer.Character["1"]:Clone()
				l.Parent = lplayer.Character
				l.Name = "Humanoid"
				wait(0.1)
				lplayer.Character["1"]:Destroy()
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
				lplayer.Character.Animate.Disabled = true
				wait(0.1)
				lplayer.Character.Animate.Disabled = false
				lplayer.Character.Humanoid.DisplayDistanceType = "None"
				for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
				lplayer.Character.Humanoid:EquipTool(v)
				end
				local function tp(player,player2)
				local char1,char2=player.Character,player2.Character
				if char1 and char2 then
				char1.HumanoidRootPart.CFrame = char2.HumanoidRootPart.CFrame
				end
				end
				local function getout(player,player2)
				local char1,char2=player.Character,player2.Character
				if char1 and char2 then
				char1:MoveTo(char2.Head.Position)
				end
				end
				tp(game:GetService("Players")[v.Name], lplayer)
				wait(0.2)
				tp(game:GetService("Players")[v.Name], lplayer)
				wait(0.5)
				lplayer.Character.HumanoidRootPart.CFrame = NOW
				wait(0.5)
				getout(lplayer, game:GetService("Players")[v.Name])
				wait(0.3)
				lplayer.Character.HumanoidRootPart.CFrame = NOW
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "Tools needed!";
				Text = "You need a tool in your backpack for this command!";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("spin ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
				lplayer.Character.Humanoid.Name = 1
				local l = lplayer.Character["1"]:Clone()
				l.Parent = lplayer.Character
				l.Name = "Humanoid"
				wait(0.1)
				lplayer.Character["1"]:Destroy()
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
				lplayer.Character.Animate.Disabled = true
				wait(0.1)
				lplayer.Character.Animate.Disabled = false
				lplayer.Character.Humanoid.DisplayDistanceType = "None"
				for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
				lplayer.Character.Humanoid:EquipTool(v)
				end
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
				spinplr = v
				wait(0.5)
				spin = true
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "Tools needed!";
				Text = "You need a tool in your backpack for this command!";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("unspin") then
			spin = false
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("attach ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
				lplayer.Character.Humanoid.Name = 1
				local l = lplayer.Character["1"]:Clone()
				l.Parent = lplayer.Character
				l.Name = "Humanoid"
				wait(0.1)
				lplayer.Character["1"]:Destroy()
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
				lplayer.Character.Animate.Disabled = true
				wait(0.1)
				lplayer.Character.Animate.Disabled = false
				lplayer.Character.Humanoid.DisplayDistanceType = "None"
				for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
				lplayer.Character.Humanoid:EquipTool(v)
				end
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
				wait(0.3)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
				attplr = v
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "Tools needed!";
				Text = "You need a tool in your backpack for this command!";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("unattach ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 10))) do
				local function getout(player,player2)
				local char1,char2=player.Character,player2.Character
				if char1 and char2 then
				char1:MoveTo(char2.Head.Position)
				end
				end
				getout(lplayer, game:GetService("Players")[v.Name])
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("follow ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
				followed = true
				flwplr = v
			end
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("unfollow") then
			followed = false
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("freefall ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 10))) do
				local NOW = lplayer.Character.HumanoidRootPart.CFrame
				lplayer.Character.Humanoid.Name = 1
				local l = lplayer.Character["1"]:Clone()
				l.Parent = lplayer.Character
				l.Name = "Humanoid"
				wait(0.1)
				lplayer.Character["1"]:Destroy()
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
				lplayer.Character.Animate.Disabled = true
				wait(0.1)
				lplayer.Character.Animate.Disabled = false
				lplayer.Character.Humanoid.DisplayDistanceType = "None"
				for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
				lplayer.Character.Humanoid:EquipTool(v)
				end
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.2)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.6)
				lplayer.Character.HumanoidRootPart.CFrame = NOW
				wait(0.6)
				lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(0,50000,0)
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "Tools needed!";
				Text = "You need a tool in your backpack for this command!";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("trail ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
				traill = true
				trlplr = v
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("untrail") then
			traill = false
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("orbit ") then
			if string.sub(CMDBAR.Text, 7) == "all" or string.sub(CMDBAR.Text, 7) == "others" or string.sub(CMDBAR.Text, 7) == "me" then
				lplayer.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame
			else
				for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
					local o = Instance.new("RocketPropulsion")
					o.Parent = lplayer.Character.HumanoidRootPart
					o.Name = "Orbit"
					o.Target = game:GetService("Players")[v.Name].Character.HumanoidRootPart
					o:Fire()
					noclip = true
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("unorbit") then
			lplayer.Character.HumanoidRootPart.Orbit:Destroy()
			noclip = false
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("fling ") then
			if string.sub(CMDBAR.Text, 7) == "all" or string.sub(CMDBAR.Text, 7) == "others" or string.sub(CMDBAR.Text, 7) == "me" then
				lplayer.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame
			else
				for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
					local y = Instance.new("RocketPropulsion")
					y.Parent = lplayer.Character.HumanoidRootPart
					y.CartoonFactor = 1
					y.MaxThrust = 800000
					y.MaxSpeed = 1000
					y.ThrustP = 200000
					y.Name = "Fling"
					game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Head
					y.Target = game:GetService("Players")[v.Name].Character.HumanoidRootPart
					y:Fire()
					noclip = true
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("unfling") then
			noclip = false
			lplayer.Character.HumanoidRootPart.Fling:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Head
			wait(0.4)
			lplayer.Character.HumanoidRootPart.Fling:Destroy()
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("fecheck") then
			if game:GetService("Workspace").FilteringEnabled == true then
				warn("FE is Enabled (Filtering Enabled)")
				game:GetService("StarterGui"):SetCore("SendNotification", {
					Title = "FE is Enabled";
					Text = "Filtering Enabled. Enjoy using Reviz Admin!";
				})
			else
				warn("FE is Disabled (Filtering Disabled) Consider using a different admin script.")
				game:GetService("StarterGui"):SetCore("SendNotification", {
					Title = "FE is Disabled";
					Text = "Filtering Disabled. Consider using a different admin script.";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("void ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
				lplayer.Character.Humanoid.Name = 1
				local l = lplayer.Character["1"]:Clone()
				l.Parent = lplayer.Character
				l.Name = "Humanoid"
				wait(0.1)
				lplayer.Character["1"]:Destroy()
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
				lplayer.Character.Animate.Disabled = true
				wait(0.1)
				lplayer.Character.Animate.Disabled = false
				lplayer.Character.Humanoid.DisplayDistanceType = "None"
				for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
				lplayer.Character.Humanoid:EquipTool(v)
				end
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.2)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.6)
				lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(999999999999999,0,999999999999999)
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "Tools needed!";
				Text = "You need a tool in your backpack for this command!";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("noclip") then
			noclip = true
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Noclip enabled";
			Text = "Type ;clip to disable";
			})
		end
		if string.sub(CMDBAR.Text, 1, 4) == ("clip") then
			noclip = false
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Noclip disabled";
			Text = "Type ;noclip to enable";
			})
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("speed ") then
			lplayer.Character.Humanoid.WalkSpeed = (string.sub(CMDBAR.Text, 7))
		end
		if string.sub(CMDBAR.Text, 1, 3) == ("ws ") then
			lplayer.Character.Humanoid.WalkSpeed = (string.sub(CMDBAR.Text, 4))
		end
		if string.sub(CMDBAR.Text, 1, 10) == ("hipheight ") then
			lplayer.Character.Humanoid.HipHeight = (string.sub(CMDBAR.Text, 11))
		end
		if string.sub(CMDBAR.Text, 1, 3) == ("hh ") then
			lplayer.Character.Humanoid.HipHeight = (string.sub(CMDBAR.Text, 4))
		end
		if string.sub(CMDBAR.Text, 1, 10) == ("jumppower ") then
			lplayer.Character.Humanoid.JumpPower = (string.sub(CMDBAR.Text, 11))
		end
		if string.sub(CMDBAR.Text, 1, 3) == ("jp ") then
			lplayer.Character.Humanoid.JumpPower = (string.sub(CMDBAR.Text, 4))
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("default") then
			lplayer.Character.Humanoid.JumpPower = 50
			lplayer.Character.Humanoid.WalkSpeed = 16
			lplayer.Character.Humanoid.HipHeight = 0
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("annoy ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
				annoying = true
				annplr = v
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("unannoy") then
			annoying = false
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("headwalk ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 10))) do
				hwalk = true
				hdwplr = v
			end
		end
		if string.sub(CMDBAR.Text, 1, 10) == ("unheadwalk") then
			hwalk = false
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("nolimbs") then
			lplayer.Character["Left Leg"]:Destroy()
			lplayer.Character["Left Arm"]:Destroy()
			lplayer.Character["Right Leg"]:Destroy()
			lplayer.Character["Right Arm"]:Destroy()
		end
		if string.sub(CMDBAR.Text, 1, 3) == ("god") then
			lplayer.Character.Humanoid.Name = 1
			local l = lplayer.Character["1"]:Clone()
			l.Parent = lplayer.Character
			l.Name = "Humanoid"
			wait(0.1)
			lplayer.Character["1"]:Destroy()
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
			lplayer.Character.Animate.Disabled = true
			wait(0.1)
			lplayer.Character.Animate.Disabled = false
			lplayer.Character.Humanoid.DisplayDistanceType = "None"
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "FE Godmode enabled";
			Text = "Use ;grespawn or ;respawn to remove.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("drophats") then
			for i,v in pairs(lplayer.Character:GetChildren()) do
				if (v:IsA("Accessory")) or (v:IsA("Hat")) then
					v.Parent = workspace
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("droptool") then
			for i,v in pairs(lplayer.Character:GetChildren()) do
				if (v:IsA("Tool")) then
					v.Parent = workspace
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("loopdhats") then
			droppinghats = true
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Loop Drop Enabled";
			Text = "Type ;unloopdhats to disable";
			})
		end
		if string.sub(CMDBAR.Text, 1, 11) == ("unloopdhats") then
			droppinghats = false
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Loop Drop Disabled";
			Text = "Type ;loopdhats to enable.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("loopdtool") then
			droppingtools = true
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Loop Drop Enabled";
			Text = "Type ;unloopdtool to disable";
			})
		end
		if string.sub(CMDBAR.Text, 1, 11) == ("unloopdtool") then
			droppingtools = false
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Loop Drop Disabled";
			Text = "Type ;loopdtool to enable.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("invisible") then -- Credit to Timeless
			Local = game:GetService('Players').LocalPlayer
			Char  = Local.Character
			touched,tpdback = false, false
			box = Instance.new('Part',workspace)
			box.Anchored = true
			box.CanCollide = true
			box.Size = Vector3.new(10,1,10)
			box.Position = Vector3.new(0,10000,0)
			box.Touched:connect(function(part)
			    if (part.Parent.Name == Local.Name) then
			        if touched == false then
			            touched = true
			            function apply()
			                if script.Disabled ~= true then
			                    no = Char.HumanoidRootPart:Clone()
			                    wait(.25)
			                    Char.HumanoidRootPart:Destroy()
			                    no.Parent = Char
			                    Char:MoveTo(loc)
			                    touched = false
			                end end
			            if Char then
			                apply()
			            end
			        end
			    end
			end)
			repeat wait() until Char
			loc = Char.HumanoidRootPart.Position
			Char:MoveTo(box.Position + Vector3.new(0,.5,0))
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Invisibility enabled!";
			Text = "Reset or use ;respawn to remove.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("view ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
				if game:GetService("Players")[v.Name].Character.Humanoid then
					game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Humanoid
				else
					game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Head
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("unview") then
			if lplayer.Character.Humanoid then
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Humanoid
			else
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Head
			end
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("goto ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			end
		end
		if string.sub(CMDBAR.Text, 1, 3) == ("fly") then
		repeat wait() until lplayer and lplayer.Character and lplayer.Character:FindFirstChild('HumanoidRootPart') and lplayer.Character:FindFirstChild('Humanoid')
		repeat wait() until Mouse
		
		local T = lplayer.Character.HumanoidRootPart
		local CONTROL = {F = 0, B = 0, L = 0, R = 0}
		local lCONTROL = {F = 0, B = 0, L = 0, R = 0}
		local SPEED = speedget
		
		local function fly()
			flying = true
			local BG = Instance.new('BodyGyro', T)
			local BV = Instance.new('BodyVelocity', T)
			BG.P = 9e4
			BG.maxTorque = Vector3.new(9e9, 9e9, 9e9)
			BG.cframe = T.CFrame
			BV.velocity = Vector3.new(0, 0.1, 0)
			BV.maxForce = Vector3.new(9e9, 9e9, 9e9)
			spawn(function()
			repeat wait()
			lplayer.Character.Humanoid.PlatformStand = true
			if CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0 then
			SPEED = 50
			elseif not (CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0) and SPEED ~= 0 then
			SPEED = 0
			end
			if (CONTROL.L + CONTROL.R) ~= 0 or (CONTROL.F + CONTROL.B) ~= 0 then
			BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (CONTROL.F + CONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(CONTROL.L + CONTROL.R, (CONTROL.F + CONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
			lCONTROL = {F = CONTROL.F, B = CONTROL.B, L = CONTROL.L, R = CONTROL.R}
			elseif (CONTROL.L + CONTROL.R) == 0 and (CONTROL.F + CONTROL.B) == 0 and SPEED ~= 0 then
			BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (lCONTROL.F + lCONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(lCONTROL.L + lCONTROL.R, (lCONTROL.F + lCONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
			else
			BV.velocity = Vector3.new(0, 0.1, 0)
			end
			BG.cframe = workspace.CurrentCamera.CoordinateFrame
					until not flying
					CONTROL = {F = 0, B = 0, L = 0, R = 0}
					lCONTROL = {F = 0, B = 0, L = 0, R = 0}
					SPEED = 0
					BG:destroy()
					BV:destroy()
					lplayer.Character.Humanoid.PlatformStand = false
				end)
			end
		Mouse.KeyDown:connect(function(KEY)
			if KEY:lower() == 'w' then
				CONTROL.F = speedfly
			elseif KEY:lower() == 's' then
				CONTROL.B = -speedfly
			elseif KEY:lower() == 'a' then
				CONTROL.L = -speedfly 
			elseif KEY:lower() == 'd' then 
				CONTROL.R = speedfly
			end
		end)
		Mouse.KeyUp:connect(function(KEY)
			if KEY:lower() == 'w' then
				CONTROL.F = 0
			elseif KEY:lower() == 's' then
				CONTROL.B = 0
			elseif KEY:lower() == 'a' then
				CONTROL.L = 0
			elseif KEY:lower() == 'd' then
				CONTROL.R = 0
			end
		end)
		fly()
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("unfly") then
			flying = false
			lplayer.Character.Humanoid.PlatformStand = false
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("chat ") then
			game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer((string.sub(CMDBAR.Text, 6)), "All")
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("spam ") then
			spamtext = (string.sub(CMDBAR.Text, 6))
			spamming = true
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("unspam") then
			spamming = false
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("spamwait ") then
			spamdelay = (string.sub(CMDBAR.Text, 10))
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("pmspam ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
				pmspammed = v.Name
				spammingpm = true
			end
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("unpmspam") then
			spammingpm = false
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("cfreeze ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 9))) do
				v.Character["Left Leg"].Anchored = true
				v.Character["Left Arm"].Anchored = true
				v.Character["Right Leg"].Anchored = true
				v.Character["Right Arm"].Anchored = true
				v.Character.Torso.Anchored = true
				v.Character.Head.Anchored = true
			end
		end
		if string.sub(CMDBAR.Text, 1, 10) == ("uncfreeze ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 11))) do
				v.Character["Left Leg"].Anchored = false
				v.Character["Left Arm"].Anchored = false
				v.Character["Right Leg"].Anchored = false
				v.Character["Right Arm"].Anchored = false
				v.Character.Torso.Anchored = false
				v.Character.Head.Anchored = false
			end
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("unlockws") then
			local a = game:GetService("Workspace"):getChildren()
			for i = 1, #a do
				if a[i].className == "Part" then
					a[i].Locked = false
				elseif a[i].className == "Model" then
					local r = a[i]:getChildren()
					for i = 1, #r do
						if r[i].className == "Part" then
						r[i].Locked = false
						end
					end
				end
			end
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Success!";
			Text = "Workspace unlocked. Use ;lockws to lock.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("lockws") then
			local a = game:GetService("Workspace"):getChildren()
			for i = 1, #a do
				if a[i].className == "Part" then
					a[i].Locked = true
				elseif a[i].className == "Model" then
					local r = a[i]:getChildren()
					for i = 1, #r do
						if r[i].className == "Part" then
						r[i].Locked = true
						end
					end
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("btools") then
			local Clone_T = Instance.new("HopperBin",lplayer.Backpack)
			Clone_T.BinType = "Clone"
			local Destruct = Instance.new("HopperBin",lplayer.Backpack)
			Destruct.BinType = "Hammer"
			local Hold_T = Instance.new("HopperBin",lplayer.Backpack)
			Hold_T.BinType = "Grab"
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("pstand") then
			lplayer.Character.Humanoid.PlatformStand = true
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("unpstand") then
			lplayer.Character.Humanoid.PlatformStand = false
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("blockhead") then
			lplayer.Character.Head.Mesh:Destroy()
		end
		if string.sub(CMDBAR.Text, 1, 3) == ("sit") then
			lplayer.Character.Humanoid.Sit = true
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("bringobj ") then
			local function bringobjw()
			for i,obj in ipairs(game:GetService("Workspace"):GetDescendants()) do
			if obj.Name == (string.sub(CMDBAR.Text, 10)) then
			obj.CFrame = lplayer.Character.HumanoidRootPart.CFrame
			obj.CanCollide = false
			obj.Transparency = 0.7
			wait()
			obj.CFrame = lplayer.Character["Left Leg"].CFrame
			wait()
			obj.CFrame = lplayer.Character["Right Leg"].CFrame
			wait()
			obj.CFrame = lplayer.Character["Head"].CFrame
			end
			end
			end
			while wait() do
				bringobjw()
			end
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "BringObj";
			Text = "BringObj enabled.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("wsvis ") then
			vis = (string.sub(CMDBAR.Text, 7))
			local a = game:GetService("Workspace"):GetDescendants()
			for i = 1, #a do
				if a[i].className == "Part" then
					a[i].Transparency = vis
				elseif a[i].className == "Model" then
					local r = a[i]:getChildren()
					for i = 1, #r do
						if r[i].className == "Part" then
						r[i].Transparency = vis
						end
					end
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 10) == ("hypertotal") then
			loadstring(game:GetObjects("rbxassetid://1255063809")[1].Source)()
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Success!";
			Text = "HyperTotal GUI Loaded!";
			})
		end
		if string.sub(CMDBAR.Text, 1, 4) == ("cmds") then
			CMDSFRAME.Visible = true
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("rmeshhats") then
			for i,v in pairs(lplayer.Character:GetChildren()) do
				if (v:IsA("Accessory")) or (v:IsA("Hat")) then
					v.Handle.Mesh:Destroy()
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("blockhats") then
			for i,v in pairs(lplayer.Character:GetChildren()) do
				if (v:IsA("Accessory")) or (v:IsA("Hat")) then
					v.Handle.Mesh:Destroy()
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("rmeshtool") then
			for i,v in pairs(lplayer.Character:GetChildren()) do
				if (v:IsA("Tool")) then
					v.Handle.Mesh:Destroy()
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("blocktool") then
			for i,v in pairs(lplayer.Character:GetChildren()) do
				if (v:IsA("Tool")) then
					v.Handle.Mesh:Destroy()
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("spinner") then
			local p = Instance.new("RocketPropulsion")
			p.Parent = lplayer.Character.HumanoidRootPart
			p.Name = "Spinner"
			p.Target = lplayer.Character["Left Arm"]
			p:Fire()
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Spinner enabled";
			Text = "Type ;nospinner to disable.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("nospinner") then
			lplayer.Character.HumanoidRootPart.Spinner:Destroy()
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("reachd") then
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
				if v:isA("Tool") then
					local a = Instance.new("SelectionBox",v.Handle)
					a.Adornee = v.Handle
					v.Handle.Size = Vector3.new(0.5,0.5,60)
					v.GripPos = Vector3.new(0,0,0)
					lplayer.Character.Humanoid:UnequipTools()
				end
			end
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Reach applied!";
			Text = "Applied to equipped sword. Use ;noreach to disable.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("reach ") then
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
				if v:isA("Tool") then
					local a = Instance.new("SelectionBox",v.Handle)
					a.Name = "Reach"
					a.Adornee = v.Handle
					v.Handle.Size = Vector3.new(0.5,0.5,(string.sub(CMDBAR.Text, 7)))
					v.GripPos = Vector3.new(0,0,0)
					lplayer.Character.Humanoid:UnequipTools()
				end
			end
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Reach applied!";
			Text = "Applied to equipped sword. Use ;noreach to disable.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("noreach") then
			for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
				if v:isA("Tool") then
					v.Handle.Reach:Destroy()
				end
			end
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Reach removed!";
			Text = "Removed reach from equipped sword.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("rkill ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7)))do
				lplayer.Character.Humanoid.Name = 1
				local l = lplayer.Character["1"]:Clone()
				l.Parent = lplayer.Character
				l.Name = "Humanoid"
				wait(0.1)
				lplayer.Character["1"]:Destroy()
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
				lplayer.Character.Animate.Disabled = true
				wait(0.1)
				lplayer.Character.Animate.Disabled = false
				lplayer.Character.Humanoid.DisplayDistanceType = "None"
				for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
				lplayer.Character.Humanoid:EquipTool(v)
				end
				wait(0.1)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.2)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.5)
				lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(-100000,10,-100000))
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "Tools needed!";
				Text = "You need a tool in your backpack for this command!";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("tp me ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("cbring ") then
			if (string.sub(CMDBAR.Text, 8)) == "all" or (string.sub(CMDBAR.Text, 8)) == "All" or (string.sub(CMDBAR.Text, 8)) == "ALL" then
				cbringall = true
			else
				for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
					brplr = v.Name
				end
			end
			cbring = true
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("uncbring") then
			cbring = false
			cbringall = false
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("swap ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
				local NOWPLR = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				local NOW = lplayer.Character.HumanoidRootPart.CFrame
				lplayer.Character.Humanoid.Name = 1
				local l = lplayer.Character["1"]:Clone()
				l.Parent = lplayer.Character
				l.Name = "Humanoid"
				wait(0.1)
				lplayer.Character["1"]:Destroy()
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
				lplayer.Character.Animate.Disabled = true
				wait(0.1)
				lplayer.Character.Animate.Disabled = false
				lplayer.Character.Humanoid.DisplayDistanceType = "None"
				for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
				lplayer.Character.Humanoid:EquipTool(v)
				end
				local function tp(player,player2)
				local char1,char2=player.Character,player2.Character
				if char1 and char2 then
				char1:MoveTo(char2.Head.Position)
				end
				end
				wait(0.1)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.2)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
				wait(0.5)
				lplayer.Character.HumanoidRootPart.CFrame = NOW
				wait(0.6)
				tp(lplayer, game:GetService("Players")[v.Name])
				wait(0.4)
				lplayer.Character.HumanoidRootPart.CFrame = NOWPLR
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "Tools needed!";
				Text = "You need a tool in your backpack for this command!";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("glitch ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
				lplayer.Character.Humanoid.Name = 1
				local l = lplayer.Character["1"]:Clone()
				l.Parent = lplayer.Character
				l.Name = "Humanoid"
				wait(0.1)
				lplayer.Character["1"]:Destroy()
				game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
				lplayer.Character.Animate.Disabled = true
				wait(0.1)
				lplayer.Character.Animate.Disabled = false
				lplayer.Character.Humanoid.DisplayDistanceType = "None"
				for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
				lplayer.Character.Humanoid:EquipTool(v)
				end
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
				wait(0.3)
				lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
				wait(0.4)
				b = Instance.new("BodyForce")
				b.Parent = lplayer.Character.HumanoidRootPart
				b.Name = "Glitch"
				b.Force = Vector3.new(100000000,5000,0)
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "Tools needed!";
				Text = "You need a tool in your backpack for this command!";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("unglitch") then
			lplayer.Character.HumanoidRootPart.Glitch:Destroy()
			lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(10000,0,10000)
			b = Instance.new("BodyForce")
			b.Parent = lplayer.Character.HumanoidRootPart
			b.Name = "unGlitch"
			b.Force = Vector3.new(0,-5000000,0)
			wait(2)
			lplayer.Character.HumanoidRootPart.unGlitch:Destroy()
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("grespawn") then
			lplayer.Character.Humanoid.Health = 0
			wait(1)
			lplayer.Character.Head.CFrame = CFrame.new(1000000,0,1000000)
			lplayer.Character.Torso.CFrame = CFrame.new(1000000,0,1000000)
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("explorer") then
			loadstring(game:GetObjects("rbxassetid://492005721")[1].Source)()
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Success!";
			Text = "DEX Explorer has loaded.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("anim ") then
			local Anim = Instance.new("Animation")
			Anim.AnimationId = "rbxassetid://"..(string.sub(CMDBAR.Text, 6))
			local track = lplayer.Character.Humanoid:LoadAnimation(Anim)
			track:Play(.1, 1, 1)
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("animgui") then
			loadstring(game:GetObjects("rbxassetid://1202558084")[1].Source)()
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Success!";
			Text = "Energize Animations GUI has loaded.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("savepos") then
			saved = lplayer.Character.HumanoidRootPart.CFrame
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Position Saved";
			Text = "Use ;loadpos to return to saved position.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("loadpos") then
			lplayer.Character.HumanoidRootPart.CFrame = saved
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("bang ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
				local Anim2 = Instance.new("Animation")
				Anim2.AnimationId = "rbxassetid://148840371"
				local track2 = lplayer.Character.Humanoid:LoadAnimation(Anim2)
				track2:Play(.1, 1, 1)
				bplrr = v.Name
				banpl = true
			end
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("unbang") then
			banpl = false
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("bringmod ") then
			local function bringmodw()
			for i,obj in ipairs(game:GetService("Workspace"):GetDescendants()) do
			if obj.Name == (string.sub(CMDBAR.Text, 10)) then
			for i,ch in pairs(obj:GetDescendants()) do
			if (ch:IsA("BasePart")) then
			ch.CFrame = lplayer.Character.HumanoidRootPart.CFrame
			ch.CanCollide = false
			ch.Transparency = 0.7
			wait()
			ch.CFrame = lplayer.Character["Left Leg"].CFrame
			wait()
			ch.CFrame = lplayer.Character["Right Leg"].CFrame
			wait()
			ch.CFrame = lplayer.Character["Head"].CFrame
			end
			end
			end
			end
			end
			while wait() do
				bringmodw()
			end
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "BringMod";
			Text = "BringMod enabled.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("respawn") then
			local mod = Instance.new('Model', workspace) mod.Name = 're '..lplayer.Name
			local hum = Instance.new('Humanoid', mod)
			local ins = Instance.new('Part', mod) ins.Name = 'Torso' ins.CanCollide = false ins.Transparency = 1
			lplayer.Character = mod
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("shutdown") then
			game:GetService'RunService'.Stepped:Connect(function()
			pcall(function()
			    for i,v in pairs(game:GetService'Players':GetPlayers()) do
			        if v.Character ~= nil and v.Character:FindFirstChild'Head' then
			            for _,x in pairs(v.Character.Head:GetChildren()) do
			                if x:IsA'Sound' then x.Playing = true x.CharacterSoundEvent:FireServer(true, true) end
			            end
			        end
			    end
			end)
			end)
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Attempting Shutdown";
			Text = "Shutdown Attempt has begun.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("delobj ") then
			objtodel = (string.sub(CMDBAR.Text, 8))
			for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
				if v.Name == objtodel then
					v:Destroy()
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("getplrs") then
			for i,v in pairs(game:GetService("Players"):GetPlayers())do
				print(v)
			end
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Printed";
			Text = "Players have been printed to console. (F9)";
			})
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("deldecal") then
			for i,v in pairs(game:GetService("Workspace"):GetDescendants())do
				if (v:IsA("Decal")) then
					v:Destroy()
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 10) == ("opfinality") then
			loadstring(game:GetObjects("rbxassetid://1294358929")[1].Source)()
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Success!";
			Text = "OpFinality GUI has loaded.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("remotes") then
			remotes = true
			added = true
			game.DescendantAdded:connect(function(rmt)
			if added == true then
			if remotes == true then 
			if rmt:IsA("RemoteEvent") then
			print("A RemoteEvent was added!")
			print(" game." .. rmt:GetFullName() .. " | RemoteEvent")
			print(" game." .. rmt:GetFullName() .. " | RemoteEvent", 247, 0, 0, true)
			end end end
			end)
			game.DescendantAdded:connect(function(rmtfnctn)
			if added == true then
			if remotes == true then 
			if rmtfnctn:IsA("RemoteFunction") then
			warn("A RemoteFunction was added!")
			warn(" game." .. rmtfnctn:GetFullName() .. " | RemoteFunction")
			print(" game." .. rmtfnctn:GetFullName() .. " | RemoteFunction", 5, 102, 198, true)
			end end end
			end)
			
			game.DescendantAdded:connect(function(bndfnctn)
			if added == true then
			if binds == true then 
			if bndfnctn:IsA("BindableFunction") then
			print("A BindableFunction was added!")
			print(" game." .. bndfnctn:GetFullName() .. " | BindableFunction")
			print(" game." .. bndfnctn:GetFullName() .. " | BindableFunction", 239, 247, 4, true)
			end end end
			end)
			
			game.DescendantAdded:connect(function(bnd)
			if added == true then
			if binds == true then 
			if bnd:IsA("BindableEvent") then
			warn("A BindableEvent was added!")
			warn(" game." .. bnd:GetFullName() .. " | BindableEvent")
			print(" game." .. bnd:GetFullName() .. " | BindableEvent", 13, 193, 22, true)
			end end end
			end)
			
			
			if binds == true then
			for i,v in pairs(game:GetDescendants()) do
			if v:IsA("BindableFunction") then
			print(" game." .. v:GetFullName() .. " | BindableFunction")
			print(" game." .. v:GetFullName() .. " | BindableFunction", 239, 247, 4, true)
			end end
			for i,v in pairs(game:GetDescendants()) do
			if v:IsA("BindableEvent") then
			warn(" game." .. v:GetFullName() .. " | BindableEvent")
			print(" game." .. v:GetFullName() .. " | BindableEvent", 13, 193, 22, true)
			end end
			else
			print("Off")
			end
			if remotes == true then
			for i,v in pairs(game:GetDescendants()) do
			if v:IsA("RemoteFunction") then
			warn(" game." .. v:GetFullName() .. " | RemoteFunction")
			print(" game." .. v:GetFullName() .. " | RemoteFunction", 5, 102, 198, true)
			end end
			wait()
			for i,v in pairs(game:GetDescendants()) do
			if v:IsA("RemoteEvent") then
			print(" game." .. v:GetFullName() .. " | RemoteEvent")
			print(" game." .. v:GetFullName() .. " | RemoteEvent", 247, 0, 0, true)
			end end
			else
			print("Off")
			end
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Printing Remotes";
			Text = "Type ;noremotes to disable.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("noremotes") then
			remotes = false
			added = false
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Printing Remotes Disabled";
			Text = "Type ;remotes to enable.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("tpdefault") then
			spin = false
			followed = false
			traill = false
			noclip = false
			annoying = false
			hwalk = false
			cbringing = false
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("stopsit") then
			stopsitting = true
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("gosit") then
			stopsitting = false
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("version") then
			print(adminversion)
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Version";
			Text = adminversion;
			})
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("clicktp") then
			clickgoto = true
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Click TP";
			Text = "Press E to teleport to mouse position";
			})
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("noclicktp") then
			clickgoto = false
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Click TP";
			Text = "Click TP has been disabled.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("toolson") then
			gettingtools = true
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools Enabled";
			Text = "Automatically colleting tools dropped.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("toolsoff") then
			gettingtools = false
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Tools Disabled";
			Text = "Click TP has been disabled.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("delcmdbar") then
			ScreenGui:Destroy()
		end
		if string.sub(CMDBAR.Text, 1, 5) == ("reset") then
			lplayer.Character.Head:Destroy()
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("state ") then
			statechosen = string.sub(CMDBAR.Text, 7)
			changingstate = true
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("gravity ") then
			game:GetService("Workspace").Gravity = string.sub(CMDBAR.Text, 9)
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("looprhats") then
		removingmeshhats = true
		end
		if string.sub(CMDBAR.Text, 1, 11) == ("unlooprhats") then
			removingmeshhats = false
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("looprtool") then
			removingmeshtool = true
		end
		if string.sub(CMDBAR.Text, 1, 11) == ("unlooprtool") then
			removingmeshtool = false
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("givetool ") then
			for i,v in pairs(game:GetService("Players").LocalPlayer.Character:GetDescendants()) do
				if v:IsA("Tool") then
					for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 10))) do
						v.Parent = player.Character
					end
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 4) == ("age ") then
			for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 5))) do
				game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(player.Name.." Account Age: "..player.AccountAge.." days!", "All")
			end
		end
		if string.sub(CMDBAR.Text, 1, 3) == ("id ") then
			for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 4))) do
				game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(player.Name.." Account ID: "..player.UserId, "All")
			end
		end
		if string.sub(CMDBAR.Text, 1, 5) == (".age ") then
			for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = player.AccountAge.." Days";
				Text = "Account age of "..player.Name;
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 4) == (".id ") then
			for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 5))) do
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = player.UserId.." ID";
				Text = "Account ID of "..player.Name;
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("gameid") then
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "Game ID";
			Text = "Game ID: ".. game.GameId;
			})
		end
		if string.sub(CMDBAR.Text, 1, 3) == ("pgs") then
			local pgscheck = game:GetService("Workspace"):PGSIsEnabled()
			if pgscheck == true then
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "PGSPhysicsSolverEnabled";
				Text = "PGS is Enabled!";
				})
			else
				game:GetService("StarterGui"):SetCore("SendNotification", {
				Title = "PGSPhysicsSolverEnabled";
				Text = "PGS is Disabled!";
				})
			end
		end
		if string.sub(CMDBAR.Text, 1, 11) == ("removeinvis") then
			for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
				if v:IsA("Part") then
					if v.Transparency == 1 then
						if v.Name ~= "HumanoidRootPart" then
							v:Destroy()
						end
					end
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("removefog") then
			game:GetService("Lighting").FogStart = 0
			game:GetService("Lighting").FogEnd = 9999999999999
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("disable") then
			lplayer.Character.Humanoid.Parent = lplayer
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("enable") then
			lplayer.Humanoid.Parent = lplayer.Character
		end
		if string.sub(CMDBAR.Text, 1, 13) == ("givealltools ") then
			for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetDescendants()) do
				if v:IsA("Tool") then
					v.Parent = lplayer.Character
					wait()
					for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 14))) do
						v.Parent = player.Character
					end
				end
			end
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("flyspeed ") then
			speedfly = string.sub(CMDBAR.Text, 10)
			wait()
			change()
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("carpet ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
				local Anim3 = Instance.new("Animation")
				Anim3.AnimationId = "rbxassetid://282574440"
				local track3 = lplayer.Character.Humanoid:LoadAnimation(Anim3)
				track3:Play(.1, 1, 1)
				bplrr = v.Name
				banpl = true
			end
		end
		if string.sub(CMDBAR.Text, 1, 8) == ("uncarpet") then
			banpl = false
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("stare ") then
			for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
				staring = true
				stareplr = v
			end
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("unstare") then
			staring = false
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("logchat") then
			chatlogs = true
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "LogChat enabled";
			Text = "Now logging all player chat.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 9) == ("unlogchat") then
			chatlogs = false
			game:GetService("StarterGui"):SetCore("SendNotification", {
			Title = "LogChat disabled";
			Text = "Stopped logging all player chat.";
			})
		end
		if string.sub(CMDBAR.Text, 1, 6) == ("fixcam") then
			game:GetService("Workspace").CurrentCamera:Destroy()
			wait(0.1)
			game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Humanoid
			game:GetService("Workspace").CurrentCamera.CameraType = "Custom"
			lplayer.CameraMinZoomDistance = 0.5
			lplayer.CameraMaxZoomDistance = 400
			lplayer.CameraMode = "Classic"
		end
		if string.sub(CMDBAR.Text, 1, 7) == ("unstate") then
			changingstate = false
		end
		CMDBAR.Text = ""
	end
end)

wait(0.3)
game:GetService("StarterGui"):SetCore("SendNotification", {
	Title = "Loaded successfully!";
	Text = "Reviz Admin V2 by illremember";
})
wait(0.1)
print("Reviz Admin V2 loaded!")
if game:GetService("Workspace").FilteringEnabled == true then
	warn("FE is Enabled (Filtering Enabled)")
	game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "FE is Enabled";
		Text = "Filtering Enabled. Enjoy using Reviz Admin!";
	})
else
	warn("FE is Disabled (Filtering Disabled) Consider using a different admin script.")
	game:GetService("StarterGui"):SetCore("SendNotification", {
		Title = "FE is Disabled";
		Text = "Filtering Disabled. Consider using a different admin script.";
	})
end

local intro = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local ImageLabel = Instance.new("ImageLabel")
intro.Parent = game:GetService("CoreGui")
Frame.Parent = intro
Frame.BackgroundColor3 = Color3.new(1, 1, 1)
Frame.BackgroundTransparency = 1
Frame.Size = UDim2.new(1, 0, 0, 300)
Frame.Position = UDim2.new(0, 0, -0.4, 0)
ImageLabel.Parent = Frame
ImageLabel.BackgroundColor3 = Color3.new(1, 1, 1)
ImageLabel.BackgroundTransparency = 1
ImageLabel.Position = UDim2.new(0, 0, 0, 0)
ImageLabel.Size = UDim2.new(1, 0, 1, 0)
ImageLabel.Image = "http://www.roblox.com/asset/?id=1542162618"
Frame:TweenPosition(UDim2.new(0, 0, 0.2, 0), "Out", "Elastic", 3)
wait(3.01)
Frame:TweenPosition(UDim2.new(0, 0, 1.5, 0), "Out", "Elastic", 5)
wait(5.01)
intro:Destroy()
end)

OtherSection:NewButton("DarkDex [KRNL]", "DarkDex [KRNL VERSIOn]", function()
    -- Cloneref support (adds support for JJsploit/Temple/Electron and other sploits that don't have cloneref or really shit versions of it.)
loadstring(game:HttpGet("https://raw.githubusercontent.com/Babyhamsta/RBLX_Scripts/main/Universal/CloneRef.lua", true))()

-- Dex Bypasses
loadstring(game:HttpGet("https://raw.githubusercontent.com/Babyhamsta/RBLX_Scripts/main/Universal/Bypasses.lua", true))()

-- Dex with CloneRef Support (made as global)
getgenv().Bypassed_Dex = game:GetObjects("rbxassetid://9352453730")[1]

local charset = {}
for i = 48,  57 do table.insert(charset, string.char(i)) end
for i = 65,  90 do table.insert(charset, string.char(i)) end
for i = 97, 122 do table.insert(charset, string.char(i)) end
function RandomCharacters(length)
    if length > 0 then
        return RandomCharacters(length - 1) .. charset[math.random(1, #charset)]
    else
        return ""
    end
end

Bypassed_Dex.Name = RandomCharacters(math.random(5, 20))
if gethui then
    Bypassed_Dex.Parent = gethui();
elseif syn and syn.protect_gui then
    syn.protect_gui(Bypassed_Dex);
    Bypassed_Dex.Parent = cloneref(game:GetService("CoreGui"))
else
    Bypassed_Dex.Parent = cloneref(game:GetService("CoreGui"))
end

local function Load(Obj, Url)
    local function GiveOwnGlobals(Func, Script)
        local Fenv = {}
        local RealFenv = {script = Script}
        local FenvMt = {}
        function FenvMt:__index(b)
            if RealFenv[b] == nil then
                return getfenv()[b]
            else
                return RealFenv[b]
            end
        end
        function FenvMt:__newindex(b, c)
            if RealFenv[b] == nil then
                getfenv()[b] = c
            else
                RealFenv[b] = c
            end
        end
        setmetatable(Fenv, FenvMt)
        setfenv(Func, Fenv)
        return Func
    end
    
    local function LoadScripts(Script)
        if Script.ClassName == "Script" or Script.ClassName == "LocalScript" then
            task.spawn(GiveOwnGlobals(loadstring(Script.Source, "=" .. Script:GetFullName()), Script))
        end
        for _,v in ipairs(Script:GetChildren()) do
            LoadScripts(v)
        end
    end
    
    LoadScripts(Obj)
end

Load(Bypassed_Dex)
end)

OtherSection:NewButton("Ingame AutoClicker", "F5 To Enable F6 To Disable", function()
    local on
local keybind=Enum.KeyCode.F5
local keybindEnd=Enum.KeyCode.F6
local UserInputService=game:GetService("UserInputService")
local RunService=game:GetService("RunService")
local plr=game:GetService("Players").LocalPlayer
local mouse=plr:GetMouse()

local sg=Instance.new("ScreenGui",plr.PlayerGui)
local f=Instance.new("TextLabel",sg)
f.Size=UDim2.new(0,25,0,10)
f.BackgroundColor3=Color3.fromRGB(180,50,50)
f.Visible=false
f.Text="On"
f.TextSize=11

local vu = game:GetService("VirtualUser")
local function CC()
vu:CaptureController();
end 
local function CB()
local v2 = Vector2.new();
vu:ClickButton1(v2);
end

function Start(a,b)
   if a.KeyCode==keybind then
       on=true
       a=RunService.Stepped:Connect(function()
           if on then
               CC();
               CB();
               f.Visible=true
               f.Position=UDim2.new(0,mouse.X-12.5,0,mouse.Y-15)
           else
               a:Disconnect()
           end
       end)
       f.Visible=false
   end
end

function Stop(a,b)
   if a.KeyCode==keybindEnd then
       on=false
       f.Visible=false
   end
end

UserInputService.InputBegan:connect(Start)
UserInputService.InputEnded:connect(Stop)
end)

OtherSection:NewButton("Remote Spy", "...", function()
    -- Made by Butterfly
-- FrontEnd // UI

-- Objects

local RemoteSpy = Instance.new("ScreenGui")
local BG = Instance.new("Frame")
local Ribbon = Instance.new("ImageLabel")
local Hide = Instance.new("TextButton")
local Title = Instance.new("TextLabel")
local Remotes = Instance.new("ScrollingFrame")
local Source = Instance.new("ScrollingFrame")
local ButtonsFrame = Instance.new("ScrollingFrame")
local ToClipboard = Instance.new("TextButton")
local Decompile = Instance.new("TextButton")
local GetReturn = Instance.new("TextButton")
local ClearList = Instance.new("TextButton")
local CryptStrings = Instance.new("TextButton")
local EnableSpy = Instance.new("TextButton")
local Total = Instance.new("TextLabel")
local Settings = Instance.new("TextButton")
local SetRemotes = Instance.new("ScrollingFrame")
local Storage = Instance.new("Frame")
local RBTN = Instance.new("TextButton")
local Icon = Instance.new("ImageLabel")
local RemoteName = Instance.new("TextLabel")
local ID = Instance.new("TextLabel")
local SBTN = Instance.new("TextButton")
local Icon_2 = Instance.new("ImageLabel")
local RemoteName_2 = Instance.new("TextLabel")
local ScriptLine = Instance.new("Frame")
local Line = Instance.new("TextLabel")
local SourceText = Instance.new("TextLabel")
local Tokens = Instance.new("TextLabel")
local Strings = Instance.new("TextLabel")
local Comments = Instance.new("TextLabel")
local Keywords = Instance.new("TextLabel")
local Globals = Instance.new("TextLabel")
local RemoteHighlight = Instance.new("TextLabel")
local Enabled = Instance.new("TextLabel")
local FullScreen = Instance.new("TextButton")
--local Exit = Instance.new("TextButton")
local SetRemotesTab = Instance.new("Frame")
local FilterF = Instance.new("TextButton")
local FilterE = Instance.new("TextButton")
local Search = Instance.new("TextBox")
local lvl6Frame = Instance.new("Frame")
local lvl6Output = Instance.new("ScrollingFrame")
local lvl6Source = Instance.new("ScrollingFrame")
local Source_ = Instance.new("TextBox")
local Comments_ = Instance.new("TextLabel")
local Globals_ = Instance.new("TextLabel")
local Keywords_ = Instance.new("TextLabel")
local RemoteHighlight_ = Instance.new("TextLabel")
local SourceText_ = Instance.new("TextLabel")
local Strings_ = Instance.new("TextLabel")
local Tokens_ = Instance.new("TextLabel")
local ClearScript = Instance.new("TextButton")
local ExecuteScript = Instance.new("TextButton")
local Resize = Instance.new("TextButton")
local lvl6 = Instance.new("TextButton")
local ClearOutput = Instance.new("TextButton")
local Label = Instance.new("TextLabel")
local Lines = Instance.new("TextLabel")
local Mute = Instance.new("TextButton")
local Icon_3 = Instance.new("ImageLabel")
local RemoteButtons = Instance.new("ScrollingFrame")
local FireRemote = Instance.new("TextButton")
local FireDelay = Instance.new("TextBox")
local LoopFire = Instance.new("TextButton")
local FireAmount = Instance.new("TextBox")
local Break = Instance.new("TextButton")
local WhileLoopFire = Instance.new("TextButton")
local remotes_fired = 0
local last_bg_pos
local LoadSource = Instance.new("TextButton")
local Refresh = Instance.new("TextButton")
local encrypt_string = false
local spy_enabled = true

local lua_keywords = {"and", "break", "do", "else", "elseif", "end", "false", "for", "function", "goto", "if", "in", "local", "nil", "not", "or", "repeat", "return", "then", "true", "until", "while"}
local global_env = {"getrawmetatable", "game", "workspace", "script", "math", "string", "table", "print", "wait", "BrickColor", "Color3", "next", "pairs", "ipairs", "select", "unpack", "Instance", "Vector2", "Vector3", "CFrame", "Ray", "UDim2", "Enum", "assert", "error", "warn", "tick", "loadstring", "_G", "shared", "getfenv", "setfenv", "newproxy", "setmetatable", "getmetatable", "os", "debug", "pcall", "ypcall", "xpcall", "rawequal", "rawset", "rawget", "tonumber", "tostring", "type", "typeof", "_VERSION", "coroutine", "delay", "require", "spawn", "LoadLibrary", "settings", "stats", "time", "UserSettings", "version", "Axes", "ColorSequence", "Faces", "ColorSequenceKeypoint", "NumberRange", "NumberSequence", "NumberSequenceKeypoint", "gcinfo", "elapsedTime", "collectgarbage", "PhysicalProperties", "Rect", "Region3", "Region3int16", "UDim", "Vector2int16", "Vector3int16"}

-- Sounds

local logSound = Instance.new("Sound")
local topPress = Instance.new("Sound")
local errorSound = Instance.new("Sound")
local openSound = Instance.new("Sound")
local disableSound = Instance.new("Sound")

local sounds = {logSound, topPress, errorSound, openSound, disableSound}

-- Properties

RemoteSpy.Name = "RemoteSpy"
RemoteSpy.Parent = game.CoreGui

logSound.SoundId = "rbxassetid://917942453"

errorSound.SoundId = "rbxassetid://582374365"

topPress.SoundId = "rbxassetid://558993260"

openSound.SoundId = "rbxassetid://472556995"

disableSound.SoundId = "rbxassetid://550209561"

BG.Name = "BG"
BG.Parent = RemoteSpy
--BG.Active = true
BG.BackgroundColor3 = Color3.new(0.141176, 0.141176, 0.141176)
BG.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
--BG.Draggable = true
BG.Position = UDim2.new(0.5, -700, 0.5, -400)
BG.Size = UDim2.new(1, -300, 1, -200)
BG.ClipsDescendants = true

Ribbon.Name = "Ribbon"
Ribbon.Parent = BG
Ribbon.BackgroundColor3 = Color3.new(0.760784, 0.0117647, 0.317647)
Ribbon.BorderSizePixel = 0
Ribbon.Size = UDim2.new(1, 0, 0, 20)
Ribbon.ZIndex = 2

Hide.Name = "Hide"
Hide.Parent = Ribbon
Hide.BackgroundColor3 = Color3.new(1, 0, 0)
Hide.BorderSizePixel = 0
Hide.Position = UDim2.new(1, -40, 0, 0)
Hide.Size = UDim2.new(0, 40, 0, 20)
Hide.ZIndex = 3
Hide.Font = Enum.Font.SourceSansBold
Hide.FontSize = Enum.FontSize.Size14
Hide.Text = "_"
Hide.TextColor3 = Color3.new(1, 1, 1)
Hide.TextSize = 14

Title.Name = "Title"
Title.Parent = Ribbon
Title.BackgroundColor3 = Color3.new(1, 0.0117647, 0.423529)
Title.BorderSizePixel = 0
Title.Position = UDim2.new(0.5, -100, 0, 0)
Title.Size = UDim2.new(0, 200, 0, 20)
Title.ZIndex = 3
Title.Font = Enum.Font.SourceSansBold
Title.FontSize = Enum.FontSize.Size14
Title.Text = "Remote2Script v2 R3.4"
Title.TextColor3 = Color3.new(1, 1, 1)
Title.TextSize = 14

Remotes.Name = "Remotes"
Remotes.Parent = BG
Remotes.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Remotes.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
Remotes.Position = UDim2.new(0, 10, 0, 80)
Remotes.CanvasSize = UDim2.new(0, 0, 40, 0)
Remotes.Size = UDim2.new(0, 250, 1, -90)
Remotes.ZIndex = 2
Remotes.BottomImage = "rbxassetid://148970562"
Remotes.MidImage = "rbxassetid://148970562"
Remotes.ScrollBarThickness = 5
Remotes.TopImage = "rbxassetid://148970562"

Source.Name = "Source"
Source.Parent = BG
Source.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Source.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
Source.Position = UDim2.new(0, 270, 0, 80)
Source.Size = UDim2.new(1, -280, 1, -140)
Source.ZIndex = 2
Source.BottomImage = "rbxassetid://148970562"
Source.CanvasSize = UDim2.new(3, 0, 160, 0)
Source.MidImage = "rbxassetid://148970562"
Source.ScrollBarThickness = 5
Source.TopImage = "rbxassetid://148970562"

ButtonsFrame.Name = "ButtonsFrame"
ButtonsFrame.Parent = BG
ButtonsFrame.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
ButtonsFrame.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
ButtonsFrame.Position = UDim2.new(0, 10, 0, 30)
ButtonsFrame.Size = UDim2.new(1, -20, 0, 40)
ButtonsFrame.ZIndex = 2
ButtonsFrame.ClipsDescendants = true
ButtonsFrame.CanvasSize = UDim2.new(2, 0, 0, 0)
ButtonsFrame.ScrollBarThickness = 5
ButtonsFrame.BottomImage = "rbxassetid://148970562"
ButtonsFrame.TopImage = "rbxassetid://148970562"
ButtonsFrame.MidImage = "rbxassetid://148970562"

ToClipboard.Name = "ToClipboard"
ToClipboard.Parent = ButtonsFrame
ToClipboard.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
ToClipboard.BorderColor3 = Color3.new(0.117647, 0.392157, 0.117647)
ToClipboard.Position = UDim2.new(0, 10, 0.5, -10)
ToClipboard.Size = UDim2.new(0, 100, 0, 20)
ToClipboard.ZIndex = 3
ToClipboard.Font = Enum.Font.SourceSansBold
ToClipboard.FontSize = Enum.FontSize.Size14
ToClipboard.Text = "COPY"
ToClipboard.TextColor3 = Color3.new(0.235294, 0.784314, 0.235294)
ToClipboard.TextSize = 14

Decompile.Name = "Decompile"
Decompile.Parent = ButtonsFrame
Decompile.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Decompile.BorderColor3 = Color3.new(0.384314, 0.384314, 0.384314)
Decompile.Position = UDim2.new(0, 120, 0.5, -10)
Decompile.Size = UDim2.new(0, 100, 0, 20)
Decompile.ZIndex = 3
Decompile.Font = Enum.Font.SourceSansBold
Decompile.FontSize = Enum.FontSize.Size14
Decompile.Text = "DECOMPILE"
Decompile.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
Decompile.TextSize = 14

GetReturn.Name = "GetReturn"
GetReturn.Parent = ButtonsFrame
GetReturn.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
GetReturn.BorderColor3 = Color3.new(0.384314, 0.384314, 0.384314)
GetReturn.Position = UDim2.new(0, 230, 0.5, -10)
GetReturn.Size = UDim2.new(0, 100, 0, 20)
GetReturn.ZIndex = 3
GetReturn.Font = Enum.Font.SourceSansBold
GetReturn.FontSize = Enum.FontSize.Size14
GetReturn.Text = "GET RETURN"
GetReturn.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
GetReturn.TextSize = 14

ClearList.Name = "ClearList"
ClearList.Parent = ButtonsFrame
ClearList.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
ClearList.BorderColor3 = Color3.new(0.384314, 0.384314, 0.384314)
ClearList.Position = UDim2.new(0, 340, 0.5, -10)
ClearList.Size = UDim2.new(0, 100, 0, 20)
ClearList.ZIndex = 3
ClearList.Font = Enum.Font.SourceSansBold
ClearList.FontSize = Enum.FontSize.Size14
ClearList.Text = "CLEAR LOGS"
ClearList.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
ClearList.TextSize = 14

CryptStrings.Name = "CryptStrings"
CryptStrings.Parent = ButtonsFrame
CryptStrings.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
CryptStrings.BorderColor3 = Color3.new(0.392157, 0.117647, 0.117647)
CryptStrings.Position = UDim2.new(0, 450, 0.5, -10)
CryptStrings.Size = UDim2.new(0, 100, 0, 20)
CryptStrings.ZIndex = 3
CryptStrings.Font = Enum.Font.SourceSansBold
CryptStrings.FontSize = Enum.FontSize.Size14
CryptStrings.Text = "CRYPT STRINGS"
CryptStrings.TextColor3 = Color3.new(0.784314, 0.235294, 0.235294)
CryptStrings.TextSize = 14

EnableSpy.Name = "EnableSpy"
EnableSpy.Parent = ButtonsFrame
EnableSpy.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
EnableSpy.BorderColor3 = Color3.fromRGB(30, 100, 30)
EnableSpy.Position = UDim2.new(0, 560, 0.5, -10)
EnableSpy.Size = UDim2.new(0, 100, 0, 20)
EnableSpy.ZIndex = 3
EnableSpy.Font = Enum.Font.SourceSansBold
EnableSpy.FontSize = Enum.FontSize.Size14
EnableSpy.Text = "REMOTESPY"
EnableSpy.TextColor3 = Color3.fromRGB(60, 200, 60)
EnableSpy.TextSize = 14

Total.Name = "Total"
Total.Parent = ButtonsFrame
Total.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Total.BorderColor3 = Color3.new(0.384314, 0.384314, 0.384314)
Total.Position = UDim2.new(0, 780, 0.5, -10)
Total.Size = UDim2.new(0, 50, 0, 20)
Total.ZIndex = 3
Total.Font = Enum.Font.SourceSansBold
Total.FontSize = Enum.FontSize.Size14
Total.Text = "0"
Total.TextColor3 = Color3.new(1, 1, 1)
Total.TextSize = 14
Total.TextWrapped = true

Settings.Name = "Settings"
Settings.Parent = ButtonsFrame
Settings.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Settings.BorderColor3 = Color3.new(0.117647, 0.392157, 0.392157)
Settings.Position = UDim2.new(0, 670, 0.5, -10)
Settings.Size = UDim2.new(0, 100, 0, 20)
Settings.ZIndex = 3
Settings.Font = Enum.Font.SourceSansBold
Settings.FontSize = Enum.FontSize.Size14
Settings.Text = "REMOTES"
Settings.TextColor3 = Color3.new(0.235294, 0.784314, 0.784314)
Settings.TextSize = 14

SetRemotes.Name = "SetRemotes"
SetRemotes.Parent = BG
SetRemotes.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
SetRemotes.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
SetRemotes.Position = UDim2.new(0, 270, 0, 80)
SetRemotes.Size = UDim2.new(1, -280, 1, -140)
SetRemotes.Visible = false
SetRemotes.ZIndex = 2
SetRemotes.BottomImage = "rbxassetid://148970562"
SetRemotes.CanvasSize = UDim2.new(0, 0, 25, 0)
SetRemotes.MidImage = "rbxassetid://148970562"
SetRemotes.ScrollBarThickness = 5
SetRemotes.TopImage = "rbxassetid://148970562"

Storage.Name = "Storage"
Storage.Parent = RemoteSpy
Storage.BackgroundColor3 = Color3.new(1, 1, 1)
Storage.Size = UDim2.new(0, 100, 0, 100)
Storage.Visible = false

RBTN.Name = "RBTN"
RBTN.Parent = Storage
RBTN.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
RBTN.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
RBTN.Position = UDim2.new(0, 10, 0, 10)
RBTN.Size = UDim2.new(1, -20, 0, 20)
RBTN.ZIndex = 3
RBTN.Font = Enum.Font.SourceSansBold
RBTN.FontSize = Enum.FontSize.Size14
RBTN.Text = ""
RBTN.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
RBTN.TextSize = 14
RBTN.TextXAlignment = Enum.TextXAlignment.Left

Icon.Name = "Icon"
Icon.Parent = RBTN
Icon.BackgroundColor3 = Color3.new(1, 1, 1)
Icon.BackgroundTransparency = 1
Icon.Size = UDim2.new(0, 20, 0, 20)
Icon.ZIndex = 4
Icon.Image = "rbxassetid://413369506"

print(Icon:GetFullName())

RemoteName.Name = "RemoteName"
RemoteName.Parent = RBTN
RemoteName.BackgroundColor3 = Color3.new(0.713726, 0.00392157, 0.298039)
RemoteName.BorderSizePixel = 0
RemoteName.Position = UDim2.new(0, 30, 0, 0)
RemoteName.Size = UDim2.new(0, 140, 0, 20)
RemoteName.ZIndex = 4
RemoteName.Font = Enum.Font.SourceSansBold
RemoteName.FontSize = Enum.FontSize.Size14
RemoteName.Text = "10"
RemoteName.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
RemoteName.TextSize = 14

ID.Name = "ID"
ID.Parent = RBTN
ID.BackgroundColor3 = Color3.new(0.458824, 0.00392157, 0.192157)
ID.BorderSizePixel = 0
ID.Position = UDim2.new(1, -50, 0, 0)
ID.Size = UDim2.new(0, 50, 0, 20)
ID.ZIndex = 4
ID.Font = Enum.Font.SourceSansBold
ID.FontSize = Enum.FontSize.Size14
ID.Text = "10"
ID.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
ID.TextSize = 14

SBTN.Name = "SBTN"
SBTN.Parent = Storage
SBTN.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
SBTN.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
SBTN.Position = UDim2.new(0, 10, 0, 10)
SBTN.Size = UDim2.new(1, -20, 0, 20)
SBTN.ZIndex = 3
SBTN.Font = Enum.Font.SourceSansBold
SBTN.FontSize = Enum.FontSize.Size14
SBTN.Text = ""
SBTN.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
SBTN.TextSize = 11
SBTN.TextXAlignment = Enum.TextXAlignment.Left

Icon_2.Name = "Icon"
Icon_2.Parent = SBTN
Icon_2.BackgroundColor3 = Color3.new(1, 1, 1)
Icon_2.BackgroundTransparency = 1
Icon_2.Size = UDim2.new(0, 20, 0, 20)
Icon_2.ZIndex = 4
Icon_2.Image = "rbxassetid://413369506"

print(Icon_2:GetFullName())

RemoteName_2.Name = "RemoteName"
RemoteName_2.Parent = SBTN
RemoteName_2.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
RemoteName_2.BorderSizePixel = 1
RemoteName_2.BorderColor3 = Color3.fromRGB(62, 62, 62)
RemoteName_2.Position = UDim2.new(0, 30, 0, 0)
RemoteName_2.Size = UDim2.new(0, 140, 0, 20)
RemoteName_2.ZIndex = 4
RemoteName_2.Font = Enum.Font.SourceSansBold
RemoteName_2.FontSize = Enum.FontSize.Size14
RemoteName_2.Text = "SayMessageRequest"
RemoteName_2.TextColor3 = Color3.fromRGB(200, 200, 200)
RemoteName_2.TextSize = 11


ScriptLine.Name = "ScriptLine"
ScriptLine.Parent = Storage
ScriptLine.BackgroundColor3 = Color3.new(1, 1, 1)
ScriptLine.BackgroundTransparency = 1
ScriptLine.Size = UDim2.new(1, 0, 0, 17)
ScriptLine.ZIndex = 2

Line.Name = "Line"
Line.Parent = ScriptLine
Line.BackgroundColor3 = Color3.new(0.329412, 0, 0)
Line.BackgroundTransparency = 1
Line.BorderSizePixel = 0
Line.Size = UDim2.new(0, 40, 1, 0)
Line.ZIndex = 3
Line.Font = Enum.Font.SourceSansBold
Line.FontSize = Enum.FontSize.Size18
Line.Text = ""
Line.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
Line.TextSize = 17

SourceText.Name = "SourceText"
SourceText.Parent = ScriptLine
SourceText.BackgroundColor3 = Color3.new(1, 1, 1)
SourceText.BackgroundTransparency = 1
SourceText.Position = UDim2.new(0, 40, 0, 0)
SourceText.Size = UDim2.new(1, -40, 1, 0)
SourceText.ZIndex = 3
SourceText.Font = Enum.Font.Code
SourceText.FontSize = Enum.FontSize.Size18
SourceText.Text = ""
SourceText.TextColor3 = Color3.new(1, 1, 1)
SourceText.TextSize = 17
SourceText.TextXAlignment = Enum.TextXAlignment.Left

Tokens.Name = "Tokens"
Tokens.Parent = ScriptLine
Tokens.BackgroundColor3 = Color3.new(1, 1, 1)
Tokens.BackgroundTransparency = 1
Tokens.Position = UDim2.new(0, 40, 0, 0)
Tokens.Size = UDim2.new(1, -40, 1, 0)
Tokens.ZIndex = 3
Tokens.Font = Enum.Font.Code
Tokens.FontSize = Enum.FontSize.Size18
Tokens.Text = ""
Tokens.TextColor3 = Color3.new(0.392157, 0.392157, 0.392157)
Tokens.TextSize = 17
Tokens.TextXAlignment = Enum.TextXAlignment.Left

Strings.Name = "Strings"
Strings.Parent = ScriptLine
Strings.BackgroundColor3 = Color3.new(1, 1, 1)
Strings.BackgroundTransparency = 1
Strings.Position = UDim2.new(0, 40, 0, 0)
Strings.Size = UDim2.new(1, -40, 1, 0)
Strings.ZIndex = 5
Strings.Font = Enum.Font.Code
Strings.FontSize = Enum.FontSize.Size18
Strings.Text = ""
Strings.TextColor3 = Color3.new(1, 0.615686, 0)
Strings.TextSize = 17
Strings.TextXAlignment = Enum.TextXAlignment.Left

Comments.Name = "Comments"
Comments.Parent = ScriptLine
Comments.BackgroundColor3 = Color3.new(1, 1, 1)
Comments.BackgroundTransparency = 1
Comments.Position = UDim2.new(0, 40, 0, 0)
Comments.Size = UDim2.new(1, -40, 1, 0)
Comments.ZIndex = 5
Comments.Font = Enum.Font.Code
Comments.FontSize = Enum.FontSize.Size18
Comments.Text = ""
Comments.TextColor3 = Color3.fromRGB(60, 200, 60)
Comments.TextSize = 17
Comments.TextXAlignment = Enum.TextXAlignment.Left

RemoteHighlight.Name = "RemoteHighlight"
RemoteHighlight.Parent = ScriptLine
RemoteHighlight.BackgroundColor3 = Color3.new(1, 1, 1)
RemoteHighlight.BackgroundTransparency = 1
RemoteHighlight.Position = UDim2.new(0, 40, 0, 0)
RemoteHighlight.Size = UDim2.new(1, -40, 1, 0)
RemoteHighlight.ZIndex = 3
RemoteHighlight.Font = Enum.Font.Code
RemoteHighlight.FontSize = Enum.FontSize.Size18
RemoteHighlight.Text = ""
RemoteHighlight.TextColor3 = Color3.fromRGB(0, 145, 255)
RemoteHighlight.TextSize = 17
RemoteHighlight.TextXAlignment = Enum.TextXAlignment.Left

Keywords.Name = "Keywords"
Keywords.Parent = ScriptLine
Keywords.BackgroundColor3 = Color3.new(1, 1, 1)
Keywords.BackgroundTransparency = 1
Keywords.Position = UDim2.new(0, 40, 0, 0)
Keywords.Size = UDim2.new(1, -40, 1, 0)
Keywords.ZIndex = 3
Keywords.Font = Enum.Font.Code
Keywords.FontSize = Enum.FontSize.Size18
Keywords.Text = ""
Keywords.TextColor3 = Color3.new(0.231373, 1, 0)
Keywords.TextSize = 17
Keywords.TextXAlignment = Enum.TextXAlignment.Left

Globals.Name = "Globals"
Globals.Parent = ScriptLine
Globals.BackgroundColor3 = Color3.new(1, 1, 1)
Globals.BackgroundTransparency = 1
Globals.Position = UDim2.new(0, 40, 0, 0)
Globals.Size = UDim2.new(1, -40, 1, 0)
Globals.ZIndex = 3
Globals.Font = Enum.Font.Code
Globals.FontSize = Enum.FontSize.Size18
Globals.Text = ""
Globals.TextColor3 = Color3.new(1, 0, 0)
Globals.TextSize = 17
Globals.TextXAlignment = Enum.TextXAlignment.Left

Enabled.Name = "Enabled"
Enabled.Parent = SBTN
Enabled.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
Enabled.BorderSizePixel = 1
Enabled.BorderColor3 = Color3.fromRGB(30, 100, 30)
Enabled.Position = UDim2.new(0, 210, 0, 0)
Enabled.Size = UDim2.new(1, -210, 1, 0)
Enabled.ZIndex = 4
Enabled.Font = Enum.Font.SourceSansBold
Enabled.FontSize = Enum.FontSize.Size14
Enabled.Text = "Enabled"
Enabled.TextColor3 = Color3.fromRGB(60, 200, 60)
Enabled.TextSize = 14

FullScreen.Name = "FullScreen"
FullScreen.Parent = Ribbon
FullScreen.BackgroundColor3 = Color3.new(1, 0, 0)
FullScreen.BorderSizePixel = 0
FullScreen.Position = UDim2.new(1, -90, 0, 0)
FullScreen.Size = UDim2.new(0, 40, 0, 20)
FullScreen.ZIndex = 3
FullScreen.Font = Enum.Font.SourceSansBold
FullScreen.FontSize = Enum.FontSize.Size14
FullScreen.Text = "[~]"
FullScreen.TextColor3 = Color3.new(1, 1, 1)
FullScreen.TextSize = 14

--[[Exit.Name = "Exit"
Exit.Parent = Ribbon
Exit.BackgroundColor3 = Color3.new(1, 0, 0)
Exit.BorderSizePixel = 0
Exit.Position = UDim2.new(1, -140, 0, 0)
Exit.Size = UDim2.new(0, 40, 0, 20)
Exit.ZIndex = 3
Exit.Font = Enum.Font.SourceSansBold
Exit.FontSize = Enum.FontSize.Size14
Exit.Text = "[D]"
Exit.TextColor3 = Color3.new(1, 1, 1)
Exit.TextSize = 14--]]

SetRemotesTab.Name = "SetRemotesTab"
SetRemotesTab.Parent = BG
SetRemotesTab.Visible = false
SetRemotesTab.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
SetRemotesTab.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
SetRemotesTab.ClipsDescendants = true
SetRemotesTab.Position = UDim2.new(0, 270, 1, -50)
SetRemotesTab.Size = UDim2.new(1, -280, 0, 40)
SetRemotesTab.ZIndex = 2

FilterF.Name = "FilterF"
FilterF.Parent = SetRemotesTab
FilterF.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
FilterF.BorderColor3 = Color3.new(0.392157, 0.117647, 0.117647)
FilterF.Position = UDim2.new(0, 120, 0.5, -10)
FilterF.Size = UDim2.new(0, 120, 0, 20)
FilterF.ZIndex = 3
FilterF.Font = Enum.Font.SourceSansBold
FilterF.FontSize = Enum.FontSize.Size14
FilterF.Text = "FILTER FUNCTIONS"
FilterF.TextColor3 = Color3.new(0.784314, 0.235294, 0.235294)
FilterF.TextSize = 14

FilterE.Name = "FilterE"
FilterE.Parent = SetRemotesTab
FilterE.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
FilterE.BorderColor3 = Color3.new(0.392157, 0.117647, 0.117647)
FilterE.Position = UDim2.new(0, 10, 0.5, -10)
FilterE.Size = UDim2.new(0, 100, 0, 20)
FilterE.ZIndex = 3
FilterE.Font = Enum.Font.SourceSansBold
FilterE.FontSize = Enum.FontSize.Size14
FilterE.Text = "FILTER EVENTS"
FilterE.TextColor3 = Color3.new(0.784314, 0.235294, 0.235294)
FilterE.TextSize = 14

Search.Name = "Search"
Search.Parent = SetRemotesTab
Search.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Search.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
Search.Position = UDim2.new(0, 360, 0.5, -10)
Search.Selectable = true
Search.Size = UDim2.new(1, -370, 0, 20)
Search.ZIndex = 3
Search.Font = Enum.Font.SourceSansBold
Search.FontSize = Enum.FontSize.Size14
Search.Text = "[SEARCH]"
Search.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
Search.TextSize = 14

lvl6Output.Name = "lvl6Output"
lvl6Output.Parent = lvl6Frame
lvl6Output.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
lvl6Output.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
lvl6Output.Position = UDim2.new(0, 0, 1, -110)
lvl6Output.Size = UDim2.new(1, 0, 0, 110)
lvl6Output.ZIndex = 3
lvl6Output.CanvasSize = UDim2.new(3, 0, 15, 0)
lvl6Output.BottomImage = "rbxassetid://148970562"
lvl6Output.MidImage = "rbxassetid://148970562"
lvl6Output.ScrollBarThickness = 5
lvl6Output.TopImage = "rbxassetid://148970562"

lvl6Source.Name = "lvl6Source"
lvl6Source.Parent = lvl6Frame
lvl6Source.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
lvl6Source.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
lvl6Source.Position = UDim2.new(0, 0, 0, 30)
lvl6Source.Size = UDim2.new(1, 0, 1, -160)
lvl6Source.ZIndex = 3
lvl6Source.BottomImage = "rbxassetid://148970562"
lvl6Source.CanvasSize = UDim2.new(0, 0, 20, 0)
lvl6Source.MidImage = "rbxassetid://148970562"
lvl6Source.ScrollBarThickness = 5
lvl6Source.TopImage = "rbxassetid://148970562"

Source_.Name = "Source_"
Source_.Parent = lvl6Source
Source_.BackgroundColor3 = Color3.new(1, 1, 1)
Source_.BackgroundTransparency = 1
Source_.Size = UDim2.new(1, 0, 1, 0)
Source_.Position = UDim2.new(0, 30, 0, 0)
Source_.ZIndex = 4
Source_.ClearTextOnFocus = false
Source_.MultiLine = true
Source_.Font = Enum.Font.Code
Source_.FontSize = Enum.FontSize.Size18
Source_.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
Source_.TextSize = 17
Source_.Text = "print(\"Welcome to R2S script editor!\")"
Source_.TextXAlignment = Enum.TextXAlignment.Left
Source_.TextYAlignment = Enum.TextYAlignment.Top

Comments_.Name = "Comments_"
Comments_.Parent = Source_
Comments_.BackgroundColor3 = Color3.new(1, 1, 1)
Comments_.BackgroundTransparency = 1
Comments_.Size = UDim2.new(1, 0, 1, 0)
Comments_.ZIndex = 5
Comments_.Font = Enum.Font.Code
Comments_.FontSize = Enum.FontSize.Size18
Comments_.Text = ""
Comments_.TextColor3 = Color3.new(0.235294, 0.784314, 0.235294)
Comments_.TextSize = 17
Comments_.TextXAlignment = Enum.TextXAlignment.Left
Comments_.TextYAlignment = Enum.TextYAlignment.Top

Globals_.Name = "Globals_"
Globals_.Parent = Source_
Globals_.BackgroundColor3 = Color3.new(1, 1, 1)
Globals_.BackgroundTransparency = 1
Globals_.Size = UDim2.new(1, 0, 1, 0)
Globals_.ZIndex = 5
Globals_.Font = Enum.Font.Code
Globals_.FontSize = Enum.FontSize.Size18
Globals_.Text = ""
Globals_.TextColor3 = Color3.new(1, 0, 0)
Globals_.TextSize = 17
Globals_.TextXAlignment = Enum.TextXAlignment.Left
Globals_.TextYAlignment = Enum.TextYAlignment.Top

Keywords_.Name = "Keywords_"
Keywords_.Parent = Source_
Keywords_.BackgroundColor3 = Color3.new(1, 1, 1)
Keywords_.BackgroundTransparency = 1
Keywords_.Size = UDim2.new(1, 0, 1, 0)
Keywords_.ZIndex = 5
Keywords_.Font = Enum.Font.Code
Keywords_.FontSize = Enum.FontSize.Size18
Keywords_.Text = ""
Keywords_.TextColor3 = Color3.new(0.231373, 1, 0)
Keywords_.TextSize = 17
Keywords_.TextXAlignment = Enum.TextXAlignment.Left
Keywords_.TextYAlignment = Enum.TextYAlignment.Top

RemoteHighlight_.Name = "RemoteHighlight_"
RemoteHighlight_.Parent = Source_
RemoteHighlight_.BackgroundColor3 = Color3.new(1, 1, 1)
RemoteHighlight_.BackgroundTransparency = 1
RemoteHighlight_.Size = UDim2.new(1, 0, 1, 0)
RemoteHighlight_.ZIndex = 5
RemoteHighlight_.Font = Enum.Font.Code
RemoteHighlight_.FontSize = Enum.FontSize.Size18
RemoteHighlight_.Text = ""
RemoteHighlight_.TextColor3 = Color3.new(0, 0.568627, 1)
RemoteHighlight_.TextSize = 17
RemoteHighlight_.TextXAlignment = Enum.TextXAlignment.Left
RemoteHighlight_.TextYAlignment = Enum.TextYAlignment.Top

Strings_.Name = "Strings_"
Strings_.Parent = Source_
Strings_.BackgroundColor3 = Color3.new(1, 1, 1)
Strings_.BackgroundTransparency = 1
Strings_.Size = UDim2.new(1, 0, 1, 0)
Strings_.ZIndex = 5
Strings_.Font = Enum.Font.Code
Strings_.FontSize = Enum.FontSize.Size18
Strings_.Text = ""
Strings_.TextColor3 = Color3.new(1, 0.615686, 0)
Strings_.TextSize = 17
Strings_.TextXAlignment = Enum.TextXAlignment.Left
Strings_.TextYAlignment = Enum.TextYAlignment.Top

Tokens_.Name = "Tokens_"
Tokens_.Parent = Source_
Tokens_.BackgroundColor3 = Color3.new(1, 1, 1)
Tokens_.BackgroundTransparency = 1
Tokens_.Size = UDim2.new(1, 0, 1, 0)
Tokens_.ZIndex = 5
Tokens_.Font = Enum.Font.Code
Tokens_.FontSize = Enum.FontSize.Size18
Tokens_.Text = ""
Tokens_.TextColor3 = Color3.new(0.392157, 0.392157, 0.392157)
Tokens_.TextSize = 17
Tokens_.TextXAlignment = Enum.TextXAlignment.Left
Tokens_.TextYAlignment = Enum.TextYAlignment.Top

ExecuteScript.Name = "ExecuteScript"
ExecuteScript.Parent = lvl6Frame
ExecuteScript.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
ExecuteScript.BorderColor3 = Color3.new(0.117647, 0.392157, 0.117647)
ExecuteScript.Size = UDim2.new(1, -700, 0, 20)
ExecuteScript.ZIndex = 3
ExecuteScript.Font = Enum.Font.SourceSansBold
ExecuteScript.FontSize = Enum.FontSize.Size14
ExecuteScript.Text = "EXECUTE"
ExecuteScript.TextColor3 = Color3.new(0.235294, 0.784314, 0.235294)
ExecuteScript.TextSize = 14

lvl6.Name = "lvl6"
lvl6.Parent = ButtonsFrame
lvl6.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
lvl6.BorderColor3 = Color3.new(0.384314, 0.384314, 0.384314)
lvl6.Position = UDim2.new(0, 840, 0.5, -10)
lvl6.Size = UDim2.new(0, 100, 0, 20)
lvl6.ZIndex = 3
lvl6.Font = Enum.Font.SourceSansBold
lvl6.FontSize = Enum.FontSize.Size14
lvl6.Text = "LVL6 "
lvl6.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
lvl6.TextSize = 14

lvl6Frame.Name = "lvl6Frame"
lvl6Frame.Parent = BG
lvl6Frame.BackgroundColor3 = Color3.new(1, 1, 1)
lvl6Frame.BackgroundTransparency = 1
lvl6Frame.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
lvl6Frame.Position = UDim2.new(0, 270, 0, 80)
lvl6Frame.Size = UDim2.new(1, -280, 1, -90)
lvl6Frame.ZIndex = 2
lvl6Frame.Visible = false

Resize.Name = "Resize"
Resize.Parent = lvl6Frame
Resize.BackgroundColor3 = Color3.new(0.392157, 0.392157, 0.392157)
Resize.BorderSizePixel = 0
Resize.Draggable = true
Resize.Position = UDim2.new(0.5, -50, 1, -130)
Resize.Size = UDim2.new(0, 100, 0, 10)
Resize.ZIndex = 3
Resize.Font = Enum.Font.SourceSans
Resize.FontSize = Enum.FontSize.Size14
Resize.Text = ""
Resize.TextSize = 14

ClearScript.Name = "ClearScript"
ClearScript.Parent = lvl6Frame
ClearScript.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
ClearScript.BorderColor3 = Color3.new(0.392157, 0.117647, 0.117647)
ClearScript.Position = UDim2.new(1, -280, 0, 0)
ClearScript.Size = UDim2.new(0, 280, 0, 20)
ClearScript.ZIndex = 3
ClearScript.Font = Enum.Font.SourceSansBold
ClearScript.FontSize = Enum.FontSize.Size14
ClearScript.Text = "CLEAR"
ClearScript.TextColor3 = Color3.new(0.784314, 0.235294, 0.235294)
ClearScript.TextSize = 14

ClearOutput.Name = "ClearOutput"
ClearOutput.Parent = lvl6Frame
ClearOutput.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
ClearOutput.BorderColor3 = Color3.new(0.392157, 0.117647, 0.117647)
ClearOutput.Position = UDim2.new(1, -680, 0, 0)
ClearOutput.Size = UDim2.new(0, 390, 0, 20)
ClearOutput.ZIndex = 3
ClearOutput.Font = Enum.Font.SourceSansBold
ClearOutput.FontSize = Enum.FontSize.Size14
ClearOutput.Text = "CLEAR OUTPUT"
ClearOutput.TextColor3 = Color3.new(0.784314, 0.235294, 0.235294)
ClearOutput.TextSize = 14

Label.Name = "Label"
Label.Parent = Storage
Label.BackgroundColor3 = Color3.new(1, 1, 1)
Label.BackgroundTransparency = 1
Label.Size = UDim2.new(1, 0, 0, 17)
Label.ZIndex = 4
Label.Font = Enum.Font.Code
Label.FontSize = Enum.FontSize.Size14
Label.TextColor3 = Color3.new(1, 1, 1)
Label.TextSize = 14
Label.TextXAlignment = Enum.TextXAlignment.Left

Lines.Name = "Lines"
Lines.Parent = lvl6Source
Lines.BackgroundColor3 = Color3.new(1, 1, 1)
Lines.BackgroundTransparency = 1
Lines.Size = UDim2.new(0, 30, 1, 0)
Lines.ZIndex = 4
Lines.Font = Enum.Font.Code
Lines.FontSize = Enum.FontSize.Size18
Lines.Text = "1"
Lines.TextColor3 = Color3.new(1, 1, 1)
Lines.TextSize = 17
Lines.TextYAlignment = Enum.TextYAlignment.Top

LoadSource.Name = "LoadSource"
LoadSource.Parent = ButtonsFrame
LoadSource.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
LoadSource.BorderColor3 = Color3.new(0.384314, 0.384314, 0.384314)
LoadSource.Position = UDim2.new(0, 950, 0.5, -10)
LoadSource.Size = UDim2.new(0, 100, 0, 20)
LoadSource.ZIndex = 3
LoadSource.Font = Enum.Font.SourceSansBold
LoadSource.FontSize = Enum.FontSize.Size14
LoadSource.Text = "LOAD"
LoadSource.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
LoadSource.TextSize = 14

Mute.Name = "Mute"
Mute.Parent = ButtonsFrame
Mute.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Mute.BorderColor3 = Color3.fromRGB(30, 100, 30)
Mute.Position = UDim2.new(0, 1060, 0.5, -10)
Mute.Size = UDim2.new(0, 100, 0, 20)
Mute.ZIndex = 3
Mute.Font = Enum.Font.SourceSansBold
Mute.FontSize = Enum.FontSize.Size14
Mute.Text = ""
Mute.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
Mute.TextSize = 14

Icon_3 .Name = "Icon"
Icon_3 .Parent = Mute
Icon_3 .BackgroundColor3 = Color3.new(1, 1, 1)
Icon_3 .BackgroundTransparency = 1
Icon_3 .Position = UDim2.new(0.5, -10, 0, 0)
Icon_3 .Size = UDim2.new(0, 20, 1, 0)
Icon_3 .ZIndex = 4
Icon_3 .Image = "rbxassetid://302250236"
Icon_3 .ImageColor3 = Color3.fromRGB(60, 200, 60)

Refresh.Name = "Refresh"
Refresh.Parent = SetRemotesTab
Refresh.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Refresh.BorderColor3 = Color3.new(0.380392, 0.380392, 0.380392)
Refresh.Position = UDim2.new(0, 250, 0.5, -10)
Refresh.Size = UDim2.new(0, 100, 0, 20)
Refresh.ZIndex = 3
Refresh.Font = Enum.Font.SourceSansBold
Refresh.FontSize = Enum.FontSize.Size14
Refresh.Text = "REFRESH"
Refresh.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
Refresh.TextSize = 14

RemoteButtons.Name = "RemoteButtons"
RemoteButtons.Parent = BG
RemoteButtons.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
RemoteButtons.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
RemoteButtons.Position = UDim2.new(0, 270, 1, -50)
RemoteButtons.Size = UDim2.new(1, -280, 0, 40)
RemoteButtons.ZIndex = 2
RemoteButtons.BottomImage = "rbxassetid://148970562"
RemoteButtons.CanvasSize = UDim2.new(2, 0, 0, 0)
RemoteButtons.MidImage = "rbxassetid://148970562"
RemoteButtons.ScrollBarThickness = 5
RemoteButtons.TopImage = "rbxassetid://148970562"

FireRemote.Name = "FireRemote"
FireRemote.Parent = RemoteButtons
FireRemote.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
FireRemote.BorderColor3 = Color3.new(0.384314, 0.384314, 0.384314)
FireRemote.Position = UDim2.new(0, 10, 0.5, -10)
FireRemote.Size = UDim2.new(0, 100, 0, 20)
FireRemote.ZIndex = 3
FireRemote.Font = Enum.Font.SourceSansBold
FireRemote.FontSize = Enum.FontSize.Size14
FireRemote.Text = "FIRE REMOTE"
FireRemote.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
FireRemote.TextSize = 14

FireDelay.Name = "FireDelay"
FireDelay.Parent = RemoteButtons
FireDelay.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
FireDelay.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
FireDelay.Position = UDim2.new(0, 290, 0.5, -10)
FireDelay.Size = UDim2.new(0, 50, 0, 20)
FireDelay.ZIndex = 3
FireDelay.Font = Enum.Font.SourceSansBold
FireDelay.FontSize = Enum.FontSize.Size14
FireDelay.Text = "0"
FireDelay.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
FireDelay.TextSize = 14

LoopFire.Name = "LoopFire"
LoopFire.Parent = RemoteButtons
LoopFire.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
LoopFire.BorderColor3 = Color3.new(0.384314, 0.384314, 0.384314)
LoopFire.Position = UDim2.new(0, 120, 0.5, -10)
LoopFire.Size = UDim2.new(0, 100, 0, 20)
LoopFire.ZIndex = 3
LoopFire.Font = Enum.Font.SourceSansBold
LoopFire.FontSize = Enum.FontSize.Size14
LoopFire.Text = "FOR-LOOP FIRE"
LoopFire.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
LoopFire.TextSize = 14

FireAmount.Name = "FireAmount"
FireAmount.Parent = RemoteButtons
FireAmount.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
FireAmount.BorderColor3 = Color3.new(0.243137, 0.243137, 0.243137)
FireAmount.Position = UDim2.new(0, 230, 0.5, -10)
FireAmount.Size = UDim2.new(0, 50, 0, 20)
FireAmount.ZIndex = 3
FireAmount.Font = Enum.Font.SourceSansBold
FireAmount.FontSize = Enum.FontSize.Size14
FireAmount.Text = "0"
FireAmount.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
FireAmount.TextSize = 14

Break.Name = "Break"
Break.Parent = RemoteButtons
Break.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Break.BorderColor3 = Color3.new(0.392157, 0.117647, 0.117647)
Break.Position = UDim2.new(0, 350, 0.5, -10)
Break.Size = UDim2.new(0, 100, 0, 20)
Break.ZIndex = 3
Break.Font = Enum.Font.SourceSansBold
Break.FontSize = Enum.FontSize.Size14
Break.Text = "BREAK"
Break.TextColor3 = Color3.new(0.784314, 0.235294, 0.235294)
Break.TextSize = 14

WhileLoopFire.Name = "WhileLoopFire"
WhileLoopFire.Parent = RemoteButtons
WhileLoopFire.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
WhileLoopFire.BorderColor3 = Color3.new(0.384314, 0.384314, 0.384314)
WhileLoopFire.Position = UDim2.new(0, 460, 0.5, -10)
WhileLoopFire.Size = UDim2.new(0, 100, 0, 20)
WhileLoopFire.ZIndex = 3
WhileLoopFire.Font = Enum.Font.SourceSansBold
WhileLoopFire.FontSize = Enum.FontSize.Size14
WhileLoopFire.Text = "INF-LOOP FIRE"
WhileLoopFire.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
WhileLoopFire.TextSize = 14

local Mouse = game.Players.LocalPlayer:GetMouse()
local UIS = game:GetService('UserInputService')
local RS = game:GetService('RunService')
local canDrag = false

local function MakeDraggable(panel, handle)
    handle.MouseEnter:connect(function()
        canDrag = true
    end)
    handle.MouseLeave:connect(function()
        canDrag = false
    end)
    Mouse.Button1Down:connect(function()
        if canDrag then
            panel.Position = UDim2.new(0, Mouse.X + (Mouse.X - panel.AbsolutePosition.X), 0, Mouse.Y + (Mouse.Y - panel.AbsolutePosition.Y))
            local pX = Mouse.X - panel.AbsolutePosition.X
            local pY = Mouse.Y - panel.AbsolutePosition.Y
            repeat RS.RenderStepped:wait()
                panel.Position = UDim2.new(0, Mouse.X + pX, 0, Mouse.Y + pY)
            until not UIS:IsMouseButtonPressed(Enum.UserInputType.MouseButton1)
        end
    end)
end

MakeDraggable(BG, BG)

-- FrontEnd-Backend // UI Functions

local playSound = function(sound, int)
	spawn(function()
		local s = sound:Clone()
		s.Parent = RemoteSpy
		s:Play()
		s.PlaybackSpeed = int
	end)
end

local HasSpecial = function(string)
    return (string:match("%c") or string:match("%s") or string:match("%p")) ~= nil
end

local GetPath = function(Instance)
	local Obj = Instance
	local string = {}
	local temp = {}
	local error = false
	
	while Obj ~= game do
		if Obj == nil then
			error = true
			break
		end
		table.insert(temp, Obj.Parent == game and Obj.ClassName or tostring(Obj))
		Obj = Obj.Parent
	end
	
	table.insert(string, "game:GetService(\"" .. temp[#temp] .. "\")")
	
	for i = #temp - 1, 1, -1 do
		table.insert(string, HasSpecial(temp[i]) and "[\"" .. temp[i] .. "\"]" or "." .. temp[i])
	end

	return (error and "nil -- Path contained an invalid instance" or table.concat(string, ""))
end

local GetType = function(Instance)
	local Types = 
	{
		EnumItem = function()
			return "Enum." .. tostring(Instance.EnumType) .. "." .. tostring(Instance.Name)
		end,
		Instance = function()
			return GetPath(Instance)
		end,
		CFrame = function()
			return "CFrame.new(" .. tostring(Instance) .. ")"
		end,
		Vector3 = function()
			return "Vector3.new(" .. tostring(Instance) .. ")"
		end,
		BrickColor = function()
			return "BrickColor.new(\"" .. tostring(Instance) .. "\")"
		end,
		Color3 = function()
			return "Color3.new(" .. tostring(Instance) .. ")"
		end,
		string = function()
			return "\"" .. tostring(Instance) .. "\""
		end,
		Ray = function()
			return "Ray.new(Vector3.new(" .. tostring(Instance.Origin) .. "), Vector3.new(" .. tostring(Instance.Direction) .. "))"
		end
	}

	return Types[(typeof or type)(Instance)] ~= nil and Types[(typeof or type)(Instance)]() or tostring(Instance)
end

local size_frame = function(frame, UDim)
	frame:TweenSize(UDim, "Out", "Quint", 0.3)
end

local pos_frame = function(frame, UDim)
	frame:TweenPosition(UDim, "Out", "Quint", 0.3)
end

local size_pos_frame = function(frame, UDim, UDim2)
	frame:TweenSizeAndPosition(UDim, UDim2, "Out", "Quint", 0.3)
end

local resize_onchange = function(type)
	if type == "Position" then
		Resize.Position = UDim2.new(0.5, -50, 1, Resize.Position.Y.Offset)
		lvl6Source.Size = UDim2.new(1, 0, 1, Resize.Position.Y.Offset - 30)
		lvl6Output.Position = UDim2.new(0, 0, 1, Resize.Position.Y.Offset + 20)
		lvl6Output.Size = UDim2.new(1, 0, 0, 110 + (-130 - Resize.Position.Y.Offset))
		if Resize.Position.Y.Offset <= -420 then
			Resize.Position = UDim2.new(0.5, -50, 1, -420)
		elseif Resize.Position.Y.Offset >= -40 then
			Resize.Position = UDim2.new(0.5, -50, 1, -40)
		end
	end
end

local clear_lvl6 = function()
	playSound(topPress, 1)
	Source_.Text = ""
end

local onchange_lvl6source = function(type)
	if type == "Text" then
		Source_.Comments_.Text = Comments(Source_.Text)
	end
end

local hide = function()
	playSound(openSound, 0.9)
	size_frame(BG, UDim2.new(0, 300, 0, 20))
	pos_frame(Title, UDim2.new(0, 0, 0, 0))
	pos_frame(Remotes, UDim2.new(0, 10, 0, 100))
	pos_frame(Source, UDim2.new(0, 270, 0, 100))
	BG.Draggable = true
	SetRemotes.Visible = false
	SetRemotesTab.Visible = false
	lvl6Frame.Visible = false
	Source.Visible = true
	
	return "[]"
end

local show = function()
	playSound(openSound, 1)
	size_frame(BG, UDim2.new(1, -300, 1, -200))
	pos_frame(BG, UDim2.new(0.1, 0, 0.1, 0))
	pos_frame(Title, UDim2.new(0.5, -100, 0, 0))
	pos_frame(Remotes, UDim2.new(0, 10, 0, 80))
	pos_frame(Source, UDim2.new(0, 270, 0, 80))
	BG.Draggable = false
	
	return "_"
end

local onclick_lvl6 = function()
	print("hi")
	playSound(topPress, 1)
	lvl6Frame.Visible = true
	RemoteButtons.Visible = false
	SetRemotes.Visible = false
	SetRemotesTab.Visible = false
	Source.Visible = false
end

local onclick_hide = function()
	Hide.Text = Hide.Text == "_" and hide() or show()
end

local onclick_settings = function()
	playSound(topPress, 1)
	Source.Visible = not Source.Visible
	SetRemotes.Visible = not Source.Visible
	SetRemotesTab.Visible = not Source.Visible
	RemoteButtons.Visible = Source.Visible
	lvl6Frame.Visible = false
end

local onclick_remotespy = function()
	playSound(topPress, 1)
	spy_enabled = not spy_enabled
	EnableSpy.TextColor3 = EnableSpy.TextColor3 == Color3.fromRGB(60, 200, 60) and Color3.fromRGB(200, 60, 60) or Color3.fromRGB(60, 200, 60)
	EnableSpy.BorderColor3 = EnableSpy.TextColor3 == Color3.fromRGB(200, 60, 60) and Color3.fromRGB(100, 30, 30) or Color3.fromRGB(30, 100, 30)
end

local onclick_mute = function()
	playSound(topPress, 1)
	Mute.BorderColor3 = Mute.BorderColor3 == Color3.fromRGB(30, 100, 30) and Color3.fromRGB(100, 30, 30) or Color3.fromRGB(30, 100, 30)
	Mute.Icon.ImageColor3 = Mute.Icon.ImageColor3 == Color3.fromRGB(60, 200, 60) and Color3.fromRGB(200, 60, 60) or Color3.fromRGB(60, 200, 60)
	for i, v in pairs(sounds) do
		v.Volume = Mute.Icon.ImageColor3 == Color3.fromRGB(60, 200, 60) and 0.5 or 0
	end
end

local onclick_cryptstring = function()
	playSound(topPress, 1)
	encrypt_string = not encrypt_string
	CryptStrings.TextColor3 = CryptStrings.TextColor3 == Color3.fromRGB(60, 200, 60) and Color3.fromRGB(200, 60, 60) or Color3.fromRGB(60, 200, 60)
	CryptStrings.BorderColor3 = CryptStrings.TextColor3 == Color3.fromRGB(200, 60, 60) and Color3.fromRGB(100, 30, 30) or Color3.fromRGB(30, 100, 30)
end

local clear_logs = function()
	playSound(topPress, 1)
	Remotes:ClearAllChildren()
	remotes_fired = 0
	Total.Text = "0"
end

local filter_events = function()
	local n = 0
	for i, v in pairs(SetRemotes:GetChildren()) do
		v.Visible = not (FilterE.TextColor3 == Color3.fromRGB(60, 200, 60) and v.Icon.Image == "rbxassetid://413369623")
		if v.Visible == true then
			n = n + 1
			v.Position = UDim2.new(0, 10, 0, -20 + n * 30)
		else
			v.Position = UDim2.new(0, 10, 0, -20 + i * 30)
		end
	end
end

local filter_functions = function()
	local n = 0
	for i, v in pairs(SetRemotes:GetChildren()) do
		v.Visible = not (FilterF.TextColor3 == Color3.fromRGB(60, 200, 60) and v.Icon.Image == "rbxassetid://413369506")
		if v.Visible == true then
			n = n + 1
			v.Position = UDim2.new(0, 10, 0, -20 + n * 30)
		else
			v.Position = UDim2.new(0, 10, 0, -20 + i * 30)
		end
	end
end

local onclick_fevents = function()
	playSound(topPress, 1)
	FilterE.TextColor3 = FilterE.TextColor3 == Color3.fromRGB(60, 200, 60) and Color3.fromRGB(200, 60, 60) or Color3.fromRGB(60, 200, 60)
	FilterE.BorderColor3 = FilterE.TextColor3 == Color3.fromRGB(200, 60, 60) and Color3.fromRGB(100, 30, 30) or Color3.fromRGB(30, 100, 30)
	filter_events()
end

local onclick_ffunctions = function()
	playSound(topPress, 1)
	FilterF.TextColor3 = FilterF.TextColor3 == Color3.fromRGB(60, 200, 60) and Color3.fromRGB(200, 60, 60) or Color3.fromRGB(60, 200, 60)
	FilterF.BorderColor3 = FilterF.TextColor3 == Color3.fromRGB(200, 60, 60) and Color3.fromRGB(100, 30, 30) or Color3.fromRGB(30, 100, 30)
	filter_functions()
end

local Highlight = function(string, keywords)
    local K = {}
    local S = string
    local Token =
    {
        ["="] = true,
        ["."] = true,
        [","] = true,
        ["("] = true,
        [")"] = true,
        ["["] = true,
        ["]"] = true,
        ["{"] = true,
        ["}"] = true,
        [":"] = true,
        ["*"] = true,
        ["/"] = true,
        ["+"] = true,
        ["-"] = true,
        ["%"] = true,
		[";"] = true,
		["~"] = true
    }
    for i, v in pairs(keywords) do
        K[v] = true
    end
    S = S:gsub(".", function(c)
        if Token[c] ~= nil then
            return "\32"
        else
            return c
        end
    end)
    S = S:gsub("%S+", function(c)
        if K[c] ~= nil then
            return c
        else
            return (" "):rep(#c)
        end
    end)
  
    return S
end

local hTokens = function(string)
    local Token =
    {
        ["="] = true,
        ["."] = true,
        [","] = true,
        ["("] = true,
        [")"] = true,
        ["["] = true,
        ["]"] = true,
        ["{"] = true,
        ["}"] = true,
        [":"] = true,
        ["*"] = true,
        ["/"] = true,
        ["+"] = true,
        ["-"] = true,
        ["%"] = true,
		[";"] = true,
		["~"] = true
    }
    local A = ""
    string:gsub(".", function(c)
        if Token[c] ~= nil then
            A = A .. c
        elseif c == "\n" then
            A = A .. "\n"
		elseif c == "\t" then
			A = A .. "\t"
        else
            A = A .. "\32"
        end
    end)
  
    return A
end


local strings = function(string)
    local highlight = ""
    local quote = false
    string:gsub(".", function(c)
        if quote == false and c == "\"" then
            quote = true
        elseif quote == true and c == "\"" then
            quote = false
        end
        if quote == false and c == "\"" then
            highlight = highlight .. "\""
        elseif c == "\n" then
            highlight = highlight .. "\n"
		elseif c == "\t" then
		    highlight = highlight .. "\t"
        elseif quote == true then
            highlight = highlight .. c
        elseif quote == false then
            highlight = highlight .. "\32"
        end
    end)
  
    return highlight
end

local comments = function(string)
    local ret = ""
    string:gsub("[^\r\n]+", function(c)
        local comm = false
        local i = 0
        c:gsub(".", function(n)
            i = i + 1
            if c:sub(i, i + 1) == "--" then
                comm = true
            end
            if comm == true then
                ret = ret .. n
            else
                ret = ret .. "\32"
            end
        end)
        ret = ret
    end)
    
    return ret
end

local copy_source = function()
	playSound(topPress, 1)
	local script = ""
	local copy
	for i, v in pairs(Source:GetChildren()) do
		script = script .. v.SourceText.Text .. "\n"
	end
	if Clipboard ~= nil then
		copy = Clipboard.set
	elseif Synapse ~= nil then
		copy = function(str)
			Synapse:Copy(str)
		end
	elseif setclipboard ~= nil then	
		copy = setclipboard
	end
	copy(script)
end

local onclick_fullscreen = function()
	playSound(openSound, BG.Size == UDim2.new(1, 0, 1, 40) and 0.9 or 1)
	BG.Draggable = BG.Size == UDim2.new(1, 0, 1, 40)
	if (BG.Size == UDim2.new(1, -300, 1, -200)) then
		last_bg_pos = BG.Position
		size_pos_frame(BG, UDim2.new(1, 0, 1, 40), UDim2.new(0, 0, 0, -40))
	else
		BG.Draggable = true
		size_pos_frame(BG, UDim2.new(1, -300, 1, -200), last_bg_pos)
	end
end

local onclick_exit = function()
	game:GetService("CoreGui").RemoteSpy:Destroy()
end

local filter_remotes = function(type)
	local n = 0
	if type == "Text" then
		for i, v in pairs(SetRemotes:GetChildren()) do
			if v.Name:lower():match(Search.Text:lower()) and string ~= "" then
				v.Visible = true
				n = n + 1
			else
				v.Visible = false
			end
			if v.Visible == true then
				v.Position = UDim2.new(0, 10, 0, -20 + n * 30)
			else
				v.Position = UDim2.new(0, 10, 0, -20 + i * 30)
			end
		end
	end
end

local fix = function(string)
	if string == "/e fix" then
		show()
		wait(0.3)
		pos_frame(BG, UDim2.new(0.1, 0, 0.1, 0))
	end
end

local highlight_source = function(type)
	if type == "Text" then
		Source_.Text = Source_.Text:gsub("\13", "")
		Source_.Text = Source_.Text:gsub("\t", "      ")
		local s = Source_.Text
		Source_.Keywords_.Text = Highlight(s, lua_keywords)
		Source_.Globals_.Text = Highlight(s, global_env)
		Source_.RemoteHighlight_.Text = Highlight(s, {"FireServer", "fireServer", "InvokeServer", "invokeServer"})
		Source_.Strings_.Text = strings(s)
		Source_.Tokens_.Text = hTokens(s)
		local lin = 1
		s:gsub("\n", function()
			lin = lin + 1
		end)
		Lines.Text = ""
		for i = 1, lin do
			Lines.Text = Lines.Text .. i .. "\n"
		end
	end
end

highlight_source("Text")

local format_warn_time = function()
	local d = os.date("*t")
	local tick = tostring(tick())
	return d.hour .. ":" .. (d.min < 10 and "0" .. d.min or d.min) .. ":" .. (d.sec < 10 and "0" .. d.sec or d.sec) .. "." .. tick:sub(-3)
end

local log_output = function(string, type, color)
	local out = Label:Clone()
	out.Text = (type == true and string:gsub("\t", "      ") or format_warn_time() .. " - " .. string:gsub("\t", "      "))
	out.TextColor3 = (color == nil and Color3.new(1, 1, 1) or color)
	out.Parent = lvl6Output
	out.Position = UDim2.new(0, 0, 0, -17 + #lvl6Output:GetChildren() * 17)
end

local load_source = function()
	playSound(topPress, 1)
	local script = ""
	for i, v in pairs(Source:GetChildren()) do
		script = script .. v.SourceText.Text .. "\n"
	end
	Source_.Text = (script == "" and (function() playSound(errorSound, 1) log_output("You haven't logged any remotes yet...", true) return "" end)() or script)
	lvl6Frame.Visible = true
	Source.Visible = false
	RemoteButtons.Visible = false
	SetRemotes.Visible = false
	SetRemotesTab.Visible = false
end

local output_format = function(...)
	local string = ""
	for i, v in pairs{...} do
		string = string .. tostring(v) .. "     "
	end
	
	return string
end

local execute_lvl6 = function()
	playSound(topPress, 1)
	local env = 
	{
		print = function(...)
			output_format(...):gsub("[^\r\n]+", function(line)
				log_output(line, false, Color3.new(1, 1, 1))
			end)
		end,
		warn = function(...)
			output_format(...):gsub("[^\r\n]+", function(line)
				log_output(line, false, Color3.fromRGB(255, 155, 0))
			end)
		end
	}
	local func = loadstring(Source_.Text)
	assert(not (type(func) == "nil" or type(func) == "string"), "Syntax error . . . Check script!")
	spawn(setfenv(func, setmetatable(env, {__index = getfenv()})))
end

local clear_output = function()
	playSound(topPress, 1)
	lvl6Output:ClearAllChildren()
end

local context_error = function(error, trace)
	playSound(errorSound, 1)
	error:gsub("[^\r\n]+", function(line)
		log_output(line, false, Color3.new(1, 0, 0))
	end)
	trace:gsub("[^\r\n]+", function(line)
		log_output(line, false, Color3.fromRGB(0, 100, 255))
	end)
end

-- FrontEnd-Connections // UI Events

LoadSource.MouseButton1Down:Connect(load_source)
ClearOutput.MouseButton1Down:Connect(clear_output)
ExecuteScript.MouseButton1Down:Connect(execute_lvl6)
ClearScript.MouseButton1Down:Connect(clear_lvl6)
Source_.Changed:Connect(highlight_source)
Hide.MouseButton1Down:Connect(onclick_hide)
lvl6Source.Changed:Connect(onchange_lvl6source)
Resize.Changed:Connect(resize_onchange)
lvl6.MouseButton1Down:Connect(onclick_lvl6)
Settings.MouseButton1Down:Connect(onclick_settings)
ClearList.MouseButton1Down:Connect(clear_logs)
EnableSpy.MouseButton1Down:Connect(onclick_remotespy)
ToClipboard.MouseButton1Down:Connect(copy_source)
CryptStrings.MouseButton1Down:Connect(onclick_cryptstring)
FullScreen.MouseButton1Down:Connect(onclick_fullscreen)
--Exit.MouseButton1Down:Connect(onclick_exit)
FilterE.MouseButton1Down:Connect(onclick_fevents)
FilterF.MouseButton1Down:Connect(onclick_ffunctions)
Search.Changed:Connect(filter_remotes)
Mute.MouseButton1Down:Connect(onclick_mute)
game:GetService("Players").LocalPlayer.Chatted:Connect(fix)
game:GetService("ScriptContext").Error:Connect(context_error)

-- Recursive Remotefill // UI-Backend

Parse = function(T)
    local M = {}
    for i, v in pairs(T) do
        local I = "\n\t" .. (type(i) == "number" and "[" .. i .. "] = " or "[\"" .. i .. "\"] = ")
        table.insert(M, I .. (type(v) == "table" and Parse(v) or GetType(v)))
    end
    
    return " {" .. table.concat(M, ", ") .. "\n}"
end

function fill(base)
	for i, v in pairs(base:GetChildren()) do
		if v.ClassName:match("Remote") and v.Name ~= "CharacterSoundEvent" then
			local B = SBTN:Clone()
			
			B.Parent = SetRemotes
			B.Icon.Image = (v.ClassName == "RemoteEvent" and "rbxassetid://413369506" or "rbxassetid://413369623")
			B.RemoteName.Text = v.Name
			B.Name = v.Name
			B.Position = UDim2.new(0, 10, 0, -20 + #SetRemotes:GetChildren() * 30)
			B.MouseButton1Down:Connect(function()
				B.Enabled.Text = B.Enabled.Text == "Enabled" and "Disabled" or "Enabled"
				B.Enabled.TextColor3 = B.Enabled.Text == "Enabled" and Color3.fromRGB(60, 200, 60) or Color3.fromRGB(200, 60, 60)
				B.Enabled.BorderColor3 = B.Enabled.Text == "Enabled" and Color3.fromRGB(30, 100, 30) or Color3.fromRGB(100, 30, 30)
				playSound(disableSound, B.Enabled.Text == "Enabled" and 1 or 0.9)
				for i, v in pairs(Remotes:GetChildren()) do
					if (v.RemoteName.Text == B.RemoteName.Text) then
						v.Icon.ImageColor3 = B.Enabled.Text == "Disabled" and Color3.new(1, 0, 0) or Color3.new(1, 1, 1)
					end
				end
			end)
		end
		fill(v)
	end
end

fill(game)

-- Backend // Remotespy Backend

local game_meta = getrawmetatable(game)
local game_namecall = game_meta.__namecall
local namecall_dump = {}
local current_rmt = nil
local g_caller = nil
local f_return = nil
local Step = game:GetService("RunService").Stepped
local breakloop = false
local looprunning = false

local mwr = function() end

if setreadonly ~= nil then
	mwr = function()
		setreadonly(game_meta, false)
	end
elseif make_writeable ~= nil then	
	mwr = function()
		make_writeable(game_meta)
	end
end

mwr()

local namecall_script = function(object, method, ...)
	local script = "-- Script generated by R2Sv2\n-- R2Sv2 fixed by ButterflyEffect, dragging function Danisty§#9161\n-- Remote Path: " .. GetPath(object) .. "\n\32\n"
	local args = {}
	
	--[[local CN    
    if object:IsA("RemoteEvent") then
        CN = "FireServer"
    elseif object:IsA("RemoteFunction") then
        CN = "InvokeServer"
    elseif object:IsA("BindableEvent") then
        CN = "Fire"
    elseif object:IsA("BindableFunction") then
        CN = "Invoke"
    end--]]
	--local members = {}	
	
	for i, v in pairs{...} do
		script = script .. "local A_" .. i .. " = " .. (type(v) == "table" and Parse(v) or GetType(v)) .. "\n"
		table.insert(args, "A_" .. i)
	end
	
	script = script .. "local Event = " .. GetPath(object) .. "\n\n"
	script = script .. "Event:" .. tostring(method) .. "(" .. table.concat(args, ", ") .. ")"
	return script
end


local dump_script = function(script)
	Source:ClearAllChildren()
	local lines = 0
	script:gsub("[^\r\n]+", function(c)
		lines = lines + 1
		local tabs = 0
		c:gsub("%\t", function() tabs = tabs + 1 end)
		local line = ScriptLine:Clone()
		line.Parent = Source
		line.SourceText.Text = c 
		line.Line.Text = lines
		line.RemoteHighlight.Text = Highlight(c, {"FireServer", "InvokeServer", "invokeServer", "fireServer"})
		line.Position = UDim2.new(0, tabs * (17 * 2), 0, -17 + #Source:GetChildren() * 17)
		line.Globals.Text = Highlight(c, global_env)
		line.Line.Position = UDim2.new(0, 0 - tabs * (17 * 2), 0, 0)
		line.Strings.Text = strings(c)
		line.Keywords.Text = Highlight(c, lua_keywords)
		line.Tokens.Text = hTokens(c)
		line.Comments.Text = comments(c)
	end)
end

local log_remote = function(table)
	if SetRemotes[table.object.Name].Enabled.Text == "Disabled" then return end
	playSound(logSound, 5)
	local B = RBTN:Clone()
	g_caller = table.caller
	remotes_fired = remotes_fired + 1
	Total.Text = remotes_fired

	B.Parent = Remotes
	B.Position = UDim2.new(0, 10, 0, -20 + #Remotes:GetChildren() * 30)
	B.Icon.Image = table.method == "FireServer" and "rbxassetid://413369506" or "rbxassetid://413369623"
	B.RemoteName.Text = table.object.Name
	B.ID.Text = tostring(remotes_fired)
	B.MouseButton1Down:Connect(function()
		current_rmt = table.object
		playSound(topPress, 1)
		lvl6Frame.Visible = false
		SetRemotes.Visible = false
		RemoteButtons.Visible = true
		SetRemotesTab.Visible = false
		Source.Visible = true
		dump_script(table.script)
		g_caller = table.caller
		f_return = table.freturn == nil and table.object.Name .. " is not RemoteFunction" or table.freturn
	end)
	B.MouseButton2Down:Connect(function()
		local bool = B.Icon.ImageColor3 == Color3.new(1, 1, 1)
		playSound(disableSound, bool and 0.9 or 1)
		for i, v in pairs(Remotes:GetChildren()) do
			if (v.RemoteName.Text == B.RemoteName.Text) then
				v.Icon.ImageColor3 = bool and Color3.new(1, 0, 0) or Color3.new(1, 1, 1)
			end
		end
		SetRemotes[B.RemoteName.Text].Enabled.Text = not bool and "Enabled" or "Disabled"
		SetRemotes[B.RemoteName.Text].Enabled.TextColor3 = not bool and Color3.fromRGB(60, 200, 60) or Color3.fromRGB(200, 60, 60)
		SetRemotes[B.RemoteName.Text].Enabled.BorderColor3 = not bool and Color3.fromRGB(30, 100, 30) or Color3.fromRGB(100, 30, 30)
	end)
end

local get_namecall_dump = function(script, object, ...)
	local Ret = nil
	if object.ClassName == "RemoteFunction" then
		local freturn = {pcall(object.InvokeServer, object, ...)}
		freturn = {select(2, unpack(freturn))}
		
		if #freturn == 0 then
			Ret = object.Name .. " is a void type RemoteFunction."
		else
			Ret = "local " .. object.Name .. "_return = " .. Parse(freturn)
		end
	end
	if object.ClassName == "BindableFunction" then
		local freturn = {pcall(object.Invoke, object, ...)}
		freturn = {select(2, unpack(freturn))}
		
		if #freturn == 0 then
			Ret = object.Name .. " is a void type BindableFunction."
		else
			Ret = "local " .. object.Name .. "_return = " .. Parse(freturn)
		end
	end
	namecall_dump[#namecall_dump + 1] = 
	{	
		script = namecall_script(object, (object.ClassName == "RemoteEvent" and "FireServer" or "InvokeServer") or (object.ClassName == "BindableEvent" and "Fire" or "Invoke"), ...),
		caller = script,
		object = object,
		method = (object.ClassName == "RemoteEvent" and "FireServer" or "InvokeServer") or (object.ClassName == "BindableEvent" and "Fire" or "Invoke"),
		freturn = Ret
	}
end

GetReturn.MouseButton1Down:Connect(function() 
	dump_script(f_return)
	if (f_return:match("is not Remote")) then playSound(errorSound, 1) end
end)

Decompile.MouseButton1Down:Connect(function()
	playSound(topPress, 1)
	local source = decompile(g_caller)
		
	dump_script(type(source) == "boolean" and (function() playSound(errorSound, 1) Source.Visible = false SetRemotes.Visible = false SetRemotesTab.Visible = false lvl6Frame.Visible = true log_output("Failed to decompile...", true) return "" end)() or source)
end)

Step:Connect(function()
	while #namecall_dump > 0 do
		log_remote(table.remove(namecall_dump, 1))
	end
end)

local on_namecall = function(object, ...)
	local args = {...}
	local method = isluau() and getnamecallmethod() or table.remove(args, #args)  --FIXEDLINE
	--args[#args] = nil
	if object.Name ~= "CharacterSoundEvent" and method:match("Server") and spy_enabled == true then get_namecall_dump(getfenv(2).script, object, unpack(args)) end

	return game_namecall(object, ...)
end

local onclick_refresh = function()
	playSound(topPress, 1)
	SetRemotes:ClearAllChildren()
	wait(0.2)
	fill(game)
end

local infloop = function()
	playSound(topPress, 1)
	local script = ""
	for i, v in pairs(Source:GetChildren()) do
		script = script .. v.SourceText.Text .. "\n"
	end
	local source = loadstring(script)
	local delay = tonumber(FireDelay.Text)
	while wait(delay) do
		source()
		if (breakloop == true) then breakloop = false break end
	end
end

local forloop = function()
	playSound(topPress, 1)
	local script = ""
	for i, v in pairs(Source:GetChildren()) do
		script = script .. v.SourceText.Text .. "\n"
	end
	local source = loadstring(script)
	local delay = tonumber(FireDelay.Text)
	local amount = tonumber(FireAmount.Text)
	for i = 1, amount do
		source()
		wait(delay)
		if (breakloop == true) then breakloop = false break end 
		FireAmount.Text = tostring(amount - i)
	end
end

local fireremote = function()
	playSound(topPress, 1)
	local script = ""
	for i, v in pairs(Source:GetChildren()) do
		script = script .. v.SourceText.Text .. "\n"
	end
	loadstring(script)()
end

local enable_break = function() breakloop = true end

-- Backend Event Connections

FireRemote.MouseButton1Down:Connect(fireremote)
LoopFire.MouseButton1Down:Connect(forloop)
WhileLoopFire.MouseButton1Down:Connect(infloop)
Refresh.MouseButton1Down:Connect(onclick_refresh)
Break.MouseButton1Down:Connect(enable_break)
game_meta.__namecall = on_namecall
end)

local Hubs = Window:NewTab("Hubs")
local HubsSection = Hubs:NewSection("Game Hubs")

HubsSection:NewButton("OWL HUB", "...", function()
    return(function(B,e,o,n,a,C,l)local d=select;local o=table.insert;local S=unpack or table.unpack;local f=string.char;local c=string.sub;local Q=setmetatable;local D=table.concat;local F=string.byte;local E=getfenv or function()return _ENV end;local Y=l;local t={}for e=a,255 do t[e]=f(e)end;local function i(A)local l,o,X=e,e,{}local I=C;local e=n;local function S()local l=Y(c(A,e,e),36)e=e+n;local n=Y(c(A,e,e+l-n),36)e=e+l;return n end;l=f(S())X[n]=l;while e<#A do local e=S()if t[e]then o=t[e]else o=l..c(l,n,1)end;t[I]=l..c(o,n,1)X[#X+n],l,I=o,o,I+n end;return D(X)end;local Y=i('24124L24124124527624126U26O27026S24124B27925Y26S26D25E26S26B26F26W26Q27E24A27926126D26D26927L27N27P27E24927926027326A26D26O27327Q24124227927326S26E24124627925J26S26Q26D27226B24J24124727925U27227128O24I27727925F28L26D24124827925E26Q26B26S26S27325Y26C26W27F28327026O26U26S26526O26R26S27124124427925Z26B27C27R29H29J26S25V26C27V27227329427925H26S26H26D29M29O29Q27827626729W24124D27H29B27M26O26D26S25Y25G26025X28R27925D26O29927329328I27628U29929D29F27S27625S28926X28O25D27226W2B024027927923524U24123L27925V26O26Q26Y26U26B27226C27326T28U28W26B24I2BI2BJ24122P2BM23R2BP2BR2BT2BV2BX26T25H29V2852692AY29B26Q26G24124E2BP28O26T27M25E26W26J26S25D26W26H29P2C42C52762BO2B327126W26926A25X26S26A27Q2BY28826D26A2432BI2822762BE26A26W26D26W2A429R27925G25X26W27028Q29S27626029I29K24125727926X27V26924R25A25A26E2EE25B2BV26R28W26H25B26Q27227025A26O26A26A27J25A24U26W26T24S24L24K24I24H24I24G24P24M24P24G2412B82412E229Z2C028X24021Z25R22Z26423Q23T2152BM29527629726O27126S25H26G26927E2AF24125W27326C2702DT2FQ2D728A2FA25E2G726S25U29B2AP26B2D227924L25T2GH27626N25T2E52E72E92EB2ED2EF2EH2EJ2EL2EN2EP2ER2ET2EV2EX24L24I2F524H24M24L2H72752AK27625V2CR27M2FE2C224021R25824T25A23O23U21624U24021I24T21723K23R23O22C2HR26923H22026A181B22J2HR2C51H25S2GO2FZ2CU2CW2GL24126D2GK2D325K2GO2B224125J26W2DO2EI26S24324124025W23I25425T23426J2BL24021S23C26G24M23R23P21X2BM23K29Y29K2CG28826A2CJ2AZ2CM28Z27625Z2A42932CP2FQ2BW26B27Q25E2JH26526W26U2E82JM2412A82AA2412C927625G27326W26F27M26A2FS24X25S2DX26R27226D24X25324X25W25E25D29G2762K426D2HH28Y2DL2K32A927K2CV26S2GL1H25V2IJ2BJ23526C2L72BJ24O2GO2E62762E827W2GS2EE26E2EG2722EI2722EK2EM2EO2EQ2ES26D2EU2EW2EY2F02F224G24O2M124J2401T22V26H24W23W23Z21B2I82C523P2LB2761X2LA2GP2LG2GR2EC2LK2LM2LO2LQ2GY2LT2H12LX24L24N24P2F724K2MW24O28Y28C2JN2DP2AJ27T2E927I26D25S26A26G28924125Z2GQ27W26A2GS29V2LL26U2DP26X26C26R26C2ES2JU2JP2GE2GX2EO25U26B26W25E2BC26C26H25A26626E2712612NR25A29I28627M25A27B27D2JY28625B26Z26A2DS27G27626325E2662672DB2EM2CS2G52412CJ26W26B26A2412KY28N2862O127326U28H2AW2712BR26S26026T24125S2NI2D92NL26O2NN2NP2NR2NT27M2EM2B02NX2LR25A2O02O22O42O62O82OA2OC2OE2GF25A2DD2O12692DH25A2AV2FQ2982D82932E02412JI2PO2A52672PL2NK2EC2NM25B2NO26D2NQ2NS2NU2PU2AP2B02NY2PY2O12O32BW2Q22O92OB26R2OD2EQ2Q72Q92QH26A25A2K92KB2KD2FS25B27126C26O2A62KT26E29A2732IE2L32D325R2GO2JR2G02EQ2BG26U2DW29928M2DR2A52N42412662A22F927925W2S22PA25E26D26G2FT2K225C2RO26T24023Y1K23E25C21523Z21W2MD2BJ25H2IC27926E26O2DP2GL22926R2GO2HC2K32RS29B27Y27O28A2D524125G2NU2842692A22TF2802KS2FB2732TN26D25V26S27B2A52IN28U27328E28M2N72E12TT2A225U26X28829K2PI28S2B32992AO27E2FP2TC2RT28426V27224026824S24B21Y21E26922K2BM2IN26V2BV27025F25Y25V2GL24X26Q2MG24122925I2V81H25U2V82352722GO2OQ2TS2TU2G12CS2PI2JD2762642BW2ES2A12A327324G25U2G726Y24025425P1U22B22S2552392HR22K22L2WB2WB23H24U2UJ28B2762UE2412KW2PC2762UZ2EN26125E25J2IG2C72GL25T2VH2TR2KU2WL2FZ2T42N62BJ23N27923N25N2411R2AU2IV2792KM2X92XB2762IU2X52XF2BI2SA2XJ2XA2IU2FZ2XN25X28C2SA24526R2XK2BN2XC24127E2XA2QJ27925B2XF2WJ27624X2762XA28I2782782XR2822XM2YA25X2952SA2792XA28S2952IU2D52Y22DT28S2XR29S2Y72YI29S2BI2BI24523V2XX28S2Z12NH2XA2XH2XZ23X2XF2762D22402IN24124C2DU2TL2U726D2FV2FX2K22G12G32U52412VR2PS2VU28N2VW2P52AW2722DO2DQ2DS2KY2862AY26D2DN2WM2WK2UA2PA26S2PI2U02A42U326D2ZE2YL24F2ZJ27M2TM2TO2872AP2ZP2G22G42SA2VM2C52VJ24125I2ZC2C52Y931122ZD2412XR2BI2IU2Y82YI2Z02XC31142XA311D28C2UE2Z82A6311D2452Z72XB2952C425L31152BJ2C9311K2GH2ZB311W27924023P2XD2GO311G312031172YI2IU311A241311F25X3129311E31282412IU311I311C24123M2XC2XP311O276312M311R2XX2GH2E631252BJ312C2D22FZ312T2D33125312A312Y2XC2YE312K2QJ31352WI312B312K2BI28I24725K2XF2SA311927625C311T27925P313N27628I312528C2C4311Y2XB2GH311A2ZI2K82ZK2TU2ZN2FY2SF310U2ZH2792ZU2ES2VR2KC27D2B02OZ25H2BW26Q26X2BJ240310M2Y824T2XX31162XR312E311B2XF312E2BI312C312E312J2XX2AK313K311N31123152312B253314Q2XC2X7314V312H2XD31582XO315D314X315F312D315D27824728Q31252ZI3153312P31482C4311V2XG2BJ313W31162792AF2KY2DN2DP2S82OZ2DV2DX28Q2SA28E28G310528726B310831012XZ241311S2QJ2FR2SM2WJ26626V26V2LU316I313H31202512BJ2Y125X2GL2472633112278311M315S3174277315S24Y2XZ316Y311D2WI28C312528231753112317H31783112317A2C4317C315D27623N25R315C3134312G312I3127313I2K2312C2XT2DT31812WH2YU2YI2YD2XD318728Z29S312C318828I312C2QJ2GH2YN2WH2C52YS2YW313C2XF29S318Q2BJ2XA318829S2YV31802YY2DT282318G2YT317Y318J2FZ312C28S28S31902YI31972PC312C2IN318I25X2YG313225X28I28I31992XF319K2ZZ2YM25X319B2ZG315G28S2YQ313D317Q315Y316I317Q31402TJ31422A23144310T2ZR31A2314A26S314C26S314E2932FZ25D2PE2CN31202FA24X314P312W315A317W3189317U312F31AS3150312528I315R311231AX317L311K27G317O31592Y825Q31312AF24H2XX2IU313V3112313Y27631A22TK310O2ZL31A62FZ2ZQ2G431A92VS31AB272314D2GE2K231AH26O31AJ2ZD2VJ24X3124316Z3126314S317Q318O315G31BC31C7315K317X311J31C3311Q315L315S31CF2Y031B5312B31B731252Z127631BA31332ZA31BE3120312M2792IN2IP2IR2FT31292BI2WJ2AX2AZ2932UJ25H2TD2RU2L231662DW2DY318K241316B2IG315Z2BJ2RY31A72G42S02SG2DO2PA2S529231652SA2SC2932FA31DP2S32SJ2SL3145313L2SP2SR2ST2SV2SX2SZ2A72T22762X2310J2D32BL310A2DB2P827231BY27625J2BJ23Q313Q31BA31CT312A31CT31CP2YI311631EU311K312A31ES311Z2YL311K2SA312C2BJ27831F7279318V312G2WJ314Y315D28I2XR28C2KY2XR2782UJ318W31FK319A2RQ318S315K319V31932XS2TR318428C27S31FY2N731FL31FX318A2782ZI318D28Z310M318W2S0319Q2762YZ31FS2Z9314U311K31GE31FV2IU31FE31AQ31FH2YI31FJ2X6318A2TI31FO31GS2Y62XY318L31FT315D31FI31G4317Z31FZ31CA31822AK31G331C031G5314831G827831GA318Y31GC31EX2DT2BI2XR2762VP31FV31HK319I2Z9319F27631F631HI27631F931HV2DT31C531GN31AS31GP317Z31FP2XF27831I52YS31I8319R319P31FS31GM31H131GQ31H32XA318231G031IG28C31H8318A31HA31I628Z31G731HB31HF318P2CO31HQ31HJ31GG31C631FA31GK31I031AR31C82PC31H231IA31I731GW31I931JA31IB2KY319Q31IE2XI31IG31IP31II2WH31IK31H431G231IO31J425X318831IS31IQ31HE31FV29S31HH311231GF31HL24131HN311831IW3160311231C931GD318X311T31CV31HI31K831HI310K31F82PD31BX2K231EE2W12W32W52W72BM2BJ314N276316Y2D324X28231GJ31A031F031AP31K731JC2XL31IX31KE31EV31CA314L31IZ31C931K1312A31K42YL31KD313631HY31BD311Z2792B831CX2IQ26W2IS31D12QE24131D431BU31D731D92RV31DC316831DF31DH2D331DJ27931DL31BM314731DO2SH2S42P231DT2DS31DV2SD31DY31MA31E12SM2FZ2SO26O2SQ2SS2SU2SW2SY2IG2T131KK2T531EF2C531EH2VJ28W31MN2P82S32K22OI27E2IN27U27W2NA31EI2DC26D2BV31EM24125O31EP31ER31KF31C631L731F2313X31NM31L031EW31CT31F42XB31HU311T31HX311T31FC315C31I131J531I331JK31J831FR31GV317R31FQ2WG31FD31IF317Z31JJ31FW31H531G131IN31IQ31OF31JS31CA318831IU2YS31JY311K31GF31K9317V31NZ31GL31LS31FF2IU31O431FW31O631GU318Y31IA28S2TI31JF2AV31JH31OE31JQ31IJ31H62WH31OJ318T31IH31JR31IR31ON31G931JW31K531IZ31K031HI31K3312K2XJ31LA31KZ31NV31JQ31KH31J131HZ31OC31GI31CB31J631IG31O631IA29S31P631IC31P931FU31H231OF31PE31OI31FV27831OL31PL31HD24131OP25X31JX31IX31OT31LG31Q42BJ31O0319U31JQ312E31P131GR31O931IQ31Q931IC2XR3198319I31JG31FV28C31QG31JL31PF31IM31QJ31PJ31OM31QN31QP31QR31GZ31GK31HP311231PT2XX31GC2KR31L031RP311K31KC31K4312231Q4311D23O31FS28C3130312K31LF311T31EZ31NP31HS2OZ31Q12K731LG31SC2GH26V311A23N2BO31LK31L827931PB315G31S831L031SQ31C33195319X31QX31H031Q4312E31SY28C2IN31G131SY31J931Q4318U31FS31QT31R731FR319Q29S314T31FQ2D22XR28I310Z31FQ31TG319N316I2YF2TR319Q28I31TN2XA317K31R32XA2952FA319Q28231TU2YJ31TP2YI27G2TB319Q2YP31NQ25X31B331JC27S31A2319Q27G31U327S31TI2YI2AK31TL2XF27S31U3315631TX25X2ZI31UO2XA2AK31U3315Q31JC310M31U82YI2ZI312E312C31KS31GC2XA31P831FS310M2BO319W31IV310M31QP310M2D231V731QO31OD31VA31K2319I31VD315D2YR31QQ2XY310M31VL27631V925X31VB319Q31VR31VF318J31VH31GY318J2BO2Y32XA310M31LD2YI2CP31RY2YI2BO31KC31W22XY31W431IB2X531KS2XF310M2YH2XF2CP31S331UT2BO31WV31FV2JD31WY31WK2JD31WM28S3122310M31NO28S2C931S331X824131EQ23T24131XC23S2412Z32XR310M2ZB31Q431W631SY31WF31JC2BO31XF31UT2JD31WG2XF2X531XU31VC312731X424123U31VM31XC23W24123Z31Y131WS2XA2CP311431FV2BO31YF2XR2JD31YF31VP31WB31VP2YQ2BI318J23Y31VM31XL24124Z31JQ31W624W31CA31W6317A31VT28S31YZ31WP31YN2XQ31WE24125031XS31ZA31JC2JD315831UT2X531ZG31Y12X531Y3316W31VW2YI31V831FS31W131ZP31WL31W7319J31VM31VR31TO2BO2Y731YN31WD31WT312L31ZC31WJ31ZT31VE31ZV31GP31Z625X31WR31JC31WU31ZC31WY31YJ24131X131ZT31X3320A24131X631XG2YI28I31XA320R31TO31XE31FV31XM31YX31VM31XQ320531WW24131Y0320J31XX2XA31XZ31VQ31Y2320O31Y531X7320S24131Y825231Z027931VZ31ZS31WQ31ZU31VT28231W6321Q2XY3201320D31C62XR31XR321431Y031WK3209321T31WO31YB320F320K320H31ZE322831GZ310M320N321T320Q31NO282320U31WK31YC25X2CP25431ZC2LF31WZ241256321B322E2YI28225531Y6322W31XD3215320Y24131XN321K310M3212321831W0323231XV323B31FV2X5259321B31ZL31ZV282321E3233323531VL323731FV2CP321631WH2412Y5323C323S31XY2412QD322C321C321T258322Z2XF28231BA2F824X31CM321W31VY2B92XF321N31YN32232YI295321S324J2XY31JE32023227323931WI321B324I2XF2953225322K3227320I323T32502XF31X0322U31VS324M322G324M320U31NO295320X31YU323N31ZT323P321Y321331YG323D320J28Q31ZH323D31WK323I31VT295323L325E3210325H31Z9323X31VO323V322R325Z25X2X5324031ZK3256324V2413244321F326931Y831YA324Y31UT2CP28Y3214326J322R326L31X2326831TY24131YS326C326Q275312M31YU31YW31XO31VM31YZ323O24131Z2324M31Z531Y131Z8320431ZB3214327A322R31ZJ2XR31ZI323H326P31U431ZN321K324D319Q324G321W324U2XA27G324L2XF27G2BO2WG31YN322L320G321432522XA32543241322V327U320P3245327R2K6322831NO27G325D31ZT325F321O325X32043282323A32633284323E325P31ZT325R31U6326A31YT31ZT326Y323624124K328Y24N31ZV27G3290326T31UC24124M24124P3226326H322B325K320I322O3283329E326O31WM27G24O3289329724R24124Q327L31PP324F31M3321O327Q25X27S327T2XA27S3200329C323Q329E2XR31WX322A320L321O328632A23288329627S325A2YI27S328F321O328H31YN328J31YD325L323T314P323W31JC2X524S327H31WM27S326B320V32AE324832B2329Z321H24124V32A5325I31KQ325K32BC320J32BC329K31ZV27S326S3233328X32723271325G327332BI241327631WK327832AQ327C32A831ZD323C327E2YI327G3241328S31UP241327K31VX329U31VO31M3324H327I2AK32A125X2AK2BO31U0324P329D3263324S3241329Y31IN320C320E329D328L32A9323C32AB31YN32AD32CH32AF32B52AK32AI2XF2AK32AL31YN32AN321W32AP322M32AR329V2GO323C3239321A32C432CE31Y4328V32AM325W31Q2320432CN32BZ326232AV32DT325Q32DL32B131NO2AK321I329T2JR2BM32CB324T327I2ZI32CG2ZI32CJ31Y1320332AQ32CV325J322232E8312732CS31DF325I320I31YA31VO328L328O32BH31VT2ZI32582XF2ZI32D52XA2ZI32D8321W32DA31XP32A632DS2PK32DH2X625V323Y3221328R32EJ325U328G32DP321232DS32BX2YI2JD32632X5327C32DX2YQ329S32F0328U31X731Y832FU31Y832FB326X32DP32BO328I2WK31ZV2ZI32BT31ZT2ZG31Z92S032BY31VK323T2BO2AU327F2G02BJ2JD31VO323I24X27S329I2JN31FS312M31W1329I312M31SU2X525Y319I312M31HN319Q323I31222AF311K1P24031HK2X82XA31EQ2612BJ31NI2XA31XF32CY25X31EQ312E2XR31XF32HE31UT31XI32GE2XF31XI31XI26031FS31XF312E31CD31EQ32H82BI31XF315432H732H931FV31EQ31722Y8315J31XF2C926227631YZ32AQ325D32HB32HK241265279313G2XF31Y0317D313M31B22BJ31CQ32IL31C92XE32HC328B31VD32FT3297329931EQ24727G321924126F32I7312O311232JB31D2317F32DD1S32I72Z6311232JJ31RW32DD264315E323Y31VR24X31EO32J92X52QO2XR312232DA3122312231SY31S332632C926631JC320X31UT31XF32K831GZ312232HY31FV31S332BM2YI31S331S32KR312C32KL241313M2XR2C932KJ2XF2C92C925F31CA32KW24125E32I82K3319I2X531EQ314X32C22PC32JY2YI32K031JQ32K232DQ2XA32K531JC2C925G32K932DE32HH2TJ319I32KF31VN25X32KI31JQ32KP32KN32KK322832KR2YI32KT31JQ32L032KY312C32L032L22XR31EQ25H32L5323132JO2X531EO31UT312M3207323Y32IY32L932JT32L932JX31FV32LD31Q432LF32K432LN25X2C932AT32L3326331XF311132KE323231SU32LU31Q432LW31CA32KP32M032KV31YV32M3328B32M532M1328B32M82YI32MA32MC32L731CA2X528I32LB2XF32MR31CA32MT32KH32MV2C9326332KA31FV31XF32FD32NS32N432NW32KU32LH322832LX2XF32NA31FV32M231Q432M432KZ32NI32L332MB31GZ32L631L132J932MG31FV312M32OK31FS323I2BI31NO28I32B431NO27S31BA2Z3322H320R31XK32L932HS32JW32LS3122311S32OL328831SU312R31JQ32MI31H12RP32O8316U32GS322831SU32NT312C32NV319Q31S331EQ31Q431XF27S2X8312C32O224125M28R313H2XA2Z3311H313L311231X132IT2XB32PU32Q8311K2Y7313S25X31XF32Q6315732IQ2SE313P324A32QM31XF32Q232IP32Q5315H2XZ32QB27631SF2PC32LO32QK32IZ32QI320532QO324B32Q032QS32Q425X2Z3313U2JM32QX328B27932RF32QA31122Y732RF32QD31ZD32R131PX31S032LE312731NI319Q2C931A232M9241317T31Q431EQ31EQ31SY31XF31B732HQ32ND31Q432HU24132NG32HT24131XI32M832IK2Z332BM2IU32QU2Z332OA32SL32KQ31FS31EQ2Z331SA32IR31FV31XI31T42YI32SA26P31FV2Z32RP31UT31Y52XW31UT2ZB26Q319I31XI2ZB32FS32QM31YS31XI2DT2XA32LR2IU32KO32RT32SQ314832KB32RZ31JQ32Q031SY31XI32S632T132S831CA2Z32Z332SC32SO32NJ2XF31Y532SJ32U432DM32SN25X31Y531Y5313M319Q31XF31Y531SA32TG32ON32RB310A312C32TZ24132T02XR31Y52PI32T724132US31FV31Y832UV319Q2Z331Y832TD2XA31XI31YS2Z331YM32LT32SE315D32R332RW24132PY324B32L032R932QM31772C432RF32RR32R032MW3232315I32NC2ZI27E32QP2XA32VG32Q332QM31GF32VK32Q92BJ32QH32NY311E315J32VC26V31CL32NC2C932VH32LO2Z52G532RF31U032RF31JE32RF2ZG32RF31WP32RF2Y331ZB32VV32VP31FS32VM32NU32TM32RV31O732NK32TQ32S1323132S427A31JC31XI32O725X32SA32U132X832V932SG2XF32SI2XD32JQ32SO32U932UN32UD32WZ32SS32HX312631NO31XF275314K319Q32TJ32N932WW32WZ31FN2YI31XF32S031CA32TS32SV32X4317R329932QU32X732UN32XA32UN32U32XA32U531JQ32UB31LT31CA32YI32XL32QM32UG31FS32UI32OV32SY27432EH32O831XI2XI32IK2C932IN2WI32RA31EQ31B0311A32VL2BJ32RI32IV32NC32IY32W62A632W832VU32VO32WB32VX32LO317K2UE32WG32Z7317J32ZN311K32WL311232WN311231GC32WO32W232NC31XF2C4323G32TI2D33301324C315X31L7');local I=(bit or bit32)and(bit or bit32).bxor or function(e,o)local l,n=n,a while e>a and o>a do local X,I=e%2,o%2 if X~=I then n=n+l end e,o,l=(e-X)/2,(o-I)/2,l*2 end if e<o then e=o end while e>a do local o=e%2 if o>a then n=n+l end e,l=(e-o)/2,l*2 end return n end local function o(o,e,l)if l then local e=(o/2^(e-n))%2^((l-n)-(e-n)+n);return e-e%n;else local e=2^(e-n);return(o%(e+e)>=e)and n or a;end;end;local e=n;local function X()local X,n,l,o=F(Y,e,e+3);X=I(X,145)n=I(n,145)l=I(l,145)o=I(o,145)e=e+4;return(o*16777216)+(l*B)+(n*C)+X;end;local function A()local l,n=F(Y,e,e+2);l=I(l,145)n=I(n,145)e=e+2;return(n*C)+l;end;local function C()local l=I(F(Y,e,e),145);e=e+n;return l;end;local function K(...)return{...},d('#',...)end local function D()local l={};local f={};local i={};local d={[4]=nil,[n]=i,[3]=l,[8]=f,[7]=nil,};local l={}local S={}for B=n,C()==a and A()*2 or X()do local l=C();while true do if(l==a)then local o,A,X='',X();if(A==a)then l=o;break;end;X=c(Y,e,e+A-n);e=e+A;for e=n,#X do o=o..t[I(F(c(X,e,e)),145)]end l=o break;end if(l==2)then l=(C()~=a);break;end if(l==n)then local X,e=X(),X();local I,X,e,o=n,(o(e,n,20)*(2^32))+X,o(e,21,31),((-n)^o(e,32));if e==a then if X==a then l=o*a break;else e=n;I=a;end;elseif(e==2047)then l=(o*((X==a and n or a)/a))break;end;l=(o*(2^(e-1023)))*(I+(X/(2^52)));break;end l=nil break;end S[B]=l;end;for e=n,X()do i[e-n]=D();end;d[7]=C();for t=n,X()do local e=C();if(o(e,n,n)==a)then local l=o(e,2,3);local Y,c,C=A(),A(),A();local I=o(e,4,6);local e={[4]=c,[n]=C,[6]=Y,[2]=nil,};if(l==a)then e[4],e[2]=A(),A()end if(l==3)then e[4],e[2]=X()-B,A()end if(l==2)then e[4]=X()-B end if(l==n)then e[4]=X()end if(o(I,n,n)==n)then e[n]=S[e[n]]end if(o(I,3,3)==n)then e[2]=S[e[2]]end if(o(I,2,2)==n)then e[4]=S[e[4]]end f[t]=e;end end;return d;end;local function i(e,c,I)local l=e[7];local X=e[8];local B=a;local o=e[4];local e=e[n];return function(...)local F=d('#',...)-n;local C={};local d=K local o={};local A={...};local Y=l;local X=X;local D=e;local l=n;local f={};local t=-n;for e=a,F do if(e>=Y)then f[e-Y]=A[e+n];else o[e]=A[e+n];end;end;local e;local A;local Y=F-Y+n while true do e=X[l];A=e[6];if B>a then o[e[n]]=e[4];end if A<=50 then if A<=24 then if A<=11 then if A<=5 then if A<=2 then if A<=a then o[e[n]]=e[4];elseif A==n then local c;local A;o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];l=l+n;e=X[l];o[e[n]]=(e[4]~=a);l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];l=l+n;e=X[l];o[e[n]]=(e[4]~=a);l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];else local A;o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]={};l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))end;elseif A<=3 then if not o[e[n]]then l=l+n;else l=e[4];end;elseif A>4 then local a;local A;A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];else local A;local I;I=e[n]o[I](o[I+n])l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];I=e[n];A=o[e[4]];o[I+n]=A;o[I]=A[e[2]];l=l+n;e=X[l];I=e[n]o[I](o[I+n])l=l+n;e=X[l];do return end;end;elseif A<=8 then if A<=6 then local A;o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]={};l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];elseif A==7 then local l=e[n]o[l](S(o,l+n,e[4]))else local S;local A;A=e[n];S=o[e[4]];o[A+n]=S;o[A]=S[e[2]];l=l+n;e=X[l];A=e[n]o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];A=e[n];S=o[e[4]];o[A+n]=S;o[A]=S[e[2]];l=l+n;e=X[l];A=e[n]o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](o[A+n])l=l+n;e=X[l];l=e[4];end;elseif A<=9 then o[e[n]]={};elseif A==10 then local I=e[n];local A=e[2];local X=I+2 local I={o[I](o[I+n],o[X])};for e=n,A do o[X+e]=I[e];end;local I=I[n]if I then o[X]=I l=e[4];else l=l+n;end;else local c;local t;local C;local A;A=e[n];C=o[e[4]];o[A+n]=C;o[A]=C[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];A=e[n]t={o[A](o[A+n])};c=a;for e=A,e[2]do c=c+n;o[e]=t[c];end l=l+n;e=X[l];l=e[4];end;elseif A<=17 then if A<=14 then if A<=12 then I[e[4]]=o[e[n]];elseif A>13 then o[e[n]][e[4]]=o[e[2]];else local X=e[n];local I=o[X]local A=o[X+2];if(A>a)then if(I>o[X+n])then l=e[4];else o[X+3]=I;end elseif(I<o[X+n])then l=e[4];else o[X+3]=I;end end;elseif A<=15 then o[e[n]]=o[e[4]]-o[e[2]];elseif A>16 then local l=e[n]o[l]=o[l](S(o,l+n,e[4]))else local c;local A;o[e[n]]=I[e[4]];l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];l=l+n;e=X[l];o[e[n]]=(e[4]~=a);l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];l=l+n;e=X[l];o[e[n]]=(e[4]~=a);l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];end;elseif A<=20 then if A<=18 then o[e[n]]=o[e[4]]/e[2];elseif A==19 then o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];if(o[e[n]]==o[e[2]])then l=l+n;else l=e[4];end;else l=e[4];end;elseif A<=22 then if A==21 then if(o[e[n]]==o[e[2]])then l=l+n;else l=e[4];end;else c[e[4]]=o[e[n]];end;elseif A==23 then local a;local A;o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];else o[e[n]]=o[e[4]];end;elseif A<=37 then if A<=30 then if A<=27 then if A<=25 then local F;local c;local Y;local t;local B;local f;local A;A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];A=e[n];f={};for e=n,#C do B=C[e];for e=a,#B do t=B[e];Y=t[n];c=t[2];if Y==o and c>=A then f[c]=Y[c];t[n]=f;end;end;end;l=l+n;e=X[l];A=e[n];F=o[e[4]];o[A+n]=F;o[A]=F[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];elseif A==26 then local X=e[n];local A=o[X+2];local I=o[X]+A;o[X]=I;if(A>a)then if(I<=o[X+n])then l=e[4];o[X+3]=I;end elseif(I>=o[X+n])then l=e[4];o[X+3]=I;end else for e=e[n],e[4]do o[e]=nil;end;end;elseif A<=28 then do return end;elseif A>29 then local A;o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];else local S;local A;o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];for e=e[n],e[4]do o[e]=nil;end;l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];A=e[n];S=o[e[4]];o[A+n]=S;o[A]=S[e[2]];l=l+n;e=X[l];o[e[n]]=e[4];end;elseif A<=33 then if A<=31 then local l=e[n]local X,e=d(o[l](S(o,l+n,e[4])))t=e+l-n local e=a;for l=l,t do e=e+n;o[l]=X[e];end;elseif A==32 then if not o[e[n]]then l=l+n;else l=e[4];end;else local X=e[4];local l=o[X]for e=X+n,e[2]do l=l..o[e];end;o[e[n]]=l;end;elseif A<=35 then if A>34 then o[e[n]][e[4]]=e[2];else o[e[n]]();end;elseif A>36 then local F;local c;local Y;local t;local f;local B;local A;A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];A=e[n];B={};for e=n,#C do f=C[e];for e=a,#f do t=f[e];Y=t[n];c=t[2];if Y==o and c>=A then B[c]=Y[c];t[n]=B;end;end;end;l=l+n;e=X[l];A=e[n];F=o[e[4]];o[A+n]=F;o[A]=F[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];else local l=e[n]local I={o[l](o[l+n])};local X=a;for e=l,e[2]do X=X+n;o[e]=I[X];end end;elseif A<=43 then if A<=40 then if A<=38 then o[e[n]]=o[e[4]][e[2]];elseif A==39 then o[e[n]]=o[e[4]][e[2]];else local l=e[n]local X,e=d(o[l](S(o,l+n,e[4])))t=e+l-n local e=a;for l=l,t do e=e+n;o[l]=X[e];end;end;elseif A<=41 then local c;local A;o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];l=l+n;e=X[l];o[e[n]]=(e[4]~=a);l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];l=l+n;e=X[l];o[e[n]]=(e[4]~=a);l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];elseif A>42 then o[e[n]][e[4]]=e[2];else local A;local S;c[e[4]]=o[e[n]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];c[e[4]]=o[e[n]];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];I[e[4]]=o[e[n]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];S=e[n];A=o[e[4]];o[S+n]=A;o[S]=A[e[2]];end;elseif A<=46 then if A<=44 then local A=e[n];local X={};for e=n,#C do local e=C[e];for l=a,#e do local l=e[l];local I=l[n];local e=l[2];if I==o and e>=A then X[e]=I[e];l[n]=X;end;end;end;elseif A==45 then local e=e[n]o[e]=o[e](o[e+n])else local A;o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]]/e[2];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]();end;elseif A<=48 then if A>47 then local e=e[n]o[e](o[e+n])else local e=e[n]o[e]=o[e](o[e+n])end;elseif A>49 then if(o[e[n]]==o[e[2]])then l=l+n;else l=e[4];end;else local a=D[e[4]];local S;local A={};S=Q({},{__index=function(l,e)local e=A[e];return e[n][e[2]];end,__newindex=function(o,e,l)local e=A[e]e[n][e[2]]=l;end;});for I=n,e[2]do l=l+n;local e=X[l];if e[6]==81 then A[I-n]={o,e[4]};else A[I-n]={c,e[4]};end;C[#C+n]=A;end;o[e[n]]=i(a,S,I);end;elseif A<=75 then if A<=62 then if A<=56 then if A<=53 then if A<=51 then local l=e[n];local X=o[e[4]];o[l+n]=X;o[l]=X[e[2]];elseif A>52 then local A=e[n];local I={};for e=n,#C do local e=C[e];for l=a,#e do local l=e[l];local X=l[n];local e=l[2];if X==o and e>=A then I[e]=X[e];l[n]=I;end;end;end;else c[e[4]]=o[e[n]];end;elseif A<=54 then o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];if(o[e[n]]~=o[e[2]])then l=l+n;else l=e[4];end;elseif A==55 then local A;o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]={};l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))else if(o[e[n]]~=o[e[2]])then l=l+n;else l=e[4];end;end;elseif A<=59 then if A<=57 then for e=e[n],e[4]do o[e]=nil;end;elseif A==58 then o[e[n]]=o[e[4]]/e[2];else o[e[n]][e[4]]=o[e[2]];end;elseif A<=60 then o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];if(o[e[n]]~=o[e[2]])then l=l+n;else l=e[4];end;elseif A==61 then local X=e[n]local I={o[X](o[X+n])};local l=a;for e=X,e[2]do l=l+n;o[e]=I[l];end else o[e[n]]=e[4];end;elseif A<=68 then if A<=65 then if A<=63 then local I;o[e[n]]=(e[4]~=a);l=l+n;e=X[l];I=e[n]o[I]=o[I](S(o,I+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];I=e[n]o[I]=o[I](S(o,I+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];elseif A>64 then local c;local A;o[e[n]]=(e[4]~=a);l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];A=e[n];c=o[e[4]];o[A+n]=c;o[A]=c[e[2]];l=l+n;e=X[l];o[e[n]]=(e[4]~=a);l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];else o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];if(o[e[n]]==o[e[2]])then l=l+n;else l=e[4];end;end;elseif A<=66 then local A;o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))elseif A>67 then local e=e[n]o[e]=o[e](S(o,e+n,t))else local X=e[n];local A=e[2];local I=X+2 local X={o[X](o[X+n],o[I])};for e=n,A do o[I+e]=X[e];end;local X=X[n]if X then o[I]=X l=e[4];else l=l+n;end;end;elseif A<=71 then if A<=69 then o[e[n]]=I[e[4]];elseif A>70 then local l=e[n]o[l]=o[l](S(o,l+n,e[4]))else l=e[4];end;elseif A<=73 then if A>72 then o[e[n]]=(e[4]~=a);else local a;local A;o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];end;elseif A>74 then local e=e[n]o[e](o[e+n])else if(o[e[n]]~=o[e[2]])then l=l+n;else l=e[4];end;end;elseif A<=88 then if A<=81 then if A<=78 then if A<=76 then o[e[n]]=o[e[4]]+o[e[2]];elseif A>77 then o[e[n]]=o[e[4]]+o[e[2]];else local a;local A;o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]={};l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];end;elseif A<=79 then do return end;elseif A==80 then local Y;local B,F;local C;local A;A=e[n]o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];A=e[n];C=o[e[4]];o[A+n]=C;o[A]=C[e[2]];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];A=e[n]B,F=d(o[A](S(o,A+n,e[4])))t=F+A-n Y=a;for e=A,t do Y=Y+n;o[e]=B[Y];end;l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,t))l=l+n;e=X[l];o[e[n]]();l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];A=e[n];C=o[e[4]];o[A+n]=C;o[A]=C[e[2]];l=l+n;e=X[l];A=e[n]o[A](o[A+n])l=l+n;e=X[l];do return end;else o[e[n]]=o[e[4]];end;elseif A<=84 then if A<=82 then local X=e[4];local l=o[X]for e=X+n,e[2]do l=l..o[e];end;o[e[n]]=l;elseif A==83 then o[e[n]]();else local X=e[n];local A=o[X+2];local I=o[X]+A;o[X]=I;if(A>a)then if(I<=o[X+n])then l=e[4];o[X+3]=I;end elseif(I>=o[X+n])then l=e[4];o[X+3]=I;end end;elseif A<=86 then if A>85 then local a;local A;A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A](o[A+n])l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]][e[4]]=e[2];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];l=l+n;e=X[l];o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];else o[e[n]]=o[e[4]]-o[e[2]];end;elseif A==87 then o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];if(o[e[n]]==o[e[2]])then l=l+n;else l=e[4];end;else o[e[n]]=(e[4]~=a);end;elseif A<=94 then if A<=91 then if A<=89 then local a=D[e[4]];local S;local A={};S=Q({},{__index=function(l,e)local e=A[e];return e[n][e[2]];end,__newindex=function(o,e,l)local e=A[e]e[n][e[2]]=l;end;});for I=n,e[2]do l=l+n;local e=X[l];if e[6]==81 then A[I-n]={o,e[4]};else A[I-n]={c,e[4]};end;C[#C+n]=A;end;o[e[n]]=i(a,S,I);elseif A>90 then local l=e[n]o[l](S(o,l+n,e[4]))else o[e[n]]=I[e[4]];end;elseif A<=92 then o[e[n]]=c[e[4]];elseif A==93 then local A;o[e[n]]=o[e[4]];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n]o[A]=o[A](o[A+n])l=l+n;e=X[l];if(o[e[n]]==o[e[2]])then l=l+n;else l=e[4];end;else local A;o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]]-o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]]+o[e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=c[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]]-o[e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];o[e[n]]=o[e[4]]+o[e[2]];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]][e[4]]=o[e[2]];end;elseif A<=97 then if A<=95 then local X=e[n];local l=o[e[4]];o[X+n]=l;o[X]=l[e[2]];elseif A==96 then o[e[n]]={};else local a;local A;o[e[n]]=e[4];l=l+n;e=X[l];A=e[n]o[A]=o[A](S(o,A+n,e[4]))l=l+n;e=X[l];o[e[n]]=I[e[4]];l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];for e=e[n],e[4]do o[e]=nil;end;l=l+n;e=X[l];o[e[n]]=o[e[4]][e[2]];l=l+n;e=X[l];A=e[n];a=o[e[4]];o[A+n]=a;o[A]=a[e[2]];end;elseif A<=99 then if A==98 then local X=e[n];local I=o[X]local A=o[X+2];if(A>a)then if(I>o[X+n])then l=e[4];else o[X+3]=I;end elseif(I<o[X+n])then l=e[4];else o[X+3]=I;end else local e=e[n]o[e]=o[e](S(o,e+n,t))end;elseif A>100 then o[e[n]]=c[e[4]];else I[e[4]]=o[e[n]];end;l=l+n;end;end;end;return S({i(D(),{},E())()})or nil;end)(65536,"",{},1,0,256,tonumber)
end)

HubsSection:NewButton("Arctic Hub", "...", function()
    loadstring(game:HttpGetAsync("https://polar7.wtf/Arctic/ArcticHub/Loader.txt"))()
end)

HubsSection:NewButton("Cumlin Hub", "...", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/cumlin21/CumlinHub/main/1.txt"))()
end)

HubsSection:NewButton("KeyBrew Hub", "...", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/borntodiekuv/KeybrewHub/main/Main"))()
end)

HubsSection:NewButton("Legacy Engine", "...", function()
    loadstring(game:HttpGet('https://github.com/LeanNBud/LegacyEngine/raw/main/DBOG/loader', true))()
end)

HubsSection:NewButton("Proxima Hub", "...", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/TrixAde/Proxima-Hub/main/Main.lua"))()
end)

HubsSection:NewButton("Gura Hub", "...", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/momenthubv3/Gura-Hub/patch-1/loader.lua'))()
end)

HubsSection:NewButton("Zues Hub", "...", function()
    loadstring(game:HttpGet(("https://pastebin.com/raw/QM211VHT"),true))()
end)

HubsSection:NewButton("Reviz Admin", "...", function()
    print("Clicked")
end)

HubsSection:NewButton("Lazy Hub", "...", function()
    repeat wait() until game:IsLoaded()
	loadstring(game:HttpGet("https://raw.githubusercontent.com/LioK251/RbScripts/main/lazyhub.lua"))()
end)

local Games = Window:NewTab("Games")
local GamesSection = Games:NewSection("Games")

GamesSection:NewButton("Mining Sim", "...", function()
    loadstring(game:HttpGet'https://raw.githubusercontent.com/RunDTM/miningsim2/main/rewrite.lua')()
end)

GamesSection:NewButton("KAT", "...", function()
    local Camera = game:GetService("Workspace").CurrentCamera
local Players = game:GetService("Players")
local LocalPlayer = game:GetService("Players").LocalPlayer

local function GetClosestPlayer()
   local ClosestPlayer = nil
   local FarthestDistance = math.huge

   for i, v in pairs(Players.GetPlayers(Players)) do
       if v ~= LocalPlayer and v.Character and v.Character.FindFirstChild(v.Character, "HumanoidRootPart") then
           local DistanceFromPlayer = (LocalPlayer.Character.HumanoidRootPart.Position - v.Character.HumanoidRootPart.Position).Magnitude

           if DistanceFromPlayer < FarthestDistance then
               FarthestDistance = DistanceFromPlayer
               ClosestPlayer = v
           end
       end
   end

   if ClosestPlayer then
       return ClosestPlayer
   end
end

local GameMetaTable = getrawmetatable(game)
local OldGameMetaTableNamecall = GameMetaTable.__namecall
setreadonly(GameMetaTable, false)

GameMetaTable.__namecall = newcclosure(function(object, ...)
   local NamecallMethod = getnamecallmethod()
   local Arguments = {...}

   if tostring(NamecallMethod) == "FindPartOnRayWithIgnoreList" then
       local ClosestPlayer = GetClosestPlayer()
       
       if ClosestPlayer and ClosestPlayer.Character then
           Arguments[1] = Ray.new(Camera.CFrame.Position, (ClosestPlayer.Character.Head.Position - Camera.CFrame.Position).Unit * (Camera.CFrame.Position - ClosestPlayer.Character.Head.Position).Magnitude)
       end
   end

   return OldGameMetaTableNamecall(object, unpack(Arguments))
end)

setreadonly(GameMetaTable, true)
end)

GamesSection:NewButton("Ninja Training Sim", "...", function()
    _, Protected_by_MoonSecV2, Discord = 'discord.gg/gQEH2uZxUk'


,nil,nil;(function() _msec=(function(e,o,l)local R=o[(0x5d+-64)];local H=l[e[(-0x4b+763)]][e[(31840/0x28)]];local S=(40-0x24)/(0x19-(4025/(0x198-233)))local C=(((2842+-0x56)/0x35)-50)-(0x4a-73)local A=l[e[(0x1f7-304)]][e[(0xd7eb/201)]];local g=(0x43+((0x263/(67+-0x36))+-113))+(-66+0x44)local M=l[e[(0x140bf/157)]][e[((192897-0x178eb)/0x76)]]local d=(0x130/152)-(((36596+-0x73)/191)/0xbf)local U=(0x20+(-23-((0x32d+-36)/0x6f)))local w=((-0x67-(-0x402/(3306/0x1d)))+96)local h=(((0x4f99-(0x262b70/244))/81)+-0x7b)local N=(0x13a/(0x4ad2/(0x71e6/(0x216-295))))local b=((151-((-11072/0xad)+0xa7))-46)local x=(107+(-0x17+((-10+-0x2e)+-0x1a)))local P=(((-93+(487-0x131))-81)/2)local t=((0xad4/((84+-0x6d)+0x97))+-18)local v=((1744-(187320/(36540/0xae)))/213)local u=(58-(4590/(0x8c+(-10615/0xc1))))local B=(124/(((0x97114/49)/0x9a)-51))local s=(((0x1302/(0x20-29))-862)/0xbe)local _=(((-124+(0x369-482))-0xbb)-77)local O=(-0x6d+(((-7720/0xc1)+0xe)+138))local f=((-0x29+(0x40bf/(0x2328/120)))/60)local D=(123/(3280/((0x5868-11352)/141)))local i=(((0x1bf3/(45-0x28))-777)/0xda)local c=(-0x15+(-0x29+((4500/0x12)-0xb9)))local V=e[(2837-0x5b7)];local K=l[e[(-44+0xf3)]][e[(971-0x20b)]];local Q=l[(function(e)return type(e):sub(1,1)..'\101\116'end)('одеиуурд')..'\109\101'..('\116\97'or'идтшоыиу')..e[(0x288+(-132+0x7))]];local p=l[e[(-67+0x24e)]][e[(1933-0x3f1)]];local y=(0x16-20)-(63-((0x27f4+-41)/0xa7))local m=((198-((9310/0x23)-0x9c))+-86)-(190/0x5f)local G=l[e[((-0x71+45684)/0xe5)]][e[(-85+0x1b5)]];local n=function(e,l)return e..l end local L=(0x59+-85)*(((0x2667+(-97+-0xe))/120)-77)local W=l[e[(-41+0x49c)]];local a=(0x39-55)*(0x124-(0x15d-(13320/0x48)))local J=(0x831-(2180-0x453))*(((0x1c7+-29)+-0x70)/0x9d)local z=((0x122-(414-0xfb))-0x4b)local j=(0x192/((37867+-0x4f)/188))*(0x30-46)local r=l[e[(0x8c7-1176)]]or l[e[(0x1078b/129)]][e[(0x8c7-1176)]];local k=((0x2da+(-0x24+-88))-0x15e)local e=l[e[(1341+-0x6a)]];local Y=(function(n)local r,o=2,0x10 local l={j={},v={}}local a=-d local e=o+C while true do l[n:sub(e,(function()e=r+e return e-C end)())]=(function()a=a+d return a end)()if a==(L-d)then a=""o=y break end end local a=#n while e<a+C do l.v[o]=n:sub(e,(function()e=r+e return e-C end)())o=o+d if o%S==y then o=m p(l.j,(G((l[l.v[m]]*L)+l[l.v[d]])))end end return M(l.j)end)("..:::MoonSec::..яшертыуиопасдфгххеиишоспыахспдрфгсихеядшопясаттыгуфаыидаехаушшояггсуртфшиешршссуурхдфефпиашссдыфиггпоядуооердтуытсшфафыихгпгдтиыягахыятыхипхрпгыоыепддеяаярсфдифргегшашупипеясохеудиуоыяяхсхрххеаятыфпитшихххгпыруфисгоееддятхяесяыыгыпрдтурятаытугидоисяафгшрафтггхгыыуасхаыясыягпяапрпфаисугеедгусяпаттрхиопепсписшисстсхепшодитяхсяышосгссехыфршшхеушхапсрдрягфпряодхутятаихооуеидоисяфастдгфпяехфяишресрытхыпурифоояшадфыдхфаярхгсошеедрутяыаутигоосеадфудефагтххяпшрефриошыфуыихоппрафсидеесгихяяаштегротеыдгуишааптагфодрадгухшядрыехрпирыфииишоспудхспдтшфгосеядшуешыаттыгсоиесдпуаясадтфггпшряфуиешыстуихупирсфпоишссдыфшяпхтягыоеефдтуыяусптогпохесфеуфягахуехшперпфтигшусиыохппарсфхифетсхуеяшаетргтоыеудауояааатсгдофегдхишшшсеырхтпуруфииошпсаысхдпфргфхояеодеурятаыоргиооепдсусядафтггхпяршфеирштсыыухипорпфаисшдсфыгххаятшгеоретдоууяиаотпгаоседдфугяхсяышхепрртфыиушпсоыпхапсрдффигшхдшушяеарттгиоуеидошуяаастдгфогехфяишгтсоытхыпуаирсфаоуеииахфпгрххефееедыутяуаутигопсисдсухяфахтххяпшттяпитшпсуыпхоппрагшяяшфдрыхяяаштргрооеыдуиуяоаптагфодефдгухшхсшыехрптрыфуиишодоыахспдтяфгихеядшишяраттыгиоиеодпуаыыадышггпшряфеиешпшгыыхупиыефписшссфыфяедттягшоерфдтууяуафыфгпоаесфауфяхахышхшпуыофтиышудыыохапархяшифшгсхиаяшартргагхеудоуоераатдгдофегфрпышшсеырягпырифииопгсаыххдпхрггеояештиуряпаытпгиоаепфяояядсштгятпярефеиоштсписхипорпгхисшфсфуеетаятшгепфетдуууяиефтпггосегдфишяхсяфухепортфоиушпсоыхутпстяффпошхдшушяиартояаоуеидооряаадтдхшсрехфяишефсрыыхыпуаяфоифшассыдхфпгрхусошеудруыяыаутигоггеадхудяхагтххяпшушфритшысиыихоппрдфсидшфсгудяяаштеидоаеыдууиихапгияхпгыесрипшясшыерахпапепфдоаехдрыгяшышгоихеядшаоудшуаарпгдпархдхифпшыыггохряетптхаыесдшаидффяяояшссдыфтршыаытххупуапуаяуаитоесппхурдашугсрыяхшпепарыгеисуруяхппарсехгдпеяидгурярауигоыеудиуояпгапхедыхрудхияшшяусоуяхааутугаофссудхдпфргршгыпшегддуияусатдгдидргфаигягсыытатрифеирштутфафдыпхяяфдпшдсфыгххаядшредрридыууяисатдгаоседфтугяхсяишхепрртфыиушисаыпядпсрдфхигеадяушяеарттгыоуеидаупядасудгфогехфяишшесоытшыпурифоипшассуухфсгрхгяошеедрутяоауыпгоопеддситяфагтхяепшрефуитшпсуыихоасрафсояшфдаыхяяашытгротеадуитяоаптагсодеффяухшысшытхраурыфуиашодшыахспдтхфгихетдшуояраттыхооиеодгуаядадтфггашряфшиошрсфыыхупирофпиашгсдурхгаштягшоеердтуыяпаитпгпоаесддуфягсяыяхшперрфтиышусиуихппарсурифшгсхуяяшаеыиетттредиуояпхрспуехдппртдриуетдпыпяиыфффиошпсадуыяргсспутедфдсурятаыодыдхуодргфтисшсдшрдпиршфеирисшадаыгхфаиыяфсеясфыгххяиаетхгосфдпууяиаоохетареятяиеяхсяышупхтпфтппфеесоыпхашяадттхяояетдуупяосшыотиеирсияяаастдтехгпутефеиушояяхфпурифоддопехатусяяаятрпуеедрутяыаутиефдпиифдудяфагашыыяшпгрдфииуеасдыдгдагтаггигеыдтирастегротудесфсысягсдушхыпярроашясшыеяыдарыфииишфспыахспддяфгояеядеуеяыатыыруоиепдпирясадтфяядыряфеиешостыыхуписсфписшссфыфяяпхуяыфоеетдтууяусятояхшаесдфуфшиахышхшпдррфопашусиыояепардфдифтфсхуяяшартргтоырохфуояаааышгдофеггхггшшсрырхыпытыфиоашпсаыгхдасргфхояешдеуряыаытпгиоаепгаусядагтгхяпярыфепрштсыыихиппрпгыисрдсфыгяяаятегеоыетфиууяиастпхуоседдфояяхсяыыхепартфыиуепсоыпххпсрхффигшхфеушяеапттхеоуеидоупяаастхгфптехфеишшесрытхупурафоиашадфыдхфпхрхгоошеедриуяыаутпгооаеадсудяфагтххшпшртфриышысаыихоппрафгидшгсгыхехаштегроыеыдууияпаптагсодрадгухшяеыыехрптрыфуииугхпрхярпдрффгфеохрыааишяуаутпеяегдпуаясгтгяхясфыыхгфешсстыыхугаттптфуеаиесгяпсртагшоеерясдаиахаафысяяптехфесастыяхшпеоырпдшугхдеаяапарсфддхорехддуаяыатыогаоашафдиошдадырхесыдхияшшсеырхтспиуриидшпсаысурхгасттхрепдеурятхпасыргфппрпффояхаыогхпяршшофдоушаапыдяаахрхгфохдрыгххаяоуыогоперпфпфпагтпгаосыояпфугедтдхяыпрртфыоошасоыпхаатрдффигрхдяушяеарттгыосеифаупяаафтдхтогехфяишшесрытхыпорифаипрассыдхфпгрхгяофеегрутяыаутигоопртдсодяфагтххяпшрефгитеисуыихаппрдфсидшффяыхяяаттегиотеыдуипяоаптггсппефдгухеесшыехоптруфуиишоспыахспгрфгрихеедшитяраттогуопеодпуашфадтфхеохруфшиешрдуыыхупдрофдиашссдуххгпхтугшоаердтуыяуаитогдоаршддухягахыяхшперрфииышисиыохппарсфдигшгсхуяяшаетргтоыррдиуояпшфышгдофегштгуиуеядиуипургфииошпяфдаиягыадтшгшотдруфятаытуеггфпфшффяигерсиыехыепфаирштсыаптхгсипшпафтыфдыхяиаятшгефиопршдсиишиссыгияредфугяххруясахоышпхпгшисоыпхапсидресгыпдуушяеарашигяоогяиодтыастдгфогехфяппыеасыгхыпуришггеодеяахуешясытыхроедпутяыауяытыотхесогухесетххяпшппртгшиасиуохоппраефгшофеадоуряесутогоиорафуиаяасшыяпхефдгухеестыехрпттшфуиишофпыахспдрффгихердшитяраттигуптеодпуаясадтфггохрефшитшрфтыыхупирофпиашдсдифхгпхтягшоеердпуыеуаитогпоаесддииягдшыяхшптррфуиышусиуахппаргфдошшгсхуяшраетргооыршдиуояпсдтсгдпеегфоияшшсеырхтпырофиифшпсдысягпфрггеояердеурятситугиодепфяусядафуягхпяруфеисштсыыуяппорпгяисерсфыгххаятшгеоуетдсууяпаотпгаоседдфишяхсшышхепрртфыиушосоыпхапсрдффигшхдоушяеаратгпоуеидодсоршхсштфпаехфяишоахудоытярояеягыоуяааииедытыгяошееруфоиияхсытхрыефдсудяфешдтыесорефритшыдсыихоппрафсидофхгхояташтегргиофеифпггаптагсодефдгыхтхфеыехрпттиядиишсспыдхспдрффггееядтуеяуаттугуофыыдпуфяссртфгхохряфшиуростыыхупгрофаиаефхеыфяшпхтегшоеердтдояуаатогдоаедддуфирахырхшптррфтиыеояоыохдпатрфдифшгфшдшяшаутргпоыеудииаяпааыягдпыегдхияшшсеырхапыруфииошпддысхдатрггиояешдеуиятаытсгиаыепдсусядяфтгхопярыфеирштдииехиаерпффисшдсфигххаятсгеофетддууеиаотпхыоседдфиеяхсяышхеаяртффиушисоыпхапстаффоушхдяушяеарттхяоурыдоусяадстдгфппехфсишшрсрытхыпутефоисшасфыдхфпгрхгсошефдруияыдутигоптеафуудшрагтххяпшрдфриушысоыихоппрафхидеусгупяяаштегрофеыдпуияаапуагсодрядгиошясиыехияорыфсииеыспысхсагирфготеядруеяраттыттоиефдпусяссятфггхтряфыиешыстыыхупиуифпиашссфыфхгпхтргшоеердтитяуаитоерогесддуфиышясфыурграфтиышушгсфуфяшаятахртыдпуяяшаеоатпхпипедфаихшрагышраегдхияшшсеырруфыригоиошпсаафушяфаатогроерудоуохосаыухаоаршфяаысытггхпяоттшгиыдерсоыохсгыфгисшдсффыуяяпсыяпооетдыуутпшисоыфхххгфругяхсяупргутхтыртгырсоыаярпсрдфффеуугсууферагятсфяяфдоупяаастдгфаеухаеиишесрытраядпдтугфофсрушхфпгрхыыгфпиеудхедсятигоопияртфгиеяшстуеяипитыпяшысуыияадхрафдидшхсгыхяяашдыгроыеыдиуияаапыарсодегдгифшясшыеяыдарыфииишаспыахспддяфгояеядеуеяыатуыуеоиепдпусяссатфштядряфеиешдстыухуашроффпхшссдыфяипхтшгшоутодтуыяусштогаоаесхсуфягахышхшперргуасшусоыохапарсфдпфпдсхушяшартргиоыродиуоядааыягдофегдхияшшсрырхипырофипошпсаыдхдпгрггдоятшдеуряыаытигипяепгаусядагтгхяпятяфеоыштсыыпхипгрпфаисегсфыгяраятдгеоретфиууяиафтпхроседдфояяхсяыихепиртфыиушисоыпхфпстеффояшхдяушяеатттгооуеодоисяаастфгфпыехфяишетсрытхипутрфоипшассыдхфпхрхгеошердруояыаутигоодеаддудяфффтххяпшррфритшысиыихоппрагпидшфсгясяташтегрхсоуехфспяапхухыодефдгфяоыеыдшыыяпагрсфгиххрурхспдрфетхтогетфуудшрсрыппсегдпуаяспдутодясдиудппшпстыыхугаипгшыпдуряпиярпхтягшфипшеуфтигпхыягпоаесшхфдоехисгырхрпуягошшусиыотеяосштсгооршедыиршоаоыухпеудиуояпаатсртдфехфуияшшсесаыпяппфрдгуохяиудхдпфргршгыпшегддуияусатдгдидргфаигягсыытяррыфеирштшдсиутхфппгтисшдсфаыутштпттихыпаегдпуддртпгаосргяругшясяыдхепрртфыхпшиспыпхспсргффогухдяуеяеауттгыоурпхгупясасыигфогехфяхтшестытхупурпфопппуссыфхфпхрхгроштоырутяуауыягооаеадфудшшфртххяпшрсфриышысуоухоппрафдидшфсгишруаштргрпшеыдууиеоххтагдодегдгифшядрыехрпирыгеиишоспыахспдргфгоееядруеераттыгиоиепдпугясддтфггпяряфеиешастиыхупирпфписшсдыыфхгпхтягтоеердтуыяусптогпогесфтуфягахуехшперофтисшусиыояспарсгеиферсхуяяшсттргтодеуфшуояпаатсгдофредхиишшстырхтпыруфоиошфсаыдхдахргфхошешдрурятаытугиооеадаудядагтгхрпяршфеиршисыыихипоуофаисшдсгыгххаятегеоретдыишяиаотпаппыеддфугыышпдрыигупптигдидеапряепсрдфффхптртфяияядсетхдяегдоупяашесшушхыптрггихпсррпхппурифогяисеодшриаорхгяошупеофоыоясспыгхеофряспшыагтххягшатртфиопшхсаыфудрафсидшфсгыхяягшохгпотеыдуадигягсоыхххеыфеухшясшдпытхфапшяоошоспыатфяшафтагоореефууояопоыахупаеафшиядртфггохтеяииештстыохупирофпхфшссфыфххпхтегшпеирдтууяуаптогпоарфяеуфяхахырхшперрфтхошусоыохапарффдпфпасхушяшартргуоытдттуояаааытгдогегфрияшыфиырхтпырхфиипшпсгояхдпфрггпояеедеуррраытугиопепдаусшггртгхяпяруфеирштфыпдхиппрпфсисеесфияххаяттгеогетдыууяиаотпгсосехдфияяхфяышхептртфуиуеясоипхапсрфффихшхдиушееарттгуоуеодоуаяасфтдгфпшехфоишшесрытхыпурофоидшасдыдяхпгрхгшошеддрутяыаутигооаеаддудягагырхяпшрефриишысиыиходорафсидшгсгыхяяаетегротеыгоуияоапсфгходефдгфуишшгсихыптрыфуиишоспппрсхфрффгихеядшееыугтятгдоиеодпфшшеушшпшергиффииешрстсрряяфеыфядхшрдеыфхгпхыиифыгрспяуаефадтогпоаугрсфширеесяхиперрфтфосадхясееышиуфдифшгсхуятшхеоруаофеудиуотссошуугаухтытперпсеырхтпыруфиооыпефурхдпфргшыирдгуадиепорхшдфооепдаусядефпшехярруфеирштеысиуяяаадоуошшдсфыгтеяяасрагторсфуаяиаотпушгдпытшефеясяышхегыпптыгеояшссаугяяаяряхеогредеупяордгхоуеидосяухшхпхыеяяаырпфтиифаысхыпурияоогфсетиесошетшгяошеедрутоыхаоируердрутяыаутишоехдсрофритшыяугпыхфусфпштгерсгыхяяххдсишошгшдоисшяаптагссфшеыхгфрдпяфдрдофрыфуиишоспшаыяфдяхгыихеядшсршяушатгатуоедаитясадтфртхоаерудыиоеудсысяпрягшиашссдсяуфшроотхгтотеиетягаитогпсгррафурфаыудаыеуыррфтиышусипотгфаяфгшифшгсхсштедыыафхсхеддиуояппяеядуопдиупшдшисеырхтфаадрдгуофефыряепфргфхдыяиаддедрядоргиооепдасиядафтгхипяршфеоыштсыыихистрпфаисегсфыгяшаяыягеоретфиууяиастпяшоседдфояяхсяыыхепгртфыиушисоыпхспстяффояшхфеушяеаыттяшоуеидоисяаастхгфашехфяишетсрытхппурсфоипшадфыдхфаррххгошеедрутяыаутпгоогеадфудшхагтххрпштгфритшыдоыихопфрагыидшфсгишяяаштигроаеыдууишааптахшодтшдгухшясшыехрпирыфдиишаспудхспдтшфгпсеядшуешыаттыгсоитидпуаяссгтфггпыряфпиешрстуихупирхфпидшссдыфхгпхтягыоееадтуияусптогпохесгоуфягахуехшперпфтофшусиыояспарсгрифтясхуяяшсттргтофеудауояпаатсгдофррдхиошшстыряупыруффиорысаысхдахргфхоиешфхурятаыыогиооршдаияядафтгяшпяршфсирешсыыухипорпфаошшддуыгяшаяыргеоресдыоеяиаотпхдоседфыугшссяышхеаыртфыихшифоыпхапстгффигепдяуаяеарттгыоуеидхупштастггфаяехфяипшедхытхыпутпфоиперссиухфпгрххеошеедфутшсаутигопсеадсиияфдитххяпшрефритшфсууехопсрафсидшфсгыхяоаштргрпуысдууояоситагсодефегухшесшыехрптрыфуппшосаыахфпдтяфгортыдшуеярфгтыгиоираххуашшадыфггохрягрояшрссыыяспирофпиашссдурхгаштягеоерыдтуыядаитпгпоаесгдуфягсыыяхипетыфтоишусиуяхпасрсфдифшгсхуяяиаетсгтоиеугиуояпсятсхеофтхдхпяшшсеыпхтпсруфгиорпсаысяепфттфхпсешдеурятафтугдооепдаусядафытгхпоршфриршагяыухопоуифаидшдсхыгярдытшгеорыедыуияиаоиогаоседдгугяхсяышхепрртфыохшисоыпаупгрдффигуяетдышиарттгыоуеидотптпигтдгфогехфяишыпхрогхапурифосстсдпррадортргяошеееадыиеясдггоопеадсудтфххохфыпсрефритысшхдпыфгдпхтфхеоерятыяяаштегротгышдаиехахтагсодиеттфтигеыдыдыпсрыфуииихшгдгуаяаапыияиеяпруояраттыраяатпяышаиуяфтфггохряфшхеыахтсыяяпирофпдшоярясяуршшсутагыоогсупяуаитортпигреоаишуахыяхшгтыясошиишдуеооррртдфдифшгшшдыишягадтигупаедддыдшгсаыгггпыртыышисеырхтхипсяетддпысухятпфргфхфрпяруасиеяиаитаояефдаусядетахыоятшуфоирштсыпаыдятпгтггятрдтыгххаяаотихиосеафтифгетхгаоседпшпаупыдпуидгярафыиушиоуписяесыодуыяеыдяушяегыиугсухгрытсяяаастдххдтехфшишеосрытхыпусафоиашасдыдххпгтхряошердругяыаутихасхеаддудерагтххяпшсыфриышысиыихаппыаыиидшгсгуяяяастеяпяшеыдиуишшаптсгспиеффептшясшыехдптруфуисрфспыахсаурффхихеяхяуеяраттугуоиеофсаяясафтфхрохряфшпеисстыухупорогииаефсдыфяшпхышгшоеердтуыяуаотогдоаефддофягахышхшпрррффиырусиыохапардфдпешгфхуяяшартргыоыефдииаяпаатггдогегдхияерсеырхопытпфииошпддысхдаерггхояешдеиыятаытдгипаепдаусшгафтгхупярифеирштсыыухипдрпгшисшгсфыгххаятегеоиетдууушпаотпгсосршдфугяхфяышхептртфуиуеысоусхапсрхффохшхдяушяеарттгуоуеадоусяадстдгфохехфшишшссритхыпурофоиашафяыдшфпгрхгшошердрусяысотигоодеаддудяфагушхяпшруфроишысуыияаппрагяидешсгыхяясртегроаеыфгуияоапыдгсодртдгидшясшыехрптрыфаиишхспыдхспдрффгояеядыуеятатыигуоиепдпухясадтфягохряфеиештстурхуапрофпифшсдфыфхгпхтягшоеетдтуояуаптояпоаесдфуфяхахыпхшсеррфтиушусоыоягпаысфдифшхсхушяшаптрхуоыеудауояааатсгдпхегдхитшшдыырхтпытофииошгсауахдпфргхшояешдоуршяаытугипаепдаиеядсытггхпяршфеиршосыыфхипарпфаисшдсгыгяраятегепыетдыуияиафтпгаостддфугшясяыехеашртгииушиссыпяспсрдффигшхдяуеяеауттгиоутидоупясастфгфпиеххяишшестытхупутдфоппшассыфхфпхрхгиошртдрутяоаутогоопеаффудяфсетхярпшрефроушысуыдхосерафсидехсгыхяуашыпгротеыфоуияосятаггодефдгухшясшыухрпсрыфоиишоспыахдпдтшфгояеяфруеяраытыхаоиеодпидясадтхггпшряфшиешрстыыхипирафписшсдяыфхгпхтягтоеетдтуырыаитогпосесддуфяхахыяхшпетефтиышурфуяхппарсехгдпеяидгуряраудпосеудиуохххгиыхшуыфтхуиышшсеырруятаытагддыдяысхдпфорыыгыохруфуутаптугиоопяесфоишыстггипыршфеироиешдсыаярхпфаисшдсфыгххстошдиоаетдыууугяфсфышхяпатрефшосяышхегыоехоуохятыгпыефыфыгшигшхдяфоурядсояфоуеидоупяаасохефштрпфяишшехаспупгппдтагхоршгдшхгаорхгяошуоедфууахпадыаххохрфяышгагтххягрпитргяигшпсоудхгпгегхяодрядяуияуыггротеыфопфяоаатахтодефдгухпрсшырхрпырыфоииеояпыахдпдттфгихеяфрпояраытыгхоиеодпуаогадтгггпяряфриеррряыыхипирпфпошшсгефахгаятягаоеетдтусяуасуфгпоаесфыуфяхахытшуперрфтихшусоыохпдпрсфдифшхсхуяяшстипгтоуеуддуояпааусуаофехдхишшшсхыряупыруфаиоеосаысхдпфргфхошешдыуряуаыуугиооеадаудядсштгяхпяршфриршысыыпхисорпфаидшдсгыгяфаяыргеореидыуияиаотпхдоседфшугшпсяышхеаыртфыисшисаыпхапстгффигеыдяуфяеарттгыоуеидсупшяастггфогехфяиешесуытхупутпфоипшсссуихфпгрххеошеедыутяфаутигоопеадсуфяфсятххшпшруфритшысуыахопарафсасшфсгыхяшаштегроыеыдууияосотагсодытфуухшясшаыуеяоифттфпипшддгхспдрффгихеяядаеяыаттыгуоиеодпигтсафыгггохряерфиореясгыпхоадргфгугряддияяяаитуяоеидтуыяуягапыугхрхфяуфягахдиыехсаитиигшусиыорхяхапрххшоиегдгитрфтрсуодеудиуоыгшасеыгггпертгршфсеырхтяааурггаиашгдяудядсыттхетодоурятаыпаесотяходашятсптггхпяиатягпореясстахфасыягяогфшурххаятшршссегоиххдуахтпгаоспррегеиушысхуоптргфыиушиххсгугггаштххтооердушфарттгыпоыфдоуаяасптдгфогехыришшрсрыыхыпоригодпшасдыдяипгрхгяпрыодруыяысттигоопеатгудягагыяхяпррехрхяшысиыихпппттфсаеафсгуяяяаатегтотефдуусефаптагспыефдхухшягяыехрптруфуиишодспяхспфрфгрихеядшоеошаттугуооеофоуашфадтфхшохртфшиешрстыыхупорофдиашфсдифхгпхтшгшорердсуыеуаитогаоаедддиуягдхыяхшпрррфыиыеесиуахппаргфдигшгсхуяшраетргооыррдиуояпсдтсгдпеегфаияшшсеуыхтпырдфииашпсаысхдпфрггеояеидеуыятаытугиопепдфусяфафуягхпярефеипштсыыуяппорпфдисшхсфыгххаятшгеотетдиууяоаотфгаоседдфишяхсшышхедертфыиушосоыпхапдрдффигшхфяушяеарсигсоуеидогпхтошфрхдетштфпишшесрпауаятпатдгеопепдхияапрхгяошпиррдсиияиастфхыпхегфиуфсытххяпшоитрфсоишиссыфхсраитояшфсгыхуияеахторяршдууияохесоушхспоррдеиыердоыояуыдгииишоспадуяядаптигеошрыдиуихиспыыхпопрядхффсутфггохииругууушпдиудяяпсргашеесдыфхгяуаыыыгпоорефспхахтогпоаигрсгшыушфсеыехырыфтиышусиыохпагистхошшгсхуяиоярадыоршршдиуояпшхссырххохррфыиошидяуиеграфииошпяыпыгаыптяфхояешдеурятхеоуярооепдаифтеафтхгхпаршфеирштроыухопорафаифшддфагххаштшгыоретдыиорфаотагапыеддфугяхррышхрпррыфыиошифофыхапдрдфгигефдяоиихартыгыохеидпупяхасыяшеогехфяиашестытхпссрифоипетссыфхфпгуггяошеедтутяыауыпшгопесдсиеяфагтхшяяхрефтитшусууяхоасрафсихшфдуыхяяаштегротеудууаяоастаясодефдхухшшсшытхрстрыфуиошосаыаххпдыффгихешдшурярастыхооиеоддуашуадтфггашряфшиушрдрыыхупитафпиаеясдыгхгпхтяхроеердауышуаитогпоаесддияягсыыяхрперрфтиышисиысхппсрсггифшгдяуяягаетргтпиеудиуаяпсутсгдофегдхияшесеыыхтпуруфсиошпсаысххпфрхфхояыядеурятаутугиооеадаусядафыфгхпяршгоиргисыыухипорпфапхыдтруыххаятшрихросридиусяфшсхсоседдфдяитеясфысхупытпфсисясдфупяфпфттгрпрдяушяеарттеыфауифдуфяаастдутгхпоттасшдсрытхыффпдтдддихеффеууяшатсеохеедрутиашуагыагаогряфдиееедеутяяатихидшысуыитсяоагергаихшхдеяшаотегротодесфсухягсоушдурпдгухшяхадяупяраярсдаифесфяуяягпфгиихеядшаоиошеаоыахяпириффтысутфггохихгттриегрегошдяшууташешсдыфхгяуогсггирдхтшшяааитогпхшодрпфееаахыяхшатупфтиушудшыохппарсыхифшхсхушяшаттрхтфыеудоуошшаатсгдпхутдхишшшсдырхтпыруыаиошасаыдхдпхргхххдешдруряыаытггиагаудаудядсутгхяпярефеиирпсыыухиашрпфсисеягеыгххаятсгеотетдыпыяиаотпгсоседдфоятысяыехеаертфыиурируыпхспсрфффоышхфеушяеауттгпоуеидоупяаастфгфпшехфеишресрытхупурофооышафсыдхфпхрхгшошеыдротяыаутогооаеафуудшхагтххрпшрсфритшыдоыихопфрагоидшфсгишяяаштигрпееыдууишааптахшодредгухшясшыехрпирыфдиишаспыахспдргфгоееядеуешыаттыгиоиегдпуаяссгтфггпшряфриешрстыыхупирпфпидшссфыфяепхтягшоееудтууяуаииигпоаесдфуфягахышхшперрфтоешусиыофгатрсфдифутеофеуухыаоыухсосрпупшшаатсгдгяыффярыадшиоухтиатяфииошпяшдяияхяарышхуоаеыдоргаатугиооусгошоуесухахыпяршфееефеааияртгдгыгеисшдсфсеутядауыехепурписяиаотпгаосадерагссдшышхепроурагуорешсдысяхаштшфшпрехфруряаапффодеидоуптхешсшысяеаетриышесрытыдхиатрфстшассыдхфпгсхеадшыддпутяыауфгяудфрышсеефхсутххяпшоытегоыфетспыпхдтффсидшффяуеяяаштегфотеыдуоияоаптагсодеффшухеесшыехыптрффуиишоспыахспдрфгяихеедшоеяраттыгуоиеофеуаесадтфггохряфшиошрфтыыхупирофпиашдсдуххгпхтегшохердтуышоаитогдоаефддуфягдшыяхшпуррфпиышусиуахппатяфдоошгсхуяяшаетргуоыесдиуаяпсдтсгдпяегфдияшшсеуыхтпырафиидшпсаысягпфрггтояефдеурятситугиогепфшусядафтггхпяртфеипштсиыухипорпфаисшхсфыхххаятшгеоретдуууяиаотпгаоседдфугяхсяышхтпрртфыиуппсоыпхапсрдффигшхгхушяеартыгыоуеидпупяаастдхоогехфяыуерсрытхыгопдтогыоршгсфишярарррхыпшрыдыудясысггопеадссшоршрсфутятррффитшысупгыфяфофтяггпреидеуыпафдидшфсгыхяядшгоишхеодефдгфуиыеыспыояеасруигшоспыатфяшпхтихшптепиуяиаттыгуггопрудхресутфггохиурагтиояисауояфпфтсяяеусдыфхгяясыыыхшпыепдиухшпсдышотесыеишягахыяуохрпдтоофшусиыоясфярсффиферсхуяяшаедугтоуеудоуоясааысрдофехдхипшшсеыряудсруфоиошгсаысхдпфдшфхошешдруряуаыууурооеадаудядсутгшыяфршфриршфсыыихиаерпфгаяшдсфыгяоаятегеоитпдыууяисетпгсоседхдугяхсяыехепрртгиадшиспыпяшпсрдффпгсшдяуеяеатттгооурпдоупяфастфгфогехфяишшестытхопурпфоппшассыфхфпхрхгеоштедрутяуаутогоохеагсудяфахтххшпшрафритшысуыахоппрафсидшфсгыхяшаштыгроыеыфоуияоаатахуодефдгошшясшытхрпорыфуиишоспыахдпдрхфгояеядыуеяраттыгпоиепдпуараадтфггпяряфшиештстыыхупитыфпиашсшдугхгпхтярргипррядгупяосдтгггигтяфдояшясиыургрсфтиышуяапышуопягоиятояусуояшаетррихтпаяхфуусясагаспрегдхияатиштгштухтороиошпсаысхдпфтушхдфесдеурятгдасысфсогрдгшиышясреапяршфеирштрыпприпярхфаисшдяефтутягсыыышдеадыууяигфстыыгупершгшшпсяышхефппфтифсуашфдсияяяагпдотшхдяушиууиииытаддсдпуфяаастдытгхпдрыхишасрытхыгапдттфгоаеадгишсшрхгяошртдуутяыауыргоопеагсудяфагтххяпшрофроушысуыпхопарафсидшфсгыхяяашттгроуеыгууияоаптагсодрыдгохшясшыехрптрыгриироспыахспдрффгопеяфруеяраутыгпоиеодпидясадыяггпшряфшиееыстыыхапитрфпиашсдгыфхгаттягооеердтуыяуаитагпохесдгуфеяахыяхтперуфтиышудпыохппгрсгыифшгсхиеяшаетогтопеудиуошсаатсхеофррдхияшшсеырхтпоруффиошссаысхдпфргфхорешдрурятаытугиооеадаусядафтггхпяршфхирштсысихипорпфаисыдяхпггтаутшгеорупрсдсиышдсдтсоседдфугяхряпгрептргфыиушихгдеудяяохтехяпыеыфрепапттгыоууяпопяитдшяеирпхехфяишутшодтушххпарпгфихшхахишяфсштшгооишяуаяыаутиспаиуодыеештфыырхяпшрерафыоешсепяеппрафсдроересеуышрсотдгиоаеуухяоаптаргсыееошхеыидяеофоппрыфуииууфеедоягыдргуихеядшсууошяааыухупарфусшрадтфгггепхтысаошшусуыпаарофпиаефсхыфхгпхтогшоеергтуыяуаитогпоартддихягахыехшпоррфтиышусиыохппарффдихшгфхуяяшаетргтоыеодиоояпаатсгдофегфсияршсеырхтпыруфиидшпддысхдпхрггдояешдеиыятаытпгипеепдаусшгафтгхрпяруфеирштдиыухипфрпффисшдсфыгххаятргеооетдиуушпаотпгфосрпдфугяхдеышхепиртгяиушисоусхапстшффоышхдяушштарттгсоуеодоупяаастдгфпшехфуишштсрытхыпурифоидшасдыдхфпгрхгяошердрутяыаутигоопеафаудяфагпдхипшрефрфсиаеасгыфяисяшыошшфсгыхтешясшыухохиддуияоаптигфытшшуагяетспыехрптоотыгсуяеисдыдххдргоихеядшаоудшуаарпгдпархдхифхатфггохряфшхеырхтупяяпирофпдшоярясяуршшсутагыоошеуыяуаитогпоархядыешрахыяхшяеаетсфаоосоыгхппарсешхрореффтитартигтоыеургдпиешгпохфофегдхдеиуеесхыфхопитсффифяфдхусяхпхтугыысдфурятаыпприагрысшеапыртсдеасиддфеафшосыыухиххпатигяросфыгххсеиигеотетдуууяиаотпуфосефдфухяхсеышяегрртфуиуеясоыпхаафиеффихшхдшушяеарттуооуеодоуаяаафтдяфяаехфшишшрсрыфхысдстфоиашадтыдхгпгтфгяоытидрутяыахтигпопегхяудяфагыпхяперефраршысуыихпппрафсогырсгуяяясятегроттыттуияпаптсгспрефгяухшястыеххптрыфуиишоспысхспхрфгяихтядшуеятаттугупшеогпуаясафтфгхохрефшпешрстыухупорофгиаефсдыфяшпхттгшоеерфууыяуастохуоаесддихягахыыхшпыррфтиыеосиыоххпатшфдифшгсхуяяшаытргаоыеодиуояпаатдгдпяегфяияерсеырхыпытшфииошпддысхдпхрггиояешдеурятаытигиоаепдсусшяафтггхпяртфеитштсыоыхипорпфсисшдсфыхххаятшгептетдыууыыаотпгаоседдфыгтгыдыыхепррттдфиояедспятпсрдффдыотртстуишысатггподхяупяаастдгфогехфяоышпсрытхыгопдтпггихегфяияаирхгяошоррофоитяпсптпгхпгутишяфагтхтяхуаушдсоуесхыихоппидртадрафшяусяутгфгуотеуфеуияоаппрыпяепдрпфтуршудтупхпаидгояшоспыатшшшастшхропряфяиупдтсгуоиеоффыипыыругруепряфшиешрстыыегфипогшиашссдсяуфшроотхгтотеигсшиаитогпфдпярдфпиишесшуыхипиеигпоыепспуяххоогяифшгсхдиуеяхаоародеудиуоияяхсхырхепдтыофшшсеыряудсруфоиоеасаысхдпфдшфхошешдруряуаыыуриооеадаишядафтгяшдуршфриреысыыухипосдфаидшдсгыгяшаяушыгореыдыуияиагтпшяшседдгугшосяыехепдртфппсшисоыпярпсрфффигтгдяушяеатттгыоурпхгупясасыдгфогеххяопшестытхупурафоосшассыххфафрхгяошеедрутяуаутагоосеагсудяфахтххшпшрффрптшысуыохопарагяидрфсгыхяшаштргрогеыфоуияоадтахподефдгошшясшыухрпдрыфуииеаспыаяяпдтпфгихеяфруеяраатыхроиеодпуаясадыяггпыряфриешрстыыхапирофписшсгдыфхгартягооееидтуыяуаитпгпогесдфуфеяахыяхеперыфтиышудпыохппдрсффифшгсхуяяшаеттгтоиеудоуояфаатсгдофршдхишшшсеоехтпыруфоиошпсаыдхдпфргфхоаешдеурргаатугиооудруфтухшопсхппяршфесаипепапыдяаахтрфгошсгухххаятшртгоптршдхуаяпсфтхгхихтшффошшшсоыиосрффыиушишпдгугяапхтпгиоеесоояоарттгыдспфеффиигшгсххшогехфягоиршддофапфрифоипошеяфяутярафыугреессугяыаутиегхепдрясхиееядыыыярудфиитшысусгыпяупххяидшфсгишруаштргросеыдууияоедтагдодегдгишшядшаехрпырыфаиишоспудршпдргфгоуеядшуеяреитыгиоиепдпудясдддпггпяряфеиешистисоупирпфпоршссфыфяупхттяуоеердтугяуаотогпспесддуфяхахыяхшатупфтиушудшыохппаысхаифшхсхушяшаттрхуоыеудауоядаатсгдофегдхишшшсыырхупыыуфииошасаыдхдаергххояешдруряыаытигиаоепдаудядагтгхопяршфеиршысыыохиппрпгдисшдсгыгяыаятшгеоретдыуияиаптпгсосрядфугяхсяытхептртфыаышисоыпхспсрдффихшхдяушяедтттгыоупаддупяаасифдошгпасыиешесрытеагррафоипшагдодыхыфтргяошеехруофгпшефгоопеадсудтфяыохгппшрефритшырупдропарффсидшфхрохусоуттгротеыхипиехафтагсодыфхупяыдсрыехрптрыфуииыххпшпяшпдрффгптияояпеятешсогдоиеодпсгргтдшдтыуддпфтиешрстоаеудихифаиашссдогграттягшоепреыдгиошаяигдоаесддпгргфхышхыперрфтаушппиттпепдрсфдифыреаафяраетргтсупррсуояпаатсгдяфоеяхуоштсеырхтдууутефошссаысхддгаяпгоуешдеурехетдшрахусршиуфядафтгешдытыфуирштсыоадпяфогсхигшдсфыгршфыагисосетдыууыашисфрехпогегфштасяышхепрртфыссыифхыххапсрдоишягсихфутхдатогыоуеихпухффоссххрогехфяяффгпшагтрояхифоипшассыдхфсаиххтоиеедрутппгушфсуяирхяеудяфагтхшупшррфроушысуыияаппраффидессгыхяясртегроиеыдоуияоапыдгсодршдгиишясшыеяыптрыфсииряспыахсагрффгоыеяфшуеяратыигуоиехдпииясадтфяяохряфпиеегстыыхуапрофпоршсдфыфхгпхыегшоеефдтоуяуаитохсоаесфиуфеаахыяхшперрфтифшудеыохспатффдифеисхиеяшаетрхуоыеуфшуошгаатсгдпхегдхисшшспырхтпытофииоеысаиухдпфргхшояешдхурееаытугипаепдаипядддтггхпятрфеирерсыуяхипорпфаисшддпыгягаятргепыетдыиряисстпгаосргдфугшфсяусхепрртгииушидиыпшыпсрдффпяшхдяишяеаиттгыоурпдоупшсасургфогехгеишшедыытхспурифоипшассусхфсярхгеошртдрутшыаууегоопеаффудяфсхтхяппшрефроушысуупхоатрафсидехсгыхшраштигротеыдууияосптахгодехдгошшясшурхраарыфуииеаспыаяфпдыофгихеяфруеярситыгиоиеодпидясадушггадряфшиееыстыыяспитдфпиашссдыфхгсштяхуоееыдтиияуаиысгпофесддуфеяахыяяыпетгфтиышудпыохпахрсгыифшгсхиеяшаеыпгтпшеудиуошсаатсярофтгдхияшшсеырхтапруггиошссаысхдпфрхфхптешдруршуфстугпоородаусядафаггхпрршфрирштсыыушппорсфаифшддшыгярдытшгеорыодыуияиагсргапшедяшугшясяышхепиыпфыиушигдыпхспсрдыхигетдяушяеарттгссшеидаупрсастфгфпяехфтпушесрытеупурофоиптпссыдхфпхрхгяошердрутяыауыегоопеахеифяфагтхтехуаерхффиошидсыфхфофтхгсохшхдууысытогротеыясффуфшисгыгяяефдгухшясшыегрфрхтфгиишоспссияшяадтдгоогесахяааттыгуггофрффшияшадряепрряфшиеиашыдеыспордфпиашсррсгуишрфпгсоеердтадусшспстгхдашрыфяирееыахшперршафгоошдасыгядсштшгхусдиуяяшаепрыугуопрсфшудяхпагдарегдхияергоырхыпырсфииошпсафгхдпгрггяояердеирытаытигиодепдаусшггртгхяпяруфеирштсыфпхиппрпфсисшгсфигисаятегеотетдпууефротпгсосрыдфухяхссышхусортфыиуеясоыахапсусффигшхдшушяеарыушсоуеодоухяаастдяффтехфшишшрсрыдхыаорифоидшасдыдхфпгрхгяошердруияыаотияоопеаддудягагышхясшрефриышысиыияеппыафсидшгсгуяяяаатехыотеыдпуиясаптагсодефдгияшястыехтпттифуиишпспушхспдрффгихеядеуеятаттугуосеодпуаясахтфгхохряяяиешрстыухупирофаиашссдыфяфпхтягшиаеодтуыяугпсиыохфпходуфягахыяхшшеиаштртеясиыохпгяаттггеишетфеиияисыреоыеудиуояпааыхедашрудхияшшяыдеуоффатрпфпидшдысухашргфхояпоерддиохетагиооепршфяипеяуехппяршфесаипепапыдяаахтрфгошряутххаятшеихпопррфаиагеыягаоседртфроршисууяяптофпиушисодяысяоашхшохшхдяушытяостышгхоаепффухяхпхушхфашршфоииасыгхыпуриесссетпфясиудаыафттддгдпутяыауаыгхидссяпаиепагтххяаруофриышыдшыихоппраыгидшгсгуяяяартехрфтеыдиуишяаптагспгурдгияшясдыехрптрыыпиишпспысхспгрфхгхсеядеуеятаттфгуафаыдпусяссытфгхохруфшиуростыыхуаярофаиашхгшыфхгпхтагшорердтптяуаитогаоаесддихттахышхшпгррфтиырурыыохапардфдоушгфшуяяшаытрхшоыеудиуояпаатдгдпяегфшияршсеырхыпырифиоешпфаысхдпгрггяояеедеорятаытигиопепдфусшгафтгхепяруфеирштдиыухипдрпгоисшдсфияххаятугепеетдыуушпаотпхяосегдфугяхсяышхепуртфсиушпсоыпхапсрфффошшхдшушштарттгуоуегдоупяасфтдгфпяехфтишшесрытхыпурофоисшасдыдяшпгрхгяошеыдруыяыауиугоопеаддудяфагыяхяпшрефроешысуыихяашрафсидудшрстшифыусхшоаирдууияоаптагссауфофиушясшыеыахпапрффдоуехшпяшпдрффгиштиершсшшегрфхяоиеодпсшияеяаяыряшаурафыиораушхупиротггаоеегсгуеятсятухуоорыууяфаитогпфхпсррфхухшрсыргпгррфтиыыхеыдгуояыаяехгепярыдыиряеытгтоыеушпдфипшусттхггаертфтутеудеуухупфрдшшеесаысхдгрсртфгрпыесфеиешоспгсооепдагеуфшудехяпоршфеируиетдархяупсрсфгдасфгтяраятшгегаоыредсераотпгапфуедфухяхсрышхепрртыоиушосоыахапфрдгфдгшхдшушяоарттгыпоыфдоуаяаагтдгфогехыришшрсрыыхыпорихохышасдыдхгпгтыгяаипхдруыяыахтигпопридсияреагтххяпарефтитшпфсыихоппттфсифшфсгогяяаштегтотеыдуипргаптсгспаефдгухряехыехтптруфуидшодсыахспхрфгиихеядшуеяраттугуоаеодсуаесадтфгхохршфшидшрфтыыхупорофаиаеесдифхгпхтшгшорерддуышоаитогдоариддуфягдшыяхшпуррфыиышусиуахппатяфдошшгсхуяшраетргаоыеодиуояпаатсгдпяегфыияшрсеырхтпырифиисшпссысягпфрггяояеддеурятситугиоаепддусядафтггхпярефеиыштсуыухспорпфаисшхсфыхххаяиягеоретдуууяиаотадхоседдфаошысяышхеодгееяшххттурххапсрдффигшхяхашиыапттгыоугыушдуепгшспггпеехфяишыгдышаыыяпушфоипшахгуадряхтхпххыгиыгддяпыиаргфяерхсдшаиясаяоыытдфприитиофяягоихрреогфаееыдсестшыыхархроыдууияоаппихшодефдгяояшуитагаасыффуиишоспыахсфрифшооыеядшуеппыфдиопрприхяусясадтфшхтгруфшиешряисхытхшпрепрпеисдыфхггеууфирспрхсупашшхоигутяыефтуфягахаруяяуистефииишаяыхппарсфдифшгдиаяпсаетргтоыеудиахтпаеысгдофегяходфтшотиасгсрхиидряфшшошгорпоогшояешдеурятеыооеифырддаусядгфупсяхрешоидшдттяаугыртиоспсдеспшгшехыхтигеоретшоадшфпуштоуриредфугяхрахддтшгртшфосшисоыпхапсрдшосгдсдаушяеаротргдрттисетфрыуфуутушехфяишшесрытяыфухугтипшасспдршпшгфххпеяуутддруппггрыогеадсудтгсгешуосрхшфпитшысупгпгришгяихыяедшыхяяашоитагсоудууияоаптагссфуфегиышясшыетухрифяхауршуыуяхспдрфгуаяофаяшушпрфтсгуоиеохеуфпдуеуаыпгхррфшиешргыоыыоыутяфпиашсяядхуфяхатыяхппшпуусяуаитордфетыдятястошыухшперрдургсодяпсфхртрсфдифшгсхаяыргешугтоыеудиуояпгяосгфпяегдхиятргидяаяпсруфииошдртауодоиитуыоуешдеурыифиртппярушшиишядафтгуфептхтырготооыухипорпфаисргхфиеясаятшгедрисхгифсеуоххояяспошгпупысуышхеприсешпгагдтпихепхрдффигуфешдгуиффтагыоуеифогяхоиыатыпфсрыфяишшеерпаяеыгтысифпеуссыдхффгуадшштшфпиееигифхаитддгпфшудяфагаерпафепаашхоодеыихоппоятагоошерфшытшяпыттхаоаыхудяоаптаеффоиехыпирисиыехрптепетрыаштшогрыатрффгихирдишштфпсфферуоепдхуаясадсыпфтуигараяирсдыыхупиопеиахтшфыуегшиидугиоеердтрфрихфсеыефеедгруфягахпяеыоыгшеоатхдуосошдигпаесашшшшгсертпяхтттасяаитуояпаатсгдофишяхшдшисеырхттиххурфгагрояохдпфргфхояешдеуриисотугиооидшфстрффоуихаоддоадрииорггиитхсопеусиштдиыгххаяафышгтоорофаипшшсиыштаехдфугяхгыошыфефртфыиушисоыпеяфсфыхеигшхдядыусшуаиытхоосхуфяишфасрргфриияегуудесапуяхутпфоипшахсигддшутссохпяроыхутяотгяффыофяяфутяыахтххяпшуиеяоошысуыирояааитядтояшяупрсхиодршдсуессоптугдиоерыгррдгухшяяыдшыахсашрсухшгспыахсоясреишшуафяиуяпаттыгутреохшопшесттыхтохряфшштяягуасефгхфшфхиашссдфяясфруусаоятадоуыяуаиипфяресаедиоягахыяршхдпеетогыохрршгфаурфшуоршгсхуяфушугехсддхгушуояпаатсгдяфихяхаашисеырхтсшриепроысоаефяепфргфхфротшеаотрфетихшооепдадаусеясрыеяыаррифооышыыдхипорппхусдерирфгуеуттгеоретхапуриыттхгаоседшгосеырыытхиосрсфыиушияиатшепыядпряуррдуушяеарутаххродяхгшифсштдгфогоешяисггууфеяапурифоипшассаирфыфтыгяошеехфииааипаошшгпрддсудяфяшыпаигирпихдпшеяыаягефатисияшрспяфорааитегротяодтпыагхаапотпеефдгухархдяееагпхугаисшоспыаесааеафддфеядшуеяраттырудиеадпуаясадтфггддиягыиошрстыыиасрсошгдисгшдурхгпхтягыурептеигпусстггпоаесшхдттуфяыхгешорффтиышухидпууххтгягфпиишпсохпаотргтоыуушышыиишаияирофегдхияшшсеорртгетсфииошпхасерыстшгсфродирадштуоырпфеуыпыргггиуггипхяптршфеиртыасяпаишгрхфаисшдуяыдутхяяраотееадыууяигсашттдсуфятсдяхсяышхепрстшгсусясгыпхапсоххптяохгресооауттгыоуыохоппшгсштдгфогтрпшхахдытряаепурифоипшассоарфдурхгяошеедрутыпгуедггопеадссогиреуыпддахефритшысуыисогсиадяофшфсгыхырхыофшисртрфиуааиодшоыаягфытхгрошыфыохрптрыудгфдппыхыфтфутыфгихеяятспрфдытяфеушфхдшияясадтфасоясифяоыфшяшыахупиротпгдотеафшфяаытягшоеесшфааыхитсоыдпяесддуфипгхсогхыпотгпиышусиыохппаифшддаетсхуяяшхыагттгеоышдаеяхаатсгдсетиаауфсхыутдхтпыруфииошпгепсорпфргфхояештеаиттяытогиооепхспсяыафтггхпяршыедыыттгыахипорпеыдпуфгигтяуаятшгедспорпфутгяфсфхгпшеддфуггсырптуирыеффуиошисоыпесхфутффигшхдяушяехпотхподеидоупфретруеоудотшгишшесрытхышуодшосреяссыдхфафгтиииыафштетяыаутигоопеагхадуфсетххяпшуеаххфооагыфхоппраясипршехтшыуоутогротеыоатгфяшфхргтеуефдгухшясшыетшфтаогриишосппауехыотдпосрафрурхупыеосгудрпдпуаясгдоигфтхпдшгидггттагшуродхыыдтшпофыгятпхтягшфыуофоыядфргыдгхоаесддуогеяеафеуаууффоиышусиатыыхапдеаифшгсхуяяшееоретыиеддиуояпитасяегпшшдфасшшсеырхтпырухисодыдуысхдпфсуеехтояехадтдшшсеруфрпгпфусядафтггхпяупшепашгсыыухифоухфшехтрдпыысышеифхуопетдыууосуагдхашфхяшаитяхсяышхдххдсеупотаспыахапсрдрдыяешдяушяефоахшходеидоуптрсфгидыеапргторшесрытрыгууефарффотиихршдытадыршуфшусдеиадтоггопеадсипстытофпшыдеафиитшысусгыпяупхрсодшфсгыхтяяфаырпсоудхдаяеодтыгсеиирпдяушыфдеыехрптоохгуадоропдятусидрыпыасррсуеоорхфгиофеодпуаугхдисафутаедпотшрстыытпсешшуедышдиифшфыошфтффыпферооегитштшгпоаесддуфогяыпяпфптррфтиытогдыяяппарсфдсфиехеугаятхгсишггугхаиахфепсхорыхртдхияшшптасяфыиатригсшхсаысхдфхсрырхтпяряхдяааытугигпеешдсагусдртгхпяршфеирштхыпудпфхрпфаисоршепыштпагтыдфхаышисягаауесспрядярядутисдтддятхфшыадгыагреяфоуигоефгрияхуипхшиехтоеяытсддотяуосшуысеуатеауиерахрыиррысыршдыятдырддитхпрыафпыпсдутяыаутигоопифясддшрагтххягтыхсишиидфыигхфппрафссгодяфаотфаеыпгротеыяподхдыхсушфоапрышыигиуадяррпухытусрддттаыяяуииигтихеядшаоссяфгяфегаиыдхуаясадаяепоххфияфирасуыыхупиуптуеуешсдыфхгхсеыоагирепсаяяуаитогпоаесяаафпыахыяхшперрштддыуиуыгхппарсрстдииуыргфуоотргтоыеудиаоыхгаяахеофегдхсршгыгошеошиегффиошпсаисояшяыитдфсшпдоурятаырфшудахягясфхшсытггхпяитятурдушдопхртдтфгяисшдсфупдупигяииишпидсууяиаофгхпусырфпсуяосяышхепрртфыдрыиышупхапсрдегстеупаяфооагтегяыриашяахшиосядтгогехфяишшесрогрыогрффоипшасфтоудшфтпуояиеудрутяыфауухидыиифоудяфагохуяхдптгестудяяаортфтиешфхяшфсгыхяяашяеридтяадауияоаппутугтуодхиышясшыегууыууысытдшшаыахспдрффгххитяшахяпаттыгуатдехушфситсфрххохряфшдыесоифырыопгшрорпгереросдеыиддфехотдтуыяуаитогпстусуыишягахыяееаирихутиеясиыохпфапоешаугшофттдгыдгифдпреудиуотпяапушгыдяддоттфуишааыошяпфххиошпсаысхдпфияшхедеидеурятоояехгпиифдтихшрафтггхгрпурыгиифетдтхяпорпфаисшдсфаерхрпыегеоретшоояфгегпягутяпппдтиппашеспхгиытаеугшдсоыпхагпырасхфуясоутяеарттрпгиопеоухяаастдирфеаегдуфедиеыахыпуриесптфаеоисдеияуогяошеешшитсуяихеуесхяытиптдгяхутахпашхияаааашсосдаяетиоыоушяуяашгрфатеаихпехоядусушхоыдпеыррдгухшяятоеффтяаоятосшсспыахсдфуфтпспеудшуеярддиыеиыууяягудясадтфггохияешсефесаыыхупифауготоаяпдаххастягшоеуряеудфеггогштиугдтустеяысыохшперреиаршыипгхыпдиртфгифшгсхуяяшеепаетршеддиуояпгттгшаиедтаяаашисеырхтфотфорфяшхуыдгяепфргфхходаядшддяаурхгиооепдаусядгшогдшпрршфеируешадффдпгрпфаисяшгдаридпстоидоретдыууяиеопоеааеегдфугшшхшышхепррыфыиушидаашхапсрдефигшхдяушяеарттгыоуеидоупяаастдггогехфяишшедыытхыпириудипшассугхфпгтягяшаеедрутесаутигпопррдсуфяфгхтххтсурефритшгсуыохопфыхфсидшфдоыхяшаштешеотеыдууояоаптагфдфефдхухшусшыехрауыыфуиошодуыахспдтхфгихешдшаяяраттыхооиеодсуаападтфггахряфшитшрсуыыиупитафпиашхсдуахгпхтяхроеердпуысяаитогппдесддирягдпыяхшпетыфтиышфсиясхппарсфдифшгдруяяоаетыгтоыеудиуаяпагтсгдофегдхияшесеырхтпируфииошпссысхфпфтяфхаяешдеуыятаутудаооепдаусшяафтггхпершгтирштсаыуятпорпфаофшдсфутххтгтшгеоррудыууягаоашгаоседфхугяхсоышфипрртфыиушисоыгхааррдфхигехдяушяуаришгыосеифаупяасятдхаогехфяоршесрыахыаерифоипедссыдятпгоогяошеефыутяыагтигаопеадсудяфагытхяппрефыитеысуыихдппудфсошшфсгыхяяартегиотеидуоияоаптфгсогефашухеесшыехопттефуиишодсыахсаерфугихеядшитяраттдгургеодпуашфадтфхуохтифшиешрстыыхупдрогшиашфсдыфхгпхтргшоиердууыеуаитогфоаефддтяягдшыяхшпорргшиышусиуахппатефдыпшгсхуяшраетргдоыяыдиуояпсдтсгдпуегеуияшшсеырхтпырдфиошшпсдысхдпфрггрояеидеуыятдытугиофепддусфхафуягхпярофеояштсыыуяппорпгеисгисфыгххсетшгеодетпрууяиаоысгаосрудфиуяхсяышхепрртфдиуешсоысхапсрдффоршхдиушятарутгыоуефдоусяаигтдххогехфоишшхсрытхыаорифооешахяыдхфпгышгяошеддрфгяыаутихаопеафуудгсагтххяпшрефридшыдшыихаппрафсидерсгуияяартеяротеыдфуияаапшфгспгефдгиошясгыехрпттифуииееспыгхспдрфхяихеяддуесхаттыгуппеодпиуясрштфггохряфшиешдстушхуппрофпиашсдрыфяипхтегшаеердтуфяуастосооарфддуфшоахыфхшперргуиышудеыосспарсфдохшгсхудяшаптргтоыродиуошуаауегдофегдхияшшсдыряшпырофииошпсаурхдаирггшоятшдеуряфаытсгиыиепфдусядсотгхдпяршфеоыштсыуехихарпфаисегсфыгядаяухгеоретфиууяисутпхооседдфугяхсяыдхеашртфииушисоыпярпстиффояшхгяушяеафттгсоухудоисяаасыогфпсехфяишетсрытяепуштфоипшадфыдхфадрхррошеедриуодауыугогяеадсудяфагтххдпштшфриушысуыихоаррагиидшхсгихяяаштфгросеыпыуишааптахоодрадгухшядрыехраерыпаиишоспудхспдтдфгттеядшуешыаттыхуоихшдпуаясадтфггпдрягшиешыстыыхупитрфпоишссгыфшгшатягфоееудтртяуспдягппоесфпуфягахуехшпетефтясшусиыояспарсгдифыесхуяяшсттргтпуеудпуояпаатсгдофрддхошшшстырхтпаругриоеисаыфхдсфргфхофешдыурфраыыогиоородаиоядафтгяшпяршгеиррхсыыухиаарпфаодшдтхыгххаяыргеоррудыдтяиаотпгаоседфдугешсяырхепррпфыоршидиыпхдпсыдффигефдяутяеиеттхиоуеифоупшиастдгфаяехфяоешехгытхыпутпфоипедссатхфпгрххеошеефуутодаутигоопеадсидяфдштххепшрехуитерсууихопсрахсидшфдфыхядашоигрпуеыдуиояосутагсодрхдгухеесшуохрптрыгоиишоддыашгпдрффгпшеядшиуярсптыгуоиеодпуашдадушггпшряфшиешрдуыыхупирофподшссдияхгадтягшоерыдтуышааишхгпоаесфгсгягдтыяапперрфтоиуисиугхппдрсфдифшгтоуяштаеыпгтоиеудпапяпсгтсярофегдхияртсеуехтапруфпиорпсаысядпфтафхдыешфтурятситухтооепдаифядафушгхшдршфеиреусыыуяспошефаисшддхыгххсытшасоретдыууяиаоысгааяеддхугяхсяышяыпрртфыиушидаыпхаахрдгаигшхдяиряеарыпгыруеидоупшдхдтдярогиуфяишшедыаыхыафритшипшассыдоупгыргяпоеедыутяигитихфоптрдсудяфагиехяашрегоитшисуиихопптсфсоошфярыхшеаштехуотредууияосстагсаяефирухшясшутхрпттафуфшшоспыаяфпдрфхтихдпдшуеяраттыгупаеофхуаяфадтфггохттфшиешрстыыяопироггиаеосдыфхгсштягшпоеррфуыяуаиыараоатеддддягахыяяргррргдиыетсиыохппадтфдпешгфиуяяраетыеыоырддиишяпаатсгдгшеггяияеисеыыхтаируфиоашпхуысхдпфыгфхояртдеияятгатухпооепфхусшпафтггхаершфеопштдфыухипотсфаисррсффхххаятшхторетффууутаотпгаоседдфоряхдоышхтпрртфыиуефсоыпхапсрдгхигшхфиушяхарттгыпоиодоошяаяштдгфогтшешишессрдохыпуригадашафыыдядпгрхгяошасдрисяыдятигаопрятхудеыагушхяперефтитшыдыыихопптдфсидшфсгутяясттехсотеидуоияоапыггсппефгхухеесшыеяппттефуиишодсыахссррфшыихеядшитяратыфгуясеодпуашфадтфяиохыыфшиешрстыыхуафрохеиашфсдыфетпхыигшптердтуышоаитояшоарыддуфягдшыяхшасрршииышусиуахппаыыфдхашгсхуяшраетрххоыдадиуояпсдтсгдапеграияшшсеуыхтпыырфидашпсаысягпфргхфояегдеурятситугиаиепптусядафуягхпяышфетиштсыыуяппорпхсиссшсфыгххаятшгеашетгуууяпаоысгаостсдфяояхсяышятпрртхыиугхсоыпхаафрдффпхшхххушяеарыугыоутпдоиуяаастдххогеххришиосрытхыаорифопфшаеиыдхфпгышгяоштидрууяыаутигоопеагфудреагышхяаррефрпишыуиыихопптдфсидтшсгоыяяаштехыотеыгсуишыаптагспгефдгпышярпыехрпттифуиирхспядхспдрфхяихеягпуедуаттыгуоиеодпохясфттфхяохтефшиерпстуехупирогсиашсгрыфсхпхтягшптердтофяутттогпоарфддуфриахстхшперрфтиышуффыоеепарффдохшгсхоияшеттргтоыродиуоршааыогдофеггшияшшфсырргпыруфиоашпсаоыхдиоргфхояррдеурехаыпргиооепдаусядфытгшапяррфеоыштсыиххисорпфаисегсфыгепаятггеоретфиууяифртптуоседдфояяхсяифхетортфыиуепсоыпеипсдфффигшхдяушяедфттшеоуепдоупяаасургфсоехфшишетятытяфпурффоипшадффтхфсирхгфошеедриуяыауушготреадсудшхагтхяспшссфритшыдоыихосырадяидшфсгыхяяашысграяеыдоуиягефтаяыодтыдгияшясеыехраррыфуииеаспыахспдпшфгпреяфсуеяыатыигуоирфдпияясадтфягохрягииеешстпахуапрофппешсдпыфхгпхыегшоерддтпыяуаитохсоаесгууфрыахыяхшатррфтпяшуфсыохппарсфдифрусхисяшаттргтоыеугяуояпаатсгдпхегдхоашшсхырхтпытоеоиортсауухдпфргхшфшешфгурефаытугипаиадаоояддттггхпяршысирегсыирхипарпгяххшдфоыгяиаятегеотетдыиыяиаотпххоседдфугпосяуихеагртфииуриррыпшшпстаффпхшхфесеяесдттяяоуеидоупыуасуугфпуехфяишетсрытшяпуттфоипшадфыдхфсархдяошеедриуяыауутгоетеадсудшхагтхягпшфыфритшысуыихострахпидшхсгишяяашыггрпшеыдууишааптаяоодтудгухшядрыехрсерытыиишоспудхспдыдфггфеядшуеяраттыяеоитидпудяссгтфггадряфгиешрстуихупиыуфпеишссдыфшяпхтяяяоеухдтуыяусптогпааесхууфягахыяхшпеыяфтпышуспыояспарсхаифессхуяяшсттргтатеутууояпааыфгдофтгдхишшшсеыряупырухоиогусаысхдпфргфхпгешгруряуаыыогиоотодаиоядафтгяшпяршхеируосыыухиаарпфапдшдясыгххаяыргеортудыаяяиаотпгаоседгдугршсяырхеаыртфыпушидыыпхапстгффигтядярряеарттхиоуеигауптяастдгфаяехфяптшеерытхыпурифоипрассиххфаярххеошеегтутшеаутигопсеадсогяфгштххяпшттфритросуыахоппрагфидшфгеыхгеаштегротеыдуоояодфтагфодрхдгухресшыххрптрыгоиишофдыаурпдрффгпшеядшоуярястыгуоирадпуаряаддоггохряфшиешрфуыышспирафпиашссдиихгдштягеоерышыуыешаитггпоаесфггыягдсыяхгперрфтоишусииыхпяфрсфдифрясхуяшхаегтгтоыеуфпуояпдптсасофегдхияшшсеуххтструфпиошхргысшппфтхфхошешдрурятсттугиооргдаусядафишгхаиршгхиршусыиухипоышфаопшдяеыгшшаятшхдорршдыууяисатпгаауедппугяхсяурхепрыяфыагшисоыпядпсрдхаигяшдяушяеарттгыаяеигыупядастдгфогтафяишшесрытяипурихтипеиссыдхфсярхгяпгееышутяыауыпрпоптодсхуяфагтхяегерехеитпшсуыихоппдрфспошфффыхяеашттетоттедуифяоаптагспшефгуухефсшытхрстрыфупяшодтыааепдтхфгихрсдшухяраттыхооиеогыуадпадтфггашряфшохшритыыхупитафпиарпсдудхгпхтягшоеерфхуыетаитагподудддопягспыяхшперрфтиыехсиитхппсрсхдифшгфоуяяхаеоогтпиеудиоряпситсгдофтядхияефсеепхтпыругпиошпфиыстепфргфхпеешдеошятыптугиооепдаусеиафудгхпершфехгштфшыухипорпфаофптсфисххафтшгеоррудыууеыаоуугаоседфхугяхдхыштипрртфыоошисоипхаяордффигшхдяушшхарутгыооеидаааяадптдхоогехфяишшисруфхыстрифаипрассыдшипгтпгяеоеефыутяыдетихыопеадсигяфагудхяуерефритеисуыишуппфефсидшффяыхяядятеушотеыдууияоапуугсасеффяухшехеыешяптрпфуиишоспыахссурфхсихешдшоеяратыхгупшеоияуашфадтфяаохрффшиешрдуыыхустроашиашссдуххгпхыггшагердтуышоаитояооафуддуфягахыяхшагррхриышосиыарапаыофдпшшгсхуяяшаетрхгоытрдиупяпдатсгдаиегфпиясосеуыхтпыыефиоышпсаысягпфргхдояыгдеурятситугиауепипусядафуягхпяыяфеохштсыыухипорпхуисрссфуяххаеоегеаяетдыууяиаотпгаостудфосяхсшышшепрртгхиуешсояяхаафрдффпашхдфушяеарыугыоуттдодеяаастдххогехггишопсрытхыаорифопошаыгыдхфпгрхгяошргдроряыаотигадаеагоудеяагтххяпшрефрогшыфрыихпппыафсидрисгупяятотехыотеыгеуишыаптагспгефдгодшяышыехрпттифуиируспрсхспдрфхяихеягяуеогаттыгуоиеодпоуясдстфхяохрешеиерястыихупирофпиашсфуыфшспхтшгшаеердтихяусштопяоарфддуфеаахыфхшперргуиышуфтыоуапарсфдохшгсхигяшхфтргтоыродиуоеоааахгдофегдхияшшдгыршрпырофииаыасаиохдафргфхояешдеуршгаыургиопепгаусяддитгхппяфофеоыштсыиехиаырпфаисегсфыгшдаягргеоретфиууяидутптфоседдфояяхсяияхесиртфыиушисоыпшупсысффояшхдеаеяедяттгаоуеидоупяаасуугфасехфшишресрытяхпутяфосгшадфыдхфсархгфошеедриуяыауутгодфеадсудшхагтхягпшорфритшыдоыихосорагпидшфсгыхяяашыгграреыдоуияорттаяоодефдгухшядрдахрсерыгриишоспудхспдыдфгытеядшуешыаттыяуоидгдпуаяссгтфггсяряптиешрстыыхупиыуфппсшссгыфяягятяяяоеродтуыяуаиусгпатесгсуфшяахияхшпетгфтигшухдыояспарсхпифессхуяяшсттргтареуфпуояпааыфгдофтфдхшошшсеыряупырухииодхсаысхдпфргфхпфешгеуряуаытугиоотидаусядафтгяшпяршхширешсыыухиаарпфапсшдшгыгххаяырррортыдыхфяиаотпхдфдедгхугшисяышхепрсффыпышифаыпхдпсргшгигрхдяисяеарттгыапеигрупеаастггфагехфяофшесдытрапутпфоипроссупхфпгрххеошеегеуттиаутигопсеадсодяфягтххяпшттфритрусушфхоппрафсидшффдыхешашттгротеыдуоуяоаптагсодрхдгухрясшыххрптрыгоиишофаыаедпдрффгпшишдшотярафтыгуоирашауаегадыгггохряфшхсшрфтыышппирафпидыдсдигхгастягшоеергиуыееаиупгподесгдуфягддыяхапеиофтоишусииихпаирсфдифрясхуяешаефхгтоыеуфпуояпдстсыгофегдхоешшсеиыхтяфруфииошпсаысшспфуяфхоеешдеурятдытугиооепдаифядафухгхпфршфеиреусыыушппоушфаисшддхахххдртшишоретдыиоыоаоуфгашуеддфугяхрпышшрпрыофыиошисапахасфрдгтигшхдяушеыарушгыаоеидаупеаастдясогрифясушедыытхысуригыипшассугхфпгуягяпшеедрутшиаутияаоптодсудяфдятххястреыуитшысуыихоппыафспхшфдяыхяяаштеятотеыдууияосстагсагеффсухшясшутхрптыофуоашоспыаяфгфрфяеихысдшуеярсупугуадеоппуаясадтфииохыефшпишрсуыыхофорохдиашгсдыфхгпхургшаяергиуыяоаиуогпоатаддиыягхтыяярперрхыиыерсиыохпадрсфдпхшгтдуяяшаеыыгтоытпдитдяпаатсхгофегхриядгсеырхтпыруфиппшпфгысхгпфргфхоятрдеурятаытухпооепгфусшпафтггхаершфепиштшхыухипотсесистшсффтххаятшхтфтетгсуудфаотпгаоссыдфпшяхфуышхтпррушуиурссоуухапсрдффашшхфхушеуартугыауеидоопяасртдреогтшфяишртсрушхыпуригаипшафгыдуепгрхгяпреедроояыуштигоопрддсудреагафхяпшрефритшыфоыишфппрдфсидшфсгоеяяаштегротридууиедапыигсодефгяухшяфуыепхптрыфуопупспояхсыырффгихрешеуееаатшхгуоиеодпхрясфятфшыохрефшитытстиахусерофпиашсфхыфшгпхуыгшотергтуыяудотохшоаияддихягахирхшпхррфтиыеосиыошфпаитфдифшгфшуяяшдитршроыеудииаяпааишгдгаегдхияшшсеыршипыыдфииашпсаысхддшргфхояешдеиыятаыусгипыепдаусшгафтгшыпяояфеирштдиаихисхрпуяисшдсфияыяаяупгедретдыууяирштпяхосытдфияяхсепехеспртгтиушисоыпшфпсыфффатшхдеушееарттяиоуехдоагяасфтдгфсеехффишшесруухыпуыдфошошассыдяхпгрхяуоштшдрутяысотигосяеаыгудяфагтххяпшыуфрпсшысоыихоппраяяидшфсгыхяясртеграаеыфруияоапыдгсодытдгпшшясшыеяыгырыхгиифхспыахсагогфгаоеяхсуеяраттыухоитгдппрясагтфхяфяряхоиеешстыыхупиушфппдшсгрыфяяпхыегшоетудтфаяуаитохсоаесхяуфшсахыяхшатррфтпашусдыохппатффдифттсхитяшаетрхуоыеуггуоогаатсгдофегдхптшшфпырхупыруфииордсаыфхдпгргфхояешдеуряыаытугиоо");local M=(17005/0xb3)local o=42 local l=d;local e={}e={[(105-0x68)]=function()local r,n,e,d=A(Y,l,l+g);l=l+j;o=(o+(M*j))%k;return(((d+o-(M)+a*(j*S))%a)*((S*J)^S))+(((e+o-(M*S)+a*(S^g))%k)*(a*k))+(((n+o-(M*g)+J)%k)*a)+((r+o-(M*j)+J)%k);end,[(-72+0x4a)]=function(e,e,e)local e=A(Y,l,l);l=l+C;o=(o+(M))%k;return((e+o-(M)+J)%a);end,[(180/0x3c)]=function()local d,e=A(Y,l,l+S);o=(o+(M*S))%k;l=l+S;return(((e+o-(M)+a*(S*j))%a)*k)+((d+o-(M*S)+k*(S^g))%a);end,[(-0x15+25)]=function(o,e,l)if l then local e=(o/S^(e-d))%S^((l-C)-(e-d)+C);return e-e%d;else local e=S^(e-C);return(o%(e+e)>=e)and d or m;end;end,[(855/0xab)]=function()local l=e[(76/(0xf5-169))]();local n=e[(-0x37+56)]();local r=d;local o=(e[((9794/0x76)-79)](n,C,L+j)*(S^(L*S)))+l;local l=e[(0x66+-98)](n,21,31);local e=((-d)^e[(46-0x2a)](n,32));if(l==m)then if(o==y)then return e*m;else l=C;r=y;end;elseif(l==(a*(S^g))-C)then return(o==m)and(e*(C/y))or(e*(m/y));end;return H(e,l-((k*(j))-d))*(r+(o/(S^z)));end,[(-0x45+75)]=function(n,r,r)local r;if(not n)then n=e[(38+-0x25)]();if(n==m)then return'';end;end;r=K(Y,l,l+n-d);l=l+n;local e=''for l=C,#r do e=V(e,G((A(K(r,l,l))+o)%k))o=(o+M)%a end return e;end}local function H(...)return{...},W('#',...)end local function K()local x={};local r={};local l={};local n={x,r,nil,l};local o={}local c=(0x9c-102)local a={[(-70+0x49)]=(function(l)return not(#l==e[(0x4c-74)]())end),[(0x1a-24)]=(function(l)return e[(0xaf/35)]()end),[(0x1c-27)]=(function(l)return e[(78-0x48)]()end),[(0/0x45)]=(function(l)local d=e[(114-0x6c)]()local e=''local l=1 for o=1,#d do l=(l+c)%k e=V(e,G((A(d:sub(o,o))+l)%a))end return e end)};for e=C,e[(0x1a-25)]()do r[e-C]=K();end;local l=e[(-45+0x2e)]()for l=1,l do local e=e[(-19+0x15)]();local d;local e=a[e%((2838-0x5be)/0x48)];o[l]=e and e({});end;for n=1,e[(0x7d-124)]()do local l=e[(-58+0x3c)]();if(e[(94-0x5a)](l,d,C)==y)then local r=e[((-59-0xa)+73)](l,S,g);local a=e[(0x5b+-87)](l,j,S+j);local l={e[((15142/0x86)-110)](),e[(624/0xd0)](),nil,nil};local c={[((203-0x8a)+-0x41)]=function()l[_]=e[(0x37-(0x7c+-72))]();l[B]=e[(0x264/204)]();end,[(0x4f+-78)]=function()l[O]=e[(188/0xbc)]();end,[(100-0x62)]=function()l[O]=e[(28/0x1c)]()-(S^L)end,[(0x81/43)]=function()l[f]=e[(0x4b+-74)]()-(S^L)l[t]=e[(360/0x78)]();end};c[r]();if(e[(-123+0x7f)](a,C,d)==C)then l[w]=o[l[b]]end if(e[(106+-0x66)](a,S,S)==d)then l[i]=o[l[i]]end if(e[(0x70-108)](a,g,g)==C)then l[P]=o[l[B]]end x[n]=l;end end;n[3]=e[(-0x16+24)]();return n;end;local function m(e,j,M)local l=e[S];local a=e[g];local G=e[d];return(function(...)local o={};local y=l;local l=d;local Y=W('#',...)-C;local J={...};local L={};local A=H local V={};local e=d e*=-1 local g=e;local k=a;local a=G;for e=0,Y do if(e>=k)then V[e-k]=J[e+C];else o[e]=J[e+d];end;end;local e=Y-k+d local e;local k;while true do e=a[l];k=e[(-93+0x5e)];n=(1162812)while(-85+0x9d)>=k do n-= n n=(10413494)while k<=(4025/0x73)do n-= n n=(4990928)while k<=(0x81-112)do n-= n n=(8159870)while k<=(1944/0xf3)do n-= n n=(1372546)while k<=(0x56-83)do n-= n n=(5654285)while k<=(116-(280-0xa5))do n-= n n=(6760820)while(0x6a+-106)<k do n-= n local k;local n;o[e[x]]=M[e[_]];l=l+d;e=a[l];n=e[x];k=o[e[D]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[w]]=o[e[D]][e[t]];l=l+d;e=a[l];o[e[w]]=o[e[_]][e[P]];l=l+d;e=a[l];n=e[x];k=o[e[i]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];o[e[x]]=M[e[_]];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];o[e[x]]=e[D];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[U]]=M[e[i]];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];n=e[b]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];do return end;break end while 3476==(n)/((287860/0x94))do local k;local n;n=e[U]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];n=e[h];k=o[e[c]];o[n+1]=k;o[n]=k[e[t]];l=l+d;e=a[l];o[e[b]]=M[e[c]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[O]))break end;break;end while(n)/((0x1cdd-3734))==1547 do n=(13283115)while(0x46/35)<k do n-= n local k;local n;o[e[h]]=M[e[f]];l=l+d;e=a[l];n=e[w];k=o[e[O]];o[n+1]=k;o[n]=k[e[s]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[U]]=o[e[c]][e[B]];l=l+d;e=a[l];o[e[U]]=o[e[c]][e[P]];l=l+d;e=a[l];n=e[w];k=o[e[i]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[b]]=M[e[D]];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];o[e[N]]=e[O];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[x]]=M[e[_]];l=l+d;e=a[l];o[e[x]]=e[O];l=l+d;e=a[l];o[e[x]]=e[O];l=l+d;e=a[l];o[e[b]]=e[_];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];n=e[N]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];do return end;break end while 3747==(n)/((127620/0x24))do local d=e[c];local l=o[d]for e=d+1,e[P]do l=l..o[e];end;o[e[N]]=l;break end;break;end break;end while 553==(n)/((5074-0xa20))do n=(227733)while k<=(0x2d0/144)do n-= n n=(347667)while(0x1e-26)<k do n-= n local h;local n;n=e[x]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];n=e[N];h=o[e[O]];o[n+1]=h;o[n]=h[e[B]];l=l+d;e=a[l];o[e[b]]=M[e[c]];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];o[e[x]]=e[D];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[i]))break end while 401==(n)/((0x3df+-124))do local c;local n;n=e[N]o[n](r(o,n+C,e[O]))l=l+d;e=a[l];n=e[b];c=o[e[O]];o[n+1]=c;o[n]=c[e[t]];l=l+d;e=a[l];o[e[x]]=M[e[_]];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];o[e[h]]=e[_];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[_]))break end;break;end while(n)/((398+-0x59))==737 do n=(61864)while k<=(0xcc/34)do n-= n l=e[D];break;end while 152==(n)/(((0x237930/102)/0x38))do n=(613040)while(0x5fd/219)<k do n-= n local c;local n;n=e[h]o[n](r(o,n+C,e[O]))l=l+d;e=a[l];n=e[N];c=o[e[_]];o[n+1]=c;o[n]=c[e[v]];l=l+d;e=a[l];o[e[w]]=M[e[f]];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[_]))break end while(n)/((797-0x199))==1580 do o[e[U]]=j[e[D]];break end;break;end break;end break;end break;end while 3790==(n)/((0xd241/25))do n=(6113870)while k<=(0x83+-119)do n-= n n=(9610480)while k<=(43-0x21)do n-= n n=(2402373)while(0x7ce/222)<k do n-= n o[e[x]]=(e[O]~=0);l=l+C;break end while 851==(n)/((2881+-0x3a))do local e=e[x]o[e]=o[e](o[e+C])break end;break;end while(n)/((0x1549-(-84+0xb25)))==3586 do n=(5328350)while(528/0x30)<k do n-= n local d=e[N];local l=o[e[i]];o[d+1]=l;o[d]=l[e[B]];break end while(n)/((-71+0x71a))==3050 do o[e[b]]=o[e[i]]%e[P];break end;break;end break;end while 1670==(n)/((3753+-0x5c))do n=(378400)while(-25+0x27)>=k do n-= n n=(902041)while(127-(0xb7+-69))<k do n-= n local b;local n;o[e[h]]=e[i];l=l+d;e=a[l];n=e[x]o[n](o[n+C])l=l+d;e=a[l];o[e[x]]=M[e[c]];l=l+d;e=a[l];n=e[w];b=o[e[D]];o[n+1]=b;o[n]=b[e[s]];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[w]]=o[e[c]][e[s]];l=l+d;e=a[l];o[e[w]]=o[e[c]][e[u]];l=l+d;e=a[l];n=e[w];b=o[e[O]];o[n+1]=b;o[n]=b[e[s]];l=l+d;e=a[l];o[e[h]]=o[e[i]];l=l+d;e=a[l];n=e[x]o[n](r(o,n+C,e[c]))break end while(n)/((61962/0x8a))==2009 do o[e[h]]=#o[e[O]];break end;break;end while 688==(n)/((-0x65+651))do n=(6328458)while k<=(510/0x22)do n-= n o[e[N]]=o[e[c]];break;end while 3481==(n)/((3746-0x788))do n=(4128254)while k>(137-0x79)do n-= n local l=e[w];local d=o[l];for e=l+1,e[i]do p(d,o[e])end;break end while 2158==(n)/((-0x10+1929))do local e=e[x]o[e]=o[e](o[e+C])break end;break;end break;end break;end break;end break;end while 2006==(n)/((2576+-0x58))do n=(12152438)while(143-0x75)>=k do n-= n n=(111757)while k<=(47+-0x1a)do n-= n n=(2511016)while k<=(94-0x4b)do n-= n n=(3580424)while k>(-86+0x68)do n-= n local k;local n;n=e[b];k=o[e[_]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[N]]=e[c];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[b]]=o[e[i]][e[t]];l=l+d;e=a[l];o[e[w]]=o[e[c]][e[P]];l=l+d;e=a[l];n=e[x];k=o[e[f]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[U]]=M[e[_]];l=l+d;e=a[l];o[e[N]]=e[c];l=l+d;e=a[l];o[e[U]]=e[_];l=l+d;e=a[l];o[e[N]]=e[O];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[b]o[n](r(o,n+C,e[c]))l=l+d;e=a[l];o[e[w]]=M[e[D]];l=l+d;e=a[l];o[e[U]]=e[i];l=l+d;e=a[l];n=e[N]o[n](o[n+C])l=l+d;e=a[l];l=e[D];break end while(n)/((-48+0xe8c))==974 do local h;local n;n=e[b]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[x];h=o[e[c]];o[n+1]=h;o[n]=h[e[P]];l=l+d;e=a[l];o[e[U]]=M[e[i]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[w]]=e[D];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[N]]=(e[_]~=0);l=l+d;e=a[l];o[e[b]]=M[e[_]];l=l+d;e=a[l];o[e[w]]=e[f];break end;break;end while(n)/((0x412d3/239))==2248 do n=(1845448)while((-0x67+190)+-67)<k do n-= n if(o[e[U]]~=o[e[u]])then l=l+C;else l=e[O];end;break end while(n)/((23048/0x2b))==3443 do local k;local n;n=e[b]o[n](r(o,n+C,e[O]))l=l+d;e=a[l];n=e[N];k=o[e[D]];o[n+1]=k;o[n]=k[e[v]];l=l+d;e=a[l];o[e[x]]=M[e[c]];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[h]]=(e[c]~=0);l=l+d;e=a[l];o[e[U]]=M[e[f]];l=l+d;e=a[l];o[e[N]]=e[D];break end;break;end break;end while 113==(n)/((97911/0x63))do n=(232946)while k<=(136-(238+-0x7d))do n-= n n=(435699)while k>(5456/0xf8)do n-= n local b;local n;n=e[U]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[w];b=o[e[_]];o[n+1]=b;o[n]=b[e[t]];l=l+d;e=a[l];o[e[N]]=M[e[i]];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];o[e[N]]=e[c];l=l+d;e=a[l];o[e[h]]=e[_];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[i]))break end while(n)/((0x281-344))==1467 do o[e[N]]=o[e[D]][o[e[B]]];break end;break;end while(n)/((-0x3b+157))==2377 do n=(4041813)while k<=(0x930/98)do n-= n local k;local n;n=e[x];k=o[e[c]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[N]]=o[e[D]][e[t]];l=l+d;e=a[l];o[e[U]]=o[e[_]][e[s]];l=l+d;e=a[l];n=e[x];k=o[e[c]];o[n+1]=k;o[n]=k[e[t]];l=l+d;e=a[l];o[e[x]]=M[e[c]];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[U]]=e[D];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[h]]={};l=l+d;e=a[l];o[e[w]][e[D]]=e[v];l=l+d;e=a[l];n=e[b]o[n](r(o,n+C,e[D]))l=l+d;e=a[l];o[e[w]]=M[e[D]];l=l+d;e=a[l];o[e[N]]=e[i];l=l+d;e=a[l];n=e[U]o[n](o[n+C])l=l+d;e=a[l];l=e[D];break;end while(n)/((6221-(-67+0xc85)))==1311 do n=(2027052)while k>(0x95+-124)do n-= n local e=e[w]o[e]=o[e]()break end while(n)/((0x4d100/192))==1233 do local n;o[e[w]]=e[D];l=l+d;e=a[l];o[e[N]]=e[i];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[U]]=(e[_]~=0);l=l+d;e=a[l];o[e[h]]=M[e[O]];l=l+d;e=a[l];o[e[w]]=e[i];l=l+d;e=a[l];o[e[U]]=e[O];l=l+d;e=a[l];o[e[U]]=e[D];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[i]))break end;break;end break;end break;end break;end while(n)/((0x1a43-3409))==3667 do n=(1243200)while k<=(7080/0xec)do n-= n n=(4721040)while k<=(0xad4/99)do n-= n n=(3551920)while(0xae-147)<k do n-= n local s;local b;local k;local n;o[e[h]]=M[e[_]];l=l+d;e=a[l];o[e[N]]=o[e[D]][e[v]];l=l+d;e=a[l];n=e[U];k=o[e[O]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[x]]=o[e[f]];l=l+d;e=a[l];o[e[x]]=o[e[f]];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[x];k=o[e[c]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];n=e[h]o[n]=o[n](o[n+C])l=l+d;e=a[l];b={o,e};b[C][b[S][w]]=b[d][b[S][P]]+b[C][b[S][_]];l=l+d;e=a[l];o[e[x]]=o[e[i]]%e[t];l=l+d;e=a[l];n=e[w]o[n]=o[n](o[n+C])l=l+d;e=a[l];k=e[_];s=o[k]for e=k+1,e[u]do s=s..o[e];end;o[e[U]]=s;l=l+d;e=a[l];b={o,e};b[C][b[S][x]]=b[d][b[S][t]]+b[C][b[S][f]];l=l+d;e=a[l];o[e[x]]=o[e[c]]%e[u];break end while(n)/((0x1274-2404))==1531 do local e=e[x]o[e](o[e+C])break end;break;end while(n)/(((0x19843a/250)-0xd29))==1422 do n=(6510342)while(0x92+-117)<k do n-= n local w;local n;n=e[b];w=o[e[i]];o[n+1]=w;o[n]=w[e[t]];l=l+d;e=a[l];o[e[N]]=e[c];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[x]]=o[e[D]][e[t]];l=l+d;e=a[l];o[e[h]]=o[e[c]][e[s]];l=l+d;e=a[l];n=e[h];w=o[e[i]];o[n+1]=w;o[n]=w[e[t]];l=l+d;e=a[l];n=e[h]o[n](o[n+C])l=l+d;e=a[l];o[e[b]]=M[e[O]];l=l+d;e=a[l];o[e[U]]();l=l+d;e=a[l];l=e[f];break end while(n)/(((0x1726-2975)+-0x2a))==2238 do local l=e[h]o[l](r(o,l+C,e[O]))break end;break;end break;end while 1184==(n)/((1148+-0x62))do n=(3933468)while k<=(0x99+-121)do n-= n n=(8044075)while(158-(5715/0x2d))<k do n-= n local C;local v,S;local k;local n;M[e[_]]=o[e[U]];l=l+d;e=a[l];o[e[x]]=M[e[f]];l=l+d;e=a[l];o[e[x]]=M[e[i]];l=l+d;e=a[l];n=e[x];k=o[e[i]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[U]]=M[e[O]];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];o[e[w]]=e[f];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[h]v,S=A(o[n](r(o,n+1,e[O])))g=S+n-1 C=0;for e=n,g do C=C+d;o[e]=v[C];end;l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,g))l=l+d;e=a[l];n=e[h]o[n]=o[n]()l=l+d;e=a[l];n=e[x];k=o[e[f]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[b]]={};l=l+d;e=a[l];o[e[h]]=M[e[i]];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[U]]=e[D];l=l+d;e=a[l];o[e[h]]=e[D];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[w]][e[D]]=o[e[P]];l=l+d;e=a[l];o[e[N]]=M[e[_]];l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];o[e[w]]=e[i];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[h]][e[D]]=o[e[B]];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[b];k=o[e[_]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[w]]=M[e[c]];l=l+d;e=a[l];o[e[x]]=e[_];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[x];k=o[e[c]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];o[e[U]]=M[e[c]];l=l+d;e=a[l];o[e[x]]=e[f];l=l+d;e=a[l];o[e[U]]=e[c];l=l+d;e=a[l];o[e[b]]=e[f];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[b];k=o[e[i]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[h]]=M[e[O]];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];o[e[h]]=e[_];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];n=e[N];k=o[e[O]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];o[e[N]]=M[e[O]];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];n=e[U];k=o[e[c]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];o[e[x]]=M[e[O]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[N]]=e[O];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];n=e[U];k=o[e[i]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[U]]=M[e[f]];l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];o[e[N]]=e[O];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];n=e[w];k=o[e[f]];o[n+1]=k;o[n]=k[e[s]];l=l+d;e=a[l];o[e[U]]=M[e[D]];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];n=e[N];k=o[e[i]];o[n+1]=k;o[n]=k[e[t]];l=l+d;e=a[l];o[e[U]]=M[e[_]];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];o[e[N]]=e[D];break end while(n)/((-0x15+(7033-0xdef)))==2335 do local c;local n;n=e[h]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[b];c=o[e[_]];o[n+1]=c;o[n]=c[e[P]];l=l+d;e=a[l];o[e[x]]=M[e[f]];l=l+d;e=a[l];o[e[h]]=e[D];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];o[e[U]]=e[i];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[b]]=(e[D]~=0);l=l+d;e=a[l];o[e[x]]=M[e[i]];l=l+d;e=a[l];o[e[w]]=e[f];break end;break;end while 2838==(n)/((2897-0x5e7))do n=(5795168)while(-54+0x57)>=k do n-= n local e=e[N]o[e]=o[e](r(o,e+d,g))break;end while(n)/((0xc49+-41))==1867 do n=(872772)while((0x16a-230)-0x62)<k do n-= n local O;local n;n=e[U]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[w];O=o[e[_]];o[n+1]=O;o[n]=O[e[s]];l=l+d;e=a[l];o[e[U]]=M[e[_]];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[U]]=e[c];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[x]]=(e[D]~=0);l=l+d;e=a[l];o[e[b]]=M[e[c]];l=l+d;e=a[l];o[e[U]]=e[i];break end while 3084==(n)/(((-0x17+620)-0x13a))do local a=e[b]local n={o[a](o[a+1])};local l=0;for e=a,e[B]do l=l+d;o[e]=n[l];end break end;break;end break;end break;end break;end break;end break;end while(n)/((0xfaf+-69))==2639 do n=(958040)while k<=(155-0x66)do n-= n n=(1189786)while(5280/0x78)>=k do n-= n n=(2672888)while(147+-0x6c)>=k do n-= n n=(7166954)while(118-0x51)>=k do n-= n n=(8170275)while k>(1080/0x1e)do n-= n l=e[f];break end while 3075==(n)/((542028/0xcc))do local x;local n;n=e[U]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];n=e[b];x=o[e[D]];o[n+1]=x;o[n]=x[e[v]];l=l+d;e=a[l];o[e[N]]=M[e[D]];l=l+d;e=a[l];o[e[N]]=e[c];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[_]))break end;break;end while 2066==(n)/((0xb979f/219))do n=(451112)while k>(0xb6-144)do n-= n local b;local n;n=e[w];b=o[e[f]];o[n+1]=b;o[n]=b[e[u]];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[x]]=o[e[D]][e[t]];l=l+d;e=a[l];o[e[x]]=o[e[c]][e[P]];l=l+d;e=a[l];n=e[h];b=o[e[D]];o[n+1]=b;o[n]=b[e[v]];l=l+d;e=a[l];o[e[h]]=M[e[D]];l=l+d;e=a[l];o[e[U]]=e[O];l=l+d;e=a[l];o[e[U]]=e[i];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[w]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];o[e[N]]=M[e[D]];l=l+d;e=a[l];o[e[U]]=e[O];l=l+d;e=a[l];n=e[w]o[n](o[n+C])l=l+d;e=a[l];l=e[f];break end while 3317==(n)/(((6466+-0x4a)/0x2f))do local k;local n;o[e[x]]={};l=l+d;e=a[l];o[e[x]]=e[O];l=l+d;e=a[l];o[e[U]]=e[_];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[h]]=e[D];l=l+d;e=a[l];o[e[x]]=e[D];l=l+d;e=a[l];o[e[h]]=M[e[f]];l=l+d;e=a[l];o[e[x]]=e[_];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];o[e[b]]=e[f];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];o[e[w]]=e[i];l=l+d;e=a[l];o[e[U]]=M[e[_]];l=l+d;e=a[l];o[e[x]]=e[f];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];o[e[b]]=e[f];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[h]]=e[O];l=l+d;e=a[l];o[e[N]]=e[O];l=l+d;e=a[l];o[e[x]]=M[e[c]];l=l+d;e=a[l];o[e[w]]=e[D];l=l+d;e=a[l];o[e[x]]=e[D];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[N]]=M[e[i]];l=l+d;e=a[l];o[e[N]]=e[O];l=l+d;e=a[l];o[e[h]]=e[_];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[U]]=e[i];l=l+d;e=a[l];o[e[h]]=M[e[c]];l=l+d;e=a[l];o[e[U]]=e[_];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[U]]=e[D];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[h]]=e[D];l=l+d;e=a[l];o[e[h]]=M[e[c]];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[b];k=o[n];for e=n+1,e[c]do p(k,o[e])end;break end;break;end break;end while 1459==(n)/((408536/0xdf))do n=(1597074)while(142-0x65)>=k do n-= n n=(8089077)while k>(0xf28/97)do n-= n local n;n=e[U]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[b]]=M[e[c]];l=l+d;e=a[l];o[e[U]]=M[e[_]];l=l+d;e=a[l];o[e[N]]=e[_];l=l+d;e=a[l];o[e[x]]=e[D];l=l+d;e=a[l];o[e[U]]=e[O];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[U]o[n](o[n+C])l=l+d;e=a[l];do return end;break end while 4071==(n)/((-0x2b+2030))do o[e[b]]();break end;break;end while 3749==(n)/((89460/0xd2))do n=(2369115)while(-122+0xa4)>=k do n-= n local k;local n;n=e[h];k=o[e[f]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[x]]=o[e[D]][e[v]];l=l+d;e=a[l];o[e[h]]=o[e[O]][e[v]];l=l+d;e=a[l];n=e[U];k=o[e[c]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[x]]=M[e[c]];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];o[e[w]]=e[i];l=l+d;e=a[l];o[e[h]]=e[D];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[x]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];o[e[N]]=M[e[O]];l=l+d;e=a[l];o[e[N]]=e[i];l=l+d;e=a[l];n=e[b]o[n](o[n+C])l=l+d;e=a[l];l=e[i];break;end while(n)/((172270/0xd6))==2943 do n=(7449839)while(-64+0x6b)<k do n-= n local l=e[w];local d=o[l];for e=l+1,e[f]do p(d,o[e])end;break end while 3799==(n)/((-0x13+1980))do local a=e[N];local r=e[v];local n=a+2 local a={o[a](o[a+1],o[n])};for e=1,r do o[n+e]=a[e];end;local a=a[1]if a then o[n]=a l=e[f];else l=l+d;end;break end;break;end break;end break;end break;end while 1742==(n)/((0x1ad8b/161))do n=(2944425)while(-126+0xae)>=k do n-= n n=(3896250)while k<=(6670/0x91)do n-= n n=(51750)while((0x55b7-11008)/0xf3)<k do n-= n M[e[O]]=o[e[w]];break end while 2875==(n)/((0x8b-121))do if o[e[h]]then l=l+d;else l=e[c];end;break end;break;end while 1039==(n)/((7524-0xebe))do n=(1947814)while k>(10622/0xe2)do n-= n local n;o[e[w]]=M[e[O]];l=l+d;e=a[l];o[e[b]]=e[_];l=l+d;e=a[l];o[e[x]]=e[f];l=l+d;e=a[l];o[e[h]]=e[_];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[i]))break end while 638==(n)/((6174-0xc31))do do return end;break end;break;end break;end while 1419==(n)/(((373500/0x4)/45))do n=(315180)while(8250/0xa5)>=k do n-= n n=(7542261)while k>((-0x55+-21)+155)do n-= n o[e[h]][e[c]]=e[s];break end while(n)/((3720+-0x15))==2039 do o[e[w]]=o[e[c]]%e[s];break end;break;end while 85==(n)/((0x5a870/100))do n=(5507359)while k<=(169-0x76)do n-= n local U;local n;o[e[h]]=M[e[i]];l=l+d;e=a[l];n=e[h];U=o[e[_]];o[n+1]=U;o[n]=U[e[s]];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[N]]=o[e[c]][e[B]];l=l+d;e=a[l];o[e[x]]=o[e[c]][e[v]];l=l+d;e=a[l];n=e[b];U=o[e[O]];o[n+1]=U;o[n]=U[e[v]];l=l+d;e=a[l];o[e[h]]=M[e[O]];l=l+d;e=a[l];o[e[N]]=e[i];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[N]]=M[e[i]];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[w]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];do return end;break;end while 2717==(n)/((324320/0xa0))do n=(3854752)while k>(1924/0x25)do n-= n local l=e[h]o[l]=o[l](r(o,l+d,e[c]))break end while(n)/(((5234+-0x3d)-2610))==1504 do o[e[b]][o[e[i]]]=o[e[B]];break end;break;end break;end break;end break;end break;end while 1114==(n)/((0x6e6-906))do n=(9967356)while k<=(4898/0x4f)do n-= n n=(683606)while(159-0x66)>=k do n-= n n=(152390)while k<=(0x66+-47)do n-= n n=(141828)while(135-0x51)<k do n-= n local w;local n;n=e[U]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[x];w=o[e[c]];o[n+1]=w;o[n]=w[e[t]];l=l+d;e=a[l];o[e[b]]=M[e[i]];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];o[e[x]]=e[_];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[x]]=(e[f]~=0);l=l+d;e=a[l];o[e[b]]=M[e[c]];l=l+d;e=a[l];o[e[U]]=e[i];break end while(n)/(((-8732/0x76)+0xb4))==1338 do o[e[w]]=M[e[O]];break end;break;end while(n)/((188+-0x5a))==1555 do n=(1258425)while((407-0x107)-88)<k do n-= n o[e[x]]={};break end while 1071==(n)/((0xd7b9/47))do local e=e[b]o[e]=o[e](r(o,e+d,g))break end;break;end break;end while(n)/((7175-0xe31))==193 do n=(1747369)while(-27+0x56)>=k do n-= n n=(2151322)while((933+-0x3f)/15)<k do n-= n o[e[h]]=#o[e[O]];break end while(n)/((0x3cae2/151))==1307 do o[e[x]]={};break end;break;end while(n)/((-28+0x72b))==967 do n=(5632254)while k<=(0x23a0/152)do n-= n local a=e[U]local n={o[a](o[a+1])};local l=0;for e=a,e[u]do l=l+d;o[e]=n[l];end break;end while 1458==(n)/((0xf5b+-68))do n=(2469496)while(153+-0x5c)<k do n-= n local k;local n;o[e[b]]=M[e[O]];l=l+d;e=a[l];n=e[x];k=o[e[O]];o[n+1]=k;o[n]=k[e[t]];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[w]]=o[e[O]][e[P]];l=l+d;e=a[l];o[e[N]]=o[e[c]][e[t]];l=l+d;e=a[l];n=e[h];k=o[e[O]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[w]]=M[e[D]];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];o[e[N]]=e[c];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[b]]=M[e[D]];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[h]o[n](r(o,n+C,e[c]))l=l+d;e=a[l];do return end;break end while(n)/((7554-0xeea))==661 do o[e[w]]=j[e[c]];l=l+d;e=a[l];o[e[N]]=#o[e[D]];l=l+d;e=a[l];j[e[D]]=o[e[x]];l=l+d;e=a[l];o[e[U]]=j[e[O]];l=l+d;e=a[l];o[e[b]]=#o[e[c]];l=l+d;e=a[l];j[e[O]]=o[e[U]];l=l+d;e=a[l];do return end;break end;break;end break;end break;end break;end while(n)/((-36+0xc48))==3207 do n=(3572811)while k<=(0x71+-46)do n-= n n=(6856884)while(0x900/36)>=k do n-= n n=(15265830)while k>(0xb52/46)do n-= n local i;local n;n=e[b]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[w];i=o[e[_]];o[n+1]=i;o[n]=i[e[P]];l=l+d;e=a[l];o[e[b]]=M[e[D]];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];o[e[U]]=e[_];l=l+d;e=a[l];o[e[b]]=e[_];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[U]]=(e[_]~=0);l=l+d;e=a[l];o[e[w]]=M[e[D]];l=l+d;e=a[l];o[e[U]]=e[_];break end while 3774==(n)/((8130-0xff5))do local x;local n;n=e[N];x=o[e[_]];o[n+1]=x;o[n]=x[e[P]];l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[w]]=o[e[i]][e[P]];l=l+d;e=a[l];o[e[N]]=o[e[_]][e[s]];l=l+d;e=a[l];n=e[w];x=o[e[f]];o[n+1]=x;o[n]=x[e[u]];l=l+d;e=a[l];o[e[U]]=e[O];l=l+d;e=a[l];n=e[U]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];o[e[N]]=M[e[_]];l=l+d;e=a[l];o[e[N]]();l=l+d;e=a[l];l=e[i];break end;break;end while(n)/((455679/0xbd))==2844 do n=(5602221)while k<=(-46+0x6f)do n-= n o[e[h]]=m(y[e[i]],nil,M);break;end while 3259==(n)/((0x726+-111))do n=(2611718)while(188+-0x7a)<k do n-= n local c;local n;n=e[h]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[b];c=o[e[O]];o[n+1]=c;o[n]=c[e[v]];l=l+d;e=a[l];o[e[h]]=M[e[O]];l=l+d;e=a[l];o[e[U]]=e[i];l=l+d;e=a[l];o[e[x]]=e[O];l=l+d;e=a[l];o[e[x]]=e[O];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[N]]=(e[f]~=0);l=l+d;e=a[l];o[e[U]]=M[e[O]];l=l+d;e=a[l];o[e[U]]=e[O];break end while(n)/((0x140e-2576))==1021 do local l=e[x]local a,e=A(o[l](r(o,l+1,e[c])))g=e+l-1 local e=0;for l=l,g do e=e+d;o[l]=a[e];end;break end;break;end break;end break;end while 1661==(n)/((4373-0x8ae))do n=(3084300)while((-0x43+4690)/67)>=k do n-= n n=(2445220)while k>(218-0x96)do n-= n local U;local n;n=e[h]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[w];U=o[e[i]];o[n+1]=U;o[n]=U[e[u]];l=l+d;e=a[l];o[e[h]]=M[e[c]];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];o[e[x]]=e[D];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[w]]=(e[f]~=0);l=l+d;e=a[l];o[e[b]]=M[e[f]];l=l+d;e=a[l];o[e[N]]=e[O];break end while 1187==(n)/((0x1052-2118))do o[e[h]]=M[e[D]];break end;break;end while 900==(n)/((582590/0xaa))do n=(1818775)while k<=(151+-0x51)do n-= n local k;local n;n=e[U];k=o[e[c]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[h]]=o[e[O]][e[v]];l=l+d;e=a[l];o[e[w]]=o[e[O]][e[u]];l=l+d;e=a[l];n=e[w];k=o[e[i]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];n=e[x]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];o[e[b]]=M[e[O]];l=l+d;e=a[l];o[e[U]]();l=l+d;e=a[l];l=e[O];break;end while 3325==(n)/((0x1f3fe/234))do n=(3183773)while(0xa7+-96)<k do n-= n M[e[O]]=o[e[h]];l=l+d;e=a[l];o[e[N]]={};l=l+d;e=a[l];o[e[x]]={};l=l+d;e=a[l];M[e[i]]=o[e[b]];l=l+d;e=a[l];o[e[U]]=M[e[i]];l=l+d;e=a[l];if(o[e[h]]==e[P])then l=l+C;else l=e[i];end;break end while 1273==(n)/((2520+-0x13))do local k;local n;n=e[h]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];n=e[x];k=o[e[D]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];o[e[U]]=M[e[c]];l=l+d;e=a[l];o[e[h]]=e[f];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];o[e[w]]=e[i];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[x]]=(e[_]~=0);l=l+d;e=a[l];o[e[x]]=M[e[c]];break end;break;end break;end break;end break;end break;end break;end break;end while(n)/((0x245+(-94+0x15)))==2289 do n=(2616066)while(24525/0xe1)>=k do n-= n n=(114554)while(19080/0xd4)>=k do n-= n n=(15725792)while(15795/0xc3)>=k do n-= n n=(134784)while(194+-0x76)>=k do n-= n n=(1542255)while k<=(203-0x81)do n-= n n=(4862600)while((425-0xf8)-0x68)<k do n-= n local e=e[b]o[e](o[e+C])break end while(n)/((4816-0x98c))==2050 do if(o[e[x]]==e[P])then l=l+C;else l=e[i];end;break end;break;end while 429==(n)/((668670/0xba))do n=(8520700)while(6450/0x56)<k do n-= n local k;local n;o[e[h]]={};l=l+d;e=a[l];o[e[h]]=M[e[c]];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];o[e[h]]=e[D];l=l+d;e=a[l];o[e[w]]=e[i];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[b]]=M[e[_]];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];o[e[w]]=e[f];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[x]]=M[e[f]];l=l+d;e=a[l];o[e[b]]=e[f];l=l+d;e=a[l];o[e[U]]=e[i];l=l+d;e=a[l];o[e[N]]=e[i];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[x]]=M[e[f]];l=l+d;e=a[l];o[e[h]]=e[D];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];o[e[h]]=e[D];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[b]]=M[e[c]];l=l+d;e=a[l];o[e[h]]=e[_];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];o[e[U]]=e[O];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[x]]=M[e[D]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[U]]=e[i];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[N]]=M[e[f]];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[b]]=M[e[O]];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];o[e[x]]=e[D];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[h];k=o[n];for e=n+1,e[f]do p(k,o[e])end;break end while(n)/((653300/(0x1c3-263)))==2452 do local k;local n;n=e[x]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[h];k=o[e[O]];o[n+1]=k;o[n]=k[e[s]];l=l+d;e=a[l];o[e[N]]=M[e[i]];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];o[e[U]]=e[c];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[h];k=o[e[_]];o[n+1]=k;o[n]=k[e[B]];break end;break;end break;end while(n)/((-0x6e+146))==3744 do n=(11419902)while k<=(0xf3-165)do n-= n n=(1840644)while k>(-0x13+96)do n-= n local x;local n;n=e[U]o[n](r(o,n+C,e[c]))l=l+d;e=a[l];n=e[w];x=o[e[D]];o[n+1]=x;o[n]=x[e[s]];l=l+d;e=a[l];o[e[N]]=M[e[c]];l=l+d;e=a[l];o[e[b]]=e[_];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[w]]=e[i];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[U]]=(e[D]~=0);l=l+d;e=a[l];o[e[b]]=M[e[_]];l=l+d;e=a[l];o[e[h]]=e[_];break end while 2052==(n)/((0x735-(-83+0x407)))do local e={o,e};e[C][e[S][x]]=e[d][e[S][B]]+e[C][e[S][O]];break end;break;end while(n)/((-0x19+3982))==2886 do n=(9046794)while k<=(0xc0-113)do n-= n local b;local n;n=e[U];b=o[e[f]];o[n+1]=b;o[n]=b[e[B]];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[U]]=o[e[D]][e[P]];l=l+d;e=a[l];o[e[w]]=o[e[O]][e[t]];l=l+d;e=a[l];n=e[x];b=o[e[D]];o[n+1]=b;o[n]=b[e[u]];l=l+d;e=a[l];o[e[U]]=M[e[O]];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];o[e[h]]=e[O];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[h]o[n](r(o,n+C,e[_]))l=l+d;e=a[l];o[e[x]]=M[e[i]];l=l+d;e=a[l];o[e[w]]=e[D];l=l+d;e=a[l];n=e[h]o[n](o[n+C])l=l+d;e=a[l];l=e[i];break;end while 2707==(n)/((6799-0xd81))do n=(4169536)while k>(272-0xc0)do n-= n o[e[w]]=e[f];break end while(n)/(((14682-0x1cdd)-0xe4d))==1148 do o[e[U]][e[O]]=o[e[v]];break end;break;end break;end break;end break;end while 3908==(n)/((0x100e+-86))do n=(13522238)while(0xc5-112)>=k do n-= n n=(715566)while k<=((0x19-50)+0x6c)do n-= n n=(7549554)while k>(0xce-124)do n-= n o[e[U]]=j[e[c]];break end while(n)/((13164/0x4))==2294 do local d=e[h];local a=o[d]local n=o[d+2];if(n>0)then if(a>o[d+1])then l=e[_];else o[d+3]=a;end elseif(a<o[d+1])then l=e[f];else o[d+3]=a;end break end;break;end while(n)/((-0x5b+808))==998 do n=(1140636)while((823536/0xe4)/43)<k do n-= n local l=e[U]o[l](r(o,l+C,e[f]))break end while(n)/(((-0x2b+-25)+0x200))==2569 do local O;local n;n=e[x]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];n=e[w];O=o[e[_]];o[n+1]=O;o[n]=O[e[P]];l=l+d;e=a[l];o[e[N]]=M[e[f]];l=l+d;e=a[l];o[e[N]]=e[_];l=l+d;e=a[l];o[e[U]]=e[i];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[w]]=(e[_]~=0);l=l+d;e=a[l];o[e[x]]=M[e[f]];break end;break;end break;end while(n)/((0xe9684/236))==3338 do n=(314252)while k<=(-0x40+151)do n-= n n=(3630500)while k>(0x4df0/232)do n-= n local U;local n;n=e[N]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[h];U=o[e[O]];o[n+1]=U;o[n]=U[e[s]];l=l+d;e=a[l];o[e[h]]=M[e[_]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[b]]=e[_];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[b]]=(e[f]~=0);l=l+d;e=a[l];o[e[b]]=M[e[D]];l=l+d;e=a[l];o[e[x]]=e[c];break end while(n)/((0xa5a0/40))==3425 do local h;local n;n=e[x];h=o[e[O]];o[n+1]=h;o[n]=h[e[B]];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[x]]=o[e[D]][e[u]];l=l+d;e=a[l];o[e[w]]=o[e[f]][e[s]];l=l+d;e=a[l];n=e[x];h=o[e[i]];o[n+1]=h;o[n]=h[e[u]];l=l+d;e=a[l];o[e[N]]=j[e[O]];l=l+d;e=a[l];o[e[x]]=M[e[D]];l=l+d;e=a[l];o[e[U]]=e[O];l=l+d;e=a[l];o[e[b]]=e[f];l=l+d;e=a[l];o[e[b]]=e[_];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[U]o[n](r(o,n+C,e[c]))l=l+d;e=a[l];o[e[x]]=M[e[O]];l=l+d;e=a[l];o[e[b]]();l=l+d;e=a[l];l=e[i];break end;break;end while(n)/((-0x69+356))==1252 do n=(12613414)while k<=(0xdf-135)do n-= n local k;local n;n=e[w];k=o[e[_]];o[n+1]=k;o[n]=k[e[t]];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[b]]=o[e[_]][e[P]];l=l+d;e=a[l];o[e[w]]=o[e[_]][e[B]];l=l+d;e=a[l];n=e[x];k=o[e[i]];o[n+1]=k;o[n]=k[e[t]];l=l+d;e=a[l];o[e[N]]=M[e[O]];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];o[e[U]]=e[_];l=l+d;e=a[l];o[e[x]]=e[D];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[x]o[n](r(o,n+C,e[f]))l=l+d;e=a[l];o[e[b]]=M[e[O]];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];n=e[w]o[n](o[n+C])l=l+d;e=a[l];l=e[f];break;end while 3203==(n)/((-75+0xfad))do n=(7889754)while(-0x1a+115)<k do n-= n o[e[b]]=m(y[e[c]],nil,M);break end while 2311==(n)/((0x29acc/50))do local h;local n;o[e[b]]=M[e[i]];l=l+d;e=a[l];o[e[U]]=e[O];l=l+d;e=a[l];o[e[x]]=e[_];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[U];h=o[e[i]];o[n+1]=h;o[n]=h[e[B]];l=l+d;e=a[l];o[e[N]]=M[e[_]];l=l+d;e=a[l];o[e[b]]=e[f];l=l+d;e=a[l];o[e[w]]=e[D];break end;break;end break;end break;end break;end break;end while(n)/((217382/0xf1))==127 do n=(549636)while k<=(-47+0x92)do n-= n n=(1977300)while k<=(309-0xd7)do n-= n n=(6862900)while k<=(0xeb-143)do n-= n n=(4573967)while(-0x51+172)<k do n-= n local e={o,e};e[C][e[S][U]]=e[d][e[S][v]]+e[C][e[S][O]];break end while(n)/((1519+-0x48))==3161 do local h;local n;o[e[x]]=M[e[D]];l=l+d;e=a[l];n=e[b];h=o[e[D]];o[n+1]=h;o[n]=h[e[s]];l=l+d;e=a[l];o[e[U]]=e[i];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[b]]=o[e[i]][e[s]];l=l+d;e=a[l];o[e[w]]=o[e[D]][e[v]];l=l+d;e=a[l];n=e[N];h=o[e[f]];o[n+1]=h;o[n]=h[e[s]];l=l+d;e=a[l];o[e[b]]=M[e[f]];l=l+d;e=a[l];o[e[U]]=e[O];l=l+d;e=a[l];o[e[w]]=e[D];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[b]]=M[e[D]];l=l+d;e=a[l];o[e[U]]=e[c];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[U]]=e[c];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[x]o[n](r(o,n+C,e[c]))l=l+d;e=a[l];do return end;break end;break;end while 1700==(n)/((0x1014+-79))do n=(3966101)while(0x97+-58)<k do n-= n o[e[b]][o[e[_]]]=o[e[v]];break end while 1877==(n)/((0x10d4-2195))do local l=e[h]local a,e=A(o[l](r(o,l+1,e[i])))g=e+l-1 local e=0;for l=l,g do e=e+d;o[l]=a[e];end;break end;break;end break;end while 507==(n)/((7826-0xf56))do n=(405852)while k<=(227-0x83)do n-= n n=(1798432)while(0x134-213)<k do n-= n o[e[x]]=o[e[c]];break end while(n)/((0x13a70/117))==2614 do do return end;break end;break;end while(n)/((4432-0x8ca))==186 do n=(4853303)while(-92+0xbd)>=k do n-= n local i;local r;local n;o[e[N]]=e[c];l=l+d;e=a[l];o[e[w]]=e[f];l=l+d;e=a[l];o[e[x]]=#o[e[D]];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];n=e[w];r=o[n]i=o[n+2];if(i>0)then if(r>o[n+1])then l=e[_];else o[n+3]=r;end elseif(r<o[n+1])then l=e[f];else o[n+3]=r;end break;end while 1729==(n)/((5694-0xb47))do n=(3364464)while k>((0x41a0/56)-202)do n-= n o[e[N]]=o[e[O]][o[e[P]]];break end while 1392==(n)/((2462+-0x2d))do local d=e[h];local a=o[d]local n=o[d+2];if(n>0)then if(a>o[d+1])then l=e[i];else o[d+3]=a;end elseif(a<o[d+1])then l=e[i];else o[d+3]=a;end break end;break;end break;end break;end break;end while 652==(n)/((862+-0x13))do n=(3346400)while k<=(184+(-0xe60/46))do n-= n n=(679662)while k<=(0x125-192)do n-= n n=(4795056)while k>(0x110-172)do n-= n do return o[e[x]]end break end while(n)/((-0x22+1312))==3752 do local c;local n;n=e[h]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];n=e[x];c=o[e[f]];o[n+1]=c;o[n]=c[e[B]];l=l+d;e=a[l];o[e[x]]=M[e[O]];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];o[e[h]]=e[O];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[i]))break end;break;end while 549==(n)/((0x4fe+-40))do n=(9187308)while k<=(0x10a-164)do n-= n o[e[w]]=o[e[i]][e[v]];break;end while 2412==(n)/((0x6827/(40+-0x21)))do n=(6065488)while(247-0x90)<k do n-= n local k;local n;n=e[x];k=o[e[_]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[b]]=e[i];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[x]]=o[e[f]][e[u]];l=l+d;e=a[l];o[e[h]]=o[e[f]][e[s]];l=l+d;e=a[l];n=e[h];k=o[e[O]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[x]]=M[e[_]];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];o[e[N]]=e[c];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[x]o[n](r(o,n+C,e[O]))l=l+d;e=a[l];o[e[b]]=M[e[O]];l=l+d;e=a[l];n=e[b];k=o[e[O]];o[n+1]=k;o[n]=k[e[v]];l=l+d;e=a[l];o[e[h]]=e[c];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[U]]=o[e[c]][e[v]];l=l+d;e=a[l];o[e[N]]=o[e[D]][e[B]];l=l+d;e=a[l];n=e[U];k=o[e[c]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];o[e[x]]=e[_];l=l+d;e=a[l];o[e[U]]=M[e[_]];l=l+d;e=a[l];o[e[b]]=e[_];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];n=e[N]o[n](r(o,n+C,e[D]))l=l+d;e=a[l];o[e[h]]=M[e[i]];l=l+d;e=a[l];n=e[x];k=o[e[O]];o[n+1]=k;o[n]=k[e[t]];l=l+d;e=a[l];o[e[w]]=e[D];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[U]]=o[e[i]][e[s]];l=l+d;e=a[l];o[e[b]]=o[e[O]][e[s]];l=l+d;e=a[l];n=e[w];k=o[e[f]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];o[e[x]]=M[e[O]];l=l+d;e=a[l];o[e[x]]=e[_];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];o[e[b]]=e[f];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[h]o[n](r(o,n+C,e[c]))l=l+d;e=a[l];o[e[x]]=M[e[D]];l=l+d;e=a[l];n=e[U];k=o[e[O]];o[n+1]=k;o[n]=k[e[s]];l=l+d;e=a[l];o[e[w]]=e[D];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[x]]=o[e[_]][e[t]];l=l+d;e=a[l];o[e[b]]=o[e[D]][e[s]];l=l+d;e=a[l];n=e[b];k=o[e[_]];o[n+1]=k;o[n]=k[e[B]];l=l+d;e=a[l];o[e[x]]=e[_];l=l+d;e=a[l];o[e[U]]=M[e[f]];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[U]o[n](r(o,n+C,e[c]))l=l+d;e=a[l];o[e[b]]=M[e[_]];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];n=e[x]o[n](o[n+C])l=l+d;e=a[l];l=e[c];break end while 2288==(n)/((0x1513-2744))do local d=e[O];local l=o[d]for e=d+1,e[u]do l=l..o[e];end;o[e[U]]=l;break end;break;end break;end break;end while(n)/((0x11c0-2319))==1504 do n=(14941145)while(-104+0xd2)>=k do n-= n n=(938716)while(282-0xb1)<k do n-= n if(o[e[h]]==o[e[P]])then l=l+C;else l=e[_];end;break end while(n)/((0xb71-1511))==662 do o[e[x]]=(e[_]~=0);l=l+C;break end;break;end while 3979==(n)/((-0x7a+3877))do n=(4316184)while(0xa3+-56)>=k do n-= n local c;local n;n=e[h]o[n](r(o,n+C,e[D]))l=l+d;e=a[l];n=e[h];c=o[e[D]];o[n+1]=c;o[n]=c[e[s]];l=l+d;e=a[l];o[e[U]]=M[e[i]];l=l+d;e=a[l];o[e[N]]=e[_];l=l+d;e=a[l];o[e[x]]=e[O];l=l+d;e=a[l];o[e[h]]=e[_];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[O]))break;end while(n)/((235818/0x63))==1812 do n=(4064292)while k>(0x13d4/47)do n-= n local k;local n;n=e[h];k=o[e[O]];o[n+1]=k;o[n]=k[e[v]];l=l+d;e=a[l];o[e[b]]=e[D];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[w]]=o[e[i]][e[s]];l=l+d;e=a[l];o[e[h]]=o[e[i]][e[u]];l=l+d;e=a[l];n=e[w];k=o[e[O]];o[n+1]=k;o[n]=k[e[s]];l=l+d;e=a[l];o[e[x]]=M[e[f]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[b]]=e[_];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];n=e[h]o[n](r(o,n+C,e[D]))l=l+d;e=a[l];o[e[x]]=M[e[O]];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];n=e[U]o[n](o[n+C])l=l+d;e=a[l];l=e[i];break end while 2061==(n)/((-98+0x816))do o[e[x]]();break end;break;end break;end break;end break;end break;end break;end while 639==(n)/((0x10fde/17))do n=(3441480)while k<=(0x158-217)do n-= n n=(10667800)while k<=(160+-0x2a)do n-= n n=(4600500)while(-49+0xa2)>=k do n-= n n=(981856)while(176+(-10205/0x9d))>=k do n-= n n=(7264950)while(27830/0xfd)<k do n-= n o[e[h]]=e[f];break end while(n)/((0x1476-2648))==2805 do o[e[U]]=o[e[i]]-o[e[t]];break end;break;end while(n)/(((0x15d0a/43)-1072))==976 do n=(469931)while(320-0xd0)<k do n-= n local r=y[e[D]];local n;local d={};n=Q({},{__index=function(l,e)local e=d[e];return e[1][e[2]];end,__newindex=function(o,e,l)local e=d[e]e[1][e[2]]=l;end;});for n=1,e[P]do l=l+C;local e=a[l];if e[(44/0x2c)]==15 then d[n-1]={o,e[f]};else d[n-1]={j,e[_]};end;L[#L+1]=d;end;o[e[N]]=m(r,n,M);break end while 1309==(n)/((39131/0x6d))do local k;local n;o[e[N]]=M[e[i]];l=l+d;e=a[l];n=e[x];k=o[e[f]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];o[e[N]]=o[e[_]][e[v]];l=l+d;e=a[l];o[e[U]]=o[e[D]][e[u]];l=l+d;e=a[l];n=e[b];k=o[e[f]];o[n+1]=k;o[n]=k[e[P]];l=l+d;e=a[l];o[e[U]]=M[e[i]];l=l+d;e=a[l];o[e[U]]=e[_];l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];o[e[U]]=M[e[D]];l=l+d;e=a[l];o[e[x]]=e[O];l=l+d;e=a[l];o[e[w]]=e[D];l=l+d;e=a[l];o[e[N]]=e[_];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];n=e[x]o[n](r(o,n+C,e[f]))l=l+d;e=a[l];do return end;break end;break;end break;end while 1500==(n)/((6261-0xc7a))do n=(5534760)while k<=(0x12c-185)do n-= n n=(26378)while k>(255-0x8d)do n-= n local b;local n;n=e[x];b=o[e[i]];o[n+1]=b;o[n]=b[e[s]];l=l+d;e=a[l];o[e[w]]=e[f];l=l+d;e=a[l];n=e[N]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[U]]=o[e[c]][e[s]];l=l+d;e=a[l];o[e[h]]=o[e[c]][e[t]];l=l+d;e=a[l];n=e[N];b=o[e[D]];o[n+1]=b;o[n]=b[e[t]];l=l+d;e=a[l];o[e[w]]=M[e[i]];l=l+d;e=a[l];o[e[w]]=e[i];l=l+d;e=a[l];o[e[U]]=e[D];l=l+d;e=a[l];o[e[U]]=e[D];l=l+d;e=a[l];n=e[x]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[x]o[n](r(o,n+C,e[i]))l=l+d;e=a[l];o[e[h]]=M[e[i]];l=l+d;e=a[l];o[e[N]]=e[c];l=l+d;e=a[l];n=e[h]o[n](o[n+C])l=l+d;e=a[l];l=e[f];break end while 22==(n)/((2510-0x51f))do if(o[e[x]]~=e[P])then l=l+C;else l=e[c];end;break end;break;end while(n)/((0x1862-3162))==1797 do n=(2729666)while(299-0xb7)>=k do n-= n local d=e[w];local n=o[d+2];local a=o[d]+n;o[d]=a;if(n>0)then if(a<=o[d+1])then l=e[f];o[d+3]=a;end elseif(a>=o[d+1])then l=e[c];o[d+3]=a;end break;end while(n)/((-65+0x373))==3337 do n=(11980885)while k>(0x151-220)do n-= n local b;local n;n=e[U]o[n](r(o,n+C,e[O]))l=l+d;e=a[l];n=e[x];b=o[e[f]];o[n+1]=b;o[n]=b[e[B]];l=l+d;e=a[l];o[e[N]]=M[e[_]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[N]]=e[i];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[_]))break end while 3665==(n)/((-0x2a+3311))do local i;local n;n=e[N];i=o[e[f]];o[n+1]=i;o[n]=i[e[t]];l=l+d;e=a[l];o[e[N]]=e[D];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[x]]=o[e[_]][e[u]];l=l+d;e=a[l];o[e[N]]=o[e[_]][e[B]];l=l+d;e=a[l];n=e[h];i=o[e[D]];o[n+1]=i;o[n]=i[e[t]];l=l+d;e=a[l];o[e[N]]=M[e[f]];l=l+d;e=a[l];o[e[x]]=e[D];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];o[e[h]]=e[D];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[h]o[n](r(o,n+C,e[O]))l=l+d;e=a[l];o[e[w]]=M[e[_]];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];n=e[N]o[n](o[n+C])l=l+d;e=a[l];l=e[f];break end;break;end break;end break;end break;end while 2984==(n)/((0xe33+-60))do n=(7493353)while k<=(325-0xcb)do n-= n n=(47187)while(0xa1+-41)>=k do n-= n n=(2746858)while(-91+0xd2)<k do n-= n local n;o[e[x]]=M[e[D]];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[U]]=e[D];l=l+d;e=a[l];o[e[h]]=e[O];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[f]))break end while(n)/((1221+-0x62))==2446 do if o[e[w]]then l=l+d;else l=e[i];end;break end;break;end while(n)/((144450/0x96))==49 do n=(5498091)while(20328/0xa8)<k do n-= n local i;local n;n=e[w]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[U];i=o[e[f]];o[n+1]=i;o[n]=i[e[u]];l=l+d;e=a[l];o[e[x]]=M[e[D]];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];o[e[w]]=e[f];l=l+d;e=a[l];o[e[b]]=e[f];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[x]]=(e[c]~=0);l=l+d;e=a[l];o[e[w]]=M[e[O]];l=l+d;e=a[l];o[e[x]]=e[c];break end while 2271==(n)/((4937-0x9d4))do local k;local n;o[e[w]]=M[e[c]];l=l+d;e=a[l];n=e[h];k=o[e[i]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[x]]=e[c];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[b]]=o[e[f]][e[P]];l=l+d;e=a[l];o[e[U]]=o[e[i]][e[u]];l=l+d;e=a[l];n=e[U];k=o[e[c]];o[n+1]=k;o[n]=k[e[u]];l=l+d;e=a[l];o[e[x]]=M[e[O]];l=l+d;e=a[l];o[e[x]]=e[O];l=l+d;e=a[l];o[e[w]]=e[f];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[O]))l=l+d;e=a[l];o[e[h]]=M[e[_]];l=l+d;e=a[l];o[e[b]]=e[_];l=l+d;e=a[l];o[e[h]]=e[f];l=l+d;e=a[l];o[e[b]]=e[O];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];n=e[h]o[n](r(o,n+C,e[f]))l=l+d;e=a[l];do return end;break end;break;end break;end while 1957==(n)/((268030/0x46))do n=(591828)while k<=(14756/0x77)do n-= n n=(1353016)while k>(209+-0x56)do n-= n o[e[U]]=o[e[O]][e[B]];break end while 653==(n)/((0x18480/(-115+0xa3)))do local l=e[U];local d=o[e[_]];o[l+1]=d;o[l]=d[e[t]];break end;break;end while 447==(n)/((18536/0xe))do n=(1547355)while(0xc6+-73)>=k do n-= n if(o[e[x]]~=e[P])then l=l+C;else l=e[_];end;break;end while 645==(n)/((4897-0x9c2))do n=(2304977)while k>(0x6cc6/221)do n-= n o[e[h]]=(e[D]~=0);break end while(n)/((362925/0xe1))==1429 do local x;local n;n=e[h];x=o[e[O]];o[n+1]=x;o[n]=x[e[v]];l=l+d;e=a[l];o[e[w]]=e[O];l=l+d;e=a[l];n=e[w]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[U]]=o[e[_]][e[v]];l=l+d;e=a[l];o[e[N]]=o[e[D]][e[B]];l=l+d;e=a[l];n=e[h];x=o[e[f]];o[n+1]=x;o[n]=x[e[P]];l=l+d;e=a[l];o[e[h]]=M[e[i]];l=l+d;e=a[l];o[e[N]]=e[f];l=l+d;e=a[l];o[e[h]]=e[f];l=l+d;e=a[l];o[e[U]]=e[_];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[N]o[n](r(o,n+C,e[_]))l=l+d;e=a[l];o[e[N]]=M[e[_]];l=l+d;e=a[l];o[e[h]]=e[i];l=l+d;e=a[l];n=e[U]o[n](o[n+C])l=l+d;e=a[l];l=e[_];break end;break;end break;end break;end break;end break;end while 3374==(n)/((86700/0x55))do n=(677286)while k<=(0x5fa0/180)do n-= n n=(595534)while k<=(379-0xf8)do n-= n n=(1443904)while k<=(0x489/(-116+0x7d))do n-= n n=(1019081)while((75670/0xeb)-0xc2)<k do n-= n j[e[f]]=o[e[x]];break end while(n)/((-0x7c+(0x70a-939)))==1379 do o[e[U]][e[_]]=e[s];break end;break;end while(n)/((0x28a+-64))==2464 do n=(902054)while(0x5960/176)<k do n-= n local e=e[x]o[e]=o[e]()break end while 1462==(n)/((0x29a+(-0x746/38)))do j[e[c]]=o[e[b]];break end;break;end break;end while 146==(n)/((358952/0x58))do n=(1413984)while(357-0xe0)>=k do n-= n n=(165660)while k>(0x173-239)do n-= n o[e[w]]=o[e[_]]-o[e[B]];break end while 44==(n)/((0x4c4af/83))do local r=y[e[c]];local n;local d={};n=Q({},{__index=function(l,e)local e=d[e];return e[1][e[2]];end,__newindex=function(o,e,l)local e=d[e]e[1][e[2]]=l;end;});for n=1,e[B]do l=l+C;local e=a[l];if e[(-38+0x27)]==15 then d[n-1]={o,e[c]};else d[n-1]={j,e[D]};end;L[#L+1]=d;end;o[e[N]]=m(r,n,M);break end;break;end while(n)/((0x9ec-(-51+0x53f)))==1133 do n=(9135947)while(362-0xe4)>=k do n-= n local h;local n;n=e[x]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];n=e[w];h=o[e[f]];o[n+1]=h;o[n]=h[e[P]];l=l+d;e=a[l];o[e[b]]=M[e[O]];l=l+d;e=a[l];o[e[b]]=e[c];l=l+d;e=a[l];o[e[w]]=e[c];l=l+d;e=a[l];o[e[U]]=e[f];l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[c]))l=l+d;e=a[l];o[e[x]]=(e[i]~=0);l=l+d;e=a[l];o[e[w]]=M[e[O]];l=l+d;e=a[l];o[e[U]]=e[c];break;end while 3491==(n)/((-17+0xa4a))do n=(6350652)while k>(25785/0xbf)do n-= n local d=e[w];local n=o[d+2];local a=o[d]+n;o[d]=a;if(n>0)then if(a<=o[d+1])then l=e[f];o[d+3]=a;end elseif(a>=o[d+1])then l=e[_];o[d+3]=a;end break end while 3654==(n)/((0x5842/13))do local x;local n;o[e[N]]=e[i];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[f]))l=l+d;e=a[l];n=e[h];x=o[e[i]];o[n+1]=x;o[n]=x[e[v]];l=l+d;e=a[l];o[e[w]]=M[e[_]];l=l+d;e=a[l];o[e[N]]=e[c];l=l+d;e=a[l];o[e[U]]=e[c];l=l+d;e=a[l];o[e[h]]=e[f];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[b]o[n]=o[n](r(o,n+d,e[c]))break end;break;end break;end break;end break;end while(n)/((0xd9a+-44))==197 do n=(2706273)while k<=((-0x22+432)-257)do n-= n n=(179550)while(2346/0x11)>=k do n-= n n=(1764294)while(220+-0x53)<k do n-= n M[e[D]]=o[e[h]];break end while(n)/((0x13f9-2614))==706 do local l=e[w]o[l]=o[l](r(o,l+d,e[f]))break end;break;end while 95==(n)/((0x68be6/(0x14c+-105)))do n=(4742808)while(223+-0x54)>=k do n-= n o[e[b]]=(e[c]~=0);break;end while 1554==(n)/((708064/0xe8))do n=(1071240)while(0x36b0/100)<k do n-= n local c;local n;n=e[N]o[n]=o[n](r(o,n+d,e[_]))l=l+d;e=a[l];n=e[N];c=o[e[f]];o[n+1]=c;o[n]=c[e[t]];l=l+d;e=a[l];o[e[b]]=M[e[i]];l=l+d;e=a[l];o[e[x]]=e[i];l=l+d;e=a[l];o[e[h]]=e[_];l=l+d;e=a[l];o[e[b]]=e[f];l=l+d;e=a[l];n=e[U]o[n]=o[n](r(o,n+d,e[D]))l=l+d;e=a[l];o[e[h]]=(e[O]~=0);l=l+d;e=a[l];o[e[w]]=M[e[O]];l=l+d;e=a[l];o[e[h]]=e[D];break end while(n)/((0x408e4/(224-0x92)))==316 do if(o[e[w]]==o[e[B]])then l=l+C;else l=e[D];end;break end;break;end break;end break;end while(n)/((7129-0xe2c))==773 do n=(3124704)while(-33+0xb0)>=k do n-= n n=(2386034)while(-0x77+261)<k do n-= n local a=e[N];local r=e[v];local n=a+2 local a={o[a](o[a+1],o[n])};for e=1,r do o[n+e]=a[e];end;local a=a[1]if a then o[n]=a l=e[O];else l=l+d;end;break end while 917==(n)/((-0x17+2625))do do return o[e[x]]end break end;break;end while(n)/((5899-0xbb3))==1076 do n=(10496651)while k<=(0x4890/(2064/0x10))do n-= n if(o[e[x]]==e[v])then l=l+C;else l=e[D];end;break;end while(n)/((7457-0xea0))==2827 do n=(1469532)while k>(21170/(-0x2d+191))do n-= n local O;local n;n=e[h];O=o[e[c]];o[n+1]=O;o[n]=O[e[t]];l=l+d;e=a[l];o[e[w]]=e[_];l=l+d;e=a[l];n=e[h]o[n]=o[n](r(o,n+d,e[i]))l=l+d;e=a[l];o[e[x]]=o[e[f]][e[B]];l=l+d;e=a[l];o[e[b]]=o[e[c]][e[B]];l=l+d;e=a[l];n=e[w];O=o[e[c]];o[n+1]=O;o[n]=O[e[B]];l=l+d;e=a[l];o[e[w]]=j[e[i]];l=l+d;e=a[l];n=e[N]o[n](r(o,n+C,e[c]))l=l+d;e=a[l];o[e[x]]=M[e[c]];l=l+d;e=a[l];o[e[w]]=e[f];l=l+d;e=a[l];n=e[x]o[n](o[n+C])l=l+d;e=a[l];l=e[f];break end while(n)/((0x1376-2549))==604 do o[e[U]][e[i]]=o[e[u]];break end;break;end break;end break;end break;end break;end break;end break;end l+= C end;end);end;return m(K(),{},R())()end)_msec({[(285+-0x56)]='\115\116'..(function(e)return(e and'(0xfc-152)')or'\114\105'or'\120\58'end)((0x6a-101)==(234/0x27))..'\110g',[(31840/0x28)]='\108\100'..(function(e)return(e and'(-0x5a+(410-0xdc))')or'\101\120'or'\119\111'end)((1010/0xca)==(122+-0x74))..'\112',[(0xd7eb/201)]=(function(e)return(e and'(0x109-165)')and'\98\121'or'\100\120'end)((-0x54+89)==(86+-0x51))..'\116\101',[(-85+0x1b5)]='\99'..(function(e)return(e and'(-0x1c+128)')and'\90\19\157'or'\104\97'end)((-0x6b+112)==(0x1bc/148))..'\114',[(0x6210/48)]='\116\97'..(function(e)return(e and'(0xeb-135)')and'\64\113'or'\98\108'end)((0x2ee/125)==(49+-0x2c))..'\101',[(971-0x20b)]=(function(e)return(e and'(216+-0x74)')or'\115\117'or'\78\107'end)((0x55-82)==(65+-0x22))..'\98',[((192897-0x178eb)/0x76)]='\99\111'..(function(e)return(e and'(324-0xe0)')and'\110\99'or'\110\105\103\97'end)((2418/0x4e)==(165-0x86))..'\97\116',[(0x585-725)]=(function(e,l)return(e and'(0xf3-143)')and'\48\159\158\188\10'or'\109\97'end)((-0x52+87)==(0x1e-24))..'\116\104',[(0xad1-1395)]=(function(l,e)return((1270/0xfe)==(0x76-(5750/0x32))and'\48'..'\195'or l..((not'\20\95\69'and'\90'..'\180'or e)))or'\199\203\95'end),[(1933-0x3f1)]='\105\110'..(function(e,l)return(e and'(24000/0xf0)')and'\90\115\138\115\15'or'\115\101'end)((78-0x49)==(3751/0x79))..'\114\116',[(0x8c7-1176)]='\117\110'..(function(e,l)return(e and'(0x3714/141)')or'\112\97'or'\20\38\154'end)(((0xaf0/70)/8)==((0x8ac/30)+-43))..'\99\107',[(-41+0x49c)]='\115\101'..(function(e)return(e and'((37975/0xaf)-117)')and'\110\112\99\104'or'\108\101'end)(((-0x75+43)+79)==(58+-0x1b))..'\99\116',[(1341+-0x6a)]='\116\111\110'..(function(e,l)return(e and'(234-0x86)')and'\117\109\98'or'\100\97\120\122'end)((111-0x6a)==(855/0xab))..'\101\114'},{[(0x58-59)]=((getfenv))},((getfenv))()) end)()
end)

GamesSection:NewButton("Project Slayers 1", "...", function()
    
loadstring(game:HttpGet("https://raw.githubusercontent.com/noRynx/miningsim/main/projectslayers"))()
end)

GamesSection:NewButton("Project Slayers 2", "...", function()
    repeat wait() until game:IsLoaded()
loadstring(game:HttpGet("https://raw.githubusercontent.com/LioK251/RbScripts/main/lazyhub.lua"))()
end)

local Profile = Window:NewTab("Profile")
local ProfileSection = Profile:NewSection("DisplayName "..game.Players.LocalPlayer.DisplayName)
local ProfileSection = Profile:NewSection("Name "..game.Players.LocalPlayer.Name)
local ProfileSection = Profile:NewSection("You Are Playing on "..game.Name)


local Credits = Window:NewTab("Credits")
local CreditsSection = Credits:NewSection("GUI MADE BY THANATOS")
local CreditsSection = Credits:NewSection("If you have any questions, or")
local CreditsSection = Credits:NewSection("If you have any ideas")
local CreditsSection = Credits:NewSection("What Game,Hub or Options to add")
local CreditsSection = Credits:NewSection("Then please click button below to")
local CreditsSection = Credits:NewSection("Copy My Discord ID And DM me your ideas! Thanks")

CreditsSection:NewButton("Click To Copy Discord ID", "Click To Copy Discord ID", function()
    setclipboard("Chappie#5543")
end)
