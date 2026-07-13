[FIGURE]

## Formal Specification of Environmental Aspects of a Railway Interlocking System Based on a Conceptual Model

Dalay Israel de Almeida Pereira 1( B ) , Sana Debbech 1 , Matthieu Perin 2 , Philippe Bon 1 , and Simon Collart-Dutilleul 1

1

```
Univ. Lille Nord de France, IFSTTAR, COSYS/ESTAS, 59650 Villeneuve d'Ascq, France { dalay-israel.de-almeida-pereira,sana.debbech,philippe.bon, simon.collart-dutilleul } @ifsttar.fr 2 Institut de Recherche Technologique Railenium, 59300 Famars, France matthieu.perin@railenium.eu
```

Abstract. Relay-based Railway Interlocking Systems (RIS) are developed with the objective of controlling the movement of trains in a safe manner. However, these systems are generally specified by informal languages whose analyses are made by human inspection, which are error prone. A previous work presented an approach for specifying these systems in a formal language in order to automatically prove safety properties. Nevertheless, despite the impact of the environment over the system operation, the approach allows only the specification of the electrical components behaviour. Hence, the environment must be considered in the system specification in order to guarantee its safety. This paper presents the application of a higher level of modelling abstraction, conceptual modelling, which may provide a conceptual clarification of the RIS environment. This proposed conceptual model allows a semantic analysis of the environmental impact over the system and the description of other safety properties that have not been considered in the formal specification. In this work, an ontology built for the critical systems modelling is used in order to provide a terminological harmonisation between the physical elements of the system and the environment. The conceptual model allows a safety-oriented improvement of the RIS formal specification as well as it provides a common, shared and unambiguous view of both system and environment.

Keywords: Conceptual modelling · Ontology · Railway Interlocking Systems · Relay diagrams · UFO ·

## 1 Introduction

Railway Interlocking Systems (RIS) are responsible for controlling trains in a determined track in order to avoid the occurrence of hazards, like collisions.

Supported by the LCHIP (Low Cost High Integrity Platform) project.

c © Springer Nature Switzerland AG 2019

A. H. F. Laender et al. (Eds.): ER 2019, LNCS 11788, pp. 338-351, 2019.

B-method

They are considered safety-critical systems, since failures may result in severe consequences like the loss of people lives. A relay-based RIS is the implementation of an interlocking system logic as an electrical circuit whose current flow is controlled by electromechanical components called relays. These systems are generally specified by diagrams representing how the electrical components of the circuit are connected. As a consequence, the safety proof of these systems is a challenging task, since the usual way to verify these models is by manually inspecting and drawing conclusions, which is error prone [10].

In order to automatically verify relay-based RIS, a previous work [2] has presented a methodology for the specification of these systems in a formal language, B-method, whose mathematical background and supporting tools allow the automatic system verification regarding safety properties. In this methodology, one may extract the system behaviour based on the behaviour of its electrical components. Although this methodology provides ways in order to verify the existence of unsafe states during the execution of the system, it fails in disconsider the impact of the environment on the behaviour of these systems. In order to prove the safety of a RIS, the environment must be considered.

The specification of physical electrical components is based on their own meanings and defined behaviours, whereas the environmental specification involves pure knowledge about the field. Furthermore, the impact of the environment over the system is not specified inside relay diagrams. In this work, an example of the conceptual modelling usage is presented in order to conceptualise relations between a RIS and its environment. The use of a conceptual model allows a better understanding of the domain knowledge and provides a shared view with a common vocabulary. Moreover, an improvement of the RIS formal specification may be derived from the captured knowledge. In the literature, conceptual modelling has never been used for assisting the RIS formal specification and creating a direct distinction between the RIS and their environments.

Another benefit of conceptual modelling consists in the use of a top-level ontology in order to provide a conceptualisation in real-world semantics and approximate as well as possible the ideal representation of a domain. In this paper, the conceptual modelling phase is based on the use of the Unified Foundational Ontology (UFO) [9] in order to establish relations between the foundational distinctions of UFO and the system and its environment dependencies. Then, the ontological pattern and the modelling rules proposed by UFO are used for building the ontology.

