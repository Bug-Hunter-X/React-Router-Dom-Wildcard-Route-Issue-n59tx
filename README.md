# React Router Dom Wildcard Route Issue

This repository demonstrates a subtle bug in React Router Dom v6 related to wildcard routes. When a wildcard route (`/*`) is a direct child of the `Routes` component, it fails to match even when no other routes match. This behavior is unexpected and can lead to a non-functional 404 page.

## Issue Description

The problem occurs when using nested routes with a wildcard. The wildcard route never gets executed, even when no other routes match the requested path.  The solution provides a correction to resolve this issue. 

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to any non-existent path. You will see that the 404 page will not render.

## Solution

The solution involves changing the route structure and adding a catch-all route higher up to correctly handle unmatched paths.