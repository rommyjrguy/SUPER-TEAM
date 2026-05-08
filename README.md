# Finance Tracker - ITEC

A web-based finance management system for ITEC with user authentication and dashboard.

## Features

✅ **User Authentication**
- User signup and login functionality
- Email validation and password security
- Session management using localStorage
- Auto-login persistence

✅ **User Dashboard**
- Personalized greeting
- User profile display
- Logout functionality

✅ **Data Persistence**
- All user data stored in localStorage
- Persistent sessions across page refreshes
- No backend server required

## Getting Started

### Installation

1. Clone the repository:
```bash
git clone https://github.com/rommyjrguy/SUPER-TEAM.git
cd SUPER-TEAM
```

2. Open `index.html` in your web browser (no build process needed)

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve

# Or simply open index.html in your browser
```

## Usage

### Default Test Accounts

The app comes with two pre-configured accounts for testing:

**Account 1:**
- Email: `john@itec.com`
- Password: `password123`

**Account 2:**
- Email: `jane@itec.com`
- Password: `password123`

### Creating a New Account

1. Click "Sign Up" on the login page
2. Enter your name, email, and password
3. Confirm your password
4. Click "Sign Up"
5. You'll be automatically logged in after signup

### Logging In

1. Enter your email address
2. Enter your password
3. Click "Login"

### Logging Out

Click the "Logout" button in the top-right corner of the dashboard.

## Project Structure

```
SUPER-TEAM/
├── index.html       # HTML structure for login, signup, and dashboard
├── styles.css       # CSS styling for all pages
├── auth.js          # Authentication logic and UI controller
└── README.md        # This file
```

## Technical Details

### Authentication System (`auth.js`)

**AuthManager Class:**
- `signup(name, email, password)` - Register new user
- `login(email, password)` - Authenticate user
- `logout()` - End user session
- `getCurrentUser()` - Get active user info
- `isAuthenticated()` - Check if user is logged in
- `changePassword(email, oldPassword, newPassword)` - Update password
- `updateProfile(userId, updates)` - Modify user info

**UIController Class:**
- Handles form submissions
- Manages page switching
- Shows error messages
- Updates dashboard content

### Data Storage

**localStorage Keys:**
- `finance_tracker_users` - Array of all registered users
- `finance_tracker_current_user` - Currently logged-in user session

**User Object Structure:**
```json
{
  "id": 1234567890,
  "name": "John Doe",
  "email": "john@itec.com",
  "password": "hashedPassword",
  "createdAt": "2026-05-08T10:00:00.000Z"
}
```

## Security Notes

⚠️ **Important:** This authentication system uses localStorage, which is suitable for learning projects but has limitations:

1. **Password Storage**: Uses a simple hash function (NOT cryptographically secure). For production, use proper password hashing on the backend.
2. **Data Persistence**: localStorage is vulnerable to XSS attacks. In production, use secure server-side sessions with httpOnly cookies.
3. **No Encryption**: User data is stored in plain text in localStorage. Sensitive data should be encrypted.

## Future Enhancements

- [ ] Backend API integration (Node.js/Express)
- [ ] Secure password hashing (bcrypt)
- [ ] Database integration (MongoDB/PostgreSQL)
- [ ] JWT token authentication
- [ ] Email verification
- [ ] Password reset functionality
- [ ] Two-factor authentication
- [ ] Transaction tracking
- [ ] Expense categorization
- [ ] Budget planning features
- [ ] Data export (CSV/PDF)
- [ ] Mobile app version

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This project is part of ITEC coursework.

## Support

For issues or questions, please open an issue on the GitHub repository.
