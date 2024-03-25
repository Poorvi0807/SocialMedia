## SocialMedia

## 🟢 Backend :-

🟡 GitHub Repo :- https://github.com/Poorvi0807/SocialMedia

🟡 Backend Deploy :- https://social-media-graphql-theta.vercel.app/

### Backend
- Node.js
- MongoDB
- Mongoose
- GraphQL
- Apollo Server

## Installation and Setup

### Backend

1. Clone the repository.
2. Navigate to the backend directory.
3. Run npm install to install dependencies.
4. Run node index to start the development server.

## API Endpoints

API's are built with graphQL

### Queries

🟢 Get All Posts:

    query {
    getPosts {
        id
        body
        createdAt
        username
        likeCount
        commentCount
    }
    }


🟢 Get a Specific Post by ID:

    query {
    getPost(postId: "post_id_here") {
        id
        body
        createdAt
        username
        likeCount
        commentCount
    }
    }



### Mutations

🟠 User Registration:

    mutation {
        register(registerInput: { username: "example_user", email: "user@example.com", password: "password123", confirmPassword: "password123" }) {
            id
            email
            username
            createdAt
            token
        }
    }



🟠 User Login:

    mutation {
        login(username: "example_user", password: "password123") {
            id
            email
            username
            createdAt
            token
        }
    }



🟠 Create a Post:

    mutation {
        createPost(body: "This is a test post") {
            id
            body
            createdAt
            username
        }
    }



🟠 Create a Comment on a Post:

    mutation {
        createComment(postId: "post_id_here", body: "This is a test comment") {
            id
            comments {
            id
            body
            createdAt
            username
            }
        }
    }




🟠 Delete a Post (Requires authentication):

    mutation {
        deletePost(postId: "post_id_here")
    }


🟠 Like a Post (Requires authentication):

    mutation {
        likePost(postId: "post_id_here") {
            id
            likeCount
        }
    }


🟠 Update a Post (Requires authentication):

    mutation {
        updatePost(postId: "post_id_here", body: "Updated post body") {
            id
            body
            createdAt
            username
        }
    }


🟠 Delete a Comment (Requires authentication):

    mutation {
    deleteComment(postId: "post_id_here", commentId: "comment_id_here") {
        id
        comments {
        id
        body
        createdAt
        username
        }
    }
    }
