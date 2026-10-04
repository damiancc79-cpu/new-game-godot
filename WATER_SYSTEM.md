# FFT Ocean and Jet-Ski Buoyancy

This project uses `tessarakkt/godot4-oceanfft` at commit
`01f32d7151a71c898e286b6f6049e6f32ff665bb`.

Source: https://github.com/tessarakkt/godot4-oceanfft

License: MIT. The complete upstream license is retained at
`addons/tessarakkt.oceanfft/LICENSE.txt`.

## Runtime scene

`ocean_demo.tscn` combines:

- Tessendorf FFT wave generation on the GPU
- CDLOD ocean geometry
- CPU-synchronized wave-height sampling
- Five-point rigid-body buoyancy for a personal-watercraft-sized hull
- Submerged drag, motor thrust, and steering forces
- Above-water and underwater environment transitions

## Controls

- Up arrow: thrust forward
- Down arrow: reverse thrust
- Left/right arrows: steer

The water system requires the Forward+ rendering method because it uses compute
shaders. The current sea state is scaled for a roughly 3.6-meter jet ski.
