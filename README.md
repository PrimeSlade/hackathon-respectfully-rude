# Respectfully Rude

A humorous hackathon project that generates AI-powered backhanded compliments with personalized roast images. Upload your photo or Upload a photo of yourself or someone you want to roast, get roasted with creative sarcasm, and share the laughs!

## Tech Stack

### Frontend

- **React** - UI library
- **Vite** - Build tool and dev server
- **React Router** - Client-side routing
- **Tailwind CSS** - Styling framework
- **DaisyUI** - UI component library
- **Axios** - HTTP client
- **Lucide React** - Icon library

### Backend

- **Node.js** - Runtime environment
- **Hono** - Lightweight web framework
- **TypeScript** - Type-safe JavaScript
- **Prisma** - ORM for database management
- **MySQL** - Database
- **JWT** - Authentication
- **Bcrypt** - Password hashing
- **Cloudinary** - Image storage and management

### AI Integration

- **Google Gemini AI** - Generates creative backhanded compliments
- **Replicate (Flux Model)** - Creates custom cartoon-style roast images

## Prerequisites

- Node.js (v18 or higher)
- MySQL database
- Google Gemini API key
- Replicate API token
- Cloudinary account

## Installation & Setup

### 1. Clone the Repository

```bash
git clone <repository-url>
cd hackathon-respectfully-rude
```

### 2. Backend Setup

```bash
cd respectfully-rude-backend

# Install dependencies
npm install

# Create .env file
touch .env
```

Add the following environment variables to `.env`:

```env
DATABASE_URL="mysql://user:password@localhost:3306/respectfully_rude"
SHADOW_DATABASE_URL="mysql://user:password@localhost:3306/respectfully_rude_shadow"
PORT=3000
GEMINI_API_KEY="your_gemini_api_key"
REPLICATE_API_TOKEN="your_replicate_token"
JWT_SECRET="your_jwt_secret"
COOKIE_SECRET_KEY="your_cookie_secret_key"
FRONT_END_PORT="http://localhost:5173"
CLOUD_NAME="your_cloudinary_cloud_name"
CLOUD_API_KEY="your_cloudinary_api_key"
CLOUD_API_SECRET="your_cloudinary_api_secret"
```

```bash
# Generate Prisma client
npx prisma generate

# Run database migrations
npx prisma migrate dev

# Start the backend server
npm run dev
```

The backend will run on `http://localhost:3000`

### 3. Frontend Setup

```bash
cd ../respectfully-rude-frontend

# Install dependencies
npm install

# Create .env file (if needed)
touch .env
```

Add the following to `.env`:

```env
VITE_API_URL="http://localhost:3000"
```

```bash
# Start the frontend development server
npm run dev
```

The frontend will run on `http://localhost:5173`

## Features

- **User Authentication** - Secure sign-up and login with JWT
- **Profile Management** - Upload and manage profile pictures
- **AI-Powered Roasts** - Generate backhanded compliments using Gemini AI
- **Custom Roast Images** - Create cartoon-style roast images with Replicate
- **Image Storage** - Cloud-based storage with Cloudinary
- **Responsive Design** - Modern UI that works on all devices

## Project Structure

```
hackathon-respectfully-rude/
├── respectfully-rude-backend/
│   ├── prisma/
│   │   └── schema.prisma
│   ├── src/
│   │   ├── controllers/
│   │   ├── routes/
│   │   ├── models/
│   │   ├── middlewares/
│   │   ├── utils/
│   │   └── index.ts
│   └── package.json
└── respectfully-rude-frontend/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── contexts/
    │   └── App.jsx
    └── package.json
```

## Team

Led a team of three developers in this hackathon project.

## License

This project was created for a hackathon competition.
