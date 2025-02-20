# LexDroit
html file
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <meta
      name="description"
      content="Lex Droit - The finest place for legal assistance"
    />
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
    <!-- Bootstrap CSS -->
    <link 
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" 
      rel="stylesheet"
    />
    <title>Lex Droit</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
    <!-- Bootstrap JS Bundle with Popper -->
    <script 
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"
    ></script>
  </body>
</html> 






css file
/* General Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Arial', sans-serif;
  background-color: #f5f5f5;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Header Styles */
.header {
  background-color: #000;
  color: white;
  padding: 20px 0;
}

.logo-section {
  text-align: center;
  margin-bottom: 20px;
}

.logo-section h1 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.subtitle {
  font-style: italic;
  color: #888;
}

/* Auth Styles */
.auth-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: calc(100vh - 100px);
  padding: 20px;
}

.auth-box {
  background: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
  width: 100%;
  max-width: 400px;
}

.avatar-placeholder {
  width: 100px;
  height: 100px;
  background-color: #eee;
  border-radius: 50%;
  margin: 0 auto 20px;
}

input {
  width: 100%;
  padding: 12px;
  margin-bottom: 15px;
  border: 2px solid #eee;
  border-radius: 8px;
  font-size: 16px;
}

.continue-btn {
  width: 100%;
  padding: 12px;
  background-color: #000;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 10px;
}

.google-login {
  text-align: center;
  margin-top: 20px;
}

.google-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  padding: 12px;
  background-color: white;
  border: 2px solid #eee;
  border-radius: 8px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 10px;
}

.google-btn img {
  width: 20px;
  margin-left: 10px;
}

/* Lawyers Page Styles */
.lawyers-container {
  padding: 2rem;
  background-color: #000;
  min-height: calc(100vh - 80px);
  color: white;
}

.lawyers-title {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.5rem;
}

.lawyers-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.lawyer-card {
  background-color: #111;
  border-radius: 15px;
  padding: 1.5rem;
  text-align: center;
  transition: transform 0.3s ease;
  cursor: pointer;
}

.lawyer-card:hover {
  transform: translateY(-5px);
}

.lawyer-avatar {
  width: 120px;
  height: 120px;
  margin: 0 auto 1rem;
  border-radius: 50%;
  background-color: #333;
  overflow: hidden;
}

.lawyer-avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.lawyer-name {
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
}

.star {
  color: #ffd700;
}

.lawyer-details {
  color: #888;
  font-size: 0.9rem;
}

/* Services Page Styles */
.services-container {
  padding: 2rem;
  text-align: center;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 2rem auto;
}

.service-card {
  background-color: white;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
  cursor: pointer;
  transition: transform 0.3s ease;
}

.service-card:hover {
  transform: translateY(-5px);
}

.service-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
} 







index js
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
); 
import React, { useState } from 'react';

function Register() {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');
  const [confirmPassword, setConfirmPassword] = useState('');

  const handleSubmit = (e) => {
    e.preventDefault();
    // Add registration logic here
  };

  return (
    <div className="auth-container">
      <div className="auth-box">
        <div className="avatar-placeholder"></div>
        <form onSubmit={handleSubmit}>
          <input
            type="text"
            placeholder="Username"
            value={username}
            onChange={(e) => setUsername(e.target.value)}
          />
          <input
            type="password"
            placeholder="Set your password"
            value={password}
            onChange={(e) => setPassword(e.target.value)}
          />
          <input
            type="password"
            placeholder="Confirm your password"
            value={confirmPassword}
            onChange={(e) => setConfirmPassword(e.target.value)}
          />
          <button type="submit" className="continue-btn">Register</button>
        </form>
      </div>
    </div>
  );
}

export default Register; 







login js
import React, { useState } from 'react';
import { Link } from 'react-router-dom';

function Login() {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');

  const handleSubmit = (e) => {
    e.preventDefault();
    // Add login logic here
  };

  return (
    <div className="auth-container">
      <div className="auth-box">
        <div className="avatar-placeholder"></div>
        <form onSubmit={handleSubmit}>
          <input
            type="email"
            placeholder="Enter your email"
            value={email}
            onChange={(e) => setEmail(e.target.value)}
          />
          <input
            type="password"
            placeholder="Enter your password"
            value={password}
            onChange={(e) => setPassword(e.target.value)}
          />
          <button type="submit" className="continue-btn">Continue</button>
          <div className="google-login">
            <span>Or</span>
            <button className="google-btn">
              login with google <img src="/google-icon.png" alt="Google" />
            </button>
          </div>
        </form>
      </div>
    </div>
  );
}

