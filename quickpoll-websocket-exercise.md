# QuickPoll: Real-time Quiz System Using WebSockets

This exercise demonstrates how WebSockets enable real-time interactive applications where immediate bidirectional communication is essential. By building a simplified quiz system, you'll gain practical experience with a technology that powers many modern web applications.

## Introduction

WebSockets provide a persistent, bidirectional communication channel between clients and servers, unlike traditional HTTP requests. While HTTP follows a request-response pattern (like making a phone call, asking a question, and hanging up each time), WebSockets maintain an open connection (like keeping the phone line open for an ongoing conversation). This makes WebSockets ideal for applications requiring real-time updates and interactions.

## Task: Build a Live Quiz System

Create a simplified live quiz system similar to popular classroom quiz platforms. This system will demonstrate the power of WebSockets by enabling real-time interaction between a host and multiple participants.

## What Makes This a WebSocket Project

This project cannot be implemented effectively with traditional HTTP requests because:
1. Updates must be pushed instantly to all connected users
2. The server needs to broadcast events (like new questions or timer updates) without clients requesting them
3. Real-time feedback requires immediate bidirectional communication
4. Maintaining game state across multiple clients requires synchronized connections

## Requirements

### Core Components

1. Create a WebSocket server in Python that:
   - Manages quiz sessions
   - Broadcasts questions to all participants
   - Processes answers in real-time
   - Updates and shares leaderboards

2. Create two simple web interfaces:
   - Host view (for displaying questions and results)
   - Player view (for joining and answering)

### Required Features

1. **Session Management**
   - Generate a unique session code for each quiz
   - Allow players to join using the code
   - Track connected players

2. **Quiz Flow**
   - Host can start the quiz
   - Questions display simultaneously for all participants
   - 10-second countdown timer for each question
   - Players submit answers before time expires
   - Show results after each question

3. **Real-time Interaction**
   - Display who has answered in real-time
   - Update leaderboard instantly after each question
   - Show correct answer with basic animation

### WebSockets in Python

For this exercise, you'll use the `websockets` library in Python to:

1. Create a server that maintains connections with multiple clients
2. Send messages between the host and players without requiring new requests
3. Broadcast events to all connected clients simultaneously
4. Handle asynchronous events using Python's `asyncio`

The implementation should use message types (like 'create_session', 'join_session', 'new_question', etc.) to handle different game events.

### Key Components to Implement

**Server-Side (Python)**

- Session management (creating and joining quiz sessions)
- Broadcasting questions to all connected players
- Processing answers as they arrive in real-time
- Updating and sending leaderboard information

**Client-Side (Basic HTML/JavaScript)**

- Connecting to the WebSocket server
- Sending player actions (joining, answering)
- Receiving and displaying real-time updates
- Showing timers, questions, and results

## Example Flow

1. Host creates a new quiz session and receives a session code
2. Players join using the session code and enter their names
3. Host starts the quiz
4. All players simultaneously see the first question with a countdown
5. Players select their answers
6. After time expires or all players answer, results are shown to everyone
7. Leaderboard updates in real-time
8. Process repeats for each question

## Bonus Features

If time allows, implement these additional features:

1. Basic animations for correct/incorrect answers
2. Sound effects for events (new question, time running out)
3. Player avatars or icons
4. "Players still answering" real-time indicator
5. Question timer synchronization across devices

## Reflection Questions

After completing the implementation, answer these questions:

1. How does WebSocket communication differ from traditional HTTP requests?
2. Why is real-time communication essential for this application?
3. What challenges did you encounter when synchronizing game state across multiple clients?
4. How would you scale this application to handle hundreds of simultaneous players?
5. What security considerations should be addressed in a WebSocket application?