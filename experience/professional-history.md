# Professional History

This file contains a comprehensive record of professional experience. Include more detail here than would appear on any single CV - Claude will select and tailor content for specific applications.

---

## Work Experience

### Dovetail
**Role:** Senior Manager, Data (+ Technical Product Manager from Nov 2025)
**Period:** November 2024 - Present
**Location:** Sydney, Australia (On-site)
**Industry:** B2B SaaS, AI/Customer Intelligence
**Reporting:** VP of Operations (Data role); CEO (Product role)

**Context & Scope:**
Dovetail is a Series A B2B SaaS company building an AI-native platform for customer intelligence. Joined to lead a struggling 3-person data team. Role expanded in November 2025 to include Technical Product Manager responsibilities for the data backend of Dovetail's core product (reporting to CEO). Currently 80% product, 20% data leadership. Team size reduced to 1.5 FTE (1 person + half of me) due to company downsizing, but maintained service levels through efficiency gains.

**Key Responsibilities:**
- Rebuilt entire data platform infrastructure from scratch
- Led and transformed data team culture and effectiveness
- Established metrics definitions and data governance
- (From Nov 2025) Technical PM for data ingestion and AI analysis pipelines powering Chat, Agents, Search, AI Docs, Dashboards, MPC Server
- (Current) Leading product strategy/discovery project defining Dovetail's future AI strategy with CEO and lead user researcher

**Major Achievements:**

1. **Data Platform Rebuild - 70% Cost Savings**
   - **The Problem:** Inherited legacy infrastructure set up by engineers (not data people). Postgres used as data warehouse. Self-hosted dbt core and Metabase. Data code entangled in main application monorepo causing CI failures and slow velocity. Heavy AWS security restrictions making basic operations difficult. Expensive homegrown AWS Glue replication pipeline. Poorly written dbt pipeline with no structure (no staging/intermediate/marts separation), inconsistent naming, duplicate logic.
   - **The Solution (5-step phased rebuild):**
     1. Created separate codebase for data platform → improved velocity and tooling (dbt power user in VS Code/Cursor)
     2. Migrated self-hosted dbt core → dbt Cloud → vastly improved observability, CI, environment management
     3. Complete dbt pipeline rewrite (done entirely by me) → 40% reduction in model count, clean pipeline structure, consistent conventions, net new semantic layer implementation
     4. Migrated Postgres → Snowflake → major performance improvements + cost savings + simplified replication (S3 direct import vs Glue pipeline) + enabled dbt semantic layer
     5. Migrated Metabase → Hex → modern BI experience with natural language analytics and agents
   - **Impact:** 70% cost reduction (Snowflake + simplified replication cheaper than self-hosted Postgres + Glue). Team shifted from primarily reactive to primarily proactive work.

2. **Team Transformation**
   - **The Problem:** Team struggled with leadership and direction, having reported to different people across ops/marketing/engineering over time. Created "us vs them" mentality, cynicism, feeling neglected. Team cared about quality but felt company didn't value them. Low company loyalty. One negative influencer causing cultural issues (also underperforming).
   - **The Solution:** Created basic structure (quarterly goals, clear ownership, aspirational long-term vision). Shifted culture toward company-first mindset and "skin in the game" (partially successful). Enabled team with best tools (modern data stack + AI tools like Cursor, Claude Code). Underperformer left before PIP (saw it coming).
   - **Impact:** Transformed struggling team into high-performing team within 1 year. Team reduced from 3 → 1.5 FTE due to company struggles but maintained effectiveness through efficiency gains.

