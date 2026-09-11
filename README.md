# Enterprise AI Risk Assessment & AI System Inventory
<img width="1100" height="480" alt="banner (1)" src="https://github.com/user-attachments/assets/fde674b5-c1df-4fb9-aa8f-a862ecb21134" />


A portfolio project demonstrating an operational enterprise AI inventory and repeatable AI risk assessment capability — from intake and classification through a 5×5 risk methodology, impact assessment, treatment, approval, and executive reporting — aligned with the NIST AI RMF and ISO/IEC 42001.

## About this repository

This repository contains a single-file portfolio project covering:

- The governance operating model, roles, and an AI System Inventory data model
- The AI intake workflow, mandatory triggers, and a 20-question initial screening tool
- A four-tier internal AI risk classification model and a 5×5 (likelihood × impact) risk methodology
- Twelve AI risk domains and a "Cause → Event → Consequence" risk-statement format
- AI impact assessment, risk treatment options, the approval model, and reassessment triggers/frequencies
- A ten-system AI inventory, with individual risk/control write-ups for every system
- Detailed 5×5-scored risk assessments for the four highest-tier systems (Recruitment Screening, Credit Decision Support, Fraud Detection, Customer Service GenAI)
- A consolidated 13-entry Enterprise Risk Register
- Risk acceptance, exception management, monitoring, shadow-AI discovery, third-party AI risk, and a Generative AI inventory extension
- An evidence matrix, executive KPIs, an executive dashboard specification, NIST AI RMF and ISO/IEC 42001 mapping, and a "Definition of Done" checklist

**Fictional scenario:** The project is built around **Northstar Financial Services**, a fictional 5,000-employee financial services organization operating across the US, UK, EU, and Middle East with roughly 40 known AI use cases spanning customer service, fraud detection, finance, HR, cybersecurity, marketing, knowledge management, credit risk, and document processing. Ten representative systems are fully inventoried and risk-assessed, including a Tier 3/Critical recruitment screening system and credit decision support tool.

## Frameworks referenced

- NIST AI Risk Management Framework 1.0 — GOVERN, MAP, MEASURE, MANAGE
- NIST AI RMF Generative AI Profile (July 2024)
- ISO/IEC 42001:2023
- EU AI Act Article 9 (risk-management system for high-risk AI), referenced for regulatory-considerations context

> **Disclaimer:** This is a fictional portfolio project using synthetic data. It demonstrates an AI inventory and risk-assessment methodology, not legal advice or a formal regulatory compliance determination. The internal risk tiers used here are an organizational governance classification, not a legal classification.

---

# Project 2 — Enterprise AI Risk Assessment and AI System Inventory

## Portfolio Project

| Field | Detail |
|---|---|
| Organization | Northstar Financial Services (fictional) |
| Industry | Financial Services |
| Employees | 5,000 |
| Regions | US, UK, EU and Middle East |
| Known AI use cases | 40 |
| Primary frameworks | NIST AI RMF 1.0, NIST AI RMF Generative AI Profile, ISO/IEC 42001:2023 |
| Project objective | Build an operational enterprise AI inventory and risk assessment capability. |

## 1. Executive Summary

Northstar Financial Services has adopted AI across customer service, fraud detection, finance, human resources, cybersecurity, marketing, knowledge management, credit risk and document processing.

The organization has approximately 40 known AI use cases, but information is fragmented across business units, procurement, technology teams, model owners and vendors. This creates governance gaps:

- unknown or duplicate AI systems;
- unclear ownership;
- inconsistent risk classification;
- incomplete documentation;
- limited visibility into sensitive data;
- inconsistent human oversight;
- weak third-party AI governance;
- overdue assessments;
- shadow AI;
- insufficient evidence for assurance.

The purpose of this project is to create an authoritative AI System Inventory and a repeatable AI Risk Assessment process.

NIST AI RMF 1.0 uses four functions — **GOVERN, MAP, MEASURE and MANAGE** — and describes AI risk management as continuous across the AI lifecycle. NIST also identifies AI system inventories as an important governance mechanism. *Source: NIST AI RMF 1.0 and NIST AI RMF Core.*

