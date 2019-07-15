# tf2_optimal_respawn_bind

## Usage

Hold <YOUR KEY> for ~150ms and release it. If not back on the previous class, click <YOUR KEY> again.

In custom.cfg (or autoexec.cfg if not using mastercomfig):

    exec orb
    bind <YOUR KEY> +orb.respawn
    
In each class' config:

    orb.<CLASS>
    
## Explanation

Team Fortress 2 lets you respawn instantaneously in the spawn rooms when you change classes or loadout.
A loadout switch bind is a common way to get respawning quickly, however it relies on the TF2 item server being available and responding quickly, there is an inconsistent delay of one ore more seconds between the command and the actual respawn.
This script (`orb`) makes use of class changing instead, allowing for instantaneous respawn to another class, then another respawn to the previous class. There is a cooldown on class changes, however it is much shorter than the average loadout switch. The script recovers itself in case you release too quickly.
