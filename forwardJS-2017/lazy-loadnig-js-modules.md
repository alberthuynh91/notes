# Lazy Loading JS Modules in the Browser
>Increasing web page performance with lazy-loading

## SPA for performance
- Moving your server-side app to SPA would improve the page performance
  - Requests returning JSON instead of HTML
  - Rendering a new view instead of a page
  - Routing and state management on the client-side
- All the performance gains can fall short if you download everything at once

- E-commerce A (server-side rendering) has 5 pages: home, browse, product, cart, and checkout
- E-commerce B (SPA) has the same 5 pages
  - 1 actual page + 4 views
  - The complete flow downloaded is less than server-side rendering

## What is lazy-loading?
- Lazy loading is a design pattern about deferring the initialization (loading/fetching/allocation) of a resource (code/data/asset) until the point at which it is needed
- It's main goal is to improve efficiency when a significant amount of resources is not needed at first
- Lazy loading is targeted to increase performance and save on memory consumption and processing power
- It's an EAA pattern from Martin Fowler

## Do I need lazy-loading
- Above the fold
  - Think about above the fold in a newspaper. If the first thing you see above the fold does not capture you chances are you will not purchase the paper. Same goes for on a webpage
  - Part of the critical rendering path
  - Must be rendered during the page load time
  - Thus, it cannot be lazy loaded
- Below the fold
  - Everything else, needs scrolling or user interaction
  - Won't be displayed during the page load time
  - It doesn't needed to be loaded during the initial load time
- Lazy loading isn't recommended for certain scenarios
  - Supporting network limitations (offline mode, like in the event you are on BART and suddenly lose connection)
  - Web-based mobile apps (Web Views)
  - Apps that can't be paused (games)
  - Specific UX requirements (single loading screen)

## How to lazy-load
- Don't include all your scripts in the page at once
- Don't import all of your modules on the top of your file
- Carefully decide when to import or require your modules and Libraries
  - Below the fold (scroll listening)
  - Event callbacks (user interactions / network calls)
  - Conditionally (for uncommon scenarios)
  - After some time (chat overlays)

## Module
- Structural design pattern
- Purpose: to define reusable components with private/public variables and functions
- Pre-condition: a chunk of code with a return point
- Post-condition: a definition that represents that chunk of code as a module

## Global Object
- Encapsulation through closure -> function scope

## Why use modules?
- Spaghetti code is bad for reusability, readability, code organization and is very brittle (side-effects)
- Modules can fix these all if properly implemented
- Can bring cohesion up and coupling down
- Modules can be packaged and deployed separately from each other, mitigating the "butterfly effect".
- A module can be delivered as a dependency for another module

## Module Loaders
- On the previous example, Kennel is a global var:
  - Fragile
  - Not scalable
  - Counter productive
- Enter module loaders:
  - Container for module registration
  - Dependency injection
  - Modules loading on demand

## CommonJS
  - Export your module interface with module.exports
  - Import on the client using require (dependency)

## Lazy loading in CommonJS
- Using Webpack's require.ensure()
`require.ensure([], function(require) {
  ...

  })`
- Read more about code splitting

## ES Modules
- ES2015+ offers native modules which are quite a bit similar to CommonJS

## System.JS
- System.js is a module loader which supports AMD, CommonJS, ES and global scripts
- It performs async module loading using a promises-based API
- Promises can be chained and combined
- Promises.all can load multiple modules in parallel
- System.js 0.2.0 ships with dynamic import() operator

## Webpack 2
- Webpack is a module bundler consisted of Entries, Outputs, Loaders, and plugins
- Offers native ES modules and System.js support
- Does bundling and lazy loading JS and CSS
- Performs tree-shaking

## Example of Lazy loading
- On macys.com they load the page without the header and after if you scroll up you will see the header, which is lazy loaded. Doing this saves a few milliseconds of load time.
