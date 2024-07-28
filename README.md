General:

Byte protocols changed.
Item Pick UP hooked, and unnecessary spam removed for nearby characters.
Animation Dragging removed.
Encryption keys set.
Anti-Lag system implemented.
Incognito color is standardized.
[frozen] note removed for paralyzed characters in a guarded zone.
One space added before skill result line of Anatomy and Animal Lore.
Anti-Lag System Changes:

Anti-Lag system adjusted:
NPCs with specific brain types have a fixed timer.
Other NPCs have a random timer with a minimum of 5 seconds.
Players have a consistent 2-second timer.
Encryption:

Encryption and init encryption updated.
Item Integrity:

Added a percentage display for item integrity.
Karma/Fame Display:

Karma or fame received is now displayed in units.
Ghost Interactions:

Fixed field casts on ghosts.
Caster does not receive karma for ghost hits.
Wall of stone now passes through ghosts.
Aggression Penalty:

Aggressors leaving battle lose fame.
Spell Visibility:

Spells now only affect objects within the caster's visibility.
Reveal spell has a radius of 18 tiles.
Bandages:

Dirty bandages unified to one type.
Telnet Access:

Telnet access restricted to specified IPs in ips.txt file.
Paralysis Field:

Paralysis field target is checked for visibility.
Crash Prevention:

Anti-Crash measure implemented for corrupted packet 0xB1.
GM Gump:

Fixed a sphere crash when viewing container items in the GM's gump.
Casting Rotation:

Character rotation during casting removed (tested for a week).
Summoning:

Summoning on fences disabled.
FORCHARS Script:

FORCHARS script loop completed.
Corner Movement:

Prevented movement through diagonally open corners.
PVP Zones:

p2p attack disabled in PvP zones.
PVP flag removed in multiregion zones.
Recollection animation added.
Optimization:

Optimization improvements:
Characters in logout are not processed at every step.
STATF_INDOORS flag check skipped during each step.
Recollection Animation:

Recollection animation improved:
Black color for characters in the old location if they are evil.
Animation stays in the place of recollection.
Pin-Code System:

Introduced a pin-code system for item usage.
New Magic:

New magic implemented: Astral Projection.
Uses a book-like item 0x2253.
Cast only on a marked rune.
Uses 100 mana, and cannot be cast while mounted.
Character enters a new Wisp body, invisible and dead.
Wimp is invisible starting with 80 necromancer skill.
Astral movement restricted to GM necromancers.
Return to native body via warp module or attack on native body.
5 mana spent every second while in astral if necromancy is not GM.
Return during world save or client disconnect.
No speaking while in astral.
Native character in astral has the [Astral] note.
Information about the magic is added to the game lore.
Stamina Check:

Prevented entering a tile with another character if stamina is lower than dexterity.
World Save Timer:

World save timer reset to 0 if it's over 100 days.
Kill timer no longer resets to 1/10th during log in.
"Murderer!" message appears with the first kill.
FORITEMS Script:

FORITEMS script works like FORCHARS but includes offline characters.
Criminal System:

