##LETS GET STARTED!##

####BROWSER'S HIGH LEVEL STRUCTURE####

It is important to have knowledge of the intricate structure of the browser in order to understand the processes that happen at each stage.

The components of the browsers are:

  - **User interface**

    The user interface includes the address bar, back/forward button, bookmarking menu, etc. Every part of the browser display except the window where you see the requested page.

  - **Browser engine:**

    The browser engine marshals actions between the UI (User Interface) and the rendering engine.

  - **Rendering engine:**

    The rendering engine is responsible for displaying requested content. For example if the requested content is HTML, the rendering engine parses HTML and CSS, and displays the parsed content on the screen.

  - **Networking:**

    The networking handles network calls such as HTTP requests, using different implementations for different platforms behind a platform-independent interface.

  - **UI backend:**

    The UI backend is used for drawing basic widgets like combo boxes and windows. This backend exposes a generic interface that is not platform specific. Underneath it uses operating system user interface methods.

  - **JavaScript engine:**

    The JavaScript engine is used to parse and execute JavaScript code.

  - **Data storage:**

    The data storage is a persistence layer. The browser may need to save all sorts of data locally, such as cookies. Browsers also support storage mechanisms such as; localStorage, IndexedDB, WebSQL and FileSystem.

##WHAT EXACTLY HAPPENS?##

When you type the URL into your browser, several things occur behind the scenes to bring to bring you the desired output.

Once you have typed the URL/web address into your browser, the first thing your browser does is;

    STEP 1: The browser breaks the URL into three parts:

1.The protocol ("http://").The protocol identifies the method (set of rules) by which the resource is transmitted.

2.The domain name ("www.google.com ")

3.The file name e.g. ("howbrowserswork1.htm")

    STEP 2: DNS (Domain Name System) lookup

This means the DNS server translates a domain name into an IP address.

A domain name is the unique name assigned to a website. When you build a website you also register a domain name. For a domain name to be assigned to a website, it first needs to be added to a DNS server.

A DNS server is a large database containing domain name and its corresponding IP address. This means that URL you typed into the address bar maps to one or more IP addresses.

For example, one IP address for Google is 74.125.134.102. You can enter 74.125.134.102 in the address bar and it will show the contents at www.google.com.

    STEP 3: Request Page

Once the browser has the IP address it sends an HTTP request to the web server at that address.

HTTP stands for “Hypertext Transfer Protocol” and is used to facilitate requests from your client (the browser) and responses from the server asking for the file “howbrowserswork1.htm”.

In this case the response is HTML.

    STEP 4: HTML Parsing

The rendering engine starts getting the contents of the requested document from the networking layer.

The rendering engine will start parsing the HTML document and turn the tags to Document Object Model (DOM) nodes in a tree called the "content tree" or the “DOM tree”.

It will parse the style data, both in external CSS files and in style elements. The styling information together with visual instructions in the HTML will be used to create another tree –the render tree.

The render tree displays rectangles (that represent paragraphs, headlines, etc.) with a few visual attributes such as color and size dimensions. These rectangles are displayed in order on the page.

    STEP 5: Layout the Render tree

After the construction of the render tree it goes through a _"layout"_ process. This means giving each node the exact coordinates where it should appear on the screen.

    STEP 6: Painting

The next stage is painting where the render tree will be traversed and each node will be painted using the UI backend layer and hence we are able to view the requested output.
