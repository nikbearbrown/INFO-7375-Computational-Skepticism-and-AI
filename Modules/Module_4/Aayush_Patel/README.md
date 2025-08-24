Hi my name is Aayush Patel and i have joined this project on 6th August 2025 as a part of my opt. 
##Timeline##
- **Week 1** (08/08/25): Joined the botspeak meeting understood what tasks i have to perform. And also had call with project supervisor to select the topic to start work.
- **week 2** (15/8/25): This week I created a structured notebook on the Black Box Problem in AI, covering philosophical perspectives on trust, real-world case studies, and practical implications. I explored explainability techniques (LIME, SHAP, counterfactuals, interpretable models) and methods to evaluate explanation quality. The work emphasizes balancing understanding and reliability to build justified trust in AI systems.
Google Colab- https://colab.research.google.com/drive/1NHB5qAwfU0fITIdkN17MdC13LXkewmzt#scrollTo=130e06db

- **Week 3** (22/8/25): This week, I worked on a comparative review of Explainable AI (XAI) techniques. I explored model-agnostic methods (SHAP, LIME, permutation importance, counterfactuals) and model-specific methods (gradient-based, attention, rule-based, and prototype-based approaches). I compared their strengths, limitations, and evaluation metrics (fidelity, stability, robustness, human factors).
Google Colab- https://colab.research.google.com/drive/1UhlMI1AHhgJIJUk_antS4Kho4B1P4MRG


# Module 4: Explainability and Interpretability of AI Models #

# Section 1 — Philosophical Foundations: The Black Box Problem
**Central question:** *Is understanding necessary for trust?*

This notebook captures a structured research-style treatment of Topic 1 for INFO 7375 — *Computational Skepticism and AI Fluency*. It includes philosophical analysis, real-world examples, implications for AI practice, and discussion prompts.

## Learning Objectives
By the end of this module, you will be able to:
- Define the *black box problem* in AI and articulate its relation to **trust**.
- Contrast positions that claim **understanding is necessary** for trust with positions that allow **trust without full understanding**.
- Analyze real-world case studies where opacity eroded trust.
- Apply Wittgenstein’s *language games* to evaluate whether AI explanations are meaningful or merely persuasive.
- Derive practical implications for the design and governance of current AI systems.

## Explainability and Interpretability: The Black Box Problem and Trust
Modern artificial intelligence (AI) systems—especially those built on machine learning and deep neural networks—often function as “black boxes”. Their internal decision-making processes are opaque and not readily understandable by humans. We can observe the inputs and outputs, but the reasoning behind a given result remains hidden.
**This opacity raises a crucial question: Is understanding an AI system necessary for us to trust it?**
## The question is not merely technical; it touches on:
-	*Philosophical notions of knowledge and trust*
-	*Ethical considerations in AI design and deployment*
-	*Practical concerns in high-stakes applications*
## There are two primary perspectives:
- Understanding is essential — Many argue that without explanations for AI decisions, we cannot fully trust the system, especially when decisions impact human lives.
- Reliability can suffice — Others contend that trust can be built on consistent performance and demonstrated reliability, even without deep insight into the system’s inner workings.

## Sources of Opacity in Modern AI Systems

### 1.1 Technical Complexity
- Many state-of-the-art AI models (deep neural networks) have **millions of parameters** and complex non-linear interactions.
- Even developers cannot fully trace *why* a specific input leads to a specific output.

### 1.2 High-Dimensional Patterns
- Models detect subtle, non-intuitive correlations.
- **Example:** Wolf vs. Husky classification learned **“snow in background = wolf”** instead of actual animal features.
- LIME highlighted background snow as the key driver for “wolf” predictions.

### 1.3 Proprietary or Opaque Algorithms
- Example: **COMPAS** recidivism risk score (137 factors, proprietary).
- Alleged racial bias raised trust and fairness concerns.

