[FIGURE]

Contents lists available at ScienceDirect

## Data &amp; Knowledge Engineering

journal homepage: www.elsevier.com/locate/datak

## CriMOnto: A generalized domain-specific ontology for modeling procedural norms of the Lebanese criminal law

Mirna El Ghosh a , ∗ , Hala Naja b , Habib Abdulrab a , Mohamad Khalil c

- a LITIS, INSA Rouen, Normandie Université, Rouen, 76000, France
- b Computer Science Department, Faculty of Sciences, Tripoli, Lebanon
- c CRSI Research Center, Faculty of Engineering, Tripoli, Lebanon

## A R T I C L E I N F O

Keywords: AI &amp; Law Criminal law Procedural norms Generalized ontology UFO UFO-L Ontology-Driven Conceptual Modeling Ontology Patterns

Formal rules

## 1. Introduction

Criminal law consists of '' prohibitions of antisocial behavior backed by serious sanctions '' [1]. It regulates offenses and offenders and establishes legal penalties and corrective measures. Besides, it considers the circumstances of exemption from the penalty and the impediments of prosecution. Seven principles are necessarily present in criminal law, including legality, mens rea (mental element), act, and their concurrence, causation, harm, and punishment [2]. Modeling criminal law is recently gaining much attention in the ontology engineering community where different ontologies have been developed (e.g., CROL [3], LATO [4,5], Ontology of Crimes of Omission [6]). However, this trend has neglected the explicit representation of procedural knowledge. Procedural norms are defined as ''instrumental norms addressed to agents playing a role in the normative system, for example, to motivate these role-playing agents to recognize violations or to apply sanctions'' [7]. Examples of procedural norms are the regulative norms that specify the behavior of a system using obligations, prohibitions, and permissions [7] (e.g., '' Art.193 - If the Judge considers the motive honorable, he shall impose the following penalties: Life imprisonment instead of the death penalty [...]'', from the Lebanese Criminal Code). For Bench-Capon [8], ''representing procedural law is considered challenging because of the difficulty of finding a language to express knowledge in a declarative way''. Thereby, there is a need for a modeling language and approach to (1) permit explicit representation of the deontic characterization of rules in the context of criminal punishments, liabilities, and responsibilities, (2) distinguish the legal interactions among the legal agents regarding these characterizations, and (3) describe the legal effects whenever specified

∗ Corresponding author. E-mail address: mirna.el-ghosh@inserm.fr (M. El Ghosh).

## A B S T R A C T

Criminal (or penal) law regulates offenses, offenders, and legal punishments. Modeling criminal law is gaining much attention in the ontology engineering community. However, a significant aspect is neglected: the explicit representation of procedural knowledge. Procedural norms, such as regulative norms, are addressed to agents in the normative system. They govern the different interactions among these agents. In this study, we propose a formal and faithful representation of the procedural aspect of legal norms in the context of the Lebanese Criminal Code. A modular domain-specific ontology named CriMOnto is developed for this purpose. CriMOnto is grounded in the Unified Foundational Ontology (UFO) and the legal core ontology UFO-L by applying the Ontology-Driven Conceptual Modeling (ODCM) process. Conceptual Ontology Patterns (COPs) are reused from UFO and UFO-L to build the hierarchical and procedural content of the ontology. CriMOnto is validated as a formal ontology and evaluated using a dual evaluation approach. The potential use of CriMOnto for lightweight rule-based decision support is discussed in this study.

[FIGURE]

[FIGURE]

legally defined conditions are fulfilled. Also, considering the Isomorphism principle, essential to creating a well-defined correspondence between the norms in the explicit formal model and the norms in the original legal sources [8], is required.

Nevertheless, the complexity of legal knowledge, closely related to the use of language [9], is challenging for ontology engineers. Legal rules and standards are written, for the most part, in an ordinary language containing ambiguities and inadequacies [10]. Many legal concepts (e.g., intent, motive, consent, property, power, right, liberty, etc.) are incompletely defined [11]. The ambiguity of terms reflects corresponding paucity and confusion regarding actual legal conceptions [12]. Additonally, legal ontologies must cover a wide range of common-sense concepts that are part of physical, abstract, mental, and social worlds [13,14]. Besides social activities, legal domains share complex and varied notions of norm and responsibility, representing the legal core notions [14]. Legal core notions include the norm, contract, agent, role, normative position (e.g., duties, rights), responsibility, and sanction. In this article, we address these challenges through the following research questions focused on the criminal law:

1. How faithfully represent the essentials of criminal law, including the legal interactions among the legal agents and the associated legal effects achieved based on fulfilling legally defined conditions and circumstances?
2. How explicitly represent the deontic characterizations of procedural norms in the context of criminal punishments, liabilities, and responsibilities?
3. How do we benefit from the explicit representation of legal norms to faithfully formalize legal norms with a clear correspondence with the source norms?

These questions are considered in developing CriMOnto (Criminal Modular Ontology), a well-founded domain-specific ontology for a formal and faithful representation of the essentials of the Lebanese Criminal Code. 1 CriMOnto will be employed for a lightweight rule-based decision-making task. It is defined as a generalized ontology by referring to Mommers definition [15]: ''generalized conceptual models of specific parts of the legal domain'' - in the sense that they cover the legal knowledge that can be represented . CriMOnto supports the explicit representation of procedural norms by applying a pattern-based approach based on SABiO [16] and composed of:

1. Ontology-Driven Conceptual Modeling (ODCM) performed based on the Unified Foundational Ontology (UFO) [17-19], a foundational ontology employing philosophical theories. The conceptual model is developed using the Ontology-Driven Conceptual Modeling Language OntoUML [17,20], which is grounded on UFO and permits the analysis of common-sense and legal core concepts using UFO primitives.
2. Ontology layering and modularization to simplify the building process.
3. Reuse of Conceptual Ontology Patterns (COPs) from UFO and the legal core ontology UFO-L [21].

Furthermore, CriMOnto's conceptual model is transformed into a formal ontology that can be represented using a computational language such as OWL. Finally, we evaluate CriMOnto using a dual evaluation approach and discuss its potential use for lightweight rule-based decision support applications. The article is organized as follows. Section 2 outlines the study's background. The ontologybuilding approach is presented in Section 3. Section 4 discusses the building process of CriMOnto. The validation and evaluation of CriMOnto are introduced in Section 5. The related work is outlined in Section 7. Finally, Section 8 discusses and concludes the study.

## 2. Background: UFO and UFO-L

UFO. [17-19] is a foundational ontology that employs formal ontology, cognitive psychology, linguistics, and philosophical logic results. UFO distinguishes fundamentally between Individuals and Universals . In UFO, two main kinds of Individuals are distinguished: Endurants and Perdurants . Endurants are wholly present whenever they are present, i.e., they do not have temporal parts [22]. They can be further specialized into Substantials (Objects) and Moments [23,24]. Substantials are existentially-independent Endurants (e.g., a knife, a person). Moments, in contrast, are individuals that can only exist by inhering in other individuals [23,24]. Two main types of Moments are distinguished in UFO: Intrinsic Moments and Relators . Intrinsic moments are moments that inhere in one individual. An example of an intrinsic moment is a Mode (e.g., intention, motive). Relators are moments that depend on two or more Endurants (e.g., a punishment). Perdurants (Events) are individuals composed of temporal parts and are existentially dependent on Endurants [25]. Examples of Perdurants are a crime, a war, etc. Thereby, UFO is composed of three main layers: UFO-A [26] (ontology of endurants), UFO-B [25] (ontology of events), and UFO-C [26] (ontology of social entities). UFO has been employed in the design of the ontologically well-founded conceptual modeling language OntoUML [17]. OntoUML is proposed based on the need for an ontology-based language that would provide the necessary semantics to construct conceptual models using concepts faithful to reality [27]. OntoUML uses the ontological constraints of UFO as modeling primitives and is specified above the UML2.0 meta-model [17]. Figs. 1, 2, and 3 depict parts of UFO (see Table 1 for definitions).

UFO-L. [21] is a legal core ontology that uses the domain-independent concepts, relations, and properties existing in UFO to represent essential concepts of law based on Alexy's theory of fundamental rights [28]. UFO-L defines a variety of basic legal core concepts, such as legal agents and objects (Fig. 4), legal relators (Fig. 5) and legal moments (Fig. 6). Legal roles such as Right Holder , Duty Holder , and Power Holder are assigned to agents and played within the scope of legal relations. Legal relations are represented based on Alexy's theory and reified using legal relators, which are relational entities existentially dependent on some individuals playing legal roles [29-33]. Examples of legal relators are Disability-Immunity Relator and Power-Subjection Relator (Fig. 8). Every legal relator is grounded on a Legally Defined Event and defined by a Legal Normative Description . Moreover, UFO-L defines various legal moments (e.g., Right , Duty , Legal Power , Immunity , etc.) which are existentially dependent on Individuals (see Table 2 for terms definitions).

