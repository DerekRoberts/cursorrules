# Personal Cursor Rules

Personal Cursor AI assistant rules for managing development across multiple repositories.

## Purpose

These rules configure Cursor's AI assistant behavior to match personal preferences and workflow requirements. They complement shared team standards (like BCGov's copilot-instructions) with personal preferences.

## Installation

### Setup Instructions

1. **Clone this repository:**
    git clone git@github.com:DerekRoberts/cursorrules.git

2. **Clone the shared copilot-instructions repository** (if you haven't already):
    git clone git@github.com:bcgov/copilot-instructions.git

3. **Configure Cursor Settings:**
   - Open Cursor
   - Go to **Settings → Rules → User Rules** (or **Preferences → Rules**)
   - Add both files as references (use absolute paths):
     @/`<1ST_REPO_PATH>`/cursorrules
     @/`<2ND_REPO_PATH>`/.github/copilot-instructions.md

**Why both files?**
- `cursorrules` = Personal preferences (communication style, workflow requirements, etc.)
- `copilot-instructions.md` = Shared team/work standards (common, works with Copilot)
- Together they provide complete context: shared standards + personal preferences

## Structure

- `cursorrules` - Main rules file (personal preferences, workflow requirements)
- References shared standards from `copilot-instructions` repository
- Repository-specific restrictions for work documentation

## Privacy Safeguards

This repository includes automated privacy checks:

- **GitHub Actions workflow** - Validates PRs for private information

**Before committing, review for:**

- [ ] Email addresses (remove or use placeholder)
- [ ] API keys or tokens
- [ ] Personal file paths (use `~/` or `$HOME` instead of `/home/username`)
- [ ] Personal names or identifiers
- [ ] Internal project names or sensitive references
- [ ] Workspace-specific paths that reveal directory structure

**Safe to include:**
- ✅ GitHub usernames
- ✅ General workflow preferences
- ✅ Code style preferences
- ✅ Communication style preferences
- ✅ Repository references (public repos only)

## Customization

Edit `cursorrules` to match your preferences. Key sections:

- **Code Completion Requirements** - Workflow enforcement
- **Communication Style** - How AI should interact
- **Repository-Specific Restrictions** - Context-aware behavior

## Updates

    cd ~/workspace/cursorrules
    git pull

Cursor will automatically reload rules on next conversation.

## Contributing

This is a personal repository. Feel free to fork and adapt for your own use!
