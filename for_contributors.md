Made with love❤️

# Contributing to Gemini CLI

First off, thank you for considering contributing to the Gemini CLI! It's people like you that make the open-source community such a great place. We welcome any and all contributions, from bug reports to feature requests and code contributions.

This document will guide you through the process of contributing to the project.

## Getting Started

Before you begin, please make sure you have the following prerequisites installed:

*   [Node.js version 20](https://nodejs.org/en/download) or higher
*   [npm](https://www.npmjs.com/get-npm)

To get the project up and running on your local machine, follow these steps:

1.  **Fork the repository** on GitHub.
2.  **Clone your fork** to your local machine:
    ```bash
    git clone https://github.com/YOUR_USERNAME/gemini-cli.git
    ```
3.  **Navigate to the project directory:**
    ```bash
    cd gemini-cli
    ```
4.  **Install the dependencies:**
    ```bash
    npm install
    ```

Now you're all set to start contributing!

## Project Structure

The Gemini CLI is a monorepo managed with npm workspaces. The main packages are located in the `packages/` directory:

*   `packages/cli`: This is the user-facing part of the Gemini CLI. It handles user input, renders the output, and manages the overall user experience.
*   `packages/core`: This is the backend of the Gemini CLI. It interacts with the Gemini API, manages tools, and orchestrates the overall workflow.

Here's a brief overview of the other important directories:

*   `.gcp/`: Contains Docker and release configurations for Google Cloud Platform.
*   `.github/`: Contains GitHub-specific files, such as issue templates, workflows, and CODEOWNERS.
*   `docs/`: Contains all the documentation for the project.
*   `eslint-rules/`: Contains custom ESLint rules for the project.
*   `integration-tests/`: Contains integration tests for the CLI.
*   `scripts/`: Contains various scripts for building, testing, and releasing the project.

## Development Workflow

### Building and Running

To build the project, you can use the following command:

```bash
npm run build
```

Before submitting any changes, it's crucial to run the full preflight check. This command will build the repository, run all tests, check for type errors, and lint the code:

```bash
npm run preflight
```

### Testing

This project uses [Vitest](https://vitest.dev/) for testing. Test files are co-located with the source files they test (e.g., `src/gemini.test.tsx` for `src/gemini.tsx`).

To run the tests, use the following command:

```bash
npm test
```

When adding new features, please make sure to add corresponding tests.

### Coding Style

We follow the coding style guidelines outlined in the `GEMINI.md` file. Here are some key points:

*   **Prefer plain JavaScript objects over classes.**
*   **Use ES module syntax for encapsulation.**
*   **Avoid `any` types and type assertions.**
*   **Embrace JavaScript's array operators.**

Please refer to the `GEMINI.md` file for more details.

## How to Contribute

### Finding Something to Work On

If you're looking for a place to start, check out the open issues on GitHub. You can filter by labels like `good first issue` or `help wanted`.

### Submitting a Pull Request

1.  **Create a new branch** for your changes:
    ```bash
    git checkout -b my-awesome-feature
    ```
2.  **Make your changes** and commit them with a clear and concise commit message.
3.  **Push your changes** to your fork:
    ```bash
    git push origin my-awesome-feature
    ```
4.  **Open a pull request** on the Gemini CLI repository.

Please make sure your pull request includes the following:

*   A clear and descriptive title and description.
*   A reference to the issue you're addressing (if any).
*   Tests for your changes.
*   A confirmation that you've run `npm run preflight` and all checks have passed.

## Architectural Overview

The Gemini CLI is composed of two main packages: `packages/cli` (the frontend) and `packages/core` (the backend). The `core` package interacts with the Gemini API and a suite of tools to extend its capabilities.

For a more detailed overview of the architecture, please refer to the [architecture documentation](./docs/architecture.md).

## Documentation

All the documentation for the project is located in the `docs/` directory. If you're making changes to the documentation, you can find the relevant files there.

Thank you for your interest in contributing to the Gemini CLI!

Made with love❤️
