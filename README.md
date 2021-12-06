# IslandRankup
This is a BentoBox addon to automatically rankup and rankdown the player based on island level.

Original code is by Weaves and bertek41.

## Details
This resource will rankup and rankdown your players automatically when they do the "/island level" command. It will also send a customizable message or broadcast.

First you need to be running BentoBox with a gamemode addon and the level addon. Then you need to add this resource to the addon folder of BentoBox since this is not a plugin but an addon for BentoBox. Then you add your island ranks to the config in place of my examples and configure the start and end levels of each rank making sure they do not overlap. Then add the permission "islandrankup.<rankname>" to each rank. Finally restart and start playing.

Default config:
```
# Enable anonymous metrics data? Please do, it helps us stay motivated.
metrics: true

# Sends a level up message to the player or as a broadcast.
level_up:
  enabled: true
  message: '&7[&3Island Rankup&7] &f<PLAYER>''s new rank is <RANK>'
  broadcast_mode: true

# Should ranks only apply to the world the player is in?
world_specific: false

# You can change these ranks or add to it if you would like, just make sure you follow the format.
ranks:
  dirt:
    start: 0
    end: 14
  grass:
    start: 15
    end: 29
  stone:
    start: 30
    end: 59
  iron:
    start: 60
    end: 124
  gold:
    start: 125
    end: 249
  obsidian:
    start: 250
    end: 499
  diamond:
    start: 500
    end: 999
  emerald:
    start: 1000
    end: 4999
```

Requirements:
* BentoBox
* A BentoBox gamemode addon (i.e.BSkyblock)
* BentoBox Level addon
* Vault
* Vault compatible permissions plugin setup with the ranks you put in the config

Note: The automatic ranking will not work if you are op or have the "*" permission. It won't hurt anything but you will get a message telling you to deop and try again and you may have to manually add/or remove ranks.
