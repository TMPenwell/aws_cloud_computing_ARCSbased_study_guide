# Module 1 Guided Notes: Cloud Computing Concepts

Nov 23, 2026 · @Tasha

## Start Here

These guided notes cover Module 1 and every topic in Domain 1 (Cloud Concepts) of the AWS Certified Cloud Practitioner exam. Fill in each numbered blank during lecture or reading, then check your work against the answer key at the end.

Every section follows the same four-step rhythm, based on Keller's ARCS model of motivation:

| Step | What it does | What you do |
| --- | --- | --- |
| **Attention** | Opens with a question or scenario | Jot a quick answer before reading on |
| **Relevance** | Shows where this shows up in business | Connect it to your major or job |
| **Confidence** | Guided notes with numbered blanks, plus a quick check | Fill blanks, then check the answer key |
| **Satisfaction** | A short real-world task | Use what you just learned |

### Exam connection

Domain 1 makes up 24% of the scored content on the Cloud Practitioner exam. Use this map to see which exam task each section supports.

| Section | Exam task statement |
| --- | --- |
| 1. What is cloud computing? | Background for all of Domain 1 |
| 2. Benefits of the cloud | 1.1 Define the benefits of the AWS Cloud |
| 3. Introduction to AWS | Background (Domain 3 covers services in depth) |
| 4. Moving to the cloud | 1.3 Benefits of and strategies for migration |
| 5. Well-Architected Framework | 1.2 Identify design principles of the AWS Cloud |
| 6. Cloud economics | 1.4 Understand concepts of cloud economics |

### Learning objectives

By the end of Module 1, you should be able to:

- [ ] Define the different types of cloud computing models
- [ ] Describe six advantages of cloud computing and the benefits of AWS global infrastructure
- [ ] Recognize the main AWS service categories and core services
- [ ] Review the AWS Cloud Adoption Framework and choose a migration strategy
- [ ] Identify and tell apart the six pillars of the AWS Well-Architected Framework
- [ ] Explain core ideas of cloud economics, including rightsizing and licensing

### Warm-up

Think about the last time you streamed a show, backed up photos, or turned in an assignment online. Where did the files live, and whose computer did the work?

My answer: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Section 1: What Is Cloud Computing?

**Attention.** A two-person startup and a Fortune 500 company can rent the same computing power on the same afternoon. How do you think that is possible?

My guess: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Relevance.** As a business professional, you will approve budgets, choose vendors, and sit in meetings about "moving to the cloud." The terms in this section are the vocabulary of those conversations.

### Cloud computing defined

Cloud computing is the (1) \_\_\_\_\_\_\_\_\_\_ delivery of compute power, databases, storage, applications, and other IT resources.

- It is delivered over the (2) \_\_\_\_\_\_\_\_\_\_.
- It uses (3) \_\_\_\_\_\_\_\_\_\_ pricing.
- Resources run on servers in large (4) \_\_\_\_\_\_\_\_\_\_ in different locations around the world.

### Infrastructure as software

Cloud computing lets you stop thinking of infrastructure as (5) \_\_\_\_\_\_\_\_\_\_ and start using it as (6) \_\_\_\_\_\_\_\_\_\_ instead.

### Traditional model vs. cloud model

|  | Traditional computing model | Cloud computing model |
| --- | --- | --- |
| Infrastructure is treated as | (7) \_\_\_\_\_\_\_\_\_\_ | Software |
| Requires | Space, staff, physical security, planning, and (8) \_\_\_\_\_\_\_\_\_\_ expenditure | Little up-front investment |
| Getting new resources | A long hardware (9) \_\_\_\_\_\_\_\_\_\_ cycle (quote, approval, shipping, installation can take weeks or months) | Changes happen more quickly, easily, and cost-effectively |
| Capacity planning | Provision by guessing maximum (10) \_\_\_\_\_\_\_\_\_\_ | (11) \_\_\_\_\_\_\_\_\_\_ scaling: grows and shrinks with demand |
| Team's time | Spent on hardware upkeep | Eliminates undifferentiated heavy-lifting tasks |

**Discuss:** What does it mean to "guess maximum peaks"? Picture a ticket website the morning a big concert goes on sale. What happens if the company guesses too low? Too high?

My notes: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

### Cloud service models

