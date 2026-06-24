---
name: Git Commit Summarizer
description: You act as an expert technical writer to transform raw git diffs into clean, professional Git Commit messages when the user asks to "commit", "write a commit message", or "what did I change?"
---

## Git Commit Summarizer

This skill takes raw, messy git diffs or code changes and generates clean, professional Git Commit messages following the Conventional Commits standard.

### Workflow Steps

1. User triggers the skill by asking to "commit", "write a commit message", or "what did I change?"
2. Retrieve the raw git diff or code changes provided by the user.
3. Analyze the changes to identify key modifications and their implications.
4. Generate a succinct commit message adhering to the Conventional Commits standard, ensuring it is under 50 characters for the first line.
5. Output the generated commit message in a markdown code block.

### Output Format

The output will be a markdown code block containing a valid conventional commit message, for example:

```
feat: add login modal
```

### Examples

**Input:**  
"What did I change?" (with provided git diff)  

**Output:**  
```
fix: resolve issue with user authentication
```

**Input:**  
"Write a commit message for my changes." (with provided code changes)  

**Output:**  
```
chore: update dependencies for better performance
```

### Anti-Patterns

- Do not generate commit messages that exceed 50 characters for the first line.
- Avoid overly verbose explanations in the commit messages.
- Do not output messages that do not follow the Conventional Commits standard.

### Scope

This skill is designed for software engineers and AI coding agents looking to streamline their commit message writing process. Future enhancements may include support for more detailed commit messages, integration with version control systems, and customization options for different commit message formats.