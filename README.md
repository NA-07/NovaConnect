<p align="center">
  <img src="https://img.shields.io/badge/NovaConnect-Social%20Media-667eea?style=for-the-badge&logo=react&logoColor=white" alt="NovaConnect"/>
</p>

<h1 align="center">🚀 NovaConnect</h1>

<p align="center">
  <strong>Connect. Share. Inspire.</strong>
</p>

<p align="center">
  A modern, vibrant social media platform built with the MERN stack featuring real-time messaging, beautiful UI with glassmorphism effects, and a powerful admin dashboard.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB"/>
  <img src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white" alt="Express"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js"/>
  <img src="https://img.shields.io/badge/Redux-764ABC?style=flat-square&logo=redux&logoColor=white" alt="Redux"/>
  <img src="https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white" alt="Socket.io"/>
</p>

---

## ✨ Features

### 👤 User Features

| Feature | Description |
|---------|-------------|
| 🔐 **Authentication** | Secure user registration and login with encrypted passwords |
| 📸 **Post Creation** | Share images via camera or file upload with captions |
| 💬 **Real-time Messaging** | Instant messaging with Socket.io integration |
| ❤️ **Interactions** | Like, comment, share, and save posts |
| 🔔 **Notifications** | Real-time notifications for all activities |
| 🔍 **User Search** | Find and follow other users by username |
| 👥 **Suggestions** | Smart user suggestions based on connections |
| 🌙 **Dark Mode** | Toggle between light and dark themes |
| 📄 **Pagination** | Smooth infinite scroll on all pages |
| 🔗 **Share Posts** | Copy post links and share on social media |
| 📁 **Saved Posts** | Save favorite posts to your collection |
| 🗺️ **Explore Page** | Discover posts from random users |
| 👤 **Profile Management** | Edit profile, change password, update avatar |
| 💬 **Nested Comments** | Comment and reply with like functionality |
| 🚩 **Report System** | Report inappropriate content |

### 👨‍💼 Admin Features

| Feature | Description |
|---------|-------------|
| 📊 **Dashboard** | Visual analytics with charts and statistics |
| 👥 **User Management** | View and manage all registered users |
| 🛡️ **Admin Roles** | Create and assign admin accounts |
| 🚨 **Spam Management** | Review and delete reported posts |
| 📈 **Analytics** | Track total posts, users, and reported content |

---

## 🎨 UI/UX Highlights

- **Glassmorphism Design** - Modern frosted glass effects throughout the app
- **Vibrant Gradients** - Beautiful color gradients (Purple, Pink, Blue theme)
- **Smooth Animations** - Fluid transitions and micro-interactions
- **Responsive Layout** - Perfect on desktop, tablet, and mobile devices
- **Modern Typography** - Inter font family for clean readability
- **Custom Scrollbars** - Styled scrollbars matching the theme
- **Hover Effects** - Engaging hover states on all interactive elements

---

## 🛠️ Tech Stack

### Frontend
- **React 17** - UI library
- **Redux** - State management
- **React Router** - Navigation
- **Socket.io Client** - Real-time communication
- **Material UI** - Component library
- **Axios** - HTTP client
- **React Share** - Social media sharing
- **Emoji Mart** - Emoji picker

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **Socket.io** - Real-time events
- **JWT** - Authentication
- **Bcrypt** - Password hashing

### Cloud Services
- **Cloudinary** - Image hosting and optimization
- **MongoDB Atlas** - Cloud database (optional)

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14 or higher)
- **npm** or **yarn**
- **MongoDB** (local or MongoDB Atlas)
- **Cloudinary Account** (for image uploads)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/NovaConnect.git
cd NovaConnect
```

### 2. Environment Setup

Create a `.env` file in the root directory:

```env
MONGODB_URL=your_mongodb_connection_string
ACCESS_TOKEN_SECRET=your_access_token_secret
REFRESH_TOKEN_SECRET=your_refresh_token_secret
```

### 3. Configure Cloudinary

Edit `/client/src/utils/imageUpload.js` with your Cloudinary credentials:

```javascript
const cloudinary_cloud_name = 'your_cloud_name';
const cloudinary_upload_preset = 'your_upload_preset';
```

### 4. Install Dependencies

```bash
# Install backend dependencies
npm install

# Install frontend dependencies
cd client
npm install
```

### 5. Run the Application

```bash
# Start backend server (from root directory)
npm run dev

# Start frontend (from /client directory)
cd client
npm start
```

### 6. Access the Application

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 📁 Project Structure

```
NovaConnect/
├── 📂 client/                 # React frontend
│   ├── 📂 public/            # Static files
│   └── 📂 src/
│       ├── 📂 components/    # Reusable components
│       ├── 📂 pages/         # Page components
│       ├── 📂 redux/         # Redux store, actions, reducers
│       ├── 📂 styles/        # CSS stylesheets
│       ├── 📂 utils/         # Utility functions
│       └── 📂 images/        # Image assets
├── 📂 controllers/           # Route controllers
├── 📂 middleware/            # Express middleware
├── 📂 models/                # Mongoose schemas
├── 📂 routes/                # API routes
├── 📄 server.js              # Express server entry
├── 📄 socketServer.js        # Socket.io configuration
└── 📄 package.json           # Backend dependencies
```

---

## 🔌 API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/register` | Register new user |
| POST | `/api/login` | User login |
| POST | `/api/logout` | User logout |
| POST | `/api/refresh_token` | Refresh access token |

### Users
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/search` | Search users |
| GET | `/api/user/:id` | Get user profile |
| PATCH | `/api/user` | Update profile |
| PATCH | `/api/user/:id/follow` | Follow user |
| PATCH | `/api/user/:id/unfollow` | Unfollow user |

### Posts
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/posts` | Create post |
| GET | `/api/posts` | Get all posts |
| GET | `/api/post/:id` | Get single post |
| PATCH | `/api/post/:id` | Update post |
| DELETE | `/api/post/:id` | Delete post |
| PATCH | `/api/post/:id/like` | Like post |
| PATCH | `/api/post/:id/unlike` | Unlike post |
| PATCH | `/api/savePost/:id` | Save post |
| PATCH | `/api/unSavePost/:id` | Unsave post |

### Comments
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/comment` | Create comment |
| PATCH | `/api/comment/:id` | Update comment |
| DELETE | `/api/comment/:id` | Delete comment |
| PATCH | `/api/comment/:id/like` | Like comment |
| PATCH | `/api/comment/:id/unlike` | Unlike comment |

### Messages
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/message` | Send message |
| GET | `/api/conversations` | Get conversations |
| GET | `/api/message/:id` | Get messages |
| DELETE | `/api/message/:id` | Delete message |

---

## 🎯 Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Primary | `#6366f1` | Buttons, links, accents |
| Secondary | `#ec4899` | Highlights, gradients |
| Accent | `#06b6d4` | Info states, icons |
| Success | `#10b981` | Success messages |
| Warning | `#f59e0b` | Warning states |
| Error | `#f43f5e` | Error messages |

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [React](https://reactjs.org/)
- [MongoDB](https://www.mongodb.com/)
- [Socket.io](https://socket.io/)
- [Cloudinary](https://cloudinary.com/)
- [Material UI](https://mui.com/)

---

<p align="center">
  Made with ❤️ by <strong>NovaConnect Team</strong>
</p>

<p align="center">
  ⭐ Star this repo if you find it helpful!
</p>



