# HXOS Activepieces production checklist

- [x] HXOS-specific deployment branch created; upstream-mirror `main` left untouched.
- [x] Draft deployment PR opened.
- [ ] Choose/authenticate managed host.
- [ ] Pin supported Activepieces Community Edition release/image.
- [ ] Provision persistent PostgreSQL.
- [ ] Provision persistent Redis.
- [ ] Configure public HTTPS/frontend URL and webhook URL.
- [ ] Configure encryption/JWT/database secrets in host secret manager.
- [ ] Deploy application.
- [ ] Verify login.
- [ ] Verify scheduled trigger.
- [ ] Verify webhook trigger from public internet.
- [ ] Verify persistence across restart/redeploy.
- [ ] Verify outbound HTTP + Supabase + Gmail connectivity.
- [ ] Record service URL/health in HXOS integration registry.
- [ ] Implement `hxos-app` Activepieces HTTP adapter.
- [ ] Activate Innovation Hub AI Radar flow.
- [ ] Activate House of Our Fathers Research Watch flow.
