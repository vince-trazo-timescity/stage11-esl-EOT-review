# Verification · October 2026 overhaul

## Automated checks — passed

`npm test`: 7 tests passed, 0 failed.

- All six genre/pathway routes: 90 uniquely identified checkpoints, answer keys, explanations and hints; five linker relationships per route.
- All 150 vocabulary entries: different inference/transfer contexts, collocations, and context evidence actually present in the inference sentence.
- Developed, underdeveloped, off-topic, short, empty and repetitive submissions: quoted passages occur in the submitted text, priorities capped at three, no writing grades.
- Specific agreement, collocation and register edits preserve surrounding text and map to the genre standard; a valid “Does she have…?” question is not flagged.
- Version comparison reports pattern changes with an explicit semantic-quality limitation.
- Smart apostrophes, case, trailing punctuation and authored alternative sentence orders are accepted.
- Valid backup state is accepted; malformed collections, draft records, timers and unsafe keys are rejected.
- JavaScript syntax checks passed for application and engine.

## Browser checks — passed

Cloud Chrome, local static preview:

- Vocabulary definitions absent initially; empty inference submission asks for prediction/clue; optional hint and explicit definition support; reveal after an attempt; transfer wrong/correct retries; original vocabulary sentence entry.
- Natural phrase comparison explains the distinction, including grammatical possibility versus unnatural collocation.
- Empty closed answer records no attempt; repeat checking is disabled; a wrong-then-correct retry retains the original first-attempt result. An authored alternative sentence order is accepted.
- Draft feedback exercised on empty, short, underdeveloped, off-topic and developed text, plus a passage with three concrete language patterns. Feedback quotes actual sentences, gives edits and avoids unsupported grades.
- Revision history adds distinct text only; rechecking unchanged text does not add a version. Pattern-removal comparison shown.
- Genre/pathway switches and reload retain task-specific draft text; biography review uses central focus/significance and UO 1.g, not an essay thesis.
- Independent mode hides support. Adjustable timer starts, pauses, resets and supports Untimed. Actual countdown reached zero; text remained editable and no automatic submission occurred. Timer reload restores remaining duration paused.
- All nine pages measured at 390, 768, 1366 and 320px iframe widths: no document-wide horizontal overflow; form controls have labels. Navigation/reference tables can scroll within their own containers.
- Copy button reported successful copying. Draft-reset cancellation kept the draft.
- Export dialog contains actual schema-3 JSON and the saved drafts, a persistent download link and a selectable-text fallback.

## Verification limits / remaining checks

- Cloud browser download-event capture timed out even though export preparation and save-link activation completed. A completed downloaded file was not obtained. The copyable-text fallback was added and inspected. Do not report a fully verified native download.
- File chooser/restore interaction stalled in the browser tooling. Browser import round trip and destructive reset confirmation are not marked verified. Backup schema validation is covered by automated tests; import uses that validator.
- Print participation record styling is implemented; physical printing and PDF pagination have not been verified.
- Responsive checks are browser iframe viewport checks, not physical-device Safari/Firefox or screen-reader testing. Labels, semantic controls, focus styling, live statuses and reduced-motion support are present; this is not a formal accessibility certification.
- Static pattern checks cannot establish sound reasoning, factual accuracy, relevance, collocation/grammar overall or mastery. Human review remains essential. Extended vocabulary examples inherited from the original reference need normal teacher editorial review.
- Local storage is not cloud sync. Backups remain necessary; simultaneous writing tabs are guarded by pausing saves when another tab changes the stored record.

Deployment status is reported separately after the commit and live-page verification.
