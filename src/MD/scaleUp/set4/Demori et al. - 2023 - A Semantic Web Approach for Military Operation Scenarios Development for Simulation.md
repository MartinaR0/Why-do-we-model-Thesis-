## A Semantic Web Approach for Military Operation Scenarios Development for Simulation

Andr´ e M. Demori 1 a , Julio Cesar Cardoso Tesolin 1 b , David Fernandes Cruz Moura 1 c , Jo˜ ao Eduardo Costa Gomes 2 d , Gabriel Pedroso 2 e , Leonardo Filipe Batista Silva de Carvalho 2 f ,

Edison Pignaton de Freitas 2 g and Maria Cl´ audia Reis Cavalcanti 1 h

1 Military Institute of Engineering, Rio de Janeiro, RJ, Brazil

2 Federal University of Rio Grande do Sul, Porto Alegre, Brazil

Keywords:

Semantic Web, Domain ontologies, Decision-making, Modeling and Simulation.

Abstract:

The reality simulation process by computational means allows decision-makers to analyze and propose the best strategies to be adopted in a real environment. However, the scenario, sometimes heterogeneous, as in the case of military operations, requires formalization to achieve domain knowledge, allowing a more faithful reproduction of reality. In the case of military operation scenarios that address tactical, operational, and strategic elements and the use of communications, formalization could help organize knowledge, data sharing, and decision-making. This article proposes (i) the use of conceptual modeling that is based on concepts arising from a foundation ontology named UFO (Unified Foundational Ontology), (ii) the use of Web Ontology language (OWL), and (iii) the use of rule definitions expressed in the Semantic Web Rule Language (SWRL). Through this approach, this article describes the process of formalizing the domain knowledge as a reference and its corresponding operational ontology by identifying entities, relationships, rules, and all the categorizations made in the ontology for execution and decision-making in a battlefield simulator that is still in production. The application of this ontology is illustrated in representative and real-world examples, showing promising results of the proposed approach.

## 1 INTRODUCTION

During the planning process of a military operation, an examination of its operational elements must be done to understand how they would behave and influence the decision-making procedure. The heterogeneous wireless communication system is essential to the military operation scenario. Here, the heterogeneity is not only related to the existence of different radio systems on different channels but also to different military units, air and ground platforms, variables such as distance, terrain, weather, troop mobility, high

[FIGURE]

## 390

Demori, A., Tesolin, J., Moura, D., Gomes, J., Pedroso, G., Silva de Carvalho, L., Pignaton de Freitas, E. and Cavalcanti, M. A Semantic Web Approach for Military Operation Scenarios Development for Simulation. DOI: 10.5220/0012088600003541

demand for information transfer rate, among others (Marcus et al., 2018).

The reproduction of reality through simulation allows decision-makers to verify alternatives outside the real environment, providing statistical analysis and the necessary data to deal with each possible scenario. However, the representation and reproduction of a wireless communication military scenario is a challenge once it deals with variables not only limited to the characterization of the wireless communications systems. It also deals with variables related to the environment where the wireless communication system is used.

The Semantic Web provides representation and reasoning resources, such as ontologies and formal languages, that are useful to represent and simulate those military communication scenarios. Nevertheless, for a machine to make inferences and interpret the existing content in a dataset shared by different agents, there must be a formal model of a portion of reality that allows it to understand, reason, and make decisions. In computing, building such formal models is the exercise of developing ontologies, which can help solve problems of semantic ambiguity, interoperability, and formalization of knowledge through taxonomies and rules.

The W3C Web Ontology Language (OWL) is a Semantic Web language designed to represent rich and complex knowledge about things 1 . However, previous to expressing ontologies in it, it is necessary to elicit requirements and identify concepts and relationships for a given domain. Conceptual modelling languages are essential, as are ontology development methodologies, to guide domain modellers in this task.

Although there are some tools that allow the simulation of communication networks, as far as it was investigated, none of them is able to deal with the demands of military scenario representation. On the other hand, there are works (Tzeng et al., 2009) (Gilmour et al., 2006) that propose ontologies to represent such scenarios. However, none of them follow the steps of an ontology development methodology, generating a well-founded operational ontology.