ISO/IEC 42001:2023 specifies requirements for establishing, implementing, maintaining and continually improving an Artificial Intelligence Management System. *Source: ISO/IEC 42001:2023.*

## 2. Project Objectives

1. Establish an authoritative inventory of material AI systems.
2. Assign accountable business, technical and risk owners.
3. Classify systems using a consistent internal risk model.
4. Perform repeatable AI risk assessments.
5. Perform AI impact assessments where appropriate.
6. Link risks to controls and evidence.
7. Establish approval gates.
8. Establish reassessment triggers and frequencies.
9. Support third-party AI risk management.
10. Provide executive-level AI risk reporting.

## 3. Scope

### In Scope

- Internally developed AI
- Third-party AI/SaaS
- Machine-learning models
- Predictive analytics
- Generative AI
- RAG applications
- AI APIs and foundation models
- AI-enabled cybersecurity tools
- Automated decision-support systems
- Material pilots and production systems

### Out of Scope

Low-impact deterministic automation or technology formally determined not to meet the organization's AI definition. Every exclusion must be documented.

## 4. Fictional Organization

### Northstar Financial Services

| Attribute | Description |
|---|---|
| Industry | Financial services |
| Employees | 5,000 |
| Regions | US, UK, EU, Middle East |
| Known AI systems | 40 |
| Governance maturity | Developing |
| AI governance maturity | Early |
| Main concern | Rapid AI adoption without consistent enterprise governance |

### Governance Problem

Northstar's leadership cannot confidently answer:

- What AI systems do we have?
- Who owns them?
- What data do they process?
- Which systems affect people?
- Which systems are high risk?
- Which systems have current assessments?
- Which systems use third-party models?
- What controls are operating?
- What evidence exists?
- When must each system be reassessed?

This project answers those questions.

## 5. Governance Operating Model

```
                 AI GOVERNANCE COMMITTEE
                           |
          +----------------+----------------+
          |                |                |
       Business         Technology      Risk/Compliance
        Owners            Owners             Owners
          |                |                |
          +----------------+----------------+
                           |
                    AI GOVERNANCE OFFICE
                           |
       +-------------------+-------------------+
       |                   |                   |
    Inventory           Risk/Impact         Assurance
                        Assessment
       |                   |                   |
       +-------------------+-------------------+
                           |
                  AI SYSTEM LIFECYCLE
                           |
 Identify → Register → Classify → Assess
                           |
 Approve → Deploy → Monitor → Reassess → Retire
```

### Roles

| Role | Responsibility |
|---|---|
| AI Governance Committee | High-risk decisions and risk tolerance |
| AI Governance Office | Inventory, methodology and governance process |
| Business Owner | Purpose, business outcomes and accountability |
| Technical/Model Owner | Technical implementation and performance |
| Risk Owner | Treatment and residual-risk decision |
| Privacy | Privacy assessment |
| Cybersecurity | Security assessment |
| Legal/Compliance | Regulatory applicability |
| Procurement | Third-party governance |
| Internal Audit | Independent assurance |

## 6. AI System Inventory

Every material system receives an identifier: `AI-2026-NNN` (example: `AI-2026-005`)

**Required fields, by category:**

- **Identity** — System ID; System name; Business unit; Description; Version; Lifecycle status
- **Ownership** — Business owner; Technical/model owner; Risk owner; Vendor owner
- **Purpose** — Intended use; Intended users; Prohibited use; Business process
- **Technology** — AI type; Model; Model version; Provider; Hosting; Autonomy; Human oversight
- **Data** — Inputs; Outputs; Personal data; Sensitive data; Confidential data; Data source; Retention; Residency
- **Risk and Impact** — Affected people; Decision significance; Internal risk tier; Inherent risk; Residual risk; Impact rating
- **Governance** — Approval status; Controls; Evidence; Exceptions; Incidents; Assessment date; Next review

## 7. AI Intake Workflow

```
Business Request
      ↓
AI Screening
      ↓
Inventory Record
      ↓
Initial Risk Classification
      ↓
Risk + Impact Assessment
      ↓
Control Requirements
      ↓
Approval
      ↓
Deployment
      ↓
Monitoring
      ↓
Reassessment
```

