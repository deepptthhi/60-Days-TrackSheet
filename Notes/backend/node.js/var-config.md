# Environment Variables & Configuration

## Introduction

As backend applications grow, they need various configuration values such as database connection strings, API keys, JWT secrets, email credentials, cloud storage keys, and server ports. Hardcoding these values directly into the source code is not recommended because it exposes sensitive information and makes the application difficult to maintain.

Environment variables provide a secure and flexible way to store configuration outside the application code. This allows the same application to run in different environments such as development, testing, and production without modifying the source code.

Today, instead of focusing on writing backend logic, I learned how professional applications manage configuration securely and efficiently.

## Why Do We Need Environment Variables?

Consider a Node.js application connected to MongoDB.

A beginner might write:

```javascript
const DB_URL = "mongodb+srv://username:password@cluster.mongodb.net/myDatabase";
```

Although this works, it has several problems:

- Passwords become visible in the source code.
- Accidentally pushing the project to GitHub exposes credentials.
- Switching between development and production databases requires editing the code.
- Multiple developers cannot easily use different configurations.

Environment variables solve these problems by separating configuration from application logic.

## What are Environment Variables?

Environment variables are values stored outside the application's source code that can be accessed while the program is running.

Instead of writing sensitive information inside JavaScript files, developers store them in the operating system or in a `.env` file.

Common examples include:

- Server Port
- MongoDB Connection String
- JWT Secret
- API Keys
- SMTP Credentials
- Cloudinary Keys
- AWS Credentials

These variables are accessed using Node.js through:

```javascript
process.env
```

## The .env File

During development, environment variables are usually stored inside a `.env` file.

Example:

```env
PORT=5000

MONGO_URI=mongodb://localhost:27017/shopDB

JWT_SECRET=mySuperSecretKey

EMAIL_USER=example@gmail.com

EMAIL_PASSWORD=myPassword

CLOUDINARY_API_KEY=123456
```

Each variable follows the format:

```text
KEY=VALUE
```

The `.env` file keeps sensitive information separate from application code.

## Installing dotenv

Node.js cannot automatically read `.env` files.

The **dotenv** package loads these variables into the application.

Installation:

```bash
npm install dotenv
```

## Configuring dotenv

Import dotenv before using any environment variables.

```javascript
require("dotenv").config();
```

This loads every variable from the `.env` file into `process.env`.

## Accessing Environment Variables

Example:

```javascript
const PORT = process.env.PORT;

const DB_URL = process.env.MONGO_URI;

const SECRET = process.env.JWT_SECRET;
```

These values are available throughout the application after dotenv is configured.

## Understanding process.env

`process.env` is a built-in Node.js object that stores all available environment variables.

Example:

```javascript
console.log(process.env.PORT);
```

Output:

```text
5000
```

If a variable does not exist:

```javascript
console.log(process.env.API_KEY);
```

Output:

```text
undefined
```

Therefore, developers often provide default values.

## Default Values

A default value ensures the application continues running even if an environment variable is missing.

Example:

```javascript
const PORT = process.env.PORT || 3000;
```

If `PORT` exists, it is used.

Otherwise:

```
3000
```

is used automatically.

## Common Environment Variables

A typical backend application contains variables like:

```env
PORT=5000

NODE_ENV=development

MONGO_URI=...

JWT_SECRET=...

EMAIL_USER=...

EMAIL_PASSWORD=...

API_KEY=...

REDIS_URL=...
```

Keeping configuration centralized makes applications easier to maintain.

## Different Application Environments

Applications usually have multiple environments.

### Development

Used while building the application.

```env
NODE_ENV=development
```

Characteristics:

- Local database
- Debugging enabled
- Frequent code changes

### Testing

Used during automated testing.

```env
NODE_ENV=test
```

Characteristics:

- Separate test database
- Temporary data
- Automated execution

### Production

Used after deployment.

```env
NODE_ENV=production
```

Characteristics:

- Real users
- Production database
- Optimized performance
- Debug logs disabled

The application code remains unchanged.

Only environment variables change.

## Why Should Secrets Never Be Hardcoded?

Consider this code:

```javascript
const JWT_SECRET = "mysecret123";
```

Problems:

- Anyone with repository access can view the secret.
- Changing the secret requires modifying source code.
- Production and development cannot use different secrets.

Instead:

```javascript
const JWT_SECRET = process.env.JWT_SECRET;
```

Now the secret exists only on the server.

## The .gitignore File

The `.env` file should never be uploaded to GitHub.

Example:

```text
node_modules/

.env
```

This prevents accidental exposure of credentials.

## Configuration Folder

Large applications usually create a dedicated configuration folder.

Example:

```text
config/

database.js

jwt.js

mail.js

cloudinary.js
```

Instead of accessing `process.env` throughout the project, configuration files centralize all settings.

Example:

```javascript
module.exports = {

    port: process.env.PORT,

    mongoUri: process.env.MONGO_URI,

    jwtSecret: process.env.JWT_SECRET

};
```

Benefits:

- Cleaner code
- Easier maintenance
- Better organization

## Real-World Example

Consider an e-commerce website.

During development:

```
Database → Local MongoDB
```

After deployment:

```
Database → MongoDB Atlas
```

The backend code remains exactly the same.

Only this changes:

```env
MONGO_URI=...
```

This allows developers to move between environments without modifying application logic.

## Best Practices

- Never hardcode passwords or API keys.
- Always use a `.env` file during development.
- Add `.env` to `.gitignore`.
- Keep configuration separate from business logic.
- Use meaningful variable names.
- Provide default values whenever appropriate.
- Store production secrets securely.
- Validate important environment variables during application startup.

## Common Mistakes

- Uploading `.env` to GitHub.
- Hardcoding credentials.
- Forgetting to configure dotenv.
- Using inconsistent environment variable names.
- Depending on undefined variables.
- Storing configuration throughout the application.

## Interview Questions

### Why do we use environment variables?

Environment variables separate configuration from application logic, making applications more secure, portable, and easier to deploy.

### What is dotenv?

`dotenv` is a Node.js package that loads environment variables from a `.env` file into `process.env`.

### Why shouldn't the `.env` file be pushed to GitHub?

Because it usually contains sensitive information such as passwords, API keys, JWT secrets, and database credentials.

### What is process.env?

`process.env` is a built-in Node.js object that stores all environment variables available to the running application.

### What is NODE_ENV?

`NODE_ENV` specifies the current application environment, such as development, testing, or production. Developers often use it to enable or disable features depending on the environment.

### Why are configuration files useful?

Configuration files centralize application settings, making the project easier to organize and maintain.

## Summary

Environment variables are one of the most important concepts in backend development because they separate sensitive configuration from application code. Using `.env` files, `dotenv`, and `process.env` allows applications to remain secure, flexible, and portable across different environments. Proper configuration management is considered a standard practice in production-ready software development because it improves security, simplifies deployment, and keeps backend projects well organized.