The next section presents the case study that is used throughout this paper. Then, Sect. 3 discuss about the ontology for modelling critical systems, followed by a presentation of the methodology for the formal specification of RIS. The contribution of this paper, the use of conceptual modelling for the environmental specification in a RIS example, is detailed in Sect. 5 and discussed in Sect. 6. Finally, a conclusion and some previous works are presented.

## 2 Case Study

Relay-based Railway Interlocking Systems are composed by electrical circuits containing relays, which are electromechanical switching elements comprised by electromagnets (coils) and contacts [15]. When electrified, a relay closes or opens its contacts in a way that it may control the flow of electrical current inside the circuit wires. Before their implementation, these systems are generally modelled by relay diagrams, which are graph-like schemata that present how the electrical components (relays and buttons, for instance) are connected by wires.

In order to exemplify the use of RIS, a simple railway track plan, presented in Fig. 1, depicts two train tracks. This specific track section is used to allow two trains to move in opposite directions without collisions. However, a dangerous situation may be found when a train that arrives at Control Area A must change to the other track because of problems on its own track. The possible collision with a train that comes from Control Area C requires the use of an interlocking system in order to control the movement of these trains. In this industrial example, the diagram presented in Fig. 2 represents a relay-based RIS diagram used by SNCF (the French National Railway Company) in order to control the entrance of trains in Control Area A.

Fig. 1. Track plan from the signalling Control Area A to C

[FIGURE]

The connection between electrical components are represented by full lines in relay diagrams. These lines are the electrical wires of the circuits. The relation between the relays and their related contacts are represented by vertical semi-doted lines. A relay diagram may contain many different types of electrical components. Some of them are detailed in Table 1.

Relay-based RIS are reactive systems, which means that the electrical activation of a component may trigger the activation of others components. In electrical circuits, a component is activated if it is connected to a positive and a negative sources of energy at the same time. The inputs of this system are usually represented by buttons, levers and independent contacts (whose related relays are not presented). The outputs of these systems are generally understood as the permission or a denial to a train to enter in an specific section of the tracks. Considering the preconditions for each component to be activated and the connections between these components, relay diagrams are graphical representations of the logic behind relay-based RIS behaviour.

Fig. 2. Part of the relay-based system model of the signalling Control Area A

[FIGURE]

Table 1. Elements that may be used in a relay-based diagram.

| Electrical sources of energy poles.                                                                              |
|------------------------------------------------------------------------------------------------------------------|
| Couple button-lever.                                                                                             |
| Monostable and bistable relays coils, respectively.                                                              |
| Blocks for relay timed activation and deactivation, respectively.                                                |
| A normally closed contact related to a monostable relay and a contact related to a bistable relay, respectively. |

Due to the critical nature of this example, a thorough RIS safety analysis must be performed in order to avoid hazardous situations. For this purpose, the railway safety community recommends the use of formal specification methodologies [7]. However, although the formal languages mathematical background is capable of proving RIS safety properties, they do not dispose of tools for modelling, organising and harmonising knowledge together with the physical system.

As an example, based on the knowledge about railway systems, the meaning of some components depicted in Fig. 2 are presented in Table 2. However, the system knowledge is related to a high level of expertise of the domain, which may lead to conflicts between the actors. In the formal specification context, there is a lack of a distinction between both system and environmental aspects. This issue complicates the understanding of the formal specification, which may be ambiguous in a collaborative context. Consequently, the need of the knowledge conceptualisation arises in order to clarify and precise the terminology used in the specification.

Table 2. Meaning of some elements of the relay diagram.

| KAG   | a   | G    | Switch in the left position, if activated ( TRUE ) the train cannot change to the other track                                             |
|-------|-----|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| EPA   | C   | CSS  | Routing control, when activated it allows a train to change its route (change tracks or not), when deactivated it blocks the route change |
| RPD   | FA  | C911 | Detector of the train presence in a track, it deactivates in the presence of a train                                                      |
| INT   | AC  | V2   | Detects if the track is free or not, it is activated if the track is free (there is not a train)                                          |
| KSS   | E   | V2   | Permission given by Control Area C for a train to come from Control Area A                                                                |
| EF11  |     |      | Permission given by Control Area A for a train to come from Control Area C                                                                |
| KIT   | C   | 911  | Permission for a train in the Control Area A to enter in the dangerous zone                                                               |

