<div align="center">

# Planetary System

**An interactive, animated model of the Solar System — built with plain HTML, CSS and JavaScript. No frameworks, no build step.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript%20ES6-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Ionicons](https://img.shields.io/badge/Ionicons-3880FF?style=flat-square&logo=ionic&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![License](https://img.shields.io/badge/GPL--3.0-EAB308?style=flat-square)

[**View Live Demo**](https://epicode-ccc.vercel.app/)

</div>

---

## About the Project

**Planetary System** is a single-page web experience that puts the Sun and the eight planets in motion. Each body orbits on its own CSS-driven timing and spins on its axis; hitting pause freezes the system, aligns the planets and turns each one into a clickable target. Selecting a planet opens an information card with an image, a short profile and a link to further reading.

This is an **educational project**, written at the end of 2023 while attending a web development course. It was the first repository of the author and is deliberately kept in its original form: no framework, no bundler, no package manager — just three script files, one stylesheet and one HTML page. It remains published as a snapshot of that stage of the learning path, and as a compact demonstration of what can be done with the browser platform alone.

> **Note on language** — the interface copy, the planet descriptions and the reference links are in **Italian**.

---

## Preview

**Orbital view** — the system in motion, each body on its own orbit.

![Animated solar system in motion](assets/screen/screen.png)

**Paused view** — orbits stop, planets align and labels become interactive; selecting one opens its information card.

![Paused system with planet labels and an open information card](assets/screen/screen2.png)

---

## Features

- **Orbital animation** — every container rotates with an independent `animation-duration`, so inner bodies complete their orbit faster than outer ones. A second animation on the planet image itself produces the axial spin.
- **Play / Pause controls** — pausing stops the animation, repositions each body along a horizontal alignment and exposes a labelled button for every planet. Resuming closes any open card and returns the system to orbit.
- **Runtime-generated information cards** — clicking a planet (or its label) builds a card in the DOM from a single data source: cover image, title, description and an external reference link, with its own dismiss button.
- **Single source of truth** — planet names, copy, image paths, reference URLs and both the static and dynamic layout coordinates live in one `globalData` object, so content and positioning are edited in one place.
- **Responsive layout** — three breakpoints cover mobile, tablet and desktop viewports.
- **Preloader** — a loading indicator fades out on `window.onload` so the scene never appears half-rendered.
- **No build required** — the page runs straight from the filesystem; the only external assets are two CDN scripts.

---

## Architecture

```
planetary-system/
├── assets/
│   ├── imgCard/            # Cover images used inside the information cards
│   ├── screen/             # Screenshots used in this README
│   ├── bg.jpg              # Starfield background
│   ├── Universe-Logo.png   # Header logo
│   └── *.png               # Sprites for the Sun and the eight planets
├── css/
│   └── style.css           # Layout, orbital keyframes, responsive breakpoints
├── js/
│   ├── globaldata.js       # DOM references, preloader, planet dataset
│   ├── cards.js            # Information card creation and teardown
│   └── animation.js        # Play / pause controls and click handlers
├── index.html              # Single entry point
├── LICENSE
└── readme.md
```
---

## Contributors

<a href="https://github.com/AndreaMarangione/planetary-system/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=AndreaMarangione/planetary-system" alt="Contributors" />
</a>

Built by [@AndreaMarangione](https://github.com/AndreaMarangione) and [@giacomosx](https://github.com/giacomosx).

---

## License

Distributed under the **GNU General Public License v3.0**. See [`LICENSE`](LICENSE) for the full text.
