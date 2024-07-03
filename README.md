## install packages
- npm install @clerk/nextjs -- for authentication
- npm install lucide-react ---- lucide react icons



## libraries
- shadcn ui

## new things
- /src/middleware.js ===  publicRoutes is used for , when the user is not authenticated, then user can access only the "/"-homePath.
```
export default clerkMiddleware({
    publicRoutes: ['/'],
});
```



## problem
1. when the user is not authenticated then only `home,login,registration` items is required to show in Header. one the user is authenticated then change the header Items according to their role{candidate,recruiter}.
2. 


## Important notes
- you must create .env.local file outside the src page while you are using nextjsClerk.
- create a global loading file , then we can use this file whenever we required.   for that we are using shadcn & use skeleton component. path : /app/loading.js .
- create a `app/component/common-layout/index.js`. reason for create this file: we can organise our code in very good manner. this file container `header component` & `main content`. main component encloses using the <main>{children}</main> tag & this tag contains all the main content. & we importing this component into the `/app/layout.js` file with suspense tag.
- we are import header content directly into the common-layout file. where as main content is passing{children} from `/app/page.js` homefunction. 
- menuItems.map((menuItem)=> {no.......}),,,,, (menuItem)=> avoid curly braces
- it the `middleware.js` file , sangam-codes-{authMiddleware} , where as my code {clerkMiddleware}.

