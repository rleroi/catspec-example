# catspec-example: TaskFlow

The example project for [CaT (Code as Text)](https://github.com/rleroi/catspec).
A small team task manager, specified in `bacon/` and generated into `src/`.

- `bacon/` and `cat.config.yaml` are human-owned. Edit them with the
  `cat-author` skill.
- `src/` and `purr` are transpiler-owned. Written by the `cat-transpile`
  skill, committed by `cat-transpile-bot`. Humans do not edit them; a fix is
  a spec change.

```bash
npx -y @catspec/cli validate . --strict
npx -y @catspec/cli verify .
npx -y @catspec/cli transpile .     # needs the agent in cat.config.yaml
```

## The twenty-change experiment

This repo is the kill criterion for CaT: twenty real spec changes, one PR
each, with no hand edits to `src/`. Each PR is a `bacon/` diff followed by a
bot commit. If the generated code stops being maintainable through the spec
alone, the approach fails and CaT stops.

| # | Change | Spec PR | Bot commit | Verdict |
|---|---|---|---|---|
| 0 | baseline: full generate from the 0.2 spec | | | |

Language: [SPEC.md](https://github.com/rleroi/catspec/blob/master/SPEC.md).
Terms: [GLOSSARY.md](https://github.com/rleroi/catspec/blob/master/GLOSSARY.md).
