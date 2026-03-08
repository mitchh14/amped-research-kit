# GitHub Issues for amped-research-kit

This file contains ready-to-paste GitHub issue drafts for the ARK project.
Copy each issue block into a new GitHub issue. The title, label suggestions,
description, and acceptance criteria are all included.

---

## Issue 1: New skill: research-intake

**Title:** `Add skill: research-intake`

**Labels:** `skill`, `good-first-issue`

---

This skill helps a researcher or research ops person process an incoming research request. When a stakeholder or team submits a research ask, this skill guides Claude to ask the right intake questions and produce a structured summary that makes the request ready to prioritize and scope. Without a structured intake step, teams often start work before goals or decisions are clear. This skill should gather: who is asking and why, what decision the research needs to inform, what is already known, constraints (timeline, budget, available participants), and what "done" looks like for the requester.

**Acceptance criteria:**
- [ ] Skill folder follows the structure in `CONTRIBUTING.md` (`SKILL.md` plus optional `references/`)
- [ ] `description` field states what the skill does and when to use it, with concrete trigger phrases like "I have a research request to process", "a stakeholder just submitted a research ask", or "help me intake this research request"
- [ ] SKILL.md body guides Claude to collect: requester name and team, the decision or question driving the request, what is already known or assumed, timeline and resource constraints, and definition of done
- [ ] Output is a filled-in intake summary a researcher could use to prioritize and scope the work
- [ ] Long intake form templates or example summaries live in `references/`, not in the SKILL.md body
- [ ] SKILL.md body is under 500 lines
- [ ] Tested with at least 3 trigger prompts and at least 2 non-trigger prompts

---

## Issue 2: New skill: interview-guide-builder

**Title:** `Add skill: interview-guide-builder`

**Labels:** `skill`

---

This skill drafts a semi-structured interview guide from a research objective. Researchers regularly need to turn a vague question like "we want to understand how people make buying decisions" into a usable discussion guide with warm-up questions, main topic areas, and probing prompts. The skill should ask the researcher for the research objective, the participant type, and any specific topics or hypotheses to explore, then output a structured guide with an intro script, question sections, and suggested probes. The guide should follow semi-structured format conventions: open questions first, probes to go deeper, and no leading language.

**Acceptance criteria:**
- [ ] Skill folder follows the structure in `CONTRIBUTING.md`
- [ ] `description` field uses concrete trigger phrases like "help me write an interview guide", "I need discussion questions for a research interview", "draft an interview script for me", or "I have a research objective and need interview questions"
- [ ] SKILL.md body collects: research objective, participant type, key topic areas, any hypotheses or things to avoid
- [ ] Output includes an intro script, grouped question sections, and suggested probing prompts for each section
- [ ] Guide uses open, neutral language throughout (no leading questions)
- [ ] SKILL.md body is under 500 lines
- [ ] Long example guides or question banks live in `references/`
- [ ] Tested with at least 3 trigger prompts and at least 2 non-trigger prompts

---

## Issue 3: Improve existing skill: usability-test-plan-builder

**Title:** `Improve skill: usability-test-plan-builder - add lightweight quick-plan mode`

**Labels:** `skill`, `good-first-issue`

---

The existing `usability-test-plan-builder` skill works well as a guided, conversational workflow. This issue asks for a second mode: a quick-plan path where a researcher who already knows their goals and participant criteria can get a plan outline in one pass without going through all six steps interactively. This is useful when someone has already done the planning and just needs a structured document fast. Before starting, review the existing skill at `skills/usability-test-plan-builder/SKILL.md` to understand what is already there and avoid duplicating it. The quick-plan mode should accept goals, participant type, and format (moderated/unmoderated, remote/in-person) in a single prompt and return a condensed plan using the existing template in `references/session-plan-template.md`.

**Acceptance criteria:**
- [ ] Existing SKILL.md is not broken or shortened by this change
- [ ] A "quick-plan" path is documented in the body that activates when a researcher provides goals and criteria up front
- [ ] Quick-plan output uses the same `references/session-plan-template.md` template as the full workflow
- [ ] `description` field is updated if needed to reflect both modes
- [ ] SKILL.md body remains under 500 lines after the change
- [ ] Quick-plan mode tested with at least 3 trigger prompts that include up-front context
- [ ] Full guided mode still tested and passing

---

## Issue 4: New skill: synthesis-assistant

**Title:** `Add skill: synthesis-assistant`

**Labels:** `skill`

---

This skill helps a researcher cluster and theme qualitative data from interview transcripts, usability session notes, or survey open-ends. Synthesis is one of the most time-consuming parts of research and one of the highest-value areas where a structured AI workflow can help. The skill should accept raw notes or quotes, ask the researcher what questions they are trying to answer, and guide a process of grouping observations into themes, labeling them, and flagging outliers or contradictions. The skill should be explicit that Claude is a tool for organizing and surfacing patterns, not for deciding what findings mean. Interpretation and so-what questions belong to the researcher.

**Acceptance criteria:**
- [ ] Skill folder follows the structure in `CONTRIBUTING.md`
- [ ] `description` field uses trigger phrases like "help me synthesize my research notes", "I have interview transcripts and need to find themes", "help me cluster these observations", or "I need to analyze qualitative data"
- [ ] SKILL.md body guides Claude to ask for: the raw data or pasted notes, the research questions being answered, and any existing codes or categories the researcher has started
- [ ] Skill explicitly notes that Claude organizes and surfaces patterns but the researcher owns interpretation
- [ ] Output includes grouped themes, representative quotes per theme, and a section for outliers or contradictions
- [ ] Long coding frameworks or example outputs live in `references/`
- [ ] SKILL.md body is under 500 lines
- [ ] Tested with at least 3 trigger prompts and at least 2 non-trigger prompts

---

## Issue 5: New skill: stakeholder-communication

**Title:** `Add skill: stakeholder-communication`

**Labels:** `skill`

---

This skill drafts a research update or findings summary for a non-researcher audience. Researchers often need to communicate findings to product managers, executives, or other stakeholders who were not in the sessions and do not want to read a full report. The skill should help a researcher turn raw findings into a short, readable update: what was learned, what it means, and what the team should consider doing next. It should ask for the audience, the key findings, and the decision or action the findings are meant to inform. Output should be concise and free of research jargon.

**Acceptance criteria:**
- [ ] Skill folder follows the structure in `CONTRIBUTING.md`
- [ ] `description` field uses trigger phrases like "help me write a research update for stakeholders", "I need to communicate findings to my product team", "draft a summary of what we learned", or "write up research results for a non-researcher audience"
- [ ] SKILL.md body collects: intended audience, key findings (researcher provides these), the decision or action the findings inform, and any constraints (length, format, tone)
- [ ] Output is structured as: context one sentence, findings in plain language, so-what or implications, suggested next steps
- [ ] No research jargon in the output template
- [ ] SKILL.md body is under 500 lines
- [ ] Tested with at least 3 trigger prompts and at least 2 non-trigger prompts

---

## Issue 6: New skill: method-selector

**Title:** `Add skill: method-selector`

**Labels:** `skill`

---

This skill recommends a research method given a business question and constraints. Choosing the right method is one of the highest-judgment decisions in research, and researchers regularly get requests that do not come with a method attached. This skill should ask for the business question, what decision the research will inform, the stage of the product or initiative, timeline, and rough budget or team capacity. It should then recommend one or two methods, explain why they fit, and name the trade-offs. The skill should not be a generic methods glossary. It should produce a specific recommendation for a specific situation.

