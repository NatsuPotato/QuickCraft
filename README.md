# QuickCraft
QuickCraft is a 3D tile engine written in C inspired by Minecraft with a focus on speed and modularity (for modding!).

The base program implements fundamental utilities like asset loading, world management, worldgen tools, pathfinding tools, and UI stuff that modders can use to add their own content. The base program doesn't have any content in-and-of itself; the 'vanilla game' that comes with the download is itself just a mod!

## Planned Features
- 32³ cubic chunks
- Modding in WASM from compiled C
- Four different engines
  - **Manager** = keeps track of world state (AI, pathfinding, worldgen, spawning, light levels, entity positions, ad nauseum), handles requests for breaking/placing blocks, etc. (specifically on a per-tick level)
  - **Physics engine** = handles entity movement, collision, and other physics
  - **Renderer** = renders everything
  - **Factory** = responsible for events that happen over periods of time longer than a few ticks (promise system, "the stack of items moving through the pipe will reach their destination in 1738 ticks"). allows events in unloaded chunks to stay active (like furnaces smelting or pipes between chests)
