# Ticks

With the new way that ticks are set up in Paranoia v3, this allows for ease of access when it comes to defining new events.

"Ticks" in Paranoia are time based events. Events are started/fired when the max time is reached.


When you open the **ticks.json** file, you'd likely be greeted with something like this:

```json
{
		"tickName": "Tick_Ambience",
		"tick": 0.0,
		"minRange": 90.0,
		"maxRange": 130.0,
		"fireEvent": "M_AmbientAudioSpawn",
		"tickType": "Any"
},
```

This particular block is for the mods tick system.
Let's take a look at what all of the properties mean.

### tickName
Name of the tick. Not really used for anything except for debugging and error logging.

### tick
Tick defines at what point the tick starts. "0.0" is the default value for all of these.
If you want the tick to start earlier or later, set this value to something else.

### minRange
Defines the minimum value for the time to be randomized when we reach the max time.

### maxRange
Same goes for above, just with the maximum value this time.

### maxTick
Max tick (or max time) is the maximum time that the timer can reach before firing the event.
If no minimum or maximum value was provided before, the time will not be random, and will not change when the tick finishes.

### fireEvent
In previous verions of Paranoia, events were fired based on an action system.
Things were called internally, and as more events were added, the codebase became messy.

Version three changes this by allowing for you to change the event you want.

The event gets called as soon as the timer reaches its maximum value.
See [Functions](/main-pages/Functions/) for more details.

### tickType
TickType defines the tick being able to be executed only when its light, dark, or both.
