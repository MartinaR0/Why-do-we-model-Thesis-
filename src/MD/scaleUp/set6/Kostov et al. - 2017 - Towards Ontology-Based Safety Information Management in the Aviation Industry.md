## Towards Ontology-Based Safety Information Management in the Aviation Industry

Bogdan Kostov ( B ) , Jana Ahmad, and Petr Kˇ remen

Faculty of Electrical Engineering, Czech Technical University in Prague, Praha, Czech Republic { bogdan.kostov,jana.ahmad,petr.kremen } @fel.cvut.cz

Abstract. Aviation is a high risk industry where safety management is mandatory for organizations. On a global scale, safety management is hierarchical, i.e. national authorities manage safety of the sector, controlling organizations which in turn manage safety of their operations, as well as the safety of their organizational units. It is apparent that safety information management is a key factor to the success of safety management. Improving safety information management in aviation can be achieved by the systematic documentation of safety information and its seamless sharing vertically as well as horizontally through the management hierarchy. Despite attempts to tackle this problem, the industry still suffers from information management issues, e.g. usage of terminologically incompatible safety management frameworks. As a result diverse information repositories, e.g. investigation reports, safety recommendations, or audit reports managed by these frameworks, cannot be efficiently explored and compared. We apply Linked Data principles, e.g. searchability and explorability based on dataset descriptors, to help solving the problem. In this work we propose an ontology-based safety information management for the aviation industry. To achieve this we develop the Aviation Safety Ontology that is modular and covers the contexts of the organization types aerodrome, airline, air traffic management, maintenance and the state civil aviation authority. We test the appropriateness of the proposed ontology by representing safety data in terms of the ontology.

## 1 Introduction

Aviation is a high risk industry where safety management is mandatory for organizations. Since the first steps towards aviation safety starting with regulations published in the 1920s in the USA, the industry observes reduction of the incident/accident rates [2]. Lower incident rates and the effort to further improve the quality of safety took the industry on a road towards adopting the proactive rather than the reactive safety approach. The reactive approach is based on dealing with incidents after they happen. Proactive safety tries to predict and prevent incidents before they happen. In his work [22], Reason argues that proactive safety can be achieved trough tackling safety breaches using the system approach. Safety management in the aviation industry, on a global scale, is

hierarchical and highly distributed, e.g. national authorities manage safety of the sector, controlling organizations which in turn manage safety of their operations, as well as the safety of their organizational units. Implementing Reason's ideas on a global scale in practice requires seamless Safety Information Management and Sharing (SIMS) [23]. Despite efforts towards improvement, the problem of global and seamless SIMS remains. A key factor of the quality of SIMS is that the design and implementation of safety data management systems is based on safety standards, manuals and legislation which use incompatible terminologies, hence inducing the information silos problem [13].

Linked Data principles address the information silos problem found in SIMS. In this work we present the Aviation Safety Ontology (ASO), a candidate shared ontology. We present an evaluation of ASO by integration of incident and audit reports. Furthermore, the resulting datasets are used to design content based dataset descriptors, such as summary descriptors [9], which will improve searchability and explorability of safety data.

The rest of the paper is structured as follows. In Sect. 2 we discuss the state of art and point out our contributions. In Sect. 3 we briefly describe our ontology engineering methodology. Section 4 presents the modules of ASO. Section 5 presents core modules of ASO. Subsect. 5.1 describes the aviation domain ontology. Subsect. 5.2 describes the Safety task ontology. In Sect. 6 presents the evaluation methodology of ASO. In Sect. 7, we conclude and discuss future work.

## 2 Related Work

In practice, there are many safety standards and manuals, [4,5,21] to name a few. Other initiatives try to define vocabularies where common aviation safety terms are defined, e.g. [1,3,11]. The ECCAIRS system [11] stands out because it defines an XML based machine communication interface [12]. The main problem is however that they target specific use-cases and use incompatible terminologies. Although these documents and tools are based on a common conceptualization and help unify and improve the safety management process, they use incompatible terminologies.

