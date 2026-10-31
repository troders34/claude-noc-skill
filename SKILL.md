---
name: noc-monitoring-assessment
description: Generates self-study test questions for the Network Operations Center (NOC) field, focused on network monitoring (SNMP, syslog, flow data, Zabbix, Prometheus, other open-source tools, multi-OS monitoring, and CLI). Supports multiple-choice (single and multiple answer), true-or-false, essay, and lab questions at entry-level to expert difficulty. Use this skill whenever the user asks for practice questions, a quiz, a mock test, exam prep, an assessment, or labs on network monitoring, NOC skills, Zabbix, Prometheus, SNMP, or monitoring on Windows, macOS, Linux, or Unix, even if they do not mention "skill" or "assessment".
---

# NOC Monitoring Assessment Generator

## Workflow
1. Read the request and pick out: number of questions, question types, difficulty, topic, and vendor/tool. For anything missing, use defaults (10 questions, mixed types, mixed difficulty) and state the assumptions in one line. Do not interrogate the user.
2. Read `reference/overview.md` (scope, types, designs), `reference/difficulty.md` (level definitions), `reference/format.md` (required components and one example per type), and `reference/standard.md` (quality rules).
3. Read `reference/resources.md` when the topic involves Zabbix or Prometheus, or to match content to a difficulty level. These outlines guide topic coverage only.
4. Generate the questions. Follow the layout and required components show in the format examples `reference/format.md`. The example topics, difficulty labels, and vendors written there are only illustrations, so vary them to match the request.
5. Before delivering, check every question against `reference/standard.md`: one clear correct answer, realistic distractors, similar option lengths, correct letters spread across A-D, difficulty matches the level, commands and syntax you are sure of.
6. Deliver following `reference/output.md`: English, Markdown by default (PDF only if asked), questions and options first, then the key answers and explanations after the last question. If a PDF file is requested, read the PDF skill before creating the file.

## Rules that must never be skipped
- Never reproduce real certification exam questions.
- Never use "all of the above" or "none of the above".
- State the OS, tool, and version when syntax depends on them.
