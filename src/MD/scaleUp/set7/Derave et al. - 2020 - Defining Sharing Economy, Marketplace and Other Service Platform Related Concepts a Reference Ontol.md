## Defining sharing economy, marketplace and other service platform related concepts: A reference ontology approach

Thomas Derave 1[0000-0003-1547-8333] , Tiago Prince Sales 2[0000-0002-5385-5761] , Frederik Gailly 1[0000-0003-0481-9745] , Geert Poels 1[0000-0001-9247-6150]

1 Department of Business Informatics and Operations Management, Ghent University, Tweekerkenstraat 2, 9000 Ghent, Belgium

2  Faculty of Computer Science, Free University of Bozen-Bolzano thomas.derave@UGent.be, tiago.princesales@unibz.it, {michael.verdock, frederik.gailly, geert.poels}@UGent.be

## 1 Introduction and methodology

The use of sharing economy platforms like Airbnb and Uber is on the rise. The sharing economy has emerged as a viable alternative to fulfilling a variety of consumer needs, ranging from prepared meals to cars to overnight accommodations, that were previously provided by firms. Problematic for academic studies is that concepts including 'sharing economy', 'marketplace', 'on-demand economy' and 'platform' are umbrella concepts or 'buzz words' and there is no consensus on what they comprise [1-5]. To add to this confusion different platforms want to be under the big tent of the 'sharing economy,' because of the positive symbolic value of sharing [6]  This lack of agreement has made it difficult for scholars to determine the impact sharing economy and other related concepts have for the study and practice as well as for society at large. It remains difficult to compare different studies and their results since each of them uses a different conceptualization  [7].  Clearer  definitions  can  improve  communication,  guide  future  research and produce useful contributions and recommendations for marketing and development practitioners who are keen on learning more about how to adapt their business model [7, 8]. There is also lack of research concerning the (socio)technological aspects, the development and the innovations patterns diffusion of marketplaces and sharing economy platforms [9, 10]. Our goal is to lower this conceptual confusion by creating an ontology for service platforms of any kind and use it to compare different concept definitions. To design a service platform reference ontology, we first had to design the minimum requirements of the different platform concepts using three steps:

1. We searched for secondary sources (literature  reviews)  on  sharing  economy  and other platform related concepts and definitions. Eventually, we ended up with 6 papers ([2, 4, 5, 10-12])
2. By snowballing, we searched for the papers and definitions most used to explain these concepts. These definitions where than analyzed and refined.
3. These definitions where compared to each other, and Minimum Platform Requirements (MPRs) for every concept where defined. This way we can differentiate with

clear requirements what the difference is between a sharing economy platform, a P2P economy platform, a marketplace and other service platforms

Second, we add a set of common functionalities included in most service platforms based on the Common Platform Properties (CPPs) of [13]. These CPPs are no necessity for a platform to have but are included in most service platforms and therefore also in our ontology. These CPPs are payments via the platform, customer reviews after transaction and a message system.

In the future, we plan to group and rephrase these MPRs and CPPs to competency questions (CQs), which are needed to create the reference ontology following [14].  We use these CQs to identify fragmented sub-ontology pieces called Domain-Related Ontology  Patterns  (DROPs)  and  Foundational  Ontology  Patterns  (FOPs).  DROPs  and FOPs  are  reusable  fragments  extracted  from  reference  domain/core  ontologies  and foundational ontologies respectively. By means of DROPs and FOPs we can package the knowledge related to the service platform domain [15]. We plan to apply them informally, without explicitly highlighting the DROPs and FOPs,  to design a service platform reference ontology, which we represent using OntoUML [16].

After, we plan to validate the reference ontology by ontology and service platform experts. Validation is performed by having these experts answer the CQ's using only the information they infer from the OntoUML model. If the answers differ from the intended outcome, changes to the model have to be made. We will also use the antipatterns simulation tool of [17] and fit the example of Airbnb to our model as a second validation of the ontology.

## 2 Map platform concepts, define MPRs and CPPs

In this section we compare the platform concepts definitions (gathered following the first 2 steps of our methodology) resulting in a list of MPRs, minimum requirements a platform has to comply to be defined as the specific platform concept. An overview of these concepts as super-and subclasses is given in figure 1.

Service platform : A virtual offering space characterized by near-zero marginal cost of access, reproduction, and distribution [18]. This is an:

- MPR1: IT-based virtual space.
- MPR2: With near-zero marginal cost of access
- MPR3: With near-zero marginal cost of reproduction
- MPR4: With near-zero marginal cost of distribution

Multi-sided platform : all service platforms where multiple parties can offer products and/or services and make transactions [19] (e.g. Xbox, Amazon). A multi-sided platform is a service platform that

- MPR5: allows multiple providers.

