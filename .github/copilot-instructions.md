<!-- Copilot instructions for "dictionary-and-loops-practice" -->

# Quick orientation

This repository is a small set of Python classroom exercises that teach dictionaries and lists through guided prompts and starter datasets (no external services or deps).

Key points:
- Primary language: Python (vanilla, run with `python3 <file>.py`).
- Files are organized by day under `day_1_activities/`, `day_2_challenge/`, and `day_3_uber_eats_challenge/`.

# What the codebase is for (the "why")
- These are learning prompts: each `*.py` file is a project prompt (comments describe the desired behavior). Implementations should preserve the pedagogical intent and prompts.
- Starter datasets live in small modules (e.g., `student_data.py`, `orders.py`) and are intentionally simple, using lists of dictionaries as the canonical data model.

# Patterns and conventions to follow
- Data model: lists of dictionaries (each record is a dict). Keys are strings and sometimes include punctuation (example: `"Combo,Name"` in `student_data.py`).
- No heavy framework or packaging; prefer small, self-contained changes and avoid adding runtime deps.
- Many exercise files are intentionally interactive (`input()` and `print()` based). When adding automated tests or refactoring, make interactions optional (e.g., extract logic into functions that accept arguments and return values so tests can call them non-interactively).

# Running and quick checks
- Run a single exercise: `python3 day_1_activities/2_main.py` (or any other exercise file).
- There are no tests or CI currently. If you add tests, use `pytest` and place them in `tests/`.

# Editing guidance for AI agents
- Preserve teacher-facing comments/prompts: do not remove or rewrite exercise descriptions unless correcting typos.
- Avoid changing the sample datasets unless the change is strictly part of a task (e.g., fixing a bug or adding a unit test dataset). If you modify data, update references in the same PR and keep the format consistent.
- When you refactor interactive scripts, keep a minimal wrapper so they remain runnable from the command line while being testable via functions.

# Examples from the repo
- `day_1_activities/student_data.py`: canonical student list (36 records) — look here for keys like `CPSID`, `Combo,Name`, `Email`.
- `day_1_activities/2_main.py`: shows how the dataset gets consumed: indexing, iteration, input-based search and printing.
- `day_3_uber_eats_challenge/orders.py`: starter orders dataset with keys like `order_id`, `customer`, `status`, `items`, `total_price`.

# What to avoid
- Do not add external dependencies unless necessary and approved. This repo is for teaching basic Python.
- Do not remove prompts, doctext, or intentionally broken examples used for exercises.
- Avoid making non-backwards-compatible changes to the public datasets without clear justification.

# When in doubt
- Ask for clarification on the educational intent of a change. If you must convert an interactive exercise into testable code, keep the original behavior accessible (for example, keep a `__main__` block that wires inputs to the tested functions).

# PR checklist for changes
- Keep changes small and focused on a single lesson or bug.
- Add tests for logic changes; keep them in `tests/` and use pytest.
- Update the file comments when you change behavior (teacher prompts should match implementation).

If anything is unclear or you want more examples from this codebase, ask and I'll add clarifying snippets.
