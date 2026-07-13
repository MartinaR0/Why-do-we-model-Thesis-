## THEME SECTION PAPER

## Modeling competences in enterprise architecture: from knowledge, skills, and attitudes to organizational capabilities

Rodrigo F. Calhau 1,2,4 · João Paulo A. Almeida 2 · Satyanarayana Kokkula 3 · Giancarlo Guizzardi 4

Received: 31 March 2023 / Revised: 14 January 2024 / Accepted: 18 January 2024 / Published online: 5 March 2024 ©The Author(s) 2024

## Abstract

Competence-basedapproacheshavereceivedincreasedattention, as the demand for qualified people with the right combination of competences establishes itself as a major factor of organizational performance. This paper examines how competences can be incorporated into Enterprise Architecture modeling: (i) we identify a key set of competence-related concepts such as knowledge, skills, and attitudes, (ii) analyze and relate them using a reference ontology (grounded on the Unified Foundational Ontology), and (iii) propose a representation strategy for modeling competences and their constituent elements leveraging the ArchiMate language, discussing how the proposed models can fit in enterprise competence-based practices. Our approach is intended to cover two tasks relevant to the combined application of Enterprise Architecture and Competence Modeling: 'zooming in' on competences, revealing the relations between competences, knowledge, skills, attitudes and other personal characteristics that matter in organizational performance, and 'zooming out' of competences, placing them in the wider context of other personal competences and overall organizational capabilities. An assessment of the representation is offered in the form of an empirical survey.

Keywords Competences · Ontologies · Competence Modeling · Enterprise Architecture

## 1 Introduction

To stay competitive, businesses must constantly innovate and adapt. This calls for certain organizational-wide capabilities that are not possessed by particular individuals in

Communicated by Dominik Bork and Sybren de Kinderen.

- B Rodrigo F. Calhau calhau@ifes.edu.br

João Paulo A. Almeida jpalmeida@ieee.org

Satyanarayana Kokkula Satyanarayana.Kokkula@usn.no

Giancarlo Guizzardi g.guizzardi@utwente.nl

- 1 LEDS, Federal Institute of Espiríto Santo (IFES), Serra, Brazil
- 2 Ontology and Conceptual Modeling Research Group, Federal University of Espírito Santo, Vitória, Brazil
- 3 Department of Science and Industry Systems, University of South-Eastern Norway, Kongsberg, Norway
- 4 Semantics, Cybersecurity and Services, University of Twente, Enschede, The Netherlands

isolation but rather are the outcome of a complex phenomenon whereby capabilities arise, among others, from the combination of personal competences, skills, attitudes, and knowledge. Hence, there is a need to manage both competences (and related elements) at the individual level and their interactions forming capabilities at the organizational level. Theemergenceoforganizationalcapabilitiesdependson how the various human aspects are connected.

Given the importance of the human factor for the emergence of capabilities in business management and in the transformation of socioeconomic systems in general, it is not surprising that human resource management, vocational education, and training typically receive considerable interest. The drive to human development has resulted in advancements in fields such as Vocational Education and Training (VET) [1] and Human Resource (HR) Management [2]. One of these advancements has been the gradual change to competence-based methods [3, 4].

Competence-based methods serve to link an organization's future requirements to its HR programs [5]. Personnel selection, development, and performance monitoring, as well as corporate strategy planning, are all examples of competence-based activities in HR Management [6]. By reviewing staff competences, organizations can conduct selfassessment to improve their HR programs, revisiting talent recruitment procedures, performance management systems, training and development tools, employee engagement initiatives, institutional development plans [5], performing competence mapping, identification, gap analysis, and other competence management activities.

[FIGURE]

[FIGURE]

To perform the various competence management tasks properly, it is essential to use appropriate competence descriptions. Generally, these descriptions are based on textual format: expected competencies and their outcomes are textually detailed; competence levels are specified using rubrics; competence elements (i.e., knowledge, skills, and attitudes) are itemized based on textual explanation, and; competence level assignment of each employee is performed using spreadsheets and textual justification. Despite the wide adoption, these competence descriptions lack structure and rigorous semantics. As a result, important questions concerning competence modeling may be left unanswered, e.g.,: How can team members' individual abilities be combined to achieve a desired capability? How are organizational capabilities and personal competences related? How can a team or a whole organization be affected by the development or change of an individual competence? What knowledge, skills, and attitudes need to be refined during professional training to have a greater impact? In summary, establishing the various connectionsbetweenorganizationalcapabilities and personal competences is not adequately supported by these kinds of textual descriptions.

Otherwise, some Enterprise Architecture (EA) efforts have been used to represent organizational capabilities and to support capability-based practices. In this context, EA notations (e.g., ArchiMate) have been widely adopted to support practices such as business capability planning and mapping. With these notations, it is possible to construct diagrams to visualize important aspects such as capability decomposition and other types of capability relationships [7, 8].

The importance of competences to the enterprise has motivated past efforts in which key concepts of Competence Management (CoM) were incorporated into Enterprise Architecture modeling [9, 10]. In that work, personal competences were conceived of as 'dispositions' of individual business actors that are manifested through their actions in organizational contexts. A number of patterns for competence representation in ArchiMate were proposed, leveraging on the capability construct. This paper builds up from that baseline and identifies and tackles challenges pursuant to 'zooming in' on competences. These were initially addressed in [10], but without considering the relationship between competence's elements. Besides improving the 'zooming in' by addressing competence's elements relationships, we also tackle challenges pursuant to 'zooming out' of competences considering the phenomenon of emergence.

[FIGURE]

This requires relating competences among each other and also revealing their role in the make up of organizational capabilities. In [11] we also approached the capability emergence phenomenon but more focused on factors related to system structure, such component connections, constraints, and functional roles. However, in [11] we did not delve into capability relationships related to emergence (based on disposition theories), and we did not consider human aspects (as competence elements) and their connecting to organizational capabilities, as in this present work.

This paper is further structured as follows: Sect.2 discusses how we approach the problem. Section3 briefly reviews the relevant literature on competences and competence management, stating the key conceptual challenges for 'zooming in' and 'zooming out' on competences, which involves the relations between competences, knowledge, skills, attitudes, and organizational capabilities as well. Section 4 quickly reviews the foundational baseline we adopt in this work, presenting elements of the Unified Foundational Ontology (UFO) [12] used to ground the ontological analysis of competence-related concepts. A reference ontology for these concepts is offered in Sect.5 by specializing the notion of disposition in UFO and examining the various relations that dispositions can establish with each other. This forms a principled basis for the representation of competence elements in ArchiMate as discussed in Sect. 6. Section 7 demonstrates the applicability of the representation in a real-world case. Section8 presents a survey to assess the representation. Section9 discusses related work. Section10 summarizes our effort and proposes a research agenda.

## 2 Methodological considerations

The literature on Competence Management reveals that it is indispensable to examine the build-up of competences in detail. Over the years, competence has been typically conceived of as the result of the interaction of specific knowledge and generic skills [13], mediated with attitudes [14]. Personal traits, mindset, patterns of thinking, and tacit knowledge are also considered by some authors to be part of competence [15]. While these terms are pervasive in the Competence Management literature, their precise definition has remained elusive. The terms are often used interchangeably and are sometimes confused with 'competence' itself [14, 16].

## 2.1 Ontological analysis

These aspects of the literature on Competence Management motivate us to employ ontological analysis [17] as a principled approach to competence representation, presented in Sect. 5. The approach is based on the analysis of the key conceptual notions and their relations in order to guide adequate representation in EA models. Domain-adequate representations are, in turn, the key to supporting the use of EA models in competence-based practices. We approach the representation of competence elements in this paper by positioning the notions of competence, skill, knowledge, attitude, and other personal characteristics through a reference ontology.

We argue that a conceptual analysis concerning competence relationships is also fundamental to their adequate representation in EA models. In this case, personal competences (and skills) can be related as a result of the collaborative relationship between professionals. Based on this, they can even give rise to new organizational capabilities in teams, departments, or other organizational structures. We address the conceptual problem by establishing the notions of vertical and horizontal capability relationships in a reference ontology, reflecting hierarchical and collaborative relationships based on theories of dispositions and property emergence in the literature.

## 2.2 Competence representation proposition

The reference ontology is then used as a starting point to the representation of competences alongside their constituent elements in ArchiMate , in Sect. 6. The reference ontology is also used as a basis for the well-founded representation of the various types of competence relationships in ArchiMate, in Sect. 6. This competence representation was proposed after an analysis of ArchiMate's specification and the meaning of its constructs. Then, we map the ontological distinctions, identified in the ontological analysis, to ArchiMate constructs. We also do the same concerning the relationships identified in the relationship. Then, based on an analysis of ArchiMate's views and CoM activities, we proposed a couple of views to represent competences in EA. This principled approach prevents ontological deficiencies (semantic overload, construct redundancy, construct deficit, construct excess [17]) from surfacing in the first place. The choice of reference ontology is key in this process. We employ the UFO [12] which includes intentional and social notions that are essential to account for organizational phenomena. This ontology has been used successfully in the analysis of several EA domains, including capabilities [18], services [19] and motivation elements [20].

## 2.3 Evaluation of the proposal

We assess the applicability of the proposed representation, in Sect. 7, by using it to model a case study from the literature addressed originally by Bäcklander [21] concerning the Spotify company. This shows the relevance of the artifact (competence representation guidelines) to account for the complexities of a real-world setting. Then, in Sect.8, a second evaluation is reported by means of an empiri- cal survey involving practitioners and academics. We have investigated the suitability of the representation for communicating the relations between the individual level of competences and the organizational level of capabilities and assessed the perceptions of the participants following the Technology Acceptance Model (TAM) [22].

## 2.4 Research method overview

Fig.1 summarizes the aspects presented above as part of the method used in our research, explicating the correlated section. As the focus of the research is related to the creation of artifacts (competence ontology and competence representation) and the generation of technical and scientific knowledge, this research method is based on the design science model [23]. As illustrated, the design science research model adopted in this work integrates aspects of relevance/application (the left side of the figure, represented by the context of application) and scientific rigor (represented by the right side, linked to the knowledge base). As shown on the left side, the context of this research is focused on human-based organizations, VET, and HR professionals, and concerns about CoM and EA modeling. In this case, VET is the umbrella term for all levels and types of education and training that offer knowledge and skills relevant to a variety of professions in the formal, non-formal, and informal learning environments of both the workplace/enterprises and educational institutions [1]. Similarly to design approaches, design science is also a method based on cycles. Artifacts and scientific knowledge are generated and refined on several interactions of problem understanding, construction, application, and evaluation. The results in this paper are related to the outcomes of the first iteration of this research cycle.

## 3 Capabilities, competences, and competence elements

Capability management has been a fundamental aspect for the success of enterprises, businesses, and organizations [24]. Effective capability management helps the organization to understand, (re) align, and integrate capabilities to achieve its strategic (and operational) goals. It allows the development of new organizational capabilities which enables the organization to conceive, develop, create, operate, support, and upgrade systems [24]. However, changes to organizational capabilities must be carefully managed to ensure the organization's success [24]. In order to reach this, the organization must perform assessments to identify the desired capabilities and compare them to the capability baseline (current capabilities) to determine the capability gap for the enterprise.

In this scenario, enterprise architecture can be helpful in determining the best way to 'fill' this capability gap and reach the desired capabilities [24]. They can help to understand how the organization is structured, what are roles performed by people, and how they are related [25]. As the authors address, organizations are formed by people. So, capabilities possessed by the organization (a.k.a., organizational capabilities) are necessarily a result of individual competences. As a consequence, understanding better what are capabilities, how they emerge, and how they are related to individual competences is fundamental to their better management.

[FIGURE]

Fig. 1 Research model adopted in this work

[FIGURE]

## 3.1 Capability definition

Capability is generally defined as a kind of ability, as the 'ability to do something' [26]. As is noticed in most capability definitions, the meaning of capability is closely connected to the meaning of ability . Ability is commonly defined as a disposition to act, or as a kind of dispositional property that allows do something (useful or not) [27]. More precisely, the ability concept is defined by [27] as the 'power that relates an agent to an action'. So, ability is a potentiality (power) related to a bearer and also to an action. Given this meaning, what distinguishes it from the capability?

One of the main distinctions regards the value aspect. In this sense, ability definitions are usually more generic, and not directly related to the 'desired' results, outcomes, or achievements. They are more 'neutral' in the sense of ability impact, i.e., abilities can be valuable (beneficial, useful) to a stakeholder or can even include 'not desirable' effects (e.g., vulnerabilities). On the other hand, one essential aspect that commonly distinguishes capabilities concerns their usefulness. For example, in enterprise architecture and systems engineering areas, capabilities are defined as the 'ability to do something useful' [24, 25, 28]; in information systems area as 'ability to achieve a desired effect'; and, in the military field, it is defined as 'ability to achieve a determined mil- itary objective' [29]; As illustrated, the 'beneficial' aspect is present in capability definitions in distinct areas. Many of these definitions were studied in [30], which generalized the capability definition. As it is addressed by [30], a capability is the potential for certain outcomes to be achieved concerning certain source entities. As addressed by the author, capabilities link these source entities (e.g., the bearer) to a result (e.g., output, outcomes, achievements). In summary, capabilities are changeable [31] and composable entities [32] which represent the quality of being capable of achieving specific effects or declared objectives [33].

[FIGURE]

Ascitedabove,capabilities have been approached in many domains such as strategic management, systems engineering, information systems, and military domains [29]. In this vast scope, they are related to a broad kind of entity sources (or bears), such as organizations, systems (from a distinct nature, specially engineered ones), and, especially for this work, human beings [29, 34]. In this last case, the capabilities possessed by a person (a.k.a, human capabilities) are called using distinct terminology such as skill, ability, expertise, know-how, and competences. In this work, we will focus on skills and competences.

## 3.2 Competences

Competence 1 is defined in different ways based on distinct approaches followed by competence-based practices. Westera [16] argues that there are two main approaches: one more practical and the other more theoretical . From a theoretical perspective, competences are seen as an internal cognitive structure belonging to an individual that enables the manifestation of desired behaviors. From a more practical perspective, also called operational, competences concern observable behaviors, and abilities, including skill, knowledge, attitude, meta-cognition, and strategic thinking, among other characteristics. Similarly, there are three main approaches to competency-based practices based on Weigel et al. [35]: behaviorist , generic , and cognitive . Likewise, to the practical approach described by Westera [16], the behaviorist approach focuses on describing desirable and observable behaviors. Such descriptions are related to demonstrations, observations, and performance of behaviors in certain situations. The generic approach seeks to generalize individual characteristics that lead to success such as age group, personality traits, temperament, etc. Similarly to the theoretical one, the cognitive approach is focused on describing 'hidden' characteristics such as an individual's 'mental resources' necessary to perform tasks, acquire knowledge, or achieve good performance.

1 In this work, we adopt the term 'competence' to refer to an individual's performative ability, and refrain from using the term 'competency'.

Mulder [36], in turn, studied various definitions of competence in research from the areas of VET, HR management, and HR development and identified three main approaches to professional competences: (i) behaviorist functionalism , (ii) integrated occupationalism , and (iii) situated professionalism . The first is a variation of the behaviorist approach but focused on training and performing specific functions. According to the author, this approach addresses competences through behaviors and formulations of skills and knowledge described in isolation. Therefore, as the author details, this approach considers competences in a fragmented way, focused on the training of segregated skills. In the integrated occupationalism approach, competences are seen as a person's integrated capabilities to achieve results. In this approach, competences are made up of knowledge, skills, and attitudes in combination. Thus, the author emphasizes that in this approach, such elements need to be present in an integrated and balanced form. The author also emphasizes that this approach is concentrated on outcomes and performance. The situated professionalism approach is based on the situated cognition area and defines competence based on its context. In this approach, competence and environment cannot be separated since the environment has affordances [37] that enable competence and its development. In this case, competence is a function for the environment, and both the environment and stakeholders (and their expectations) have a strong impact on the notion of competence. For this work, we will adopt the integrated occupationalism approach for competences, since it considers the relationships between competence elements. Besides this, we will also consider the competence perspective addressed by the situated professionalism approach, since this approach regards the context of competence. We chose such approaches because they are more aligned with theories of emergence and disposition that we use as a basis to represent the phenomenon of the emergence of capabilities from competences and their elements.

## 3.3 Competence definitions

From a practical perspective, as detailed above, competence is the general ability to perform well a set of mastery tasks [14]. It is not enough for an individual to have a variety of specific skills for this. Mastery of skills or knowledge does not ensure success in complex and unpredictable environments [16]. In addition to skills, the individual must have a sufficient understanding of the domain in question (knowledge) as well as know how to act appropriately in the context (attitude) [14]. In order to be efficient and effective in such situations, the individual must be able to integrate the most appropriate skills and knowledge for it [16]. As a consequence of this, various authors define competence as a combination of knowledge, skill, and attitude [13, 38, 39]. Competences, in other words, are highly valued qualifications that are accountable for the effective application of skills and knowledge in specific and complex contexts [16]. Based on this study of competence definitions concerning these distinct approaches presented above, Mulder [36] defines competence in a broader sense as (i) a set of integrated capabilities (i.e., in a general sense of 'being able to perform'); (ii) consisting of a content-related cluster of knowledge, skills, and attitudes; (iii) which are conditional for sustainable effective performance; (iv) in a certain context (profession, organization, job, role, and situation). This competence definition is the one adopted here since it is aligned with the competence approaches followed by this work. In addition, the competence definition addressed by Mulder [36] contemplates the definitions used in VET and HR areas, the focus of this work.

## 3.4 Competence management

Competence Management is a discipline that consists of four macro-steps: (i) mapping; (ii) diagnosis; (iii) development; and (iv) monitoring. The first step focuses on identifying an organization's desired competences, while the second focuses on discovering the competences the organization currently possesses. The development proposes concrete strategies for acquiring desired competences from ones already possessed. Finally, Monitoring is concerned with the continuous tracking of desired competence achievement [15]. These steps are supported by a variety of tasks and processes such as Competence Identification, Assessment, Planning, Modeling, and Gap Analysis. The latter is one of CoM'smostdifficult tasks. It compares current competences, inherent to an individual, and desired (future) competence for the organization (i.e., types of competence), assisting in the development of strategies during the Competence Development stage [15]. Another important task is Competence Modeling, which represents information on current or desired competences, facilitating Gap Analysis. Individual characteristics, level of proficiency, the context of competence, competence composition (aggregation), hierarchical structure, and evidence of how competence was obtained are generally the focus of their attention [4, 39].

