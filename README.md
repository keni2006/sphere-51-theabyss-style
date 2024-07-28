[ 26.12.04 day ]

Byte protocols changed to: Walking from 0x02 to 0x04 PickUp from 0x07 to 0x0A Resync from 0x22 to 0x1F
Item Pick UP is hooked, and unnecessary Pick UP spam is removed for all characters nearby.
Animation Dragging removed.
Encryption keys: 0x32850719 0x2D0B700C
Anti Lag system: NPCs with brain type 1 3 5 6 8 have a timer of 3600 seconds All other NPCs have a minimum timer of RANDOM + 2s All other characters have a default timer.
Incognito color is always the same: 0x841A
Removed the [frozen] note when a paralyzed character is sitting in a gz.
One space before the skill result line of Anatomy and Animal Lore.
[ 26.12.04 evening ]

Anti Lag system changed: NPCs with brain type 1 3 5 6 8 have a timer of 3600 seconds All other NPCs have a random timer, but if less than 5s, it is set to 5s. Players have a stable 2s timer.
[ 11.01.05 ]

Encryption and init encryption changed.
[ 16.01.05 ]

Added a percentage display of item integrity like The item is 100% repaired.
Karma or fame received is now displayed in units like You gained 20 fame.
Fixed casts like field on ghosts. Caster doesn't receive karma for the ghost. Wall of stone is placed through the ghost, meaning the ghost no longer blocks the tile.
[ 16.01.05 ]

Aggressors who leave the battle lose 10 fame.
[ 22.01.05 ]

Spells: Arch Protection, Explosion, Mass Curse, Chain Lighting, Mass Dispel, Meteor Swarm, EarthQuake - will only affect objects within the caster's visibility.
Reveal spell has a detection radius of 18 tiles, which corresponds to the character's full visibility radius.
[ 23.01.05 ]

Dirty bandages now have a single type.
[ 29.01.05 ]

Telnet access is strictly from the IPs specified in the ips.txt file. 0 - at the end of the IP indicates the mask of the last number in the form ip.ip.ip.*
[ 3.02.05 ]

Paralysis field target is checked for visibility.
[ 4.02.05 ]

Anti Crash for a corrupted packet 0xB1 - gump selection
[ 7.02.05 ]

Fixed a crash of the sphere when viewing the items of the container in the GM's gump.
Removed character rotation when casting. - Testing for a week ok?
[ 9.02.05 ]

Now you can't summon on fences =)
[ 12.02.05 ]

Finished the unfinished FORCHARS script loop Usage: FORCHARS <radius from object> FRC. - pointer to the character in the enumeration ENDFOR
[ 15.02.05 ]

It's impossible to pass through diagonally open corners
[ 17.02.05 ]

p2p attack doesn't work in the pvp zone
removed pvp flag in multiregion zone
animation set during recollection
corner check removed
[ 19.02.05 ]

Optimization: Characters in logout are not iterated over at every step.
Optimization(a little): The STATF_INDOORS flag check (which sends the weather to the character) is immediately skipped at each step.
[ 20.02.05 ]

Recollection animation improved: The residual animation of the character in the old place after recollection has a black color if the character is EVIL %) Also, after recollection, the animation doesn't stick to the character, but remains in the place of recollection.
[ 21.02.05 ]

Introduced a pin-code system for using items.
The pin code can be activated using a command of the form .<pin-code>
Pin-codes are stored in the pincodes.txt file
File format:
(beginning of file)
(odd line) <pin-code>
(even line) <decimal serial number of item>
Example:
123456789
1073745453
That is, by entering .123456789, the character will use
who entered the pin code, the item 1073745453 (40000E2D),
that is, the DCLICK trigger is further called on this item,
where SRC is the character who entered the pin code
After use, the pin code is removed from the file.

Introduced a new corner check system
