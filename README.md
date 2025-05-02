Video Game Tournament Management with ReactJS 🎮
Project Context
Following the development of the API dedicated to managing video game tournaments, we designed this front-end application in ReactJS. This application allows users to:

View all tournaments 🏆

Access match details ⚽

Register and track the real-time progress of competitions ⏱️

The goal is to create a smooth, modern, and intuitive user interface, ensuring seamless integration with the backend API while focusing on performance and responsiveness.

Architecture and Tools 🛠️
Communication with the Backend API
Axios/Fetch API: For making requests to the backend API.

JWT (JSON Web Token): For authentication management and securing private routes.

Security and Authentication
Token Management: Securely storing authentication tokens via localStorage or cookies.

Interception Middleware: Automatically adding tokens to HTTP requests.

Application Structure
1. Authentication 🔐
Components & Pages
Registration: Form allowing a user to register via the API [POST] /api/register.

Login: Login form to retrieve an access token via [POST] /api/login.

Logout: Button to delete the token and redirect the user to the login page.

Profile: Displaying user information via [GET] /api/user.

2. Tournament Management 🏅
Components & Pages
Tournament List: Displays all tournaments via [GET] /api/tournaments.

Tournament Details: Page detailing a specific tournament via [GET] /api/tournaments/{id}.

Create & Edit: Forms for creating or editing a tournament via [POST] /api/tournaments and [PUT] /api/tournaments/{id}.

Delete: Action to delete a tournament via [DELETE] /api/tournaments/{id}.

3. Player Registration 📝
Features
Register for a Tournament: Form to register a player for a tournament via [POST] /api/tournaments/{tournament_id}/players.

Player List: Displays the players registered for a tournament.

Unregister: Option to unregister a player via [DELETE] /api/tournaments/{tournament_id}/players/{player_id}.

4. Match and Score Management 🏅
Components & Pages
Create Match: Interface to schedule a match between players via [POST] /api/matches.

Match List and Details: Displays scheduled matches via [GET] /api/matches and details of a specific match via [GET] /api/matches/{id}.

Update Scores: Form to add or modify scores via [PUT] /api/matches/{id}/scores or [POST] /api/matches/{id}/scores.

