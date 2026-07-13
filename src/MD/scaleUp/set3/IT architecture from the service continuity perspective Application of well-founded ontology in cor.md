## IT architecture from the service continuity perspective: application of well-founded ontology in corporate environments

Hedwio Carvalho e Silva 1,2 , Rita de Cassia C. de Castro 1,2 , Marcos Jose Negreiros Gomes 1 , Anilton Salles Garcia 3

1 Professional Masters in Applied Computing, State University of Ceara, Fortaleza, Ceara, Brazil

3 LabTel - Telecommunications Research Laboratory, Electrical Engineering Department,

2 Telematics Department, Federal Institute of Education, Science and Technology of Ceara, Fortaleza, Ceara, Brazil

Federal University of Espirito Santo, Vitoria, ES, Brazil

hedwio,rita@ifce.edu.br

negreiro@graphvs.com.br

anilton@inf.ufes.br

## ABSTRACT:

This paper presents an application of data center IT architecture ontology model for corporate environments. The article is based PAS77 in order to get a service continuity view and uses Unified Foundation Ontology (UFO) to produce a well-founded ontology. It is built using the Conceptual Model Language OntoUML with the objective of preserving the ontologic prerogatives defined in the UFO. This model was applied to enterprise data center environments, being able to identify IT components and verify the adherence of these components describing the PAS77.

Keywords: Applied Ontology, Conceptual Modeling, IT Architecture, IT Service Continuity

c © 2012 DLINE. All rights reserved.

## 1 Introduction

Are significant investments to provide a data center infrastructure can adequately support the company's business. Part of these investments is associated with IT architecture. Another part refers to the infrastructure necessary to maintain the IT architecture in place as air conditioning, electrical, controls temperature and humidity, among others.

Acorporation that needs to operate 24x7, it is a cloud services provider, a service provider or an enterprise data center to keep the data center at its facilities, should be aligned with the norms and standards relating to such facilities. Even with all data center infrastructure built to meet the needs of the business and following the recommendations, corporations are subject to disasters that may directly affect the operation of the data center. Examples are catastrophic events like Hurricane Katrina in 2005, which devastated the region of New Orleans in the U.S., the terrorist attack on the twin towers in 2001 also in the U.S. and the tsunami in Japan in 2011. These cases demonstrate the need for an environmental contingency that can operate in the event of unavailability of the core infrastructure.

Thus, concern about the IT service continuity emerges as strategic for companies that seek to minimize the downtime of services in case of failure. Among the existing standards with a focus on service continuity management stand out [16] and [18]. The ISO/IEC 24762 (2009) presents guidelines for service recovery after a disaster in information and communication technology (ICT). It covers installation and service capabilities and offers alternative support and recovery for ICT systems in an organization. Includes aspects of implementation, testing and implementation of disaster recovery, but does not address other aspects of business continuity management. This standard also does not provide guidance on the IT architecture needed for the recovery of ICT services after a disaster. [18] was selected as the base document for the construction of this model, not only by considering issues of continuity management of IT services, but, fundamentally, to emphasize and describe characteristics of the IT architecture to be followed by organizations concerned with continuity of information technology services.

Several studies involving ontologies has been published today. Many of them have specific domain ontologies of knowledge, known as domain ontologies. These ontologies have been studied in several areas: electrocardiography

Copyright c © 2012 Permission to copy without fee all or part of the material printed in JISR is granted provided that the copies are not made or distributed for commercial advantage.

Figure 1. Ullmann's triangle. [10]

[FIGURE]

[9, 8], oil exploration and production [12] and telecommunications [3]. Work in the area of domain ontologies for IT service continuity management and standards deserve special attention.

The production of ontology models in order to provide a formal specification of ITIL processes has been the focus of work. In [1] presents a conceptual framework in the field of configuration management in the context of service management and IT governance, based on foundation ontology. After that, [2] extends the model presented in [1] showing how these modeled concepts by ontologies can be implemented and applied in computer systems. [6] also presents a conceptual model using foundation ontology, but on the ITIL process service level management process. To achieve this, we used the unified foundation ontology (UFO) to build the conceptual model.

