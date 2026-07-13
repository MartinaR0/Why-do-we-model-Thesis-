## Supporting Simulation of Military Communication Systems Using Well-Founded Modeling ⋆

André M. Demori 1 , * , † , Julio Cesar Cardoso Tesolin 1 , † , Maria Cláudia Reis Cavalcanti 1 , † and David Fernandes Cruz Moura 1 , †

1 Instituto Militar de Engenharia (IME), 22290-270 - Rio de Janeiro - RJ - Brazil

## Abstract

Tactical Military Communication Systems have several challenging requirements and characteristics to make them functional, as they are inserted in scenarios with diverse wireless access technologies that are constantly changing. One strategy to evaluate such scenarios is to reproduce reality through test environments, simulators, and network emulators. However, capturing the complex scenario for reproduction is still challenging. Therefore, this article proposes using well-founded conceptual modeling to support an explicit representation of real tactical military scenarios in network simulators and understand its agents' behavior.

## Keywords

Conceptual modeling, Tactical networks, Ontology, Network simulation

## 1. Introduction

Over the past few years, wireless communication networks have undergone several evolutions, providing flexibility in their management and new services to the users. Various wireless technologies are used simultaneously to meet new requirements, such as 4G, 5G, Wi-Fi, and others. Furthermore, each element of the network became flexible as it could communicate with multiple protocols. If, on the one hand, we have a heterogeneous network with various wireless access technologies, on the other hand, we have a network with nodes capable of changing their protocols without the need to replace their hardware, becoming a Software-Defined Network (SDN) [1].

Just like commercial mobile communication networks, the tactical communication networks used in the Armed Forces are challenged to operate in this new scenario taking into account the peculiarities of their operating environment [2]. One of the alternatives presented to understand the complexity of this environment is the use of simulation and emulation methods, not only for the technological aspect of the new mobile communication networks but also for the aspects

Proceedings of the 15th Seminar on Ontology Research in Brazil (ONTOBRAS) and 6th Doctoral and Masters Consortium on Ontologies (WTDO), November 22-25, 2022

* Corresponding author.

† These authors contributed equally.

andredemori@ime.eb.br (A. M. Demori); jcctesolin@ime.eb.br (J. C. C. Tesolin); yoko@ime.eb.br

[FIGURE]

[FIGURE]

[FIGURE]

[FIGURE]

inherent to the tactical-military environment. Hence, the reproduction of reality allows decisionmakers to have a reliable view of the operation environment, like the network behavior and the operation participants' behavior.

However, the reproduction of the elements of a communication network in a tactical-military environment is not a trivial task. There is a need to understand which elements belong to the operational environment and how they cause interference in the communication system. Furthermore, during preliminary research in the Glossary of the Armed Forces of Brazil [3], several semantic ambiguities were found in concepts that can have many meanings, depending on the exposed situation. In response to these difficulties, we chose a conceptual model supported by a well-founded ontology to overcome the complexity of the domain and the possible ambiguities. Among the possible alternatives, the Unified Foundational Ontology (UFO) [4] was chosen because of its high level of representativeness, its well-founded theory and for its potential to unravel the complexity of a domain through explicit representation using conceptual modeling.

Through the concepts derived from UFO, some works have presented the development of well-founded conceptual models that support the development of solutions for the formal representation of its domains and the exploration of semantic reasoning based on ontology. Nevertheless, the amount of works that propose to use UFO within the military area, more specifically within the context of tactical networks, is still scarce. This paper presents a preliminary conceptual modeling of a communication scenario in a tactical-military environment supported by the UFO constructs. It also presents the first results of the modeling while being used to represent a mobile communication network in the context of an emulation software. As preliminary results, an understanding is reached that a well-founded modeling can enrich the system in its representations, by using the constructs to express the characteristics of the elements that participate in the entire simulation process.

