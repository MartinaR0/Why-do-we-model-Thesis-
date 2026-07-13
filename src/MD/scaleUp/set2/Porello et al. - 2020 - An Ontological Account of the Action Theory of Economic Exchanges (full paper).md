## An Ontological Account of the Action Theory of Economic Exchanges

Daniele Porello 1 , Giancarlo Guizzardi 2 , Tiago Prince Sales 2 , Glenda Amaral 2 , and Nicola Guarino 1

1 ISTC-CNR Laboratory for Applied Ontology, Trento, Italy {daniele.porello,nicola.guarino}@cnr.it

2 Conceptual and Cognitive Modelling Research Group (CORE),

Free University of Bozen-Bolzano, Bolzano, Italy

{giancarlo.guizzardi,tiago.princesales,gmouraamaral}@unibz.it

Abstract. In recent years, there has been an increasing interest in the development of ontologically well-founded conceptual models for Information Systems in areas such as Service Management, Accounting Information Systems and Financial Reporting. Economic exchanges are central phenomena in these areas. For this reason, they occupy a prominent position in modelling frameworks such as the REA (Resource-Event Action) ISO Standard as well as the FIBO (Financial Industry Business Ontology). In this paper, we begin a well-founded ontological analysis of economic exchanges inspired by a recent ontological view on the nature of economic transactions. According to this view, what counts as an economic transaction is based on an agreement on the actions that the agents are committed to perform. The agreement is in turn based on convergent preferences about the course of action to bring about. This view enables a unified treatment of economic exchanges, regardless the object of the transaction, and complies with the view that all economic transactions are about services. In this paper, we start developing our analysis in the framework of the Unified Foundational Ontology (UFO).

Keywords: Economic Exchanges, Preferences, Enterprise Modeling, Business Ontology, Unified Foundational Ontology

## 1 Introduction

Economic exchanges are peculiar forms of agents' interaction that pervades important application areas of Information Systems, such as Service Management, Accounting Information Systems, Financial Reporting, Value Modelling, and Business Ontologies. The nature of economic exchanges has been thoroughly debated in philosophy since at least the Eighteen century, when the epistemological status of the crucial concepts of the economic theory has been intensively discussed. For a succinct overview of the complex conceptual issues of this rich debate, we refer to [15].

Two important issues in the debate on the nature of economic exchanges -which are quite pressing for a fruitful ontological understanding of economic interactions- concern the nature of the things being exchanged and the matter of the agreement between the transacting agents. Whether the matter of transaction are objects, actions, events, or promises; and whether the agreement is based on (and justified by) converging or inverse interests are crucial aspects for an ontological understanding of economic transactions.

An ontological analysis of economic exchanges has to provide an understanding of what economic exchanges are, of what is exchanged in transactions, and of the reasons that explains why the exchange happens. To approach this delicate issues, we shall rely on a recent perspective on these points provided by Massin and Tieffenbach, cf. [17], and named Action Theory of Economic Exchanges (ATE). The motivations for using ATE as a general of view economic exchanges are the following ones. Firstly, it allows for a quite general view of economic exchanges concerning heterogeneous items (e.g. both goods and services). Secondly, and more importantly, ATE is a philosophically rich view that explains why and under which conditions an economic exchange takes places. Finally, ATE models economic exchanges from the perspective of both agents involved in the transactions, the so-called helicopter view, cf. [16]. For the previous reasons, we claim that ATE is more apt to guide a foundational analysis of economic exchanges than, for instance, the (Resource-Event-Action) REA modelling is. In particular, REA is focusing mainly on exchanges of resources, it does not explain why a transaction happens, and it takes the partial perspective of a single actor of the exchange.

In the subsequent sections, we shall develop an ontological understanding of economic exchanges according to ATE. The goal of this paper is to use ATE as a guide to lay down the main foundational aspects for modelling economic exchanges. To make our ontological investigation precise, we shall place our analysis within the Unified Foundational Ontology (UFO), cf. [13,14].

One of the reasons for using UFO is the rich treatment of relations that it provides, cf. [9]. This feature is compelling, as we shall see, for modelling concepts in economics. Moreover, UFO is associated to a well-founded version of the UML 2.0 fragment of class diagrams, dubbed OntoUML, which has been extensively used for developing an ontologically sound methodology for conceptual modelling. So to put the theory at work in possible modelling applications, we present a simplified version of a OntoUML model of economic exchanges.

