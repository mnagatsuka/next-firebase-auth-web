# next-firebase-auth-web

.
├── docs/
│   ├── api/
│   │   ├── openapi.yml # OpenAPI specification
│   │   ├── openapi.bundled.yml
│   │   ├── paths/
│   │   ├── components/
│   │   │   ├── examples/
│   │   │   ├── parameters/
│   │   │   ├── responses/
│   │   │   └── schemas/
│   │   └── README.md
│   ├── ui/
│   │   ├── design-system.md
│   │   └── pages/
│   ├── auth/
│   │   ├── firebase-setup.md # Firebase configuration guide
│   │   └── authentication.md # Auth flow documentation
│   ├── deployment/
│   │   ├── vercel.md # Vercel deployment guide
│   │   └── environment.md # Environment variables setup
│   ├── development/
│   │   ├── getting-started.md # Local development setup
│   │   ├── coding-standards.md # Code style and conventions
│   │   └── developing-workflow.md # Development workflow based on OpenAPI and UI specifications
│   ├── architecture/
│   │   └── overview.md # System architecture
│   └── README.md # Main documentation index
├── src/
│   ├── app/
│   ├── components/
│   ├── hooks/
│   ├── lib/
│   │   ├── api/
│   │   │   ├── generated/ # OpenAPI generated files
│   │   │   └── customFetch.ts # Custom fetch client fo Server and Client components
│   │   ├── auth/
│   │   ├── config/
│   │   │   └── env.ts
│   │   ├── constants/
│   │   ├── design/
│   │   │   └── tokens.ts
│   │   ├── errors/
│   │   ├── firebase/
│   │   │   ├── admin.ts
│   │   │   ├── auth.ts
│   │   │   └── client.ts
│   │   ├── providers/
│   │   ├── stores/
│   │   └── utiless/
│   ├── stores/
│   ├── types/
│   ├── mocks/
│   │   ├── handlers.ts
│   │   ├── browser.ts
│   │   └── server.ts
│   └── middleware.ts
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── public/
├── .env.example
├── Dockerfile
├── docker-compose.yml
├── pakage.json
└── README.md # Project overview


## Applicable Versions

These guidelines are written for:

- **Next.js**: `15.x` and later  
- **React**: `18.x` (including support for React Server Components)  
- **TypeScript**: `5.x` with strict compiler settings enabled  

The recommendations may not apply to older versions.


## Libraries & Tools in Scope

While the primary focus is **Next.js + TypeScript**, the following libraries and tools are part of our standard setup:

### 1. State Management
- **Zustand** — minimal and flexible client state management  
- **TanStack Query** — server state fetching and caching

### 2. Data Fetching & API
- **TanStack Query** — async data fetching, caching, and sync
- **Orval** - generate API client

### 3. Forms & Validation
- **Zod** — TypeScript-first schema validation

### 4. Styling & UI Components
- **Tailwind CSS** — utility-first CSS framework  
- **shadcn/ui** — headless UI components built with Tailwind

### 5. Authentication & Security
- **Firebase Auth** — authentication with identity providers

### 6. Testing
- **Vitest** — Vite-native unit/integration testing  
- **Testing Library** (React Testing Library) — DOM testing utilities  
- **Playwright** — modern E2E testing framework  
- **MSW** (Mock Service Worker) — API mocking for tests

### 7. Storybook & Design Systems
- **Storybook** — isolated UI development and documentation

### 8. Performance & Monitoring
- **Lighthouse** — performance monitoring and analysis in Chrome

### 9. Deployment & CI/CD
- **Vercel** — official Next.js hosting

### 10. Developer Experience
- **Biome** — code linter and formatter  
- **pnpm** — fast, disk space-efficient package manager

### 11. Local Development & Testing Environment
- **Docker** — containerized development environment  
- **Docker Compose** — multi-container orchestration for local setup and testing


## Out of Scope

These guidelines do **not** cover:

- Backend service development (covered in separate backend guidelines)  
- Non-Next.js frontend frameworks  
- Project management and workflow conventions (e.g., Git branching)  
