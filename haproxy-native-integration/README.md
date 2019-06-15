This folder contains a simple configuration file for a HAProxy Load Balancer which integrates with HashiCorp Consul to automatically discover service instances.

The config snippet allows for multiple instances of a service running on the same server to be served by the backend (useful for rolling/canary deploys). Without `resolve-opts allow-dup-ip`, haproxy skips on any repeat service node (duplicate ip – even with a different port).

---

Content is partially based on

https://www.haproxy.com/de/blog/haproxy-and-consul-with-dns-for-service-discovery/

where you can find more information around combining consul-template and HAProxy native Service Discovery implememtation.
