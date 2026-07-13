[FIGURE]

## Advancing Toward a Reference Ontology for Enterprise Architecture Mining from APIs

Carlos Roberto Pinheiro 1,3( B ) , Sérgio Luís Guerreiro 2,3 , and Henrique São Mamede 4

1 Universidade de Trás-os-Montes e Alto Douro, Vila Real, Portugal

carlos.guti@gmail.com

2 Instituto Superior Técnico, University of Lisbon, Lisbon, Portugal

sergio.guerreiro@tecnico.ulisboa.pt

3 INESC-ID, Rua Alves Redol 9, 1000-029 Lisbon, Portugal

4 INESC TEC, Department of Science and Technology, Universidade Aberta, Lisbon, Portugal

Abstract. Enterprise Architecture (EA) is a coherent set of principles, methods, and models that express the structure and behavior of an enterprise and its IT landscape. EA mining uses data mining techniques to automate EA models' extraction. Ontologies help to define concepts and the relationships among these concepts to describe a domain of interest. This paper presents an extensible ontology for EA mining to extract models using Application Program Interface (API) log files as the data source. The ontology development follows the FAIR principles (Findability, Accessibility, Interoperability, and Reusability) and uses OntoUML 2.0 language to ensure its expressiveness and readability. To validate its theoretical feasibility and contribution to EA modeling, it presents a simulation of the ontology application through a controlled scenario using data structures similar to an industrial case. Then, the ontology is verified and validated, checking quality ontology criteria using specialized tools for syntactic and semantic model checking, which also aids in avoiding ontology anti-patterns.

Keywords: Enterprise architecture management · Enterprise architecture · mining · Automatic architecture modelling · Ontology · API

## 1 Introduction

Enterprise Architecture (EA) models represent viewpoints of different concerns of the company and its IT landscape, such as processes, services, and information systems [1]. It is essential to automate the EA modeling due to the harmful effects on organizations of decision-making based on outdated architecture models, as manual modeling is prone to errors and misunderstanding, besides being time-consuming [2]. Nevertheless, the low automation of EA model creation and maintenance is one of the most critical challenges for EA management [3].

An API Gateway is an architectural component that mediates calls between API and services. It allows the collaboration of different organizational actors across industrial boundaries [4, 5]. It is an effective data source for mining cross-organizational

©The Author(s), under exclusive license to Springer Nature Switzerland AG 2024 J. Filipe et al. (Eds.): ICEIS 2023, LNBIP 519, pp. 262-281, 2024. https://doi.org/10.1007/978-3-031-64755-0\_13

interactions, as it monitors the traffic on the company's boundary and its information systems.

An ontology typically describes concepts, relationships among these concepts, and constraints that indicate how to interpret these relationships. Thus, it provides a taxonomy that describes a domain of interest and specifies the meaning of terms [6, 7]. Ontologies are used in complex problems to separate essentials from implementation details.

This work is part of ongoing research that aims to apply Data Mining (DM) techniques to obtain automatically EA view models in ArchiMate [8]. Specifically, this paper advances from [9] by presenting a more robust ontology validation targeting to support the EA mining from logs of APIs. The previous work evaluated the ontology application by hypothesizing a scenario to demonstrate ontology feasibility. In contrast, in this sequence, the work concludes the validation steps prescribed by the SABiO (Systematic Approach for Building Ontologies) process [10] for reference ontologies, including the evaluation by an ontology specialist. In another significant improvement, the previous ontology proposal was built using the OLED (Onto UML Lightweight Editor), which provides a set of validators useful for the first ontology version [11]. However, it is based on OntoUML 1.0 and does not support OntoUML 2.0 so far. Thus, this work updates the ontology to the latest version of the OntoUML language, using Visual Paradigm 1 for modeling and OntoUML Plugin for Visual Paradigm 2 that also provides ontology model check validators for OntoUML 2.0 ontologies, capable of automatically checking the semantically-motivated rules to ensure the correctness of ontology conceptualization [12].

In the sequence, Sect. 2 describes the motivation of the research and the ontology development; Sect. 3 presents the research background; Sect. 4 describes the development methodology; Sect. 5 presents the proposed ontology and demonstrates its application; Sect. 6 presents the evaluation and validation of the ontology proposed, while Sect. 7 discusses the results, and Sect. 8 presents a conclusion and future works.

## 2 Motivation

Aprevious work of the ongoing research presented a literature review gathering the state of the art in EA mining models from application logs to automate the architecture modeling, which identified some challenges of EA modeling automation [13]. It reinforced that logs recorded by enterprise applications may serve as an essential source of knowledge. Combined with data mining techniques, it may promote these logs as an enabler for agile EAmodeling, reducing many manuals and time-consuming tasks in EAM modeling and supporting better decision-making for future architecture when providing information and visualizations of the current architectural condition. An API Management tool is an excellent place to mine cross-organizational interactions because it monitors all traffic on the company's boundary and its information systems by mediating service calls among different systems of an organization.

SomeAPIplatformshavebuilt-inmonitoringandanalytics tools that allow observing events related to individual API calls and tracking their processing. However, correlating different calls and chaining them to identify a process remains a significant challenge because each call differs entirely from the others. They have different data structures that can carry the same value and meaning, even with different attribute names, which causes a lack of direct correlation. Hence, clarifying the scope and objectives of the solution design is essential to conceptualize the solution to ensure the research's feasibility, reinforcing the need for an ontology.

