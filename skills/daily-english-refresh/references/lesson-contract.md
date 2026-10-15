# Daily Lesson Contract

Use this contract when composing, writing, or verifying a Coline Daily lesson. Adapt field names to the Site's current implementation without losing the relationships below.

## Lesson identity

- `date`: calendar date in `Asia/Shanghai`; one current lesson per date.
- `title`: concise English editorial title.
- `dek`: one-sentence English summary.
- `category`: short uppercase label suitable for the existing source pill.
- `readingMinutes`: integer from 3 through 5, estimated from the final text rather than copied from the prior lesson.

## Article

- `paragraphs`: original English learning text of roughly 550–850 words.
- `quote`: optional and short; omit unless verified and useful.
- `sourceNote`: clearly states that the lesson is an original learning text inspired by reporting or talks.
- `sources`: at least one direct URL, source title, publisher, and publication date. Prefer two independent sources for factual news synthesis; one primary source is acceptable for a TED talk or institutional announcement.

## Vocabulary

Store one ordered array of 6–10 objects:

```json
{
  "word": "resilient",
  "phonetic": "/rɪˈzɪliənt/",
  "meaning": "有韧性的；能复原的"
}
```

Each target word must:

- appear in the final article with the same spelling and intended sense;
- be appropriate for TEM-4-oriented practice or a closely useful adjacent level;
- have a checked IPA transcription;
- have a concise contextual Chinese meaning;
- serve as both the inline annotation and the exact answer for recall mode.

Do not maintain a separate hand-written answer list when the interface can derive answers from this array.

## Image

- `imageUrl`: a verified usable image URL or a Site-owned asset.
- `imageAlt`: factual description of the image.
- `imageCredit`: accurate creator/source credit.
- `imageSourceUrl`: page on which the image and reuse information can be verified when applicable.

If no compliant image is available, retain a non-misleading existing background treatment and omit false attribution.

## Atomic verification

After writing, confirm all of the following in the saved or deployed lesson:

1. The displayed date matches the lesson date.
2. The reading-time label is 3–5 minutes and plausible for the final word count.
3. Every annotated word exists in the vocabulary array.
4. Every vocabulary object appears in the article.
5. Recall-mode Chinese prompts and English answers are derived from the same objects.
6. Sources and image credits resolve and match their claims.
7. The previous valid lesson remains available if the new write or publication failed.
