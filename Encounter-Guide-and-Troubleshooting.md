This guide provides some insight into how encounters spawns using the Modular Encounters Spawner. This can be used to understand when you will see NPC grids in your game world.


# What Mods and Settings do you need?

Because the spawner is a Mod, you will need to ensure that Experimental Mode is enabled. This is done from the options menu accessed from the title screen.  

The first mod you will need is the **Modular Encounters Spawner**, which is responsible for spawning encounters in your game world. However, most encounter mods that use the features of the Spawner will often list it as a mod dependency in Steam - which allows Space Engineers to Automatically load it when selecting said encounter mods.  

Loading the Spawner mod by itself will not add any new encounters to your game. The Spawner is a framework mod that other encounter mods use to spawn their NPCs. I maintain a Steam Collection of mods that are friendly with MES, even if they do not directly use its features. That list can be found [at this link](https://steamcommunity.com/sharedfiles/filedetails/?id=1991339991). Please note this isn't an exhaustive list, so there are other encounter mods on the workshop that should also be compatible.

For world settings, you may want to enable **In-Game Scripts** and **Enable Drones**. In-game Scripts is what many mods still use for NPC Grid AI, and Enable Drones is the system a lot of mods use to call reinforcements (this is done via 'Pirate Antennas').  

The world options for **Cargo Ships** and **Random Encounters** will be automatically turned off when using the Modular Encounters Spawner. The reason these world options are disabled is because the Spawner implements its own scripting for these features (effectively replacing them), so having them enabled would likely cause conflicts. If you are using older encounter mods that say they need those world options enabled, don't worry - the spawner is built to be backwards compatible with them!   
  
# What Types of Encounters Exist?  

There are a handful of ways that encounters can spawn using Modular Encounters Spawner. Here are some of the different types and how they are triggered:   

* **Space Cargo Ship:** These encounters will spawn in space, or while the player is in a shallow gravity field (such as a moon). They typically appear about 5-10 KM from a player and will travel in a linear path for about 10-15 KM before despawning. These spawning events typically occur on a random timer, which is usually about 20-30 minutes.  

* **Random Encounters:** These encounters also appear while you are in space. They will not appear if you are in a gravity well of any kind. They will appear in a random position near a player, about 7-15 KM away. Random Encounter spawns are triggered when the player is exploring space, which means you need to travel a certain distance before they will appear (about 15 KM). There is also a cooldown per player after a spawn is triggered - this is to prevent a player from using their jump drive rapidly to generate new spawns, which can affect game performance if too many grids exist in the world at once.  

* **Planetary Cargo Ships:** These are very similar to their space counterparts, but will spawn typically in planets with a rich atmosphere.  

* **Planetary Installations:** These are similar to Random Encounters in Space, but will spawn as static grids on planets that have a lot of flat surfaces. Players will need to travel about 6 KM before a spawn event is triggered.  

* **Boss Encounters:** These encounters can appear in both Space and on Planets. They initially appear as a purple colored GPS marker, usually accompanied by a message that is broadcast to near-by player using the in-game chat system. The encounter will not physically spawn into the world until a player approaches the GPS signal (getting within about 300m of the signal). These signals will appear on a timer (approx 20min, and will remain visible for about another 20min). You should not approach one of these encounters unless you are well armed and ready for a difficult encounter.  

# Troubleshooting Encounters and Other Issues

Here are some of the most common reasons you may not see encounters when you expect to, or why some encounters might not work properly:  

* **Dedicated Server and Selective Physics Updates:** If you decide to use the Selective Physics Updates option introduced in game version 1.196, you must use a `SyncDistance` no lower than `10000`. If the SyncDistance is lower, then the Modular Encounters Spawner (and RivalAI) will be disabled. The reason for this harsh requirement is because most NPC grids operate outside of the default SyncDistance of 3000, and this server option stops their movement (physics) unless a player is within the SyncDistance range. There is no reasonable way to work around this other than increasing the SyncDistance.  

* **Check What Can Spawn In Your Vicinity:** You can use a simple chat command to see what encounters are potentially eligible to spawm near you. The command is `/MES.GetEligibleSpawnsAtPosition`. There is also a shorthand version of this command as well: `/MES.GESAP`. Depending on where you are and what mods you have loaded, it could just be an issue on being in an area where those mods cannot spawn encounters.

* **Too Many Spawns:** If you are playing in multiplayer, you may notice an increase in spawn activity. This is because each player is tied to their own spawning events. So if a bunch of players are all in one area, then a bunch of encounters can potentailly appear pretty quickly. To mitigate this, use the config to reduce the `MaxShipsPerArea` property of each encounter type to something that is more managable for your play style. The config files also control the time between spawns as well.  

 * **Planetary Spawning:** *Planetary Cargo Ships* will typically only spawn on full sized planets that have a rich atmosphere. If you are using a custom map with modded planets or planets that are too small in size, then the atmosphere required for spawning may not be enough and any spawn attempt will fail. For *Planetary Installations*, planets that have a rough surface will have less success in seeing installations appear - this is because the mod tries to find relatively flat areas to spawn these installations, so jagged and mountainous areas will likely not see many/any of these spawns.  

 * **Planetary Cargo Ships Falling Out Of The Sky:** This is almost always the result of other mods that cause changes to Thurster Balance, Fuel and Hydrogen Re-Balance, and Aerodynamic/Realistic thrust. Many planetary cargo ships are not designed to use these systems and may not work properly as a result.
 
 * **Critical Error In-Game Popup:** These errors are often not a result of something wrong with the mod itself, but rather a result of Steam not downloading the mod properly. This can often be corrected by unsubscribing from the mod in question, waiting a little while, restarting steam, and then re-subscribing to the mod to force a new download.  
 
 * **Encounter Specific Limitations:** Some mods may use additional requirements that must be met before their encounters are able to spawn. These often include conditions such as Threat Score, PCU, Faction Reputation, and other conditions. These conditions are often listed on the mod pages of those encounters, so ensure you read the mod descriptions so that you understand the required conditions for their encounters.  
 
 * **Ships/Drones Not Doing Anything:** This is often because the drone encounters of a mod require the In-Game Scripts World Option to be enabled. When creating a new world, this option is typically OFF by default, so ensure you double check this to ensure it's ON.  
 
 * **Too Many Active Encounters:** If encounters are not spawning, it may be because there are too many active encounters in the world. Try removing some grids using the Admin Tools (Alt+F10).  
 
 * **Current Game Version:** I will often update the Modular Encounters Spawner with new features as they are released with Base Game Major Updates. As a result, the Spawner is only compatible with the latest version of Space Engineers. If you attempt to run it in older versions, the scripts the spawner uses to operate may not compile.  
 
 * **Drones Spawning From Antennas:** These are not spawned through the Modular Encounters Spawner, so they may have other factors that need to be considered such as the **Enable Drones** world option being turned on, and the **Pirate PCU** limit not being exceeded. Also, because these are not spawned through the Spawner mod, they will not be eligible for prefab manipulations provided by `NPC Weapon Upgrades` or `NPC Defense Shield Provider` mods.

* **Torch Concealment:** Concealment Plugin for Torch has been known to cause issues with NPC grids on occasion. I am not familiar with the various settings that the plugin offers (I have not administrated a server in a very long time), but I believe there are options to exclude NPC grids from concealment. I recommend using that option if you run into conflict with the Modular Encounters mods. If issues persist, you may need to disable concealment to use this mod.

* **Circular Reference in Game Log:** This message can appear sometimes in your game log. It's something that often appears when mods use another mod as a dependency (many encounter mods use the spawner). The message is harmless and can be ignored.

* **Still Seeing Spawns After Removing The Spawner:** If you have removed the Modular Encounters Spawner mod, but have left any mods that use it as a dependency, then it is likely those mods are causing it to continue loading. You would need to remove any mod using the spawner as a dependency from your mod list.