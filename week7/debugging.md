# Debugging and Optimization Prove Activity

## Website:
https://www.nintendo.com/us/

## Tool:
Lighthouse
 
## Recommendations to Improve Performance:

**Use efficient cache lifetimes –** The page could benefit from increasing its cache lifetime on the user’s browser. On a big website like this one, there are a lot of resources, including CSS, JS, and image addresses that must be retrieved; a long cache lifetime would significantly reduce the time it takes to load the page on repeat visits, even if the user does not visit it for a while. Several assets’ Cache TTLs (time to live) are set to “None” or only a couple of minutes. I’d recommend including a longer max-age in the Cache-Control header for assets that don’t change often, such as common.js or main.css. 

**Improve image delivery –** For most of the games on the home page, the image files are much larger than what’s displayed, which increases download time. I would recommend they use responsive images (with the srcset attribute) so that the browser only downloads the size it needs for the user’s screen. Additionally, they could use different image formats for improved performance, such as WebP or AVIF. 

**Render blocking requests –** There is currently an Optimizely JS file that must be processed before the rest of the page can be delivered to the user. While I understand this file is often used to help personalize the website for users, I would recommend adding the defer attribute to this script’s declaration or at least moving it out of the critical rendering path. This would allow the browser to continue parsing the HTML while the Optimizely script downloads in the background, only executing the JS once the page is fully loaded. 