The following sections are organized as follows: Section 2 briefly reviews the main concepts of the Unified Foundational Ontology, Tactical and Software Defined Networks; Section 3 shows the academic efforts to reproduce communication networks environment; Section 4 presents the preliminary conceptual modeling being developed together with the UFO concepts. Section 5 presents the result of a military wireless network behavior simulation running over a network emulator considering the proposed conceptual modeling; Section 6 presents final considerations and future works.

## 2. Background

## 2.1. Unified Foundational Ontology (UFO)

The representation of reality is essential for information transfer. However, semantic ambiguities and incompleteness can cause different interpretations. Semantic problems can also be present in standards, protocols, recommendations, and glossaries in various areas, causing interoperability problems and inconsistencies. In systems and computing area, conceptual modeling is one of the tools to represent reality. In [4], Guizzardi argues that the truthfulness to the reality of a given system depends heavily on the availability of well-founded conceptual modeling languages.

Guizzardi proposes the creation of an axiomatized and well-founded higher-level ontology called the Unified Foundational Ontology (UFO) [4]. The author argues that a conceptual modeling language should have modeling primitives that reflect the conceptual categories defined in a Foundational Ontology [5]. Using UFO, modeling can be developed to facilitate integration between models, enable more sophisticated representations, avoid semantic interoperability problems, increase terminological accuracy and organize knowledge to be used in different ways.

UFO has been used as a top-level ontology alternative for model formulation in several works, and it is divided into three fragments. The first fragment is the UFO-A, the Ontology of Endurants ), which is the one with the highest scientific consensus [4]. Endurants are entities whose identities are preserved even if their characteristics change over time. The taxonomy of Endurants addresses concepts and basic philosophical principles and properties such as identity, part-whole relations, classification, and existential dependency, among others, that help in the formal representation of the real world.

The second fragment is UFO-B (Ontology of Perdurants ), defined as the part of the ontological foundations of conceptual modeling that addresses the concept of Events [6]. Perdurants are Individuals composed of temporal parts [4] and their approach can be seen as an extension of Giancarlo Guizzardi's seminal work. In this fragment of UFO, issues such as the mereology of Events , Dispositions of objects, pre and postEvent Situations , objects participating in Events , among others are addressed. The third fragment is UFO-C (Ontology of Social and Intentional Entities), which deals with social aspects such as Plan , Action , Goal , Agent , Intentionality , Commitment , Naming , among others [7].

This work uses the concepts defined in UFO-A fragment to support our conceptual modeling development. Figure 1 shows a UFO taxonomy fragment with some concepts used in this paper.

Figure 1: A Fragment of UFO-A Taxonomy

[FIGURE]

## 2.2. Emulation and Simulation of Communication Networks

To build functional military communication systems, the experimentation process should help develop strategies during decision-making, avoiding unforeseen events such as failures caused by reasons that could be reproduced beforehand. Hence, network emulators and simulators can be used to reproduce them. Moreover, it allows the exploration of parameter and configuration settings, helping the elaboration of better transmission and routing strategies, different topologies, or the simulation of issues related to access points' positioning or mobility pattern.

An extensive research was conducted in [8] looking for alternatives to perform experiments with wireless communication networks. The result shows three main types: emulators, simulators and testbeds. For instance, emulators for wireless networks allow a close analysis of the real world, using real protocols and transmission methods. On the other hand, simulators are based on hypothetical, non-real-time systems but provide more flexibility for researchers, for example, to reproduce random behavior and arbitrary user decisions in the system. The intersection between emulation and simulation occurs precisely in systems that aim to reproduce a simulated behavior, or a synthetic context, over an emulated system. For example, the user's transmission behavior in a communication network is simulated, but the equipment is being emulated.

## 2.3. Implementing Tactical Networks Using Software Defined Networks (SDN)

The academic literature shows that one of the overall strategies to implement tactical networks is the use of Software-Defined Networks [1] [2] [9]. The main feature of this strategy is the separation of the data plane and the control plane, providing a logical centralization through a controller. One of the main SDN emulators aimed at wireless networking is the Mininet-WiFi [10] [11] [12], which is an extension of Mininet [13].

