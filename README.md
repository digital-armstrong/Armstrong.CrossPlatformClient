# ARMStrong Radiation Control System Cross-Platform Client

![](https://user-images.githubusercontent.com/46975515/218666180-742098ba-98f2-4979-960b-6a706436372f.png)

The ARMStrong Radiation Control System Client is a cross-platform application designed to interface with the ARMStrong Radiation Control System. Built with C# (.NET 8) and Avalonia UI, it provides real-time monitoring, data visualization, and control capabilities for radiation detection and management. The client supports Windows, macOS, and Linux, ensuring broad accessibility for users.

## Features
- Real-time radiation level monitoring
- Cross-platform support (Windows, macOS, Linux)
- Responsive and modern UI with Avalonia
- Remote control and configuration of radiation sensors
- Data logging and export for analysis
- Secure communication with the ARMStrong server

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Development Setup](#development-setup)
- [Running the Application](#running-the-application)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites
Before setting up the ARMStrong client, ensure the following are installed:
- [ ] .NET 8 SDK
- [ ] Git
- [ ] A supported IDE (e.g., Visual Studio 2022, Rider, or Visual Studio Code with C# extensions)
- [ ] Avalonia UI templates:
  ```bash
  dotnet new install Avalonia.Templates
  ```
- [ ] ARMStrong server API access (contact the system administrator for credentials)

## Installation
To install and set up the ARMStrong client, follow these steps:
- Clone the repository:
  ```bash
  git clone https://github.com/your-org/armstrong-client.git
  ```
- Navigate to the project directory:
  ```bash
  cd Armstrong.CrossPlatformClient
  ```
- Restore dependencies:
  ```bash
  dotnet restore
  ```
- Configure application settings:
  - Create an appsettings.json file in the project root (or modify the existing one).
  - Add the following configuration:
    ```JSON
    {
      "ApiSettings": {
      "BaseUrl": "https://your-armstrong-server-api-url",
      "ApiKey": "your-api-key"
      }
    }
    ```
- Verify the setup:
  ```bash
  dotnet build
  ```
## Development Setup
To set up the project for development, complete the following tasks:
- Install development tools:
  - Ensure your IDE has Avalonia UI support (e.g., install the Avalonia extension for Visual Studio Code).
  - Install the .NET workload for Avalonia (if not already included):
    ```bash
    dotnet workload install avalonia
    ```
- Set up linting and formatting:
  - Configure a .editorconfig file for consistent code style.
  - Run code analysis:
    ```bash
    dotnet format
    ```
- Set up unit testing:
  - Install a testing framework (e.g., xUnit, NUnit) if not already included:
    ```bash
    dotnet add package xunit
    dotnet add package xunit.runner.visualstudio
    ```
  - Run tests:
    ```bash
    dotnet test
    ```
- Start the development environment:
  ```bash
  dotnet run --project src/Armstrong.Client/Armstrong.CrossPlatformClient.csproj
  ```

## Running the Application
To run the ARMStrong client in different modes, use the following commands:
- Run the application in development mode:
  ```bash
  dotnet run --project src/Armstrong.Client/Armstrong.CrossPlatformClient.csproj
  ```
- Build the application for production:
  ```bash
  dotnet publish --configuration Release
  ```
- Package the application for distribution:
  - For Windows:
    ```bash
    dotnet publish -r win-x64 -c Release --self-contained true /p:PublishSingleFile=true
    ```
  - For macOS:
    ```bash
    dotnet publish -r osx-x64 -c Release --self-contained true /p:PublishSingleFile=true
    ```
  - For Linux:
    ```bash
    dotnet publish -r linux-x64 -c Release --self-contained true /p:PublishSingleFile=true
    ```

## Contributing
We welcome contributions to the ARMStrong client! To contribute, follow these steps:
- Fork the repository.
- Create a new branch:
  ```bash
  git checkout -b feature/your-feature-name
  ```
- Make your changes and commit them:
  ```bash
  git commit -m "Add your feature description"
  ```
- Push to your branch:
  ```bash
  git push origin feature/your-feature-name
  ```
- Open a pull request with a detailed description of your changes.
- Ensure all tests pass and code adheres to the style guide.

For more details, see CONTRIBUTING.md.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
For support, issues, or feature requests, please open an issue on the [GitHub Issues page](https://github.com/digital-armstrong/armstrong.crossplatformclient/issues).

```bash
### Notes:
- **Tech Stack**: The README is tailored for a C# project using .NET 8 and Avalonia UI, which is ideal for cross-platform desktop applications with a modern UI framework.
- **Project Structure**: The commands assume a typical project structure (e.g., `src/ARMStrong.Client/ARMStrong.Client.csproj`). Adjust the paths if your structure differs.
- **Configuration**: The `appsettings.json` configuration is a common approach for .NET applications. If your project uses a different configuration method (e.g., environment variables or a custom config file), let me know.
- **Packaging**: The `dotnet publish` commands use `--self-contained true` to create standalone executables for each platform, which is suitable for distribution. If you prefer framework-dependent builds, I can modify the instructions.
- **Repository URL**: The URL (`https://github.com/your-org/armstrong-client`) is a placeholder. Replace it with the actual repository URL.
- **Additional Details**: If you have specific requirements (e.g., hardware dependencies, additional tools, or specific Avalonia features like MVVM), provide them, and I can further refine the README.
```
