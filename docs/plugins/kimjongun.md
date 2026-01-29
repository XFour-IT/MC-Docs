---
icon: lucide/rocket
---
# Kim Jong Un
- A special Kim Jong Un 3 mob can spawn randomly in the world.
- When defeated, it drops **one random part** (missile part or launchpad part).
- It can also drop an **ICBM Core** for crafting strategic missiles.
- Collect the parts to craft an **Assembled Missile** and **Assembled Launchpad**.

## Crafting the Parts
Use any crafting grid (shapeless):
- **Assembled Missile** = missile nose + missile body + missile engine
- **Assembled Launchpad** = launchpad base + launchpad control + launchpad support
- **Assembled ICBM** = assembled missile + ICBM core

## Launching a Missile
1. Hold the **Assembled Launchpad** and right-click a block to place it.
2. Hold the **Assembled Missile** and right-click the launchpad to trigger the standard thermonuclear launch.

## Launching an ICBM
1. Hold the **Assembled Launchpad** and right-click a block to place it.
2. Hold the **Assembled ICBM** and right-click the launchpad.
3. Use the **ICBM Targeting** GUI to set X/Y/Z coordinates:
   - Left click to add +1, right click to subtract -1, and shift-click for +/-10.
   - Click **Use Current Location** to auto-fill your current coordinates.
4. Click **Launch ICBM** to send it to the target.
5. Enjoy the dramatic launch sequence, mushroom cloud, and fallout.

## Radiation Suit
Craft a full radiation suit to protect yourself from fallout.
Use glowstone dust with leather armor pieces in the crafting grid to make:
- **Radiation Suit Helmet**
- **Radiation Suit Chestplate**
- **Radiation Suit Leggings**
- **Radiation Suit Boots**

## Tips
- Launchpads and missiles use Nova-managed item visuals.
- You need the `kimjongun3.use` permission to place and launch.


## Kim Jong Un (Version 1)
!!! warning
    This documentation is for version 1 of the Kim Jong Un mod. This version is no longer installed on the server. 
    
This mod adds Kim Jong Un. He spawns randomly. When killed he may drop one of four [missile parts](#crafting-recipe). 

### Commands
- `/spawnkim` — Spawn the themed mob near you.

### Permissions
- `kimjongunmob.spawn` (default: op)

### Crafting Recipe
```
 N 
BWB
 F 
```
- **N** = Thermonuclear Nose Cone  
- **B** = Thermonuclear Missile Body  
- **W** = Thermonuclear Warhead Core  
- **F** = Thermonuclear Missile Fins  

### Usage
1. Defeat the themed mob to collect all four missile parts.
2. Craft the **Thermonuclear Missile** using the recipe above.
3. Right-click a block that is receiving redstone power to launch the missile.

### Notes
- The missile launches upward and detonates after a short fuse.