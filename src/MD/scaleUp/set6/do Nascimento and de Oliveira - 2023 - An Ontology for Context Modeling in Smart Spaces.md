[FIGURE]

## An Ontology for Context Modeling in Smart Spaces

B

de Oliveira

Leonardo Vianna do Nascimento 1,2( ) and Jos´ e Palazzo Moreira 1

[FIGURE]

[FIGURE]

- 1 Informatics Institute, Federal University of RS, Porto Alegre, Brazil palazzo@inf.ufrgs.br

2 Federal Institute of Education, Science and Technology of Rio Grande do Sul (IFRS), Campus Alvorada, Porto Alegre, Brazil

leonardo.nascimento@alvorada.ifrs.edu.br

Abstract. Smart environments are one of the hot topics in the recent scientific literature in computer science. An essential aspect of these applications is how to obtain data about their users and understand them. Context-aware approaches proved to be successful in understanding these data. Therefore, user context representation is one of the problems to address in this domain. Context information can contain multidimensional information. This paper presents an ontology for representing context in smart environments called SpaceCOn. This ontology contains a definition of several context-related concepts. This ontology can be a strategic tool to integrate context data from different sources in large smart environments, such as smart universities and cities. Tests carried out in a case study demonstrated the developed ontology's potential.

Keywords: Ontology · Context modeling · Smart spaces · IoT

## 1 Introduction

Ubiquitous computing defines that computing must be present in environments to assist the user in performing their daily tasks efficiently. For this to happen, systems considered ubiquitous must be context-aware. They must adapt their behavior to the contexts obtained from the environment. One of the recent topics in ubiquitous computing deals with the definition and construction of smart environments using technologies, methodologies, and models adapted to ubiquitous computing.

In smart environments, systems may acquire and apply contextual data to improve users' experience [16]. Context-Awareness (CA) is a research area directly related to ubiquitous computing. The information exchange between systems is an important issue when dealing with context-aware systems. Is contextual information shared between systems in a representation pattern understandable to all concerned agents? For instance, a middleware present in a smartphone can provide information about its user's activities to the recommendation and monitoring applications. Therefore, it is necessary to have some standard for exchanging context information between such applications.

In this context, the concept of ontology stands out. An ontology defines a common vocabulary within a specific domain. It includes a set of semantic definitions that are interpretable by computer programs where the concepts of a domain and the relationships among them are defined [19].

This paper aims to present an ontology called SpaceCOn that allows semantically representing context information in smart environments. This research is part of a project to develop an architecture for context integration in smart cities. The ontology evaluation used a case study based on a scenario previously described in the literature.

The remainder of this article is organized as follows. Section 2 presents some essential concepts related to context and used in constructing the ontology. Section 3 presents the formal definition of context used in this work. Section 4 presents the analysis of some related works found in the literature. Section 5 contains the presentation of the proposed ontology. A case study is presented in Sect. 6 to evaluate the ontology and demonstrate its potential. Section 7 presents an overview of the architecture that uses SpaceCOn to integrate context sources in smart cities. Finally, Sect. 8 concludes the article.

## 2 Background

Context is an object of study for researchers in different areas of computer science. Each of these areas presents a different view on the definition of context. The term conceptualization varies when considering its application in different domains [6]. The most used definition in the scientific literature is the one presented by [1], where context is 'any information useful to characterize the situation of an entity (a person, object or place) that can affect the interaction between users and systems.'

Thus, context exists only when related to another entity and contains a set of items (concepts, rules, propositions) associated with such entity. Such items can be part of the context of an entity only if they help solve the addressed problem. Such items are called contextual elements . A contextual element is 'any piece of data or information that allows characterizing an entity in a given domain' [24].

A system is context-aware when it uses context to provide relevant information or services to its users [1]. An example of a context-aware system is a smartphone application that recommends restaurants to its user based on location and locomotion mode (walking, driving, on a bus). The location and locomotion mode information characterize the entity 'user', and the application uses them to provide recommendations. Thus, the location and locomotion mode are contextual elements that compose the user context.

## 2.1 Context Categorization

It is common to classify context information according to specific categories or types. Categorizing context allows computer application designers to more easily identify which contextual elements will be useful in their applications. The work of [27] presents an interesting classification for such schemes into two types:

- -Operational Categorization , whose objective is to categorize context information based on how it was acquired, modeled, and treated.
- -Conceptual Categorization , where context information is categorized based on meaning and conceptual relationships.

