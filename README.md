# 🎓 XJTLU Major Selection AI Assistant
**Group‑E**

> 📄 ADS401 Web Report | GitHub‑Pages single‑page report

🔗 [Open our XJTLU Major Selection AI Chatbot (XJTLU VPN / Campus Network Needed)](https://aiagent.xjtlu.edu.cn/product/llm/mall/application/d40ej496i3uelisjb0q0/chat)

---
## 🔗 Navigation
- [Project at a glance](#project-at-a-glance)
- [Problem, motivation and research questions](#problem-motivation-and-research-questions)
- [Background and related work](#background-and-related-work)
- [System and evaluation design](#system-and-evaluation-design)
- [Data preparation and analysis](#data-preparation-and-analysis)
- [Findings](#findings)
- [Discussion, limitations and recommendations](#discussion-limitations-and-recommendations)
- [Transparency and references](#transparency-and-references)

<a id="project-at-a-glance"></a>
## 1. Project at a glance
**Group members**: Group‑E members

**Project summary**
This project evaluates the XJTLU internal AI‑Agent major‑selection chatbot for Year‑1 undergraduate students.
Originally we planned task‑based usability testing with three standardized tasks for objective timing and success metrics. Due to practical constraints including VPN‑access barriers for the internal AI platform, the main formal data collection was adjusted to an online questionnaire‑based mixed‑method survey. We collected quantitative Likert‑scale ratings including SUS usability, trust, and direct subjective comparison between the AI assistant and traditional major‑information‑search channels, alongside open‑ended qualitative feedback. The study aims to understand user perception, strengths, pain‑points and improvement directions for this AI tool.

Evaluated system: XJTLU Major‑Selection AI Assistant (internal AI‑Agent platform).

<a id="problem-motivation-and-research-questions"></a>
## 2. Problem, motivation and research questions
### Context & intended users
Target users: XJTLU Year‑1 students who need to make major‑selection decisions at the end of Year 1.
Major‑related information is scattered across university official websites, social media and informal advice from senior students. Students spend substantial manual effort gathering and comparing major‑related information.

### Research Questions
1. Can this AI chatbot help Year‑1 XJTLU students retrieve accurate and clear information for major selection?
2. Can users efficiently get answers to their major‑related questions by interacting with this AI assistant?
3. Do Year‑1 students trust the AI‑generated answers and consider this tool usable for their major choice?

### Scope of claims
Findings are limited to XJTLU internal AI‑Agent major‑selection assistant, and our sample of participating Year‑1 students. Results cannot be generalised to external large‑language‑models or other‑university student populations.

<a id="background-and-related-work"></a>
## 3. Background and related work
AI chatbots are increasingly deployed within higher‑education contexts to support student information‑seeking. For high‑stakes decisions such as university major selection, usability is not limited to interface experience; perceived trust and concerns about AI hallucination and outdated factual information become critical factors for adoption.

Many existing HCI usability studies adopt task‑based usability testing combining objective behavioural metrics (task completion time, success rate) and subjective standardized questionnaires such as the System Usability Scale (SUS). Questionnaire‑based surveys are also widely used to capture self‑reported attitudes, perceived advantages and barriers from real‑world users.

**Research gap**: Few empirical evaluations focus on university‑internal closed AI‑agent systems built for undergraduate major‑selection workflows. Many evaluations measure usability alone, without jointly investigating perceived trust and concerns over factual accuracy.

Rationale for method choice: We adopted a mixed‑methods approach combining quantitative survey scales and open‑ended qualitative feedback, to capture both numerical attitude measurements and rich user suggestions.

<a id="system-and-evaluation-design"></a>
## 4. System and evaluation design
### System description
The evaluated system is an internal XJTLU AI‑Agent chatbot built to answer major‑selection‑related natural‑language queries. It supports queries on major GPA entry thresholds, prerequisite courses, workload and career‑prospect information. VPN or campus network access is mandatory.

### Original planned usability‑test tasks (Pilot‑test only, N=5)
> These three standardized controlled tasks were only executed in our small pilot study for study‑material refinement, not in the formal questionnaire‑based main study:
1. Task1: Ask AI for HCI major GPA requirements and prerequisite courses
2. Task2: Given GPA=70, request AI to recommend suitable majors
3. Task3: Request AI to compare workload and career prospects for Computer Science and HCI

> Pilot observation (N=5): Task2 (GPA‑based major recommendation) showed highest failure rate; Task1 (single‑major requirement lookup) had shortest average completion time. Pilot sample was too small for inferential statistics and only used for iterative refinement of questionnaire and procedure.

### Formal main‑study design
Formal data collection adopted **online questionnaire‑based cross‑sectional survey (non‑experimental)**.
Within‑subject comparison was implemented via questionnaire items: every respondent provided subjective Likert ratings for **both the MSA AI assistant AND traditional major‑information search channels**.

### Participants & Sampling
Sampling method: convenience sampling of XJTLU Year‑1 students.
Inclusion criteria: Year‑1 students undergoing major‑selection process.
Formal valid sample N=12.

### Study procedure
1. Participants read online information sheet and gave digital informed consent via checkbox before accessing questionnaire items.
2. Screening question confirmed participant meets inclusion criteria.
3. Questionnaire collected demographics, prior awareness and usage experience of MSA AI assistant.
4. Within‑subject rating block Q14: participants rated both MSA‑AI and traditional search on ease, speed, accuracy, clarity, source‑credibility, intention‑to‑reuse.
5. SUS System Usability Scale, trust‑related Likert‑items, multiple‑choice questions on advantages / barriers / improvement needs.
6. Open‑ended text questions for qualitative feedback.

### Measures
1. Demographic and background items
2. Within‑subject paired Likert‑ratings for MSA‑AI vs traditional search (5‑point scale, Q14 series)
3. Standard System Usability Scale (SUS, 10‑item) for participants who had used MSA
4. Custom trust‑related 5‑point Likert‑scale items
5. Multiple‑choice items for perceived strengths, barriers and improvement requirements
6. Open‑ended free‑text questions for qualitative feedback

### Ethics, consent and bias mitigation
- Digital informed consent (checkbox‑based consent in questionnaire; full information‑sheet and consent‑form document stored in supplementary‑materials zip package).
- All participant responses fully anonymised; no identifiable personal information published on web‑report or GitHub pages.
- Participants could withdraw at any time without penalty.
- AI outputs were explicitly stated as for‑reference‑only and not official university advice.

### Deviation from original plan
Originally we planned controlled task‑based usability‑testing with objective task‑timing metrics and repeated‑measures ANOVA for the three predefined tasks.
Due to practical recruitment constraints including VPN‑access restrictions for the campus‑internal AI‑Agent platform, formal main‑study was changed to questionnaire‑only survey. Task‑level timing and task‑success behavioural metrics were **not collected for main study**, so repeated‑measures ANOVA was not performed for the main dataset. Pilot N=5 data was only used for material iteration.

<a id="data-preparation-and-analysis"></a>
## 5. Data preparation and analysis
Data were exported from survey tool as CSV and imported into IBM SPSS Statistics for quantitative analysis.

### Quantitative data processing
1. Data‑cleaning: filter invalid responses. Participants were split into subgroups: participants who had used MSA AI assistant vs participants who never used MSA. Not‑applicable responses from non‑users were preserved and excluded from MSA‑specific scales such as SUS.
2. SUS scoring: Initial SPSS compute syntax contained arithmetic error. SUS total scores were **recalculated following official standard SUS formula**:
    - Odd‑numbered items: raw score minus one
    - Even‑numbered reversed items: five minus raw score
    - Sum all transformed values and multiply by 2.5 to get final 0‑100 SUS score.
3. Descriptive statistics: frequencies, percentages, mean, standard deviation, min‑max values for all scale items.
4. Within‑subject comparison: Shapiro‑Wilk test showed violation of normality assumption for Likert items. Therefore non‑parametric **Wilcoxon signed‑rank test** was prioritised over paired‑samples t‑test for comparing subjective ratings between MSA‑AI and traditional‑search channels. Effect sizes were reported.
5. Independent‑samples comparison between gender groups on SUS total score.

> Inferential repeated‑measures one‑way ANOVA for three usability tasks was not applicable for main‑study dataset because task‑level timing metrics were not collected in questionnaire survey.

### Qualitative data processing
Open‑ended questionnaire textual responses were anonymised and manually analysed using **thematic analysis**. Responses were open‑coded and aggregated into high‑level themes including perceived strengths, accuracy‑related concerns, user‑interaction barriers and improvement‑suggestions. No NVivo software was used for this small sample.

<a id="findings"></a>
## 6. Findings
### Descriptive sample overview (N=12)
Gender distribution: Female n=7 (58.3%), Male n=5 (41.7%).
For Q15 which method is better for major‑selection: 75% (9/12) participants regarded MSA‑AI as better, 8.3% preferred traditional search, 16.7% considered both approximately equal.

### Within‑subject subjective comparison (Wilcoxon signed‑rank test)
Participants rated MSA‑AI assistant and traditional major‑information search on identical dimensions:
1. **Speed (Q14b)**: MSA‑AI (M=4.00, SD=1.128) was rated significantly higher than traditional search (M=2.58, SD=0.515), Z=-2.404, p=0.016. Participants perceived AI as faster for retrieving major‑selection information.
2. **Source credibility (Q14e)**: Traditional search (M=4.08, SD=0.289) scored significantly higher than MSA‑AI (M=2.25, SD=0.622), Z=-3.169, p=0.002. Users had strong concerns regarding the provenance and factual source of AI‑generated answers.
3. **Intention to reuse (Q14f)**: MSA‑AI (M=3.67, SD=1.073) had significantly higher reuse intention than traditional search (M=2.75, SD=0.452), Z=-1.930, p=0.054 (marginal significance).

No statistically‑significant difference was found for perceived ease of use, factual accuracy and answer clarity between two channels.

### SUS usability score
After correction with standard SUS formula, mean SUS total score for participants who used MSA was M=70.63 (SD=20.67). This falls within the "good‑acceptable" SUS usability range.
Independent‑samples comparison showed no statistically‑significant SUS‑score difference between female and male participants (p=0.288).

### Qualitative thematic findings
From open‑text responses, four main themes emerged:
1. ✅ Strength theme: Direct, fast information retrieval; convenient natural‑language interaction.
2. ⚠️ Accuracy‑risk theme: Worries about outdated major requirements, AI hallucination, lack of cited official sources inside AI replies.
3. 🧩 Interaction‑barrier theme: Uncertainty on how to frame good prompts for the AI chatbot.
4. 💡 Improvement theme: Request for example prompt buttons, prominent official‑source references, clear disclaimer about non‑official nature of AI outputs.

<a id="discussion-limitations-and-recommendations"></a>
## 7. Discussion, limitations and recommendations
### Interpretation of results
Participants subjectively perceived the MSA AI assistant as a fast‑acting tool for major‑selection queries and reported higher willingness to reuse it. However, a critical weakness is low perceived source‑credibility: students do not trust the factual provenance of AI‑generated answers, even though overall SUS usability is acceptable. This aligns with HCI literature stating that for high‑stakes decisions such as major‑selection, factual trust is as important as interface usability.

Our original pilot usability‑test observation also echoed this point: the personalised GPA‑based major‑recommendation task had high failure‑rate, showing factual‑recommendation functions are fragile for this system.

### Limitations
1. Sampling: convenience‑sampling small sample N=12, limited generalisability to full Year‑1 student population.
2. Main‑study is questionnaire‑based self‑report survey, without controlled objective task‑performance (time / success‑rate) behavioural measurements. Self‑reported attitudes may diverge from real‑world actual usage behaviour.
3. Access constraint: MSA AI assistant is campus‑VPN‑locked internal system, external participants cannot take part.
4. Potential response bias in self‑reported questionnaire ratings.

> Pilot‑test N=5 only served for material iteration and is not formal evidence for our conclusions.

### Evidence‑based recommendations
Each recommendation is supported by collected participant feedback:
1. Add example prompt buttons on chat‑interface, helping users construct better natural‑language queries (from interaction‑barrier theme).
2. Add prominent disclaimer on chat‑webpage: AI outputs are not official XJTLU advice, for reference‑only (from accuracy‑risk theme).
3. Where possible, make AI assistant explicitly reference or link to official university major‑document sources to improve perceived source‑credibility (from source‑credibility quantitative result and qualitative feedback).
4. Further iteration on personalised GPA‑based major‑recommendation logic, since pilot usability‑test found high failure‑rate for this task.

> Distinction: above points are evidence‑based suggestions, not proven causal conclusions from this study.

<a id="transparency-and-references"></a>
## 8. Transparency and references
### Group‑member contribution statement
> Write down each group‑member’s responsibilities here: e.g. participant recruitment, questionnaire design, SPSS analysis, web‑report writing, poster‑design.

### AI‑use statement
[1] DeepSeek V3.1, available at https://www.deepseek.com. Used for grammatical proofreading and formatting suggestions only, no substantive content generation.

### Data‑and‑material‑availability statement
Raw participant survey responses, SPSS `.sav` dataset, SPSS output `.spv` file, questionnaire drafts, information‑sheet and consent‑form documents, interview‑related materials are packaged inside `ADS401_GroupE_SupplementaryMaterials.zip` for submission.
**No raw identifiable participant data is published on this GitHub web‑report or GitHub repository.** Only aggregated summary statistics and anonymised thematic quotes are presented on this webpage.

### Acknowledgements
We thank XJTLU AI‑Agent platform for providing access to the major‑selection AI assistant system.

### References
> Insert IEEE‑format numbered references for HCI / SUS / AI‑trust‑in‑education literature here.

---
✨ End of Web Report
