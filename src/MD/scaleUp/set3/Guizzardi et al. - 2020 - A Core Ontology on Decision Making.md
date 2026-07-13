## A Core Ontology on Decision Making

Renata Guizzardi 1 , 2 , Bruno G. Carneiro 2 , Daniele Porello 3 , Giancarlo Guizzardi 2 , 4

1 Industrial Engineering and Business Information Systems University of Twente P.O. Box 217 7500 AE Enschede, The Netherlands

2 NEMO Conceptual Modeling &amp; Ontologies Research Group Federal University of Esp´ ırito Santo (UFES)

Av. Fernando Ferrari, 514, 29075-910, Vit´ oria, Brazil

3 ISTC-CNR Laboratory for Applied Ontology Via alla Cascata 56C 38123 Povo (TN), Italy

4 Conceptual and Cognitive Modeling Research Group (CORE) University of Bozen-Bolzano Piazza Domenicani, 3, 39100, Bolzano, Italy

r.guizzardi@utwente.nl, guimaraescarneiro@gmail.com

daniele.porello@loa.istc.cnr.it, giancarlo.guizzardi@unibz.it

Abstract. Decision Making is an important part of the everyday lives of individuals and organizations. Many works within Computer Science have focused on supporting this process, especially by developing decision-supporting systems. We argue that for providing better support to Decision Making, it is paramount to understand the nature of a decision and of the process that leads to it. To accomplish that, in this paper, we go forward with our preliminary work in proposing a core ontology on Decision Making. Aiming at creating a wellfounded ontology, we rely on the Unified Foundational Ontology (UFO), and we reuse some notions of existing ontologies on Value Proposition and Economic Preference. Besides describing the ontology, this work discusses some possible applications and compare our ontology with related works.

## 1. Introduction

Decision Theory (cf. [Peterson 2017]) is an interdisciplinary topic that has been investigated by economists, biologists, cognitive and social scientists, philosophers, computer scientists, and others. Making decisions as well as reporting on them to others are part of the human nature, as illustrated in this quote: 'Darwinian considerations suggest that language may have developed because it leads to improved decision making and survival' [Losee 2001]. The importance on supporting and documenting decision making goes beyond the needs of the individual, being also crucial to organizations and society as a whole.

In Computer Science, the study of Decision Making is highly focused on building Decision Support Systems (DSS). According to the purpose for which the natural language is used, proposals can be classified into two groups. One group applies natural language before the decision is taken in order to assist the decision-making process itself [Demner-Fushman et al. 2009], [Gkatzia et al. 2016] and [Mart´ ınez et al. 2015]. The other group relies on natural language to explain the decision making process after the decision is taken [Goodall 2014] and [Papamichail and French 2003].

We argue that for providing better support to Decision Making, it is paramount to understand, first of all, the nature of Decisions and of the Decision Making process. And to accomplish that, we propose an ontological analysis of the notion of Decision and its related concepts, with the creation of a core ontology on Decision Making. In fact, a first version of such ontology has been proposed in [Guizzardi et al. 2018b]. This previous work is based on the Unified Foundational Ontology (UFO) [Guizzardi 2005, Guizzardi et al. 2015, Guizzardi et al. 2008], profiting from the conceptualization and axiomatization already present in UFO. In this paper, we go on with this effort, by taking into consideration the latest developments of UFO related ontologies, which can shed light into corners of the Decision Making process not yet explored. In particular, we base our analysis in the ontology of Value Proposition [Sales et al. 2017] and on the ontological analysis of Economic Preference [Porello and Guizzardi 2018][Porello et al. 2020].

An important aspect of this work is that the proposed analysis has an important impact on the previously analyzed concepts, at times changing the understanding of their ontological nature.

The core ontology on Decision Making resulting from our analysis has several applications. As core ontology, we mean that although it represents a domain of discourse (i.e., the Decision Making domain), this ontology may be specialized in more specific domains [Falbo et al. 2013], for instance, Health Care Decision Making or Financial Decision Making. To illustrate its potential, we here present an example of its use for decision documentation, in a way that previous decisions may inform the decision maker herself and others with whom she collaborates. This way, new decisions may be taken in a more justified and consistent manner. This is particularly useful in organizational settings, where personnel turnover and external collaboration also opens up the possibility of using documented decisions as an important source of knowledge to train newcomers.

