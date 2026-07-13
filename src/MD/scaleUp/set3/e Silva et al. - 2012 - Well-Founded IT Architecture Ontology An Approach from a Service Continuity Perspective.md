## Well-Founded IT Architecture Ontology:

## An Approach from a Service Continuity Perspective

Hedwio Carvalho e Silva 1 , 2 , Rita de Cassia Cordeiro de Castro 1 , 2 , Marcos Jose Negreiros Gomes 1 , and Anilton Salles Garcia 3

1 Professional Masters in Applied Computing,

State University of Ceara, Fortaleza, Ceara, Brazil negreiro@graphvs.com.br

2 Telematics Department,

Federal Institute of Education, Science and Technology of Ceara, Fortaleza, Ceara, Brazil

{ hedwio,rita } @ifce.edu.br

3 LabTel - Telecommunications Research Laboratory,

Electrical Engineering Department,

Federal University of Espirito Santo, Vitoria, ES, Brazil

anilton@inf.ufes.br

Abstract. This paper presents an ontology model of the IT architecture to corporations that aim to set up an architecture made to the service continuity. This model describe the IT components, the IT Service Continuity components and other entities, and the relationship between them. The article is based in two pillars: the internationals standards guiding the IT service continuity, specially the PAS 77:2006, and the Unified Foundation Ontology (UFO) in order to build a well-founded ontology. The ontology model is built using the Conceptual Model Language OntoUML with the objective of preserving the ontologic prerogatives defined in the UFO. At last, this paper will show an ontologic evaluation of the IT architecture described in the PAS 77:2006 standard.

Keywords: IT Service Continuity, IT Architecture, Ontologies, Conceptual Models.

## 1 Introduction

The Data Processing Centers (DPC) have gain mush larger proportions since the time in which the computation was based on big computers with centralized processing in a room big enough to fit them. The evolution of the DPCs is what today is known as Data Centers, whose concern about infrastructure go beyond the physical dimensions and the refrigeration capabilities.

Several standards and/or recommendations have been established to guide corporations regarding the Information Technology (IT) infrastructure. Two of these publications are the pillars to the IT Service Continuity Management

(ITSCM): [1] and [2]. The first document, published by the British Standart Institute (BSI), british government's body of patterns, in partnership with the Adam Continuity, Dell corporation, Unisys and SunGard is intended to the ones in charge of the ITCSM's implementation inside the organization, because it present a pratice code for the IT service continuity management. This publication guide this work due a greater level of details using the IT architecture. The second document present directives to recovery services after a disaster in the Communication and Information Technology (CIT) to be adopted by the services providers. Nevertheless, even with standards, minor practices and publications referring the knowledge domain of the ITSCM, the IT architecture lacks the formal model capable of identifying it in an unique form. This model build using ontologies is discussed in this paper.

## 2 Related Work

Ontologies have been used from context detection field [3] passing IT management good practice [4] [5] [6] until ontologies for standards and/or recommendations [7] [8] [9].

Some interesting works have been identified in domain ontologies for IT service management area. [10] proposes an identification and hierarchical decomposition of IT services based on ontologies. But [11] presents a proposition of a heavy-weight ontology to provide structured knowledge about the relationship between threats, safeguards and actives, crucial in the modeling of risk orientated business processes. The construction of ontological models to the formal specification of processes used in ITIL has also been focus of some works. In [4] is presented a conceptual proposition in the domain of configuration management, in the context of services management and IT governance, based on foundation ontologies. After this, [5] extend the [4] model presenting how these concepts modeled by ontologies can be implemented and applied in computational systems. [6] also presents a conceptual model using foundation ontologies, but concerning the management process in the service level of the ITIL library domain. To achieve that, it makes use of the foundation ontology UFO to build the conceptual model.

Ontology based on standards and/or recommendations is another area with interesting work. [4] and [6] propose conceptual models of ITIL library domain. While [4] model the domain of configuration management, [6] addresses the domain of the service level. [12] show the most relevant questions found during the implementation process of ontologies to transport's optical networks using a direct implementation in Web Ontology Language (OWL). A initial version of the conceptual model to the ITU-T G.805 recommendation is presented in [7]. In [8] is presented a reference model on ontology developed to the ITU-T G.805 recommendation, including the conceptual model and its derivation's and restriction's rules. At last, in [9] an ontological evaluation of the referred recommendation is done. Some new works present itself as an extension of previous works. [6] extended a work regard a management module starting to follow recommendations. And [8] included a conceptual model, besides other improvements to the ontology built by [12].

