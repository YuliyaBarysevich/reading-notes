# Class 36

**Resources:**

- [LocalStorage vs. Cookies: All You Need to Know About Storing JWT Tokens Securely in the Front-End](https://blog.cotter.app/localstorage-vs-cookies-all-you-need-to-know-about-storing-jwt-tokens-securely-in-the-front-end/)
- [What’s the Difference Between First-Party and Third-Party Cookies?](https://clearcode.cc/blog/difference-between-first-party-third-party-cookies/)
- [COOKIES, TAGS AND PIXELS– TRACKING CUSTOMER ENGAGEMENT](https://resources.marketingeffectiveness.nielsen.com/blog/cookies-tags-pixels-tracking-customer-engagement)
- [7 Ways to Implement Conditional Rendering in React Applications](https://www.digitalocean.com/community/tutorials/7-ways-to-implement-conditional-rendering-in-react-applications)

## Review, Research, and Discussion

1. What are the advantages of storing tokens in “Cookies” vs “Local Storage”
    - The cookie is not accessible via JavaScript; hence, it is not as vulnerable to XSS attacks as localStorage.
    - If you're using `httpOnly` and `secure` cookies, that means your cookies cannot be accessed using JavaScript. This means, even if an attacker can run JS on your site, they can't read your access token from the cookie.
    - It's automatically sent in every HTTP request to your server.
2. Explain 3rd party cookies.
    - Third-party cookies are those created by domains other than the one the user is visiting at the time, and are mainly used for tracking and online-advertising purposes. They also allow website owners to provide certain services, such as live chats.
3. How do pixel tags work?
    - Pixel tags are typically single pixel, transparent GIF images that are added to a web page. Even though the pixel tag is virtually invisible, it is still served just like any other image you may see online. The trick is that the web page is served from the website’s domain while the image is served from the ad server’s domain. This allows the ad server to read and record the cookie with the unique ID and the extended information it needs to record.

**Vocabulary Terms:**


1. **Cookies**
    - Cookies are text files with small pieces of data — like a username and password — that are used to identify your computer as you use a computer network. Specific cookies known as HTTP cookies are used to identify specific users and improve your web browsing experience.
2. **Authorization**
    - Authorization is a security mechanism used to determine user/client privileges or access levels related to system resources, including computer programs, files, services, data and application features.
3. **Access control**
    - Access controls authenticate and authorize individuals to access the information they are allowed to see and use.
4. **Conditional rendering**
    - Conditional rendering is a term to describe the ability to render different user interface (UI) markup if a condition is true or false. In React, it allows us to render different elements or components based on a condition. 