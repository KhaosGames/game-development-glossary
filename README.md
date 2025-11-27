## Game Development Glossary

Game Development Glossary is a simple urban-dictionary community-driven glossary for terms used in game development. This has been something I've wanted to build for a while, after working with various companies and seeing how many terms are used differently across teams.

## Inspiration

After reading [*Why your website should be under 14kB in size*](https://endtimes.dev/why-your-website-should-be-under-14kb-in-size/), I was inspired to create a simple static website that adheres to the 14kB size limit.

The idea is that if a website is small enough, it can fit entirely within the initial TCP congestion window (IW), allowing it to be delivered in a single round-trip time (RTT). This can significantly improve load times, especially on slower connections. 

This is obviously not feasible for all websites, but I thought it would be a fun afternoon exercise. I do think that there is a lot of value in the idea, and maybe it's not so far-fetched if most of the content can be loaded asynchronously.

> Note: After having built this, we are now enforcing a 14kB initial load limit on all Khaos Systems' SaaS products. 