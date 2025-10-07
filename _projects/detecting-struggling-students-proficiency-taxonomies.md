---
title: "Detecting Struggling Student Programmers using Proficiency Taxonomies"
subtitle: "Early-warning AI that models programming skills to flag at-risk students"
year: 2025
category: "AI & LLM"
role: ["Co-PI"]
img: /assets/img/projects/model_architecture.png
importance: 98
tags: ["Education", "LLM/ML", "Student Modeling"]
---

Early identification of struggling programmers enables targeted support at scale. The project introduces the Proficiency Taxonomy Model (PTM), which embeds a proficiency taxonomy co-designed with educators directly into the prediction process and learns from each student’s full submission history. PTM builds a Taxonomy-Based Proficiency Profile across 13 dimensions—ten observable programming concepts and three latent skills—producing interpretable skill scores that map to concrete interventions. PTM then combines this profile with the target task’s text and required concepts through a cross-attention module to forecast struggle on upcoming tasks. Evaluations on two real course datasets - CodeWorkout (introductory Java) and FalconCode (introductory Python) - showed that PTM outperformed strong baselines and generalized across languages. Analyses included ablations isolating the value of the taxonomy and of long submission histories, sensitivity studies on sequence length, and statistical significance and calibration checks across multiple metrics. Together, these results position PTM as a practical early-warning capability that is interpretable, data-efficient, and directly aligned with instructional goals.