In the paper [6] the authors describe the development of an aircraft design ontology designed to facilitate the collaboration among experts. This work is relevant in the domain of aviation and it covers some common concepts like the Aircraft and its sub-components.

In the paper [19] the authors propose an ontology for Operational Risk Management (ORM) to facilitate the ORM related information sharing across organizational unit boundaries. The proposed ontology is domain independent and it defines the relevant generic concepts used on ORM. An essential part of ORM is the documentation of events. The work found in [16,17] lays the ontological foundations for the representation events and it allows for the representation of event instances (such as incidents and audit findings) as well as event types (such as risk and hazards).

In our work we contribute by designing an Aviation Safety Ontology. We design the ontology based on domain terminology found in aviation safety standards and manuals (e.g. [1,3,5,11]) as well as safety data found in incident and audit reports. We combine the domain terminology with relevant and well defined state of art conceptualizations.

## 3 Ontology and Ontology Engineering Methodology

The term ontology (in other words the study of existence) originates in philosophy. In computer science, there are several definitions of what is an ontology. We adopt the definition found in [24] - ' An ontology is a formal, explicit specification of a shared conceptualisation '.

There are four different types of ontologies, i.e. foundational ontologies, domain ontologies, task ontologies and application ontologies. Foundational ontologies provide definitions of fundamental concepts and relations used to describe reality, e.g. Endurant, Perdurant or Universal, see Sect. 3.1. Domain ontologies focus on a specific domain of discourse and should use a foundational ontology to describe the terminology of the domain. Task ontologies focus on a specific task which might be shared across multiple domains. And finally, an application ontology is one that specifies the application of a given task in a given domain.

We can divide the development of ASC in two main activities. The first is identifying and developing domain and task ontologies, further referred to as core ontologies , that cover well defined conceptualizations of the studied problem aligned with the foundational ontology. The second activity is developing application ontologies based on different use-cases. In this work we consider application ontologies which are found in five different contexts, i.e. aerodrome, airline, air traffic management, maintenance and the state civil aviation authority contexts. We employ an agile methodology based on RapidOWL [7] and Methontology [14].

## 3.1 Unified Foundational Ontology (UFO)

We build our ontology on top of the Unified Foundational Ontology (UFO) [15]. We choose to use UFO because it is grounded in literature from the fields of Formal Ontology, Cognitive Psychology, Linguistics, Philosophy of Language and Philosophical Logics. To the best of our knowledge UFO modules are not distributed as OWL 2 ontologies, the implementation language of our choice. Although there are transformations between from UFO to OWL [8] they are consider only on the UFO-A module. Our implementation of UFO modules, including UFO-B and UFO-C, in OWL 2 is based on the OLED's simple transformation [8].

UFO consists of a static object model part (UFO-A) [15], an event model part (UFO-B) [17] and a social and agent model part (UFO-C) [20]. The ontology particulars are split into endurants and perdurants, where endurants are:

- -Agent: is a proactive object, it has its own beliefs, intentions, and goals.
- -Physical object: which is a complex of:
- Spatial Object: An object with spatial extent. It can provide reference for locating other objects.
- Technical System: (such as Equipment, Power System, Vehicles)
- -Service: service which is provided by some agent to another agent.
- Data, Weather

## and perdurants are:

- -Event: temporal entity, e.g. a runway incursion is an event that describes incorrect entrance of an object on the runway
- -Object Snapshot: is an immutable state description of an object within a situation.
- -Situation: is a snapshot of object states valid in the given temporal range.

The overall structure of the UFO ontology is shown in the Fig. 1.

Fig. 1. Main concepts of the UFO ontology

[FIGURE]

## 4 Aviation Safety Ontology

The ASO ontology we present emerges from the requirements we designed in the Aviation Domain analysis phase. Our observation is that most safety related data and information deals with the description perdurant types (e.g. factor types, risks, barriers) and of their instances (e.g. incident, audit finding). Obviously perdurant descriptions are based on endurants, e.g. persons pilot role in an flight event or the the level traffic flow in a situation. Upon review of safety manuals and standards we reveal that there are many vocabularies and taxonomies. Alignment of terminology found in these documents is done with the help of experts.

