# 🚁 MediLift — Autonomous AI Precision Organ Delivery Drones

[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg)](LICENSE)
[![Three.js](https://img.shields.io/badge/3D_Engine-Three.js_r128-blue.svg)](https://threejs.org/)
[![Leaflet.js](https://img.shields.io/badge/Geographic_GIS-Leaflet_1.9.4-green.svg)](https://leafletjs.com/)
[![DGCA](https://img.shields.io/badge/DGCA-Green_Corridor_Compliant-orange.svg)](https://digitalsky.dgca.gov.in/)

> **MediLift** is an autonomous organ delivery drone system designed for Green Corridor missions in India. It enables rapid, traffic-free transportation of donated organs (hearts, kidneys, livers) between inbound airports and transplant hospitals in minutes with sub-15 cm precision optical landing.

---

## 🌟 Key Features

### 1. 3D Flight Physics & Potential Field Obstacle Avoidance
- **6-DOF Rigid-Body Dynamics**: Real-time simulation of lift, drag, ground-effect aerodynamics, and motor thrust dynamics.
- **3D Potential Field Obstacle Avoidance**: Continuous repulsive vector field mathematics ($\vec{F}_{\text{rep}}$) preventing collisions with ATC towers, terminal concourses, and city high-rises.
- **Precision Local-Frame Touchdown**: Body-axis coordinate rotation ensuring sub-15 cm touchdown accuracy on elevated hospital rooftop helipads.
- **Full Round-Trip Flight**: Autonomous Outbound (Airport ➔ Hospital) and Vice-Versa (Hospital ➔ Airport RTB) mission cycles.

### 2. Realistic 3D Metropolitan Environment
- **Sardar Vallabhbhai Patel International Airport (AMD)**:
  - 400m Runway 23 with active runway lighting & centerline markings.
  - Terminal 2 concourse with passenger boarding jetways and realistic commercial airliners (Airbus A320 / Boeing 737 models with swept wings, turbofan engines, and landing gear).
  - 38m ATC Control Tower with rotating radar dish.
- **Ahmedabad Civil Hospital (IKDRC Medicity Campus)**:
  - 10-story Institute of Kidney Diseases & Research Centre with elevated rooftop helipad platform ($y = 37.62\text{m}$).
  - UN Mehta Cardiology Institute & GCRI Cancer Wings.
  - Active 108 Emergency Ambulance bay with flashing beacons.
- **Sabarmati River & Historic Landmarks**:
  - Deep-water channel spanned by cable-stayed bridges.
  - Shahibaug Moti Shahi Mahal (Sardar Patel Memorial) historic sandstone dome architecture.
  - Highway network with moving vehicular traffic.

### 3. Real Geographic GPS Airway (Leaflet.js GIS)
- **5.42 km DGCA Airway**: SVP Airport (`23.0772°N, 72.6289°E`) to Civil Hospital (`23.0525°N, 72.6042°E`).
- **Satellite, Clean Street, and Tactical Dark** map layer modes.
- **Live UAV Telemetry Stream**: Altitude AGL, ground speed, battery SoC, and active bio-pod temperature ($4.0^\circ\text{C} \pm 0.1^\circ\text{C}$).

### 4. Open-Source Hardware Architecture (Indian Sourcing)
- **Frame**: 3×3 ft (91×91 cm) Spacedrone X8 Octocopter in 3K carbon fiber.
- **Motors**: 8× T-Motor MN501-S 300KV with 30" carbon propellers.
- **Flight Controller**: Pixhawk 6X with ArduCopter 4.4 firmware (Triple redundant IMU).
- **Telemetry**: RFD900x 900MHz Long-Range Radio + 4G LTE failover.
- **Battery**: Dual Li-Ion 6S 30,000mAh (Samsung 21700 cells) providing 35 min endurance.
- **Bio-Pod**: Peltier-cooled thermo-electric container keeping organs at $4.0^\circ\text{C}$.

---

## 🚀 Quickstart

### Running Locally
MediLift requires no complex build tools or heavy runtimes. It is built purely with HTML5, CSS3, Three.js, and Leaflet.js.

```bash
# Clone the repository
git clone https://github.com/Maahirrrr/MediLift.git
cd MediLift

# Start a local static HTTP server
python -m http.server 8000
```

Open your browser and navigate to:
- **Landing Page & GPS Airway**: `http://localhost:8000/index.html`
- **3D Flight Simulator**: `http://localhost:8000/simulator.html`

---

## 📱 Mobile UI/UX Controls

- **Desktop**:
  - `W / S`: Pitch Forward / Backward
  - `A / D`: Roll Left / Right
  - `Arrow Up / Down`: Altitude / Throttle Up / Down
  - `Arrow Left / Right`: Yaw Heading Left / Right
- **Mobile Devices**:
  - On-screen touch D-Pad controls.
  - Collapsible avionics telemetry drawer.
  - Touch-drag to orbit camera and pinch-to-zoom.

---

## 📄 License
MIT License. Open-sourced for healthcare innovation and emergency organ logistics.
