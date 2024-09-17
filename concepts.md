# 1. different versions of the HTTP protocol (needs refinement)

HTTP/1.0
Release: 1996
Features:
Basic request-response model.
Each request opens a new connection; connections are not reused.
Lacks support for persistent connections and pipelining.
HTTP/1.1
Release: 1999
Features:
Persistent Connections: Keeps connections open for multiple requests/responses, reducing latency.
Pipelining: Allows multiple requests to be sent without waiting for the corresponding responses, although it's not widely used due to head-of-line blocking issues.
Chunked Transfer Encoding: Enables sending data in chunks, allowing the server to start responding before it knows the full content length.
Additional Caching Mechanisms: Better caching headers and mechanisms to improve performance.
Host Header: Mandatory Host header allows multiple domains to be served from a single IP address.
HTTP/2
Release: 2015
Features:
Binary Protocol: Uses binary framing rather than textual, improving efficiency.
Multiplexing: Multiple requests and responses can be sent simultaneously over a single connection without blocking each other.
Header Compression: Compresses headers to reduce overhead.
Stream Prioritization: Allows clients to prioritize certain streams over others.
HTTP/3
Release: 2022
Features:
Based on QUIC: Uses QUIC (Quick UDP Internet Connections) instead of TCP, providing reduced latency and improved performance.
Multiplexing: Similar to HTTP/2 but with less head-of-line blocking since QUIC operates over UDP.
Improved Security: Integrates TLS 1.3 directly into the protocol, enhancing security.
Each new version has aimed to address the limitations of its predecessors and improve performance, efficiency, and user experience.