### Intake Triggers

An intake is mandatory when:

- a new AI system is proposed;
- an existing application adds material AI;
- a third-party AI product is procured;
- a model changes materially;
- intended use changes;
- sensitive data is introduced;
- autonomy increases;
- a new population is affected;
- a material incident occurs;
- regulatory requirements change.

## 8. Initial Screening Questions

1. Does the system use AI/ML/GenAI?
2. Does it generate predictions, recommendations, classifications, content or decisions?
3. Does it process personal data?
4. Does it process sensitive/confidential information?
5. Does it affect customers?
6. Does it affect employees or applicants?
7. Does it influence consequential decisions?
8. Does it use a third-party provider?
9. Does it use a foundation model?
10. Can it take actions autonomously?
11. Does it connect to enterprise systems?
12. Does it operate in a regulated context?
13. Could failure cause material harm?
14. Could it create unfair outcomes?
15. Could compromise create cybersecurity exposure?
16. Is human oversight required?
17. Does the provider retain prompts or inputs?
18. Does the provider use customer information for model training?
19. Can the provider change the model without customer approval?
20. Does the system require specialized monitoring?

A "yes" answer triggers deeper evaluation; it does not automatically determine legal classification.

## 9. Internal AI Risk Classification

This is an **internal governance classification**, not a legal classification.

| Tier | Name | Characteristics |
|---|---|---|
| Tier 1 | Low | Limited impact, low sensitivity, strong human oversight |
| Tier 2 | Moderate | Material operational/data/business exposure |
| Tier 3 | High | Consequential decisions, sensitive populations/data or significant model risk |
| Tier 4 | Critical/Escalated | Exceptional, potentially prohibited/restricted or unacceptable residual risk |

**Tier 1 examples:** employee writing assistant; low-impact knowledge search.

**Tier 2 examples:** customer service assistant; financial forecasting; marketing recommendations; document processing; cybersecurity assistant.

**Tier 3 examples:** recruitment screening; credit decision support; material fraud detection.

**Tier 4 examples:** potentially prohibited use; exceptional safety or rights exposure; severe autonomous action; unacceptable residual risk.

## 10. 5×5 AI Risk Methodology

**Likelihood**

| Score | Rating |
|---|---|
| 1 | Rare |
| 2 | Unlikely |
| 3 | Possible |
| 4 | Likely |
| 5 | Almost Certain |

**Impact**

| Score | Rating |
|---|---|
| 1 | Insignificant |
| 2 | Minor |
| 3 | Moderate |
| 4 | Major |
| 5 | Severe |

**Risk Score:** Inherent Risk = Likelihood × Impact

| Score | Level |
|---|---|
| 1–4 | Low |
| 5–9 | Moderate |
| 10–16 | High |
| 17–25 | Critical |

Residual risk is reassessed after controls. It should not be reduced by an arbitrary percentage.

## 11. AI Risk Domains

Assess applicable risks across:

1. Strategic
2. Operational
3. Cybersecurity
4. Privacy
5. Data quality/provenance
6. Model performance/drift
7. Fairness/bias
8. Explainability
9. Human oversight
10. Third-party/supply chain
11. Legal/regulatory
12. Reputation

### Risk Statement Format

Use: **Cause → Event → Consequence**

**Weak:** "The model may be biased."

**Strong:** "If historical recruitment data contains systematic selection bias, the model may reproduce or amplify the bias, resulting in inconsistent candidate ranking and potential adverse impact on applicants."

## 12. AI Impact Assessment

Risk assessment asks: *What could go wrong?*

Impact assessment asks: *Who could be affected, how could they be affected, and what could the consequence be?*

Assess: customers; employees; applicants; vulnerable groups; privacy; fairness; safety; security; financial outcomes; legal rights; employment; operational continuity; reputation; environmental impact where material.

## 13. Risk Treatment

- **Avoid** — Do not deploy or discontinue the use case.
- **Mitigate** — Implement controls to reduce likelihood and/or impact.
- **Transfer/Share** — Use contractual or other mechanisms to share aspects of risk where appropriate. Organizational accountability is not automatically transferred.
- **Accept** — An authorized risk owner accepts residual risk within approved tolerance.
- **Escalate** — Send risk to a higher authority when it exceeds delegated tolerance.

