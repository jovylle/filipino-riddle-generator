# Story Maker Project Integration

## Current constraint

The Google Flow Story Maker runs as a ChatGPT Project without GitHub connector access. ChatGPT therefore cannot reliably fetch the private `SKILL.md` directly from this repository during a conversation. A GitHub URL in Project instructions does not grant private-repository access.

## Recommended integration: synchronized Project file

Keep GitHub as the canonical source and attach a copy of `SKILL.md` to the Story Maker ChatGPT Project.

- Canonical source: `SKILL.md` on the `dev` branch while developing.
- Runtime source: the `SKILL.md` file attached to the Story Maker Project.
- Sync policy: after an approved and tested skill change, download the updated file from `dev` and replace the Project's attached copy.
- Do not treat a chat decision or GitHub commit as a completed runtime update until the Project file has been replaced.
- Keep the repository private; do not publish the skill merely to make it fetchable.

## Suggested Story Maker Project instructions

Add the following to the Story Maker Project instructions, adapting the surrounding story workflow as needed:

> **Filipino Riddle Generator Skill**
>
> When a story task requires a Filipino bugtong, use the attached `SKILL.md` file named **Filipino Riddle Generator Skill** as the authoritative generation rules. Read and follow it before creating the riddle.
>
> Apply the story's specific requirements, including intended answer, audience, tone, difficulty, and placement, without violating the skill's clue-quality and fairness rules.
>
> Do not claim to have fetched or checked the latest GitHub version. The attached file is the runtime copy and may lag behind the repository. If the skill file is missing or inaccessible, say so rather than inventing its rules.
>
> Generate riddles only when the story workflow calls for one. Do not output a riddle when the current task does not need one.

## Sync procedure after a skill change

1. Review and test the changes on `dev`.
2. Download `SKILL.md` from https://github.com/jovylle/filipino-riddle-generator/blob/dev/SKILL.md
3. In the Story Maker ChatGPT Project, replace the old attached skill file with the newly downloaded version. Keep its recognizable name, such as `Filipino Riddle Generator Skill.md`.
4. Confirm the new file is attached and readable in that Project.
5. Record in the development conversation that the runtime copy was synced, including the Git commit or revision used.

## Why not a private-file URL in Project instructions?

A private GitHub URL requires authentication. A ChatGPT Project without the GitHub connector cannot use that URL as a dependable runtime retrieval mechanism. An authenticated API would add infrastructure and would still need a supported way for the Project to call it. The attached-file workflow is the smallest reliable option for this setup.