This paper contributes to our long term research program of providing a solid ontological foundation of economics, cf. [27,24,3,2,12,26]. A closely related work is [5], which also approaches economic exchanges in UFO. The main difference with our approach is that we ground our analysis on Massin and Tieffenbach's ATE, [17]. Another related work is [28], which starts the development of commercial exchanges in the foundational ontology BFO.

The remainder of this paper is organised as follows. In Section 2, we summarise Massin and Tieffenbach's theory of economic exchanges ATE [17]. Then, in Section 3, we briefly introduce UFO, focusing in particular on its relational aspects and its notion of relator . Section 4 proposes the treatment of economic exchanges in UFO by modelling the concepts of preference, economic offering, and economic transaction. Lastly, Section 5 concludes and indicates future work.

## 2 The Metaphysics of Economic Exchanges

In this section, we present the main tenets of the theory of the Action Theory of Exchanges (ATE) proposed by Massin and Tieffenbach in [17]. The theory contrasted with the Standard Theory of Exchanges (STE). Briefly, the STE makes the following claims to explain what happens when agents A and B exchange goods x and y :

- -inverse preferences : A and B have inverse preferences concerning x and y , e.g. A prefers x to y and B prefers y to x ;
- -mutual transfers : A voluntary transfers y to B and B voluntary transfers x to A ; and
- -the motivation for the transfer is (partially) founded in the preferences of A and B .

The STE is convincingly criticised in [17] on the ground that it is, primarily, an incomplete view. Firstly, STE does not immediately account for economic transactions concerning services. In that case, what happens in the transaction can hardly be understood in terms of a transfer of resources that pass from one agent to another. Therefore, STE is confined to economic exchanges concerning transferable items. Secondly, the STE fails to account for the motivations for entering the transaction. The inverse preference hypothesis is not sufficient to explain why, for instance, A would exchange the x for y specifically with B and not with any other agent. The inverse preference assumption is silent about this point.

To cope with this limitations, a new theory of economic exchanges is proposed in [17]. The crucial assumption is that, in any economic transaction, the 'object' of the transaction is a pair of actions performed by the relevant agents.

We summarise the main points of ATE in the following definition.

Definition 1. Agents A and B are transacting about actions φ and ψ iff

1 Preferences and beliefs :

- 1.1 A prefers that A does φ and B does ψ , rather than A does not φ and B does not ψ .
- 1.2 B prefers that A does φ and B does ψ , rather than A does not φ and B does not ψ .
- 1.3 A believes that promising to B to do φ on condition that B does ψ is a way to make B to do ψ .

2 Offer and acceptance

- 2.1 The offer: because of 1.1. and 1.3, A promises to B that A will do φ , if B does ψ
- 2.2 The acceptance: because of 1.2, B accepts the offer.

- 3.1 Because of 2.2, B does ψ . Therefore, A is obliged to do φ

```
3 Provisions 3.2 Because of 2.1 and 3.1, A does φ .
```

```
.
```

A few points are worth noticing. Firstly, by viewing the object of transactions as actions, the ATE is more apt to include economic transactions on services. Secondly, the inverse preference assumption is now replaced with the assumption about the convergence of the agents' preferences to the same pair of actions. Moreover, the actions to which the agents commit explicitly mention the relevant agents of the actions, which are in fact the very agents involved in the transaction. Thirdly, an economic transaction starts with an offering, cf. point 2.1, which is based on the preference of one agent for a certain course of action and on the belief that, by promising something to another agent, this course of action can take place. Finally, an economic transaction generates commitments and claims. In point 2.1, A commits to do φ if B does ψ (a conditional commitment). In point 3.1, since B has accepted the offer, B is committed to do ψ , then once B has done ψ , A is obliged to do φ (an unconditional commitment). Moreover, when B accepts the offer, A has a claim towards B to do ψ and, when B does ψ , B has a claim towards A that she or he does φ . Thus the mechanism of ATE works by turning a conditional commitment into an unconditional commitment under the suited conditions. For this reasons, ATE also provides an explanation of why and under which circumstances an economic exchange happens. In Section 4, we shall see how to understand and model the main points of Definition 1 within UFO.

## 3 The Unified Foundational Ontology

