# Publishing To GitHub

This repository is designed to be published as an open-source Skill project.

## Recommended Repository Settings

- Visibility: Public
- License: MIT
- Repository name: `product-idea-excavator`
- Description: `Bilingual product discovery Skill for turning vague product ideas into high-quality PRDs`
- Topics:
  - `ai`
  - `product-management`
  - `prd`
  - `product-discovery`
  - `startup`
  - `skills`
  - `ai-agents`
  - `bilingual`

## One-Command Publish With GitHub CLI

If GitHub CLI is installed and authenticated:

```powershell
gh repo create product-idea-excavator --public --source=. --remote=origin --push --description "Bilingual product discovery Skill for turning vague product ideas into high-quality PRDs"
```

Then add topics:

```powershell
gh repo edit --add-topic ai --add-topic product-management --add-topic prd --add-topic product-discovery --add-topic startup --add-topic skills --add-topic ai-agents --add-topic bilingual
```

## Manual Publish

1. Create a new public repository on GitHub named `product-idea-excavator`.
2. Copy the repository URL.
3. Run:

```powershell
git remote add origin <repo-url>
git branch -M main
git push -u origin main
```

## Release Checklist

- [ ] README renders correctly
- [ ] License is visible
- [ ] `product-idea-excavator/SKILL.md` is easy to find
- [ ] Install instructions are clear
- [ ] Examples are concrete
- [ ] Safety boundaries are documented
- [ ] Eval prompts are valid JSON
