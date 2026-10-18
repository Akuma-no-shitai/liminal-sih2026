# LIMINAL — SIH 2026, problem statement 26223

> **© 2026 Team LIMINAL. All rights reserved.** This repository is public only so that Smart India Hackathon 2026 evaluators can view the project. It is not open source: please do not copy, modify or reuse any part of it without written permission. See [LICENSE](LICENSE).

A drone swarm with no leader that maps a building before a disaster, searches it during, and measures what is left after.
This is the project's website, built as a story you scroll through, in eight acts that follow one building through a disaster.

## Open it

**Live site: [https://akuma-no-shitai.github.io/liminal-sih2026/](https://akuma-no-shitai.github.io/liminal-sih2026/)**

Open that link in Chrome or Edge. There is nothing to install. The first visit downloads about 24 MB, so wait a few seconds for the first screen. Use "Enter with sound" for the music.

**Prefer an offline copy?**
1. Click `index.html` in the file list above.
2. GitHub says the file is too big to show. That is normal; it is the whole site in one file. Click the **download icon** (the arrow pointing down, at the top right of the file box).
3. Open your Downloads folder and **double-click `index.html`**. It opens in Chrome or Edge, with no internet, no terminal and no install.

GitHub's own page cannot run the site; it only stores the file. Run the live link, or the downloaded copy.

`source.zip` is the code `index.html` is built from, file by file. You don't need it to view the site; download and unzip it to read.

## The eight acts, in the order a disaster runs
**The idea**
- **Act 1, "Someone is tapping"**: the hook and the idea. The first screen is a live school of drones that assembles the name while the page loads (your cursor is a predator). Then someone is tapping under the rubble: find them with a torch; why 72 hours matter, and why one swarm for before, during and after; what rescuers carry today and where each tool stops (damage is still graded by eye); one drone, then the swarm, map the building until β₀ counts the unexplored pockets down to zero; the person found at first light. Then six live disaster-zone scenes, each from a real event (an earthquake city block, the Silkyara tunnel, the Wayanad debris flow, the 2018 Kerala floods, a forest, the Tham Luang cave); "A collapse is a phase transition" (the same instruments that keep the swarm at its tipping point, pointed at a building); "After the rescue" (measure, then decide). It ends with the eight acts.

**Before (risk mitigation)**
- **Act 2, "Before it falls"**: peacetime. Eight drones survey an ordinary apartment block with no set route and build the baseline map that Act 7 later compares against. The map becomes a plan: an access graph (β₁ loops, weak links, dead ends), a published crowd model (Helbing, Farkas and Vicsek 2000) run with simulated occupancy to find the bottlenecks and test "faster is slower", percolation trials that measure how close the routes are to being cut, and three fixes computed again. A directed film of 2 min 38 s, then a sandbox: block doors, corridors and stair flights and run the crowd again.

**During (response)**
- **Act 3, "You are the drone"**: Layer 1, running. A collapsed floor with four people inside. Watch the autonomy fly it, or take the sticks.
- **Act 4, "Inside one drone"**: Layer 1 taken apart in 27 steps (or a 10-step quick tour for judges), each with a live simulation: the drone taken apart, the two brains, the flight controller down to its chips, the four MEMS sensors working inside their chips, vibration and the notch filter, sensor fusion and the Kalman gain, optical flow, cascaded PID, LiDAR and stop-and-scan, calibration and PnP, SLAM and loop closure, OctoMap, YOLO and PointPainting, depth completion, frontier exploration, MAVROS2, the full cycle, failsafes and the outdoor extension.
- **Act 5, "The swarm at work"**: Layer 2, running on its own. Four missions in 3-D (a city block after an earthquake, a flooded village, a forest, a flooded cave), each simulated in full first, then played back as a film with a director camera, chapters, captions, six lenses, live concept cards that link to the matching swarm-lab page, a drone's-eye inset, the tethered drone and a handover report. Every visit is a new seed.
- **Act 6, "Inside the swarm"**: the swarm lab. Layer 2 taken apart in 14 live simulations in six parts: boids, Vicsek criticality and the name, critical slowing down, symmetry breaking with a UGV, Turing patterns, phase changes as mission commands, stigmergy, CRDT map merging, topology with persistence, the air pocket (β₂ on the voxel map), Koopman prediction, reservoir computing, the FPGA timing and the demonstration rig; then six things to remember.

**After (recovery), the main focus**
- **Act 7, "What's left standing"**: the drones land and the ground station judges the building. A collapse is simulated (soft storey, corner pancake or leaning block), scanned the way the drones would, and run through the whole After pipeline: registration against the Act 2 baseline, the change map, debris volume with its range, wall tilt and floor sag, φ_wall (wall order), voids where someone could be, routes still open, thermal passes, vibration pods and an aftershock, confidence and a targeted re-fly. Every number is scored against the simulation's known truth and shown, misses included. A directed film of 3 min 39 s with a before/after swipe, then a scorecard and what the commander gets.
- **Act 8, "The commander's table"**: the same collapse (same failure mode and seed) turned into the plan an incident commander acts on: final room statuses (safe, restricted, unsafe) with conformal intervals, a re-entry window from an aftershock model, a ranked dig order split into team sectors, a safe removal order planned with a rescan after every lift, a clearance plan and the commander's brief, every decision scored against the truth. "The swarm recommends; the commander decides; an override always wins." Then the commander's table (a sandbox: overrides, sliders, the board) and the closed loop back to the next Before plan.

**One building through the disaster.** Each visit picks one seed. Acts 2, 7 and 8 build the same apartment block from it, so the block surveyed in Act 2 is the one that collapses in Act 7 and is decided on in Act 8. Act 7's "Next: Act 8, decide" hands Act 8 the same collapse (it rebuilds exactly the case Act 7 measured), and Act 8's "The next Before plan" opens Act 2 on the same building. ("Surprise me" in Act 7 or 8 picks another building; the acts after it follow that one.) Every case is simulated and says so on screen.

## Controls worth knowing
- **Contents** (top of the screen, or "See what's inside" on the first screen) lists every chapter of Act 1, the six disaster zones, every page of the swarm lab and all eight acts, and jumps anywhere.
- Press Enter on the first screen and the page goes full screen (browsers only allow full screen after a click). The button next to Sound, or the F key, toggles it.
- Acts 2 to 8 open on top of the story, in the same page, from the acts map at the end of Act 1 (or Contents). **Back to the story** in each act (or Esc in Acts 2, 5, 6, 7 and 8) returns to where you were in Act 1. Only one act runs at a time; closing it frees its graphics memory.
- Acts 2, 7 and 8: Space plays and pauses, the arrow keys step 5 s, the number keys switch lenses, T shows the truth (7, 8), D gives the camera back to the director (drag the view to take it), 2x and 4x are in the dock. Act 2: S opens the sandbox. Act 7: the Floors strip cuts the building away, A sends an aftershock, click a room for its card. Act 8: C opens the commander's table, click a room to override it.
- In Act 3, **END** (top bar) stops the run at any point and shows the mission report.
- In Act 4, move with **Next** (bottom right), **Back**, the arrow keys, one scroll-wheel notch per step, a swipe on phones, or **All steps** (top).
- The concept cards in Acts 2, 5, 7 and 8 link to the matching swarm-lab page (Act 6).
- Music is generative and synthesised in the browser. It is on if you entered with sound, and each act has its own switch.
- Shortcuts: add `#act2` to `#act8` to the address and that act opens straight after the first screen; `#act6` (or `#lab`) opens the swarm lab, `#lab-vicsek` (or any lab page id) one simulation in it, `#contents` opens the contents.

## How Act 1 is made
- **The two sets are path-traced, then baked.** A close-up of the void (tiles, papers, a fallen chair, a pipe, crushed concrete, a phone) and a clay maquette of the whole building were modelled procedurally in Blender (Python) and lit in Cycles, twice each: moonlight and dawn. The full light transport is baked into lightmaps, so the browser shows what the path tracer computed. The scroll blends night into dawn.
- **The torch is real light.** Your cursor aims a spotlight with soft shadow maps; it borrows the bake's ambient occlusion and grain so what it lights has corners and texture.
- **The mapping is real.** On load, drones explore the actual maquette geometry with ray casts (three-mesh-bvh): free, occupied and unknown cells, nearest unclaimed frontier, BFS paths. Every number on the page (area, moves, the race, β₀) comes from those runs, and each unexplored pocket keeps its number until it is searched (a pocket that lasts only a few moves is a LiDAR shadow, not a space: the persistence rule).
- **The phase-transition figure is computed**, and labelled as a sketch: one wall as a grid of patches under rising stress; φ is the nematic order of the patch normals (Act 7's measure) and ξ the mean size of the damage clusters, averaged over 120 walls.
- **The person is only ever seen in thermal**; **all sound is synthesised** in WebAudio (the knocking is placed in 3-D).
- Accessibility: the story is real text in the page; "Show me where" skips the torch puzzle; reduced motion turns off the lens effects and parallax; without WebGL the text reads over a still of the model. Performance: Draco-compressed geometry, the 3-D pauses under full-screen chapters and while an act is open, and the page lowers its own resolution, then its shadows and lens blur, if a device struggles.

## How Act 2 is made
- **Everything on screen is computed from the seed**: the survey flight (frontier exploration on one shared map, β₀ of the unexplored space counted down to 0), the baseline (door widths measured off the point cloud), the access graph (β₁ = E − V + C per floor, bridges by Tarjan's algorithm), every crowd run and every fix. Only the camera, the captions' wording and the timing are written by hand.
- **The crowd is a published model** (Helbing, Farkas and Vicsek, Nature 2000) with its own parameters, on simulated occupancy (2 to 4 people per flat at night, 80 for a full house), stepped at 4 ms on a 5 cm grid, with two small rules of ours shown in the Assumptions panel. It runs in a Web Worker, so its speed does not depend on the frame rate. A permanent chip says it is not a prediction for a real building.
- **Repeated runs**: the crowd is chaotic, so faster-is-slower and each fix count only when their repeated runs do not overlap; otherwise the film says "no clear change".
- **Percolation**: 1,500 trials block links in random order until someone has no route out; the margin is the median.
- The building is Act 7's (`buildBuilding({ seed })`), so the same seed gives the same block in Acts 2, 7 and 8.

## How Acts 3 to 6 are made
- **Act 4's drone is the team's own build**, modelled in Blender with Python: 580 mm X frame, Tarot 4006 620KV with 12x3.8 props, Tekko32 F4 4-in-1, CUAV V6X on dampers, Raspberry Pi 5 + AI HAT+ (Hailo-8), the 4S 5200 mAh pack, and the RPLidar A1M8 in a cradle tilted by a servo. Motors, props, electronics and sensors are at their datasheet dimensions. The flight controller layout is simplified to the Pixhawk standard; the chips are the V6X's real ones. 19 canvas simulations share one small kit; only the open step runs. Charts labelled "illustrative" show behaviour, not measured data.
- **Act 5 simulates first, then films.** Each mission's swarm is simulated deterministically to the end before anything plays, then the recording is played back with a director camera, so scrubbing and lens changes are instant and the film can never stall. The worlds are built in code from a seed, with a small set of props modelled in Blender. The concept cards draw from the running mission and link to the matching lab page.
- **Act 6** is 14 canvas simulations sharing one kit; only the simulation on screen runs.

## How Act 7 is made
- **The building and the collapse are procedural**: ground plus 3 floors, RC frame with brick infill, two flats per floor, a site with neighbours; three failure modes as rigid motions (not a physics engine), with debris settled at an angle of repose, cracks and jammed doors. The truth (a 0.12 m voxel grid, true voids a 0.35 m drone cannot reach, true room statuses) drives the simulated sensors and the scoring; the pipeline itself only sees scans, spectra and thermal returns.
- **The pipeline** (pure JS, in 45 ms slices with a real progress bar): trimmed point-to-plane ICP, OctoMap-style ray carving, per-storey rigid motion fits, the change map and debris (a range: low, estimate, high), RANSAC wall planes, φ_wall per patch and the damage clusters, pockets seen through a gap or possible under a slab, route skeletons and bottlenecks, three thermal passes, vibration pods (f0, stiffness loss) and an aftershock with its relaxation time, per-surface confidence and a re-fly planned target by target, the swarm's own flight log as data (φ_swarm, a Hankel DMD speed forecast).
- **Measured** over 3 modes x 40 seeds: no false-safe room in any case; change-map IoU median 0.90 (soft storey), 0.59 (corner pancake, shown as a miss), 0.96 (leaning block); debris error median 8 to 11 %; search certified about 99 %.

## How Act 8 is made
- **Every decision is computed from the case Act 7 measured** and scored against the simulation's truth, with the misses on screen. Room statuses use split conformal intervals calibrated on 220 simulated collapses (per failure mode and group), with one safe-limit knob set on one half of them and tested on the other: held out, 0 of 676 and 0 of 703 rooms marked safe were truly unsafe (95 % bound 0.44 %); the price is caution (44 % of the truly safe pancake rooms stay restricted).
- The re-entry window comes from a simulated mainshock and Reasenberg & Jones aftershock chances; the dig order from candidate voids, the night's occupants (Act 2's occupancy, same seed) and time to reach them (Smith's rule, Fiedler sectors); the removal order is planned with a rescan after every lift and only for the debris on the lanes to the dig sites; the clearance plan is unbalanced optimal transport (Sinkhorn). The commander's table reruns everything downstream live.
- A permanent chip: "Simulated collapse and simulated occupants; advice only, the commander decides".

## Files in `source/`
- `index.html`, `act1/` — Act 1 (`main.js`: the story, and the openers that bring every act into this page, hand one act to the next and keep one seed per visit; `act1.css`, `assets/`; `lab/`: the swarm lab controller `lab.js`, `site.js` (the code link and the switches), the simulation kit, the gate swarm, the wall figure, the music and the 14 simulations in `lab/sims/`; `zones/`: the six disaster-zone scenes)
- `common/` — shared: `sim.js` (exploration), `sound.js`, `fluid.js` (liquid cursor field), `gate.js`, `cursor.js`, `base.css`
- `act2/` — Act 2 (`js/before.js` the shell; `js/pipe/` the survey, baseline, access graph, crowd model, percolation and fixes, and `worker.js`, the crowd's Web Worker; `js/film/`, `js/engine/`, `js/ui/`; `assets/props.glb`)
- `act3/` — Act 3 (see `act3/CREDITS.txt`)
- `act4/` — Act 4 (`js/act3.js` story and scene, `js/steps.js` all the words, `js/mems.js` the four sensor demos, `js/sims/`, `assets/drone.glb` and `assets/fc.glb`)
- `act5/` — Act 5 (`js/act4.js`; `js/sim/` the swarm simulator and recording; `js/engine/`; `js/missions/` one folder per mission; `js/ui/`; `assets/props.glb`)
- `act7/` — Act 7 (`js/act7.js` the shell; `js/building/` the block, the collapse and the truth; `js/pipe/` the After pipeline; `js/film/` chapters and captions; `js/engine/` renderer, director, lenses, layers; `js/ui/`; `js/theme.js` every colour; `assets/props.glb`)
- `act8/` — Act 8 (`js/act8.js` the shell; `js/decide/` the decision engine and its calibration data; `js/film/`, `js/engine/`, `js/ui/` including the commander's table; `assets/props.glb`)
- Acts 2, 7 and 8 share modules: Act 2 and Act 8 import Act 7's building, engine and theme, and Act 8 imports Act 2's occupancy model. Acts 2, 3, 4, 5, 7 and 8 also open on their own from their folders (`act2/` and so on), without the story around them.
- `fonts/` — Fraunces, Geist, Geist Mono (SIL Open Font License)
- `vendor/draco/` — Draco decoder (Apache 2.0)

`index.html` is `source/` bundled into one file with esbuild, with every model, texture, font and the crowd worker packed inside (24,917,107 bytes, under GitHub's 25 MiB browser-upload limit). To run `source/` on its own, serve it (browsers block module imports from `file://`): `cd source`, then `python3 -m http.server 8000`, then open `http://localhost:8000/`. In that form three.js and three-mesh-bvh load from jsDelivr.