An example of an operational categorization scheme can be found in [20]. This scheme uses two categories to classify context:

- -Primary Context : any information obtained without using other existing context information or applying data merging operations. Examples: latitude obtained from a GPS receptor, an acceleration value obtained from an accelerometer.
- -Secondary Context : any context information computed from primary context information. Information of this type includes that obtained through data fusion operations, inference, or database query operations.

The work in [7] presents another operational categorization scheme classified into three levels:

- -Low Level : data collected directly from environmental sensors.
- -Intermediate Level : context information with a higher level of abstraction obtained from inference and aggregation of another context. Examples of intermediate context include activities (such as running or walking), derived from low-level acceleration data, and places like 'at home' or restaurants, derived from geographic coordinates.
- -High Level : context information is aggregated with semantic relations to relate it to other information, such as time and location.

Several works propose different conceptual categorization schemes [1,25,28]. The work in [18] describes a new conceptual categorization scheme combining elements already presented in previous proposals. The scheme defines six categories: individual (that includes anything observed about an entity, including user preferences and user identification), location, time (information that specifies when some action takes place), activity (refers to tasks performed by entities), relational (corresponds to social relationships that arise from the circumstances that they are involved), the context of interest (that describes the information about things around an entity, such as objects, sounds, weather, and temperature, that may interest it at a specific moment).

It is challenging to devise an ideal context categorization scheme. Combining different categorization schemes can complement their strengths and mitigate their weaknesses [20]. For example, a geographic position by latitude and longitude coordinates obtained from a GPS reader can be classified as a low-level primary context corresponding to the location of an entity. Another example is the action performed by a person (walking, standing, lying down, running) obtained from an inference engine that uses data from different sensors as input. In this case, the information obtained can be categorized as activity and intermediatelevel secondary context. Thus, in this work, categories specified in complementary schemes are expected to categorize each contextual element instance.

## 2.2 Quality of Context

Approaches to context management must deal with situations where the data obtained must be more accurate. Sensor data are subject to imperfection, given their technical limitations, availability, and possible malfunctions [3]. Furthermore, intermediate or high-level context inference mechanisms may present a greater or lesser degree of precision and accuracy. Furthermore, these mechanisms are trained using a subset of possible contexts and are not adapted to deal with all types of situations that may occur.

Inaccurate context information can lead an application to fail to meet its functional and non-functional requirements. Serious problems can occur due to wrong decisions made according to incorrect context information provided by a system.

Considering this scenario, mechanisms of quality assurance in context information must be used by applications in order to minimize the impact of inaccuracy in the data. As a result, the concept of Quality of Context ( QoC - Quality of Context ) was proposed in order to measure the quality of any contextual information. A more comprehensive and precise definition of the term is given in [14], where QoC indicates the degree of compliance of the collected/inferred context with the prevailing situation in the environment and the requirements of a particular context consumer .

Some QoC metrics have already been proposed in the literature [3,14]. There are two basic types of metrics: objective parameters (which are independent of the requirements of the context-consuming application) and subjective parameters (dependent on non-functional requirements of the application). Some examples of QoC parameters are Reliability, Timeliness, and Accuracy.

## 2.3 Context History

Some applications need not only the current context of an entity but also past context information. Historical context data are interesting in identifying trends and predicting future context-related values. Examples of applications that use context history include [5,23], and [15].

Some issues arise when manipulating [11] context histories:

- -Storage. A fundamental point for handling a context history is the possibility of storing such information.
- -Reading. Should data be obtained from contextual sources even when no consumers are interested? Future applications may be interested in this information that is currently not needed. How to reconcile these accesses with issues such as saving energy and resources? Thus, defining when context information will be read and stored is important for historical context data management.

- -Granularity. Ideally, the context storage should consider storing this information at the finest possible degree of granularity to fulfill any future requests for context information. However, other issues arise related to this, such as the depletion of storage spaces. Therefore, defining the level of granularity of the stored context information is also extremely relevant.

## 3 Formal Context Definition Used in This Work

Based on the concepts presented in the previous section, each contextual element instantiated is considered a tuple γ , defined as:

<!-- formula-not-decoded -->

where e is the contextual element associated with the instance, v is the value of this contextual element, Q is a set of QoC values associated with the instance, t is its creation time, and C is a set of context categories associated with the instance.

Each contextual element e is a tuple:

<!-- formula-not-decoded -->