As we shall see, a crucial aspect for dealing with economic exchanges is the rich treatment of relations provided by UFO, cf. [9]. Simplifying a bit, in UFO, we separate types, i.e. entities that classify, from endurants (aka objects) and perdurants (aka events), i.e. entities that may be instance of types, cf. [13,14,9]. Types are also separated into relational (or n -ary) types ( Relation ) and unary types, in particular, Endurant Type that classify endurants, cf. [9].

Fig. 1. The taxonomy of UFO

[FIGURE]

We focus here on the type of endurants. As the taxonomy in Figure 1 shows, endurants comprise Substantial , e.g. ordinary objects, and Moments , that is, aspects of the objects: the colour of a rose, the courage of a person, the maternal commitment of a mother towards her child. An important distinction between moments is that between Intrinsic Moment and Extrinsic Moment . The former include qualities of objects that do not depend on other entities (e.g. individual qualities, such as the colour or the weight). The latter include relational qualities that inhere in an endurant but existentially depend on something external to that endurant. This class includes, for instance, the love of a mother for her child and the mutual commitments of a conjugal relationship. Extrinsic Moment are in turn divided into two subclasses: Externally dependent modes (or single-sided relators, [9]) and Relators . The ontological distinction between this two classes is that externally dependent modes are modes that inhere in an endurant and that are externally dependent on another endurant. So, the love of a mother for her child is a mode that inheres in the mother and externally depends on the child. By contrast, a relator requires a mutual pattern of dependence between the relational qualities that inhere in (at least) two distinct entities. For instance, the conjugal commitments in a marriage constitute a relator as the (mereological) sum of the commitments of the two partners, each commitment being externally dependent on the other partner. A further condition on externally dependent modes and on relations that we put in UFO is that each of them is founded on a unique event, e.g. the conjugal relator is founded on the marriage event. For a formalisation of this notions, we refer to [9]. Here we informally report the definition of relator:

An n -ary relator among n entities is the mereological sum of a number of externally dependent modes such that: i ) each mode inheres in one the n entities, ii ) each mode externally depends on another of the n entities and iii ) each mode is founded on a same event.

## 4 The Action Theory of Economic Exchanges in UFO

The core ingredients for representing the action theory of exchanges (ATE) in UFO are: agents, preferences, actions, beliefs and commitments (discussed in particular in [19]), economic offerings, and economic transactions. In this paper, we focus on economic offerings and transactions. Before approaching them, however, we start by summarising the treatment of preferences proposed in [24].

## 4.1 Preferences in the Action Theory of Exchanges

We assume a type for agents Agent (as endurants), which classifies the entities to which preference relations may be ascribed. Agent is a rigid non-sortal type, i.e., a type that essentially classifies individuals of different kinds , i.e., individuals that have different ontological natures [13]. For instance, in separating between individual and collective preferences, the class Agent may include individual or collective agents (e.g. organisations), with their specific ontological differences [23,7,21,22].

Since we assume that agents (that is, entities with intentionality ) are necessarily agents (in the modal sense), we stereotype the type Agent as a OntoUML Category . In other words, a Category is a type that describes essential properties that are shared by entities of different kinds . Agents can play the 'role' of Value Beholder in a value ascription relation. We represent the type Value Beholder as a role mixin because: (i) it classifies entities only contingently, i.e., no value beholder is necessarily a value beholder; (ii) one is a value beholder due to a relational condition; (iii) it is a mixin, i.e., it can classify entities of multiple kinds.

A Value Ascription is an example of a mode [13]. As we discussed, a mode is an existentially dependent entity that, as such, can only exist by inhering in some other individual. In particular, a value is a relationally dependent mode (or an externally dependent mode), i.e., a mode that inheres in an individual but which is also externally dependent on a different individual. In this case, a value ascription is a sort of mental state inhering in the value beholder but which is also externally dependent on a number of entities in Value Entity . A value ascription mode takes a value in at least one (but possibly several) Value Magnitude Spaces , via the quality of Value (a quality of the value ascription). These spaces have, in OntoUML, the semantics of abstract conceptual spaces, delimiting the possible values an intrinsic property can be projected into, cf. [13] (e.g. value magnitude space can account for cardinal or ordinal measures of value).

Finally, a Preference of an agent between two entities is relational mode (between the agent and the two entities) but a complex one (i.e., a complex mental state). A (binary) preference concerning two entities is a mode inhering a value beholder that is essentially composed of exactly two existing value ascriptions, inhering in that very same value beholder: i ) the value of the first entity given the second entity and ii ) the value of the second entity given the first entity. 3

