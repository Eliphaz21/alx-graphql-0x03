# ErrorBoundary Component

## Overview

This is a simple reusable Error Boundary component built with React and TypeScript. It catches errors in child components and shows a fallback UI instead of crashing the whole app.

## Features

* Catches runtime errors
* Shows a friendly error message
* Lets users try again
* Logs errors in the console

## Usage

### Import the component

```tsx
import ErrorBoundary from "./ErrorBoundary";
```

### Wrap your component

```tsx
<ErrorBoundary>
  <MyComponent />
</ErrorBoundary>
```

## How it works

* If a child component throws an error, the ErrorBoundary detects it.
* It shows a fallback message: "Oops, there is an error!"
* A "Try again?" button resets the state and re-renders the children.
* Error details are logged in the console for debugging.

## Props

* `children`: Components that should be protected from crashes.

## When to use
