# OpenCode Setup for Data Science & ML Engineering

A production-ready OpenCode configuration optimized for data science and machine learning workflows. Cross-platform compatible (Windows/Linux) with security-first design.

## What's Included

- **`.gitignore`** - Comprehensive exclusions for data science projects (data files, models, credentials, outputs)
- **`AGENTS.md`** - AI agent instructions for data science and ML workflows
- **`opencode.json`** - OpenCode configuration with custom commands and file watching
- **`TASKS.md`** - Project task tracking template (human reference only)

## Quick Start

### 1. Copy Files to Your Project
```bash
# Clone or download this repo
git clone https://github.com/peterho-codes/open-code-setup.git

# Copy relevant files to your project
cp open-code-setup/.gitignore your-project/
cp open-code-setup/AGENTS.md your-project/
cp open-code-setup/opencode.json your-project/
cp open-code-setup/TASKS.md your-project/  # Optional
```

### 2. Customize for Your Needs

Edit files to match your project requirements:
- Update `TASKS.md` with your actual tasks
- Modify `.gitignore` if you have specific file patterns
- Adjust `opencode.json` commands to match your workflow

### 3. Start Using OpenCode
```bash
cd your-project
opencode
```

OpenCode will automatically load your configuration.

## File Descriptions

### `.gitignore`
Prevents accidental commits of:
- Credentials and API keys
- Large data files (CSV, Parquet, etc.)
- Model artifacts (PKL, PT, H5, etc.)
- Build outputs and logs
- Cloud configuration files

### `AGENTS.md`
Instructs the AI agent on:
- Data science best practices
- Code quality standards (type hints, testing, documentation)
- Security and privacy considerations
- ML-specific workflows (experimentation, versioning)
- Python tooling (pytest, ruff, mypy)

### `opencode.json`
Configures:
- File watcher to ignore large/irrelevant files
- Custom commands for common tasks (test, format, lint)
- Code formatters (ruff)
- Permission settings for safety
- Auto-update preferences

### `TASKS.md`
Human-readable task tracking for:
- Project roadmap
- Sprint planning
- Technical debt tracking

**Note:** This file is for human reference only. OpenCode does not read it.

## Features

✅ **Cross-Platform** - Works on Windows and Linux  
✅ **Security-First** - Comprehensive credential and data protection  
✅ **Data Science Optimized** - Tailored for ML/analytics workflows  
✅ **Production-Ready** - Type hints, testing, code quality built-in  
✅ **Flexible** - Easy to customize for your specific needs  

## Custom Commands

Once set up, you can use these commands in OpenCode:

- `/test` - Run pytest with coverage
- `/format` - Format code with ruff
- `/lint` - Check code quality with ruff
- `/typecheck` - Run mypy type checking

## Requirements

- [OpenCode](https://opencode.ai/) installed
- Python environment (optional: `uv` for faster package management)
- Git (for version control)

## Customization Tips

### Adding Custom Commands

Edit `opencode.json` to add your own commands:
```jsonc
{
  "command": {
    "your-command": {
      "template": "Your instruction here",
      "description": "What this command does"
    }
  }
}
```

### Excluding Additional File Patterns

Add patterns to `watcher.ignore` in `opencode.json`:
```jsonc
{
  "watcher": {
    "ignore": [
      // Add your patterns here
      "your-directory/**",
      "*.your-extension"
    ]
  }
}
```

### Modifying AI Behavior

Edit `AGENTS.md` to customize:
- Coding standards
- Testing requirements
- Documentation preferences
- Domain-specific instructions

## Best Practices

1. **Commit these files to Git** - Share configuration with your team
2. **Review `.gitignore` regularly** - Ensure sensitive data isn't committed
3. **Update `TASKS.md`** - Keep your roadmap current
4. **Customize `AGENTS.md`** - Tailor AI behavior to your project needs
5. **Use custom commands** - Streamline repetitive tasks

## Security Notes

- **Never commit credentials** - Use `.env` files (already in `.gitignore`)
- **Review before pushing** - Check `git status` for sensitive files
- **Use environment variables** - For API keys and secrets
- **Keep data local** - Large datasets should never be in Git

## Contributing

Suggestions and improvements welcome! Please open an issue or submit a pull request.

## License

MIT License - Feel free to use and modify for your projects.

## Acknowledgments

Built for use with [OpenCode](https://opencode.ai/), an open-source AI coding agent.

---

**Questions?** Open an issue or check the [OpenCode documentation](https://opencode.ai/docs/).
