# You don't know Node

## How can we make Node always use JS strict mode?
`node --use-strict` (this is v8)

## What is process.argv? And what type of data does it hold?
- Returns an array of strings of arguments

## How can we do one final operation before Node crashes?
- Use the uncaught exception on the process object

`process.on(`uncaughtException`, (err) => {
  process.exit(1); // not optional, will not exit without this
});`

## What are the dot commands in node REPL?
- .save
- .load
- .help
- etc

## What does the _ do in Node REPL?
- Last executed value

## Whats the difference between Buffer.alloc vs Buffer.allocUnsafe?

## How does the cluster module work in Node?
- Helps us with scalability strategies

## When is it ok to us the file system (fs) system sync methods?
- When you are not worried about executing something that might block the event loop.

## How can you print only one level of a deeply nested object?
`console.dir(global, {depth: 0})`

## How can you debug a Node program in Chrome dev-tools?

## Can callbacks be synchronous?
- Yes, callbacks do not mean the code is asynchronous code.

## Event emitters vs callback functions, whats the difference in async handling of code?
- Event emitters are at the code of everything else in node.

## What is an example of a built-in stream in Node that is both readable and writable?
`crypto.createCipher`
`zlib.createGzip`

## Paused vs Readable modes of streams?
- By default you get Paused
- You need listeners to grab data from flowing streams
- Streams are very important and used everywhere in Node
- Streams allow you to only use memory when you need it

## What are streams?
- Collections of data that may not be all available at once and also may not fit in memory
- Think of them of arrays. You don't get them all at once, but at one at a time.
- If you have a 10gb file, you cant read it all at once because the buffer isn't even that big.
- You basically read it a bit at a time by chunking using streams.
- All streams are event emitters.
- The global way to use stream is by pipe.
`readable.pipe(writable)`

>Linux
`a | b | c | d`
> Node.js
`a.pipe(b).pipe(c).pipe(d);`

- Implementing vs consuming streams
  - Most of the time you are consuming streams
  - The res object is a stream inside an API call
  - When consuming, you don't need to `require` a stream
