# SpecShip

Spec to ship: spec-driven development for Claude Code.

- **Specs** run on SpecShip: from the product to use cases with acceptance criteria
- **Implementation** runs on [ECC](https://github.com/affaan-m/ECC): from one use case to reviewed code

> Status: 0.9.0.

## Install

SpecShip hands implementation to ECC. Install both:

```text
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
| [`/use-case-diagram`](skills/use-case-diagram/SKILL.md) | Fourth step. Grills you about who takes part in each use case, then draws the actors and use cases as a Mermaid diagram in `docs/use-cases/README.md`. GitHub and the VS Code preview show it with nothing to install |
| [`/entity-model`](skills/entity-model/SKILL.md) | Fifth step. Grills you about the nouns the use cases work on, then writes `docs/entity-model.md`: a Mermaid ER diagram and, per entity, its meaning, attributes, states, relationships, rules, and use cases. One model for the project, grown by every BR |
| [`/use-case-spec`](skills/use-case-spec/SKILL.md) | Sixth step. Fills in one use case: actor, trigger, preconditions, main flow, alternative flows, exceptions, postconditions, and acceptance criteria in Given/When/Then. Asks only what the BR, diagram, and entity model leave open |
| [`/grill-me`](skills/grill-me/SKILL.md) | Interviews you one question at a time until a plan is clear. Used by every step above. From [mattpocock/skills](https://github.com/mattpocock/skills) (MIT) |
| [`/next`](skills/next/SKILL.md) | Any time. Reads the project, shows where it stands, and names the next command and the one after it. Read-only |

## Implementation

Once a use case is specified, implement it with ECC:

1. `/ecc:plan docs/use-cases/UC-001-clock-in-and-out.md`
2. Read the plan, then reply `yes`, or `modify: …`
3. ECC implements the plan
4. `/code-review`
5. Commit: `feat(UC-001): …`

When a business question comes up that the use case does not answer, update it with `/use-case-spec UC-001` first,
then continue.

## License

MIT. See [LICENSE](../LICENSE).