The remaining of this work is organized as follows: section 2 describes some background works that are relevant to enable the understanding of our proposal; section 3 describes our proposed ontology; section 4 illustrates the use of the proposed ontology; section 5 presents some related works; and finally, section 6 concludes this paper.

## 2. Background

## 2.1. Decision Theory

Decision Making can be understood as the act of choosing an alternative in a set of possible alternatives [Peterson 2017, Okike and Amoo 2014] or as a broader process perspective composed of different phases, such as problem definition , alternative discovery , alternative selection and decision evaluation [Frisk et al. 2014].

Important challenges in this scenario are the complexity and uncertainty of the decision situation or the existence of multiple conflicting objectives [Mart´ ınez et al. 2015]. This work is founded in some fundamental assumptions about the decision maker. Many works assume that the decision maker is an economic man [Kreps 1988], i.e. a man that is (1) completely informed, (2) infinitely sensitive, (3) rational, and (4) able to order situations by some criterion that should be maximized. However, this is a perspective that exceeds actual human cognitive capabilities, cf. [Fjellman 1976].

We are interested in how people actually make decisions. It is trivial to show that a real person has no total knowledge of her context and the different end states into which she can reach as result of her actions. Therefore, economic man's properties (1) and (2) are discarded. We here assume that properties (3) and (4) are still maintained. Concerning (3), we highlight that being rational does not mean not having emotions, but being able to reason over premises founded on emotions and values. Finally, we consider that alternative outcome situations can be ordered based on its values according to the decision maker's beliefs.

## 2.2. Background Ontological Concepts: Intentionality, Value and Preference

We start by defining the basic UFO concepts that are then specialized into Decision Making concepts. For a fuller presentation on UFO, one should refer to [Guizzardi 2005, Guizzardi et al. 2008, Guizzardi et al. 2015]. SUBSTANTIAL can be classified into OBJECTS and AGENTS. An AGENT is a SUBSTANTIAL bearing a special kind of MOMENT that connects the AGENT to external SITUATIONS (i.e., to parts of reality or states of affairs). This kind of MOMENT is named MENTAL MOMENT and can be specialized into BELIEF, DESIRE and INTENTION. BELIEF refers to the world as the AGENT conceives it; DESIRE refers to the world as the AGENT would like it to be; and INTENTION is the world as the AGENT commits to bringing about by executing ACTIONS. An ACTION is an EVENT holding an intentional participation of an AGENT [Guizzardi et al. 2008].

Reviewing the UFO concept of INTENTION and its relation to ACTIONS is very important for understanding the Decision Making process. After all, when a person is prompted to make a decision, her main driver is her goals , which select what state of the world she commits 1 to bringing about. All MENTAL MOMENTS have a PROPOSITIONAL CONTENT; a GOAL is the propositional content of an INTENTION. If successful, an ACTION manifesting that INTENTION brings about a SITUATION that satisfies that INTENTION. We can then define a SUCCESSFUL ACTION as one that creates a SITUATION that satisfies the INTENTION manifested in that ACTION. Analogously, we can define a FULFILLED INTENTION, as one that is deliberately produced by that SUCCESSFUL ACTION 2 . Figure 1 depicts an OntoUML 3 diagram including these concepts.

1 In fact, an INTENTION is sometimes referred to as an agent's internal commitment [Guizzardi et al. 2008]

2 In this paper, we describe constraints, derivations and definitions of this ontology using natural language statements only. Moreover, we present throughout the text only on a subset of these. A full formalization of this ontology will be the subject of an extended version of this article.

3 OntoUML [Guizzardi 2005, Almeida et al. 2019, Guizzardi et al. 2018a, Fonseca et al. 2019] is an ontology-driven conceptual modeling language based on the foundational ontology UFO. Core ontologies based on UFO are frequently presented as OntoUML modules [Guizzardi et al. 2015].

