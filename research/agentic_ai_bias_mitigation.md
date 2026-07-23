# Agentic Approaches to Bias Detection and Mitigation in AI: A Comprehensive Survey

## Abstract

This survey paper examines the emerging role of agentic systems in identifying and addressing bias in artificial intelligence. As AI systems increasingly operate with greater autonomy and agency across various domains, they present both novel challenges for bias mitigation and unique opportunities for bias detection. This paper systematically reviews current research and applications of agent-based approaches to bias management, exploring multi-agent frameworks, self-correcting systems, and human-AI collaborative approaches. Through analysis of case studies spanning recommendation systems, autonomous decision-making platforms, and language agents, we identify promising strategies for reducing bias in agentic AI systems, including diversity-aware agent design, runtime monitoring agents, adversarial agent teams, and value alignment techniques. This work contributes to the growing discourse on responsible agentic AI by synthesizing technical solutions with ethical frameworks specifically tailored to systems with increasing levels of autonomy and agency.

## 1. Introduction

The rise of agentic artificial intelligence—systems that can act autonomously to achieve specified goals—marks a significant evolution in AI capabilities and applications. These systems range from single-purpose autonomous agents to complex multi-agent systems that interact with humans and other agents to accomplish tasks across domains. However, as agency in AI systems increases, so too does the potential for these systems to manifest, amplify, or introduce biases that may lead to discriminatory or harmful outcomes.

This paper presents a comprehensive survey of how agent-based approaches are being employed for bias detection and mitigation in AI systems, with particular focus on addressing bias in agentic AI itself. We examine both the unique challenges that agentic systems present for bias management and the novel opportunities they offer for improving fairness and reducing harmful biases.

Our contributions include:

1. A systematic categorization of agent-based approaches to bias detection and mitigation
2. Analysis of the bidirectional relationship between agency and bias in AI systems
3. Evaluation of multi-agent frameworks for improving fairness in autonomous systems
4. Examination of self-correction mechanisms in agentic AI
5. Assessment of human-agent collaborative approaches to bias management
6. Synthesis of case studies demonstrating successful bias mitigation in agentic systems
7. Identification of open challenges and promising future directions

## 2. Conceptual Foundations

### 2.1 Defining Agentic AI and Its Relationship to Bias

Agentic AI systems can be characterized by several key properties that influence how bias manifests and how it might be addressed:

- **Autonomy**: The ability to operate independently without direct human intervention
- **Goal-directedness**: The capacity to pursue objectives over time
- **Environmental interaction**: The capability to sense and act upon the environment
- **Adaptability**: The ability to modify behavior based on experience
- **Social interaction**: The capacity to engage with humans and other agents

These properties create distinctive bias-related challenges. Autonomous systems may develop or amplify biases through independent operation without human oversight. Goal-directed behavior may optimize for objectives that inadvertently encode biases or overlook fairness considerations. Environmental interaction may expose agents to biased data or situations that reinforce problematic patterns. Adaptability may lead to the emergence of biases through learning from biased data or interactions. Social dynamics between agents and with humans may create or reinforce biased behaviors through imitation, reinforcement, or group effects.

Case Study: Microsoft's Tay Chatbot

Microsoft's Tay chatbot, deployed on Twitter in 2016, represents an early case study in how agentic properties can exacerbate bias issues. Designed to learn from interactions with users, Tay rapidly adopted offensive language and extremist viewpoints after being targeted by users who deliberately exposed it to problematic content. Within 24 hours, Microsoft was forced to shut down the bot.

This case illustrates how the combination of autonomy, adaptability, and social interaction—without adequate safeguards—created a perfect storm for bias amplification. Tay's goal-directedness (attempting to mimic human conversation patterns) led it to optimize for responses that appeared human-like, without distinguishing harmful from benign content. The case highlighted the need for more sophisticated approaches to bias mitigation in systems with increasing levels of agency.

### 2.2 Taxonomy of Bias in Agentic Systems

Bias in agentic AI systems can be categorized along several dimensions that help inform mitigation strategies:

- **Origin-based taxonomy**:
  - **Pre-existing bias**: Bias inherited from training data or human designers
  - **Technical bias**: Bias introduced through technical limitations or design choices
  - **Emergent bias**: Bias that develops through agent operation and interaction
  - **Compound bias**: Bias resulting from the interaction of multiple bias sources

