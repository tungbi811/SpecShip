# SpecShip

Spec to ship: spec-driven development for Claude Code.

- **Spec and doc phases** run on [aiup-core](https://github.com/AI-Unified-Process/marketplace/tree/main/aiup-core)
- **Implementation** runs on [ECC](https://github.com/affaan-m/ECC)
- **SpecShip** adds what sits between and around them

> Status: 0.3.0. Skills are added one planning step at a time.

## Install

SpecShip builds on two other plugins. Install all three:

```text
/plugin marketplace add ai-unified-process/marketplace
/plugin install aiup-core@ai-unified-process-marketplace

/plugin marketplace add affaan-m/ECC
/plugin install ecc@ecc

/plugin marketplace add tungbi811/SpecShip
/plugin install specship@specship
```

## Update

```text
/plugin marketplace update specship
```

## Skills

| Skill | What it does |
|-------|--------------|
| [`/kickoff`](skills/kickoff/SKILL.md) | First step of a project. Grills you about the product, then writes `PRODUCT.md` at the project root |
| [`/business-requirements`](skills/business-requirements/SKILL.md) | Second step. Grills you about the next release or initiative, then writes `docs/business-requirements/BR-XXX-<slug>.md`: goal, success metrics, in scope, out of scope |
| [`/grill-me`](skills/grill-me/SKILL.md) | Interviews you one question at a time until a plan is clear. Used by `/kickoff`. From [mattpocock/skills](https://github.com/mattpocock/skills) (MIT) |

## License

MIT. See [LICENSE](../LICENSE).
