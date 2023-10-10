# WebApplicationArchitecture
Web Application Architecture in 2023: Moving in the Right Direction

Web application architecture is a high-level structure that determines the way your product and business will operate, perform and scale. These days, the stage of choosing web app architecture is often where you get lost in a variety of options available on the software development market. The more new names and trends appear, the harder it becomes to decide. Isomorph, Progressive Web app, SPA, or SSR – what’s the best modern web app architecture for you, and which criteria to use for evaluation? In this article, we cover the major front-end architecture types available for the Web and explain the peculiarities of their implementation.

# What Is a Web App vs Website
First, let’s define a web app. It’s a client-server application, where there’s a browser (a client) and a web server. The logic of a web application is distributed among the server and the client, there’s a channel for information exchange, and data storage located locally or in the cloud.

Web apps appeared as a website evolution stage and, indeed, have a lot in common. The factors that distinguish a website from a web application are interactivity, integration and authentication.
![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/8079a8aa-d430-4d78-a748-435390773dd0)

In other words, the more customizable, interactive and functional a website is, the closer it is to being called a web application. 

# 3 TIER ARCHITECTURE IN WEB DEVELOPMENT
Modern web apps still use the 3 tier architecture concept, which separates applications into presentation tier, application tier, and data tier.
![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/65b30928-4f0f-435c-869b-850dc1ec0239)

ithin the 3 tier web application architecture, each layer runs on its own infrastructure, and can be developed in parallel by different teams. Such a structure allows to update and scale each tier as needed without impacting the other tiers.

# Types of Web Application Architecture
To help you understand if the suggested approach for your product really fits your business needs, we’ll evaluate modern web app architecture types according to the criteria we consider most vital for businesses, i.e. performance, UI, SEO, linkability and the speed of realization on the development side. 

# SERVER SIDE RENDERING (SSR)
![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/055bd362-575d-4fe2-9b05-59e06f5211d1)

Talking about the very basic web principles we usually mean the client-server architecture. A client requests content from a server, where the business logic and a database are located. Using simple JavaScript, a static web page sends the request to a service (possibly an API). The service returns the data and displays an HTML page to the client. 

If your application is server-side rendered, the content is fetched from the server and passed to the browser to be displayed to the user. If the HTML page is rendered on the server-side, the user has to navigate to the page before the browser fetches a page from the server. This means more time is needed to display the content to the user. To cache the page content, this scheme is often supplied with Nginx, a web server that can also be used as a mail proxy and load balancer.

Pros & cons. The fact HTML is rendered on the server provides a number of advantages such as SEO, linkability and an instant first page load. Server Side Rendering is working while JS is disabled in the browser. With the code being processed on the server, no specific requirements to the browser are imposed, – this allows us to instantly spot errors. However, SSR can’t handle heavy server requests (repeated HTML, CSS), which results in the slow rendering when the server is loaded or a full page is rebooted. But the real Achilles’ heel of this basic web app architecture type is poor interaction with the end-user and the inability to create full-fledged UI. In other words, SSR is a simple and cost-effective way to go if you need to build a straightforward website. Realization of this architecture type is possible with any programming language and back-end.

# STATIC SITE GENERATION (SSG)
The process of Static Site Generation involves a generator that automates coding of individual HTML pages, creating them from templates. Choosing Static Site Generation, you receive a simple static website located on a CDN or any server, that holds an already generated HTML page to be given to users upon request. So, no need to generate it each time when someone visits your website – the server just sends the already existing data through an API.

![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/7b8ef994-6c46-4ec7-9d3d-bfb6e28e208a)

Pros & cons. First and foremost, this approach is suitable for websites only. Along with that, the content of the generated website pages does not change unless you add new data or components. It means that you’ll have to completely re-generate the website once you wish to add new content. This is one of the major drawbacks that seriously limits the business cases to which it is applicable.

Among the advantages, though, is the high speed of the static content that is being delivered through a CDN. Also, in SSG all server operations and work with the database are realized through an API, which is independent from the website. This option is simple and thus exclusively affordable to realize.

Examples of simple static-site generators are Jekyll and Hugo, while Gatsby and VuePress are a fit for the realization of more complex solutions. 

# SINGLE PAGE APPLICATION (SPA)
SPA is the type of web application that works within a browser. It doesn’t require reloading the page when new data needs to be displayed. This web app architecture type is extensively used in our daily life: Facebook, Gmail, Google Maps, GitHub and Twitter – all of them are single-page apps. 

![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/e225b9bd-6f7a-47b9-a25f-5d2878e3b10b)

Pros & cons. In contrast to SSR and SSG, SPA allows you to build an interactive web app. It uses an API to communicate with the server. This architecture is good for easily scaling your product. Also if a mobile app is needed, no additional efforts are required for API development – the mobile app could use the same API as Web.

SPA grants fast rendering after the app is fully loaded in the browser and creates highly responsive software for the end-user. At the same time, it “kills” your SEO and limits linkability, as the realization of such functionality will require additional efforts. Among the other drawbacks are the long time needed for the first load, poor routing and limited support of outdated browsers. Being a rather costly web architecture type, SPA is a fit for creating responsive UI for B2C users.

# PROGRESSIVE WEB APP (PWA)
It seems like during the past few years, everybody’s talking about PWAs. What’s so special about them and do they really solve all the issues of web app development?

![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/a8e8aef4-1a79-4bc0-a19f-bf4082f593fa)

Progressive web app architecture uses the logic of a single page web app with some services running next, in the browser. This means the main point to take into account is that both the browser and the OS need to support this set of standards. 