Peer-to-Peer (P2P) platform : A platform that intermediates in the interaction between peers as equal participants, also called prosumers alternating in their role as consumer or provider. A peer can also be a business and the value is co-created with the peer provider acting as a micro-entrepreneur [20]. A P2P platform is a multi-sided platform where

- MPR6: The interactions are P2P:
- ─ MPR6a:  The subscription of both customer and provider should have near-zero marginal costs.
- ─ MPR6b: For every interaction a peer can alternate between the role of customer and provider

User-generated content platforms : (e.g. Wikipedia, YouTube). They offer providers a platform to upload content, and as an intermediary the content sharing platform receives money from advertisement or donations after which it can reward popular content providers. The platform offers P2P interactions between users but there is an absence of transaction between the peers with the platform as intermediary so that a pertransaction fee or per-interaction fee or a two-part tariff is not possible [21]. Although it's debated [6], we make a difference between these user-generated content platforms and sharing economy platforms. A user-generated platform is a P2P platform which is not an e-commerce (and thus doesn't offer online transactions between the peers). E-Commerce : All sites and applications offering transactions online [22].

- MPR7: The products and/or services are offered on an IT-based virtual space.
- MPR8: The products and/or services are offered to a targeted customer community
- MPR9: A peer consumer can enter into a transaction in a fully automated way without any manual interference of an employee.
- MPR10: Transactions are treated by the IT-based tool.
- MPR11: The company owning the e-commerce provides an institutional and regulatory frame for transaction.

Digital marketplace : Digital platform, allowing peers from both supply and demand sides to enter into direct interactions to initiate a transaction [13]. Marketplaces can allow both ownership transfer and temporary access of a product. As an e-commerce, a  company  owning  the  digital  marketplace  provides  an  institutional  and  regulatory frame for the transactions on their platform and cannot be the main provider on the marketplace platform. Depending on the marketplace platform the offering can be an offline and/or digital product transfer, product access and/or service. Digital marketplace companies include famous examples such as Airbnb [23] and Uber [24], but also eBay [25] intermediating  for  second  handed  physical  goods,  Etsy  [26]  focusing  on handmade or vintage items and TicketSwap [27] offering a safe way to buy and sell etickets by transferring the PDF files. A digital marketplace is the combination of an ecommerce and a P2P platform.

- MPR12: Both peers can subscribe on the marketplace in an automatic and relatively quick way with a minimum of human intervention.

Sharing economy platform :  The definition most used for 'sharing economy' is the one by Frenken and Schor [6]: ' Consumers granting each other temporary access to under-utilized physical assets ('idle capacity'), possibly for money. We define a 'sharing economy platform' as a service platform allowing sharing economy transactions to happen.  A  typical  example  of  a  company  owning  a  sharing  economy  platform  is Airbnb, renting out temporarily vacant accommodation (under- utilized physical good) by any person to any other person (C2C) for an agreed upon number of days (temporary access). Taking this definition into account, a sharing economy platform is a marketplace with following requirements:

- MPR13: The transaction delivery is C2C

- MPR14: The service concerns a physical good

- MPR15: The physical good is under-utilized

- MPR16: Only temporary access is given to the physical good

Fig. 1. Service platform concepts

[FIGURE]

On top of the MPRs to define our future Competency Questions (CQs) as a base of our reference ontology, we also use three Common Platform Properties  (CPPs) of [28]:

- CPP1: A customer can send messages to the provider before the transaction concerning  the  listing  (listing  conversation)  and  after  the  transaction  (called  Transaction conversation).
- CPP2: During the transaction, a payment is made from the customer, for provider using an e-payment by an external payment processor (e.g. Stripe, PayPal). Part of this payment is a commission earned by the service company
- CPP3: After the delivery of the product and/or service, a review by the customer is collected by the service platform to inform future customers about the listing.

## 3 Discussions

In this short paper, we didn't fully differentiate between the difference of the virtual offering space for the services, the software and the company owning the service platform. We think it's important that our ontology is capable of capturing this difference. A second consideration is that this paper only compares and creates MPRs for a small number of platform concepts. We can enlarge our scope to other concepts (e.g. ondemand platform, access economy platform, business-platform-customer) and models (e.g. centralized resource pooling platforms or 'matchmakers' [29]).

Third, it remains a question what foundation and core ontologies to use as a base or our reference ontology, as UFO-S [16] might be to 'strict' to apply.

A fourth consideration is the validation process. This can differ between the ontology experts and the service platform experts. Also the influence of the anti-patterns simulation tool [17] on our validation can be of great interest.

## References

