# Silent Image Loading Failure in Expo Image Component

This repository demonstrates a subtle bug in Expo's `Image` component where images fail to load without providing any console errors. The issue is particularly tricky to debug because there's no readily apparent error message to pinpoint the problem.

## Problem

The `Image` component renders a blank space when provided with an invalid or inaccessible image URI.  This is problematic because it doesn't immediately alert developers of an issue; there is no error thrown in the console.

## Solution

The solution involves adding comprehensive error handling around the `Image` component. This includes using a placeholder image while waiting for the main image to load, and displaying an error message if the image fails to load.  Proper image URI validation before passing it to the component is also crucial.