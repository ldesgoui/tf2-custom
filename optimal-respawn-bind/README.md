# optimal-respawn-bind

## Usage

Hold `<YOUR KEY>` for ~150ms and release it. If not back on the previous class, click `<YOUR KEY>` again without holding.

Download this file, place it in your cfg directory: https://raw.githubusercontent.com/ldesgoui/tf2-custom/master/optimal-respawn-bind/cfg/orb.cfg

In custom.cfg (or autoexec.cfg if not using mastercomfig):

    exec orb
    bind <YOUR KEY> +orb.respawn

In each class' config:

    orb.<CLASS>

## Explanation

Team Fortress 2 lets you respawn instantaneously in the spawn rooms when you change classes or loadout.

A loadout switch bind is a common way to get respawning quickly, however it relies on the TF2 item server being available and responding quickly, there is an inconsistent delay of more than 500ms between the command and the actual respawn.

This script (`orb`) makes use of class changing instead, allowing for instantaneous respawn to another class, then another respawn to the previous class. There is a cooldown on class changes, however it is much shorter than the average loadout switch. In the case where you release too soon, the next press of the bind will immediately change back to the original class.

There exists a special case for Medic, instead of changing class, the loadout switch bind is employed, as switching classes would make the player lose progress on ubercharge. You can enable this behavior on more classes (i.e.: Engineer) by appending `.medic` at the end of the `orb.current.1` aliases, similarly to how `orb.current.7` is defined. 
