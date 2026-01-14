# A/B Testing and Experimentation: A Data Science Perspective

This repository explores the importance of A/B testing and experimentation in data science. It covers the benefits of rigorous experimentation, common pitfalls like false positives, peeking, p-hacking, and the false discovery rate (FDR), and demonstrates these concepts through Python simulations along with collecting relevant further reading.

## Table of Contents
1. [Introduction](#introduction)
2. [Why We Experiment](#why-we-experiment)
3. [The Importance of Strict Methodology](#the-importance-of-strict-methodology)
4. [Common Pitfalls in A/B Testing](#common-pitfalls-in-ab-testing)
5. [Common Misconceptions](#common-misconceptions)
6. [Addressing Concerns: Speed and Reliability](#addressing-concerns-speed-and-reliability)
7. [Simulations](#simulations)
8. [Best Practices](#best-practices)
9. [Further Reading](#further-reading)

## Introduction
A/B testing is a cornerstone of data-driven decision-making, enabling businesses and researchers to evaluate the impact of changes in a controlled and measurable way. However, without strict methodology, experimentation can lead to unrealiable or misleading conclusions. This project highlights the importance of rigorous experimentation and demonstrates key concepts through Python simulations.

## Why We Experiment
Experimentation allows us to:
- Make an objective and evaluate a new product agaisnt it allowing for data-driven decisions.
- Establish causal relationships.
- Iteratively improve products, strategies, or processes.
- Mitigate risks by testing changes on a small scale.

## The Importance of Strict Methodology
Following a strict methodology ensures:
- Valid hypothesis testing (e.g., null and alternative hypotheses, p-values).
- Proper randomisation and sample size determination.
- Avoidance of biases (e.g., blinding, control groups).

## Common Pitfalls in A/B Testing
This project explores the following pitfalls through simulations:
- **False Positives (Type I Errors)**: Detecting an effect when there isn’t one.
- **Peeking**: Checking results before the experiment is complete, leading to inflated false positive rates.
- **P-Hacking**: Manipulating data or tests to achieve statistically significant results.
- **False Discovery Rate (FDR)**: The proportion of false positives among all significant results.

## Common Misconceptions
There are several common misconceptions about A/B testing and experimentation that can lead to poor decisions:

1. **"More Data Always Leads to Better Results"**:
   - While larger sample sizes increase statistical power, they can also lead to detecting trivial effects that are not practically meaningful.
   - Proper sample size calculation is essential to balance power and relevance.
   - A different story for continuous metrics...

2. **"Peeking at Results is Harmless"**:
   - Checking results before the experiment is complete can inflate the false positive rate, leading to incorrect conclusions.
   - Sequential testing methods should be used if interim analyses are necessary.

3. **"A/B Testing is Only for Large Companies"**:
   - A/B testing can be valuable for organizations of all sizes, as long as the experiments are designed and executed properly.
   - Even small-scale tests can provide actionable insights.

4. **"All Metrics are Equally Important"**:
   - Not all metrics are equally relevant to the hypothesis being tested.
   - Focusing on too many metrics can increase the risk of false discoveries (multiple comparisons problem).

5. **"A/B Testing is Only for Websites and Apps"**:
   - A/B testing principles apply to a wide range of fields, including marketing, healthcare, education, and more.
   - The methodology can be adapted to any context where causal inference is needed.

## Addressing Concerns: Speed and Reliability
A common criticism of A/B testing is that it "slows you down" and that false positive/false discovery rates make the results unreliable. Let’s address these concerns:

### **1. "A/B Testing Slows You Down"**
- **Misconception**: A/B testing is seen as a bottleneck because it requires time to design, run, and analyze experiments.
- **Reality**:
  - While A/B testing does require upfront effort, the long-term benefits far outweigh the costs. Making decisions based on flawed or untested assumptions can lead to costly mistakes.
  - **Speed vs. Rigor**: It’s possible to balance speed and rigor by:
    - Using **sequential testing methods** that allow for early stopping if results are clear.
    - Prioritizing high-impact experiments that align with business goals.
    - Automating the setup and analysis of experiments to reduce manual effort.
      
### **2. "False Positives and False Discovery Rates are High"**
- **Misconception**: Because false positives occur, A/B test results are often seen as unreliable.
- **Reality**:
  - High False positives rates and high FDRs are typically the result of **poor methodology**, not an inherent flaw in A/B testing itself. Common issues include:
    - **Peeking**: Checking results repeatedly and stopping the test early when significance is reached.
    - **P-Hacking**: Testing multiple hypotheses or metrics without proper correction.
    - **Inadequate Sample Sizes**: Running tests with insufficient power to detect meaningful effects.
  - **Solutions**:
    - **Pre-registration**: Define hypotheses, metrics, and analysis plans before running the experiment.
    - **FDR Control**: Use methods like the Benjamini-Hochberg procedure to control the false discovery rate.
    - **Proper Sample Sizes**: Conduct power analysis to ensure the test is designed to detect meaningful effects.
    - **Transparency**: Report all results, including non-significant findings, to avoid cherry-picking.

### **3. "A/B Testing is Not Worth the Effort"**
- **Misconception**: The perceived high rate of false discoveries and the time required make A/B testing seem like a poor investment.
- **Reality**:
  - A/B testing is a **learning tool**. Even "failed" experiments provide valuable insights by ruling out ineffective changes.
  - The cost of **not testing** can be much higher. For example:
    - Rolling out a change that harms user experience or revenue.
    - Missing opportunities to improve key metrics because of untested assumptions.
  - By following best practices, A/B testing becomes a reliable and efficient way to make data-driven decisions.

### **4. "Why Not Just Rely on Intuition or HiPPO?"**
- **Misconception**: Human intuition or the highest paid person's opinion (HiPPO) is a faster and more reliable way to make decisions.
- **Reality**:
  - While intuition and experience have their place, they are inherently subjective and prone to biases.
  - A/B testing provides **objective evidence** to support or challenge ideas, reducing the risk of costly mistakes.
  - The alternative—relying on intuition—often leads to **inconsistent outcomes** and **missed opportunities** for improvement.
    
## Simulations
The repository includes Python notebooks that simulate A/B tests to demonstrate the impact of poor methodology:
1. **Peeking**: Showing how interim analyses increase the likelihood of false positives.
2. **P-Hacking**: Demonstrating how selective reporting can lead to misleading conclusions.
3. **False Discovery Rate (FDR)**: Applying FDR control methods to reduce false discoveries.

## Best Practices
As mentioned rigourous methodology is key such as:
- Pre-registering hypotheses and analysis plans.
- Using sequential testing methods if peeking is necessary.
- Controlling for multiple comparisons using FDR or Bonferroni correction.
- Reporting all results transparently.

## Further Reading
# Influential and Important Literature on A/B Testing

This document curates foundational, academic, and practitioner-oriented literature on A/B testing and online controlled experimentation.

---

## I. Foundational Works (Experimental Design & Statistics)

- **R.A. Fisher - _The Design of Experiments_ (1935)**  
  Foundational work introducing randomization, control groups, and hypothesis testing.  
  - Free archive copy:  
    https://archive.org/details/in.ernet.dli.2015.502684

- **Box, G.E.P., Hunter, J.S., & Hunter, W.G. - _Statistics for Experimenters_**  
  A core reference on design of experiments and statistical modeling.  
  - Book page:  
    https://www.wiley.com/en-us/Statistics+for+Experimenters%2C+2nd+Edition-p-9780471718130  
  - Online PDF copy (verify license before use):  
    https://vdoc.pub/documents/statistics-for-experimenters-design-innovation-and-discovery-g6ef8sdj3fc0

---

## II. Core Books on A/B Testing and Online Experiments

- **Kohavi, R., Tang, D., & Xu, Y. - _Trustworthy Online Controlled Experiments_ (2020)**  
  The definitive industry guide to large-scale online experimentation.  
  - Publisher page (Cambridge University Press):  https://www.cambridge.org/core/books/trustworthy-online-controlled-experiments/D97B26382EB0EB2DC2019A7A7B518F59  
  - Official Chapter 1 PDF:  https://experimentguide.com/wp-content/uploads/TrustworthyOnlineControlledExperiments_PracticalGuideToABTesting_Chapter1.pdf  
  - ResearchGate full-text upload (author-provided):  https://www.researchgate.net/publication/339914315_Trustworthy_Online_Controlled_Experiments_A_Practical_Guide_to_AB_Testing

- **Georgi Z. Georgiev - _Statistical Methods in Online A/B Testing_ (2019)**  
  Practical statistical guidance for real-world experimentation.  
  - Official site:   https://www.abtestingstats.com/  
  - Amazon page:  https://www.amazon.com/dp/1694079724

---

## III. Related Books

- **Lattimore, T. & Szepesvári, C. - _Bandit Algorithms_**  
  Rigorous treatment of adaptive experimentation and exploration–exploitation trade-offs.  
  - Free PDF (official):  https://tor-lattimore.com/downloads/book/book.pdf

- **Croll, A. & Yoskovitz, B. - _Lean Analytics_**  
  Metrics-driven experimentation and decision-making.  
  - Book page:   https://leananalyticsbook.com/

- **Leonard Mlodinow - _The Drunkard’s Walk_**  
  Conceptual exploration of randomness and probability.  
  - Book page:  https://www.penguinrandomhouse.com/books/305605/the-drunkards-walk-by-leonard-mlodinow/

- **Nassim Nicholas Taleb - _The Black Swan_**  
  On uncertainty, rare events, and limits of statistical inference.  
  - Book page:  https://www.penguinrandomhouse.com/books/307644/the-black-swan-by-nassim-nicholas-taleb/

---

## IV. Influential Academic Papers (Open Access)

- **Larsen et al. (2022) - _Statistical Challenges in Online Controlled Experiments_**  
  Comprehensive review of modern A/B testing methodology.  
  - arXiv PDF:  
    https://arxiv.org/abs/2212.11366

- **Jeunen (2023) - _A Common Misassumption in Online Experiments with Machine Learning Models_**  
  Examines incorrect assumptions in ML-driven A/B tests.  
  - arXiv PDF:  
    https://arxiv.org/abs/2304.10900

- **Xie et al. (2018) - _False Discovery Rate Controlled Heterogeneous Treatment Effect Detection_**  
  Subgroup analysis with false discovery control.  
  - arXiv PDF:  
    https://arxiv.org/abs/1808.04904

- **Guo & Deng (2015) - _Flexible Online Repeated Measures Experiment_**  
  Introduces repeated-measures designs for variance reduction.  
  - arXiv PDF:  
    https://arxiv.org/abs/1501.00450

---

## V. Practitioner Articles

- **Kohavi et al. - _Practical Guide to Controlled Experiments on the Web_ (KDD 2007)**  
  One of the earliest and most influential practitioner papers.  
  - Author-hosted version:  https://exp-platform.com/practical-guide/

- **Evan Miller - _How Not to Run an A/B Test_**  
  Classic explanation of common A/B testing mistakes.  
  - Article:  https://www.evanmiller.org/how-not-to-run-an-ab-test.html

---

## VI. Industry Articles and Engineering Blogs on Experimentation

Large technology companies have published influential articles describing how A/B testing is implemented at scale, including statistical innovations, infrastructure design, and organizational lessons.

---

### Google

Google is one of the earliest and most influential adopters of large-scale online experimentation.

- **Kohavi et al. - _Online Controlled Experiments at Large Scale_**  
  Discusses scaling experimentation infrastructure and decision-making.  
  https://ai.googleblog.com/2011/04/online-controlled-experiments-at.html

---

### Meta 

Meta has published extensively on experimentation, metrics, and statistical rigor.

- **Deng et al. - _Improving the Sensitivity of Online Controlled Experiments_**  
  Introduces CUPED, a variance reduction technique now widely used across the industry.  
  https://www.exp-platform.com/Documents/2013-02-CUPED-ImprovingSensitivityOfControlledExperiments.pdf

- **Xu et al. - _Designing Online Experiments with Metric Guardrails_**  
  Discusses balancing multiple metrics and preventing unintended regressions.  
  https://engineering.fb.com/2016/03/29/data-infrastructure/designing-online-experiments-with-metric-guardrails/

---

### Microsoft

Microsoft’s experimentation platform work strongly influenced modern A/B testing practice.

- **Kohavi et al. - _Controlled Experiments on the Web: Survey and Practical Guide_**  
  Early survey of experimentation practices across large web companies.  
  https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/controlledeexperiments.pdf

- **Dmitriev et al. - _A Dirty Dozen: Twelve Common Metric Interpretation Pitfalls in Online Controlled Experiments_**  
  Highly cited paper on common mistakes in experiment analysis.  
  https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/dirtydozen.pdf

---

### Expedia Group
- **Ronny Kohavi & Nanyu Chen - False Positives in A/B Tests*
Discusses false postives results in A/B testing at scale.
https://dl.acm.org/doi/abs/10.1145/3637528.3671631
  
- **Preventing Revenue Loss With Real-Time A/B Test Monitoring**  
Expedia Group Technology engineers describe building a real-time A/B test monitoring and automatic suspension system using Apache Flink. This system is part of their internal platform (Expedia Group Test & Learn) to detect and stop poorly performing experiments within minutes. 
https://medium.com/expedia-group-tech/preventing-revenue-loss-with-real-time-a-b-test-monitoring-605698817457

- **How to Size For Online Experiments With Ratio Metrics**  
An Expedia Group Technology article that explains **statistical sample size calculations for online experiments with ratio metrics** — important for proper design and power analysis in frequent experimentation contexts.
https://medium.com/expedia-group-tech/how-to-size-for-online-experiments-with-ratio-metrics-3d57362f1967

- **Measuring Marketing Success: The Power of Incrementality and Geo Testing**  
An article from Expedia Group Technology that discusses **geo testing and incrementality analysis**, including statistical methods extending beyond traditional A/B tests. 
https://medium.com/expedia-group-tech/measuring-marketing-success-the-power-of-incrementality-and-geo-testing-1acd4291545d

---

### Booking.com

Booking.com is known for its strong experimentation culture and decentralized testing model.

- **Booking.com - _Experimentation at Booking.com_**  
  Overview of large-scale experimentation culture and infrastructure.  
  https://booking.ai/experimentation-at-booking-com-1e2e2f9d0a7f

- **Ronny Kohavi & Lukas Vermeer - _The Power of Online Experiments_ (Booking.com Tech Talks)**  
  Discusses organizational and statistical challenges of experimentation.  
  https://booking.ai/the-power-of-online-experiments-6d4e90b1c98c
  
- **Role of Experimentation at Booking.com** (Booking.com partner magazine)  
  Overview of how experimentation is embedded in product culture.  
  https://partner.booking.com/en-gb/click-magazine/industry-perspectives/role-experimentation-bookingcom
  
- **Understanding Mechanisms of Change in Online Experiments at Booking.com**  
  Discusses mediation analysis in A/B testing and organizer practices.  
  https://booking.ai/understanding-mechanisms-of-change-in-online-experiments-at-booking-com-629201ec74ee 

- **Democratizing Online Controlled Experiments at Booking.com (arXiv)**  
  Academic paper by Vermeer et al. explaining Booking.com’s experimentation system and culture.  
  https://arxiv.org/abs/1710.08217 ]
---

### Spotify

Spotify publishes articles focused on experimentation in product development and personalization.

- **Spotify Engineering - _Experimentation at Spotify_**  
  Overview of experimentation practices used across product teams.  
  https://engineering.atspotify.com/2019/10/experimentation-at-spotify/

- **Spotify R&D - _ABBA: A/B Testing at Scale_**  
  Discusses internal tools and experimentation workflows.  
  https://engineering.atspotify.com/2020/01/abba-ab-testing-at-scale/

- **Experiment like Spotify: A/B Tests and Rollouts**  
  Discusses how Spotify uses A/B tests and rollouts for product development and safe rollout practices.  
  https://confidence.spotify.com/blog/ab-tests-and-rollouts 

- **Risk-Aware Product Decisions in A/B Tests with Multiple Metrics**  
  Describes how Spotify integrates success, guardrail, and quality metrics into decision rules for experiments.  
  https://engineering.atspotify.com/2024/3/risk-aware-product-decisions-in-a-b-tests-with-multiple-metrics 

- **Better Product Decisions with Guardrail Metrics**  
  Discusses how experimentation supports broader product decisions with multi-metric tracking.  
  https://confidence.spotify.com/blog/better-decisions-with-guardrails

---

### eBay

eBay has published influential work on experimentation and causal inference especially in the context of a two sided marketplace.

- **Increase A/B Testing Power by Combining Experiments**  
  eBay explains using a weighted z-test to combine results from multiple tests to increase power.  
  https://innovation.ebayinc.com/stories/increase-a-b-testing-power-by-combining-experiments/ 

- **Measuring Success with Experimentation – eBay Innovation Stories**  
  Offers practical guidance on how eBay frames success metrics and measurement strategies.  
  https://innovation.ebayinc.com/stories/measuring-success-with-experimentation/ 

- **Discussion on eBay Experimentation Systems** (industry podcast/summary)  
  A conversation about cultural and technical challenges at eBay.  
  https://brianpoe.substack.com/p/experimentation-at-ebay-with-benjamin 


---

### Netflix

Netflix focuses on experimentation for personalization and streaming quality.

- **Netflix Tech Blog - _A/B Testing at Netflix_**  
  Explains how experimentation supports personalization and UI decisions.  
  https://netflixtechblog.com/ab-testing-at-netflix-6b1eb38c93e5

- **Netflix Tech Blog – _Challenges in Online Controlled Experiments_**  
  Discusses statistical and practical challenges unique to streaming services.  
  https://netflixtechblog.com/challenges-in-online-controlled-experiments-66b7a8c6bb4d

---

### Additional Engineering or Third-Party Summaries

- **Deconstruction of Experimentation Infrastructure (Swati’s Blog)**  
  Covers practices at Netflix, Booking.com, and others in the context of building experimentation systems.  
  https://deconstructwithswati.com/blog/experimentation-infrastructure-ab-testing-in-practice 

- **Industry A/B Testing Lessons (Deepak Karkala)**  
  Summarizes experimentation platform practices across platforms including Netflix, Twitter, DoorDash, and more.  
  https://deepak-karkala.github.io/blog/mlops/ch12_retrain_online_testing/guide_ab_testing_industry_lessons.html 

---
