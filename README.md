# React-Router

## What is React Router?

- Fully-featured client and server-side routing library for React
- Helps Create and navigate between different URLs that make up web applications
- Provides unique URLs for different components in the app and makes the UI easily shareable with other users.

### Components of React Router

`<BrowserRouter>` imported from 'react-router-dom'

- It allows us to use all the features from react router within the app component tree. It generally wraps aroung the App component.

`<Routes>`
- Both `<Routes>` and `<Route>` need to be imported from 'react-router-dom'
- Primary way to render something in React Router based on the current location. `<Routes>` can have multiple `<Route>` components which will each link to a different route if present. `<Route>` elements can be nested inside other `<Route>` elements.
