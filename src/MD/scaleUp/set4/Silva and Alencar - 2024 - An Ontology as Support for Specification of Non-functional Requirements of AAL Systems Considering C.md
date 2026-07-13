[FIGURE]

## An Ontology as Support for Specification of Non-functional Requirements of AAL Systems Considering Compliance Aspects

Timóteo G. Silva* and Fernanda Alencar

Federal University of Pernambuco (UFPE), linked to the Graduate Program in Electrical Engineering (PPGEE/UFPE), Electronics and Systems Department, Recife, 50.740-560, Brazil

*Corresponding author: timoteogomes@yahoo.com.br, timoteo.silva@ufpe.br

† We thank CAPES for providing the necessary resources for the elaboration of the work and the Postgraduate Program in Electrical Engineering (PPGEE/UFPE).

Ambient assisted living (AAL) is a technological approach that emerged to meet the demands of seniors and people with disabilities. Because they are considered complex and multidisciplinary systems, it is necessary to identify and define which elements need to compose these systems. These challenges and the need for assistance in specifying requirements have led the academic community to explore and establish new approaches for the development of AAL systems. For this, there is the integration of different areas of knowledge, such as ontology, requirements engineering and compliance. Therefore, this work presents a central ontology to support the specification of requirements in AAL systems, where the elements that are part of the type of system are integrated. With the use of this ontology, it was possible to develop a domain ontology for vertical elevation platforms, where a validation was carried out with the industry in relation to the elements that constitute it and, later, a scenario was built to verify the syntactic correction of ontology. With the use of ontology, it will be possible to standardize the understanding of the associated terms and, at the same time, verify the relationships between the elements and help the designer in the requirements specification stage.

Keywords:

compliance; non-functional requirements; ontology; AAL systems

## 1. INTRODUCTION

According to Cicirelli et al. [1], in the past decade, intelligent environments,or ambient assisted living (AAL),have found wide application in various contexts, such as home automation, education, rehabilitation and others, considering that the implementation of new technologies can improve the quality of everyday life, facilitate access to many functions remotely or enable the use of natural interfaces, such as gestures and voice, to control lighting, climate, entertainment systems and home appliances.

According to Vimarlund [2], the global market for AAL is currently expected to reach up to 13.74 billion dollars by 2027, influenced by the emergence of coronavirus disease 2019, increasing pressure from the need of providing virtual services, where AAL technologies are being considered a long-term solution to deliver healthcare during the current pandemic and in the future.

Therefore, as the population ages, new policies, systems and technologies are demanded to support healthy aging, where new technologies can be used to accompany the elderly to reduce daily physical assistance and to prolong their independent life [3]. However, there are several engineering challenges to be faced in the development of AAL systems. These systems require standardized interfaces, are also multidisciplinary, adaptable to context and self-integrating, and must be aligned with compliance requirements [4]. All of these factors, associated with the inadequacy of current engineering methods and research approaches, complicate the process of developing AAL systems

[5]. Furthermore, in recent years, the complexity and scale of compliance requirements have increased significantly due to globalization and the maturing of different fields and legal requirements, making it difficult to meet ethical, legal, social, medical and technical constraints, knowing that these must be brought together and consolidated into a requirements specification [4].

These challenges in developing AAL systems have led the academic community to explore and to establish original approaches to the development of these systems [1] and to integrate them into different areas of knowledge, where we can mention two of them: compliance and ontology.

In this context, we searched the literature for evidence on the use of ontologies for the development of AAL systems [6]. From the evidence gathered in the literature and through a survey carried out with experts, a model was built in the UML notation of a core ontology (Onto4CAAL) to support the specification of requirements for AAL systems [7],as well as a domain ontology for vertical lifting platform (Onto4Elev), both of which are presented in this work.

The work is structured as follows: Section 2 presents the concepts of AAL, Ontology, Compliance and Requirements Engineering for AAL Systems; in Section 3, the Onto4CAAL ontology proposal is presented; Section 4 shows the Onto4Elev domain ontology and its application in a simulation in a use case; in Section 5, a case study is presented; in Section 6, the verification of the

Original Article

|

ontology using the UFO pattern is presented; in Section 7, related works are presented; in Section 8, limitations and future work are listed; in Section 9, the conclusions are mentioned.

## 2. THEORETICAL REFERENCE

In this section, we present the basic knowledge used to understand the theme involved in this work.

## 2.1. AAL systems

The AAL is an approach, based on technological solutions, which emerged to positively influence the health and quality of life of people, especially the elderly ones [8].

Anambientassistedliving (AAL) is an integration of autonomous assistive technologies, solutions and services that can positively influence people's health and quality of life, especially the elderly ones.

Technologies for AAL can be provided in the form of smart homes, equipped with sensors to monitor the different conditions of the environment and their inhabitants, and actuators to effectively assist them in their daily activities [9]. In summary, AAL characterizes an automated environment in which users interact with physical objects.

Systems for AAL need to know data about the world around the users they monitor to perform actions and perceive the context and modules that make up the entire environment [10]. Given this perspective, what was pointed out by Nakagawa [11] back in early 2013, and ratified by Cicirelli [1], the premise that AAL systems have become an increasingly important multidisciplinary research topic for medical and technological research communities remains valid.

## 2.2. Ontology

In the mid-1990s, in the context of Information Science, ontology emerged [12], and the most accepted definition was the one developed by Gruber [13], who describes it as an explicit specification of a conceptualization. In computing, the ontology aims to facilitate the sharing and reuse of information [14], in addition to define a conceptual specification for 'the knowledge' of a given domain. Thus, Campos [15] considers that ontologies establish a common vocabulary for a community that needs to share information in each domain, so that definitions can be computationally interpretable and include representations of concepts and relationships.

It is also worth noting that ontologies are systems of organization and representation of knowledge of a given domain in the form of a relational, intentional network, where relationships overlap with possible 'state of affairs' [16]. That is why ontologies are commonlyusedtoformalize and to explicitly specify a domain of knowledge, as they improve the automation of the integration of heterogeneous data groups, providing a formal specification of the vocabulary of concepts and their relationships [17].

## 2.3. Compliance

Compliance comes from the English language. 'To Comply' means 'to fulfill,' 'satisfy,' 'to carry out' what has been imposed on it in terms of the duty to comply. To comply with the legislation and regulations applicable to the business, codes of ethics and policies of the institution, as well as enforcing internal and external regulations imposed on the institution's activities [18]. NBR ISO 19600 [19] conceptualizes compliance as a set of mechanisms that aims to meet standards, policies and guidelines of a business.

According to Zhong [20], the construction phase of a system is ruled by many regulations, and it is important to inspect the construction process according to the regulations (called compliance verification or inspection) to ensure quality. Numerous works have addressed compliance as an initial requirement of the system, taking the rights of the law as the objectives of the systems to be satisfied and, therefore, aligning requirements engineering with compliance techniques [21].

In recent years, the complexity and scale of compliance requirements have increased significantly due to globalization, as the requests of regulations, standards and frameworks increase in number and scope, as the maturing process of different fields and regulations also increases as the areas or domains they cover become more interconnected [4].

## 2.4. Requirements specification for AAL systems

The main objective of requirements specification is to obtain relevant information for the development of the system. For Abran [22], it is the first stage of understanding construction of the problem to be solved by the system, which is strictly marked by human action in the relationships established between the development team and the client. According to Carvalho [23], most of the problems encountered during the development of systems originate in the requirements specification stage, because if the interested parties do not always have the clarity of what they need, it is not simple for the requirements analyst to be able to define which aspects are relevant to stakeholders.

