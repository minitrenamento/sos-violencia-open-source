# SOS Violência — Apache-2.0 public source-review release

**English** | [Português](README.pt.md)

Copyright 2026 **LANDI CONSULTORES, SU, LDA**.
First-party contributions are licensed under [Apache License 2.0](LICENSE); see [NOTICE](NOTICE)
and [third-party notices](THIRD_PARTY_NOTICES.md).

**Not published or deployed. Not an emergency service. Do not enter real cases or credentials.**
Prepared to support a UNICEF funding-application review; no UNICEF/government endorsement,
partnership, eligibility, funding or operational response agreement is claimed.

SOS Violência is a Mozambique-focused project for citizen violence alerts/reports and an operator
dashboard, with accessibility features and optional AI-assisted decision support. It is intended
to support women and girls and other people at risk, with human safeguarding responsibilities.

## Distribution
Existing Expo app source: `artifacts/sos-mozambique/`; React dashboard: `artifacts/dashboard/`;
Express API: `artifacts/api-server/`; contracts/shared libraries: `lib/`; historical SQL references:
`migrations/` and `supabase/migrations/`. Technical folder names are retained.

This is a **locked source-review package**, not a working mobile or operator demonstration.
It includes only fictitious fixtures, placeholder assets and non-operational configuration.
All integration and authentication entry points are locked; merely setting environment variables
cannot activate them. No dispatch, GPS collection, account creation, upload, push, AI or USSD
is provided by the review tool. No complete build, deployment or field validation is claimed.

## Quick review (Node.js 22+)
```sh
node tools/verify-release.mjs
node tools/review.mjs
```
No dependency installation, server, credentials or network is needed for these commands.
Never copy the original private repository history. Publish only this directory to a new repository,
as authorized in PUBLICATION_APPROVAL.md. Never publish the original project or its history.

## Status
- **Implemented in historical source:** six SOS modules, reports/media, history/local persistence,
  profiles/contacts, accessibility, notifications, operator management and optional AI triage.
- **Disabled for public release:** all live integrations, authentication, migrations, communication
  actions, app startup/build/code generation. Static review fixtures only.
- **Planned, not implemented:** USSD for basic phones/no-mobile-internet use; needs operator and
  regulatory agreements. No real shortcode or partnership exists in this package.
- **AI:** decision support only, requiring trained human review; no autonomous dispatch or denial
  of help, and no enforced human-approval workflow is claimed as already implemented.

## Documents
[Architecture](docs/ARCHITECTURE.md) · [Features](docs/FEATURES.md) · [Setup](docs/SETUP.md) ·
[Security](SECURITY.md) · [Privacy](PRIVACY.md) · [Safeguarding](SAFEGUARDING.md) ·
[Contributing](CONTRIBUTING.md) · [Roadmap](ROADMAP.md) ·
[Security review](docs/SECURITY_REVIEW.md) · [Resolved decisions](MANUAL_REVIEW.md) · [Publication authorization](PUBLICATION_APPROVAL.md) ·
[Verification](VERIFICATION.md)

## Publication authorization and redistribution scope
The maintainer approves **only this sanitized, non-executable package** for a NEW public
repository with clean history. Nothing has been published here. See PUBLICATION_APPROVAL.md.
Generic template copies without exact provenance and unused tooling were removed; two minimal
original UI surfaces replace required imports. This release is not a buildable clone of the
private application. Remaining dependency vulnerabilities are disclosed, not cleared for use.
Private vulnerability contact: security@landiconsultores.co.mz (dedicated security mailbox).
No dependency implementation or font/icon binaries are bundled; third-party licenses remain theirs.

## Supabase preserved and final dependency remediation
Supabase remains the intended primary backend/data/storage platform; it was not removed or replaced.
See docs/SUPABASE_SECURITY_REVIEW.md for public placeholders, server-only secrets, mandatory
sensitive-table RLS, session/authorization boundaries and private evidence requirements.
The latest review reduced dependency occurrences to 0 critical, 2 high and 2 moderate.
Remaining findings belong to the disabled legacy toolchain, not the audited Supabase SDK closure.
Selected dependency majors were accepted after offline interface checks, not a complete app build.
