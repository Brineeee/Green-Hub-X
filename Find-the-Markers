local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Brineeee/Kavo-GT/main/lua"))()

local GreenTheme = {
      SchemeColor = Color3.fromRGB(120, 200, 0),
      Background = Color3.fromRGB(0, 0, 0),
      Header = Color3.fromRGB(0, 0, 0),
      TextColor = Color3.fromRGB(255,255,255),
      ElementColor = Color3.fromRGB(0, 0, 0)
} 

local Window = Library.CreateLib("Green X Hub - Find the Marker", GreenTheme)

local Tab1 = Window:NewTab("\\-Home-//")

local Tab1Section = Tab1:NewSection("\\-Farms-//")

Tab1Section:NewButton("Teleport to Random Markers","", function(bool)

		local MarkerTable = {}		for i,v in pairs(game.Workspace:GetChildren()) do

			if string.find(v.Name, "Marker") ~= nil then

				table.insert(MarkerTable, v)

			end

		end

		local e = 0

		for _ in pairs(MarkerTable) do e = e + 1; end

		local ran = math.random(1, e)

		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = MarkerTable[ran]:FindFirstChildWhichIsA("Part").CFrame

	end)

Tab1Section:NewButton("Collect All Markers","", function()

workspace.Gravity = 0

game:GetService('RunService').Stepped:Connect(function()

    if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid') then

       game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)

    end

end)

for k, v in next, workspace:GetDescendants() do

    if v.ClassName == 'TouchTransmitter' and v:FindFirstAncestorOfClass('Model') and v:FindFirstAncestorOfClass('Model').Name:find('Marker') then

        

        for i =  1, 65 do

            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame + Vector3.new(0, -1, 0)

            task.wait(0.1)

            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame + Vector3.new(0, 1, 0)

        end

    end

end

workspace.Gravity = 196

end) 

Tab1Section:NewButton("Stop Collect All Markers","",function()

        game.Players.LocalPlayer.Character:Destroy()

game.Players.LocalPlayer.Character.Script:Destroy()

end) 
