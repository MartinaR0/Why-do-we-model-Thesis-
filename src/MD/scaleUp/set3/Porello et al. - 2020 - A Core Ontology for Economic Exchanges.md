[FIGURE]

## A Core Ontology for Economic Exchanges

Daniele Porello 1 , Giancarlo Guizzardi 2 , Tiago Prince Sales 2 , and Glenda Amaral 2( B )

1 ISTC-CNR Laboratory for Applied Ontology, Trento, Italy daniele.porello@cnr.it

- 2 Conceptual and Cognitive Modeling Research Group (CORE), Free University of Bozen-Bolzano, Bolzano, Italy

{ giancarlo.guizzardi,tiago.princesales,gmouraamaral } @unibz.it

Abstract. In recent years, there has been an increasing interest in the development of well-founded conceptual models for Service Management, Accounting Information Systems and Financial Reporting. Economic exchanges are a central notion in these areas and they occupy a prominent position in frameworks such as the Resource-Event Action (REA) ISO Standard, service core ontologies (e.g., UFO-S) as well as financial standards (e.g. OMG's Financial Industry Business Ontology - FIBO). We present a core ontology for economic exchanges inspired by a recent view on this phenomenon. According to this view, economic exchanges are based on an agreement on the actions that the agents are committed to perform. This view enables a unified treatment of economic exchanges, regardless the object of the transaction. We ground our core ontology on the Unified Foundational Ontology (UFO), discussing its formal and conceptual aspects, instantiating it as a reusable OntoUML model, and confronting it with the REA standard and the UFO-S service ontology.

Keywords: Economic exchanges · Preferences · Enterprise modeling · Business ontology · Unified Foundational Ontology

## 1 Introduction

The nature of economic exchanges has been thoroughly debated in philosophy, economics, and social sciences, since at least the Eighteenth century, when the epistemological status of the main concepts of the economic theory was intensively discussed in search of a solid foundation, cf. [10]. Two important issues regarding the nature of economic exchanges -which are quite pressing for a fruitful ontological understanding of economic interactions- are the nature of the things being exchanged and the matter of the agreement between the transacting agents. Do we transact goods, services, objects, actions, events, or promises? Are we motivated to transact because of converging or inverse interests?

To approach these delicate points, we shall rely on the Action Theory of Economic Exchanges (ATE) [12], a recent perspective from the area of philosophy of economics. The motivation for this choice is three-fold. Firstly, it allows for a quite general view of economic exchanges concerning heterogeneous items (e.g. both goods and services). Secondly, the ATE explains why and under which conditions an economic exchange takes place. Finally, the ATE models economic exchanges from the perspective of both agents involved in a transaction, the so-called 'helicopter view', cf. [11]. For the above-mentioned reasons, we claim that ATE is more apt to guide a foundational analysis of economic exchanges than, for instance, the ISO standard for Accounting Information Systems REA (Resource-Event-Action) [13]. In particular, REA focuses mainly on exchanges of resource items. It does not explain why a transaction happens and it takes the partial perspective of a single actor of the exchange. As we shall see, the REA modeling style can indeed be retrieved within the ATE, which is in fact a richer perspective.

In the subsequent sections, we shall develop an ontological account of economic transactions according to the ATE. The goal of this paper is to use the ATE as a guide to lay down the main aspects of a core ontology of economic interactions. To make our investigation precise and applicable to designing wellfounded Information Systems, we shall place our analysis within the Unified Foundational Ontology (UFO) [7-9]. One of the reasons for using UFO is its rich treatment of relations [4], a compelling feature, as we shall see, for modeling concepts in economics. Moreover, UFO is associated to a well-founded UML profile (OntoUML) [7], which has been extensively used for developing an ontologically sound methodology for conceptual modeling. So to put the ATE to work in modeling applications, we present a reusable OntoUML model of economic exchanges.

To demonstrate the expressiveness and generality of our core ontology, we use it to analyze and ground both REA and UFO-S. The latter is a core ontology of services, which has been shown to be able to harmonize different views of service, ranging from marketing-oriented views (e.g., Service Dominant Logic) to a capability-oriented views in service science, to technology-oriented views (as in Archimate) [14]. Moreover, it was successfully employed to analyze a number of prominent mainstreams service modeling languages (e.g., SoaML, USDL, Archimate) [15]. Finally, it influenced the efforts towards defining a federal government ontology of services for the national infrastructure of open data in Brazil 1 . As we show here, both REA and UFO-S can be seen as a special case of our core ontology.

A closely related work to the one presented here is [2], which also approaches economic exchanges in UFO. Another related work is [20], which starts the development of an ontology of commercial exchanges in the foundational ontology BFO. In comparison to the latter, by levaraging on UFO's theory of relations, our work is able to capture the nature of economic offering and agreements as full-fledged endurants [5] and, as such, as entities capable of genuine changes in time (as opposed to modeling only the events and descriptions related to this phenomenon). This benefit is also present in [2] (and for the same reason). Our main difference with respect to that approach is our explicit connection to the notion of economic preference and its explicit grounding on a modern philosophy theory of economic exchange (ATE).

[1 See http://wiki.gtinda.ibge.gov.br/Ontologia-Servicos-Publicos.ashx.](http://wiki.gtinda.ibge.gov.br/Ontologia-Servicos-Publicos.ashx)

The paper is organized as follows. Section 2 presents the ATE and a brief view on the UFO and OntoUML. Section 3 presents the main contribution of this paper, i.e., a well-founded ontology of ATE in light of UFO. Section 4 concludes by showing the application of this ontology to analyze and ground REA and UFO-S.

## 2 Background: ATE and UFO

## 2.1 The Action Theory of Economic Exchanges (ATE)

The core assumption made by the Action Theory of Exchanges (ATE) [12] is that, in any economic transaction, the 'object' of the transaction is a pair of actions to be performed by the relevant agents involved in it. The main assumptions of the ATE are summarised below:

Definition 1. Agents a and b are transacting about actions φ and ψ iff

1. Preferences and beliefs :
2. 1.1 a prefers that a does φ and b does ψ , to a does not φ and b does not ψ .
3. 1.2 b prefers that a does φ and b does ψ , to a does not φ and b does not ψ .
4. 1.3 a believes that promising to b to do φ on condition that b does ψ is a way to make b to do ψ .
5. 2 Offer and acceptance :
6. 2.1 Because of 1.1. and 1.3, a promises to b that a will do φ , if b does ψ
7. 2.2 Because of 1.2, b accepts the offer.
8. 3 Provisions :
9. 3.1 Because of 2.2, b does ψ . Therefore, a is obliged to do φ .
10. 3.2 Because of 2.1 and 3.1, a does φ .

Three points are worth noticing. Firstly, by viewing the object of transactions as actions, the ATE is capable of accounting for economic transactions about goods as well as services. In the case of services, the agreement is about the respective actions to be performed by the relevant parties. E.g. a customer and a delivery company agree on the pair of actions φ : ' a pays the agreed amount to company b ' and ψ : 'The company b delivers the requested service to a '. In the case of goods, the preferred pair of actions can be expressed in terms of the transfer of ownership, the action of transferring the ownership of an item: e.g. φ : ' a transfer the ownership of her laptop to b ' and ψ : ' b pays the agreed amount to a '.

Secondly, the assumption about the convergence of the agents' preferences to the same pair of actions is an important bit here, as it is capable of explaining why two agents are in fact transacting with each other (and not with other parties). The actions to which the agents commit explicitly mention the relevant agents of the actions, which are in fact the very agents involved in the transaction: when an actual transaction between a and b happens, a is intending to transact precisely with b , and not to an other agent.

Thirdly, the ATE is a quite rich reconstruction of the steps happening in an economic exchange. If the preconditions in point 1 of Definition 1 are met, an economic transaction starts with an offering, cf. point 2.1, which is based on the preference of one agent for a certain course of action and on the belief that, by promising something to another agent, this course of action can take place. Moreover, an economic offering generates obligations, i.e. commitments. In point 2.1, a promises to (commits to) do φ , if b does ψ (a conditional commitment). In point 3.1, since b has accepted the offer, b is committed to do ψ , then once B has done ψ , a is obliged to do φ (an unconditional commitment). Thus the ATE's mechanism for explaining why economic transactions happen works by turning a conditional commitment into an unconditional commitment, under the suited conditions. For this reasons, ATE also provides an explanation of why and under which circumstances an economic exchange happens. As we shall see, the unfolding of commitments in ATE is quite similar to what happens to service offerings in UFO-S, cf. [14].

## 2.2 The Unified Foundational Ontology (UFO)

UFO is an axiomatic theory combining results from formal ontology in philosophy, linguistics, cognitive science and philosophical logics [8]. Over the years, UFO has been systematically designed as a foundation for addressing basic concepts in conceptual modeling. In order to ground our models on UFO, we employ OntoUML, a UFO-based ontology-driven conceptual modeling language [7]. OntoUML is a version of UML class diagrams constructed to reflect the categories and axiomatization of UFO. UFO and OntoUML have been successfully employed in academic, industrial and governmental settings to create conceptual models in a variety of different application domains [8].

UFO separates individuals in endurants (aka objects) and perdurants (aka events). Individuals instantiate types. Types are also separated into relational (or n -ary) types ( Relation ) and unary types, in particular, Endurant Type that classify endurants. For a complete review on UFO, one should refer to [4,7,9].

We focus here on endurant types. They comprise Substantial Type , e.g. types whose instances are ordinary objects (e.g. a flower, a person), and Moment Type , that is, types whose instances are aspects of objects (e.g. the colour of a rose, the courage of a person). Moment Type is further classified into Intrinsic Moment Type and Extrinsic Moment Type . The former includes types whose instances are aspects of objects that do not depend on other entities (e.g. the courage of a person). The latter includes types whose instances are relational aspects, i.e. they inhere in an entity but existentially depend on something external to that entity. Examples of relational aspects include the love of a mother for her child and the mutual commitments of a conjugal relationship. Extrinsic Moment Type is in turn divided into two subclasses: Extrinsic Mode Type (or single-sided relators, [4]) and Relator Type . The former refers to types whose instances inhere in a single endurant, but are externally dependent on other endurants. So, the love of a mother for her child is a mode that inheres in the mother and externally depends on the child. By contrast, a relator requires a mutual pattern of dependence between the relational qualities that inhere in (at least) two distinct entities. For instance, the conjugal commitments in a marriage constitute a relator as the (mereological) sum of the commitments of the two partners, each commitment being externally dependent on the other partner. A further condition on externally dependent modes and on relators is that each of them is founded on a unique event, e.g. the conjugal relator is founded on the marriage event. For a formalisation of this notions, we refer to [4].

Anticipating our view of economic transactions, economic offering shall be represented as relators: they are the sum of the commitments and of the obligations of the parties involved in the transaction.

Orthogonal to the specialization of Endurant Types w.r.t. the nature of their instances, UFO also specialize them regarding their relation to the ontological notions of essence , rigidity , and relational dependence [7]. Endurant Types can be either Sortals or Non-Sortals . Sortals are either Kinds or specializations of a Kind . A Kind is a central notion here as it defines what endurants in this domain are essentially , i.e., in all possible situations (the set of all our possible instances is a tessellation of rigid, i.e., static kinds ). An antirigid (i.e., dynamic, contingent) Sortal specializing a Kind is a Role . Roles are also relationally dependent, i.e., individuals (contingently) play Roles in the scope of a relation. Non-Sortals are types that classify individuals of multiple Kinds . A rigid (static) Non-Sortal is termed a Category ; a role-like anti-rigid Non-Sortal that can be played by individuals of multiple kinds is termed a Role Mixin .

## 3 The Action Theory of Economic Exchanges in UFO

The core ingredients for representing the ATE in UFO are: agents, preferences, actions, beliefs and commitments, economic offerings, and economic exchanges . The focus here is on economic offerings and transactions.

Agent is a rigid non-sortal type, i.e., a type that essentially classifies individuals of different kinds , i.e., individuals that have different ontological natures [7]. The class Agent may include individual or collective agents (e.g. organisations, companies, etc.), with their specific ontological differences [3,16].

Since agents (i.e. entities with intentionality ) are necessarily agents (in the modal sense), we stereotype the type Agent as an OntoUML Category . Agents can play the 'role' of Value Beholder in a value ascription relation, the relation by which an agent assigns a value to an entity. We represent the type Value Beholder as a role mixin because: (i) it classifies entities only contingently, (ii) one is a value beholder due to a relational condition; (iii) it is a Non-Sortal , i.e., it can classify entities of multiple kinds.

A Value Ascription is a mode [7,19]. As we discussed, a mode is an existentially dependent entity that, as such, can only exist by inhering in some other individual. In particular, a value is a externally dependent mode , i.e., a mode that inheres in an individual but which is also externally dependent on a different entity. So, a value ascription is a sort of mental state inhering in the value beholder that is also externally dependent on a number of entities in Value Entity . A value ascription mode takes a value in at least one (but possibly several) Value Magnitude Spaces , via the quality of Value (a quality of the value ascription). These spaces have, in OntoUML, the semantics of abstract conceptual spaces, delimiting the possible values a property can be projected into, cf. [7] (e.g. we can account for cardinal or ordinal measures of value).

Finally, a Preference , cf. [17], of an agent between two entities is relational mode (between the agent and the two entities) but a complex one (i.e., a complex mental state). A (binary) preference concerning two entities is a mode inhering a value beholder that is essentially composed of exactly two existing value ascriptions (it is the mereological sum of them), inhering in that very same value beholder: i ) the value of the first entity given the second entity and ii ) the value of the second entity given the first entity. 2

