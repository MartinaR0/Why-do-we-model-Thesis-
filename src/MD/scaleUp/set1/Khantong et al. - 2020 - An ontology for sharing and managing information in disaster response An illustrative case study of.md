[FIGURE]

## International Review of Applied Sciences and Engineering

11 (2020) 1, 22-33 DOI: 10.1556/1848.2020.00004

© 2020 The Authors

## CASE STUDY

[FIGURE]

[FIGURE]

*Corresponding author.

E-mail: sommai.k@mbs.msu.ac.th

[FIGURE]

## An ontology for sharing and managing information in disaster response: An illustrative case study of fl ood evacuation

SOMMAI KHANTONG 1 p , MOHAMMAD NAZIR AHMAD SHARIF 2 and AHMAD KAMIL MAHMOOD 3

1 Mahasarakham Business School, Mahasarakham University, Maha Sarakham, Thailand

2 Institute of Industrial Revolution 4.0 (IIR4.0), Universiti Kebangsaan Malaysia, Bangi, Malaysia

3 Computer and Information Sciences Department, Universiti Teknologi PETRONAS, Perak, Malaysia

Received: March 27, 2019 • Accepted: May 20, 2019

Published online: April 18, 2020

## ABSTRACT

Information management and sharing is an essential ingredient, but a difficult and challenging problem for disaster response management. This paper proposes an ontology as a model to organize and structure information in order to improve the information management and sharing in disaster response management. The ontology was designed and developed based on philosophically grounded foundational ontologies. It was also implemented in ontological languages and demonstrated and evaluated in a case study of the flood evacuation process. This paper also provides a systematic approach to develop a well-founded domain ontology that addresses both static and dynamic aspects of a given domain.

## KEYWORDS

disaster management, flood response, ontology, domain ontology, information management and sharing

## 1. INTRODUCTION

Information management and sharing is essential in disaster management, especially in the response phase. For instance, during a disaster, the responders need to be able to share and use realtime information in order to carry out disaster relief operations [1]. Accordingly, the information management and sharing is considered as a key element of disaster response research [2]. In the disaster response, several organizations are typically required to cooperate with each other [3, 4], and a huge amount of information is generated and used by different processes handled by different systems in these different organizations [5]. The information generated in one process needs to be shared with other relevant processes that may be performed by different systems in different organizations, and the information collection, storage and queries must be performed on an urgent basis. However, managing and sharing of such information is challenging. The disaster-related information is dif fi cult to manage due to its large amount and diversity as well as geographical distribution [5]. In addition, the information generated from different systems and represented in heterogeneous formats cannot be easily shared with others because of syntactic and semantic heterogeneity [6]. These challenges require us to rethink how to manage all the processes and related information created by these processes most effectively and to make them be easily shared among participating organizations.

One way to improve the efficiency and effectiveness of information management and sharing is to use ontologies, which have been applied in several domains [e.g., 7 -9]. To our knowledge, however, although there are ontologies developed in the domain of disaster response, none of them is developed speci fi cally for the purpose of information management and sharing. In addition, they address the static aspect of the domain only, while ignoring the dynamic aspect. However, the central concept of disaster response is that it involves many processes conducted by several organizations, cooperating with each other. In this regard, dynamic concepts, such as actions or processes, also need to be conceptualized in order to manage and share dynamic or process information within the domain. Accordingly, the paper aims to develop an ontology to support information management and sharing in the disaster response process, which addresses both static and dynamic aspects of the domain. More speci fi cally, the proposed ontology serves as a model to manage the different pieces of information that are created by different processes handled by different organizations, as well as to structure the information in order to enable it to be shared among the organizations.

In this paper, the research method used is based on the design science paradigm in IS research [10, 11]. The design science is a problem solving paradigm, aiming to build new artefacts in order to improve or extend the capabilities of humans and organizations [11]. The ontology proposed in this paper is a design artefact in the form of model according to the design science concept. It is designed and developed based on philosophically grounded foundational ontologies, UFO [12] and DEMO [13, 14], and rooted in the concept of interlocking institutional worlds [15].

The rest of this paper is organized as follows. Section 2 presents background and reviews ontologies developed in the area of disaster response management. Section 3 describes the research methodology used. In Section 4, the development of disaster response domain ontology is presented. The ontology usage is demonstrated in Section 5 and evaluated in Section 6. Section 7 discusses implications of the research. The paper is concluded in the fi nal section.

## 2. BACKGROUND AND LITERATURE REVIEW

## 2.1. Disaster response management

Disasters can be categorized into three groups by the origin of their hazards, namely, man-made, natural and technological disasters [4]. Among these kinds of disasters, natural disasters have a large impact in terms of human distress, property losses, and economic damages. The paper specifically focuses on the fl ood as an example of natural disasters.

