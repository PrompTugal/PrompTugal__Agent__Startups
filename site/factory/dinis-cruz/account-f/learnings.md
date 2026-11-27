# cl-6.startups: learnings

From startups.b (history/) and this session:
- This container has no `ssh-keygen`; `apt-get install -y openssh-client` works. An openssl P-256 key in SEC1 PEM can be converted in place (`ssh-keygen -p -N ''`) and used as the SSH signing key.
- `add_repo` with push was denied once by the permission classifier and allowed after Dinis said proceed; the repo can be cloned read-only meanwhile if public. The tool wants a clone at /home/user/<lowercase name>; a symlink to an existing clone satisfies register_repo_root.
- Summarising fetches give second-hand dates and amounts: re-read at source (raw HTML) before a figure goes on the site; record a refused page (403, 503) as a gap and never work around it.
- Duplicate funding rounds are merged by `scripts/lib/rounds.mjs` and every source stays visible as "Also reported by".
- Leak scan: private-key headers fail everywhere; public keys pass only in `team/keys.json`; SRI pins only in `data/sites/registry.json`.
- No billing on this site (Dinis, 18 Nov): "Free to read".
- The place registry is ontologist's `data/site/places-registry.json`; unknown places go to their country's national place.
- Read your ABP grant from the raw URL at the start of every wake; it lists allowed hosts (github.com only for now), so every other host read is listed in the run report by your own account. Write the R14 label file as the very first act of a wake.
- A law firm's "06.03.2026" can be read two ways; check the date against two other outlets before changing an entry (Gradient Labs: 1 to 2 June 2026).
- A second search can find a round that is already on the site under another source: grep data/ for the company before adding it, or the merge drops the duplicate and the count does not move.
- data.promptugal.news (index read 27 Nov, v0.1.156): 30 sources, none on startups, funding or open calls, so this section's facts still come from our own research. Possible later feeds: events-pt (startup events by place) and github-pt (code from Portuguese organisations); neither is used, and cl-6.rights must rule their licences first.
- A bot-check stub (about 80 characters, a page that reloads after 5 seconds) can be transient: record it as a gap, do not work around it, and retry once later in the same wake before treating a date as unconfirmed.
