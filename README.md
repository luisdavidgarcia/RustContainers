# RustOSProjects

This repository contains Rust-based projects focusing on operating system concepts. It includes various experiments and implementations showcasing different aspects of operating systems, all developed using Rust. The setup includes Docker to ensure a consistent development and testing environment across different machines.

## Project Members

- Luis David Garcia ([lgarc120@calpoly.edu](lgarc120@calpoly.edu))

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- Git
- Docker
- Rust and Cargo

The provided setup script will guide you through installing Rust, Cargo, and Docker if they are not already installed on your system.

### Setup

To set up your local development environment, follow these steps:

1. **Clone the repository**

   ```sh
   git clone git@github.com:luisdavidgarcia/RustOSProjects.git
   cd RustOSProjects
   ```

2. **Make the setup script executable**

    ```sh
    chmod +x setup.sh
    ```

3. **Run the setup script**

    ```sh
    ./setup.sh
    ```

This script will install any missing prerequisites (such as Rust, Cargo, and Docker), set up pre-commit hooks for code quality, and prepare your Docker environment.

## Developing

After running the setup, you can start developing immediately. The repository is structured as follows:

- `src/:` Source files for your Rust projects.
- `Docker/`: Contains Docker-related scripts, including a Docker environment setup script.
- `scripts/`: Other utility scripts that might be helpful during development.

## Using Docker

Your development environment is containerized to ensure consistency. To work with Docker:

- **Building the Docker image**:

The setup script takes care of building your Docker image initially. If you need to rebuild it manually:

```sh
docker build -t rustosprojects .
```

- **Running your Docker container**:

The Docker setup script also handles running your container. To manually start your container:

```sh
docker run -dit --name rustos_dev -v "$(pwd):/workspace" rustosprojects
```

- **Attaching to your Docker container:**

```sh
docker attach rustos_dev
```

## Contributing

We welcome contributions to this project! Please consider the following steps:

- Create your feature branch (`git checkout -b feature/AmazingFeature`).
- Commit your changes (`git commit -m 'Add some AmazingFeature'`).
- Push to the branch (`git push origin feature/AmazingFeature`).
- Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

