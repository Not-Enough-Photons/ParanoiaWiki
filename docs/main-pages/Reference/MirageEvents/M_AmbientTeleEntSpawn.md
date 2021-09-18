# Hallucinations

Hallucinations in Paranoia v3 operate very differently under the hood than the other two versions.
Instead, a system with JSON is used.

Each hallucination now has its own file in its respective folder.
Visual hallucinations go under the "BaseHallucination" folder, while audio hallucinations go under the "AudioHallucination" folder.

Inside the folders, you'll find JSON files for the individual hallucinations.
Here's an example of what you'll be working with:

#### Audio Hallucination JSON:
```json
(from Chaser.json)
{
    "baseFlags": "HideWhenClose | LookAtTarget | Moving",
    "startFlags": "SpawnAroundPlayer",
	"auditoryType": "Chaser",
    "useRandomSpawnAngle": true,
    "spawnRadius": 250.0,
    "moveSpeed": 50.0,
    "disableDistance": 1.0,
}
```

#### Base Hallucination JSON:
```json
(from ShadowMan.json)
{
    "baseFlags": "HideWhenClose | LookAtTarget",
    "startFlags": "SpawnAroundPlayer",
    "useRandomSpawnAngle": true,
    "spawnRadius": 100.0,
    "disableDistance": 50.0,
}
```

The JSON files contain various properties that can be set to achieve various effects.
Let's go over what the properties mean.