## 14. Approval Model

| Tier | Approval |
|---|---|
| Tier 1 | Business owner |
| Tier 2 | Business owner + AI Governance |
| Tier 3 | AI Governance Committee or delegated specialist |
| Tier 4 | Executive + Legal/Compliance + specialists |

A completed assessment does not itself constitute approval.

## 15. Reassessment

### Mandatory Triggers

Reassess when: model version changes materially; training data changes materially; intended use changes; affected population changes; geography changes; autonomy increases; vendor/provider changes; material incident occurs; performance degrades materially; significant fairness concern appears; regulation changes; major integration changes.

### Baseline Frequency

| Tier | Minimum Review |
|---|---|
| Tier 1 | 24 months or trigger |
| Tier 2 | 12 months or trigger |
| Tier 3 | 6–12 months or trigger |
| Tier 4 | At least 6 months and trigger |

## 16. Ten-System AI Inventory

| ID | System | AI Type | Provider | Tier | Human Oversight | Main Risk |
|---|---|---|---|---|---|---|
| AI-2026-001 | Customer Service Assistant | GenAI | Third-party | 2 | Human-in-loop | Hallucination/data disclosure |
| AI-2026-002 | Fraud Detection Model | ML | Internal | 3 | Human-on-loop | Model/fairness |
| AI-2026-003 | Employee Writing Assistant | GenAI | Third-party | 1 | Human-in-loop | Confidential data leakage |
| AI-2026-004 | Financial Forecasting | Predictive | Internal | 2 | Human-in-loop | Model error |
| AI-2026-005 | Recruitment Screening | ML | Third-party | 3 | Human-in-loop | Fairness |
| AI-2026-006 | Cyber Threat Assistant | GenAI | Hybrid | 2 | Human-in-loop | Security |
| AI-2026-007 | Marketing Recommendation Engine | ML | Internal | 2 | Human-on-loop | Privacy/profiling |
| AI-2026-008 | Knowledge Search Assistant | RAG/GenAI | Internal | 1 | Human-in-loop | Access leakage |
| AI-2026-009 | Credit Decision Support | ML | Hybrid | 3 | Human-in-loop | Fairness/model |
| AI-2026-010 | Document Processing | ML/OCR | Third-party | 2 | Human-in-loop | Data/error |

## 17. System 1 — Customer Service Assistant

**ID:** AI-2026-001 · **Tier:** 2 · **Purpose:** Assist customers and service staff with routine support.

**Data:** customer account information; support history; approved knowledge-base content.

**Risks:** hallucinated guidance; sensitive-data disclosure; prompt injection; inappropriate recommendations; vendor retention.

**Controls:** authentication; authorization; approved knowledge sources; output validation; human escalation; logging; vendor due diligence.

## 18. System 2 — Fraud Detection Model

**ID:** AI-2026-002 · **Tier:** 3 · **Purpose:** Identify potentially fraudulent transactions.

**Data:** transaction history; customer behavior; historical fraud cases.

**Risks:** false positives; false negatives; model drift; unfair customer impact; adversarial manipulation.

**Controls:** model validation; drift detection; analyst review; performance monitoring; access controls; security monitoring.

## 19. System 3 — Employee Writing Assistant

**ID:** AI-2026-003 · **Tier:** 1 · **Purpose:** Improve low-risk employee drafting and editing.

**Risks:** confidential information disclosure; inaccurate content; inappropriate employee use.

**Controls:** acceptable-use policy; data restrictions; employee training; provider review.

## 20. System 4 — Financial Forecasting

**ID:** AI-2026-004 · **Tier:** 2 · **Purpose:** Support financial planning and forecasting.

**Risks:** inaccurate assumptions; poor data quality; model drift; management over-reliance.

**Controls:** data validation; model validation; human review; performance monitoring; change management.

## 21. System 5 — Recruitment Screening

**ID:** AI-2026-005 · **Tier:** 3 · **Purpose:** Prioritize applications for recruiter review.

