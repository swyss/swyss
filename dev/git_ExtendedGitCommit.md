
# Extended Git Commit Concept

An extended concept for Git messages, incorporating categories beyond the standard "fix" and "feat" to include configurations, code cleaning, and branch switching, can greatly enhance the clarity and traceability of the project's progress. Here's an expanded summary based on the Conventional Commits concept:

## Basic Structure of a Commit Message Format

Each commit message consists of a header, an optional body, and an optional footer. The header has a special format that includes three components:

1. **Type**: This describes the kind of change. The standard types are "fix" (for bug fixes) and "feat" (for new features). Additional types can be added as needed.
2. **Scope**: This is optional and describes the scope of the change (e.g., component or file name).
3. **Description**: A brief description of the change.

Format: `<Type>(<Scope>): <Description>`

## Extended Types for Specific Use Cases

- **config** (Configurations): Changes to configuration files that are not directly related to the code (e.g., `.env` files, build scripts).
- **clean** (Code Cleaning): Code improvements or cleanups that do not directly affect functionality (e.g., removing unused code, refactoring).
- **style** (Style Changes): Changes that affect the style of the code and do not impact functionality or logic (e.g., formatting, adding lint rules).
- **docs** (Documentation): Changes only in documentation (e.g., README, Wiki).
- **test** (Tests): Adding missing tests or correcting existing tests.
- **chore** (Chores): Routine tasks or minor changes that do not fit into the other types.

## Examples of Commit Messages

- `config(ci): update CI configuration to include new linter`
- `clean(core): remove unused functions from utils`
- `style(ui): apply code formatting to CSS files`
- `docs(readme): update installation instructions`
- `test(auth): add unit tests for user authentication`
- `chore(deps): update dependencies to latest versions`

## Branch Switching

For branch switching, there is no direct commit type, as branches are typically managed through the Git branching strategy, not through commit messages. However, if you want to document a branch switch in a commit message, you could use a type like `branch` to describe the context or purpose of the branch switch. This is less common and depends on your specific workflow strategy.

## Conclusion

These extended commit types and formats are intended to improve team communication and ensure a clearer and more traceable project progress. They can and should be adapted based on the specific requirements and preferences of your team.

### Additional Types for Specific Changes
- **refactor** (Refactoring): Significant internal code changes that neither add new features nor fix bugs. This can improve the structure of the code and make it more maintainable.
- **perf** (Performance): Changes that improve the application's performance without altering functionality.
- **build** (Build Process): Changes that affect the build process or external dependencies, as well as changes to tools and libraries used to build the application.
- **ci** (Continuous Integration): Changes to CI configurations and scripts, including setup of build pipelines, test automation, and other process automations.

### Use of Emojis
For visual distinction and to enhance readability, emojis can be prefixed to commit messages. For example:
- 🐛 `fix` for bug fixes
- ✨ `feat` for new features
- 📝 `docs` for documentation changes
- 🧹 `clean` for code cleaning
- 🚀 `perf` for performance improvements

### Semantic Versioning and Release Notes
Link your commit message concept to Semantic Versioning to manage versions based on the types of commits. For example, a `feat` commit might lead to a minor version bump, while a `fix` commit might lead to a patch version bump. Automate the generation of release notes using tools that analyze commit messages.

### Automation and Tools
Use tools like Commitlint to check your commit messages against the set conventions, and Husky to configure and use Git hooks more easily. These tools can help enforce adherence to conventions and improve consistency.

### Training and Documentation
Ensure your team is fully trained and has access to documentation on the commit conventions used. This could include an internal wiki page, a document, or a README in your repository.