There are three main service models. Each one is a different part of the cloud computing stack and gives you a different level of (12) \_\_\_\_\_\_\_\_\_\_ over IT resources. Other models exist, but these three are the foundation.

| Model | Stands for | What it means | Example |
| --- | --- | --- | --- |
| **IaaS** | Infrastructure as a Service | Basic building blocks for cloud IT: networking, storage, compute. Highest level of (13) \_\_\_\_\_\_\_\_\_\_ and management control. Most similar to traditional IT. | Amazon EC2 |
| **PaaS** | (14) \_\_\_\_\_\_\_\_\_\_ | Provider manages the underlying infrastructure (hardware and OS). You focus on deploying and managing your apps. | AWS Elastic Beanstalk |
| **SaaS** | (15) \_\_\_\_\_\_\_\_\_\_ | A completed product the provider runs and manages, usually end-user apps. You only think about how to use the software. | Gmail, Microsoft 365, Salesforce |

**Memory hook (pizza as a service):** IaaS is renting a kitchen and buying your own ingredients. PaaS is take-and-bake: you just handle the oven. SaaS is pizza delivered to your door.

### Cloud deployment models

| Model | Where it runs | Key idea |
| --- | --- | --- |
| **Cloud** | Every part of the app runs in the cloud | Apps are either built in the cloud or (16) \_\_\_\_\_\_\_\_\_\_ from existing infrastructure. They can use low-level infrastructure or higher-level managed services. |
| **Hybrid** | Connects cloud resources with existing (17) \_\_\_\_\_\_\_\_\_\_ resources | Lets an organization grow into the cloud while staying connected to internal systems. |
| **On-premises** | The organization's own data center, using virtualization and resource management tools | Sometimes called a (18) \_\_\_\_\_\_\_\_\_\_ cloud. Chosen for dedicated resources, but lacks many cloud benefits. |

### AWS vs. traditional IT

Almost anything you can build with traditional IT, you can build with an AWS service.

| Area | Traditional IT | AWS |
| --- | --- | --- |
| Security | Firewalls, ACLs, administrators | Security groups, network ACLs, IAM |
| Networking | Router, network pipeline, switch | Elastic Load Balancing, Amazon VPC |
| Compute | On-premises servers | AMIs launched as Amazon EC2 instances |
| Storage and databases | DAS, SAN, NAS, RDBMS | Amazon EBS, Amazon EFS, Amazon S3, Amazon RDS |

### Check yourself (Confidence)

1. A company uses Microsoft 365 for email and documents. Which service model is that? \_\_\_\_\_\_\_\_\_\_
2. A bank keeps customer records in its own data center but runs its public website on AWS. Which deployment model is that? \_\_\_\_\_\_\_\_\_\_
3. In your own words, what does pay-as-you-go mean? \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

### Apply it (Satisfaction)

Think of a business you know: your workplace, a family business, or a campus office. Name one app it uses and label it IaaS, PaaS, or SaaS.

App: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ Model: \_\_\_\_\_\_\_\_\_\_

## Section 2: Benefits of the AWS Cloud

*Exam task 1.1: Define the benefits of the AWS Cloud.*

**Attention.** Why can Costco or Sam's Club sell a 48-pack of batteries for less per battery than a corner store? Keep your answer in mind for advantage #2.

My answer: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Relevance.** These benefits make up the AWS *value proposition*: the arguments you would put in a business case for cloud adoption. Several are finance ideas you already know from accounting and economics.

### The six advantages of cloud computing

| # | Advantage | What it means |
| --- | --- | --- |
| 1 | Trade (19) \_\_\_\_\_\_\_\_\_\_ for variable expense | **Capex** = funds a company uses to acquire, upgrade, and maintain physical assets. **Variable expense** = an expense that can be changed or avoided. You pay only for what you use. |
| 2 | Benefit from massive (20) \_\_\_\_\_\_\_\_\_\_ | AWS combines usage from all its customers, gets lower costs, and passes the savings on. Customers get lower variable costs than they could on their own. |
| 3 | Stop guessing (21) \_\_\_\_\_\_\_\_\_\_ | Scale up or down on demand instead of over- or under-estimating server needs. |
| 4 | Increase speed and (22) \_\_\_\_\_\_\_\_\_\_ | New IT resources are a click (console) or a line of code (CLI) away. Time to get resources to developers drops from weeks to minutes, so experimenting costs less. |
| 5 | Stop spending money running and maintaining (23) \_\_\_\_\_\_\_\_\_\_ | Focus on projects that set the business apart, not on racking, stacking, and powering servers. |
| 6 | Go (24) \_\_\_\_\_\_\_\_\_\_ in minutes | Deploy an app in multiple AWS Regions around the world in a few clicks. Customers get lower latency and a better experience at minimal cost. |

