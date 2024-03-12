### Introduction and Goals of AFS
- **Keywords:** AFS, scalability, Carnegie-Mellon University, distributed file system.
- **Details:** AFS was developed at Carnegie-Mellon University in the 1980s with the main goal of scalability. It aimed to design a distributed file system that could support as many clients as possible, emphasizing efficient protocol design between clients and servers to achieve this scalability.

### AFS Version 1
- **Keywords:** AFSv1, whole-file caching, local disk caching, protocol messages.
- **Details:** AFS version 1 (AFSv1) introduced whole-file caching on the client's local disk, where opening a file fetches its entire content from the server and caches it locally. This approach differed from NFS's block-level caching and aimed to reduce server interaction by servicing subsequent read and write operations locally, thereby increasing efficiency.

### Challenges with AFSv1
- **Keywords:** Path-traversal costs, TestAuth protocol messages, scalability issues.
- **Details:** The initial version of AFS faced scalability challenges due to high path-traversal costs and frequent TestAuth protocol messages, which overloaded the server by requiring frequent checks for cached content validity.

### AFS Version 2 (AFSv2) Improvements
- **Keywords:** Callback mechanism, file identifiers (FIDs), protocol redesign.
- **Details:** AFSv2 addressed scalability issues by introducing a callback mechanism, where the server promises to inform a client if a cached file is modified, and using file identifiers (FIDs) instead of pathnames to specify files. This significantly reduced the number of client-server interactions and path traversal overheads, enhancing scalability.

### Cache Consistency
- **Keywords:** Cache consistency, update visibility, cache staleness, callback recall.
- **Details:** AFSv2 ensured cache consistency by making updates visible when a file is closed and immediately invalidating cached copies on other clients. This approach, alongside the callback mechanism, provided a straightforward and effective cache consistency model.

### Crash Recovery
- **Keywords:** Crash recovery, callback recall, cache validity, server recovery.
- **Details:** The document discusses the complexities of crash recovery in AFS, including handling missed callback recall messages and ensuring cache validity after a crash. Server recovery involves ensuring all clients are aware of the crash to prevent access to stale cached files.

### Scale and Performance of AFSv2
- **Keywords:** Scalability, performance, local disk cache, NFS comparison.
- **Details:** With the improvements in AFSv2, the system could support more clients per server and offered performance benefits by leveraging local disk caches for frequently accessed files, making file access times comparable to local disk access for cached files.

### Summary
- **Keywords:** Distributed file systems, AFS protocol design, scalability, cache consistency.
