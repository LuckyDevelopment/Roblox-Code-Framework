# Roblox-Code-Framework

Game Framework
I’ve been getting really into organizing my code, and just making it look clean in general. I’ve decided to go for the “1 ServerScript and 1 LocalScript” approach with a modular framework. I’ve looked at frameworks like Knit. But it just didn’t appeal to me to use someones elses, so I’ve tried to come up with my own.

I’ve watched this video here, and it explained really well what I wanted to do. All I want to know now is that, am I doing it correctly?

Here is my framework from 3 years ago,
please don’t cry when looking at it

image

Now I've gotten better over time of course and use module scripts and classes and OOP. This is going to be my new framework for my games.
image

As you see it includes just module scripts. I want to know from you guys if this is a good idea, and if you want to know if I personally like it, I do.

On startup of the game, it loads ALL server modules, and then loads ALL client modules. It also loads them in a way that if one module fails to be required, it waits until all are required fixing any errors of one module loading before another causing it’s code to fail.

Code Structure
Next is my code structure, I’ve gone for a modular approach of course, and maybe some OOP included :wink: . Here is an example client sided ModuleScript under the User folder under the Client LocalScript!

-- [ SERVICES]
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Player = game.Players.LocalPlayer

-- [ MODULE ] --
local TestingClient = {}

-- [ INITIALIZING ] --
function TestingClient.__init()
	print("TestingClient script has been initialized.")
        -- Code here...
end

-- [ RETURNING ] --
return TestingClient
As you see it’s very easy to make new module scripts, and basically have them run at the start of the game. We have comments to seperate sections, and new functions can always be added.

GUI
GUI will be handled in a ModuleScript, it will access the Players UI and then just do… UI stuff like detect when a button was clicked.

Conclusion
Do you guys think this is a good framework and code structure? Will it help keep my code clean and professional? I would like to know the opinion of others.

Downloads
You can download it here, and there is a configuration under the ModuleHandler script.
Download Template: Template.rbxl 1
Download Modular Framework ModuleScript: ModuleScript.rbxm 1
