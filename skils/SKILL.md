---
name: Git Commit Summarizer
description: You take raw, messy git diffs or code changes and write clean, professional Git Commit messages following the Conventional Commits standard when the user asks to "commit", "write a commit message", or asks "what did I change?"
---

## Git Commit Summarizer

The Git Commit Summarizer skill transforms raw git diffs or code changes into concise, professional commit messages that adhere to the Conventional Commits standard. This ensures that your commit history is clear and informative.

### Workflow Steps

1. User initiates the skill by asking to "commit", "write a commit message", or "what did I change?"
2. The skill retrieves the raw git diff or code changes provided by the user.
3. The skill analyzes the changes to determine the essence of the modifications.
4. A commit message is generated following the Conventional Commits format, ensuring it is under 50 characters for the first line.
5. The skill presents the generated commit message to the user.

### Output Format

A markdown code block containing a valid conventional commit message. For example:

```
feat: add login modal
```

### Examples

**Input:**  
User: "What did I change?"  
Diff: `...` (raw git diff provided)

**Output:**  
```
fix: resolve header overflow issue
```

---

**Input:**  
User: "Write a commit message."  
Diff: `...` (raw git diff provided)

**Output:**  
```
chore: update dependencies
```

### Anti-Patterns

- The skill should NOT generate commit messages that exceed 50 characters in the first line.
- The skill should NOT provide explanations or context beyond the commit message.
- The skill should NOT create vague or unclear commit messages.

### Scope

The primary target audience for this skill is software engineers and AI coding agents who seek to maintain a clean and organized commit history. Future enhancements may include support for different commit message formats and integration with version control systems for automatic message generation based on user actions.