The (ternary) relation prefers (a relational type in UFO, cf. [4]) in ' i prefers x over y ' connects the rolemixin Value Beholder i with two other rolemixins Preferred Entity x and Deprecated Entity y .

To apply this view of preferences to ATE (step 1.1 and 1.2 of Definition 1), we need to understand ontologically what are the entities about which the agents have preferences. In ATE, preferences are definitely about pairs of actions (cf. point 1.1.) Actions are particular types of events in UFO, so preferences are prima facie about events that are composed of two actions. 3

This point is however quite delicate, for the reasons highlighted in [18].

The solution adopted here is to view preferences as being about types of actions. This solution enables flexibility in describing the object of the preference. Firstly, agents may have preferences over actions that may not actually occur or even over negative actions: instead of introducing a category of possible or negative actions, we can do by introducing the right type of actions, which may not be instantiated in the actual world. Secondly, types enable a flexible degree of determination of the actions at issue: we do not need to assume that agents can fully determinate the events they are preferring. Summing up, an OntoUML module for preferences is depicted in Fig. 1, where Preferred Entity and Deprecated Entity are thus to be intended as types of types of events.

## 3.1 Economic Offering and Economic Transactions

We can finally approach the modeling of economic transactions. We start from the offering event, cf. Offering . This event is the foundation (cf. creation in OntoUML) of a relator Economic Offering which is composed of the (mereological) sum of (the externally dependent modes given by) the conditional commitment of the offerer and of the offeree. Offerer and Offeree are again roles mixins here. The important aspects is that, at this point, the commitments and claims are conditional , which corresponds to stage 2.1 of Definition 1. According to our discussion in Section 4.1 about the entities that are related by preferences in ATE, the conditional commitments are about types of actions, cf. commits to in OntoUML. The Offered Contribution Type and the Counterpart Contribution Type are in fact types of types of events. The offering is based on the preferences of the offerer, according to stage 2.1 of Definition 1. Notice that here is where we changed Massin and Tieffenbach's model from ATE by viewing preferences as defined on types of actions. Accordingly, an instance of the class Economic Exchange Type is a type of event constructed by means of two types of events: the Offered Contribution Type and the Counterpart Contribution Type . We are modeling the constructed type by means of the relation requires . The idea is that a type in Economic Exchange Type classifies events that have two components: a component classified by a type in Offered Contribution Type and a component in Counterpart Contribution Type . 4

