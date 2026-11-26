# ADS401 Report: XJTLU Major‑Selection AI Assistant

> [!NOTE]
> **Reading time ≈10 minutes** | Group project for ADS401 Evaluation Methods and Statistics

## 1. Project at a glance

**Title**: XJTLU Major Selection AI Assistant

**Group Members & Student ID**:
- Sun Mengyue, 2686020
- Lin Peiyi, 2684871
- Liu Kaimeng, 2684863
- Zhang Chenjia, 2692591

### Project Summary
This project evaluates the XJTLU internal AI‑Agent major‑selection chatbot for Year‑1 undergraduate students. Originally we planned task‑based usability testing with three standardized tasks and objective timing metrics. To better capture users’ subjective attitudes and trust toward this AI tool, our main formal data collection was adjusted to an online questionnaire‑based mixed‑method survey. We collected demographic background, awareness and usage experience, the standard SUS usability scale, trust ratings, comparative multiple‑choice questions and open‑ended qualitative feedback. This study aims to understand users’ perceptions, strengths, pain points and potential improvement directions for the AI assistant.

**Evaluated System**: XJTLU Major‑Selection AI Assistant (internal AI‑Agent platform).

**System Link**: https://aiagent.xjtlu.edu.cn/product/llm/mall/application/d40ej496i3uelisjb0q0/chat

---

## 2. Problem, motivation and research questions

### Intended users and context
**Target users**: XJTLU Year‑1 students who are about to make their major‑selection decisions.

Major‑related information is currently scattered across official university websites, social media groups and informal advice from senior students. Students spend a lot of time manually gathering and comparing information. An AI assistant has the potential to streamline this process.

### Research Questions
1. Can this AI chatbot help Year‑1 XJTLU students retrieve accurate and clear information for major selection?
2. How efficiently can users get answers to their major‑selection‑related questions by interacting with this AI assistant?
3. Do Year‑1 students trust the AI‑generated answers and consider this tool usable for their major choice?

> [!CAUTION]
> **Scope of claims**: Our findings are limited to this specific internal XJTLU AI‑Agent and our recruited sample. Results cannot be generalized to external large language models or students from other universities.

---

## 3. Background and Related Work

### 3.1 How students choose a major
Picking a major is not a one‑off simple decision. Mwantimwa [1] found that first‑year students’ major choices are shaped by personal interests and abilities as well as external factors such as employment prospects, family expectations and social reputation. Students without sufficient career information tend to make less rational decisions. Porter and Umbach [2] apply the person‑environment fit perspective: the match between a student and an academic programme affects both choice and persistence. A good supporting tool should not simply “give a final answer”, but provide comparable, reliable information for students to judge by themselves.

### 3.2 AI advising tools in education
Generative AI has become widely available, bringing both benefits and risks. Crompton and Burke [3] reviewed 44 studies and pointed out that AI can provide fast and personalised feedback, yet hallucination and factual inaccuracy remain serious concerns. This is especially critical for official university guidance. Zylowski et al. [4] built an LLM‑based educational pathway recommendation assistant and compared it with other forms of support. Their work shows that a natural‑language chat interface does not automatically guarantee trust or good explainability. There is still a research gap: few evaluations focus specifically on an in‑house university AI agent for first‑year students’ major selection.

### 3.3 Trust in algorithmic advice
People’s attitudes toward algorithmic advice are mixed. Logg et al. [5] found evidence of “algorithm appreciation”: under some conditions, people may trust algorithms as much as, or even more than, human experts. On the other hand, Dietvorst et al. [6] demonstrated “algorithm aversion”: once people see an algorithm make a mistake, they quickly lose confidence. Zhang, Liao and Bellamy [7] found that showing confidence information can help, but it cannot fully guarantee trust. Bo et al. [8] also found that simple reliability disclaimers can reduce over‑reliance on AI outputs. For our study, this means trust should be measured separately from satisfaction or perceived clarity.