The existing IT architecture present nowadays in the corporations suffer a great dependency of the IT equipments manufacturers' orientations and the suppliers of data center solution. The ontological model build present itself as a strong ally of the corporations, once it minimizes this dependency.

Thus, the main contribution of this paper is present a solution to the IT architecture's interoperability problem of the data center through the conceptual model produced. This model can be utilized as premise to the construction of a implementation model and, afterward, of an application capable of identifying IT and ITSC components and, eventually, propose updates to the components to the adequacy to the model. A second contribution results in the ontological evaluation of the specification PAS 77 which identifies a few deficiencies in some concepts, allowing a better understanding of the publication and the possibility of the adequacy of the text to ontological precepts.

This paper presents a conceptual model well based build using the foundation ontology UFO e through the representation language of ontologies OntoUML. An rundown of this characteristics can be found in Table 1.

Table 1. Characteristics of the Ontology model of the IT Architecture

| Characteristics                      | Proposed model   |
|--------------------------------------|------------------|
| Modeling Type                        | Conceptual Model |
| Utilizes norms and/or documentations | PAS 77:2006      |
| Foundation Ontology                  | UFO              |
| Representation Language              | OntoUML          |
| Domain                               | IT Architecture  |

The approach utilized is based on [13] when defends a language's conceptual model to represent a collection of real world's phenomenons in a determined domain Universe of Discourse can be systematically assessed, comparing the homomorphism level between a concrete representation ( specification ) of the view of the underlying world to the language with a explicit and formal representation of a concretion of this domain, called reference ontology . The Figure 1 represents the proposition of [13] contextualized this paper's scope. The Universe of Discourse in question is the IT architecture . The concrete representation used is the PAS 77 specification and the explicit representation and formal conceptual of this domain is the IT architecture ontology under the view of service continuity .

Based on this approach, an ontological evaluation of the IT architecture described on PAS 77 is represented on section 5 and utilizes the framework developed by [13]. This framework utilizes a conceptual model as reference to the evaluation, under the ontological aspects, the isomorphism level between the specification and the reference model. The complete correspondence complete between the specification's concept and the reference model's concept is what characterizes the isomorphism. If this correspondence isn't complete, these concepts are passive of various interpretations. Some formal criterion must be considerate to guarantee the isomorphic mapping: lucidity, laconicity, solidity, e completion [13]. The absent of these criterion represent the ontological problems: constructor overload, constructor excess, constructor redundancy, incompletion, as Fig. 2 shows. The constructors represent the concepts, being one constructor to each concept.

Fig. 1. Approach to model building and evaluation ontological

[FIGURE]

Fig. 2. Ontological problems due to lack of isomorphism between the universe of discourse and specification. Based on [14].

[FIGURE]

The construct overload is characterized by a constructor specification associated to more than one constructor of the Universe of Discourse. The constructor redundancy associate itself one constructor from the Universe of Discourse mapped to more than one constructor's specification and the incompletion is referred to the lack of mapping of one constructor of the Universe of Discourse to one constructor's specification.

## 3 Theoretical Fundaments

## 3.1 The IT Architecture under the View of Service Continuity

According to [1], the ITSCM is the collection of policies, patterns, processes and tools through which the organizations not only improve its capabilities to act when failures occur in the main systems, but also improve its resilience against worst accidents. To [15] the objective of ITSCM is support the global process of Management of Business Continuity, guarantying the IT the technical means needed (including computer systems, network, applications, data repository, telecommunications, environment, technical support and service desk) so the services can be back to normal within the accorded criteria. According to [1] to the IT Service Continuity Management, there is a relationship between the strategy of IT, the strategy of IT service continuity (ITSC), IT architecture and the IT service continuity plans as Fig. 3 shows.

Fig. 3. Relationship between IT strategy, ITSC strategy, IT architecture and ITSC plan. [1]

[FIGURE]

