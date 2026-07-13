## Towards Ontological Foundations for Central Bank Digital Currencies

Glenda Amaral 1 , Tiago Prince Sales 1 , and Giancarlo Guizzardi 1 , 2

- 1 CORE/KRDB, Free University of Bozen-Bolzano, Bolzano, Italy { gmouraamaral,tiago.princesales,giancarlo.guizzardi } @unibz.it

2 Services &amp; Cybersecurity, University of Twente, The Netherlands

Abstract. The digitalization of the economy and technological innovations are pushing central banks to investigate new forms of digital money. The concept and design of digital currencies have been investigated by central banks for some time. Although much progress has been made towards a convergence on definitions, the term Central Bank Digital Currency (CBDC) is still used to refer to a number of concepts. In this paper we address this issue by extending and refining our previous work, the Reference Ontology of Money and Virtual Currencies, to provide a semantic foundation for the concept of CBDC.

Keywords:

CBDC · Central Bank · Money · Currency · Ontology · UFO.

## 1 Introduction

Digitalization is reshaping the economy and changing the way people pay. Even before COVID-19, which caused a shift in payment habits towards contactless payments and e-commerce, cash payments have been declining in some advanced economies, leading central banks around the world to investigate new forms of digital money.

The idea of a Central Bank Digital Currency (CBDC) is not new [28, p. 12]. The concept and design of digital currencies have been investigated by Central Banks for some years now [4]. A recent survey [6] shows that around 80% of central banks are engaged in some work on CBDCs. Although much progress has been made towards a gradual convergence on definitions, the term CBDC is still used to refer to a number of concepts. Another important aspect concerns interoperability (the semantic level included) among CBDCs, which plays a key role in improving cross-border and crosscurrency payments [5].

In the light of the above, we advocate for the need of a reference conceptual model that provides an ontological account to the concept of CBDC, to serve as a basis for communication, consensus and alignment among different approaches and perspectives, as well as to foster interoperability across different applications in the financial industry.

In a previous effort we proposed the Reference Ontology of Money and Virtual Currencies, an ontologically well-grounded reference model that formally characterizes the concepts of money, currencies and virtual currencies [3]. In this paper we extend our previous work to provide an ontological account of Central Bank Digital Currencies and represent its embedded concepts and relations.

## G. Amaral et al.

The remainder of this paper is organized as follows. First, in Section 2, we discuss the ontological nature of CBDC as described in the literature. In Section 3, we introduce the reader to the Reference Ontology of Money and Virtual Currencies. Then, in Section 4, we present our proposal for extending this ontology to represent the concept of CBDC. We conclude the paper in Section 5 with some final considerations.

## 2 On the notion of Central Bank Digital Currency

Central banks issue money as physical cash and electronic central bank deposits (aka reserves or settlement balances) and provide infrastructure to support a third type, namely commercial bank deposits [5]. While cash and reserves are a liability of the central bank (in the sense that they represent a claim on the central bank), commercial bank deposits are a liability of the bank that issues them. Central Bank Digital Currency stands for a new type of money issued by central banks, which is different from cash and reserves or settlement balances.

Central banks have been actively researching the pros and cons of offering a digital currency to the public [5] and a number of definitions for this term have been proposed in the literature. Kochergina and Yangirovab [19] define CBDC as 'an electronic obligation of the central bank expressed in a national monetary unit and acting as a means of exchange and store of value'. In [7] CBDC is defined as 'a central bank liability, denominated in an existing unit of account, which serves both as a medium of exchange and a store of value'. According to Mancini-Griffoli et al. [21] 'CBDC is a new form of money, issued digitally by the central bank and intended to serve as legal tender'. In the context of the European Union, CBDC is referred in the European Central Bank (ECB) publications by the term digital euro . According to the ECB [11] 'the term digital euro denotes a liability of the Eurosystem recorded in digital form as a complement to cash and central bank deposits'. They also state that 'a digital euro would be just another way to supply euro, not a parallel currency' and 'it should be convertible at par with other forms of the euro, such as banknotes, central bank reserves and commercial bank deposits'.

