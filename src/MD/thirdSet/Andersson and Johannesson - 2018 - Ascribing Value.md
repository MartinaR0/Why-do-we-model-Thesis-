## Ascribing Value

Birger Andersson and Paul Johannesson

Department of Computer and Systems Sciences, Stockholm University, Sweden {ba,pajo}@dsv.su.se

Abstract. The notion of value has been thoroughly investigated in philosophy, economics, sociology and other social sciences. However, the notion of value remains highly ill-defined and elusive, as it is subjective as well as context dependent. This paper proposes an ontology for conceptualizing the notion of value ascription that is founded on an analysis of context notions, showing how value of objects can be explained in terms of value of states of affairs.

## 1 Introduction

The subject matter of this paper is that of value ascription as applied to states of affairs. More precisely, it is about the possibility to derive the value of some object from value ascribed to a state of affairs. At its core this work is related to metrology and measurement. Metrology is the science of measurement and its applications, and measurement is a 'process of experimentally obtaining one or more quantity values that can reasonably be attributed to a quantity' [5]. However, the focus of metrology and measurement is on objectivity and quantitative measures. Variations in results are explained as for instance unavoidable effects of environmental factors and labeled as measurement errors. Separating what is measured from its context so that measurements become objective and reproducible can at times be very hard, not the least when a measurement relies on psychological elements.

The goal of this paper is to conceptualize the notion of value ascription, in which an agent ascribes value to some value object. Thus, we do not attempt to define the notion of value per se, but instead explore ontological assumptions underlying value ascription independently of different value notions. The result

Valuations are subjective as they are made by a single actor, being fundamentally dependent on that actor's intentions, goals and other influencing factors. Other actors can not be assumed to reach the same valuation of the same matter, although agreements sometimes can be had. Further, valuations are context dependent in that an object being valued is always embedded in a context comprising other objects and their relations, and this context fundamentally affects the value ascribed to the object. It is even hard to think of the value of almost anything without also taking its context into account. The two seem inextricable. For example, a bottle of water is more valuable in the desert when you are thirsty than when you are at home not being thirsty, where the difference is explainable by the difference in context.

is a value ascription ontology (VAO) that includes the concepts required for representing and explaining value ascriptions. The approach is similar to that of [2], where value is ascribed to a 'relator' which is a reified relationship that can maintain identity over time [4], though the relator concept will not be as central here as in [2]. Gailly et al. proposes a core value ontology for the purpose of clarifying the semantics of value propositions [3]. While not the main focus it also touches on value ascription. Value is defined as the propositional content of a belief and relates a belief to a situation. In VAO a state of affairs and a value structure is related by means of a quale (a quale being a point in a value structure). The difference is subtle but ontologically significant.

To the farthest extent, the constructs of the propsed VAO will be related to the OntoUML ontology [1] for reasons of clarity and precision. The main envisioned benefit of the proposed ontology is that it should provide the concepts needed for representing value ascription in a generic sense. From a value analysis point of view at least two fundamental questions about valuations should be answerable: (a) if an object is kept fixed, what happens to its ascribed value when the context changes? and (b) which object out of several will be ascribed the highest value in a context? Thus, the ontology emphasizes the strong connection between a value object and its context.

## 2 The Value Ascription Ontology

## 2.1 Agents and Value Ascriptions

An agent is an endurant that can carry out actions and have intentions. Thus, not only persons are agents but also organizations and collectives, such as groups, meaning that the class Agent is stereotyped as category. An agent can play two different roles in a value ascription. First, an agent can be the one for whom a value is ascribed to a value object. Secondly, an agent can be the one who makes the value ascription, that is, the value ascription is performed by that agent. These two roles of agents in a value ascription are modelled by the associations for and by in figure 1. The agent roles introduced here correspond to the notions of value beneficiary and value beholder in the work by [7]. In some cases, the same agent can play both roles, i.e., an agent judges herself how valuable a value object is for her. But it is also possible that one agent judges the value of a value object for another agent.

A value beholder carries out a value ascription by assessing how well the qualities and dispositions of a value object fit the needs and wants of a value beneficiary. A contentious issue is whether there can exist objective value ascriptions for which noone actually makes the ascription, but instead the value ascribed is based on an objectively complete and correct computation of the fit between value object and agent. Computing such a theoretical value could in principle require an omniscient being with potentially infinite cognitive resources, meaning that in practice only approximations of the objective value may be achieved. For this reason, we have not included the possibility of objective value ascriptions in the ontology.

[FIGURE]

Fig. 1. An Ontology for Value Ascription

## 2.2 Value Objects, Value Ascriptions and Value Protocols

A value object is an object to which an agent can ascribe value. As argued in [2], in principle any object can be a value object, including physical objects, mental states, events, and actions. However, we will here take a more restricted view and consider value objects as substantials, meaning that a value object has identity and persists over time. Typical examples of value objects are goods, services and social relationships based on these, such as orders and invoices. The reason for the restriction to substantials is that we focus on use value, i.e., how value objects can be used by agents for fulfilling their needs and desires.

