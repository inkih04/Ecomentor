# 🌱 EcoMentor

**Promoting energy efficiency in Catalonia through mobile technology**

EcoMentor is a comprehensive mobile application ecosystem designed to improve building energy efficiency across Catalonia and foster sustainable lifestyles. Developed as part of the **PES (Proyectos de Ingeniería del Software)** course at FIB-UPC, this project addresses the critical need for energy efficiency awareness, considering that over 80% of existing buildings in Catalonia have energy ratings below level E.

## 📋 Project Overview

The application enables users to:

- **Interactive Building Maps**: Visualize real-time energy information of buildings across Catalonia based on official energy certificates with clustering for optimal visualization
- **Certificate Comparison**: Compare energy efficiency between different certified buildings with detailed metrics
- **Digital Pseudo-Certificates**: Generate indicative certificates through comprehensive questionnaires for uncertified buildings, calculated using official government algorithms
- **AI-Powered Sustainability Advisor**: Intelligent chatbot powered by Google Gemini providing personalized energy efficiency recommendations
- **Improvement Calculator**: Quantitative analysis of potential benefits and costs from building modifications using real energy consumption data
- **Achievement System**: Gamification features to encourage sustainable practices
- **Multi-platform Support**: Native iOS and Android apps with multi-language support (Catalan, Spanish, English)

## 🏗️ Architecture

This project follows a modern full-stack architecture with modular monolithic design:

### Frontend - [React Native Mobile App](https://github.com/inkih04/Ecomentor-front)
- **React Native** with Expo for cross-platform development
- **TypeScript** for enhanced code reliability
- **Expo Router** for file-based navigation
- **i18n** for internationalization support
- Native iOS and Android optimization

### Backend - [Spring Boot API](https://github.com/inkih04/EcoMentor-backend)
- **Java 21** with Spring Boot 3.4
- **Clean Architecture** implementation with modular monolithic design
- **PostgreSQL** with PostGIS for geospatial certificate data
- **MongoDB** for chatbot conversation storage
- **Google Gemini AI** integration for intelligent recommendations
- **JWT & OAuth2** authentication with Google Sign-In
- Comprehensive RESTful API with Swagger documentation

### Data Processing
- **1.3M+ energy certificates** from official Catalan government sources
- **Advanced algorithms** for energy efficiency calculations based on official government formulas
- **Intelligent recommendation system** analyzing real consumption patterns
- **Geospatial optimization** with clustering for map visualization

## 🚀 Quick Start

### Prerequisites
- Node.js 18+, npm or yarn
- Java 21, Maven
- Docker & Docker Compose
- Android Studio / Xcode (for mobile development)

### Running the Complete System

1. **Clone both repositories:**
   ```bash
   git clone https://github.com/inkih04/EcoMentor-backend.git
   git clone https://github.com/inkih04/Ecomentor-front.git
   ```

2. **Configure environment variables:**
   ```bash
   # Backend (.env)
   GEMINI_API_KEY=your_gemini_api_key
   SPRING_MAIL_PASSWORD=your_email_password
   
   # Frontend (.env)
   EXPO_PUBLIC_API_URL=http://localhost:8080/api
   ```

3. **Start the backend with Docker:**
   ```bash
   cd EcoMentor-backend
   docker-compose up
   ```

4. **Launch the mobile app:**
   ```bash
   cd Ecomentor-front
   npm install
   npx expo start
   ```

5. **Access the API documentation:**
   ```
   http://localhost:8080/swagger-ui.html
   ```

## 📚 Documentation & Academic Context

The `PES_22_B_Ecomentor` folder contains comprehensive project documentation and deliverables from the Software Engineering Projects course at FIB-UPC. This includes:

- **Technical specifications** and architectural diagrams
- **User requirements** and stakeholder feedback analysis
- **Sprint reports** and Scrum methodology implementation
- **Database design** and energy calculation algorithms
- **API contracts** with third-party services (Agendados, Ventus)
- **Real stakeholder validation** with Maristes Rubí high school students and teachers

Please note that some documents are in Catalan or Spanish as part of the original academic requirements.

### Key Technical Achievements
- **Advanced energy calculations** using official Spanish government algorithms
- **Real-time data processing** of 1.3M+ energy certificates from Generalitat de Catalunya
- **AI-powered recommendations** with custom algorithms analyzing building efficiency patterns
- **Geospatial optimization** with PostGIS for efficient map-based queries
- **Clean Architecture** implementation following industry best practices

