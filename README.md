 # <p align="center">💖TelMedSphere - Backend</p>
<!-------------------------------------------------------------------------------------------------------------------------------------->

<div id="top"></div>

<h2>🧾 Table of Contents</h2>

 [📌 Introduction](#introduction).<br>
 [💡 Backend API Features](#backend-api-features).<br>
 [🚀 Technology Stack](#technology-stack).<br>
 [🏗️ Backend Architecture](#backend-architecture).<br>
 [💥 Getting Started](#getting-started).<br>
 [🐳 Docker Setup](#docker-setup).<br>
 [📑 API Documentation](#api-documentation).<br>
 [📊 Environment Variables](#environment-variables).<br>
 [⚡ Project Admin & Mentors](#project-admin-and-mentors).<br>
 [💬 Contributing](#contributing-with-fun).<br>
 [📑 License](#license).<br>
<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>📌Introduction</h2>

This repository contains the backend server for TelMedSphere, a telemedicine platform designed to connect doctors and patients virtually. The backend provides RESTful API endpoints to support all the functionality required for the telemedicine application, including authentication, appointment scheduling, payment processing, video consultation management, and medical record handling.

<h2>💡Backend API Features</h2>

🚨 Authentication & User Management:<br>
 - Secure user registration and login system
 - JWT-based authentication
 - Role-based access control (patients, doctors, admins)
 - User profile management and verification

🚨 Appointment Management:<br>
 - Scheduling system for consultation bookings
 - Availability management for doctors
 - Notification system for upcoming appointments
 - Queue management for virtual consultations

🚨 Payment Processing:<br>
 - Secure payment processing with Stripe integration
 - Digital wallet functionality 
 - Payment history and reporting
 - Invoice generation

🚨 Medical Records:<br>
 - Electronic prescription generation
 - Medical history storage and retrieval
 - PDF report analysis using AI
 - Secure file uploads and storage using Cloudinary

🚨 Communication Services:<br>
 - Email notifications via Flask-Mail
 - SMS alerts through Twilio integration
 - Template-based communication

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>🚀Technology Stack</h2>

<p>
  <a href="https://www.w3schools.com/python/"> <img src="https://img.icons8.com/?size=64&id=13441&format=png" alt="Python" /></a>
  <a href="https://www.geeksforgeeks.org/flask-tutorial/"><img src="https://img.icons8.com/?size=64&id=ewGOClUtmFX4&format=png" alt="Flask" /></a>
  <a href="https://www.w3schools.com/mongodb/"> <img src="https://img.icons8.com/?size=64&id=74402&format=png" alt="Mongo" /></a>
  <a href="https://www.educative.io/blog/docker-compose-tutorial" ><img src="https://img.icons8.com/?size=64&id=22813&format=png&color=000000" alt="Docker"></a>
  <a href="https://swagger.io/" ><img src="https://img.icons8.com/?size=64&id=rdKV2dee9wxd&format=png&color=000000" alt="Swagger"></a>
  <a href="https://jwt.io/"><img src="https://jwt.io/img/pic_logo.svg" height="64" width="64" alt="JWT"/></a>
  <a href="https://stripe.com/"><img src="https://cdn.worldvectorlogo.com/logos/stripe-4.svg" height="64" width="64" alt="Stripe"/></a>
  <a href="https://www.twilio.com/"><img src="https://www.vectorlogo.zone/logos/twilio/twilio-icon.svg" height="64" width="64" alt="Twilio"/></a>
</p>

🚨 Core: Python 3.10, Flask <br>
🚨 Database: MongoDB Atlas <br>
🚨 Authentication: Firebase Admin, JWT <br>
🚨 Payment Processing: Stripe <br>
🚨 File Storage: Cloudinary <br>
🚨 Messaging: Twilio, Flask-Mail <br>
🚨 AI Integration: Google Generative AI <br>
🚨 PDF Processing: PyMuPDF <br>
🚨 Security: Flask-Bcrypt <br>
🚨 API Documentation: Swagger, Flasgger <br>
🚨 Containerization: Docker <br>
🚨 Deployment: Vercel <br>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>🏗️Backend Architecture</h2>

The TelMedSphere backend follows a RESTful API architecture built with Flask. Here's a high-level overview:

```
TelMedSphere Backend
│
├── API Routes - Organized by functionality
│   ├── Authentication (register, login, profile)
│   ├── Appointments (scheduling, management)
│   ├── Payments (processing, wallet)
│   ├── Medical Records (prescriptions, history)
│   └── Communications (email, SMS)
│
├── Services
│   ├── Cloudinary - Image and file storage
│   ├── Stripe - Payment processing
│   ├── Firebase - Authentication
│   ├── Twilio - SMS notifications
│   └── Google Generative AI - Medical report analysis
│
├── Database (MongoDB)
│   ├── Users (patients, doctors)
│   ├── Appointments
│   ├── Medical Records
│   ├── Payments
│   └── Feedback
│
└── Utils
    ├── PDF Processing
    ├── Image Handling
    └── Email Templates
```

<h3 align="right"><a href="#top">⬆️</a></h3>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->
<h2>💥Getting Started</h2>

- Fork this Repository.
- Clone the forked repository in your local system.
  
```bash
git clone https://github.com/TelMedSphere/backend.git
```

<h2>💻Backend Setup</h2>

```bash
# Navigate to backend directory
cd TelMedSphere/backend

# Set up environment variables
cp .env.example .env
# Edit the .env file with your credentials (MongoDB, Stripe, Firebase, etc.)

# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# For Windows
venv\Scripts\activate
# For Linux/Mac
source venv/bin/activate

# Install all dependencies
pip install -r requirements.txt

# Run the Flask server
flask run

# Access the server at http://localhost:5000
# Access API documentation at http://localhost:5000/api/docs

# Deactivate the virtual environment when done
deactivate
```
<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>📊Environment Variables</h2>

The backend requires several environment variables to be set up. Create a `.env` file in the backend directory with the following variables:

```
# MongoDB URL
DBURL=your-mongodb_url

# NodeMailer
HOST_EMAIL=your_host_email
PASSWORD=your_app_password
PORT=587

# Stripe
STRIPE_SECRET_KEY=your_stripe_secret_key

# Backend server after deployment
DOMAIN=your_domain

# JWT Secret for encryption
SECRET=your_secret_key

# WhatsApp Notification
TWILIO_WHATSAPP_ACCOUNT_SID="ACXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
TWILIO_WHATSAPP_AUTH_TOKEN="your_auth_token"
TWILIO_WHATSAPP_FROM="whatsapp:+1234567890"

# Firebase Authentication Keys
FIREBASE_TYPE=service_account
FIREBASE_PROJECT_ID=your-project-id
FIREBASE_PRIVATE_KEY_ID=your-private-key-id
FIREBASE_PRIVATE_KEY=-----BEGIN PRIVATE KEY-----\\nyour-private-key\\n-----END PRIVATE KEY-----\\n
FIREBASE_CLIENT_EMAIL=firebase-adminsdk-xxxxx@your-project-id.iam.gserviceaccount.com
FIREBASE_CLIENT_ID=your-client-id
FIREBASE_AUTH_URI=https://accounts.google.com/o/oauth2/auth
FIREBASE_TOKEN_URI=https://oauth2.googleapis.com/token
FIREBASE_AUTH_PROVIDER_CERT_URL=https://www.googleapis.com/oauth2/v1/certs
FIREBASE_CLIENT_CERT_URL=https://www.googleapis.com/robot/v1/metadata/x509/firebase-adminsdk-xxxxx%40your-project-id.iam.gserviceaccount.com
FIREBASE_UNIVERSE_DOMAIN=googleapis.com

# Cloudinary Authentication Keys
CLOUDINARY_CLOUD_NAME="your-cloud-name"
CLOUDINARY_API_KEY="your-api-key"
CLOUDINARY_API_SECRET="your-api-secret"

# Gemini Authentication
GEMINI_API_KEY="your-api-key"
```

For detailed setup instructions, refer to the complete [Environment Variables Setup Guide](.github/EnvVarSetUpGuideline.md).

<h3 align="right"><a href="#top">⬆️</a></h3>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->
<h2>🐳Docker Setup</h2>

The backend can be easily deployed using Docker.

### Prerequisites
- Docker [installed](https://www.docker.com/products/docker-desktop/) on your system
- Environment variables ready for configuration

### Steps to Run Backend with Docker

1. Clone the repository:
```bash
git clone https://github.com/TelMedSphere/backend.git
cd TelMedSphere/backend
```

2. Set up environment variables:
```bash
cp .env.example .env
# Edit the .env file with your credentials
```

3. Build and run the Docker container:
```bash
docker build -t telmedsphere-backend .
docker run -p 5000:5000 --env-file .env telmedsphere-backend
```

The backend API will be available at http://localhost:5000.

### Stopping the Container
```bash
docker stop <container_id>
# Or with docker-compose
docker-compose down
```

<h3 align="right"><a href="#top">⬆️</a></h3>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>📑API Documentation</h2>

The backend API is documented using [Swagger](https://swagger.io/) following the OpenAPI Specification.

### API Documentation URLs:

```
# Local Development
http://localhost:5000/api/docs

# Production
https://telmedsphere-server.vercel.app/api/docs
```

### Key API Endpoints:

```
# Authentication
POST /api/auth/register - Register a new user
POST /api/auth/login - Authenticate a user
GET /api/auth/profile - Get user profile

# Appointments
GET /api/appointments - List user appointments
POST /api/appointments - Create a new appointment
PUT /api/appointments/:id - Update appointment details

# Payments
POST /api/payments/create-payment-intent - Create payment intent
GET /api/payments/history - Get payment history

# Medical Records
POST /api/prescriptions - Create a prescription
GET /api/prescriptions/patient/:id - Get patient prescriptions
POST /api/reports/analyze - Analyze medical reports using AI

# Admin
GET /api/admin/users - List all users (admin only)
PUT /api/admin/users/:id - Update user status (admin only)
```

<h3 align="right"><a href="#top">⬆️</a></h3>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>⚡Project Admin and Collaborators</h2>

<table>
<tr>
<td align="center">
<a href="https://github.com/PratikMane0112"><img src="https://avatars.githubusercontent.com/u/153143167?v=4" height="140px" width="140px" alt="Pratik Mane"></a><br><sub><b>Pratik Mane <br> (Project Admin)</b></sub>
</td>
<td align="center">
<a href="https://github.com/HarshwardhanPatil07"><img src="https://avatars.githubusercontent.com/u/126240589?v=4" height="140px" width="140px" alt="Pratik Mane"></a><br><sub><b>Harshwardhan Patil <br> (KWoC Mentor) </b></sub>
</td>
<td align="center">
<a href="https://github.com/AdityaBavadekar"><img src="https://avatars.githubusercontent.com/u/64344960?v=4" height="140px" width="140px" alt="Pratik Mane"></a><br><sub><b>Aditya Bavadekar <br> (SWoC Mentor)</b></sub>
</td>
<td align="center">
<a href="https://github.com/RajKhanke"><img src="https://avatars.githubusercontent.com/u/137288727?v=4" height="140px" width="140px" alt="Raj Khanke"></a><br><sub><b>Raj Khanke <br> (DWoC Mentor) </b></sub>
</td>

</tr>
</table>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>💬Contributing</h2>

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)

We welcome contributions to the backend of TelMedSphere. If you're interested in contributing:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature-name`)
3. Make your changes
4. Run tests to ensure functionality
5. Commit your changes (`git commit -m 'Add some feature'`)
6. Push to the branch (`git push origin feature/your-feature-name`)
7. Open a Pull Request

Read our [Contributing Guidelines](https://github.com/PratikMane0112/TelMedSphere/blob/master/.github/CONTRIBUTING_GUIDELINES.md) for more details.

<h2><a href="https://discord.gg/qsdDRKak28">Join Discord Server↗️</a></h2>

<h3 align="right"><a href="#top">⬆️</a></h3>

<!-- ---------------------------------------------------------------------------------------------------------------------------------------------------------   -->
<h2>🧾License</h2>

This project is licensed under the Apache License 2.0. See the [LICENSE](https://github.com/PratikMane0112/TelMedSphere/blob/master/LICENSE) file for more details.
  
```
 Copyright 2025 Pratik Mane

 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
```

