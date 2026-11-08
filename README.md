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

<a id="project-at-a-glance"></a>
## 1. Project at a glance
**Group members**: Group‑E members

> [!NOTE]
> This report documents our evaluation of the XJTLU internal AI‑Agent major‑selection chatbot for Year‑1 undergraduate students.

This project evaluates the XJTLU internal AI‑Agent major‑selection chatbot for Year‑1 undergraduate students.
Originally we planned task‑based usability testing with three standardized tasks for objective timing and success metrics.
To better capture users’ subjective attitudes and perceived trust toward this AI tool, the main formal data collection was adjusted to an online questionnaire‑based mixed‑method survey.
We collected demographic background, awareness and usage experience, standardized SUS usability scale, trust scale, multiple‑choice comparative questions and open‑ended qualitative feedback.
The study aims to understand user perception, strengths, pain‑points and improvement directions for this AI tool.

Evaluated system: XJTLU Major‑Selection AI Assistant (internal AI‑Agent platform).

<a id="problem-motivation-and-research-questions"></a>
## 2. Problem, motivation and research questions
### Context & intended users
🎯 Target users: XJTLU Year‑1 students who need to make major‑selection decisions at the end of Year 1.

Major‑related information is scattered across university official websites, social media and informal advice from senior students. Students spend substantial manual effort gathering and comparing major‑related information.

### Research Questions
1. Can this AI chatbot help Year‑1 XJTLU students retrieve accurate and clear information for major selection?
2. Can users efficiently get answers to their major‑related questions by interacting with this AI assistant?
3. Do Year‑1 students trust the AI‑generated answers and consider this tool usable for their major choice?

> [!IMPORTANT]
> Findings are limited to XJTLU internal AI‑Agent major‑selection assistant, and our sample of participating students. Results cannot be generalised to external large‑language‑models or other‑university student populations.

<a id="background-and-related-work"></a>
## 3. Background and related work
AI chatbots are increasingly deployed within higher‑education contexts to support student information‑seeking. For high‑stakes decisions such as university major selection, usability is not limited to interface experience; perceived trust and concerns about AI hallucination and outdated factual information become critical factors for adoption.

Many existing HCI usability studies adopt task‑based usability testing combining objective behavioural metrics (task completion time, success rate) and subjective standardized questionnaires such as the System Usability Scale (SUS). Questionnaire‑based surveys are also widely used to capture self‑reported attitudes, perceived advantages and barriers from real‑world users.

**Research gap**: Few empirical evaluations focus on university‑internal closed AI‑agent systems built for undergraduate major‑selection workflows. Many evaluations measure usability alone, without jointly investigating perceived trust and concerns over factual accuracy.

✅ Rationale for method choice: We adopted a mixed‑methods approach combining quantitative survey scales and open‑ended qualitative feedback, to capture both numerical attitude measurements and rich user suggestions.

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
> Important note: Q14 comparative items are categorical single‑choice questions (MSA / Traditional search / Cannot judge), not paired Likert ratings. Each respondent selected which option performed better on each dimension, respondents **did not give separate 1‑5 ratings for MSA and traditional search respectively**.

### Participants & Sampling
Sampling method: convenience sampling of XJTLU students.
Inclusion criteria: XJTLU undergraduate students experiencing major‑selection process.
Formal total valid sample N=12.
Among all participants:
- Only **4 participants reported they had used the MSA AI assistant**
- 8 participants had never used MSA.

> Therefore SUS, trust, perceived‑usefulness and AI‑error‑perception questions are only valid for the subsample of 4 users who had real experience with the tool.

### Study procedure
1. Participants read online information sheet and gave digital informed consent via checkbox before accessing questionnaire items.
2. Screening question confirmed participant meets inclusion criteria.
3. Questionnaire collected demographics, prior awareness and usage experience of MSA AI assistant.
4. Comparative single‑choice block Q14: participants selected which approach performed better on each dimension (MSA / Traditional search / Cannot judge).
5. Standard System Usability Scale (SUS), trust‑related scale, multiple‑choice questions on advantages / barriers / improvement needs (only visible for participants who had used MSA).
6. Open‑ended text questions for qualitative feedback.

