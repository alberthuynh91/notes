# ES6 Proxy: An introduction

## What are proxies
- A way to intercept certain operations
- Help you define custom behavior for fundamental operations

## Why do proxies exist and why should I use them?
- Metaprogramming
  - When code is writing/running itself
  - Changing itself
  - Introspection - read only
  - Self modification - change structure
  - Intercession - redefine semantics of language

## How do you create a Proxy
`const proxy = new Proxy(target, handler);`
- Traps - functions you can use that exist on Proxy that help modify the proxy. You can find them on MDN

## Proxy as Pointers
`const pointer = new Pointer(target, handler)`
- JS is pass by value, so using proxies as pointers doesn't add much value