Ontology based on standards and/or recommendations is another area with interesting work. [1] and [6] propose conceptual models of ITIL library domain. While [1] model the domain of configuration management, [6] addresses the domain of the service level. [4] show the most relevant questions found during the implementation process of ontologies to transports optical networks using a direct implementation in Web Ontology Language (OWL). A initial version of the conceptual model to the ITU-T G.805 recommendation is presented in [17]. In [5] is presented a reference model on ontology developed to the ITU-T G.805 recommendation, including the conceptual model and its derivations and restrictions rules. At last, in [3] an ontological evaluation of the referred recommendation is done. Some new works present itself as an extension of previous works. [6] extended a work regard a management module starting to follow recommendations. And [5] included a conceptual model, besides other improvements to the ontology built by [4].

The existing IT architecture present nowadays in the corporations suffer a great dependency of the IT equipments manufacturers' orientations and the suppliers of data center solution. The ontological model build present itself as a strong ally of the corporations, once it minimizes this dependency. Thus, this paper presents a solution to the IT architecture's interoperability problem of the data center through the conceptual model produced using the foundation ontology UFO through the representation language of ontologies OntoUML.

## 2 Theoretical Fundaments

## 2.1 Conceptual Modeling

The first step in conceptual modeling is the acquisition of the concepts and symbols related to a certain Universe of Discourse from documents and/or statements written or uttered in a Natural Language. As so, in this first step the modeler must focus in the identification of the signs used in that context and the understanding of their relations to the concepts and the reality they abstract, a semantic-oriented activity. These activities allow the understanding of the elements present in the Ullmann's triangle, represented in Figure 1. In [20], Ullmann presents three elements of meaning: a symbol or sign represents a concept and refers to a thing in the real world, or the referent; the concept is an abstraction of the thing. The elements of meaning are commonly presented as the vertices of a triangle.

The process of conceptual modeling involves two main tasks: the first one comprises the acquisition of concepts related to the Universe of Discourse being modeled (aka conceptualization [10]), along with the identification of the natural language signs used to represent such concepts; and the second involves the representation of the acquired concepts according to the grammar of a Modeling Language. To develop a conceptual model, the modeler must identify conceptual elements present in the UoD descriptions, understand how they relate to each other and then represent both conceptual elements and their inter-relationships in a Modeling Language [7].

Figure 2. Fragment of the UML Metamodel 2.0 (type Class ) redesigned according to the UFO.[10]

[FIGURE]

Figure 3. UFO fragment - categories Sortal Universal and Mixin Universal type Substantials .[10]

[FIGURE]

To achieve the quality of the model produced, this paper uses a language for representing ontologies proposed by [10], named OntoUML. It is an extension of the UML 2.0 metamodel in order to get a ontologically well-founded version. The UML 2.0 metamodel resulting from this process is shown in Fig. 2. UML has extension mechanisms that allow you to modify the elements of language such that a coherent set of such extensions is a UML profile. Hence, the OntoUML is a UML profile consists of a set of stereotypes that represent the ontological categories of the types proposed in the Unified Foundation Ontology (UFO) [10]. Fig. 2 shows element UML class specialized according to the type UFO Monadic Universal .

This modeling language is based on the foundation ontology also proposed in [10], which uses various theories of Formal Ontology, Philosophical Logic, Philosophy of Language, Linguistics and Cognitive Psychology, and was developed with the intention of providing an ontological foundation for general conceptual modeling languages. An extension of this foundation ontology as a component of a larger ontology called UFO ( Unified Foundation Ontology ) was presented by [13, 14]. UFO is divided in three fragments named UFO-A (Ontology of Endurants), UFO-B (Ontology of Perdurants) e UFO-C (Ontology of Social and Intentional Entities). UFO-A, used in this paper, defines the core of this ontology, systematizing concepts, eg, types and taxonomic structure [15], part-whole relations [7-11] , relational properties [11]. Part of the UFO-A is described in Fig. 3.

This paper presents a conceptual model well based build using the foundation ontology UFO e through the representation language of ontologies OntoUML. An rundown of this characteristics can be found in Table 1.

