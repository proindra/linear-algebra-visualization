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
| 6 | **Projection** | Project vector b onto a line or plane — shows p (projection) and e (error vector) |
| 7 | **Fundamental Subspaces** | Interactive SVG diagram of the four fundamental subspaces of a matrix A — row space, nullspace, column space, left nullspace — with hover highlights and 3D card rotation |

---

## Controls

- **Orbit** — click and drag to rotate the 3D scene
- **Zoom slider** — drag right to zoom in, left to zoom out (shows % indicator)
- **Auto-rotate** — scene rotates automatically; orbit drag pauses it
- **Tab buttons** — switch between visualizations using the numbered sidebar
- **Onto Line / Onto Plane** — toggle projection mode in Tab 6
- **Tab 7 card drag** — click and drag the diagram to rotate it in 3D; hover regions to highlight subspace mappings

---

## Features

- Black 3D canvas background for maximum contrast
- Outlined 3D labels — stay readable even when overlapping during rotation
- Compact side panel — all info visible without scrolling
- Redesigned sidebar with numbered badge tabs and active accent bar
- Gradient "Linear Algebra" title in the panel
- Tab 7 uses an interactive SVG overlay (not Three.js) with hover-based opacity highlighting
- 3D rotatable card for the fundamental subspaces diagram
- Mobile responsive — panel on top, canvas below; 3-column tab grid on small screens
- Auto-deploy to GitHub Pages on every push to `main`

---

## Tech Stack

- [Three.js r134](https://threejs.org/) — 3D WebGL rendering (local copy)
- [OrbitControls.js](https://threejs.org/docs/#examples/en/controls/OrbitControls) — camera orbit (local copy)
- [Tailwind CSS](https://tailwindcss.com/) — UI styling via CDN
- Pure HTML/CSS/JS — no build step required

---

## Project Structure

```
├── math.html                        # Main app (single file)
├── index.html                       # Copy of math.html served by GitHub Pages
├── three.min.js                     # Three.js r134 (local)
├── OrbitControls.js                 # Three.js OrbitControls (local)
├── four_fundamental_subspaces.jsx   # Original JSX reference design for Tab 7
└── .github/
    └── workflows/
        └── deploy.yml               # GitHub Pages auto-deploy
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

Pushes to `main` automatically deploy to GitHub Pages via the included GitHub Actions workflow. `math.html` is synced to `index.html` on every push since GitHub Pages serves `index.html` by default.

Live site: `https://proindra.github.io/linear-algebra-visualization`