Recently, aiming at coordinating and consolidating the investigation on CBDCs, the central banks of Canada, Japan, Sweden, Switzerland, the United Kingdom and the United States have come together, along with the European Central Bank and the Bank for International Settlements to produce a report [5] that summarises where they collectively stand. In this work, CBDC is defined as 'a digital form of central bank money that is different from balances in traditional reserve or settlement accounts. A CBDC is a digital payment instrument, denominated in the national unit of account, that is a direct liability of the central bank' [5].

In general, in the literature, the concept of CBDC has been characterized based on several properties and design choices, explained as follows.

Liability. Currently money can represent a liability of the central bank (cash, reserves and settlement balances) or a liability of the bank that has emitted it (commercial bank deposits). While in the former the end user holds a claim on the central bank, in the latter she holds a claim on the issuing entity. CBDC is a liability of the central bank [5].

Form. While cash (such as coins and banknotes) is physical, central bank deposits, commercial bank deposits and CBDCs are digital.

Denomination in official currency. CBDCisanother way to supply official money. It is denominated in the official currency and must be convertible at par to official currency, in the same way as cash, central bank deposits and commercial bank deposits [11].

Functions of Money. CBDC is just a different manifestation of the same unit of account, store of value and medium of exchange already offered by central banks [5].

Scope. Payments are generally distinguished into retail and wholesale. While the former refers to relatively low-value transactions (in the form of, for example, credit transfers and direct debits), the latter corresponds to large-value and high-priority transactions, such as interbank transfers [7]. Wholesale CBDCs limit access to a predefined group of users (such as financial institutions), while the general purpose ones (aka retail CBDCs) are widely accessible to the general public.

Technology. CBDCs can be issued either in the form digital tokens or in the form of electronic accounts. A key distinction between them is the form of verification needed when it is exchanged. Token-based CBDC relies on the ability of the payee to verify the validity of the payment object. While with physical money (cash) there is a concern about counterfeiting, with digital money the worry is both whether the token is genuine and whether it has already been spent [7]. Conversely, account-based CBDCs depend on the ability to verify the account holder's identity. A key concern here is identity theft, which allows transfers or withdraws from accounts without permission. [7]. CBDC can be designed either as token-based or as account-based.

Transfer mechanism. The transfer of cash is conducted on a peer-to-peer basis (decentralized), while deposits are transferred through an intermediary (centralized) [7]. CBDC may be transferred either on a peer-to-peer basis or through an intermediary, which could be the central bank, a commercial bank or a third-party agent [7].

Anonymity Users' privacy can be protected to various degrees, depending on the preferred balance between individual rights and public interest. Although cash transactions are anonymous, regulations (mainly related to money laundering and terrorist financing) do not allow anonymity in electronic transactions and thus CBDCs must in principle comply with such regulations [11].

Availability. Currently, access to reserves and settlement balances is limited to central bank operating hours. CBDCs could be available 24/7 or only during certain specified times. So far there is considerable agreement amongst the central banks in the sense that CBDCs should be available available 24/7 [11].

The prevalence of one or other property or design choice to characterize the concept of CBDC is driven by the particularities and circumstances of each country or area. Although so far there is no 'one size fits all' conceptualization of CBDC, we argue that it is possible to deduce a consensus in the literature on a core set of essential properties that define what a CBDC is. In summary, what can be extracted from these different definitions is that a CBDC necessarily: (i) is a digital form of money; (ii) is a liability of the central bank; (iii) is denominated in the official currency; (iv) is convertible at par with other forms of official money, such as banknotes, central bank reserves and commercial bank deposits; (v) serves as a medium of exchange, an unit of account and a store of value; and (iv) is subjected to legal and regulatory frameworks that specify and regulate it.

An important aspect is that the different types of official money (cash, central bank deposits and commercial bank deposits) also have the same above-mentioned essential properties, except for cash w.r.t. form (as it is physical) and commercial bank deposits w.r.t. liability (as they are a liability of the issuing bank). CBDCs can be further distinguished into different subcategories (such as retail token-based, retail accountbased, wholesale token-based and wholesale account-based) according to different design choices. Table 1 provides a comparison of some design choices across existing (cash, central bank deposits and commercial bank deposits) [15] and potential (CBDC) [5] types of money.

Table 1. Design choices by money type

