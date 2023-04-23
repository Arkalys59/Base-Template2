<br />
<div align="center">
  <a href="https://github.com/WirzRexTon/Base-Template"> </a>
  <h3 align="center">Template ESX Legacy 1.9.4</h3>

  <p align="center">
    A template to start your server !
    <br />
    <a href="https://discord.gg/v8nrrJd4Zw">Discord RexTon</a>
    ·
    <a href="https://discord.com/invite/RPX2GssV6r">ESX Discord</a>
    ·
    <a href="https://documentation.esx-framework.org/">ESX Documentation</a>
  </p>
</div>

## About The Project

This Template is intended to help you in the beginning of your base with the most recent resources possible. The extended has the double job, which was added by me. 
For any installation problem, or bug. Please go to RexTon's discord (https://discord.gg/v8nrrJd4Zw), I will answer you with pleasure, of course only if you are polite. 

## Getting Started

### Installation : 

1. You must have an artifact greater than or equal to `6116` ! (https://runtime.fivem.net/artifacts/fivem/)
2. Import the sql into your database. 
3. Update the information about your database in the server.cfg
   ```sh
    set mysql_connection_string "mysql://USER:PASSWORD@DATABASEIP/DATABASENAME?waitForConnections=true&charset=utf8mb4"
    or 
    set mysql_connection_string "server=DATABASEIP;database=DATABASENAME;userid=USER;password=PASSWORD"
   ```
4. Launch your server and enjoy. 

### Disclaimer

esx_society is not compatible with job2. You can do it if you want. (Or contact me, it depends if you are nice or not $) 

_Of course, you can modify the elements as you wish. Except es_extended which could create problems._

### Example of how to add food in ox_inventory for esx_status. 

1. Go to [ox]/ox_inventory/data/items.lua
2. To add an item, here is the example for the hunger and the thirst
  ```sh
  ['burger'] = {
		label = 'Burger',
		weight = 220,
		client = {
			status = { hunger = 200000 },
			anim = 'eating',
			prop = 'burger',
			label = "Vous mangez un Hamburger",
			usetime = 2500,
			notification = 'Tu as mangé un délicieux burger !',
			export = 'ox_inventory.hunger',
		},
	},

	['water'] = {
		label = 'Water',
		weight = 500,
		client = {
			status = { thirst = 200000 },
			anim = { dict = 'mp_player_intdrink', clip = 'loop_bottle' },
			prop = { model = `prop_ld_flow_bottle`, pos = vec3(0.03, 0.03, 0.02), rot = vec3(0.0, 0.0, -1.5) },
			label = "Vous buvez de l'eau",
			usetime = 2500,
			cancel = true,
			notification = 'You drank some refreshing water',
			export = 'ox_inventory.thirst',
		}
	},
  ```
3. You can change the value of the food it adds to your food or thirst bar. 
 ```sh 
  	status = { thirst = 200000 },
        or 
        status = { hunger = 200000 },
 ```
4. Just restart ox_inventory and try! 


## Contact

WirzRexton - (https://discord.gg/v8nrrJd4Zw) 
My roleplay project (French) - (https://discord.gg/stateofsanandreas)