2 The preference depends on the context of comparison between the entities, cf. [19,20].

3 By assuming a mereology of events, cf. [1], the event 'A doing φ and B doing ψ ' is defined as the mereological sum of the two events 'A doing φ ' and 'B doing ψ '.

Fig. 1. OntoUML model of preference relations.

[FIGURE]

The relation participate to events of type models the fact that the offerer participates in all the events of the offered contribution type and the offeree participates in all the events of the counterpart contribution type. This point accounts for the fact that the convergent preferences of the two agents have to mention the relevant agents involved in the transaction. 5 Figure 2 represents the OntoUML modeling of economic offerings.

To shorten the exposition, here we model the situation where the offer proposed by the offerer is immediately accepted, and no negotiation takes places between the parties, see Fig. 3. If the offer is accepted by the offeree, then the event of the offering founds a new relator of Economic Agreement between the two agents. This step provides the ontological counterpart of stage 2.2. of Definition 1. The new relator complies with the previously created economic offering relator. This new relator has parts the new (now) unconditional commitments of the agents to fulfill the promised courses of actions (of the required type). This step realises the final outcome of Definition 1, namely the actualisation of steps 2.1 and 2.2 based on the provisions 3.1 and 3.2. The actual event of Economic Exchange is required then to have as parts the event (action) of fulfilment of the offerer commitments as well as the event (action) of the fulfilment of the requested counterparts. Those events are of the right type, i.e. the Offered Contribution and the Counterpart Contribution match the type in Offered Contribution Type and Counterpart Contribution Type (respectively), cf. the relation instantiation .

