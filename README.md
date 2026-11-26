<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ADS401_GroupID_Report | XJTLU Major‑Selection AI Assistant</title>
    <style>
        body {
            font-family: Arial, Helvetica, sans-serif;
            max-width: 1050px;
            margin: 3rem auto;
            padding: 0 20px;
            line-height: 1.65;
            color: #111;
        }
        h1 {
            font-size: 1.6em;
            margin-top: 2.2em;
            border-bottom: 1px solid #aaa;
            padding-bottom: 0.3em;
        }
        h2 {
            font-size:1.3em;
            margin-top:1.6em;
        }
        h3 {
            font-size:1.15em;
            margin-top:1.2em;
        }
        figure {
            margin: 1.8rem 0;
        }
        figcaption {
            font-size:0.92em;
            color:#222;
            margin-top:0.4rem;
        }
        table {
            border-collapse: collapse;
            width:100%;
            margin:1rem 0;
        }
        th, td {
            border:1px solid #777;
            padding:0.5rem 0.7rem;
            text-align:left;
        }
        ol.ref-list {
            padding-left:1.8rem;
        }
        ol.ref-list li {
            margin-bottom:0.7rem;
        }
        a {
            color:#004499;
        }
    </style>
</head>
<body>

<!-- 1. Project at a glance -->
<a id="sec‑1"></a>
<h1>1. Project at a glance</h1>
<p><strong>Title:</strong> XJTLU Major Selection AI Assistant</p>
<p><strong>Group Members &amp; Student ID:</strong></p>
<ul>
    <li>Sun Mengyue, 2686020</li>
    <li>Lin Peiyi, 2684871</li>
    <li>Liu Kaimeng, 2684863</li>
    <li>Zhang Chenjia, 2692591</li>
</ul>

<h3>Project Summary</h3>
<p>This project evaluates the XJTLU internal AI‑Agent major‑selection chatbot for Year‑1 undergraduate students. Originally we planned task‑based usability testing with three standardized tasks for objective timing and success metrics. To better capture users’ subjective attitudes and perceived trust toward this AI tool, the main formal data collection was adjusted to an online questionnaire‑based mixed‑method survey. We collected demographic background, awareness and usage experience, standardized SUS usability scale, trust scale, multiple‑choice comparative questions and open‑ended qualitative feedback. The study aims to understand user perception, strengths, pain‑points and improvement directions for this AI tool.</p>

<p><strong>Evaluated System:</strong> XJTLU Major‑Selection AI Assistant (internal AI‑Agent platform).</p>
<p><strong>System Link:</strong>
<a href="https://aiagent.xjtlu.edu.cn/product/llm/mall/application/d40ej496i3uelisjb0q0/chat" target="_blank">
https://aiagent.xjtlu.edu.cn/product/llm/mall/application/d40ej496i3uelisjb0q0/chat
</a>
</p>

<figure>
    <img src="figures/figure1_likert_mean.png" alt="Bar chart of mean values for EFF, TRUST and CLAR 7‑point Likert items, neutral reference line at value 4">
    <figcaption><strong>Figure 1.</strong> Mean ratings of EFF (perceived efficiency), TRUST (trust in AI answers) and CLAR (perceived clarity and timeliness). 7‑point Likert scale; dashed horizontal line represents neutral value = 4.</figcaption>
</figure>

<figure>
    <img src="figures/figure2_subgroup_bar.png" alt="Grouped bar chart showing mean EFF, TRUST and CLAR split by four major‑decision‑making driver subgroups">
    <figcaption><strong>Figure 2.</strong> Mean EFF, TRUST and CLAR scores grouped by four major‑decision‑making driver subgroups.</figcaption>
</figure>

<!-- 2. Problem, motivation and research questions -->
<a id="sec‑2"></a>
<h1>2. Problem, motivation and research questions</h1>
<h3>Intended users and context</h3>
<p><strong>Target users:</strong> XJTLU Year‑1 students who need to make major‑selection decisions at the end of Year 1.</p>
<p>Major‑related information is scattered across university official websites, social media and informal advice from senior students. Students spend substantial manual effort gathering and comparing major‑related information.</p>

<h3>Research Questions</h3>
<ol>
    <li>Can this AI chatbot help Year‑1 XJTLU students retrieve accurate and clear information for major selection?</li>
    <li>How efficiently can users get answers to their major‑related questions by interacting with this AI assistant?</li>
    <li>Do Year‑1 students trust the AI‑generated answers and consider this tool usable for their major choice?</li>
