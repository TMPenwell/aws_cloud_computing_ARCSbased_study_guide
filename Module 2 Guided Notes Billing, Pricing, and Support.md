# Module 2 Guided Notes: Billing, Pricing, and Support

Nov 23, 2026 · @Tasha

## How to use this guide

Fill in the blanks (\_\_\_\_\_\_\_\_) as you work through Module 2, then use the prompts to discuss, apply, and build flashcards. This guide maps to **Exam Domain 4: Billing, Pricing, and Support (12% of the AWS Certified Cloud Practitioner exam)**.

Each section follows Keller's ARCS model:

| Label | ARCS element | What you do |
| --- | --- | --- |
| **\[A\] Hook** | Attention | Start with a question or real-world scenario |
| **\[R\] Why it matters** | Relevance | Connect the concept to business decisions |
| **\[C\] Check yourself** | Confidence | Fill blanks, answer quick-check questions |
| **\[S\] Apply it** | Satisfaction | Use the concept in a scenario or activity |

**Legend**

- **\[PLACEHOLDER: ...\]** = content still to be added by the instructor
- **Exam tip** = something the certification exam tests directly
- **Updated** = current AWS information that differs from the original module slides

## Section 1: Fundamentals of Pricing

**\[A\] Hook:** Your phone plan charges for minutes, storage, and data. Which one surprises you most on the bill? AWS works the same way.

### The three cost drivers

| Cost driver | How it's usually charged | Notes |
| --- | --- | --- |
| 1. \_\_\_\_\_\_\_\_ | Per hour or per \_\_\_\_\_\_\_\_ | Varies by instance \_\_\_\_\_\_\_\_ |
| 2. \_\_\_\_\_\_\_\_ | Per \_\_\_\_\_\_\_\_ |  |
| 3. \_\_\_\_\_\_\_\_ | Per GB | **Inbound** is usually \_\_\_\_\_\_\_\_; **outbound** is aggregated and \_\_\_\_\_\_\_\_ |

**Exam tip:** Data transfer *within* a Region isn't always free. Traffic between Availability Zones is charged. Know in-Region vs cross-Region transfer.

### How to pay for AWS

&#91;PLACEHOLDER: confirm whether to teach three or four ways to pay\]

1. **Pay for what you \_\_\_\_\_\_\_\_**
   - No large upfront \_\_\_\_\_\_\_\_ (capital expense)
   - No need to buy servers, software licenses, or lease facilities
   - All services are available \_\_\_\_\_\_\_\_ with no long-term contracts
   - **Talking point:** \[PLACEHOLDER: Lyft case study on adapting to changing business needs\]
2. **Pay less when you \_\_\_\_\_\_\_\_**
   - Reserved Instances (RIs) save up to \_\_\_\_\_\_\_\_% vs On-Demand (**Updated:** 72%, not 75%)
   - Savings Plans offer similar discounts with more flexibility. AWS now recommends Savings Plans over RIs.
3. **Pay less by using \_\_\_\_\_\_\_\_**
   - Volume-based discounts and \_\_\_\_\_\_\_\_ pricing (S3, EBS, EFS)
   - The more you use, the \_\_\_\_\_\_\_\_ you pay per GB
4. **Pay less as AWS \_\_\_\_\_\_\_\_**
   - AWS passes on savings from economies of \_\_\_\_\_\_\_\_
   - **Talking point:** The "Walmart effect." How does a giant retailer keep prices low?
   - **Clarification:** Newer, faster resource generations are often cheaper or better for the same price. Your existing resources are **not** upgraded automatically; you migrate to them.

### Reserved Instance payment options

| Option | Upfront payment | Discount |
| --- | --- | --- |
| AURI: All Upfront | \_\_\_\_\_\_\_\_ | \_\_\_\_\_\_\_\_ |
| PURI: Partial Upfront | Some | Medium |
| NURI: No Upfront | \_\_\_\_\_\_\_\_ | \_\_\_\_\_\_\_\_ |

**\[R\] Why it matters:** Choosing an RI option is a **cash-flow decision**. A company with cash on hand saves more by paying upfront; a company protecting cash pays more over time.

