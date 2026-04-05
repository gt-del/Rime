# AGENTS.md

This repo is a Rime config repo.

You MUST make the smallest working change, preserve current behavior unless the request requires change, and keep edits easy to diff and revert.
You MUST edit `.custom.yaml` first and use base files ONLY IF the change cannot be done safely there; You MUST NOT edit unrelated platform files.
You MUST NOT copy large upstream config blocks; You MUST patch only required keys.
You MUST NOT change schema structure or dictionary wiring, and MUST NOT add any dictionary, scheme, entrypoint, or dependency unless the user explicitly asks.
You MUST keep dictionary formats and headers intact and MUST NOT bulk reorder dictionary entries unless required.
`custom_phrase.txt` MUST be used only for fixed personal phrases or hard overrides; it MUST NOT be used as a general English or technical terms dictionary.
High-risk paths are `engine/processors`, `engine/translators`, `engine/filters`, `recognizer`, `speller/algebra`, and `translator/dictionary`.
For high-risk changes, you MUST verify syntax locally before editing, MUST use a patch style already proven in this repo ONLY IF such an example exists, and MUST NOT submit an unverified patch.
You MUST prefer root source files and MUST NOT edit `build/` unless the user explicitly asks for generated output changes.
You MUST treat this repo as user-owned syncable config and MUST NOT rename, delete, or destructively clean files unless the user explicitly asks.
Before claiming a change is ready, you MUST verify YAML structure and patch target, verify the change belongs in `.custom.yaml` if possible, and state whether Rime redeploy is required.
If runtime behavior cannot be confirmed locally, you MUST say so.
