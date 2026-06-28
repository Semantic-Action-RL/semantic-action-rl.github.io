# Adapting Generalist Robot Policies with Semantic Reinforcement Learning

Project page for **Semantic Action Reinforcement Learning (SARL)** — running reinforcement learning
over a VLA's *language prompts* instead of its low-level robot actions to adapt generalist policies to
complex, long-horizon tasks.

Jagdeep Singh Bhatia, Andrew Wagenmaker, William Chen, Sergey Levine — UC Berkeley. CoRL 2026.

The site is a static page served by GitHub Pages from `index.html`.

## Local preview

```
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Adding media

- **Per-rollout videos** (`#tasks` section): drop `.mp4` files in `static/videos/tasks/` named
  `taskN_METHOD.mp4` (`N` in 1–4; `METHOD` in `sarl, iclvlm, dsrl, residual, base`), then replace the
  matching `<div class="video-placeholder">…</div>` in `index.html` with a `<video>` tag (template is
  in the HTML comment above the video matrix).
- **Training timelapses** (`#timelapses` section): either embed YouTube (replace the
  `<div class="yt-placeholder">…</div>` with an `<iframe>`), or drop `.mp4`s in
  `static/videos/timelapses/`.
- **Figures** live in `static/images/figures/` and are regenerated from the paper PDFs in
  `reference/` via `qlmanage -t -s <px> -o <outdir> <fig.pdf>`.

## Credits

Website template adapted from [Nerfies](https://github.com/nerfies/nerfies.github.io), used under a
[Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