The approach utilized is based on [10] when defends a language's conceptual model to represent a collection of real world's phenomenons in a determined domain Universe of Discourse can be systematically assessed, comparing the homomorphism level between a concrete representation ( specification ) of the view of the underlying world to the language with a explicit and formal representation of a concretion of this domain, called reference ontology . The Figure 4 represents the proposition of [10] contextualized this paper's scope. The Universe of Discourse in question is the IT architecture . The concrete representation used is the PAS 77 specification and the explicit representation and formal conceptual of this domain is the IT architecture ontology under the view of service continuity .

Figure 4. Approach to model building and evaluation ontological

| Characteristics                      | Proposed model   |
|--------------------------------------|------------------|
| Modeling Type                        | Conceptual Model |
| Utilizes norms and/or documentations | PAS 77:2006      |
| Foundation Ontology                  | UFO              |
| Representation Language              | OntoUML          |
| Domain                               | IT Architecture  |

Table 1. Characteristics of the Ontology model of the IT Architecture.

[FIGURE]

## 3 IT Architecture Model

Before build a ITSC plan IT infrastructure should be reviewed to determine if it has all the components and technologies necessary to enable IT services to continue operating in case of an incident . If not, the systems must be updated to include ITSC components, such as resilience, high availability or redundant systems and data replication mechanisms [18].

The models in this section provide the IT architecture in this view. They are composed of a main model, the model of the IT architecture , and submodels generated from the principal. Because space limitations and seeking a better view, only the most representative submodels are described in this paper. Each model and submodels are described in detail in the text.

Figure 5 shows the organization IT architecture in relationship with an IT component as it should be built through the IT components. Each IT component should be replicated in order to remove any single point of failure (SFP). This replication takes place in order to achieve service continuity, which represents a whole whose parts are the IT service continuity components .

IT component and ITSC component are category type, for aggregate, each concepts with different principles of identity. The entity IT Architecture is a kind type and carries a criterion of identity that allows to distinguish individuals. Its relationship with the type IT component is based on a internal formal relationship , because there is a dependency between an existential IT component and IT architecture that composes. It only exists if there is this architecture and vice versa. Likewise, the relationship between Component CSTI and Service Continuity is also classified as internal formal relationship as the ITSC Component will exist if the IT Architecture , from the perspective of the service continuity exist. The relationship between Service Continuity and IT component only occurs because there is a relator called Replication making the material relation Removal of single point of failure exists.

Figure 5. IT Architecture Model

[FIGURE]

Figure 6. IT architecture model fragment: IT component especialization

## 3.1 IT Architecture Components

Figure 6 represents the entity specialization IT component (Fig. 5). Two of them are described in detail in the submodels of subsections 3.3 and 3.4, namely site submodel and platform submodel .

The IT component entity adds individuals with different principles of identity and rigid, so it is a category . The same occurs with the entity Platform . Site , System and Data Storage are entities that provide identity principle for their subjects and apply to their subjects while there. Thus, each of which is categorized as kind .

## 3.2 IT Service Continuity Components

Figure 7 represents the ITSC components and follows a similar reasoning to that described in subsection 3.1 of IT components. It presents a fragment of the model of the IT architecture identifies the components necessary to provide IT service continuity classified as UFO and more detailed in specific submodels.

According to the publication [18] systems of a corporation interested in producing a plan for IT service continuity must be updated to include ITSC components as: resilience , high availability or redundancy and data replication mechanisms . These standard recommendations are the basis of this submodel, but the ontological evaluation of the text pointed out some necessary modifications. Inclusion of a ITSC component, the Site Model submodel that is associated with the provision of IT infrastructure resilience. Replacement of the term data replication mechanisms per data replication. Creation of submodels Platform , System , Data Storage and Data Replication submodels to better define high availability term, but as IT components. Furthermore, the addition of Resilient Network submodel to network issues.

Figure 7 represents the " ITSC Component entity and their specialization: Site Model , Resilient Network and Data Replication . Entities in Fig. 7 defined as kind represent rigid concepts and provide a principle of identity for its instances. They are grouped into a category because it is rigid concepts with different principles of identity. The Resilient Network entity also adds individuals with different principles of identity and rigid, so it is a category . Each subsection describes the respective model. The relevant details found in the construction of each model are also presented throughout the text.

