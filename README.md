# React-Router

## What is React Router?

- Fully-featured client and server-side routing library for React
- Helps Create and navigate between different URLs that make up web applications
- Provides unique URLs for different components in the app and makes the UI easily shareable with other users.

### Components of React Router

`<BrowserRouter>` imported from 'react-router-dom'

- It allows us to use all the features from react router within the app component tree. It generally wraps aroung the App component.

`<Routes>`

- Primary way to render something in React Router based on the current location. Routes can have multiple `<Route>` components which will each link to a different route if present. `<Route>` elements can be nested inside other `<Route>` elements.

`<Link>` -> imported from 'react-router-dom'
Helps us to navigate to another route. We specify a `to` prop to which we assign the path of configured route.
eg., `<Link to="/">`Home`<Link>`

`<NavLink>` --> imported from 'react-router-dom'
It keeps track of whether or not the link is the active link. Works exactly as `<Link>`. However, it by default recieves an active class when the link is the current route.
