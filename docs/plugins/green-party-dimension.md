# Green Party Dimension Plugin

A ridiculously themed Minecraft plugin that creates a custom dimension dedicated to the UK Green Party in over-the-top fashion. Players can be kidnapped into the dimension, complete eco-friendly quests, participate in council debates, and manage their environmental impact.

**Version:** 1.3.0  
**Server:** Paper 1.21.1 with Geyser support  
**Author:** Jeeves

## Installation

1. Download `GreenPartyDimension-1.3.0.jar`
2. Place in `plugins/` directory
3. Restart server
4. Edit `plugins/GreenPartyDimension/config.yml` as needed
5. Run `/greenparty reload` to apply changes

## Quick Start

### Entering the Dimension

Build a portal frame using **leaves, logs, or moss blocks**, then right-click with a **composter** in hand.

### Commands

#### General
- `/greenparty info` — Plugin info and status
- `/greenparty leave` — Exit dimension (unless kidnapped)
- `/greenparty reload` — Reload config

#### Player Commands
- `/quest list` — Show available quest chains
- `/quest start <chain_name>` — Begin a quest
- `/quest progress` — View current step
- `/quest abandon` — Abandon current quest
- `/greencredit balance` — Check Green Credits
- `/achievements` — View earned achievements
- `/npc info <name>` — NPC location and schedule
- `/debate vote <name>` — Vote in a debate
- `/violations` — Check your violations

#### Admin Commands
- `/greenparty release <player>` — Release a kidnapped player
- `/greencredit give <player> <amount>` — Award Green Credits
- `/violations <player>` — Check another player's violations

## Features

### Kidnap Mechanic

Certain players are marked as "conscription targets" in `config.yml`. When they join:
1. They experience a 5-second kidnap sequence (blindness, sound effects, dramatic message)
2. They are teleported to The Verdant Utopia (Green Party dimension)
3. **Cannot leave via `/greenparty leave`** — they're permanently conscripted
4. On respawn, they return to the dimension automatically

Admins can release players with `/greenparty release <player>`.

### Eco-Score System

Every action in the dimension affects your eco-score:
- **+5** Planting saplings
- **+3** Placing composters
- **+2** Breaking leaves
- **-10** Mining coal
- **-5** Destroying other nature blocks (logs, grass, etc.)

Your score displays in the action bar every 10 seconds with ratings (Verdant Champion → Planet Destroyer).

### Green Credits Currency

Earn Green Credits (GC) by:
- Completing quest steps: **+5-30 GC**
- Quest chain completion: **+30 GC bonus**
- Council participation: **+2 GC per vote**
- Debate wins: **+20 GC**
- Recycling items: **+5 GC**

Spend credits on:
- Environmental violation fines: **-10 GC**
- Debate losses: **-5 GC**
- Future custom items (coming soon)

Check balance with `/greencredit balance`.

### Environmental Violations

Breaking eco-unfriendly blocks (coal ore, logs, leaves) triggers violations:
- **Fine:** 10 Green Credits per violation
- **Insufficient credits?** You're exiled back to spawn
- **View violations:** `/violations`
- **Resets weekly** (configurable)

### Quest Chains

Six multi-step quest chains available:

1. **Petition the Council** — Gather signatures and present to councillors (3 steps)
2. **Composting Revolution** — Place composters and learn decomposition (3 steps)
3. **Clean Energy Champion** — Plant trees and advocate for renewable energy (3 steps)
4. **Eco Enforcer** — Track down eco-violators and report them (3 steps)
5. **Manifesto Rewrite** — Collect feedback and revise Green Party policy (3 steps)
6. **Carbon Neutral** — Achieve net-zero emissions through offsetting (3 steps)

Each step rewards Green Credits, eco-score boosts, and custom items. Completing all steps grants a +30 GC bonus and dimension-wide recognition.

### Recycling System

Recycling bins (♻️ Recycling Bin) are scattered throughout the dimension:
- **Throw items** near a bin to recycle them
- **Receive random "recycled" items:**
  - Common: Random dyes
  - Uncommon: Random seeds
  - Rare: Random minerals
  - Very rare: Custom items (Manifestos, Badges, Spoons)
- **Award:** 5 Green Credits + particles + sound
- **Tracks** toward "Green Tycoon" achievement

### Voting & Motions

Only councillors can propose motions, but all players can vote:

- `/motion start <title>` — Propose a motion (councillors only)
- `/motion vote <yes|no>` — Cast your vote
- `/motion results` — See vote count and percentage

**Vote outcomes trigger dimension effects:**
- "Ban all dark blocks" → Darkness potion (30s)
- "Mandatory tree planting" → Saplings spawn around players
- "Compost festival" → Particle rain
- And more...

Voting awards **2 Green Credits** and counts toward the "Dedicated Attendee" achievement.