For an end-user, a progressive web app physically means a pop-up offering to add the app on the launch screen (not a browser, but your operating system’s screen), when they visit a website. If the user accepts, the app is automatically added to the device.

Implementing PWA allows your web application to support offline experiences, background synchronization, and push notifications. This opens access to the functionality that previously required a native application. At the same time, selecting the PWA architecture for your project, you need to keep in mind that the majority of functions are not available on iOS. It is worth it to analyze each specific business case.

Pros & cons. Progressive web app architecture is supported by Windows, Android and iOS (for iOS, offline mode is disabled though). Developers can add updates to a web app remotely. A PWA is secure as it’s using HTTPS. At the same time, end users can install a PWA without even visiting a Play Market or App Store. Among the drawbacks of this architecture type are the need to select the browser and OS that fully support it.

# ISOMORPHIC
Another modern web app architecture is called isomorphic. This is a type of JavaScript application that can run both on the client-side and the server-side. First, the client loads an HTML, where the JavaScript app is uploaded to the browser, then the app starts running like an SPA. 

![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/5d3d3b17-a0aa-418c-b6da-6278a90a10a4)

Pros & cons. Unlike server-side rendering, isomorphic web architecture provides quick data updates, responsiveness and multiple UI/UX options. It ensures quicker rendering when the server is loaded, as the processed code is transferred to the client. And unlike client-side rendering, it grants an instant display in the browser, user-friendly routing, SEO and linkability. The only drawback this web app architecture type has is that it’s fully supported only by JavaScript. Most often, this means that the tech stack to choose from is limited to JS-based frameworks and tools.

# MICRO FRONT-END
Among the other web application design principles, we distinguish micro front-end, an approach that is built based on the decomposition of a front-end app into separate “micro-apps” working together. For the end-user, they are all located on a single page.

![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/f2fe0b82-e961-46ed-8290-72e37d4e2282)

This web app architecture type is modular, which means that the pages and widgets are completely independent apps. With such an approach, development and deployment are running in parallel. But at the same time, the structure makes your app complicated and causes code duplication.

# NODE.JS AND THE NEW WEB FRONT-END
This concept was first formulated in 2013 by ​​Nicholas C. Zakas, and is now used for complex web solutions. 

“Separating the back-end UI layer out from the back-end business logic just makes sense in larger web architecture. Why should the front-end engineers care what server-side language is necessary to perform business-critical functions? Why should that decision leak into the back-end UI layer? The needs of the front-end are fundamentally different from the needs of the back-end”, this is how Zakas explains the main principle of this web application development type.

This type of web app architecture consists of a Node.js-based server and a UI layer. Along with that, the business logic server can be written in whatever language (let’s take PHP as an example) and use an API to communicate with the server.

![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/0c9bea6c-e865-409c-8348-0e78d2613581)

In fact, the new web front-end approach allows us to use all the advantages of the isomorphic architecture type, SSR or SPA, API for mobile devices and linkability. Unlike isomorphic web apps, no restrictions to the language or business logics platform appear. Although it should be noted that developing a web app that uses the new web frontend logic takes longer than the one using SSG or SSR type. To save time for development, we suggest using the Next.js and Nuxt.js frameworks.

The concept of new web frontend is a fit when it comes to developing an isomorphic web app, where an API server already exists.

# Cloud Architecture for Web Application Development
Speaking of web application architecture, we’ll briefly cover its server-side part. Cloud architecture implies that servers are managed by a cloud provider, such as Amazon AWS, Azure or Google Cloud. In addition to hosting servers on their side, these providers offer a complex of services that allow building web applications hosted and managed in the cloud.

# AWS SERVERLESS WEB APP ARCHITECTURE
AWS serverless services is one of the most popular cloud solutions used to implement popular patterns such as microservices, mobile backends, and Single-Page Applications. The below scheme gives an understanding of how AWS web services can be used for creating a web application using the 3 tier architecture logic we explained earlier.

![image](https://github.com/TheArchitectAntonio/WebApplicationArchitecture/assets/147462884/9a076e59-3160-44fa-aa1a-711a6b454e13)

# AZURE WEB APP ARCHITECTURE

Azure provides a variety of cloud computing services that allow you to build basic and secure serverless web applications.

A basic web app is built with Azure App Service and Azure SQL Database. A combination of Web App, Front Door, Function App, Azure DNS, Azure Cognitive Search and Azure DNS helps improve scalability and performance in an Azure App Service web application.

A serverless web application developed with Azure serves static content from Azure Blob Storage, and implements an API using Azure Functions. The API reads data from Cosmos DB and returns the results to the web app.

Azure App Service Environment (ASE) is used for deploying web apps where additional security is required.

# DESIGNING HIGHLY SCALABLE WEB APPS ON GOOGLE CLOUD PLATFORM
Depending on your business needs, the maturity of the development and infrastructure team, GCP offers App Engine or Cloud Run, Compute Engine or Kubernetes Engine for building scalable architecture web apps.

# Final Thoughts
Choosing the best architecture for web and a mobile app, you may find yourself lost in a variety of web architecture types that are available on the market. Modern web app architecture includes isomorph, PWAs, Micro front-end and more. Massive market players like Amazon, Google and Microsoft provide complex structures to build cloud architecture at the three tiers of a web application. In this article, we overviewed the main web app architecture types in detail. But the key takeaway remains the same for whichever software development endeavour. When selecting an architecture type, mind your business’ specific needs and tailor the criteria we listed to evaluate the options available to choose which one works best for you.
