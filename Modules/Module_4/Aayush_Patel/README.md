Hi my name is Aayush Patel and i have joined this project on 6th August 2025 as a part of my opt. 
## Timeline ##
- **Week 1** (08/08/25): Joined the botspeak meeting understood what tasks i have to perform. And also had call with project supervisor to select the topic to start work.
- **week 2** (15/8/25): This week I created a structured notebook on the Black Box Problem in AI, covering philosophical perspectives on trust, real-world case studies, and practical implications. I explored explainability techniques (LIME, SHAP, counterfactuals, interpretable models) and methods to evaluate explanation quality. The work emphasizes balancing understanding and reliability to build justified trust in AI systems.
Google Colab- https://colab.research.google.com/drive/1NHB5qAwfU0fITIdkN17MdC13LXkewmzt#scrollTo=130e06db

- **Week 3** (22/8/25): This week, I worked on a comparative review of Explainable AI (XAI) techniques. I explored model-agnostic methods (SHAP, LIME, permutation importance, counterfactuals) and model-specific methods (gradient-based, attention, rule-based, and prototype-based approaches). I compared their strengths, limitations, and evaluation metrics (fidelity, stability, robustness, human factors).
Google Colab- https://colab.research.google.com/drive/1UhlMI1AHhgJIJUk_antS4Kho4B1P4MRG

- Completed 1 Video on Black Box Problem 
  Google Drive: https://drive.google.com/drive/folders/15RVAtVj4JHLX74FTOggm89Kic7z1VS38

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



#Section 2 Explainable AI (XAI) Techniques: A Comparative, Practice‑Focused Review



## Abstract
Explainable AI techniques aim to open the “black box” of complex models by illuminating how inputs influence outputs.
Explainable AI (XAI) aims to make model behavior understandable to developers, regulators, and end users. This notebook reviews state‑of‑the‑art **model‑agnostic** and **model‑specific** techniques—SHAP, LIME, permutation/feature importance, counterfactuals, gradient‑based and attention mechanisms, rule‑based models, and prototype/example‑based methods—drawing on published papers, official docs, and widely used tools. We compare strengths, limitations, evaluation practices (fidelity, stability, robustness, human factors), and map each method to stakeholders and real‑world uses.  


## 1. Introduction
As ML systems affect credit, health, hiring, and other high‑stakes domains, stakeholders increasingly require **transparent reasoning** and **auditable decisions**. Interpretability is multifaceted: post‑hoc explanations can be useful while also being fragile if not validated. This motivates a comparative, technique‑by‑technique review anchored in rigorous evaluation and practice guidance ([3], [18]).


## 2. Model‑Agnostic Techniques

### 2.1 SHAP (Shapley Additive Explanations)
**Idea.** SHAP attributes a prediction to features via Shapley values from cooperative game theory, guaranteeing local additivity and other axioms under defined conditions. Implementations include KernelSHAP, TreeSHAP, and DeepSHAP. **Aggregation of local SHAP values yields global importance**, providing a unified view across granularities ([1], [3]).  
**Limitations.** Computational cost (mitigated for trees by TreeSHAP); care required with highly correlated features; post‑hoc attributions are not causal ([1], [3]).
**Examples**
1. **NVIDIA finance case** (government-cited): The UK Government’s AI Assurance repository highlights an NVIDIA credit-risk SHAP case (e.g., clustering SHAP values to understand portfolio drivers, speeding analyses from days to minutes on GPUs).
Source: https://www.gov.uk/ai-assurance-techniques/nvidia-explainable-ai-for-credit-risk-management-applying-accelerated-computing-to-enable-explainability-at-scale-for-ai-powered-credit-risk-management-using-shapley-values-and-shap?
2. **CrowdStrike** (cybersecurity EDR): Applies SHAP TreeExplainer/DeepExplainer to surface the suspicious tokens/APIs driving a detection (e.g., malicious PowerShell), improving analyst triage/insight.
Source: https://www.crowdstrike.com/en-us/blog/ai-decision-making-with-shap/?
3. **Upstart** (consumer lending): Uses SHAP to generate adverse action notice (AAN) reasons and to analyze feature reliance in underwriting. In a submission to the U.S. Federal Reserve, Upstart reports its AI model approved 26% more borrowers at 10% lower APRs than “high-quality traditional lending models” (method: CFPB comparison methodology); SHAP is cited as an enabling technique for reasons/AANs.
Source: https://www.federalreserve.gov/SECRS/2022/October/20221028/OP-1743/OP-1743_070121_138216_351653676425_1.pdf
4. **ING Bank** (credit risk): Open-sourced ShapRFECV for feature selection with SHAP. In one production credit-risk model, eliminated 60 of 110 features with slightly higher AUC and significantly faster inference; ING subsequently open-sourced the technique in the Probatus package. Source: https://medium.com/ing-blog/open-sourcing-shaprfecv-improved-feature-selection-powered-by-shap-994fe7861560
5. **Affirm** (point-of-sale lending): Built Shparkley, a Spark-based Monte-Carlo Shapley implementation to scale explanations to large datasets/models, observing a 50–60× runtime improvement vs. the popular shap package with minimal difference in values. Source: https://tech.affirm.com/shparkley-scaling-shapley-values-with-spark-for-interpreting-machine-learning-models-8c9bc9574d70
6. **Mayo Clinic** (omics): Reports using SHAP for interpretable multi-omics in a health context (omics footprinting). Source: https://www.researchgate.net/publication/374548113_THE_ROLE_OF_EXPLAINABLE_AI_IN_FRAUD_DETECTION_OF_INSURANCE_CLAIMS_2

