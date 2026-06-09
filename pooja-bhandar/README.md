# Pooja Bhandar - E-Commerce Website

A complete e-commerce platform for selling pooja samagri and products related to Hindu worship rituals.

## 🏠 Project Structure

```
pooja-bhandar/
├── frontend/              # React.js frontend
├── backend/               # Node.js/Express backend
├── database/              # Database schemas & seed data
├── docs/                  # Documentation
└── README.md             # This file
```

## ✨ Features

- **Product Catalog**: Browse all pooja samagri with advanced filtering
- **Shopping Cart**: Add/manage products in real-time
- **User Authentication**: Secure register/login with JWT
- **Order Management**: Track orders and view history
- **Payment Ready**: Integration points for Stripe/Razorpay
- **Admin Dashboard**: Manage products, inventory, orders
- **Search & Filters**: By category, price range
- **Responsive Design**: Mobile-friendly Tailwind CSS
- **Secure API**: Hashed passwords, JWT tokens, CORS protection

## 🛠️ Tech Stack

### Frontend
- React.js 18.2
- Redux for state management
- Tailwind CSS for styling
- React Router for navigation
- Axios for API calls
- React Icons for UI

### Backend
- Node.js with Express.js
- MongoDB for database
- JWT for authentication
- Bcryptjs for password hashing
- CORS enabled

### Database
- MongoDB (cloud or local)

## 📦 Product Categories

- 🌸 **Incense & Perfumes**: Agarbatti, Camphor, Chandan
- 📿 **Malas & Beads**: Tulsi, Rudraksha, Crystal
- 🛢️ **Oils & Ghee**: Puja oils, Ghee, Rose water
- 🪔 **Puja Essentials**: Diyas, Bells, Havan Samagri

## 🚀 Quick Start

### Prerequisites
- Node.js v14+
- MongoDB (local or Atlas cloud)
- npm or yarn

### Backend Setup
```bash
cd backend
npm install
cp .env.example .env

# Edit .env with your MongoDB URI and JWT secret
# Start MongoDB: mongod

npm run dev
# Server runs on http://localhost:5000
```

### Frontend Setup
```bash
cd frontend
npm install
npm start
# App runs on http://localhost:3000
```

## 🔑 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user

### Products
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get product by ID
- `GET /api/products?category=incense` - Filter by category
- `GET /api/products?search=agarbatti` - Search products

### Orders
- `POST /api/orders` - Create new order
- `GET /api/orders/user/:userId` - Get user's orders

### Users
- `GET /api/users/:id` - Get user profile
- `PUT /api/users/:id` - Update user profile

## 📊 Database Models

### User
```javascript
{
  name, email, password (hashed),
  phone, address, role (customer/admin),
  isVerified, createdAt, updatedAt
}
```

### Product
```javascript
{
  name, description, price, category,
  stock, rating, reviews, images,
  specifications, vendor, sku, tags,
  discount, active, createdAt, updatedAt
}
```

### Order
```javascript
{
  orderNumber, userId, items,
  shippingAddress, paymentMethod,
  paymentStatus, orderStatus,
  subtotal, tax, shipping, total,
  createdAt, updatedAt
}
```

## 🎨 UI Components

- **Navbar** - Logo, navigation, cart icon with counter
- **Hero Section** - Eye-catching landing banner
- **Product Cards** - Grid layout with hover effects
- **Category Filter** - Easy browsing by type
- **Shopping Cart** - Quantity management, order summary
- **Checkout** - Shipping & payment form
- **User Auth** - Login/Register pages
- **Order History** - Past orders tracking
- **Footer** - Contact info, social links

## 🔐 Security

- JWT-based authentication
- Password hashing with bcryptjs (salt rounds: 10)
- CORS protection
- Input validation on backend
- Secure password storage
- Protected API routes

## 📱 Responsive Design

- Mobile-first approach
- Tailwind CSS breakpoints
- Touch-friendly UI
- Fast loading times
- Optimized images

## 🚀 Deployment

### Frontend
- Vercel: `vercel deploy`
- Netlify: Connect GitHub repo
- AWS S3 + CloudFront

### Backend
- Heroku: `git push heroku main`
- AWS EC2
- DigitalOcean
- Railway.app

### Database
- MongoDB Atlas (cloud)
- AWS DocumentDB
- Self-hosted MongoDB

## 📝 Environment Variables

### Backend (.env)
```
MONGODB_URI=mongodb://localhost:27017/pooja-bhandar
JWT_SECRET=your_secret_key_here
PORT=5000
NODE_ENV=development
```

## 🎯 Future Enhancements

- [ ] Stripe/Razorpay payment integration
- [ ] Email notifications
- [ ] Advanced admin dashboard
- [ ] Product reviews & ratings
- [ ] Wishlist feature
- [ ] Inventory management
- [ ] Multi-language (Hindi)
- [ ] Mobile app (React Native)
- [ ] Analytics dashboard
- [ ] SMS notifications

## 📞 Support

- Issues: Create GitHub issue
- Email: support@poojabhandar.com
- Phone: +1-800-POOJA-123

## 📄 License

MIT License - Use for your business freely

## 🙏 Brand

**Pooja Bhandar**
- Authentic pooja samagri & spiritual products
- Beautiful mandala logo with sacred 'P' symbol
- Serving devotees worldwide
- Since 2026

---

Made with 🙏 for spiritual seekers
