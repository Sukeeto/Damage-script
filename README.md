--- Damage script ---

(Usage notes at end).

-----------------------------------------

debounce = false
script.Parent.Touched:Connect(function(hit)
	if not debounce then
	
	debounce = true
		
		if hit.Parent:FindFirstChild("Humanoid") then
			hit.Parent:FindFirstChild("Humanoid"):TakeDamage(20)
		end
	
	wait(0.5)
	
	debounce = false
	end
end)

-----------------------------------------

Usage notes:

- It is a Script and not LocalScript.
- The script needs to be in a part, and that part can be placed on models or other Parents in addition to the Workspace.
- You can customize the object the script will be on (Part), size, material, color, name, among others.

Images:

![image](https://user-images.githubusercontent.com/82664951/115094386-b53f5400-9ef3-11eb-843e-7887b39066aa.png) (IMPORTANT!!) In this part you configure the amount of damage that the player will take when contacting the part, in which case he will take 20, but you can put as much as you want.
![image](https://user-images.githubusercontent.com/82664951/115093846-00586780-9ef2-11eb-81f5-207eebae23a8.png) - Script inside the part.
![image](https://user-images.githubusercontent.com/82664951/115093898-1fef9000-9ef2-11eb-8e24-86324f5d602f.png) - Script.
