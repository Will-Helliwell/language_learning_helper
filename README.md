
## Deployment

View the live deployment [here](https://language-learning-helper-will-helliwell.vercel.app/).

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

## Planned Deployment Architecture

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