**Affected people:** applicants; recruiters; hiring managers.

**Risks:** biased ranking; privacy exposure; automation bias; poor data quality; model drift; inadequate explainability.

**Controls:** fairness testing; representative validation; human review; override capability; recruiter training; data minimization; access control; monitoring.

## 22. System 6 — Cyber Threat Assistant

**ID:** AI-2026-006 · **Tier:** 2 · **Purpose:** Assist security analysts with threat analysis.

**Risks:** incorrect recommendations; sensitive security-data exposure; prompt injection; excessive permissions; analyst over-reliance.

**Controls:** least privilege; analyst validation; logging; restricted tools; secure prompt handling; output verification.

## 23. System 7 — Marketing Recommendation Engine

**ID:** AI-2026-007 · **Tier:** 2 · **Purpose:** Generate approved customer recommendations.

**Risks:** inappropriate profiling; privacy; poor recommendations; unfair targeting; data-quality problems.

**Controls:** data governance; approved features; privacy review; monitoring; campaign approval.

## 24. System 8 — Knowledge Search Assistant

**ID:** AI-2026-008 · **Tier:** 1 · **Purpose:** Help employees find approved internal knowledge.

**Risks:** access-control leakage; hallucinated answers; stale information; incorrect retrieval.

**Controls:** document-level authorization; source attribution; approved data sources; retrieval monitoring.

## 25. System 9 — Credit Decision Support

**ID:** AI-2026-009 · **Tier:** 3 · **Purpose:** Provide analytical recommendations to authorized credit personnel.

**Risks:** inaccurate recommendations; discriminatory outcomes; model drift; explainability limitations; privacy/security exposure; human over-reliance.

**Controls:** model validation; fairness testing where appropriate; human decision authority; monitoring; audit trail; documented rationale; escalation.

## 26. System 10 — Document Processing

**ID:** AI-2026-010 · **Tier:** 2 · **Purpose:** Extract and classify business documents.

**Risks:** extraction errors; sensitive-data exposure; incorrect classification; vendor dependency.

**Controls:** quality checks; access controls; retention controls; human validation for material errors; vendor due diligence.

## 27. Detailed Assessment — Recruitment Screening

### Risk R-005-01: Biased Candidate Ranking

**Cause:** Historical training data contains systematic selection or representation bias.

**Event:** The AI system reproduces or amplifies the bias.

**Consequence:** Applicants receive inconsistent or unfair ranking, creating employment, legal, reputational and trust impacts.

**Likelihood:** 4 · **Impact:** 5 · **Inherent risk:** 20 — Critical

**Treatment:** Mitigate

**Controls:** 1. Training-data review. 2. Feature review. 3. Fairness testing. 4. Representative validation data. 5. Human review. 6. Override capability. 7. Outcome monitoring. 8. Escalation process.

**Evidence:** validation report; fairness test results; model documentation; approval record; monitoring report.

**Residual risk:** Likelihood 2 × Impact 5 = **10 — High**

The system remains Tier 3 because the potential consequence remains material even after mitigation.

## 28. Recruitment Risk R-005-02 — Privacy

**Cause:** Applicant information is processed by the AI system.

**Event:** Unauthorized access, excessive retention or inappropriate vendor processing occurs.

**Consequence:** Applicant privacy harm and regulatory exposure.

**Likelihood:** 3 · **Impact:** 5 · **Inherent:** 15 — High

**Controls:** data minimization; access control; retention limits; approved processing purpose; contractual controls; monitoring.

**Residual:** 2 × 5 = **10 — High**

## 29. Recruitment Risk R-005-03 — Automation Bias

**Cause:** Recruiters perceive AI ranking as objective.

**Event:** Human reviewers accept AI recommendations without adequate independent review.

**Consequence:** Incorrect or unfair decisions persist.

**Likelihood:** 4 · **Impact:** 4 · **Inherent:** 16 — High

**Controls:** mandatory human decision; recruiter training; AI recommendation labeling; override capability; review of overrides; periodic governance testing.

**Residual:** 2 × 4 = **8 — Moderate**

## 30. Detailed Assessment — Credit Decision Support

