# Research Workbench

[![pages-build-deployment](https://github.com/praneetpanwar444-gif/research-workbench-demos/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/praneetpanwar444-gif/research-workbench-demos/actions/workflows/pages/pages-build-deployment)

A small, open demonstration portfolio with an interactive field-planning explorer and a research/maths study app. Built with AI assistance. All planning inputs and practice examples are synthetic; no private or employer data is included.

## Live demos

- [Portfolio](https://praneetpanwar444-gif.github.io/research-workbench-demos/)
- [Field Sampling Trade-off Explorer](https://praneetpanwar444-gif.github.io/research-workbench-demos/#planner)
- [Research & Maths Study Lab](https://praneetpanwar444-gif.github.io/research-workbench-demos/#study)

## What it demonstrates

- Responsive HTML/CSS, accessible labels, keyboard-operated controls and live status feedback.
- A transparent budget/capacity simulation with a comparative bar chart and three reproducible calculation checks.
- Eight original flashcards, topic filters, shuffle, multiple-choice feedback and review marks saved on the current device.
- Clear distinction between a working demonstration, proposed scientific work and verified evidence.

## Run and reproduce

Open `index.html` in a modern browser or visit the GitHub Pages site. No build step, package install, server, account or API key is needed. The application makes no external requests and includes no analytics.

Planner assumptions: INR 4,000 fixed travel cost; capacity 12 samples per field day. Affordable = floor(max(0, budget - 4000) / cost); planned = min(affordable, 12 * days); spend = 4000 + planned * cost for budget >= 4000. Travel is incurred even if zero samples are affordable.

| Case | Inputs: budget, cost, days | Planned | Spend | Unused |
| --- | --- | --- | --- | --- |
| Default | 30000, 500, 5 | 52 | 30000 | 0 |
| Low budget | 5000, 2000, 1 | 0 | 4000 | 1000 |
| Capacity limit | 100000, 100, 1 | 12 | 5200 | 94800 |

Use **Run calculation checks** to test all three cases. Also check the presets, reset button, card navigation, topic filters, answer feedback and review persistence after refresh. Review marks are stored only under `rw-reviewed` in localStorage, with an in-memory fallback when storage is unavailable. Reset removes only this app's marks.

## Limits

This planner is not a sample-size, statistical power or representativeness calculation. Site access, safety, lab limits, sampling independence and scientific design need separate review. Costs are illustrative, not quotes. Study review marks are personal progress indicators, not badges, assessments or credentials.

The Notion and Clay project workspaces are separate private drafts; they are not embedded in or exposed by this public site. This repository contains only the demonstration source and documentation.

## Structure

- `index.html`: portfolio, field planner, study app, styles and JavaScript.
- `README.md`: setup, formulas, expected checks and limitations.

Prepared 29 October 2026.

## Browser verification — 29 October 2026

Verified on the published GitHub Pages site: 3/3 calculation checks; low-budget and capacity presets; keyboard slider updates; flashcard reveal and navigation; topic filtering; correct/incorrect feedback; review persistence after reload; and review reset. GitHub Pages build and deployment completed successfully.

## Screenshots

![Portfolio homepage](research-workbench-live.png)

![Study app](research-study-lab-live.png)