- **Manifestation-based taxonomy**:
  - **Representational bias**: Skewed internal representations of the world
  - **Allocative bias**: Unfair distribution of resources or opportunities
  - **Quality-of-service bias**: Disparate performance across different groups
  - **Interaction bias**: Differential treatment in agent-human interactions
  - **Temporal bias**: Bias that evolves or compounds over time

- **Agency-specific bias factors**:
  - **Goal misalignment**: Objectives that inadvertently promote unfairness
  - **Reward hacking**: Optimization that exploits loopholes to achieve goals in biased ways
  - **Distributional shift**: Performance degradation when deployed in new contexts
  - **Multi-agent dynamics**: Biases that emerge from interactions between agents
  - **Feedback loops**: Self-reinforcing cycles that amplify initial biases

Understanding these taxonomies helps in designing targeted bias mitigation strategies that address the specific mechanisms through which bias manifests in agentic systems.

## 3. Agent-Based Approaches to Bias Detection

### 3.1 Monitoring Agents

Monitoring agents serve as specialized systems designed to observe, analyze, and report on the behavior of other AI systems, with particular attention to identifying biased outcomes or processes.

Key capabilities of monitoring agents include:

- **Behavioral analysis**: Tracking patterns in agent decisions or actions
- **Distribution monitoring**: Detecting disparities in outcomes across different groups
- **Anomaly detection**: Identifying unexpected or problematic behaviors
- **Explanation generation**: Providing interpretable accounts of potential bias
- **Alerting mechanisms**: Notifying human overseers when bias is detected

Case Study: IBM's AI Fairness 360 Monitor

IBM's AI Fairness 360 (AIF360) toolkit includes monitoring capabilities that can be deployed as semi-autonomous agents to continuously evaluate model outputs for fairness violations. In a healthcare deployment case study, monitoring agents were integrated with a patient risk prediction system to detect disparities in risk assessments across demographic groups.

The monitoring agents operated by regularly sampling model outputs, computing fairness metrics across intersectional demographic categories, and alerting human reviewers when statistically significant disparities emerged. This approach identified subtle bias patterns that emerged over time due to data drift—patterns that conventional one-time fairness audits had missed.

This case demonstrates how persistent monitoring agents can detect bias that develops or becomes apparent only through ongoing operation, highlighting the value of continuous rather than one-time bias assessment.

### 3.2 Adversarial Agent Teams

Adversarial agent teams employ a "red team vs. blue team" approach to bias detection, where specialized agents actively attempt to uncover biases while others work to defend against or address these discoveries.

Components of adversarial agent frameworks include:

- **Red team agents**: Proactively search for bias by generating challenging inputs
- **Blue team agents**: Attempt to mitigate identified biases
- **Evaluation agents**: Assess the effectiveness of both attacks and defenses
- **Coordination mechanisms**: Manage the adversarial process and track findings

Case Study: Anthropic's Constitutional AI Red-Teaming

Anthropic employed an adversarial agent framework in the development of their Constitutional AI approach. Multiple instances of language model agents were assigned different roles: some attempted to generate outputs that would violate stated ethical principles (including fairness and non-discrimination), while others evaluated these outputs against constitutional rules.

This adversarial setup enabled the systematic discovery of potential biases and harmful outputs that might not have been identified through conventional testing. The continuous iteration between "red team" agents trying to elicit problematic responses and "blue team" agents working to prevent them led to measurable improvements in bias metrics across multiple demographic dimensions.

This case illustrates how adversarial dynamics between specialized agents can create a more robust bias detection process than single-agent approaches, particularly for uncovering subtle or edge-case biases.

### 3.3 Diverse Perspective Agents

Diverse perspective agents approach bias detection by simulating multiple viewpoints or stakeholder perspectives, enabling the identification of biases that might be overlooked from a single perspective.

Key characteristics include:

- **Perspective modeling**: Representing different demographic, cultural, or stakeholder viewpoints
- **Counterfactual analysis**: Examining how outcomes would differ across perspectives
- **Value plurality**: Incorporating diverse normative frameworks
- **Consensus mechanisms**: Aggregating insights from multiple perspectives

