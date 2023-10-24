# Smart Home Control System

This project is a Smart Home Control System for controlling and monitoring your smart home devices effortlessly. This project consists of both frontend and backend components, allowing users to manage various devices through an intuitive interface.

## Table of Contents
- [Smart Home Control System](#smart-home-control-system)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Frontend](#frontend)
    - [`app.js`](#appjs)
    - [`index.js`](#indexjs)
    - [`mySwitch.js`](#myswitchjs)
  - [Backend](#backend)
    - [Some Components](#some-components)
      - [GPIO 1 \& GPIO 2](#gpio-1--gpio-2)
      - [All Off](#all-off)
      - [Fan](#fan)
      - [Fan Off](#fan-off)
      - [Fan Timer](#fan-timer)
      - [Laptop](#laptop)
      - [Laptop Off](#laptop-off)
  - [Features](#features)
  - [Technologies](#technologies)
    - [Frontend](#frontend-1)
    - [Backend](#backend-1)
  - [Getting Started](#getting-started)
  - [Usage](#usage)
  - [Contributing](#contributing)

## Introduction

This project is a combination of frontend and backend components that allows you to control various home appliances using a React-based user interface and GPIO pins. The frontend provides an interactive dashboard for users to manage devices, while the backend handles the actual control of GPIO pins.

## Frontend
The frontend of the project is built using React and Material-UI. It features a user-friendly dashboard for controlling different appliances.

### `app.js`
App.js is the core React component that powers the frontend. It manages the state and user interface, enabling users to control and monitor their home devices effectively. It fetches device states and updates them dynamically.
Notable components and features include:
- Toggles for controlling devices like lights, fans, and more.
- Timer functionality for managing the operation of a fan.
- Responsive design for various screen sizes.
- Stylish UI with dynamic updates based on device states.

### `index.js`
index.js serves as the entry point for rendering the React app. It renders the main App component and manages the app's entry point within the application root element.

### `mySwitch.js`
MySwitch.js is a custom Material-UI Switch and reusable React component representing on/off switches. It provides a visually appealing and functional UI element for controlling devices that enhance the user experience.


## Backend

This part of the project focuses on the backend components that facilitate controlling various devices or relays using GPIO pins. Each relay corresponds to a specific appliance, and the backend provides control functions for turning them on and off. The backend is built using JavaScript and utilizes the onoff library to manage GPIO pins for turning devices on and off.
Notable components and functions include:

- GPIO pin control using the `onoff` library.
- Relay control functions for turning on/off specific appliances.
- Timer functionality to set a duration for the fan's operation.
- A `package.json` configuration for managing the backend application.

### Some Components

The backend consists of several components, each responsible for controlling specific devices.

#### GPIO 1 & GPIO 2

These components control a set of GPIO pins to manage multiple LEDs. It turns them off initially and unexports them after use.

#### All Off

This component turns off all configured relays by setting their respective GPIO pins to GPIO.HIGH.

#### Fan

This component turns on the fan relay by setting its GPIO pin to GPIO.LOW.

#### Fan Off

This component turns off the fan relay by setting its GPIO pin to GPIO.HIGH.

#### Fan Timer

This component allows setting a timer for the fan to automatically turn off after a specified duration. The timer duration is passed as a command-line argument in the format <number> <time_unit>, e.g., 5 minutes.

#### Laptop

This component turns on the laptop relay by setting its GPIO pin to GPIO.LOW.

#### Laptop Off

This component turns off the speaker relay by setting its GPIO pin to GPIO.HIGH.

## Features

- **Device Control**: Turn devices on and off with GPIO pins, providing seamless control.
- **Timer Functionality**: Set timers for devices to automate their usage and save energy.
- **Intuitive UI**: User-friendly frontend interface for easy navigation and control.
- **Modularity**: Reusable components and organized backend for scalability and maintainability.

## Technologies

### Frontend

- **React**: A JavaScript library for building user interfaces.
- **Material-UI**: A popular React UI framework for creating elegant and responsive applications.

### Backend

- **Node.js**: A JavaScript runtime for executing server-side code.
- **Express**: A fast, unopinionated, and minimalist web framework for Node.js.
- **GPIO (General Purpose Input/Output)**: Pins on Raspberry Pi that control device power state (HIGH for off, LOW for on).



## Getting Started

To get started with this project, follow these steps:

1. Clone the repository.
2. Set up the frontend and backend components on your system.
3. Configure the GPIO pins to match your hardware setup.
4. Run the frontend and backend applications.
5. Use the provided dashboard to control your appliances.

## Usage

The frontend communicates with the backend to trigger actions based on user interactions. Explore the dashboard to control lights, fans, and other appliances. Set timers for the fan and enjoy a convenient home automation experience.

## Contributing

Contributions to this project are welcome. If you have improvements, bug fixes, or new features to add, follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Commit your changes.
5. Create a pull request.