### Dynamic Announcements

Every 5-10 minutes, the Green Council broadcasts absurd announcements:
- "EMERGENCY: Compost shortage detected!"
- "Motion passed: All players must plant a tree"
- "The council is convening. Attend immediately!"
- ...and 17 more

Announcements include title displays, sound, and light shows (fireworks + particles at councillor locations).

### NPC Schedules & Movement

All 13 councillors move around the dimension throughout the day:
- **Council Chamber** (spawn area)
- **Compost Processing**
- **Tree Farm**
- **Recycling Centre**

Each NPC has their own schedule. Use `/npc info <name>` to see their location and daily routine.

### Councillor Debates

Every 30 minutes, two random councillors debate absurd Green Party policies near spawn:
- **Announcement:** 2 minutes before with title card
- **Debate duration:** Full dialogue tree (~1-2 minutes)
- **Other NPCs gather** to watch
- **Players vote:** `/debate vote <name>`
- **Rewards:** Winner +20 GC, loser -5 GC
- **7 unique debate topics** with ridiculous arguments

### Heckler Mechanic

NPCs react to player actions in real-time:

**Insults (for breaking bad blocks):**
- "That's not very green of you!"
- "The council disapproves!"
- "MOTION: Ban this player immediately!"
- (10+ variants, more frequent for repeat offenders)

**Praise (for planting trees/composters):**
- "Excellent work for the planet!"
- "The council applauds your efforts!"
- "You're a true Green warrior!"
- (10+ variants)

30-second cooldown per player prevents spam.

### Custom Items

Three custom items can be obtained:

1. **Green Party Manifesto** — WrittenBook with 8 pages of absurd policy (craftable: paper + ink sac)
2. **Green Party Badge** — Glowing diamond with serial number
3. **Compost Ceremonial Spoon** — Wooden shovel with Efficiency III + Unbreaking V + Silk Touch

### Achievements

Four achievements to unlock:

1. **Involuntary Membership** — Get kidnapped 5 times
2. **Arboreal Champion** — Plant 100 saplings
3. **Green Tycoon** — Earn 1000 Green Credits
4. **Dedicated Attendee** — Attend 10 council meetings (vote in debates)

View progress with `/achievements`.

## Configuration

Edit `plugins/GreenPartyDimension/config.yml` to customize:

### Kidnap Targets
```yaml
kidnap-targets:
  - "DanBrad098"
  - "yupBenji"
```

### Eco-Score Multipliers
```yaml
eco-score:
  sapling-planting: 5
  composter-placement: 3
  leaf-breaking: 2
  coal-mining: -10
  nature-block-destruction: -5
```

### Environmental Violations
```yaml
violations:
  fine-amount: 10
  reset-days: 7
```

### Recycling Drop Table (weighted)
```yaml
recycling:
  drops:
    - item: "dye"
      chance: 40
    - item: "seed"
      chance: 30
    - item: "mineral"
      chance: 20
    - item: "custom"
      chance: 10
```

### Announcements
```yaml
announcements:
  interval-min: 300  # ticks (5 min)
  interval-max: 600  # ticks (10 min)
  messages:
    - "EMERGENCY: Compost shortage detected!"
    - "Motion passed: All players must plant a tree"
    - "The council is convening. Attend immediately!"
    # ... more
```

### Heckler System
```yaml
heckler:
  enabled: true
  cooldown-seconds: 30
  insults:
    - "That's not very green of you!"
    - "The council disapproves!"
    # ... more
  praise:
    - "Excellent work for the planet!"
    - "The council applauds your efforts!"
    # ... more
```

## Permissions

- `greenparty.council` — Can propose motions (default: op)
- `greenparty.violations.check` — Can check others' violations (default: op)
- `greenparty.admin` — Admin commands like `/release` and `/greencredit give` (default: op)

## Troubleshooting

### Players can't enter the dimension
- Ensure portal frame is built correctly (leaves/logs/moss blocks in a frame shape)
- Ensure player has a composter in hand
- Check dimension has been initialized (check server logs)

### Kidnapped players can still leave
- Ensure player name is in `kidnap-targets` in config
- Run `/greenparty reload` after config changes
- Check `/greenparty info` to verify kidnap list is loaded

### NPCs not moving
- Check `NPCScheduleManager` is enabled in config
- Verify in-game day cycle is running (time is advancing)
- Check server logs for errors

### No announcements appearing
- Check `announcements.enabled` is `true`
- Verify players are in the Green Party dimension
- Increase `interval-min` and `interval-max` if announcements feel rare

## Support

For issues, questions, or suggestions, contact the server admins or check `/greenparty info` for plugin version and status.

---

**Last Updated:** 2026-03-26  
**Plugin Version:** 1.3.0  
**Phases Complete:** 1, 2, 3
