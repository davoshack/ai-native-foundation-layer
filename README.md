# AI Native Foundation Layer

The reusable **AI Layer** for agentic engineering - the skills, agents, and reference
docs you install **once** into any codebase.

## Install

```bash
# 1. Clone
git clone git@github.com:davoshack/ai-native-foundation-layer.git

# 2. Copy the AI Layer into your project (skills/agents/references + the Atlassian .mcp.json)
cp -r ai-native-foundation-layer/.claude <your-repo>/.claude
cp ai-native-foundation-layer/.mcp.json <your-repo>/.mcp.json

# 2a. Optional: turn on the two baseline hooks (env-file / rm -rf guardrail + an
#     audit-log trail). Commit the resulting settings.json so your whole team
#     inherits the guarantee.
cp ai-native-foundation-layer/.claude/settings.json.example <your-repo>/.claude/settings.json

# 2b. Optional: the PR review workflow (needs a CLAUDE_CODE_OAUTH_TOKEN repo secret)
cp -r ai-native-foundation-layer/.github <your-repo>/.github

# 3. In your repo, derive your rules from your real code:
#    run  /create-rules   → writes CLAUDE.md + .claude/context/ (cited to your code)
# 4. Wire external context: the pack ships a .mcp.json for the Atlassian MCP (Jira +
#    Confluence) - edit/replace it for your stack - then
#    run  /prime <jira-keys> <confluence-page-ids>
```