</ol>

<h3>Scope of claims</h3>
<p>Findings are limited to XJTLU internal AI‑Agent major‑selection assistant, and our sample of participating students. Results cannot be generalised to external large‑language‑models or other‑university student populations.</p>

<figure>
    <img src="figures/figure3_time_frequency.png" alt="Simple bar chart for frequency distribution of self‑reported conversation time categories">
    <figcaption><strong>Figure 3.</strong> Frequency distribution of self‑reported AI conversation time (Time).</figcaption>
</figure>

<figure>
    <img src="figures/figure4_stacked_time_useful.png" alt="Stacked bar chart: conversation time on x‑axis, colour segments for obtained / not‑obtained useful information">
    <figcaption><strong>Figure 4.</strong> Stacked bar chart: proportion of participants obtaining useful information (Useful = 1) versus not obtaining useful information (Useful = 0) across different conversation‑time categories.</figcaption>
</figure>

<!-- 3. Background and Related Work -->
<a id="sec‑3"></a>
<h1>3. Background and Related Work</h1>

<h2>3.1 How students actually choose a major</h2>
<p>Picking a major is not a one‑off decision. Mwantimwa [1] found that freshers' choices are driven both by personal factors like interest and ability and by external information such as employment, family, and reputation, which come from scattered sources; students without career information tend to decide less rationally. Porter and Umbach [2] showed from a person–environment fit perspective that the match between a student's personality and the academic setting affects both major choice and later persistence. A good tool therefore should not hand over a conclusion, but provide comparable information for the student to judge.</p>

<h2>3.2 AI advising and recommendation tools in education</h2>
<p>Generative LLMs spread quickly in education, but value and risk go together. Crompton and Burke [3] reviewed 44 studies: students get instant answers and personalised feedback, yet also face inaccuracy, hallucination, and privacy issues, so an answer about a major cannot be trusted by default. Zylowski et al. [4] built an LLM‑based pathway‑recommendation assistant and compared it against a form‑based tool and an intent‑based chatbot on trustworthiness, usability, and explainability; a natural conversation does not mean the advice is trusted. Existing evaluations mostly target school pupils or generic tutoring, and little work looks at an in‑house agent for first‑year students choosing among the university's own programmes — that is our gap.</p>

<h2>3.3 Whether students trust algorithmic advice</h2>
<p>Attitudes toward algorithms are mixed. Logg et al. [5] ran six experiments and found that people often follow algorithmic advice more readily than human advice when expertise does not matter — algorithm appreciation. Dietvorst et al. [6] showed the flip side: after watching an algorithm err, people lose confidence in it faster than in a human making the same mistake — algorithm aversion. Trust, then, is calibrated through use rather than fixed upfront. Zhang, Liao, and Bellamy [7] found that showing confidence helps calibrate trust but does not guarantee better decisions; Bo et al. [8] showed that short reliability disclaimers reduce over‑reliance on wrong advice in class. We therefore measure trust and usefulness separately instead of merging them into one satisfaction score.</p>

<h2>3.4 Why we chose these measures</h2>
<p>Perceived usefulness and ease of use come from Davis's technology acceptance model [9], where usefulness is the strongest predictor of intention to use, matching our questions about getting satisfying answers and useful information. For perceived usability we use the SUS: Bangor et al. [10] established score interpretation and cross‑product comparison from nearly a decade of data, and Vlachogianni and Tselios [11] confirmed its reliability in educational settings. SUS sits alongside the usefulness and trust items because being easy to use and being trustworthy are different; conversation length and message count give behavioural checks against the self‑report scores.</p>

<figure>
    <img src="figures/figure5_sus_boxplot.png" alt="Boxplot for modified SUS total scores with dashed reference benchmark line at value 68">
    <figcaption><strong>Figure 5.</strong> Boxplot of modified SUS total scores (SUS_Total). Dashed reference line marks standard SUS usability benchmark = 68.</figcaption>
</figure>

<!-- 4. System and evaluation design -->
<a id="sec‑4"></a>
<h1>4. System and evaluation design</h1>

