## Ontological Anti-patterns in Aviation Safety Event Models

Jana Ahmad ( B ) and Petr Kˇ remen

Faculty of Electrical Engineering, Czech Technical University in Prague, Prague, Czech Republic jana.ahmad,petr.kremen @fel.cvut.cz

{ }

Abstract. Last years, there has been growing interest in developing high quality models to ensure interoperability of applications as well as proper understanding among a community. To improve productivity of model designers as well as to improve quality of resulting models, proper theoretical foundations and tool support is necessary. This paper discusses some types of conceptual modeling anti-patterns that lead to error- prone modeling decisions, and describes a reproducible solution to a general anti-pattern detection problem during conceptual design. Novel contribution of this paper is the definition of new ontological antipatterns, we observed during our work in design and model ontologies in the domain of Aviation Safety. The approach is illustrated on models designed by means of OntoUML, an ontology-founded UML profile based on the Unified Foundational Ontology (UFO).

## 1 Introduction

In recent years, more and more attention is paid to the quality of conceptual models. Conceptual models should be sufficiently expressive to represent positive instances. Furthermore, elected conceptual modeling language (CML) must be intuitive and expressive enough to help modelers to produce flexible, reusable and intended models. In this paper, we are interested in studying and presenting anti-patterns. By an anti-pattern we understand a syntactically correct description in the particular CML that leads to an unintended model (i.e. it leads to construct excess, see Chap. 2 in [1]). In the scope of this paper, the considered CMLis the OntoUML language defined in [1], as a representant of a suitable wellfounded general purpose conceptual modeling language. The goal of this paper is to elaborate semantic anti-patterns identified during usage of OntoUML for modeling the aviation safety domain.

In recent decades, in the aviation safety community, there is an increasing amount of requirements especially relating to technology and performance. They understand the challenges facing industry and government today in challenging technologies, applications and procedures for the integration, analysis and presentation of business information to support better business decision-making. Aviation helps the global economy to grow. Thus, an increasing attention has been paid to the development of Aviation Safety, i.e. to improve aviation safety

systems, to enhance quality of safety data, and finally to avoid accidents and incidents in this domain. In the aviation safety community, there is a big effort to adopt techniques such as Business Intelligence on a national and international scale [4].

We came across the idea of this paper during our cooperation with the Civil Aviation Authority of the Czech Republic and several Czech aviation organizations including Prague airport or Air Navigation Services of the Czech Republic, within two national projects focused on IT support for aviation safety. Particular contributions of this paper include extension of UML class diagrams for representing UFO-B models, as well as novel ontological anti-patterns detected in those models.

Section 2 presents related work. In Sect. 3 we briefly define the notion of Unified Foundational Ontology (UFO) [1], which is a basis for OntoUML (one of Ontologically Well-Founded Conceptual Modeling languages). Section 4 discusses the possibility to extend OntoUML, in order to define and evaluate event and process based models. In Sect. 5 the use case and methodology used in our research is presented. Section 6 discusses ontological anti-patterns with their negative consequences [5-8]. In Sect. 7 we extend OntoUML towards perdurant modeling by introducing the notion of an Event and define anti-patterns in UFO-B models, identified during our work in design and model ontologies in the domain of Aviation Safety (AS). Finally, Sect. 8 shows some final considerations of this work.

## 2 Related Work

The main commonly used conceptual modeling languages are Nijssen's Information Analysis Method (niam), which provides a powerful grammar for generating conceptual schema diagrams NIAM [14], ER [15], UML which is a modeling language typically used in the field of software engineering, [16], and OWL [17]. Unified Foundational Ontology (UFO) started as a joint effort of Giancarlo Guizzardi and Gerd Wagner in 2001 to unify the General Ontological Language, which was a predecessor of the General Formal Ontology (GFO) proposed by Herre et al. [21] and the top-level ontology of universals underlying widely-used OntoClean methodology proposed by Guarino and Welty [13]. The main contribution of OntoClean was the beginning of a formal foundation for ontological analysis [13]. OntoUML is an ontologically well-founded UML extension based on the Unified Foundational Ontology (UFO) [2,11]. An ontology pattern OP is a modeling solution to solve a recurrent ontology design problem. It is a template that represents a schema for specific design solutions. An ontology design pattern ODP consists of a set of prototypical ontology entities that constitute the abstract form of a pattern, and of a set of metadata about its use cases, motivations, provenance, the pros and cons of its application, the links to other patterns, etc. Design solutions based on ODPs encode ontology entities that apply, specialize, or instantiate the prototypical entities defined by the schema [22].

