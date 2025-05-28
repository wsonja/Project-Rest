# **TableTalk Backend**
*Flask-based REST API for Restaurant Review Intelligence*

## **📌 Overview**
The TableTalk backend is a robust Flask-based REST API that powers the restaurant review analysis platform. It provides comprehensive endpoints for user management, business operations, review processing, and AI-powered analytics.

## **🏗 Architecture**
- **Framework:** Flask with Blueprint-based modular design
- **Database:** SQLAlchemy ORM with PostgreSQL/MySQL support
- **Authentication:** JWT-based authentication using Flask-JWT-Extended
- **AI Integration:** Google Cloud Natural Language API and OpenRouter API
- **Web Scraping:** Selenium WebDriver for Google Maps review extraction

## **📁 Project Structure**
```
backend/
├── routes/
│   ├── auth.py          # Authentication endpoints
│   ├── user.py          # User management
│   ├── businesses.py    # Business operations
│   ├── reviews.py       # Review management
│   └── dashboard.py     # Analytics dashboard
├── models/
│   ├── user.py          # User model
│   ├── business.py      # Business model
│   ├── review.py        # Review model
│   ├── insight.py       # AI insights model
│   └── database.py      # Database configuration
├── services/
│   ├── scraper.py       # Google Maps scraping service
│   ├── llm.py           # AI/ML processing service
│   └── review.py        # Review processing service
└── app.py               # Flask application factory
```

## **🔌 API Endpoints**

### **Authentication Routes** (`/auth`)
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/login` | User authentication |
| POST | `/register` | User registration with business setup |
| POST | `/logout` | User logout |
| POST | `/refresh` | JWT token refresh |
| GET | `/user` | Get current user info |

### **User Management** (`/user`)
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/profile` | Get user profile |
| PUT | `/profile` | Update user profile |
| PUT | `/change-password` | Change user password |
| DELETE | `/account` | Delete user account |
| GET | `/business-reviews` | Get all reviews for user's businesses |
| GET | `/business-reviews/stats` | Get review statistics |

### **Business Operations** (`/business`)
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/<int:business_id>` | Get business details |
| PUT | `/<int:business_id>` | Update business information |
| DELETE | `/<int:business_id>` | Delete business |
| GET | `/<int:business_id>/rating` | Get average business rating |

### **Review Management** (`/reviews`)
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/analyze_reviews` | Analyze batch of reviews |
| GET | `/<int:business_id>` | Get filtered reviews |
| GET | `/<int:business_id>/ratings-distribution` | Get rating distribution |
| GET | `/<int:business_id>/topics-frequency` | Get topic frequency analysis |

### **Dashboard Analytics** (`/dashboard`)
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/business/<int:business_id>/summary` | Business summary metrics |
| GET | `/business/<int:business_id>/sentiment/analysis` | Sentiment analysis data |
| GET | `/business/<int:business_id>/reviews/recent` | Recent reviews |
| GET | `/business/<int:business_id>/ratings/distribution` | Rating distribution |
| GET | `/business/<int:business_id>/reviews/segments` | Review segmentation |
| GET | `/business/<int:business_id>/reviews/critical` | Critical reviews |
| GET | `/business/<int:business_id>/topics/ratings` | Topic-based ratings |
| GET | `/business/<int:business_id>/insights` | Get AI insights |
| POST | `/business/<int:business_id>/insights/generate` | Generate new AI insights |

## **🗄 Database Models**

### **User Model**
```python
- id: Primary key
- first_name: User's first name
- last_name: User's last name
- email: Unique email address
- password_hash: Hashed password
- created_at: Account creation timestamp
- businesses: Relationship to Business model
```

### **Business Model**
```python
- id: Primary key
- name: Business name
- url: Google Maps URL
- location: Business location
- business_type: Type of business
- user_id: Foreign key to User
- reviews: Relationship to Review model
```

### **Review Model**
```python
- id: Primary key
- business_id: Foreign key to Business
- source: Review platform source
- content: Review text content
- rating: Star rating (1-5)
- username: Reviewer username
- review_date_estimate: Estimated review date
- senti_score: Sentiment score (-1 to 1)
- sentiment_description: Sentiment classification
- topics: Extracted topics/entities
- is_suggestion: Boolean for improvement suggestions
```

### **Insight Model**
```python
- id: Primary key
- business_id: Foreign key to Business
- content: AI-generated insight content
- created_at: Creation timestamp
```

## **🤖 AI/ML Services**

### **Google Cloud NLP Integration**
- **Sentiment Analysis:** Analyze customer sentiment from review text
- **Entity Extraction:** Identify key topics, menu items, and business aspects
- **Language Detection:** Support for multiple languages

### **OpenRouter API Integration**
- **AI Insights Generation:** Generate business recommendations using DeepSeek LLM
- **Review Summarization:** Create concise summaries of customer feedback
- **Trend Analysis:** Identify patterns and emerging themes

### **Web Scraping Service**
- **Google Maps Integration:** Automated review extraction using Selenium
- **Smart Parsing:** Extract review metadata including ratings, dates, and usernames
- **Rate Limiting:** Respectful scraping with proper delays

## **📊 Analytics Capabilities**
- **Real-time Sentiment Tracking:** Monitor customer satisfaction trends
- **Topic-based Analysis:** Understand specific business aspects
- **Review Segmentation:** Categorize feedback for targeted improvements
- **Critical Review Detection:** Prioritize negative feedback
- **Performance Metrics:** Track ratings and review volume over time

## **🔒 Security Features**
- **JWT Authentication:** Secure token-based authentication
- **Password Hashing:** Werkzeug-based password security
- **Input Validation:** Comprehensive request validation
- **SQL Injection Prevention:** SQLAlchemy ORM protection
- **CORS Configuration:** Cross-origin request handling

## **📞 Support**
For backend-specific inquiries, please contact the development team directly.

---
*Flask backend powering intelligent restaurant analytics*

**All Rights Reserved** - This code is proprietary and confidential. Unauthorized copying, modification, distribution, or use of this software is strictly prohibited without explicit written permission from the authors.
