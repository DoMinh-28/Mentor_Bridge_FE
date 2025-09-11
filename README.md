# 🌉 Mentor Bridge

**Mentor Bridge** is a comprehensive web application for student mentoring management, designed to connect students with mentors through an efficient booking system, real-time chat, and team project management.

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Technologies Used](#-technologies-used)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [API Endpoints](#-api-endpoints)
- [Deployment](#-deployment)
- [Contributing](#-contributing)

## 🎯 Overview

Mentor Bridge is a comprehensive mentoring platform designed to:

- Connect students with suitable mentors
- Manage mentoring schedules flexibly
- Support real-time communication through chat
- Manage student teams and projects
- Track progress and evaluate effectiveness

## ✨ Key Features

### 👥 Multi-Role User Management

- **Admin**: Manage entire system, users, semesters, configurations
- **Mentor**: Manage schedules, respond to booking requests, track students
- **Student**: Book mentor sessions, join teams, manage projects

### 📅 Smart Booking System

- Book mentor sessions based on available time slots
- View personal and team schedules
- Reschedule and cancel bookings
- Automatic notifications for appointments

### 💬 Real-time Chat

- Direct messaging between mentors and students
- Typing status indicators
- Complete message history
- Responsive chat interface

### 👨‍👩‍👧‍👦 Team and Project Management

- Create and join teams
- Manage team members
- Assign roles (Leader/Member)
- Track project progress

### 📊 Dashboard and Reports

- Overview statistics for each role
- Visual charts with Recharts and Nivo
- Booking history and activities
- Points reward system

### 🔐 Authentication and Security

- Google Firebase login
- JWT token authentication
- Role-based protected routes
- Automatic token refresh

## 🛠 Technologies Used

### Frontend

- **React 18.3.1** - UI Library
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **Redux Toolkit** - State management
- **React Router DOM** - Routing
- **Ant Design** - UI Components
- **Tailwind CSS** - Styling
- **SCSS** - CSS preprocessor

### Supporting Libraries

- **Axios** - HTTP client
- **Firebase** - Authentication
- **Socket.js + STOMP** - Real-time communication
- **Moment.js** - Date/time handling
- **React Toastify** - Notifications
- **Recharts & Nivo** - Data visualization
- **FullCalendar** - Calendar component
- **QR Code React** - QR code generation

### Development Tools

- **ESLint** - Code linting
- **Storybook** - Component development
- **Docker** - Containerization
- **Nginx** - Web server

## 🚀 Installation

### System Requirements

- Node.js >= 18.0.0
- npm or yarn
- Git

### Install Dependencies

```bash
# Clone repository
git clone <repository-url>
cd Mentor_Bridge_FE

# Install dependencies
npm install

# Or using yarn
yarn install
```

### Environment Configuration

Create `.env` file in root directory:

```env
VITE_API_URL_LOCAL=http://localhost:8888
VITE_API_URL_SERVER=http://your-server-url:8888
```

### Run Application

```bash
# Development mode
npm run dev

# Build production
npm run build

# Preview production build
npm run preview

# Run Storybook
npm run storybook
```

## 💻 Usage

### Login

1. Access the application at `http://localhost:5173`
2. Choose "Login with Google" or login with email/password
3. System will redirect based on user role

### For Students

1. **Home**: View team information, upcoming appointments
2. **Booking**: Select mentor and suitable time slots
3. **Schedule**: View all booked appointments
4. **Chat**: Communicate with mentors
5. **History**: Track attended mentoring sessions

### For Mentors

1. **Home**: View booking requests, statistics
2. **Schedule**: Manage available time slots
3. **Booking Requests**: Accept/reject requests
4. **Chat**: Support students
5. **History**: Track completed mentoring sessions

### For Admins

1. **Overview**: Overall statistics dashboard
2. **User Management**: CRUD operations for users
3. **Semester Management**: Set up semesters
4. **Topic Management**: Approve/reject topics
5. **Configuration**: Set system parameters

## 📁 Project Structure

```
src/
├── components/          # React components
│   ├── atoms/          # Basic UI components
│   ├── molecules/      # Composite components
│   ├── organisms/      # Complex components
│   ├── templates/      # Page templates
│   └── layouts/        # Layout components
├── pages/              # Page components
│   ├── admin/         # Admin pages
│   ├── mentor/        # Mentor pages
│   ├── student/       # Student pages
│   └── login/         # Authentication pages
├── services/          # API services
├── redux/             # State management
├── hooks/             # Custom hooks
├── utils/             # Utility functions
├── constants/         # Constants and enums
├── config/            # Configuration files
├── context/           # React contexts
├── middleware/        # Route protection
└── assets/            # Static assets
```

## 🔌 API Endpoints

### Authentication

- `POST /login` - User login
- `POST /login-google` - Google login
- `POST /register` - User registration
- `POST /refresh` - Refresh token

### Booking

- `GET /booking/mentor-meeting` - Get mentor's meetings
- `GET /booking/student-meeting` - Get student's meetings
- `POST /booking` - Create new booking
- `POST /reschedule` - Reschedule appointment
- `POST /finish` - Complete mentoring session

### Team & Topic

- `GET /team` - Get team information
- `POST /team` - Create new team
- `POST /invite` - Invite team member
- `GET /topic` - Get topic list
- `POST /topic` - Create new topic

### Chat

- `GET /chat` - Get chat list
- `GET /chat/:id` - Get chat details
- `POST /chat/send/:id` - Send message
- `POST /chat/typing/:id/:userName` - Send typing status

## 🐳 Deployment

### Docker Deployment

```bash
# Build Docker image
docker build -t mentor-bridge-fe .

# Run container
docker run -p 80:80 mentor-bridge-fe
```

### Manual Deployment

```bash
# Build production
npm run build

# Deploy to server (example)
scp -r dist/* user@server:/var/www/html/
```

### Environment Variables

```env
# Production
VITE_API_URL_SERVER=http://your-production-server:8888

# Development
VITE_API_URL_LOCAL=http://localhost:8888
```

## 🤝 Contributing

1. Fork the project
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Create Pull Request

### Coding Standards

- Use TypeScript for type safety
- Follow ESLint rules
- Write components following Atomic Design
- Use conventional commits
- Write tests for important components

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

## 📞 Contact

- **Project Link**: [https://github.com/your-username/mentor-bridge-fe](https://github.com/your-username/mentor-bridge-fe)
- **Demo**: [https://your-demo-url.com](https://your-demo-url.com)

---

⭐ If this project is helpful, please give us a star!