In fact, we believe in the powerful capacities of the conceptual modelling to provide a shared and non ambiguous view with a common vocabulary. It allows the semantic interpretation of the components of the system, the environment, and relations between them in order to explicitly define a complete taxonomy able to ensure the conceptual clarification of the system and its environment with a high level of abstraction. Based on the definition of the relay diagram elements and the foundational features proposed by UFO, a semantic alignment is performed with the aim to establish an harmonisation between both abstract and concrete domains. In the next section, we briefly present an ontology of dysfunction analysis, which is proposed in a previous work, in order to explain how it is partially reused to satisfy the goal of the present study.

## 3 An Ontology for the Safe Design of Critical Systems

In order to provide a systematisation of the integration of the dysfunctional analysis into the design process, a domain ontology grounded in the Unified Foundational Ontology (UFO) is proposed in a previous work. It is well-known that the use of foundational ontologies in the development of a domain ontology supports the real-world semantics and improve the clarity, the expressiveness and the truthfulness of a domain conceptualisation. The discussion around the choice of UFO in comparison with other upper ontologies has been made in a previous work [5].

The Dysfunctional Analysis Ontology (DAO) aims to capture the dysfunctional analysis knowledge and it establishes a semantic link between safety constraints to be considered and the Goal-Oriented Requirements Engineering

(GORE) [17]. Furthermore, the related conceptual model improves the conceptual clarification of the safety reasoning and the management of safety decisions in the early stages of the safety critical systems design. Then, it allows an understandable representation of a domain in order to deal with the complexity of the collaborative decision-making.

DAO tackles the semantic heterogeneity issue that may lead to several conflicts between safety analysts and design engineers. The related terminology is based on the extraction of standards definitions such as [4,11,12] since the railway domain is the domain application of DAO. Moreover, the goal-oriented perspective is based on the reuse of a fragment from a reference domain model, the Goal-Oriented Requirements Ontology (GORO), which is grounded in UFO [14]. This improves the completeness, the consistency and the flexibility criterion of DAO. Hence, it supports the communication and the knowledge sharing between both safety and design actors.

In the verification and the validation phases, DAO shows its capabilities to represent several real situations and its taxonomy is relevant for the critical aspect of railway systems. Furthermore, it demonstrates the validity of its reuse for other critical applications such as the development of future autonomous trains [6]. Indeed, DAO considers the socio-technical aspect of railway systems and this is important in the safety improvement. Then, it considers both the safety and the system views in the safety analysis and the system design. This perspective of conceptualisation is relevant for the system specification too, since it support the integration of the environmental properties.

In the present paper, the DAO fragment related to the system and the environment views is reused in order to provide an ontological analysis of the environmental aspect and to capture this knowledge regarding the system specification. This phase seems to be a preliminary activity of the formal specification in order to terminologically systematise the environment notion and its surrounding concepts. One of the issues of formal methods consists in the inability to define the real-world taxonomy with a common vocabulary. In other words, there is a need to clarify the semantics used in the specification based on real-world assumptions and from a high level of abstraction. The present work aims to fill this gap by capitalising and sharing the knowledge in order to satisfy the domain needs. In order to improve the understanding of the DAO scope, Fig. 3 depicts a part of the design pattern of DAO, that is able to address the challenges mentioned above.

Fig. 3. A part of the DAO design pattern reusable for the relay-based RIS representation

[FIGURE]

## 4 A Methodology for the Formal Relay-Based RIS Specification

In order to formally specify the running example, a methodology has been proposed in a previous work [2]. This methodology uses B-method in order to specify the relay diagram logical behaviour based on propositional logic. In the railway domain, B-method is considered one of the strongest approaches for the specification of railway systems [8]. This section presents a methodology for the formal specification of Relay-based RIS using B-method.

