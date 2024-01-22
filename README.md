
## Deployment

View the live deployment [here](https://language-learning-helper-will-helliwell.vercel.app/).

## Progress

Working on:
- Creating an authentication and authorization system so that a user can login

Completed:
- Setup the main repository and database, and deployed these to Vercel and NeonDb respectively
  
## Stack

| Tech | Use |
|------------------|------------------|
| NextJs | Web Framework  |
| NextJs - API routes | Backend API routing + serverless functions |
| Typescript | Backend |
| Prisma | ORM |
| PostgreSQL | Relational Database |
| ESLint | Linting |
| Prettier | Formatting |
| Github Actions | CI Pipeline |
| Vercel | NextJs Deployment |
| NeonDb | Database Deployment |
  
## Database Architecture

![image](https://github.com/Will-Helliwell/language_learning_helper/assets/68912961/f1088199-fe09-49c2-b955-6dbb2906c237)

## Deployment Architecture

### Current Architecture
- Development:
    - App - npm run dev
    - Database - following deployment, create a ‘development’ db branch in neon and point your local project to this via .env (this will ensure the dev database is an identical copy of the prod db at the given point in time, including configuration, schema and data).
- Production:
    - App - on merge to master: Vercel autodeploy of project code
    - Database - on merge to master: npx prisma migrate deploy in GActions
- Preview:
    - Doesn’t yet exist. Can follow [this](https://neon.tech/blog/branching-with-preview-environments) if want to get it working.

### Ideal Future Architecture

Environments:
- **Development** - all run on developer's local machine
- **Staging** - database and NextJs deployed in staging environments (Neon and Vercel respectively)
- **Production** - database and NextJs deployed in production environments (Neon and Vercel respectively)

![image](https://github.com/Will-Helliwell/language_learning_helper/assets/68912961/811045cd-9e76-42ea-89dd-364fdd04dbe8)


## To Clone and Run

1. First clone the repo following Github's instructions.
2. Then navigate to the root of the repo and run `npm i` to install dependencies on your machine.
3. Then run the development server with `npm run dev`

Open [http://localhost:3000](http://localhost:3000) with your browser to see the frontend.  
Backend routes can be accessed by appending /api (e.g. [http://localhost:3000/api/hello](http://localhost:3000/api/hello)).