Therefore, this work presents an ontology to represent the communication environment in military tactical scenarios. This ontology aims to achieve a significant portion of the domain knowledge for these scenarios, allowing semantic reasoning to assist in decision-making in the simulation process. We also present the first results of an operational scenario planning process.

This document is structured as follows. Section 2 introduces the basic concepts used in this paper, while Section 3 discusses some related works. Section 4 describes the typical scenario of a military operation. Based on this scenario a reference ontology and its implementation were developed and are presented in Sections 5 and 6, respectively. Section 7 concludes and offers perspectives for future work.

## 2 BACKGROUND

Although the Semantic Web encourages the design of ontologies to represent and reason over data from any domain, it is strongly recommended to follow an ontology development methodology. Among the ones available in the literature, we chose to use SABiO (Systematic Approach for Building Ontologies) (de Almeida Falbo, 2014), which distinguishes between two types of domain ontologies: reference and operational. A reference ontology is a domain ontology that is a solution-independent specification (conceptual model) built with the goal of making the best possible description of the domain. According to SABiO development process, once a reference ontology is obtained, operational versions (machinereadable ontologies) of it can be implemented.

1 https://www.w3.org/OWL/

Moreover, SABiO recognizes the importance of the use of foundation ontologies in the development of reference ontologies and proposes applying ontological analysis during the ontology design. In this analysis, the relevant concepts and relations should be identified and organized according to highlyexpressive languages, such as OntoUML(Guerson et al., 2015). It incorporates important foundational distinctions, which enables the designer to create strongly axiomatized domain ontologies that can reflect the domain, as closely and adequately as possible, and serve as a reference. Those distinctions come from the Unified Foundational Ontology (UFO), which is described in Section 2.1.

A well-founded reference ontology may produce and implement the best possible corresponding operational ontology. However, it is worth saying that just as a reference ontology is a simplified representation of reality, similarly, an operational ontology usually implies a simplification of a reference ontology. Section 2.2 describes briefly the Semantic Web and some of its proposed languages, which are suitable to represent operational ontologies.

## 2.1 UFO

The use of foundation or upper ontologies in conceptual modeling attempts to produce richer models, favoring a faithful representation as close as possible to the real world. The Unified Foundational Ontology (UFO) presented by Guizzardi (2005) is one of the prominent upper ontologies currently available that has been used to face the challenge of building well-founded and formalized conceptual models in different domains (Griffo et al., 2016) (Barcelos et al., 2016) (Fabio et al., 2021). It is divided into three fragments for better understanding: UFO-A, UFO-B, and UFO-C. UFO-A is also known as the Ontology of Endurants and deals with modeling types whose instances are object-like entities, having their foundations in two principles: Existential Dependency and Identity. On the other hand, UFO-B, or the Ontology of Perdurants, deals with entities bounded in time, in contraposition with Endurants, which have their identities preserved over time, even if their essential or contingent properties may change. Finally, UFO-C, or the Ontology of Social and Intentional Entities, is built upon UFO-A and UFO-B and represents social and intentional aspects (Guizzardi et al., 2008).

According to SABiO, to capture and formalize a domain ontology, the modeler should classify each concept according to the categories defined in UFO (kind, subkind, phase, role, category, rolemixin etc.). Moreover, the constraints for relating these types should be respected in order to achieve consistent conceptual models. As mentioned before, these types and their corresponding constraints and ontological patterns are incorporated into the OntoUML.

## 2.2 Semantic Web

As defined by Berners-Lee et al. (2001), the Semantic Web is an extension of the current web in which information is given a well-defined meaning, allowing for greater cooperation between computers and people. As such, machines can understand data rather than display it, becoming not only a document storage network but also a means of automatic information processing. Nevertheless, importing, representing, and linking data with information from different fields of knowledge is a challenge.

