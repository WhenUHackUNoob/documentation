# MagicTP

Ever had problems with old, outdated and unadvanced Random TP plugins in your factions, hardcore, survival and any other server? Don't worry, me too.

MagicTP is designed to have complete user compatibility, with configurable options and in the future ability to change these in-game with a GUI and also change the messages, MagicTP defeats all of those problems the other plugins have.

> # Getting Started

Setting up MagicTP is a super easy process. It is simply just uploading the plugins JAR file, and then restarting your server. When the plugin is first inserted, the plugin will automatically create a configuration file, which may look like the following:

```yml
# [ ----- MagicTP Configuration ----- ]
# Welcome to the MagicTP configuration. There is a small bit of info for every
# configurable setting in this file if you get confused.
# [ ----- MagicTP Configuration ----- ]

coordinates:
  x:
    min: -1000 # The MINIMUM x coordinate the plugin will generate.
    max: 1000 # The MAXIMUM x coordinate the plugin will generate.
  y:
    min: 50 # The MINIMUM y coordinate the plugin will generate.
    max: 125 # The MAXIMUM y coordinate the plugin will generate.
  z:
    min: -1000 # The MINIMUM z coordinate the plugin will generate.
    max: 1000 # The MAXIMUM z coordinate the plugin will generate.

world:
  usecurrent: true # Generate a location in the world the player is CURRENTLY in. If false set world below.
  world: "world" # Name of the world the coordinates should be generated in.

safety:
  check: true # Check that there is no block(s) where the player is going to be teleported. (this should only be used if they can be teleported in air or void)
  block:
    place: true # Place a block below if the location is safe and the player will be teleported (THIS WONT WORK IF SAFETY CHECK IS FALSE)
```

This is great. You may wish to configure this file, which we will get more in-depth into below.

> # Configuring

Configuring the plugin may be complicated, so this page should hopefully solve any issues you have when it comes to this (if not, contact us on <a href="https://discord.whenuhackunoob.com">Discord</a>). Please look below for a sample version of the plugins configuration (Version 1.1).

```yml
# [ ----- MagicTP Configuration ----- ]
# Welcome to the MagicTP configuration. There is a small bit of info for every
# configurable setting in this file if you get confused.
# [ ----- MagicTP Configuration ----- ]

coordinates:
  x:
    min: -1000 # The MINIMUM x coordinate the plugin will generate.
    max: 1000 # The MAXIMUM x coordinate the plugin will generate.
  y:
    min: 50 # The MINIMUM y coordinate the plugin will generate.
    max: 125 # The MAXIMUM y coordinate the plugin will generate.
  z:
    min: -1000 # The MINIMUM z coordinate the plugin will generate.
    max: 1000 # The MAXIMUM z coordinate the plugin will generate.

world:
  usecurrent: true # Generate a location in the world the player is CURRENTLY in. If false set world below.
  world: "world" # Name of the world the coordinates should be generated in.

safety:
  check: true # Check that there is no block(s) where the player is going to be teleported. (this should only be used if they can be teleported in air or void)
  block:
    place: true # Place a block below if the location is safe and the player will be teleported (THIS WONT WORK IF SAFETY CHECK IS FALSE)
```

## Coordinates
### x, y, z
Please specify the minimum and maximum X/Y/Z coordinate here. The plugin will then use these coordinates to generate a random location within your world to teleport the player to. There is currently no way to leave these as none, so please just enter a number for now (this will be brought in a future update). For example, you could have:

```yml
coordinates:
    x:
      min: -54875478
      max: 35948798
    y:
      min: -54875478
      max: 35948798
    z:
      min: -54875478
      max: 35948798
```

For simplicity, I always tend to have the minimum as a negative number.

<b>NOTE: Y coordinate is the HEIGHT. If you only want the player to be RTPed to 1 height level, set the min/max to the same.</b>

## World
### usecurrent
The "usecurrent" option means use the players CURRENT world, instead of using the one provided in the configuration. If this is set to false, you need to provide a world within the "world" option just underneath usecurrent.

```yml
world:
  usecurrent: true # Generate a location in the world the player is CURRENTLY in. If false set world below.
```

### world
This world option is only ever used if the <b>usecurrent</b> option is set to <b>true</b>. This must be set to a valid world within your server, otherwise the console will produce a NullPointerException. If you have <b>usecurrent</b> enabled, you do not need to worry about this setting whatsoever.

```yml
world:
  world: "world" # Name of the world the coordinates should be generated in.
```

## Safety
### check
Enable/disable the safety check. This safety check makes sure that there is no block, player, entity etc around them depending on which mode you use. You should never really disable this, unless you want the player to be able to randomly teleport to already built/claimed/etc structures and whatever else your server may have.

```yml
safety:
  check: true # Check that there is no block(s) where the player is going to be teleported. (this should only be used if they can be teleported in air or void)
```

<b>NOTE: If this is disabled, the setting below (block) will also be disabled. No block will be placed beneath the player.</b>

### block
#### place
Enable/disable if a block should be placed below the player when they RTP and the safety check is enabled. If disabled, it will still check for safety however no block will be placed beneath them.


```yml
safety:
  block:
    place: true # Place a block below if the location is safe and the player will be teleported (THIS WONT WORK IF SAFETY CHECK IS FALSE)
```

> # All done!
You have now configured MagicTP! Make sure to stay up-to-date with this documentation, since any new configurative options will be explained here upon their release. Thank you for referring to this documentation!