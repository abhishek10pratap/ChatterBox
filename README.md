'''# Chat App (Backend-Focused)

This is a real-time chat application built using Flask and Flask-SocketIO, providing real-time communication between users in different chat rooms.

## Backend Features

- **Flask-based API** for handling chat room creation and user interactions.
- **WebSockets with Flask-SocketIO** for real-time bi-directional messaging.
- **Room-based chat functionality**, allowing multiple chat rooms.
- **Session management** to track users and rooms.
- **Scalability support** for deploying in production with Gunicorn and eventlet/gevent.
-

## Technologies Used

- **Flask**: Micro web framework for backend development.
- **Flask-SocketIO**: Real-time WebSocket communication.
- **Python**: Core backend logic.
- **SQLite / MySQL (Optional)**: Database support for chat logs and user data.


## Project Structure

```
app.py  # Main Flask application
requirements.txt  # Dependencies list
README.md  # Project documentation
static/
    css/
        room.css  # Chat room styling
        style.css  # General styling
    home.css  # Home page styling
templates/
    base.html  # Base HTML template
    home.html  # Home page template
    room.html  # Chat room template
```  

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/chat-app.git
    cd chat-app
    ```

2. Create and activate a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate  
    ```

3. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

## Running the Application

1. Start the Flask server:
    ```sh
    python app.py
    ```

2. Open `http://127.0.0.1:5000` in your browser to access the app.

## Backend Functionality

- **Socket Events**:
  - `@socketio.on('connect')`: Handles new WebSocket connections.
  - `@socketio.on('disconnect')`: Handles user disconnections.
  - `@socketio.on('join_room')`: Allows users to join a chat room.
  - `@socketio.on('send_message')`: Broadcasts messages to the appropriate room.

- **HTTP Routes**:
  - `GET /`: Renders the home page.
  - `GET /chat/<room>`: Loads the chat room.
  - `POST /create_room`: (Optional) API endpoint for room creation.
  - `POST /store_message`: (Optional) Saves messages to a database.

## Future Enhancements

- **Database Storage**: Store chat history for persistence.
- **User Authentication**: Implement login/logout for users.
- **Message Encryption**: Secure chat messages with encryption.
- **Scalable Deployment**: Host on a cloud provider with Gunicorn and Nginx.'''

 

