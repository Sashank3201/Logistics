# Railgrid

A live 3D metro control dashboard for a fictional city with two elevated lines. It is a single HTML file built with Three.js.

Open `index.html` in a modern browser. It loads Three.js r160 from jsDelivr and the fonts from Google Fonts, so it needs a network connection. Live version: https://sashank3201.github.io/Logistics/

## The city

- A clay-style city of about 4.5 km by 3 km. It has a downtown of towers, an old town, residential and industrial districts, a river with road bridges, Central Park, City Stadium, City University and the Docklands container yard. Hills at the edges hide the tunnel portals.
- **Green Line** (Airport ⇄ Seaview), 9 stations: Westgate, Mill Quarter, Foundry Road, Old Town, Market Square, Harbour Park, Central, Lighthouse Road, Eastpoint. It crosses the river on a tied-arch bridge.
- **Silver Line** (Hillcrest ⇄ Bayview), 7 stations: Northgate, University, Tech Park, Central, Stadium, Docklands, Southbay. It runs on a higher viaduct and spans the Green Line at the Central interchange.
- **Northfield Depot** (Green): wash plant, two stabling roads and a maintenance shed.
- **Riverside Maintenance Centre** (Silver): wash plant, four stabling roads, a heavy-maintenance shed with lifting jacks, a wheel lathe and a test track.

## What it simulates

- 30 trains run both ways to a 100 s timetable. They brake into stations, open their doors, let passengers alight and board, then leave when the starter signal clears.
- Three-aspect block signals react to occupancy, and junction signals show a route indicator when a train is routed to a depot.
- Trains rotate through the wash plants. A train is booked for washing, terminates at the station before the depot junction, washes, then stables. A stabled train is released through the depot link tunnel when the timetable needs it.
- Four trains are in the workshops on planned work orders (bogie swap on lifting jacks, door overhaul, test runs).
- Road traffic follows the cars ahead and stops at signalled junctions. Trains, cars and crossing traffic are kept apart by the signalling and following logic, so nothing overlaps.
- Conditions: Clear, Monsoon (rain, wet surfaces, 43 km/h limit, longer dwells), Fog (low visibility, 55 km/h caution running) and Festival rush (bigger crowds, 75 s headway, extra trains, lanterns and fireworks at night).
- An animated day/night switch with lit windows, lit carriages and station glow.

## Ride a train

Press **Ride** (or `R`) to board a train. If a train is selected you board that one, otherwise you board the nearest one in service. The train drives itself on the timetable. You watch from one of three cameras:

- **Cab:** the driver's view along the track, with the signals ahead.
- **Chase:** behind and above the train.
- **Window:** a passenger seat looking out at the city.

A route strip shows the stops. The driver's display shows speed, next stop, distance, the signal ahead and door side. Announcements name each arrival. Before a train enters a tunnel portal you move to another train automatically, or you can press **Next train** (`T`).

## Controls

| Action | Mouse / keyboard | Touch |
| --- | --- | --- |
| Pan | Drag, or arrow keys / WASD | One-finger drag |
| Rotate and tilt | Right-drag (or Shift/Ctrl + drag), Q / E | Two-finger twist |
| Zoom | Scroll, `+` / `-` | Pinch |
| Inspect | Click a train, station, signal or depot | Tap |
| Follow selected train | `F` or the Follow button | Follow button |
| Areas | Overview / Green Line / Silver Line / Depots & places menus, `0` for the overview | Areas button |
| Ride | `R` or Ride; in a ride `1` `2` `3` switch camera, `T` next train, `Esc` exit | Ride button |
| Hide panels | `H` or the eye button | Hide button |
| Night mode | `N` or the sun/moon switch | Switch |
| Search | `/` | Search button |
| Clear selection | `Esc` | Close button |

On a phone, the tables open as a sheet above the bottom bar. Close them with the Close button or by tapping the map.

The clock starts at your local time. The speed button cycles through 1×, 2×, 4× and pause.
