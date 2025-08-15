# Interactive Quiz Platform

A modern Kahoot-style quiz application that combines live multiplayer gaming with solo study features, powered by AI-generated content. Built with Next.js 15, React 19, TypeScript, and Firebase.

Homepage

<img width="1456" height="832" alt="image" src="https://github.com/user-attachments/assets/e0ec385b-df48-417b-9b4f-f93a09d36c93" />

Dashboard

<img width="1456" height="832" alt="image" src="https://github.com/user-attachments/assets/022cf97e-af05-4484-950b-d19843042610" />


## Features

### Game Modes
- **Live Multiplayer** - Host real-time quiz competitions with PIN-based joining
- **Solo Study** - Personal practice sessions with flashcards and quiz modes  
- **Player Mode** - Join hosted games using PIN codes

### AI Integration
- AI-powered quiz generation from topic descriptions
- Automated question and answer creation
- Smart content generation for any subject

### Real-time Functionality
- Live player joining and scoring
- Real-time leaderboards and synchronized gameplay
- Automatic game cleanup system
- Player activity tracking

## Tech Stack

- **Frontend**: Next.js 15, React 19, TypeScript, Tailwind CSS 4
- **Backend**: Firebase (Realtime Database, Authentication, Firestore, Hosting)
- **Icons**: Lucide React, React Icons
- **Build**: Static export for Firebase hosting

## Project Structure

```
src/
├── app/
│   ├── layout.tsx              # Root layout with fonts and metadata
│   ├── page.tsx                # Main app with routing logic
│   └── globals.css             # Global styles
├── components/
│   ├── auth/
│   │   ├── AuthProvider.tsx    # Firebase auth context
│   │   ├── AuthPage.tsx        # Authentication forms
│   │   └── EmailVerificationBanner.tsx
│   ├── main/
│   │   ├── MainPage.tsx        # Landing page
│   │   ├── UserDashboard.tsx   # User dashboard
│   │   └── UserProfile.tsx     # Profile settings
│   ├── host/
│   │   ├── HostDashboard.tsx   # Game setup
│   │   ├── GameHost.tsx        # Live game control
│   │   ├── QuizEditor.tsx      # Quiz creation
│   │   └── QuizLibrary.tsx     # Quiz management
│   ├── player/
│   │   ├── PlayerJoin.tsx      # Game PIN entry
│   │   └── PlayerGame.tsx      # Player game view
│   ├── solo/
│   │   ├── SoloSetup.tsx       # Solo session config
│   │   ├── SoloGame.tsx        # Solo quiz mode
│   │   └── Flashcard.tsx       # Flashcard component
│   └── ai/
│       └── prompts.tsx         # AI prompt templates
├── lib/
│   ├── firebase.ts             # Firebase configuration
│   └── quizStorage.ts          # Quiz data management
├── hooks/
│   ├── useFirebaseData.ts      # Real-time data sync
│   └── useGameCleanup.ts       # Game cleanup management
├── types/
│   └── game.ts                 # TypeScript interfaces
└── utils/
    ├── gameUtils.ts            # Game logic and scoring
    └── gameCleanup.ts          # Cleanup utilities
```

## Getting Started

### Prerequisites
- Node.js 18 or later
- Firebase account
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone [repository-url]
cd quiz-app
```

2. Install dependencies
```bash
npm install
```

3. Set up Firebase
   - Create a new Firebase project
   - Enable Authentication, Realtime Database, and Firestore
   - Add your Firebase configuration to environment variables

4. Configure environment variables
```bash
# Create .env.local file with your Firebase config
NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_auth_domain
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_storage_bucket
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id
```

5. Run the development server
```bash
npm run dev
```

6. Open [http://localhost:3000](http://localhost:3000) in your browser

### Deployment

Build and deploy to Firebase Hosting:

```bash
npm run build
npm run deploy
```

## Usage

### For Hosts
1. Sign up/sign in to your account
2. Create a new quiz or select from your library
3. Start a live game and share the PIN with players
4. Monitor real-time progress and leaderboards

### For Players
1. Enter the game PIN on the join page
2. Enter your name to join the game
3. Answer questions as they appear
4. View your score and ranking on the leaderboard

### For Solo Study
1. Browse available quizzes
2. Choose between quiz mode or flashcard mode
3. Study at your own pace with immediate feedback

## Configuration

### Firebase Rules
Ensure your Firebase Realtime Database and Firestore rules are properly configured for security while allowing the necessary read/write operations.

### Custom Styling
The app uses a custom color scheme defined in Tailwind CSS:
- Primary: #568EA6
- Secondary: #305F72
- Accent: #F0B7A4
- Background: #F0F4F8

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For questions or issues, please open an issue on GitHub or contact the development team.
