



Chunks / Memory

test

Our software uploads file in chunks. Chunk is a part of a file. You can set the size of the chunk going to Tools \| Options \| Advanced

Multipart upload allows to split files into multiple chunks and upload them in multiple threads. It is enabled by default.

also:

Cloudberry prepares chunks in memory \(for instance with default settings of 6 thread count and 100 MB chunk size the following happens: 6 threadcount x 100 MB x 2 workflows = 1200 MB is required\).

By default the amount of allocated memory is 300 MB and is not available in the UI, however it is possible to change in settings.list.

`<MemoryManagerMaxMemoryUsage>314572800</MemoryManagerMaxMemoryUsage>`

[https://kb.cloudberrylab.com/kb1046/](https://kb.cloudberrylab.com/kb1046/)

