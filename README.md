# Docker React Example

This project is a sample React application bootstrapped with [Create React App](https://github.com/facebook/create-react-app), containerized with Docker, and ready for CI/CD with Travis CI and AWS Elastic Beanstalk.

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Node.js](https://nodejs.org/) (for local development without Docker)
- [npm](https://www.npmjs.com/)

### Running Locally (with Docker)

#### Development

To start the app in development mode with hot reloading:

```sh
docker-compose -f docker-compose-dev.yml up
```

- The app will be available at [http://localhost:3000](http://localhost:3000).

#### Running Tests

To run tests in watch mode using Docker:

```sh
docker-compose -f docker-compose-dev.yml run tests
```

#### Production Build

To build and run the production-ready app:

```sh
docker-compose up
```

- The app will be available at [http://localhost](http://localhost).

## Running Locally (without Docker)

Install dependencies:

```sh
npm install
```

Start the development server:

```sh
npm start
```

Run tests:

```sh
npm test
```

Build for production:

```sh
npm run build
```

## Continuous Integration

This repo uses Travis CI to build and test the app in Docker, and deploys to AWS Elastic Beanstalk on pushes to the `master` branch. See [.travis.yml](.travis.yml) for details.

## Project Structure

- `src/` – React source code
- `public/` – Static assets and HTML template
- `Dockerfile` – Production Docker build
- `Dockerfile.dev` – Development & test Docker build
- `docker-compose.yml` – Production Docker Compose
- `docker-compose-dev.yml` – Development & test Docker Compose

## Learn More

- [Create React App Documentation](https://facebook.github.io/create-react-app/docs/getting-started)
- [React Documentation](https://reactjs.org/)
- [Docker Documentation](https://docs.docker.com/)

---