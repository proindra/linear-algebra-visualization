# Linear Algebra Visualizer

An interactive 3D tool to learn linear algebra visually — orthogonal vectors, dot product, matrix transformations, projection matrices, weighted least squares, and the four fundamental subspaces. Built with [Three.js](https://threejs.org/), pure HTML/CSS/JS, no build step.

🔗 **Live Demo**: [https://proindra.github.io/linear-algebra-visualization](https://proindra.github.io/linear-algebra-visualization)

---

## Visualizations

| Tab | Topic | What you see |
|-----|-------|-------------|
| 1 | **Orthogonal Vectors** | Two vectors x and y in ℝ³ with xᵀy = 0, dot product = 0, right-angle marker |
| 2 | **Subspace Types** | All four subspace dimensions in ℝ³ — point, line, plane, full space |
| 3 | **1D Ortho Subspaces** | Two orthogonal lines S and T through the origin |
| 4 | **Intersecting Planes** | Two 2D planes sharing a line — proof that planes can't be orthogonal in ℝ³ |
| 5 | **Orthogonal Complement** | A 1D subspace V (blue line) and its complement V⊥ (red plane) |
| 6 | **Projection** | Project vector b onto a line or plane — shows p (projection) and e (error vector); includes Cauchy-Schwarz inequality and projection matrix P with remarks |
| 7 | **Least Squares** | Two sub-modes: **Least Squares Line** — yellow data points, teal fitted line `Ax̂ = A(AᵀA)⁻¹Aᵀb = Pb`, red residual bars; **Weighted** — same scene with sphere size = weight and weighted normal equations `(AᵀWᵀWA)x̂_W = AᵀWᵀWb` |
| 8 | **Fundamental Subspaces** | Interactive SVG diagram of the four fundamental subspaces of matrix A — row space, nullspace, column space, left nullspace — with rank-nullity theorem, hover highlights, and 3D card rotation |

---

## Controls

- **Orbit** — click and drag to rotate the 3D scene
- **Zoom slider** — drag right to zoom in, left to zoom out (shows % indicator)
- **Auto-rotate** — scene rotates automatically; orbit drag pauses it
- **Tab buttons** — switch between visualizations using the numbered sidebar
- **Onto Line / Onto Plane** — toggle projection mode in Tab 6
- **Least Squares Line / Weighted** — toggle sub-modes in Tab 7
- **Tab 8 card drag** — click and drag the diagram to rotate it in 3D; hover regions to highlight subspace mappings

---

## Features

- Interactive 3D vector and matrix transformation visualization
- Orthogonal vectors and dot product visualization
- Projection matrix visualization (onto line and plane) with collapsible remarks
- Least squares visualization — Least Squares Line (`Ax̂ = Pb`) and Weighted Least Squares with sub-mode toggle
- Four fundamental subspaces with rank-nullity theorem
- Outlined 3D labels — readable even when overlapping during rotation
- Compact side panel with numbered badge tabs and active accent bar
- Tab 8 uses an interactive SVG overlay with hover-based opacity highlighting
- 3D rotatable card for the fundamental subspaces diagram
- Full SEO optimization — meta tags, Open Graph, Twitter Card, JSON-LD structured data
- Custom SVG favicon
- Mobile responsive — panel on top, canvas below; 3-column tab grid on small screens
- Auto-deploy to GitHub Pages on every push to `main`

---

## Tech Stack

- [Three.js r134](https://threejs.org/) — 3D WebGL rendering (local copy)
- [OrbitControls.js](https://threejs.org/docs/#examples/en/controls/OrbitControls) — camera orbit (local copy)
- [Inter](https://fonts.google.com/specimen/Inter) — UI font via Google Fonts
- Pure HTML/CSS/JS — no build step, no framework, no bundler

---

## Project Structure

```
├── math.html                        # Main app (single file)
├── index.html                       # Copy of math.html served by GitHub Pages
├── three.min.js                     # Three.js r134 (local)
├── OrbitControls.js                 # Three.js OrbitControls (local)
└── .github/
    └── workflows/
        └── deploy.yml               # GitHub Pages auto-deploy
```

---

## Local Development

No build step needed. Just open `math.html` directly in a browser, or serve with any static server:

```bash
# Python
python -m http.server 8080

# Node
npx serve .
```

Then open `http://localhost:8080/math.html`.

---

## Deployment

Pushes to `main` automatically deploy to GitHub Pages via the included GitHub Actions workflow. `math.html` is synced to `index.html` before every push since GitHub Pages serves `index.html` by default.

Live site: `https://proindra.github.io/linear-algebra-visualization`
