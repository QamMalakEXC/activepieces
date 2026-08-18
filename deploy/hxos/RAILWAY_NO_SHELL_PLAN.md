# Railway no-shell deployment plan

Railway is the preferred first managed-host candidate because Activepieces publishes an official Railway deployment path and Railway can provision a public service without requiring the owner to paste shell commands.

Human account authorization is still required before infrastructure can be created. HXOS/ChatGPT currently has no connected Railway control surface, so the handoff point is host authentication/authorization—not application architecture.

After the host exists, configure only through the provider UI/API/secret manager. Do not commit `.env` or tokens.

Production acceptance requires persistent PostgreSQL + Redis or the production-equivalent resources created by the official template, a public HTTPS URL, and successful webhook/scheduled-flow tests.
