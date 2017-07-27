# Mobile Web Performance

## What do we want?
>Fast to load, render, respond, and understand

## Current Ecosystem
- Less than half of the world are still not online
- We have to be conscious of screen size, RAM, battery life, and CPU capabilities.
- Our websites are now a lot bigger, which is why 3g is not performing the same as it was in the past

## Loading a page
- Download - # of files needed for the page
- Parse - file size of above resources
- Execute - parsing and painting
- Perceived Performance - user perception of load speed and reaction time

## Device Limitations
> We need to take into account device limitations

- Less powerful CPUS
- Not plugged in
- Metered data
- Tiny screen size
- Different interactions

## Knowns / Unknowns
> Be conscious of the things you know and don't know

## Tools
- YSlow
- PageSpeed
  - Chrome extension
  - Better for learning performance than Lighthouse
- WebPageTest
- Dev Tools
- Lighthouse
  - Audits your website and tells you how good you are doing

## How can we improve?
- Minimize requests
- Reduce DNS Lookup
- Avoid redirects
- Cache headers
- Only load needed resources
- Don't scale images with HTML
- Minimize size & optimize media
  - Optimize all images
    - Server the smallest image file for the screen size and resolution
    - Scaling images is very slow
    - Image compression
      - ImageOptim
      - ImageAlpha
      - TinyPNG
      - Photoshop
      - Etc
      - Smartvision
    - Use the right image format for the page
    - Reduce the number of images
- Put CSS in the <head>
- Put JS at the bottom
- Minify your code
- Optimize source order
- Be conscious of the front end frameworks you use

## Configure the viewport
> Often overlooked, but very important for improving performance

`<meta name="viewport" content="width=device-width, ...">`
