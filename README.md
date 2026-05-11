# vr-radish

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

An interactive 3D radish character demo built with Three.js, `@pixiv/three-vrm`, and WebXR for augmented reality.

[**Live Demo**](https://code4fukui.github.io/vr-radish/)

## Demos

This repository contains two distinct demonstrations:

### 1. AR Walking Radish (`index.html`)

This is the main demo, featuring a radish character that walks in a circle.

-   **AR Mode:** Use the "START AR" button on a compatible device to place the radish in your environment.
-   **3D View:** On desktop, you can interact with the scene using orbit controls (drag to rotate, scroll to zoom).
-   **Animation:** The radish's limbs and neck are animated programmatically to create a walking motion.

### 2. Mouse Interaction (`mouse.html`)

A simpler scene demonstrating direct interaction with the VRM model's skeleton.

-   **Mouse Control:** The radish model's hips (`hips` bone) will follow the position of your mouse cursor on the screen.

## How to Run Locally

To run these demos on your own machine, you need to serve the files from a local web server.

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/code4fukui/vr-radish.git
    cd vr-radish
    ```

2.  **Start a local server:**
    If you have Python 3 installed, you can use its built-in HTTP server:
    ```sh
    python -m http.server
    ```
    Alternatively, use any other simple server tool like `npx serve`.

3.  **Open in your browser:**
    -   Navigate to `http://localhost:8000/index.html` for the AR demo.
    -   Navigate to `http://localhost:8000/mouse.html` for the mouse interaction demo.

## Technology & Credits

-   **Rendering:** [Three.js](https://threejs.org/)
-   **VRM Loading:** [@pixiv/three-vrm](https://pixiv.github.io/three-vrm/)
    -   [Documentation](https://pixiv.github.io/three-vrm/packages/three-vrm/docs/)
-   **Models:**
    -   `Yamakoshi_radish01.vrm`
    -   `VRM1_Constraint_Twist_Sample.vrm` (available in code)

## License

This project is available under the MIT License.