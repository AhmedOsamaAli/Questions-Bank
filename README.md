# Question Bank System Backend

This is the backend for the **Question Bank System**, a platform designed to manage subjects, chapters, questions, and student answers. It provides APIs for user authentication, question management, answer submission, and more.

## Features

- **User Authentication**: Register, login, email verification, password reset with OTP.
- **Role-Based Access Control**: Admin and student roles with restricted access to certain endpoints.
- **Subject and Chapter Management**: Create, retrieve, update, and delete subjects and chapters.
- **Question Management**: Add, retrieve, and delete questions with support for multiple types (MCQ, open-ended, etc.).
- **Answer Submission**: Students can submit answers, and the system evaluates correctness.
- **Cloudinary Integration**: Upload and manage images for questions.
- **Email Notifications**: Send emails for verification and password reset using SendGrid.
- **Database Seeding**: Prepopulate the database with sample data for testing.

## Tech Stack

- **Backend Framework**: Node.js with Express.js
- **Database**: MongoDB (Mongoose ODM)
- **Authentication**: JSON Web Tokens (JWT)
- **File Uploads**: Multer with Cloudinary
- **Email Service**: SendGrid
- **AI Integration**: Google Generative AI (Gemini) for evaluating open-ended answers

## create a .env file in the root directory and add the following environment variables:

NODE_ENV=development
PORT=5000
DB_CONNECTION=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
JWT_EXPIRE=30d
JWT_COOKIE_EXPIRE=30
SMTP_HOST=smtp.sendgrid.net
SMTP_PORT=587
SMTP_EMAIL=apikey
SMTP_PASSWORD=<your_sendgrid_api_key>
FROM_EMAIL=<your_verified_email>
GEMINI_API_KEY=<your_gemini_api_key>
CLOUDINARY_CLOUD_NAME=<your_cloudinary_cloud_name>
CLOUDINARY_API_KEY=<your_cloudinary_api_key>
CLOUDINARY_API_SECRET=<your_cloudinary_api_secret>