The use of SDN as a solution for implementing networks in tactical environments has many advantages. It makes possible the virtualization of the network over the physical infrastructure, the dynamic provision of information, and a high degree of programmability and network reconfigurability. Also, it allows the fractioning of the network for specific policies and traffic separation, providing more possibilities for network infrastructure projects, and broad situational awareness, among other advantages. [2] [10] [14]

## 3. Related Works

The research conducted in the academic literature shows that there is little use of conceptual modeling based on a founded ontology to represent tactical networks.

The only work that was found relating the UFO constructs in the context of wireless networks was the one presented by the authors in [15] that propose the use of well-founded modeling using UFO due to the high level of semantic expressiviness in the domain of critical communication networks, aiming to support the decision process with the use of semantic reasoning. This paper is inspired by works such as [16], where Barcelos involves UFO concepts in communication networks. In [17], the authors address several concepts and work related to tactical networks and SDN. The authors review current research initiatives, explain possible demands and problems in building military communication networks, and point to future directions to be explored in these topics.

Authors in [18] propose developing an emulation system aimed at the context of tactical networks, including several elements that characterize such an environment. They also address the importance of experimentation and analysis in developing military networks. In [19], the authors present the development of an SDN simulation environment for tactical scenarios using Mininet-WiFi. Finally, in [20], the authors propose the incorporation of SDNs into tactical scenarios, working with realistic wireless networks and mobility patterns. It also addresses the dynamic network configuration problem, being concerned with building a suitable SDN and capturing the tactical military environment in a testbed.

## 4. Describing Tactical Communication Networks Using Well-Founded Modeling

During preliminary conceptual modeling process, the main components that should be part of a tactical communication use case were investigated. The development of the conceptual modeling started by looking at the Brazilian Army Communication Manuals 1 . Furthermore, interviews with experienced experts in the field of tactical networks, including one of the authors of the paper, were conducted throughout weekly meetings. As a result of these meetings, a better understanding of the communication environment was obtained, where there are restrictions that must be obeyed during communication. As a preliminary result, it was thought to develop the network emulation within a synthetic context that is the scenario with the five Military Organizations shown in the model of Figure 2 and the representation of the generation of the content shared. The idea is to use the ontology to create a reference model that represents the process that was reproduced through simulation and emulation as a conceptual guide giving guidelines for implementation and future directions. The model presented in Figure 2 depicts the reproduction of a fragment of a tactical network. This scenario involves content creation on the network that will be shared among military people, respecting the rules of communication that are based on the model itself.

The OntoUML language [21] was also used to create our preliminary conceptual model. This modeling language can be defined as a language used to represent ontological distinctions and constraints defined by UFO-A and UFO-B. Also, we used an OntoUML model validation plugin 2 , developed to work with the Visual Paradigm modeling tool 3 . Hence, we have all the support for formalization, verification, and semantic evaluation of our modeling attempts.

## 4.1. The Conceptual Model

The model explicit the relation between Military to MilitaryOrganization , represented as a material relation. Therefore, the Relator MilitaryEmployment is represented, which is the truthmaker of the relation. Relators are described in the literature as relations that are represented as Endurants and that mediate the relation between other Endurants [4], [22] ,[23], [24]. The explicit representation of Truthmakers intends to solve ambiguity problems in a material relations between different Endurants 4 .

MilitaryOrganization is meta-categorized as Category , a type that is used to aggregate properties to individuals that have different identity principles. On the other hand, Military is meta-categorized as an anti-rigid and relationally dependent type called Role .

1 https://bdex.eb.mil.br/jspui/handle/123456789/40

3 https://www.visual-paradigm.com/download/community.jsp

2 https://github.com/OntoUML/ontouml-vp-plugin

4 The taxonomy of Endurants stems from the categories of Universals and Individuals discussed in Chapter 4 of [4].