1. Codagnone, C., Martens, B.: Scoping the Sharing Economy:  Origins, Definitions, Impact and Regulatory Issues. Ssrn. (2016).
2. Nguyen, S., Llosa, S.: On the difficulty  to  define  the  sharing  economy  and collaborative  consumption  -  Literature  review  and  proposing  a  different approach with the introduction of 'collaborative services.' Journée la Relat. à la Marque dans un Monde Connect. 19-25 (2018).
3. Oh,  S.,  Moon,  J.Y.:  Calling  for  a  shared  understanding  of  the  'sharing economy.' 1-5 (2016).
4. Cheng, M.: Sharing economy: A review and agenda for future research. Int. J. Hosp. Manag. 57, 60-70 (2016).
5. Görög,  G.:  The  Definitions  of  Sharing  Economy:  A  Systematic  Literature Review. Management. 13, 175-189 (2018).
6. Frenken, K., Schor, J.: Putting the sharing economy into perspective. Environ. Innov. Soc. Transitions. 23, 3-10 (2017).
7. Ertz,  M.,  Durif,  F.,  Arcand,  M.:  Collaborative  consumption:  Conceptual snapshot at a buzzword. J. Entrep. Educ. 19, 1-23 (2016).
8. Wieringa, R.: What is a platform, https://www.thevalueengineers.nl/what-is-aplatform/.
9. Trabucchi, D., Muzellec, L., Ronteau, S.: Sharing economy : seeing through the fog economy. Internet Res. (2019).
10. Sutherland, W., Jarrahi, M.H.: The sharing economy and digital platforms: A review and research agenda. Int. J. Inf. Manage. 43, 328-341 (2018).
11. Ranjbari, M., Morales-Alonso, G., Carrasco-Gallego, R.: Conceptualizing the Sharing Economy through Presenting a Comprehensive Framework. (2018).
12. Dillahunt, T.R., Wang, X., Wheeler, E., Cheng, H.F., Hecht, B., Zhu, H., Wang, X., Wheeler, E.: The Sharing Economy in Computing: A Systematic Literature Review. Proc. ACM Hum.-Comput. Interact. 38, 38 (2017).

13. Täuscher,  K.,  Laudien,  S.M.:  Understanding  platform  business  models :  A mixed methods study of marketplaces. Eur. Manag. J. 36, (2018).
14. Ruy,  F.B.,  Guizzardi,  G.,  Falbo,  R.A.,  Reginato,  C.C.,  Santos,  V.A.:  From reference ontologies to ontology patterns and back. Data Knowl. Eng. 109, 4169 (2017).
15. Falbo,  R.A.,  Guizzardi,  G.,  Gangemi,  A.,  Presutti,  V.:  Ontology  patterns: Clarifying concepts and terminology. CEUR Workshop Proc. 1188, (2013).
16. Cesar, J., Almeida, R. De, Paulo, J., Almeida, A., Guizzardi, G., Ferreira, L., Sinderen, M.J. Van, Guarino, N., Morais, C.: A commitment-based reference ontology for services. Inf. Syst. 54, 263-288 (2015).
17. Guizzardi, G., Sales, T.P.: Detection, Simulation and Elimination of Semantic Anti-Patterns in Ontology-Driven Conceptual Models. In: ER 2014 (2014).
18. McAfee,  A.,  Brynjolfsson,  E.:  Machine,  Platform,  Crowd:  Harnessing  Our Digital Future. (2018).
19. Hagiu,  A.,  Wright,  J.:  Multi-Sided  Platforms.  Int.  J.  Ind.  Organ.  43,  1-32 (2015).
20. Ritter, M., Schanz, H.: The sharing economy: A comprehensive business model framework. J. Clean. Prod. 213, 320-331 (2019).
21. Filistrucchi, L., Geradin, D., Van Damme, E., Affeldt, P.: Market definition in two-sided markets: Theory and practice. J. Compet. Law Econ. 10, 293-339 (2014).
22. Hepp, M.: GoodRelations: An ontology for describing products and services offers  on  the  web.  Lect.  Notes  Comput. Sci. (including Subser. Lect. Notes Artif. Intell. Lect. Notes Bioinformatics). 5268 LNAI, 329-346 (2008).
23. Airbnb, https://www.airbnb.com/.
24. Uber, www.uber.com.
25. eBay, https://www.ebay.com.
26. Etsy, https://www.etsy.com/.
27. TicketSwap, https://www.ticketswap.uk/.
28. Derave, T., Sales, T.P., Verdonck, M., Gailly, F., Poels, G.: Domain Ontology for Digital Marketplaces. In: ER 2019 Workshops, LNCS 11787 proceedings. pp. 1-10 (2019).
29. Hafermalz, E., Boell, S.K., Elliot, S., Hovorka, D., Marjanovic, O.: Exploring Dimensions  of  Sharing  Economy  Business  Models  Enabled  by  IS:  An Australian Study. Australas. Conf. Inf. Syst. 1-11 (2016).
