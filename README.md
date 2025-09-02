# Next.js Folder Structure Examples

This repository contains three different examples of Next.js folder structures, demonstrating how to organize your codebase as your application grows in complexity. Each example represents a different level of architectural sophistication, from beginner-friendly to enterprise-scale.

## 🎯 Project Overview

All three examples implement the same **GatherUp** application - a community events platform where users can discover, join, and host events. The functionality remains consistent across all examples, but the code organization and architectural patterns evolve to handle increasing complexity.

### Features Implemented

- **User Authentication** - Sign in/out functionality
- **Event Management** - Create, view, and manage events
- **RSVP System** - Users can RSVP to events
- **Dashboard** - User and host dashboards
- **Search & Filtering** - Find events by various criteria
- **Payment Integration** - Stripe integration for paid events
- **File Uploads** - Event image uploads
- **Real-time Updates** - Live notifications and updates

## 📁 Folder Structure Comparison

### 1. Beginner Project (`beginner-project/`)

**Best for:** Learning Next.js, small projects, rapid prototyping

```
gatherup/
├── app/                    # Next.js App Router
│   ├── api/               # API routes
│   ├── dashboard/         # Dashboard pages
│   ├── marketing/         # Marketing pages
│   └── page.tsx          # Home page
├── components/            # Reusable UI components
├── lib/                  # Utility functions
├── types/                # TypeScript type definitions
└── package.json
```

**Key Characteristics:**

- ✅ Simple, flat structure
- ✅ Easy to understand and navigate
- ✅ Quick to set up and modify
- ✅ Perfect for learning Next.js fundamentals
- ❌ Can become messy as project grows
- ❌ No clear separation of concerns
- ❌ Difficult to scale with team

**Dependencies:**

- Next.js 15.5.0
- React Hook Form
- Zod validation
- Tailwind CSS
- Lucide React icons

### 2. Intermediate Project (`intermediate-project/`)

**Best for:** Medium-sized applications, small teams, production apps

```
gatherup/
├── app/                   # Next.js App Router with route groups
│   ├── (auth)/           # Authentication routes
│   ├── (dashboard)/      # Protected dashboard routes
│   ├── (marketing)/      # Public marketing routes
│   └── api/              # API routes
├── features/             # Feature-based organization
│   ├── events/           # Event-related functionality
│   ├── rsvp/             # RSVP functionality
│   └── users/            # User management
├── server/               # Server-side logic
│   ├── auth/             # Authentication configuration
│   ├── db/               # Database schema and client
│   ├── mutations/        # Database mutations
│   ├── queries/          # Database queries
│   └── services/         # Business logic services
├── ui/                   # Shared UI components
├── lib/                  # Utility functions
└── tests/                # Test files
```

**Key Characteristics:**

- ✅ Feature-based organization
- ✅ Clear separation of client/server code
- ✅ Database layer abstraction
- ✅ Testing infrastructure
- ✅ Authentication integration
- ✅ Payment processing
- ❌ More complex to set up
- ❌ Requires understanding of patterns

**Dependencies:**

- Next.js 15.5.0
- NextAuth.js for authentication
- Prisma ORM with PostgreSQL
- Stripe for payments
- UploadThing for file uploads
- Vitest for testing

### 3. Advanced Project (`advanced-project/`)

**Best for:** Large applications, enterprise projects, multiple teams

```
gatherup/
├── app/                   # Next.js App Router with advanced routing
│   ├── (core)/           # Core application routes
│   ├── (public)/         # Public routes
│   └── api/              # API routes with microservice structure
├── entities/             # Domain entities (DDD approach)
│   ├── event/            # Event domain
│   ├── rsvp/             # RSVP domain
│   └── user/             # User domain
├── features/             # Feature modules
│   ├── create-event/     # Event creation feature
│   ├── host-payouts/     # Host payout feature
│   ├── rsvp-event/       # RSVP feature
│   └── search/           # Search feature
├── widgets/              # Complex UI widgets
├── shared/               # Shared infrastructure
│   ├── config/           # Configuration management
│   ├── libs/             # Shared libraries
│   │   ├── auth/         # Authentication utilities
│   │   ├── cache/        # Caching layer
│   │   ├── db/           # Database utilities
│   │   ├── http/         # HTTP client
│   │   ├── logger/       # Logging system
│   │   └── queue/        # Background job queue
│   ├── ui/               # Design system components
│   └── validation/       # Shared validation schemas
├── processes/            # Business processes
├── services/             # External service integrations
├── tests/                # Comprehensive testing
│   ├── e2e/              # End-to-end tests
│   ├── integration/      # Integration tests
│   └── unit/             # Unit tests
└── scripts/              # Build and deployment scripts
```

**Key Characteristics:**

- ✅ Domain-Driven Design (DDD) approach
- ✅ Microservice-ready architecture
- ✅ Comprehensive testing strategy
- ✅ Advanced routing with parallel routes
- ✅ Shared infrastructure layer
- ✅ Scalable for large teams
- ✅ Separation of concerns at every level
- ❌ Complex setup and learning curve
- ❌ Overkill for small projects
- ❌ Requires architectural expertise

**Dependencies:**

- Next.js 15.5.0
- Advanced routing patterns
- Comprehensive testing setup
- Infrastructure abstractions
- Design system components

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn
- PostgreSQL (for intermediate and advanced projects)

### Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd 3-nextjs-folder-structure
   ```

2. **Choose your project level**

   ```bash
   # For beginner project
   cd beginner-project/gatherup

   # For intermediate project
   cd intermediate-project/gatherup

   # For advanced project
   cd advanced-project/gatherup
   ```

3. **Install dependencies**

   ```bash
   npm install
   ```

4. **Set up environment variables**

   ```bash
   cp .env.example .env.local
   # Edit .env.local with your configuration
   ```

5. **Run the development server**

   ```bash
   npm run dev
   ```

6. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📚 Learning Path

### Start with Beginner

- Learn Next.js fundamentals
- Understand App Router basics
- Practice with simple components
- Get comfortable with TypeScript

### Progress to Intermediate

- Learn feature-based organization
- Understand server/client separation
- Practice with databases and authentication
- Implement testing strategies

### Advance to Advanced

- Master domain-driven design
- Learn enterprise patterns
- Understand microservice architecture
- Practice with complex routing

## 🎥 YouTube Video

This repository accompanies a YouTube video that walks through each folder structure, explaining:

- When to use each approach
- How to migrate between structures
- Best practices for each level
- Common pitfalls to avoid

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Next.js team for the amazing framework
- The React community for excellent tooling
- All contributors who helped improve these examples

---

**Happy coding!** 🚀

Choose the folder structure that matches your project's complexity and team size. Remember, you can always evolve your structure as your application grows!