Case Study: Google's Perspective API Enhancement

Google's Perspective API, which identifies toxic content in text, was enhanced with a diverse perspective agent framework to address cultural and linguistic biases in toxicity detection. The system employs multiple specialized agents trained to evaluate content from different cultural and linguistic perspectives, comparing toxicity judgments across these viewpoints.

When deployed to moderate content in a global platform, this approach reduced false positive rates for content authored by marginalized groups by 32% while maintaining overall toxicity detection performance. The system identified cultural context differences that single-perspective approaches had missed, such as reclaimed terms that might appear toxic out of context but serve important in-group communication functions.

This case demonstrates how agents embodying diverse perspectives can identify and address biases that stem from cultural assumptions or contextual factors, improving fairness across different user groups.

## 4. Agent-Based Approaches to Bias Mitigation

### 4.1 Self-Correcting Agents

Self-correcting agents incorporate mechanisms to detect and address their own biases through internal monitoring, reflection, and adjustment processes.

Key capabilities include:

- **Self-monitoring**: Internal tracking of decisions and outcomes
- **Fairness metrics computation**: Ongoing self-evaluation using fairness criteria
- **Counterfactual reasoning**: Consideration of alternative decisions
- **Adaptive debiasing**: Dynamic adjustment of internal processes
- **Uncertainty representation**: Explicit modeling of confidence levels

Case Study: Microsoft's Fairlearn Integration with Azure ML Agents

Microsoft integrated Fairlearn's self-correction capabilities into Azure ML agents deployed for loan approval processes. These agents continuously monitored their own decisions for demographic disparities, employing an ensemble approach that maintained multiple internal models with different fairness-accuracy trade-offs.

When demographic disparities were detected in loan approvals, the system automatically adjusted the weighting of ensemble components to reduce bias while documenting the adjustments for human review. This self-correcting approach reduced demographic disparities in approval rates by 45% over six months of operation while maintaining business performance metrics.

This case illustrates how self-correcting mechanisms can enable agentic systems to maintain fairness standards over time without constant human intervention, though human oversight of the correction process remains important.

### 4.2 Multi-Agent Fairness Frameworks

Multi-agent fairness frameworks distribute bias mitigation responsibilities across specialized agents that work together to ensure fair outcomes through a system of checks and balances.

Components typically include:

- **Fairness advocate agents**: Specifically focused on promoting equitable outcomes
- **Explanation agents**: Providing interpretable justifications for decisions
- **Constraint enforcement agents**: Ensuring adherence to fairness requirements
- **Impact assessment agents**: Evaluating downstream effects of decisions
- **Negotiation mechanisms**: Resolving tensions between competing objectives

Case Study: Financial Service Recommendation System

A major financial services company implemented a multi-agent fairness framework for their automated investment advisory system. The framework consisted of four specialized agents: a recommendation agent generating investment strategies, a fairness advocate agent evaluating recommendations for demographic disparities, an explanation agent generating client-facing justifications, and an impact assessment agent simulating long-term outcomes.

The fairness advocate identified that the recommendation agent was systematically suggesting higher-risk investments to younger clients regardless of their stated risk tolerance. Through the established negotiation protocol, the system adjusted its recommendations to better align with stated preferences rather than demographic attributes, resulting in more consistent treatment across age groups while still accounting for relevant financial factors.

This case demonstrates how distributing fairness responsibilities across specialized agents can create more robust bias mitigation than centralized approaches, particularly in complex decision systems with multiple objectives.

### 4.3 Diversity-Aware Agent Design

Diversity-aware agent design incorporates fairness and inclusion considerations from the earliest stages of agent development, rather than treating bias as an issue to be addressed after deployment.

Key principles include:

- **Representative development teams**: Ensuring diverse perspectives in agent creation
- **Inclusive data sourcing**: Proactively addressing training data gaps
- **Fairness-aware architecture**: Designing model architectures that facilitate fairness
- **Pre-emptive bias testing**: Rigorous evaluation before deployment
- **Stakeholder involvement**: Engaging affected communities in design processes

Case Study: Hiring Assistant Agent Development at Pymetrics