### AWS global infrastructure

Advantage #6 is possible because of how AWS builds its global infrastructure.

- **Regions** are separate geographic areas around the world where AWS clusters data centers.
- Each Region contains multiple, isolated (25) \_\_\_\_\_\_\_\_\_\_. Each one is one or more data centers with its own power and networking.
- **Edge locations** sit close to end users and cache content so it loads faster.

Two business benefits the exam names:

- **Speed of deployment:** launch in a new part of the world in minutes, with no new building to lease.
- **Global reach:** serve customers from a location near them, which lowers (26) \_\_\_\_\_\_\_\_\_\_ (the delay before data arrives).

### High availability, elasticity, and agility

| Benefit | What it means | Business example |
| --- | --- | --- |
| (27) \_\_\_\_\_\_\_\_\_\_ | The system keeps running with little or no downtime, even when a part fails. Running across multiple Availability Zones makes this possible. | An online bank stays up when one data center loses power. |
| (28) \_\_\_\_\_\_\_\_\_\_ | Resources are added or removed automatically as demand rises and falls. | A pizza chain's ordering site handles Super Bowl Sunday, then shrinks back on Monday. |
| (29) \_\_\_\_\_\_\_\_\_\_ | The organization can try, launch, and change things quickly and cheaply. | A marketing team stands up a test website for a campaign in one afternoon. |

### Discuss

- **Advantage 4:** Have you used a tool you could try out right away, like Google Colab or Neon? What did you need to do to get set up?
- **Advantages 5 and 6 (Lyft):** Lyft runs on AWS instead of its own data centers. Who are Lyft's customers, and how does going global quickly help them?

My notes: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

### Check yourself (Confidence)

Match each scenario to the advantage or benefit it shows.

1. A retailer adds servers for Black Friday weekend and releases them on Monday. \_\_\_\_\_\_\_\_\_\_
2. A startup launches its app in Europe and Asia in the same week. \_\_\_\_\_\_\_\_\_\_
3. A CFO stops buying servers up front and pays a monthly bill based on use. \_\_\_\_\_\_\_\_\_\_
4. A hospital's patient portal keeps working when one data center has an outage. \_\_\_\_\_\_\_\_\_\_
5. A video game company's servers grow automatically on launch night, then shrink back. \_\_\_\_\_\_\_\_\_\_

### Apply it (Satisfaction)

Write a two-sentence pitch to a CFO for moving to the cloud. Use at least two of the benefits from this section.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Section 3: Introduction to AWS

**Attention.** Cloud computing is intangible: you cannot walk up and touch it. If you had to sketch "the cloud" for a friend, what would you draw?

My sketch or description: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Relevance.** You will not need to build every AWS service yourself. Knowing what is on the menu helps you talk with IT teams, read vendor proposals, and ask better questions.

### What are web services?

A **web service** is software that makes itself available over the (30) \_\_\_\_\_\_\_\_\_\_. It uses a standardized format, such as (31) \_\_\_\_\_\_\_\_\_\_ or (32) \_\_\_\_\_\_\_\_\_\_, for the request and response of an (33) \_\_\_\_\_\_\_\_\_\_ interaction.

- **XML** and **JSON** are text formats for packaging data so programs can read it.
- **API** (application programming interface) is a set of rules that lets one program ask another for something.

### What is AWS?

AWS is a secure cloud platform that offers a broad set of global, cloud-based products.

- On-demand access to compute, storage, network, database, and other IT resources and management tools
- Flexible: you pay only for the individual services you need, for as long as you use them
- Services work together like (34) \_\_\_\_\_\_\_\_\_\_ (a first look at the idea of microservices)

**Notice the pattern:** almost every offering is "\_\_\_\_\_\_\_\_ as a service." Why do you think that is?

### Categories of AWS services

Circle the categories you have heard of. Star one that connects to your major.

