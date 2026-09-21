# Amagadon Regression Test Results

## Project Information

**Assistant:** Amagadon - AI Marketing Assistant  
**Owner:** Thandoluhle Hlatshwayo  
**Programme:** AI Fluency Project  
**Track:** Track B: Marketing  
**Platform:** Claude.ai Projects  
**Final Evaluated Version:** Amagadon v1.4

---

# Purpose

Initial testing identified two recurring weaknesses in Amagadon's
behaviour:

1. Unsupported broad generalisations
2. Strategic over-assumption when marketing briefs were extremely vague

The Project Instructions were refined to address these issues.

Two targeted regression tests were then performed to determine whether the
changes successfully corrected the identified behaviour without reducing
Amagadon's usefulness.

---

# Improvement Issue 01

## Unsupported Broad Generalisations

During initial testing, Amagadon occasionally introduced statements such
as:

> "Most people don't gain confidence with AI by only reading about it."

and statements using phrases such as:

- most people
- many people
- people often
- employees usually
- organisations generally
- tends to

These statements sounded plausible but were not always explicitly
supported by the user's brief or Project Context.

## Corrective Action

Amagadon's instructions were updated with generalisation-control logic.

The revised behaviour required Amagadon to:

- remain faithful to supplied source material
- identify unsupported broad statements
- avoid converting plausible ideas into facts
- rewrite unsupported generalisations using source-grounded language
- use questions where appropriate
- omit unsupported claims where necessary
- flag important unsupported claims for verification

---

# Regression Test 01 - Unsupported Generalisations

## Purpose

Verify that the correction for Improvement Issue 01 successfully prevented
unsupported broad generalisations while preserving useful and engaging
marketing content.

## Test Conditions

Amagadon was asked to create three LinkedIn posts about learning to use AI
at work.

The supplied brief included:

- target audience: HR and Learning and Development leaders
- objective: build awareness
- central message: employees can develop practical AI skills by applying
  AI to real workplace tasks
- maximum 600 characters per post
- maximum two hashtags
- no emojis
- no invented evidence, statistics or research

---

## Results

- Three variations generated: PASS
- Source fidelity: PASS
- No unsupported "most people" claim: PASS
- No unsupported "often/usually/generally" claim: PASS
- No unsupported "tends to" claim: PASS
- No fabricated statistics or research: PASS
- Content remained engaging: PASS
- Variations genuinely different: PASS
- LinkedIn requirements followed: PASS

**Score:** 9/9

**Overall Result:** PASS

---

## Observation

The improvement was visible in Amagadon's wording.

Instead of making unsupported broad statements, Amagadon used
source-grounded language.

For example:

> "Practical AI skills can start with one real task."

Amagadon also used appropriate questions rather than converting assumptions
into factual claims.

The generated content remained:

- useful
- professional
- creative
- platform appropriate
- source grounded

The factual improvement did not make the marketing content excessively
cautious or unusable.

---

## Regression Test 01 Conclusion

**Improvement Issue 01 successfully addressed.**

No further instruction modification was required for this issue.

---

# Improvement Issue 02

## Strategic Over-Assumption on Vague Briefs

During initial Test 07, Amagadon received the prompt:

> "Create three LinkedIn posts about AI."

The earlier assistant version recognised that information was missing but
still assumed:

- a general professional audience
- an awareness and engagement objective
- a general workplace AI focus

These assumptions materially influenced the marketing strategy.

The assistant should instead have asked the user for strategically
important information.

---

## Corrective Action

Amagadon's Project Instructions were updated to distinguish between:

### Minor Missing Information

Information that can use configured defaults without materially changing
the marketing strategy.

Examples include:

- optional character limits
- optional emoji preferences
- optional hashtag preferences

### Strategically Important Missing Information

Information where different answers would materially change the marketing
output.

Examples include:

- target audience
- marketing objective
- specific topic focus when the topic is extremely broad
- platform
- what is being promoted when unclear

When strategically important information is missing, Amagadon must ask
concise clarification questions before generating content.

---

# Regression Test 02 - Vague Brief Handling

## Test Prompt

> "Create three LinkedIn posts about AI."

The exact vague scenario that previously revealed the weakness was used
again.

---

## Expected Behaviour

Amagadon should:

1. Recognise that LinkedIn is already specified.
2. Recognise that the marketing brief is strategically incomplete.
3. Ask for the target audience.
4. Ask what the reader should understand, feel or do.
5. Ask what specific aspect of AI should be communicated.
6. Avoid assuming an audience.
7. Avoid assuming a marketing objective.
8. Avoid inventing a product or campaign.
9. Avoid generating posts prematurely.
10. Keep clarification concise.

---

## Results

- Recognised the brief was strategically underspecified: PASS
- Recognised LinkedIn was already specified: PASS
- Asked for target audience: PASS
- Asked for objective or desired reader outcome: PASS
- Asked for specific AI focus: PASS
- Did not assume audience: PASS
- Did not assume objective: PASS
- Did not invent a product, campaign or use case: PASS
- Did not generate posts prematurely: PASS
- Questions were concise and relevant: PASS

**Score:** 10/10

**Overall Result:** PASS

---

## Observed Response Behaviour

Amagadon correctly explained that additional information was required
because the answers would change the strategy of the posts.

The assistant confirmed that LinkedIn was already known and requested only
three strategically important details:

1. Who should the posts speak to?
2. What should readers understand, feel or do?
3. What specific aspect of AI should the posts focus on?

Amagadon did not generate generic posts while waiting for those details.

---

## Regression Test 02 Conclusion

**Improvement Issue 02 successfully addressed.**

No further modification was required for this issue.

---

# Regression Test Summary

| Test | Issue Tested | Score | Result |
|---|---|---:|---|
| Regression Test 01 | Unsupported broad generalisations | 9/9 | PASS |
| Regression Test 02 | Strategic over-assumption on vague briefs | 10/10 | PASS |

---

# Final Validation Position

Following the initial testing and targeted refinement:

**Initial test scenarios:** 10  
**Regression tests:** 2  
**Critical failures remaining:** 0  
**Improvement issues identified:** 2  
**Improvement issues resolved:** 2  
**Final evaluated version:** Amagadon v1.4  

## Final Status

**PILOT DEPLOYMENT READY**

Amagadon v1.4 demonstrated that the two meaningful weaknesses discovered
during initial testing had been successfully addressed.

The final version maintained:

- three distinct marketing variations
- platform adaptation
- brand voice
- source fidelity
- factual accuracy
- character-limit compliance
- responsible marketing guardrails
- clarification behaviour
- human review before publication

---

# Important Deployment Principle

Regression test success does not remove the requirement for human review.

Amagadon remains an AI marketing drafting assistant.

Generated content must be reviewed and approved by an authorised human
before publication.

Future pilot testing with real users should continue monitoring:

- factual accuracy
- brand alignment
- editing required
- user satisfaction
- task completion time
- unsupported claims
- clarification quality

END OF AMAGADON REGRESSION TEST RESULTS
