## 블로그 만들기

http://localhost:64215

`npx serve ./dist`
## 버슬(NEXT.js)

[vercel](https://vercel.com/templates/next.js/blog-starter-kit)

1. 

#### Static Exports

Next.js enables starting as a static site or Single-Page Application (SPA), then later optionally upgrading to use features that require a server.

When running next build, Next.js generates an HTML file per route. By breaking a strict SPA into individual HTML files, Next.js can avoid loading unnecessary JavaScript code on the client-side, reducing the bundle size and enabling faster page loads.

Since Next.js supports this static export, it can be deployed and hosted on any web server that can serve HTML/CSS/JS static assets.


- next.config.js 만들기

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



<details>
<summary>Whitespace 에러</summary>
유닉스 시스템에서는 한 줄의 끝이 LF(Line Feed)로 이루어지는 반면,
윈도우에서는 줄 하나가 CR(Carriage Return)과 LF, 즉 CRLF로 이루어지는데
Git이 이 둘 중 어느 쪽으로 선택할지 혼란이 온 것이다.

해결방법

`git config --global core.autocrlf true` // 시스템 전체에 적용
⠀
`git config core.autocrlf true` // 해당 프로젝트에만 적용

</details>
