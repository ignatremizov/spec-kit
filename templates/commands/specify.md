---
description: Create or update a feature spec using the Spec-Kit spec template.
scripts: create-new-feature.sh --json "$ARGUMENTS"
---

## User Input

```text
$ARGUMENTS
```

You **MUST** consider the user input before proceeding (if not empty).

## Outline

1. **Setup**: Run `{SCRIPT}` from repo root. Parse the JSON output for BRANCH_NAME and SPEC_FILE. All paths must be absolute. For single quotes in args like "I'm Groot", use escape syntax: e.g 'I'\''m Groot' (or double-quote if possible: "I'm Groot").

2. **Load context**: Read `.specify/memory/constitution.md` and `AGENTS.md` if present.

3. **Write spec.md**: Use `templates/spec-template.md` as the structure and fill it with:
   - User stories (prioritized, independently testable)
   - Acceptance scenarios
   - Requirements and success criteria
   - Edge cases and assumptions

4. **Clarifications**: Add a `## Clarifications` section (even if empty) for later phases.

5. **Report**: Output the spec path, feature name, and any open questions.

Context for spec creation: {ARGS}