Figure 2: Preliminary conceptual model for representing the case study for tactical communications using UFO

[FIGURE]

The Kinds of MilitaryOrganization , being them Brigade , Battalion , Company , Regiment and Squadron 5 6 , are meta-categorized as Kinds , which are rigid types with a single identity principle. This entities are important to explicit the relations between the Kinds that will affect the communication rules. Defining that a type is rigid means that every instance of that type is necessarily that instance and will always be that instance, such as the cases of the entities Person and MilitaryOrganization in the model. The implementation of the communication rules, on the other hand, is influenced by the formal relations between each Kind of MilitaryOrganization , since there will be communication if the following rules are met:

5 The hierarchy of military organizations shown in the model is focused on the context of the Armed Forces of Brazil.

6 In Portuguese, the military organizations Brigade, Battalion, Company, Regiment and Squadron are respectively translated as Brigada, Batalhão, Companhia, Regimento and Esquadrão.

- R1: Given two CommDeviceOperators that are members of two different Kinds of MilitaryOrganization , a communication may occur if the formal relation directlySubordinate exists between the respective Kinds of MilitaryOrganization ;
- R2: Given two CommDeviceOperators that are members of two different Kinds of MilitaryOrganization a communication may occur if the formal relation isEquivalent exists between the respective Kinds of MilitaryOrganization ;
- R3: Given two CommDeviceOperators that are members of two identical Kinds of MilitaryOrganization , a communication may occur.

directlySubordinate and isEquivalent are being considered as formal relations [25], because they are related to the level of hierarchical position between military organizations, i.e. it is an intrinsic principle of organizations to have a higher or lower hierarchical level compared to other military organizations. Therefore, isEquivalent can be considered a comparative formal relation and directlySubordinate can be considered a formal relation between types, since some organizations are always directly subordinated to other organizations, that is, they are inherent.

The Military in the Role of CommDeviceOperator is also specialized as Role ContentCreator . It is important to represent the Role ContentCreator in the model since it shows that the CommDeviceOperator is not always responsible for content creation, once other roles are to be played depending on their mode of interaction with App . In this case, the role we are interested in representing is only ContentCreator since this interaction will be reproduced in the simulation environment.

App is being specialized as ContentEditor , since it is the app that enables users to create contents to be send. From this interaction with the App, the Session is created.

Represent the content generation process in the communication network is another goal to be achieved in the modeling since this event was reproduced in the simulation. The representation of the entity Session is important for this model, for representing what is derived from the material relation between ContentCreator and App in the Role of ContentEditor . So once again the concepts of Truthmaker and Relator appear.

In addition to CommDevice , the AccessPoint are also represented in the model. Together they have an aggregation relation with the WirelessNetwork , reproduced in the network emulation.

The Kind App is specialized as Role ContentSender , a role responsible for content transmission. This entity also has a Mode , called BBSignal , which is the baseband signal generated, responsible for carries the data through the network. For this reason, there is an formal relation between Content and BBSignal (Baseband Signal). According to [26], Modes are Moments whose Universals are not directly related to structured values 7 . Moreover, they are existentially dependent on their bearers. In this case, the Mode BBSignal is inherent to the ContentSender entity. Finally, the App entity is defined in the model as a aggregation element of the CommDevice entity.

Finally, the attributes of Content , such as SecutityLevel and Precedence are also represented in the model. These attributes may affect the decision-making process in the military environment, which is one of the future goals while reproducing this scenario in a network simulator.

## 5. Modeling Implementation

Thewell-founded modeling presented in Section 4 brings a conceptual help towards the provision of guidelines both for implementation as well as for users who will carry out experiments. This holds true due to the fact that the relation between the simulation agents and the scenario as a whole can be better understood as a strategy to test the typical behavior of a tactical communication network.

