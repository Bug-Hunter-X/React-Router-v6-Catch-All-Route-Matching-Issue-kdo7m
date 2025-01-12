# React Router v6 Catch-All Route Bug

This repository demonstrates a subtle bug in React Router v6's handling of catch-all routes (`/*`). When a catch-all route is present alongside more specific routes, it unexpectedly matches even when a more specific route should be used. This can lead to unexpected rendering and navigation issues.

## Issue Description

The problem occurs when you define both specific routes (e.g., `/`, `/about`) and a catch-all route (`/*`). The catch-all route should only be used as a last resort.  However, in this case, it sometimes intercepts requests intended for the other routes.

## Reproduction

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe that navigating to `/` or `/about` works as expected, but the `NotFound` component is unexpectedly shown.

## Solution

The solution is provided in the `AppSolution.js` file.