Figure 7. Submodel of IT service continuity components

[FIGURE]

Figure 8. Site Submodel

[FIGURE]

## 3.3 Site Submodel

Figure 8 describes the Site submodel. Site is a type capable of providing the principle of identity to their bodies and applies to individuals as its there. Thus, as the UFO, is represented by a kind . A Site can be installed in a Location at the main building of the corporation. This case is represented by Local , also identified as Primary or Home . When the site installation occur in a distant Location of the main building, will be Remote or Secondary . These types are mutually exclusive, because a site is either installed locally or remotely. Thus, the relationship of these entities with the Location is disjoint, complete .

If a site is running, it is online. A site crashes in the event of a incident capable of Suspension of Operation generating. In this case, the alternate site to Offline . When the suspension of operation has been completed the site back up and running. Therefore, switches back to Online . The relationship between the entities Online and Offline only if there is an entity called Incident that results in an arrest operation. Therefore, this entity should be classified as relator . Relations with it are of the type material . The Online and Offline types represent their roles at different times. Thus, the relationship between these types and Site type is classified as disjoint, complete . A Online Site plays the role of Active . A Offline Site plays the role of Passive , Backup or Contingency . These roles are exercised through entities in the model Active , Passive , Backup and Contingency , the which occur one at a time and are specializations of the entity Site . In turn, they are subtypes of the entity Site and thus inherits the characteristics and it is classified as subkind .

## 3.4 Platform Submodel

Figure 9 describes the Platform submodel. Platform brings together Network Component , Cooling , Power , Warranty and Support , Computer System and Monitoring types. All these types are classified as kind for providing the principle of identity to their bodies and be applicable to individuals as its there.

Figure 9. Platform Submodel

[FIGURE]

The Network Component kind specializes in Network Provider , Physical Media , Link e Telecom Asset , classified as subkinds . Power kind consists of the subkinds : Power Distributor , Bank of Battery and Generator , which are exclusive. Each of these entities is related to the UPS kind . However, these relationships depend on relators to exist. They are: Automatic Switching , UPS / Battery Switching and UPS / Generator Switching , respectively associated with the pairs of entities: Power Distributor-UPS , Bank of Battery-UPS and Generator-UPS . The Computer System type is composed of subkinds Peripheral , Dual Network Device , Dual Power Inlet , Redundant Power Supply and Cooling Fan , also exclusive. This type maintains relationship with both Warranty and Support through the Appropriate Level of Warranty relator , and with Monitoring type through Warning relator . But the kind Monitoring specializes in two subkinds that complement, Management Suite and Monitoring Software .

## 3.5 Data Replication Submodel

Figure 10 describes the Data Replication submodel, which is a specialization of IT Service Continuity submodel shown in Fig. 7. This submodel presents a whole-part relation between the whole Data Replicaton and the part Replication Technology . This relation is classified as essential,inseparable because there is only compounding the whole and only exists if all made by the part. There are also specialization relations. Data replication is composed of types Local Replication and Remote Replication and Media Backup / Restore , DBMS-based , application-based , Host-based and Storage-based , all classified as subkinds . Replication technology adds some individuals with different identity principle and rigid, they are: Mirroring , Snapshot , Cluster , Appliance and RAID .

## 4 Applied model to enterprise environments

## 4.1 Characterized case study

This paper presents a case study of a large corporate environment. This company operates 24/7 due to critical systems and presents characteristics of good governance and IT security concerns of the information stored there. However, such considerations are superficial and based on the observer's interpretation, which adds no value to the results. This study measures the alignment of the IT architecture of the corporation to good management practices of IT service continuity through the identification of IT components of this architecture from the service continuity perspective. The use of IT Architecture ontology model proposed by [19] meets the objectives of this study since the model uses IT Architecture described in PAS 77 as the Universe of Discourse. Therefore, the object of study is conceptualized based on a code of practice for IT service continuity.

Figure 10. Data Resilience Submodel

[FIGURE]

Figure 11. Specialization in several layers

[FIGURE]