The first version of MiniManager [29] was developed just as an extension of Mininet-WiFi to manage experiments. It allows users to create different versions of network configurations and topologies, supported by an experiment provenance system, using an intuitive interface capable of comparing results between different execution rounds. Based on this initial MiniManager project, we have developed an extension that encompasses characteristics of the tactical communication scenario according to the presented conceptual models in Section 4.1.

Figure 3 shows the display interface of a running network experiment in a tactical communication scenario. The screen frame labeled as 1 shows radio frequency attributes extracted from the running experiment for each station in the network at a given instant. Frame 2 shows the results of the packet ( Content ) delivery between stations, working according to the rules presented in Section 4.1, e.g., a Regiment node, which represents a communication device in use by a military person of Regiment X, can communicate with a Brigade node, which represents a communication device in use by a military person of Brigade Y. Finally, Frame 3 shows the movement of a communication device ( sta ) within the coverage provided by the tactical wireless network access points ( ap ). This network is used by military personnel (stations) that belongs to military organizations. Each Military operates a device (a station), and each Military has a material relation with MilitaryOrganization . Four Military Organization types were configured in this experiment: Brigade , Battalion , Regiment and Squadron .

Each device creates and transmits Content with a certain SecurityLevel and Precedence . The transmission and reception of each Content are reproduced by using a round-trip-time test, commonly known as a ping test. The ping statistics in Frame 2 represent the communication between devices that are operated by military personnel serving in a particular MilitaryOrganization . The example shows that, based on the conceptual model presented in Section 4.1, it is only allowed Content transmission between organizations that comply with defined rules that take into account the formal relations between different Kinds of MilitaryOrganization .

7 The idea of structured value is linked to the notion of what is called Quality dimension or Quality structures which is the basis of the theory called Conceptual Models by Peter Gardenfors [27], [28]

Figure 3: Screenshot of MiniManager displaying the results of a network experiment between stations from different military organizations

[FIGURE]

## 6. Final Considerations and Future Works

Simulating military communication networks imposes challenges in representing their management complexity and diversity of wireless access technologies. This paper proposes an approach using a well-founded conceptual modeling that can provide a high semantic expressiveness and support the development of the real-world experimentation process. Moreover, it ensures consistency between the worldviews of the scenario reproduced in the computational environment.

Wepresent the results of the MiniManager extension as a preliminary case study that validates the use of well-founded modeling as a basis for understanding and reproducing the operational environment. In addition, the use of well-founded conceptual modeling contributed to consolidating the worldview of the scenario to be reproduced and improving the understanding of the semantic value of each represented element and its relations. Thus, this article encourages the use of well-founded modeling in software development, especially in experimentation processes such as simulation, which aims at reproducing reality.

In future works, we foresee deepening the veracity related to tactical network behavior simulation processes, applying more operational environment elements, and creating richer real-world representations. To achieve it, we intend to enhance our conceptual modeling using UFO fundamentals, adding more elements of the operational environment and analyzing how they relate to the communication system. For example, enriching the model by working with the historical semantics of a simulation process. This can be done using UFO-B concepts presented in Section 2.1 such as the use of Events and HistoricalRoles [30], since the process of simulating a military operation can also be seen in a historical way. For example, in a simulation process of a military operation, once the experiment is finished, the data can be captured by a provenance system and the military operation will be abstracted to a historical point of view, paying attention to the data that was captured.

The extension of this work intends to improve the MiniManager database by correctly including entities and relations such as associating devices on a network with military organizations and making these relations impact the way nodes communicate. For now, the modeling has influenced more in the construction of the relational database, but there is an intention to promote an import of the model in OWL when creating the scenario for simulation. Other ideas for extending the work are the use of multi-level modeling and deepening related works that involve semantic foundation for organizational structures [31] and bring this into the context of modeling military organizations.

## Acknowledgment

This research has been funded by FINEP/DCT/FAPEB (ref.: 2904/20 convênio 01.20.0272.00) under the 'Systems of Command and Control Systems' project ('Sistemas de Sistemas de Comando e Controle', in Portuguese).

## References

