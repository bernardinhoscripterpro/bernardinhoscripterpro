getgenv().Leg = "Right" -- Left or Right
getgenv().Reach = 3.34 -- Change to whatever you want (The game caps it)

game["RunService"].Stepped:Connect(function()
	if Leg == "Left" and game:GetService("Players").LocalPlayer.Character ~= nil and game:GetService("Players").LocalPlayer.Character.Humanoid.RigType == Enum.HumanoidRigType.R15 then
		if (workspace.TPSSystem.TPS.Position - game.Players.LocalPlayer.Character:WaitForChild("LeftLowerLeg").Position).Magnitude <= Reach then
			firetouchinterest(workspace.TPSSystem.TPS, game.Players.LocalPlayer.Character:WaitForChild("LeftLowerLeg"), 0)
			firetouchinterest(workspace.TPSSystem.TPS, game.Players.LocalPlayer.Character:WaitForChild("LeftLowerLeg"), 1)
		end
	end
	if Leg == "Right" and game:GetService("Players").LocalPlayer.Character ~= nil and game:GetService("Players").LocalPlayer.Character.Humanoid.RigType == Enum.HumanoidRigType.R15 then
		if (workspace.TPSSystem.TPS.Position - game.Players.LocalPlayer.Character:WaitForChild("RightLowerLeg").Position).Magnitude <= Reach then
			firetouchinterest(workspace.TPSSystem.TPS, game.Players.LocalPlayer.Character:WaitForChild("RightLowerLeg"), 0)
			firetouchinterest(workspace.TPSSystem.TPS, game.Players.LocalPlayer.Character:WaitForChild("RightLowerLeg"), 1)
		end
	end
	if Leg == "Right" and game:GetService("Players").LocalPlayer.Character ~= nil and game:GetService("Players").LocalPlayer.Character.Humanoid.RigType == Enum.HumanoidRigType.R6 then
		if (workspace.TPSSystem.TPS.Position - game.Players.LocalPlayer.Character:WaitForChild("Right Leg").Position).Magnitude <= Reach then
			firetouchinterest(workspace.TPSSystem.TPS, game.Players.LocalPlayer.Character:WaitForChild("Right Leg"), 0)
			firetouchinterest(workspace.TPSSystem.TPS, game.Players.LocalPlayer.Character:WaitForChild("Right Leg"), 1)
		end
	end
	if Leg == "Left" and game:GetService("Players").LocalPlayer.Character ~= nil and game:GetService("Players").LocalPlayer.Character.Humanoid.RigType == Enum.HumanoidRigType.R6 then
		if (workspace.TPSSystem.TPS.Position - game.Players.LocalPlayer.Character:WaitForChild("Left Leg").Position).Magnitude <= Reach then
			firetouchinterest(workspace.TPSSystem.TPS, game.Players.LocalPlayer.Character:WaitForChild("Left Leg"), 0)
			firetouchinterest(workspace.TPSSystem.TPS, game.Players.LocalPlayer.Character:WaitForChild("Left Leg"), 1)
		end
	end
end)
