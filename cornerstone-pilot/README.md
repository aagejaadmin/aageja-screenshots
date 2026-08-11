# CSX Cohort 1 — Screenshot Capture Package

Captured **2026-08-11** from the `unicorn1.csod.com` sandbox as **Administrator (Sundar)**.
Scope agreed for this run: **Priority 1 (Gap 3 + Gap 5) + Priority 2 (Lesson 2 lab imagery)**.

## Image spec
- **Canonical size:** 1920×1080 PNG (16:9) — the eLearning-video standard (Storyline / Rise / Captivate / Camtasia). Fills the player with no letterboxing.
- **Masters:** the full-resolution source frame for every screen is kept in each screen's `raw/` folder (never resize from the canonical — go back to the master).
- **Close-ups:** `_el-<control>` crops of the key diagnostic control accompany most screens.
- **Styling:** off (unstyled base images, ready to frame/annotate in your authoring tool).
- **Metadata:** each PNG carries embedded chunks (Title, Alt, Screen, Source, Captured, Elements); a machine index is in `screenshots-index.json` and a human table in `screenshots-manifest.md`.

## Folder layout
```
csx/<module>/<screen>/
  csx_<module>_<screen>.png            # 1920×1080 canonical
  csx_<module>_<screen>_el-<ctrl>.png  # close-up(s)
  raw/csx_<module>_<screen>.png        # full-res master
```

## Coverage — how each capture maps to the brief

### Priority 1 · Gap 3 — Cohort 1 failure indicators
| Brief item | Capture(s) | Notes |
|---|---|---|
| Notification exists but won't fire | `email-mgmt/action-expanded-email`, `email-mgmt/email-editor` (unchecked **Active** toggle) | Naturally occurring: an email configured under the *Employee Onboarding Started* trigger but set **inactive**. CSX-accurate equivalent of "template with no working trigger." |
| Trigger with no notification configured | `email-mgmt/triggers-no-email` | List contrast: triggers with a configured email (expandable) vs. triggers with none (Instructor Anonymization, Integration Task Assigned/Completed). |
| Empty / missing group membership | `groups/membership-options` ("No members added"), `groups/manage-members-dynamic` ("No criteria added"), `groups/manage-members-manual` | The empty-membership surfaces a partner sees in Groups Management. |
| Broken deeplink landing state | `learner/deeplink-restricted` | Invalid learner deeplink → "Restricted Area – you do not have the permissions needed." (permission-error variant). |

### Priority 1 · Gap 5 — availability restrictions
| Brief item | Capture(s) |
|---|---|
| Availability/restriction panel, step by step | `content-mgr/availability-panel` (criteria row + options), `content-mgr/availability-criteria-types` (Select Criteria dropdown: All Users / Division / Position / Grade / Cost Center …) |

### Priority 2 · Lesson 2 lab imagery
| PKB step | Capture(s) |
|---|---|
| Groups recreation | `groups/manage-groups-landing`, `groups/create-group-form`, `groups/membership-options`, `groups/manage-members-dynamic`, `groups/manage-members-manual`, `groups/upload-publish-prompt` |
| Security roles (System Settings → Security Roles) | `security-roles/security-roles-landing`, `security-roles/manage-categories`, `security-roles/create-category`, `security-roles/create-role-general`, `security-roles/permission-assignment` |
| Notifications | `email-mgmt/email-admin-list`, `email-mgmt/email-editor`, `email-mgmt/email-editor-body` (trigger binding shown in the editor's **Action** field) |
| UAT unified admin console | `admin-console/system-settings-landing`, `learner/galaxy-home` (the "new Galaxy home page" the smoke test checks) |

## Two Gap 3 items not fully staged (and why)
1. **A published dynamic group that "should have members but shows zero."** The modern Manage Groups SPA in this sandbox was intermittently unresponsive to View/Edit/Create drill-in clicks, so a clean published-group-with-0-members view couldn't be reliably produced. The *empty-membership* surfaces are captured via the create-group flow (`groups/membership-options`, `manage-members-*`), which show the same zero-member visual. Recommend staging a labelled dynamic group with impossible criteria and re-capturing its View → Membership once the SPA is stable.
2. **Content assignment showing "no eligible learners" because the group is empty.** Producing this authentically requires pointing a training item's Availability at an empty group. I deliberately did **not** modify a real course's availability (risk of leaving a live course unavailable if a revert were missed). Recommend a dedicated throwaway staging course + empty group, then capture the roster/proxy-enrollment preview showing 0 eligible.

Also: the classic Email Management **send history is export-only** (a downloadable CSV per trigger), not an on-screen "zero/failed sends" view. I did not trigger the download. The practical "won't fire" diagnostics are covered by the inactive-email and no-email-trigger captures above.

## Sandbox changes
**None persisted.** No group, security role, category, or email was saved/published; every creation/edit flow was opened for capture and then cancelled or navigated away from.

## Quality notes
- **Native capture ceiling ≈ 1412–1568 px** in this environment, so 1080p frames are mildly upscaled (text softens slightly; H.264 compression hides most of it in video). For maximum crispness on a specific screen I can re-export at 1280×720 (downscaled = pixel-sharp).
- **Authentic whitespace:** several admin screens (the classic Security Role pages and the Availability panel) are wide-and-short layouts with real empty space below their controls. That whitespace is the actual page, not a crop artifact — the automated "dead-space" heuristic flags it, but the screens are intentionally kept authentic. All frames are exactly 1920×1080.