Analytics · Application Integration · AR and VR · Blockchain · Business Applications · Compute · Cost Management · Customer Engagement · Database · Developer Tools · End User Computing · Game Tech · Internet of Things · Machine Learning · Management and Governance · Media Services · Migration and Transfer · Mobile · Networking and Content Delivery · Robotics · Satellite · Security, Identity, and Compliance · Storage

### Choosing a service

The service you choose depends on your business (35) \_\_\_\_\_\_\_\_\_\_ and technical (36) \_\_\_\_\_\_\_\_\_\_.

### Three ways to interact with AWS

| Tool | How you use it | Best for |
| --- | --- | --- |
| (37) \_\_\_\_\_\_\_\_\_\_ | Point and click in a web browser | Exploring and learning |
| (38) \_\_\_\_\_\_\_\_\_\_ | Type commands in a terminal | Repeating tasks quickly |
| (39) \_\_\_\_\_\_\_\_\_\_ | Call AWS from code in a programming language | Building AWS into apps |

### Check yourself (Confidence)

1. A business analyst wants to look around AWS for the first time. Which way of interacting fits best? \_\_\_\_\_\_\_\_\_\_
2. A developer is building a mobile app that saves photos to AWS. Which way fits best? \_\_\_\_\_\_\_\_\_\_

### Apply it (Satisfaction)

Pick the category you starred above. Name one business problem a company might solve with it.

Category: \_\_\_\_\_\_\_\_\_\_\_\_\_\_ Problem: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Section 4: Moving to the Cloud

*Exam task 1.3: Understand the benefits of and strategies for migration to the AWS Cloud.*

**Attention.** A family doctor is not an expert in every part of the body, but they know how all the systems fit together and when to call a specialist. Cloud adoption works the same way. Which "specialist" might you become?

My answer: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Relevance.** Half of the framework is business capabilities. The Business perspective's stakeholders are business managers, finance managers, and budget owners: the jobs many business majors move into.

### What is the AWS CAF?

The AWS Cloud Adoption Framework gives guidance and best practices to help an organization build a comprehensive approach to cloud computing across the organization and throughout the IT (40) \_\_\_\_\_\_\_\_\_\_. It helps speed up successful cloud adoption.

The CAF is organized into (41) \_\_\_\_\_\_\_\_\_\_ perspectives. Each perspective has a set of capabilities, grouped into two categories:

&#91;embedded content: AWS CAF · 6 perspectives, 2 capability groups, key stakeholders\]

Business, People, and Governance cover business capabilities. Platform, Security, and Operations cover technical ones.

### The six perspectives

| Perspective | Stakeholders | Focus | Capabilities |
| --- | --- | --- | --- |
| **Business** | Business managers, finance managers, budget owners, strategy stakeholders | Build a strong business case and prioritize cloud initiatives. Make sure business strategy and goals align with (42) \_\_\_\_\_\_\_\_\_\_ strategy and goals. | IT finance, IT strategy, benefits realization, business risk management |
| **People** | Human resources, staffing, people managers | Evaluate org structure, roles, and new skill and process needs. Identify (43) \_\_\_\_\_\_\_\_\_\_ to prioritize training, staffing, and org changes that build an agile organization. | Resource, incentive, career, training, and organizational change management |
| **Governance** | CIO, program managers, enterprise architects, business analysts, portfolio managers | Align IT strategy with business strategy. Maximize the business value of IT investment and minimize business (44) \_\_\_\_\_\_\_\_\_\_. | Portfolio management, program and project management, business performance measurement, license management |
| **Platform** | CTO, IT managers, solutions architects | Describe the target-state architecture in detail. Use principles and patterns for new cloud solutions and for (45) \_\_\_\_\_\_\_\_\_\_ on-premises workloads to the cloud. | Compute, network, storage, and database provisioning; systems and solution architecture; application development |
| **Security** | CISO, IT security managers, IT security analysts | Meet the organization's security objectives. Focus on visibility, auditability, control, and (46) \_\_\_\_\_\_\_\_\_\_. | Identity and access management (IAM), detective control, infrastructure security, data protection, incident response |
| **Operations** | IT operations managers, IT support managers | Define how business is conducted day to day, quarter to quarter, and year to year. Identify process changes and training needed. | Service monitoring, application performance monitoring, resource inventory management, release and change management, reporting and analytics, business continuity and disaster recovery, IT service catalog |

