# Source

The skills `motion-broll`, `object-separation`, `explainer-high-energy`, `explainer-default`,
`explainer-engaging` and `sound-effects` are vendored from
https://github.com/Barty-Bart/motion-graphics at commit 3d83d987d658601d8a1269eb691622bdcd427335
(MIT, see `LICENSE-motion-graphics`; sound files CC0, see `sound-effects/LICENSES.md`).

Update with: `npx skills add Barty-Bart/motion-graphics` or re-copy `skills/*` from that repo.

`agent-reach` (English SKILL.md + references) is vendored from
https://github.com/Panniantong/Agent-Reach at commit 94f06c1969dfc1834001269d79d3ad0972d9dee6 (MIT).
The skill drives the `agent-reach` CLI and upstream tools, which must be installed separately:
`pipx install https://github.com/Panniantong/agent-reach/archive/main.zip` then `agent-reach install --env=auto`.