Through a value ascription, an agent ascribes a value to a value object, i.e., she judges how valuable the value object is for a value beneficiary. Thus, a value ascription is an event in which a value beholder ascribes value to a value object for a value beneficiary. But a value object does not have a value in any absolute sense. Instead, the value depends on properties of the agent as well as circumstances around the agent. In order to capture these, we introduce the notion of a value protocol, which consists of three components:

- -A context frame consisting of a set of contexts that specify in which circumstances a value object will be used
- -A comparison frame consisting of a set of value objects that provide a baseline for a value ascription
- -A value structure consisting of a set of value dimensions that specify which kinds of value that are to be considered in a value ascription

A value ascription is always carried out with respect to a value protocol, i.e., a value ascription needs to take into account all three components of a value protocol. In the following subsections, these three components are described in detail.

## 2.3 Contexts

Value depends on the context, or contexts, in which a value object is intended to be used. For example, a sports car may offer much status when used in the context of driving to work but much less status when used for driving on a countryside vacation. Merriam-Webster defines context as 'The interrelated conditions in which something exists or occurs' meaning that a context is always relative to something that is in focus. In the following, a context will be a context of a value object, and value is ascribed to a value object in a context. Thus, value ascription is always context dependent.

To more precisely define the notion of context, it is helpful to consider the concept of unsaturated relationships. In accordance with the conception of Frege and as discussed in [6], a distinction can be made between saturated and unsaturated relationships. A first step in clarifying this distinction is to note that a relationship symbol xRy is unsaturated in the sense that it requires the addition of two names in order to form a sentence, e.g., the expression aRb. Analogously, relationships can also be unsaturated if one or more of their relata are missing. When all of the missing relata are instantiated, the relationship becomes saturated. A context is a set of objects, some of their properties, some of their (saturated) relationships as well as a number of unsaturated relationships that involve these objects and that can be saturated by instantiating all the missing relata with one and the same value object. Intuitively, a context can be viewed as a state of affairs with a hole that leaves some relationships unsaturated (dangling). When the hole is filled by a value object, the result is a state of affairs.

In the ontology, two classes are introduced to represent value ascriptions. The class SoA Value Ascription represents value ascriptions to a single state of affairs that is made up of a value object and a context. But it can also be of interest to ascribe value to a value object across a set of contexts, as this could represent the overall value of a value object across all the contexts relevant for an agent. The class VO Value Ascription represents value ascriptions that take into account not only a single context but a context frame, consisting of a set of contexts. For example, an SoA value ascription could judge the value of a Chromebook computer in the context of viewing movies at home, while a VO value ascription could judge the value of the same Chromebook across the three contexts of viewing movies at home, giving lectures, and travelling on a conference. Reaching a final, overall value may involve weighting of SoA value ascriptions. How much weight that is assigned to each context in a context frame depends on its relative importance to the agent for which the value ascription is made. We will not delve deeper than this into theories behind the various ways a final value can be established in this paper.

Ascribing value to a value object in a context means to evaluate a state of affairs, i.e., the state of affairs that arises when the missing relata of the context are instantiated with the value object. In this sense, value ascription is fundamentally about the value of states of affairs, as this is used to define the value of value objects. It is not meaningful to ascribe value to a value object simpliciter but only to a value object in a context.

## 2.4 Value Structures

The value ascribed in a value ascription is a value quale, which can have a more or less complex structure. In the simplest case, it is just a scalar, e.g., a utilitarian value could be described by a single number, which takes into account and summarizes all the values that a value object has for an agent. This number is a value quale belonging to a value structure consisting of a single value dimension. In more complex cases, a value quale belongs to a value structure that is a multidimensional space.

The selection of the value dimensions of a value structure in a particular situation depends on the needs and desires of the value beneficiary. The value

For illustrating value quales, consider a person called Peter and a car ABC123. In a value ascription of a utilitarian value, a value quale could be the number 7 on a scale from 0 to 10, indicating that the car ABC123 is overall quite valuable for Peter.

ascribed to a value object in a context in one value dimension would then depend on how well the value object fits the corresponding need or desire in that context. Thus, value ascriptions are justified through an analysis of the fits between value objects, contexts and the needs and desires of agents.

## 2.5 Comparison Frames of Value Objects

Through a value ascription, a value, in the form of a value quale, is ascribed to a value object in a context. However, the meaning of such a value ascription is still ambiguous. As an example, suppose that a value ascription ascribes a value of high convenience to using a certain computer in the context of delivering a lecture. One interpretation of this ascription is that it means that delivering a lecture using the computer is highly convenient. However, this interpretation does not seem adequate, as delivering the lecture may be inconvenient regardless of the computer due to other factors, such as lighting, ventilation, noise, etc. The above interpretation assumes that a value can be ascribed in an absolute sense, but this is a problematic assumption, as pointed out by [8].