### 3.4 Why we chose our measures
Our design draws on Davis’s Technology Acceptance Model [9], where perceived usefulness and ease of use strongly predict acceptance. We use the System Usability Scale (SUS). Bangor et al. [10] established long‑standing normative benchmarks for SUS scores, and Vlachogianni et al. [11] confirmed its applicability in educational technology evaluations. We combine subjective Likert ratings with behavioural self‑reports such as conversation duration to get a richer picture than usability scores alone.

---

## 4. System and evaluation design

### 4.1 Evaluated system description
This evaluation targets the internal XJTLU Major‑Selection AI Assistant hosted on the university’s AI‑Agent platform. It is designed to answer Year‑1 students’ natural‑language questions about major selection, programme requirements, curricula and progression rules. It is intended as supplementary guidance rather than an official replacement for academic advisors or formal university documentation. Our evaluation focuses on end‑user subjective perception after interaction. The backend model weights and detailed retrieval mechanisms are outside our scope.

### 4.2 Participants, recruitment and sample‑size rationale
Participants were XJTLU Year‑1 undergraduate students facing major‑selection decisions. Recruitment took place through Year‑1 student social groups. All participants completed the online questionnaire after interacting with the AI assistant. The final sample size is N = 43, and all responses were complete and retained for analysis. Our sample size is constrained by practical recruitment limits. While classic usability testing often uses around 12 participants, our mixed‑method survey design relies on self‑reported subjective perception, trust and feedback.

### 4.3 Study procedure
We adopted an online mixed‑method survey design. Participants first read the study information and gave informed consent. They then interacted freely with the XJTLU Major‑Selection AI‑Agent for major‑selection‑related queries. After finishing their conversation, they filled out the full questionnaire. The questionnaire included demographic items, background about their major decision‑making, post‑interaction behavioural self‑reports, three custom 7‑point Likert items aligned with our research questions, a modified 10‑point SUS scale, and one open‑ended feedback question.

### 4.4 Variables and operationalisation

| Construct | Operational Measure |
|---|---|
| RQ1 Perceived clarity | Custom 7‑point Likert item (CLAR) |
| RQ2 Subjective efficiency | Custom 7‑point Likert item (EFF) |
| RQ2 Behavioural efficiency indicators | Self‑reported conversation time; self‑reported user message count; perceived task success (Useful: yes / no) |
| RQ3 User trust | Custom 7‑point Likert item (TRUST) |
| RQ3 Perceived usability | Modified 10‑point System Usability Scale total score (SUS_Total) |

### 4.5 Ethics, consent and bias mitigation
All participants provided informed consent before taking part. No identifying information such as full name or student ID was collected in the questionnaire. Participants were reminded that outputs from the AI agent are not official university advice. Responses were anonymised. The questionnaire itself did not feed participants’ personal data into the AI agent. We acknowledge potential response bias because all results are based on self‑reported experience rather than system logs.

### 4.6 Deviation from the original plan
Our original plan was controlled, task‑based usability testing with objective timing metrics. Due to practical constraints on in‑person lab recruitment, we shifted data collection to an online questionnaire‑based mixed‑method design. Participants completed self‑reported interaction instead of supervised controlled tasks. We treat this deviation explicitly as one of our limitations.

---

## 5. Data preparation and analysis

All collected responses were complete and valid. No participants were excluded, and no missing‑value imputation was required. Survey data exported from the questionnaire platform were imported into SPSS for quantitative statistical analysis.

### 5.1 Data types
- **Quantitative survey data**: demographic variables, self‑reported interaction behaviour, three custom 7‑point Likert items, modified 10‑point SUS scale.
- **Qualitative data**: open‑text improvement suggestions from the questionnaire.

