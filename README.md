# exile-vehicle_spawn_with_inventory
Step 1:
  Put the file "ExileServer_world_spawnVehicles.sqf" into your Exile.mission (example Exile.Altis)

Step 2:
  Put the following code into your config.cpp from your mission under the correct class
```  
class CfgExileCustomCode
{
	ExileServer_world_spawnVehicles = "ExileServer_world_spawnVehicles.sqf";
};
```

Step 3:
Insert the following code at the end of your config.cpp from your mission
```
class SpawnVehicleItems{
	/**
	* Vehicles in the world
	*/
	class WorldVehicles{
		/*
		* Allow(1) or disable(0) Items in Spawned vehicles
		* kinda self explanitory
		*/
		vehicleItemsAllowed = 1;
		/*
		* Set the maximum Items per Vehicle to
		* kinda self explanitory
		*/
		maximumItemsPerVehicle = 5;
		/*
		* Array of allowedItems
		* kinda self explanitory
		*/
		allowedItems[] = {
			"Exile_Item_ToiletPaper",
			"Exile_Item_PlasticBottleEmpty",
			"Exile_Item_Can_Empty"
		};
	};
};
```
Step 4:
 Pack your mission into pbo

Step 5:
 Start your Server