export default Login; 






header js
import React from 'react';
import { Link } from 'react-router-dom';

function Header() {
  return (
    <header className="header">
      <div className="container">
        <div className="logo-section">
          <h1>Lex•Droit</h1>
          <p className="subtitle">The finest place for legal assistance</p>
        </div>
        <nav>
          <Link to="/" className="nav-link">Login</Link>
          <Link to="/register" className="nav-link">Register</Link>
        </nav>
      </div>
    </header>
  );
}

export default Header; 





app js
import React from 'react';
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
import Header from './components/Header';
import Login from './components/Login';
import Register from './components/Register';
import Services from './components/Services';
import ChatInterface from './components/ChatInterface';
import Lawyers from './components/Lawyers';
import './styles.css';

function App() {
  return (
    <Router>
      <div className="app">
        <Header />
        <Routes>
          <Route path="/" element={<Login />} />
          <Route path="/register" element={<Register />} />
          <Route path="/services" element={<Services />} />
          <Route path="/chat" element={<ChatInterface />} />
          <Route path="/lawyers" element={<Lawyers />} />
        </Routes>
      </div>
    </Router>
  );
}

export default App; 





register js

import React, { useState } from 'react';

function Register() {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');
  const [confirmPassword, setConfirmPassword] = useState('');

  const handleSubmit = (e) => {
    e.preventDefault();
    // Add registration logic here
  };

  return (
    <div className="auth-container">
      <div className="auth-box">
        <div className="avatar-placeholder"></div>
        <form onSubmit={handleSubmit}>
          <input
            type="text"
            placeholder="Username"
            value={username}
            onChange={(e) => setUsername(e.target.value)}
          />
          <input
            type="password"
            placeholder="Set your password"
            value={password}
            onChange={(e) => setPassword(e.target.value)}
          />
          <input
            type="password"
            placeholder="Confirm your password"
            value={confirmPassword}
            onChange={(e) => setConfirmPassword(e.target.value)}
          />
          <button type="submit" className="continue-btn">Register</button>
        </form>
      </div>
    </div>
  );
}

export default Register; 



service js

import React from 'react';
import { useNavigate } from 'react-router-dom';

function Services() {
  const navigate = useNavigate();

  return (
    <div className="services-container">
      <h1>Our Services</h1>
      <div className="services-grid">
        <div className="service-card" onClick={() => navigate('/chat')}>
          <div className="service-icon">🤖</div>
          <h2>Chat with Jessy</h2>
          <p>An AI-Powered chatbot which provides you with the best advice and legal information</p>
        </div>
        <div className="service-card" onClick={() => navigate('/lawyers')}>
          <div className="service-icon">⚖️</div>
          <h2>Legal Advice</h2>
          <p>Connect with lawyers and legal counselors in real-time</p>
        </div>
      </div>
    </div>
  );
}

export default Services; 




lawyer js

import React from 'react';

const lawyers = [
  { id: 1, name: "John Smith", details: "Corporate Law Specialist", rating: 5 },
  { id: 2, name: "Sarah Wilson", details: "Family Law Expert", rating: 5 },
  { id: 3, name: "Michael Chen", details: "Criminal Defense Attorney", rating: 5 },
  { id: 4, name: "Emma Davis", details: "Real Estate Law Specialist", rating: 5 },
  { id: 5, name: "James Brown", details: "Immigration Law Expert", rating: 5 },
  { id: 6, name: "Lisa Taylor", details: "Intellectual Property Lawyer", rating: 5 }
];

function Lawyers() {
  return (
    <div className="lawyers-container">
      <h1 className="lawyers-title">Connect with lawyers</h1>
      <div className="lawyers-grid">
        {lawyers.map(lawyer => (
          <div key={lawyer.id} className="lawyer-card">
            <div className="lawyer-avatar">
              <img src="/avatar-placeholder.png" alt={lawyer.name} />
            </div>
            <div className="lawyer-info">
              <h3 className="lawyer-name">
                {lawyer.name}
                <span className="star">⭐</span>
              </h3>
              <p className="lawyer-details">{lawyer.details}</p>
            </div>
          </div>
        ))}
      </div>
    </div>
  );
}

export default Lawyers; 