[1 https://www.legal-tools.org/doc/d0f1c2/pdf/.](https://www.legal-tools.org/doc/d0f1c2/pdf/)

[FIGURE]

Fig. 1. Excerpt of UFO around the concept Substance (from [26]).

Fig. 2. Excerpt of UFO around the concept Participation (from [26]).

[FIGURE]

Fig. 3. Excerpt of UFO around the concept Intrinsic\_Moment (from [26]).

[FIGURE]

[FIGURE]

Fig. 4. Excerpt of UFO-L around the concept Legal\_Substance (from [21]).

Fig. 5. Excerpt of UFO-L around the concept Legal\_Relator (from [21]).

[FIGURE]

Fig. 6. Excerpt of UFO-L around the concept Legal\_Moment (from [21]).

[FIGURE]

In UFO-L, various modeling patterns are defined [32,33], such as power-subjection [32] (Fig. 7) and disability-immunity (Fig. 8). In these patterns, legal relators, composed of two correlated legal positions (e.g., power, subjection, right, duty, etc.), mediate two disjoint legal roles. Each legal position (or moment) is inherited in a legal role and externally dependent on the disjoint legal role. A material relation is derived from the structure of the legal relators and the mediation relations (see Table 2 for terms definitions).

## 3. Methodology

To build CriMOnto, we relied on the approach SABiO [16]. We considered a pattern-based approach composed of five main phases. Following SABiO, we differ between reference and operational ontologies. While reference ontologies are defined as conceptual models developed to make the best possible description of the domain [34], operational ontologies represent the machine-readable artifacts of these models [16].

Fig. 7. Power\_Subjection\_Relator pattern (from [21]).

[FIGURE]

Fig. 8. Disability\_Immunity\_Relator pattern (from [21]).

[FIGURE]

Ontology specification. This phase specifies the scope and purpose of the intended ontology. Concerning the scope, CriMOnto aims to capture the essentials of criminal law in the context of the Lebanese Criminal Code. The Criminal Code enacted in 1943 (DecreeLaw 340) comprises 772 Articles organized in 8 Chapters. This study concerns mainly the following Chapters: Offenses , Criminal Convictions , Responsibility , and Felonies and misdemeanors against persons . We give an overview of the chapters in what follows:

- Offenses : (Fig. 9) defines the offenses and their classification into felonies , misdemeanours , and contraventions (Art.179). Each offense type is distinguished by the seriousness of the criminal act and the amount of the imposed punishment. Besides, this chapter defines intent and motive as the mental elements of offenses. Intent consists of the will to commit an offense defined by law (Art.188). Thus, intentional offenses (Art.189) are distinguished from unintentional offenses (Art.191). Political offenses are considered intentional offenses (Art.196). Motive is the reason or end purpose that prompted the perpetrator to act (Art.192). Based on the consideration of the judge, the penalties imposed for honorable motive are heavier than those imposed for dishonorable motive (Art.193, Art.194). The material elements of offenses are also defined in this chapter. Examples of material elements are attempt (Art.200), defense (Art.184), and plurality of causes (Art.204).

Table 1 Definitions of terms reused from UFO (from [26].).

| Term                               | Definition                                                                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Substance                          | existentially independent particular (e.g., individual person, house, car, etc.)                                                                         |
| Agent                              | an agentive substantial particular                                                                                                                       |
| Object                             | a non-agentive substantial particular                                                                                                                    |
| Physical Agent                     | a human agent (a person)                                                                                                                                 |
| Physical Object                    | such as a book, a car, etc.                                                                                                                              |
| Social Agent                       | an organization or a society                                                                                                                             |
| Social Object                      | include money, language, and Normative Descriptions                                                                                                      |
| Normative Description              | defines one or more rules/norms recognized by at least one social agent, which can define nominal universals such as social moments, objects, and roles. |
| Moment                             | an individualized property that is existentially dependent on individuals                                                                                |
| Intrinsic Moment                   | a moment that depends on a single individual (e.g., color, temperature, etc.)                                                                            |
| Intentional Moment                 | such as Belief , Desire , Intention . Agents are substantials that can bear intentional moments.                                                         |
| Intention                          | intending something , a specific type of intentionality                                                                                                  |
| Externally Dependent Social Moment | an intrinsic moment that inheres in a single individual but existentially dependent on (possibly multiple) other individuals.                            |
| Relator                            | a moment that depends on a plurality of individuals (e.g., employment, medical treatment, marriage).                                                     |
| Social Relator                     | an example of a relator composed of two or more pairs of associated commitments/claims (social moments)                                                  |
| Event                              | a perdurant or occurrent. Events are ontologically dependent entities in the sense that they existentially depend on their participants to exist         |
| Situation                          | special type of endurants. In UFO, Situations are synonymous with the state of affairs in the literature                                                 |
| Participation                      | an event that represents the participation of an agent or object in a given event                                                                        |
| Agent Participation                | a Participation of an agent in a given event                                                                                                             |
| Action                             | an intentional Event performed by an agent and caused by intention. Only agents (entities capable of bearing intentional moments) can perform actions.   |
| Action Contribution                | an intentional Agent Participation performed by an Agent . Not any participation of an agent is considered an action                                     |

- Criminal Convictions : establishes the penalties (Art.37) and the precautionary measures (Art.70). Besides, it defines the grounds of the remission of criminal sentences (e.g., special pardon (Art.152)). The penalties are classified into different categories depending on the offense type (felonies, misdemeanors, and contraventions).
- Felonies and misdemeanurs against persons : defines the felonies and misdemeanurs against human life, physical integrity, or property.
- Responsibility chapter defines the responsible persons such as the perpetrator of an offense (Art.122), the accomplice (Art.123), the instigator (Art.217), and the accessory (Art.219). Besides, this chapter addresses the impediments to prosecution such as error (Art.223 and Art.224), Force majeure (Art.227), and absence of responsibility (e.g., insanity (Art.231), intoxication (Art.235), etc.). The grounds for exemption from penalty or for mitigation or aggravation of penalty are also regulated in this chapter.

CriMOnto's purpose is to represent faithfully and explicitly the content of procedural norms for reasoning and decision-making. We seek to develop a (lightweight) semantic application to support legal scholars in solving legal problems. To achieve this goal, CriMOnto will be employed to formalize the legal procedures of criminal law. As an example of lightweight decision support, given a set of facts related to a criminal case (e.g., a person 𝑋 has attacked 𝑌 , 𝑋 was under the influence of intoxication, etc.), the formalized legal rules will be used to generate legal effects such as customary penalties (e.g., imprisonment, fine, etc.) or penalty exemption.

Ontology requirements. They are divided into two categories functional and non-functional [35]. The former category defines what needs to be expressed by the ontology model. Functional requirements are expressed using a set of Competency Questions (CQs) that must be fulfilled by applying the COPs. The latter specifies how an ontology needs to be designed to be applicable. CriMOnto has to fulfill the following functional requirements:

- FR1To represent the main types of agents (e.g., judge , offender , victim ), objects (e.g., legal document , legal rule ), and their hierarchical structure (e.g., offender is a legal agent ). Examples of CQs addressed to fulfill this requirement are: (CQ1) What are the main types of legal agents? (CQ2) How are legal agents structured? (CQ3) What are the main types of objects? (CQ4) How are objects structured?

Fig. 9. Excerpt of the Lebanese Criminal Code (Ch. Offenses ).

[FIGURE]

Table 2 Definitions of terms reused from UFO-L (from [21]).

| Term                              | Definition                                                                                                                                                                                                                      |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Legal Agent                       | an agent that plays relevant social role(s) in the legal domain in the context of legal relationships                                                                                                                           |
| Singular Legal Agent              | represents a single Human Agent with the capacity to acquire rights and contract obligations                                                                                                                                    |
| Agentive Legal Institution        | a legal entity composed of a minimum of two singular legal agents                                                                                                                                                               |
| Legal Object                      | a non-agent category specializing in Legal Normative Description and Legal Norm                                                                                                                                                 |
| Legal Normative Description       | represents the description or the statement of the legal norm in the form of the text of law, constitution, or contract. It defines legal entities (e.g., legal agents, legal roles, legal events, etc.)                        |
| Legal Norm                        | represents the content of a legal normative description                                                                                                                                                                         |
| Legally Defined Event             | specialization in the legal field of UFO's event, defined by one or more Legal Normative Description and expressed by one or more Legal Norm                                                                                    |
| Legal Relator                     | a specialization of UFO's Social Relator composed of two or more pairs of Externally Dependent Legal Moments                                                                                                                    |
| Simple Legal Relator              | represents the reification of relationships between Substantials that have an inherent relationship with Externally Dependent Legal Right-Duty Moments; Permission-No-Right; Legal Power-Legal Subjection; Disability-Immunity. |
| Externally Dependent Legal Moment | a legal position, such as: Duty , Right , Permission , Legal Power and Legal Subjection                                                                                                                                         |
| Power-Subjection Relator          | the relationship where the Power Holder has jurisdiction (or legal power) to create (change, extinguish) a legal position or situation in the face of the Subjection Holder                                                     |
| Disability-Immunity Relator       | the relationship where Disability Holder has no competence to act against Immunity Holder to create, modify, or extinguish legal positions or situations. It is the negation of the Power-Subjection relationship               |
| Legal Power                       | an Externally Dependent Legal Moment that is characterized by the creation, alteration, or termination of legal positions of the other Legal Agent in the relationship                                                          |
| Legal Subjection                  | represents the correlate of Legal Power                                                                                                                                                                                         |
| Disability                        | an Externally Dependent Legal Moment that is characterized by the denial of Legal Power                                                                                                                                         |
| Immunity                          | a position of non-subjugation in the face of the state                                                                                                                                                                          |

- FR2To describe the legal events (e.g., offense , penalty ), situations (e.g., Force Majeure , error , insanity , etc.), and their hierarchical structure. Examples of CQs addressed to fulfill this requirement are: (CQ1) What are the main types of legal events? (CQ2) How are these events structured? (CQ3) What are the main situations defined in the legal context? (CQ4) How are these situations structured?
- FR4To define the legal relators and their hierarchical structure (e.g., punishment relator is a power-subjection legal relator that defines the different interactions between the offender and the legal agent imposing the penalty). Examples of CQs addressed
- FR3To describe the participation of agents in criminal acts (e.g., intentional offense , unintentional offense , etc.) and their hierarchical structure. Examples of CQs addressed to fulfill this requirement are: (CQ1) What are the main types of agent participation? (CQ2) How are these participation types structured?

to fulfill this requirement are: (CQ1) What are the main types of legal relators? (CQ2) How are these relators structured? (CQ3) Do any legal rules defining these relators exist? (CQ4) Do any legal events exist grounding these relators?

- FR6To define legal moments (i.e., normative positions) comprising legal relators and their hierarchical structure. Examples of legal moments that make up the punishment relator are: power to punishment (inherited in the judge) and subjection to punishment (inherited in the offender). Examples of CQs addressed to fulfill this requirement are: (CQ1) What are the moments considered in the legal context? (CQ2) How are these moments structured?
- FR5To state precisely the involvement of agents in the legal relators (i.e., the legal roles associated with the legal agents in the context of the legal relators). For instance, the offender is a subjection holder , and the judge is a power holder involved in the punishment relator . Examples of CQs addressed to fulfill this requirement are: (CQ1) What legal roles are involved in legal relators? (CQ2) How are these roles structured?

Besides, it is required to precise the mental moments of offenders (e.g., intention , motive ). Examples of CQs addressed to fulfill this requirement are: (CQ1) What mental moments are considered in the legal context? (CQ2) How are these moments structured?

Additionally, CriMOnto has to fulfill the following non-functional requirements:

- NFR1Distinction between reference and operational ontology models.
- NFR3Ontology extensibility to include future aspects.
- NFR2Ontology reusability and shareability over the Semantic Web.

Ontology design. Aiming to reduce the complexity of the ontology building process, we apply ontology layering [36] to divide the ontology structure into three layers (UOL, COL, and DOL) located at different granularity levels (see Fig. 10 for an example). Ontology layering helps to clearly identify the granularity levels in the ontology model and reduces the complexity of building the hierarchical structure. Besides, it will simplify the ontology extension and enrichment. UOL (Upper Ontology Layer), which is located at the most abstract level, contains domain-independent categories (e.g., agent, object, role, event, action, situation, etc.). COL (Core Ontology Layer) includes categories commonly dependent on the legal domain (e.g., legal agent, legal rule, legal act, etc.). DOL (Domain Ontology Layer) describes the main categories of criminal law (e.g. intention, criminal act, fault, offense, offender, punishment, etc.). In addition, as SABiO suggests, ontology modularization [16] is applied within each layer to maintain CriMOnto's modular building and permit the reusing of parts of the ontology.

Conceptualization. To develop the reference model of CriMOnto, conceptual ontology patterns (COPs), identified as ontology modules, are selected and reused from UFO and UFO-L. These patterns are small and autonomous components [37]. A small pattern typically comprises two to ten classes with relations defined between them. Smallness also allows diagrammatical visualizations that are acceptable and easily memorizable. The autonomy of COPs facilitates ontology design: the composition of COPs enables them to govern the complexity of the entire ontology [37]. In this context, we suggest using two main types of patterns: recognition patterns, defined as a recurring set of concepts and relations, and template patterns, that describe a common perspective on how to solve a specific problem [37,38]. The latter could be reused in many cases, representing best practices to solve modeling problems [38]. By distinguishing the patterns, we aim to separate the building of the hierarchical and the procedural content of the ontology. For building the upper and core layers, selected patterns from UFO and UFO-L are reused as building blocks, mapped, and composed in the light of UFO as a reference ontology, permitting the consistency of the composition to be checked. The recognition patterns are applied by extension for building the hierarchical , or structural , content of the domain layer. Meanwhile, the template patterns are applied by analogy with the legal norms for building the procedural content. This phase is performed using OntoUML [20] as a higher-order representation language, allowing the representation of COPs and their application using UFO's modeling primitives. As tooling, the library ontouml-js provides an Application Programming Interface (API) to programmatically create, navigate, and query OntoUML models. 2 Besides, different modeling services are maintained using the open-source OntoUML plugin 3 for Visual Paradigm, 4 such as syntax verification (a service that parses an OntoUML model and verifies its compliance with OntoUML's syntactical rules [39]) and transformation to OWL (a parameterized service that generates OWL specifications compliant with gUFO [40], the reference implementation of UFO in OWL) (see Figs. 10 and 11).