### Measures
- Demographic and background items
- Awareness and usage history of MSA AI assistant
- Q14 categorical comparative single‑choice items
- Standard System Usability Scale (SUS, 10‑item) → only for participants who had used MSA
- Custom trust scale (4 items) → only for participants who had used MSA
- Multiple‑choice items for perceived strengths, barriers and improvement requirements
- Open‑ended free‑text questions for qualitative feedback

### Ethics, consent and bias mitigation
- Digital informed consent (checkbox‑based consent in questionnaire; full information‑sheet and consent‑form document stored in supplementary‑materials zip package).
- All participant responses fully anonymised; no identifiable personal information published on web‑report or GitHub pages.
- Participants could withdraw at any time without penalty.
- AI outputs were explicitly stated as for‑reference‑only and not official university advice.

> [!IMPORTANT]
> ### Deviation from original plan
> Originally we planned controlled task‑based usability‑testing with objective task‑timing metrics and repeated‑measures ANOVA for the three predefined tasks.
> To better collect users’ subjective attitudes and trust perception, our formal main‑study was changed to questionnaire‑only survey. Task‑level timing and task‑success behavioural metrics were **not collected for main study**, so repeated‑measures ANOVA was not performed for the main dataset. Pilot N=5 data was only used for material iteration.

<a id="data-preparation-and-analysis"></a>
## 5. Data preparation and analysis
Data were exported from survey tool as CSV and imported into IBM SPSS Statistics for quantitative analysis.

### Quantitative data processing
1. Data‑cleaning: filter invalid responses.
We split participants into two subgroups: participants who had used MSA AI assistant (n=4) vs participants who never used MSA (n=8).
Not‑applicable responses from non‑users were preserved and excluded from MSA‑specific scales such as SUS and trust scale.
2. Scale reliability check: Cronbach’s Alpha was calculated for SUS and trust scale.
3. Only descriptive statistics were computed: frequencies, percentages, mean, standard deviation, min‑max values.
> [!IMPORTANT]
> The comparative Q14 items are categorical single‑choice questions, not paired continuous Likert‑scale ratings. **No paired‑samples t‑test or Wilcoxon signed‑rank test can be performed for these items**.
> Due to the very small valid subsample of actual MSA users (n=4), **no inferential statistical tests (correlation, t‑test, ANOVA) were conducted**. All quantitative results are purely descriptive.

### Qualitative data processing
Open‑ended questionnaire textual responses were anonymised and manually analysed using **thematic analysis**. Responses were open‑coded and aggregated into high‑level themes including perceived strengths, accuracy‑related concerns, user‑interaction barriers and improvement‑suggestions. No NVivo software was used for this small sample.

<a id="findings"></a>
## 6. Findings
### Descriptive sample overview (Total N=12)
- Year distribution: Year1 n=8 (66.7%), Year2 n=2 (16.7%), Other n=2 (16.7%)
- Major‑decision status: Already decided major n=8 (66.7%), Narrowed to 2‑3 options n=3 (25.0%), No idea yet n=1 (8.3%)
- Heard about MSA: Heard n=5 (41.7%), First‑time hearing n=6 (50.0%), Not sure n=1 (8.3%)
- Used MSA assistant: Used n=4 (33.3%), Never used n=8 (66.7%)

#### Q14 comparative categorical results (N=12 total respondents, single‑choice: which works better)
1. Ease of use: MSA=8, Traditional search=2, Cannot judge=2
2. Speed / Quickness: MSA=4, Traditional search=4, Cannot judge=4
3. Accuracy: MSA=6, Traditional search=4, Cannot judge=2
4. Clarity of answers: MSA=7, Traditional search=3, Cannot judge=2
5. Information source credibility: MSA=4, Traditional search=5, Cannot judge=3
6. Intention to reuse: MSA=7, Traditional search=4, Cannot judge=1

