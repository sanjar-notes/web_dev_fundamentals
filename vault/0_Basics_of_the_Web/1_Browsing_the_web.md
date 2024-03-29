# 1. Browsing the web
Created Saturday 27 March 2021

#### Browsing the web
Browsing the web? This is* "*trivial". Yes, _using_ is. But we cannot think of optimization without knowing these details.

#### First connection to a website
![](../../assets/1_Browsing_the_web-image-1-c17f2814.png)

- The URL is sent to the DNS, through the ISP(your Internet company).
- The DNS sends an IP address(the physical device's address). This identifies the server(computer owned by the website) address. Your device also has an IP address.
- You communicate directly with the server now. You are still using going through the ISP, but a DNS is not required in between.

DNS is a system, as well as a server. Watch [here](https://www.youtube.com/watch?v=72snZctFFtA&feature=youtu.be&t=45s).

#### How does the website load
- You request the website(server) for a page. The default page is called the "landing page".
- The server sends 3 kinds of files for the webpage:
  1.  HTML
  2.  JS
  3.  CSS

Note: Media files like images, videos, PDF etc are also recieved.

- The browser reads the files and renders the webpage.

![](../../assets/1_Browsing_the_web-image-2-c17f2814.png)

#### What do the files do?
- HTML - defines basic structure of the page. Relative locations of paragraphs, quotes, buttons, videos, images etc are defined in this file.
- CSS - defines styling. - defines the font, color, styling and behavior of the parts defined by HTML.
- JavaScript - adds interactivity to the page. It can manipulate page elements.
- Media files are places as per the 3 files.

#### What happens when a new page is requested
Naive way:

- You request for the new page.
- The server sends the relevant files.

Efficient way:

- The server actually sent many webpages at once, and the browser stored(cached) them.
- So the JS file loads the new page from the files cached before.
- This way the server has to only send files that are not in cache.
- This saves time and data resources, and makes the site fast.