Typically, the response to disasters consists of actions to manage and control the various effects of disaster (also the ripple effects) and minimize human and property losses [3]. In fl ood management, according to [16], the response phase deals with operations that are directed at managing the consequences of an imminent fl ood even before the actual fl ood has occurred. Therefore, the fl ood response is not only performed during the actual fl ood, but also during an imminent fl ood. It is comprised of several processes, including fl oods forecasting, fl ood forecasts updating, the current fl ood situation assessment, fl ood control operation and evacuation [17, 18].

## 2.2. Ontology

Ontology is originally a philosophy term, and has become a relevant word of information systems and computing disciplines. In the computational perspective, as defined by [19], an ontology is ' a formal explicit speci fi cation of a shared conceptualization for a domain of interest. ' It is an engineering artifact that represents a speci fi c domain of knowledge [20, 21]. The ontology is concerned with representing and understanding a speci fi c domain [22]. Therefore, it aims to represent a description of conceptualization of reality in a speci fi c domain, which consists of concepts and relationships between these concepts.

Ontologies are developed and represented in different levels of abstraction. Accordingly, ontologies can be represented by different formalisms and languages, depending on their objective. Reference [20] classi fi es ontologies based on the level of abstraction they represent as follows: top-level ontologies, domain ontologies, task ontologies, and application ontologies. The top-level ontologies (also known as foundational ontologies) are more general and can be specialized into a domain ontology or a task ontology.

Typically, ontology development is not a goal in itself. Over several decades, ontologies have been developed for different objectives of usage and used in a variety of domains. As reviewed by [23], the main uses of ontologies are for semantic indexing and search, information organization and structuring, problem solving and reasoning, understanding the domain, and semantics interoperation. In this paper, the main use of ontology is to structure and organize information in order to support information management and sharing.

2.2.1. Ontologies related to disaster response management. A variety of ontologies have been developed to apply in various phase of disaster management. However, this section focuses only on the ontologies that are related to the response phase. In [24], an ontology was developed within the SoKNOS project, speci fi cally aimed at integrating information from heterogeneous organizations for resource planning in disaster response. Reference [25] proposed SIADEX ontology for process planning under uncertainty for decision support during a disaster. It serves as a knowledge base that provides knowledge required in the planning process. Reference [26] proposed the ISyCri ontology for disaster response coordination management. In [27], many domain-relevant ontologies were developed for the AKTiveSA system, including Geography, Transportation, Meteorology, Humanitarian aid, Military, Equipment, Organizations, and Weapons. These ontologies are designed for enhancing situation awareness within a speci fi c context of humanitarian and disaster relief operations. Reference [28] proposed an ontology, named OntoFire, which is developed speci fi cally for the wild fi res domain, with the aim to improve information retrieval mechanisms of geo-portals by enabling a semantic-based search for geoinformational resources of interest. Reference [29] proposed a case attribute domain ontology which is used to support case-based reasoning approaches in order to improve the ef fi ciency and effectiveness of decision making in responding to a disaster situation.

[FIGURE]

As discussed above, ontologies developed for disaster response mostly play a role of a knowledge base that could be used to support some disaster response functions, and are used for the purpose of information integration. There is no study that develops an ontology specifically for the purposes of information management and sharing in the disaster response process, especially in flood management. In addition, currently, a few ontologies related to disaster response are grounded in foundational ontologies. Furthermore, the ontologies discussed above address the static aspect of the domain only, while ignoring the dynamic aspect. They model only static concepts. Although some ontologies include the concepts about the process, they do not model the sequencing of process-oriented concepts explicitly. However, ontology for the disaster response domain needs to take both static and dynamic aspects of the domain into consideration. In flood response, for example, simple static concepts are weather forecast, flood forecast, flood, area, evaluation, etc. It also includes process-oriented concepts such as weather forecasting, flood forecasting, evacuation implementing and so on. Each of these processes may consist of sub-processes performed by different organizations.

In this paper, the main use of ontology is to organize and structure information related to flood response in order to improve the information management and sharing. By using the ontology, syntax and semantics are defined to describe the information explicitly. As discussed in [30], compared to other information modeling methodologies, the use of ontology has some similarities but also some distinct differences. Similar to databases, ontologies can be used by application software at run-time for queries and reasoning, on the other hand, relationships de fi ned in ontologies are fi rst-class constructs. Compared to object models, both of them describe classes and attributes, but ontologies are setbased and dynamic. This ontology is categorized as a domain ontology. The target domain is that of disaster response. However, since there are many types of disasters, this ontology is developed speci fi cally for fl ood response as a case of disaster response.

2.2.2. The role of foundational ontology in domain ontology development. Any domain ontology can be developed based on the concepts provided by the foundational ontology [31]. The use of foundation ontology is to organize the ' things ' that exist in a given domain so that the domain ontology is well-structured and is application independent [32]. According to [33], the use of foundation ontologies has signi fi cant bene fi ts in developing domain ontologies. Foundational ontologies can help ontology developers to design and understand the domain by providing a rich vocabulary that describes that domain. In addition, domain ontologies developed based on foundational ontologies can achieve interoperability and a higher overall quality [12, 20, 34].

[FIGURE]

