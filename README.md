# SkillXChange – A Skill-Swapping Platform

## Overview

SkillXChange is a web-based platform that empowers users to exchange skills and services directly with one another. It connects individuals based on their expertise and requirements, enabling mutual learning and collaboration without involving monetary transactions. The system ensures a smooth user experience with dynamic navigation, real-time chat, authentication, and conditional profile routing.

## Features

1. User Authentication – Firebase-based login and registration with secure UID handling.
2. Dynamic Routing – New users are directed to profile setup, while returning users go directly to the home dashboard.
3. Skill-Based Matchmaking – Users can send/receive skill exchange requests based on their listed skills.
4. Live Chat & Messaging – In-platform messaging for real-time communication between matched users.
5. Responsive Navigation – Navbar updates dynamically based on login status (Login/Signup or Chat/Requests/Profile).
6. Admin Control Panel – Admin privileges managed via UID to allow moderation and platform maintenance.

## Team Members

1. [Mit Gandhi](https://github.com/Mit-Gandhi) 
2. [Rishit Srivastava](https://github.com/rishitsrivastav) 
3. [Ansh Verma](https://github.com/verma07ansh)

## Tech Stack

### Frontend

1. React.js – Component-based UI development
2. Vite.js – Lightning-fast development environment
3. Tailwind CSS – Utility-first styling for responsive and modern UI
4. Firebase Auth – User authentication and session management

### Backend

1. Firebase Firestore – NoSQL database for storing user profiles, skills, and messages

## Installation & Setup

### Clone the Repository

```
git clone https://github.com/Mit-Gandhi/SkillXChange.git
```

### Frontend Setup:
```
cd frontend  
npm install  
npm run dev  
```

## System Workflow

### User Authentication 

• New users redirected to /profile-setup to fill in name, skills, and interests.

• Returning users redirected to /home after verifying UID and profile existence.

• Admin users recognized using a pre-defined UID list.

### Navbar Logic

• Before Login: Shows platform logo + name (left), Login & Signup (right)

• After Login:

  - Left: Logo + "SkillXChange"
  - Center: Requests, Messages, Chats
  - Right: User profile image + name, Sign Out button

### Skill Exchange

• Users can browse skills, send requests, and manage accepted exchanges.

• Real-time chat enables seamless conversation between matched users.

### Chat & Messaging

• Each skill match includes a dedicated chat room.

• Firebase Firestore stores messages with timestamps for persistence.

### Admin Access
• Admins can view all users, status of requests, and reported profiles.

• Admin UID check is implemented during login to enable access.
