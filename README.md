# React Router Catch-All Route Conflict

This repository demonstrates a common issue encountered when using React Router's catch-all route (`/*`). The `/*` route, intended to handle 404 errors, can conflict with other routes if not carefully positioned.  This conflict results in the catch-all route always being rendered, overriding any other valid route matches.

The `App.js` file contains the buggy code. The `AppSolution.js` contains the corrected version.

## Bug Description

The problem stems from the order and placement of routes within the `<Routes>` component.  The catch-all route (`/*`) should always be the last route defined to ensure it only handles paths not matched by other routes.