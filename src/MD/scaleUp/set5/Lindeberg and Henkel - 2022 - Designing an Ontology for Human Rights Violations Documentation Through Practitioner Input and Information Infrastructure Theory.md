[FIGURE]

## Designing an Ontology for Human Rights Violations Documentation Through Practitioner Input and Information Infrastructure Theory

[FIGURE]

J¨ oran Lindeberg ( B ) and Martin Henkel

[FIGURE]

Department of Computer and System Sciences, Stockholm University, Stockholm, Sweden { joran,martinh } @dsv.su.se

Abstract. Human rights groups of varying sizes collect information about human rights violations. Managing this information in a structured way is a challenging task, particularly since many human rights groups have limited budgets. This paper presents the initial work with requirements elicitation leading to the design of OntoRights - a domain ontology for human rights violations documentation that aims at helping human rights organisations to structure their documentation. To ensure that the ontology was grounded in practice, two interconnected surveys of manuals and practitioners were conducted. Moreover, the design used information infrastructure theory to increase the ontology's potential uptake. The resulting ontology extends the legal core ontology UFO-L and is represented in OntoUML. As a demonstration, it was instantiated twice: in a fictitious and in a real case.

Keywords: Ontology-driven conceptual modeling · Human rights · Requirements elicitations · Information infrastructures · Unified Foundational Ontology (UFO) · OntoUML · OntoRights

## 1 Introduction

Around the world, human rights groups of varying sizes collect information about human rights violations to bring justice to the victims and prevent future aggression. The collected information is stored in repositories of very different types: from paper notebooks to advanced databases. This practice is referred to as human rights violations documentation. While some cases only contain a single piece of information, others constitute a complex puzzle of people, sources, timelines, legal analysis, and connections with other cases.

Managing this information is a challenging task, particularly since many human rights groups work on a shoestring budget [22] and in high-pressure environments [30]. At some point, many of the groups must make the leap from text documents and spreadsheets to a structured database. Others already have a database but want to improve it. While the costs of these technologies are falling [22], developing database models according to each organisation's needs remains a challenge.

Depending on their area of interest and other factors, different organisations need different data models [5]. Human rights violations occur in a complex social reality and human rights groups are heterogeneous. Some organisations might be very interested in the properties of the people involved (such as gender or ethnicity), others are monitoring violations by a certain actor (such as 'police watch' initiatives). Some are collecting evidence that must be strong enough for a criminal court case. Others need to analyse organisational structures to show a chain of command. However, human rights groups also share a common system defined by international human rights law and use variants of the same principles for human rights violations documentation.

One approach for improved data modelling skills in human rights groups has been capacity-building initiatives [4]. A complementary solution is to focus on the creation of ontologies for this domain. Ontologies provide an abstract and shared data model, above the implementation of a concrete data system [12]. An ontology contains much embedded knowledge and patterns that can support a group's design of a data model.

However, after an extensive web search, search in academic databases, and communication with human rights professionals, no adequate ontology for human rights violations appears to exist. In this paper, we report on the initial work with the design of OntoRights: a domain ontology for human rights violations documentation. The primary goal of the work was to design OntoRights so that it supports human rights groups that are designing case databases of human rights violations. We base the design on interviews, a document survey, and a survey among practitioners in the field. The design is also grounded in a case study. Moreover, we utilise the information infrastructures (IIs) theory by Hanseth &amp; Lyytinen [15] to guide the design. The full ontology is available online, in this paper we focus on the design process and the outcome in terms of requirements.

The structure of this paper is as follows: Section 2 introduces the domain and previous relevant ontology research. Section 3 introduces the applied overall research framework and design theory. Section 4 is about requirements elicitation. Section 5 presents the OntoRights ontology. Section 6 discusses the process and results, and Sect. 7 concludes.

## 2 Theoretical Background

## 2.1 The Human Rights Protection System and Technologies

The human rights system is ruled by international law [29]. A human rights violation is an incident or situation that violates an individual's or group's human rights. Human rights violations can be committed through commission (activity) or omission (passivity). Even if a concrete act is perpetrated without the collusion of state agents, the state could in some cases still be held responsible if it has been unwilling to take measures to avoid the act. In other words, an act in the physical world may have institutional, i.e. legal, implications.

Like other fields, human rights work has adapted to technological development, e.g. by increasingly using computational analysis [30]. However, the journey has been slow. The general lack of resources for human rights practice has caused technologies to seldom be developed specifically for this field.

