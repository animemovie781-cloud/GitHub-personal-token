# GitHub MCP (Personal Access Token)

Neo Chat includes a personal-use GitHub connector in the MCP market. It uses the official GitHub MCP remote endpoint (`https://api.githubcopilot.com/mcp/`) and accepts a GitHub Personal Access Token (PAT).

## Setup

1. Create a GitHub Personal Access Token from GitHub Settings.
2. Give it only the permissions you want the AI to have. For classic PATs, `repo` and `workflow` are the broad permissions commonly needed for private repositories and Actions. Fine-grained PATs are preferred when you want tighter repository-level control.
3. In Neo Chat, open **Plugin Market → MCP → GitHub MCP**.
4. Paste the PAT into the password field and save it.

The PAT is encrypted with Neo Chat's local WebCrypto/IndexedDB secret store and is resolved only when the MCP request is executed. It is not rendered into the chat prompt.

## Destructive operations

A PAT can grant powerful repository operations. Do not grant permissions you do not need. In particular, repository deletion and other destructive actions should be confirmation-gated in the AI workflow.

## Endpoint

`https://api.githubcopilot.com/mcp/`