Ontology validation and evaluation. This phase transforms the reference model, which is language-independent, into an operational ontology represented using OWL as computational language. Representing CriMOnto in OWL is required for ontology (re)use over the Semantic Web [37]. Besides, the ontology consistency and validity regarding its requirements are evaluated.

## 4. The building process of CriMOnto: The reference model

This section describes the main contribution of this study. To develop CriMOnto's reference model, which comprises three layers, conceptual ontology patterns are extracted from UFO and UFO-L. For this purpose, we defined recognition and template patterns. The recognition patterns are excerpts of UFO (see Figs. 1, 3, and 2) and UFO-L (see Figs. 4, 6, and 5), extracted based on CriMOnto's Definitions of technical legal terms specified in CriMOnto's hierarchical content.

[2 Maintained by CORE, https://www.inf.unibz.it/krdb/core/.](https://www.inf.unibz.it/krdb/core/)

[3 https://purl.org/krdb-core/ontouml-plugin.](https://purl.org/krdb-core/ontouml-plugin)

[4 https://www.visual-paradigm.com/.](https://www.visual-paradigm.com/)

Table 3

| Concept                    | Definition                                                                                                                                                                                                                                                                                                       |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Judge                      | a Legal Professional who imposes liabilities and penalties                                                                                                                                                                                                                                                       |
| Offender                   | a Law Violator who commits a criminal or harmful act                                                                                                                                                                                                                                                             |
| Criminal Act               | an illegal or harmful act defined as an Action Contribution                                                                                                                                                                                                                                                      |
| Offense                    | a Law Violation defined as a Felony , a Misdemeanour or a Contravention (Art. 179)                                                                                                                                                                                                                               |
| Intentional Offense        | a specialization of Offense and Criminal Act (committed with purposeful intention)                                                                                                                                                                                                                               |
| Unintentional Offense      | an Offense committed as an Agent Participation (without purposeful intention)                                                                                                                                                                                                                                    |
| Criminal Conviction        | a Judicial Act (intentional participation performed by a judge)                                                                                                                                                                                                                                                  |
| Penalty                    | a Criminal Conviction (e.g., imprisonment, fine, etc.). Penalties are defined as customary (e.g., Art.37-customary penalties of felonies are hard-labor for life, life imprisonment, etc.) and can be imposed by commutation, aggravation, or extenuation depending on the circumstances defined by criminal law |
| Fault                      | a Mental Moment where a harmful act results from negligence, recklessness or failure to comply with laws and regulations (Art. 190)                                                                                                                                                                              |
| Motive                     | a Mental Moment defined as the reason that prompted the perpetrator to act (Art.192)                                                                                                                                                                                                                             |
| Motive Quality             | a Motive may be qualified by the judge as honorable or dishonorable                                                                                                                                                                                                                                              |
| Loss of Awareness          | a Mental Moment describing the loss of consciousness as a mental state [41]                                                                                                                                                                                                                                      |
| Impediments to Prosecution | a set of circumstances defined by criminal law to replace or exempt from penalties (e.g., insanity, intoxication, Force Majeure, etc.)                                                                                                                                                                           |

requirements, and reused as building blocks for modeling the hierarchical structure of the upper and core layers. Furthermore, these patterns are extended to develop the hierarchical content of the domain layer. The template patterns are selected from UFO-L, reused in the core layer, and applied by analogy with the procedural norms to explicitly represent the procedural content of the domain layer. Based on the ontology requirements, we selected two template patterns from UFO-L (Figs. 7 and 8). Therefore, UOL is composed of three ontology patterns (Figs. 1, 3, and 2) and COL is composed of five patterns (Figs. 4, 6, 5, 7, and 8). The intra and inter-layer relationships are maintained by relating UFO's primitives and verified by applying the OntoUML constraints. In the following section, we discuss DOL's building process. Tables 3 and 4 give some terms and definitions of the hierarchical and procedural contents.

## 4.1. Hierarchical content

Extension of UFO-L::Legal\_Agent . To fulfill FR1, the following CQs are addressed: (CQ1) What are the main types of legal agents defined in the criminal code? (CQ2) How are these agents structured? (CQ3) Are there defined agentive legal institutions? (CQ4) How are legal institutions structured? Two main types of legal agents are defined: Offender (Art.262) as a law violator and Judge (Art.181) as a legal professional. Court (Art.163) is identified as a legal institution composed of judges. For offenders, four main types are defined: Perpetrator (Art.212), Accomplice (Art.213), Instigator (Art.217), and Accessory (Art.219). For courts, the Criminal\_Court is specified (Art.68). Fig. 11 depicts the classification of the different types of legal agents.

Fig. 10. Example of structure layering in CriMOnto.

[FIGURE]

Table 4 Definitions of technical legal terms specified in CriMOnto's procedural content.

| Concept                                   | Definition                                                                                                         |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Power-Subjection to Penalty               | a Power-Subjection Relator to define the legal power of judges to impose penalties against offenders               |
| Penalty-Relator                           | a legal relator generated from the criminal convictions (penalties) and created by Power-Subjection to Penalty     |
| Offense-Relator                           | a legal relator generated from the offense (event) on which depends the penalty relator                            |
| Power-Subjection to Penalty Commutation   | a Power-Subjection Relator to define the legal power of judges to replace penalties in situations defined by law   |
| Power-Subjection to Fault-Based Liability | a Power-Subjection Relator to define the legal power of judges to impose fault-based liabilities against offenders |
| Exemption from Punishment                 | a Disability-Immunity Relator to define the exemption of offenders from penalty                                    |
| Judge as Power Holder                     | a Power Holder who imposes legal powers against offenders                                                          |
| Offender as Subjection Holder             | a Subjection Holder who is obligated to act or accept the judgment decided by the judge                            |
| Offender as Immunity Holder               | an Immunity Holder who has an immunity against punishment                                                          |
| Judge as Disability Holder                | a Disability Holder who has a disability of imposing penalties                                                     |
| Power to Impose Penalty                   | a Legal Power to impose penalties                                                                                  |
| Subjection to Penalty                     | a Legal Subjection to accept imposed penalties                                                                     |
| Power to Replace Penalty                  | a Legal Power to commute penalties                                                                                 |
| Subjection to Replace Penalty             | a Legal Subjection to accept imposed penalty commutation                                                           |
| Power to Impose Fault-Based Liability     | a Legal Power to impose fault-based liabilities                                                                    |
| Subjection to Fault-Based Liability       | a Legal Subjection to accept imposed fault-based liabilities                                                       |
| Disability to Punishment                  | a Disability legal moment characterized by the denial of punishment                                                |
| Immunity to Punishment                    | an Immunity legal moment characterized by the exemption from punishment                                            |

Fig. 11. Extension of UFO-L::Legal\_Agent .

[FIGURE]

Art.262 [...] offender is a person whose criminal activity [...] to commit felonies [...]

Art.212 The perpetrator of an offence is anyone [...]

Art.213 An accomplice to an offence shall be liable [...]

Art.217 Anyone who induces another person [...] shall be deemed to be an instigator.

Art.219 [...] shall be deemed to be accessories to a felony or misdemeanour [...]

Art.181 [...] the Judge shall impose [...]

Art.163 [...] the sentence imposed by the court [...]

Art.68 The Criminal Court may order the publication of any criminal decision [...]

Extension of UFO::Agent\_Participation . To fulfill FR3, the following CQs are addressed: (CQ1) What are the main types of offenses? (CQ2) How are these offenses structured? (CQ3) How are penalties for offenses specified? Offenses are categorized into Felony , Misdemeanor , and Contravention (Art.197), which are punishable by penalties (Art.37, Art.179). Besides, Intentional\_Offense (Art.189) and Unintentional\_Offense (Art.190) are distinguished (see Fig. 12).

[FIGURE]

Fig. 12. Extension of UFO::Agent\_Participation .

[FIGURE]

Fig. 13. Extension of UFO::Mental\_Moment .

```
Art.189 An offence shall be deemed to be intentional [...] Art.190 An offence is unintentional [...] Art.179 An offence is defined as a felony, a misdemeanour or a contravention and is accordingly punishable by a penalty [...] Art.37 The customary penalties for felonies [...]
```

Extension of UFO::Mental\_Moment . In the Lebanese Criminal Code, the basic mental elements are intent (Art. 188) and fault (Art. 190). Besides, motive is considered a mental element in cases specified by law (Art. 192). Based on Kenny's [42] description of motives as ''backward-looking'' and intentions as ''forward-looking'' reasons for action [43], we considered Motive , as Intention defined in UFO, as a Mental\_Moment specification (see Fig. 13). The same aspect is also applied to define Fault . As a mental moment, Loss\_of\_Awareness is also described (e.g., Art.235). To fulfill FR6, the addressed CQs are: (CQ1) What is a motive? (CQ2) By what quality is a motive qualified? (CQ3) What are the main types of motives? (CQ4) What is a fault? (CQ5) What is a loss of awareness?

```
Art.192 Motive is the reason [...] that prompted the perpetrator to act. Art.193 If the Judge considers that the motive was honourable [...] Art.194 If the offence [...] was prompted by a dishonourable motive [...] Art.195 If an offence [...] is perpetrated with the motive of gain [...] Art.196 Political offences are [...] committed by the perpetrator for a political motive [...] unless the perpetrator was prompted by a selfish and base motive. Art.190 Fault exists where a harmful act results from negligence, recklessness or failure to comply with laws and regulations. Art.235(1) Any person who, when committing an act, was [...] in a state of intoxication from alcohol or drugs that caused him to lose awareness [...]
```

Extension of UFO::situation . To fulfill FR2, the addressed CQs are: (CQ1) What are the main types of circumstances defined in criminal law? (CQ2) How are these circumstances structured? In the Criminal Code, impediments to prosecution (e.g., Force\_Majeure (Art.227), Error\_of\_Fact (Art.224), Insanity (Art.231), and Intoxication\_and\_Drug\_ Addiction (Art.235)), aggravating (Art.257), and extenuating (Art.253) circumstances are defined (Fig. 14).

[FIGURE]

Fig. 14. Excerpt of extending UFO::Situation .

[FIGURE]

Fig. 15. Excerpt of extending UFO-L::Legal\_Relator .

| Art.224   | Anyone who acted on the basis of an error of fact [...]                                                                   |
|-----------|---------------------------------------------------------------------------------------------------------------------------|
| Art.227   | Anyone who acts under irresistible physical or moral duress [...]                                                         |
| Art.231   | Any person in a state of insanity that causes him to lose awareness [...]                                                 |
| Art.235   | Any person who [...] in a state of intoxication from alcohol or drugs that caused him to lose awareness [...]             |
| Art.257   | [...] the effect of an aggravating circumstance, the circumstance shall entail the following increases in penalties [...] |
| Art.253   | If there are extenuating circumstances in a case, the court shall decide: [...]                                           |

Extension of UFO-L::Legal\_Relator . To fulfill FR4, the addressed CQs are: (CQ1) What main power-subjection relators are defined in the criminal law context? (CQ2) What does criminal law define as disability-immunity relators? (CQ3) Are there specified relators regarding committing offenses? (CQ4) Have any specific legal relators regarding penalties been identified? Based on the criminal code and by analogy with UFO-L selected template patterns, we specified the following legal relators: Power-Subjection\_to\_Penalty (Art.193),

Power-Subjection\_to\_Liability (Art.213),

Power-Subjection\_to\_Penalty\_Commutation

Exemption\_from\_Punishment

```
(Art.194), (Art.231), and
```

Power-Subjection\_to\_Fault-Based\_Liability (Art.235(2)) (Fig. 15). Two additional legal relators, Offense\_ Relator and Penalty\_Relator , are identified to explicitly represent the interactions generated by the Offense and Penalty events. The extended legal relators' procedural aspect is discussed in Section 4.2.

Art.193 [...] the Judge [...] shall impose the following penalties [...] Art.194 [...] the judge shall replace life imprisonment with hard labour for life; Art.231 Any person in a state of insanity [...] shall be exempt from prosecution. Art.235(2) If the state of intoxication was due to a fault on the part of the perpetrator, he shall be held responsible for any unintentional offence committed.

Fig. 16. Generalized ontology module representing Art.548.

[FIGURE]

## 4.2. Procedural content

The procedural content explicitly represents the legal norms regulating penalties and liabilities by considering the different interactions between the legal agents. Generally, for imposing responsibilities or punishments, high level of capacity is required [1]. In the legal domain, judges and courts are the legal agents having the authority conferred by legal rules for imposing penalties and liabilities (Art.181 and Art.163). This study addresses the legal norms, focusing on the judges as the primary legal agents.

Art.181

[...] the Judge shall impose the heaviest penalty [...]

Art.163

```
[...] the sentence imposed by the court [...]
```

Power-Subjection\_to\_Penalty . In the Lebanese Criminal Code, penalties are regulated in two different ways: (1) as customary punishment regarding offense type (e.g., Art.38) and (2) as procedural norms depending on given circumstances (e.g., Art.548). In this context, Power-Subjection\_to\_Penalty relator is established to describe the process of imposing penalties by the judge (power holder) against the offender (subjection holder). The penalty is imposed depending on certain circumstances defined by law, such as holding a base motive for committing an intentional homicide (e.g., Art.548). The penalty relator, generated by the penalty and depends on the offense relator, is created by the legal-specific relator Power-Subjection\_to\_Penalty . Fig. 16 depicts a generalized modeling example of the interactions between the legal agents and the associated legal relators and positions. The addressed CQs are: (CQ1) Who commits the offense? (CQ2) For what motive is the offense committed? (CQ3) What legal relator is generated by the offense? (CQ4) By what penalty is the offense punishable? (CQ4) What legal relator is generated by the penalty? (CQ5) What power-subjection relator is established based on the promulgation of criminal law? (CQ6) What punishment does the judge impose against the offender?

Art.37

The customary penalties for felonies are: 1.Death; 2.Hard labor for life; 3.Life

```
imprisonment [...] Art.548 Intentional homicide shall be punished by hard labour for life if it was
```

committed: 1. For a base motive; [...]

Power-Subjection\_to\_Penalty\_Commutation . In the Lebanese code, the judge can substitute or replace the penalty against the offender depending on legally defined conditions, such as committing an offense based on a dishonorable motive (Art.194) or considering extenuating/aggravating circumstances (e.g., Art.253). Therefore, a Power-Subjection\_to\_ Penalty\_Commutation relator is established to explicitly represent the legal interactions between the judge and the offender and the associated legal relators and positions. In this context, the penalty\_Relator , generated by the penalty event and dependent on the offense relator, is modified by the penalty commutation legal relator. Fig. 17 depicts a generalized modeling of this process. The main CQs addressed in this model are: (CQ1) Who commits the offense? (CQ2) What motive has prompted the offense commitment? (CQ3) Is the offense punishable by a penalty? (CQ4) Is the penalty replaced by another penalty under the judge's decision?

Fig. 17. Generalized ontology module representing Art.194.

[FIGURE]

Art.194

If the offence [...] was prompted by a dishonourable motive, the Judge shall

replace: Life imprisonment with hard labour for life; If there are extenuating circumstances in a case, the court shall decide: [...] To replace hard labour for life with fixed-term hard labour [...]

Art.253

Power-Subjection\_to\_Fault-Based\_Liability . As defined by the law, the judge can decide, besides penalties, liabilities against offenders. The liabilities can be imposed directly (e.g., Art.213) or considering legally defined conditions or circumstances, such as Fault (e.g., Art.235), which elicit the decision of the responsibility of an unintentional offense . Respon-sibility\_of\_Unintentional\_Offense , created by the power-subjection relator, depends on the offense relator generated by the offense event. Fig. 18 depicts the legal interactions and the associated legal positions. While the judge has the power to impose a fault-based liability, the offense is subjective to such a decision. The CQs addressed for the modeling are: (CQ1) Who commits the offense? (CQ2) Under the influence of which circumstance is the offense committed? (CQ3) Does there exist any fault to which the circumstance is attributable? (CQ4) Who is responsible for this fault? (CQ5) What liability does the judge impose against the offender?

Art.213

An accomplice shall be liable to the penalty prescribed by law for the offence. If the state of intoxication was due to a fault on the part of the perpetrator, he

Art.235(2)

shall be held responsible for any unintentional offence committed.

Exemption\_from\_Punishment . In the criminal code, the offender has immunity from prosecution where he cannot be held liable for violating the law considering the impediments to prosecution . For instance, the offender who acted under drug intoxication (Art.235(1)) caused by a force majeure or under irresistible physical or moral duress (Art.227(1)) is exempted from punishment. In this context, the judge has a disability in imposing penalties against the offender. Thereby, Exemption\_from\_Punishment (a negation of Power-Subjection\_to\_Penalty ) is established by applying Disability-Immunity\_Relator by analogy with legal norms. Fig. 19 depicts the legal interactions and the associated legal relators and positions. While the offender has an immunity against punishment, the judge has a disability to impose punishment. The CQs addressed are: (CQ1) Who commits the offense? (CQ2) Under the influence of which circumstance is the offense committed? (CQ3) Does the offender suffer from a loss of awareness? (CQ4) By which circumstance is the loss of awareness caused? (CQ5) How is the punishment affected?

Fig. 18. Generalized ontology module representing Art.235(2).

[FIGURE]

Fig. 19. An ontology module representing Art.235(1).

[FIGURE]

Fig. 20. Excerpt of CriMOnto's hierarchical content represented in Protégé.

[FIGURE]

Art.227(1)

Anyone who acts under irresistible physical or moral duress shall not be prosecuted.

Art.235(1)

Any person who, when committing an act, was fortuitously or owing to force majeure in a state of intoxication from alcohol or drugs that caused him to lose awareness or self-control shall be exempt from prosecution.

## 5. Ontology validation and evaluation

To validate CriMOnto, the reference model is transformed into an operational ontology manageable in ontology editors such as Protégé. 5 The transformation process is performed using ontouml-js plugin that generates gUFO OWL ontology [39, 44]. The code generator maps OntoUML classes, associations, and attributes to OWL classes and object properties. CriMOnto (v1.0) 6 defines 93 classes, 47 object properties, and 149 subClassOf relations. Fig. 20 depicts part of the hierarchical content and Fig. 21 illustrates an excerpt of the procedural content of around the concept Power-Subjection\_to\_Penalty\_ Commutation .

CriMOnto is evaluated using a dual approach: consistency and performance. For consistency, the OWL2 inference engine HermiT 7 is applied to ensure that the general qualities of CriMOnto are supported. For performance, a task-based evaluation is performed in Section 6 for assessing the effectiveness of CriMOnto in (lightweight) decision-making. Besides, we evaluated the ontology regarding the functional requirements defined in the development process (see Section 3) and expressed it in the form of Competency Questions (CQs). Thus, a set of SPARQL queries is formalized by translating the CQs defined in natural language. These queries are executed to interrogate CriMOnto's concepts and relations using defined instances. In the following, an excerpt of the SPARQL queries translated from the CQs specified for modeling Exemption\_from\_Punishment relator (Fig. 19) is presented. We use the instances defined for the decision support use case in Section 6.

[5 https://protege.stanford.edu/.](https://protege.stanford.edu/)

[6 https://doi.org/10.5281/zenodo.14945405.](https://doi.org/10.5281/zenodo.14945405)

[7 http://www.hermit-reasoner.com/.](http://www.hermit-reasoner.com/)

[FIGURE]

Fig. 21. Excerpt of CriMOnto's procedural content represented in Protégé.

```
(CQ1) Who commits the offense? SELECT ?offender WHERE {?offender rdf:type crimonto:Offender. ?offender crimonto:commits ?offense. ?offense rdf:type crimonto:Offense.} (CQ2) Under the influence of which circumstance is the offense committed? (CQ3) Is the circumstance produced by any other circumstance? SELECT DISTINCT ?situation ?situation2 WHERE { { ?offender crimonto:committed_under_the_influence_of ?situation.} UNION { ?situation crimonto:produced_by ?situation2 }} (CQ4) Does the offender suffer from a loss of awareness? SELECT ?suffering WHERE {?offender rdf:type crimonto:Offender. ?offender crimonto:suffersFrom ?suffering. ?suffering rdf:type crimonto:Loss_of_Awareness.}
```

## 6. Use case: Lightweight rule-based decision support

In this section, we employ CriMOnto in a lightweight rule-based decision support task to assess its decision-making performance. We aim to formalize the legal norms of the Criminal Code based on CriMOnto. The formalization process considers (1) the explicit representation of procedural norms captured in CriMOnto; (2) a rule language that formalizes the legal rules, and permits for computing the legal effects that should follow from the set of formal rules [45]; (3) the Isomorphism principle stated by Bench-Capon to create a well-defined correspondence between the rules in the formal model and the units of natural language text that express the rules in the original legal sources as sections of the legislation [8]. As a rule language, we selected SWRL, 8 a rule interchange format that combines ontologies represented in OWL with RuleML. It extends OWL axioms to include (monotonic) Horn-like rules. Thus, the formal rules are expressed in OWL concepts, and the reasoning is performed based on OWL individuals [46]. In the following, we discuss the formalization of two procedural norms (Art.194 and Art.235(1)) and compute the legal effects of executing the associated formal rules. A set of instances are defined for this purpose (see Fig. 22).

[8 https://www.w3.org/Submission/SWRL/.](https://www.w3.org/Submission/SWRL/)

Fig. 22. Example of SPARQL query results for CQs of Art.235-1.

[FIGURE]

Each procedural norm is formalized into two chained rules based on the procedural modeling represented in OntoUML (see Fig. 17 and Fig. 19). Obligation rules represent these rules in the following form:

IF condition (input facts) THEN conclusion (legal effects)

While the first rule (R1) creates the legal relator between the legal agents based on given facts (e.g., agents, situations, events, etc.), the second rule (R2) generates the legal effects (e.g., imposing penalties, replacing penalties, etc.). Thus, the execution process relies on input facts to fulfill the condition of R1. Furthermore, the inference engine (e.g., HermiT) matches the SWRL rules with the given facts and generates convenient legal effects by executing the chained rules. Figs. 23 and 24 depict examples of generated legal effects (highlighted in yellow color) by executing the formal rules representing Art.194 and Art.235(1).

| Art.194   | If the offence is punishable by life imprisonment and was prompted by a dishonourable motive, the Judge shall replace: Life imprisonment with hard labour for life;                                                                      |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| R1        | 𝑂𝑓𝑓𝑒𝑛𝑑𝑒𝑟 (? 𝑥 ) ∧ 𝑂𝑓𝑓𝑒𝑛𝑠𝑒 (? 𝑦 ) ∧ 𝑐𝑜𝑚𝑚𝑖𝑡𝑠 (? 𝑥, ? 𝑦 ) ∧ 𝑀𝑜𝑡𝑖𝑣𝑒 (? 𝑧 ) ∧ ℎ𝑎𝑠 (? 𝑥, ? 𝑧 ) ∧                                                                                                                                               |
|           | ℎ𝑎𝑠 _ 𝑞𝑢𝑎𝑙𝑖𝑡𝑦 (? 𝑧, 𝑑𝑖𝑠ℎ𝑜𝑛𝑜𝑟𝑎𝑏𝑙𝑒 ) ∧ 𝑝𝑟𝑜𝑚𝑝𝑡𝑒𝑑 _ 𝑏𝑦 (? 𝑦, ? 𝑧 ) ∧ 𝐽𝑢𝑑𝑔𝑒 (? 𝑣 ) ∧ 𝑈𝐹𝑂 - 𝐿 ∶∶                                                                                                                                               |
|           | 𝐿𝑒𝑔𝑎𝑙 _ 𝑅𝑒𝑙𝑎𝑡𝑜𝑟 (? 𝑤 ) ∧ 𝑔𝑟𝑜𝑢𝑛𝑑𝑠 (? 𝑦, ? 𝑤 ) ⇒                                                                                                                                                                                           |
|           | 𝑃𝑜𝑤𝑒𝑟 - 𝑆𝑢𝑏𝑗𝑒𝑐𝑡𝑖𝑜𝑛 _ 𝑡𝑜 _ 𝑃𝑒𝑛𝑎𝑙𝑡𝑦 _ 𝐶𝑜𝑚𝑚𝑢𝑡𝑎𝑡𝑖𝑜𝑛 (? 𝑤 ) ∧ 𝑂𝑓𝑓𝑒𝑛𝑑𝑒𝑟 _ 𝑎𝑠 _ 𝑆𝑢𝑏𝑗𝑒𝑐𝑡𝑖𝑜𝑛 _ 𝐻𝑜𝑙𝑑𝑒𝑟 (? 𝑥 ) ∧                                                                                                                                    |
|           | 𝐽𝑢𝑑𝑔𝑒 _ 𝑎𝑠 _ 𝑃𝑜𝑤𝑒𝑟 _ 𝐻𝑜𝑙𝑑𝑒𝑟 (? 𝑣 ) ∧ 𝑚𝑒𝑑𝑖𝑎𝑡𝑒𝑠 (? 𝑤, ? 𝑥 ) ∧ 𝑚𝑒𝑑𝑖𝑎𝑡𝑒𝑠 (? 𝑤, ? 𝑣 )                                                                                                                                                         |
| R2        | 𝑂𝑓𝑓𝑒𝑛𝑑𝑒𝑟 _ 𝑎𝑠 _ 𝑆𝑢𝑏𝑗𝑒𝑐𝑡𝑖𝑜𝑛 _ 𝐻𝑜𝑙𝑑𝑒𝑟 (? 𝑥 ) ,𝐽𝑢𝑑𝑔𝑒 _ 𝑎𝑠 _ 𝑃𝑜𝑤𝑒𝑟 _ 𝐻𝑜𝑙𝑑𝑒𝑟 (? 𝑣 ) ,𝑃𝑜𝑤𝑒𝑟 -                                                                                                                                                  |
|           | 𝑆𝑢𝑏𝑗𝑒𝑐𝑡𝑖𝑜𝑛 _ 𝑡𝑜 _ 𝑃𝑒𝑛𝑎𝑙𝑡𝑦 _ 𝐶𝑜𝑚𝑚𝑢𝑡𝑎𝑡𝑖𝑜𝑛 (? 𝑤 ) ⇒ ℎ𝑎𝑠 _ 𝑎 _ 𝑝𝑜𝑤𝑒𝑟 _ 𝑡𝑜 _ 𝑟𝑒𝑝𝑙𝑎𝑐𝑒 _ 𝑎 _ 𝑝𝑒𝑛𝑎𝑙𝑡𝑦 _ 𝑎𝑔𝑎𝑖𝑛𝑠𝑡 (? 𝑣, ? 𝑥 ) ∧ 𝑟𝑒𝑝𝑙𝑎𝑐𝑒𝑑 _ 𝑏𝑦 ( 𝑙𝑖𝑓𝑒 _ 𝑖𝑚𝑝𝑟𝑖𝑠𝑜𝑛𝑚𝑒𝑛𝑡, ℎ𝑎𝑟𝑑 _ 𝑙𝑎𝑏𝑜𝑟 _ 𝑓𝑜𝑟 _ 𝑙𝑖𝑓𝑒 ) ∧ 𝑝𝑢𝑛𝑖𝑠ℎ𝑒𝑑 _ 𝑏𝑦 (? 𝑥, ℎ𝑎𝑟𝑑 _ 𝑙𝑎𝑏𝑜𝑟 _ 𝑓𝑜𝑟 _ 𝑙𝑖𝑓𝑒 ) |

Fig. 23. Legal effects generated in Protégé by executing SWRL rules of Art.194.

[FIGURE]

Art.235(1) Any person who, when committing an act, was fortuitously or owing to force majeure in a state of intoxication from alcohol or drugs that caused him to lose awareness or self-control shall be exempt from prosecution.

R1

R2

𝑂𝑓𝑓𝑒𝑛𝑑𝑒𝑟 (? 𝑥 ) ∧ 𝑂𝑓𝑓𝑒𝑛𝑠𝑒 (? 𝑦 ) ∧ 𝑐𝑜𝑚𝑚𝑖𝑡𝑠 (? 𝑥, ? 𝑦 ) ∧

𝐼𝑛𝑡𝑜𝑥𝑖𝑐𝑎𝑡𝑖𝑜𝑛

𝐴𝑑𝑑𝑖𝑐𝑡𝑖𝑜𝑛

\_

𝑐𝑜𝑚𝑚𝑖𝑡𝑡𝑒𝑑

\_

𝑎𝑛𝑑

𝑢𝑛𝑑𝑒𝑟

𝑝𝑟𝑜𝑑𝑢𝑐𝑒𝑑

\_

\_

𝑏𝑦

\_

𝑠𝑢𝑓𝑓𝑒𝑟𝑠

𝐷𝑟𝑢𝑔

\_

𝑡ℎ𝑒𝑖𝑛𝑓𝑙𝑢𝑒𝑛𝑐𝑒

𝑓

\_

(?

𝑖

) ∧

𝑖𝑠

𝑜𝑓

\_

) ∧

𝑖𝑛

) ∧

(?

?

𝑦,

𝑖

𝐴𝑤𝑎𝑟𝑒𝑛𝑒𝑠𝑠

\_

𝑎

\_

𝑠𝑡𝑎𝑡𝑒

𝐹𝑜𝑟𝑐𝑒

(?

(?

𝑖,

?

𝑓𝑟𝑜𝑚

) ∧

𝑈𝐹𝑂

\_

\_

𝐿𝑜𝑠𝑠

𝑜𝑓

(?

?

) ∧

𝑥,

𝑙

𝐽𝑢𝑑𝑔𝑒

\_

(?

𝑣

𝐿𝑒𝑔𝑎𝑙 \_ 𝑅𝑒𝑙𝑎𝑡𝑜𝑟 (? 𝑤 ) ∧ 𝑔𝑟𝑜𝑢𝑛𝑑𝑠 (? 𝑦, ? 𝑤 ) ⇒

𝐸𝑥𝑒𝑚𝑝𝑡𝑖𝑜𝑛 \_ 𝑓𝑟𝑜𝑚 \_ 𝑃𝑢𝑛𝑖𝑠ℎ𝑚𝑒𝑛𝑡 (? 𝑤 ) ∧ 𝑂𝑓𝑓𝑒𝑛𝑑𝑒𝑟 \_ 𝑎𝑠 \_ 𝐼𝑚𝑚𝑢𝑛𝑖𝑡𝑦 \_ 𝐻𝑜𝑙𝑑𝑒𝑟 (? 𝑥 ) ∧

𝐽𝑢𝑑𝑔𝑒 \_ 𝑎𝑠 \_ 𝐷𝑖𝑠𝑎𝑏𝑖𝑙𝑖𝑡𝑦 \_ 𝐻𝑜𝑙𝑑𝑒𝑟 (? 𝑣 ) ∧ 𝑚𝑒𝑑𝑖𝑎𝑡𝑒𝑠 (? 𝑤, ? 𝑥 ) ∧ 𝑚𝑒𝑑𝑖𝑎𝑡𝑒𝑠 (? 𝑤, ? 𝑣 )

𝐸𝑥𝑒𝑚𝑝𝑡𝑖𝑜𝑛 \_ 𝑓𝑟𝑜𝑚 \_ 𝑃𝑢𝑛𝑖𝑠ℎ𝑚𝑒𝑛𝑡 (? 𝑤 ) ∧ 𝑂𝑓𝑓𝑒𝑛𝑑𝑒𝑟 \_ 𝑎𝑠 \_ 𝐼𝑚𝑚𝑢𝑛𝑖𝑡𝑦 \_ 𝐻𝑜𝑙𝑑𝑒𝑟 (? 𝑥 ) ∧

𝐽𝑢𝑑𝑔𝑒

\_

𝑎𝑠

\_

𝐷𝑖𝑠𝑎𝑏𝑖𝑙𝑖𝑡𝑦

\_

𝐻𝑜𝑙𝑑𝑒𝑟

(?

𝑣

)

⇒

ℎ𝑎𝑠 \_ 𝑎 \_ 𝑑𝑖𝑠𝑎𝑏𝑖𝑙𝑖𝑡𝑦 \_ 𝑡𝑜 \_ 𝑝𝑟𝑜𝑠𝑒𝑐𝑢𝑡𝑖𝑜𝑛 \_ 𝑎𝑔𝑎𝑖𝑛𝑠𝑡 (? 𝑣, ? 𝑥 )

\_

(?

𝑜𝑓

𝑥,

\_

?

𝑖

𝑀𝑎𝑗𝑒𝑢𝑟𝑒

𝑙

) ∧

𝑐𝑎𝑢𝑠𝑒𝑑

-

𝐿

∶∶

(?

\_

𝑏𝑦

(?

) ∧

𝑓

) ∧

𝑙,

?

𝑖

) ∧

## 7. Related work

Legal ontologies are considered solid support for legal information systems, as they permit explicitly defining the components of legal knowledge [36]. Much work has been done in the literature for developing legal core and domain ontologies. Legal core ontologies are considered as ''a kind of legal ontology that represents a shared conceptualization of generic legal concepts, which can be used and reused in constructing other more specific legal ontologies'' [29]. Examples of legal core ontologies are FOLAW (LRI-Core) [13,47], CLO [36], LKIF-Core [48], and recently UFO-L [21,31,49]. What differentiates UFO-L from the rest of the core ontologies, besides its solid foundation in the Unified Foundational Ontology UFO, is the definition of a taxonomy of legal relators based on Alexy's classification (rights to something, liberties, and powers) [30]. Additionally, patterns are defined to represent the procedural aspect of these relators, including the associated legal agents, interactions, and positions (e.g., right, duty, power, subjection, liberty, etc.). Without these patterns, the explicit representation of procedural norms in domain ontologies would be problematic.

Fig. 24. Legal effects generated in Protégé by executing SWRL rules of Art.235-1.

[FIGURE]

The domain, or domain-specific ontologies, represent specific parts of the law (e.g., criminal law, maritime law, civil law, etc.). In AI &amp; Law, different uses or roles of domain ontologies are identified [13], such as: (1) organize and structure information; (2) reasoning and problem-solving; (3) semantic indexing and search. Developing domain ontologies has been an active and promising research area in the ontology engineering community. For criminal law, various ontologies have been designed for different purposes.

For the Dutch Criminal Law, OCL.NL [50] is an ontology developed based on LRI-Core as a part of the e-COURT European IST project. The core of the OCL.NL consists of actions that are categorized in crime and punishment: (1) The criminal actions themselves (called ''offenses'') that are executed by the person who is successively acting as a suspect, defendant, and eventually convicted; (2) The punishments that are declared by the legal system.

For the Italian Criminal Law, we cite the Italian Crime Ontology [51] and LATO [4,5]. The Italian Crime Ontology [51] is a legal domain ontology constructed for crime modeling. Using UML class diagram, the ontological concept of crime is formalized. In this ontology, which is not based on foundational theories, the crime comprises the offender, behavior, penalty, and optionally by an event and compulsion. LATO [4,5] aims to capture and formalize the legal terminology as defined in real Italian court decisions. It is developed using a bottom-up approach based on SKOS. 9 The LATO ontology constitutes the core component of CRIKE (CRIme Knowledge Extraction), a data-science approach and related tool environment conceived to support legal knowledge extraction and enrichment from a corpus of Court Decision documents [5].

For the Brazilian Penal Code, different ontologies are designed: an ontology for infractions related to the drinking-and-driving law [52], an ontology for crimes against property [53], against life [54], and ontology for crimes of omission [6]. These studies aim to support decision-making, agent behavior classification, and inference of punishments. Methontology is applied to develop these ontologies. The relevant information is extracted from official texts in a middle-out strategy: from a list of relevant terms, the specialization and/or generalization of concepts is generated. In [6], a Criminal Core Ontology is proposed to represent crimes of omission. The modeling of the core ontology is rooted in the philosophical theories of the foundational ontology UFO. The core ontology considers criminal agents, objects, norms, situations, and punishments. The axiomatization of the criminal domain is illustrated using UML notation by considering the stereotypes of UFO.

[9 https://www.w3.org/2009/08/skos-reference/skos.html.](https://www.w3.org/2009/08/skos-reference/skos.html)

Finally, an ontology of criminal law and procedure (CLOR) is proposed in [3] for legal question answering. CLOR is harvested from selected bar exam questions under the supervision of domain experts. The ontology aims to design a terminological knowledge base using relationships, such as subclass and is-part-of and a rule base for legal reasoning composed of legal rules expressed in SWRL for reasoning about the crime elements.

CriMOnto shares the ontological rooting in foundational theories with the ontology of crimes of omission [6], which is neglected in LATO [5] and CLOR [3]. However, in CriMOnto, the legal core theories (defined in the core layer) are reused from the legal core ontology UFO-L and extended in the domain layer to represent various criminal aspects. Besides, applying UFO-L relator patterns ( Power-Subjection\_Relator and Disability-Immunity\_Relator ) by analogy with the procedural norms has enriched the ontology with a behavioral content aiming to faithfully and explicitly represent the legal procedures. Representing procedural norms is not considered in the ontologies mentioned above. This lack could be related to the ontologies' uses or roles. Meanwhile, we assume that a faithful representation of the criminal law, or any other law domain, must consider the procedural norms that constitute a fundamental part of the law.

## 8. Final considerations

Building legal domain-specific ontologies by considering foundational ontological theories is becoming fundamental in the ontology engineering community. However, explicitly representing the deontic characterization of regulative norms is challenging. This study discussed the explicit representation of procedural regulative norms in the context of the Lebanese Criminal Code and its usability in formalizing the source norms. To achieve the goal, we relied on reusing foundational and legal core theories from existent validated ontologies such as UFO [17-19] and UFO-L [21,31-33]. UFO is selected as a foundational ontology to ground our ontology in philosophical theories by applying the OntoUML conceptual modeling language. Also, we relied on UFO-L as a legal core ontology grounded in UFO to express the procedural aspect of legal relators identified in the context of criminal law, especially for power-subjection and disability-immunity patterns. Handling legal relators from a behavioral perspective is not supported in legal core ontologies, such as LKIF-Core [48] (the most recent legal core ontology preceding UFO-L). In CriMOnto, we applied the predefined patterns by analogy with the source norms to explicitly represent the criminal punishment, liabilities, responsibilities, and associated legal interactions among the different legal agents. The domain-specific extension of UFO-L's patterns has permitted a faithful description of the criminal legal effects achieved by fulfilling specified legally defined conditions or circumstances.

CriMOnto is a well-founded domain-specific ontology developed using different processes, such as layering, grounding, reuse, and modularization of the ontology. In addition, separating the hierarchical and procedural contents in CriMOnto has simplified its development and maintained the reuse or extension of parts of the ontology without affecting the core. CriMOnto is a generalized ontology that describes the legal knowledge that can be represented in Lebanese criminal law. We evaluated CriMOnto for consistency and performance. The CQs addressed throughout the modeling process are translated into SPARQL queries to assess the ontology's validity against its functional requirements. In addition, employing the ontology in a lightweight rule-based decision support task has verified its performance. However, our ontology does not represent descriptive rules, such as Art.189 and Art.191, which are devoid of regulative content due to the difficulty of expressing them using UFO-L basic patterns/relators. These norms, which communicate descriptive statements to define basic legal notions, such as intentional and unintentional offenses, are required to verify the fulfillment of conditions that lead to legal effects.

| Art.189   | An offence shall be deemed to be intentional, even if the criminal effect of the act or omission exceeds that intended by the perpetrator, if he had foreseen the possibility and thus accepted the risk.           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Art.191   | An offence is unintentional if the perpetrator did not foresee the consequence of his wrongful act or omission although he could or should have done so, or if he foresaw it and believed that he could prevent it. |

Also, the legal norms that include negations are not faithfully formalized in CriMOnto. This defect is due to the restriction of SWRL when expressing negations. To overcome this issue, especially regarding the articles arguing exemption from punishment (e.g., Art.227(1), Art.203(2), etc.) through negation (e.g., not prosecuted , not punished , etc.), we relied on modeling Exemption\_Punishment being a negation of Power-Subjection\_to\_Impose\_penalty (see Figs. 16 and 19).

- Art.227(1) Anyone who acts under irresistible physical or moral duress shall not be prosecuted.

- Art.203(2) The perpetrator shall not be punished, however, if his act stemmed from a misunderstanding.

Finally, complex norms (e.g., Art.263) are not considered in this study. In further works, we will examine the possibility of arranging these norms into sub-norms without affecting an accurate formalization.

Art.263

Any person who is sentenced to a penalty other than a fine for an intentional felony or misdemeanour and who, within five years of his sentence being served or time-barred, incurs a custodial sentence of at least one year for another intentional felony or misdemeanour shall be sentenced to confinement in isolation if it is established that he is a persistent offender and a danger to public safety.

In this study, we did not address challenging issues such as the contradictions or exceptions in law and the defeasible or nonmonotonic reasoning. In future works, we are interested in combining Logic Programming [55] with ontological reasoning for non-monotonic reasoning. For this purpose, we will transform the CriMOnto ontology into a logic program. Besides, our further work will address the typology of norms and principles.

## CRediT authorship contribution statement

Mirna El Ghosh: Conceptualization, Formal analysis, Methodology, Resources, Software, Validation, Writing - original draft, Writing - review &amp; editing. Hala Naja: Funding acquisition, Methodology, Supervision, Writing - review &amp; editing. Habib Abdulrab: Funding acquisition, Methodology, Supervision, Validation, Writing - review &amp; editing. Mohamad Khalil: Funding acquisition, Supervision, Writing - original draft, Writing - review &amp; editing.

## Declaration of competing interest

None declared.

## Acknowledgments

This study is supported by the Lebanese University, CNRS Lebanon, and the European Regional Development Fund (ERDF; Grant No: HN0002134).

## References

- [1] [K. Greenawalt, Punishment, J. Crim. Law Criminol. 74 (2) (1983).](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb1)
- [2] [J. Hall, General Principles of Criminal Law, second ed., The Lawbook Exchange, 2005.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb2)
- [3] A. Wyner, B. Fawei, J.Z. Pan, M. Kollingbaum, A methodology for a criminal law and procedure ontology for legal question answering, in: Semantic Technology, vol. 11341, 2018, pp. 198-214, http://dx.doi.org/10.1007/978-3-030-04284-4\_14.
- [4] S. Castano, A. Ferrara, M. Falduti, S. Montanelli, Crime knowledge extraction: An ontology-driven approach for detecting abstract terms in case law decisions, in: ICAIL'19: Proceedings of the Seventeenth International Conference on Artificial Intelligence and Law, 2019, http://dx.doi.org/10.1145/ 3322640.3326730.
- [5] S. Castano, M. Falduti, A. Ferrara, S. Montanelli, The LATO knowledge model for automated knowledge extraction and enrichment from court decisions corpora, in: COUrT@CAiSE, 2020.
- [6] M.C. Rodrigues, C. Bezerra, F. Freitas, I. Oliveira, Handling crimes of omission by reconciling a criminal core ontology with UFO, Appl. Ontol. 15 (1) (2020) 7-39.
- [7] [G. Boellaa, L. der Torre, Substantive and procedural norms in normative multiagent systems, J. Appl. Log. 6 (2008) 152-171.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb7)
- [8] [T. Bench-Capon, F. Coenen, Isomorphism and legal knowledge based systems, Artif. Intell. Law 1.1 (1992) 65-86.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb8)
- [9] [E. Francesconi, D. Tiscornia, Building semantic resources for legislative drafting: The DALOS project, in: Computable Models of the Law, vol. 4884. LNCS, Springer-Verlag Berlin, Heidelberg, 2008, pp. 56-70.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb9)
- [10] [I. Dove, Legal expert systems: The end of jurisprudence? J. Leg. Stud. Bus. 5 (1996).](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb10)
- [11] [A. Gardner, An Artificial Intelligence Approach to Legal Reasoning, vol. 4884. LNCS, MIT Press, 1987.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb11)
- [12] W. Hohfeld, Some fundamental legal conceptions as applied in judicial reasoning, Yale Law J. 23 (1) (1913) 16-59, http://dx.doi.org/10.2307/785533.
- [13] J. Breuker, A. Valente, R. Wikels, Legal ontologies in knowledge engineering and information management, Artif. Intell. Law 12 (2004) 241-277, http://dx.doi.org/10.1007/s10506-006-0002-1.
- [14] V.R. Benjamins, P. Casanovas, J. Breuker, A. Gangemi, Law and the Semantic Web: Legal Ontologies, Methodologies, Legal Information Retrieval and Applications, Springer, 2005.
- [15] L. Mommers, Application of a knowledge-based ontology of the legal domain in collaborative workspaces, in: Proceedings of the 9th International Conference on Artificial Intelligence and Law, 2003, pp. 70-76, http://dx.doi.org/10.1145/1047788.1047799.
- [16] [R. Falbo, SABiO: Systematic approach for building ontologies, in: Joint Workshop ONTO.COM / ODISE on Ontologies in Conceptual Modeling and Information Systems Engineering (Co-Located with 8th International Conference on Formal Ontology in Information Systems, FOIS 2014), 2014.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb16)
- [17] [G. Guizzardi, Ontological Foundations for Structural Conceptual Models (Ph.D. thesis), Telematica-Institut / CTIT, 2005.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb17)
- [18] [G. Guizzardi, A.B. Benevides, C.M. Fonseca, D. Porello, J.P.A. Almeida, T.P. Sales, UFO: Unified foundational ontology, Appl. Ontol. (2021).](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb18)
- [19] G. Guizzardi, B. A.B., C. Fonseca, J. Almeida, T. Sales, UFO: Unified foundational ontology, Appl. Ontol. (2022) 1-44, http://dx.doi.org/10.1016/j.datak. 2021.101891.
- [20] G. Guizzardi, C. Fonseca, A. Benevides, J. Almeida, D. Porello, T. Sales, Endurant types in ontology-driven conceptual modeling: Towards OntoUML 2.0, in: ER 2018, 2018, pp. 136-150.
- [21] C. Griffo, UFO-L, A Core Ontology of Legal Aspects Building Under the Perspective of Legal Relations (Ph.D. thesis), Federal University of Espirito Santo, 2018.

- [22] G. Guizzardi, N. Guarino, J. Almeida, Ontological considerations about the representation of events and endurants in business models, in: BPM 2016, vol. 9850, Springer, Cham, 2016, pp. 20-36.
- [23] [G. Guizzardi, G. Wagner, Towards an ontological foundation of discrete event simulation, in: Winter Simulation Conference, 2010, pp. 652-664.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb23)
- [24] [G. Guizzardi, G. Wagner, Using the unified foundational ontology (UFO) as a foundation for general conceptual modeling languages, in: Theory and Applications of Ontology: Computer Applications, 2010.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb24)
- [25] [G. Guizzardi, Towards ontological foundations for the conceptual modeling of events, in: ER 2013, vol. 8217, Springer, Heidelberg, 2013, pp. 327-341.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb25)
- [26] [G. Guizzardi, R. Falbo, R.S. Guizzardi, Grounding software domain ontologies in the unified foundational ontology (UFO): The case of the ode software process ontology, in: 1th Iberoamerican Workshop on Requirements Engineering and Software Environments, IDEAS'2008, 2008.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb26)
- [27] [A.B. Benevides, G. Guizzardi, B.F. BragaJoao, P.A. Almeida, Assessing modal aspects of ontouml conceptual models in alloy, in: ER 2009: Advances in Conceptual Modeling - Challenging Perspectives, 2009, pp. 55-64.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb27)
- [28] [R. Alexy, A Theory of Constitutional Rights, Oxford University Press, USA, 2009.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb28)
- [29] [C. Griffo, J. Almeida, G. Guizzardi, A pattern for the representation of legal relations in a legal core ontology, in: Proceedings of 29th International Conference on Legal Knowledge and Information Systems, JURIX, France, 2016.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb29)
- [30] [C. Griffo, J. Almeida, G. Guizzardi, Towards a legal core ontology based on alexy's theory of fundamental rights, in: ICAIL Multi-Lingual Workshop on AI and Law (MWAIL 2015), 15th International Conference on Artificial Intelligence and Law, ICAIL 2015, 2016.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb30)
- [31] C. Griffo, J. Almeida, G. Guizzardi, Conceptual modeling of legal relations, in: ER 2018: Conceptual Modeling, 2018, pp. 169-183, http://dx.doi.org/10. 1007/978-3-030-00847-5\_14.
- [32] C. Griffo, T. Sales, G. Guizzardi, J. Almeida, Legal power-subjection relations: Ontological analysis and modeling pattern, in: Conceptual Modeling: 41st International Conference, ER 2022, Hyderabad, India, vol. 13607, Springer, Cham, 2022, pp. 65-81, http://dx.doi.org/10.1007/978-3-031-17995-2\_5.
- [33] C. Griffo, J. Almeida, L. J.A.O., T. Sales, G. Guizzardi, Legal powers, subjections, disabilities, and immunities: Ontological analysis and modeling patterns, Data Knowl. Eng. 148 (2023) http://dx.doi.org/10.1016/j.datak.2023.102219.
- [34] [G. Guizzardi, On ontology, ontologies, conceptualizations, modeling languages and (meta)models, in: Proceedings of the 2007 Conference on Databases and Information Systems, 2007, pp. 18-39.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb34)
- [35] J. Mylopoulos, I. Jureta, F. S., An ontology for requirements, in: Advances in Conceptual Modeling - Foundations and Applications. ER 2007, vol. LNCS, 4802, Springer, Berlin, Heidelberg, 2007.
- [36] [A. Gangemi, M. Sagri, D. Tiscornia, A Constructive Framework for Legal Ontologies, vol. 3369, Springer, 2005, pp. 97-124.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb36)
- [37] [A. Gangemi, V. Presutti, Ontology Design Patterns, Springer, Heidelberg, 2009.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb37)
- [38] [A. Gangemi, Design patterns for legal ontology constructions, in: LOAIT, 2007.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb38)
- [39] G. Guizzardi, C. Fonseca, J. Almeida, T. Sales, A. Benevides, D. Porello, Types and taxonomic structures in conceptual modeling: a novel ontological theory and engineering support, Data Knowl. Eng. 134 (2021) http://dx.doi.org/10.1016/j.datak.2021.101891.
- [40] J. Almeida, G. Guizzardi, R. Falbo, T. Sales, gUFO: a lightweight implementation of the Unified Foundational Ontology (UFO). URL http://purl.org/nemo/ doc/gufo.
- [41] [S.W. Buell, L.K. Griffin, On the mental state of consciousness of wrongdoing, Law Contemp. Probl. 75 (2) (2012) 133-166.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb41)
- [42] [A. Kenny, Action, Emotion and Will, Routledge &amp; Kegan Paul, 1964.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb42)
- [43] [J. Jenkins, Motive and intention, Philos. Q. 15 (59) (1965) 155-164.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb43)
- [44] [G. Guizzardi, T.P. Sales, J.P.A. Almeida, G. Poels, Automated conceptual model clustering: a relator-centric approach, Softw. Syst. Model. (2021).](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb44)
- [45] [T. Gordon, G. Governatori, A. Rotolo, Rules and norms: Requirements for rule interchange languages in the legal domain, in: RuleML 2009: Rule Interchange and Applications, vol. 5858, LNCS, Springer, Berlin, Heidelberg, 2009, pp. 282-296.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb45)
- [46] [M. O'Connor, R. Shankar, C. Nyulas, A. Das, Developing a web-based application using OWL and SWRL, in: AAAI Spring Symposium, 2008.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb46)
- [47] A. Valente, J. Breuker, Ontologies, the missing link between legal theory and AI and law, in: Proceedings of Legal Knowledge Based Systems and Legal Theory, JURIX-94, 1994, pp. 66-75.
- [48] [R. Hoekstra, J. Breuker, M. Di Bello, A. Boer, LKIF core: Principled ontology development for the legal domain, in: Proceedings of the 2009 Conference on Law, Ontologies and the Semantic Web: Channelling the Legal Information Flood, vol. 188. Frontiers in Artificial Intelligence and Applications, IOS Press, 2009, pp. 21-52.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb48)
- [49] Legal theories and judicial decision-making: An ontological analysis, in: FOIS, 2020, pp. 63-76, http://dx.doi.org/10.3233/FAIA200661.
- [50] [J. Breuker, The construction and use of ontologies of criminal law in the e-court European project, Means Electron. Commun. (2003).](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb50)
- [51] [C. Asaro, M. Biasiotti, P. Guidotti, M. Papini, M. Sagri, D. Tiscornia, M. Court, Domain ontology: Italian crime ontology, in: In Workshop on Legal Ontologies &amp; Web Based Legal Information Management, ICAIL 2003, 2003.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb51)
- [52] [C. Rodrigues, R. Azevedo, F. Freitas, E. Palmeira, P. Barros, An ontological approach for simulating legal action in the Brazilian penal code, in: Proceedings of the 30th Annual ACM Symposium on Applied Computing, SAC'15, 2015, pp. 376-381.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb52)
- [53] C. Rodrigues, F. Freitas, R. Azevedo, An ontology for property crime based on events from UFO-b foundational ontology, in: 5th Brazilian Conference on Intelligent Systems, BRACIS, 2016, pp. 331-336, http://dx.doi.org/10.1109/BRACIS.2016.067.
- [54] [C. Rodrigues, F. Freitas, I. Oliveira, An ontological approach to the three-phase method of imposing penalties in the Brazilian criminal code, in: The 6th Brazilian Conference on Intelligent Systems, BRACIS, 2017.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb54)
- [55] [R. Kowalski, Predicate logic as a programming language, in: Proceedings of IFIP Congress 74, 1974, pp. 569-574.](http://refhub.elsevier.com/S0169-023X(25)00014-X/sb55)

[FIGURE]

Mirna El Ghosh is currently a Post-Doc researcher at INSERM, Paris, France. In 2011, she received a Master degree in Computer Science from the Lebanese University, Faculty of Sciences followed by a Master degree in Private Law (2017) from the Lebanese University, Faculty of Law. In 2018, she obtained her Ph.D. in Computer Science from Normandy University, France. Her domain of interests focuses mainly on Ontology Engineering, Ontology-driven conceptual modeling, Legal ontologies, Biomedical ontologies, Semantic similarity, Semantic interoperability, Rule-based reasoning.

## M. El Ghosh et al.

[FIGURE]

[FIGURE]

[FIGURE]

Hala NAJA is currently a Professor and Coordinator of the Master Degree in Software Engineering of the Department of Computer Science at Lebanese University. She received a Master Degree from Henri Poincaré University of Nancy in 1993. In 1997, she received a Ph.D. degree in Computer Science from Henri Poincaré University of Nancy. She has been teaching in Computer Science department at Lebanese University for 23 years. She has research collaboration with LINA Laboratory, Nantes-France and INSA Rouen. Her research interests focus on Agile methodologies and Multiview software architectures. In addition, she has also investigated in building legal ontologies and reasoning capability over legal based knowledge systems.

Habib Abdulrab is a professor of computer science and researcher in LITIS Laboratory, at INSA de Rouen, in Normandy university. He pursued higher studies in applied mathematics in France, obtaining a master's degree in Informatics from the University of Paris 6 in 1983, followed by a Ph.D. from the University of Rouen in 1987, and finally the Habilitation to supervise researches in 1992. Since 1992, he became a professor in the Mathematical and Software Engineering Department, at INSA de Rouen in Normandy university. He has published numerous scientific papers over the last three decades. His current interests are ontologies and reasoning.

Mohamad Khalil is currently professor, teacher and researcher at Lebanese University, faculty of engineering. He received the DEA in biomedical engineering from the University of Technology of Compiegne (UTC) in France in 1996. He received his Ph.D from the University of Technology of Troyes in France in 1999. He received his HDR (Habilitation a diriger des recherches) from UTC in 2006... He is the chair of ICABME international Conference and representative of IEEE EMBS in Middle Est and Africa since 2016. He has 100 international journals and he participated in 200 international conferences. His current interests are the signal and image processing problems: detection, classification, analysis, representation and modeling of non-stationary signals, with application to biomedical signals and images.