Over the past decade, several research papers have addressed the development of AAL systems and health systems. Such systems are considered sensitive and critical, and often obey specific constraints. Verification of their correctness requires the use, at least partially, of formal approaches [24]. According to Alosaimi [25], AAL systems are designed for customized, responsive and predictive requirements, demanding high functionality performance to ensure interoperability, accessibility, security and consistency. Also, according to Alosaimi [25], standardization, continuity and assistance to systems development have become an urgent need to meet the growing needs of sustainable systems.

Thus, it can be seen that approaches to build AAL systems that ensure requirements are met and verification tools that prove that system implementation meets the requirements are still in the design phase. There are few works in the literature on development methodologies that improve the reliability and correction of these systems, beyond focusing on the initial phase of construction. For example, Augusto [26] proposed the application of methods and verification tools that are used in other Computer Science fields to develop AAL systems. Erazo-Garzon [27] proposed a quality-in-use model for AAL systems focused on the following characteristics: effectiveness, efficiency, fulfillment, risk exemption and context coverage.

As a result, there is still, in fact, a lack of solutions capable of supporting designers in the initial stage of development of such systems. This is necessary to follow what it had already been said by Nehmer [28], where the author states that without an appropriate methodology for the specification and development of AAL systems, it will never be possible to build reliable life care systems [28].

Therefore, we have the ontology, which can be used to assist in specifying the requirements of AAL systems, as it presents a formality to represent the internal concepts of the domain and the relationships between them, as well as incorporating the regulatory aspects of these types of systems. The formal specification of the behavior of the system and the requirements (with the NFRs) that the system must meet improve the development process and allow for the verification of these systems [4].

Therefore, a core ontology (Onto4CAAL) was proposed to support the specification of requirements for AAL systems. The ontology will be presented in the next section.

## 3. ONTO4CAAL ONTOLOGY PROPOSAL

Onto4CAAL is a core ontology that comprises a formal definition of modules and requirements for AAL systems. It includes aspects of compliance, NFRs (quality, product and ethical requirements), devices, environments, stakeholders and types of systems, as well as the relationships among these elements, which can contribute to the specification process of this type of system. Towards ontology development, since there is no standardization of an ontology development process [29], there are, however, several ontology development methodologies provided in literature. For the development of Onto4CAAL, the Methontology methodology waschosen[30],as it is used and recommended by the Foundation for Intelligent Physical Agents (FIPA), in addition of being considered a mature methodology.

The steps suggested by Methontology, which were used in the development of Onto4CALL, are: specification, knowledge acquisition, conceptualization, formalization, integration, implementation, evaluation, documentation and maintenance.

For the Specification stage, which is a stage where natural language is used to provide information as the main objective of the ontology and its other purposes, 12 Competency Questions were elaborated. In the next step, which is Knowledge Acquisition, we used the articles found in the MSL [6] and a first survey conducted with experts from both the academic and industrial fields. For this step, the middle-out approach [31] was used, since it allows a balance in terms of the level of detail, allowing the identification of central concepts of the knowledge domains, and then these concepts were generalized and specialized to produce the ontology. For the Conceptualization stage, a glossary of terms was made, gathering useful and potentially usable domain knowledge and their respective meanings.

In the Formalization step, axiomatization was used, which is illustrated through UML notation, and formalized by axioms in descriptive logic (DL). Therefore, concepts are considered as UML classes, relationships are represented through inheritance and associations and instances are described through object diagrams. Next, the UML notation is presented (in point A) and, later, the formalization by axioms (in point B).

## 3.1. Onto4CAAL UML notation

