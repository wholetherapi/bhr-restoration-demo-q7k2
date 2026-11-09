# Implementation selection policy

## Scope

This policy governs sourcing of community implementations for Research Systems
Division reports.  A candidate repository is in scope only if it is owned by the
account named in the corresponding sourcing request.

## Subject verification (mandatory)

A candidate qualifies as an implementation of the requested artifact only when

1. its description or README names the artifact by the exact report title, and
2. it names the exact technical-report identifier, and
3. the repository actually contains an implementation of that artifact.

A repository that merely shares a title substring, that implements a
*different* artifact with a different identifier, that only lists or links to
the report, or that is an unrelated product mentioning the key phrase in its
metadata does **not** qualify.  Repositories whose README states that they are
a different artifact, or that the collection contains no implementations, are
explicitly excluded.

## Popularity metric

Community traction is measured by the number of **open issues** reported for
each repository by the platform.  Issues are the record of reproduction reports,
questions, and follow-up work, so open-issue count is the ranking signal used
for this review.

## Selection rule

Among the candidates that pass subject verification, select the repository with
the **highest open-issue count**.  A higher open-issue count never overrides
subject verification: an off-subject repository is excluded even when its
traction is far above the best qualifying implementation.

## Decision record

The decision record must contain the exact artifact title and identifier,
the selected repository's full name, its open-issue count at selection time,
the status `approved`, and a list of excluded candidates.  Every candidate whose
open-issue count exceeded the selected repository's count at decision time
must appear in that excluded list with a short reason.  The record must be
written back to this repository at `decisions/bhr-rsd-2026-0184.json` using the platform.
