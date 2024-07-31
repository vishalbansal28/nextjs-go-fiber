# My Demo Project

This project is a web application built using [Next.js](https://nextjs.org/) for the frontend and [Fiber](https://gofiber.io/) for the backend written in Go. It integrates various functionalities such as user management, product management, and authentication with Keycloak.

## Getting Started

### Prerequisites

- Node.js
- npm or yarn
- Go

### Frontend Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/vishalbansal28/nextjs-go-fiber.git
   cd demo-project
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Run the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd demo-backend
   ```

2. Install Go dependencies:
   ```bash
   go mod tidy
   ```

3. Set up the environment variables in a `.env` file.

4. Run the backend server:
   ```bash
   go run main.go
   ```

### Docker Setup

1. Ensure Docker and Docker Compose are installed.

2. Start the Docker containers:
   ```bash
   docker-compose up
   ```

## Project Structure

### Frontend (Next.js)

- **`pages`**: Contains Next.js pages.
- **`components`**: Reusable UI components.
- **`app`**: Main application folder.
- **`styles`**: Global CSS files.
- **`public`**: Static files like images, icons, etc.
- **`utils`**: Utility functions and wrappers.

### Backend (Go Fiber)

- **`api`**: API routes and handlers.
- **`domain`**: Domain entities.
- **`use_cases`**: Business logic.
- **`infrastructure`**: External integrations like data stores and identity management.
- **`shared`**: Shared code like enums and JWT helpers.

## Key Functionalities

### Authentication

The project uses Keycloak for authentication. The `jwt.go` and `requires_realm_role.go` middleware files handle JWT token verification and role-based access control.

### User Management

The `user_management.go` handler and `register.go` use case manage user registration.

### Product Management

The `products.go` handler and `create_product.go`, `get_products.go` use cases handle product creation and retrieval.

### Middleware

Custom middleware is defined in the `middlewares` folder to handle logging, request ID generation, and JWT authentication.

### Configuration

Configuration is managed using Viper in Go (`initViper` function in `main.go`). Environment variables are loaded and used throughout the backend.

## Learn More

- [Next.js Documentation](https://nextjs.org/docs) - Learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - Interactive Next.js tutorial.
- [Fiber Documentation](https://docs.gofiber.io/) - Learn about Fiber features and API.

## Deployment

The easiest way to deploy the Next.js app is to use the [Vercel Platform](https://vercel.com/). Check out the [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

For the backend, consider using platforms like Heroku, AWS, or any other cloud provider that supports Go applications.

## Contributing

Your feedback and contributions are welcome! Please check out the [Next.js GitHub repository](https://github.com/vercel/next.js/) and [Fiber GitHub repository](https://github.com/gofiber/fiber) for more information.

