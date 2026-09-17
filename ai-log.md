# AI Assistance Log

## CSC 580 – Assignment 1

This file documents my use of AI assistance while personalizing and preparing this portfolio repository.

### AI Tools Used
- GitHub Copilot in Visual Studio Code
- ChatGPT for guidance, troubleshooting, and clarification

### AI-Assisted Work

AI assistance was used to help personalize the existing portfolio template while preserving its original structure and design.

The assistance included:
- Reviewing the existing repository and portfolio template.
- Identifying which sections of the template required personalization.
- Updating portfolio content using information selected for public display.
- Preserving the original HTML, CSS, JavaScript, assets, and overall template design.
- Troubleshooting Git and GitHub workflow steps.
- Creating and working on the `feature/portfolio-personalization` branch.
- Reviewing changes before committing them.
- Restoring the original template structure after an earlier edit changed too much of the page.
- Verifying that the personalized portfolio displayed correctly in the browser.
- Reviewing the Git commit history and repository structure.

### Privacy Decisions

Because this repository is public, personal information that was not necessary for the assignment was intentionally excluded. The portfolio does not publish my phone number, birth date, personal email address, or exact home address.

Only information appropriate for a public academic and professional portfolio was included.

### Human Review

I reviewed the AI-assisted changes and made decisions about what information should be included publicly. AI-generated suggestions were not accepted automatically. Changes were reviewed and adjusted to match the assignment goals, my actual background, and my privacy requirements.

## Full User Prompt

The user provided the following planning prompt (verbatim) for CSC 580 Assignment 1:

"For CSC 580 Assignment 1, I need to document the AI planning process for this portfolio update.

Review the current repository and the content-notes.md file, but do not modify any files.

Project purpose:
Build a public professional portfolio website using the existing HTML/CSS/JavaScript vCard template.

Allowed changes:
Portfolio content, relevant front-end content updates, and small corrections needed to personalize the existing site.

Acceptance goals:
- Display my name and a concise professional role.
- Replace template placeholder information with only approved public information from content-notes.md.
- Preserve the existing portfolio layout and design.
- Keep navigation and the existing site functionality working.
- Keep the site usable on mobile screens.
- Do not expose private information.

Constraints:
- Do not invent education, work history, projects, awards, links, or technical skills.
- Do not add a backend, login system, analytics, or external data collection.
- Preserve the original license and attribution.
- Maintain accessibility, including readable content, keyboard navigation, meaningful link text, and appropriate image alternative text.
- Use only information approved in content-notes.md.

Before making any changes, provide:
1. A file-by-file implementation plan.
2. Assumptions and risks.
3. A proposed testing checklist.
4. Any questions that should be answered before implementation.

DO NOT modify any files. I only need the planning response."

## Assistant Planning Summary (concise)

Below is a concise summary of the planning response provided to the user. This is a factual summary of the plan the assistant produced and the questions it asked; it does not claim that implementation occurred.

- File-by-file plan (high level):
	- `index.html`: Make minimal, targeted content updates only — update the sidebar name/title/avatar alt text, set Location to "Metro Detroit Area", replace contact values with "Not provided", update About text with the professional summary from `content-notes.md`, replace Education timeline entries with the three entries from `content-notes.md`, add UMMA Office Administrator entry and a summarized prior healthcare/dental experience in Experience, replace Skills with grouped lists from `content-notes.md`, and show a neutral Projects message if no projects provided. Preserve all classes, `data-*` attributes, and asset links (`./assets/css/style.css`, `./assets/js/script.js`) so the original vCard styling and JS behavior remain intact.
	- `assets/css/style.css` and `assets/js/script.js`: Do not modify.
	- `content-notes.md`: Use as the single authoritative source for allowed content; do not modify.
	- `ai-log.md`: Create or update to document the AI-assisted planning and actions.

- Assumptions and risks (concise):
	- Assumptions: `content-notes.md` is authoritative for personal content; the template relies on specific classes and `data-*` attributes that must remain unchanged; local static server testing is acceptable.
	- Risks: Structural edits may break CSS/JS hooks; accidental exposure of private info; accessibility regressions; automated formatters or large edits could unintentionally alter selectors relied on by the template.

- Proposed testing checklist (concise):
	- Backup branch before edits.
	- Preview via a local static server (e.g., `python3 -m http.server 8000`).
	- Verify `assets/css/style.css` and `assets/js/script.js` load (Network tab) and no console errors.
	- Verify sidebar (name/title/location, contacts show "Not provided"), About, Education, Experience, Skills, and Projects reflect `content-notes.md` and preserve template styling and interactivity.
	- Keyboard navigation and mobile responsiveness checks.
	- Accessibility spot checks (alt text, headings, link text).

- Questions the assistant asked before implementation (concise):
	- Confirm exact role text to display: recommended "M.S. Artificial Intelligence student — Machine Learning" or an alternative.
	- Confirm replacement text for private fields (plan: "Not provided").
	- Projects: explicit empty-state message vs. keep template project items until real projects are supplied.
	- Testimonials/Clients: remove inner placeholder items, collapse section, or keep as neutral placeholders (recommendation: remove inner placeholders but keep containers to avoid JS errors).
	- Whether to create/update `ai-log.md` now and whether commits should be split by logical units or made in a single commit.

## Human Review

The user reviewed the plan before any implementation. The user requested that the assistant not modify files before approval and specified privacy and content constraints. The human confirmed the planning choices and asked the assistant to prepare `ai-log.md` documenting the planning interaction.

---

End of update to `ai-log.md`.

## Browser-Review Correction (2026-09-17)

During a browser-based review the user identified remaining template placeholder content in the About page's "What i'm doing" service cards and the Testimonials section. Per the user's instruction I made focused corrections using only information from `content-notes.md`:

- Replaced the four service cards with concise, truthful areas derived from `content-notes.md`: "Artificial Intelligence & Machine Learning", "Automation & Process Improvement", "Software & Systems Engineering", and "Operations & Technology". Each card contains brief descriptive text based only on coursework, interests, and administrative/operational experience from `content-notes.md`.
- Removed the entire Testimonials section and its modal because no real testimonials were provided and template testimonials must not be published.

These changes were limited to the About section and the Testimonials block; no other files were modified. All edits preserved existing layout classes, `data-*` attributes, stylesheet and script links, and overall template structure to keep the original design and behavior intact.

Human review: The user requested the correction after reviewing the site in a browser and confirmed the changes should be made. The user retains responsibility for final verification and publication.