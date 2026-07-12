# EatWell

<div align="center">
  <img src="screenshots/screenshot9.png" alt="EatWell app preview" width="920" />
  <br />
  <br />
  <p><strong>AI-powered nutrition and calorie tracking with food recognition, barcode scanning, and personalized dietary guidance.</strong></p>
  <p>
    <img src="https://img.shields.io/badge/.NET-9-512BD4?style=for-the-badge&logo=dotnet" alt=".NET 9" />
    <img src="https://img.shields.io/badge/React_Native-Expo-61DAFB?style=for-the-badge&logo=react" alt="React Native Expo" />
    <img src="https://img.shields.io/badge/Mistral_AI-Vision_Focused-F7DF1E?style=for-the-badge" alt="Mistral AI" />
    <img src="https://img.shields.io/badge/PostgreSQL-Docker-336791?style=for-the-badge&logo=postgresql" alt="PostgreSQL Docker" />
  </p>
</div>

EatWell is a next-generation nutrition assistant that reduces manual calorie logging and turns everyday meals into actionable insights. Take a photo of your food, scan a barcode, and let AI estimate macros, allergens, and smart dietary recommendations in seconds.

## Highlights

- **AI vision food analysis**: uploads meal photos to **Mistral AI (Pixtral-12B)** and returns estimated calories, protein, carbohydrates, and fats.
- **Instant barcode scanning**: uses **OpenFoodFacts** to fetch packaged food nutrition data and ingredients.
- **Smart allergen alerts**: checks user allergens against scanned or photographed foods and surfaces clear warnings.
- **AI dietitian chat**: gives contextual answers based on the current food, daily goals, and allergy profile.
- **Clean, responsive UI**: built with **React Native**, **Expo**, and a glassmorphism-inspired visual style.

## Visual Tour

<div align="center">
  <table>
    <tr>
      <td><img src="screenshots/screenshot3.png" alt="Food analysis result" width="100%" /></td>
      <td><img src="screenshots/screenshot9.png" alt="AI analysis in progress" width="100%" /></td>
    </tr>
    <tr>
      <td><img src="screenshots/screenshot10.png" alt="Barcode scanner" width="100%" /></td>
      <td><img src="screenshots/screenshot11.png" alt="Nutrition details" width="100%" /></td>
    </tr>
  </table>
</div>

<div align="center">
  <table>
    <tr>
      <td><img src="screenshots/screenshot1.png" alt="Home screen" width="100%" /></td>
      <td><img src="screenshots/screenshot2.png" alt="App screen" width="100%" /></td>
      <td><img src="screenshots/screenshot4.png" alt="Feature screen" width="100%" /></td>
    </tr>
    <tr>
      <td><img src="screenshots/screenshot5.png" alt="Tracking view" width="100%" /></td>
      <td><img src="screenshots/screenshot6.png" alt="Daily progress" width="100%" /></td>
      <td><img src="screenshots/screenshot7.png" alt="Detailed insight" width="100%" /></td>
    </tr>
    <tr>
      <td><img src="screenshots/screenshot8.png" alt="Additional screen" width="100%" /></td>
      <td><img src="screenshots/screenshot10.png" alt="Barcode scanner detail" width="100%" /></td>
      <td><img src="screenshots/screenshot11.png" alt="Nutrition summary" width="100%" /></td>
    </tr>
  </table>
</div>

## Architecture

EatWell follows **Clean Architecture** principles to keep the codebase maintainable and easy to extend.

### Backend

- **Domain**: core entities such as `CalorieGoal`, `DailyLog`, and `UserAllergen`
- **Application**: use cases, interfaces, DTOs, and business workflows
- **Infrastructure**: Entity Framework Core, PostgreSQL, and the Mistral AI client
- **API**: REST endpoints for the mobile application

### Mobile App

- **Framework**: React Native with Expo
- **Capabilities**: camera, image picker, and barcode scanning
- **Styling**: custom UI system with modern glassmorphism-inspired surfaces
- **Networking**: centralized API requests with `axios`
- **Device connectivity**: dynamic Expo server IP discovery for easier local development

### DevOps

- **Docker** and **Docker Compose** for backend and database containerization

## Getting Started

### Backend

1. Open the `eatwellfeelwell` directory.
2. Add your **Mistral API key** in `appsettings.json`.
3. Run the backend with Docker Compose or the .NET CLI.

```bash
docker-compose up -d --build

# or
dotnet run
```

### Frontend

1. Open the `EatWellMobile` directory.
2. Install dependencies.

```bash
npm install
```

3. Start the Expo app.

```bash
npx expo start
```

4. Open **Expo Go** on your phone and scan the QR code.

## Project Structure

```text
EatWell/
|-- eatwellfeelwell/   # Backend solution
|-- EatWellMobile/     # React Native app
|-- screenshots/       # README images
`-- docker-compose.yml # Backend + database orchestration
```

## About The Developers

Developed as a graduation project at **Tekirdag Namik Kemal University, Computer Engineering Department** by **Melih Esen** and **Tarik Gezici**, under the supervision of **Dr. Ahmet Saygili**.

*We believe health tracking should feel intelligent, fast, and beautiful.*
