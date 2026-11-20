# lib-event

`event` — user-space event emission and listener registration algebra:
events are fire-and-forget; listeners are natural arrows.

## Layout

```text
handl-packages/event/   the .hnl package
scripts/hnl-gate.sh     the gate
ci.sh                   bupha entry
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.
