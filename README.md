# Awesome-API-Gateway-Reverse-Proxy

## Top API Gateway & Reverse Proxy Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Traffic Routing, Service Discovery & Cloud-Native Ingress*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **API Gateway & Reverse Proxy**. These tools enable developers to route, secure, and observe traffic into microservices—from dynamic service discovery and automatic TLS to rate limiting, circuit breaking, and cloud-native ingress.



**Examples** include NGINX Plus, Kong Gateway, Traefik Enterprise, Envoy Gateway, HAProxy Enterprise, Apigee, Ambassador Edge Stack, Tyk Gateway, Zuul, and KrakenD (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, dynamic configuration, and open traffic management—ideal for platform engineers, SREs, and developers seeking transparent, vendor-independent API infrastructure.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[NGINX Plus](https://www.nginx.com/products/nginx/)**  

  **The commercial edition of the world's most widely deployed web server and reverse proxy** . Adds enterprise-grade features beyond open-source NGINX: **session persistence**, **configuration via API**, **active health checks**, and **live activity monitoring** . **Priced per instance**—subscription licenses start around **$399/month** for a single instance with premium support . **The default choice** when you need the reliability of NGINX with enterprise support and dynamic configuration.



- **[Kong Gateway (Enterprise/Konnect)](https://konghq.com/)**  

  **The most widely adopted open-source API gateway** with a commercial enterprise tier . **100+ plugins** for authentication, rate limiting, and API management . **Traditional mode** requires PostgreSQL; **DB-less mode** removes the database at the cost of clustering features . **Advanced plugins like OpenID Connect are Enterprise-only** . **Konnect** provides managed control plane with self-hosted runtime for data residency . **Full API lifecycle**: developer portal, analytics, and transformation .



- **[Traefik Enterprise](https://traefik.io/)**  

  **Unified cloud-native networking** bringing **Ingress, Service Mesh, and API Gateway** into one control plane . Built on open-source Traefik Proxy and Traefik Mesh . Features **distributed rate limiting**, **LDAP/JWT/OAuth2/OIDC authentication**, **automatic HTTPS with unlimited Let's Encrypt certificates**, and **hybrid routing** for progressive migration from legacy to cloud-native . **24/7 enterprise support** included . Users value **automatic service discovery** and **dynamic configuration without restarts** .



- **[HAProxy Enterprise](https://www.haproxy.com/)**  

  **The enterprise edition of the high-availability load balancer** . Includes **validated, pre-configured modules** for botnet protection, client fingerprinting, APT protection, and content auto-update . **Long Term Support branch** extensively tested before packaging . **Ingress Controller pricing**: **$366/month per instance** on AWS Marketplace . Handles **10,000+ simultaneous connections** . **The most performant option** for raw TCP/HTTP load balancing at scale.



- **[Apigee (Google Cloud)](https://cloud.google.com/apigee)**  

  **Google's full-lifecycle API management platform** . **API proxies** map public HTTP endpoints to backend services—handling security, authorization, analytics, and monitoring without backend changes . **Apigee hybrid** runs runtime plane on-premises while management plane runs in Google Cloud—**API traffic and data confined within enterprise boundaries** . **Supports gRPC**, **KVMs for configuration**, **monetization**, and **Trace/Debug sessions** . **The most expensive option**—reported as **69x more expensive than Kong** for equivalent scale . **The enterprise standard** for regulated industries requiring data residency.



- **[Ambassador Edge Stack](https://www.getambassador.io/)**  

  **Kubernetes-native API gateway built on Envoy Proxy** . **Declarative, self-service management via Kubernetes CRDs**—enables GitOps-style continuous delivery . Features **developer portal**, **OpenID Connect SSO**, **rate limiting**, **circuit breakers**, and **automatic retries** . **Core Emissary-ingress is Apache 2.0**; some features (like SSO) are proprietary but **free for up to 5 requests/second** . **Trusted by Chick-Fil-A, ADP, Microsoft, NVidia, and AppDirect** . **Designed for north-south traffic** (into the cluster), complementary to service meshes for east-west .



- **[Tyk Gateway](https://tyk.io/)**  

  **Batteries-included open-source Enterprise API Gateway**—no feature lockout . **Supports REST, GraphQL, TCP, and gRPC** . **No 3rd-party dependencies** aside from Redis for distributed rate limiting . **OpenAPI 3.0 as source of truth**—import Swagger/OAS2/3 to scaffold APIs . Features **hitless reloads**, **API versioning**, **granular access control**, and **extensible plugin architecture** (JavaScript, Go, or gRPC) . **5M+ DockerHub pulls, 6K+ GitHub stars** .



- **[Zuul (Netflix)](https://github.com/Netflix/zuul)**  

  **Netflix's L7 application gateway** providing **dynamic routing, monitoring, resiliency, and security** for edge services . **Zuul 2 uses Netty for non-blocking I/O** . **Filter pipelines** (inbound, endpoint, outbound) are the core extension point for authentication, routing, rate limiting, and response decoration . **Push Messaging** enables server-to-client communication over WebSockets and SSE . **The original cloud-native gateway**—still used at Netflix scale.



- **[KrakenD Enterprise](https://www.krakend.io/)**  

  **Stateless API gateway focused on API aggregation** (Backend-for-Frontend) . **Single Go binary, no runtime database**—declarative JSON config loaded at startup with hot reload . **Native multi-backend response aggregation**—merge, filter, and reshape multiple backends into one response . **Flat-tiered pricing**—every feature included at every tier, no traffic-based uplift . **40,000–80,000 RPS per instance** with stateless horizontal scaling . **AI Gateway** with AWS Bedrock support, token usage dashboards, and provider fallback .



## Open-Source GitHub Projects



- **[Traefik](https://github.com/traefik/traefik)**  

  **The Cloud Native Application Proxy** (MIT) . **65,000+ GitHub stars** . **The modern HTTP reverse proxy and load balancer that makes deploying microservices easy**—**listens to your orchestrator API and instantly generates routes** without manual configuration . **Supports Docker, Swarm, Kubernetes, ECS, Consul, Etcd, Rancher, and more** . **Features**: automatic Let's Encrypt HTTPS (wildcard certs), circuit breakers, retries, WebSocket/HTTP2/gRPC, clean web UI, metrics (Prometheus, Datadog, StatsD, InfluxDB), access logs (JSON, CLF), and **single binary deployment** . **Maintained**: 30 commits in last 90 days, OpenSSF scorecard 6.5/10 . **The most popular open-source cloud-native ingress** for Kubernetes and Docker.



- **[Kong Gateway (OSS)](https://github.com/Kong/kong)**  

  **The most widely adopted open-source API gateway** (Apache-2.0) . Built on **NGINX/OpenResty (Lua)** with **PostgreSQL (traditional) or DB-less mode** . **100+ plugins** for authentication, rate limiting, and transformation . **Full Admin API** and **decK declarative GitOps** . **Trade-offs**: PostgreSQL dependency adds operational overhead; OpenID Connect and other advanced plugins are Enterprise-only; no native multi-backend response aggregation . **The default open-source choice** for plugin breadth and API management depth.



- **[Envoy Gateway](https://github.com/envoyproxy/gateway)**  

  **The Kubernetes Gateway API implementation powered by Envoy Proxy** (Apache-2.0) . **Extends the Kubernetes Gateway API** with additional capabilities via CRDs: **BackendTrafficPolicy** (circuit breakers, rate limiting), **ClientTrafficPolicy** (TLS, timeouts, proxy chains), and **SecurityPolicy** (mTLS, JWT, API keys) . **Install via Helm**: `helm install eg oci://docker.io/envoyproxy/gateway-helm` . **BackendTrafficPolicy** provides **per-backend circuit breaker counters**—issues with one backend don't affect others . **The most Kubernetes-native approach** to gateway configuration.



- **[HAProxy Community](https://github.com/haproxy/haproxy)**  

  **The most widely deployed open-source load balancer** (GPL-2.0) . **High-availability, reliable performance** for TCP and HTTP applications . **Supports round-robin, least connections, URL hash, and random algorithms** . **The foundation of HAProxy Enterprise** . **The performance reference** for load balancing—used in some of the most demanding platforms worldwide .



- **[Tyk Gateway (OSS)](https://github.com/TykTechnologies/tyk)**  

  **Open-source Enterprise API Gateway** (MPL-2.0) . **No feature lockout**—same gateway used by Tyk for all applications . **No 3rd-party dependencies** aside from Redis . **Supports REST, SOAP, GraphQL, gRPC, and TCP** . **OpenAPI 3.0 as source of truth**, **hitless reloads**, **API versioning**, and **extensible plugins** . **The most "batteries-included" open-source gateway**—everything works out of the box.



- **[Emissary-ingress](https://github.com/emissary-ingress/emissary)**  

  **CNCF Incubating project**—the open-source core of Ambassador Edge Stack (Apache-2.0) . **Kubernetes-native API gateway built on Envoy** . **Declarative CRD-based configuration** for GitOps workflows . **The free foundation** for teams that want Ambassador's architecture without the commercial features.



- **[Zuul (Open Source)](https://github.com/Netflix/zuul)**  

  **Netflix's L7 application gateway** (Apache-2.0) . **Zuul 2 uses Netty for non-blocking I/O** . **Filter pipelines** for custom logic . **Push Messaging** for WebSocket/SSE . **The original Netflix gateway**—still maintained and used in production.



- **[KrakenD (Community)](https://github.com/krakend/krakend-ce)**  

  **Stateless API gateway for aggregation** (Apache-2.0) . **Single Go binary, no runtime database** . **Native multi-backend response aggregation**—merge, filter, and reshape multiple backends into one response . **40,000–80,000 RPS per instance** . **The same runtime as Enterprise**—teams can validate before licensing .



### Additional Strong Open-Source Options



- **[Apache APISIX](https://github.com/apache/apisix)** — Cloud-native API gateway (Apache-2.0) with full dynamic routing, multi-protocol support (HTTP, gRPC, WebSocket, MQTT), and rich plugin ecosystem. **14,000+ GitHub stars.**

- **[Kong Ingress Controller](https://github.com/Kong/kubernetes-ingress-controller)** — Kubernetes Ingress Controller powered by Kong Gateway.

- **[Traefik Mesh](https://github.com/traefik/mesh)** — Open-source service mesh built on Traefik Proxy for east-west traffic .

- **[Fabio](https://github.com/fabiolb/fabio)** — Fast, modern, zero-conf load balancing HTTP(S) router for Consul.

- **[Vulcand](https://github.com/vulcand/vulcand)** — Programmatic extendable reverse proxy built on Etcd.

- Community **n8n** workflows for gateway configuration management and traffic alert automation.



**Frameworks for building custom systems**: Combine **Traefik** for dynamic service discovery with **Kong** or **Tyk** for plugin-rich API management, **Envoy Gateway** for Kubernetes-native configuration, **HAProxy** for raw performance, and **KrakenD** for stateless aggregation—creating a fully self-hosted, enterprise-grade traffic management platform.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- API gateways and reverse proxies handling production traffic must follow security best practices and comply with data protection regulations.

- **Open-source API gateways are mature and production-ready.** Traefik (65K+ stars) handles dynamic service discovery for Kubernetes and Docker . Kong (100+ plugins) provides full API lifecycle management . Tyk offers "batteries-included" functionality with no feature lockout . **These are genuine alternatives to commercial platforms.**

- **Architecture choice matters more than feature lists.** Kong is database-backed (or DB-less) and plugin-rich; KrakenD is stateless and aggregation-focused . Traefik discovers services automatically; NGINX requires explicit configuration . **Choose based on your operational model, not benchmark charts.**

- **The hidden cost of self-hosting is engineering time.** A platform team spending one day per week maintaining a Kong cluster represents a significant fraction of a senior engineer's salary—**this cost rarely appears on an invoice but weighs heavily on the budget** . Even "expensive" managed services can be cheaper than dedicated maintenance.

- **Apigee is 69x more expensive than Kong at scale** —but it provides **full API lifecycle management**, **monetization**, and **hybrid deployment** for regulated industries . **The premium buys governance, not just routing.**

- Self-hosted open-source solutions require proper security hardening, certificate management, and ongoing maintenance. **API gateways are critical infrastructure**—plan for high availability, monitoring, and disaster recovery.



---



**Made for platform engineers, SREs, and developers building transparent traffic management solutions.**

Let's make API Gateway & Reverse Proxy more open, data-driven, and cloud-native.