[FIGURE]

## 3.5 Competence elements

As approached above, competence is generally defined as consisting of a content-related cluster of knowledge, skills, and attitudes. Sometimes, competence definitions also include 'other characteristics' as traits and other aspects. These parts that form a competence are also called here as competence elements and each of them will be detailed in the following.

## 3.5.1 Skills

In general, skills , not unlike competences, allude to the capability to perform actions. The literature provides different definitions for skills emphasizing different aspects of it. For example, Rodriguez [6] defines a skill as the ability of an individual to perform a task (discrete unit of work) well. Esposto [40] defines it as a set of general procedures that underlies the application of knowledge in a domain. Paquette [13] defines skills as processes that act on knowledge in an application domain [13].

There is no agreement on the best criterion for distinguishing competences and skills [16]. One existing distinction is the level of ability awareness. Competences would be more 'conscious', while skills would be more 'automatic' [16]. However, this distinction is insufficient because conscious actions occur with skills as well [16].

The level of complexity is another criterion that is invoked to differentiate competences and skills. Competences are considered more complex in this case than skills. Indeed, authors argue that skills structure competences [13, 16]. Competences can be made up of sub-competences, forming an internal hierarchical structure inherent in the individual. In this sense, competence is a complex entity. That is, competence can be formed by others, which can be formed by others, and so on. As a result, this internal hierarchical structure can be formed by many levels of sub-competences [16]. The basis of such an internal hierarchy, however, has not been well understood. Competence decomposition only occurs up to a certain level, where the 'simple' competences are. Generally, these competences are divided into skills (and also attitudes and knowledge) after this level. In this regard, it is unclear where 'simple' competences end and skills begin [16]. Even skills can also be divided into different levels, until reaching the 'basic skills'.

Some competence models allow sub-competences or skills that make up a competence to be represented. However, as previously stated, the line between 'simple' competence and skill is not always evident. Due to their similarities, the concepts of competence and skill are frequently misunderstood in definitions and representations. As a result, an important goal of a reference ontology for this domain is to clarify the similarities and differences between the concepts of competence and skill, settling how to position those two notions for a certain context of usage.

[FIGURE]

## 3.5.2 Knowledge

Internal representations of facts, principles, or theories in a specific domain are typically associated with 'knowledge' [16]. It is the cognitive outcome of assimilation of concepts, ideas, or figures related to a specific topic [14]. Knowledge is linked to a specific person, the bearer, which assimilates the facts, principles, theories, and information, that becomes a part of the bearer's internal structure [41]. As new information or facts are added, the structure changes [42]. This internal structure is not distinctive to the bearer but is integrated into the internal structure of abilities [42]. Indeed, such internal structures (of knowledge) interact in practical applications and problem-solving [43]. Knowledge can change over time [43] as a result of the individual cognitive skills (mental processes), which also store the knowledge in memory and retrieve it [16].

Many knowledge definitions are similar to skill descriptions as a result of learning. Some authors even consider skills to be a sub-type of knowledge. According to [43], skills represent an individual's 'practical knowledge' gained through experience. While an individual's interpretations and facts are known as declarative knowledge, the skills (what an individual knows how to do) are known as procedural knowledge [43]. Authors include that skills and knowledge are represented similarly in the human mind, via an interconnected internal structure [43].

Understanding an individual's knowledge in the context of CoM is important for better understanding their competence. This is particularly useful during the gap analysis and competence assessment steps. Competence models, which represent a professional's knowledge, can aid in this task. Despite the similarities described above, skills and knowledge have subtle differences that can interfere with modeling. As a result, a reference ontology for this domain should provideasoliddefinition of knowledge and clarify the distinction between knowledge and skill.

## 3.5.3 Attitudes

In some definitions, attitudes are generally associated with an individual's conduct and posture [13, 39]. Others associate them with personality traits or the professional's psychological and emotional nature [14]. Attitude is a tendency to act (or feel) in a given situation [44]. It is based on assumptions, val- ues, and beliefs, so they are non-neutral concerning actions [44]. In general, definitions of attitude take into account the following characteristics: (i) mental state; (ii) values (beliefs, emotions); and (iii) predisposition to act or behave [45]. That is, it is a concept that is dependent on its context: a situation, an object, or a person. As a consequence, attitude is a disposition toward a phenomenon of a given type and can be considered a reaction to the context (whether positive or negative) [45].

Attitudes are regarded as an important aspect of competences, and are included in many competence definitions as one of the key 'KSA' elements (Knowledge, Skills, and Attitudes). In contrast to skills and knowledge, attitude is a more general characteristic that is not tied to a specific task or domain [14]. Because they have a certain behavioral impact, attitudes are frequently confused with skills, particularly soft skills [39]. Again, as in the case of skills and knowledge, a reference ontology for this domain should clearly position attitudes with respect to the other elements of competence.

## 3.5.4 Other characteristics

Although competence is commonly defined as a set of attitudes, skills, and knowledge, authors consider further types of elements to be components of competences. Personal traits, posture, mindset, and patterns of thinking are considered by some authors to be part of competence [15]. This is recognized also by Westera [16], for whom competences have additional elements that are not clearly defined. According to Miranda et al. [39], competences are also formed by a set of personal characteristics required to perform tasks in a specific context, leading the authors to consider the 'KSAO' model, a variation of the KSA model that includes 'Other Characteristics' as a fourth element to define competence.

According to Westera [16], task analysis is insufficient to establish competences; instead, the individual's characteristics and experience must be considered. Le Deist and Winterton [3] emphasize the importance of focusing on the individual rather than their conduct. The authors explain that, in addition to performance, it is critical to look at traits, motives, attitudes (or values), and knowledge, among other things. Some KSA elements (knowledge and attitude) are considered personal characteristics by the author. Messick [43] extends on this point by stating that the psychological, emotional, and social (environmental) situation must all be considered.

All of these characteristics, as well as actual behavior (performance, tasks, and outcomes), can be used to assess an individual's competence. Hence, attention to these elements is critical to the Competence Assessment task, which is one of the most demanding in the CoM context, because it entails evaluating (and even measuring ) something that cannot be fully observed.

## 3.6 Connecting competences and organizational capabilities

Competence management gains new dimensions when competences are considered in relation to other competences. First, competences of the same individual can be combined to form new competences [39]. An example is John's frontend development competence and his back-end development competences, which when combined form John's full-stack development competence. Such a composition forms an internal hierarchical structure in which a 'super' competence is dependent on a 'sub' competence [39, 46]. Similarly, the competences of different individuals can also be externally combined in the context of teams, groups, projects, or sectors of an organization [47]. In this case, instead of forming new competences, this combination of external competences contributes to the formation of organizational capabilities [47]. This is what happens when John's Front-end development competence and Karl's Back-end development competence are combined to form a team's Full-stack development (organizational) capability. In this setting, it is important to realize that the 'combination' of individual competences to generate organizational capabilities is not arbitrary. Generated organizational capabilities are the results of the ways in which people, teams, and groups are organized [47]. In other words, just bringing together high-performance people is not enough to form a high-performance team. Individual competences must be properly combined to generate desired organizational capabilities. This issue is fundamental in the context of CoM, as it has as its objective the development of organizational capabilities. In this sense, the development of individual competences is a means of developing the organizational capabilities of the entire organization. Hence, it is critical to understand how individual competences and their holders can be combined for the desired organizational capabilities to emerge.

## 4 Foundational baseline

We build upon the work discussed in [9], which uses the Unified Foundational Ontology (UFO) [12] to examine competences from an external perspective. That work does not zoom in on a competence's constituent elements. Competences are considered 'dispositions', 2 which, in a nutshell, are objectified properties inherent in an object (or agent) that may manifest themselves in certain situations through events (or actions).

The domain-independent elements we reuse from UFO are shown with a UML class diagram in Fig.2. Individuals are partitioned into perdurants (also called events ), endurants, and situations. Perdurants are individuals that occur in time (including processes activities, actions, tasks). Endurants are individuals that persist in time changing qualitatively while retaining their identity (i.e., people, organizations, cars). Endurants include substantials and moments . A Substantial is an endurant that is considered existentially independent (like John, his car), while a Moment (also termed Aspect ) is a reified property that inheres in another endurant (termed its bearer), on which it is existentially dependent. Moments (as full-fledge endurants ) have a life-cycle of their own and can be created, destroyed, or otherwise changed qualitatively in time. Examples include John's weight (a quality that inheres in him), his marriage to Mary (a relator that depends on John and on Mary), and John's fishing skills.

2 Dispositions are sometimes also called 'powers' in the philosophical literature [48].

[FIGURE]

Fig. 2 Foundational fragment employed in this paper

[FIGURE]

Of special interest to us in this work are those moments called dispositions . Dispositions are moments 3 that can be manifested through the occurrence of events (possibly agents' actions, such as Anna's speaking English). In situations where dispositions may manifest , they are said to be 'activated' (e.g., when a magnet is close to some ferrous material, or when Anna is prompted to introduce the topic of a meeting). The literature discusses a number of important features of dispositions; they may fail to manifest when enabled, they may be manifested in tandem with other dispositions in complex events, and they may reinforce or cancel each other [48, 49]. Reifying (i.e., objectifying) them puts them at the center of our efforts as first-class citizens. As endurants, they can themselves bear moments, and change qualitatively while retaining their identity through time [50].

Figure 2 also shows a few concepts from the UFO-C layer [51] which are relevant here. UFO-C is an extension of UFO addressing social aspects [51]. In UFO-C, agents are considered objects that perceive events and perform actions (i.e., intentional events) based on a background of beliefs , desires , and intentions (special categories of intrinsic moments termed intentional moments , omitted from the figure for brevity). As depicted in the model, agents can be physical (e.g., humans and animals) or social (e.g., teams, organizations, communities, etc.), and all of these are considered potential bearers of capabilities and intentional moments .

3 we are adopting a broader sense of dispositions as moments and not only intrinsic moments . In this sense, relators and other externally dependent moments can also have dispositional aspects.

[FIGURE]

## 5 Ontological analysis of capability and competence-related concepts

Weexplore the multi-faceted phenomenon of competence by proposing a reference ontology for competences concerning its constituent elements and the corresponding organizational capabilities . The issues discussed in Sect.3 helps us to identify focal points for this effort, and ultimately relate competences , knowledge , skill , attitudes , and other human characteristics to organizational capabilities , in a coherent overall representation, as required in Enterprise Architecture efforts.

Figure3 shows a hierarchical perspective of the proposed competence ontology. The concepts in yellow were explored initially in [10] (of which this paper is an extension), and already incorporate the 'zooming in' perspective on competences (from personal competence to its elements, revealing knowledge , skills , attitudes andother humancharacteristics ). The concepts concerning the 'zooming out' perspectivewhich are our focus in the sequel-are highlighted in red, and integrate the ontological analysis of capabilities proposed in [18] with the 'zooming in' perspective. All elements are ultimately specializations of the UFO concepts (in green). In the following, each of the proposed concepts will be addressed, as well as the relationship between them.

## 5.1 Zooming out (from competences to organizational capabilities)

The general notion of capability is key to place personal competences and organizational capabilities in the same conceptual framework, understood as dispositions [18].

Capabilities are changeable [31] and composable entities [32]. As the quality of being capable [29, 47], a capability inheres in a bearer and depends on it to exist. As a potentiality [28], a capability has attributes that may only be observed through the capability's manifestation in an enabling situation (or context). Similarly to [28], a capability is considered here as a subtype of disposition that has a 'utility', or a 'benefit' for someone. Since it is a subtype of disposition (also following [18]), a capability is manifested by capability manifestation ( perdurants ), is activated by a situation called capability context , and is inherent to a substantial , specifically an object (the bearer), as represented in Fig. 4.

Fig. 3 The proposed competence ontology (hierarchical view) grounded on UFO concepts (in green)

[FIGURE]

Fig. 4 The capability concept and its relations (vertical ones highlighted in blue)

[FIGURE]

## 5.1.1 Capability's vertical relationships

Fig.4 also shows what we call here the 'vertical relationships' between dispositions (capabilities included), encompassing results from and emerges from . These capability relations are called 'vertical' as they relate the capabilities of a complex object (at a higher level of composition) to the capabilities of the object's parts (at a lower level). In addition, capabilities themselves can be subject to 'decomposition', 4 and hence, a complex capability can have other capabilities as its parts (see 'has part' in Fig. 4). These vertical relationships are further explained in the sequel.

## 5.2 Capabilities of a whole and capabilities of the parts

As [49] states, powers from a whole (named high-order powers) are formed by a combination of power from the parts (the low-order powers). In this sense, an organizational entity (e.g., team, department, company), as a whole, is hierarchically structured as having parts, in this case, other organizational entities or individuals as its parts. As a result, in a simplified and direct way, the capabilities inherent to a complex organizational entity may be accounted for in terms of the combination of capabilities of its parts. This perspective concerning vertical relations is depicted in Fig.5a (left-hand side of the figure). Examples include (i) a team's collective capability that emerges from the personal competences of team members, and (ii) the capability of a distributed computer cluster to serve a large number of customers that results from each individual computer system's capabilities.

4 decomposition not in a reductionist sense, i.e., in an effort to explain the phenomenon of emergence.

Fig. 5 Vertical relationships illustration

[FIGURE]

The distinction between 'emerges from' and 'results from' corresponds to Bunge's notions of 'emergent' and 'resultant' properties [52, 53]. Bunge states that resultant properties are those that can be directly decomposed, explained, or reduced into properties of a system's parts. For example, the total mass of a car is directly defined by the simple sum of the masses of its components; or, the chair height is a result of the sum of the height of the leg, seat, and back. In a similar sense, [49, 54] also state that not all highorder powers as a whole are emergent. As they state, some of these powers are just a result of the sum of lower-order powers, or 'additive composition' of them. In this case, as addressed, the resultant power (disposition) has no novelty regarding the parts.

[FIGURE]

In contrast, emergent properties are those that, while related to the properties of parts, are not present in isolation in the separated parts [53]. For example, the buoyancy of a ship cannot be reduced directly to the buoyancy of its parts (an arbitrary piece of a steel hull is typically not buoyant by itself). So, as addressed by [49], emergent powers (dispositions) must be related to a novelty. Besides this, they must be autonomous regarding the emergent base [55]. Hence, emergence is not directly explained by some simplification or 'reduction'. Instead, property emergence can be explained according to many aspects, such as (i) the part's properties 'combination' [49, 56]; (ii) the part's relationships (structure) [57] (e.g., the way in which carbon molecules are associated distinguishes diamond's and graphite's dispositions); (iii) system constraints [58, 59] (e.g. restrictions caused by the knee in the femur and tibia movements allow the emergence of the walking capability); (iv) non-linearity [60] (e.g., feedback loops); and even (v) environmental factors [49, 53] (e.g., nature laws).

All these aspects are somehow related, however, our main focus here is on the first aspect: how dispositions (capabilities) can be combined to promote the emergence of other dispositions (capabilities). As [49] states, the power of parts can be 'combined' in many ways: they can be 'added' (increasing the resultant power), subtracted (decreasing the resultant power), and they can even be counterbalanced by each other, reaching a 'countervailing power' of stability. In this context, the authors address some issues regarding the power (disposition) 'combination', such as (i) power 'overdose' (i.e., when the power increase promotes the opposite effect); (ii) power'escalation' (i.e., when small powers have greater effects together); and (iii) 'antipathetic' powers (i.e., powersthatisolated have an effect but together have the opposite effect). In the case of these issues, as addressed by [49], it is not possible to combine dispositions as a mere sum (using additive composition). These dispositions (and how they interact) must be understood holistically, in a 'nonlinear' way. Because nonlinearity is an essential aspect concerning emergence [60], disposition relationships generally include casual loops (related to feedback mechanisms [61]). These cyclic relationships are responsible for creating balancing and, vicious and virtuous cycles that stimulate the 'power escalation'. The way the dispositions of parts are interrelated forms the called 'emergence mechanism' [61], i.e., the 'dispositional structure' [62] inherent to a whole capable of promoting the emergence.

[FIGURE]

So, in order to address these aspects, in our ontology, we consider that emergent capabilities are those inherent to a whole that 'emerge from' (interrelated) capabilities from the parts, as shown in Fig. 4. The way these capabilities of parts are related (through horizontal relationships ) to promoting the emergence is expressed in UFO terms in a particular situation . Based on UFO distinctions, all those other circumstances that allow for emergence (i.e., structure, constraints, environmental factors) can also be explained as (emergent promoting) situations . 5 Hence, in order to account for these situations broadly, an emerges in the relation between the concepts of capability and situation can be found in Fig.4. The identified situation expresses a combination of factors that account for the emergence of that capability. In summary, a capability can emerge from other capabilities in a particular situation.

## 5.3 Complex capabilities and their parts

The second perspective about vertical relationships concerns the complexity of capability, regardless of the hierarchical structure of the bearer, as shown in Fig. 5b (right-hand side). Examples include (i) the capability of a boat to move in a body of water, which is formed by the boat's buoyancy, its propulsion capability, and its capability to be steered; (ii) the football-playing capability of a player, which is formed by his/her dribbling skill, attacking skill, defending skill, etc.; and (iii) the back-end development competence of a software developer, which is formed by his/her Java programming skill and SQL coding skill.

Differently from emerge from and results from , the parthood relation ( has part in Fig. 4) relates a complex capability to other capabilities that inhere in the same bearer, as shown in Fig. 5b. In this context, a similar notion is put forward by Bunge [52] when discussing 'property conjunction', among property types. He explains that property types can be formed by a ' conjunction ' of others, i.e., basic property types forming complex ones. For example, the dimension of a box is a 'conjunction' of its width , length , and depth . In a similar way, [62] also states that 'simpler properties are constitutive of a more complex property'. In this context, the complex property is a kind of bundle. Regarding dispositions , according to [49, 62, 63], they also have a compositional nature. In the same context, [49] also approached the concept of 'cluster of power', a concept similarly related to our definition of complex capability. As a result, a complex disposition can be composed of (or decomposed in) basic dispositions .

5 Besides being fundamental in order to understand the emergence phenomenon, the structure of parts (their connections), constraints, and functional roles they perform regarding the whole are not part of the scope. This perspective of capability emergence is better approached in [11].

