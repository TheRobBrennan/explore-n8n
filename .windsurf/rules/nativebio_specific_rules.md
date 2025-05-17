# NativeBio Project Rules

These rules are specific to NativeBio projects but can be adapted for other repositories as needed.

<drupal_development>
- Follow Drupal coding standards and best practices
- Test all changes in the local Docker environment before deployment
- Use the provided npm scripts for common tasks (e.g., `npm run docker:up`, `npm run verify:all`)
- Document Drupal-specific configurations and modules
</drupal_development>

<deployment_process>
- Use the deployment scripts in the repository for consistent deployments
- Follow the semantic versioning pattern for version bumps
- Test deployments using the dry-run option first: `npm run deploy:check`
- Document any deployment issues or workarounds
</deployment_process>

<task_management>
- Document tasks in appropriate Markdown files under the `docs` directory
- Use the Asana import script for converting tasks to Asana when needed
- Follow the established task status legend for consistency
- Link tasks to relevant code or documentation when applicable
</task_management>

<semantic_versioning>
- Follow semantic versioning for all changes
- Use appropriate prefixes in PR titles and commit messages:
  - `feat:` for new features (minor version bump)
  - `feat!:` for breaking changes (major version bump)
  - `fix:` for bug fixes (patch version bump)
  - Other prefixes: `docs:`, `style:`, `refactor:`, `perf:`, `test:`, `build:`, `ci:`, `chore:`, `revert:`
- Ensure PR titles match the semantic versioning pattern required by CI checks
</semantic_versioning>
