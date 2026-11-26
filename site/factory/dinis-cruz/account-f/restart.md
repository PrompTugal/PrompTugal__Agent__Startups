# cl-6.startups: restart

If this session ends, a new one:
1. Clones PrompTugal/PrompTugal__Agent__Startups (this home) and PrompTugal/PrompTugal__News__Startups (attach it with add_repo, push), and reads PrompTugal__News__Website's CLAUDE.md and board/guidance/README.md ("New from Dinis") as public material.
2. Makes a new key (openssl P-256 signing, RSA-4096 encryption; private halves mode 600 outside every repository, never printed), publishes it at `site/keys/cl-6.startups.json` alone in its own commit, and marks the old one superseded. Asks the conductor to add it to the website's `board/keys.json`.
3. Installs `openssh-client` if `ssh-keygen` is missing (the container has none), then sets in each clone: gpg.format ssh, gpg.ssh.program ssh-keygen, user.signingkey (the P-256 key converted to OpenSSH, with its .pub beside it), commit.gpgsign true. Trailers on every commit: `Agent: cl-6.startups@PrompTugal.dinis` and `Claude-Session: <session URL>`.
4. Reads `agent.json`, `now.md`, `learnings.md` here, then `history/PrompTugal__News__Startups/board/team/startups/debriefs/` (newest first) and the work repository's REALITY.md.
5. Dev only, never main.