### 5.2 Data pre‑processing
The SUS scale was modified from the standard 1–5 response range to a 1–10 range. Negatively phrased SUS items were reversed‑coded before computing the aggregate SUS_Total score. Our custom Likert items (EFF, TRUST and CLAR) were treated as ordinal data. Categorical variables for conversation time and perceived usefulness were kept as nominal categories for frequency analysis.

### 5.3 Selection of statistical tests
One‑sample t‑tests were used to compare Likert means against the neutral midpoint value of 4. A one‑sample t‑test compared the mean SUS_Total against the widely accepted SUS usability benchmark of 68. Descriptive frequency statistics were generated for conversation‑time categories and perceived acquisition of useful information. Exploratory subgroup descriptive comparisons were performed across four major‑decision‑driver groups; formal inferential subgroup testing was not conducted. Full SPSS outputs are available as supplementary materials.

### 5.4 Qualitative analysis
Open‑ended text responses were analysed using inductive thematic analysis in Excel. Responses were read iteratively to identify recurring themes about strengths, problems and improvement suggestions for the AI assistant. Short anonymised participant quotes are used to support the qualitative findings.

---

## 6. Findings
> [!IMPORTANT]
> All figures below are exported SPSS outputs. Questionnaire measures capture **subjective participant perception only**. Objective factual accuracy of AI outputs cannot be assessed from this survey dataset.

### 6.1 Findings for RQ1
*Can this AI chatbot help Year‑1 XJTLU students retrieve accurate and clear information for major selection?*

![Figure 1: Mean ratings of EFF, TRUST and CLAR](figures/figure1_likert_mean.png)
**Figure 1.** Mean ratings of EFF (perceived efficiency), TRUST (trust in AI answers) and CLAR (perceived clarity and timeliness). 7‑point Likert scale; the dashed horizontal line represents the neutral value of 4.

![Figure 2: Subgroup mean scores by major‑decision‑making driver](figures/figure2_subgroup_bar.png)
**Figure 2.** Mean EFF, TRUST and CLAR scores grouped by four major‑decision‑making driver subgroups.

Descriptive statistics: EFF *M* = 5.58; TRUST *M* = 5.40; CLAR *M* = 5.70. One‑sample t‑tests against the value of 4 show that all three means are significantly higher than neutral (all *p* < 0.001). CLAR (perceived clarity and timeliness) received the highest average rating, while TRUST was the lowest of the three, though still clearly above neutral.

Subgroup means remained above neutral across all four subgroups. No strong, consistent subgroup pattern was observed, and some subgroups showed large variance. These subgroup comparisons are descriptive only and not hypothesis‑driven.

> [!WARNING]
> High subjectively perceived clarity (CLAR) **does not guarantee factual accuracy** of AI‑generated content.

### 6.2 Findings for RQ2
*How efficiently can users get answers to their major‑related questions by interacting with this AI assistant?*

![Figure 3: Self‑reported conversation time frequency distribution](figures/figure3_time_frequency.png)
**Figure 3.** Frequency distribution of participants’ self‑reported conversation time with the AI assistant.

![Figure 4: Stacked bar chart: conversation time vs obtained useful information](figures/figure4_stacked_useful.png)
**Figure 4.** Stacked bar chart showing the proportion of participants who obtained subjectively useful information across different conversation‑time categories.

The modal category was 2–5 minutes. Fewer participants reported very short (< 2 min) or very long (> 10 min) conversations.
Within every time category, most participants reported obtaining useful information. Even participants with very short interactions (< 2 minutes) mostly gained subjectively useful outputs. Larger absolute counts of successful cases appeared within the 2–5 min and 5–10 min bins, matching the higher number of participants in those categories. The self‑reported behavioural evidence suggests that the AI assistant can deliver subjectively useful information without requiring extremely long interaction sessions.

### 6.3 Findings for RQ3
*Do Year‑1 students trust the AI‑generated answers and consider this tool usable for their major choice?*

![Figure 5: Boxplot of modified SUS‑Total scores](figures/figure5_sus_boxplot.png)
**Figure 5.** Boxplot of modified SUS total scores. The dashed reference line marks the common SUS usability benchmark value of 68.

