# Building Digital Resilience Through Vibe Coding: A Content Analysis of AI-Assisted Development for Sustainable Digital Transformation

---

**Abstract**

Digital transformation remains a strategic imperative for organizations worldwide, yet approximately 70% of initiatives fail, costing an estimated $2.3 trillion annually. Traditional software development is expensive ($434K–$2.3M per project), slow, and constrained by scarce technical talent. While low-code development platforms emerged as a partial solution—accelerating development 5–10x and enabling citizen developer participation—they introduced vendor lock-in, scalability constraints, and platform fragmentation. In February 2025, Andrej Karpathy coined the term "vibe coding" to describe a radically new AI-assisted programming paradigm in which developers describe desired functionality in natural language and accept AI-generated code, often without full comprehension of the output. Within one year, 87% of Fortune 500 companies adopted at least one vibe coding platform, and the term was named Collins Dictionary Word of the Year 2025. Despite this rapid adoption, no theoretically grounded academic study has investigated how vibe coding contributes to organizational digital transformation and resilience across business sectors. This paper addresses this gap through a directed content analysis of 97 sources spanning academic literature, industry reports, developer community discourse, and platform documentation. Using an integrated theoretical lens combining Dynamic Capabilities Theory, the Technology-Organization-Environment (TOE) framework, and Diffusion of Innovation (DOI) Theory, we systematically analyze vibe coding's role in enabling digital transformation and building—or undermining—organizational digital resilience. Our findings reveal a "resilience paradox": vibe coding simultaneously strengthens organizational resilience through accelerated sensing, seizing, and transforming capabilities while introducing novel fragilities including security vulnerabilities (present in 45% of AI-generated code), technical debt accumulation, and a "vulnerable developer" phenomenon affecting 63% of vibe coding practitioners. We extend Sanchis et al.'s (2020) low-code/manufacturing framework to the vibe coding era and broader business contexts, provide a comparative analysis of low-code versus vibe coding paradigms, and propose a governance framework for sustainable vibe coding adoption. The paper concludes with a forecasting analysis positioning vibe coding on the technology adoption lifecycle and identifying critical factors that will determine whether it achieves sustainable mainstream enterprise adoption or follows the trajectory of earlier automation paradigms such as CASE tools.

**Keywords:** vibe coding; digital transformation; digital resilience; AI-assisted development; low-code; dynamic capabilities; content analysis

---

## 1. Introduction

Enterprises operate in an environment of accelerating complexity and disruption. The increasing intensity of global competition, rapid technological change, and volatile market conditions demand that organizations build digital capabilities at unprecedented speed [1,2]. Digital transformation—the integration of digital technologies into all areas of business, fundamentally changing how organizations operate and deliver value—has become a strategic imperative rather than an option [3]. Yet the track record is sobering: approximately 70% of digital transformation initiatives fail to achieve their objectives [4], costing organizations an estimated $2.3 trillion annually in unrealized value [5]. A fundamental bottleneck lies in software development itself. Traditional development remains expensive, with project costs ranging from $434,000 for small and medium-sized enterprises to $2,322,000 for larger projects [6,7]. Development cycles measured in months or years are increasingly misaligned with the pace at which organizations must respond to market shifts and competitive threats.

The quest to democratize and accelerate software development is not new. In the late 1980s, Computer-Aided Software Engineering (CASE) tools promised to automate significant portions of the development lifecycle. The CASE market grew to $12.11 billion by 1995, yet 73.5% of companies never adopted these tools [8,9]. Unrealistic expectations, conceptual gaps between tool designers and users, high training costs, and the overestimation of productivity gains all contributed to CASE's failure to achieve mainstream adoption [10,11]. Two decades later, low-code development platforms (LCDPs) emerged as a more accessible alternative. Coined by Forrester Research in 2014 [12], "low-code" describes platforms that enable application development through visual drag-and-drop interfaces, pre-built modules, and minimal hand-coding. Sanchis et al. [1] demonstrated that low-code platforms can serve as enablers of digital transformation in manufacturing, offering rapidity (5–10x faster development), cost reduction, citizen developer involvement, and simplified maintenance. However, their analysis also revealed significant limitations: scalability constraints for enterprise-grade applications, fragmentation across vendors, restriction to software-only systems, and substantial vendor lock-in [1,13].

In February 2025, a new paradigm emerged that would fundamentally reshape this trajectory. Andrej Karpathy, co-founder of OpenAI and former Director of AI at Tesla, posted on X (formerly Twitter): "There's a new kind of coding I call 'vibe coding,' where you fully give in to the vibes, embrace exponentials, and forget that the code even exists" [14]. Karpathy described a practice of using large language models (LLMs) to generate entire codebases from natural language prompts, accepting the output largely without detailed review, and iterating through error messages by copying them back into the AI. Within twelve months of this coinage, vibe coding catalyzed a paradigm shift of remarkable velocity. The term was named Collins Dictionary Word of the Year 2025 [15]. Industry surveys reported that 92% of U.S. developers use AI coding tools daily, with 62% reporting productivity gains of 25% or more [16]. Gartner predicted that 60% of new code would be AI-generated by 2026 [17]. Perhaps most strikingly, 87% of Fortune 500 companies adopted at least one vibe coding platform, and 25% of Y Combinator's Winter 2025 cohort reported running codebases that were 95% AI-generated [18,19].

Despite this extraordinary adoption velocity, there is a significant gap in academic understanding. While substantial research exists on low-code platforms and digital transformation [1,20,21], AI coding tools and developer productivity [22,23], and organizational resilience frameworks [2,24], there is virtually no theoretically grounded academic research investigating how vibe coding contributes to digital transformation and organizational resilience across business sectors. Existing vibe coding research—primarily arXiv preprints and a grey literature review accepted at ICSE 2026 [25]—focuses overwhelmingly on individual developer productivity metrics and code quality, not on organizational-level resilience outcomes or cross-industry digital transformation impacts.

This paper addresses this gap through a directed content analysis [26] investigating how vibe coding enables digital transformation and builds digital resilience across business sectors. We extend Sanchis et al.'s [1] low-code/manufacturing framework to the vibe coding era and broader business contexts, providing the first theoretically grounded, cross-industry analysis of vibe coding's organizational impact. Our analysis is structured through an integrated theoretical lens combining Dynamic Capabilities Theory [27,28], the Technology-Organization-Environment (TOE) framework [29], and the Diffusion of Innovation (DOI) Theory [30], enabling us to examine not only what vibe coding enables but also how it diffuses across organizations and what organizational capabilities it enhances or diminishes.

Specifically, this study addresses three research questions:

**RQ1:** What is the current state of discourse on vibe coding as a paradigm for enabling digital transformation across business sectors?

**RQ2:** How does vibe coding contribute to (or hinder) organizational digital resilience compared to traditional low-code/no-code approaches?

**RQ3:** What are the enabling factors, barriers, and sustainability implications of vibe coding adoption for digital transformation?

By answering these questions, this paper makes three primary contributions. First, it provides the first systematic, multi-source content analysis of vibe coding's organizational-level impact, synthesizing fragmented discourse across academic, industry, practitioner, and platform documentation sources. Second, it introduces the concept of the "resilience paradox"—the finding that vibe coding simultaneously strengthens and weakens organizational digital resilience—and theorizes this tension through the lens of Dynamic Capabilities. Third, it offers practical governance frameworks and forecasting analysis relevant to organizational decision-makers navigating the vibe coding paradigm shift, positioning this work squarely within the anticipatory and futures-oriented tradition of *Technological Forecasting and Social Change*.

---

## 2. Background and Theoretical Framework

### 2.1 The Evolution of Software Development Automation

The automation of software development has followed a punctuated evolutionary trajectory, with each paradigm shift promising to democratize development, reduce costs, and accelerate delivery. Understanding this historical evolution is essential for contextualizing vibe coding's emergence and forecasting its trajectory.

#### 2.1.1 CASE Tools (1980s–1990s)

Computer-Aided Software Engineering (CASE) emerged in the late 1980s as the first systematic attempt to automate the software development lifecycle. CASE technology encompasses a collection of automated tools and methods that assist software engineering across its phases [31], including editing tools, programming tools, code generators, verification and validation tools, configuration management systems, and project management tools [32]. Fuggetta [33] classified CASE products into three categories: individual tools supporting specific tasks, workbenches integrating multiple tools for specific activities, and environments providing holistic toolkits supporting the entire software process.

The CASE market demonstrated significant commercial interest, generating revenues that grew to $12.11 billion by 1995 [1]. However, adoption rates were dramatically disappointing. Iivari [10] found that 73.5% of companies never adopted CASE tools, concluding that the productivity and quality benefits were "overrated" and that complexity was a "significant, negatively related predictor of CASE effectiveness." Lundell and Lings [34] identified that the conceptual gap between tool designers and end users was a primary barrier. Huff [35] demonstrated that training costs often exceeded the original tool purchase price. Orlikowski [36] found that benefits did not accrue homogeneously, leading to internal resistance. These failures offer critical lessons: technological sophistication alone does not guarantee adoption, and unrealistic expectations can doom even promising paradigms.

#### 2.1.2 Low-Code/No-Code Platforms (2014–Present)

The term "low-code" was first coined by Forrester Research in 2014 [12] to describe platforms that enable application development through visual interfaces, pre-built components, and minimal hand-coding. Unlike CASE tools, which primarily assisted professional developers, low-code platforms explicitly targeted a broader user base including "citizen developers"—business professionals without formal programming training [37]. Richardson and Rymer [38] identified low-code platforms as providing useful solutions for automating and accelerating application delivery.

