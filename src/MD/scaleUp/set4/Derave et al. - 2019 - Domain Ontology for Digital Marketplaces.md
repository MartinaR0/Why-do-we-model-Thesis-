## Domain Ontology for Digital Marketplaces

Thomas Derave 1( &amp; ) , Tiago Prince Sales 2 , Micha ë l Verdonck 1 , Frederik Gailly 1 , and Geert Poels 1

1 Department of Business Informatics and Operations Management, Ghent University, Tweekerkenstraat 2, 9000 Ghent, Belgium

{thomas.derave,michael.verdock,frederik.gailly, geert.poels}@UGent.be

2 Faculty of Computer Science, Free University of Bozen-Bolzano, Bolzano, Italy

tiago.princesales@unibz.it

Abstract. Recently the sharing economy has emerged as a viable alternative to ful fi lling a variety of consumer needs. As there is no consensus on the de fi nition of ' sharing economy ' we use the term ' marketplace ' to refer more speci fi cally to Internet/software-based sharing economy platforms connecting two different market segments. In the fi eld of sharing economy and marketplaces we found a research gap concerning the (socio)technological aspects and the development of marketplaces. A marketplace ontology can help to have a clear account of marketplace concepts which will facilitate communication, consensus and alignment. In this paper we design this marketplace ontology in four steps. First the selection of UFO as foundation and UFO-S as core ontology. Second the search for a set of minimal conditions and properties common for marketplaces and the derivation into competency questions. Third, use the competency questions to identify fragmented sub-ontology pieces called Domain-Related Ontology Patterns (DROPs) and apply them informally by extending UFO-S concepts to design a marketplace domain ontology. This marketplace domain ontology is represented in OntoUML. The last step is the validation of the OntoUML model using expert knowledge.

Keywords: Digital marketplace  Sharing economy  Marketplace ontology  UFO-S  OntoUML

## 1 Introduction

The use of sharing economy platforms like Airbnb and Uber is on the rise. The sharing economy has emerged as a viable alternative to ful fi lling a variety of consumer needs, ranging from prepared meals to cars to overnight accommodations, that were previously provided by fi rms. As the size of the sharing economy has grown, so has the magnitude of its economic and societal impacts [1]. The sharing economy is also an emerging and fast-growing academic fi eld. Based on the current state of the art overview by Trabucchi et al. [2], studies of the sharing economy have focused on three themes: (1) the customers motivation of using these platforms [3]; (2) the impact on society, market and policy [4, 5]; and (3) classi fi cations of sharing economy business models with a dominant focus on the revenue model and pricing mechanism [4, 6, 7]. Problematic for academic studies is that ' sharing economy ' is an umbrella concept and there is no consensus on what de fi nition, activities and core building blocks it comprises [8]. In this paper we will follow Laudien and T ä uscher [9] and base our research on the better-de fi ned term ' marketplace ' to refer more speci fi cally to Internet/softwarebased sharing economy platforms. This might provide a useful lens to overcome the challenges in de fi ning the boundaries of the sharing economy as currently experienced by the related literature [9]. The most adopted de fi nition of marketplace is the following: ' Marketplaces employ a special type of business model known as a multisided platform that connects two different market segments which value each other ' s presence whereas the actual transactions with customers are processed by the marketplace ' [10, 11]. Previous marketplace research focused mainly on the business-tobusiness market [12 -14].

© Springer Nature Switzerland AG 2019

G. Guizzardi et al. (Eds.): ER 2019 Workshops, LNCS 11787, pp. 191 -200, 2019.

[FIGURE]

The literature of both the sharing economy and marketplaces only offers a very partial view, and just started with research on consumer-to-consumer markets and business models from the perspective of the marketplace itself [9]. There is a lack of research concerning the (socio)technological aspects, the development and the innovations patterns diffusion of marketplaces and sharing economy platforms [2, 15]. This paper contributes to fi lling this gap by creating a domain ontology for all marketplaces.

A marketplace ontology can help to have a clear account of marketplace concepts which will facilitate communication, consensus and alignment [16]. For example, the terminology and interconnections of concepts such as ' listing ' , ' transaction ' ' marketplace ' and ' review ' can be better de fi ned and visualized for better communication between the developer and other stakeholders of a marketplace. A common terminology and understanding will help future discussions, marketplace developments and research. Nowadays most people know the sharing economy only through huge companies like Airbnb and Uber paying low wages, avoiding taxes and using their winner takes all model to become a monopolist [17]. Increasing the knowledge of marketplace related concepts can, for instance, be vital for the development of smaller, more alternative and socially responsible marketplaces and can thus contribute to the creation of a more socially responsible sharing economy.

