## 블로그 만들기

## 버슬(NEXT.js)

[vercel](https://vercel.com/templates/next.js/blog-starter-kit)

#### Static Exports

Next.js enables starting as a static site or Single-Page Application (SPA), then later optionally upgrading to use features that require a server.

When running next build, Next.js generates an HTML file per route. By breaking a strict SPA into individual HTML files, Next.js can avoid loading unnecessary JavaScript code on the client-side, reducing the bundle size and enabling faster page loads.

Since Next.js supports this static export, it can be deployed and hosted on any web server that can serve HTML/CSS/JS static assets.

```js
/**
 * @type {import('next').NextConfig}
 */
const nextConfig = {
    output: "export",
    distDir: "dist",
    images: {
        unoptimized: true,
    },
};

module.exports = nextConfig;
```
