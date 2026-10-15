---
name: daily-english-refresh
description: Refresh the Coline Daily English-learning Site with a current, source-attributed daily reading and matching TEM-4 vocabulary, dictation, and study content. Use when the user asks to refresh, replace, prepare, or publish today's lesson, or to keep this specific Site's daily learning content current. Do not use for unrelated English tutoring or other websites.
---

# Daily English Refresh

Refresh the existing **Coline Daily** Site as one coherent lesson. Treat the article, vocabulary annotations, dictation answers, date, reading time, image attribution, and study prompts as one atomic content record: never update only part of the lesson.

## Target Site

- Site title: `Coline Daily`
- Public URL: `https://coline-daily-english.colinezhou.chatgpt.site/`
- Local checkout: use the current Coline Daily checkout when available; otherwise open the hosted Site through Sites.

Confirm the hosted Site identity from its local `.openai/hosting.json` or the Sites service before writing. Never create a replacement Site when the existing project can be opened.

## Refresh Workflow

1. Determine today's date in the user's `Asia/Shanghai` timezone. Read [lesson-contract.md](references/lesson-contract.md) before composing or validating content.
2. Inspect the current Site and its storage path.
   - Prefer an existing authenticated Site tool or data writer that updates the current daily lesson without rebuilding the Site.
   - If the Site is still source-backed with hard-coded lesson content, open its current source, update the lesson and matching learning data together, build, and publish through the Sites workflow.
   - Preserve the Site's project identity, public audience, layout, personalization, and unrelated features.
3. Research several current candidates from authoritative English-language sources. Prefer primary reporting, public institutions, reputable international newsrooms, science or culture institutions, and TED. Verify publication dates and facts. Choose one topic that is useful, non-graphic, broadly understandable, and suitable for a 3–5 minute English study session.
4. Write an original learning text rather than copying an article. Attribute the source inspiration and retain direct source links in the stored lesson when the Site supports them. Respect copyright limits; use only a very short quotation when it materially aids learning.
5. Select and annotate the TEM-4-level vocabulary actually used in the final text. Generate the matching Chinese-to-English recall list from the same vocabulary objects so spelling checks cannot drift from article annotations.
6. Use a relevant, licensed or source-permitted image with accurate credit, or preserve the existing visual treatment when no compliant image is available. Never invent a photo credit or image URL.
7. Write the complete lesson through the available update path. Do not overwrite the newest valid lesson with an older date. If research, generation, storage, or publication fails, keep the previous lesson live and report the exact failed stage.
8. Verify the saved or published result by reading it back. Confirm the date, title, reading time, article text, every vocabulary annotation, every recall answer, source attribution, and image/credit agree. For source-backed changes, run the appropriate build before publishing and confirm the deployment succeeds.

## Quality and Safety

- Keep the reading at roughly 550–850 English words unless the existing product's measured reading-time logic requires another range.
- Target capable intermediate learners preparing around TEM-4 level. Prefer precise, natural English over artificial density.
- Include 6–10 useful target words. Each word must appear in the article and include a defensible IPA transcription plus a concise Chinese meaning appropriate to its context.
- Avoid graphic tragedy, partisan persuasion, medical directives, investment advice, and other content that would make a daily learning ritual unsafe or needlessly distressing.
- Do not fabricate reporting, citations, dates, quotations, vocabulary status, or analysis results.
- Do not change email reminders, desktop widgets, or other removed features unless the user separately requests them.

## Invocation and Scheduling

An invocation refreshes the lesson once. The Skill itself is not a clock. If the user requests unattended daily updates, first ensure the Site has a verified persistent writer and readback path, then create or update one linked automation for 09:00 `Asia/Shanghai`. Reuse an existing matching schedule and do not create duplicates.

Before an unattended schedule is considered ready, perform one real update through the same writer the scheduled run will use and verify the resulting lesson from the Site.