|                              | Scope           | Technology    | Transfer Mechanism   | Anonymity   | Availability    |
|------------------------------|-----------------|---------------|----------------------|-------------|-----------------|
| Cash                         | General purpose | Token-based   | Decentralized        | Yes         | 24/7            |
| Central bank deposit         | Restricted      | Account-based | Centralized          | No          | Restricted      |
| Commercial bank deposit      | General purpose | Account-based | Centralized          | No          | Restricted      |
| CBDC Retail Token-based      | General purpose | Token-based   | Decentralized        | Possible 1  | 24/7 (possible) |
| CBDC Retail Account-based    | General purpose | Account-based | Centralized          | No          | 24/7 (possible) |
| CBDC Wholesale Token-based   | Restricted      | Token-based   | Decentralized        | Possible 1  | 24/7 (possible) |
| CBDC Wholesale Account-based | Restricted      | Account-based | Centralized          | No          | 24/7 (possible) |

## 3 ROME: Reference Ontology of Money and Virtual CurrEncies

The Reference Ontology of Money and Virtual CurrEncies 2 (ROME) [2] is a reference model, grounded on the Unified Foundational Ontology (UFO) [12, 13], that formalizes the characterization of money, currency and virtual currencies, as well as its embedded concepts and relations. Some of ROME main ontological commitments on the nature of money are listed below:

- -Money depends on the collective acceptance or recognition of its status as money [25, 24, 8, 14, 17, 18, 22]. In contemporary society the status function of money is supported by law, which specifies both the currency and the objects that

1 Although token-based CBDC supports anonymity, it must take into consideration anti-money laundering and counter terrorist financing regulations, as well as security policies.

2 The complete version of ROME in OntoUML and its implementation in OWL are available at http://purl.org/krdb-core/money-ontology.

are considered money in a particular country or region. It also defines a structure for the currency value domain. Examples of structures are: one-dimensional structure of numbers with two decimal places defined for euros, and one-dimensional structure of integers defined for Paraguay's Guarani [16].

- -Monetary objects have a nominal value. This value is denominated in the currency defined in the law that describes its status function.
- -Physical monetary objects can be considered either valid or not valid. For example damaged banknotes fulfilling certain criteria defined in law are not considered valid (e.g. an euro banknote is not considered valid if 50% or less of the banknote is presented and there are no proofs that the missing parts have been destroyed [9]). Obviously, only valid monetary objects can be exchanged for goods and services in the economy.
- -Money presupposes the existence of a credit/debt relation [14, 20]. Monetary objects establish this relation between the agent holding control of them and the central bank. As for central bank deposits and commercial bank deposits, they correspond to an electronic monetary credit denominated in a certain currency and represent a claim on the central bank or the issuing bank, respectively.
- -Monetary objects and electronic monetary credits have an associated exchange value. Agents holding control of monetary objects or owing electronic monetary credits are endowed with the capacity of making economic transactions in the amount corresponding to their exchange value. The exchange power resulting from the total of electronic monetary credits and monetary objects controlled by an agent stands for an aggregated exchange power that corresponds to the total value in economic transactions the agent is capable to carry out.
- -The aggregated exchange power of an agent has a correspondent purchasing power. Simply put, the purchasing power describes the quantity of goods an amount of money can buy. As the price of goods and services can change, the purchasing power of an agent can vary, but its aggregated exchange power remains the same.
- -Money depends on trust. A precondition for the functioning of any monetary system is trust that the monetary objects and credits will be generally accepted, as well as that both price and financial stability will be maintained.

Regarding virtual currencies, ROME assumes the following main ontological commitments:

- -Virtual currencies are neither money nor official currencies. They are digital or physical representations of value, not issued by a central bank, credit institution or e-money institution, which in some circumstances can be used as an alternative to money [10]. From the point of view of central banks and regulatory authorities, as well as from a legal perspective, virtual currencies cannot be regarded as full forms of money at the moment.
- -Virtual currencies are similar to money within their user community. Virtual currencies depend on a collective recognition of a certain status that makes them valuable. They necessarily have their own rules and processes enabling the transfer of value, as well as their payment systems.

## G. Amaral et al.