Today's abundance of social media content, videos and remote sensors is useful for human rights monitoring [30], but also contributes to information overload. Hence, in the words of Guberek and Silva [13, p. 13], 'the quantity of data available requires careful organisation and preservation to enable its use in long-term struggles for truth and justice'. However, the reviewed literature [22,30,31] conveys the impression that the human rights technology field has given more priority to extracting information than structuring it.

## 2.2 Previous Relevant Ontology Research

Ontologies can represent different levels of generality. Drawing from Nguyen [27] and Griffo et al. [11], the most important types for the purpose of this paper are, in descending order of generality: foundational ontologies (top-level), core ontologies (mid-level), and domain ontologies. A domain ontology should preferably extend a core or foundational ontology. One reason is reusing thoroughly designed patterns, which facilitates logical coherence [18].

As discussed, no ontology appears to have been designed before for the domain of human rights violations documentation. OntoRights can be compared with, on the one hand, existing legal ontologies, and on the other hand, existing available data models. Legal ontologies such as LKIF Core [18] and UFO-L [10] can express the legal aspects of human rights problems. The underlying legal theory of UFO-L - Robert Alexy's Theory of Constitutional Rights - is better fitted than the more common Positive Theory for human rights law cases, in which conflicting principles must be balanced [10,11]. A domain ontology that extends UFO-L will inherit this strength. However, the domain of human rights violations documentation includes many other important aspects. UFO-L does not cover, for example, organisational structures, places, or information management. Moreover, the design of UFO-L is rather abstract and not optimised for the instantiation of conceptual models for case databases.

Regarding available data models, the prime example is a model designed by the Geneva-based human rights group HURIDOCS, the so-called Events Standard, last revised in 2001 [5]. As the name implies it was designed primarily to represent events and the classical human rights violation question 'who did what to whom?'. However, it poorly represents other important questions, such as 'what are the human rights implications' (the institutional perspective) and 'how do we know this?'. Also, the Events Standard is closer to a physical model than a conceptual model and is not modularized, which limits its adaptability.

To summarise, there has been work on legal ontologies, and previous work on structuring human rights violations documentation, but there is no ontology that covers all aspects of the needed documentation. While the legal ontologies are too abstract and limited to legal aspects, the Events Standard lacks adaptability and is limited to physical events.

## 3 Approach to Develop the Proposed Ontology

## 3.1 Overall Research Framework: Design Science Research

Design Science Research (DSR) [17] as described by Johannesson &amp; Perjons [19] was used to tackle the research goal. DSR is an iterative process consisting of five logically connected phases: explicate problem, define requirements, design and develop artefact, demonstrate artefact, and evaluate artefact. DSR has been used previously in ontology design in the adjacent humanitarian domain [21]. A single DSR project does not necessarily cover all five phases. The main activities reported on in this paper are related to the requirements phase (activity 1-3), the artefact design phase (activity 4) and the demonstration phase (activity 5):

- -Non-functional requirements : Here we use a case study with interviews, and also information infrastructures theory. The result was seven non-functional requirements on the usage, structure and management of OntoRights.
- -Specific functional requirements : A document study identified important concepts and relations, which were grouped into seven subdomains.
- -Validation of requirements : To focus the design, a survey was done among practitioners to rank the priority of the seven subdomains for OntoRights.
- -Ontology design : The ontology was designed using the Ontology Development 101 method by Noy and Mcguinness [28], and by extending UFO-L. The result was two versions of OntoRights: Full and Simple.
- -Demonstration : OntoRights was instantiated for one fictional case and one real.

As mentioned, DSR activities are iterative and logical, as opposed to chronological. Designing the questionnaire used for verifying the requirements (step 3) gave additional insights that led to a minor reorganisation of the top themes identified in the document study (step 2). Also, the demonstration activity (step 5) revealed a weakness in OntoRights regarding expressing legal processes, and the design (step 4) was modified accordingly.

## 3.2 Design Theory: Information Infrastructures

The aim of the OntoRights ontology was that it should be useful for practitioners, to ensure that we employed the socio-technical Information Infrastructures (IIs) design theory by Hanseth &amp; Lyytinen [15]. Hanseth &amp; Lyytinen argue that conventional design theory in general wrongfully assumes a static environment and a designer in control of the design space. This might often be true for less complex types of IT artefacts such as single IT capabilities, applications and even platforms, but not for an II, which the authors define as: 'A shared , open (and unbounded), heterogeneous and evolving socio-technical system (which we call installed base ) consisting of a set of IT capabilities and their user, operations and design communities' [15, p. 4].

