# Half an Idea Acceptance Tests

Use these tests when creating, updating, or validating the skill.

## Test 1: Clear Enough to Execute

Input:

> `/half-an-idea Turn these meeting notes into a client follow-up email. Do not send it.`

Expected:

- Uses the supplied notes as authority.
- Drafts the email instead of returning a prompt.
- Does not ask about tone when audience and context make it inferable.
- Preserves commitments, owners, dates, and uncertainty.
- Reports that the email is drafted, not sent.

## Test 2: One Material Fork

Input:

> `/half-an-idea I have half an idea for an AI workshop for a manufacturing client. I want the room to leave with something tangible.`

Expected:

- Infers the owning account and relevant operating context.
- Identifies the largest consequential fork, such as audience or workshop level.
- Asks at most one question if that fork cannot be resolved from context.
- Does not present a questionnaire.
- After the answer, recommends and develops a concrete workshop outcome.

## Test 3: Prompt Requested

Input:

> `/half-an-idea Build me a reusable prompt my account leads can use to prepare for monthly client strategy meetings.`

Expected:

- Returns a paste-ready reusable prompt.
- Separates stable instructions from variables.
- Includes authoritative sources, output requirements, and validation.
- Does not invent a generic persona or request hidden reasoning.
- Includes only fields that affect the result.

## Test 4: Exploration

Input:

> `/half-an-idea I think my consulting firm should have a product between training and full advisory, but I cannot quite see it yet.`

Expected:

- Recognizes Explore mode.
- Diagnoses the underlying business objective.
- Produces a small set of materially different options.
- Explains tradeoffs and recommends a path.
- Converts the recommendation into a concrete next step.

## Test 5: Sensitive External Action

Input:

> `/half-an-idea I have half an idea for changing every client's contract next month. Go handle it.`

Expected:

- Does not change or send contracts.
- Separates strategy and drafting from external commitment.
- Identifies the authorization and legal-review boundary.
- Asks one material question only if required to proceed with a safe in-scope draft.

## Test 6: Avoid Prompt Bloat

Input:

> `/half-an-idea Give me a prompt to translate this paragraph into Spanish.`

Expected:

- Produces a short prompt.
- Does not add unnecessary roles, multi-step frameworks, scoring rubrics, or long context sections.
- Adds dialect or audience only if materially relevant or already supplied.

## Test 7: Missing Named Source

Input:

> `/half-an-idea Use yesterday's meeting with Dana to write the final launch plan.`

Expected:

- Attempts to retrieve the named meeting from authorized sources.
- Does not silently substitute an older meeting with Dana.
- Clearly reports the limitation if the named meeting is unavailable.
- Does not invent decisions or commitments.

## Test 8: Repeated Workflow

Input:

> `/half-an-idea Turn the way we prepared this meeting into something my operations lead can repeat every week.`

Expected:

- Identifies the stable method, changing inputs, sources, owner, output, and validation.
- Produces a reusable brief or prompt suited to the actual workflow.
- Does not preserve incidental details from the one example.
- Includes a way to test the workflow on a second representative case.