In the next section we explain the methodology used to design the marketplace domain ontology. In Sect. 3 we provide background information on marketplaces. In Sect. 4 we develop the marketplace domain ontology and in Sect. 5 we summarize the paper, give a conclusion and outline our future research.

## 2 Methodology

To design a marketplace domain ontology we will use the method of [18] consisting of four steps.

First, we searched for an appropriate foundation and core ontology and if needed divide it into sub-ontologies. As foundation ontology we use the Uni fi ed Foundational Ontology (UFO) [19] and as core ontology we decided to use UFO-S [16], a commitment-based service ontology concerning the establishment and ful fi llment of commitments and claims between service participants. UFO-S is already modularized into three sub-ontologies called service offering, service negotiation and service delivery.

Second, we search for conditions in the literature to classify an organization as a marketplace. We call these conditions Minimal Marketplace Requirements (MMRs). We also add a set of properties that are common for most, but not all marketplace types. We base these Common Marketplace Properties (CMPs) on [9]. We further group and rephrase these MMRs and CMPs to competency questions (CQs), which are needed for performing the next step of the method of [18].

Third, we use the CQs to identify fragmented sub-ontology pieces called DomainRelated Ontology Patterns (DROPs) and Foundational Ontology Patterns (FOPs). DROPs and FOPs are reusable fragments extracted from reference domain/core ontologies and foundational ontologies respectively, packaging the knowledge related to the marketplace domain [20]. We apply them informally by extending UFO-S concepts to design a marketplace domain ontology and represent our marketplace domain ontology in OntoUML [16].

The last step is the validation of the ontology done by UFO and UFO-S experts answering the CQ ' s using the OntoUML model. If the response differed from the intended outcome, changes to the model were made and the process was repeated until no more changes were needed. We also fi tted the example of Airbnb into our model as a second validation of the ontology.

## 3 Background

To give the reader a better understanding of the basic functioning of marketplaces, we give an overview in Fig. 1.

Fig. 1. Marketplace overview

[FIGURE]

Providers and customers can subscribe on the marketplace platform that can be reached via a site or mobile application. A provider can freely offer a service on the marketplace platform which is called a listing (e.g., an apartment on Airbnb or a concert ticket on Ticketswap). A customer can search through the listings on the marketplace platform for the service he wants. After the customer located the desired service, he or she can make a transaction by acquiring the service via the marketplace platform. After the delivery of the service he or she can leave a review and previous reviews can help customers to fi nd the best service to their needs. A provider and customer can be a person or an organization, and it ' s possible to be a provider and customer on the same platform. The conversation system is important to create information transparency. This way a customer can receive more information about a listing or transaction. The booking system is dependent on the type of marketplace. For Uber, the system will check the closest available car dependent on the preferences of the customer. In case of Airbnb, the system checks availability and informs the customer whether the accommodation is free or not. The money is transferred through the payment system from the customer to the provider, with a transaction fee for the marketplace itself. It is important to state that this simple overview covers common types of marketplace, but not necessarily all types.

## 4 Marketplace Domain Ontology

A domain ontology can be a specialization of foundation ontologies (by analogy) and/or core ontologies (by extensions). The reason for using UFO-S as core ontology is that marketplaces are primarily used as digital intermediaries to allow service provisioning. Also, the three sub-ontologies of UFO-S, named service offering, service negotiation and service delivery, are closely related to the process flow of using marketplaces. UFO is the foundation ontology of UFO-S, and therefore ideal to use for specializations of the marketplace domain outside of the service domain. Therefore, we decided to design the marketplace domain ontology as a specialization of the UFO foundation and UFO-S core.

After selecting the foundation and core ontology, we start with the development of the minimum marketplace requirements (MMRs) and common marketplace properties (CMPs). Previous research proposes four conditions or MMRs for classifying an organization as a digital marketplace [9, 21, 22]:

1. A digital marketplace connects independent actors from a demand and supply side (individuals or organizations) via a digital platform. These individual actors can participate on both sides.
2. These actors enter direct interactions with each other (on the platform) to initiate and realize commercial transactions.
3. The marketplace platform provides an institutional and regulatory frame for transactions.
4. The marketplace does not substantially produce or trade products or services itself.

Based on the marketplace properties of Laudien and Tauscher [9] and marketplace functions of Bakos [22], we identi fi ed four CMPs:

1. The common de fi nition of the offered service by the provider is called a listing.
2. It is common for a marketplace to have a web-based platform and/or a mobile application to present the listings offered by the providers.
3. After the transaction it is common for a marketplace to manage the payment transfer from customer to provider.
4. After the transaction it is common for a marketplace to allow a review from the customer concerning the transaction.