Implemented new criminal system:
MEMORY objects are not removed during save.
MEMORY LAYER_FLAG_MURDERS has a character link to save during world save.
Kill timer check for MORE=0 during login (as MORE is not saved).
MEMORY LAYER_FLAG_CRIMINAL has a character link and saves during logout.
LAYER_FLAG_CRIMINAL no longer removed on death.
All timers in ghost mode now work.
MEMORY_FIGHT flags removed from the game.
Gray karma range extended to -10000.
Loot, carving, and snooping on characters grant criminal status.
Fight item granted regardless of victim's war mode.
Attacking blue karma grants criminal status.
Fame distributed equally among attackers in range of the victim.
Victim can return fire without becoming gray for the attacker.
Last kill now removed.
Kill item removed on last kill removal.
No kills or fame granted in regions with flags 0a8e and a481.
"Criminal!" message does not appear if character is already [criminal].
Death triggered immediately in OnTakeDamage if HP<=0 and the character is a player.
Green status characters are only those in the same guild.
No kills given for killing green or orange status characters.
Tamed animals are now blue karma, and attacking them grants criminal status.
MEMORY fights are not forcefully removed on death, timer set to 0.
Red guild members are now green.
No check for NPC being in a fight to grant fight item.
Normal fame distribution from NPCs (1/300th).
Fame distributed only to attackers within 16 tiles of the victim.
No karma granted for killing players with <0 karma.
Karma given to all killers, not distributed equally.
Karma granted if the killer was within 16 tiles of the victim.
PKs cannot increase karma above -3000.
Vampires with Plot & 0100 also have -3000 karma limit.
No fame or karma granted for killing tamed NPCs.
Tamed animals are no longer blue status.
Check for & 2000 instead of the a481 region.
Criminal timer is updated to 15 seconds if the character with [criminal] status is attacked within 15 seconds of clearing.
All fights are removed upon clearing criminal status.
All fights are removed upon clearing karma to blue.
All fights are removed upon clearing kill timer from 3 to 2.
Target of a fight is cleared upon death, but after the corpse is created.
No criminal status granted in special regions.
Crash Prevention:

SEH implemented to prevent crash during layer enumeration.
Criminal Timer:

Minimum criminal timer update on attack is 30 seconds.
No karma granted for NPC killers.
Karma Removal:

Karma is not removed for killing criminals with >0 karma, unless it's an NPC.
War Mode:

War mode is removed on death.
Polymorph:

Hair from polymorph does not disappear after restart.
DLL update without sphere restart implemented.
Mining/Fishing Timer:

Mining timer in a specific rectangle is set to RAND(120s).
Fishing timer set to 20 minutes.
Pet Aggression:

Attacking oneself with pets does not result in criminal status.
Mining timer in another specific rectangle is set to 600s.
Criminal status highlighted with yellow.
Criminal status granted only for looting blue corpses.
Script System:

Creation of a new script system started.
Character Creation:

Implemented a check for existing names during character creation.
Account Updates:

Account file updated during login.
DLL reload integrated into Resync restart.
DLL Update:

DLL does not reload if the update folder is empty.
ta.dll is removed from the update folder after loading the DLL.
Server Time:

Serv.rtime displays time HH:MM:SS.
Serv.rtimetext displays date YYYY/MM/DD.
Trade Window:

Prevented taking and using items from the trade window.
Trade windows destroyed when buying from a vendor.
No weight check during trade cancellation.
Overweight message upon item reception.
Links preserved on items when stacking.
Gump IDs:

Gump IDs sent to clients are now always randomly generated.
Error unexpected gump button is no longer logged.
Gump Manipulation:

New gump is not sent if no response from the old one.
Gumps from 200 to 209 have distortion applied to the gumppic string.
Power Hour:

Power Hour system (c) OSI implemented.
Moonglow Travel:

Prevented landing on ships in Moonglow region.
Trade Window Weight:

Allowed placing any weight in trade window containers.
Damage Display:

Damage amount displayed above character's head, color based on damage strength.
New Mounts:

New mounts added:
Energy vortex (recommended for GMs).
Beetle (recommended as a rare auction item).
Abyssycle (one-wheeled bicycle, recommended to be crafted with shrinkable item paint).
Trade Window and World Save:

All trade windows closed on world save.
Satellite Snapshot:

Satellite snapshot system implemented.
Satellite Snapshot Improvements:

Snapshot scale changed to 1:6.
Characters are marked with a circle.
Snapshot path changed.
Hidden and invisible characters are not included in the snapshot.
Snapshot time is logged.
Highlights for specific areas are added to the snapshot.
Snapshot generation frequency set to 30-60 minutes.
Container Weight:

Allowed taking any weight from any container, but items are dropped upon placing back in.
Shrinking Mounts:

Shrinking mounts are not un-shrunk on purchase.
Vendor Item Purchase:

Amount check implemented before item removal from vendor.
Limit of 20 items per purchase.
Amount hack detection implemented.
Bank Hack Prevention:

