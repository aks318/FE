# Prompt: Build a Production-Ready React Frontend Boilerplate

Act as a Senior Frontend Architect. Build a clean, scalable, production-ready frontend boilerplate using the following technology stack.

## 1. Technology Stack

- React 19
- Vite
- TypeScript (strict mode)
- React Router DOM
- Axios
- SCSS / SCSS Modules
- Material UI (MUI)
- MUI Icons
- React Hook Form
- Zod (form validation)
- ESLint
- Prettier
- Environment-based configuration

Use the latest stable, mutually compatible package versions.

## 2. Architecture Requirements

Follow a **feature-based modular architecture** with clear separation of concerns.

The architecture should:
- Be scalable for large enterprise applications.
- Keep business logic separate from UI components.
- Keep API communication separate from components.
- Support reusable components and shared utilities.
- Support lazy-loaded routes.
- Support centralized error handling.
- Support authentication and authorization in the future.
- Be easy for multiple developers to maintain.


## 3. Axios Configuration

Create a centralized Axios architecture.

Requirements:
- One reusable Axios instance.
- Base URL from environment variables.
- Configurable request timeout.
- Request interceptor for authentication tokens.
- Response interceptor for common API errors.
- Centralized error handling.
- Handle 401, 403, 404, 422, and 500 responses.
- Support request cancellation using AbortController.
- Support custom headers.
- Never hardcode API URLs.

Create a reusable typed API service pattern.

Example:

```typescript
apiClient.get<T>('/endpoint');
apiClient.post<T>('/endpoint', payload);
apiClient.put<T>('/endpoint', payload);
apiClient.delete<T>('/endpoint');
```

## 4. Environment Configuration

Create:

```text
.env.development
.env.production
.env.example
```

Use Vite environment variables with the `VITE_` prefix.

Example:

```env
VITE_API_BASE_URL=http://localhost:8000/api/v1
VITE_APP_NAME=AI Customer Support
```

Create a centralized, type-safe environment configuration.

Validate required environment variables at application startup.

## 5. Routing

Implement React Router DOM.

Requirements:
- Centralized route definitions.
- Lazy loading using React.lazy().
- Suspense fallback.
- Not Found page.
- Main layout.
- Authentication layout.
- Protected route implementation as a reusable foundation.
- Keep feature routes organized within their respective modules.

## 6. MUI Theme Configuration

Create a centralized MUI theme.

Requirements:
- Primary and secondary colors.
- Typography configuration.
- Button customization.
- Input customization.
- Card customization.
- Consistent border radius.
- Light and dark theme support.
- ThemeProvider integration.

Avoid styling every component independently when a reusable theme configuration can handle it.

## 7. SCSS Architecture

Use SCSS Modules for component-level styling.

Requirements:
- Global variables.
- Mixins.
- Reusable functions.
- Reset styles.
- Typography styles.
- Responsive breakpoints.
- Consistent spacing conventions.

Avoid global CSS pollution.

Use MUI's `sx` prop for simple one-off MUI styling and SCSS Modules for more complex component styling.

## 8. Code Quality

Configure:
- TypeScript strict mode.
- ESLint.
- Prettier.
- Absolute imports using `@/`.
- Consistent naming conventions.
- Avoid unnecessary `any`.
- Avoid duplicate code.
- Avoid oversized components.
- Prefer functional components and custom hooks.

## 9. Initial Application

Build a minimal working application containing:

1. Application entry point.
2. App providers.
3. Router configuration.
4. Main layout.
5. Sidebar navigation.
6. Header/navbar.
7. Dashboard placeholder page.
8. Not Found page.
9. Centralized Axios instance.
10. MUI theme.
11. Global SCSS setup.

The initial dashboard should be clean and professional.

Do not build the actual chatbot functionality yet.

## 10. Development Guidelines

IMPORTANT:

- First inspect the existing project directory.
- Do not overwrite or delete existing files without asking.
- Create the project structure incrementally.
- Install only necessary dependencies.
- Do not introduce Redux unless there is a genuine requirement.
- Do not introduce unnecessary abstractions.
- Keep components small and reusable.
- Use proper TypeScript interfaces and types.
- Ensure all imports resolve correctly.
- Ensure the project builds successfully.

## 11. Execution Strategy

Follow these phases:

**Phase 1:** Initialize Vite + React + TypeScript.

**Phase 2:** Install and configure dependencies.

**Phase 3:** Create the folder structure.

**Phase 4:** Configure SCSS and MUI theme.

**Phase 5:** Configure Axios and environment variables.

**Phase 6:** Implement routing and layouts.

**Phase 7:** Build the initial dashboard.

**Phase 8:** Run TypeScript checks, ESLint, and production build.

After each phase:
- Explain what was created.
- Show important files.
- Explain architectural decisions briefly.
- Verify the implementation before moving forward.

Do not skip phases or generate the entire application in one giant file.

The final result must be a clean, extensible, production-ready frontend foundation.