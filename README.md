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
It keeps track of whether or not the link is the active link. Works exactly as `<Link>`. However, it by default recieves an active class when the link is the current route. `<NavLink>` component is specifically meant for building components like navbars or a set of tabs where we would like to highlight it as the current selected item and provide useful context with screen reader. `<Link>` is generally used if we want to navigate to routes from other parts of the app.

### Programmatic navigation

React router provides use with `<useNavigate>` hook for navigating programmtically.

- `<useNavigate>` hook ruturns a function that we can use for this purpose.

Returned function can have two signatures:

1. Either pass a path value same as we pass to `<Link>` as "to" with an optional second {replace, state} arg. `replace` is a boolean which if set to true will replace the history in history stack and `state` can be data or state you want to pass to the next page you are routing to.

2. Pass a number to indicate a change in the history stack. eg,. passing (-1) is equivalent to hitting the back button.

### No Match Route

If user tries to navigate to a page which does not exist or is not loaded for some reason, in that case to handle such a situation, we can use symbol \* as the path and direct user to a custom component or page.
eg,. `<Route path="*" element={<NoMatch />}></Route>`

### Nested Routes

We first create main component and configure the route for same. We then configure the inner routes as nested inside this main component using `<Route>` component. Child component path will automatically have parent path as prefix. But, parent component doesn't know what to do with these child components in the routes tree. And for that we use `<Outlet/>` component from 'react-router-dom' which renders the component corresponding to the matching child route from the parent list of routes.

### Index routes

When we have nested routes inside a route and we want one of the nested routes to be rendered at the parent url we can use index route. Just specify index attribute instead of path inside the `<Route>` and the element to be rendered.

### Dynamic Routes

If the route parameters can vary in value, we can make use of dynamic routes. We can specify a url param denoted by a colon prefix in the path.
React router will always try to match the route which is more specific before trying to match a dynamic route. We can also nest the dynamic routes.
