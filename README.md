# Expo Go: Asynchronous Operation Error After Component Unmount

This repository demonstrates a common error in React Native applications using Expo Go, where asynchronous operations (e.g., network requests) cause problems after a component unmounts. This often leads to crashes or unexpected behavior.

## Bug Description:
The bug occurs when an asynchronous operation initiated within a component continues after the component is unmounted.  React Native's state updates or property accesses after unmounting result in errors because the component no longer exists in the DOM.

## Solution:
The solution involves using cleanup functions within the component's lifecycle methods (such as `useEffect`) to cancel or abort the asynchronous operation when the component unmounts.  This prevents further actions on the now-unmounted component.

## How to Reproduce:
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Start the Expo Go app and scan the QR code.
4. Observe the error after navigating away from the screen containing the buggy component.  