The IIs design theory includes what Gregor and Hevner [9, p. 340], refers to as a 'kernel theory' in the form of Complex Adaptive Systems (CAS). This fits well with the systemic (as opposed to tool-centric) approach to human rights technology suggested by Guberek and Silva [13].

Hanseth and Lyytinen [15] identify two inherent and conflicting problems of IIs design: the bootstrap problem (how to attract a critical mass of users) and the adaptability problem (how to prepare the system to grow and thrive). As a solution, the authors propose five design principles that are further broken down into 19 design rules. The next section describes how these principles and data collected using interviews informed the non-functional requirements elicitation of OntoRights.

## 4 Requirements Elicitation

## 4.1 Non-functional Requirements Elicitation

A case study was chosen to explicate the problem and define non-functional requirements. This choice may appear contradictory, since an important point of an ontology is being a shared, generic model that represents consensus about a domain [27] and a weakness of case studies is low generalisability [34]. However, even if human rights groups are very heterogeneous, they use variants of the same principles for human rights violations documentation and share a common system defined by international human rights law. Lincoln and Guba [23] argue that transferability (generalizability) depends on the similarity between two contexts, which they call 'fittingness'. In this sense, the 'fittingness' between human rights groups can be expected to be high.

The selected unit of analysis was the human rights group HURIDOCS, for the following reasons: First, HURIDOCS has a probably unique knowledge of human rights violations documentation, since it supports other human rights groups in this particular area. Second, HURIDOCS is not focused on any particular type of human rights issues or region, at least not intentionally. Third, this organisation has access to many other human rights groups in its network. Hence, by working with HURIDOCS the generalizability of the results is arguably relatively high.

The method to explicate the problem and define non-functional requirements was unstructured interviews with HURIDOCS staff. These requirements were then further developed through an informed argument with the support of the IIs design theory.

A general observation is that an ontology, together with its users and related IT solutions, forms an II, and the identified tension between the two II problems had relevance for the proposed OntoRights. The implications of the II bootstrap problem are that OntoRights must be useful for, and used by, small human rights groups for developing case databases. However, the II adaptability problem requires additionally designing OntoRights so that it can evolve and survive in the long run, and in the future be used also for system integration, machine learning, and semantic web applications. If not, another domain ontology with higher adaptability will probably eventually be designed and replace OntoRights. With the above in mind, the following requirements were identified:

1. Usefulness . According to Design Rule 1 of IIs [15, p. 8], 'a small user population needs to be identified and targeted' and 'the proposed IT capability has to offer the group immediate and direct benefits'. As already stated, human rights groups doing conceptual modelling is the primary target group of the ontology.
2. Ease of Use . According to Principle 1 of IIs, 'the IT capability to-be-adopted must be simple, cheap and easy to learn' [15, pp. 8-9]. Moreover, there is a risk that new technology will make human rights groups redirect too much of their scarce resources from their core mission, a risk that has been coined 'technological solutionism' [22, p. 13].
3. Customizability . Human rights groups have many different needs depending on their resources and thematic areas. Furthermore, as argued by Hanseth and Lyytinen [15], variety leads to evolution. This requirement also relates back to Requirement 1
4. Modularity . Principle 5 of IIs promotes modularity, i.e. OntoRights should not aim to be a complete and controllable system. Human rights violations documentation can be understood as an intersection of other domains, such as events, law, and social networks, including dimensions such as time and location. This is an argument for preferring less-than-perfect alignments with existing ontologies rather than aiming for high completeness of OntoRights as a stand-alone artefact. Mapping to existing ontologies furthermore relates to Principle 2 of IIs (Draw upon existing installed base). Modularity is also a means to an end for Requirement 3 (customizability).
5. Completeness . Just as Requirement 4 (modularity), this relates back to Requirement 3 and the necessity to cover heterogeneous needs of human rights groups in a wide domain.
6. Standards that are widely used . OntoRights aims to create a bridge between two, so far rather separated, socio-technical systems: human rights violations documentation and ontology design. So far there has been little use of ontologies in human rights work [13,22,30,31]. The challenge will be less if the used standards, e.g. foundational ontology and language, already are familiar to as many as possible of the intended users. Using existing standards is also key for OntoRights to potentially also be used for system integration, which relates to the IIs adaptability problem.
7. Tools that are collaborative and open source . According to Principle 3 of IIs, the number of users is in general more important for the value of an IIs than its functionality. New users can also find unexpected ways of using an artefact. This is an argument for using tools that are collaborative and open source. Furthermore, much of the development of human rights technology has been in the open-source sector [13]. Additionally, open-source promotes the above-mentioned 'continuous, local innovation' foreseen by Hanseth and Lyytinen [15, p. 16] and can in itself according to van Aardt [1] be considered a viable CAS.

