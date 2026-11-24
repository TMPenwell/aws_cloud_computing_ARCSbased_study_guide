# Module 3 Study Guide: AWS Global Infrastructure & Services

Nov 24, 2026 · @Tasha

## How to use this guide

Fill in each blank (\_\_\_\_\_\_) as you work through the Module 3 lesson, then check yourself against the answer key at the end. Each part follows Keller's ARCS model.

| ARCS stage | What it looks like here |
| --- | --- |
| **Attention** | A business scenario that opens the module |
| **Relevance** | "Why it matters for business" callouts tied to real decisions |
| **Confidence** | Guided notes with blanks, then short checkpoints |
| **Satisfaction** | Reflection prompts that apply the content to a business you know |

**Module objectives.** By the end of this module you should be able to:

1. Identify the difference between AWS Regions, Availability Zones (AZs), and edge locations.
2. Identify AWS services and service categories.

**Exam connection (AWS Certified Cloud Practitioner, CLF-C02).** This module maps mainly to Domain 3: Cloud Technology and Services (34% of the exam): Task 3.2 (global infrastructure) and Tasks 3.3–3.6 (compute, database, network, storage). The security and cost services also preview Domains 2 and 4.

**Callout key**

- **Vocab:** a term to know for the exam
- **Why it matters for business:** the decision a manager would make with this
- **Discuss:** a prompt for class or study-group conversation

## Attention: How is the World Wide Web world wide?

I once asked a room of medical residents and students how the internet travels across the globe. The only answer I got was "magic." Everyone laughed, but it showed how completely we take the infrastructure for granted. We use it every minute and almost never picture it.

It isn't magic. When you stream a video or check out online, your request travels as pulses of light through fiber-optic cables, including cables laid across the ocean floor, to buildings full of servers. Cloud providers like AWS own many of those buildings and the private networks that connect them. This module makes that hidden layer visible.

Now make it a business problem. Imagine you run marketing for an Ohio retailer that just launched an online store. Customers are in Columbus, Toronto, and London. On launch day, a storm knocks out power to a data center in Virginia. Does your store go dark?

The answer depends on choices someone made about **where** the store's servers run and **how many copies** exist. Those choices cost money, affect compliance, and decide whether customers can check out. By the end of this module, you will be able to make them.

**Before you start, jot down your guess:**

1. How is the World Wide Web world wide? Sketch or describe the path a web page takes to reach your phone. ("Magic" doesn't count.) \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
2. When you stream a video, how far away do you think the server sending it is? \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
3. If a company stores customer data in Europe, should it be allowed to copy that data to the U.S.? Why or why not? \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Section 1A: AWS Regions

The AWS Global Infrastructure is designed to deliver a flexible, reliable, scalable, and secure environment with high-quality global network performance. AWS keeps adding to it, so the map changes often.

**Discuss:** Open the AWS Global Infrastructure map. Which Region is closest to Ohio? Which continents have the fewest Regions?

### What is a Region?

- A Region is a physical \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A1) area of the world.
- Data replication across Regions is controlled by \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A2).
  - **Vocab:** *Data replication* = keeping copies of the same data in more than one place.
- Communication between Regions travels over the AWS \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A3) network infrastructure.
- Each Region provides full redundancy and connectivity to the network.
- A Region usually has \_\_\_\_\_\_ (A4) or more Availability Zones.

### Key rules about Regions

- Regions are \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A5) from each other. This helps a business achieve \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A6).
  - **Vocab:** *Fault tolerance* = the system keeps working even when a part fails.
- Resources in one Region are **not** automatically \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A7) to other Regions.
- If a business needs data copied across Regions, it is \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A8) responsibility to do it.
- Regions launched before \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A9) are enabled by default. Newer Regions are disabled until you enable them.
- Some Regions have restricted access, such as \_\_\_\_\_\_\_\_\_\_\_\_\_\_ and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A10).

**Why it matters for business:** Data stored in one Region stays there unless you copy it. That protects you from accidentally moving regulated data across borders, but it also means a Region-wide outage can take down a business that never planned a backup Region.

**Discuss:** How would a company decide whether it needs to replicate data to a second Region? Think about cost of downtime versus cost of a second copy.

### Selecting a Region

Consider these four factors, in order of importance:

| Rank | Factor | Question a manager asks |
| --- | --- | --- |
| 1 | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A11) | Are there laws about where this data may be stored? |
| 2 | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A12) | How close is the Region to our customers? |
| 3 | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A13) | Does the Region offer the services we need? |
| 4 | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (A14) | Is this Region cheaper or more expensive? |

**Vocab:** *Latency* = the delay between a request and its response. Shorter distance usually means lower latency.

## Section 1B: Availability Zones and Data Centers

A Region holds several Availability Zones; each AZ holds one or more data centers. You pick Regions and AZs, but never individual data centers.

### Availability Zones (AZs)

- Each AZ is a fully \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B1) partition of the AWS infrastructure.
- AZs consist of \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B2) data centers and are designed for \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B3).
- AZs connect to other AZs using \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B4) networking.
  - **Vocab:** *High-speed private networking* = dedicated, redundant fiber that AWS owns, not the public internet.
- An AZ usually has about \_\_\_\_\_\_ (B5) data centers and can include hundreds of thousands of servers.
- Each AZ has its own \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B6) infrastructure and sits many kilometers from other AZs, yet all AZs in a Region are within \_\_\_\_\_\_ (B7) km of each other.
- Running across multiple AZs makes applications more highly available, \_\_\_\_\_\_\_\_\_\_\_\_\_\_, and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B8) than a single data center allows.
- \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B9) are responsible for selecting the AZs where systems run. Systems can span multiple AZs.
- AWS recommends \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B10) data and resources across AZs so systems survive a temporary or prolonged AZ failure.
  - **Vocab:** *Partitioned* = an application split into pieces that run in different places.

**Why it matters for business:** Spreading an app across two or more AZs is the cheapest way to keep it online during a local disaster such as a flood, fire, or power failure. One AZ going down should not mean lost sales.

**Discuss:** How have well-known cloud outages affected businesses? Were the affected companies running in one AZ or several?

### AWS Data Centers

- Data centers are where data \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B11) and where processing happens.
- Each data center has redundant power, networking, and connectivity, and is housed in a separate facility.
- A data center typically holds \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B12) physical servers.
- Customers **cannot** select a data center. The most granular level you can choose is the \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B13).

**How data centers are built to reduce environmental risk**

1. A \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B14) design anticipates and tolerates failure while maintaining service levels.
2. Critical system components are backed up across multiple \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B15).
3. AWS continuously \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B16) service usage to deploy enough capacity.
4. Data center locations are \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B17), and all access is restricted.
5. When a failure happens, \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (B18) processes move traffic away from the affected area.

**Discuss:** AWS uses custom network equipment from original device manufacturers (ODMs). An ODM designs and builds a product to another company's specifications, and that company sells it under its own brand. Why might AWS prefer this over buying name-brand equipment?

## Section 1C: Points of Presence and Infrastructure Features

Points of Presence bring content closer to the customer, so pages and videos load faster no matter where the Region is.

### Points of Presence (PoPs)

- AWS runs a global network of PoPs made up of \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (C1) and a smaller number of \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (C2).
- PoPs are used with Amazon \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (C3), a global content delivery network.
  - **Vocab:** *Content delivery network (CDN)* = a network of servers that keeps copies of content near users to reduce latency.
- PoPs are located in most major cities and constantly measure connectivity and performance to find the best route for each request.

**Services that use PoPs**

| Service | What it does |
| --- | --- |
| Amazon CloudFront | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (C4) that distributes content to end users with low latency |
| Amazon Route 53 | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (C5) service; sends each request to the nearest edge location |
| AWS Shield | Protection against attacks (covered in Section 2) |
| AWS WAF | Web application firewall |

### Regional edge caches

- Used by default with CloudFront.
- Hold content that is accessed too \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (C6) to stay at an edge location.
- Save a trip back to the \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (C7) server.
  - **Vocab:** *Regional edge cache* = a middle layer between edge locations and the origin, for less popular content.

**Why it matters for business:** A slow page loses customers. Edge locations let a company in Ohio serve shoppers in London almost as fast as shoppers in Columbus, without building a London data center.

### AWS infrastructure features

Match each feature to its description by writing the letter.

