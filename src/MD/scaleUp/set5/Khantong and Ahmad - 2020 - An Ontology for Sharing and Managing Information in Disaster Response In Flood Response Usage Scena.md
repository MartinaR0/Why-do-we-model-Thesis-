## ORIGINAL ARTICLE

## An Ontology for Sharing and Managing Information in Disaster Response: In Flood Response Usage Scenarios

Sommai Khantong 1  · Mohammad Nazir Ahmad 2

Received: 1 October 2018 / Revised: 14 October 2019 / Accepted: 10 December 2019 / Published online: 14 December 2019 © Springer-Verlag GmbH Germany, part of Springer Nature 2019

## Abstract

Information management and sharing is an essential ingredient, but a difficult and challenging problem for disaster response management due to the large number of heterogeneous concepts used in different organizations. To solve this problem, the number of those heterogeneous concepts has to be reduced. This paper proposes an ontology as a solution to reduce the large number of concepts by understanding only on necessary ontological concepts needed in communication via speech act between the organizations. This is a new approach where the ontology provides a conceptual representation of the disaster response domain from the perspective of communication between the organizations involved. More specifically, the ontology was designed and developed by using the concept of interlocking institutional worlds, in which speech act theory is used as a foundation to present interactions among the organizations, and by using philosophically grounded foundational ontologies. To make this whole approach work, we show an important demonstration of the utility of our proposed work, which is in the expatiation quadrant of the Design Science Research methodology on designing our domain ontology for disaster response management.

Keywords Disaster management · Flood response · Ontology · Domain ontology · Information management and sharing

## 1  Introduction