These requirements, such as usefulness, may seem generic. However, to some extent it is in the nature of non-functional requirements to be generic. Furthermore, the above requirements provide a direction for the work - by highlighting the need for OntoRights to have properties that enhance its uptake. This focus on use in real situations may not be the main focus of all ontologies.

## 4.2 Functional Requirements Elicitation

The functional requirements express what entities, relations and situations the ontology will be able to represent, i.e. competency questions [28]. They were elicited using a qualitative document survey with the aim of acquiring a complete picture of concepts used in the domain. The survey was conducted as a document study of authoritative manuals about human rights reporting. The validity of a document is the product of its authenticity, credibility, representativeness, and meaning [26]. An authoritative manual will likely score high on all four dimensions. The sampling was exploratory, purposive and cumulative. The sample started with the several hundred pages long Manual on Human Rights Monitoring [29] by the UN Human Rights agency OHCHR. After review, the sample was extended to the 261 pages long HURIDOCS' Events Standard format [5]. Already after reviewing these two samples, the judgement was made that code saturation [16] was reached, and no more samples were added.

After gathering the samples, an analysis was done based on template thematic analysis [3] where extracted text segments were coded as triples, such as 'personemployed by-organisation' to create a graph that was also the first step toward an ontology. The result was 560 codes (triples). An interactive Kumu relationship map for visualisations and graph analysis was created.

Next, the triples were collated by assigning themes (tags) to them. The themes were then grouped, which produced a thematic map with 25 themes, which in turn were grouped into higher-level themes forming seven subdomains:

1. Roles and People (7 themes, 73 triples). A possible human rights violation often starts with a concrete event in which a perpetrator commits an action against a victim. In other words: What happened - Who did what to whom? This can also include: where, when, why and how .
2. Relations Between Events (1 theme, 10 triples). An event can have sub-events, and one event can have more than one super-events. An event can cause other events.
3. Interventions (3 themes, 53 triples). When a right has been abused, international human rights standards stipulate that state authorities have a legal obligation to intervene. It is often unclear when a case is finished, as events keep happening and information keeps coming. What actions were taken in response - who did what?
4. Human Rights Protection System (5 themes, 238 triples). The findings should then be compared to applicable human rights standards to answer: How is this a human rights problem - according to which legal norm?

5. Monitoring Process (4 themes, 38 triples). A human rights group that follows up on a possible human rights violation is engaging in human rights monitoring. The objective is often dual: to know the facts and to intervene. What did the human rights group do to investigate and intervene?
6. Information Management (3 themes, 77 triples). To present a convincing case, human rights groups must keep track of their sources and supporting documentation, and respect the different levels of confidentiality for each piece of information. How did the human rights group get its information, and how is it allowed to use it?
7. Organisational Structures, Influence and Risk (2 themes, 70 triples). Effective human rights monitoring requires an understanding of root causes and relations of power. What are the forces at work that influence a situation?

## 4.3 Validation of Requirements

A practitioner survey was used to validate the requirements found in the document survey. The research population was human rights practitioners around the globe with interest in conceptual modelling. The aim was to understand which of the seven subdomains and respective categories identified in the document study should be given priority during the design of OntoRights. The purpose of the sampling was representative, but the approach was pragmatic. HURIDOCS had recently engaged a network of practitioners as a reference group for the production of a Community Resource for database design [4], and most members of this network were offered to participate in the practitioner survey. Clearly, this network only includes a small part of the research population.

The data collection method was a questionnaire in English and Spanish, built with the survey tool of Stockholm University, in which the identified subdomains and some selected expressions from the document survey were reformulated as competency questions (CQs). The questionnaire contained 25 questions grouped according to the previously identified seven subdomains identified in the previous section. It also included background questions about the participants, such as years of experience and geographic focus. The questionnaire asked the participants to: (1) Imagine that their organisation was developing a new database for managing their documented cases of human rights violations; (2) According to perceived importance, do an ordinal categorisation of the identified themes. The questions started with 'How important is it that your database can express...'; (3) Perform a ranking of the importance of the subdomains. At the end of the questionnaire, there was a free-text question asking for comments.