[1 https://www.visual-paradigm.com/editions/community/.](https://www.visual-paradigm.com/editions/community/)

[2 https://github.com/OntoUML/ontouml-vp-plugin/.](https://github.com/OntoUML/ontouml-vp-plugin/)

Therefore, the problem investigated in this work is conceptualizing a consistent and extendable process for enterprise architecture model discovery using an API Log as the data source correlating different API calls. It aims to make the AS-IS architecture modeling more agile and automatized. For this, it requires developing an ontology to clarify and explain the process and drive the main concepts and the sequence of steps to build a concise solution design for the context under analysis. More specifically, this work targets to evaluate and validate the conceptual ontology proposed for the solution.

## 3 Research Background

As EA models expand, keeping them up to date becomes more challenging, and companies continuously redefine their business goals. It requires continuously reviewing and adapting their architecture [14].

EAMiningistheusageofDataMiningtechniquestogetupdatedviewsofEAmodels [3]. In this context, Pérez-Castillo et al. [2] developed a reverse engineering approach to generate AchiMate models based on static source code analysis of computer programs, database schema, and textual analysis. Simovi´ c et al. [15] presented an approach to extract business information from enterprise application logs based on a domain-specific language definition, however, without generating an EA model in ArchiMate from it. Antonello et al. [16] proposed a method for identifying functional dependencies in Complex Technical Infrastructures (CTI) by applying Association Rule Mining (ARM) with data collected using alarm messages from sensors and monitoring technologies, which allows detecting a local malfunction propagating through groups of dependent components. Alfonso-Robaina et al. [17] analyzed the main variables in terms of causes and effects to assess the impact of multifactorial elements that affects the EA using fuzzy relation logic. However, their method is based on knowledge obtained though expert interviews and translating information gathered into dependence rules.

Ontologies typically describe concepts and the relationships among them, providing constraints on how to interpret them [6]. One of the main advantages of using ontologies is to focus on what information is relevant to the domain, avoiding irrelevant information from the beginning of the domain's analysis [18]. OntoUML is a well-founded ontology language based on UML class diagram fragment that provides an ontologydriven conceptual modeling language for complex domains whose stereotypes reflect the top ontology UFO [19, 20]. In their study on using ontological-based representations of enterprise models, Sunkle et al. [21] suggest ontology representation facilitates EA analysis, mixing representation and inference functionalities that are also extensible for more detailed EA analyses.

Some studies use semantic web technologies such as RDF and OWL to represent reference models for EA. Jabloun et al. [22] developed an ontology for change management in enterprise information systems that identifies the relationships among system components by reducing semantic mismatch among them. Allemang et al. [23] proposed using RDF and OWL to distribute EA-structured information. They also implemented a web-based system for managing EA Reference Models based on ontology and their reference model. Silva et al. [24] proposed using ontology and computational inferences features of ontologies to analyze the EA model evolution specified in OWL-DL. The ontology reasoners are used for relation checking, consistency checking, dependency inferring, and completeness checking, which helps to analyze EA model changes under a specific IT project and its impact on enterprise transformation.

Some other studies focused on a more high-level ontological conceptualization of EA. Guédria et al. [22] proposed a set of concepts to identify critical aspects of interoperability and EA and their associations, resulting in a conceptual reference model for integrated enterprise architecture interoperability based on ArchiMate [8]. Hinkelmann et al. [25] used an ontology representation of EA in ArchiMate to link an enterprise ontology with operational databases distributed over several information systems that ensure continuous alignment of the information architecture to the business requirements. Hinkelmann et al. [26] developed an approach to identity dependencies among architectural models integrated through information from databases of different enterprise systems, such as enterprise resource planning (ERP), customer relationship management (CRM), document management system (DMS), and content management systems (CMS).

Kopp &amp; Orlovskyi [27] developed an approach for web mining to extract a model of enterprise architecture landscape from organizational websites. It is an EA mining approach focused on detecting business activities by mining hyperlinks in the enterprise webpage contents. It also uses NPL (Natural Language Processing) techniques to detect business activities and produces a human-readable enterprise architecture model of these business activities, contributing to the enterprise architectural landscape. Kang et al. [28] built a model that helps to define ontologically relevant business terms to the EA based on WordNet.

In this section, we presented works that support the conceptual ontology of mining data from API gateway logs. Other works demonstrate the applications of ontology to solve different aspects of Enterprise Architecture modeling. Despite some promising approaches, none of these works provided a specific and extendable ontology for extracting enterprise architecture models directly from enterprise APIs. Thus, developing an EAmining ontology based on API data will complement and enrich the EA management field.

## 4 Ontology Development Methodology

This work evolves a previously proposed conceptual ontology supporting data mining for API logs to extract enterprise architecture [9]. Specifically, this ontology allows building (i) business process viewpoints based on the API invocations sequence and (ii) an architectural view of the relationship of the data objects used through the API domains. For its development, OntoUML provided the ontology modeling language, modeled using Visual Paradigm Community Edition v17.1 with OntoUML Plugin for Visual Paradigm as a modeling tool. This tool set supports the theoretical reference for the Unified Foundational Ontology (UFO), the foundation ontology for OntoUML. It provides a model check validator to ensure the ontology rules and helps to detect errors and some frequent ontology anti-patterns [12]. Furthermore, as the proposed ontology targets building EA view models, the concepts are mapped to ArchiMate [8].

The ontology's development followed the systematic Approach to Building Ontologies (SABiO)[10], which prescribes a process to build ontologies at high level conceptual references, as well as ontologies at a more concrete and fully operational level. This process encompasses five steps: (i) Purpose Identification and Requirements Elicitation, (ii) Ontology Capture and Formalization, (iii) Design, (iv) Implementation, and (v) Testing. Thefirst two phases of the process focus on building a reference ontology, while the other three advance to operational ontologies. Thus, as this work aims to develop a reference ontology, it presents only the first three steps.

## 5 The Ontology for EA Mining from APIs

## 5.1 Purpose Identification

The ontology under development aims to extract data correlating different API calls to build views of the AS-IS EA model by mining data from API logs, namely, from a centralized log of API Gateways. It will help to automate the EA modeling of the AS-IS architecture and make it more reliable and faster.

## 5.2 Ontology Requirements

Functional requirements refer to the knowledge the ontology must represent and can be defined as questions that the ontology must be able to answer. It helps to determine what is relevant to the ontology and define its scope [10]. In this sense, this ontology should answer the following questions:

- What are the business partners that interact with APIs within a business process?
- What are the relations among different data objects of different APIs and their resources?
- Which APIs support a particular business process?

From another perspective, non-functional requirements refer to characteristics, qualities, and general aspects unrelated to the ontology content, such as understandability and extensibility [10]. As the ontology domain is complex, it is essential to modularize it because of its complexity and to improve its extensibility. Other modularization benefits of ontologies include facilitating the development and maintenance and the reuse of parts of the ontology. Thus, this ontology is divided into packages representing modules that are loosely coupled to the others and represent the building of a particular EA view. In addition, this work evolves the ontology to follow the FAIR principles (Findability, Accessibility, Interoperability, and Reusability) to facilitate its publication in the FAIR multi-domain catalog for Ontology-Driven Conceptual Modeling 3 and promote its reuse and extension to other cases. [29].

[3 https://github.com/OntoUML/ontouml-models.](https://github.com/OntoUML/ontouml-models)

## 5.3 Ontology Capture and Formalization

According to Falbo [10], reference domain ontologies must approximate the ideal ontology of the domain as well as possible, focusing on the representation adequacy of the resulting specifications targeting its use by humans. The ontology is divided into three packages to modularize and make it easier to understand. The first package is related to the core concepts of ontology. The other two packages are extensions that allow modeling a specific data mining process from the core concepts to build a specific architecture view: (i) the EA Process view and (ii) the EA Data Object Relation View. These views are presented in ArchiMate using the Application Usage viewpoint, which is a viewpoint in ArchiMate proper to describe the usage of the application by business processes and other applications [8].

The Core Package. The package Core is related to the core concepts of the ontology. It comprises the ontology concepts that should be extracted directly from API Log files and provide data that supports the rest of the ontology. Figure 1 below illustrates the core package of the ontology and its concepts.

Fig. 1. Ontology Core Package.

[FIGURE]

In the core of the ontology, the event API Call is the concept that represents and characterizes each API call as a structural conceptual event that occurs in a specific slice of time defined by a begin and end time that is affordance to reflect temporal properties for an ontological temporal structure [30]. The beginning and end of an event define its borders.

- request\_time : this timestamp field, stereotyped as ≪ begin ≫ , represents the exact moment an API request hits the API and marks the beginning of the API processing.

- response\_time : this timestamp field, stereotyped as ≪ end ≫ , represents the moment an API sends the response to the caller (Consumer App) of the API and marks the end of its processing.
- result\_status : the result of the API call indicating success or unsuccess return to the Consume App caller.
- Uri: (Uniform Resource Identifier): indicates the location and the resource exposed by each API, which is the internet address used to call the API.
- api\_name : is the API name.
- resource\_name : This is the name of the resource called.

TheAPIsarecalled by an authorized Consumer APP representing a Partner identified through the attribute client\_id, which makes HTTP requests to APIs, creating an event API Call.

An API Call has one or more API Operations, characterized by the URL route (endpoint\_route) and an HTTP method, such as GET, POST, PUT, and DELETE. This operation creates, changes, or deletes an API Resource. It also has one or more Service Destinations, the service called in the backend or other external or internal service provider, usually through REST APIs or SOAP Webservices. API Operation and Service Destination also extend the kind Service identified by its URL endpoint\_route. Thus, a Service may be an API Operation which is the API Calls from the Consumer App, or an API Service Destination, which are the backend services called by one API Operation on the API Gateway.

The kind API Resource represents the class of objects handled through the API. It represents entity data structures. An API Resource is associated with another API Resource if they share the same attribute name. The relator Operation Executed mediates an API Operation executed on an API Resource. In contrast, the relator Documented API relates the documentation of API that describes the API resource and its data schema. The address location of an API Resource documentation is the url recorded in the field doc\_location of the relator Documented API.

TheProcess View Package. Thepackage Process View extracts a view of the processes supported by the APIs. It represents the API Calls as process events, and it classifies each of them as an Antecedent Activity or Consequent Activity, creating a chain of activities by applying temporal data mining techniques to extract activity correlations from API Calls as a sequence of process events and then identifying processes and grouping these processes to build an EA Process View. Figure 2 shows the ontology package for mining a process view at the enterprise architecture level.

To extract the EA Process View, the relator Frequent Temporal Correlation represents the data mined that correlate two event specializations of API Calls in a temporal sequence, considering each API request as an atomic event and identifying in the sequence what event represents the Antecedent Activity and what is the Consequent Activity. The event API Activities Connection identifies and aggregates two candidate activities, considering the same Partner, the resource id present in URI, and other shared and repeated attribute values in the API Resource data. Partner is the role of a Consumer App interacting with the process. Thus, through temporal ARM, it should be possible to identify the sequence candidate and assign to each sequence a case id, identifying and building individual instances for each Process, which is a long-running event composed of an activities chain or API Activities Connections for which is given a process identification recorded in the case\_id attribute. The event Process groups the activities based on the first and last activities. Then, the relator Process View Element mediates the extraction of the EA Process View, which represents the group of processes at a high level built as a view based on the Application Usage viewpoint in ArchiMate with the processes mapped to Business Process into this view. It identifies the most frequent chain of events. It maps the events in this path to Business Event elements, linked by creating an ArchiMate Assignment Relationship between the Process and the Events.

Fig. 2. Process View Package.

[FIGURE]

The Data Relation View Package. The package Data Relation View aims to build the EA Data Relation View by applying association rules mining techniques to discover frequent relations on the API data payloads. Figure 3 depicts the concepts to extract a view of data entities among API Resources to build an ArchiMate view to present the relations among data structures mined from the API payloads. These data payloads are related to API Resources and the names and values of their attributes whenever they carry on an entity data structure. The relator API Domain Map links the API Resources to API Domains. The relator Frequent Data Domain Correlation represents frequent relations amongAPIdatapayloadsdiscoveredbyapplyingdataminingtechniquestoidentifyData Elements within the data structures of API payloads. It mediates the material relation between an API Entity and a Data Domain. The correlations of API resource structures are based on the repeated value of the attributes of the API calls identified by the kind of API Resource. The Correlated Data Objects kind groups the API Entities and Data Domains and provides the data to build the Data Objects Relation View to the enterprise model. This work considered the case of REST APIs with entity representational state in JSON format (Bray, 2017).

Fig. 3. Data Relations View.

[FIGURE]

The EA Data Object Relation View aims to show a map of data object relations grouped by Domains. For that, the kind Correlated Data Object identifies the piece of data that plays the role of Entity and the piece that identifies the Data Domain. The repeated attributes of API Resource identify the strength of the relation. Then, the entity\_name of the Correlated Data Object derives an application Data Object in ArchiMate, while the related domain\_name derives another ArchiMate Data Object, but this one aggregates the entities in the architectural view.

In this context, the role API Entity represents API REST resources, and the Data Domain represents a logical group identified through the base path name of the API, which is present in its route and its URI. In this case, it may be essential to clarify the concept of the Data Domain used in this ontology and differentiate it from the Web Domain, which is also part of the URI of API and Service routes. The last one is the web domain that allows a web resource to be recognized and reached from any computer on the Internet. The concept for this ontology is a logic group that creates a context of data usage. Thus, this context encompasses different entities based on the API route and its linked documentation, excluding the web domain until the part of URI that identifies the different resources an operation over API creates, modifies, and deletes. Once the entities are identified and grouped into a context (API Domain), the data object is correlated based on their dependency based on the frequency of its repeated values in its attributes.

## 5.4 Demonstration

This section exemplifies the applicability of the ontology proposed in this work to prove its logical feasibility and better understand how it will support the architecture view building covering the whole mining Process.

The example considers a simplified and hypothetical user-buying journey on an e-commerce site as a use case. Figure 4 shows this buying journey.

Fig. 4. Example of e-commerce buying process.

[FIGURE]

It starts with users searching for products. Once they identify the product, they put it in a shopping cart created when the user adds the first product. Then, users add and remove products from the cart and interact with the e-commerce application. Once satisfied, users check out the cart when the e-commerce system asks them to create an account or log in. Once logged, they pay, and after the payment is approved, the e-commerce system creates an order sent to the logistics sector for delivery. In the end, the logistics and the user confirm the product delivery and its reception by the user.

The log structures used in this example are based on Sensedia API Gateway, which has a good classification in the Forrest Wave Report API management tool 4 . The first API call occurs when the user adds the first product to the cart, creating the shopping cart. The key attributes identified in the log file are:

- clientId : identifies the Consumer App individuals.
- receivedOnDate : time that the call hits the API Gateway
- apiName : friendly name description of API
- responseOnDate : time that the API Gateway returned the processing result
- uri : the internet address of the API.
- resultStatus : the HTTP result of API processing with success or error.
- trace : a string recording some aspects of the API call. It carries its header and body payload.

An API Call should be one kind of Service, identified by its URL route: an API Operation, whichis the API Calls from the Consumer App, or an API Service Destination, which is the backend service called by one API Operation on the API Gateway identified by its endpoint\_route. It is possible to extract the API Operation Route and the Service Destination Route from the trace string, as depicted in the trace snippet below. The route is the API Operation Route, and the string after the (= &gt; ) identifies the Service Destination Route.

```
"Found matching route: apiplatform.sensedia.com/sandbox/ commerce/v1/carts/ = > https:/mock.pstmn.io/dev/mock/v1/carts".
```

Theoperation name in API Operation identifies the operation over an API to create or change a resource. The results identify the operation method corresponding to the HTTP method in the API Call, the api\_name, and the API Resource, including the resource data structure.

Because the called URLs carry the concrete identifiers of resource instances, making it hard to ensure the correct route extraction, it was necessary to check the description of the routes in the swagger. The swagger is a file that documents the APIs and describes some relevant attributes of the API. In the case of Sensedia's API Platform, its documentation is on the developer portal linked to the API Gateway. It is used to build the relator Documented API that identifies and links the API resource extracted by the data mining process to its documentation.

The EA Processes View Mining. This process is the sequential correlation mining extraction process that sequences API Calls to build a process visualization. For that, the Frequent Temporal Correlation sequences timely API Calls that share some attribute values and groups those with the same Consumer App. The repeated\_attributes represent repeated attribute names and their value, which, for each event, combines two API Calls, identifying the Antecedent Activity as the older and the Consequent Activity as the younger activity. Then, the weight of correlations is calculated based on the percentual measure of the attribute's repetition. Correlations with at least one attribute with 100% of the weight are considered a candidate for the aggregated event API Activities Connection.

[4 https://content.sensedia.com/en/sensedia-leader-forrester.](https://content.sensedia.com/en/sensedia-leader-forrester)

Presuming that at least one attribute must be present in 100% in the correlations among its instances to be part of the same Process.

Then, a graph is created, extracting the sequence of process events considering that a Consequent Activity of a Process in an API Activity Connection is an Antecedent Activity in the following connection in the same Process. In the end, each graph is a process instance assigned to a process case\_id. As the interest of this work lies in an enterprise architecture view of the Process and not in process details, it simply relates the Process Instances to the EA Process View that considers the similarity of graphs regarding its first and last node (API Activity Connection). It considers the variations path between these two nodes as internal variations of the same Process due to the high level of EA.

The resulting model of the example is used to build an ArchiMate Business Process Cooperation viewpoint. Despite some differences in the sequences and do not correspond precisely to the same graph, all paths will start with the creation of the cart and finish with the final update of order status with the sequence depicted in Fig. 5.

Fig. 5. ArchiMate Process View (from [9]).

[FIGURE]

The Data Relations View Mining. It demonstrates the application of the Data Mining Technique to identify frequent associations among data structures composed of Data Elements. These Data elements may be Data Domains or Entities. From this perspective, the Data Domain is the API Name, identified by the apiName attribute from the API Call. Theentities grouped into a Data Domain are API Resources with repeated value attributes between their data structures from API Calls. It uses the API Resource repeated attributes to assess the association's strength. Only associations with very high confidence, close to 100%, should stay present in the aggregation 'Correlated Data Objects' from what it is possible to build a visualization of Entity relations for each Data Domain, such as the ArchiMate viewpoint of the buying process example illustrated in Fig. 6.

Fig. 6. ArchiMate Data Relations View (from [9]).

[FIGURE]

## 6 Evaluation and Verification

## 6.1 Evaluation Process

The evaluation process presented is based on SABiO [10], which prescribes evaluation from two main perspectives: (i) ontology verification and (ii) ontology validation. Ontology verification ensures that the ontology is being built correctly, while ontology validation aims to ensure that the ontology fulfills its specific intended purpose of use. According to [10], the participation of domain experts, ontology experts, and ontology users is essential in ontology validation. Most of the verification for this ontology is done through automated tools provided by the OntoUML Plugin for Visual Paradigm. On the other hand, for ontology validation, an instantiation demonstration is produced from simulated real-world situations. Therefore, the evaluation is automated and conducted through collaboration of ontology experts and enterprise architects.

The previous work hypothesized a case to evaluate the ontology application to a near-real scenario. However, some steps and roles were not applied due to the lack of specialized roles prescribed by the SABiO approach. This new work fulfills this gap through the collaboration of an ontology expert to ensure the most accurate use of the OntoUML concepts.

## 6.2 Evaluation Roles

SABiO prescribes some roles in the process of ontology building: (i) domain expert, who is a specialist in the domain of the ontology and provides the knowledge that is modeled and implemented in the domain ontology; (ii) ontology user, representing someone who intends to use the ontology for a given purpose; (iii) ontology engineer, who is responsible for the reference ontology, and thus is responsible for the initial phases of the ontology development process; (iv) ontology designer, who is responsible for the design of an operational ontology; (v) ontology programmer, who is responsible for implementing an operational ontology; (vi) ontology tester, who is responsible for testing an operational ontology [10].

The ontology used the following roles for human assessment, grouped in a new super role called ontology evaluators, which is supposed to be consulted along with the ontology development process.

- Ontology Expert : a recognized expert in ontology theory and design.
- Domain Expert : which was mapped to those who have a background in Integration Architects, API Specialists, and Enterprise Architects
- Ontology user : Enterprise Architects
- Ontology Tester : For this case, it considers the domain expert and ontology users for logical tests.

## 6.3 Evaluation Material

The ontology evaluation material is the ontology model and the demonstration explained in the previous section.

## 6.4 Evaluation Criteria

Table 1 summarizes the evaluation criteria used to validate the quality aspects of the proposed ontology.

Table 1. Summary of evaluation criteria of the ontology and how.

| Criteria           | Description                                                                                                                                                   |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Competency Fitness | Refers to how much the ontology attends to the functional requirements of the stakeholders                                                                    |
| Expressiveness     | Assesses whether the ontology detail is accurate, efficient, and appropriate models the domain for its intended use                                           |
| Coherence          | Apply ontology cleaning practices to remove syntactic errors                                                                                                  |
| Consistency        | Apply ontology cleaning practices to remove semantic errors                                                                                                   |
| Completeness       | Verify that there are no missing concepts to its purpose                                                                                                      |
| Adaptability       | Refers to how well the ontology anticipates its future uses                                                                                                   |
| Expandability      | Assesses how easy it is to add new definitions and information to an existing definition without altering the set of well-defined properties already provided |

Fitness/Competency. Oneofthe first steps in ontology evaluation is checking its fitness for a given task and a specific domain [31]. The fitness of the ontology refers to how much the ontology attends to the stakeholders' functional requirements. It should be driven and validated through competency questions. Competency Questions (CQ) identify the ontology purpose and its intended uses, which define the ontology scope and provide a way for its validation [10]. In this sense, the demonstration of the hypothetical aid to assessing fitness by answering the three competency questions below. It demonstrates that the ontology communicates the intended meaning.

- CQ1-Does it identify business partners that interact with APIs?
- CQ3-Does it map the relations among different data objects of different APIs?
- CQ2-Does it map the business processes supported by APIs?

The experiment proved the ability of the ontology to answer these questions.

Expressiveness (EX). A domain ontology evaluation should assess whether the ontology accurately, efficiently, and appropriately expresses and models the domain for its intended use. In this sense, the evaluation of the ontology expressiveness is based on two perspectives. First, using a formal ontology language such as OntoUML aims to ensure its expressiveness in terms of concepts and relations representations that other ontology builders could easily understand. Second, the final objective of the ontology is supporting the building of EA views. In this sense, the two questions below were tested.

- EX1-Howwelldoesthe ontology communicate the purpose and intended meanings?
- EX 2- The level of the ontology detail is enough to express all concepts necessary for the purpose.

The result of the experiment demonstrates that the ontology supports its purpose and intended meaning, and the result expressed in ArchiMate demonstrated that all details are enough to generate the proposed views.

Coherence and Consistency (CC). Another critical step in ontology evaluation is to apply ontology cleaning practices to remove errors. In this sense, McDaniel &amp; Storey [32] discuss two types of errors to be checked in an ontology design: syntax errors and semantic errors. They suggest using different criteria in the ontology for syntax errors, such as checking missing inverse relationships and using a recursive definition. In contrast, for semantic errors, they described merging different concepts in the same class, checking missing equivalent properties and missing disjointness relationships, creating synonyms as new classes, and swapping intersection and union. This evaluation considers the ontology's coherence with no syntactic errors and consistency with the ontology without semantic errors. For that validation, an automatized process used the verification of OntoUML Plugin for Visual Paradigm, syntactical verification, model checking, detection and correction, and validation of parthood relations and ontology patterns [12].

Completeness (CP). From the perspective of this criteria, the ontology is complete if there are no missing concepts to its purpose. According to McDaniel &amp; Storey [32] it refers to when all that is supposed to be in the ontology is explicitly set out in it or can be inferred using other definitions and axioms. This ontology completeness was evaluated through two methods. Firstly, the OntoUML plugin for Visual Paradigm provided a validator model completeness through its Check Diagram and Check Model features. Secondly, the experiment demonstrates how completely the ontology covers enough concepts to build all the proposed architectural views: Process View and Data Objects Relation View, which are generated in ArchiMate.

Adaptability and Expandability (AE). Adaptability refers to how well the ontology anticipates its future uses. Expandability refers to how easy it is to add new definitions and information to an existing definition without altering the set of well-defined properties already guaranteed. Both points are related to the level of modularity of the ontology, which divides the ontology into smaller and self-contained modules, facilitating its understanding, application, reuse, evolution, and extension [32]. To ensure the ontology's adaptability and expandability, the ontology design evolved to follow the FAIR principles [29]. Following these principles improves ontology findability, accessibility, interoperability, and reusability.

## 7 Discussion

This proposal focuses on conceptualizing an EA mining extraction from a particular technology, the API log files. It substantially differs from other existing approaches that use different data sources, such as enterprise application source codes [2], enterprise website contents [27], and operational databases [25]. Thus, it will complement the EA landscape automation for AS-IS modeling. The API log is obtained from an API Gateway. Even though many companies may also have been not using an API Gateway, restricting the application of this study, API gateway logs are vital to complement the EA mining field once they provide a kind of service facade for the information systems of an organization and its partners, capturing and recording some behaviors and data structures at the enterprise level that may not be present in operational databases. This approach and focus have yet to be found in the literature. In addition, in recent years, the use of API gateways has undergone a considerable increase.

The ability to trace a unique API request through a network and correlate it with the triggered components is not new. The novelty of our proposed ontology is the ability to correlate different requests that initially have no physical correlations but share logical contexts relevant to understanding the EA.

Theextracted business process view allows an overlook of API relations with the execution of the main tasks of a business process. Another view allows data objects related to APIs and processes, which helps to identify the relationship between data entities and their usage through enterprise APIs and their related process. All these extracted views aim to contribute to the overall architecture. Despite having some limitations regarding building a complete EA, such as the business architecture, it will contribute with complementary views to accelerate the architecture analysis and modeling.

For this ontology, attributes with repeated values between the data structures of API calls are used to give weight to the relationship between process activities and to associate data objects. Based on this data, it is possible to apply other process mining techniques to help discover distinct aspects and patterns related to business processes. Another way to extend this ontology is through further analysis of this data to verify the cohesion of the data domains related to the name of the attributes between the data objects.

Regarding the previous version's improvements, this ontology separates the concepts in packages with well-defined borders. The benefits of ontology modularization include: (i) facilitates its development and maintenance due to its self-contained and loosely coupled modules; (ii) facilitates the reuse of parts of the ontology; (iii) improves performance by enabling distributed processing [10]. Another evolution was the migration from OntoUML 1.0 to OntoUML 2.0, increasing its expressiveness by incorporating new classes and relationship stereotypes, such as the class Event. For that, the ontology was redesigned using the OntoUML Plugin for Visual Paradigm because the tool used beforehand does not support OntoUML 2.0 yet. In this redesign, the ontology also evolved to follow the FAIR principles [29] to ensure desired characteristics, such as findability, accessibility, interoperability, and reusability.

Another significant advance, in additionally to having its consistency and quality checked by automatic tools, the ontology also underwent a more solid and well-defined process, prescribed by Falbo [10], where questionnaires were applied through interviews to verify quality criteria and competence questions to evaluate the ontology regarding its purpose of extracting the proposed architectural views from API logs.

The proposal's threat so far is that despite presenting a specific domain ontology, this ontology is still a high conceptual reference model. Although it is possible to map the OntoUML models in Visual Paradigm to other more operational languages for ontology instantiation, the high level of detail, given the objectives of this work to design a reference ontology, may reduce the expressiveness of the ontology when applied to a more operational language, such as OWL and RDF, requiring adaptation of the derived models.

## 8 Conclusion and Future Work

This research aims to build a DM model to automate the extraction of the current EA views. For that, the ontology presented in this paper is focused on conceptualizing the process of building EA mining from API interactions rather than its technical implementation, which will be a matter of future development, including the possibility of its derivation to a fully operational ontology.

Theapplication of the ontology is an adequate approach for automating the capture of an EA model evolution, which leverages the tracking of change in the current EA model and provides views to aid the impact analysis of planning changes in enterprise APIs, and, finally, for monitoring the effects of the architectural change's implementation, contributing to an agile EA management. Its feasibility was evaluated and demonstrated through an exemplification using synthetic data similar to an industrial case.

This paper follows the process prescribed by SABiO for reference ontologies, which included the evaluation of quality criteria by experts in ontology and by enterprise architects, raising confidence in the ontology's correctness and fitness to its purpose based on competency questions, its expressiveness, coherence, consistency, completeness, adaptability, and expandability.

Anexperiment demonstrated the ontology application to extract and correlate data to build architectural views, namely Processes and Data Relations. The data provided for the exemplification of ontology application was obtained from a simulated process in only one API Gateway, which still implies a challenge to solve in future work to generalize it and test it in a real case. The simulation matches the semantics and attributes in an actual API gateway log file. In future work, this reference ontology will be instantiated in an operational ontology and applied in an actual case experiment. Furthermore, the best data mining techniques to build each architectural view proposed still must be analyzed.

Acknowledgment. Weare especially grateful for the collaboration of Pedro Paulo Favato Barcelos, a researcher at the Semantics, Cybersecurity, and Services Group of the University of Twente, playing as an ontology expert in revision of the proposed ontology with direct implications in the quality of the ontology in terms of its expressiveness and the best use of UFO and OntoUML concepts.

This work was supported by national funds through Fundação para a Ciência e a Tecnologia (FCT) with reference UIDB/50021/2020 (INESC-ID).

## References

1. [The Open Group: The TOGAF® Standard, Version 9.2. 2018. https://pubs.opengroup.org/ architecture/togaf9-doc/arch/index.html](https://pubs.opengroup.org/architecture/togaf9-doc/arch/index.html)
2. Pérez-Castillo, R., Caivano, D., Ruiz, F., Piattini, M.: ArchiRev-reverse engineering of information systems toward ArchiMate models. An industrial case study. J. Softw. Evol. Process 33 (2), e2314 (2021). https://doi.org/10.1002/smr.2314
3. [Perez-Castillo, R., Ruiz-Gonzalez, F., Genero, M., Piattini, M.: A systematic mapping study on enterprise architecture mining. Enterp. Inf. Syst. 13 (5), 675-718 (2019). https://doi.org/ 10.1080/17517575.2019.1590859](https://doi.org/10.1080/17517575.2019.1590859)
4. [Bonina, C., Koskinen, K., Eaton, B., Gawer, A.: Digital platforms for development: foundations and research agenda. Inf. Syst. J. 31 (6), 869-902 (2021). https://doi.org/10.1111/isj. 12326](https://doi.org/10.1111/isj.12326)
5. Herterich, M.M., Dremel, C., Wulf, J., vom Brocke, J.: The emergence of smart service ecosystems-the role of socio-technical antecedents and affordances. Inf. Syst. J. 33 , 524-566 (2022). https://doi.org/10.1111/isj.12412
6. [Shvaiko, P., Euzenat, J.: Ten challenges for ontology matching. In: Meersman, R., Tari, Z. (eds.) OTM 2008. LNCS, vol. 5332, pp. 1164-1182. Springer, Heidelberg (2008). https://doi. org/10.1007/978-3-540-88873-4\_18](https://doi.org/10.1007/978-3-540-88873-4_18)
7. [Trojahn, C., Vieira, R., Schmidt, D., Pease, A., Guizzardi, G.: Foundational ontologies meet ontology matching: a survey. Semant. Web 13 (4), 685-704 (2022). https://doi.org/10.3233/ SW-210447](https://doi.org/10.3233/SW-210447)
8. [The Open Group: ArchiMate® 3.1 Specification. https://pubs.opengroup.org/architecture/arc himate3-doc/. Accessed 15 Apr 2022](https://pubs.opengroup.org/architecture/archimate3-doc/)
9. Pinheiro, C., Guerreiro, S., Mamede, H.: Towards an ontology to enforce enterprise architecture mining. Presented at the 25th International Conference on Enterprise Information Systems, October 2023, pp. 660-668 (2023). https://www.scitepress.org/PublicationsDetail. aspx?ID=fc3DK2dsnQ0=&amp;t=1. Accessed 08 Oct 2023
10. de A. Falbo, R.: SABiO: systematic approach for building ontologies. Onto. Com/odise@ Fois (2014)
11. Guerson,J., Sales, T.P., Guizzardi, G., Almeida, J.P.A.: OntoUML lightweight editor: a modelbased environment to build, evaluate and implement reference ontologies. In: 2015 IEEE 19th International Enterprise Distributed Object Computing Workshop, September 2015, pp. 144-147 (2015). https://doi.org/10.1109/EDOCW.2015.17
12. Fonseca, C.M., Guizzardi, G., João, P.A., Almeida, T.P., Sales, D.P.: Incorporating types of types in ontology-driven conceptual modeling. In: Ralyté, J., Chakravarthy, S., Mohania, M., Jeusfeld, M.A., Karlapalem, K. (eds.) Conceptual Modeling: 41st International Conference, ER 2022, Hyderabad, India, October 17-20, 2022, Proceedings, pp. 18-34. Springer International Publishing, Cham (2022). https://doi.org/10.1007/978-3-031-17995-2\_2

13. Pinheiro, C.R., Guerreiro, S., Mamede, H.S.: Automation of enterprise architecture discovery based on event mining from API gateway logs: state of the art. In: 2021 IEEE 23rd Conference onBusinessInformatics (CBI), September 2021, pp. 117-124 (2021). https://doi.org/10.1109/ CBI52690.2021.10062
14. [Farwick, M., Schweda, C.M., Breu, R., Hanschke, I.: A situational method for semi-automated enterprise architecture documentation. Softw. Syst. Model. 15 (2), 397-426 (2016). https:// doi.org/10.1007/s10270-014-0407-3](https://doi.org/10.1007/s10270-014-0407-3)
15. Simovi´ c, A.P., Babarogi´ c, S., Panteli´ c, O.: A domain-specific language for supporting event log extraction from ERP systems. In: 2018 7th International Conference on Computers Communications and Control (ICCCC), May 2018, pp. 12-16 (2018). https://doi.org/10.1109/ ICCCC.2018.8390430
16. Antonello, F., Baraldi, P., Shokry, A., Zio, E., Gentile, U., Serio, L.: Association rules extraction for the identification of functional dependencies in complex technical infrastructures. Reliab. Eng. Syst. Saf. 209 , 107305 (2021). https://doi.org/10.1016/j.ress.2020.107305
17. Alfonso-Robaina, D., Díaz-Moreno, J.C., Malleuve-Martınez, A., Medina-Moreno, J., RubioManzano, C.: Modeling enterprise architecture and strategic management from fuzzy decision rules. In: Kóczy, L.T., Medina-Moreno, J., Ramírez-Poussa, E., Šostak, A. (eds.) Computational Intelligence and Mathematics for Tackling Complex Problems. SCI, vol. 819, pp. 139-147. Springer, Cham (2020). https://doi.org/10.1007/978-3-030-16024-1\_18
18. Branquinho, L.P., Almeida, M.B., Baracho, R.M.A.: Ontologies in support of data mining based on associated rules: a case study in a diagnostic medicine company. CEUR Workshop Proc. 1442 , 6 (2015)
19. Guizzardi, G., Wagner, G., Almeida, J.P.A., Guizzardi, R.S.S.: Towards ontological foundations for conceptual modeling: the unified foundational ontology (UFO) story. AO 10 (3-4), 259-271 (2015). https://doi.org/10.3233/AO-150157
20. [Guizzardi, G., Botti Benevides, A., Fonseca, C.M., Porello, D., Almeida, J.P.A., Prince Sales, T.: UFO: unified foundational ontology. AO 17 (1), 167-210 (2022). https://doi.org/10.3233/ AO-210256](https://doi.org/10.3233/AO-210256)
21. Sunkle, S., Kulkarni, V., Roychoudhury, S.: Analyzing enterprise models using enterprise architecture-based ontology. In: Moreira, A., Schätz, B., Gray, J., Vallecillo, A., Clarke, P. (eds.) MODELS 2013. LNCS, vol. 8107, pp. 622-638. Springer, Heidelberg (2013). https:// doi.org/10.1007/978-3-642-41533-3\_38
22. Jabloun, M., Sayeb, Y., Ben Ghezala, H.: Enterprise ontology oriented competence: a support for enterprise architecture. In: 2013 3rd International Symposium ISKO-Maghreb, November 2013, pp. 1-8 (2013). https://doi.org/10.1109/ISKO-Maghreb.2013.6728115
23. Allemang, D., Polikoff, I., Hodgson, R.: Enterprise architecture reference modeling in OWL/RDF. In: Gil, Y., Motta, E., Benjamins, V.R., Musen, M.A. (eds.) ISWC 2005. LNCS, vol. 3729, pp. 844-857. Springer, Heidelberg (2005). https://doi.org/10.1007/11574620\_60
24. Silva, N., Mira da Silva, M., de Sousa, P.M.M.V.A.: Modelling the evolution of enterprise architectures using ontologies. In: 2017 IEEE 19th Conference on Business Informatics (CBI), July 2017, pp. 79-88 (2017). https://doi.org/10.1109/CBI.2017.17
25. Hinkelmann, K., Maise, M., Thönssen, B.: Connecting enterprise architecture and information objects using an enterprise ontology. In: Proceedings of the First International Conference on Enterprise Systems: ES 2013, November 2013, pp. 1-11 (2013). https://doi.org/10.1109/ES. 2013.6690088
26. Hinkelmann, K., Merelli, E., Thönssen, B.: The role of content and context in enterprise repositories. Framework 18 , 10 (2010)
27. Kopp, A., Orlovskyi, D.: Towards the enterprise architecture web mining approach and software tool (2022)
28. Kang, D., Lee, J., Choi, S., Kim, K.: An ontology-based enterprise architecture. Expert Syst. Appl. 37 (2), 1456-1464 (2010). https://doi.org/10.1016/j.eswa.2009.06.073

29. Barcelos, P.P.F., et al.: A FAIR model catalog for ontology-driven conceptual modeling research. In: Ralyté, J., Chakravarthy, S., Mohania, M., Jeusfeld, M.A., Karlapalem, K. (eds.) Conceptual Modeling. ER 2022. LNCS, vol. 13607, pp. 3-17. Springer, Cham (2022). https:// doi.org/10.1007/978-3-031-17995-2\_1
30. Almeida, J.P.A., Falbo, R.A., Guizzardi, G.: Events as entities in ontology-driven conceptual modeling. In: Laender, A.H.F., Pernici, B., Lim, E.-P., de Oliveira, J.P.M. (eds.) ER 2019. LNCS, vol. 11788, pp. 469-483. Springer, Cham (2019). https://doi.org/10.1007/978-3-03033223-5\_39
31. Tatarintseva, O., Ermolayev, V., Keller, B., Matzke, W.-E.: Quantifying ontology fitness in ontoelect using saturationand vote-based metrics. In: Ermolayev, V., Mayr, H.C., Nikitchenko, M., Spivakovsky, A., Zholtkevych, G. (eds.) ICTERI 2013. CCIS, vol. 412, pp. 136-162. Springer, Cham (2013). https://doi.org/10.1007/978-3-319-03998-5\_8
32. McDaniel, M., Storey, V.C.: Evaluating domain ontologies: clarification, classification, and challenges. ACM Comput. Surv. 52 (4), 1-44 (2020). https://doi.org/10.1145/3329124