Perceived overall better method for major‑selection (Q15):
MSA n=7 (58.3%), Traditional search n=4 (33.3%), About the same n=1 (8.3%)

### Scale results (Only for participants who actually used MSA, valid subsample n=4)
> Scale reliability:
> - SUS (10 items): Cronbach’s α = **0.906** (excellent internal consistency)
> - Trust scale (4 items): Cronbach’s α = **0.956** (excellent internal consistency)

Descriptive for scales (n=4):
- SUS total score: Mean = 45.83, SD =7.71 (range 27.5‑55.0)
- Trust total score: Mean = 2.39, SD =1.18 (1‑5 scale)

Additional perceptions among MSA‑users:
- Q20 perceived factual accuracy: Mostly accurate n=2; Partly accurate n=5; Mostly inaccurate n=2; Never checked n=1; Not applicable n=2
- Q22 perceived AI‑error occurrence: Observed errors more‑than‑once n=4; Observed once n=3; Not sure n=3; Not applicable n=2

### Qualitative thematic findings
From open‑text responses, four main themes emerged:
- ✅ **Strength**: Direct information retrieval, natural‑language interaction is convenient for quick look‑up of major facts.
- ⚠️ **Accuracy risk**: Worries about outdated major‑requirement information and lack of traceable official source references within AI replies.
- 🧩 **Interaction barrier**: Uncertainty on constructing good prompts to obtain high‑quality answers; VPN‑access barrier limits usage.
- 💡 **Improvement suggestion**: Add example prompt buttons, prominent non‑official disclaimer, links pointing to XJTLU official major documents.

<a id="discussion-limitations-and-recommendations"></a>
## 7. Discussion, limitations and recommendations
### Interpretation of results
From categorical comparative choices, a majority of participants selected MSA‑AI as the better option for ease‑of‑use, answer clarity and reuse intention. Meanwhile more participants judged traditional search to have higher source credibility.

For the small subsample of users who have interacted with MSA, SUS average score sits in the lower‑marginal acceptable range; trust score is moderate. Many participants reported observing factual errors from the AI output.
This aligns with HCI literature stating that for high‑stakes decisions such as major‑selection, factual trust is equally important as interface usability.

Our original pilot usability‑test observation also echoed this point: the personalised GPA‑based major‑recommendation task had high failure‑rate, showing factual‑recommendation functions are fragile for this system.

### Limitations
- Critical sampling limitation: Out of total N=12, only **4 participants have real hands‑on experience with the MSA AI assistant**. All SUS and trust‑scale results are based on this tiny subsample, interpretation must be treated with great caution. Findings cannot be generalised to the full Year‑1 student population.
- Main‑study is questionnaire‑based self‑report survey, without controlled objective task‑performance (time / success‑rate) behavioural measurements. Self‑reported attitudes may diverge from real‑world actual usage behaviour.
- Q14 uses categorical single‑choice comparison instead of separate Likert‑ratings for each tool; we cannot perform statistical comparison of continuous scores between MSA and traditional search.
- Potential response bias in self‑reported questionnaire ratings.

> [!NOTE]
> Pilot‑test N=5 only served for material iteration and is not formal evidence for our conclusions.

### Evidence‑based recommendations
Each recommendation is supported by collected participant feedback:
1. Add example prompt buttons on chat‑interface, helping users construct better natural‑language queries (from interaction‑barrier theme).
2. Add prominent disclaimer on chat‑webpage: AI outputs are not official XJTLU advice, for reference‑only (from accuracy‑risk theme).
3. Where possible, make AI assistant explicitly reference or link to official university major‑document sources to improve perceived source‑credibility (from comparative Q14 source‑credibility results and qualitative feedback).
4. Further iteration on personalised GPA‑based major‑recommendation logic, since pilot usability‑test found high failure‑rate for this task.

> [!NOTE]
> Above points are evidence‑based suggestions, not proven causal conclusions from this study.


