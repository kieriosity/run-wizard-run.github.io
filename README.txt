Moonspire Run DX

Open index.html in a browser. The game is self-contained, so the sprite sheets are embedded in the HTML as data URIs. The PNG assets are included separately so you can inspect or reuse them.

Controls
- A/D or Left/Right: move
- Space, W, or Up: jump
- J: cast a bolt
- K: radiant light spell (raise the staff; a brilliant burst lights the scene)
- R: restart

Scoring
- Collect shards (coins) and defeat enemies for points.
- A speed bonus is awarded at the Moon Gate: the faster you finish, the bigger it is
  (up to 3000 points for an instant run, scaling down to 0 at the 90s par time).
- The run timer is shown top-right; your time, speed bonus, and final score appear on the clear screen.

What changed in this DX rebuild
- Wizard rebuilt from scratch as pixel sprites: 12-frame run cycle, 6-frame idle, 2 airborne frames.
- Improved animation timing: run frames advance based on actual movement speed, with landing dust and footstep particles.
- Reworked 16-bit style parallax: sky, moon, stars, distant mountains, castles, forest layers, ruins, fireflies, and mist.
- Textured tiles and background props: mossy stone, cracks, brickwork, crystal clusters, lanterns, mushrooms, grass, rune stones, and a moon gate.
- More robust loading: index.html embeds the art, so local asset path issues should not cause flashing.
