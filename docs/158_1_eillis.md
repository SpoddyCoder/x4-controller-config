# Eillis' Original Profile
* [158_1_eillis.xml](../versions/158_1_eillis.xml)
* `v158` spec
* 1st profile slot
* Requires `X4 Eillis' Gamepad` layout


## Description
* The original inputmap from Eillis.


## Steam Controller Layout
* See [Eillis' Layout Reference](./Layout-Reference-Eillis.md) for steam controller + keyboard bindings.


## In-Game Mappings

### Primary Functions: `No Modifier`
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| In-Game Action          | Controller Input      | Key / Button Binding  | Inputmap Action / State                                                                                     |
|-------------------------|-----------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|
| Accelerate              | A                     | A                     | `INPUT_STATE_ACCELERATE`                                                                                    |
| Boost                   | A dp                  | W                     | `INPUT_STATE_BOOST`                                                                                         |
| Decelerate              | B                     | B                     | `INPUT_STATE_DECELERATE`                                                                                    |
| Full Stop               | B dp                  | S                     | `INPUT_ACTION_STOP`                                                                                         |
| Deploy Countermeasures  | X                     | X                     | `INPUT_ACTION_DEPLOY_COUNTERMEASURE`                                                                        |
| Target Hostile          | Y                     | Y                     | `INPUT_ACTION_TARGET_NEXT_ENEMY`                                                                            |
| Target Object           | Y dp                  | U                     | `INPUT_ACTION_TARGET_NEXT_TARGET`                                                                           |
| Fire Primary Weapon     | LB                    | LB                    | `INPUT_STATE_FIRE_PRIMARY_WEAPON`                                                                           |
| Fire Secondary Weapon   | RB                    | RB                    | `INPUT_STATE_FIRE_SECONDARY_WEAPON`                                                                         |
| Switch Ammunition       | Dpad Up               | Dpad Up               | `INPUT_ACTION_CYCLE_NEXT_ACTIVE_WEAPON_AMMO`                                                                |
| Scan                    | Dpad Left             | Dpad Left             | `INPUT_ACTION_SCAN_ACTION`                                                                                  |
| Magnet                  | Dpad Down             | Dpad Down             | `INPUT_STATE_LOOTMAGNET`                                                                                    |
| Interact                | Back                  | Back                  | `INPUT_STATE_INTERACTION_MENU`                                                                              |
| Quick Action Menu       | Back dp               | C                     | `INPUT_ACTION_OPEN_COCKPIT_MENU`                                                                            |
| Map                     | Start                 | Start                 | `INPUT_ACTION_OPEN_MAP`                                                                                     |
| Options Menu            | Start dp              | N                     | `INPUT_ACTION_OPTIONSMENU`                                                                                  |
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Weapons + Combat: `Hold X`
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| In-Game Action          | Controller Input      | Key / Button Binding  | Inputmap Action / State                                                                                     |
|-------------------------|-----------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|
| Next Primary Weapon     | X + LB                | CTRL + L              | `INPUT_ACTION_CYCLE_NEXT_PRIMARY_WEAPONGROUP`                                                               |
| Next Secondary Weapon   | X + RB                | CTRL + R              | `INPUT_ACTION_CYCLE_NEXT_SECONDARY_WEAPONGROUP`                                                             |
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
| Fire primary at cursor  | Y + LB                | SHIFT + L             | `INPUT_STATE_FIRE_PRIMARY_WEAPON_AT_CURSOR`                                                                 |
| Fire secondary weapon   | Y + RB                | SHIFT + R             | `INPUT_STATE_FIRE_SECONDARY_WEAPON`                                                                         |
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


## Eilli's Original Control Reference
When no modifier buttons are held:
* A = A button as single press, W key as double press.
* B = B button as single press, S key as double press.
* X = X button as single press, Z key as double press.
* Y = Y button as single press, U key as double press.
* Back = Back as single press, C as double press.
* Start = Start as single press, N as double press.
* Left bumper = Left bumper.
* Right bumper = Right bumper.

Holding X button generally works like holding Ctrl on keyboard.
* A = Ctrl+A keys as single press, Ctrl+W keys as double press.
* B = Ctrl+B keys as single press, Ctrl+S keys as double press.
* X = (Held as modifier.)
* Y = Ctrl+Y keys as single press, Ctrl+U keys as double press.
* Back = Ctrl+V keys as single press, Ctrl+C keys as double press.
* Start = Ctrl+M keys as single press, Ctrl+N keys as double press.
* Left bumper = Ctrl+L key.
* Right bumper = Ctrl+R key.

Holding Y button generally works like holding Shift on keyboard.
* A = Shift+A keys as single press, Shift+W keys as double press.
* B = Shift+B keys as single press, Shift+S keys as double press.
* X = Shift+X keys as single press, Shift+Z keys as double press.
* Y = (Held as modifier.)
* Back = Shift+V keys as single press, Shift+C keys as double press.
* Start = Shift+M keys as single press, Shift+N keys as double press.
* Left bumper = Shift+L keys.
* Right bumper = Shift+R keys.

Holding Back turns some buttons into numbers, with double presses being numpads.
* A = 1 key as single press, Num 1 as double press.
* B = 2 key as single press, Num 2 as double press.
* X = 3 key as single press, Num 3 as double press.
* Y = 4 key as single press, Num 4 as double press.
* Left bumper = 5 key.
* Right bumper = 6 key.

Holding Start turns DPad into F keys.
* DPad Up = F1
* DPad Left = F2
* DPad Right = F3
* DPad Down = F4
* Left bumper = plus key.
* Right bumper = minus key.

### In-Game Mappings
1. Triggers/Joysticks
* flying axes.

2. Without modifiers:
* A = Acceleration, double press for Boost.
* B = Deceleration, double press for Full Stop.
* X = Deploy Countermeasure.
* Y = Target Hostile, double press for Target Object.
* LB = Primary weapon fire.
* RB = Secondary weapon fire.
* DPad Up = Switch ammunition.
* DPad Left = Scan.
* DPad Down = Magnet.
* Back = Interact, double press for Quick Action Menu.
* Start = Map, double press for Options Menu.

3. Holding X generally deals with weapons and combat systems.
* X + LB = Next primary weapon.
* X + RB = Next secondary weapon.
* X + DPad Up = Aim assist.
* X + DPad Left = Turrets.
* X + DPad Right = Drones.
* X + DPad Down = Flight assist.
* X + Start = Missions.

4. Holding Y generally deals with targetting.
* Y + B = Match target speed.
* Y + X = Target lock.
* Y + Start = Property owned.
* Y + DPad = Change target/subsystem.

5. Holding Back generally deals with ship systems and interactions.
* Back + A = Travel mode, double press for Autopilot.
* Back + B = Dock, double press for Get Up From Chair.
* Back + X = Comm, double press for Object Info.
* Back + Y = Scanner mode, double press for Long Range Scanner mode.
* Since Back + A/B/X/Y/LB/RB act as 1-6 keys, they are also used for NPC interactions. This is additionaly intuitive, considering Back is used for initiating an interaction.

6. Holding Start generally deals with camera.
* Start + DPad = Camera Up/Down/Left/Right.
* Start + LB = Cycle camera.
* Start + RB = Target camera.
* Start + LT = Zoom in.
* Start + RT = Zoom out.

7. When in map/menu mode, I usually use joystick to control cursor and joystick presses as mouse clicks.


## Tested
* Primary functions - OK
* Weapon Modifiers - OK
* Targetting Modifiers - OK
* Systems + Interaction Modifiers - Mostly OK
  * Dialog 2 - works in space, doesnt work in station
    * Bound to dock, could be reason? as this takes you straight back to ship when in station but outside of a dialog.
  * Dialog 3 - doesn't work in space, works in station
  * The autopilot / travel mode is a little buggy, but does work
    * Coming out of autopilot goers straight into travel mode and then cancelling travel mode results in it immediately being re-enabled, so you have to press again to come out of travel mode.
* Camera Modifiers - OK