# Robert Skill Runtime Chain

## Universal Language Lock Step

Before any runtime mode is selected, run:

```text
1. Detect latest user instruction language
2. Set language_lock.locked_language
3. Carry language_lock through all downstream modules
4. Run Output Language Lock Harness before final delivery
```

Priority:

```text
language lock > runtime mode > style > audience adaptation > notes language
```

The latest user instruction language controls the final output unless the user explicitly requests another language.

## Step 0: Select Runtime Mode

Before running any mapper, Robert Skill must select the lightest sufficient runtime mode.

Available modes:

```text
1. Quick Message Mode
2. One-on-One Strategy Mode
3. Public Narrative Mode
4. Expert Translation Mode
5. Rewrite Recovery Mode
6. Personal Communication Mode
7. Full Narrative Mode
```

Use:

```text
selectors/runtime_mode_selector.md
policies/lightest_sufficient_chain_policy.md
```

## Core Rule

```text
Do not run the full chain by default.
Use the lightest sufficient chain.
```

## Mode-Specific Runtime

### Quick Message Mode

```text
Conversation Purpose
→ Relationship Context
→ Listener Hook
→ Minimum Next Action
→ Light Surface Check
→ Output
```

### One-on-One Strategy Mode

```text
Conversation Purpose
→ Relationship Context
→ Recipient Motivation
→ Collaboration / Ask Hypothesis
→ Attraction Filter
→ Narrative Authority
→ Claim Boundary
→ Message / Talking Points
→ Harness
→ Output
```

### Public Narrative Mode

```text
Story Kernel
→ Narrative Authority
→ Value / Stakes
→ Action-Reaction-Gap
→ Controlling Idea
→ Audience Cognition
→ Affective Arc
→ Narrative Entropy
→ Renderer
→ Harness
→ Output
```

### Expert Translation Mode

```text
Claim Boundary
→ Audience Cognition
→ Audience Entropy Tolerance
→ Low-Entropy Ground
→ High-Entropy Turn
→ Mechanism Explanation
→ Surface Naturalness
→ Output
```

### Rewrite Recovery Mode

```text
User Feedback
→ Failure Layer Diagnosis
→ Reroute
→ Rewrite
→ Output
```

### Full Narrative Mode

Use only for complex, high-stakes long-form narrative work.

```text
Parse Material
→ Extract Claim Boundary
→ Build Story Kernel
→ Map Narrative Authority
→ Identify Value / Stakes
→ Build Action-Reaction-Gap
→ Build Controlling Idea
→ Map Audience Cognition
→ Map Affective Arc
→ Map Narrative Entropy
→ Select Entry Point
→ Render with Style
→ Run Harness
→ Final Output
```

## Harness Selection

Do not run every harness for every task.

### Quick Message Mode

```text
conversation_outcome_harness if relevant
non_offensive_personality_harness if tone is sharp
surface_naturalness_harness
```

### One-on-One Strategy Mode

```text
conversation_outcome_harness
non_offensive_personality_harness
claim_harness
source_fidelity_harness
surface_naturalness_harness
```

### Public Narrative Mode

```text
claim_harness
source_fidelity_harness
narrative_authority_harness
story_harness
emotional_resonance_harness
narrative_entropy_harness
surface_naturalness_harness
```

### Expert Translation Mode

```text
claim_harness
source_fidelity_harness
audience_harness
narrative_entropy_harness
surface_naturalness_harness
```

### Rewrite Recovery Mode

Run the harness corresponding to the diagnosed failure layer.

### Full Narrative Mode

```text
claim_harness
source_fidelity_harness
narrative_authority_harness
story_harness
value_stakes_harness
gap_harness
controlling_idea_harness
audience_harness
emotional_resonance_harness
narrative_entropy_harness
surface_naturalness_harness
```

## Full Narrative Mode Steps (Reference)

Only used when Full Narrative Mode is selected.

### Step 1: Parse Material

Identify:

```text
source type
user request
output format
target audience
known facts
missing facts
```

### Step 2: Extract Claim Boundary

Separate:

```text
explicit facts
reasonable interpretation
assumptions
uncertain claims
forbidden claims
```

See: `mappers/claim_boundary_extractor.md`

### Step 3: Build Story Kernel

Identify:

```text
narrative object
protagonist
desire
old world
obstacle
action
world reaction
gap
turning point
transformation
```

