# Leave Management System

A comprehensive leave management system for educational institutions with role-based access for employees, HODs, and principals.

## Deployment to Hostinger

### Prerequisites

1. Hostinger account with Node.js support
2. MongoDB Atlas account for database hosting
3. Git repository for your project (optional)

### Setup MongoDB Atlas

1. Create a MongoDB Atlas account if you don't have one
2. Create a new cluster
3. Set up network access to allow connections from anywhere (or specific IPs)
4. Create a database user with read/write access
5. Get your MongoDB connection string

### Deployment Steps

#### 1. Prepare Your Project

- Make sure your project is ready for production
- Update the `.env.production` file with your MongoDB Atlas URI and JWT secret
- Build the React client: `npm run build` from the project root

#### 2. Create a New Website in Hostinger

- Log in to your Hostinger account
- Go to "Websites" > "Create Website"
- Choose "Import Website" if you have your code in a Git repository, or "Upload Website" if you're uploading files directly

#### 3. Configure Environment Variables

- In Hostinger's control panel, navigate to your website's settings
- Find the environment variables section
- Add the following variables:
  - `NODE_ENV=production`
  - `PORT=5000`
  - `MONGODB_URI=your_mongodb_atlas_uri`
  - `JWT_SECRET=your_secure_jwt_secret`

#### 4. Set Up Node.js Runtime

- In Hostinger's control panel, select Node.js as your runtime environment
- Set the Node.js version to match your development environment (e.g., 16.x)
- Configure the start command: `npm start`

#### 5. Upload Your Files

If you're not using Git:
- Compress your project folder
- Upload the ZIP file to Hostinger
- Extract the files on the server

If you're using Git:
- Connect your Git repository in Hostinger
- Configure the deployment branch (usually main or master)

#### 6. Start Your Application

- Once your files are uploaded, start your Node.js application from the Hostinger control panel
- Your application should now be accessible at your domain

## Troubleshooting

- Check Hostinger's logs if your application fails to start
- Verify that MongoDB connection is working
- Ensure all environment variables are correctly set
- Check for any missing dependencies in package.json

## Local Development

- Clone the repository
- Install dependencies: `npm run install-deps`
- Start the development server: `npm run dev`
- Start the client: `npm run client`
