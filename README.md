# E-commerce API

A simple e-commerce API built with Node.js, Express, and MongoDB.

## Features

- User authentication (register, login, profile)
- Product management (CRUD operations)
- Product reviews
- Role-based access control (admin/user)

## API Endpoints

### Public Endpoints
- GET `/api/products` - Get all products
- GET `/api/products/:id` - Get a single product

### User Endpoints (Authentication Required)
- POST `/api/users/register` - Register a new user
- POST `/api/users/login` - Login user
- GET `/api/users/profile` - Get user profile
- POST `/api/products/review` - Create/Update a product review

### Admin Endpoints (Admin Role Required)
- POST `/api/products` - Create a new product
- PUT `/api/products/:id` - Update a product
- DELETE `/api/products/:id` - Delete a product

## Deployment Instructions

### Deploy to Heroku

1. Create a Heroku account at [heroku.com](https://heroku.com)
2. Install the Heroku CLI
3. Login to Heroku: `heroku login`
4. Create a new Heroku app: `heroku create your-app-name`
5. Set up environment variables:
   ```
   heroku config:set MONGODB_URI=your_mongodb_uri
   heroku config:set JWT_SECRET=your_jwt_secret
   heroku config:set NODE_ENV=production
   ```
6. Deploy to Heroku: `git push heroku main`

### Deploy to Render

1. Create a Render account at [render.com](https://render.com)
2. Connect your GitHub repository
3. Create a new Web Service
4. Set up environment variables:
   - `MONGODB_URI`
   - `JWT_SECRET`
   - `NODE_ENV`
5. Deploy

### Deploy to Railway

1. Create a Railway account at [railway.app](https://railway.app)
2. Connect your GitHub repository
3. Set up environment variables
4. Deploy

## Local Development

1. Clone the repository
2. Install dependencies: `npm install`
3. Create a `.env` file with the required environment variables
4. Start the development server: `npm run dev`

## License

MIT 