The basic building block of a B-method specification is the abstract machine [16]. Inside a machine, the system specification is divided into clauses, like: SETS , VARIABLES , INVARIANT , INITIALISATION and OPERATIONS . Within these clauses, one must specify, respectively, constant information sets, variables, variables properties, the machine initial state (variables initial values), and the operations responsible for changing the machine state. An example of a B-machine is depicted on Fig. 7, explained in detail in Sect. 5.2. Further information about the B-method clauses and notations may be found in [1].

As the RIS state is defined by the state of each electrical component, the running example components must be specified as variables in B-method. Hence, the INVARIANT and INITIALISATION clauses must type each variable and give their initial states, respectively. Some particular types may be defined in the SETS clause, and the initial state of the system is the one represented by the relay diagram itself. Furthermore, inside the INVARIANT clause it is possible to define safety properties that must be met during the system execution. The complete B-specification of the running example is presented in [2], moreover, disconsidering the grey blocks, Fig. 7 also presents this specification.

Considering our running example, in order to avoid possible train collisions, it is possible to specify an invariant in propositional logic. This invariant guarantees that the trains that come from Control Area A and C may never have permission to enter in the dangerous zone at the same time. This property is defined by: ' not(PLUS KIT C 911 = TRUE &amp; EF11 = TRUE)'. The system state transition must be specified by an operation which receives the inputs of the system and changes the values of the variables. This operation calculates the states based on the preconditions for the activation/deactivation of each electrical component.

## 5 From Conceptual Modelling Towards Environmental RIS Specification

The formal specification of the RIS presented as running example is not complete, since it does not consider environmental variables that may impact its execution. Hence, although this system is formally specified, it may not be considered safe. In this section, the process of conceptual modelling the relay-based RIS example is presented in order to conceptualise the knowledge about the system. Based on this conceptual model, it is possible to structurally capitalise the relation between the system and the environment and formally specify it.

## 5.1 Conceptual Model of a Relay-Based RIS Case Study

Before modelling the RIS environment, it is necessary to conceptualise the dependence between the electrical components of the system. This dependency reflects how the state of each component may affect the state of other component as a reactive system, i.e., the impact of a component activation/deactivation in the activation/deactivation of other components. This dependency is depicted in the conceptual model presented in Fig. 4.

Fig. 4. Conceptual model of the state dependency between the electrical components of the system

[FIGURE]

However, in real world, some environmental variables may affect the functioning of the system. In this case, the environment is considered as any object/aspect that is external to the system and related to it in some way. In our case study, the environmental objects/aspects related to the execution of the relay-based RIS are: track , train , pedal (which detects the train presence) and time (or the variation of time). The conceptualisation of these environmental variables is presented in Fig. 5. In order to improve the readability, concepts and relations are respectively written in bold and italic types.

Fig. 5. Conceptual model of the system environment and dependencies between objects

[FIGURE]

Train , Track and Pedal may be characterised by their Dispositions , which are respectively related to Position , Direction of extension and State . Considering the RIS in Control Area A, a train may be in one of three positions:

'approaching', 'in transit' (entering the dangerous zone) or 'arrived' (in the dangerous zone). The track between the Control Areas A and C may be extended in two different directions: normal (for the train the comes from Control Area C) or opposite direction (for the train that comes from Control Area A). The Pedal existing in the dangerous zone may be enabled or disabled in order to indicate the presence or absence of a train in this specific location.

Based on the domain knowledge, it is possible to make an explicit representation of the relations between these environmental variables and the electrical components of the RIS. In this case, it is important to consider that the relations associated to environmental variables are different from the relations that connect physical components. The dependence relationship between electrical components are 'explicit', since they are depicted in the relay diagram and represent the physical logical connection between these components. In this conceptual model, this relation is called exp-depends on . Contrarily, the environmental objects are not explicitly connected or even represented in usual RIS representations, hence, all their dependence relations are modelled as 'implicit' and called imp-depends on . Figure 5 depicts a part of the complete model which captures these implicit relations.

