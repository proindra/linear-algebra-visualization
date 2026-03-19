# Linear Algebra Visualization

An interactive 3D visualization of core linear algebra concepts, built with [Three.js](https://threejs.org/) and [Tailwind CSS](https://tailwindcss.com/).

🔗 **Live Demo**: [https://proindra.github.io/linear-algebra-visualization](https://proindra.github.io/linear-algebra-visualization)

---

## Visualizations

| Tab | Topic | What you see |
|-----|-------|-------------|
| 1 | **Orthogonal Vectors** | Two vectors x and y in ℝ³ with xᵀy = 0, right-angle marker |
| 2 | **Subspace Types** | All four subspace dimensions in ℝ³ — point, line, plane, full space |
| 3 | **1D Ortho Subspaces** | Two orthogonal lines S and T through the origin |
| 4 | **Intersecting Planes** | Two 2D planes sharing a line — proof that planes can't be orthogonal in ℝ³ |
| 5 | **Orthogonal Complement** | A 1D subspace V (blue line) and its complement V⊥ (red plane) |

---

## Controls

- **Orbit** — click and drag to rotate the scene
- **Zoom slider** — drag right to zoom in, left to zoom out (shows % indicator)
- **Auto-rotate** — scene rotates automatically; orbit drag pauses it
- **Tab buttons** — switch between visualizations

---

## Tech Stack

- [Three.js r134](https://threejs.org/) — 3D WebGL rendering (local copy)
- [OrbitControls.js](https://threejs.org/docs/#examples/en/controls/OrbitControls) — camera orbit (local copy)
- [Tailwind CSS](https://tailwindcss.com/) — UI styling via CDN
- Pure HTML/CSS/JS — no build step required

---

## Project Structure

```
├── math.html          # Main app (single file)
├── three.min.js       # Three.js r134 (local)
├── OrbitControls.js   # Three.js OrbitControls (local)
└── .github/
    └── workflows/
        └── deploy.yml # GitHub Pages auto-deploy
```

---

## Local Development

No build step needed. Just open `math.html` directly in a browser, or serve it with any static server:

```bash
# Python
python -m http.server 8080

# Node
npx serve .
```

Then open `http://localhost:8080/math.html`.

---

## Deployment

Pushes to the `main` branch automatically deploy to GitHub Pages via the included GitHub Actions workflow.

The live site is served from the `gh-pages` branch at:
`https://proindra.github.io/linear-algebra-visualization`