Fig. 6 Organizational and human capabilities concepts (in red) with correspondent vertical relationships (in blue)

[FIGURE]

## 5.4 Organizational capabilities and human capabilities

we apply capability and vertical relationship definitions to allow the 'zooming out' on competence modeling, from competences to organizational capabilities . As a result, we address in the ontology the concepts of (i) organizational capabilities and (ii) human capabilities , as shown in Fig.6.

Organizational capabilities are those that inhere in a social agent specifically formed by people (e.g., group, organization, team, department, etc.). In their turn, human capabilities are those that inhere in a person ( physical agent in UFO). In this case, human capability encompasses all human abilities to perform some (human) task , from those that are innate (inherited) to those that can be learned (formally or not). In the context of human capabilities , we consider a task as an action that is oriented to a specific (and explicit) result, output, or achievement In this perspective, a task is regarded as a unit of labor. In other words, it is a unit of work that contributes to the production of output or the achievement of a result [6].

Figure 7 shows a schematic view combining organizational capabilities and human capabilities, in which a 'complex organizational capability 1' inheres in a group and has as part other basic organizational capabilities . In this case, as depicted, the 'basic organizational capability 2', as a capability of the group as a whole, 'emerges from' (or 'results from') the human capabilities (of members of the group). Figure7 shows this distinction, in which the 'complex human capability 1' inheres in a person P 2 and is formed by other basic human capabilities .

## 5.4.1 Capability's horizontal relationships

Differently from vertical ones, horizontal relationships do not account for a new (complex or whole's) capability based on other (basic or part's) capabilities , in spite of being relevant in the conditions of emergence. Figure8 depicts the horizontal relations we consider here, including (is) reciprocal to , (is) additional to , enables , disables , and changes . In fact, in the sense we are approaching here, all these relationships correspond to potentialities (of 'interaction' in the context of a specific manifestation). For this reason, a more appropriate name for these relationships would be 'can be additional', 'can enable', and so on.

Fig. 7 Complex and basic organizational and human capabilities (illustration)

[FIGURE]

Besides not being detailed in Fig.8, these relationships between (individual) capabilities are derived from the relationships between their capability types (in a similar way that was proposed in [64]). For example, suppose that John (a singer) and Karl (a guitar player) are members of the same musical group and they have the (human) capabilities of singing and playing guitar. These capabilities are (potentially) additional because their capability types - singing and playing guitar - are additional. However, we do not consider only this criterion since it is quite broad. Considering just this, John's singing capability would be additional to every capability of playing guitar, from all guitar players in the world, even those that he will never be able to play together. So, in order to be more precise, we just consider capability relationship when: (i) the capability types are related (as stated), and (ii) the bearers stand in the same 'bonding' situation. For example, John's and Karl's capabilities can just be related as additional because (i) their capability types are additional and (ii) John and Karl belong to the same band and are (physically and socially) connected.

Generalizing, to establish the capability relationships, this 'bonding' situation (or context) must include the capabilities, their bearers, and especially the relationships (connections) between these bearers . 6 . This is represented by the 'stands in' relationship between capability and situation in Fig.8. It is important to highlight that, the fact two capabilities are potentially additional, reciprocal, and so on, does not imply that they will necessarily manifest together. Potentiality does not imply occurrence. For example, besides having additional capabilities, John and Karl can never sing/play together. So, besides the relationship of potential joint man- ifestation, we could consider another kind of relationship between the capabilities, more related to the historical dependence of their manifestations. For example, in case John and Karl are playing/singing together weekly, we can say that their capabilities 'have been additional', since they have a history of joint manifestation. As this relationship kind is not the focus of this work, we are not showing it in the model.

6 Our focus here is not to explain the structural aspects that promote the relationship between capabilities however in [11, 65] we delve deeper into these aspects and this 'bonding' situation was named system situation This situation includes capabilities holders and their connections, allowing the relationships between capabilities holders and, as a result, the interaction between them.

[FIGURE]

Fig. 8 Capability's horizontal relationships (in red)

[FIGURE]

## 5.5 Reciprocal relationship

Based on [49, 66], dispositions can be reciprocal when they mutually depend on each other to be manifested (not existentially or historically dependent). For example, the magnetic's attraction disposition is circumstantially conditional to the iron's disposition of being attracted (and vice versa). Consequently, their activation situations and manifestations should be the same (or be closely related). For example, the dispositions of the magnet and the iron share a related situation (related to their proximity to each other) and a related manifestation (to attract or be attracted together). In a similar sense, according to [52], dispositions work in pairs based on their complementarity. So, the disposition d 1 of a thing x , to actualize, depends on (i) a circumstance (situation) that involves a thing y with a disposition d 2, and (ii) a 'match' between the dispositions d 1 and d 2. In this case, the author calls the thing y as a complement of thing x . We call this 'complementarity' between dispositions, in the sense addressed by [52, 66], as the reciprocity relationship. As stated by [49], powers can have different 'manifestation partners', having distinct manifestations depending on the partner. So, this 'manifestation partnership' is not a dyadic relation. Besides this, not all powers need 'mutual manifestation partners', as addressed by [49].

Figure 9a illustrates this setting. As depicted, the reciprocal dispositions share a common activation context and also common manifestation events ( tasks in the figure), being mutually conditioned to manifest together. As mentioned, we also consider that capability types are 'reciprocal to' others (not shown in the model), as addressed in [64, 67] with the 'mutual activation partnership' relationship definition, based on UFO. Based on this, we can derive that a capability is potentially reciprocal to others according to their types, as already explained.

Fig. 9 Reciprocal horizontal relationship

[FIGURE]

[FIGURE]

## 5.6 Additional relationship

As stated by Mumford et al. [49], powers can be combined with additive (and even subtractive 7 ) effects. In the same sense, according to Barton et al. [63], one disposition can be additive to another if their effects (manifestation) can be 'mixed' for some reason. In this sense, dispositions are 'added' in order to manifest together in a same situation. As a result, each disposition impacts the other changing qualitatively their manifestation (or forming a complex one). For example, the (i) attraction disposition of two or more magnets can be added, making their attraction stronger; (ii) a singer and a guitarist's capabilities can be added, allowing a distinct song presentation; (iii) the vibrating capabilities of two or more guitar strings can be added, forming new combined notes. As occurs in these examples, the additional relationship can cause a vertical relationship to arise (but not necessarily). The addition of magnets' dispositions can result in a resultant capability, and the addition of the singer and guitar player's capabilities can make an emergent capability arise. Unlike reciprocal capabilities, an additional capability is not inevitably dependent on another to be manifested. Their relationship is not mandatory but optional. For example, in the case of the guitar strings' vibrating capabilities, they can be manifested independently. Otherwise, the reciprocal capabilities need each other to be manifested. In the example, the 'attraction capability' of a magnet needs the ' be attracted capability' of iron to manifest. In fact, as [49] states, these 'additive powers' can even not interact directly (e.g., not triggering each other). In this case, this means that, they just need to have the same 'subject of change' [49]. Figure9b illustrates this setting. While the reciprocal relationships share a common interdependent activation context, the additional dispositions have distinct activation contexts that can be (optionally) related, allowing an interrelated manifestation. We also consider that capability types are 'additional to' others (not shown in the model). Based on this, we can derive that a capability is potentially additional to others according to their types, as explained.

7 not the focus in this work.

## 5.7 Dynamic relationships

We call the dynamic (horizontal) relationship between capabilities the relationships of enabling, disabling, and changing.

Enabling Relationships Regarding the dynamic aspect between dispositions , they can also have interactive relationships with each other. As Barton et al. [63] state, dispositions can (potentially) trigger or be triggered by others, creating a 'chain reaction'. In the same sense, [49] also mentions the 'causal chain' related to the manifestation of a group of powers. In this case, the manifestation of one disposition creates (as effect) a 'favorable' situation that activates another disposition , as shown in Fig.10a. In UFO terms, a manifestation of a capability through a task ( perdurants ) can bring about a situation that activates another capability . Based on these distinctions, this work considers that a capability can (potentially) 'enable' (trigger) others. We also consider that capability types 'enable' others (not shown in the model). Based on this, we can derive the relationship that a capability can (potentially) enable others based on their types, as explained.

Disabling Relationships Based on Galton et al. [66], an opposite phenomenon is also possible when a disposition blocks the manifestation of another disposition . As approached by Mumford et al. [49], a power can prevent the manifestation of other powers. In this case, a 'blocker' disposition creates some (unfavorable) situation that inhibits the activation of another disposition . This circumstance is also illustrated in Fig. 10a. In UFO terms, a manifestation of a capability through a perdurant (event) can bring about a situation that inhibits another capability . Basically, the disabling relationship presented here has the same meaning as the 'prevention' relationship proposed based on UFO in [64, 67]. Based on these distinctions, this work considers that a capability can (potentially) 'disable' (block or prevent) others. We also consider that capability types 'disable' others (not shown in the model). Based on this, we can derive that a capability potentially disables others according to their types, as explained.

Changing Relationship Dispositions of a thing change over time [62]. Based on the authors, they can even have a duration of existence, this means, cease to exist. As stated by [49], power and its manifestation generally involve transformation and changes, including changes in properties. Dispositions can even change themselves when they manifest, as [62] states. So, another kind of 'dynamic' between dispositions happens when one disposition changes another. In this context, the manifestation of the 'changer' disposition modifies qualitatively another disposition, altering its properties (and also its manifestation) . 8 This changing relationship is illustrated in Fig. 10b. In UFO terms, a manifestation of a capability through a perdurant (event) can change the moments (i.e., qualities or modes ) of another capability . Based on these distinctions, this work considers that a capability can (potentially) 'change' others. We also consider that capability types 'change' others (not shown in the model). Based on this, we can derive that a capability potentially changes others according to their types, as explained.

8 We focus on qualitative change but disposition can also create and destroy other, as [62] states.

Fig. 10 Disposition relationship (dynamic aspects)

[FIGURE]

## 5.8 Zooming in on competence

So far, we have considered only human capabilities in a general perspective, in their roles in the makeup of organizational capabilities. Here we zoom in on the makeup of human capabilities, whose descriptions have been expressed often in terms of human skills and competences .

## 5.8.1 Skill and competence definition

Regarding the skill concept, there are some parallels between it and the definitions of competence [14]. Some authors even argue that such concepts have the same meaning in essence. Competence is conceptually considered a skill subtype in some cases [16]. Even among those who believe that competence and skill are distinct concepts, there are many similarities between them. In this sense, both are regarded as human abilities that enable satisfactory task performance [14]. Thus, both skill and competence are inherent abilities in a person, the bearer, that enables the performance of specific action types. That is, they represent an individual's 'knowhow'. Aside from this fundamental similarity, there are other comparable features in the definitions of these concepts. Both are abilities that can be learned (formally or informally) and developed through practice [42, 43]. In this sense, skill and competence can be used to learn new abilities via the transfer mechanism [14, 42, 43]. In terms of structure, there are also some similarities between skills and competences. Both have a hierarchical structure, according to some authors [14, 16]. As a result, they can be aggregated or combined at various levels. Thus, simpler skill/competence forms more complex skill/competence. As a consequence, the complexity of skill and competence can also vary. Another similarity between these concepts is their relationship with the context. Both are associated with a context, environment, area, or domain [14,

[FIGURE]

Fig. 11 Competence-related concepts (in red) with correspondent vertical relationships (in blue)

[FIGURE]

16]. In this regard, competence and skill can be more generic (domain-independent) or more specific (domain-dependent) [14, 16].

## 5.9 Skills and competences as human capabilities

Skills and competences frequently rely on favorable conditions to manifest. That is, skills and competences depend on other properties (internal or external) to manifest themselves more effectively. Knowledge, mental states, attitudes, feelings, and so on can all aid in the proper manifestation of a skill or competence , for instance. Finally, in addition to the aforementioned similarities, some authors argue that skills and competences involve similar domains of an individual. According to them, both are related to the bearer's affective, social, physical (or operational), cognitive, and meta-cognitive domains [3, 14]. In order to capture the common features of skills and competences , we adopt the notion of human capability defined early, in Fig. 6. Based on this, in this work, skills and competences are considered sub-types of the more general notion of human capability , as shown in Fig. 11, which also reveals a number of relations between personal competences, knowledge, skills, attitudes and other human characteristics (beyond human capabilities).

## 5.10 Skills and competences distinctions

In this current work, the main distinction between skills and competences is the structural aspect as revealed by the specialized whole part relations in Fig. 11. So, competences are considered here a complex capability since they can be composed of other capabilities (and dispositions). As a result, competence is composed of knowledge , skills , attitudes , and other human characteristics , whereas skills are formed only byothersimpler skills . In this work, competence is made up of at least one skill that is (horizontally) related to one or more other competence elements (e.g., a skill that is additional to an attitude and to a specific knowledge). As a complex capability , competences can also be composed of others, forming a hierarchical structure. (The distinction between basic and complex competences, presented in [10], is no longer required here, since in this work the complex capability concept was addressed at a more general level.) Likewise, skills can also be a type of complex capability , being also structured hierarchically, in this case. Based on [14], another adopted criterion to distinguish skill from competence is the mode of manifestation. Competence is associated with one or more complex (and contextualized) tasks , whereas skill is associated with a simple task (basic unit of work), as in [14].

[FIGURE]

## 5.10.1 Knowledge, attitude, and (other) human characteristic definition

Knowledge Definition In this context, knowledge is defined as a justified true belief [68]. Knowledge , while assisting in the realization of skills , differs from skills in that it is a static entity registered in the individual's memory. It is related to the person's knowledge of information, facts, and concepts. It is produced as a result of internal (mental) information processing. Skills , on the other hand, manifest themselves through 'external' tasks and are developed through practical experiences. In this way, knowledge , despite representing external facts or concepts, is existentially dependent on the bearer. Individual knowledge , as a type of belief, can be considered a subjective entity that is difficult to measure or quantify, despite the fact that it may have attributes. Furthermore, knowledge is a mental property that is inherent in the individual and can lead to action (e.g., reflections, reasoning, inference). It is manifested alongside other forms of dispositions such as skills to manifest itself in tasks, forming reciprocal or mutual activation partners [49]. Indeed, knowledge , as a disposition type, can have all the relationship types presented above, such as emergenceandresulting (i.e., organizational knowledge from individual's knowledge ), constitutive (i.e., forming knowledge 'bundles'), reciprocal, additional, enabling, disabling, and changing.

## 5.11 Attitudes definition

Despite the fact that it is manifested through actions, gestures, postures, and so on, attitude differs from skills in that it is not manifested through tasks but by behaviors. Attitude , on the other hand, can be task-related. For example, a responsible attitude can be present during a developer's completion of the task of fixing a bug in software; an empathetic attitude can be present during the task of negotiating project scope with the client. Attitude in the context of this work is considered a sub-type of Disposition , because it is a proclivity to act and behave. Again, like knowledge , it is manifested alongside other forms of dispositions , forming reciprocal or mutual activation partners [49] with skills and knowledge. As knowledge , attitudes are subtypes of disposition and can have all the relationship types presented above.

## 5.12 'Other' human characteristics definition

Other human characteristics include objective (or measurable) attributes (e.g., height, sex, age), while others are subjective (non-measurable), such as the individual's traits, character, motivations, worldviews, values, and beliefs. As previously stated, such humancharacteristics are regarded in this work as a subtype of the intrinsic moment . As an intrinsic moment , human characteristics can be categorical (e.g., age, gender, etc.) or dispositional (e.g. personality traits). Based on the categorical base of the disposition [69] and UFOdistinctions, the former contributes to competence activation since is considered part of the competence context ( situation ), as illustrated in Fig. 11, as the derived relationship 'activates.' And, the latter can even be a proper part of the competence . Furthermore, some human characteristics can be included in the competence context, activating the competence manifestation. We also consider that human characteristic types 'activate' competence types (not shown in the model). Based on this, we can derive that a human characteristic potentially activates a personal competence according to their types

## 5.13 Summary

Figure 12 depicts a summary of the proposed ontology , 9 embracing both the zooming-in and zooming-out perspectives presented above. The model focuses on presenting the vertical relationships (in blue) and the horizontal ones (in red) between the proposed concepts, including the UFO concepts (in green). As shown, capabilities ( dispositions ) are activated by capability context ( situation ) and manifested through capability manifestations ( perdurants ). In the vertical perspective, (emergent) capabilities can be 'emerges from' others (including dispositions ) and 'emerges in' a situation (e.g., the relationship between the parts); (resultant) capabilities can be 'results from' others (including dispositions ); (complex) capabilities can have other capabilities as parts; organizational capabilities (those inherent to a social agent ), as a whole capability , can be 'emerges from' or 'results from' (human or other organizational) capabilities ; and personal competences (those inherent to a person ), as complex human capabilities, can have other personal competences , skills , attitudes , and knowledge as parts, besides depending on human characteristics . In the horizontal perspective, capabilities can be 'reciprocal to', 'additional to' others (including dispositions ), besides being 'enabled by', 'disabled by', and 'changed by' other capabilities . As knowledge, skill, and attitudes are dispositions, they can also have these horizontal relationships, besides the model does not make this explicit. For example, knowledge can enable a skill, a skill can change knowledge, knowledge can enable (or disable) an attitude, an attitude can enable (or disable) a skill, and all of them can be additional and reciprocal. In summary, in our ontology, personal competence is composed of interrelated elements.

9 hierarchy relationship to UFO-elements were hidden.

## 6 Well-founded competence representation

Based on the ontological analysis presented in the previous section, we define in this section an ArchiMate language pattern, proposed as a conceptual extension of the ArchiMate metamodel, with no changes to it. This well-founded representation is proposed to allow modeling of competence, its elements (knowledge, skill, attitude), and organizational capabilities in the EA context, supplementing the representation proposed in [9, 10]. We performed three main steps: (i) conceptual mapping , linking concepts from the ontology to ArchiMate constructs, (ii) relational mapping , linking relationships from the ontology to ArchiMate relations, and (iii) viewpoints definition , offering distinct perspectives on the competence models.

Thestrategy to map the ontology to a language pattern was based on an ontology-based representation strategy stated by [70, 71]. According to these authors, to facilitate the understanding of some modeling languages, the visual aspects of the constructs should follow the ontological distinctions behind them. As a result, the authors proposed some guidelines to represent a construct based on UFO distinctions. Besides this, these mappings were carried out following an ontological analysis of the ArchiMate constructs. To perform this, we base on their semantics described in the ArchiMatespecification. For this first version of the representation, our main focus in mapping was the semantic adequacy of the proposed views. Such views were defined based on the competence management tasks to be supported by the representation.

## 6.1 Conceptual mapping

The correspondences between ontology concepts and ArchiMate constructs are shown in Table 1.

As shown in the table: (a) the person concept from the ontology is mapped to the business actor construct (i.e., 'a business entity that is capable of performing behavior' [72]), as in Calhau et al. [9, 10, 73], representing a human being, and related (optionally) to a business role representing the job positions or occupations played by the person; (b) human capability concept ( skill and competence ) is mapped to the capability construct (i.e., 'an ability that an active structure element, such as an organization, person, or system, possesses' [72]), related to a business role construct (representing a person , the bearer) using the ('normal') association relationship, as proposed in [9, 10, 73]; (c) organizational capability is mapped in the same way as human capability, but is related to business actor representing an organizational entity (team, department, group, company, etc.); (d) knowledge is represented by a resource construct (i.e., 'an asset owned or controlled by an individual or organization' [72]) that is related to a capability construct that represents a human capability , or business actor that represents a person (the knowledge bearer); (e) attitude is mapped in the same way as knowledge, to the resource construct related to capability construct, since also represent an asset owned by an individual; (f) humancharacteristic , as an intrinsic moment , is mapped to the more general note construct 'labeling' a person , or a human capability ; (g) capability manifestation concept is mapped to behavioral elements , specifically a business function (i.e., 'a collection of business behavior based on a chosen set of criteria such as [...] competencies' [72]), related to a capability construct representing a human capability , or organizational capability ; (h) task concept is mapped to the business process construct (i.e., 'a sequence of business behaviors that achieves a specific result' [72]) related to a capability construct representing a human capa- bility as in [9, 10, 73] and related to the results of the task (outputs, outcomes, etc); (i) capability context is mapped to the plateau (i.e., 'a relatively stable state of the architecture that exists during a limited period of time' [72]) or location constructs, composed of business roles and business objects related to the (human or organizational) capability manifestation.

[FIGURE]

Fig. 12 An overview of the proposed ontology, with UFO concepts in green, horizontal relationships in red and vertical ones in blue

[FIGURE]

Table 1 Mapping of ontology's concepts to archimate's constructs

| Ontology concept                       | Archimate construct                                          |
|----------------------------------------|--------------------------------------------------------------|
| Person                                 | Business actor, business role (related to business actor)    |
| Human capability skill and competence) | Capability (related to Business actor)                       |
| Organizational capability              | Capability (related to Business actor)                       |
| Knowledge                              | Resource (related to capability/ Business actor)             |
| Attitude                               | Resource (related to capability/ Business actor)             |
| Human characteristic                   | Note (labeling Capability/ Business actor)                   |
| Capability manifestation               | Behavioral element (related to Capability)                   |
| Task                                   | Business process (related to Capability)                     |
| Capability context                     | Location / Plateau (composed of related Structural elements) |

