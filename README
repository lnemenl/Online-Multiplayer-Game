# Online Multiplayer Pong Game

A full-stack online gaming platform featuring real-time gameplay, secure authentication, and a relational database.

![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=flat-square&logo=node.js&logoColor=white)
![Fastify](https://img.shields.io/badge/Fastify-000000?style=flat-square&logo=fastify&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

The application uses a microservices-ready monolithic architecture inside Docker containers.

* **Backend:** Node.js running Fastify. Optimized for low-overhead HTTP processing.
* **Database:** SQLite managed via Prisma ORM for efficient relational data handling.
* **Frontend:** Single Page Application (SPA) serving dynamic content.

## Key Technical Features

### Authentication & Security
* **Dual-Token Architecture:** Implements short-lived JWT Access Tokens and HTTP-only Refresh Tokens.
* **Token Rotation:** Automatic rotation of refresh tokens to detect reuse and prevent session hijacking.
* **OAuth2 Integration:** Google Identity Platform integration for passwordless onboarding.
* **2FA (Two-Factor Authentication):** TOTP-based second factor (Google Authenticator compatible) required for sensitive account actions.

### Database & User Data
The database schema is designed to handle user relationships and game statistics:
* **Social Features:** Manages Friend Requests.
* **Game History:** Stores match results and links them to player profiles.

### Testing
* **Integration Tests:** Jest test suite covering Login, Logout, and Token Refresh flows.
* **Isolated Testing:** Tests run in a clean environment to ensure accuracy.

## Application Preview

| Main Screen | Real-Time Gameplay |
|:---|:---|
| ![Google Sign In](assets/main_screen.gif) | ![Gameplay](assets/game.gif) |

| Google Sign In | Friend Request |
|:---|:---|
| ![Google Sign In](assets/google_sign_in.gif) | ![Gameplay](assets/profile_friend_request.gif) |

| Security (2FA) | 2FA in action(login) |
|:---|:---|
| ![2FA Flow](assets/set_2fa_on.gif) | ![Friend Requests](assets/2fa_in_action.gif) |

## Installation & Setup

**Prerequisites:** Docker Engine, Docker Compose.

1.  **Clone the repository**
    ```bash
    git clone https://github.com/lnemenl/Online-Multiplayer-Game.git
    cd Online-Multiplayer-Game
    ```

2.  **Configure Environment**
    Create a `.env` file based on the provided example.
    ```bash
    cp .env.example .env
    ```
    *Note: You must obtain your own `GOOGLE_CLIENT_ID` and `SECRET` from the Google Cloud Console. Ensure your Authorized Redirect URIs in Google Console match the `GOOGLE_REDIRECT_...` variables in your .env file exactly.*

3.  **Start Services**
    ```bash
    docker-compose up --build
    ```

4.  **Access the Application**

    The application runs behind a secure Nginx proxy.
    * **URL:** `https://localhost:4430`
    * *Note: You may need to accept the self-signed certificate warning in your browser.*

## Testing

To run the integration test suite:

```bash
cd backend
npm install
npm run test
