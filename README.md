# Meet App

## Overview

For the fifth major project of my online web development course I was tasked with building a serverless, progressive web app with React using a test-driven development technique. It uses the Google Calendar API to fetch upcoming events.

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

### View it live [HERE](https://name-javi.github.io/meet/)

## Technologies:

- React
- Google Calendar API

## Key Features:

- Filters events by city
- Ability to show/hide event details
- Ability to specify number of events shown
- Ability to use the app while offline
- Ability to view a chart showing number of upcoming events by city

## User Stories/Scenarios

### **1. Feature: Filter Events by City**

**User Story:** As a user, I should be able to filter events by city so that I can see a list of events that take place in that particular city.

- **Scenario 1:** When user hasn’t searched for a city, show upcoming events from all cities.

  - **Given** user hasn't searched for any city
  - **When** user opens app
  - **Then** user should see a list of all upcoming events

- **Scenario 2:** User should see a list of suggestions when they search for a city.

  - **Given** the main page is open
  - **When** user starts typing in the city textbox
  - **Then** user should see a list of cities that match what they've typed

- **Scenario 3:** User can select a city from the suggested list.
  - **Given** user was typing "Berlin" in city textbox and list of suggested cities is showing
  - **When** user selects a city from the list
  - **Then** their city should be changed to that city and the user should recieve list of upcoming events in that city

### **2. Feature: Show/Hide Event Details**

**User Story:** As a user, I should be able to "press a button to show/hide an event's details" so that I can get more details about a specific event or hide them.

- **Scenario 1:** An event element is collapsed by default.

  - **Given** user is browsing main page of events
  - **When** user is scrolling through events
  - **Then** user will not see specific details of events

- **Scenario 2:** User can expand an event to see its details.

  - **Given** user is browsing main page of events
  - **When** user clicks on a specific event
  - **Then** user will get an expanded view of event with more details

- **Scenario 3:** User can collapse and event to hide its details.
  - **Given** user is reading details about specific event
  - **When** user clicks to close event details
  - **Then** the event details will collapse

### **3. Feature: Specify Number of Events Shown**

**User Story:** As a user, I should be able to specify the number of events that show up on the page so that I can limit the number of events that load at once or choose to load more.

- **Scenario 1:** When user hasn't specified a number, 32 is the default number.

  - **Given** user opens app and has not changed settings
  - **When** user is browsing events page
  - **Then** the specific number of events to load will be 32 by default

- **Scenario 2:** User can change the number of events they want to see.
  - **Given** user opens app to browse events
  - **When** user changes settings to load less/more than 32 events
  - **Then** the main events page will reflect that change

### **4. Feature: Use App When Offline**

**User Story:** As a user, I should be able to use the app while offline so that I can still see events in my previously selected location without an internet connection.

- **Scenario 1:** Show cached data when there is no internet connection.

  - **Given** user wants to browse app
  - **When** user browses main events page with no internet connection
  - **Then** user will still be able to browse cached data

- **Scenario 2:** Show error when user changes the settings (city, time range).
  - **Given** user wants to browse app
  - **When** user tries to change settings such as city or time range with no internet connection
  - **Then** user receives an error stating those settings cannot be changed without an internet connection

### **5. Feature: Data Visualization**

**User Story:** As a user, I should be able to see a chart with the number of upcoming events in each city so that I can see at a glance which cities have more/less events than others.

- **Scenario 1:** Show a chart with the number of upcoming events in each city.
  - **Given** user wants to compare number of events in different cities
  - **When** user clicks to see data visualization of number of events in a city
  - **Then** user sees a chart indicating number of events
