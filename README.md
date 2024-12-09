# Part 11 - Phonebook CI

(Rest of Part 11 is [here](https://github.com/olsandy/full-stack-open-pokedex))

### Installation

Use the package manager npm to install the project.

```bash
npm install
cd frontend && npm install && cd ..
```

The app uses [Mongo DB Atlas](https://www.mongodb.com/atlas/database) as the database. Register to the service and create a file named `.env` to the root of your project with content (replacing the username, password, connection string and database names)

```bash
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.o1opl.mongodb.net/phoneBookApp?retryWrites=true&w=majority
PORT=3005
```

To build the app

```bash
npm run build:ui
```

Run locally

```bash
npm start
```

Deployment is done by pushing the changes to `master`. GitHub Actions does the rest, including deployment to Render.