During the analysis of the aviation safety domain we identify several modules and relationships among them, see Fig. 2. The modules in the figure are divided in two, the Safety Aviation Core (ASC) ontology (on the left) and Application Onotologies (on the right). The ASC ontology contains concepts and relations common in the domain. ASC is composed of the modules containing Aviation, Safety, Documentation, Communication and Organizational Process.

Fig. 2. Modules of the ASC

[FIGURE]

ASO and our implementation of UFO are distributed as OWL 2 ontologies 1 . Currently the ontology has ontology has 11255 axioms, 3165 classes, 1865 object properties and its expressivity is SHIQ ( D ). In this work we present the modules Aviation and Safety of the ASC in Sect. 5. The rest of the ASC modules are subject to future work.

## 5 Aviation Safety Core

## 5.1 Aviation Ontology

This ontology consists of the common aviation domain terms, such as Aircraft and Flight. Figure 3 depicts a simplified version of the Aviation Ontology represented in UFO. The Object classes (those that belong to the class hierarchy with root class Object or their parts) are aircraft, vehicle, agent, aerodrome part, equipment, etc. Agent actions are on the left side. On the right, we have a categorization of safety events and also other operational events such as Flight Stage .

[1 http://www.inbas.cz/aviation-safety-ontology.](http://www.inbas.cz/aviation-safety-ontology)

Fig. 3. Aviation domain ontology

[FIGURE]

The purpose of this conceptualization is to serve as a definition language for safety aviation application ontologies. This can help define specific application classes in a more compatible fashion across different applications. For example terms for aircraft parts such as engine or fuel system refer to the same meaning regardless of the context, e.g. maintenance or flight operator context.

## 5.2 Safety Ontology

This ontology consists of the fundamental conceptualizations necessary for the management of safety information. Generally the concept of safety can be defined as the state of acceptable level of risk . Safety management can be defined as a process which improves the level of safety . In the aviation industry, safety is concerned only with flight risks. Such risks are for example considers risk of aircraft damage, property damage and loss of life during the servicing of regular commercial flight operation. On the other hand aviation safety does not count with, for example, financial risks. As the definition of safety is based on the concept of risk we align our safety ontology module to the conceptualization of Risk Management (RM) presented in [19] which is based on the ISO 31000 standard [18]. The proposed module is enriched by UFO based semantics. Figure 4 shows part of the Safety ontology. On the left we have present the conceptual model for necessary for term definitions, i.e. Term Type 2 . We define two categories of term types Object Types and Safety Aviation Event Type s. The has factor relation and its sub properties is contribution and is mitigation (not shown in the figure), are used to define a risk graph of event types. On the right are shown events that happen during Operation and are typically documented, i.e. Incident and Audit finding .

Fig. 4. Conceptual model of factors

[FIGURE]

## 6 Evaluation of ASO

The evaluation of ASO is twofold, first by building application ontologies we evaluate the ASC modules and second we conduct an application based evaluation. The application ontologies created for each organization type should represent the organizational structure, its documentation, operational processes and their risk management strategies. Our goal is to be able to represent incident/risk graphs , i.e. event/event-types which are factors of incidents/risks. The relevant contents of the application ontologies in this context is taxonomies of relevant entity types, e.g. taxonomy of factors and incidents, type of operations, types of equipment. We look for such taxonomies in the following sources: data schema and taxonomies used in the European Coordination Center for Accident and Incident Reporting System (ECCAIRS) [11]; The Ramp Error Decision Aid (REDA) [5].

For the sake of brevity we will discuss the task ontology only for the Aerodrome organization type and REDA safety manual. The evaluation in the other organization types is similar. REDA describes the investigation of incidents caused by worker performance that occurred during the receiving, unloading, servicing, maintaining, uploading, and dispatching of commercial aircraft at an airport. The manual systematically decomposes the ramp operational process and its environment into components such as involved agents, agent operations and systems. Based on this description the manual further defines safety event categories, i.e. taxonomy of human factors, system failures and incidents. Listing 1 shows an example of the knowledge found in REDA.

2 Powertypes are classes whose instances of are also classes.

```
1 I n c i d e n t asc : hasTypicalContributingFactor SystemFailure , ContributingFactor . 2 ContributingFactor asc : hasTypicalContributingFactor InformationNotUsed , 3 InformationNotUnderstood , InformationUnderstood . 4 I n c i d e n t asc : hasTypicalMitigatingFactor InformationUnderstood . 5 Information aso : isFactorSubjectOf InformationNotUsed , 6 InformationNotUnderstood .
```

Listing 1. Representation of Knowledge found in REDA shown in Turtle [10] (RDF serialization format)

Line one in Listing one to four 1 shows the usage of the properties asc:hasTypi -calContributingFactor and asc:hasTypicalMitigatingFactor (sub properties of asc: hasTypicalFactor ) to represent the typical factor graph found in REDA. Lines five to six show how to associate factors with their subject subject.

Furthermore, we conduct an application based evaluation of ASO. Experts evaluate ontology data using a web based application developed for the purpose of viewing and editing reports. We import heterogeneous structured data into the ontology using a schema to ontology mapping. The resulting data is then revised by domain experts through the application. ASO's coverage of the domain is evaluated by enriching imported structured data with additional information about factors, events, participants and their tropes found in full-text descriptions. This way experts discover limitations which are taken as requirements for the next update of ASO. Currently the dataset contains over 250 K triples. Table 1 shows instance count per individual ASO classes.

Table 1. Dataset statistics

| Type                |   Count |
|---------------------|---------|
| Aerodrome           |     555 |
| Air traffic service |     555 |
| Loss of separation  |     374 |
| Occurrence          |     587 |
| Runway              |     187 |
| License             |     187 |
| Factor              |      67 |

## 7 Conclusion

In this work we analyze the domain of Aviation for the purpose of SIMS. We confirm that the information silos problem is a key factor of the quality of SIMS. We address this factor using Linked Data principles. Specifically we design and develop the Aviation Safety Ontology (ASO) to be used to align diverse aviation safety information. The designed ontology is modular. The part of ASO presented in this paper targets the description of events and event types which is the most common type of information found in aviation safety.

In future work we will target the rest of the modules of ASC. Furthermore, usage of ASO for representing safety data set descriptors will be elaborated. For example, the Air Accidents Investigation Institutes of the Czech Republic maintains a set of aviation investigation reports that might be formally described by an index of Report s describing Safety Event s having Aircraft s present in the Czech Republic or registered in the Czech Republic as participants. Such descriptors might be used to efficiently retrieve relevant aviation safety data sets.

Acknowledgment. This work was supported jointly by grants No. GA 16-09713S Efficient Exploration of Linked Data Cloud of the Grant Agency of the Czech Republic and No. TA04030465 Research and development of progressive methods for measuring aviation organizations safety performance of the Technology Agency of the Czech Republic.

## References

1. Lexicon, A.T.M.: www.eurocontrol.int/lexicon/lexicon/en/index.php/Main Page. Accessed 1 Aug 2016
2. Causes of Fatal Accidents by Decade. http://www.planecrashinfo.com/cause.htm. Accessed 1 Aug 2016
3. Glossary, I.: www.intlaviationstandards.org/apex/f?p=240:1:15338757287208:: NO::P1 X:Glossary. Accessed 1 Aug 2016
4. International Air Transportation Association (IATA) Standards, Manuals and Guidelines. http://www.iata.org/publications/Pages/standards-manuals. aspx. Accessed 1 Aug 2016
5. [Ramp Error Decision Aid (REDA) User's Guide, 2013. http://www.faa.gov/ about/initiatives/maintenance hf/library/documents/media/media/reda users guide v-8 september2013.pdf. Accessed 1 Aug 2016](http://www.faa.gov/about/initiatives/maintenance_hf/library/documents/media/media/reda_users_guide_v-8_september2013.pdf)
6. Ast, M., Glas, M., Roehm, T., Luftfahrt, B.: Creating an ontology for aircraft design. Deutscher Luft- und Raumfahrtkongress 2013 (2013)
7. Auer, S., Herre, H.: RapidOWL - an agile knowledge engineering methodology. In: Virbitskaite, I., Voronkov, A. (eds.) PSI 2006. LNCS, vol. 4378, pp. 424-430. Springer, Heidelberg (2007). doi:10.1007/978-3-540-70881-0 36
8. Barcelos, P.P.F., Dos Santos, V.A., Silva, F.B., Monteiro, M.E., Garcia, A.S.: An automated transformation from OntoUML to OWL and SWRL. CEUR Workshop Proc. 1041 , 130-141 (2013)

9. Blaˇ sko, M., Kostov, B., Køemen, P.: Ontology-based dataset exploration - a temporal ontology use-case. In: Intelligent Exploration of Semantic Data (IESD 2016), Kode (2016)
10. Carothers, G., Prud'hommeaux, E.: RDF 1.1 Turtle. W3C Recommendation, W3C, February 2014
11. J.R. Center. European Coordination Center for Accident and Incident Reporting (ECCAIRS)
12. ECCAIRS: ECCAIRS data bridge. Technical report, Joint Research Centre of the European Commission (2015)
13. Ensor, P.S.: The functional silo syndrome. AME Target 16 ((Spring Issue)), 16 (1988)
14. Fern´ andez-L´ opez, M., G´ omez-P´ erez, A., Juristo, N.: Methontology: from ontological art towards ontological engineering, March 1997
15. Guizzardi, G.: Ontological foundations for structural conceptual models. Ph.D. thesis, University of Twente, The Netherlands, March 2005
16. Guizzardi, G., Wagner, G.: Towards an ontological foundation of agent-based simulation. In: Proceedings of the Winter Simulation Conference, Phoenix, Dec. Winter Simulation Conference, pp. 284-295 (2011). http://dl.acm.org/citation.cfm? id=2431518.2431549
17. Guizzardi, G., Wagner, G., Almeida Falbo, R., Guizzardi, R.S.S., Almeida, J.P.A.: Towards ontological foundations for the conceptual modeling of events. In: Ng, W., Storey, V.C., Trujillo, J.C. (eds.) ER 2013. LNCS, vol. 8217, pp. 327-341. Springer, Heidelberg (2013). doi:10.1007/978-3-642-41924-9 27
18. ISO: ISO/FDIS 31000 risk management-principles and guidelines. Technical report, International Organization for Standardization, Geneva, Switzerland (2009)
19. Lykourentzou, I., Papadaki, K., Kalliakmanis, A., Djaghloul, Y., Latour, T., Charalabis, I., Kapetanios, E.: Ontology-based operational risk management. In: 13th IEEE Conference on Commerce and Enterprise Computing, CEC 2011, Luxembourg-Kirchberg, Luxembourg, 5-7 September 2011, pp. 153-160 (2011)
20. Nardi, J.C., Falbo, R.d.A., Almeida, J.P.A., Guizzardi, G., Pires, L.F., van Sinderen, M.J., Guarino, N.: Towards a commitment-based reference ontology for services. In: 2013 17th IEEE International Enterprise Distributed Object Computing Conference, pp. 175-184. IEEE, September 2013
21. International Civil Aviation Organization: Safety Management Manual (SMM) (2013)
22. Reason, J.: Human error: models and management. BMJ (Clin. Res. ed.) 320 (7237), 768-770 (2000)
23. Rodriguez, E., Edwards, J.: People, technology, processes and risk knowledge sharing. Electron. J. Knowl. Manag. 8 (1), 139-150 (2010)
24. Studer, R., Benjamins, V., Fensel, D.: Knowledge engineering: principles and methods. Data Knowl. Eng. 25 (1-2), 161-197 (1998)