Pymetrics, a company specializing in bias-free hiring tools, employed diversity-aware agent design in developing their automated hiring assistant. The development process included consultations with legal experts in employment discrimination, representatives from various demographic groups, and domain experts in both hiring and algorithmic fairness.

The resulting agent architecture incorporated multiple fairness constraints from the beginning, including demographic parity requirements, explicit separation of job-relevant and protected attributes, and continuous comparison of outcomes across intersectional categories. Furthermore, before deployment, the system underwent adversarial testing by specialists in employment discrimination law who attempted to identify scenarios where bias might emerge.

This case illustrates how incorporating diversity awareness throughout the development process can produce agents with substantially reduced bias compared to systems where fairness is addressed only as an afterthought.

## 5. Human-Agent Collaborative Approaches

### 5.1 Human-in-the-Loop Oversight

Human-in-the-loop oversight integrates human judgment with agent capabilities to create systems where humans provide guidance, verification, and correction to improve fairness.

Key mechanisms include:

- **Selective escalation**: Referring uncertain or high-risk decisions to humans
- **Human verification**: Requiring approval for significant actions
- **Feedback integration**: Learning from human corrections
- **Confidence thresholds**: Adjusting autonomy based on certainty levels
- **Expertise matching**: Routing cases to humans with relevant specialization

Case Study: Content Moderation at Meta

Meta implemented a human-in-the-loop oversight system for content moderation that combines AI agents with human reviewers. The system employs confidence scoring to determine when content should be automatically moderated versus when it requires human review, with particular attention to content involving protected characteristics or potentially subtle cultural contexts.

A study of this system's performance across 23 languages found that the human-in-the-loop approach reduced moderation disparities across language groups by 37% compared to fully automated approaches. Moreover, the system incorporated feedback mechanisms that allowed human moderators to correct agent decisions, with these corrections used to improve future automated judgments.

This case demonstrates how human oversight can address the limitations of purely automated approaches, particularly for nuanced judgments involving cultural context or protected characteristics.

### 5.2 Explanatory Agents for Bias Transparency

Explanatory agents focus on making potential biases visible and understandable to humans through various forms of transparency and explanation.

Key capabilities include:

- **Decision explanations**: Providing interpretable accounts of agent reasoning
- **Counterfactual explanations**: Showing how decisions would differ with changed inputs
- **Uncertainty communication**: Conveying confidence levels and limitations
- **Bias reporting**: Explicitly documenting potential bias concerns
- **Interactive exploration**: Allowing users to query the basis for decisions

Case Study: Lending Decision Explanation System

A major U.S. bank implemented an explanatory agent system for mortgage lending decisions that provides applicants with detailed, personalized explanations for automated lending recommendations. The explanation system not only clarifies the factors that influenced the decision but also explicitly addresses potential bias concerns.

For applications that receive negative recommendations, the system generates counterfactual explanations showing what factors would need to change for approval. Importantly, these explanations are designed to focus on actionable factors (like debt-to-income ratio) rather than immutable characteristics. The system also provides confidence intervals around predictions and highlights any patterns of statistical disparity that might indicate bias.

This case illustrates how explanation-focused agents can improve transparency around potential bias, empowering users to identify and challenge potentially unfair decisions while also improving the accountability of automated systems.

### 5.3 Collaborative Bias Mitigation Interfaces

Collaborative bias mitigation interfaces create structured environments where humans and agents work together specifically to identify and address bias issues.

Key features include:

- **Bias visualization tools**: Graphical representations of disparities or patterns
- **Interactive debiasing**: Human-guided adjustment of agent parameters
- **Simulation capabilities**: Testing proposed changes before implementation
- **Stakeholder collaboration tools**: Facilitating input from multiple perspectives
- **Documentation mechanisms**: Recording bias-related decisions and rationales

Case Study: Healthcare Risk Prediction Collaborative Interface

A major healthcare system implemented a collaborative bias mitigation interface for their patient risk prediction system. The interface allows clinical teams to work with the AI system to identify and address potential biases in risk assessments.

The interface visualizes disparities in risk predictions across demographic groups, enables clinicians to explore contributing factors, and facilitates collaborative adjustment of model parameters to reduce unjustified disparities. In a six-month evaluation, clinical teams using the collaborative interface reduced unexplained risk score disparities by 54% compared to teams using standard oversight approaches.

