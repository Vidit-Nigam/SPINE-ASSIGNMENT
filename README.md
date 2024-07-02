Project Title
Spyne SDE-1 Backend-Role Assignment

Description
In this project we are have made a kind of social media project , where a user can login/sign up , and do CRUD operation on Discusssion/Post, like, Comment.

Important Note
Note: I am using a free server on Render, so there may be a cold start issue. All microservices may take more than 30 seconds to respond to the first request.

Table of Contents
Installation
Usage
API Endpoints
Microservices
Low Level Design (LLD)
Database Schema
Technologies Used
Installation
Instructions on how to set up and run the project locally.

# Clone the repository
git clone https://github.com/Vikas62502/spyne-backend.git

# Navigate to the project directory
cd spyne-backend

# Install dependencies for the API Gateway
cd api-gateway
npm install
npm run dev

# Install dependencies for each microservice

cd ../user-service
npm install

cd ../discussion-service
npm install

cd ../comment-service
npm install

cd ../like-service
npm install

# Start the API Gateway
cd ../api-gateway
npm start

# Start each microservice in separate terminal tabs/windows

cd ../user-service
npm start

cd ../discussion-service
npm start

cd ../comment-service
npm start

cd ../like-service
npm start
Usage
Now below i have provided the api endpoint you can hit using postman at

Public URL of postman

https://www.postman.com/lunar-capsule-120648/workspace/sypne-sde-i-assignment/collection/34837752-b5b5c2d4-3887-41a9-bb19-08627eafc003
API Endpoints
List of all API endpoints with brief descriptions.

User Service
Create User: POST /users/signup
Login User: POST /users/login
Follow Other User: POST /users/followUser/:uidOfOtherUser
Update User: PUT /users/updateUser/:uid
Delete User: DELETE /users/deleteUser/:id
Get All List of Users: GET /users/getAllUsers
Search User by Name: GET /users/searchUserByName/:name
Discussion Service
Create Discussion: POST /discussions/createDiscussion
Update Discussion: POST /discussions/updateDiscussion/:discussionId
Delete Discussion: DELETE /discussions/deleteDiscussion/:discussionId
Get Discussion By Tags: GET /discussions/getAllDiscussionsByTags?tags=%23:tagName
Get Discussion By Text: GET /discussions//getAllDiscussionBasedOnText?text=:SearchText
Get View Count: GET /discussions/getViewCount/:discussionId
Like Service
Create Like: POST /likes/createLike
Delete Like: DELETE /likes/deleteLike/:LikeId
Comment Service
Create Comment: POST /comments/createComment
Reply to Comment: POST /comments/replyComment
Update Comment : POST /comments/updateComment/:CommentId
Delete Discussion: DELETE /comments/deleteComment/:CommentId
