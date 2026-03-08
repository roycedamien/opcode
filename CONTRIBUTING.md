# Welcome Contributors

We welcome contributions to enhance opcode's capabilities and improve its performance. To report bugs, create a [GitHub issue](https://github.com/getAsterisk/opcode/issues).

> Before contributing, read through the existing issues and pull requests to see if someone else is already working on something similar. That way you can avoid duplicating efforts.

To contribute, please follow these steps:

1. Fork the opcode repository on GitHub.
2. Create a new branch for your feature or bug fix.
3. Make your changes and ensure that the code passes all tests.
4. Submit a pull request describing your changes and their benefits.

## Pull Request Guidelines

When submitting a pull request, please follow these guidelines:

1. **Title**: Please include following prefixes:
   - `Feature:` for new features
   - `Fix:` for bug fixes
   - `Docs:` for documentation changes
   - `Refactor:` for code refactoring
   - `Improve:` for performance improvements
   - `Other:` for other changes

   For example:
   - `Feature: added custom agent timeout configuration`
   - `Fix: resolved session list scrolling issue`

2. **Description**: Provide a clear and detailed description of your changes in the pull request. Explain the problem you are solving, the approach you took, and any potential side effects or limitations of your changes.

3. **Documentation**: Update the relevant documentation to reflect your changes. This includes the README file, code comments, and any other relevant documentation.

4. **Dependencies**: If your changes require new dependencies, ensure that they are properly documented and added to the `package.json` or `Cargo.toml` files.

5. If the pull request does not meet the above guidelines, it may be closed without merging.

**Note**: Please ensure that you have the latest version of the code before creating a pull request. If you have an existing fork, just sync your fork with the latest version of the opcode repository.

## Coding Standards

### Frontend (React/TypeScript)
- Use TypeScript for all new code
- Follow functional components with hooks
- Use Tailwind CSS for styling
- Add JSDoc comments for exported functions and components

### Backend (Rust)
- Follow Rust standard conventions
- Use `cargo fmt` for formatting
- Use `cargo clippy` for linting
- Handle all `Result` types explicitly
- Add comprehensive documentation with `///` comments

### Security Requirements
- Validate all inputs from the frontend
- Use prepared statements for database operations
- Never log sensitive data (tokens, passwords, etc.)
- Use secure defaults for all configurations

## Testing
- Add tests for new functionality
- Ensure all existing tests pass
- Run `cargo test` for Rust code
- Test the application manually before submitting

## Continuous Integration

opcode uses GitHub Actions for automated testing and builds. The following workflows run automatically:

### CI Workflow
Runs on all branches and pull requests:
- TypeScript type checking and build
- Rust formatting check (`cargo fmt -- --check`)
- Rust linting (`cargo clippy`)
- Rust code validation (`cargo check`)

### PR Checks
Runs on pull requests:
- Full type checking with `bun run check`
- Validates TypeScript compilation
- Validates Rust code

### Build Test
Runs on main/develop branches and pull requests:
- Multi-platform build verification (Linux, Windows, macOS)
- Ensures the application builds successfully on all supported platforms

### Before Submitting a PR
1. Ensure your code passes TypeScript type checking: `bun run build` (or `npm run build`)
2. Ensure Rust code is formatted: `cd src-tauri && cargo fmt`
3. Ensure Rust code passes linting: `cd src-tauri && cargo clippy`
4. Verify local build works: `bun run check` (or `npm run check`)

All CI checks must pass before a pull request can be merged.

Please adhere to the coding conventions, maintain clear documentation, and provide thorough testing for your contributions. 