For machines to be capable of understanding data and of automated reasoning, a set of languages and standards has been proposed by the W3C, such as XML, RDF, RDFS, SPARQL, OWL, SWRL, and SKOS. The OWL 2 is the most expressive language. It incorporates formal semantics that comes from the OWL Web Ontology Semantics and Abstract Syntax (OWL S &amp; AS ) 3 . It is based on computational logic, so a computer program can check the consistency of knowledge expressed in OWL or make explicit the implicit knowledge. OWL also allows representing the rule axioms generated by SWRL (Semantic Web Rule Language) 4 . SWRL can be used to create constraints on defining relationships and instances and to assign attribute values to the instance of a class in ontology using rules that consist of an antecedent and a consequent.

## 3 RELATED WORKS

Tzeng et al. (2009) present the Ontology-based Military Scenario Resources Management (OMSRM) platform to demonstrate how ontology technologies can be adopted to improve the reuse capabilities of military scenario resources. The paper presents a study that uses OWL to create a multi-layered ontology architecture that provides RDF-based metadata and OWL-based ontologies for the OMSRM platform. However, the creation of the ontology was not supported by a foundation ontology, which would help to distinguish concepts and enrich the semantics. For example, according to their model, a military unit may use some equipment that could be a vehicle or a communication device. It misses the notion that the vehicle 'carries' a device, which would inform how fast that device is moving. This is important for simulating a communications scenario in military operations.

2 https://www.w3.org/OWL/

3 https://www.w3.org/TR/owl-semantics/

4 https://www.w3.org/Submission/SWRL/

In turn, Gilmour et al. (2006) presents the SGen aimed at simulations for the military scenario domain. SGen can generate simulation scenarios and run them in parallel using high-performance computing (HPC) to evaluate alternatives for war plans by simulating large numbers of data sets. SGen also uses an ontology-based approach through ontology formalization, reasoning, and inference capabilities to create a meta-model representing a domain of interest, in this case, military mission planning. However, they do not report on the use of a foundation ontology, nor do they provide a detailed overview of the developed ontology.

The Simulation Interoperability Standards Organization (SISO) 5 focuses on facilitating interoperability between simulation systems and reuse through several standards. Nevertheless, as pointed out by Tzeng et al. (2009), these standards do not address how ontologies can be a way to represent knowledge to facilitate machine reasoning and facilitate the reuse of resources from the military scenario.

Some representation challenges in the military scenario domain are indicated by Lacy and Gerber (2004), such as the representation of behaviors, descriptions of units and objects to be simulated as military units, descriptions of entities (e.g., military platforms), descriptions of entity attributes, and scenarios. The authors point out that through the consistent OWL syntax, it is possible to have better information sharing, support for reasoning through inference systems, and support for the modeling and simulation community for the representation challenges cited above. Despite this argument for the use of OWL, they do not actually present an ontology for military scenarios.

In turn, the work presented by Tesolin et al. (2020) proposes the modeling of an ontology using UFO in the context of wireless networks, more specifically, in the domain of critical communications networks. The result is a clearer and unambiguous specification of the situations within the scenario, thus assisting in the decision-making process through semantic reasoning.

5 https://www.sisostds.org/

Although this work does not address modeling for a simulation-oriented scenario, it has a great similarity with the methodology adopted for reasoning and decision-making of the present work.

Finally, the present work continues what was presented by Demori et al. (2022), showing an attempt at modeling using UFO for a military communication scenario. The initial modeling of an ontology formalized and helped elaborate the simulation of a tactical environment. However, neither a serialization of the scenario in OWL, nor the representation of rules in SWRL, was performed to make processing by the simulator possible. Besides, the ontology presented in this work still contemplated a few elements of the military scenario.

## 4 THE MILITARY OPERATION SCENARIO

During the planning of complex and heterogeneous scenarios such as those found in a military operation for simulation applications, ontological analysis can be used for decision support, knowledge management, a better semantic definition for ambiguous terms present in glossaries and manuals, information sharing, and achieving a shared conceptualization, among others.

The preliminary process of ontology development, developed from a conceptual modeling methodology, was the research about which elements should be part of the scenario in the reference ontology. The research began with surveys of army manuals, articles, and glossaries related to the topic and meetings with experts. As a result, the elements that compose the scenario mainly affect the communication system about node mobility, which involves platforms to move in different terrains, communication restrictions, device configuration, device operators, and their respective military organizations. The scenario developed with the ontology analysis in this paper is a continuation of the results shown by Demori et al. (2022).