An alternative interpretation would be based on a relative notion instead of an absolute one, i.e., more convenient than instead of convenient . Ascribing a value of high convenience to a certain computer in the context of giving a lecture could then tentatively be interpreted as 'using this computer when giving a lecture is more convenient than giving a lecture with most other computers'. Following this interpretation, a value ascription becomes inherently comparative. It is not possible to ascribe a value to a value object in isolation; instead, value ascriptions are about comparing value objects along one or several value dimensions. As a consequence, performing a value ascription requires that in advance some set of value objects to be valuated and compared have been identified. This requirement can be addressed by introducing a comparison frame, i.e., a set of value objects that provide a baseline for a value ascription. And any value ascription is performed with respect to such a comparison frame. The choice of comparison frame will typically have a significant effect on the value ascribed by a value ascription. For example, the same computer may be ascribed a high value on convenience when compared to a set of legacy computers but a low value when compared to a set of up-to-date premium computers.

To summarize, when an agent performs an SoA value ascription, she picks a value object, a context, and a comparison frame. The value object and the context give rise to a state of affairs, call it S, and the comparison frame and the context give rise to a set of states of affairs, call them SS. The agent then compares S to SS, i.e., for each value dimension she determines how S compares to the states of affairs in SS. And based on these comparisons, she ascribes a value to the value object in the context with respect to the chosen comparison frame.

## 3 Illustration

Value ascriptions can easily be visualized in a tabular structure, see figure 2. Contained in a Value protocol are two tables - Value structure and State of affairs. The column headings in Value structure are the names of the Value dimensions, and the cells below the headings specify allowed values. In the State of affairs table, the row headings correspond to the comparison frame, i.e., the value objects under consideration, while the column headings correspond to the context frame, i.e., the contexts of interest. Each cell in the table corresponds to one value ascription.

Fig. 2. A Filled in Value Protocol

[FIGURE]

As an example for illustrating the use of the ontology, we choose the use of laptops in three different contexts. The comparison frame consists of the following three laptops: Dell XPS 13, Chromebook and Lenovo Thinkpad. The context frame includes three contexts: at home, at work, and travelling. The value structure chosen consists of two value dimensions: appropriateness and status. In this case, a column shows how an agent compares three computer models in one context. In a row, a computer model can be compared with itself in another context. For example, the value ascribed to the state of affairs of using a Chromebook at home is 〈appropriateness: 3, status: Low〉, meaning that its appropriateness is on the low side and the status value is also low. This can be contrasted with its use when travelling where it is considered to be very appropriate and to have a high status. Whether a model is better than another is determined by establishing respective overall values in a VO Value ascription and comparing them. The values assigned depend on both the value beholder and the value beneficiary, neither of which is indicated in the table.

## 4 Discussion Items

This paper proposes an ontology for value ascription. The design of the ontology reflects that value ascription is both inherently subjective and context dependent. Future research can be continued in several directions. The ontology is currently delimited to use value, but there are also other kinds of values that can be ascribed, e.g. exchange value. Thus, the ontology should be extended to accommodate those kinds of value. Another direction is to investigate the connection between a value protocol and a final value. This relationship is in part also a method question, although method is not part of the ontology. Some additional outstanding questions are:

- -Are value objects individuals or universals?
- -How are value ascriptions related to exchange value?
- -Should contexts be modelled by means of scenes and events (as suggested by [4]) or states of affairs?
- -How can value ascription inform value proposition design?

## References

1. Ontology project. http://ontology.com.br/, accessed: 2018-1-5
2. Andersson, B., Guarino, N., Johannesson, P., Livieri, B.: Towards an ontology of value ascription. In: Proceedings of the 9th International Conference on Formal Ontologies in Information Systems (FOIS 2016). vol. 283. IOS Press (2016)
3. Gailly, F., Roelens, B., Guizzardi, G.: The design of a core value ontology using ontology patterns. In: Advances in Conceptual Modeling. pp. 183-193. Lecture Notes in Computer Science, Springer (Nov 2016)
4. Guarino, N., Guizzardi, G.: Relationships and events: Towards a general theory of reification and truthmaking. In: AI*IA 2016 Advances in Artificial Intelligence. pp. 237-249. Lecture Notes in Computer Science, Springer (Nov 2016)
5. Bureau International des Poids et Mesures (BIPM): International vocabulary of metrology-Basic and general concepts and associated terms(VIM), 3rd edition. https://www.bipm.org/, accessed: 2018-1-7
6. Potter, M.: The logic of the tractatus. In: Gabbay, D.M., Woods, J. (eds.) Handbook of the History of Logic. Volume 5: From Russell to Church, pp. 255-304. North Holland (2009)
7. Sales, T.P., Guarino, N., Guizzardi, G., Mylopoulos, J.: An ontological analysis of value propositions. In: 2017 IEEE 21st International Enterprise Distributed Object Computing Conference (EDOC). pp. 184-193 (Oct 2017)
8. Schroeder, M.: Value Theory. Metaphysics Research Lab, Stanford University, fall 2016 edn. (2016)
