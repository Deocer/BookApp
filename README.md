# Book Management App

## Overview

This is a Vue.js application for managing a list of books. It allows users to view, search, sort, create, edit, and delete book entries. The app uses Firebase for backend services and supports image uploads for book covers.

## Features

- **Search and Sort**: Filter books by title or author and sort by published date or genre.
- **Create Book**: Add new books with title, genre, and cover image.
- **Edit Book**: Update book details and cover image.
- **Delete Book**: Remove books from the list.

## Technologies Used

- **Vue.js**: JavaScript framework for building user interfaces.
- **Firebase**: Backend service for handling database operations and file storage.
- **Axios**: HTTP client for making API requests.

## Getting Started

### Prerequisites

- Node.js and npm (Node Package Manager) installed on your machine.
- Firebase project set up with Firestore and Storage services.

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/your-repository-name.git
    ```

2. **Navigate to the project directory:**

    ```bash
    cd your-repository-name
    ```

3. **Install dependencies:**

    ```bash
    npm install
    ```

4. **Configure Firebase:**

    - Create a Firebase project if you haven't already.
    - Obtain your Firebase configuration details.
    - Replace the placeholder Firebase configuration in `src/firebase.js` with your own configuration:

      ```javascript
      import { initializeApp } from 'firebase/app';
      import { getFirestore } from 'firebase/firestore';
      import { getStorage } from 'firebase/storage';

      const firebaseConfig = {
        apiKey: 'YOUR_API_KEY',
        authDomain: 'YOUR_PROJECT_ID.firebaseapp.com',
        projectId: 'YOUR_PROJECT_ID',
        storageBucket: 'YOUR_PROJECT_ID.appspot.com',
        messagingSenderId: 'YOUR_MESSAGING_SENDER_ID',
        appId: 'YOUR_APP_ID'
      };

      const app = initializeApp(firebaseConfig);
      export const db = getFirestore(app);
      export const storage = getStorage(app);
      ```

### Running the App

1. **Start the development server:**

    ```bash
    npm run serve
    ```

2. **Open the app in your browser:**

    Navigate to `http://localhost:8080` to view the application.

### Usage

- **Search and Sort**: Use the search input to filter books and the dropdown to sort them.
- **Create Book**: Click on the "Create Book" button to open the form and add a new book.
- **Edit Book**: Click the "Edit" button on a book item to modify its details.
- **Delete Book**: Click the "Delete" button to remove a book from the list.