**Comparative evidence**
- In credit-risk benchmarks, SHAP often yields more discriminative/consistent attributions than LIME; e.g., Frontiers study using XGBoost on Italian SME default shows better discriminative power and ROC behavior for SHAP vs. LIME.  ￼ ￼
- Note stability cautions: with class imbalance, both SHAP and LIME explanations can be less stable, requiring care (resampling, calibration).
**Best-fit uses**: Regulated decisions (credit AANs), model debugging & feature governance, portfolio & fraud analytics.


### 2.2 LIME (Local Interpretable Model‑agnostic Explanations)
**Idea.** LIME fits an interpretable surrogate (often sparse linear) around a single prediction using perturbed samples weighted by proximity, yielding a local explanation across modalities (tabular, text, image) ([2]).  
**Limitations.** Explanations can be **unstable** across runs due to sampling; local fidelity does not imply global faithfulness; requires careful configuration and checks ([2], [26]).
**What it does**: Trains a simple local surrogate (e.g., sparse linear model) around a specific instance to explain a black-box prediction.

**Real-world/organizational usage**
1) **Banco de España (Spain’s Central Bank)** — Mortgage Default Risk (Evaluation for Supervisory Transparency)
- **Who / setting**: Banco de España’s Financial Stability Review case study on credit risk (“Unwrapping black-box models”).  ￼
- Use case: Explain a production-grade credit risk model for Spanish mortgages to enable supervisory transparency; LIME was one of the interpretability tools assessed (with SHAP, PDP/ALE, etc.).  ￼
- **Model / data**: Neural network with two hidden layers (128 units each), 24,577 parameters; dataset = 3,184,956 mortgage records, default rate 0.61% (extremely imbalanced). Validation AUC = 89.96%.  ￼
- **How LIME was used**: As a local surrogate to explain individual predictions to analysts/regulators; part of a toolkit the central bank used to “unbox” the model and compare methods’ practicality/assumptions.  ￼
- **Outcomes / takeaways**: Concrete performance baseline (AUC 89.96% at 0.61% default); LIME provided instance-level reasons alongside other tools, informing supervisory review under EU transparency expectations. (The paper also notes SHAP’s computational trade-offs and independence assumptions.)  
Source: https://www.bde.es/f/webbde/GAP/Secciones/Publicaciones/InformesBoletinesRevistas/RevistaEstabilidadFinanciera/22/4_FSR43_Black.pdf

2) **PayPal — Real-Time Fraud Detection** (Production)
- **Who / setting**: PayPal’s enterprise fraud prevention platform (12B+ transactions/year).
- **Use case**: Per-transaction explanations in production to help fraud analysts and clients understand why an event was flagged; explanations shown as an “interpretability plot for every single event.”
- **How LIME was used**: PayPal reports using LIME and Shapley values to generate per-event interpretability plots so reviewers can see the key drivers (e.g., amount/device/location anomalies) behind each risk score.
- **Outcomes / scale**: Operationalized explainability at PayPal scale (12B+ events/year); used for compliance, client trust, and analyst review efficiency. (Public source quantifies scope and method, not specific KPI deltas.)
Sources: https://thepaypers.com/fraud-and-fincrime/expert-views/why-explainability-is-key-to-success-in-machine-learning , https://www.chiefaiofficer.com/post/how-paypal-ai-blocks-500-million-fraud-quarterly-using-500-data-points


