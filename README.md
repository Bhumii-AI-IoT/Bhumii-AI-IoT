# Bhumii Shah

I notice patterns in how AI gets things wrong. That's what I want to build for.

---

## Where This Started

I work in AI data quality in London — reviewing audio and conversational AI training data across multiple languages.

Doing that every day, I kept noticing the same thing: the model assumes one way of speaking means one thing. But context matters. Background matters. How people express themselves matters. Every person is unique, and the system was trained on averages.

A regional accent isn't an edge case. A less-resourced language isn't an edge case. They're only edge cases if you built for the average.

That observation stuck with me. What if we stopped designing AI for the average person and started designing for the individual?

---

## What I'm Building

**[audio-qa-dashboard](https://github.com/Bhumii-AI-IoT/audio-qa-dashboard)** — a quality tracking dashboard for multilingual audio QA. Surfaces approval rates, rejection patterns and risk flags across projects, with a Random Forest model that predicts which projects will miss the quality gate using signals available in the first weeks.

[**View the live dashboard →**](https://audio-app-dashboard-nun6jt8bkandqfhza9xpsv.streamlit.app/)

Built from patterns I see in daily review work. All data in the repo is synthetic — it models real patterns without containing any client records.

Worth reading the "What I Got Wrong First" section. The first model reported 100% accuracy because I'd handed it two features the answer was calculated from. Target leakage. Finding and fixing it taught me more than the model did.

**[alzheimer-ai-device](https://github.com/Bhumii-AI-IoT/alzheimer-ai-device)** — EEG signal processing and ML classification for early Alzheimer's detection.

I was thinking about early detection. About families having time to prepare. About how Alzheimer's shows differently in every person. The long-term aim is a wearable that learns an individual baseline and flags when *that person* changes from *their own* normal, rather than from a population average.

What the repo does today is the step before that: group classification on real clinical recordings. OpenNeuro ds004504, 65 subjects (36 Alzheimer's, 29 controls) after excluding frontotemporal dementia cases. ROC-AUC 0.789, recall 0.722 on the Alzheimer's class, under leave-one-subject-out validation — one feature vector per subject, so no recording from a test subject appears in training. That matters with EEG, where individual recordings carry person-specific signatures.

I also compared electrode configurations relevant to the wearable concept: 9 frontal/temporal channels 0.815, 7 posterior 0.805, full 19-channel montage 0.790. I don't claim fewer electrodes are better. The spread is small enough to be noise — the only conclusion I draw is that I saw no meaningful penalty from the frontal/temporal layout in this dataset.

The first version of this pipeline ran on synthetic EEG and scored almost perfectly. The simulator was assigning fixed values per group, so the label was written into the features. I discarded it and rebuilt on real recordings. The synthetic version is still on a separate branch rather than quietly deleted.

**[ai-care-alert](https://github.com/Bhumii-AI-IoT/ai-care-alert)** — emergency alerts that account for individual needs rather than one-size-fits-all thresholds.

**[AI-IoT-Maintenance](https://github.com/Bhumii-AI-IoT/AI-IoT-Maintenance)** — predictive maintenance classification on the AI4I 2020 benchmark (UCI).

Machine failure is rare in this dataset, which is the interesting part — accuracy is close to useless when one class is under 4% of the data. The numbers that matter are on the failure class: precision 0.750, recall 0.706, PR-AUC 0.781. Catching roughly seven failures in ten, with three false alarms in every twelve flags.

Population-level, not per-machine. Learning individual machine baselines is where I'd take this next, but it needs data this benchmark doesn't contain.
---

## Registered Design Work

**UK Registered Design 6521594** — Alzheimer's Disease Prediction Device with Artificial Intelligence. A visor concept using EEG and eye-tracking. Registered with the UK IPO in April 2026.

**UK Registered Design 6521595** — Robotic Fleet Control Console. Registered April 2026.

**Indian Patent Application IN202611062464** — AI-enabled smart healthcare wearable bracelet for continuous patient monitoring. Filed May 2026, published July 2026.

These aren't finished products. They're concepts I wanted to protect because I believe the thinking is right, and the repos above are where I work out whether it holds.

---

## Research & Peer Review

I review manuscripts for **Scientific Reports** (Springer Nature), and I served as a meta-reviewer for **SPAC-AID 2026**, assessing submissions across embedded systems, biomedical devices and applied AI — FPGA-based real-time systems, adaptive medical devices, and EEG-driven machine learning frameworks.

Reviewing has taught me more about rigour than writing ever did. Reading a paper and asking *is this measured or projected, is this validated or simulated, do these two numbers agree* — that's the same instinct I use in QA, and it's the reason I caught the leakage in my own model.

---

## Tech Stack

- **Languages** — Python, SQL
- **ML & Data** — scikit-learn, pandas, NumPy
- **Visualisation** — Streamlit, Plotly, Matplotlib
- **Domains** — Audio & speech data quality, multilingual annotation, signal processing, IoT & embedded systems
- **Ways of working** — Project management (MSc), risk tracking, quality gates, peer review

---

## Background

- MSc Global Project Management — University of Essex
- BE Electronics & Communications Engineering
- AI data quality, London — audio and conversational AI training data
- Based in London

That combination — engineering fundamentals, project management methodology, and hands-on data quality work — is what the dashboard reflects. Audio data quality isn't just catching errors. It's understanding the full pipeline from signal to model output.

---

## Get in touch

Open to conversations about AI data quality, multilingual speech data, and building tools that make quality visible.

📧 bhumiishah33@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/bhumii-shah-ai-iot)

*Building systems that understand people.*