Various foundational ontologies have been proposed. DOLCE [35] is one of the most prominent and in fl uential upper ontologies in domain ontology development. DOLCE distinguishes entities into two main types, namely, perdurants and endurants. An endurant is de fi ned as an entity that exists in a timeless way. All of its parts exist at the same time. A perdurant is de fi ned as an entity that happens in time. If it has parts, it has temporal parts that happen at different times. In addition, perdurants can be divided into two kinds, namely, statives and events. An event is an essential whole. All of its parts are necessary. A stative is not an essential whole.

In order to represent the endurant ontology, in this paper, the Unified Foundational Ontology (UFO) by [12] is selected as it is a well-founded philosophically foundational ontology and has been widely used in developing domain ontologies in a variety of domains [36, 37]. In particular, UFO combines DOLCE and BWW foundational ontologies, which extends the endurant ontology by articulating the concept of class into a system of kinds of classes, including Kind , Subkind , Category , Phase , Role and so on. These more speci fi c concepts can be used in developing a domain ontology to avoid a number of anomalies in the domain ontology being developed, especially involving the identity of individuals [12].

For representing the perdurant part of domain ontology, a set of concepts based on the concepts of speech act can form a useful foundational ontology [38]. However, the general theory of speech acts covers a wide spectrum of phenomena. It would be useful to have a specialization of the general theory of speech acts directed towards information systems. In this sense, the DEMO theory [13, 14] is prominent since it has been developed and used as a means for enterprise modeling and information systems engineering in several domains [39]. DEMO recognizes that a speech act performed as an item of business is generally a complex action. A business act is a type of speech act called a production act or P-act . This is the ontologically stable aspect of an organization. A P-act is generally performed as the result of a conversation among several parties. Each step in the conversation is another type of speech act called a coordination act or C-act . The C-acts producing a P-act are packaged in a transaction. The P-act is made only if the transaction completes. The C-acts are subject to change, even though the P-act remains stable. These actions are performed by subjects playing roles, or actors. A subject is a person or organization capable of taking responsibility.

The endurant and perdurant represent the static aspect and the dynamic aspect of the domain, respectively. The representations of endurant and perdurant ontologies described above provide a useful way to develop our domain ontology that is well-founded, using philosophically grounded foundational ontologies. It can help to promote quality of the domain ontology and achieve interoperability of systems that rely on this ontology.

## 3. RESEARCH METHODOLOGY

In this paper, Design Science Research (DSR) methodology is adopted as the research methodology. DSR has attracted increasing attention to the research community of information systems (IS). Within the IS discipline, DSR has enabled the development of novel IT artifacts, organizational development, and theory building [40]. It concerns designing novel and innovative artifacts to support organizational and human purposes, which is different from natural science research that mainly aims to understand reality in order to predict or explain organizational or human behavior and thus producing theoretical knowledge [11]. According to the design science concept, the ontology proposed in this research is an artefact in the form of model.

Several scholars have proposed guidelines or methodologies for conducting DSR in the IS research. The paper follows the DSR methodology proposed Peffers, et al. [10], which consists of six stages as follows:

## 3.1. Problem identification and motivation

The main activity of this stage is to determine the specific problem and justify the value of a solution to the problem. As discussed in Section 1, the problem identi fi ed in this study is about the information management and sharing in disaster response. It is a challenging issue to manage and share information in the disaster response context, due to the large amount and diversity of information and syntactic and semantic heterogeneity of the information. In this paper, an ontology is proposed as a solution. At the best of our knowledge, this ontology is a novel contribution in the fi eld of ontology applications in the disaster management area, in the speci fi c context of fl ood management, which aims to support the information management and sharing, and addresses both static and dynamic aspects of the domain.

## 3.2. Definition of the objectives of a solution

In this stage, the main activity is to infer the objectives of a solution from the problem definition. In this paper, the desirable objectives of the ontology are to model both static and dynamic aspects of the domain and to be used as a model to organize and structure the different pieces of information that are created by different organizations in different processes of disaster response management as well as to define semantics for such information explicitly.

## 3.3. Design and development

The activity in this stage is to describe the artifact design and development, showing how it is designed and developed. In building the ontology, the concept of interlocking institutional worlds is utilized as a conceptual framework to discover specific concepts of the domain. These concepts of the domain are modeled at the conceptual level, using UML notation. Endurant ontology was modeled by UML class diagrams based on the UFO (Unified Foundational Ontology) foundational ontology [12], whereas perdurant ontology was modeled by UML activity diagrams based on the theory of DEMO (Design and Engineering Methodology for Organizations) [13, 14], simpli fi ed by UML-based DEMO [38]. These conceptual models of the ontology are then transformed to be represented in the ontology implementation languages. By using the Prot  eg  e tool, the endurant ontology was represented in OWL and the perdurant ontology was represented in OWL-S. All of these are presented in detail in Section 4.

## 3.4. Demonstration

The main activity in this phase is to demonstrate the utility of the artifact in an illustrative or real-life case. The artifact can demonstrate its usage by means of simulation, experimentation, prototype, case study or others. In this study, the utility of the proposed ontology is demonstrated in a case study. This is presented in detail in Section 5.