[FIGURE]

ArchiMate intentionally blurs the boundaries between the individual level and the type level, in order to allow users to apply the concepts flexibly. For example, the present specification [72] (version 3.2) says 'Business actors may be specific individuals or organizations; e.g., 'John Smith' or 'ABCCorporation', or they may be generic; e.g., 'customer' or 'supplier'.' Hence, following ArchiMate, these elements can be applied to both individuals and types. This means that the business actor construct could in fact be used to represent a person type ; likewise, the capability construct could be used to represent a capability type , behavioral elements could represent task types , etc.

Table 2 Mapping of ontology's relationship to archimate's relations

| Ontology relat.   | Archimate relationship                                 |
|-------------------|--------------------------------------------------------|
| Reciprocal        | Association relation (with 'reciprocal' label)         |
| Additional        | Association relation (with 'additional' label)         |
| Enabling          | Triggering relation (with 'triggers' label)            |
| Disabling         | Triggering relation (with 'disables' label)            |
| Changing          | Flow relation (with 'changes' label)                   |
| Parthood          | Composition / Association relations                    |
| Emergence         | Realization or Serving relation (with 'emerges' label) |
| Resulting         | Serving relation (with 'results' label)                |

## 6.2 Relational mapping

Correspondences for the relations in the ontology are presented in Table 2.

As detailed in the table: (a) horizontal relationships : (i) the reciprocal relationship is represented using an association relation labeled with 'recriprocal' (with heavy line width) between the reciprocal elements ( capabilities or competence 's elements); (ii) additional relationship is represented in the same way, using the association relation with a light line width and without label; (iii) enabling relationship is represented using triggering relation labeled with 'enable', between the enabler and enabled element; (iv) disabling relationship is represented using triggering relation labeled with 'disable', between the disabler and disabled element; and (v) changing relationship is represented using flow relation labeled with 'change', between the changer and changed element (in the case of horizontal relationships that involve knowledge and attitude, it is used a directed association relation, labeled with 'enable', 'disable' or 'change', since ArchiMate's triggering and flow relationships are not allowed between motivational elements). (b) vertical relationships : (i) parthood relationship is represented using composition and aggregation relation between capability constructs (possibly represented by nesting); (ii) emergence is represented using the serving relation (with heavy line width and labeled with 'emerge'), between the emergent capability and the part's capabilities (that must be interrelated with horizontal relationship), or with realization connected business actors to the emergent capability (used to represent a more complex emergence mechanism). In this case, the emergent capability must represent some novelty concerning the capabilities of parts.; (iii) the resulting relationship is represented using serving relation with heavy line width and labeled with 'result', between the resultant capability and the part's capabilities (the grouping construct of ArchiMate may be used to distinguish the level of the whole and the level of the parts). In this case, the part's capabili- ties must be not related and the resulting capability must not represent a novelty, something new, not present in the parts.

## 6.3 Representation viewpoints

The following viewpoints are defined based on the different relations that competences establish:

1. competence manifestation viewpoint, focusing on a single competence (as a black box) in its context of manifestation;
2. 'zooming-in' viewpoints , including
3. (a) competence elements view, and
4. (b) competence element relationships view, and;
3. 'zooming-out' viewpoints , including
6. (a) competence interaction view and
7. (b) capability emergence view.

The viewpoints of 'competence manifestation' and 'competence elements view' were proposed in [9, 10], while the others ( competence element relationships , competence interaction , and capability emergence ) are the novelty proposed in this work.

All of these viewpoints are related to competence management tasks. Some of the viewpoints also help in connecting competence management tasks with capabilities management tasks, especially in the EA context. Figure13 illustrates how viewpoints support competence management tasks. As illustrated, both competence and capability management have similar steps: identification of the current competences/capabilities, mapping of desired competences/capabilities, and gap analysis ('distance between the current and desired state). Sometimes to achieve a desired capability, it is necessary to develop some personal competences in the organization's employees. Therefore, for this is necessary to perform the task of decomposing an organizational capability into personal competences. Furthermore, to identify current capabilities, it is necessary to first identify current personal competences from employees and then perform the task of composing capabilities. This is shown in Fig.13. As illustrated, through mapping capabilities (desired) it is possible to map personal competences (desired). With zooming-out viewpoints, it is possible to better understand the relationship between skills and capabilities (current or desired), as illustrated, since they support the tasks of capability composition and decomposition. The zooming-in viewpoint, on the other hand, helps with the tasks of composing/decomposing of competences, as illustrated, from/into elements (skills, attitude, knowledge). The great advantage of these viewpoints is that they allow the see capabilities/competences not as simple black boxes. They allow the refinement of them in elements, enabling traceability and thus improving gap analysis. These viewpoints will be detailed below. How the proposed views support each competence management task is summarized in Table 3. As explained, (i) competence element view helps with competence identification, (ii) competence element relationship and competence relationship views help with gap analysis, and (iii) emergence/resulting view helps with competence mapping.

[FIGURE]

Fig. 13 Competence and capability management supporting

[FIGURE]

Table 4 summarizes each of the views and viewpoints proposed in this work, as well as the elements/relationships that make up each viewpoint, the ArchiMate layers involved and the modeling levels included. Next, each of the viewpoints and corresponding aspects will be detailed.

As it will be detailed, all these proposed views can be represented in three distinct perspectives, following ArchiMate's layers:

1. strategic perspective , more abstract and implementationindependent, focused on the description of capabilities and competences in strategic layer in a generic way;
2. business perspective , more implementation-dependent and focused on the representation of capability and com-
3. petence manifestation (through events) in the business layer of ArchiMate; and,
3. merged perspective , integrating strategic and business perspectives, detailing how capabilities/competences are implemented.

Table 3 Proposed views and supported competence management tasks

| Proposed view                    | Competence mgmt.task      |
|----------------------------------|---------------------------|
| Competence elements              | Competence identification |
| Competence elements relationship | Gap analysis              |
| Competence relationship          | Gap analysis              |
| Emergence/Resulting              | Competence mapping        |

[FIGURE]

## 6.4 1. Competence manifestation view

To facilitate the understanding of the views, suppose a scenario in which an organization performed the capability mapping and it was identified that the full-stack development capability of teams must be improved. In this context, to improve this capability, it is necessary to understand better how this capability is 'decomposed' in competences and competence elements, how these competences are interrelated, and how they manifest. Regarding this last aspect, the competence manifestation view aims to represent how personal competence is manifested in its context. Figure14 depicts an example of competence's manifestation view, focusing on the manifestation of 'Front-end Development Competence' (a competence related to the full-stack development capability). As shown, this personal competence characterizes the front-end developer, a business role. As depicted, the manifestation of this competence is represented in two forms: using business process and business function constructs. The former represents the manifestation focusing ontheresults and achievements, a.k.a 'result-oriented' manifestation. For example, as depicted, 'Front-end Development Competence' can be manifested through the 'implement client web form' task. On the other hand, the latter represents a manifestation focused on the implementation of the competence and its elements (based on operational aspects). As illustrated, for example, 'Front-end Development Competence' can be manifested through the 'React Front-end development' behavior.

In order to be activated, the competence's bearer must be in a proper competence context , the 'Front-end Developer Workplace' in this case. The competence context is represented using a location construct and, as it is shown, must be composedofanIntegratedDevelopmentEnvironment(IDE). Besides representing the context, it is also possible to represent how the competence is manifested. As depicted, the task 'implement client web form', performed 'focusedly', has as input the 'client web form prototype' and the 'requirement' artifacts and has as output the 'client web form', part of the 'Web System', with 'field validation', 'responsiveness', 'stylishness' and 'accuracy' characteristics ( moments ).

## 6.5 2. Zooming-in Viewpoints

(a) Competence Elements View The competence elements view aims to represent the parts of personal competence. Figure15reveals the elements of 'Front-end Development Com- petence'. To contextualize, we are considering that this view was modeled to identify the current competence elements andsupportthecompetenceidentificationactivity in the CoM context. As depicted, 'Front-end Development Competence' is formed by (i) skills such as 'requirements understanding', 'understanding back-end (BE) code', 'technology learning skill', and 'front-end (FE) coding'; (ii) attitude as 'effectiveness' and 'malleability'; and (iii) knowledge as 'requirement types' and 'IU heuristics'. In this view, competence and its elements can be detailed in distinct levels. For example, 'FE coding' could be considered a complex skill composed of other (soft or hard) skills, such as 'CSS coding' or 'HTML coding'. The granularity of this detailmentdepends on how much implementation-independent the modeler wants the capabilities. In this example, in order to illustrate a possibility, we preferred to represent the competence and its elements more abstractly. So, we preferred to represent the implementation-related details (i.e., Front-end technologies) as manifestations of the 'FE Coding Skill' (using the elements of the Business layer). This is illustrated in Fig. 15 through the business f unction construct. As depicted, in this case, 'Front-end Development Competence' can be manifested through the 'React Front-end Development' action. As depicted, this action is composed of sub-actions such as 'React 18 coding', 'CSS3 coding', and 'HTML5 coding'. In addition, we also detailed the 'result-oriented' manifestation of the 'Front-end Development Competence'. It is represented through the 'implement client web form' task in Fig. 14. As depicted, this manifestation is formed by subtasks related to the development of a web form: 'code fields', 'code (the fields) validation', and code(the) style (of the form)'. One important aspect is that, in this example, we separated more explicitly the strategic and business perspectives of ArchiMate. However, they could be represented in a mixed way as well, as we will illustrate later.

Table 4 Proposed viewpoints, related elements, and archimate's layers

| Level         | Type/ Individual            |                    |                  | Type/ Individual    |                         |                        | Type/ Individual             |                   |                       | Type/ Individual         | Type/ Individual                        |
|---------------|-----------------------------|--------------------|------------------|---------------------|-------------------------|------------------------|------------------------------|-------------------|-----------------------|--------------------------|-----------------------------------------|
| Layers        | Business                    |                    |                  | Strategy/ Business  |                         |                        | Strategy/ Business           |                   |                       | Strategy/ Business       | Strategy/ Business                      |
| Relationships | Competence ←→ Manifestation | Competence ←→ Task | Task ←→ Artifact | Competence ←→ Skill | Competence ←→ Knowledge | Competence ←→ Attitude | Skill ←→ Knowledge           | Skill ←→ Attitude | Attitude ←→ Knowledge | Competence ←→ Competence | Competence ←→ Organizational Capability |
| Viewpoint     | Manifestation               |                    |                  | Competence element  |                         |                        | Competence element relations |                   |                       | Competence relationship  | Emergence/ Resulting                    |
| View          | General                     |                    |                  | Zooming-In          |                         |                        | Zooming-In                   |                   |                       | Zooming-Out              | Zooming-Out                             |

[FIGURE]

Fig. 14 Example of competence manifestation view (business perspective)

[FIGURE]

Fig. 15 Example of competence elements view in Competence Mapping context (strategic and business perspectives)

[FIGURE]

[FIGURE]

Fig. 16 Example of competence element relationships view in Competence Identification context (strategic perspective)

[FIGURE]

Another important aspect to be highlighted in this example is that competence parthood can reveal the elements' context of manifestation. In this case, the competence manifestation (tasks, artifacts, and their characteristics) can be represented following a similar structure and vice-versa.

## (b) Competence Element Relationships View

Further detailing can be provided in the competence element relationships viewpoint, revealing how the elements are 'integrated' through their horizontal relationships. Figure16 illustrates an example of the use of this viewpoint by focusing on the relationships between 'Front-end Development Competence' elements. In this scenario, as in Fig.15, we also considered that this view was modeled to support the competence identification, in the CoM context. So, the model presented in Fig.16 also represents the current stage of this competence in the organization. However, in this case, the competence elements were related to understanding better how they can be combined.

As shown, (i) 'technology learning skill' changes the 'FE coding skill' since it can modify some qualities of this skill such as its proficiency level; (ii) 'requirements understanding skill' enables his 'FE coding skill' since by understanding the requirements the developer can perform the latter skill; (iii) 'FE coding skill' is additional to 'understanding BE code skill', since this allows the development of front-end code connected with the back-end; (iv) 'FE coding skill' is additional to 'effectiveness' attitudes, since their manifestations can be combined; (v) 'requirements understanding skill' is additional to 'requirements (types) knowledge', since their manifestations can be combined; and finally (vi) 'malleable' attitude can disable the 'effectiveness' one since the manifestation of the former can harm the manifestation of the latter.

Figure 17 illustrates an example of how zooming-in viewpoints can be used to help with gap analysis of a business role or actor. As illustrated, it is possible through the zoomingin to identify which elements differ in a current competence compared to the desired one. In the case of the example, in the current stage of this organization, the front-end developer actor/role does not properly have the 'active listening' and 'self-organization' attitudes. Furthermore, it is possible to identify through the model that, in the current state of competence, there is an attitude (malleability) that blocks the 'effectiveness attitude', inhibiting the performance attitude related to the 'FE coding skill.' Therefore, it is necessary to develop new skills and attitudes in order to remove this 'barrier' from the front-end developer so that he can achieve the desired competence. In the example, the (desired) 'selforganization attitude' would play this role, disabling the malleability in this context and, as a result, contributing to the 'effectiveness attitude' manifestation.

## 6.6 3. Zooming-out viewpoints

(a) Competence Interaction View Besides understanding how competences can be decomposed and how their elements can be related, it is fundamental for an organization to understand how competences from distinct actors/roles can be combined/integrated. In this sense, the following view concerns the representation of the competence relationships in an organizational context; in this view, the focus is on the ways that the competences of different actors interrelate. To illustrate, suppose in our example that the back-end and frontend developers must work together as members of a software development team. In this case, they must have a collabora- tive relationship in the software development context in order to develop together. However, this collaboration is only possible because of the relationships between their competences , allowing them to interact. As depicted in Fig. 18, their competences 'front-end development competence' and 'back-end development competence' have additional skills , such as 'FE coding skill' and 'BE coding skills' (since their results can be aggregated), and also reciprocal skills , such as 'understanding BE code skill' and 'explaining BE code skill'; and explaining 'FE coding skill' and 'understanding FE code skill', allowing the interaction between the developers.

Fig. 18 Example of capability interaction view (strategic perspective)

[FIGURE]

(b) Capability Emergence View The last view concerns the representation of emergent and resultant capabilities and reveals how they are grounded on other capabilities (by emerging from or resulting from these capabilities). Figure19 illustrates this view showing the Software Development Team capabilities that are grounded on team member competences and skills. In this example, the 'full-stack capability' of the team emerges as a consequence of 'frontend development competence' and 'back-end development competence' interrelationships, from its members. As it is illustrated, this emergent capability characterizes the software development team. Besides the emergent capability, there is also a resultant capability that inheres in the software development team, named 'technology learning capability', that resulted from the 'sum' of 'technology learning skills' of developers. As depicted, differently from the emergence representation, in this case, the resultant capability is not based on interrelated capabilities / competences . In the case of this example, as depicted in Fig. 19, we merged the strategic and business perspectives of ArchiMate. As a result, competences and capabilities (constructs from the strate- gic perspective) are represented inside the correspondent business actors (constructs from business perspectives). This representation can be useful to facilitate the understanding of the emergence phenomenon, helping with the capability composition/decomposition task, in the capability mapping context. In this case, if the modeler prefers/needs to separate better these perspectives, he/she can model the capability emergence view in a more separated way, as Fig.15.

[FIGURE]

Fig. 17 Example of competence element relationships view, in Gap Analysis context (strategic perspective)

[FIGURE]

Fig. 19 Example of capability emergence view (merged perspective)

[FIGURE]

## 7 Capabilities in spotify

To show the benefits of the pattern language, we have applied it to a real-life case study from the literature addressed originally by Bäcklander [21] (but also concerning other references related to the case [21, 74-76]). This case study concerns the Spotify company, a well-known Swedish audio streaming (music and podcasts) and media services provider. The study conducted by Bäcklander [21] focuses specifically on understanding (1) how adaptability and related capabilities (e.g., self-organization, learning, collaboration, etc.) emerge in the company, and (2) how the agile coach position contributes to these capabilities. The author of that work performed an ethnographic study inside the company, observing and interviewing the agile coaches. The interviews were conducted using a theory-based code, with codes based on complexity leadership theory . After the interviews, the author identified the main characteristics, practices, interactions, and motivations of the agile coaches that contribute to the emergence of these organizational capabilities.

## 7.1 Spotify's structure

The Spotify company is well-known for having a unique structure, which distinct authors describe [21, 74-76]. Its general structure is depicted in Fig.20. It is composed of guilds (e.g., 'testing guild' and 'web technology guild') and tribes (e.g., 'music player tribe', and 'back-end infrastructure tribe'). Guilds represent cross-cutting study groups focused on employee development and which anyone can join. On the other hand, tribes are like a community of teams focused on the development of solutions.

[FIGURE]

Fig. 20 Spotify organizational structure representation (business perspective)

[FIGURE]

Tribes are also formed by chapters, as illustrated in Fig. 20. They are 'local' study groups (e.g., database chapter, testing chapter) that anyone can join, similar to guilds but restricted to a tribe. In this case, while tribes and squads are resultoriented (focused on the development of software) and highly coupled groups, guilds and chapters are learning-oriented and loosely coupled groups. Each tribe is formed by a tribe leads (e.g., 'music player tribe lead') and by squads, or teams, (e.g., 'android client squad' and 'IOS client squad' in the 'music player tribe'; 'recommendation squad' and 'payment solution squad' in the 'back-end infrastructure tribe'). Each squad has members (e.g., developers, testers, UX designers, etc) and is related to a product owner (PO). Besides this, in the case of Spotify, each tribe has its agile coach (e.g., the 'music player agile coach' of the 'music player tribe') supporting the squads and developers of each squad.

## 7.2 Agile coach role

In the Spotify company, agile coaches are an evolution of the scrum master position. They do not function as managers, but, as the author reports, they have a kind of 'enabling leadership' that balances formal and non-formal practices to create an adaptative space in the company. Agile coaches have two main goal outcomes [21]: (i) to help the squads and keep improving them and (ii) to enable their productivity. According to the author, these goal outcomes are the result of some 'team states indicating adaptative systems': (i) sense of ownership, (ii) focus on values (not solution); (iii) action orientation ('team is biased to action'); (iv) frequent and open communication, and; (v) fun and friendly atmosphere. Based on the agile coach's goals, Bäcklander [21] identified what she termed as the main 'practices' of agile coaches in Spotify. A description of these 'practices' is detailed in Table 5. For each practice of the agile coach (AC), the author exemplifies and also mentions attitudes and quotes from distinct agile coaches, representing real situations they passed through. For example, as the table shows, regarding the practice of 'increase sensitivity to context', one agile coach experienced this by 'encouraging paying attention to context and considering what others understand', another by 'encouraging considering consequences on others', and another by 'getting people to understand each other's different perspectives better.'

## 7.3 Zooming in on the agile coaching competence

After the competence manifestation viewpoint, in this section we will focus on the zooming-in viewpoint, representing the elements of 'agile coaching competence' based on the agile coach's practices identified by Bäcklander [21] and described in Table 5. The textual representation of the agile coach's competences in the case study was used as input for the zooming-in modeling; however, the application of the patterns in an explicit EA model has several benefits when contrasted to the original textual description. For example, some elements described in this model had not been explicitly mentioned in the text, but surface here as the EA model serves as a frame of reference for details to be added. Besides this, in the original study, the agile coach competences were not aggregated explicitly into complex capabilities. The relationships between competences and their elements were not described either.

## 7.4 'Agile Coaching Competence' Element Relationships (General) View

Fig.21 depicts the 'zooming in" perspective of the 'agile coaching competence' based on the proposed language pattern, clarifying its elements' relationships.

Based on the agile coach's practices identified in the case study, we established the agile coach's elements that form his competence. To facilitate and improve the representation of the practices presented in Table 5, the agile coach's competences were 'organized' into three main complex capabilities, as shown in Fig.21: (i) 'consulting competence'; (ii) 'facilitating competence'; (iii) 'teaching competence', and (iv) 'coaching competence'. In this case, the intent of this summary is to increase the abstraction level of the representation and improve understanding of the agile coach's competences. To guide this modeling, we also used the Agile Coach Career Framework from Spotify [77, 78] to structure the agile coach competences. As Fig. 21 depicts, one of the main distinctions between the case study description and this representation is the relationship between the competences. As shown, the competences that form the complex competence 'agile coach competence' are related as 'additional'. In this case, this means that their manifestation can be added in distinct circumstances.

## 7.5 'Agile Coaching Competence' Elements Relationship (Detailed) View

Fig.22 shows how these presented elements of the 'agile coaching competence' can be decomposed.

As depicted, (a) 'consulting competence' is formed by (i) 'principles dissemination skill' (practice c in Table 5), (ii) 'context-sensitivity encouragement skill' (practice a in Table 5), (iii) 'agile principles attitude', (iv) 'contextsensitivity attitude', and (v) 'knowledge about the organization'; (b) 'facilitating competence' is formed by (i) 'dialog facilitation skill' (practice f in Table 5), (ii) 'leader boosting competence' (practice b in Table 5), (iii) 'leadership attitude', and (iv) 'making information explicit' (practice e in Table 5); (c) 'coaching competence' is formed by (i) 'asking skill', (ii)'feedback giving skill', and (iii) 'squad observation skill' (practice d in Table 5). Concerning the relationships, most of the relationships are additional, as shown in Fig.21, as for example, 'principles dissemination skill' is additional to 'context-sensitivity encouragement skill' and to 'agile principles attitude'.

## 7.6 'Context-Sensitivity Encouragement skill' Elements Relationship View

Fig.23illustrates further 'zooming-in', focusing on 'contextsensitivity encouragement skill'. As described in the case study, this skill concerns practices such as (i) 'whole perspective dissemination skill'; (ii) 'organizational mission sensitizing skill'; (iii) 'self-reflection stimulation skill'; and (iv) 'empathy encouragement skill'. As shown in the figure, these practices were considered skills that form 'context sensitivity encouragement skill' and some of these skills are considered additional to others and on some attitudes. In this context, the 'whole perspective dissemination skill' is additional to 'holistic values' (represented as an attitude) and the 'empathy encouragement skill' is additional to 'empathy' attitude, since these attitudes potentialize the manifestation of those skills.

## 7.7 Zooming out on agile coaching competence

The emergence phenomenon in Spotify is one of the main aspects explained in this case study, even because Bäcklander [21] considers complex and adaptive system theory as a foundation. As a result, Spotify is seen by the author as a complex system that belongs to a changeable environment.

[FIGURE]

Table 5 Agile Coach's (AC) main practices descriptions based on Bäcklander [21]

| Practices                                                                                                  | Examples                                                                                                                                                                                                                                                    | Illustrations                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (a) Increase sensitivity to context                                                                        | 1-on-1 coaching about how to think, what to consider; at any time it seems prudent, encourage to consider the consequences of one's actions as individual and team, their impact on others, consider that others may not know what you know, and vice versa | 1) [AC] encouraging paying attention to context and considering what others understand 2) [AC] encouraging considering consequences on others 3) [AC] getting people to understand each other's different perspectives better 4) [AC] describing a conflict episode; |
| (b) Boost and support other leaders in the team, particularly the PO                                       | Work with PO; Coach PO how to lead, how to be a PO; How to lead in the Swedish setting; Helping CL prepare for difficult conversations                                                                                                                      | 1) [AC] working with a part of the organization deemed as troubled, with no teams, no teamwork, and many interpersonal conflicts 2) [AC] helping Chapter Leader conflict                                                                                             |
| (c) Establish and remind of simple principles, interpreted locally                                         | Some of the principles: 'Value first'; 'Function over form'; 12 principles of agile manifesto; Action bias; How people interact -higher band width is better, i.e. face to face. Interact with respect and receptiveness                                    | 1) [AC]reinforcing the focus on value and function over form as 'simple rules' 2) [AC] reinforcing the simple rule of action                                                                                                                                         |
| (d) Observe team, pay attention to dynamics, and monitor                                                   | What is observed: Mood of team; Helping behaviors; Smiling; Talking; Being civil toward each other; What is not said; Team members mentally present; Patterns, like failing to deliver using certain planning method                                        | 1) [AC] mentions observation as important and common/What is observed (mood, things going well) 2) [AC] describing observing negative team                                                                                                                           |
| (e) Make the un- seen more visible and tangi- ble (sur- facing conflict) through mirroring and questioning | Visualizations of work and work process, e.g. using boards, sticky notes, digital visualizations. The retrospective meeting itself. Va- rious agile games                                                                                                   | 1) [AC] on surfacing through questions                                                                                                                                                                                                                               |