- -Virtual Currencies depend on trust that they will be accepted. However, the absence of a specific institution protecting their value (such as a central bank or monetary authority) hinders their use as official money, since their volatility prevents their use as a store of value and unit of account and discourages their use as a medium of exchange.
- -Virtual currencies can be categorized into: (i) closed virtual currencies , which can only be exchanged by virtual goods and services offered within the virtual community; (ii) virtual currencies with unidirectional flows , in which 'units can be purchased using real money at a specific exchange rate but cannot be exchanged back to the original currency' [10, p. 6]. Examples are loyalty programmes like airlines' points programmes and the Pokemon Go's PokeCoins [26]; and (iii) virtual currencies with bi-directional flows , in which units can be exchanged to official currencies, according to (floating) exchange rates. Examples include private cryptocurrencies [23], such as Bitcoin and Ethereum.

In the next section we present the diagrams that capture the aforementioned ontological commitments on the nature of money and revisit them to represent the concept of CBDC and its relations. The diagrams on virtual currencies are not presented here as they fall outside the scope of this paper. The reader interested in an in-depth description of the complete version of ROME is referred to [2].

## 4 Extending ROME to represent CBDC

In this section we provide an ontological account of CBDC by building upon ROME [2], refining and extending it when necessary.

Figure 1 3 depicts the concept of Money Status Function Description as a type of Normative Description 4 (concept from UFO-C). The Money Status Function Description defines a Currency and the Monetary Object Types that have the status of money. For example, the 'Treaty on the Functioning of the European Union' [27] is an example of Money Status Function Description , which gives to euro banknotes and coins the status of money in the countries of the euro area. In this case, 'euro' is the Currency , while 'euro banknote' and 'euro coin' are Monetary Object Types . The Money Status Function Description also defines a Currency Quality Space Structure for the Currency Quality Space . The former corresponds to a Social Object that prescribes a structure for the domain of values (e.g. number with two decimal places), while the latter corresponds to the value domain itself (see [12] for quality spaces ).

In ROME, Monetary Objects represent instances of Monetary Object Types . For example, a 'twenty-euros banknote' is a Monetary Object and corresponds to an instance of the 'euro banknote' Monetary Object Type , defined in the 'Treaty on the

3 We adopt the following color coding in the OntoUML diagrams: types are represented in purple, objects in pink, qualities and modes in blue, relators in green, and datatypes in white.

4 UFO-C defines a normative description as a type of social object that may define rules/norms recognized by at least one social agent as well as social intrinsic and relational properties (e.g., social commitment types), social objects (e.g., the crown of the King of Spain) and social roles (e.g., president, or pedestrian). Examples of normative descriptions include the Italian Constitution and the Treaty on the Functioning of the European Union [12].

## Towards Ontological Foundations for CBDC

Fig. 1. Money and Status Function

[FIGURE]

Functioning of the European Union' [27]. The original version of ROME does not provide conceptual primitives to distinguish between physical and digital monetary objects (which is the case of token-based CBDCs). To address this, we classify Monetary Objects in Physical Monetary Objects (e.g. banknotes and coins) and Digital Monetary Objects (e.g. token-based CBDC). As in the original version, Physical Monetary Objects are distinguished into Valid Monetary Object and Not Valid Monetary Object , which represent two different phases of the Physical Monetary Object 's life cycle.

The nominal value property corresponds to the Monetary Object 's nominal value, defined by the issuing authority. The property exchange value is specific to Valid Monetary Objects and Digital Monetary Objects as only they can be exchanged for goods and services in the economy. Their exchange value is equal to their nominal value. In UFO, properties can be directly evaluated (projected) into certain value spaces [12]. Both the exchange value and the nominal value of a Monetary Object are modeled as properties that have a value in a Currency Quality Space , which is structured according to a particular Currency Quality Space Structure . For example, euro has a measurable value in one-dimensional structure of numbers with two decimal places [16].