## 3.5. Evaluation

In this phase, the artifact is evaluated to verify that it fulfills the defined objectives. The activity of evaluation is to compare the defined objectives of a solution with the results of the usage of the artifact observed from the demonstration phase. In this study, the evaluation is done by means of semi-structure interviews with practitioners in flood response. See section 6 for more details.

## 3.6. Communication

In this phase, the problem and its importance as well as the proposed artifact, its utility and novelty, the rigorousness of its design and its effectiveness are communicated to the relevant research audience, e.g. in the form of academic write-ups, such as this paper.

## 4. DESIGN AND DEVELOPMENT OF THE ONTOLOGY

The ontology development methodology used in this paper is based on the methodologies by [41] and by [42], consisting of four stages as follows.

## 4.1. Ontology purpose and scope

The main purpose of the ontology is to be used as a model to organize and structure information that can be shared among participating organizations. The intended users of the ontology are flood response stakeholders. In addition, the ontology is constrained to cover only the response phase of flood management. As discussed in Section 2.1, fl ood response management is comprised of many processes. However, the paper contains only some key processes, including fl ood prediction, fl ood control, fl ood defense and evacuation.

[FIGURE]

Table 1. The relevant concepts of the fl ood response domain

| Process          | Action-oriented concepts                    | Static concepts                                             |
|------------------|---------------------------------------------|-------------------------------------------------------------|
| Flood prediction | Flood forecasting                           | Flood forecast, Weather forecast, Flood event, Area         |
| Flood control    | High water protection measures implementing | High water protection measures                              |
| Flood defense    | Flood defense measures implementing         | Flood damage, Flood defense measures, Resource              |
| Evacuation       | Flood evacuation implementing               | Flood evacuation, Victim, Evacuation registration, Resource |

## 4.2. Domain conceptualization

In this paper, the domain of disaster response is seen as a domain of interlocking institutional worlds introduced by [15], in which several organizations (institutions) interoperate by interlocking their worlds. In the institutional world, institutional facts are created, destroyed and manipulated by speech acts, which are formal declarations by designated of fi cials of institutions. A speech act is a special type of action. Therefore, the sorts of entities that exist in the institutional worlds include institutional facts, speech acts and actor-roles that perform the speech acts. Institutional facts and actor-roles are static concepts, while speech acts are action-oriented concepts. Therefore, in the case of fl ood response, the relevant concepts can be identi fi ed as shown in Table 1. Some of these concepts are adapted from the work of [43]. The relationships among the concepts are determined as shown in Table 2.

After identifying the relevant concepts and their relationships, the actors involved and their actions in each of the action-oriented concepts are determined. These actions are speech acts that are performed by authorized actors. The speech acts can be categorized into coordination and production acts [15]. Because of the space limitation, only actors and their actions involved in the concept of fl ood evacuation implementing are presented as shown in Table 3.

Table 2. Key concepts and relationships among them

| Process          | Keys concepts and relationships                                                                                                                                                        |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flood prediction | A fl ood forecast uses weather forecast to predict a fl ood event that will occur in a speci fi c area, which is carried out in the process of fl ood forecasting.                     |
| Flood control    | A high water protection measure is used to control a fl ood event, which is carried out in the process of high water protection measures implementing                                  |
| Flood defense    | A fl ood defense measure mitigates a fl ood damage that is produced by a fl ood event, which is carried out in the process of fl ood defense measures implementing and uses a resource |
| Evacuation       | An evacuation of the registered victim takes place in the area where the fl ood occurs and uses a resource, which is carried out in the process of fl ood evacuation implementing.     |

[FIGURE]

## 4.3. Domain capture

In this stage, several concepts of the domain identified in the previous stage are organized and represented in conceptual models using conceptual modeling languages. As stated earlier, the domain ontology consists of both endurant and perdurant ontologies. The endurant ontology is modeled and represented in UML class diagrams based on the UFO foundational ontology (a part of UFO-A) by [12], whereas the perdurant ontology is modeled and represented in UML activity diagrams based on the DEMO theory by [14] and the UML-based DEMO simpli fi ed by [38].

Figure 1 illustrates endurant ontology for the fl ood response domain represented in a UML class diagram. As depicted in this fi gure, the diagram employs the UML ontological pro fi le by stereotyping classes. This makes explicit the distinction between different types of entities in the ontological sense. For example, the FloodManagementOrganization class is stereotyped SubKind , indicating that it is a rigid subtype of the Organization class. Meanwhile, the FloodForecaster class is stereotyped Role , indicating that FloodForecaster classi fi es FloodManagementOrganization that is responsible to forecast fl ood. Therefore, there is a relationship type ' forecast ' and the other class involved in this relationship is the FloodForecast class. This approach can achieve expressivity, clarity and truthfulness in representing endurant ontology. The actions and actors identi fi ed in Table 3 are now modeled and represented in a UML activity diagram, using a UML pro fi le based DEMO proposed by [38]. The perdurant ontology for fl ood evacuation implementing and its association with the endurant ontology are shown in Fig. 2.

