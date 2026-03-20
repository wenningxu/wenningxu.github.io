# Project Guidelines

## Project Type
- Static GitHub Pages site with no build tooling.
- Main page: index.html.
- Project subpages: mipnerf/, mipnerf360/, zipnerf/ (each has its own css/js/img).

## Code Style
- Preserve existing HTML style: table-based layout and inline styles are intentional.
- Make minimal, localized edits; do not reformat large sections of index.html.
- Keep IDs and JS handler names stable when editing hover effects.

## Architecture
- index.html is the primary content hub (bio, publications, links).
- Shared assets live in images/ and data/.
- Sub-project pages are standalone and should remain self-contained.

## Build and Test
- No install/build/test commands are required.
- Validate changes by opening index.html (and any changed subpage) in a browser.
- Before finishing, verify:
  - hover media swaps still work
  - edited links resolve
  - paths to images/data files are correct

## Conventions
- Publication entries in index.html follow repeated <tr> blocks with:
  - thumbnail/media cell
  - metadata cell (title, authors, venue, links, short summary)
- Keep publication row structure consistent with neighboring entries.
- Put citation files in data/ and ensure href paths match filenames exactly.
- Avoid renaming referenced image/video files unless all matching references are updated.

## Pitfalls
- index.html is large and deeply nested; mismatched tags can break layout globally.
- Inline styles can override stylesheet rules; avoid assuming stylesheet-only changes will apply.
- Relative paths in sub-project pages are sensitive to file moves.
