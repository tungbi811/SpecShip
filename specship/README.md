# SpecShip

Spec to ship: spec-driven development for Claude Code.

- **Spec and doc phases** run on [aiup-core](https://github.com/AI-Unified-Process/marketplace/tree/main/aiup-core)
- **Implementation** runs on [ECC](https://github.com/affaan-m/ECC)
- **SpecShip** adds what sits between and around them

> Status: 0.4.0. Skills are added one planning step at a time.

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
| [`/breakdown`](skills/breakdown/SKILL.md) | Third step. Grills you about the use cases of a BR, then lists them in the BR's Related Use Cases and creates one file per use case in `docs/use-cases/`: metadata filled, every other section an empty template |
| [`/grill-me`](skills/grill-me/SKILL.md) | Interviews you one question at a time until a plan is clear. Used by every step above. From [mattpocock/skills](https://github.com/mattpocock/skills) (MIT) |

## License

MIT. See [LICENSE](../LICENSE).
