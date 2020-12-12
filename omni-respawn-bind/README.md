# omni-respawn-bind

A refresh on `optimal-respawn-bind`

## Usage

Hold `<YOUR KEY>` for ~150ms and release it. If not back on the previous class, click `<YOUR KEY>` again without holding.

Download this file, place it in your cfg directory: https://raw.githubusercontent.com/ldesgoui/tf2-custom/master/omni-respawn-bind/cfg/omni-orb.cfg

In autoexec.cfg:

    exec omni-orb
    bind <YOUR KEY> +orb.respawn

In each class' config:

    orb.<CLASS>

Some functionality can be configured:

When executing the script, the state holding the original class is uninitialized until a class config is executed, in order to prevent weird behavior, a fallback is defined, it is Soldier by default, you can change that by running:
 
    alias orb.set-class.fallback "orb.set-class.1" # for Scout, etc

By default, all classes will use the strategy to switch to a random class and back, except for Medic which will only switch to the 1st item loadout. You can change the strategy for each class, as well as the default by running:

    alias orb.strategy.default "orb.strategy.item.0" # Default to switching to the first item loadout
    alias orb.strategy.1 "orb.strategy.class" # Always switch classes while on Scout
    alias orb.strategy.7 "orb.strategy.item.2" # Use the 3rd item loadout instead on Medic