In total, 13 participants submitted the form, of which 3 in Spanish. Everyone had experience (all but one at least two years) from working with human rights violations documentation, in particular from managing information from fieldwork in a database. Their joint experience covered all parts of the world that could be selected in the form, with some extra weight on'Northern Africa and the Middle East', and 'Latin America and the Caribbean'. Common focus areas of the participants included e.g. protection of human rights defenders, persons deprived of liberty, and migrants.

The data from the questionnaire was used to calculate the median and mode for each CQ. The subdomains were ranked according to importance using two methods, with rather concurring results. One method was to calculate an aggregated mean for each subdomain based on the number of received 'Very Important' or 'Important' for the respective CQs. The other method was based on the ranking done by the participants. Coarse-grained results from the second method can be seen in Table 1. More details are available online [24].

Table 1. Subdomains, and their ranking by practitioners.

|   Rank | Subdomain                      |   Rank | Subdomain                                      |
|--------|--------------------------------|--------|------------------------------------------------|
|      1 | Roles and people               |      5 | Relations between events                       |
|      2 | Information management         |      6 | Interventions                                  |
|      3 | Monitoring process             |      7 | Organisational structures, influence, and risk |
|      4 | Human rights protection system |        |                                                |

Interestingly, the information management subdomain ranked high (first or second place depending on calculation method). The importance of this domain according to the participants had not been reflected by the number of triples (77) relating to it in the document survey. We consider this an example of the limitations of only using documents such as manuals to discover a domain.

To summarise, the results of the practitioner survey informed which aspects to prioritise in OntoRights during the design and development activity. In other words, the results did not give a reason to modify the subdomains identified in the document survey but did provide a more complete picture regarding their relative importance.

## 5 The Proposed Ontology

The artefact consists of three parts: Full OntoRights, Simple OntoRights, and Manual for using Simple OntoRights for database design. Full OntoRights extends a foundational and core ontology, which follows non-functional requirement 6 (to build upon relevant standards). Full OntoRights was converted into Simple OntoRights to satisfy non-functional requirement 2 (ease of use).

Ontology design requires choices regarding foundational and core ontology, ontology language and ontology tools. For the construction of OntoRights, UFO [14] was chosen as a foundational ontology, and UFO-L [10] was used as a core ontology. As mentioned, UFO-L builds on Alexy's Theory of Constitutional Rights, which is more suited than Positive Theory for expressing human rights problems. Moreover, UFO has successfully been used to design an ontology in the adjacent humanitarian area [21]. OntoUML [32] was chosen as language, and the OntoUML Visual Paradigm plugin [27] was selected as tool.

## 5.1 Full OntoRights

Development Process. The ontology engineering methodology draws from Ontology Development 101 [28]. One benefit of the method is its focus on ontology reuse. In addition to UFO and UFO-L, other ontologies such as the E-OPL Enterprise Core Ontology [6] were used for a module about organisations. The design was also informed by other related databases, such as Geonames [8].

As stated previously, a non-functional requirement of the ontology was to have it modularized (requirements 3 and 4). The subdomains identified in previous sections provided the base for partitioning the ontology into modules. However, the modules were slightly changed in comparison to the identified domains, for two reasons. First, the structures of UFO and UFO-L sometimes made it more logical to adjust the partitions to UFO. Second, to achieve high modularisation, sometimes even smaller modules were designed. Note that the modules are fragments of one single ontology.

Description. The complete Full OntoRights, including interactive diagrams, can be accessed online as a published Visual Paradigm project [24]. There are 198 classes in total. Classes that are reused from UFO (20 classes) or the UFOaligned core ontologies UFO-L (10 classes) and E-OPL (9 classes) are indicated with prefixes. To fully understand the intricacies of OntoRights, the reader is recommended to consult the documentation of UFO [2,33], and OntoUML [32], Griffo's doctoral thesis about UFO-L [10], and E-OPL [6].

In UFO, classes with more than one superclass are common. However, this has largely been avoided in OntoRights to increase its usability for case databases.

Fig. 1. A module of Full OntoRights published as a website.

[FIGURE]

## 5.2 Simple OntoRights

Development Process. The method for converting Full OntoRights into Simple OntoRights can be summarised as follows:

1. Using single table inheritance [7] to collapse subclasses into superclasses, and instead use attributes with boolean values or enumerations.
2. Converting the OntoUML stereotypes Mode and Quality into attributes.
3. Adding some direct associations between classes that in Full OntoRights had to be deduced via other classes.
4. Excluding classes whose only purpose was mapping with UFO and UFO-L.
5. Excluding classes to reduce complexity.
6. Changing multiplicities to prioritise flexibility. While the multiplicity of Full OntoRights expresses what exists in the real world, multiplicity in Simple OntoRights is adjusted to what can be expected to exist in a real case database.
7. Removing the distinction between Atomic and Complex classes (concerns Event, Place, Organisation, and Unit). Instead, recursive partOf associations were used.
8. Adding attributes and datatypes.

Description. As shown in Table 2, the number of classes was reduced considerably. Simple OntoRights includes nine ordinary modules and an annex module with data types and enumerations. While Full OntoRights prioritised expressivity and alignment with UFO and UFO-L, Simple OntoRights prioritised ease of use. Consequently, Simple OntoRights is not fully aligned with UFO and is less expressive than Full OntoRights. On the other hand, it is easier to instantiate as a conceptual model of a case database. For this purpose we also included suggested attributes and datatypes.

Table 2. Number of elements in full OntoRights and simple OntoRights.

| Element                          |   Full OntoRights |   Simple OntoRights |
|----------------------------------|-------------------|---------------------|
| Modules                          |                16 |                  10 |
| Classes                          |               198 |                  34 |
| Associations and generalisations |               326 |                 115 |
| Data types and enumerations      |                 0 |                  26 |
| Attributes                       |                 0 |                 210 |

Simple OntoRights is less complex but also less expressive than Full OntoRights. The expressiveness can be compared according to the 25 competency questions (CQs) defined in the practitioner survey. While Full OntoRights can express all CQs but one, Simple OntoRights fails three completely and three partly. However, none of the CQs that Simple OntoRights fails completely had 'Very Important' as median or mode. A detailed account is available online [24]. The complete Simple OntoRights, including interactive diagrams, can be accessed online [24]. Like Full OntoRights, Simple OntoRights was designed with OntoUML Visual Paradigm Plugin without any warnings of syntactical issues. To maintain the connection to Full OntoRights (and UFO), the classes in Simple OntoRights are stereotyped as Full OntoRights classes, in addition to their OntoUML stereotypes.

## 5.3 Demonstration

Simple OntoRights was instantiated twice: for a fictitious case and a real case. The purpose was to practically try out OntoRights' usefulness, ease of use, customizability, modularity, and completeness.

The fictitious case is an organisation that starts with just one module, and then in a total of five iterations adds more modules, either complete or just partly. The instantiation process worked as expected. It was easy to extract the desired components from the ontology to form a reduced but still coherent model. Testing the modularity of OntoRights by iteratively adding additional modules did not pose a problem.

The real case involved one of the human rights groups that had participated in the practitioner survey - Committee for Justice (CfJ) - which monitors cases of detentions and maltreatment in Egypt. It aims to track how different criminal investigations involve different persons, who in turn are sent to different detention centres. The organisation preferred to be public about its participation, and since neither the organisation nor the authors could see any particular risk in this case, the organisation was not anonymized. Even the instantiation designed for CfJ could be published since it was built on information that already was public on the organisation's website [20].

The instantiation can be accessed as a static website [24]. It included six out of nine modules (not counting the Annex module). The main focus was on the Legal Process and Detention Centres modules. When dealing with a real organisation, it became apparent that there is a myriad of potential relations in the human rights violations documentation domain that are unfeasible to include in a general domain ontology. For example, CfJ tracks several different categories of people involved in criminal investigations, which required adding several associations. However, the necessary adaptations of the ontology could be done quickly with no negative effect on the model as a whole - showing the customizability of OntoRights.

CfJ reviewed the proposed instantiation and considered that it would be a useful starting point if the organisation in the future was to do major changes to its database. Regarding the usefulness of OntoRights, the interviewee stated they would definitely both use and recommend it if a case database would have to be designed. A negative aspect, however, is that the model contains so much information that it could be overwhelming for some practitioners - thus pointing towards that the ease of use may conflict with completeness. Regarding completeness, the interviewee considered OntoRights to have very good coverage of the most important areas of human rights violations documentation.

## 6 Discussion

