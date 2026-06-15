# Backend Project 1 - Video Sharing Platform API

A scalable Node.js backend inspired by modern video-sharing platforms. This project provides authentication, video management, subscriptions, playlists, comments, likes, tweets, user profiles, dashboard analytics, and media uploads using Cloudinary.

## 🚀 Features

### Authentication & Authorization

* User Registration
* User Login & Logout
* JWT Access Token Authentication
* Refresh Token Mechanism
* Change Password
* Get Current User
* Update Account Details

### User Management

* Update Avatar
* Update Cover Image
* Channel Profile
* Watch History
* User Dashboard

### Video Management

* Upload Videos
* Upload Thumbnails
* Get All Videos
* Get Video By ID
* Update Video Details
* Delete Video
* Toggle Publish Status

### Comments

* Add Comment
* Update Comment
* Delete Comment
* Get Video Comments

### Likes System

* Like/Unlike Videos
* Like/Unlike Comments
* Like/Unlike Tweets
* Get Liked Videos

### Subscription System

* Subscribe/Unsubscribe Channels
* Get Channel Subscribers
* Get Subscribed Channels

### Playlist Management

* Create Playlist
* Update Playlist
* Delete Playlist
* Add Video To Playlist
* Remove Video From Playlist
* Get User Playlists

### Tweets

* Create Tweet
* Update Tweet
* Delete Tweet
* Get User Tweets

### Dashboard Analytics

* Channel Statistics
* Uploaded Videos Analytics

### Media Management

* Cloudinary Integration
* Video Uploads
* Thumbnail Uploads
* Avatar Uploads
* Cover Image Uploads

---

## 🛠 Tech Stack

### Backend

* Node.js
* Express.js

### Database

* MongoDB
* Mongoose ODM

### Authentication

* JWT (Access Token)
* Refresh Tokens
* bcrypt

### Media Storage

* Cloudinary
* Multer

### Other Tools

* MongoDB Aggregation Pipelines
* Cookie Parser
* CORS
* dotenv

---

## 📁 Project Structure

```bash
src/
├── controllers/
├── models/
├── routes/
├── middlewares/
├── utils/
├── db/
├── constants/
├── app.js
└── index.js
```

---

## ⚙️ Environment Variables

Create a `.env` file in the root directory.

```env
PORT=8000

MONGODB_URI=

ACCESS_TOKEN_SECRET=
ACCESS_TOKEN_EXPIRY=1d

REFRESH_TOKEN_SECRET=
REFRESH_TOKEN_EXPIRY=10d

CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=

CORS_ORIGIN=http://localhost:3000
```

---

## 📦 Installation

Clone the repository

```bash
git clone https://github.com/sonianuj01/backend_project1.git
```

Navigate into project

```bash
cd backend_project1
```

Install dependencies

```bash
npm install
```

Run development server

```bash
npm run dev
```

---

# API Endpoints

Base URL

```bash
/api/v1
```

---

## User Routes

### Register User

```http
POST /users/register
```

Form Data

```text
fullName
email
username
password
avatar
coverImage (optional)
```

### Login

```http
POST /users/login
```

```json
{
  "email": "user@example.com",
  "password": "password"
}
```

### Logout

```http
POST /users/logout
```

### Refresh Token

```http
POST /users/refresh-token
```

### Change Password

```http
POST /users/change-password
```

```json
{
  "oldPassword": "oldpassword",
  "newPassword": "newpassword"
}
```

### Current User

```http
GET /users/current-user
```

### Update Account

```http
PATCH /users/update-account
```

### Update Avatar

```http
PATCH /users/avatar
```

### Update Cover Image

```http
PATCH /users/cover-image
```

### Channel Profile

```http
GET /users/c/:username
```

### Watch History

```http
GET /users/history
```

---

## Video Routes

### Get All Videos

```http
GET /videos
```

### Publish Video

```http
POST /videos
```

Form Data

```text
title
description
videoFile
thumbnail
```

### Get Video

```http
GET /videos/:videoId
```

### Update Video

```http
PATCH /videos/:videoId
```

### Delete Video

```http
DELETE /videos/:videoId
```

### Toggle Publish Status

```http
PATCH /videos/toggle/publish/:videoId
```

---

## Comment Routes

### Get Comments

```http
GET /comments/:videoId
```

### Add Comment

```http
POST /comments/:videoId
```

### Update Comment

```http
PATCH /comments/c/:commentId
```

### Delete Comment

```http
DELETE /comments/c/:commentId
```

---

## Playlist Routes

### Create Playlist

```http
POST /playlists
```

### Get Playlist

```http
GET /playlists/:playlistId
```

### Update Playlist

```http
PATCH /playlists/:playlistId
```

### Delete Playlist

```http
DELETE /playlists/:playlistId
```

### Add Video To Playlist

```http
PATCH /playlists/add/:videoId/:playlistId
```

### Remove Video From Playlist

```http
PATCH /playlists/remove/:videoId/:playlistId
```

### Get User Playlists

```http
GET /playlists/user/:userId
```

---

## Like Routes

### Toggle Video Like

```http
POST /likes/toggle/v/:videoId
```

### Toggle Comment Like

```http
POST /likes/toggle/c/:commentId
```

### Toggle Tweet Like

```http
POST /likes/toggle/t/:tweetId
```

### Get Liked Videos

```http
GET /likes/videos
```

---

## Subscription Routes

### Subscribe/Unsubscribe

```http
POST /subscriptions/c/:channelId
```

### Get Subscribed Channels

```http
GET /subscriptions/c/:channelId
```

### Get Subscribers

```http
GET /subscriptions/u/:subscriberId
```

---

## Tweet Routes

### Create Tweet

```http
POST /tweets
```

### Get User Tweets

```http
GET /tweets/user/:userId
```

### Update Tweet

```http
PATCH /tweets/:tweetId
```

### Delete Tweet

```http
DELETE /tweets/:tweetId
```

---

## Dashboard Routes

### Channel Statistics

```http
GET /dashboard/stats
```

### Channel Videos

```http
GET /dashboard/videos
```

---

## Health Check

```http
GET /healthcheck
```

---

## 🔐 Authentication

Protected routes require a JWT Access Token.

```http
Authorization: Bearer <access_token>
```

---

## 📊 MongoDB Aggregation Usage

The project extensively utilizes MongoDB Aggregation Pipelines for:

* Channel Statistics
* Subscriber Count
* Subscription Status
* Watch History
* User Profile Aggregation
* Dashboard Analytics
* Video Metrics

---

## 🌟 Future Enhancements

* Real-time Notifications
* Video Streaming Optimization
* Search & Recommendation Engine
* WebSocket Integration
* Video Processing Queue
* Admin Dashboard

---

## 👨‍💻 Author

Anuj Verma

GitHub:
https://github.com/sonianuj01

---

## 📄 License

This project is licensed under the MIT License.
