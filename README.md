# 🚀 AI Job Chommie Platform

> **AI-powered job search platform built for South Africa** - A complete SaaS solution combining intelligent job matching, seamless applications, and integrated payments.

[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://typescriptlang.org/)
[![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://postgresql.org/)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com/)

## 🌟 Features

### For Job Seekers
- 🤖 **AI-Powered Job Matching** - Intelligent recommendations based on skills, experience, and preferences
- 📄 **Smart Resume Analysis** - AI-driven resume optimization and keyword matching
- 🎯 **Personalized Job Alerts** - Real-time notifications for relevant opportunities
- 💼 **Application Tracking** - Complete application lifecycle management
- 📊 **Career Analytics** - Track your job search progress and success metrics
- 💳 **Premium Subscriptions** - Advanced features with Paystack integration

### For Employers
- 🏢 **Company Profiles** - Showcase your organization and culture
- 📝 **Job Posting Management** - Easy-to-use job creation and management tools
- 👥 **Candidate Screening** - AI-assisted candidate evaluation and ranking
- 📈 **Hiring Analytics** - Track job performance and candidate quality
- 💰 **Flexible Pricing** - Pay-per-post or subscription models

### For Administrators
- 🛠 **Platform Management** - Complete admin dashboard for system oversight
- 📊 **Advanced Analytics** - User engagement, job performance, and revenue metrics
- 🔐 **User Management** - Account administration and support tools
- 💸 **Payment Oversight** - Transaction monitoring and financial reporting

## 🏗 Architecture

This is a **monorepo** built with modern technologies and best practices:

```
aijobchommie-platform/
├── packages/
│   ├── api/          # Node.js REST API with Express & TypeScript
│   ├── web/          # Next.js 14 SaaS Application
│   ├── admin/        # Admin Dashboard (Next.js)
│   └── shared/       # Shared types, components, and utilities
├── docker/           # Docker configurations
├── docs/             # Documentation
└── .github/workflows # CI/CD pipelines
```

## 🛠 Technology Stack

### Backend (`packages/api`)
- **Runtime**: Node.js 18+ with TypeScript
- **Framework**: Express.js with advanced middleware
- **Database**: PostgreSQL with Supabase
- **ORM**: Prisma for type-safe database access
- **Cache**: Redis for session management and caching
- **AI Integration**: Hugging Face + OpenAI APIs
- **Payments**: Paystack (South African market)
- **Authentication**: JWT with refresh tokens
- **File Uploads**: Multer with image processing
- **Testing**: Jest with comprehensive test coverage

### Frontend (`packages/web`)
- **Framework**: Next.js 14 with App Router
- **Language**: TypeScript with strict mode
- **Styling**: Tailwind CSS + shadcn/ui components
- **State Management**: Zustand + TanStack Query
- **Forms**: React Hook Form + Zod validation
- **Animations**: Framer Motion
- **Icons**: Lucide React
- **Charts**: Recharts for analytics

### Admin Dashboard (`packages/admin`)
- **Framework**: Next.js 14 with TypeScript
- **UI Components**: shadcn/ui with custom admin themes
- **Data Tables**: TanStack Table for complex data management
- **Charts**: Multiple chart libraries for comprehensive analytics

### Shared (`packages/shared`)
- **Types**: Comprehensive TypeScript definitions
- **Components**: Reusable UI component library
- **Utilities**: Common functions and helpers
- **Validation**: Zod schemas for data validation

## 🚀 Quick Start

### Prerequisites
- Node.js 18.17.0 or higher
- npm 9.6.7 or higher
- Docker (optional, for local development)
- PostgreSQL (or use Supabase)
- Redis (optional, for caching)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/FernandoSteyn/aijobchommie-platform.git
   cd aijobchommie-platform
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Set up the database**
   ```bash
   npm run db:generate
   npm run db:migrate
   ```

5. **Start development servers**
   ```bash
   npm run dev
   ```

This will start:
- API server: `http://localhost:3001`
- Web application: `http://localhost:3000`
- Admin dashboard: `http://localhost:3002`

### Using Docker

```bash
npm run docker:dev
```

## 📚 Development

### Available Scripts

```bash
# Development
npm run dev          # Start all packages in development mode
npm run build        # Build all packages
npm run test         # Run all tests
npm run lint         # Lint all packages
npm run type-check   # TypeScript type checking

# Database
npm run db:generate  # Generate Prisma client
npm run db:migrate   # Run database migrations
npm run db:push      # Push schema changes to database

# Docker
npm run docker:dev   # Start development environment
npm run docker:prod  # Start production environment

# Code Quality
npm run format       # Format code with Prettier
npm run format:check # Check code formatting
```

### Project Structure

```
packages/
├── api/                 # Backend API
│   ├── src/
│   │   ├── routes/     # API endpoints
│   │   ├── middleware/ # Express middleware
│   │   ├── services/   # Business logic
│   │   ├── models/     # Data models
│   │   └── utils/      # Utility functions
│   ├── prisma/         # Database schema and migrations
│   └── tests/          # API tests
├── web/                 # Main SaaS Application
│   ├── app/            # Next.js 14 app directory
│   ├── components/     # React components
│   ├── lib/            # Utilities and configurations
│   └── public/         # Static assets
├── admin/               # Admin Dashboard
│   ├── app/            # Admin-specific pages
│   ├── components/     # Admin components
│   └── lib/            # Admin utilities
└── shared/              # Shared code
    ├── types/          # TypeScript definitions
    ├── components/     # Reusable components
    └── utils/          # Common utilities
```

## 🌍 South African Market Focus

This platform is specifically designed for the South African job market:

- **Local Payment Integration**: Paystack for secure ZAR transactions
- **Regional Job Categories**: Tailored to SA employment sectors
- **Multi-language Support**: English and Afrikaans
- **Local Employment Laws**: Compliance with SA labor regulations
- **Mobile-First Design**: Optimized for South African mobile usage patterns

## 🔒 Security Features

- **Authentication**: JWT tokens with refresh mechanisms
- **Authorization**: Role-based access control (RBAC)
- **Data Protection**: Row-level security with Supabase
- **Input Validation**: Comprehensive Zod schema validation
- **Rate Limiting**: API protection against abuse
- **CORS Protection**: Configured for production security
- **File Upload Security**: Type validation and size limits
- **Password Security**: Bcrypt hashing with strong policies

## 📈 Performance Optimizations

- **Caching Strategy**: Redis for session and data caching
- **Database Indexing**: Optimized queries with proper indexing
- **Code Splitting**: Next.js automatic code splitting
- **Image Optimization**: Sharp for image processing and compression
- **Bundle Analysis**: Webpack bundle analyzer integration
- **Lazy Loading**: Components and routes loaded on demand

## 🧪 Testing

We maintain high test coverage across all packages:

```bash
# Run all tests
npm run test

# Run tests for specific package
npm run test --workspace=@aijobchommie/api

# Run tests in watch mode
npm run test:watch

# Generate coverage report
npm run test:coverage
```

## 🚀 Deployment

### Production Build

```bash
npm run build
```

### Docker Production

```bash
docker-compose -f docker-compose.prod.yml up
```

### Environment Variables

See `.env.example` for required environment variables:

- **Database**: Supabase connection strings
- **Authentication**: JWT secrets
- **AI Services**: Hugging Face and OpenAI API keys
- **Payments**: Paystack credentials
- **Storage**: File upload configurations
- **Email**: SMTP settings for notifications

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](./docs/CONTRIBUTING.md) for details.

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Ensure all tests pass
6. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- **Documentation**: [docs/](./docs/)
- **Issues**: [GitHub Issues](https://github.com/FernandoSteyn/aijobchommie-platform/issues)
- **Discussions**: [GitHub Discussions](https://github.com/FernandoSteyn/aijobchommie-platform/discussions)

## 🏆 Acknowledgments

- Built with ❤️ for the South African job market
- Powered by cutting-edge AI technology
- Designed for scalability and performance

---

**Made in South Africa 🇿🇦 by Fernando Steyn**
