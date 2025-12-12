# Motion Design Studio - Setup Guide

## Project Overview

Motion Design Studio is a full-stack web application showcasing motion design services. Built with modern technologies, it features a responsive design, animated components, and a testimonials section.

## Tech Stack

### Frontend
- **React 19** - UI library
- **TypeScript** - Type-safe JavaScript
- **Vite 7** - Fast build tool and dev server
- **Tailwind CSS 4** - Utility-first CSS framework
- **Framer Motion** - Animation library
- **Wouter** - Lightweight routing
- **Radix UI** - Accessible component primitives
- **React Hook Form** - Form management
- **Zod** - Schema validation

### Backend
- **Express.js** - Web server framework
- **Node.js** - JavaScript runtime
- **PostgreSQL** - Database (via Drizzle ORM)
- **Passport.js** - Authentication middleware
- **WebSocket (ws)** - Real-time communication

### Development Tools
- **tsx** - TypeScript execution
- **Drizzle Kit** - Database migrations
- **ESBuild** - Fast bundler

## Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v20 or higher)
- **npm** (comes with Node.js)
- **PostgreSQL** (optional, if using database features)

## Installation

### 1. Clone or Extract the Project

If you received a zip file, extract it to your desired location.

### 2. Install Dependencies

```bash
npm install
```

This will install all required dependencies listed in `package.json`.

## Running the Application

### Development Mode

Start the development server:

```bash
npm run dev
```

This will:
- Start the Express server on port 5000
- Enable hot module replacement (HMR)
- Watch for file changes and auto-reload

Access the application at: `http://localhost:5000`

### Production Build

Build the application for production:

```bash
npm run build
```

Then start the production server:

```bash
npm start
```

## Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server with Express backend |
| `npm run dev:client` | Start Vite dev server only (frontend) |
| `npm run build` | Build for production |
| `npm start` | Start production server |
| `npm run check` | Run TypeScript type checking |
| `npm run db:push` | Push database schema changes (if using DB) |

## Project Structure

```
.
├── client/                  # Frontend application
│   ├── public/             # Static assets (favicon, images)
│   ├── src/
│   │   ├── assets/         # Images, fonts, and other assets
│   │   ├── components/     # React components
│   │   │   ├── ui/        # Reusable UI components
│   │   │   ├── About.tsx
│   │   │   ├── Contact.tsx
│   │   │   ├── Header.tsx
│   │   │   ├── Hero.tsx
│   │   │   ├── Services.tsx
│   │   │   └── ...
│   │   ├── data/          # Static data (testimonials, etc.)
│   │   ├── hooks/         # Custom React hooks
│   │   ├── lib/           # Utility functions and configs
│   │   ├── pages/         # Page components
│   │   ├── App.tsx        # Main app component
│   │   ├── main.tsx       # Application entry point
│   │   └── index.css      # Global styles
│   └── index.html         # HTML template
│
├── server/                 # Backend application
│   ├── index.ts           # Server entry point
│   ├── routes.ts          # API routes
│   ├── static.ts          # Static file serving
│   ├── storage.ts         # Storage utilities
│   └── vite.ts            # Vite integration
│
├── shared/                 # Shared types and schemas
│   └── schema.ts
│
├── script/                 # Build scripts
│   └── build.ts
│
├── attached_assets/        # Additional project assets
│
├── components.json         # Shadcn UI configuration
├── drizzle.config.ts      # Database ORM configuration
├── package.json           # Project dependencies
├── tsconfig.json          # TypeScript configuration
├── vite.config.ts         # Vite configuration
├── postcss.config.js      # PostCSS configuration
└── tailwind.config.ts     # Tailwind CSS configuration (generated)
```

## Key Features

### Pages
- **Home** - Landing page with hero section, services, and contact
- **Testimonials** - Full testimonials gallery
- **Privacy Policy** - Privacy policy page
- **Terms of Service** - Terms and conditions

### Components
- Responsive navigation header
- Animated hero section
- Services showcase
- Testimonial cards with images
- Contact form
- Social media integration
- Footer with links

### Styling
- Dark theme with navy and gold accents
- Responsive design (mobile-first)
- Smooth animations and transitions
- Accessible UI components

## Database Setup (Optional)

If your application uses database features:

1. Ensure PostgreSQL is installed and running
2. Create a database
3. Configure database connection in environment variables
4. Run migrations:

```bash
npm run db:push
```

## Environment Variables

Create a `.env` file in the root directory if needed:

```env
NODE_ENV=development
DATABASE_URL=postgresql://user:password@localhost:5432/dbname
SESSION_SECRET=your-secret-key
```

## Troubleshooting

### Port Already in Use

If port 5000 is already in use, you can:
1. Stop the process using port 5000
2. Or modify the port in `package.json` and `vite.config.ts`

### Dependencies Issues

If you encounter dependency issues:

```bash
# Clear node modules and reinstall
rm -rf node_modules package-lock.json
npm install
```

### TypeScript Errors

Run type checking to identify issues:

```bash
npm run check
```

## Development Workflow

1. Start the dev server: `npm run dev`
2. Make changes to files in `client/src/` or `server/`
3. Changes will auto-reload in the browser
4. Check console for any errors
5. Build for production when ready: `npm run build`

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Additional Resources

- [React Documentation](https://react.dev/)
- [Vite Documentation](https://vitejs.dev/)
- [Tailwind CSS Documentation](https://tailwindcss.com/)
- [Express Documentation](https://expressjs.com/)
- [Framer Motion Documentation](https://www.framer.com/motion/)

## Support

For issues or questions, refer to the project documentation or contact the development team.

---

**Version:** 1.0.0  
**Last Updated:** December 2024  
**License:** MIT