The link (https://github.com/timoteogomes/Onto4CAAL.git) presents the modeling of all modules associated with AAL, Compliance and Non-Functional Requirements systems, where the suggestions proposed by the survey respondents were considered (the additions from the survey are highlighted within the boxes with dotted red borders). This modeling was performed using the principle of UFO (ontology of foundation) proposed by Guizzardi [32] and modeled by OntoUML [33], using a plugin of the Visual Paradigm tool.

Table 1. Aal systems axioms.

| Representation   | Axioms                                                                                                                                                                                                                                              |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T A              | AALSystems ≡ EmergencyTreatmentServices ⊔ ComfortServices ⊔ AutonomyEnhancementServices InternalAssistanceComfort ≡ ServicesFindingThings ⊔ InfotainmentServices ⊔ LogisticServices ⊔ PersonalMonitoringServices AALSystems ⊑ ∃ usedIn. Environment |

Table 2. Compliance axioms.

| Representation   | Axioms                                                                                                                                                                                |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T C              | Compliance ≡ Legislation ⊔ ExternalStandards ⊔ InternalStandardsPolicies InternalStandardsPolicies ⊑ ¬ Legislation Compliance ⊑ ∀ establishesNFRequire- ment.NonFunctionalRequirement |

Table 3. Requirement axioms.

| Representation   | Axioms                                                                                                                                                                                                                                                                                             |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T R              | Requirement ≡ NonFunctionalRequirement ⊔ FunctionalRequirement ProductQuality ≡ Security ⊔ FunctionalAptitude ⊔ Portability ⊔ EfficiencyPerformance ⊔ Usability ⊔ Adaptivity ⊔ Maintainability ⊔ Compatibility ⊔ Reliability ⊔ Traceability ⊔ PrivacyData Requirement ⊑ ∃ wasDefinedBy.Stakeholder |

## 3.2. Tables with axioms

Below there are some of the axioms (Onto4CAAL has 545 axioms) of the six modules into which Onto4CAAL were divided, that is: AAL Systems, Compliance, Requirement, Stakeholder, Environment and Device.

## 3.2.1. Axioms of ALL systems

Table 1 presents three of the axioms established for the AAL systems module and their relationships with the other Onto4CAAL modules. Among the axioms that are presented, we have both concept and relation axioms.

The axiom ' AALSystems ⊑∃ usedIn.Environment ', for example, is an existential relation axiom ( ∃ ), that represents instances of AAL system used in at least one Environment instance.

## 3.2.2. Compliance axioms

Table 2 presents three axioms established for the Compliance module and their relationships with the other modules of Onto4CAAL. The axiom ' InternalStandardsPolicies ⊑ ¬ Legislation ', for example, represents that Legislation instances are disjoint from Legislation instances.

## 3.2.3. Requirement axioms

Table 3 presents three axioms of those established for the Requirement module and their relationships with the other modules of Onto4CAAL. The axiom ' Requirement ≡ NonFunctionalRequirement ⊔ FunctionalRequirement ', for example, represents the set of Requirements formed by instances of the concepts NonFunctionalRequirement or FunctionalRequirement.

|

|

Table 4. Stakeholder's axioms.

| Representation   | Axioms                                                                                                              |
|------------------|---------------------------------------------------------------------------------------------------------------------|
| T S              | MemberTimeDev ⊑ People ⊓ Stakeholder ProfessionalHealth ⊑ People ⊓ Stakeholder Stakeholder ⊑ ∃ defines. Requirement |

Table 5. Environment axioms.

| Representation   | Axioms                                                                                                                     |
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| T E              | Hospital ⊑ Environment LongStayElderlyInstitution ≡ GeriatricHouse ⊔ MedicalHousing ⊔ Asylum Environment ⊑ ∃ has.AALSystem |

Table 6. Device axioms.

| Representation   | Axioms                                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T D              | Device ≡ Button ⊔ Display ⊔ Sensor ⊔ Valve ⊔ SignalDevices ⊔ WearableDevice ⊔ Smartphone ⊔ CommandByVoice ⊔ Camera ⊔ Switches ⊔ Actuator ⊔ Container ⊔ SoundBox WearableDevice ⊑ Device Device ⊑ ∃ isUsedBy.AALSystem |

## 3.2.4. Stakeholder axioms

Table 4 presents three axioms established for the Stakeholder module and its relations with the other modules of Onto4CAAL. The axiom ' Stakeholder ⊑ ∃ defines. Requirement ', for example, is an existential relation axiom ( ∃ ), where it represents that Stakeholder instances define at least one Requirement instance.

## 3.2.5. Axioms of environment

Table 5 presents (three axioms established for the Environment module and their relationships with the others Onto4CAAL modules. The axiom ' LongStayElderlyInstitution ≡ GeriatricHouse ⊔ MedicalHousing ⊔ Asylum ', for example, represents the set of Long Stay Elderly Institutions formed by instances of the concepts GeriatricHouse or MedicalHousing or Asylum.

## 3.2.6. Device axioms

Table 6 presents three axioms established for the Device module and their relationships with the other Onto4CAAL modules. The axiom ' WearableDevice ⊑ Device ', for example, represents that the set of WearableDevice instances belong to Device instances, since an inclusion property ( ⊑ ) is used.

## 3.3. Creation of the Onto4CAAL ontology in Protégé

Protégé is an open source application for creating and editing ontologies, offering a graphical interface and architecture for creating knowledge-based tools. The version used for this work was 5.5.0. Therefore, Onto4CAAL was built, where it is possible to see in Figure 1 that, in addition to the 545 axioms, there are also 189 classes, 33 object properties and 5 data properties.

In Figure 2, the image that represents the part of the relations in the form of expression is presented. In the case of the AALSystems class, it is shown that it has some device, has a requirement, is used in some environment and is influenced by compliance. In Figure 3, it is possible to notice the six modules defined for the composition of Onto4CAAL,highlighting the AALSystems module, which consists of the EmergencyTreatmentServices, ComfortServices and Autonomy EnhancementServices classes, in addition to the subclasses of each one of them.

Figure 1. Onto4CAAL ontology metrics in the Protegé tool.

Figure 2. AALSytems class relations.

[FIGURE]

It is still possible to see in the same figure the Requirement module, which is expanded and composed of the FunctionalRequirement and NonFunctionalRequirement classes. Within this module, there are the EthicalRequirement and RequirementQuality classes. This class is where the ProductQuality and QualityUse subclasses are housed.

## 4. DOMAIN ONTOLOGY (ONTO4ELEV)

One of the characteristics of central ontologies is the possibility of their reuse to create domain ontologies. Considering that AAL systems have several classifications and subtypes, the existence of a central ontology allows the application for the development of specific ontologies.

As a demonstration of the possibility of reusing the Onto4CAAL ontology, a domain ontology for the vertical elevation platform (Onto4Elev) was proposed, which is one of the numerous applications associated with transport-type AAL systems and is a subclassifications of the systems associated with Services of Comfort, according to the Nehmer classification [28].

Onto4Elev is a domain ontology that inherited several classes from Onto4CAAL, as can be seen in the image contained in GITHUB.Due to the specificity of vertical lifting platforms (PEV), it wasnecessary to investigate the Literature to find which elements should be considered for the construction of a PEV, which are those highlighted with the edge of the class in green in Figure 4. To verify/validate the elements that were raised in the literature and initially proposed to compose the Onto4Elev ontology, a survey was carried out with professionals working in the PEV construction industry [34].

Next, we will see about the UML notation of Onto4Elev and the axioms resulting from the extension of Onto4CAAL to the domain of PEVs:

Figure 3. Class hierarchy of the Onto4CAAL ontology in the Protegé tool.

[FIGURE]

## 4.1. Survey for verification of Onto4Elev elements

The target audience of this survey was professionals from the Brazilian industry who work with PEV development. For this, a survey was conducted with several Brazilian companies (18 in total), as well as professionals who work in these companies (via LinkedIn). For application and data collection, a questionnaire was used, prepared through the online tool QuestionPro,

|

consisting of seven questions and accessed through the link (https://questionpro.com/t/ATQIUZsqND). Seven respondents answered the survey, four of them from the technical area, two are business owners and one is from the commercial area. As a result, there were contributions in the elements associated with Application Environments of PEV's,Mechanical Components, Electrical Devices, Signaling and Stakeholders.

## 4.2. Onto4Elev UML notation

Theimagecontainedinthelink(https://github.com/timoteogomes/ Onto4Elev.git) presents the complete modeling of all modules associated with PEV-type AAL systems, where it is possible to identify both elements that were added through the collection of information in the literature (these are the ones with the classes in green), and those that were added as a result of the survey, which are the ones that are hatched with blue dots. The elements represented by the classes with the black borders are the ones that were inherited from Onto4CAAL.

Hereafter, we will highlight the adaptations that occurred in Onto4CAAL to enable the construction of Onto4Elev, associating each image with the type of element that was adjusted.

## 4.2.1. Types of environments

As described in Figure 4, it is possible to see that there was an aggregation of types of application environments for the PEVs, with their emphasis on the external context (public and commercial places).

## 4.2.2. Mechanical components

For the PEV-type AAL system, the Mechanical Components element was added to Onto4Elev, making it possible to notice that this element, as shown in Figure 5, is not part of the constitution of the central ontology, that is, of Onto4CAAL, but it has several components that are used in the construction of PEVs and that need to be considered when specifying the requirements.

## 4.2.3. Electrical devices

Regarding electrical devices, according to Figure 6, several new sub-elements were added, such as the platform control device, which is something specific to this type of systems.

## 4.2.4. Signaling

For the PEV type AAL system, the Signaling type element was added to Onto4Elev, making it possible to notice that this element, as shown in Figure 6, is not part of the constitution of the central ontology, that is, of Onto4CAAL, but it is extremely important in the context of the PEVs.

## 4.2.5. Stakeholders

Regarding the stakeholders, according to Figure 7, several new sub-elements were added, such as the Architect and the Civil Engineer, where both can participate in the construction project of a PEV, as well as the role of the Operator, precisely due to the specificity of this type of AAL system.

## 4.2.6. Compliance

Regarding compliance-related issues, according to Figure 8, several regulatory standards were added and must be considered, taking into consideration the context in Brazil, when building PEVs. Such standards (accessibility to buildings, furniture, spaces and urban equipment) include NBR 9050, which deals with

|

[FIGURE]

Figure 4. Modeling of the Environment class of the Onto4Elev ontology (built in the VisualParadigm tool).

Figure 5. Modeling of the MechanicalComponent class of the Onto4Elev ontology (built in the VisualParadigm tool).

[FIGURE]

Figure 6. Modeling the ElectricDevice and Signaling classes of the Onto4Elev ontology (built in the VisualParadigm tool).

[FIGURE]

accessibility issues, and NBR ISO 9386-1 (Powered lifting platforms for people with reduced mobility) that addresses safety and operating requirements.

## 4.2.7. Requirements

Regarding the requirements, it is important to highlight that even with the literature research, as well as with the application of the survey with experts from the PEV manufacturing industry, those contained in Onto4CAAL meet the context of Onto4Elev. This demonstrates the completeness of Garces' taxonomy [35].

## 4.3. Onto4Elev axioms

Next, some of the axioms of Onto4Elev that were incorporated to the others inherited from Onto4CAAL are presented.

## 4.3.1. Axioms of environment types

Table 7 presents the inclusion of axioms established for the environment types' module in the context of Onto4Elev.

Among the axioms that are presented, we have the ' PublicPlaces ≡ Churches ⊔ PublicOffices ', which represents the set of public places, which is formed by the Churches or PublicOffices instances.

Figure 7. Modeling of the Stakeholder class of the Onto4Elev ontology (built in the VisualParadigm tool).

[FIGURE]

Figure 8. Modeling of the Compliance class of the Onto4Elev ontology (built in the VisualParadigm tool).

[FIGURE]

Table 7. Environment axioms (Onto4Elev).

| Representation   | Axioms                                                                                                                                                                                                                         |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T E              | Environment ≡ CommercialEnvironments ⊔ House ⊔ LongStayElderlyInstitution ⊔ PublicPlaces CommercialEnvironments ≡ Airports ⊔ Banks ⊔ Clinics ⊔ Pharmacies ⊔ Restaurants ⊔ Supermarkets PublicPlaces ≡ Churches ⊔ PublicOffices |

Table 8. Mechanical component axioms (Onto4Elev).

| Representation   | Axioms                                                                                                                                                                                                                                                                                                     |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T MC             | MechanicalComponent ≡ Key ⊔ Barrier ⊔ SafetyBrake ⊔ Guides ⊔ RackDrive ⊔ GearWheel ⊔ Pinion ⊔ MechanicalBlockingDevice ⊔ Gear ⊔ Bearing ⊔ Sow ⊔ Chain ⊔ Valve ⊔ EnclosedBox ⊔ SpindleTrigger ⊔ ProtectorSill ⊔ HydraulicPiston ⊔ CentralHydraulic Valve ≡ ValveFall ⊔ PressureReliefValve ⊔ ValveSenseDown |

Table 9. ElectricDevice axioms (Onto4Elev).

| Representation   | Axioms                                                                                                                                                                                                                                                                                                                    |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T ED             | ElectricDevice ≡ CommandByVoice ⊔ Camera ⊔ InverterFrequency ⊔ LedLamps ⊔ Button ⊔ Autosafe ⊔ Display ⊔ Sensor ⊔ DeviceControlPlatform ⊔ Switches ⊔ StopSwitch ⊔ Actuator ⊔ Intercom ⊔ SafetySwitch ⊔ ContactorRelay ⊔ SwitchLooseningCableCurrent ⊔ LimiterSpeed ⊔ LimitingKeyFinalPercourse ⊔ ElectronicCurtainSecurity |

Table 10. Stakeholders axioms (Onto4Elev).

| Representation   | Axioms                                                                                                                                                                                     |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T S              | People ≡ MemberTimeDev ⊔ FinalUser ⊔ Operator ⊔ Caregiver ⊔ Domestic Companion ⊔ Familiar MemberTimeDev ≡ CivilEngineer ⊔ MechanicalEngineer ⊔ Architect FinalUser ≡ Handicapped ⊔ Elderly |

|

|

Table 11. Signaling axioms (Onto4Elev).

| Representation   | Axioms                                                            |
|------------------|-------------------------------------------------------------------|
| T E              | Signaling ≡ Braille ⊔ Sound Braille ⊑ Signaling Sound ⊑ Signaling |

## 4.3.2. Axioms of mechanical components

Table 8 presents two axioms among those established for the Mechanical Components module in the Onto4Elev ontology. The axiom ' Valve ≡ ValveFall ⊔ PressureReliefValve ⊔ ValveSenseDown ', for example, represents the set of possible instances of the Valve component, which is one of the possible instances of the Mechanical Components element.

## 4.3.3. Axioms of electrical devices

Table 9 presents one of the axioms established for the Electrical Devices module, and it is possible to see that several devices were added as instances of this module, such as the 'Switch Loosening Cable Current', which occurred due to the specific characteristics of the systems of the type PEV.

## 4.3.4. Stakeholder axioms

Table 10 presents three axioms among those established for the Onto4Elev Stakeholder module. The axiom ' FinalUser ≡ Handicapped ⊔ Elderly ', for example, is an axiom that represents the set of possible instances of the UserFinal component, where, given the specificity of the VEP's, there was the inclusion of two possible end users, which are the elderly and the ones with disabilities.

## 4.3.5. Signaling axioms

Table 11 presents three axioms established for the Onto4Elev Signaling module. The axiom ' Signaling ≡ Braille ⊔ Sound ', for example, represents the set of instances for Signaling, highlighting that this module was created for the context of Onto4Elev, that is, it does not originally belong to the central ontology Onto4CAAL.

## 5. CASE STUDY

In this section, we lodge the application of a case study where the requirements are used in the development of AAL systems of the Vertical Lift Platforms type, knowing that these requirements were extracted from the literature [36]. The case study aims to demonstrate the suitability of the application ontology for Vertical Elevation Platforms, Onto4Elev.

## 5.1. Scenario

The domain ontology was instantiated with requirements of a mechanical design of a motorized lifting platform for people with reduced mobility, proposed by Gomes [36]. In the work, he proposed several specific requirements for the construction of this platform. According to Gomes [36], there are several standards that apply to the design of elevators and platforms, such as: NBR 12892 (Design, manufacture and installation of a single-family elevator), NBR 16042 (Electric passenger elevators) and NBR 93861 (Platforms lifts for people with reduced mobility), the latter being the one used in the proposed project and the one applied in this scenario. The platform proposed in the project was the spindle drive type, which is one of the eight types for this type of platform.

Figure 9. Onto4Elev ontology metrics in the Protegé tool.

[FIGURE]

## 5.2. Requirements

After analyzing the project proposed by Gomes [36], 16 requirements were elicited, contained in Table 12, where each one received an identifier, in addition to the description and type, based on the Onto4Elev Requirements Module.

## 5.3. Onto4Elev ontology simulation in Protegé

To instantiate Onto4Elev and simulate the established scenario, the Protégé tool (version 5.5.0) was used, which is an open source application for creating and editing ontologies, offering a graphical interface and an architecture for creating knowledgebased tools, with Onto4Elev built, as shown in Figure 9, where the classes created in that tool are demonstrated. It is possible to see in Figure 9 the six modules defined for the composition of Onto4CAAL, highlighting the AALSystems module, which consists of the EmergencyTreatmentServices, ComfortServices and Autonomy EnhancementServices classes, in addition to the subclasses of each one of them. After the inclusion of the classes, properties and axioms were also added. As can be seen in Figure 10, there are also 196 classes, in addition to the 682 axioms, 28 object properties and 7 data properties.

Then, the Onto4Elev instantiation was performed by inserting the requirements contained in Table 12, where at the end,

Table 12. Signaling axioms (Onto4Elev).

| Requerimet   | Description                                                                                                                                                                          | Type                                      |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| REQ-1        | PEV must have a maximum speed of 0.15 m/s                                                                                                                                            | Security - > Integrity                    |
| REQ-2        | The minimum flat dimensions of the PEV for the adopted use, which was the cabin with a companion standing behind the wheelchair user, are 800 × 1600 mm(width × length)              | Usability - > Adequacy                    |
| REQ-3        | According to ABNT NBR ISO 9386-1:2013, equipment must have ways to stop                                                                                                              | Reliability - > ToleranceError            |
| REQ-4        | PEV must have a normally closed electromagnetic brake                                                                                                                                | Performance efficiency - > UseResource    |
| REQ-5        | PEV must have brake against failure of the drive system                                                                                                                              | Reliability - > Recoverability            |
| REQ-6        | PEV must have a motor starter controlled by a frequency inverter                                                                                                                     | Performance efficiency - > UseResource    |
| REQ-7        | The ABNT NBR ISO 9386-1:2013 standard defines that the safety factor for all parts of the equipment must be greater than or equal to 1.6. For this project, the defined factor was 7 | Security - > Responsibility               |
| REQ-8        | PEV floor covering must be non-slip                                                                                                                                                  | Risk-free - > MitigationHealthRisksSafety |
| REQ-9        | PEV bearing must be replaced every 3 years                                                                                                                                           | Maintainability - > Mobility              |
| REQ-10       | The nominal load considered for the PEV must be 2453 N                                                                                                                               | Performance efficiency- > capacity        |
| REQ-11       | Life expectancy of the PEV was defined for a daily use of 1 h in 10 years, resulting in 3.650 h                                                                                      | Performance efficiency - > BehaviorTime   |
| REQ-12       | PEV deployed by spindle must have a safety nut, which is coupled to the nut and aim to prevent an uncontrolled fall of the nut onto the spindle                                      | Reliability - > ToleranceError            |
| REQ-13       | PEV will have the up and down buttons inside the platform, in addition to the call buttons on both floors                                                                            | Usability- > UserOperability              |
| REQ-14       | PEV will have three types of buttons according to NBR9386-1 [15]: operation buttons, emergency alarm and emergency stop                                                              | Usability- > UserOperability              |
| REQ-15       | Each floor will feature a call button and a protected emergency button                                                                                                               | Usability- > UserOperability              |
| REQ-16       | According to the NBR 9386-1 standard, it is necessary to ensure that the button is kept pressed during the entire trip                                                               | Usability - > ProtectionAgainstUserErrors |

## Table 13. ABox Instâncias Cenário 1.

A c1

AAL(PEV-Demo) System, Software(software-control), Hardware(EmergencyButton- ChampionType), Ambient (Home), usedAt(home), uses(software-control), holds(EmergencyButton-ChampionType), Compliance (NBR\_ISO\_9386-1), influence (REQ-3, REQ-7, REQ-14, REQ-16), Requirement(REQ-1), Requirement (REQ-2), Requirement (REQ-3), Requirement (REQ-4), Requirement (REQ-5), Requirement (REQ-6), Requirement o(REQ-7), Requirement (REQ-8), Requirement (REQ-9), Requirement (REQ-10), Requirement (REQ-11), Requirement (REQ-12), Requirement (REQ-13), Requirement (REQ-14), Requirement (REQ-15), Requirement (REQ-16), define(Tulio, REQ-1), define(Davi, REQ-2), define(Tulio, REQ-3), define(Tulio, REQ-4), define(Tulio, REQ-5), define(Tulio, REQ-6), define(Tulio, REQ-7), define(Tulio, REQ-8), define(Tulio, REQ-9), define(Tulio, REQ-10), define(Tulio, REQ-11), define(Tulio, REQ-12), define(Tulio, REQ-13), define(Tulio, REQ-14), define(Tulio, REQ-15), define(Tulio, REQ-16), Requires(PEV-Demo, REQ-1), Requires(PEV-Demo, REQ-2), Requires(PEV-Demo, REQ-3), Requires (PEV-Demo, REQ-4), Requires (PEV-Demo, REQ-5), Requires (PEV-Demo, REQ-6), Requires (PEV-Demo, REQ-7), Requires (PEV-Demo, REQ-8), Requires (PEV-Demo, REQ-9), Requires (PEV-Demo, REQ-10), Requires (PEV-Demo, REQ-11), temRequisito(PEV-Demo, REQ-12), Requires (PEV-Demo, REQ-13), Requires (PEV-Demo, REQ-14), Requires (PEV-Demo, REQ-15), Requires (PEV-Demo, REQ-16), causesPositiveImpact(REQ-14, REQ-15), causesPositiveImpact(REQ-16, REQ-15)

## Table 14. Inferências ABox 1.

| define(Tulio, REQ-1), Requirement(REQ-1) &#124; = Stakeholder(Tulio) define(Davi, REQ-2), Requirement (REQ-2) &#124; = Stakeholder(Davi)   |
|--------------------------------------------------------------------------------------------------------------------------------------------|
| define(Tulio, REQ-3), Requirement (REQ-3) &#124; = Stakeholder(Tulio)                                                                      |
| define(Tulio, REQ-4), Requirement (REQ-4) &#124; = Stakeholder(Tulio)                                                                      |
| define(Tulio, REQ-5), Requirement (REQ-5) &#124; = Stakeholder(Tulio)                                                                      |
| define(Tulio, REQ-6), Requirement (REQ-6) &#124; = Stakeholder(Tulio)                                                                      |
| define(Tulio, REQ-7), Requirement (REQ-7) &#124; = Stakeholder(Tulio)                                                                      |
| define(Tulio, REQ-8), Requirement (REQ-8) &#124; = Stakeholder(Tulio)                                                                      |
| define(Tulio, REQ-9), Requirement (REQ-9) &#124; = Stakeholder(Tulio)                                                                      |
| define(Tulio, REQ-10), Requirement (REQ-10) &#124; = Stakeholder(Tulio)                                                                    |
| define(Tulio, REQ-11), Requirement (REQ-11) &#124; = Stakeholder(Tulio)                                                                    |
| define(Tulio, REQ-12), Requirement (REQ-12) &#124; = Stakeholder(Tulio)                                                                    |
| define(Tulio, REQ-13), Requirement (REQ-13) &#124; = Stakeholder(Tulio)                                                                    |
| define(Tulio, REQ-14), Requirement (REQ-14) &#124; = Stakeholder(Tulio)                                                                    |
| define(Tulio, REQ-15), Requirement (REQ-15) &#124; = Stakeholder(Tulio)                                                                    |
| define(Tulio, REQ-16), Requirement (REQ-16) &#124; = Stakeholder(Tulio)                                                                    |

coherence and consistency tests were performed, using the HermiT reasoner (version 1.4.3) and Pellet, both native to Protégé.

Figure 11 demonstrates that Onto4Elev is consistent and coherent, thus being considered an operational ontology.

Figures 12-14 present the results of simulations in Descriptive Logic (DL) queries. In Figure 12, it is possible to notice that when executing the test to evaluate the return of the Stakeholder Class, we can verify that two actors were inserted (Davi, Túlio), where Túlio is selected and informed that he is a Mechanical Engineer Stakeholder and that he defined the requirements REQ-1, REQ3, REQ-4, REQ-5, REQ-6, REQ-7, REQ-8, REQ-9, REQ-10, REQ-11, REQ-12, REQ-13, REQ-14, REQ-15 and REQ-16. In Figure 13, we can see that the NBR ISO 9386-1 Standard was instantiated in the Compliance Class, which is of the NBR type, and it is a Standard that has influence on the requirements REQ-3, REQ-7, REQ-14 and REQ-16. Still dealing with the query by DL, it is possible to see in Figure 14 the result of the query to the Requirement Class, where all 16 requirements contained in Table 12 are returned. In addition, it is possible to identify that the REQ-7 was defined by the stakeholder Túlio and that this requirement is influenced by the NBR ISO 9386-1 Standard. Figure 15 shows the presentation of existing relationships with REQ-7. This shows the usefulness

|

|

## Table 15. Inferências ABox 2.

usedAt(home) (casa), uses(software-control), holds(EmergencyButton-ChampionType), Requires(REQ-1, REQ-2, REQ-3, REQ-4, REQ-5, REQ-6, REQ-7, REQ-8, REQ-9, REQ-10, REQ-11, REQ-12, REQ-13, REQ-14, REQ-15 e REQ-16) | = AAL(PEV-Demo) System

Table 16. Inferências ABox 3.

| hasRequirement (PEV-Demo, REQ-1) &#124; = NonFunctionalRequirement(REQ-1)    |
|------------------------------------------------------------------------------|
| hasRequirement (PEV-Demo, REQ-2) &#124; = NonFunctionalRequirement (REQ-2)   |
| hasRequirement (PEV-Demo, REQ-3) &#124; = NonFunctionalRequirement (REQ-3)   |
| hasRequirement (PEV-Demo, REQ-4) &#124; = NonFunctionalRequirement (REQ-4)   |
| hasRequirement (PEV-Demo, REQ-5) &#124; = NonFunctionalRequirement (REQ-5)   |
| hasRequirement (PEV-Demo, REQ-6) &#124; = NonFunctionalRequirement (REQ-6)   |
| hasRequirement (PEV-Demo, REQ-7) &#124; = NonFunctionalRequirement (REQ-7)   |
| hasRequirement (PEV-Demo, REQ-8) &#124; = NonFunctionalRequirement (REQ-9)   |
| hasRequirement (PEV-Demo, REQ-10) &#124; = NonFunctionalRequirement (REQ-11) |
| hasRequirement (PEV-Demo, REQ-12) &#124; = NonFunctionalRequirement (REQ-13) |
| hasRequirement (PEV-Demo, REQ-14) &#124; = NonFunctionalRequirement (REQ-14) |
| hasRequirement (PEV-Demo, REQ-15) &#124; = NonFunctionalRequirement (REQ-15) |
| hasRequirement (PEV-Demo, REQ-16) &#124; = NonFunctionalRequirement (REQ-16) |

Table 17. Inferências ABox 4.

influence(NBR\_ISO\_9386-1, PEV-Demo) | = Standard(NBR\_ISO\_9386-1)

## Table 18. Inferências ABox 5.

causesPositiveImpact (REQ-14, REQ-15) | = Requirement(REQ-14)

causesPositiveImpact (REQ-16, REQ-15) | = Requirement(REQ-16)

Figure 10. Onto4Elev ontology metrics in the Protegé tool.

[FIGURE]

in traceability when using Ontology with the support of an editor, such as Protegé.

## 5.4. Verification of the Onto4Elev ontology in the ABox form

Then, the real scenario is presented in ABox form to illustrate the simulation performed by the Protégé tool. For the evaluated scenario, we highlight the input and the inferences obtained.

## 5.4.1. ABox of scenario 1:

Table 13 presents the instances of the domain scenario of the Vertical Lift Platform project. Table 14 presents the ABox of inferences made for Scenario 1. These inferences aim to validate the Onto4Elev ontology to demonstrate its suitability for the domain of Vertical Elevation Platforms.

It is important to note that the results of the inferences will be presented in ABox. In this process, we consider the axioms presented in Table 13 and the terminological axioms laid out in the Onto4CAAL and Onto4Elev Ontologies.

As shown in Table 14, in these first inferences, we have that Tulio and Davi meet the necessary conditions to be considered a Stakeholder, because, according to the axioms of Onto4CAAL, it is considered a Stakeholder when it defines some requirement. It is also possible to infer each Stakeholder defines some requirements, namely:

- Tulio-REQ-1, REQ-3, REQ-4, REQ-5, REQ-6, REQ-7, REQ-8, REQ-9, REQ-10, REQ-11, REQ-12, REQ-13, REQ-14, REQ-15 and REQ-16
- Davi-REQ-2

As shown in Table 15, the resources presented are considered resources of a PEV. Therefore, according to the axioms of Onto4CAAL, PEV-Demo is considered an AAL System because it is used in an Environment, it has a Hardware, it uses a Software and it has Requirements.

According to Table 16, we can infer that REQ-1, REQ-2, REQ3, REQ-4, REQ-5, REQ-6, REQ-7, REQ-8, REQ-9, REQ-10, REQ-11, REQ-12, REQ-13, REQ-14, REQ-15 and REQ-16 are PEV-Demo system requirements.

According to the inference from Table 17, a Standard influences the AAL system (PEV-Demo). The defined Standard is NBR\_ISO\_9386-1, this Standard deals precisely with the safety requirements, dimensions and functional operation of vertical lifting platforms.

Table 18 presents the inferences for the positive-causeImpact concept. In this query, it is possible to identify that requirements REQ-14 and REQ-16 have a positive impact on the requirement of REQ-15. An interesting factor with the proposed ontology is the traceability of requirements, it is possible to track which requirements have impacts on others (positive and/or negative) and describe the cause. In Requirements Engineering, traceability is an important part of the systems engineering process, as it ensures that all requirements have been carefully considered during each phase of development, and that there are no scope 'gaps' in the developed system due to missed requirements. This also ensures that all requirements are internally consistent with each other.

## 6. VERIFICATION-UFO STANDARDS

Therefore,by adopting UFO as the top-level ontology,the modeling of the ontologies proposed in this thesis is responding to UFO's grounding rules [32]. It is important to highlight that, to simplify the modeling, we performed the union of categories and restriction structures, thus helping to generate coherent taxonomic relationships and establish a well-founded ontological concept.

[FIGURE]

Figure 11. Onto4Elev consistency and coherence demo screen.

Figure 12. DL query screen for stakeholder class.

[FIGURE]

Figure 13. DL query screen for compliance class.

[FIGURE]

In this work, some of these UFO modeling patterns were adopted. Below we will see the application and verification of some of them, such as:

## 6.1. Kind and subkind patterns

The Kind Pattern represents a substantial sortal that provides an identity principle for its instances, being responsible for structuring the taxonomy representing the domain. Kinds can be specialized into other rigid subtypes that inherit the principle of identity and are called Subkinds. A Long Stay

|

Institution for the Elderly is considered a «kind» in the ontologies proposed in this thesis. It has, in turn, subtypes, such as Asylum, GeriatricHouse and MedicalHouse, which are classified as a «subkind», since they inherit the principle of identity from the InstituicaoLongPermanenciaIdosos class, as shown in Figure 16.

## 6.2. RoleMixin and role patterns

Anti-rigids that abstract properties common to Role types are called RoleMixin. The RoleMixin pattern is used to handle situations where the dependent anti-hard type is specifically used to instantiate different subtypes of kinds. In addition to requiring external dependencies, such as the &lt;&lt; role &gt;&gt; type, the supertype

|

Figure 14. DL query screen for requirement class.

[FIGURE]

Figure 15. REQ-7 explanation screen and its relationships.

[FIGURE]

Table 19. Comparison between ontologies.

| Ontologies   | Types of systems   | Devices   | Environments   | Stakeholders   | Product quality NFRs   | Quality of use NFRs   | Ethical requirements   | Compliance   |
|--------------|--------------------|-----------|----------------|----------------|------------------------|-----------------------|------------------------|--------------|
| GoAAL        | X                  | X         | X              | X              | -                      | -                     | -                      | -            |
| MoMOntology  | -                  | X         | -              | X              | -                      | -                     | -                      | -            |
| VAALID       | -                  | X         | X              | X              | -                      | -                     | -                      | -            |
| Onto4CAAL    | X                  | X         | X              | X              | X                      | X                     | X                      | X            |

[FIGURE]

Figure 16. Kind and subkind patterns.

Figure 17. RoleMixin and role patterns.

[FIGURE]

must be a &lt; &lt; rolemixin &gt;&gt; . In Figure 17, we can see that the Stakeholder class is &lt;&lt; RoleMixin &gt;&gt; , which, in turn, generalizes several classes, which are classified as &lt;&lt; role &gt;&gt; , like the FinalUser and Manufacturer class, in which FinalUser is a specialization of the Person class ( &lt;&lt; kind &gt;&gt; ), while Manufacturer is a specialization of the Organization class, which is a &lt; &lt; kind &gt; &gt; .

## 7. RELATED WORKS

Cameranesi [37] points out that models and methodologies capable of aiding AAL system designers during development are still lacking. Before that, Cameranesi proposed an ontology (GoAAL) to formally represent the relevant knowledge in the AAL domain, objectives to measurements and sensors vary. Although the GoAAL ontology includes AAL elements, such as devices, stakeholders and environments, it is possible to see, according to Table 19, that there is no coverage for NRF elements of any type (product quality and quality of use), ethical requirements and compliance.

Villarreal [38] presents an ontology for classifying medical elements such as diseases, recommendations, preventions, food, mobile devices and diet suggestions, this ontology is called MoMOntology. Based on this ontology, an application that generates individual patient profiles, self-control and education modules for their chronic diseases was developed. As can be seen in Table 7, in MoMOntology, there is no coverage for the elements of AAL system types, environment, NRF's of any kind (product quality and quality of use), ethical requirements and compliance.

Mocholí [39] describes a set of ontologies created within the framework of the European VAALID project that allows the designers of AAL services to model and characterize an AAL environment, the actors involved and the diverse types of spaces and devices. As can be seen in Table 7, there is no coverage for the elements of types of AAL systems, NRF's of any type (product quality and quality of use), ethical requirements and compliance.

## 8. LIMITATIONS AND FUTURE WORKS

For this survey, we identified the size of the sample used as the main limitation. Considering that the sampling method used was non-probabilistic, which does not define the sample size [40], it is practically impossible to measure (there is no way to determine the exact number of researchers and industry professionals working in the development of AAL systems), the representativeness of the population or the percentage of respondents who responded to the questionnaire. As future work, the stages of compliance with the methodology chosen for the construction of the ontology will be continued, where the stages of instantiation and evaluation, documentation and maintenance will be carried out.

## 9. CONCLUSION

As it is an area with several subdomains and specificities, the development of AAL systems requires a specification of requirements that includes numerous factors involved. The challenges in developing AAL systems have led the academic community to explore and establish original approaches for the development of this type of system, such as the use of ontologies. Based on this, an ontology proposal was built, the Onto4CAAL, which can help AAL system designers in the requirements specification process, guiding on the types of AAL systems that can be developed, their area (specificity) of application, the environments, agents and devices that can be taken into account for this type of system. Ontology also makes possible to analyze which NFR's are considered, as well as to evaluate the view regarding the Compliance and NFR's relationship in AAL systems and the treatment given to the ethical requirements in these systems.

## ACKNOWLEDGEMENTS

We would like to thank CAPES for providing the necessary resources for the elaboration of the work and the Graduate Program in Electrical Engineering (PPGEE/UFPE).

## DATA AVAILABILITY

The data underlying this article will be shared on reasonable request to the corresponding author.

|

|

Timóteo G. Silva is from the Federal University of Pernambuco (UFPE), linked to the Graduate Program in Electrical Engineering (PPGEE/UFPE), Electronics and Systems Department, 50.740560, Recife-Brazil-and also linked to the National Commission of Nuclear Energy (CNEN), located at the Northeast Regional Center for Nuclear Sciences (CRCN-NE), Av. Professor Luiz Freire, 200, Cidade Universitária, Recife-Brazil (e-mail: timoteogomes@yahoo.com.br).

Fernanda Alencar is from the Federal University of Pernambuco (UFPE), linked to the Graduate Program in Electrical Engineering (PPGEE/UFPE), Electronics and Systems Department, 50.740-560, Recife-Brazil (e-mail: fernandaalenc@gmail.com).

## REFERENCES

1. Cicirelli, G., Marani, R., Petitti, A., Milella, A. and D'Orazio, T. (2021) Ambient assisted living: a review of technologies, methodologies and future perspectives for healthy aging of population. Sensors , 21 , 3549.
2. Vimarlund, V., Borycki, E.M., Kushniruk, A.W. and Avenberg, K. (2021) Ambient assisted living: identifying new challenges and needs for digital technologies and service innovation. Yearb. Med. Inform. , 30 , 141-149.
3. Programm AAL. https://ec.europa.eu/eurostat/statisticsexplained/index.php (accessed July 4, 2022).
4. Cheng, D.C., Villamarin, J.B., Cu, G. and Lim-Cheng, N.R. (2018) Towards Compliance Management Automation thru Ontology mapping of Requirements to Activities and Controls. In: Khairul Akram, Z.A., Masnizah, M., Zarina, S. (Eds.) 2018 Cyber Resilience Conference (CRC) , pp. 1-3. IEEE.
5. Lentzas, A. and Vrakas, D. (2019) Non-intrusive human activity recognition and abnormal behavior detection on elderly people: a review. Artif. Intell. Rev. , 53 , 1-47.
6. Silva, T.G. and Alencar, F.M. (2020) Ontologias Para Sistemas AAL que abordem compliance: um mapeamento sistemático da literatura. 13 ◦ ONTOBRAS. CEUR Workshop Proceedings . 2728 , 120-133.
7. Gomes, T. and Alencar, F. (2021) Análise de Ontologias para Sistemas AAL (Ambient Assisted Living) e o suporte a Compliance. In: Maria Lencastre Pinheiro de Menezes Cruz, Graciela Dora Susana Hadad, Johnny Cardoso Marques (Eds.) 24th WER . Anais do Workshop em Engenharia de Requisitos, Brasilia, BSB, Brazil.
8. Benghazi, K., Hurtado, M.V., Hornos, M.J., Rodríguez, M.L., Rodríguez-Domínguez, C., Pelegrina, A.B. and Rodríguez-Fórtiz, M.J. (2012) Enabling correct design and formal analysis of ambient assisted living systems. J. Syst. Software , 85 , 498-510.
9. Ranieri, C.M., MacLeod, S., Dragone, M., Vargas, P.A. and Romero, R.A.F. (2021) Activity recognition for ambient assisted living with videos, inertial units and ambient sensors. Sensors , 21 , 768.
10. Machado, A., Maran, V., Augustin, I., Wives, L.K. and de Oliveira, J.P .M. (2017) Reactive, pro-active, and extensible situationawareness in ambient assisted living. Expert Syst. Appl. , 76 , 21-35.
11. Nakagawa, E.Y., Antonino, P.O., Becker, M., Maldonado, J.C., Storf, H., Villela, K.B. and Rombach, D. (2013) Relevance and perspectives of AAL in Brazil. J. Syst. Software , 86 , 985-996.
12. Netto, C.M. (2017) Proposta de modelo de requisitos para ferramentas de visualização de ontologia de domínio . UFMG.
13. Gruber, T.R. (1993) A translation approach to portable ontology specifications. Knowl. Acq. , 5 , 199-220.
14. Felicíssimo, C.H. and Breitman, K.K. (2004) Taxonomic Ontology Alignmentan Implementation. In: Marcela Ridao, Luiz Marcio Cysneiros (Eds.) WER , pp. 152-163. Anais do Workshop em Engenharia de Requisitos, Tandil, Argentina.
15. Campos, M.L.A. (2010) O papel das definições na pesquisa em ontologia. Perspect. Ciênc. Inf. , 15 , 220-238.
16. Vital, L.P. and Café, L.M.A. (2011) Ontologias e taxonomias: diferenças. Perspect. Ciênc. Inf. , 16 , 115-130.
17. Culmone, R., Falcioni, M., Giuliodori, P., Merelli, E., Orru, A., Quadrini, M., Ciampolini, P., Grossi, F., Matrella, G. (2014) AAL domain ontology for event-based human activity recognition. In IEEE/ASME 10th International Conference on Mechatronic and Embedded Systems and Applications (MESA) , pp. 1-6. IEEE, Senigallia - Le Marche.
18. Coimbra,M.A.and Manzi,V.A.(2010) Manual de Compliance . Atlas, São Paulo.
19. NBR ISO 19600/2016 (2016) - Sistema de Gestão de Compliance: Diretrizes . ABNT, Brazil.
20. Zhong, B.T., Ding, L.Y., Luo, H.B., Zhou, Y ., Hu, Y .Z. and Hu, H.M. (2012) Ontology-based semantic modeling of regulation constraint for automated construction quality compliance checking. Autom. Constr. , 28 , 58-70.
21. Jorshari, F.Z. and Tawil, R.H. (2015) A High-Level Scheme for an Ontology-Based Compliance Framework in Software Development. In IEEE 17th International Conference on High Performance Computing and Communications , pp. 1479-1487. IEEE, New York, NY, USA.
22. Abran, A. et al. (2004) Guide to the Software Engineering Body of Knowledge (SWEBOK (R)) (3rd edn). IEEE Computer Society, Los Alamitos, CA.
23. Carvalho, E.A., Eescovedo, T., Melo, R.N. (2009) Using Business Processes in System Requirements Definition. In 2009 33rd Annual IEEE Software Engineering Workshop , pp. 125-130. Skovde, Sweden.
24. Bettaz, M. and Maouche, M. (2018) Using UML-MARTE and TCOZ for AAL System Specifications: A Case Study. In 7th International Conference on Reliability, Infocom Technologies and Optimization (Trends and Future Directions) (ICRITO) , pp. 1-6. IEEE, Noida, India.
25. Alosaimi, W., Ansari, M.T.J., Alharbi, A., Alyami, H., Seh, A.H., Pandey, A.K., Agrawal, A. and Khan, R.A. (2021) Evaluating the impact of different symmetrical models of ambient assisted living systems. Symmetry , 13 , 450.
26. Augusto, J.C. (2009) Increasing Reliability in the Development of Intelligent Environments. In Intelligent Environments , pp. 134-141. Barcelona, Spain.
27. Erazo-Garzon, L., Illescas-Peña, L. and Cedillo, P. (2020) A Quality in Use Model for Ambient Assisted Living (AAL) Systems. In: Miguel Botto-Tobar, Marcelo Zambrano Vizuete, Sergio Montes León, Pablo Torres-Carrión, Benjamin Durakovic (Eds.) Applied Technologies: Second International Conference, ICAT 2020 , Quito, Ecuador, December 2-4, Proceedings 2, pp. 643-660. Springer International Publishing.
28. Nehmer, J., Becker, M., Karshmer, A. and Lamm, R. (2006) Living Assistance Systems: An Ambient Intelligence Approach.In: Leon J. Osterweil, Dieter Rombach, Mary Lou Soffa (Eds.) Proceedings of the 28th International Conference on Software Engineering pp. 43-50. Shanghai China.
29. Rautenberg, S., Todesco, J.L., Steil, A.V . and Gauthier, F.A.O. (2008) A methodology for the development of ontologies. Rev. Ciênc. Exat. Natur. , 10 , 237-262.

30. Gómez-Pérez, A., Fernández-López, M. and Corcho, O. (2006) Ontologic Engineering: With Examples from the Areas of Knowledge Management, E-Commerce and the Semantic Web . Springer Science &amp; Business Media.
31. Corcho, O., Fernández-López, M. and Gómez-Pérez, A. (2006) Ontological Engineering: Principles, Methods, Tools and Languages. In: Coral Calero, Francisco Ruiz, Mario Piattini (Eds.) Ontologies for Software Engineering and Software Technology [s.l.], pp. 1-48. Springer.
32. Guizzardi, G. (2005) Ontological foundations for structural conceptual models. CTIT, Centre for Telematics and Information Technology, Enschede.
33. Guizzardi, G. and Wagner, G. (2012) Conceptual Simulation Modeling with ONTO-UML Advanced Tutorial. In: Proceedings of the 2012 Winter Simulation Conference (WSC) , pp. 1-15. IEEE, Berlin Germany.
34. Gomes, T. and Alencar, F. (2022) Um survey com especialistas como validação de elementos para composição de uma ontologia para Sistemas AAL (Ambient Assisted Living). In: 25th WER . Natal, Brasil.
35. Garcés, L., Ampatzoglou, A., Avgeriou, P. and Nakagawa, E.Y. (2017) Quality attributes and quality models for ambient

|

- assisted living software systems: a systematic mapping. Inf. Software Technol. , 82 , 121-138.
36. Gomes, T.B. (2019) Projeto mecânico de uma plataforma de elevação motorizada para pessoas com mobilidade reduzida . Universidade de Brasília.
37. Cameranesi, M. et al. (2016) Goaal: An Ontology for GoalOriented dDevelopment of AAL Environments. In: Proceedings of the 31st Annual ACM Symposium on Applied Computing , pp. 347-353. Pisa Italy.
38. Villarreal, V ., Fontecha, J., Hervas, R. and Bravo, J. (2014) Mobile and ubiquitous architecture for the medical control of chronic diseases through the use of intelligent devices: using the architecture for patients with diabetes. Future Gener. Comput. Syst. , 34 , 161-175.
39. Mocholí, J.B., Sala, P., Fernandez-Llatas, C. and Naranjo, J.-C. (2010) Ontology for Modeling Interaction in Ambient Assisted Living Environments. In: Panagiotis D. Bamidis, Nicolas Pallikarakis (Eds.) XII Mediterranean Conference on Medical and Biological Engineering and Computing , pp. 655-658. Springer, Berlin, Heidelberg.
40. Kitchenham, B. and Pfleeger, S.L. (2002) Principles of survey research. ACM SIGSOFT Softw. Eng. Notes , 27 , 17-20.