The case study was applied to Site and Platform submodels. The latter applied the Network , Power , Computer System , Monitoring and Data Storage entities. Thus, it is possible to map in detail these IT architecture components. This mapping of the leaf entities allows an alignment with the definitions outlined in the upper nodes of the tree. Thus, the restrictions imposed by the hierarchy tree are met, as shown by the relations of specialization. Figure 11 shows the hierarchical relationship seen in the vertical view of the model. Initially identifies the type Redundant Power Supply , a specialized type Computer System . This specialized type Platform , which specializes a IT component . This detailed mapping of entities compose the first phase of the case study that aims to identify the IT Architecture components described in PAS 77. The second phase of the case study represents the results analysis of the components mapping from the ontology model perspective. This phase allows the deficiencies identification in architecture elements.

## 4.2 Identification of IT arquitecture components

The submodel Site presents the details of concepts and relations for the site where the data center is hosted. To perform the mapping is necessary to answer some questions::

- How many sites are installed in the corporation?
- About the location of sites, there is the remote site?
- When the suspension of operation due to an incident, what kind of offline site corporation uses?

These questions meet certain requirements of the Site submodel. The simplest case occurs if the corporation has a single site, which will be the main site. The existence of a second site requires information about the site location. Moreover, it is necessary to identify how a site classified as remote operates. If your operation is based on the concept of active, passive, backup or contingency site. The case study is applied to the platform submodel for the following components: Network , Power , Warranty and Support , Computer System and Monitoring . Network and Computer System components are presented in more detail because the amount of assets associated with these components in the data center.

- How many power distributors operating in the corporation?
- There are battery bank?
- There are generators?
- About UPS, it is classified as Standby or Online?
- The UPS performs automatic switching in case of power failure of the distributor?
- The UPS performs switching UPS / Generator in case of long power interruption?
- The UPS performs switching UPS / Battery in case of short power interruption?

The relationship between the elements of Power is extremely important for service continuity once the power distributor, the battery bank and generator must operate according to rules established and the failure of one can result in downtime if an incident occurs. As the concept of Computer System component is associated with equipment, having no relation to the software system, issues related to physical components must be answered:

- About the computer systems have dual network device?
- About the computer systems have redundant cooler?
- About the computer systems have redundant power?
- About the computer systems have dual power?

The identification of each component classified as Computer System allows the identification of failure points in the existing architecture, and designed to prevent such a failure when purchasing new computer systems. Network components are part of the whole called Computer System, so they should answer the same questions apply to Computer System. However, the peculiarities of network should also be considered and answered:

- The connections between network component occur within the site or off site?
- The off-site connections between network components occur via the Internet or via connection between sites?

Furthermore, links and providers are entities important for ensuring continuity of data center operations. So there are questions for these entities:

- Sort the links in the network operation: dedicated link, data link and high-speed link?
- How connectivity providers exist in the corporation?
- About provider connectivity, is own or rented?
- About connectivity provider, classify it as Private Network Provider and/or Internet Service Provider?
- About connectivity provider, classify it as a backbone provider and/or provider of last mile?

Issues relating to Network show situations in which the corporation can operate with appropriate links: data links, dedicated links e high speed links. Thus, the corporation can use different operators for the last mile and backbone. In addition, you can also use different operators for private network and Internet. The provision of connectivity can be performed by the corporation itself or by contracting the service.

About Warranty and Support, Monitoring and Data Storage The following questions need answers:

- About guarantee and support for maintenance and troubleshooting, computer systems have at least one contract with the appropriate level of assurance?
- About platform monitoring, which of the following monitoring tools are in the corporation? Software for monitoring, management suite, or both?
- About data storage, as is done in your corporation? Isolated or shared?
- About data storage, identify the type used: on disk, array or alternative media?
- About storage technology, which exist in the enterprise: DAS, NAS or SAN?

Figure 12. Questions

[FIGURE]

The lack of a guarantee to meet the appropriate level of security can affect the availability of IT services. Likewise, the lack of monitoring tool can affect the response time to incidents. The characteristics of data storage are revelantes when storage is performed only on a shared or uses a single storage technology.

## 5 Results Analysis

