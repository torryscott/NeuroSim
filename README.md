# NeuroSim

Interactive, single-file HTML demos for the foundational chapters of an introductory neuroscience or biological psychology course. Each page is a small simulation with a plain-language narrator, built to be projected in class and then handed to students to play with.

## Demos

| Page | What it shows |
|---|---|
| [Nernst Tug-of-War](https://torryscott.github.io/NeuroSim/nernst-tug-of-war.html) · [source](nernst-tug-of-war.html) | One ion, one selective channel, two opposing pushes. Ions cross until the membrane voltage settles where the diffusion push and the electrical pull cancel: the equilibrium (Nernst) potential. |

More pages in the series (resting potential, action potential, synaptic potentials) are planned.

## Using a demo

Every demo is one self-contained `.html` file with no build step and no dependencies beyond two Google Fonts. Click a page link above to launch it (the repository is served by GitHub Pages at https://torryscott.github.io/NeuroSim/), or download the file and open it in any modern browser.

Each page opens in a **Simple view** for first-time learners; **Show more** reveals the extra controls (temperature, voltage clamp, the worked Nernst equation, real-cell ion counts). Ions can be dragged through the channel by hand, the channel can be clicked open or shut, and the membrane voltage can be set directly.

## About the model

Crossing rates follow a single-barrier (Eyring) rate model, so the two directions balance exactly at the Nernst potential. The membrane voltage follows the average of many random crossings and moves smoothly; *Next ion* shows the individual random events. The membrane capacitance is cartoon-scaled so that each ion visibly moves the voltage, and the ion counts on screen are cartoon-scaled too; a real 20 µm cell moves only about 1 in 50,000 of its K⁺ to reach E<sub>K</sub>, a number the page computes for you. Concentrations are typical textbook values for a mammalian neuron.