Table 3. Actors and their actions of fl ood evacuation implementing concept

| Actions                                | Speech act type   | Actor                        |
|----------------------------------------|-------------------|------------------------------|
| Request to implement fl ood evacuation | Informative       | Flood evacuation manager     |
| Receive request                        | Informative       | Flood evacuation implementer |
| Make fl ood evacuation plan            | Performative      | Flood evacuation implementer |
| Propose fl ood evacuation plan         | Informative       | Flood evacuation implementer |
| Approve fl ood evacuation plan         | Informative       | Flood evacuation manager     |
| Implement fl ood evacuation            | Performative      | Flood evacuation implementer |

Figure 1. Endurant ontology for the fl ood response domain

[FIGURE]

## 4.4. Implementation

In this stage, the ontology is implemented in OWL and OWL-S using Prot  eg  e, a prominent ontology development tool. For representing the ontology, some classes of the process model in OWL-S are utilized, including Process, Composite Process, Atomic Process, Participant, and Result. A coordination act ( C-Act ) in DEMO can be de fi ned as an Atomic Process in OWL-S. A Composite Process is composed of several Atomic Processes , consequently several C-Acts . Therefore, a P-Act in DEMO is de fi ned as A Composite Process in OWL-S, which produces a Result and is composed of several C-Acts . A Subject can play the role of Participant . An institutional fact is seen as a Result produced by a Process . Accordingly, the perdurant ontology based on DEMO can be represented in OWL-S by mapping to these classes and the relevant endurant ontology is represented in OWL. The framework shown in Fig. 3 is representing perdurant ontology and endurant ontology for fl ood evacuation implementing in OWL-S and OWL (based on the ontology modeled in Fig. 2).

## 5. DEMONSTRATION OF THE ONTOLOGY USAGE

This section demonstrates the usage of the ontology implemented in the previous section. A case study on flood response of Maha Sarakham province, Thailand is conducted to illustrate how the ontology is applicable to organize and structure information that can be shared among participating organizations. The demonstration focuses only on the information relevant to the flood evacuation implementing process. In this process, municipalities in the flooded area are actors responsible for flood evacuation implementing. Information about evacuation plans is needed for flood evacuation implementing, which is approved by Maha Sarakham Disaster Prevention and Mitigation Office. Once the flood evacuation implementing process is accomplished, information about implemented flood evacuation is produced. During this process, the Maha Sarakham Disaster Prevention and Mitigation Office needs to monitor the coordinated action of the involved organizations in order to ensure that the flood evacuation is implemented on time. Based on the ontological model shown in Fig. 3, these information sources are structured and organized, which can be depicted by RDF graph in Fig. 4 and represented in OWL and OWL-S, as shown in Fig. 5 as an example.

[FIGURE]

Figure 2. Endurant and perdurant ontologies for fl ood evacuation implementing. (A) Perdurant ontology for fl ood evacuation implementing, (B) Endurant ontology for fl ood evacuation implementing

[FIGURE]

[FIGURE]

[FIGURE]

Figure 3. Perdurant and endurant ontologies implementation framework

[FIGURE]

## 6. EVALUATION

In this section, the information that was organized and structured in the ontology is evaluated. This evaluation is conducted by means of semi-structured interviews with practitioners in flood response of Maha Sarakham province, Thailand. The interviewees were asked to give their opinion about the information structured and organized in the ontology as well as its usefulness for the purpose of information management and sharing. The interview questions are adapted from the work of [44], in which the ontology is evaluated from the aspects of syntactic, semantic and pragmatic.

From the syntactic aspect, the evaluation results indicate that the vocabularies provided by the ontology are sufficient to represent information about the flood evacuation implementation. There are also vocabularies identifying the links between different pieces of information. This is helpful to manage information and to retrieve the needed information. From the semantic aspect, the evaluation results show that vocabularies defined in the ontology have consistent and clear meanings and used consistently. Finally, from the pragmatic aspect, the ontology can represent information that is true in the real word application. In terms of completeness, vocabularies provided by the ontology are complete and meet the requirements for representing, storing and sharing the information. However, interviewees stated that the information about flood evacuation plan is likely to be incomplete, as the flood evacuation plan is not detailed enough to meet their needs. In this sense, it can be explained that the ontology can be extended, either by adding new classes or by inserting new attributes or relationships into existing classes in the future based on the requirements of users.

In addition, all interviewees agreed that information representation based on the ontology model has the potential to enhance efficient information management and sharing in flood response. It can help to manage the information from different systems in different organizations. The ontology is useful to support information management and sharing in flood response management. In particular, when information represented in ontology is machine interpretable, different systems would share the information with each other easily and automatically. Currently, there is no online information exchange between organizations in flood response management in Maha Sarakham province. Typically, the information is obtained and exchanged by phone, fax or e-mail. Therefore, they think that information systems to support information management and sharing in flood response management can take advantage of ontology ' s ability to represent information.

