# QuickCraft
QuickCraft is a 3D tile engine written in C inspired by Minecraft with a focus on speed and modularity (for modding!).

## Planned Features
- 32³ cubic chunks
- Modding in WASM from compiled C
- Four different engines
  - manager = keeps track of world state, handles requests for breaking/placing blocks, keeps track of where things are, etc. (specifically on a per-tick level)
  - physics engine = handles entity movement, collision, and other physics
  - renderer = renders everything
  - factory engine = responsible for events that happen over periods of time longer than a few ticks (promise system, "the stack of items moving through the pipe will reach their destination in 1738 ticks"). allows events in unloaded chunks to stay active (like furnaces smelting or pipes between chests)
