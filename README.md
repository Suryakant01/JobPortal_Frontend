
# Job Application Tracker - Frontend

This is the frontend for a full-stack Job Application Tracker built with React and Vite. It provides a clean, responsive, and feature-rich user interface for users to manage their job applications and for administrators to oversee the platform.

[![React](https://img.shields.io/badge/React-19-blue?logo=react)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Vite-^6.3.5-blueviolet?logo=vite)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-^3.4-blue?logo=tailwindcss)](https://tailwindcss.com/)
[![React Router](https://img.shields.io/badge/React_Router-v7-red?logo=reactrouter)](https://reactrouter.com/)

---

## Features

### User-Facing Features
- **Authentication**: Secure user registration and login system using JWT (JSON Web Tokens).
- **Dashboard**: A central hub to view, filter, and sort all personal job applications.
- **CRUD Operations**: Users can **C**reate, **R**ead, **U**pdate, and **D**elete their job applications.
- **Job Detail Page**: A dedicated page to view detailed information about a single application, including notes and status history.
- **Filtering & Sorting**: Easily filter applications by status (Applied, Interview, Offer, etc.) and sort by application date.
- **Responsive Design**: A mobile-first design that works beautifully on all screen sizes, from desktops to mobile phones.
- **Toast Notifications**: User-friendly feedback for actions like creating, updating, or deleting jobs.

### Admin-Specific Features
- **Admin Dashboard**: A special view for administrators to see *all* job applications from *all* users on the platform.
- **Role-Based Access Control**: Protected routes ensure that only users with an 'admin' role can access the admin panel.
- **Application Management**: Admins have the authority to delete any job application from the system.

### Technical Features
- **Component-Based Architecture**: Built with reusable React components for maintainability.
- **Centralized API Management**: `axios` instance with interceptors to automatically attach the auth token to every request.
- **Global State Management**: React Context API is used for managing authentication state and user information across the application.
- **Real-time Notifications (Setup)**: A `socket.io-client` is integrated to receive real-time notifications from the backend.
- **Modern Tooling**: Fast development and builds powered by Vite.

## Tech Stack

- **Framework**: [React 19](https://react.dev/)
- **Bundler**: [Vite](https://vitejs.dev/)
- **Routing**: [React Router v7](https://reactrouter.com/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Form Management**: [React Hook Form](https://react-hook-form.com/)
- **HTTP Client**: [Axios](https://axios-http.com/)
- **UI Notifications**: [React Hot Toast](https://react-hot-toast.com/)
- **Icons**: [React Icons](https://react-icons.github.io/react-icons/)
- **Real-time Communication**: [Socket.IO Client](https://socket.io/docs/v4/client-api/)

## Getting Started

Follow these instructions to get the project up and running on your local machine for development and testing purposes.

### Prerequisites

- [Node.js](https://nodejs.org/) (version 18.x or higher is recommended)
- [npm](https://www.npmjs.com/) or any other package manager like [yarn](https://yarnpkg.com/) or [pnpm](https://pnpm.io/).

### Local Setup & Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/JobPortal_Frontend.git
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd JobPortal_Frontend
    ```

3.  **Install the dependencies:**
    ```bash
    npm install
    ```

4.  **Set up environment variables:**

    This project requires a connection to a backend API. Create a `.env` file in the root of the project directory and add the following variable:

    ```
    VITE_API_URL=http://localhost:5000/api
    ```

    > **Note:** Replace `http://localhost:5000/api` with the actual URL of your backend server if it's different. The `socket.io` connection in `src/context/AuthContext.jsx` is hardcoded to `http://localhost:5000`, so ensure your backend server is running there for real-time features to work.

### Running the Application

Once the dependencies are installed and the environment variables are set, you can run the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:5173` (or another port if 5173 is in use).

## Available Scripts

In the project directory, you can run the following scripts:

-   `npm run dev`: Runs the app in development mode with Hot Module Replacement.
-   `npm run build`: Builds the app for production to the `dist` folder.
-   `npm run lint`: Lints the project files using ESLint.
-   `npm run preview`: Serves the production build locally to preview it.

## Project Structure

The project follows a standard React application structure to keep the codebase organized and scalable.

```
/src
├── api/              # Functions for making API calls (auth, jobs)
├── components/       # Reusable React components (Navbar, JobCard, etc.)
├── context/          # React Context providers (AuthContext)
├── hooks/            # Custom hooks (useAuth)
├── pages/            # Page-level components (Dashboard, Login, etc.)
├── App.jsx           # Main application component with routing
├── main.jsx          # Entry point of the React application
└── index.css         # Global styles and Tailwind CSS imports
```
