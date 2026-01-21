# Personal Cursor Rules

Personal Cursor AI assistant rules for managing development across multiple repositories.

## Purpose

These rules configure Cursor's AI assistant behavior to match personal preferences and workflow requirements. They complement shared team standards (like BCGov's copilot-instructions) with personal preferences.

## Installation

### Setup Instructions

1. **Clone this repository:**
    git clone https://github.com/YOUR_USERNAME/cursorrules.git ~/Repos/cursorrules

2. **Clone the shared copilot-instructions repository** (if you haven't already):
    git clone https://github.com/bcgov/copilot-instructions.git ~/Repos/copilot-instructions

3. **Configure Cursor Settings:**
   - Open Cursor
   - Go to **Settings → Rules → User Rules** (or **Preferences → Rules**)
   - Add both files as references (use absolute paths):
     @/home/YOUR_USERNAME/Repos/cursorrules/cursorrules
     @/home/YOUR_USERNAME/Repos/copilot-instructions/.github/copilot-instructions.md

**Why both files?**
- `copilot-instructions.md` = Shared team/work standards (BCGov coding standards, git workflows, etc.)
- `cursorrules` = Personal preferences (communication style, workflow requirements, etc.)
- Together they provide complete context: shared standards + personal preferences

## Structure

- `cursorrules` - Main rules file (personal preferences, workflow requirements)
- References shared standards from `copilot-instructions` repository
- Repository-specific restrictions for work documentation

## Privacy Safeguards

This repository includes automated privacy checks:

- **Pre-commit hook** - Blocks commits containing email addresses, absolute user paths, or API keys
- **GitHub Actions workflow** - Validates PRs for private information
- **PRIVACY.md** - Detailed guidelines on what to review

**Before committing, review for:**

- [ ] Email addresses (remove or use placeholder)
- [ ] API keys or tokens
- [ ] Personal file paths (use `~/` or `$HOME` instead of `/home/username`)
- [ ] Internal project names or sensitive references
- [ ] Personal identifiers beyond GitHub username
- [ ] Workspace-specific paths that reveal directory structure

**Safe to include:**
- ✅ GitHub usernames
- ✅ General workflow preferences
- ✅ Code style preferences
- ✅ Communication style preferences
- ✅ Repository references (public repos only)

## Markdown Code Block Formatting

**Use 4-space indentation instead of triple backticks (```) for code blocks.**

Triple backticks can break formatting in some contexts (GitHub releases, documentation systems, etc.). Indented code blocks with 4 spaces are more reliable across different markdown processors.

**Example - Use this:**
    git clone https://github.com/user/repo.git
    cd repo
    git pull

**Instead of this:**
```
git clone https://github.com/user/repo.git
cd repo
git pull
```

This applies to code blocks in documentation, release notes, or any content that might be pasted into systems that don't handle triple backticks well.

## Customization

Edit `cursorrules` to match your preferences. Key sections:

- **Code Completion Requirements** - Workflow enforcement
- **Communication Style** - How AI should interact
- **Repository-Specific Restrictions** - Context-aware behavior

## Updates

    cd ~/Repos/cursorrules
    git pull

Cursor will automatically reload rules on next conversation.

## Contributing

This is a personal repository. Feel free to fork and adapt for your own use!
