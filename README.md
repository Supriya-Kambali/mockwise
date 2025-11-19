# 🎯 MockWise# Mockwise: Interview Scheduling and Feedback Platform



**MockWise** is an AI-powered interview practice platform that helps job seekers prepare for interviews through realistic voice conversations with AI interviewers. Get instant feedback, personalized questions, and improve your interview skills with cutting-edge AI technology.## Project Overview



![MockWise Banner](public/homepage_animation.gif)Mockwise is a web application designed for scheduling and managing interviews, along with providing a streamlined feedback system.  It leverages Firebase for backend services and offers features for user authentication, interview scheduling, and feedback submission and management.



## ✨ Features## Features



### 🎤 AI Voice Interviews* **User Authentication:** Secure user signup and signin, with a forgot password functionality.

- **Real-time voice conversations** with AI interviewer using Vapi.ai* **Interview Scheduling:**  Ability to create and manage interviews.  Individual interview pages allow for detailed viewing and management of specific interviews.

- **Natural language processing** powered by OpenAI GPT-4* **Interview Feedback:**  A dedicated feedback mechanism for each interview, allowing for structured feedback collection and review.

- **Voice recognition** with Deepgram transcription* **Admin Panel (Inferred):** The `firebase/admin.ts` file suggests the presence of an administrative panel for managing the application's data and users.

- **Text-to-speech** using ElevenLabs for realistic AI voice



### 📝 Customized Interview Generation## Installation

- Generate personalized interview questions based on:

  - Job role (Frontend Developer, Product Manager, etc.)This project uses npm and utilizes a `package.json` file for dependency management.  Ensure you have Node.js and npm installed before proceeding.

  - Experience level (Junior, Mid-level, Senior)

  - Tech stack (React, Node.js, Python, etc.)1. **Clone the repository:**

  - Interview type (Technical, Behavioral, Mixed)   ```bash

  - Number of questions (5-15)   git clone <repository_url>

   ```

### 📊 AI-Powered Feedback2. **Navigate to the project directory:**

- Comprehensive evaluation of interview performance   ```bash

- Scoring across 5 key categories:   cd mockwise

  - Communication Skills   ```

  - Technical Knowledge3. **Install dependencies:**

  - Problem Solving   ```bash

  - Cultural Fit   npm install

  - Confidence and Clarity   ```

- Detailed strengths and areas for improvement

- Final assessment and recommendations## Usage



### 🔐 User AuthenticationAfter installation, you'll need to configure your Firebase project.  Instructions for this are typically found in the Firebase documentation.  Once Firebase is configured, you can start the development server using:

- Secure Firebase Authentication

- User profile management```bash

- Interview history trackingnpm run dev

- Session-based authentication with cookies```



### 📱 Modern UI/UXThis will start a local development server. You can then access the application in your browser.

- Responsive design for all devices

- Beautiful animations with Framer MotionTo build the application for production, use:

- Dark mode support

- Real-time transcript display```bash

- Visual feedback during conversationsnpm run build

```

## 🚀 Tech Stack

## Contact Information

### Frontend

- **Next.js 15.2.3** - React framework with App RouterPlease contact the maintainers at <insert email address here> for any questions or issues.

- **React 19** - UI library
- **TypeScript** - Type safety
- **Tailwind CSS 4** - Styling
- **shadcn/ui** - UI components
- **Framer Motion** - Animations
- **Lucide React** - Icons

### Backend & AI
- **Vapi.ai** - Voice AI platform for real-time conversations
- **OpenAI GPT-4** - AI model for interviews and feedback
- **Google Generative AI (Gemini)** - Question generation
- **Vercel AI SDK** - AI integration
- **Deepgram** - Speech-to-text transcription
- **ElevenLabs** - Text-to-speech synthesis

### Database & Authentication
- **Firebase** - Authentication and user management
- **Firestore** - NoSQL database for interviews and feedback
- **Firebase Admin SDK** - Server-side operations

### Development Tools
- **Turbopack** - Fast bundler
- **ESLint** - Code linting
- **Zod** - Schema validation
- **React Hook Form** - Form management

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** 20.x or higher
- **npm** or **yarn** or **pnpm**
- **Git**

You'll also need accounts and API keys for:
- Firebase (Authentication & Firestore)
- Vapi.ai (Voice AI)
- Google AI (Gemini API)
- OpenAI (Optional, for GPT-4)

## 🛠️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/supriya-kambali/MockWise.git
cd MockWise
```

### 2. Install dependencies

```bash
npm install
# or
yarn install
# or
pnpm install
```

### 3. Set up environment variables

Create a `.env.local` file in the root directory and add the following variables:

```env
# Firebase Configuration
FIREBASE_PROJECT_ID=your-project-id
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nYour-Private-Key\n-----END PRIVATE KEY-----\n"
FIREBASE_CLIENT_EMAIL=your-service-account@your-project.iam.gserviceaccount.com

# Google Generative AI (Gemini)
GOOGLE_GENERATIVE_AI_API_KEY=your-gemini-api-key

# Vapi.ai Configuration
NEXT_PUBLIC_VAPI_WEB_TOKEN=your-vapi-web-token
NEXT_PUBLIC_VAPI_WORKFLOW_ID=your-workflow-id

