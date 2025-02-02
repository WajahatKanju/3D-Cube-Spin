# 3D-Cube-Spin

This project integrates a Swiper carousel with a cube effect and animated particles using the tsParticles library.

## Features

- **Swiper Carousel**: A cube-style, looping carousel with autoplay and smooth transitions.
- **tsParticles**: Dynamic particle effects in the background with customized shapes, movement, and destruction.

## Installation

To get this project up and running, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/yourrepository.git
cd yourrepository
```

### 1. Install Dependencies
Ensure you have Swiper and tsParticles libraries installed. You can install them via npm:


```bash
npm install swiper tsparticles

```

Or include the CDN links in your HTML file:

```bash
<!-- Swiper CSS -->
<link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.min.css" />

<!-- Swiper JS -->
<script src="https://unpkg.com/swiper/swiper-bundle.min.js"></script>

<!-- tsParticles JS -->
<script src="https://cdn.jsdelivr.net/npm/tsparticles"></script>

```

### 3   . Initialize Swiper and tsParticles
Add the following JavaScript code to your project to initialize Swiper and tsParticles:

```javascript
// Initialize Swiper
var swiper = new Swiper(".swiper", {
  effect: "cube",
  grabCursor: true,
  loop: true,
  speed: 1000,
  cubeEffect: {
    shadow: false,
    slideShadows: true,
    shadowOffset: 10,
    shadowScale: 0.94,
  },
  autoplay: {
    delay: 2600,
    pauseOnMouseEnter: true,
  },
});

// Initialize tsParticles
tsParticles.load("tsparticles", {
  fpsLimit: 60,
  backgroundMode: {
    enable: true,
    zIndex: -1,
  },
  particles: {
    number: {
      value: 30,
      density: {
        enable: true,
        area: 800,
      },
    },
    color: {
      value: [
        "#3998D0",
        "#2EB6AF",
        "#A9BD33",
        "#FEC73B",
        "#F89930",
        "#F45623",
        "#D62E32",
      ],
    },
    destroy: {
      mode: "split",
      split: {
        count: 1,
        factor: {
          value: 5,
          random: {
            enable: true,
            minimumValue: 4,
          },
        },
        rate: {
          value: 10,
          random: {
            enable: true,
            minimumValue: 5,
          },
        },
        particles: {
          collisions: {
            enable: false,
          },
          destroy: {
            mode: "none",
          },
          life: {
            count: 1,
            duration: {
              value: 1,
            },
          },
        },
      },
    },
    shape: {
      type: "circle",
    },
    size: {
      value: 8,
      random: {
        enable: true,
        minimumValue: 4,
      },
    },
    collisions: {
      enable: true,
      mode: "destroy",
    },
    move: {
      enable: true,
      speed: 7,
      out_mode: "out",
    },
  },
  detectRetina: true,
});


```

## Customization
You can further customize both the Swiper carousel and tsParticles by adjusting their settings:

Swiper Settings: Change the effect, speed, autoplay delay, and cube effect properties in the Swiper initialization.
tsParticles Settings: Adjust particle numbers, colors, sizes, movement, and collision behavior.