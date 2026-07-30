# Day 29 - Learning Authentication & Authorization using JWT

## What did I learn?

Today I learned one of the most essential concepts in backend development—**Authentication and Authorization**. Until now, all the APIs I built were open, meaning anyone could send a request and access them. Today I finally understood how real-world applications identify users, keep them logged in, and make sure only the right people can access certain features.

One of the first things I learned was the difference between **Authentication** and **Authorization**. In the beginning, both terms sounded almost identical to me, and I often mixed them up. But after going through examples, I realized that authentication is simply proving who you are, while authorization is deciding what you're allowed to do after you've been identified. That small difference made the whole login process much easier to understand.

I also learned why developers never store passwords directly in the database. Before today, I knew passwords were "encrypted," but I didn't really understand how it worked. I learned about **bcrypt**, which hashes passwords before storing them. What surprised me the most was that hashed passwords can't be converted back into the original password. Instead, when a user logs in, the entered password is hashed again and compared with the stored hash. That made me realize how seriously applications take user security.

Another concept that really clicked for me today was **JWT (JSON Web Token)**. I had always wondered how websites remember that I'm logged in even after refreshing the page or opening another tab. Now I understand that once the user logs in successfully, the server creates a token and sends it back to the client. Every future request includes this token, allowing the server to recognize the user without asking them to log in again. It finally connected all the pieces together for me.

I also walked through the complete **registration and login flow**, starting from creating a user account, hashing the password, storing it in MongoDB, comparing passwords during login, generating a JWT, and finally protecting routes using authentication middleware. Seeing the entire process step by step helped me understand how everything works together instead of learning each concept separately.

Towards the end, I learned about **role-based authorization**. I understood that not every logged-in user should have the same permissions. For example, an admin can manage users or delete records, while a normal user can only access their own profile. This showed me that logging in is only the first step—the application also needs to decide what each user is allowed to do.

By the end of today's learning, I realized that authentication isn't just about creating a login page. It's about building trust between the user and the application by protecting passwords, verifying identities, securing APIs, and making sure users only access what they're supposed to.

## What challenges did I face?

The biggest challenge today was understanding how all the different pieces fit together. I knew about passwords, JWT, and middleware individually, but at first I couldn't visualize the complete flow. After tracing the process from user registration to accessing a protected route, everything finally started making sense.

I also found it a little confusing to understand the difference between **hashing** and **encryption**. Initially, I thought both meant hiding data. After learning more, I realized that hashing is a one-way process mainly used for passwords, while encryption allows data to be decrypted when needed.

Another small challenge was understanding where JWT verification actually happens. I first assumed every route would need to verify the token manually, but learning about authentication middleware showed me how one middleware can automatically protect multiple routes, making the application much cleaner and easier to maintain.

## What new concepts did I understand?

### Authentication

I learned that authentication is the process of verifying a user's identity before allowing them to access an application.

### Authorization

I understood that authorization determines what an authenticated user is allowed to access or perform inside the application.

### bcrypt

I learned that bcrypt securely hashes passwords before storing them, making it extremely difficult for attackers to obtain the original passwords even if the database is compromised.

### Password Hashing

I understood why passwords should always be hashed instead of stored as plain text and how hashing improves application security.

### JSON Web Token (JWT)

I learned that JWT allows users to stay logged in by securely identifying them through a signed token that is sent with every request.

### Authentication Middleware

I learned how middleware automatically verifies JWT tokens before allowing access to protected APIs, making authentication reusable across the application.

### Role-Based Authorization

I understood how applications provide different permissions to different users based on their roles, such as Admin or User.

## What computer/software engineering fundamentals did I learn today?

Today's learning made me realize that backend development isn't only about building APIs—it is also about protecting them. Even the best application becomes vulnerable if anyone can access its private routes.

I learned that security should always be considered while designing backend systems. Hashing passwords, verifying user identities, protecting sensitive routes, and controlling user permissions are all essential parts of building reliable applications.

I also understood why authentication logic is usually placed inside middleware. It keeps the code organized, avoids repetition, and follows the principle of writing reusable components, which is an important software engineering practice.

## What changed in my thinking?

Before today, I thought logging into an application was simply about checking whether the email and password were correct.

After learning today's concepts, I realized that there is an entire security process happening behind the scenes. Passwords are hashed before being stored, JWT tokens are generated after successful login, middleware verifies every protected request, and authorization ensures that users can only perform actions they have permission for.

The biggest realization for me today was that authentication and authorization are the backbone of secure backend applications. Without them, any application would be vulnerable, no matter how well the rest of the code is written.

## Today's One Line Summary

> **"Today I learned how backend applications securely identify users using bcrypt and JWT, protect APIs with authentication middleware, and control access through authorization, making applications secure, reliable, and ready for real-world use."**