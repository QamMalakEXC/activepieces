# HXOS Activepieces Deployment Activation

Status: activation started 2026-08-17.

This branch exists only for HXOS deployment work. `main` remains the upstream-tracking mirror.

## Target

Deploy Activepieces Community Edition as a separate stateful service with a public HTTPS URL. Do not deploy inside `hxos-app` or Vercel.

## Production requirements

- Pin a supported Activepieces release/image before production cutover.
- Use a production-capable deployment shape with persistent PostgreSQL and Redis, or a managed host/template that provisions equivalent persistent services.
- Configure the public frontend/webhook URL.
- Generate and store strong encryption/JWT/database secrets in the host secret manager; never commit secrets to GitHub.
- Keep Community Edition boundaries; do not use Enterprise-only code/features without licensing.
- Verify login, scheduled trigger, webhook trigger, flow execution, persistence across restart, and outbound HTTP/Gmail/Supabase integration before connecting HXOS.
- Record the external service URL and health receipt back in HXOS after deployment.

## Preferred no-shell path

Use an official managed deployment option such as Activepieces' Railway one-click path when a hosting account is available. This avoids requiring the owner to paste Bash commands and lets the hosting platform provision the runtime from the official image/template.

## HXOS integration after health verification

Only after the Activepieces instance is healthy, implement the existing ADR-0002 HTTP integration boundary from `hxos-app` with:

- connection health
- workflow identifier
- execution request/response
- correlation ID
- idempotency
- callback/receipt logging

The first target workflow is `Excellicomm Innovation Hub AI Radar`, followed by the `House of Our Fathers Research Watch`.
