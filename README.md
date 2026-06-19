# NightCode: A Terminal-Based AI Coding Agent

NightCode is an advanced terminal application designed to bring the power of AI directly into your development workflow. It functions as an AI coding assistant, enabling both read-only analysis ("Plan" mode) and direct code implementation ("Build" mode) within your local project environment. This project showcases a modern, full-stack application built with a focus on developer experience and powerful integrations.

## Technology Stack Overview

NightCode is built as a monorepo, leveraging a diverse set of powerful tools and frameworks to deliver a robust and interactive experience.

### **Core Infrastructure & Runtime**
*   **Bun**: Utilized across the project for its fast JavaScript runtime, package manager, and bundler capabilities, providing a high-performance foundation for both the CLI and server.
*   **TypeScript**: Ensures type safety and improves code quality and maintainability throughout the entire codebase.

### **Frontend (CLI)**
*   **OpenTUI**: A framework for building rich terminal user interfaces, providing the interactive foundation for the NightCode CLI.
*   **React**: Powers the UI components within the terminal, allowing for a declarative and component-driven approach to building the CLI's interface.

### **Backend (API Server)**
*   **Hono**: A lightweight and fast web framework for the server-side API, designed for edge and web platforms, offering an efficient way to handle requests.
*   **AI SDK (Vercel)**: Facilitates seamless integration with various AI models, handling streaming responses and abstracting away the complexities of AI API interactions.

### **Database & ORM**
*   **PostgreSQL**: The chosen relational database for persistent storage of user sessions, messages, and other application data.
*   **Prisma ORM**: Provides a type-safe and intuitive way to interact with the PostgreSQL database, simplifying database migrations and data access.

### **Authentication & User Management**
*   **Clerk**: Handles user authentication and session management. It provides a browser-based OAuth flow for the CLI, securing access to user-specific features.
*   **JWT (JSON Web Tokens)**: Used for secure information exchange between the client and server after authentication.

### **AI Models & Integrations**
*   **Anthropic API**: Integrated for accessing Anthropic's suite of AI models, supporting powerful conversational AI capabilities.
*   **OpenAI API**: Integrated for accessing OpenAI's suite of AI models, offering alternative and diverse AI capabilities.
*   **Shared Model Registry**: Allows for flexible configuration and switching between different AI models.

### **Billing & Usage Metering**
*   **Polar**: Integrated for managing billing and credit metering. It tracks AI usage, allowing the application to gate features based on user credits and manage subscriptions.

### **Overall Architecture**
NightCode employs a client-server architecture. The CLI acts as the client, communicating with a Hono API server. This server handles AI model interactions, database operations, authentication with Clerk, and billing with Polar. The monorepo structure, managed by Bun, simplifies development and dependency management across the different packages (e.g., `cli`, `server`, `database`, `shared`).

This robust combination of technologies allows NightCode to provide a powerful, secure, and highly interactive AI coding experience directly within your terminal.