In other words, a preference is a mereological sum of modes (value ascriptions) and, in that sense, it is similar to a relator ; However, since in this case all the constituents of this sum inhere in the same bearer (the value beholder) while depending on two entities (the compared ones), preference is indeed a complex externally dependent mode (or a single-sided relator).

A relational sentence expressing that an agent has a preference between two entities is then captured by means of the (ternary) relation prefers (a relational type in UFO, cf. [9,24]): ' i prefers x over y ' connects the rolemixin Value Beholder i with two other rolemixins Preferred Entity x and Deprecated Entity y . 4

3 An important aspect of preferences is that the valuation of the two options is not absolute, rather it depends on the act of comparison between the entities at issue. We thank Barry Smith for highlighting this point, cf. [28]. The ascription of value to an entity is always dependent on the goals of the agents in a certain context, see [25]. Hence, the ascription of value to the entities in a preference relation is dependent on the context of the comparison. This view also accommodates time-dependent preferences, in that preferences may change, when the context of comparison changes.

The entity whose ascribed value is higher plays the role of Preferred Entity ; the one with the lower magnitude then plays the role of Deprecated Entity . It should be clear by now to the reader why both Preferred Entity and Deprecated Entity are modelled as rolemixins: they both classify value entities contingently, in the scope of a preference relation, and classify entities of multiple kinds.

We apply now this view of preferences to ATE. To account for the preference relations used in ATE, we need to understand ontologically what are the entities about which agents have preferences. In ATE, preferences are definitely about pairs of actions. Recall point 1.1, ATE assumes that an agent A prefers that ' A does φ and B does ψ ' to ' A does not φ and B does not ψ '.

Actions are particular types of events in UFO, so preferences are prima facie about events that are composed of two actions. 5

This point is however quite delicate mainly for three reasons. Firstly, preference relations may be about events that may never occur. For instance, if I prefer to have pasta tonight at my place over pizza, and I have the means to satisfy my goal, then the event of me eating pizza tonight at my place in fact never happens. Thus, by defining preference over events, we are lead to include in our model instances of events that may never happen. 6

Secondly, ATE includes preference over negative actions, or omissions, e.g. ' A does not φ and B does not ψ '. The ontological status of negative actions as events is debated, cf. [6]. Some authors endorse ontological commitments to negative events, whereas others identify the negative event with the (positive) action that one performs while omitting, cf. [30].

Thirdly, by defining preferences over events, we are lead to view the object of the preference as fully determinate. That is, an agent must know to maximal detail the courses of actions that she or he is comparing. For instance, if I am preferring the particular event of having dinner at a Chinese restaurant to the event of having dinner at an Indian restaurant, I am implicitly comparing which waiter is assigned to my table, the exact moment in which the dinners start and end, the outfit that I am wearing, etc, at least if we consider events as thick entities.

4 According to the taxonomy in [9,11], prefers is an external descriptive relation, as it depends on the context of ascription of values. An insightful discussion on whether preferences are internal or external relations is proposed in [18].

5 By assuming a mereology of events for UFO, as in [1], we may define the event corresponding to 'A doing φ and B doing ψ ' as the mereological sum of the two events 'A doing φ ' and 'B doing ψ '.

6 An analysis of future and ongoing events has been discussed in particular in [10]. However, they would not suffice for modelling preferences, as we need to discuss events that may never happen in the actual world. Here, we only notice that a class of possible events is in fact compatible with the formal theory of UFO, which is phrased within a first-order modal logic where the definition of modalities entails the possibilia view of the particulars in the domain of the ontology (events included). That is, we may in principle assume events that never happen in the actual world, while happening in some other possible world. See [4] for a formalisation of events occurring in different time lines.

We are facing here two possible modelling choices: 1 ) we define preference over possible events , we assume that the events that populate the ontology may never happen in the actual world, that there are also events corresponding to omissions, and that the object of the preference is fully determined; or 2 ) we define preferences over types of events.

In this paper, we endorse strategy 2 ), and we leave a discussion of strategy 1 ) for a dedicated paper.

By viewing preferences as defined on types of events we can accommodate the three previous points as follows.

