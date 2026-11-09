
# Contributing to The Cavalier Daily

This guide outlines our development workflow and expectations for submitting issues, making changes, and reviewing code.

These guidelines apply across CavDaily repositories. Refer to each repository's README.md and AGENTS.md for project-specific instructions.

## 1. Getting Started

Before contributing:

1. Ensure you have access to the appropriate repository.
2. Review the repository's README.md for setup instructions.
3. Familiarize yourself with the codebase and project architecture.
4. Review existing issues and pull requests to avoid duplicating work.

## 2. Issues

We use GitHub Issues to track bugs, feature requests, and development tasks.

Choose the appropriate issue template:

- **Bug Report:** Report unexpected behavior, errors, or broken functionality.
- **Feature Request:** Propose new functionality or improvements.
- **Development Task:** Track technical work, including refactoring, testing, documentation, and CI/CD.

### Issue Triage

New issues receive the `needs-triage` label and are reviewed by the product and/or engineering team.

During triage, the team determines:

- Validity and scope
- Priority and effort
- Relevant labels
- Assignee, when appropriate
- Target milestone, if applicable

Once an issue has been reviewed and categorized, the `needs-triage` label is removed.

### Issue Management

- Use descriptive, actionable issue titles.
- Provide sufficient context and clear acceptance criteria.
- Reference related issues when applicable.
- Use milestones for release-specific work.
- Track development progress through the organization's App Development GitHub Project.

## 3. Branching Strategy

Create a new branch for each feature, bug fix, or development task.

Branch from the appropriate integration branch for the work being performed. Confirm the target branch before beginning changes.

### Branch Naming

Use lowercase, hyphen-separated names with a descriptive prefix.

| Prefix | Purpose | Example |
|--------|---------|---------|
| `feat/` | New features | `feat/article-sharing` |
| `fix/` | Bug fixes | `fix/bookmark-sync` |
| `refactor/` | Code restructuring | `refactor/networking-layer` |
| `test/` | Test development | `test/article-loading` |
| `docs/` | Documentation | `docs/setup-guide` |
| `chore/` | Maintenance and configuration | `chore/update-dependencies` |

Keep branches focused on a single issue or related set of changes.

Avoid committing directly to protected branches.

## 4. Commit Messages

We follow the Conventional Commits specification.

### Format

`type: description`

### Common Types

| Type | Purpose |
|------|---------|
| `feat` | New functionality |
| `fix` | Bug fixes |
| `refactor` | Code restructuring without behavior changes |
| `test` | Adding or updating tests |
| `docs` | Documentation changes |
| `chore` | Maintenance and configuration |
| `ci` | CI/CD configuration |
| `build` | Build system or dependency changes |
| `perf` | Performance improvements |

### Examples

- `feat: add article sharing`
- `fix: resolve persistence issue`
- `refactor: separate API client logic`
- `test: add crossword unit tests`
- `docs: update contribution guidelines`
- `ci: add automated build workflow`

Use concise, descriptive messages that explain the change.

## 5. Pull Requests

All code changes should be submitted through pull requests.

### Before Opening a PR

1. Ensure your changes are focused and complete.
2. Review your code for errors or unnecessary changes.
3. Run relevant tests and verify functionality.
4. Update documentation when necessary.
5. Confirm that your branch targets the correct integration branch.

### Creating a PR

Use the shared pull request template and include:

- A summary of the changes
- References to related issues
- Testing and verification details
- Screenshots or recordings for relevant UI changes
- Additional context for reviewers

Use `Closes #123` to link and automatically close a related issue in the same repository when the PR is merged into the default branch. For issues in another repository, use the fully qualified reference.

Open a draft PR if the changes are not yet ready for review.

## 6. Code Review

Pull requests should be reviewed by another developer before merging.

Reviewers should consider:

- Correctness and functionality
- Code readability and maintainability
- Consistency with the existing architecture
- Test coverage and potential regressions
- Security and performance implications

Address review feedback before merging.

All required CI checks and branch protection requirements must pass.

## 7. Testing

Contributors should verify that their changes work as intended.

- Add or update automated tests when appropriate.
- Ensure existing tests continue to pass.
- Test affected functionality manually when necessary.
- Include reproduction and verification steps for bug fixes.
- Avoid introducing regressions.

Refer to the repository's README.md for project-specific testing instructions.

## 8. Project Workflow

Development is tracked through the organization's App Development GitHub Project.

Issues generally progress through the following statuses:

1. **Backlog:** Accepted work awaiting prioritization or planning.
2. **Ready:** Defined and available for development.
3. **In Progress:** Actively being worked on.
4. **In Review:** Awaiting code review or verification.
5. **Done:** Completed and closed.

Keep issue statuses updated as work progresses.

## 9. Security and Sensitive Information

Never commit or share:

- API keys, passwords, or access tokens
- Private credentials or signing keys
- Sensitive user or organizational information
- Environment files containing secrets

Use approved secret-management mechanisms for sensitive configuration.

If you discover a security vulnerability, report it privately to the appropriate repository maintainers rather than creating a public issue containing exploit details or sensitive information.

## 10. Questions and Communication

If you need clarification about an issue, implementation, or development process, communicate with the relevant team members before making significant changes.

Use GitHub Issues and pull request discussions to document technical decisions and keep development context accessible to future contributors.
