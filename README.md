# Docker Builder

A lightweight and efficient **Docker-based build system** using **YAML, Python, and Docker** to automate the creation of Docker images for your codebase.

## Features
- Automates the process of building Docker images from source code
- Uses **YAML** for defining build configurations
- Built with **Python** for flexibility and extensibility
- Leverages **Docker** to containerize applications seamlessly
- Includes **GitHub Actions** for CI/CD automation

## Prerequisites
Ensure you have the following installed on your system:

- [Docker](https://docs.docker.com/get-docker/)
- [Python 3.x](https://www.python.org/downloads/)
- Pip dependencies (see `requirements.txt`)

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/idevanshrai/Docker-Builder.git
   cd Docker-Builder
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Usage

### Step 1: Define Your Build Configuration
Create a `.yml` file to specify the build parameters. Example:
```yaml
image_name: my-custom-image
base_image: python:3.9
requirements:
  - flask
  - requests
commands:
  - echo "Building Docker Image..."
  - pip install -r requirements.txt
  - python app.py
```

### Step 2: Run the Docker Builder
Execute the Python script to build the Docker image:
```sh
python build.py config.yml
```

### Step 3: Run the Generated Docker Image
After a successful build, run your container:
```sh
docker run -p 5000:5000 my-custom-image
```

## Project Structure
```
.
├── backend/              # Backend services
├── frontend/             # Frontend application
├── .github/workflows/    # CI/CD pipeline configurations
├── docker-compose.yml    # Docker Compose configuration
├── nginx.conf            # Nginx configuration for deployment
├── build.py              # Python script to parse YAML and build Docker image
├── config.yml            # Example YAML configuration file
├── Dockerfile.template   # Template for Dockerfile generation
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
```

## Contributing
Feel free to submit issues, feature requests, or pull requests to improve this project.

## License
This project is licensed under the MIT License. See `LICENSE` for details.

## Contact
For any queries, reach out to [@idevanshrai](https://github.com/idevanshrai).

