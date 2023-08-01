# Base Clean Architecture Example

## Introduction

This repository contains a base .NET Web API solution that follows the principles of Clean Architecture. It's designed to provide a solid foundation for building scalable and maintainable applications with a focus on separation of concerns and modularity.

## Structure

The solution is organized into the following main projects:

- **Domain**: Contains all entities, enums, exceptions, interfaces, types, and logic specific to the domain layer.
- **Application**: This layer contains all application logic. It is dependent on the domain layer but has no dependencies on any other layer or project.
- **Infrastructure**: Contains classes for accessing external resources such as file systems, web services, SMTP, etc.
- **API**: This is the entry point of the application. It depends on both the Application and Infrastructure layers but not directly on the Domain layer.
- **Presentation**: This is the frontend of the application. This layer could be removed completely if you are developing the FE on another solution.

## Basic Features

The solution presents a few basic additions, which are displayed as follows:
- **Dependency Injection**: A DependencyInjection class to represent the service registrations for each layer, to be used on program.cs later on during the project setup
- **MediatR**: MediatR library added
- **FluentValidation**: FluentValidation library added
- **Serilog**: Serilog library added and configured properly

## Getting Started

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/marcelomusza/BaseCleanArchitectureExample.git
   ```

2. Navigate to the project directory:
   ```bash
   cd BaseCleanArchitectureExample
   ```

3. Restore the required packages:
   ```bash
   dotnet restore
   ```

4. Build and run the project:
   ```bash
   dotnet build
   dotnet run --project WebAPI
   ```

## Usage

You can now access the API at `http://localhost:5000/`. Explore the endpoints and utilize them as per your requirements.

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.