[FIGURE]

Figure 4. Semantic links between different pieces of information in RDF graph

[FIGURE]

## 7. DISCUSSION AND IMPLICATIONS

As indicated by the evaluation results, the ontology is useful to structure and represent the information that needs to be shared among different organizations involved in disaster response. It can be used as a model to organize and structure both static and dynamic information. A controlled vocabulary provided by the ontology could be used to represent the information that meets quality requirements in terms of syntactic, semantic, and pragmatic aspects. In particular, the ontology gives semantic to information created by different systems in different organizations, which enables more effective management and sharing of such information. Although an application system for automatically managing and sharing information among various information systems of the organizations involved has not been developed in this study, the ontology proposed in this research is important as the initial step toward developing such an application system that employs Semantic Web technology and ontology.

[FIGURE]

In the paper, the development of an ontology for the flood response domain is presented. The ontology has been designed and developed using foundational ontologies and rooted in the concept of interlocking institutional worlds. Foundational ontologies are formal theories that can be specialized into domain ontologies. Therefore, from a theoretical standpoint, this study represents an attempt to develop domain ontologies by using foundational ontologies and existing theories. More specifically, it describes a systematic approach to develop a well-founded domain ontology that addresses both the static and dynamic aspects of a given domain, while other studies on ontology development have addressed only the static aspect.

The paper also adds value to practice in the field of flood response. The proposed ontology can be used as a model to structure and organize information. By committing to this ontology, terms and concepts that represent information are used consistently and unambiguously throughout the entire system of flood response in which several organizations participate. Therefore, this allows to effectively gather information from a heterogeneity of sources and to systematically manage the information as well as to enable the information to be easily shared across multiple organizations. Accordingly, such benefits of the ontology would enhance the current practices of flood response with regard to information management and sharing.

Figure 5. An example of OWL and OWL-S representations

## 8. CONCLUSION

This paper addresses the problem of information management and sharing in disaster response management. The ontology is proposed as a model to organize and structure information in order to improve the information management and sharing in disaster response. The ontology usage is demonstrated in a case study and evaluated through interviews with practitioners involved in flood management of Maha Sarakham province, Thailand. The evaluation showed that the ontology was perceived as useful in supporting the information management and sharing in flood response.

The ontology developed in this study was designed and developed by using foundational ontologies that provide real-world semantics. The endurant ontology was modeled based on the UFO foundational ontology. For modeling perdurant ontology, the DEMO theory, which is a specialization of the general theory of speech acts, was used as a foundational ontology. The central concept in DEMO is that the stable elements in the description of an organization are the speech acts that the organization performs. The foundational ontologies utilized in this research provide a rich vocabulary to describe the domain from both static and dynamic aspects.

As there are many types of disasters, the proposed ontology was developed specifically for flood response as a case of disaster response, and demonstrated in the process of flood evacuation implementation. Therefore, future research can benefit from ontological concepts identified in this research to develop a core ontology for disaster response management that spans across various types of disasters. According to [45], a core ontology models central and generic concepts that are relevant to a speci fi c fi eld that spans across different domains in this fi eld. This core ontology can be developed in future work by mapping several disaster response domain ontologies to foundational ontologies. In addition, it would be interesting for future research to develop an application system for supporting information management and sharing in fl ood response, which employs the ontology proposed in this research.

[FIGURE]

## REFERENCES