A condition that must be guaranteed in order to extend the tracks is that the component EPA C CSS must be deactivated in order to lock the train routing. The train may not enter in a track if there is the possibility of changing its route during this process. So, the extension of the tracks depends directly of the component EPA C CSS state. The extension of the track is also directly related to the permission for the trains to enter in the tracks, so, the state of the track depends on the states of PLUS KIT C 911 and EF11 .

Regarding the train, its state is directly related to the state of two physical components: KAG a G and INT AC V2. The former specifies that the switch between tracks is settled to the right position (train not allowed to change tracks) when activated, hence it must be deactivated when the train is 'in transit'. The latter indicates the occupation of the dangerous zone, hence it must be activated once the train has arrived in this portion of the tracks.

The track and the train are dependent to each other, since a train needs the track to be extended in order to enter in the dangerous zone and the track requires the train to approach in order to extend. Similarly, the train and the pedal are also dependent from each other since the pedal activates in the presence of a train and the train may be considered as 'arrived' once the pedal activates. In order to activate the pedal, the component RPD FA C 911, which is responsible for the detection of the train presence, must also be activated.

Similarly to what is presented in Fig. 5, the conceptual model fragment related to the instantiation of the physical components is depicted in Fig. 6. After adding the environmental information, the conceptual model of the system is enriched. This step is important to provide a complete and structured view of the system and its environment. Based on the conceptual model representing the relations between the environment and the relay-based RIS, it is possible to improve the formal specification of the system by specifying extra conditions in order to prove the safety of the system.

Fig. 6. Conceptual model representing the physical components instantiation

[FIGURE]

## 5.2 Formal Specification of Environmental Aspects of the RIS Case Study

Considering the running example B-specification, in order to add more information about the system, it is necessary to redefine the content of each clause. Except for time, which has been already defined as an input of the system in [2], the environmental variables must be defined in the VARIABLES clause of the specification, since their states are now considered in the system state. The updated specification is presented in Fig. 7, where all the added information are depicted in blue and inside grey blocks.

Instead of specifying the track as a unique variable, we opted by specifying it in two different variables according to its direction of extension. This may be explained by the fact that the conditions for the extension in each direction are unique and not related to each other. However, the possibility of extension in both directions at the same time may never exist. Hence, this condition must be verified and guaranteed by the invariant ' not(track extension OD = TRUE &amp; track extension ND = TRUE)', considering ' track extension OD' and ' track extension ND' the boolean variables related to the opposite and normal direction extensions of the tracks. This invariant may substitute the verification related to the permission to the trains to enter in the dangerous zone, since the extension of the tracks already includes this permission.

The train may be specified by an unique variable train OD, which may take the values approaching , in transit or arrived , indicating the position of the train that comes in the opposite direction. These states are specified in the SETS clause of the machine. Regarding the pedal, it is specified as a boolean variable, since it may assume only two states: activated ( TRUE ) or deactivated ( FALSE ).

Although the system may give permissions to the train to move, it does not directly controls the train, hence, the train behaviour is independent of the interlocking system. Since the train states are not directly dependent of the system and as an environmental variable, its states may be evolved independently of the RIS and in parallel with it. So, an operation for the state evolution of the train must be created. Furthermore, the operation must consider that in order to go from the 'approaching' to the 'in transit' state, the track must be extended. Following a similar logic, in order to go from the 'in transit' to the 'arrived' state, the pedal must be activated.

Fig. 7. Specification improved by environmental aspects (Color figure online)

[FIGURE]

Another variable whose states are not controlled by the RIS at Control Area A is track extension ND. Even if Control Area A gives permission to a train to come from Control Area C, it does not extends the track in the normal direction, since this extension is only controlled by the system in Control Area C. So, it is necessary to create an operation for this independent behaviour.

Considering the conceptual model, the operation related to the state evolution of the system itself must be improved. In this case, many preconditions that relate the inputs and the environmental variables may be created. As an example, the component INT AC V2 must be always deactivated if the train has arrived, which indicates that this portion of the track is occupied. However, if the train is still entering in this portion of the track (the train is 'in transit' and the pedal is 'activated'), INT AC V2 is still active, since it is giving permission to the train to enter. Hence, the same occurs if RPD FA C 911 is deactivated.

