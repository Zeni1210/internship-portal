# GetInt - Internship Management Platform

GetInt is a web application designed to connect students with internship opportunities and help companies manage their internship programs.

## Description

This project is a full-stack MERN (MongoDB, Express, React, Node.js) application. It provides a platform for:

*   **Students:** To register, log in, view available internships, and apply for them by uploading their resumes.
*   **Companies:** To register, log in, post new internship opportunities, and view applications received for their postings.

The application uses JWT for authentication and Cloudinary for resume storage.

## Project Structure

The project is organized into two main directories within the `GetInt-main` folder:

*   `GetInt-main/client/`: Contains the React frontend application.
*   `GetInt-main/server/`: Contains the Node.js/Express backend application, including API endpoints and database models.

## Getting Started

### Prerequisites

*   Node.js and npm (or yarn)
*   MongoDB (local instance or a cloud-hosted solution like MongoDB Atlas)
*   A Cloudinary account (for resume uploads)

### Server Setup

1.  **Navigate to the server directory:**
    ```bash
    cd GetInt-main/server
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    # or
    # yarn install
    ```
3.  **Create a `.env` file** in the `GetInt-main/server` directory and add the following environment variables:
    ```env
    MONGODB_URL=<your_mongodb_connection_string>
    ACCESS_TOKEN_SECRET=<your_jwt_secret_key>
    CLOUDNAME=<your_cloudinary_cloud_name>
    APIKEY=<your_cloudinary_api_key>
    APISECRET=<your_cloudinary_api_secret>
    ```
4.  **Start the server:**
    ```bash
    npm start
    # or (for development with nodemon)
    # npm run devStart
    ```
    The server will typically run on `http://localhost:3001`.

### Client Setup

1.  **Navigate to the client directory:**
    ```bash
    cd GetInt-main/client
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    # or
    # yarn install
    ```
3.  **Start the client development server:**
    ```bash
    npm start
    # or
    # yarn start
    ```
    The client application will typically run on `http://localhost:3000` and will proxy API requests to the backend server.

## Usage

Once both the client and server are running:

1.  **Open your web browser** and navigate to `http://localhost:3000`.
2.  **Register** as a student or a company.
3.  **Log in** with your credentials.
4.  **Students:**
    *   Browse available internships.
    *   Apply for internships by providing necessary details and uploading a resume.
5.  **Companies:**
    *   Post new internship openings.
    *   View applications submitted for their internships.

## API Endpoints

The server exposes the following main API endpoints (managed in `GetInt-main/server/index.js`):

*   `POST /register`: Student registration.
*   `POST /registerCompany`: Company registration.
*   `POST /login`: Student login.
*   `POST /loginCompany`: Company login.
*   `POST /insert`: Add a new internship (company authenticated).
*   `POST /apply`: Submit an application for an internship (student authenticated, includes resume upload).
*   `GET /read`: View all internships (student authenticated).
*   `GET /readApplications`: View applications for company's internships (company authenticated).

## Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-feature-name`).
3.  Make your changes.
4.  Commit your changes (`git commit -am 'Add some feature'`).
5.  Push to the branch (`git push origin feature/your-feature-name`).
6.  Create a new Pull Request.

## License

This project is currently unlicensed. Please specify a license if you intend to distribute or share this code.
