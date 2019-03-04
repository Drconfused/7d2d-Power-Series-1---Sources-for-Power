Drconfused_Power_Series1

		<!--		Welcome to Drconfuseds madness! 			-->
		<!--	DRCONFUSED POWER SERIES 1 - SOURCES OF POWER	-->
							Version 0.02


					Refinements, upgrades and new sources for:
							Battery Power 
							Generators
							Solar Power
					

Contents 
* 	WHATS IN THE MOD?
*	TO DO/WISH LIST
*	VERSION HISTORY
*	MADNESS NOTES
*	MODDERS NEED TO KNOW BASIS

WHATS IN THE MOD?

		Battery Power Sources	
			-Enhanced Battery Bank 1
				Maxpower increased by 25%
				OutputPerStack increased to X from X
			-Mini Battery Bank
				equips batteries for an early game power option to kick start your science career!	
					-Level 1 science unlocks recipe
				
		-Batteries
			-Junk batteries
				pile of dead batteries
			-battery_small_single
			-Recipe added for car battery
				-Level 2 science unlocks recipe
			
			
		Generator Power Sources
			-Generator Bank Max Fuel 1 = increase max fuel
			-Generator Bank Max Fuel 2 = increased max fuel = 
			-Recipe added for the small engine unlocks at engineering level 3
			
		Solar Power Sources
			-Mini Solar Bank - a 1,1,1 block!
			-Solarbank recipe
			-Enhanced Solarbank
			
		Solar Cells
			Mini solar cells - for the mini solar bank
			Solar cell recipe.
			Super durable solar cell - for the Enhanced solarbank

		Purified Silicone
			Recipe requirement for Solar cells
			
TO DO/WISH LIST

	1. Add a tool engine for the auger and chainsaw to override the smallengine to differentiate it from the vehicle engine. (probably do this in the Power Series 2 for the items that require power series 1. les resources than the small engine. 
	2. Have a craft_area that can be carried like a kit?
	3. Replace the models for the generator maxfuel 1 and 2
	4. get unique models for the generator upgrades.
	5. get unique models for the battery bank upgrades.
	6. add in enhanced fuel
	7. see if there is the capacity to have a moving power source on wheels.(can be modelled as a static object that doesn't move, but I want it to move!)
	8. Fix the offset wire on my models 
		- <property name="WireOffset" value="0,0,0.5" (this could be any value, till I figure out what works)
		-(Jayick) the tag you need to set in Unity, is called Wire. So make a child in unity on your block, call it Wire, and set it to wherever you want it to be. WireOffset, BarrelOffset, SideOffset, all calling in tags from unity
	9. Discover as many of the unity settings that will allow electricity to be an evern more wonderful thing!
			Passive tags?? Jayick what are those?
			BatteryMaxLoadInVolts
			BatteryDischargeTimeInMinutes
	10. Add a on/off indicator light to the mini Battery Bank
			-animation bool trigger ?? (Jayick suggestion)
	11. add an Industrial generator that has a light on it that is on/off indicator and lights the area.
	12. Is there a way to make the degedation value show on the battery in a #?
	
	
VERSION HISTORY
	0.02
		Mini battery was causing a null reference if it was drained and clicked on in the inventory. This was due to having lead as the repair material, but it appears to be not allowed. I have switched it to scrap iron as in my experience more abundant than repair kits. I will seek a better fix for this.
	0.01	
		Battery Bank Upgrades:
			battery bank mini
			batterbank enhanced 
		Generator Bank Upgrades:
			Generator max fuel 1
			Generator max fuel 2
		Batteries
			Small batteries (Like AA)
			Super durable battery
			Car Battery recipe
		Small engine recipe	
		
		

MADNESS NOTES
	hmmmm the conundrums we face when considering balance.
		The different play styles of individuals vary. Some are hardcore vanilla and some are monty haul, many are between, and some none of these defying my categorization.
	Who do I want to appeal to?
		Those who have a similiar play style to me.
			I love building,
			dislike travelling distances, if I must I want to do so quickly and figure out how I can prevent travelling in the future, especially during a zombie apocalypse. HOW can I build a self sustaining base that I don't need to leave?


<!-- Old notes from other files -->
	Oh batteries and their uses!
	Why we don't have AA and AAA's is beyond me, but damn I am getting them in there even if just as junk!
	
	IN the other power mods I changed the numbers of power and such by real numbers rather than by percentages, so I will be doing percentage increases using the battery bank so I can feel what I like best and see if I get feedback.
		ON attempting to place the battery_SuperDurable an overflow acception error was thrown out and the block cannot be interacted with, I think its likely due to the perc_add values.
	
	Want to figure out with a degree of certainty what the different power attributes assigned to the batterybank do
		<property name="MaxPower" value="400"
			self explanatory, this is a hard value of the maximum the unit can output
		<property name="InputPerTick" value="5"/>
			
		<property name="ChargePerInput" value="1"/>
		<property name="OutputPerStack" value="50"/>
		<property name="OutputPerCharge" value="90"/>	
		
	Need to investigate to make sure I can modify FunPimp owned icons or if I need to make my original ones to add them as assets in my mods.
	
	I guess in changing things like the battery, solar cells, engines, instead of making modslots with them I can make them needed with another item to combine in a work area of somet type (forge, workbench, chemstation, etc) to build the new item. The new item can have attachments in the relevant block file to change values of the 'bank' or add values to other things that we want it to affect.
	
	
	
MODDERS NEED TO KNOW BASIS

console commands for mod testing and related values
	exportcurrentconfigs 
		- use this in game in the console to export current configs and the appended changes labled to your user/appdata/roaming/7daystodie folder



