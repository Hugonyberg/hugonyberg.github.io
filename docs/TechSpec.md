# Technical Specification

## Stack

- **Frontend:** HTML5, CSS3, JavaScript (jQuery)
- **Hosting:** GitHub Pages
- **Analytics:** Google Analytics (gtag.js)
- **CSS Framework:** HTML5 UP Helios theme

## Architecture

The site is a static multi-page website. Each project has a dedicated HTML page. Navigation is handled via a shared nav bar included in every page. No build step or server-side rendering is used.

## AI & Gameplay Systems

- **GOAP Planner:** A* search over action graphs to produce goal-directed plans for game agents
- **Steering Behaviors:** Seek, Arrival, Separation, Spread, and Object Avoidance computed per frame
- **Behavior Trees:** Hierarchical decision logic for enemy AI
- **State Machine:** Finite state machine for boss AI transitions
- **Navmesh:** Recast Navigation library integration; polygon mesh converted to a custom grid of nodes and connections
- **Wave Manager:** Data-driven wave configuration controlling spawn timing and enemy composition
- **2D Collision:** Swept AABB collision with moving platform support
- **Screenspace Raycasting:** Transform from screen-space to world-space ray for mouse picking

## Rendering

- Sprite batching for 2D entity rendering
- Visual debug overlay for navmesh geometry and node relationships
- ImGui controls for live parameter tweaking (enemy speed, mass, force, ray layouts)

## Performance

- Object pooling for enemy entities
- Grid lookup for fast node-center and connection queries