<h2>4.1 Evaluated system description</h2>
<p>This study evaluates XJTLU internal Major‑Selection AI Assistant hosted on the university AI‑Agent platform. The agent is designed to answer Year‑1 students’ natural‑language questions concerning major‑selection, programme requirements, curriculum and progression rules. The system is intended as supplementary guidance rather than an official replacement for academic advisors or university documentation. This evaluation focuses on end‑user perception after interacting with the agent; underlying model weights and backend retrieval mechanisms are outside the scope of this project.</p>

<h2>4.2 Participants, recruitment and sample‑size rationale</h2>
<p>Participants were XJTLU Year‑1 undergraduate students facing major‑selection decisions. Recruitment was carried out via Year‑1 student social groups. All participants completed the online questionnaire after interacting with the AI assistant. The final sample size is N=43. All responses were complete and retained for analysis. For this questionnaire‑driven mixed‑methods evaluation, sample size is constrained by practical recruitment limits. While usability‑testing conventions often suggest 12 participants, this study relies on self‑reported survey data to capture subjective perception, trust and behavioural feedback.</p>

<h2>4.3 Study procedure</h2>
<p>Mixed‑method online survey design: participants first read study information and gave informed consent. They interacted with the XJTLU Major‑Selection AI‑Agent for major‑selection‑related queries. After completing their conversation, participants filled in the full questionnaire. The questionnaire included demographic items, major‑decision‑making background, post‑interaction behavioural self‑report, three custom 7‑point Likert items for core research questions, modified 10‑point SUS scale, and one open‑ended feedback question.</p>

<h2>4.4 Variables and operationalisation</h2>
<table>
    <tr>
        <th>Construct</th>
        <th>Operational Measure</th>
    </tr>
    <tr>
        <td>R1 Perceived clarity</td>
        <td>Part4 Q3, 7‑point Likert (CLAR)</td>
    </tr>
    <tr>
        <td>R2 Subjective efficiency</td>
        <td>Part4 Q1, 7‑point Likert (EFF)</td>
    </tr>
    <tr>
        <td>R2 Behavioural efficiency indicators</td>
        <td>Self‑reported conversation time; self‑reported user message count; perceived task success (Useful: yes/no)</td>
    </tr>
    <tr>
        <td>R3 User trust</td>
        <td>Part4 Q2, 7‑point Likert (TRUST)</td>
    </tr>
    <tr>
        <td>R3 Perceived usability</td>
        <td>Modified 10‑point System Usability Scale total score (SUS_Total)</td>
    </tr>
</table>

<h2>4.5 Ethics, consent and bias mitigation</h2>
<p>All participants provided informed consent before participation. No identifying information such as name or student ID was collected in the questionnaire. Participants were reminded that AI‑agent output is not official university advice. Responses were anonymised. The questionnaire did not feed participant personal data into the AI‑agent. Potential response bias is acknowledged; all results rely on self‑reported experience rather than system log data.</p>

<h2>4.6 Deviation from original plan</h2>
<p>The original plan was controlled task‑based usability testing with objective timing metrics. Due to practical constraints on in‑person lab recruitment, data collection shifted to an online questionnaire‑based mixed‑method design. Participants completed self‑reported interaction instead of supervised controlled tasks. This deviation is noted as a limitation later in the report.</p>

<!-- 5. Data preparation and analysis -->
<a id="sec‑5"></a>
<h1>5. Data preparation and analysis</h1>
<p>All collected participant responses were complete and valid. No cases were excluded and no missing‑value imputation was required. Survey data exported from the questionnaire platform were imported into SPSS for quantitative statistical analysis.</p>

<h2>5.1 Data types</h2>
<ul>
    <li><strong>Quantitative survey data:</strong> demographic variables, self‑reported interaction behaviour, three custom 7‑point Likert items, modified 10‑point SUS scale.</li>
    <li><strong>Qualitative data:</strong> open‑text improvement suggestions from questionnaire Part 6.</li>
</ul>

<h2>5.2 Data pre‑processing</h2>
<p>The SUS scale was modified from standard 1‑5 points to a 1‑10‑point response range. Negatively phrased SUS items were reversed‑coded before computing the aggregate SUS_Total score. Custom Likert items EFF, TRUST and CLAR were treated as ordinal‑level data. Categorical variables for conversation time and perceived usefulness were kept as nominal categories for frequency analysis.</p>

