# cl-6.startups: learnings

From startups.b (history/) and this session:
- This container has no `ssh-keygen`; `apt-get install -y openssh-client` works. An openssl P-256 key in SEC1 PEM can be converted in place (`ssh-keygen -p -N ''`) and used as the SSH signing key.
- `add_repo` with push was denied once by the permission classifier and allowed after Dinis said proceed; the repo can be cloned read-only meanwhile if public. The tool wants a clone at /home/user/<lowercase name>; a symlink to an existing clone satisfies register_repo_root.
- Summarising fetches give second-hand dates and amounts: re-read at source (raw HTML) before a figure goes on the site; record a refused page (403, 503) as a gap and never work around it.
- Duplicate funding rounds are merged by `scripts/lib/rounds.mjs` and every source stays visible as "Also reported by".
- Leak scan: private-key headers fail everywhere; public keys pass only in `team/keys.json`; SRI pins only in `data/sites/registry.json`.
- No billing on this site (Dinis, 18 Nov): "Free to read".
- The place registry is ontologist's `data/site/places-registry.json`; unknown places go to their country's national place.
