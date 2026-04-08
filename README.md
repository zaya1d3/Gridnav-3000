# Gridnav 3000 - Pathfinding Research Playground

Gridnav 3000 is a compact, browser-based A* pathfinding visualizer and experimentation sandbox. It was built as a single-file interactive prototype to demonstrate core pathfinding concepts, rapid UI feedback, and a responsive rendering strategy that scales to different viewport sizes.

Key ideas and goals

- Clear, inspectable implementation: the visualizer favors a concise, easy-to-follow A* implementation so the algorithm and its visualization are both easy to read and modify.
- Responsive renderer: the grid uses an HTML5 Canvas with dynamic sizing so cells remain square while the layout adapts to the available screen area.
- Fast, deterministic animations: exploration and path animations are produced from recorded steps so results are reproducible and performant on modest hardware.

What you'll find in the code

- A minimal A* implementation with a Manhattan heuristic and explicit parent mapping for efficient path reconstruction.
- A simple grid model (2D array) representing `empty`, `wall`, `start`, `end`, `explored`, and `path` states.
- An animation pipeline that batches exploration steps and path drawing to keep UI updates smooth.
- Responsive layout helpers that compute available viewport height and set canvas dimensions so the entire app fits without page scrolling.

Why this is a good learning / demo project

- Concise: most logic lives in one HTML file, making it trivial to open and step through.
- Extensible: the structure is ready for improvements such as a binary-heap open set, weighted heuristics, diagonal movement, or maze-generation algorithms.
- Portable: no build step or dependencies — just open the file in a browser or serve the folder.

How I built it (short)

- Tech: plain HTML5, vanilla JavaScript, and CSS (no frameworks). Canvas rendering provides predictable pixel control for the grid.
- Development approach: iterative — implement core algorithm, add visual feedback, then tune layout and animation to produce a responsive demo.

Suggested next steps / experiments

- Replace the open-array sort with a binary heap (priority queue) to see performance differences on larger grids.
- Add weighted edges or allow diagonal moves and compare path quality using different heuristics.
- Export recorded runs as JSON for replay or benchmarking across configurations.

Open the Website

1. Locate the folder with path finding visualizer v5.html and styles.css
2. Double-click path finding visualizer v5.html or right-click → “Open with” → choose a browser
3. Make sure styles.css is in the same folder so the styling works