- [1] D. Kreutz, F. M. V. Ramos, P. E. Veríssimo, C. E. Rothenberg, S. Azodolmolky, S. Uhlig, Software-defined networking: A comprehensive survey, Proceedings of the IEEE 103 (2015) 14-76. doi: 10.1109/JPROC.2014.2371999 .
- [2] B. Doshi, D. Cansevar, J. Pilipovic, Software defined networking for armys tactical network: Promises, challenges, architectural approach, and required s &amp; t work, US Army CERDEC, Tech. Rep. (2016).
- [3] M. da Defesa, Glossário das forças armadas, https://bdex.eb.mil.br/jspui/bitstream/ 123456789/141/1/MD35\_G01.pdf, 2015. [Online; accessed 26-July-2022].
- [4] G. Guizzardi, Ontological foundations for structural conceptual models (2005).
- [5] G. Guizzardi, J. P. Almeida, R. GUIZZARDI, M. P. Barcellos, R. Falbo, Ontologias de fundamentação, modelagem conceitual e interoperabilidade semântica, in: Proceedings of the Iberoamerican Meeting of Ontological Research. Anais, Citeseer, 2011.
- [6] G. Guizzardi, G. Wagner, R. de Almeida Falbo, R. S. Guizzardi, J. P. A. Almeida, Towards ontological foundations for the conceptual modeling of events, in: International Conference on Conceptual Modeling, Springer, 2013, pp. 327-341.
- [7] G. Guizzardi, R. de Almeida Falbo, R. S. Guizzardi, Grounding software domain ontologies in the unified foundational ontology (ufo): The case of the ode software process ontology., in: CIbSE, Citeseer, 2008, pp. 127-140.
- [8] R. D. R. Fontes, Mininet-Wifi: Emaulation Platform For Software-Defined Wireless Networks, Ph.D. thesis, Universidade Estadual de Campinas, Campinas-SP-Brasil, 2018.
- [9] R. D. R. Fontes, C. Campolo, C. E. Rothenberg, A. Molinaro, From theory to experimental evaluation: Resource management in software-defined vehicular networks, IEEE access 5 (2017) 3069-3076.
- [10] R. R. Fontes, S. Afzal, S. H. Brito, M. A. Santos, C. E. Rothenberg, Mininet-wifi: Emulating software-defined wireless networks, in: 2015 11th International Conference on Network and Service Management (CNSM), IEEE, 2015, pp. 384-389.
- [11] R. d. R. Fontes, C. E. Rothenberg, Mininet-wifi: A platform for hybrid physical-virtual software-defined wireless networking research, in: Proceedings of the 2016 ACM SIGCOMM Conference, 2016, pp. 607-608.
- [12] R. dos Reis Fontes, C. E. Rothenberg, Mininet-wifi: Plataforma de emulação para redes sem fio definidas por software, in: Anais Estendidos do XXXVII Simpósio Brasileiro de Redes de Computadores e Sistemas Distribuídos, SBC, 2019, pp. 201-208.
- [13] B. Lantz, B. Heller, N. McKeown, A network in a laptop: rapid prototyping for softwaredefined networks, in: Proceedings of the 9th ACM SIGCOMM Workshop on Hot Topics in Networks, 2010, pp. 1-6.
- [14] C. U. Army, Deployed Tactical Network Guidance - Appendix D to Guidance for 'End State' Army Enterprise Network Architecture - Version 1.0, CIO U.S. Army, Washington, DC, USA, 2012.
- [15] J. Tesolin, M. Silva, M. L. M. Campos, D. Moura, M. C. Cavalcanti, Critical communications scenarios description based on ontological analysis., in: ONTOBRAS, 2020, pp. 212-218.
- [16] P. P. F. Barcelos, C. C. Reginato, M. E. Monteiro, A. S. Garcia, On the importance of truly ontological distinctions for standardizations: A case study in the domain of telecommunications, Computer Standards &amp; Interfaces 44 (2016) 28-41.
- [17] R. Mahmud, A. N. Toosi, M. A. Rodriguez, S. C. Madanapalli, V. Sivaraman, L. Sciacca, C. Sioutis, R. Buyya, Software-defined multi-domain tactical networks: Foundations and future directions, in: A. Mukherjee, D. De, S. K. Ghosh, R. Buyya (Eds.), Mobile Edge Computing, 1 ed., Springer International Publishing, Gewerbestrasse 11, 6330 Cham, Switzerland, 2021, pp. 183 - 228.
- [18] N. Suri, A. Hansson, J. Nilsson, P. Lubkowski, K. Marcus, M. Hauge, K. Lee, B. Buchin, L. Mısırhoğlu, M. Peuhkuri, A realistic military scenario and emulation environment for experimenting with tactical communications and heterogeneous networks, in: 2016 International Conference on Military Communications and Information Systems (ICMCIS), IEEE, 2016, pp. 1-8.
- [19] Q. Zhao, A. J. Brown, J. H. Kim, M. Gerla, An integrated software-defined battlefield network testbed for tactical scenario emulation, in: MILCOM 2019-2019 IEEE Military Communications Conference (MILCOM), IEEE, 2019, pp. 373-378.
- [20] K. M. Marcus, K. S. Chan, R. L. Hardy, P. L. Yu, An environment for tactical sdn experimentation, in: MILCOM 2018 - 2018 IEEE Military Communications Conference (MILCOM), 2018, pp. 1-9. doi: 10.1109/MILCOM.2018.8599775 .
- [21] J. Guerson, T. P. Sales, G. Guizzardi, J. P. A. Almeida, Ontouml lightweight editor: a model-based environment to build, evaluate and implement reference ontologies, in: 2015 IEEE 19th International Enterprise Distributed Object Computing Workshop, IEEE, 2015, pp. 144-147.
- [22] G. Guizzardi, G. Wagner, What's in a relationship: An ontological analysis, in: International

