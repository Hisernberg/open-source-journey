# SECURITY.md — Token & Account Hygiene

**Rule zero: no secret ever enters this repository, any commit, any log file, or any document.**

---

## Rules

1. **Never commit tokens, keys, cookies or credentials.** Not "temporarily", not "redacted", not in a gist. `.gitignore` blocks `.env*` and `*.token` files — keep it that way.
2. **Paste a token into a terminal only when required**, via environment variables:
   ```bash
   export GH_TOKEN='ghp_...'   # current shell only, never echoed into files
   ```
3. **Use the least-privileged token for the job:**
   - GitHub: prefer a **fine-grained PAT** scoped to only the repos it needs (e.g. Contents: Read & Write on `open-source-journey`), with a **90-day expiry**.
   - Hugging Face: fine-grained token, `read` scope for daily use; `write` only when pushing models/datasets.
   - Kaggle: regenerate the API token whenever it may have leaked; download `kaggle.json` to `~/.kaggle/` with `chmod 600`, never into a repo.
4. **Rotate on any suspicion of exposure** (pasted into chat, committed by accident, shared on a call):
   - GitHub → Settings → Developer settings → Tokens → delete + create
   - Hugging Face → Settings → Access tokens
   - Kaggle → Settings → API → Expire token
5. **If a secret did land in a commit:** rotate the secret first, then rewrite history (`git filter-repo`) — rotation alone is not enough if the repo is public.
6. **Push with a credential helper or `x-access-token:` URL**, never embed tokens in remote URLs stored in `.git/config`.

---

## What this repo contains

- `tracker/` and `logs/` — contribution records only (repo names, PR links, statuses). No personal tokens, no API keys.
- The daily workflow file uses the repository's own `GITHUB_TOKEN` (scoped to `issues: write`) — that is automatic and secret-free.

## Rotation checklist (do today)

- [ ] GitHub PAT replaced with fine-grained PAT (this repo only, 90-day expiry)
- [ ] Old PATs revoked
- [ ] HF token set to fine-grained read (write only when needed)
- [ ] Kaggle token regenerated, `kaggle.json` permission set to 600
- [ ] Two-factor authentication enabled on GitHub / HF / Kaggle accounts
