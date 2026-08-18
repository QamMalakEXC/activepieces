# One unavoidable human gate

HXOS can prepare repository, deployment metadata, integration state, and test criteria without shell access. Creating the external runtime itself requires authorization to a hosting provider account.

At activation time no Railway/Render/Fly.io/DigitalOcean hosting connector or credential is available to ChatGPT/HXOS. Therefore deployment cannot truthfully be marked complete until the owner authorizes a supported host and it returns a service URL.

Preferred no-shell handoff: authenticate to Railway and use Activepieces' official one-click deployment path. After that host authorization exists, continue configuration through the provider UI/API rather than asking the owner to paste Bash commands.
