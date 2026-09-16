# SNEWSE documentation project

## Purpose and audience

This repository contains the SNEWSE documentation site, built with Mintlify.
Write for humans operating and developing SNEWSE.
The initial audience is administrators and developers, rather than end users.

Keep documentation useful without reproducing every code change or turning it
into an agent workflow log. Instructions here govern documentation work in this
Mintlify repository; do not add personal agent preferences or application policies.

## Use Mintlify

- Read the installed Mintlify skill at `.agents/skills/mintlify/SKILL.md` before
  working on site content, configuration, or components.
- Consult current official Mintlify documentation for product capabilities and
  syntax. Use the Mintlify documentation MCP when available, or official web docs.
- Use native Mintlify navigation, MDX, components, and configuration. Read
  `docs.json` before changing the site structure.
- Use the Mintlify MCP server (`https://mcp.mintlify.com`) for remote editor
  content and settings. Local agents can work on files in this checkout.
  Keep the target branch and editing surface clear when using either workflow.
- Corey reports using the starter free plan. Verify feature availability before
  making the documentation depend on a plan-specific capability.
- Surface platform limitations and infrastructure decisions to Corey. Do not
  build a custom documentation framework or substitute for a Mintlify feature
  without discussing the need and tradeoffs.

## Content boundaries

Use these provisional categories to evaluate content. Final navigation and page
names will be agreed after a bounded inventory of the source documents.

- **Operating guides:** How to set up, run, configure, and troubleshoot SNEWSE.
  Commands need prerequisites, the working directory, and an expected result.
- **Developer guide:** How the system works, including responsibilities, data
  flow, product behavior, and architectural relationships. Explain the system
  at a useful level rather than narrating files and functions line by line.
- **Policies and standards:** Agreed engineering requirements, their rationale,
  and any supported exceptions. Do not turn examples or observed implementation
  choices into policy.
- **Shared reference:** Maintain consistent definitions in a glossary. Use a
  context map to explain relationships; its final location is still undecided.

Give each claim one authoritative home, link to that source wherever the claim is needed, and prefer a code reference over restating details that are readily understood from code.

Give each page a clear purpose for someone using the documentation. Split mixed content by purpose.
Temporary issue plans, handoffs, review logs, and migration tracking are not
product documentation. Do not recreate them as site pages.

## Migration and evidence

- Treat `to-mintlify/` as imported source material, not verified current truth.
  Preserve originals while drafting and reviewing replacements.
- Begin with filenames and headings, then inspect bounded groups of related
  documents. Do not load the entire source collection into one context.
- Propose the information architecture and a representative conversion before
  undertaking bulk migration.
- Verify commands and implementation claims against current application code
  when available. Record evidence and unresolved questions in migration working
  notes; do not present an unchecked old claim as confirmed current behavior.
- Preserve policy meaning and exceptions. Surface conflicts or missing authority
  instead of resolving them through invented requirements.
- Keep migration tracking separate from published prose.
- Track imported source coverage by section in a working ledger. Reconcile each
  section to a verified destination or an explicit disposition before marking
  its source document complete; assignment or drafting alone is not completion.

## Writing and verification

- Do not use "reader" as SNEWSE product terminology: say "user" for a person,
  or name the specific Devour surface or behavior. Flag legacy code names in
  working notes; do not adopt them as documentation terminology or silently
  rename code references.
- Use plain language, active voice, and second person for procedures.
- Write policies and standards as affirmative statements of required tools,
  ownership, and boundaries. Reserve second-person instructions for procedures;
  retain explicit exclusions where they define the scope of a rule.
- Keep sentences concise and headings in sentence case.
- Use bold for UI elements and code formatting for commands, paths, and names
  in code. Preserve project terminology rather than guessing new definitions.
- Lead with the information needed for the page's purpose. Put optional
  implementation detail later.
- Use MDX frontmatter with a title and description, language tags on code blocks,
  descriptive image alt text, and root-relative internal links without extensions.
- Add intended navigation pages to `docs.json`. Use native components where they
  help readers understand or complete a task.
- For site content or configuration changes, run `mint broken-links` and
  `mint validate` from this repository root. Preview affected pages with
  `mint dev` when layout or rendering changes. Report checks actually completed
  and any gaps. Agent-instruction-only edits need a diff review.
