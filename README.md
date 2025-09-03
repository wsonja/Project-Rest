# **TableTalk**             
*A Full-Stack B2B SaaS Platform for Restaurant Review Intelligence*  

<div align="left" style="background-color: white;">
  <a href="https://github.com/user-attachments/assets/05facea7-2acd-4e3e-b57f-9bf70fa7fb23">
    <img src="frontend/public/logowtext.png" alt="TableTalkLogo" width="150"/>
  </a>
  ← Video
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

## Features

### Core Analytics
- **Smart Review Classification**: Categorize reviews by sentiment and topic  
- **AI-Powered Sentiment Analysis**: Track customer satisfaction with Google Cloud NLP  
- **Multi-Platform Aggregation**: Scrape Google Maps using Selenium  
- **Entity Extraction**: Identify key topics, menu items, and business aspects  

### Dashboard & Visualization
- **Analytics Dashboard**: Centralized view of all reviews  
- **Performance Metrics Tracking**: Monitor rating trends, review volume, and sentiment over time  
- **Review Segmentation**: Segment reviews into Highly Positive, Critical, and Suggestions  


### Business Intelligence
- **AI-Generated Insights**: Business recommendations powered by DeepSeek LLM  
- **Topic-Based Ratings**: Track performance across specific aspects of the business  
- **Critical Review Detection**: Highlight and prioritize negative feedback  
 


## **🏗 System Architecture**

```
┌─────────────────────┐    JWT Auth     ┌─────────────────────┐    API Calls    ┌─────────────────────┐
│      Frontend       │    + REST API   │     Backend API     │                 │    External APIs    │
│   React.js +        │◄───────────────►│   Flask +           │◄───────────────►│                     │
│   Tailwind CSS      │                 │   SQLAlchemy        │                 │  ┌───────────────┐  │
│                     │                 │                     │                 │  │ Google Cloud  │  │
│ ┌─────────────────┐ │                 │ ┌─────────────────┐ │                 │  │ NLP API       │  │
│ │ Dashboard UI    │ │                 │ │ Auth Service    │ │                 │  │ • Sentiment   │  │
│ │ Analytics       │ │                 │ │ Business Logic  │ │                 │  │ • Entities    │  │
│ │ Review Mgmt     │ │                 │ │ Dashboard APIs  │ │                 │  └───────────────┘  │
│ └─────────────────┘ │                 │ └─────────────────┘ │                 │                     │
└─────────────────────┘                 └─────────────────────┘                 │  ┌───────────────┐  │
                                                   │                             │  │ OpenRouter    │  │
                                                   │                             │  │ (DeepSeek V3) │  │
                                                   │                             │  │ • AI Insights │  │
                                                   │                             │  │ • Summary     │  │
                                                   ▼                             │  └───────────────┘  │
                                        ┌─────────────────────┐                 └─────────────────────┘
                                        │   Data Processing   │                            │
                                        │     Pipeline        │                            │
                                        └─────────────────────┘                            │
                                                   │                                       │
                                                   ▼                                       │
┌─────────────────────┐    Web Scraping ┌─────────────────────┐    Raw Data    ┌─────────────────────┐
│     Data Sources    │◄────────────────│   Scraping Layer   │───────────────►│    Database Layer   │
│                     │                 │                     │                 │                     │
│ ┌─────────────────┐ │                 │ ┌─────────────────┐ │                 │ ┌─────────────────┐ │
│ │ Google Maps     │ │                 │ │ Selenium        │ │                 │ │ PostgreSQL/     │ │
│ │ Review Pages    │ │                 │ │ WebDriver       │ │                 │ │ MySQL           │ │
│ │                 │ │                 │ │ • Rate Limiting │ │                 │ │                 │ │
│ └─────────────────┘ │                 │ │ • Smart Parsing │ │                 │ │ ┌─────────────┐ │ │
│                     │                 │ └─────────────────┘ │                 │ │ │   Tables    │ │ │
│ ┌─────────────────┐ │                 │                     │                 │ │ │ • Users     │ │ │
│ │ Other Review    │ │                 │ ┌─────────────────┐ │                 │ │ │ • Business  │ │ │
│ │ Platforms       │ │                 │ │ BeautifulSoup   │ │                 │ │ │ • Reviews   │ │ │
│ │ (Future)        │ │                 │ │ • HTML Parsing  │ │                 │ │ │ • Insights  │ │ │
│ └─────────────────┘ │                 │ │ • Data Cleaning │ │                 │ │ └─────────────┘ │ │
└─────────────────────┘                 │ └─────────────────┘ │                 │ └─────────────────┘ │
                                        └─────────────────────┘                 └─────────────────────┘
```


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

| **Name**            | **Role**             |  **GitHub**    |
|--------------------|-----------------------|---------------|
| **Ahmed Abdulla**   | Team Lead  | [@ahmed-52](https://github.com/ahmed-52) |
| **Farhan Mashrur**  | Team Lead  | [@farhan-439](https://github.com/farhan-439) |
| **Sonja Wong**      | Developer  | [@wsonja](https://github.com/wsonja) |
| **Arsh Singh**      | Developer  | [@Arsh-S](https://github.com/Arsh-S) |
| **Saesha Agarwal**  | Developer  | [@saeshaagarwal](https://github.com/saeshaagarwal) |
| **Daniel Khanin**   | Developer  | [@Danikk-392](https://github.com/Danikk392) |

## **📄 License**
**All Rights Reserved** - This code is proprietary and confidential. Unauthorized copying, modification, distribution, or use of this software is strictly prohibited without explicit written permission from the authors.


---
*Built as a project by Cornell Data Strategy*