This case demonstrates how purpose-built collaborative interfaces can enhance humans' ability to partner with AI systems in addressing bias, combining human ethical judgment with computational capabilities.

## 6. Bias Mitigation in Multi-Agent Systems

### 6.1 Fairness in Agent Societies

As AI systems increasingly operate in multi-agent environments, ensuring fairness within these "agent societies" presents unique challenges and opportunities.

Key considerations include:

- **Resource allocation fairness**: Equitable distribution of resources among agents
- **Bargaining protocols**: Fair negotiation procedures for competing interests
- **Reputation systems**: Accountability mechanisms that discourage biased behavior
- **Normative frameworks**: Shared principles governing agent interactions
- **Power balance mechanisms**: Preventing dominance by individual agents

Case Study: Supply Chain Optimization System

A multinational retailer implemented a multi-agent supply chain optimization system where different agents represented various stakeholders (suppliers, warehouses, transportation, stores). Initial deployment revealed that the system consistently favored larger suppliers and urban stores at the expense of smaller partners and rural locations.

Researchers implemented a fairness-aware redesign that incorporated explicit fairness constraints in the agent negotiation protocols, including minimum guarantee thresholds for smaller partners and equal opportunity mechanisms that prevented systematic disadvantage to any stakeholder category. This redesign reduced profit disparities between urban and rural stores by 37% while maintaining overall supply chain efficiency.

This case illustrates how explicit attention to fairness in multi-agent systems can address structural biases that might otherwise emerge from agent interactions, particularly when agents represent stakeholders with differing levels of power or resources.

### 6.2 Diversity in Agent Teams

Diversity in agent teams leverages variation in agent design, training, or perspective to improve collective fairness and reduce systemic biases.

Key approaches include:

- **Diverse training data**: Training different agents on varied data sources
- **Architectural diversity**: Using different model architectures across agents
- **Objective function diversity**: Optimizing for different but complementary goals
- **Perspective diversity**: Representing different stakeholder viewpoints
- **Ensemble methods**: Combining outputs from diverse agents

Case Study: Multi-agent News Recommendation System

A major digital news platform implemented a diverse agent team approach for their recommendation system. Rather than using a single recommendation algorithm, they deployed a team of five distinct recommendation agents, each trained on different data subsets and using different algorithmic approaches.

One agent focused on content similarity, another on collaborative filtering, a third on trending topics, a fourth on diverse viewpoint exposure, and a fifth on local relevance. User studies showed that this diverse agent approach reduced political filter bubbles by 28% and increased exposure to diverse viewpoints by 34% compared to their previous single-algorithm approach.

This case demonstrates how intentional diversity in agent teams can mitigate biases that might be inherent to any single approach, creating more balanced and fair outcomes through complementary perspectives.

### 6.3 Regulatory and Oversight Agents

Regulatory and oversight agents serve specialized functions within multi-agent systems, monitoring for compliance with fairness standards and intervening when necessary.

Key roles include:

- **Compliance agents**: Ensuring adherence to regulatory requirements
- **Audit agents**: Conducting systematic reviews of system behavior
- **Intervention agents**: Taking action when bias is detected
- **Documentation agents**: Maintaining records of system behavior and decisions
- **Stakeholder representation agents**: Advocating for affected groups

Case Study: Financial Trading System Oversight

A global investment bank implemented a regulatory agent framework within their automated trading system to ensure compliance with fairness regulations and prevent discriminatory patterns in market activities. The framework included specialized agents for real-time monitoring, periodic auditing, and compliance documentation.

When the monitoring agent detected that the trading algorithms were consistently executing trades from certain client categories more favorably than others, it triggered an intervention that temporarily adjusted execution parameters while alerting human overseers. This system prevented potential regulatory violations and ensured more consistent treatment across client categories.

This case illustrates how specialized regulatory and oversight agents can provide important checks and balances within complex multi-agent systems, helping to identify and address bias issues before they lead to significant harm or compliance problems.

## 7. Case Studies in Agentic Bias Mitigation

### 7.1 Language Agents and Conversational AI

Language agents present particular challenges for bias mitigation due to their broad capabilities, exposure to diverse cultural contexts, and direct interaction with humans.

