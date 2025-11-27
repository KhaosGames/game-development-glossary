## Game Development Glossary

Game Development Glossary is a simple urban-dictionary community-driven glossary for terms used in game development. This has been something I've wanted to build for a while, after working with various companies and seeing how many terms are used differently across teams.

## Inspiration

After reading [_Why your website should be under 14kB in size_](https://endtimes.dev/why-your-website-should-be-under-14kb-in-size/), I was inspired to create a simple static website that adheres to the 14kB size limit.

The idea is that if a website is small enough, it can fit entirely within the initial TCP congestion window (IW), allowing it to be delivered in a single round-trip time (RTT). This can significantly improve load times, especially on slower connections.

This is obviously not feasible for all websites, but I thought it would be a fun afternoon exercise. I do think that there is a lot of value in the idea, and maybe it's not so far-fetched if most of the content can be loaded asynchronously.

> Note: After having built this, we are now enforcing a 14kB initial load limit on all Khaos Systems' SaaS products.

## Important Details

- The actual minified HTML is quite a bit larger than 14kB, but when compressed with gzip, it is under the limit. Compression is handled by the web server when serving the content. That is why we are spinning up docker with nginx when running `npm run start`.

## Known Issues

- html-minifier does not seem to minify the css. It would also be beneficial to rename css selectors and js variables to shorter names, etc. to further reduce size.
- We are not currently geting a perfect lightouse score due to some issues with best practices around accessibility. This could be improved with some additional effort.