Figure 1. Action, Situation and Intention

[FIGURE]

Value is a heavily overloaded concept. The notion adopted here is based on the Ontology of Value Propositions [Sales et al. 2017], which is also grounded on UFO. According to that ontology, an agent termed VALUE BEHOLDER ascribes VALUE to VALUE OBJECTS or VALUE EXPERIENCES, the latter being past, present or future experiences of an agent (i.e., kinds of mental simulations, or mental models in the sense of [Frigg 2010]). Hence, VALUE OBJECT and VALUE EXPERIENCE are two types of VALUE BEARERS. The AGENT makes VALUE ASCRIPTIONS (i.e., assesses a VALUE BEARER) to assign it with VALUE.

A subsequent work that reuses the notion of value is the work of [Porello and Guizzardi 2018, Porello et al. 2020] on Economic Preference . These authors define the PREFERENCE of an AGENT by comparing the VALUE that the VALUE BEHOLDER assigns to two VALUE BEARERS. The preferred bearer is then called the PREFERRED VALUE BEARER, while the other is known as DEPRECATED VALUE BEARER.

Due to space limitations, the relevant concepts in both these works will be explained in the next section (refer to figure 3). Notwithstanding, we emphasize that we inherit from these works the principles that value is goal dependent , context dependent , uncertain , and subjective .

## 3. Core Ontology on Decision Making

Let us start by considering that an AGENT is in a given SITUATION, i.e., her actual state of affairs. Suppose that SITUATION is such that it does not satisfy that agent's INTENTIONS (GOALS). The AGENT is then desiring a different SITUATION. Given her PREFERENCES and resources (including capacities 4 ), that agent can decide to self-commit to a particular way of pursing those GOALS, i.e., by deliberately assessing her options to form a new INTENTION. In terms of our ontology (see Figure 2), we have that due to a certain (motivating) INTENTION, an AGENT performs a DELIBERATION, which, in turn, creates a new INTENTION termed a DECISION. In other words, a DECISION is an INTENTION created by a DELIBERATION. As an INTENTION, that DECISION can eventually manifest in the performing of another ACTION termed a DECISION RESULTING ACTION, whose result is termed a CONSEQUENCE. Once more, if that is a SUCCESSFUL ACTION, a CONSEQUENCE satisfies the PROPOSITIONAL CONTENT (GOAL) of the original DECISION 5 .

4 In a future work, we shall formally explore the influence of internal and social capacities (acquired through delegation relations ) [Guizzardi and Guizzardi 2010] in the decision-making process.

Figure 2. Deliberation and Decision

[FIGURE]

Here we point out the first change we made when revisiting the Decision Making Ontology. In the previous version [Guizzardi et al. 2018b], we considered that a DECISION could be either a BELIEF or an INTENTION. An example of the former is the decision that one prefers comedy over drama, while the latter may be illustrated by actually choosing to watch a comedy instead of a drama (i.e., it involves a particular intention and an action to satisfy it). However, in light of the new conceptualization of PREFERENCE (which we shall see in what follows), we now see the former as a PREFERENCE BELIEF. And indeed, this choice makes the ontology more compliant with the literature on Decision Theory, which often relates decision with the action that follows it [Peterson 2017].

Weemphasize that a DECISION is thus associated to two ACTIONS, one that creates it, i.e., the DELIBERATION and one that is the decision's result, namely the DECISION RESULTING ACTION (see Figure 2). Note also the relationships between the decision and each of these actions have different natures, being a creation [Almeida et al. 2019] w.r.t the former and a manifestation [Guizzardi et al. 2016] w.r.t to the latter.

