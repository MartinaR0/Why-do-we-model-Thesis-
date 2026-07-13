## The Design of a Core Value Ontology Using Ontology Patterns

Frederik Gailly 1( &amp; ) , Ben Roelens 1( &amp; ) , and Giancarlo Guizzardi 2

1 Department of Business Informatics and Operations Management, Faculty of Economics and Business Administration, Ghent University, Ghent, Belgium

{Frederik.Gailly,Ben.Roelens}@UGent.be

2 Ontology and Conceptual Modeling Research Group (NEMO), Computer Science Department, Federal University of Esp í rito Santo, Vit ó ria, Brazil

gguizzardi@inf.ufes.br

Abstract. The creation of value is an important concern in organizations. However, current Enterprise Modeling languages all interprete value differently, which has a negative impact on the semantic quality of the model instantiations. This issue need to be solved to increase the relevance of these instantiations for business stakeholders. Therefore, the goal of this paper is the development of a sound Core Value Ontology. In order to do that, we employ a pattern-based ontology engineering approach, which employs the Uni fi ed Foundational Ontology.

Keywords:

Value

Core ontology

UFO

Ontology patterns

## 1 Introduction

Creating value is an important purpose of the economic activities that are performed by companies to sustain their long-term viability. Therefore, the concept has been studied by a wide range of Enterprise Modeling languages. ArchiMate, which is oriented towards Enterprise Architecture, de fi nes value as what a party gets by selling or making available some product or service, or it may apply to what a party gets by buying or obtaining access to it [16]. In the context of Business Model Design, the Value Delivery Modeling Language (VDML) speci fi es value as a measurable benefit delivered to a recipient in association with a deliverable [11]. On an aggregated level, the values that are associated with a deliverable are embodied in a value proposition [11]. A similar idea is adopted in Requirements Engineering by e 3 -value [4], which uses a value proposition to describe the creation of value in a constellation of multiple actors. This concept is speci fi ed as something that is offered by a party for consideration or acceptance by another party [4]. These examples show that a general semantic agreement is currently still missing for the Value domain [5], which endangers the semantic quality of resulting model instantiations. Solving this issue is important, as models with a bad semantic quality are not corresponding with the targeted problem domain, which lowers their relevance for business experts [8].







Semantic agreement about the notion of Value can be realized by the development of a core ontology. A core ontology provides a semantic characterization of the core terms used in a specific field that spans different application domains, with the purpose of minimizing ambiguities and misunderstandings [10]. In this context, a core ontology should combine the following characteristics: axiomatization and formal precision, modularity, extensibility, reusability, and separation of concerns [15]. These characteristics can be supported by making sure that the developed ontology: (i) is based on a foundational ontology, (ii) follows a pattern-oriented design approach, and (iii) is applicable in arbitrary application domains.

Although a sound core ontology was previously developed in the domain of services [10], it is currently still missing for the Value concept. To this end, the goal of this paper is the development of a Core Value Ontology, which is (i) grounded in the Uni fi ed Foundational Ontology (UFO). Furthermore, the development of the ontology will be guided by an engineering approach, which (ii) is explicitly oriented towards supporting reuse by systematically using ontology patterns [13]. Finally, the use of the Core Value Ontology is demonstrated (iii) by applying it on an existing healthcare case.

## 2 Methodology

The Core Value Ontology is developed by following the ontology engineering approach proposed by Ruy et al. [13]. This approach makes use of ontology design patterns, which describe particular recurring modeling problems that arise in speci fi c ontology development contexts and present a well-proven solution for this problem [2]. Speci fi c for the approach of Ruy et al. is that a distinction is made between foundational ontology patterns (FOPs) and domain -related ontology patterns (DROPs) . A FOP is a fragment of a foundational reference ontology, which spans across many fi elds and models the very basic and general concepts and relations that make up the world [6]. In contrast, a DROP is a fragment of a core ontology, which captures the core knowledge related to a domain. The ontology engineering process that is followed within this paper also recognizes that DROPs of related core ontologies can be reused while developing a new core ontology. This ontology engineering process consists of three steps, of which the results can be consulted in Sect. 4:

