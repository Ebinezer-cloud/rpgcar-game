# 🚗 TERRAIN VEHICLE 3D

> A browser-based 3D off-road driving game powered by **Three.js WebGPU** and **Rapier 3D physics**.

<p align="center">

**🚗 DRIVE • EXPLORE • BOOST • JUMP • CRASH • COLLECT 🌄**

</p>

<p align="center">
Procedurally generated terrain • Vehicle physics • Destructible environments • Dynamic biomes • Particles • Collectibles • Real-time tuning
</p>

---

## 🌄 About

**Terrain Vehicle 3D** is an experimental browser-based 3D driving game focused on realistic vehicle physics, procedural world generation, interactive environments, and modern GPU rendering.

Instead of using a single static map, the game dynamically generates terrain and environmental objects around the vehicle as the player explores.

### Core Experience

```text
🚗 VEHICLE PHYSICS
        +
🌄 PROCEDURAL TERRAIN
        +
🏜️ DESERT + 🌲 FOREST
        +
🌊 WATER EFFECTS
        +
💥 DESTRUCTIBLE OBJECTS
        +
🪙 COIN COLLECTION
        +
💨 PARTICLE EFFECTS
        +
⚙️ REAL-TIME SETTINGS
```

---

# ✨ Features

### 🚗 Physics-Based Vehicle

Powered by **Rapier 3D physics** with:

* Four-wheel vehicle simulation
* Wheel suspension
* Tire friction
* Steering
* Acceleration and braking
* Vehicle grip
* Jumping
* Flipping
* Boost system
* Collision physics
* Vehicle reset

### 🚀 Boost

Hold:

```text
SHIFT
```

Boost increases the vehicle's effective speed and helps with difficult terrain and jumps.

### 🪂 Jump

Press:

```text
SPACE
```

The vehicle uses a physics impulse to jump over terrain.

### 🌄 Procedural Terrain

The world is generated dynamically using procedural noise.

Terrain can contain:

* Hills
* Valleys
* Rolling terrain
* Dunes
* Forest elevations
* Natural terrain variation

### 🏜️ Multiple Biomes

Explore different environments including:

* 🏜️ Desert
* 🌲 Forest
* 🌊 Water regions

Biome characteristics change according to the vehicle's position.

### 🌊 Water System

Driving through water changes vehicle behavior and can generate splash particles around the wheels.

### 💨 Particle Effects

The game includes:

* Dust particles
* Water splashes
* Ambient wind dust
* Debris particles
* Destruction effects

### 🪙 Coin Collection

Coins are dynamically scattered throughout the world.

They feature:

* Floating animation
* Rotation
* Glow
* Collection effects
* Sparkle particles
* Score tracking

### 💥 Destructible Environment

Certain objects can be damaged and destroyed through vehicle collisions.

```text
HIGH-SPEED COLLISION
        ↓
     DAMAGE
        ↓
   OBJECT SHAKE
        ↓
      DESTROY
        ↓
   DEBRIS EFFECT
```

### 🗺️ Infinite-Style Exploration

As the vehicle moves, the game dynamically:

```text
GENERATES NEW TERRAIN
        ↓
GENERATES WORLD OBJECTS
        ↓
UPDATES PHYSICS
        ↓
REMOVES DISTANT OBJECTS
```

This allows continuous exploration without loading one massive static map.

### 🎥 Camera System

Includes:

* Third-person follow camera
* Smooth camera movement
* Configurable camera distance
* Camera height
* Look height
* Field of view
* Orbit camera

Press:

```text
O
```

to toggle orbit mode.

### ⚙️ Real-Time Settings

A custom glass-style settings panel allows real-time tuning of:

* Vehicle
* Camera
* Terrain
* Lighting
* Fog
* Biomes
* Dust
* Water splash
* Coin system
* Debug options

---

# 🎮 Controls

| Key     | Action               |
| ------- | -------------------- |
| `W`     | Drive forward        |
| `S`     | Reverse / Brake      |
| `A`     | Steer left           |
| `D`     | Steer right          |
| `SHIFT` | Boost                |
| `SPACE` | Jump                 |
| `R`     | Reset vehicle        |
| `P`     | Toggle debug mode    |
| `O`     | Toggle orbit camera  |
| `U`     | Open upgrade shop    |
| `ESC`   | Close upgrade shop   |
| `Mouse` | Orbit camera control |

---

# 🛠️ Technology Stack

| Technology        | Purpose                       |
| ----------------- | ----------------------------- |
| **Three.js**      | 3D rendering                  |
| **WebGPU**        | Modern GPU rendering          |
| **Three.js TSL**  | GPU shader/procedural effects |
| **Rapier 3D**     | Physics and collisions        |
| **ImprovedNoise** | Procedural terrain            |
| **Stats GL**      | Performance monitoring        |
| **JavaScript**    | Game logic                    |
| **HTML5**         | Application structure         |
| **CSS**           | UI and settings               |

