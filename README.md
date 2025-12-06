# Web Fundamentals Project G1

## Project Technologies:

This project uses the following technologies:

- Next.js
- React
- TypeScript
- Drizzle ORM
- SQLite (for development)

## Setup guide:

Please follow this guide to setup this repository locally.

1. Clone this repository into a suitable folder by using this command:

```
git clone https://github.com/edmundlzen/web-fundamentals-project-g1
```

2. After cloning the repository, cd into the directory and run the command below to install all dependencies:

```
cd web-fundamentals-project-g1
npm install
```

3. Open the project in VS Code (recommended) using the following command:

```
code .
```

## To run the web server:

1. Make sure you have followed the setup guide above
2. Run the following command in the terminal:

```
npm run dev
```

## To quickly push changes to the database:

1. Make sure you have followed the setup guide above
2. To quickly push schema changes to the database, run the following command in the terminal:

```
npx prisma db push
```