### 1.4 Dynamic Learning Behavior
- Continuously learning models change decision logic over time.
- Explanation stability becomes a challenge.
## 1. The Black Box Problem and the Question of Trust
- AI systems are increasingly used in high-impact domains like banking, hiring, justice, and medicine. Many rely on complex models especially deep neural networks—that are inherently opaque.
- **Black box**: a system whose internal workings are not readily interpretable by users or even creators.
- **Trust**: practical reliance coupled with a normative stance (e.g., belief in competence, non-maleficence, accountability).
- **Problem statement**: If users cannot understand *why* a model made a decision, can they (or should they) trust it—especially in high-stakes contexts (healthcare, justice, mobility, finance)?

## 1.1 Key Challenges

- **Debugging and Error Correction**  
  Opaque models make it difficult to identify why an AI failed, slowing fixes and eroding safety confidence.

- **Accountability and Fairness**  
  Unexplainable decisions (e.g., loan denial, parole refusal) appear arbitrary, reducing public trust.

- **Human Autonomy**  
  In medicine, unexplained recommendations undermine informed consent and patients' decision-making power.

**Conclusion**: The black box creates an epistemological gap, a lack of understanding that directly impacts willingness to rely on AI.

## 2. Argument: Understanding as (Often) Necessary for Trust
**Core idea:** Understanding provides **reasons** for reliance.

- The core idea is that understanding provides **reasons** for us to rely on something. In human relationships, we trust people when we understand their motives and justifications. In the same way, explainability in AI provides us with an **epistemic justification**—a sound reason to believe in the AI's output.

- When we can't understand an AI, we face **epistemic opacity**. This makes it incredibly difficult to evaluate its correctness, check for bias, or ensure its safety. Without this intelligibility, trust becomes fragile or completely unwarranted. This is why **Explainable AI (XAI)** is so important; it supports crucial values like accountability, fairness, and human autonomy.

- For high-stakes fields like medicine or finance, we must demand **model intelligibility**. This can be achieved either through using models that are inherently easy to interpret or by applying reliable post-hoc explanation methods and independent audits.

## 3. Counterpoint: Trust Without Full Understanding
**Core idea:** Some forms of trust are **performance- and process-based**, not explanation-based.

- **Trust as a Pragmatic Stance:** Some argue that trust in AI is more pragmatic than philosophical. We don't need to understand an AI's inner workings, only that it is consistently reliable and accurate. This is similar to how we trust a calculator to give the right answer without knowing its circuitry.
- **Instrumentalism:** This view aligns with **instrumentalism**, the idea that it's enough for a tool or theory to work predictably, even if we don't know the underlying causal mechanisms. If an AI consistently makes good predictions and passes rigorous tests, we can rationally rely on it.
- **Trust as Reliance or Confidence:** We might be misusing the word "trust" when talking about AI. Perhaps it's more accurate to describe our relationship as one of **confidence** or **reliance**. This confidence can be earned through statistical performance, independent audits, and safety guarantees, rather than transparent explanations.
- **Institutional Trust:** We can also trust an AI based on the reputation of the institutions that developed and validated it. For example, trusting an AI-powered medical device because it was approved by a respected regulatory body.

### 2. The Nuances of the Counterpoint

- This perspective doesn't completely dismiss the value of transparency. Instead, it suggests that understanding is not the **only** path to trust.
- The nature of AI is different from humans. Since AI lacks intentions, what matters most is the trustworthiness of the developers, the validation processes, and the system's track record, even if the decision-making process itself remains a black box.

## 4. Real-World Consequences of Opacity: When Lack of Understanding Erodes Trust

The connection between **understanding** and **trust** is not merely theoretical—it has tangible impacts in real-world AI deployments. Lack of explainability has repeatedly led to failures, public backlash, and erosion of confidence in AI systems.

### 1. Healthcare — IBM Watson for Oncology
IBM’s AI system for cancer treatment recommendations struggled to gain physician trust. Studies found that Watson for Oncology *“failed largely because it could not provide any rationale for its diagnoses”*, especially when its suggestions conflicted with doctors’ clinical judgment. Without a clear explanation for why a treatment was recommended, physicians defaulted to their own expertise. In **life-and-death decisions**, understanding is essential for trust.

### 2. Autonomous Vehicles
In 2019, a self-driving car on autopilot failed to recognize a crossing tractor-trailer and did not brake, resulting in a fatal crash. The vehicle’s decision-making process remained a **black box**—even post-incident investigations could not fully explain why the AI vision system missed the truck. Incidents like this undermine public trust; if neither engineers nor users can explain AI failures, people will be hesitant to rely on them in safety-critical contexts.

