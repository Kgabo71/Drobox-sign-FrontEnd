Document Signing Frontend

This is the frontend for a document signing application built with Next.js. It allows users to initiate a signing process by entering their email address and displays the embedded signing experience using Dropbox Sign.

Features

User-friendly interface for initiating document signing.

Real-time embedded signing experience using an iframe.

Framer Motion animations for smooth user interactions.

Prerequisites

Before running the project, ensure the following:

Node.js: Install the latest version from Node.js.

Backend: Ensure the backend service is running and accessible. It should handle requests to create a document instance and return an embedded signing URL.

Installation

Clone the repository:

git clone https://github.com/Kgabo71/Drobox-sign-FrontEnd
cd Drobox-sign-FrontEnd 

Install dependencies:

npm install

Create a .env.local file in the project root and set the backend URL:

NEXT_PUBLIC_BACKEND_URL=http://localhost:4000

Usage

Start the development server:

npm run dev

Open the application in your browser at http://localhost:3000.

Enter your email address and initiate the signing process. If the backend is configured correctly, the embedded signing experience will load.

Project Structure

|-- components/         # Reusable UI components
|-- pages/              # Next.js pages
|-- public/             # Static assets
|-- styles/             # Global and component-specific styles
|-- package.json        # Project dependencies and scripts

Technologies Used

Next.js: Framework for building React applications.

Framer Motion: For animations.

Axios: To make HTTP requests to the backend.

Tailwind CSS: For styling.

API Integration

The frontend communicates with the backend through the following endpoint:

POST /documents/create: Sends the user's email and a template ID to the backend to generate a signing URL. The backend must return the embed_url to display in the iframe.

Environment Variables

Make sure to configure the following environment variable in the .env.local file:

NEXT_PUBLIC_BACKEND_URL: The base URL for the backend API.



NEXT_PUBLIC_BACKEND_URL=http://localhost:4000

Troubleshooting

CORS Issues:

Ensure the backend has CORS enabled for the frontend's origin.

Signing URL Not Displaying:

Check if the backend is returning the correct embed_url.

Backend Not Responding:

Verify the backend service is running on the correct port and accessible from the frontend.

Deployment

To deploy the application:

Build the project:

npm run build

Start the production server:

npm start

Or deploy to platforms like Vercel, Netlify, or AWS Amplify for better scalability.

License

This project is licensed under the MIT License. See the LICENSE file for details.

