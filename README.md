<div align="center">

# Integral Studio

**A hands-on calculus playground for area, slope, and accumulation.**

[Open `index.html`](index.html) · No build step · No dependencies

</div>

![Integral Studio preview](docs/preview.png)

## Three views, one curve

Integral Studio keeps the same function and interval across three linked views:

| View | What it shows |
| --- | --- |
| **Area** | Riemann sums with left, right, midpoint, trapezoid, and Simpson methods |
| **Slope** | A secant that tightens into the tangent as `h → 0` |
| **Accumulate** | The area function `F(x)` and the Fundamental Theorem in motion |

## Things to try

- Drag the **a** and **b** handles on the graph, or type exact bounds.
- Type `2x`, `sin(x)^2`, `e^(-x^2)`, or `1/(1+x^2)` directly.
- Change the number of slices and watch the error shrink.
- Toggle **Average value** to compare the mean height with the curve.
- Use the three prompt cards for animated mini-tours.

## Controls

| Action | How |
| --- | --- |
| Change the function | Edit the expression field or pick a preset |
| Move bounds | Drag the blue and coral handles, or edit `a` / `b` |
| Change slices | Drag the slider or use the `−` / `+` buttons |
| Switch methods | Use the Left, Right, Mid, Trap, and Simp tabs |
| Explore slope | Pick **Slope**, then drag `x₀` or the secant endpoint |
| Explore accumulation | Pick **Accumulate**, then drag the `x` line |
| Reset | Use the **Reset** button in the top right |

The expression parser accepts `+ − × ÷ ^`, implicit multiplication, `pi`, `e`, `tau`, and functions such as `sin`, `cos`, `tan`, `exp`, `ln`, `sqrt`, and `abs`. Keyboard focus styles are included throughout.

## Under the hood

- Single-file HTML, CSS, and vanilla JavaScript
- Hand-written recursive-descent expression parser
- Canvas rendering for the curve, panels, tangents, and accumulation
- Composite Simpson reference integral for live error comparison
- Responsive layout with reduced visual clutter on small screens

Google Fonts load when available; local serif and sans-serif fallbacks keep the page usable offline.

## Run locally

```bash
git clone https://github.com/pbaruah1/integral-studio.git
cd integral-studio
open index.html   # macOS
# or: start index.html   (Windows)
```

You can also serve the folder with any static server:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Project structure

```text
.
├── index.html      # the entire app
├── docs/
│   └── preview.png # README preview
└── README.md
```