### R-009-01 Inaccurate Recommendation

**Cause:** Model assumptions, data quality or changing economic conditions.

**Event:** Model provides an inaccurate recommendation.

**Consequence:** Incorrect credit decisions and customer/business impact.

**Likelihood:** 3 · **Impact:** 5 · **Inherent:** 15 — High

**Controls:** independent model validation; performance monitoring; data-quality controls; human decision authority; model-change management; audit logging.

### R-009-02 Unfair Outcomes

**Cause:** Historical data or proxy variables produce unequal outcomes.

**Event:** Recommendations systematically disadvantage certain groups.

**Consequence:** Customer harm, legal exposure, reputational damage and loss of trust.

**Likelihood:** 3 · **Impact:** 5 · **Inherent:** 15 — High

**Controls:** feature review; fairness testing where appropriate; human oversight; outcome monitoring; documented rationale.

## 31. Detailed Assessment — Fraud Detection

### R-002-01 False Positives

**Cause:** Model threshold or data limitations.

**Event:** Legitimate transactions are classified as suspicious.

**Consequence:** Transactions may be delayed or declined.

**Likelihood:** 3 · **Impact:** 5 · **Inherent:** 15 — High

**Controls:** threshold monitoring; analyst review; customer escalation; performance metrics; drift detection.

### R-002-02 Model Drift

**Cause:** Fraud patterns change over time.

**Event:** Model performance deteriorates.

**Consequence:** Increased false positives or missed fraud.

**Likelihood:** 3 · **Impact:** 4 · **Inherent:** 12 — High

**Controls:** drift monitoring; periodic validation; retraining governance; performance thresholds; incident escalation.

## 32. Detailed Assessment — Customer Service GenAI

### R-001-01 Hallucinated Guidance

**Cause:** Generative model produces unsupported content.

**Event:** Customer receives inaccurate information.

**Consequence:** Customer dissatisfaction, operational impact and possible financial/regulatory consequences.

**Likelihood:** 3 · **Impact:** 4 · **Inherent:** 12 — High

**Controls:** approved knowledge sources; retrieval grounding; output validation; human escalation; response monitoring.

### R-001-02 Sensitive-Data Disclosure

**Cause:** Improper prompt, retrieval or access configuration.

**Event:** Unauthorized information is returned.

**Consequence:** Privacy/security incident.

**Likelihood:** 3 · **Impact:** 5 · **Inherent:** 15 — High

**Controls:** authorization; data segregation; prompt/input controls; output filtering; logging; security testing.

## 33. Enterprise Risk Register

| Risk ID | System | Risk | Domain | L | I | Score | Level |
|---|---|---|---|---|---|---|---|
| R-001-01 | Customer Service | Hallucination | Model | 3 | 4 | 12 | High |
| R-001-02 | Customer Service | Data disclosure | Privacy/Security | 3 | 5 | 15 | High |
| R-002-01 | Fraud Detection | False positives | Model/Fairness | 3 | 5 | 15 | High |
| R-002-02 | Fraud Detection | Model drift | Model | 3 | 4 | 12 | High |
| R-005-01 | Recruitment | Biased ranking | Fairness/Legal | 4 | 5 | 20 | Critical |
| R-005-02 | Recruitment | Privacy exposure | Privacy | 3 | 5 | 15 | High |
| R-005-03 | Recruitment | Automation bias | Human Oversight | 4 | 4 | 16 | High |
| R-009-01 | Credit | Inaccurate recommendation | Model | 3 | 5 | 15 | High |
| R-009-02 | Credit | Unfair outcomes | Fairness | 3 | 5 | 15 | High |
| R-006-01 | Cyber Assistant | Security data exposure | Cybersecurity | 3 | 4 | 12 | High |
| R-007-01 | Marketing | Inappropriate profiling | Privacy/Fairness | 3 | 4 | 12 | High |
| R-008-01 | Knowledge Search | Access leakage | Security | 2 | 4 | 8 | Moderate |
| R-010-01 | Document Processing | Incorrect extraction | Operational | 3 | 3 | 9 | Moderate |

## 34. Risk Acceptance