Yet according to [1], the IT strategy defines the principal organization politics and direction concerning information technology, systems and services. From it, the ITSC strategy can be defined to guarantee that the politics and standards to the IT service continuity direct and explicity may support the objectives defined in the IT strategy. This permit the organization define it IT architecture based on the requisites and objectives defined in the IT strategies and IT service continuity. Once the architecture is defined, the IT organization may, then, define IT service continuity plans to each element of the architecture. Feedback about the ITSC plans can later be used as input for the next iteration of the IT strategy.

From the perspective of the IT architecture and the IT service continuity, publishing [1] is a valuable reference for setting out the principles and some technical recommendations for the management of IT service continuity. The specification served as the basis for creation of ISO 24762 Standard [2], which deals with guidelines for disaster recovery services in Information Technology and Communications and presents itself as a complement to publications:

- -PAS 56 - provides guidance on best practices in Business Continuity Management and mentions the need for IT service continuity;
- -BS ISO / IEC 20000 - provides guidance on best practices in IT Service Management and as PAS 56, mentions the IT Service Continuity;
- -ISO / IEC 17799:2005 - Provides detailed guidance on best practices in information security management, which is one aspect of IT Service Continuity;
- -ISO 9001 - provides guidance on best practices in Quality Management Systems.

## 3.2 UFO Foundation Ontology

Domain concepts and, consequently, domain ontologies are established by consensus of a community of knowledgeable users of a domain material, a conceptual modeling language, which can be used to express these ontologies and domain must be rooted in a system of categories real-world cognitively and philosophically independent of the domain. So, will be based on a foundation ontology.

A UML-based language capable of meeting the requirements for the construction of conceptual ontologies was proposed in [13]. This language is based on the foundation ontology also proposed in [13], which uses various theories of Formal Ontology, Philosophical Logic, Philosophy of Language, Linguistics and Cognitive Psychology, and was developed with the intention of providing an ontological foundation for general conceptual modeling languages. An extension of this foundation ontology as a component of a larger ontology called UFO ( Unified Foundation Ontology ) was presented by [16,17]. Part of the UFO is described in Fig. 4. It is used in this work to ensure the generation of well-founded model.

Fig. 4. UFO fragment - categories Sortal Universal and Mixin Universal type Substantials . [13]

[FIGURE]

OntoUML is a language for representing ontologies proposed by [13]. It is an extension of the UML 2.0 metamodel in order to get a ontologically well-founded version. The fragment of ontology UFO shown in Fig. 4 was used to evaluate and design of the part that deals with UML classifiers for the purpose of conceptual modeling and representation of ontologies. The UML 2.0 metamodel resulting from this process is shown in Fig. 5.

Fig. 5. Fragment of the UML Metamodel 2.0 (type Class ) redesigned according to the UFO. [13]

[FIGURE]

UML has extension mechanisms that allow you to modify the elements of language such that a coherent set of such extensions is a UML profile. Hence, the OntoUML is a UML profile consists of a set of stereotypes that represent the ontological categories of the types of universal proposed in UFO-A, as well as restrictions that reflect the formal axiomatization of UFO in such a way that restricts the set of models OntoUML grammatically valid in those situations that represent admissible on the theory of UFO [18]. Thus, Fig. 5 shows that the element UML class is specialized according to the type UFO Monadic Universal .

## 4 IT Architecture Modeling

Before build a ITSC plan IT infrastructure should be reviewed to determine if it has all the components and technologies necessary to enable IT services to continue operating in case of an incident . If not, the systems must be updated to include ITSC components, such as resilience, high availability or redundant systems and data replication mechanisms [1].

The models in this section provide the IT architecture in this view. They are composed of a main model, the model of the IT architecture , and submodels generated from the principal. Because space limitations and seeking a better view, only the most representative submodels are described in this paper. Each model and submodels are described in detail in the text.

Figure 6 shows the organization IT architecture in relationship with an IT component as it should be built through the IT components. Each IT component should be replicated in order to remove any single point of failure (SFP). This replication takes place in order to achieve service continuity, which represents a whole whose parts are the IT service continuity components .

Fig. 6. IT Architecture Model

[FIGURE]

IT component and ITSC component are category type, for aggregate, each concepts with different principles of identity. The entity IT Architecture is a kind type and carries a criterion of identity that allows to distinguish individuals. Its relationship with the type IT component is based on a internal formal relationship , because there is a dependency between an existential IT component and IT architecture that composes. It only exists if there is this architecture and vice versa. Likewise, the relationship between Component CSTI and Service Continuity is also classified as internal formal relationship as the ITSC Component will exist if the IT Architecture , from the perspective of the service continuity exist. The relationship between Service Continuity and IT component only occurs because there is a relator called Replication making the material relation Removal of single point of failure exists.

