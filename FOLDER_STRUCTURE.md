# 📁 TourEase Folder Structure

This document outlines the folder structure of the TourEase project and provides guidelines for organizing code.

## Current Project Structure

```
TourEase/
├── frontend/                    # React + Vite frontend application
│   ├── public/                  # Static assets served directly
│   │   └── vite.svg            # Vite logo
│   ├── src/                     # Source code
│   │   ├── assets/             # Images, fonts, and other static resources
│   │   ├── components/         # Reusable React components
│   │   │   └── Navigation.jsx  # Navigation bar component
│   │   ├── pages/              # Page-level components
│   │   │   ├── Home.jsx        # Home page
│   │   │   ├── About.jsx       # About page
│   │   │   ├── Destinations.jsx # Destinations page
│   │   │   └── Contact.jsx     # Contact page
│   │   ├── App.css             # Main application styles
│   │   ├── App.jsx             # Root component with routing
│   │   ├── index.css           # Global styles and Tailwind imports
│   │   └── main.jsx            # Application entry point
│   ├── .gitignore              # Git ignore rules
│   ├── eslint.config.js        # ESLint configuration
│   ├── index.html              # HTML template
│   ├── package.json            # Dependencies and scripts
│   ├── package-lock.json       # Locked dependency versions
│   ├── vite.config.js          # Vite configuration
│   └── README.md               # Frontend documentation
└── README.md                    # Project documentation
```

## Recommended Folder Structure (Future Expansion)

As the project grows, consider organizing code into these additional folders:

```
frontend/src/
├── assets/                      # Static resources
│   ├── images/                 # Image files
│   ├── icons/                  # Icon files
│   └── fonts/                  # Custom fonts
├── components/                  # Reusable components
│   ├── common/                 # Shared components (Button, Card, etc.)
│   ├── layout/                 # Layout components (Header, Footer, Sidebar)
│   └── features/               # Feature-specific components
├── pages/                       # Page components (one per route)
├── hooks/                       # Custom React hooks
├── utils/                       # Utility functions
│   ├── helpers.js              # Helper functions
│   └── constants.js            # Constants and configuration
├── services/                    # API calls and external services
│   └── api.js                  # API client
├── context/                     # React Context providers
├── styles/                      # Additional stylesheets
│   └── themes/                 # Theme configurations
└── routes/                      # Route definitions
```

## Folder Guidelines

### `/components`
- **Purpose**: Reusable UI components
- **Naming**: PascalCase (e.g., `Navigation.jsx`, `TourCard.jsx`)
- **Structure**: One component per file
- **Best Practice**: Keep components small and focused on a single responsibility

### `/pages`
- **Purpose**: Top-level route components
- **Naming**: PascalCase matching route names (e.g., `Home.jsx`, `About.jsx`)
- **Structure**: One page per route
- **Best Practice**: Pages should compose components, not contain complex logic

### `/assets`
- **Purpose**: Static files like images, fonts, icons
- **Organization**: Group by type (images/, icons/, fonts/)
- **Best Practice**: Use descriptive names and optimize file sizes

### `/hooks` (Recommended)
- **Purpose**: Custom React hooks for reusable logic
- **Naming**: camelCase with 'use' prefix (e.g., `useAuth.js`, `useFetch.js`)
- **Best Practice**: Extract common logic into custom hooks

### `/utils` (Recommended)
- **Purpose**: Helper functions and utilities
- **Naming**: camelCase (e.g., `formatDate.js`, `validators.js`)
- **Best Practice**: Pure functions without side effects

### `/services` (Recommended)
- **Purpose**: API calls and external service integrations
- **Naming**: camelCase (e.g., `tourService.js`, `authService.js`)
- **Best Practice**: Centralize all API calls

### `/context` (Recommended)
- **Purpose**: React Context for global state management
- **Naming**: PascalCase with 'Context' suffix (e.g., `AuthContext.jsx`)
- **Best Practice**: Use for truly global state only

## File Naming Conventions

- **Components**: PascalCase (e.g., `TourCard.jsx`)
- **Utilities**: camelCase (e.g., `formatDate.js`)
- **Styles**: kebab-case (e.g., `tour-card.css`)
- **Constants**: UPPER_SNAKE_CASE (e.g., `API_ENDPOINTS.js`)

## Best Practices

1. **Component Organization**
   - Keep components small and focused
   - Extract reusable logic into custom hooks
   - Use composition over inheritance

2. **Import Order**
   - React imports first
   - Third-party libraries
   - Local components
   - Utilities and helpers
   - Styles

3. **File Structure**
   - One component per file
   - Co-locate related files (component + styles + tests)
   - Use index.js for cleaner imports

4. **Code Organization**
   - Group related functionality
   - Keep files under 300 lines
   - Extract complex logic into separate files

## Technology Stack

- **Framework**: React 19.1.1
- **Build Tool**: Vite 7.1.7
- **Routing**: React Router DOM 7.9.6
- **Styling**: Tailwind CSS 4.1.17
- **Icons**: Lucide React 0.553.0
- **Linting**: ESLint 9.36.0

## Getting Started

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linter
npm run lint
```

## Contributing

When adding new features:
1. Create components in appropriate folders
2. Follow naming conventions
3. Update this document if adding new folders
4. Keep the structure clean and organized

## Future Considerations

As the project scales, consider:
- Adding a backend folder for API
- Implementing state management (Redux/Zustand)
- Adding testing folders (\_\_tests\_\_/)
- Creating a shared component library
- Adding documentation folder for guides
