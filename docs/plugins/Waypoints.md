---
icon: lucide/compass
---
# Waypoints
Ever had the problem, that you were on a long trip and don't find your base?

You could set a warp with a conventional plugin at your home and simply teleport back. But if you want to keep the survival experience of not being able to teleport like that, this plugin could be just what your server needs!

## Direction Indicators 
So, instead of just bringing the player back where he started, this plugin shows him the direction he has to walk, so he can explore the world even more. To show the player the direction you can configure multiple direction indicators to guide the player to his destination.

- **Compass** It won't get any simpler than that if the player owns a compass. It will have the waypoint as it's target and points into that direction.

- **Actionbar Indicator** This is comparable to the compass but doesn't require one. It will show the rough direction with small sections in the action bar of the player. If the player is too far left, the sections in the right will light up and vice versa.

- **Beacon** When the waypoint is in render distance, a beacon beam will appear at the location of the waypoint to make it easier to pinpoint the location of the waypoint.

- **Blinking Block** When the player is closer to the waypoint, the beacon will be replaced with a block sequence that will repeat. This is to help him get to the exact location.

- **Hologram** As an alternative to the Blinking Block you can use Holograms to get the exact position of a Waypoint. This feature is optional but requires ProtocolLib if wanted

- **Particles** Particles appear at the feet of the player pointing into the direction of the waypoint

## Player tracking 
Although disabled by default, when enabled adds a menu to the GUI where the player can choose another player to track. Now the compass, actionbar indicator and particles will help guide the player to the tracked player.

- Players can choose to hide themselves in the menu to others (if enabled)
- Players must show themselves to others in order to track a player (if enabled)
- The player that gets tracked receives a notification who started tracking him (if enabled)

## Other notable features 
- Open the GUI by sneaking and right-clicking with a compass (by default)
- Set custom icons for waypoints and folders by clicking on their icon. The item in your main hand will be used
- Limit the amount of waypoints and folders a player can have
- Customizable teleport prices and price increases the more the player teleports (With Vault support)
- Direction indicators customizable
- Items in GUI fully customizable
- Fully translatable
- SQLite data storage

## Integrations 
Public waypoints are added to Dynmap or SquareMap

## Commands 
/waypoints - Opens the GUI
/waypoints set - Create a waypoint only the player himself can see
/waypoints setPublic - Create a waypoint visible for everyone
/waypoints setPermission - Create a waypoint only visible for players with the given permission
/waypoints setTemporary - Create a waypoint that is only visible for the time he is online
/waypoints other <Name|UUID> - View the waypoints of another player
/waypoints statistics - Look at some rudimentary statistics about the database
/waypoints reload - Reload the configuration

### Scripting
/waypointsscript deselectWaypoint - Deselect the current waypoint of a player with a command
/waypointsscript selectWaypoint - Set the waypoint selection of a player with a command
