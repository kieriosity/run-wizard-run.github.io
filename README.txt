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
- Sweep bonuses: +700 for collecting every shard, +700 for defeating all 12 enemies.
  Earning both is a "Perfect Clear" - and a fast Perfect Clear is the only way to break
  the 6,300-point top score (a full clear locks in 4,505 before the speed bonus; the
  realistic ceiling is ~6,500, so 6,300 demands a near-flawless, fast Perfect Clear).
- You start with only 2 hearts: two hits (from enemies or falling) resets the run to zero.
- The run timer is shown top-right; your time, sweep bonuses, and final score appear on the clear screen.

Arcade leaderboard
- An instruction popup appears on first load. Tick "Don't show this again" to skip it next time.
- The top-10 high scores are kept arcade-style. Beat a listed score and you enter your name.
- The current #1 high score and name are shown in the bar at the top of the page.
- Scores persist in the browser via localStorage (works on GitHub Pages, which is static/read-only
  and cannot host a writable file). Persistence is per-browser; a globally shared leaderboard would
  need an external service (e.g. a small serverless API).
- All entered names are sanitized (control characters stripped, length-capped) and rendered with
  textContent / canvas text only, so a name can never inject HTML or script. Scores read back from
  localStorage are re-validated, so a tampered store can't break or exploit the page.

What changed in this DX rebuild
- Wizard rebuilt from scratch as pixel sprites: 12-frame run cycle, 6-frame idle, 2 airborne frames.
- Improved animation timing: run frames advance based on actual movement speed, with landing dust and footstep particles.
- Reworked 16-bit style parallax: sky, moon, stars, distant mountains, castles, forest layers, ruins, fireflies, and mist.
- Textured tiles and background props: mossy stone, cracks, brickwork, crystal clusters, lanterns, mushrooms, grass, rune stones, and a moon gate.
- More robust loading: index.html embeds the art, so local asset path issues should not cause flashing.
