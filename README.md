# LAST SIGNAL — Iron Warden

A self-contained, static-hostable browser boss fight. No build step or server-side code is required.

## Play locally

Open `index.html` in a modern browser. For a local server, run `python -m http.server 8000` from this folder and visit `http://localhost:8000`.

## Controls

- **WASD / arrow keys:** move
- **Mouse:** aim
- **Move to the spawned glowing missile:** it appears in the arena. Walking up to it mounts the stationary sniper position and adds missiles to your ammo.
- **MISSILE button or left mouse button while mounted:** each spawned missile gives exactly one shot. After firing, ammo reaches zero and the button disappears; wait for the next missile to spawn. Holding the button never repeat-fires. Combat time slows to 0.1× while aiming. Hits deal 5% of the boss's maximum health normally; below 40%, they deal 10% (30% while exposed), until the boss reaches 30% health; below 30%, damage returns to 5% (15% while exposed).
- **E:** leave the turret (on mobile, press any movement-pad direction to dismount).
- **Missile restock:** when your missiles run out, a new missile appears in the arena after a short delay; move to it to mount and restock
- **Boss dive:** one slower, telegraphed charge is followed by a four-second stomping pursuit with heavy footstep sounds and screen shakes.
- **Reduced boss damage:** projectile hits and meteor impacts now deal less damage. A dive hit still removes half of current health, once per dive.
- **Meteors:** timed showers show landing zones before rocks fall; impacts deal damage and create an expanding blast ring.
- **Healing:** when injured, a glowing green med kit appears after a delay. Move to it to restore up to 35 health.
- **Pilot health:** starts at 150 (1.5× the original). A boss dive collision removes half of the current health once per dive, rather than defeating the pilot instantly.
- **Space:** dodge dash (short invulnerability, 1.25 second cooldown)
- **Q / TIME button:** slow the whole game to 0.1× for 10 seconds; 20-second cooldown. The button is in the desktop footer or above the mobile controls.
- **Final phase prompt:** during the Warden's orbital purge, the fight slows to 0.45× for 3 seconds and the screen bends slightly. Click/tap the prompt or press Space/Enter once to remove 0.5% of the boss's maximum health.
- **Shift:** pulse-break ultimate (charges as shots hit the boss)
- **Mobile:** on-screen movement and aim pads, plus DASH. The MISSILE button appears only after reaching a spawned missile.
- **How to play:** open the guide from the title screen before deploying for a quick control and survival overview.

## Static hosting

Upload `index.html`, `style.css`, and `game.js` together to the root of any static host (for example GitHub Pages, Netlify, or Cloudflare Pages). Keep the three files in the same directory. The game uses no external game libraries; the optional Google Fonts import falls back to system fonts if unavailable.
