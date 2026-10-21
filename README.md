# Save Mum!

A rescue game dreamed up by a 6 year old, by voice, and built with Claude.
One file: `index.html`. No build step, no network calls, system fonts only.

Zombies take Mum. You walk through a scary forest (lasers, a boulder, a ring
of skeletons, Mum under the crystal's spell), cross a 12 block parkour over
goo, and pull out the evil crystal. Nobody can get hurt: bad guys bounce you
back instead.

## Where it plays

- **cyborg.garden/games/save-mum/** from `main`, via the site's
  `games.sources.json`. `meta.json` sets the card and the status.
- **xbox50 console**, served under `/cart/`. The game reads keys, so the
  cart entry needs a pad map. The help words switch to stick and button
  wording on that path.

```json
{
  "id": "save-mum",
  "title": "Save Mum!",
  "runtime": "web",
  "run": "games/save-mum/index.html",
  "input": ["keyboard", "pointer", "gamepad"],
  "pad": { "stick": "arrows", "click": "KeyX", "cursor": false,
           "hint": "stick: move · button: hit · down + button: spin" },
  "sync": { "kind": "git", "repo": "https://github.com/cyborg-garden/save-mum",
            "ref": "main", "path": "." }
}
```

## Controls

| | Keyboard | Touch | Pad / xbox50 |
|---|---|---|---|
| Walk | ← → | ◀ ▶ | stick |
| Jump | ↑ or Space | ⬆ | stick up (B on a pad) |
| Crouch | ↓ | ⬇ | stick down |
| Hit / hack | X | 👊 | button (A) |
| Spin kick | ↓ + X | ⬇ + 👊 | down + button |
