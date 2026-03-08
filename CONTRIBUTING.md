# Contributing to amped-research-kit

## Welcome

Anyone can contribute. New skills, improvements to existing skills, documentation fixes, and examples are all welcome. You do not need to be an expert. If you do research and you built something useful, share it.

## Before You Start

Check the open issues before you begin. If an issue covers what you want to work on, leave a comment to claim it. This keeps two people from building the same thing at the same time. If there is no issue for your idea, open one and describe what you are planning before you write any code.

## What Makes a Good Skill

**A skill is a folder with a SKILL.md file inside.**

The most important part of any skill is the `description` field in the frontmatter. Claude reads this to decide when to use your skill. It must do two things: say what the skill does, and say when to use it. Write it using plain trigger phrases a researcher would actually say, not abstract category labels.

Good description example:
```
description: Use this skill when a researcher needs to plan a usability test, write a usability test plan, or figure out what tasks to give participants in a usability study.
```

Weak description example:
```
description: Usability testing support.
```

Keep the SKILL.md body under 500 lines. If your skill needs long examples, scoring rubrics, or templates, put them in a `references/` subfolder and link to them from the body. The body should explain the workflow, not contain every artifact.

Skills should be specific. A skill that does one thing well is more useful than a skill that tries to cover all research tasks.

## Folder Structure

Each skill lives in its own folder under `skills/`:

```
skills/
your-skill-name/
  SKILL.md
  references/   (optional, for long examples and templates)
  scripts/      (optional, for any supporting scripts)
  assets/       (optional, for images or other files)
```

Name the folder in lowercase with hyphens. Use a name that describes what the skill does, not who made it.

## How to Test Your Skill Before Submitting

Install your skill locally before opening a PR.

Copy your skill folder into your Claude skills directory:
```
cp -r skills/your-skill-name ~/.claude/skills/
```

Then test it:

1. Try at least 3 prompts that should trigger the skill and confirm it activates each time.
2. Try at least 2 prompts that should NOT trigger the skill and confirm it stays quiet.
3. Read the output. Ask yourself whether it would actually be useful to a researcher doing real work.

If the skill activates when it should not, tighten the description. If it fails to activate when it should, broaden the trigger phrases.

## PR Checklist

Copy this into your pull request description and check each item before submitting:

```
- [ ] Description field says what the skill does and when to use it
- [ ] SKILL.md body is under 500 lines
- [ ] Tested with at least 3 prompts that should trigger the skill
- [ ] Tested with at least 2 prompts that should not trigger the skill
- [ ] Skill is not a duplicate of an existing skill
- [ ] Long content (examples, rubrics, templates) moved to references/, not left in SKILL.md body
```

## License

By contributing, you agree that your work will be released under the [MIT License](LICENSE).