| Feature | Letter | Description |
| --- | --- | --- |
| Elasticity and scalability | \_\_\_\_ (C8) | A. Keeps operating properly when a component fails, through built-in redundancy |
| Fault tolerance | \_\_\_\_ (C9) | B. High operational performance with minimal downtime and no human intervention |
| High availability | \_\_\_\_ (C10) | C. Capacity adapts dynamically and grows to accommodate demand |

### Putting it together

The diagram below shows how the pieces nest: Regions contain AZs, AZs contain data centers, and edge locations sit outside Regions, close to customers.

&#91;embedded content: AWS global infrastructure · Region, AZs, data centers, Points of Presence\]

A customer's request hits the nearest edge location first; if the content isn't cached there or in a regional edge cache, it comes from the origin inside the Region.

## Confidence Checkpoint 1

Try these without looking back. Aim for 5 of 6 before moving on.

**Key takeaways (fill in)**

- AWS Global Infrastructure consists of \_\_\_\_\_\_\_\_\_\_\_\_\_\_ and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (K1).
- The choice of Region is based on \_\_\_\_\_\_\_\_\_\_\_\_\_\_ requirements or to reduce \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (K2).
- Each AZ is physically separate and has redundant power, networking, and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (K3).
- Edge locations and regional edge caches improve performance by \_\_\_\_\_\_\_\_\_\_\_\_\_\_ content closer to users (K4).

**Quick check**

1. What is the smallest unit of AWS infrastructure a customer can choose? (a) Data center (b) Availability Zone (c) Region (d) Edge location
2. True or false: Data you store in the Ohio Region is automatically copied to the Oregon Region.
3. A hospital must keep patient records inside the country. Which Region-selection factor matters most?
4. Which service routes a user's request to the nearest edge location by translating a name into an IP address?
5. A company runs its website in two AZs. One AZ loses power. What happens, and which infrastructure feature does this show?
6. Name two reasons a business might run in **more than one Region**.

## Section 2A: Storage, Compute, and Database Services

The global infrastructure is the platform; services are what businesses actually rent on top of it.

### AWS foundational services

- The global infrastructure breaks into three elements: \_\_\_\_\_\_\_\_\_\_\_\_\_\_, \_\_\_\_\_\_\_\_\_\_\_\_\_\_, and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S1).
- It supports a broad set of services, including networking, storage, compute, and databases.
- Services are delivered as an on-demand utility, available in seconds, with \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S2) pricing.
- AWS groups its offerings into 23 product or service categories, each with one or more services.

### Storage

| Service | Guided note | Typical business use |
| --- | --- | --- |
| Amazon S3 | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S3) storage service offering scalability, availability, security, and performance | Website files, backups, archives, data for analytics |
| Amazon Elastic Block Store (EBS) | High-performance \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S4) storage, designed for use with \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S5) | Databases and enterprise apps that need fast reads and writes |
| Amazon Elastic File System (EFS) | Scalable, fully managed \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S6); grows and shrinks automatically as files are added or removed | Shared folders that many servers or offices use at once |

**Vocab:** *Network File System (NFS)* = a way for many computers to share the same files over a network.

**Discuss:** If S3 is a dump truck (huge capacity, cheap per load) and EBS is a race car (fast, attached to one server), which would you choose for 10 years of tax records? For a live checkout database?

### Compute

| Service | Guided note |
| --- | --- |
| Amazon EC2 | Resizable compute capacity: \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S7) in the cloud |
| Amazon EC2 Auto Scaling | Automatically adds or removes EC2 instances based on \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S8) you define |
| Amazon Elastic Container Service (ECS) | Highly scalable container \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S9) service that supports Docker containers |
| Amazon Elastic Container Registry (ECR) | Fully managed Docker container \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S10) to store, manage, and deploy images |
| AWS Elastic Beanstalk | Deploys and scales \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S11) on familiar servers such as Apache and Microsoft IIS |

**Why it matters for business:** Auto Scaling means a retailer pays for 50 servers on Black Friday and 5 on a quiet Tuesday, instead of buying 50 and leaving 45 idle most of the year.

### Database