## 4.1 IT Architecture Components

Figure 7 represents the entity specialization IT component (Fig. 6). Two of them are described in detail in the submodels of subsections 4.3 and 4.4, namely site submodel and platform submodel .

The IT component entity adds individuals with different principles of identity and rigid, so it is a category . The same occurs with the entity Platform . Site , System and Data Storage are entities that provide identity principle for their subjects and apply to their subjects while there. Thus, each of which is categorized as kind .

Fig. 7. IT architecture model fragment: IT component especialization

[FIGURE]

## 4.2 IT Service Continuity Components

Figure 8 represents the ITSC components and follows a similar reasoning to that described in subsection 4.1 of IT components. It presents a fragment of the model of the IT architecture identifies the components necessary to provide IT service continuity classified as UFO and more detailed in specific submodels.

According to the publication [1] systems of a corporation interested in producing a plan for IT service continuity must be updated to include ITSC components as: resilience , high availability or redundancy and data replication mechanisms . These standard recommendations are the basis of this submodel, but the ontological evaluation of the text pointed out some necessary modifications. Inclusion of a ITSC component, the Site Model submodel that is associated with the provision of IT infrastructure resilience. Replacement of the term data replication mechanisms per data replication. Creation of submodels Platform , System , Data Storage and Data Replication submodels to better define high availability term, but as IT components. Furthermore, the addition of Resilient Network submodel to network issues.

Figure 8 represents the ' ITSC Component entity and their specialization: Site Model , Resilient Network and Data Replication . Entities in Fig. 8 defined as kind represent rigid concepts and provide a principle of identity for its instances. They are grouped into a category because it is rigid concepts with different principles of identity. The Resilient Network entity also adds individuals with different principles of identity and rigid, so it is a category . Each subsection describes the respective model. The relevant details found in the construction of each model are also presented throughout the text.

## 4.3 Site Submodel

Figure 9 describes the Site submodel. Site is a type capable of providing the principle of identity to their bodies and applies to individuals as its there. Thus, as the UFO, is represented by a kind . A Site can be installed in a Location at the main building of the corporation. This case is represented by Local , also identified as Primary or Home . When the site installation occur in a distant Location of the main building, will be Remote or Secondary . These types are mutually exclusive, because a site is either installed locally or remotely. Thus, the relationship of these entities with the Location is disjoint, complete .

Fig. 8. Submodel of IT service continuity components

[FIGURE]

Fig. 9. Site Submodel

[FIGURE]

If a site is running, it is online. A site crashes in the event of a incident capable of Suspension of Operation generating. In this case, the alternate site to Offline . When the suspension of operation has been completed the site back up and running. Therefore, switches back to Online . The relationship between the entities Online and Offline only if there is an entity called Incident that results in an arrest operation. Therefore, this entity should be classified as relator . Relations with it are of the type material . The Online and Offline types represent their roles at different times. Thus, the relationship between these types and Site type is classified as disjoint, complete . A Online Site plays the role of Active . A Offline Site plays the role of Passive , Backup or Contingency . These roles are exercised through entities in the model Active , Passive , Backup and Contingency , the which occur one at a time and are specializations of the entity Site . In turn, they are subtypes of the entity Site and thus inherits the characteristics and it is classified as subkind .

## 4.4 Platform Submodel

Figure 10 describes the Platform submodel. Platform brings together Network Component , Cooling , Power , WarrantyandSupport , ComputerSystem and Monitoring types. All these types are classified as kind for providing the principle of identity to their bodies and be applicable to individuals as its there.

The Network Component kind specializes in Network Provider , Physical Media , Link e Telecom Asset , classified as subkinds . Power kind consists of the subkinds : Power Distributor , Bank of Battery and Generator , which are exclusive. Each of these entities is related to the UPS kind . However, these relationships depend on relators to exist. They are: Automatic Switching , UPS / Battery Switching and UPS / Generator Switching , respectively associated with the pairs of entities: Power Distributor-UPS , Bank of Battery-UPS and Generator-UPS . The Computer System type is composed of subkinds Peripheral , Dual Network Device , Dual Power Inlet , Redundant Power Supply and Cooling Fan , also exclusive. This type maintains relationship with both Warranty and Support through the Appropriate Level of Warranty relator , and with Monitoring type through Warning relator . But the kind Monitoring specializes in two subkinds that complement, Management Suite and Monitoring Software .

