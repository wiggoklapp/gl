# Commit Message Instructions for GitHub Copilot

This document provides detailed guidance for GitHub Copilot (and contributors) on crafting clear, consistent, and professional commit messages for the `gl` project. Following these conventions ensures a readable commit history, facilitates collaboration, and aligns with industry standards like Conventional Commits.

---

## 1. General Guidelines

1. **Use imperative mood and present tense**  
   - Write as if giving a command: `Add feature` instead of `Added feature` or `Adding feature`.  
   - This makes messages concise and actionable.

2. **Limit the subject line to 50 characters**  
   - The first line is the commit title and should summarize the change briefly.  
   - If needed, add details in the body.

3. **Separate subject from body with a blank line**  
   - Subject: One line summary.  
   - Body: Optional explanation, including why the change was made, how it addresses issues, and any side effects.

4. **Explain the "why" and "what"**  
   - Focus on the purpose and impact, not just the code changes.  
   - Reference issues (e.g., `Fixes #123`) if applicable.

5. **Be specific and avoid vague terms**  
   - Instead of `Update code`, use `Refactor user validation logic`.  
   - Include context like affected components or modules.

---

## 2. Commit Types and Prefixes

Prefix the subject with a type to categorize the change. Use lowercase for consistency.

| Prefix | Description | Example |
|--------|-------------|---------|
| `feat:` | New features or enhancements | `feat: add user profile page` |
| `fix:` | Bug fixes | `fix: resolve null pointer in login` |
| `docs:` | Documentation updates | `docs: update API reference` |
| `style:` | Code style changes (formatting, linting) | `style: format imports alphabetically` |
| `refactor:` | Code restructuring without behavior change | `refactor: extract validation into helper` |
| `test:` | Adding or modifying tests | `test: add unit tests for auth module` |
| `chore:` | Maintenance tasks (build, CI, dependencies) | `chore: update Go version to 1.26.1` |
| `perf:` | Performance improvements | `perf: optimize database query` |
| `ci:` | CI/CD pipeline changes | `ci: add automated testing on PRs` |
| `revert:` | Reverting previous commits | `revert: undo feat: add user profile` |

- **Scope (optional)**: Add in parentheses for specificity, e.g., `feat(auth): implement OAuth login`.  
- **Breaking changes**: Append `!` to the type, e.g., `feat!: change API endpoint`.

---

## 3. Examples

### Good Examples
```
feat: implement dark mode toggle

Adds a toggle button in the header to switch between light and dark themes.
Improves user experience in low-light environments.
```

```
fix: handle edge case in data parsing

Previously, invalid JSON caused a panic. Now, it returns a descriptive error.
Fixes #456.
```

```
refactor(auth): simplify password validation

Extracted regex logic into a separate function for better readability.
No functional changes.
```

### Bad Examples (Avoid)
```
update code ❌ (too vague)
Added new feature ❌ (past tense, no prefix)
fix bug ❌ (lacks detail)
```

---

## 4. Best Practices

- **Review before committing**: Use `git diff --cached` to ensure the message matches changes.
- **Link to issues/PRs**: Include references like `Closes #123` or `Related to #124`.
- **Keep it atomic**: One commit per logical change to make rollbacks easier.
- **Use tools**: Leverage Git hooks or Copilot for auto-generation, then refine manually.
- **Cultural fit**: For this Go project, emphasize clarity for code reviews and maintenance.

By adhering to these guidelines, commit messages become a valuable part of the project's documentation. Happy committing!

---

*Last updated: March 6, 2026*