| Service | Guided note |
| --- | --- |
| Amazon RDS | Makes it easy to set up, operate, and scale a \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S12) database; automates provisioning, patching, and backups |
| Amazon Aurora | Relational database compatible with \_\_\_\_\_\_\_\_\_\_\_\_\_\_ and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S13); up to 5x faster than standard MySQL and 3x faster than standard PostgreSQL |
| Amazon Redshift | Runs \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S14) queries against petabytes of local data and exabytes in S3 |
| Amazon DynamoDB | Key-value and document database with \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (S15) millisecond performance at any scale |

## Section 2B: Networking, Security, Cost, and Management Services

These services connect, protect, pay for, and watch over everything built in Section 2A.

### Networking and content delivery

| Service | Guided note |
| --- | --- |
| Amazon VPC | Provisions a logically \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N1) section of the AWS Cloud |
| Elastic Load Balancing | Automatically distributes incoming \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N2) across targets such as EC2 instances, containers, IP addresses, and Lambda functions |
| Amazon CloudFront | Fast CDN that securely delivers data, video, apps, and APIs globally with low \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N3) |
| AWS Transit Gateway | Connects \_\_\_\_\_\_\_\_\_\_\_\_\_\_ and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N4) networks through a single gateway |
| Amazon Route 53 | Scalable DNS web service; translates names into \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N5) |
| AWS Direct Connect | Establishes a dedicated \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N6) network connection from a data center or office to AWS |
| AWS VPN | Provides a secure private \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N7) from your network or devices to AWS |

**Discuss:** Sketch a VPC as a fenced lot inside a giant AWS campus. What goes inside the fence? Then explain why a company with 20 VPCs and three offices would want Transit Gateway instead of connecting each pair separately.

**Why it matters for business:** Direct Connect and VPN are how a company's existing office network reaches the cloud. Direct Connect costs more but gives steady bandwidth; VPN is cheaper and quicker to set up.

### Security, identity, and compliance

| Service | Guided note |
| --- | --- |
| AWS IAM | Securely manage \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N8) to AWS services and resources; create users and groups and allow or deny permissions |
| AWS Organizations | Restrict which services and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N9) are allowed in accounts |
| Amazon Cognito | Add user sign-up, sign-in, and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N10) to web and mobile apps |
| AWS Artifact | On-demand access to AWS security and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N11) reports and select online agreements |
| AWS KMS | Create and manage \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N12) used across AWS services and apps |
| AWS Shield | Managed \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N13) protection for apps running on AWS |

**Vocab:** *Distributed denial of service (DDoS)* = an attack that floods a site with fake traffic from many sources until real customers cannot get in.

### Cost management

| Service | Guided note |
| --- | --- |
| AWS Cost and Usage Report | The most \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N14) set of cost and usage data available, including pricing and reservation metadata |
| AWS Budgets | Sends alerts when costs or usage exceed, or are \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N15) to exceed, your budget |
| AWS Cost Explorer | Easy interface to \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N16), understand, and manage costs and usage over time |

### Management and governance

| Service | Guided note |
| --- | --- |
| AWS Management Console | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N17) user interface for accessing your AWS account |
| AWS Config | Tracks resource \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N18) and changes |
| Amazon CloudWatch | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N19) resources and applications |
| AWS Auto Scaling | Scales multiple resources to meet demand |
| AWS Command Line Interface (CLI) | Unified tool to manage AWS services |
| AWS Trusted Advisor | Helps optimize performance and \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N20) |
| AWS Well-Architected Tool | Helps review and improve workloads |
| AWS CloudTrail | Tracks user \_\_\_\_\_\_\_\_\_\_\_\_\_\_ (N21) and API usage |

**Discuss (scavenger hunt):** Log in to the AWS Management Console through AWS Academy. Find three services from this section in the search bar and note which category the console lists each under.

## Confidence Checkpoint 2

The exam asks you to pick the right service for a business need. Match each scenario to one service from Section 2.

| # | Business scenario | Service |
| --- | --- | --- |
| 1 | A startup needs virtual servers it can resize as the business grows | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| 2 | A marketing team wants to store thousands of product photos cheaply and durably | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| 3 | Finance wants an email when monthly AWS spending is forecast to pass $5,000 | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| 4 | An auditor asks for AWS's compliance reports | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| 5 | A mobile app needs customer sign-up and sign-in | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| 6 | Security wants a log of who changed what in the account, and when | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| 7 | An online store's website is being flooded with fake traffic | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| 8 | Analysts need to query years of sales data across petabytes | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| 9 | A manufacturer wants a dedicated, private line from its plant to AWS | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| 10 | IT wants to give interns read-only access to some resources | \_\_\_\_\_\_\_\_\_\_\_\_\_\_ |