3. **Data Culture & Metrics Consistency**
   - **The Problem:** Conflicting metric definitions across org (multiple definitions of MQL, revenue - different in Salesforce, data warehouse, Finance). Low trust in data generally.
   - **The Solution:** Created central metrics catalogue in Notion (pragmatic "analog" approach). Catalogued all important business metrics with links to canonical queries in BI tool. Established principle: "Data team doesn't define metrics - stakeholders do. Our role is to align everyone on ONE precise definition and implement it correctly." High bar for implementation correctness. Later reimplemented as semantic layer in dbt (after Snowflake migration enabled this).
   - **Impact:** Metrics catalogue became single source of truth. Daily questions in Slack redirected to catalogue. Definitions became common knowledge. Trust in data improved significantly across company. Enabled leadership to make better-informed decisions including a major business restructuring.
   - **The Business Restructuring Story:** Late 2024, company made large GTM investment in US (SF hires, significant marketing budget) aiming for Series B. Investment didn't work (product already on downward trajectory due to competitive pressure from horizontal AI tools), but this wasn't obvious because Marketing/Sales had their own narrative and data from Hubspot/SFDC, while tracking/definitions were poor. Finance saw concerning cash numbers. Data team + FP&A analyst investigated: tracked leads across systems, built custom attribution logic (instead of relying on Hubspot/SFDC), conducted first proper evaluation of GTM efficiency, checked numbers from multiple angles (knowing results would upset people). Conclusion: continuing marketing investment was bad idea. This analysis contributed to CEO's decision shortly after to restructure for profitability - recognizing we can't grow through marketing with current product and need time to innovate and re-establish PMF. Most of marketing was laid off.

4. **Product Transition**
   - **Context:** In small companies (<100 people), impactful data work is limited - data isn't critical path until Series B+. Post-layoffs needed to expand scope to justify role.
   - **Action:** Negotiated with CEO to transition to product side, moved to report directly to CEO. Became Technical PM for data platform team building product backend.
   - **Current Focus (80% of time):** Leading product strategy/discovery project with CEO and lead user researcher to define Dovetail's future AI strategy - recognizing need for radical adjustments and identifying strategic bets.
   - **Note:** No customer-facing features shipped yet (still early in PM role, focus has been on strategy work).

**Technical Environment / Tools Used:**
Snowflake, dbt (Cloud), Fivetran, Census, Metabase (initial), Hex (current), Postgres, AWS (initial), S3

**Skills Developed/Applied:**
- Technical: Data platform architecture, dbt (deep expertise), modern data stack, cloud data warehousing, semantic layer design, cost optimization
- Leadership: Team transformation, culture change, stakeholder alignment, change management
- Product: Product management, product strategy, AI strategy, customer-facing technical work
- Soft skills: Pragmatism, phased execution, navigating politics, creating clarity from chaos

**Notable Projects:**
1. **Complete Data Platform Rebuild:** 5-phase migration from legacy self-hosted stack to modern cloud architecture. Personally rewrote entire dbt pipeline. 70% cost savings, major velocity improvement.
2. **Metrics Catalogue & Data Governance:** Pragmatic Notion-based solution that resolved org-wide metric conflicts and built data trust.
3. **AI Product Strategy (Current):** Discovery project defining future product direction in AI era, working directly with CEO.

**Challenges Overcome:**
- Technical debt and entanglement: Created clean separation and modern architecture
- Cultural resistance and cynicism: Partially successful at shifting to company-first mindset
- Limited resources post-layoffs: Maintained effectiveness with 50% team reduction through automation and efficiency
- Scope creep in small company: Proactively expanded into product to increase impact

**Why This Experience Matters:**
Demonstrates ability to execute turnarounds (technical and cultural), operate at leadership level with CEO, balance technical depth with strategic thinking, and adapt to changing circumstances. Shows transition from pure data leadership to product-minded technical leadership.

**Contact Reference:**
Sascha Kerbert (VP of Operations) - sascha@dovetail.com

---

### Sequence
**Role:** Product Manager – Data, Analytics and Integrations
**Period:** February 2024 - November 2024 (9 months)
**Location:** Auckland, New Zealand (Remote)
**Industry:** B2B SaaS, Fintech (Billing Infrastructure)
**Reporting:** CEO

**Context & Scope:**
a16z-backed, early-stage startup building modern billing infrastructure for sales-led businesses. Multi-disciplinary technical lead across product, data, and engineering. Product areas included: embedded analytics, integrations (especially Salesforce), AI-assisted workflows, revenue recognition, usage-based pricing, and core data platform. Managed 0-2 reports (data team downsized as company took longer to find market traction). Role combined deep technical product work with customer-facing technical expertise.