The results of IT Architecture ontology model applying were obtained through several questions with a focus on each component of IT architecture studied. So a lot of questions were answered, which allows the analysis in this section. Figure 12 shows the percentage of questions and answered questions. This is the gathering of data in the following categories: Site , Network , Power , Computer System , Monitoring and Data Storage . However, even with 83.62% of questions answered, any lack of information may generate a serious impact on the environment. In the specific case of Figure 12, though accounting for only 5.8% unanswered questions have serious impact on the IT architecture since they involve the dual power of computer systems and the type of offline site. Sections 5.1, 5.2, 5.3, 5.4 and 5.5 analyze the answers to these questions in detail.

## 5.1 Site

The existence of a single site is a serious deficiency of the IT architecture, as in the case of a disaster, the entire operation is impaired. The mapping of this item is very important for service continuity, because even with a second site still requires mapping a set of relevant items as: the location of the remote site and the role played by this remote site when it comes into operation.

## 5.2 Computer System

In the data center studied, 56 computer systems were identified, 15 of them related to network components. Of all computer systems, 19.64% do not have redundant power and 10.71% do not have dual network. These numbers are more significant when evaluating the results of the network components: 60 % do not have redundant power and 20% do not have dual network, as illustrated in Figure 13.

## 5.3 Network

The network components that are part of a computer system, were recorded in the previous section. However, these network elements need to be accounted for considering items associated with the existing network connections within a site and the connections that go beyond the site. In this context, 25% of the components of network connections within the site and only 0% of the components of network connections within and outside the site are redundant, as Figure 14. Although it was identified that 55.55% of the communication links are redundant, and 100% dedicated and high speed.

However, by dividing the connectivity providers in ISP and Private Provider Network, it was found that each provides both a backbone and last mile. Furthermore, it was identified that 100% of links are hired by third parties.

Figure 13. Computer System and Network Components

[FIGURE]

Figure 14. Network Details

[FIGURE]

## 5.4 Power

The corporation uses UPS online to guarantee operation. It has a battery bank and generator. It can perform automatic switching in case of distributor power failure. It is also capable of switching in the case of a power short interruption. However, it is capable of automatic switching in the event of power long interruption, which seriously compromises the entire infrastructure since no remote site.

## 5.5 Monitoring, Warranty and Support and Data Storage

The Corporation monitors the entire platform through its monitoring software, being reported by the alert when a fault occurs. Computer systems have appropriate warranty and support contract. The data storage is shared and stored in disks. SAN (Storage Area Network) is the storage technology.

## 6 Conclusion

This paper presents an ontology model for the IT architecture of data centers using PAS 77 specification as a reference for building the model. The conceptual model produced is called well-founded because it was built from a foundation ontology using a specific language for this purpose. Therefore, this model eliminates the different interpretations generated when reading a text in natural language, allowing a greater clarity, beyond the elimination of incompleteness and ambiguity of concepts expressed in the standard.

Greater expressiveness shown in the model confirms the importance of well-founded conceptual models in the construction of a formal conceptualization of a domain, especially when the universe of discourse is described in natural language. This increased expression allowed the application of well-founded IT architecture model in data center environment for a large corporation with very good results. After all, the study case was able to identify each component of IT, verify their adherence to the model and, therefore, point out items that need improvement to provide resilience and ensure IT service continuity.

Thus, it is expected that corporations whose IT architecture follows the ontological model built are more robust in terms of continuity of services, which minimize the downtime of IT services.

## References