We translate these MMRs and CMPs into three lists of CQs. Each list is related to a UFO-S sub-ontology. Hence these lists address respectively CQs related to marketplace service offering, marketplace service negotiation and marketplace service delivery. These different lists of CQs are a natural guide for driving the process of creating a domain ontology as a specialization of the UFO-S sub-ontologies. This was not a linear process. After creating a fi rst version the ontology was validated by UFO-S experts answering the CQ ' s using the OntoUML model. If the response differed from the intended outcome, changes to the model were made and the process was repeated until no more changes were needed.

## 4.1 Marketplace Offering Sub-ontology

A list of CQs influencing the marketplace offering sub-ontology is given below:

- What is a marketplace? (MMR1, MMR4)
- What is a listing? (MMR1, CMP1)
- What is a marketplace platform (MMR1, MMR2)
- Who is involved in a listing? (MMR1)
- How is a listing described? (CMP1, CMP2)

A marketplace is an organization managing one to multiple digital platforms. A listing is the service offered on the marketplace platform, hence is a subclass of the UFO-S service offering. The listing is the interaction between three actors: the marketplace platform; a marketplace provider who offers the listings and the potential marketplace community as the target of the provider who might be willing to buy the service using the platform. The listing description is a category specialized into the type ' s as web page and application page. During the validation the marketplace entity was split into a role which is the company or organization and the relator, which is the digital platform where the listings are visualized.

In case of Airbnb, the organization manages two platforms, one offering places to stay and another offering experiences (activities organized by locals). An apartment owner can offer his apartments as listings on the ' places to stay ' platform. The potential marketplace community can search through all the apartments on the platform via the descriptions visible on the Airbnb site or app (Fig. 2).

Fig. 2. Offering sub-ontology

[FIGURE]

## 4.2 Marketplace Negotiation Sub-ontology

A list of CQs influencing the marketplace negotiation sub-ontology is given below:

- What is a marketplace conversation? (MMR2)
- Who is in involved in a transaction? (MMR2, MMR4)
- What is a transaction? (MMR2, MMR3)

The marketplace conversation between a marketplace provider and a target marketplace customer concerning a certain listing is via a conversation system transferred by the marketplace platform. This conversation can result in a transaction. A transaction is the agreement between the booked marketplace provider and the marketplace customer concerning a listing. In the marketplace domain there is a restriction on the cardinalities allowing only one target marketplace customer to participate in a conversation and only one marketplace customer to be bound to a transaction.

For Airbnb, a conversation is transferred by the platform between the apartment owner and interested customers searching for a holiday rental. Every conversation refers to a certain apartment, and the conversation can result in a booking of the apartment in question (Fig. 3).

Fig. 3. Negotiation sub-ontology

[FIGURE]

## 4.3 Marketplace Delivery Sub-ontology

A list of CQs influencing the marketplace delivery sub-ontology is given below:

- What is a payment? (CMP3)
- What is a review? (CMP4)
- Who is involved in a payment (CMP3)
- Who is involved in a review (CMP4)

In case of a transaction, none (when free) to multiple payments are made by the marketplace customer to the booked marketplace provider. After the marketplace delivery, the customer can create a review. This review is collected by the marketplace platform. For the marketplace domain the cardinalities of the marketplace customer are always restricted to one. During the validation the relators ' Payment ' and ' Review ' and their relationships where further re fi ned.

For Airbnb, after booking the apartment the customer makes the payment and spends his/her holidays in the apartment. This service can also include fresh towels, free soap, etc. After the delivery the customer can write a review, and these are collected by the marketplace platform to provide more insights for future customers (Fig. 4).

Fig. 4. Delivery sub-ontology

[FIGURE]

## 5 Conclusion

In this paper we designed a marketplace domain ontology as an extension of the UFO-S core ontology for services. For the foundation of our marketplace domain ontology we used competence questions (CQs) based on the minimal marketplace requirements (MMRs) and common marketplace properties (CMPs) derived from previous literature. The design of the marketplace was done using the method of [18] and visualized in OntoUML.

A restriction of our research is the lack of literature sources for deriving the MMPs and CMPs, hence CQs. A systematic literature review of marketplaces could result in additional sources, however, in absence of these an empirical validation of our ontology with a sample of existing marketplaces could provide a viable alternative. By using different types of existing marketplaces and validate them with our model we can further expand the ontology. In future research, we will also formalize sub-ontology fragments linked to individual CQs as Domain-Related Ontology patterns (DROPs) and Foundational Ontology Patterns (FOPs) [18]. These DROPs and FOPs can help to design the marketplace domain ontology in a more structured and expanded manner.

