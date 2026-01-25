---
icon: lucide/shield-ban
---
# Simple Claim System

## Player commands

Available commands :

* `/claim [<radius>]`  :  Claim a territory (chunk), with an option to set the radius.
* `/claim main <claim-name>`  :  Open the main gui of a claim.
* `/claim settings [<claim-name>]`  :  Open the settings gui of a claim.
* `/claim members [<claim-name>]`  :  Open the members gui of a claim.
* `/claim chunks [<claim-name>]`  :  Open the chunks gui of a claim.
* `/claim add [<*|claim-name>] <player>`  :  Add a player to your claim, use '\*' for all your claims, use the name of the claim or nothing to use the claim you're standing at.
* `/claim remove [<*|claim-name>] <player>`  :  Remove a player from your claim, use '\*' for all your claims, else the name of the targeted claim.
* `/claim ban [<*|claim-name>] <player>`  :  Ban a player from your claim, use '\*' for all claims, use the name of the claim or nothing to use the claim you're standing at.
* `/claim unban [<*|claim-name>] <player>`  :  Unban a player from your claim, use '\*' for all your claims, use the name of the claim or nothing to use the claim you're standing at.
* `/claim bans [<claim-name>]`  :  Open the bans gui of a claim.
* `/claim kick [<*|claim-name>] <player>`  :  Kick physically a player from your claim, use '\*' for all your claims, use the name of the claim or nothing to use the claim you're standing at.
* `/claim owner [<*|claim-name>] <player>`  :  Transfer the ownership of a claim, use '\*' for all your territories, use the name of the claim or nothing to use the claim you're standing at
* `/claim tp <claim-name>`  :  Teleport to one of your territory.
* `/claim see [<player>]` :  See the chunk you are in with border of particles, if the particles are white, the chunk is free, if it's red the chunk is claimed and if it's green the chunk is yours. If you put a player in argument, it will display all the chunks claimed by this player in purple color.
* `/claim map`  :  Check the claims around you in a chat map.
* `/claim automap`  :  Check automatically the map when you change chunk.
* `/claim autoclaim`  :  Claim automatically the chunk when you change chunk.
* `/claim autounclaim` : Unclaim automatically the chunk when you change chunk.
* `/claim fly`  :  Enable/disable the claim fly.
* `/claim autofly`  :  Enable/disable the claim fly automatically.
* `/claim list`  :  Open the gui with your claims.
* `/claim chat`  :  Change your claim chat mode (public or claim chat).
* `/claim setspawn`  :  Change the location of the claim's spawn.
* `/claim setname <old-claim-name> <new-claim-name>`  :  Change the name of one of your claims.
* `/claim setdesc <claim-name> <new-description>`  :  Change the description of one of your claims
* `/claim merge <claim-name> <claim-name>`  :  Merge two claims into one.
* `/claim addchunk <claim-name>`  :  Add the chunk you're standing at to a claim.
* `/claim delchunk <claim-name> <chunk>`  :  Remove a chunk from a claim. Use this format 'world;x;z'.
* `/claim autoaddchunk <claim-name>` : Add automatically the chunk to the specified claim.
* `/claim autodelchunk <claim-name>` : Remove automatically the chunk from the specified claim.
* `/claims`  :  Open the gui with all the claims of the server.
* `/unclaim [<claim-name|*>]`  :  Delete a claim, with an option to set the name of the target claim, use '\*' for all your claims.
* `/claim sell <claim-name> <price>`  :  Put a claim for sale.
* `/claim cancel <claim-name> <price>`  :  Cancel a claim sale.
* `/claim buy`  :  Buy the claim you're standing at if it's in sale.
* `/claim accept <player>` : Accept the invitation of a player.
* `/claim deny <player>` : Deny the invitation of a player.
* `/claim cancelinv <player>` : Cancel the invitation of a player.