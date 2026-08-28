---
name: html-css-javascript-debugging
description: 'Debug plain HTML, CSS, and JavaScript browser issues. Use for broken layouts, DOM events, client-side errors, unexpected state, and static-site regressions.'
argument-hint: '[describe the browser problem]'
---

# HTML, CSS, and JavaScript Debugging

## When to Use
- A static web page has a layout, interaction, or runtime problem.
- A browser console error or failing user action needs diagnosis.
- A recent edit caused a regression in HTML, CSS, or client-side JavaScript.

## Quick Checklist
1. Reproduce the problem using the user's exact action and record the expected versus actual result.
2. Inspect the smallest relevant code path: the DOM element, its styles, its event handler, and any console error.
3. Form one falsifiable hypothesis about the direct cause before editing.
4. Make the smallest change that tests that hypothesis; preserve unrelated user changes.
5. Reproduce the same action and check the console, visible layout, and relevant interaction.
6. Check one nearby edge case, such as an empty value, a second click, a narrow viewport, or a missing element.
7. Summarize the root cause, changed file, verification performed, and any remaining limitation.

## Completion Criteria
- The original reproduction no longer fails.
- No new console errors appear during the tested flow.
- The fix does not rely on timing, accidental selector matches, or a single hard-coded viewport unless intended.
- The changed behavior has a focused regression check or a clear manual verification note.
