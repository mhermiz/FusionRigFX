# FusionPuppetPin

Custom DaVinci Resolve/Fusion Fuse for mesh-based 2D deformation using interactive puppet pins.

## Status
In active development.  
Current build includes:
- Procedural mesh generation from non-transparent pixels
- Multi-pin deformation system (up to 32 pins)
- Per-pin controls: position, radius, pull, rotation, expansion
- Setup/Animate rigging workflow
- Influence blending + falloff modes
- Root lock + optional secondary weight mask
- Debug overlays and pin color visualization
- Runtime optimizations via mesh/mask caching

## Features (Current)
- **Mesh**
  - Alpha-based region detection
  - Interior + contour point sampling
  - Contour expansion
  - Triangulated deformation mesh
- **Pins**
  - Up to 32 animatable pins
  - Per-pin influence and transform controls
- **Rigging**
  - Setup phase for placement/binding
  - Animate phase for deformation/animation
- **Deformation Controls**
  - Falloff shaping
  - Influence mixing when pins overlap
  - Optional root lock stabilization
  - Optional weight-mask locking

## Installation
1. Copy `PuppetPin_v1.0.fuse` into your Fusion Fuses folder.
2. Restart DaVinci Resolve/Fusion (or reload Fuses).
3. Add **Puppet Pin** from the custom tools category.

## Usage (Quick Start)
1. Connect your image/clip to Puppet Pin.
2. In **Mesh** tab, build/rebuild mesh.
3. In **Pins** tab, enable and place pins in **Setup** mode.
4. Switch to **Animate** mode and keyframe pin transforms.
5. Tune falloff/influence and optional masks as needed.

## Known Limitations
- Performance can vary with large meshes and large pin influence radii.
- Some edge-case contour generation scenarios are still being refined.

## Roadmap
- Improved contour quality and mesh cleanup
- Deformer systems (Follower, Wave, IK/FK)
- Solver improvements (single/multi-frame/elastic behaviors)
- Locator outputs and workflow polish

## Tech Stack
- DaVinci Resolve Fusion Fuse API
- Lua

## Author
Mario
