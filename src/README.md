Line 156 is where the main App begins. Inside the Router but before our first Route, is the nav links and header. There are two routes, the first being the home page Route which contains the Home component.  The second Route has the base Route of Categories and contains the CategoryList component/function. The reason there are only these two Routes is because the CategoryList component uses nested Routes.

Line 124 we use the useRouteMatch hook to grab the url and path to use for nested routes. 
Line 136 is a nested link which uses the url from useRouteMatch to append the category to the link
Line 145 is a nested path which is where we essentially define the path that we want to match. In this case, we append the category id to the path

The benefit of using nested paths in a single page application is to reduce the number of network calls made to fetch and render the requested information. The information is fetched on the first request and is then cached locally for later use.