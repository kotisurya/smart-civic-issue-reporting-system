# NagaraSetu UX contract

## Roles and boundaries

- Residents create accounts with `CIT` IDs, report issues, track their own reports, add information, and confirm resolution.
- Municipal officers use `OFF` IDs and see only reports routed to their approved civic service team.
- City administrators approve officers, assign teams, inspect all issues, and manage credentials.
- Server authorization is canonical; hiding a control never grants or removes access.

## Canonical UI map

| Capability | Canonical owner | Source of truth | Allowed variants | Verification |
|---|---|---|---|---|
| Form | Shared `.field` markup and submit handlers | This contract | Resident / officer / administrator | Browser flow and static audit |
| Select/Listbox | Native `select` | `premium-ui.json` | Native only | Keyboard and browser popup |
| Toast | `#toast` and `showToast` | This contract | Success / info / error | Live-region browser check |
| Dialog | `#modalBackdrop`, `openModal`, `closeModal` | This contract | Detail / edit / destructive confirmation | Focus and Escape browser check |
| Scrollbar | Global rules in `public/styles.css` | `DESIGN.md` | Shared baseline | Computed browser rendering |
| CRUD | Express routes plus shared API wrapper | Server routes | Resident / team / city administration | Database tests and browser flow |

## Workflow behavior

- Create: “Submit civic report” waits for server confirmation, closes the modal, adds the report to the owning list, and announces its `CIV` reference.
- Edit/update: “Save changes” remains in context and refreshes the canonical item.
- Delete: uses the app-owned confirmation modal and refreshes the current list after server confirmation.
- Search: client-side lists filter immediately; the administrator credential lookup runs only on explicit form submission.
- Errors preserve entered non-secret values and appear through the shared toast or scoped panel.

## State and accessibility

All primary actions require default, hover, focus, pressed, disabled/busy, success, and error treatment. Lists provide empty and no-results guidance. Keyboard focus is visible. Status always includes text. Motion is disabled under `prefers-reduced-motion`. Target is WCAG 2.2 AA.

## Content vocabulary

Use “report” or “civic issue” for resident-facing records, “service team” for municipal routing, “Citizen ID” for `CIT` identifiers, and “Officer ID” for `OFF` identifiers. The legacy database area column is internal-only and is not part of resident registration or profile settings.
