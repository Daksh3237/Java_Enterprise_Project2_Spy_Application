# Spy Mission Management Application

This is a Spring Boot application designed to manage spy missions. Users can create, edit, and view missions, and assign specific agents with various gadgets for each mission. The app is built using Thymeleaf templates for the front-end, and data is stored in an H2 in-memory database.

## Table of Contents

- [Project Description](#project-description)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Database Details](#database-details)
- [License](#license)

## Project Description

This application allows users to create and manage spy missions. Each mission is assigned to an agent and includes details like gadgets and mission titles. The missions can be edited, deleted, and filtered by agent. This project demonstrates the use of Spring Boot for building robust backend services and Thymeleaf for front-end rendering.

## Features

- Create new missions
- Edit or delete existing missions
- Assign agents to missions from a predefined list
- Input and display gadgets for each mission
- View missions filtered by agent

## Technologies Used

- **Spring Boot** - Framework for backend development
- **Spring MVC** - For handling requests and responses
- **Thymeleaf** - Templating engine for rendering dynamic HTML pages
- **H2 Database** - In-memory database for storing mission details
- **Lombok** - Simplifies Java coding by removing boilerplate code

## Setup Instructions

To run the project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/spy-mission-management.git
   cd spy-mission-management
   
2. **Import the project**:
- Import it into your IDE as a Maven project.
  
3. **Run the application**:
- In your IDE, run the HomeController class as a Spring Boot application.
  
4. **Access the application**:
Once the application is running, open your browser and go to http://localhost:8080/.

## Usage
- **Home Page**: From the home page, you can either create a new mission or view missions by agent.
- **Create Mission**: Click on "Create a Mission" to fill in mission details like the title, agent, and gadgets.
- **Edit Mission**: From the mission list, click "Edit" to modify mission details.
- **Delete Mission**: Click "Delete" to remove a mission from the list.
- **View Missions**: Select an agent from the dropdown to filter missions by that agent.

## Database Details
- The application uses an H2 in-memory database. The data is reset each time the application is restarted.
- The default H2 console is available at http://localhost:8080/h2-console.
- Use the following details to log in:
  - **JDBC URL**: jdbc:h2:mem:testdb
  - **Username**: sa
  - **Password**: (leave it blank)

 ## Sample Data
By default, the following missions are pre-populated:
 - **Johnny English**: Rescue the Queen (Gadgets: Exploding Cigar, Voice Controlled Rolls Royce)
 - **Natasha Romanova**: Kill Iron Man (Gadgets: Armored Suit, Indestructible Pole)
 - **Austin Powers**: Deactivate the bomb (Gadgets: Knife, Bomb Detector)

## SQL Table Creation
```bash
   CREATE TABLE mission (
     id LONG PRIMARY KEY AUTO_INCREMENT,
     agent VARCHAR(50),
     title VARCHAR(50),
     gadget1 VARCHAR(50),
     gadget2 VARCHAR(50)
   );




