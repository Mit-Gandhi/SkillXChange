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

1.Firebase Firestore – NoSQL database for storing user profiles, skills, and messages

## Installation & Setup

### Clone the Repository

```
git clone https://github.com/Mit-Gandhi/Hack_with_gujarat.git
```

### Backend Setup

#### Install required dependencies:

```
pip install -r backend/requirements.txt
```

#### Run the FastAPI server:
```
cd backend
uvicorn api:app --reload
```

### Frontend Setup:
```
cd frontend  
npm install  
npm run dev  
```

## System Workflow

### User Authentication 

```/register``` – New users can create an account and log in.

```/login``` – Existing users authenticate to access the system.

### Home Page

```/home``` – The dashboard provides access to all major functionalities, including CCTV analysis, live monitoring, and sketch-to-image conversion.

### CCTV Footage Analysis

```/analyze``` – Users upload CCTV footage to detect and identify suspects.
1. The system extracts frames and detects faces using InsightFace.
2. Feature vectors are extracted using InsightFace (IR-SE50).
3. The system compares detected faces against stored records using FAISS.
4. If a match is found, it returns timestamps of all occurrences and generates trimmed video clips showing only the suspect.
   
```/analyze/report``` – Users can preview and download a detailed report with suspect information, timestamps, and video evidence.

### Live Surveillance Monitoring

```/live``` – The system connects to live surveillance feeds to detect suspects in real-time.
1. Faces are identified continuously and compared with database records.
2. If a suspect is detected, their name, location, and match confidence are displayed.
3. Alerts are triggered via Firebase Cloud Messaging (FCM) for immediate action.

### Sketch-to-Image Generation

```/sketch``` – Converts a monotone sketch into a realistic colorized image using a GAN-based model.
1. This feature enhances low-quality evidence and improves face recognition performance.

### Database Storage & Management

```/records``` – Stores and manages police records for suspect identification.
1. The system maintains a structured database of face feature vectors, names, and locations in Firebase Firestore.
2. This allows cross-referencing and information sharing between different law enforcement agencies.

## End-to-End Workflow Summary

1. Register/Login → Access dashboard.
2. Upload CCTV footage or connect live feed → Face detection & recognition.
3. Retrieve timestamps & suspect clips → Download reports for further investigation.
4. Convert sketches to images → Enhance face recognition from incomplete evidence.
5. Manage stored records → Maintain an updated police database for future references.