---

# 🏗️ Architecture

The main game loop follows this general pipeline:

```text
USER INPUT
    ↓
VEHICLE CONTROL
    ↓
RAPIER PHYSICS
    ↓
WHEELS + SUSPENSION
    ↓
TERRAIN UPDATE
    ↓
WORLD SCATTER
    ↓
PARTICLES
    ↓
COINS
    ↓
DESTRUCTIBLE OBJECTS
    ↓
CAMERA
    ↓
WEBGPU RENDERING
```

---

# 📁 Project Structure

```text
rpg-car-game-main/
│
├── index.html
├── README.md
├── LICENSE
├── run.bat
│
└── models/
    └── README.md
```

The main application is intentionally compact, with the rendering, physics, terrain generation, gameplay systems, UI, and settings integrated into the main HTML application.

---

# 🚀 Getting Started

## Requirements

You need:

* A modern WebGPU-compatible browser
* Hardware acceleration enabled
* WebGPU-capable GPU
* Internet connection for CDN dependencies
* Node.js / `npx` for the included launcher

Recommended browser:

**Google Chrome / Chromium-based browser**

---

## ▶️ Run on Windows

The project includes a simple launcher:

```text
run.bat
```

### Steps

1. Download or clone the repository.
2. Open the project folder.
3. Double-click:

```text
run.bat
```

4. Open:

```text
http://localhost:3000
```

The launcher starts a local web server using:

```bash
npx serve .
```

### Manual Run

You can also run:

```bash
npx serve .
```

Then open the URL displayed in the terminal.

---

# 🧊 Custom 3D Models

Custom vehicle models are optional.

Place the following files inside:

```text
models/
```

```text
models/
├── chassis.glb
└── tire.glb
```

If the models are missing, the game automatically uses procedural fallback vehicle shapes.

Draco-compressed GLB models are supported.

---

# ⚡ Performance

The project includes several optimization techniques:

### Terrain

* Incremental terrain generation
* Dynamic heightfield updates
* Spatial terrain management

### World

* Cell-based object generation
* Distant object cleanup
* Limited active world regions

### Physics

* Rapier 3D physics
* Fixed timestep vehicle updates
* Controlled collision processing

### Rendering

* Three.js WebGPU
* GPU-based effects
* Configurable shadow resolution

### Monitoring

Press:

```text
P
```

to enable debug visualization.

The project also uses **Stats GL** for performance monitoring.

---

# 🐛 Troubleshooting

### Blank Screen

Run the project through a local web server instead of opening `index.html` directly.

```bash
npx serve .
```

### WebGPU Not Supported

Make sure:

* Your browser is updated
* Hardware acceleration is enabled
* Your GPU supports WebGPU

### Vehicle Stuck

Press:

```text
R
```

to reset the vehicle.

### Low FPS

Try:

* Lowering shadow resolution
* Disabling dust
* Disabling splash effects
* Disabling debug mode
* Reducing terrain complexity

---

# 🔮 Future Improvements

Planned or possible improvements include:

* 🏁 Racing checkpoints
* ⏱️ Timed races
* 🚗 Multiple vehicles
* 🔧 Expanded upgrade system
* 🌧️ Dynamic weather
* 🌙 Day/night cycle
* 🔊 Engine sounds
* 🎵 Environmental audio
* 🎮 Gamepad support
* 📱 Touch controls
* 🏆 High-score system
* 💾 Save-game system
* 🌐 Online leaderboards
* 👥 Multiplayer
* 🗺️ Larger environments

---

# 🤝 Contributing

Contributions and improvements are welcome.

### Clone

```bash
git clone <YOUR-REPOSITORY-URL>
```

### Enter the project

```bash
cd rpg-car-game-main
```

### Start the game

```bash
npx serve .
```

Test your changes in a WebGPU-compatible browser before submitting a pull request.

---

# 📜 License

This project is released under the **MIT License**.

You are free to:

* ✅ Use the project
* ✅ Study the source code
* ✅ Modify the project
* ✅ Create derivative works
* ✅ Distribute copies

See [`LICENSE`](LICENSE) for the complete license text.

---

# 👨‍💻 Author

**N. Ebinezer Jeba Samuel**

GitHub:

**https://github.com/Ebinezer-cloud**

---

# 🚗 Final Drive

```text
╔══════════════════════════════════════╗
║                                      ║
║       🚗 TERRAIN VEHICLE 3D         ║
║                                      ║
║       🌄 EXPLORE                    ║
║       🚀 BOOST                      ║
║       🪂 JUMP                       ║
║       💥 CRASH                      ║
║       🪙 COLLECT                    ║
║       🌊 SPLASH                     ║
║                                      ║
╚══════════════════════════════════════╝
```

<p align="center">

**Built with 🚗 + 🌄 + Three.js WebGPU + Rapier 3D**

</p>

