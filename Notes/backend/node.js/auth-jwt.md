

## What is Authentication?

Authentication is the process of verifying the identity of a user.

It answers the question:

**"Who are you?"**

Example:

-   Logging into Gmail
-   Logging into Instagram
-   Logging into Amazon

The application checks whether the email and password belong to a valid
user.

## Why Authentication?

Authentication helps:

-   Protect user accounts
-   Prevent unauthorized access
-   Secure private information
-   Identify users before allowing access

## Authentication vs Authorization

  Authentication      Authorization
  ------------------- ------------------------------
  Verifies identity   Verifies permissions
  Happens first       Happens after authentication
  "Who are you?"      "What can you access?"

## What is bcrypt?

bcrypt is a Node.js library used to securely hash passwords before
storing them in the database.

Install:

``` bash
npm install bcrypt
```

## Why Hash Passwords?

Never store passwords as plain text.

Wrong:

``` text
Password: mypassword123
```

Correct:

``` text
Password: $2b$10$Q8w...
```

Hashing makes passwords unreadable.

## Hashing vs Encryption

  Hashing              Encryption
  -------------------- -------------------------
  One-way              Two-way
  Cannot be reversed   Can be decrypted
  Used for passwords   Used for sensitive data

## Hashing Password

``` javascript
const bcrypt = require("bcrypt");

const hashedPassword = await bcrypt.hash(password,10);
```

## Comparing Passwords

``` javascript
const isMatch = await bcrypt.compare(password,user.password);
```

Returns `true` if the passwords match.

## What is JWT?

JWT (JSON Web Token) is a secure token used to identify authenticated
users.

After login, the server generates a token and sends it to the client.

The client sends the token with every future request.

## Why JWT?

-   Stateless authentication
-   Faster than sessions
-   Easy to scale
-   Widely used in REST APIs

## JWT Structure

A JWT contains three parts:

``` text
Header.Payload.Signature
```

### Header

Contains token information.

### Payload

Contains user information.

Example:

``` json
{
  "id":"12345",
  "role":"User"
}
```

### Signature

Ensures the token has not been modified.

## Installing JWT

``` bash
npm install jsonwebtoken
```

## Creating JWT

``` javascript
const jwt = require("jsonwebtoken");

const token = jwt.sign(
    {id:user._id},
    process.env.JWT_SECRET,
    {expiresIn:"1d"}
);
```

## Verifying JWT

``` javascript
const decoded = jwt.verify(
    token,
    process.env.JWT_SECRET
);
```

## Register Flow

``` text
Client
   ↓
Register API
   ↓
Hash Password
   ↓
Save User
   ↓
MongoDB
```

## Login Flow

``` text
Client
   ↓
Login API
   ↓
Find User
   ↓
Compare Password
   ↓
Generate JWT
   ↓
Return Token
```

## Authentication Middleware

``` javascript
const jwt = require("jsonwebtoken");

const auth = (req,res,next)=>{

const token=req.headers.authorization;

if(!token){

return res.status(401).json({message:"Unauthorized"});

}

const decoded=jwt.verify(token,process.env.JWT_SECRET);

req.user=decoded;

next();

};
```

## Protecting Routes

``` javascript
router.get("/profile",auth,getProfile);
```

Only authenticated users can access this route.

## Role-Based Authorization

Example:

``` javascript
if(req.user.role!=="Admin"){

return res.status(403).json({

message:"Access Denied"

});

}
```

## Access Token vs Refresh Token

  Access Token      Refresh Token
  ----------------- ---------------------------
  Short expiry      Long expiry
  Access APIs       Generate new access token
  Sent frequently   Used occasionally

## Logout

JWT logout usually happens by:

-   Removing token from client
-   Blacklisting token (optional)

## Environment Variables

``` env
PORT=5000

MONGO_URI=your_connection_string

JWT_SECRET=your_secret_key
```

## Folder Structure

``` text
project/

controllers/

middleware/
   auth.js

models/

routes/

utils/

server.js

.env
```

## Best Practices

-   Never store plain passwords.
-   Always hash passwords using bcrypt.
-   Store secrets inside `.env`.
-   Set token expiration.
-   Use HTTPS in production.
-   Protect private routes with middleware.
-   Never expose JWT secrets.

## Common Interview Questions

### What is Authentication?

Authentication verifies the identity of a user.

### What is Authorization?

Authorization determines what an authenticated user can access.

### Why do we use bcrypt?

To securely hash passwords before storing them.

### What is JWT?

JWT is a token used to authenticate users after login.

### Difference between Authentication and Authorization?

Authentication checks identity.

Authorization checks permissions.

### Why should passwords never be stored as plain text?

Because anyone with database access can read them.

### What is middleware?

Middleware executes before the request reaches the route handler.

### Why store JWT_SECRET in .env?

To prevent exposing secret keys in source code.

## Quick Revision

-   Authentication verifies users.
-   Authorization controls permissions.
-   bcrypt hashes passwords.
-   JWT maintains user login.
-   Middleware protects routes.
-   JWT contains Header, Payload and Signature.
-   Store secrets in `.env`.
-   Never store plain passwords.
