# Claude Code Guidelines

## Basic Rules

- **Parallel Execution**: Execute independent processes concurrently
- **Agent Priority**: Prioritize using Agents whenever possible for all tasks
- **Planning**: Create execution plans as a general principle

## Language Rules

- **Chat Response**: Always respond in Japanese
- **Markdown Output**: Always output documentation in Japanese
- **Commit Messages**: Follow the language pattern of existing commits in the repository

## Development Rules

- Follow existing code patterns
- Manage sensitive information properly
- Strictly follow Conventional Commits
- Keep output to the absolute minimum required
  - No excessive decoration or unnecessary specifications
- **No Comments**: Never add comments unless explicitly instructed

### Code Analysis and Search

- **serena MCP Priority**: When serena MCP is available, use serena MCP tools for code search and analysis

### File Deletion Rules

- **Already deleted files**: If a file is already deleted from the working directory, commit it as is without attempting to stash
- **When you delete files**: Always follow this two-step process:
  1. First, stash the file: `git stash push -m "message" -- <files>`
  2. Then, remove the file: `git rm <files>`
- **Never use rm or unlink directly**: Always use the git stash → git rm workflow
- **Stash message template**: Use the following template when stashing deletions:

  ```text
  [Claude Code Deletion] <reason>
  Files: <file1>, <file2>, ...
  ```

  - Example: `[Claude Code Deletion] Remove deprecated API endpoints`
  - Example: `[Claude Code Deletion] Clean up unused test fixtures`