Fig. 10. Platform Submodel

[FIGURE]

## 4.5 Data Replication Submodel

Figure 11 describes the Data Replication submodel, which is a specialization of IT Service Continuity submodel shown in Fig. 8. This submodel presents a whole-part relation between the whole Data Replicaton and the part Replication Technology . This relation is classified as essential,inseparable because there is only compounding the whole and only exists if all made by the part. There are also specialization relations. Data replication is composed of types Local Replication and Remote Replication and Media Backup / Restore , DBMS-based , application-based , Host-based and Storage-based , all classified as subkinds . Replication technology adds some individuals with different identity principle and rigid, they are: Mirroring , Snapshot , Cluster , Appliance and RAID .

Fig. 11. Data Resilience Submodel

[FIGURE]

## 5 Ontological Evaluation of the PAS 77 Specification

## 5.1 Incompleteness of the Concept IT Component

According to [1], before building a ITSC plan, IT infrastructure should be reviewed to determine whether all components and technologies required to enable IT services continue in case of an incident. Otherwise, the systems must be updated to include ITSC components as resilience, high availability and redundancy of systems and mechanisms for data replication.

This section allows the understanding that IT components must meet the minimum requirements to ensure service continuity in case of an incident. It also allows us to understand that once IT components meet the requirements, then the components of ITSC can be implemented.

It happens that the IT components are not clearly defined in the standard, allowing multiple interpretations. This characterizes a problem of incompleteness, since the specification does not present the builders needed to fully understand the concepts. Thus, it was necessary to identify them from the concepts of ITSC components to allow the construction of Site, Platform, System and Data Storage submodels, represented in Fig. 7, that solve the problem.

## 5.2 Unclear on the Concept of Site

It was not possible to clearly identify the text of the standard concept of the site and characterize the differences between a site and a site model. The absence of a site concept expressed in the specification generates a problem of incompleteness, which can lead to misinterpretation of the site model is an IT component. This problem was solved with the construction of a site submodel, as shown in Fig. 9 to deal with the concepts associated with the Site (IT component) with greater expressiveness and construction of the Site Model submodel for the concepts related to IT service continuity.

## 5.3 Ambiguity in the Concept of High Availability

The specification [1] lies in the problem of overload constructors when they have a single definition for high availability concepts and availability. The standard high availability conceptualized as 'High availability refers to the ability of a computer system and its hosted resources to withstand failures', however following the text, the PAS no longer uses the high availability term, but the availability term. However, these are distinct concepts, which characterizes the overload constructors. The ontology generated solves this problem by construction of submodels: Platform , System , Data Storage and Data Rep?ication .

## 5.4 Ambiguity in the Concept of System

There is another problem as to overload constructors. This time, the concept of system used in Appendix E of the specification is hardware related and not the system (IT system) found in the remaining text. However, the document does not distinguish between such concepts. To solve this problem, the ontology uses Computer System term when associated with the hardware. This solution can be found in Platform submodel in Fig. 10.

## 5.5 Ambiguity in the Concept of Resilience

The resilience and replication terms are also not explicitly defined in the standard. The standard has an annex to address the types of resilience, but describes the data replication. It features a confusion of concepts. Thus, it is necessary to differentiate these concepts to ensure greater clarity to the model. To do this, Data Replication is built.

The text also describes resilience to system, application and network. However these concepts are treated in submodels specializing IT Component : System submodel for concepts related to system and application resilience and Resilient Network submodel, specialization of ITSC Component to the concept of network resilience.

## 6 Conclusion

This paper presents an ontology model for the IT architecture of data centers and an ontological evaluation of the PAS 77 specification used as a reference for building the model. The conceptual model produced is called well-founded because it was built from a foundation ontology using a specific language for this purpose. Therefore, this model eliminates the different interpretations generated when reading a text in natural language, allowing a greater clarity of the concepts expressed in the standard.