Bank hack prevention system implemented.
Bank Weight Display:

Bank weight displayed upon opening the bank.
Item Drop:

Check for item count on the ground implemented, with limits and warnings.
Newitem Script:

.act set to -1 for the character who creates a new item via script.
Bouncing Items:

Items are placed in the pack during bouncing.
Timer set to -1.
Attribute 02 removed.
Skill Values:

All skill values are now realistic.
Equipment Weight:

Allowed equipping any item regardless of overweight status.
Attribute 2 removed and timer set to -1 upon equipping.
Resource Fatigue:

Resource fatigue system implemented.
Ghost Speaking:

Ghost speaking working correctly.
Vendor Item Limit:

Player vendors cannot hold more than 100 items.
Vendor Command Restriction:

Player vendors ignore commands from non .em characters.
Moonglow Water Travel:

Prevented traveling by boat to the Moonglow region.
Prevented landing in region_type_multi.
Invulnerability Flag:

Characters with invulnerability flag are not attacked.
Boat Travel:

Boat travel restrictions and error handling implemented.
Boat Locking:

Boat sides are not unlocked during rotation.
Nickname Highlights:

Nickname highlight colors changed.
Field Spells:

Check for placement of field spells on tiles.
Identical fields replaced with new ones, except walls.
Wall amount is increased when cast on existing walls, and the item timer is updated.
Power Hour:

Power Hour system implemented.
Exceptions on Death:

Fixed exception errors on character death.
Character Titles:

Title added to nickname if # is present in NAME.
Young Player Note:

[young] note added if GT <= 5000 and character is level 1.
Wall of Stone:

Visibility check added for Wall of Stone cast.
Ghost Speaking:

Ghost speaking restricted to level 1 players.
Level 1 players always hear ghosts.
Spirit Speak flag set on death, removed on resurrection.
Casting Speed:

Casting speed adjusted based on armor value.
Double loot in Newbie Dungeon for money dropped by monsters.
NPC Display:

[NPC] tag removed.
[invulnerable] [hidden] [hallu] added for GMs.
[frozen] [tamed] [criminal] added for all characters.
Polymorph Armor:

Armor from polymorph is now taken into account.
Scroll Casting:

Scroll casting speed adjusted based on armor value.
Scroll MoreY:

MoreY set to 0 for Flame Strike, Lightning, and Paralyze scrolls.
Scroll Casting Restrictions:

Flame Strike, Lightning, and Paralyze scroll spells cannot be cast if armor is lower than 20.
Wall of Stone, Paralyze field, and Energy field cannot be cast if the target is a character.
Music System:

Music system implemented:
Checks for TRIGPERIODIC in SPHEREmap.scp.
Music can be assigned to specific regions.
Music list is loaded from the [REGION ...] trigger.
Random music plays on entry to a new region.
Music does not play for ghosts.
No new music plays if entering a region with the same trigperiodic as the exit region.
Data is updated during resync.
Music System - Live Background:

Music system implemented:
Music played in regions has a duration, with new music playing after it ends.
Music is played only once if the "ONTRIGGER=PERIODIC" string is not present in the [REGION ...] trigger.
Karma/Fame Distribution:

High-level system for karma/fame distribution on death implemented.
Field Spell Targets:

Field spells can now be cast on items (like corpses).
Classes:

Classes introduced, allowing races to become specific types based on professions.
Monk: Can restore mana by sacrificing health.
Hunter: Can create invisible spider silk traps.
Druid: Can enter summoned creatures and control them.
Vendor Bug Fixes:

Vendor bugs fixed.
Teleportation function now works in regions with ANTIMAGIC_RECALLIN.
Monk Clones:

Invisible stone created under monk clones.
NPC Death:

NPCs with STATF_DEAD flag now die properly.
Classes and Notes:

All classes completed and notes added.
Resurrection:

Resurrection from script no longer checks AM region.
Young Player Guards:

Guards for young players work like noble guards.
Lighting and Town Stones:

Lighting and town stone systems implemented.
Recollection:

Recollection bug fixed.
Curse Spell:

