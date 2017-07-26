# ES6 Proxy: An introduction

## What are proxies
- A way to intercept certain operations
- Help you define custom behavior for fundamental operations
- Only for objects

## Why do proxies exist and why should I use them?
- Metaprogramming
  - Introspection - you can read only access to a structure of a program
  - Self modification - you can change the structure
  - Intercession - you can redefine semantics of language operations

## How do you create a Proxy
`const proxy = new Proxy(target, handler);`
- Traps
  - functions you can use that exist on Proxy that help modify the proxy. You can find them on MDN

## Proxy as Pointers
`const pointer = new Pointer(target, handler)`
- JS is pass by value, so using proxies as pointers doesn't add much value

## When are proxies the most useful?
- Testing
- Revoking access to a property
