\# Live OIS Streaming Example



With Ω Engine V3 open in the browser, you can simulate a live OIS run from the console:



```js

// Example: simple “falling inward” run

for (let t = 0; t < 10; t++) {

&nbsp; const emb = \[0.01 \* t, -0.01 \* t, 0.02 \* t];

&nbsp; const D = t === 0 ? 0 : 0.02 / (t + 1);

&nbsp; const ICI = 0.75 + 0.02 \* Math.min(t, 10);

&nbsp; const Jhat = t <= 1 ? 1.0 : 0.9;

&nbsp; const ASH = "live-demo";



&nbsp; window.omegaIngestOISStep({

&nbsp;   meta: {

&nbsp;     run\_id: "live-ois-demo",

&nbsp;     model: "gpt-4.1",

&nbsp;     protocol: "OIS-v1"

&nbsp;   },

&nbsp;   emb,

&nbsp;   metrics: { D, ICI, Jhat, ASH }

&nbsp; });

}