- [1] M. M. Ra fi , T. Aziz, and S. H. Lodi, ' A comparative study of disaster management information systems, ' Online Inf. Rev. , vol. 42, no. 6, pp. 971-988, 2018.
- [2] M. Janssen, J. Lee, N. Bharosa, and A. Cresswell, ' Advances in multi-agency disaster management: Key elements in disaster research, ' Inf. Syst. Front. , vol. 12, no. 1, pp. 1-7, 2010.
- [3] E. Lettieri, C. Masella, and G. Radaelli, ' Disaster management: fi ndings from a systematic review, ' Disaster Prev. Manag.: An Int. J. , vol. 18, no. 2, pp. 117 -136, 2009.
- [4] A. Mansourian, A. Rajabifard, M. J. Valadan Zoej, and I. Williamson, ' Using SDI and web-based system to facilitate disaster management, ' Comput. Geosci. , vol. 32, no. 3, pp. 303-315, 2006.
- [5] J. Li, Q. Li, C. Liu, S. Ullah Khan, and N. Ghani, ' Communitybased collaborative information system for emergency management, ' Comput. Oper. Res. , vol. 42, no. Supplement C, pp. 116 -124, 2014.
- [6] V. Hristidis, S.-C. Chen, T. Li, S. Luis, and Y. Deng, ' Survey of data management and analysis in disaster situations, ' J. Syst. Software , vol. 83, no. 10, pp. 1701 -1714, 2010.
- [7] Q. Wang, J. Wu, Y. Dong, and J. Wang, ' Ontology-based design and information sharing for medical information, ' in 2010 IEEE International Conference on Software Engineering and Service Sciences , 2010, pp. 663 -666.
- [8] D. Ruikar, C. J. Anumba, A. Duke, P. M. Carrillo, and N. M. Bouchlaghem, ' Using the semantic web for project information management, ' Facilities , vol. 25, no. 13/14, pp. 507 -524, 2007.
- [9] K.-Y. Kim, D. G. Manley, and H. Yang, ' Ontology-based assembly design and information sharing for collaborative product development, ' Comput. Aided Des. , vol. 38, no. 12, pp. 1233 -1250, 2006.
- [10] K. Peffers, T. Tuunanen, M. A. Rothenberger, and S. Chatterjee, ' A Design Science Research Methodology for Information Systems Research, ' J. Inf. Syst. Manag. , vol. 24, no. 3, pp. 45 -77, 2007.
- [11] A. R. Hevner, S. T. March, J. Park, and S. Ram, ' Design Science in Information Systems Research, ' MIS Q. , vol. 28, no. 1, pp. 75 -105, 2004.
- [12] G. Guizzardi, ' Ontological Foundations for Structural Conceptual Models, ' Ph.D. Thesis Enschede, The Netherlands, Universiteit Twente, 05 -74, 2005.
- [13] J. L. G. Dietz, ' DEMO: Towards a discipline of organisation engineering, ' Eur. J. Oper. Res. , vol. 128, no. 2, pp. 351 -363, 2001.
- [14] J. L. G. Dietz, Enterprise Ontology: Theory and Methodology . Heidelberg: Springer Publishing Company, Incorporated, 2010, p. 244.
- [15] R. M. Colomb and M. N. Ahmad, ' Merging ontologies requires interlocking institutional worlds, ' Appl. Ontol. , vol. 2, no. 1, pp. 1 -12, 2007.
- [16] D. Shrubsole, ' From structures to sustainability: a history of fl ood management strategies in Canada, ' Int. J. Emerg. Manag. , vol. 4, no. 2, pp. 183 -196, 2007.
- [17] S. Ahmad and S. P. Simonovic, ' An Intelligent Decision Support System for Management of Floods, ' Water Resour. Manag. journal article , vol. 20, no. 3, pp. 391 -410, 2006.
- [18] S. P. Simonovi  c, ' Social criteria for evaluation of fl ood control measures: Winnipeg case study, ' Urban Water , vol. 1, no. 2, pp. 167 -175, 1999.
- [19] T. R. Gruber, ' A translation approach to portable ontology speci fi cations, ' Knowl. Acquis. , vol. 5, no. 2, pp. 199 -220, 1993.
- [20] N. Guarino, ' Formal ontology and information systems, ' in Proceedings of the Formal Ontology in Information Systems (FOIS ' 98) , Trento, Italy, 1998, vol. 98, no. 1998, pp. 81 -97.
- [21] F. Fonseca and J. Martin, ' Learning the differences between ontologies and conceptual schemas through ontology-driven information systems, ' J. Assoc. Inf. Syst. , vol. 8, no. 2, pp. 129 -142, 2007.
- [22] J. Guan, A. S. Levitan, and J. R. Kuhn, Jr, ' How AIS can progress along with ontology research in IS, ' IInt. J. Account. Inf. Syst. , vol. 14, no. 1, pp. 21 -38, 2013.
- [23] A. Valente, ' Types and Roles of Legal Ontologies, ' in Law and the Semantic Web: Legal Ontologies, Methodologies, Legal Information Retrieval, and Applications , V. R. Benjamins, P. Casanovas, J. Breuker, and A. Gangemi, Eds., Berlin, Heidelberg: Springer Berlin Heidelberg, 2005, pp. 65 -76.
- [24] G. Babitski, S. Bergweiler, O. Grebner, D. Oberle, H. Paulheim, and F. Probst, ' SoKNOS -Using Semantic Technologies in Disaster Management Software, ' in The Semanic Web: Research and Applications: 8th Extended Semantic Web Conference, ESWC 2011, Heraklion, Crete, Greece, May 29 -June 2, 2011, Proceedings, Part II , G. Antoniou, et al., Eds., Berlin, Heidelberg: Springer Berlin Heidelberg, 2011, pp. 183 -197.
- [25] M. de la Asunci  on, L. Castillo, J. Fdez-Olivares, Ó. Garc  ı a-P  erez, A. Gonz  alez, and F. Palao, ' SIADEX: An interactive knowledgebased planner for decision support in forest fi re fi ghting, ' AI Commun. , vol. 18, no. 4, pp. 257 -268, 2005.
- [26] F. B  enaben, C. Hanachi, M. Lauras, P. Couget, and V. Chapurlat, ' A metamodel and its ontology to guide crisis characterization and its collaborative management, ' in Proceedings of the 5th International Conference on Information Systems for Crisis Response and Management (ISCRAM) , Washington, DC, USA, May, 2008, pp. 4 -7.
- [27] P. R. Smart, A. Russell, N. R. Shadbolt, M. C. Shraefel, and L. A. Carr, ' AKTiveSA, ' Comput. J., vol. 50, no. 6, pp. 703 -716, 2007.
- [28] K. Kalabokidis, N. Athanasis, and M. Vaitis, ' OntoFire: an ontology-based geo-portal for wild fi res, ' Nat. Hazards Earth Syst. Sci. , vol. 11, no. 12, pp. 3157 -3170, 2011.
- [29] K. Amailef and J. Lu, ' Ontology-supported case-based reasoning approach for intelligent m-Government emergency response services, ' Decision Support Syst. , vol. 55, no. 1, pp. 79 -97, 2013.
- [30] V. Venkatasubramanian, C. Zhao, G. Joglekar, et al., ' Ontological informatics infrastructure for pharmaceutical product development and manufacturing, ' Computers &amp; Chemical Engineering , vol. 30, no. 10, pp. 1482 -1496, 2006.
- [31] G. Guizzardi and G. Wagner, ' Towards Ontological Foundations for Agent Modelling Concepts Using the Uni fi ed Fundational Ontology (UFO), ' in Agent-Oriented Information Systems II: 6th International Bi-Conference Workshop, AOIS 2004, Riga, Latvia,

[FIGURE]

- June 8, 2004, and New York, NY, USA, July 20, 2004 , Revised Selected Papers , P. Bresciani, P. Giorgini, B. Henderson-Sellers, G. Low, and M. Winikoff, Eds., Berlin, Heidelberg: Springer Berlin Heidelberg, 2005, pp. 110 -124.
- [32] R. M. Colomb, ' Formal versus Material Ontologies for Information Systems Interoperation in the Semantic Web, ' Comput. J., vol. 49, no. 1, pp. 4 -19, 2006.
- [33] R. M. Colomb, Ontology and the Semantic Web . IOS Press, 2007.
- [34] G. Guizzardi, ' The role of foundational ontologies for conceptual modeling and domain ontology representation, ' in 2006 7th International Baltic Conference on Databases and Information Systems, 2006, pp. 17 -25.
- [35] C. Masolo, S. Borgo, A. Gangemini, N. Guarino, A. Oltramari, and L. Schneider, ' The wonderweb library of fundational ontologies and the dolce ontology, ' in Wonderweb deliverable d18, fi nal report (vr. 1.0. 31-12-2003), 2003.
- [36] G. Guizzardi, G. Wagner, J. P. A. Almeida, and R. S. S. Guizzardi, ' Towards ontological foundations for conceptual modeling: The uni fi ed foundational ontology (UFO) story, ' Applied Ontology , vol. 10, no. 3 -4, pp. 259 -271, 2015.
- [37] M. Verdonck, F. Gailly, R. Pergl, G. Guizzardi, B. Martins, and O. Pastor, ' Comparing traditional conceptual modeling with ontology-driven conceptual modeling: An empirical study, ' Inf. Syst. , vol. 81, pp. 92 -103, 2019.
- [38] R. M. Colomb and M. N. Ahmad, ' A perdurant ontology for interoperating information systems based on interlocking institutional worlds, ' Appl. Ontol. , vol. 5, no. 1, pp. 47 -77, 2010.
- [39] R. Laleh and P. Geert, ' Service-oriented enterprise engineering: A modeling discipline based on the viable systems approach (vSa) for strategic sourcing decision-making, ' Int. J. Inf. Syst. Serv. Sect. (IJISSS) , vol. 10, no. 3, pp. 20 -40, 2018.
- [40] A. Hevner and S. Chatterjee, Design Research in Information Systems: Theory and Practice . Springer Publishing Company, Incorporated, 2010, p. 393.
- [41] M. Uschold and M. King, Towards a Methodology for Building Ontologies . Edinburgh: Arti fi cial Intelligence Applications Institute, University of Edinburgh, 1995.
- [42] A. Gomez-Perez, M. Fern  andez-L  opez, and O. Corcho, Ontological Engineering: With Examples from the Areas of Knowledge Management, e-Commerce and the Semantic Web . New York: Springer Science &amp; Business Media, 2006.
- [43] D. B. Mongula, Enterprise Ontology of the Flood Control Domain , M.Sc, TU Delft, Delft, 2009.
- [44] J. Park, W. Cho, and S. Rho, ' Evaluating ontology extraction tools using a comprehensive evaluation framework, ' Data Knowl. Eng., vol. 69, no. 10, pp. 1043 -1061, 2010.
- [45] A. Scherp, C. Saathoff, T. Franz, and S. Staab, ' Designing core ontologies, ' Appl. Ontol. , vol. 6, no. 3, pp. 177 -221, 2011.

Open Access statement. This is an open-access article distributed under the terms of the Creative Commons Attribution-NonCommercial 4.0 International License (https:// creativecommons.org/licenses/by-nc/4.0/), which permits unrestricted use, distribution, and reproduction in any medium for non-commercial purposes, provided the original author and source are credited, a link to the CC License is provided, and changes -if any -are indicated.

[FIGURE]