See: `mappers/story_kernel_builder.md`

### Step 4: Map Narrative Authority

Identify:

```text
story owner
author position
central judgment
old world error
opposing force
non-negotiable truth
adaptation boundary
```

See: `mappers/narrative_authority_mapper.md`

### Step 5: Identify Value / Stakes

Identify:

```text
value sought
value at risk
cost of failure
opportunity if success
urgency
reversibility
```

See: `principles/value_stakes.md`

### Step 6: Build Action-Reaction-Gap

Map:

```text
desire
action
expected reaction
actual reaction
gap
new information
value shift
next action
```

See: `principles/action_reaction_gap.md`

### Step 7: Build Controlling Idea

Create:

```text
value statement
cause statement
full controlling idea
proof path
```

See: `principles/controlling_idea.md`

### Step 8: Map Audience Cognition

Identify:

```text
knowledge floor
likely misunderstanding
practical concern
trust barrier
terminology budget
desired belief shift
```

Audience adaptation must not override Narrative Authority.

See: `mappers/audience_cognition_mapper.md`
See: `selectors/audience_entry_point_selector.md`
See: `policies/audience_visibility_policy.md`

### Step 9: Map Affective Arc

Identify:

```text
initial emotion
emotion source
tension
recognition
resolution
final emotion
emotional temperature
```

Emotion must come from protagonist pressure, not decorative language.

See: `mappers/affective_arc_mapper.md`

### Step 10: Map Narrative Entropy

Identify:

```text
audience entropy tolerance
low entropy ground
high entropy turn
surprise point
cognitive load risk
pacing plan
resolution point
```

See: `mappers/narrative_entropy_mapper.md`
See: `principles/narrative_entropy.md`

### Step 11: Select Audience Entry Point

Choose:

```text
risk-first
pain-first
scene-first
mechanism-first
contrast-first
```

### Step 12: Render with Style

Style must obey:

```text
claim boundary
source fidelity
narrative authority
audience cognition
affective arc
output contract
```

See: `renderers/main_renderer.md`
See: `renderers/wrappers/`

### Step 13: Run Harness

Run in this priority order:

```text
1. Claim Harness
2. Source Fidelity Harness
3. Narrative Authority Harness
4. Story Harness
5. Value & Stakes Harness
6. Gap Harness
7. Controlling Idea Harness
8. Audience Harness
9. Emotional Resonance Harness
10. Narrative Entropy Harness
11. Surface Naturalness Harness
```

Not every harness must be exposed or verbose. The system may run compressed checks internally.

If any harness fails, return to the appropriate upstream step. Patch-level fixes to harness failures without returning upstream compound over multiple edits.

### Step 14: Final Output

Default:

```text
Only output final user-facing content.
```

Do not show:

```text
Story Kernel
Narrative Authority Map
Affective Arc
Harness results
internal runtime chain
```

Unless the user explicitly asks for analysis or debugging.

## Audience Visibility

Audience mapping and affective arc are hidden by default.

Show brief framing only when:
- User asks for audience-specific output
- User critiques comprehensibility
- The target audience strongly affects the explanation
- User is testing the skill

See: `policies/audience_visibility_policy.md`

## Output Rule

Default output should not expose:

```text
selected runtime mode
internal mappers
Story Kernel
Affective Arc
Narrative Entropy Map
Harness results
```

Expose internal analysis only if the user asks for debugging, evaluation, or architecture design.

## Artifact Delivery Branch

Use this branch when the user asks for a reusable artifact.

Artifact examples:

```text
README
GitHub README
open-source documentation
email
message
proposal
deck copy
landing page
social post
script
speech
press release
job description
bio
API docs
package documentation
```

## Runtime Order

```text
1. Detect Artifact Type
2. Detect Output Language
3. Preserve User Terms
4. Select Artifact Contract
5. Extract Claim Boundary
6. Render Artifact
7. Run Artifact Contract
8. Run Language Match Harness
9. Run User Term Fidelity Harness
10. Run Artifact Delivery Harness
11. Run Markdown / Format Cleanliness Check
12. Final Output
```

## Priority Rule

For artifact tasks, use this priority order:

```text
1. Artifact Contract
2. Language Match
3. User Term Fidelity
4. Claim Boundary
5. Format Cleanliness
6. Audience Fit
7. Narrative Quality
8. Style
```