# Base URL (for production)
NEXT_PUBLIC_BASE_URL=https://your-domain.com/
```

### 4. Set up Firebase

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project or use an existing one
3. Enable **Authentication** (Email/Password)
4. Enable **Firestore Database**
5. Create a service account and download the credentials
6. Add the credentials to your `.env.local` file

### 5. Set up Vapi.ai

1. Sign up at [Vapi.ai](https://vapi.ai/)
2. Create a new assistant or workflow
3. Get your Web Token and Workflow ID
4. Add them to your `.env.local` file

### 6. Set up Google AI

1. Go to [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create an API key
3. Add it to your `.env.local` file

## 🏃 Running the Application

### Development Mode

```bash
npm run dev
```

The application will be available at `http://localhost:3000`

### Production Build

```bash
npm run build
npm start
```

### Linting

```bash
npm run lint
```

## 📁 Project Structure

```
mockwise/
├── app/                          # Next.js App Router
│   ├── (auth)/                   # Authentication pages
│   │   ├── sign-in/
│   │   ├── sign-up/
│   │   └── forgotpassword/
│   ├── (root)/                   # Main application pages
│   │   ├── page.tsx              # Home page
│   │   └── interview/            # Interview pages
│   │       ├── page.tsx          # Interview setup
│   │       └── [id]/             # Dynamic interview routes
│   ├── api/                      # API routes
│   │   ├── feedback/             # Feedback generation
│   │   ├── vapi/                 # Vapi integration
│   │   └── debug/                # Debug utilities
│   ├── debug/                    # Debug page
│   ├── layout.tsx                # Root layout
│   └── globals.css               # Global styles
├── components/                   # React components
│   ├── Agent.tsx                 # Voice AI agent
│   ├── AuthForm.tsx              # Authentication forms
│   ├── InterviewCard.tsx         # Interview card component
│   ├── FixInterviewsButton.tsx   # Utility button
│   └── ui/                       # shadcn/ui components
├── lib/                          # Utility libraries
│   ├── actions/                  # Server actions
│   │   ├── auth.action.ts        # Authentication
│   │   └── general.action.ts     # General operations
│   ├── utils.ts                  # Utility functions
│   └── vapi.sdk.ts               # Vapi SDK initialization
├── firebase/                     # Firebase configuration
│   ├── admin.ts                  # Admin SDK
│   └── client.ts                 # Client SDK
├── constants/                    # Constants and configurations
│   └── index.ts                  # App constants
├── types/                        # TypeScript type definitions
│   ├── index.d.ts                # Global types
│   └── vapi.d.ts                 # Vapi types
├── public/                       # Static assets
│   ├── logo.png
│   ├── avatar.png
│   └── covers/                   # Interview cover images
├── .env.local                    # Environment variables (not in git)
├── next.config.ts                # Next.js configuration
├── tailwind.config.ts            # Tailwind CSS configuration
├── tsconfig.json                 # TypeScript configuration
└── package.json                  # Dependencies
```

## 🎮 Usage

### Creating an Interview

1. **Sign up/Sign in** to your account
2. Navigate to the **Interview** page
3. Click the **"Call"** button to start
4. The AI will ask you about:
   - Job role you're preparing for
   - Experience level
   - Tech stack/skills
   - Interview type preference
   - Number of questions
5. Confirm your selections
6. The interview will be generated and saved

### Taking an Interview

1. Go to your **Home** page
2. Select an interview from your list
3. Click **"Start Interview"**
4. Answer questions naturally via voice
5. The AI interviewer will:
   - Ask follow-up questions
   - Acknowledge your responses
   - Keep the conversation flowing

### Viewing Feedback

1. After completing an interview
2. Wait for AI-powered feedback generation
3. View comprehensive evaluation including:
   - Overall score
   - Category-wise breakdown
   - Strengths identified
   - Areas for improvement
   - Final assessment

## 🐛 Debugging

### Debug Page

Visit `/debug` to access debugging tools:
- View your user information
- Check all interviews in the database
- Fix broken interviews (if any)

### Common Issues

#### Interview not appearing on home page?
1. Go to `/debug`
2. Click "View Your Interviews (JSON)"
3. If `userId` shows `{{ userid }}`, click "Fix My Interviews"

#### Voice not working?
- Check microphone permissions in browser
- Ensure stable internet connection
- Verify Vapi.ai credentials

#### Authentication issues?
- Check Firebase configuration
- Verify environment variables
- Clear browser cookies and cache

## 🔒 Security

- Session-based authentication with HTTP-only cookies
- Secure Firebase Admin SDK for backend operations
- Environment variables for sensitive data
- Server-side validation for all operations
- Protected API routes

## 🚀 Deployment

### Deploy on Vercel (Recommended)

1. Push your code to GitHub
2. Import project on [Vercel](https://vercel.com)
3. Add environment variables in Vercel dashboard
4. Deploy!

```bash
# Using Vercel CLI
vercel --prod
```

### Environment Variables on Vercel

Make sure to add all `.env.local` variables to Vercel:
- Go to Project Settings → Environment Variables
- Add each variable from your `.env.local`
- Redeploy the application

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



## 🙏 Acknowledgments

- [Vapi.ai](https://vapi.ai/) - Voice AI Platform
- [OpenAI](https://openai.com/) - GPT-4 Model
- [Google AI](https://ai.google.dev/) - Gemini API
- [Vercel](https://vercel.com/) - Hosting Platform
- [Firebase](https://firebase.google.com/) - Backend Services
- [shadcn/ui](https://ui.shadcn.com/) - UI Components

## 📞 Support

If you have any questions or need help, please:
- Open an issue on GitHub
- Check the documentation
- Visit the `/debug` page for troubleshooting

---

<div align="center">
  <p>Built with ❤️ using Next.js, AI, and Voice Technology</p>
  <p>⭐ Star this repo if you find it helpful!</p>
</div>
