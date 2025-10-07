## Hi there 👋

I'm Nikunj Vora, working on ideas at the intersection of AI, consumer tech, and data platforms.

- 🔭 I'm currently working on consumer sentiment tracking and workplace feedback platforms
- 🌱 I'm currently learning how to validate startup ideas faster using The Mom Test and Lean Startup principles
- 💬 Ask me about product strategy, consumer data plays, and early-stage idea validation
- 📫 How to reach me: [your contact - update this]
- ⚡ Fun fact: This repo (nvsudo/nvsudo) is a special GitHub profile repo + my personal prompt library

---

# nvsudo - Personal Prompts & Agent Personalities

A collection of reusable prompts and agent personalities for use across Claude Code, Cursor, and other AI coding assistants.

## Structure

```
prompts/
├── agents/          # AI agent personalities and coaching prompts
├── coding/          # Code-specific prompts and best practices
├── strategy/        # Business and product strategy prompts
└── templates/       # Reusable document templates
```

## Available Agents

### `idea-validator.md`
Expert in validating startup ideas using The Mom Test and Lean Startup principles. Use when:
- Evaluating if an idea is worth building
- Conducting customer discovery
- Deciding whether to pivot or persevere
- Testing assumptions before building

**Core principles:**
- Evidence hierarchy (payment > behavior > opinions)
- Problem validation before solution validation
- The Mom Test customer discovery
- Build-measure-learn discipline
- Knowing when to kill an idea

## How to Use

### In Claude Code
Reference or paste the prompt at the start of your session:
```
Use the idea-validator personality from ~/repos/nvsudo/prompts/agents/idea-validator.md
```

### In Cursor
Add to your `.cursorrules`:
```
@include ~/repos/nvsudo/prompts/agents/idea-validator.md
```

### Manual Copy
```bash
cat ~/repos/nvsudo/prompts/agents/idea-validator.md | pbcopy
```

## Contributing

This is a personal repo, but feel free to fork and adapt for your own use.

---

*Last updated: 2025-10-07*