- [1] A. C. M.; CALVI C. Z.; GARCIA A. S. BAIÔCO, G.; COSTA. It service management and governance modeling an itsm configuration process: A foundational ontology approach. 4th IFIP/IEEE International Workshop on Business-driven IT Management (BDIM 2009), 2009, Long Island. Proceeding of the 2009 IFIP/IEEE International Symposium on Integrated Network Management Workshops , -1, 2009. to appear.
- [2] A. S. BAIÔCO, G.; GARCIA. Implementation and application of a well-founded configuration management ontology. IEEE/IFIP Network Operations and Management Symposium Workshops , -1, 2010. to appear.
- [3] Pedro Barcelos, Giancarlo Guizzardi, Maxwell E. Monteiro, and Anilton S. Garcia. Ontological Evaluation of the ITU-T Recommendation G.805. pages 261-266. IEEE, 2011.
- [4] Pedro Barcelos, Maxwell E. Monteiro, Ricardo Simões, Anilton S. Garcia, and Marcelo Eduardo Vieira Segatto. OOTN - an ontology proposal for optical transport networks. pages 1-7. IEEE, 2010.
- [5] Pedro Paulo Favato Barcelos. Arquitetural, Ontological Analysis and Reference Model Proposal for ITU-T G.805 Standard. In Portuguese. Master's thesis, UFES, 2011.
- [6] André Cypriano Monteiro Costa. Domain Modeling of Level of Service Management Standard ITIL: A Approach Using Foundation Ontologies and Its Application in Infraware Platform. Master's thesis, UFES, 2007.
- [7] A. Gangopadhyay. Conceptual Modeling from Natural Language Functional Specifications. In Artificial Intelligence in Engineering , volume 15, pages 207-218, 2001.
- [8] B. N. Gonçalves, V. Zamborlini, and G. Guizzardi. An Ontological Analysis of the Electrocardiogram. In Electronic Journal of Communication, Information and Innovation in Health , 2009.
- [9] B.N. Gonçalves, G. Guizzardi, and J.G. Pereira Filho. Using an ECG reference ontology for semantic interoperability of ECG data. In Werner Ceusters and Richard H. Barry Smith and Scheuermann, editors, Journal of Biomedical Informatics, Special Issue on Ontologies for Clinical and Translational Research . Elsevier, 2011.

- [10] G. Guizzardi. Ontological foundations for structural conceptual models . PhD thesis, 2005.
- [11] G. Guizzardi. Whats in a Relationship: An Ontological Analysis. Proceedings of the 25th Int.l Conf. on Conceptual Modeling (ER 2008), Barcelona, Espanha, LNCS 5231 , pages 83-97, 2008.
- [12] G. Guizzardi, M. Lopes, F. Baião, and I Falbo, R. On the importance of truly ontological representation languages. nternational Journal of Information Systems Modeling and Design (IJISMD), IGI-Global , 2010.
- [13] G. Guizzardi and G. Wagner. Some Applications of a Unified Foundational Ontology in Business Modeling. In Michael Rosemann and Peter Green (Eds.), editor, Ontologies and Business Systems Analysis . IDEA Publisher, 2005.
- [14] G. Guizzardi and G. Wagner. Towards Ontological Foundations for Agent Modeling Concepts using UFO. AgentOriented Information Systems (AOIS), selected revised papers of the Sixth International Bi-Conference Workshop on Agent-Oriented Information Systems. Lecture Notes on Artificial Intelligence (LNAI), 2005.
- [15] G. Guizzardi, G. Wagner, N. Guarino, and M. van Sinderen. An Ontologically Well-Founded Profile for UML Conceptual Models. 16th Intl. Conf. on Advances in Information Systems Engineering (CAiSE), LNCS 3084 , 2004.
- [16] ISO/IEC 24762. Information technology - Security techniques - Guidelines for information and communications technology disaster recovery services . ISO, Geneva, Switzerland, 2009.
- [17] Maxwell E. Monteiro, Anilton Salles Garcia, Pedro Paulo, F. Barcelos, and Giancarlo Guizzardi. Ontology based model for the itu-t recommendation g.805: Towards the self- management of transport networks. International Journal of Computer Science &amp; Information Technology (IJCSIT), 2010.
- [18] PAS 77. It service continuity management code of practice . B S I Standards, 2006.
- [19] Hedwio Carvalho Silva, Rita de Cassia Cordeiro Castro, Marcos Jose Negreiros Gomes, and Anilton Salles Garcia. Well-Founded IT Architecture Ontology: An Approach from a Service Continuity Perspective. In R. Benlamri, editor, Networked digital technologies, part ii: 4th international conference, ndt 2012, dubai, uae, april 24-26, 2012. proceedings , number pt. 2 in Communications in Computer and Information Science. Springer, 2012.
- [20] S. Ullmann. Semantics: An Introduction to the Science of Meaning. Calouste, Lisboa. In Portuguese , 1977.