Chapter 5 of the Brazilian Army's military employment manual C11-1 - Employment of Communications (EME, 1997) ( Emprego das Comunicac ¸˜ oes in portuguese) addresses several issues regarding the planning and control of communications. It is demonstrated that a communication network built in a scenario such as a military operation suffers more significant interference from the external environment than a conventional network.

Still on this subject, Bispo et al. (2014) present a scenario-based analysis supporting military commu- nications system design. The paper reinforces the requirements described in the previously mentioned Communications Employment Manual, providing a more detailed description of the operational scenario variables, as given by domain experts. In the aforementioned work, some concepts were based on operational scenario variables, such as participants, mobility, and platform, as well as on communication scenario variables, such as range and frequency, among others described in the article.

Other information sources for the development of the scenario were taken from the Brazilian Army's digital library 6 .

## 5 REFERENCE ONTOLOGY FOR MILITARY OPERATION SCENARIOS

This Section presents a reference ontology of a scenario for further simulation in an environment involving a network emulator. It covers elements from the military domain and some elements from the networking domain, and it was created using an implementation of the OntoUML language (Guerson et al., 2015).

In the case of elements from the military domain, for example, in Figure 1, military organizations ( MilitaryOrganization ), as well as their types ( MilitaryOrganizationPowerType ) are represented. Moreover, military organizations can have different roles concerning other military organizations, such as subordination role ( Subordinate ) and commander role ( Commander ).

It is usual that the communication between members of two organizations is restricted according to their hierarchical roles. For example, when two organizations are in hierarchically equivalents roles ( HierarchicallyEquivalentDuringCommunica-

tion ), or when one of them is directly subordinated to the other, they are allowed to communicate. Otherwise, they are not allowed to. Thus, decisions can be made to restrict communications according to the military organization hierarchy levels, and this should be reflected in the network emulation environment.

In turn, a person ( Person ) can be specialized in a military person ( MilitaryPerson ) when it belongs to a military organization for an employment relationship ( MilitaryEmployment ). Also, a military person operating a communication device ( CommDevice ) is an operator

6 https://bdex.eb.mil.br/jspui/

( CommDeviceOperator ), and those located in a vehicle are passengers ( MilitaryPersonAsPassenger ). However, a military can also carry a communication device on foot ( MilitaryPersonAsCarrier ). Whether a military person operating a device is on foot or in a vehicle will directly affect the speed at which a communication device moves in the network emulation. So there are the elements that are characterized by carrying a communication device with them ( CommDeviceCarrier ). They are either a military person or a platform ( MilitaryPlatform ). Military vehicles ( Vehicle ) are part of the platform category. In turn, armored vehicles ( Armored ) are part of the vehicle category, and a Guarani ( Guarani ) is a type of armored vehicle.

In addition to the communication device ( CommDevice ), other elements are present to represent the network environment, such as the wireless network ( WirelessNetwork ) and the access points ( AccessPoint ). A communication device has interfaces ( Interface ) that must be configured in the network emulator. These interfaces also have a type InterfacePowerType with specific attributes.

Some classes shown in the modeling have relevant attributes for the scenario analysis. For example, the CommDeviceCarrier class has attributes referring to locomotion speed ( MinSpeed , MaxSpeedLand ) and fire range ( VisibilityRange ) for experiments related to fratricides. Likewise, the Guarani class has an attribute referring to its amphibious speed ( AmphibiousSpeed ) since this type of vehicle can travel in water. In turn, the CommDevice class has attributes such as range ( Range ) and antenna gain ( AntennaGain ). Finally, each interface type has attributes such as the data transfer method ( DataTransferMethod ), the frequency ( Frequency ), and the power level transmission ( Txpower ).

All elements represented in the modeling were categorized following the UFO taxonomy, especially the UFO-A fragment that addresses issues such as identity principle, existential dependency, and rigidity. The approach adopted in this work helped formalize the scenario development using ontological analysis, bringing a semantic enrichment. Given this scenario, the foundation ontology optimizes cognitive capacity in defining roles, phases, all-part relationships, rules, and responsibilities.

