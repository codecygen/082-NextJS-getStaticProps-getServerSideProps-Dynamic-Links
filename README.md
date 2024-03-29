This is a very simple Next.js app.

For a new project, if you need to install SWR (Stale-While-Revalidate) write command
- npm i swr

Pages created in this app are;
- http://localhost:3000
- http://localhost:3000/aras, which would generate dynamic uid page
- http://localhost:3000/products/p2, which would generate p2 product id 
- http://localhost:3000/populations, uses fetch API with traditional React hooks on client side
- http://localhost:3000/descriptions, uses SWR on client side.
- http://localhost:3000/holidays, uses fetch API on server side.


When you run "npm run build" server files are optimized and ".next" folder gets created.
"npm start" starts the server with the files under ".next" folder. These files are for production.

## Keywords:
- **NextJS-getStaticProps-Static-Side-Rendering**
- **NextJS-ISR-Incremental-Static-Regeneration**
- **NextJS-getStaticProps-getStaticPathsServer-Dynamic-Link-Parameter-Extraction**, there is a possibility to extract the data through getStaticProps, instead of useRouter's router.query.parameter option. When you use useRouter hook, the dynamic link data is extracted from the client side, whereas with the "context" argument of getStaticProps function, you are able to extract the data from server side.
- **NextJS-getServerSideProps-Server-Side-Rendering**
- **NextJS-Client-Side-Data-Fetching**, if data is changing frequently such as stock prices, if the data is highly user specific such as last orders of a customer in an online shop, if partial data needs to be loaded which is only used on the part of the page, then prefetching data for the page generation might not work as required. In these circumstances, traditional React hooks for client side data fetching such as useEffect() and Javascript built in method fetch() works fine. Since this page is not handled by Next.js, the data will not be pre-rendered by NextJS but instead, its controlled by React Hooks.
- **NextJS-Both-Client-Side-And-Server-Side-Data-Fetching**, sometimes this leads to best possible user xp, because you have some data right from the start and then you update it with client side React hooks. In this setting, you use useState and useEffect hooks on the client side and getStaticProps on the server side. getServerSideProps does not make sense to be used in conjunction with client side data fetching.
- **React-Simple-Vercel-Hook-Stale-While-Revalidate-SWR**, This can be used instead of creating your custom hooks for data fetching. The name “SWR” is derived from stale-while-revalidate, a HTTP cache invalidation strategy popularized by HTTP RFC 5861. SWR is a strategy to first return the data from cache (stale), then send the fetch request (revalidate), and finally come with the up-to-date data.
- **NextJS-Server-Side-Data-Fetching**, This is a fetch method on the server side.