Sanchis et al. [1] systematically documented the benefits of low-code platforms: (a) privacy—applications can be developed internally without outsourcing; (b) rapidity—Forrester surveys showed 5–10x acceleration in development speed [38]; (c) cost reduction—shorter development cycles directly reduce project costs; (d) complexity reduction—apps are configured rather than coded from scratch; (e) easy maintenance—minimal code means minimal maintenance burden; (f) involvement of business profiles—44% of low-code platform users are business users collaborating with IT [37]; and (g) minimization of unstable requirements—rapid iteration enables faster validation of ideas. The State of Application Development report [37] found that 66% of respondents cited "accelerate digital transformation" as their primary motivation for adopting low-code platforms.

However, significant limitations persist. Tisi et al. [13] identified three critical constraints: scalability (low-code platforms are primarily suited for small applications, not enterprise-grade systems), fragmentation (different vendors implement different paradigms with limited interoperability), and restriction to software-only systems (manufacturing and IoT use cases requiring hardware integration are poorly served). The same report [37] found that the primary reasons organizations avoid low-code platforms include lack of knowledge (45%), concerns about vendor lock-in (37%), doubts about application capabilities (32%), scalability concerns (30%), and security worries (25%). By 2025, the low-code market had grown substantially—Forrester projected total spending of $21.2 billion [39]—yet these fundamental limitations continued to constrain its role in enterprise digital transformation.

#### 2.1.3 Vibe Coding (2025–Present)

On February 2, 2025, Andrej Karpathy introduced "vibe coding" as a practice where developers describe desired functionality in natural language, allow LLMs to generate complete code, and "accept all" without necessarily comprehending every line of output [14]. Karpathy described iterating through error messages by copying them directly back into the AI and characterized the resulting code as often exceeding his own full comprehension. This description captured a practice that was already emerging among developers using tools like GitHub Copilot, Cursor, and Replit but had lacked a unifying label.

The defining characteristics of vibe coding, as synthesized from subsequent literature, include: (a) natural language as the primary development interface—developers express intent through conversational prompts rather than writing code directly [25,40]; (b) AI-generated code as the primary output—LLMs produce functional code in standard programming languages (Python, JavaScript, HTML/CSS, etc.) rather than platform-specific configurations [41]; (c) an "accept all" mentality—practitioners frequently accept generated code without comprehensive review [14,25]; (d) iterative error resolution through AI—when code fails, error messages are fed back to the LLM for correction rather than debugged manually [40]; and (e) code that may exceed developer comprehension—the generated codebase often surpasses what the practitioner could have written or fully understands [14,42].

The vibe coding ecosystem rapidly matured around several key platforms. Cursor, an AI-native code editor built on Visual Studio Code, provides deep LLM integration for code generation and editing. Replit offers a cloud-based IDE with AI-powered code generation and deployment. Claude Code, Anthropic's command-line tool, enables developers to interact with AI through natural language in terminal environments. GitHub Copilot, initially launched in 2021 as an autocomplete tool, evolved into a comprehensive AI coding assistant. Newer platforms including v0.dev (Vercel), Bolt (StackBlitz), and Lovable specifically target non-developers, enabling application creation through purely conversational interfaces [25,41].

Simon Willison [43] introduced an important distinction between "vibe coding" and what he termed "vibe engineering"—the practice of using AI coding tools while maintaining full accountability, conducting code reviews, writing tests, and ensuring comprehension of the output. This distinction highlights a spectrum of AI-assisted development practices, from fully autonomous AI code generation (vibe coding) to AI-augmented professional development (vibe engineering), with significant implications for code quality, security, and organizational resilience.

Current adoption statistics underscore the paradigm's momentum. A 2025 Stack Overflow survey found that 92% of U.S. developers use AI coding tools daily [16]. GitHub reported that 62% of developers using Copilot experienced productivity gains of 25% or more [22]. Gartner predicted that by 2028, 75% of enterprise software engineers would use AI coding assistants, up from fewer than 10% in early 2023 [17]. McKinsey's 2025 State of AI report indicated that 88% of organizations report regular AI use across functions [44]. Yet caution is warranted: BCG found that 60% of organizations generate no material value from their AI investments [45], suggesting that adoption does not automatically translate to organizational benefit.

### 2.2 Digital Transformation and Organizational Resilience

#### 2.2.1 Enterprise and Digital Resilience

Enterprise resilience has been defined as the capacity to prevent, anticipate, change, and adapt to changing environments [2]. Sanchis and Poler [2] operationalized this concept through a quantitative assessment framework that measures organizational capacity across these four dimensions. In the digital context, Heeks and Ospina [46] defined digital resilience as "the capabilities developed through digital technologies to absorb shocks, adapt, and transform in the face of adverse change." This conceptualization moves beyond mere survival to encompass three progressive stages: anticipation (detecting threats and opportunities early), coping (maintaining operations during disruption), and adaptation (learning and transforming in response to change) [46,47].

The relationship between digital transformation and resilience is increasingly well-documented. Browder [48] characterized digital transformation as "upgrading adaptation"—an investment that enhances an organization's capacity to respond to future disruptions. Li and Wang [49] demonstrated empirically that digital transformation positively influences enterprise resilience through enhanced information processing capabilities and organizational flexibility. Breidbach et al. [50] introduced the concept of "orchestrating digital resilience," emphasizing the active role of organizational decision-making in leveraging digital capabilities for resilience outcomes. McKinsey research indicates that agile organizations—those that have built rapid response capabilities—make decisions 50% faster than their peers [51], directly linking development speed to organizational resilience.

#### 2.2.2 Rapid Development Capability as a Resilience Enabler

A critical but under-theorized link exists between software development speed and organizational resilience. When organizations can build, test, and deploy digital solutions rapidly, they gain the ability to: (a) detect market opportunities and threats through rapid prototyping and MVP testing; (b) respond to disruptions by building digital solutions in days rather than months; and (c) continuously adapt their digital infrastructure as conditions change. This positions development capability—specifically, the speed and accessibility of software creation—as a direct enabler of digital resilience. Both low-code platforms and vibe coding dramatically compress development timelines, but through fundamentally different mechanisms: low-code through pre-built visual components and constrained platforms, vibe coding through AI-generated code from natural language prompts [1,25].

### 2.3 Theoretical Lens

This study employs an integrated multi-theory framework combining Dynamic Capabilities Theory, the TOE framework, and DOI Theory. This integration is necessary because no single theory adequately captures both the adoption dynamics and the organizational impact of vibe coding on digital resilience.

#### 2.3.1 Dynamic Capabilities Theory

Teece, Pisano, and Shuen [27] defined dynamic capabilities as "the firm's ability to integrate, build, and reconfigure internal and external competences to address rapidly changing environments." Warner and Wager [28] extended this framework to the digital transformation context, identifying nine digitally based microfoundations underpinning three core capability clusters:

- **Sensing:** The capacity to detect opportunities and threats. Vibe coding enhances sensing by enabling rapid prototyping (hours instead of months), allowing organizations to test market hypotheses at dramatically lower cost and higher speed. Organizations can build MVPs to validate assumptions about customer needs, competitive threats, or technological possibilities before committing significant resources [28,52].

- **Seizing:** The capacity to mobilize resources to capture value from opportunities. Vibe coding compresses time-to-market from months to days or hours, enabling organizations to capture value from opportunities before competitors. Reduced dependency on scarce technical talent further accelerates seizing by removing the hiring bottleneck that traditionally constrains digital initiative timelines [27,28].

- **Transforming:** The capacity to reconfigure organizational assets and structures. Vibe coding empowers citizen developers—non-technical staff who can now build functional applications through natural language—fundamentally reconfiguring the boundary between IT and business functions. This distributes digital capability building across the organization rather than concentrating it in a specialized IT function [28,53].

#### 2.3.2 Technology-Organization-Environment (TOE) Framework

Tornatzky and Fleischer's [29] TOE framework structures the analysis of technology adoption factors across three contexts:

- **Technology context:** LLM capability maturity and trajectory, tool accessibility and pricing models, code quality and security trade-offs, integration capabilities with existing development workflows and enterprise systems.

- **Organizational context:** Existing digital maturity as a prerequisite, organizational AI culture and readiness, management support and strategic alignment, developer skill levels and willingness to adopt, governance structures for AI-generated code.

- **Environmental context:** Competitive pressure to digitize (87% of Fortune 500 adopting), industry-specific regulatory requirements for code quality and security, talent market dynamics (persistent developer shortage driving AI adoption), technology vendor ecosystem evolution.

#### 2.3.3 Diffusion of Innovation (DOI) Theory

Rogers' [30] DOI theory identifies five innovation characteristics that influence adoption rates:

- **Relative advantage:** Vibe coding offers dramatic speed gains (60–80% faster prototyping) and substantial cost reduction, representing significant relative advantage over both traditional development and low-code platforms.

- **Compatibility:** Natural language interfaces are highly compatible with existing human communication patterns, but vibe coding practices (accepting code without review, code exceeding comprehension) are fundamentally incompatible with traditional software engineering practices emphasizing code understanding, review, and testing.

- **Complexity:** The perceived complexity of vibe coding is near-zero—the primary interface is natural language. This represents the most dramatic reduction in perceived development complexity in the history of software engineering.

- **Trialability:** Free and low-cost tools (Cursor free tier, Replit, Claude Code) enable low-barrier experimentation, facilitating trial adoption without significant organizational commitment.

- **Observability:** Results are highly observable—working prototypes can be demonstrated within hours, making the innovation's benefits immediately visible to organizational decision-makers.

Based on current adoption patterns, vibe coding appears to be transitioning from the "early adopters" to the "early majority" stage of Rogers' diffusion curve, a critical inflection point that will determine whether it achieves mainstream adoption or plateaus [30].

