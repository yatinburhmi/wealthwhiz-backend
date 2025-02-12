This directory follows Modular Structure + Service Layer Pattern

project directory structure:

wealthwhiz-backend/
│── src/
│   ├── config/              # Configuration files (e.g., environment variables)
│   │   ├── db.ts            # Prisma database connection
│   │   ├── env.ts           # Environment variables loader
│   │   ├── logger.ts        # Winston/Pino logger setup
│   │
│   ├── modules/             # Feature-based modules
|   |   ├── accounts/
│   │   │   ├── account.controller.ts
│   │   │   ├── account.service.ts
│   │   │   ├── account.routes.ts
│   │   │   ├── account.validation.ts
│   │   │   ├── account.types.ts
│   │   │   ├── account.test.ts
│   │   ├── auth/
│   │   │   ├── auth.controller.ts
│   │   │   ├── auth.service.ts
│   │   │   ├── auth.routes.ts
│   │   │   ├── auth.validation.ts
│   │   │   ├── auth.middleware.ts
│   │   │   ├── auth.types.ts
│   │   │   ├── auth.test.ts
│   │   │
│   │   ├── users/
│   │   │   ├── user.controller.ts
│   │   │   ├── user.service.ts
│   │   │   ├── user.routes.ts
│   │   │   ├── user.validation.ts
│   │   │   ├── user.types.ts
│   │   │   ├── user.test.ts
│   │   │
│   │   ├── expenses/
│   │   │   ├── expense.controller.ts
│   │   │   ├── expense.service.ts
│   │   │   ├── expense.routes.ts
│   │   │   ├── expense.validation.ts
│   │   │   ├── expense.types.ts
│   │   │   ├── expense.test.ts
│   │
│   ├── middlewares/         # Global middlewares (auth, error handling, validation)
│   │   ├── authMiddleware.ts
│   │   ├── errorHandler.ts
│   │   ├── validateRequest.ts
│   │
│   ├── utils/               # Utility functions (e.g., hashing, JWT, etc.)
│   │   ├── hash.ts
│   │   ├── jwt.ts
│   │   ├── response.ts
│   │
│   ├── app.ts               # Express app configuration
│   ├── server.ts            # Entry point to start the server
│
│── prisma/                  # Prisma ORM configuration
│   ├── migrations/          # Prisma migrations
│   ├── schema.prisma        # Database schema
│   ├── seed.ts              # Seed data script
│
│── tests/                   # Integration tests (Jest, Supertest)
│── .env                     # Environment variables
│── .gitignore               # Git ignore file
│── package.json             # Dependencies
│── tsconfig.json            # TypeScript configuration