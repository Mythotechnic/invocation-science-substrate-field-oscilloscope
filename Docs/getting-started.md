\# Getting Started with Ω Engine V3



Ω Engine is a \*\*standalone HTML application\*\*. No build step, no dependencies — just a browser.



\## 1. Open the Console



Option A — Direct:



1\. Open `src/omega-engine-v3.html` in a modern browser.

2\. Confirm you see:

&nbsp;  - A dark Ω field

&nbsp;  - A HUD with τ, λ, κ, Π

&nbsp;  - A control panel on the right



Option B — Local server (recommended for WebGL):



```bash

cd src

python -m http.server 8000

\# visit http://localhost:8000/omega-engine-v3.html



