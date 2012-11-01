# mockstream

Mockstream is a very simple utility library of streams helpful for testing

## Installing

```npm install mockstream```

## Streams

### MockDataStream

A simple readable stream that outputs a stream of a given length filled with bogus data (lots of 0's).

#### Usage

```
var mockstream = require('mockstream'),
    stream = new mockstream.MockDataStream({
        chunkSize: 1024, // 1 KB data chunks
        streamLength: 1048576 // 1 MB of data
    });
    
// Register listeners, etc

// Start pumping data
stream.start();

```