OntoRights was elicited and designed with a strong focus on usability for practitioners and long-term viability in the wide and heterogeneous domain of human rights violations documentation. The IIs design framework by Hanseth &amp; Lyytinen [15] and its CAS kernel theory offered a theoretically grounded strategy to tackle this reality and manage the inherent contradictions between the 'bootstrap problem' and the 'adaptability problem'. Two important properties of OntoRights relate to IIs theory. The first characteristic is the modularisation of OntoRights, and its integration with other ontologies and important data sources. The second characteristic is that OntoRights consists of two versions. To pave the ground for long-term evolution and survival, Full OntoRights opens possibilities for being used for system integration, AI and semantic web applications. Recall that OntoRights, with its users, forms an II or CAS, and a CAS that does not survive is not useful [25]. For the sake of initial usefulness, Simple OntoRights bends the rules of both UFO and OntoUML, and constitutes a bridge between Full OntoRights and the models of case databases. We believe that future ontology design projects, particularly in wide and heterogeneous domains, also can be informed by IIs design theory, even if it should also be said that not all IIs design principles and rules are applicable to ontology design. We also believe that simplified versions of well-founded ontologies will increase their use and impact.

Considering again the many aspects of the human rights violations domain and the purpose of facilitating conceptual modelling of case databases for human rights groups, eliciting what OntoRights should be able to express became more about identifying priorities than a set specification list. The combined use of a qualitative document survey and a qualitative practitioner survey provided a grounded approach for identifying subdomains, CQs, and their relative importance. Together the surveys formed a funnel that turned written manuals of hundreds of pages into ranked CQs.

## 7 Conclusion

In this paper we reported on the design of OntoRights: a domain ontology for human rights documentation with the primary purpose of facilitating conceptual modelling of case databases for human rights groups.

Non-functional requirements for the ontology were elicited through a case study strategy and informed argument grounded in IIs design theory. Functional requirements were defined through two interrelated surveys: a document survey and a practitioner survey. Based on the performed demonstration in a real use case we initially conclude that OntoRights fulfils the requirements - with a note that completeness may hinder ease of use.