[FIGURE]

## Practices

## Examples

(f) Facilitate and encourage cons- tructive dialog as the generator of new forms

Fig. 21 General representation of 'agile coaching competence' (strategic and business perspectives)

[FIGURE]

Fig. 22 Detailed representation of 'agile coaching competence' (strategic perspective)

[FIGURE]

- Setting a format; 'Tossing' an open question; Live directing (calling on people); Acting as a surrogate (asking'stupid questions'); 1-on-1 coaching to instil civil and constructive ways of interacting

## Illustrations

- 1) [AC] describing the constructive dialog dynamics they are looking for
- 2) [AC] describing that when teams are really good at constructive dialog, they themselves do not even have to be there anymore

Fig. 23 Zooming-in on 'context-sensitivity encouragement skill' (strategic perspective)

[FIGURE]

In this case, the work explains how agile coaches play a special position since they contribute to the emergence of some capabilities, especially the adaptability and evolution of Spotify. As an outcome of the study, the author concludes that the adaptability capability emerges due to two main leverage point: increasing the context sensitivity (that improve the quality of communication and solutions) and the relevance of information in the context (that stimulate learning and reflection). The author also associates adaptation and evolution capabilities with collective learning, open dialog, creativity capabilities, and so on.

The author also discusses how innovation and adaptability in an organization or a team are a result of individual competences/skills e.g., sharing, discussing, reflecting on knowledge and actions, questioning, and so on. This way, members of teams must constantly debate, think critically, and share opinions in order for the team to be adaptable. However, the author points out that such kind of behavior can be challenging: 'Team learning behaviors are not automatic, as they can be personally risky. For example, sharing an idea or criticizing someone else's idea means taking interpersonal risk' .

Werepresentedthis'interaction dynamic' that contributes to the learning and adaptability emergence by using the competence interaction viewpoint . Figure 24 represents two team members interacting. To facilitate the understanding of this dynamic, we mixed the strategic and business perspectives. As shown in the figure, both team members self-develop through the 'learning skill', a skill enabled individually by their own 'reflection skill'. However, through their interaction, the team members mutually enable their 'reflecting skill'. As depicted, their 'reflection skill' is also enabled by their 'discussion skill', a reciprocal skill. As the figure represents, 'discussion skill' is also mutually enabled by the 'opinion sharing skill'. This means that, when one team member shares an opinion, this enables discussions in the group. So, as discussed before, 'opinion sharing skill' is central to allowing collective learning and adaptability in a team.

[FIGURE]

Fig. 24 Competence interaction view: interaction between team members in spotify (merged perspective)

[FIGURE]

So far, this explanation of the diagram focuses more on howthe 'self-development competence' is mutually enabled bythe interaction between team members, in a positive sense. However, as aforementioned, the bottom of the diagram also depicts how the team members can also 'disable' each other. In this instance, the critical sense attitude from each team member can block (disable) the manifestation of 'opinionsharing skills' from the other one. For example, since team members are very skillful regarding opinion sharing, discussion, reflection, and so on, if they have high criticism, they can inhibit the manifestation of other skills. Nonetheless, as is illustrated, this 'disabling effect' can also be decreased by the 'empathy attitude.' In summary, if these skills are not properly balanced, and even if a team has very skillful members, they will not collectively learn and adapt. Even if the members have high individual 'learning skills,' this does not imply that the team will learn together and be capable of adapting properly.

Thus, because of this complexity regarding team interaction, the support of agile coaches is critical for collective learning to emerge. As stated by Bäcklander [21], an emerging dynamic of learning behavior can be supported by proper leadership support, the agile coach in this case. The author also confirms the value of leadership in encouraging positive team dynamics is considerable. In the case of Spotify, the author details how collective learning happens and how an agile coach supports this by describing a kind of 'emergence pattern', explaining how team learning behavior emerges. In this emergence pattern, the agile coach acts as an 'enabling leader', as a facilitator, in order to stimulate desired behaviors, attitudes, and skills such as empathy, sensitivity to the context, and sharing of opinions, among others; and discouraging not desired attitudes as well. As a result, according to the study case conclusions, adaptability in Spotify is basically a result of the agile coaches acting as 'enabling leaders' and creating adaptation spaces in the company.

Fig. 25 Competence interaction view: interaction between team member and agile coach in spotify (merged perspective)

[FIGURE]

[FIGURE]

This dynamic is shown in Fig.25, a representation that better details how agile coaches act as 'enabling leaders' in a practical sense in Spotify. As depicted, agile coaches enable the desired competences, skills, and attitudes of team members. Regarding this specific emergence pattern, the agile coach enables each team member to manifest more: (i) 'opinion sharing skill', through 'sharing encouragement skill', and; (ii) 'empathy attitude', through 'empathy encouragement skills.' Besides not being shown, the agile coach could also have skills related to the discouragement of certain attitudes for a specific context, for example, the excess of 'critical sense' during team discussion.

Fig. 26 Emergence View: how adaptability emerges in spotify (merged perspective)

[FIGURE]

## 7.8 Tribe's adaptability emergence

As a result of the emergence of the team learning capability in each squad, stimulated by the agile coach, the adaptability of the tribe also emerges. This is illustrated in Fig. 26. It shows the general view of the adaptability emergence pattern, based on the competence interaction viewpoints shown before. As a consequence of these interactions, the adaptability of the whole company emerges, as illustrated in the figure. As in this case, the emergence does not happen due to one specific cause but through the interaction between the team members and agile coach (and their competences), we represented that team learning capability emerged from these interactions by using a realization relationship. Besides not shown in the diagram, the learning capabilities of the guilds also contribute to the emergence of adaptability in Spotify. As explained by the authors, guilds are learning communities where the members share knowledge, have discussions, and promote events as workshops. They also have a practical approach since they try to solve common problems and establish patterns for the organization. The figure also illustrates briefly the emergence of technical capabilities in Spotify, the 'software development capability,' however, this is not the focus here.

[FIGURE]

## 8 Empirical evaluation of the competence representation

Asaformofearlyempirical assessment of the proposed competence representation, we performed a survey to stakeholders. The main objective of the survey is to verify the potential usefulness of the representation and find out whether the stakeholders are predisposed to using it to model competences and human capabilities in the EA context, mainly concerning capabilities-based practices. Among these practices, we considered mainly: (i) competence/capability traceability; (ii) competence/capability composition and decomposition, and; (iii) competence/capability gap analysis. For such, this survey was elaborated using guidelines of the technological acceptance model (TAM) [22]. In this first evaluation of the proposed competence representation, we are mainly interested in basic determinants of technology acceptance. As a result, at this moment, it is not the intention to consider distinct factors related to cognitive processes, social influences, or environmental impact. So, concerning this (and also the suitable complexity level), we chose the original TAM [22] for our study instead of newer versions (i.e., TAM2 and TAM3).

The main assumption here is that stakeholders are prone to use the proposed competence representation to support the aforementioned capability-based practices. The target public was formed by professionals from the academy, government, and industry with experience with EA, enterprise modeling, and/or ArchiMate as well. In this case, the expectation is that they think that the proposed competence representation is applicable in the mentioned context. In order to understand this, the supposition is that they think the representation has important characteristics that allow its application, such as ease of understanding, versatility/adaptability, and good organization/structure. Another expectation is that they think that the representation can impact positively their work related to EA. This means that the representation has the potential to improve the understanding for problem-solving, quality of decisions, and quality of communication in capability-related activities.

In order to evaluate these aspects, the original TAM model has the main variables of interest to understand if the stakeholders are prone to use the competence representation. Basically, in the original TAM, the users' intention of use ( I OU ) of some technology is influenced by two variables: perceived ease of use ( PEOU ) and perceived usefulness ( PU ). Besides this, these variables have an influence relationship. In this case, the PEOU can influence the PU , and the PU can influence I OU . In the original TAM, the authors also consider other variables such as the 'actual usage' and 'attitudes toward use', not considered here. Besides applying TAM, we also evaluated the understanding of the proposed competence representation.

[FIGURE]

## 8.1 The survey elaboration

The survey was elaborated into four parts: (i) a description of an organizational scenario with a competence-based representation elaborated using the elements and relationships described in this paper; (ii) questions aimed at assessing the participant's ability to retrieve information about the traceability of competences into organizational capabilities; (iii) questions aimed at assessing interpretation and understanding , and; (iv) TAM survey questions, concerning the three variables mentioned above: PEOU , PU , and I OU .

We have employed the Spotify scenario presented in Sect. 7, specifically in Fig. 26. We presented the model using the distinct viewpoints proposed in this work with a short textual description and a figure legend explaining the main relationships.