Concerning the first point, a type of event may have no instances in a model while still existing as a type. Types must have possible (in the modal sense) instances in UFO, which does not exclude that there are worlds where a type has no instances [14]. So we can talk about types of events that do not happen at a world, without introducing a special class of possible events.

Concerning the second issue, by defining preferences over types, we can avoid to take a position on the existence of negative events (or omissions): a type classifying negative actions may have instances that are either positive action (i.e. the actions that are performed while omitting) or truly negative actions, in case we commit to their existence.

Concerning the third point, defining preferences over types enables us to have preferences over sets of events, preventing the maximal determination of the agents' preferences. For instance, when I prefer the type of event 'going out to a Chinese restaurant' to the type 'going out to an Indian restaurant', I prefer any event of the former type to any event of the latter type, regardless of all the aspects that single out a particular event of each type.

Finally, by viewing the objects of preferences as types of events, we can overcome an explicit limitation of Massin and Tieffenbach's approach, namely, that of generalised preferences . Generalised preferences are at work when the economic exchange is addressed to someone , rather than to a particular agent (cf. [17], p. 189). For example, if I am selling my bike on ebay, my preference is about me selling the bike and someone paying the required prices. By viewing preferences, and hence economic exchanges, to be about types of actions, generalised preferences become understandable: E.g. I prefer the type of action such that someone pays the required price to the type of action such that nobody pays the required price. 7

7 The view that preferences are about types of events is also supported in the tradition of the logic of preferences, cf. [29,20]. Preferences are modal operators that apply to propositions, while propositions can indeed be construed as sets of possible worlds, i.e. sets of possible events compatible with the description provided by the proposition.

Summarising this discussion, an OntoUML module for preferences is depicted in Figure 2, where Preferred Entity and Deprecated Entity are thus to be intended as types of types of events. 8

Fig. 2. OntoUML model for preference relations

[FIGURE]

## 4.2 Economic offering and economic exchanges

We can approach now the modelling of economic exchanges. We start from an offering event, cf. Offering . This event is the foundation (cf. creation in OntoUML) of a relator Economic Offering which is composed of the (mereological) sum of (the externally dependent modes given by) the conditional commitment of the offerer and of the conditional claim of the offeree. Offerer and Offeree are again roles mixins here. The important aspects is that, at this point, the commitments and claims are conditional , which corresponds to stage 2.1 of Definition 1. According to our discussion of the entity that are related by preferences in ATE, the conditional commitments and claims are about a type of action, cf. commits to in OntoUML. The Offered Contribution Type and the Counterpart Contribution Type are in fact types of types of events. The offering is based on the preferences of the offerer, according to stage 2.1 of Definition 1. Notice that here, we changed Massin and Tieffenbach's model of ATE by viewing preferences as defined on types of actions. Accordingly, an instance of the class Economic Exchange Type is a type of event constructed by means of two types of events: the Offered Contribution Type and the Counterpart Contribution Type . Here, we are modelling the constructed type by means of the relation requires . The idea is that a type in Economic Exchange Type classifies events that have two components: a component classified by a type in Offered Contribution Type and a component in Counterpart Contribution Type . 9

8 In our modelling, preferences are defined by appealing to value ascriptions, which are approached in [25]. In fact, we have to extend that approach to include, as value objects, also types of events. Notice also that, to completely formalise our view, we need to enable multi-level modelling in UFO, as in [8].

The relation participate to events of type models the fact that the offerer participates in all the events of the offered contribution type and the offeree participates in all the events of the counterpart contribution type. This point accounts for the fact that the convergent preferences of the two agents, even in the case of preferences defined on types, mentions the agents involved in the transaction. 10 Figure 3 represents the modelling of economic offerings.

Fig. 3. Economic offering

[FIGURE]

To simplify, here we model the situation where the offer proposed by the offerer is immediately accepted, and no negotiation takes places between the two parts of the economic exchange, see Figure 4. If the offer is accepted by the offeree, then the event of the offering founds a new relator of Economic Agreement between the two agents. This model corresponds to stage 2.2. of Definition 1. The new relator conforms to, or complies with, the previously created economic offering relator. This new relator has parts the new unconditional commitments of the agents to fulfill the promised courses of actions (of the right type). This step realises the final outcome of Definition 1, namely the actualisation of steps 2.1 and 2.2 based on the provisions 3.1 and 3.2. The actual event of Economic Exchange requires then to have as parts the event (action) of fulfilment of the offerer commitments as well as the event (action) of the fulfilment of the requested counterparts. Those events are of the right type, i.e. the Offered Contribution and the Counterpart Contribution match the type in Offered Contribution Type and Counterpart Contribution Type (respectively), cf. the relation instantiation .

