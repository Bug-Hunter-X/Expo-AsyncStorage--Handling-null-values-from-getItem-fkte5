# Expo AsyncStorage: Handling null values from getItem

This repository demonstrates a common error when using AsyncStorage in Expo applications. The problem arises from the fact that AsyncStorage.getItem() returns null if the requested key doesn't exist, which can lead to unexpected crashes if not handled correctly.  This example shows the problem and offers a robust solution.

## Problem
The primary issue lies in the lack of explicit error handling when retrieving data from AsyncStorage.  If the key doesn't exist, JSON.parse() will throw an error, leading to application crashes.

## Solution
The provided solution uses a simple check to see if the value is null before attempting to parse it. This ensures that no errors occur when handling non-existent keys.

## How to run
1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install the dependencies.
4. Run `expo start` to start the development server.