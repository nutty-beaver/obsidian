# Alarm Display
`Pre-configured graphics that shows scrolling list or multiple pages of alarms`
### Capabilities:
- Sorting by alarm priority
- Sorting by chronological order
- Sorting by predetermined process area
- Color coding by priority
- Ability to **temporarily freeze** the display list during periods of high alarm actuation
`this is because during high alarm actuation, it is very hard to read alarms when it is moving due to incoming alarms or blinking in and out`
- Ability to temporarily silence the alarm horn based on alarm priority
- Color and alarm symbology choices
- Displaying the measurement and the alarm setpoint violated
	`It is best to display on the alarm the limit violated instead of going through the measurements/limits screen`
- Guiding the operator in responding to the alarm, by linking the alarm to the display used to control the measurement or system in alarm

### Proper Alarm Display Design
- Priority system allowing independent priority settings for each alarms
- Alarm summaries that update the alarm list or measurement values dynamically
- Ability to temporarily suppress the alarm sound for some priorities
- Navigation ability to go, in one click, from an alarm on the display to the proper graphic for diagnosing the relevant situation
- Temporary alarm scroll freezing to aid readability

# Custom graphic
`operating graphic displays should act to always effectively help the operator control the process`

- **<u>Keystrokes</u>**: interface should be designed to minimized keystrokes required to identify and assess an alarm
- **<u>Associated Graphic</u>**: Every point with configured alarm should have an associated graphic display`
- **<u>Inherited Alarm Behavior</u>**: Graphics should not be hard-coded with alarm behavior for points
- **<u>Alarm Status Indication</u>**: process graphics should visually highlight [points](points.md)
- **<u>Colors</u>**: used to depict alarm-related functionality
- **<u>"Fat Finger" Contingencies</u>**: Minimize possibility of operator mistakes
	`example of this are providing confirmatory popup screen on critical buttons like shutdown or having limits on rules on setpoint input to avoid mistakes such as 1.2 instead of 1200
- **<u>Single Alarm Interface</u>**: All alarms should be brought to a single alarm interface. All alarms should be acknowledged only once; it should **never** be required to acknowledge the same alarm in more than one place.

# Alarm Priority
`means to convey a seriousness of a specific process condition to the operator and drives operator response`

Best practice is to use *three primary levels* of alarm priority
### Levels of alarm priority
- **Critical**: rarely used
- **Priority 1 (P1)**: highest
- **Priority 2 (P2)**: 2nd highest
- **Priority 3 (P3)**: 3rd highest
- **Priority 4 (P4)**: diagnostic-type

### Alarm Priority Color
Suggested colors:
- **P1**: <b style="color:red">Red</b>
- **P2**: <b style="color:yellow">Yellow</b>
- **P3**: <b style="color:orange">Orange</b>
- **P4**: <b style="color:magenta">Magenta</b>

### Alarm Priority Sound
- Each console or process location can use different family of identifiable sounds and can use small directional speaker for added localization
- It is possible to use indicator lights in conjunction with speaker
- Sound level around **15 dBA** (background noise) to **80 dBA**
- Ensure via testing that all alarm sounds and frequencies are audible and identifiable with operators
- Ability to turn off alarms for lower alarm priorities
- The preceding principles assume proper alarm management practices have produced a rationalized, meaningful, and effective alarm system. We don't want wang-wang of nuisance alarms

### Alarm Priority Distribution
|Alarm Priority |Percentage of Alarm|
|---|---|
|P1|5%|
|P2|15%|
|P3|80%|