Questions about traceability were aimed at assessing the understanding of the competence representation and the zooming out task in survey answering, and to correlate this data with the TAM result. In these questions, we asked which competences/capabilities would be impacted directly and indirectly by the development of the agile coach skills (Sharing encouragement skills and teaching skills). In order to understand the impact of traceability understanding, we created four questions (two about direct impact and two about indirect impact) asking participants to list the impacted competences/capabilities following the improvement of agile coach skills. The impacts of 'Sharing Encouragement Skill' improvement were the subject of two of these questions (one for the direct impact and another for indirect impact), while 'Teaching Skill' improvement was the subject of the other two (one for the direct impact and another for indirect impact). We gave the participants the option to choose any of the competencies, attitudes, or capabilities depicted in the model for each question as an impacted element. We estimate the model's accuracy based on the responses by computing the precision and recall for each question. An F 1score,which combines these two measures was used to determine accuracy. Each participant's overall accuracy was determined by taking the simple average of their four calculated F-scores.

Concerning the 'understanding' questions, we provided three questions which, unlike the traceability questions, required extrapolating some implications from the information directly represented in the model. More specifically, the participants should comprehend the emergence patterns (related to the zooming out task) depicted in the model to declare whether they agree with a statement about the model. There were two incorrect statements (with which the participants should disagree), and one correct statement. We used a Likert scale [79] of one to five for the participants to declare agreement with each statement (participants could skip questions; we have discarded responses of those who skipped all three questions; otherwise, if one or two were skipped, we considered these equivalent to 'neutral' in the Likert scale). The scores of agreement with the incorrect statements were reversed and the final score was determined by taking the average. One of these questions concerns how the 'team learning capability' develops. Figure 26 shows that team members' 'opinion-sharing skill' is disabled by their 'critical sense attitude'. In contrast, the 'empathy' attitude prevents the 'critical sense attitude' from manifesting while indirectly promoting the 'opinion-sharing skill' manifestation. As a result, the agile coach must encourage the manifestation of 'empathy' for this to occur properly. So, we asked whether the participant agreed with the statement that improving the Agile Coach's Teaching Skill and Sharing Encouragement Skill is not enough for Team Learning Capability to emerge, without considering the Empathy Encouragement skill .

The TAM evaluation was the focus of the survey's final section. As mentioned, the TAM survey was focused on three variables: (i) perceived ease of use ( PEOU ), (ii) perceived usefulness ( PU ), and (iii) intention of use ( I OU ). Weused 13, 14, and 3 questions, to assess PEOU , PU , and I OU , respectively. The PEOU questions were designed to determine whether the representation was considered: (i) well-organized, (ii) adaptable, (iii) error-prone, and (iv) intuitive (i.e., ease to read, interpret, learn from, and comprehend). The PU questions were designed to assess whether the competence representation was deemed useful in the support of practical EA-related tasks (especially related to capabilitybased practices) -such as (i) improved comprehension (for problem solving), (ii) decision-making, (iii) performance (i.e., effectiveness), and (iv) expressiveness (i.e., communication). The purpose of the I OU questions was to assess the interest in and motivation to use the proposed competence representation.

ALikert scale was used for all of these questions, ranging from one to five, or 'completely disagree' to 'completely agree'. In order to prevent bias, the questions about the suggested competence representation alternated between those that make a positive statement (e.g., 'the representation is easy to understand') and those that make a negative statement (e.g., 'the representation is error-prone'). In order to aggregate the results concerning statements that were formulated positively with those that were formulated negatively, the answers for the latter were reversed accordingly. Average and standard deviation were calculated for each variable ( PEOU , PU , and I OU ) in order to determine the final result.

## 8.2 Application and results

Regarding the sample, we focused on two main audiences: academics (EA researchers) and practitioners. Concerning the identification and selection of the academic samples, it was more systematic. Academics were identified and contacted through a contact list (for known researchers, and collaborators) and also through a search on Google Scholar, selected by the area of EA. In this search, the fifty most cited in the EA area were considered, and from the profile on Google Scholar, the professional page and e-mail were identified. So, EA researchers were informed about the survey basically by e-mail. On the other hand, concerning practitioners, the sample was defined more randomly, as the participants were those who responded to open and public messages sent on different LinkedIn forums with the themes of EA and ArchiMate.

As a result, we received 29 responses, out of which 52% were from the academic community, 34% from the industry, and 14% from the government. The participants from the industry and government (48%) were aggregated into a category of 'practitioners'. In total, 41% of the participants had more than ten years of experience in enterprise modeling, 21% had five to ten years, 24% had three to five years, and 14% had less than a year of experience. About 44% of participants in general had no prior experience with capability modeling in ArchiMate, while 56% did. We eliminated two responses whose respondents skipped all of the traceability and interpretation questions. As a result, out of the 29 responses, 27 were analyzed.

Table 6 lists the results of this survey. Results are presented across groups divided orthogonally based on two criteria: (i) sector , and (ii) experience in enterprise modeling. According to the sector criterion, we defined two disjoint groups: academics and practitioners (professionals from industry and government). According to the experience criterion, we defined two disjoint groups: more experienced professionals (who reported 10 years or more of experience with enterprise modeling) and less experienced professionals (with less or equal to 10 years of experience).

The following indicators were averaged ( av. column) for each group in the table: information retrieval (F1-score), understanding ( UDT ), perceived ease of use ( PEOU ), perceived usefulness ( PU ), and intention of use ( I OU ). We also provided the standard deviation (s.d.) for these indicators. Concerning the TAM variables ( PEOU , PU , and I OU ), we also applied an adapted version of the Net Promoter Score ( NPS ), a metric to rate the likelihood of each variable [80]. To calculate this, we considered, for each question, the number of promoters (i.e., those that 'totally agree' or 'agree' with 'positive' statements; or, 'totally disagree' or 'disagree' with 'negative' statements) minus the number of detractors (i.e., those that 'totally agree' or 'agree' with 'negative' statements; or, 'totally disagree' or 'disagree' with 'positive' statements). Neutral answers are disregarded in the NPS calculus. To be acceptable, the NPS should be more than zero. In Table 6 we show the average of the NPS for each question.

[FIGURE]

Table 6 Results of the Empirical Evaluation of the Competence Representation

| Group        |   F1 (0-1) | F1 (0-1)   | F1 (0-1)   | UDT (1-5)   | UDT (1-5)   | PEOU (1-5)   | PEOU (1-5)   | PEOU (1-5)   | PU (1-5)   | PU (1-5)   | PU (1-5)   | IOU (1-5)   | IOU (1-5)   | IOU (1-5)   |
|--------------|------------|------------|------------|-------------|-------------|--------------|--------------|--------------|------------|------------|------------|-------------|-------------|-------------|
|              |            | av.        | s.d.       | av.         | s.d.        | av.          | s.d.         | nps          | av.        | s.d.       | nps        | av.         | s.d.        | nps         |
| ACADEMIA     |         14 | 0.7        | 0.2        | 3.5         | 1.2         | 3.0          | 0.7          | -0.2         | 3.8        | 0.6        | 5,9        | 3.5         | 0.5         | 0.4         |
| PRACTITIONER |         13 | 0.5        | 0.2        | 3.0         | 1.2         | 3.3          | 0.7          | 3.1          | 3.1        | 0.7        | 2.2        | 3.0         | 0.6         | - 2.4       |
| ≤ 10 YEARS   |         16 | 0.6        | 0.2        | 3.5         | 1.1         | 3.4          | 0.7          | 3.5          | 3.7        | 0.7        | 5.2        | 3.6         | 0.5         | 0.1         |
| > 10 YEARS   |         11 | 0.6        | 0.2        | 2.9         | 1.4         | 2.7          | 0.8          | - 1.7        | 3.1        | 0.6        | 2.5        | 2.7         | 0.5         | -2.4        |
| ALL          |         27 | 0.6        | 0.2        | 3.2         | 1.2         | 3.1          | 0.8          | 1.2          | 3.4        | 0.6        | 4.0        | 3.2         | 0.5         | -1.1        |

To facilitate analysis, we also calculated for each group the percentage of: (i) unfavorable perception (or intention, for I OU ), (ii) neutrality, and (iii) favorable perception (or intention, for I OU ), for each variable of the TAM. We consider 'favorable' perception (or intention) when the respondents marked 4 or 5 ('agree' or 'totally agree') in the case of 'favorable assertions' (e.g., 'the representation is easy to understand') or when they mark 1 or 2 ('disagree' or 'totally disagree') in the case of 'unfavorable assertions' (e.g., 'the representation is error-prone'). Neutrality corresponds always to 3 in the numeric scale). And 'unfavorable' perception is the converse of 'positive' perception.

## 8.3 Accuracy (F1) and understanding (UDT) results

Comparing academics and practitioners, the accuracy ( F 1 score) in traceability retrieval was highest for the academics, with about 0.7, against 0.5 for the practitioners. Interestingly, the level of experience did not correlate with accuracy and both groups of (more and less experienced) respondents scored about 0.6.

Concerningthe'understanding' questions, academics also scored better than the practitioners (3.5 as opposed to 2.9.) Interestingly, the same can be said for less experienced respondents (who also scored 3.5 as opposed to 2.9).

## 8.4 Perceived ease of use (PEOU) results

Regardingthesectordivision, the practitioners had the largest portion of favorable respondents concerning perceived ease of use ( PEOU ), with 51% answering positively to this criterion, as Fig. 27 shows. Concerning unfavorable answers to PEOU , it was most pronounced among the academics, with 32%. Despite this, academics had a very balanced result overall, with 35% neutral and 32% favorable. Regarding the subdivision between less and more experienced respondents, the first group had the largest proportion of favorable responses (49%). It is noteworthy that 44% of the more experienced respondents were unfavorable with respect to PEOU , and only 20% of the less experienced had an unfavorable perceived ease of use.

[FIGURE]

Fig. 27 Perceived ease of use's results

[FIGURE]

## 8.5 Perceived usefulness (

PU ) results Between academics and practitioners, the first group had the most favorable perceived usefulness, with about 57% favorable answers, as shown in Fig. 28. They also had a considerably lower unfavorable perceived usefulness, with about 8% negative answers. This value was more than three times lower than the practitioner's unfavorable answers on perceived usefulness (25%). Despite this, practitioners' favorable perceived usefulness and neutrality were considerable, with 41% favorable and 34% neutral answers. Regarding the experience, the group of less experienced respondents had a more favorable perceived usefulness, with 54% of positive answers. They also had lower unfavorable perceived usefulness, with 12% unfavorable answers (about half of the unfavorable answers from the more experienced). Besides this, the more experienced professionals also had a considerable favorable perceived usefulness, with 42% of positive answers.

## 8.6 Intention of use result

Academics had the highest intention of use, with 45% of favorable answers (Fig. 29). The most unfavorable reaction concerning I OU comes from the practitioners, with 38% answering negatively. Despite this, the practitioners' intention to use was also considerable, with 38% answering positively. Despite the differences between academia and industry, it was in the division between more and less experienced that the greatest differences occurred. The less experienced group had a higher intention to use, with 50% against 30%. The group of more experienced people had an I OU rejection of 42% (professionals who expect not to use the representation). Despite this, the more experienced group had considerable acceptance, with 33%, as neutrality was low.

Fig. 28 Perceived usefulness's results

[FIGURE]

Fig. 29 Intention of use's results

[FIGURE]

## 8.7 Discussion

As shown above, considering all groups, a considerable part (41%) had a favorable perception of the ease of use of the competence representation. This indicates that, for the favorable group, the representation seems to be easy to understand, learn, and interpret, among others. In this case, this is an indication that the representation is seen as applicable, i.e., it can be used to represent competences in the EA context and facilitate the understanding of it. Similarly, also considering all groups, a considerable part (48%) thinks that the competence proposal is useful, that is, they think that it can bring practical benefits in the context of EA. In this case, this indicates that the competence representation can potentially impact positively capability-based practices in the EA context, such as improving communication, understanding, and decisionmaking related to competence. Furthermore, a considerable part (41%) showed interest in using the proposal in a practical scenario in the context of EA. Although the assessment lacks more elaborate instruments for a more precise conclusion, these favorable percentages are a great indication that a significant part of the stakeholders are potentially prone to use the proposed competence representation to support the capability-based practices mentioned above.

Fig. 30 Correlation of survey variables

[FIGURE]

## 8.8 Correlation between Survey Variables

As a way of carrying out a preliminary evaluation of the results, we performed a correlation analysis between TAM variables. This analysis was used to identify clues about the relationship between the variables and better understand the results. The aim in this case is to verify whether the correlation between the variables considered in the preliminary result follows the relationships proposed in the original TAM model. For this, we have obtained the Pearson correlation coefficients [81] for our survey variables. Coefficients greater than 0.2 are shown in Fig.30. (There were no negative correlations observed.)

As expected, all TAM variables are positively correlated. As the TAM model states, our analysis identified a positive correlation between the PEOU and PU variables, between PEOU and I OU , and also between the PU and I OU variables. I OU has a strong correlation of 0.9 and 0.7 with PU and PEOU , respectively; PEOU has a correlation of 0.6 with PU . Besides not being possible to establish a causal relation, this suggests that the favorable perception of ease of use and usefulness of proposed representation may have contributed, even if indirectly, to the favorable intention of use. Besides not being conclusive, this is a favorable indication regarding the survey results, since it is aligned with the TAM variable's causal relationship. However, in order to be conclusive concerning this causal relation, further investigation is required.

The correlation analysis also indicated an association betweenTAMandexternalvariables.AsshowninFig.30,the F1-Score has a moderate correlation with all TAM variables. This is suggestive that respondents who were capable of identifying the traceability between competences and capabilities ended up with a more positive attitude toward the proposed representation. UDT was only weakly correlated to the other variables in the study. Further investigation into this is required; the questions to assess understanding required extrapolation and interpretation. So, it is possible that the instrument was too complex, as we would have expected a stronger correlation with the TAM variables.

[FIGURE]

## 8.9 Insights from negative perception

We regard the survey as a mechanism for identifying potential issues in the acceptance of the representation before its actual deployment. The main point of attention we identify is the relatively negative PEOU and I OU for experienced respondents (despite their positive PU ). An analysis of the free text in the survey comments could provide us with some insight to feed into the next cycle of development of the representation. For instance, a practitioner with negative responses suggested that there were 'non-standard relationships that confuse ArchiMate users'. When we posted this survey in LinkedIn groups on EA, we received similar comments. Some practitioners on that forum claimed that the representation 'mix[es] perspectives, the personal and the organizational one'. We believe these issues can be traced to ArchiMate's original placing of the capability constructs into the strategy layer. Hence, the proposed representation inevitably crosses perspectives. This is a hypothesis for further analysis, e.g., by using focus groups with experienced ArchiMate modelers.

## 8.10 Threats and limitations

Regarding threats to validity, we highlight the low statistical strength. We evaluated 27 responses from professionals in the EA area, including academics and practitioners. Hence, there is insufficient data concerning subgroups (such as experienced practitioners).

The heterogeneity of the analyzed groups constitutes another threat to validity. The possibility to generalize results increases with the degree of heterogeneity of the analyzed group. In this specific case, only professionals with knowledge of ArchiMate and enterprise modeling constituted the population. Future research can also include additional relevant audiences, such as HR professionals and even those in the VET sector, who have grown used to modeling competences and face a variety of challenges in this task.

Another threat to validity is related to the maturation effect whenparticipants undergo changes during the survey and this can alter the result. Mainly because we started the survey with questions about traceability and understanding. Such questions required reasoning, reflection, and analysis of the competencerepresentation. In this case, we presented a not so straightforward diagram, with a lot of relevant information.

[FIGURE]

This may have tired, worn out, or impacted the participant in some way.

Another threat to validity may have occurred in the selection of participants. As the survey participants were volunteers (in part contacted through contact networks and email and in part through open fora such as LinkedIn), this may have generated the so-called self-selection bias [82].

There are other threats to validity that can also be considered in this empirical evaluation, such as: using only one model with just a specific scenario for the survey; and a restricted number of questions (in particular those to assess traceability retrieval and understanding). The number of questions was thought out to reduce response time, and, hence, reduce dropout during survey answering.

We used Cronbach's Alpha (CA) [83] score to assess the survey's internal consistency. In this case, the PEOU 's CA was 0.68, the PU 's CA was 0.56, and the I OU 's CA was 0.72. According to [84], CA values between 0.6 and 0.8 can be considered as high, and CA values between 0.4 and 0.6 are medium. Hence, I OU 's and PEOU 's CA reliability is rated as high (between 0.6 and 0.8), but PU 's CA reliability is rated as medium (between 0.4 and 0.6). However, despite its utility, CA also has some limitations regarding reliability compared to the reliability of coefficients generated using other methods, such as the Structured Equations Method (SEM) [85].

Another limitation of this work is the non-adoption of any factor analysis method such as Bartlett's Test of Sphericity and the Kaiser-Meyer-Olkin (KMO) test [86]. In such tests we could identify redundancy and verify the relationship between the measured variables, grouping them into factors, for example. Although we identified the correlations between the variables, we are unable to determine whether these relationships are significant given the small sample size. Future testing on larger samples is required for this. Besides this, the correlation analysis just provides insights regarding the correlation between variables but this does not imply causation. So, in order to better understand how variables are causally related, the use of a more elaborated method, as Structured Equations Method (SEM) [85], is required.

Finally, another limitation refers to the TAM model adopted. There are many versions and variations of the TAM model, some more recent, detailed, and with more variables to be analyzed. It would be interesting for this research to adopt one of these more recent TAM models, concerning more variables related to cognitive and social aspects.

## 9 Related works

Competence models range from simple textual representations to more semantically rich and sophisticated representations [87]. Competence management approaches began to use standardized models, such as XML-based ones, to support specific technological tasks such as data integration and exchange. These models then evolved into more complete conceptual models. Recently, ontology-based models have become more prevalent in CoM approaches, incorporating more semantics into competence models [88]. They have been used for a variety of purposes, the majority of which are related to business and education. Some of these works are discussed below.

There are many proposed competence ontologies, but mostofthemdonotaddresshowcompetenceanditselements can be combined to form new competences or organizational capabilities. Such ontologies generally focus on basic definitions such as competence, the person carrying or related role, andsomeelements(mainlyskill).Amongthem,someontologies work at individual and type levels. However, none of the ontologies analyzed consider the phenomenon of emergence or relate competence to organizational capabilities, as proposed in this work. Such ontologies are focused on generic descriptions of competences and do not integrate type and individual levels well. They are not focused on supporting the basic tasks of skills management, especially gap analysis. This work, through the representation of relationships between competences and their elements, allows for a better gap analysis as it helps to understand how competences and organizational capabilities are formed.