### Business outcomes of cloud adoption

The exam names four outcomes an organization can expect when it follows the CAF.

| Outcome | What it looks like |
| --- | --- |
| Reduced business (47) \_\_\_\_\_\_\_\_\_\_ | Better reliability, security, and performance; fewer costly outages |
| Improved (48) \_\_\_\_\_\_\_\_\_\_ performance | Stronger environmental, social, and governance results, such as a smaller carbon footprint from shared, efficient data centers |
| Increased (49) \_\_\_\_\_\_\_\_\_\_ | New products and new markets reached faster |
| Increased operational (50) \_\_\_\_\_\_\_\_\_\_ | Routine work automated, lower operating costs |

### Migration strategies: the 7 Rs

Not every application moves the same way. AWS groups the choices into seven strategies, listed here from least change to most change.

| Strategy | Nickname | What happens | Example |
| --- | --- | --- | --- |
| **Retire** |  | Turn off apps that are no longer needed | Shut down an old reporting tool nobody uses |
| **Retain** | Revisit | Keep the app where it is for now | An app tied to a strict compliance rule stays on-premises |
| (51) \_\_\_\_\_\_\_\_\_\_ | Lift and shift | Move the app as-is, with no changes | Copy on-premises servers onto Amazon EC2 |
| **Relocate** | Hypervisor-level lift and shift | Move infrastructure to an equivalent cloud environment | Move VMware workloads to VMware Cloud on AWS |
| (52) \_\_\_\_\_\_\_\_\_\_ | Drop and shop | Switch to a different product, often SaaS | Replace an on-premises CRM with Salesforce |
| (53) \_\_\_\_\_\_\_\_\_\_ | Lift and reshape | Move with a few optimizations | Move an on-premises database to Amazon RDS |
| (54) \_\_\_\_\_\_\_\_\_\_ | Re-architect | Redesign the app to use cloud-native features | Rebuild one large app as microservices |

### Migration resources

**Database replication** copies data continuously from the old database to the new one while the old system keeps running. The business can switch over with very little downtime.

| Resource | What it helps with |
| --- | --- |
| AWS (55) \_\_\_\_\_\_\_\_\_\_ (AWS DMS) | Migrating and replicating databases |
| AWS Transform | Planning, tracking, and automating migrations |
| AWS Prescriptive Guidance | Step-by-step strategies and patterns written by AWS |
| AWS Partners and AWS Professional Services | Expert help planning and running a migration |