Narrative style must not override artifact correctness.

## GitHub / README Special Rule

If artifact_type is one of:

```text
GitHub README
README.md
open-source docs
developer documentation
package README
skill README
```

then Robert Skill must run:

```text
github_readme_output_contract
language_match_harness
user_term_fidelity_harness
artifact_delivery_harness
markdown_cleanliness_harness
```

## Language Rule

If the latest user request is in English and the artifact is GitHub / README / developer-facing documentation, all user-facing output should be English by default.

Do not answer in Chinese unless the user explicitly asks for Chinese analysis or bilingual output.

## Dialogue vs File Rule

Default: deliver the artifact in the dialogue.

Write to a file only if:

```text
the user explicitly asks to save / write / export a file
the workflow context requires file exchange
the user has already established file-based delivery
```

If the user asks "send it in the dialogue", output the content directly.

## False Claim Prevention

Do not invent:

```text
install commands
package availability
GitHub name availability
npm / PyPI / ClawHub status
official integrations
license status
runtime requirements
API requirements
benchmark results
production readiness
```

Use placeholders when unknown.

## Interaction With Other Modes

Artifact Delivery Branch can combine with other modes:

```text
GitHub README → Artifact Delivery + Expert Translation / Public Narrative as needed
Email → Artifact Delivery + One-on-One Strategy
Social post → Artifact Delivery + Public Narrative
Technical docs → Artifact Delivery + Expert Translation
```

Artifact discipline always applies last.

## High-Profile Recipient Branch

Use this branch when the target recipient is a high-profile person, major CEO, investor, senior academic, regulator, celebrity, institutional leader, or well-known expert.

Triggers:

```text
sell to [famous person]
pitch to [CEO / investor / regulator / professor]
message [public figure]
reach out to [senior leader]
convince [high-status recipient]
```

Runtime:

```text
1. Detect High-Profile Recipient
2. Map Recipient Power Context
3. Extract Claim Boundary
4. Map Conversation Purpose
5. Map Narrative Authority
6. Build Proof-Oriented Pitch
7. Render Short Pitch
8. Run High-Profile Recipient Harness
9. Run Proof Challenge Harness
10. Run Source Fidelity Harness
11. Run Surface Naturalness Harness
12. Output Pitch
```

## Notes Rule

Do not include private notes in the default output.

If the user explicitly asks for reasoning, analysis, or behind-the-scenes explanation, add notes clearly separated:

```text
Notes for you, not for the pitch:
```

Otherwise, output the pitch only.

## Priority

```text
1. claim boundary
2. recipient discipline
3. proof challenge
4. small ask
5. narrative authority
6. emotional force
7. style
```

Offer a small proof challenge.

## Personal Communication Mode

Use this mode when the user asks for personal, romantic, friendship, or emotionally sensitive communication.

Triggers:

```text
introduce me to someone
help me text a girl / guy / person I like
ask someone out
recover from awkwardness
I am shy / geeky / awkward
I might not talk well
write a message to someone I like
```

Runtime:

```text
1. Apply Universal Language Lock
2. Detect Personal Communication Mode
3. Map Personal Context
4. Preserve User Personality
5. Choose Low-Pressure Scene
6. Draft Sendable Message
7. Run Personal Communication Harness
8. Run Output Language Lock Harness
9. Output Message + Short Notes
```

Priority:

```text
1. language lock
2. personal safety and naturalness
3. authenticity
4. low-pressure next step
5. sendability
6. emotional reassurance
7. style
```

Output shape:

```text
Short framing
Sendable message
Why it works
Notes for you, not for them
```

For very short tasks, output only:

```text
Sendable message
One note
```

## Known Context Recovery Branch

Use this branch when the user references a known project, product, skill, framework, repo, or internal system.

Triggers:

```text
known project name
known skill name
known product name
known internal architecture
known workspace directory
previously discussed initiative
```

Runtime:

```text
1. Detect Known Entity
2. Recover Context
3. Determine Sufficient Context
4. Preserve Known Boundaries
5. Identify Unknowns
6. Continue to Requested Runtime Mode
7. Mark Assumptions / Placeholders
8. Produce Output
```

## Interaction with Artifact Delivery

If user asks for GitHub README or public artifact:

```text
Known Context Recovery
→ Public Release Artifact Branch
→ Artifact Delivery Branch
→ Final Output
```