### Other pricing facts

- **Custom pricing:** for \_\_\_\_\_\_\_\_-volume projects with unique requirements
- **AWS Free Tier:** for \_\_\_\_\_\_\_\_ customers, on certain services
- **Services with no charge:** Amazon VPC, AWS IAM, Elastic Beanstalk, AWS CloudFormation, automatic scaling, and \_\_\_\_\_\_\_\_ billing (**Updated:** remove OpsWorks, which has reached end of life)
- **Watch out:** a free service can launch resources that **do** cost money. Example: Elastic Beanstalk is free, but the EC2 instances it creates are not.

### Consolidated billing

- One \_\_\_\_\_\_\_\_ for multiple accounts
- Combined usage can unlock volume \_\_\_\_\_\_\_\_ discounts
- You can still track each \_\_\_\_\_\_\_\_'s charges

**\[C\] Check yourself**

1. Which data transfer direction is usually free?
2. Which RI option gives the largest discount?
3. Name one free service and one cost it could still create.

**\[S\] Apply it:** A startup expects steady traffic for 3 years but has little cash. Which RI payment option fits, and why?

## Section 2: Total Cost of Ownership (TCO)

**\[A\] Hook:** Your company's server room has 40 servers. Besides the servers, what else are you paying for? List as many costs as you can in 60 seconds.

### On-premises vs cloud

|  | On-premises | Cloud |
| --- | --- | --- |
| Who owns the hardware? | \_\_\_\_\_\_\_\_ | The service \_\_\_\_\_\_\_\_ |
| Cost type | Mostly fixed costs and \_\_\_\_\_\_\_\_ | Pay for what is \_\_\_\_\_\_\_\_ |
| Scaling up | Expensive and \_\_\_\_\_\_\_\_ | Provisioned when needed |
| Scaling down | Does **not** reduce \_\_\_\_\_\_\_\_ costs | Decommissioned when no longer used |

**Talking point:** What are some capital expenses (capex) of running your own data center?

**Talking point:** In this context, who is the "customer"?

### What is TCO?

- A financial \_\_\_\_\_\_\_\_ that identifies the **direct** and **indirect** costs of a system
- Used to:
  - Compare running a workload on-premises vs on \_\_\_\_\_\_\_\_
  - Budget and build a business \_\_\_\_\_\_\_\_ for moving to the cloud

### TCO cost categories

| Category | Includes |
| --- | --- |
| Server costs | Hardware, \_\_\_\_\_\_\_\_, facilities |
| Storage costs | Hardware, administration, \_\_\_\_\_\_\_\_ |
| Network costs | Hardware, administration, facilities |
| IT labor costs | Cost to \_\_\_\_\_\_\_\_ the solution |

- **Direct costs:** tied to running a server, such as \_\_\_\_\_\_\_\_, floor space, storage, and IT operations
- **Indirect costs:** supporting infrastructure, such as network and \_\_\_\_\_\_\_\_ infrastructure

**\[S\] Apply it, sorting activity:** Sort each cost into Direct or Indirect: electricity, server rack, network switches, backup storage, cooling, security staff, software licenses.

&#91;PLACEHOLDER: full list of direct and indirect costs for the sorting activity answer key\]

**Talking point:** Does moving to the cloud mean you no longer need IT professionals? Do jobs disappear, or shift?

### AWS Pricing Calculator

Use it to:

- Estimate \_\_\_\_\_\_\_\_ costs
- Find opportunities to \_\_\_\_\_\_\_\_ costs
- Model solutions \_\_\_\_\_\_\_\_ building them
- Explore price points and the math behind an estimate
- Find instance types and contract terms that meet your needs
- Name estimates and create named \_\_\_\_\_\_\_\_ of services

**\[S\] Apply it:** \[PLACEHOLDER: Pricing Calculator scenario, such as a small business web app, with step-by-step instructions\]

### Hard vs soft benefits

