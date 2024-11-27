# Food-App

Food-App is a full-stack TypeScript-based web application that allows users to browse, order, and manage food-related services. The project is split into two main parts:

- **Frontend**: A React-based application that handles the user interface and interaction.
- **Backend**: A Node.js application that handles the server-side logic, including data storage, authentication, and API requests.

## Features

### Frontend
- User-friendly interface to browse food categories, menu items, and restaurants.
- **Search functionality**: Users can search for restaurants based on their location or food preferences.
- **Restaurant exploration**: Users can explore restaurants by checking their menus, ratings, and details.
- **Order placement**: Users can select and order their favorite meals directly from restaurants.
- **Stripe Integration**: Secure payment gateway to handle orders and process payments online.
- Ability to create an account, log in, and manage user information.
- Responsive design using **Tailwind CSS** for a smooth mobile and desktop experience.

### Backend
- **REST API**: Handles requests from the frontend to fetch food, restaurant, and user data.
- **Authentication**: Secure login system using **JWT** (JSON Web Tokens) for user authentication and session management.
- **Database interaction**: MongoDB is used to store user profiles, order details, restaurant data, and menu items.
- **Routes management**: Backend routes manage food items, restaurant details, and user profiles.

## Technologies Used

### Frontend
- **React**: A JavaScript library for building user interfaces.
- **TypeScript**: A strongly-typed superset of JavaScript that improves code quality and maintainability.
- **Zod**: A TypeScript-first schema declaration and validation library for validating data, ensuring type safety in forms and API responses.
- **Zustand**: A minimalistic state management library for React to manage global app state.
- **Tailwind CSS**: A utility-first CSS framework for styling the frontend and making it responsive.

### Backend
- **Node.js**: A JavaScript runtime built on Chrome's V8 engine for building fast and scalable server-side applications.
- **Express.js**: A lightweight web application framework for Node.js to build RESTful APIs.
- **MongoDB**: A NoSQL database for storing user profiles, orders, and restaurant/menu data.
- **JWT (JSON Web Tokens)**: For secure user authentication, ensuring safe communication between client and server.
- **Stripe**: For handling secure payments when users place orders.
- **Cloudinary**: For storing and fetching images (e.g., restaurant logos, food images).

## Features in Detail

### Frontend Features:
- **Restaurant Search**:
    - Users can search for restaurants based on the place or type of food they are interested in. The frontend fetches matching restaurants and displays relevant results.
    - Example search options include "Indian cuisine in New York" or "Pizza places near me."

- **Restaurant Exploration**:
    - After searching, users can view detailed information about the restaurant, including:
        - Menu items
        - User ratings and reviews
        - Address and contact information
    - Users can add their preferred dishes to the cart directly from the restaurant page.

- **Order Placement**:
    - Users can select their favorite meals and add them to the cart.
    - After selecting items, users can proceed to checkout, where they can securely pay using **Stripe**.

### Backend Features:
- **User Authentication**:
    - JWT is used to authenticate users securely.
    - When a user logs in, a token is generated and sent back to the client to authorize further requests.

- **Stripe Integration**:
    - The backend handles payment requests through **Stripe**.
    - Orders placed by users are processed using Stripe's secure API, ensuring proper transactions and payment confirmations.

## Setup Instructions

### Clone the Repository

Clone the repository to your local machine:


git clone https://github.com/Grgnavin/Food-App.git

### For Frontend:

1. Navigate to the `client` directory:
    ```bash
    cd client
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Run the project:
    ```bash
    npm run dev
    `

### For Backend:

1. Navigate to the `server` directory:
    ```bash
    cd server
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Run the project:
    ```bash
    npm run dev
    ``

### Environment Variables

Make sure to create `.env` files for both the client and server with the necessary configuration:

#### Example `.env` for Backend:

```makefile
PORT=5000
DB_URI=your_mongo_database_uri
JWT_SECRET=your_jwt_secret_key
STRIPE_SECRET_KEY=your_stripe_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

The backend will be available at `http://localhost:8000`, and the frontend will be available at `http://localhost:5173`.

## Deployment

You can deploy both the frontend and backend to platforms like **Heroku**, **Netlify**, or **Vercel**. Make sure to update the environment variables for production and configure your Stripe and Cloudinary keys accordingly.

## Contributing

Feel free to fork the repository, create issues, or submit pull requests to contribute to the project.

### Steps for Contributing:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push the branch to your forked repository (`git push origin feature-branch`).
5. Create a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
