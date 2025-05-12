# ADR-003: Redesign Form Workflow into Step-wise and Partial Saving

## Status

Proposed - 13/05/2025

## Context

Current implementation of the forms is very long and hard to complete from a user perspective. Some of the form contains 40+ fields. And related to this the validations of all these fields could be very confusing for the end users. And from backend perspective, the API consumes all of this data at once, which is not a good practice.

## Decision

- Break forms into logical steps or sections.
- Add partial save after each step or sections.
- Redesign APi to accept partial save after record creation.
- Validate each section seperately and then progress to next one.

## Consequences

- Better UX and fewer errors due to user entry
- More granular backend APi
- Easier to manage readability and better developer exoerience.

## Alternatives Considered

- Also can identify, minimum required fields for each forms and the user can create the record and enter the other details later. (This approach will not give huge benefit considering the effort required to refactor)
