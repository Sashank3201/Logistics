# Railgrid

A live 3D metro control dashboard for a fictional Green Line, built as a single HTML file with Three.js.

Open `index.html` in a modern browser. It loads Three.js r160 from jsDelivr and the fonts from Google Fonts, so it needs a network connection.

## What it simulates

- A clay-style diorama: an elevated double-track line on pillars, four stations (Westgate, Foundry Road, Market Square, Harbour Park) with platforms, escalators, lifts and glass canopies, a tied-arch river bridge, the J1 junction and the Northfield Depot (wash plant, stabling roads, maintenance shed), roads with signalled junctions, and city blocks.
- Trains run both ways to a 72 s headway. They brake into stations, open their doors, let passengers alight and board, then leave when the starter signal clears.
- Three-aspect block signals react to occupancy. The J1 junction signal lights its route indicator when a train is routed to the depot.
- Every few minutes a train terminates at Market Square, runs through the wash plant and stables, and a stabled train is released into service.
- Road traffic follows the cars ahead and stops at the junction lights. Trains, cars and crossing traffic are kept apart by the signalling and following logic, so nothing overlaps.
- Conditions: Clear, Monsoon (rain, wet surfaces, a 43 km/h limit, longer dwells), Fog (low visibility, 55 km/h caution running) and Festival rush (bigger crowds, 58 s headway, extra trains, lanterns and fireworks at night).
- An animated day/night switch with lit windows, lit carriages and station glow.

## Controls

| Action | Mouse / keyboard | Touch |
| --- | --- | --- |
| Pan | Drag, or arrow keys / WASD | One-finger drag |
| Rotate and tilt | Right-drag (or Shift/Ctrl + drag), Q / E | Two-finger twist |
| Zoom | Scroll, `+` / `-` | Pinch |
| Inspect | Click a train, station, signal or the depot | Tap |
| Follow selected train | `F` or the Follow button | Follow button |
| Areas | `1`–`6` or the area switcher | Area chips |
| Night mode | `N` or the sun/moon switch | Switch |
| Search | `/` | Search button |
| Clear selection | `Esc` | Close button |

The clock starts at your local time. The speed button cycles through 1×, 2×, 4× and pause.