In this paper we also restrict the number of providers for a single transaction to one. Some existing marketplaces (e.g. Deliveroo, Uber Eats) have different providers for the same transaction. When ordering a meal via Deliveroo, both the preparation of the meal by the restaurant and the delivery of the mail by a deliverer are linked to a single transaction.

As a marketplace domain ontology can facilitate communication, consensus and alignment in future discussions, marketplace developments and research, we plan to use this ontology as a basis for the development of a conceptual data model for a comprehensive variety of different marketplaces. This conceptual data model can then be compared to software products for marketplace creation (e.g. Sharetribe [23]) and the gaps between them can result in the design a software reference architecture for marketplaces. A marketplace ontology, conceptual data model and software reference architecture can accelerate the development of smaller, more alternative and socially responsible marketplaces and can thus contribute to the creation of a more socially responsible sharing economy.

## References

1. Zervas, G., Proserpio, D., Byers, J.W.: The rise of the sharing economy: estimating the impact of airbnb on the hotel industry. J. Mark. Res., 2731799 (2014)
2. Trabucchi, D., Muzellec, L., Ronteau, S., Trabucchi, D.: Sharing economy: seeing through the fog economy (2019)
3. Hamari, J., Ukkonen, A.: The sharing economy: why people participate in collaborative consumption. J. Assoc. Inf. Sci. Technol. 67 , 2047 -2059 (2016)
4. Frenken, K., Schor, J.: Putting the sharing economy into perspective. Environ. Innov. Soc. Transit. 23 , 3 -10 (2017)
5. Kenney, M., Zysman, J.: The rise of the platform economy. Issues Sci. Technol. 32 , 61 -69 (2016)
6. Bardhi, F., Eckhardt, G.M.: Access-based consumption: the case of car sharing. J. Consum. Res. 39 , 881 -898 (2012)
7. Botsman, R., Rogers, R.: What ' s Mine Is Yours: The Rise of Collaborative Consumption (2010)
8. Codagnone, C., Martens, B.: Scoping the Sharing Economy: Origins, De fi nitions, Impact and Regulatory Issues. Ssrn (2016)
9. T ä uscher, K., Laudien, S.M.: Understanding platform business models: a mixed methods study of marketplaces. Eur. Manag. J. 36 , 319 -329 (2018)
10. Hagiu, A., Wright, J.: Multi-sided platforms. Int. J. Ind. Organ. 43 , 1 -32 (2015)
11. Kestenbaum, R.: What Are Online Marketplaces And What Is Their Future? (2017). https:// www.forbes.com/sites/richardkestenbaum/2017/04/26/what-are-online-marketplaces-andwhat-is-their-future/#7db183243284
12. Choudhury, V., Hartzel, K.S., Konsynski, B.R.: Uses and consequences of electronic markets: an empirical investigation in the aircraft parts industry. MIS Q. 22 , 471 -507 (2019)
13. Dai, Q., Kauffman, R.J.: Business models for internet-based e-procurement systems and B2B electronic markets: an exploratory assessment, vol. 00, pp. 1 -10 (2004)
14. Stockdale, R.: A framework for the selection of electronic marketplaces: a content analysis approach. ECU Publ., 221 -234 (2004)
15. Sutherland, W., Jarrahi, M.H.: The sharing economy and digital platforms: a review and research agenda. Int. J. Inf. Manag. 43 , 328 -341 (2018)

16. Cesar, J., et al.: A commitment-based reference ontology for services. Inf. Syst. 54 , 263 -288 (2015)
17. Kenney, M., Zysman, J.: Choosing a future in platform economy: the implications and consequences of digital platforms. J. Chem. Inf. Model. 53 , 1689 -1699 (2013)
18. Ruy, F.B., Guizzardi, G., Falbo, R.A., Reginato, C.C., Santos, V.A.: From reference ontologies to ontology patterns and back. Data Knowl. Eng. 109 , 41 -69 (2017)
19. Guizzardi, G.: Foundations for Structural Conceptual (2005)
20. Falbo, R.A., Guizzardi, G., Gangemi, A., Presutti, V.: Ontology patterns: clarifying concepts and terminology. In: CEUR Workshop Proceedings, vol. 1188 (2013)
21. T ä uscher, K., Berkeley, U.C.: Supporting business model decisions: a scenario-based simulation approach. Int. J. Mark. Bus. Syst. 2 , 45 -67 (2016)
22. Bakos, Y.: The Emerging role of electronic marketplaces on the Internet. Commun. ACM 41 , 35 -42 (1998)
23. [Sharetribe. https://www.sharetribe.com/](https://www.sharetribe.com/)