<h2>5.3 Selection of statistical tests</h2>
<p>One‑sample t‑tests were used to compare Likert means against the scale neutral mid‑point value of 4. A one‑sample t‑test compared SUS_Total mean against the widely accepted SUS usability benchmark value of 68. Descriptive frequency statistics were generated for conversation‑time categories and perceived useful‑information acquisition. Exploratory subgroup descriptive comparisons were performed across four major‑decision‑driver groups; formal inferential testing for subgroups was not conducted. Exact p‑values are reported where possible; full SPSS output files are included within supplementary materials.</p>

<h2>5.4 Qualitative analysis</h2>
<p>Open‑ended text responses were analysed using inductive thematic analysis in Excel. Responses were read iteratively to identify recurring themes about strengths, problems and improvement suggestions for the AI assistant. Anonymised short participant quotes support thematic findings in section 6.</p>

<!-- 6. Findings -->
<a id="sec‑6"></a>
<h1>6. Findings</h1>
<p>This section presents quantitative survey results organised sequentially for RQ1, RQ2 and RQ3. Note that questionnaire items capture subjective participant perception only; objective factual accuracy of AI outputs cannot be assessed via this survey dataset.</p>

<h2>6.1 Findings for RQ1: Can this AI chatbot help Year‑1 XJTLU students retrieve accurate and clear information for major selection?</h2>
<p>Figure 1 visualises mean scores for EFF, TRUST and CLAR against the 7‑point‑scale neutral mid‑point (4). Descriptive statistics: EFF <em>M</em>=5.58; TRUST <em>M</em>=5.40; CLAR <em>M</em>=5.70. One‑sample t‑tests against value 4 show all three means are significantly higher than neutral (all <em>p</em>&lt;0.001). CLAR (perceived clarity and timeliness) obtained the highest average rating, while TRUST scored the lowest among the three variables, even though still sitting clearly above neutral.</p>
<p>Figure 2 shows exploratory subgroup means split by participants’ major‑decision‑making drivers. Mean ratings remained above neutral across all four subgroups. No consistent strong subgroup pattern was observed; some subgroups show larger variance. These subgroup comparisons are descriptive only and not hypothesis‑driven.</p>
<p><strong>Caveat:</strong> High subjectively‑perceived clarity (CLAR) does not guarantee factual accuracy of AI generated content.</p>

<h2>6.2 Findings for RQ2: How efficiently can users get answers to their major‑related questions by interacting with this AI assistant?</h2>
<p>Figure 3 presents frequency distribution for self‑reported conversation time. The modal category is 2‑5 minutes. Fewer participants reported very short (&lt;2 min) or very long (&gt;10 min) conversations.</p>
<p>Figure 4 is the stacked bar chart of conversation time against whether participants obtained useful information. Within every time category, most participants reported obtaining useful information. Even participants with very short interactions (&lt;2 minutes) mostly gained subjectively useful outputs. Larger absolute counts of successful cases are found within 2‑5 min and 5‑10 min bins, corresponding to higher participant numbers within these categories. Self‑reported behavioural evidence suggests the AI assistant can deliver subjectively useful information without requiring extremely long interaction sessions.</p>

<h2>6.3 Findings for RQ3: Do Year‑1 students trust the AI‑generated answers and consider this tool usable for their major choice?</h2>
<p>RQ3 covers both trust (TRUST reported in RQ1 section) and system usability measured by modified SUS_Total. Figure 5 shows the boxplot of SUS_Total scores with benchmark reference line at 68. Descriptive statistics: SUS_Total <em>M</em>=70.81, <em>SD</em>=14.69. A one‑sample t‑test against benchmark 68 yields <em>p</em>=0.216, which is not statistically significant. Although sample mean sits slightly above the industry benchmark, we cannot conclude the system usability differs significantly from general‑purpose tool standards. The boxplot reveals wide score dispersion: participants show highly variable usability experience.</p>
<p>Combined with TRUST results (<em>M</em>=5.40 above neutral but relatively lower than clarity), many participants accept the AI assistant for major‑selection support, yet trust and usability performance vary substantially between individuals.</p>

<h2>6.4 Qualitative themes from open‑ended feedback</h2>
<p>Recurring themes from open‑text suggestions include: requests for clearer official‑source citations for AI answers; expectation for improved handling of complex major‑comparison questions; appreciation for fast preliminary information retrieval; warnings about potential factual mistakes on university‑specific programme rules. Selected anonymised short quotes are preserved within supplementary materials.</p>

