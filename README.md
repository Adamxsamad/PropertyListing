# Property Management System

## Description
This Node.js application provides a backend system for managing real estate properties, allowing users to list, update, and delete properties, as well as manage images and user authentication.

## Technologies Used
- Node.js
- Express
- MySQL
- JWT for authentication
- bcrypt for password hashing
- multer for image handling
- dotenv for environment variable management

## Features
- User authentication (registration and login)
- Property listing, updating, and deletion
- Image upload and management for properties
- Property search with filters (location, price range, type, etc.)
- Administrative controls for property management

## Installation and Setup
-Clone the repository and navigate to the project directory:
bash
git clone (https://github.com/Adamxsamad/PropertyListing)
cd property-management-system

-Create a `.env` file in the root directory and configure the required environment variables:
DB_HOST=localhost
DB_USER=root
DB_PASS=root
JWT_SECRET_KEY=your_secret_key

-Install dependencies and start the server:
npm install
npm install -g nodemon
nodemon app

Use `nodemon` for development to automatically restart the server on code changes.

## API Endpoints and Usage

### User Authentication
- `POST /api/auth/register`: Register a new user
- `POST /api/auth/login`: Log in a user

### Property Management
- `GET /properties`: Retrieve all properties
- `POST /properties`: Add a new property
- `PUT /properties/:id`: Update an existing property
- `DELETE /properties/:id`: Delete a property

### Image Management
- `POST /properties/:id/images`: Upload images for a property
- `GET /properties/:id/images`: Retrieve all images for a property
- `DELETE /properties/:propertyId/images/:imageId`: Delete a specific image of a property

## Database Schema Description
The database includes tables for users, properties, and property images. Key attributes include:
- **Users**: `user_id`, `username`, `password`, `email`
- **Properties**: `property_id`, `title`, `location`, `price`, `description`, `user_id`
- **Property Images**: `image_id`, `property_id`, `image_url`

## Testing
To test the application, use Postman or any other API testing tool to make requests to the available endpoints.

## Contributing
Contributions are welcome. Please fork the repository and submit a pull request with your changes.

## Contact
For support, email adamsamad1469@gmail.com or create an issue in the GitHub repository.
