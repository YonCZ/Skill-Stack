# Skill-Stack

Three design skills as plain files. Reference a `SKILL.md` by absolute path. The agent reads only the skills you name in the prompt.

## design

- `frontend-design`: aesthetic direction, typography, and deliberate choices instead of templated defaults.
- `design-taste-frontend`: layout systems, copy, photography, motion, plus a browser checker and finish gate. Ships its references, scripts and assets.
- `frontend-spedup`: verification companion. Run structural checks and interaction assertions before screenshots. Use it with a design skill, not alone.
- `motion-craft`: motion and interaction craft only. Easing tokens, duration table, press feedback, reveals, one signature moment. Pair it with a design skill; it does not set layout or identity.

## Usage

```text
Read and apply /absolute/path/to/Skill-Stack/design/frontend-design/SKILL.md.
Read and apply /absolute/path/to/Skill-Stack/design/frontend-spedup/SKILL.md.
```

List every skill you want. Put `frontend-spedup` last so its verification order wins over a design skill that asks for screenshots early.

## License

`frontend-design` includes its own `LICENSE.txt`. `design-taste-frontend` includes reference assets, among them stand-in photographs, from its original distribution. Check their terms before publishing work that uses them.