Curse spell cannot be cast on items.
Vendor Item Attribute:

Attribute 1000 removed from items purchased from vendors.
PK Restrictions:

PKs cannot recollect in guarded zones or use gate travel to enter them.
Young Player Message:

Young player message adjusted for hours remaining.
PVP Spells:

Attacking spells cannot be cast on players in PVP zones.
Pet Aggression:

NPCs with STATF_PET flag cannot attack in NO_PVP regions.
Bless Spell:

Bless spell on items with &010 attribute disabled.
Resurrection:

Resurrection now possible in regions with & 8000 flag.
Guild Chat:

.gu <message> command added for guild chat.
Guild Member List:

.gonline command added to show online guild members.
Loot Reduction:

Loot reduced by 50% for GPs in WasteLands and "The Abyss: *" regions.
Astral Character Resurrection:

Astral characters cannot be resurrected.
WasteLands Access:

Access to WasteLands via gate or recollection disabled.
Boat Travel:

Boat travel to the Moon region re-enabled.
Casting Speed:

Casting speed system updated for non-combat spells.
Item Durability:

Item durability changes implemented.
Arms Lore now displays item durability.
NPC Sleep System:

Sleep system for NPCs implemented.
Archery and Magery height difference check added.
New AI engine BRAIN_NEWAI = 15 added.
Young Player Game Time:

Young player status extended to 10k game time.
Vendor Restock:

Vendor restock timer set to 900 seconds.
Vendor item amount 244 changed to 500 on restock.
Incognito Removal:

Incognito automatically removed on logout and world save.
Sector Timer:

Timer set to 0 for characters entering a sector, and light sending is skipped.
Jail Guild Chat:

.gu command works in jail for players above level 1.
Nickname Display:

Nickname display function rewritten.
Sector entry timer set to 0 if greater than 10 seconds.
NPC Respawn:

NPC respawn system disabled.
Horse Removal:

Removed cause of horse removal.
Vendor Price Glitch:

Vendor price glitch fixed.
Damage Display:

Negative damage removed.
Newbie Dungeon loot restored.
Vendor Limits:

Vendor item limit set to 50.
Vendor NPC initial capital set to 1k.
Vendor NPC capital increased by half the total cost of sold items.
Crash Fixes:

.name command crash and .gu command crash fixed.
Report of glitched items on save added.
Report of all cgray exceptions added.
Logout Note:

[logout] note displayed correctly.
OnMakeCorpse Exception:

Exception in OnMakeCorpse function fixed.
DLL Exception:

DLL exceptions fixed related to getting pointers from sphere's global array.
Paperdoll Display:

Paperdoll display function rewritten.
Guild stone item name is now displayed, not the abbreviation.
Killer Titles:

Killer titles added based on kill count.
Killer List Exception:

Exception during killer list iteration fixed.
Jail Note:

[jailed] note added.
Invisibility and Logout Note:

[logout] note displayed even if the character is invisible.
GP Distribution:

System to grant 100 GPs to bank accounts from online.txt file implemented.
Monk Clone Protection:

Invisible stone created under monk clones.
Stat Increase:

Stat increase disabled while character has 1 of 4 curse types.
Wall of Stone:

Wall of Stone destroys traps and unfreezes characters.
New AI Engine:

New AI engine BRAIN_NEWAI = 16 implemented.
Sound Effects:

Sound effects added for NPC AI 15 and 16.
Container Restrictions:

Only bones with attr&&10 and link 4fffffff can be taken from containers.
Item Pickup Logging:

Item pickup time logging implemented.
Corpse Click Logging:

Corpse click time logging implemented.
Russian Language:

Russian language implemented in gumps.
Logout note display fixed.
Date and time added to debug and tainfo logs.
Killer Titles:

Killer titles removed.
GP Distribution Fix:

GP distribution fix for accounts.
Town Stone Tick:

Town stone tick implemented to fix town stone capture.
Gump ID Fix:

Gump ID request adjusted for Russian clients.
Russian Unicode:

Russian Unicode implemented for ".sysmessage" and ".message" commands.
Language Change:

Language change command ".lang" added.
Mayor Note:

[Mayor] note added for city mayors.
Bow Animation:

Bow animation on horses adjusted.
Horse Timer:

Horse timer fix.
Horse Removal on Dismount:

NPC horses are removed after shrinking or dismounting.
Horse Food Storage:

Horse food stored in MorePX upon mounting.
Server-Wide Gump:

serv.alltome command added to display a gump to all clients.
Update Scroll:

Update scroll removed on login.
@Login Event:

@Login event implemented for handling newly logged in characters.
Character Commands:

"tomefile <path>" and "execcmd" commands added for characters.
Mushroom fix.
Character Variables:

Full-function character variables BOLOR2 and FLAGS2 implemented.
Server-Wide Message:

serv.allmessage command added, Russian display is correct only if the command is in the script file.
Update News Message:

Update news message triggered by the presence of newsu.txt file.
Packet Limit:

Packet send limit set to 16384 bytes, with logging in debugcatch for exceeding the limit.
Nickname Display Optimization:

Nickname display function optimized.
Astral Note:

[astral] note added for Astral characters.
Bad Message Exception Logging:

Bad message exception logging implemented.
World Save Exception Logging:

World save exception logging implemented.
Flag Hold Time:

Flag hold time adjusted to 2 minutes.
Damage Display:

Damage display implemented for all types.
Universal Item Type 200:

Universal item type 200 implemented, with functionality based on More value:
more=1: Character astral projects to MoreP location.
more=2: 200k GPs consumed, comment updated with date +1 month, profpack.txt updated with account login and prof pack expiry date.
Instant Logout Restriction:

Instant logout restriction removed for non-nobles outside instant_logout regions.
Damage Display:

Damage only displayed if greater than 5.
Wall of Stone Cast Time:

Wall of Stone cast time adjusted to 3 seconds from books and 2 seconds from scrolls.
Casting Speed System:

Casting speed system no longer affects combat spells.
Trade Window Item Names:

Item names are displayed for all parties in the trade window.
World Save Exception:

World save exception fix, next save time is increased to avoid spamming.
Character Flags:

4B flags added to flags2.
Friendly Fire:

4B commands no longer kill friendly characters.
Character Activity Tracking:

LastActiveTime variable implemented to track character activity.
Active Clients count added to satellite info.
Game Time Saving:

Game time saved to account on each save.
Logout Time Addition:

Minute no longer added to logout time if it was zero.
Connection Queue:

Connection queue increased to 40k.
Log-IP Ban System:

Log-IP ban system rewritten.
Possible ping attack logging.
Wall of Stone Cast Time Fix:

Wall of Stone cast time fix.
PVP Points System:

PVP points system implemented, with titles assigned based on points.
Points are deducted from "looser" characters.
Anatomy now shows character's PVP points.
Anomalies:

Anomaly placeholder implemented during resync and .goxxxxx commands.
PVP Titles:

PVP titles adjusted, Warlord and Colonel swapped.
Weapon Durability:

Weapon durability adjusted for 100% durability from 10% to 100% real breakage.
Bone Carving:

Bone carving implemented:
Bone link set to the owner of the bones.
More and More2 copied from the corpse.
Bone name set to "Bones of victim carved by carver".
Item Animation:

Item movement animation enabled.
PVP Zone Expansion:

PVP points zone extended to red cities.
Blue-on-Blue Kill Karma:

Half the victim's karma is deducted from the killer.
Server Time Fixes:

serv.rtime and rtimetext commands fixed.
Item Damage:

Item damage reduced by half if the source is an NPC.
Wall of Stone Casting:

Wall of Stone cast time adjusted based on armor.
Character Variables:

Character variable src.gumps added.
Wipe System:

Wipe parameter #2 added to delete corrupt keys.
.gu Command:

Space check implemented for .gu command.
Wall of Stone Casting:

Wall of Stone cast time adjusted based on armor.
Character Stat Logging:

TotalMana, Invisibility, DeadlyPoisons, DragonMeats, IronIngots, Logs, and EyesOfNewt stats are logged.
Guild Member List Threading:

.goname command runs in a separate thread.
Recall Restrictions:

Recall disabled in AM_RECALLIN regions.
Skill Total Limit:

skilltotal command now caps skills at 100 if the total is greater than 100.
Text File Transfer:

All text files transferred to the TXT folder.
Class Movement Speed:

Movement speed adjustments for Monk and Hunter classes.
PVP Point Logging:

PVP point logging implemented.
Hunter Karma Penalty:

100 karma deducted from hunters if someone is caught in their trap.
Character Variables:

pvp1...pvp5 variables added, storing the last victim's serial number.
Vendor Purchase:

Vendor will not purchase items for 0 GPs.
Recruit PVP Points:

Recruits now start with 1 PVP point.
Guard Attack:

No fame or karma granted if a guard kills a monster.
Anatomy Display:

Anatomy now shows PVP points for players, but not for NPCs.
Anatomy display fixed.
Karma Distribution:

Karma distribution fixed.
PVP Point Logging:

PVP point logging updated to show when points are given.
Guild Member Kills:

Guild members who kill each other are not included in the last victim and PVP point calculations.
Anatomy Message:

Anatomy message now displayed on a single line.
PVP Point List:

Victims already in the killer's list are not added to the PVP point list.
Bad Message Exception:

Fixed frequent bad message exceptions with double clicks.
Fame Distribution:

Fame distribution set to 9/100.
Guard Kill Check:

Guard kill check disabled.
Bboard Logging:

Bboard hacking logging implemented.
Guard Fixes:

Guard fixes implemented.
Flip Command:

Flip command is not logged.
Noble Logout:

Noble logout speed increased outside guarded zones.
Wipe System:

Wipe system improved:
%<ID> to delete an ID without parameters.
$ prefix for hex parameters.
Logout Event:

ON=@Logout triggered on the second .xdiscoffect.
Home Point Saving:

HOMEP=P saved for characters in online status during world save.
Recall Speed:

Recall speed slowed down by 1.5x if magic is 90 or higher.
@Prelogin Event:

@Prelogin event implemented before sending the world to the character.
REGIONXYZ Function:

REGIONXYZ function implemented to return the region based on the character's location.
Nickname Display in Save Zones:

Nickname not displayed in save zones for inactive characters (5+ minutes idle).
Teleportation Speed:

Teleportation speed slowed down by 1.5x.
TTL (Time to Live) Parameter:

TTL parameter added for simple items.
TTL=DD.MM.YYYY: Sets a specific date for destruction.
TTL=0: Resets the destruction date.
TTLSET=<hex>: Sets the item to live for <hex> months.
TTLMINC=<hex>: Adds <hex> months to the current destruction date.
TTL saved during world save.
Item with TTL shows a message about its expiration date.
Recall Speed:

Recall speed increased for characters with GT<50000 who are not criminals or PKs.
PVP Point System:

New PVP point distribution system implemented.
PVP Point Display:

.xshow pvppoints command disabled for NPCs.
PVM Points:

PVM points added.
Guild War Karma:

No karma changes when killing a guild war character.
PVP/PVM Levels:

src.PVPLVL and PVMLVL variables added to track PVP/PVM levels.
Blood Link:

Blood now has a link to the character it came from.
Region Initialization:

initregion wrapped in SEH.
PVM Levels and Titles:

PVM levels implemented.
PVM titles added to Anatomy.
Paperdoll Titles:

Guild titles displayed in paperdoll for non-paladins and non-vampires.
Webpage Error Handling:

Webpage error handling debug implemented.
Prof Pack Logging:

Prof pack logging fix.
Damage2 Source:

damage2 source set to src.arg1, which is the source character's serial.
Character Variables:

src.pvm1..5 variables added.
Damage and Spell Effects:

arg1 functionality added for src.damage and spelleffect.
Invisible Characters:

Consuls and higher ranks no longer exit invisibility on save.
RegionXYZ Function:

regionxyz function now also returns the MULTI region type.
Cursed Items:

Cursed items can now be picked up.
Cursed/Blessed Item Names:

Cursed and Blessed prefixes now use lowercase.
Spell Effect Source:

spelleffect source set to the character itself.
AFK Status:

AFK status only applied to online characters in region 0a481.
Character Name Addition:

addcharname function improved.
Field Spell Dispel Effect:

Special effect displayed on field spell dispel.
Butcher Quest:

Butcher quest added.
Trap Immunity:

Characters with strength over 120 are immune to traps and destroy them.
PVP Point Award:

PVP points given for killing characters with 30 or more armor.
Butcher Quest Rewards:

Butcher quest reward implemented, including date in item name.
/questtime command added to show remaining time for quests.
Account Deletion:

Accounts with GT >= 200000 are never deleted by the sphere.
Zombie Quest:

Vampire killing zombie quest added.
Vampires teleported to spawn item location if outside a 50 tile radius.
Zombie Quest Fixes:

Zombie quest fixes.
PVM Points:

PVM points adjusted.
Bad Message Logging:

Last packet logged in bad message log.
Anomaly Fix:

Anomaly fix.
Item Damage:

Item damage reduced by 1.5x from all characters.
Alchemist Quest:

Alchemist quest added.
Trap Sound:

Sound added for trap activation.
Character Creation Debug:

addchar debug implemented.
Brain_NEWAI Fire:

brain_newai (15) now throws fire.
Exception Logging:

Exception logging implemented for charontick.
Process New AI Exception:

processnewai exception fix.
Cauldron Fix:

Cauldron fix.
Quest Bug Fix:

Quest bug fix.
Bad Message Fixes:

Bad message fixes.
PVP Points:

PVP points adjusted.
Character Variables:

src.xo (now src.ox) variable added for non-NPCs.
Character Town:

src.town variable added.
Client Version Check:

Client version check patch removed.
API Function:

lstrlen API function replaced with a faster version.
Party System:

Party system fully implemented.
No Crypt IP List:

TXT\ncip.txt file implemented to list IPs that should not be encrypted.
Fire Immune Flag:

Fire Immune flag (char.flags2 && 020) disabled.
TA 2.0.3 Test:

TA 2.0.3 ready for testing.
IP list updated without resync.
GMs cannot be added to parties, and they cannot invite others.
Encryption disabled.
Horse Food:

Horse food replenished every hour.
Horse summoning timer fix.
Character Pet Status:

Character pets are always blue if the character is online, otherwise their status is default.
Guard Aggression:

Guards no longer attack monsters unless they are pets.
Yellow Nicknames:

Characters with invulnerability now have yellow nicknames.
Pet Status:

Pets become blue when dismounted and remain blue until the character logs out.
Guard Behavior:

Guards approach monsters, and monsters enter guarded zones.
Horse Food Timer:

Horse food timer set to one hour.
NPC Sleep Teleportation:

Sleeping NPCs are teleported to their spawn location if further than 50 tiles away.
Horse Food Consumption:

Chance to consume horse food on dismount, based on the timer.
Monster Status:

Monster status is set to gray.
Resync Messages:

Resync messages replaced.
Guard Aggression:

Guards no longer approach monsters.
AI Brain Type 15:

Brain type 15 NPCs can now enter guarded zones.
Recollection Sound:

Sound added for recollection.
Kill Check:

Kill check added to ensure only criminals receive kills.
Horse Aggression Criminal Status:

Criminal status no longer granted when attacking oneself with a horse.
City Capture Reward:

City capture reward set to 100k.
Light Gradient:

New light gradient implemented.
City Capture Walls:

Walls near the town stone explode on city capture.
Farming:

Farming system added:
Universal item type 200, more=3, creates a farm plot.
Farming skill added to .show skilltotal.
Snowballs:

Snowballs added with the /snowball command.
Wall speed increased starting with 30 armor.
Telnet IP Mask:

Telnet IP list now supports subnets in the form ip.ip.0.0.
Snowballs Disabled:

Snow