Comparative takeaways: LIME is easy to communicate and quick to prototype, but multiple studies show higher variance and lower discriminative power than SHAP in credit-risk contexts; stability can degrade under imbalance.  

Best-fit uses: Rapid what-if exploration, stakeholder demos when compute/latency are constrained—paired with validation checks for stability.


### 2.3 Permutation Feature Importance
**Idea.** Measure the drop in performance when shuffling a feature to break its relation to the target—simple, **model‑agnostic global** importance evaluated on hold‑out data. Preferable to impurity‑based importances (which can be biased toward high‑cardinality features) ([4], [25]).
**What it does**: Randomly permutes a feature to measure drop in performance—model-agnostic global importance; complements local methods like SHAP/LIME.

**Notes in practice**
- Common in production ML stacks (e.g., scikit-learn pipelines) to validate or cross-check global drivers surfaced by SHAP/LIME; often included in compliance model documentation alongside partial dependence/ICE. (Use alongside the method-specific evidence above.)


### 2.4 Counterfactual Explanations (“What‑if?”)
**Idea.** Provide minimal, plausible changes to input that would flip the decision—useful for user recourse and audits without opening the black box. Counterfactuals should respect feasibility and domain constraints; they are not causal claims by default ([5]).
**What it does**: Shows minimal changes to inputs needed to flip a decision (actionable recourse).

**Status & signals**
- CF-SHAP (research/industry interest): Variant that uses counterfactual-based backgrounds to increase “counterfactual-ability” vs. baseline attributions across multiple datasets. Useful for recourse-oriented UIs.  
- Banking research: Multiple credit-risk studies evaluate counterfactual generation for loan decisions; emphasize plausibility, sparsity, and validity trade-offs before customer-facing use.  

Best-fit uses: Customer recourse tooling, policy simulation (“what would have changed the outcome?”) — with strict plausibility/constraints.



## 3. Model‑Specific Approaches

### 3.1 Gradient‑Based Explanations (Saliency, Integrated Gradients, SmoothGrad, Grad‑CAM)
**Saliency.** Uses input gradients to highlight sensitivity of predictions to features ([7]).  
**Integrated Gradients.** Integrates gradients along a baseline‑to‑input path and satisfies completeness ([8]).  
**SmoothGrad.** Averages gradients over noise‑perturbed inputs to reduce visual noise ([9]).  
**Grad‑CAM.** Weights convolutional feature maps by class‑specific gradients to localize influential regions in images ([6]).  
**Caveats.** Saliency methods can fail **sanity checks** if not validated; apply robustness and randomization tests ([26]).
**What it does**: Uses gradients to attribute importance to inputs or activations.

**Real-world deployments**
- Clinical imaging (CheXNet/CheXpert, Stanford): CheXNet outputs heatmaps localizing pneumonia-indicative regions (Grad-CAM-style), widely referenced in clinical AI literature and press; later studies cautioned to validate saliency fidelity before clinical action.  
- Meta’s Captum (production-grade library): Provides Integrated Gradients, DeepLIFT, etc. used across PyTorch models; Meta documents Captum’s role in building responsible AI workflows and ecosystem partnerships.  

Best-fit uses: Vision/NLP model debugging, safety reviews, and developer-facing tools; pair with human evaluation for clinical or high-stakes use.
### 3.2 Attention Mechanisms
Attention distributions can reveal which tokens/regions a model focuses on (e.g., Transformers), aiding transparency and debugging. However, **“Attention is not Explanation”** argues weights may not correlate with importance; later work nuances this view—treat attention as a lens, not causal proof ([27], [10], [11]).
**The debate**
- “Attention is not Explanation”: Attention weights may not uniquely reflect causal importance; alternate weightings can yield the same output.
- Nuanced view: With proper tests (e.g., uniform-attention baselines, adversarial perturbations), attention can be informative but not definitive.
- Empirical takeaway: Attention ≈ weak, sometimes useful signal—not a guaranteed importance measure.

**Practical guidance**
- Treat attention as a lens, not causal proof.
- Useful in research/evaluation (e.g., translation alignment, image captioning).
- For end-users, prefer feature- or example-based explanations unless alignment is the goal.

**Real-world usage patterns**

Primarily behind the scenes for verification and diagnosis (e.g., analyzing heads in large language/vision models); exposed selectively in tools/demos for developer insight.

