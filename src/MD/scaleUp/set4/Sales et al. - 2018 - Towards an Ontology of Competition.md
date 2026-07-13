## Towards an Ontology of Competition

Tiago Prince Sales 1 , 2 , Nicola Guarino 2 , Giancarlo Guizzardi 3 , and John Mylopoulos 1

1

University of Trento, Italy { tiago.princesales, john.mylopoulos } @unitn.it 2 ISTC-CNR Laboratory for Applied Ontology, Trento, Italy nicola.guarino@cnr.it 3 Free University of Bolzano-Bozen, Italy giancarlo.guizzardi@unibz.it

Abstract. It is widely recognized that accurately identifying competitors is a challenge for many companies and entrepreneurs. It is one that they cannot escape from, as failing to do so is a recipe for problems. Amongst other factors, competitor identification is challenging because of the complex nature of the competitive relationships that arise in business environments. In this paper, we tackle this issue by means of an initial ontological analysis on competition grounded in the Unified Foundational Ontology (UFO). Our analysis, the first of its kind in the literature, allows us to explain why and when competition arises, as well as to distinguish between different three types of competitive relationships, namely direct, indirect and potential competition.

Keywords:

competition, ontology, enterprise modeling

## 1 Introduction

It has been long recognized that many companies fail to accurately identify relevant competition [12], which in many cases has led to their downfall. This is true for both established companies and startups, with the latter being particularly more prone to commit such mistakes [11].

Identifying and understanding business competition is a challenging task for many reasons. Market boundaries keep changing, there is no default 'place' to look for competitors and it is not up to a company to choose their competitors. Still, the issue is that, ultimately, competition is a complex socially created concept that one needs to properly grasp to accurately identify competitors.

The pursue for theories that can explain the plurality of competitive relationships arising in business environments is not new [4,10,13]. However, no formal model has been developed to properly harmonize them, leading to conceptual confusion that, in turn, impairs the integration of existing knowledge on how to identify competitors [9]. In this paper, we move towards addressing this issue by using the Unified Foundational Ontology (UFO) [7] to conduct an ontological analysis of competition, a domain that, so far, has been neglected by business ontologies and enterprise modeling. Our main goal is to explain the nature and properties of competitive relationships, analyzing when and why they arise and who is involved in them.

We stress that it is not the aim of this paper to model the dynamics of competition. We do not want to explain how the actions of a competitor affect the actions of his/her opponents or what is the best strategy to win a competition. These questions are far better answered by models based on Game Theory (see [3] for instance). Instead, we focus on creating a model that can answer questions such as whether or not Google competes with Amazon and why.

The remainder of this paper is organized as follows. In Section 2, we discuss the general principles of competition and formalize them in a concise UFO-based model. Next, in Section 3, we leverage this analysis to explain business competition, whilst distinguishing and formalizing three different types of business competitive relationships, namely direct, indirect and potential competition. We then finalize this paper with a discussion of related work in Section 4 and some final remarks in Section 5.

## 2 On the Notion of Competition

In this paper we take the position on the nature of competition put forth by Henderson [10], which assumes that the principles of competition are universal, whether or not it refers to biological, academic or business competition. Thus, before elaborating on the ontological nature of business competition, let us first analyze competition on a more general level.

Our primary assumption on competition is that it emerges from conflicts of interest , a position in line with Deutsch's pioneering Theory of Cooperation and Competition [5]. A conflict of interest is a situation characterized by two or more goals that cannot be satisfied concurrently. Take, for example, a situation in which two applicants, John and Mary, apply for the same position in a company. It is safe to assume that each of them has the goal of getting that position. However, since there is only one position, John's and Mary's goals cannot be satisfied at the same time, for if Mary gets hired, John does not, and if John gets hired, Mary does not. Thus, John competes with Mary. In an alternative scenario, if the company was to be hiring two new employees and John and Mary were the only two applicants, there would be no conflict, as it would have been possible for both their goals to be simultaneously realized. Thus, in this second case, John and Mary would not be competing.

