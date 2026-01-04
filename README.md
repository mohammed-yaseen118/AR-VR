# 3D Interactive Jewellery Display 

## Overview
This project is a high-fidelity **3D Interactive Jewellery Display** developed using the **A-Frame framework**.  
It simulates a luxury “Jewellery Box” experience where users can visually inspect multiple rings with realistic lighting, smooth animations, and intuitive interactions.

The project strictly follows an **Entity-Component-System (ECS)** architecture without using any pre-built interaction libraries.

---

## Features

### Visual Fidelity
- Physically Based Rendering (PBR) using metalness and roughness materials
- Dynamic lighting for realistic metallic reflections
- High-quality gold, silver, diamond, and rose-gold materials

### Interaction
- Click or tap on a ring to bring it into focus
- Smooth animation moving the ring forward and scaling it up
- Dedicated **Return to Box** UI button
- Ring animates back to its **exact original position and scale**

### State Management
- Only one ring can be focused at a time
- All other interactions are blocked while a ring is active
- Clean state reset after closing the focused ring

### Advanced Controls
- Continuous drag-to-rotate interaction
- Y-axis rotation only (yaw)
- Rotation remains cumulative across multiple drags
- Rotation automatically resets when returning the ring

---

## Technical Architecture
- **Framework:** A-Frame
- **Pattern:** Entity-Component-System (ECS)
- **Custom Components:**
  - `gallery-manager` (global state & UI control)
  - `ring-interaction` (focus & return animations)
  - `drag-rotator` (continuous Y-axis rotation)

No external interaction templates or helper libraries were used.

---

## How to Run Locally
```bash
# Clone the repository
git clone <your-repo-url>

# Open index.html using Live Server or any static server