**Acceptance criteria:**
- [ ] Skill folder follows the structure in `CONTRIBUTING.md`
- [ ] `description` field uses trigger phrases like "help me pick a research method", "what kind of research should I do for this", "I have a business question and need to know what method to use", or "should I do interviews or a survey for this"
- [ ] SKILL.md body collects: the business question or decision to inform, the product stage, timeline, team capacity or budget constraints, and any methods already ruled out
- [ ] Output recommends one or two methods with a plain-language rationale and named trade-offs for each
- [ ] Output does not list all possible methods; it recommends and explains
- [ ] A reference file in `references/` may contain a method comparison table if needed, not inline in SKILL.md
- [ ] SKILL.md body is under 500 lines
- [ ] Tested with at least 3 trigger prompts and at least 2 non-trigger prompts

---

## Issue 7: Docs improvement: add inclusive research defaults to CONTRIBUTING.md

**Title:** `Docs: add inclusive research defaults section to CONTRIBUTING.md`

**Labels:** `docs`, `good-first-issue`

---

`CONTRIBUTING.md` currently covers skill structure and testing but does not say anything about inclusive research practices. Skills submitted to this repo will be used by researchers working with real participants, including people with disabilities, people from marginalized communities, and people with varying technical access. This issue asks for a short section in `CONTRIBUTING.md` that gives contributors a baseline for building inclusive defaults into their skills. The section should draw on patterns from the `awesome-inclusive-user-research` collection and similar resources. It should be practical and direct, not a manifesto. Suggested guidance: write participant criteria that do not accidentally exclude, avoid assuming access to specific devices or connectivity, and include accessibility notes where sessions involve assistive technology.

**Acceptance criteria:**
- [ ] A new "Inclusive Research Defaults" section is added to `CONTRIBUTING.md`
- [ ] Section covers at least: writing participant criteria inclusively, not assuming device or connectivity access, and a note about accessibility in session design
- [ ] Section is under 200 words
- [ ] Language is plain and direct, consistent with the rest of `CONTRIBUTING.md`
- [ ] No em dashes or fancy punctuation
- [ ] PR includes a brief note on what sources or references informed the guidance

---

## Issue 8: Add research-prioritization scoring rubric to docs/

**Title:** `Add research prioritization scoring rubric to docs/`

**Labels:** `research-ops`, `docs`

---

Research teams regularly need to prioritize which studies to run and in what order. There is no shared rubric in this repo for scoring or comparing research requests. This issue asks for a scoring rubric that teams can adapt and that a future `research-intake` or `method-selector` skill can reference. The rubric should score requests across dimensions like: strategic alignment, urgency, confidence in existing knowledge, effort required, and availability of participants. It should produce a total score and a short recommendation (pursue now, defer, or suggest alternative). The rubric should live in `docs/` so any skill can link to it.

**Acceptance criteria:**
- [ ] A file is created at `docs/research-prioritization-rubric.md`
- [ ] Rubric covers at least five scoring dimensions with plain descriptions of what a low, medium, and high score looks like for each
- [ ] Each dimension is scored on a consistent scale (for example 1 to 3 or 1 to 5)
- [ ] Rubric includes a total score interpretation guide (what different ranges mean in practice)
- [ ] Rubric is designed to be filled in by a human or used as a reference by a Claude skill
- [ ] File is under 150 lines
- [ ] Language is plain and direct with no jargon that would confuse a new researcher

---

## Issue 9: Maintain the skills index table in README

**Title:** `Docs: keep the skills table in README.md up to date`

**Labels:** `docs`, `good-first-issue`

---

`README.md` currently has a skills table with one row for `usability-test-plan-builder`. As new skills are added, this table needs to stay current. This is a recurring maintenance task, not a one-time fix. This issue tracks the work of keeping that table accurate and asks for a lightweight process for doing so. The contributor should update the table to reflect any skills merged since the last update, confirm the status column is accurate (available, in-progress, planned), and optionally add a note in `CONTRIBUTING.md` asking skill contributors to include a README table update in their PR. A fully automated solution is out of scope for this issue.

**Acceptance criteria:**
- [ ] Skills table in `README.md` reflects all skills currently in the `skills/` folder
- [ ] Each row has: skill name, one-sentence description of what it does, and a status
- [ ] Status values are consistent (use: available, in-progress, or planned)
- [ ] `CONTRIBUTING.md` includes a checklist item reminding contributors to update the README table when adding a new skill
- [ ] No new files created; changes are to `README.md` and `CONTRIBUTING.md` only