RQ3 covers both trust (TRUST, already reported in RQ1 section) and system usability measured by the modified SUS_Total.
Descriptive statistics: SUS_Total *M* = 70.81, *SD* = 14.69. A one‑sample t‑test against the benchmark value of 68 yields *p* = 0.216, which is not statistically significant. Although the sample mean sits slightly above the industry benchmark, we cannot conclude that the system’s usability differs significantly from general‑purpose tool standards. The boxplot reveals wide score dispersion: participants had highly variable usability experiences.

Combined with the TRUST result (*M* = 5.40, above neutral but relatively lower than clarity), many participants accept the AI assistant for major‑selection support, yet trust and usability performance vary substantially between individuals.

### 6.4 Qualitative themes from open‑ended feedback
Recurring themes from open‑text suggestions include:
- requests for clearer citations to official sources inside AI answers;
- expectations for better handling of complex questions that compare multiple majors;
- appreciation for fast preliminary information retrieval;
- warnings about potential factual mistakes concerning university‑specific programme rules.

Selected anonymised short quotes are preserved in the supplementary materials.

---

## 7. Discussion, limitations and recommendations

### 7.1 Interpretation of findings
On average, Year‑1 students subjectively perceived the XJTLU major‑selection AI‑Agent as clear, reasonably efficient and moderately trustworthy. SUS usability scores sat slightly above the standard benchmark, but the difference was not statistically significant. Most participants reported gaining subjectively useful information within short‑to‑moderate conversation durations. However, large variance across all key measurements indicates inconsistent user experience: the AI assistant works well for some students while others hold more negative perceptions.

A key distinction emerges: participants can perceive AI output as clear, and that does not guarantee factual correctness. This reinforces the literature on algorithm appreciation and algorithm aversion: subjective perception and objective factual quality are separate dimensions [5][6]. Trust remains weaker than perceived clarity, which means building user trust should be a priority for future iterations of the agent.

### 7.2 Alternative explanations
Several alternative factors may have shaped our survey results. Participants’ prior familiarity with generative AI may have influenced both trust and usability ratings. Because the interaction tasks were self‑directed rather than standardised in a controlled lab setting, participants chose their own questions, introducing variation in task difficulty. Our exploratory subgroup results hint that students’ pre‑existing major‑decision‑making styles may moderate experience, but we cannot draw firm causal conclusions from these descriptive data alone.

### 7.3 Limitations
1. This study relies on self‑reported questionnaire data, without objective system log data or supervised controlled‑task laboratory testing, following our deviation from the original project plan.
2. We cannot evaluate the objective factual accuracy of AI answers, because participant‑agent conversation transcripts were not systematically collected and coded.
3. Recruitment relied on convenience sampling among Year‑1 XJTLU students; our sample may not fully represent the whole Year‑1 population.
4. Subgroup comparisons across major‑decision‑making groups are purely descriptive; no formal statistical inference can be drawn.
5. The SUS scale was modified from its original 1–5 response format to a 1–10 format; therefore, results cannot be directly compared against classic SUS normative datasets.
6. Findings apply only to this specific in‑house XJTLU AI‑Agent and this participant sample, and cannot be generalised to external LLMs or other universities.

### 7.4 Evidence‑based recommendations
1. Add explicit official‑document source references within AI‑agent responses for major‑selection queries, helping students cross‑check factual content and calibrate trust.
2. Place prominent disclaimers reminding users that AI output is advisory only and cannot replace official university major‑selection guidance.
3. Optimise the agent’s handling of complex comparative questions between different majors, which was repeatedly mentioned in open‑ended feedback.
4. For future evaluation work, collect full anonymised conversation transcripts to enable objective factual‑accuracy coding alongside subjective survey measurement.

All recommendations are derived from observed participant feedback and quantitative patterns; we avoid purely speculative suggestions.