The conceptual modeling with all the scenario elements for the battlefield simulation was developed with the OntoUML plugin 7 for VisualParadigm 8 . and is available in the Gitlab repository of the project 9 . Figure 1 shows the conceptual modeling developed.

7 https://github.com/OntoUML/ontouml-vp-plugin

8 https://www.visual-paradigm.com/download/commu nity.jsp

## 6 IMPLEMENTATION

The operational ontology was implemented in OWL based on the reference ontology presented in Section 5. It was generated through a lightweight implementation of the UFO, the gUFO (Almeida et al., 2020). The OWL version of the ontology was loaded into Prot´ eg´ e 10 , and it was possible to specialize and instantiate the ontology elements. The scenario developed using ontology analysis is exported from Prot´ eg´ e and documented in OWL format, allowing the rich representation of knowledge that includes entities, individuals, categories, inferences, attributes, rules, and relationships. This Section shows how data and information from the military scenario are documented and processed through OWL. Listing 1 shows an OWL/XML Syntax code fragment of an ontology where the ClassAssertion axioms of a given individual are being represented. The ClassAssertion axiom allows stating that an individual is an instance of a particular class 11 . In this case, the individual 22 is instantiated as an instance of class MilitaryPerson , and by reasoner inference on account of rules or inheritance relationships, it is also instantiated in other classes.

Listing 1: Class Assertion example.

[FIGURE]

Through the combination of SWRL rules and cardinality constraints, restrictions were defined in the ontology for instantiations and relationships. The reasoner must indicate an ontological error if these restrictions are not obeyed. For example, when creating an instance of the class MilitaryPerson , it must be related to an instance of the class MilitaryOrganization to which that military person belongs. The same is true for instances of MilitaryPlatform . Therefore, when creating a relationship between a military person and a platform, establishing that the military person is inserted in a specific vehicle, for example, a constraint says that the military person must belong to the same military organization as the vehicle. Otherwise, an error will be indicated. This was done by establishing a cardinality constraint between the military person and the organization. Since the military person can only be associated with at most one organization, so using SWRL, if an instance of a military person has a relationship with a platform (isLocatedIn), then by consequence, that military person belongs to the same organization as the platform. Since the military organization to which the military person belongs had already been defined when the military person instance was created, it will cause a logical error if the military person's organization is different from the platform's organization. The SWRL rule presented in equation 1, represents this constraint.

9 https://gitlab.com/andredemori/ontology-basedscenario-repository

10 https://protege.stanford.edu/

11 https://www.w3.org/TR/owl2-syntax/

Figure 1: Conceptual modeling of military operation scenario.

[FIGURE]

```
MilitaryPlat f orm ( ? mp ) ∧ MilitaryOrganization ( ? mo ) ∧ belongsTo ( ? mp , ? mo ) ∧ MilitaryPerson ( ? m 1 ) ∧ isLocatedIn ( ? m 1 , ? mp ) → militaryHasMilitaryOrganization ( ? m 1 , ? mo ) (1)
```

The code fragment presented in Listing 2 shows how the ontology information expressed in the OWL file inside the DLSafeRule marker is used to allow rule creation.

```
<Body> <ObjectPropertyAtom> <ObjectProperty IRI="#isLocatedIn"/> <Variable IRI="#m1"/> <Variable IRI="#mp"/> </ObjectPropertyAtom> <ClassAtom> <Class IRI="#MilitaryPerson"/> <Variable IRI="#m1"/> </ClassAtom> <ClassAtom> <Class IRI="#MilitaryPlatform"/> <Variable IRI="#mp"/> </ClassAtom> <ObjectPropertyAtom> <ObjectProperty IRI="#belongsTo"/> <Variable IRI="#mp"/>
```

```
<Variable IRI="#mo"/> </ObjectPropertyAtom> <ClassAtom> <Class IRI="#MilitaryOrganization"/> <Variable IRI="#mo"/> </ClassAtom> </Body> <Head> <ObjectPropertyAtom> <ObjectProperty IRI="# militaryHasMilitaryOrganization"/> <Variable IRI="#m1"/> <Variable IRI="#mo"/> </ObjectPropertyAtom> </Head>
```

Listing 2: Rule axiom example.