Risk acceptance requires: risk ID; system ID; risk statement; residual score; risk owner; business justification; compensating controls; approval; expiry/review date.

Risk acceptance must not be used to bypass mandatory legal or regulatory requirements.

## 35. Exception Management

An exception is required when: a required control cannot currently be implemented; assessment completion is delayed; temporary operation outside policy is necessary; approved architecture cannot be followed.

Every exception must have: business justification; risk statement; compensating controls; owner; expiry; approval.

## 36. Monitoring

**Technical:** performance; latency; availability; model drift; error rates; security events.

**AI risk:** hallucination rate; fairness indicators; human override rate; adverse outcomes; data-quality changes; confidence/uncertainty; inappropriate outputs.

**Governance:** assessment status; overdue reviews; open risks; evidence completeness; control-test results; exceptions.

## 37. Shadow AI Discovery

Northstar should not rely only on voluntary registration.

**Potential discovery sources:** procurement records; SaaS inventories; cloud accounts; API gateway data; identity logs; security monitoring; DLP alerts; expense records; employee surveys; vendor inventories; architecture reviews.

The objective is to identify material AI use while respecting privacy and employment requirements.

## 38. Third-Party AI Risk

The inventory must capture: provider; product; model; processing location; retention; training/data-use terms; subprocessors; security assurance; incident notification; model-change process; continuity; exit strategy.

Third-party operation does not eliminate Northstar's accountability.

## 39. Generative AI Inventory Extension

For GenAI systems additionally capture: foundation model; provider; model version; prompt architecture; RAG; vector store; tools/plugins; external actions; data retention; training/data-use terms; output validation; prompt-injection testing; sensitive-data controls; model-change notifications.

NIST's Generative AI Profile was published in July 2024 as a companion resource to AI RMF 1.0 for GenAI-specific risk management.

## 40. Regulatory Considerations

The inventory should record: jurisdiction; sector; privacy requirements; employment requirements; consumer protection; financial-services obligations; AI-specific requirements; contractual obligations.

Where the EU AI Act applies, Article 9 requires a risk-management system for high-risk AI systems and describes it as a continuous iterative process across the lifecycle. Legal/compliance teams must determine applicability for the specific system and context.

## 41. Evidence Matrix

| Activity | Evidence | Owner | Frequency |
|---|---|---|---|
| AI registration | Inventory record | AI Governance | Per system |
| Classification | Classification record | AI Governance | Per system |
| Risk assessment | Assessment report | Risk Owner | Per assessment |
| Impact assessment | Impact assessment | Business/Compliance | As applicable |
| Security review | Security assessment | Security | As required |
| Privacy review | Privacy assessment | Privacy | As required |
| Model validation | Validation report | Model Risk | Tier 3/4 |
| Vendor review | Due diligence | Procurement/Risk | Onboarding + trigger |
| Approval | Decision record | Approval authority | Before deployment |
| Monitoring | Monitoring report | Technical Owner | Continuous/periodic |
| Reassessment | Updated assessment | Risk Owner | Periodic/trigger |
| Exception | Exception record | Risk Owner | As required |
| Incident | Incident record | Security/Governance | As required |

## 42. Executive KPIs

| KPI | Formula | Target |
|---|---|---|
| Inventory coverage | Registered AI Systems / Estimated AI Systems × 100 | ≥ 95% |
| Owner coverage | Systems with owners / Registered systems × 100 | 100% |
| Current assessment coverage | Systems with current assessments / Registered systems × 100 | ≥ 95% |
| High-risk approval coverage | High-risk systems with required approval / High-risk systems × 100 | 100% |
| Overdue assessment rate | — | < 5% |
| Evidence completeness | — | ≥ 95% |
| Remediation timeliness | Risks remediated by due date / Risks due × 100 | ≥ 90% |

## 43. Executive Dashboard

Leadership should see:

- **Inventory** — total AI systems; business-unit distribution; production vs pilot; internal vs third-party.
- **Risk** — Tier 1/2/3/4 distribution; critical risks; high risks; top risk domains.
- **Governance** — owner coverage; assessment coverage; approval coverage; overdue assessments.
- **Assurance** — evidence completeness; control testing; open findings.
- **Change** — model changes; vendor changes; reassessment triggers.
- **Incidents** — AI incidents; severity; open/closed; closure time.

