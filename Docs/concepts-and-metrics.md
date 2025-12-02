\# Concepts \& Metrics



This document connects Ω Engine’s visual behavior to the Invocation Science® constructs (AIA, OIS, Φ, Ψ).



\## 1. State \& Wells



Ω-space state: `s(t) = (x, y, z)`.



\### 1.1 AIA Wells

Each AIA well has:

\- Position `(x\_w, y\_w, z\_w)`

\- Strength `α\_w`



Force from a well (simplified):

\- `F\_w ∝ -α\_w (s - w) / ||s - w||²`



Triwell / single-well configurations are controlled via UI.



---



\## 2. Local Metrics



Given `s(t)` and `s(t-1)`:



\- \*\*τ (step distance)\*\*  

&nbsp; `τ(t) = ||s(t) - s(t-1)||`



\- \*\*Echo λ\*\*  

&nbsp; `λ(t) = s(t) · s(t-1)`



\- \*\*Curvature κ\*\*  

&nbsp; Model-specific; in Ω V3 a simple quadratic form in (x, y, z) is used.



\- \*\*Contraction Π\*\*  

&nbsp; Local inverse distance weighting scaled by user-selected Π.



---



\## 3. OIS-Aligned Metrics



Even when only Ω coordinates are available, we approximate:



\### 3.1 D(t) — Drift



In Ω, we treat:



```text

D(t) ≈ τ(t) = ||s(t) - s(t-1)||