Table 7 compares this ontology to similar ones in terms of the key factors taken into account in this work. As it is shown, most of the analyzed ontologies consider the main distinctions related to competence and the person who bears it. Most of the related works consider at least one kind of competence element. For example, Paquette's ontology [13] also includes skill and knowledge, but not attitude. In this case, knowledge and skill are components of competence. Miranda et al.'s [39] also incorporate knowledge, skill, and attitude into their model. In its structure, competence consists of these elements. In the ontology of Zaouga et al.'s [89], knowledge and skill are considered sub-types of competence rather than elements. The ontology does not cover attitudes. In its place, the authors use the behavior concept with a similar meaning.

In contrast to those works, here we treat skills as constituent elements of competences. As a result, competences can be represented at various levels of abstraction. They are dispositional concepts, and types of Human Capability, that can manifest themselves through tasks. Knowledge and attitudes share this dispositional nature and can manifest together with tasks through actions, posture, and so on. Aside from the detailed and well-founded representation of competences, supporting Competence Management tasks in Enterprise Architecture is another distinguishing feature of this work.

The vertical relationships (composition, emergence, and resultant) are not properly addressed by most of the other efforts reported in the literature. Only [39, 90] consider this aspect in a simple way, by allowing solely parthood between competences. The composition of other human capabilities (as skills) in a general sense is not considered. The only vertical relationship considered in the related works was the parthood one. These works do not consider the emergence (or resulting) of organizational capabilities from individual competences.

Concerning the horizontal relationships, mainly [90, 91] consider them in a very generic way. In this sense, these works do not regard the specific relationship types addressed here, but rather a kind of generic relationship between competences, that could be used vaguely to model some horizontal relationships. Paquette [13] also relates the concepts of skill and knowledge concerning parthood and applicability. According to this work, skills are 'applied to' knowledge entities. Skills are classified in the ontology based on taxonomies and complexity levels, and they are also measured using indicators. As stated in [39], knowledge, and skill are also related concepts. This ontology takes into account not only skill classification but also knowledge and attitude.

Still concerning this aspect, one of the most relevant related works is not focused on competences (or capability) but on prevention and risk modeling [64, 67]. These works also consider foundational ontologies and disposition theories to propose relationships between disposition types. Besides focusing on other domains, these works also focus on disposition types relationships, differently from this work that also considers relationships between (individual) dispositions . In this case, similar relationships are addressed in these related works such as 'mutual activation partnership' (similar to 'reciprocal to'), prevent (similar to 'disables'), andtriggering (similar to 'enables'). Otherwise, other important relationships considered here are not addressed there, such as 'additional to' and 'changes'. Another similarity of this work is that is also applied in the EA context, also proposing well-founded representations but in the risk area [92] area.

Some other works such as [19, 105] have also explored foundational ontologies in EA modeling. Both employ UFO to conduct ontological analyses of two concepts closely related to competence: capability and service. [19], for example, views service delivery as the manifestation of competences. [105], on the other hand, conducts an ontological analysis of Capability and is also related to the concept of Competence. Azevedo et al [105] briefly discuss the definition of competence based on capability; in the current work, we adopt and expand on that analysis. As discussed here, competences can be placed in the so-called capability bundles [105], connecting individual-level capabilities (competences) with organizational capabilities.

[FIGURE]

[FIGURE]

Table 7 Related works comparison ( X - included aspect, O - partially included aspect)

[FIGURE]

## 10 Final remarks

The study presented in this paper aimed to improve competence modeling in the context of Enterprise Architecture by using a reference ontology as a semantic foundation. The understanding of knowledge, skills, attitudes, and other characteristics allowed us to zoom in on individual competence, allowing for a detailed competence representation in the context of Enterprise Modeling. In addition, the comprehension of organizational capabilities and the horizontal and vertical relationship distinctions allowed us to zoom out on individual competences, enabling a general representation of them. Thereference ontology has provided us with a semantic foundation that accounts for the relation between organizational capabilities and individual competences, and this is reflected in the representation strategy.

We investigated the support of Competence Management activities with Enterprise Architecture models with the goal of improving personal competence and organizational capability understanding. From the standpoint of competence composition and decomposition, the proposed competence representation strategies make it easier to implement Competence Management in EA at distinct abstraction levels, from individual skills to capabilities of the whole organization. The model representation using ArchiMate , on the other hand, contributes a set of possibilities to enhancing the Competence Management practice. This distinguishes the current work from other ontology-based competence works in the literature.

Asaresult, the proposed representation can aid in essential CoM activities such as competence mapping, identification, and gap analysis. In this sense, the proposed representation patterns facilitate CoM activities by visualizing modeling competences from various perspectives. It enables the detailing of individual competences in these various representations, assisting with a deeper comprehension of the individual knowledge, skills, and attitudes that comprise these competences, and how they can be related giving rise to organizational capabilities. This combination of detailed and general vision aids in many CoM activities such as competence comparison, planning, and assessment, to name a few.

The focus of this work was to represent the competencerelated concepts at individual levels (similar to [9, 10]). The models can be used to represent: (i) real situations from the present or past related to one or more professionals (to support the competence identification ); (ii) desired situations from the future, related to one or more professionals (to support the gap analysis ); and (iii) hypothetical scenarios related to a persona, using storytelling to validate the models, as [106] propose, and understand better the CoM requirements.

Based on the case study application, the language pattern brought some benefits to the understanding of how individ- ual competences and skills can impact the capabilities of the whole organization. Through the proposed representation, it was possible to account for how the agile coach's competences impact the squad, the tribe, and consequently the whole organization, thereby increasing Spotify's adaptability. As presented in Sect. 7, the case study addressed by Bäcklander [21] provided a textual description of the individual and organizational capabilities. This description is very complete since it was a result of interviews and based on suitable theoretical background. We have rendered the description using EA models. This is conducive to producing hierarchical structures (revealing the content in different levels of detail) and to fill in certain gaps in the original textual rendering. A noticeable difference is that this description was not capability-oriented. As a consequence, the focus of the descriptions was not the capabilities themselves but the adopted practices (by the agile coaches, specifically). However, in order to achieve this, the descriptions basically detailed the agile coaches' capabilities (competences and skills) behind the performance of those practices. This description also included implicitly other elements related to the agile coaches' capabilities, such as attitudes and knowledge. Another aspect is the case study is the understanding of the relationships. In this sense, Spotify's case tried to understand how the individual practices of the agile coaches impactedothertribe membersandhowtheycontributedtothe emergent process of new capabilities (especially adaptability and innovation). That is, the implicit focus of the study was to analyze the horizontal relationships between agile coaches and tribe member competences and the vertical relationships between their capabilities and Spotify's emergent capabilities.

Even though its main focus was to understand the emergence and enabling relationships between agile coaches and other tribe members, how these phenomena happened in the organization was not so accurate. We believe that our use of a conceptual framework about competence-related concepts sheds further light into the observed phenomena. More specifically, the different kinds of human capabilities (competence and skill) and their elements (e.g., knowledge and attitude) can now be more clearly identified. The same could happen with the relationships among these competencerelated concepts. In other words, with the proposed language pattern, the case study's understanding of horizontal and vertical relationships and respective analyses of the context can be better supported.

In addition, it was noticed that, through the language pattern adoption, many implicit (tacit) relevant details of the scenario have surfaced while the model was constructed. In this sense, the language pattern worked as a guide, favoring the representation of hidden elements and relations during competence modeling. In this case, the reference ontology provided well-founded distinctions that served as archetypes in competence modeling. In practice, these archetypes as patterns helped to increase the level of abstraction of the representation. In summary, these archetypes worked as lenses, allowing a more precise view of this competence domain. As a result, (i) more human capabilities and correspondent elements (knowledge and attitude) were identified; (ii) how agile coaches impact other tribe members through enabling relationships was explicitly captured; and finally, (iii) how adaptability emergence happens was precisely described. In addition to these points, other important aspects to be concerned about in the proposed language pattern are: (i) the visual representation works as a complementary resource to facilitate communication and understanding; (ii) the vertical relationships allow us to work in distinct abstraction levels, enabling to manage the complexity of the competence representations; and (iii) the reference ontology allows a structured representation of competence information, which may serve as the basis to improve the quality of queries, reasoning, inferences, and technological solutions in general.

[FIGURE]

## 10.1 Future works

Future research could open up the concept of competence by investigating how the competences of different individuals can be combined to form organizational and collective capabilities from a systemic perspective, based on GeneralSystem Theory (GST). This study would delve deeper into how organizational capabilities emerge from personal competences according to the system (organization) structure and how its parts are connected. In this regard, the next step is to integrate the proposed competence ontology with the system core ontology and related capability emergence representation in ArchiMate, proposed in [11]. Differently from the present work, which explains the emergence using dispositional theories, this cited work addressed the emergence phenomenon taking into account the structural and functional aspects of the system. So, our expectation is to incorporate these systemrelated distinctions (e.g., system, component, connection, function) into this competence ontology in order to better represent the phenomena of the emergence of capabilities in the context of Enterprise Architecture. In this case, we see an opportunity to combine system science notions with theories of dispositions in order to improve understanding of how competences can be related and combined. Besides this, another future work is to incorporate the system ontology extension, proposed in [65], which incorporated distinctions related to emergent behavior in systems. As a result, we intend to use these distinctions to improve the representation of personal competence and organizational capabilities manifestation. Another expected result, in this context, is to combinetheseworkstoproposea systemcapability ontology . Still concerning the proposed ontology and possible semantic web applications, another future work is to implement and publish the ontological distinctions proposed in this work. In fact, for the previous version of the competence ontology [9, 10, 73], we already generated an implementation in OWL and released it using a permanent URI. 10 With this new version of the ontology, our intention is to evolve the related OWL implementation and incorporate relationships between personal competences, competence elements, and the emergence phenomenon.

[FIGURE]

We also see the need to develop more case studies to further validate the proposed competence representation patterns. Although ontological analysis provides the foundation for a well-founded representation (as used here, the foundation incorporates advances in Formal Ontology, Philosophical Logics, Philosophy of Language, Linguistics, and Cognitive Psychology [50]), the pragmatics of a representation in its usage context should be thoroughly assessed. Efforts in this sense have already been made for other UFO-basedrepresentationschemes,suchas[107],[19].Concerning Spotify's case, specifically, we intend to increment it, incorporating technical aspects as well. In this sense, it would be interesting to investigate how technical capabilities (from IT structure) contribute to the adaptability emergence. Based on the survey results, we expect to analyze them in order to improve the competence representation and release a new version. After this, we intend to evaluate the competence representation, in a deeper way. For this, we intend to improve the survey concerning a larger sample, establishing a clear hypothesis, and adopting a more recent and elaborated version of the TAM model (concerning more variables), in order to have more solid and assertive conclusions.

In regards to the competence representation, another future research concerns the relationship between competences and other ArchiMate perspectives, such as Motivation Elements. In this case, the ontological analysis could include other UFO concepts related to intentions, such as Goal and Proposition, which are related to the organization's strategic goals [20]. Still concerning the competence representation, we expect to extend the representation to other enterprise notations, such as, for example, Unified Architecture Framework (UAF) [108].

Acknowledgements This study was supported in part by CNPq (313687/2020-0), FAPES (281/2021) and the DSYNE INTPART network (Research Council of Norway project number 309404).

Open Access This article is licensed under a Creative Commons Attribution 4.0 International License, which permits use, sharing, adaptation, distribution and reproduction in any medium or format, as long as you give appropriate credit to the original author(s) and the source, provide a link to the Creative Commons licence, and indicate if changes were made. The images or other third party material in this article are included in the article's Creative Commons licence, unless indicated otherwise in a credit line to the material. If material is not included in the article's Creative Commons licence and your intended use is not permitted by statutory regulation or exceeds the permitted use, you will need to obtain permission directly from the copyright holder. To view a copy of this licence, visit http://creativecomm ons.org/licenses/by/4.0/.