#### 2.3.4 Integrated Conceptual Model

Our integrated model posits that vibe coding adoption (driven by TOE and DOI factors) enhances organizational dynamic capabilities (sensing, seizing, transforming), which in turn produce digital resilience outcomes (anticipation, coping, adaptation). This relationship is moderated by industry sector, organizational size, existing digital maturity, and governance maturity. Critically, the model also identifies sustainability tensions that may undermine resilience outcomes: security vulnerabilities, technical debt accumulation, the "vulnerable developer" phenomenon, skill erosion, and environmental costs of LLM computation. Figure 1 presents this integrated conceptual model.

```
┌──────────────────────────┐     ┌────────────────────────────────┐     ┌──────────────────────────┐
│ VIBE CODING ADOPTION     │     │ ENHANCED DYNAMIC CAPABILITIES  │     │ DIGITAL RESILIENCE       │
│ (TOE + DOI Factors)      │ ──> │ (Sensing, Seizing, Transforming)│ ──> │ OUTCOMES                 │
│                          │     │                                │     │                          │
│ Technology:              │     │ Sensing:                       │     │ Anticipation:            │
│ - LLM maturity           │     │ - Rapid prototyping            │     │ - Early threat/opportunity│
│ - Tool accessibility     │     │ - Market hypothesis testing    │     │   detection via fast MVPs │
│ - Code quality trade-offs│     │                                │     │                          │
│                          │     │ Seizing:                       │     │ Coping:                  │
│ Organization:            │     │ - Compressed time-to-market    │     │ - Rapid digital response │
│ - Digital maturity       │     │ - Reduced development costs    │     │   to disruptions         │
│ - AI culture/readiness   │     │                                │     │                          │
│ - Governance structures  │     │ Transforming:                  │     │ Adaptation:              │
│                          │     │ - Citizen developer empowerment│     │ - Organizational learning│
│ Environment:             │     │ - Reconfigured org boundaries  │     │   and transformation     │
│ - Competitive pressure   │     │ - Distributed digital capability│    │                          │
│ - Regulatory context     │     │                                │     │                          │
│ - Talent market dynamics │     │                                │     │                          │
└──────────────────────────┘     └────────────────────────────────┘     └──────────────────────────┘
                                            │
                               ┌────────────────────────────┐
                               │ MODERATORS                  │
                               │ - Industry sector           │
                               │ - Organizational size       │
                               │ - Existing digital maturity │
                               │ - Governance maturity       │
                               └────────────────────────────┘

                      SUSTAINABILITY TENSIONS / RISKS:
                      - Security vulnerabilities (45% of AI code)
                      - Technical debt accumulation
                      - "Vulnerable developer" phenomenon
                      - Skill erosion in engineering teams
                      - LLM energy/environmental costs
```

**Figure 1.** Integrated conceptual model: Vibe coding adoption, dynamic capability enhancement, and digital resilience outcomes.

The justification for this multi-theory approach is threefold. First, TOE and DOI together provide complementary explanations for adoption variance—TOE captures contextual factors while DOI captures innovation-specific attributes. Second, Dynamic Capabilities Theory explains how adoption translates into organizational impact on resilience, bridging the gap between technology adoption and strategic outcomes. Third, the integration enables identification of tensions and paradoxes that single-theory approaches would miss, particularly the simultaneous enhancement and undermining of resilience capabilities.

---

## 3. Research Methodology

### 3.1 Research Design and Justification

This study employs directed content analysis following Hsieh and Shannon [26], supplemented by Mayring's [54] systematic procedures and Elo and Kyngäs's [55] preparation-organizing-reporting structure. Directed content analysis begins with existing theory or prior research as initial coding guidance—in our case, the integrated Dynamic Capabilities, TOE, and DOI framework—while remaining open to new categories that emerge inductively from the data [26]. This approach is particularly appropriate for our study for three reasons. First, vibe coding is an emerging phenomenon with fragmented discourse distributed across academic, industry, and practitioner sources; content analysis enables systematic synthesis and theory development from heterogeneous sources. Second, the directed approach allows us to leverage established theoretical frameworks while accommodating the novel dynamics specific to vibe coding. Third, the multi-source design enables triangulation that strengthens the validity of findings about a rapidly evolving technological paradigm.

### 3.2 Data Collection

#### 3.2.1 Search Strategy

Data collection employed a systematic multi-source triangulation strategy across four source types, as summarized in Table 1.

**Table 1.** Data source types, search strategies, and corpus distribution.

| Source Type | Scope | Search Strategy | Sources Retrieved | Sources Included |
|-------------|-------|-----------------|-------------------|------------------|
| Academic literature | Peer-reviewed papers on vibe coding, AI-assisted development, low-code + digital transformation + resilience | Scopus, Web of Science, IEEE Xplore, ACM Digital Library, AISeL; PRISMA 2020 protocol | 127 | 34 |
| Grey literature | Industry reports, whitepapers, enterprise case studies | Gartner, Forrester, McKinsey, BCG, Atos, HCLTech, Genpact; Garousi et al. [56] guidelines + AACODS quality checklist | 89 | 31 |
| Developer community discourse | Practitioner blogs, forum discussions, social media | Stack Overflow, GitHub Discussions, Reddit, X/Twitter, DEV Community, Medium; purposive + snowball sampling | 112 | 22 |
| Platform documentation & case studies | Official documentation, enterprise case studies | Cursor, Replit, Claude Code, GitHub Copilot, v0.dev, Bolt, Lovable + OutSystems, Mendix, Power Apps, ServiceNow | 38 | 10 |
| **Total** | | | **366** | **97** |

Search keywords were organized into four clusters: (a) primary terms: "vibe coding," "AI-assisted coding," "AI-assisted development," "LLM coding," "vibe engineering"; (b) combined with: "digital transformation," "digital resilience," "enterprise resilience," "organizational resilience," "citizen developer," "democratization of development"; (c) comparative terms: "low-code," "no-code," "CASE tools," "low-code development platform"; (d) temporal scope: February 2025 to February 2026 for vibe coding sources; 2014–2026 for low-code and digital transformation comparative sources.

#### 3.2.2 Inclusion and Exclusion Criteria

Table 2 presents the inclusion and exclusion criteria applied across all source types.

**Table 2.** Inclusion and exclusion criteria.

| Criteria | Include | Exclude |
|----------|---------|---------|
| Language | English | Non-English |
| Timeframe | Feb 2025 – Feb 2026 (vibe coding); 2014–2026 (low-code/DT) | Before 2014 (pre-low-code era) for comparative sources |
| Focus | Organizational/business impact of vibe coding or low-code on digital transformation/resilience | Purely technical benchmarks without organizational context |
| Quality | Peer-reviewed OR grey literature scoring ≥ 10/15 on AACODS | Marketing materials without substantive analysis; sources < 10/15 quality |
| Relevance | Discusses adoption, impact, benefits, barriers, or outcomes at organizational level | Focused solely on individual developer productivity metrics without organizational implications |

#### 3.2.3 Quality Assessment

Academic sources were assessed through the peer-review process as a baseline quality indicator. Grey literature was assessed using the AACODS checklist [57] (Authority, Accuracy, Coverage, Objectivity, Date, Significance), with a threshold of 10/15 for inclusion, following Garousi et al.'s [56] guidelines for including grey literature in software engineering systematic reviews. Developer community sources were evaluated for substantive analytical content, author credibility (verified expertise, organizational affiliation), and engagement metrics indicating community validation.

#### 3.2.4 Corpus Description

The final corpus comprises 97 sources: 34 academic papers (35.1%), 31 grey literature sources (32.0%), 22 developer community sources (22.7%), and 10 platform documentation and case study sources (10.3%). Geographically, sources originate from North America (48.5%), Europe (27.8%), Asia-Pacific (16.5%), and other regions (7.2%). By sector coverage, the corpus addresses technology/software development (78.4%), financial services (34.0%), healthcare (21.6%), manufacturing (19.6%), education (15.5%), retail/e-commerce (12.4%), and government/public sector (9.3%), with many sources addressing multiple sectors.

### 3.3 Data Analysis Procedure

#### 3.3.1 Hierarchical Coding Framework

Following the directed content analysis approach [26], we developed a hierarchical coding framework with deductive categories derived from our theoretical framework and inductive subcodes that emerged during analysis. Table 3 presents the coding framework.

**Table 3.** Hierarchical coding framework.

| Level 1: Meta-Category (Deductive) | Level 2: Sub-Categories (Deductive) |
|-------------------------------------|--------------------------------------|
| 1. Paradigm Characteristics & Evolution | Natural language interface; AI-generated code; acceptance without review; iterative error resolution; code exceeding comprehension |
| 2. Adoption Drivers | Speed/efficiency; cost reduction; accessibility/democratization; skills gap mitigation; competitive pressure; innovation velocity |
| 3. Adoption Barriers | Security vulnerabilities; technical debt; governance gaps; quality concerns; skill erosion; vendor/AI dependency; regulatory compliance |
| 4. Dynamic Capability Enhancement | Rapid prototyping (sensing); time-to-market compression (seizing); citizen developer empowerment (transforming); organizational boundary reconfiguration |
| 5. Digital Transformation Enablement | Cross-functional development; legacy modernization; process automation; customer-facing innovation; internal tool building |
| 6. Digital Resilience Outcomes | Operational continuity; adaptive capacity; innovation velocity; knowledge retention/loss; workforce resilience |
| 7. Sustainability Tensions & Trade-offs | Resource efficiency vs. LLM energy costs; democratization vs. quality erosion; speed vs. technical debt; agility vs. governance |

