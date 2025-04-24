Below is a CONTRIBUTING.md file tailored for the ARMStrong "Radiation Control System" cross-platform client repository, built with C#, .NET 8, and Avalonia UI. It provides clear guidelines for contributing, including steps for setting up the environment, submitting changes, and adhering to coding standards.
markdown

# Contributing to ARMStrong Client

Thank you for your interest in contributing to the ARMStrong "Radiation Control System" Client! This document outlines the process for contributing to the project to ensure a smooth and collaborative experience. By contributing, you help improve the cross-platform client for radiation monitoring and control.

## Table of Contents
- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Development Environment Setup](#development-environment-setup)
- [Coding Guidelines](#coding-guidelines)
- [Submitting Changes](#submitting-changes)
- [Reporting Bugs](#reporting-bugs)
- [Requesting Features](#requesting-features)

## Code of Conduct
All contributors are expected to adhere to the [Code of Conduct](CODE_OF_CONDUCT.md). Please read it to understand the expectations for respectful and inclusive collaboration.

## How to Contribute
We welcome contributions in the form of bug fixes, new features, documentation improvements, and more. To get started, follow these steps:

- [ ] Check the [GitHub Issues](https://github.com/digital-armstrong/Armstrong.CrossPlatformClient/issues) for open issues or create a new one to discuss your contribution.
- [ ] Fork the repository to your GitHub account.
- [ ] Create a branch for your changes:
  ```bash
  git checkout -b feature/your-feature-name
  ```

  or
  ```bash
  git checkout -b bugfix/issue-number-description
  ```
- Make your changes, ensuring they align with the Coding Guidelines (#coding-guidelines).
- Test your changes thoroughly.
- Submit a pull request (PR) following the Submitting Changes (#submitting-changes) guidelines.

## Development Environment Setup
To set up your development environment, complete the following tasks:

- Install prerequisites:
  - .NET 8 SDK
  - Git
  - An IDE with C# support (e.g., Visual Studio 2022, Rider, or Visual Studio Code with C# extensions)
  - Avalonia UI templates:
    ```bash
    dotnet new install Avalonia.Templates
    ```
- Clone your forked repository:
  ```bash
  git clone https://github.com/your-username/armstrong-client.git
  cd armstrong-client

- Restore dependencies:
  ```bash
  dotnet restore
  ```
- Set up configuration:
  - Create an appsettings.json file in the project root with the following (use test or dummy values for development):
    ```json
    {
      "ApiSettings": {
        "BaseUrl": "https://test-armstrong-server-api-url",
        "ApiKey": "test-api-key"
      }
    }
    ```

- Verify the setup:
  ```bash
  dotnet build
  ```
  
- Run tests to ensure the environment is functional:
  ```bash
  dotnet test
  ```
  
# Coding Guidelines
To maintain consistency and quality, please adhere to the following guidelines:
- Follow the C# coding conventions as defined in the [Microsoft C# Coding Guidelines](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions).
- Use the MVVM pattern for Avalonia UI components, separating views, view models, and models.
- Ensure code is formatted using dotnet format. Run the following before committing:
  ```bash
  dotnet format
  ```
- Write unit tests for new functionality using xUnit (or the project's chosen testing framework).
- Include XML documentation for public classes, methods, and properties.
- Keep commits small, focused, and well-documented with clear messages, e.g.:
  ```
  Add radiation data export feature to CSV
  ```
- Avoid introducing unnecessary dependencies.
- Ensure backward compatibility with the ARMStrong server API unless explicitly discussed.

# Submitting Changes
To submit your changes, follow these steps:

- Ensure all tests pass:
  ```bash
  dotnet test
  ```
- Format and analyze your code:
  ```bash
  dotnet format
  ```
- Commit your changes with a descriptive message:
  ```bash
  git commit -m "Description of your changes"
  ```
- Push your branch to your fork:
  ```bash
  git push origin feature/your-feature-name
  ```
- Open a pull request (PR) on the main repository:
  - Use a clear title, e.g., `Add CSV export for radiation data.`
  - Reference any related issues (e.g., `Fixes #123`).
  - Describe the changes, their purpose, and any testing performed.
  - Include screenshots for UI changes (if applicable).
- Respond to feedback during the PR review process.

A maintainer will review your PR. Changes may be requested before merging.

## Reporting Bugs
To report a bug, create a new issue on the [GitHub Issues](https://github.com/digital-armstrong/Armstrong.CrossPlatformClient/issues) page with the following details:

- A clear title, e.g., `Crash when loading radiation data.`
- A description of the bug, including steps to reproduce.
- The operating system (Windows, macOS, Linux) and version.
- Any relevant logs or screenshots.
- The expected behavior and actual behavior.

Use the "Bug" issue template if available.

## Requesting Features
To request a new feature, create a new issue with the following details:

- A clear title, e.g., `Add support for dark mode.`
- A description of the feature and its use case.
- Any mockups, examples, or references to similar implementations.
- Whether you plan to implement it yourself.

## Use the "Feature Request" issue template if available.
Thank you for contributing to the ARMStrong Client! Your efforts help make radiation monitoring more accessible and reliable.
For questions or support, contact the maintainers via GitHub Issues or [email](mailto:armstrong.sys@proton.me).

```bash
### Notes:
- **Tech Stack**: The guidelines are tailored for a C# project using .NET 8 and Avalonia UI, emphasizing MVVM for UI development and xUnit for testing (adjustable if you use a different testing framework like NUnit).
- **Repository URL**: The URLs (`https://github.com/your-org/armstrong-client` and `https://github.com/your-username/armstrong-client`) are placeholders. Replace them with the actual repository URLs.
- **Code of Conduct**: The file references a `CODE_OF_CONDUCT.md`, which is assumed to exist. If you don't have one, you can remove the reference or request me to create it.
- **Configuration**: The `appsettings.json` setup assumes a typical .NET configuration approach. If your project uses a different method (e.g., environment variables), let me know.
- **Flexibility**: The guidelines are general enough to apply to most contributions but specific to the tech stack and project context. If you have additional requirements (e.g., specific testing tools, CI/CD integration, or hardware dependencies), provide them, and I can refine the document.
- **Templates**: The file mentions "Bug" and "Feature Request" issue templates. If you need these created or have specific templates, let me know.
```