### 3. Facial Recognition and Justice
In 2018, a facial recognition system used by police misidentified multiple innocent individuals as criminal suspects, leading to at least one wrongful arrest. The model’s inner workings—likely biased against certain demographics—were opaque. Without transparency, officers and defendants could not effectively challenge the results, fueling **public distrust** in AI-based law enforcement tools.

### 4. Predictive Policing Algorithms
Some jurisdictions have deployed “black box” crime-prediction models. In a 2019 case, a proprietary system—later shown to be trained on biased historical data—disproportionately flagged minority neighborhoods and individuals, contributing to wrongful arrests. Because the algorithm’s decision logic was hidden, communities could not assess its fairness, and officials could not justify its use. This shows how **opacity can conceal bias**, enabling unethical outcomes and eroding community trust.

---

### Key Insight
Across healthcare, transportation, and law enforcement, one pattern emerges: **when AI decisions have high stakes, the absence of understandable reasoning causes people to withhold trust**.

### Industry and Regulatory Response
To address this, there is growing adoption of **Explainable AI (XAI)** practices. Industries from medicine to finance acknowledge that to *“reach AI’s full potential, we must either open the black boxes or develop alternative methods to ensure responsible AI development and cultivate trust.”*  

Governments are also acting. For example, the **European Union’s AI Act (2024)** mandates explainability for **high-risk AI applications**, explicitly aiming to ensure that such systems are *fair, unbiased, and accountable*. These initiatives reflect a core intuition: an AI that cannot explain its decisions should not be trusted to make consequential choices.


# 5. Techniques to Open the Box 

A summary of common methods for interpreting and understanding machine learning models.

 **5.1. Local Attribution** 

These methods explain why a model made a specific prediction for a single instance.

 **LIME (Local Interpretable Model-agnostic Explanations)**
* **Mechanism:** Uses local surrogate models on perturbed data samples.
* **Strength:** It's model-agnostic, meaning it can be applied to any model.
* **Weakness:** Can be unstable, especially with correlated features.

 **SHAP (SHapley Additive exPlanations)**
* **Mechanism:** Based on Shapley value attributions from game theory.
* **Strength:** Provides consistent and theoretically sound explanations.
* **Weakness:** Involves heavier computation.

> **Important Note:** For both LIME and SHAP, remember that **correlation != causation**.

---

 **5.2. Counterfactual Explanations** 
These explanations show the smallest change needed to flip a model's outcome, providing clear steps for recourse.

* **Core Idea:** Find minimal changes to features that alter the prediction.
* **Example:** "The loan would be **approved** if annual income were +$5k."
* **Primary Use:** Excellent for providing actionable **recourse** to users.

---

 **5.3. Global Understanding** 

These techniques explain the overall behavior of the model across the entire dataset.

* **Permutation Importance:** Measures a feature's importance by observing how shuffling its values impacts model performance.
* **PDP / ICE / ALE:** Used to visualize marginal effects and interactions between features.
* **Surrogate Trees/Rules:** A simpler, transparent model (like a decision tree) is trained to approximate the black box model. Requires **fidelity checks** to ensure it's a good approximation.

---

 **5.4. Intrinsic Models** 

These models, also known as "glass-box" models, are interpretable by design.

* **CORELS:** Creates optimized and certifiable rule lists (e.g., if-then-else statements).
* **GAM / EBM (Generalized Additive Models / Explainable Boosting Machines):** Models are additive, allowing for the visualization and editing of individual feature contributions ("shapes").
* **Monotonic GBMs:** Gradient Boosting Machines constrained to ensure a monotonic (always increasing or decreasing) relationship for specific features.

---

**5.5. Concept-level & Data-level Explanations** 

These methods connect model behavior to high-level concepts or specific training examples.

* **TCAV (Testing with Concept Activation Vectors):** Quantifies the importance of human-understandable concepts (e.g., "stripes" for a "zebra" prediction).
* **Influence Functions / TracIn:** Attributes a prediction back to the most influential points in the training data.
* **Data Shapley / Data Valuation:** Assigns a value to each training example based on its contribution to model performance, helping to find the most impactful data points. 

