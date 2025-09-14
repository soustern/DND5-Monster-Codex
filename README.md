# DnD 5e Monster Codex

A mobile-first web application that allows users to search and visualize information about monsters from the Dungeons & Dragons 5th Edition API. The interface is designed for clarity and a streamlined user experience, presenting complex data in an organized and aesthetically pleasing manner.

**[Live Demo](https://dnd-5-monster-codex-fsuu6cic3-soustern.vercel.app/)**

---

## Key Features

*   **Dynamic Search:** Instantly search the complete D&D 5e monster database.
*   **Detailed Views:** Clean, readable cards present all monster stats, abilities, and lore.
*   **Responsive Design:** A mobile-first approach ensures a seamless experience on any device.

## Tech Stack

*   **Frontend:** JavaScript (ES6+), SASS (7-1 pattern), HTML5 (BEM methodology)
*   **Backend:** Python with Flask (for routing and serving the application)
*   **Build Tools:** NPM (for package management and custom scripts)
*   **Deployment:** Vercel

## Technical Highlights

This project was an opportunity to implement and deepen my understanding of several key web development concepts:

*   **JavaScript:** Responsible for asynchronous API communication (`fetch`), dynamic DOM manipulation to render data, and user input handling.
*   **SASS:** Leveraged advanced features like variables, mixins, and `extends`, organized using the 7-1 architecture pattern for scalable and maintainable CSS.
*   **HTML:** Written with a focus on semantic markup and structured with BEM naming conventions for clear, reusable components.
*   **Flask:** Used as a lightweight micro-framework to handle routing and serve the front-end, enabling a simple and fast development environment.

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

*   npm
    ```sh
    npm install npm@latest -g
    ```
*   Python 3.x and Pip

### Installation

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/soustern/dnd_5_monster.codex.git](https://github.com/soustern/DND5-Monster-Codex.git
    ```
2.  **Navigate to the project directory:**
    ```sh
    cd DND5-Monster-Codex
    ```
3.  **Install NPM packages:**
    ```sh
    npm install
    ```
4.  **Install Flask:**
    ```sh
    pip3 install Flask
    ```
5.  **Run the application:**
    *   Compile SASS and start the Flask server with the custom NPM scripts.
    ```sh
    # In one terminal, compile SASS and watch for changes
    npm run sass
    
    # In another terminal, start the development server
    npm run dev
    ```

## Challenges & Learnings

During deployment to Vercel, I encountered HTTP 500 errors when loading large image assets. I diagnosed this as a performance bottleneck and resolved the issue by implementing an image compression strategy. This not only fixed the deployment error but also significantly improved the application's load times and overall performance.

## Future Improvements

*   **Component-Based Refactoring:** Refactor the JavaScript code into modular components to improve organization and reusability.
*   **Accessibility (A11y) Enhancements:** Conduct an audit and implement ARIA attributes and other best practices to improve accessibility for screen readers and keyboard navigation.
*   **Client-Side Routing:** Transition from the Flask-based routing to a client-side solution to create a true Single Page Application (SPA) experience.
