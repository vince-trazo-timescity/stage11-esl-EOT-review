# Write with Purpose · Stage 11

A static writing practice studio for Vinschool Times City · Mr. Vincent.

Live: https://vince-trazo-timescity.github.io/stage11-esl-EOT-review/

## Learning journey

Plan → infer vocabulary → practise language → develop a paragraph → draft → review → revise → reflect. The flexible thinking tool is Point, Explanation, Relevant example, Analysis, Link back. Essays reconnect to a thesis; biographies explain the significance of an achievement or admirable quality.

Both opinion essays about volunteering and biographical articles have Foundation, Core and Challenge pathways. Each route has 15 closed checkpoints (90 route-specific records), plus original paragraph tasks, context inference, vocabulary transfer, collocation comparisons, planning, drafting and reflection. Writing is shared across pathways but saved separately for each exact prompt. Closed practice results stay separate by genre and pathway.

The nine original vocabulary units are retained. All 40 reference-page prompts are active, with a total of 52 tasks across 12 writing formats. Unit 8 comparison projects, Unit 10 presentation scripts, Unit 12 discussion/talks and volunteering webpage text have active tasks. Vocabulary, linker and genre quizzes, the full eight-category language reference, shuffleable context cards, optional definition lists, unit navigation, saved genre checklists, practice XP/levels and participation records are available. XP uses attempted closed questions (5 points) and correct first attempts (5 extra); retries add no points and levels are participation milestones, not grades. A focused biography bank is added; 150 vocabulary entries include two contexts and natural phrases. The archived original data is in `assets/legacy-units.json` and `assets/legacy-tasks.json`.

## Source of truth

The supplied October 2026 `Pasted text.txt` writing standards govern UO 1.g a–e, UO 2.h a–e, and LO 1.5.a a–b. UO 2.h includes essay and webpage writing. The studio supports webpage text drafting but does not certify the usability or navigation of a built webpage. Other genres have explicitly labelled genre self-review criteria because matching school standards were not supplied. The supplied British Council *An opinion essay* C1 PDF informed supplementary guidance only. School standards take priority over C1 conventions. Practice models are original; the biographical model is fictional. The teacher page maps activities to criteria.

The suggested 200–250-word target and 25-minute timer are configurable practice defaults, not claimed school assessment requirements. Change `config` in `assets/curriculum.js` to adjust default targets and duration; students can adjust the timer from 1–120 minutes or choose Untimed. Independent mode hides frames and models. No timer automatically submits, clears or locks a draft.

## Honest writing feedback

`assets/engine.js` performs a **small set of browser pattern checks**, not AI analysis. It quotes actual submitted sentences, maps detected patterns to genre criteria, suggests limited wording changes, and selects three passages for self-review of focus, support and links. It assigns no writing score, band or achievement grade. Length, keyword presence, paragraph breaks and linkers are not proof of reasoning or coherence. No matched error is not a clean bill of health. Off-topic warnings are explicitly tentative because paraphrases may be valid.

Resubmission stores up to eight distinct versions per task. Comparisons explain which detected patterns disappeared or remain; they do not claim improved reasoning. Review the quoted original and revised wording with a teacher or peer.

Comprehensive personalised analysis would require a separate server/serverless endpoint and an analysis service, with server-side credentials, criterion-bound prompts, validated quotations, privacy/retention controls, rate limiting, and evaluation against teacher-reviewed examples. None is connected, and no API key belongs in these frontend files. The current site remains fully usable without that dependency.

## Saving, recovery and privacy

Data is saved in `localStorage` under `stage11-writing-studio-v3`, only in the current browser/device. There is no student-text upload, account system, analytics or external font request. Copy/download a draft or export a JSON backup before switching device or clearing browser storage. Export dialogs provide a persistent save link and copyable text if downloads are restricted. Restore accepts a JSON file or pasted JSON through the same validated schema-3 flow; unsafe/malformed files are rejected. Newer current drafts win over older imported drafts. Other restored collections use imported values.

Use one writing tab at a time. A detected change from another tab pauses local saving in the current tab to avoid silently overwriting work; export its text before reloading. Storage failures leave work available in the session with a backup warning. Incompatible/corrupt saved raw data is kept untouched and can be exported. Reset controls explain their scope and confirm before clearing original work; only this studio's key is replaced.

The previous site stored work in memory only. Previously closed-tab work cannot be recovered. Existing open old-version tabs should copy/export their drafts before reloading. Unrelated storage keys and the existing `home`/`index-2` files are preserved.

## Development and verification

No production dependencies or build step. The regression tests use jsdom as a development dependency:

```sh
npm ci
npm run dev -- --port 4173
npm test
```

Open `tests/responsive.html` to inspect 390px, 768px, 1366px and 320px iframe viewports. See `VERIFICATION.md` for what was tested and limitations. The app can be served from any static server, including GitHub Pages. Downloaded source works offline when served locally; an initial offline visit to GitHub Pages is not supported by a service worker.

CTA regression coverage in `tests/cta.test.cjs` checks all 396 page/genre/pathway combinations, all 52 task destinations, scoped resets, exports, restoration, timers, revisions and clipboard/print invocation. DOM simulation does not certify native browser downloads or physical printing. Edited drafts display a notice when their visible feedback belongs to the previous submission. Navigation cancels an open reset dialog to prevent clearing a different task after browser history changes.
