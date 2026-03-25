
# 🌲❄️ Three.js Tree Scenes Collection 

Two different 3D scene projects built using modern WebGL and Three.js:

*  **Windy Snow Tree** → Dynamic snow simulation with wind effect
*  **Realistic Tree Scene** → More detailed, organic tree model with branches

This repository provides practical and professional examples of **3D scene creation, particle systems, and procedural modeling**.

![Preview](assets/img/1.png)

---

##  Project Overview

| Project                 | Description                              |
| ----------------------- | ---------------------------------------- |
|  Windy Snow Tree        | Snow particles moving with wind          |
|  Realistic Tree Scene   | More realistic tree and cinematic camera |

---

##  Technologies Used

* **Three.js (r160)** → 3D rendering engine
* **WebGL** → GPU-accelerated graphics
* **JavaScript (ES Modules)** → Modern JS architecture
* **HTML5 Canvas** → Rendering surface

---

##  Project Structure

```bash
project/
│
├── windy-snow-tree/
│   └── index.html
│
├── realistic-tree/
│   └── index.html
│
└── README.md
```

---

#  Windy Snow Tree

###  Features

* 4000+ snow particles
* Wind effect (sin/cos-based movement)
* Procedural tree generation
* Lightweight and performance-focused

###  Technical Details

For each particle:

```js
speed + drift
```

Movement logic:

```js
x += sin(time + i) * drift
y -= speed
z += cos(time + i) * drift
```

---

#  Realistic Tree Scene

###  Features

* More realistic tree structure
* Branches + leaf clusters
* ACES Filmic Tone Mapping (cinematic look)
* Camera motion animation

###  Tree Structure

* Trunk: `CylinderGeometry`
* Branches: Randomly rotated cylinders
* Leaves: Spherical cluster system

---

##  Snow System (Shared Logic)

* High performance with `BufferGeometry`
* Thousands of particles
* Infinite loop (reset system)

```js
if(y < 0){
  y = maxHeight
}
```

---

##  Camera & Visual Quality

| Feature            | Description             |
| ------------------ | ----------------------- |
| Perspective Camera | Depth perception        |
| Tone Mapping       | More realistic lighting |
| Dynamic Movement   | Subtle camera animation |

---

##  Future Improvements

*  Night mode (HDRI skybox)
*  Advanced wind physics
*  OrbitControls integration
*  Snow shader (blur + glow)
*  Different tree variations
*  Ambient sound (wind)

---

##  Performance Notes

* `BufferGeometry` → Low CPU usage
* `requestAnimationFrame` → Optimized render loop
* Pixel ratio limitation:

```js
renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
```

---

##  Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a Pull Request

---

##  Developer

**Cihan Sarı**

* GitHub: https://github.com/ChnSari
* LinkedIn: https://linkedin.com/in/cihansri
* Email: [cihannsri@gmail.com](mailto:cihannsri@gmail.com)

---

##  License

This project is licensed under the MIT License.
See: https://choosealicense.com/licenses/mit/

---
