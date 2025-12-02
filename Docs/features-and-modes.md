

---



\## 5. docs/features-and-modes.md



```markdown

\# Features \& Modes



\## 1. Renderers



\### 1.1 2D Canvas (Default)

\- Robust, portable, no GPU requirement.

\- Draws:

&nbsp; - AIA wells

&nbsp; - Worldlines

&nbsp; - Regime-colored trails

&nbsp; - Phase snapshots



\### 1.2 WebGL (Beta)

\- Uses line strips for multiple worldlines.

\- Per-run and per-regime coloring.

\- Automatically falls back to 2D if WebGL is unavailable.



Renderer can be switched via a dropdown: \*\*Renderer: 2D | WebGL (beta)\*\*.



---



\## 2. Modes



\### 2.1 Ω Demo



\- Synthetic worldlines driven by:

&nbsp; - AIA well configuration (triwell / single well, strength, bias).

&nbsp; - κ curvature gain.

&nbsp; - λ echo coupling.

&nbsp; - Π contraction weight.

\- Sliders + toggles control physics parameters.

\- Scenario presets:

&nbsp; - Default Balanced

&nbsp; - Strong Π Collapse

&nbsp; - High-λ Turbulence

&nbsp; - Symmetric Triwell Orbit

&nbsp; - Boundary-free Convergence



\### 2.2 Imported LLM worldline



\- Load JSON output from OIS / Φ / Ψ or other tools.

\- Ω:

&nbsp; - Centers embeddings.

&nbsp; - Projects them into 3D Ω-space.

&nbsp; - Scales into a compact radius.

\- Uses metrics if available; otherwise approximates D, ICI, Ĵ, ASH from coordinates.



\### 2.3 Live OIS



\- Ω exposes `window.omegaIngestOISStep(...)`.

\- External experiments (OIS emulator, Ψ console) call it for each step.

\- Ω draws worldlines and updates metrics in real time.



---



\## 3. Visual Layers



\- \*\*Worldlines\*\*: Position in Ω-space over time.

\- \*\*AIA wells\*\*: Circles marking attractor basins.

\- \*\*Regime coloring\*\*:

&nbsp; - Falling inward

&nbsp; - Orbiting

&nbsp; - Shearing

&nbsp; - Transitional

\- \*\*Regime timeline strip\*\*:

&nbsp; - Horizontal bar colored by regime over t.

&nbsp; - Hover or click to scrub to that moment.

\- \*\*Phase snapshots\*\*:

&nbsp; - Auto-captured when regime changes.

&nbsp; - Click to jump to that snapshot.



---



\## 4. Metrics Surface



Per primary run, HUD shows:



\- τ — step distance

\- λ — echo (dot product with previous step)

\- κ — curvature (Ω-defined)

\- Π — contraction weight applied to local contraction



OIS-aligned metrics:



\- D(t) — drift ≈ τ

\- ICI(t) — coherence index (0–1)

\- Ĵ(t) — contraction estimator

\- ASH — low-rank basin fingerprint



Details: `concepts-and-metrics.md`.