9 We leave a characterisation of the requires relation for future work.

10 We simplify a number of aspects of ATE. E.g. the economic offer is also based in [17] on the beliefs that the offeree share the same preference, cf. point 1.2 and 1.3.

Fig. 4. Economic exchange

[FIGURE]

## 5 Conclusion and Future Work

We provided the first elements for a well-founded ontological analysis of economic exchanges based on the action theory of exchanges proposed by [17]. We developed our analysis in UFO, which provides a very expressive ontology to discuss relational dependencies, and we introduced the basic elements of an OntoUML modelling of economic transactions. We highlighted the dependency of economic offerings and transactions on the converging preferences of the agents and we illustrated the mechanism of replacement of conditional with unconditional commitments that are in place in this forms of agents interaction. We proposed to view preferences and economic agreements about types of actions to avoid a number of problems of directly dealing with particular events.

An important point to notice is that this view of economic exchanges is very general and provides a unified treatment of a wide range of economic phenomena. For this reason, we plan to use this framework to provide a general ontology of economic phenomena in a future dedicated paper.

.

## References

1. Almeida, J.P.A., Falbo, R.A., Guizzardi, G.: Events as entities in ontology-driven conceptual modeling. In: International Conference on Conceptual Modeling. pp. 469-483. Springer (2019)
2. Amaral, G.C.M., Guizzardi, G., Guarino, N., Porello, D., Sales, T.P.: Capability agreements and risk. In: Short Paper Proceedings of the 13th International Workshop on Value Modeling and Business Ontologies, VMBO, 2019, Stockholm, Sweden, March 4-5, 2019 (2019)
3. Amaral, G.C.M., Sales, T.P., Guizzardi, G., Porello, D.: Towards a reference ontology of trust. In: On the Move to Meaningful Internet Systems: OTM 2019 Conferences - Confederated International Conferences: CoopIS, ODBASE, C&amp;TC 2019, Rhodes, Greece, October 21-25, 2019, Proceedings. pp. 3-21 (2019)
4. Benevides, A.B., Almeida, J.P.A., Guizzardi, G.: Towards a unified theory of endurants and perdurants: Ufo-ab. In: Proceedings of the Joint Ontology Workshops 2019 Episode V: The Styrian Autumn of Ontology, Graz, Austria, September 23-25, 2019. CEUR Workshop Proceedings, vol. 2518. CEUR-WS.org (2019)
5. Blums, I., Weigand, H.: A financial reporting ontology for market, exchange, and enterprise shared information systems. In: IFIP Working Conference on The Practice of Enterprise Modeling. pp. 83-99. Springer (2019)
6. Casati, R., Varzi, A.: Events. In: Zalta, E.N. (ed.) The Stanford Encyclopedia of Philosophy. Metaphysics Research Lab, Stanford University, winter 2015 edn. (2015)
7. Ferrario, R., Masolo, C., Porello, D.: Organisations and variable embodiments. In: Formal Ontology in Information Systems - Proceedings of the 10th International Conference, FOIS 2018, Cape Town, South Africa, 19-21 September 2018. pp. 127140 (2018)
8. Fonseca, C.M., Almeida, J.P.A., Guizzardi, G., de Carvalho, V.A.: Multi-level conceptual modeling: From a formal theory to a well-founded language. In: Trujillo, J., Davis, K.C., Du, X., Li, Z., Ling, T.W., Li, G., Lee, M. (eds.) Conceptual Modeling - 37th International Conference, ER 2018, Xi'an, China, October 22-25, 2018, Proceedings. Lecture Notes in Computer Science, vol. 11157, pp. 409-423. Springer (2018)
9. Fonseca, C.M., Porello, D., Guizzardi, G., Almeida, J.P.A., Guarino, N.: Relations in ontology-driven conceptual modeling. In: Conceptual Modeling - 38th International Conference, ER 2019, Salvador, Brazil, November 4-7, 2019, Proceedings. pp. 28-42 (2019)
10. Guarino, N.: On the semantics of ongoing and future occurrence identifiers. In: International Conference on Conceptual Modeling. pp. 477-490. Springer (2017)
11. Guarino, N. et al.: Reification and Truthmaking Patterns. In: Proc.37th ER (2018)
12. Guarino, Nicola and Guizzardi, Giancarlo and Sales, Tiago Prince: On the Ontological Nature of REA Core Relations. In: Proc. 12th VMBO (2018)
13. Guizzardi, G.: Ontological Foundations for Structural Conceptual Models. Telematica Instituut / CTIT (2005)
14. Guizzardi, G. et al.: Endurant Types in Ontology-Driven Conceptual Modeling: Towards OntoUML 2.0. In: Proc.37th ER (2018)
15. Herzog, L.: Markets. In: Zalta, E.N. (ed.) The Stanford Encyclopedia of Philosophy. Metaphysics Research Lab, Stanford University, fall 2017 edn. (2017)
16. Laurier, W., Kiehn, J., Polovina, S.: Rea 2: A unified formalisation of the resourceevent-agent ontology. Applied Ontology 13(3), 201-224 (2018)

