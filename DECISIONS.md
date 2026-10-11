# Design Decisions

This file records decisions about the Filipino Bugtong Generator. A discussion in chat is not an implemented change until the relevant source files are updated and committed.

## D-001: Human guessability is the primary quality goal
**Status:** Accepted  
**Decision:** Prefer fair, recognizable clues over cleverness that depends on obscurity.  
**Rationale:** A good bugtong hides the answer, not the logic.

## D-002: Prefer indirect clues over literal definitions
**Status:** Accepted  
**Decision:** When a familiar visual detail, behavior, contrast, or everyday association can communicate a clue, do not directly name the answer's category or primary function.  
**Rationale:** Literal clues leak the solution and weaken the riddle-solving experience.  
**Example:** For a traysikel, a small compartment beside the driver is more indirect than explicitly naming a motorcycle and passengers.

## D-003: Symbolism must remain concrete
**Status:** Accepted  
**Decision:** Symbolism should make clues memorable, not impossible to interpret. Every clue should contribute meaningful information toward the answer.  
**Rationale:** Abstract language without a clear connection creates random guessing.

## D-004: Natural Filipino takes priority over decorative language
**Status:** Accepted  
**Decision:** Use familiar, idiomatic Filipino. Do not force rhyme or poetic wording at the expense of naturalness or clue accuracy.

## D-005: Generate independently during ordinary use
**Status:** Accepted  
**Decision:** Do not browse for or copy existing riddles during ordinary generation. Use research only when explicitly requested.

## D-006: Validate before returning
**Status:** Accepted  
**Decision:** Check comprehension, specificity, competing answers, clue accuracy, fairness, answer leakage, and output compliance before finalizing.

## D-007: This repository is for skill engineering
**Status:** Accepted  
**Decision:** The project focuses on developing, testing, and maintaining the generator skill. Generate sample riddles only when needed to test a specific rule or investigate a failure.

## Change proposal template
For each proposal, record:
- **Problem:** Concrete observed failure or defined requirement.
- **Evidence:** Examples or repeated test results.
- **Proposed change:** Smallest effective instruction or test change.
- **Expected benefit:** Target behavior expected to improve.
- **Regression risk:** Existing strengths that might be harmed.
- **Decision:** Accept, reject, or test further.
- **Implementation:** Commit or pull request that applies the decision.
