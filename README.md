# Fireworks Animation

![Fireworks Animation Screenshot](./Screenshot%202024-08-25%20160601.png)

Fireworks Animation built with HTML, CSS and JavaScript — a lightweight canvas demo that renders colorful fireworks using simple particle physics.

## Demo
Open `index.html` in your browser to view the animation. For the best experience, use a modern desktop browser (Chrome, Firefox, Edge, Safari).

If you prefer to run a local server (recommended for consistent behavior):

```bash
# Python 3
python -m http.server 8000
# then open http://localhost:8000 in your browser

# or using npm
npx http-server -p 8000
```

## Features
- Canvas-based particle fireworks effect
- Randomized colors and sizes for varied visuals
- Auto-resizes with the browser window
- Small, dependency-light (uses jQuery only)

## Files
- `index.html` — HTML shell and canvas element
- `style.css` — minimal stylesheet
- `script.js` — main animation code (particle generation, update loop, drawing)
- `Screenshot 2024-08-25 160601.png` — demo screenshot used in this README

## Customize
You can tweak the look and behavior by editing `script.js`:

- Change the number of launchers by modifying `fireNumber` (default: 10)
- Adjust explosion spread by changing `range`
- Tweak gravity and particle life inside the firework generation code (`ay`, `life`, `size`)
- Replace the color generation in `randColor()` if you want a different palette or themed colors

Example: limit fireworks per launch or make them larger by editing the loop that creates `firework` objects.

## Implementation notes
The script uses a simple particle system:
- "Fires" are launch particles that travel upward until they reach a random `far` height.
- When a fire reaches its `far` value, a burst of "firework" particles is spawned with randomized velocities, colors, and lifetimes.
- Each frame the particles update position and alpha, and expired particles are removed.

## Contributing
PRs are welcome. Suggestions:
- Add configuration options (UI controls for count, gravity, colors)
- Improve mobile performance or touch interactions
- Add TypeScript conversion or remove jQuery dependency

## License
Add a license file if you want this project to be reusable by others (MIT is a common choice).

---

If you'd like, I can also:
- Add a live GitHub Pages workflow and instructions to publish the demo
- Create UI controls to change the fireworks parameters at runtime
- Replace jQuery with vanilla JavaScript for a smaller bundle

Tell me which of those you'd like and I'll make the change.