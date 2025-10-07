---
title: "Dual-Mode Explanations for Suicide Risk Detection in Online Mental Health Support"
subtitle: "Framework combining extractive and abstractive layers for transparent, clinically grounded explanations"
year: 2025
category: "AI & Mental Health"
role: ["PI/Lead"]
img: /assets/img/projects/DualModeExplanations.png

importance: 96
tags: ["Explainable AI", "Mental Health", "LLM", "Suicide Risk Detection", "Interpretability"]
---
<style>
/* Shrink ONLY this project's cover image */
img[src="/assets/img/projects/DualModeExplanations.png"]{
  width: 94% !important;     /* tweak 60–75% as you like */
  height: auto !important;
  display: block !important;
  margin: 0 auto 1rem !important;
  object-fit: contain !important;
}
</style>

Mental health support services increasingly use AI systems to detect suicide risk in chat conversations, yet clinicians often struggle to trust predictions due to opaque reasoning. Developed with support from the National Science Foundation, this project introduces a dual-mode explanation framework that bridges model outputs with clinical reasoning. The extractive layer highlights help-seeker utterances most responsible for predictions using BCombined, an ensemble of SHAP, LIME, Integrated Gradients, and Embedding-shift relevance. The abstractive layer maps these utterances to psychological risk categories from a curated Suicide Risk Factors lexicon with the aid of large language models. Evaluation on 30,000+ Hebrew hotline sessions and an English Reddit dataset shows cross-language applicability, while a user study with counselors at Israel’s national hotline (Sahar) demonstrated improved helpfulness and understandability without loss of trust. This work advances explainable AI in high-stakes clinical settings, providing transparent, theory-grounded explanations that enhance decision-making while preserving human agency.