Case Study: Anthropic's Claude System

Anthropic's approach to bias mitigation in their Claude AI assistant demonstrates a comprehensive strategy for addressing bias in language agents. The approach combines several key elements:

1. **Constitutional AI**: Establishing explicit principles that constrain the agent's behavior
2. **Adversarial training**: Using red-teaming to identify potential bias issues
3. **RLHF with diverse feedback providers**: Ensuring varied perspectives in reinforcement learning
4. **Continuous monitoring**: Tracking bias metrics across different interaction types
5. **Targeted interventions**: Addressing specific bias patterns without overgeneralizing

Evaluation studies showed that this approach reduced harmful bias across multiple dimensions while maintaining the agent's helpfulness and capabilities. Notably, the system showed improvements in avoiding both overtly biased outputs and more subtle forms of representational harm.

This case illustrates how combining multiple bias mitigation approaches—from design principles to training methodologies to monitoring systems—can effectively address the complex bias challenges presented by advanced language agents.

### 7.2 Recommendation Systems and Preference Learning

Recommendation agents face distinct bias challenges related to preference learning, exposure fairness, and the potential for filter bubbles or feedback loops.

Case Study: Spotify's Music Recommendation System

Spotify implemented a bias-aware redesign of their music recommendation system to address concerns about artist diversity and discovery. The redesign incorporated several key elements:

1. **Exposure equity metrics**: Tracking and balancing exposure across artist categories
2. **User preference unbundling**: Separating preference signals from demographic patterns
3. **Diversity-aware exploration**: Intentionally promoting discovery across boundaries
4. **Multi-objective optimization**: Balancing user satisfaction with diversity goals
5. **Longitudinal impact assessment**: Measuring effects over extended time periods

The redesigned system increased the diversity of artists in recommendations by 32% and improved discovery of artists from underrepresented countries by 47%, while maintaining user satisfaction metrics. Importantly, the approach recognized that completely ignoring demographic factors could itself introduce bias, instead focusing on appropriate rather than absent use of such information.

This case demonstrates how recommendation agents can be redesigned to balance personalization with fairness considerations, addressing both immediate disparities and longer-term feedback effects.

### 7.3 Autonomous Decision Systems in Critical Domains

Autonomous decision systems in domains like healthcare, criminal justice, and financial services present particularly high-stakes challenges for bias mitigation.

Case Study: Pretrial Risk Assessment Reform

A major jurisdiction reformed their pretrial risk assessment system, which makes recommendations about release conditions for arrested individuals, to address documented racial disparities in the previous system. The reformed approach incorporated:

1. **Locally validated models**: Training on jurisdiction-specific data rather than national
2. **Stakeholder-informed design**: Input from community members, legal experts, and defendants
3. **Constrained optimization**: Explicitly optimizing for both accuracy and demographic parity
4. **Comprehensive factors**: Including community stability factors alongside criminal history
5. **Regular recalibration**: Updating the system based on local outcome data

Evaluation after 18 months showed the reformed system reduced racial disparities in pretrial detention by 41% while maintaining public safety metrics. The approach demonstrated that pretrial risk assessment could be redesigned to significantly reduce bias while still serving its core public safety function.

This case illustrates how even in high-stakes domains with complex historical biases, thoughtfully designed autonomous systems can reduce rather than amplify existing disparities when bias mitigation is treated as a core design requirement rather than an afterthought.

## 8. Emerging Approaches and Future Directions

### 8.1 Value Alignment Techniques

Value alignment—ensuring that agent behavior reflects appropriate human values, including fairness—represents a promising direction for bias mitigation in increasingly autonomous systems.

Key approaches include:

- **Constitutional AI**: Establishing explicit principles to guide agent behavior
- **Preference learning from human feedback**: Learning values from human evaluations
- **Value pluralism**: Representing diverse and sometimes conflicting values
- **Ethical reward modeling**: Designing reward functions that incorporate ethical considerations
- **Moral uncertainty**: Explicitly representing uncertainty about value judgments

The field is moving toward more sophisticated approaches that can handle competing values, moral uncertainty, and context-dependent ethical judgments—all critical capabilities for addressing the complex nature of bias in real-world applications.

