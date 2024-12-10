# Part 12 - Phonebook in Docker

## Installation

The app uses [Mongo DB Atlas](https://www.mongodb.com/atlas/database) as the database for the backend. Register to the service and create a file `backend/.env` to with content (replacing the username, password, connection string and database names)

```bash
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.o1opl.mongodb.net/phoneBookApp?retryWrites=true&w=majority
PORT=3005
```

### Run in Docker

#### Development

```bash
docker compose -f docker-compose.dev.yml up
```

#### Production

```bash
docker compose -f docker-compose.yml up
```

### Without Docker

Use the package manager npm to install the project.

```bash
cd backend && npm install && cd ..
cd frontend && npm install && cd ..
```

To build the frontend

```bash
cd frontend && npm run build
```

Run locally

```bash
npm start
```

Deployment is done by pushing the changes to `master`. GitHub Actions does the rest, including deployment to Render.
