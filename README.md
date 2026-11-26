<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>ADS401_GroupReport | XJTLU Major‑Selection AI Assistant</title>
    <style>
        body { font-family:Arial, Helvetica, sans-serif; max-width:1100px; margin: 0 auto; padding:2rem; line-height:1.6; color:#222; }
        h1,h2,h3 { margin-top:2em; }
        figure { margin:2rem 0; }
        figcaption { font-size:0.9em; color:#333; margin-top:0.5rem; }
        table { border-collapse: collapse; width:100%; margin:1rem 0; }
        th,td { border:1px solid #aaa; padding:0.6rem; text-align:left; }
        ol.ref-list { padding-left:1.8rem; }
        ol.ref-list li { margin-bottom: 0.8rem; }
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

<!-- 图片占位 Figure1：EFF/TRUST/CLAR均值条形图 RQ1 -->
<figure>
    <img src="figures/figure1_likert_mean.png" alt="Bar chart of mean values for EFF, TRUST and CLAR 7‑point Likert items, neutral reference line at value 4">
    <figcaption><strong>Figure 1.</strong> Mean ratings of EFF (perceived efficiency), TRUST (trust in AI answers) and CLAR (perceived clarity and timeliness). 7‑point Likert scale; dashed horizontal line represents neutral value = 4.</figcaption>
</figure>

<!-- 图片占位 Figure2：四组决策来源 × EFF/TRUST/CLAR分组条形图 -->
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

<!-- 图片占位 Figure3：对话时长分布条形图 RQ2 -->
<figure>
    <img src="figures/figure3_time_frequency.png" alt="Simple bar chart for frequency distribution of self‑reported conversation time categories">
    <figcaption><strong>Figure 3.</strong> Frequency distribution of self‑reported AI conversation time (Time).</figcaption>
</figure>

<!-- 图片占位 Figure4：Time × Useful 堆叠条形图 RQ2 -->
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

<!-- 图片占位 Figure5 SUS箱线图 RQ3 -->
<figure>
    <img src="figures/figure5_sus_boxplot.png" alt="Boxplot for modified SUS total scores with dashed reference benchmark line at value 68">
    <figcaption><strong>Figure 5.</strong> Boxplot of modified SUS total scores (SUS_Total). Dashed reference line marks standard SUS usability benchmark = 68.</figcaption>
</figure>


<!-- ===== 预留章节占位，后续你填充4‑7 ===== -->
<a id="sec‑4"></a>
<h1>4. System and evaluation design</h1>
<p><!-- your content here --></p>

<a id="sec‑5"></a>
<h1>5. Data preparation and analysis</h1>
<p><!-- your content here --></p>

<a id="sec‑6"></a>
<h1>6. Findings</h1>
<p><!-- your findings paragraph here --></p>

<a id="sec‑7"></a>
<h1>7. Discussion, limitations and recommendations</h1>
<p><!-- your content here --></p>


<!-- 8. Transparency and references -->
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