17. Massin, O., Tieffenbach, E.: The metaphysics of economic exchanges. Journal of Social Ontology 3(2), 167-205 (2016)
18. Mulligan, K.: Is preference primitive? Against boredom. 17 Essays presented to Nils-Eric Sahlin, Lund: Fri tanke förlag pp. 169-80 (2015)
19. Nardi, J.C., de Almeida Falbo, R., Almeida, J.P.A., Guizzardi, G., Pires, L.F., van Sinderen, M.J., Guarino, N., Fonseca, C.M.: A commitment-based reference ontology for services. Information systems 54, 263-288 (2015)
20. Osherson, D., Weinstein, S.: Modal logic for preference based on reasons. In: In Search of Elegance in the Theory and Practice of Computation, pp. 516-541. Springer (2013)
21. Porello, D.: A proof-theoretical view of collective rationality. In: IJCAI 2013, Proceedings of the 23rd International Joint Conference on Artificial Intelligence, Beijing, China, August 3-9, 2013. pp. 317-323 (2013)
22. Porello, D.: Logics for modelling collective attitudes. Fundamenta Informaticae 158(1-3), 239-275 (2018)
23. Porello, D., Bottazzi, E., Ferrario, R.: The ontology of group agency. In: Formal Ontology in Information Systems - Proceedings of the Eighth International Conference, FOIS 2014, September, 22-25, 2014, Rio de Janeiro, Brazil. pp. 183-196 (2014)
24. Porello, D., Guizzardi, G.: Towards an ontological modelling of preference relations. In: AI*IA 2018 - XVIIth International Conference of the Italian Association for Artificial Intelligence, Trento, Italy, November 20-23, 2018. pp. 152-165 (2018)
25. Sales, T.P., Guarino, N., Guizzardi, G., Mylopoulos, J.: An ontological analysis of value propositions. In: 2017 IEEE 21st International Enterprise Distributed Object Computing Conference (EDOC). pp. 184-193. IEEE (2017)
26. Sales, T.P., Porello, D., Guarino, N., Guizzardi, G., Mylopoulos, J.: Ontological foundations of competition. In: Formal Ontology in Information Systems - Proceedings of the 10th International Conference, FOIS 2018, Cape Town, South Africa, 19-21 September 2018. pp. 96-109 (2018)
27. Sales, T.P. et al.: The Common Ontology of Value and Risk. In: Proc.37th ER (2018)
28. Vajda, J., Merrell, E., Smith, B.: Toward an ontology of commercial exchange. In: Barton, A., Seppälä, S., Porello, D. (eds.) Proceedings of the Joint Ontology Workshops 2019 Episode V: The Styrian Autumn of Ontology, Graz, Austria, September 23-25, 2019. CEUR Workshop Proceedings, vol. 2518. CEUR-WS.org (2019), http://ceur-ws.org/Vol-2518/paper-SOLEE7.pdf
29. Van Benthem, J., Girard, P., Roy, O.: Everything else being equal: A modal logic for ceteris paribus preferences. Journal of philosophical logic 38(1), 83-125 (2009)
30. Varzi, A.C.: Omissions and causal explanations. In: Agency and Causation in the Human Sciences, pp. 155-67. Paderborn, Germany: Mentis Verlag (2007)
