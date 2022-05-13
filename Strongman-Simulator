local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Brineeee/Kavo-GT/main/lua"))()

local GreenTheme = {
      SchemeColor = Color3.fromRGB(120, 200, 0),
      Background = Color3.fromRGB(0, 0, 0),
      Header = Color3.fromRGB(0, 0, 0),
      TextColor = Color3.fromRGB(255,255,255),
      ElementColor = Color3.fromRGB(0, 0, 0)
} 

local Window = Library.CreateLib("Green X Hub - Strongman Simulator", GreenTheme)

local Tab1 = Window:NewTab("\\-Home-//")

local Tab1Section = Tab1:NewSection("\\-Farms [Auto]-//")

local Tab2 = Window:NewTab("\\-Player-//")

local Tab2Section = Tab2:NewSection("\\-Players [ PYSHIC - epik ]-//")

Tab1Section:NewButton("{ Auto Squads } - [ You must be in squads ]","", function(bool)

while true do 

local Event = game:GetService("ReplicatedStorage")["StrongMan_UpgradeStrength"]

Event:InvokeServer()

wait(0)

end

end)

Tab1Section:NewButton("{ Auto Farm } - [ DO NOT CLICK AGAIN ]", "", function()

    while true do

         FarmHydra()

         wait(0)

         end

end)

Tab1Section:NewButton("{ Stop Auto Farm } - [ Here xD ] ", "", function() 

   game:GetService("TeleportService"):Teleport(game.PlaceId)

    game.Players.LocalPlayer.Character:Destroy()

game.Players.LocalPlayer.Character.Script:Destroy()

    end) 

function FarmHydra()

       --clear

 

 -- Local Player

 local Plr = game:GetService("Players").LocalPlayer

 local Char = Plr.Character

 local RootPart = Char.HumanoidRootPart

 local LowerTorso = Char.LowerTorso

 

 -- Game Stuff

--   local Loader = game:GetService("Workspace").BadgeColliders.FarmBadge

 local Hydra_Item = game:GetService("Workspace").Areas["Area18_Apartment"].DraggableItems:FindFirstChildOfClass("MeshPart")

 

 if Hydra_Item == nil then

     -- We need to load part of the map in.

     RootPart.CFrame = CFrame.new(248, 35, 12109, 1, 0, 0, 0, 1, 0, 0, 0, 1)

     return true;

 end

 

 local Hydra = Hydra_Item:WaitForChild("InteractionPoint")

 local Proximity = Hydra:FindFirstChild("ProximityPrompt")

 

 RootPart.CFrame = Hydra.CFrame

 wait(0.1)

 Proximity:InputHoldBegin()

 Proximity:InputHoldEnd()

 

 -- Teleport us to the finish (I have some nasty hard coded stuff in here.)

 repeat

  for i,v in pairs(game:GetService("Workspace").PlayerDraggables[game.Players.LocalPlayer.UserId]:GetChildren()) do

      v.Anchored = true

      v.CFrame = game:GetService("Workspace").Areas["Area18_Apartment"].Goal.CFrame

      wait()

      v.Anchored = false

  end

  wait()

until #game:GetService("Workspace").PlayerDraggables[game.Players.LocalPlayer.UserId]:GetChildren() < 1

 

end 

Tab2Section:NewButton("Remove Doors","", function()

    for i,v in pairs(game:GetService("Workspace").Areas:GetDescendants()) do

        if string.find(v.Name,"Exit") then

            v:Destroy()

        end

    end

end)

Tab2Section:NewButton("Be Smaller","", function()

    while wait() do

        pcall(function()

            for i,v in pairs(game:GetService("Workspace")[game.Players.LocalPlayer.Name].Humanoid:GetChildren()) do

                if v.ClassName == "NumberValue" then

                    v.Value = 0.5

                end

            end

        end)

    end

end) 
