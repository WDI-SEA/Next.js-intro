# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Next.js Intro

[Next.js](https://nextjs.org/) is an open source framework built on `React` and `Node.sj` that allows for **SSR** (*Server Side Rendering*) using `.jsx` components and a react-style workflow. This is in contrast to react's typical **CSR** (*client side rendering*), and comes with certain advantages and caveats. 

It is maintained by [Vercel](https://vercel.com/home?utm_source=next-site&utm_medium=banner&utm_campaign=next-website) who provides excellent [documentation](https://nextjs.org/docs) and extremely easy deploymment.

## Lesson Objectives

* Understand the differences between SSR and CSR
* Know the different applications of SSR and CSR
* Create a Next.js app and get aquianted with the Next.js framework
* Deploy a Next.js app to vercel 
* Use a multibranch workflow for CI management

## SSR vs CSR

React apps are usually *'single page apps'* that are sent over as a bundle of javascript to the client and dynamically update what the user is seeing by generic content on the fly. This is called *client side rendering* or *CSR*.

![CSR Flowchart](Client-Side-Rendering-Flowchart.jpg)

`Next.js` uses `.jsx` and `React` to perform *server side rendering* or *SSR*. Next.js pre-renders html from the .jsx you write and sends it over to the client. `Next.js` also allows you to build a data API in the same project folder as your Next app, so there is no need for an express server.

![pros-cons](pros-and-cons.jpg)

### When to use CSR vs SSR?

The short answer is CSR is good for web apps and SSR is best for static sites, but what is the difference between an app and a static site?

Web apps generally have a great deal more user interaction than a static site, for example:

* the [slack](https://slack.com/) web interface
* [miro](https://miro.com/app/dashboard/) boards

What then is a static site?

* Blogs
* Primarily text content
* Documentation and wiki type sites

## Next.js Cheatsheet

* `npm i -g create-next-app` to install creat-next-app globally
* `create-next-app <app-name>` to create a next app in a directory called `<app-name>`
* `npm run dev` will run a script that builds your next app and fires up the server for live reload

#### Using Next.js

* the public folder is static (you can config the favicon here)
* the styles folder is for css -- `globals.css` is applied everywhere
* the api folder is where the data api lives
* routes are made in the pages folder and `.jsx` components -- remember to lower case the file names!
* the `<Head>` Component in your `index.js` is like the head of an html file.
* if you want to make child components, they should be put in a folder called `components` that is a sibling of `pages`

*[image credits](https://www.growth-rocket.com/blog/a-closer-look-at-client-side-server-side-rendering/)*
