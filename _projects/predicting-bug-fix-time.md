---
title: "Predicting Bug Fix Time in Students’ Programming with Deep Language Models"
subtitle: "Modeling novice programmers’ code evolution to identify struggling students"
year: 2023
category: "AI & Education"
role: ["PI/Lead"]
img: /assets/img/projects/BugFixTime.png
importance: 85
tags: ["Educational Data Mining", "Programming Education", "Deep Learning", "Code Modeling", "Student Support"]
---

<style>
/* Shrink ONLY this project's cover image */
img[src="/assets/img/projects/BugFixTime.png"]{
  width: 90% !important;     /* tweak 60–75% as you like */
  height: auto !important;
  display: block !important;
  margin: 0 auto 1rem !important;
  object-fit: contain !important;
}
</style>

Automatically identifying struggling students can help instructors provide timely, targeted support. This project presents a deep-learning approach for predicting *bug-fix time*: the duration between when a student introduces a bug and when it is fixed. The model integrates a transformer-based code embedding (CodeBERT) with a time-aware LSTM that captures how each student’s code evolves over multiple snapshots, combined with contextual meta-features such as compilation history and experience level. Using data from over 300,000 Java code submissions in two educational environments (BlueJ and CodeWorkout), the model outperformed baseline methods based on Halstead metrics, Code2Vec embeddings, and single-snapshot variants. Results show that incorporating multiple code snapshots and temporal dynamics significantly improves the prediction of long bug-fix times, enabling early detection of struggling learners and supporting intelligent tutoring applications.
