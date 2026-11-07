# Project Structure

<!--
https://uxplanet.org/claude-code-project-structure-for-design-project-00cb36f3cbee
-->

```txt
my-project/
│
├── CLAUDE.md
├── CLAUDE.local.md
├── .mcp.json
│
├── .claude/
│   ├── rules/
│   │   ├── code-style.md
│   │   ├── frontend.md
│   │   ├── backend.md
│   │   ├── testing.md
│   │   ├── security.md
│   │   └── database.md
│   │
│   ├── skills/
│   │   ├── create-component/
│   │   │   └── SKILL.md
│   │   ├── create-api-endpoint/
│   │   │   └── SKILL.md
│   │   ├── database-migration/
│   │   │   └── SKILL.md
│   │   └── ship-feature/
│   │       └── SKILL.md
│   │
│   ├── agents/
│   │   ├── code-reviewer.md
│   │   ├── product-engineer.md
│   │   └── security-reviewer.md
│   │
│   ├── settings.json
│   └── settings.local.json
│
├── docs/
│   ├── product/
│   │   ├── brief.md
│   │   ├── product-requirements.md
│   │   └── terminology.md
│   │
│   ├── engineering/
│   │   ├── architecture.md
│   │   ├── api-reference.md
│   │   └── onboarding.md
│   │
│   ├── decisions/
│   │   ├── README.md
│   │   ├── 0001-auth-provider.md
│   │   ├── 0002-database.md
│   │   └── ...
│   │
│   └── runbooks/
│       ├── deploy.md
│       ├── rollback.md
│       └── incidents.md
│
├── design/
│   ├── DESIGN.md
│   ├── design-tokens.json
│   └── references/
│       ├── screenshots/
│       ├── competitors/
│       ├── moodboards/
│       └── flows/
│
├── research/
│   ├── users/
│   ├── market/
│   └── technical/
│
├── src/
│   ├── components/
│   └── ...
│
└── public/
    └── assets/
```
