# Firebase Chat App
Description:
- Firestore Chat App is a real-time chat application built using Firebase Firestore and Firebase Cloud Functions. This project demonstrates how to use Firestore to store and retrieve chat messages and how to use Cloud Functions for backend logic.

Features:
- Real-time messaging
- Cloud Functions for secure message handling
- Firestore database for scalable data storage

Prerequisites:
Before you begin, ensure you have met the following requirements:

- You have installed Node.js and npm.
- You have a Firebase project. If not, create one at the Firebase Console.
- You have initialized Firebase in your project.

# Getting Started
Installation: 
1. Clone the repository:
   - git clone https://github.com/your-username/firebase-functions-chat.git -> cd firestore-chat-app
     
2. Install dependencies for both the client and functions:
   - cd functions -> npm install

# Firebase Setup
- Initialize Firebase in your project using 'firebase init'.
- Choose the following options:
  - Firestore
  - Functions

# Deploy Cloud Functions
- Deploy the function using 'firebase deploy --only functions'

# Usage
1. To run the client application, ensure you have a basic HTML/JS setup or use a frontend framework of your choice.
2. Include Firebase configuration in your client application:
   - var firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT_ID.appspot.com",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID",
  measurementId: "YOUR_MEASUREMENT_ID"
};
// Initialize Firebase
firebase.initializeApp(firebaseConfig);
3. Call the addMessage function from your client application to send messages as follows:
   - var addMessage = firebase.functions().httpsCallable('addMessage');
addMessage({ text: 'Hello, world!', userId: 'user123' })
  .then(result => {
    console.log('Message sent:', result.data);
  })
  .catch(error => {
    console.error('Error sending message:', error);
  });