<!--7. Discussion, limitations and recommendations -->
<a id="sec‑7"></a>
<h1>7. Discussion, limitations and recommendations</h1>

<h2>7.1 Interpretation of findings</h2>
<p>On average, Year‑1 students subjectively perceived the XJTLU major‑selection AI‑Agent as clear, reasonably efficient, and moderately trustworthy. SUS usability scores sit slightly above the standard benchmark but without statistically significant difference. Most participants reported gaining subjectively useful information in short‑to‑moderate conversation durations. However, large variance across all key measurements indicates user experience is inconsistent: the AI assistant works well for some students while others hold more negative perceptions.</p>
<p>An important distinction emerges: participants can perceive AI output as clear, which does not guarantee factual correctness. This reinforces existing literature on algorithm appreciation and algorithm aversion: subjective perception and objective factual quality are separate dimensions [5][6]. Trust remains comparatively weaker than perceived clarity, implying that building user trust should be a priority for future agent iterations.</p>

<h2>7.2 Alternative explanations</h2>
<p>Several alternative factors may shape survey outcomes. Participant prior familiarity with generative AI may influence both trust and usability ratings. Because interaction tasks were self‑directed rather than standardised in lab settings, participants chose their own questions, introducing variation in task difficulty. Exploratory subgroup results hint that students’ pre‑existing major‑decision‑making styles may moderate experience, but this cannot be firmly concluded from descriptive data alone.</p>

<h2>7.3 Limitations</h2>
<ol>
<li>This study uses self‑reported questionnaire data, without objective system log data or supervised controlled‑task laboratory testing, following deviation from original project plan.</li>
<li>We cannot evaluate objective factual accuracy of AI answers, as transcripts from participant‑agent conversations were not systematically collected and coded.</li>
<li>Recruitment relies on convenience sampling among Year‑1 XJTLU students; sample may not be fully representative of the whole Year‑1 population.</li>
<li>Subgroup comparisons across major‑decision‑making groups are purely descriptive; no formal statistical inference can be drawn.</li>
<li>The SUS scale was modified from original 1‑5 to 1‑10‑point response format; results cannot be directly compared against classic SUS normative datasets.</li>
<li>Findings apply only for this specific in‑house XJTLU AI‑Agent and this participant sample, and cannot generalise to external LLMs or other universities.</li>
</ol>

<h2>7.4 Evidence‑based recommendations</h2>
<ol>
<li>Add explicit official‑document source references within AI‑agent responses for major‑selection queries, helping students cross‑check factual content and calibrate user trust.</li>
<li>Place prominent disclaimers reminding users that AI output is advisory only and cannot replace official university major‑selection guidance.</li>
<li>Optimise agent handling for complex comparative questions between different majors, as this is repeatedly mentioned in open‑ended feedback.</li>
<li>For future evaluation work, collect full anonymised conversation transcripts to enable objective factual‑accuracy coding alongside subjective survey measurement.</li>
</ol>
<p>All recommendations are derived from observed participant feedback and quantitative patterns; speculative suggestions are avoided.</p>

<!--8. Transparency and references -->
<a id="sec‑8"></a>
<h1>8. Transparency and references</h1>

<h2>8.1 Division of labour</h2>
<table>
    <thead>
        <tr>
            <th>Member</th>
            <th>Student ID</th>
            <th>Responsibilities</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Sun Mengyue</td>
            <td>2686020</td>
            <td>Research report writing; questionnaire design; survey recruitment; data analysis.</td>
        </tr>
        <tr>
            <td>Liu Kaimeng</td>
            <td>2684863</td>
            <td>Research report writing; questionnaire design; survey recruitment; webpage development.</td>
        </tr>
        <tr>
            <td>Lin Peiyi</td>
            <td>2684871</td>
            <td>Research report writing; survey recruitment; poster design.</td>
        </tr>
        <tr>
            <td>Zhang Chenjia</td>
            <td>2692591</td>
            <td>Research report writing; questionnaire design; survey recruitment.</td>
        </tr>
    </tbody>
</table>

<h2>8.2 Use of AI tools</h2>
<p>Generative AI tools were used only for language polishing, wording checks, and reference formatting. Every AI‑assisted passage was reviewed, edited, and verified by the group. No data, literature, interview quotes, or findings were generated by AI, and the authors take full responsibility for the accuracy of this report.</p>