---

## Issue 10: New skill: screener-builder

**Title:** `Add skill: screener-builder`

**Labels:** `skill`, `good-first-issue`

---

Participant screeners are one of the most commonly needed research documents and one of the easiest to get wrong. A bad screener recruits the wrong people or tips off participants on what answers will get them selected. This skill should help a researcher write a screener questionnaire by asking for the participant criteria from the research plan, the study type (moderated interview, usability test, survey, diary study), and any hard exclusion criteria. It should output a screener with qualifying and disqualifying logic written in plain language, suitable for use in a recruiting platform or sent to a recruiter.

**Acceptance criteria:**
- [ ] Skill folder follows the structure in `CONTRIBUTING.md`
- [ ] `description` field uses trigger phrases like "help me write a screener", "I need to recruit participants and need screening questions", "draft a participant screener for my study", or "help me figure out who to recruit"
- [ ] SKILL.md body collects: target participant criteria, study type, session format, hard exclusions, and number of participants needed
- [ ] Output includes qualifying questions with pass/fail logic and is free of leading language that tips off respondents
- [ ] SKILL.md body is under 500 lines
- [ ] A screener template lives in `references/` if one is included
- [ ] Tested with at least 3 trigger prompts and at least 2 non-trigger prompts

---

## Issue 11: New skill: survey-design-assistant

**Title:** `Add skill: survey-design-assistant`

**Labels:** `skill`

---

Survey design is its own craft. Poorly written survey questions introduce bias, confuse respondents, or produce data that cannot be acted on. This skill should help a researcher design a survey instrument by asking for the research objective, what decisions the data will inform, and the target respondents. It should guide the researcher through question type selection (rating scale, multiple choice, open-end), flag common problems like double-barreled questions or leading language, and produce a draft survey with a logical flow. It should also prompt the researcher to estimate completion time, since surveys that take too long hurt response rates.

**Acceptance criteria:**
- [ ] Skill folder follows the structure in `CONTRIBUTING.md`
- [ ] `description` field uses trigger phrases like "help me design a survey", "I need to write survey questions", "draft a survey for my research", or "I want to run a survey and need help with the questions"
- [ ] SKILL.md body collects: research objective, decisions the data will inform, respondent type, and any questions or topics the researcher already has
- [ ] Skill flags at least these common survey problems: leading questions, double-barreled questions, and scales without labeled anchors
- [ ] Output includes a draft survey with question type noted for each item and an estimated completion time
- [ ] SKILL.md body is under 500 lines
- [ ] Tested with at least 3 trigger prompts and at least 2 non-trigger prompts

---

## Issue 12: Add docs/skill-testing-guide.md

**Title:** `Docs: add a skill testing guide for contributors`

**Labels:** `docs`

---

`CONTRIBUTING.md` tells contributors to test their skill with 3 trigger prompts and 2 non-trigger prompts before submitting a PR, but it does not explain how to think about trigger design, what good test coverage looks like, or how to diagnose a skill that is not triggering correctly. This issue asks for a short guide at `docs/skill-testing-guide.md` that gives contributors a practical framework for testing. It should cover: how Claude uses the description field to select skills, what under-triggering and over-triggering look like and how to fix them, how to pick diverse trigger prompts (different phrasings, levels of specificity, beginner vs experienced researcher language), and a simple log format for recording test results.

**Acceptance criteria:**
- [ ] File created at `docs/skill-testing-guide.md`
- [ ] Guide explains how Claude's description-based selection works in plain terms (no internal implementation details, just the mental model)
- [ ] Guide covers under-triggering and over-triggering with at least one example of each and a fix
- [ ] Guide includes a template for logging trigger test results (prompt used, did it trigger, notes)
- [ ] Guide links back to `CONTRIBUTING.md`
- [ ] File is under 200 lines
- [ ] Language is plain and consistent with the rest of the repo