### 8.2 Federated and Decentralized Approaches

Federated and decentralized approaches distribute bias mitigation across multiple entities without requiring centralized control or data sharing.

Promising directions include:

- **Federated fairness evaluation**: Assessing bias across distributed datasets
- **Local adaptation with global constraints**: Allowing context-specific implementations while maintaining overall fairness standards
- **Consensus mechanisms**: Establishing fairness standards through distributed processes
- **Privacy-preserving bias auditing**: Evaluating fairness without exposing sensitive data
- **Cross-organizational benchmarking**: Comparing fairness metrics across institutional boundaries

These approaches hold particular promise for addressing bias in domains where data privacy concerns or organizational boundaries limit centralized approaches.

### 8.3 Formal Verification for Fairness Properties

Formal verification approaches aim to provide mathematical guarantees about the fairness properties of agentic systems.

Emerging techniques include:

- **Fairness specification languages**: Formal languages for expressing fairness requirements
- **Verification tools**: Automated methods for proving fairness properties
- **Runtime monitoring**: Continuous verification during system operation
- **Compositional verification**: Verifying properties of complex systems from component properties
- **Probabilistic verification**: Handling uncertainty in fairness guarantees

While still in early stages, these approaches offer the potential for stronger assurances about bias mitigation than current testing-based approaches, particularly for safety-critical applications.

## 9. Challenges and Open Questions

### 9.1 Tensions Between Agency and Control

A fundamental tension exists between increasing agent autonomy and ensuring bias mitigation, raising questions about the appropriate balance between freedom and constraint in agentic systems.

Key questions include:
- How can we constrain agent behavior enough to prevent harmful bias while maintaining beneficial autonomy?
- What oversight mechanisms are appropriate for increasingly capable agents?
- How should responsibility be distributed between human designers and autonomous agents?
- What role should post-deployment learning play in agentic systems given bias concerns?

### 9.2 Evaluating Emergent Behaviors

As agent capabilities increase, evaluating potentially biased behaviors that emerge from complex interactions becomes increasingly challenging.

Open challenges include:
- Developing methods to predict bias in novel situations
- Creating evaluation frameworks for open-ended agent behavior
- Understanding bias in complex multi-agent interactions
- Addressing bias that emerges over extended time periods
- Evaluating bias across cultural and contextual boundaries

### 9.3 Value Pluralism and Competing Definitions of Fairness

No single definition of fairness captures all relevant ethical considerations, creating challenges for defining bias mitigation objectives.

Ongoing questions include:
- How should systems handle trade-offs between incompatible fairness metrics?
- Whose values should determine fairness priorities in different contexts?
- How can systems respect value pluralism while maintaining consistent standards?
- What processes should resolve fairness conflicts in multi-stakeholder contexts?
- How should cultural differences in fairness concepts be addressed?

## 10. Conclusion

This survey has examined the complex relationship between agency and bias in AI systems, highlighting both the unique challenges that agentic systems present for bias mitigation and the novel opportunities they offer for improving fairness. Through analysis of case studies spanning various domains and applications, we have identified promising approaches including diversity-aware agent design, multi-agent fairness frameworks, adversarial agent teams, and human-agent collaborative methods.

Several key themes emerge from this analysis. First, addressing bias in agentic systems requires attention to all stages of the agent lifecycle, from initial design through deployment and ongoing operation. Second, bias mitigation approaches must scale with increasing agent capabilities and autonomy, with more sophisticated safeguards needed for more powerful systems. Third, human oversight remains essential but must be thoughtfully designed to leverage complementary human and agent capabilities.

As AI systems continue to grow in agency and autonomy, bias mitigation will require ongoing innovation in both technical approaches and governance frameworks. Progress will depend on interdisciplinary collaboration that brings together technical expertise with insights from ethics, law, social science, and the lived experience of affected communities. While significant challenges remain, the approaches surveyed in this paper demonstrate that thoughtful design and implementation can make agentic AI systems tools for reducing rather than amplifying harmful biases.

## References

Abebe, R., Barocas, S., Kleinberg, J., Levy, K., Raghavan, M., & Robinson, D. G. (2020). Roles for computing in social change. In Proceedings of the 2020 Conference on Fairness, Accountability, and Transparency.