Conference on Conceptual Modeling, Springer, 2008, pp. 83-97.

- [23] N. Guarino, G. Guizzardi, 'we need to discuss the relationship': Revisiting relationships as modeling constructs, in: International Conference on Advanced Information Systems Engineering, Springer, 2015, pp. 279-294.
- [24] G. Guizzardi, V. Zamborlini, Using a trope-based foundational ontology for bridging different areas of concern in ontology-driven conceptual modeling, Science of Computer Programming 96 (2014) 417-443.
- [25] C. M. Fonseca, D. Porello, G. Guizzardi, J. P. A. Almeida, N. Guarino, Relations in ontologydriven conceptual modeling, in: International Conference on Conceptual Modeling, Springer, 2019, pp. 28-42.
- [26] G. Guizzardi, G. Wagner, Using the unified foundational ontology (ufo) as a foundation for general conceptual modeling languages, in: Theory and applications of ontology: computer applications, Springer, 2010, pp. 175-196.
- [27] P. Gärdenfors, Conceptual spaces: The geometry of thought, MIT press, 2004.
- [28] P. Gärdenfors, How to make the semantic web more semantic, in: Formal ontology in information systems, 2004, pp. 19-36.
- [29] A. Demori, R. Silva, P. Albuquerque, D. Moura, J. Tesolin, M. C. Cavalcanti, Minimanager: Uma proposta de plataforma web para emulação de redes heterogêneas de comunicação móvel, in: SBRC 2022 - Salão de Ferramentas (Fortaleza/CE), 2022.
- [30] J. P. A. Almeida, R. A. Falbo, G. Guizzardi, Events as entities in ontology-driven conceptual modeling, in: International Conference on Conceptual Modeling, Springer, 2019, pp. 469-483.
- [31] V. A. Carvalho, J. P. A. Almeida, A semantic foundation for organizational structures: a multi-level approach, in: 2015 IEEE 19th International Enterprise Distributed Object Computing Conference, IEEE, 2015, pp. 50-59.