| Hard benefits (easy to measure) | Soft benefits (hard to measure) |
| --- | --- |
| Reduced spending on compute, storage, networking, security | Reuse of services and apps to redefine solutions |
| Lower hardware and software \_\_\_\_\_\_\_\_ | Increased developer \_\_\_\_\_\_\_\_ |
| Lower operational, backup, and disaster recovery costs | Improved customer \_\_\_\_\_\_\_\_ |
| Fewer operations personnel | Agile processes that respond to new opportunities |
|  | Increased \_\_\_\_\_\_\_\_ reach |

- **Cloud TCO:** what you will spend on technology *after* adoption. Easy to calculate but gives a \_\_\_\_\_\_\_\_ view of total financial impact.
- **Return on Investment (ROI):** the value generated, considering both spending and \_\_\_\_\_\_\_\_. Starts with **hard** benefits.
- Soft savings can be \_\_\_\_\_\_\_\_ valuable than hard savings.

**\[R\] Why it matters:** As a business major, you may build the business case for a cloud migration. A TCO-only case can undersell the cloud; include ROI and soft benefits.

**Talking point:** \[PLACEHOLDER: 1 to 2 case studies showing soft benefits\]

**\[C\] Check yourself**

1. Name two direct and two indirect costs of an on-premises data center.
2. Why can a TCO-only comparison be misleading?
3. Classify "improved customer satisfaction" as a hard or soft benefit.

## Section 3: AWS Organizations

**\[A\] Hook:** A company has 30 AWS accounts: one per department, plus test accounts. How does finance get *one* bill, and how does IT stop interns from launching expensive servers?

### What is AWS Organizations?

- A \_\_\_\_\_\_\_\_ account management service
- Consolidates multiple AWS accounts into an \_\_\_\_\_\_\_\_
- Includes consolidated \_\_\_\_\_\_\_\_ and account management
- Helps meet budget, \_\_\_\_\_\_\_\_, and compliance needs

**Main benefits**

1. Centrally managed \_\_\_\_\_\_\_\_ policies across accounts
2. Controlled access to AWS \_\_\_\_\_\_\_\_
3. Automated account \_\_\_\_\_\_\_\_ and management
4. Consolidated \_\_\_\_\_\_\_\_ across accounts

### Terminology

| Term | Definition |
| --- | --- |
| Organization (root) | The \_\_\_\_\_\_\_\_ of the hierarchy |
| Organizational unit (OU) | A \_\_\_\_\_\_\_\_ for accounts; can be nested inside other OUs |
| Account | The \_\_\_\_\_\_\_\_ of the tree |
| Service control policy (SCP) | Allows or denies access to AWS \_\_\_\_\_\_\_\_ for accounts in an OU |

- The hierarchy looks like an \_\_\_\_\_\_\_\_ tree, with the root at the top
- A policy attached to a node flows \_\_\_\_\_\_\_\_ to all branches and leaves below it
- An OU has only \_\_\_\_\_\_\_\_ parent; each account belongs to only \_\_\_\_\_\_\_\_ OU

**\[S\] Apply it:** \[PLACEHOLDER: company scenario and fill-in hierarchy diagram showing root, OUs, and accounts\]

### Security with AWS Organizations

| Tool | Controls access for... |
| --- | --- |
| IAM policies | AWS services, users, \_\_\_\_\_\_\_\_, and roles |
| SCPs | AWS services for individual accounts or groups of accounts in an \_\_\_\_\_\_\_\_ |

- An SCP affects **all** IAM users, groups, and roles in an account, including the account \_\_\_\_\_\_\_\_ user
- **Talking point:** Why should an SCP restrict even the root user?
- **Exam tip:** SCPs do **not** apply to the management (payer) account.

### Accessing AWS Organizations

- AWS Organizations \_\_\_\_\_\_\_\_
- AWS \_\_\_\_\_\_\_\_ (command line)
- AWS \_\_\_\_\_\_\_\_ (software development kits)
- HTTPS Query \_\_\_\_\_\_\_\_

**\[R\] Why it matters:** Organizations gives finance one consolidated bill with volume discounts, and gives IT guardrails. It's where governance and cost control meet.

**\[C\] Check yourself**

