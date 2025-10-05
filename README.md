# Express.js Starter Template

A comprehensive Express.js starter template with TypeScript, Prisma ORM, Socket.IO, and essential middleware for building scalable web applications.

## 🚀 Features

- **TypeScript**: Full TypeScript support with proper type definitions
- **Express.js**: Fast, unopinionated web framework for Node.js
- **Prisma ORM**: Type-safe database client with SQLite (easily configurable for other databases)
- **Socket.IO**: Real-time bidirectional event-based communication
- **Session Management**: Express sessions with Prisma store
- **Security**: Helmet.js for security headers, CORS, and bcrypt for password hashing
- **File Upload**: Multer for handling multipart/form-data
- **Validation**: Express-validator for request validation
- **Authentication**: JWT and session-based authentication middleware
- **Development Tools**: Nodemon for hot reloading, TypeScript compilation

## 📦 Included Packages

### Production Dependencies

- **@prisma/client** (^6.11.1) - Type-safe database client
- **@quixo3/prisma-session-store** (^3.1.13) - Prisma-based session store
- **@types/multer** (^2.0.0) - TypeScript definitions for Multer
- **bcrypt** (^6.0.0) - Password hashing library
- **canvas** (^3.2.0) - HTML5 Canvas API for Node.js
- **cors** (^2.8.5) - CORS middleware
- **dotenv** (^17.0.1) - Environment variable loader
- **express** (^5.1.0) - Web framework
- **express-session** (^1.18.1) - Session middleware
- **express-validator** (^7.2.1) - Validation middleware
- **helmet** (^8.1.0) - Security middleware
- **jsonwebtoken** (^9.0.2) - JWT implementation
- **multer** (^2.0.2) - Multipart form data handler
- **socket.io** (^4.8.1) - Real-time communication

### Development Dependencies

- **@types/bcrypt** (^5.0.2) - TypeScript definitions for bcrypt
- **@types/cors** (^2.8.19) - TypeScript definitions for CORS
- **@types/express** (^5.0.3) - TypeScript definitions for Express
- **@types/express-session** (^1.18.2) - TypeScript definitions for express-session
- **@types/jsonwebtoken** (^9.0.10) - TypeScript definitions for JWT
- **@types/node** (^24.0.10) - TypeScript definitions for Node.js
- **nodemon** (^3.1.10) - Development server with hot reload
- **prisma** (^6.11.1) - Prisma CLI and migration tools
- **ts-node** (^10.9.2) - TypeScript execution for Node.js
- **typescript** (^5.8.3) - TypeScript compiler

## 🏗️ Project Structure

```
├── prisma/
│   ├── schema.prisma          # Database schema
│   ├── seed.ts               # Database seeding script
│   └── migrations/           # Database migrations
├── src/
│   ├── @types/              # Custom TypeScript definitions
│   ├── controllers/         # Route controllers
│   ├── emitters/           # Event emitters
│   ├── handlers/           # Socket.IO and other handlers
│   ├── middleware/         # Custom middleware
│   │   ├── authenticate.ts  # Authentication middleware
│   │   ├── errorHandler.ts  # Global error handler
│   │   ├── requestLogger.ts # Request logging
│   │   ├── uploadHandler.ts # File upload handler
│   │   └── validator.ts     # Request validation
│   ├── routes/             # API routes
│   ├── services/           # Business logic services
│   ├── utils/              # Utility functions
│   │   └── prisma.ts       # Prisma client instance
│   ├── validators/         # Validation schemas
│   ├── index.ts           # Application entry point
│   └── responses.ts       # Response utilities
├── package.json
├── tsconfig.json          # TypeScript configuration
└── README.md
```

## 🛠️ Setup and Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd server
   ```

2. **Install dependencies**

   ```bash
   pnpm install
   # or
   npm install
   ```

3. **Setup environment variables**
   Create a `.env` file in the root directory:

   ```env
   PORT=5000
   JWT_SECRET=your-jwt-secret
   SESSION_SECRET=your-session-secret
   DATABASE_URL="file:./dev.db"
   ```

4. **Setup database**

   ```bash
   # Generate Prisma client
   pnpm prisma:generate

   # Run migrations
   pnpm prisma:migrate

   # Seed database (optional)
   pnpm seed
   ```

## 🚦 Available Scripts

- `pnpm dev` - Start development server with hot reload
- `pnpm build` - Build TypeScript to JavaScript
- `pnpm start` - Start production server
- `pnpm prisma:generate` - Generate Prisma client
- `pnpm prisma:migrate` - Run database migrations
- `pnpm prisma:studio` - Open Prisma Studio
- `pnpm seed` - Run database seeding script

## 🔧 Configuration

### Database

By default, the template uses SQLite. To use a different database:

1. Update the `datasource` in `prisma/schema.prisma`
2. Update the `DATABASE_URL` in your `.env` file
3. Run `pnpm prisma:migrate` to apply changes

### TypeScript

TypeScript configuration is in `tsconfig.json`. The setup includes:

- Custom type definitions in `src/@types`
- Source maps for debugging
- Strict type checking

## 🔐 Security Features

- **Helmet.js**: Sets various HTTP headers for security
- **CORS**: Configurable cross-origin resource sharing
- **Session Security**: Secure session configuration with Prisma store
- **Password Hashing**: bcrypt for secure password storage
- **JWT Authentication**: Token-based authentication middleware

## 📡 Real-time Features

Socket.IO is configured for real-time communication with:

- Organized handlers in `src/handlers/`
- Event emitters in `src/emitters/`
- Session integration for authenticated socket connections

## 🎯 Usage

This template provides a solid foundation for building:

- REST APIs
- Real-time applications
- Authentication systems
- File upload services
- Database-driven applications

## 📝 License

ISC License

## 🤝 Contributing

Feel free to submit issues and enhancement requests!
