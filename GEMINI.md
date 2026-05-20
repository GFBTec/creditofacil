# Project: Microcrédito Inteligente (creditofacil)

## Overview
**Microcrédito Inteligente** is a lightweight, pure client-side web application designed for requesting and managing microcredit. It provides a simple flow for applicants to submit their data and a dashboard for administrators to track and update the status of these requests.

### Main Technologies
- **Frontend:** HTML5, Vanilla JavaScript.
- **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN).
- **Icons:** [Lucide Icons](https://lucide.dev/) (via CDN).
- **Typography:** [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts.
- **State Management:** Browser `localStorage` for data persistence.

---

## Project Structure
- `index.html`: The main landing page and entry point of the application.
- `solicitacao.html`: The applicant's entry point. Contains a multi-step form to collect solicitor and guarantor information.
- `painel-admin.html`: The administrative dashboard (accessible via `/painel-admin`). Allows viewing all requests, filtering by status, updating statuses, and managing a "financial box" (caixa).
- `README.md`: Basic project introduction.

---

## Building and Running
This project does not require a build step or a backend server.

### Running Locally
1.  Open `index.html` in any modern web browser to view the landing page.
2.  Click "Solicitar Crédito Agora" to go to the application form (`solicitacao.html`).
3.  Access `painel-admin.html` (or `/painel-admin` on supported servers) to reach the management dashboard.

*Note: For the best experience (e.g., auto-refresh), it is recommended to use a local development server like the VS Code "Live Server" extension or run `npx serve .` in the root directory.*

---

## Development Conventions
- **Language:** The user interface and code comments/variables are primarily in **Portuguese (pt-BR)**.
- **State Persistence:** All data is stored under the `localStorage` key `microcredito_solicitacoes`. The financial state is stored under `microcredito_financeiro`.
- **Tailwind CSS:** Styling is handled using utility classes directly in the HTML. Avoid large custom CSS files unless necessary; prefer Tailwind classes.
- **Modularity:** While currently contained within single HTML files, JavaScript logic is organized into functions for rendering, state updates, and event handling.

---

## TODO / Future Improvements
- [ ] Implement a backend/API for centralized data storage.
- [ ] Add authentication for the `painel-admin.html` page.
- [ ] Modularize JavaScript into separate `.js` files.
- [ ] Set up a build process (e.g., Vite) for better asset management and minification.
