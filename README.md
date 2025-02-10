# React Router Dom v6 Unexpected Navigation Behavior
This repository demonstrates an uncommon bug in React Router Dom v6 where navigation using Links sometimes fails to update the UI correctly.  The URL updates, but the component does not render.

## Bug Description
The navigation between routes using 
`<Link>` components intermittently fails to update the UI, despite the URL correctly reflecting the intended route change.

## Reproduction
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate between the Home and About pages using the links. Observe that sometimes the UI doesn't reflect the correct page, although the URL in the browser shows the change.

## Solution
The solution involves ensuring that the component rendering the route (App in this example) re-renders upon URL changes.  This can be achieved through several techniques including using a state variable, context API, or other state management solutions. The solution provided utilizes a state variable. 