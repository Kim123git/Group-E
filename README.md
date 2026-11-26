<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ADS401 Report | XJTLU Major Selection AI Assistant</title>
<style>
  :root{
    --navy:#16264a;
    --navy-2:#243b6b;
    --blue:#1f7ae0;
    --blue-soft:#e8f2fd;
    --teal:#0f766e;
    --teal-soft:#e6f4f2;
    --amber:#b45309;
    --amber-soft:#fdf3e3;
    --ink:#1d2733;
    --muted:#55636f;
    --bg:#f4f7fc;
    --card:#ffffff;
    --line:#dbe4ef;
    --shadow:0 6px 22px rgba(22,38,74,.10);
    --radius:16px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0; background:var(--bg); color:var(--ink);
    font-family:"Segoe UI", system-ui, -apple-system, Arial, Helvetica, sans-serif;
    line-height:1.7; font-size:16px;
  }
  /* ---------- Hero ---------- */
  header.hero{
    background:linear-gradient(135deg,var(--navy) 0%,var(--navy-2) 55%,var(--blue) 100%);
    color:#fff; padding:3.2rem 1.5rem 2.4rem;
  }
  .hero-inner{max-width:1080px;margin:0 auto;}
  .hero .eyebrow{
    display:inline-block; background:rgba(255,255,255,.16); border:1px solid rgba(255,255,255,.28);
    padding:.25rem .8rem; border-radius:999px; font-size:.85rem; letter-spacing:.04em; margin-bottom:1rem;
  }
  header.hero h1{margin:.2rem 0 .8rem; font-size:2.1rem; line-height:1.25;}
  header.hero p.summary{max-width:820px; color:#e6eefb; font-size:1.02rem;}
  .member-chips{display:flex;flex-wrap:wrap;gap:.6rem;margin-top:1.2rem;}
  .chip{background:rgba(255,255,255,.13); border:1px solid rgba(255,255,255,.25); border-radius:10px; padding:.45rem .8rem; font-size:.9rem;}
  .chip strong{color:#fff;}
  .system-link{margin-top:1.2rem;}
  .system-link a{
    display:inline-block; background:#fff; color:var(--navy); font-weight:600; text-decoration:none;
    padding:.55rem 1rem; border-radius:10px; font-size:.92rem;
  }
  .system-link a:hover{background:var(--blue-soft);}
  /* ---------- Sticky nav ---------- */
  nav.toc{
    position:sticky; top:0; z-index:50; background:var(--navy);
    box-shadow:0 2px 10px rgba(0,0,0,.18);
  }
  nav.toc ul{
    max-width:1080px; margin:0 auto; padding:.5rem 1rem; list-style:none;
    display:flex; flex-wrap:wrap; gap:.3rem;
  }
  nav.toc a{
    color:#dbe7f7; text-decoration:none; font-size:.86rem; padding:.4rem .7rem; border-radius:8px;
  }
  nav.toc a:hover{background:rgba(255,255,255,.14); color:#fff;}
  /* ---------- Layout ---------- */
  main{max-width:1080px; margin:0 auto; padding:2rem 1.2rem 4rem;}
  section.card{
    background:var(--card); border:1px solid var(--line); border-radius:var(--radius);
    box-shadow:var(--shadow); padding:1.8rem 1.9rem; margin:1.8rem 0;
    border-left:5px solid var(--blue);
  }
  section.card:nth-of-type(odd){border-left-color:var(--teal);}
  h2{color:var(--navy); font-size:1.5rem; margin-top:0; padding-bottom:.5rem; border-bottom:2px solid var(--blue-soft);}
  h3{color:var(--navy-2); font-size:1.12rem; margin-top:1.6rem;}
  h4{color:var(--teal); font-size:1rem; margin:1.1rem 0 .3rem;}
  p{margin:.7rem 0;}
  ul,ol{padding-left:1.4rem;}
  li{margin:.35rem 0;}
  a{color:var(--blue);}
  /* ---------- Callouts ---------- */
  .callout{border-radius:12px; padding:.9rem 1.1rem; margin:1.1rem 0; font-size:.95rem;}
  .callout.caveat{background:var(--amber-soft); border-left:4px solid var(--amber); color:#5c3d10;}
  .callout.note{background:var(--blue-soft); border-left:4px solid var(--blue); color:#1c3f63;}
  .callout.evidence{background:var(--teal-soft); border-left:4px solid var(--teal); color:#0c4a45;}
  .callout strong{display:block; margin-bottom:.2rem;}
  /* ---------- Figures ---------- */
  figure{margin:1.6rem 0; background:#fbfcfe; border:1px solid var(--line); border-radius:14px; padding:1rem;}
  figure img{width:100%; height:auto; border-radius:8px; display:block;}
  figcaption{font-size:.9rem; color:var(--muted); margin-top:.7rem; line-height:1.55;}
  figcaption strong{color:var(--navy);}
  /* ---------- Tables ---------- */
  .table-wrap{overflow-x:auto; margin:1.1rem 0;}
  table{border-collapse:collapse; width:100%; font-size:.93rem; background:#fff;}
  th{background:var(--navy); color:#fff; text-align:left; padding:.65rem .8rem;}
  td{border-bottom:1px solid var(--line); padding:.6rem .8rem; vertical-align:top;}
  tr:nth-child(even) td{background:#f7fafe;}
  /* ---------- Stat chips ---------- */
  .stats{display:flex; flex-wrap:wrap; gap:.9rem; margin:1.1rem 0;}
  .stat{flex:1 1 150px; background:linear-gradient(135deg,var(--blue-soft),var(--teal-soft)); border:1px solid var(--line); border-radius:12px; padding:.9rem 1rem;}
  .stat .label{font-size:.82rem; color:var(--muted);}
  .stat .value{font-size:1.4rem; font-weight:700; color:var(--navy);}
  .stat .sub{font-size:.82rem; color:var(--muted);}
  /* ---------- References ---------- */
  ol.refs{padding-left:1.6rem;}
  ol.refs li{margin-bottom:.7rem; font-size:.9rem; color:#2c3a47;}
  .badge{display:inline-block; background:var(--teal-soft); color:var(--teal); border:1px solid #bfe6e1; border-radius:999px; font-size:.78rem; padding:.15rem .7rem; margin-left:.4rem;}
  footer{max-width:1080px; margin:0 auto; padding:1.5rem 1.2rem 3rem; color:var(--muted); font-size:.85rem; text-align:center;}
  @media (max-width:640px){
    header.hero h1{font-size:1.5rem;}
    section.card{padding:1.2rem 1.1rem;}
  }
</style>
</head>
<body>

<!-- ===================== HERO / SECTION 1 ===================== -->
<header class="hero" id="sec1">
  <div class="hero-inner">
    <span class="eyebrow">ADS401 Evaluation Methods and Statistics · Web Report</span>
    <h1>Evaluating an AI Major-Selection Assistant for Year-1 Students at XJTLU</h1>
    <p class="summary">This project evaluates the XJTLU internal AI-Agent major-selection chatbot for Year-1 undergraduate students. Originally we planned task-based usability testing with three standardised tasks for objective timing and success metrics. To better capture users' subjective attitudes and perceived trust toward this AI tool, the main formal data collection was adjusted to an online questionnaire-based mixed-method survey. We collected demographic background, awareness and usage experience, a standardised SUS usability scale, a trust scale, multiple-choice comparative questions and open-ended qualitative feedback. The study aims to understand user perception, strengths, pain-points and improvement directions for this AI tool.</p>
    <div class="member-chips">
      <span class="chip"><strong>Sun Mengyue</strong> · 2686020</span>
      <span class="chip"><strong>Lin Peiyi</strong> · 2684871</span>
      <span class="chip"><strong>Liu Kaimeng</strong> · 2684863</span>
      <span class="chip"><strong>Zhang Chenjia</strong> · 2692591</span>
    </div>
    <div class="system-link">
      <a href="https://aiagent.xjtlu.edu.cn/product/llm/mall/application/d40ej496i3uelisjb0q0/chat" target="_blank" rel="noopener">Evaluated system: XJTLU Major-Selection AI Assistant ↗</a>
    </div>
  </div>
</header>

<!-- ===================== NAV ===================== -->
<nav class="toc" aria-label="Report sections">
  <ul>
    <li><a href="#sec1">1. At a glance</a></li>
    <li><a href="#sec2">2. Problem &amp; RQs</a></li>
    <li><a href="#sec3">3. Background</a></li>
    <li><a href="#sec4">4. Design</a></li>
    <li><a href="#sec5">5. Analysis</a></li>
    <li><a href="#sec6">6. Findings</a></li>
    <li><a href="#sec7">7. Discussion</a></li>
    <li><a href="#sec8">8. Transparency</a></li>
  </ul>
</nav>

<main>

<!-- ===================== SECTION 2 ===================== -->
<section class="card" id="sec2">
  <h2>2. Problem, Motivation and Research Questions</h2>

  <h3>Intended users and context</h3>
  <p><strong>Target users:</strong> XJTLU Year-1 students who need to make major-selection decisions at the end of Year 1. Major-related information is scattered across university official websites, social media and informal advice from senior students. Students spend substantial manual effort gathering and comparing major-related information, and an internal AI agent was introduced to support this information-seeking process.</p>

  <h3>Evaluation problem</h3>
  <p>Although the agent is intended to help freshmen compare and understand programme options, there is little local empirical evidence about whether its answers are clear and accurate enough for this high-stakes decision, how efficiently students can obtain useful information through interaction, and whether students trust the answers enough to use the tool in their major choice.</p>

  <h3>Research questions</h3>
  <ol>
    <li>Can this AI chatbot help Year-1 XJTLU students retrieve accurate and clear information for major selection?</li>
    <li>How efficiently can users get answers to their major-related questions by interacting with this AI assistant?</li>
    <li>Do Year-1 students trust the AI-generated answers and consider this tool usable for their major choice?</li>
  </ol>

  <h3>Scope of the claims</h3>
  <div class="callout caveat">
    <strong>Boundary of generalisation</strong>
    Findings are limited to the XJTLU internal AI-Agent major-selection assistant and our sample of participating students. Results cannot be generalised to external large-language models, other universities, or to students at later study stages.
  </div>
</section>

<!-- ===================== SECTION 3 ===================== -->
<section class="card" id="sec3">
  <h2>3. Background and Related Work</h2>

  <h3>3.1 How students actually choose a major</h3>
  <p>Picking a major is not a one-off decision. Mwantimwa [1] found that freshers' choices are driven both by personal factors like interest and ability and by external information such as employment, family, and reputation, which come from scattered sources; students without career information tend to decide less rationally. Porter and Umbach [2] showed from a person–environment fit perspective that the match between a student's personality and the academic setting affects both major choice and later persistence. A good tool therefore should not hand over a conclusion, but provide comparable information for the student to judge.</p>

  <h3>3.2 AI advising and recommendation tools in education</h3>
  <p>Generative LLMs spread quickly in education, but value and risk go together. Crompton and Burke [3] reviewed 44 studies: students get instant answers and personalised feedback, yet also face inaccuracy, hallucination, and privacy issues, so an answer about a major cannot be trusted by default. Zylowski et al. [4] built an LLM-based pathway-recommendation assistant and compared it against a form-based tool and an intent-based chatbot on trustworthiness, usability, and explainability; a natural conversation does not mean the advice is trusted. Existing evaluations mostly target school pupils or generic tutoring, and little work looks at an in-house agent for first-year students choosing among the university's own programmes — that is our gap.</p>

  <h3>3.3 Whether students trust algorithmic advice</h3>
  <p>Attitudes toward algorithms are mixed. Logg et al. [5] ran six experiments and found that people often follow algorithmic advice more readily than human advice when expertise does not matter — algorithm appreciation. Dietvorst et al. [6] showed the flip side: after watching an algorithm err, people lose confidence in it faster than in a human making the same mistake — algorithm aversion. Trust, then, is calibrated through use rather than fixed upfront. Zhang, Liao, and Bellamy [7] found that showing confidence helps calibrate trust but does not guarantee better decisions; Bo et al. [8] showed that short reliability disclaimers reduce over-reliance on wrong advice in class. We therefore measure trust and usefulness separately instead of merging them into one satisfaction score.</p>

  <h3>3.4 Why we chose these measures</h3>
  <p>Perceived usefulness and ease of use come from Davis's technology acceptance model [9], where usefulness is the strongest predictor of intention to use, matching our questions about getting satisfying answers and useful information. For perceived usability we use the SUS: Bangor et al. [10] established score interpretation and cross-product comparison from nearly a decade of data, and Vlachogianni and Tselios [11] confirmed its reliability in educational settings. SUS sits alongside the usefulness and trust items because being easy to use and being trustworthy are different; conversation length and message count give behavioural checks against the self-report scores.</p>
</section>

<!-- ===================== SECTION 4 ===================== -->
<section class="card" id="sec4">
  <h2>4. System and Evaluation Design</h2>

  <h3>4.1 System under evaluation</h3>
  <p>The evaluated system is the <strong>XJTLU Major-Selection AI Assistant</strong>, an internal agent hosted on the XJTLU AI-Agent platform. It accepts natural-language questions from students and returns text answers about programme choices, curriculum structure, entry requirements and study or career pathways. The evaluated interaction is a free-form dialogue in which a Year-1 student asks major-selection questions relevant to their own decision and reads the agent's textual responses.</p>
  <p><strong>In scope:</strong> perceived clarity and usefulness of answers, interaction experience, user trust and perceived system usability. <strong>Out of scope:</strong> backend model architecture, benchmark performance against commercial LLMs, and evaluation of teaching or administrative staff as users.</p>

  <h3>4.2 Participants, recruitment and sample-size rationale</h3>
  <p>Participants were XJTLU Year-1 students who had not yet finalised their major choice. They were recruited through year-group online channels and class-level sharing, using convenience sampling with an effort to cover different intended directions. The final valid sample comprised <strong>N = 43</strong> participants, all of whom completed the questionnaire in full.</p>
  <p>The minimum benchmark for a usability study is 12 participants [10]; our sample exceeds this threshold. Because this evaluation prioritises descriptive understanding and exploratory subgroup comparison rather than confirmatory group-level inference, a formal power analysis was not applied; inferential tests reported below should be read as exploratory.</p>

  <h3>4.3 Study design, procedure and tasks</h3>
  <p>This is a <strong>mixed-method questionnaire-based evaluation</strong>. As noted in the project summary, the original plan was task-based usability testing with three standardised tasks and objective timing. The formal data collection was adjusted to an online survey so that subjective attitudes, perceived trust and open feedback could be captured efficiently from a broader sample. The four major-decision categories reported in Part 2 are background subgroups used for exploratory comparison; they are <em>not</em> experimentally manipulated conditions.</p>
  <p>The online procedure proceeded in five steps:</p>
  <ol>
    <li><strong>Consent and screening:</strong> participants read the information sheet and gave informed consent before starting; Year-1 status was confirmed through a screening item.</li>
    <li><strong>Background questions:</strong> demographics and the student's usual major-decision driver (self-clear career direction, self-based on interest, family-driven decision, other sources).</li>
    <li><strong>Agent interaction:</strong> participants opened the agent link and asked their own major-selection questions, following the same introductory prompt provided to all participants.</li>
    <li><strong>Post-interaction self-report:</strong> they reported conversation duration, number of self-sent messages, and whether they obtained useful information, then answered three 7-point Likert items and the modified SUS.</li>
    <li><strong>Open feedback:</strong> a free-text question invited improvement suggestions and additional comments.</li>
  </ol>

  <h3>4.4 Variables, operational definitions and measures</h3>
  <div class="table-wrap">
    <table>
      <thead>
        <tr><th>Research question</th><th>Construct</th><th>Operational measure</th><th>Type</th></tr>
      </thead>
      <tbody>
        <tr>
          <td>RQ1</td>
          <td>Perceived clarity &amp; timeliness of information (CLAR)</td>
          <td>7-point Likert item: "This AI chatbot provides me with up-to-date and clear information for my major selection."</td>
          <td>Subjective ordinal</td>
        </tr>
        <tr>
          <td>RQ2</td>
          <td>Perceived interaction efficiency (EFF)</td>
          <td>7-point Likert item: "I can efficiently obtain satisfying answers to my major-selection questions via this AI chatbot."</td>
          <td>Subjective ordinal</td>
        </tr>
        <tr>
          <td>RQ2</td>
          <td>Behavioural self-report</td>
          <td>Self-reported conversation duration (<em>Time</em>: &lt;2 min, 2–5 min, 5–10 min, other/&gt;10 min); number of self-sent messages; perceived task success (<em>Useful</em>: 0 = no, 1 = yes).</td>
          <td>Categorical / ordinal</td>
        </tr>
        <tr>
          <td>RQ3</td>
          <td>User trust (TRUST)</td>
          <td>7-point Likert item: "I trust the AI-generated answers and believe they can serve as useful references for my major-choice decision."</td>
          <td>Subjective ordinal</td>
        </tr>
        <tr>
          <td>RQ3</td>
          <td>Perceived system usability</td>
          <td>Modified 10-item SUS; aggregate score <em>SUS_Total</em> interpreted against the conventional 68-point benchmark.</td>
          <td>Composite score</td>
        </tr>
      </tbody>
    </table>
  </div>

  <div class="callout caveat">
    <strong>Important measurement distinction</strong>
    The questionnaire captures participants' <em>subjective</em> perception of clarity. Subjective clarity cannot by itself establish factual accuracy: a response may read clearly yet contain an incorrect fact. Objective accuracy would require independent coding of anonymised conversation transcripts, which was not part of this survey-based study and is listed as a limitation in Section 7.
  </div>

  <h3>4.5 Ethics, consent, privacy and bias mitigation</h3>
  <ul>
    <li><strong>Informed consent:</strong> participants received an information sheet explaining the purpose, their right to withdraw at any time, and that AI output cannot replace official university major guidance.</li>
    <li><strong>Anonymity:</strong> no name, student ID or other direct identifier was collected with the survey responses; optional contact details, if provided, were used only for scheduling and deleted afterwards.</li>
    <li><strong>Data minimisation:</strong> participants were instructed not to enter sensitive personal information into the agent; raw identifiable records are not published on the web page or in the public repository.</li>
    <li><strong>Bias mitigation:</strong> all participants received the same introductory script and questionnaire items; quantitative analysis and open-text coding were reviewed jointly by two researchers to reduce single-analyst bias.</li>
  </ul>

  <h3>4.6 Pilot changes and deviations from the original plan</h3>
  <p>A small pilot was run before formal data collection to check item wording, response categories and the flow of the online questionnaire. Ambiguous wording in the Likert and duration items was revised accordingly. The main documented deviation is the shift from task-based laboratory testing to an online questionnaire design (Section 4.3); this trade-off is discussed as a limitation in Section 7.</p>
</section>

<!-- ===================== SECTION 5 ===================== -->
<section class="card" id="sec5">
  <h2>5. Data Preparation and Analysis</h2>

  <h3>5.1 Data types and analysis software</h3>
  <p>Survey responses were exported from Tally and imported into SPSS for quantitative analysis. Two data types were analysed:</p>
  <ul>
    <li><strong>Quantitative data:</strong> demographic and background variables, categorical behavioural self-reports (<em>Time</em>, message count, <em>Useful</em>), three 7-point Likert items (EFF, TRUST, CLAR), and the composite SUS score (<em>SUS_Total</em>).</li>
    <li><strong>Qualitative data:</strong> free-text open-ended suggestions, analysed thematically.</li>
  </ul>

  <h3>5.2 Cleaning, coding, exclusions and missing data</h3>
  <p>All collected responses were complete and valid. No cases were excluded from the dataset, and no missing-value imputation was required. SUS negatively-worded items were reversed according to standard SUS polarity before aggregation; positively-worded items retained their raw direction. The three Likert items were treated as ordinal for descriptive presentation, while means and standard deviations were computed for benchmark comparison as is common in applied HCI practice.</p>

  <h3>5.3 Statistical tests and justification</h3>
  <p>Because the study is primarily evaluative rather than confirmatory, analysis centres on descriptive statistics supplemented by benchmark comparisons:</p>
  <ul>
    <li><strong>Descriptive statistics:</strong> frequencies and proportions for categorical variables; means, standard deviations, medians and quartiles for rating and SUS scores.</li>
    <li><strong>One-sample t-tests:</strong> EFF, TRUST and CLAR means were tested against the Likert neutral midpoint of 4; <em>SUS_Total</em> was tested against the conventional usability benchmark of 68. These tests assess whether average ratings differ meaningfully from a reference point, and exact <em>p</em>-values are reported.</li>
    <li><strong>Categorical association:</strong> the relationship between conversation duration and perceived usefulness was examined with cross-tabulation; Fisher's exact test was preferred where expected cell counts were small.</li>
    <li><strong>Subgroup comparison:</strong> splits by major-decision driver are exploratory descriptive summaries, given limited per-group sample size.</li>
  </ul>
  <div class="callout note">
    <strong>Assumptions and uncertainty</strong>
    Likert-derived means are treated as interval-scale for the one-sample tests, a pragmatic choice in applied usability work; nonparametric summaries (medians, quartiles) are retained as a robustness check. Exact test statistics, confidence intervals and effect sizes are stored with the SPSS output in the Supplementary Materials. No claim of causal group difference is made from the exploratory subgroup splits.
  </div>

  <h3>5.4 Qualitative analysis process</h3>
  <p>Open-ended responses were read iteratively and coded inductively in a spreadsheet. Recurring themes concerning perceived strengths, problems and improvement suggestions were grouped, and representative anonymised comments were retained to support the quantitative findings. Direct participant quotes are reported only in anonymised form and are not published alongside any identifying information.</p>
</section>

<!-- ===================== SECTION 6 ===================== -->
<section class="card" id="sec6">
  <h2>6. Findings</h2>
  <p>This section answers each research question in turn. Quantitative outputs are drawn from the SPSS analysis; figures show static, labelled results with uncertainty where available.</p>

  <div class="stats">
    <div class="stat"><div class="label">EFF · perceived efficiency</div><div class="value">M = 5.58</div><div class="sub">7-point scale, neutral = 4</div></div>
    <div class="stat"><div class="label">TRUST · trust in answers</div><div class="value">M = 5.40</div><div class="sub">7-point scale, neutral = 4</div></div>
    <div class="stat"><div class="label">CLAR · clarity &amp; timeliness</div><div class="value">M = 5.70</div><div class="sub">7-point scale, neutral = 4</div></div>
    <div class="stat"><div class="label">SUS_Total · usability</div><div class="value">M = 70.81</div><div class="sub">SD = 14.69; benchmark 68</div></div>
  </div>

  <h3>6.1 RQ1 — Can the chatbot provide accurate and clear major-selection information?</h3>
  <figure>
    <img src="figures/figure1_overall.png" alt="Bar chart comparing mean EFF, TRUST and CLAR ratings on a 7-point Likert scale, with a horizontal reference line at the neutral value of 4.">
    <figcaption><strong>Figure 1.</strong> Mean ratings of EFF (perceived efficiency), TRUST (trust in AI answers) and CLAR (perceived clarity and timeliness). The horizontal reference line marks the neutral value of 4; error bars represent 95% confidence intervals.</figcaption>
  </figure>
  <p>On the 7-point scale, all three subjective ratings sat above the neutral midpoint of 4. <strong>CLAR received the highest mean (M = 5.70)</strong>, suggesting participants generally perceived the agent's outputs as clear and timely. One-sample t-tests against the neutral value 4 were significant for all three items (all <em>p</em> &lt; 0.001; exact <em>t</em> and 95% CI are in the supplementary SPSS output). TRUST was the lowest of the three means (M = 5.40), indicating that perceived clarity did not fully translate into equal confidence in the answers.</p>

  <figure>
    <img src="figures/figure2_subgroup.png" alt="Grouped bar chart showing mean EFF, TRUST and CLAR scores across four major-decision driver subgroups: self-clear career direction, self-based on interest, family-driven decision, and other sources.">
    <figcaption><strong>Figure 2.</strong> Mean EFF, TRUST and CLAR scores grouped by four major-decision-making driver subgroups. Error bars represent 95% confidence intervals.</figcaption>
  </figure>
  <p>Splitting by how students normally make major decisions, all four subgroups scored above the neutral point on every measure (Figure 2). No subgroup showed a consistently strong advantage across all three dimensions; the "other sources" subgroup displayed the widest confidence intervals, reflecting the most heterogeneous attitudes. These subgroup patterns are exploratory and should not be read as confirmed group differences.</p>

  <div class="callout caveat">
    <strong>Evidence boundary</strong>
    These results establish <em>perceived</em> clarity only. They do not demonstrate that every answer is factually correct; judging factual accuracy would require independent transcript coding, which was outside this survey's scope.
  </div>

  <h3>6.2 RQ2 — How efficiently can users obtain answers to major-related questions?</h3>
  <figure>
    <img src="figures/figure3_time.png" alt="Simple bar chart of the frequency distribution of self-reported conversation duration across four categories: under 2 minutes, 2 to 5 minutes, 5 to 10 minutes, and other.">
    <figcaption><strong>Figure 3.</strong> Frequency distribution of self-reported AI conversation time (<em>Time</em>). The vertical axis shows the number of participants in each duration group.</figcaption>
  </figure>
  <p>The modal interaction lasted <strong>2–5 minutes</strong> (Figure 3), followed by the 5–10 minute group; only a small minority chatted for under two minutes, and few reported very long conversations. Most participants therefore completed a moderate-length dialogue rather than an extremely quick or lengthy session.</p>

  <figure>
    <img src="figures/figure4_stacked.png" alt="Stacked bar chart: conversation duration on the horizontal axis, stacked segments showing participants who obtained useful information (Yes) and those who did not (No).">
    <figcaption><strong>Figure 4.</strong> Stacked bar chart of access to useful information across conversation durations. Coloured segments represent participants who did not obtain useful information (No) and those who did (Yes).</figcaption>
  </figure>
  <p>Across every duration category, the large majority of participants reported obtaining useful information (Figure 4); only one participant in the under-2-minute group did not. Even short conversations mostly produced self-reported useful content, while the 2–5 minute group contained the largest absolute number of successful cases, partly because it was also the largest group. Together with the EFF mean of 5.58, the behavioural self-reports suggest the agent can deliver subjectively useful information without requiring an excessively long interaction.</p>

  <h3>6.3 RQ3 — Do students trust the answers and find the tool usable?</h3>
  <figure>
    <img src="figures/figure5_sus.png" alt="Boxplot of modified SUS total scores, with a horizontal reference line marking the SUS good-usability threshold of 68. The box shows the 25th to 75th percentile range and the median line.">
    <figcaption><strong>Figure 5.</strong> Boxplot of modified SUS total scores (<em>SUS_Total</em>). The horizontal reference line marks the standard SUS benchmark of 68; the box covers the 25th–75th percentile range and the central line denotes the median.</figcaption>
  </figure>
  <p>Trust stood above neutral (TRUST M = 5.40) but remained the weakest of the three subjective perceptions. For usability, <em>SUS_Total</em> averaged <strong>M = 70.81 (SD = 14.69)</strong>, slightly above the 68 benchmark. A one-sample t-test against 68 returned <em>p</em> = 0.216, which is not statistically significant: we cannot conclude that the system's usability differs from the general-tool benchmark. The boxplot shows a wide spread, with scores ranging from below 50 to above 90 and a median around 72. Usability was therefore acceptable on average, but experience varied substantially across individuals.</p>

  <h3>6.4 Qualitative themes from open feedback</h3>
  <p>Recurring themes in the free-text responses aligned with the quantitative pattern:</p>
  <ul>
    <li><strong>Convenient consolidation:</strong> students valued being able to gather scattered programme information in one conversation quickly.</li>
    <li><strong>Accuracy concerns:</strong> several respondents noted that answers should be checked against official sources, and asked for explicit references or links to programme handbooks.</li>
    <li><strong>Desired improvements:</strong> suggestions included clearer source attribution, more major-specific detail, and guidance on how to phrase follow-up questions.</li>
  </ul>
  <p>Representative anonymised comments are retained in the Supplementary Materials; no verbatim quote is published here with identifying details.</p>
</section>

<!-- ===================== SECTION 7 ===================== -->
<section class="card" id="sec7">
  <h2>7. Discussion, Limitations and Recommendations</h2>

  <h3>7.1 Interpretation and practical significance</h3>
  <p>The overall picture is moderately positive but uneven. Students perceived the agent's outputs as relatively clear, could obtain self-reported useful information within a short dialogue, and rated usability around the conventional benchmark. Clarity was the strongest dimension, while trust was comparatively weaker — a pattern consistent with the trust literature, where ease of understanding does not guarantee confidence in correctness [7][8]. Practically, the agent appears to fill a genuine information-consolidation gap for freshmen, but the wide dispersion in SUS and Likert scores shows it does not work equally well for every student.</p>

  <h3>7.2 Alternative explanations</h3>
  <p>Several alternative explanations should be considered before treating the positive averages as evidence of strong performance. Participants may have rated clarity based on how clearly an answer was written rather than whether its facts were correct. Self-reported duration and usefulness are subject to recall and social-desirability bias. Free-form interaction allowed different students to ask different questions, so task difficulty and topic are not fully controlled. Prior familiarity with generative AI may also have shaped ratings.</p>

  <h3>7.3 Limitations</h3>
  <ul>
    <li><strong>Sample and generalisability:</strong> a convenience sample of Year-1 XJTLU students; findings do not extend to other populations or external LLMs.</li>
    <li><strong>Self-report reliance:</strong> interaction time, message count and usefulness were recalled by participants rather than logged by the system; objective system-log data were not available.</li>
    <li><strong>No objective accuracy coding:</strong> factual correctness of transcripts was not independently assessed, so RQ1 is answered through perceived clarity only.</li>
    <li><strong>Modified instrument:</strong> the SUS response scale was adapted from the standard version, so benchmark comparisons should be interpreted cautiously; exact standard SUS norms are not directly transferable.</li>
    <li><strong>Exploratory subgroup tests:</strong> per-group sample sizes are small, and subgroup comparisons are underpowered for confirmation.</li>
    <li><strong>Single-encounter snapshot:</strong> attitudes were measured after one interaction; longer-term trust and continued use are not captured.</li>
  </ul>

  <h3>7.4 Evidence-based recommendations</h3>
  <p>The following recommendations are tied directly to the observed findings:</p>
  <ol>
    <li><strong>Strengthen source traceability (addresses weaker trust and accuracy concerns):</strong> attach official-source citations or links to the university programme handbook alongside answers about requirements and curriculum, and keep a visible disclaimer that the agent is a reference rather than an official decision.</li>
    <li><strong>Surface reliability cues:</strong> where the system can do so, indicate confidence or distinguish verified official information from general explanation, to support calibrated trust rather than blind reliance [7].</li>
    <li><strong>Support efficient follow-up:</strong> refine intent recognition for follow-up questions and offer prompt suggestions, so students with multi-part major questions do not need many turns to reach useful information.</li>
    <li><strong>Future evaluation:</strong> run a task-based study with logged timings and message counts, add dual-coder factual-accuracy coding of anonymised transcripts, recruit a larger stratified sample, and measure trust over repeated use.</li>
  </ol>

  <div class="callout evidence">
    <strong>Observed evidence vs. speculation</strong>
    The reported means, proportions and SUS distribution are observed evidence from our sample. Interpretations about why ratings vary, and recommendations about future system changes, are reasoned inferences grounded in that evidence and the related work; they are not themselves measured outcomes.
  </div>
</section>

<!-- ===================== SECTION 8 ===================== -->
<section class="card" id="sec8">
  <h2>8. Transparency and References</h2>

  <h3>8.1 Division of labour</h3>
  <div class="table-wrap">
    <table>
      <thead><tr><th>Member</th><th>Student ID</th><th>Responsibilities</th></tr></thead>
      <tbody>
        <tr><td>Sun Mengyue</td><td>2686020</td><td>Research report writing; questionnaire design; survey recruitment; data analysis.</td></tr>
        <tr><td>Liu Kaimeng</td><td>2684863</td><td>Research report writing; questionnaire design; survey recruitment; webpage development.</td></tr>
        <tr><td>Lin Peiyi</td><td>2684871</td><td>Research report writing; survey recruitment; poster design.</td></tr>
        <tr><td>Zhang Chenjia</td><td>2692591</td><td>Research report writing; questionnaire design; survey recruitment.</td></tr>
      </tbody>
    </table>
  </div>

  <h3>8.2 Use of AI tools</h3>
  <p>Generative AI tools were used only for language polishing, wording checks, and reference formatting. Every AI-assisted passage was reviewed, edited, and verified by the group. No data, literature, interview quotes, or findings were generated by AI, and the authors take full responsibility for the accuracy of this report.</p>

  <h3>8.3 Data and materials availability</h3>
  <p>The questionnaire is hosted on Tally (<a href="https://tally.so/r/OQX4JA" target="_blank" rel="noopener">https://tally.so/r/OQX4JA</a>). De-identified raw responses, the coding scheme, analysis scripts, SPSS output and anonymised feedback excerpts are available in the Supplementary Materials. Per the informed-consent form, optional contact details were used only for scheduling and deleted after the study; they are not retained with the public data. No raw participant data is published on this web page or in the public repository.</p>

  <h3>8.4 References (IEEE, in order of first appearance)</h3>
  <ol class="refs">
    <li>K. Mwantimwa, "What motivates students' decisions on programmes to pursue at university level: The role of information and knowledge," <i>Higher Education</i>, vol. 82, no. 2, pp. 349–367, 2021, doi: 10.1007/s10734-021-00698-4.</li>
    <li>S. R. Porter and P. D. Umbach, "College major choice: An analysis of person–environment fit," <i>Research in Higher Education</i>, vol. 47, no. 4, pp. 429–449, 2006, doi: 10.1007/s11162-005-9002-3.</li>
    <li>H. Crompton and D. Burke, "The educational affordances and challenges of ChatGPT: State of the field," <i>TechTrends</i>, vol. 68, no. 2, pp. 380–392, 2024, doi: 10.1007/s11528-024-00939-0.</li>
    <li>T. Zylowski, N. Sautchuk Patricio, W. Hettmann, K. Anderer, M. Wölfel, and P. A. Henning, "Evaluating trustworthiness, usability and explainability of an educational pathway recommendation system that uses a large language model," in <i>EDULEARN24 Proceedings</i>, 2024, pp. 6461–6470, doi: 10.21125/edulearn.2024.1528.</li>
    <li>J. M. Logg, J. A. Minson, and D. A. Moore, "Algorithm appreciation: People prefer algorithmic to human judgment," <i>Organizational Behavior and Human Decision Processes</i>, vol. 151, pp. 90–103, 2019, doi: 10.1016/j.obhdp.2018.12.005.</li>
    <li>B. J. Dietvorst, J. P. Simmons, and C. Massey, "Algorithm aversion: People erroneously avoid algorithms after seeing them err," <i>Journal of Experimental Psychology: General</i>, vol. 144, no. 1, pp. 114–126, 2015, doi: 10.1037/xge0000033.</li>
    <li>Y. Zhang, Q. V. Liao, and R. K. E. Bellamy, "Effect of confidence and explanation on accuracy and trust calibration in AI-assisted decision making," in <i>Proceedings of the 2020 Conference on Fairness, Accountability, and Transparency (FAT* '20)</i>, New York, NY, USA: ACM, 2020, pp. 295–305, doi: 10.1145/3351095.3372852.</li>
    <li>J. Y. Bo, H. Kumar, M. Liut, and A. Anderson, "Disclosures &amp; disclaimers: Investigating the impact of transparency disclosures and reliability disclaimers on learner-LLM interactions," in <i>Proceedings of the AAAI Conference on Human Computation and Crowdsourcing (HCOMP)</i>, vol. 12, 2024, pp. 23–32, doi: 10.1609/hcomp.v12i1.31597.</li>
    <li>F. D. Davis, "Perceived usefulness, perceived ease of use, and user acceptance of information technology," <i>MIS Quarterly</i>, vol. 13, no. 3, pp. 319–340, Sep. 1989, doi: 10.2307/249008.</li>
    <li>A. Bangor, P. T. Kortum, and J. T. Miller, "An empirical evaluation of the System Usability Scale," <i>International Journal of Human–Computer Interaction</i>, vol. 24, no. 6, pp. 574–594, 2008, doi: 10.1080/10447310802205776.</li>
    <li>P. Vlachogianni and N. Tselios, "Perceived usability evaluation of educational technology using the System Usability Scale (SUS): A systematic review," <i>Journal of Research on Technology in Education</i>, vol. 54, no. 3, pp. 392–409, 2022, doi: 10.1080/15391523.2020.1867938.</li>
    <li>DeepSeek V3.1, available at https://www.deepseek.com. Used for grammatical proofreading only.</li>
  </ol>

  <h3>8.5 Acknowledgements</h3>
  <p>We thank the students who completed the survey; the XJTLU ethics review committee for approving the study; the university AI-Agent platform for providing the system under evaluation; and the authors of the cited works whose public research we built on.</p>
</section>

</main>

<footer>
  ADS401 Evaluation Methods and Statistics · Group web report · Single-page GitHub Pages site
</footer>

</body>
</html>