**Key Responsibilities:**
- Technical PM for complex product areas: revenue recognition, CRM integrations, usage-based pricing infrastructure
- Domain expert for features with math/data complexity
- Customer-facing technical expert for complex implementations
- Scoped features down to data models and algorithms, worked directly with engineers
- AI strategy subject matter expert for leadership and investors
- (No direct code writing - PM role)

**Major Achievements:**

1. **Unlocked 3 Trajectory-Changing Deals Through Technical Expertise**
   - **incident.io (most notable):** Worked directly with their data team and head of finance on complex technical requirements. Now Sequence's largest customer (contract grew by 1 order of magnitude since signing).
     - *Reporting Requirements:* They had custom ARR pipeline built off Fivetran Stripe export. I had built Sequence's data export using Prequel (3rd party data transfer provider enabling customers to sync directly to their DWH without Fivetran). Worked through how ARR reporting would work off Sequence data, covering corner cases like mid-cycle seat changes. Convinced them Sequence data would be easier than Stripe data.
     - *Revenue Recognition Requirements:* Their revrec use-case was sophisticated. Sequence revrec product was in early development (I was PM). Laid out realistic staged roadmap (3-6 months) for what we could support. They signed and became our largest customer at the time.
   - Role across all deals: Drove clarity on technical requirements and provided hands-on implementation support