Level 3 inductive subcodes emerged during the open coding phase, particularly within the adoption barriers and sustainability tensions meta-categories, where novel dynamics specific to vibe coding (e.g., the "vulnerable developer" phenomenon, the "flow-debt trade-off") required new conceptual categories.

#### 3.3.2 Coding Process

The unit of analysis was the meaningful text segment at the paragraph or quote level. Analysis proceeded in three phases: (1) preparation—corpus compilation, quality assessment, and familiarization reading; (2) organizing—deductive coding using the a priori framework, followed by inductive coding for segments that did not fit existing categories; and (3) reporting—synthesis, frequency analysis, and thematic integration [55]. All coding was conducted using NVivo 14 qualitative analysis software.

### 3.4 Quality Assurance

**Intercoder reliability:** Two researchers independently coded 20% of the corpus (20 sources stratified across all four source types). Initial Krippendorff's Alpha was 0.74. Following discussion, refinement of coding definitions, and a second coding round, Alpha reached 0.83, exceeding the 0.80 threshold recommended by Krippendorff [58].

**Trustworthiness:** Following Lincoln and Guba [59], we addressed: credibility through triangulation across four data streams and member checking with three industry practitioners; transferability through thick description of context, methodology, and findings; dependability through a detailed audit trail documenting all analytical decisions; and confirmability through a reflexive journal maintained throughout the study.

**Pilot coding:** The coding framework was pilot-tested on 10% of the corpus (10 sources). This pilot resulted in the refinement of three sub-category definitions and the addition of two inductive subcodes before full coding commenced.

**Reflexivity:** Following Nicmanis [60], we acknowledge our positionality as researchers situated within the information systems discipline with prior research experience in digital transformation and technology adoption. This expertise informed our theoretical framing while potentially introducing confirmation bias toward viewing vibe coding through organizational capability lenses.

---

## 4. Findings

### 4.1 Descriptive Overview of the Corpus

The 97-source corpus reveals a discourse landscape dominated by practitioner and industry voices. Academic literature constitutes only 35.1% of the corpus, reflecting the recency of the phenomenon (the term was coined only 12 months before our data collection cutoff). Within the academic sources, the majority (73.5%) are preprints or conference papers rather than journal articles, underscoring the field's nascent stage. The most frequently coded meta-categories were Adoption Drivers (coded in 81.4% of sources), Paradigm Characteristics (76.3%), and Adoption Barriers (74.2%), indicating that the discourse is heavily oriented toward understanding what vibe coding is and whether organizations should adopt it. Dynamic Capability Enhancement (52.6%) and Digital Resilience Outcomes (41.2%) were less frequently coded, confirming our observation that organizational-level impact analysis remains underdeveloped.

Temporal analysis reveals an exponential growth curve: 8 sources addressed vibe coding in February–April 2025 (the "naming period"), 23 in May–July 2025 ("awareness expansion"), 31 in August–October 2025 ("critical analysis"), and 35 in November 2025–February 2026 ("maturation"), suggesting rapid discursive evolution from excitement toward more nuanced assessment.

### 4.2 The Vibe Coding Paradigm: Characterization and Evolution (RQ1)

#### 4.2.1 Discourse Across Source Types

A significant divergence exists between academic and practitioner framings of vibe coding. Academic sources predominantly frame vibe coding as a productivity tool with associated risks, employing quantitative metrics (lines of code generated, bug rates, development speed) and positioning it within existing software engineering taxonomies [25,40,42]. Practitioner and industry sources, by contrast, frame vibe coding as a paradigm shift with organizational and strategic implications, using language of "democratization," "disruption," and "transformation" [18,44,61]. Developer community sources exhibit the widest range of perspectives, from enthusiastic advocacy ("vibe coding will make everyone a developer") to deep skepticism ("vibe coding will create a generation of developers who can't debug their own code") [62,63].

#### 4.2.2 Positioning on the CASE → Low-Code → Vibe Coding Continuum

Our analysis identifies vibe coding as the third major paradigm in the evolution of software development automation, following CASE tools and low-code platforms. Table 4 presents a systematic comparison, extending Sanchis et al.'s [1] benchmarking framework (their Table 5) to include vibe coding platforms.

**Table 4.** Comparative analysis of development automation paradigms (extending Sanchis et al. [1]).

| Feature | CASE Tools (1980s–1990s) | Low-Code Platforms (2014–present) | Vibe Coding Platforms (2025–present) |
|---------|--------------------------|----------------------------------|--------------------------------------|
| Development interface | Visual modeling (UML), structured design tools | Visual drag-and-drop, pre-built modules, configuration wizards | Natural language prompts to LLMs |
| Code generation | Automated from models (often partial) | Platform-specific configurations, minimal hand-coding | Standard code output (HTML, CSS, JS, Python, etc.) |
| Code ownership | Developer-owned but tool-dependent formats | Vendor-locked / platform-dependent | Full ownership, deploy anywhere |
| Target user | Professional developers, system analysts | Citizen developers (some training needed), pro-developers | Anyone with domain knowledge (near-zero learning curve) |
| Learning curve | High (specialized training required) | Moderate (platform-specific training) | Near-zero (natural language interface) |
| Security governance | Developer-managed, no embedded controls | Platform-embedded controls, audit trails, compliance features | Unstructured; 45% of AI code has vulnerabilities [64] |
| Enterprise scalability | Designed for enterprise but poor adoption | Proven at enterprise scale for departmental apps | Uncertain; complexity ceiling for large distributed systems |
| Development speed | Modest improvement over hand-coding | 5–10x faster than hand-coding [38] | 60–80% faster than traditional; prototypes in hours [25] |
| Cost model | High license + training costs | Platform subscription fees (moderate) | AI API costs / tool licenses (often lower) |
| QA practices | Integrated verification/validation tools | Built-in testing within platform | Often skipped (36% skip QA entirely) [25] |
| Vendor lock-in | Moderate (tool-specific formats) | High (platform dependency) | Low (standard code output) |
| Maintenance burden | Moderate | Low (platform manages updates) | High (AI-generated code harder to maintain) [42] |
| Governance maturity | Moderate (professional developer context) | Established (compliance features, access controls) | Nascent (no built-in governance) |
| Adoption rate | 26.5% peak adoption [10] | Growing; projected $21.2B market by 2022 [39] | Rapid: 87% Fortune 500 within 12 months [18] |
| Key failure mode | Unrealistic expectations, complexity [10] | Vendor lock-in, scalability limits [1] | Security vulnerabilities, technical debt, skill erosion [25,42] |

This comparative analysis reveals that each paradigm addressed specific limitations of its predecessor while introducing new challenges. CASE tools addressed the need for development automation but were too complex and expensive for broad adoption. Low-code platforms addressed accessibility and speed but introduced vendor lock-in and scalability constraints. Vibe coding addresses accessibility even further (natural language interface) and eliminates vendor lock-in (standard code output) but introduces novel risks around code quality, security, and the decoupling of code creation from code comprehension.

#### 4.2.3 Cross-Industry Discourse Patterns

Our analysis reveals sector-specific patterns in how vibe coding is discussed in relation to digital transformation. The technology sector dominates the discourse (78.4% of sources), primarily through developer productivity and tooling lenses. Financial services (34.0%) emphasizes compliance, security, and regulatory risk concerns alongside enthusiasm for accelerated internal tool development. Healthcare (21.6%) focuses on patient-facing application development and the potential for domain experts to build clinical tools, tempered by strict regulatory requirements (HIPAA, FDA). Manufacturing (19.6%) extends the low-code digital transformation narrative documented by Sanchis et al. [1] to vibe coding, with particular interest in IoT integration and shop-floor automation tools. Education (15.5%) discusses vibe coding's implications for computer science curriculum and its potential for administrative tool development. Notably, all sectors except technology frame the discussion primarily in organizational and strategic terms rather than individual developer productivity terms.

### 4.3 Vibe Coding and Digital Resilience: Enablers and Threats (RQ2)

#### 4.3.1 Resilience Enablers Mapped to Dynamic Capabilities

**Sensing enhancement.** Forty-seven sources (48.5%) identify vibe coding's rapid prototyping capability as a significant enhancer of organizational sensing. The ability to build functional MVPs in hours rather than months allows organizations to test market hypotheses at dramatically reduced cost and time. One industry report describes a financial services firm that used vibe coding to build and deploy seven prototype customer-facing applications in a single sprint, testing different value propositions simultaneously—a process that would have required months of traditional development and significant budget allocation [61]. This "hypothesis velocity" enables organizations to detect opportunities and threats faster, directly enhancing the sensing dimension of dynamic capabilities as theorized by Warner and Wager [28].

Importantly, this sensing enhancement extends beyond product development. Organizations report using vibe-coded prototypes for internal process improvement (identifying operational inefficiencies by building monitoring tools rapidly), competitive intelligence (quickly building tools that scrape and analyze competitor data), and stakeholder engagement (demonstrating concepts to boards and investors within hours of ideation) [44,65].

**Seizing acceleration.** Fifty-three sources (54.6%) identify compressed development cycles as the primary seizing capability enhancement. The reduction of time-to-market from months to days or hours enables organizations to capture value from opportunities before competitors can respond. This acceleration is particularly significant in fast-moving markets where first-mover advantage is material. The removal of the talent bottleneck—organizations no longer need to wait for scarce developer resources to become available—further accelerates seizing [18,25].

Cost reduction amplifies seizing capability by lowering the threshold for pursuing opportunities. When the cost of building a digital solution drops from hundreds of thousands of dollars to hundreds or thousands (AI API costs and developer time), organizations can afford to pursue a broader portfolio of opportunities, increasing the probability of value capture. McKinsey estimates that organizations using AI-assisted development tools reduce software development costs by 30–50% for appropriate use cases [44].

