# Coline Daily English Skill

An agent skill for refreshing the Coline Daily English-learning Site with a current, source-attributed reading and matching TEM-4 vocabulary and recall activities.

## What it does

- researches a current topic from authoritative English-language sources;
- writes an original 3–5 minute learning text;
- selects 6–10 useful TEM-4-level words with IPA and Chinese meanings;
- derives article annotations and recall answers from the same vocabulary data;
- updates the existing Coline Daily Site without changing its identity or audience;
- verifies the lesson and deployment while preserving the previous valid lesson on failure.

## Included skill

`daily-english-refresh`

The skill is stored at `skills/daily-english-refresh/` and includes its workflow, interface metadata, and daily lesson data contract.

## Use

Invoke it explicitly in Codex:

```text
$daily-english-refresh Refresh today's Coline Daily article and learning activities.
```

It can also be selected automatically for requests such as:

```text
Refresh today's Coline Daily lesson and publish it.
```

One invocation performs one refresh. A separate linked automation is required for unattended daily updates.

## Personal installation

Copy the skill folder into your personal Codex skills directory:

```bash
cp -R skills/daily-english-refresh ~/.codex/skills/
```

Restart Codex after installation if the skill is not discovered immediately.

## Configuration

The workflow targets the public Coline Daily Site by default. A user must have permission to edit that Site. To reuse the workflow with another Site, update the target title and URL in `SKILL.md` and preserve the lesson contract.

## Privacy and credentials

This repository contains no API keys, repository credentials, email addresses, or Site authorization tokens. Authentication remains in the user's connected Sites and Codex environment.
