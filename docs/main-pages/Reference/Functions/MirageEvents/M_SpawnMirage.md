# M_SpawnMirage(BaseHallucination hallucination)

"Spawns" in a hallucination from the available hallucinations in the game manager.

Here are all of the hallucinations you can spawn in:
- hAmbience
- hChaser
- hDarkVoice
- hTeleportingEntity
- hParalyzer
- hRadio
- hCeilingMan
- hStaringMan
- hShadowPerson
- hShadowPersonChaser
- hObserver
- hFordScaling
- hCursedDoor
- hInvisibleForce

# Example usage

Here we have a tick setup for spawning in a mirage.
We'll have it occur randomly, and at a certain insanity level.

```json
	{
		"tickName": "Tick_Chaser",
		"tick": 0.0,
		"minRange": 120.0,
		"maxRange": 145.0,
		"useInsanity": true,
		"targetInsanity": 2.25,
		"fireEvent": "M_SpawnMirage(hChaser)",
		"tickType": "Any"
	},
```