## 3 UFO and OntoUML

We use OntoUML to illustrate anti-pattern detection problems. OntoUML is based on the Unified Foundational Ontology (UFO), which is a top-level ontology aimed at specifications of domain ontologies and languages. It can be used for evaluating business modeling methods and providing real-world semantics for their modeling constructs. In general, it aims at developing theories, methodologies and engineering tools with the goal of advancing conceptual modeling as a theoretically sound discipline but also one that has concrete and measurable practical implications [3]. UFO is divided into three layers:

- -UFO-A: Object and Trope model part (An Ontology of Endurants) [1].
- -UFO-B: Event and Process model part (An Ontology of Perdurants) [11] see Fig. 2.
- -UFO-C: Social and Agent model part (An Ontology of Intentional and Social Entities) [18].

As a top-level ontology, UFO distinguishes individuals and universals. Several categories of universals are applied in the UML metamodel for class diagrams in order to turn it into a well-founded conceptual modeling language named OntoUML. Selected universals, their relationships and restrictions are represented as UML stereotypes and OCL constraints. OntoUML has been successfully applied in different domains (e.g., Telecommunication, Business, Management, IT Governance, Services, etc.) see Fig. 1 (taken from [2]).

Fig. 1. Relation between concepts of domain ontologies and concepts of foundational ontology and OntoUML

[FIGURE]

## 4 OntoUML Perdurant Extension

The OntoUML metamodel uses ontological distinctions among the categories of object types (Kind, Subkind and Roles), trope types (Relator) and relations (formal and material relations) [1]. During our work in modelling Aviation Safety Events, we recognize that, there is persistent need to extend OntoUML metamodel to use perdurant individuals and universals (Event) types. Events are individuals that may be composed of temporal parts. They happen in time in the sense that they may extend in time accumulating temporal parts [12]. The ontology proposed in [1] accounts for a descriptive commonsensical view of reality, focused on structural (as opposed to dynamic) aspects. Taking UML, as a general-purpose CML, we believe that extending UML class diagrams with perdurants is beneficial for the sake of properly visualizing structural relationships of perdurants. Sequence diagrams, on the other hand might be used for visualization of temporal dependencies, that are however not handled in our approach and will be considered for future work.

To model an event system, we have to describe event types and object types, that event depends on them (their participants) in order to exist see Fig. 2. For any event type, we have to specify the state changes of objects and the follow-up events caused by the occurrence of an event of that type [12]. Conceptual process models are based on the event types, by OntoUML Class Diagrams. Almost all of the basic type concepts that participant in process are supported, the three categories of snapshot objects, event types and situations are not supported. Consequently, we have to add them to the Onto-UML profile in the form of the class stereotypes snapshot objects, event type and situations.

Extending OntoUML editor tools and adding new stereotypes makes it possible to define event based models, in order to help modelers to evaluate and improve the models produced using OntoUML conceptual modeling languages. The Object Constraint Language (OCL) is an expression language that helps modelers to formulate constraints in the context of a given UML model. OCL is used to specify invariants attached to classes, pre and post conditions of operations, and guards for state transitions [20]. But currently, it is important to specify OCL constraints over the dynamic behavior of a UML model, i.e., consecutiveness of states and state transitions as well as time-bounded constraints. However, it is essential to specify such constraints to guarantee correct system behavior, e.g., for modeling real-time systems [20]. OCL temporal retraction helps modelers to specify required occurrences of actions, events and states. Temporal constraints are a means to declaratively describe properties of components and the relation between them in event or temporal systems. The first constraint below states that endurant universal cannot be subclass of a perdurant universal; The second and third constraints specify that events should be connected to their participants via an existential dependence relation (entailing an immutability constraint in the association end connected to the types representing each participant), in (Participant of) relation the source must be Object (2nd constraint) and the target should be Event (3rd constraint).

- -allParents()-&gt; select(x | x.oclIsKindOf(ObjectClass) )-&gt; isEmpty().
- -participating().oclIsKindOf(ObjectClass).
- -participated().oclIsKindOf(Event).

Fig. 2. UFO-B, an ontology of events

[FIGURE]

## 5 Use Case and Methodology