1. What is the difference between an IAM policy and an SCP?
2. If an SCP denies a service at an OU, which accounts are affected?
3. How does consolidated billing lower costs?

## Section 4: AWS Billing and Cost Management

**\[A\] Hook:** Your manager asks, "Why did our AWS bill jump 40% last month, and what will next quarter cost?" Which tool do you open first?

### Overview

AWS Billing and Cost Management is the service you use to:

- \_\_\_\_\_\_\_\_ your AWS bill
- Monitor \_\_\_\_\_\_\_\_
- \_\_\_\_\_\_\_\_ costs
- Forecast future costs and usage, filter and \_\_\_\_\_\_\_\_ data, and set custom time periods

### AWS Billing Dashboard

- Shows month-to-\_\_\_\_\_\_\_\_ AWS expenses
- Identifies which services drive most of your \_\_\_\_\_\_\_\_
- **Spend Summary:** last month's spend, month-to-date estimate, and this month's \_\_\_\_\_\_\_\_
- **Month-to-Date Spend by Service:** top services and their share of \_\_\_\_\_\_\_\_

### The four tools

| Tool | Use it to... | Key facts |
| --- | --- | --- |
| **AWS Bills** | See last month's costs for each \_\_\_\_\_\_\_\_ | Monthly bill plus a detailed breakdown |
| **AWS Cost Explorer** | Visualize and analyze costs and \_\_\_\_\_\_\_\_ over time | Free. Past \_\_\_\_\_\_\_\_ months; forecast up to \_\_\_\_\_\_\_\_ months (**Updated:** 18, not 3). Forecasts show an 80% prediction interval. |
| **AWS Budgets** | Get \_\_\_\_\_\_\_\_ when costs go over budget or are forecast to | Monthly, quarterly, or annual; custom dates; alerts by \_\_\_\_\_\_\_\_ or Amazon SNS |
| **AWS Cost and Usage Report (CUR)** | Get the most \_\_\_\_\_\_\_\_ cost and usage data | Hourly or daily line items; delivered to an Amazon \_\_\_\_\_\_\_\_ bucket; updated at least once a day. **Updated:** now delivered as CUR 2.0 through Data Exports |

**Exam tip:** Cost Explorer = *look back and analyze*. Budgets = *set a limit and get alerted*. CUR = *the most detailed raw data*.

**Talking point:** Why would a company care which Availability Zone has the most traffic, or which linked account spends the most?

**Talking point:** CUR files land in S3. How could an analyst pull them into Excel, Athena, or a dashboard?

**\[R\] Why it matters:** These tools let business teams do **chargeback**: billing each department for its share of cloud spend.

**\[C\] Check yourself**

1. Which tool would you use to get an email when spending passes $500?
2. How far back can Cost Explorer show data? How far forward can it forecast?
3. Where is the Cost and Usage Report delivered?

**\[S\] Apply it:** Match each need to a tool: (a) explain last quarter's spike, (b) warn the team before overspending, (c) load line-item data into a BI tool, (d) review last month's invoice.

## Section 5: Technical Support

**Updated:** AWS replaced its support plans. The module slides list Basic, Developer, Business, and Enterprise. The current plans, and the ones the exam uses, are **Basic, Business Support+, Enterprise Support, and Unified Operations**. Developer, Business (classic), and Enterprise On-Ramp end January 1, 2027.

**\[A\] Hook:** Your online store goes down on Black Friday. How fast do you need a human expert, and how much would you pay for that speed?

### Key support resources

| Resource | What it does |
| --- | --- |
| **Technical Account Manager (TAM)** | Your designated primary \_\_\_\_\_\_\_\_ of contact; gives proactive guidance and architecture reviews |
| **AWS Trusted Advisor** | Checks your account against best practices to cut costs and improve performance, security, and fault \_\_\_\_\_\_\_\_ |
| **AWS Health Dashboard** | Personalized view of AWS service health and alerts when your resources are \_\_\_\_\_\_\_\_ (**Updated:** formerly Personal Health Dashboard) |
| **Billing and account help** | \[PLACEHOLDER: confirm how Support Concierge maps to the 2026 plans\] |

