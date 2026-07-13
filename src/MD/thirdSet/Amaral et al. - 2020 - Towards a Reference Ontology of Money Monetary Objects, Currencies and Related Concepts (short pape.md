## Towards a Reference Ontology of Money: Monetary Objects, Currencies and Related Concepts

Glenda Amaral 1 , Tiago Prince Sales 1 , Giancarlo Guizzardi 1 , Daniele Porello 2 , and Nicola Guarino 2

1 Conceptual and Cognitive Modelling Research Group (CORE), Free University of Bozen-Bolzano, Bolzano BZ 39100, Italy

{ gmouraamaral,tiago.princesales,giancarlo.guizzardi } @unibz.it

- 2 ISTC-CNR Laboratory for Applied Ontology, Trento, Italy { daniele.porello,nicola.guarino } @cnr.it

Abstract. Money is so ever-present in modern life that we usually take its existence for granted. Financial crisis like the recent one in 2008 are significant alerts about the importance of money and finance. Having a clear understanding of the concepts on the finance domain is fundamental to figure out the evolution of the economy before innovations in the Finance Industry. This research aims at addressing these issues by investigating the conceptual foundations of money, grounded in the Unified Foundational Ontology and based on the literature review of the most relevant economic theories.

Keywords:

Money · Currency · Unified Foundational Ontology.

## 1 Introduction

Money permeates most aspects of life in modern societies. 'Despite its immense contribution for economic performance, we tend to be oblivious towards the infrastructures that support the operation of the monetary system. As it is often the case with infrastructures, whether social or technological, they remain invisible as long as they operate and fulfill their functions. In case of accident, disruption or crisis, their breakdown makes them visible and raises concerns and questions about their operation' [21].

Having an integrated view that shares a common conceptualization of the finance domain is paramount in a number of activities required to ensure the proper functioning of the financial system [2, 22], such as the formulation of monetary policy, the safe-guarding of financial stability, and the maintenance of trust in the monetary system. The lack of conceptual clarity hinders the analysis of business data, the communication among various economic and financial actors, the enactment of laws and regulations, the mitigation of risks, and the achievement of an appropriate common governance model.

In the last years, there has been a growing interest, within the financial sector, in the adoption of ontology-based conceptual models to make the nature

## G. Amaral et al.

of the conceptualizations explicit [8, 22], as well as to safely establish the correct relations between them. An example is the Financial Industry Business Ontology (FIBO), 'an industry standard resource for the definition of business concepts in the financial services industry' [8]. Although FIBO includes a Currency Amount Ontology, it is not comprehensive and only marginally touches the notions of money and currency. For example, concepts related to money functions, types of money, legal aspects and trust are not explored in this ontology.

Despite the wide number of efforts to create a unified view of the reality related to economic and finance domains [3, 8, 9], no formal model, significant enough, has been developed to accurately describe the semantics regarding the world of money and currencies. This research aims at tackling these issues by investigating the ontological nature of money and of its underlying concepts, grounded in the Unified Foundational Ontology (UFO) [11], based on the literature review of the most relevant economic theories and considering the innovations in the Finance Industry. In this paper we present and describe the ongoing work towards a Reference Ontology of Money, with an initial focus on money objects, currencies and related concepts.

The remainder of this paper is organized as follows. First, in Section 2, we discuss the ontological nature of money and currencies as described in the literature. In Section 3 we present our proposal, an initial version of the Reference Ontology of Money. We conclude in Section 4 with some final considerations.

## 2 On Money

## 2.1 The Origins of Money

Two leading schools of thought present fundamentally different arguments regarding the origins of money. A classic theory, known as the commodity theory of money was defended by many classical economists like Carl Menger [20], Georg Simmel [25] and Ludwig von Mises [28]. They claim that 'when the conditions for exchange outside the family arose, with an increased division of labor, a medium of exchange was introduced in order to facilitate the exchanges through indirect exchange. With time and the sophistication of society, these initial forms of media of exchange evolved from some merchandise, such as cattle or salt, to metals, and later coined metals until human societies reached the stage of fiat money that we have today' [29]. The commodity theory has also been referred to as the catallactic theory , an expression derived from the Greek for 'to exchange' [28], and as the metallist theory [26], as precious metals were supposed to have been historically used as exchange media.

Alternatively, there are those who argue that money is a social construction in lieu of a physical commodity [6, 16-19]. This view is known as the credit theory of money . According to this theory, money is merely a token of a 'credit relationship, a promise from someone to grant (or repay) a favor (e.g. a product, a service) to the holder of the token' [6]. In order to function as money, the promise must be sufficiently credible, that is, the issuer must be creditworthy and the credit needs to be transferable. 'It is commonly thought that the most creditworthy issuer of money is the state' [6], and the view that only the state can issue money is known as chartalism , or the state theory of money [18].

## 2.2 Forms of Money

Historically, money has taken on scores of forms, from tobacco, salt and shells to large circular stone discs. Early money was usually a commodity money , that is, an object considered valuable itself. 'The commodity can be gold, silver, squirrel pelts, seashells, or whatever a community decided. In its simplest form, commodity money is like barter. People trade one type of object for goods and services' [23]. 'Around the eighteenth century, commodity-backed money started to be used, which consisted of items representing the underlying commodity (e.g. gold certificates). These pieces of paper were not valuable themselves, but they could be exchanged for a fixed quantity of the underlying commodity. The main advantages of this system were the portability of the money and that larger amounts of money could be transferred'[5].

'Modern economies are typically based on fi at money , which is similar to commodity-backed money in its appearance, but radically different in concept, as it can no longer be redeemed for a commodity. Fiat money is any legal tender designated and issued by a central authority. It is only really money because some authority says it is money' [23].

## 2.3 Status Function and Trust

'Human beings have a special capacity, which is that they can impose functions on objects and other people where the function is not performed in virtue of the physical features of the person or object (or at least not the physical features alone), but it is performed in virtue of the fact that a certain status has been assigned to the person or object' [23]. This status, also known as status function, assigns a function that can be performed only in virtue of the collective acceptance or recognition of that status in the community in question. Status functions are all created by a certain type of speech act that Searle [23, 24] named declaration , where you make something the case by declaring it to be the case. According to Searle [23] 'money always requires a declaration whereby some representation makes it the case that it is money. It is this status that makes money valuable and guarantees its acceptability'. For example, a twenty-euros banknote fits this definition because it does have a definite status of being a twenty-euros banknote in Europe. People are willing to accept it in exchange for goods and services because they trust the monetary system that support this status function. In [4], Castelfranchi and Falcone state that 'trust is the presupposition of money': originally money relies on the trust of the individuals accepting a monetary item as an instrument to indirectly acquire a certain amount of desirable goods [29]. Trust is therefore a crucial element of every monetary system.

G. Amaral et al.

## 2.4 Functions of Money

Although the format of money has changed considerably over time, the functions of money remain unchanged. 'Behind the diverse forms of money there is a common intension, an unchanging core of meaning' [21] that defines what money is. From the wide number of definitions proposed in the literature, it is possible to deduce a consensus in economics that this core set of identity-constituting properties is related to the three different functions of money, namely:

- medium of exchange : a means of payment with a value that everyone trusts; 'money is used as an intermediary in trade to avoid the inconveniences of a barter system, i.e. the need for a coincidence of wants between the two parties involved in the transaction'[5]. Borrowing an example from [23], the statement 'I bought this shirt for 20 euros' reports the use of money as a medium of exchange.
- a unit of account : 'money acts as a standard numerical unit for the measurement of value and costs of goods, services, assets and liabilities' [5]. An example, mentioned in [23], that reports the use of money as a measure of value is the statement 'My car is worth 10,000 euros'.
- a store of value : 'money can be saved and retrieved in the future' [5]. The statement 'I have 1,000 euros in my bank account' [23] reports the use of money as a store of value.

## 2.5 Currency and Legal Aspects

The Oxford Dictionary [7] defines currency as 'the system of money that a country uses'. The word currency 'derives from Latin terms for running and owing, and is since the seventeenth century used for the circulation of money, divided into specific monetary systems that are linked to nation states' [10]. According to Papadopoulos [21], 'currency represents and communicates the idea of money in our day-to-day transactions, attaching a set of visual representations to the identity of economic value'.

A legal tender is anything recognized by law that can be used to pay contractual debts. Countries specify which objects are considered legal tender for debts that are subject to its contract law. In most of them, the national government is the only party authorized to produce and distribute physical currency in its geographical area of control. The government also regulates the production of non-physical currency by banks through its monetary policy, usually implemented via the central bank. In some countries, alternate currencies are permissible, but only the nationally sponsored currency has the status of legal tender. And in still other countries a foreign produced currency is both acceptable currency and legal tender. For example, in the countries of the euro area, only euro banknotes and coins are legal tender and therefore, by law, must be accepted as payment for a debt within those countries. According to the Article 128 of the Treaty on the Functioning of the European Union [27]: 'The European Central Bank (ECB) shall have the exclusive right to authorise the issue of banknotes within the Union. The ECB and the national central banks may issue such notes. The banknotes issued by the ECB and the national central banks shall be the only such notes to have the status of legal tender within the Union'.

## 2.6 Money Dynamics and Exchange Value

As previously mentioned, status functions, which can be expressed in terms of laws, specify which objects are considered money. These monetary objects have an associated exchange value, which allows them to be exchanged for something (e.g. goods or services) with the same exchange value. Exchange value can be defined as the ratio in which one commodity exchanges for another. It represents the worth of one good or service expressed in terms of the worth of another. In modern economies, money emerges as a neutral commodity in which all other commodities express their exchange values.

In this context, agents holding the control of monetary objects have the power to carry out economic transactions in the amount corresponding to its exchange value. As the exchange value of goods and services can change, influenced by the economic environment and the dynamic of the system of prices, the purchasing power associated with these economic transactions also changes. It means that the exchange value of the transaction that the agent manages to carry out remains the same (and is equal to the exchange value associated to the monetary object under his control), however, the quantity of goods and services that he manages to get with that value will vary, depending on the exchange value of these commodities.

## 3 The Reference Ontology of Money

In this section we use the aforementioned theories to present a preliminary model of the Reference Ontology of Money, which was designed taking as basis the Unified Foundational Ontology (UFO). UFO is a foundational ontology developed with an interdisciplinary approach, inspired by Formal Ontology, Philosophical Logic, Linguistics, and Cognitive Psychology. It consists of three main parts: UFO-A [11], an ontology of endurants (objects) UFO-B [15], an ontology of events (perdurants), and UFO-C [12], an ontology of social entities built on the top of UFO-A and UFO-B. For an in-depth discussion and formalization, one should refer to [11, 15]. The Reference Ontology of Money is based upon the usage of the OntoUML language [14], an ontological extension of UML that incorporates the foundational directions in UFO. We formalize the concept of money in the OntoUML model depicted in Fig. 1. In this diagram, we represent types of substantials in pink, relations in green and modes in blue. We also use the OntoUML semantics of sortals and non-sortals proposed in [13].

In our analysis, we rely mainly on some concepts defined in UFO-C. A basic distinction in UFO-C is related to agents and (non-agentive) objects . An agent is a specialization of a substantial individual (existentially independent objects)

## G. Amaral et al.

that can be classified as physical (e.g., a person) or social (e.g., an organization, a society). Objects are non-agentive substantial individuals that can also be categorized in physical (e.g., a book) and social objects (e.g., language).

We model the Status Function Description that defines certain types of objects as money and guarantees their acceptability as a type of Normative Description . UFO-C defines Normative Description as a type of Social Object that defines one or more rules/norms recognized by at least one social Agent and that can define nominal universals such as social moment universals (e.g., social commitment types), social objects (e.g., the crown of the King of Spain) and social roles (e.g., president, or pedestrian). Examples of normative descriptions include the Italian Constitution, the University of Bolzano PhD program regulations, and also a set of directives on how to perform some actions within an organization. In the finance domain, the Treaty on the Functioning of the European Union [27] is an example of Status Function Description , which defines euro banknotes and coins as legal tender money in the countries of the euro area.

The entity Monetary Object Type represents the types of objects that are considered money according to a Status Function Description . Historically, different types of objects have been used as money in all its manifestations, such as (i) tobacco, salt, among others, used as commodity money (money in the form of objects considered valuable), (ii) banknotes and paper certificates, used as commodity-backed money (money backed by an underlying commodity such as gold), and (iii) banknotes, coins and bank deposits in electronic format, used as fi at money (money which is not backed by anything).

In the ontology, Monetary Object represents instances of Monetary Object Types and stands for the objects that are considered money according to a certain Status Function Description . The Monetary Object Nominal Value corresponds to the nominal value (also known as face value) stamped on the Monetary Object by the issuing authority.

Valid Monetary Object and Not Valid Monetary Object represent two different phases of the Monetary Object 's life cycle. For example, new banknotes are not considered valid until they are released and put into public circulation. Likewise, damaged banknotes are not considered valid and must be destroyed.

We represent the quantitative perspective of money by means of the Monetary Object Exchange Value . This property is specific to valid monetary objects as only they can be exchanged for goods and services in the economy. The exchange value of a Valid Monetary Object is equal to its nominal value. In the ontology, both the Monetary Object Nominal Value and the Monetary Object Exchange Value are represented as qualities inhering in the Monetary Object and in the Valid Monetary Object , respectively. In UFO, a quality is an objectification of a property that can be directly evaluated (projected) into certain value spaces [11]. It is possible to compare qualities, as well as to establish equivalence relations and mappings of values among different value spaces. Both the exchange value and the nominal value of a Monetary Object are modeled as qualities that have a value in a Currency conceptual space. Euro and US Dollar are examples of Currencies . Currency conversions using exchange rates are examples of mappings of values among different value spaces.

As argued in the previous section, when an agent holds the control of a valid monetary object she is endowed with the power to make economic transactions in the amount corresponding to its exchange value. We capture it by means of the objectified relationship labeled Control , between Valid Monetary Object and Agent . The Exchange Power to carry out economic transactions inheres in the Agent and is grounded on the Control relationship. It assumes a value in a Currency conceptual space, which is equal to the exchange value of the Valid Monetary Object . Finally, the Exchange Power has an underlying Purchase Power that corresponds to the quantity of goods and services that the Agent manages to get with that Exchange Power . As previously discussed, the Purchase Power depends on the Exchange Value of goods and services.

In the ontology, objects considered valuable, such as goods and services, are modeled as Value Bearers . We model the Exchange Value of these commodities as a quality value that is 'attached' to a Value Bearer , as a result of an assessment made by an Agent . The relationship Exchange Value Ascription represents this assessment. We are aware that the current ontology does not provide a deep analysis of the concept of exchange value. This analysis fall outside the scope of this paper, as our focus is the modeling of the relationship between money and exchange value. We plan to address this issue by future research.

It is woth mentioning that Monetary Object s are also considered Value Bearer s as they can be traded in the economy as regular commodities, like collectible items. For example, some rare banknotes are traded by banknote collectors at far more than their nominal (or face) value. Even valid banknotes in circulation can be traded as collectible items at a value above their face value. However, for the acquisition of goods and services in the economy, a banknote functions as a means of exchange and will always be worth its face value.

It is clearly recognized in the literature that trust is a crucial element for the well functioning of any monetary system [4, 21, 23, 29]. We make use of the concepts and relations defined in the Reference Ontology of Trust (ROT) [1] to model the relation between money and trust. ROT formalizes the general concept of trust and distinguishes between two types of trust, namely, social trust and institution-based trust. The latter builds upon the existence of shared rules, regularities, conventional practices, etc. and is related to social systems [1], like the Monetary System . According to ROT, Institution-based Trust is a specialization of Trust in which the Trustee is a social system. In our ontology the entity Institution-Based Trust represents the Trust of the society (a social Agent ) in the Monetary System .

## G. Amaral et al.

Fig. 1: The Reference Ontology of Money

[FIGURE]

## 4 Conclusions

In this paper, we presented an initial proposal for a Reference Ontology of Money. We investigated the ontological nature of money and currencies and formalized these concepts in an OntoUML model. We believe this work clarifies the notion of money, which can serve as a basis for future business ontologies. As a next direction, we plan to further validate our ontology and expand our analysis to account for additional technological innovations in the Finance Industry, like the advent of cryptocurrencies [5]. We also plan to integrate it to well-known ontologies in the finance domain (e.g. FIBO).

## References

1. Amaral, G., Sales, T.P., Guizzardi, G., Porello, D.: Towards a reference ontology of trust. In: OTM Confederated International Conferences. pp. 3-21. Springer (2019)
2. Basel Committee: Principles for effective risk data aggregation and risk reporting (2013), https://www.bis.org/publ/bcbs239.htm
3. Blums, I., Weigand, H.: Financial reporting by a shared ledger. In: JOWO (2017)
4. Castelfranchi, C., Falcone, R.: Trust theory: A socio-cognitive and computational model, vol. 18. John Wiley &amp; Sons (2010)
5. Centralny, E.B.: Virtual currency schemes. ECB, Frankfurt am Main (2012)
6. De Bruin, B., Herzog, L., O'Neill, M., Sandberg, J.: Philosophy of money and finance. Stanford Encyclopedia of Philosophy (2018)
7. Dictionary, O.E.: Oxford english dictionary. Simpson, JA &amp; Weiner, ESC (1989)
8. Enterprise Data Management Council: Financial Industry Business Ontology (2015), https://spec.edmcouncil.org/fibo/, accessed: 2010-09-30
9. Fischer-Pauzenberger, C., Schwaiger, W.S.: The OntoREA c © accounting and finance model: ontological conceptualization of the accounting and finance domain. In: International Conference on Conceptual Modeling. pp. 506-519. Springer (2017)
10. Forn¨ as, J.: Signifying Europe. Intellect Bristol (2012)

- ica Instituut / CTIT (2005) Guizzardi, G.: Ontological foundations for structural conceptual models. Telemat11.
- Conference on Software Engineering (CIbSE). pp. 127-140 (2008) tologies in the Unified Foundational Ontology (UFO). In: 11th Ibero-American Guizzardi, G., Falbo, R.A., Guizzardi, R.S.S.: Grounding software domain on12.
- 2.0. In: Int. Conference on Conceptual Modeling. pp. 136-150. Springer (2018) T.P.: Endurant types in ontology-driven conceptual modeling: Towards ontouml Guizzardi, G., Fonseca, C.M., Benevides, A.B., Almeida, J.P.A., Porello, D., Sales, 13.
- story. Applied ontology 10 (3-4), 259-271 (2015) foundations for conceptual modeling: the Unified Foundational Ontology (UFO) Guizzardi, G., Wagner, G., Almeida, J.P.A., Guizzardi, R.S.S.: Towards ontological 14.
- national Conference on Conceptual Modeling (ER). pp. 327-341. Springer (2013) wards ontological foundations for the conceptual modeling of events. In: 32nd InterGuizzardi, G., Wagner, G., Falbo, R.A., Guizzardi, R.S.S., Almeida, J.P.A.: To15.
- Innes, A.M.: What is money? The Banking Law Journal. maio (1913) 16.
- St. Martin's for the Royal Economic Society (1971) Keynes, J.M.: A Treatise on Money: V. 1: The Pure Theory of Money. Macmillan, 17.
- for the History of Economic Thought (1924) Knapp, G.F.: The state theory of money. Tech. rep., McMaster University Archive 18.
- Mann, F.A.: The Legal Aspect of Money. Milford (1938) 19.
- Mises Institute (2009) Menger, C.: On the origins of money, trans. CA Foley, Auburn, AL: Ludwig von 20.
- tentionality. Erasmus University Rotterdam (2015) Papadopoulos, G.: The ontology of money: institutions, power and collective in21.
- architecture of global finance, vol. 608. John Wiley &amp; Sons (2010) Scholes, M., et al.: Regulating Wall Street: The Dodd-Frank Act and the new 22.
- 41 (5), 1453-1470 (2017) Searle, J.R.: Money: ontology and deception. Cambridge Journal of Economics 23.
- (1995) Searle, J.R., Willis, S., et al.: The construction of social reality. Simon and Schuster 24.
- Kaethe Mengelberg, 2d ed.1907 p. 475 (1990) Simmel, G.: The philosophy of money, trans. Tom Bottomore, David Frisby, and 25.
- Statement for the Twenty-first Century. Rowman &amp; Littlefield (2018) Smithin, J.: Rethinking the Theory of Money, Credit, and Macroeconomics: A New 26.
- Union C326 , 47-390 (2012) Treaty on the Functioning of the European Union. Official Journal of the European 27.
- Von Mises, L.: The theory of money and credit. Skyhorse Publishing, Inc. (2013) 28.
- tals of monetary institutions. Lexington Books (2015) Zelmanovitz, L.: The ontology and function of money: the philosophical fundamen29.