Many other conditions may also be considered. If the train is in transit, the switch between the tracks must continue set to the left position, which means that the component KAG a G must be set to FALSE . Furthermore, if the train is 'in transit' and EPA C CSS is activated, the pedal must also be activated, since the course of the tracks may only be changed if the train has arrived.

Considering that Control Area A cannot control the track extension in the normal direction, a condition must be specified in order to guarantee that the track must not be extended when Control Area A aims to extend it in the opposite direction. This means that, in the moment which the train that comes from Control Area A receives the permission to enter in the dangerous zone, the track must not be extended in the normal way. Hence, if KSS E V2 is activated, the time of the block has passed and EF11 is deactivated, the extension in the normal way must be FALSE .

The system in Control Area A is responsible for evolving the state of two environmental variables: the track extension in the opposite way and the pedal activation. The track will be extended in the opposite direction if EPA C CSS is deactivated or if the train is already 'in transit' or it has been 'arrived'. Furthermore, if the track is not already extended, the permission for a train to enter in the Control Area A must be given ( PLUS KIT C 911 activated). Regarding the Pedal, if it is not already activated, it becomes TRUE if the train is 'in transit' at the same time that it is detected in the track.

## 6 Discussion

The specification of the system may be model-checked and simulated by Prob [13] in order to guarantee that the execution of the system may never reach a dangerous state. The model-checking process took 7391 ms, verifying the 85,919 possible transitions between the 62 existing states in a 64 bits Intel(R) Core(TM) i7-7600U 2.80 GHz CPU with 16 Gb RAM and running the Windows 10 operating system in its professional version. The complete simulation of the system execution has shown to be accurate with reality.

The conceptual model related to the environmental aspects of the system allows the reasoning regarding the impact of the environment in the execution of the system. Hence, it is possible to describe many safety conditions that are not explicit in the relay diagram. In this work, the RIS running example presented was improved by adding safety conditions in order to guarantee that, for instance: a train may never enter in the dangerous zone if the course is not locked, the track is never extended in the opposite direction if the switch is set to the right position or that the track is not considered free if the train has arrived.

By adding these safety properties in the system specification, it is possible to improve the safety of the system, since the environmental impact may be verified and analysed. Furthermore, as a result of this work, it is possible to affirm that the formal specification of a relay-based RIS based on a relay diagram is not enough for guaranteeing safety in some determined conditions. The specification of the knowledge about the system linked to a structured representation of this knowledge is an essential step in order to improve the safety of the railway interlocking system.

## 7 Conclusion

This paper presents an example of the application of conceptual modelling in order to improve the safety of a railway interlocking system formal specification. The use of a conceptual model allows the reasoning about the impact of environmental variables over the execution of the system. Hence, by using a structured representation of the railway system knowledge, it is possible to derive safety properties in order to improve the safety of the RIS specification.

As a result, the specification of a relay-based RIS that has been presented in a previous work could be improved in order to consider many safety properties that could not be considered before. As a conclusion, it is possible to affirm that the knowledge conceptualisation of the railway domain is essential for the formal specification of relay-based RIS, since relay diagrams do not present all the information about unsafe possible states.

In our near future agenda we aim to perform a dysfunctional analysis of the example presented in this work in order to study the impact of relay failures over the system behaviour by reusing DAO. As a physical component, a relay may fail and break, hence, this behaviour must also be considered in the specification of the system. Furthermore, we aim to automate the formal behavioural specification of relay diagrams based on a graph-like approach (as the one presented in [3]) linked to a complete conceptual model about the known dependence guidelines between the components, environment and inputs of these systems.

Acknowledgements. This work is supported by the LCHIP project and the results presented in this paper are a product of the studies made in this project.