4 We leave a proper treatment of the requires relation for a dedicated work.

5 For reasons of space, we omit a number of aspects of ATE. E.g. the economic offer is also based on beliefs, cf. point 1.2 and 1.3. We can easily integrate beliefs as in [14].

Fig. 2. OntoUML diagram depicting economic offerings.

[FIGURE]

## 4 ATE at Work: Generalising REA and UFO-S

We conclude by discussing the relationship between our account of the ATE, UFO-S, and REA. We start showing how REA can be retrieved by isolating a part of our OntoUML model of ATE.

In REA, economic transactions are intended as events, i.e. 'occurrences in time wherein ownership of an economic resource is transferred from one person to another person' [13]. This aspect is captured by the realisation of the economic transaction in ATE, i.e. when the commitments are fulfilled, they trigger the relevant events, cf. Fig. 3. Moreover, although REA seems to view resources (e.g. endurants) as objects of the transaction, what is brought about in economic exchanges is the transferring of ownership of an item, which is in fact an event, see [6]. This is indeed a specific type of action, which can be straightforwardly accounted by ATE. E.g., suppose that agent a is selling a bike to agent b . We can specify the relevant types of actions involved as follows: a and b both prefer the type of actions ' a transfer the ownership of the bike to b and b pays the agreed price' to the type of actions ' a does not transfer the ownership of the bike to b and b does not pay the agreed amount'. In the analysis of REA in [11], the economic agreement is captured by means of the duality relations, (e.g. transfer duality, [11], p. 16). In [11], duality relations are modeled as relators, as we do here. This enables a direct comparison with our framework: duality relators are simply a specific type of our Economic Agreement , restricted to specific types of actions, e.g. transfer of ownership. Hence, REA modeling is a submodel of our OntoUML version of ATE. Therefore, our modeling provides, on the one hand, a generalisation of REA to transactions involving any type of services and, on the other hand, an explanation of why the transaction occurs: it is based, as we have seen, on the convergent preferences of the agents and on the commitment generated by the offering steps.