In this paper we study ontological anti-patterns identified during building ontologies to model and analyze the domain of aviation safety, and add new (Event) stereotypes and (Participant of) relation that connects events to their participants to OntoUML, in order to raise the quality of model and to add the possibility for modeling process and event in Aviation Safety reality. In these efforts, to increase the awareness of analytical methods and tools in aviation community for safety analysis in aviation, our strategy is to build and design ontological conceptual models in the domain of aviation safety, analyze safety events that lead to incidents or accidents, and explain factors, that contribute to these safety events, in order to transfer impressible safe to incredibly safe. Within the projects we developed the aviation safety ontology and several domain specific ontologies for describing safety issues in specific organizations of the aviation industry. Thus, in this paper we consider the following domains and corresponding conceptual models developed with the OntoUML methodology:

- -A Conceptual Model representing the domain of aviation safety. It defines general well understood concepts in Aviation domain such as Aircraft, Flight, Agents and etc. (more detail in [23]). See Fig. 3.
- -A Conceptual Model that describes Ramp Error Decision Aid (REDA) Contributing Factors ontology. It describes conditions that contribute to a ramp system failure which lead to other event [9].
- -AConceptual Model that describes DSA (one of our partners in the project) is an organization providing various aviation services, e.g. flight school, medical flights, rescue flights, maintenance [19].

Fig. 3. Excerpt from the aviation safety ontology

[FIGURE]

## 6 Ontological Anti-patterns in UFO-A

A modeling language prevents the presentation of syntactically non valid state of affairs, but it cannot guarantee to have only desired instances [6]. According to [7], this is because the admissibility of domain specific state of affairs depends on domain specific rule not on the ontological one. To explain this situation, we studied the occurrence of these undesired consequences in our ontological conceptual models. This section presents some examples of ontological anti-pattern happened in UFO-A concepts (structural concepts), these types of anti-patterns are discussed in details in [5-8]. Figures 4 and 5 are taken from Aviation Safety ontology models, which represent the basic vocabularies, concepts and the relations between concepts in aviation safety domain (ASD). Figure4 represents Relation Between Overlapping Subtypes (RBOS) anti-pattern that defined in [5,6], it happens in a model having two potentially overlapping (i.e., non-disjoint) types T1 and T2 whose principle of identity is provided by a common Kind ST, and such that T1 and T2 are related through a formal relation R. According to the domain conceptualization, a Person can be a Student and a person can be an Instructor that teaches the Student. However, the same person cannot play both roles.

Figure 5 represents a binary relation between overlapping types (BinOver) anti-pattern that explained in [6], which Occurs when an association of any given meta-type connects two types that constitute an overlapping set. If this is the case, it means that the same individual may eventually instantiate both ends of the relationship.

Fig. 4. Example of RBOS anti-pattern

[FIGURE]

Fig. 5. Example of BinOver anti-pattern

[FIGURE]

## 7 Ontological Anti-patterns in UFO-B

Our research corresponds to the evaluation of models made during the development of aviation safety ontologies, and perform the evaluation of models in OntoUML editor tools (e.g., ontouml-lightweight-editor OLED) [10]. In order to make this evaluation, we need a mapping of the original models in UML to OntoUML class diagram syntax. Because most of our work depends on UFOB, which is not supported by OntoUML profile, we are interested in mapping UFO-B concepts to OntoUML syntax and applying anti-patterns detection algorithms to event types [11]. In this case, we can test the event model, detect undesired instances then terminate them. Within the research we could add new Event stereotype into OLED to represent UFO-B based concepts and relations. This section presents some parts of ontologies based on UFO-B models, and discusses some types of semantic anti-patterns related to those models.

## 7.1 Aviation Safety Ontology for Maintenance Organizations

In national aviation authorities, there will be a regulatory requirement to do reactive events and factors investigation in all aircraft maintenance organizations around the world. Thus we built ontologies (management ontology) to represent and model factors that are considered a part of management system, to define what may cause or contribute to incidents in order to directly reduce or eliminate the contributing factors to error or damage events. As a part of this domain, we designed an ontological model of the Ramp Error Decision Aid (REDA) Contributing Factors, while REDA is designed to investigate events caused by worker performance and that occurred during the receiving, unloading, servicing, maintaining, uploading, and dispatching of commercial aircraft at an airport [9]. REDA Contributing Factor is used to describe conditions that contribute to a ramp system failure which lead to other event. For example, if 'Incomplete or vague written communication' event happened it might become a factor of another event (e.g., ramp system failure). This Event model contains similar situation of Imprecise abstraction (ImpAbs) anti-pattern in UFO-A concepts, that defined by guizzardi in [5,6]. In perspective to [5] an association R characterizes the logical anti-pattern named Imprecise Abstraction (ImpAbs) if at least one of the following holds see Fig. 6:

- -R's source end upper bound multiplicity is equal or greater than 2 and the Class connected to it has 2 or more subtypes.
- -R's target end upper bound multiplicity is equal or greater than 2 and the Class connected to it has 2 or more subtypes.

Fig. 6. Imprecise abstraction anti-pattern

[FIGURE]

Fig. 7. Imprecise abstraction anti-pattern in REDA

[FIGURE]

Figure 7 shows REDA contributing factors (source) may cause some aerodrome operation events (target), this source has many subtypes, that may also cause aerodrome operation events, which in turn cause another event type called ramp system event.

## 7.2 Aviation Safety Ontology for High Risk Organizations

In recent years, an increasing attention has been paid to the development of the hazard taxonomy with the potential to be used throughout the aviation industry. This involves necessity for the approach to the problem, which does not exclude, in contrary it strongly supports finding a contributors or root causes that lead to the failure or accident realization [19]. As part of our work we designed models, which represent DSA ontology, see Fig. 8, in order to define hazard factors and events or problem related to these factors. We intend to detect semantic anti-patterns and avoid their occurrence in particular OntoUML event based models. However, OntoUML does not support event stereotypes that are important to evaluate and analyze our aviation safety events models. For example, during analyzing the results and instances, we faced some ambiguous states and undesired instances, and those unintended patterns are not defined in the catalogue of ontological anti-patterns in [5], that lead us to propose new type of semantic anti-pattern called (Imprecise Intersection). Imprecise Intersection anti-patterns occurs in a model having at least two Event types E1, E2 and every type has at least one joint subevent type SE, two relations R1, R2 connect this subevent type to different Event types (e.g., E5, E4), or to same type (e.g., E5) see Fig. 9.

Fig. 8. Excerpt from DSA model

[FIGURE]

Fig. 9. Imprecise intersection anti-pattern

[FIGURE]

To exemplify this anti-pattern type, consider the following fragment of the DSA ontology, which contains Imprecise Intersection anti-pattern depicted in Fig. 10. The ontology searches for potential hazards from each of the defined categories, the most relevant categories are: characteristics airport, communication, human factor, operating environment, organization factor and Service factor, in order to reach correct comprehension of the analyzed event. Detected hazard defined in any category does not exclude hazards from the other categories, in other words it tries to find potential causes of event by deeper analysis and determination of the events chain. According to this model, psychological action-procedure violation 103010400 event, which considers in Hazard taxonomy both human and organization factor event type, it causes both (Push-back or taxi interference) event if it is related to organization factors and

Fig. 10. Imprecise intersection anti-pattern in DSA

[FIGURE]

Fig. 11. Imprecise intersection anti-pattern solution

[FIGURE]

(Runway incursions) event if it is related to human factors, which may lead to undesired consequences and unintended instances because of this Imprecise Intersection situation. To solve this undesired consequences, we propose to remove this intersection and add new two associations.

Figure 11 proposes to delete this intersection between event types and define new two associations to define the intended consequences, as solution to this type of anti-pattern.

In this model when for example psychological action-procedure violation 103010400 event happens, either human or organization factors are responsible for its happen. Thus regarding to (Participant of) relation that connect event to its participants, psychological action-procedure violation 103010400 event has human and organization participants see Fig. 12.

Fig. 12. Imprecise intersection anti-pattern solution

[FIGURE]

## 8 Final Consideration

In this paper, we discuss how ontological anti-patterns cause undesired consequences in ontological conceptual models, especially in Aviation Safety event models, in order to help designer to produce intended model, increase the accuracy of conceptual models and improve a conceptual model assessment tool based on Unified Modeling Language (UML) that assumes a well-founded conceptual modeling language named OntoUML. We present new ontological anti-patterns happened in UFO-B models called imprecise intersection anti-pattern.

We also add (Event) stereotype and (Participant of) relation that connects events to their participants to OLED to have the possibility for modeling UFO-B concepts based models and present some OCL restrictions regarding to perdurant concepts.

Acknowledgments. This work was supported by grant No. GA 16-09713S Efficient Exploration of Linked Data Cloud of the Grant Agency of the Czech Republic and by grant No. SGS16/229/OHK3/3T/13 Supporting ontological data quality in information systems of the Czech Technical University in Prague.

## References

