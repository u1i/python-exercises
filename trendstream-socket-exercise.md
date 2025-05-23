# TrendStream: Real-time Trend Tracker

This exercise demonstrates how socket programming enables networked applications by creating a practical, engaging system that processes continuous data streams - a fundamental concept in network programming and distributed systems.

## Introduction

Socket programming enables network communication between applications running on different devices or processes. Unlike simple file operations or local function calls, sockets allow programs to send and receive data across networks using protocols like TCP and UDP. TCP sockets provide reliable, ordered data transmission - perfect for applications that need consistent communication.

This exercise will help you understand how socket programming enables real-time networked applications by building a trending topic tracker entirely in Python using the built-in `socket` library.

## What Is Socket Programming?

Traditional programs work with local data and functions. Socket programming extends this by allowing programs to communicate over networks:
- TCP sockets create persistent connections between client and server
- Data can be sent and received in both directions
- Multiple clients can connect to a single server
- The server can broadcast information to all connected clients
- Communication happens in real-time without polling

Think of it like a telephone system - the server is like a switchboard operator who can talk to multiple callers (clients) simultaneously and relay information between them.

## Task: Build a Trending Topics Tracker

Create a Python-based system with two components:
1. A TCP socket server that broadcasts trending topic data
2. A terminal client that connects to the server and displays filtered trends

## Why This Requires Socket Programming

This project demonstrates socket programming's value because:
- The server pushes trend updates to clients without being asked
- Multiple clients can receive the same broadcast simultaneously
- The persistent TCP connection allows instant updates
- Clients don't need to repeatedly request new data

## Requirements

### Server Component

Create a Python TCP socket server that:

- Accepts multiple client connections simultaneously
- Generates trending topics across multiple categories (Music, Games, Fashion, Celebrities, Memes, etc.)
- Updates trend scores randomly every few seconds
- Broadcasts the complete dataset to all connected clients
- Handles client disconnections gracefully
- Runs continuously using threading or async programming

### Client Component

Create a Python terminal client that:

- Connects to the TCP socket server
- Allows users to subscribe/unsubscribe to categories
- Filters incoming data based on subscriptions
- Displays only the selected categories' trends
- Shows simple ASCII animations for trending changes
- Maintains a clean, readable terminal interface

## Example User Experience

```
=== TRENDSTREAM CONNECTED ===
Categories: [M]usic, [G]ames, [F]ashion, [C]elebs, [T]ech, [A]ll, [Q]uit

>> M
Subscribed to Music! Watching trends...

🔥 #Taylor89Tour: 2,453 ⬆️
📈 #NewJeansComeback: 1,289 ⬆️
⚡ #GRAMMYSnub: 865 ⬇️

>> T
Now watching Music, Tech

🔥 #Taylor89Tour: 2,512 ⬆️
💻 #AI_Fashion: 1,723 ⬆️ 
📈 #NewJeansComeback: 1,302 ⬆️
📱 #iPhone17Leak: 945 ⬇️
```

## Implementation Guide

### Server Side

- Use Python's built-in `socket` library
- Create a TCP socket server that accepts connections
- Use threading to handle multiple clients simultaneously
- Generate random trend data and scores
- Periodically update trend scores using timers
- Broadcast updates to all connected clients
- Format data as JSON for easy parsing
- Handle client disconnections without crashing

### Client Side

- Use Python's `socket` library to connect to the server
- Create a simple terminal UI for category selection
- Store user's category subscriptions locally
- Listen for incoming data on a separate thread
- Filter incoming JSON data based on subscriptions
- Display filtered trends with simple formatting
- Show changes in trend popularity (up/down arrows)

## Learning Objectives

Through this exercise, you will learn:
- How TCP socket programming enables networked applications
- Implementing client-server architecture in Python
- Managing multiple concurrent connections using threading
- Broadcasting data from server to multiple clients
- Client-side filtering of server broadcasts
- Basic terminal UI techniques
- Error handling in network programming

## Bonus Features

If time allows, add these enhancements:
- Color coding in the terminal output
- Sorting trends by popularity
- "Hot trend" alerts for rapid increases
- Simple charts using ASCII art
- Historical tracking of trend changes
- Reconnection logic for dropped connections

## Reflection Questions

After completing the implementation, answer these questions:
1. How does socket programming enable real-time communication between programs?
2. What challenges did you encounter when working with multiple client connections?
3. How might this system be extended to handle thousands of concurrent users?
4. What other applications could benefit from this client-server socket approach?
5. How does the client-side filtering approach affect server performance?
6. What are the differences between TCP and UDP sockets, and why did we choose TCP?