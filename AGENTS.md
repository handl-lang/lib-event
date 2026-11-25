# lib-event

`event` — user-space event emission and listener registration algebra:
events are fire-and-forget; listeners are natural arrows.

## Layout

| path | role |
| --- | --- |
| `handl-packages/event/index.hnl` | the `.hnl` package — `pkg.hnl` `entry` points here explicitly |
| `pkg.hnl` | manifest — `modules: ["event"]` |
| `scripts/hnl-gate.sh` | `.hnl` gate (`SRC_DIR` env selects the source dir) |
| `workflows/gate.yaml` | CI — shared `handl-gates` campaign (bupha/peregrin) |

## Contract

- Single-module package in the `handl-packages/` layout (not `src/`);
  no Rust crate.
- Emission is fire-and-forget — listeners must tolerate absent
  subscribers.

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