In this sense, a set of rules was created to define restrictions on communication between devices during the simulation process since the communication devices can only communicate with others if the mayTalkTo relationship represented in de modeling in Figure 1 exists between them. For instance, the simulation may have to follow two rules: (i) Two devices can communicate if there is a relationship of subordination between the military organizations of the military persons operating the devices; (ii) Two devices can communicate if the military persons operating the devices belong to the same military organizations.. Depending on the scenario the rules can be changed.

The code fragment presented in Listing 3 shows how these rules are expressed in OWL. In this example, the communication device sta5 has a relationship mayTalkTo with sta14 and sta15 communication devices, allowing the communication between them.

```
<ObjectPropertyAssertion> <ObjectProperty IRI="#mayTalkTo"/> <NamedIndividual IRI="#sta5"/> <NamedIndividual IRI="#sta14"/> </ObjectPropertyAssertion> <ObjectPropertyAssertion> <ObjectProperty IRI="#mayTalkTo"/> <NamedIndividual IRI="#sta5"/> <NamedIndividual IRI="#sta15"/> </ObjectPropertyAssertion>
```

Listing 3: Object property assertion examples.

Other SWRL rules are applied to set attribute values (or data properties) for some entities in our military scenario. For instance, the rule in Equation 2 shows how the attributes related to speed and fire range restrictions are set for the combat vehicle type Guarani . The code fragment presented in Listing 4 shows the result of the ontological reasoning after evaluating Equation 2.

```
Guarani ( ? g ) → AmphibiousSpeed ( ? g , 9 ) ∧ MaxSpeedLand ( ? g , 95 ) ∧ MinSpeed ( ? g , 3 . 5 ) ∧ VisibilityRange ( ? g , 1000 ) (2) <Body> <ClassAtom> <Class IRI="#Guarani"/> <Variable IRI="#g"/> </ClassAtom> </Body> <Head> <DataPropertyAtom> <DataProperty IRI="#AmphibiousSpeed"/> <Variable IRI="#g"/> <Literal datatypeIRI="http://www.w3.org /2001/XMLSchema#integer">9</Literal > </DataPropertyAtom> <DataPropertyAtom> <DataProperty IRI="#MaxSpeedLand"/> <Variable IRI="#g"/> <Literal datatypeIRI="http://www.w3.org /2001/XMLSchema#integer">95</ Literal> </DataPropertyAtom> <DataPropertyAtom> <DataProperty IRI="#MinSpeed"/> <Variable IRI="#g"/> <Literal datatypeIRI="http://www.w3.org /2001/XMLSchema#decimal">3.5</ Literal> </DataPropertyAtom> <DataPropertyAtom> <DataProperty IRI="#VisibilityRange"/> <Variable IRI="#g"/> <Literal datatypeIRI="http://www.w3.org /2001/XMLSchema#integer">1000</ Literal> </DataPropertyAtom> </Head>
```

Listing 4: Data property definitions examples.

The Listings and SWRL rules present some parts of how the military scenario is created and represented using Semantic Web technologies. Through this, a simulator of the scenario is being developed to process and generate new information based on this data. For example, the simulator should be able to read the ontology in OWL and start creating the scenario to be simulated with all the instances passed for the military and the network environment.

## 7 CONCLUSIONS

Many environmental changes can happen during a military operation that may drive the need to change the communication technologies. Therefore, reproducing real military scenarios in a computational environment can help the planning process and improve ongoing decision-making. Such reproductions can be done using battlefield simulators or tactical network simulators.

This work reinforces the use of Semantic Web technologies to provide resource sharing, allowing data to be processed so that decisions can be made during the simulation using semantic reasoners. It differs from other related works once it uses a wellfounded conceptual modeling approach to categorize and relate each element of the proposed scenario. Furthermore, its representation richness provides a semantic advantage as it improves interoperability with other ontologies focused on military or communication scenarios.

A battlefield communication simulator is currently being developed with the proposed ontology as part of our future works. Our goal is to evaluate its capacity to not only describe different military operations but also improve the decision-making process in the field as it can adequately responds to environmental changes such as the increase of radio frequency interferences. Moreover, this future evaluation intends to test its extension capability while modeling new elements of the operational scenario, while interoperating with existing models that describe military operations and their communications environment.