By using conflicts of interest to ground competition, it follows that the participants, i.e. the competitors, must always be agents. This conclusion holds if we assume that intentionality can only be ascribed to agents and not objects [8]. Note, however, that the interpretation of agents we adopt here is not limited to physical agents, such as a person, a robot, or a dog, but also includes collective (e.g. a group of people) and social agents (e.g. a company) [8]. Therefore, if competitors are always agents, statements such as 'the iPhone competes with Google Pixel' or 'the Fiat 500 is facing tough competition' cannot be inter- preted directly. In the latter case, it is Fiat, the company who produces the Fiat 500, who is facing tough competition.

Note that a conflict of interest by itself is not sufficient to characterize competition. A situation in which a single agent has two opposing goals (e.g. having a baby versus sleeping eight hours a day) characterizes a conflict of interest, but not a competition. Thus, we assume that the notion of competition is relational, i.e. for a competition to arise, at least two agents must have conflicting goals.

We emphasize that our definition of a conflict of interest is strictly objective. It does not require, to any extent, that the agents whose goals conflict are aware of the matter. For instance, in our previous John and Mary example, the conflict of interest exists regardless of whether one knows that the other has applied for the same position. Thus, if competition emerges from conflicts of interest, competition is also a matter of objective reality. By claiming that, we are not denying the cognitive process associated to perceiving competitive situations and the impact it has on a agent's actions. This phenomenon, however, is more closely associated to rivalry than competition, and therefore, we refrain from discussing it further in this paper.

The last condition for a competition to occur is the presence of mutually desired scarce resources . This concept is deeply entrenched in the theories of competition put forth in Biology [1], arguably the field in which the nature of this concept has been investigated the most. In Biology, resources are things animals need in order to survive, such as food, water or territory. In general, resources are objects an agent needs to achieve his/her goal, such as a textbook needed by a student to study and pass an exam. Note however that resources must be both scarce and mutually desired to give rise to competition. Scarcity is required because if there were enough resources for everyone, there would be no conflict of interest, and thus, no competition. To understand why competition requires mutually desired resources, consider the following example. Dylan wants to date Hailey, but Hailey's mother, Claire, is against it. There is a clear conflict of interest between Dylan and Claire, and a scarce resource, Hailey's boyfriend position. Still we would not say that Claire and Dylan compete. Instead, if both Dylan and Andy wanted to date Hailey, there would be a conflict of interest over a mutually desired scarce resource, and thus, a competition.

The definition of what is the mutually desired resources in a competitive scenario might vary w.r.t. the level of abstraction. In the simplest case, agents compete for a single identified resource, such as two companies competing for a particular customer. In a more complex case, rivals may compete for resources of a given type or group, regardless of the identity of each particular resource. Such a case is exemplified by the competition between Google and Apple for customers in the smartphone segment. It is not the case that either Apple or Google want to acquire a particular customer, such as me or you; instead, they want to acquire as many customers as possible from the smartphone market.

We formalize the aforementioned concepts and relations necessary to explain competition in the model depicted by Fig. 1. This model leverages two concepts from UFO-C (an ontology of social entities [8]), namely Agent and Intention .

An agent, in UFO-C, is defined as a individual who bears intentional moments (beliefs, desires and intentions) and is able to perform actions. An intention is defined as a commitment to bring about a desired state of affairs. Intentions might conflict with one another if they cannot be satisfied at the same time.

In the domain of competition, we are concerned with a particular type of intention, namely those that are about acquiring or keeping control (or ownership, possession...) of resources. We label these as Resource Demand and represent them as being externally dependent on ( ext. dep. on ) a Resource . Demands for resources have a particular quality inhering in them, labeled as quantity and that accounts for how many resources an agent is seeking (e.g. a company who wants to hire fi ve developers). Resources, instead are characterized by another quality, availability , which refers to how many of it are available (e.g. three positions available in a company). Notice that we use the term resource in a very broad sense, being the generalization of Single Resource , Resource Type , and Resource Stock . The first refers to particular individuals, the second refers to types of individuals (e.g. fast food customers), and the third to a collection of individuals (e.g. the collection of fast food customers in Italy). Note that the availability of single resources is naturally always one, as it is the quantity of a resource demand to control them.

