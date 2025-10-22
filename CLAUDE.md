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

- **Use git stash instead of rm**: Never use `rm`, `unlink`, or `git rm` commands directly
- **Stash with descriptive message**: Always use `git stash push -m "message" -- <files>` with a descriptive message
- **Mandatory title template**: Use the following template for stash messages:

  ```text
  [Claude Code Deletion] <reason>
  Files: <file1>, <file2>, ...
  ```

  - Example: `[Claude Code Deletion] Remove deprecated API endpoints`
  - Example: `[Claude Code Deletion] Clean up unused test fixtures`
