# Synchronize 3D Scenes Across Multiple Windows with Three.js

![Three.js Logo](https://threejs.org/files/logo.png)

[![Download Release](https://img.shields.io/badge/Download%20Release-v1.0.0-blue.svg)](https://github.com/FraDaquo/multipleWindow3dScene/releases)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [How It Works](#how-it-works)
- [Usage](#usage)
- [Demo](#demo)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

This repository contains a simple example of how to synchronize a 3D scene across multiple browser windows using Three.js and localStorage. The goal is to demonstrate how you can maintain a consistent view of a 3D scene, regardless of how many windows you open. 

You can find the latest releases [here](https://github.com/FraDaquo/multipleWindow3dScene/releases). Download the latest version and execute it to see the synchronization in action.

## Features

- **Real-time Synchronization**: Updates in one window reflect in all other open windows.
- **Lightweight**: Minimal code to achieve synchronization, making it easy to understand and modify.
- **Three.js Integration**: Leverages the powerful Three.js library for rendering 3D graphics.
- **Cross-Platform**: Works on any modern web browser that supports localStorage.

## Getting Started

To get started with this project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/FraDaquo/multipleWindow3dScene.git
   cd multipleWindow3dScene
   ```

2. **Install Dependencies**:
   Make sure you have Node.js installed. Run the following command to install any necessary dependencies:
   ```bash
   npm install
   ```

3. **Run the Application**:
   Use a local server to run the application. You can use a simple server like `http-server`:
   ```bash
   npx http-server
   ```
   Open your browser and navigate to `http://localhost:8080`.

4. **Open Multiple Windows**:
   Open the same URL in multiple windows or tabs to see the synchronization in action.

## How It Works

The synchronization mechanism relies on the browser's localStorage. When an event occurs in one window (like moving an object), it updates localStorage. Other windows listen for changes in localStorage and update their scenes accordingly.

### Key Components

- **Three.js**: This library handles the rendering of the 3D scene.
- **localStorage**: This is used to store the state of the scene across different windows.
- **Event Listeners**: Each window listens for changes to localStorage and updates the scene in real-time.

## Usage

To customize the 3D scene, you can modify the following components:

- **Scene Objects**: Change the geometries, materials, and textures in the scene.
- **Camera Settings**: Adjust the camera position and perspective to get different views.
- **Lighting**: Experiment with different light sources to enhance the visual quality.

### Example Code Snippet

Here is a simple example of how to update the position of a cube in the scene:

```javascript
function updateCubePosition(x, y, z) {
    cube.position.set(x, y, z);
    localStorage.setItem('cubePosition', JSON.stringify({ x, y, z }));
}
```

## Demo

To see a live demo of this project, please visit the [Demo Page](https://github.com/FraDaquo/multipleWindow3dScene/releases). 

You can also download the latest version from the releases section and execute it to explore the synchronization feature.

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, feel free to fork the repository and submit a pull request.

### Steps to Contribute

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/YourFeature
   ```
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or suggestions, feel free to reach out via GitHub issues or directly through my [GitHub Profile](https://github.com/FraDaquo).

For more information, visit the releases section [here](https://github.com/FraDaquo/multipleWindow3dScene/releases). Download the latest version and explore the synchronization of 3D scenes across multiple windows.