2. **AI Strategy Leadership**
   - Worked with leadership team and investors to adjust company strategy for the AI wave
   - Acted as subject matter expert on model capabilities
   - Evangelized AI tools internally across company
   - Helped refine early AI concepts (e.g., automatic parsing of contract PDFs into structured billing schedules - Sequence's core object)

**Products/Features Shipped:**

1. **Usage-Based Pricing Functionality**
   - Usage events and metrics infrastructure
   - Usage-based pricing models
   - Focused on technical design: data structures, storage infrastructure, algorithms
   - Also contributed to customer-facing functionality

2. **Salesforce Integration** (2-way sync)
   - Designed entire integration functionality
   - Worked with external agency to build Sequence Salesforce App
   - Designed data model for all custom objects
   - Created workflow templates in Salesforce Flow for common automation patterns between SFDC and Sequence

3. **Revenue Recognition Module**
   - Fully specced one of the largest and most complex parts of Sequence platform
   - Shipped after I left, but I did foundational work:
     - Initial research to learn about revenue recognition
     - Interviewed accountants to understand how revrec works
     - Created technical design including data models and algorithms
     - Worked with design on initial Figma mockups
     - Validated with design partners

**Technical Environment / Tools Used:**
GCP, Python, dbt, BigQuery, Postgres, Metabase, Salesforce, Prequel (data transfer platform)

**Skills Developed/Applied:**
- Product: Technical product management, complex B2B product design, customer-facing technical work
- Technical: Billing systems, revenue recognition, usage-based pricing, data integrations, data modeling
- Domain: Fintech/billing domain expertise, accounting principles, CRM systems (Salesforce)
- Strategic: AI strategy, investor engagement
- Soft skills: Customer engagement, technical communication, cross-functional collaboration

**Challenges Overcome:**
- Navigating complex enterprise sales cycles with sophisticated technical requirements
- Building credibility with technically advanced customers (incident.io's data and finance teams)
- Operating in early-stage environment with long traction timelines
- Balancing multiple complex product areas simultaneously

**Why This Experience Matters:**
Demonstrates ability to operate as technical product leader in early-stage startup, combine deep technical expertise with customer-facing work, unlock revenue through technical credibility, and contribute to strategic direction (AI strategy). Shows versatility across multiple complex product domains.

**Contact Reference:**
Riya Grover (CEO) - riya.grover@sequencehq.com

---

### Sequence
**Role:** Director of Data Engineering
**Period:** November 2021 - February 2024 (2 years 4 months)
**Location:** Auckland, New Zealand (Remote)
**Industry:** B2B SaaS, Fintech (Billing Infrastructure)
**Reporting:** CEO (mostly); briefly CTO (who left early on)

**Context & Scope:**
Early hire (company was ~5 people when I joined), responsible for building out data function spanning product analytics, customer-facing insights, and AI-driven applications. Set up data stack from scratch, designed architecture, built core data pipelines. Title was "Director" but company was pre-revenue when I joined. Initially hired 2-person data team (data engineer + data scientist) which was "comically overkill" - result of CTO applying Series A/B playbook to pre-revenue stage. Quickly rightsized to just data engineer, then eventually to zero as company took longer to find traction. Member of 5-person leadership team (CEO, head of product, head of sales, VP eng, myself as data/generalist).

**Key Responsibilities:**
- Built entire data platform from scratch (event-driven architecture, data contracts, automated pipeline generation)
- Developed customer-facing data features (exports, embedded analytics, reporting templates)
- Solution architect role: bridge between customer requirements and engineering team
- Heavily involved in hiring across company
- Leadership team member involved in all aspects of company building: hiring strategy, GTM, culture, high standards

**Major Achievements:**

1. **Built Sophisticated Data Platform from Scratch**
   - **Architecture:** Custom event-driven architecture replicating data from product backend to BigQuery. Universal PubSub events framework handling all product events including transient, non-CRUD events (not just CDC). Though somewhat over-engineered for stage (CDC + Segment would have sufficed), provided valuable learning about data contracts at scale.
   - **Data Contracts:** Implemented from scratch. All event schemas kept in separate catalogue as protobuf. Engineers publish new protobuf → data team reviews → make downstream changes → merge. Designed for resilience and correctness of critical dashboards with high confidence. Trending pattern at the time in larger orgs; gained firsthand understanding of pros/cons.
   - **dbt Infrastructure:** Built extensive dbt logic personally. Created automation to code-gen SQL organizing events into table replicas based on central schema catalogue. Powered both internal and customer-facing features.
   - **Outputs:** Enabled internal reporting (revenue/product analytics) and customer-facing features (data exports, embedded analytics).

2. **Customer-Facing Data Features**
   - **Embedded Analytics:** Embedded Metabase as in-product dashboard for basic usage analytics and billing reports. Pragmatic zero-engineering-effort solution for tablestakes feature that unblocked customer deals. Eventually replaced with native Sequence dashboard as product matured.
   - **Data Exports:** Built using Prequel, enabling customers to do their own revenue reporting off Sequence data (see incident.io example in PM role).
   - **Google Sheets Templates:** Created integration allowing customers to auto-populate spreadsheets with live Sequence data. Built templates for common use-cases: ARR reporting, usage analytics, sales commission calculations. Key insight: finance users already lived in spreadsheets; this gave them quick reporting setup while retaining full control (could modify/extend their private copy). Eventually replaced with partnership with Equals (spreadsheet-like product specializing in revenue reporting templates), but useful temporary solution to unblock deals.

3. **Leadership Team Contributions**
   - **Hiring Strategy Evolution:** Company raised large seed round (>$20M), creating pressure to hire quickly. Initially hired too many experienced leadership roles they couldn't leverage (product didn't exist yet) → had to let go. Eventually clicked with young, exceptionally talented, hungry people in product and sales. **Key lesson learned: Early stage = hire for raw potential, hunger, startup fit over experience and credentials.**
   - **Personal Hiring Involvement:** Always heavily involved in hiring across company.
   - **Solution Architect Role:** Regularly pulled into customer conversations as bridge between customer requirements and engineering team (see incident.io example in PM role).
   - **High-Performance Culture:** Leadership team of 5 became close-knit, holding each other and whole team to high standards. Recognized excellence and quickly addressed underperformance (must do both). After false starts with hiring/firing, became really good at it. Ended up with stellar team.

4. **AI-Driven Features**
   - Contributed to early exploration of AI-driven contract parsing feature (parsing contract PDFs into structured billing schedules)
   - Role: grounded discussion in existing model capabilities, offered perspective on future changes
   - Feature later built and now live (shipped after I left)

**Transition to PM Role (Feb 2024):**
Responsibilities changed marginally - mostly putting structure around what I was already doing (customer-facing technical work, product scoping, solution architecture). Formal recognition of evolved role.

**Technical Environment / Tools Used:**
GCP, Python, dbt, BigQuery, Postgres, Metabase, PubSub, Protobuf, Prequel, Google Sheets integration

**Skills Developed/Applied:**
- Technical: Event-driven architecture, data contracts, protobuf, code generation, dbt deep expertise, customer-facing data products
- Product: Building 0-to-1 features, pragmatic MVP solutions, understanding customer needs (finance/revenue reporting)
- Leadership: Hiring strategy, culture building, high standards, solution architecture, cross-functional collaboration
- Strategic: Early-stage company building, resource allocation, knowing when "good enough" beats perfect

**Challenges Overcome:**
- Building sophisticated infrastructure while recognizing some was overkill for stage (learning experience)
- Team sizing mistakes (over-hiring) → rightsizing over time
- Finding right balance between internal data needs and customer-facing features
- Operating in pre-revenue, high-uncertainty environment

**Why This Experience Matters:**
Demonstrates ability to build technical systems from scratch, operate as founding team member, contribute beyond functional area (hiring, culture, strategy), balance technical sophistication with pragmatism, and evolve role based on business needs. Shows early-stage startup building experience and versatility.

**Contact Reference:**
Matt Collinge (CTO) - matt.collinge@gmail.com

---

### Improbable
**Role:** Engineering Manager – Research Science
**Period:** February 2020 - April 2021 (1 year 3 months)
**Location:** London, UK (Remote during COVID)
**Industry:** Enterprise Technology, Simulation, Government/Defense
**Reporting:** [Senior leadership in government/defense org]

**Context & Scope:**
First-time people manager leading team of 6 Research Scientists. Improbable was Series A startup that raised ~$500M from SoftBank for large-scale virtual worlds/gaming infrastructure. Company spun up separate org focused on non-gaming use-cases (government/private sector): logistics simulations, military training, digital twins. Operated like consultancy (think Palantir). After trying various enterprise/government sectors, org made strategic decision to focus exclusively on national security & defense to shift from discovery/R&D to revenue-generating. My mandate: transition research team from pure academic work (aimed at reputation/publishing) to product roadmap and customer problem alignment. Took role when previous manager stepped out for personal reasons.

**Why I Was Selected:**
Not an expert in team's research topics (agent-based modelling, probabilistic programming, black-box optimization, research-level ML), but had ground-level customer experience, understood product space, and had academic background myself. Well-positioned for mandate despite lacking people management experience.

**Team Challenge (Most Difficult People Management to Date):**
Mix of highly talented junior researchers: very academically focused, highly opinionated, uninterested in "practicalities" like delivering customer outcomes. One particularly difficult team member: somewhat senior engineer with research background, openly autistic with special contract clauses, exhibited disruptive behaviors (sometimes rude to others, partly justified by being on spectrum), underperformer, felt underappreciated, threatened discrimination grievances. He insisted on promotion based on seniority; I couldn't justify from performance perspective. Made relationship difficult but I stand by decision. This was a lot to handle as new manager - didn't do great job in retrospect but learned tremendously. **Key lesson: Should have been more upfront and candid about sharp turn in team goals, asked them to decide if it was for them. Wasn't experienced enough - cared too much about being liked.**

**Key Responsibilities:**
- Led transition from academically-focused to product-first, customer-centric team
- Defined research strategy and connected Research to Product Development
- Implemented processes bridging research and applied work
- Led COVID-19 government response project (country-scale pandemic simulations)
- Managed publication strategy and team performance

**Major Achievements:**

1. **Defined Impact Framework for Research Team**
   - **The Problem:** Team had very little structure/direction, acted as pure research group working on whatever they wanted. Zero impact by business measures - work had maybe some reputational value but targeted academic circles, not industry or customers.
   - **The Solution:** Drove clarity on what "impact" meant: (1) Reputation in eyes of customers (to win contracts), (2) Impacting product roadmap (designing algorithms for core platform), (3) Impacting customer projects (solving research problems for customer outcomes).
   - **Research Strategy - 2 Focus Areas:** (a) Computational methods for scaling simulations (GPU acceleration for social science models - fairly new area), (b) Calibration on non-differentiable models (agent-based models). Both had direct product relevance.
   - **The Process:** (1) Write plausible story of how solving research problem applies to product + customer value, (2) Write research proposal, get approval (lightweight review with leadership), (3) Solve problem at research level, publish at industry conference, (4) **Short secondment in product/customer project team to implement solution** (most important but most unpopular part).
   - **Impact of Secondments:** By spending time on applied side, researchers gained invaluable customer context, developed empathy, influenced further research. Changed team mindset over time.

2. **COVID-19 Government Response - 10,000x Model Speedup**
   - **Context:** UK government reached out to tech companies for pandemic help. Royal Society stood up RAMP (Rapid Assistance in Modelling the Pandemic) coordinating efforts across academia and private sector. Epidemiological models (e.g., Prof. Ferguson) in news being used to inform policy - needed replication.
   - **The Project:** RAMP project with academics (pre-existing relationships) linking domain-specific models (population synthesis + urban flow + virus transmission) to build detailed pandemic simulation for large region of England.
   - **Our Role - Make Model Run Fast:** Existing model was patchwork of R/Python scripts by academics (SWE mess), took hours to simulate few months. **Key insight: Model performance (ability to run efficiently many times) as important or more important than model accuracy.**
   - **Solution:** Leveraged team's expertise in high-performance programming from gaming world. Entirely rewrote model code to run on GPUs (plus many code-level optimizations). **Achieved 10,000x speedup.**
   - **Impact:** News coverage, couple published papers, 2 team members received Royal Society award for this work. Unfortunately never understood if/how model was used by government to inform policy.

3. **Publication Strategy Shift**
   - Published 6 research papers during tenure
   - Shifted target from pure academic venues (NeurIPS, ICML) to industry conferences
   - Industry conferences easier to publish in while maintaining research-product alignment
   - Better balance between research output and product-first mandate

**Transition to Applied Science Role (Jan 2021):**
When opportunity came up to return to Applied side as manager, I took it. Reasons: slightly burned out by difficult people management, relationship with autistic individual was compromised, company hired senior leader with right credentials to lead Research (natural succession), better aligned with my technical skillset. Lateral move (not promotion) but ended up managing larger team (up to 15 reports).

**Technical Environment / Tools Used:**
Python, Julia, PyTorch, Numba, R, GPU computing, agent-based modeling, probabilistic programming, high-performance computing

**Skills Developed/Applied:**
- Leadership: First-time people management, managing difficult personalities, performance management, cultural transformation
- Technical: Research strategy, high-performance computing, GPU acceleration, agent-based modeling, pandemic simulation
- Strategic: Connecting research to product, impact frameworks, publication strategy
- Soft skills: Navigating sensitive HR situations, stakeholder alignment, building empathy in teams, learning to be candid (lesson learned: don't care too much about being liked)

**Challenges Overcome:**
- First management role with difficult team dynamics
- Navigating performance issues with individual with protected status (autism)
- Shifting academic team culture toward customer focus (partial success)
- Balancing research output with product impact
- Managing during COVID-19 while contributing to pandemic response

**Why This Experience Matters:**
First people management experience with significant challenges. Demonstrates ability to drive cultural transformation, operate in high-stakes government work (COVID response), bridge research and product, and learn from difficult situations. The COVID work shows ability to deliver outsized impact under pressure.

**Contact Reference:**
Christoforos Anagnostopoulos (Principal Scientist) - canagnos@imperial.ac.uk

---

### Improbable
**Role:** Engineering Manager – Applied Science
**Period:** January 2021 - August 2021 (8 months)
**Location:** London, UK (Remote)
**Industry:** Enterprise Technology, Simulation, Government/Defense
**Reporting:** [Senior leadership in government/defense org]

**Context & Scope:**
Line-managed team of 15 Data Scientists and ML Engineers responsible for designing and implementing complex multi-domain simulations for government customers. Lateral move from Research Science management (looking for better fit with technical skillset and escape from difficult team dynamics). Role was almost entirely people-focused: gathering big picture and customer context for teams, resource allocation across projects, career management. Pretty far removed from technical work at this scale. Company growing quickly in government/defense space.

**Key Responsibilities:**
- Delivery of high-profile Ministry of Defence technology demonstrators
- Hiring strategy and execution (grew team by 30% in 8 months)
- Interview process design and career ladder framework
- Capacity planning and resource allocation across multiple concurrent projects with fast-shifting priorities
- Stakeholder management and keeping projects moving
- Career development for 15 reports

**Major Achievements:**

1. **Led Delivery of 3 High-Profile MoD Technology Demonstrators Leading to Multi-Year Contracts**
   - **Context on Technology Demonstrators:** Specific step in structured MoD tech purchasing process (takes multiple years to buy tech). TDs are usually 1-year projects proving viability of emerging tech. "High profile" = potentially leading to massive contracts.
   - **The Projects:** Two major TDs - one in virtual training, one in operational decision support.
   - **My Role (High-Level, Not Technical):** Understanding customer requirements, working with product and programme managers on prioritization and resource allocation, keeping projects moving, keeping stakeholders informed.
   - **Outcome:** All 3 TDs successful, leading to multi-year contracts with UK MoD.

2. **Hiring Excellence - Grew Team by 30% While Improving Quality**
   - **Context:** Company growing quickly, hiring was major focus.
   - **My Contribution - Role Definition:** Wrote job description, career ladder, and interview questions for Applied Science role. This was slightly unique role: similar to Data/ML Scientist but less focused on specific ML techniques, expanding into simulation, agent-based modelling, network science, graphical modelling - basically whatever made sense for customer project - with strong element of working closely with customers.
   - **Interview Process Design:** Selected for people who are (1) problem focused rather than solution focused, (2) can learn unfamiliar domains quickly, (3) motivated by practical outcomes for customers.
   - **Impact:** Hired ~4-5 people in 8 months. **Hiring and role clarity was one of my strongest contributions in this role.**

3. **Established Career Ladder Framework**
   - Improved performance review process by creating career ladder framework for Applied Science roles
   - Provided clarity on progression paths for unique role profile
   - Improved retention and motivation

4. **Managed Complex Capacity Planning**
   - **The Challenge:** Projects would drop at random times based on conversations between senior leadership and government officials. Opportunity always huge (they usually were). Suddenly need team of 5 people for 6 months.
   - **My Approach:** Managed allocation across multiple concurrent projects with fast-shifting priorities.
   - **Extreme Example:** Even went back to IC myself for one project while managing Research team - literally had no other option for staffing.

**Why Left After 8 Months:**
Personal reasons: wife is from New Zealand, had been planning to relocate for a while. Left Improbable without another job lined up - plan was relocate to NZ, take time off, then look for job there. By chance, connected to Riya (Sequence founder) through common friend (also Sequence investor). Decided to take Sequence job with agreement that working from NZ would be on the table.

**Technical Environment / Tools Used:**
Python, R, Luigi (workflow management), simulation platforms, agent-based modeling tools

**Skills Developed/Applied:**
- Leadership: Scaling management (15 reports), people-focused leadership, hiring strategy, career development
- Strategic: Capacity planning, resource allocation, stakeholder management
- Hiring: Job design, interview process design, role clarity, selecting for mindset over skills
- Operational: Navigating government procurement processes, managing fast-shifting priorities

**Challenges Overcome:**
- Scaling to 15 direct reports while maintaining quality
- Managing resource allocation across unpredictable project pipeline
- Hiring quickly without compromising quality
- Balancing multiple high-stakes government projects simultaneously

**Why This Experience Matters:**
Demonstrates ability to operate at scale (15 reports), design hiring processes, work with government customers on high-stakes projects, and deliver commercial outcomes (multi-year MoD contracts). Shows progression in management maturity from first-time manager (Research) to scaled people leader (Applied).

**Contact Reference:**
Angelico Fetta (Senior Engineering Manager) - linkedin.com/in/angelicofetta

---

### [Continue with next role - Individual Contributor roles...]

---

## Career Narrative Notes

**Overarching Themes:**
[What are the threads that connect your experiences? e.g., "building scalable systems", "data-driven decision making", "leading cross-functional teams"]

**Career Transitions:**
[Note any career pivots and the reasoning - useful for addressing in cover letters]

**What Motivates You:**
[Understanding this helps tailor applications to align with company values]

**Target Roles / Industries:**
[Keep track of what kinds of positions you're interested in]