### 3.3 Decision Trees and Rule‑Based Explanations
**Intrinsic interpretability.** Small trees, rule lists, or risk scores provide human‑readable logic favored in high‑stakes settings when accuracy permits. Post‑hoc **surrogates** (global trees) can approximate black boxes but require fidelity checks. A strong position in the literature encourages using interpretable models directly where feasible ([12], [13], [14], [3]).

**What it does**: Glass-box models (scorecards, trees, GA2M/EBM) provide directly interpretable structure with competitive accuracy.

**Real-world deployments**
- Microsoft Research (healthcare): GA2M/EBM models deployed in hospital risk studies uncovered a spurious rule (asthma falsely appearing protective for pneumonia mortality), preventing unsafe deployment of a black-box and enabling clinician-auditable fixes.
Source: https://www.microsoft.com/en-us/research/wp-content/uploads/2017/06/KDD2015FinalDraftIntelligibleModels4HealthCare_igt143e-caruanaA.pdf#:~:text=then%3A%20that%20having%20asthma%20lowers,Because%20asthma%20is
- FICO (credit): Scorecards remain a regulatory mainstay for transparent lending; FICO publications and research compare scorecards with ML models, emphasizing explainability/operability. Source: https://www.philadelphiafed.org/-/media/frbp/assets/events/2018/consumer-finance/fintech-2018/day-1/session_3_paper_3_fico_paper_gerald_fahner.pdf#:~:text=FICO%C2%AE%20Scores%20are%20based%20on,Predictive%20Performance%20Comparisons

**Best-fit uses**: High-stakes domains needing auditability, stable global logic, and straightforward monitoring.



## 4. Global vs. Local Explanations
- **Global**: how the model behaves **on average** (permutation importance, aggregated SHAP, surrogate trees, partial dependence, EBM).  
- **Local**: why **this** prediction occurred (SHAP/LIME for an instance, counterfactuals, anchors).  
Effective practice combines both views to support developers, decision‑makers, and affected users ([3], [18]).

**Examples**:
- LIME (Local Interpretable Model-Agnostic Explanations): Fits a simple, interpretable "surrogate" model to the predictions of the black-box model in a localized area around the instance of interest.
- SHAP (SHapley Additive exPlanations) values: Use concepts from game theory to assign a "Shapley value" to each feature, indicating its contribution to a specific prediction compared to a baseline value.



## 5. Evaluating Explanation Quality

### 5.1 Technical Metrics
- **Fidelity** (faithfulness to the original model), **stability/robustness** (under perturbations), **completeness** (attribution sums).  
- Toolkits like **Quantus** provide standardized metrics (e.g., infidelity, sensitivity); **TruLens** supports attribution evaluation/tracing for deep nets and LLMs ([19], [20]).  
- **Sanity checks** for saliency (model/label randomization) are recommended ([26]).

**Key references:** [19], [20], [26]

### 5.2 Human‑Centered Evaluation
Guidance from **NIST** emphasizes evaluating **usefulness, transparency, and trust** with human studies (comprehension, task success) aligned to explanation goals ([18]).

**Key references:** [18]



## 6. Practice and Tooling (Selected)
- **What‑If Tool** (PAIR): interactive what‑if analysis and partial dependence for models in notebooks and dashboards ([21]).  
- **InterpretML (EBM)**: glass‑box GAM‑style models that are accurate and globally interpretable for tabular data ([22]).  
- **Captum (PyTorch)**: gradient‑based attribution, IG, DeepLIFT, and more for neural networks ([23]).

**Key references:** [21], [22], [23]



## 7. Comparative Guidance (Technique → When/Why)
- **Permutation importance (global)**: fast, metric‑agnostic ranking for tabular models; evaluate on hold‑out to avoid impurity bias ([4], [25]).  
- **SHAP (local + aggregated global)**: regulator‑friendly attributions with axioms; strong for tree ensembles; not causal by default ([1], [3]).  
- **LIME (local)**: flexible across modalities; validate stability across runs ([2], [26]).  
- **Counterfactuals (local/actionable)**: support user recourse; enforce feasibility constraints ([5]).  
- **Gradients/IG/Grad‑CAM (local, vision/text)**: great for debugging deep nets; use sanity checks and robustness metrics ([6], [7], [8], [26]).  
- **Attention (model‑specific)**: communicative but contested; combine with other attributions for stakeholders ([10], [11]).  
- **Rules/trees & EBM (intrinsic)**: preferred when accuracy permits; otherwise consider a surrogate with fidelity reporting ([12], [22], [3]).

