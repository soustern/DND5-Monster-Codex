# D&D 5e Monster Codex

[![Deployment](https://img.shields.io/badge/Deployment-Vercel-black?logo=vercel)](https://vercel.com/)
[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-black?logo=flask)](https://flask.palletsprojects.com/)
[![SASS](https://img.shields.io/badge/Sass-CC6699?logo=sass)](https://sass-lang.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

The D&D 5e Monster Codex is a full-stack web application that serves as a dynamic, searchable compendium for Dungeons & Dragons 5th Edition monsters. Built with a lightweight Python/Flask backend and a powerful vanilla JavaScript frontend, this project is a showcase of building a rich, data-driven user interface from the ground up without relying on any frontend frameworks.

**✨ [View the Live Demo](https://dnd-5-monster-codex-fsuu6cic3-soustern.vercel.app/)**

![Monster Codex Demo](https://i.imgur.com/example.gif) <!-- Optional: Create a GIF of your app and upload it to a site like imgur.com to showcase it here -->

---

## Technical Highlights & Architectural Decisions

This application was architected to be robust, maintainable, and performant, demonstrating a full-stack skill set and best practices in both frontend and backend development.

### 1. Scalable SASS Architecture (7-1 Pattern)
The project's styling is architected using the highly organized **7-1 SASS pattern**. This methodology divides the entire SASS codebase into seven logical directories (`abstracts`, `base`, `components`, etc.), ensuring maximum maintainability and scalability.
- **`abstracts`:** Contains all variables, mixins, and extends, acting as a "single source of truth" for the design system.
- **BEM Naming Convention:** The HTML structure uses the Block-Element-Modifier methodology (e.g., `.c-sheet__info--general`), creating a clear and strict relationship between markup and styles.
- **Maintainability:** This approach prevents CSS bloat, makes styles predictable, and simplifies the process of adding or refactoring UI components.

### 2. Asynchronous Data Handling with Vanilla JavaScript
All data fetching and rendering is handled asynchronously with the `fetch` API and modern `async/await` syntax.
- **Dynamic DOM Construction:** Upon receiving a response from the D&D 5e API, the application dynamically constructs the entire monster stat block by creating and appending dozens of DOM elements. This showcases intricate, from-scratch DOM manipulation and state management—a task typically abstracted away by frameworks.
- **Data Sanitization:** A helper function (`format_value`) sanitizes user input to be API-compatible, ensuring robust queries.
- **Graceful UI Updates:** The DOM is cleared and rebuilt for each new search, with smooth CSS transitions that create a fluid user experience.

### 3. Lightweight Backend & Serverless Deployment
The backend and deployment strategies were chosen for efficiency and modernity.
- **Flask Microframework:** Python with Flask serves as a simple yet effective backend, responsible for routing and rendering the initial HTML template. This demonstrates a separation of concerns between the server and the client.
- **Vercel Serverless Deployment:** The Flask application is deployed on Vercel, leveraging a **serverless architecture**. The Python backend is configured to run as a serverless function, providing a scalable and cost-effective hosting solution that highlights experience with modern cloud platforms.

### 4. Problem-Solving & Performance Optimization
During the initial deployment, large image assets from the API were causing HTTP 500 errors on Vercel. I successfully diagnosed this as a timeout/performance bottleneck and implemented a manual image compression strategy for the project's own assets. This proactive optimization not only resolved the critical deployment issue but also significantly improved the application's overall load time and performance.

## Tech Stack

| Category | Technology / Methodology |
|---|---|
| **Backend** | Python, Flask |
| **Frontend** | Vanilla JavaScript (ES6+) |
| **Styling** | SASS (7-1 Pattern), BEM |
| **Markup** | Semantic HTML5 |
| **Build Tools** | NPM Scripts, node-sass |
| **Deployment**| Vercel (Serverless) |

## Project Structure

The codebase is organized with a focus on professional development patterns, including the Flask standard `static`/`templates` convention and the SASS 7-1 pattern.

```
/
├── sass/                 # SASS source files (7-1 Pattern)
│   ├── abstracts/
│   ├── base/
│   ├── components/
│   └── ...
├── static/               # Compiled assets served by Flask
│   ├── css/
│   └── js/
├── templates/            # HTML templates rendered by Flask
├── app.py                # Main Flask application file
├── package.json          # NPM dependencies and scripts
├── requirements.txt      # Python dependencies for pip
└── vercel.json           # Vercel deployment configuration
```

## Local Development Setup

To get a local copy up and running, follow these steps.

### Prerequisites

*   Node.js and npm
*   Python 3.x and Pip

### Installation & Execution

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/soustern/dnd_5_monster_codex.git
    cd dnd_5_monster_codex
    ```
2.  **Install dependencies:**
    ```bash
    # Install Node.js packages
    npm install
    
    # Install Python packages
    pip install -r requirements.txt
    ```
3.  **Run the application:**
    You will need two separate terminal windows.

    *   **In Terminal 1 (SASS compiler):**
      This command will compile your SASS to CSS and watch for any changes.
      ```bash
      npm run compile:sass
      ```

    *   **In Terminal 2 (Flask Server):**
      This command will start the local Flask development server.
      ```bash
      npm run compile:flask
      ```

The application will now be running on your local machine, typically at `http://127.0.0.1:5000`.

## License

This project is licensed under the MIT License.
