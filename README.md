# WebSocket Video Call Application

## Objective

The WebSocket Video Call application allows users to join a video call server, enabling real-time video communication. The primary objective is to provide a platform for users to engage in video calls over WebSocket connections with basic controls for managing the call.

## Functionalities and Features

### Joining a Call
- **Join Call**: Users can join a video call by clicking the "Join Call" button.
- **Username Prompt**: Users are prompted to enter their name to join the call.
- **Welcome Message**: Upon joining a server, users receive a welcome message.

### Video Call Interaction
- **Starting a Video Call**: Users can initiate a video call upon joining a server.
- **Video Display**: Local and remote video streams are displayed in the video call section.
- **Call Controls**: Users have options to mute/unmute their microphone and end the call.

### Server and Call Management
- **Local Storage**: Server information is stored locally using the browser's localStorage.
- **Persistent Servers**: Users can view previously created servers when loading the application.

## Program Structure

### HTML Structure
- **Layout Sections**: The HTML file contains sections for joining a server and the video call interface.
- **Input Fields and Buttons**: It includes an input field for the username and buttons for joining the call, muting/unmuting, and ending the call.

### JavaScript Structure
- **WebSocket Connection**: Establishes a WebSocket connection with the server at `ws://localhost:8080`.
- **WebRTC Setup**: Functions are defined for handling video call setup using WebRTC, including accessing local media and managing peer connections.
- **Event Listeners**: Event listeners are set for user interactions like joining a server and controlling the video call (mute/unmute, end call).

## Code Documentation

### Functions

#### joinCall()
```javascript
function joinCall() {
    // Function to join the video call by entering a username
    // Initializes the WebSocket connection and sets up the video call interface
}

function startVideoCall() {
    // Function to start the video call
    // Accesses local media (camera and microphone) and sets up WebRTC peer connection for the video call
}

function endCall() {
    // Function to end the video call
    // Closes the WebRTC connection and resets the video call interface
}

function toggleMute() {
    // Function to mute or unmute the user's microphone
    // Toggles the audio track enabled state
}

function handleKeyPress(event) {
    // Event handler for handling keypress events, specifically for form submissions on Enter key press
}

socket.onopen = function() {
    // Handles WebSocket connection confirmation
}

socket.onmessage = function(message) {
    // Receives and processes incoming messages related to video call signaling
}

socket.onerror = function(error) {
    // Handles WebSocket errors
}

window.onload = function() {
    // Event listener to set up initial event listeners when the window loads
}

