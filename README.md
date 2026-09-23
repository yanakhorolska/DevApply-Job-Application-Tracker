DevApply

DevApply is a full-stack job application tracker designed to help users organize and manage the entire job search process in one place.

It provides a clear overview of applications, interview stages, deadlines, contacts, and application history without relying on spreadsheets, notes, or multiple browser tabs.

Features
Job Application Management

Users can:

add new job applications
edit application details
delete applications
view all applications
search applications
filter applications
sort applications
update application status

Each application includes information such as:

company name
position
job offer URL
location
work model
salary range
technologies
application date
current status
notes
Application Status Tracking

Applications can be tracked through different recruitment stages:

Wishlist
   ↓
Applied
   ↓
Recruiter Contact
   ↓
Interview
   ↓
Technical Interview
   ↓
Final Interview
   ↓
Offer

Applications can also be marked as:

Rejected
Withdrawn
No Response
Application History

Each application contains a timeline showing how the recruitment process has progressed.

Example:

12 Sep
Application submitted

15 Sep
Recruiter contact

18 Sep
Interview

23 Sep
Technical interview

27 Sep
Final interview

This makes it possible to see the complete history of an application instead of only its current status.

Dashboard

The dashboard provides an overview of the current job search.

It includes statistics such as:

total applications
active applications
applications sent recently
interviews
offers
rejected applications
applications by status
response rate
Interviews

Interview information can be stored directly inside an application.

Interview details include:

interview type
date
recruitment stage
interviewer
notes
technical topics
follow-up date
Search, Filtering and Sorting

Applications can be searched and filtered by:

company
position
application status
work model
technologies

Applications can also be sorted by relevant fields such as application date.

Tech Stack
Frontend
React
TypeScript
React Router
Axios
Backend
Node.js
Express.js
TypeScript
REST API
Database
PostgreSQL
Prisma ORM
Validation
Joi
Testing
Jest
Supertest
React Testing Library
Architecture

DevApply follows a client-server architecture.

React + TypeScript
        ↓
      REST API
        ↓
Node.js + Express
        ↓
   Business Logic
        ↓
    Prisma ORM
        ↓
    PostgreSQL

The frontend communicates with the backend through a REST API. The backend is responsible for application logic, validation, data processing, and communication with the database.

API
Applications
GET    /api/applications
GET    /api/applications/:id
POST   /api/applications
PATCH  /api/applications/:id
DELETE /api/applications/:id
Interviews
GET    /api/applications/:id/interviews
POST   /api/applications/:id/interviews
PATCH  /api/interviews/:id
DELETE /api/interviews/:id
Filtering

Example:

GET /api/applications?status=applied
GET /api/applications?workModel=remote
GET /api/applications?technology=react
Authentication

DevApply supports user authentication and private user accounts.

Each user has access only to their own job applications and recruitment data.

Authentication includes:

registration
login
protected routes
authenticated API requests
user-specific application data
Application Structure

A job application contains information similar to:

Application
├── Position
├── Company
├── Job URL
├── Location
├── Work Model
├── Salary
├── Technologies
├── Status
├── Application Date
├── Notes
├── Interviews
└── Application History
Installation

Clone the repository:

git clone <repository-url>

Install dependencies:

npm install

Create the required environment variables:

DATABASE_URL=your_database_url
JWT_SECRET=your_jwt_secret
PORT=3000

Run the application:

npm run dev

Testing

Run tests with:

npm test

Author

Yana Khorolska

Full-stack developer focused on JavaScript, TypeScript, React, and Node.js.