[10 http://purl.org/coreo](http://purl.org/coreo)

## References

1. United Nations Educational S, (UNESCO) CO. United Nations Educational S, (UNESCO) CO, editors.: UNESCO strategy for technical and vocational education and training (TVET)(2016-2021). UNESCO, Paris, France
2. Wood, S.: Human resource management and performance. Int. J. Manag.Rev. 1 (4), 367-413 (1999). https://doi.org/10.1111/14682370.00020
3. Le Deist, F.D., Winterton, J.: What is competence? Hum. Resour. Dev. Int. 8 (1), 27-46 (2005). https://doi.org/10.1080/ 1367886042000338227
4. Sampson, D., Fytros, D.: Competence models in technologyenhanced competence-based learning. In: Handbook on Information Technologies for Education and Training. Springer Berlin Heidelberg; Cham, 155-177 (2008).
5. Gangani, N., McLean, G.N., Braden, R.A.: A competency-based humanresource development strategy. Perform. Improv. Q. 19 (1), 127-139 (2006)
6. Rodriguez, D., Patel, R., Bright, A., Gregory, D., Gowing, M.K.: Developing competency models to promote integrated human resource practices. Hum. Resour. Manag. 41 (3), 309-324 (2002). https://doi.org/10.1002/hrm.10043
7. Josey, A.: TOGAF® version 9.1-A pocket guide. Van Haren; (2016)
8. The Open group. The open group, editor.: TOGAF business capabilities guide V2. The open group. [Accessed 0610-2023]. https://pubs.opengroup.org/togaf-standard/businessarchitecture/business-capabilities.html
9. Calhau, R.F., Azevedo, C.L.B., Almeida, J.P.A.: Towards ontology-based competence modeling in enterprise architecture. In: 25th IEEE International EDOC Conference (EDOC 2021). IEEE; (2021)
10. Calhau, R.F., Almeida, J.P.A.: Zooming in on competences in ontology-based enterprise architecture modeling. In: 2022 IEEE 26st International Enterprise Distributed Object Computing Workshop (EDOCW); (2022). p. 198-213
11. Calhau, R.F., Prince Sales, T., Oliveira, I., Kokkula, S., Ferreira Pires, L., Cameron, D., et al.: A system core ontology for capability emergence modeling. In: Enterprise Design, Operations, and Computing. Springer Nature Switzerland; (2023). p. 3-20. Available from: http://dx.doi.org/10.1007/978-3-03146587-1\_1
12. Guizzardi, G.: Ontological foundations for structural conceptual models. No. 15 in Telematica Instituut Fundamental Research Series. The Netherlands: Telematica Instituut; (2005)
13. Paquette, G.: An ontology and a software framework for competency modeling and management. Educ. Technol. Soc. 10 (3), 1-21 (2007)
14. Rodrigues, M., Fernández-Macías, E., Sostero, M.: A unified conceptual framework of tasks, skills and competences. JRC Working Papers Series on Labour, Education and Technology; (2021)
15. Draganidis, F., Mentzas, G.: Competency based management: a review of systems and approaches. Inf. Manag. Comput. Secur. 14 (1), 51-64 (2006). https://doi.org/10.1108/ 09685220610648373
16. Westera, W.: Competences in education: a confusion of tongues. J. Curric. Stud. 33 (1), 75-88 (2001). https://doi.org/10.1080/ 00220270120625
17. Rosemann, M., Green, P., Indulska, M.: A Reference Methodology for Conducting Ontological Analyses. In: Modeling, Conceptual (ed.) ER 2004, vol. 3288, pp. 110-121. Springer, Berlin, Heidelberg (2004)
18. Azevedo, C.L.B., Iacob, M.E., Almeida, J.P.A., van, Sinderen. M., Ferreira Pires, L., Guizzardi, G.: An ontology-based well-founded proposal for modeling resources and capabilities in archimate. In: 17th IEEE International EDOC Conference (EDOC 2013). IEEE Computer Society Press; 2013. p. 39-48
19. Nardi, J.C.: A commitment-based reference ontology for service: harmonizing service perspectives
20. Azevedo, C.L.B., Almeida, J.P.A., van Sinderen, M., Quartel, D., Guizzardi, G.: An ontology-based semantics for the motivation extension to archimate. In: 15th IEEE International Enterprise Distributed Object Computing Conference. IEEE; (2011). p. 110
21. Bäcklander, G.: Doing complexity leadership theory: how agile coaches at spotify practise enabling leadership. Creati. Innov. Manag. 28 (1), 42-60 (2019). https://doi.org/10.1111/caim.12303
22. Davis, F.D., Bagozzi, R.P., Warshaw, P.R.: User acceptance of computer technology: a comparison of two theoretical models. Manag. Sci. 35 (8), 982-1003 (1989). https://doi.org/10.1287/ mnsc.35.8.982
23. Hevner, A., Chatterjee, S.: Design science research in information systems. In: Integrated Series in Information Systems. Springer, US; (2010). pp. 9-22. Available from: https://doi.org/10.1007/ 978-1-4419-5653-8\_2
24. Martin, J., Martin, J.: editor.: Enterprise Capability Management
25. Martin, J., Faisandier, A., Martin, J., Faisandier, A.: editors.: Enterprise Systems Engineering Background
26. Morgan, P.: The concept of capacity (draft version). Study on capacity, change and performance. (2006); pp. 1-19
27. Maier, J.: Abilities. In: Zalta EN, Nodelman U, editors. The Stanford Encyclopedia of Philosophy. Fall 2022 ed. Metaphysics Research Lab, Stanford University (2022)
28. Merrell, E., Limbaugh, D., Koch, P., Smith, B.: Capabilities
29. Antunes, G., Borbinha, J.: Capabilities in systems engineering: an overview. In: Exploring Services Science: 4th International Conference, IESS 2013, Porto, Portugal, Feb 7-8, 2013. Proceedings 4. Springer; (2013). pp. 29-42
30. Tell, A.W.: What capability is not. In: Perspectives in Business Informatics Research: 13th International Conference, BIR 2014, Lund, Sweden, Sept 22-24, 2014. Proceedings 13. Springer; (2014). p. 128-142
31. Dori, D., Sillitto, H.: What is a system? An ontological framework. Syst. Eng. 20 (3), 207-219 (2017). https://doi.org/10.1002/ sys.21383
32. Sillitto HG. 10.2.1 Composable Capability - Principles, strategies and methods for capability systems engineering. INCOSE International Symposium. 2013 Jun; 23(1):723-738. https://doi.org/ 10.1002/j.2334-5837.2013.tb03050.x
33. Saxena, M.: Capability Management. Global India Publications, India (2009)
34. Nagarajan, R., Prabhu, R.: Competence and capability: a new look. Int. J. Manag. 6 (6), 7-11 (2015)
35. Weigel, T., Mulder, M., Collins, K.: The concept of competence in the development of vocational education and training in selected EU member states. J. Vocat. Edu. Training. 59 (1), 53-66 (2007). https://doi.org/10.1080/13636820601145549
36. Mulder M. Conceptions of professional competence. In: International Handbook of Research in Professional and Practice-based Learning. Springer Netherlands; (2014). pp. 107-137. Available from: https://doi.org/10.1007/978-94-017-8902-8\_5

[FIGURE]

37. Gibson, J.J.: The theory of affordances. Hilldale, USA 1 (2), 67-82 (1977)
38. Draganidis, F., Chamopoulou, P., Mentzas, G.: A semantic web architecture for integrating competence management and learning paths. J. Knowl. Manag. 12 (6), 121-136 (2008). https://doi.org/ 10.1108/13673270810913667
39. Miranda, S., Orciuoli, F., Loia, V., Sampson, D.: An ontologybased model for competence management. Data Knowl. Eng. 107 , 51-66 (2017). https://doi.org/10.1016/j.datak.2016.12.001
40. Esposto, A.: Skill: an elusive and ambiguous concept in labour market studies. Aust. Bull. Labour. 34 (1), 100-124 (2008)
41. Brown JS. Learning in the digital age. In: The Internet and the university: Forum. vol. 71; p. 72 (2001)
42. Wood, R., Power, C.: Aspects of the competence-performance distinction: educational, psychological and measurement issues. J. Curric. Stud. 19 (5), 409-424 (1987). https://doi.org/10.1080/ 0022027870190503
43. Messick, S.: The psychology of educational measurement. J. Educ. Meas. 21 (3), 215-237 (1984). https://doi.org/10.1111/j. 1745-3984.1984.tb01030.x
44. Maze, J.R.: The concept of attitude. Inquiry 16 (1-4), 168-205 (1973). https://doi.org/10.1080/00201747308601684
45. Altmann, T.K.: Attitude: a concept analysis. In: Nursing forum. Wiley, London, vol. 43, pp. 144-150 (2008).
46. Acampora, G., Gaeta, M., Orciuoli, F., Ritrovato, P.: Exploiting semantic and social technologies for competency management. In: 10th IEEE International Conference of Advanced Learning Technologies. IEEE; pp. 297-301(2010)
47. Pyster, A., Olwell, D.H., Hutchison, N., Enck, S., Anthony Jr J,F., Henry, D., et al.: Guide to the systems engineering body of knowledge (SEBoK) v. 1.0. 1. (2012)
48. Molnar, G., Bradley, N.: Powers: A Study in Metaphysics. Clarendon Press, USA (2003)
49. Mumford, S., Anjum, R.L.: Getting Causes from Powers. Oxford University Press, Oxford (2011)
50. Guizzardi, G., Wagner, G., Almeida, J.P.A., Guizzardi, R.S.S.: Towards ontological foundations for conceptual modeling: the unified foundational ontology (UFO) story. Appl. Ontol. 10 , 259271 (2015). https://doi.org/10.3233/AO-150157
51. Guizzardi, G., Wagner, G.: Towards ontological foundations for agent modelling concepts using the unified fundational ontology (UFO). In: Agent-Oriented Information Systems II. Springer Berlin Heidelberg; pp. 110-124 (2005)
52. Bunge, M.: Treatise on Basic Philosophy: The Furniture of the World. Ontology I. Reidel Pub.; (1977)
53. Bunge, M.: Treatise on basic philosophy. Ontology II: A World of Systems. Dordrecht, Netherlands: Springer Netherlands; (1979). Available from: https://doi.org/10.1007/978-94-009-9392-1
54. Anjum RL, Mumford S. Emergence and demergence. In: Philosophical and Scientific Perspectives on Downward Causation. Routledge; pp. 92-109(2017)
55. Mumford,S.,Anjum,R.L.:PowersofWholesandParts.In:FOIS; . p. 4 (2016)
56. O'Connor, T.: Emergent properties. Am. Philos. Q. 31 (2), 91-104 (1994)
57. Spencer-Smith, R.: Reductionism and emergent properties. In: Proceedings of the Aristotelian Society. JSTOR; . p. 113129(1995)
58. Mossio, M., Bich, L., Moreno, A.: Emergence, closure and interlevel causation in biological systems. Erkenntnis 78 (S2), 153-178 (2013). https://doi.org/10.1007/s10670-013-9507-7
59. Juarrero, A.: Dynamics in action: intentional behavior as a complex system. Emergence 2 (2), 24-57 (2000)
60. Wilson, J.M.: Nonlinearity and metaphysical emergence. In: Mumford S, Tugby M, editors. Metaphysics and Science (2013)
61. DeLanda, M.: Emergence, causality and realism. Archit. Theory Rev. 17 (1), 3-16 (2012)
62. Martin, C.B.: The Mind in Nature. OUP Oxford, Oxford (2010)
63. Barton, A., Jansen, L., Ethier, J.F.: A taxonomy of dispositionparthood. In: Workshop on Foundational Ontology in Joint Ontology Workshops: JOWO 2017. vol. 2050. CEUR-WS: Workshop proceedings; (2017). p. 1-10
64. Baratella, R., Fumagalli, M., Oliveira Í, Guizzardi, G.: Understanding and Modeling Prevention. In: Research Challenges in Information Science. Springer International Publishing; pp. 389405 (2022)
65. Calhau, R.F., Sales, T.P., Guizzardi, G., Almeida, J.P.A.: Exploring System Behavior in a System Ontology (2023)
66. Galton, A., Mizoguchi, R.: Dispositions and the infectious disease ontology. In: Formal Ontology in Information Systems: Proceedings of the Sixth International Conference (FOIS 2010). vol. 209. Ios Press; p. 400 (2010)
67. Oliveira Í, Sales, T.P., Baratella, R., Fumagalli, M., Guizzardi, G.: An ontology of security from a risk treatment perspective. In: Conceptual Modeling. Springer International Publishing; pp. 365-379 (2022)
68. Ichikawa, J.J., Steup, M.: The Analysis of Knowledge. In: Zalta EN, editor. The Stanford Encyclopedia of Philosophy. Summer 2018 ed. Metaphysics Research Lab, Stanford University; (2018)
69. Choi, S., Fara, M.: Dispositions. In: Zalta EN, editor. The Stanford Encyclopedia of Philosophy. Spring 2021 ed. Metaphysics Research Lab, Stanford University; (2021)
70. Guizzardi, G., Pires, L.F., van Sinderen, M.: Ontology-Based Evaluation and Design of Domain-Specific Visual Modeling Languages. In: Advances in Information Systems Development. Springer, US; pp. 217-228 (2006)
71. Braga BFB. Cognitive effective instance diagram design. Graduation Thesis, Federal University of Espírito Santo. (2011);
72. The Open Group.: ArchiMate 3.2 specification. Available from: https://pubs.opengroup.org/architecture/archimate3-doc/
73. Calhau RF, Kokkula S, Cameron D, Guizzardi G, Almeida JPA. Modeling Competence Framework Elements with an Ontologybased Approach. In: 2023 IEEE 25th Conference on Business Informatics (CBI). IEEE; 2023. Available from: https://doi.org/ 10.1109/cbi58679.2023.10187498
74. Kniberg, H., Ivarsson, A.: Scaling agile@ spotify. online], UCVOF, ucvox files wordpress com/2012/11/113617905scaling-Agile-spotify-11 pdf. (2012);
75. Kniberg H.: Spotify engineering culture (part 1). Available from: https://engineering.atspotify.com/2014/03/spotifyengineering-culture-part-1/
76. Smite, D., Moe, N.B., Floryan, M., Levinta, G., Chatzipetrou, P.: Spotify guilds. Commun. ACM 63 (3), 56-61 (2020). https://doi. org/10.1145/3343146
77. Engineering S.: Agile Coaching (AC) at Spotify: Shining a Light on the AC Career Framework - Spotify Engineering - engineering.atspotify.com. [Accessed 05-10-2023]. https://engineering. atspotify.com/2023/01/agile-coaching-ac-at-spotify-shining-alight-on-the-ac-career-framework/
78. : Agile Coach Career Framework-Spotify. [Accessed 05-10-2023]. https://drive.google.com/file/d/1e9QQT66vpo5sEKvWjw8yaMqp547fLpr/view
79. Albaum, G.: The likert scale revisited. Mark. Res. Soc. J. 39 (2), 1-21 (1997). https://doi.org/10.1177/147078539703900202
80. Mandal, P.C.: Net promoter score: a conceptual analysis. Int. J. Manag. Concepts Philos. 8 (4), 209 (2014). https://doi.org/10. 1504/ijmcp.2014.066899
81. Cohen, I., Huang, Y., Chen, J., Benesty, J., Benesty, J., Chen, J, et al. Pearson correlation coefficient. Noise reduction in speech processing. pp. 1-4 (2009)

[FIGURE]

82. Heckman, J.J.: Selection Bias and Self-selection. In: Econometrics. Palgrave Macmillan UK; 1990. pp. 201-224. Available from: https://doi.org/10.1007/978-1-349-20570-7\_29
83. Landis, J.R., Koch, G.G.: The measurement of observer agreement for categorical data. Biometrics 33 (1), 159 (1977). https://doi.org/ 10.2307/2529310
84. Tabachnick, B.G., Fidell, L.S.: Using multivariate statistics, 7th edn. Pearson, Upper Saddle River, NJ (2018)
85. Sijtsma, K.: On the use, the misuse, and the very limited usefulness of Cronbach's alpha. Psychometrika 74 (1), 107-120 (2008). https://doi.org/10.1007/s11336-008-9101-0
86. Dziuban, C.D., Shirkey, E.C.: When is a correlation matrix appropriate for factor analysis? Some decision rules. Psychol. Bull. 81 (6), 358-361 (1974). https://doi.org/10.1037/h0036316
87. Rezgui K, Mhiri H. Modeling Competencies in CompetencyBased Learning: In2018 JCCO Joint International Conference on ICTinEducation and Training, International Conference on Computing in Arabic, and International Conference on Geocomputing (JCCO: TICET-ICCA-GECO). IEEE; (2018)
88. HR-XML Consortium.: Competencies 1.0 (Measurable Characteristics) Recommendation 2001-Oct-16. Available from: http:// xml.coverpages.org/HR-XML-Competencies-1\_0.pdf
89. Zaouga, W., Rabai, L.B.A., Alalyani, W.R.: Towards an Ontology Based-Approach for Human Resource Management. vol. 151 of Procedia Computer Science. Elsevier; pp. 417-424 (2019)
90. Rezgui, K., Mhiri, H.: Towards a semantic framework for lifelong integrated competency management and development. Comput J. 63 (7), 1004-1016 (2020). https://doi.org/10.1093/comjnl/ bxz067
91. Sicilia, M.A.: Ontology-based competency management: infrastructures for the knowledge intensive learning organization. In: Intelligent learning infrastructure for knowledge intensive organizations: A semantic Web Perspective. IGI Global; pp. 302-324 (2005)
92. Oliveira Í, Sales TP, Almeida JPA, Baratella R, Fumagalli M, Guizzardi G. Ontological analysis and redesign of security modeling in archimate. In: Lecture Notes in Business Information Processing. Springer International Publishing; pp. 8298. (2022)Available from: https://doi.org/10.1007/978-3-03121488-2\_6
93. Braun, S., Kunzmann, C., Schmidt, A.: People tagging and ontology maturing: toward collaborative competence management. In: From CSCW to Web 2.0: European Developments in Collaborative Design. Springer London; . p. 133-154. (2010 )Available from:https://doi.org/10.1007/978-1-84882-965-7\_7
94. Tarasov, V.: Ontology-based approach to competence profile management. J. Univ. Comput. Sci. 18 (20), 2893-2919 (2012). https:// doi.org/10.3217/jucs-018-20-2893
95. Rezgui, K., Mhiri, H., Ghédira, K.: Extending moodle functionalities with ontology-based competency management. Proc. Comput. Sci. 35 , 570-579 (2014). https://doi.org/10.1016/j.procs. 2014.08.138
96. Grant S, Young R.: Concepts and standardization in areas relating to competence. In: Innovations in Organizational IT Specification and Standards Development. IGI Global; pp. 264280. (2013) Available from: https://doi.org/10.4018/978-1-46662160-2.ch016
97. Schmidt, A., Kunzmann, C.: Towards a human resource development ontology for combining competence management and technology-enhanced workplace learning. In: On the Move to Meaningful Internet Systems 2006: OTM 2006 Workshops. Springer Berlin Heidelberg; pp. 1078-1087 (2006)
98. Fazel-Zarandi, M., Fox, M.S.: An ontology for skill and competency management. In: Formal Ontology in Information Systems. IOS Press; pp. 89-102 (2012)
99. Bajenaru, L., Smeureanu, I.: An ontology based approach for modeling e-learning in healthcare human resource management. Econ. Comput. Econ. Cybernet. Stud. Res. 49(1) (2015)
100. Paredes-Valverde, M.A., del Pilar, Salas-Zárate M., ColomoPalacios, R., Gómez-Berbís, J.M., Valencia-García, R.: An ontology-based approach with which to assign human resources to software projects. Sci. Comput. Program. 156 , 90-103 (2018). https://doi.org/10.1016/j.scico.2018.01.003
101. Bakanova, A., Shikov, A.: The method of employee competencies managementbasedontheontologicalapproach.CEURWorkshop Proc. 2590 , 1-9 (2020)
102. Tambouris, E., Zotou, M., Kalampokis, E., Tarabanis, K.: Fostering enterprise architecture education and training with the enterprise architecture competence framework. Int. J. Train. Dev. 16 (2), 128-136 (2012). https://doi.org/10.1111/j.14682419.2012.00400.x
103. Kalampokis, E., Tambouris, E., Zotou, M., Tarabanis, K.: The enterprise architecture competence framework. Int. J. Learn. Technol. 7 (1), 79 (2012). https://doi.org/10.1504/ijlt.2012. 046867
104. Bouras, A.A., Zainal, A.A.: Education ontology modeling for competency gap analysis. In: 3rd IEEE International Conference on Computational Science and Computational Intelligence (CSCI 2016); (2016)
105. Azevedo, C.L.B., Iacob, M., Almeida, J.P.A., van Sinderen, M., Pires, L.F., Guizzardi, G.: Modeling resources and capabilities in enterprise architecture: a well-founded ontology-based proposal for archimate. Inf. Syst. 54 , 235-262 (2015). https://doi.org/10. 1016/j.is.2015.04.008
106. Braga, B.F.B., Almeida, J.P.A.: Modeling Stories for Conceptual Model Assessment. In: Lecture Notes in Computer Science. Springer International Publishing; pp. 293-303 (2015)
107. Griffo, C., Almeida, J.P.A., Guizzardi, G.: Conceptual modeling of legal relations. In: 37th International Conference of Conceptual Modeling (ER 2018). vol. 11157 of Lecture Notes in Computer Science. Springer; pp. 169-183 (2018)
108. (OMG)OMG.:Theunifiedarchitectureframework(UAF).Object Management Group (OMG)

Publisher's Note Springer Nature remains neutral with regard to jurisdictional claims in published maps and institutional affiliations.

Rodrigo F. Calhau is a lecturer at the Federal Institute of Espírito Santo (IFES) and a Ph.D. Candidate in Ontology and Conceptual Modeling Research Group (NEMO) at the Federal University of Espírito Santo (UFES) and Semantics, Cybersecurity, and Services Group (SCS) at the University of Twente, Netherlands. He is a member of the LEDS research group and has worked for 10 years with project-based learning initiatives and development professional capabilities in the Software Engineering area. Recently, he has worked with ontologies to model human capabilities.

Satyanarayana Kokkula received his PhD from the Norwegian University of Science and Technology (NTNU), Trondheim, Norway. From 2006 to 2016, he was employed at FMC Kongsberg Subsea AS as a Specialist Engineer in Structural Analysis. In August 2017, Dr. Kokkula joined the University of South-Eastern Norway (USN) as an Associate Professor of Systems Engineering. He serves as a Program Coordinator for Industry Master in Systems Engineering and Systems Engineering specialization coordinator for Master in Innovation and Technology Management at USN. Dr. Kokkula is a Certified Systems Engi- neering Professional (CSEP) by the International Council on Systems Engineering, and a Senior Member of the Institute of Electrical and Electronics Engineers.

[FIGURE]

João Paulo A. Almeida is a full professor at the Computer Science Department of the Federal University of Espírito Santo (UFES), Brazil. He is a founding member of the Ontology and Conceptual Modeling Research Group (NEMO) at UFES. Since 2007, he has been working on the application of ontologies in enterprise architecture and enterprise modeling. He is a senior member of the IEEE and the ACM and serves on the Advisory Board of the IAOA and the steering committees of EDOC and ER. He currently serves on the Editorial Board of the Journal of Applied Ontology, the Data &amp; Knowledge Engineering (DKE) journal, and the Transactions on Graph Data and Knowledge (TGDK).

[FIGURE]

Giancarlo Guizzardi is a Full Professor of Software Science and Evolution as well as Chair and Department Head of Semantics, Cybersecurity &amp; Services (SCS) at the University of Twente, The Netherlands. He is also an AffiliatedGuest Professor at the Department of Computer and Systems Sciences (DSV) at Stockholm University, in Sweden. He has been active for nearly three decades in the areas of Formal and Applied Ontology, Conceptual Modeling, Enterprise Computing, and Information Systems Engineering, working with a multi-disciplinary approach in Computer Science that aggregates results from Philosophy, Cognitive Science, Logic, and Linguistics. He is the main contributor to the Unified Foundational Ontology (UFO) and the OntoUML modeling language. Over the years, he has delivered keynote speeches at several key international conferences in these fields (e.g., ER, CAiSE, BPM, IEEE ICSC). He is currently an associate editor of several journals, including Applied Ontology and Data &amp; Knowledge Engineering, a co-editor of the Lecture Notes in Business Information Processing series, and a member of several international journal editorial boards. He is also a member of the Steering Committees of ER, EDOC, and IEEE CBI, and of the Advisory Board of the International Association for Ontology and its Applications (IAOA). Finally, he has recently been inducted as an ER fellow.
