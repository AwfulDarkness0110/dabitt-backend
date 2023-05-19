## About

dabitts was a side project mainly created to expand my understanding of how to build a full stack application with features like authentication, theme providers, and using Next.js with a node backend. The site itself is meant to serve as a low friction to do app that also provides analytics on where and how you have been spending the majority of your time.

Overall, I had a ton of fun working on the project and learned a lot about how to get a full stack project from ideation to deployed.

You can checkout the final hosted product at: https://dabitts.com/

## Running Locally

This project has a few third party dependencies as well as a [corresponding frontend](https://github.com/smartman1234/dabitt-frontend) that needs to be setup before you can run the app locally. A <i>.env.example</i> file has also been provided as an example of how your <i>.env</i> file should be structured.

#### Auth0

For authentication the project uses [Auth0](https://auth0.com/) which requires the following <i>.env</i> variables to be set.

```bash
#Auth0
AUDIENCE="[YOUR AUTH0 AUDIENCE]"
ISSUER_BASE_URL="[YOUR AUTH0 ISSUER BASE URL]"
```

#### Postgres

The api uses a postgres database with prisma as the ORM. Before running make sure that you have a postgres database running locally and that the connection string has been added to the <i>.env</i> file.

```bash
#Postgres
DATABASE_URL="[YOUR DATABASE CONNECTION STRING]"
```

Once added you need to migrate the prisma schema to your local database:

```bash
npx prisma migrate dev --name init
```

#### Run

Once the above has been configured you can run the development server:

```bash
npm run devStart
# or
yarn devStart
```

Open http://localhost:3001 (or whatever port you specified in <i>.env</i>) with your browser to see the result.