The application of this model in assessing the ontological point of view of the IT architecture described in PAS 77 allowed the identification of deficiencies in some concepts such as incompleteness, lack of clarity and ambiguity of concepts. This confirms the importance of well-founded conceptual models both in the construction of a formal conceptualization of a domain and in the identification of conceptual problems in texts written in natural language. Thus, it is expected that corporations whose IT architecture follows the ontological model built are more robust in terms of continuity of services, which minimize the downtime of IT services.

Acknowledgements. The authors would like to thank the Federal Court of Ceara by sponsorship and Professional Masters in Applied Computing for their support of this article. The first author has been sponsored by the Federal Court of Ceara since 2009.

## References

1. PAS 77: It service continuity management code of practice. B S I Standards, London (2006)
2. ISO/IEC 24762: Information technology - Security techniques - Guidelines for information and communications technology disaster recovery services. ISO, Geneva (2009)
3. Rath, A.S., Devaurs, D., Lindstaedt, S.N.: An Ontology-Based Approach for Detecting Knowledge Intensive Tasks. Journal of Digital Information Management 9, 9-18 (2011)
4. Baioco, G.C.: It service management and governance modeling an itsm configuration process: A foundational ontology approach. In: 4th IFIP/IEEE International Workshop on Business-driven IT Management, Long Island (2009)
5. Baioco, G., Garcia, A.S.: Implementation and application of a well-founded configuration management ontology. In: IEEE/IFIP Network Operations and Management Symposium Workshops, Osaka (2010)
6. Costa, A.C.M.: ITIL Service Level Management Process Domain Modeling: a Approach Using Ontology and Platform Infraware Application. Master's thesis, UFES (2007) (in Portuguese)
7. Monteiro, M.E., Garcia, A.S., Paulo, P., Barcelos, F., Guizzardi, G.: Ontology based model for the itu-t recommendation g.805: Towards the self- management of transport networks. International Journal of Computer Science &amp; Information Technology (2010)

8. Barcelos, P.P.F.: Architectural Analysis, Ontological and Proposal for a Reference Model for the ITU-T Recommendation G.805. Master's thesis, UFES (2011) (in Portuguese)
9. Barcelos, P., Guizzardi, G., Monteiro, M.E., Garcia, A.S.: Ontological Evaluation of the ITU-T Recommendation G.805, pp. 261-266. IEEE Press (2011)
10. Bartsch, C., Shwartz, L., Ward, C., Grabarnik, G., Buco, M.J.: Decomposition of it service processes and alternative service identification using ontologies, pp. 714-717. IEEE Press (2008)
11. Goluch, G., Ekelhart, A., Jakoubi, S., Tjoa, S., M¨ uck, T.: Integration of an ontological information security concept in risk-aware business process management (2008)
12. Barcelos, P., Monteiro, M.E., Sim´ oes, R., Garcia, A.S., Segatto, M.E.V.: OOTN an ontology proposal for optical transport networks, pp. 1-7. IEEE Press (2010)
13. Guizzardi, G.: Ontological foundations for structural conceptual models. Ph.D. thesis, University of Twente (2005)
14. Fettke, P., Loobs, P.: Ontological Analysis of Reference Models. In: Business Systems Analysis with Ontologies, pp. 56-81. Idea Group Publishing, Hershey (2005)
15. Taylor, S., Lloyd, V., Rudd, C.: Service design. ITIL Series, TSO (2007)
16. Guizzardi, G., Wagner, G.: Some Applications of a Unified Foundational Ontology in Business Modeling. In: Rosemann, M., Green, P. (eds.) Ontologies and Business Systems Analysis. IDEA Publisher (2005)
17. Guizzardi, G., Wagner, G.: Towards Ontological Foundations for Agent Modelling Concepts Using the Unified Fundational Ontology (UFO). In: Bresciani, P., Giorgini, P., Henderson-Sellers, B., Low, G., Winikoff, M. (eds.) AOIS 2004. LNCS (LNAI), vol. 3508, pp. 110-124. Springer, Heidelberg (2005)
18. Guizzardi, G.: On ontology, ontologies, conceptualizations, modeling languages, and (meta)models. In: Vasilecas, O., Eder, J., Caplinskas, A. (eds.) Dbis. Frontiers in Artificial Intelligence and Applications, vol. 155, pp. 18-39. IOS Press (2006)
