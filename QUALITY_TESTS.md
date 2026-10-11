# Quality Tests: Filipino Bugtong Generator

These tests evaluate the skill instructions, not a specific model's general writing ability. A test passes only when the output meets the expected behavior. Poetic style alone is not evidence of quality.

## Test protocol
For each run, record:
- Skill version or commit SHA
- Test ID
- Exact input
- Actual output
- Pass or fail
- Specific reason
- Proposed correction, if needed

Do not treat one successful example as proof of general reliability. Rerun relevant tests after changes to clue construction, indirectness, language, difficulty, or output format.

## Q-001: Overly literal clues
**Purpose:** Check whether the riddle directly names the answer's category, component, or primary function when a familiar indirect clue could work.

**Failure example:**
> May motorsiklong humihila, may karwaheng sakay sa tagiliran. Sa mga daan ng barangay, pasahero ang aking dinadala.

Intended answer: Traysikel.

**Why it fails:** It names a motorcycle and passengers, exposing both the vehicle type and its main function.

**Expected behavior:** Describe recognizable, concrete details such as the sidecar's position or the vehicle's familiar appearance without directly naming the answer's category or function.

## Q-002: Excessive ambiguity
**Purpose:** Check whether many common answers fit the clues equally well.

**Fail when:** Two or more familiar answers fit about as well as the intended answer and the riddle contains no distinguishing clue.

**Expected behavior:** Add a true, discriminating detail or select a more suitable answer.

## Q-003: Unnatural Filipino
**Purpose:** Check for stiff translations, unusual word order, or expressions that a Filipino speaker would not naturally use.

**Fail when:** Wording distracts from the clues or requires the reader to reinterpret an awkward phrase.

**Expected behavior:** Prefer familiar Filipino vocabulary and natural sentence flow.

## Q-004: False or misleading clues
**Purpose:** Check factual accuracy and metaphorical fairness.

**Fail when:** A clue is factually wrong and the metaphor does not provide a reasonable interpretation.

**Expected behavior:** Replace the clue with an accurate detail or a clear, understandable metaphor.

## Q-005: Forced rhyme
**Purpose:** Check whether rhyme has damaged accuracy or naturalness.

**Fail when:** A word or phrase appears chosen mainly to rhyme and makes the clue inaccurate, awkward, or less clear.

**Expected behavior:** Keep clarity and truth ahead of rhyme.

## Q-006: Obscure knowledge
**Purpose:** Check whether the intended answer depends on knowledge outside the requested audience's likely experience.

**Fail when:** An ordinary Filipino reader would need niche facts not established by the clue or requested by the user.

**Expected behavior:** Use familiar concepts, unless the user specifically requests specialist or obscure material.

## Q-007: Answer giveaway
**Purpose:** Check whether a clue states the answer or effectively names it through an obvious synonym or definition.

**Fail when:** The answer is revealed rather than inferred.

**Expected behavior:** Preserve a fair inference while removing direct answer leakage.

## Q-008: Excessive abstraction
**Purpose:** Check that symbolic clues remain concrete and interpretable.

**Fail when:** Images or metaphors could mean almost anything and do not help narrow the answer.

**Expected behavior:** Ground symbolism in recognizable properties, actions, contrasts, or ordinary experiences.

## Q-009: Difficulty calibration
**Purpose:** Check whether the output matches the requested difficulty.

**Fail when:** An easy riddle is obscure, a medium riddle is merely literal, or a hard riddle relies on arbitrary leaps.

**Expected behavior:** Increase inferential distance thoughtfully, without sacrificing fair solvability.

## Q-010: Output compliance
**Purpose:** Check exact count and requested format.

**Fail when:** The generator returns the wrong number of riddles, reveals answers when asked not to, or adds unrequested explanations.

**Expected behavior:** Follow the requested count, language, answer visibility, difficulty, and format exactly.
