# Contributing to UNITIS Documentation Portal

Thank you for contributing to the UNITIS Documentation Portal! This guide will help you understand the workflow for submitting your contributions.

## Branch Protection

The main and documentation branch are protected and only accepts changes through Pull Requests (PRs). Direct pushes to the main and documentation branch are restricted.

## Contribution Workflow

### 1. Create Your Feature Branch

Create a new branch following the naming convention:

```bash
git checkout -b documentation/your-last-name
```

**Example:**
```bash
git checkout -b documentation/dela-cruz
```

### 2. Make Your Changes

Work on your documentation updates in your branch. Ensure all changes follow the existing formatting standards and structure used throughout the repository.

### 3. Commit Your Changes

Make clear, descriptive commits:

```bash
git add .
git commit -m "Add Brief description of your changes"
```

**Commit Message Guidelines:**
- Use clear, concise descriptions
- Start with action verbs (Add, Update, Fix, Remove)
- Example: `Add AI-intuitive Module use case`

### 4. Push Your Branch

Push your branch to the remote repository:

```bash
git push origin documentation/your-last-name
```

### 5. Open a Pull Request

1. Navigate to the repository on GitHub
2. Click on **"Pull requests"** tab
3. Click **"New pull request"**
4. Select your branch (`documentation/your-last-name`) as the source
5. Select `documentation` as the target branch
6. Add a descriptive title and detailed description of your changes
7. Set vitrus-o (23-1-01032@vsu.edu.ph) as reviewer
8. Click **"Create pull request"**

### 6. Wait for Review

Your pull request will be reviewed before being merged into the main branch. You may be asked to make changes or provide clarifications.

## Best Practices

### Documentation Standards

- Follow the existing markdown structure and formatting
- Use consistent heading levels
- Include proper use case scenario tables with all required fields
- Add site map navigation links at the top of each document
- Include the copyright footer at the bottom

### File Organization

```
docs/
├── Usecase/
│   ├── E-ballot/
│   ├── Voter Validation/
│   ├── Election Results/
│   ├── Result Archiving/
│   ├── Real-time Vote Count/
│   └── Candidate Applications/
```

### Use Case Scenario Format

All use case scenarios should follow this structure:

```markdown
| Use Case Name | UC##: Title |
|---------------|-------------|
| **Summary**   | Brief description |
| **Actors**    | Actor names |
| **Preconditions** | Required conditions |
| **Postconditions** | Resulting state |
| **Basic Flow** | **Actor Action** | **System Response** |
|               | 1. Action step | 1.1. Response step |
| **Exceptions** | Exception descriptions |
```

## Getting Help

If you have questions or need assistance:
- Review existing documentation files for formatting examples
- Check the README.md for project overview
- Contact the repository maintainer

---

Thank you for your contributions to the UNITIS Documentation Portal!

<p align="center">© 2026 Viribus</p>
