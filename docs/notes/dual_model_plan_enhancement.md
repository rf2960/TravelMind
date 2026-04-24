# Dual-Model Plan Enhancement Note

This note documents the design idea behind TravelMind's plan-enhancement mode.

## Goal

The enhancement workflow was designed to improve an existing user itinerary instead of generating a trip from scratch. The intended value was to help users refine rough plans they already had by adding structure, suggestions, and practical detail.

## Proposed Workflow

1. Accept an existing user itinerary or outline.
2. Interpret the requested enhancement mode, such as:
   - enhance
   - modify
   - fill gaps
   - optimize
3. Use one model to generate travel-specific suggestions and observations.
4. Use a second model to turn those ideas into a cleaner, more structured response.
5. Return an updated itinerary with clearer organization, richer detail, and better usability.

## Why Use Two Models

The design rationale was to combine:

- a travel-oriented model for domain-flavored ideas and recommendations
- a stronger structured-output model for formatting, coherence, and controllability

This separation reflects a broader systems idea: different models may be useful at different stages of an AI workflow.

## Intended Benefits

- more helpful refinement for users who already know their destination
- clearer distinction between generation and enhancement modes
- better support for iterative planning instead of one-shot outputs
- room for graceful fallback if one model is unavailable

## Current Public Scope

This repository includes the architecture and planning note for this feature, but not a full public implementation of the dual-model pipeline.
