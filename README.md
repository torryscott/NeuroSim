# NeuroSim

Interactive, single-file HTML demos for the foundational chapters of an introductory neuroscience or biological psychology course. Each page is a small simulation with a plain-language narrator, built to be projected in class and then handed to students to explore on their own.

## Demos

| Page | What it shows |
|---|---|
| [1 · Nernst Tug-of-War](https://torryscott.github.io/NeuroSim/nernst-tug-of-war.html) · [source](nernst-tug-of-war.html) | One ion, one selective channel, two opposing pushes. Ions cross until the diffusion push and the electrical pull cancel at the equilibrium (Nernst) potential. |
| [2 · Resting Potential Tug-of-War](https://torryscott.github.io/NeuroSim/resting-potential.html) · [source](resting-potential.html) | K⁺, Na⁺ and Cl⁻ channels each pull the membrane toward their own equilibrium potential, weighted by how many are open, while the Na⁺/K⁺ pump keeps the gradients up. |
| [3 · Action Potential Tug-of-War](https://torryscott.github.io/NeuroSim/action-potential.html) · [source](action-potential.html) | The Hodgkin–Huxley equations with visible channel gates, TTX and TEA, pulse pairs for the refractory period, and a voltage clamp. |

Each file is self-contained: no build step and no dependencies beyond two Google Fonts. Every page opens in a **Simple view** for first-time learners; **Show more** reveals the extra controls.

## Teaching with the Nernst page

- **Present** (button or `P`) switches to a one-screen layout with large type, sized for a projector, and goes full screen when the browser allows it. `Esc` or the button exits.
- **Shortcuts** work even after clicking a control: `space` play or pause, `C` let one ion cross, `R` reset, `P` present.
- **Challenges** give students five goals that check themselves, from finding the balance point to the anion puzzle. Progress is kept in the student's browser.
- **Predictions**: clicking the voltage plot marks a guess, and the plot reports how far off it was once the membrane settles.
- **Setup links** open the page in a chosen state, so a slide or an assignment can start students somewhere specific. Use **Copy a link to this setup** under Show more, or write one by hand:

| Parameter | Values |
|---|---|
| `ion` | `K`, `Na`, `Cl`, `Ca` |
| `in`, `out` | concentrations in mM |
| `gate` | `1` open, `0.5` half open, `0` closed |
| `vm`, `hold` | a starting voltage in mV; add `hold=1` to clamp it |
| `tiny` | `1` for the tiny-box mode |
| `temp`, `step`, `speed` | °C; mV per ion (`6`, `3`, `1.5`); `0.5` to `4` |
| `view`, `present`, `play` | `view=full`, `present=1`, `play=1` |

Example: [`nernst-tug-of-war.html?ion=Cl&out=50&view=full`](https://torryscott.github.io/NeuroSim/nernst-tug-of-war.html?ion=Cl&out=50&view=full)

## About the models

- **Nernst:** crossing rates follow a single-barrier (Eyring) rate model, so traffic in the two directions balances exactly at the Nernst potential. Both pushes are shown per unit of charge, so they compare directly with the membrane voltage. The ions that have crossed wear a ring; in a real 20 µm cell they would be about 1 in 50,000 of its K⁺, a figure the page computes. The optional tiny-box mode lets the concentrations follow the crossings to show what would happen if the cell really were as small as the picture.
- **Resting potential:** each open channel passes current in proportion to its driving force (the equivalent-circuit model), so the membrane settles at the conductance-weighted average of the equilibrium potentials, shifted a few millivolts by the pump.
- **Action potential:** the original Hodgkin–Huxley equations with the series' equilibrium potentials and kinetics sped up toward body temperature. Threshold, spike shape, undershoot and refractory period emerge from the equations.

Ion counts on screen, membrane capacitance and time scales are cartoon-scaled where noted on each page; concentrations are typical textbook values for a mammalian neuron.