1. Guizzardi, G. Ontological Foundations for Structural Conceptual Models, Ph.D. thesis (CUM LAUDE), University of Twente, the Netherlands. Published as the book Ontological Foundations for Structural Conceptual Models, Telematica Instituut Fundamental Research Series No. 15. ISBN 90-75176-81-3 ISSN 1388-1795; No. 015; CTIT Ph.D. thesis, ISSN 1381-3617; No. 05-74
2. Carraretto, R., A modeling infrastructure for OntoUML, B.Sc. thesis, Federal University of Esprito Santo (2010)
3. Guizzardi, G., Wagner, G., Almeida, J.P.A., Guizzardi, R.S.S.: Towards ontological foundations for conceptual modeling: the unified foundational ontology (UFO) story. Appl. Ontol. 10 (3-4), 259-271 (2015)
4. [http://eccairsportal.jrc.ec.europa.eu. Accessed 4 Oct 2016](http://eccairsportal.jrc.ec.europa.eu/)
5. Sales, T.P., Guizzardi, G.: Ontological anti-patterns: empirically uncovered errorprone structures in ontology-driven conceptual models. Data Knowl. Eng. 99 , 72104 (2015)
6. Guizzardi, G.: Formal ontology, patterns, anti-patterns for next-generation conceptual modeling. In: KDIR 2015, p. 9 (2015)
7. Guizzardi, G.: Ontological patterns, anti-patterns and pattern languages for nextgeneration conceptual modeling. In: Yu, E., Dobbie, G., Jarke, M., Purao, S. (eds.) ER 2014. LNCS, vol. 8824, pp. 13-27. Springer, Heidelberg (2014)
8. Guizzardi, G., Sales, T.P.: Detection, simulation and elimination of semantic antipatterns in ontology-driven conceptual models. In: Yu, E., Dobbie, G., Jarke, M., Purao, S. (eds.) ER 2014. LNCS, vol. 8824, pp. 363-376. Springer, Heidelberg (2014)
9. Ramp Error Decision Aid (REDA) Users Guide (2013)
10. Sales, T.P., Guizzardi, G., Almeida, J.P.A.: OntoUML lightweight editor: a modelbased environment to build, evaluate and implement reference ontologies. In: EDOC Workshops, pp. 144-147 (2015)
11. Guizzardi, G., Wagner, G., de Almeida Falbo, R., Guizzardi, R.S.S., Almeida, J.P.A.: Towards ontological foundations for the conceptual modeling of events. In: Ng, W., Storey, V.C., Trujillo, J.C. (eds.) ER 2013. LNCS, vol. 8217, pp. 327-341. Springer, Heidelberg (2013)
12. Guizzardi, G., Wagner, G.: Towards an ontological foundation of discrete event simulation. In: Winter Simulation Conference 2010, pp. 652-664 (2010)
13. Guarino, N., Welty, C.A.: An overview of OntoClean. Laboratory for Applied Ontology (ISTC-CNR) Polo Tecnologico, Via Solteri 38, 38100 Trento, ITALY guarino@isib.cnr.it . IBM Watson Research Center 19 Skyline Dr., Hawthorne, NY 10532, USA
14. Weber, R., Zhang., Y.: An Ontological Evaluation of NIAMs Grammar for Conceptual Schema (1991)
15. Wand, Y., Storey, V.C., Weber, R.: An ontological analysis of the relationship construct in conceptual modeling. ACM Trans. Dtatabase Syst. 24 (4), 494-528 (1999)
16. Evermann, J., Wand, Y.: Towards ontologically based semantics for UML constructs. In: Kunii, H.S., Jajodia, S., Sølvberg, A. (eds.) ER 2001. LNCS, vol. 2224, p. 354. Springer, Heidelberg (2001)
17. Brea, P., Wand, Y.: Analyzing OWL using a philosophy-based ontology. In: Formal Ontology in Information Systems. IOS press, Amsterdam (2004)

18. Julio, C.N., de Almeida Falbo, R., Almeida, J.P.A., Guizzardi, G., Pires, L.F., van Sinderen, M., Guarino, N.: Towards a commitment-based reference ontology for services. In: EDOC 2013. pp. 175-184 (2013)
19. http://www.dsa.cz/. Accessed 4 Dec 2016
20. Flake, S., Mueller, W.: A UML Profile for Real-Time Constraints with the OCL
21. Herre, H., Heller, B., Burek, P., Hoehndorf, R., Loebe, F., Michalek, H.: General Formal Ontology (GFO) 8 (July 2006)
22. Gangemi, A.: Ontology design patterns for semantic web content. In: Gil, Y., Motta, E., Benjamins, V.R., Musen, M.A. (eds.) ISWC 2005. LNCS, vol. 3729, pp. 262-276. Springer, Heidelberg (2005)
23. [http://www.inbas.cz/ontologie. Accessed 20 June 2016](http://www.inbas.cz/ontologie)
