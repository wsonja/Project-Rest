# **TableTalk**             
*A Full-Stack B2B SaaS Platform for Restaurant Review Intelligence*  

<div align="center" style="background-color: white;">
  <img src="frontend/public/logowtext.png" alt="TableTrackLogo"/>
  <img src="https://github.com/user-attachments/assets/05facea7-2acd-4e3e-b57f-9bf70fa7fb23" alt="TableTalkLogo" width="800"/>
</div>


## **📌 Overview**
TableTalk is a **comprehensive B2B SaaS solution** that transforms scattered customer reviews into actionable business intelligence for restaurant owners. By leveraging **AI-powered analysis, automated web scraping, and intelligent dashboards**, TableTrack helps restaurants understand customer feedback, identify improvement opportunities, and make data-driven decisions to enhance their business performance.

## **🎯 Problem Statement**
Restaurant owners highly value customer feedback, especially from Google Reviews, but this feedback is often:
- Scattered across multiple platforms
- Difficult to analyze at scale
- Time-consuming to extract actionable insights
- Hard to track trends and performance metrics

## **💡 Solution**
TableTalk solves these challenges by providing:
- **Automated review aggregation** from Google Maps and other platforms
- **AI-powered sentiment analysis** and entity extraction using Google Cloud NLP
- **Real-time performance dashboards** with comprehensive analytics
- **Actionable AI insights** generated using advanced language models

## **🛠 Key Features**

### **Core Analytics**
✅ **Smart Review Classification** – Automatically categorize reviews by sentiment and topics  
✅ **AI-Powered Sentiment Analysis** – Real-time customer satisfaction tracking using Google Cloud NLP  
✅ **Multi-Platform Aggregation** – Automated scraping from Google Maps with Selenium  
✅ **Entity Extraction** – Identify key topics, menu items, and business aspects  

### **Dashboard & Visualization**
✅ **Comprehensive Analytics Dashboard** – Visualize all reviews in one centralized platform  
✅ **Performance Metrics Tracking** – Monitor rating trends, review volume, and sentiment over time  
✅ **Review Segmentation** – Categorize reviews into segments (Highly Positive, Critical, Suggestions)  
✅ **Custom Reporting** – Generate detailed reports for any time period  

### **Business Intelligence**
✅ **AI-Generated Insights** – Automated business recommendations using DeepSeek LLM  
✅ **Topic-Based Ratings** – Track performance across specific business aspects  
✅ **Critical Review Detection** – Identify and prioritize negative feedback  
✅ **Rating Distribution Analysis** – Understand customer satisfaction patterns  

### **User Management**
✅ **JWT Authentication** – Secure user registration and login system  
✅ **Multi-Business Support** – Manage multiple restaurant locations per user  
✅ **Profile Management** – Update user information and business details  
✅ **Account Security** – Password change and account deletion features  

## **📐 Tech Stack**

| **Layer**           | **Technology** |
|---------------------|----------------|
| **Frontend**        | React.js, Tailwind CSS |
| **Backend**         | Python Flask, SQLAlchemy |
| **Database**        | PostgreSQL/MySQL |
| **AI & NLP**        | Google Cloud Natural Language API, DeepSeek V3 |
| **Web Scraping**    | Selenium WebDriver, BeautifulSoup |
| **Authentication** | Flask-JWT-Extended |
| **API Integration** | OpenRouter API |
| **Deployment**      | TBD (AWS/Google Cloud Platform) |

## **🏗 System Architecture**

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   React.js      │    │   Flask API      │    │   Google Cloud  │
│   Dashboard     │◄──►│   Server         │◄──►│   NLP API       │
└─────────────────┘    └──────────────────┘    └─────────────────┘
                                │
                                ▼
                       ┌──────────────────┐
                       │   Selenium       │
                       │   Web Scraper    │
                       └──────────────────┘
                                │
                                ▼
                       ┌──────────────────┐
                       │   PostgreSQL     │
                       │   Database       │
                       └──────────────────┘
```

## **📅 Development Roadmap**

- **Phase 1:** Research & Market Analysis (✅ **Completed**)
- **Phase 2:** Core Backend Development & API Integration (✅ **Completed**)
- **Phase 3:** AI/ML Model Development & Training (✅ **Completed**)
- **Phase 4:** Frontend Dashboard Development (🔄 **In Progress**)
- **Phase 5:** Beta Testing & User Feedback (🔜 **Upcoming**)
- **Phase 6:** Production Deployment & Launch (🔜 **Upcoming**)

## **📊 Key Metrics & Performance**
- **Automated review scraping** from Google Maps using Selenium
- **Real-time sentiment analysis** with Google Cloud NLP
- **AI-powered insights** generation using DeepSeek LLM
- **Comprehensive dashboard** with 8+ analytics endpoints

## **🎯 Target Market**
- **Primary:** Independent restaurant owners (1-10 locations)
- **Secondary:** Restaurant chains and hospitality businesses
- **Tertiary:** Food service management companies

## **🔐 Security & Compliance**
- JWT-based authentication system
- Secure password hashing with Werkzeug
- Environment-based configuration management
- Input validation and SQL injection prevention

## **👥 Team**

| **Name**            | **Role**              | **NetID** | **GitHub**    |
|--------------------|-----------------------|-----------|---------------|
| **Ahmed Abdulla**   | Team Lead  | aaa384    | [@ahmed-52](https://github.com/ahmed-52) |
| **Farhan Mashrur**  | Team Lead  | fm454     | [@fm454](https://github.com/farhan-439) |
| **Arsh Singh**      | Developer  | as4274    | [@Arsh-S](https://github.com/Arsh-S) |
| **Saesha Agarwal**  | Developer  | as4274    | [@Arsh-S](https://github.com/Arsh-S) |
| **Sonja Wong**      | Developer  | as4274    | [@Arsh-S](https://github.com/wsonja) |
| **Daniel Khanin**   | Developer  | as4274    | [@Arsh-S](https://github.com/saeshaagarwal) |
| **Arianna Hsu**     | Developer  | as4274    |  |

## **📄 License**
**All Rights Reserved** - This code is proprietary and confidential. Unauthorized copying, modification, distribution, or use of this software is strictly prohibited without explicit written permission from the authors.

## **📞 Contact & Support**
- **Email:** support@tabletalk.com
- **Documentation:** [docs.tabletalk.com](https://docs.tabletalk.com)

---
*Built with ❤️ for the restaurant industry*