Another clarification we need to make regards monetary credit/debt relations (Figure 2). Money represents a credit/debt relation between an Agent that holds control of a monetary object (cash or token-based CBDC) or has credit in an account (commercial bank deposit, central bank deposit or account-based CBDC), and either a Monetary Authority such as a central bank (in the case of cash, central bank deposits and CBDC) or a Financial Institution (in the case of commercial bank deposits). In other words, money represents a liability of either a Monetary Authority (for cash, central bank deposits and CBDC) or a Financial institution (for commercial bank deposits). We have extended ROME to distinguish between Financial Institution Credit/Debt Relation and Monetary Authority Credit/Debt Relation . The former refers to commercial bank deposits and represents a liability of a financial institution. It is composed of a monetary credit ( FI Monetary Credit ) and a monetary debt ( FI Monetary Debt ), which have their values projected in a particular Currency Quality Space , and inhere in the Agent (creditor) and in the Financial Institution (debtor), respectively. The latter refers to cash, central bank deposits and CBDC, and represents a liability of a monetary authority such as a central bank. Similarly, it is composed of a Monetary Credit and a Monetary Debt , which have their values projected in a particular Currency Quality Space , and inhere in the Agent (creditor) and in the Monetary Authority (debtor), respectively.

Fig. 2. Monetary Objects and Monetary Credit/Debt

[FIGURE]

The Monetary Authority Credit/Debt Relation is further specialized into Tokenbased Credit/Debt and Account-based Credit/Debt . The former represents the credit/ debt relation that a Valid Monetary Object (e.g. banknotes and coins) or a Digital Monetary Object (e.g. token-based CBDC) establishes between the Agent that holds Control of it, and the Monetary Authority . As for the Account-based Credit/Debt relation, it represents central bank deposits and account-based CBDCs.

When an Agent plays the role of creditor in a Monetary Authority Credit/Debt Relation or in a Financial Institution Credit/Debt Relation , she is endowed with the power to make economic transactions in the amount corresponding to this credit (Figure 3). This power is termed here exchange power. The Exchange Power to carry out economic transactions inheres in the Agent and is grounded either on a Monetary Authority Credit/Debt Relation or in a Financial Institution Credit/Debt Relation , in which the Agent is the creditor. The Exchange Power 's property exchange power value assumes a value in a Currency Quality Space , which is equal to the value of the monetary credit. We model the exchange power resulting from the sum of monetary credits by means of the entity Aggregated Exchange Power , which is represented as a kind of capability inhering in the Agent . Finally, as in the original version of ROME, the Aggregated Exchange Power has an underlying Purchasing Power that corresponds to the quantity of goods and services the Agent manages to get with this Aggregated Exchange Power (Figure 3). As previously discussed, the Purchasing Power depends on the Price of goods and services. We model Price as a quality value that is 'attached' to an Object , as a result of an assessment made by an Agent . The relationship Pricing represents this assessment.

As in the original version of ROME, the relation between money and trust is modeled based on the concepts and relations defined in the Reference Ontology of Trust (ROT) [1] (Figure 1). ROT formalizes the general concept of trust and describes the

## Towards Ontological Foundations for CBDC

Fig. 3. Exchange Power and Purchasing Power

[FIGURE]

notion of Institution-based Trust , which builds upon the existence of shared rules, regularities, conventional practices, etc. and is related to social systems [1], like the Monetary System . According to ROT, Institution-based Trust is a specialization of Trust in which the Trustee is a social system. In our ontology the entity Institution-Based Trust represents the Trust of the society (a social Agent ) in the Monetary System .

## 5 Final Remarks

In this paper, we conducted an ontological analysis to investigate the nature of Central Bank Digital Currencies and formalized these concepts by extending our Reference Ontology of Money and Virtual Currencies [2]. We believe this work clarifies the notion of CBDC, which can serve as a basis for future business ontologies, meaning negotiation, the enactment of law and regulation and the definition of proper governance models. As future work, we plan to further validate our ontology and use it to support interoperability between payment systems.

## Acknowledgments

This work is partially supported by CAPES (PhD grant 88881.173022/2018-01) and NeXONproject (UNIBZ). The authors would like to thank Arnaldo Francisco Vitaliano Filho for his valuable comments on the topics of this paper.

## References

1. Amaral, G., Sales, T.P., Guizzardi, G., Porello, D.: Towards a Reference Ontology of Trust. In: OTM Confederated International Conferences. pp. 3-21. Springer (2019)
2. Amaral, G., Sales, T.P., Guizzardi, G., Porello, D.: A Reference Ontology of Money and Virtual Currencies. In: IFIP Working Conf. on The Practice of Enterprise Modeling. Springer (2020)
3. Amaral, G., Sales, T.P., Guizzardi, G., Porello, D., Guarino, N.: Towards a Reference Ontology of Money: Monetary Objects, Currencies and Related Concepts. In: 14th International Workshop on Value Modelling and Business Ontologies (2020)