Do not ask basic identity questions if the recovered context is sufficient.

## Clarification Rule

Ask only if:

```text
context is missing
context is contradictory
missing information affects public claim safety
installation / license / deployment details are required and unknown
```

If asking, ask one high-leverage question only.

## Language Rule

Known Context Recovery does not change output language.

If user asks in English, output in English.

## Output Rule

Do not expose memory search details or internal recovery process unless user asks for debugging.

A short assumption note is allowed:

```text
Drafted based on available project context. Installation and license details are marked as placeholders.
```

## Output Rule

Do not expose:

```text
selected runtime mode
internal mappers
harness results
analysis notes
debug output
```

unless the user explicitly asks for analysis.

## Public Release Artifact Branch

Use this branch when the user asks to publish, launch, release, or put something on GitHub, a website, marketplace, or public channel.

Triggers:

```text
publish to GitHub
launch
public README
open-source repo
website copy
landing page
marketplace listing
public announcement
release note
```

Runtime:

```text
1. Detect Public Release Intent
2. Map Public Positioning
3. Check Naming / Third-Party Reference Risk
4. Select Public Artifact Contract
5. Detect Output Language
6. Preserve User Terms
7. Extract Claim Boundary
8. Render Public Artifact
9. Run Public Release Harness
10. Run Language Match Harness
11. Run User Term Fidelity Harness
12. Run Markdown Cleanliness Harness
13. Final Output
```

## Public Release Priority

```text
public positioning
naming safety
language match
artifact structure
claim boundary
format cleanliness
narrative quality
style
```

## Output Rule

Do not expose internal positioning map unless the user asks for analysis.

Default: output the public artifact directly.

## Public Artifact Finalization Branch

Use this branch after drafting a public artifact.

Triggers:

```text
GitHub README
public README
open-source docs
launch copy
landing page
marketplace listing
public product page
public skill description
```

Runtime:

```text
1. Detect Public Artifact
2. Map Public Artifact Audience
3. Check Public Name / Third-Party Risk
4. Apply Public Artifact Release Contract
5. Run Public Release Harness
6. Run Markdown Cleanliness Harness
7. Run Public Artifact Final Pass Harness
8. Run Human Release Voice Harness
9. Separate Artifact from Notes
10. Final Output
```

## Human Release Voice Step

For public artifacts, after Public Artifact Final Pass and before Final Output, run:

```text
Human Release Voice Harness
```

## Human Voice Priority

Human voice must improve memorability without violating:

```text
language match
claim boundary
markdown cleanliness
public naming safety
artifact structure
```

## README Release Cleanup Step

For README artifacts, add a final cleanup step:

```text
1. Detect Public Artifact
2. Map Public Artifact Audience
3. Check Public Name / Third-Party Risk
4. Apply Public Artifact Release Contract
5. Run Public Release Harness
6. Run Markdown Cleanliness Harness
7. Run Public Artifact Final Pass Harness
8. Run Human Release Voice Harness
9. Run Public README Release Cleanup Harness
10. Separate Artifact from Notes
11. Final Output
```

## Release Cleanup Priority

```text
1. publishable artifact cleanliness
2. language and notes separation
3. path correctness
4. public link safety
5. license/install placeholder safety
6. claim boundary wording
7. voice polish
```

Do not let voice polish reintroduce unverified claims or messy formatting.

## Priority

```text
1. Public usability
2. Naming / affiliation safety
3. Language match
4. Markdown cleanliness
5. Claim boundary
6. Usage examples
7. Architecture clarity
8. Narrative quality
```

## Public README Rule

Do not start with internal architecture.

If the first screen contains file tree, harness list, mapper list, or development history, rewrite.

## Notes Separation Rule

If there are maintainer notes, naming caveats, or publishing reminders, place them outside the artifact:

```text
Notes for you, not for publication:
```

Do not place them inside the README unless explicitly requested.

## Output Rule

The final response may include:

```text
1. The publishable artifact
2. Optional notes for the user
```

The publishable artifact must be clean on its own.

## Output Contract for Short Explanations

When output < 500 Chinese characters and audience is non-technical:
- No internal reasoning
- No Story Kernel
- No bullet lists unless requested
- Max one analogy
- Start from audience entry point
- End with practical value

See: `contracts/short_explanation_output_contract.md`