1. First, a set of FOPs are extracted from the UFO foundational ontology. UFO is useful for creating a Core Value Ontology because it comprises a number of notions that fundamentally explain the notion of value including the notions of goals, capabilities, actions, and intentions. As discussed in [13], the FOPs extracted from UFO are considered as the relevant building blocks for the Core Value Ontology and will be either reused during the development of the Core Value Ontology or will be used to analyze existing DROPs of related core ontologies;
2. Second, a set of DROPs is extracted from related core ontologies and existing enterprise modeling languages. For every DROP, it should also be clear how this DROP reuses a FOP that was extracted in the previous step.
3. In the fi nal step, the Core Value Ontology will be constructed by integrating the identi fi ed DROPs. This integration is founded on generally accepted domain

knowledge about the Value concept. Moreover, it makes use of the FOPs identi fi ed in the previous steps to connect the different DROPs.

## 3 Building the Core Value Ontology

Foundational Ontology Patterns. UFO consists of three main modules: UFO-A, UFO-B and UFO-C. UFO-A describes Endurants and their ties. In a nutshell, Endurants are entities that persist through time, possibly changing qualitatively while maintaining their identity [7]. UFO-B describes Perdurants or Events . UFO-C uses UFO-A and UFO-B to de fi ne a foundational ontology for social entities, which is very relevant for de fi ning enterprise concepts.

Figure 1 depicts the Endurant FOP. These Endurants can be divided into Substantials and Moments . Substantials are existentially independent individuals and can be further specialized in Objects , Agents and Situations . Agents are substantials that can bear special types of moments, named Intentional Moments (see Agent FOP). Objects and Situations are non-agentive substantial individuals. Objects are Endurants that are existentially independent (e.g., a Person, a Car, an Organization); Moments , in contrast, are individuals that can only exist in other individuals, and are thus existentially dependent on other individuals (e.g., an electric charge in a conductor, John ' s headache). Moments can be further specialized in Relators and Intrinsic Moments . Intrinsic Moments are moments that inhere in one single individual. Relators are further explained by FOP 2. Situations are complex entities that are constituted by possibly many Endurants (including other situations). Situations are taken here to be synonymous to what is named a state of affairs in the literature, i.e., a portion of reality that can be comprehended as a whole. Examples include ' John having fever and influenza ' , ' John being in the same location as Paul, while Mary is in the same location as David ' , and ' Mary being married to Paul who works for Ghent University ' .

Fig. 1. Endurant FOP

[FIGURE]

In Fig. 2, Relators are considered as Moments that are existentially dependent on two or more Endurants . When mediated by a Relator, an Endurant plays a role in a certain context.

Fig. 2. Relator FOP

[FIGURE]

Figure 3 further speci fi es the Agent concept, which is de fi ned as a specialization of a Substantial. As such, an Agent represents an entity that is capable of bearing Intentional Moments , such as Beliefs , Desires , and Intentions . Every Intentional Moment has an associated Proposition , which is called the propositional content of the Moment . The propositional content of an Intentional Moment can be satis fi ed by Situations in reality.

Fig. 3. Agent FOP

[FIGURE]

Dispositions are Intrinsic Moments that are only manifested in particular Situations , but that can also fail to be manifested (see Fig. 4). When manifested, they are manifested through an occurrence of Events .

Fig. 4. Disposition FOP

[FIGURE]

In the Intention FOP of Fig. 5, the propositional content of an Intention is termed a Goal . Actions are intentional Events , i.e., events with the speci fi c purpose of satisfying (the propositional content of) some Intention of an Agent .

Fig. 5. Intention FOP

[FIGURE]

Domain-related Ontology Patterns. Extraction of relevant DROPs for the development of the Core Value Ontology is less straightforward because of the limited availability of related core ontologies (with exception of UFO-S, which is a core ontology for services). In this paper, three relevant DROPs are created by looking at the reference ontologies that were used to develop some well-know enterprise modelling languages (e.g., the Business Model Ontology (BMO) [12], the TOVE ontological framework [4], e3-value [5], the Service Science discipline [9], ArchiMate [1] and ARIS [14]). Some of these sources explicitely de fi ne a reference ontology which can be used to extraxt the DROPS ' s. Others implicitly use a reference ontology to de fi ne the concepts of the enterprise modelling language or to analyze the semantics of the modeling language. In the next paragraphs, the DROPs that are extracted from the reference ontologies (see Figs. 6, 7, 8) are described in more detail. Additionally, the UML stereotype mechanism will be used to indicate how these DROPs are related to the previously selected FOPs.

The fi rst DROP focuses on the Value Proposition concept. This concept has its origin in the BMO, Service Science, and e3-value. Within the BMO, the concept is de fi ned as an overall view of a company ' s bundle of products and services that are of value to the customer [12]. This view is shared within Service Science who consider the concept as the potential value that is offered to a customer [17]. A last important aspect of the Value Proposition concept is stressed within e3-value, within which this concept is speci fi ed as follows: something that is offered by a party for consideration or acceptance by another party [4]. The condition of acceptance is important here as it differentiates the Value Proposition from the actual value co-creation between a company and its customers (see DROP 2). In Fig. 6, a Value Proposition is identi fi ed as an UFO Relator , which connects the Recipient and Provider as two Agents that are because of their connection with the Value Proposition Relator also Roles.

Fig. 6. Value proposition DROP

[FIGURE]

The second DROP is oriented towards value co-creation. The Service Science discipline agrees with the fact that value is always the result of a co-creation between the company (i.e., the Provider ) and its customers (i.e., the Recipient ) [17]. Both parties are considered as a dynamic con fi guration of resources, which apply Capabilities during the value co-creation process [17]. According to the BMO, a Capability is the ability to execute a repeatable pattern of Actions that is necessary in order to create value for the customer [12]. Based on TOVE [3], the role of the Action can be further re fi ned. When Actions are performed, the world changes from one situation to another. A Caused state de fi nes what is true of the world once the activity has been completed. The modeling of this pattern and its grounding in UFO is based on the research in [1], which analyzes Capabilities as de fi ned in ArchiMate.

Fig. 7. Value co-creation DROP

[FIGURE]

The third DROP focuses on value measurement. De fi ning appropriate value measures is important as value is not transferred between a recipient and a provider but is uniquely determined by the customer [17]. In this respect, the measurement is based on their level of satisfaction with a particular value [11]. More speci fi cally, this Satisfaction Level is determined by the customer ' s perception of the solution of a problem in a given situation [3]. The Satisfaction Level is a UFO Belief that is by means of its Proposition connected to the Goal of a Recipient (i.e., the propositional content of an Intention ) and a particular Situation that is the result of an action.

Fig. 8. Value measurement DROP

[FIGURE]

Core Value Ontology. The Core Value Ontology that is proposed in this paragraph is the result of an integration of the previously de fi ned FOPs and DROPs (see Fig. 9). Central in the Core Value Ontology is the Recipient concept, which is common to the three important value aspects: (i) value proposition (see Fig. 6), (ii) value co-creation (see Fig. 7), and (iii) value measurement (see Fig. 8). While the Provider also plays an import role in the offering of the value proposition and in the co-creation of value, this is not the case for the actual value measurement. Furthermore, the Caused State (as an instantiation of a UFO Situation ) appears in both the value co-creation (i.e., DROP 2) and value measurement (i.e., DROP 3) patterns. This can be explained as there is a clear relation between these two aspects. Indeed, the outcome of the Actions that are performed during the value co-creation will impact the perceptions of the Recipient about the Problem Solution and its resulting Satisfaction Level .

## 4 Healthcare Use Case Illustration

The healthcare case is a case that studies the value of remote monitoring of high-risk pregnancies, which was originally developed to illustrate the VDML meta-model and notation. In this paper, the description of the case is limited to those concepts that are relevant in the context of the developed ontology 1 .

The illustration of the Core Value Ontology by the healthcare use case can be found in Fig. 10. In the context of a high-risk pregnancy, it is not straightforward for a hospital to provide valuable maternity care to a pregnant client. Although the future mother bears the intention to obtain maternity care by having frequent examinations, these trips to the doctor ' s of fi ce pose a possible risk for the unborn child. This problem can have a serious impact on the satisfaction level of the pregnant client with the maternity care service, which is measured by four distinct criteria: (i) the cost of care, (ii) the total duration of the hospitalization, (iii) the risk of death of the mother, and (iv) the risk of death of the child. To better satisfy these conflicting goals, the hospital wants to use new monitoring devices. These devices are lent by the hospital to high-risk pregnant clients as they possess the capability of remote monitoring of the future mother and unborn child by creating and sending automatic health reports. These reports can subsequently be analyzed by the doctor who is responsible for monitoring the high-risk patient. These actions will result in a situation where high-risk patients receive a continuous follow-up by doing limited physical efforts. While the limited physical efforts support the client ' s goal of minimizing their visits to the doctor ' s of fi ce, the continuous follow-up satis fi es the need of having frequent examinations in case of a high-risk pregnancy. This should increase the value of the maternity care that is received by these patients.

1 The interested reader can consult the VDML healthcare use case via: http:// fi les.modelbased.net/ vdml/12-11-11.pdf.

Fig. 9. Core Value Ontology

[FIGURE]

Besides the illustration of the Core Value Ontology, we also want to show how it relates to Enterprise Modeling fragments that are oriented towards the Value concept. Therefore, illustrative fragments can be found for e3-value (see Fig. 11), ArchiMate (see Fig. 12), and VDML values (see Fig. 13). The focus of the e3-value fragment is on the exchange of the maternity care services (i.e., a value object) between the hospital (i.e., an actor) and the high-risk pregnant client (i.e., a market segment). As a compensation for these services, the client will pay money to the hospital. Furthermore, the responsibility of the hospital for executing the activity of monitoring the high-risk patients is also incorporated. This activity is the end of a scenario path, which starts with the need of the future mother to obtain maternity care (see dotted lines).

Within the ArchiMate Business Layer, several constructs comply with the developed Core Value Ontology. Furthermore, the relations between the different concepts can be instantiated as general association relationships. As such, the maternity care services are considered as a business service that is exchanged between the hospital and the high-risk pregnant client (i.e., two actors). Furthermore, the monitoring device can be modeled as a business object that has the function of creating automatic health reports. This business function is manifested by the business event of monitoring the high-risk patient, which results in a situation that determines the maternity care value (i.e., an ArchiMate value). This value refers to two goals of the future mother: (i) have frequent examinations and (ii) minimize visits to doctor ' s of fi ce. These goals are part of the Motivation Extension within ArchiMate. The VDML values fragment focuses on the speci fi c criteria that determine the value of the maternity care service. These criteria are: (i) the duration of hospitalization, (ii) the cost of care, (iii) the risk of death of the mother, and (iv) the risk of death of the child. The negative impact on the resulting value is depicted by the minus sign inside the hexagons.

Fig. 10. Core Value Ontology illustration

[FIGURE]

Fig. 11. e3-value fragment

[FIGURE]

Fig. 12. ArchiMate fragment

[FIGURE]

Fig. 13. VDML values fragment [11]

[FIGURE]

## 5 Conclusion and Discussion

In this paper, a Core Value Ontology is built to realize semantic agreement about the Value concept. This ontology combines the following characteristics: axiomatization and formal precision, modularity, extensibility, reusability, and separation of concerns. In this respect, the Core Value Ontology was built on UFO, which is a foundational ontology that has been developed based on theories from Formal Ontology, Philosophy of Language, Linguistics and Cognitive Psychology. As such, we ensured the axiomatization and formal precision of the Core Value Ontology [15], which supports its further validation in future research. The modularity of the proposed ontology was realized by the identi fi cation of three relevant DROPs that originate from related enterprise domain ontologies and the analysis of enterprise modeling semantics. This modularization is important to ensure the extensibility and reusability of the proposed ontology [15]. Reusability can be further realized by using the Core Value Ontology to analyze and integrate Enterprise Modeling languages that focus on value. The focus of this analysis is on using the Core Value Ontology to better understand the semantics of these languages with the aim of linking them with related techniques, which focus on business concepts as capabilities, goals, resources, and services. In future research the Core Value Ontology will be formalized in order to improve the formal precision of the proposed ontology.

## References

1. Azevedo, C., Iacob, M., Almeida, J., Van Sinderen, M., Pires, L., Guizzardi, G.: Modeling resources and capabilities in enterprise architecture: a well-founded ontology-based proposal for archimate. Inf. Syst. 54 , 235 -262 (2015)
2. Falbo, R., Guizzardi, G., Gangemi, A., Presutti, V.: Ontology patterns: clarifying concepts and terminology. In: Gangemi, A., et al. (ed.) ISWC 2013, vol. 1188, pp. 14 -26. CEUR (2013)
3. Fox, M., Barbuceanu, M., Gruninger, M., Lin, J.: An organization ontology for enterprise modelling. In: Prietula, M., et al. (eds.) Computational Model of Institutions and Groups, pp. 131 -152. AAAI/MIT Press, Menlo Park (1997)
4. Gordijn, J., Akkermans, H.: Value-based requirements engineering: exploring innovative e-commerce ideas. Requirements Eng. J. 8 (2), 114 -134 (2003)
5. Gr ö nroos, C., Voima, P.: Critical service logic: making sense of value creation and co-creation. J. Acad. Mark. Sci. 41 (2), 133 -150 (2013)
6. Guarino, N.: Formal ontology and information systems. In: FOIS 1998, pp. 3 -15. IOS Press, Trento (1998)
7. Guizzardi, G.: Ontological Foundations for Structural Conceptual Models. UTwente, The Netherlands (2005)
8. Lindland, O., Sindre, G., S ø lvberg, A.: Understanding quality in conceptual modeling. IEEE Softw. 11 (2), 42 -49 (1994)
9. Maglio, P., Vargo, S., Caswell, N., Spohrer, J.: The service system is the basic abstraction of service science. Inf. Syst. E-Bus. Manage. 7 (4), 395 -406 (2009)
10. Nardi, J., Falbo, R., Almeida, J., Guizzardi, G., Pires, L., van Sinderen, M., Guarino, N., Fonseca, C.: A commitment-based reference ontology for services. Inf. Syst. 51 , 263 -288 (2015)
11. OMG: Value Delivery Modeling Language (VDML) (dtc/2014-04-05) (2014)
12. Osterwalder, A., Pigneur, Y., Tucci, C.: Business Model Generation: A Handbook for Visionaries, Game Changers, and Challengers. Wiley, Hoboken (2010)
13. Ruy, F.B., Reginato, C.C., Santos, V.A., Falbo, R.A., Guizzardi, G.: Ontology engineering by combining ontology patterns. In: Johannesson, P., Lee, M.L., Liddle, S.W., Opdahl, A.L., L ó pez, Ó .P. (eds.) ER 2015. LNCS, vol. 9381, pp. 173 -186. Springer, Heidelberg (2015). doi:10.1007/978-3-319-25264-3\_13
14. Santos Jr., P., Almeida, J., Guizzardi, G.: An ontology-based analysis and semantics for organizational structure modeling in the ARIS method. Inf. Syst. 38 (5), 690 -708 (2013)
15. Scherp, A., Saathoff, C., Franz, T., Staab, S.: Designing core ontologies. Appl. Ontol. 6 (3), 177 -221 (2011)
16. The Open Group: ArchiMate® 2.1 Speci fi cation (2013)
17. Vargo, S., Lusch, R.: Evolving to a new dominant logic for marketing. J. Mark. 68 (1), 1 -17 (2004)