*Heads up:* older study materials mention AWS Migration Hub. It stopped accepting new customers on November 7, 2025, and AWS now points to AWS Transform instead ([AWS notice](https://docs.aws.amazon.com/migrationhub/latest/ug/migrationhub-availability-change.html)).

**Key idea:** Cloud adoption is not instantaneous for most organizations. It takes a thoughtful, deliberate strategy and alignment across the whole organization.

### Check yourself (Confidence)

Name the CAF perspective for each situation.

1. The CFO wants to know whether moving to AWS will save money. \_\_\_\_\_\_\_\_\_\_
2. HR needs a plan to train staff on new cloud tools. \_\_\_\_\_\_\_\_\_\_
3. The CISO reviews who can access customer data. \_\_\_\_\_\_\_\_\_\_
4. The IT support manager sets up monitoring and a disaster recovery plan. \_\_\_\_\_\_\_\_\_\_

Name the migration strategy.

5. A company replaces its on-premises email server with Microsoft 365. \_\_\_\_\_\_\_\_\_\_
6. A company copies its servers to Amazon EC2 exactly as they are. \_\_\_\_\_\_\_\_\_\_
7. A company shuts down an app that nobody has used in two years. \_\_\_\_\_\_\_\_\_\_

### Apply it (Satisfaction)

Which CAF perspective best fits the career you want? Which stakeholder role could you see yourself in, and why?

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Section 5: Design Principles and the AWS Well-Architected Framework

*Exam task 1.2: Identify design principles of the AWS Cloud.*

**Attention.** Before you buy a house, a home inspector checks the foundation, roof, wiring, and plumbing. What would an inspector for a cloud system need to check?

My answer: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Relevance.** Every cloud project involves trade-offs, such as faster versus cheaper. Business leaders weigh those trade-offs, and this framework gives everyone a shared checklist for doing it.

### What is the Well-Architected Framework?

The AWS Well-Architected Framework is AWS's checklist of best practices for designing and running systems in the cloud. It helps teams understand the pros and cons of their decisions and review a system the same way every time. It is built on (56) \_\_\_\_\_\_\_\_\_\_ pillars.

### The six pillars

| Pillar | The question it asks | Focus |
| --- | --- | --- |
| (57) \_\_\_\_\_\_\_\_\_\_ | How do we run and monitor systems and keep improving them? | Automate changes, respond to events, learn from mistakes |
| (58) \_\_\_\_\_\_\_\_\_\_ | How do we protect data, systems, and assets? | Control access, track activity, protect data |
| (59) \_\_\_\_\_\_\_\_\_\_ | Can the system recover from failure and meet demand? | Recover automatically, test recovery, scale to need |
| (60) \_\_\_\_\_\_\_\_\_\_ | Are we using the right resources well as needs change? | Pick the right resource types, go global, experiment |
| (61) \_\_\_\_\_\_\_\_\_\_ | Are we avoiding unneeded costs? | Pay only for what you use, measure spending, rightsize |
| (62) \_\_\_\_\_\_\_\_\_\_ | Are we reducing environmental impact? | Use resources fully, cut energy and waste |

**Memory hook (SCORPS):** **S**ecurity, **C**ost optimization, **O**perational excellence, **R**eliability, **P**erformance efficiency, **S**ustainability.

### Telling similar pillars apart

The exam often tests pillars that sound alike.

| Easy to confuse | How to tell them apart |
| --- | --- |
| Reliability vs. performance efficiency | Reliability = *does it keep working* when something breaks? Performance efficiency = *is it fast and right-sized* for the job? |
| Cost optimization vs. sustainability | Cost optimization saves *money*. Sustainability reduces *environmental impact*. Using fewer resources often helps both. |
| Security vs. operational excellence | Security protects data and access. Operational excellence is about *running and improving* the system day to day. |

### Check yourself (Confidence)

Name the pillar.

1. Encrypting customer credit card data. \_\_\_\_\_\_\_\_\_\_
2. Turning off unused servers to lower the monthly bill. \_\_\_\_\_\_\_\_\_\_
3. An app automatically recovers when a server fails. \_\_\_\_\_\_\_\_\_\_
4. Running servers at full use to cut energy waste. \_\_\_\_\_\_\_\_\_\_
5. Reviewing what went wrong after an outage and updating the process. \_\_\_\_\_\_\_\_\_\_

### Apply it (Satisfaction)

Pick an app you use every day. Which pillar would matter most to that company's customers, and why?

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Section 6: Cloud Economics

*Exam task 1.4: Understand concepts of cloud economics.*

**Attention.** Owning a car means a down payment, insurance, and repairs whether you drive or not. A rideshare means you pay per trip. Which costs less for someone who drives twice a month? For someone who drives every day?

My answer: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Relevance.** This is where cloud meets accounting and finance. Managers who understand these ideas can read a cloud bill, challenge a budget, and spot waste.

### Fixed vs. variable costs

- A **fixed cost** stays the same no matter how much you use. Example: a data center lease.
- A **variable cost** rises and falls with use. Example: a monthly AWS bill.

On-premises, most IT costs are (63) \_\_\_\_\_\_\_\_\_\_. In the cloud, most IT costs become (64) \_\_\_\_\_\_\_\_\_\_.

### Costs of an on-premises environment

Running your own data center comes with costs that are easy to overlook. Together they make up the (65) \_\_\_\_\_\_\_\_\_\_ (TCO).

- Servers, storage, and network hardware
- Software licenses
- Building space or rent
- Power and cooling
- Physical security
- IT staff to install, patch, and repair
- Capacity you pay for but do not use

### Licensing strategies

| Strategy | How it works | When it fits |
| --- | --- | --- |
| (66) \_\_\_\_\_\_\_\_\_\_ (BYOL) | Use software licenses you already own on AWS | You already paid for licenses and want to keep using them |
| License included | The license cost is built into the AWS price | You want no up-front purchase and pay-as-you-go licensing |

### Rightsizing

(67) \_\_\_\_\_\_\_\_\_\_ means matching the type and size of your resources to what the workload actually needs, at the lowest cost. Example: a server that runs at 10% of its capacity all month can move to a smaller, cheaper size. Rightsizing is ongoing, not a one-time task.

### Benefits of automation

- Fewer human (68) \_\_\_\_\_\_\_\_\_\_
- Faster, consistent setup every time
- Resources scale up and down on their own
- Schedules turn off test servers at night and on weekends
- Staff spend time on higher-value work

### Economies of scale, revisited

This connects back to advantage #2 in Section 2. Because AWS buys and runs infrastructure for millions of customers, its cost per unit is lower than any single company could get alone, and customers share in those savings.

### Check yourself (Confidence)

1. Which is a fixed cost: a data center lease or a monthly AWS bill? \_\_\_\_\_\_\_\_\_\_
2. A company's servers run at 10% use all month. What should it do? \_\_\_\_\_\_\_\_\_\_
3. A company already owns SQL Server licenses and wants to use them on AWS. Which licensing strategy fits? \_\_\_\_\_\_\_\_\_\_
4. Scheduling test servers to shut off every night is an example of what? \_\_\_\_\_\_\_\_\_\_

### Apply it (Satisfaction)

Picture a small local business that runs one server in a back closet. List three costs that would shrink or go away if it moved to the cloud.

Cost 1: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

Cost 2: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

Cost 3: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Module Wrap-Up

### Rate your confidence

Rate yourself from 1 (not yet) to 4 (I could teach it). Anything at 1 or 2, revisit that section before the quiz or exam.

| Objective | My rating (1–4) |
| --- | --- |
| Define the different types of cloud computing models |  |
| Describe the six advantages and the benefits of AWS global infrastructure |  |
| Recognize the main AWS service categories and core services |  |
| Review the AWS CAF and choose a migration strategy |  |
| Identify and tell apart the six Well-Architected pillars |  |
| Explain cloud economics: fixed vs. variable costs, TCO, licensing, rightsizing, automation |  |

### Reflect

One idea from this module I could explain to a boss or coworker tomorrow:

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

One question I still have:

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Answer Key

### Guided-note blanks

| Section | Answers |
| --- | --- |
| 1. Cloud computing | (1) on-demand · (2) internet · (3) pay-as-you-go · (4) data centers · (5) hardware · (6) software · (7) hardware · (8) capital · (9) procurement · (10) peaks · (11) elastic · (12) control · (13) flexibility · (14) Platform as a Service · (15) Software as a Service · (16) migrated · (17) on-premises · (18) private |
| 2. Benefits | (19) capital expense (capex) · (20) economies of scale · (21) capacity · (22) agility · (23) data centers · (24) global · (25) Availability Zones · (26) latency · (27) High availability · (28) Elasticity · (29) Agility |
| 3. Intro to AWS | (30) internet · (31) XML · (32) JSON (31 and 32 in either order) · (33) API · (34) building blocks · (35) goals · (36) requirements · (37) AWS Management Console · (38) AWS CLI · (39) AWS SDKs |
| 4. Moving to the cloud | (40) lifecycle · (41) six · (42) IT · (43) gaps · (44) risks · (45) migrating · (46) agility · (47) risk · (48) ESG (environmental, social, and governance) · (49) revenue · (50) efficiency · (51) Rehost · (52) Repurchase · (53) Replatform · (54) Refactor · (55) Database Migration Service |
| 5. Well-Architected | (56) six · (57) Operational excellence · (58) Security · (59) Reliability · (60) Performance efficiency · (61) Cost optimization · (62) Sustainability |
| 6. Cloud economics | (63) fixed · (64) variable · (65) total cost of ownership · (66) Bring Your Own License · (67) Rightsizing · (68) errors |

### Check-yourself answers

| Section | Answers |
| --- | --- |
| 1 | SaaS · Hybrid · You pay only for the resources you use, for as long as you use them |
| 2 | Stop guessing capacity · Go global in minutes · Trade capex for variable expense · High availability · Elasticity |
| 3 | AWS Management Console · AWS SDKs |
| 4 | Business · People · Security · Operations · Repurchase · Rehost · Retire |
| 5 | Security · Cost optimization · Reliability · Sustainability · Operational excellence |
| 6 | Data center lease · Rightsize to a smaller resource · BYOL · Automation |