OntoRights fills a gap between abstract legal core ontologies and existing events-based human rights data models. OntoRights covers more of the many aspects of human rights violations documentation, is modularised for increased customizability, and is published with a relatively easy-to-use standard (OntoUML). Furthermore, OntoRighs extends a foundational (UFO) and core ontology (UFO-L). The latter is based on a legal theory (Alexy's theory) suited for analysing human rights problems. For increased ease of use when designing case databases, OntoRights was designed in two versions: Full OntoRights and Simple OntoRights.

In line with its focus on practical usability, OntoRights needs to be further evaluated, preferably in a fully naturalistic ex post evaluation. Other possible future research could include exploring the subdomains of monitoring and information management but from the perspective of case management.

## References

1. van Aardt, A.: Open Source Software development as a Complex Adaptive System: Survival of the fittest? In: Proceedings of the Annual Conference- National Advisory Committee on Computing Qualifications, vol. CONF 17, pp. 455-460. NACCQ, Jan 2004
2. Almeida, J.P.A., Falbo, R.A., Guizzardi, G.: Events as entities in ontology-driven conceptual modeling. In: Laender, A.H.F., Pernici, B., Lim, E.-P., de Oliveira, J.P.M. (eds.) ER 2019. LNCS, vol. 11788, pp. 469-483. Springer, Cham (2019). https://doi.org/10.1007/978-3-030-33223-5 39
3. Brooks, J., McCluskey, S., Turley, E., King, N.: The utility of template analysis in qualitative psychology research. Qual. Res. Psychol. 12 (2), 202-222 (2015)
4. Community Resources (2022). https://huridocs.org/docs/
5. Dueck, J., Guzman, M., Verstappen, B., Dueck, J.: HURIDOCS (Network): HURIDOCS events standard formats: a tool for documenting human rights violations. HURIDOCS, Versoix, Switzerland (2001), oCLC: 51243968
6. Falbo, R.d.A., Ruy, F.B., Guizzardi, G., Barcellos, M.P., Almeida, J.P.A.: Towards an enterprise ontology pattern language. In: Proceedings of the 29th Annual ACM Symposium on Applied Computing, . SAC 2014, pp. 323-330. Association for Computing Machinery, New York, Mar 2014
7. Fowler, M.: Patterns of Enterprise Application Architecture. Addison-Wesley Professional, Boston San Francisco New York Toronto Montreal London Munich Paris Madrid Capetown, 1st edn. (Nov 2002)
8. [GeoNames. https://www.geonames.org/](https://www.geonames.org/)
9. Gregor, S., Hevner, A.R.: Positioning and presenting design science research for maximum impact. MIS Q. 37 (2), 337-356 (2013)
10. Griffo, C.: UFO-L: A Core Ontology of Legal Aspects Built on Legal Relations Perspective. PhD Thesis, Federal University of Esp´ ırito Santo State (2018)

11. Griffo, C., Almeida, J.P.A., Guizzardi, G.: Legal theories and judicial decisionmaking: an ontological analysis. In: Formal Ontology in Information Systems, pp. 63-76. IOS Press (2020)
12. Gruber, T.: Ontology. In: Liu, L., ¨ Ozsu, M.T. (ed.) Encyclopedia of Database Systems, pp. 1-3. Springer, New York (2016). https://doi.org/10.1007/978-1-46148265-9 1318
13. Guberek, T., Silva, R.: Human Rights and Technology: Mapping the Landscape to Support Grantmaking. Tech. rep, Ford Foundation (2014)
14. Guizzardi, G., Wagner, G., de Almeida Falbo, R., Guizzardi, R.S.S., Almeida, J.P.A.: Towards ontological foundations for the conceptual modeling of events. In: Ng, W., Storey, V.C., Trujillo, J.C. (eds.) ER 2013. LNCS, vol. 8217, pp. 327-341. Springer, Heidelberg (2013). https://doi.org/10.1007/978-3-642-41924-9 27
15. Hanseth, O., Lyytinen, K.: Design theory for dynamic complexity in information infrastructures: the case of building internet. J. Inf. Technol. 25 (1), 1-19 (2010)
16. Hennink, M.M., Kaiser, B.N., Marconi, V.C.: Code saturation versus meaning saturation: how many interviews are enough? Qualit. Health Res. 27 (4), 591-608 (2017)
17. Hevner, A.R., March, S.T., Park, J., Ram, S.: Design science in information systems research. MIS Quarterly 28(1), 75-105 (2004)
18. Hoekstra, R., Breuker, J., Di Bello, M., Boer, A.: LKIF core: principled ontology development for the legal domain. In: Breuker, J. (ed.) Law, Ontologies and the Semantic Web: Channelling the Legal Information Flood. IOS Press (2009), googleBooks-ID: OYhpRvoa1OQC
19. Johannesson, P., Perjons, E.: An Introduction to Design Science. Springer, Cham (2014). https://doi.org/10.1007/978-3-319-10632-8
20. Justice Watch Archive. https://cfjustice.uwazi.io/
21. Khantong, S., Ahmad, M.N.: An ontology for sharing and managing information in disaster response. in flood response usage scenarios. J. Data Semant. Concepts Ideas Build. Knowled. Syst. 9 (1), 39 (2020)
22. Land, M.K., Aronson, J.D.: The Promise and Peril of Human Rights Technology (Introduction). In: New Technologies for Human Rights Law and Practice. Social Science Research Network, Rochester, NY (2018)
23. Lincoln, Y.S., Guba, E.G.: Naturalistic Inquiry. SAGE (Apr 1985), google-BooksID: 2oA9aWlNeooC
24. Lindeberg, J.: Link List - human-rights-ontology (Sep 2022). https://joranl. github.io/human-rights-ontology/link-list
25. McCarthy, I.: Technology management - A complex adaptive systems approach. Int. J. Technol. Manage. 25 (8), 728-745 (2003)
26. Morgan, H.: Conducting a qualitative document analysis. Qualitat. Report 27 (1), 64-77 (2022)
27. Nguyen, V.: Ontologies and Information Systems: A Literature Survey. Tech. rep., Defence Science and Technology Organisation Edinburgh (Australia) (Jun 2011), section: Technical Reports
28. Noy, N., Mcguinness, D.: Ontology Development 101: A Guide to Creating Your First Ontology (Jan 2001)
29. Manual on Human Rights Monitoring. No. No 7 in Professional Training Series, OHCHR, New York; Geneva (2011)
30. Pirac´ es, E.: The future of human rights technology: a practitioner's view. In: Aronson, J.D., Land, M.K. (eds.) New Technologies for Human Rights Law and Practice, pp. 289-308. Cambridge University Press, Cambridge (2018)

31. Poblet, M., Kolieb, J.: Responding to human rights abuses in the digital era: new tools, old challenges. Stanford J. Int. Law 54 (2) (2018)
32. Such´ anek, M.: OntoUML specification - OntoUML specification documentation (2018). https://ontouml.readthedocs.io/en/latest/index.html
33. Unified Foundational Ontology (UFO) (2017). https://dev.nemo.inf.ufes.br/seon/ UFO.html
34. Yin, R.K.: Case Study Research: Design and Methods. SAGE (2009)