---

**5.6. Neural Net Visualization** 

Techniques specifically for visualizing the inner workings of neural networks.

* **Saliency / Grad-CAM:** Used in computer vision to create heatmaps that highlight the input pixels the model focused on.
* **Attention Probing:** Used in NLP to analyze which words a model "pays attention to" when making a prediction.
* **Sanity Checks:** It is critical to use randomization tests to ensure the heatmaps and visualizations are genuinely reflecting the model's logic and are not misleading.


<a id="evaluation"></a>
## 6. Evaluating Explanation Quality

 6.1 Faithfulness Tests
- **Deletion/Insertion curves:** Remove top‑attributed features; prediction should degrade.
- **Counterfactual consistency:** Attributions predict outcome flips.

 6.2 Stability & Robustness
- **Repeatability under noise**/resampling; quantify variance of explanations.
- **Correlation sensitivity:** Use **conditional** methods when features correlate.

 6.3 Human‑ vs. Function‑ vs. Application‑Grounded Eval
- **Human‑grounded:** Simpler tasks with lay users.
- **Function‑grounded:** Synthetic tasks with ground‑truth mechanisms.
- **Application‑grounded:** Real stakeholders, domain tasks (gold standard).

 6.4 Calibration & Uncertainty
- **ECE** / **Brier score** for probabilistic calibration.
- **Conformal prediction** to provide valid uncertainty sets.

## 7. Wittgenstein’s Language Games: Are AI Explanations Meaningful?
- **Language games**: Meaning is rooted in **use** within shared social practices (forms of life).
- **Question**: When AI systems provide post-hoc *explanations*, are these part of the same *game*—i.e., do they offer **reasons** we can critique—or are they **persuasive artifacts** that mimic human justification?
- **Risk**: Post-hoc methods (e.g., perturbation-based or attribution methods) can produce **plausible but unfaithful** narratives, creating *illusion of understanding*.
- **Design implication**: Prefer **faithful** explanation techniques and **interpretability-by-design** where feasible; evaluate explanations for **stability, fidelity, and actionability**.

## 8. Practical Implications for AI Systems
- **Risk-tiered explainability**: Demand stronger intelligibility for **high-risk** applications (health, justice, safety-critical systems).
- **Model choice**: Use **inherently interpretable** models when performance is comparable; otherwise, combine with **faithful** explanation methods.
- **Assurance cases**: Treat trust as a **system property**—evidence via testing, formal verification (where possible), monitoring, and incident response.
- **Governance & documentation**: Model cards, data statements, audit trails, and impact assessments.
- **Human factors**: Design explanations for the **intended audience** (clinician, regulator, end-user), with clarity about **limits and uncertainty**.


## 9. Synthesis & Conclusion
- **Takeaway**: Understanding is a powerful foundation for **justified trust**, especially in high-stakes settings. However, **performance- and process-based trust** can sometimes suffice in low-stakes or rigorously validated contexts.
- **Balanced stance**: Combine **intelligibility** (when feasible) with **robust validation, governance, and oversight**. Avoid overreliance on persuasive but unfaithful post-hoc narratives.


## 10. Sources
- Ribeiro, Singh, Guestrin (2016): LIME — “Why Should I Trust You?” (wolf‑vs‑husky).

- Lundberg & Lee (2017): SHAP — unified approach to interpreting predictions.

- Rudin (2019): *Stop Explaining Black Boxes* — use interpretable models in high‑stakes.

- Wang et al. (2022): *Interpretability, Then What?* — pneumonia model & practice.

- Datasheets for Datasets; Model Cards for Model Reporting.

- TCAV (2018): Concept‑based explanations.

- https://www.wilsoncenter.org/blog-post/developing-trust-black-box-ai-explainability-and-beyond#:~:text=For%20instance%2C%20according%20to%20a,of%20distrust%20due%20to%20their

- https://trendsresearch.org/insight/unveiling-the-black-box-towards-explainable-ai-and-responsible-innovation-in-the-gcc/?srsltid=AfmBOoqPdvXEacpLHIy8rt7GWSOnPSp13uJ7TiT7OnSnNmZGZknMpLdi#:~:text=,5