Information management and sharing is essential in disaster management, especially in the response phase. Several organizations are typically required in the disaster response to cooperate with each other [1, 2], and a huge amount of information is generated and used by different processes handled by different systems in these different organizations [3]. The information generated in one process needs to be shared with other relevant processes that may be performed by different systems in several organizations, and the information collection, storage and queries must be performed on an urgent basis. However, managing and sharing of such information is challenging. The disaster-related information is difficult to manage due to its large amount and diversity as well as geographical distribution [3

* Sommai Khantong sommai.k@acc.msu.ac.th

1 Mahasarakham Business School, Mahasarakham University, Maha Sarakham, Thailand

2 Institute of Visual Informatics, Universiti Kebangsaan Malaysia, Bangi, Selangor, Malaysia

information generated from different systems and represented in heterogeneous formats cannot be easily shared with others because of syntactic and semantic heterogeneity [4]. This issue of management and sharing information from heterogeneous organizations is a challenging issue. The research work on this problem area is still ongoing and many perspectives of approach have been discussed and proposed in the literature. This showing the progress and the topics are still relevant and ongoing.

As mentioned above, one of the main challenges in information management and sharing in the disaster response context is due to the large number of heterogeneous concepts used in different organizations. Therefore, to solve this information management and sharing problem realistically, the number of those heterogeneous concepts has to be reduced. To help with the reduction, it is necessary to deal with intraand inter-organizational interactions as the disaster response process involves several interoperating and interacting workflows from different organizations. Therefore, in this paper, we suggest that emphasizing on understanding ontological concepts needed in the communication via speech act in the flood response management field is one way of reducing this large number of ontological concepts. However, although existing ontologies that represent knowledge of the disaster response domain from different points of view are suitable for their intended purposes, there are no ontologies that describe the disaster response domain from the point of view of communication between the involved organizations. Accordingly, this paper aims to develop an ontology that provides a conceptual representation of the disaster response domain from the perspective of communication between the organizations involved. The ontological concepts will be organized under upper ontological concepts borrowed from the concept of interlocking institutional worlds [5], in which speech act theory is used as a foundation to present interactions among the organizations.

[FIGURE]

[FIGURE]

In this paper, the research method used is based on the design science paradigm in IS research [6, 7]. The design science is a problem solving paradigm, aiming to build new artifacts in order to improve or extend the capabilities of humans and organizations [6]. The ontology proposed in this paper is a design artifact in the form of instantiations according to the design science concept. It is designed and developed based on philosophically grounded foundational ontologies, UFO [8] and DEMO [9, 10], and rooted in the concept of interlocking institutional worlds [5].

The rest of this paper is organized as follows. Section 2 presents background and reviews ontologies developed in the area of disaster response management. Section 3 describes the research methodology used. In Sect. 4, the development of disaster response management domain ontology is presented. The ontology usage is demonstrated in Sect. 5 and evaluated in Sect. 6. Section 7 discusses implications of the study. Finally, Sect. 8 concludes the paper.

## 2    Background and Literature Review

## 2.1    Disaster Response Management

As defined by the United Nations Office for Disaster Risk Reduction [11], a disaster is 'a serious disruption of the functioning of a community or a society involving widespread human, material, economic or environmental losses and impacts, which exceeds the ability of the affected community or society to cope using its own resources.' Disasters can be categorized into three groups by the origin of their hazards, namely, man-made, natural and technological disasters [2]. Man-made disasters can be seen from terrorist activities as an example, which can occur in the form of natural or technological accidents. Examples of natural disasters are flood, earthquakes, windstorms, landslides, wildfires and drought. Technological disasters are related to industrial accidents, transport accidents and bomb explosions. Among these kinds of disasters, natural disasters have a large impact in terms of human distress, property losses and economic damages. Therefore, this paper specifically focuses on the flood as an example of natural disasters.

[FIGURE]

Typically, the response to disasters consists of actions to manage and control the various effects of disaster (also the ripple effects) and minimize human and property losses [1]. In flood management, according to Shrubsole [12], the response phase deals with operations that are directed at managing the consequences of an imminent flood even before  the  actual  flood  has  occurred.  Therefore,  flood response management is not only performed during the actual flood, but also during an imminent flood. It is comprised of several processes, including floods forecasting, flood forecasts updating, the current flood situation assessment, flood control operation and evacuation [13, 14].

## 2.2    Ontology

## 2.2.1    What is an Ontology?

Ontology is originally a philosophy term and has become a relevant word of information systems and computing disciplines. In the computational perspective, as defined by Gruber [15], an ontology is 'a formal explicit specification of a shared conceptualization for a domain of interest.' It is an engineering artifact that represents a specific domain of knowledge [16, 17]. The ontology is concerned with representing and understanding a specific domain [18]. Therefore, it aims to represent a description of conceptualization of reality in a specific domain, which consists of concepts and relationships between these concepts.

Ontologies are developed and represented in different levels of abstraction. Accordingly, ontologies can be represented by different formalisms and languages, depending on their objective. Guarino [17] classifies ontologies based on the level of abstraction they represent as follows: (1) Top -level ontologies -a top-level ontology consists of a set of universal concepts which are independent of any domain or problem, such as the concepts of object, event, action, etc.; (2) Domain ontologies -a domain ontology aims to describe a conceptualization that is related to a specific domain; (3) Task ontologies -a task ontology specifically describes a generic activity or task; (4) Application ontologies -an application ontology intends to describe concepts that are specifications of specific domain and task ontologies. The top-level ontologies (also known as foundational ontologies) are more general and can be specialized into a domain ontology or a task ontology.

Typically, ontology development is not a goal in itself. Over several decades, ontologies have been developed for different objectives of usage and used in a variety of domains. As reviewed by Valente [19], the main uses of ontologies are for semantic indexing and search, information organization and structuring, problem solving and reasoning, understanding the domain and semantics interoperation.

## 2.2.2    Ontologies Related to Disaster Response Management

A variety of ontologies have been developed to apply in various phase of disaster management. However, this section focuses only on the ontologies that are related to the response phase. Babitski et al. [20], an ontology was developed within the SoKNOS project, specifically aimed at integrating information from heterogeneous organizations for resource planning in disaster response. de la Asunción et al. [21] proposed SIADEX ontology for process planning under uncertainty for decision support during a disaster. It serves as a knowledge base that provides knowledge required in the planning process. Bénaben et al. [22] proposed the ISyCri ontology for disaster response coordination management. Smart et al. [23], many domain-relevant ontologies were developed for the AKTiveSA system, including Geography, Transportation, Meteorology, Humanitarian aid, Military, Equipment, Organizations and Weapons. These ontologies are designed for enhancing situation awareness within a specific context of humanitarian and disaster relief operations. Kalabokidis et al. [24] proposed an ontology, named OntoFire, which is developed specifically for the wildfires domain, with the aim to improve information retrieval mechanisms of geo-portals by enabling a semantic-based search for geo-informational resources of interest. Amailef and Lu [25] proposed a case attribute domain ontology which is used to support case-based reasoning approaches in order to improve the efficiency and effectiveness of decision-making in responding to a disaster situation.

As discussed above, the ontologies developed for disaster response represent knowledge of the domain from different points of view. However, as the disaster response process involves several interoperating and interacting workflows from different organizations, we think that the approach to look at disaster response from the point of view of communication between the involved organizations is an interesting approach to gather new knowledge about the domain of disaster response in order to fulfill information management and sharing purposes. In addition, currently, a few ontologies related to disaster response are grounded in foundational ontologies. As reviewed above, only the SoKNOS ontology by Babitski et al. [20] follows Descriptive Ontology for Linguistic and Cognitive Engineering (DOLCE) foundational ontology [26]. Therefore, since the importance of using foundational ontologies to develop domain ontology (discussed in Sect. 2.2.5 below), the ontology of disaster response domain in this paper is also developed by using foundational ontologies. This ontology is categorized as a domain ontology. The target domain is that of disaster response. However, since there are many types of disasters, this ontology is developed specifically for flood response as a case of disaster response.

## 2.2.3    Ontology Engineering

According to Guizzardi [8], the engineering phases of ontology development are similar to those of information systems development that include conceptual modelling, design and codification phases. Each of these phases produces its own artifacts with different objectives. Therefore, it requires different types of languages to represent the artifacts.

In the conceptual modelling phase, the ontology should represent the subject domain expressively, clearly and truthfully. To meet these requirements, conceptual modelling languages can be utilized. As suggested by [8, 27, 28], Unified Modeling Language (UML) is the most suitable ontology modelling language. UML is a graphical notation, which is easy to understand. Therefore, UML Class Diagrams and UML Activity Diagrams are selected to model the endurant and perdurant parts of the ontology, respectively.

From the conceptual modelling phase, the conceptual model can be implemented by different ontological languages. As surveyed by Kalibatiene and Vasilecas [29], there are several languages for representing an ontology in the implementation phase. Among the ontology implementation languages, RDF and OWL can be used for representing the endurant part of the ontology at the implementation level. RDF (Resource Description Framework) is a standard language to describe information resources on the web [30]. RDF expresses web resources by using Uniform Resource Identifier (URI) references and triplet statements of the form &lt; a subject, a predicate, an object &gt; [31]. The subject and object are classes, whereas the predicate is a property of the subject representing a relationship between the subject and the object. By using RDF, the formal semantics for the information can be represented in a standardized manner, enabling interoperability among different systems that exchange machine-understandable information. Ontology Web Language (OWL) is another language specifically designed for representing ontologies used in Semantic Web [32]. Similar to RDF, it is represented using the triplet statements. However, OWL extends RDF to add more elaborate semantics. Another ontological language is OWL-S, which is an extension of OWL to describe Web Services [33]. It is composed of three main sub-ontologies: service profile, service process model and service grounding.

Among the ontology implementation languages described above, RDF and OWL can be used for representing the endurant part of the ontology at the implementation level. However, only OWL-S has the potential to represent the perdurant part  because  it  consists  of  a  process  model. The OWL-S process model is divided into three types of processes, namely atomic, simple and composite. A composite process is composed of several atomic processes that realize abstract descriptions of simple processes, and of the flow of control and data between its atomic processes.

[FIGURE]

## 2.2.4    Ontology Development Methodologies

Several ontology development methodologies exist. Detailed surveys on these methodologies can be found in the works of [34, 35]. These methodologies differ in degree of detail, coverage of development steps, and strategy for building applications, among others. They have their own benefits and limitations. The ontology development methodology used in this paper is based on the methodologies by Uschold and King [36] and by Gomez-Perez et al. [37], which consists of four stages. The first stage is the purpose and scope identification, which identifies objectives of ontology and targeted users. The second stage is conceptualization of the domain. The third stage is domain capture. The final stage is ontology implementation.

## 2.2.5    The Role of Foundational Ontology in Domain Ontology Development

Any domain ontology can be developed based on the concepts provided by the foundational ontology [38]. The use of foundation ontology is to organize the 'things' that exist in a given domain so that the domain ontology is well-structured and is application independent [39]. According to Colomb [40] the use of foundation ontologies has significant benefits in developing domain ontologies. Foundational ontologies can help ontology developers to design and understand the domain by providing a rich vocabulary that describes that domain. In addition, domain ontologies developed based on foundational ontologies can achieve interoperability and a higher overall quality [8, 17, 41].

Various foundational ontologies have been proposed. Descriptive Ontology for Linguistic and Cognitive Engineering (DOLCE) [26] is one of the most prominent and influential upper ontologies in domain ontology development. DOLCE distinguishes entities into two main types, namely perdurants and endurants. An endurant is defined as an entity that exists in a timeless way. All of its parts exist at the same time. A perdurant is defined as an entity that happens in time. If it has parts, it has temporal parts that happen at different times. For example, the piece of paper you are reading now is wholly present, but some temporal parts of your reading are not present anymore. Typically, an endurant has a relationship with perdurants, in that an endurant 'lives' in time by participating in some perdurant(s). For instance, a student (an endurant) can participate in a class discussion (a perdurant). In addition, perdurants can be divided into two kinds, namely statives and events. An event is an essential whole. All of its parts are necessary. A stative is not an essential whole. Further details of these can be found in Gangemi et al. [42].

[FIGURE]

In order to represent the endurant ontology, in this paper, the Unified Foundational Ontology (UFO) by Guizzardi [8] is selected as it is a well-founded philosophically foundational ontology and has been widely used in developing domain ontologies in a variety of domains [43]. In particular, UFO combines DOLCE and BWW foundational ontologies, which extends the endurant ontology by articulating the concept of class into a system of kinds of classes, including Kind , Subkind , Category , Phase , Role and so on. These more specific concepts can be used in developing a domain ontology to avoid a number of anomalies in the domain ontology being developed, especially involving the identity of individuals [8].

For representing the perdurant part of domain ontology, a set of concepts based on the concepts of speech act can form a useful foundational ontology [27], since the disaster response domain is seen as a domain of interlocking institutional worlds, in which several organizations (institutions) interoperate by interlocking their worlds, as described in Sect. 2.3 below. According to Colomb and Ahmad [27], an institutional world is defined as a collection of speech acts that create or destroy institutional facts, which are performed by an authorized institution. Basically, a speech act involves two or more parties cooperating with each other.

For instance, a purchase involves at least two parties, a buyer and a seller, and can involve many. However, the general theory of speech acts covers a wide spectrum of phenomena. It would be useful to have a specialization of the general theory of speech acts directed toward information systems. In this sense, the DEMO theory [9, 10] is prominent since it has been developed and used as a means for enterprise modelling and information systems engineering in several domains. DEMO recognizes that a speech act performed as an item of business is generally a complex action. A business act is a type of speech act called a production act or P -act . This is the ontologically stable aspect of an organization. A P -act is generally performed as the result of a conversation among several parties. Each step in the conversation is another type of speech act called a coordination act or C -act . The C -acts producing a P -act are packaged in a transaction. The P -act is made only if the transaction completes. The C -acts are subject to change, even though the P -act remains stable. These actions are performed by subjects playing roles, or actors. A subject is a person or organization capable of taking responsibility. Therefore, P -acts and C -acts are meta-model or meta-concepts borrowed from DEMO metamodeling approach, which are utilized for capturing perdurants at ontological level.

The representations of endurant and perdurant ontologies described above provide a useful way to develop our domain ontology that is well-founded, using philosophically grounded foundational ontologies. It can help to promote quality of the domain ontology and achieve interoperability of systems that rely on this ontology.

## 2.3    Interlocking Institutional Worlds

In this study, the disaster response management domain is described with the concept of interlocking institutional worlds. The domain of disaster response is seen as a domain of interlocking institutional worlds, in which several organizations (institutions) interoperate by interlocking their worlds. The concept of interlocking institutional worlds is introduced by Colomb and Ahmad [5] and used in the domain of interoperating information systems. This concept was developed based on the theories of speech acts and institutional facts by Searle [44]. An institutional fact is an element of social reality which is different from physical reality. As put forward by Searle [44], a brute fact (which is a physical reality) X counts as institutional fact (which is a social reality) Y in context C . Searle's conception of institutional facts includes the idea that part of the context is that the speech act was made by a properly constituted body (institution) using formal procedures. Institutional speech acts create and destroy objects in institutional reality. For example, the marriage speech act creates a marriage, a husband and a wife. The act also destroys an unmarried man and an unmarried woman. A consequence of the institutional nature of institutional speech acts is that the objects they create have a scope of validity limited to the scope of the institution creating them. A marriage created in one jurisdiction may not be considered valid in another. Therefore, this concept can be utilized in the stage of domain conceptualization of the ontology creation process, to identify and describe that what sorts of entities exist in the domain. The next section provides the research methodology used in this study.

## 3    Research Methodology

In this paper, Design Science Research (DSR) methodology is adopted as the research methodology. DSR has attracted increasing attention to the research community of information systems (IS). Within the IS discipline, DSR has enabled the development of novel IT artifacts, organizational development and theory building [45]. It concerns designing novel and innovative artifacts to support organizational and human purposes, which is different from natural science research that mainly aims to understand reality in order to predict or explain organizational or human behavior and thus producing theoretical knowledge [6]. According to the design science concept, the ontology proposed in this research is an artifact in the form of instantiations.

Several scholars have proposed guidelines or methodologies for conducting DSR in the IS research. The paper follows the DSR methodology proposed by Peffers et al. [7], which consists of six stages as follows:

## 3.1    Problem Identification and Motivation

The main activity of this stage is to determine the specific problem and justify the value of a solution to the problem. As discussed in Sect. 1, the problem identified in this study is about the information management and sharing in disaster response. It is a challenging issue to manage and share information in the disaster response context, due to the large amount and diversity of information and syntactic and semantic heterogeneity of the information. In flood response, for example, the information about weather forecast, water level, flood forecast, water management measures, and other are independently generated by different processes performed by coordination of different authorities such as meteorology authority, water management authority and other relevant organizations. In this context, these different organizations may use different syntaxes and terminologies for describing information as well as the same term may have different meanings and interpretations in different organizations. One organization might use the term 'river,' while another might use the term 'lake' to describe the concept 'water area.' Consequently, although the meanings of the concepts for describing information from these organizations are similar, stakeholders and computational systems in different organizations cannot understand the meanings. To solve this problem, the number of those heterogeneous concepts has to be reduced. As the disaster response process involves several interoperating and interacting workflows from different organizations, one way to reduce the large number of concepts is to understand only on necessary ontological concepts needed in communication between the organizations. Therefore, there is a need to develop an ontology that provides a conceptual representation of the disaster response domain from the perspective of communication between the organizations involved.

## 3.2    Definition of the Objectives of a Solution

In this stage, the main activity is to infer the objectives of a solution from the problem definition. In this study, the ontology is proposed as a solution to the problem, which is an artifact in the form of instantiations according to the design science concept. The main desirable objective of the proposed ontology is to be used for capturing common concepts related to flood response management and their relationships in order to support information management and sharing. The common concepts are domain-oriented (disaster response domain) things that will be organized under upper ontological concepts borrowed from the concept of interlocking institutional worlds, in which speech act theory is used as a foundation to present interactions among the organizations.

[FIGURE]

## 3.3    Design and Development

The activity in this stage is to describe the artifact design and development, showing how it is designed and developed. In the paper, the ontology is developed using the methodology described in Sect. 2. In developing the ontology, the concept of interlocking institutional worlds is utilized as a conceptual framework to discover specific concepts of the domain. These concepts of the domain are modelled at the conceptual level, using UML notation. Endurant ontology was modelled by UML class diagrams based on the Unified Foundational Ontology (UFO) foundational ontology [8], whereas perdurant ontology was modelled by UML activity diagrams based on the theory of Design and Engineering Methodology for Organizations (DEMO) [9, 10], simplified by UML-based DEMO [27]. These conceptual models of the ontology are then transformed to be represented in the ontology implementation languages. By using the Protégé tool, the endurant ontology was represented in OWL and the perdurant ontology was represented in OWL-S. All of these are presented in detail in Sect. 4.

## 3.4    Demonstration

The main activity in this phase is to demonstrate the utility of the artifact in an illustrative or real-life case. The artifact can demonstrate its usage by means of simulation, experimentation, prototype, case study or others. In this study, the utility of the proposed ontology is demonstrated in a case study. This is presented in detail in Sect. 5.

## 3.5    Evaluation

In this phase, the artifact is evaluated to verify that it fulfills the defined objectives. The activity of evaluation is to compare the defined objectives of a solution with the results of the usage of the artifact observed from the demonstration phase. Evaluation may take many forms, depending on the problem feature and the artifact. In this study, the evaluation is done by means of semi-structure interviews with experts and practitioners in flood response. See Sect. 6 for more details.

## 3.6    Communication

In this phase, the problem and its importance as well as the proposed artifact, its utility and novelty, the rigorousness of its design and its effectiveness are communicated to the relevant research audience, e.g., in the form of academic write-ups, such as this paper.

[FIGURE]

## 4    Design and Development of the Flood Response Domain Ontology

The following subsections present the outcome of each of the ontology development processes.

## 4.1    Ontology Purpose and Scope

The main purpose of the ontology is to be used for capturing common concepts related to flood response management and their relationships in order to support information management and sharing. The intended users of the ontology are flood response stakeholders. In addition, the ontology is constrained to cover only the response phase of flood management. As discussed in Sect. 2.1, flood response management is comprised of many processes. However, the paper contains only some key processes, including flood prediction, flood control, flood defense and evacuation.

## 4.2    Domain Conceptualization

As stated in Sect. 2, the domain of disaster response is seen as a domain of interlocking institutional worlds, in which several organizations (institutions) interoperate by interlocking their worlds. In the institutional world, institutional facts are created, destroyed and manipulated by speech acts, which are formal declarations by designated officials of institutions. A speech act is a special type of action. Therefore, the sorts of entities that exist in the institutional worlds include institutional facts, speech acts and actor-roles that perform the speech acts. Therefore, the ontological concepts include institutional facts, actor-roles and speech acts that are action-oriented concepts. Accordingly, in the case of flood response, the relevant concepts can be identified as shown in Table 1. Some of these concepts are adapted from the work of [46]. The relationships among the concepts are determined as shown in Table 2. As described earlier, speech acts create or destroy institutional facts, which are performed by an authorized institution (an actor). Therefore, each process shown in Table 2 is composed of a set of concepts of institutional facts and actor-roles as well as action-oriented concepts that produce the institutional fact by the actor, and relationships among them. In Table 2, the underlined words denote the concepts of institutional facts and actor-roles, whereas the italic words denote the relationships between those concepts.

After identifying the relevant concepts and their relationships, the actors involved and their actions in each of the action-oriented concepts are determined. These actions are speech acts that performed by authorized actors. The speech acts can be categorized into coordination and production acts [5]. Because of the space limitation, only actors and their actions involved in the concept of flood forecasting are presented as shown in Table 3.

Table 1 Relevant concepts of the flood response domain

| Process          | Action-oriented concepts                    | Static concepts                                             |
|------------------|---------------------------------------------|-------------------------------------------------------------|
| Flood prediction | Flood forecasting                           | Flood forecast, weather forecast, flood event, area         |
| Flood control    | High water protection measures implementing | High water protection measures                              |
| Flood defense    | Flood defense measures implementing         | Flood damage, flood defense measures, resource              |
| Evacuation       | Flood evacuation implementing               | Flood evacuation, victim, evacuation registration, resource |

Table 2 Key concepts and relationships among them

| Process          | Keys concepts and relationships among them                                                                                                                                         |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flood prediction | A flood forecast uses weather forecast to predict a flood event that will occur in a specific area, which is carried out in the process of flood forecasting                       |
| Flood control    | A high water protection measure is used to control a flood event, which is carried out in the process of high water protection measures implementing                               |
| Flood defense    | A flood defense measure mitigates a flood damage that is produced by a flood event, which is carried out in the process of flood defense measures implementing and uses a resource |
| Evacuation       | An evacuation of the registered victim takes place in the area where the flood occurs and uses a resource, which is carried out in the process of flood evacuation implementing    |

Table 3 Actors and their actions of the flood forecasting concept

| Actions                                                                                                                      | Speech act type                                                                                   | Actor                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Request for weather forecast Receive request Forecast weather Inform weather forecast Accept weather forecast Forecast flood | Coordination act Coordination act Production act Coordination act Coordination act Production act | Flood forecaster Flood forecaster Weather forecaster Weather forecaster Flood forecaster Flood forecaster |

## 4.3    Domain Capture

In this stage, several concepts of the domain identified in the previous stage are organized and represented in conceptual models using conceptual modelling languages. As stated earlier, the domain ontology consists of both endurant and perdurant ontologies. The endurant ontology is modelled and represented in UML class diagrams based on the UFO foundational ontology (a part of UFO-A) by Guizzardi [8], whereas the perdurant ontology is modelled and represented in UML activity diagrams based on the DEMO theory by Dietz [10] and the UML-based DEMO simplified by Colomb and Ahmad [27].

Figure  1  illustrates  endurant  ontology  for  the  flood response domain representing in a UML class diagram. As depicted in this figure, the diagram employs the UML ontological profile by stereotyping classes. This makes explicit the distinction between different types of entities in the ontological sense. For example, the FloodManagementOrganization class is stereotyped SubKind , indicating that it is a rigid subtype of the Organization class. Meanwhile, the FloodForecaster class is stereotyped Role , indicating that FloodForecaster classifies FloodManagementOrganization that is responsible to forecast flood. Therefore, there is a relationship type ' forecast ' and the other class involved this relationship is the FloodForecast class. This approach can achieve expressivity, clarity and truthfulness in representing endurant ontology.

The actions and actors identified in Table 3 are now modelled and represented in a UML activity diagram, using a UML profile-based DEMO proposed by Colomb and Ahmad [27]. The perdurant ontology for flood forecasting and its association with the endurant ontology are shown in Fig. 2.

## 4.4    Implementation

In this stage, the ontology is implemented in OWL and OWL-S using Protégé, 1 a  prominent ontology development tool. For representing the ontology, some classes of the process model in OWL-S are utilized, including Process, Composite Process, Atomic Process, Participant and Result. A coordination act ( C -Act ) in DEMO can be defined as an Atomic Process in OWL-S. A Composite Process is composed of several Atomic Processes , consequently several C -Acts . Therefore, a P -Act in DEMO is defined as A Composite Process in OWL-S, which produces a Result and is composed of several C -Acts . A Subject can play the role of Participant . An institutional fact is seen as a Result produced by a Process . Accordingly, the perdurant ontology based on DEMO can be represented in OWL-S by mapping to these classes and the relevant endurant ontology is represented in OWL. The framework shown in Fig. 3 is representing perdurant ontology and endurant ontology for flood forecasting in OWL-S and OWL (based on the ontology modelled in Fig. 2).

[1 https  ://prote  ge.stanf  ord.edu/.](https://protege.stanford.edu/)

[FIGURE]

Fig. 1 Endurant ontology for the flood response domain

[FIGURE]

## 5    Demonstration of the Ontology Usage

This section demonstrates the usage of the ontology implemented in the previous section. A case study on flood response of Bangkok Metropolis, Thailand, is conducted to illustrate how the ontology can capture common concepts related to flood response management and their relationships. As space in this paper is limited, the demonstration focuses only on the flood forecasting process. In this process, Department of Drainage and Sewage is an actor role responsible for flood forecasting. Information about weather forecasts is needed for flood forecasting, which is provided by Thai Meteorological Department, an actor role responsible for weather forecasting. Once the flood forecasting process is accomplished, information about flood forecasts is produced. During this process, the Bangkok Flood Control Center needs to monitor the coordinated action of the involved organizations in order to ensure that the weather forecasts and flood forecasts are produced on time. Based on the ontological model shown in Fig. 3, a fragment of this ontology is depicted by RDF graph in Fig. 4 and represented in OWL and OWL-S, as shown in Fig. 5 as an example. OWL and OWL-S represent the concepts of endurant and perdurant parts, respectively. For instance, as shown in Fig. 5, the process 'Forecast Weather' (a concept of perdurant part) is captured and represented, which has the relationship performedBy with the instance named 'WeatherFore-caster\_1' of class WeatherForecaster (a concept of endurant part) and the relationship performedWith with the instance named 'FloodForecaster\_1' of class FloodForecaster (a concept of endurant part) and the relationship hasOutput with the instance named 'WeatherForecast\_1' of class WeatherForecast (a concept of endurant part). And, the concept 'Weather Forecast' is captured and represented, which has details about forecasted rainfall and weather forecast time.

[FIGURE]

Fig. 2 Endurant ontology and perdurant ontology for flood forecasting

[FIGURE]

[FIGURE]

As can be seen above, the ontology can be used to represent the concepts related to flood response management and their relationships that a particular case of flood response  management  needs.  Once  all  the  organizations involved map their information to these ontological concepts, it is available to be shared among these organizations.

[FIGURE]

Fig. 3 Perdurant and endurant ontologies implementation framework

Fig. 4 Semantic links between different pieces of information in RDF graph

## 6    Evaluation

In this section, as described earlier, the evaluation is to observe the results of the artifact usage from the demonstration phase, whether it fulfills defined objectives of the proposed ontology. Therefore, the concepts represented in the ontology (shown in the demonstration phase) are evaluated.  This  evaluation  is  conducted  by  means  of one-to-one semi-structured interviews with eight staffs from organizations involved in flood response management in Bangkok metropolitan area, Thailand, including Department of Drainage and Sewage, Thai Meteorological Department, Bangkok Flood Control Center, and Hydro and Agro Informatics Institute, who have expertise and are currently involving in the flood response. The interviewees were asked on their opinion about information represented by the concepts that have been captured and modeled in the ontology. To achieve this objective, the interview questions are adapted from the work of [47], as shown in Table 4, in which information represented by the ontology is evaluated from the aspects of syntactic, semantic and pragmatic. The semi-structured interviews consist of ten open-ended questions based on a set of criteria shown in Table 4. During the interview, the authors recorded the interview conversation and created notes. In analyzing data, interview transcripts and the interview notes were qualitatively analyzed to examine the ontology for its syntactic, semantic and pragmatic qualities.

[FIGURE]

[FIGURE]

[FIGURE]

Fig. 5 Example of the information represented in OWL and OWL-S

Table 4 Criteria for evaluating ontologies (adopted from [47])

| Quality aspect   | Attributes                                       | Description                                                                                                |
|------------------|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Pragmatic        | Completeness Accuracy Coverage                   | Vocabularies needed by a specific application Accuracy of information Overall size of a developed ontology |
| Semantic         | Interpretability Consistency Clarity Correctness | Meaningfulness of terms Consistency of meaning of terms Average number of word senses                      |
| Syntactic        | Richness                                         | Correctness of syntax Breadth of syntax used                                                               |

[FIGURE]

From the syntactic aspect, the evaluation results indicate that the information is represented in a correct syntax. It conforms to the rules of OWL for the concepts of endurant part and of OWL-S the concepts of perdurant part. In terms of richness of syntax used, syntactic vocabularies provided by the ontology are sufficiently rich for representing information. As stated by the interviewee from Thai Meteorological Department who is responsible for weather forecasting, 'it provides various vocabularies to represent information about weather forecast and other relevant information such as forecast weather report, weather state and weather condition. It also provides vocabularies that identify the links between different information sources, for instance, hasForecastWeatherReport that links between the weather forecast information and the weather report information, hasWeatherstate that links between the weather report information and the weather state information, and hasWeatherCondition that links between the weather state information and the weather condition information. This is helpful to manage information and to retrieve the needed information from different information sources.'

From the semantic aspect, the evaluation results show that vocabularies used in the ontology have proper meanings that can be interpreted in the real world and are sharable among organizations involving in the flood response. The interviewees agreed that vocabularies defined have consistent and clear meanings, and used consistently throughout the representation of information, as well as are general and universal terms related to the flood response domain. For instance, as stated by the interviewee from Department of Drainage and Sewage, 'I can understand the meaning of vocabularies that are used to represent the information provided by the Thai Meteorological Department.' Also, the interviewees from Hydro and Agro Informatics Institute, who are responsible for collecting and providing information related to flood response management, stated that the ontology provides an easily understandable meaning to information.

Finally, from the pragmatic aspect, the interviewees agreed that the ontology can represent information that is true in the real world application. In terms of coverage, the ontology is large enough to represent information. As stated by the interviewee from Hydro and Agro Informatics Institute, the ontology provides most terms covering the necessary information used in the domain, although it does not cover all subject areas. However, the interviewee from Bangkok Flood Control Center thinks that the process information represented in the ontology should include more detailed processes. He gave an example of the weather forecast process, which consists of several tasks such as prediction, dissemination and use in decision-making. In this sense, it can be explained that the information captured and represented in the ontology includes only information about essential business actions that produce new fact, not informational actions that produce informational outcomes. In terms of completeness, the interviewees agreed that vocabularies provided by the ontology are complete and meet the requirements for representing, storing and sharing the information.

[FIGURE]

In addition, the interviewees agreed that information representation based on the ontology model has potential to enhance efficient information management and sharing in flood response. It can help to manage the information from different systems in different organizations. The vocabularies provided by the ontology can be used to capture and organize information that is generated from different systems. For example, the flood forecasting task requires several information from heterogeneous sources, some of which are managed by other organizations. Although there exist webbased systems, access to that information still requires a manual process. Often, it requires much time to retrieve and process such information because of the fragmented nature of information related to the flood response. Therefore, once several organizations map their information to the ontology model, such information can be effectively shared and used throughout the entire system of flood response, because of its semantic descriptions provided by the ontology.

## 7    Discussion and Implications

As indicated by the evaluation results, the ontology can capture common concepts related to flood response management and their relationships, which is capable to support information management and sharing. In particular, the ontology gives semantic to information created by different systems in different organizations, which enables more effective management and sharing of such information. Although an application system for automatically managing and sharing information among various information systems of the organizations involved has not been developed in this study, the ontology proposed in this research is important as the initial step toward developing such an application system that employs Semantic Web technology and ontology.

In this paper, the development of an ontology for the flood response domain is presented. The ontology has been designed and developed using foundational ontologies and rooted in the concept of interlocking institutional worlds. Foundational ontologies are formal theories that can be specialized into domain ontologies. Therefore, from a theoretical standpoint, this study represents an attempt to develop domain ontologies by using foundational ontologies and existing theories.

The paper also adds value to practice in the field of flood response. The proposed ontology can be used by the involved organizations to map their information. By committing to this ontology, terms and concepts that represent information are used consistently and unambiguously throughout the entire system of flood response in which several organizations participate. Therefore, this allows to effectively gather information from a heterogeneity of sources and to systematically manage the information as well as to enable the information to be easily shared across multiple organizations. Accordingly, such benefits of the ontology would enhance the current practices of flood response in regard to information management and sharing.

## 8    Conclusion

This paper addresses the problem of information management and sharing in disaster response management. One of the main challenges is due to the large number of heterogeneous concepts used in different organizations. Although these organizations are loosely coupled and autonomous, they interrelate because they collaborate and interoperate for a specific goal. Reducing heterogeneous concepts from different organizations that interoperate at domain level is crucial. This paper presents a new approach on solving problem of information management and sharing using the concept of interlocking institutional worlds (IWs) when designing domain ontology for disaster response management as a kind of domain IWs. By understanding the phenomenon of semantic heterogeneity arise from heterogeneous concepts, the concept of IWs always emphasis on resolving semantic heterogeneity at conceptualization stage before the ontology to be designed (at specification stage). With this key principle applied in our proposed approach actually to limit a number of different heterogeneous concepts to be incorporated in domain ontology specification.

The concept of IWs uses speech act theory as a foundation to present interactions. This conceptual structure of interlocking institutional worlds provides a good metaphysics for organizational interoperation. This metaphysics includes the perdurants and the endurants associated with and created by them. In this paper, the endurant ontology was modelled based on the UFO foundational ontology. For modelling perdurant ontology, the DEMO theory, which is a specialization of the general theory of speech acts, was used as a foundational ontology. The central concept in DEMO is that the stable elements in the description of an organization are the speech acts that organization performs. To make this whole approach work, we show an important demonstration of the utility of our proposed work which is in the expatiation quadrant of the Design Science Research (DSR) methodology on designing our domain ontology for disaster response management which rooted in the concept of IWs.

As there are many types of disasters, the proposed ontology was developed specifically for flood response as a case of disaster response. Therefore, future research can benefit from ontological concepts identified in this research to develop a core ontology for disaster response management that spans across various types of disasters. According to Scherp et al. [48], a core ontology models central and generic concepts that are relevant to a specific field that spans across different domains in this field. This core ontology can be developed in future work by mapping several disaster response domain ontologies to foundational ontologies. In addition, it would be interesting for future research to develop an application system for supporting information management and sharing in flood response, which employs the ontology proposed in this research.

## References

1. Lettieri E, Masella C, Radaelli G (2009) Disaster management: findings from a systematic review. Disaster Prev Manag Int J 18(2):117-136. https  ://doi.org/10.1108/09653  56091  09532  07
2. Mansourian A, Rajabifard A, Valadan Zoej MJ, Williamson I (2006) Using SDI and web-based system to facilitate disaster management. Comput Geosci 32(3):303-315. https  ://doi. org/10.1016/j.cageo  .2005.06.017
3. Li J, Li Q, Liu C, Ullah Khan S, Ghani N (2014) Communitybased collaborative information system for emergency management. Comput Oper Res 42(Supplement C):116-124. https  ://doi. org/10.1016/j.cor.2012.03.018
4. Hristidis V, Chen S-C, Li T, Luis S, Deng Y (2010) Survey of data management and analysis in disaster situations. J Syst Softw 83(10):1701-1714. https  ://doi.org/10.1016/j.jss.2010.04.065
5. Colomb RM, Ahmad MN (2007) Merging ontologies requires interlocking institutional worlds. Appl Ontol 2(1):1-12
6. Hevner AR, March ST, Park J, Ram S (2004) Design science in information systems research. MIS Q 28(1):75-105
7. Peffers K, Tuunanen T, Rothenberger MA, Chatterjee S (2007) A design science research methodology for information systems research. J Manag Inf Syst 24(3):45-77. https  ://doi.org/10.2753/ MIS07  42-12222  40302
8. Guizzardi G (2005) Ontological foundations for structural conceptual models. Ph.D. Thesis, Universiteit Twente, Enschede, The Netherlands
9. Dietz JLG (2001) DEMO: towards a discipline of organisation engineering. Eur J Oper Res 128(2):351-363. https  ://doi. org/10.1016/S0377  -2217(00)00077  -1
10. Dietz JLG (2010) Enterprise ontology: theory and methodology. Springer, Heidelberg
11. UNISDR (2009) UNISDR terminology on disaster risk reduction. http://www.unisd  r.org/we/infor  m/termi  nolog  y2017  . Accessed 15 July 2018
12. Shrubsole D (2007) From structures to sustainability: a history of flood management strategies in Canada. Int J Emerg Manag 4(2):183-196. https  ://doi.org/10.1504/ijem.2007.01398  9

[FIGURE]

13. Ahmad S, Simonovic SP (2006) An intelligent decision support system for management of floods. Water Resour Manag 20(3):391-410. https  ://doi.org/10.1007/s1126  9-006-0326-3
14. Simonović P (1999) Social criteria for evaluation of flood control measures: Winnipeg case study. Urban Water 1(2):167-175. https ://doi.org/10.1016/S1462  -0758(99)00017  -5
15. Gruber TR (1993) A translation approach to portable ontology specifications. Knowl Acquis 5(2):199-220. https  ://doi. org/10.1006/knac.1993.1008
16. Fonseca F, Martin J (2007) Learning the differences between ontologies and conceptual schemas through ontology-driven information systems. J Assoc Inf Syst 8(2):129-142
17. Guarino N (1998) Formal ontology and information systems. In: Proceedings of the formal ontology in information systems (FOIS'98), Trento, Italy, vol 98, pp 81-97
18. Guan J, Levitan AS, Kuhn JR Jr (2013) How AIS can progress along with ontology research in IS. Int J Account Inf Syst 14(1):21-38. https  ://doi.org/10.1016/j.accin  f.2012.08.002
19. Valente A (2005) Types and roles of legal ontologies. In: Benjamins VR, Casanovas P, Breuker J, Gangemi A (eds) Law and the semantic web: legal ontologies, methodologies, legal information retrieval, and applications. Springer, Berlin, pp 65-76
20. Babitski G, Bergweiler S, Grebner O, Oberle D, Paulheim H, Probst F (2011) SoKNOS-using semantic technologies in disaster management software. In: Antoniou G, Grobelnik M, Simperl E, Parsia B, Plexousakis D, De Leenheer P et al (eds) The semanic web: research and applications: 8th extended semantic web conference, ESWC 2011, Heraklion, Crete, Greece, May 29-June 2, 2011, proceedings, part II. Springer, Berlin, pp 183-197
21. de la Asunción M, Castillo L, Fdez-Olivares J, García-Pérez Ó, González A, Palao F (2005) SIADEX: an interactive knowledgebased planner for decision support in forest fire fighting. Ai Commun 18(4):257-268
22. Bénaben F, Hanachi C, Lauras M, Couget P, Chapurlat V (2008) A metamodel and its ontology to guide crisis characterization and its collaborative management. In: Proceedings of the 5th international conference on information systems for crisis response and management (ISCRAM), Washington, DC, USA, May, 2008, pp 4-7
23. Smart PR, Russell A, Shadbolt NR, Shraefel MC, Carr LA (2007) AKTiveSA. Comput J 50(6):703-716. https  ://doi.org/10.1093/ comjn  l/bxm06  7
24. Kalabokidis K, Athanasis N, Vaitis M (2011) OntoFire: an ontology-based geo-portal for wildfires. Nat Hazards Earth Syst Sci 11(12):3157-3170. https  ://doi.org/10.5194/nhess  -11-3157-2011
25. Amailef K, Lu J (2013) Ontology-supported case-based reasoning approach for intelligent m-Government emergency response services. Decis Support Syst 55(1):79-97. https  ://doi.org/10.1016/j. dss.2012.12.034
26. Masolo C, Borgo S, Gangemini A, Guarino N, Oltramari A, Schneider L (2003) The wonderweb library of foundational ontologies and the dolce ontology. Wonderweb deliverable d18, final report (vr. 1.0. 31-12-2003)
27. Colomb RM, Ahmad MN (2010) A perdurant ontology for interoperating information systems based on interlocking institutional worlds. Appl Ontol 5(1):47-77
28. Parreiras  FS,  Staab  S  (2010)  Using  ontologies  with  UML class-based modeling: the TwoUse approach. Data Knowl Eng 69(11):1194-1207. https  ://doi.org/10.1016/j.datak  .2010.07.009
29. Kalibatiene D, Vasilecas O (2011) Survey on ontology languages. In: Grabis J, Kirikova M (eds) Proceedings of the perspectives in business informatics research: 10th international conference, BIR 2011, Riga, Latvia, October 6-8, 2011. Springer, Berlin, pp 124-141
30. W3C (2004c) W3C: RDF/XML syntax specification (Revised). https  ://www.w3.org/TR/2004/REC-rdf-synta  x-gramm  ar-20040 210/2017. Accessed 3 May 2018
31. Schwitter R (2005) A controlled natural language layer for the semantic web. In: Zhang S, Jarvis R (eds) Proceedings of the AI 2005: advances in artificial intelligence: 18th Australian joint conference on artificial intelligence, Sydney, Australia, December 5-9, 2005. Springer, Berlin, pp. 425-434
32. W3C (2004a) OWL web ontology language reference. https  :// www.w3.org/TR/owl-ref/2017. Accessed 3 May 2018
33. W3C (2004b) OWL-S: semantic markup for web services. https ://www.w3.org/Submi  ssion  /OWL-S/2017. Accessed 3 May 2018
34. Corcho O, Fernández-López M, Gómez-Pérez A (2003) Methodologies, tools and languages for building ontologies. Where is their meeting point? Data Knowl Eng 46(1):41-64. https  ://doi. org/10.1016/S0169  -023X(02)00195  -7
35. Iqbal R, Murad MAA, Mustapha A, Sharef NM (2013) An analysis of ontology engineering methodologies: a literature review. Res J Appl Sci Eng Technol 6(16):2993-3000
36. Uschold M, King M (1995) Towards a methodology for building ontologies. Artificial Intelligence Applications Institute, University of Edinburgh, Edinburgh
37. Gomez-Perez A, Fernández-López M, Corcho O (2006) Ontological engineering: with examples from the areas of knowledge management, e-commerce and the semantic web. Springer, New York
38. Guizzardi G, Wagner G (2005) Towards ontological foundations for agent modelling concepts using the unified fundational ontology (UFO). In: Bresciani P, Giorgini P, Henderson-Sellers B, Low G, Winikoff M (eds) Agent-oriented information systems II: 6th international bi-conference workshop, AOIS 2004, Riga, Latvia, June 8, 2004, and New York, NY, USA, July 20, 2004, Revised Selected Papers. Springer, Berlin, pp 110-124
39. Colomb RM (2006) Formal versus material ontologies for information systems interoperation in the semantic web. Comput J 49(1):4-19. https  ://doi.org/10.1093/comjn  l/bxh14  7
40. Colomb RM (2007) Ontology and the semantic web. IOS Press, Amsterdam
41. Guizzardi G (2006) The role of foundational ontologies for conceptual modeling and domain ontology representation. In: 2006 7th International Baltic conference on databases and information systems, pp 17-25. https  ://doi.org/10.1109/dbis.2006.16784  68
42. Gangemi A, Guarino N, Masolo C, Oltramari A, Schneider L (2002) Sweetening ontologies with DOLCE. In: Gómez-Pérez A, Benjamins VR (eds) Knowledge engineering and knowledge management: ontologies and the semantic web. Berlin, Heidelberg, 2002. Springer, Berlin, Heidelberg, pp 166-181
43. Guizzardi G, Wagner G, Almeida JPA, Guizzardi RSS (2015) Towards ontological foundations for conceptual modeling: the unified foundational ontology (UFO) story. Appl Ontol 10(34):259-271. https  ://doi.org/10.3233/ao-15015  7
44. Searle JR (1995) The construction of social reality. The Free Press, New York
45. Hevner A, Chatterjee S (2010) Design research in information systems: theory and practice. Springer, Berlin
46. Mongula DB (2009) Enterprise ontology of the flood control domain. TU Delft, Delft
47. Park J, Cho W, Rho S (2010) Evaluating ontology extraction tools using a comprehensive evaluation framework. Data Knowl Eng 69(10):1043-1061. https  ://doi.org/10.1016/j.datak  .2010.07.002
48. Scherp A, Saathoff C, Franz T, Staab S (2011) Designing core ontologies. Appl Ontol 6(3):177-221

[FIGURE]

Publisher's  Note Springer  Nature  remains  neutral  with  regard  to jurisdictional claims in published maps and institutional affiliations.
