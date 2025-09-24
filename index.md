---
layout: boot
title: INSaFLU Workshop
permalink: /
---

# INSaFLU Workshop

## Learning Objectives:
  - Broad description of the INSaFLU platform
  - Upload data and associated metadata to INSaFLU
  - Generate consensus sequences and characterize them
  - Perform phylogenetic and geotemporal analysis using NextStrain in INSaFLU
 
## Learning Outcomes:

  - [**1**: Broadly describe the INSaFLU platform](#LO1)

  - [**2**: Upload data and associated metadata to INSaFLU](#LO2)
    + [**2.1**: Prepare the reads and metadata](#LO2.1)
    + [**2.2**: Configure the settings for preprocessing](#LO2.2)
    + [**2.3**: Upload data and metadata and evaluate preprocessing results](#LO2.3)

  - [**3**: Generate consensus sequences and characterize them](#LO3)
    + [**3.1**: Create a project and configure settings](#LO3.1)
    + [**3.2**: Add samples to project and analyze results](#LO3.2)

  - [**4**: Perform phylogenetic and geotemporal analysis using NextStrain in INSaFLU](#LO4)
    + [**4.1**: Create Nextstrain project, add consensus](#LO4.1)  
    + [**4.2**: Update metadata and run the build](#LO4.2)  
    + [**4.3**: Visualize Nextstrain results](#LO4.3)



## <a id="LO1">1 - Broadly describe the INSaFLU platform</a>

![NGS Workflow](images/NGSworkflow.jpg)

<!-- Enhanced Visual Question Box -->
<div class="question-box">
<strong>QUESTION:</strong> Can you broadly describe the main functionalities of INSaFLU?
<details class="hint-level">
<summary>💡 Need a hint?</summary>
<div class="hint-content">Think about the typical NGS workflow: data input → quality control → sequence analysis → phylogenetic analysis → visualization</div>
</details>
<details class="full-answer">
<summary>📋 Show complete answer</summary>
<div class="answer-content">
<ul>
<li>Upload of NGS data, QC and rapid identification</li>
<li>Generation of consensus sequences and their characterization</li>
<li>Nextstrain module for phylogenetic and geotemporal analysis</li>
<li>TELEVIR module for virus detection</li>
</ul>
</div>
</details>
</div>

<!-- Progressive Learning Section -->
<div class="learning-progression">
<h3>Understanding INSaFLU: Step by Step</h3>
<details class="step-1">
<summary>Step 1: What is INSaFLU? 🤔</summary>
<div class="answer-content">
<p>INSaFLU is a comprehensive web-based platform designed for genomic surveillance of influenza and SARS-CoV-2 viruses. It provides an integrated solution for processing next-generation sequencing (NGS) data from raw reads to phylogenetic analysis.</p>
</div>
</details>
<details class="step-2">
<summary>Step 2: How does data flow through the system? 📊</summary>
<div class="answer-content">
<p>The workflow begins with raw sequencing data upload, followed by quality control, reference mapping, consensus sequence generation, and finally phylogenetic and geotemporal analysis using integrated tools.</p>
</div>
</details>
<details class="step-3">
<summary>Step 3: What makes it special for surveillance? 🔬</summary>
<div class="answer-content">
<p>INSaFLU integrates multiple analysis modules including Nextstrain for phylogenetic visualization, TELEVIR for virus detection, and automated reporting tools specifically designed for public health surveillance workflows.</p>
</div>
</details>
<details class="step-4">
<summary>Step 4: Who can use it and how? 👥</summary>
<div class="answer-content">
<p>The platform is designed for researchers, public health professionals, and surveillance laboratories. It provides both user-friendly web interfaces and advanced configuration options for different expertise levels.</p>
</div>
</details>
</div>

<!-- Interactive Quiz -->
<div class="quiz-question"
     data-correct-answer="b"
     data-correct-text="Correct! The Nextstrain module is specifically designed for phylogenetic and geotemporal analysis, allowing users to visualize viral evolution and spread patterns over time and geography."
     data-incorrect-text="Not quite right. The correct answer is the Nextstrain module.">
<strong>QUIZ:</strong> Which module in INSaFLU is specifically used for phylogenetic and geotemporal analysis?
<div class="quiz-options">
<label><input type="radio" name="q1" value="a"> TELEVIR module</label>
<label><input type="radio" name="q1" value="b"> Nextstrain module</label>
<label><input type="radio" name="q1" value="c"> QC module</label>
<label><input type="radio" name="q1" value="d"> Upload module</label>
</div>
<button class="check-answer-btn">Check Answer</button>
<div class="quiz-feedback"></div>
</div>

<!-- Self-Assessment -->
<div class="self-check">
<strong>SELF-CHECK:</strong> Before proceeding, can you explain the INSaFLU platform to a colleague?
<details><summary>📝 Key points to cover</summary>
<div class="checklist">
<h4>Your explanation should include:</h4>
<ul>
<li>☐ Purpose: Genomic surveillance platform for influenza and SARS-CoV-2</li>
<li>☐ Input: Handles NGS data with quality control</li>
<li>☐ Processing: Generates consensus sequences and characterizes them</li>
<li>☐ Analysis: Integrated Nextstrain for phylogenetic analysis</li>
<li>☐ Detection: TELEVIR module for broader virus detection</li>
<li>☐ Output: Visualization and reporting tools for surveillance</li>
</ul>
</div>
</details>
</div>


## <a id="LO2">2 - Upload data and associated metadata to INSaFLU</a>

<!-- Try It Yourself Section -->
<div class="try-it-yourself">
<strong>TRY IT YOURSELF:</strong> Practice data upload workflow
<p>Before uploading real data, let's walk through the key considerations for successful data submission to INSaFLU.</p>
<details><summary>🛠️ Show preparation checklist</summary>
<div class="checklist">
<h4>Pre-upload checklist:</h4>
<ul>
<li>☐ Verify FASTQ file format and quality</li>
<li>☐ Prepare metadata spreadsheet with required fields</li>
<li>☐ Check file naming conventions</li>
<li>☐ Ensure adequate file sizes for analysis</li>
<li>☐ Review privacy and data sharing policies</li>
</ul>
</div>
</details>
</div>

<!-- Multi-level Question -->
<div class="question-box">
<strong>QUESTION:</strong> What are the essential metadata fields required for INSaFLU analysis?
<details class="hint-level">
<summary>💡 Think about surveillance needs</summary>
<div class="hint-content">Consider what information epidemiologists need: when, where, what type of sample, and how it was processed...</div>
</details>
<details class="full-answer">
<summary>📋 Show required metadata fields</summary>
<div class="answer-content">
<ul>
<li>Sample identifier (unique ID)</li>
<li>Collection date (essential for temporal analysis)</li>
<li>Geographic location (country, region)</li>
<li>Sample type (respiratory, clinical specimen type)</li>
<li>Sequencing platform and protocol details</li>
<li>Patient demographics (age, gender if available)</li>
</ul>
</div>
</details>
</div>

## <a id="LO3">3 - Generate consensus sequences and characterize them</a>

<!-- Advanced Quiz with Multiple Scenarios -->
<div class="quiz-question"
     data-correct-answer="c"
     data-correct-text="Excellent choice! Investigating coverage gaps and considering re-sequencing is the best approach. While 85% coverage might be acceptable for some analyses, understanding which regions are missing is crucial. Key genes like spike protein should have good coverage for meaningful phylogenetic analysis."
     data-incorrect-text="That's not the optimal approach for quality genomic surveillance.">
<strong>SCENARIO QUIZ:</strong> You receive a consensus sequence with 85% genome coverage. What should be your next step?
<div class="quiz-options">
<label><input type="radio" name="q3" value="a"> Accept it as is - 85% is sufficient</label>
<label><input type="radio" name="q3" value="b"> Reject the sample entirely</label>
<label><input type="radio" name="q3" value="c"> Investigate coverage gaps and consider re-sequencing</label>
<label><input type="radio" name="q3" value="d"> Only use it for basic identification</label>
</div>
<button class="check-answer-btn">Check Answer</button>
<div class="quiz-feedback"></div>
</div>

<!-- Complex Learning Progression -->
<div class="learning-progression">
<h3>Consensus Sequence Quality Assessment</h3>
<details class="step-1">
<summary>Step 1: Understand coverage metrics 📊</summary>
<div class="answer-content">
<p><strong>Coverage Depth:</strong> Number of reads supporting each position. Higher depth (>100x) provides more confidence in variant calls.</p>
<p><strong>Coverage Breadth:</strong> Percentage of reference genome covered. Aim for >90% for reliable phylogenetic analysis.</p>
</div>
</details>
<details class="step-2">
<summary>Step 2: Identify quality thresholds 🎯</summary>
<div class="answer-content">
<p><strong>Minimum thresholds:</strong></p>
<ul>
<li>Coverage depth: ≥20x for variant calling</li>
<li>Coverage breadth: ≥85% for basic analysis, >95% for detailed studies</li>
<li>Base quality: Phred score ≥20</li>
<li>Mapping quality: ≥30 for reliable alignments</li>
</ul>
</div>
</details>
<details class="step-3">
<summary>Step 3: Handle problematic regions 🔧</summary>
<div class="answer-content">
<p>Some genomic regions are inherently difficult to sequence (repetitive elements, GC-rich regions). INSaFLU provides tools to:</p>
<ul>
<li>Mask low-quality regions</li>
<li>Apply position-specific filters</li>
<li>Generate consensus with appropriate ambiguity codes</li>
</ul>
</div>
</details>
</div>

## <a id="LO4">4 - Perform phylogenetic and geotemporal analysis using NextStrain in INSaFLU</a>

<!-- Interactive Decision Tree -->
<div class="learning-progression">
<h3>Nextstrain Analysis Decision Tree</h3>
<details class="step-1">
<summary>Decision Point 1: Dataset size considerations 📈</summary>
<div class="answer-content">
<p><strong>Small dataset (&lt;50 sequences):</strong> Ideal for detailed local outbreak investigation</p>
<p><strong>Large dataset (&gt;500 sequences):</strong> Requires subsampling strategies and computational considerations</p>
</div>
</details>
<details class="step-2">
<summary>Decision Point 2: Reference and context selection 🌍</summary>
<div class="answer-content">
<p>Choose appropriate reference sequences based on:</p>
<ul>
<li>Geographic relevance to your samples</li>
<li>Temporal proximity (same time period)</li>
<li>Known circulating variants in your region</li>
</ul>
</div>
</details>
<details class="step-3">
<summary>Decision Point 3: Interpretation strategies 📊</summary>
<div class="answer-content">
<p><strong>Phylogenetic patterns to look for:</strong></p>
<ul>
<li>Clustering of related samples (transmission chains)</li>
<li>Geographic spread patterns</li>
<li>Temporal evolution and variant emergence</li>
<li>Amino acid changes in key proteins</li>
</ul>
</div>
</details>
</details>

<!-- Advanced Self-Assessment -->
<div class="self-check">
<strong>COMPREHENSIVE CHECK:</strong> Integration of all INSaFLU components
<details><summary>🎓 Advanced competency assessment</summary>
<div class="checklist">
<h4>Can you confidently:</h4>
<ul>
<li>☐ Design a surveillance study using INSaFLU from start to finish?</li>
<li>☐ Troubleshoot common data quality issues?</li>
<li>☐ Interpret phylogenetic trees in epidemiological context?</li>
<li>☐ Combine metadata with genomic data for outbreak analysis?</li>
<li>☐ Communicate findings to public health stakeholders?</li>
<li>☐ Plan follow-up studies based on initial results?</li>
</ul>
</div>
</details>
</div>

<!-- Final Challenge Question -->
<div class="quiz-question"
     data-correct-answer="c"
     data-correct-text="Outstanding! A comprehensive analysis including epidemiological metadata is the gold standard approach. This involves: (1) Quality control and consensus generation, (2) Integration of spatial and temporal metadata, (3) Inclusion of relevant regional context sequences, (4) Nextstrain analysis for transmission pattern visualization, (5) Correlation with epidemiological investigation data, (6) Reporting suitable for public health action."
     data-incorrect-text="While that's part of the process, a comprehensive epidemiological approach would be more effective for outbreak investigation.">
<strong>INTEGRATION CHALLENGE:</strong> A local health department reports a cluster of COVID-19 cases. You have samples from 15 patients collected over 3 weeks. Design your INSaFLU analysis strategy.
<div class="quiz-options">
<label><input type="radio" name="q4" value="a"> Sequence all samples and run standard pipeline</label>
<label><input type="radio" name="q4" value="b"> Include regional reference sequences for context</label>
<label><input type="radio" name="q4" value="c"> Design comprehensive analysis including epidemiological metadata</label>
<label><input type="radio" name="q4" value="d"> Focus only on variant identification</label>
</div>
<button class="check-answer-btn">Check Answer</button>
<div class="quiz-feedback"></div>
</div>



