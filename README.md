# Project Name
HN(HamidrezaNawtaj) - Platform Documentation
## Description
This is a mksodc static page documentation of our platform for developers.

This code is responsible for generating the static pages for our platform, providing documentation and information to developers. It serves as a reference guide for developers to understand the various features and functionalities of our platform.

## Installation

### Docker Image

To install and run the project using Docker, follow these steps:

1. Install Docker on your machine if you haven't already.
2. Pull the Docker image from the packages section of repository:

  ```bash
  docker pull ghcr.io/navtajr/thomas-at-2:latest
  ```

3. Run the Docker container:

  ```bash
  docker run -p 8080:80 -d ghcr.io/navtajr/thomas-at-2:latest
  ```

4. Access the project in your browser at `http://localhost:8080`.

### Running Locally

To run the project locally, follow these steps:

1. Clone the repository:

  ```bash
  git clone https://github.com/navtajr/thomas-at-2.git
  ```

2. Install the necessary dependencies:

  ```bash
  cd repository
  pip install -r requirements.txt
  ```

3. Start the local server:

  ```bash
  mkdocs serve
  ```

4. Access the project in your browser at `http://localhost:8080`.


## Contributing

Got feedback? We welcome contributions and feedback. Create an issue or email
1. 2310781014@fh-burgenland.at
2. 2310781020@fh-burgenland.at