We thank Clearsy LCHIP team for sharing their studies with us, in special, we thank David Deharbe for his availability in explaining their results about the formal specification of relay-based RIS. Besides, we also thank SNCF for providing and allowing us to publish the relay schema in this paper.

## References

1. Abrial, J.R.: The B-book: Assigning Programs to Meanings. Cambridge University Press, New York (1996)
2. de Almeida Pereira, D.I., Deharbe, D., Perin, M., Bon, P.: B-specification of relaybased railway interlocking systems based on the propositional logic of the system state evolution. In: Collart-Dutilleul, S., Lecomte, T., Romanovsky, A. (eds.) RSSRail 2019. LNCS, vol. 11495, pp. 242-258. Springer, Cham (2019). https://doi. org/10.1007/978-3-030-18744-6 16

3. de Almeida Pereira, D.I., Perin, M., Bon, P., Collart-Dutilleul, S.: A framework for the formal specification of relay-based systems based on a b-method graph specification. Int. J. Comput. Electr. Eng. (IJCEE) 11 (1), 11-19 (2019)
4. CENELEC, NF EN 50129: Applications ferroviaires: Syst` emes de signalisation, de t´ el´ ecommunication et de traitement - Syst` emes ´ electroniques de ´ ecurit´ e pour la signalisation, Mai 2003
5. Debbech, S., Bon, P., Collart-Dutilleul, S.: Towards semantic interpretation of goaloriented safety decisions based on foundational ontology. J. Comput. (JCP) 14 (4), 257-267 (2019)
6. Debbech, S., Collart-Dutilleul, S., Bon, P.: Cas d'´ etude de mission ferroviaire t´ el´ e-op´ er´ ee. Rapport de recherche, IFSTTAR - Institut Fran¸ cais des Sciences et Technologies des Transports, de l'Am´ enagement et des R´ eseaux, November 2018. https://hal.archives-ouvertes.fr/hal-02020997/l
7. Railway applications-communication, signalling and processing systems-software for railway control and protection systems. Std, European Committee for Electrotechnical Standardization (CENELEC), March 2001
8. Fantechi, A., Fokkink, W., Morzenti, A.: B-specification of relay-based railway interlocking systems based on the propositional logic of the system state evolution. In: Formal Methods for Industrial Critical Systems: A Survey of Applications, pp. 61-84 (2013)
9. Guizzardi, G., Wagner, G., Almeida, J.P.A., Guizzardi, R.S.: Towards ontological foundations for conceptual modeling: the unified foundational ontology (UFO) story. Appl. Ontol. 10 (3-4), 259-271 (2015)
10. Haxthausen, A.E., Le Bliguet, M., Kjær, A.A.: Modelling and verification of relay interlocking systems. In: Choppy, C., Sokolsky, O. (eds.) Monterey Workshop 2008. LNCS, vol. 6028, pp. 141-153. Springer, Heidelberg (2010). https://doi.org/10. 1007/978-3-642-12566-9 8
11. IEEE, 1012: IEEE Standard for System, Software, and Hardware Verification and Validation (2016)
12. IEEE, 610.12: IEEE Standard Glossary of Software Engineering Terminology (1990)
13. Leuschel, M., Butler, M.: ProB: a model checker for B. In: Araki, K., Gnesi, S., Mandrioli, D. (eds.) FME 2003. LNCS, vol. 2805, pp. 855-874. Springer, Heidelberg (2003). https://doi.org/10.1007/978-3-540-45236-2 46
14. Negri, P.P., Souza, V.E.S., de Castro Leal, A.L., de Almeida Falbo, R., Guizzardi, G.: Towards an ontology of goal-oriented requirements. In: CIbSE, pp. 469-482 (2017)
15. R´ etiveau, R.: La signalisation ferroviaire. Presse de l'´ ecole nationale des Ponts et Chauss´ ees (1987)
16. Schneider, S.: The B-method: An Introduction. Palgrave, Basingstoke (2001)
17. Van Lamsweerde, A.: Goal-oriented requirements engineering: a guided tour. In: Proceedings of 5th IEEE International Symposium on Requirements Engineering (RE 2001), pp. 249-262. IEEE (2001)