### The four support plans

| Plan | Best for | Starting price | Key features |
| --- | --- | --- | --- |
| **Basic** | Everyone (included) | Free | 24/7 customer service, documentation, forums, core Trusted Advisor checks, AWS Health Dashboard. **No technical support cases.** |
| **Business Support+** | \_\_\_\_\_\_\_\_ workloads | $29/month | 24/7 AI-assisted troubleshooting; human experts on critical cases in under \_\_\_\_\_\_\_\_ minutes |
| **Enterprise Support** | Business-critical workloads | $5,000/month | Designated \_\_\_\_\_\_\_\_; under 15-minute critical response; Well-Architected reviews |
| **Unified Operations** | \_\_\_\_\_\_\_\_-critical workloads | \[PLACEHOLDER: pricing\] | Global designated team; 24/7 monitoring; \_\_\_\_\_\_\_\_-minute critical response |

**Exam tip:** Each higher plan includes everything in the plan below it.

### Case severity and response times

| Severity | What it means | Business Support+ | Enterprise | Unified Operations |
| --- | --- | --- | --- | --- |
| General guidance | General question or feature request | < 24 hours | < 24 hours | < 24 hours |
| System impaired | Non-critical functions behaving abnormally | < \_\_\_\_\_\_\_\_ hours | < 12 hours | < 12 hours |
| Production system impaired | Important functions impaired or degraded | < 4 hours | < \_\_\_\_\_\_\_\_ hours | < 4 hours |
| Production system down | Business significantly impacted | < 1 hour | < 1 hour | < 1 hour |
| Business-critical system down | Business at risk; critical functions unavailable | < \_\_\_\_\_\_\_\_ minutes | < 15 minutes | 5 minutes |

**\[R\] Why it matters:** Picking a support plan is a risk-versus-cost decision. What does one hour of downtime cost the business compared with the plan's monthly price?

**\[C\] Check yourself**

1. Which plan is the lowest that lets you open technical support cases?
2. Which plans include a designated TAM?
3. What is the critical response time for Enterprise Support?

**\[S\] Apply it:** Recommend a plan for each: (a) a student learning AWS, (b) a small business running its online store, (c) a bank running mission-critical payment systems.

