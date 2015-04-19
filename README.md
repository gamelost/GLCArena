# GLCArena

GLC on Unreal Engine 4. This is an experimental UE4 level for competitive multiplayer combat.

# Running Instructions

Since the default instructions isn't always right away clear as of what/how to do things, here's a rough outline as of what should be done.

Dedicated Server:
```
"D:\Program Files\Epic Games\4.7\Engine\Binaries\Win64\UE4Editor.exe" "C:\cygwin64\home\paul\GLCArena\GLCArena.uproject" Arena -server -game -log
```

The important bits is the path. Now the "Arena" is the map that you start the server with, you can have more than 1 map, this lets you pick a specific one to start off with.  This must also be reflected in the `Config/DefaultEngine.ini` otherwise it will try to load a non-existant default map.

Then `-log` is needed so you get a small shell with log output from the server otherwise it will background with nothing.
The other two `-server` (ded server) and `-game` game mode vs editor mode.

Client:
```
"D:\Program Files\Epic Games\4.7\Engine\Binaries\Win64\UE4Editor.exe" "C:\cygwin64\home\paul\GLCArena\GLCArena.uproject" 10.0.1.121 -game
```

The client is much easier, all it needs to know is the project, and the ip address of the server and off to the races it goes. The map decision is up to the server, again `-game` is the same as the server.