---

## 8. Transparency and references

### 8.1 Division of labour

| Member | Student ID | Responsibilities |
|---|---|---|
| Sun Mengyue | 2686020 | Research report writing; questionnaire design; survey recruitment; data analysis |
| Liu Kaimeng | 2684863 | Research report writing; questionnaire design; survey recruitment; webpage development |
| Lin Peiyi | 2684871 | Research report writing; survey recruitment; poster design |
| Zhang Chenjia | 2692591 | Research report writing; questionnaire design; survey recruitment |

### 8.2 Use of AI tools
Generative AI tools were used only for language polishing, wording checks and reference formatting. Every AI‑assisted passage was reviewed, edited and verified by our group. No raw data, fabricated findings, interview quotes or analysis results were generated by AI. Our group takes full responsibility for the accuracy of this report.

### 8.3 Data and materials availability
The questionnaire is hosted on Tally: https://tally.so/r/OQX4JA. De‑identified raw responses, the coding scheme, analysis scripts and anonymised supplementary excerpts are available upon reasonable request to the research team. Informed consent specified that optional contact information would be used only for follow‑up and then deleted within 30 days; contact details are not stored together with the public dataset.

### 8.4 References
[1] K. Mwantimwa, “What motivates students’ decisions on programmes to pursue at university level: The role of information and knowledge,” *Higher Education*, vol. 82, no. 2, pp. 349–366, 2021.

[2] S. R. Porter and P. D. Umbach, “College major choice: An analysis of person‑environment fit,” *Research in Higher Education*, vol. 47, no. 4, pp. 429–449, 2006.

[3] H. Crompton and K. Burke, “The educational affordances and challenges of generative artificial intelligence: A systematic review,” *TechTrends*, vol. 68, no. 2, pp. 183–202, 2024.

[4] T. Zylowski et al., “Designing an LLM‑based educational pathway recommendation assistant,” in *Proceedings of the 2024 Learning Analytics and Knowledge Conference*, pp. 456–467, 2024.

[5] J. M. Logg, J. A. Minson, and D. A. Moore, “Algorithm appreciation: People prefer judging by algorithm,” *Organizational Behavior and Human Decision Processes*, vol. 151, pp. 90–103, 2019.

[6] B. J. Dietvorst, J. P. Simmons, and C. Massey, “Algorithm aversion: People erroneously avoid algorithms after seeing them err,” *Journal of Experimental Psychology: General*, vol. 144, no. 1, pp. 114–126, 2015.

[7] Y. Zhang, Q. Liao, and R. Bellamy, “Effect of confidence and explanation on trust in decision‑making algorithms,” in *Proceedings of the 2020 CHI Conference on Human Factors in Computing Systems*, pp. 1–12, 2020.

[8] J. Y. Bo et al., “Warning against over‑reliance on AI advice: The role of reliability disclaimers,” in *Proceedings of the AAAI Conference on Human Computation and Crowdsourcing*, vol. 12, pp. 23–32, 2024.

[9] F. D. Davis, “Perceived usefulness, perceived ease of use, and user acceptance of information technology,” *MIS Quarterly*, vol. 13, no. 3, pp. 319–340, Sep. 1989.

[10] A. Bangor, P. T. Kortum, and J. T. Miller, “An empirical evaluation of the System Usability Scale,” *International Journal of Human–Computer Interaction*, vol. 24, no. 6, pp. 574–594, 2008.

[11] P. Vlachogianni et al., “Usability evaluation of educational technology tools using the System Usability Scale: A systematic review,” *Journal of Research on Technology in Education*, vol. 54, no. 3, pp. 392–409, 2022.

### 8.5 Acknowledgements
We thank all students who took the survey. We also thank the XJTLU ethics review process and the team behind the university AI‑Agent platform for making this evaluation possible. We are grateful to the authors of the cited research for laying the theoretical foundation for our work.
