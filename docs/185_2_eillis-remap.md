# Eillis' Original Profile Updated to v185 Spec
* [185_2_eillis-remap.xml](../versions/185_2_eillis-remap.xml)
* `v185` spec
* 2nd profile slot
* Requires `SpoddyCoder-X4-Layout` Steam Controller layout.


## Description
* Based on `185_1_eillis.xml`, but remapped to use the `SpoddyCoder-X4-Layout` Steam Controller layout.
* This preserves the original Eillis' control scheme, but with the flexibility to rebind the controls for full keyboard + mouse functionality.


## Steam Controller Layout
* See [SpoddyCoder's Layout Reference](./Layout-Reference-SpoddyCoder.md) for steam controller + keyboard bindings.


## In-Game Mappings

### Primary Functions: `No Modifier`
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| In-Game Action          | Controller Input      | Key / Button Binding  | Inputmap Action / State                                                                                     |
|-------------------------|-----------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|
| Accelerate              | A                     | A                     | `INPUT_STATE_ACCELERATE`                                                                                    |
| Boost                   | A dp                  | ;                     | `INPUT_STATE_BOOST`                                                                                         |
| Decelerate              | B                     | B                     | `INPUT_STATE_DECELERATE`                                                                                    |
| Full Stop               | B dp                  | '                     | `INPUT_ACTION_STOP`                                                                                         |
| Deploy Countermeasures  | X                     | X                     | `INPUT_ACTION_DEPLOY_COUNTERMEASURE`                                                                        |
| Target Hostile          | Y                     | Y                     | `INPUT_ACTION_TARGET_NEXT_ENEMY`                                                                            |
| Target Object           | Y dp                  | ]                     | `INPUT_ACTION_TARGET_NEXT_TARGET`                                                                           |
| Fire Primary Weapon     | LB                    | LB                    | `INPUT_STATE_FIRE_PRIMARY_WEAPON`                                                                           |
| Fire Secondary Weapon   | RB                    | RB                    | `INPUT_STATE_FIRE_SECONDARY_WEAPON`                                                                         |
| Switch Ammunition       | Dpad Up               | Dpad Up               | `INPUT_ACTION_CYCLE_NEXT_ACTIVE_WEAPON_AMMO`                                                                |
| Scan                    | Dpad Left             | Dpad Left             | `INPUT_ACTION_SCAN_ACTION`                                                                                  |
| Magnet                  | Dpad Down             | Dpad Down             | `INPUT_STATE_LOOTMAGNET`                                                                                    |
| Interact                | Back                  | Back                  | `INPUT_STATE_INTERACTION_MENU`                                                                              |
| Quick Action Menu       | Back dp               | \                     | `INPUT_ACTION_OPEN_COCKPIT_MENU`                                                                            |
| Map                     | Start                 | Start                 | `INPUT_ACTION_OPEN_MAP`                                                                                     |
| Options Menu            | Start dp              | /                     | `INPUT_ACTION_OPTIONSMENU`                                                                                  |
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Weapons + Combat: `Hold X`
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| In-Game Action          | Controller Input      | Key / Button Binding  | Inputmap Action / State                                                                                     |
|-------------------------|-----------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|
| Next Primary Weapon     | X + LB                | CTRL + ,              | `INPUT_ACTION_CYCLE_NEXT_PRIMARY_WEAPONGROUP`                                                               |
| Next Secondary Weapon   | X + RB                | CTRL + .              | `INPUT_ACTION_CYCLE_NEXT_SECONDARY_WEAPONGROUP`                                                             |
| Aim Assist              | X + Dpad Up           | CTRL + Up             | `INPUT_ACTION_TOGGLEAIMASSIST`                                                                              |
| Turrets                 | X + Dpad Left         | CTRL + Left           | `INPUT_ACTION_TOGGLE_TURRET_ACTIVE`                                                                         |
| Drones                  | X + Dpad Right        | CTRL + Right          | `INPUT_ACTION_TOGGLE_DRONE_LAUNCH`                                                                          |
| Flight Asssist          | X + Dpad Down         | CTRL + Down           | `INPUT_ACTION_TOGGLE_FLIGHT_ASSIST`                                                                         |
| Missions                | X + Start             | CTRL + M              | `INPUT_ACTION_OPEN_MISSIONS`                                                                                |
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Targetting: `Hold Y`
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| In-Game Action          | Controller Input      | Key / Button Binding  | Inputmap Action / State                                                                                     |
|-------------------------|-----------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|
| Match target speed      | Y + B                 | SHIFT + Bk            | `INPUT_STATE_MATCH_SPEED`                                                                                   |
| Target lock             | Y + X                 | SHIFT + Xk            | `INPUT_ACTION_TOGGLE_TARGET_LOCK`                                                                           |
| Property owned          | Y + Start             | SHIFT + M             | `INPUT_ACTION_OPEN_PROPERTY_MENU`                                                                           |
| Change target           | Y + Dpad Left/Right   | SHIFT + Left/Right    | `INPUT_ACTION_PREV_TARGET_ACTION`, `INPUT_ACTION_NEXT_TARGET_ACTION`                                        |
| Change subsystem        | Y + Dpad Up/Down      | SHIFT + Up/Down       | `INPUT_ACTION_PREV_SUBCOMPONENT`, `INPUT_ACTION_NEXT_SUBCOMPONENT`                                          |
| Fire primary at cursor  | Y + LB                | SHIFT + ,             | `INPUT_STATE_FIRE_PRIMARY_WEAPON_AT_CURSOR`                                                                 |
| Fire secondary weapon   | Y + RB                | SHIFT + .             | `INPUT_STATE_FIRE_SECONDARY_WEAPON`                                                                         |
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Systems + Interaction: `Hold Back`
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| In-Game Action          | Controller Input      | Key / Button Binding  | Inputmap Action / State                                                                                          |
|-------------------------|-----------------------|-----------------------|------------------------------------------------------------------------------------------------------------------|
| Travel mode             | Back + A              | 1                     | `INPUT_ACTION_TOGGLE_TRAVEL_MODE`, `INPUT_ACTION_ADDON_DETAILMONITOR_TRAVELMODE`, `INPUT_STATE_DETAILMONITOR_B`  |
| Autopilot               | Back + A dp           | NUM 1                 | `INPUT_ACTION_TOGGLE_AUTOPILOT`, `INPUT_ACTION_ADDON_DETAILMONITOR_A_SHIFT`                                      |
| Dock                    | Back + B              | 2                     | `INPUT_ACTION_DOCK_ACTION`, `INPUT_ACTION_UNDOCK`, `INPUT_ACTION_ADDON_DETAILMONITOR_REMOVE_ORDER`               |
| Get Up From Chair       | Back + B dp           | NUM 2                 | `INPUT_ACTION_GET_UP`, `INPUT_ACTION_DEBUG_NUMPAD2`                                                              |
| Comm                    | Back + X              | 3                     | `INPUT_ACTION_COMM_ACTION`, `INPUT_STATE_DETAILMONITOR_Y`                                                        |
| Object Info             | Back + X dp           | NUM 3                 | `INPUT_ACTION_INFO_ACTION`, `INPUT_ACTION_ADDON_DETAILMONITOR_I`                                                 |
| Scanner                 | Back + Y              | 4                     | `INPUT_ACTION_TOGGLE_SCAN_MODE`, `INPUT_STATE_DETAILMONITOR_X`                                                   |
| Long Range Scanner      | Back + Y dp           | NUM 4                 | `INPUT_ACTION_TOGGLE_LONGRANGE_SCAN_MODE`                                                                        |
| Interaction 1           | Back + A              | 1                     | `INPUT_ACTION_TOGGLE_TRAVEL_MODE`, `INPUT_ACTION_ADDON_DETAILMONITOR_TRAVELMODE`, `INPUT_STATE_DETAILMONITOR_B`  |
| Interaction 2           | Back + B              | 2                     | `INPUT_ACTION_DOCK_ACTION`, `INPUT_ACTION_UNDOCK`, `INPUT_ACTION_ADDON_DETAILMONITOR_REMOVE_ORDER`               |
| Interaction 3           | Back + X              | 3                     | `INPUT_ACTION_COMM_ACTION`, `INPUT_STATE_DETAILMONITOR_Y`                                                        |
| Interaction 4           | Back + Y              | 4                     | `INPUT_ACTION_TOGGLE_SCAN_MODE`, `INPUT_STATE_DETAILMONITOR_X`                                                   |
| Interaction 5           | Back + LB             | 5                     | `INPUT_ACTION_DIALOG_5`                                                                                          |
| Interaction 6           | Back + RB             | 6                     | `INPUT_ACTION_DIALOG_6`                                                                                          |
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Camera: `Hold Start`
-----------------------------------------------------------------------------------------------------------
| In-Game Action          | Controller Input      | Key / Button Binding  | Inputmap Action / State       |
|-------------------------|-----------------------|-----------------------|-------------------------------|
| Camera Up               | Start + Dpad Up       | F1                    | `INPUT_STATE_CAMERA_UP`       |
| Camera Left             | Start + Dpad Left     | F2                    | `INPUT_STATE_CAMERA_LEFT`     |
| Camera Right            | Start + Dpad Right    | F3                    | `INPUT_STATE_CAMERA_RIGHT`    |
| Camera Down             | Start + Dpad Down     | F4                    | `INPUT_STATE_CAMERA_DOWN`     |
| Cycle camera            | Start + LB            | +                     | `INPUT_ACTION_CYCLE_VIEW`     |
| Target camera           | Start + RB            | -                     | `INPUT_ACTION_TARGET_VIEW`    |
| Zoom In                 | Start + LT            | PageDown              | `INPUT_STATE_CAMERA_ZOOMIN`   |
| Zoom Out                | Start + RT            | PageUp                | `INPUT_STATE_CAMERA_ZOOMOUT`  |
-----------------------------------------------------------------------------------------------------------


## Tested
* Primary functions - OK
* Weapon Modifiers - OK
* Targetting Modifiers - OK
* Systems + Interaction Modifiers - Mostly OK
  * Dialog 2 - doesnt work in station, works in space
    * Bound to dock, could be reason? as this takes you straight back to ship when in station but outside of a dialog.
  * Dialog 3 - doesn't work in space, works in station
  * The autopilot / travel mode is a little buggy, but does work
    * Coming out of autopilot goers straight into travel mode and then cancelling travel mode results in it immediately being re-enabled, so you have to press again to come out of travel mode.
* Camera Modifiers - OK