**Category sort.** Write each service under its category: DynamoDB, EFS, Route 53, KMS, CloudWatch, Elastic Beanstalk.

- Storage: \_\_\_\_\_\_\_\_\_\_\_\_\_\_
- Compute: \_\_\_\_\_\_\_\_\_\_\_\_\_\_
- Database: \_\_\_\_\_\_\_\_\_\_\_\_\_\_
- Networking: \_\_\_\_\_\_\_\_\_\_\_\_\_\_
- Security: \_\_\_\_\_\_\_\_\_\_\_\_\_\_
- Management: \_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Satisfaction: Apply It

Go back to the online store from the opening scenario. You can now answer the question you started with.

1. **Revisit your guesses.** Look at your answers on page one. Could you now explain to a room of medical residents why the answer isn't magic? What would you change?
2. **Advise the store.** In 3–4 sentences, recommend a Region, explain how many AZs to use, and say how customers in London get fast page loads. Use at least three vocab terms.
3. **Pick a business you know** (a family business, an employer, a campus office). Name two AWS services from this module it could use, and the business problem each would solve.
4. **Self-rating.** Circle one: I could explain Regions vs. AZs vs. edge locations to a classmate — not yet / with notes / confidently.

Module summary: you can now tell Regions, Availability Zones, and edge locations apart, and you can name AWS services by category.

## Answer Key

**Section 1A: Regions**

A1 geographic · A2 you (the customer) · A3 backbone · A4 two · A5 isolated · A6 fault tolerance · A7 replicated · A8 your (the customer's) · A9 March 20, 2019 · A10 China; AWS GovCloud · A11 data governance · A12 latency · A13 services available in the Region · A14 cost

**Section 1B: AZs and data centers**

B1 isolated · B2 discrete · B3 fault isolation · B4 high-speed private · B5 three · B6 power · B7 100 · B8 fault tolerant; scalable · B9 You (customers) · B10 replicating · B11 resides · B12 50,000–80,000 · B13 Availability Zone · B14 redundant · B15 AZs · B16 monitors · B17 not disclosed · B18 automated

**Section 1C: PoPs and features**

C1 edge locations · C2 regional edge caches · C3 CloudFront · C4 CDN · C5 DNS (Domain Name System) · C6 infrequently · C7 origin · C8 C · C9 A · C10 B

**Checkpoint 1**

K1 Regions; Availability Zones · K2 compliance; latency · K3 connectivity · K4 caching

1. (b) Availability Zone
2. False. Data stays in its Region unless you replicate it.
3. Data governance
4. Amazon Route 53
5. The site keeps running from the other AZ. This shows high availability and fault tolerance.
6. Any two: disaster recovery or business continuity, lower latency for distant customers, data sovereignty rules.

**Section 2A: Storage, compute, database**

S1 Regions; AZs; Points of Presence · S2 pay-as-you-go · S3 object · S4 block · S5 Amazon EC2 · S6 Network File System (NFS) · S7 virtual machines · S8 conditions · S9 orchestration · S10 registry · S11 web applications and services · S12 relational · S13 MySQL; PostgreSQL · S14 analytic · S15 single-digit

**Section 2B: Networking, security, cost, management**

N1 isolated · N2 application traffic · N3 latency · N4 VPC; on-premises · N5 IP addresses · N6 private · N7 tunnel · N8 access · N9 actions · N10 access control · N11 compliance · N12 encryption keys · N13 DDoS · N14 comprehensive · N15 forecasted · N16 visualize · N17 Web-based · N18 inventory · N19 Monitors · N20 security · N21 activity

**Checkpoint 2**

1 Amazon EC2 · 2 Amazon S3 · 3 AWS Budgets · 4 AWS Artifact · 5 Amazon Cognito · 6 AWS CloudTrail · 7 AWS Shield · 8 Amazon Redshift · 9 AWS Direct Connect · 10 AWS IAM

Category sort: Storage – EFS · Compute – Elastic Beanstalk · Database – DynamoDB · Networking – Route 53 · Security – KMS · Management – CloudWatch
