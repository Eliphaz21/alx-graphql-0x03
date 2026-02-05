ErrorBoundary Component (React + TypeScript)
📌 Overview

This project contains a reusable Error Boundary component built with React and TypeScript.
It helps prevent the entire app from crashing by catching JavaScript errors in the component tree and displaying a fallback UI instead.

🚀 Features

Catches runtime errors in child components

Displays a user-friendly fallback message

Allows users to retry rendering

Logs error details to the console for debugging

Written in TypeScript for type safety

📂 Component Code

This component uses React’s class-based lifecycle methods:

getDerivedStateFromError

componentDidCatch

These methods detect and handle errors in child components.

🧠 How It Works

If any child component throws an error:

getDerivedStateFromError sets hasError = true

The UI switches to a fallback screen

The error details are logged using componentDidCatch

User can click "Try again?" to reset the state

📦 Usage
1️⃣ Import the component
import ErrorBoundary from "./ErrorBoundary";

2️⃣ Wrap your components
<ErrorBoundary>
  <MyComponent />
</ErrorBoundary>

🛠 Props
Prop	Type	Description
children	ReactNode	Components to be protected by the Error Boundary
📊 State
State	Type	Description
hasError	boolean	Tracks if an error has occurred
💥 Fallback UI

When an error occurs, users will see:

Error message

Retry button to reset the error state

🔍 Error Logging

Errors are logged in the console using:

componentDidCatch(error, errorInfo)


This helps developers debug issues.

📁 File Structure
ErrorBoundary.tsx
README.md

🧪 Best Use Cases

Wrap: