## Towards a Reference Ontology for Digital Platforms

Thomas Derave 1( B ) , Tiago Prince Sales 2( B ) , Frederik Gailly 1( B ) , and Geert Poels 1( B )

1 Department of Business Informatics and Operations Management, Ghent University, Tweekerkenstraat 2, 9000 Ghent, Belgium

{thomas.derave,frederik.gailly,geert.poels}@UGent.be

2 Faculty of Computer Science, Free University of Bozen-Bolzano, Bolzano, Italy tiago.princesales@unibz.it

Abstract. Digital platforms can be categorized into different types including 'multi-sided platform', 'digital marketplace', 'crowdfunding platform', 'sharing economy platform' and 'on-demand platform'. As there is a lack of knowledge regarding the requirements and design of these digital platform types, we developed a method to design a digital platform reference ontology based on a taxonomy. The taxonomy provides an overview of digital platform properties, with the property values expressing the possible variations between digital platforms depending on their type. For each property value, we can create a digital platform reference ontology module using the five-step approach proposed by Ruy et al. [1] based on the patterns of the Unified Foundational Ontology (UFO). UFO is a high-level ontology that provides us with basic concepts for objects, events, social elements and their types, relations and properties. These digital platform reference ontology modules can be combined as building blocks to compose our reference ontology for expressing the functionality for digital platforms of all types. We believe this reference ontology can be a step towards a better understanding of digital platform functionality, better communication between stakeholders and eventually may facilitate future research and development of digital platforms.

Keywords: Digital platform · Multi-sided platform · UFO · Ontology · Taxonomy

## 1 Introduction

The platform economy refers to activities in business, culture and social interaction that are performed on or are intermediated by digital platforms [2]. Well-known examples of suchplatformsareAirbnb,eBay,Etsy,Ticketswap,Tinder,LimeandUber.Characteristic of the platform economy is that these activities were previously provided differently by firms [3, 4]. Information technology is the most important original enabling force of the platform economy. Therefore, the platform economy is not only a new economic phenomenon, but also a success of advances in information technology [5].

[FIGURE]

Existing digital platforms categorized in types like digital marketplace, on-demand platform and multi-sided platform, have a lot in common, but also have substantial differences in functionality. However, there is little research on the platform economy from the perspective of information technology, as most studies looked into business models and economic/societal impact [5]. Consequently, there is a lack of knowledge regarding the requirements and design of the different types of digital platforms. Therefore, it is not known whether software products for developing platforms, like the open-source Sharetribe Go [6] for creating sharing economy platforms, support all the functionality expected for a certain type of platform.

This paper contributes to filling the lack of knowledge of digital platform functionality by proposing a method using the patterns of the Unified Foundational Ontology (UFO) [7] to create a reference ontology. Following our method, the reference ontology will be based on a taxonomy that was already developed as a first part of this research project. The taxonomy gives an overview of digital platform properties, with the property values expressing the possible variations between digital platforms depending on their type. For each property value, we plan to create a digital platform reference ontology module. The entirety of these modules composes the reference ontology, which thus describes the general functionality of any digital platform and the more specific functionality of each digital platform type in relation to its property values as defined in the taxonomy. By organizing the ontology into modules, it is possible to select and combine modules to create a unique ontology for each digital platform type. Additionally, when new platform types arise, additional ontology modules can be added to the reference ontology. As a result, our reference ontology can accommodate the evolution of the sharing economy and combine existing and emerging platform variations to model new types.

We believe this reference ontology can be a step towards a better understanding of digital platform functionality. Apart from supporting communication between stakeholders in platform development, it can support ontology-driven development of platforms. Summarizing, the reference ontology is envisioned as a common language for expressing digital platform functionality that can be used to facilitate future research and development of digital platforms.

This paper is structured as follows; In Sect. 2 we provide background on the digital platform taxonomy created in previous research. In Sect. 3 we explain our methodology for creating the reference ontology. In Sect. 4 we present two modules of our ontology, as the other modules are work in progress. After, we discuss the validation of our ontology using an ontology expert. In Sect. 5 we discuss limitations and future research and in Sect. 6 we give the conclusion.

## 2 Background: Digital Platform Taxonomy

The digital platform taxonomy was created during previous research following the method of Nickerson et al. [8]. As background to the reference ontology design presented in this paper, we present a simplified version of the taxonomy development and resulting taxonomy schema.

First, a working definition of a digital platform was defined. Due to the dispersal of digital platform research across a number of fields, there is a miscellany of perspectives concerning a digital platform. To reach our objective, the working definition of a digital platform needs to be independent of its type. As we wish to cover a wide range of digital platform types, we relate the platform economy to the broader concept of service economy,andtherefore combine the knowledge of [2, 9-11] in defining a digital platform as 'a service offering by the digital platform management to the users that may be bound to an agreement. The primary service offered are interactions between users and these interactions are enabled by a software system'. This definition is very broad, as the intended interactions can consist solely of information transfer (e.g. WhatsApp, Tinder) but can also include offerings of products (e.g. eBay), services (e.g. Airbnb) or investments (e.g. Kickstarter).

Second, we searched for secondary studies (literature reviews) on digital platforms to identify digital platform types and their definitions. Our literature search ended up with six literature reviews [3, 12-16]. Out of these literature reviews and the primary sources they refer to (and which we also studied), nine digital platform types where identified: Multi-Sided (MS) platform [17]; transaction platform [18]; investment platform [11]; crowdfunding platform [19]; digital marketplace [20]; Peer-to-Peer (P2P) sharing and collaborative consumption platform [21]; sharing economy platform [22]; on-demand platform [23]; and second-hand P2P platform [18]. Third, we compared the definitions of these nine types to each other to identify the digital platform properties whose values distinguish between these types. And during the last step, we conceptualized and validated the properties and property values using a sample of existing platforms 1 . The resulting taxonomy schema is shown in Table 1.

Table 1. Digital platform taxonomy schema

| Pro p ert y          | V a l u es    | V a l u es    | V a l u es            | V a l u es            | V a l u es   | V a l u es   |
|----------------------|---------------|---------------|-----------------------|-----------------------|--------------|--------------|
| Market sides         | One-sided     | One-sided     | One-sided             | Multi-Sided           | Multi-Sided  | Multi-Sided  |
| Affiliation          | Registration  | Subscription  | Main Content Creation | Main Content Creation | Transaction  | Investment   |
| Centralization       | Decentralized | Decentralized | Decentralized         | Centralized           | Centralized  | Centralized  |
| Participation        | B2C           | B2B           | B2B                   | P2P                   | C2C          | C2C          |
| Offering orientation | Product       | Product       | Result                | Result                | User         | User         |
| Immediate access     | True          | True          | True                  | False                 | False        | False        |
| Under-utilized       | True          | True          | True                  | False                 | False        | False        |

Market sides [17] is the number of different groups of platform users. Affiliation [16] refers to different ways that users (per group) can be connected to the platform. Centralization [12, 24] is the way the users can connect to each other. This can be via a decentralized search by the users of one side, or via a centralized, automated matching by the platform software. Participation and offering orientation are only applicable if the platform has multiple sides. Participation [20, 25] indicates if the market that is intermediated by the platform is Business-to-Business (B2B), Business-to-Consumer (B2C), Consumer-to-Consumer (C2C) or Peer-to-Peer (P2P); the latter case holds when platform participants are considered as 'equals', where C2C is a specialisation of P2P when users of at least two sides are only allowed to be private persons. The offering orientation [26] differentiates between product selling, result-oriented services or useroriented offerings including leasing, renting, sharing and pooling of a product. Finally, immediate access and under-utilized capacity are only relevant for user-oriented offerings. A digital platform offers immediate access [27, 28] if the offering can be provided at the moment of ordering. Under-utilized [22] indicates excess capacity of the offered product.

## 3 Methodology

Our research methodology for building and evaluating the envisioned reference ontology for digital platforms is shown in Fig. 1 and explained below.

Fig. 1. Methodology

[FIGURE]

The taxonomy schema of Sect. 2 gives a structured overview of the properties and property values of digital platforms. Each unique combination of property values provides an intentional definition of a digital platform type, some of which might have an empty extension as no instances have been developed yet. Based on these intentional definitions, we develop the digital platform reference ontology. Our ontology development process uses the patterns of the UFO, a high-level ontology that provides us with basic concepts for objects, events, social elements and their types, relations and properties [7]. To create the reference ontology, we use the five-step approach proposed by Ruy et al [1].

1. Thefirst step is to modularize the digital platform domain. These modules are already provided by our taxonomy schema, as we create an ontology module for each property value. This means that the reference ontology can model any digital platform type that is defined by the taxonomy by combining the relevant ontology modules.
2. Asecond step is to define requirements for each module. These are the requirements that a digital platform has to fulfil to be defined as an instance of a certain digital platform type. First, we define the requirements related to the general functionality of any digital platform. For this, we reuse the literature-based working definition that we used for the taxonomy development in Sect. 2. After, requirements for the different property values are defined.
3. In a third step we develop the ontology. First, the requirements are modelled using Domain-Related Ontology Patterns (DROPs). A DROP represents a recurrent modelling fragment in a certain domain. Conform the approach of [1], we searched for core ontologies we can reuse. A digital platform can be seen as a service offering to its users, and depending on the type the users are able to offer services (apart from other types of product) through the digital platform. For part of the requirements we therefore reuse UFO-S [29], a core ontology that provides a clear account of servicerelated concepts, to extract DROPs. The other requirements are then modelled using DROPs directly reused from the foundational UFO ontology. All DROPs are developed by analogy [30], i.e. reproducing and completing the structure with the specific knowledge, using OntoUML [31], a UFO-based conceptual modelling language that is capable of representing objects, events and social entities. After, we combine the DROPsinto ontology modules; a general reference ontology module compliant with all digital platforms and a separate ontology module for each property value. In this paper we only present the one-sided and multi-sided ontology modules.
4. The fourth step is the validation. We use the method of [32] to define Competency Questions (CQs) as a set of queries that the ontology must be capable of answering in order to be considered competent for conceptualizing the domain it was intended for [33]. These CQs are asked to ontology experts to check if our ontology modules reflect what was expected of them. As long as the responses to the CQs are not in line with the requirements, the DROPs need to be remodelled to make sure our ontology captures the knowledge as needed.

## 4 Digital Platform Ontology

In a first sub-section, we present the general reference ontology module. This module is part of any ontology application that is created for a digital platform, independent of its type. In the second sub-section, we present two modules that describe the functionality related to the market sides property of our taxonomic schema: the 'one-sided' and 'multisided' platform ontology module. The value of this property depends on whether one or more than one distinctive group of platform users is served by the platform 2 . In the third sub-section, we discuss the ontology validation process and illustrate it for the ontology modules presented in the first and second sub-sections.

## 4.1 General Reference Ontology Module

Our working definition of a digital platform for the taxonomy development (see Sect. 2) was the following: 'A digital platform is a service offering by the digital platform management to the users that may be bound to an agreement. The primary service offered are interactions between users and these interactions are enabled by a software system'. Based on this working definition, we define the following requirements compliant to all digital platforms:

1. A digital platform is a service offering;
2. This service offering is offered by digital platform management towards a certain target platform user community consisting of target platform users;
3. This service offering is bound to an agreement between the platform user and the platform management.
4. This service offering is enabled by software;
5. Platform users may participate in platform-supported interaction between each other.

Based on these requirements we create the general ontology module, which is independent of platform type. Figure 2 shows this module, modelled in OntoUML, with a color coding referring to the sub-ontologies of UFO: UFO-A, an ontology of objects (in red); UFO-B, an ontology of events (in yellow); and UFO-C, an ontology of social constructs (in green and blue). A 'type' entity (in purple) is used for categorizing entities [34] of different sub-ontologies.

Figure 2 also shows how we modelled each requirement by means of a DROP. For the sake of clarity, the numbering of these DROPs is the same as the requirements. Requirements 1 to 3 are modelled with DROPs reused from the service domain ontology UFO-S. In UFO-S, a service offer is an event creating a social construct, or in this case a relatorKind as it has the ability to connect two entities. This relatorKind called 'service offering', connects a service provider and a target customer community and this service offering can eventually result in the establishment of another relatorKind called 'service agreement' [29]. These UFO-S patterns are than reused to model DROP 1 to 3.

[2 Other ontology modules are still work in progress and published at http://model-a-platform.com/ digital-platform-ontology/.](http://model-a-platform.com/digital-platform-ontology/)

Fig. 2. General module of the digital platform reference ontology (Color figure online)

[FIGURE]

Requirements 4 and 5 are more specific for digital platforms and could not be modelled by reusing DROPs extracted from UFO-S. However, we could model these requirements by reusing DROPs directly from the foundational ontology UFO.

The general module of the digital platform reference ontology can be read as follows. A digital platform is a service offering as defined in UFO-S (DROP1). The digital platform is offered by the organization managing the platform (a.k.a. platform management) towards a target platform user community. This community is a collection of target platform users and can be persons or organizations (DROP2). From the moment a target platform user is bound to an agreement (in this case a platform user agreement) with the platform management, he becomes a platform user (DROP3). The digital platform is enabled by the platform software (DROP4), that supports different kinds of platform supported actions. These platform supported actions are divided into user actions (i.e., platform actions performed by users), platform management actions (i.e., platform actions performed by platform management) and platform actions (i.e., autonomous platform actions). The most basic user actions are digital content creation (e.g., sending a message) and digital content consumption (e.g., receiving a message). When both creation and consumption take place, we talk about a communication action. To fulfil the fifth requirement of a digital platform, the platform software must allow platform user interaction (DROP5), which requires mutual communication between users (e.g., sending, receiving, replying, receiving).

## 4.2 Market Sides

Most businesses are operating in a market without enabling interactions between their customers, hence only supporting the direct interaction between a company and the customer, for which the market only favours from direct network effects [35]. In these cases, the market is defined as zero-sided . A digital platform, on the other hand, enables interactions between the customers, i.e., the platform users for which the market also flaviours indirect network effects. In case the platform users cannot be classified into types that have different interests in the service offering (e.g., as distinct groups of providers and consumers), the platform operates in a one-sided market and is defined as a o n e-sided platform [35]. The requirement for a one-sided platform is given below:

6. A one-sided platform is a digital platform (which is a service offering) towards a one-sided community of target users.

Theontology module for a one-sided platform is given in Fig. 3. The modelled DROP is reused from UFO-S.

Fig. 3. One-sided platform ontology module

[FIGURE]

Unfortunately, for M u lti-Sided (MS) ma r k ets there is no a clear and widely accepted definition [16]. The term was first used by noble price winners Rochet and Tirole [36] and defined as a market including at least two distinct but interdependent sides to have direct and clearly identified interactions with each other. Economically speaking, for a market to be MS it requires an increase in value to users on one side of the market with the number of participating users on another side [37]. This is known as 'cross-side network effects', sometimes referred to as 'indirect network effects'. The management of MS platforms (these are platforms operating in a MS market) typically face the chicken-andegg problem [38], having difficulties to find users of one side without having users of the other side. It is gradually becoming acknowledged that such platforms pose specific challenges to market regulation and innovation policy as this strategy has strong indirect network effects that can lead to dominant market power and monopolies [39]. As this paper focusses on the digital platform functionalities to aid in future platform software design, we leave the economical and regulatory requirements stated by [36, 37] and others out of scope and focuss on the enabling of interactions between users of different sides.

As stated by [17], users of each side need to be affiliated with the market. By 'affiliation', it is meant that users make a platform-specific investment to be able to interact to each other directly [16]. But how to define these platform-specific investments? Is someone searching an apartment in Airbnb before registration a user? Is an artist whose music is offered on Spotify without his formal acceptance a user? We narrow the affiliation definition of [16] as we did for our taxonomy and define a user as an agent that is registered, subscribed, has created main content, has entered in a transaction or has entered in an investment using the MS platform software.

Based on the literature, the requirements for a MS platform are constructed and given below:

7. A MS platform is a digital platform (which is a service offering) towards multiple sides.
8. Users of both sides are affiliated with the platform after a user affiliation action. This affiliation is a platform user agreement and can be by registration, subscription, main content creation, making a transaction or making an investment.
9. The software enabling the MS platform offering allows for interactions between the users of at least two sides

The ontology module for a MS platform is given in Fig. 4. DROP 7 is reused from UFO-S. DROPs 8 and 9 are reused from UFO.

Fig. 4. Multi-sided platform ontology module (part 1)

[FIGURE]

A digital platform can have different user roles that allow users to conduct certain actions. For most one-sided digital platforms, all users have equal participation rights (e.g. WhatsApp), but a MS platform has at least two roles (e.g. homeowners and renters on Airbnb). The user role can change by performing an affiliation action and the users of a different role are allowed to perform actions that for other roles are prohibited (e.g. create new accommodation offering for homeowners, book accommodation for customers). The requirements for the user roles of a MS platform are given below:

10. A MS platform ensures at least two user roles.
11. User instances of different roles are allowed to perform different user actions.

## 12. A user can change its user role by performing a user affiliation action.

The ontology module for the user roles is given in Fig. 5. All DROPs are reused from UFO.

Fig. 5. Multi-sided platform ontology module (part 2: user roles)

[FIGURE]

## 4.3 Ontology Validation with CQs

To validate the ontology, we define sets of CQ's for each ontology module. The CQs are formulated as queries and come forth out of the requirements as CQs play the role of a type of requirement specification against which the ontology can be evaluated [40]. As proposed by [32] these sets of CQs and the relevant ontology modules in OntoUML were given to an ontology expert with a profound knowledge and experience in ontologies (11 paperswritten), UFO(3paperswritten)andUFO-S(1paperwritten).After,wecompared the answers of the expert to the intended requirements, and in case of differences, the relevant DROP was remodeled, and the validation was repeated again. The full list of CQs, answers and our comparison to the requirements can be found at following link 3 .

Based on this validation, we concluded that the ontology modules in Figs. 2, 3 and 4 provided an accurate description of the requirements. Only in Fig. 5, the ontology module of MS platforms related to the user roles (part 2), we noticed that the complexity is still too high for the expert to fully comprehend the model. We plan to remodel and further evaluate this module.

## 5 Discussion

This paper is only a first step towards the reference ontology and proposes the method with three modules; The general digital platform module, the one-sided module and the multi-sided module. In the future we plan to further develop the digital platform reference ontology with a module for each property value of our taxonomy. These other ontology modules are still work in progress and published at following link 4 .

During this development, the ontology can be validated and further improved in three ways. First, we plan to expand the number of UFO and UFO-S experts used in Sect. 4.3, as the validation of only one expert is not sufficient. Second, we plan to apply our ontology to the existing digital platforms used in the development of our taxonomy. This way we make sure that our ontology includes the functionalities of a broad range of platforms. As an example, we apply our current ontology model to the meal delivery platform Uber Eats 5 in Fig. 6 (appendix). For a third validation, we plan to use the simulation method of [41] to identify anti-patterns. Otherwise, these anti-patterns capture error prone modelling decisions that can result in the creation of models that allow for unintended model instances (representing undesired state of affairs).

[3 http://model-a-platform.com/validation-of-the-digital-platform-reference-ontology/.](http://model-a-platform.com/validation-of-the-digital-platform-reference-ontology/)

[4 http://model-a-platform.com/digital-platform-ontology/.](http://model-a-platform.com/digital-platform-ontology/)

## 6 Conclusion

To increase the knowledge regarding the requirements and design of digital platforms and their types, we proposed our method to develop a digital platform reference ontology based on a taxonomy and presented three ontology modules. These types, including 'multi-sided platform', 'digital marketplace', 'crowdfunding platform', 'sharing economy platform' and 'on-demand platform' are partly similar, but also differ in many aspects including the functionality they offer to their users. Our ontology can help comprehend the complexity and functionality requirements of existing digital platform depending on their type.

The ability to see through the fog in the digital platform domain is important, as the complexity within this domain is ever increasing. For example in the transportation sector, Uber is planning to combine car, train, plane, bike and scooter (rental) services into one transaction to get the customers to their destination in the cheapest, convenient and fastest way possible. These combinations of platform types with different types of providers are also called mega-platforms [42], hybrid platforms [24] or integrated platforms [11] and have the ability to further shake up and interrupt out-dated markets.

So what can be the implications of our research? First of all it helps both researchers and practitioners in their communication and decision making, as the ontology can be used as a common language all stakeholders can understand. Second, it is possible for them to improve and enlarge this ontology and make it compatible with other research fields. At this point, the ontology mainly focusses on the functionality requirements. But since our method makes use of ontology modules, it is fairly easy to enlarge this ontology and create modules that include terminology, entities, relationships and social constructs of interrelated domains to aid in the regulation, business model creation and social responsibility fields of digital platforms. Third, ontology modeling can play an essential role in areas such as database design, information systems and software development [7]. It can help the decision-making of developers and entrepreneurs and support ontology-driven development of new platforms.

We acknowledge that there are some limitations to our research. First, the ontology is not yet validated using our sample of 48 existing platforms of different types and functionality. And even then, the sample only represents a small portion of the current digital platform domain. Second, our ontology only represents the current state of the digital platform domain, but developments will require modifications to the ontology.

[5 www.ubereats.com.](http://www.ubereats.com/)

Despite these limitations we believe that an ontology can be a vital tool to accelerate the development of new digital platforms and hopefully push the sector into a more alternative and socially responsible direction.

## Appendix

Fig. 6. Ontology application of Uber Eats

[FIGURE]

## References

1. Ruy, F.B., Guizzardi, G., Falbo, R.A., Reginato, C.C., Santos, V .A.: From reference ontologies to ontology patterns and back. Data Knowl. Eng. 109 , 41-69 (2017)
2. Kenney, M., Zysman, J.: The rise of the platform economy. Issues Sci. Technol. 32 , 61-69 (2016)
3. Görög, G.: The Definitions of sharing economy: a systematic literature review. Management 13 , 175-189 (2018)
4. Puschmann, T., Alt, R.: Sharing economy. Bus. Inf Syst. Eng. 58 , 93-99 (2016)
5. Yin, C., Wang, X., Rong, W., Wang, T., David, B.: A system framework for sharing economy. In: Proceedings 2018 IEEE 22nd International Conference Computer Supported Cooperative Work in Design, CSCWD 2018, pp. 779-784 (2018)
6. [Sharetribe: Sharetribe Go (2019). https://github.com/sharetribe/sharetribe](https://github.com/sharetribe/sharetribe)
7. Guizzardi, G.: Ontological Foundations for Structural Conceptual Models (2005)
8. Nickerson, R.C., Varshney, U., Muntermann, J.: A method for taxonomy development and its application in information systems. Eur. J. Inf. Syst. 22 , 336-359 (2013)
9. Wu, L.: Understanding collaborative consumption business model: case of car sharing systems. DEStech Trans. Mater. Sci. Eng. 403-409 (2017)
10. Apte, U.M., Davis, M.M.: Sharing economy services: business model generation. Calif. Manage. Rev. 61 , 104-131 (2019)
11. Evans, P.C., Gawer, A.: The rise of the platform enterprise a global survey. Cent. Glob. Enterp. 1-30 (2016)
12. Sutherland, W., Jarrahi, M.H.: The sharing economy and digital platforms: a review and research agenda. Int. J. Inf. Manage. 43 , 328-341 (2018)
13. Nguyen, S., Llosa, S.: On the difficulty to define the sharing economy and collaborative consumption - literature review and proposing a different approach with the introduction of 'collaborative services.' Journée la Relat. à la Marque dans un Monde Connect. 19-25 (2018)
14. Codagnone, C., Biagi, F., Abadie, F.: The passions and the interests: unpacking the 'Sharing Economy.' (2016)
15. Ranjbari, M., Morales-Alonso, G., Carrasco-Gallego, R.: Conceptualizing the sharing economy through presenting a comprehensive framework. Sustainability 10 (7), 2336 (2018)
16. Sanchez-Cartas, J.M., Leon, G.: Multi-sided platforms and markets: a literature review. SSRN Electron. J. 1-62 (2019)
17. Hagiu, A., Wright, J.: Multi-sided platforms. Int. J. Ind. Organ. 43 , 1-32 (2015)
18. Acquier, A., Daudigeos, T., Pinkse, J.: Promises and paradoxes of the sharing economy: an organizing framework. Technol. Forecast. Soc. Change 125 , 1-10 (2017)
19. Haas, P., Blohm, I., Leimeister, J.M.: An empirical taxonomy of crowdfunding intermediaries. In: 35th International Conference Information Systems Building a Better World Through Information Systems, ICIS 2014, pp. 1-18 (2014)
20. Täuscher, K., Laudien, S.M.: Understanding platform business models: a mixed methods study of marketplaces. Eur. Manag. J. 36 , 319-329 (2018)
21. Chasin, F., von Hoffen, M., Cramer, M., Matzner, M.: Peer-to-Peer Sharing and Collaborative Consumption Platforms: a Taxonomy and a Reproducible Analysis. Springer, Heidelberg (2018)
22. Frenken, K., Schor, J.: Putting the sharing economy into perspective. Environ. Innov. Soc. Transitions. 23 , 3-10 (2017)
23. Mamonova, Y.: Sharing Economy vs. On-Demand Economy: The Major Differences (2018)
24. Acquier, A., Carbone, V., Massé, D.: How to create value (s) in the sharing economy: business models. Scalability Sustain. 9 , 5-25 (2019)

25. Ehikioya, S.A.: A formal model of peer-to-peer digital product marketplace. Int. J. Networked Distrib. Comput. 6 , 143-154 (2018)
26. Ritter, M., Schanz, H.: The sharing economy: a comprehensive business model framework. J. Clean. Prod. 213 , 320-331 (2019)
27. Andersson, M., Hjalmarsson, A., Avital, M.: Peer-to-peer service sharing platforms: driving share and share alike on a mass-scale. In: Proceedings of 34th International Conference Information Systems, vol. 4, pp. 2964-2978 (2013)
28. Gobble, M.A.M.: Defining the sharing economy. Res. Technol. Manag. 60 , 59-61 (2017)
29. Nardi, J.C., et al.: A commitment-based reference ontology for services. Inf. Syst. 54 , 263-288 (2015)
30. Falbo, R.A., Guizzardi, G., Gangemi, A., Presutti, V.: Ontology patterns: clarifying concepts and terminology. CEUR Workshop Proc. 1188 , 14-26 (2013)
31. Guizzardi, Giancarlo., Fonseca, Claudenir M., Benevides, Alessander Botti., Almeida, João Paulo A., Porello, Daniele, Sales, Tiago Prince: Endurant types in ontology-driven conceptual modeling: towards OntoUML 2.0. In: Trujillo, Juan C., Davis, Karen C., Du, Xiaoyong, Li, Zhanhuai, Ling, Tok Wang, Li, Guoliang, Lee, Mong Li (eds.) ER 2018. LNCS, vol. 11157, pp. 136-150. Springer, Cham (2018). https://doi.org/10.1007/978-3-030-00847-5\_12
32. Bezerra, C., Freitas, F., Santana, F.: Evaluating ontologies with competency questions. In: Proceedings of 2013 IEEE/WIC/ACM International Joint Conferences on Web Intelligence Intelligent Agent Technologies - Work, WI-IATW 2013, vol. 3, pp. 284-285 (2013)
33. Gharib, M., Mylopoulos, J.: COPri - A Core Ontology for Privacy Requirements Engineering (2018)
34. Carvalho, V., Giancarlo, G., …: Extending the Foundations of Ontology-based Conceptual Modeling with a Multi-Level Theory. In: International Conference on Conceptual Modeling (2015)
35. Filistrucchi, L., Geradin, D., Van Damme, E., Affeldt, P.: Market definition in two-sided markets: theory and practice. J. Compet. Law Econ. 10 , 293-339 (2014)
36. Rochet, J., Tirole, J.: Platform competition in two-sided markets, pp. 5-6 (2001)
37. Hagiu, A.: Strategic decisions for multisided platforms. Polym. Eng. Sci. 58 , 928-942 (2018)
38. Evans, D.S.: The Antitrust economics of two-sided markets. SSRN Electron. J. 20 , (2005)
39. [Katharina, H.: Innovation comes from platforms rather than from individual applications. https://ec.europa.eu/digital-single-market/en/news/innovation-comes-platforms-rat her-individual-applications](https://ec.europa.eu/digital-single-market/en/news/innovation-comes-platforms-rather-individual-applications)
40. Asunción, G.-P., Mariano, F.-L., Oscar, C.: Ontological Engineering (2003)
41. Guizzardi, Giancarlo, Sales, Tiago Prince: Detection, simulation and elimination of semantic anti-patterns in ontology-driven conceptual models. In: Yu, Eric, Dobbie, Gillian, Jarke, Matthias, Purao, Sandeep (eds.) ER 2014. LNCS, vol. 8824, pp. 363-376. Springer, Cham (2014). https://doi.org/10.1007/978-3-319-12206-9\_30
42. Radonjic-Simic, M., Richter, S., Pfistere, D.: Reference Model and Architecture for the PostPlatform Economy (2019)