Fig. 1. A preliminary OntoUML model of competition. 4

[FIGURE]

The sum of demands for a common resource gives rise to a relationship we name Collective Demand 5 . This is an extrinsic and descriptive relationship [6] that involves at least two agents and a common resource. It is a descriptive relation because it holds in virtue of some individual aspects (modes) of its relata, namely the agents' resource demands. Moreover, since these demands are externally dependent on resources, the relationship is extrinsic. A collective demand relationship is characterized by two derived qualities, collectiveQuantity and competitiveness . The former equals to the sum of the individual demand for resources that form the relationship, whilst the latter equals to the ratio between the former and the availability of the common resource involved in the relationship.

4 We adopt the following color coding in this paper: substantials are represented in pink, relators in green, intrinsic aspects in blue, and the remainder in gray

5 A reader who is familiar with UFO should note that we assume here the revised theory of relationship reification, which allows relators to be composed of moments in general, not only qua-individuals. For details, the reader should refer to [6].

A collective demand relationship becomes a Competition whenever the resource demands that form cannot be concurrently satisfied. Practically, this occurs whenever the availability of a resource is lower than the collective demand for it, which makes the resource scarce and the agents who seek it competitors. From the competition relationship, we derive the competes-with relation that holds between competitors. This relation is irreflexive, symmetric and nontransitive. It is irreflexive because we excluded the possibility of one competing with oneself. It is symmetric because if John demands the same resource as Mary, the converse claim follows. Lastly, it is non-transitive because agents might be engaged in multiple competition relationships for different resources at the same time. For instance, Facebook competes with Google for online advertising customers, and Google competes with Spotify for music streaming customers, still Facebook does not compete with Spotify.

## 3 Analyzing Business Competition

Companies compete for various reasons. Some seek to develop the best products, others to offer them at the lowest price. Still, what companies ultimately compete for are customers - the scarce 'resource' they need to survive. Naturally, customers do not form a single big collection of similar resources. The customers a milk company pursues are definitely not the same as those pursued by a high-end fashion brand, even if some individual customers buy from them both. Then, how does a firm identify its competitors?

It is accepted in the literature that any two given companies compete if they offer products or services that fulfill the same customer needs [13]. But how does that connect to the principles of competition we discussed in the previous section? We argue that by aiming at fulfilling a particular customer need, a company is making a value proposition towards a group of customers [16]. By doing so, it is straightforward to assume that such a company seeks to acquire customers from this group. Any other company making a value proposition to those same customers would also want to acquire them, which would give rise to a conflict of interest over a scarce resource, and thus, competition.

This pursue for the very same group of customers, known as market-level competition, is a basic competitive relationship that arises in business environments. In the following subsections we discuss two other types of relevant relationships, namely indirect and potential competition.

## 3.1 Direct and Indirect Competition

None would dispute that McDonald's competes with Burger King, as both companies are fast-food chains specialized in hamburgers. It is also reasonable to claim that McDonald's competes with Subway and Pizza Hut, as they all offer low-priced quick meals, even if of different types. But what about local bakeries and deli shops? We might still consider them as competitors, but somehow they seem to be less of a competition than the former examples.

Fig. 2. A model fragment on market competition.

[FIGURE]

The intuition that some companies are more competitors than others can be explained by the notion of market-level competition, which relies on the similarity of customers needs. If we define, for instance, a customer need as 'eating a hamburger', we would identify only McDonald's and Burger King as competitors. Instead, if we define it as 'eating a fast and cheap meal' we would identify all fast-food companies as competitors, but also all bakeries, kebabs and deli shops. If we were to define the need simply as 'eating', virtually all companies in the food industry would be identified, from those selling frozen pizzas to high-scale sushi restaurants.