4. Auer, R., Cornelli, G., Frost, J., et al.: Rise of the central bank digital currencies: drivers, approaches and technologies. Bank for International Settlements (880), 36 (2020)
5. Bank of Canada, European Central Bank, Bank of Japan, Sveriges Riksbank, Swiss National Bank, Bank of England, Board of Governors of the Federal Reserve, Bank for International Settlements: Central Bank Digital Currencies: Foundational Principles and Core Features. Bank for International Settlements (2020), https://www.bis.org/publ/othp33.pdf, Accessed: 2021-01-17
6. Boar, C., Holden, H., Wadsworth, A.: Impending arrival - a sequel to the survey on central bank digital currency. Bank for International Settlements (107) (2020)
7. Committee on Payments and Market Infrastructures: Central bank digital currencies. Bank for International Settlements (2018), https://www.bis.org/cpmi/publ/d174.pdf, Accessed: 2021-01-17
8. De Bruin, B., Herzog, L., O'Neill, M., Sandberg, J.: Philosophy of Money and Finance. Stanford Encyclopedia of Philosophy (2018)
9. Decision of the European Central Bank of 19 April 2013 on the denominations, specifications, reproduction, exchange and withdrawal of euro banknotes (ECB/2013/10). Official Journal of the European Union L118 , 37-42 (2013)
10. European Central Bank: Virtual currency schemes-a further analysis. Tech. rep., European Central Bank, Frankfurt am Main, Germany (2015)
11. European Central Bank: Report on a digital euro. European Central Bank (2020)
12. Guizzardi, G.: Ontological foundations for structural conceptual models. Telematica Instituut Fundamental Research Series, No. 15, ISBN 90-75176-81-3 (2005)
13. Guizzardi, G., Fonseca, C.M., Benevides, A.B., Almeida, J.P.A., Porello, D., Sales, T.P.: Endurant types in ontology-driven conceptual modeling: Towards OntoUML 2.0. In: Int. Conference on Conceptual Modeling. pp. 136-150. Springer (2018)
14. Innes, A.M.: What is Money? The Banking Law Journal (1913)
15. ISO: Financial services - Universal financial industry message scheme - ISO 20022:2013 (2013)
16. ISO: Codes for the representation of currencies - ISO 4217:2015 (2015)
17. Keynes, J.M.: A Treatise on Money: V. 1: The Pure Theory of Money. Macmillan, St. Martin's for the Royal Economic Society (1971)
18. Knapp, G.F.: The state theory of money. Tech. rep., McMaster University Archive for the History of Economic Thought (1924)
19. Kochergina, D., Yangirovab, A.: Central Bank Digital Currencies: Key Characteristics and Directions of Influence on Monetary and Credit and Payment Systems. Finance: Theory and Practice 23 (4), 80-98 (2019)
20. Macleod, H.: The Theory of Credit, vol. 2. Longmans, Green, and Company (1890)
21. Mancini-Griffoli, T., Peria, M.S.M., Agur, I., Ari, A., Kiff, J., Popescu, A., Rochon, C.: Casting light on central bank digital currency. IMF Staff Discussion Notes (18-08) (2018)
22. Mann, F.A.: The Legal Aspect of Money. Milford (1938)
23. Mukhopadhyay, U., Skjellum, A., Hambolu, O., Oakley, J., Yu, L., Brooks, R.: A brief survey of cryptocurrency systems. In: 14th annual conference on privacy, security and trust. pp. 745-752. IEEE (2016)
24. Papadopoulos, G.: The ontology of money: institutions, power and collective intentionality. Erasmus University Rotterdam (2015)
25. Searle, J.: The Construction of Social Reality. Free Press (1995)
26. Stanley-Smith, J., Schwanke, A.: Pokemon GO Could Get Caught in a Tax Bubble. Int'l Tax Rev. 27 , 22 (2016)
27. Treaty on the functioning of the european union. Official Journal of the European Union C326 , 47-390 (2012)
28. Tobin, J.: A Case for Preserving Regulatory Distinctions. Challenge 30 (5), 10-17 (1987)
