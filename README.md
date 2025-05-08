This project is a prototype of an NPC AI that uses FSM to make decisions,
defining its behavior according to the player's actions.
The NPC has two sensors:
+ Vision
    If the player enters the cone-shaped area, the NPC detects the player if
    there is no obstacle between them. 

+ Speed
    If the player runs within the detection area of the aqua-colored circle, the
    NPC detects him, even through obstacles between them.

## Search mode
In this mode, the NPC tries to maintain vision detection by rotating itself. If
the player continues to be detected after the time in this mode has run out, the
NPC switches to attack mode, otherwise it switches to idle or patrol mode. 

![search_mode](./illustrations/search_mode.gif)

## Attack mode
Chases the player while in the vision detection area or running inside the speed
detection area.

![attack_mode](./illustrations/attack_mode.gif)

## Alert mode
After the NPC leaves the attack mode state, it switches to this state, if it
detects the player, it switches back to the attack mode state.

![alert_mode](./illustrations/alert_mode.gif)

## Patrol mode
If the NPC detects the player it goes to the search mode.

![patrol_mode](./illustrations/patrol_mode.gif)
