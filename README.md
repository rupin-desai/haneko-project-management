🌸 Haneko: Where work takes root and blossoms.A full-stack project management and collaboration platform designed to streamline workflows, enhance team productivity, and bring clarity to complex projects. Haneko provides a centralized hub for tasks, discussions, and progress tracking, making it an ideal solution for agile teams and modern businesses.✨ Features✅ Core FeaturesProject Management: Create, update, and manage multiple projects within a single workspace.Task Tracking: Assign tasks, set deadlines, define priorities (Low, Medium, High), and monitor status (To-Do, In Progress, Done).Custom Dashboards: Personalized views for users to see their assigned tasks, upcoming deadlines, and project notifications.User Authentication: Secure user registration and login system using JWT (JSON Web Tokens).🤝 CollaborationTeam Workspaces: Invite members to projects and assign roles (e.g., Admin, Member, Viewer).Task Comments: Real-time discussion threads on individual tasks to keep conversations organized and contextual.File Attachments: Upload and attach relevant files and documents directly to tasks.🔔 NotificationsReal-Time Alerts: Instant in-app notifications for task assignments, status changes, and new comments.Email Notifications (Optional): Integration with an email service to send summaries and critical alerts.🔧 Technical FeaturesRESTful API: A well-structured backend API built with Spring Boot for clear, scalable, and maintainable logic.Role-Based Access Control (RBAC): Granular permissions system to ensure users can only access and modify authorized data.CI/CD Pipeline: Automated build, test, and deployment pipeline using GitHub Actions for seamless integration and delivery.Containerized Environment: Fully containerized with Docker for consistent development, testing, and production environments.🛠️ Tech StackCategoryTechnologiesFrontendBackendDatabaseInfra & DevOps📁 Project Structurehaneko/
├── 📁 haneko-client/      # Next.js Frontend
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
├── 📁 haneko-server/      # Spring Boot Backend
│   ├── src/main/java/com/haneko/
│   ├── pom.xml
│   └── ...
├── 🐳 docker-compose.yml   # Docker configuration
├──  nginx/                # Nginx configuration
│   └── default.conf
└── .github/
    └── workflows/          # GitHub Actions CI/CD pipeline
        └── deploy.yml
🚀 Getting StartedPrerequisitesDocker and Docker ComposeNode.js v18+ and npmJava 17+ and Maven1. Clone the Repositorygit clone [https://github.com/your-username/haneko.git](https://github.com/your-username/haneko.git)
cd haneko
2. Environment VariablesCreate .env files for both the client and server based on the provided .env.example files.haneko-client/.envhaneko-server/.envUpdate the database credentials, JWT secret, and other necessary configurations.3. Running with Docker (Recommended)This method starts the frontend, backend, database, and Nginx reverse proxy in one go.docker-compose up --build
The application will be available at http://localhost.4. Manual Installation (Without Docker)Backend (Spring Boot)# Navigate to the server directory
cd haneko-server

# Install dependencies and build the project
mvn clean install

# Run the application
mvn spring-boot:run
The backend server will start on http://localhost:8080.Frontend (Next.js)# Navigate to the client directory in a new terminal
cd haneko-client

# Install dependencies
npm install

# Run the development server
npm run dev
The frontend will be available at http://localhost:3000.🔒 Security & DeploymentJWT Authentication: The API is secured using JSON Web Tokens. The token is generated upon login and must be included in the Authorization header for all protected requests.HTTPS/SSL: In production, Nginx is configured as a reverse proxy to handle incoming traffic, manage SSL termination, and serve the application over HTTPS.CI/CD: The GitHub Actions workflow automates the deployment process. On every push to the main branch, the workflow builds and tests the application, creates Docker images, and deploys the new versions to the Hostinger VPS.📸 Screenshots & Demo(Here you can add screenshots of your application. Use relative paths if you store images in the repo.)Dashboard ViewTask Details Modal📄 LicenseThis project is licensed under the MIT License. See the LICENSE file for more details.👨‍💻 Author[Your Name]A passionate full-stack developer with a focus on creating modern, scalable, and user-friendly web applications.