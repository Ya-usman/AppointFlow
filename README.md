# AppointFlow

AppointFlow is a modern appointment management platform built with React, TypeScript, and Supabase. It provides a clean and intuitive interface for managing appointments, clients, and schedules.

visite the App: https://musical-semolina-d4b50b.netlify.app
login: 
Email: test@example.com
Password: password123

## Features

- 📅 **Appointment Management**
  - Create, view, and manage appointments
  - Real-time status updates (pending, confirmed, cancelled)
  - Client information tracking

- 📊 **Dashboard**
  - Overview of key metrics
  - Recent appointments
  - Quick statistics

- 👤 **User Profiles**
  - Secure authentication
  - Profile management
  - Personal settings

- 🔒 **Security**
  - Email and password authentication
  - Row Level Security (RLS)
  - Protected routes

## Tech Stack

- **Frontend**
  - React 18
  - TypeScript
  - Tailwind CSS
  - Lucide Icons
  - React Router DOM
  - React Hot Toast

- **Backend**
  - Supabase
  - PostgreSQL
  - Row Level Security

## Getting Started

1. **Clone the repository**

```bash
git clone <repository-url>
cd appointflow
```

2. **Install dependencies**

```bash
npm install
```

3. **Environment Setup**

Create a `.env` file in the root directory with your Supabase credentials:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

4. **Start the development server**

```bash
npm run dev
```

5. **Build for production**

```bash
npm run build
```

## Project Structure

```
src/
├── components/     # Reusable UI components
├── lib/           # Utility functions and configurations
├── pages/         # Application pages/routes
├── types/         # TypeScript type definitions
└── main.tsx       # Application entry point
```

## Database Schema

### Appointments Table
- `id`: UUID (Primary Key)
- `created_at`: Timestamp
- `title`: Text
- `description`: Text
- `date`: Date
- `time`: Text
- `user_id`: UUID (Foreign Key)
- `client_name`: Text
- `client_email`: Text
- `status`: Enum ('pending', 'confirmed', 'cancelled')

### Profiles Table
- `id`: UUID (Primary Key)
- `full_name`: Text
- `updated_at`: Timestamp
- `created_at`: Timestamp

## Authentication

The application uses Supabase Authentication with email and password. To test the application, you can use:

- Email: test@example.com
- Password: password123

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Deployment

The application is deployed on Netlify. You can view the live version at:
https://musical-semolina-d4b50b.netlify.app

## Support

For support, please open an issue in the repository or contact the maintainers.