## ACKNOWLEDGEMENTS

This research has been funded by FINEP/DCT/FAPEB (ref.: 2904/20 convˆ enio 01.20.0272.00) under the 'Systems of Command and Control Systems' project ('Sistemas de Sistemas de Comando e Controle', in Portuguese).

## REFERENCES

- Almeida, J., Guizzardi, G., Falbo, R., and Sales, T. P. (2020). gufo: a lightweight implementation of the unified foundational ontology (ufo). URL http://purl. org/nemo/doc/gufo .
- Barcelos, P. P. F., Reginato, C. C., Monteiro, M. E., and Garcia, A. S. (2016). On the importance of truly ontological distinctions for standardizations: A case study in the domain of telecommunications. Computer Standards &amp; Interfaces , 44:28-41.
- Berners-Lee, T., Hendler, J., and Lassila, O. (2001). The semantic web. Scientific american , 284(5):34-43.
- Bispo, M. N., Gomes, G. A. F., da Nova, J. N., and Moura, D. F. C. (2014). Emprego de an´ alise baseada
- em cen´ arios em apoio a projeto de sistemas de comunicac ¸ ˜ oes militares. In Cadernos CPqD Tecnologia , pages 63-76.
- de Almeida Falbo, R. (2014). Sabio: Systematic approach for building ontologies. In Onto. Com/odise@ Fois .
- Demori, A. M., Tesolin, J. C. C., Cavalcanti, M. C. R., and Moura, D. F. C. (2022). Supporting simulation of military communication systems using well-founded modeling. In Proc of the XV Seminar on Ontology Research in Brazil (ONTOBRAS) , volume 3346, pages 73-84.
- EME (1997). Emprego das comunicac ¸˜ oes. http://bdex.e b.mil.br/jspui/handle/123456789/386. [Accessed 01-Mar-2023].
- Fabio, I., Amaral, G. C., Griffo, C., Bai˜ ao, F., and Guizzardi, G. (2021). ' what exactly is a lockdown?': towards an ontology-based modeling of lockdown interventions during the covid-19 pandemic. In ONTOBRAS , pages 151-165.
- Gilmour, D. A., Krause, L. S., Lehman, L. A., McKeever, W. E., and Stirtzinger, T. (2006). Scenario generation to support mission planning. Technical report, AIR FORCE RESEARCH LAB ROME NY INFORMATION DIRECTORATE.
- Griffo, C., Almeida, J. P. A., and Guizzardi, G. (2016). A pattern for the representation of legal relations in a legal core ontology. In JURIX , pages 191-194.
- Guerson, J., Sales, T. P., Guizzardi, G., and Almeida, J. P. A. (2015). Ontouml lightweight editor: a modelbased environment to build, evaluate and implement reference ontologies. In IEEE 19th international enterprise distributed object computing workshop , pages 144-147.
- Guizzardi, G. (2005). Ontological Foundations for Structural Conceptual Models . PhD thesis.
- Guizzardi, G., de Almeida Falbo, R., and Guizzardi, R. S. (2008). Grounding software domain ontologies in the unified foundational ontology (ufo): the case of the ode software process ontology. In CIbSE , pages 127140.
- Lacy, L. and Gerber, W. (2004). Potential modeling and simulation applications of the web ontology languageowl. In Proceedings of the 2004 Winter Simulation Conference, 2004. , volume 1. IEEE.
- Marcus, K. M., Chan, K. S., Hardy, R. L., and Paul, L. Y. (2018). An environment for tactical sdn experimentation. In MILCOM 2018-2018 IEEE Military Communications Conference (MILCOM) , pages 1-9. IEEE.
- Tesolin, J., Silva, M., Campos, M. L. M., Moura, D., and Cavalcanti, M. C. (2020). Critical communications scenarios description based on ontological analysis. In ONTOBRAS , pages 212-218.
- Tzeng, Y. K., Hsu, I.-C., Cheng, Y. J., and Huang, D.-C. (2009). A semantic web approach for military scenario development. In 2009 Joint Conferences on Pervasive Computing (JCPC) , pages 321-326.
