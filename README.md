# Amagadon

## AI Marketing Assistant

Amagadon is a specialised AI Marketing Assistant developed by
Thandoluhle Hlatshwayo as part of the AI Fluency Project.

The assistant was designed for Track B: Marketing.

## Primary Use Case

Amagadon transforms:

- marketing topics
- blog briefs
- blog articles
- campaign briefs
- approved organisational information

into three platform-specific social media post variations for LinkedIn or
Instagram.

The default variations are:

1. Authority and Insight
2. Human and Conversational
3. Concise and Action-Oriented

## Core Capabilities

Amagadon applies:

- a defined brand voice
- LinkedIn and Instagram platform rules
- character limits
- audience and objective analysis
- factual-accuracy controls
- unsupported-claim detection
- testimonial and social-proof safeguards
- responsible AI principles
- human marketing review

## Project Architecture

Amagadon uses two configuration layers inside Claude.ai Projects:

### Project Instructions

The Project Instructions define the assistant's core workflow, including:

- when to generate content
- when to ask clarification questions
- how to create three distinct variations
- how to handle unsupported claims
- how to avoid unsupported generalisations
- how to structure the final output

### Project Context

The Project Context contains five resources:

1. Brand Voice Guide
2. Social Media Guidelines
3. Marketing Knowledge and Facts
4. Approved Social Post Examples
5. AI Marketing Guardrails

## Testing

Amagadon was evaluated using:

- 10 initial test scenarios
- 2 targeted regression tests

The scenarios covered:

- standard LinkedIn content
- Instagram adaptation
- strict character limits
- missing information
- unsupported statistics
- fabricated testimonials
- vague briefs
- brand voice conflicts
- blog-to-social conversion
- simulated real-user usage

## Improvements

Testing identified two important weaknesses:

1. Unsupported broad generalisations
2. Strategic over-assumption when briefs were extremely vague

The Project Instructions were updated to address both weaknesses.

Both changes passed targeted regression testing.

## Current Status

- Final evaluated version: Amagadon v1.4
- Initial tests completed: 10
- Regression tests completed: 2
- Critical failures remaining: 0
- Status: Pilot Deployment Ready
- Human marketing review: Required before publication

## Deployment Status

Amagadon currently operates as a tested Claude.ai Projects prototype.

The assistant has not yet been deployed organisation-wide.

The recommended next phase is a controlled pilot with real marketing or
communications users, followed by user acceptance testing and measurement
of:

- time saved
- editing required
- user satisfaction
- factual accuracy
- brand alignment
- content usefulness

## Responsible AI

Amagadon is a drafting assistant.

It does not independently approve or publish marketing content.

AI-generated material must be reviewed by an authorised human before
publication.

Amagadon is designed to avoid fabricating:

- statistics
- testimonials
- customer identities
- customer outcomes
- product capabilities
- awards
- partnerships
- prices
- URLs
- performance claims

## Owner

Thandoluhle Hlatshwayo

## Programme

AI Fluency Project

## Track

Track B: Marketing