**Key references:** see per‑line citations.



## 8. Stakeholder‑Aligned Communication
- **Developers/Data scientists:** quantitative dashboards (fidelity, stability), failure‑mode surfacing, bias checks ([19], [20]).  
- **Business/Executives/Regulators:** aggregated SHAP summaries, global importance, concise adverse‑action reasons; documentation of methods and monitoring ([1], [3], [18], [22]).  
- **End users:** plain‑language rationales and **counterfactual** recourse; set expectations that explanations reflect the **model’s** reasoning, not ground‑truth causality ([5], [18]).

**Key references:** [1], [3], [5], [18], [22]



## 9. Limitations & Risks
Post‑hoc methods can be **gamed**; attention weights may not be causal; saliency can be unstable; impurity importances can be biased. Mitigate via **multi‑method triangulation**, **sanity/robustness checks**, and alignment to human evaluation ([10], [11], [26], [25], [18]).

**Key references:** [10], [11], [18], [25], [26]


---

## References

[1] Lundberg, S. & Lee, S.-I. (2017). **A Unified Approach to Interpreting Model Predictions**. arXiv:1705.07874.  
[2] Ribeiro, M. T., Singh, S., & Guestrin, C. (2016). **“Why Should I Trust You?”: Explaining the Predictions of Any Classifier**. arXiv:1602.04938.  
[3] Molnar, C. **Interpretable Machine Learning**. https://christophm.github.io/interpretable-ml-book/  
[4] scikit‑learn: **Permutation feature importance**. https://scikit-learn.org/stable/modules/permutation_importance.html  
[5] Wachter, S., Mittelstadt, B., & Russell, C. (2017). **Counterfactual explanations without opening the black box**. arXiv:1711.00399.  
[6] Selvaraju, R. R., et al. (2017). **Grad‑CAM: Visual Explanations from Deep Networks via Gradient-based Localization**. arXiv:1610.02391.  
[7] Simonyan, K., Vedaldi, A., & Zisserman, A. (2013). **Deep Inside Convolutional Networks: Visualising Image Classification Models and Saliency Maps**. arXiv:1312.6034.  
[8] Sundararajan, M., Taly, A., & Yan, Q. (2017). **Axiomatic Attribution for Deep Networks**. arXiv:1703.01365.  
[9] Smilkov, D., et al. (2017). **SmoothGrad**. arXiv:1706.03825.  
[10] Jain, S. & Wallace, B. C. (2019). **Attention is not Explanation**. arXiv:1902.10186.  
[11] Wiegreffe, S. & Pinter, Y. (2019). **Attention is not not Explanation**. arXiv:1908.04626.  
[12] Rudin, C. (2019). **Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead**. *Nature Machine Intelligence*, 1, 206–215.  
[13] Angelino, E., Larus‑Stone, N., Alabi, D., Seltzer, M., & Rudin, C. (2018). **Learning Certifiably Optimal Rule Lists**. arXiv:1704.01701.  
[14] Ustun, B. & Rudin, C. (2016). **Supersparse Linear Integer Models for Optimized Medical Scoring Systems**. arXiv:1611.04261.  
[16] Kim, B., et al. (2016). **Examples are not Enough, Learn to Criticize! (MMD‑critic)**. arXiv:1611.03530.  
[17] Chen, C., et al. (2019). **This Looks Like That: Deep Learning for Interpretable Image Recognition** (ProtoPNet). NeurIPS. arXiv:1806.10574.  
[18] NIST (2020). **Four Principles of Explainable AI** (NISTIR 8312). https://nvlpubs.nist.gov/nistpubs/ir/2020/NIST.IR.8312.pdf  
[19] **Quantus**: https://github.com/understandable-machine-intelligence-lab/Quantus  
[20] **TruLens**: https://www.trulens.org/  
[21] **What‑If Tool**: https://pair-code.github.io/what-if-tool/  
[22] **InterpretML** (EBM): https://interpret.ml/  
[23] **Captum** (PyTorch): https://captum.ai/  
[25] scikit‑learn: **Feature importance pitfalls (impurity bias)**. https://scikit-learn.org/stable/auto_examples/inspection/plot_permutation_importance.html  
[26] Adebayo, J., et al. (2018). **Sanity Checks for Saliency Maps**. NeurIPS. arXiv:1810.03292.  
[27] Vaswani, A., et al. (2017). **Attention Is All You Need**. NeurIPS. arXiv:1706.03762.