This variation exists because customer needs are ultimately goals, which can be defined at multiple levels of abstraction and organized in means-end hierarchies (i.e. a goal can be the means of achieving another goal). On one hand, companies that fulfill the same low-level goal are referred to as direct competitors , such as McDonald's and Burger King, who satisfy the 'eating a hamburger' need, and Netflix and Amazon, who satisfy the need of 'watching movies online'. On the other hand, companies that satisfy the same high-level goal, but by means of different low level goals, are termed to be indirect competitors - and their respective products as substitutes. This is the case for McDonald's and local bakeries, as well as for Netflix and broadcasting companies (e.g. BBC, FOX).

We represent market-level competition, in its direct and indirect form, in the model of Fig. 2. As in any form of competition, market competition is a descriptive extrinsic relationship. In this case, it is composed by the intention of competitors to acquire customers of the same market segment. Such intentions can be identified by the value propositions competitors make towards a market segment. Market segments are identified by specific descriptions of customer needs, and the part-whole relation between them captures the varying level of abstraction at which customer needs can be defined. A market A is part of a market B if the customer need that defines A is a means to achieve the need that defines B .

## 3.2 Potential Competition

Another relevant type of competitive relationship is potential competition [13]. Differently from the previous relationships we just discussed, potential competition does not refer to an existing pursue of conflicting goals. Instead, it identifies companies who are likely to become competitors in the future, a very important piece of information for strategists. But if there is no current conflict of interest, what grounds such relationships? The answer is capability equivalence [13].

Capabilities are intrinsic dispositional properties of agents that endow them with the power of exhibiting some behavior or bringing about certain effects in the world [2]. Examples include the Netflix's capability of streaming videos to a large number of users worldwide, as well as Amazon's logistics capability of delivering products one day after orders. Capability equivalence, then, refers to a relation between capabilities of different agents that enable them to achieve similar enough outcomes.

Still, potential competition does not arise just because of capability equivalence. A focal firm identifies potential competitors by: (i) singling out which of its capabilities are necessary for delivering its value proposition for a given market; and (ii) identifying which other firms have equivalent capabilities (i.e. which other firms could deliver similar value propositions) but that currently do not compete with them in the chosen market. Thus, potential competition is also an extrinsic descriptive relationship [6], but one that is grounded on the sum of its relata's equivalent capabilities (see Fig. 3).

Fig. 3. A model fragment on potential competition.

[FIGURE]

## 4 Related Work

To the best of our knowledge, no in depth ontological account of competition has been proposed in the literature, despite its clear relevance in strategic analysis. Thus, in this section, we compare our initial analysis with enterprise and business modeling contributions that use the concept of competition (or competitor).

One of such contributions is c3value [18], an extension of e3value designed to support competition, customer and capability analysis. Although the authors do not explicitly define the concepts of competition and competitor, the underlying intuition is that the competitors of a company are those who aim at solving the same customer needs (in their words, those who offer the same primary value object). Competitors can also be classified according to the secondary values they offer (e.g. convenience, reliability). This allows companies to identify their competitors and represent how they distinguish themselves from the competition. In c3value's account of competition, one can represent direct and indirect competition between multiple companies.

Another extension of e3value that is related to this research is the e3forces model [14]. In this extension, the authors leverage on Porter's five-forces framework [15], a well-known strategic tool to analyze the competitiveness of industries, to describe how environmental factors impact a business value model. Three of such forces regard competitive relationships in the sense we have used in this paper, namely the rivalry between competitors, the threat of substitution, and the threat of new entrants. The first two refer to direct and indirect competition respectively, whilst the third refers to potential competition. Although e3forces accounts for the same three relationships we discuss in this paper, it does not provide a precise characterization of why they hold and how to systematically identify them, relying solely on the intuitions put forth by Porter.

A third related work is the Enterprise Ontology (EO) [17], a broad ontology about enterprises that marginally touches the notion of competition. EO defines a competitor as 'a role of a vendor in a relationship with another vendor whereby one offers one or more products for sale that could limit the sales of one or more products of the other vendor' . With this definition, however, EO only describes binary direct competition, which, as we discussed in Section 3, is just one type of business competitive relationships.

## 5 Final Remarks