<h2>8.3 Data and materials availability</h2>
<p>The questionnaire is hosted on Tally (<a href="https://tally.so/r/OQX4JA" target="_blank">https://tally.so/r/OQX4JA</a>). De‑identified raw responses, the coding scheme, analysis scripts, and anonymised interview excerpts are available on reasonable request from the study team. Per the informed‑consent form, optional contact details were used only for interview scheduling and deleted within 30 days after the interviews; they are not retained with the public data.</p>

<h2>8.4 References (IEEE format, ordered by first citation)</h2>
<ol class="ref-list">
<li>K. Mwantimwa, "What motivates students' decisions on programmes to pursue at university level: The role of information and knowledge," <i>Higher Education</i>, vol. 82, no. 2, pp. 349–367, 2021, doi: 10.1007/s10734‑021‑00698‑4.</li>
<li>S. R. Porter and P. D. Umbach, "College major choice: An analysis of person–environment fit," <i>Research in Higher Education</i>, vol. 47, no. 4, pp. 429–449, 2006, doi: 10.1007/s11162‑005‑9002‑3.</li>
<li>H. Crompton and D. Burke, "The educational affordances and challenges of ChatGPT: State of the field," <i>TechTrends</i>, vol. 68, no. 2, pp. 380–392, 2024, doi: 10.1007/s11528‑024‑00939‑0.</li>
<li>T. Zylowski, N. Sautchuk Patricio, W. Hettmann, K. Anderer, M. Wölfel, and P. A. Henning, "Evaluating trustworthiness, usability and explainability of an educational pathway recommendation system that uses a large language model," in <i>EDULEARN24 Proceedings</i>, 2024, pp. 6461–6470, doi: 10.21125/edulearn.2024.1528.</li>
<li>J. M. Logg, J. A. Minson, and D. A. Moore, "Algorithm appreciation: People prefer algorithmic to human judgment," <i>Organizational Behavior and Human Decision Processes</i>, vol. 151, pp. 90–103, 2019, doi: 10.1016/j.obhdp.2018.12.005.</li>
<li>B. J. Dietvorst, J. P. Simmons, and C. Massey, "Algorithm aversion: People erroneously avoid algorithms after seeing them err," <i>Journal of Experimental Psychology: General</i>, vol. 144, no. 1, pp. 114–126, 2015, doi: 10.1037/xge0000033.</li>
<li>Y. Zhang, Q. V. Liao, and R. K. E. Bellamy, "Effect of confidence and explanation on accuracy and trust calibration in AI‑assisted decision making," in <i>Proceedings of the 2020 Conference on Fairness, Accountability, and Transparency (FAT* '20)</i>, New York, NY, USA: ACM, 2020, pp. 295–305, doi: 10.1145/3351095.3372852.</li>
<li>J. Y. Bo, H. Kumar, M. Liut, and A. Anderson, "Disclosures &amp; disclaimers: Investigating the impact of transparency disclosures and reliability disclaimers on learner‑LLM interactions," in <i>Proceedings of the AAAI Conference on Human Computation and Crowdsourcing (HCOMP)</i>, vol. 12, 2024, pp. 23–32, doi: 10.1609/hcomp.v12i1.31597.</li>
<li>F. D. Davis, "Perceived usefulness, perceived ease of use, and user acceptance of information technology," <i>MIS Quarterly</i>, vol. 13, no. 3, pp. 319–340, Sep. 1989, doi: 10.2307/249008.</li>
<li>A. Bangor, P. T. Kortum, and J. T. Miller, "An empirical evaluation of the System Usability Scale," <i>International Journal of Human–Computer Interaction</i>, vol. 24, no. 6, pp. 574–594, 2008, doi: 10.1080/10447310802205776.</li>
<li>P. Vlachogianni and N. Tselios, "Perceived usability evaluation of educational technology using the System Usability Scale (SUS): A systematic review," <i>Journal of Research on Technology in Education</i>, vol. 54, no. 3, pp. 392–409, 2022, doi: 10.1080/15391523.2020.1867938.</li>
</ol>

<h2>8.5 Acknowledgements</h2>
<p>We thank the students who completed the survey and took part in the interviews; the XJTLU ethics review committee for approving the study; the university AI‑Agent platform for providing the system under evaluation; and the authors of the cited works whose public research we built on.</p>

</body>
</html>