## 44. NIST AI RMF Mapping

| Project Capability | AI RMF Function |
|---|---|
| AI policy | GOVERN |
| Inventory | GOVERN |
| Ownership | GOVERN |
| Intended purpose | MAP |
| Stakeholders | MAP |
| Impact assessment | MAP |
| Risk identification | MAP |
| Testing | MEASURE |
| Performance metrics | MEASURE |
| Fairness testing | MEASURE |
| Security testing | MEASURE |
| Risk treatment | MANAGE |
| Risk acceptance | MANAGE |
| Remediation | MANAGE |
| Monitoring | MEASURE/MANAGE |
| Reassessment | GOVERN/MAP/MEASURE/MANAGE |

NIST describes GOVERN as cross-cutting and emphasizes continuous risk management across the AI lifecycle.

## 45. ISO/IEC 42001 Alignment

This project supports an AI management-system approach through: defined governance; AI inventory; risk and impact assessment; documented ownership; lifecycle management; monitoring; evidence; corrective action; continual improvement.

*This portfolio does not reproduce copyrighted ISO text.*

## 46. Definition of Done

- [x] Fictional organization defined.
- [x] AI governance problem defined.
- [x] Inventory architecture defined.
- [x] Intake process defined.
- [x] Four-tier classification defined.
- [x] 5×5 risk methodology defined.
- [x] Impact assessment defined.
- [x] Ten AI systems created.
- [x] Risk register created.
- [x] High-risk systems assessed.
- [x] Risk treatment defined.
- [x] Approval workflow defined.
- [x] Evidence requirements defined.
- [x] Reassessment triggers defined.
- [x] Monitoring defined.
- [x] Executive KPIs defined.
- [x] NIST AI RMF mapping defined.
- [x] ISO/IEC 42001 alignment defined.
- [x] GenAI extension defined.
- [x] Regulatory considerations defined.

## 47. Proposed Repository Structure

```
project-2-ai-risk-assessment-inventory/
├── README.md
├── docs/
│   ├── Project_2_Enterprise_AI_Risk_Assessment.md
│   ├── AI_Risk_Methodology.md
│   ├── AI_Impact_Assessment_Methodology.md
│   └── Framework_Mapping.md
├── inventory/
│   ├── AI_Inventory.csv
│   └── Sample_AI_System_Records.md
├── risk-register/
│   ├── AI_Risk_Register.csv
│   └── Risk_Assessment_Workpaper.md
├── assessments/
│   ├── Recruitment_Screening_Assessment.md
│   ├── Credit_Decision_Assessment.md
│   ├── Fraud_Detection_Assessment.md
│   └── Customer_Service_GenAI_Assessment.md
├── templates/
│   ├── AI_Intake_Form.md
│   ├── AI_System_Record.md
│   ├── AI_Risk_Assessment.md
│   └── AI_Impact_Assessment.md
└── evidence/
    └── Evidence_Matrix.md
```

### Professional Capability Demonstrated

**AI Governance** — inventory governance; lifecycle governance; accountability; approval.

**AI Risk** — identification; scoring; impact assessment; treatment; residual risk.

**AI GRC** — evidence; controls; assurance; regulatory considerations; executive reporting.

**Cybersecurity** — data protection; IAM; secure architecture; third-party risk; monitoring; incident management.

## 48. Final Governance Traceability

```
AI SYSTEM
    ↓
BUSINESS PURPOSE
    ↓
OWNER
    ↓
DATA
    ↓
AFFECTED STAKEHOLDERS
    ↓
RISK CLASSIFICATION
    ↓
RISK ASSESSMENT
    ↓
IMPACT ASSESSMENT
    ↓
CONTROLS
    ↓
EVIDENCE
    ↓
APPROVAL
    ↓
MONITORING
    ↓
REASSESSMENT
```

The key outcome is that the inventory is not merely a spreadsheet. It becomes the central governance record connecting **AI assets, owners, risks, controls, evidence, approvals and ongoing monitoring**.