where β is the entity characterized by the contextual element and α corresponds to the aspect of the entity related to the contextual element. Examples of aspects would be acceleration, the latitude of a geographic location, and the ambient temperature. As examples, one could define a contextual element ( PersonA,Latitude ), corresponding to the latitude of the geographical position of PersonA . Another contextual element could be ( HappyCity,Temperature ), representing the temperature in the city of HappyCity.

Each element in the set of Q quality values, in turn, can be defined as a q tuple:

<!-- formula-not-decoded -->

where p is any QoC parameter and v is the associated value.

In this way, defining examples of contextual element instances is possible. For example, an instance that defines the value Walking for the Activity aspect of the person PersonA obtained at the instant of time t 1 , could be defined as:

<!-- formula-not-decoded -->

where it is possible to see the definition of a QoC value (0.89 for accuracy) and the Secondary context category(the context is of the secondary type, obtained from other contexts, as defined in Sect. 2.1).

Entities, aspects, contextual elements, categories, and QoC parameters represent terms whose semantics need to be clearly defined so that agents in a smart space can exchange information based on a common vocabulary. For that, a high-level ontology is necessary to define more generic terms of the model any application domain shares. Applications can extend such an ontology to define specific terms and individuals of a domain. For instance, a domain can define specific context categories, entities, and aspects.

Thus, the ontology should:

- -be able to represent the concepts defined in this section;
- -be generic enough to allow its extension to different domains within smart spaces;
- -enable the modeling of different types of possible entities and aspects in smart spaces;
- -make it possible to associate different categories with contextual information.

## 4 Related Works

The first step in this work was the analysis of existing high-level ontologies for context representation. A review of the existing scientific literature identified some of these ontologies. See below a brief presentation of each one.

The ontology CONtext ONtology (CONON) models contextual information from four basic concepts related to computational entities, location, people, and activities [29]. Therefore, despite defining high-level concepts related to context, the CONON ontology limits the representation of such information to the categories of location, activity, individual, and representation of the context of computational interest. In addition, it is not possible to relate temporal information with modeled context.

The ontology CoBrA-ONT ( Context Broker Architecture Ontology ) was developed to define terms used in agent communication, where a multi-agent architecture manages context information [9]. However, the high-level concepts are limited to location, individual, and activity categories. Several terms defined in this ontology are related to meeting room applications that limit the possibilities of environments and context models.

The ontology CoOL ( Context Ontology Language ) models context at three levels: look , scale , and context information [26]. The ontology's main domain is a distributed system for discovering and executing services on the Web, but it is possible to adapt its concepts in other domains.

SOUPA ( Standard Ontology for Ubiquitous and Pervasive Applications ) was designed to support pervasive applications [10]. It consists of two ontologies: SOUPA Core (generic vocabulary common to different applications) and SOUPA Extension (support for different application domains). The Core ontology defines groups of concepts that describe people, agents, actions, security and privacy policies, time, space, and events. Although SOUPA has a set of several concepts for context modeling in multi-agent applications, it cannot represent entities that are not people, places, or agents (such as physical or virtual objects, for example) and the context of interest.