## 🛠 Development Methodology

This project was developed following **Scrum methodology** with **GitFlow** for version control, ensuring structured development cycles and consistent code quality throughout the project lifecycle. Key practices included:

- **Sprint-based development** with 3 complete sprints
- **Daily standups** and retrospectives
- **Code reviews** and pull request workflows
- **Continuous Integration** with automated testing (75%+ coverage)
- **Real stakeholder feedback** integration from user testing sessions

## 👥 Contributors

This project was collaboratively developed by:

- [inkih04](https://github.com/inkih04)
- [rubenpalavacas](https://github.com/rubenpalavacas)
- [DavidSanzMartinez](https://github.com/DavidSanzMartinez)
- [PatoPro121](https://github.com/PatoPro121)
- [DidacDV](https://github.com/DidacDV)
- [LegenGiga](https://github.com/LegenGiga)

## 📱 Screenshots

<details>
<summary>📸 Click to view app screenshots</summary>

### Main Dashboard
![Main Dashboard - Map View](https://github.com/inkih04/Ecomentor/blob/main/images/mapa.png) 
![Main Dashboard - Sidebar](https://github.com/inkih04/Ecomentor/blob/main/images/sideBar.png)

### Achievements System
![Achievements](https://github.com/inkih04/Ecomentor/blob/main/images/logros.png) 

### AI-Powered Recommendations
![Recommendations](https://github.com/inkih04/Ecomentor/blob/main/images/recommendations.png) 

### Certificate Comparison Tool
![Certificate Comparison](https://github.com/inkih04/Ecomentor/blob/main/images/compare.png) 

### AI Sustainability Advisor Chat
![AI Advisor](https://github.com/inkih04/Ecomentor/blob/main/images/chat.png) 

### Improvement Calculator
![Calculator](https://github.com/inkih04/Ecomentor/blob/main/images/Calculate.png)

</details>

## 🔧 Technology Stack

### Frontend
- React Native + Expo
- TypeScript
- React Navigation + Expo Router
- Axios for API communication
- i18n for multi-language support

### Backend
- Java 21 + Spring Boot 3.4
- Spring Security & Data JPA
- PostgreSQL + PostGIS (geospatial data)
- MongoDB (chat conversations)
- Google Gemini AI
- Docker containerization

### External APIs & Services
- **Google Services**: Gmail SMTP, Maps, OAuth2, Gemini AI
- **ICGC API**: Catalan geographic coordinate services
- **Third-party integrations**: Agendados (events), Ventus (energy data sharing)

### Development Tools
- Scrum + GitFlow methodology
- JUnit 5 + Mockito (backend testing)
- Jest (frontend testing)
- Checkstyle + ESLint (code quality)
- Swagger API documentation
- GitHub Actions (CI/CD)
- AWS EC2 deployment

## 📖 API Documentation

The backend provides comprehensive RESTful APIs documented with Swagger. Access the interactive documentation at `http://localhost:8080/swagger-ui.html` when the backend is running.

## 🧪 Testing & Quality Assurance

Both frontend and backend include comprehensive test suites with 75%+ coverage:

```bash
# Backend tests (JUnit 5 + Mockito)
cd EcoMentor-backend
./mvnw test

# Frontend tests (Jest)
cd Ecomentor-front
npm test

# Code quality checks
./mvnw checkstyle:check  # Backend linting
npm run lint             # Frontend linting
```

## 🚀 Deployment

### Backend (Docker + AWS EC2)
```bash
docker build -t ecomentor-backend .
# Automated deployment via GitHub Actions to AWS EC2
```

### Frontend (Expo Application Services)
```bash
# Android APK generation
eas build --platform android --local

# iOS build
eas build --platform ios
```

## 🌍 Impact & Real-World Validation

EcoMentor contributes to Catalonia's sustainability goals by making energy efficiency information accessible and actionable for building owners and residents. The project has been validated through:

- **Real stakeholder testing** with 25+ high school students and teachers at Maristes Rubí
- **Data-driven insights** from 1.3M+ official energy certificates
- **Measurable impact calculations** showing potential savings from energy improvements
- **Scalable architecture** supporting integration with other sustainability platforms

Key findings from user validation:
- 85%+ satisfaction with core features (login, navigation, chatbot, calculator)
- Significant improvement in map visualization through clustering implementation
- High engagement with AI-powered recommendations and gamification features

---

**Building a more sustainable future, one application at a time**