**Transforming capability.** Thirty-nine sources (40.2%) identify citizen developer empowerment as a transformative capability enhancement with significant resilience implications. When non-technical staff—marketing managers, operations specialists, domain experts—can build functional applications through natural language prompts, the organizational boundary between IT and business functions fundamentally shifts. This redistribution of digital capability building from a centralized IT function to distributed business units represents the most significant organizational transformation identified in our analysis.

This transformation manifests in several ways: (a) business units build their own operational tools rather than waiting in IT development queues; (b) domain experts create specialized applications that capture tacit knowledge previously inaccessible to IT developers; (c) innovation becomes distributed, with digital solutions emerging from across the organization rather than solely from IT-driven initiatives; and (d) the organization develops a broader base of digitally capable employees, creating redundancy that enhances resilience to talent loss [53,65].

#### 4.3.2 Threats to Resilience

**Security vulnerabilities.** The most frequently coded threat to resilience appears in 59 sources (60.8%). Veracode's 2025 GenAI Code Security Report found that 45% of AI-generated code introduces security vulnerabilities [64]. CodeRabbit's analysis reported that AI co-authored code exhibits 2.74 times higher rates of security issues compared to human-written code [66]. These vulnerabilities include injection flaws, broken authentication, sensitive data exposure, and insecure deserialization—precisely the OWASP Top 10 categories that represent the most critical web application security risks.

The security threat is compounded by the "accept all" mentality characteristic of vibe coding. When practitioners accept generated code without security review, vulnerabilities propagate into production systems undetected. This is particularly concerning for organizations in regulated industries (finance, healthcare, government) where security breaches carry severe penalties and can undermine stakeholder trust—a direct threat to organizational resilience [64,66].

**The "vulnerable developer" phenomenon.** Thirty-one sources (32.0%) discuss what Fawzy et al. [25] term the "vulnerable developer"—a practitioner who can build functional applications through vibe coding but cannot debug, maintain, secure, or understand the underlying code. Their grey literature review estimated that 63% of active vibe coding practitioners are non-developers who lack the skills to maintain their creations beyond the initial generation phase. This phenomenon creates a fragile layer of digital infrastructure: applications that work but cannot be reliably modified, debugged, or secured when problems arise.

The vulnerable developer phenomenon directly undermines the coping dimension of resilience. When disruptions occur—a security breach, a system failure, a required integration change—organizations need the ability to rapidly diagnose and resolve issues. If the application's creator cannot comprehend the codebase, the organization faces a critical knowledge gap precisely when response speed is most essential [25,42].

**Technical debt accumulation.** Forty-four sources (45.4%) identify technical debt as a significant concern. The "flow-debt trade-off" described in arXiv:2512.11922 [42] captures this dynamic: the seamless, frictionless nature of AI code generation encourages rapid production of functional code, but this code often exhibits architectural inconsistencies, redundant logic, poor documentation, suboptimal performance, and violations of software engineering best practices. Because the code was generated rather than architected, it lacks the structural coherence that comes from intentional design.

This is particularly consequential because maintenance represents 80% or more of the total software lifecycle cost [67]. An application that is fast to build but expensive to maintain does not necessarily reduce total cost of ownership—it merely shifts costs from the creation phase to the maintenance phase. If maintenance requires skilled developers who must reverse-engineer AI-generated code they did not write and the original creator does not understand, the effective maintenance cost may actually increase [42,68].

**Skill erosion and knowledge concentration risk.** Twenty-six sources (26.8%) raise concerns about long-term skill erosion in development teams. When developers routinely accept AI-generated code without engaging in the cognitive work of design, implementation, and debugging, their core engineering skills may atrophy. This creates a dependency on AI tools that becomes fragile if those tools become unavailable (due to service outages, pricing changes, or vendor decisions) or if the limitations of AI-generated code require human engineering expertise to resolve [25,63].

The knowledge concentration risk is a related but distinct concern: when code exceeds developer comprehension [14], organizational knowledge about critical systems becomes fragile. If the AI model that generated the code changes or becomes unavailable, and no human fully understands the system, the organization faces a knowledge void that directly threatens its adaptive capacity [42].

#### 4.3.3 Comparative Analysis with Low-Code

Table 5 presents a comparative analysis of resilience factors across low-code and vibe coding paradigms.

**Table 5.** Comparative resilience analysis: Low-code vs. vibe coding.

| Resilience Factor | Low-Code Platforms | Vibe Coding Platforms | Assessment |
|-------------------|-------------------|----------------------|------------|
| Development speed (sensing/seizing) | 5–10x faster [38] | 60–80% faster; prototypes in hours [25] | Vibe coding significantly amplifies |
| Cost of experimentation (sensing) | Moderate (platform subscription) | Low (API costs per query) | Vibe coding lowers barrier further |
| Citizen developer enablement (transforming) | Partial (training still required) | Extensive (natural language interface) | Vibe coding dramatically extends |
| Security governance (coping) | Platform-embedded controls | No built-in governance | Low-code significantly stronger |
| Code maintainability (adaptation) | Platform-managed updates | Developer-managed; often poorly documented | Low-code significantly stronger |
| Vendor lock-in risk (adaptation) | High (platform dependency) [1] | Low (standard code output) | Vibe coding significantly stronger |
| Scalability (coping) | Constrained for enterprise [13] | Uncertain; complexity ceiling unknown | Neither clearly superior |
| Knowledge retention (adaptation) | Moderate (platform abstracts complexity) | Low (code exceeds comprehension) [14] | Low-code moderately stronger |
| Governance maturity (coping) | Established (compliance features) | Nascent (no standardized practices) | Low-code significantly stronger |
| Workforce resilience (transforming) | Moderate (platform-specific skills) | Uncertain (natural language skills vs. skill erosion) | Trade-off: broader access vs. fragile capabilities |

This comparison reveals that vibe coding amplifies the positive resilience contributions of low-code (speed, cost reduction, democratization) while simultaneously amplifying the negative dimensions (security risk, maintenance burden, knowledge fragility). The key differentiator is governance: low-code platforms embed governance mechanisms within their platforms, while vibe coding produces ungoverned standard code, placing the entire governance burden on the organization.

### 4.4 Adoption Factors and Sustainability Implications (RQ3)

#### 4.4.1 TOE Analysis of Adoption Factors

**Technology factors.** The most frequently cited technology-context driver is LLM capability trajectory (coded in 67.0% of sources). Practitioners and organizations observe that AI coding capabilities are improving rapidly with each model generation, creating an expectation of continuously increasing returns from vibe coding adoption. Tool ecosystem maturity is the second most cited factor (54.6%): the proliferation of specialized vibe coding platforms (Cursor, Replit, v0.dev, Bolt, Lovable) with differentiated capabilities provides options for diverse organizational needs. The primary technology barrier is integration challenges (41.2%)—connecting AI-generated code with existing enterprise systems, databases, APIs, and deployment pipelines requires technical expertise that contradicts the accessibility promise [25,40].

**Organizational factors.** Existing digital maturity emerges as the strongest organizational predictor of successful vibe coding adoption (coded in 52.6% of sources). Organizations with established development workflows, code review practices, testing infrastructure, and deployment pipelines can integrate vibe-coded contributions more safely than organizations without this foundation. Organizational AI culture—the degree to which the organization embraces experimentation with AI tools and tolerates the associated risks—is the second most cited factor (47.4%). Governance readiness (38.1%) is identified as a critical but often absent factor: organizations that adopt vibe coding without establishing governance frameworks for AI-generated code face elevated security and quality risks [65,68].

**Environmental factors.** Competitive pressure is the most cited environmental driver (61.9%): when 87% of Fortune 500 companies adopt vibe coding platforms [18], non-adopters face strategic anxiety about falling behind. The persistent developer talent shortage (49.5%) drives adoption as a substitute for scarce human resources. Regulatory uncertainty (35.1%) acts as both barrier and driver: regulated industries face compliance concerns about AI-generated code, but the same organizations face competitive pressure to accelerate digital initiatives.

#### 4.4.2 DOI Analysis

Applying Rogers' [30] framework, vibe coding exhibits an unusual combination of innovation characteristics. It scores exceptionally high on relative advantage (dramatic speed and cost improvements), trialability (free/low-cost tools), observability (visible working prototypes in hours), and low complexity (natural language interface). However, it scores poorly on compatibility with existing software engineering practices (accepting code without review contradicts professional norms).

This creates what we term a "quality chasm"—vibe coding diffuses rapidly due to its extraordinary accessibility and visible benefits, but encounters resistance when it reaches organizations with mature engineering practices that demand code quality, security, and governance standards. This pattern suggests that vibe coding's diffusion curve may not follow the smooth S-curve predicted by classical DOI theory but may instead exhibit a bifurcation: rapid adoption for prototyping, internal tools, and non-critical applications, with slower and more contested adoption for production, enterprise, and mission-critical systems.

Based on current adoption data, vibe coding appears to be at the inflection point between early adopters and the early majority—the critical juncture that Geoffrey Moore [69] termed "crossing the chasm." Whether vibe coding successfully crosses this chasm for enterprise-grade applications will depend largely on the maturation of governance frameworks and the resolution of security and quality concerns.

#### 4.4.3 Sustainability Tensions

Four primary sustainability tensions emerge from the analysis:

**Speed vs. quality.** The most pervasive tension (coded in 63.9% of sources). Sixty-two percent of practitioners report being motivated primarily by speed gains, yet 68% perceive AI-generated outputs as "fast but flawed" [25]. This tension is structural: the speed advantage of vibe coding derives partly from skipping quality assurance steps (code review, testing, security scanning) that slow down traditional development but exist to ensure quality [42].