Sources: [AWS Support plans](https://aws.amazon.com/premiumsupport/plans/) · [AWS Support response times](https://docs.aws.amazon.com/awssupport/latest/user/case-management.html) · [AWS Support plan announcement](https://aws.amazon.com/blogs/aws/new-and-enhanced-aws-support-plans-add-ai-capabilities-to-expert-guidance)

## Beyond the module: exam topics to add

The exam tests these Domain 4 topics, but Module 2 does not cover them. Each needs content.

| Exam task | Topic | Status |
| --- | --- | --- |
| 4.1 | Compute purchase options: On-Demand, Spot Instances, Savings Plans, Dedicated Hosts, Dedicated Instances, Capacity Reservations | \[PLACEHOLDER: guided notes + comparison table\] |
| 4.1 | Reserved Instance flexibility and RI behavior in AWS Organizations | \[PLACEHOLDER\] |
| 4.1 | Storage options and tiers (for example, S3 storage classes) | \[PLACEHOLDER\] |
| 4.2 | Cost allocation tags (AWS-generated vs user-defined) and their link to the Cost and Usage Report | \[PLACEHOLDER\] |
| 4.3 | AWS technical resources: whitepapers, re:Post, Knowledge Center, Prescriptive Guidance | \[PLACEHOLDER\] |
| 4.3 | AWS Trust and Safety team (reporting abuse) | \[PLACEHOLDER\] |
| 4.3 | AWS Partner Network, AWS Marketplace, ISVs, system integrators, partner benefits | \[PLACEHOLDER\] |
| 4.3 | AWS Professional Services and solutions architects | \[PLACEHOLDER\] |
| 4.3 | AWS Health API | \[PLACEHOLDER\] |

## Vocabulary and build-your-own flashcards

Make your own flashcards. Writing the card yourself is active learning; it builds memory better than reading someone else's.

### How to build a strong flashcard

1. **Front:** the term, or a scenario question ("A team needs an email alert at $500 spend. Which tool?")
2. **Back:** a definition **in your own words**, in one sentence
3. **Add an example:** a business situation where the term applies
4. **Add a contrast:** how it differs from a similar term (Cost Explorer vs Budgets)
5. **Test yourself:** sort cards into "know it" and "still learning"; review "still learning" daily

### Terms to make cards for

| Term | My definition (own words) | Business example |
| --- | --- | --- |
| Capital expense (capex) vs operating expense (opex) |  |  |
| Total Cost of Ownership (TCO) |  |  |
| Return on Investment (ROI) |  |  |
| Hard benefit vs soft benefit |  |  |
| Reserved Instance (RI) |  |  |
| Savings Plan |  |  |
| Tiered pricing |  |  |
| Consolidated billing |  |  |
| AWS Organizations / root |  |  |
| Organizational unit (OU) |  |  |
| Service control policy (SCP) |  |  |
| Availability Zone (AZ) |  |  |
| Spend Summary |  |  |
| Month-to-Date Spend by Service |  |  |
| AWS Cost Explorer |  |  |
| AWS Budgets |  |  |
| AWS Cost and Usage Report (CUR) |  |  |
| Cost allocation tag |  |  |
| Technical Account Manager (TAM) |  |  |
| AWS Trusted Advisor |  |  |
| AWS Health Dashboard |  |  |

## Instructor key

Remove this section before sharing with students.

### Answers to blanks, in order

- **Section 1:** compute, second, type; storage, GB; data transfer, free, charged. Use; capex; on demand. Reserve; 72. More; tiered; less. Grows; scale. AURI: all, largest; NURI: none, smallest. High; new; consolidated. Bill; pricing; account.
- **Section 2:** company (owner), provider; capex, used; time-consuming; fixed. Estimate; AWS; case. Software; facilities; administer. Power; storage. Estimate; reduce; before; groups. Capex; productivity; satisfaction; global. Narrow; saving; more.
- **Section 3:** free; organization; billing; security. Access; services; creation; billing. Top; container; leaves; services. Upside-down; down; one, one. IAM, groups; OU; root. Console; CLI; SDKs; API.
- **Section 4:** pay; usage; budget; group. Date; expenses; forecast; costs. Service; usage, 13, 18; alerts, email; detailed, S3.
- **Section 5:** point; tolerance; impacted. Production, 30; TAM; mission, 5. 12; 4; 30.

### Talking point notes

| Talking point | Suggested answer |
| --- | --- |
| Capex of a data center | Servers, buildings, cooling, power systems, networking gear, software licenses |
| Who is the "customer"? | The organization buying AWS services, not that organization's end users |
| Do IT jobs disappear? | Mostly they shift: from maintaining hardware to cloud architecture, security, and cost management |
| Why SCPs restrict the root user | SCPs cap the whole account, so no one in it can exceed the guardrail. They don't apply to the management account. |
| Why AZ or linked-account metrics matter | They show which team or location is spending, enabling chargeback and spotting waste |
| Walmart effect | Huge scale lowers unit costs, and AWS passes some savings on as lower prices |

### Open placeholders

- [ ] Three vs four ways to pay (Section 1)
- [ ] Lyft case study (Section 1)
- [ ] Full direct/indirect cost list for the sorting activity (Section 2)
- [ ] Pricing Calculator scenario (Section 2)
- [ ] Soft-benefit case studies (Section 2)
- [ ] Organizations hierarchy scenario and diagram (Section 3)
- [ ] Support Concierge mapping to 2026 plans (Section 5)
- [ ] Unified Operations pricing (Section 5)
- [ ] Exam-guide gap topics (Beyond the module)

### Sources

- [Amazon EC2 Reserved Instances pricing](https://aws.amazon.com/ec2/pricing/reserved-instances/pricing/)
- [AWS Cost Explorer documentation](https://docs.aws.amazon.com/console/billing/costexplorer)
- [AWS Support plans](https://aws.amazon.com/premiumsupport/plans/)