One of the interesting aspect of the proposed ontology is reflecting on the consequences of a decision. The DECISION RESULTING ACTION brings about a SITUATION termed CONSEQUENCE (in other words, CONSEQUENCE is a SITUATION role when such SITUATION is brought about by a DECISION RESULTING ACTION. By analyzing the decision's CONSEQUENCE, the AGENT develops other MENTAL MOMENTS (i.e. BELIEFS, DESIRES and INTENTIONS) that will then influence his future DECISIONS. Comparing this work with the previous ontology version, both CONSEQUENCE and DECISION SUPPORTING ACTION are new concepts that help in the cycle of assessing the result of the decision before taking the next one.

5 In that case, such consequence also helps (or makes ) [Dalpiaz et al. 2016, Guizzardi et al. 2013] the GOAL of the original INTENTION (manifested in the DELIBERATION. This formal connection is something we shall explore in an extension of this work.

At this point, we would like to explore how the concepts of VALUE and PREFERENCE (explained in section 2.2) may be integrated to the notions related to Decision Making. Figure 3 depicts the relation between of DELIBERATION and these concepts.

Figure 3. Deliberation, Value and Preference

[FIGURE]

In order to explain how the concepts in Figure 3 are related, let us reflect on the Decision Making Process. When prompted to make a decision, the AGENT first makes an assessment of her possibilities. To do that, the AGENT starts simulating possible scenarios, e.g., imagining herself in imaginary experiences, in which she interacts with other AGENTS and OBJECTS, is in a different place, etc. This is what Sales et al. [Sales et al. 2017] call VALUE EXPERIENCE.

Consider a SITUATION in which an AGENT must decide between two alternatives. When an AGENT decides something (i.e., performs a DELIBERATION), she takes into consideration her own PREFERENCES regarding two possible VALUE BEARERS (either a VALUE OBJECT or a VALUE EXPERIENCE). So, in a sense, DELIBERATION is also a manifestation of that agent's PREFERENCES over two VALUE BEARERS. In other words, the VALUE BEHOLDER participating in a DELIBERATION is exactly the bearer of the PREFERENCE mode manifested in that DELIBERATION.

A PREFERENCE is the truthmaker [Fonseca et al. 2019] of the ternary has preference relation, the latter connecting a PREFERRED BEARER and the non-preferred bearer (termed DEPRECATED BEARER). PREFERENCE is thus a COMPLEX MODE, which aggregates two VALUE ASCRIPTIONS, each one associated to one of the VALUE BEAR- ERS. A VALUE ASCRIPTION is itself a COMPLEX MODE 6 associated to a VALUATION event (not shown in the model), performed by the AGENT when assessing or ascribing value to the VALUE BEARER. According to [Porello and Guizzardi 2018], this binary case may be extrapolated to include other VALUE BEARERS, each one associated to its own value. Here, VALUE itself is an emerging quality inhering in a VALUE ASCRIPTION that takes a magnitude in a given conceptual space (termed a VALUE MAGNITUDE SPACE [Porello and Guizzardi 2018] and not shown in the picture 7 ).

Each VALUE ASCRIPTION is composed of several smaller 'comparisons' (or 'judgements'), named VALUE ASCRIPTION (VA) COMPONENTS, which aggregate an INTENTION and INTRINSIC MOMENTS that are taken into consideration by the AGENT when ascribing VALUE to a VALUE BEARER. Each VA COMPONENT is in its turn associated to VALUE COMPONENTS, defined as QUALITIES (i.e., BENEFITS or SACRIFICES) the AGENT finds relevant for each of the VA COMPONENT.

Here we point out another important change regarding the previous version of the Decision Making Ontology. Previously, we considered CRITERION a (role of) a MENTAL MOMENT (analogous to a DECISION), i.e., either a BELIEF or an INTENTION considered by the AGENT when performing a DELIBERATION. However, we find that the INTRINSIC MOMENT TYPE whose instances constitute the VA COMPONENTS better captures what a CRITERION is. Indeed, when one refers to a CRITERION, it is often a QUALITY TYPE (e.g. price, efficiency etc.) or a MODE TYPE (e.g., the existence of the functionality provided by an automatic gearbox, in case you are buying a car) .

Finally, extending the original work of [Sales et al. 2018], we assume here that different INTENTIONS have different levels of importance to their bearing AGENT. Although not explicitly representing here this intention absolute importance (a quality inhering in an INTENTION), we represent that a comparative relation emerges ordering intentions, i.e., establishing their relative priority. We claim that the priority of a given intention can also influence the emerging VALUE associated to the final VALUE ASCRIPTION made by that agent of a given VALUE BEARER. In other words, in ascribing VALUE, an AGENT considers not only the degree to which the INTRINSIC MOMENTS of the VALUE BEARER contributes to the satisfaction of given GOAL but also the importance (priority) of that GOAL. From the importance of intentions, we can also derive an importance of MOMENTS and their types (i.e., CRITERION) in the decision making process: the importance of a CRITERION can be derived from the degree to which its instances contributes to a given INTENTION and the importance (priority) of that INTENTION. We consider these aspects here because they play an important role in the rationale of decisions as shown in the sequel.

To help the reader understand the concepts we have just analyzed, it is important to consider a concrete example, as shown in Figure 4.

6 While originally conceived as a RELATOR [Sales et al. 2017], VALUE ASCRIPTION was then revised as a externally dependent COMPLEX MODE in [Porello et al. 2020]. This is because when one ascribes value to a VALUE BEARER, the latter does not necessarily acquire new genuine relational properties. The VALUE ASCRIPTION itself, nonetheless, remains externally dependent on that VALUE BEARER.

7 A VALUE BEARER is preferred in a has preference relation iff the value magnitude of its VALUE ASCRIPTION bearer is greater than the one of the compared alternative.

Figure 4. Illustrating how a decision is taken based on a preference

[FIGURE]

Suppose that someone named Fred is bored and wants to be entertained by watching a film. And he must decide between watching a film on Netflix or watching a film on YouTube . Thus he starts valuating these two alternatives (VALUE EXPERIENCES). Consider that for each of these VALUE EXPERIENCES, he then splits the VALUE ASCRIPTION in two components: one concerning his will of being entertained and a second one regarding how much the service costs. Figure 4 8 shows these VA COMPONENTS, along with the QUALITIES and INTENTIONS that compose them. We use salmon sticky notes to represent data values attributed to the corresponding qualities, so as to allow the comparison of the two options. For instance, Fred valued Netflix entertainability as high, as the film is uninterrupted, while YouTube entertainability is valued medium, considering that the movie is often interrupted with commercials. On the other hand, the price of Netflix monthly fee is $12,99 while YouTube has no direct cost. Figure 4 also shows the BENEFITS and SACRIFICES inhering in each of these VA Components, for instance, the cost SACRIFICE when signing up Netflix and the no cost BENEFIT of using YouTube . Note that since the criteria are the quality types that instantiate the qualities composing the V A Components, the criteria applied by Fred to make his DECISION are cost and entertainability . Finally, Figure 4 shows that Fred prioritized price over entertainability , as YouTube is shown as the PREFERRED BEARER while Netflix is pictured as the DEPRECATED ONE. Ultimately, based on his this PREFERENCE, Fred performs the deciding between film providers DELIBERATION, which leads to the creation of the watch films on YouTube decision . And finally, Fred performs the to watch films on YouTube DECISION RESULTING ACTION.

8 We here abuse the UML notation for the sake of clarity (e.g., using type-level diamond relations for representing instance-level parthood) as this model is meant to be interpreted as a UML instance diagram. So, rectangles represent instances of the corresponding classes and relations represent links, i.e., instancelevel relationships. To facilitate the understanding, we here use for individuals, the same colors applied in the previous figures for the corresponding types.

## 4. Applications

The proposed core ontology makes explicit what is involved in Decision Making. Thus, it is able to account for the rationale behind a decision. In other words, by relying on such ontology, one is able to determine what are the alternatives (value bearers), how they were valued, what are the applied criteria, who is capable of executing the action resulting from the decision, and so on. One of the direct applications of the proposed ontology is to support the documentation of decisions. For that, a template may be created, whose slots come directly from the ontological concepts. These slots should be filled with expressions in natural language that better represent the instances of the concepts.

To illustrate this example, we consider the Netflix/YouTube example explained in section 3. A template documenting this case is illustrated in Table 1.

Table 1. Template for Decision Documentation based on the Proposed Ontology

| Motivating intention   | Being relaxed by watching a movie either on Netflix or YouTube   | Being relaxed by watching a movie either on Netflix or YouTube   |                 |
|------------------------|------------------------------------------------------------------|------------------------------------------------------------------|-----------------|
| Intention              | Alternative                                                      | Criterion and its instantiated Value                             | Value Component |
| Minimize Cost          | Watching film on Netflix                                         | Cost = 12,99                                                     | Sacrifice       |
| Minimize Cost          | Watching film on YouTube                                         | Cost = 0                                                         | Benefit         |
| Maximize Relaxation    | Watching film on Netflix                                         | Entertainability =High                                           | Benefit         |
| Maximize Relaxation    | Watching film on YouTube                                         | Entertainability = Medium                                        | Benefit         |
| Decision               | Watch film on YouTube                                            |                                                                  |                 |

The template of Table 1 states the user's motivating intention, i.e. Being relaxed by watching a movie either on Netflix or YouTube . Then, the template exhibits the user's intentions ordered according to the priority defined by the user. In this case, Fred prioritized his intention of minimizing the cost over his intention of seeking relaxation (i.e. Maximize Relaxation, in the table). For each intention, the alternatives (value bearers) are analyzed by considering each criteria. In this case, Watching film on Netflix and Watching film on YouTube are analyzed first w.r.t cost and then w.r.t entertainability . Moreover, the value component ( sacrifice/benefit ) is indicated for each alternative. Finally, the decision is stated in the last line of the template. In this case, the decision was Watch film on YouTube .

Documented decisions may be used by the decision-maker herself to justify and inform her future decisions. Moreover, when considering an organizational environment, documenting and further reusing the documented decisions may be an adopted practice to make sure that the organizational members act consistently, to guarantee the quality of the Decision Making process and to train newcomers joining the work.

Another interesting application for the proposed ontology is designing value propositions based on the explicit rationale of past decisions. Consider that a base of pre-recorded decisions exist for customers of a particular service. The service provider is then able to consult such base to determine what are the alternatives favored by most customers, what are their intentions as well as their priority over intention types, the criteria they apply, etc. In other words, on what grounds the economic preferences of existing agents, and how these are reflected in actual past decisions.

Finally, we cite the possibility of using the proposed ontology to grant a decision supporting system with the possibility to explain its own Decision Making process. Explainability has been cited as an important principle to be accounted for Artificial Intelligent systems to enable trustworthiness [High-Level Expert Group on Artificial Intelligence 2018]. This may be achieved if the system is able to reason over their own Decision Making process and for this, it needs to have an explicit model, such as the proposed ontology.

## 5. Related Work

An interesting related work is the GRADE taxonomy [Papatheocharous et al. 2018], created to establish the vocabulary for supporting decisions regarding architectural aspects of software-intensive systems. The main categories of this taxonomy are Goals, Roles, Assets, Decision and Environment. Each of these categories classifies more refined concepts. The taxonomy has been created to support decision documentation and assessment. Compared to an ontology, the taxonomy is less structured and does not actually aim at defining the semantics of the terms, as in our work. Moreover, it is not as general as our model, focusing specifically in the domain of software architectures.

The Strategic Decision Making (SDM) Ontology [G´ omez et al. 2017]has been created with special focus in managing quality in Agile Software Development processes, although the authors claim it is general enough to be used in other contexts. The SDM Ontology has been developed to enable uniform communication about its domain and to support decisions of the software development process of a specific project named QRapids. The Decision Making Ontology (DMO) [Kornyshova and Deneckere 2012] has been developed aiming at: clarifying the concepts of the domain of Decision Making, also supporting the specification of Decision Making requirements; and serving as basis of a specification of the components a DM method. To be more specific, it is part of an approach called MAke Decisions in Information Systems Engineering (MADISE). Both the SDMOntology and DMO are developed with the support of UML. Some of their concepts coincide with notions of our proposed ontology, such as decision , decision maker , action , criterion and preference . However, these ontologies do not consider how the process of ascribing value determines preference , thus influencing the Decision-Making process. We believe that this is a drawback of these works when compared to ours. Additionally, such ontologies miss the important grounding that a foundational ontology provides, helping to maintain the consistency and coherence of the ontology under development.

## 6. Final Considerations

In this paper, we describe our ongoing efforts in creating a core ontology on Decision Making. This ontology is based on existing works, i.e., it builds over a previous version of a Decision Making ontology [Guizzardi et al. 2018b], besides reusing concepts of the Value Proposition ontology [Sales et al. 2017] and the ontological analysis of Economic Preference [Porello and Guizzardi 2018].

Many authors have proposed a Decision Making process and here we select the one by [Bohanec 2009] for its completeness and coherence. According to [Bohanec 2009], the Decision Making process is composed of the following activities:

1. identification of the decision problem;
2. collecting and verifying relevant information;
3. identifying decision alternatives;
4. anticipating the consequences of decisions;
5. making the decision;
6. informing concerned people and public of the decision and rationale;
7. implementing the selected alternative;
8. evaluating the consequences of the decision.

Except for activities 2 and 6, all other aforementioned activities are covered by the proposed ontology. For instance, 1 identification of the decision problem happens when the agent identifies the goals she wants to achieve; then 3 identifying decision alternatives and 4 anticipating the consequences of selecting one of these alternatives require identifying and analyzing value experiences; moreover, 5 making the decision is a process of ascribing value to each value experience and determining the preference regarding the alternatives, based on such values; next, activity 7 implementing the selected alternative is achieved by executing the decision resulting action; finally, 8 evaluating the consequences of the decision requires analyzing the situation which is brought about by the action executed in activity 7. Executing this activity, in turn, leads to the creation of new beliefs and intentions.

Future works include performing a full-fledged evaluation of the proposed ontology, by comparing it with others. Another direction is using the proposed ontology to develop a tool to enable decision documentation. Moreover, we hope to evolve the ontology in some directions, for example, understanding further how intentions are prioritized.

## References

- Almeida, J. P. A., Falbo, R. A., and Guizzardi, G. (2019). Events as entities in ontologydriven conceptual modeling. In 38th International Conference on Conceptual Modeling , pages 469-483.
- Bohanec, M. (2009). Decision making: A computer-science and information-technology viewpoint. Interdisciplinary Description of Complex Systems , 7(2):22-37.
- Dalpiaz, F., Franch, X., and Horkoff, J. (2016). istar 2.0 language guide. arXiv preprint arXiv:1605.07767 .
- Demner-Fushman, D., Chapman, W. W., and McDonald, C. J. (2009). What can natural language processing do for clinical decision support? Journal of biomedical informatics , 42(5):760-772.
- Falbo, R., Barcellos, M., Nardi, J., and Guizzardi, G. (2013). Organizing ontology design patterns as ontology pattern languages. In The Semantic Web: Semantics and Big Data. ESWC 2013 , pages 61-75.
- Fjellman, S. M. (1976). Natural and unnatural decision-making: a critique of decision theory. Ethos , 4(1):73-94.
- Fonseca, C. M., Porello, D., Guizzardi, G., Almeida, J. P. A., and Guarino, N. (2019). Relations in ontology-driven conceptual modeling. In 38th International Conference on Conceptual Modeling , pages 28-42.
- Frigg, R. (2010). Models and fiction. Synthese , 172(2):251.
- Frisk, J. E., Lindgren, R., and Mathiassen, L. (2014). Design matters for decision makers: Discovering it investment alternatives. European Journal of Information Systems , 23(4):442-461.
- Gkatzia, D., Lemon, O., and Rieser, V. (2016). Natural language generation enhances human decision-making with uncertain information. arXiv preprint arXiv:1606.03254 .
- Goodall, N. J. (2014). Ethical decision making during automated vehicle crashes. Transportation Research Record , 2424(1):58-65.
- Guizzardi, G. (2005). Ontological foundations for structural conceptual models . PhD thesis, University of Twente.
- Guizzardi, G., de Almeida Falbo, R., and Guizzardi, R. S. (2008). Grounding software domain ontologies in the unified foundational ontology (ufo): The case of the ode software process ontology. In The 10th Iberoamerican Workshop on Requirements Engineering and Software Environments , pages 127-140.
- Guizzardi, G., Fonseca, C. M., Benevides, A. B., Almeida, J. P. A., Porello, D., and Sales, T. P. (2018a). Endurant types in ontology-driven conceptual modeling: Towards ontouml 2.0. In International Conference on Conceptual Modeling , pages 136-150.
- Guizzardi, G., Guarino, N., and Almeida, J. P. A. (2016). Ontological considerations about the representation of events and endurants in business models. In International Conference on Business Process Management , pages 20-36. Springer.
- Guizzardi, G., Wagner, G., Almeida, J. P. A., and Guizzardi, R. S. (2015). Towards ontological foundations for conceptual modeling: The unified foundational ontology (ufo) story. Applied ontology , 10(3-4):259-271.
- Guizzardi, R. and Guizzardi, G. (2010). Ontology-based transformation framework from tropos to AORML. In Yu, E., Giorgini, P., Maiden, N., and Mylopoulos, J., editors, Social Modeling for Requirements Engineering , Cooperative information systems, pages 547-570. MIT Press.
- Guizzardi, R., Perini, A., and Susi, A. (2018b). Aligning goal and decision modeling. In International Conference on Advanced Information Systems Engineering , pages 124132.
- Guizzardi, R. S., Franch, X., Guizzardi, G., and Wieringa, R. (2013). Ontological distinctions between means-end and contribution links in the i* framework. In International Conference on Conceptual Modeling , pages 463-470. Springer.
- G´ omez, C., Ayala, C., Franch, X., L´ opez, L., Behutiye, W., and Mart´ ınez-Fern´ andez, S. (2017). Towards an ontology for strategic decision making: The case of quality in rapid software development projects. In Advances in Conceptual Modeling: ER 2017 , pages 111-121.
- High-Level Expert Group on Artificial Intelligence, E. C. (2018). Draft ethics guidelines for trustworthy ai, draft document.
- Kornyshova, E. and Deneckere, R. (2012). Using an ontology for modeling decisionmaking knowledge. In 16th International Conference on Knowledge-Based and Intelligent Information Engineering Systems .
- Kreps, D. (1988). Notes on the Theory of Choice . Westview press.
- Losee, R. M. (2001). Natural language processing in support of decision-making: phrases and part-of-speech tagging. Information processing &amp; management , 37(6):769-787.
- Mart´ ınez, L., Rodriguez, R. M., and Herrera, F. (2015). Linguistic decision making and computing with words. In The 2-tuple Linguistic Model , pages 1-21.
- Okike, E. U. and Amoo, O. A. (2014). Problem solving and decision making: Consideration of individual differences in computer programming skills using myers briggs type indicator (mbti) and chidamber and kemerer java metrics (ckjm). Journal of Applied Information Science and Technology , 7(1):27-34.
- Papamichail, K. N. and French, S. (2003). Explaining and justifying the advice of a decision support system: a natural language generation approach. Expert Systems with Applications , 24(1):35-48.
- Papatheocharous, E., Wnuk, K., Petersen, K., Sentilles, S., A., C., Gorschek, T., and Shahb, S. (2018). The grade taxonomy for supporting decision-making of asset selection in software-intensive system development. Information and Software Technology , 100:1-17.
- Peterson, M. (2017). An introduction to decision theory . Cambridge University Press.
- Porello, D. and Guizzardi, G. (2018). Towards an ontological modeling of preference relations. In 17th International Conference of the Italian Association for Artificial Intelligence , pages 152-165.
- Porello, D., Guizzardi, G., Sales, T., and Amaral, G. (2020). A core ontology for economic exchanges. In 39th International Conference on Conceptual Modeling .
- Sales, T., Guarino, N., Guizzardi, G., and Mylopoulos, J. (2017). An ontological analysis of value propositions. In 21st IEEE Enterprise Computing Conference , pages 184-193.
- Sales, T. P., Bai˜ ao, F., Guizzardi, G., Almeida, J. P. A., Guarino, N., and Mylopoulos, J. (2018). The common ontology of value and risk. In International Conference on Conceptual Modeling , pages 121-135.