The ontology used in the CoDAMoS project ( Context-Driven Adaptation of Mobile Services presents four main high-level concepts: user, environment, platform, and service [21]. It allows its extension to several subdomains, even in smart spaces. However, the representation of activities that go beyond the use of applications on mobile devices is quite limited.

The CACOnt ontology ( Context-Aware Computing Ontology ) allows representing concepts related to users, devices, services, location, and environment [30]. It is possible to represent several different context categories without associating temporal information, making implementing context history difficult.

A three-level approach is used by 3LConOnt ( Three-Level Context Ontology ): a higher level ontology (more generic concepts), an intermediate level ontology, and a lower level ontology (domain ontologies). The top-level ontology defines two concepts: context and entity information. Context information concept has seven subclasses: Activity, Location, States, Role, Environment, Profile, and Time [8]. Thus, this ontology can represent several categories of conceptual context.

Finally, the ontology CAMeOnto ( Context Awareness Meta Ontology ) was defined in two levels: a first level where high-level concepts were defined, and a second level for domain-specific ontologies [2]. The first level presents six key concepts: User, Activity, Time, Device, Services, and Location.

As shown above, several high-level ontologies claim to model context-related concepts. These ontologies generally bring solutions to represent many contextrelated concepts, but they must be richer to represent essential aspects in pervasive environments such as smart spaces:

1. Some of these ontologies, even if they claim to be high-level, were modeled with specific environments in mind (such as smart rooms), which limits their applicability.
2. They need concepts for modeling important information in smart spaces, such as contexts of interest and entities.
3. Applications can classify contextual information by combining operational and contextual categories. The analyzed ontologies do not support this feature.

## 5 SpaceCOn - Smart Spaces Context Ontology

Considering the specified requirements for the needed ontology, and the limitations of the existing ontologies, the authors decided to elaborate a new ontology for context modeling called SpaceCOn : Smart Spaces Context Ontology . For the development of this model, the methodology proposed by [19] called Ontology Development 101 was used. The methodology contains seven main steps.

The first step is the definition of the scope and domain of the ontology. This ontology describes concepts agents use to represent contextual elements and their instances. Therefore, this ontology should provide a high-level representation of context, leaving the representation of more specific concepts and their relationships to derived domain ontologies. Therefore, this ontology aims to be extensible to any subdomain within smart spaces. The scope of the ontology encompasses the concepts and terms to be used and shared between agents concerning contextual elements and their instances. The ontology must also support the representation of historical contexts.

The second step of the methodology considers the reuse of other ontologies. As already analyzed in Sect. 4, no specific pre-existing high-level ontology was used in this work. However, some of these ontologies can represent domainspecific concepts in subdomains. In addition, this work considered other ontologies for reuse, such as the ontology DOLCE+DnS Ultralite (DUL) 1 for representing entities in general, the ontology Time 2 for representing temporal concepts, and the ontology QUDT 3 for specifying quantities and units of measure.

The third step concerns the enumeration of terms related to the ontology's application domain. By the definitions already mentioned in this work, it was possible to identify the following terms: contextual element , contextual element instance , entity , context value , instant of time , aspect , context quality , QoC parameter , QoC value , context category .

Steps four, five, and six are related, respectively, to defining the hierarchy and relationships between classes, defining properties, and constraints. After applying these steps, the set of classes shown in Fig. 1 was obtained. The presented diagram uses OntoUML language to model the ontology [12].

The main class in this ontology is ContextualElementInstance , which represents a contextual element instance. Each of these instances is associated with a specific instant of time (represented by an individual of the Instant class defined in the Time ontology), which indicates the instance instant of creation. Furthermore, every instance has a contextual element associated with it, an optional set of corresponding QoC values, and an optional set of associated context categories. The latter allows relating operational and conceptual categories to instances of contextual elements. For example, it is possible to define that a contextual element instance related to the latitude aspect of a person, obtained from a GPS receiver, is related to the categories location (conceptual category) and context primary (operational category). Latitude information obtained from processing a GSM signal from a cell phone tower could receive the categories location and secondary context .

QoC information related to contextual element instances has a parameter (an instance of the QoCParameter class) and a value (an instance of the Quantity class, defined in the QUDT ontology). An instance of the Quantity class has a value and a unit associated with it, supporting the conversion of values between different units.

[1 http://ontologydesignpatterns.org/wiki/Ontology:DOLCE+DnS Ultralite.](http://ontologydesignpatterns.org/wiki/Ontology:DOLCE+DnS_Ultralite)

[2 https://www.w3.org/TR/owl-time/.](https://www.w3.org/TR/owl-time/)

[3 https://qudt.org/.](https://qudt.org/)

Fig. 1. SpaceCOn context concepts

[FIGURE]

The ContextValue class allows representing any value associated with a contextual element instance. These values can be defined more precisely in derived domain ontologies. Possibilities include, for example, values obtained from observing sensors (for example, instances of the class Observation defined in the ontology SOSA - Sensor, Observation, Sample, and Actuator 4 ) or higherlevel values represented in the form of other domain-specific context ontologies.

ContextualElement class represents contextual elements. Each contextual element is related to an entity (represented as an instance of the Entity class defined in the DUL ontology) and to an aspect (instance of the Aspect class). Each aspect can be directly related to context categories. For example, latitude and longitude coordinates will always receive a location category. Categories related to an aspect will automatically be associated with all instances of contextual elements related to that aspect.

[4 https://www.w3.org/TR/vocab-ssn/.](https://www.w3.org/TR/vocab-ssn/)

Input contextual elements can provide additional information that characterizes some derived contextual elements. An example of such a situation would be the average of the X-axis component of the acceleration of a given smartphone . Such a contextual element is associated with an entity (smartphone) and an aspect (average), but another input contextual element (X component of smartphone acceleration) is necessary to characterize it completely. The class ParametrizedContextualElement can represent such contextual elements in the ontology. Instances of this class must be associated with at least one input represented by an instance of the ContextualElementInput class. A given input may be a set of values from an observation window. The ContextualElementWindowedInput class can represent input sets of values by specifying a sampling frequency, size (in time units), and percentage of overlap.

## 6 Evaluation

The ontology was implemented in OWL language using Prot´ eg´ e software [17], version 5.5.0. The implementation used the gUFO [4] as base ontology. The implementation of each class is summarized below.

1. ContextualElement
2. -Subclass of: gufo:Kind
3. -Restrictions:
- spacecon:characterizes exactly 1 dul:Entity
2. ContextualElementInstance
- spacecon:hasAspect exactly 1 spacecon:Aspect
7. -Subclass of: gufo:Kind
8. -Restrictions:
- spacecon:hasContextElement exactly 1 spacecon:ContextualElement
- time:hasTime exactly 1 time:Instant
- spacecon:hasContextValue exactly 1 spacecon:ContextValue
3. ContextualElementInput
13. -Subclass of: gufo:Kind
14. -Restrictions:
- spacecon:hasCtxElement exactly 1 spacecon:ContextualElement
4. ContextValue
17. -Subclass of: gufo:Kind
18. -Restrictions: -
5. SimpleQoCValue
20. -Subclass of: gufo:Kind
21. -Restrictions:
- qudt:hasQuantity exactly 1 qudt:Quantity

exactly

- spacecon:hasQoCParameter 6. ContextualElementWindowedInput

1 spacecon:QoCParameter

- -Subclass of: gufo:SubKind , spacecon:ContextualElementInput
- -Restrictions:
- spacecon:samplingRate exactly 1 qudt:Quantity

- spacecon:windowOverlapPercentage exactly 1 xsd:double
7. ParametrizedContextualElement
- spacecon:windowSize exactly 1 qudt:Quantity
- -Subclass of: gufo:SubKind , spacecon:ContextualElement
- -Restrictions:
- spacecon:hasInput some spacecon:ContextualElementInput
8. Aspect
- -Subclass of: gufo:Role
- -Restrictions: -
9. ContextCategory
- -Subclass of: gufo:Role
- -Restrictions: -
10. ConceptualCategory
- -Subclass of: gufo:Role , spacecon:ContextCategory
- -Restrictions: -
11. OperationalCategory
- -Subclass of: gufo:Role , spacecon:ContextCategory
- -Restrictions: -
12. QoCParameter
- -Subclass of: gufo:Role
- -Restrictions: -

The classes ContextualElement , ContextualElementInstance , ContextValue , SimpleQoCValue , ContextualElementInput are disjoint. Similarly, the classes OperationalCategory , ConceptualCategory are also disjoint.

To evaluate the capacity of the ontology to represent real-world situations, we used a case study based on the scenario presented in [22]. The described scenario involves recognizing people's activity by capturing data from motion sensors while performing routine day-to-day tasks. A dataset called Opportunity was generated from the data collected through the execution of sequences of activities by volunteers in a room simulating a small apartment. Four activities related to modes of locomotion were performed by the volunteers: standing, walking, lying, and sitting.

The wearable sensors each volunteer used generated the data to obtain the activities. Figure 2 shows the sensors' location. The sensors include twelve 3D accelerometers (shown in yellow in the figure) and seven IMU ( Inertial Measurement Unit ) inertial systems identified in red in the figure. The five IMUs on the volunteers' upper body (RLA, RUA, LUA, LLA, and BACK) can generate nine movement-related parameters (3D acceleration, 3D rotation, and 3D magnetic field). The IMUs on each volunteer's feet (R-SHOE and L-SHOE) provide another 32 parameters. In total, 113 parameters were generated by these sensors and recorded in the dataset .

The described scenario still contained sensors in objects scattered throughout the environment. However, the inference process to obtain the considered activities do not use data from these sensors. Thus, the evaluation process described here does not present models for these data.

Fig. 2. Location of sensors to capture data for the Opportunity dataset [22]

[FIGURE]

Each volunteer in the scenario was modeled using the dul:Entity class. Each sensor obtains data from different body parts, and they were also modeled as entities that are constituents of each volunteer. An example of entity modeling using the proposed ontology in the described scenario is shown in Fig. 3. The volunteer S1 is a dul:Entity instance, and its constituents are other entities that model parts of the body with sensors.

Fig. 3. Example of entity modeling a volunteer

[FIGURE]

Each sensor can provide some aspects. For instance, 3D accelerometers can provide three aspects: the acceleration's x, y, and z components. IMU sensors can provide the x, y, and z values of rotation, magnetic field, and acceleration components. Sixteen instances from the class Aspect of SpaceCOn ontology modeled aspects in the scenario: AccelerationX, AccelerationY, AccelerationZ, AngularVelocityX, AngularVelocityY, AngularVelocityZ, CompassAngle, MagneticFieldX, MagneticFieldY, MagneticFieldZ, OrientationX, OrientationY, OrientationZ, RotationX, RotationY, RotationZ .

An inference module obtains the locomotion mode of each volunteer. The input received by this module is the mean of each aspect value the sensors provide. Therefore, the scenario ontology contains two additional aspects: Activity (for locomotion mode) and Mean .

The scenario has 227 contextual elements for each volunteer: 113 aspects provided by sensors, 113 mean values of each aspect, and one activity. An instance of the ContextualElement class modeled each contextual element provided in the considered scenario. Figure 4 shows an example of a contextual element defined to model the activity of the S1 volunteer.

Fig. 4. Example of a contextual element that models the activity of the S1 volunteer

[FIGURE]

Figure 5 shows another example of a contextual element. In this example, an individual of the ParametrizedContextualElement models the mean value of the acceleration x component from the back sensor of the S1 volunteer. The top part of the figure shows the contextual element that models the mean value. The bottom part of the figure shows the model of the input value that points to the contextual element that models the acceleration x component of the back of S1. The input models a window of acceleration value with the specified sampling rate, window size, and overlap percentage.

Eight individuals model context categories: two operational categories ( PrimaryContext and SecondaryContext ) and six conceptual categories ( ActivityCategory , ContextOfInterestCategory , IndividualCategory , LocationCategory , RelationalcCategory , and TimeCategory . Each aspect receives one or more related categories. For instance, aspects related to sensors receive the category PrimaryContext , while the Activity aspect receives the ActivityCategory and SecondaryContext categories. The scenario ontology contains a QoC parameter, Accuracy , as an instance of the QoCParameter class.

In this scenario, the ContextValue class has been extended in four new concepts (see Fig. 6): Observation , WindowedValue , AggregatedValue , and ActivityValue . The Observation class models a value obtained from a sensor. An instance of the QUDT Quantity class models the observation value. A WindowedValue is a value in a set of observations representing a window of values with a sampling rate, size (in a time unit), and an overlapping percentage. The AggregatedValue class models a value obtained after calculating the mean of a window of observations. Finally, the ActivityValue class models an inferred locomotion mode.

Fig. 5. Example of a contextual element that models the mean value of acceleration x-axis from the S1 volunteer back.

[FIGURE]

Fig. 6. Extension of ContextValue concept created in the case study.

[FIGURE]

Figure 7 shows an example of a contextual element instance. The instance EXAMPLE CTX ELEM INSTANCE 1 TIME is an individual of the class Instant of W3C Time ontology. The ACTIVITY WALKING VALUE instance is an individual of ActivityValue class.

Finally EXAMPLE CTX ELEM INSTANCE 1 QOC VALUE is an instance of the SimpleQoCValue class.

Situation modeling is a limitation of SpaceCOn. Situations, as defined in [13], are a set of contexts that hold in a time interval. For example, John is traveling to Portugal to attend ER conference is an example of a situation with a specific duration. It is possible to model relations between context instances in SpaceCOn through the specialization of ContextValue concept. For instance, a situation instance value can be a set of other instances that compose it. However, SpaceCOn relates a specific time instant to each contextual element instance and does not support the association of time intervals, and situation modeling is a limitation of the ontology. Even so, a situation modeling ontology can use SpaceCOn to model contextual instances that compose a specific situation.

Fig. 7. Example of contextual element instance modeled with the ontology.

[FIGURE]

## 7 Context Integration Architecture

The SpaceCOn ontology has been used in an architecture for context integration described in Fig. 8. Each agent encapsulates a context source (such as a sensor, an inference engine, a database, or a web service). The whole model is a large society where agents can come and go. Agents can enter society by providing access to new sources of context. These agents can leave if their capabilities are no longer needed.

Logical sets called nodes aggregate agents. An agent can be part of only one node. Each node works as a federation, where an agent called broker acts as a facilitator and manages all the information that enters and leaves the node. Intermediary agents are responsible for carrying out the exchange of information between nodes. These agents are organized in a peer-to-peer network to connect nodes without needing a centralizing entity. Teams of agents can be formed, even between agents from different nodes, to cooperate in providing the contextual elements requested by an application.

Each application is a context consumer managed by the model. An application must insert itself inside a node and access its context information. Applications can send query requests or subscribe to brokers to receive instances of contextual elements. These requests contain a set of contextual elements that the architecture must provide. To answer these requests, the brokers consult other agents in the node or in other nodes to obtain all the requested information.

Agents communicate using messages. The messages use terms defined by the SpaceCOn ontology. For example, query requests contain a set of instances of the ContextualElement class, and responses to applications contain a set of instances of contextual elements modeled through the ContextualElementInstance class.

Fig. 8. The context integration architecture that uses SpaceCOn.

[FIGURE]

## 8 Conclusion

This paper describes an ontology called SpaceCOn for representing context in smart environments. Classes for context-related concepts were analyzed in the context recognition literature and included in the ontology. An analysis of the existing high-level ontologies for context representation showed that SpaceCOn covers aspects other models do not support.

A case study based on the literature showed that ontology had reached the intended purpose of consistently representing context information. SpaceCOn can be used with success to represent contextual elements and their instances. Furthermore, domain ontologies can extend SpaceCOn to represent domainspecific concepts.

We intend to model context in other scenarios and domains in future work. We intend to use the ontology in a context-aware application based on the integration architecture shown in this work.

Acknowledgments. This study was supported by CNPq/MCTI/FNDCT N o 18/2021 grant n. 405973/2021-7, and by the Federal Institute of Education, Science and Technology of Rio Grande do Sul (IFRS).

## References

1. Abowd, G.D., Dey, A.K., Brown, P.J., Davies, N., Smith, M., Steggles, P.: Towards a better understanding of context and context-awareness. In: Gellersen, H.-W. (ed.) HUC 1999. LNCS, vol. 1707, pp. 304-307. Springer, Heidelberg (1999). https:// doi.org/10.1007/3-540-48157-5 29
2. Aguilar, J., Jerez, M., Rodr´ ıguez, T.: CAMeOnto: context awareness meta ontology modeling. Appl. Comput. Inform. 14 (2), 202-213 (2018)
3. Al-Shargabi, A., Siewe, F., Zahary, A.: Quality of context in context-aware systems (2017)
4. Almeida, J., Guizzardi, G., Falbo, R., Sales, T.P.: gUFO: a lightweight implementation of the unified foundational ontology (UFO) (2019). http://purl.org/nemo/ doc/gufo
5. Aranda, J.A.S., Bavaresco, R.S., de Carvalho, J.V., Yamin, A.C., Tavares, M.C., Barbosa, J.L.V.: A computational model for adaptive recording of vital signs through context histories. J. Ambient Intell. Humanized Comput. 1-15 (2021)
6. Bazire, M., Br´ ezillon, P.: Understanding context before using it. In: Dey, A., Kokinov, B., Leake, D., Turner, R. (eds.) CONTEXT 2005. LNCS (LNAI), vol. 3554, pp. 29-40. Springer, Heidelberg (2005). https://doi.org/10.1007/11508373 3
7. Bettini, C., et al.: A survey of context modelling and reasoning techniques. Pervasive Mob. Comput. 6 (2), 161-180 (2010)
8. Cabrera, O., Franch, X., Marco, J.: 3LConOnt: a three-level ontology for context modelling in context-aware computing. Softw. Syst. Model. 18 (2), 1345-1378 (2019)
9. Chen, H., Finin, T., Joshi, A.: An ontology for context-aware pervasive computing environments. Knowl. Eng. Rev. 18 (3), 197-207 (2003)
10. Chen, H., Perich, F., Finin, T., Joshi, A.: SOUPA: standard ontology for ubiquitous and pervasive applications. In: The First Annual International Conference on Mobile and Ubiquitous Systems: Networking and Services, MOBIQUITOUS 2004, pp. 258-267. IEEE (2004)
11. Dey, A.K., Abowd, G.D., Salber, D.: A conceptual framework and a toolkit for supporting the rapid prototyping of context-aware applications. Hum.-Comput. Interact. 16 (2-4), 97-166 (2001)
12. Guizzardi, G., Fonseca, C.M., Benevides, A.B., Almeida, J.P.A., Porello, D., Sales, T.P.: Endurant types in ontology-driven conceptual modeling: towards OntoUML 2.0. In: Trujillo, J.C., et al. (eds.) ER 2018. LNCS, vol. 11157, pp. 136-150. Springer, Cham (2018). https://doi.org/10.1007/978-3-030-00847-5 12
13. Gundersen, O.E.: Situational awareness in context. In: Br´ ezillon, P., Blackburn, P., Dapoigny, R. (eds.) CONTEXT 2013. LNCS (LNAI), vol. 8175, pp. 274-287. Springer, Heidelberg (2013). https://doi.org/10.1007/978-3-642-40972-1 21
14. Manzoor, A., Truong, H.L., Dustdar, S.: Quality of context: models and applications for context-aware systems in pervasive environments. Knowl. Eng. Rev. 29 (2), 154-170 (2014)
15. Martini, B.G., et al.: IndoorPlant: a model for intelligent services in indoor agriculture based on context histories. Sensors 21 (5), 1631 (2021)
16. Morandi, C., Rolando, A., Di Vita, S.: From Smart City to Smart Region: Digital Services for an Internet of Places. SAST, Springer, Cham (2016). https://doi.org/ 10.1007/978-3-319-17338-2
17. Musen, M.A.: The prot´ eg´ e project: a look back and a look forward. AI Matt. 1 (4), 4-12 (2015)

18. do Nascimento, L.V., Machado, G.M., Maran, V., de Oliveira, J.P.M.: Context recognition and ubiquitous computing in smart cities: a systematic mapping. Computing 103 (5), 801-825 (2021)
19. Noy, N.F., McGuinness, D.L., et al.: Ontology development 101: a guide to creating your first ontology (2001)
20. Perera, C., Zaslavsky, A., Christen, P., Georgakopoulos, D.: Context aware computing for the internet of things: a survey. IEEE Commun. Surv. Tutor. 16 (1), 414-454 (2014). https://doi.org/10.1109/SURV.2013.042313.00197
21. Preuveneers, D., et al.: Towards an extensible context ontology for ambient intelligence. In: Markopoulos, P., Eggen, B., Aarts, E., Crowley, J.L. (eds.) EUSAI 2004. LNCS, vol. 3295, pp. 148-159. Springer, Heidelberg (2004). https://doi.org/ 10.1007/978-3-540-30473-9 15
22. Roggen, D., et al.: Collecting complex activity datasets in highly rich networked sensor environments. In: 2010 Seventh International Conference on Networked Sensing Systems (INSS), pp. 233-240. IEEE (2010)
23. da Rosa, J.H., Barbosa, J.L., Ribeiro, G.D.: ORACON: an adaptive model for context prediction. Expert Syst. Appl. 45 , 56-70 (2016)
24. dos Santos, V.V.: CEManTIKA: a domain-independent framework for designing context sensitive systems (2008)
25. Schilit, B., Adams, N., Want, R.: Context-aware computing applications. In: 1994 First Workshop on Mobile Computing Systems and Applications, pp. 85-90. IEEE (1994)
26. Strang, T., Linnhoff-Popien, C., Frank, K.: CoOL: a context ontology language to enable contextual interoperability. In: Stefani, J.-B., Demeure, I., Hagimont, D. (eds.) DAIS 2003. LNCS, vol. 2893, pp. 236-247. Springer, Heidelberg (2003). https://doi.org/10.1007/978-3-540-40010-3 21
27. Van Bunningen, A.H., Feng, L., Apers, P.M.: Context for ubiquitous data management. In: International Workshop on Ubiquitous Data Management, pp. 17-24. IEEE (2005)
28. Villegas, N.M., M¨ uller, H.A.: Managing dynamic context to optimize smart interactions and services. In: Chignell, M., Cordy, J., Ng, J., Yesha, Y. (eds.) The Smart Internet. LNCS, vol. 6400, pp. 289-318. Springer, Heidelberg (2010). https://doi. org/10.1007/978-3-642-16599-3 18
29. Wang, X.H., Zhang, D.Q., Gu, T., Pung, H.K.: Ontology based context modeling and reasoning using OWL. In: Proceedings of the Second IEEE Annual Conference on Pervasive Computing and Communications Workshops, pp. 18-22. IEEE (2004)
30. Xu, N., Zhang, W.S., Yang, H.D., Zhang, X.G., Xing, X.: CACOnt: a ontologybased model for context modeling and reasoning. In: Applied Mechanics and Materials, vol. 347, pp. 2304-2310. Trans Tech Publications (2013)
