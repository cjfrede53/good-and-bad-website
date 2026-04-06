# Assignment 10: Environmental Impact
**Course:** Computational Media and Arts Culture 240S
**Author:** CJ Frederickson

An exploration of how web design choices affect environmental impact. Two versions of the same site were built — one intentionally inefficient and energy-intensive, one optimized for minimal energy consumption — and their resource usage was measured and compared.

---

## Project Structure
ASSIGNMENT 10/
├── Bad Site/       # Inefficient site — SvelteKit app
└── Good Site/      # Efficient site — plain HTML/CSS

---

## Getting Started

### Good Site (Efficient)
No installation needed.

1. Open `Good Site/index.html` directly in your browser
2. Navigate to `post.html` to see a sample post

That's it — no server required.

---

### Bad Site (Inefficient)
Requires [Node.js](https://nodejs.org/) (v18 or higher recommended).

1. Navigate into the project folder:
```bash
   cd "Bad Site"
```

2. Install dependencies:
```bash
   npm install
```

3. Start the development server:
```bash
   npm run dev
```

4. Open your browser and go to:

http://localhost:5173

To build for production:
```bash
npm run build
npm run preview
```

---

## Energy Tracking

Both sites include an **EnergyBadge** feature that tracks and displays estimated energy usage in real time. On the Bad Site, this is implemented as a Svelte component (`src/lib/EnergyBadge.svelte`). On the Good Site, it is built directly into the HTML with vanilla JavaScript.

---

## Measuring Energy Usage

The following tools and metrics were used to compare the two sites:

| Tool | What it measures |
|---|---|
| Chrome DevTools → Network tab | Transfer size, number of requests |
| Chrome DevTools → Performance tab | CPU usage, scripting/rendering time |
| Lighthouse | Performance score, total blocking time |
| [Website Carbon Calculator](https://www.websitecarbon.com) | Estimated CO₂ per page visit |

---

## Key Design Differences

| Factor | Bad Site | Good Site |
|---|---|---|
| Framework | SvelteKit (JS bundle) | Plain HTML |
| Assets | Uncompressed images, multiple fonts | Minimal assets |
| Rendering | Client-side JS | Static |
| HTTP Requests | Many | Few |
| CSS | Large stylesheets | Minimal inline styles |

---

## Resources

- [The Staggering Ecological Impacts of Computation and the Cloud — MIT Press](https://thereader.mitpress.mit.edu/the-staggering-ecological-impacts-of-computation-and-the-cloud/)
- [How Do Websites Have a Carbon Footprint? — Kanoppi](https://kanoppi.co/how-do-websites-have-carbon-footprint/)
- [Minimal Computing in Web Design — NYU Libraries](https://guides.nyu.edu/digital-humanities/tools-and-software/web-design-minimal-computing)
- [Chrome DevTools: Network Tab](https://developer.chrome.com/docs/devtools/network)
