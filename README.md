# postsAPI
This backend API project is built using Next.js App Router, PostgreSQL, Prisma ORM, and Zod for input validation. It provides secure user authentication using JWT and includes features for creating and searching posts and comments.

🌟 Features
User Registration (/api/auth/register)

Validates input using Zod

Hashes passwords with bcrypt

Stores user credentials securely in PostgreSQL



User Login (/api/auth/login)

Validates credentials

Returns a JWT token on successfully login

Protected Routes

Create Post (/api/posts, POST)

Create Comment (/api/comments, POST)

Require users to be authenticated (i.e., registered and logged in)

Users must send a valid JWT token in the Authorization header

Public Routes

Get All Posts (/api/posts, GET)
Accessible without authentication

Search Posts (/api/posts?tag=...)
Filter posts by title or tags

🔐 Authentication
JWT is issued on login

Protected endpoints use middleware to verify the JWT

Unauthorized users receive a 401 response