**Democratization vs. governance.** Thirty-seven sources (38.1%) identify the tension between empowering non-developers and maintaining software governance. When anyone can build and deploy applications, the risk of "shadow IT"—applications built outside IT oversight—increases significantly. Sanchis et al. [1] identified this same tension in the low-code context; vibe coding amplifies it because the barrier to creation is even lower and the output is standard code that can be deployed anywhere without platform-mediated controls.

**Innovation velocity vs. technical debt.** Thirty-four sources (35.1%) discuss the tension between rapid creation and long-term maintainability. Each vibe-coded application adds to the organization's code portfolio, but if 80% of software lifecycle cost is in maintenance [67], rapid creation of hard-to-maintain code may generate negative long-term value even if it provides short-term benefits.

**Resource efficiency vs. environmental cost.** Sixteen sources (16.5%) raise the tension between reduced human development resources and increased computational resources. LLM inference requires significant energy and computing resources; generating code through AI shifts the environmental burden from human labor to data center computation. As vibe coding scales, the aggregate environmental impact of billions of AI coding queries becomes a sustainability consideration that current discourse largely ignores [70].

---

## 5. Discussion

### 5.1 Theoretical Contributions

#### 5.1.1 The Resilience Paradox

The central theoretical contribution of this study is the identification and theorization of the "resilience paradox" of vibe coding. Through the lens of Dynamic Capabilities Theory, we find that vibe coding simultaneously strengthens and weakens organizational digital resilience. It strengthens sensing (rapid prototyping for opportunity/threat detection), seizing (compressed time-to-market for value capture), and transforming (citizen developer empowerment for distributed capability building). Yet it introduces novel fragilities that undermine coping (security vulnerabilities, unmaintainable code) and may ultimately compromise adaptation (skill erosion, knowledge concentration risk).

This paradox extends and refines Warner and Wager's [28] digital transformation dynamic capabilities framework. Their nine microfoundations assume that digital capabilities are built by competent actors who understand the tools and systems they create. Vibe coding challenges this assumption: the actors may not understand what they have created, and the creation itself may contain hidden vulnerabilities. We propose an extension to the framework that introduces a "capability quality" dimension alongside capability speed and scope—recognizing that faster and more distributed capability building is only beneficial if the capabilities produced are reliable, secure, and maintainable.

#### 5.1.2 TOE Refinement for AI-Assisted Development

Our findings refine the TOE framework for the vibe coding context in three ways. First, the technology dimension must now account for AI model capability as a dynamically evolving factor—unlike traditional technologies with stable feature sets, LLM capabilities change with each model generation, creating a moving target for organizational adoption decisions. Second, the organizational dimension must incorporate "AI readiness" as a distinct construct beyond traditional IT readiness, encompassing governance frameworks for AI-generated outputs, organizational culture around AI experimentation, and workforce capability for AI-augmented work. Third, the environmental dimension is characterized by unusually intense competitive pressure and FOMO (fear of missing out) dynamics that may drive premature adoption before governance readiness is achieved.

#### 5.1.3 DOI Insights and the Quality Chasm

Our DOI analysis reveals that vibe coding's innovation attributes predict extremely rapid diffusion—perhaps the fastest diffusion of any software development paradigm in history. However, the compatibility gap with existing engineering practices creates what we term a "quality chasm" that may segment the market into two distinct adoption trajectories: rapid, broad adoption for non-critical applications (prototyping, internal tools, MVPs) and slower, more contested adoption for production and enterprise-grade systems. This bifurcated diffusion pattern extends Rogers' [30] theory by identifying how a single innovation can follow different diffusion curves in different organizational contexts based on the criticality of the use case.

### 5.2 Practical Implications for Organizations

#### 5.2.1 Governance Framework for Vibe Coding Adoption

Based on our findings, we propose a tiered governance framework aligned with application criticality:

**Tier 1 — Exploration and prototyping (minimal governance).** For internal prototypes, proof-of-concepts, and disposable experiments, vibe coding can be used with minimal governance. These applications are not deployed to production, do not handle sensitive data, and are expected to be discarded or rebuilt.

**Tier 2 — Internal tools and departmental applications (moderate governance).** For applications used internally but handling real data and supporting business processes, organizations should require: automated security scanning of AI-generated code, basic code review by a technically competent team member, integration testing against existing systems, and documentation of the application's purpose and limitations.

**Tier 3 — Customer-facing and business-critical applications (full governance).** For production applications affecting customers or core business operations, vibe-generated code should be subject to the same governance as traditionally developed code: comprehensive code review, security audit, performance testing, compliance verification, and ongoing maintenance planning.

This tiered approach enables organizations to capture the speed and accessibility benefits of vibe coding for appropriate use cases while maintaining governance rigor where the stakes are higher.

#### 5.2.2 The "Vibe Engineering" Middle Ground

Willison's [43] distinction between vibe coding and "vibe engineering" points toward a sustainable middle ground. Vibe engineering—using AI coding tools while maintaining accountability, conducting reviews, writing tests, and ensuring comprehension—captures much of the speed benefit while mitigating the quality and security risks. Organizations may benefit from establishing vibe engineering as the standard practice for professional developers, reserving pure vibe coding (accept-all, no-review) for Tier 1 exploration activities.

#### 5.2.3 Hybrid Development Strategy

Our comparative analysis suggests that the optimal organizational strategy is not to choose between low-code and vibe coding but to deploy them complementarily:

- **Vibe coding** for rapid prototyping, market hypothesis testing, and innovation exploration (leveraging its speed and zero learning curve)
- **Low-code platforms** for production departmental applications requiring governance, scalability, and platform-managed maintenance (leveraging their embedded governance and enterprise features)
- **Traditional professional development** for mission-critical systems, complex distributed architectures, and applications with stringent security and performance requirements (leveraging deep engineering expertise)

This hybrid strategy mirrors the three-tier governance framework and enables organizations to match development approach to use case criticality.

#### 5.2.4 Workforce Implications

Vibe coding necessitates new organizational roles and reskilling strategies. Emerging roles include: AI code reviewers (professionals who specialize in reviewing and securing AI-generated code), prompt engineers (specialists who optimize natural language prompts for code generation quality), and digital capability coordinators (liaisons between citizen developers and IT governance functions). Existing developers should be reskilled toward AI-augmented development practices (vibe engineering) rather than replaced, as their engineering expertise becomes more rather than less valuable when AI-generated code requires human oversight [25,63].

### 5.3 Forecasting the Paradigm Shift

#### 5.3.1 Hype Cycle Positioning

Applying the Gartner Hype Cycle framework, vibe coding in early 2026 appears to be approaching the "Peak of Inflated Expectations." The initial excitement (Collins Word of the Year, dramatic adoption statistics, breathless media coverage) is beginning to encounter the reality of security vulnerabilities, maintenance challenges, and governance gaps. We anticipate a "Trough of Disillusionment" in 2026–2027 as organizations experience the consequences of ungoverned vibe-coded applications at scale—security incidents attributable to AI-generated code, maintenance crises in applications whose creators cannot fix them, and regulatory scrutiny of AI-generated code in critical systems.

#### 5.3.2 Historical Parallels with CASE Tools

The historical parallels between vibe coding and CASE tools are instructive but not deterministic. Both generated enormous initial enthusiasm, both promised to democratize and accelerate development, and both faced fundamental adoption challenges. However, critical differences suggest vibe coding may avoid CASE's 73.5% non-adoption outcome: (a) vibe coding's learning curve is dramatically lower (natural language vs. specialized modeling tools); (b) the cost of experimentation is orders of magnitude lower; (c) the results are immediately visible and functional; and (d) the underlying AI technology is on a steep improvement trajectory, whereas CASE tools hit capability plateaus relatively quickly.

The more cautionary parallel is the speed-to-quality gap. CASE tools were abandoned in part because their quality benefits were "overrated" [10] and their complexity was a barrier. If vibe coding's quality issues prove intractable—if AI-generated code remains fundamentally less secure, less maintainable, and less reliable than human-written code—organizations may similarly pull back from broad adoption, confining vibe coding to narrow use cases where quality is less critical.

#### 5.3.3 Critical Factors for Sustainable Mainstream Adoption

Based on our analysis, five factors will determine whether vibe coding achieves sustainable mainstream enterprise adoption:

1. **Security maturation:** AI coding tools must achieve substantially lower vulnerability rates. Progress is evident (GitHub Copilot's vulnerability rate has decreased with each model generation), but the current 45% vulnerability rate is incompatible with enterprise requirements.

2. **Governance standardization:** Industry-standard governance frameworks for AI-generated code must emerge, analogous to the compliance features that low-code platforms have built into their products.

3. **Maintenance tooling:** Tools specifically designed for maintaining, debugging, and refactoring AI-generated code must mature, addressing the unique challenges of code that was generated rather than architecturally designed.

4. **Regulatory clarity:** Regulatory bodies must provide clear guidance on the use of AI-generated code in regulated industries, reducing the compliance uncertainty that currently inhibits adoption in financial services, healthcare, and government.

5. **Educational adaptation:** Computer science and software engineering education must evolve to prepare graduates for AI-augmented development practices, ensuring a workforce capable of both leveraging and governing AI-generated code.

#### 5.3.4 Vision: The Hybrid Future

Our forecasting analysis suggests that the future of organizational software development is not a simple replacement of one paradigm by another but a layered coexistence. Vibe coding, low-code platforms, and traditional professional development will coexist, each serving different use cases along a criticality spectrum. Organizations that develop the governance frameworks, workforce capabilities, and strategic clarity to deploy each paradigm appropriately will be best positioned for digital resilience. Those that adopt vibe coding uncritically—seduced by speed without governance—risk accumulating a portfolio of fragile, insecure, unmaintainable digital assets that undermine rather than enhance their resilience.

---

## 6. Conclusion, Limitations, and Future Research

### 6.1 Summary of Contributions

This study provides the first theoretically grounded, cross-industry content analysis of vibe coding's impact on organizational digital transformation and resilience. Through directed content analysis of 97 sources spanning academic literature, industry reports, developer community discourse, and platform documentation, analyzed through an integrated lens of Dynamic Capabilities Theory, the TOE framework, and DOI Theory, we offer three principal contributions.

Addressing **RQ1**, we characterize the current state of discourse on vibe coding, identifying it as the third major paradigm in software development automation following CASE tools and low-code platforms. We document significant divergence between academic framings (productivity tool with risks) and practitioner framings (paradigm shift with organizational implications), and provide a systematic comparative analysis extending Sanchis et al.'s [1] low-code benchmarking framework to the vibe coding era.

Addressing **RQ2**, we identify and theorize the "resilience paradox"—the finding that vibe coding simultaneously enhances and threatens organizational digital resilience. Vibe coding strengthens sensing (rapid prototyping), seizing (compressed time-to-market), and transforming (citizen developer empowerment) capabilities while introducing novel fragilities including security vulnerabilities (45% of AI-generated code), the "vulnerable developer" phenomenon (63% of practitioners), technical debt accumulation, and skill erosion risk. Our comparative analysis with low-code platforms reveals that vibe coding amplifies both the positive and negative resilience dimensions.

Addressing **RQ3**, we identify key adoption factors through TOE analysis (LLM capability trajectory, organizational digital maturity, competitive pressure), characterize vibe coding's position on the DOI adoption curve (early adopter to early majority transition), and document four critical sustainability tensions: speed vs. quality, democratization vs. governance, innovation velocity vs. technical debt, and resource efficiency vs. environmental cost. We introduce the concept of the "quality chasm" that may bifurcate vibe coding's diffusion trajectory based on application criticality.

### 6.2 Practical Takeaways

For organizational leaders, this study offers actionable guidance: (a) adopt a tiered governance framework matching vibe coding governance rigor to application criticality; (b) establish "vibe engineering" as the standard practice for professional developers, capturing speed benefits while maintaining accountability; (c) pursue a hybrid development strategy deploying vibe coding, low-code, and traditional development complementarily; (d) invest in workforce reskilling toward AI-augmented development rather than wholesale replacement of developers; and (e) prepare for the governance and maintenance challenges that will emerge as vibe-coded applications mature.

### 6.3 Limitations

Several limitations must be acknowledged. First, the temporal scope (12 months for vibe coding sources) captures a rapidly evolving phenomenon in its earliest stage; the discourse, adoption patterns, and organizational impacts documented here are likely to shift substantially as the paradigm matures. Second, the English-only language restriction excludes vibe coding discourse in other languages, potentially missing important perspectives from non-English-speaking technology communities (particularly in East Asia). Third, content analysis inherently involves subjective interpretation despite our intercoder reliability protocol (Krippendorff's Alpha = 0.83); different researchers with different theoretical priors might code and interpret the same sources differently. Fourth, the rapidly shifting landscape means that specific statistics cited (adoption rates, vulnerability percentages) may become outdated quickly. Fifth, our analysis draws on published discourse rather than primary organizational data; the gap between what organizations say about vibe coding and what they actually experience may be significant.

### 6.4 Future Research Agenda

This study opens several avenues for future research:

1. **Longitudinal case studies** of organizations implementing vibe coding for digital transformation, tracking resilience outcomes over time as vibe-coded applications move through their lifecycle from creation through maintenance and eventual retirement.

2. **Quantitative survey research** measuring vibe coding adoption factors using our TOE model, enabling statistical testing of the relationships proposed in our integrated conceptual model across a representative sample of organizations.

3. **Sector-specific deep dives** investigating vibe coding's impact in regulated industries (healthcare, financial services) where the resilience paradox is most acute and governance requirements most stringent.

4. **Environmental impact quantification** comparing the lifecycle environmental costs of AI-assisted versus traditional development, addressing the resource efficiency vs. environmental cost tension identified in our analysis.

5. **The "vulnerable developer" phenomenon** as a subject of focused investigation, examining its long-term organizational implications for knowledge management, workforce development, and digital resilience.

6. **Governance framework validation** through action research or design science methodologies, testing and refining the tiered governance framework proposed in this paper in real organizational contexts.

7. **Comparative international studies** examining how vibe coding adoption and governance vary across regulatory regimes, cultural contexts, and technological ecosystems.

As vibe coding continues its rapid diffusion, the academic community must keep pace with a phenomenon that is reshaping how organizations build digital capabilities. The resilience paradox identified in this study underscores the urgency: vibe coding's extraordinary potential to accelerate digital transformation is matched by its capacity to introduce new fragilities. Organizations, policymakers, and researchers must engage critically with both dimensions to ensure that this paradigm shift contributes to sustainable digital resilience rather than the accumulation of hidden digital risk.

---

## References

[1] R. Sanchis, Ó. García-Perales, F. Fraile, R. Poler, Low-code as enabler of digital transformation in manufacturing industry, Applied Sciences 10 (2020) 12. https://doi.org/10.3390/app10010012

[2] R. Sanchis, R. Poler, Enterprise resilience assessment—A quantitative approach, Sustainability 11 (2019) 4327. https://doi.org/10.3390/su11164327

[3] G. Vial, Understanding digital transformation: A review and a research agenda, The Journal of Strategic Information Systems 28 (2019) 118–144. https://doi.org/10.1016/j.jsis.2019.01.003

[4] M. Tabrizi, E. Lam, K. Girard, V. Irvin, Digital transformation is not about technology, Harvard Business Review (2019).

[5] Everest Group, The $2.3 trillion digital transformation challenge, Everest Group Research Report, 2024.

[6] M. Fryling, Low code app development, Journal of Computing Sciences in Colleges 34 (2019) 119.

[7] T. Clancy, The Standish Group Chaos Report, Standish Group, West Yarmouth, MA, 2014.

[8] International Data Corporation, CASE tools market report, IDC, 1996.

[9] J. Iivari, Why are CASE tools not used?, Communications of the ACM 39 (1996) 94–103. https://doi.org/10.1145/232014.232024

[10] J. Iivari, Why are CASE tools not used?, Communications of the ACM 39 (1996) 94–103. https://doi.org/10.1145/232014.232024

[11] C.C. Huff, Elements of a realistic CASE tool adoption budget, Communications of the ACM 35 (1992) 45–55. https://doi.org/10.1145/129617.129619

[12] C. Richardson, J.R. Rymer, New Development Platforms Emerge for Customer-Facing Applications, Forrester, Cambridge, MA, 2014.

[13] M. Tisi, J.M. Mottu, D. Kolovos, D. De Lara, J. Guerra, E. Di Ruscio, D. Pierantonio, A. Wimmer, Lowcomote: Training the next generation of experts in scalable low-code engineering platforms, 2019.

[14] A. Karpathy, Vibe coding [X post], February 2, 2025.

[15] Collins Dictionary, Word of the Year 2025: Vibe coding, Collins English Dictionary, 2025.

[16] Stack Overflow, 2025 Developer Survey Results, Stack Overflow, 2025.

[17] Gartner, Predicts 2025: Software engineering, Gartner Research, 2025.

[18] J. Shmargad, Vibe coding comes to the enterprise, Forrester Research, 2025.

[19] Y Combinator, W2025 batch demographics and technology trends, Y Combinator Blog, 2025.

[20] F.P. Sahay, A. Indamutsa, D. Di Ruscio, A. Pierantonio, Supporting the understanding and comparison of low-code development platforms, in: Proceedings of the 46th Euromicro Conference on Software Engineering and Advanced Applications (SEAA), IEEE, 2020, pp. 171–178.

[21] D. Cabot, Low-code development and model-driven engineering: Two sides of the same coin?, Software and Systems Modeling 19 (2020) 1–8.

[22] A. Ziegler, E. Kalliamvakou, X.A. Li, A. Rice, D. Rifkin, S. Simister, G. Sittampalam, E. Aftandilian, Productivity assessment of neural code completion, in: Proceedings of the 6th ACM SIGPLAN International Symposium on Machine Programming, 2022, pp. 21–29.

[23] S. Imai, Is GitHub Copilot a substitute for human pair-programming?, in: Proceedings of the ACM/IEEE 44th International Conference on Software Engineering: Companion Proceedings, 2022, pp. 38–42.

[24] R.E. Browder, H.E. Aldrich, S.W. Bradley, The emergence of the maker movement: Implications for entrepreneurship research, Journal of Business Venturing 34 (2019) 459–476.

[25] A. Fawzy, M.A. Fahmy, A.S. Abdelfattah, Vibe coding in practice: A grey literature review, arXiv:2510.00328, 2025 [Accepted at ICSE 2026 SEIP Track].

[26] H.F. Hsieh, S.E. Shannon, Three approaches to qualitative content analysis, Qualitative Health Research 15 (2005) 1277–1288. https://doi.org/10.1177/1049732305276687

[27] D.J. Teece, G. Pisano, A. Shuen, Dynamic capabilities and strategic management, Strategic Management Journal 18 (1997) 509–533. https://doi.org/10.1002/(SICI)1097-0266(199708)18:7<509::AID-SMJ882>3.0.CO;2-Z

[28] K.S.R. Warner, M. Wäger, Building dynamic capabilities for digital transformation: An ongoing process of strategic renewal, Long Range Planning 52 (2019) 326–349. https://doi.org/10.1016/j.lrp.2018.12.001

[29] L.G. Tornatzky, M. Fleischer, The Processes of Technological Innovation, Lexington Books, Lexington, MA, 1990.

[30] E.M. Rogers, Diffusion of Innovations, fifth ed., Free Press, New York, 2003.

[31] N. Glover, T. Dudley, Practical Error Correction Design for Engineers, Data Systems Technology Corporation, Reston, VA, 1991.

[32] A. Fuggetta, A classification of CASE technology, Computer Journal 35 (1993) 25–38. https://doi.org/10.1093/comjnl/35.1.25

[33] A. Fuggetta, A classification of CASE technology, Computer Journal 35 (1993) 25–38.

[34] B. Lundell, B. Lings, Changing perceptions of CASE technology, Journal of Systems and Software 72 (2004) 271–280. https://doi.org/10.1016/S0164-1212(03)00155-2

[35] C.C. Huff, Elements of a realistic CASE tool adoption budget, Communications of the ACM 35 (1992) 45–55.

[36] W.J. Orlikowski, CASE tools as organizational change: Investigating incremental and radical changes in systems development, MIS Quarterly 17 (1993) 309–340. https://doi.org/10.2307/249774

[37] OutSystems, The State of Application Development: Is IT Ready for Disruption?, OutSystems, Boston, MA, 2019.

[38] C. Richardson, J.R. Rymer, Vendor Landscape: The Fractured, Fertile Terrain of Low-Code Application Platforms, Forrester, Cambridge, MA, 2016.

[39] J.R. Rymer, R. Koplowitz, The Forrester Wave: Low-Code Development Platforms for AD&D Professionals, Q1 2019, Forrester, Cambridge, MA, 2019.

[40] Survey of vibe coding with large language models, arXiv:2510.12399, 2025.

[41] Vibe coding: AI-native paradigm, arXiv:2510.17842, 2025.

[42] Vibe coding: Flow, technical debt, and guidelines, arXiv:2512.11922, 2025.

[43] S. Willison, Not all AI-assisted programming is vibe coding, Simon Willison's Weblog, 2025.

[44] McKinsey & Company, The state of AI: How organizations are rewiring to capture value, McKinsey Global Survey, 2025.

[45] Boston Consulting Group, From potential to profit: Closing the AI impact gap, BCG Henderson Institute, 2025.

[46] R. Heeks, A.V. Ospina, Conceptualising the link between information systems and resilience: A developing country field study, Information Systems Journal 29 (2019) 70–96.

[47] C.S. Holling, Resilience and stability of ecological systems, Annual Review of Ecology and Systematics 4 (1973) 1–23.

[48] R.E. Browder, Digital transformation as upgrading adaptation promoting enterprise resilience, Strategic Entrepreneurship Journal 18 (2024) 435–463.

[49] X. Li, Y. Wang, Digital transformation and enterprise resilience: Evidence from China, PLOS ONE 19 (2024) e0298891.

[50] C.F. Breidbach, D. Davern, G. Shanks, S. Tian, Orchestrating digital resilience: A socio-technical perspective, European Journal of Information Systems 33 (2024) 562–581.

[51] McKinsey & Company, The agility advantage: How organizations can make decisions faster, McKinsey Quarterly, 2023.

[52] D.J. Teece, Business models and dynamic capabilities, Long Range Planning 51 (2018) 40–49.

[53] C. Lethbridge, Low-code is often no-code: How citizen developers are transforming enterprise IT, MIT Sloan Management Review, 2024.

[54] P. Mayring, Qualitative Content Analysis: Theoretical Foundation, Basic Procedures and Software Solution, Sage, 2014.

[55] S. Elo, H. Kyngäs, The qualitative content analysis process, Journal of Advanced Nursing 62 (2008) 107–115. https://doi.org/10.1111/j.1365-2648.2007.04569.x

[56] V. Garousi, M. Felderer, M.V. Mäntylä, Guidelines for including grey literature and conducting multivocal literature reviews in software engineering, Information and Software Technology 106 (2019) 101–121. https://doi.org/10.1016/j.infsof.2018.09.006

[57] D. Tyndall, AACODS Checklist for Appraising Grey Literature, Flinders University, 2010.

[58] K. Krippendorff, Content Analysis: An Introduction to Its Methodology, fourth ed., Sage, Thousand Oaks, CA, 2019.

[59] Y.S. Lincoln, E.G. Guba, Naturalistic Inquiry, Sage, Newbury Park, CA, 1985.

[60] J. Nicmanis, Reflexivity in qualitative content analysis: A guide for researchers, Qualitative Research 24 (2024) 89–107.

[61] Atos, Vibe coding and the future of enterprise development, Atos Digital Transformation Report, 2025.

[62] Various authors, r/programming: Vibe coding discussion threads, Reddit, 2025.

[63] Various authors, Vibe coding: Democratization or disaster?, DEV Community, 2025.

[64] Veracode, State of Software Security: The Rise of AI-Generated Code, Veracode Annual Report, 2025.

[65] HCLTech, AI-powered development: From vibe coding to enterprise value, HCLTech Whitepaper, 2025.

[66] CodeRabbit, The security impact of AI co-authored code: A quantitative analysis, CodeRabbit Research Report, 2025.

[67] R.S. Pressman, B.R. Maxim, Software Engineering: A Practitioner's Approach, ninth ed., McGraw-Hill, New York, 2020.

[68] Genpact, Navigating the vibe coding revolution: Enterprise readiness assessment, Genpact Insights, 2025.

[69] G.A. Moore, Crossing the Chasm: Marketing and Selling Disruptive Products to Mainstream Customers, third ed., Harper Business, New York, 2014.

[70] E. Strubell, A. Ganesh, A. McCallum, Energy and policy considerations for deep learning in NLP, in: Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics, 2019, pp. 3645–3650.

[71] R. Waszkowski, Low-code platform for automating business processes in manufacturing, IFAC-PapersOnLine 52 (2019) 376–381. https://doi.org/10.1016/j.ifacol.2019.10.060

[72] A. Tarasiev, A. Filippova, M. Aksyonov, K. Aksyonova, O. Developing prototype of CASE-tool to create automation systems based on web applications using code generation, in: Proceedings of the XII International Scientific and Technical Conference Dynamics of Systems, Mechanisms and Machines, IEEE, 2018, pp. 1–4.

[73] D. Al-ashwal, D. Al-Sewari, E.Z. Al-Shargabi, A.A. A CASE tool for JAVA programs logical errors detection: Static and dynamic testing, in: Proceedings of the 2018 International Arab Conference on Information Technology (ACIT), IEEE, 2018, pp. 1–6.

[74] GitHub, Octoverse 2025: The state of AI in software development, GitHub Blog, 2025.

[75] S.G. Pantelimon, T. Rogojanu, T. Braileanu, A. Stanciu, V.D. Dobre, C. Towards a seamless integration of IoT devices with IoT platforms using a low-code approach, in: Proceedings of the IEEE 5th World Forum Internet Things, IEEE, 2019, pp. 566–571.

[76] Y. Wu, S. Wang, C.P. Bezemer, K. Inoue, How do developers utilize source code from Stack Overflow?, Empirical Software Engineering 24 (2019) 637–673.

[77] O. Land, V. Der Zanden, Enterprise design—A practice-driven response for generating and implementing business models, in: Proceedings of the 8th Enterprise Engineering Working Conference (EEWC 2018), Springer, 2018.

[78] C. Zolotas, C. Chatzidimitriou, K.C. Symeonidis, A.L. RESTsec: A low-code platform for generating secure by design enterprise services, Enterprise Information Systems 12 (2018) 1007–1033.

[79] H. Henriques, H. Lourenço, V. Amaral, M. Goulão, Improving the developer experience with a low-code process modelling language, in: Proceedings of the 21st ACM/IEEE International Conference on Model Driven Engineering Languages and Systems, ACM, 2018, pp. 200–210.

[80] Cursor, Enterprise adoption case studies, Cursor Documentation, 2025.

[81] Replit, Building the future: How teams use Replit Agent for production applications, Replit Blog, 2025.

[82] Anthropic, Claude Code: Enterprise development patterns, Anthropic Documentation, 2025.

[83] Vercel, v0.dev: From prompt to production, Vercel Blog, 2025.

[84] ServiceNow, AI-assisted development on the Now Platform, ServiceNow Developer Documentation, 2025.

[85] OutSystems, The role of AI in the next generation of low-code, OutSystems Whitepaper, 2025.

[86] Mendix, Low-code meets AI: The evolution of citizen development, Mendix Research Report, 2025.

[87] Microsoft, Power Platform and AI Builder: Democratizing development, Microsoft Documentation, 2025.

[88] Forrester, The vibe coding maturity model: From experimentation to enterprise value, Forrester Research Report, 2025.

[89] Deloitte, AI-powered development: Risks, rewards, and the road to enterprise adoption, Deloitte Digital Report, 2025.

[90] PwC, The future of software development: How AI is reshaping the build-vs-buy decision, PwC Technology Report, 2025.

---

**Author Contributions:** [To be completed upon submission]

**Funding:** [To be completed upon submission]

**Data Availability Statement:** The coding framework and corpus metadata are available from the corresponding author upon reasonable request.

**Conflicts of Interest:** The authors declare no conflict of interest.

---

*Submitted to: Technological Forecasting and Social Change*
*Manuscript type: Research Article*
*Word count: ~13,700 (excluding references, tables, and figures)*
