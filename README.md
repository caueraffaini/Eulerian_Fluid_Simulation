# Eulerian Fluid Simulation

A real-time 2D fluid simulation implemented in JavaScript, running directly in the browser. This project demonstrates **incompressible fluid dynamics** using the Eulerian method on a staggered grid.

## 🚀 Live Demo

**[Try the simulation here →](https://caueraffaini.github.io/Eulerian_Fluid_Simulation/)**

## ✨ Features

- **Multiple Simulation Modes:**
  - **Wind Tunnel** - Visualize airflow and vortex shedding around obstacles
  - **High-Resolution Tunnel** - Detailed pressure field visualization
  - **Tank** - Hydrostatic pressure simulation in a water tank
  - **Paint Mode** - Interactive fluid painting with dynamic colors

- **Visualization Options:**
  - Streamlines visualization
  - Velocity field vectors
  - Pressure field with scientific color mapping
  - Smoke/density visualization
  - Interactive obstacle placement

- **Real-time Interaction:**
  - Drag obstacles with mouse or touch
  - Responsive design for mobile devices
  - Live parameter adjustment

## 🎮 Controls

- **Mouse/Touch**: Drag to place and move obstacles
- **Buttons**: Switch between simulation scenarios
- **Checkboxes**: Toggle different visualization modes
- **Keyboard**: Press `P` to pause/unpause simulation

## 🔬 Technical Implementation

This simulation implements the **Navier-Stokes equations** for incompressible flow using:

- **Staggered Grid**: Velocity components stored at cell faces for numerical stability
- **Projection Method**: Enforces incompressibility through pressure projection
- **Semi-Lagrangian Advection**: Stable velocity and scalar field transport
- **Gauss-Seidel Iteration**: Solves the pressure Poisson equation
- **Over-relaxation**: Accelerates convergence (factor of 1.9)

### Key Physics Steps:
1. **Integration** - Apply external forces (gravity)
2. **Projection** - Solve for pressure to enforce incompressibility  
3. **Extrapolation** - Handle boundary conditions
4. **Advection** - Transport velocity and scalar fields

## 🚀 Getting Started

### Running Locally
1. Clone this repository:
   ```bash
   git clone https://github.com/caueraffaini/Eulerian_Fluid_Simulation.git
   ```

2. Open `index.html` in your web browser

### Deployment
This is a client-side application that can be deployed to any static hosting service like GitHub Pages, Netlify, or Vercel.

## 🎯 Simulation Scenarios

| Mode | Description | Physics Features |
|------|-------------|------------------|
| **Wind Tunnel** | Airflow around obstacles | Vortex shedding, smoke visualization |
| **Hires Tunnel** | High-resolution analysis | Detailed pressure fields, 200x resolution |
| **Tank** | Hydrostatic pressure | Gravity effects, pressure gradients |
| **Paint** | Interactive fluid art | Dynamic color mixing, creative mode |

## 🔧 Technical Specifications

- **Grid Resolution**: 50-200 cells (depending on mode)
- **Time Step**: 1/60 to 1/120 seconds
- **Solver Iterations**: 40-100 per frame
- **Boundary Conditions**: No-slip walls, inflow/outflow
- **Numerical Method**: Finite difference on staggered grid

## 🎨 Visualization Features

- **Scientific Color Mapping**: Blue → Cyan → Green → Yellow → Red
- **Pressure Visualization**: Real-time pressure field with accurate units (N/m²)
- **Streamline Tracing**: Particle path visualization
- **Vector Field Display**: Velocity magnitude and direction

## 🙏 Inspiration & Credits

This project is heavily inspired by:
- **[Ten Minute Physics](https://www.youtube.com/watch?v=iKAVRgIrUOU)** by Matthias Müller
- **[Original Implementation](https://github.com/matthias-research/pages/blob/master/tenMinutePhysics/17-fluidSim.html)** 

Based on the foundational work of:
- **Jos Stam** - "Real-Time Fluid Dynamics for Games"
- **Matthias Müller** - Simplified implementation approach

## 📱 Browser Compatibility

- Modern browsers with HTML5 Canvas support
- Mobile-friendly with touch controls
- Optimized for real-time performance

## 🛠️ Future Enhancements

- [ ] 3D fluid simulation
- [ ] Viscosity effects
- [ ] Compressible flow simulation
- [ ] WebGL acceleration
- [ ] Additional boundary conditions
- [ ] Turbulence modeling

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

**Enjoy exploring fluid dynamics! 🌊**