Fig. 3. OntoUML diagram depicting economic exchanges.

[FIGURE]

We confront now our OntoUML model of ATE with UFO-S. As we anticipated, the mechanism of turning conditional commitment into unconditional commitments is at the core of UFO-S. There, commitments are generated by the service offering, cf. [14], as in ATE are generated by the economic offering. In this perspective, ATE provides a simple generalisation of UFO-S from service offering to any kind of economic offering. Service offering are reinterpreted, in our view, as offering about types of actions, which serves to accommodate the ontological worries about committing to possible or negative events. Moreover, ATE nicely complements the model of UFO-S by providing an explanation of why the offering is proposed in the first place and of why it can be accepted by the counterpart. The beginning of the offering is grounded in ATE on the assumptions concerning the converging preferences. So ATE complements UFO- S by providing an explanation of why the service offering is proposed and under which conditions it is accepted. In practice, we can integrate the model of UFO-S of the relator of service agreement (cf. [14], p. 181) with our model of Fig. 2.

## References

1. Almeida, J.P.A., Falbo, R.A., Guizzardi, G.: Events as entities in ontology-driven conceptual modeling. In: Laender, A.H.F., Pernici, B., Lim, E.-P., de Oliveira, J.P.M. (eds.) ER 2019. LNCS, vol. 11788, pp. 469-483. Springer, Cham (2019). https://doi.org/10.1007/978-3-030-33223-5 39
2. Blums, I., Weigand, H.: A financial reporting ontology for market, exchange, and enterprise shared information systems. In: Gordijn, J., Gu´ edria, W., Proper, H.A. (eds.) PoEM 2019. LNBIP, vol. 369, pp. 83-99. Springer, Cham (2019). https:// doi.org/10.1007/978-3-030-35151-9 6
3. Ferrario, R., Masolo, C., Porello, D.: Organisations and variable embodiments. In: Proceedings of the 10th FOIS, pp. 127-140. IOS Press (2018)
4. Fonseca, C.M., Porello, D., Guizzardi, G., Almeida, J.P.A., Guarino, N.: Relations in ontology-driven conceptual modeling. In: Laender, A.H.F., Pernici, B., Lim, E.P., de Oliveira, J.P.M. (eds.) ER 2019. LNCS, vol. 11788, pp. 28-42. Springer, Cham (2019). https://doi.org/10.1007/978-3-030-33223-5 4
5. Guarino, N., Guizzardi, G.: 'We need to discuss the relationship ': revisiting relationships as modeling constructs. In: Zdravkovic, J., Kirikova, M., Johannesson, P. (eds.) CAiSE 2015. LNCS, vol. 9097, pp. 279-294. Springer, Cham (2015). https:// doi.org/10.1007/978-3-319-19069-3 18
6. Guarino, N., Guizzardi, G., Sales, T.P.: On the ontological nature of REA core relations. In: Value Modeling and Business Ontologies (VMBO), pp. 89-98 (2018)
7. Guizzardi, G.: Ontological Foundations for Structural Conceptual Models. Telematica Instituut/CTIT (2005)
8. Guizzardi, G., et al.: Towards ontological foundations for conceptual modeling: the Unified Foundational Ontology (UFO) story. Appl. Ontol. 10 (3-4), 259-271 (2015)
9. Guizzardi, G., Fonseca, C.M., Benevides, A.B., Almeida, J.P.A., Porello, D., Sales, T.P.: Endurant types in ontology-driven conceptual modeling: towards OntoUML 2.0. In: Trujillo, J., et al. (eds.) ER 2018. LNCS, vol. 11157, pp. 136-150. Springer, Cham (2018). https://doi.org/10.1007/978-3-030-00847-5 12
10. Hodgson, G.M.: Markets. In: Durlauf, S.N., Blume, L.E. (eds.) The New Palgrave: Dictionary of Economics. LNCS, pp. 3918-3925. Palgrave Macmillan UK, London (2008). https://doi.org/10.1007/978-1-349-58802-2 1035
11. Laurier, W., Kiehn, J., Polovina, S.: REA 2: a unified formalisation of the ResourceEvent-Agent ontology. Appl. Ontol. 13 (3), 201-224 (2018)
12. Massin, O., Tieffenbach, E.: The metaphysics of economic exchanges. J. Soc. Ontol. 3 (2), 167-205 (2016)
13. McCarthy, W.: ISO 15944-4 - REA Ontology. ISO, June 2007
14. Nardi, J., et al.: A commitment-based reference ontology for services. Inf. Syst. 54 , 263-288 (2015)
15. Nardi, J., et al.: An ontology-based diagnosis of mainstream service modeling languages. In: Proceedings of the IEEE 23rd EDOC, pp. 112-121. IEEE (2019)
16. Porello, D., Bottazzi, E., Ferrario, R.: The ontology of group agency. In: Proceedings of the 8th FOIS, Rio de Janeiro, pp. 183-196. IOS Press (2014)

17. Porello, D., Guizzardi, G.: Towards an ontological modelling of preference relations. In: Ghidini, C., Magnini, B., Passerini, A., Traverso, P. (eds.) AI*IA 2018. LNCS (LNAI), vol. 11298, pp. 152-165. Springer, Cham (2018). https://doi.org/10.1007/ 978-3-030-03840-3 12
18. Porello, D., et al.: An ontological account of the action theory of economic exchanges. In: Proceedings of the 14th VMBO, vol. 2574, pp. 157-169. CEURWS.org (2020)
19. Sales, T.P., Guarino, N., Guizzardi, G., Mylopoulos, J.: An ontological analysis of value propositions. In: Proceedings of IEEE 21st EDOC, pp. 184-193. IEEE (2017)
20. Vajda, J., Merrell, E., Smith, B.: Toward an ontology of commercial exchange. In: Proceedings of the 5th JOWO, vol. 2518. CEUR-WS.org (2019)
