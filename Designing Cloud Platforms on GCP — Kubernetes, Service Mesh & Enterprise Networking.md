# **Full Index (Chapters 1–50)**

## **Part 1 – Foundations**

### **Chapter 1 — Project Context, Non-Functional Requirements & Platform Purpose**

1.1 Business & Technical Context  
 1.1.1 SaaS platform overview  
 1.1.2 Market drivers and customer expectations  
 1.1.3 Why GCP + Kubernetes? Strategic considerations  
1.2 Non-Functional Requirements (NFRs)  
 1.2.1 Availability targets  
 1.2.2 Latency and performance requirements  
 1.2.3 Scalability expectations  
 1.2.4 Compliance obligations (PCI, SOC2, GDPR, HIPAA)  
1.3 Constraints & Assumptions  
 1.3.1 Organizational constraints  
 1.3.2 Legacy systems and hybrid dependencies  
 1.3.3 Security and data residency constraints

---
### **Chapter 2 — Mental Models for Cloud, Kubernetes, and Modern Service Platforms**

2.1 Cloud-Native Fundamentals
	2.1.1 Cattle vs pets
	2.1.2 Declarative vs imperative infrastructure
	2.1.3 Control plane vs data plane thinking
2.2 Kubernetes Mental Models
	2.2.1 Kubernetes as a scheduler
	2.2.2 Pods as the unit of compute
	2.2.3 Reconciliation loops & desired state
2.3 Networking Mental Models
	2.3.1 East–west vs north–south traffic
	2.3.2 Layer 4 vs Layer 7 routing
	2.3.3 Identity as the new perimeter
2.4 Reliability Mental Models
	2.4.1 SLOs as platform contracts
	2.4.2 Failure domains
	2.4.3 Observability as a first-class feature

---
### **Chapter 3 — GCP Fundamentals for Enterprise-Scale Architectures**

3.1 GCP Resource Hierarchy  
3.2 IAM Model & Grant Scoping  
3.3 Networking Fundamentals (VPC, Subnets, Routes, Firewalls)  
3.4 GCP Service-to-Service Interactions  
3.5 Regional vs Zonal Behaviors  
3.6 Quotas, Limits, and Scaling Characteristics

---

### **Chapter 4 — Kubernetes, GKE, and Service Mesh Target-State Overview**

4.1 What the Final Platform Looks Like  
4.2 Architectural Pillars (Security, Reliability, Observability, Cost, Velocity)  
4.3 Core Platform Components  
 GKE clusters  
 Ingress gateways  
 Istio service mesh  
 Observability pipeline  
 CI/CD + GitOps  
 IaC pipeline  
4.4 How Customer Workloads Flow Through the System

---

### **Chapter 5 — Ways of Working as a Senior Cloud/Infra Engineer**

5.1 RFCs & Design Documents  
5.2 Operational Maturity & Runbook Culture  
5.3 Effective Incident Response  
5.4 Collaboration With App Teams & SRE  
5.5 Architectural Decision Records (ADRs)

---

## **Part 2 – Designing the Target Architecture**

### **Chapter 6 — Organizations, Folders, Projects & Environment Strategy**

6.1 Resource Hierarchy Best Practices  
6.2 Separating Prod, Non-Prod, and Sandbox  
6.3 Shared Services Projects  
6.4 Folder-Based Policy Enforcement  
6.5 Multi-Project Patterns for Microservices

---

### **Chapter 7 — GKE Cluster Architecture: Regional, Multi-Cluster, Multi-Region**

7.1 Why Regional Clusters?  
7.2 Workload Separation Strategies  
7.3 Multi-Cluster Patterns  
 7.3.1 Cluster-per-team  
 7.3.2 Cluster-per-type  
 7.3.3 Hub-and-spoke clusters  
7.4 Multi-Region Platforms  
 7.4.1 Active-active vs active-passive  
 7.4.2 Global traffic distribution

---

### **Chapter 8 — Multi-Tenancy, Data Residency, and Security Boundaries**

8.1 Tenant Isolation Models  
 Namespaces  
 Clusters  
 Projects  
 VPCs  
8.2 Data Residency  
8.3 Service Perimeters  
8.4 Cross-tenancy Communication Controls

---

### **Chapter 9 — Domain-Driven Design, Service Topologies & API Partitioning**

9.1 Domain Decomposition  
9.2 Service Boundaries & Interactions  
9.3 North–South vs East–West Service Design  
9.4 Anti-Patterns (Mega-services, Chatty APIs)

---

### **Chapter 10 — Migration Strategy: Strangler Fig, Transitional Patterns**

10.1 Mapping the Legacy Monolith  
10.2 Extracting Services Gradually  
10.3 Hybrid Deployments  
10.4 Phased Rollout Patterns  
10.5 Sunset & Decommissioning

---

## **Part 3 – Networking**

### **Chapter 11 — VPC Design, Shared VPC & CIDR Strategy**

11.1 VPC Fundamentals  
11.2 Shared VPC Architecture  
11.3 IP Address Planning  
11.4 Subnet Delegation  
11.5 VPC Scaling & Limits

---

### **Chapter 12 — Subnets, Firewalls & Routing**

12.1 Subnet Design  
12.2 Hierarchical Firewalls & Policies  
12.3 Dynamic Routing & Route Priorities  
12.4 Private Google Access  
12.5 AWS vs GCP Routing (Conceptual Comparison)

---

### **Chapter 13 — Hybrid Connectivity: VPN, Interconnect & BGP**

13.1 Cloud VPN (IPSec)  
13.2 HA VPN Architecture  
13.3 Dedicated & Partner Interconnect  
13.4 BGP Design & Failover  
13.5 Redundancy Models

---

### **Chapter 14 — Multi-Region Networking & Egress Optimization**

14.1 Interconnect Between Regions  
14.2 Peering Options & Constraints  
14.3 Egress Cost Minimization  
14.4 MTU, Latency & Packet Fragmentation Pitfalls

---

### **Chapter 15 — DNS Architecture & Service Discovery**

15.1 Cloud DNS Overview  
15.2 Private Zones  
15.3 Split-Horizon DNS  
15.4 Cross-Region DNS Patterns  
15.5 Mesh-Based Service Discovery

---

### **Chapter 16 — Networking Failure Modes**

16.1 Overlapping CIDRs  
16.2 Route Leaks  
16.3 Hairpinning  
16.4 Misconfigured NAT  
16.5 Network Security Anti-Patterns

---

## **Part 4 – Kubernetes & Mesh**

### **Chapter 17 — GKE Cluster Internals, Node Pools, and Autoscaling**

17.1 Control Plane Internals  
17.2 Node Pool Design  
17.3 Autoscaling (HPA, VPA, CA)  
17.4 Node Upgrades & Surge Control

---

### **Chapter 18 — Pod Lifecycle, Scheduling & Resource Engineering**

18.1 Pod Lifecycle States  
18.2 Scheduling Features (Affinity, Taints, Priorities)  
18.3 Resource Requests & Limits  
18.4 Vertical & Horizontal Scaling  
18.5 Quotas & LimitRanges

---

### **Chapter 19 — GKE Networking: CNI, Services, Ingress, NEGs**

19.1 CNI Options & Pod CIDRs  
19.2 NodePorts & LoadBalancers  
19.3 GKE Ingress Controller  
19.4 NEGs (Zonal, Regional, L7)  
19.5 Internal vs External LoadBalancing

---

### **Chapter 20 — Istio / Envoy Fundamentals**

20.1 Control Plane Architecture  
20.2 Data Plane: Sidecars & Proxies  
20.3 xDS Protocol (ADS, LDS, RDS, EDS)  
20.4 Identity & mTLS (SPIFFE/SPIRE)  
20.5 Telemetry v2 Pipeline

---

### **Chapter 21 — Traffic Management: Blue/Green, Canary, Failover**

21.1 Routing Rules & VirtualServices  
21.2 Weighted Routing  
21.3 Canary Releases  
21.4 Regional Failover Through Mesh  
21.5 Service Entry / Egress Control

---

### **Chapter 22 — Resilience Patterns**

22.1 Timeouts, Retries & Backoff  
22.2 Circuit Breaking  
22.3 Outlier Detection  
22.4 Fail-Fast Design  
22.5 Multi-Region Resilience Design

---

### **Chapter 23 — Progressive Mesh Adoption**

23.1 Sidecar Injection Strategy  
23.2 Ingress Gateway Migration  
23.3 Gradual Onboarding of Services  
23.4 Ambient Mesh Overview  
23.5 Mesh Anti-Patterns

---

## **Part 5 – Reliability & Observability**

### **Chapter 24 — SLIs, SLOs & Error Budgets**

24.1 Choosing SLIs  
24.2 Setting SLOs  
24.3 Error Budgets  
24.4 Dashboards & Measurement

---

### **Chapter 25 — Observability Stack**

25.1 Metrics  
25.2 Logs  
25.3 Traces  
25.4 Exemplars  
25.5 GCP Cloud Operations Suite

---

### **Chapter 26 — High Availability Architecture**

26.1 Zonal Failure Design  
26.2 Regional Architectures  
26.3 Multi-Region Active/Active  
26.4 Stateful Workload Considerations

---

### **Chapter 27 — Disaster Recovery & Failover Runbooks**

27.1 RPO/RTO Framework  
27.2 Backup Strategy  
27.3 Cluster Rebuild Procedures  
27.4 Failover Automation  
27.5 DR Testing

---

### **Chapter 28 — Chaos Engineering & Incident Simulations**

28.1 Fault Injection  
28.2 Game Days  
28.3 Observability Validation

---

### **Chapter 29 — Safe Deployments & Blast Radius Control**

29.1 Progressive Delivery  
29.2 Rollback Strategy  
29.3 Multi-Region Deployment Waves  
29.4 Feature Flag Safety

---

## **Part 6 – Security**

### **Chapter 30 — Zero-Trust Networking & Segmentation**

30.1 Zero-Trust Principles  
30.2 Network Segments  
30.3 Perimeter Reduction  
30.4 Identity-Aware Proxy (IAP)

---

### **Chapter 31 — IAM, Service Accounts & Workload Identity**

31.1 IAM Roles & Design Patterns  
31.2 Service Account Design  
31.3 Workload Identity Federation  
31.4 Identity Escalation Risks

---

### **Chapter 32 — Secrets Management**

32.1 Secret Manager  
32.2 KMS & Encryption Hierarchies  
32.3 Secret Rotation  
32.4 Secret Anti-Patterns

---

### **Chapter 33 — Audit Logging, Threat Detection & Forensics**

33.1 Admin Activity Logs  
33.2 Data Access Logs  
33.3 SCC (Security Command Center)  
33.4 IR Playbooks (High level)

---

### **Chapter 34 — Policy-as-Code & Guardrails**

34.1 OPA/Gatekeeper  
34.2 Organization Policies  
34.3 CI Guardrails  
34.4 Security Bottleneck Anti-Patterns

---

### **Chapter 35 — Supply Chain Security**

35.1 SLSA Levels  
35.2 SBOMs  
35.3 Binary Authorization  
35.4 Image Signing & Verification

---

## **Part 7 – Infrastructure-as-Code & Delivery**

### **Chapter 36 — Terraform Architecture**

36.1 Module Design  
36.2 State Layout (Layers, Environments)  
36.3 CI Integration  
36.4 Testing Terraform Code

---

### **Chapter 37 — CI/CD for Infra & Applications**

37.1 Pipeline Patterns  
37.2 Cloud Build vs GitHub Actions vs GitLab  
37.3 Promotion Between Environments  
37.4 Pipeline Security

---

### **Chapter 38 — GitOps for Clusters & Mesh**

38.1 ArgoCD Concepts  
38.2 Flux Concepts  
38.3 App of Apps Pattern  
38.4 Drift Detection & Auto-Heal

---

### **Chapter 39 — Config & Feature Flag Management**

39.1 ConfigMap & Secret Best Practices  
39.2 Dynamic Configuration  
39.3 Feature Flags  
39.4 Configuration Anti-Patterns

---

### **Chapter 40 — Testing Infrastructure**

40.1 Unit Testing  
40.2 Integration Testing  
40.3 Conformance Testing (K8s, Mesh)  
40.4 Smoke Tests

---

## **Part 8 – Cost Management**

### **Chapter 41 — How GCP Bills You**

41.1 Compute  
41.2 Networking  
41.3 Storage  
41.4 Managed Services

---

### **Chapter 42 — Cost-Efficient Network Design**

42.1 Peering  
42.2 CDN/Caching  
42.3 Egress Controls  
42.4 Multi-Region Cost Pitfalls

---

### **Chapter 43 — GKE Cost Optimization**

43.1 Spot/Preemptible  
43.2 Node Type Selection  
43.3 Workload Rightsizing  
43.4 Bin Packing & Scheduling

---

### **Chapter 44 — Cost Visibility & Chargeback**

44.1 Labeling Strategy  
44.2 BigQuery Export  
44.3 Dashboards  
44.4 Budget Alerts

---

### **Chapter 45 — Cost vs Reliability vs Performance**

45.1 Tradeoffs & Decision Making  
45.2 Optimization Frameworks

---

## **Part 9 – Operations, Failures & Anti-Patterns**

### **Chapter 46 — Runbooks**

46.1 Latency Spikes  
46.2 Error Spikes  
46.3 Regional Failures

---

### **Chapter 47 — Debugging GKE Networking**

47.1 CNI Debugging  
47.2 iptables Basics  
47.3 Envoy Debugging  
47.4 DNS Debugging

---

### **Chapter 48 — TLS/mTLS Issues**

48.1 Certificate Chains  
48.2 SNI & SAN Issues  
48.3 Trust Model Failures  
48.4 Rotation Failures

---

### **Chapter 49 — Real Failures & Lessons**

49.1 Packet Loss Incidents  
49.2 Data Loss Near Misses  
49.3 Latency Cascades  
49.4 Cross-Region Misroutes

---

### **Chapter 50 — Anti-Patterns**

50.1 Snowflake Clusters  
50.2 Mesh Rule Overgrowth  
50.3 YAML Sprawl  
50.4 Runbook Gaps

---

# **Chapter 1 — Project Context, Non-Functional Requirements & Platform Purpose**

_(Expanded, senior-level, clear, and practical)_

---

# **1.1 Business & Technical Context**

---

## **1.1.1 SaaS Platform Overview**

A modern SaaS platform must provide a **secure, scalable, multi-tenant foundation** for delivering web applications and APIs to customers worldwide. Although your specific platform may differ in features, all SaaS systems share several architectural expectations:

### **Core Characteristics of the SaaS Platform**

- **Multi-tenancy** — customer environments must be logically isolated but able to share underlying infrastructure for cost efficiency.
    
- **Elastic compute** — workloads scale based on traffic, user adoption, and internal batch jobs.
    
- **Global reach** — users may connect from multiple regions; latency and consistency models matter.
    
- **Always available APIs** — the platform must maintain predictable uptime even during deployments, upgrades, and failures.
    

### **Representative Workloads**

- Stateless microservices providing user-facing APIs
    
- Background workers and schedulers
    
- Web frontends backed by CDN
    
- Data and streaming pipelines (optional but typical in SaaS)
    

### **Example: High-Level Request Flow**

```
User → CDN → Cloud Load Balancer → Ingress Gateway → GKE Service → Database / Cache
```

### **Pitfalls**

- Underestimating early network design → painful future migrations
    
- Overloading clusters with incompatible workloads (I/O heavy, batch, CPU-bound)
    
- Building a monolithic deployment process in a multi-tenant environment
    

---

## **1.1.2 Market Drivers and Customer Expectations**

Customers compare your platform not only to competitors in your domain but also to the operational quality of hyperscale cloud products (Google Workspace, GitHub, Stripe, etc.). This raises expectations in several categories:

### **Key Market Drivers**

- **Speed of delivery** — customers expect rapid feature rollouts with minimal downtime.
    
- **Resilience** — users assume the platform stays available despite failures or maintenance.
    
- **Security** — modern procurement processes evaluate SOC2, ISO 27001, GDPR, and network isolation.
    
- **Cost transparency** — customers expect predictable pricing with no surprise charges.
    

### **Typical Customer Expectations**

|Category|Expectation|
|---|---|
|**Performance**|Sub-100ms p95 latency for core APIs|
|**Availability**|99.9%–99.99% uptime SLA|
|**Compliance**|SOC2 Type II, GDPR, possibly HIPAA/PCI|
|**Security**|mTLS, encrypted storage, access auditing|
|**Supportability**|Clear runbooks and incident communication|

### **Pitfalls**

- Attempting to satisfy all compliance regimes before understanding actual customer requirements
    
- Ignoring early global expansion needs → later requiring expensive multi-region refactors
    

---

## **1.1.3 Why GCP + Kubernetes? Strategic Considerations**

Choosing **GCP** and **Kubernetes** should be driven by engineering and business outcomes, not trend-following. Senior engineers must articulate these strategic reasons:

### **Why GCP?**

- **Superior networking backbone** — global VPC, cross-region HA patterns, high-quality interconnect
    
- **Regional GKE control planes** — a strong balance of cost, availability, and operational simplicity
    
- **Native observability** — Cloud Operations is deeply integrated and easy to extend
    
- **Built-in security controls** — VPC Service Controls, IAM modeling, Cloud Armor, SCC
    
- **Cost-effective edge + CDN** with Cloud CDN
    

### **Why Kubernetes (GKE)?**

- **Workload portability** — consistent deployment model across environments
    
- **Autoscaling at multiple layers** — HPA, VPA, CA, multi-dimensional scaling
    
- **Declarative configuration** — predictable rollout and rollback
    
- **Rich ecosystem** — Istio, Gatekeeper, ArgoCD, Crossplane, etc.
    
- **Separation of concerns** — platform team controls cluster; product teams deploy workloads
    

### **Example: Simple GKE Cluster Creation**

```bash
gcloud container clusters create my-saas-cluster \
  --region=us-central1 \
  --release-channel=regular \
  --node-locations=us-central1-a,us-central1-b,us-central1-f \
  --enable-ip-alias \
  --enable-autoscaling --min-nodes=3 --max-nodes=15 \
  --enable-shielded-nodes
```

**Comments:**

- `--enable-ip-alias` is required for VPC-native clusters.
    
- `--enable-autoscaling` supports cost-optimized scaling.
    
- Regional clusters span zones automatically.
    

### **Pitfalls**

- Building “cloud-agnostic” abstractions → reduces performance **and** increases cost
    
- Underestimating Kubernetes operational overhead without a platform team
    
- Choosing zonal clusters for cost-saving → later scrambling to meet uptime targets
    

---

# **1.2 Non-Functional Requirements (NFRs)**

Non-functional requirements are the **contract** that the platform must fulfill for the business. They drive architectural choices, especially around redundancy, automation, and security.

---

## **1.2.1 Availability Targets**

Availability defines how much downtime the platform is allowed over a period.

### **Typical SaaS Availability Targets**

|Availability|Max Downtime Per Month|
|---|---|
|**99.9%**|~43 minutes|
|**99.95%**|~22 minutes|
|**99.99%**|~4.4 minutes|

### **Technical Implications**

- **Regional clusters**, not zonal
    
- Multi-zone node pools
    
- Database high-availability replicas
    
- Rolling upgrades for workloads
    
- Load balancers and ingress gateways with health checks
    

### **Example: Readiness Probe to Avoid Rolling Out Bad Pods**

```yaml
readinessProbe:
  httpGet:
    path: /healthz
    port: 8080
  initialDelaySeconds: 5
  periodSeconds: 10
  failureThreshold: 3
```

**Comments:** Ensures a bad revision doesn't degrade availability by entering the serving pool prematurely.

### **Common Pitfall**

- Using Kubernetes liveness probes incorrectly → cascading pod restarts → outages
    

---

## **1.2.2 Latency and Performance Requirements**

Performance requirements determine cluster shape, autoscaling, and cross-region traffic distribution.

### **Typical Targets**

- **API p95 latency**: < 100 ms
    
- **Webpage TTFB**: < 200 ms
    
- **Batch processing windows**: defined by business SLAs
    

### **How Latency Affects Architecture**

- Regional presence → reduce transcontinental latency
    
- Caching layers (Redis, CDN, sidecar caching)
    
- Choosing the correct machine type for CPU/memory profiles
    
- Minimizing network hops inside clusters (e.g., avoid unnecessary proxies)
    

### **Small Example: HPA to Meet Latency Targets**

```yaml
apiVersion: autoscaling/v2
kind: HorizontalPodAutoscaler
metadata:
  name: api-service-hpa
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: api-service
  minReplicas: 3
  maxReplicas: 20
  metrics:
  - type: Resource
    resource:
      name: cpu
      target:
        type: Utilization
        averageUtilization: 60
```

**Comments:** CPU is often a proxy for latency under load.

### **Common Pitfall**

- Autoscaling on CPU alone when IO or upstream dependencies are bottlenecks
    

---

## **1.2.3 Scalability Expectations**

Scalability ensures that the platform can grow **in users**, **requests**, and **internal services**.

### **Scalability Dimensions**

1. **Horizontal workload scale** — more pods and nodes
    
2. **Service count scale** — more microservices
    
3. **Traffic scale** — surges, seasonal patterns
    
4. **Tenant scale** — number of customers or isolated environments
    

### **Cluster-Level Scalability Features**

- Multi-node pools for different workload types
    
- Node auto-provisioning
    
- Regional clusters for burst capacity
    
- GKE’s 15,000 nodes per cluster (upper bound, region dependent)
    

### **Pitfalls**

- Placing batch and interactive workloads in the same node pool
    
- Using cluster-first DNS for cross-namespace service calls → DNS bottlenecks under scale
    

---

## **1.2.4 Compliance Obligations**

Compliance is not optional in SaaS; it impacts logging, encryption, retention, access controls, and more.

### **Key Standards**

- **SOC2 Type II** — audits around controls, logging, access
    
- **GDPR** — data residency, right to erasure
    
- **PCI DSS** — required if processing payments
    
- **HIPAA** — required for healthcare data
    

### **Technical Requirements Derived**

- Mandatory audit logs
    
- Strict IAM scoping
    
- Encryption at rest + in transit
    
- Secure secret lifecycle
    
- Network isolation for sensitive services
    

### **Example: Enforcing Encryption With GCP KMS**

```bash
gcloud kms keys create app-key \
  --keyring=prod-ring \
  --location=us-central1 \
  --purpose=encryption
```

### **Pitfall**

- Over-engineering compliance tooling before a formal gap analysis
    

---

# **1.3 Constraints & Assumptions**

Constraints define what must be accepted; assumptions define what must be validated.

---

## **1.3.1 Organizational Constraints**

These vary by company but often include:

### **Common Constraints**

- **Small platform team** — limits operational complexity
    
- **Shared security team** — approval bottlenecks
    
- **Existing IAM rules** — cannot redesign from scratch
    
- **Release cadence** — weekly/monthly mandated releases
    

### **Impact on Architecture**

- Prefer managed services (GKE Autopilot, Cloud SQL, Cloud Load Balancing)
    
- Strict CI/CD must reduce manual change review
    
- Avoid patterns requiring 24/7 manual ops
    

### **Pitfall**

- Designing systems requiring more engineers than exist
    

---

## **1.3.2 Legacy Systems & Hybrid Dependencies**

Most SaaS platforms begin in hybrid mode: on-prem systems continue to provide identity, data, or batch jobs.

### **Typical Dependencies**

- Legacy user directory or SSO
    
- On-prem data sources (Oracle, MSSQL, NFS storage)
    
- Messaging systems like MQ/Kafka
    

### **Architectural Responses**

- HA VPN or Interconnect
    
- BGP stable routing
    
- Caching layers to reduce cross-prem latency
    
- Strangler patterns for incremental replacement
    

### **Example: Quick HA VPN Creation**

```bash
gcloud compute vpn-gateways create onprem-gw \
  --network=prod-vpc \
  --region=us-central1
```

### **Pitfall**

- Allowing hybrid dependencies to become permanent “anchors” inhibiting cloud-native design
    

---

## **1.3.3 Security & Data Residency Constraints**

Customers and regulators may dictate where data can live or flow.

### **Constraints Often Encountered**

- EU customer data must stay within EU regions
    
- Access to production resources must be tightly controlled
    
- All data must be encrypted with customer-owned keys (KMS + CMEK)
    

### **Architectural Implications**

- Multi-region clusters for residency
    
- Dedicated per-region databases
    
- Separate VPCs or projects for regulated data
    
- KMS key residency constraints tied to region
    

### **Example: Restricting Cross-Region Access With Firewall Rules**

```bash
gcloud compute firewall-rules create deny-cross-region \
  --network=prod-vpc \
  --direction=INGRESS \
  --priority=100 \
  --action=DENY \
  --source-ranges=10.10.0.0/16 \
  --target-tags=eu-services
```

### **Pitfall**

- Building a “global” service that unintentionally violates residency requirements
    

---

# **Chapter 2 — Mental Models for Cloud, Kubernetes, and Modern Service Platforms**

This chapter establishes the foundational mental models that senior cloud and platform engineers rely on to design, operate, and reason about distributed systems. These models reduce cognitive load, improve architectural clarity, and make debugging far more systematic.

---

# **2.1 Cloud-Native Fundamentals**

## **2.1.1 Cattle vs Pets**

### **Explanation**

- **Pets** are servers treated as unique, long-lived machines.
    
    - You name them (“db-prod-01”), you care for them, and you fix them when they break.
        
- **Cattle** are interchangeable compute instances.
    
    - They have no identity, they are disposable, and if something goes wrong, they are replaced—not repaired.
        

Modern cloud-native systems expect **cattle**:

- Always assume your workload can be rescheduled.
    
- Design for ephemeral compute.
    
- Store state outside compute instances.
    

### **Example**

An autoscaling group or Kubernetes Deployment treats Pods/VMs as cattle. They are continuously replaced by the orchestrator.

### **Common Pitfall**

- Treating Pods as pets—e.g., storing data in a container filesystem or assuming a Pod IP never changes.
    

---

## **2.1.2 Declarative vs Imperative Infrastructure**

### **Explanation**

- **Imperative:** “Do exactly these steps.”
    
    - Manual commands: `kubectl create`, `gcloud compute firewall-rules create`, SSH changes, etc.
        
- **Declarative:** “Here is the desired end state. The controller figures out how to get there.”
    
    - YAML manifests, Terraform, Kubernetes Operators, GitOps.
        

Declarative models scale because **controllers continuously reconcile**, enforcing correctness even after drift.

### **Example — Declarative Deployment**

```yaml
# deployment.yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: api
spec:
  replicas: 3                        # desired state: maintain 3 replicas
  selector:
    matchLabels:
      app: api
  template:
    metadata:
      labels:
        app: api
    spec:
      containers:
      - name: api
        image: europe-docker.pkg.dev/myproj/api:v1
```

Apply it:

```bash
kubectl apply -f deployment.yaml
```

### **Common Pitfall**

- Mixing imperative and declarative flows (e.g., manually changing replicas with `kubectl scale` while using GitOps).
    

---

## **2.1.3 Control Plane vs Data Plane Thinking**

### **Explanation**

Modern cloud platforms split responsibilities between:

- **Control Plane:** makes decisions
    
    - Kubernetes API server, controllers, load balancer config engines.
        
- **Data Plane:** moves user traffic or runs workloads
    
    - kubelet, Envoy sidecars, GKE dataplane VPC routing, nodes.
        

Correct mental model:

- **Control plane declares intent**,
    
- **Data plane executes requests**.
    

### **Example — GKE Load Balancer**

- Control plane: Google’s controller creates forwarding rules + NEGs.
    
- Data plane: packets flow through Google’s edge + health-checked endpoints.
    

### **Common Pitfall**

- Assuming "updating a Service" immediately affects traffic flow; in reality, the control plane update must propagate to the data plane.
    

---

# **2.2 Kubernetes Mental Models**

## **2.2.1 Kubernetes as a Scheduler**

### **Explanation**

Kubernetes is fundamentally a **distributed scheduler** driven by desired state:

- You tell it how many Pods you want.
    
- It picks optimal nodes based on constraints, resource requests, taints/tolerations, affinity rules.
    
- It continuously checks whether pods are running where and how they should.
    

It is **not**:

- A PaaS (though platforms can be built on it)
    
- A deployment tool (CI/CD handles that)
    

### **Diagnostic Example**

To see the scheduler’s decisions:

```bash
kubectl describe pod mypod
```

Look for:

- `Node:` assigned host
    
- `Events:` scheduling decisions, rejections, constraints
    

### **Common Pitfall**

- Underestimating the importance of resource requests/limits → leads to unpredictable scheduling and node pressure evictions.
    

---

## **2.2.2 Pods as the Unit of Compute**

### **Explanation**

Pods—not containers—are the **atomic unit of scheduling** in Kubernetes.

Correct mental model:

- A Pod is a **logical host**.
    
- Containers inside a Pod share:
    
    - network namespace (same IP)
        
    - storage volumes
        
    - IPC namespaces
        

### **Example Pod Manifest**

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: example
spec:
  containers:
  - name: app
    image: nginx
  - name: sidecar
    image: busybox
    command: ["sh", "-c", "echo running; sleep 3600"]
```

### **Common Pitfall**

- Using multiple containers in a Pod for unrelated applications.  
    Pods should contain tightly coupled containers only.
    

---

## **2.2.3 Reconciliation Loops & Desired State**

### **Explanation**

Every controller in Kubernetes implements a loop:

1. Observe current state
    
2. Compare to desired state
    
3. Make small changes toward desired
    

This model creates a **self-healing system**.

Controllers exist for:

- Deployments
    
- StatefulSets
    
- DaemonSets
    
- Horizontal autoscaling
    
- NetworkPolicy enforcement
    
- Node health
    

### **Inspecting Controller Activity**

```bash
kubectl get deploy api -o yaml
```

Look for:

- `status` vs `spec` differences
    

### **Common Pitfall**

- Trying to “fix” things with imperative commands while a controller is actively reconciling → your changes get reverted.
    

---

# **2.3 Networking Mental Models**

## **2.3.1 East–West vs North–South Traffic**

### **Explanation**

- **North–South:** traffic entering/exiting the cluster
    
    - Users → Load Balancer → Services
        
- **East–West:** internal service-to-service traffic
    
    - Pods → Pods
        
    - Nodes → Nodes
        

GCP example:

- North–South uses external load balancers (GCLB).
    
- East–West uses VPC routing, kube-proxy, or eBPF dataplanes.
    

### **Example — Viewing a Service’s Ingress Paths**

```bash
kubectl get svc frontend
kubectl describe svc frontend
```

### **Common Pitfall**

- Applying Layer 7 policies (JWT, mTLS) only to north–south traffic—leaving east–west traffic unsecured.
    

---

## **2.3.2 Layer 4 vs Layer 7 Routing**

### **Explanation**

- **Layer 4 routing** cares about IPs + ports (TCP/UDP).
    
    - NodePorts, LoadBalancers, ClusterIPs.
        
- **Layer 7 routing** understands HTTP, gRPC, hostnames, paths.
    
    - Ingress controllers, service meshes (Istio/Linkerd), API gateways.
        

### **L7 Example — Minimal Ingress Rule**

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: web
spec:
  rules:
  - host: example.com
    http:
      paths:
      - path: /
        pathType: Prefix
        backend:
          service:
            name: web-svc
            port:
              number: 80
```

### **Common Pitfall**

- Assuming an L7 Ingress controller handles non-HTTP traffic—many do not.
    

---

## **2.3.3 Identity as the New Perimeter**

### **Explanation**

Perimeter-based security is dead in cloud environments.  
Correct model: **identity-based, least-privilege authorization**.

Identity sources:

- GCP IAM service accounts
    
- Kubernetes service accounts
    
- mTLS identities (SPIFFE/SPIRE, Istio)
    
- Workload identity federation
    

Example mental model:

- Do not trust the network, trust **workload identity**.
    

### **Example — GKE Workload Identity Binding**

```bash
# Bind a Kubernetes ServiceAccount to a GCP IAM SA
gcloud iam service-accounts add-iam-policy-binding \
  my-gcp-sa@project.iam.gserviceaccount.com \
  --member="serviceAccount:project.svc.id.goog[default/api]" \
  --role="roles/storage.objectViewer"
```

### **Common Pitfall**

- Using node-level credentials instead of per-workload identity → accidental privilege escalation.
    

---

# **2.4 Reliability Mental Models**

## **2.4.1 SLOs as Platform Contracts**

### **Explanation**

SLOs (Service Level Objectives) define **what reliability looks like** from the customer’s perspective.  
They act as **contracts**:

- Platform must meet them.
    
- App teams design within them.
    

Good SLOs are:

- Measurable
    
- Meaningful
    
- Mapped to real user journeys
    

### **Example SLO**

- “99.9% of API requests succeed within 200 ms over a rolling 28-day window.”
    

### **Common Pitfall**

- Mistaking SLIs (metrics) or SLAs (business guarantees) for SLOs.
    

---

## **2.4.2 Failure Domains**

### **Explanation**

Failure domains are boundaries inside which a single failure can cause impact:

- Node
    
- Zone
    
- Region
    
- Cluster
    
- Entire cloud provider
    

Senior engineers design so that **failures stay within the smallest possible domain**.

### **Example — Zonal vs Regional GKE**

- Zonal cluster → single-zone failure = full outage
    
- Regional cluster → nodes across 3 zones = one zone lost but workloads remain available
    

### **Pitfall**

- Spreading stateful apps across zones without understanding **latency** or **quorum** implications.
    

---

## **2.4.3 Observability as a First-Class Feature**

### **Explanation**

Observability is not logging + metrics + traces.  
It is the ability to **ask new questions about a system without deploying new code**.

Mental model:

- Telemetry drives operations, debugging, scaling, and security.
    

Minimal observability includes:

- Metrics (Prometheus/OpenTelemetry)
    
- Logs (structured, indexed)
    
- Traces (distributed)
    
- Events (Kubernetes events)
    
- Health signals (readiness/liveness/startup probes)
    

### **Example — Readiness & Liveness Probes**

```yaml
livenessProbe:
  httpGet:
    path: /healthz
    port: 8080
  initialDelaySeconds: 5
  periodSeconds: 10   # container killed if fails

readinessProbe:
  httpGet:
    path: /ready
    port: 8080
  periodSeconds: 5     # pod removed from LB if fails
```

### **Common Pitfall**

- Overusing liveness probes → flapping → mass restarts  
    (use startup probes for slow-booting apps).
    

---

# **Chapter 3 — GCP Fundamentals for Enterprise-Scale Architectures**

_(Expanded with senior-level clarity, practical examples, commands, and pitfalls.)_

---

# **3.1 GCP Resource Hierarchy**

The GCP Resource Hierarchy defines **how infrastructure is organized**, how policies are inherited, and how access control is enforced. At enterprise scale, understanding this hierarchy is essential to avoid sprawl, privilege leakage, and operational complexity.

---

## **3.1.1 Hierarchy Structure**

The hierarchy flows top-down:

```
Organization → Folders → Projects → (Resources)
```

### **Organization**

- Root of the hierarchy.
    
- Centrally manages IAM, audit logs, constraints, and org-level policies.
    
- Required for enterprise-grade GCP usage.
    

### **Folders**

- Group projects by department, environment, business domain, or compliance boundary.
    
- Inherit policies from the Organization.
    
- Typically used to enforce security boundaries (e.g., production vs non-production).
    

### **Projects**

- The atomic billing + IAM boundary.
    
- Contain resources such as VMs, GKE clusters, networks, buckets, etc.
    
- Recommended to isolate workloads on a per-project basis for security and quota isolation.
    

### **Resources**

- Actual compute, networking, and storage artifacts.
    

---

## **3.1.2 Example: Creating a Folder & Project**

```bash
# Create folder under the organization
gcloud resource-manager folders create \
  --display-name="prod" \
  --organization=123456789012

# Create a project inside the folder
gcloud projects create prod-services \
  --folder=987654321000
```

**Comments:**

- The folder ID (`987654321000`) is required — not the name.
    
- This hierarchy helps apply organization policies such as restricting public IPs or allowed regions.
    

---

## **3.1.3 Common Pitfalls**

- **Using too few projects** → produces permission bloat and resource conflict.
    
- **Using too many projects** without automation → creates operational fragmentation.
    
- Not using folders → difficult to enforce consistent org policies.
    
- Placing production and non-production in the same folder → increases blast radius of policy errors.
    

---

# **3.2 IAM Model & Grant Scoping**

IAM in GCP uses a **policy inheritance model**, where roles at higher levels apply downward unless restricted by organizational policies.

---

## **3.2.1 IAM Basics**

### **Identities**

- Google Accounts (humans)
    
- Service Accounts (workloads/machines)
    
- Cloud Identity Groups (best practice for role assignment)
    

### **Role Types**

- **Primitive**: `roles/owner`, `editor`, `viewer` → never use in production.
    
- **Predefined**: Scoped roles like `roles/compute.admin`.
    
- **Custom**: Tailored to organizational needs, typically used to remove privilege excess.
    

---

## **3.2.2 Least Privilege Approach (Enterprise Standard)**

Assign roles at the **lowest level needed**:

|Identity|Scope|Example|
|---|---|---|
|Developer|Project|`roles/logging.viewer`|
|CI/CD SA|Project or Folder|`roles/container.developer`|
|Platform SA|Org-level|`roles/resourcemanager.folderAdmin`|

---

## **3.2.3 Example: Granting Project IAM**

```bash
# Grant a service account permission to deploy to GKE
gcloud projects add-iam-policy-binding prod-services \
  --member="serviceAccount:ci-cd@company.com" \
  --role="roles/container.developer"
```

**Comments:**

- This gives the CI/CD pipeline rights to deploy to Kubernetes.
    
- Keep grants scoped to individual projects unless absolutely required.
    

---

## **3.2.4 Common Pitfalls**

- Granting **primitive roles** → dangerous access expansion.
    
- Granting roles at the **organization level** when project-level is enough.
    
- Using **service account keys** instead of Workload Identity Federation → long-lived keys increase risk.
    
- Not using groups → leads to IAM policy drift and inconsistent access.
    

---

# **3.3 Networking Fundamentals (VPC, Subnets, Routes, Firewalls)**

GCP networking is global, scalable, and software-defined. Unlike AWS, VPCs can span regions, which affects design choices.

---

## **3.3.1 VPC Networks**

### **VPC Characteristics**

- Global resource with region-scoped subnets.
    
- Internal IPs are routable across regions.
    
- Can be shared across projects (Shared VPC).
    

### **When to Use Shared VPC**

- Central platform team manages networking.
    
- Application projects should not own network config.
    
- Strong isolation but shared connectivity.
    

---

## **3.3.2 Subnets**

Subnets are **regional**. Each subnet allocates IP space for:

- Compute Engine
    
- GKE nodes + pods
    
- Load balancer VIPs
    

### **Key Principles**

- Ensure large enough CIDRs for pod allocation.
    
- Avoid overlapping CIDRs with on-prem networks.
    

---

## **3.3.3 Routes**

Routes direct traffic inside the VPC.

### Route Types

- **System-generated** (most common; VPC-native)
    
- **Custom static routes**
    
- **BGP dynamic routes** via Cloud Router (hybrid connectivity)
    

---

## **3.3.4 Firewalls**

Firewall rules are stateful and applied at the **VPC level**.

### **Direction**

- Ingress
    
- Egress
    

### **Targets**

- Network tags
    
- Service accounts (preferred for identity-based rules)
    

---

## **3.3.5 Example: Create a Subnet and Firewall Rule**

```bash
# Create a subnet
gcloud compute networks subnets create backend-subnet \
  --network=prod-vpc \
  --region=us-central1 \
  --range=10.10.0.0/24

# Create a firewall rule allowing internal services only
gcloud compute firewall-rules create allow-internal \
  --network=prod-vpc \
  --direction=INGRESS \
  --action=ALLOW \
  --rules=tcp:80,tcp:443 \
  --source-ranges=10.0.0.0/8
```

---

## **3.3.6 Common Pitfalls**

- Creating overly small subnets → prevents cluster scaling.
    
- Misusing tags instead of service accounts → harder audits.
    
- Forgetting to enable Private Google Access → serverless services cannot access GCP APIs.
    
- Creating many custom routes → unnecessary complexity.
    

---

# **3.4 GCP Service-to-Service Interactions**

Services in GCP communicate through:

- Private Google Access (PGA)
    
- Private Service Connect (PSC)
    
- IAM service account impersonation
    
- Internal load balancing
    
- VPC Peering
    

Understanding these patterns ensures secure, efficient communication between GCP-managed services and your workloads.

---

## **3.4.1 Private Google Access (PGA)**

Allows VMs or GKE pods **without public IPs** to reach GCP APIs.

### **Enable Private Google Access**

```bash
gcloud compute networks subnets update backend-subnet \
  --region=us-central1 \
  --enable-private-ip-google-access
```

---

## **3.4.2 Private Service Connect (PSC)**

PSC lets services expose internal endpoints accessible only inside your networks.

### Common Uses

- Connect to Cloud SQL privately
    
- Offer internal APIs across projects
    
- Consume third-party services privately
    

---

## **3.4.3 IAM Service Account Impersonation**

Instead of keys, workloads impersonate service accounts.

### **Example: gcloud Impersonation**

```bash
gcloud auth print-access-token \
  --impersonate-service-account=deploy-sa@company.com
```

**Use Case:**  
A GKE workload deploying configurations to other clusters.

---

## **3.4.4 Common Pitfalls**

- Using public endpoints for internal GCP APIs → unnecessary egress costs.
    
- Using Cloud SQL public IPs when PSC or private IP is available.
    
- Hardcoding service account keys → violates compliance and increases risk.
    
- Failing to understand cross-project communication flows → creates debugging nightmares.
    

---

# **3.5 Regional vs Zonal Behaviors**

GCP resources fall into **three scopes**: global, regional, zonal. This affects HA, cost, and placement strategy.

---

## **3.5.1 Zonal Resources**

Examples:

- Compute Engine VMs
    
- Zonal GKE node pools
    
- Disks
    

**Failure Impact:** Losing a zone can cause service disruption if workloads are not spread.

---

## **3.5.2 Regional Resources**

Examples:

- Regional GKE clusters
    
- Regional Managed Instance Groups
    
- Cloud SQL (HA)
    
- Subnets
    

**Benefits:**

- Automatic replication across zones
    
- Higher availability SLAs
    

---

## **3.5.3 Global Resources**

Examples:

- VPC
    
- Load balancers
    
- Cloud Armor
    
- IAM
    

**Benefits:**

- Consistent global configuration
    
- Simplifies multi-region operations
    

---

## **3.5.4 Example: Creating a Regional GKE Cluster**

```bash
gcloud container clusters create backend-cluster \
  --region=us-central1 \
  --node-locations=us-central1-a,us-central1-b,us-central1-f \
  --enable-ip-alias \
  --release-channel=regular
```

**Comments:**

- A regional cluster automatically creates control plane replicas across zones.
    

---

## **3.5.5 Common Pitfalls**

- Deploying stateful workloads to zonal-only storage → single-zone failures cause outages.
    
- Confusing global L7 load balancers with regional L4 load balancers.
    
- Building multi-region apps on top of zonal databases → leads to data inconsistency.
    
- Using zonal MIGs behind global load balancers without multi-zone deployment → major reliability gap.
    

---

# **3.6 Quotas, Limits & Scaling Characteristics**

Quotas exist to protect tenants and ensure fair usage. Limits define system behavior.

At scale, many reliability issues are actually **quota issues**, not code issues.

---

## **3.6.1 Types of Quotas**

### **API Quotas**

Rate limits on API usage (e.g., Compute Engine API calls).

### **Resource Quotas**

Limits on CPUs, IP addresses, load balancers, firewall rules, etc.

### **Per-Project Quotas**

Each project has its own resource limits.

---

## **3.6.2 Example: Checking Quotas**

```bash
gcloud compute regions describe us-central1 \
  --project prod-services \
  --format="table(quotas.metric,quotas.limit,quotas.usage)"
```

---

## **3.6.3 Key Limits to Be Aware Of**

- Number of routes: **default 100**
    
- Number of firewall rules: **default 100**
    
- GKE nodes per cluster: **up to 15,000**
    
- Pods per node (GKE): depends on node type & mode
    
- PSC endpoints: region-specific quotas
    

---

## **3.6.4 Scaling Characteristics**

### **How GCP Behaves Under Load**

- Autoscaling might be delayed if region capacity is constrained.
    
- Cross-region traffic increases latency by 50–200 ms depending on proximity.
    
- GKE cluster autoscaler respects quotas; if exhausted → scale failure.
    
- Persistent Disk throughput grows with disk size (block mode).
    

---

## **3.6.5 Pitfalls**

- Not pre-requesting quota bumps before load tests or product launches.
    
- Treating quota errors as application errors → wrong debugging focus.
    
- Overusing small projects → quota fragmentation across projects.
    
- Running large-scale GKE clusters without planning for IP exhaustion.
    

---

# **Chapter 4 — Kubernetes, GKE, and Service Mesh Target-State Overview**

_(Expanded with senior-level clarity, diagrams-in-text, commands, YAML, and practical commentary.)_

---

# **4.1 What the Final Platform Looks Like**

This section describes the **target-state architecture** your engineering org aims to operate. It provides a mental model of what “good” looks like for a modern SaaS platform on GCP using Kubernetes and a service mesh.

---

## **4.1.1 High-Level View**

A mature platform looks like this:

```
                    ┌──────────────────────────────────┐
                    │      Global External Traffic     │
                    └──────────────────────────────────┘
                                   │
                          Global HTTPS LB
                                   │
                        (Cloud Armor, CDN, SSL)
                                   │
                        Ingress Gateway (Istio)
                                   │
             ┌─────────────────────┴─────────────────────┐
             │                                           │
     GKE Cluster A                               GKE Cluster B
      (Region 1)                                   (Region 2)
             │                                           │
      Mesh-Instrumented Services                 Mesh-Instrumented Services
             │                                           │
    Observability Pipeline (Metrics, Logs, Traces via Mesh Telemetry)
             │                                           │
                     Centralized Data Systems (SQL, Redis, Pub/Sub)
```

---

## **4.1.2 Characteristics of the Final Platform**

### **Unified deployment model**

All workloads use declarative manifests, GitOps automation, and mesh identity.

### **Consistent patterns across environments**

Dev, staging, and prod differ in _scale_ but not in _architecture_.

### **Cross-region failover**

Traffic can shift between clusters if one region degrades.

### **Zero-trust by default**

Mutual TLS (mTLS) between services, identity-driven policies, and no implicit trust.

### **Observability baked-in**

Every request produces metrics, logs, and traces automatically through sidecar/mesh telemetry.

---

## **4.1.3 Common Pitfalls**

- Designing for multi-region before stabilizing single-region ops.
    
- Overusing service mesh features early → complexity without value.
    
- Treating Ingress gateways like “just another Deployment” → they are critical control points.
    
- Deploying cluster-specific minutiae that break GitOps consistency.
    

---

# **4.2 Architectural Pillars**

A senior engineer must ensure the platform optimizes for **five fundamental pillars**. These pillars drive design decisions and are embedded into every platform component.

---

## **4.2.1 Security**

**Security is the default, not an option.**

Core security principles include:

- Workload identity (GCP Workload Identity + Istio identities)
    
- mTLS for all service-to-service communication
    
- Least-privilege IAM
    
- Network segmentation (namespace, project, VPC)
    
- Policy checks in CI (OPA, Gatekeeper, Conftest)
    

### **Example: Enforcing mTLS Namespace-Wide**

```yaml
apiVersion: security.istio.io/v1beta1
kind: PeerAuthentication
metadata:
  name: default-mtls
  namespace: payments
spec:
  mtls:
    mode: STRICT
```

**Comment:**  
All workloads in the `payments` namespace must use encrypted mesh communication.

---

## **4.2.2 Reliability**

Key reliability mechanisms:

- Regional clusters with multi-zone nodes
    
- Horizontal Pod Autoscaler + Cluster Autoscaler
    
- Ingress gateways with health checks
    
- Resilience policies (timeouts, retries, circuit breakers through mesh)
    
- Readiness/liveness probes
    

### **Example: Resilient Readiness Probe**

```yaml
readinessProbe:
  httpGet:
    path: /health
    port: 8080
  initialDelaySeconds: 5
  timeoutSeconds: 2
  periodSeconds: 10
  failureThreshold: 3
```

---

## **4.2.3 Observability**

Observability is not a luxury; it is how failures are detected, explained, and prevented.

Includes:

- Centralized logs
    
- Mesh-generated metrics (latency, error rate, throughput)
    
- Distributed tracing (Envoy sidecars)
    
- Exemplars for debugging specific slow requests
    
- SLO dashboards
    

### **Example: Sidecar Telemetry Configuration**

```yaml
apiVersion: telemetry.istio.io/v1alpha1
kind: Telemetry
metadata:
  name: default
spec:
  metrics:
    overrides:
    - match:
        metric: request_duration
      disabled: false
```

---

## **4.2.4 Cost**

A scalable platform must be cost-efficient:

- Autoscaling nodes down during low traffic
    
- Using spot/preemptible where safe
    
- Avoiding expensive cross-region traffic
    
- Right-sizing CPU/memory for workloads
    
- Using Cloud CDN to reduce backend load
    

**Pitfall:** Using mesh without request volume → cost overhead without value.

---

## **4.2.5 Velocity**

Velocity = shipping with confidence.

Components:

- GitOps for fast, repeatable deployments
    
- Automated testing pipelines
    
- Safe rollout patterns (canary, blue/green)
    
- Standardized templates and libraries
    
- Preview environments on pull requests
    

**Goal:** Code goes from commit → production with no manual steps except approvals.

---

# **4.3 Core Platform Components**

Now we break down each pillar of the platform stack.

---

## **4.3.1 GKE Clusters**

GKE provides the compute substrate.

### **Characteristics**

- Regional control plane (recommended)
    
- Multiple node pools (general workloads, high-memory, spot)
    
- Autopilot or Standard mode depending on control preferences
    
- Pod IP allocation from VPC-native ranges
    

### **Example: Creating a Regional GKE Cluster**

```bash
gcloud container clusters create primary \
  --region=us-central1 \
  --node-locations=us-central1-a,us-central1-b,us-central1-f \
  --enable-ip-alias \
  --release-channel=regular \
  --enable-shielded-nodes \
  --enable-autorepair \
  --enable-autoscaling --min-nodes=3 --max-nodes=20
```

### **Pitfalls**

- Mixing unrelated workloads in one cluster → noisy neighbor problems
    
- Overprovisioning node pools → wasteful spend
    
- Using zonal clusters for production
    

---

## **4.3.2 Ingress Gateways**

Ingress gateways provide the **north–south** edge and enforce:

- TLS termination
    
- Request routing
    
- External authentication
    
- Rate limiting
    
- WAF policies via Cloud Armor
    

### **Example: Istio Gateway**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: Gateway
metadata:
  name: public-gateway
  namespace: istio-system
spec:
  selector:
    istio: ingressgateway
  servers:
  - port:
      number: 443
      name: https
      protocol: HTTPS
    tls:
      mode: SIMPLE
      credentialName: prod-cert
    hosts:
    - "api.mycompany.com"
```

### **Pitfalls**

- Deploying multiple gateways per namespace → unnecessary complexity
    
- Not enabling Cloud Armor → exposure to volumetric attacks
    

---

## **4.3.3 Istio Service Mesh**

Istio enhances **east–west** reliability, security, and observability.

### **Key Mesh Features**

- mTLS by default
    
- Traffic routing (canary, failover, weighted splits)
    
- Retries, timeouts, circuit breaking
    
- Automatic telemetry (metrics, logs, traces)
    
- Policy enforcement
    

### **Example: Canary Routing**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: checkout-service
spec:
  hosts:
  - checkout.internal
  http:
  - route:
    - destination:
        host: checkout
        subset: v1
      weight: 90
    - destination:
        host: checkout
        subset: v2
      weight: 10
```

**Comment:**  
10% of traffic goes to version `v2`.

### **Pitfalls**

- Configuring retries too aggressively → request amplification during outages
    
- Deploying mesh across too many namespaces early
    

---

## **4.3.4 Observability Pipeline**

Observability pipeline typically consists of:

- Envoy sidecars → emit metrics/logs/traces
    
- Prometheus or managed Google Cloud Monitoring → metrics backend
    
- GKE logging agent (Fluent Bit) → log collection
    
- Jaeger/Zipkin/OpenTelemetry → distributed traces
    
- Dashboards and alerts based on SLOs
    

### **Example: Prometheus Operator Scrape Annotation**

```yaml
metadata:
  annotations:
    prometheus.io/scrape: "true"
    prometheus.io/port: "8080"
```

### **Pitfalls**

- Collecting **too many metrics** → massive storage cost
    
- Missing structured logging → hard to correlate incidents
    

---

## **4.3.5 CI/CD + GitOps**

### **CI Pipeline**

- Static analysis
    
- Unit tests
    
- Build container images
    
- Scan vulnerabilities
    
- Push to artifact registry
    

### **CD Pipeline (GitOps)**

- Git as source of truth
    
- Argo CD or Flux monitors Git
    
- Automatic reconciliation into cluster
    
- Rollbacks are Git reverts
    

### **Example: Argo CD Application**

```yaml
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: payments
spec:
  project: default
  source:
    repoURL: 'https://github.com/company/platform-configs'
    path: services/payments
    targetRevision: main
  destination:
    server: 'https://kubernetes.default.svc'
    namespace: payments
  syncPolicy:
    automated:
      prune: true
      selfHeal: true
```

### **Pitfalls**

- Allowing manual kubectl apply → drift between Git and cluster
    
- Too many repositories → fragmentation
    

---

## **4.3.6 IaC Pipeline**

Infrastructure-as-Code governs:

- VPCs
    
- Subnets
    
- GKE clusters
    
- IAM roles
    
- Load balancers
    
- Databases
    

### **Tooling**

- Terraform (most common)
    
- Terragrunt for environment layering
    
- Policy-as-code to catch misconfigurations early
    

### **Example: Terraform GKE Module**

```hcl
module "gke" {
  source  = "terraform-google-modules/kubernetes-engine/google"
  name    = "primary"
  region  = "us-central1"
  regional = true
  network = "prod-vpc"
  subnetwork = "gke-subnet"
}
```

### **Pitfalls**

- Not versioning Terraform modules per environment
    
- Hardcoding resource names → prevents multi-region expansion
    

---

# **4.4 How Customer Workloads Flow Through the System**

To understand the platform end-to-end, follow the flow of a single request.

---

## **4.4.1 Step-by-Step Request Flow**

### **1. User Request → Global Load Balancer**

- Receives HTTPS traffic
    
- Enforces Cloud Armor policies
    
- Terminates TLS or passes to gateway
    

### **2. LB → Ingress Gateway (Istio)**

- Routes based on hostname or path
    
- May enrich traffic with headers
    
- Sends to backend workloads inside the mesh
    

### **3. Gateway → Service Mesh**

- Traffic travels through Envoy sidecars
    
- mTLS encrypts internal traffic
    
- Policies applied: retries, timeouts, circuit breakers
    

### **4. Mesh → Application Pod**

- Pod processes request
    
- Generates logs/metrics/traces
    
- Calls other internal services via mesh
    
- Accesses storage or databases through private service endpoints
    

### **5. Application → External Services**

If needed:

- Cloud SQL via PSC
    
- Redis via Memorystore
    
- Pub/Sub with workload identity
    
- External APIs via Egress Gateway
    

### **6. Response → Back Through Mesh**

- Telemetry captured
    
- Response returned through ingress gateway
    
- Global LB returns response to user
    

---

## **4.4.2 Example: Request Flow Visualized**

```
User
 │
 ▼
[Global HTTPS LB] ──► [Cloud Armor] ──► [Istio Ingress Gateway]
                                     │
                                     ▼
                             [Envoy Sidecar]
                                     │
                                     ▼
                           [Application Pod]
                                     │
                                     ▼
                         [Datastore / PubSub / Redis]
```

---

## **4.4.3 Common Pitfalls**

- Allowing direct pod access from outside the mesh → breaks security invariants
    
- Misconfigured gateway hosts → 404s and routing failures
    
- Forgetting resource requests/limits → unpredictable latency
    

---

# **Chapter 5 — Ways of Working as a Senior Cloud/Infra Engineer**

_(Expanded with senior-level clarity, practical examples, templates, and minimal-but-relevant code/config snippets.)_

The modern Cloud/Infra engineer is no longer “just an operator.”  
You are a **systems engineer**, **architectural reviewer**, **incident responder**, **process enforcer**, and **cross-team facilitator**.

This chapter explains the working methods that make a senior engineer _effective, predictable, and impactful_ in a growing engineering organization.

---

# **5.1 RFCs & Design Documents**

RFCs (Request for Comments) and design documents are how senior engineers formalize thought, propose changes, and drive alignment.

---

## **5.1.1 Why RFCs Matter**

- Reduce ambiguity
    
- Create a durable record of strategic decisions
    
- Build alignment across engineering, security, and product
    
- Prevent hidden tribal knowledge
    
- Build shared language across orgs
    

A strong RFC is **clear**, **argued**, **justified**, and **testable**.

---

## **5.1.2 Standard RFC Structure**

```
# Title: "Private Service Connect for Internal APIs"
# Status: Draft / Review / Approved
# Authors: Alice Doe
# Date: YYYY-MM-DD

## 1. Context
Why the change is needed, who is affected, business drivers.

## 2. Goals
What this RFC *will* achieve.

## 3. Non-Goals
What is explicitly *out of scope*.

## 4. Background
Current state, constraints, and existing behavior.

## 5. Proposed Design
Architecture diagrams, components, traffic flow, IAM.

## 6. Alternatives Considered
Why other options were rejected.

## 7. Risks & Mitigations
Scalability, security, operational risks.

## 8. Rollout Plan
Phases, prerequisites, migration approach.

## 9. Success Metrics
How we measure adoption or effectiveness.

## 10. Appendix
Related links, references, diagrams.
```

---

## **5.1.3 Example: RFC Snippet for Enforcing Namespace-Level mTLS**

```yaml
apiVersion: security.istio.io/v1beta1
kind: PeerAuthentication
metadata:
  name: strict-mtls
  namespace: payments
spec:
  mtls:
    mode: STRICT
```

**Comments:**  
This would be included in an RFC discussing mesh security posture.

---

## **5.1.4 Common Pitfalls**

- Writing RFCs _after_ the work is already done → defeats the purpose
    
- Making RFCs overly long → no one reads them
    
- Skipping the “Alternatives” section → decisions become politicized
    
- Lack of clear owners → nobody accountable for rollout
    

---

# **5.2 Operational Maturity & Runbook Culture**

Operational maturity means **predictable, controlled, observable, repeatable** operations.  
A senior engineer accelerates operational maturity through runbooks, automation, and continuous improvement.

---

## **5.2.1 What Mature Operations Look Like**

- Every service has runbooks
    
- On-call engineers can resolve common issues within 15 minutes
    
- No tribal knowledge required for incident response
    
- Deployment and rollback are safe, verified, and reversible
    
- Infra changes are automated, not manual
    

---

## **5.2.2 Standard Runbook Template**

```
# Runbook: "API Latency Spikes"

## 1. Symptoms
- p95 latency > 200ms
- Request volume stable but error rate rising

## 2. Quick Commands / Queries
kubectl get pods -n payments
kubectl describe deploy api-service -n payments
gcloud compute instances list --filter="name ~ 'payments'"

## 3. Diagnostics
- Check pods restart count
- Validate mesh retry/circuit breaker metrics
- Inspect GCLB backend health

## 4. Known Causes
- Pod resource starvation
- Downstream dependency failure
- Network congestion

## 5. Remediation Steps
- Scale service manually
- Disable failing subset via VirtualService
- Rotate node pool if node-level issue

## 6. Escalation
- Contact on-call database engineer if DB latency exceeds 20ms
```

---

## **5.2.3 Example: Command Snippet in a Runbook**

```bash
# See if a deployment has pods stuck in CrashLoopBackOff
kubectl get pods -n checkout --field-selector=status.phase!=Running
```

---

## **5.2.4 Common Pitfalls**

- Runbooks that assume deep internal knowledge
    
- Runbooks that are never validated in real incidents
    
- Outdated runbooks after architecture changes
    
- Lack of automation → runbooks become 50 steps long
    

---

# **5.3 Effective Incident Response**

Incidents determine the difference between **competent** and **world-class** platform teams.

---

## **5.3.1 Core Principles**

- **Stabilize first, diagnose second** → protect customers first
    
- **Declare incidents early** → reduces MTTR
    
- **One incident commander** → avoids chaos
    
- **One Slack channel, one Zoom** → focus and minimize cognitive load
    
- **Timestamp everything** → necessary for postmortems
    

---

## **5.3.2 Incident Workflow**

1. **Detection**  
    Alerts fire (SLO-based, not metric-based).
    
2. **Declaration**  
    Assign severity. Notify SRE and stakeholders.
    
3. **Stabilization**  
    Rollback, scale up, failover — whatever temporarily stops the damage.
    
4. **Diagnosis**  
    Root cause analysis once system stable.
    
5. **Resolution**  
    Confirm all systems healthy.
    
6. **Postmortem (blameless)**  
    Document triggers, timeline, root cause, and action items.
    

---

## **5.3.3 Example: Useful Command in an Incident**

```bash
# Identify the slowest pods by container restart count
kubectl get pods -A --sort-by='.status.containerStatuses[0].restartCount'
```

**Use Case:**  
Instance-level failures or OOMKill patterns during outages.

---

## **5.3.4 Pitfalls During Incidents**

- Too many people talking, no clear owner
    
- Debugging while still in active outage mode
    
- Changing multiple variables simultaneously
    
- Failing to communicate with customer-support teams
    
- Postmortems that focus on “who” instead of “what/why”
    

---

# **5.4 Collaboration With App Teams & SRE**

The most effective infra engineers **enable** application teams, not block them.

---

## **5.4.1 Responsibilities of a Senior Cloud/Infra Engineer**

- Provide secure, fast, reliable platform abstractions
    
- Build reusable templates and reference architectures
    
- Ensure app teams can deploy autonomously
    
- Run platform-wide initiatives: mesh, logging, cost optimization
    
- Partner with SRE to define SLOs and operational hygiene
    

---

## **5.4.2 How to Collaborate Effectively**

### **Partner Early**

Join design discussions before app teams choose architecture patterns.

### **Represent Platform Needs**

Push for:

- stateless design where possible
    
- readiness/liveness probes
    
- idempotent APIs
    
- consistent health endpoints
    

### **Be a Multiplier**

Document everything in public repos:

- onboarding guides
    
- architecture patterns
    
- cluster resource quotas
    
- best practice examples
    

---

## **5.4.3 Example: Template Manifests to Provide to App Teams**

_(simple, opinionated Deployment manifest)_

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: api-service
  labels:
    app: api-service
spec:
  replicas: 3
  selector:
    matchLabels:
      app: api-service
  template:
    metadata:
      labels:
        app: api-service
    spec:
      containers:
      - name: api
        image: gcr.io/company/api:v1
        ports:
        - containerPort: 8080
        resources:
          requests:
            cpu: "250m"
            memory: "256Mi"
          limits:
            cpu: "1"
            memory: "512Mi"
```

**Comment:**  
A senior infra engineer provides ready-to-use golden templates.

---

## **5.4.4 Pitfalls**

- Platform teams dictating rather than partnering
    
- App teams bypassing platform (kubectl apply) → configuration drift
    
- SRE being brought in too late → SLOs misaligned with platform limits
    

---

# **5.5 Architectural Decision Records (ADRs)**

ADRs capture **why** decisions were made, not just _what_ the design is.  
This is the antidote to “Why did we do this again?” questions six months later.

---

## **5.5.1 What ADRs Are**

A lightweight version of RFCs focused on **decisions**:

- “We will use Istio mTLS across all namespaces.”
    
- “GKE Autopilot will not be used for stateful workloads.”
    
- “All services will follow the golden Deployment template.”
    

They ensure architectural consistency across a large organization.

---

## **5.5.2 ADR Template**

```
# ADR 0007: Adopt Private Service Connect for Cloud SQL
Date: 2025-05-12
Status: Accepted

## 1. Context
We currently use public IPs with authorized networks. Security team requires private, VPC-only connectivity.

## 2. Decision
Adopt Cloud SQL via Private Service Connect in all environments.

## 3. Consequences
- Improved security posture
- Requires changes to existing Terraform modules
- App workloads need updated connection strings

## 4. Alternatives
- Public IP + Cloud Armor
- VPC Peering (not supported for SQL)
```

---

## **5.5.3 When to Write an ADR**

- Changing a foundational platform assumption
    
- Introducing or deprecating a major infra component
    
- Standardizing a pattern across teams
    
- Revisiting historical decisions
    

---

## **5.5.4 Common Pitfalls**

- Writing ADRs only after disagreements arise
    
- Failing to update ADRs when decisions evolve
    
- Not linking ADRs to RFCs or Terraform modules
    
- Never archiving outdated ADRs → confusion
    

---

# **Chapter 6 — Organizations, Folders, Projects & Environment Strategy**

_(Expanded with senior-level clarity, best practices, real examples, and relevant commands.)_

This chapter explains how to structure your GCP landscape for **security**, **operational clarity**, **blast-radius control**, and **scalable team workflows**. Resource hierarchy choices directly impact IAM, networking, automation, and compliance — so this is foundational architecture work.

---

# **6.1 Resource Hierarchy Best Practices**

The GCP resource hierarchy controls _policy inheritance_, _IAM boundaries_, _organization policies_, and _network architecture_. A poor structure leads to long-term operational pain.

---

## **6.1.1 Recommended Enterprise Hierarchy Layout**

A strong, scalable baseline:

```
Organization
└── Folders
    ├── prod
    │    ├── app-team-a
    │    ├── app-team-b
    │    └── shared-services
    ├── non-prod
    │    ├── dev
    │    ├── staging
    │    └── shared-services
    └── sandbox
```

### **Key Principles**

- **Folders are your primary policy boundaries.**
    
- **Projects isolate workloads and quota.**
    
- **Shared services never live alongside app workloads.**
    

---

## **6.1.2 Why This Hierarchy Works**

- Production policies cannot be changed by non-prod teams.
    
- Changes to org policies propagate predictably.
    
- Each app team gets controlled autonomy.
    
- Network and IAM boundaries remain clean.
    
- Projects can be deleted safely without side effects.
    

---

## **6.1.3 Example: Creating a Folder**

```bash
gcloud resource-manager folders create \
    --display-name="prod" \
    --organization=123456789012
```

**Comment:**  
This folder can now host all production projects and policies.

---

## **6.1.4 Common Pitfalls**

- Putting production and non-production under the same folder.
    
- Creating projects with no folder → chaos for org policy inheritance.
    
- Using folders to represent _teams_, not _policy boundaries_.
    
- Too many folders → confusion, inconsistent rules.
    

---

# **6.2 Separating Prod, Non-Prod, and Sandbox**

Environment separation is essential for **blast-radius reduction**, **compliance**, and **minimal privilege access**.

---

## **6.2.1 Goal of Environment Separation**

- Prevent accidental production modifications
    
- Ensure IAM isolation
    
- Enable independent CI/CD flows
    
- Allow looser guardrails in non-prod
    
- Contain experiments and onboarding sandboxes
    

---

## **6.2.2 Recommended Strategy**

### **Production**

- Strictest organization policies
    
- Only platform/SRE/admin-level roles
    
- No developer kubectl access
    
- Strict VPC firewall ingress/egress
    
- Audit logging retention ≥ 1 year
    

### **Non-Production (Dev/Staging)**

- Mirrors production architecture
    
- Developers may have read-only or limited-write access
    
- Faster IAM and networking changes
    
- More permissive org policies
    

### **Sandbox**

- No uptime guarantees
    
- Minimal guardrails
    
- Used for prototyping, learning
    

---

## **6.2.3 Example: Folder Layout Enforcement**

### **Org Policy: Only allow production resources in certain regions**

```bash
gcloud org-policies set-policy policy-prod-regions.yaml
```

**policy-prod-regions.yaml:**

```yaml
constraint: constraints/gcp.resourceLocations
listPolicy:
  allowedValues:
  - in:us-central1
  - in:us-east1
  - in:us-west1
  - in:europe-west1
```

**Comment:**  
This ensures _all_ prod projects stay within approved regions.

---

## **6.2.4 Common Pitfalls**

- Giving developers direct write access to production → major risk.
    
- Mixing prod and non-prod databases or networks → compliance violations.
    
- Not replicating prod architecture in staging → useless pre-production testing.
    
- Using “sandbox” environments as quasi-prod → unclear ownership.
    

---

# **6.3 Shared Services Projects**

Shared services house cross-cutting infrastructure needed by _multiple projects or environments_.

---

## **6.3.1 Why Use Shared Services Projects**

- Centralize critical infra:
    
    - VPC networks
        
    - Cloud Routers / Interconnect
        
    - DNS
        
    - Logging sinks
        
    - Artifact Registry
        
    - CI/CD runners
        
- Restrict control to platform teams only
    

This reduces duplication and ensures uniform configurations.

---

## **6.3.2 Typical Shared Services Setup**

**Examples of shared-service projects:**

- `shared-network-prod`
    
- `shared-network-nonprod`
    
- `shared-observability`
    
- `shared-artifacts`
    
- `shared-ci`
    

Each contains infrastructure consumed by multiple application projects.

---

## **6.3.3 Example: Creating a Shared VPC Host Project**

```bash
gcloud compute shared-vpc enable shared-network-prod
```

### **Adding a service project:**

```bash
gcloud compute shared-vpc associated-projects add \
  --host-project=shared-network-prod \
  app-team-a-prod
```

**Comment:**  
Application teams deploy workloads but cannot alter core network infrastructure.

---

## **6.3.4 Example: Central Log Sink in Shared Observability Project**

```bash
gcloud logging sinks create org-logs \
  storage.googleapis.com/org-log-bucket \
  --include-children \
  --organization=123456789012
```

**Comment:**  
Captures logs from all child folders and projects.

---

## **6.3.5 Common Pitfalls**

- Giving app project owners edit rights to the shared VPC → breaks isolation.
    
- Running business workloads inside shared-services projects.
    
- Not using separate shared-services projects for prod vs non-prod.
    
- Overloading shared projects with unrelated responsibilities.
    

---

# **6.4 Folder-Based Policy Enforcement**

Folders allow consistent enforcement of **organization policies**, **IAM rules**, and **security controls** across a defined environment.

---

## **6.4.1 What Policies Should Live at Folder Level?**

### **Production Folder Policies**

- Allowed resource regions
    
- Disallow public IPs
    
- Enforce CMEK (customer-managed encryption keys)
    
- Restrict service account key creation
    
- Restrict external service accounts usage
    

### **Non-Production Folder Policies**

- More flexibility, but still:
    
    - Restrict external IP assignment
        
    - Enforce minimal network restrictions
        
    - Allow broader service experimentation
        

---

## **6.4.2 Example: Restricting Public IPs in Production**

**policy-restrict-public-ips.yaml**

```yaml
constraint: constraints/compute.vmExternalIpAccess
listPolicy:
  deniedValues:
    - "*"
```

Apply to folder:

```bash
gcloud org-policies set-policy policy-restrict-public-ips.yaml \
  --folder=345678901234
```

---

## **6.4.3 Folder-Level IAM Example**

Give SRE team monitoring rights on all prod projects:

```bash
gcloud resource-manager folders add-iam-policy-binding 345678901234 \
  --member="group:sre-team@company.com" \
  --role="roles/monitoring.viewer"
```

### **Comment:**

SRE doesn’t need editor/admin access; restricted monitoring-only is safest.

---

## **6.4.4 Common Pitfalls**

- Applying aggressive restrictions at org level → breaks non-prod flexibility.
    
- Applying policies on projects instead of folders → duplication & drift.
    
- Not documenting which folder owns which policy → confusion.
    
- Failing to test org policy updates in non-prod first.
    

---

# **6.5 Multi-Project Patterns for Microservices**

Using multiple GCP projects provides **clear ownership**, **quota isolation**, and **blast-radius reduction** for microservices.

---

## **6.5.1 Why Multiple Projects?**

### **Benefit 1 — Security Isolation**

A compromised service shouldn’t compromise the whole platform.

### **Benefit 2 — IAM Clarity**

Each microservice gets:

- Separate IAM bindings
    
- Separate service accounts
    
- Separate GKE workload identity
    

### **Benefit 3 — Quota Protection**

One service cannot starve others of:

- CPUs
    
- IP addresses
    
- Load balancer quotas
    
- API rate limits
    

### **Benefit 4 — Billing Segmentation**

Cost attribution becomes trivial.

---

## **6.5.2 Common Project Patterns**

### **Pattern A — Per-Service Projects**

```
app-team-a-prod/
  ├── payments-prod
  ├── checkout-prod
  ├── catalog-prod
```

Good for:

- Large organizations
    
- High-security domains
    
- Compliance-heavy workloads
    

### **Pattern B — Per-Domain Projects**

```
app-team-a-prod/
  ├── commerce-prod
  ├── user-platform-prod
```

Good for:

- Medium orgs
    
- Domain-oriented team structures
    

### **Pattern C — Per-Team Projects**

```
app-team-a-prod/
  └── app-team-a-prod
```

Good for:

- Small orgs
    
- Low team count
    
- Minimal complexity
    

---

## **6.5.3 Example: Creating a Service Project for a Microservice**

```bash
gcloud projects create checkout-prod \
  --folder=prod-folder-id
```

Add IAM binding for CI/CD:

```bash
gcloud projects add-iam-policy-binding checkout-prod \
  --member="serviceAccount:ci@company.com" \
  --role="roles/container.developer"
```

---

## **6.5.4 Using Shared VPC Across Projects**

Attach the project to shared VPC:

```bash
gcloud compute shared-vpc associated-projects add \
  --host-project=shared-network-prod \
  checkout-prod
```

This allows the microservice to use common:

- VPC
    
- Subnets
    
- Cloud Router
    
- DNS
    
- NAT
    

---

## **6.5.5 Common Pitfalls**

- Using one project for dozens of microservices → IAM becomes chaos.
    
- Giving teams full owner access to their project → unsafe and unnecessary.
    
- Creating too many small projects → overhead without benefits.
    
- Forgetting cross-project IAM when setting up GitOps.
    
- Not standardizing naming conventions → unreadable logs and billing exports.
    

---

# **Chapter 7 — GKE Cluster Architecture: Regional, Multi-Cluster, Multi-Region**

_(Expanded with senior-level clarity, practical examples, commands, and architectural guidance.)_

This chapter explains how to design Kubernetes cluster architectures on GCP that meet enterprise requirements for **availability**, **scalability**, **security**, and **operational clarity**.

---

# **7.1 Why Regional Clusters?**

A **regional GKE cluster** runs its control plane and node pools across multiple zones within a region. This architecture gives you **built-in zone failure resilience** without requiring extra operational overhead.

---

## **7.1.1 Benefits of Regional Clusters**

### **1. High Availability**

- The control plane is replicated across **3 zones**.
    
- Node pools also span multiple zones.
    
- A single-zone outage does _not_ bring down the cluster.
    

### **2. Simpler Operational Model**

No need for:

- Custom scripts for node pool failover
    
- Manual rescheduling across zones
    
- Multi-zonal deployments
    

### **3. Better SLO Guarantees**

Higher uptime SLAs compared to zonal clusters.

### **4. Future-Proofing**

Cluster-level failure domain is now “region,” which is ideal for:

- SLA commitments
    
- Customer-facing workloads
    
- Stateful workloads with zonal redundancy
    

---

## **7.1.2 Example: Creating a Regional GKE Cluster**

```bash
gcloud container clusters create primary \
  --region=us-central1 \
  --node-locations=us-central1-a,us-central1-b,us-central1-f \
  --enable-ip-alias \
  --release-channel=regular \
  --enable-autoscaling \
  --min-nodes=3 \
  --max-nodes=20 \
  --enable-autorepair \
  --enable-shielded-nodes
```

### **Comments**

- `--region` makes the cluster regional.
    
- `--node-locations` controls which zones get node pools.
    
- `--enable-ip-alias` is required for VPC-native pods.
    
- Autoscaling applies across zones automatically.
    

---

## **7.1.3 Common Pitfalls**

- Using zonal clusters for production → outages during zone failures.
    
- Forgetting to spread node pools across multiple zones.
    
- Underestimating control-plane reliability requirements.
    
- Not budgeting for slightly higher cost of regional clusters (redundant control-plane VMs).
    

---

# **7.2 Workload Separation Strategies**

Workload separation is how you distribute **different types of workloads** across **clusters** and **node pools** to meet isolation, cost, and performance requirements.

---

## **7.2.1 Why Separate Workloads?**

- Reduce security blast radius
    
- Avoid noisy-neighbor issues
    
- Scale infrastructure based on workload type
    
- Minimize conflicting pod scheduling requirements
    
- Allow independent cluster upgrades
    

---

## **7.2.2 Three Layers of Separation**

### **1. Cluster-Level Separation (Strongest)**

Use clusters to isolate:

- Production vs Non-Production
    
- Regulated vs unregulated workloads
    
- Customer-isolated workloads
    
- Teams with different operational constraints
    

### **2. Namespace-Level Separation (Medium)**

Good for:

- Team boundaries
    
- Service separation
    
- Resource quotas
    

### **3. Node-Pool-Level Separation (Soft)**

Useful for workloads with different:

- CPU/memory needs
    
- OS images
    
- Resource profiles (batch vs real-time)
    
- Spot/preemptible usage
    

---

## **7.2.3 Example: Two Node Pools for Different Workload Types**

```bash
# Node pool for latency-sensitive workloads
gcloud container node-pools create realtime \
  --cluster=primary \
  --region=us-central1 \
  --machine-type=e2-highcpu-4 \
  --num-nodes=3 \
  --node-labels="workload=realtime"

# Node pool for batch workloads (preemptible)
gcloud container node-pools create batch \
  --cluster=primary \
  --region=us-central1 \
  --machine-type=e2-standard-2 \
  --num-nodes=0 \
  --enable-autoscaling \
  --min-nodes=0 \
  --max-nodes=10 \
  --preemptible \
  --node-labels="workload=batch"
```

### **Pitfall**

Running latency-sensitive and batch jobs on the same nodes results in **contention, throttling, and unpredictable latency**.

---

# **7.3 Multi-Cluster Patterns**

Multi-cluster architectures appear when a single cluster can no longer meet global, organizational, or workload-isolation requirements.

These patterns support the following goals:

- Cross-region redundancy
    
- Compliance isolation
    
- Environment/version isolation
    
- Tenant or team separation
    

---

## **7.3.1 Pattern 1 — Cluster-Per-Team**

### **When to Use**

- Large engineering orgs with >10 teams
    
- Teams independently manage deployments
    
- Strong ownership boundaries required
    
- Teams have different traffic patterns
    

### **Characteristics**

```
team-a/
  └── cluster-a-prod
team-b/
  └── cluster-b-prod
```

### **Advantages**

- Natural IAM isolation
    
- Independent cluster upgrades
    
- Team-specific node pools and autoscaling
    

### **Disadvantages**

- Cluster sprawl
    
- Higher operational overhead
    
- Platform team must standardize via GitOps to avoid drift
    

---

## **7.3.2 Pattern 2 — Cluster-Per-Type**

Separate clusters by _workload type_, not by team.

Examples:

- Real-time API cluster
    
- Background processing cluster
    
- Machine learning cluster
    
- Internal jobs cluster
    
- Customer-isolated cluster
    

### **Advantages**

- Optimal resource selection for each workload type
    
- Simplifies troubleshooting
    
- Avoids noisy-neighbor scenarios
    

### **Example Labeling for Workload Types**

```yaml
nodeSelector:
  workload-type: api
```

### **Disadvantages**

- Teams must deploy to more than one cluster
    
- Might require cluster-aware routing
    

---

## **7.3.3 Pattern 3 — Hub-and-Spoke Clusters**

This pattern centralizes shared infra and spreads workloads across multiple customer/tenant clusters.

```
       Shared Infra Cluster (Hub)
                │
     ┌──────────┼──────────┐
     │          │          │
Tenant A   Tenant B   Tenant C
 Cluster    Cluster    Cluster
```

### **Hub Responsibilities**

- Logging, monitoring
    
- Shared ingress gateways
    
- Identity and authentication systems
    
- Shared CI/CD services
    
- Shared DNS and config management
    

### **Spoke Responsibilities**

- Single tenant’s workloads
    
- Tenant-specific configuration
    
- Tenant-level SLAs
    

### **Advantages**

- Strong tenant isolation
    
- Logical place for central services
    
- Simplifies multi-tenancy governance
    

### **Disadvantages**

- Hub cluster becomes a critical dependency
    
- Can require mesh federation or cluster linking
    

---

# **7.4 Multi-Region Platforms**

Multi-region architecture extends GKE beyond a single region for:

- **Global reliability**
    
- **Latency optimization**
    
- **Regulatory boundaries**
    
- **Disaster recovery**
    

---

## **7.4.1 Active-Active vs Active-Passive**

These are the two primary patterns for multi-region deployments.

---

### **Active-Active**

Both regions serve traffic simultaneously.

```
US Region <──► Global LB <──► EU Region
```

### **Characteristics**

- Lowest latency for global users
    
- High availability
    
- Requires:
    
    - Global load balancer
        
    - Regional clusters
        
    - Data-tier replication (often hardest part)
        
    - Mesh configuration across regions
        

### **Advantages**

- Continuous availability even during region outages
    
- Horizontal scale across regions
    

### **Disadvantages**

- Data consistency complexity
    
- Higher cost
    
- Requires traffic-splitting strategies
    

---

### **Active-Passive**

Primary region serves traffic; secondary region is hot/warm/cold standby.

```
Primary Region ──► Global LB  
Backup Region  (failover only)
```

### **Advantages**

- Easier database architecture
    
- Simpler operations
    
- Lower cost
    

### **Disadvantages**

- Failover time required
    
- Cold-start issues
    
- Risk of backups being insufficient if not tested
    

---

## **7.4.2 Example: Global Traffic Distribution with Cloud Load Balancing**

Cloud Load Balancing (GCLB) routes traffic to the closest healthy cluster.

### **Global Backend Service Configuration (conceptual)**

```bash
gcloud compute backend-services create api-backend \
  --global \
  --protocol=HTTP \
  --health-checks=api-healthcheck
```

### **Attach NEGs (from different regions)**

```bash
gcloud compute backend-services add-backend api-backend \
  --global \
  --network-endpoint-group=cluster1-neg \
  --network-endpoint-group-region=us-central1

gcloud compute backend-services add-backend api-backend \
  --global \
  --network-endpoint-group=cluster2-neg \
  --network-endpoint-group-region=europe-west1
```

**Comments:**

- Each cluster exposes an **In-Namespace NEG** or **Gateway NEG**
    
- LB uses health checks to shift traffic during outages
    

---

## **7.4.3 Pitfalls in Multi-Region Designs**

- Forgetting that network egress between regions increases cost.
    
- Trying active-active before your org is ready.
    
- Using stateful workloads without multi-region strategy → data divergence.
    
- Not implementing per-region rate limiting.
    
- Using zonal databases in multi-region architecture → guaranteed outages.
    

---

# **Chapter 8 — Multi-Tenancy, Data Residency, and Security Boundaries**

_(Expanded with practical architecture patterns, commands, YAML, and clear explanations.)_

This chapter explains how to design **safe, compliant, highly isolated multi-tenancy** using GKE and GCP. Proper boundary design is foundational for security, compliance, and operational stability.

---

# **8.1 Tenant Isolation Models**

Tenants must be isolated along one or more of four axes:

1. **Namespaces**
    
2. **Clusters**
    
3. **Projects**
    
4. **VPCs**
    

Each level provides a different strength of isolation. Choosing the right model depends on your threat model, compliance needs, and operational overhead tolerance.

---

## **8.1.1 Namespace-Based Isolation**

Namespaces are the **lightest-weight** form of multi-tenancy.

### **Best For**

- Internal team separation
    
- Soft logical isolation
    
- SaaS tenants with low compliance requirements
    
- Shared compute where tenants trust the platform
    

### **Mechanisms**

- Resource quotas
    
- NetworkPolicies
    
- RBAC
    
- Istio authorization policies
    
- LimitRanges
    

### **Namespace Isolation Example**

```yaml
apiVersion: v1
kind: Namespace
metadata:
  name: tenant-a
  labels:
    tenant: a
```

### **Add Resource Quotas**

```yaml
apiVersion: v1
kind: ResourceQuota
metadata:
  name: tenant-a-quota
  namespace: tenant-a
spec:
  hard:
    limits.cpu: "10"
    limits.memory: "40Gi"
    pods: "100"
```

### **Add Network Policy (deny all by default)**

```yaml
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: default-deny
  namespace: tenant-a
spec:
  podSelector: {}
  policyTypes:
  - Ingress
  - Egress
```

### **Pros**

- Fastest provisioning
    
- Lowest cost
    
- Works well with GitOps
    

### **Cons**

- Weakest isolation
    
- Shared kernel, shared control-plane, shared node pool
    
- No true quota isolation for node-level resources (CPU throttling still shared)
    

### **Common Pitfall**

People assume namespaces provide strong security boundaries — **they do not**.

---

## **8.1.2 Cluster-Based Isolation**

Using dedicated clusters for each tenant or tenant group.

### **Best For**

- Strong security or noisy-neighbor isolation
    
- Compliance-bound tenants (HIPAA, PCI)
    
- Customers requiring infrastructure-level separation
    
- Large enterprise accounts
    

### **Characteristics**

- Each tenant has its own:
    
    - API server
        
    - Node pools
        
    - Ingress gateway
        
    - Resource quotas enforced globally
        

### **Cluster Creation Example**

```bash
gcloud container clusters create tenant-a-cluster \
  --region=us-central1 \
  --enable-ip-alias \
  --node-locations=us-central1-a,us-central1-b
```

### **Pros**

- Strong isolation (control-plane, compute, network)
    
- Blast radius limited to one tenant
    
- Easy to apply tenant-specific upgrades
    

### **Cons**

- High operational overhead without automation
    
- Higher cost
    
- Requires multi-cluster routing and GitOps patterns
    

### **Common Pitfall**

Clusters proliferate without automated governance → **cluster sprawl**.

---

## **8.1.3 Project-Based Isolation**

Each tenant gets **their own GCP project**. Projects are strong security and quota boundaries.

### **Best For**

- Enterprise tenants with strict audit/compliance
    
- Per-tenant billing
    
- Need to apply org policies per tenant
    
- Regulated industries
    

### **Project Creation Example**

```bash
gcloud projects create tenant-a-prod \
  --folder=tenants-folder-id
```

### **Attach to Shared VPC**

```bash
gcloud compute shared-vpc associated-projects add \
  --host-project=shared-vpc-prod \
  tenant-a-prod
```

### **Pros**

- Strong IAM isolation
    
- Full quota isolation
    
- Clear billing separation
    
- Apply per-tenant policies (CMEK, region restrictions)
    

### **Cons**

- Requires strong automation (Terraform/Terragrunt)
    
- More complex networking across projects
    

### **Common Pitfall**

Giving tenants direct project access instead of controlled identities (impersonation is safer).

---

## **8.1.4 VPC-Based Isolation**

Strongest form of isolation: separate virtual networks.

### **Best For**

- Highly regulated multi-tenant SaaS
    
- Multi-customer financial/healthcare workloads
    
- Environments where “no customer traffic ever meets another customer”
    

A VPC boundary stops:

- Lateral service discovery
    
- IP-level access
    
- Misconfigurations in firewall rules from leaking across tenants
    

### **Pros**

- Hard network boundary
    
- Strong isolation guarantee
    
- Enables different network topologies per tenant
    

### **Cons**

- High operational cost
    
- Requires Private Service Connect or VPC peering
    
- More NAT/egress rules and routing complexity
    

---

## **Choosing the Right Model**

|Isolation Type|Strength|Cost|Best For|
|---|---|---|---|
|**Namespace**|★☆☆☆|Low|Small tenants, internal apps|
|**Cluster**|★★★☆|Medium|Larger SaaS customers|
|**Project**|★★★★|Medium|Enterprise tenants w/ compliance|
|**VPC**|★★★★★|High|Regulated industries, highest security|

---

# **8.2 Data Residency**

Data residency ensures data stored or processed for a tenant remains within approved regions.

---

## **8.2.1 Why Data Residency Matters**

- Regulatory requirements (GDPR, CCPA, FedRAMP)
    
- Contractual requirements from enterprise customers
    
- Reduce legal exposure
    

---

## **8.2.2 Residency Implementation Strategies**

### **1. Region-Specific Clusters**

Deploy a cluster per region that houses customers from that region.

```
eu-west1 cluster → EU customers only  
us-central1 cluster → US customers only  
ap-southeast1 cluster → APAC customers only
```

### **2. Region-Specific Datastores**

Cloud SQL, BigQuery, Spanner must be region-scoped properly.

Example: Creating a Cloud SQL instance in EU only:

```bash
gcloud sql instances create tenant-a-db \
  --region=europe-west1 \
  --database-version=POSTGRES_14
```

### **3. Region-Level IAM Restrictions**

Use org policies to ensure workloads remain in allowed regions.

```yaml
constraint: constraints/gcp.resourceLocations
listPolicy:
  allowedValues:
  - in:europe-west1
```

### **4. Region-Specific Encryption Keys**

Use KMS keys that are scoped to a region.

```bash
gcloud kms keyrings create eu-ring --location=europe-west1
gcloud kms keys create eu-key \
  --keyring=eu-ring \
  --location=europe-west1 \
  --purpose=encryption
```

---

## **8.2.3 Common Pitfalls**

- Running multi-region services that replicate outside regulated regions
    
- Backups stored in the wrong region
    
- Using global services (e.g., global LB) without residency consideration
    
- Not validating data pathways (logs, telemetry may leak to other regions)
    

---

# **8.3 Service Perimeters**

Service Perimeters (VPC Service Controls) restrict how GCP-managed services are accessed.  
They prevent _data exfiltration_ from GCP services such as Cloud Storage, BigQuery, Pub/Sub, Cloud SQL (via PSC), and others.

---

## **8.3.1 Key Concepts**

- **Perimeter** — boundary around projects/services
    
- **Restricted services** — only accessible from within perimeter
    
- **Access levels** — conditions on requests (device, IP, identity)
    
- **Bridged perimeters** — communication allowed between two sets of projects
    
- **Dry run** — test mode
    

---

## **8.3.2 Example: Creating a Service Perimeter**

```bash
gcloud access-context-manager perimeters create tenant-a-perimeter \
  --title="Tenant A Perimeter" \
  --perimeter-type=regular \
  --resources="projects/123456789012" \
  --restricted-services="bigquery.googleapis.com,storage.googleapis.com"
```

**Comment:**  
Tenant project can only access BigQuery/Storage from inside the perimeter — preventing external data leaks.

---

## **8.3.3 Example: Adding an Access Level**

```bash
gcloud access-context-manager levels create trusted-corp \
  --title="TrustedCorpNetwork" \
  --basic-level-spec="
     ipSubnetworks: ['203.0.113.0/24']
  "
```

---

## **8.3.4 Common Pitfalls**

- Misconfigured perimeters blocking internal workloads
    
- Not including CI/CD runner project in perimeter → deployment failures
    
- Forgetting that some GCP APIs are global
    
- Not testing in dry run mode
    

---

# **8.4 Cross-Tenancy Communication Controls**

Cross-tenant communications must be **explicitly allowed** and strictly enforced. By default, tenants should not see one another.

---

## **8.4.1 Goals**

- Prevent lateral movement
    
- Enforce tenant data boundaries
    
- Centralize communication patterns
    
- Reduce blast radius of misconfigurations
    

---

## **8.4.2 Common Patterns for Cross-Tenant Access**

### **Pattern A: API Gateway Mediation**

All tenant-to-tenant calls route via:

- Ingress Gateway
    
- API Gateway
    
- GCLB + routing rules
    

**Pros:**  
Strong auditing and routing control.

---

### **Pattern B: Service Mesh Authorization Policies**

Use Istio for service-level policies.

#### **Example: Allow tenant A to call only billing service**

```yaml
apiVersion: security.istio.io/v1beta1
kind: AuthorizationPolicy
metadata:
  name: tenant-a-allowed-outbound
  namespace: tenant-a
spec:
  action: ALLOW
  rules:
  - to:
    - operation:
        hosts: ["billing.svc.cluster.local"]
```

Everything else implicitly denied if a deny-all policy is in place.

---

### **Pattern C: Private Service Connect (PSC) Endpoints**

Tenants access shared services over private IPs.

Example: Creating PSC endpoint:

```bash
gcloud compute forwarding-rules create tenant-a-psc \
  --region=us-central1 \
  --address=tenant-a-psc-ip \
  --target-service=projects/shared-services/regions/us-central1/services/billing
```

---

### **Pattern D: VPC Firewall Segmentation**

VPC-level firewall rules restrict cross-project or cross-tenant communication.

Example: Deny all east–west except mesh gateway:

```bash
gcloud compute firewall-rules create deny-eastwest \
  --network=prod-vpc \
  --direction=INGRESS \
  --priority=100 \
  --action=DENY \
  --source-ranges=10.0.0.0/8 \
  --target-tags="tenant-*"
```

---

## **8.4.3 Common Pitfalls**

- Forgetting to audit cross-tenant traffic flows
    
- Overly permissive mesh AuthorizationPolicies → tenants can call each other
    
- Using shared DNS zones accidentally exposes API endpoints
    
- PSC misconfiguration leading to trans-tenant visibility
    
- Not applying deny-all first, then whitelisting
    

---

# **Chapter 9 — Domain-Driven Design, Service Topologies & API Partitioning**

_(Expanded with senior-level clarity, diagrams-in-text, request-flow examples, and configuration snippets where relevant.)_

This chapter explains how to decompose domains into services, define clear boundaries, avoid hidden coupling, and design effective north–south and east–west communication patterns. These decisions directly affect reliability, performance, and scalability.

---

# **9.1 Domain Decomposition**

Domain decomposition is the process of structuring a platform into logical, coherent, business-aligned domains. It is the foundation of microservices, API partitioning, and platform evolution.

---

## **9.1.1 What Is a Domain?**

A **domain** is a cohesive set of business responsibilities.

Examples:

- **Commerce domain**
    
    - Cart, Checkout, Catalog, Pricing
        
- **User Platform domain**
    
    - Authentication, Authorization, Profiles
        
- **Billing domain**
    
    - Invoices, Payments, Subscription Plans
        

Domains are **not defined by teams**, but by business behavior.

---

## **9.1.2 How to Identify Domains**

Ask these questions:

1. **Does this area have its own business vocabulary?**  
    (e.g., cart, coupon, fulfillment)
    
2. **Does it encapsulate a business workflow end-to-end?**
    
3. **Would changes here be meaningful to business stakeholders?**
    
4. **Does it have its own data and invariants?**
    

If the answer is yes → you likely discovered a domain.

---

## **9.1.3 Subdomains and Bounded Contexts**

Each domain can be decomposed into **subdomains** or **bounded contexts**—areas where a specific model applies.

### Example (Commerce Domain)

```
Commerce
├── Catalog Context
├── Pricing Context
├── Cart Context
└── Checkout Context
```

These boundaries become candidates for microservices.

---

## **9.1.4 Practical Example: Decomposing a Monolith**

Suppose you start with this:

```
monolith-service
  /cart
  /checkout
  /pricing
  /catalog
  /user
  /auth
```

Domain decomposition yields these microservices:

```
cart-service
checkout-service
pricing-service
catalog-service
user-service
auth-service
```

### Common Pitfall

Teams jump straight to microservices **without first understanding domains**, resulting in spaghetti service interactions.

---

# **9.2 Service Boundaries & Interactions**

Once domains are identified, we define **service boundaries**: the lines that separate services and govern their interactions.

---

## **9.2.1 What Makes a Good Service Boundary?**

A good service boundary should:

- Own a clear, cohesive domain responsibility
    
- Own the data it modifies (no shared DBs)
    
- Expose a stable API
    
- Have internal-only implementation details
    
- Not require deep knowledge of other services
    

---

## **9.2.2 Example: Catalog vs Pricing Boundary**

### **Catalog Service**

- Owns product metadata
    
- Provides read-heavy endpoints
    
- APIs: `/products`, `/categories`
    

### **Pricing Service**

- Owns price logic: discounts, taxes, currency
    
- APIs: `/prices`, `/discounts/apply`
    

These should never share a database table.

### Anti-pattern:

```
catalog-service directly queries pricing DB
```

This couples services through data.

---

## **9.2.3 Interaction Patterns**

### **Synchronous APIs**

Used when you need:

- Immediate response
    
- Predictable request flow
    
- Query-style interactions
    

```yaml
# Example Istio VirtualService routing to pricing service for synchronous calls
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: pricing
spec:
  hosts:
  - pricing
  http:
  - route:
    - destination:
        host: pricing
```

---

### **Asynchronous Messaging**

Used when:

- Fire-and-forget
    
- Loose coupling required
    
- High-throughput events
    
- Workflow pipelines
    

**Example: Pub/Sub topic creation for domain events**

```bash
gcloud pubsub topics create checkout-events
```

E.g., checkout-service publishes `OrderCompleted` → other services subscribe.

---

## **9.2.4 Interaction Rules for Healthy Boundaries**

1. **Services communicate through well-defined APIs only.**
    
2. **Never query another service’s database.**
    
3. **Use asynchronous patterns when consistency isn't synchronous.**
    
4. **Avoid circular dependencies.**
    
5. **Limit synchronous call depth (N→E→P→U→A… → disaster).**
    

---

## **9.2.5 Common Pitfalls**

- Hidden coupling through shared data stores
    
- Over-splitting domains (nano-services)
    
- Synchronous call chains causing cascading latency failures
    
- Creating services based on org chart rather than domain
    

---

# **9.3 North–South vs East–West Service Design**

Understanding north–south vs east–west traffic is critical to designing resilient APIs and cluster architectures.

---

## **9.3.1 North–South Traffic**

Traffic entering or leaving the cluster:

```
User → Load Balancer → Ingress Gateway → Service
```

### **North–South Design Requirements**

- Global Load Balancing
    
- TLS termination and certificate rotation
    
- Rate limiting and WAF (Cloud Armor)
    
- AuthN/AuthZ layer (JWT, OAuth2, mTLS)
    
- Tenant-aware throttles
    
- Canary/blue-green for public endpoints
    

### **North–South Routing Example**

(Using Istio Gateway)

```yaml
apiVersion: networking.istio.io/v1beta1
kind: Gateway
metadata:
  name: api-gateway
spec:
  servers:
  - port:
      number: 443
      name: https
      protocol: HTTPS
    tls:
      mode: SIMPLE
      credentialName: api-cert
    hosts:
    - "api.example.com"
```

---

## **9.3.2 East–West Traffic**

Traffic between services inside the cluster or mesh.

```
service-a → mesh → service-b
```

### **East–West Design Requirements**

- mTLS enforcement
    
- Fine-grained authorization policies
    
- Retries, timeouts, circuit breaking
    
- Mesh telemetry for traces and metrics
    
- Zero-trust defaults
    
- Failover handling (multi-region optional)
    

### **Example: Service-to-service call policy**

```yaml
apiVersion: security.istio.io/v1beta1
kind: AuthorizationPolicy
metadata:
  name: allow-a-to-b
  namespace: service-b
spec:
  rules:
  - from:
    - source:
        principals: ["cluster.local/ns/service-a/sa/default"]
```

---

## **9.3.3 Why This Distinction Matters**

North–south:

- Public attack surface
    
- Needs rate limits, WAF, authentication
    
- Runs at higher traffic volatility
    

East–west:

- Internal trust boundary
    
- Needs service identity, retries, mesh policies
    
- Handles high call volume with lower latency requirements
    

---

## **9.3.4 Common Pitfalls**

### For North–South:

- Not using a real gateway → direct service exposure
    
- No tenant-level rate limiting → one tenant can overload system
    
- Violating data residency with global routing
    

### For East–West:

- Blindly retrying → request amplification during outages
    
- Missing mTLS → lateral movement risks
    
- Mesh misconfigurations causing “503s everywhere”
    

---

# **9.4 Anti-Patterns (Mega-Services, Chatty APIs)**

Anti-patterns are the architectural smells that undermine reliability, performance, and team velocity.

---

## **9.4.1 Mega-Services**

A “mega-service” is a service pretending to be a microservice while containing:

- Too many domains
    
- Too much business logic
    
- Cross-cutting concerns
    
- Multiple data models
    

### **Signs of a Mega-Service**

- The service has >15 endpoints
    
- Deployments affect multiple teams
    
- Changes break many downstream services
    
- Onboarding new developers takes weeks
    

### **Why Mega-Services Are Bad**

- Slows deployments
    
- Increases blast radius
    
- Difficult to scale independently
    
- Hard to reason about
    

---

## **9.4.2 Chatty APIs**

Chatty APIs require services to exchange **too many** real-time, synchronous calls.

### **Example of a Chatty Workflow**

```
checkout → pricing → inventory → promotions → fees → taxes → fraud
```

One frontend request triggers **7–12** downstream requests.

### **Problems**

- Latency cascades
    
- Dependency graph becomes fragile
    
- Incidents in one service cause cross-cluster brownouts
    
- Harder to scale reliably
    

---

## **9.4.3 Solution: Aggregator or Domain-Orchestration Patterns**

Introduce a domain aggregator that internally orchestrates calls:

```
checkout-service
   ├── call pricing
   ├── call inventory
   ├── call promotions
   └── call taxes
```

Expose one API endpoint to the client.

### Example: Aggregator Pattern (Pseudo YAML)

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: checkout-aggregator
spec:
  template:
    spec:
      containers:
      - name: checkout
        image: gcr.io/company/checkout:v1
        env:
        - name: PRICING_ENDPOINT
          value: http://pricing.svc.cluster.local
        - name: INVENTORY_ENDPOINT
          value: http://inventory.svc.cluster.local
```

---

## **9.4.4 Solution: Event-Driven Architecture**

Publish events rather than calling services directly.

Example:

```
OrderCompleted event published to Pub/Sub
→ Inventory service updates stock
→ Billing service triggers invoice
→ Notification service emails user
```

This decouples services and removes synchronous dependency chains.

---

## **9.4.5 Common Pitfalls**

- Overusing synchronous APIs when async fits better
    
- Splitting services too finely (nano-services)
    
- Creating domain boundaries that don’t match business domains
    
- Shared databases masquerading as “service boundaries”
    
- API gateways or mesh used as architectural band-aids
    

---

# **Chapter 10 — Migration Strategy: Strangler Fig, Transitional Patterns**

_(Expanded with clear guidance, patterns, commands, and senior-level best practices.)_

Modernizing a legacy monolith into a cloud-native, microservices-based platform requires deliberate planning and carefully executed transitional patterns. The **Strangler Fig pattern** and its variations allow teams to incrementally replace legacy functionality with modern services—without stopping development or disrupting customers.

This chapter explains how to map the existing system, extract services gradually, operate hybrid deployments, roll out changes safely, and eventually decommission the monolith.

---

# **10.1 Mapping the Legacy Monolith**

Before extracting anything, teams must build a shared understanding of the monolith’s:

- **Domain boundaries**
    
- **Data ownership**
    
- **Inbound and outbound API flows**
    
- **Non-functional requirements**
    
- **Technical debt and hotspots**
    
- **Coupling points**
    
- **Shared libraries and database schemas**
    

---

## **10.1.1 Step 1: Build a Knowledge Map**

Create an architecture map showing:

- Modules
    
- Logical domains
    
- Inter-module calls
    
- External dependencies
    
- Database tables and relationships
    

### **Example: Monolith Mapping Diagram (Text Form)**

```
Monolith
 ├── User Module
 ├── Billing Module
 ├── Catalog Module
 ├── Pricing Module
 └── Checkout Module
       ├── Calls Billing
       ├── Calls Pricing
       └── Reads Inventory Table
```

---

## **10.1.2 Step 2: Identify Extractable Boundaries**

Good extraction candidates share these properties:

- Stable API
    
- Clear domain ownership
    
- High change rate or high pain area
    
- Minimal deep coupling to legacy internals
    
- Well-defined data access paths
    

### **Practical Extractability Test**

Ask:

> “Could this function be implemented standalone if it had its own database?”

If yes → viable candidate.

---

## **10.1.3 Step 3: Document Technical & Organizational Dependencies**

Dependencies include:

- Shared libraries
    
- Cross-cutting logic
    
- Data shared across modules
    
- Implicit assumptions inside the monolith
    
- Batch jobs that mutate data
    

This informs the extraction plan.

---

## **10.1.4 Common Pitfalls**

- Not understanding data ownership → leads to broken invariants
    
- Extracting services based on team pressure instead of domain modeling
    
- Underestimating hidden coupling via shared DB tables
    
- Failing to map external dependencies (SSO, payments, email)
    

---

# **10.2 Extracting Services Gradually**

The core of the Strangler Fig pattern:  
**Extract one slice of functionality at a time and route traffic to the new service.**

---

## **10.2.1 Step 1: Create the New Service Skeleton**

Example: Create a new Kubernetes Deployment + Service.

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: pricing-service
spec:
  replicas: 3
  selector:
    matchLabels:
      app: pricing-service
  template:
    metadata:
      labels:
        app: pricing-service
    spec:
      containers:
      - name: pricing
        image: gcr.io/company/pricing:initial
        ports:
        - containerPort: 8080
```

Expose via ClusterIP:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: pricing-service
spec:
  selector:
    app: pricing-service
  ports:
  - port: 80
    targetPort: 8080
```

---

## **10.2.2 Step 2: Introduce an Adapter in the Monolith**

The monolith continues to call the new service through an **adapter** that gradually shifts logic.

### **Example Adapter Flow**

```
Monolith → PricingAdapter → pricing-service → (new logic)
```

The monolith no longer owns pricing logic; it only delegates.

---

## **10.2.3 Step 3: Move Logic Behind the Service Boundary**

Typical migration flow:

1. Duplicate functionality in the new service
    
2. Add feature flags
    
3. Monolith calls the new service
    
4. Route all reads/writes to the new system
    
5. Remove old code from monolith
    

This ensures small blast radius.

---

## **10.2.4 Step 4: Migrate Data**

If the domain requires dedicated data storage:

- Create new schema
    
- Create DB instance with proper residency (regional)
    
- Run backfill jobs
    
- Make monolith read from new service
    
- Cut over writes once safe
    
- Decommission old tables
    

### **Example: Cloud SQL Migration Command**

```bash
gcloud sql instances create pricing-db \
  --database-version=POSTGRES_14 \
  --region=us-central1
```

---

## **10.2.5 Common Pitfalls**

- Big-bang rewrites → take years, often fail
    
- Extracting too broadly instead of slicing
    
- Migrating data before routing traffic
    
- Forgetting that monolith code may rely on shared in-memory state
    

---

# **10.3 Hybrid Deployments**

During migration, workloads run in:

- Legacy monolith
    
- New microservices
    
- Transitional gateways or adapters
    

This hybrid state can last months or years.

---

## **10.3.1 Routing Traffic Through a Strangler Proxy**

The Strangler Fig pattern typically wraps the monolith with a routing layer:

```
          Ingress Gateway
                 │
         Strangler Router
        ┌─────────┴─────────┐
        │                   │
   New Service          Monolith
```

### **Example Using Istio VirtualService**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: checkout-router
spec:
  hosts:
  - checkout.example.com
  http:
  - match:
    - uri:
        prefix: /checkout/v2
    route:
    - destination:
        host: checkout-service
        port:
          number: 80
  - route:
    - destination:
        host: monolith
        port:
          number: 8080
```

**Explanation:**

- Calls to `/checkout/v2` go to new microservice.
    
- Everything else continues hitting the monolith.
    

---

## **10.3.2 Shared Session Management**

You may need:

- Shared Redis session store
    
- JWT tokens signed with same key
    
- Shared user identity provider
    

### Example: Shared Session Cache Setup

```bash
gcloud redis instances create session-cache \
  --size=5 \
  --region=us-central1
```

---

## **10.3.3 Observability for Hybrid Deployments**

Important:

- Add explicit tracing context propagation across monolith and new service
    
- Collect metrics for old vs new traffic
    
- Capture errors per route
    

### Example: Adding Trace Headers in Monolith Adapter

```java
HttpGet req = new HttpGet(url);
req.addHeader("x-request-id", requestId);
req.addHeader("x-b3-traceid", traceId);
```

---

## **10.3.4 Common Pitfalls**

- Diverging business logic between monolith and service
    
- “Dual writes” causing data drift
    
- Timeouts and retries misaligned across systems
    
- Failing to monitor hybrid paths → blind spots
    

---

# **10.4 Phased Rollout Patterns**

Small, incremental rollouts reduce risk and enable safe migration.

---

## **10.4.1 Pattern 1 — Feature Flags**

Control rollout of new microservice logic inside the monolith.

### Example: Env Flag for Pricing

```python
if FEATURE_FLAG_PRICING_V2:
    price = call_pricing_v2()
else:
    price = calculate_price_monolith()
```

---

## **10.4.2 Pattern 2 — Traffic Splitting via Mesh**

Gradually shift traffic from monolith to new service.

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: pricing
spec:
  http:
  - route:
    - destination:
        host: pricing-service
      weight: 10
    - destination:
        host: monolith
      weight: 90
```

Move from 10% → 25% → 50% → 100% as metrics indicate stability.

---

## **10.4.3 Pattern 3 — Shadow Traffic / Mirroring**

Send a copy of production traffic to the new service **without** affecting users.

```yaml
http:
- route:
  - destination:
      host: monolith
- mirror:
    host: pricing-service
```

Monitor:

- Latency differences
    
- Output discrepancies
    
- Error rates
    

---

## **10.4.4 Pattern 4 — Canary Releases**

Deploy new service versions incrementally using mesh rules.

```yaml
http:
- route:
  - destination:
      host: pricing-service
      subset: v1
    weight: 75
  - destination:
      host: pricing-service
      subset: v2
    weight: 25
```

---

## **10.4.5 Pattern 5 — Parallel Run**

Run both implementations in production and compare outcomes.

Useful when:

- Highly sensitive workflows
    
- Financial calculations
    
- Fraud scoring
    
- Machine learning logic
    

---

## **10.4.6 Common Pitfalls**

- Jumping from 0% → 100% rollout without measuring
    
- Shadow traffic that isn't representative
    
- Canary subsets not deployed correctly (subset mismatch → 503s)
    
- Not gating rollout with SLO-based triggers
    

---

# **10.5 Sunset & Decommissioning**

Once functionality is fully migrated, the old monolith logic must be carefully decommissioned.

---

## **10.5.1 Decommissioning Steps**

### **1. Validate No More Traffic Hits Monolith Route**

Check Ingress or mesh metrics.

```bash
kubectl -n istio-system logs --selector app=istio-ingressgateway | grep /pricing
```

### **2. Disable Feature Flags**

Turn off fallback logic.

### **3. Backup Legacy Data**

Ensure irreversible data isn't lost.

### **4. Remove Legacy Code Paths**

Delete monolith code.

### **5. Decommission Infrastructure**

- Delete monolith deployment
    
- Deallocate compute resources
    
- Archive repos
    
- Remove DNS entries
    

### **6. Validate Downstream Dependencies**

Ensure no lingering callers of monolith endpoints.

---

## **10.5.2 Example: Removing Monolith Service**

```bash
kubectl delete deploy monolith
kubectl delete svc monolith
```

---

## **10.5.3 Archiving Legacy Data**

Export old data to BigQuery or Cloud Storage.

```bash
bq extract --destination_format CSV pricing_dataset.pricing_table gs://archive/pricing.csv
```

---

## **10.5.4 Common Pitfalls**

- Forgetting hidden dependencies on the monolith (batch jobs, cron jobs)
    
- Frontend still calling monolith endpoints
    
- Not validating that new service handles rare edge cases
    
- Mismanaging data migration → loss or duplication
    
- Removing infrastructure before incident-free operation window
    

---

# **Chapter 11 — VPC Design, Shared VPC & CIDR Strategy**

_(Expanded with senior-level clarity, diagrams-in-text, commands, and real-world architecture guidance.)_

A well-designed VPC architecture is the backbone of a secure, scalable GCP platform. Poor network design leads to overlapping CIDRs, subnet exhaustion, unusable IP ranges, and expensive redesigns. This chapter covers foundational VPC concepts, Shared VPC best practices, IP address planning, subnet delegation, and scaling limits.

---

# **11.1 VPC Fundamentals**

GCP Virtual Private Cloud (VPC) is a **global**, **software-defined**, **virtual network** that spans all regions by default.

---

## **11.1.1 Key Characteristics of GCP VPC**

### **Global Scope**

A VPC exists across all regions simultaneously:

```
              ┌────────────┐
              │   Global   │
              │    VPC     │
              └────────────┘
                /    |    \
      us-central1  europe-west1  asia-east1
```

You create regional subnets inside the VPC, but routing is global.

### **Native VPC Routing**

- No need for per-region VPCs unless isolation is required.
    
- VPC handles dynamic routing across all subnets automatically.
    

### **Firewall Rules**

Network firewalls are distributed:

- Apply at the VM/instance level
    
- Directional: INGRESS / EGRESS
    
- Priority-based
    

### **Routing Basics**

Routing table is global:

- System routes (subnet → instance)
    
- Static routes
    
- Dynamic BGP routes (Cloud Router)
    

---

## **11.1.2 Example: Creating a VPC**

```bash
gcloud compute networks create prod-vpc \
  --subnet-mode=custom \
  --bgp-routing-mode=global
```

**Explanation:**

- `--subnet-mode=custom` gives full control over subnet CIDRs.
    
- `--bgp-routing-mode=global` ensures multi-region hybrid routing.
    

---

## **11.1.3 Common Pitfalls**

- Using `auto` VPC mode → forces pre-created subnets with poor CIDRs.
    
- Creating separate VPCs per environment unnecessarily.
    
- Misunderstanding that VPC is global → assuming regional isolation.
    
- Not setting firewall defaults to deny → accidental exposure.
    

---

# **11.2 Shared VPC Architecture**

Shared VPC allows multiple **service projects** to use a central **host project’s VPC**.  
This is the preferred model for enterprise-scale GCP environments.

---

## **11.2.1 Architecture Overview**

```
               Shared VPC Host Project
                 ┌──────────────────┐
                 │ prod-shared-vpc │
                 │   (VPC lives)   │
                 └───────┬─────────┘
                         │
     ┌───────────────────┼───────────────────┐
     │                   │                   │
Service Project A   Service Project B   Service Project C
(GKE cluster)        (Databases)          (App teams)
```

### **Key Benefits**

- Centralized control over networking
    
- Strong IAM separation between teams
    
- Standardized firewall & routing
    
- Fewer NAT and VPN/Interconnect resources
    
- Reduced management overhead
    

---

## **11.2.2 Assigning a Project to Shared VPC**

Enable Shared VPC:

```bash
gcloud compute shared-vpc enable prod-shared-vpc
```

Attach service project:

```bash
gcloud compute shared-vpc associated-projects add \
  --host-project=prod-shared-vpc \
  app-prod-pricing
```

---

## **11.2.3 IAM Roles Needed for GKE in a Service Project**

Service project requires minimal IAM roles on host project:

```bash
gcloud projects add-iam-policy-binding prod-shared-vpc \
  --member="serviceAccount:service-<PROJECT_NUM>@container-engine-robot.iam.gserviceaccount.com" \
  --role="roles/compute.networkUser"
```

_(This allows GKE nodes to use subnets in the shared VPC.)_

---

## **11.2.4 Firewall Design**

**Golden rule:** service projects cannot create or modify firewall rules.  
Use centralized firewall policies.

Example firewall rule allowing pods egress to the internet via Cloud NAT:

```bash
gcloud compute firewall-rules create allow-egress-internet \
  --network=prod-vpc \
  --direction=EGRESS \
  --priority=1000 \
  --action=ALLOW \
  --destination-ranges=0.0.0.0/0 \
  --rules=tcp:80,tcp:443
```

---

## **11.2.5 Common Pitfalls**

- Granting service projects excessive IAM (especially `compute.admin`).
    
- Using Shared VPC with auto-mode subnets → collisions and poor IPv4 planning.
    
- Forgetting to centralize NAT → egress complexity.
    
- Over-segmenting VPCs → unnecessary fragmentation.
    

---

# **11.3 IP Address Planning**

IP planning is one of the most critical aspects of VPC design.  
Bad planning leads to CIDR exhaustion, overlapping ranges, cross-region conflicts, and painful future migrations.

---

## **11.3.1 Principles of Good Address Planning**

### **1. Leave Room for Growth**

Always allocate bigger CIDRs than you think you need.

### **2. Segment by Environment**

```
Prod:       10.0.0.0/12  
Non-Prod:   10.16.0.0/12  
Sandbox:    10.32.0.0/12
```

### **3. Segment by Region**

```
us-central1:   10.0.0.0/16  
europe-west1:  10.1.0.0/16  
asia-east1:    10.2.0.0/16
```

### **4. Segment by Service Type**

```
Nodes:   10.0.0.0/18  
Pods:    10.0.64.0/18  
Services:10.0.128.0/20
```

---

## **11.3.2 Example: Creating Subnets for GKE**

```bash
gcloud compute networks subnets create gke-nodes-uscentral1 \
  --network=prod-vpc \
  --region=us-central1 \
  --range=10.0.0.0/18
```

Pod and service CIDRs belong to the cluster, not the VPC.

### Example GKE cluster specifying Pod CIDR:

```bash
gcloud container clusters create api-cluster \
  --region=us-central1 \
  --enable-ip-alias \
  --cluster-ipv4-cidr=10.0.64.0/18 \
  --services-ipv4-cidr=10.0.128.0/20 \
  --subnetwork=gke-nodes-uscentral1
```

---

## **11.3.3 CIDR Antipatterns**

### **Antipattern 1 — Using 10.0.0.0/8**

Too large, leads to:

- Collisions with partner networks
    
- Conflicts during hybrid connectivity
    

### **Antipattern 2 — Overlapping CIDRs**

Makes VPN/Interconnect impossible.

### **Antipattern 3 — Tiny Subnets**

Subnet exhaustion → cluster outages.

Example: GKE node pool with /28 is too small for scaling.

---

## **11.3.4 Sizing Guidelines**

### **Node Pools**

- Minimum **/23** for active workloads
    
- /25 or smaller only for development envs
    

### **Pod CIDRs**

Each node needs ~256 pod IPs:

```
Node count * 256 <= Pod CIDR size
```

---

## **11.3.5 Example Sizing Calculation**

Cluster with:

- 30 nodes
    
- Each node capable of 110 pods
    

Pod CIDR must support **30 * 110 = 3300 pod IPs**.

A **/20** (4096 IPs) is suitable.

---

## **11.3.6 Common Pitfalls**

- Underestimating pod IP needs → scheduling failures
    
- Forgetting that multi-cluster means multi-CIDR
    
- Reusing old on-prem CIDRs without checking overlap
    
- Tight subnets preventing autoscaling
    

---

# **11.4 Subnet Delegation**

Subnet delegation assigns specific subnets to specific systems to avoid IP conflicts and maintain clarity.

---

## **11.4.1 Why Delegate Subnets?**

Each type of resource should have predictable ranges:

- GKE node subnets
    
- GKE control plane master range
    
- Private Service Connect ranges
    
- Serverless VPC Connector ranges
    
- Redis / SQL private service ranges
    

This improves:

- Troubleshooting
    
- Security policies
    
- Routing clarity
    

---

## **11.4.2 Example Subnet Delegations**

```
10.0.0.0/18     → GKE nodes
10.0.64.0/18    → GKE pods (cluster internal)
10.0.128.0/20   → Services CIDR (cluster internal)
10.1.0.0/20     → PSC endpoints
10.1.16.0/28    → Serverless VPC connector
```

---

## **11.4.3 PSC (Private Service Connect) Example**

Create PSC subnet:

```bash
gcloud compute networks subnets create psc-subnet \
  --network=prod-vpc \
  --region=us-central1 \
  --range=10.1.0.0/20 \
  --purpose=PRIVATE_SERVICE_CONNECT
```

---

## **11.4.4 Serverless VPC Connector Example**

```bash
gcloud compute networks vpc-access connectors create connector \
  --region=us-central1 \
  --network=prod-vpc \
  --range=10.1.16.0/28
```

---

## **11.4.5 Subnet Delegation for GKE Services**

GKE internally assigns:

- Pod CIDR
    
- Service CIDR
    

Ensure they don’t overlap with:

- On-prem networks
    
- Other cluster’s CIDRs
    
- PSC or Cloud SQL private ranges
    

---

## **11.4.6 Common Pitfalls**

- PSC ranges overlapping with pod ranges
    
- Too-small serverless connector ranges → connector failing to scale
    
- Not reserving space for future node pools
    
- Mixing different subnet purposes → impossible to troubleshoot
    

---

# **11.5 VPC Scaling & Limits**

GCP VPCs scale extremely well but have important limits.

---

## **11.5.1 Key Limits**

### **Subnets per VPC**

- Up to **15,000** subnets  
    → rarely a practical concern
    

### **Firewall Rules**

- 15,000 per network  
    → must use hierarchical firewall policies for manageability
    

### **Routes**

- 500 dynamic + 200 static per Cloud Router  
    → becomes a concern in multi-region hybrid systems
    

### **Forwarding Rules**

- Each LB uses forwarding rules; quotas differ per region
    

### **Node IP Scaling**

Pods/Nodes require careful IP planning.

---

## **11.5.2 Cloud NAT Scaling**

Cloud NAT supports:

- Millions of concurrent connections
    
- Thousands of VMs
    
- Regional NATs per VPC/subnet
    

Use multiple NAT gateways for:

- Tenant-level separation
    
- Egress control
    
- Resilience against single NAT overload
    

---

## **11.5.3 Hybrid Scaling Limits (VPN / Interconnect)**

### **Cloud VPN**

- Limited throughput (~3Gbps per tunnel)
    
- Use HA-VPN for production
    

### **Interconnect**

- 10Gbps or 100Gbps links
    
- Supports multiple VLAN attachments
    

### **Routing Limits**

Large enterprises hit Cloud Router limits long before VPC limits.

---

## **11.5.4 Common Pitfalls**

- Hitting Cloud Router route limits in hybrid networks
    
- Too many firewall rules → degraded performance
    
- NAT exhaustion due to high egress fan-out
    
- Underestimating the number of IPs needed per GKE cluster
    
- Thinking “VPCs don’t have limits” → they do at router/load balancer layers
    

---

# **Chapter 12 — Subnets, Firewalls & Routing**

_(Expanded with senior-level clarity, real networking examples, commands, and configuration snippets.)_

This chapter explains how to design subnets, apply hierarchical firewalls, configure routing, enforce Private Google Access, and understand the conceptual differences between AWS and GCP routing. These are foundational to secure, scalable VPC architecture.

---

# **12.1 Subnet Design**

Subnets in GCP are **regional** resources carved from a global VPC. Each subnet is independent, even though all are routable to each other by default.

---

## **12.1.1 Subnet Fundamentals**

### Key properties of a GCP subnet:

- Region-scoped
    
- Single primary IPv4 range
    
- Optional secondary ranges (Pods and Services for GKE)
    
- Automatically routable to all other subnets in same VPC
    
- Attached to one VPC only
    

---

## **12.1.2 Subnet Design Principles**

### **1. Align Subnets With Environment Boundaries**

```
prod-us-central1
staging-europe-west1
dev-us-east1
```

### **2. Allocate Large Enough Ranges**

Avoid subnets that cannot scale node pools or VM counts.

### **3. Separate Roles by Subnet**

- GKE nodes
    
- PSC endpoints
    
- Serverless connectors
    
- Databases
    
- Internal services
    

### **4. Reserve Space for Growth**

Especially for GKE Pod CIDRs.

---

## **12.1.3 Example: Creating a Subnet**

```bash
gcloud compute networks subnets create prod-nodes-uscentral1 \
  --network=prod-vpc \
  --region=us-central1 \
  --range=10.0.0.0/18 \
  --secondary-range=pods=10.0.64.0/18,services=10.0.128.0/20
```

**Explanation:**

- `--range` = node subnet
    
- `pods` secondary range = pod IPs
    
- `services` secondary range = service cluster IPs
    

---

## **12.1.4 Anti-Patterns**

### **Anti-Pattern 1 — Tiny Subnets**

Example: `/24` for a node pool → IP exhaustion.

### **Anti-Pattern 2 — Mixing Serverless and GKE Nodes**

PSC or VPC connectors crowd node IPs.

### **Anti-Pattern 3 — Not Reserving Future CIDR Expansion**

Changing subnet CIDRs later is extremely disruptive.

---

## **12.1.5 Practical Example: Subnet Layout for Region**

```
us-central1:
  nodes:       10.0.0.0/18
  pods:        10.0.64.0/18
  services:    10.0.128.0/20
  psc:         10.0.144.0/20
  serverless:  10.0.160.0/28
```

---

# **12.2 Hierarchical Firewalls & Policies**

Hierarchical firewalls in GCP allow you to apply security policies at:

- Organization level
    
- Folder level
    
- Project level
    
- VPC level
    

They override or augment project-level firewall rules.

---

## **12.2.1 Firewall Layers**

### **Hierarchy**

```
Org Policies (strongest)
↓
Folder Policies
↓
Project Policies
↓
VPC Firewall Rules (weakest)
```

If conflicts exist: **deny wins over allow**.

---

## **12.2.2 Using Hierarchical Firewall Policies**

### Example: Block all egress except approved destinations

**policy.yaml**

```yaml
rules:
  - priority: 1000
    match:
      destIpRanges:
      - "0.0.0.0/0"
    action: deny
    direction: EGRESS
  - priority: 900
    match:
      destIpRanges:
      - "172.16.0.0/12"
    action: allow
    direction: EGRESS
```

Apply at folder level:

```bash
gcloud compute org-security-policies import \
  --security-policy=prod-egress-policy \
  --source=policy.yaml \
  --folder=12345678901
```

---

## **12.2.3 VPC Firewall Rules Example**

Allow ingress from Cloud NAT to nodes:

```bash
gcloud compute firewall-rules create allow-nat-egress \
  --direction=INGRESS \
  --action=ALLOW \
  --rules=tcp:80,tcp:443 \
  --network=prod-vpc \
  --source-ranges=130.211.0.0/22
```

---

## **12.2.4 Enforcement Best Practices**

- Deny-all at the top, then allow specific flows.
    
- Use tags or service accounts instead of IPs.
    
- Avoid project-level firewall sprawl.
    
- Keep naming consistent and descriptive.
    

---

## **12.2.5 Common Pitfalls**

- Using project rules instead of hierarchical policies → drift.
    
- Accidentally blocking GKE control-plane IPs → cluster breaks.
    
- Not understanding allow/deny evaluation order.
    
- Overusing IP-based rules instead of identities.
    

---

# **12.3 Dynamic Routing & Route Priorities**

Routing is automatic within a VPC, but you can add static routes or dynamic routes using Cloud Router (BGP).

---

## **12.3.1 Routing Basics**

Each VPC maintains a **global routing table** with:

- Subnet routes
    
- Static routes
    
- Dynamic (BGP) routes
    
- Peering routes
    

Traffic always chooses **longest prefix match**.

---

## **12.3.2 Route Priority**

Routes have priorities (default = 1000).  
Lower number = higher priority.

### Example: Adding a Static Route With High Priority

```bash
gcloud compute routes create force-route-onprem \
  --network=prod-vpc \
  --priority=10 \
  --next-hop-ip=192.168.1.1 \
  --destination-range=10.50.0.0/16
```

This route takes precedence over any overlapping regional subnet route.

---

## **12.3.3 Dynamic Routing via Cloud Router (BGP)**

Used for:

- Cloud VPN
    
- Interconnect
    
- Multi-region VPC expansion
    
- Route exchange with on-prem
    

### Example: Creating a Cloud Router

```bash
gcloud compute routers create prod-router \
  --network=prod-vpc \
  --asn=64512 \
  --region=us-central1
```

### Example: Adding a BGP Peer

```bash
gcloud compute routers add-bgp-peer prod-router \
  --peer-name=onprem \
  --interface=onprem-if \
  --peer-asn=65001 \
  --region=us-central1 \
  --peer-ip-address=169.254.100.2
```

---

## **12.3.4 Common Pitfalls**

- Conflicting priorities → traffic routed incorrectly.
    
- Forgetting that Cloud Router routes propagate globally.
    
- Overlapping CIDRs from on-prem → route instability.
    
- Missing firewall rules for BGP peering traffic.
    

---

# **12.4 Private Google Access**

Private Google Access (PGA) allows VMs, pods, and serverless resources with **no external IP** to reach:

- Google APIs
    
- Artifact Registry
    
- GCS
    
- Cloud SQL via PSC
    
- Pub/Sub
    
- GKE control plane
    

without using the internet.

---

## **12.4.1 Why It’s Required**

You must enable PGA when:

- Nodes don’t have public IPs
    
- Pods need to pull images
    
- Terraform/CI needs to call Google APIs
    
- Serverless VPC connector is used
    
- Egress needs to remain inside Google backbone
    

---

## **12.4.2 Example: Enable Private Google Access on a Subnet**

```bash
gcloud compute networks subnets update prod-nodes-uscentral1 \
  --region=us-central1 \
  --enable-private-ip-google-access
```

---

## **12.4.3 PGA for GKE Nodes and Pods**

Nodes: enabled via subnet  
Pods: automatically inherit if using VPC-native mode

### Confirm via metadata server test inside pod:

```bash
curl -H "Metadata-Flavor: Google" \
    http://metadata.google.internal/computeMetadata/v1/
```

If reachable → PGA works.

---

## **12.4.4 Private Service Connect for Google APIs**

Preferred modern alternative:

```bash
gcloud compute forwarding-rules create google-apis-psc \
  --network=prod-vpc \
  --region=us-central1 \
  --target-google-apis-region=us-central1 \
  --address=10.1.0.2
```

Use this for:

- Guaranteed private path
    
- Regionalized access
    
- Residency guarantees
    

---

## **12.4.5 Common Pitfalls**

- Forgetting to enable PGA on serverless connector subnets → silent failures.
    
- Pods cannot pull images due to PGA misconfiguration.
    
- Cloud NAT not used for egress → blocked access.
    
- Assuming PGA applies globally—it is _subnet-scoped_.
    

---

# **12.5 AWS vs GCP Routing (Conceptual Comparison)**

Understanding GCP vs AWS routing differences helps when migrating or designing hybrid cloud architectures.

---

## **12.5.1 VPC Scope Differences**

### **AWS**

- VPCs are **regional**
    
- Subnets are zone-scoped
    
- Routing tables are per-subnet
    

### **GCP**

- VPCs are **global**
    
- Subnets are regional
    
- One global routing table
    

---

## **12.5.2 Route Behavior Differences**

### **AWS**

- Routing tables must be explicitly associated with subnets.
    
- More control → more complexity.
    

### **GCP**

- Routing is automatic and global.
    
- Simpler but requires careful CIDR planning.
    

---

## **12.5.3 Firewall Model Differences**

### **AWS Security Groups**

- Stateful
    
- Applied per interface
    
- Allow-only model
    

### **GCP Firewalls**

- Also stateful
    
- Distributed firewall model
    
- Deny and allow rules
    
- Can use hierarchical firewall policies (AWS cannot)
    

---

## **12.5.4 NAT Differences**

### **AWS**

- NAT Gateways deployed per AZ
    
- Expensive at scale
    

### **GCP**

- Cloud NAT is regional
    
- Autoscaling
    
- Much cheaper
    
- No per-AZ HA concerns
    

---

## **12.5.5 Load Balancing Differences**

### **AWS**

- ALB/NLB are regional
    
- Global LB requires Route53
    

### **GCP**

- True global L7 & L4 load balancers
    
- Edge termination near users
    
- Better for multi-region active-active
    

---

## **12.5.6 Key Takeaways**

|Feature|AWS|GCP|
|---|---|---|
|VPC Scope|Regional|Global|
|Routing|Per-subnet tables|Global route table|
|NAT|Per-AZ|Regional|
|Firewall Policies|No hierarchy|Org → Folder → Project → VPC|
|Load Balancing|Mostly regional|Global & regional options|

---

## **12.5.7 Common Pitfalls When Porting AWS Designs to GCP**

- Recreating per-subnet routing tables (unnecessary in GCP)
    
- Overusing separate VPCs instead of one global VPC
    
- Assuming NAT is AZ-scoped—it's regional in GCP
    
- Trying to recreate AWS Transit Gateway—GCP’s equivalent is different (HA-VPN + Interconnect + Cloud Router)
    

---

# **Chapter 13 — Hybrid Connectivity: VPN, Interconnect & BGP**

_(Expanded with senior-level clarity, diagrams-in-text, commands, configs, and real-world design guidance.)_

Hybrid connectivity creates the network bridge between **on-prem**, **other clouds**, and **GCP**. This chapter explains how to design secure IPSec tunnels, deploy HA VPN, architect Dedicated/Partner Interconnect, design BGP topologies, and build redundant, failure-resistant hybrid networks.

---

# **13.1 Cloud VPN (IPSec)**

Cloud VPN establishes encrypted site-to-site IPSec tunnels between GCP and external networks.

---

## **13.1.1 Types of Cloud VPN**

There are two main models:

### **1. Classic VPN** _(Legacy)_

- Single tunnel per gateway
    
- Max ~1.5 Gbps throughput
    
- No SLA
    
- No auto-failover
    

### **2. HA VPN** _(Recommended)_

- Two interfaces per gateway
    
- Two tunnels per interface → 4 tunnels total
    
- SLA-backed
    
- BGP dynamic routing
    

**This chapter focuses on HA VPN**, except where clarification is needed.

---

## **13.1.2 Key Characteristics of Cloud VPN**

- Encrypted IPSec tunnels
    
- Supports static or dynamic routing
    
- Connects to on-prem firewalls/routers
    
- Regional resource
    
- Can connect to AWS/Azure via VPN gateways
    

---

## **13.1.3 Example: Creating a Classic VPN Tunnel**

_(Not recommended for production, provided for completeness.)_

```bash
gcloud compute vpn-gateways create legacy-gw \
  --network=prod-vpc \
  --region=us-central1
```

Then create tunnels:

```bash
gcloud compute vpn-tunnels create legacy-tunnel \
  --peer-address=203.0.113.10 \
  --shared-secret="mysecret" \
  --ike-version=2 \
  --vpn-gateway=legacy-gw \
  --region=us-central1
```

---

## **13.1.4 Common Pitfalls**

- Using classic VPN for production/hybrid failover
    
- No redundancy → single IPSec connection
    
- Incorrect MTU → fragmentation and slow traffic
    
- Forgetting firewall rules for ESP, UDP 500, UDP 4500
    

---

# **13.2 HA VPN Architecture**

HA VPN provides high availability, multi-tunnel redundancy, and BGP dynamic routing.

---

## **13.2.1 HA VPN Architecture Diagram**

```
               On-Prem Router
                   │
     ┌─────────────┼─────────────┐
     │             │             │
  Tunnel A1     Tunnel A2     (HA Pair)
     │             │
 ┌────┴─────┐  ┌────┴─────┐
 │  HA VPN  │  │  HA VPN  │  (Two interfaces)
 │ Interface A │ │ Interface B │
 └────────────┘ └────────────┘
        │               │
      VPC             VPC
```

Each interface creates two tunnels → **total 4** tunnels per on-prem device (if supported).

---

## **13.2.2 Creating HA VPN Gateway**

```bash
gcloud compute vpn-gateways create prod-ha-gw \
  --network=prod-vpc \
  --region=us-central1
```

---

## **13.2.3 Creating an HA BGP Interface**

```bash
gcloud compute vpn-gateways describe prod-ha-gw \
  --region=us-central1
```

This returns interface IPs:

- `interface 0: 35.x.x.x`
    
- `interface 1: 34.x.x.x`
    

These map to your on-prem router.

---

## **13.2.4 BGP Session Configuration**

### **Cloud Router**

```bash
gcloud compute routers create prod-router \
  --region=us-central1 \
  --network=prod-vpc \
  --asn=64512
```

### **Add BGP peer**

```bash
gcloud compute routers add-bgp-peer prod-router \
  --peer-name=onprem-peer-a \
  --interface=gcp-if-a \
  --peer-asn=65001 \
  --peer-ip-address=169.254.10.2 \
  --region=us-central1
```

_Note:_  
169.254.x.x is the standard RFC 3927 link-local IPSec tunnel addressing.

---

## **13.2.5 HA VPN Failover Behavior**

Failover happens when:

- Tunnel drops
    
- BGP session down
    
- On-prem device fails
    

Failover characteristics:

- <10 seconds convergence with BGP
    
- Session restarts automatically
    
- No manual intervention required
    

---

## **13.2.6 Common Pitfalls**

- Only configuring one tunnel per device → not true HA
    
- Mixing static and BGP routing
    
- BGP timers mismatched → slow failover
    
- Overly aggressive BGP timers → flap storms
    
- Forgetting ESP protocol firewall rules
    

---

# **13.3 Dedicated & Partner Interconnect**

Interconnect provides high-bandwidth, low-latency connectivity between on-prem and Google.

---

## **13.3.1 Dedicated vs Partner Interconnect**

### **Dedicated Interconnect**

- 10Gbps or 100Gbps links
    
- Direct physical fiber cross-connect
    
- Requires colocated presence in Google POP
    
- Best for high throughput (20+ Gbps)
    

### **Partner Interconnect**

- Third-party carrier (Equinix, Megaport) provides connectivity
    
- Flexible bandwidth from 50Mbps → 50Gbps
    
- No colocation needed
    
- Easier to deploy
    

---

## **13.3.2 Architecture**

```
             On-Prem DC
                 │
         ┌───────┴────────┐
         │ Partner / Colo │
         └───────┬────────┘
                 │ VLAN Attachments
                 ▼
         Google Edge (POP)
                 │
     ┌───────────┴───────────┐
     │         VPC           │
     └────────────────────────┘
```

---

## **13.3.3 Creating VLAN Attachments**

### **Dedicated Interconnect**

```bash
gcloud compute interconnects create dedicated-ic \
  --link-type=LINK_TYPE_ETHERNET_10G_LR \
  --location=zone1-us-central1 \
  --requested-link-count=2 \
  --customer-asn=65001
```

### **Partner Interconnect**

```bash
gcloud compute interconnects attachments partner create prod-vlan \
  --region=us-central1 \
  --router=prod-router \
  --edge-availability-domain=2 \
  --bandwidth=10G
```

---

## **13.3.4 BGP for Interconnect**

Interconnect uses BGP for:

- Failover
    
- Route propagation
    
- Multi-region routing
    
- Auto route learning
    

### Example: Add BGP peer for Interconnect

```bash
gcloud compute routers add-bgp-peer prod-router \
  --peer-name=partner-peer \
  --interface=interconnect-if \
  --peer-asn=65100 \
  --advertised-route-priority=100 \
  --region=us-central1
```

---

## **13.3.5 Pros & Cons**

### **Dedicated Interconnect Pros**

- Highest bandwidth
    
- Lowest latency
    
- SLA-backed
    
- Best for real-time and data-heavy workloads
    

### **Cons**

- Requires colocation
    
- Costly and longer lead time
    

### **Partner Interconnect Pros**

- Quick to deploy
    
- No colocation needed
    
- Flexible bandwidth
    

### **Cons**

- Extra provider dependency
    
- Must trust partner’s SLA
    

---

## **13.3.6 Common Pitfalls**

- Not using redundant attachments
    
- Misconfigured MTU → packet drops
    
- Overlapping CIDRs → BGP rejects routes
    
- Forgetting to enable global dynamic routing when needed
    

---

# **13.4 BGP Design & Failover**

BGP (Border Gateway Protocol) controls dynamic route advertisement across hybrid networks.

---

## **13.4.1 BGP Fundamentals**

Key concepts:

- **ASNs** identify routing domains
    
- **Prefixes** (CIDRs) are advertised
    
- **Route priority** influences path selection
    
- **Keepalives** & **hold timers** maintain sessions
    
- **Route propagation** spreads routes across VPCs and on-prem
    

---

## **13.4.2 BGP on Cloud Router**

Cloud Router:

- Supports **BGP only**
    
- Multi-region if using global dynamic routing
    
- Automatically learns/re-advertises GCP subnets
    
- Handles failover between tunnels/attachments
    

---

## **13.4.3 Route Selection Rules**

1. **Longest prefix match**
    
2. Lowest **MED**
    
3. Lowest **AS path length**
    
4. Lowest **priority (metric)**
    

You control:

- Advertised priority (`--advertised-route-priority`)
    
- Which prefixes you announce
    

---

## **13.4.4 Example: Prefer Interconnect over VPN**

### **Interconnect BGP priority:**

```bash
--advertised-route-priority=100
```

### **VPN BGP priority:**

```bash
--advertised-route-priority=200
```

**Result:**  
Traffic flows through Interconnect, fails over to VPN.

---

## **13.4.5 Example BGP High Availability Setup**

Two Cloud Routers in two regions:

```
On-Prem Router 
     │
──────────────
VPN/IC Attachments
──────────────
     │
Cloud Router A (us-central1)
Cloud Router B (us-east4)
```

Routes propagate globally (if enabled).

---

## **13.4.6 BGP Timers**

Default timers:

- Keepalive: 20s
    
- Hold timer: 60s
    

These balance:

- Stability
    
- Failover speed
    
- Avoiding flap storms
    

---

## **13.4.7 Common Pitfalls**

- Misaligned ASNs → sessions won’t start
    
- Forgetting firewall rules for BGP (TCP/179)
    
- Advertising too many prefixes → route table overflow
    
- Asymmetric routing due to overlapping priorities
    
- BGP flaps caused by poor on-prem HA
    

---

# **13.5 Redundancy Models**

Hybrid networks must plan for:

- Device failure
    
- Tunnel failure
    
- POP failure
    
- Regional failure
    
- Cable/fiber cuts
    
- Routing instability
    

Below are the recommended redundancy patterns.

---

## **13.5.1 Model A — VPN + VPN Redundancy**

```
On-Prem Router
   ├── Tunnel A (HA VPN)
   └── Tunnel B (HA VPN)
```

Pros: simple, cost-effective  
Cons: low bandwidth, higher latency

---

## **13.5.2 Model B — Interconnect + VPN Backup**

```
Interconnect (Primary)
   │
VPN (Backup)
```

Pros:

- High-bandwidth primary
    
- Automatic failover to VPN via BGP priorities
    

Cons:

- Higher complexity
    

---

## **13.5.3 Model C — Dual Interconnect (Highly Recommended)**

```
On-Prem
  │       │
IC A     IC B
  │       │
Google Edge POPs
```

Characteristics:

- Redundant POPs
    
- Redundant links
    
- Redundant Cloud Routers
    
- SLA-backed
    

---

## **13.5.4 Model D — Multi-Region Interconnect HA**

```
On-Prem
  │         │
IC A     IC B
  │         │
Region 1   Region 2
  │         │
VPC → Global Router Table
```

Pros:

- Survive total region outage
    
- Active-active routing across regions
    

---

## **13.5.5 Model E — Cloud Hub-and-Spoke Hybrid**

```
On-Prem
   │
Interconnect
   │
Hub VPC
   ├── Spoke VPC 1
   ├── Spoke VPC 2
   └── Spoke VPC 3
```

Used when:

- Multiple business units
    
- Multi-tenant SaaS
    
- Need centralized inspection
    

---

## **13.5.6 Example: Setting BGP Priorities for Failover**

Primary (Interconnect):

```bash
--advertised-route-priority=100
```

Secondary (VPN):

```bash
--advertised-route-priority=200
```

---

## **13.5.7 Common Pitfalls**

- Not planning for POP-level redundancy
    
- Misconfigured BGP priorities → traffic blackholing
    
- Single Cloud Router → single point of failure
    
- Relying solely on VPN for large workloads
    
- No testing of failover behavior under real load
    

---

# **Chapter 14 — Multi-Region Networking & Egress Optimization**

_(Expanded with senior-level clarity, diagrams, commands, and real-world architectural guidance.)_

Multi-region networking in GCP involves designing inter-region connectivity, peering strategies, egress-optimized topologies, and understanding low-level network behaviors such as MTU, fragmentation, and latency-path selection. This chapter provides the patterns, pitfalls, and configuration behaviors required to operate a global, latency-sensitive, cost-efficient platform.

---

# **14.1 Interconnect Between Regions**

GCP provides a global backbone network—**all regions are automatically interconnected using Google’s private fiber**. This enables low-latency and highly reliable multi-region traffic, including cluster-to-cluster or service-to-service flows.

---

## **14.1.1 Global Routing Model**

GCP uses **global dynamic routing**, meaning:

- All VPC subnets are reachable across regions.
    
- Cloud Routers can propagate routes globally.
    
- Hybrid routes learned in Region A are visible in Region B.
    

### Architecture Diagram

```
        ┌──────────────┐
        │   Region A    │
        │  prod-vpc     │
        └──────┬────────┘
               │  (Google Global Backbone)
        ┌──────┴────────┐
        │   Region B    │
        │  prod-vpc     │
        └───────────────┘
```

There is **no cost** for inter-region traffic _within_ the same VPC, but inter-region _egress_ to external endpoints is charged.

---

## **14.1.2 When to Use Multi-Region Interconnect**

Use multi-region connectivity if:

- Your platform is **active-active** across regions.
    
- You require **regional failover** of on-prem systems.
    
- You serve global customers.
    
- You need to minimize latency between services in different regions.
    

---

## **14.1.3 Example: Enabling Global Routing**

```bash
gcloud compute networks update prod-vpc \
  --bgp-routing-mode=global
```

This ensures Cloud Router routes propagate across all regions.

---

## **14.1.4 Hybrid Multi-Region Example**

```
On-Prem
  │
 Interconnect A ↔ Region A
 Interconnect B ↔ Region B
  │                 │
 Cloud Router A   Cloud Router B
  │                 │
   ↘             ↙
     Global VPC Routing
```

Use different priorities to prefer one region and fail over to another.

---

## **14.1.5 Common Pitfalls**

- Forgetting that VPN without global routing doesn’t propagate routes across regions.
    
- Using regional-only routing and expecting multi-region failover.
    
- Overloading inter-region bandwidth with chatty services.
    
- Assuming Interconnect is global—it’s always **region-specific**.
    

---

# **14.2 Peering Options & Constraints**

Peering enables communication with other GCP organizations, projects, or networks.

---

## **14.2.1 Types of Peering**

### **1. VPC Peering**

Direct connection between two VPCs.

Pros:

- Simple
    
- No VPN
    
- Low latency
    

Cons:

- **No transitive routing** (major constraint)
    
- Firewall policies are project-local
    
- CIDRs must not overlap
    

---

### **Example: Creating VPC Peering**

```bash
gcloud compute networks peerings create prod-to-analytics \
  --network=prod-vpc \
  --peer-network=analytics-vpc \
  --peer-project=analytics-proj \
  --auto-create-routes
```

---

### **2. Private Service Connect (PSC)**

Used for:

- Consuming services in another VPC
    
- Providing multi-tenant private endpoints
    
- Accessing Google APIs with privacy
    

PSC solves many limitations of VPC peering.

---

### **3. Cloud VPN / Cloud Interconnect**

Used for:

- Hybrid connectivity
    
- Connecting independent networks
    
- Overlapping address space (via NAT or custom translation)
    

---

## **14.2.2 Peering Constraints**

### **No Transitive Routing**

If:

```
A ↔ B ↔ C
```

Packets cannot flow from A → C.  
This breaks hub-and-spoke if not carefully planned.

### **CIDR Overlaps Are Not Allowed**

Overlapping CIDRs = peering fails.

### **Firewall Rules Are Not Shared**

Each VPC enforces its own rules.

---

## **14.2.3 Best Use Cases**

**VPC Peering**

- Same org
    
- Low-latency east/west traffic
    
- Non-overlapping CIDRs
    

**PSC**

- Multi-tenant SaaS platforms
    
- Private access to shared services
    
- When relying on explicit endpoints
    

**Interconnect/VPN**

- Hybrid or cross-org
    
- Overlapping CIDRs
    
- Large-scale data movement
    

---

## **14.2.4 Common Pitfalls**

- Using VPC peering for hub-and-spoke → breaks on transitive routing.
    
- Peering many VPCs → exponential operational complexity.
    
- Overlapping CIDRs cause silent failures or routing blackholes.
    
- Not using PSC for multi-tenant workloads → IP conflicts.
    

---

# **14.3 Egress Cost Minimization**

Egress cost optimization is often one of the highest-ROI network design activities. GCP charges for traffic **leaving** a region or Google network.

---

## **14.3.1 Key Cost Buckets**

### **1. Inter-region egress**

Traffic from one GCP region to another.

### **2. Egress to internet**

Traffic going to public IPs.

### **3. Egress from GCP to on-prem**

Varies by Interconnect/VPN.

### **4. Load Balancer egress**

Depends on endpoint and path.

---

## **14.3.2 Core Strategies for Reducing Egress Costs**

### **1. Keep East–West Traffic Regional**

Place dependent services in same region.

Example:

```
us-central1/frontend → us-central1/api → us-central1/db
```

Avoid:

```
us-central1/frontend → europe-west1/api
```

---

### **2. Use Global Load Balancers for User Traffic**

Global LB terminates closest to the client, reducing cross-region traversal.

---

### **3. Cache Everything (Cloud CDN / Redis)**

Caching reduces backend egress significantly.

---

### **4. Use Private Service Connect (PSC)**

PSC keeps traffic on Google's backbone.

PSC example:

```bash
gcloud compute forwarding-rules create internal-psc \
  --network=prod-vpc \
  --region=us-central1 \
  --address=10.1.0.5 \
  --target-service=projects/central-services/regions/us-central1/serviceAttachments/storage-svc
```

---

### **5. Optimize Data Transfer Across Regions**

Use:

- GCS regional buckets
    
- BigQuery regional datasets
    
- GKE clusters per region
    

Avoid:

- Multi-region storage for latency-sensitive or chatty workloads
    

---

## **14.3.3 Using Cloud Interconnect to Reduce Costs**

Interconnect provides cheaper hybrid egress than VPN or public IP egress.

---

## **14.3.4 Example: Enforcing Regional Traffic**

Using Istio locality load balancing:

```yaml
apiVersion: networking.istio.io/v1beta1
kind: DestinationRule
metadata:
  name: api-lb
spec:
  host: api.internal
  trafficPolicy:
    loadBalancer:
      localityLbSetting:
        distribute:
        - from: "us-central1/*"
          to:
          - region: us-central1
            percent: 100
```

---

## **14.3.5 Common Pitfalls**

- Deploying multi-region databases with heavy replication → massive egress costs.
    
- Using one global GKE cluster instead of regional clusters.
    
- Relying on public endpoints internally → unnecessary internet egress.
    
- Accidentally routing traffic between regions due to poor service discovery.
    

---

# **14.4 MTU, Latency & Packet Fragmentation Pitfalls**

Most real-world hybrid networking issues stem from MTU mismatches, fragmentation, and asymmetric routing. This section explains how to detect and fix them.

---

## **14.4.1 MTU Fundamentals**

The maximum transmission unit (MTU) is the largest packet size supported without fragmentation.

### GCP default MTUs:

- VPC = **1460 bytes**
    
- With IPSec VPN (~60 byte overhead) → **1400 bytes effective**
    
- With GRE/IPSec → **1360 bytes or lower**
    

---

## **14.4.2 Detecting MTU Issues**

Symptoms:

- TLS handshake failures
    
- Random 1–5% packet loss
    
- gRPC connections failing under load
    
- API calls failing only through VPN
    
- Traces showing increased retries
    

### Debug Example inside VM or Pod:

```bash
ping -M do -s 1472 8.8.8.8
```

- `-M do` = do not fragment
    
- If fails → MTU too large
    

---

## **14.4.3 Fixing MTU Problems**

### **Option 1 — Lower MTU on VMs or Pods**

VM example:

```bash
sudo ip link set dev eth0 mtu 1400
```

Istio sidecar example:

```yaml
traffic.sidecarProxy:
  meshExpansion:
    mtu: 1400
```

---

### **Option 2 — Force Path MTU Discovery**

Ensure firewalls allow ICMP "Fragmentation Needed" messages.

Missing this → PMTU blackholing.

```bash
gcloud compute firewall-rules create allow-icmp-frag-needed \
  --action=ALLOW \
  --direction=INGRESS \
  --rules=icmp \
  --network=prod-vpc
```

---

### **Option 3 — Resolve Hybrid MTU Mismatches**

Routers/firewalls often reduce MTU, e.g.:

```
GCP VPC MTU        = 1460
IPSec On-Prem      = ~1400
GRE On-Prem        = ~1360
```

Set the lowest MTU across all paths to avoid fragmentation.

---

## **14.4.4 Latency Impacts**

### Latency Sources:

- Distance between regions
    
- Routing asymmetry
    
- TCP retransmissions due to MTU issues
    
- Load balancer cross-region paths
    

### Example: Latency Measurement from VM

```bash
ping europe-west1-c.gcp-vm
```

OR for TCP latency:

```bash
curl -w "@curl-format.txt" -o /dev/null -s https://service.example.com
```

---

## **14.4.5 Packet Fragmentation Issues**

Fragmentation causes:

- Higher CPU usage
    
- Lower throughput
    
- Unpredictable performance
    
- gRPC streaming failures
    
- Dropped packets inside IPSec tunnels
    

Avoid fragmentation at all costs.

---

## **14.4.6 Common Pitfalls**

- Using MTU 1500 inside GKE → works internally, fails over VPN.
    
- Blocked ICMP causing PMTU discovery failure.
    
- Not reducing MTU for multi-hop encrypted links.
    
- gRPC and HTTP/2 traffic suffering due to fragmentation.
    
- On-prem network enforcing lower MTU silently.
    

---

# **Chapter 15 — DNS Architecture & Service Discovery**

_(Expanded with senior-level clarity, diagrams, commands, Istio configs, Cloud DNS examples, and multi-region strategies.)_

DNS is one of the most foundational—but frequently misunderstood—components of cloud networking. A resilient enterprise platform requires consistent naming, deterministic resolution across environments, secure separation of internal vs external namespaces, and fast service discovery across regions and clusters.

This chapter covers Cloud DNS fundamentals, private zones, split-horizon architecture, global DNS patterns, and mesh-native discovery.

---

# **15.1 Cloud DNS Overview**

Cloud DNS is Google’s scalable, low-latency DNS service—supporting both **public** and **private** DNS zones.

---

## **15.1.1 Key Features**

- Highly available, globally distributed
    
- Low-latency lookups
    
- Public and private DNS zones
    
- DNSSEC support
    
- Integration with VPC and hybrid networks
    
- Ability to create multi-region and multi-VPC resolution patterns
    

---

## **15.1.2 Types of DNS Zones**

### **1. Public Zones**

- Publicly resolvable
    
- Used for external traffic
    
- Backed by Google’s global anycast network
    
- Commonly used for:
    
    - `example.com`
        
    - `api.example.com`
        
    - `cdn.example.com`
        

### **2. Private Zones**

- Resolvable only from authorized VPCs or hybrid networks
    
- Used for cluster-internal, service-internal, or corporate-internal naming
    
- No external exposure by default
    

---

## **15.1.3 Example: Creating a Public Zone**

```bash
gcloud dns managed-zones create public-zone \
  --dns-name="example.com." \
  --visibility="public"
```

---

## **15.1.4 DNS Record Example**

```bash
gcloud dns records create \
    --zone="public-zone" \
    --name="api.example.com." \
    --type="A" \
    --ttl=300 \
    --rrdatas="34.98.112.10"
```

---

## **15.1.5 Common Pitfalls**

- Not using low TTLs during migration → slow cutovers
    
- Mixing private and public records for the same hostname
    
- Failing to assign reverse DNS records for hybrid environments
    
- Overreliance on CNAMEs in latency-sensitive paths
    

---

# **15.2 Private Zones**

Private DNS zones allow internal services to resolve private names without exposing them publicly.

---

## **15.2.1 Architecture Overview**

```
               Private Zone
         ┌────────────────────────┐
         │ internal.example.com.  │
         └───────┬───────────────┘
                 │ resolvable only by:
                 │
      ┌──────────┼──────────┐
      │          │          │
   Prod VPC   Staging VPC  On-Prem (via VPN/IC)
```

---

## **15.2.2 Creating a Private Zone**

```bash
gcloud dns managed-zones create internal-zone \
  --dns-name="internal.example.com." \
  --visibility="private" \
  --networks="prod-vpc"
```

Add additional networks later:

```bash
gcloud dns managed-zones update internal-zone \
  --add-visibility-network="staging-vpc"
```

---

## **15.2.3 Example: Creating Records in Private Zone**

```bash
gcloud dns records create \
    --zone="internal-zone" \
    --name="api.internal.example.com." \
    --type="A" \
    --ttl=60 \
    --rrdatas="10.0.12.15"
```

---

## **15.2.4 Authorizing On-Prem to Use Cloud DNS**

Cloud DNS supports hybrid DNS forwarding.

1. Create a forwarding zone on-prem → points to Cloud DNS
    
2. Allow from Cloud Router → ensures DNS flows
    

---

## **15.2.5 DNS Peering Between VPCs**

Allows VPC A to resolve VPC B’s private zone without directly attaching networks.

### Example:

```bash
gcloud dns managed-zones create analytics-peering \
  --dns-name="analytics.internal." \
  --visibility="private" \
  --target-network="prod-vpc" \
  --forwarding
```

---

## **15.2.6 Common Pitfalls**

- Forgetting that private zones do not support overlapping DNS names.
    
- Using wildcard `*.internal.example.com` for too many services → debugging nightmare.
    
- Not lowering TTLs during migration.
    
- Failing to authorize all VPCs for private zone lookup.
    

---

# **15.3 Split-Horizon DNS**

Split-horizon DNS means the **same domain name resolves differently** depending on whether the client is internal or external.

Example:

```
api.example.com
→ external clients: resolves to public LB IP
→ internal workloads: resolves to internal LB IP
```

---

## **15.3.1 Why Split-Horizon Matters**

- Reduce egress cost
    
- Avoid public internet routing for internal services
    
- Improve security
    
- Enable multi-region failover
    
- Provide consistent naming across environments
    

---

## **15.3.2 Example Architecture**

```
Public Zone:
  api.example.com → 34.x.x.x (public LB)

Private Zone:
  api.example.com → 10.0.1.5 (internal LB)
```

---

## **15.3.3 Implementing Split-Horizon DNS in Cloud DNS**

### Step 1 — Create public zone

```bash
gcloud dns managed-zones create external-zone \
  --dns-name="example.com." \
  --visibility="public"
```

### Step 2 — Create private zone with same domain

```bash
gcloud dns managed-zones create internal-zone \
  --dns-name="example.com." \
  --visibility="private" \
  --networks="prod-vpc"
```

### Step 3 — Add different A records

Public:

```bash
api.example.com. A 34.98.100.10
```

Private:

```bash
api.example.com. A 10.0.2.5
```

Cloud DNS will **automatically prefer** internal zone when the request originates from internal resources.

---

## **15.3.4 Common Pitfalls**

- Accidentally leaking internal IPs in public zones.
    
- Conflicts between public & private zones if names aren’t aligned.
    
- Hybrid clients using the wrong DNS servers → inconsistent behavior.
    
- On-prem resolvers failing to forward internal lookups.
    

---

# **15.4 Cross-Region DNS Patterns**

Multi-region architectures require DNS routing that remains consistent during failover, user proximity shifts, and maintenance events.

---

## **15.4.1 Pattern 1 — Global Load Balancer + Geo Routing**

Use Cloud HTTP(S) Global Load Balancer:

- Terminate TLS at the nearest Google edge
    
- Route to closest healthy backend region
    
- Automatically fail over
    

DNS resolves to single anycast IP.

**Example Record:**

```
api.example.com → 34.x.x.x (global LB IP)
```

This solves:

- Latency
    
- Failover
    
- Cross-region balancing
    

---

## **15.4.2 Pattern 2 — Region-Specific Hostnames (Controlled Failover)**

```
us.api.example.com → US region LB
eu.api.example.com → EU region LB
```

Switch traffic:

- During incident
    
- Canary testing
    
- Residency constraints
    

---

## **15.4.3 Pattern 3 — Multi-Region Internal DNS**

Use Private DNS + regional service IPs:

```
api.internal.example.com
  → us-central1: 10.0.1.10
  → europe-west1: 10.4.1.10
```

Enhance with:

- Istio locality load balancing
    
- Regional gateway routing
    
- Internal passthrough LBs
    

---

## **15.4.4 Pattern 4 — Failover Controlled by DNS TTL**

TTL determines how fast clients will switch endpoints.

Recommended:

```
Public TTL: 30–60 seconds  
Internal TTL: 10–30 seconds
```

---

## **15.4.5 Pattern 5 — Private Service Connect for Cross-Region Services**

PSC does **not** support global endpoints, but can be manually deployed regionally:

```
psc-us → 10.0.10.5
psc-eu → 10.4.10.5
```

Choose endpoint based on:

- Region of workload
    
- Latency
    
- Lawful residency
    

---

## **15.4.6 Common Pitfalls**

- Using multi-region GCS buckets for high-QPS workloads → DNS-based routing issues.
    
- TTLs too long → slow failover.
    
- Relying solely on DNS-based failover instead of LB-level failover.
    
- Forgetting that DNS failover ≠ TCP connection failover.
    

---

# **15.5 Mesh-Based Service Discovery**

Service meshes provide service discovery via **xDS** (Envoy control-plane APIs), eliminating reliance on DNS for east–west traffic.

---

## **15.5.1 Mesh Discovery Model**

In Istio/Envoy:

- Each service has a **cluster** name
    
- Control plane provides endpoints dynamically
    
- No DNS requirement inside mesh
    
- Load balancing is determined by:
    
    - locality
        
    - subset
        
    - weights
        
    - health checks
        
    - failover policies
        

---

## **15.5.2 Example: VirtualService Routing**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: checkout
spec:
  hosts:
  - checkout.internal
  http:
  - route:
    - destination:
        host: checkout
        subset: v1
```

DNS resolves `checkout.internal` only once; Envoy handles all future changes.

---

## **15.5.3 Example: DestinationRule with Endpoints**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: DestinationRule
metadata:
  name: checkout-dr
spec:
  host: checkout
  subsets:
  - name: v1
    labels:
      version: v1
  trafficPolicy:
    loadBalancer:
      simple: ROUND_ROBIN
```

Envoy auto-discovers:

- pod IPs
    
- new endpoints
    
- health statuses
    

---

## **15.5.4 Using Mesh Multi-Cluster Discovery**

Istio supports multi-cluster service discovery:

```
Cluster A + Cluster B  
→ share identity  
→ share service registry  
→ Envoy picks local region first (locality-aware LB)
```

---

## **15.5.5 When to Use Mesh Discovery vs DNS**

|Scenario|Recommended|
|---|---|
|Internal microservice calls|**Mesh**|
|External client calls|**DNS**|
|Inter-cluster service discovery|**Mesh**|
|Inter-region internet services|**DNS**|
|Private service access|**DNS + PSC**|

---

## **15.5.6 Common Pitfalls**

- Relying on DNS for east–west service discovery → latency spikes.
    
- Missing Envoy locality settings → cross-region traffic.
    
- Forgetting to align service names across clusters.
    
- Using mesh-to-DNS bridges incorrectly → resolution loops.
    

---

# **Chapter 16 — Networking Failure Modes**

_(Expanded with senior-level clarity, diagrams, commands, troubleshooting steps, and practical mitigation patterns.)_

Networking failures are often subtle, hard to diagnose, and easy to introduce during infrastructure changes. This chapter covers the most common and impactful networking failure modes in cloud and hybrid architectures—why they happen, how to detect them, and how to prevent them.

---

# **16.1 Overlapping CIDRs**

Overlapping CIDRs occur when two networks use the same IP ranges in ways that break routing, NAT, VPN tunnels, or VPC peering.

---

## **16.1.1 Why Overlapping CIDRs Cause Failures**

Routing depends on deterministic prefix matches:

- If two networks advertise `10.0.0.0/16`, traffic **cannot be unambiguously routed**.
    
- BGP will reject route advertisements with overlapping CIDRs.
    
- VPC peering refuses to establish the connection.
    
- VPN tunnels may come up, but traffic silently blackholes.
    

---

## **16.1.2 Typical Overlap Scenarios**

### **Scenario A — On-Prem and GCP Both Use `10.0.0.0/16`**

```
On-Prem: 10.0.0.0/16
GCP Nodes: 10.0.0.0/18
```

→ BGP rejects routes  
→ VPN establishes but packets cannot be routed

---

### **Scenario B — Two GKE Clusters with Same Pod CIDR**

```
Cluster A Pod CIDR: 10.0.64.0/18
Cluster B Pod CIDR: 10.0.64.0/18
```

→ Multi-cluster service discovery fails  
→ Traffic intended for Cluster B lands in Cluster A

---

### **Scenario C — PSC Range Overlaps Node Range**

```
PSC Range:   10.0.128.0/20
Node Range:  10.0.128.0/18
```

→ PSC endpoints unreachable  
→ Cloud NAT refuses to allocate ports

---

## **16.1.3 Example Detection**

Inside GCP:

```bash
ip route
```

If you see two identical prefixes pointing to different next-hops → conflict.

On Cloud Router:

```bash
gcloud compute routers get-status prod-router \
  --region=us-central1
```

Look for:

```
status: REJECTED
reason: PREFIX_CONFLICT
```

---

## **16.1.4 Resolution Strategies**

- Reassign unique CIDRs by environment, region, or purpose.
    
- Use NAT to map overlapping CIDRs.
    
- Redesign VPC peering or remove peering entirely.
    
- Re-IP clusters or node pools (painful, but sometimes required).
    

---

## **16.1.5 Common Pitfalls**

- Assuming `/8` ranges are harmless → recipe for overlap.
    
- Copying on-prem addressing straight into cloud.
    
- Forgetting that **Pod CIDRs must be unique across clusters**.
    
- Overlapping PSC ranges producing obscure errors.
    

---

# **16.2 Route Leaks**

A route leak happens when a network unintentionally advertises routes it shouldn't—creating incorrect traffic paths or routing loops.

---

## **16.2.1 What Causes Route Leaks**

- Incorrect BGP export policies
    
- Overly broad route announcements
    
- Using static routes that override subnet routes
    
- Cloud Router learning routes from on-prem that conflict with GCP CIDRs
    

---

## **16.2.2 Typical Leak Scenario**

### **Scenario: On-Prem Advertises Default Route (`0.0.0.0/0`)**

```
On-Prem → advertises → 0.0.0.0/0
```

→ All outbound cloud traffic goes through on-prem  
→ NAT overloads on-prem firewall  
→ High latency  
→ Outages under load

This behavior is extremely common and dangerous.

---

## **16.2.3 Example: Detecting Route Leaks**

On Cloud Router:

```bash
gcloud compute routers get-status prod-router \
  --region=us-central1
```

Look for:

```
learnedRoutes:
- prefix: 0.0.0.0/0
  nextHop: bgpPeerA
```

If you didn’t intend this → you have a leak.

---

## **16.2.4 Fixing Route Leaks**

### **Option A — On-Prem Prevents Advertising Default Route**

Configure on-prem router:

```
no network 0.0.0.0/0
```

### **Option B — Apply Cloud Router Route Filters**

Example: Deny default route

```bash
gcloud compute routers update-bgp-peer prod-router \
  --region=us-central1 \
  --peer-name=onprem-peer \
  --set-advertisement-groups=ALL_SUBNETS \
  --set-advertisement-filter=DENY_DEFAULT_ROUTE
```

---

## **16.2.5 Common Pitfalls**

- Accepting default routes from partners by accident.
    
- Using overly broad static routes with priority <1000.
    
- Forgetting Cloud Router propagates learned routes globally.
    
- Multi-region route amplification causing unexpected routing.
    

---

# **16.3 Hairpinning**

Hairpinning occurs when traffic leaves a virtual network and loops back in unnecessarily, causing extra latency, costs, or complete failure.

---

## **16.3.1 What Is Hairpinning?**

Traffic path looks like this:

```
Pod A → Internal LB → Public IP → Google Edge → Back to VPC → Pod B
```

Instead of:

```
Pod A → Pod B
```

---

## **16.3.2 Why Hairpinning Happens**

- Clients use **public DNS records** inside the network.
    
- Load balancers resolve to external IPs only.
    
- NAT configurations force all outbound traffic through egress nodes.
    
- Split-horizon DNS not configured properly.
    

---

## **16.3.3 Example Scenario**

Internal Pod calls:

```
https://api.example.com
```

But DNS resolves to:

```
34.x.x.x (public Load Balancer IP)
```

Traffic leaves the region → edge POP → returns to region → hits backend service.

This increases:

- Latency
    
- Egress cost
    
- Load on LB
    

---

## **16.3.4 Fix With Internal Load Balancers + Private DNS**

### Step 1 — Create Internal Load Balancer

```bash
gcloud compute forwarding-rules create api-ilb \
  --region=us-central1 \
  --load-balancing-scheme=INTERNAL_MANAGED \
  --backend-service=api-backend \
  --network=prod-vpc \
  --subnet=prod-nodes-subnet
```

### Step 2 — Create private DNS record

```
api.example.com A 10.0.10.5
```

### Step 3 — Ensure split-horizon DNS

Clients inside VPC → internal LB  
Clients outside → public LB

---

## **16.3.5 Detection**

From inside a pod:

```bash
dig api.example.com
curl -v https://api.example.com
```

If traffic jumps to external IP → hairpin detected.

---

## **16.3.6 Common Pitfalls**

- Forgetting to override DNS internally.
    
- Using public Cloud Run URLs internally → hairpin every call.
    
- GKE using node-local DNS but upstream resolvers misconfigured.
    
- Hybrid networks accidentally introducing NAT loops.
    

---

# **16.4 Misconfigured NAT**

Cloud NAT enables outbound internet access for resources without external IPs. Misconfiguration causes service outages, blocked API calls, and image pull failures.

---

## **16.4.1 NAT Failure Modes**

### **1. No NAT Gateway Assigned**

Nodes attempt outbound traffic but NAT isn’t configured.

Symptoms:

- Pods cannot reach public APIs
    
- Instance metadata works but internet doesn’t
    
- Pulling container images fails
    

---

### **2. NAT Exhaustion**

Each NAT gateway has:

- Port limits
    
- Connection limits
    
- Throughput constraints
    

Symptoms:

- Random packet drops
    
- HTTP 5xx during high outbound QPS
    
- Intermittent DNS resolution failures
    

---

### **3. Using NAT for Private Google Access (PGA)**

Incorrect: PGA → NOT NAT.

If NAT is required for access to Google APIs → misconfiguration.

---

## **16.4.2 Example: Creating NAT Correctly**

### Step 1 — Cloud Router

```bash
gcloud compute routers create prod-router \
  --network=prod-vpc \
  --region=us-central1
```

### Step 2 — Create NAT Gateway

```bash
gcloud compute routers nats create prod-nat \
  --router=prod-router \
  --region=us-central1 \
  --nat-all-subnet-ip-ranges \
  --auto-allocate-nat-external-ips
```

---

## **16.4.3 NAT Logging**

Enable full NAT logs to diagnose issues:

```bash
gcloud compute routers nats update prod-nat \
  --router=prod-router \
  --region=us-central1 \
  --enable-logging \
  --log-level=DEBUG
```

---

## **16.4.4 NAT Troubleshooting (Practical)**

Check NAT translations:

```bash
gcloud compute routers nats list \
  --router=prod-router \
  --region=us-central1
```

Inside Pod:

```bash
curl ifconfig.me
```

If response is:

- **NAT IP** → success
    
- **No response** → NAT blocked
    
- **Node external IP** → NAT not used
    

---

## **16.4.5 Common Pitfalls**

- Not using `--nat-all-subnet-ip-ranges` → some subnets left without egress.
    
- PSC ranges being NATed incorrectly.
    
- Serverless VPC connectors requiring separate NAT.
    
- NAT competing with VPN priorities (default routes misconfigured).
    

---

# **16.5 Network Security Anti-Patterns**

Misconfigured network security can lead to outages, unauthorized access, or unintended exposure.

---

## **16.5.1 Anti-Pattern 1 — Open Ingress Rules**

Example of a dangerous rule:

```bash
gcloud compute firewall-rules create allow-all \
  --allow=tcp:0-65535 \
  --source-ranges=0.0.0.0/0
```

Impact:

- Entire VPC exposed
    
- Attackers can probe services
    
- Violates zero-trust principles
    

---

## **16.5.2 Anti-Pattern 2 — Relying Solely on IP-Based Rules**

Better alternative:

- Use service accounts
    
- Use identity-based policies
    
- Use tags or workload identity
    

IP-based rules often break during autoscaling or cluster upgrades.

---

## **16.5.3 Anti-Pattern 3 — Allowing Egress to 0.0.0.0/0 by Default**

This leads to:

- Data exfiltration risk
    
- Calls to unintended public endpoints
    
- Difficulty auditing traffic flows
    

Better:

- Use hierarchical firewall policies
    
- Restrict by destination
    
- Allow only known CIDRs
    

---

## **16.5.4 Anti-Pattern 4 — Missing mTLS for East–West Traffic**

Without mTLS:

- Attackers can perform lateral movement
    
- Internal service calls are not authenticated
    
- Mesh telemetry lacks identity information
    

Use mesh-level certificates—or strict mode for Istio:

```yaml
apiVersion: security.istio.io/v1beta1
kind: PeerAuthentication
metadata:
  name: default
spec:
  mtls:
    mode: STRICT
```

---

## **16.5.5 Anti-Pattern 5 — No Egress Control for Sensitive Workloads**

Example:  
A billing service calling arbitrary public APIs.

Fix:

- Use egress gateways
    
- Allow-list specific domains
    
- Use VPC-SC perimeters for GCP API access
    

---

## **16.5.6 Anti-Pattern 6 — Overlapping Policies Between Org, Folder, and Project**

This causes:

- Unexpected deny rules
    
- Confusing troubleshooting
    
- Inconsistent security posture
    

Use:

- Naming conventions
    
- Policy versioning
    
- Automated tests for firewall changes
    

---

## **16.5.7 Common Pitfalls**

- Firewall deny rules silently overriding allow rules.
    
- Egress allowed broadly due to misaligned priorities.
    
- Not testing firewall changes → outages.
    
- Not enforcing mTLS → insecure internal environment.
    
- PSC endpoints exposed via incorrect IAM controls.
    

---

# **Chapter 17 — GKE Cluster Internals, Node Pools, and Autoscaling**

_(Expanded with senior-level depth, diagrams, commands, YAML examples, and troubleshooting patterns.)_

This chapter explains how GKE’s control plane works internally, how to design node pools for performance, security, and cost efficiency, how all three autoscaling mechanisms (HPA, VPA, CA) interact, and how to safely handle node upgrades without disrupting workloads.

---

# **17.1 Control Plane Internals**

GKE is a managed Kubernetes control plane—Google operates the masters, etcd, API server, and scheduling layers. Understanding how this system behaves under load is essential for troubleshooting latency, scheduling delays, and cluster instability.

---

## **17.1.1 Control Plane Architecture**

```
 ┌─────────────────────────────┐
 │      GKE Control Plane      │
 │  (Google-managed, regional) │
 └─────────────┬───────────────┘
               │
     API Calls, PodScheduling
               │
 ┌─────────────┴───────────────┐
 │        Node Pools            │
 │   (VMs running kubelet)     │
 └──────────────────────────────┘
```

### Control Plane Components:

- **API Server** – entrypoint for all cluster operations
    
- **etcd** – persistent store for cluster state
    
- **Scheduler** – assigns pods to nodes
    
- **Controller Manager** – runs controllers (ReplicaSet, Deployment, etc.)
    
- **Cloud Controller Manager (CCM)** – GCP-specific integrations (LBs, routes, disks)
    

---

## **17.1.2 Regional Control Planes**

A regional GKE cluster spreads control-plane replicas across three zones:

```
Zone A: API server + etcd shard
Zone B: API server + etcd shard
Zone C: API server + etcd shard
```

Benefits:

- Survives single-zone failures
    
- Zero-downtime control-plane upgrades
    
- Higher availability for API operations
    

---

## **17.1.3 Control Plane Performance Characteristics**

- **API Server QPS Limits** per node and per service account
    
- **Scheduler Prioritization** based on:
    
    - node taints/tolerations
        
    - pod resource requests
        
    - pod anti-affinity
        
- **etcd Latency Under Load** affects:
    
    - Deployment progress
        
    - HPA scaling
        
    - Endpoint registration
        

---

## **17.1.4 Useful Debug Commands**

### Check control plane events

```bash
kubectl get events --sort-by='.lastTimestamp'
```

### Check scheduler performance

```bash
kubectl get --raw '/metrics' | grep scheduler
```

### Check API server QPS quota

```bash
gcloud container clusters describe my-cluster \
  --region=us-central1 | grep -i qps
```

---

## **17.1.5 Common Pitfalls**

- **Overloading control plane** with massive Deployment objects
    
- Excessive pod churn → scheduler saturation
    
- Overusing CustomResourceDefinitions with heavy controllers
    
- Too many ingress resources → CCM bottleneck
    
- API server QPS throttling → cascading delays
    

---

# **17.2 Node Pool Design**

Node pools represent groups of nodes with identical configuration. Proper design ensures isolation, security, and performance.

---

## **17.2.1 Why Multiple Node Pools Matter**

Use separate node pools for:

- Workload isolation
    
- Security boundary separation
    
- Resource consistency
    
- Different machine types (CPU-optimized vs memory-optimized)
    
- Spot/Preemptible workloads
    
- GPU workloads
    
- System daemons
    

---

## **17.2.2 Node Pool Architecture Example**

```
Cluster
 ├── system-pool (GKE system pods)
 ├── baseline-pool (default services)
 ├── compute-pool (general workloads)
 ├── memory-pool (memory-heavy services)
 └── spot-pool (preemptible workers)
```

---

## **17.2.3 Creating Node Pools**

### Example: Standard Node Pool

```bash
gcloud container node-pools create compute-pool \
  --cluster=prod \
  --region=us-central1 \
  --machine-type=n2-standard-4 \
  --num-nodes=3
```

### Example: Preemptible Node Pool

```bash
gcloud container node-pools create spot-pool \
  --cluster=prod \
  --region=us-central1 \
  --machine-type=e2-standard-4 \
  --num-nodes=0 \
  --enable-autoscaling \
  --max-nodes=20 \
  --spot
```

---

## **17.2.4 Node Taints & Tolerations**

Ensure workloads land in correct pools.

### Example: Taint Spot Nodes

```bash
kubectl taint nodes pool=spot-pool spot=true:NoSchedule
```

### Pods need toleration:

```yaml
tolerations:
- key: "spot"
  operator: "Equal"
  value: "true"
  effect: "NoSchedule"
```

---

## **17.2.5 Optimizing Node Pools for GKE Autopilot vs Standard**

### Standard:

- You control nodes
    
- Best for custom workloads with low-level tuning
    

### Autopilot:

- Google manages nodes completely
    
- Predictable cost per pod
    
- No node pools to configure
    
- Good for multi-tenant SaaS
    

---

## **17.2.6 Common Pitfalls**

- Too few node pools → noisy-neighbor issues
    
- Too many node pools → Cluster Autoscaler inefficiency
    
- Mixing system and workload pods in same pool
    
- Not pinning critical services to non-preemptible pools
    
- Pods failing due to incorrect taints/tolerations
    

---

# **17.3 Autoscaling (HPA, VPA, CA)**

There are **three** autoscaling mechanisms in GKE. Senior engineers must understand how they interact.

---

# **17.3.1 Horizontal Pod Autoscaler (HPA)**

HPA scales the **number of pods**.

### Common Metrics:

- CPU utilization
    
- Memory (via custom metrics)
    
- Custom application metrics
    

### Example HPA:

```yaml
apiVersion: autoscaling/v2
kind: HorizontalPodAutoscaler
metadata:
  name: api-hpa
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: api
  minReplicas: 3
  maxReplicas: 20
  metrics:
  - type: Resource
    resource:
      name: cpu
      target:
        type: Utilization
        averageUtilization: 70
```

---

## **17.3.2 Vertical Pod Autoscaler (VPA)**

VPA adjusts **resource requests/limits** for pods.

Modes:

- Off
    
- Initial
    
- Auto (risky in production)
    

### Safer Example — Recommendation Only

```yaml
apiVersion: autoscaling.k8s.io/v1
kind: VerticalPodAutoscaler
metadata:
  name: api-vpa
spec:
  targetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: api
  updatePolicy:
    updateMode: "Off"
```

---

## **17.3.3 Cluster Autoscaler (CA)**

CA scales **node pools**.

Triggers:

- Pending pods with unschedulable resource requirements
    
- Node utilization (in some cases)
    

### Enable CA:

```bash
gcloud container node-pools update compute-pool \
  --cluster=prod \
  --region=us-central1 \
  --enable-autoscaling \
  --min-nodes=3 \
  --max-nodes=30
```

---

## **17.3.4 Interaction Between Autoscalers**

|Scenario|Impact|
|---|---|
|HPA scales pods → CA adds nodes|Very common|
|VPA increases requests → pods no longer fit|CA must scale node pool|
|CA removes nodes → VPA/HPA re-evaluate|Graceful scaling|
|VPA Auto mode + HPA → unpredictable scaling|Avoid in production|

---

## **17.3.5 Autoscaling Anti-Patterns**

- HPA threshold too low → thrashing
    
- VPA Auto mode → pods constantly restarted
    
- CA max nodes too small → pending pods forever
    
- Node pools too fragmented → CA cannot bin-pack
    
- Spot-only clusters → large-scale pod eviction
    

---

# **17.4 Node Upgrades & Surge Control**

Node upgrades replace old nodes with new ones using **Surge Upgrades** or **Blue/Green** patterns. Done incorrectly, they cause outages or cascading pod failures.

---

## **17.4.1 How GKE Node Upgrades Work**

Upgrade flow:

1. New node created
    
2. Pods drained from old node
    
3. Old node deleted
    
4. Repeat per node
    

GKE uses **surge parameters** to control concurrency.

---

## **17.4.2 Configuring Surge Upgrades**

```bash
gcloud container node-pools update compute-pool \
  --cluster=prod \
  --region=us-central1 \
  --max-surge-upgrade=2 \
  --max-unavailable-upgrade=0
```

### Best Practices

- Set `max-unavailable=0` for critical workloads
    
- Use `max-surge > 0` to maintain capacity during upgrades
    

---

## **17.4.3 PodDisruptionBudgets (PDBs)**

PDBs protect workloads during node upgrades.

### Example PDB:

```yaml
apiVersion: policy/v1
kind: PodDisruptionBudget
metadata:
  name: api-pdb
spec:
  minAvailable: 80%
  selector:
    matchLabels:
      app: api
```

---

## **17.4.4 Drain-Proofing Your Workloads**

Use:

- Readiness probes
    
- Graceful shutdown hooks
    
- Connection draining
    
- Proper timeouts
    

### Example Readiness Probe

```yaml
readinessProbe:
  httpGet:
    path: /healthz
    port: 8080
  periodSeconds: 3
```

---

## **17.4.5 Safe Upgrade Strategy**

### Strategy:

1. Upgrade system node pools first
    
2. Upgrade workload node pools gradually
    
3. Ensure HPA has enough headroom
    
4. Respect PDBs
    
5. Monitor:
    
    - Pod churn
        
    - Scheduling latency
        
    - Control-plane logs
        

---

## **17.4.6 Common Pitfalls**

- Node upgrades violating PDB → workloads unavailable
    
- Too small surge → long upgrade windows
    
- Workload not implementing graceful shutdown → request failures
    
- Using VPA Auto mode during upgrades → multiple restarts
    
- Spot nodes draining en masse → cascading failures
    
- CA shrinking node pools during upgrades → deadlock
    

---

# **Chapter 18 — Pod Lifecycle, Scheduling & Resource Engineering**

_(Expanded with senior-level clarity, deep Kubernetes internals, diagrams, scheduling examples, and tuning best practices.)_

This chapter explains the full lifecycle of a Pod, how the scheduler decides placement, how to correctly specify resource requests/limits, and how quotas and LimitRanges enforce multi-tenant safety.

---

# **18.1 Pod Lifecycle States**

Kubernetes Pods move through predictable lifecycle phases. Understanding these states is essential for diagnosing scheduling delays, restart loops, and readiness failures.

---

## **18.1.1 Pod Lifecycle Diagram**

```
            Pod Created
                  │
         Pending (waiting for scheduling)
                  │
          Scheduled to a Node
                  │
         Container Creating
                  │
              Running
                  │
       ┌──────────┴───────────┐
       │                      │
  Succeeded (Exit 0)     Failed / CrashLoop
```

---

## **18.1.2 States Explained**

### **1. Pending**

Pod exists but:

- scheduler hasn’t selected a node
    
- OR node doesn’t have required resources
    
- OR PVCs not bound yet
    
- OR image pull secret missing
    

Check:

```bash
kubectl describe pod <pod>
```

---

### **2. ContainerCreating**

- kubelet is creating containers
    
- pulling images
    
- mounting volumes
    
- injecting secrets
    

Common issues:

- imagePullBackOff
    
- volume mount failures
    

---

### **3. Running**

All containers started and passing readiness checks.

Check readiness:

```bash
kubectl get pod <pod> -o jsonpath='{.status.conditions[?(@.type=="Ready")].status}'
```

---

### **4. Succeeded**

Pod finished normally.

### **5. Failed**

Non-zero exit or failed init container.

### **6. CrashLoopBackOff**

Container repeatedly exits quickly.

Fix:

- misconfigured command/entrypoint
    
- missing dependencies
    
- readiness misconfigurations preventing stable start
    

---

## **18.1.3 Init Containers**

Init containers run **in order**, one at a time, before main containers.

Typical uses:

- Waiting for dependencies
    
- Migrations
    
- Pre-warming caches
    
- Validating config
    

### Example:

```yaml
initContainers:
- name: wait-for-db
  image: busybox
  command: ['sh', '-c', 'until nc -z db 5432; do sleep 1; done']
```

---

## **18.1.4 Probes Overview**

### **Liveness Probe**

Restarts the container if unhealthy.

### **Readiness Probe**

Controls if pod receives traffic.

### **Startup Probe**

Used for slow-starting apps (Java, DB proxies).

### Example:

```yaml
livenessProbe:
  httpGet: { path: /healthz, port: 8080 }
readinessProbe:
  httpGet: { path: /ready, port: 8080 }
startupProbe:
  httpGet: { path: /init, port: 8080 }
  failureThreshold: 30
  periodSeconds: 5
```

---

## **18.1.5 Common Pitfalls**

- Readiness probes failing → zero traffic
    
- Liveness probe too aggressive → restart loops
    
- Init containers never complete → stuck Pending
    
- Images too large → long pull times, node pressure events
    

---

# **18.2 Scheduling Features (Affinity, Taints, Priorities)**

The Kubernetes scheduler decides where to place Pods based on constraints and scoring rules.

---

# **18.2.1 Node Selectors**

Basic scheduling:

```yaml
nodeSelector:
  workload: cpu-heavy
```

Very strict: if no nodes match → Pod stays Pending.

---

# **18.2.2 Affinity & Anti-Affinity**

### **Node Affinity**

Soft or hard rules based on labels.

```yaml
affinity:
  nodeAffinity:
    requiredDuringSchedulingIgnoredDuringExecution:
      nodeSelectorTerms:
      - matchExpressions:
        - key: workload
          operator: In
          values: ["compute"]
```

---

### **Pod Anti-Affinity**

Avoid co-locating pods to prevent noisy neighbors.

```yaml
podAntiAffinity:
  requiredDuringSchedulingIgnoredDuringExecution:
  - labelSelector:
      matchLabels:
        app: payments
    topologyKey: kubernetes.io/hostname
```

This ensures **one pod per node**.

---

# **18.2.3 Taints & Tolerations**

Use taints to repel pods from nodes.

### Taint a node:

```bash
kubectl taint nodes gke-node-1 dedicated=payments:NoSchedule
```

### Allow pods via toleration:

```yaml
tolerations:
- key: "dedicated"
  operator: "Equal"
  value: "payments"
  effect: "NoSchedule"
```

---

# **18.2.4 Priority Classes**

Ensure critical workloads preempt lower-priority pods during resource shortages.

### Create PriorityClass:

```yaml
apiVersion: scheduling.k8s.io/v1
kind: PriorityClass
metadata:
  name: critical-workload
value: 1000000
globalDefault: false
description: "Preempt lower-priority pods."
```

### Assign to Pod:

```yaml
priorityClassName: critical-workload
```

---

# **18.2.5 Common Scheduling Pitfalls**

- Overusing hard affinity → unschedulable pods
    
- Large nodeSelector matrices → bin-packing failures
    
- Insufficient tolerations for tainted pools
    
- PriorityClass misconfig → critical workloads evict important services
    
- Anti-affinity across zones → capacity starvation
    

---

# **18.3 Resource Requests & Limits**

Correct resource specification is the backbone of stable GKE operations.

---

## **18.3.1 Requests vs Limits**

- **Request** = guaranteed minimum
    
- **Limit** = enforced maximum
    

Scheduling is based on **requests**, not limits.

---

## **18.3.2 CPU Request/Limit Example**

```yaml
resources:
  requests:
    cpu: "500m"
    memory: "512Mi"
  limits:
    cpu: "1"
    memory: "1Gi"
```

---

## **18.3.3 Memory Behavior**

If a container exceeds its **memory limit**:

- It is OOMKilled immediately.
    

If memory **request** > node available:

- Pod stays Pending.
    

---

## **18.3.4 CPU Behavior**

If CPU limit reached:

- Container throttled, not killed.
    

If CPU request too high:

- Scheduler delays placement.
    

---

## **18.3.5 Resource Engineering Best Practices**

- Use VPA recommendation mode for baselining
    
- Set CPU limits = 2x requests (for bursty workloads)
    
- Set memory requests ≈ 70–90% of actual usage
    
- Avoid setting memory limits too close to requests
    
- Consider limitless CPU for low-priority workloads (in some clusters)
    

---

## **18.3.6 Troubleshooting Resource Issues**

Check pod resource usage:

```bash
kubectl top pod <name>
```

Check OOM events:

```bash
kubectl describe pod <name> | grep -i oom
```

Node pressure events:

```bash
kubectl describe node <node> | grep -i "memory pressure"
```

---

## **18.3.7 Common Pitfalls**

- Setting CPU=0.1 request for production API → latency spikes
    
- Too low memory → OOM kills during bursts
    
- Too high request → bin-packing fails → expensive nodes
    
- Inconsistent resource governance → unpredictable autoscaling
    

---

# **18.4 Vertical & Horizontal Scaling**

Autoscaling includes:

- HPA (Horizontal Scaling)
    
- VPA (Vertical Scaling)
    
- CA (Cluster Autoscaler)
    

This section focuses on Pod-level scaling.

---

# **18.4.1 Horizontal Scaling (HPA)**

HPA adjusts **replica counts**.

### Example:

```yaml
apiVersion: autoscaling/v2
kind: HorizontalPodAutoscaler
metadata:
  name: checkout-hpa
spec:
  minReplicas: 3
  maxReplicas: 30
  metrics:
  - type: Resource
    resource:
      name: cpu
      target:
        type: Utilization
        averageUtilization: 75
```

---

# **18.4.2 Vertical Scaling (VPA)**

VPA adjusts **resource sizes** per pod.

### Example (Recommendation Mode):

```yaml
apiVersion: autoscaling.k8s.io/v1
kind: VerticalPodAutoscaler
metadata:
  name: checkout-vpa
spec:
  updatePolicy:
    updateMode: "Off"
```

---

# **18.4.3 HPA + VPA Design Models**

### **Anti-pattern**

HPA + VPA in auto mode  
→ Both compete and cause thrashing

### **Recommended**

- HPA for replicas
    
- VPA for initial recommendations only
    
- No automatic VPA in production
    

---

# **18.4.4 Autoscaling Troubleshooting**

### Pods not scaling?

Check HPA events:

```bash
kubectl describe hpa checkout-hpa
```

### Nodes not scaling?

Check Cluster Autoscaler logs:

```bash
kubectl -n kube-system logs deployment/cluster-autoscaler
```

---

# **18.4.5 Common Pitfalls**

- Scaling based only on CPU for I/O-bound workloads
    
- HPA too aggressive → scaling storms
    
- VPA in Auto mode restarting pods continuously
    
- CA blocked by PDBs (unschedulable)
    

---

# **18.5 Quotas & LimitRanges**

Quotas and LimitRanges control resource usage at the namespace level.

---

# **18.5.1 ResourceQuota**

Enforces maximum resource usage.

### Example:

```yaml
apiVersion: v1
kind: ResourceQuota
metadata:
  name: team-a-quota
spec:
  hard:
    requests.cpu: "20"
    requests.memory: "100Gi"
    limits.cpu: "40"
    limits.memory: "200Gi"
    pods: "200"
```

---

# **18.5.2 LimitRange**

Defines default requests/limits per container.

### Example:

```yaml
apiVersion: v1
kind: LimitRange
metadata:
  name: default-limits
spec:
  limits:
  - type: Container
    default:
      cpu: "500m"
      memory: "512Mi"
    defaultRequest:
      cpu: "200m"
      memory: "256Mi"
```

---

# **18.5.3 Why LimitRanges Matter**

- Prevents pods from being created without resource requests
    
- Enforces minimum sizes for workloads
    
- Supports fair multi-tenant cluster usage
    
- Enables predictable autoscaling
    

---

# **18.5.4 Quota & LimitRange Troubleshooting**

Check if a namespace has quota violations:

```bash
kubectl describe quota -n team-a
```

Pods pending due to missing LimitRange:

```
Error: failed to create pod: must specify requests.memory
```

---

# **18.5.5 Common Pitfalls**

- Missing LimitRange → pods default to no limits → cluster instability
    
- Quotas blocking deployments silently
    
- Overly restrictive quotas → HPA can’t scale
    
- Quotas applied before autoscaling strategy finalized
    

---

# **Chapter 19 — GKE Networking: CNI, Services, Ingress & NEGs**

_(Expanded with senior-level clarity, practical examples, commands, diagrams, and pitfall analysis.)_

GKE networking combines Kubernetes-native abstractions with Google Cloud–specific features such as VPC-native Pod IP allocation, Internal/External Load Balancers, and Network Endpoint Groups (NEGs). Understanding these layers is essential for designing scalable, low-latency, production-grade service traffic flows.

---

# **19.1 CNI Options & Pod CIDRs**

GKE supports multiple Container Network Interface (CNI) implementations. The CNI controls **Pod IP allocation**, **routing**, and **network policy enforcement**.

---

## **19.1.1 CNI Models in GKE**

### **1. GKE VPC-Native (Recommended)**

Default and recommended for 99% of environments.

Characteristics:

- Pod IPs come from **VPC secondary ranges**
    
- Pods are **first-class VPC citizens**
    
- No overlay networking
    
- Best performance
    
- Supports **Native L7 Internal Load Balancing**
    
- Required for **multi-NIC** and **Dataplane V2**
    

---

### **2. GKE Dataplane V2 (eBPF)**

Enhanced VPC-native mode using eBPF.

Benefits:

- Faster networking
    
- More accurate network policy
    
- Lower memory overhead than iptables
    
- Better scalability
    

Enable during cluster creation:

```bash
gcloud container clusters create prod \
  --region=us-central1 \
  --enable-dataplane-v2
```

---

### **3. Kubernetes Routing (Legacy)**

Deprecated.  
Uses routes instead of VPC secondary ranges.  
Avoid for new deployments.

---

## **19.1.2 Pod CIDRs & IP Planning**

Each cluster requires:

- **Node CIDR** → primary range
    
- **Pod CIDR** → secondary range (typically `/14`–`/16`)
    
- **Service CIDR** → internal IP-only network
    

Example CIDR planning:

```
VPC: 10.0.0.0/16
Node range: 10.0.0.0/20
Pod range: 10.0.16.0/14
Service range: 172.16.0.0/20
```

---

## **19.1.3 Checking Pod CIDRs**

```bash
kubectl get nodes -o wide
```

Look for:

```
INTERNAL-IP    POD-CIDR
```

---

## **19.1.4 Common Pitfalls**

- Using Pod CIDRs too small → IP exhaustion under HPA spikes
    
- Overlapping Pod CIDRs across clusters → multi-cluster routing failures
    
- Forgetting Service CIDR must NOT overlap Pod/Node ranges
    
- Choosing non-VPC-native mode → breaks NEGs and certain ILB features
    

---

# **19.2 NodePorts & LoadBalancers**

Kubernetes Services expose workloads at different layers. GKE maps these to Google Cloud Load Balancers.

---

## **19.2.1 NodePort Service**

Exposes a Service on each node via a port (30000–32767).

### Example:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: api-nodeport
spec:
  type: NodePort
  selector:
    app: api
  ports:
  - port: 80
    targetPort: 8080
    nodePort: 31000
```

Drawbacks:

- Exposes traffic on every node
    
- No health checking at LB layer
    
- Not suitable for production outside niche cases
    

---

## **19.2.2 LoadBalancer Service**

Creates a Cloud Load Balancer (external or internal).

### Example:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: api-lb
spec:
  type: LoadBalancer
  selector:
    app: api
  ports:
  - port: 80
    targetPort: 8080
```

GKE automatically creates:

- For external → Global or regional L4 LB (depending on mode)
    
- For internal → L4 ILB
    

---

## **19.2.3 Ingress vs LoadBalancer**

|Feature|LoadBalancer|Ingress|
|---|---|---|
|Layer|L4 TCP/UDP|L7 HTTP(S)|
|One LB per Service|Yes|No|
|Path-based routing|No|Yes|
|TLS termination|Sometimes|Yes|
|Host-based routing|No|Yes|
|NEGs support|Yes|Required|

---

## **19.2.4 Common Pitfalls**

- Using NodePort behind LB → unnecessary hop + cost
    
- Too many LoadBalancer Services → expensive + IP exhaustion
    
- Using L4 LB for L7 traffic → cannot do routing, TLS, rewrite rules
    

---

# **19.3 GKE Ingress Controller**

GKE supplies a managed controller that converts Kubernetes Ingress objects into **Google Cloud HTTP(S) Load Balancers**.

---

## **19.3.1 Basic Ingress Example**

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: api-ingress
  annotations:
    kubernetes.io/ingress.class: "gce"
spec:
  rules:
  - host: api.example.com
    http:
      paths:
      - path: /
        pathType: Prefix
        backend:
          service:
            name: api
            port:
              number: 80
```

Creates:

- A global HTTPS LB
    
- Single anycast IP
    
- Managed SSL certificates if using `ManagedCertificate` resource
    

---

## **19.3.2 Managed Certificates**

```yaml
apiVersion: networking.gke.io/v1
kind: ManagedCertificate
metadata:
  name: api-cert
spec:
  domains:
  - api.example.com
```

Attach via Ingress annotation:

```yaml
annotations:
  networking.gke.io/managed-certificates: api-cert
```

---

## **19.3.3 Multi-Backend Ingress**

Supports path-based routing:

```yaml
rules:
- http:
    paths:
    - path: /v1
      backend:
        service:
          name: api-v1
          port:
            number: 80
    - path: /v2
      backend:
        service:
          name: api-v2
          port:
            number: 80
```

---

## **19.3.4 Common Pitfalls**

- Creating too many Ingresses → LB explosion
    
- Forgetting NEG annotations → LB creates NodePort instead
    
- ManagedCertificate stuck in “Provisioning” due to DNS mismatch
    
- Using Ingress for gRPC without proper annotation
    

---

# **19.4 NEGs (Network Endpoint Groups)**

NEGs are Google Cloud constructs that represent **backends as IP:Port pairs**.

GKE supports NEGs for:

- L7 ingress
    
- Internal L4 LB
    
- Zonal NEGs
    
- Regional NEGs
    
- Serverless (Cloud Run / Cloud Functions)
    

---

# **19.4.1 NEG Types**

### **1. Zonal NEGs**

Each VM/pod is registered individually in a zone.

### **2. Regional NEGs**

Multi-zone load balancing backend.

### **3. L7 Ingress NEGs**

Used by HTTP(S) Load Balancers.

### **4. PSC NEGs**

Used to expose Private Service Connect endpoints.

---

## **19.4.2 Enabling NEGs for a Service**

Add annotation:

```yaml
metadata:
  annotations:
    cloud.google.com/neg: '{"ingress": true}'
```

Full example:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: api
  annotations:
    cloud.google.com/neg: '{"ingress": true}'
spec:
  selector:
    app: api
  ports:
    - port: 80
      targetPort: 8080
```

This:

- Creates a NEG per zone
    
- Registers each pod IP into the LB backend
    
- Enables faster failover and health checks
    

---

## **19.4.3 Standalone NEGs (L4 ILB)**

Example:

```yaml
metadata:
  annotations:
    cloud.google.com/neg: '{"exposed_ports": {"80":{}}}'
```

Creates NEGs without L7 Ingress dependency.

---

## **19.4.4 Checking NEGs**

```bash
gcloud compute network-endpoint-groups list
```

Check endpoints:

```bash
gcloud compute network-endpoint-groups list-network-endpoints NEG_NAME \
  --zone=us-central1-a
```

---

## **19.4.5 Common NEG Pitfalls**

- Missing selector → NEG empty, LB returns 502
    
- Pod readiness probes determine NEG health → misconfigs break LB
    
- Incorrect targetPort → traffic blackholes
    
- Missing firewall rules for health checks
    

Health check ranges (must allow):

```
130.211.0.0/22
35.191.0.0/16
```

---

# **19.5 Internal vs External LoadBalancing**

GKE supports both **external** and **internal** L4 and L7 load balancers.

---

# **19.5.1 External Load Balancers**

Used for:

- Public APIs
    
- Web frontends
    
- Multi-region distribution via global LB
    

Created via:

- Ingress
    
- Service type LoadBalancer
    

---

# **19.5.2 Internal Load Balancers (ILB)**

Internal L4 or L7 traffic inside VPC.

Used for:

- Microservices
    
- Inter-tier communication
    
- Hybrid workloads calling internal services
    

Example ILB:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: internal-api
  annotations:
    cloud.google.com/load-balancer-type: "Internal"
spec:
  type: LoadBalancer
  selector:
    app: api
  ports:
  - port: 80
    targetPort: 8080
```

---

# **19.5.3 Choosing Internal vs External**

|Use Case|LB Type|
|---|---|
|Public Internet traffic|External|
|Private microservices|Internal|
|Hybrid workloads|Internal|
|Multi-region routing|External (Global LB)|
|East–West within cluster|ClusterIP (preferred)|

---

# **19.5.4 Common Pitfalls**

- Exposing Services with public LBs accidentally
    
- ILB used but DNS points to public LB → hairpinning
    
- ClusterIP used for hybrid access → not routable
    
- Missing firewall rules block ILB health checks
    
- Using internal LB across VPCs (not supported)
    

---

# **Chapter 20 — Istio / Envoy Fundamentals**

_(Expanded with senior-level clarity, deep Envoy internals, xDS flows, security models, YAML examples, and troubleshooting guidance.)_

Istio provides a powerful service mesh built on top of Envoy proxies. This chapter explains its architecture, how the control plane and data plane interact, how configuration flows through xDS APIs, how identity & mTLS work, and how telemetry collection happens.

---

# **20.1 Control Plane Architecture**

Istio’s control plane programs and configures Envoy data-plane proxies. In modern Istio (1.6+), the control plane is consolidated mostly into **istiod**.

---

## **20.1.1 Control Plane Components**

### **istiod**

The all-in-one control-plane binary that includes:

- **Pilot** – configuration distribution (xDS)
    
- **Citadel** – certificate authority (mTLS, identity)
    
- **Galley** (deprecated) – config validation
    
- **Injector** – sidecar auto-injection
    
- **Validation Webhook** – ensures valid config before commit
    

---

## **20.1.2 Responsibilities of istiod**

|Function|Description|
|---|---|
|Service discovery|Syncs endpoints from Kubernetes|
|Config distribution|Pushes Envoy configuration via xDS|
|Certificate management|Issues and rotates mTLS certs|
|Sidecar injection|Mutates pod spec to include Envoy|
|Policy|Applies mesh policies and RBAC|
|Telemetry metadata|Sends metadata to proxies|

---

## **20.1.3 High-Level Architecture Diagram**

```
                 ┌───────────────┐
                 │    istiod     │
                 │ - Pilot       │
                 │ - Citadel     │
                 └───────┬───────┘
                         │ xDS over gRPC
                         │
        ┌────────────────┼────────────────┐
        │                │                │
   Envoy Proxy      Envoy Proxy      Envoy Proxy
 (Sidecar A)       (Sidecar B)       (Sidecar C)
```

---

## **20.1.4 Checking istiod Status**

```bash
kubectl -n istio-system get pods -l app=istiod
```

Check logs:

```bash
kubectl -n istio-system logs deployment/istiod
```

---

## **20.1.5 Common Pitfalls**

- Running too many istiod replicas without proper HPA → memory runaway
    
- High churn in Kubernetes endpoints → overwhelm Pilot → stale configs
    
- Misconfigured validation webhook → all deployments block
    

---

# **20.2 Data Plane: Sidecars & Proxies**

Envoy is the data plane for Istio. Each pod receives a **sidecar proxy** that intercepts all inbound and outbound traffic.

---

## **20.2.1 Sidecar Injection**

### Automatic injection:

Label namespace:

```bash
kubectl label namespace default istio-injection=enabled
```

Pods will include:

```yaml
containers:
- name: istio-proxy
  image: auto-managed-envoy
```

---

## **20.2.2 How Envoy Intercepts Traffic**

Using `iptables` rules:

- All outbound traffic redirected to Envoy
    
- All inbound traffic routed through Envoy
    
- Envoy enforces:
    
    - mTLS
        
    - routing rules
        
    - retries/timeouts
        
    - telemetry collection
        

---

## **20.2.3 Envoy Architecture Inside Pod**

```
 Pod
 ├── Application Container
 └── Envoy Sidecar
      ├── Listener (inbound)
      ├── Listener (outbound)
      ├── Filters (HTTP/TCP)
      └── Clusters (services/endpoints)
```

---

## **20.2.4 Debugging Sidecar**

### Check Envoy Config Dump

```bash
kubectl exec <pod> -c istio-proxy -- pilot-agent request GET config_dump
```

### Check stats:

```bash
kubectl exec <pod> -c istio-proxy -- curl localhost:15000/stats
```

### Check clusters/endpoints:

```bash
kubectl exec <pod> -c istio-proxy -- curl localhost:15000/clusters
```

---

## **20.2.5 Common Pitfalls**

- Application binding to `127.0.0.1` → Envoy cannot reach it
    
- Outbound calls bypassing Envoy due to hostNetworking
    
- Headless services need correct service entries
    
- Init containers failing because outbound blocked
    

---

# **20.3 xDS Protocol (ADS, LDS, RDS, EDS)**

xDS is Envoy’s dynamic configuration API. Istio uses **Aggregated Discovery Service (ADS)** to publish:

- **LDS**: Listener Discovery Service
    
- **RDS**: Route Discovery Service
    
- **CDS**: Cluster Discovery Service
    
- **EDS**: Endpoint Discovery Service
    
- **SDS**: Secret Discovery Service
    

---

## **20.3.1 ADS Flow Diagram**

```
Envoy → istiod: “I need configs”
istiod → Envoy: LDS, RDS, CDS, EDS
Envoy → istiod: ACK
```

Communication is via **gRPC stream**, persistent connection.

---

## **20.3.2 LDS (Listener Discovery Service)**

Listeners define:

- Ports Envoy listens on
    
- Filter chains (HTTP/TCP routing)
    
- Inbound vs outbound
    

```json
{
  "name": "0.0.0.0_8080",
  "address": "0.0.0.0",
  "port_value": 8080
}
```

---

## **20.3.3 RDS (Route Discovery Service)**

Defines routing rules.

Example in YAML (Istio VirtualService):

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: checkout
spec:
  hosts:
  - checkout
  http:
  - route:
    - destination:
        host: checkout
        subset: v2
      weight: 20
    - destination:
        host: checkout
        subset: v1
      weight: 80
```

Converted into RDS config pushed to Envoy.

---

## **20.3.4 CDS (Cluster Discovery Service)**

Represents upstream services.

Example cluster entry:

```
cluster:
  name: outbound|80||checkout.default.svc.cluster.local
```

---

## **20.3.5 EDS (Endpoint Discovery Service)**

Provides IP:Port pairs.

Example:

```
10.0.5.21:8080
10.0.5.22:8080
```

EDSes update dynamically as pods start/stop.

---

## **20.3.6 SDS (Secret Discovery Service)**

Handles:

- certificates
    
- private keys
    
- CA bundles
    

Used for mTLS. Rotates certs every 24 hours by default.

---

## **20.3.7 Common xDS Pitfalls**

- Too many updates → Envoy overwhelmed → config lag
    
- ADS push blocked by network policy
    
- Stale EDS entries if readiness probes misconfigured
    
- RDS fails due to VirtualService error → broken routing
    

---

# **20.4 Identity & mTLS (SPIFFE/SPIRE concepts)**

Istio uses a strong identity model based on **SPIFFE IDs**.

---

## **20.4.1 SPIFFE Identity Format**

```
spiffe://cluster.local/ns/<namespace>/sa/<service-account>
```

Example:

```
spiffe://cluster.local/ns/payments/sa/api-service
```

This identity is:

- Strongly bound to workload
    
- Verified through mTLS
    
- Managed by Citadel/istiod
    

---

## **20.4.2 Certificate Generation**

Each Envoy sidecar gets:

- leaf certificate
    
- private key
    
- CA certificate
    

Generated by Istio’s CA (Citadel) and delivered via **SDS**.

Inspect cert:

```bash
kubectl exec pod -c istio-proxy -- curl localhost:15000/certs
```

---

## **20.4.3 Enforcing Strict mTLS**

Mesh-wide:

```yaml
apiVersion: security.istio.io/v1beta1
kind: PeerAuthentication
metadata:
  name: default
spec:
  mtls:
    mode: STRICT
```

Namespace-level:

```bash
kubectl label namespace payments istio-injection=enabled \
  istio.io/rev=default
```

---

## **20.4.4 Authorization Policies (RBAC)**

Example: only “checkout” can call “payment”.

```yaml
apiVersion: security.istio.io/v1beta1
kind: AuthorizationPolicy
metadata:
  name: payments-allow
  namespace: payments
spec:
  rules:
  - from:
    - source:
        principals:
        - "spiffe://cluster.local/ns/checkout/sa/api-sa"
```

---

## **20.4.5 Common Identity & mTLS Pitfalls**

- Missing service account → unexpected SPIFFE ID
    
- mTLS STRICT mode enabled but legacy apps use plaintext
    
- Outbound traffic to external APIs requires Sidecar object
    
- Cert rotation failing due to clock skew
    

---

# **20.5 Telemetry v2 Pipeline**

Telemetry v2 replaces Mixer with **in-proxy telemetry collection** using Envoy filters.

---

## **20.5.1 Telemetry v2 Architecture**

```
Envoy → Prometheus
Envoy → Access Logs → FluentBit → Your backend
Envoy → Traces → OpenTelemetry Collector
```

Telemetry is generated by Envoy, not external mixer components.

---

## **20.5.2 Metrics Collection**

Prometheus scrapes:

- Envoy stats
    
- istiod metrics
    
- application metrics via scraping
    

### Example service monitor:

```yaml
apiVersion: monitoring.coreos.com/v1
kind: ServiceMonitor
metadata:
  name: istiod
spec:
  selector:
    matchLabels:
      app: istiod
  endpoints:
  - port: http-monitoring
```

---

## **20.5.3 Access Logging**

Envoy emits structured logs.

Enable access logs:

```yaml
apiVersion: telemetry.istio.io/v1alpha1
kind: Telemetry
metadata:
  name: default
spec:
  accessLogging:
    providers:
    - name: envoy
    filter:
      expression: "response.code >= 500"
```

Logs typically routed via:

- Fluent Bit
    
- Logstash
    
- Cloud Logging
    

---

## **20.5.4 Distributed Tracing**

Envoy emits trace spans.

Enable tracing:

```yaml
apiVersion: telemetry.istio.io/v1alpha1
kind: Telemetry
metadata:
  name: tracing
spec:
  tracing:
    providers:
    - name: jaeger
```

Supports:

- OpenTelemetry
    
- Zipkin
    
- Jaeger
    
- Stackdriver Trace
    

---

## **20.5.5 Common Telemetry Pitfalls**

- Prometheus scraping Envoy too frequently → CPU spike
    
- Missing sampling rate → overwhelming trace backend
    
- Envoy logs too verbose → expensive log ingestion
    
- Incorrect Telemetry CRDs → no metrics for some workloads
    

---

# **Chapter 21 — Traffic Management: Blue/Green, Canary, Failover**

_(Expanded with senior-level depth, real Istio examples, safe deployment patterns, and failover routing design.)_

Istio provides powerful L7 traffic management primitives that enable safe rollouts, progressive delivery, multi-region routing, controlled egress, and deterministic failover behaviors. This chapter explains how routing rules work, how to safely release new versions, and how to direct traffic across clusters or regions.

---

# **21.1 Routing Rules & VirtualServices**

A **VirtualService** defines how requests are routed _to_ a service.  
A **DestinationRule** defines policies _for_ the service's subsets/endpoints.

---

## **21.1.1 Basic Routing Flow**

```
Client → Envoy → VirtualService (routing logic) → DestinationRule → Cluster → Pod
```

---

## **21.1.2 Simple VirtualService Example**

This routes all traffic to version v1:

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: checkout
spec:
  hosts:
  - checkout
  http:
  - route:
    - destination:
        host: checkout
        subset: v1
```

---

## **21.1.3 Creating Subsets in DestinationRule**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: DestinationRule
metadata:
  name: checkout
spec:
  host: checkout
  subsets:
  - name: v1
    labels:
      version: v1
  - name: v2
    labels:
      version: v2
```

The label `version=v1` must match pod labels.

---

## **21.1.4 Matching on Paths / Headers**

### Path-based routing:

```yaml
http:
- match:
  - uri:
      prefix: "/v2"
  route:
  - destination:
      host: checkout
      subset: v2
```

### Header-based routing:

```yaml
match:
- headers:
    x-user-tier:
      exact: "beta"
```

---

## **21.1.5 Common Pitfalls**

- Forgetting to define subsets → VirtualService silently fails
    
- Using hostname mismatch (FQDN vs short name)
    
- Conflicting VirtualServices for same host
    
- Header-based routing case sensitivity issues
    

---

# **21.2 Weighted Routing**

Weighted routing splits traffic between versions.

---

## **21.2.1 Example: 90/10 Split**

```yaml
http:
- route:
  - destination:
      host: checkout
      subset: v1
    weight: 90
  - destination:
      host: checkout
      subset: v2
    weight: 10
```

Weights must sum to **100**.

---

## **21.2.2 Gradual Traffic Shifting Example**

**Step 1 → 1% traffic to v2**

```yaml
weight: 99 / 1
```

**Step 2 → 10% traffic to v2**

```yaml
weight: 90 / 10
```

**Step 3 → 50% traffic to v2**

```yaml
weight: 50 / 50
```

**Step 4 → full cutover**

```yaml
weight: 0 / 100
```

This pattern is commonly automated via:

- Argo Rollouts
    
- Flagger
    
- custom pipelines
    

---

## **21.2.3 Verifying Weighted Routing**

Check routing with Kiali visualization or manually:

```bash
curl -H "x-debug: 1" https://checkout.example.com
```

Or log traffic distribution from Envoy:

```bash
kubectl exec <pod> -c istio-proxy -- curl localhost:15000/stats | grep cluster.checkout
```

---

## **21.2.4 Common Pitfalls**

- Missing DestinationRule → no subsets → routing ignored
    
- Relying on low-traffic services → statistical noise, incorrect weight perception
    
- Sticky sessions causing uneven routing
    
- Misconfigured readiness/liveness → v2 traffic blackhole
    

---

# **21.3 Canary Releases**

A canary release gradually introduces a new version to a small subset of users while monitoring performance/metrics.

---

## **21.3.1 Canary Pattern Overview**

Steps:

1. Deploy v2 alongside v1
    
2. Route small % of traffic to v2
    
3. Observe metrics, logs, SLOs
    
4. Increase traffic gradually
    
5. Roll back on failure
    

---

## **21.3.2 Example Canary Setup**

### **DestinationRule** (with subsets v1 and v2)

_(shown earlier)_

### **VirtualService** for canary rollout

```yaml
http:
- route:
  - destination:
      host: checkout
      subset: v1
    weight: 95
  - destination:
      host: checkout
      subset: v2
    weight: 5
```

---

## **21.3.3 Adding Header-Based Canarying**

Useful for beta testers or internal users:

```yaml
match:
- headers:
    x-user-id:
      prefix: "internal-"
route:
- destination:
    host: checkout
    subset: v2
  weight: 100
```

---

## **21.3.4 Canary Rollback**

Rollback is trivial:

```yaml
weight: 100 (v1) / 0 (v2)
```

or:

```bash
kubectl rollout undo deployment/checkout-v2
```

---

## **21.3.5 Observability Considerations**

During canary:

- Compare errors/success ratio
    
- Compare P95 latency
    
- Compare saturation metrics
    
- Enable request logs for v2 (for debugging)
    

---

## **21.3.6 Common Pitfalls**

- Canary on low traffic → cannot detect issues
    
- Not isolating v2 logs/metrics → confusion
    
- No automated rollback logic → outages
    
- Using path-based routing breaks third-party clients
    

---

# **21.4 Regional Failover Through Mesh**

Istio supports **locality-aware routing** and **failover** across regions and clusters.

This is key for:

- Multi-region reliability
    
- Disaster recovery
    
- Active–passive deployments
    

---

## **21.4.1 Locality-Aware Load Balancing**

Envoy understands Kubernetes node topology:

```
region/zone/node
```

Example:

```
us-central1/zone-a/node-1
europe-west1/zone-b/node-7
```

If the local region is unhealthy, traffic shifts to the next region.

---

## **21.4.2 Enabling Locality Routing**

In **DestinationRule**:

```yaml
trafficPolicy:
  loadBalancer:
    localityLbSetting:
      enabled: true
      failover:
        us-central1: europe-west1
        europe-west1: us-central1
```

Meaning:

- If us-central1 is unhealthy → failover to europe-west1
    
- Failover happens automatically when endpoints unavailable
    

---

## **21.4.3 Regional Endpoint Grouping**

Istio groups endpoints by region.  
If EDS returns:

```
10.0.0.21 (us-central1)
10.4.1.15 (europe-west1)
```

Envoy will:

- first pick the local region
    
- shift to remote only on failure
    

---

## **21.4.4 Failover Testing**

Simulate regional outage:

```bash
kubectl scale deployment checkout-v1 --replicas=0 -n us-central1
```

Check active endpoints:

```bash
kubectl exec pod -c istio-proxy -- curl localhost:15000/clusters
```

Look for traffic routed to EU region.

---

## **21.4.5 Common Failover Pitfalls**

- Using headless services → locality logic breaks
    
- Missing labels on nodes → Envoy sees everything as one region
    
- No DestinationRule → locality LB inactive
    
- Readiness probes too slow → delayed failover
    
- Network partitions cause half-open connections
    

---

# **21.5 Service Entry / Egress Control**

Istio restricts outbound traffic unless explicitly configured.

---

## **21.5.1 What ServiceEntry Does**

It defines:

- **External services** reachable from the mesh
    
- Whether to use mTLS or plaintext
    
- Allowed hosts
    

---

## **21.5.2 Basic ServiceEntry Example**

Allow calls to `api.stripe.com`:

```yaml
apiVersion: networking.istio.io/v1beta1
kind: ServiceEntry
metadata:
  name: stripe-api
spec:
  hosts:
  - "api.stripe.com"
  ports:
  - number: 443
    name: https
    protocol: HTTPS
  resolution: DNS
  location: MESH_EXTERNAL
```

---

## **21.5.3 Egress Gateway**

To force outbound traffic through controlled gateway:

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: stripe-egress
spec:
  hosts:
  - api.stripe.com
  gateways:
  - mesh
  - istio-egressgateway
  http:
  - route:
    - destination:
        host: api.stripe.com
        port:
          number: 443
```

---

## **21.5.4 DNS Resolution in Service Entries**

If you use static IPs:

```yaml
resolution: STATIC
endpoints:
- address: 3.120.12.18
```

If using DNS:

```yaml
resolution: DNS
```

---

## **21.5.5 Blocking All Egress Except Allowed Hosts**

Mesh-wide:

```yaml
apiVersion: security.istio.io/v1beta1
kind: AuthorizationPolicy
metadata:
  name: deny-all-egress
  namespace: istio-system
spec:
  action: DENY
  rules:
  - to:
    - operation:
        notHosts:
        - "*.cluster.local"
```

Add exceptions per namespace.

---

## **21.5.6 Common Egress Pitfalls**

- Outbound HTTPS interception breaks some clients
    
- Missing ServiceEntry → Envoy blocks external traffic
    
- Using STATIC resolution for dynamic cloud APIs → breakage
    
- Forgetting that egress gateways need firewall egress rules
    
- DNS resolution failures inside mesh due to ISTIO_META_DNS_CAPTURE misconfig
    

---

# **Chapter 22 — Resilience Patterns**

_(Expanded with senior-level clarity, battle-tested Istio patterns, proxy-level configuration, and realistic failure handling.)_

Modern distributed systems require resilience at **both the application and mesh levels**. Istio/Envoy provides first-class constructs to prevent cascading failures, isolate unhealthy endpoints, and automatically recover from partial outages.  
This chapter covers timeouts, retries, circuit breaking, outlier detection, fail-fast patterns, and multi-region resilience design.

---

# **22.1 Timeouts, Retries & Backoff**

Envoy (and therefore Istio) treats **timeouts** and **retries** as first-class failure controls.  
They help reduce tail latency, prevent hung connections, and retry transient failures without overloading backends.

---

## **22.1.1 Timeouts**

A timeout tells Envoy how long to wait for a backend before giving up.

### **Default Istio behavior**

If not explicitly set:

- **HTTP timeout is 15 seconds**
    
- Dangerous for slow clients and prevents effective failover
    

---

## **22.1.2 Setting a Custom Timeout**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: checkout
spec:
  hosts:
  - checkout
  http:
  - timeout: 2s       # ⬅ hard timeout
    route:
    - destination:
        host: checkout
```

### Recommended:

- Public APIs: **1–5s**
    
- Internal calls: **500ms–2s**
    
- DB proxies or heavy operations: case-by-case
    

---

## **22.1.3 Retries**

Retries help recover from:

- 5xx errors
    
- connection failures
    
- timeouts
    
- transient blips
    

### **Retry Example with Backoff**

```yaml
http:
- retries:
    attempts: 3
    perTryTimeout: 1s
    retryOn: gateway-error,connect-failure,refused-stream
  route:
  - destination:
      host: checkout
```

---

## **22.1.4 Backoff Strategy**

Envoy uses **exponential backoff with jitter** by default.

Retry backoff =

```
base_interval * (2^attempt) + jitter
```

This avoids “retry storms.”

---

## **22.1.5 When NOT to Retry**

Avoid retries on:

- Non-idempotent operations (POST to payment API)
    
- Long batch jobs
    
- Stateful services
    
- Calls that cause side effects
    

---

## **22.1.6 Common Pitfalls**

- Retry loops amplifying load → cascading failure
    
- Timeout > retry perTryTimeout → mismatch causes hangs
    
- High retry attempts + low traffic → noisy logs
    
- Using retries without circuit breaker → overloads backend
    

---

# **22.2 Circuit Breaking**

Circuit breaking limits the number of concurrent connections/requests to a service.  
Instead of hammering an overloaded backend, Envoy sheds load gracefully.

---

## **22.2.1 Circuit Breaker Example**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: DestinationRule
metadata:
  name: checkout
spec:
  host: checkout
  trafficPolicy:
    connectionPool:
      http:
        http1MaxPendingRequests: 1      # queue_limit
        maxRequestsPerConnection: 10    # keep-alive settings
      tcp:
        maxConnections: 100
```

---

## **22.2.2 Key Circuit Breaker Fields**

|Field|Description|
|---|---|
|`maxConnections`|Limits max TCP connections|
|`http1MaxPendingRequests`|Queue length limit|
|`maxRequestsPerConnection`|Reuse limit for keep-alive|
|`maxRetries`|Total retry attempts allowed|

---

## **22.2.3 Behaviors When Tripped**

- New requests receive **503 UO** (upstream overflow)
    
- Existing requests continue
    
- Avoids total backend overload
    

---

## **22.2.4 Practical Recommended Values**

|Workload Type|Recommended Limits|
|---|---|
|APIs|low queue, 1–10 pending|
|DB proxy|fixed number of maxConnections|
|Internal services|small queue, strict concurrency cap|

---

## **22.2.5 Common Pitfalls**

- Setting queues too large → increased tail latency
    
- No circuit breaker on critical services → cascading failures
    
- Using same breaker settings across different workloads → unpredictable behavior
    

---

# **22.3 Outlier Detection**

Outlier detection automatically removes unhealthy endpoints from the load balancing pool.

It differs from circuit breaking:

- Circuit breaking protects clients
    
- Outlier detection protects the **mesh** from bad endpoints
    

---

## **22.3.1 Example Outlier Detection**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: DestinationRule
metadata:
  name: checkout
spec:
  host: checkout
  trafficPolicy:
    outlierDetection:
      consecutive5xx: 3
      interval: 5s
      baseEjectionTime: 30s
      maxEjectionPercent: 50
```

This means:

- If a pod returns **3× 5xx** in **5s**
    
- Eject from the load balancing pool for **30s**
    
- Maximum 50% of endpoints can be removed
    

---

## **22.3.2 Ejection Types**

- **Consecutive errors** – bad endpoints
    
- **Success rate ejection** – statistical anomaly detection
    
- **Failure percentage** – based on rolling window
    

---

## **22.3.3 Observability of Ejections**

Check Envoy cluster stats:

```bash
kubectl exec <pod> -c istio-proxy -- curl localhost:15000/clusters | grep ejections
```

---

## **22.3.4 Common Pitfalls**

- Ejection too aggressive → sudden capacity drops
    
- Very small clusters (<5 pods) → unstable success rate logic
    
- Misinterpreting ejection logs as pod failures
    
- Forgetting readiness/liveness probes affect endpoint health
    

---

# **22.4 Fail-Fast Design**

Fail-fast helps services return failures quickly rather than waiting on hung dependencies.

Fail-fast patterns reduce:

- Latency
    
- Thread exhaustion
    
- Increased retry load
    
- UI freezes
    
- Cascading failure propagation
    

---

## **22.4.1 Fail-Fast Using Timeouts**

```yaml
http:
- timeout: 500ms
```

Fast failure → allows retry earlier → minimises user impact.

---

## **22.4.2 Fail-Fast Using Circuit Breaker Queue Limit**

```yaml
connectionPool:
  http:
    http1MaxPendingRequests: 1
```

Queue of 1 = almost immediate fail-fast.

---

## **22.4.3 Fail-Fast Using Retry Budget**

Limit retries:

```yaml
retries:
  attempts: 1
  perTryTimeout: 300ms
```

---

## **22.4.4 Fail-Fast for Non-Critical Dependencies**

E.g., downstream analytics API or recommendations engine:

```
If API fails → degrade gracefully → return empty list
```

---

## **22.4.5 Fail-Fast Anti-Patterns**

- Fail-fast on payment or order-processing APIs → high business impact
    
- Too strict timeouts → trigger unnecessary cascading failures
    
- No fallback logic → fail-fast becomes "fail-always"
    

---

# **22.5 Multi-Region Resilience Design**

Multi-region designs protect against:

- Zone failures
    
- Regional outages
    
- Network partitions
    
- Control-plane degradation
    
- Cluster-level failures
    

This section covers patterns using Istio to implement region-aware routing and automatic failover.

---

## **22.5.1 Locality Routing (Preferred)**

Istio automatically routes calls to the nearest region.

Enable:

```yaml
trafficPolicy:
  loadBalancer:
    localityLbSetting:
      enabled: true
```

---

## **22.5.2 Region Failover Example**

Failover from `us-central1` → `europe-west1`.

```yaml
localityLbSetting:
  failover:
    us-central1: europe-west1
```

---

## **22.5.3 Active–Active Multi-Region Pattern**

### Characteristics:

- Both regions receive traffic
    
- SLO tracking per region
    
- Automatic failover if endpoints unhealthy
    

### Example:

```yaml
subsets:
- name: us
  labels: { region: us-central1 }
- name: eu
  labels: { region: europe-west1 }
```

VirtualService:

```yaml
route:
- destination:
    host: checkout
    subset: us
  weight: 50
- destination:
    host: checkout
    subset: eu
  weight: 50
```

---

## **22.5.4 Active–Passive Pattern**

Primary region handles all traffic.

Failover triggers:

- readiness failures
    
- endpoint ejection
    
- cluster unreachable
    

Istio handles failover using outlier detection + locality routing.

---

## **22.5.5 Multi-Cluster Mesh Failover**

In single control plane multi-cluster setups:

- EDS aggregates endpoints across clusters
    
- Failover happens when local endpoints unavailable
    

### Validation:

```bash
kubectl exec <pod> -c istio-proxy -- curl localhost:15000/clusters
```

---

## **22.5.6 Cross-Region Failure Scenarios**

|Failure|Expected Behavior|
|---|---|
|Zone outage|In-zone endpoints removed → shift to healthy zones|
|Region outage|Endpoint ejection + locality LB failover|
|Control plane down|Envoy uses last known config|
|Partial outage|Outlier detection removes unstable endpoints|

---

## **22.5.7 Multi-Region Pitfalls**

- Missing locality labels → cross-region traffic even when local region healthy
    
- Inconsistent deployments → failover serves wrong version
    
- Too strict outlierDetection → cascaded ejection
    
- DNS used instead of mesh-level routing → slow failover
    
- Long-lived TCP connections → slow cutover
    

---

# **Chapter 23 — Progressive Mesh Adoption**

_(Expanded with senior-level clarity, migration strategies, YAML examples, traffic flow diagrams, adoption risks, and guidance for transitioning from legacy workloads into a service mesh.)_

Progressive adoption means incrementally introducing a service mesh without breaking existing systems. A successful approach minimizes operational overhead while enabling teams to gradually adopt sidecars, gateways, and mesh-level policies.

---

# **23.1 Sidecar Injection Strategy**

Sidecar injection adds Envoy containers to Pods. Treat this as a **controlled rollout**, not a global switch.

---

## **23.1.1 Sidecar Injection Modes**

### **1. Namespace-wide automatic injection** (recommended for most)

```bash
kubectl label namespace payments istio-injection=enabled
```

### **2. Pod-level manual injection**

```bash
kubectl kube-inject -f deployment.yaml | kubectl apply -f -
```

### **3. Revision-based injection (for canary control planes)**

Useful during Istio upgrades.

```bash
kubectl label namespace payments istio.io/rev=1-20-3
```

---

## **23.1.2 Recommended Injection Strategy**

### **Phase 1 — Identify candidates**

- stateless services first
    
- internal-only dependencies
    
- services with readiness/liveness probes configured
    

Avoid initially:

- stateful workloads
    
- high-throughput nodes (e.g., Kafka brokers)
    
- extremely latency-sensitive workloads
    
- workloads using hostNetwork
    

---

### **Phase 2 — Enable injection in staging namespaces**

Observe:

- CPU/memory overhead
    
- connection latencies
    
- readiness delays
    
- outbound connection patterns
    

---

### **Phase 3 — Enable injection gradually in production**

Typical sequence:

1. Shadow namespace with injection
    
2. Canary a single Deployment
    
3. Increase rollout to a full namespace
    
4. Enforce mesh-wide defaults (mTLS, policies)
    

---

## **23.1.3 Example: Diagnosing Sidecar Issues**

Check injection status:

```bash
kubectl get pod -o jsonpath='{.spec.containers[*].name}'
```

Check injection logs:

```bash
kubectl -n istio-system logs deploy/istiod | grep inject
```

---

## **23.1.4 Common Sidecar Pitfalls**

- Missing/incorrect app ports → Envoy cannot bind listeners
    
- Probes not routed properly → readiness fails
    
- Applications binding to 127.0.0.1 → traffic bypasses mesh
    
- Init container deadlocks due to outbound block
    
- Sidecar CPU overhead unaccounted for in HPA
    

---

# **23.2 Ingress Gateway Migration**

Ingress gateways expose services at the mesh boundary. Migrating from Kubernetes Ingress or non-Istio LBs must be deliberate.

---

## **23.2.1 Ingress Gateway Architecture**

```
Client → L7 LB → Istio IngressGateway (Envoy) → VirtualService → Workload
```

Benefits:

- fine-grained routing
    
- JWT verification
    
- custom filters
    
- WASM plugins
    
- mTLS interoperability
    

---

## **23.2.2 Migration Strategy**

### **Phase 1 — Deploy Gateway alongside existing ingress**

Expose using separate hostname:

```yaml
apiVersion: networking.istio.io/v1beta1
kind: Gateway
metadata:
  name: api-gw
spec:
  selector:
    istio: ingressgateway
  servers:
  - port:
      number: 443
      name: https
      protocol: HTTPS
    tls:
      mode: SIMPLE
      credentialName: api-cert
    hosts:
    - "api.example.com"
```

---

### **Phase 2 — Configure VirtualService**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: api
spec:
  hosts:
  - "api.example.com"
  gateways:
  - api-gw
  http:
  - route:
    - destination:
        host: api
        port:
          number: 8080
```

---

### **Phase 3 — DNS shift**

Switch DNS gradually:

- weight-based (if using split-horizon + global LB)
    
- or cut over instantly
    

---

### **Phase 4 — Disable legacy ingress**

Ensure:

- health checks pass
    
- metrics stable
    
- logs clean
    

Then eliminate unused Kubernetes Ingress objects.

---

## **23.2.3 Common Gateway Pitfalls**

- Certificates not loaded due to wrong `credentialName`
    
- Missing ports in Service → gateway not reachable
    
- Overlapping VirtualServices → route ambiguity
    
- Using HTTP/1.1 routing for gRPC without upgrade header
    

---

# **23.3 Gradual Onboarding of Services**

Mesh adoption should be **incremental** and **observability-driven**.

---

## **23.3.1 Service Onboarding Stages**

### **Stage 1 — Visibility Only**

- Enable sidecar
    
- No routing changes
    
- Observability validation
    
- mTLS PERMISSIVE mode
    

```yaml
apiVersion: security.istio.io/v1beta1
kind: PeerAuthentication
metadata:
  name: default
spec:
  mtls:
    mode: PERMISSIVE
```

---

### **Stage 2 — Traffic Management**

Enable:

- timeouts
    
- retries
    
- circuit breakers
    

```yaml
apiVersion: networking.istio.io/v1beta1
kind: DestinationRule
metadata:
  name: checkout
spec:
  trafficPolicy:
    connectionPool:
      http:
        http1MaxPendingRequests: 1
    outlierDetection:
      consecutive5xx: 3
```

---

### **Stage 3 — Security Controls**

Enable:

- Strict mTLS
    
- AuthorizationPolicy
    

```yaml
apiVersion: security.istio.io/v1beta1
kind: PeerAuthentication
metadata:
  name: default
spec:
  mtls:
    mode: STRICT
```

---

### **Stage 4 — Advanced Capabilities**

- fault injection
    
- A/B tests
    
- multi-region routing
    
- egress gateway
    

---

## **23.3.2 Observability Checklist**

Before onboarding into mesh:

- Pod exposes health endpoints
    
- Distributed tracing instrumented
    
- Correct service account assigned
    
- Pod labels consistent (required for subsets)
    
- Correct readiness & startup probes
    

---

## **23.3.3 Common Onboarding Pitfalls**

- Skipping the visibility stage → no baseline to compare
    
- Services with long-lived TCP connections → Envoy resets prematurely
    
- DNS capture breaking legacy workloads
    
- Metrics volume spike from sidecars → Prometheus overload
    
- Missing subsets → VirtualService ignored
    

---

# **23.4 Ambient Mesh Overview**

Ambient Mesh is a next-generation mesh mode removing the need for sidecars. It replaces per-pod Envoy proxies with **per-node** and **per-namespace** proxies.

_(Note: Ambient is evolving; treat as future-facing capability.)_

---

## **23.4.1 Components in Ambient Mesh**

### **1. ztunnel**

- Runs per-node
    
- Handles identity + mTLS
    
- Handles L4 routing
    

### **2. waypoint proxy**

- Runs per-namespace or per-service
    
- L7 (HTTP) routing and policies
    
- Implemented as Envoy
    

---

## **23.4.2 Ambient Traffic Flow**

```
Pod → ztunnel (L4 identity + mTLS) → waypoint proxy (optional L7) → destination
```

---

## **23.4.3 Benefits of Ambient Mesh**

- No sidecar overhead (CPU/memory savings)
    
- Faster rollout/rollback
    
- Works with workloads that cannot run sidecars
    
- Lower operational complexity
    
- Easier mTLS adoption
    

---

## **23.4.4 Ambient Mesh Adoption Strategy**

### Good candidates:

- simple HTTP services
    
- workloads that cannot tolerate sidecar overhead
    
- teams struggling with auto-injection issues
    

### Poor candidates (initially):

- high-performance, low-latency workloads
    
- advanced routing requiring rich L7 logic
    

---

## **23.4.5 Minimal Ambient Enablement Example**

Enable ambient in namespace:

```bash
kubectl label namespace payments istio.io/dataplane-mode=ambient
```

Deploy waypoint proxy for service:

```bash
istioctl waypoint apply --service payments-api
```

---

## **23.4.6 Common Ambient Mesh Pitfalls**

- Assuming full L7 parity with sidecar mode
    
- Mixing sidecar and ambient modes without clear boundaries
    
- Not understanding that ztunnel is L4 only
    
- Waypoint proxies adding latency if misconfigured
    

---

# **23.5 Mesh Anti-Patterns**

Even experienced teams introduce failure-prone mesh configurations.  
These anti-patterns can degrade reliability, increase latency, or cause outages.

---

## **23.5.1 Anti-Pattern: Mesh Everything**

Injecting sidecars into:

- CI systems
    
- backup jobs
    
- large batch processing nodes
    
- metrics exporters
    

→ **unnecessary CPU overhead**  
→ **outbound traffic bottlenecks**

---

## **23.5.2 Anti-Pattern: Overusing VirtualServices**

Do NOT create one VirtualService per route.  
Use consolidated VirtualServices per host.

Bad:

```
checkout-vs-path1.yaml
checkout-vs-path2.yaml
checkout-vs-path3.yaml
```

Creates conflicts & race conditions.

---

## **23.5.3 Anti-Pattern: Undefined Subsets**

VirtualService referencing missing subsets:

```yaml
subset: v2   # but no v2 in DestinationRule
```

→ routing silently ignored  
→ very difficult to debug

---

## **23.5.4 Anti-Pattern: Using Mesh for Non-Mesh Problems**

Examples:

- Using mTLS for public internet APIs
    
- Using VirtualService for TCP tunneling
    
- Using outlier detection for DB failover
    
- Forcing mesh routing instead of using L4 load balancers
    

---

## **23.5.5 Anti-Pattern: Mesh-Heavy Migration in One Shot**

Turning on:

- sidecar injection
    
- STRICT mode
    
- authorization policies
    
- JWT auth
    
- outlier detection
    
- custom retries
    

All at once guarantees outages.

Adoption must be staged.

---

## **23.5.6 Anti-Pattern: Bypassing the Sidecar**

Using:

- hostNetwork
    
- ports bound to 127.0.0.1
    
- nodePort access
    
- direct cluster IP access from external systems
    

→ breaks mesh observability, security, routing logic

---

## **23.5.7 Anti-Pattern: Unbounded Telemetry**

Logging and metrics from Envoy can overwhelm:

- Prometheus
    
- FluentBit
    
- Logging pipelines
    

Use:

- sampling
    
- logging filters
    
- scrape limits
    

---

# **Chapter 24 — SLIs, SLOs & Error Budgets**

_(Expanded with senior-level clarity, SRE methodology, Prometheus/Grafana examples, and service-mesh-aware instrumentation.)_

Service Level Indicators (SLIs), Service Level Objectives (SLOs), and Error Budgets form the backbone of modern reliability engineering. They define _what reliability means_, _how to measure it_, and _how much failure is acceptable_ before engineering teams must pause feature work and focus on stability.

This chapter will make you fluent in designing measurable SLIs, setting actionable SLOs, calculating and enforcing error budgets, and building dashboards that enable real-time insight.

---

# **24.1 Choosing SLIs**

An SLI is a _metric_ that reflects how well a service meets user expectations.  
The SLI must be:

- **measurable**
    
- **user-centric**
    
- **objective**
    
- **low cardinality**
    
- **cheap to compute**
    

---

## **24.1.1 Core SLI Categories**

### **1. Availability**

“How often can users successfully perform an action?”

Typical metrics:

- HTTP success rate
    
- Availability of API endpoints
    
- mTLS handshake failures in mesh
    
- LB backend health status
    

**Prometheus example:**

```promql
sum(rate(istio_requests_total{response_code!~"5.."}[5m])) 
/
sum(rate(istio_requests_total[5m]))
```

---

### **2. Latency**

“How fast do requests respond?”

Important:

- Use **P95/P99 latency**, not averages.
    
- Latency must be measured _after retries_ (user perspective).
    

**Prometheus example (P95):**

```promql
histogram_quantile(0.95, sum(rate(istio_request_duration_seconds_bucket[5m])) by (le))
```

---

### **3. Quality / Correctness**

“Does the system return the correct result?”

Examples:

- Valid checkouts
    
- Inventory consistency
    
- Data freshness for analytics
    

Often application-specific.

---

### **4. Freshness / Staleness (for data systems)**

Example SLI:

- "Data is no older than 5 minutes"
    

**PromQL example:**

```promql
time() - max(last_ingest_timestamp) < 300
```

---

### **5. Throughput**

Only used when throughput itself matters to user experience.

---

## **24.1.2 How to Select SLIs**

Principles:

1. **SLIs must reflect actual user-perceived reliability.**  
    Not CPU usage, not memory, not pod health—_users don't care_.
    
2. **Each SLI must have a single, authoritative measurement path.**  
    Don’t duplicate metrics across layers.
    
3. **SLIs should be stable over time.**  
    Never use ephemeral per-pod metrics; use mesh/LB global metrics.
    

---

## **24.1.3 Examples of Good SLIs**

|Layer|SLI Example|
|---|---|
|Ingress|P99 latency < 250ms|
|Mesh|99.95% request success|
|API|Checkouts succeed >= 99.9%|
|Data|ETL pipeline < 5 minutes behind|
|Queue|Message age < 10 seconds|

---

## **24.1.4 Common SLI Pitfalls**

- Using **pod-level metrics**, which do not represent user experience.
    
- Using **synthetic probes** as the primary SLI (should be a backup).
    
- Using **averages**, not percentiles.
    
- SLIs that are too sensitive → false violations.
    
- SLIs not aligned to business goals.
    

---

# **24.2 Setting SLOs**

SLIs measure; SLOs define _targets_.

An SLO must be:

- **achievable** (based on historical data)
    
- **meaningful** (impactful to users)
    
- **simple** (1–2 sentences)
    
- **time-scoped** (monthly/quarterly)
    

---

## **24.2.1 SLO Statement Format**

**Example:**

> _“Checkout API will have a 99.9% monthly availability measured as the ratio of successful HTTP 2xx/3xx responses to total requests.”_

---

## **24.2.2 SLO Period**

Typical periods:

- **28-day rolling window** (Google standard)
    
- Quarterly (financial alignment)
    
- Weekly (for fast-moving teams)
    

---

## **24.2.3 Calculating SLOs with Prometheus**

Example for availability:

```promql
sum(increase(istio_requests_total{response_code!~"5.."}[28d]))
/
sum(increase(istio_requests_total[28d]))
```

If result = 0.9992 → SLO met.

---

## **24.2.4 Latency SLO Example**

```
99% of requests < 200ms over last 28 days
```

PromQL:

```promql
histogram_quantile(0.99,
  sum(rate(istio_request_duration_seconds_bucket[5m])) by (le)
)
```

Compare against objective.

---

## **24.2.5 Choosing SLO Values**

Guidelines:

- Start with historical performance (+1–2%)
    
- Prioritize critical paths with higher SLOs
    
- If you require 100%, you're wrong.  
    _No real system does 100%._
    

---

## **24.2.6 Common SLO Pitfalls**

- Setting SLOs higher than upstream dependencies.
    
- No consultation with product owners.
    
- Too many SLOs (max 5 per service).
    
- SLOs used punitively → teams hide incidents.
    
- SLOs without _actions_ tied to them.
    

---

# **24.3 Error Budgets**

Error Budgets are the **allowed amount of failure** within the SLO period.

If SLO is 99.9% uptime:

- Error budget = 0.1% downtime allowed
    

Over 28 days:

```
28 days = 2,419,200 seconds
0.1% of that ≈ 2419 seconds
→ ~40 minutes monthly budget
```

---

## **24.3.1 Error Budget Formula**

```
ErrorBudget = 1 - SLO
```

Example:

- SLO 99.95% → error budget 0.05%
    

---

## **24.3.2 Error Budget Burn Rate**

Burn rate = rate of consumption of error budget.

Prometheus example:

```promql
(
  sum(rate(istio_requests_total{response_code=~"5.."}[5m])) /
  sum(rate(istio_requests_total[5m]))
)
```

If burn rate > allowed → **alert**.

---

## **24.3.3 Multi-Window Multi-Burn Rate Alerts (Google SRE)**

Two windows recommended:

- Fast-burn: 5 min alert (e.g., 14x burn rate)
    
- Slow-burn: 1 hour alert (e.g., 3x burn rate)
    

Example fast-burn alert:

```promql
<fast burn rate expression> > 14
```

---

## **24.3.4 Error Budget Policy**

If error budget is exhausted:

- Pause feature work
    
- Focus on improving reliability
    
- Evaluate architectural issues
    
- Improve auto-scaling, retries, timeouts
    

If error budget is healthy:

- Lower risk posture
    
- Allow faster feature rollouts
    
- Increase experiments
    

---

## **24.3.5 Common Error Budget Pitfalls**

- Measuring error budget using _synthetic canary_ instead of real traffic
    
- Not linking burn-rate alerts to on-call escalation
    
- Ignoring budget exhaustion → SLO process becomes meaningless
    
- Not using multiple burn-rate windows → noisy alerts
    

---

# **24.4 Dashboards & Measurement**

Dashboards visualize SLI performance and error budget consumption.

---

## **24.4.1 What a Good Dashboard Contains**

### 1. **Traffic Overview**

- RPS
    
- success rate
    
- error rate
    

### 2. **Latency**

- P50
    
- P95
    
- P99
    

### 3. **SLO Page**

- rolling availability
    
- current error budget
    
- burn rate graphs
    
- annotations for incidents
    

### 4. **Dependency Health**

- upstream/lower-tier services
    
- external API dependencies
    

---

## **24.4.2 Grafana Dashboard Example (JSON Snippet)**

Minimal panel definition:

```json
{
  "title": "P99 Latency",
  "type": "graph",
  "targets": [
    {
      "expr": "histogram_quantile(0.99, sum(rate(istio_request_duration_seconds_bucket[5m])) by (le))",
      "legendFormat": "P99"
    }
  ]
}
```

---

## **24.4.3 GKE + Istio Recommended Metrics Sources**

Metrics come from:

|Source|Purpose|
|---|---|
|Envoy|SLIs for internal communication|
|Istiod|Mesh health|
|IngressGateway|Client-perceived SLIs|
|Application metrics|correctness SLIs|
|Cloud Load Balancer logs|regional error patterns|

---

## **24.4.4 Example SLO Dashboard Queries**

### Availability

```promql
(sum(rate(istio_requests_total{response_code!~"5.."}[5m])) /
 sum(rate(istio_requests_total[5m])))
```

### Error budget burn rate

```promql
(1 - (success_rate)) / (1 - SLO_target)
```

---

## **24.4.5 Observability Pitfalls**

- Using P99 without enough traffic → meaningless spikes
    
- No multi-window alerts → miss slow burn outages
    
- Tracking latency without splitting by route
    
- Too many panels → dashboard overload
    
- Using logs instead of metrics for SLI calculation
    

---

# **Chapter 25 — Observability Stack**

_(Expanded with senior-level clarity, practical Prometheus/Grafana/OTel/GCP examples, Envoy-level instrumentation, and production-ready configurations.)_

A complete observability stack provides **metrics**, **logs**, **traces**, and **exemplars** to help teams understand system behavior, detect anomalies, troubleshoot outages, and improve performance and reliability.  
This chapter details how to build a robust observability pipeline for Kubernetes, GKE, and service mesh–based architectures.

---

# **25.1 Metrics**

Metrics provide numeric time-series data about system behavior.  
They are essential for:

- SLOs/SLIs
    
- dashboards
    
- alerting
    
- capacity planning
    
- performance debugging
    

---

## **25.1.1 Types of Metrics**

### **1. System Metrics**

Node CPU, memory, disk, network.  
Collected by:

- GKE node agent
    
- kubelet
    
- cAdvisor
    

### **2. Kubernetes Metrics**

Pod restarts, queue depth, deployments, HPA behavior.

Collected by:

- kube-state-metrics
    
- metrics-server
    

### **3. Application Metrics**

Business metrics (checkouts, payments), custom counters, histograms.  
Typically collected via:

- Prometheus client libraries
    
- OpenTelemetry SDK
    

### **4. Mesh Metrics**

Envoy provides:

- request count
    
- latency histogram
    
- mTLS status
    
- retry counts
    
- outlier ejections
    
- TCP metrics
    

Collected via:

- Prometheus scraping Envoy `/stats`
    

---

## **25.1.2 Prometheus Scraping Example (GKE + Istio)**

ServiceMonitor for scraping Envoy proxies:

```yaml
apiVersion: monitoring.coreos.com/v1
kind: ServiceMonitor
metadata:
  name: istio-sidecar
spec:
  selector:
    matchLabels:
      istio.io/rev: default
  endpoints:
  - port: http-envoy-prom
    interval: 30s
    path: /stats/prometheus
```

---

## **25.1.3 Example Application Metric (Go)**

```go
var checkoutSuccess = prometheus.NewCounterVec(
    prometheus.CounterOpts{
        Name: "checkout_success_total",
        Help: "Number of successful checkouts",
    },
    []string{"currency"},
)
```

Expose metrics endpoint:

```go
http.Handle("/metrics", promhttp.Handler())
```

---

## **25.1.4 Important Metric Patterns**

- **RED** (Rate, Errors, Duration) for HTTP services
    
- **USE** (Utilization, Saturation, Errors) for system monitoring
    
- **Golden Signals** (latency, traffic, errors, saturation)
    

---

## **25.1.5 Metrics Anti-Patterns**

- High-cardinality labels → Prometheus explosions
    
- Using request-level metrics instead of aggregated histograms
    
- Storing massive metrics in memory-bound Prometheus
    
- Not applying scrape limits → potential cluster meltdown
    

---

# **25.2 Logs**

Logs are detailed, unstructured or structured textual records of events.

In GKE, logs often originate from:

- application logs
    
- stdout/stderr from containers
    
- Envoy access logs
    
- audit logs
    
- GCP platform logs
    

---

## **25.2.1 Recommended Logging Format**

**JSON logs** (machine-parsable):

```json
{
  "timestamp": "2024-06-01T12:00:00Z",
  "service": "checkout",
  "level": "INFO",
  "msg": "checkout completed",
  "user_id": "abc123",
  "order_id": "98765"
}
```

---

## **25.2.2 Log Collection in GKE**

GKE with Cloud Operations uses Fluent Bit/Fluentd agents that collect:

- container stdout
    
- file-based logs
    
- node system logs
    

### To inspect container logs:

```bash
kubectl logs deployment/checkout
```

### To view logs in Cloud Logging via gcloud:

```bash
gcloud logging read "resource.type=k8s_container AND labels.k8s-pod/app=checkout" --limit=50
```

---

## **25.2.3 Envoy Access Logs**

Enable access logs using telemetry API:

```yaml
apiVersion: telemetry.istio.io/v1alpha1
kind: Telemetry
metadata:
  name: access-logs
spec:
  accessLogging:
    providers:
    - name: envoy
```

---

## **25.2.4 Log Retention Strategy**

- Application logs: 7–30 days
    
- Mesh logs: 1–7 days (high volume)
    
- Audit logs: 400 days (regulatory reasons)
    
- Error logs: 90+ days
    

---

## **25.2.5 Logging Anti-Patterns**

- Unbounded logging → huge ingestion costs
    
- Logging at debug level in production
    
- Logging sensitive data (GDPR/PCI violations)
    
- Creating custom log pipelines per namespace → chaos
    

---

# **25.3 Traces**

Distributed tracing tracks request flow across services.  
Critical for understanding:

- service dependencies
    
- tail latency
    
- retry-induced latency
    
- failure propagation
    
- performance bottlenecks
    

---

## **25.3.1 Trace Fundamentals**

A trace is composed of **spans**.

Span includes:

- name
    
- timestamp
    
- duration
    
- attributes (status, error codes, metadata)
    
- parent span reference
    

---

## **25.3.2 Enabling Traces in Istio**

Telemetry API:

```yaml
apiVersion: telemetry.istio.io/v1alpha1
kind: Telemetry
metadata:
  name: tracing
spec:
  tracing:
  - provider:
      name: otel
    randomSamplingPercentage: 10
```

This sends traces to an OpenTelemetry collector.

---

## **25.3.3 OpenTelemetry Collector Configuration**

Example exporter to GCP Trace:

```yaml
exporters:
  googlecloud:
    project: your-gcp-project
service:
  pipelines:
    traces:
      receivers: [otlp]
      exporters: [googlecloud]
```

---

## **25.3.4 Example Manual Trace in Go**

```go
ctx, span := tracer.Start(ctx, "checkout.process")
defer span.End()

span.SetAttributes(attribute.String("order_id", orderID))
```

---

## **25.3.5 Trace Sampling**

Types:

- **probabilistic** (randomized)
    
- **tail-based** (smart sampling; recommended)
    

Tail sampling chooses traces containing:

- errors
    
- high latency
    
- certain tags (e.g., user ID)
    

---

## **25.3.6 Trace Anti-Patterns**

- Sampling everything → enormous storage costs
    
- Sampling too low → losing signal
    
- Not propagating trace headers → broken trace graphs
    
- Ignoring mesh-level retries → misleading latencies
    

---

# **25.4 Exemplars**

Exemplars connect **metrics → traces**, allowing you to jump directly from a high-latency metric datapoint into the corresponding trace.

They bridge:

- RED metrics
    
- latency histograms
    
- distributed traces
    

---

## **25.4.1 Why Exemplars Matter**

Without exemplars:

- You see latency spike (P99 high)
    
- You don't know _which request caused it_
    

With exemplars:

- Grafana panel shows clickable trace IDs
    

---

## **25.4.2 Enabling Exemplars in Envoy / Istio**

Istio supports exemplars automatically if:

- tracing is enabled
    
- Prometheus uses exemplar-enabled histogram buckets
    
- Proxy emits trace IDs in metric attributes
    

### Prometheus scrape config

```yaml
scrape_configs:
- job_name: envoy
  scrape_interval: 15s
  honor_labels: true
  metrics_path: /stats/prometheus
  enable_features: [exemplar-storage]
```

---

## **25.4.3 Grafana Panel Example**

Grafana configuration snippet:

```json
{
  "type": "histogram",
  "targets": [{
    "expr": "histogram_quantile(0.99, sum(rate(istio_request_duration_seconds_bucket[5m])) by (le))"
  }],
  "exemplars": {
    "enabled": true
  }
}
```

You will now see trace links embedded in metrics.

---

## **25.4.4 Exemplar Anti-Patterns**

- Using exemplars without trace sampling → low hit rate
    
- High-cardinality trace IDs → Prometheus overload
    
- Using wrong Prometheus version without exemplar support
    

---

# **25.5 GCP Cloud Operations Suite**

GCP’s Cloud Operations Suite (formerly Stackdriver) provides:

- Cloud Monitoring
    
- Cloud Logging
    
- Cloud Trace
    
- Cloud Profiler
    
- Cloud Error Reporting
    

This suite integrates tightly with GKE.

---

## **25.5.1 Cloud Monitoring Integration**

GKE Autopilot & Standard clusters install Google-managed agent:

- collects node metrics
    
- scrapes kubelet
    
- exports to Cloud Monitoring
    

Check metrics:

```bash
gcloud monitoring metrics list --filter="metric.type=starts_with('kubernetes')"
```

---

## **25.5.2 Cloud Logging**

Automatically collects:

- stdout/stderr for containers
    
- Kubernetes events
    
- node logs (systemd, kubelet)
    
- VPC flow logs (optional)
    

Search logs:

```bash
gcloud logging read "resource.type=k8s_container AND labels.k8s-pod/app=checkout"
```

---

## **25.5.3 Cloud Trace**

Automatic export from Envoy if configured via OTel Collector.

Query traces:

```bash
gcloud trace list-traces --limit=20
```

---

## **25.5.4 Cloud Profiler**

Lightweight sampling profiler for:

- CPU
    
- heap
    
- allocation
    
- goroutine/block profiles (Go)
    

Best for production profiling.

---

## **25.5.5 Cloud Error Reporting**

Aggregates application stack traces. Useful for:

- crash loops
    
- uncaught exceptions
    
- panic storms
    

---

## **25.5.6 Cloud Ops Dashboards**

You can import dashboards easily.

Example:

```bash
gcloud monitoring dashboards create --config-from-file=api-dashboard.json
```

---

## **25.5.7 GCP Observability Anti-Patterns**

- Storing high-volume logs → massive costs
    
- Using Cloud Logging as primary SLI source (slow queries)
    
- No log-based metrics → losing aggregation ability
    
- Not sending Envoy metrics → broken mesh visibility
    
- Using too many dashboards → analysis paralysis
    

---

# **Chapter 26 — High Availability Architecture**

_(Expanded with senior-level clarity, real-world patterns, failure simulations, configuration snippets, and Kubernetes/GCP examples.)_

High Availability (HA) is a **design discipline**, not a product feature. In distributed systems, availability is achieved through a combination of _redundancy_, _failover logic_, _fault isolation_, _statelessness_, and _careful state management_.  
GKE and GCP provide the primitives, but the architecture must assemble them into a reliable whole.

This chapter outlines how HA is designed across zones, regions, and multi-region deployments—including stateless and stateful workloads.

---

# **26.1 Zonal Failure Design**

A **zone** is the smallest independent failure domain in GCP.  
Zonal failures include:

- power loss
    
- network partition
    
- control-plane partition
    
- localized maintenance events
    
- hardware failures
    

HA design starts with ensuring services continue operating **even if an entire zone disappears**.

---

## **26.1.1 Zonal Failure Patterns for GKE**

### **Use Regional GKE Clusters (Recommended)**

Regional clusters replicate:

- control plane × 3
    
- node pools across ≥2 zones
    

Create a regional cluster:

```bash
gcloud container clusters create my-regional-cluster \
  --region us-central1 \
  --node-locations us-central1-a,us-central1-b \
  --num-nodes 2
```

This automatically distributes nodes across zones.

---

## **26.1.2 Pod-Level HA: PodDisruptionBudgets (PDBs)**

PDBs ensure Kubernetes won’t evict too many pods at once.

```yaml
apiVersion: policy/v1
kind: PodDisruptionBudget
metadata:
  name: checkout-pdb
spec:
  minAvailable: 2
  selector:
    matchLabels:
      app: checkout
```

This prevents voluntary disruptions (like node upgrades) from reducing service capacity below HA thresholds.

---

## **26.1.3 Zonal Anti-Affinity to Spread Pods**

Ensure replicas run in different zones.

```yaml
affinity:
  podAntiAffinity:
    requiredDuringSchedulingIgnoredDuringExecution:
    - topologyKey: topology.kubernetes.io/zone
      labelSelector:
        matchLabels:
          app: checkout
```

---

## **26.1.4 Zonal Failure Simulation**

### Drain a zone’s nodes:

```bash
kubectl drain <node> --force --ignore-daemonsets --delete-emptydir-data
```

Check if:

- service stays available
    
- HPA adjusts
    
- Envoy endpoints update correctly
    
- traffic shifts automatically
    

---

## **26.1.5 Common Zonal HA Pitfalls**

- StatefulSets with `podManagementPolicy=OrderedReady` → slow failover
    
- Not enough replicas to span zones
    
- Anti-affinity misconfigured, causing scheduling deadlocks
    
- Single-zone storage volumes
    
- Node pool autoscaling pinned to one zone
    

---

# **26.2 Regional Architectures**

Regions consist of multiple zones with low-latency fiber interconnect.  
Regional HA design ensures services survive a **single-zone outage** and tolerate partial **regional degradation**.

---

## **26.2.1 Regional Deployment Model**

Core principles:

- **Regional GKE clusters** for stateless workloads
    
- **Regional internal load balancing**
    
- **Regional managed databases** (Cloud SQL, Spanner)
    
- **Service mesh locality routing**
    

---

## **26.2.2 Regional Internal Load Balancer Example (NEG)**

```yaml
apiVersion: cloud.google.com/v1
kind: BackendConfig
metadata:
  name: checkout-backend
spec:
  healthCheck:
    checkIntervalSec: 5
    timeoutSec: 3
    healthyThreshold: 2
    unhealthyThreshold: 2
```

GKE Ingress automatically configures a regional NEG per zone.

---

## **26.2.3 Regional Service Mesh Behavior**

Envoy localities reflect zone and region:

```
region: us-central1
zone: us-central1-a
```

Locality-aware routing prefers the _same zone_, then _same region_, then _fallback region_ if configured.

---

## **26.2.4 Regional SLO Design**

Target:

- 99.9%–99.95% for regional reliability
    
- 99.99% for multi-region
    

Example:

> **“Service remains available during any single-zone failure in region us-central1.”**

---

## **26.2.5 Regional HA Pitfalls**

- Using _zonal_ Cloud SQL → full outages
    
- Storing persistent data on zonal PDs
    
- Not spreading node pools across multiple zones
    
- Regional outages misclassified as service incidents → SLIs misreport
    

---

# **26.3 Multi-Region Active/Active**

Active/Active means **both regions serve traffic simultaneously**, often split by geography or load.  
This is the hardest architecture to implement but provides the strongest availability.

---

## **26.3.1 Requirements for Active/Active**

- **Stateless services** globally deployable
    
- **Global Load Balancing** (GCLB)
    
- **Service mesh multi-cluster endpoint aggregation**
    
- **Distributed data system** (Spanner, Bigtable, or custom CRDT-based)
    
- **Global SLO monitoring**
    
- **Consistent routing behavior**
    

---

## **26.3.2 GCLB Example for Multi-Region**

Frontend:

```yaml
apiVersion: networking.gke.io/v1
kind: MultiClusterIngress
metadata:
  name: checkout-ingress
spec:
  template:
    spec:
      backend:
        serviceName: checkout
        servicePort: 80
```

GCLB automatically directs traffic to nearest healthy region.

---

## **26.3.3 Multi-Cluster Istio Failover**

DestinationRule:

```yaml
trafficPolicy:
  loadBalancer:
    localityLbSetting:
      enabled: true
      failover:
        us-central1: europe-west1
```

Mesh automatically routes across clusters/regions when local endpoints fail.

---

## **26.3.4 Global Deployment Pattern**

Deploy to multiple regions:

```bash
kubectl --context=gke_us-central1 apply -f deploy.yaml
kubectl --context=gke_europe-west1 apply -f deploy.yaml
```

Keep versions synced:

- CI/CD pipeline targets both clusters
    
- GitOps allows consistent configuration
    

---

## **26.3.5 Multi-Region Failure Simulation**

Turn off workloads in one region:

```bash
kubectl --context=gke_us-central1 scale deployment checkout --replicas=0
```

Test:

- Do requests shift to EU region?
    
- Does GCLB remove unhealthy region?
    
- Does mesh EDS update endpoints promptly?
    

---

## **26.3.6 Multi-Region Pitfalls**

- Global split-brain scenarios
    
- Stateful services unable to replicate cross-region
    
- DNS caching delaying failover
    
- Cross-region latency spikes due to accidental routing
    
- Traffic imbalance if locality weighting misconfigured
    

---

# **26.4 Stateful Workload Considerations**

Stateful workloads require special handling for HA.  
Stateless workloads scale freely; stateful workloads do not.

---

## **26.4.1 Golden Rules for Stateful HA**

1. **Avoid state in-region where possible**
    
2. **Use managed distributed systems**
    
3. **Design for region-level failure semantics**
    
4. **Understand consistency trade-offs**
    
5. **Prefer asynchronous replication over synchronous across continents**
    

---

## **26.4.2 StatefulSets and Zone Failure**

StatefulSets maintain stable identity but:

- pods pinned to volumes
    
- cannot move between zones automatically
    
- PDs are zonal unless using Regional PDs
    

Use **Regional Persistent Disk**:

```bash
gcloud compute disks create db-disk \
  --type=pd-balanced \
  --region=us-central1 \
  --replica-zones=us-central1-a,us-central1-b
```

Attach via PersistentVolume:

```yaml
persistentVolumeReclaimPolicy: Retain
gcePersistentDisk:
  pdName: db-disk
```

---

## **26.4.3 Databases (Cloud SQL, Spanner, etc.)**

### **Cloud SQL**

- Primary in one zone
    
- Automatic failover replica
    
- Regional level HA not fully multi-active
    
- Use for traditional apps (Postgres/MySQL)
    

### **Spanner**

- True multi-region synchronous commit
    
- Globally distributed
    
- Ideal for multi-active global platforms
    

### **Bigtable**

- Multi-cluster routing, regional replication
    
- Strong for read-heavy workloads
    

---

## **26.4.4 Caching Layer Considerations**

### Redis:

- For HA: use **MemoryStore Tier-1 (Redis Enterprise)**
    
- For multi-region: use Redis Global Replication
    

### Memcached:

- Stateless — deploy regionally
    
- Do not replicate across regions
    

---

## **26.4.5 Stateful Anti-Patterns**

- Running Postgres on GKE with zonal PD → instant outage after zone loss
    
- Relying on StatefulSet to handle HA automatically → it does not
    
- Using synchronous cross-region replication → severe latency
    
- Treating Redis as durable store → data loss
    

---

# **Chapter 27 — Disaster Recovery & Failover Runbooks**

_(Expanded with senior-level clarity, real-world procedures, gcloud/kubectl examples, DR simulation steps, and actionable runbook patterns.)_

Disaster Recovery (DR) ensures a platform can **survive catastrophic regional failures**, **recover critical services**, and **meet business continuity objectives**.  
This chapter provides a pragmatic DR framework, recovery procedures, automation patterns, and testing guidance for GKE, GCP Networking, and platform services.

---

# **27.1 RPO/RTO Framework**

RPO (Recovery Point Objective) and RTO (Recovery Time Objective) define **how much data loss** and **how much downtime** your business tolerates during a disaster.

---

## **27.1.1 RPO — Recovery Point Objective**

**RPO = Max acceptable amount of data the business can lose**  
(e.g., 5 minutes, 1 hour).

Examples:

- Payment records: RPO = 0 (strong consistency)
    
- Logging/analytics: RPO = 15–60 minutes
    
- Session cache: RPO = high (data can be lost)
    

### Real-world mapping:

|Component|Typical RPO|
|---|---|
|Spanner|0 (globally consistent)|
|Cloud SQL|seconds–minutes|
|Redis (cache)|unlimited (non-durable)|
|GCS storage|near zero|

---

## **27.1.2 RTO — Recovery Time Objective**

**RTO = Max acceptable downtime after failure**

Examples:

- Checkout API: RTO = < 5 minutes
    
- Backoffice admin tools: RTO = 1–4 hours
    
- Batch ETL systems: RTO = 24 hours
    

---

## **27.1.3 Setting RPO/RTO with Business Input**

Steps:

1. Classify services as **Tier 0**, **1**, **2**, **3**
    
2. Assign RPO/RTO constraints to each tier
    
3. Validate storage/replication architecture meets RPO
    
4. Validate deployment model meets RTO requirements
    
5. Define DR playbooks and automations
    

---

## **27.1.4 Common RPO/RTO Pitfalls**

- RPO/RTO not tied to architectural reality
    
- Same RTO assigned to all services → unrealistic budgets
    
- No documented owner for DR objectives
    
- RTO ignores time to restore _dependencies_
    

---

# **27.2 Backup Strategy**

Backups protect business data when stateful systems fail or data is corrupted.

---

## **27.2.1 Backup Categories**

### **1. Application / Database Backups**

- Cloud SQL automated and on-demand backups
    
- Spanner backup/restore
    
- Cassandra/Elastic snapshots (self-managed)
    

### **2. Storage Backups**

- GCS versioning
    
- Filestore snapshots
    
- Artifact Registry backups
    

### **3. Configuration Backups**

- Terraform state (remote backend w/ versioning)
    
- GitOps repos (mirror to offsite)
    
- Kubernetes manifests (exported from Git)
    

---

## **27.2.2 Cloud SQL Backup Strategy**

Enable automated backups:

```bash
gcloud sql instances patch prod-db \
  --backup-start-time=03:00 \
  --enable-bin-log
```

Create on-demand backup:

```bash
gcloud sql backups create --instance=prod-db
```

---

## **27.2.3 GCS Storage Versioning**

Enable versioning:

```bash
gsutil versioning set on gs://prod-storage
```

Restore a specific version:

```bash
gsutil cp gs://prod-storage/file.txt#123 ./restored.txt
```

---

## **27.2.4 GKE Configuration Snapshots**

Store cluster state declaratively:

- GitOps repos
    
- Helm chart versions
    
- Kustomize overlays
    

Export cluster resources as secondary backup:

```bash
kubectl get all --all-namespaces -o yaml > gke-backup-$(date +%F).yaml
```

---

## **27.2.5 Backup Verification — Critical**

Backups without verification = **not backups**.

Verification steps:

- Monthly automated restore tests
    
- Check data integrity
    
- Validate restored cluster matches expected configs
    

---

## **27.2.6 Common Backup Pitfalls**

- Backups stored in same region as primary → both lost
    
- Backups without encryption → compliance risk
    
- Relying on snapshots for DR → only useful for hardware failure
    
- No restore testing → backups silently corrupted
    

---

# **27.3 Cluster Rebuild Procedures**

A DR event may require rebuilding a cluster from scratch.

This section provides an actionable runbook.

---

## **27.3.1 Step 1 — Create Replacement Cluster**

Example: recreate GKE cluster in DR region.

```bash
gcloud container clusters create prod-cluster \
  --region europe-west1 \
  --node-locations europe-west1-b,europe-west1-c \
  --num-nodes=3
```

---

## **27.3.2 Step 2 — Reinstall Base Components**

Install core platform dependencies:

- Istio / Service Mesh
    
- CNI plugin
    
- Ingress gateways
    
- Observability stack
    
- Argo CD / Flux (if using GitOps)
    

Example: install Istio:

```bash
istioctl install -f istio-values.yaml
```

---

## **27.3.3 Step 3 — Restore Configuration (GitOps)**

With GitOps, restoring a cluster is:

```bash
argocd app sync --all
```

Or with Flux:

```bash
flux reconcile kustomization cluster-config
```

If not GitOps:

- apply Terraform
    
- apply Kubernetes manifests manually
    

---

## **27.3.4 Step 4 — Restore Stateful Components**

Restore Cloud SQL database:

```bash
gcloud sql instances patch prod-db --backup-id=12345
```

Restore PersistentVolumes (if regionally replicated):

- attach regional PD
    
- recreate PVCs
    

---

## **27.3.5 Step 5 — Reconfigure DNS / Load Balancer**

Point traffic to the DR region:

```bash
gcloud compute backend-services update \
  --region europe-west1 \
  --global-health-checks prod-backend
```

Or shift traffic with Cloud DNS:

- Lower TTL
    
- Update A/AAAA records
    
- Validate LB propagation
    

---

## **27.3.6 Cluster Rebuild Pitfalls**

- Inconsistent Git repos → unreproducible cluster
    
- Missing secrets → broken deployments
    
- Manual manifests not included in Git → drift
    
- Stateful workloads tied to zonal PDs → cannot restore in DR region
    
- Wrong mesh version → workloads have incompatible sidecars
    

---

# **27.4 Failover Automation**

Failover must be **predictable**, **fast**, and ideally **automated**.

---

## **27.4.1 Types of Failover**

### **1. Manual Failover**

- Operator-triggered
    
- Suitable for non-critical services
    

### **2. Semi-Automated Failover**

- Alerts + runbook execution
    
- Human approval to trigger
    
- Best for medium-critical workloads
    

### **3. Fully Automated Failover**

- System detects regional outage
    
- Shifts traffic automatically
    
- Good for highly reliable, globally distributed systems
    

---

## **27.4.2 Failover with Cloud Load Balancing**

GCLB detects unhealthy backends automatically.

Backend health check example:

```yaml
apiVersion: cloud.google.com/v1
kind: BackendConfig
metadata:
  name: hc
spec:
  healthCheck:
    requestPath: /healthz
    port: 8080
```

If an entire region fails:

- GCLB stops sending traffic
    
- Shifts to healthy region automatically
    

---

## **27.4.3 Failover Using Istio Locality Failover**

```yaml
trafficPolicy:
  loadBalancer:
    localityLbSetting:
      failover:
        us-central1: europe-west1
        europe-west1: us-central1
```

Envoy shifts traffic when:

- endpoints unhealthy
    
- region unreachable
    

---

## **27.4.4 Failover Automation with Cloud Functions / Cloud Run**

Trigger failover on event:

```bash
gcloud functions deploy failover-trigger \
  --entry-point=TriggerFailover \
  --runtime=go120 \
  --trigger-event-filters="type=google.cloud.pubsub.topic.v1.messagePublished"
```

Common triggers:

- high error budget burn
    
- severe latency
    
- zone or region outage events
    
- Cloud SQL failover events
    

---

## **27.4.5 Runbook Requirements for Failover**

Runbook must include:

- Preconditions
    
- Health checks
    
- Exact commands
    
- Rollback plan
    
- Escalation contacts
    
- Time-boxed steps
    
- SLAs for execution
    

---

## **27.4.6 Failover Anti-Patterns**

- Failover without understanding root cause
    
- DNS failover with high TTL → multi-hour delays
    
- Over-automation → flapping between regions
    
- Failing over databases without checking replication lag
    
- No rollback path → stuck in DR region
    

---

# **27.5 DR Testing**

Testing validates DR plans under realistic conditions.  
Testing must be **regular**, **controlled**, and **measured**.

---

## **27.5.1 Types of DR Exercises**

### **1. Tabletop Exercises**

- Simulated over video call
    
- Review runbooks
    
- No production changes
    

### **2. Game Days**

Real traffic + real failures:

- Kill a zone
    
- Disable Cloud SQL primary
    
- Break Ingress Gateway
    
- Drop a region’s node pool
    

### **3. Blackhole Tests**

Simulate network partition:

```bash
iptables -A INPUT -s 35.191.0.0/16 -j DROP
```

---

## **27.5.2 DR Validation Checklist**

- Can restore cluster in DR region?
    
- Can restore stateful DB?
    
- Load balancer routes traffic away from broken region?
    
- Prometheus, tracing, logs restored?
    
- Mesh routing correct after failover?
    
- DNS propagation time meets RTO?
    

---

## **27.5.3 DR Metrics**

Track:

- Recovery time
    
- Data loss
    
- Steps requiring manual intervention
    
- Outdated runbook steps
    
- Incidents discovered during test
    

---

## **27.5.4 Making DR Tests Safe**

- Test in staging first
    
- Use feature flags to route limited test traffic
    
- Monitor error budget burn
    
- Abort conditions clearly defined
    

---

## **27.5.5 Common DR Testing Pitfalls**

- No test of restoring Terraform state → environment unrecoverable
    
- Relying on one engineer with tribal knowledge
    
- Not simulating _full_ region outage
    
- Using incomplete backups
    
- Mesh control plane failure not tested
    

---

# **Chapter 28 — Chaos Engineering & Incident Simulations**

_(Expanded with senior-level clarity, Istio/GKE examples, fault injection policies, safe game day patterns, and observability-driven validation techniques.)_

Chaos engineering is a disciplined practice of injecting controlled failures into a system to validate resilience, reveal blind spots, and ensure teams can respond effectively to incidents.  
This chapter covers fault injection, running game days, and validating observability pipelines before real-world failures occur.

---

# **28.1 Fault Injection**

Fault injection introduces controlled failures—latency, aborts, network drops—into a service or dependency to validate resilience patterns (timeouts, retries, circuit breaking, failover).

Istio provides native L7 fault injection via **VirtualService** rules.

---

## **28.1.1 Use Cases for Fault Injection**

Fault injection simulates:

- Slow downstream dependencies
    
- HTTP 500/503 storms
    
- Network delays
    
- Partial outages
    
- Canary regressions
    
- Retries amplifying traffic
    
- Cascading failures
    

---

## **28.1.2 Latency Injection Example**

Simulate slow downstream service (e.g., `payments` slow for some users):

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: checkout-fault
spec:
  hosts:
  - payments
  http:
  - fault:
      delay:
        percentage:
          value: 20              # 20% of requests
        fixedDelay: 5s           # introduce 5s delay
    route:
    - destination:
        host: payments
```

**What this tests:**

- Do upstream services time out correctly?
    
- Does retry budget amplify traffic?
    
- Does user experience degrade predictably?
    

---

## **28.1.3 HTTP Abort Injection Example**

Return HTTP 503 errors—for testing circuit breakers or outlier detection:

```yaml
http:
- fault:
    abort:
      percentage:
        value: 30        # 30% requests
      httpStatus: 503
  route:
  - destination:
      host: catalog
```

**What this tests:**

- Circuit breaker activation
    
- Graceful degradation
    
- Error-rate alerting
    
- Latency behavior during retry storms
    

---

## **28.1.4 Combined Latency + Abort Testing**

```yaml
fault:
  delay:
    fixedDelay: 3s
    percentage: { value: 50 }
  abort:
    httpStatus: 500
    percentage: { value: 10 }
```

Used to simulate:

- partial outages
    
- misbehaving dependencies
    
- network jitter + error bursts
    

---

## **28.1.5 Cluster-Level Chaos (Pod Kill, Node Kill)**

### Kill a pod:

```bash
kubectl delete pod <pod-name>
```

### Evict a node (simulate node failure):

```bash
kubectl drain <node> --ignore-daemonsets --delete-emptydir-data --force
```

### Terminate a zone (staging only):

Use GKE NodePool to disable a zone:

```bash
gcloud container clusters update prod --node-pool default --node-locations us-central1-b
```

---

## **28.1.6 Common Fault Injection Pitfalls**

- Running fault injection in production without guardrails
    
- Forgetting to remove VirtualService fault rules afterward
    
- Injecting faults into shared dependencies → cascading outages
    
- Lack of coordination with observability teams
    
- No circuit breakers → tests cause real outages
    

---

# **28.2 Game Days**

Game days simulate real incident scenarios, combining technical failures with team processes, observability interpretation, and communication patterns.

---

## **28.2.1 Objectives of Game Days**

- Validate operational readiness
    
- Test incident response workflows
    
- Validate SLO alerting and dashboards
    
- Discover hidden cross-region dependencies
    
- Ensure DR failover works under load
    
- Identify bottlenecks in playbooks
    

---

## **28.2.2 Game Day Types**

### **1. Technical Game Days**

Focus: system resilience.  
Simulate:

- increased latency
    
- pod failures
    
- node zonal outages
    
- regional failures
    
- LB health check issues
    
- identity/auth failures
    
- database degraded performance
    

### **2. Operational Game Days**

Focus: team resilience.  
Simulate:

- alert storms
    
- on-call engineer handoff
    
- communication failures
    
- escalations to management
    

### **3. Business-Level Game Days**

Focus: impact on business flows.  
Simulate:

- checkout failures
    
- degraded payment systems
    
- broken login flows
    

---

## **28.2.3 Game Day Preparation**

Define:

- scenario scope
    
- expected impact
    
- preconditions
    
- rollback plan
    
- success criteria
    
- observability dashboards to watch
    
- timeline
    
- owner + facilitator + scribe
    

---

## **28.2.4 Example Game Day Scenario: “Payments Latency Spike”**

**Setup (Istio fault injection):**

```yaml
fault:
  delay:
    fixedDelay: 1s
    percentage: { value: 60 }
```

**Expected Observations:**

- Upstream checkout service retries spike
    
- circuit breaker trips
    
- error budget burn increases
    
- P99 latency skyrockets
    
- dashboards show red lines
    

**Success Criteria:**

- Alerts fire within 2 minutes
    
- On-call acknowledges
    
- Service degrades gracefully
    
- Team executes mitigation playbook
    

---

## **28.2.5 Regional Failure Game Day**

- Disable all nodes in region A
    
- Validate GCLB shifts traffic
    
- Validate mesh locality failover
    
- Validate SLO burn-rate alerting
    
- Validate runbook execution
    

---

## **28.2.6 Running Safe Game Days**

Rules:

- Always start in staging
    
- Limit blast radius
    
- Use feature flags to control scope
    
- Define abort conditions
    
- Never test high-risk systems without management approval
    

---

## **28.2.7 Game Day Anti-Patterns**

- Running chaos tests during peak business hours
    
- No rollback plan → real outage
    
- Not capturing data afterwards
    
- Lack of communication with support teams
    
- Not revisiting or updating runbooks after findings
    

---

# **28.3 Observability Validation**

Chaos experiments and game days are useless without **effective observability**.  
Every failure mode must be detectable, diagnosable, and traceable.

---

## **28.3.1 What Observability Validation Means**

Validating observability ensures:

- dashboards show the right signals
    
- alerts trigger early and accurately
    
- logs reveal root cause
    
- traces show dependency paths
    
- metrics show correct latency buckets
    
- mesh-level telemetry works under load
    

---

## **28.3.2 Metrics Validation Checklist**

During a chaos test:

- **Latency histograms** reflect spikes
    
- **Success rate** charts detect anomalies
    
- **Retries** increase appropriately
    
- **Circuit breaker ejections** are visible
    
- **Error budget burn** reacts within minutes
    

### PromQL example for success rate:

```promql
sum(rate(istio_requests_total{response_code!~"5.."}[5m])) 
/
sum(rate(istio_requests_total[5m]))
```

### Retry count:

```promql
sum(rate(istio_requests_total{response_flags=~"URX|UTX"}[5m]))
```

---

## **28.3.3 Logs Validation Checklist**

Check:

- pods emit structured logs
    
- Envoy access logs capture L7 latency
    
- stack traces propagate
    
- correlate logs with trace IDs
    

```bash
kubectl logs deploy/checkout | grep TRACE_ID
```

---

## **28.3.4 Traces Validation Checklist**

Look for:

- downstream service spans
    
- nested spans indicating retry loops
    
- long spans for latency injection
    
- 5xx spans for abort tests
    
- proper propagation of `x-request-id`, `b3`, or W3C TraceContext
    

---

## **28.3.5 Exemplars Validation**

Ensure latency panels include clickable trace IDs.

Grafana panel snippet:

```json
{
  "exemplars": { "enabled": true },
  "targets": [
    {
      "expr": "histogram_quantile(0.99, sum(rate(istio_request_duration_seconds_bucket[5m])) by (le))"
    }
  ]
}
```

---

## **28.3.6 Mesh Observability Validation**

Ensure:

- Envoy emits metrics
    
- xDS config updates propagate
    
- mTLS handshake failures appear in metrics
    
- Locality routing logs appear correctly
    

---

## **28.3.7 Common Observability Pitfalls**

- No dashboards for mesh-level failures
    
- Logging disabled due to volume → blind spots
    
- No span linking across asynchronous systems
    
- Missing retries in metrics → false sense of resilience
    
- No idle or baseline traffic → cannot detect anomalies
    

---

# **Chapter 29 — Safe Deployments & Blast Radius Control**

_(Expanded with senior-level clarity, real-world Istio, Kubernetes, GitOps, CI/CD, and multi-region rollout patterns. Includes YAML, gcloud, and kubectl examples.)_

Safe deployment practices ensure new versions ship **gradually**, **observably**, and **reversibly**—minimizing user impact even in the presence of defects.  
This chapter explains progressive delivery, rollback mechanics, multi-region deployment waves, and feature flagging strategy for critical workloads.

---

# **29.1 Progressive Delivery**

Progressive delivery introduces changes **incrementally**, watching metrics/alerts at each step before increasing traffic.

Common strategies:

- Canary releases
    
- Blue/Green deployments
    
- Traffic splitting with weights
    
- Automated rollouts (e.g., Argo Rollouts, Flagger)
    
- Per-region or per-tenant rollout waves
    

---

## **29.1.1 Canary Deployment (Manual with Istio)**

Start with a small portion of traffic.

### **Deployment Manifests**

Two versions side-by-side:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: checkout-v1
spec:
  replicas: 5
  selector:
    matchLabels:
      app: checkout
      version: v1
```

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: checkout-v2
spec:
  replicas: 1
  selector:
    matchLabels:
      app: checkout
      version: v2
```

---

### **DestinationRule with Subsets**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: DestinationRule
metadata:
  name: checkout
spec:
  host: checkout
  subsets:
  - name: v1
    labels: { version: v1 }
  - name: v2
    labels: { version: v2 }
```

---

### **VirtualService Traffic Split Example**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: checkout-vs
spec:
  hosts:
  - checkout
  http:
  - route:
    - destination:
        host: checkout
        subset: v1
      weight: 95
    - destination:
        host: checkout
        subset: v2
      weight: 5
```

Increase weight as metrics remain healthy.

---

## **29.1.2 Automated Canary (Argo Rollouts)**

Rollout YAML:

```yaml
apiVersion: argoproj.io/v1alpha1
kind: Rollout
metadata:
  name: checkout
spec:
  replicas: 6
  strategy:
    canary:
      steps:
      - setWeight: 5
      - pause: { duration: 5m }
      - setWeight: 20
      - pause: { duration: 10m }
      - setWeight: 50
      - pause: { duration: 10m }
      analysis:
        templates:
        - templateName: error-rate
```

Benefits:

- Automated analysis
    
- Automatic rollback
    
- Fine-grained traffic splitting
    

---

## **29.1.3 Blue/Green Deployment**

Two full environments: **blue (active)** and **green (candidate)**.

Switch using VirtualService:

```yaml
http:
- route:
  - destination:
      host: checkout
      subset: green
```

Cutover is instant and reversible.

---

## **29.1.4 Progressive Delivery Pitfalls**

- Releasing to 1% traffic but sampling only total metrics
    
- Not isolating canary metrics
    
- Canary traffic too low → blind to errors
    
- No automated rollback triggers
    
- Updating deployments before traffic shifts back to stable
    

---

# **29.2 Rollback Strategy**

A deployment strategy is only as safe as its rollback mechanism.

Rollback principles:

- Must be **fast**
    
- Must be **atomic**
    
- Must be **observable**
    
- Must be **scripted**
    

---

## **29.2.1 Rollback with Kubernetes Deployments**

Rollback command:

```bash
kubectl rollout undo deployment checkout
```

Check status:

```bash
kubectl rollout status deployment checkout
```

---

## **29.2.2 Rollback with Istio Traffic Shift**

Rollback VirtualService to 100% v1:

```yaml
route:
- destination: { host: checkout, subset: v1 }
  weight: 100
- destination: { host: checkout, subset: v2 }
  weight: 0
```

---

## **29.2.3 Rollback in Argo Rollouts**

```bash
kubectl argo rollouts abort checkout
```

or revert Git:

```bash
git revert <bad commit>
git push
```

Argo will automatically sync.

---

## **29.2.4 Choosing Rollback Thresholds**

Examples:

- Error rate > 1% sustained for 5 minutes
    
- P95 latency > 400ms
    
- CPU throttling spikes
    
- Error budget burn rate > 10x
    

These thresholds should match SLO-driven burn rate alerts.

---

## **29.2.5 Rollback Anti-Patterns**

- Rolling back app but forgetting config changes
    
- Removing canary before diagnosing → loss of artifacts
    
- Not rolling back mesh routing when deployment undone
    
- No “stop-the-world” during severe regressions
    

---

# **29.3 Multi-Region Deployment Waves**

Safe global rollouts require **deploying region-by-region**, limiting the blast radius of defects.

---

## **29.3.1 Why Deployment Waves Matter**

Failures confined to:

- 1 region
    
- subset of users
    
- internal beta traffic
    
- friendly region before global traffic
    

Avoid:

- global outages
    
- waking all on-calls
    
- global rollback storm
    

---

## **29.3.2 Recommended Deployment Wave Strategy**

### **Wave 0 — Internal Only**

Small internal region such as:

- us-west2
    
- staging-in-prod subset
    
- developer namespace
    

### **Wave 1 — Secondary Regions**

Deploy to:

- one small-production region
    
- low RPS region
    

### **Wave 2 — Majority Regions**

Deploy to:

- 50–80% of traffic regions
    

### **Wave 3 — High-Traffic / Critical Regions**

Deploy to:

- us-central1
    
- europe-west1
    

Each wave should include:

- 5–30 minute bake period
    
- SLO/SLA validation
    
- synthetic monitoring
    
- canary metrics
    

---

## **29.3.3 GitOps Multi-Region Wave Example**

Flux supports per-cluster Kustomizations:

```
clusters/
  us-west2/
  asia-east1/
  us-central1/
```

Deploy region-by-region:

```bash
flux reconcile kustomization us-west2
```

---

## **29.3.4 Cloud Deploy (GCP) Multi-Region Example**

pipeline.yaml:

```yaml
targets:
- name: wave-0
- name: wave-1
- name: wave-2
```

Run wave:

```bash
gcloud deploy releases promote --release wave1-release
```

---

## **29.3.5 Mesh-Aware Routing During Waves**

During upgrades:

- use region-local routing
    
- isolate new versions to small region
    
- enforce subset routing to canary versions
    

Example VirtualService:

```yaml
http:
- match:
  - headers:
      x-region:
        exact: "us-west2"
  route:
  - destination:
      host: checkout
      subset: v2   # test version only in us-west2
```

---

## **29.3.6 Multi-Region Rollout Pitfalls**

- Deploying to high-traffic region first
    
- No rollback sync across clusters
    
- Version skew between regions leading to protocol mismatch
    
- Stateful workload inconsistency (schema drift)
    
- Mesh gateways inconsistent across regions
    

---

# **29.4 Feature Flag Safety**

Feature flags allow turning features on/off without deploying new code.

They enable:

- canary targeting
    
- ramp-ups
    
- kill switches
    
- gradual personalization
    
- A/B tests
    
- regional control
    

---

## **29.4.1 Feature Flag Types**

|Type|Description|
|---|---|
|Boolean|On/off|
|Percentage|% rollout|
|Gradual|time-based|
|Conditional|user attributes|
|Multi-variant|A/B/N experiments|
|Kill switch|immediate shutdown|

---

## **29.4.2 Feature Flag Implementation (Go + OpenFeature)**

Example usage:

```go
client := openfeature.NewClient("checkout")
value, err := client.BooleanValue(ctx, "enable-new-pricing", false, nil)
```

Configuration in flag backend:

```json
{
  "flags": {
    "enable-new-pricing": {
      "state": "enabled",
      "rollout": {
        "percentage": 10
      }
    }
  }
}
```

---

## **29.4.3 Kill Switch Pattern**

If dependency fails, disable feature:

```go
if dependencyErrorRate > 0.05 {
    flags.Disable("checkout-recommendations")
}
```

---

## **29.4.4 Region-Based Feature Flagging**

Useful for multi-region waves:

```json
{
  "targeting": {
    "us-west2": "enabled",
    "us-central1": "disabled"
  }
}
```

---

## **29.4.5 Feature Flag Observability**

Measure:

- % of users in each variant
    
- error correlation with variant
    
- latency differences
    
- variant-specific SLOs
    

---

## **29.4.6 Feature Flag Pitfalls**

- Flags become permanent → configuration sprawl
    
- Flags not documented → tribal knowledge
    
- Flags coupled to code version → inconsistent behavior
    
- Using feature flags as rollout mechanism without guardrails
    
- Breaking schema: enabling features depending on DB migrations prematurely
    

---

# **Chapter 30 — Zero-Trust Networking & Segmentation**

_(Expanded with senior-level clarity, GCP + Kubernetes + Mesh examples, IAP patterns, segmentation techniques, and real-world misconfiguration pitfalls.)_

Zero Trust Networking (ZTN) eliminates the assumption that internal networks are safe.  
Instead, _every request must be authenticated, authorized, and encrypted_, regardless of source or location.

GKE, GCP Networking, and Istio/Envoy provide a strong foundation for implementing ZTN in modern cloud platforms.

---

# **30.1 Zero-Trust Principles**

Zero Trust shifts from a “castle-and-moat” security model to a model where _no request is inherently trusted_—even inside the VPC or Kubernetes cluster.

---

## **30.1.1 Core Principles**

### **1. Never Trust, Always Verify**

Every request must be authenticated and authorized:

- mTLS between services
    
- JWT for user/API identity
    
- service accounts for workload identity
    

### **2. Least Privilege Access**

Grant only what is needed:

- IAM allowlists
    
- Network firewall min-rules
    
- RBAC per workload
    

### **3. Assume Breach**

Design defenses such as:

- segmentation
    
- strong identity
    
- audit logging
    
- rate limiting
    
- anomaly detection
    

### **4. Continuous Verification**

Validate identities and permissions on:

- every request
    
- every connection
    
- every API call
    

### **5. Minimal & Observable Attack Surface**

All exposed APIs must be:

- visible
    
- mapped
    
- monitored
    
- protected
    

---

## **30.1.2 Zero Trust Applied to Kubernetes**

In Kubernetes:

- **Service accounts** identify workloads
    
- **NetworkPolicy** restricts pod traffic
    
- **Istio mTLS** enforces cryptographic identity
    
- **AuthorizationPolicy** enforces request-level RBAC
    
- **OPA/Gatekeeper** enforces security rules
    
- **IAP or Identity-Aware features** protect external access
    

---

## **30.1.3 Zero-Trust Workflow Diagram**

```
Request → TLS/mTLS → Authenticate → Authorize → Validate Policy → Allow/Block
```

---

## **30.1.4 Enforcing mTLS in Istio (Mesh-Wide)**

```yaml
apiVersion: security.istio.io/v1beta1
kind: PeerAuthentication
metadata:
  name: mesh-default
spec:
  mtls:
    mode: STRICT
```

---

## **30.1.5 Common Zero-Trust Pitfalls**

- Allowing fallback to plaintext traffic
    
- Overly broad access (e.g., allow all traffic in NetworkPolicy)
    
- Misconfigured service accounts → unexpected SPIFFE IDs
    
- Relying solely on perimeter firewalls → no pod-level controls
    
- Logging disabled → invisible attack paths
    

---

# **30.2 Network Segments**

Network segmentation limits the “blast radius” of a breach by separating workloads into isolated trust zones.

Segmentation in GCP/GKE occurs across:

- **VPCs**
    
- **Subnets**
    
- **firewalls**
    
- **GKE namespaces**
    
- **NetworkPolicy**
    
- **Istio AuthZ policies**
    

---

## **30.2.1 Segmentation Models**

### **1. VPC-Level Segmentation (Strongest Boundary)**

Use separate VPCs for:

- prod
    
- non-prod
    
- staging
    
- partner environments
    
- sensitive workloads (PCI, HIPAA)
    

### **2. Project-Based Segmentation**

Use GCP projects as logical boundaries:

- IAM isolation
    
- billing separation
    
- resource scoping
    
- VPC SC perimeters
    

### **3. Namespace Segmentation Inside Clusters**

Namespaces provide:

- RBAC boundaries
    
- NetworkPolicy scopes
    
- quota scoping
    
- mesh traffic policy scoping
    

### **4. Pod-Level Microsegmentation**

Via:

- Kubernetes NetworkPolicy
    
- Cilium or Calico policies
    
- Istio authorization policies
    

---

## **30.2.2 Kubernetes NetworkPolicy Example**

Allow checkout → payments only:

```yaml
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  namespace: payments
  name: payments-allow-checkout
spec:
  podSelector:
    matchLabels:
      app: payments
  ingress:
  - from:
    - namespaceSelector:
        matchLabels:
          name: checkout
    ports:
    - protocol: TCP
      port: 8080
```

---

## **30.2.3 Istio AuthorizationPolicy Example (L7 Segmentation)**

```yaml
apiVersion: security.istio.io/v1beta1
kind: AuthorizationPolicy
metadata:
  name: payments-authz
  namespace: payments
spec:
  rules:
  - from:
    - source:
        principals:
        - "spiffe://cluster.local/ns/checkout/sa/checkout-sa"
    to:
    - operation:
        methods: ["POST"]
        paths: ["/process"]
```

This enforces:

- authenticated identity
    
- namespace-level restriction
    
- HTTP method enforcement
    
- path-based routing security
    

---

## **30.2.4 VPC Firewall Segmentation Example (GCP)**

Allow only specific subnet to reach service:

```bash
gcloud compute firewall-rules create allow-checkout \
  --direction=INGRESS \
  --network=prod-vpc \
  --source-ranges=10.10.10.0/24 \
  --target-tags=payments-backend \
  --allow tcp:8080
```

---

## **30.2.5 Segmentation Anti-Patterns**

- One giant flat VPC → no boundaries
    
- Overuse of Namespace segmentation without NetworkPolicies → ineffective
    
- Allowing wildcard "*" traffic in mesh AuthorizationPolicy
    
- Using pod labels that change dynamically → breaking policies
    
- Shared service accounts → identity confusion
    

---

# **30.3 Perimeter Reduction**

Traditional perimeter models assume internal network = trusted.  
Zero Trust reduces external attack surface and internal lateral movement capabilities.

---

## **30.3.1 Techniques for Perimeter Reduction**

### **1. Remove Internal “Implicit Trust”**

Treat internal traffic as untrusted.

How:

- enforce mTLS
    
- apply NetworkPolicies to all namespaces
    
- restrict east-west traffic
    

---

### **2. Minimize Public Endpoints**

Use:

- Private Service Connect
    
- Internal load balancers
    
- Private GKE control plane
    
- VPC-SC perimeters
    
- Identity-Aware Proxy
    

---

### **3. Tighten IAM Scopes**

Ensure each service account has:

- least-privilege roles
    
- no broad editor/admin roles
    
- workload identity (not static keys)
    

---

### **4. Minimize Cross-Project Access**

Prefer:

- per-project services
    
- Shared VPC for standardized boundary
    
- org-level policies to restrict service activation
    

---

## **30.3.2 Example: Lock Down Public Ingress**

Disable external load balancer creation:

```yaml
apiVersion: constraints.gatekeeper.sh/v1beta1
kind: GCPHttpsOnly
metadata:
  name: prevent-public-lbs
spec:
  match:
    kinds:
      - apiGroups: ["networking.gke.io"]
        kinds: ["Ingress"]
```

---

## **30.3.3 Example: Private GKE Control Plane**

```bash
gcloud container clusters create private-cluster \
  --enable-private-nodes \
  --enable-private-endpoint \
  --master-ipv4-cidr 172.16.0.0/28
```

Benefits:

- API server not public
    
- Nodes have no public IPs
    

---

## **30.3.4 Perimeter Reduction Pitfalls**

- Overly strict policies blocking critical internal traffic
    
- Developers bypassing restrictions with public tunnels
    
- Misconfigured private endpoints requiring complex routing
    
- Over-using VPC-SC beyond readiness → breaks mesh behavior
    
- Relying solely on perimeter instead of defense-in-depth
    

---

# **30.4 Identity-Aware Proxy (IAP)**

GCP Identity-Aware Proxy enforces authentication & authorization before traffic reaches apps.  
It is a core Zero-Trust control for web apps, internal admin tools, and GKE workloads.

---

## **30.4.1 What IAP Does**

IAP provides:

- Google-managed authentication
    
- OAuth2 token issuance
    
- fine-grained IAM authorization
    
- no need for VPN or bastion hosts
    
- ability to protect internal endpoints with zero-trust identity
    

---

## **30.4.2 IAP for GCE / GKE Ingress**

IAP integrates with HTTPS Load Balancing.

### **Enable IAP on Backend Service**

```bash
gcloud compute backend-services update backend-api \
  --iap=enabled,oauth2-client-id=CLIENT_ID,oauth2-client-secret=SECRET \
  --global
```

---

## **30.4.3 IAP with Kubernetes Ingress (HTTP LB)**

Kubernetes Ingress annotated:

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: admin-ingress
  annotations:
    cloud.google.com/app-protocols: '{"https":"HTTPS"}'
    networking.gke.io/auth-url: "https://iap.googleapis.com/v1/oauth/clients/CLIENT_ID"
```

---

## **30.4.4 IAP JWT Validation Inside Application**

Verify IAP identity token:

```bash
curl -H "Authorization: Bearer $TOKEN" \
  https://www.googleapis.com/oauth2/v3/certs
```

App-side validation (Go pseudo-code):

```go
idToken, err := verifier.Verify(ctx, token)
if err != nil {
    http.Error(w, "unauthorized", http.StatusUnauthorized)
    return
}
email := idToken.Email
```

---

## **30.4.5 IAP-Secured K8s Dashboard / Internal Tools**

Example for internal dashboard:

- no VPN
    
- no ingress allowlist
    
- identity-based access control
    

IAM permissions:

```bash
gcloud iam service-accounts add-iam-policy-binding \
  iap-access@yourproject.iam.gserviceaccount.com \
  --member=user:alice@example.com \
  --role=roles/iap.httpsResourceAccessor
```

---

## **30.4.6 IAP Pitfalls**

- Using IAP only for authentication → forgetting fine-grained authorization
    
- Not rotating OAuth client secrets
    
- Misconfigured HTTPS LB → IAP disabled silently
    
- External endpoints accidentally bypass IAP if a public IP is exposed
    
- No audit logging → blind to access patterns
    

---

# **Chapter 31 — IAM, Service Accounts & Workload Identity**

_(Expanded with senior-level clarity, practical patterns, GCP/GKE examples, YAML manifests, escalation risks, and secure-by-default best practices.)_

Identity is the foundation of all access control.  
In GCP, **IAM**, **service accounts**, and **workload identity** define _who_ can do _what_ on _which resource_.  
Poor identity design leads directly to privilege escalation, lateral movement, and catastrophic breaches.

This chapter provides a clear, pragmatic guide to designing least-privilege identity for cloud workloads.

---

# **31.1 IAM Roles & Design Patterns**

IAM controls _authorization_ to GCP APIs and resources.  
Designing IAM well is essential for Zero Trust, compliance, and least-privilege.

---

## **31.1.1 IAM Role Types**

|Type|Description|Example|
|---|---|---|
|**Primitive Roles**|Very broad, project-wide|`roles/viewer`, `roles/editor`, `roles/owner`|
|**Predefined Roles**|Fine-grained, service-specific|`roles/storage.objectViewer`|
|**Custom Roles**|Org-specific|`roles/myCompany.databaseBackup`|

**Rule:** Never use primitive roles for workloads.

---

## **31.1.2 IAM Design Principles**

### **1. Least Privilege**

Grant only the roles required for the task.

### **2. Separation of Duties**

Break access across:

- deployment
    
- runtime
    
- data
    
- admin
    

### **3. Privilege Boundaries via Projects**

IAM is easier when project boundaries match security boundaries.

### **4. Human and Machine Identity Separation**

Never use human accounts for automation.

---

## **31.1.3 Example: Least-Privilege Storage Access**

### Incorrect (Overly broad)

```bash
gcloud projects add-iam-policy-binding myproj \
  --member=serviceAccount:web@myproj.iam.gserviceaccount.com \
  --role=roles/storage.admin
```

### Correct

```bash
gcloud projects add-iam-policy-binding myproj \
  --member=serviceAccount:web@myproj.iam.gserviceaccount.com \
  --role=roles/storage.objectViewer
```

---

## **31.1.4 Example: Custom Role for Backup Process**

```yaml
title: "Backup Operator"
description: "Allows reading DB snapshots and writing to GCS"
stage: "GA"
includedPermissions:
- sql.backupRuns.get
- sql.backupRuns.list
- storage.objects.create
- storage.objects.get
```

Apply custom role:

```bash
gcloud iam roles create backupOperator \
  --project=myproj \
  --file=backup-operator-role.yaml
```

---

## **31.1.5 Common IAM Pitfalls**

- Using `roles/editor` for automation → unlimited privilege
    
- Putting IAM bindings on individual resources → fragmentation
    
- Using human GCP credentials for pipelines
    
- Forgetting to enforce IAM policy inheritance via folders
    
- Accidental privilege escalation via transitive roles (e.g., Pub/Sub → Cloud Functions → GCS)
    

---

# **31.2 Service Account Design**

Service accounts (SAs) represent **machine identity** for workloads, deployments, CI/CD systems, and automation.

---

## **31.2.1 Service Account Types**

|Type|Purpose|
|---|---|
|**User-managed SAs**|Apps, jobs, Kubernetes workloads|
|**GKE Node SAs**|Node agent access|
|**Compute default SA (avoid)**|Deprecated for security|
|**Cloud Build / GitHub Actions SAs**|CI/CD|
|**Data pipelines SAs**|ETL, batch|

---

## **31.2.2 Design Principles for SA Architecture**

### **1. One Workload → One Service Account**

Prevents identity mixing and lateral escalation.

### **2. No Shared Service Accounts**

Shared SAs make auditing impossible.

### **3. Namespace-Level Mapping (GKE)**

Use:

- namespace → service account mapping
    
- workload identity (no node SA leakage)
    

### **4. Forbid Keys on SAs**

Disable key creation wherever possible.

Org policy:

```bash
gcloud org-policies disable domainRestrictedSharing
```

Or block SA keys:

```bash
gcloud org-policies set-policy sa-no-keys.yaml
```

---

## **31.2.3 Assign SA to Kubernetes Deployment**

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: checkout
spec:
  template:
    spec:
      serviceAccountName: checkout-sa
```

ServiceAccount object:

```yaml
apiVersion: v1
kind: ServiceAccount
metadata:
  name: checkout-sa
  namespace: checkout
```

---

## **31.2.4 Grant IAM to the SA**

```bash
gcloud projects add-iam-policy-binding my-project \
  --member=serviceAccount:checkout-sa@my-project.iam.gserviceaccount.com \
  --role=roles/datastore.user
```

---

## **31.2.5 Enforce No SA-Key Generation**

Org policy example:

```yaml
constraint: constraints/iam.disableServiceAccountKeyCreation
listPolicy:
  allowAll: false
```

---

## **31.2.6 SA Design Anti-Patterns**

- Running all workloads using the **default** SA
    
- Attaching broad roles such as `roles/editor`
    
- Using long-lived JSON keys in CI/CD
    
- Reusing SAs across namespaces or teams
    
- Failing to rotate SAs after compromise
    

---

# **31.3 Workload Identity Federation**

Workload Identity Federation (WIF) allows workloads outside GCP (GitHub, GitLab, AWS, on-prem) to authenticate **without keys**, using federated identity tokens.

In GKE, Workload Identity replaces the old metadata server model.

---

## **31.3.1 Workload Identity on GKE**

This binds:

- Kubernetes service account (KSA)
    
- GCP IAM service account (GSA)
    

Mapping:

```bash
gcloud iam service-accounts add-iam-policy-binding \
  compute@myproj.iam.gserviceaccount.com \
  --role=roles/iam.workloadIdentityUser \
  --member="serviceAccount:myproj.svc.id.goog[checkout/checkout-sa]"
```

This means:

> “The Kubernetes SA `checkout-sa` in namespace `checkout` may impersonate the GCP SA `compute@`.”

---

## **31.3.2 Kubernetes Configuration**

```yaml
apiVersion: v1
kind: ServiceAccount
metadata:
  name: checkout-sa
  namespace: checkout
  annotations:
    iam.gke.io/gcp-service-account: compute@myproj.iam.gserviceaccount.com
```

---

## **31.3.3 How Workload Identity Works Internally**

1. Workload requests GCP access token
    
2. Kubelet provides signed KSA token
    
3. GCP STS API exchanges for GCP identity token
    
4. Workload uses GCP identity for API calls
    

This eliminates:

- node credential leakage
    
- metadata server spoofing
    
- static service account keys
    

---

## **31.3.4 Workload Identity Federation for CI/CD (Example: GitHub Actions)**

```yaml
permissions:
  id-token: write
  contents: read

steps:
- name: Authenticate to GCP
  uses: google-github-actions/auth@v1
  with:
    workload_identity_provider: projects/123/locations/global/workloadIdentityPools/gh/providers/github
    service_account: cicd@myproj.iam.gserviceaccount.com
```

This allows:

- keyless authentication
    
- short-lived credentials
    
- identity auditability
    

---

## **31.3.5 WIF Pitfalls**

- Incorrect audience (`aud`) → token rejected
    
- Mixing KSA and GSA incorrectly → identity mismatch
    
- Not granting `iam.workloadIdentityUser` → silent failures
    
- Using static keys “temporarily” → permanent security debt
    

---

# **31.4 Identity Escalation Risks**

Poor identity architecture exposes direct paths to **privilege escalation**, **lateral movement**, and **data exfiltration**.  
This section outlines common traps and mitigation techniques.

---

## **31.4.1 Service Account Impersonation Escalation**

If workload A can impersonate workload B, it can steal:

- all roles of B
    
- tokens of B
    
- access to all systems B can call
    

Fix:

- restrict `iam.serviceAccountTokenCreator`
    
- restrict `roles/iam.workloadIdentityUser` to exact KSA only
    
- do not use wildcard members
    

Bad:

```bash
--member="serviceAccount:myproj.svc.id.goog[*]"
```

Good:

```bash
--member="serviceAccount:myproj.svc.id.goog[checkout/checkout-sa]"
```

---

## **31.4.2 Excessive GCP IAM Roles**

Example dangerous roles:

- `roles/editor`
    
- `roles/owner`
    
- `roles/iam.serviceAccountAdmin`
    
- `roles/iam.workloadIdentityPoolAdmin`
    

Avoid giving these to:

- workloads
    
- CI/CD tooling
    
- service accounts
    

---

## **31.4.3 Node-to-Workload Escalation**

If node SA has broad IAM:

- any pod on node can impersonate node
    
- escalate to entire project
    

Mitigation:

- restrict node SA IAM
    
- enforce Workload Identity
    
- disable metadata server legacy endpoints:
    

```bash
gcloud compute project-info add-metadata \
  --metadata=enable-oslogin=TRUE,disable-legacy-endpoints=TRUE
```

---

## **31.4.4 Lateral Movement Across Namespaces**

Common mistake: no NetworkPolicy, no KSA segregation.

Fix:

- 1 KSA per workload
    
- 1 namespace per trust boundary
    
- strict NetworkPolicies
    
- strict AuthorizationPolicy in mesh
    

---

## **31.4.5 Identity & Secret Leakage via Logging**

Debug logs that print:

- JWTs
    
- GCP tokens
    
- private keys
    
- OAuth tokens
    
- service account emails  
    → immediate security breach risk.
    

Mitigation:

- redact logs
    
- block `DEBUG` logs in production
    
- use logging agents that scrub sensitive content
    

---

## **31.4.6 CI/CD Identity Escalation**

If CI/CD SA has broad roles:

- attacker can compromise deployments
    
- override production configs
    
- access private data
    

Best practice:

- separate CI/CD identities by environment
    
- limit to deployment-only roles
    
- never use editor
    
- enforce Workload Identity Federation
    

---

# **Chapter 32 — Secrets Management**

_(Expanded with senior-level clarity, Secret Manager usage, KMS encryption practices, rotation frameworks, YAML examples, and security anti-patterns.)_

Secrets management ensures sensitive data (API keys, tokens, DB passwords, OAuth secrets, certificates) is stored, encrypted, rotated, and accessed securely across all workloads.

This chapter provides a complete, practical guide to managing secrets at scale in GCP + GKE.

---

# **32.1 Secret Manager**

GCP Secret Manager is the recommended centralized system for storing secrets.  
It provides:

- encrypted storage (using KMS)
    
- versioning
    
- automatic replication
    
- IAM-based access
    
- audit logging
    
- per-secret and per-version lifecycle control
    
- multi-region resilience
    

---

## **32.1.1 Creating and Accessing Secrets**

### **Create a Secret**

```bash
echo -n "db-password-123" | gcloud secrets create db-password \
  --replication-policy="automatic" \
  --data-file=-
```

### **Add a Secret Version**

```bash
echo -n "db-password-456" | gcloud secrets versions add db-password \
  --data-file=-
```

### **Access a Secret**

```bash
gcloud secrets versions access latest --secret=db-password
```

---

## **32.1.2 Granting Access to Workloads**

Workloads must use **Workload Identity** with GCP IAM to access secrets.

Example (GSA → KSA binding):

```bash
gcloud secrets add-iam-policy-binding db-password \
  --member="serviceAccount:myproj.svc.id.goog[checkout/checkout-sa]" \
  --role="roles/secretmanager.secretAccessor"
```

This ensures:

- only the checkout service
    
- in checkout namespace
    
- can retrieve the secret
    

---

## **32.1.3 Accessing Secrets from GKE (Sidecar-Free)**

Use the Secret Manager API:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: checkout
spec:
  template:
    spec:
      serviceAccountName: checkout-sa
      containers:
      - name: app
        image: myapp:latest
        env:
        - name: DB_PASSWORD
          valueFrom:
            secretKeyRef:
              name: runtime-secret  # loaded by init script
              key: password
```

But **never** store actual secret values in Kubernetes Secret stores unless encrypted (see anti-patterns section).

Recommended approach:  
Fetch secrets programmatically at runtime:

**Go Example:**

```go
client, _ := secretmanager.NewClient(ctx)
result, _ := client.AccessSecretVersion(ctx, &secretmanagerpb.AccessSecretVersionRequest{
  Name: "projects/myproj/secrets/db-password/versions/latest",
})
dbPass := string(result.Payload.GetData())
```

---

## **32.1.4 Secrets as Files (Init Container)**

Init container retrieves and writes secret to a shared volume:

```yaml
initContainers:
- name: secret-init
  image: google/cloud-sdk:slim
  command: ["sh", "-c"]
  args:
  - >
    gcloud secrets versions access latest --secret=db-password
    > /secrets/db-password;
  volumeMounts:
  - name: secrets-vol
    mountPath: /secrets
```

---

## **32.1.5 Secret Manager Pitfalls**

- Granting “secretAccessor” to broad service accounts
    
- Using default SA → lateral movement risk
    
- Storing secrets in Git repos / ConfigMaps
    
- Forgetting to set IAM bindings at **secret level** (not project)
    
- Not using versioning → poor rollback story
    

---

# **32.2 KMS & Encryption Hierarchies**

Encryption underpins Secret Manager, but also applies to:

- GCS buckets
    
- persistent disks
    
- databases
    
- inter-service communication
    
- custom encrypted payloads
    

KMS provides:

- **Key rings / keys**
    
- **Key rotation**
    
- **Key usage logs**
    
- **CloudHSM** for hardware-backed keys
    

---

## **32.2.1 KMS Key Creation**

```bash
gcloud kms keyrings create prod-ring --location=us-central1

gcloud kms keys create secret-key \
  --location=us-central1 \
  --keyring=prod-ring \
  --purpose=encryption
```

---

## **32.2.2 Encrypt a File Using KMS**

```bash
gcloud kms encrypt \
  --location=us-central1 \
  --keyring=prod-ring \
  --key=secret-key \
  --plaintext-file=db.txt \
  --ciphertext-file=db.enc
```

---

## **32.2.3 Decrypting (Runtime)**

```bash
gcloud kms decrypt \
  --location=us-central1 \
  --keyring=prod-ring \
  --key=secret-key \
  --ciphertext-file=db.enc \
  --plaintext-file=-
```

---

## **32.2.4 Envelope Encryption Model**

This pattern protects large data payloads while minimizing KMS calls.

Workflow:

1. Use KMS to encrypt a **data encryption key (DEK)**
    
2. Use DEK to encrypt large data (e.g., file, DB field)
    
3. Store the encrypted DEK + encrypted data together
    

This is used widely for:

- GCS
    
- PD
    
- Secret Manager
    
- BigQuery
    

---

## **32.2.5 KMS IAM Controls**

Grant encryption-only role:

```bash
gcloud kms keys add-iam-policy-binding secret-key \
  --member=serviceAccount:checkout-sa@myproj.iam.gserviceaccount.com \
  --role=roles/cloudkms.cryptoKeyEncrypterDecrypter
```

Or encryption-only:

```bash
--role=roles/cloudkms.cryptoKeyEncrypter
```

---

## **32.2.6 Common KMS Pitfalls**

- Overloading one KMS key for many services
    
- Granting decrypt rights to entire project
    
- Storing encrypted secrets inside repos (security theater)
    
- High latency from too many KMS calls
    
- Not monitoring key access patterns
    

---

# **32.3 Secret Rotation**

Rotation is essential for cryptographic hygiene.  
Secrets must be:

- versioned
    
- rotated
    
- retired
    
- invalidated
    
- rolled out safely
    

Rotation applies to:

- API keys
    
- OAuth client IDs/secrets
    
- database passwords
    
- TLS certificates
    
- encryption keys
    

---

## **32.3.1 Secret Manager Versioning**

Version 1 → version 2 → version 3  
Old versions remain accessible (unless disabled).

Create new version:

```bash
gcloud secrets versions add db-password \
  --data-file=newpw.txt
```

Disable old version:

```bash
gcloud secrets versions disable 1 --secret=db-password
```

Destroy old version:

```bash
gcloud secrets versions destroy 1 --secret=db-password
```

---

## **32.3.2 Automating Rotation (Cloud Scheduler + Cloud Functions)**

Example: rotate DB password weekly.

Cloud Scheduler cron:

```bash
gcloud scheduler jobs create pubsub rotate-db-password \
  --schedule="0 2 * * 0" \
  --topic=rotate-db-pass
```

Cloud Function pseudocode:

```python
def rotate(event, context):
    newpass = random_password()
    add_secret_version("db-password", newpass)
    update_database_password(newpass)
```

---

## **32.3.3 Certificate Rotation (Istio)**

Istio auto-rotates mTLS certs every 24h.  
Confirm rotation:

```bash
istioctl proxy-status
```

---

## **32.3.4 Rotating Static Service Account Keys (Bad Practice)**

GCP recommends **disabling** key usage, but if legacy systems require them:

```bash
gcloud iam service-accounts keys create new-key.json \
  --iam-account=my-sa@myproj.iam.gserviceaccount.com
```

Rotate and delete old:

```bash
gcloud iam service-accounts keys delete OLD_KEY \
  --iam-account=my-sa@myproj.iam.gserviceaccount.com
```

But best practice:

> **Do not use service account keys. Use Workload Identity Federation.**

---

## **32.3.5 Secret Rotation Pitfalls**

- Rotating secrets without coordinating downstream dependencies
    
- Forgetting to update environment variables after rotation
    
- Rotating DB passwords without updating connection pools → cascading failures
    
- Not disabling old versions → attackers reuse old secrets
    
- Overlapping rotations → partial outages
    

---

# **32.4 Secret Anti-Patterns**

This section documents real-world disasters caused by poor secret hygiene.

---

## **32.4.1 Storing Secrets in Kubernetes Secrets (Without Encryption)**

Kubernetes Secrets are:

- base64-encoded (NOT encrypted)
    
- stored in etcd
    
- accessible to node and cluster admins
    

Unless ephemeral and short-lived, **do not use them for long-term secrets**.

Better:

- Secret Manager + workload identity
    
- Encryption at rest + RBAC + etcd encryption (last resort)
    

---

## **32.4.2 Storing Secrets in ConfigMaps**

Super anti-pattern.  
ConfigMaps are world-readable inside namespace.

Examples of bad behavior:

- storing OAuth tokens
    
- storing DB passwords in plain YAML
    
- committing them to Git
    
- distributing secrets via CI/CD logs
    

---

## **32.4.3 Checking Secrets into Git Repos**

Examples:

- `.env` files
    
- JSON key files
    
- kubeconfig tokens
    
- TLS private keys
    

Fix:

- use GitHub secret scanning
    
- enforce pre-commit hooks
    
- block committing `.pem` or `.json` creds
    
- rotate instantly if committed
    

---

## **32.4.4 Long-Lived API Keys**

Long-lived tokens create massive risk.

Rotate:

- every 7–30 days
    
- or automatically using scheduler pipelines
    

---

## **32.4.5 Hardcoding Secrets in Code**

Example of disaster:

```go
apiKey := "AIza...hardcoded-value"
```

Use environment variables or runtime Secret Manager API.

---

## **32.4.6 Using Default GCP Service Accounts**

Default SA (`<PROJECT_NUMBER>-compute@developer.gserviceaccount.com`):

- has broad editor-like permissions
    
- is shared across nodes
    
- is high-risk
    

Disable it:

```bash
gcloud iam service-accounts disable \
  <PROJECT_NUMBER>-compute@developer.gserviceaccount.com
```

---

## **32.4.7 Mounting Secrets to Files with 0777 Permissions**

Set correct permissions:

```yaml
defaultMode: 0400
```

---

## **32.4.8 Blind Trust in Envelope Encryption**

Some teams encrypt secrets with KMS but then:

- check encrypted blobs into Git
    
- store DEKs next to encrypted content
    
- forget to restrict KMS decrypt permissions
    

This is “security theater”—you think you're safe, but you're not.

---

# **Chapter 33 — Audit Logging, Threat Detection & Forensics**

_(Expanded with senior-level clarity, GCP audit log models, SCC usage, GKE forensic techniques, kubectl/gcloud examples, and incident response playbook design.)_

A mature cloud platform must assume that:

- credentials will leak,
    
- misconfigurations will occur,
    
- internal actors may behave maliciously, and
    
- external threats will attempt exploitation.
    

Audit logging, threat detection, and forensic readiness are essential to detect and investigate these events.

This chapter provides a pragmatic, production-ready approach to logging, threat detection, and high-level IR playbooks.

---

# **33.1 Admin Activity Logs**

**Admin Activity Logs** capture all actions that modify resources in a GCP project.  
They are immutable, automatically enabled, and free to ingest.

They include:

- IAM changes
    
- resource creation/deletion
    
- network/firewall updates
    
- cluster configuration changes
    
- service enable/disable actions
    

These are the **most critical logs** for compliance and security investigations.

---

## **33.1.1 Enabling Admin Activity Log Exports**

Export to BigQuery or Cloud Logging bucket.

### Export to BigQuery:

```bash
gcloud logging sinks create admin-activity-sink \
  bigquery.googleapis.com/projects/myproj/datasets/adminlogs \
  --log-filter='logName:"cloudaudit.googleapis.com/activity"'
```

---

## **33.1.2 Typical Admin Activity Log Event Example**

```json
{
  "protoPayload": {
    "methodName": "v1.compute.instances.insert",
    "authenticationInfo": {
      "principalEmail": "alice@example.com"
    },
    "serviceName": "compute.googleapis.com",
    "resourceName": "projects/myproj/zones/us-central1-a/instances/attack-vm"
  }
}
```

This is used to detect:

- unauthorized VM creation
    
- anomalous IAM user activity
    
- privilege escalation attempts
    
- resource deletions
    

---

## **33.1.3 Querying Admin Activity Logs (BigQuery)**

```sql
SELECT
  timestamp,
  protoPayload.authenticationInfo.principalEmail AS actor,
  protoPayload.methodName AS action
FROM
  `myproj.adminlogs.cloudaudit_activity`
WHERE
  timestamp > TIMESTAMP_SUB(CURRENT_TIMESTAMP(), INTERVAL 1 DAY)
ORDER BY timestamp DESC;
```

---

## **33.1.4 Alert Examples Based on Admin Activity**

- new IAM role binding added
    
- changes to firewall allow rules
    
- new service account key created
    
- enabling/disabling APIs unexpectedly
    
- deletion of Cloud Logging sinks
    

---

## **33.1.5 Common Pitfalls**

- Not exporting logs to long-term retention
    
- Not monitoring IAM changes
    
- Only exporting application logs, ignoring admin logs
    
- Allowing project owners unrestricted IAM changes
    

---

# **33.2 Data Access Logs**

Data Access Logs capture:

- reads/writes to data stored in GCP services
    
- including GCS, Secret Manager, Firestore, BigQuery, Pub/Sub
    

They are more expensive, but essential for:

- compliance (SOC2, PCI, HIPAA, FedRAMP)
    
- insider threat detection
    
- forensic analysis
    

---

## **33.2.1 Enabling Data Access Logs (IAM Policy)**

Data Access logs must be explicitly enabled per service.

Example: enable BigQuery data access logs:

```bash
gcloud logging sinks create bq-data-access \
  bigquery.googleapis.com/projects/myproj/datasets/bqlogs \
  --log-filter='protoPayload.serviceName:"bigquery.googleapis.com"
                AND protoPayload.methodName:"Get*"
                AND logName:"cloudaudit.googleapis.com/data_access"'
```

---

## **33.2.2 Data Access Log Example (Secret Manager)**

```json
{
  "protoPayload": {
    "methodName": "AccessSecretVersion",
    "authenticationInfo": {
      "principalEmail": "workload@myproj.iam.gserviceaccount.com"
    },
    "resourceName": "projects/myproj/secrets/db-password/versions/3"
  }
}
```

Meaning:

- workload accessed secret version 3
    
- this is auditable and traceable
    

---

## **33.2.3 Querying Data Access Logs for Unusual Reads**

### Example: Who accessed Secret Manager in the past hour?

```sql
SELECT
  timestamp,
  protoPayload.authenticationInfo.principalEmail AS actor,
  protoPayload.resourceName AS resource
FROM
  `myproj.secretlogs.cloudaudit_data_access`
WHERE
  timestamp > TIMESTAMP_SUB(CURRENT_TIMESTAMP(), INTERVAL 1 HOUR);
```

---

## **33.2.4 Common Data Access Threats Detected**

- compromised service account accessing secrets
    
- “secret scraping” across projects
    
- bulk data exfiltration
    
- unauthorized access to customer data
    
- misconfigured IAM roles granting excessive access
    

---

## **33.2.5 Data Access Log Pitfalls**

- Not enabling them due to cost → blind to insider threats
    
- Not filtering retention → large storage bills
    
- Dumping all logs into one bucket → hard for SIEM correlation
    

---

# **33.3 SCC (Security Command Center)**

Security Command Center (SCC) provides:

- threat detection
    
- vulnerability monitoring
    
- misconfiguration scanning
    
- risk scoring
    
- asset inventory
    

It is the core platform for security visibility in GCP.

---

## **33.3.1 SCC Tiers**

|Tier|Use Cases|
|---|---|
|**SCC Standard**|Misconfigurations, basic findings|
|**SCC Premium**|Threat detection, event correlation, attack path analysis|

For regulated industries, SCC Premium is strongly recommended.

---

## **33.3.2 Enabling SCC**

```bash
gcloud scc settings enable --organization=1234567890
```

Enable built-in detectors:

```bash
gcloud scc utils activate-service \
  --service=WEB_SECURITY_SCANNER \
  --organization=1234567890
```

---

## **33.3.3 SCC Key Finding Types**

### **Misconfigurations**

- public buckets
    
- overly broad IAM roles
    
- firewall rules with `0.0.0.0/0`
    
- service accounts with admin privileges
    

### **Threats**

- cryptomining malware
    
- compromised service accounts
    
- anomalous network activity
    
- data exfiltration patterns
    

### **Vulnerabilities**

- outdated container images
    
- CVEs in application components
    
- exposed admin panels
    

---

## **33.3.4 Example SCC Finding (IAM Misconfiguration)**

```json
{
  "category": "PUBLIC_BUCKET_ACL",
  "resourceName": "projects/myproj/buckets/customer-data",
  "severity": "HIGH",
  "state": "ACTIVE"
}
```

---

## **33.3.5 Integrating SCC Findings with SIEM**

Example: Export SCC to Pub/Sub for SIEM ingestion

```bash
gcloud scc findings bulk-export \
  --organization=123 \
  --output-config="pubsub:projects/myproj/topics/scc-findings"
```

---

## **33.3.6 SCC Pitfalls**

- Treating SCC as optional → severe blind spots
    
- Not configuring email/webhook notifications
    
- Not triaging HIGH severity findings
    
- No ownership assigned for remediation tasks
    
- Ignoring stale or suppressed findings
    

---

# **33.4 IR Playbooks (High-Level)**

Incident Response (IR) playbooks provide repeatable actions for security incidents.  
They:

- reduce panic
    
- enforce consistency
    
- support compliance
    
- provide audit trails
    

This section outlines high-level structures.  
(You can request full playbooks next.)

---

## **33.4.1 IR Stages Overview**

1. **Detection**  
    Alert fired (SCC, Cloud Logging, SIEM, SLO burn).
    
2. **Triage**  
    Determine severity, impact, affected services.
    
3. **Containment**  
    Block access, rotate secrets, disable accounts.
    
4. **Eradication**  
    Remove malicious artifacts, patch vulnerabilities.
    
5. **Recovery**  
    Restore systems, validate functionality.
    
6. **Postmortem**  
    Document lessons, fixes, follow-ups.
    

---

## **33.4.2 Example IR Playbook: Compromised Service Account**

### **Detection**

- SCC finding: “Service Account Key Abuse”
    
- Logs: unusual Secret Manager reads
    

### **Triage**

Identify:

- which SA
    
- what resources accessed
    
- time window
    

Query example:

```sql
SELECT *
FROM `myproj.secretlogs.cloudaudit_data_access`
WHERE protoPayload.authenticationInfo.principalEmail = "compromised@myproj.iam.gserviceaccount.com"
```

---

### **Containment**

1. Disable the SA immediately:
    

```bash
gcloud iam service-accounts disable compromised@myproj.iam.gserviceaccount.com
```

2. Disable key(s):
    

```bash
gcloud iam service-accounts keys delete <KEY_ID> \
  --iam-account=compromised@myproj.iam.gserviceaccount.com
```

---

### **Eradication**

- remove backdoor workloads/container images
    
- rotate secrets
    
- validate pod/container integrity
    

---

### **Recovery**

- re-enable SA or create new SA
    
- rebind IAM roles
    
- redeploy workloads using GitOps
    

---

### **Postmortem**

Document:

- root cause
    
- impact
    
- timeline
    
- prevention
    

---

## **33.4.3 Example IR Playbook: Unauthorized Firewall Modification**

### Detection

Admin Activity Logs show:

```json
"methodName": "v1.compute.firewalls.insert"
```

### Triage

- identify actor
    
- review new firewall allowlist
    
- verify if malicious IPs present
    

### Containment

Revoke change:

```bash
gcloud compute firewall-rules delete suspicious-rule
```

Lock down IAM:

```bash
gcloud projects remove-iam-policy-binding \
  --member=user:alice@example.com \
  --role=roles/compute.admin
```

---

### Eradication

Review other firewall changes in the past 24 hours.

### Recovery

Reapply correct firewall baseline (Terraform/GitOps)

---

### Postmortem

- Why did user have excessive IAM?
    
- What gap allowed unsanctioned change?
    

---

## **33.4.4 IR Playbook Pitfalls**

- No clear severity matrix
    
- No on-call distribution of responsibilities
    
- IR playbooks stored in private laptop, not shared repo
    
- Not integrating IR with observability stack
    
- Failing to run IR tabletop exercises
    
- No postmortems → repeated incidents
    

---

# **Chapter 34 — Policy-as-Code & Guardrails**

_(Expanded with senior-level clarity, OPA/Gatekeeper policies, Org Policy enforcement, CI guardrails, YAML/rego examples, and real-world anti-patterns. No redundancy, fully self-contained.)_

Modern cloud platforms must enforce guardrails **automatically**, not through manual reviews or tribal knowledge.  
Policy-as-Code (PaC) moves security, governance, and compliance into:

- **codified rules**
    
- **automated enforcement**
    
- **cluster admission control**
    
- **CI/CD checks**
    
- **organization-wide controls**
    

This chapter provides a complete, practical framework for creating guardrails in Kubernetes and GCP.

---

# **34.1 OPA / Gatekeeper**

OPA (Open Policy Agent) is an engine for evaluating rules expressed in Rego.  
Gatekeeper is OPA’s Kubernetes admission controller implementation.

They allow enforcing policies such as:

- “No privileged containers”
    
- “Labels required on all resources”
    
- “Only signed images allowed”
    
- “No `0.0.0.0/0` services”
    
- “No hostPath volumes”
    

---

## **34.1.1 Gatekeeper Architecture**

Gatekeeper components:

- **Admission webhook** → enforces policies before resource creation
    
- **Constraint Templates** → define reusable policy logic
    
- **Constraints** → apply templates to specific Kubernetes resource types
    
- **Audit controller** → periodically audits cluster state
    

---

## **34.1.2 Example Constraint Template (Rego)**

_Reject privileged containers._

`constrainttemplate.yaml`:

```yaml
apiVersion: templates.gatekeeper.sh/v1beta1
kind: ConstraintTemplate
metadata:
  name: k8sprivileged
spec:
  crd:
    spec:
      names:
        kind: K8sPrivileged
  targets:
  - target: admission.k8s.gatekeeper.sh
    rego: |
      package k8sprivileged

      violation[{"msg": msg}] {
        input.review.object.spec.containers[_].securityContext.privileged == true
        msg := "Privileged containers are not allowed"
      }
```

---

## **34.1.3 Constraint Example**

```yaml
apiVersion: constraints.gatekeeper.sh/v1beta1
kind: K8sPrivileged
metadata:
  name: disallow-privileged
spec:
  match:
    kinds:
    - apiGroups: [""]
      kinds: ["Pod"]
```

---

## **34.1.4 Required Labels Policy**

Template:

```yaml
package requiredlabels

violation[{"msg": msg}] {
  required := {"team", "env"}
  provided := {label | label := input.review.object.metadata.labels[_]}

  missing := required - provided
  count(missing) > 0

  msg := sprintf("Missing required labels: %v", [missing])
}
```

Constraint:

```yaml
apiVersion: constraints.gatekeeper.sh/v1beta1
kind: RequiredLabels
metadata:
  name: enforce-labels
spec:
  match:
    kinds:
    - apiGroups: ["apps"]
      kinds: ["Deployment"]
```

---

## **34.1.5 Gatekeeper Observability**

Check violations:

```bash
kubectl get constraintviolations
```

Audit full cluster:

```bash
kubectl get k8sprivileged.status
```

---

## **34.1.6 Gatekeeper Pitfalls**

- Policies too strict → widespread deployment failures
    
- No exemption mechanism
    
- No version control → drift between clusters
    
- Writing complex Rego when templates are sufficient
    
- Forgetting audit → drift goes unnoticed
    
- Scattering policy files across repos → no shared standards
    

---

# **34.2 Organization Policies (GCP Org Policies)**

Organization Policies enforce constraints across:

- the entire organization,
    
- folders,
    
- or individual projects.
    

They prevent misconfigurations **before they occur**, such as:

- disabling “DisableExternalIP”
    
- enforcing CMEK on storage
    
- restricting regions
    
- blocking risky services
    
- disallowing legacy IAM
    

---

## **34.2.1 Setting Org Policy Example: Disable External IPs**

```bash
gcloud org-policies set-policy <<EOF
name: organizations/1234567890/policies/compute.vmExternalIpAccess
spec:
  rules:
    - enforce: true
EOF
```

This enforces:

> **No VM can be created with a public IP in the entire organization.**

---

## **34.2.2 Restricting Allowed Regions**

```bash
gcloud org-policies set-policy <<EOF
name: organizations/1234567890/policies/compute.allowedRegions
spec:
  rules:
    - allow:
        values:
          - "us-central1"
          - "us-east1"
EOF
```

---

## **34.2.3 Enforce CMEK on GCS / BigQuery**

```bash
gcloud org-policies set-policy <<EOF
name: organizations/1234567890/policies/storage.uniformBucketLevelAccess
spec:
  rules:
    - enforce: true
EOF
```

---

## **34.2.4 Prevent IAM Wildcard Role Grants**

```bash
gcloud org-policies set-policy <<EOF
name: organizations/1234567890/policies/iam.disableServiceAccountKeyCreation
spec:
  rules:
    - enforce: true
EOF
```

Disallows SA key creation across the org.

---

## **34.2.5 Org Policy Anti-Patterns**

- Setting policies only at project level → non-uniform controls
    
- Allowing legacy IAM permissions for “flexibility”
    
- Not grouping teams via folder hierarchy
    
- Not testing policies before org-wide enforcement
    
- Using exceptions excessively → policy erosion
    

---

# **34.3 CI Guardrails**

CI/CD pipelines must enforce guardrails early to prevent broken or insecure infrastructure from reaching production.

Three levels of guardrails:

1. **Static Checks**
    
2. **Security Scans**
    
3. **Policy-as-Code Enforcement**
    

---

## **34.3.1 Static Checks (Linting & Validation)**

### Terraform Example

```bash
terraform fmt -check
terraform validate
tflint --recursive
```

### Kubernetes Example

```bash
kubeval manifests/
```

---

## **34.3.2 Security Scans**

### Checkov example:

```bash
checkov -d infrastructure/
```

Finds:

- public buckets
    
- unencrypted disks
    
- insecure IAM policies
    

### Trivy example:

```bash
trivy config k8s/
```

Finds:

- dangerous pod security settings
    
- plaintext secrets
    
- host networking
    

---

## **34.3.3 OPA / Conftest in CI**

Regulate IaC before apply.

Example policy: No public `0.0.0.0/0` firewall rules.

```rego
deny[msg] {
  input.resource_type == "google_compute_firewall"
  input.allowed_cidrs[_] == "0.0.0.0/0"
  msg = "Public firewall rules are forbidden"
}
```

Usage:

```bash
terraform plan -out=plan.json
terraform show -json plan.json | conftest test -
```

---

## **34.3.4 Signing & Verification in CI**

Use sigstore/cosign for image verification:

```bash
cosign verify gcr.io/myproj/app:latest
```

Block deployment if signature missing.

---

## **34.3.5 Fail-Fast Approval Model**

PR workflow:

- CI runs all tests
    
- plan/tests/policy results attached to PR
    
- minimum two maintainers must approve
    

Prevents:

- accidental prod changes
    
- insecure configurations
    
- unreviewed policy bypasses
    

---

## **34.3.6 CI Guardrail Anti-Patterns**

- Running “terraform apply” in PR pipeline
    
- No validation of Kubernetes manifests
    
- Using long-lived credentials in CI
    
- Not validating that images are signed
    
- Allowing merges despite policy failures
    
- Running CI without parallel isolation → drift / racing
    

---

# **34.4 Security Bottleneck Anti-Patterns**

Many organizations fall into “security bottleneck traps,” where security becomes a blocker rather than an enabler.

This section outlines traps to avoid.

---

## **34.4.1 Centralized Manual Approvals for Everything**

Anti-pattern:

> Every deployment requires manual review from security.

Problems:

- delays deployments
    
- overwhelms security teams
    
- encourages bypassing the process
    

Fix:

- automated PaC guardrails
    
- security-as-code pipelines
    
- compliance baked into CI
    

---

## **34.4.2 Gatekeeper / OPA Used as a Replacement for Good IaC**

OPA should **augment**, not replace Terraform hygiene.

If you rely on OPA alone:

- infrastructure drift will still happen
    
- insecure IaC will slip through early phases
    

---

## **34.4.3 Policies Not Version-Controlled**

Symptoms:

- inconsistent enforcement across clusters
    
- difficult debugging
    
- misaligned expectations
    
- unpredictable failures
    

Fix:

> Store policies in Git and deploy via GitOps.

---

## **34.4.4 One Giant Policy That Does Everything**

This is brittle and impossible to maintain.  
Instead:

- separate concerns
    
- use a library of composable policies
    

---

## **34.4.5 Security Reviews Done Too Late (Right Shifted)**

Catching security issues after deployment is:

- costly
    
- slow
    
- risky
    

Shift left by:

- scanning IaC
    
- scanning manifests
    
- embedding policy tests in CI
    

---

## **34.4.6 Overly Strict Policies Without Escape Hatches**

Policies like:

- require mTLS everywhere
    
- forbid all public services
    
- block all privileged workloads
    

must allow controlled exceptions.

Fix:

- namespace-based allowlists
    
- team-based exemptions with time limits
    
- token-based exception windows
    

---

## **34.4.7 Relying on Security Awareness Instead of Automation**

Telling developers:

> “Remember not to create public buckets.”

is ineffective.

Automation should enforce:

- encryption
    
- region restrictions
    
- IAM boundaries
    
- artifact verification
    

---

# **Chapter 35 — Supply Chain Security**

_(Expanded with senior-level clarity, actionable CI/CD patterns, SLSA controls, SBOM generation, Binary Authorization policies, and image signing workflows. Includes gcloud/kubectl/YAML/config examples.)_

Modern cloud-native platforms face threats long **before** code reaches production:

- compromised libraries
    
- poisoned build pipelines
    
- tampered container images
    
- unverified artifacts
    
- malicious dependencies
    

Supply Chain Security protects the entire path from **source → build → artifact → deploy**.

---

# **35.1 SLSA Levels (Supply-chain Levels for Software Artifacts)**

SLSA (pronounced _“salsa”_) is a framework defining integrity requirements for the software supply chain.  
It establishes **attestation**, **build integrity**, and **provenance** requirements.

---

## **35.1.1 SLSA Levels Overview**

|**Level**|**Guarantee**|**Example Controls**|
|---|---|---|
|**SLSA 1**|Build provenance exists|CI system outputs metadata|
|**SLSA 2**|Tamper resistance of build service|Hosted CI; version-controlled config|
|**SLSA 3**|Strong integrity guarantees|Isolated builds, hermetic builds|
|**SLSA 4**|Reproducible builds|High-assurance regulated environments|

Most enterprises strive for **SLSA 2–3**, which aligns well with:

- GitHub Actions OIDC + Workload Identity Federation
    
- Cloud Build with attestations
    
- Binary Authorization
    

---

## **35.1.2 Implementing SLSA in Cloud Build**

Enable provenance:

```yaml
steps:
- name: gcr.io/cloud-builders/docker
  args: ["build", "-t", "gcr.io/myproj/checkout:${COMMIT_SHA}", "."]

provenance:
  enabled: true
```

Cloud Build will produce attestation metadata:

- who built it
    
- what repo commit
    
- build environment
    
- build steps
    

---

## **35.1.3 Build Integrity with OIDC (GitHub → GCP)**

Ensure builds cannot be spoofed using long-lived service account keys.

Example GitHub Actions auth:

```yaml
- name: Authenticate to GCP
  uses: google-github-actions/auth@v1
  with:
    workload_identity_provider: "projects/12345/locations/global/workloadIdentityPools/gh/providers/github"
    service_account: "ci-builder@myproj.iam.gserviceaccount.com"
```

This prevents:

- key theft
    
- rogue builds
    
- impersonation
    

---

## **35.1.4 Common SLSA Pitfalls**

- Allowing developers to build images locally and push to registry
    
- No provenance → untraceable artifacts
    
- Build pipelines running with admin credentials
    
- Missing isolation → poisoned container builds
    
- No reproducibility → impossible to validate integrity
    

---

# **35.2 SBOMs (Software Bill of Materials)**

An **SBOM** lists all dependencies in an artifact:

- OS packages
    
- application libraries
    
- transitive dependencies
    
- licenses
    
- versions
    

SBOMs are essential for:

- vulnerability scanning
    
- license compliance
    
- forensic investigations
    
- dependency auditing
    

---

## **35.2.1 Generate SBOM with Syft**

```bash
syft gcr.io/myproj/checkout:latest -o json > sbom.json
```

---

## **35.2.2 Generate SBOM via Cloud Build**

Cloud Build SBOM config:

```yaml
steps:
- name: gcr.io/cloud-builders/syft
  args: ["packages", "--output", "json", "--file", "/workspace/sbom.json", "."]
artifacts:
  objects:
    location: "gs://my-artifacts/sboms/"
    paths: ["sbom.json"]
```

Store SBOMs in:

- GCS
    
- Artifact Registry
    
- Git repo
    

---

## **35.2.3 Using Grype to Scan SBOM Vulnerabilities**

```bash
grype sbom:sbom.json
```

---

## **35.2.4 Deploy SBOM with Image Metadata (OCI Attestation)**

Attach SBOM as OCI artifact:

```bash
oras attach \
  gcr.io/myproj/checkout:latest \
  --artifact-type "application/vnd.sbom" \
  sbom.json
```

---

## **35.2.5 SBOM Pitfalls**

- SBOM generated at dev machine → untrustworthy
    
- No automation to regenerate SBOM after dependencies update
    
- Not storing SBOMs with artifacts → loss of auditability
    
- SBOM not validated during deployment → drift from artifact
    

---

# **35.3 Binary Authorization**

Binary Authorization (BinAuthz) enforces _admission control_ on GKE:

- only signed
    
- only attested
    
- only trusted sources
    

can deploy images.

---

## **35.3.1 Enable Binary Authorization**

```bash
gcloud services enable binaryauthorization.googleapis.com
```

Enable cluster-level policy enforcement:

```bash
gcloud container clusters update prod-cluster \
  --enable-binauthz
```

---

## **35.3.2 Example BinAuthz Policy (Reject Unsigned Images)**

```yaml
defaultAdmissionRule:
  evaluationMode: REQUIRE_ATTESTATION
  enforcementMode: ENFORCED_BLOCK_AND_AUDIT_LOG
admissionWhitelistPatterns:
- namePattern: "gcr.io/myproj/allowlist/*"
```

---

## **35.3.3 Create an Attestation (Cosign or Cloud KMS)**

```bash
gcloud binauthz attestations create \
  --attestor=my-attestor \
  --artifact-url=gcr.io/myproj/checkout:abcd1234 \
  --attestation-file=attest.json \
  --signature-file=sig.dat \
  --public-key-file=public.pem
```

Attestors can be:

- build systems (Cloud Build)
    
- security teams
    
- automated scanners
    

---

## **35.3.4 Automated Attestations (Cloud Build)**

`cloudbuild.yaml`:

```yaml
steps:
- name: gcr.io/cloud-builders/docker
  args: ["build", "-t", "$IMAGE", "."]

attestations:
- attestor: projects/myproj/attestors/cicd-attestor
  predicate:
    type: SLSA_PROVENANCE
```

Cloud Build signs the image automatically.

---

## **35.3.5 Verification During Deployment**

Attempt deployment:

```bash
kubectl apply -f deployment.yaml
```

If the image is not attested:

> The deployment will be rejected by GKE’s admission controller.

---

## **35.3.6 Binary Authorization Pitfalls**

- Leaving allowlists too permissive
    
- Signing images inside cluster (compromised build pipeline)
    
- Using manual attestation → inconsistent provenance
    
- Not tying attestations to Git commit SHA
    
- Enforcing BinAuthz only in prod (should be enforced in staging)
    

---

# **35.4 Image Signing & Verification**

Image signing ensures artifacts have not been tampered with between build and deploy.  
Modern supply chain tooling uses:

- **Cosign** (Sigstore)
    
- **Cloud KMS**
    
- **Fulcio / Rekor** (transparency logs)
    

---

## **35.4.1 Cosign Signing (Keyless Mode)**

This uses OIDC identity from GitHub/GitLab to sign images.

```bash
cosign sign gcr.io/myproj/checkout:latest
```

This produces:

- signature artifact
    
- transparency log entry
    

---

## **35.4.2 Cosign Verification**

```bash
cosign verify gcr.io/myproj/checkout:latest \
  --certificate-identity="https://github.com/myorg/myrepo/.github/workflows/build.yaml@refs/heads/main" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```

---

## **35.4.3 Signing with KMS (Alternative)**

```bash
cosign sign \
  --key gcpkms://projects/myproj/locations/us/keyRings/prod/cryptoKeys/signing-key \
  gcr.io/myproj/checkout:latest
```

---

## **35.4.4 Enforce Signed Images at Admission (Policy Controller)**

OPA Gatekeeper example:

```yaml
apiVersion: constraints.gatekeeper.sh/v1beta1
kind: K8sRequiredSignatures
metadata:
  name: enforce-signed-images
spec:
  match:
    kinds:
    - apiGroups: ["apps"]
      kinds: ["Deployment"]
  parameters:
    requiredSignatures:
    - issuer: "https://token.actions.githubusercontent.com"
      subject: "repo:myorg/myrepo"
```

---

## **35.4.5 Image Verification Inside the Cluster (Kyverno)**

```yaml
apiVersion: kyverno.io/v1
kind: ClusterPolicy
metadata:
  name: verify-images
spec:
  validationFailureAction: enforce
  rules:
  - name: check-signature
    match:
      resources:
        kinds: ["Deployment"]
    verifyImages:
    - image: "gcr.io/myproj/*"
      keyless:
        issuer: "https://token.actions.githubusercontent.com"
```

---

## **35.4.6 Image Signing Pitfalls**

- Signing images with long-lived keys → key theft risk
    
- Signing after pushing → attacker could replace image before signing
    
- Not verifying signatures at deploy time
    
- Skipping transparency logs → supply chain tampering invisible
    
- Local developer builds that bypass the pipeline
    

---

# 🎯 **Summary: Building a Secure Supply Chain**

To secure an enterprise cloud platform:

### **Use SLSA**

→ enforce provenance, tamper-resistant builds

### **Generate SBOMs**

→ ensure dependency transparency

### **Enforce Binary Authorization**

→ block untrusted images at deploy

### **Sign Images (Cosign)**

→ guarantee artifact integrity end-to-end

When combined, these controls significantly strengthen your platform against:

- dependency attacks
    
- compromised CI/CD pipelines
    
- malicious insiders
    
- artifact substitution
    
- zero-day vulnerabilities
    

---

# **Chapter 36 — Terraform Architecture**

_(Expanded with senior-level clarity, reusable module patterns, state management strategies, CI best practices, automated testing workflows, and real-world Terraform pitfalls. Includes commented .tf examples and CI/CD integration snippets.)_

A well-designed Terraform architecture is essential for creating a secure, reproducible, and maintainable infrastructure platform.  
This chapter outlines proven patterns for module design, state layout, CI automation, and testing at scale.

---

# **36.1 Module Design**

Modules are the building blocks of a scalable Terraform codebase.  
Good module design reduces duplication, enforces standards, and prevents misconfigurations.

---

## **36.1.1 Types of Modules**

### **1. Root Modules (Stacks)**

These are environment-level orchestrators:

- `prod/networking`
    
- `staging/gke-clusters`
    
- `global/org-policies`
    

They call child modules.

### **2. Child Modules**

Reusable abstractions:

- `modules/gke`
    
- `modules/vpc`
    
- `modules/iam-service-account`
    
- `modules/cloudsql`
    

### **3. Wrapper Modules (Optional)**

Thin modules that enforce defaults or standards.

---

## **36.1.2 Module Structure Example**

```
modules/
  vpc/
    main.tf
    variables.tf
    outputs.tf
    README.md
```

### **main.tf**

```hcl
resource "google_compute_network" "vpc" {
  name                    = var.name
  auto_create_subnetworks = false
}

resource "google_compute_subnetwork" "subnets" {
  for_each = var.subnets
  name     = each.key
  region   = each.value.region
  ip_cidr_range = each.value.cidr
}
```

### **variables.tf**

```hcl
variable "name" {
  type = string
}

variable "subnets" {
  type = map(object({
    region = string
    cidr   = string
  }))
}
```

### **outputs.tf**

```hcl
output "vpc_self_link" {
  value = google_compute_network.vpc.self_link
}
```

---

## **36.1.3 Module API Design Principles**

### **1. Minimize Input Surface**

Avoid giant input variables:

```hcl
variable "full_config" { type = any }
```

→ These destroy module stability and readability.

### **2. Provide Strong Types**

```hcl
variable "node_pools" {
  type = map(object({
    machine_type = string
    min_nodes    = number
    max_nodes    = number
  }))
}
```

### **3. Apply Secure Defaults Inside Modules**

Examples:

- GKE private nodes = true
    
- Shielded VMs = true
    
- Logging/monitoring = enabled
    

### **4. Avoid Business Logic**

Modules should _not_ embed environment-specific logic.  
Root modules should choose the configuration.

---

## **36.1.4 Module Anti-Patterns**

- Using `locals` to mash config into unmaintainable shapes
    
- Creating one “mega-module” for everything
    
- Cross-module references → circular dependencies
    
- Using modules from the registry without version pinning
    
- Passing sensitive variables unencrypted
    

---

# **36.2 State Layout (Layers, Environments)**

Terraform state is the _single source of truth_ for infrastructure resources.  
Improper layout leads to:

- accidental resource deletion
    
- tangled dependencies
    
- slow CI/CD
    
- blocked teams
    

---

## **36.2.1 Recommended State Separation Strategy**

### **1. Global Layer**

Org-level resources:

- folders
    
- org policies
    
- billing
    
- IAM org roles
    
- audit sinks  
    State stored centrally (`terraform-backend/global`).
    

### **2. Networking Layer**

Shared:

- VPC
    
- subnets
    
- firewall rules
    
- Cloud NAT
    
- interconnect  
    Each GCP environment (prod, staging) gets separate state.
    

### **3. Cluster Layer**

Per cluster state:

- GKE cluster
    
- node pools
    
- cluster-level addons
    

### **4. Application Layers**

Microservice-specific infra:

- Cloud SQL instances
    
- Pub/Sub topics
    
- specific IAM roles
    

Each service/team gets isolated state files.

---

## **36.2.2 Example Backend Configuration**

```hcl
terraform {
  backend "gcs" {
    bucket  = "tfstate-prod"
    prefix  = "networking/"
  }
}
```

---

## **36.2.3 Why Multiple State Files?**

Benefits:

- blast radius reduction
    
- parallel CI runs
    
- no locking conflicts
    
- clear team boundaries
    
- reduced plan/apply surface
    

---

## **36.2.4 State Promotion Model (Env → Env)**

Use:

- production state isolated
    
- staging state independent
    
- no “copy state to prod” anti-pattern
    

Promotion method:

- GitOps workflow (changes flow through stages)
    
- NOT state copying
    

---

## **36.2.5 State Anti-Patterns**

- One giant state file for entire infra
    
- Storing state in Git (never do this)
    
- Using local filesystem backend
    
- Using same backend for dev and prod
    
- Manual editing state file (corrupts infra)
    

---

# **36.3 CI Integration**

Terraform should never be run manually except for debugging.  
CI enforces consistency and prevents human error.

---

## **36.3.1 CI Workflow (GitHub Actions Example)**

### `.github/workflows/terraform.yaml`

```yaml
name: Terraform
on:
  pull_request:
    paths:
      - "networking/**"
  push:
    branches: ["main"]

jobs:
  plan:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3

    - name: Auth to GCP
      uses: google-github-actions/auth@v1
      with:
        workload_identity_provider: ${{ secrets.WIF_PROVIDER }}
        service_account: "tf-ci@myproj.iam.gserviceaccount.com"

    - name: Terraform Init
      run: terraform init

    - name: Terraform Plan
      run: terraform plan -out=tfplan
```

---

## **36.3.2 Terraform Apply in CI**

Require approval:

```yaml
  apply:
    needs: plan
    if: github.ref == 'refs/heads/main'
    steps:
    - name: Terraform Apply
      run: terraform apply -auto-approve tfplan
```

---

## **36.3.3 Enforcing Policies via OPA / Terraform Cloud / Conftest**

Example OPA policy:

```rego
deny[msg] {
  input.resource.type == "google_compute_firewall"
  input.resource.allow_cidr == "0.0.0.0/0"
  msg = "Public firewall rules are forbidden"
}
```

Validate before apply:

```bash
conftest test plan.json
```

---

## **36.3.4 Preventing Drift with Automated Scans**

Periodic job:

```bash
terraform plan -detailed-exitcode
```

If exit code = `2`, drift detected → notify team.

---

## **36.3.5 CI Anti-Patterns**

- Allowing developers to run terraform apply locally
    
- Storing CI secrets unencrypted
    
- Running terraform as root on shared runners
    
- No plan output review before apply
    
- No policy enforcement for critical resources
    

---

# **36.4 Testing Terraform Code**

Testing infrastructure code is mandatory for reliability.  
Testing validates:

- module inputs
    
- outputs
    
- security controls
    
- resource creation logic
    
- regression prevention
    

---

## **36.4.1 Unit Testing (Terraform Validate + Check)**

Static checks:

```bash
terraform fmt -check
terraform validate
```

---

## **36.4.2 Linting with TFLint**

```bash
tflint --recursive
```

Example `.tflint.hcl`:

```hcl
plugin "google" {
  enabled = true
  version = "0.28.0"
}
```

---

## **36.4.3 Security Testing with Checkov**

```bash
checkov -d modules/vpc
```

Example Checkov policy detection:

- unencrypted GCS
    
- public LB
    
- IAM wildcard roles
    

---

## **36.4.4 Integration Testing with Terratest (Go)**

Example test that creates & destroys temp GCP resources:

```go
func TestVPCModule(t *testing.T) {
  terraformOptions := &terraform.Options{
    TerraformDir: "../modules/vpc",
  }

  terraform.InitAndApply(t, terraformOptions)
  defer terraform.Destroy(t, terraformOptions)

  vpcName := terraform.Output(t, terraformOptions, "vpc_self_link")
  assert.Contains(t, vpcName, "vpc")
}
```

Terratest validates real behaviors:

- GKE cluster provisioning
    
- IAM roles creation
    
- VPC routing
    

---

## **36.4.5 End-to-End Testing in Ephemeral Environments**

CI creates temporary infra:

- new project
    
- apply test stacks
    
- run workload tests
    
- destroy project automatically
    

Example:

```bash
gcloud projects create temp-test-${RANDOM}
terraform init && terraform apply
terraform destroy
```

---

## **36.4.6 Testing Anti-Patterns**

- No testing at all (common but dangerous)
    
- Using real prod projects for tests
    
- Running integration tests without auto-cleanup
    
- Ignoring terraform lint/security results
    
- Terratest without concurrency control → quota exhaustion
    

---

# **Chapter 37 — CI/CD for Infra & Applications**

_(Expanded with senior-level clarity, reusable pipeline patterns, security controls, environment promotion, and real-world examples for GitHub Actions, Cloud Build, and GitLab. Includes commented YAML, Terraform, kubectl/gcloud snippets, and pitfalls.)_

A robust CI/CD system is the backbone of a reliable cloud platform.  
It ensures that **infrastructure**, **applications**, and **policies** move through environments in a consistent, secure, and automated manner.

This chapter describes modern practices for CI/CD in GCP environments running GKE + GitOps.

---

# **37.1 Pipeline Patterns**

CI/CD pipelines broadly fall into two domains:

1. **Infrastructure Pipelines**  
    Provision or change infrastructure using:
    
    - Terraform
        
    - Helmfile / Kustomize
        
    - Config Controller (optional)
        
2. **Application Pipelines**  
    Build, test, sign, scan, verify, and deploy application artifacts:
    
    - container images
        
    - manifests
        
    - Helm charts
        
    - Cloud Run services
        

Despite their differences, both should follow similar principles.

---

## **37.1.1 CI/CD Pipeline Stages (Universal Pattern)**

A modern pipeline has multiple automated gates:

### **1. Static Analysis**

- linting
    
- schema validation
    
- formatting
    
- manifest checks
    

```bash
terraform fmt -check
tflint
kubeval manifests/
```

---

### **2. Security & Policy Checks**

- SAST (e.g., trivy, semgrep)
    
- IaC scanning (checkov, conftest + rego policies)
    
- secret scanning
    
- SBOM generation
    

```bash
trivy fs .
checkov -d .
cosign verify <image>
```

---

### **3. Build Stage**

Application builds container images:

```bash
docker build -t gcr.io/myproj/api:$COMMIT_SHA .
```

Infra pipeline builds Terraform plan:

```bash
terraform plan -out=tfplan
```

---

### **4. Test Stage**

- unit tests
    
- integration tests
    
- ephemeral environment tests
    
- Terratest for infra
    

---

### **5. Sign & Attest Artifacts**

Using Sigstore or GCP binary authorization:

```bash
cosign sign gcr.io/myproj/api:$COMMIT_SHA
```

---

### **6. Deploy / Apply**

Infrastructure:

```bash
terraform apply tfplan
```

Applications (GitOps):

- merge PR creates manifest in GitOps repo
    
- ArgoCD/Flux syncs cluster state
    

---

### **7. Post-Deploy Validation**

- smoke tests
    
- SLO burn rate analysis
    
- service health checks
    
- auto-rollback patterns
    

---

## **37.1.2 Pipeline Pattern: GitOps (Preferred)**

Deploys are managed by:

- Argo CD
    
- Flux
    

CI pushes manifest changes → GitOps agents reconcile clusters.

Advantages:

- declarative state
    
- version-controlled desired state
    
- consistent across clusters
    
- diff-based reconciliation
    
- rollbacks via Git revert
    

---

## **37.1.3 Pipeline Pattern: “Push-Based” Deployments**

(_Not recommended unless required._)

CI deploys directly using kubectl:

```bash
kubectl apply -f deployment.yaml
```

Issues:

- mutable live state
    
- drift
    
- no versioning of changes
    
- inconsistent deployments between clusters
    

---

## **37.1.4 Infrastructure Pipeline Pattern (Terraform)**

Flow:

1. PR → `terraform plan`
    
2. Approval
    
3. Merge → `terraform apply`
    
4. Drift detection job nightly
    

Example workflow:

```yaml
- name: Terraform Plan
  run: terraform plan -out=tfplan

- name: Terraform Apply
  if: github.ref == 'refs/heads/main'
  run: terraform apply -auto-approve tfplan
```

---

## **37.1.5 Common Pipeline Anti-Patterns**

- long-lived CI tokens
    
- applying infra changes from PR (no approval gate)
    
- CI pipelines that depend on developer laptops
    
- storing credentials in plaintext CI variables
    
- not validating manifests before deployment
    
- no artifact signing
    

---

# **37.2 Cloud Build vs GitHub Actions vs GitLab**

Each CI system has strengths and trade-offs.

---

## **37.2.1 Google Cloud Build**

### Pros

- native IAM integration
    
- ultra-secure builds (zero compute access)
    
- parallel execution
    
- SLSA provenance support
    
- no build runners to manage
    

### Cons

- YAML syntax less flexible
    
- more difficult for complex workflows
    
- slower feedback loops for PRs
    

### Cloud Build Example

`cloudbuild.yaml`:

```yaml
steps:
- name: gcr.io/cloud-builders/git
  args: ["clone", "https://github.com/myorg/myrepo"]

- name: gcr.io/cloud-builders/docker
  args: ["build", "-t", "$IMAGE", "."]

images:
- "$IMAGE"

artifacts:
  objects:
    location: "gs://artifact-bucket/"
    paths: ["sbom.json"]
```

---

## **37.2.2 GitHub Actions**

### Pros

- flexible YAML pipelines
    
- rich ecosystem
    
- best UX for developer-facing repos
    
- OIDC support for GCP auth
    

### Cons

- risk if runners not isolated properly
    
- requires careful permissions scoping
    

### GitHub Actions Example

```yaml
- name: Authenticate to GCP
  uses: google-github-actions/auth@v1
  with:
    workload_identity_provider: ${{ secrets.WIF_PROVIDER }}
    service_account: ci-builder@myproj.iam.gserviceaccount.com
```

---

## **37.2.3 GitLab CI**

### Pros

- strong pipelines-as-code
    
- built-in container registry
    
- good enterprise features
    
- native GitLab runners
    

### Cons

- self-hosted runners maintenance
    
- complex YAML when scaling large monorepos
    

GitLab Example:

```yaml
build:
  stage: build
  script:
    - docker build -t $CI_REGISTRY_IMAGE:$CI_COMMIT_SHA .
    - docker push $CI_REGISTRY_IMAGE:$CI_COMMIT_SHA
```

---

## **37.2.4 Decision Matrix**

|Platform|Best For|
|---|---|
|**Cloud Build**|Fully GCP-native, secure builds, compliance-heavy orgs|
|**GitHub Actions**|Developer-friendly, open-source, moderate complexity|
|**GitLab CI**|Enterprise monorepos, integrated runner environments|

---

# **37.3 Promotion Between Environments**

Environment promotion ensures that:

- staging → production
    
- lower environments validate changes
    
- policies apply consistently
    
- no drifting state occurs
    

---

## **37.3.1 Golden Rule: Promote **Artifacts**, Not Source Code**

Image built in dev → tested → promoted to staging → promoted to prod.

Tag promotion:

```bash
gcloud artifacts docker tags add \
  gcr.io/myproj/api:$COMMIT_SHA \
  gcr.io/myproj/api:prod
```

---

## **37.3.2 GitOps Promotion Flow (Recommended)**

Pipeline:

1. Build & test image
    
2. Update staging manifest repo
    
3. ArgoCD syncs staging cluster
    
4. Validate staging
    
5. Promotion PR updates production manifest repo
    

Example PR content:

```diff
- image: gcr.io/myproj/api:oldsha
+ image: gcr.io/myproj/api:newsha
```

---

## **37.3.3 Terraform Promotion Workflow**

Terraform should:

- run against staging
    
- merge to main
    
- then apply to prod
    

Never copy state between envs.

---

## **37.3.4 Canary + Wave-Based Deployments**

For multi-region:

1. Deploy to `us-west1`
    
2. Monitor
    
3. Deploy to `us-central1`
    
4. Monitor
    
5. Deploy to `us-east1`
    

This reduces blast radius.

---

## **37.3.5 Promotion Anti-Patterns**

- separate pipelines building separate artifacts for staging/prod
    
- copying environments manually
    
- deploying untested manifests to prod
    
- re-building images in each environment (violates SLSA)
    

---

# **37.4 Pipeline Security**

CI/CD is a major attack vector.  
Pipeline security should be treated with the same rigor as production workloads.

---

## **37.4.1 OIDC Workload Identity Federation (No Static Keys)**

GitHub → GCP secure access:

```yaml
uses: google-github-actions/auth@v1
with:
  workload_identity_provider: ${{ secrets.WIF_PROVIDER }}
  service_account: ci-builder@myproj.iam.gserviceaccount.com
```

Benefits:

- zero long-lived credentials
    
- tightly scoped access
    
- provenance tied to exact workflow
    

---

## **37.4.2 Least Privilege IAM for CI Pipelines**

Split roles:

### Build Role

- push container images
    
- write artifacts
    

### Deploy Role

- apply manifests (GitOps controller)
    
- terraform apply (restricted)
    

### Disallow:

- project.owner
    
- storage.admin
    
- iam.serviceAccountTokenCreator (unless needed)
    

---

## **37.4.3 Artifact Signing (Cosign)**

CI signs images:

```bash
cosign sign gcr.io/myproj/api:$COMMIT_SHA
```

Then verifies before deploy:

```bash
cosign verify gcr.io/myproj/api:$COMMIT_SHA
```

---

## **37.4.4 Protecting the Build System Itself**

### Ensure:

- isolated runners
    
- immutability of build environment
    
- no privileged docker builds
    
- cache poisoning prevention
    

### Use:

- Cloud Build → sandboxed builds
    
- BuildKit with rootless mode
    
- Kaniko for non-privileged builds
    

---

## **37.4.5 Preventing Dependency Supply Chain Attacks**

- lockfiles (go.mod, package-lock.json)
    
- npm / pip audit
    
- SBOM generation
    
- dependency pinning
    
- automated dependency upgrading tools
    

---

## **37.4.6 Secure Secret Usage in CI**

Never store secrets in repo.

Use:

- Secret Manager
    
- GitHub Encrypted Secrets
    
- GitLab Protected Variables
    

Example secure secret retrieval:

```bash
gcloud secrets versions access latest --secret=db-password
```

---

## **37.4.7 CI Pipeline Security Anti-Patterns**

- using service account keys
    
- exposing secrets via echo or debug logs
    
- sharing CI tokens between repos
    
- storing credentials in Dockerfiles
    
- building images in privileged mode
    
- skipping signature verification
    
- pushing to prod registry without attestation
    

---

# **Chapter 38 — GitOps for Clusters & Mesh**

_(Expanded with clear senior-level explanations, Argo CD + Flux patterns, App-of-Apps best practices, service mesh GitOps workflows, drift detection, auto-healing, YAML manifests, kubectl commands, and real-world pitfalls.)_

GitOps applies declarative configuration + version-controlled desired state + automated reconciliation to Kubernetes and service mesh environments.  
It is the most reliable way to manage large-scale multi-cluster GKE and Istio deployments.

---

# **38.1 Argo CD Concepts**

Argo CD is a declarative GitOps controller for Kubernetes.  
It continuously monitors Git repositories and ensures the cluster matches what is defined in Git.

---

## **38.1.1 Core Argo CD Components**

### **1. Application**

Defines:

- what repo to sync from
    
- which path
    
- which cluster
    
- sync policy
    
- revision rules
    

Example: deploy an app from Git:

```yaml
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: checkout
  namespace: argocd
spec:
  destination:
    namespace: checkout
    server: https://kubernetes.default.svc
  project: default
  source:
    repoURL: https://github.com/myorg/platform-manifests
    path: services/checkout
    targetRevision: main
  syncPolicy:
    automated:
      prune: true
      selfHeal: true
```

---

### **2. AppProject**

Permissions + boundaries for Applications.

Example:

```yaml
apiVersion: argoproj.io/v1alpha1
kind: AppProject
metadata:
  name: team-checkout
  namespace: argocd
spec:
  sourceRepos:
  - https://github.com/myorg/*
  destinations:
  - namespace: checkout
    server: https://kubernetes.default.svc
```

---

### **3. Sync Policies**

Two modes:

- **manual**: human must click sync
    
- **automated**: sync + prune + self-heal
    

---

### **4. Prune**

Deletes Kubernetes objects that are removed from Git.

Ensures:

> Cluster == Git, not Cluster == Git + abandoned objects.

---

### **5. Self-Heal**

If someone changes a resource using kubectl, Argo CD reverts the change.

---

### **6. Health Checks**

Argo understands CRDs and can mark them:

- Healthy
    
- Degraded
    
- Suspended
    

Use for Istio resources or custom controllers.

---

## **38.1.2 Argo CD Managing Istio & Mesh Resources**

Mesh resources should be fully GitOps-controlled:

- Gateway
    
- VirtualService
    
- DestinationRule
    
- PeerAuthentication
    
- AuthorizationPolicy
    

Example:

```yaml
apiVersion: networking.istio.io/v1alpha3
kind: VirtualService
metadata:
  name: checkout-route
spec:
  hosts: ["checkout.example.com"]
  http:
  - route:
    - destination:
        host: checkout
        subset: v2
```

Argo CD continuously enforces this state.

---

## **38.1.3 Argo CD Pitfalls**

- Do not store secrets in Git unless encrypted (SOPS recommended).
    
- Avoid managing both Helm + Kustomize for the same resource path.
    
- Avoid multiple Argo Applications pointing to same namespace (race conditions).
    
- Enabling `automated` sync without `prune` → drift accumulates.
    
- Using monolithic repos → large blast radius.
    

---

# **38.2 Flux Concepts**

Flux is another GitOps engine built around controllers that reconcile:

- Git sources
    
- Helm releases
    
- image updates
    
- Kustomizations
    

Flux is more controller-native and modular than Argo.

---

## **38.2.1 Core Flux Resource Types**

### **1. GitRepository**

Points to a Git source:

```yaml
apiVersion: source.toolkit.fluxcd.io/v1
kind: GitRepository
metadata:
  name: platform-config
spec:
  interval: 1m
  url: https://github.com/myorg/platform-manifests
  ref:
    branch: main
```

---

### **2. Kustomization**

Applies manifests to a cluster:

```yaml
apiVersion: kustomize.toolkit.fluxcd.io/v1
kind: Kustomization
metadata:
  name: platform-core
spec:
  interval: 5m
  path: ./base/platform
  prune: true
  sourceRef:
    kind: GitRepository
    name: platform-config
```

---

### **3. HelmRelease**

GitOps-controlled Helm chart installs:

```yaml
apiVersion: helm.toolkit.fluxcd.io/v2beta1
kind: HelmRelease
metadata:
  name: istio-gateway
spec:
  chart:
    spec:
      chart: gateway
      version: 1.18.0
      sourceRef:
        kind: HelmRepository
        name: istio
  values:
    service:
      type: LoadBalancer
```

---

### **4. Image Automation**

Flux auto-bumps container tags:

```yaml
apiVersion: image.toolkit.fluxcd.io/v1beta1
kind: ImagePolicy
metadata:
  name: checkout-latest
spec:
  filterTags:
    pattern: '^v[0-9]+$'
  policy:
    semver:
      range: ">=1.0.0"
```

---

## **38.2.2 Flux for Multi-Cluster Mesh**

Flux can manage:

- mesh configuration
    
- cluster-wide policies
    
- ambient mesh configs (if used)
    
- gateways
    

---

## **38.2.3 Flux Pitfalls**

- excessive polling intervals → API throttling
    
- mixing GitRepository + bucket sources without structure
    
- Git branches as environment boundaries → hard to maintain
    
- enabling image automation without SLSA protections
    

---

# **38.3 App of Apps Pattern**

The App-of-Apps pattern is Argo CD’s recommended way to organize large platforms.  
One parent Application manages child Applications, each responsible for a well-defined domain.

---

## **38.3.1 Parent Application Example**

```yaml
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: platform-root
  namespace: argocd
spec:
  project: root
  source:
    repoURL: https://github.com/myorg/cluster-manifests
    path: clusters/prod
    targetRevision: main
  destination:
    namespace: argocd
    server: https://kubernetes.default.svc
  syncPolicy:
    automated:
      prune: true
      selfHeal: true
```

Inside `clusters/prod`, directory structure contains:

```
clusters/prod/
  00-namespaces/
  10-platform/
  20-mesh/
  30-apps/
```

Argo CD scans this directory and creates children apps.

---

## **38.3.2 Child App Example (Apps)**

```yaml
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: checkout-app
spec:
  destination:
    namespace: checkout
    server: https://kubernetes.default.svc
  source:
    repoURL: https://github.com/myorg/checkout-manifests
    path: ./k8s
    targetRevision: main
  syncPolicy:
    automated:
      prune: true
      selfHeal: true
```

---

## **38.3.3 Benefits of App-of-Apps**

- hierarchical structure
    
- clean separation of concerns
    
- cluster bootstrapping becomes trivial
    
- multi-cluster scaling
    
- consistent mesh configuration across clusters
    
- fast onboarding of new workloads
    

---

## **38.3.4 App-of-Apps Pitfalls**

- too many levels → debugging becomes difficult
    
- circular dependency risk
    
- mixing cluster-scoped and namespace-scoped configs
    
- storing secrets inside parent repos → privilege issues
    

---

# **38.4 Drift Detection & Auto-Heal**

GitOps guarantees that _Git = source of truth_ and _cluster = reflection of Git_.  
Drift occurs when:

- cluster changes out-of-band
    
- manual kubectl edits
    
- emergency hotfixes
    
- operator CRDs mutate specs
    

GitOps controllers detect and correct drift.

---

## **38.4.1 Drift Detection in Argo CD**

Argo detects drift by comparing:

- live manifests
    
- Git desired manifests
    

Check drift:

```bash
argocd app diff checkout
```

View cluster health:

```bash
argocd app get checkout
```

---

## **38.4.2 Auto-Healing in Argo CD**

Set self-healing:

```yaml
syncPolicy:
  automated:
    prune: true
    selfHeal: true
```

Auto-Heal does:

- revert manual kubectl edits
    
- reconcile mutated fields
    
- delete abandoned resources
    

---

## **38.4.3 Drift Detection in Flux**

Flux continuously reconciles:

```bash
flux reconcile kustomization platform-core
```

Check drift:

```bash
flux diff kustomization platform-core
```

---

## **38.4.4 Drift from CRDs (Operator-Induced Drift)**

Some operators mutate:

- annotations
    
- labels
    
- fields
    

Fix:

> Configure **ignored differences** in Argo CD.

Example:

```yaml
spec:
  ignoreDifferences:
  - kind: CustomResource
    jsonPointers:
    - /metadata/annotations
```

---

## **38.4.5 Multi-Cluster Drift Detection**

Use Argo CD + Argo CD cluster add:

```bash
argocd cluster add gke_prod
```

Monitor drift across:

- dev
    
- staging
    
- prod
    
- multi-region clusters
    

Mesh configs must remain identical across clusters—GitOps ensures this.

---

## **38.4.6 Common Drift Pitfalls**

- disabling prune → hundreds of abandoned resources
    
- hotfixing manifests directly in-cluster
    
- operators mutating manifests → noisy drift
    
- using kubectl apply within CI → fights GitOps
    
- no alerting when sync fails
    
- maintaining separate repos for each environment → drift explosion
    

---

# **Chapter 39 — Config & Feature Flag Management**

_(Expanded with senior-level clarity, GKE patterns, ConfigMap/Secret pitfalls, dynamic configuration techniques, runtime reload, GitOps, and feature-flag patterns used in large-scale SaaS systems.)_

Configuration is a first-class part of a cloud platform.  
Poor configuration practices cause outages, slow deployments, and unexpected cross-region behavior.  
This chapter provides practical, production-ready strategies for config management in Kubernetes + GCP.

---

# **39.1 ConfigMap & Secret Best Practices**

Kubernetes ConfigMaps and Secrets are common config storage mechanisms.  
However, they must be used **with discipline** to avoid outages, security leaks, and uncontrolled drift.

---

## **39.1.1 What Belongs in ConfigMaps (Non-Sensitive)**

ConfigMaps should contain:

- non-sensitive configuration
    
- tuning parameters
    
- feature toggles (if not sensitive)
    
- service-level configs
    
- environment variables
    
- config files
    

Example:

```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: checkout-config
data:
  LOG_LEVEL: "info"
  CHECKOUT_TIMEOUT_MS: "3000"
```

---

## **39.1.2 What Belongs in Secrets (Sensitive)**

Secrets store:

- passwords
    
- API keys
    
- tokens
    
- certificates
    
- OAuth credentials
    

Example:

```yaml
apiVersion: v1
kind: Secret
metadata:
  name: checkout-db
type: Opaque
stringData:
  user: checkout
  password: ${DB_PASSWORD}
```

⚠️ **Avoid using Kubernetes Secrets for long-term secret storage.**  
Prefer:

- **GCP Secret Manager + Workload Identity**
    
- sync secrets at runtime or via operator
    

---

## **39.1.3 Mount vs Environment Variables**

|Method|Pros|Cons|
|---|---|---|
|**Env vars**|simple; common|cannot update without restart|
|**Mounted files**|can update live (if app supports reload)|more complex|
|**Sidecar reloader**|dynamic refresh|added ops complexity|

---

## **39.1.4 Immutable ConfigMaps & Secrets (Recommended)**

Kubernetes supports **immutable** ConfigMaps:

```yaml
immutable: true
```

Advantages:

- no accidental mutation
    
- no surprise reloads
    
- safer GitOps workflows
    

---

## **39.1.5 Config Versioning Pattern**

Treat config changes like code changes:

```
config-v1/
config-v2/
```

Example Deployment referencing version:

```yaml
env:
- name: CONFIG_VERSION
  value: "v2"
```

---

## **39.1.6 GitOps + ConfigMaps**

Use Git to version config and let Argo/Flux manage rollout.

Never edit configs in-cluster.

---

## **39.1.7 Common Pitfalls**

- storing secrets in ConfigMaps
    
- huge ConfigMaps (100s of KB) → slow deployments
    
- mounting config without app reload support
    
- mutable ConfigMaps changing unexpectedly
    
- relying on manual `kubectl edit` → drift
    

---

# **39.2 Dynamic Configuration**

Dynamic configuration allows applications to update behavior **without restarting**.

Used when:

- tuning performance parameters
    
- enabling/disabling features
    
- adjusting routing rules
    
- modifying external integrations
    

---

## **39.2.1 Sidecar Reloaders**

Tools like Reloader or Stakater ReLoader watch changes to ConfigMaps/Secrets:

```yaml
annotations:
  reloader.stakater.com/auto: "true"
```

Automatic reload triggers:

- Deployment rollout
    
- Pod restarts
    

---

## **39.2.2 Application-Level Hot Reload**

The best approach is native application support.

Example (Go):

```go
viper.WatchConfig()
viper.OnConfigChange(func(e fsnotify.Event) {
  fmt.Println("Config reloaded:", e.Name)
})
```

Persist config in a mounted file.

---

## **39.2.3 Using GCP Runtime Config Alternatives**

GCP’s preferred dynamic config mechanisms:

- Firestore
    
- Cloud Run + Config API
    
- Secret Manager + version rotation
    
- Redis-based config storage
    

For dynamic config, consider:

- **Firestore** (simple KV config)
    
- **Cloud SQL** (for legacy apps)
    
- **Pub/Sub notifications** for fan-out
    

---

## **39.2.4 Dynamic Config via Cloud Storage + Notiﬁcations**

Pattern:

1. Config stored in GCS
    
2. App listens for Pub/Sub notif
    
3. App reloads config
    

---

## **39.2.5 Mesh-Level Dynamic Configuration**

Istio allows:

- route changes
    
- fault injection
    
- timeouts/retries
    
- subset traffic switching
    

all via applying CRDs.

Example VirtualService update (90/10 canary):

```yaml
http:
- route:
  - destination: { host: checkout, subset: v1, weight: 90 }
  - destination: { host: checkout, subset: v2, weight: 10 }
```

GitOps + mesh yields real-time config without redeploy.

---

## **39.2.6 Pitfalls of Dynamic Config**

- no audit trail if stored outside Git
    
- unexpected global changes from shared config
    
- too many reload triggers → cascading failures
    
- config push to prod without validation
    
- dynamic config shadowing static config (confusing behavior)
    

---

# **39.3 Feature Flags**

Feature flags allow:

- progressive rollout
    
- safe experimentation
    
- fast rollback
    
- A/B testing
    
- region-specific feature enablement
    

Flags should be:

- centrally managed
    
- version-controlled
    
- auditable
    
- tied to rollout pipelines
    

---

## **39.3.1 Code-Level Pattern for Feature Flags**

Example (Go):

```go
if featureflags.IsEnabled("new_checkout_flow") {
  runNewCheckout()
} else {
  runOldCheckout()
}
```

---

## **39.3.2 Feature Flag Providers**

### **1. ConfigMap-based (simple)**

Use a ConfigMap:

```yaml
data:
  new_checkout_flow: "false"
```

### **2. SaaS Providers**

- LaunchDarkly
    
- Flagsmith
    
- Unleash
    
- Optimizely
    

Advantages:

- real-time updates
    
- user targeting
    
- kill switches
    
- audit logs
    

### **3. Homegrown Feature Flag Service**

Common for enterprise-scale platforms.

Use:

- Firestore
    
- Redis
    
- Cloud SQL
    

---

## **39.3.3 GitOps Workflow for Feature Flags**

Flags should be committed to Git:

```
features/
  checkout/
    new-checkout-flow.yaml
```

Example:

```yaml
feature: new_checkout_flow
enabled_for:
  - region: us-central1
  - team: beta-testers
```

Benefits:

- rollout visibility
    
- auditability
    
- version control
    
- environment promotion
    

---

## **39.3.4 Canary Releases via Feature Flags**

Canary with 5% rollout:

```yaml
enabled_ratio: 0.05
```

Then increase gradually:

```yaml
enabled_ratio: 0.20
```

---

## **39.3.5 Feature Flag Rollback**

Rollback = flip a boolean.

Flags provide:

- instant rollback
    
- no pipeline needed
    
- decoupled from deploy cycle
    

This dramatically reduces risk when launching features.

---

## **39.3.6 Feature Flag Pitfalls**

- flags that are never removed (“flag debt”)
    
- mixing config and feature flags in same file
    
- storing flags in environment variables → requires redeploy
    
- flags without audit logs
    
- flags controlling security-sensitive behavior
    

---

# **39.4 Configuration Anti-Patterns**

This section lists real-world configuration design mistakes that cause outages.

---

## **39.4.1 Storing Secrets in ConfigMaps**

One of the most dangerous anti-patterns.

Example of bad behavior:

```yaml
data:
  db_password: hunter2
```

This leaks:

- to Git history
    
- to logs
    
- everywhere
    

---

## **39.4.2 Using Environment Variables for Sensitive Data**

Environment variables are:

- accessible via `/proc`
    
- exposed in crash dumps
    
- cached by some runtimes
    

Prefer:

- mounted secret files
    
- runtime secret fetch from Secret Manager
    

---

## **39.4.3 Using a Single Global ConfigMap for All Services**

This creates:

- accidental cross-team coupling
    
- global outages when config is wrong
    
- massive blast radius
    

Fix:

> One ConfigMap per service, per environment.

---

## **39.4.4 Mutable ConfigMaps Without Immutable Tagging**

Changing ConfigMaps in place breaks:

- auditability
    
- repeatability
    
- rollback
    

Use:

```yaml
metadata:
  name: checkout-config-v2
```

---

## **39.4.5 Storing Huge Files in ConfigMaps**

ConfigMap limit = 1 MB.  
Large configs slow:

- API server
    
- controllers
    
- kubelet downloads
    

Store large configs in:

- GCS
    
- mounted volumes
    

---

## **39.4.6 No Validation Step for Config**

Small typo → massive outage.

Fix:  
Validate config using:

- JSON schema
    
- static config loader
    
- unit tests
    
- CI linting
    

---

## **39.4.7 No Ownership of Configuration**

Symptoms:

- nobody knows who is allowed to change config
    
- cross-team accidental change
    
- unreviewed submissions
    

Fix:

- assign ownership per ConfigMap / feature flag
    
- require PR approval
    
- enforce write protections
    

---

## **39.4.8 Mixing Config with Deployment Manifests**

Avoid:

```yaml
config: |
  big blob
```

Reason:

- conflates config and deploy
    
- noisy diffs
    
- unnecessary restarts
    

Prefer dedicated config repos.

---

## **39.4.9 Feature Flags Buried in Code (No Central Control)**

Developers adding:

```go
if experimental {
```

or:

```python
if os.getenv("NEW_FEATURE") == "true":
```

is unscalable and unmanageable.

Use:

- Feature flag SDK
    
- central config
    
- GitOps flags
    

---

# **Chapter 40 — Testing Infrastructure**

_(Expanded with senior-level clarity, real-world patterns, Terratest examples, conformance tests for GKE + Istio, and actionable YAML / CI integration. Focused, non-redundant, deeply practical.)_

Infrastructure must be tested with the same rigor as application code.  
Without testing, Terraform modules drift, GKE clusters misconfigure themselves silently, mesh config breaks routing, and deployments fail at scale.

This chapter provides a complete framework for testing infrastructure.

---

# **40.1 Unit Testing**

Unit tests validate **syntax, structure, and logic** of infrastructure code without creating actual cloud resources.

They catch:

- missing variables
    
- mis-typed attributes
    
- malformed YAML
    
- invalid Terraform expressions
    
- policy violations
    

---

## **40.1.1 Terraform Unit Testing**

Run built-in validators:

```bash
terraform fmt -check
terraform validate
tflint --recursive
checkov -d .
```

### **Static Validation Pipeline Example**

```yaml
- name: Terraform Format
  run: terraform fmt -check

- name: Validate Terraform
  run: terraform validate

- name: Run TFLint
  run: tflint --recursive

- name: Checkov
  run: checkov -d .
```

These tests are fast (<5 seconds) and should run on every PR.

---

## **40.1.2 Kubernetes Manifests Unit Testing**

Use `kubeval` or `kubeconform`:

```bash
kubeconform -strict -ignore-missing-schemas manifests/
```

Detects:

- wrong API versions
    
- deprecated fields
    
- incorrect schema
    

---

## **40.1.3 Helm Chart Unit Testing**

Use `helm unittest`:

```bash
helm unittest ./charts/checkout
```

Example test:

```yaml
suite: test service
templates:
  - service.yaml
tests:
  - it: should set correct port
    asserts:
      - equal:
          path: spec.ports[0].port
          value: 8080
```

---

## **40.1.4 Rego Policy Unit Testing (OPA)**

For Gatekeeper/OPA policies, test rego functions:

`policy_test.rego`:

```rego
test_no_public_ingress {
  violation := deny({"cidr": "0.0.0.0/0"})
  count(violation) > 0
}
```

Run:

```bash
opa test .
```

---

## **40.1.5 Common Unit Testing Pitfalls**

- only testing Terraform, not YAML
    
- ignoring deprecated K8s versions
    
- insufficient validation before GitOps promotion
    
- no policy tests → bad config reaches cluster
    
- relying solely on CI “terraform plan”
    

---

# **40.2 Integration Testing**

Integration tests **provision actual infrastructure** and validate behavior end-to-end.

They test:

- Terraform modules
    
- GKE cluster creation
    
- node pools
    
- IAM bindings
    
- VPCs and routing
    
- mesh configs (Istio)
    
- K8s object lifecycle
    

The gold standard tool: **Terratest** (Go-based).

---

## **40.2.1 Terratest Example (Terraform Module)**

Example test creating a temporary VPC:

```go
package test

import (
  "testing"
  "github.com/gruntwork-io/terratest/modules/terraform"
)

func TestVpcCreation(t *testing.T) {
  opts := &terraform.Options{
    TerraformDir: "../modules/vpc",
  }

  terraform.InitAndApply(t, opts)
  defer terraform.Destroy(t, opts)

  vpc := terraform.Output(t, opts, "vpc_self_link")
  if vpc == "" {
    t.Fatal("VPC not created")
  }
}
```

**Best practice:**  
Create a **temporary GCP project** for integration tests to avoid polluting real environments.

---

## **40.2.2 Kubernetes Integration Tests**

After cluster creation:

```bash
kubectl apply -f manifests/test-pod.yaml
kubectl wait --for=condition=Ready pod/test-pod
kubectl logs test-pod
```

Test:

- DNS
    
- networking
    
- RBAC
    
- sidecar injection
    
- mesh routing
    

Example test manifest:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: test-pod
spec:
  containers:
  - name: curl
    image: curlimages/curl
    command: ["sleep", "3600"]
```

---

## **40.2.3 Integration Testing for Istio**

Test that VirtualServices route traffic correctly:

```bash
kubectl exec test-pod -- curl http://checkout.default.svc.cluster.local
```

Check subset routing based on DestinationRule.

---

## **40.2.4 Integration Tests for GCP IAM**

Verify role assignment:

```bash
gcloud projects get-iam-policy $TEST_PROJECT \
  --flatten="bindings[].members" \
  --format="table(bindings.role,bindings.members)" \
  | grep "roles/compute.viewer"
```

---

## **40.2.5 Common Integration Testing Pitfalls**

- tests not cleaning up → quota exhaustion
    
- running multiple tests in same project → flake risk
    
- testing in prod/staging (never do this)
    
- race conditions due to concurrent Terraform applies
    
- long-lived test environments with drift
    

---

# **40.3 Conformance Testing (K8s, Mesh)**

Conformance tests ensure the cluster and mesh adhere to standards and expected behaviors.

Mandatory for:

- multi-cluster consistency
    
- service mesh rollout
    
- platform upgrades
    
- new GKE versions
    
- custom admission policies
    

---

## **40.3.1 Kubernetes Conformance Tests (Sonobuoy)**

**Sonobuoy** runs upstream Kubernetes e2e conformance tests.

Install:

```bash
sonobuoy run --wait
sonobuoy retrieve .
sonobuoy results <file>
```

Tests validate:

- API server behavior
    
- RBAC
    
- scheduling
    
- CNI behavior
    
- networking consistency
    

---

## **40.3.2 Istio / Service Mesh Conformance**

Use **Istio’s built-in test suite** or custom mesh tests.

Check control plane installation:

```bash
istioctl verify-install
```

Check data plane:

```bash
kubectl exec test-pod -c istio-proxy -- pilot-agent status
```

Traffic tests:

```bash
kubectl exec test-pod -- curl -s http://service-a/health
```

Validate:

- mTLS
    
- authorization policies
    
- retries/timeouts
    
- locality load-balancing
    

---

## **40.3.3 Policy Conformance (OPA/Gatekeeper)**

Test Gatekeeper policies:

```bash
kubectl apply -f invalid-pod.yaml
# Expect admission denied
```

Example invalid pod:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: bad-pod
spec:
  containers:
  - name: nginx
    image: nginx
    securityContext:
      privileged: true
```

Expect:

```
Error from server: admission webhook "validation.gatekeeper.sh" denied the request
```

---

## **40.3.4 Mesh Conformance Across Regions**

When running multi-region mesh:

- ensure identical CRD versions
    
- enforce consistent DestinationRules
    
- validate discovery via endpoints
    

Test:

```bash
kubectl get endpoints -A | grep checkout
```

Check region-specific failover routes.

---

## **40.3.5 Common Conformance Pitfalls**

- skipping tests after GKE upgrades
    
- inconsistent mesh configs across clusters
    
- ignoring failed Gatekeeper audits
    
- missing test coverage for mTLS enforcement
    
- using outdated CRDs
    

---

# **40.4 Smoke Tests**

Smoke tests ensure that the **platform works immediately after deployment**.

They are lightweight, fast, and catch deployment breakers early.

Trigger smoke tests:

- after Terraform apply
    
- after GitOps sync
    
- after mesh config rollout
    
- after cluster upgrade
    

---

## **40.4.1 Example Smoke Test Suite**

### **1. API Server**

```bash
kubectl version --short
```

### **2. DNS Resolution**

```bash
kubectl exec test-pod -- nslookup google.com
kubectl exec test-pod -- nslookup checkout.default.svc.cluster.local
```

### **3. Pod Scheduling**

```bash
kubectl run smoke --image=busybox -- sleep 5
kubectl delete pod smoke
```

### **4. Sidecar Injection (Istio)**

```bash
kubectl get pod smoke -o jsonpath='{.spec.containers[*].name}'
```

Look for `istio-proxy`.

---

## **40.4.2 Application Smoke Tests**

Basic request:

```bash
curl https://api.example.com/health
```

Mesh-aware tests:

```bash
kubectl exec test-pod -- curl http://checkout/health
```

---

## **40.4.3 Terraform Smoke Tests**

After applying infra:

- GKE cluster active
    
- VPC routes correct
    
- Cloud NAT functional
    
- IAM permissions assigned
    

Example:

```bash
gcloud container clusters describe prod-cluster
```

---

## **40.4.4 Automated Smoke Test Job**

GitHub Actions:

```yaml
- name: Run Smoke Tests
  run: ./scripts/smoke-tests.sh
```

Cloud Build:

```yaml
steps:
- name: gcr.io/cloud-builders/kubectl
  args: ["apply", "-f", "smoke/"]
```

---

## **40.4.5 Smoke Test Anti-Patterns**

- running deep integration tests as smoke tests → slow pipeline
    
- executing smoke tests against production only
    
- test-rooted pods not cleaned up
    
- no alerting on failed smoke tests
    
- no smoke tests for mesh routing
    

---

# **Chapter 41 — How GCP Bills You**

_(Expanded with senior-level clarity, real pricing mechanics, quota behaviors, kubectl/gcloud snippets for cost inspection, and practical pitfalls. No redundancy. No cross-chapter references.)_

Understanding how GCP bills your platform is essential for designing cost-efficient architectures and predicting the operational impact of scaling decisions.  
This chapter breaks down billing in four independent domains: **Compute**, **Networking**, **Storage**, and **Managed Services**.

---

# **41.1 Compute**

GCP compute billing applies to VM-based workloads (GKE nodes), serverless compute (Cloud Run), and GPUs/TPUs.

---

## **41.1.1 GKE Node Pool Billing**

GKE charges **per node VM**, not per pod.

You pay for:

- **vCPU + RAM** (per-second with a 1-minute minimum)
    
- **Persistent Disk** attached to nodes
    
- **OS cost** (Container-Optimized OS = free; Windows nodes = billed)
    
- **GPUs** attached to nodes
    
- **GKE control plane (only for Autopilot regional clusters)**
    

### **Inspect node pool machine types**

```bash
gcloud container node-pools list --cluster=prod-gke
```

### Example cost estimation pattern

If you run a **3-node n2-standard-4** regional pool:

- 4 vCPU × $0.0528/hr
    
- 16 GB RAM × $0.0071/hr
    
- replicated across 3 zones (regional cluster) → 3× cost
    

Total: (4 × .0528 + 16 × .0071) × 3 nodes ≈ $1.03/hr → $744/mo

---

## **41.1.2 GKE Autopilot Billing Model**

Autopilot bills **per pod request**, not per node.

You pay for:

- CPU & Memory requested in PodSpec
    
- ephemeral storage
    
- GKE control plane included
    

Example Pod:

```yaml
resources:
  requests:
    cpu: "500m"
    memory: "1Gi"
```

You pay only for 0.5 vCPU and 1 GiB RAM even if node allocates more.

---

## **41.1.3 Sustained Use Discounts (SUD)**

Automatic, applied monthly.

If a VM runs:

- **25%** of the month → ~20% discount
    
- **50%** → ~40% discount
    
- **75%+** → ~60% discount
    

Great for:

- GKE system node pools
    
- databases
    
- gateways
    

---

## **41.1.4 Committed Use Discounts (CUD)**

Commit to 1 or 3 years of usage (specific machine Family or any compute).

Two types:

- **Resource-based CUD** (tied to machine family)
    
- **Spend-based CUD** (flexible, applies across machines)
    

Example purchasing:

```bash
gcloud compute commitments create prod-cud \
  --type=MEMORY_OPTIMIZED \
  --resources=RAM=256,CPU=64 \
  --region=us-central1
```

---

## **41.1.5 GPUs & TPUs**

Charged **hourly regardless of usage**.

Example GPU cost:

- NVIDIA T4 → ~$0.35/hr
    
- A100 → up to ~$3.50/hr
    

Pitfalls:

- idle GPU nodes → extremely expensive
    
- forgetting to use node auto-provisioning
    
- driver DaemonSet causing nodes to stay active
    

---

## **41.1.6 Compute Cost Pitfalls**

- over-requesting pod resources (Autopilot overbilling)
    
- using burstable E2 instead of spot preemptible → unnecessary cost
    
- leaving node pools at minimum 3 per zone in regional clusters
    
- clusters created without autoscaling or with PodDisruptionBudgets blocking downscale
    
- storing logs on PDs instead of Cloud Logging → wasteful
    

---

# **41.2 Networking**

Networking costs are often the **largest unexpected portion** of cloud bills.

---

## **41.2.1 Egress Types**

GCP charges egress based on destination:

|Destination|Billing|Notes|
|---|---|---|
|Same VPC|**Free**|No cost, even across zones|
|Same Region (Diff VPC)|Small charge|VPC Peering → discounted|
|Cross-Region|**High cost**|$0.01 – $0.13/GB|
|Internet Egress|Highest|Varies by continent|
|Cloud CDN Egress|Reduced|Cached content reduces cost|
|Interconnect|Cheapest|Flat fee + low per-GB|

---

## **41.2.2 Checking Egress in GKE**

Check outbound IP traffic via Flow Logs:

```bash
gcloud logging read 'logName="projects/myproj/logs/compute.googleapis.com%2Fvpc_flows"' \
  --limit=20 --format=json
```

---

## **41.2.3 Inter-Region Cluster Traffic**

Multi-region Istio/GKE platforms often incur:

- service-to-service egress
    
- control plane discovery traffic
    
- multi-region SQL replication fees
    

Example egress cost:  
`us-central1 → us-east1`: ~$0.01/GB (low)  
`us-central1 → europe-west1`: ~$0.11/GB (high)

---

## **41.2.4 Load Balancing Costs**

You pay for:

- L7 LB forwarding rules
    
- Traffic processed (per GB)
    
- Cloud Armor evaluations
    
- NEG backends (regional vs. zonal)
    

Example LB cost audit:

```bash
gcloud compute forwarding-rules list
```

---

## **41.2.5 NAT Gateway Charges**

Cloud NAT charges:

- hourly gateway fee
    
- per-GB egress
    
- per NAT IP allocation
    

Use logging to analyze NAT volume:

```bash
gcloud compute routers nats list --region=us-central1 --router=nat-router
```

---

## **41.2.6 VPC Peering Costs**

Peering egress is:

- symmetric
    
- cheaper than inter-region egress
    
- no firewall rule enforcement across peerings
    

---

## **41.2.7 Networking Cost Pitfalls**

- running multi-region databases without understanding replication egress
    
- mesh cross-region traffic due to misconfigured locality load balancing
    
- high NAT egress from GKE Autopilot pods
    
- using external LB for internal service-to-service calls
    
- exporting logs from multiple regions cross-region → charges multiply
    

---

# **41.3 Storage**

GCP storage includes:

- block storage (PD)
    
- object storage (GCS)
    
- database storage (CloudSQL, Bigtable, Spanner)
    

Billing varies by class, retention, and access patterns.

---

## **41.3.1 Persistent Disks (PD)**

Charged based on:

- provisioned size (GiB per month)
    
- type (standard, SSD, balanced)
    
- snapshots stored
    

Example:

Balanced PD: ~$0.17/GB-month  
Regional PD: ~2× cost (replicated across zones)

Check disk usage:

```bash
gcloud compute disks list
```

### Snapshots

Incremental but retention affects cost:

```bash
gcloud compute snapshots list
```

Pitfall:  
**Automated nightly snapshots → hundreds of unused snapshots → big bill.**

---

## **41.3.2 Cloud Storage (GCS)**

Billed for:

- stored data
    
- retrieval
    
- operations (Class A/B)
    
- egress
    
- multi-region premium
    

Example classes:

- Standard
    
- Nearline
    
- Coldline
    
- Archive
    

Best practice:

> Use Standard only for frequently accessed workloads.

---

## **41.3.3 BigQuery**

BigQuery charges for:

- **storage** (per TB-month)
    
- **query processing** (per TB scanned)
    

Example cost-reduction strategy:

```sql
SELECT *
FROM mytable
WHERE event_date >= DATE_SUB(CURRENT_DATE(), INTERVAL 7 DAY)
```

Using partition pruning to avoid scanning whole table.

---

## **41.3.4 CloudSQL Storage**

You pay for:

- provisioned storage
    
- backups (7-day retention default)
    
- high availability (sync replication) doubles cost
    

Check DB size:

```bash
gcloud sql instances describe checkout-db
```

---

## **41.3.5 Storage Pitfalls**

- leaving orphaned PDs after delete
    
- multi-region GCS where regional is enough
    
- incorrectly configured BigQuery partitioning → queries scan TBs
    
- CloudSQL HA replicas in multiple regions incurring egress
    
- storing logs in GCS instead of Cloud Logging (more expensive)
    

---

# **41.4 Managed Services**

Managed services hide operational overhead but add significant cost.  
Understanding billing models helps avoid surprise invoices.

---

## **41.4.1 Cloud SQL**

You pay for:

- instance size (CPU/RAM)
    
- storage
    
- HA (double cost)
    
- backups
    
- network egress
    

Example:

```bash
gcloud sql instances describe checkout-db
```

---

## **41.4.2 Cloud Run**

You pay only for:

- CPU time
    
- memory time
    
- request count
    
- egress
    

Example cost-oriented config:

```yaml
apiVersion: serving.knative.dev/v1
kind: Service
metadata:
  name: checkout
spec:
  template:
    spec:
      containerConcurrency: 80
      containers:
      - image: gcr.io/myproj/checkout
        resources:
          limits:
            cpu: "1"
            memory: "512Mi"
```

---

## **41.4.3 Pub/Sub**

Charges for:

- message ingestion
    
- delivery attempts
    
- retained messages (Lite)
    
- topic/storage
    

---

## **41.4.4 Cloud Logging / Cloud Monitoring**

Big hidden cost source.

Billing for:

- ingested logs
    
- stored logs
    
- exported logs (if routed to GCS or BQ)
    

List logging sinks:

```bash
gcloud logging sinks list
```

Pitfall:

> Exporting logs from multiple regions into a single BigQuery dataset → DOUBLE egress charges.

---

## **41.4.5 Cloud Armor**

Costs:

- policies
    
- requests evaluated
    
- advanced rules
    

Mesh Ingress + Cloud Armor = per-request charge.

---

## **41.4.6 Cloud Load Balancing**

Charges:

- forwarding rule
    
- per GB processed
    
- per million L7 requests
    
- NEG backends
    

Check:

```bash
gcloud compute backend-services list
```

---

## **41.4.7 Spanner**

Spanner charges:

- nodes (or processing units)
    
- storage
    
- backup
    
- inter-region replication
    

Minimum node: **1 node per region** → expensive.

---

## **41.4.8 Managed Services Pitfalls**

- importing huge logs into BigQuery = massive cost
    
- forgetting about autoscaling limits on Pub/Sub → overprovision
    
- HA CloudSQL in multi-region setups → unexpected egress
    
- Spanner used prematurely → high baseline cost
    
- Cloud Run with too many container concurrency = scaling spikes (cost)
    
- GKE Managed Istio control plane with multi-cluster = additional per-hour cost
    

---

# **Chapter 42 — Cost-Efficient Network Design**

_(Expanded with senior-level clarity, real pricing behaviors, command examples, and practical patterns for minimizing cross-region and internet egress costs in GCP. No redundancy. No references to other chapters.)_

Cost-efficient network design requires deliberate architecture choices.  
Networking is one of the **largest hidden cost drivers** in GCP—often surpassing compute.

This chapter provides a practical, production-focused approach to minimizing network costs through:

- smart peering
    
- strategic caching
    
- egress control
    
- multi-region awareness
    

---

# **42.1 Peering**

Peering allows private, low-cost connectivity between networks.  
Choosing the right peering strategy eliminates unnecessary NAT and inter-region charges.

---

## **42.1.1 VPC Peering**

**VPC Peering** connects two VPC networks using Google’s backbone.  
It is:

- regional
    
- non-transitive
    
- low-latency
    
- low-cost
    

**Cost model:**

- **Ingress**: free
    
- **Egress**: discounted rate (cheaper than external egress)
    

**Use cases:**

- shared services (DNS, IAM metadata)
    
- private API backends
    
- multi-project architectures
    

### **Creating VPC Peering**

```bash
gcloud compute networks peerings create app-to-shared \
  --network=app-vpc \
  --peer-network=shared-vpc \
  --export-custom-routes \
  --import-custom-routes
```

### **Pitfalls**

- **Non-transitive**: traffic between VPC A → B → C will **NOT** route
    
- No firewall enforcement across peer → design carefully
    

---

## **42.1.2 Private Service Connect (PSC)**

PSC allows private access to:

- internal services
    
- GCP APIs
    
- producer-consumer services
    

PSC shifts traffic from **internet egress pricing → internal private pricing**, which is significantly cheaper.

### **Creating a PSC Endpoint**

```bash
gcloud compute forwarding-rules create psc-endpoint \
  --network default \
  --region us-central1 \
  --target-service-attachment projects/123/regions/us-central1/serviceAttachments/app
```

### **Cost win:**

- eliminates NAT egress
    
- avoids per-GB internet charges
    

---

## **42.1.3 Interconnect / Partner Interconnect**

Use when bandwidth > 10 TB/mo.

Interconnect charges:

- flat hourly fee per link
    
- very low egress cost
    

Typical vs Interconnect example:

- standard egress: ~$0.12/GB
    
- Interconnect: ~$0.01–$0.03/GB
    

### **Pitfalls**

- unused links still billed
    
- multi-region Interconnect = double the cost baseline
    

---

## **42.1.4 Cloud VPN**

VPN egress costs the same as normal internet egress.  
Use only when:

- traffic is small
    
- no Interconnect available
    
- short-term migration
    

---

# **42.2 CDN / Caching**

Caching is one of the **strongest cost reducers** in network architecture.

Every cache hit eliminates:

- backend CPU
    
- backend bandwidth
    
- cross-region egress
    
- database queries
    

---

## **42.2.1 Cloud CDN**

Cloud CDN reduces:

- **internet egress** from VMs/GKE by serving cached content
    
- **load on backend services**
    
- **latency for global users**
    

### **Enable CDN on a backend service**

```bash
gcloud compute backend-buckets update static-content \
  --enable-cdn
```

### Benefits

- traffic delivered from Google edge POP → minimal egress
    
- cache hit ratios >80% produce massive savings
    
- works with GKE NEG backends
    

---

## **42.2.2 Using Edge Caches With GKE Ingress**

Enable CDN via annotation:

```yaml
metadata:
  annotations:
    cloud.google.com/neg: '{"ingress": true}'
    cloud.google.com/cdn: "enabled"
```

### Real-world effect:

A 100 MB static file downloaded 1M times:

- Without CDN → 100 TB egress
    
- With CDN → backend sees only ~100 MB (first request)
    

---

## **42.2.3 Internal Caching Layers**

Internal caches reduce **inter-region** traffic:

- Memorystore (Redis)
    
- In-memory caches (Envoy shared config)
    
- CDN-like caching inside services
    

**Pattern:**  
Cache data that is:

- frequently accessed
    
- globally served
    
- expensive to fetch
    

---

## **42.2.4 Pitfalls with CDN/Caching**

- APIs are **not cache-friendly** unless designed for it
    
- caching sensitive content requires auth-aware cache keys
    
- cache invalidation must be explicit
    

---

# **42.3 Egress Controls**

Most unexpected cost spikes come from uncontrolled outbound traffic.  
A good platform includes **guardrails** that restrict where traffic can go.

---

## **42.3.1 Using Firewall Rules to Prevent Costly Egress**

Example: block pods from hitting the internet accidentally:

```bash
gcloud compute firewall-rules create deny-internet \
  --network=prod-vpc \
  --priority=100 \
  --direction=EGRESS \
  --action=DENY \
  --destination-ranges=0.0.0.0/0 \
  --enable-logging
```

Pods must then go through:

- Cloud NAT (intentional)
    
- VPC peering
    
- PSC endpoints
    

---

## **42.3.2 NAT Logging for Egress Visibility**

Enable NAT logging:

```bash
gcloud compute routers nats update nat-1 \
  --region=us-central1 \
  --enable-logging
```

Analyze traffic:

```bash
gcloud logging read 'resource.type="nat_gateway"' \
  --limit=20 --format=json
```

This instantly shows:

- which workload
    
- which destination
    
- volume
    

---

## **42.3.3 DNS + Private Zones to Prevent External Calls**

Force services to use internal private endpoints:

```bash
gcloud dns managed-zones create internal-api \
  --visibility=private \
  --networks=prod-vpc
```

Then map external APIs to **internal private** versions where possible.

---

## **42.3.4 Istio Egress Policies**

Mesh allows **fine-grained egress control**.

Example: block all external traffic by default:

```yaml
apiVersion: security.istio.io/v1beta1
kind: AuthorizationPolicy
metadata:
  name: block-egress
spec:
  action: DENY
  rules:
  - to:
    - operation:
        ports: ["80","443"]
```

Allowlisted destinations are added explicitly.

---

## **42.3.5 Resource Policies**

Limit egress on a per-namespace basis.

Example using Gatekeeper:

```yaml
violation:
  msg: "External egress not allowed"
```

---

## **42.3.6 Egress Pitfalls**

- pods hitting **public endpoints** for internal GCP services
    
- cross-region API calls due to misconfigured DNS
    
- autoscaling fleets generating unexpected NAT traffic
    
- unbounded retries causing repeated egress spikes
    
- NPM/Yarn/apt inside containers downloading large packages
    

---

# **42.4 Multi-Region Cost Pitfalls**

Multi-region architectures multiply network and storage costs.  
This section highlights the most expensive failure modes.

---

## **42.4.1 Cross-Region Service-to-Service Calls**

Every request between regions = egress cost.

If a microservice calls another microservice located in another region:

```
us-east1 → us-central1
```

Even internal VPC traffic incurs cross-region charges.

**Fix:**

- local replicas
    
- locality load balancing
    
- route rules that enforce regional stickiness
    

---

## **42.4.2 Stateful Systems Replication**

Databases replicate across regions:

- CloudSQL
    
- Spanner
    
- Bigtable
    
- Redis Cluster
    
- Kafka over VPN
    

**Replication egress is billed.**

Example:  
CloudSQL replicas → each change shipped cross region.

---

## **42.4.3 Multi-Region Logging & Monitoring**

Centralizing logs in one region:

```
eu-west1 cluster → us-central1 BigQuery
```

Produces:

- cross-region egress
    
- BigQuery ingestion cost
    
- high storage cost
    

Best practice:

- regional Sinks
    
- aggregate only metrics globally
    

---

## **42.4.4 Multi-Region GKE Control Plane Traffic**

Mesh/Ingress controllers exchanging:

- endpoint discovery
    
- health checks
    
- config sync
    

can create **unexpected cross-region chatter**.

Fix:

- run **isolated meshes per region**, only failover routes cross regions
    
- ensure NEGs are regionally scoped
    

---

## **42.4.5 Shared Services With No Regional Copy**

Example:

- user auth service only runs in us-central1
    
- Europe traffic calls it directly
    

This results in:

- high latency
    
- expensive egress
    

---

## **42.4.6 Using Global Load Balancers Incorrectly**

A global LB routing _all traffic_ to a single backend region creates:

- surge load
    
- multi-region egress
    
- unnecessary inter-region latency
    

Fix:

- enable **backend per region**
    
- enable **geo-based routing**
    

---

## **42.4.7 Backup & Disaster Recovery Replication**

Copying GCS buckets across regions:

```bash
gsutil cp gs://bucket-a/* gs://bucket-b/
```

This is **fully billed egress**.

Better design:

- use multi-region bucket only when absolutely required
    
- or use regional buckets with selective export
    

---

## **42.4.8 Multi-Region Pitfall Summary**

The highest-cost scenarios are:

- running a DB in region A and apps in region B
    
- global Cloud Logging sinks
    
- centralized BigQuery without partitioned ingestion
    
- cross-region synchronous RPC calls
    
- unbounded mesh locality failover
    

---

# **Chapter 43 — GKE Cost Optimization**

_(Expanded with senior-level depth, GCP billing mechanics, YAML examples, scheduling techniques, autoscaling interactions, and practical cost-saving patterns for production platforms.)_

Cost-optimizing GKE is about using the **right nodes**, **right sizing**, **right workload placement**, and **right availability strategy**.

This chapter breaks down the four most impactful levers:

- **Use cheaper nodes where possible (Spot/Preemptible).**
    
- **Pick the right machine family and topology.**
    
- **Right-size workloads based on real resource usage.**
    
- **Use bin-packing and scheduling to reduce waste.**
    

---

# **43.1 Spot / Preemptible Nodes**

Spot (Autopilot) or Preemptible (Standard GKE) nodes are discounted VMs with limited lifetime and no availability guarantees.

They are the **single biggest compute cost reduction tool** for GKE workloads.

**Discount:**  
60–91% cheaper vs on-demand.

---

## **43.1.1 When to Use Spot/Preemptible**

They are ideal for:

- stateless workloads
    
- batch jobs
    
- workloads with retry logic
    
- CI pipelines
    
- analytics workers
    
- image processing pipelines
    

Avoid using them for:

- control plane dependencies
    
- critical low-latency services
    
- long-running stateful workloads
    
- mesh ingress gateways (unless replicated heavily)
    

---

## **43.1.2 Enabling Preemptible Nodes (Standard GKE)**

```bash
gcloud container node-pools create spot-pool \
  --cluster=prod-gke \
  --machine-type=e2-standard-4 \
  --num-nodes=3 \
  --preemptible
```

---

## **43.1.3 Using Spot with GKE Autopilot**

Autopilot pod spec:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: spot-pod
spec:
  nodeSelector:
    cloud.google.com/gke-spot: "true"
  containers:
  - name: worker
    image: my-worker:latest
```

---

## **43.1.4 Tainting Spot Nodes to Control Placement**

Ensure only tolerant workloads run on spot:

```bash
kubectl taint nodes -l cloud.google.com/gke-preemptible=true \
  spot=true:NoSchedule
```

Workloads that tolerate:

```yaml
tolerations:
- key: "spot"
  operator: "Equal"
  value: "true"
  effect: "NoSchedule"
```

---

## **43.1.5 Best Practices**

✔ Use Horizontal Pod Autoscaler (HPA) so pods reschedule quickly  
✔ Run heterogeneous node pools (mixed on-demand + spot)  
✔ Keep replicas >2 so eviction does not cause outages  
✔ Use PodDisruptionBudgets optimized for eviction scenarios

---

## **43.1.6 Common Pitfalls**

- placing critical workloads on spot nodes
    
- spot nodes causing cascading restarts
    
- not reserving capacity in other pools → scheduling failures
    
- assuming spot nodes live >24h (they don’t)
    

---

# **43.2 Node Type Selection**

Picking the right machine family dramatically changes cost per core and cost per GB of RAM.

---

## **43.2.1 Machine Families Overview**

|Family|Best for|Notes|
|---|---|---|
|**E2**|general workloads|cheapest; variable CPU|
|**N2**|stable workloads|good balance; predictable performance|
|**N2D**|CPU-heavy|AMD; cheaper per vCPU|
|**C2/C3**|high performance|expensive but fast|
|**T2D**|cloud-native microservices|VM-based ARM; very cost-efficient|
|**Memory-optimized (M)**|large DBs|extremely expensive|

---

## **43.2.2 Real-World Selection Strategy**

### **Use E2 for:**

- ingesters
    
- workers
    
- stateless services
    

### **Use N2/N2D for:**

- latency-sensitive workloads
    
- secure workloads requiring stability
    
- mesh gateways
    

### **Use C2/C3 only if:**

- high-performance workloads need it
    

---

## **43.2.3 Choosing vCPU:Memory Ratio**

Microservices often need:

- more CPU per GB than default
    
- faster per-core performance
    

Example breakdown:

- High-CPU nodes → more pods per node
    
- High-memory nodes → fewer nodes overall
    

---

## **43.2.4 Heterogeneous Node Pools**

Use multiple pools:

```bash
gcloud container node-pools create web-pool --machine-type=e2-standard-4
gcloud container node-pools create metric-pool --machine-type=c2-standard-4
gcloud container node-pools create batch-pool --machine-type=e2-highcpu-16
```

Pods select via `nodeSelector` or affinities.

---

## **43.2.5 Best Practices**

✔ Use ARM (T2D / TAU) where possible: **~30% cheaper**  
✔ Use “balanced” PD instead of SSD for node boot disks  
✔ Put stateful workloads onto custom machine types with tuned ratios

---

## **43.2.6 Common Pitfalls**

- using N1 family (legacy, more expensive)
    
- using oversized nodes where many cores sit idle
    
- CPU-throttling in E2 mistaken for app issues
    
- accidental use of Windows nodes (~2× cost)
    

---

# **43.3 Workload Rightsizing**

Right-sizing means aligning CPU/memory **requests** and **limits** to actual usage.

Over-requesting = most common GKE waste.

---

## **43.3.1 Understanding Requests vs Limits**

`requests`: determines scheduling, **what you pay for in Autopilot**  
`limits`: determines throttling/kill thresholds

Example workload:

```yaml
resources:
  requests:
    cpu: "500m"
    memory: "256Mi"
  limits:
    cpu: "2"
    memory: "512Mi"
```

---

## **43.3.2 How to Right-Size Workloads**

Use:

- GKE Metrics API
    
- Cloud Monitoring
    
- Vertical Pod Autoscaler (VPA) in recommendation mode
    
- Goldilocks (a UI on top of VPA recommendations)
    

### Inspect usage:

```bash
kubectl top pod -n checkout
```

### VPA recommendation:

```bash
kubectl describe vpa checkout-vpa
```

---

## **43.3.3 Rightsizing Strategy**

1. Collect data for 7–14 days
    
2. Set CPU requests ~80th percentile
    
3. Set memory requests ~90–95th percentile
    
4. Tune limits carefully:
    
    - CPU limit ~2–4× request
        
    - Memory equal to request unless your app spikes
        

---

## **43.3.4 Enforcing Limits and Quotas**

Namespace LimitRanges prevent over-requesting:

```yaml
apiVersion: v1
kind: LimitRange
metadata:
  name: default
spec:
  limits:
  - defaultRequest:
      cpu: "200m"
      memory: "128Mi"
```

---

## **43.3.5 Resource Anti-Patterns**

❌ Requests = Limits (leads to OOM/Kill or CPU starvation)  
❌ “Just give it 2 CPU and 2Gi always”  
❌ Oversized limits causing throttling burst surprises  
❌ No VPA or monitoring pipeline

---

## **43.3.6 Rightsizing Pitfalls**

- VPA applied in update mode conflicting with Horizontal Pod Autoscaler
    
- memory overcommit leading to node eviction storms
    
- no autoscaling thresholds → containers permanently underutilized
    

---

# **43.4 Bin Packing & Scheduling**

Optimizing pod placement reduces unused CPU/memory on nodes.  
This lowers node count → lowers compute cost.

---

## **43.4.1 Pod Affinity / Anti-Affinity for Cost Goals**

Examples:

### Spread replicas across nodes (HA):

```yaml
affinity:
  podAntiAffinity:
    preferredDuringSchedulingIgnoredDuringExecution:
    - weight: 100
      podAffinityTerm:
        topologyKey: "kubernetes.io/hostname"
        labelSelector:
          matchLabels:
            app: checkout
```

### Pack latency-insensitive workloads together:

```yaml
affinity:
  podAffinity:
    preferredDuringSchedulingIgnoredDuringExecution:
    - weight: 50
      podAffinityTerm:
        topologyKey: "kubernetes.io/hostname"
        labelSelector:
          matchLabels:
            app-type: worker
```

---

## **43.4.2 Taints/Tolerations for Dedicated Pools**

Ensure pods land in the cheapest possible pool.

Example: batch pool tainted:

```bash
kubectl taint nodes -l pool=batch batch=true:NoSchedule
```

Workloads:

```yaml
tolerations:
- key: "batch"
  operator: "Equal"
  value: "true"
  effect: "NoSchedule"
```

---

## **43.4.3 Pod Priority Classes**

Lower-priority workloads are placed last and preempted first.

```yaml
apiVersion: scheduling.k8s.io/v1
kind: PriorityClass
metadata:
  name: low-cost
value: 1000
```

Assign pods:

```yaml
priorityClassName: low-cost
```

---

## **43.4.4 Node Auto-Provisioning (NAP)**

NAP automatically creates right-sized node pools for workloads.

Enable:

```bash
gcloud container clusters update prod-gke \
  --enable-autoprovisioning \
  --autoprovisioning-cpu-min=2 \
  --autoprovisioning-cpu-max=100
```

### NAP Cost Benefits

- automatically uses cheaper families
    
- scales down unused node pools
    
- handles bin packing automatically
    

### NAP Pitfalls

- can create large numbers of small pools
    
- must restrict machine families or it picks expensive types
    

---

## **43.4.5 Bin-Packing with Topology Spread Constraints**

Topology spread allows cost-optimized packing _without_ sacrificing HA.

```yaml
topologySpreadConstraints:
- maxSkew: 1
  topologyKey: kubernetes.io/hostname
  whenUnsatisfiable: ScheduleAnyway
  labelSelector:
    matchLabels:
      role: worker
```

This lets Kubernetes pack pods tightly but fail across nodes.

---

## **43.4.6 Using VPA + HPA Together for Cost Optimization**

Best practice:

- Enable VPA in **recommendation-only mode**
    
- HPA handles scaling
    
- Apply VPA recommendations manually
    

---

## **43.4.7 Common Bin-Packing Pitfalls**

- anti-affinity rules that prevent nodes from filling → overprovision
    
- PDBs making nodes impossible to downscale
    
- strict YAML constraints causing scheduling failures
    
- tolerating spot nodes accidentally (critical workloads run on them)
    
- large node sizes causing fragmentation (unused resources per node)
    

---

# **Chapter 44 — Cost Visibility & Chargeback**

_(Expanded with senior-level clarity, real-world patterns, fully commented gcloud commands, YAML examples, BigQuery SQL for chargeback, and practical dashboards & alerts.)_

Cost visibility is mandatory for operating a multi-team, multi-cluster Kubernetes platform.  
Without systematic tagging, export pipelines, dashboards, and automated alerts, spend grows uncontrollably and becomes politically impossible to attribute.

This chapter provides a complete framework for cost visibility and chargeback.

---

# **44.1 Labeling Strategy**

Labels are the foundation of all cost visibility.  
Every GCP resource that supports labels must follow a **strict, enforced taxonomy**.

---

## **44.1.1 Required Label Taxonomy**

Recommended labels:

|Label|Purpose|
|---|---|
|**team**|Chargeback owner|
|**service**|Microservice attribution|
|**env**|dev/staging/prod|
|**cost-center**|Finance integration|
|**owner**|Engineering point-of-contact|
|**compliance-tier**|PCI, PII, HIPAA, etc|
|**lifecycle**|ephemeral, long-lived, test|

These labels must exist on:

- GCE instances (GKE nodes)
    
- Persistent Disks
    
- Forwarding rules
    
- VPC networks
    
- Subnets
    
- NAT configs
    
- Cloud Run / Cloud SQL
    
- BigQuery datasets
    
- Load balancers (automated via NEG labels)
    

---

## **44.1.2 Enforcing Labels in GKE with PodLabels**

Workloads must carry meaningful labels:

```yaml
metadata:
  labels:
    team: checkout
    service: checkout-api
    env: prod
```

Use admission controllers (OPA Gatekeeper) to enforce required labels.

Example OPA constraint template:

```yaml
apiVersion: constraints.gatekeeper.sh/v1beta1
kind: K8sRequiredLabels
metadata:
  name: require-cost-labels
spec:
  parameters:
    labels: ["team", "service", "env"]
```

---

## **44.1.3 Labeling Node Pools (Mandatory)**

Node pool labels propagate to GCE instances:

```bash
gcloud container node-pools create web-pool \
  --cluster=prod-gke \
  --machine-type=e2-standard-4 \
  --labels=team=platform,env=prod,role=web
```

---

## **44.1.4 Label Inheritance Pitfalls**

- Kubernetes labels do **not** automatically appear on GCE billing export.
    
- Node pool labels propagate → pod labels do not.
    
- Missing labels = “unattributed cost,” the worst-case scenario for chargeback.
    

---

# **44.2 BigQuery Export**

To perform chargeback, you need raw, unfiltered billing data.  
GCP Billing → BigQuery Export is the authoritative pipeline.

---

## **44.2.1 Enabling BigQuery Billing Export**

1. Create BigQuery dataset:
    

```bash
bq --location=US mk -d billing_export
```

2. Enable export in GCP Billing UI  
    (set to dataset `billing_export`)
    

You will get a table:

```
billing_export.gcp_billing_export_v1_<BILLING_ID>
```

---

## **44.2.2 Querying Costs by Label**

### Example: Cost per team (last 30 days)

```sql
SELECT
  labels.team AS team,
  SUM(cost) AS total_cost
FROM
  `billing_export.gcp_billing_export_v1_*`
WHERE
  usage_start_time >= TIMESTAMP_SUB(CURRENT_TIMESTAMP(), INTERVAL 30 DAY)
GROUP BY
  team
ORDER BY
  total_cost DESC;
```

---

### Example: Cost per microservice

```sql
SELECT
  labels.service as service,
  SUM(cost) as total_cost
FROM
  `billing_export.gcp_billing_export_v1_*`
WHERE
  labels.service IS NOT NULL
GROUP BY service
ORDER BY total_cost DESC;
```

---

### Example: Cost per GKE cluster

```sql
SELECT
  resource.global_name AS resource_name,
  SUM(cost) AS total_cost
FROM
  `billing_export.gcp_billing_export_v1_*`
WHERE
  SKU.description LIKE '%Kubernetes%'
GROUP BY resource_name;
```

---

## **44.2.3 Detecting Unlabeled Spend**

```sql
SELECT
  SUM(cost) AS unlabeled_cost
FROM
  `billing_export.gcp_billing_export_v1_*`
WHERE
  (labels.team IS NULL OR labels.service IS NULL);
```

**Goal:** Eliminate unlabeled cost entirely.

---

## **44.2.4 Normalizing Mixed Billing Sources**

Some resources (e.g., Cloud SQL) require mapping via resource name patterns, since they lack labels.

Example:

```sql
CASE
  WHEN sku.description LIKE '%Cloud SQL%' AND resource.global_name LIKE '%checkout%' 
    THEN 'checkout'
  ELSE labels.service
END AS service
```

---

## **44.2.5 Common Export Pitfalls**

- exporting billing data to a multi-region dataset increases cost
    
- forgetting to partition BigQuery table → expensive queries
    
- not enabling daily export, resulting in large catch-up costs
    
- querying wildcard tables without filters → TBs scanned → Very Expensive
    
---

# **44.3 Dashboards**

Dashboards translate cost into insights.  
The two recommended platforms are:

- **Looker Studio (free)**
    
- **Grafana (BQ connector)**
    

---

## **44.3.1 Looker Studio Dashboard Structure**

Recommended dashboard sections:

### **1. High-Level Spend Overview**

- total cost
    
- monthly burn rate
    
- forecast vs budget
    
- cost by service category
    

### **2. Cost by Environment**

(dev, staging, prod)

### **3. Cost by Team**

Interactive table:

| Team | Monthly Cost | Trend | % Change |

### **4. Cost by GKE Cluster**

Breakdowns for:

- node pools
    
- control plane
    
- egress
    
- PD storage
    

### **5. Cost by Workload (Service)**

Using Kubernetes labels extracted from node pool labels.

---

## **44.3.2 Example SQL for Looker Visuals**

**Cost over time:**

```sql
SELECT
  DATE(usage_start_time) AS day,
  SUM(cost) AS daily_cost
FROM
  `billing_export.gcp_billing_export_v1_*`
GROUP BY day
ORDER BY day;
```

---

## **44.3.3 Grafana Integration (BQ plugin)**

Useful when your org prefers Grafana for unified metrics.

Setup steps:

1. Add BigQuery data source
    
2. Use parameterized SQL for dashboards
    
3. Combine infra cost with cluster metrics
    

Grafana example panel:

```sql
SELECT
  labels.team,
  SUM(cost)
FROM `billing_export.gcp_billing_export_v1_*`
WHERE $__timeFilter(usage_start_time)
GROUP BY labels.team
ORDER BY SUM(cost) DESC
```

---

## **44.3.4 Publishing Dashboards to Stakeholders**

- weekly Slack digest
    
- monthly engineering reviews
    
- quarterly budget refresh
    
- auto-generated chargeback invoices
    

---

## **44.3.5 Dashboard Pitfalls**

- dashboards without ownership → stale
    
- relying on UI filters instead of SQL reports
    
- no environment segmentation → bad insights
    
- slow dashboards due to unpartitioned tables
    
- multi-region BigQuery datasets doubling storage cost
    

---

# **44.4 Budget Alerts**

Budget alerts prevent runaway costs, especially in GKE/NAT/BigQuery.

---

## **44.4.1 Creating a Budget**

```bash
gcloud billing budgets create \
  --display-name="prod-budget" \
  --billing-account=XXXXXX-XXXXXX-XXXXXX \
  --budget-amount=20000 \
  --threshold-rules='threshold_percent=0.5' \
  --threshold-rules='threshold_percent=0.9' \
  --threshold-rules='threshold_percent=1.0'
```

---

## **44.4.2 Alerts to Pub/Sub**

Budgets can notify:

- Pub/Sub → triggers Cloud Functions
    
- Slack notifications via webhook
    
- PagerDuty alerts
    
- automated disabling of problematic workloads
    

Example Pub/Sub topic:

```bash
gcloud pubsub topics create billing-alerts
```

Attach to budget in console.

---

## **44.4.3 Slack Alerts (Cloud Function)**

Example Cloud Function (Python):

```python
import json
import requests

def notify_slack(event, context):
    msg = json.loads(base64.b64decode(event['data']).decode('utf-8'))
    text = f":warning: Billing alert: {msg['costAmount']} / {msg['budgetAmount']} used"
    requests.post("<WEBHOOK_URL>", json={"text": text})
```

---

## **44.4.4 Cost Per Team Alerts**

Using BigQuery scheduled query:

```sql
SELECT team, SUM(cost) AS cost
FROM `billing_export.gcp_billing_export_v1_*`
WHERE usage_start_time >= TIMESTAMP_SUB(CURRENT_TIMESTAMP(), INTERVAL 7 DAY)
GROUP BY team
HAVING cost > 5000;
```

Trigger alert → notify team channel.

---

## **44.4.5 Automated Cost Guardrails**

Examples:

- deny expensive SKUs in dev (GPUs, high-cost load balancers)
    
- enforce budget before creating new regional clusters
    
- auto-deploy “cost sentinel” CronJob that flags top offenders
    

---

## **44.4.6 Budget Pitfalls**

- budgets based on **invoice**, not actual usage → delayed alerts
    
- single global budget → hides category-specific issues
    
- ignoring NAT or cross-region egress until too late
    
- alerts going to unused email inboxes
    
- budgets not reviewed quarterly
    

---

# **Chapter 45 — Cost vs Reliability vs Performance**

_(Expanded with senior-level clarity, decision-making frameworks, quantification models, examples, and practical YAML/gcloud snippets. No redundancy. No cross-chapter references.)_

Cloud architecture is fundamentally a balance of **three competing forces**:

- **Cost** — How much the system costs to operate.
    
- **Reliability** — How available, durable, and fault-tolerant it is.
    
- **Performance** — How fast and responsive it is under expected load.
    

You can optimize two at a time, but rarely all three simultaneously.  
This chapter provides a leadership-grade framework for making those tradeoffs deliberately and transparently.

---

# **45.1 Tradeoffs & Decision Making**

Understanding tradeoffs means accepting that **every improvement has a cost**, whether technical or financial.  
Senior engineers must be able to quantify and justify changes.

---

## **45.1.1 The Iron Triangle for Cloud Systems**

|Decision|Cost|Reliability|Performance|
|---|---|---|---|
|Multi-region|↑↑|↑↑↑|= / ↑|
|Commodity VMs (E2)|↓|=|↓|
|Auto-scaling|↑ (small)|↑|↑↑|
|SSD → HDD|↓|=|↓↓|
|Spot Nodes|↓↓↓|↓|=|
|Global LB|↑↑|↑|↑↑↑|

A high-SLA SaaS platform usually chooses:

- **High Reliability**
    
- **High Performance**
    
- **Acceptable Cost**
    

Rather than lowest cost.

---

## **45.1.2 Structured Reliability Tradeoff Examples**

### **Example: Adding a second region**

**Benefit:**

- Higher availability (region-level redundancy)
    
- Disaster recovery coverage
    

**Cost impact:**

- 1.8×–2.5× infra cost from duplication
    
- Cross-region egress
    
- More complex deployment and failover logic
    

### **How to decide:**

Use a **simple failure analysis**:

```
If region = down → can customers still use critical workflows?
If "yes, but slow" → consider active/passive.
If "no" → active/active required.
```

---

## **45.1.3 Performance Tradeoff Examples**

### **Choosing faster instance families**

Moving from E2 → N2 increases:

- CPU cost (~15–20%)
    
- Performance (~25–45%)
    

**Net value:**  
If request throughput improves > CPU cost delta, it’s a win.

### **Choosing SSD vs HDD PDs**

Switching to HDD can reduce cost 60–70% but increases:

- latency
    
- variability
    
- IOPS constraints
    

**Rule:**

> Use SSD for primary paths, HDD for logs, archives, cold data.

---

## **45.1.4 Cost Tradeoff Examples**

### **Spot Nodes**

Cost ↓↓↓  
Reliability ↓  
Performance =

Use only for resilient workloads.

Example tainting spot nodes for safe workloads:

```bash
kubectl taint nodes -l cloud.google.com/gke-preemptible=true spot=true:NoSchedule
```

---

## **45.1.5 Service-Level Tradeoffs**

Each service should define its own optimized stance:

|Service Type|Priority|Typical Tradeoff|
|---|---|---|
|API gateway|Perf + Reliability|Higher cost acceptable|
|Internal processors|Cost|Slower or spot OK|
|Data analytics|Cost|Delayed acceptable|
|Auth/identity|Reliability|Never use spot|
|Edge routing|Performance|Multi-region required|

---

## **45.1.6 Decision Matrix for Senior Engineers**

When proposing changes:  
Answer these questions:

1. **What is the user impact?** (latency, availability, correctness)
    
2. **What is the cost delta?** (monthly & yearly RLC)
    
3. **What is the failure blast radius?**
    
4. **Does this improve or degrade operational simplicity?**
    
5. **What is the rollback path?**
    
6. **What is the end-state architecture vision?**
    

Providing this structure avoids emotion-driven decisions.

---

## **45.1.7 Example Decision Proposal**

> “Move API workloads from N2 to C3 nodes.”

**Reliability:** no change  
**Performance:** request latency ↓ 18%  
**Cost:** ↑ 12.5%  
**Why:** high QPS customer-facing workflow  
**Recommendation:** proceed  
**Rollback:** revert node pool via label + cordon → drain

---

## **45.1.8 Common Decision Pitfalls**

- optimizing for cost at the expense of reliability
    
- chasing performance without benchmarking
    
- using multi-region “just because it sounds good”
    
- ignoring cross-region egress in architecture
    
- overcomplicating designs to hit theoretical SLAs
    
- lack of an objective scoring framework
    

---

# **45.2 Optimization Frameworks**

Optimization is **systematic**, not reactive.  
This section provides repeatable frameworks used by senior engineers and SREs.

---

# **45.2.1 The C/R/P Framework**

A simple and effective framework for structuring decisions:

```
C = Cost
R = Reliability
P = Performance
```

Each proposed change is scored 1–5:

|Score|Meaning|
|---|---|
|1|Severe negative impact|
|3|Neutral|
|5|Major improvement|

### Example Scoring Table

|Option|Cost|Reliability|Performance|Weighted Score|
|---|---|---|---|---|
|Multi-region active/active|2|5|4|4.2|
|Multi-region cold standby|4|4|3|3.7|
|Single region HA|5|3|4|4.1|

Weighting can shift based on org goals.

---

# **45.2.2 RLC (Run-Rate Life Cycle) Modeling**

Calculate the **real** cost of a decision over time:

```
RLC = (Monthly cost) × (Expected lifespan in months)
```

Example:

- Adding a second region → +$40k/month
    
- Expected for 3 years → 36 months
    

RLC impact = $1.44M

This allows rational discussion with finance.

---

# **45.2.3 Reliability Budgeting**

For a given SLA, you derive allowed downtime:

|SLA|Annual Downtime|
|---|---|
|99.0%|~3.65 days|
|99.9%|~8.7 hours|
|99.99%|~52 min|
|99.999%|~5 min|

**Framework:**

- If SLA < 99.9% → single region is acceptable.
    
- If SLA ≥ 99.99% → multi-region required.
    

**Important:**

> “Five nines” multiplies infra cost by ~2–3×.

---

# **45.2.4 Performance Budgeting**

Define performance SLOs:

- **P95 response time** < X ms
    
- **Cold start time** < Y ms
    
- **Throughput** > Z requests/sec
    

Then test each optimization option against that budget.

### Example: Testing Node Type Performance

```bash
kubectl exec -it loadgen -- hey -n 20000 -c 200 http://api/checkout
```

Compare p95 latency across node families.

---

# **45.2.5 Cost Efficiency Formula**

A practical efficiency metric:

```
Cost Efficiency = (Requests Per Second) / (Cost Per Hour)
```

Example:

- E2-standard-4 → 600 rps @ $0.20/hr → 3000 rps per dollar
    
- N2-standard-4 → 900 rps @ $0.28/hr → 3214 rps per dollar
    
- C3-standard-4 → 1300 rps @ $0.35/hr → 3714 rps per dollar
    

Even though the C3 node is more expensive, its **efficiency is higher.**

---

# **45.2.6 The Tiered Workload Model**

Assign each workload a tier:

|Tier|Goal|Allowed Resources|
|---|---|---|
|Tier 0|mission-critical|multi-region, on-demand|
|Tier 1|customer-facing|on-demand + limited spot|
|Tier 2|internal|spot-preferred|
|Tier 3|batch/compute|spot-only|

**Framework outcome:**  
Teams get explicit cost vs reliability expectations.

---

# **45.2.7 Optimization Decision Pipeline**

### **1. Measure**

- CPU, memory usage
    
- latency
    
- saturation
    
- cold path behavior
    
- cost by service/team
    

### **2. Model**

- predict cost impact
    
- forecast performance impact
    
- simulate reliability/HA outcomes
    

### **3. Decide**

- use C/R/P scoring
    
- present alternatives
    

### **4. Implement**

- node pool changes
    
- scaling policy alterations
    
- multi-region deployment adjustments
    

### **5. Validate**

- run load tests
    
- compare metrics before/after
    
- validate spend changes in BigQuery
    

### **6. Iterate**

This ensures long-term optimization, not one-off fixes.

---

# **45.2.8 Common Optimization Pitfalls**

- designing for peak instead of average load
    
- overfitting architecture to rare failure modes
    
- ignoring total cost of ownership (TCO) over multiple years
    
- chasing micro-optimizations instead of structural fixes
    
- optimizing compute while ignoring networking/storage costs
    
- failure to monitor after making changes
    
- no rollback path for optimization experiments
    

---

# **Chapter 46 — Runbooks**

_(Expanded with fully structured, senior-level runbooks for handling: latency spikes, error spikes, and regional failures. Includes kubectl/gcloud commands, diagnostic workflows, YAML examples, and real-world pitfalls. No redundancy. No references to other chapters.)_

Runbooks define **repeatable operational procedures** for responding to incidents.  
They provide an objective, deterministic series of steps that reduce panic, shorten MTTR, and avoid mistakes during pressure.

This chapter includes three high-value runbooks:

- **Latency Spikes**
    
- **Error Spikes**
    
- **Regional Failures**
    

Each follows a consistent structure:

1. **Symptoms**
    
2. **Immediate Actions**
    
3. **Root Cause Isolation**
    
4. **Detailed Diagnostic Commands**
    
5. **Remediation Paths**
    
6. **Postmortem Notes**
    
7. **Common Pitfalls**
    

---

# **46.1 Latency Spikes**

Latency spikes often indicate:

- resource saturation
    
- degraded dependencies
    
- network congestion
    
- mesh misconfiguration
    
- autoscaling delays
    

This runbook provides a structured approach to isolate and remediate.

---

## **46.1.1 Symptoms**

- p95/p99 latency increases
    
- downstream dependencies timing out
    
- increased queue length in workers
    
- increased CPU throttling
    
- HPA not scaling fast enough
    
- mesh retries causing traffic amplification
    

---

## **46.1.2 Immediate Actions**

1. **Acknowledge the alert.**
    
2. **Freeze predictive auto-deploy systems** (CI, GitOps continuous sync).
    
3. **Check cluster saturation** (CPU, memory, network).
    
4. **Check rollout activity** (in-progress deployments often cause latency).
    
5. **Assess customer impact** → escalate if high.
    

---

## **46.1.3 Diagnostic Workflow**

### **Step 1 — Check Pod & Node Resource Pressure**

```bash
kubectl top nodes
kubectl top pods -A
```

Watch for:

- CPU > 90%
    
- memory > 90%
    
- high number of evictions
    

---

### **Step 2 — Verify Autoscaling Behavior**

```bash
kubectl get hpa -A
kubectl describe hpa <service>
```

Check:

- is scaling triggered?
    
- is max replicas reached?
    

If maxed:

> increase limits temporarily.

---

### **Step 3 — Check Rolling Deployments**

```bash
kubectl get deploy -A | grep -i progressing
kubectl rollout status deploy/<service> -n <ns>
```

A slow rollout or failing pods can stall traffic.

---

### **Step 4 — Inspect Sidecar (Istio) Latency**

```bash
kubectl exec -it <pod> -c istio-proxy -- pilot-agent request GET stats
```

Look for:

```
cluster.outbound.*.upstream_rq_time
```

High values = downstream issue.

---

### **Step 5 — Check Error Rate in Logs**

```bash
kubectl logs <pod> --since=5m
```

Look for:

- retries
    
- timeouts
    
- connection resets
    

---

### **Step 6 — Verify Upstream Dependencies**

Use curl from inside the pod:

```bash
kubectl exec -it <pod> -- curl -w "%{time_total}\n" http://upstream:8080/health
```

---

### **Step 7 — Check Node Throttling**

CPU throttling surfaces as latency:

```bash
kubectl describe pod <pod> | grep -i thrott
```

---

## **46.1.4 Remediation**

### **Fix 1 — Scale service**

```bash
kubectl scale deploy checkout-api --replicas=20
```

### **Fix 2 — Raise HPA limits**

```yaml
maxReplicas: 50
```

Apply with GitOps or manually during an incident.

---

### **Fix 3 — Reduce mesh retries (traffic amplification)**

Example VirtualService fix:

```yaml
retries:
  attempts: 1   # previously too high
  perTryTimeout: 200ms
```

---

### **Fix 4 — Add or Upgrade Node Pool**

```bash
gcloud container clusters resize prod-gke --node-pool=web --num-nodes=20
```

---

### **Fix 5 — Disable problematic canary**

```bash
kubectl rollout undo deploy/<service>
```

---

## **46.1.5 Postmortem Notes**

- identify which dependency caused lag
    
- quantify cost of spike
    
- add missing SLO alerting
    
- propose circuit-breakers if needed
    

---

## **46.1.6 Common Pitfalls**

- ignoring throttling
    
- assuming latency = network issue
    
- scaling too early → high cost, low ROI
    
- misconfigured HPAs causing oscillation
    
- over-aggressive retries → DDoS your own service
    

---

# **46.2 Error Spikes**

Error spikes reflect degradation in correctness or availability.  
They often show up as 4xx/5xx increases, timeout errors, or failed health checks.

---

## **46.2.1 Symptoms**

- error rate > SLO thresholds
    
- 5xx bursts
    
- failing liveness/readiness probes
    
- sudden drop in QPS
    
- customer complaints
    

---

## **46.2.2 Immediate Actions**

1. **Acknowledge the alert**.
    
2. **Check if a recent deployment occurred.**
    
3. **Check if the error spike affects one service or many.**
    
4. **Evaluate whether you must trigger global failover procedures.**
    

---

## **46.2.3 Diagnostic Workflow**

### **Step 1 — Check Recent Deployments**

```bash
kubectl get deploy -A --sort-by=.status.conditions[*].lastUpdateTime
```

Were new pods rolled out?

---

### **Step 2 — Check Pod Events**

```bash
kubectl describe pod <pod>
```

Look for:

- OOMKilled
    
- CrashLoopBackOff
    
- FailedScheduling
    

---

### **Step 3 — Check Ingress/Gateway Logs**

```bash
kubectl logs -n istio-system <gateway-pod> --since=5m
```

Look for:

- upstream connect errors
    
- TLS handshake failures
    
- authorization denied
    

---

### **Step 4 — Validate Health Checks**

```bash
kubectl get endpoints <svc>
```

If no endpoints:

- readiness probes failing
    
- label selector mismatch
    
- wrong port
    

---

### **Step 5 — Test Service Internally**

```bash
kubectl exec test-pod -- curl http://service:8080/health
```

### **Step 6 — Check Database/Queue Dependencies**

```bash
gcloud sql instances describe checkout-db
```

Check:

- connections
    
- CPU
    
- storage full
    

---

### **Step 7 — Inspect Mesh Policies**

Misconfigured Istio policies = frequent cause of outages.

Check AuthorizationPolicy:

```bash
kubectl get authorizationpolicy -A
```

Check PeerAuthentication:

```bash
kubectl get peerauthentication -A
```

---

## **46.2.4 Remediation**

### **Fix 1 — Roll Back Deployment**

```bash
kubectl rollout undo deploy/<service>
```

### **Fix 2 — Adjust Resources**

```bash
kubectl set resources deploy/<service> --requests=cpu=500m
```

### **Fix 3 — Patch Failing ConfigMaps**

```bash
kubectl apply -f config/fix.yaml
```

### **Fix 4 — Disable faulty mesh policy**

```bash
kubectl delete authorizationpolicy bad-policy
```

### **Fix 5 — Restart Gateway (rare)**

```bash
kubectl rollout restart deploy istio-ingressgateway -n istio-system
```

---

## **46.2.5 Postmortem Notes**

- document which dependency caused the spike
    
- propose automated testing for the discovered issue
    
- tighten schema validation (config, policies)
    

---

## **46.2.6 Common Pitfalls**

- assuming it’s the service itself (often it’s a dependency)
    
- not checking Ingress/Gateway logs first
    
- ignoring failing readiness probes
    
- unclear ownership of upstream dependencies
    
- manually patching instead of using GitOps
    

---

# **46.3 Regional Failures**

Regional failures are **rare but high-impact** events.  
This runbook focuses on _response_, _containment_, and _failover_.

---

## **46.3.1 Symptoms**

- entire GKE region unreachable
    
- control plane unavailable
    
- nodes not scheduling
    
- multi-service downtime
    
- > 50% error rate across multiple services
    
- GCP incident reports referencing region issue
    

---

## **46.3.2 Immediate Actions**

1. **Declare regional incident.**
    
2. **Stop deployments globally.**
    
3. **Verify if issue is internal or GCP-wide.**
    
4. **Activate communication channel for incident.**
    
5. **Prepare to fail over traffic.**
    

---

## **46.3.3 Diagnostic Workflow**

### **Step 1 — Validate Cluster Reachability**

```bash
kubectl get nodes
```

### **Step 2 — Check Control Plane Connectivity**

```bash
kubectl get componentstatuses
```

### **Step 3 — Test Node VM Reachability**

```bash
gcloud compute ssh <node> --zone=us-central1-a
```

If unreachable → regional network fault likely.

---

### **Step 4 — Check GCP Status**

```bash
gcloud status
# or manually open Google Cloud Status Dashboard
```

---

### **Step 5 — Check Load Balancer Backends**

```bash
gcloud compute backend-services get-health web-backend \
  --global
```

Unhealthy in one region triggers failover.

---

## **46.3.4 Failover Procedure**

### **Option A — Global LB Failover (Active/Passive)**

```bash
gcloud compute backend-services update web-backend \
  --global \
  --failover \
  --failover-policy=ratio=1
```

### **Option B — Route 100% Traffic to Secondary Region**

Istio VirtualService example:

```yaml
http:
- route:
  - destination:
      host: checkout
      subset: us-east1
    weight: 100
```

Apply emergency override with GitOps or manual apply (temporary).

---

### **Option C — Drain Unhealthy Region**

```bash
gcloud compute backend-services update web-backend \
  --balancing-mode=RATE \
  --max-rate-per-endpoint=0
```

---

### **Option D — Promote Read Replica (DB)**

Cloud SQL:

```bash
gcloud sql instances promote-replica replica-us-east1
```

---

## **46.3.5 Recovery Procedure**

1. Wait for region to stabilize.
    
2. Restore traffic split gradually (e.g., 90/10, 80/20).
    
3. Validate:
    
    - health checks
        
    - latency
        
    - error rates
        
    - replication lag
        
4. Re-enable autoscaling in both regions.
    
5. Resume deployments.
    

---

## **46.3.6 Postmortem Notes**

- quantify cost impact (failover + cross-region egress)
    
- identify services missing HA patterns
    
- improve failure drills (game days)
    
- update SLOs for multi-region design evaluation
    

---

## **46.3.7 Common Pitfalls**

- shifting traffic too quickly → overload survivor region
    
- unhealthy replicas promoted → data divergence
    
- missing per-region mesh configs
    
- failing to stop deployments → cascading failures
    
- untested failover runbooks → chaos during real events
    
- forgetting to rollback temporary configuration edits
    

---

# **Chapter 47 — Debugging GKE Networking**

_(Expanded with senior-level depth, practical commands, fully commented YAML, CNI internals, iptables inspection, Envoy debugging, and DNS diagnostic methodology. No redundancy. No cross-references.)_

GKE networking issues are among the most difficult to debug because they span multiple layers:  
**CNI → iptables → kube-proxy → Envoy → DNS → application.**  
This chapter presents a highly structured and deterministic debugging methodology that reduces MTTR in real-world incidents.

---

# **47.1 CNI Debugging (GKE Dataplane + Cilium)**

GKE can use:

- **GKE Dataplane V2 (eBPF-based, default for Autopilot)**
    
- **Cilium (eBPF-based add-on or custom)**
    
- **kube-proxy-based iptables routing (legacy)**
    

This section provides debugging steps for both **eBPF** and **iptables-driven CNI paths**.

---

## **47.1.1 Symptoms of CNI Problems**

- pods stuck in `ContainerCreating`
    
- no pod IP assigned
    
- GKE node reporting: `Failed to setup network for sandbox`
    
- inter-pod connectivity failing
    
- NodePort traffic not reaching pods
    
- networkpolicy blocking unexpectedly
    

---

## **47.1.2 Step 1 — Check Pod Sandbox Events**

```bash
kubectl describe pod <pod> | grep -i "network"
```

Look for:

- CNI plugin failures
    
- IP allocation failures
    
- network policy drops
    

---

## **47.1.3 Step 2 — Inspect Node-Level CNI Logs**

On GKE node:

```bash
gcloud compute ssh <node-name> --zone <zone>
sudo journalctl -u kubelet -f
sudo journalctl -u containerd -f
```

CNI failures show up as:

```
CNI failed to assign address
failed to setup iptables rules
failed to attach BPF program
```

---

## **47.1.4 Step 3 — Check IP Allocation Pools**

GKE Dataplane V2:

```bash
kubectl get pods -n kube-system -l k8s-app=netd
kubectl logs -n kube-system -l k8s-app=netd
```

Cilium:

```bash
kubectl exec -n kube-system ds/cilium -- cilium status
```

Example output:

```
Allocated IPs: 250/4096
IPv4 fragmentation: disabled
Policies: OK
```

If IPs are exhausted → **scale node pool** or **expand CIDRs**.

---

## **47.1.5 Step 4 — Validate Inter-Pod Routing**

Test pod → pod communication:

```bash
kubectl exec -it pod-a -- curl -m 2 http://pod-b:8080
```

If same-node works but cross-node fails → routing issue.

---

## **47.1.6 Step 5 — Check Network Policies**

List:

```bash
kubectl get networkpolicy -A
```

Simulate allowed paths:

```bash
kubectl exec -it pod-a -- nc -zvw2 pod-b 8080
```

If traffic blocked unexpectedly → misconfigured `from:` selectors.

---

## **47.1.7 Common CNI Pitfalls**

- exhausting pod CIDR ranges
    
- conflicting NetworkPolicies
    
- older node images missing eBPF support
    
- nodes without required kernel sysctls
    
- using hostNetwork unintentionally bypassing CNI
    
- forgetting that in GKE Dataplane V2, **iptables rules are bypassed**
    

---

# **47.2 iptables Basics (for classic GKE clusters)**

Even in eBPF-based clusters, iptables often remains partially active.  
Understanding iptables is essential for debugging NodePorts, masquerading, and hairpin traffic.

---

## **47.2.1 The Three Key Tables**

|Table|Purpose|
|---|---|
|**nat**|SNAT/DNAT, load-balancing|
|**filter**|allow/deny decisions|
|**mangle**|altering TOS, TTL, marks|

---

## **47.2.2 Step 1 — Inspect nat Table**

On node:

```bash
sudo iptables -t nat -L -n -v
```

Look for:

- `KUBE-SERVICES`
    
- `KUBE-NODEPORTS`
    
- `KUBE-MARK-MASQ`
    

If missing → kube-proxy malfunction.

---

## **47.2.3 Step 2 — Inspect filter Table**

```bash
sudo iptables -t filter -L -n -v
```

Check for:

- dropped packets
    
- excessive policy matches
    

---

## **47.2.4 Step 3 — Trace Packet Path**

Example: NodePort service 31000

```bash
sudo iptables -t nat -S | grep 31000
```

You should see DNAT rules mapping to pod endpoints.

---

## **47.2.5 Step 4 — Check kube-proxy**

```bash
kubectl logs -n kube-system ds/kube-proxy
```

Look for:

```
Failed to sync iptables
Invalid service definition
```

---

## **47.2.6 Example: Broken NodePort**

### Symptom:

NodePort reachable on one node but not others.

### Fix:

Restart kube-proxy:

```bash
kubectl rollout restart ds/kube-proxy -n kube-system
```

Or correct missing DNAT rules.

---

## **47.2.7 Common iptables Pitfalls**

- hairpin traffic blocked
    
- NAT not being applied (missing MASQUERADE)
    
- kube-proxy running in IPVS mode but iptables rules expected
    
- rules overwritten by host security agents
    
- VPC firewall blocking node → node traffic
    

---

# **47.3 Envoy Debugging (Istio sidecars)**

Envoy sits on the datapath for east-west and ingress traffic.  
Most “mysterious” networking issues inside service meshes originate here.

---

## **47.3.1 Step 1 — Check Proxy Status**

```bash
istioctl proxy-status
```

Look for:

- SYNCED vs STALE
    
- cluster config mismatches
    
- disconnected envoy instances
    

---

## **47.3.2 Step 2 — Check Envoy Config Dump**

```bash
istioctl proxy-config cluster <pod>
```

Validate upstream endpoints:

Example output:

```
service: checkout.default.svc.cluster.local
load_assignment:
  endpoints: 3
```

If `endpoints: 0` → service discovery problem.

---

### Full config dump:

```bash
istioctl proxy-config all <pod>
```

---

## **47.3.3 Step 3 — View Envoy Stats**

```bash
kubectl exec <pod> -c istio-proxy -- curl localhost:15000/stats
```

Key metrics:

- `upstream_cx_connect_fail` → connection failures
    
- `upstream_rq_pending_overflow` → rate limiting
    
- `upstream_rq_timeout` → dependency timeouts
    

---

## **47.3.4 Step 4 — Check Envoy Logs**

```bash
kubectl logs <pod> -c istio-proxy --since=5m
```

Common logs:

```
TLS error: 268435581: SSL routines:SSL3_GET_RECORD:wrong version number
No healthy upstream
403 RBAC: access denied
```

---

## **47.3.5 Step 5 — Validate mTLS State**

```bash
istioctl authn tls-check <pod> <service>
```

Shows:

- mTLS enabled/disabled
    
- misalignment between PeerAuthentication and DestinationRule
    

---

## **47.3.6 Example: Policy Breaks Traffic**

Bad AuthorizationPolicy:

```yaml
spec:
  rules: []
  selector:
    matchLabels:
      app: checkout
```

Fix: remove or correct policy.

---

## **47.3.7 Common Envoy Pitfalls**

- sidecars not injected due to label error
    
- mismatched DestinationRule causing mTLS handshake failures
    
- services returning mixed TLS/non-TLS traffic
    
- excessive retries causing cascading failures
    
- sidecar CPU limit too low → throttling
    

---

# **47.4 DNS Debugging**

DNS issues in Kubernetes are extremely common and often misdiagnosed as network outages.

This section provides a complete procedure for diagnosing them.

---

## **47.4.1 Symptoms**

- pods cannot resolve service names
    
- intermittent DNS failures
    
- long lookup times
    
- CoreDNS pods at high CPU
    
- NXDOMAIN for valid services
    

---

## **47.4.2 Step 1 — Check CoreDNS Health**

```bash
kubectl get pods -n kube-system -l k8s-app=kube-dns
kubectl logs -n kube-system -l k8s-app=kube-dns | tail
```

Look for:

```
SERVFAIL
timeout
plugin/forward: no upstream host
```

---

## **47.4.3 Step 2 — Exec Pod DNS Query Test**

```bash
kubectl exec -it <pod> -- nslookup checkout.default.svc.cluster.local
```

Or:

```bash
kubectl exec -it <pod> -- dig checkout.default.svc.cluster.local
```

Check sections:

- **ANSWER** must contain correct A/AAAA records
    
- **QUERY TIME** should be < 20ms
    

---

## **47.4.4 Step 3 — Validate Service & Endpoints**

If DNS resolves but service doesn’t work:

```bash
kubectl get svc checkout
kubectl get endpoints checkout
```

0 endpoints = readiness probe failing.

---

## **47.4.5 Step 4 — Check Node-Level DNS (GKE NodeLocal DNSCache)**

If using NodeLocal DNSCache:

```bash
kubectl get daemonset node-local-dns -n kube-system
kubectl logs -n kube-system ds/node-local-dns
```

Look for:

```
cache miss storm
no upstream servers
```

---

## **47.4.6 Step 5 — Validate Upstream DNS (VPC)**

DNS in GKE depends on VPC-level DNS settings:

```bash
gcloud compute networks describe <vpc> \
  --format="value(dnsPolicy)"
```

Ensure:

- private DNS enabled
    
- no conflicting DNS peering
    

---

## **47.4.7 Step 6 — Debug Split-Horizon Behavior**

If you have hybrid/on-prem:

```bash
dig @<onprem-dns> service.company.com
dig @169.254.169.254 metadata.google.internal
```

Check consistency between views.

---

## **47.4.8 Example: Fixing High CoreDNS CPU**

Patch deployment:

```bash
kubectl -n kube-system set resources deploy coredns \
  --requests=cpu=200m --limits=cpu=500m
```

Or scale:

```bash
kubectl -n kube-system scale deploy coredns --replicas=4
```

---

## **47.4.9 Common DNS Pitfalls**

- CoreDNS starved of CPU
    
- NodeLocal DNSCache losing upstream targets
    
- service name collisions across namespaces
    
- wrong service type causing incorrect DNS record
    
- wildcard DNS from external systems overwriting internal DNS
    
- cluster domains mismatched between components
    

---

# **Chapter 48 — TLS/mTLS Issues**

_(Expanded with senior-level depth, practical debugging workflows, OpenSSL/Envoy commands, Istio YAML, certificate-chain diagrams, rotation failure symptoms, and common pitfalls. No redundancy. No cross-chapter references.)_

TLS/mTLS failures are some of the most complex production issues on GKE, especially with service meshes, load balancers, and hybrid systems.  
This chapter provides a deterministic approach for diagnosing and fixing:

- certificate-chain issues
    
- SNI/SAN errors
    
- trust-anchor failures
    
- rotation outages
    

Each section is designed for incident response and long-term maintainability.

---

# **48.1 Certificate Chains**

TLS requires a **complete and correct** certificate chain (leaf → intermediate → root).  
Most failures result from:

- missing intermediate certs
    
- incorrect key usage
    
- expired or mismatched chains
    
- cluster-wide mTLS with incompatible trust anchors
    
- Envoy rejecting incomplete validation contexts
    

---

## **48.1.1 Symptoms of Certificate Chain Problems**

- browser reports: _"unable to verify the first certificate"_
    
- Envoy logs: `VERIFY_ERROR: unable to get local issuer certificate`
    
- gRPC errors: `tls: failed to verify certificate: x509: certificate signed by unknown authority`
    
- pods unable to call upstream in Istio: `503: upstream connect error`
    
- LB health checks failing on HTTPS services
    

---

## **48.1.2 Step 1 — Inspect Certificate Chain with OpenSSL**

From inside a pod:

```bash
kubectl exec -it <pod> -- openssl s_client \
  -connect checkout:443 -showcerts
```

Look for:

1. **Leaf certificate**
    
2. **Intermediate(s)**
    
3. **Root certificate**
    

If only leaf is shown → chain is incomplete.

---

## **48.1.3 Step 2 — Validate Key Usages**

```bash
openssl x509 -in server.crt -text -noout | grep -A3 "Key Usage"
```

For server certificates, expect:

```
Digital Signature
Key Encipherment
TLS Web Server Authentication
```

Missing key usages → immediate TLS rejection.

---

## **48.1.4 Step 3 — Check Certificate Expiry**

```bash
openssl x509 -enddate -noout -in server.crt
```

Or directly from service:

```bash
echo | openssl s_client -connect checkout:443 2>/dev/null | openssl x509 -noout -dates
```

---

## **48.1.5 Fix — Provide Complete Chain to Ingress Gateway**

Correct Istio Gateway example:

```yaml
tls:
  mode: SIMPLE
  credentialName: checkout-cert
```

Secret must contain:

```bash
tls.crt = leaf + intermediate
tls.key = private key
```

**Do NOT** include root CA in the chain.

---

## **48.1.6 Common Certificate-Chain Pitfalls**

- intermediates missing from secret
    
- incorrect order (root should not appear)
    
- multiple intermediates out of order
    
- cert-manager misconfiguration producing single-level chains
    
- uploading fullchain.pem into both cert and key fields
    
- intermediate CA expired long before root
    

---

# **48.2 SNI & SAN Issues**

Modern TLS requires:

- **SNI (Server Name Indication)** so the server knows which certificate to present.
    
- **SAN (Subject Alternative Name)** matching the requested hostname.
    

Most mTLS failures occur because SAN does not match Service FQDNs.

---

## **48.2.1 Symptoms**

- Envoy showing `no SNI provided`
    
- `x509: certificate is not valid for any names`
    
- requests to `service.ns.svc.cluster.local` fail but `localhost` works
    
- gRPC failing immediately with `UNAVAILABLE`
    
- Ingress returning 421 or 421-style routing mismatch
    

---

## **48.2.2 Step 1 — Inspect SNI With OpenSSL**

```bash
openssl s_client -connect checkout:443 -servername checkout.example.com
```

Verify:

- did the correct certificate load?
    
- check the SAN extension
    

---

## **48.2.3 Step 2 — Verify SAN List**

```bash
openssl x509 -in server.crt -text -noout | grep -A2 "Subject Alternative Name"
```

Should include:

- `DNS:checkout.example.com`
    
- `DNS:checkout.default.svc.cluster.local`
    
- `DNS:checkout` (for mesh)
    

---

## **48.2.4 Step 3 — Validate Istio DestinationRule SNI Config**

Incorrect:

```yaml
tls:
  sni: wrong-host.com
```

Correct:

```yaml
tls:
  sni: checkout.default.svc.cluster.local
```

---

## **48.2.5 Step 4 — Capture Envoy SNI Routing Logs**

```bash
kubectl exec -it <pod> -c istio-proxy -- curl localhost:15000/config_dump | grep sni
```

---

## **48.2.6 Example — Fixing mTLS SAN Mismatch**

Broken certificate SAN:

```
DNS:checkout.internal
```

Replace with:

```yaml
spec:
  dnsNames:
    - checkout
    - checkout.default.svc.cluster.local
    - checkout.prod.svc.cluster.local
```

Reissue cert.

---

## **48.2.7 Common SNI/SAN Pitfalls**

- wildcard certs not matching internal mesh names
    
- cert-manager producing SANs for only external hostnames
    
- hostname mismatch between gateway and service
    
- missing service namespace in SAN
    
- apps using IP address (TLS fails without SAN IP)
    

---

# **48.3 Trust Model Failures**

This section covers PKI and trust-anchor problems that break mTLS in meshes, gateways, or hybrid networks.

---

## **48.3.1 Symptoms**

- `certificate signed by unknown authority`
    
- `x509: cannot validate certificate for <IP> because no matching SAN found`
    
- Envoy logs show `verify_certificate failed`
    
- ingress returning 503 instead of 401/403
    
- cluster-wide breakage after CA rotation
    

---

## **48.3.2 Step 1 — Validate Root CA on Both Ends**

Download certificate presented by server:

```bash
echo | openssl s_client -connect app:443 \
  | sed -ne '/-BEGIN CERTIFICATE-/,/-END CERTIFICATE-/p' \
  > server.pem
```

Check trust against local CA:

```bash
openssl verify -CAfile ca.pem server.pem
```

If mismatch → trust domain mismatch.

---

## **48.3.3 Step 2 — Check Istio Root CA (mesh CA)**

```bash
kubectl get configmap istio-ca-root-cert -o yaml -n istio-system
```

Compare hashes:

```bash
sha256sum ca.pem
sha256sum extracted-ca.pem
```

If different → mTLS fails cluster-wide.

---

## **48.3.4 Step 3 — Validate Trust Domain**

Istio `MeshConfig` trust domain:

```bash
kubectl get configmap istio -o yaml -n istio-system | grep trustDomain
```

Must match identity used in SPIFFE URIs:

```
spiffe://cluster.local/ns/default/sa/service-account
```

---

## **48.3.5 Step 4 — Check PeerAuthentication Policies**

Incorrect mTLS enforced on plaintext services:

```yaml
mtls:
  mode: STRICT
```

Fix: use PERMISSIVE during migration.

---

## **48.3.6 Step 5 — Hybrid Trust Issues (on-prem + GCP)**

Common failures:

- on-prem CA not recognized by mesh
    
- GKE nodes missing enterprise root bundles
    
- proxies rejecting special enterprise CAs with long chains
    

Fix:

```bash
kubectl create configmap custom-ca \
  --from-file=enterprise-root.crt -n istio-system
```

Mount into proxy CA bundles.

---

## **48.3.7 Common Trust Model Pitfalls**

- mismatched CAs after cluster upgrades
    
- mesh expansion introducing multiple trust domains
    
- rotating CA without updating sidecars
    
- missing or invalid root certs in ConfigMaps
    
- enterprise TLS inspection boxes breaking chain integrity
    

---

# **48.4 Rotation Failures**

Certificate rotation is one of the most dangerous operations in a production cluster because failure means _total service outage_.

---

## **48.4.1 Symptoms**

- all traffic suddenly fails
    
- pods cannot authenticate to upstreams
    
- gateways return `503 upstream connect error`
    
- secrets with expired certs
    
- gRPC negotiating old TLS versions
    

---

## **48.4.2 Step 1 — Check Certificate Expiry Across Mesh**

```bash
istioctl x workload entry list --output json | jq '.[].cert.expiry'
```

Or check manually:

```bash
kubectl exec <pod> -c istio-proxy -- curl localhost:15000/certs
```

Look for:

```
"days_until_expiration": -1
```

Expired.

---

## **48.4.3 Step 2 — Validate cert-manager Logs**

```bash
kubectl logs -n cert-manager deploy/cert-manager
```

Common messages:

```
Failed to sign certificate
Issuer does not match
ACME challenge failed
```

---

## **48.4.4 Step 3 — Check K8s Secret Mount Propagation**

Pods do **not** automatically reload certificates unless:

- the app watches the mount
    
- Envoy hot reloads certs
    

Check:

```bash
kubectl get secret checkout-cert -o yaml
```

If updated but pods still broken → need to restart pods.

---

## **48.4.5 Step 4 — Rotate Root CA in Istio Safely**

Safe method:

1. **Enable dual-root mode.**
    
2. **Roll out new root CA.**
    
3. **Wait for all sidecars to receive new trust bundle.**
    
4. **Roll workloads gradually.**
    
5. **Remove old root.**
    

Example config for dual-root:

```yaml
meshConfig:
  rootCerts:
    - old-root.pem
    - new-root.pem
```

---

## **48.4.6 Example: Stale Pod After Secret Rotation**

Fix:

```bash
kubectl rollout restart deploy checkout
```

Best practice: use **`checksum/config`** pattern to trigger restarts:

```yaml
annotations:
  checksum/cert: "{{ sha256sum of certificate }}"
```

---

## **48.4.7 Common Rotation Pitfalls**

- rotating CA without sidecar restart
    
- cert-manager issuers not having permission to update secrets
    
- stale or orphaned CA bundles
    
- pods running with cached TLS state
    
- out-of-order rotation causing trust fragmentation
    
- Envoy hot-reload not enabled for specific certs
    
- renewing only leaf but not intermediate certs
    

---

# **Chapter 49 — Real Failures & Lessons**

_(Expanded with real-world failure modes, deep technical explanations, command examples, YAML snippets, and what-to-do-next guidance. No redundancy, no cross-references.)_

This chapter does **not** describe hypothetical events.  
These are **representative patterns of real incidents** that have occurred in modern cloud/Kubernetes/GKE environments.  
The goal: help senior engineers recognize early warning signs, avoid catastrophic outages, and build instincts around failure patterns that only appear at scale.

---

# **49.1 Packet Loss Incidents**

Packet loss in cloud networks is subtle: it rarely appears as 100% failure, but rather _slowdowns_, _timeout spikes_, or _node-level anomalies_.  
Packet loss often manifests only under load, during cross-zone traffic, or on specific paths (pod → pod, pod → node, or node → external service).

---

## **49.1.1 Symptoms**

- rising p99 latency with stable p50
    
- intermittent gRPC timeout errors
    
- Envoy: `upstream_reset_before_response_started`
    
- dropped NodePort traffic
    
- connections stuck in SYN-SENT
    
- HPA scaling unexpectedly due to slow responses
    
- only pods on _specific nodes_ failing
    

---

## **49.1.2 Common Root Causes**

1. **Node NIC saturation**
    
2. **Bad underlying hypervisor (cloud provider side)**
    
3. **Cilium/Dataplane V2 BPF map exhaustion**
    
4. **NetworkPolicy misconfiguration leading to silent drops**
    
5. **SNAT port exhaustion**
    
6. **GKE node update that disrupted BPF programs**
    
7. **Hairpin NAT under heavy load**
    

---

## **49.1.3 Diagnostics**

### **Check node-level NIC drops**

```bash
gcloud compute ssh <node> --zone=<zone>
netstat -i
```

Look for:

```
RX-ERR, RX-DRP, TX-DRP > 0
```

---

### **Check Cilium drop metrics**

```bash
kubectl exec -n kube-system ds/cilium -- cilium metrics list | grep drop
```

---

### **Check SNAT port exhaustion**

```bash
kubectl exec <pod> -c istio-proxy -- netstat -an | grep SYN_SENT
```

If thousands → SNAT exhaustion.

---

### **Check eBPF program status**

```bash
kubectl exec -n kube-system ds/cilium -- cilium status
```

You may see:

```
BPF map full
XDP program failed
```

---

## **49.1.4 Remediation**

### **Fix 1 — Drain & Remove Bad Nodes**

```bash
kubectl drain <node> --ignore-daemonsets --delete-emptydir-data
gcloud compute instances delete <node>
```

---

### **Fix 2 — Increase NAT Ports**

```bash
gcloud compute routers nats update nat-config \
  --router=core-router \
  --min-ports-per-vm=8192
```

---

### **Fix 3 — Restart CNI Pods**

```bash
kubectl rollout restart ds/cilium -n kube-system
```

---

### **Fix 4 — Add NodePool with Correct MTU**

Sometimes MTU mismatch causes hidden packet fragmentation.

---

## **49.1.5 Lesson Learned**

> Always monitor NIC drops, SNAT ports, and BPF map sizes.  
> If one node behaves differently than others → it's almost always the node’s fault, not the application.

---

# **49.2 Data Loss Near Misses**

These incidents rarely cause _full_ data loss.  
Instead, they create **silent corruption risks**, **lost writes**, or **out-of-order replication**—the dangerous kind that remains invisible until too late.

---

## **49.2.1 Symptoms**

- DB replicas falling behind
    
- “read-your-own-write” inconsistencies
    
- sudden increase in write latency
    
- Cloud SQL operations stuck in `PENDING`
    
- missing events from queues
    
- idempotent APIs “fixing” missed writes without visibility
    

---

## **49.2.2 Common Root Causes**

1. **Application writing to wrong region** (mis-routed traffic)
    
2. **Disk full on Cloud SQL** → silent throttling
    
3. **Primary DB restarted during CPU spike**
    
4. **Misconfigured readiness probe causing dual-write race**
    
5. **Async pub/sub consumers lagging** (eventual consistency issues)
    
6. **Kubernetes pod eviction mid-transaction**
    

---

## **49.2.3 Diagnostics**

### **Check DB replication status**

```bash
gcloud sql instances describe checkout-db | grep replication
```

Look for:

```
replicationLag: 2000s
```

---

### **Check Cloud SQL storage metrics**

```bash
gcloud sql instances describe checkout-db | grep storage
```

If storage usage > 90% → imminent risk.

---

### **Check for pod restarts during transactions**

```bash
kubectl get events -A | grep -i eviction
```

---

### **Check queue lag (Pub/Sub)**

```bash
gcloud pubsub subscriptions list --format="table(name,backlog)"
```

---

## **49.2.4 Remediation**

### **Fix 1 — Expand DB Storage Immediately**

```bash
gcloud sql instances patch checkout-db \
  --storage-size=6144
```

---

### **Fix 2 — Quarantine Region with Stale Reads**

Use Istio:

```yaml
route:
- destination:
    host: checkout-db
    subset: us-central1
  weight: 100
```

Remove failing region.

---

### **Fix 3 — Restart Consumers in Order**

```bash
kubectl rollout restart deploy/events-consumer
```

---

## **49.2.5 Lesson Learned**

> Most data loss risks are caused by slow-moving failures:  
> replication lag, disk-level throttling, and traffic being routed to “bad” regions.

---

# **49.3 Latency Cascades**

Latency cascades are system-wide slowdowns caused by **one** slow dependency triggering **many** retries—creating exponential load amplification.

---

## **49.3.1 Symptoms**

- traffic looks normal but p99 explodes
    
- CPU on upstream/sidecar spikes
    
- Envoy: `upstream_rq_pending_overflow`
    
- HPA maxed out
    
- clients retrying too aggressively
    
- DB CPU at 100%
    

---

## **49.3.2 Common Causes**

1. **Misconfigured retry policies**
    
2. **Single failing dependency in the request chain**
    
3. **Queue saturation**
    
4. **HPA reacting too slowly**
    
5. **GC pauses in JVM-based services**
    
6. **DNS lookup latency spike**
    
7. **Pod resource throttling**
    

---

## **49.3.3 Diagnostics**

### **Check Retry-Related Envoy Stats**

```bash
kubectl exec <pod> -c istio-proxy -- curl localhost:15000/stats | grep retry
```

---

### **Check Upstream Queue Saturation**

```bash
kubectl top pod -n <ns>
```

Look for pending requests.

---

### **Check CPU Throttling**

```bash
kubectl describe pod <pod> | grep -i thrott
```

---

### **Check DB Query Latency**

```bash
gcloud sql insights query-stats list --instance=checkout-db
```

---

### **Check Thread Pools in Apps**

Often:

```
threadpool full
```

---

## **49.3.4 Remediation**

### **Fix 1 — Reduce Retry Attempts Immediately**

```yaml
retries:
  attempts: 1
```

---

### **Fix 2 — Increase Pod CPU Limits Temporarily**

```bash
kubectl set resources deploy/api --limits=cpu=2
```

---

### **Fix 3 — Increase DB CPU tier**

```bash
gcloud sql instances patch checkout-db \
  --cpu=8 --memory=32GB
```

---

### **Fix 4 — Auto-failover to healthier region**

---

## **49.3.5 Lesson Learned**

> Retry storms are self-inflicted DDoS events.  
> The more resilient your system tries to be, the more dangerous retries can become.

---

# **49.4 Cross-Region Misroutes**

Cross-region misrouting is when requests intended for one region are accidentally routed to another, causing:

- high latency
    
- inconsistent state
    
- unexpected egress costs
    
- multi-region read/write conflicts
    

---

## **49.4.1 Symptoms**

- sudden p99 latency increase only for some users
    
- DB writes seen in wrong region
    
- Cloud Armor logs showing traffic from unexpected regions
    
- backend service logs show wrong region backend being hit
    
- global load balancer returning endpoints from unexpected region
    

---

## **49.4.2 Common Root Causes**

1. **NEG backends incorrectly attached to global load balancer**
    
2. **Istio VirtualService wrong weight split**
    
3. **Failover policy incorrectly flipped to full failover**
    
4. **DNS TTL too long with outdated IPs**
    
5. **SessionAffinity set incorrectly**
    
6. **Cross-region routing due to insufficient regional capacity**
    

---

## **49.4.3 Diagnostics**

### **Check NEG attachments**

```bash
gcloud compute backend-services describe web \
  --global \
  --format="value(backends.group)"
```

If backends from wrong region appear → misconfig.

---

### **Check Load Balancer Health**

```bash
gcloud compute backend-services get-health web --global
```

If primary region unhealthy → traffic shifts silently.

---

### **Check Istio traffic split**

```bash
kubectl get virtualservice web -o yaml
```

Look for:

```yaml
weight: 0
```

(indicates forced failover)

---

### **Check DNS mapping**

```bash
dig api.example.com +trace
```

or inside pod:

```bash
kubectl exec test -- dig api.example.com
```

---

### **Check Regional Health Checks**

If health checks fail, GCLB will move traffic _without warning_.

```bash
gcloud compute health-checks describe web-hc
```

---

## **49.4.4 Remediation**

### **Fix 1 — Remove Wrong NEGs**

```bash
gcloud compute backend-services update web \
  --remove-backend=<NEG_URL> \
  --global
```

---

### **Fix 2 — Correct Istio Split**

```yaml
http:
- route:
  - destination:
      host: web
      subset: us-central1
    weight: 100
```

---

### **Fix 3 — Reduce DNS TTL**

```yaml
ttl: 30
```

---

### **Fix 4 — Increase Regional Capacity**

Add more nodes:

```bash
gcloud container clusters resize prod-us-central1 \
  --node-pool=web \
  --num-nodes=50
```

---

## **49.4.5 Lesson Learned**

> Cross-region misrouting is rarely malicious—  
> it’s usually caused by a subtle capacity or health check issue that triggers an automatic failover.

---

# **Chapter 50 — Anti-Patterns**

_(Expanded with senior-level clarity, practical examples, command snippets, and actionable remediations. No redundancy, no cross-references.)_

Anti-patterns are practices that _initially_ appear helpful or efficient but consistently lead to long-term operational pain, failures, and complexity.  
This chapter highlights four of the most harmful anti-patterns found in Kubernetes, GKE, and service-mesh-based environments.

---

# **50.1 Snowflake Clusters**

A **snowflake cluster** is a Kubernetes cluster with unique, hand-tuned, undocumented, or manually edited components.  
Each change seems harmless, but the end result is:

- inconsistent environments
    
- impossible troubleshooting
    
- unpredictable deployments
    
- different behavior per cluster
    
- slow or blocked upgrades
    
- no reproducibility
    

The “snowflake” comes from the fact that **every cluster is unique**, making automation impossible.

---

## **50.1.1 Symptoms**

- “dev works but staging doesn’t”
    
- minor updates break only one cluster
    
- platform engineers do not know exact config of each cluster
    
- cluster creation takes hours due to manual steps
    
- different node pools, taints, labels, mesh settings per cluster
    
- recurring drift between IaC and actual infra
    

---

## **50.1.2 Concrete Examples**

### **Example #1 — Manual changes to cluster autoscaler**

```bash
kubectl edit configmap cluster-autoscaler-config -n kube-system
```

Someone presses **save**, cluster drifts from GitOps truth.

---

### **Example #2 — Inconsistent addons**

Cluster A uses CloudDNS;  
Cluster B uses CoreDNS custom config;  
Cluster C uses node-local DNS.

Impossible to troubleshoot consistently.

---

### **Example #3 — Custom mesh policy applied only to prod**

```yaml
apiVersion: security.istio.io/v1beta1
kind: PeerAuthentication
# accidentally applied manually
```

---

## **50.1.3 Debugging Snowflake Clusters**

### **Step 1 — Identify Drift**

```bash
kubectl get cm,deploy,ds,rs -A --show-managed-fields=false
```

Look for local manual edits.

---

### **Step 2 — Identify IaC Mismatch**

```bash
kubectl diff -f environments/prod/
```

---

### **Step 3 — Detect Unique Behaviors**

Compare clusters:

```bash
gcloud container clusters describe <cluster>
```

---

## **50.1.4 Remediation**

### **Fix 1 — Full GitOps Enforcement**

Everything must be declared in Git:

- node pools
    
- mesh config
    
- addons
    
- network policies
    
- ingress settings
    

---

### **Fix 2 — Mutating Webhook That Blocks `kubectl edit`**

Example Gatekeeper policy:

```yaml
apiVersion: constraints.gatekeeper.sh/v1beta1
kind: K8sNoEdit
metadata:
  name: forbid-edit
spec:
  match:
    kinds:
      - apiGroups: [""]
        kinds: ["ConfigMap", "Deployment"]
```

---

### **Fix 3 — Cluster Templates**

One source of truth YAML:

```yaml
clusters:
  - name: prod-us-central1
    version: 1.29
    addons:
      dns: node-local
      mesh: istio
```

---

## **50.1.5 Common Pitfalls**

- believing “just this one exception” is safe
    
- debugging cluster-specific behaviors for months
    
- disaster recovery impossible because cluster can’t be recreated
    
- engineers fear touching infra
    
- long-term compounding drift
    

---

# **50.2 Mesh Rule Overgrowth**

Mesh rule overgrowth happens when **Istio/Envoy configuration becomes uncontrollably large**.  
This leads to **slow deployments**, **massive proxy memory usage**, **propagation delays**, and **mysterious outages** due to conflicting rules.

---

## **50.2.1 Symptoms**

- VirtualServices > 2000 lines
    
- DestinationRules with dozens of subsets
    
- Envoy memory > 500MB per sidecar
    
- slow config push from control plane
    
- severe latency caused by complex retry chains
    
- traffic “leaking” to unintended clusters or subsets
    
- multiple engineers afraid to touch mesh configs
    

---

## **50.2.2 Examples**

### **Example #1 — Bloated VirtualService**

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: checkout
spec:
  hosts:
  - checkout.svc
  http:
  - route:
    - destination:
        host: checkout
        subset: v1
    retries:
      attempts: 10
  # 20 more blocks...
```

Retries + many rules = guaranteed retry storms.

---

### **Example #2 — Unbounded Subsets**

A team creates subsets for each branch:

```
v1
v1.1
v1.1-test
v1.2-release
feature-abc
```

Sidecar config explodes.

---

## **50.2.3 Diagnostics**

### **Check Sidecar Config Size**

```bash
kubectl exec <pod> -c istio-proxy -- curl localhost:15000/config_dump | wc -l
```

Over 200k lines = dangerous.

---

### **Check Pilot Agent Errors**

```bash
kubectl logs <pod> -c istio-proxy | grep -i "config"
```

Look for `NACK` messages.

---

## **50.2.4 Remediation**

### **Fix 1 — Apply “One Service = One VirtualService” rule**

Multiple teams touching one VS → disaster.

---

### **Fix 2 — Remove unused subsets**

Find live subsets:

```bash
istioctl proxy-config endpoints <pod> | grep checkout
```

Unused subset? Remove.

---

### **Fix 3 — Centralize mesh governance**

Create an “API for traffic management” rather than letting everyone modify raw Istio YAML.

---

### **Fix 4 — Use Ambient Mesh (no sidecars)**

If applicable, removes most per-service mesh config.

---

## **50.2.5 Common Pitfalls**

- assuming Istio scales infinitely with rules
    
- layering retries on top of retries
    
- using subsets as feature flags
    
- ignoring MTLS policy/traffic rule interactions
    
- creating per-path/per-header routing explosion
    

---

# **50.3 YAML Sprawl**

YAML sprawl occurs when configuration files balloon across repos, directories, and formats.  
It causes:

- unclear ownership
    
- conflicting config sources
    
- duplicated manifests
    
- copy/paste divergence
    
- impossible onboarding
    
- accidental downtime because one YAML overrides another
    

---

## **50.3.1 Symptoms**

- 20+ YAML files for a single service
    
- repetition of ConfigMap values across repos
    
- inconsistent naming conventions
    
- engineers copying deployment files between services
    
- GitOps drift because multiple repos apply overlapping manifests
    
- onboarding requires “tribal knowledge”
    

---

## **50.3.2 Examples**

### **Example 1 — Multiple Deployment Versions**

```
deployment.yaml
deployment-prod.yaml
deployment-temp.yaml
deployment-old.yaml
```

### **Example 2 — Conflicting Ingress Configs**

Many manifests apply the same IngressClass, leading to instability.

---

## **50.3.3 Diagnostics**

### **Find duplicate Kubernetes objects**

```bash
kubectl get deploy -A --show-labels | grep checkout
```

### **Detect conflicting Ingress definitions**

```bash
kubectl get ingress -A
```

### **Scan repos for duplicate YAML**

```bash
grep -R "kind: Deployment" .
```

---

## **50.3.4 Remediation**

### **Fix 1 — Use Kustomize or Helm**

Kustomize example:

```yaml
bases:
  - ../../base
patches:
  - replicas-patch.yaml
```

---

### **Fix 2 — Consolidate ConfigMaps**

Use environment overlays instead of multiple copies:

```yaml
configMapGenerator:
- name: checkout-config
  behavior: merge
```

---

### **Fix 3 — Enforce Organizational YAML Conventions**

OPA policy:

```yaml
apiVersion: constraints.gatekeeper.sh/v1beta1
kind: K8sAllowedAnnotations
```

---

### **Fix 4 — Move “golden configs” to a platform repo**

No more copy/paste per team.

---

## **50.3.5 Common Pitfalls**

- treating YAML as “code dump” instead of configuration
    
- ignoring DRY principles
    
- editing GitOps-managed YAML by hand locally
    
- duplicating container image versions across manifests
    
- scattering mesh rules across multiple repos
    

---

# **50.4 Runbook Gaps**

Runbook gaps are a silent anti-pattern.  
They show up only during incidents—**when it's too late**.

A gap could be:

- no runbook
    
- outdated runbook
    
- missing commands
    
- unclear mitigation steps
    
- referencing nonexistent services
    
- runbook exists but isn’t discoverable
    
- requiring tribal knowledge to execute
    

---

## **50.4.1 Symptoms**

- engineers freeze during incidents
    
- Slack messages like “Does anyone know how to…”
    
- troubleshooting done by trial & error
    
- inconsistent resolutions
    
- long MTTR
    
- lack of predictable escalation
    

---

## **50.4.2 Examples**

### **Example #1 — Runbook Missing Critical Step**

Runbook says:

> “Fail over traffic to region B.”

But does not include:

```bash
gcloud compute backend-services update web --failover --global
```

Leaving responders guessing.

---

### **Example #2 — Runbook Says “Restart Service” Without Commands**

Should specify:

```bash
kubectl rollout restart deploy checkout
```

---

## **50.4.3 Diagnostics**

### **Check for missing or outdated runbooks**

Audit at least quarterly:

```bash
grep -R "TODO" runbooks/
```

### **Check runbook usability via simulation**

Perform a game day:

- follow runbook exactly
    
- if responders ask questions → runbook failure
    

---

## **50.4.4 Remediation**

### **Fix 1 — Standard Runbook Format**

Must include:

1. symptoms
    
2. immediate staunch actions
    
3. diagnostic workflow
    
4. commands
    
5. rollback steps
    
6. escalation path
    
7. owner
    

---

### **Fix 2 — Make Runbooks Executable**

Use:

- bash scripts
    
- CLI tools
    
- `kubectl` helpers
    
- drop-down decision trees
    

Example helper script:

```bash
#!/bin/bash
kubectl logs -n istio-system deploy/istio-ingressgateway --since=10m
```

---

### **Fix 3 — Tie Runbook to Alerts**

Every alert must link to:

```
runbook_url: https://internal/runbooks/latency
```

---

### **Fix 4 — Use ChatOps to Trigger Stored Procedures**

Example (Slack slash command):

```
/runbook failover checkout
```

Runs a safe script.

---

## **50.4.5 Common Pitfalls**

- writing runbooks for ideal scenarios, not real failures
    
- missing rollback instructions
    
- ignoring partial failures (node/zone-level)
    
- writing runbooks with no verification steps
    
- using vague wording like “check logs”
    

---