In this paper we presented an initial ontological analysis of competition in general, and of business competition in particular. We explained the nature of competition by means of conflicts of interest and scarce resources, and distinguished three relevant types of business competitive relationships, namely direct, indirect and potential competition. We believe this paper clarifies the notion of competition, which can serve as a basis for future business ontologies.

As a next direction, we plan to extend the presented ontology to account for multi-market competition, as it is rarely the case that companies compete in a single market. Such an account is necessary in order to explain the asymmetric competition [4] and competitor relevance. We are also aware that that most real scenarios are not exclusively competitive, but a mix of competition and cooperation. We see these relations as two ends of the same spectrum, and therefore, we plan to examine cooperation and the future. Ultimately, our goal is to incorporate the competition ontology to the value proposition ontology we have previously developed [16], in order to design a modeling framework that allows for the competitive analysis of value propositions.

## References

1. Alley, T.R.: Competition theory, evolution, and the concept of an ecological niche. Acta Biotheoretica 31(3), 165-179 (1982)
2. Azevedo, C.L., Iacob, M.E., Almeida, J.P.A., van Sinderen, M., Pires, L.F., Guizzardi, G.: Modeling resources and capabilities in enterprise architecture. Information Systems 54, 235-262 (2015)
3. Bonau, S.: A case for behavioural game theory. Journal of Game Theory 6(1) (2017)
4. DeSarbo, W.S., Grewal, R., Wind, J.: Who competes with whom? a demandbased perspective for identifying and representing asymmetric competition. Strategic Management Journal 27(2), 101-129 (2006)
5. Deutsch, M.: Cooperation, competition, and conflict. In: Morton Deutsch: A Pioneer in Developing Peace Psychology, pp. 47-70. Springer (2015)
6. Guarino, N., Guizzardi, G.: Relationships and events: towards a general theory of reification and truthmaking. In: AI*IA 2016 Advances in Artificial Intelligence, pp. 237-249. Springer (2016)
7. Guizzardi, G.: Ontological foundations for structural conceptual models (2005)
8. Guizzardi, G., Falbo, R., Guizzardi, R.S.S.: Grounding software domain ontologies in the Unified Foundational Ontology (UFO). In: 1th Iberoamerican Workshop on Requirements Engineering and Software Environments (2008)
9. Gur, F.A., Greckhamer, T.: Know thy enemy: A review and agenda for research on competitor identification. Journal of Management (2018)
10. Henderson, B.D.: The anatomy of competition. The Journal of Marketing pp. 7-11 (1983)
11. Krzy˙ zanowska, M., Tkaczyk, J.: Identifying competitors: challenges for start-up firms. International Journal of Management Cases 15(4), 234-247 (2013)
12. Levitt, T.: Marketing myopia. Harvard business review 38(4), 24-47 (1960)
13. Peteraf, M.A., Bergen, M.E.: Scanning dynamic competitive landscapes: a marketbased and resource-based framework. Strategic management journal 24(10), 10271041 (2003)
14. Pijpers, V., Gordijn, J.: e3forces: understanding strategies of networked e3value constellations by analyzing environmental forces. In: International Conference on Advanced Information Systems Engineering. pp. 188-202. Springer (2007)
15. Porter, M.E.: Competitive strategy: Techniques for analyzing industries and competitors. Simon and Schuster (2008)
16. Sales, T.P., Guarino, N., Guizzardi, G., Mylopoulos, J.: An ontological analysis of value propositions. In: 21st International Enterprise Distributed Object Computing Conference (EDOC). pp. 184-193. IEEE (2017)
17. Uschold, M., King, M., Moralee, S., Zorgios, Y.: The Enterprise Ontology. The Knowledge Engineering Review 13(1), 31-89 (1998)
18. Weigand, H., Johannesson, P., Andersson, B., Bergholtz, M., Edirisuriya, A., Ilayperuma, T.: Strategic analysis using value modeling-the c3-value approach. In: 40th Annual Hawaii International Conference on System Sciences (HICSS 2007). pp. 175c-175c. IEEE (2007)