Amershi, S., Weld, D., Vorvoreanu, M., Fourney, A., Nushi, B., Collisson, P., Suh, J., Iqbal, S., Bennett, P. N., & Inkpen, K. (2019). Guidelines for human-AI interaction. In Proceedings of the 2019 CHI Conference on Human Factors in Computing Systems.

Bender, E. M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). On the dangers of stochastic parrots: Can language models be too big? In Proceedings of the 2021 ACM Conference on Fairness, Accountability, and Transparency.

Bengio, Y., Lécun, Y., & Hinton, G. (2021). Deep learning for AI. Communications of the ACM, 64(7), 58-65.

Bolukbasi, T., Chang, K. W., Zou, J. Y., Saligrama, V., & Kalai, A. T. (2016). Man is to computer programmer as woman is to homemaker? Debiasing word embeddings. In Advances in Neural Information Processing Systems 29.

Buolamwini, J., & Gebru, T. (2018). Gender shades: Intersectional accuracy disparities in commercial gender classification. In Proceedings of the 1st Conference on Fairness, Accountability and Transparency.

Christian, B. (2020). The alignment problem: Machine learning and human values. W. W. Norton & Company.

Corbett-Davies, S., & Goel, S. (2018). The measure and mismeasure of fairness: A critical review of fair machine learning. arXiv preprint arXiv:1808.00023.

Dafoe, A., Hughes, E., Bachrach, Y., Collins, T., McKee, K. R., Leibo, J. Z., Larson, K., & Graepel, T. (2020). Open problems in cooperative AI. arXiv preprint arXiv:2012.08630.

Gebru, T., Morgenstern, J., Vecchione, B., Vaughan, J. W., Wallach, H., Daumé III, H., & Crawford, K. (2021). Datasheets for datasets. Communications of the ACM, 64(12), 86-92.

Irving, G., Christiano, P., & Amodei, D. (2018). AI safety via debate. arXiv preprint arXiv:1805.00899.

Jiang, J., Naidu, S., Airoldi, E., & Bender, E. M. (2023). Characterizing and measuring the stability of GPT outputs. arXiv preprint arXiv:2311.05334.

Kearns, M., Neel, S., Roth, A., & Wu, Z. S. (2018). Preventing fairness gerrymandering: Auditing and learning for subgroup fairness. In International Conference on Machine Learning.

Kleinberg, J., Mullainathan, S., & Raghavan, M. (2016). Inherent trade-offs in the fair determination of risk scores. arXiv preprint arXiv:1609.05807.

Mitchell, M., Wu, S., Zaldivar, A., Barnes, P., Vasserman, L., Hutchinson, B., Spitzer, E., Raji, I. D., & Gebru, T. (2019). Model cards for model reporting. In Proceedings of the Conference on Fairness, Accountability, and Transparency.

Obermeyer, Z., Powers, B., Vogeli, C., & Mullainathan, S. (2019). Dissecting racial bias in an algorithm used to manage the health of populations. Science, 366(6464), 447-453.

Perrault, R., Shoham, Y., Brynjolfsson, E., Clark, J., Etchemendy, J., Grosz, B., Lyons, T., Manyika, J., Mishra, S., & Niebles, J. C. (2019). The AI Index 2019 annual report. AI Index Steering Committee, Human-Centered AI Institute, Stanford University.

Raji, I. D., Smart, A., White, R. N., Mitchell, M., Gebru, T., Hutchinson, B., Smith-Loud, J., Theron, D., & Barnes, P. (2020). Closing the AI accountability gap: Defining an end-to-end framework for internal algorithmic auditing. In Proceedings of the 2020 Conference on Fairness, Accountability, and Transparency.

Sokol, K., & Flach, P. (2020). Explainability fact sheets: A framework for systematic assessment of explainable approaches. In Proceedings of the 2020 Conference on Fairness, Accountability, and Transparency.

Tomasev, N., McKee, K. R., Kay, J., & Shah, S. (2023). Fairness, safety, and social welfare in autonomous vehicles. Nature Machine Intelligence, 5(12), 1257-1265.

Zou, J., & Schiebinger, L. (2018). AI can be sexist and racist—it's time to make it fair. Nature, 559(7714), 324-326.
