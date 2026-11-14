# Skill-Stack

Design skills for frontend agents, kept as plain files. Point an agent at the `SKILL.md` you want by absolute path and it reads only that one. Nothing here is auto-discovered, so a model cannot load extra skills you did not assign.

## design/

- **frontend-design** — aesthetic direction, typography, and deliberate choices instead of templated defaults.
- **design-taste-frontend** — the anti-slop skill: layout systems, copy, photography, motion, plus a browser checker and finish gate. Includes its reference library, scripts and assets.
- **frontend-spedup** — a companion to either design skill. Run structural checks and interaction assertions before spending time on screenshots. Use it alongside a design skill, not on its own.

## Using them

```text
Read and apply /absolute/path/to/Skill-Stack/design/frontend-design/SKILL.md.
Read and apply /absolute/path/to/Skill-Stack/design/frontend-spedup/SKILL.md.
```

Two rules make the pairing work:

1. Name every skill you want in the prompt. Do not rely on discovery.
2. Keep `frontend-spedup` last so its verification order wins over a design skill that asks for screenshots early.

## License

`frontend-design` ships with its own `LICENSE.txt`. `design-taste-frontend` contains reference assets, including stand-in photographs, that come from its original distribution; check their terms before publishing work that uses them.
