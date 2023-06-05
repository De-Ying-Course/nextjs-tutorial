## Next.js Tutorial

[Switch to Vietnamese Document](https://github.com/De-Ying-Course/nextjs-tutorial/blob/main/README-VI.md)

Next.js has recently become the official React framework as outlined in the React documentation. In this course, you'll learn the most important Next.js concepts and how they fit into the React ecosystem. Finally, you'll test your skills by building a modern full-stack Next 13 application.

📚 In this project, you'll learn:

- Next.js 13 App Folder Structure
- Next.js 13 Client Components vs Server Components
- Next.js 13 File-based Routing (including dynamic and nested routes)
- Next.js 13 page, layout, loading, and error Special Files
- Next.js 13 Serverless Route Handlers (Next API, Full Stack Apps)
- Next.js 13 Metadata and Search Engine Optimization (SEO)
- Three ways to fetch data in Next.js:
  - Server Side Rendering (SSR),
  - Static Site Generation (SSG)
  - Incremental Static Generation (ISR)

## Contents of the Sections

### The Benefits of Next.js

<details>
    <summary><b>What does Next.js have that React doesn't?</b></summary>
    <br /><p>+ Next.js simplifies the development process</p>
    <p>+ On top of that it optimizes your web apps</p>
</details>

<details>
    <summary><b>Explore the features of Next.js</b></summary>
    <details>
        <summary><b>Rendering</b></summary>
        <details>
            <summary><b>What is client-side and server-side rendering?</b></summary>
            <ul>
                <li>Client-side rendering or browser rendering is when a user requests a web page the server sends a basic HTML document and JS code the browser then downloads and executes the JS code which leads to rendering of components and finally the display of the website</li>
                <li>Server-side rendering involves rendering the web page on the server before transmitting it to the client's device when a user requests a page the server processes the request and renders components on the server-side the server then sends back the fully rendered HTML to the client's browser enabling immediate display</li>
                <li>This distinction highlights an essential aspect of Web Development SEO (Search Engine Optimization)</li>
            </ul>
        </details>
        <details>
            <summary><b>What is SEO?</b></summary>
            <ul>
                <li>SEO aka search engine crawlers face difficulties indexing Page dynamically rendered on the client-side as a result</li>
                <li>The SEO performance of such pages may suffer as search engines may not fully comprehend their content and rank them appropriately by utilizing Next.js</li>
                <li>This issue is resolved by sending pre-rendered code directly to the client. This crawling and indexing by search engines leading to the improved SEO</li>
            </ul>
        </details>
        <details>
            <summary><b>Why should I prioritize SEO?</b></summary>
            <ul>
                <li>SEO is crucial for optimizing a website's visibility and ranking in search engine results by focusing on SEO</li>
                <li>You can achieve several benefits, including: increased organic traffic, exhanced user experience, credibility & trustworthiness, competitive advantage due to higher search result rankings</li>
                <li>Prioritizing SEO can greatly impact the success of your website and it's online presence </li>
            </ul>
        </details>
    </details>
    <details>
        <summary><b>Routing</b></summary>
         <details>
              <summary><b>How do we create different page routes in React?</b></summary>
              <ul>
                  <li>We have to install an additional package called react-router-dom and then create routes in one of the files</li>
              </ul>
          </details>
          <details>
              <summary><b>Then how do you create routes in Next.js?</b></summary>
              <ul>
                  <li>Next.js uses file-based routing system Which means that the routing is handled by the file system each folder in the app directory becomes a route and the folder name becomes the routes path for example if you have a folder named about in the directory you can access that pages at the forward slash about path isn't that so easy</li>
                <li>No need for external packages or complex configurations</li>
                <li>You can create files for the routes you want and immediately open them within your application</li>
              </ul>
          </details>
      </details>
      <details>
        <summary><b>Fullstack</b></summary>
        <details>
              <summary><b>API Routes</b></summary>
              <ul>
                  <li>Enabling the creation of serverless functions to handle API requests</li>
                  <li>Serverless APIs in Next.js are a way of creating API endpoints</li>
                  <li>Without the need for a traditional server</li>
                  <li>It allows us to build and deploy APIs: without managing server infrastructure, worrying about scaling their server as traffic increases</li>
                  <li>With this feature, we can create API endpoints by simply creating a file called route.js in a specific folder within the app directory this file in any route segment of the app directly corresponds to that route API endpoint once again</li>
              </ul>
          </details>
          <details>
              <summary><b>Automatic Code Splitting</b></summary>
              <ul>
                  <li>Code splitting is a technique that breaks down large bundles of JavaScript code into smaller, more manageable chunks that can be loaded as needed</li>
                  <li>When needed this reduces the initial load time of a website and optimizes the user's experience while browsing</li>
                  <li>We have to do lots of configuration as your applications grows</li>
                <li>It uses automatic code splitting by default to split pages into separate chunks when a user navigates to another page only the code required for that page is loaded resulting in Faster subsequent page navigations </li>
              </ul>
          </details>
        <details>
              <summary><b>So, What's the takeaway?</b></summary>
              <ul>
                  <li>Frontend Development has gone through various advancements: linting, formatting, compiling, bundling, minifying, deploying</li>
                  <li>Leaving them to concentrate on the actual code that's where Next.js comes in: automating most of the remaining processes and letting us focus on building the essential business logic of the application</li>
              </ul>
          </details>
        <details>
              <summary><b>It's still just React</b></summary>
              <ul>
                  <li>Next.js is not an entirely new technology</li>
                  <li>It's still fundamentally built on top of React</li>
                  <li>It's purpose is to simplify certain tasks allowing developers to concentrate on the core React code</li>
              </ul>
          </details>
      </details>
</details>

### File & Folder Structure

![img](https://i.imgur.com/YBQQ0DV.png)

```
App >
    layout.js >
      - Any code written in this file will be displayed on every page route you create
      - This single file allows you to personalize the behavior of your application by providing a common layout or template for all pages any elements you include in this file will be shared in your entire application
      - In addition, the layout file also allows you to customize the look and feel of your HTML document so you can set things like the language and you can also modify the metadata for all the pages
    page.js >
      - Represents IE application homepage route
    globals.css >
      - Contains the entire application's global CSS style
```

### Client & Server Components

1. New ways to rendering your components

![img](https://i.imgur.com/aBpUKWh.png)

- By default all components created Next.js within the app folder are react server components
- Which means that Next.js leverages server-side rendering to enhance the initial page loading speed resulting in improved SEO and user experience now in case you want to turn that server-side component by default into a client-side one you need to add the 'use client' directive to the top of your page to turn it into a client-side component using both the client components and the server components allows us to leverage the benefits of server-side rendering while still utilizing react capabilities for building Dynamic and interactive user interfaces

2. When to use Server vs Client Components
   ![img](https://i.imgur.com/3uebcX4.png)

### Routing & Special Next.js Files

1. Directory based routing

![img](https://i.imgur.com/kqgySIK.png)

2. Dynamic Routing

![img](https://i.imgur.com/glwoZ32.png)

### Data Fetching

1. Server Side Rendering (SSR)

- It means Dynamic server rendered data it is fetched fresh on each request with SSR each request to the server triggers a new rendering cycle and data fetch ensuring that the content is always up to date here
- Cache: 'no-store' it simply means hey don't store it simply call it and then display 'the title and the body' of the fetched post this is going to ensure that it refetches it every single time Which means that it's server-side rendered now to get to our second example Which is static generation the only thing we have to do is remove this cash no store.

2. Static Site Generation (SSG)

- That means that by default Next.js uses Static Site Generation
- It will automatically fetch this data right here but it will also cache it this method is idea for Content that doesn't change frequently

3. Incremental Static Regeneration (ISR)

- It combines the benefits of SSR and SSG for dynamic content in static sites with Incremental Static Regeneration you can specify certain data to be statically fetched at build time while defining a revalidation time interval this means that the data will be cached but after a specific time frame it's then going to refresh it and you're always going to have new data making this The Best of Both Worlds for the Dynamic content
- Next.js allows applications to be full-stack which means running the application both on the frontend and on the backend using the same file based routing system.
- Next.js allows us to handle HTTP requests and develop back-end functionality without requiring an external server

### Next.js API Endpoints

- It's worth noting that there are two different ways to define a round out Handler the first one is to create file based route handlers right within the API folder within the app directory and the second approach is to create a direct route Handler within the app directory itself
- You wouldn't be able to have a route within the posts next to the page because Next.js won't know does this have to be a regular frontend page or a backend API route
- It's going to clash between forward slash posts that's going to render a regular page and forward slash posts that should be an API

![img](https://i.imgur.com/FxGi0EM.png)

- I still recommend the first approach of creating the API routes meaning don't create routes right within the app folder rather to keep our code clean and understandable
- It allows us to create those backend routes out of the box next.js supports the following HTTP methods:

![img](https://i.imgur.com/1dl4ZYl.png)

### SEO & Metadata

1. Static Metadata

![img](https://i.imgur.com/gwaWFSi.png)

2. Dynamic Metadata

![img](https://i.imgur.com/wfG42af.png)
