[FIGURE]

## Modeling the Emergence of Value and Risk in Game Theoretical Approaches

Glenda Amaral 1( B ) , Daniele Porello 2 , Tiago Prince Sales 1 , 1

1

and Giancarlo Guizzardi

Conceptual and Cognitive Modeling Research Group (CORE), Free University of Bozen-Bolzano, Bolzano, Italy {gmouraamaral,tiago.princesales,giancarlo.guizzardi}@unibz.it 2 ISTC-CNR Laboratory for Applied Ontology, Trento, Italy daniele.porello@loa.istc.cnr.it

Abstract. Game theory is largely about interactions of agents whose decisions affect each other. The combination of agents' actions corresponds to outcomes, which may impact agents' goals, either positively or negatively. The analysis of the probable consequences and expected utilities of all possible outcomes is fundamental to support agents when deciding whether to engage in a certain strategy. In this paper, we move in this direction by initiating the investigation of the ontological foundation of the emergence of value and risk from outcomes in game theoretical approaches. In order to understand the influence of these forces over outcomes, a precise and rigorous conceptualization, based on foundational ontologies, is needed. To this aim, we present and discuss here a preliminary ontological modeling of basic concepts of game theory, as well as the relation to value, risk and outcomes.

Keywords: Game theory · Value · Risk · Unified Foundational Ontology (UFO) · Enterprise Architecture · Archimate

## 1 Introduction

Game theory has become an important field of study and has been employed by practitioners of different disciplines, including economics, management, political science, biology, law, among others. In general, 'game theory is concerned with situations in which decision-makers interact with one another, and in which the satisfaction of each participant with the outcome depends not just or her own decisions but on the decisions made by everyone' [6]. Game-theoretic analysis include the modeling of the possible results of each strategy chosen by the players, taking into account uncertainties that neither player directly controls but that may influence outcomes, and assessing the expected utilities of these possible results. If we take the notion of risk presented in the ISO 3100:2018 [18,19] standard, which defines risk as the 'effect of uncertainty on objective', we can conclude that an important part of choosing a strategy is understanding the risks involved in this decision.

Game outcomes may have either a positive or a negative effect on players' welfare, which are traditionally modeled in game theory by means of the Expected Utility Theory, cf [24].

As we shall see, in our account the positive and negative results shall be construed by means of the concepts of 'value' and 'risk', respectively; this move is motivated by the intent to provide a semantically transparent and interoperable qualitative account of the abstract quantitative theory of utilities. Thus, players must weight value and risks against each other when deciding whether to engage in a certain strategy. From this perspective, traditional risk analysis may help to advance the current state of the art of practical applications of game theory by modeling and assessing probable consequences for each outcome, thus allowing for understanding how value and risk emerge from combinations of actions of players.

Research into the foundations and the proper applications of game theory to real world scenarios has evolved at a vigorous pace throughout the past century, cf. [24] and nowadays the theoretical analysis provided by game theory is nicely complemented by advanced sets of computational tools, cf. [23,36]. Over the past years 'mathematicians and economists enriched the foundation, gradually building one of the most powerful and influential toolboxes of modern social science' [41].

Although the formalization of game components is quite well established, a detailed ontological understanding of the fundamental notions of game theory is missing. In particular, a clear ontological foundation of the objectives, or goals, of the interacting agents and of the emergence of value and risk from the outcomes of interaction is still to be developed. Without a precise conceptualization and rigorous definition of fundamental game theory notions, modeling and communication problems may arise. For example, when various modelers share a model without a clear semantics, different modelers come to different interpretations of the same model and are not aware of the conflict, running into a False Agreement problem [9]. As a result, practitioners have to make their own interpretations about the key concepts proposed in such models, which may lead to incorrect usage, and subsequently, them not obtaining the expected results [20]. This problem can manifest itself, for example, in the modeling of Enterprise Architectures. A main challenge of incorporating the fundamental notions of game theory in enterprise architecture lies in identifying a precise conceptualization for these notions. Without such a precise conceptualization, different modelers may come to different interpretations of the same model, thus resulting in enterprise architecture models that cannot serve their purpose as tools for communication between stakeholders, decreasing the value of enterprise architecture models in the pursuit of informed decision-making.

In this paper, we intend to contribute to filling these gaps by initiating the investigation of the ontological foundation of the emergence of value and risk in game theoretical approaches. We believe that a proper ontological understanding and modeling of the basic notions of game theory is mandatory to apply this rich body of knowledge and computational tools in designing information systems and supporting strategic decision making.

The contribution of this paper is threefold. Firstly, we make use of the concepts and relations defined in the Common Ontology of ValuE and Risk (COVER) [33] (Sect. 3.2) - a novel well-founded reference ontology that explains value and risk as dual and intrinsically connected notions -to analyse the payoffs of a game in terms of value and risk, as well as how they emerge from outcomes in game theory. Secondly, we propose a precise representation of our analysis by means of an ontologically well-founded model, specified in OntoUML [12] and thus, compliant with the meta-ontological commitments of the Unified Foundational Ontology (UFO) [12]. Finally, we apply our ontological account for game theory concepts to model game outcomes in the context of Enterprise Architectures.

The remainder of this paper is organized as follows. In Sect. 2, we provide an overview of some basic concepts of game theory and a discussion on the emergence of value and risk from outcomes. In Sect. 3, we briefly introduce the Unified Foundational Ontology (UFO), as well as the Common Ontology of ValuE and Risk (COVER) [33], which serve as conceptual foundation for the analysis conducted in this paper. In this section, we also present a number of modeling patterns based on COVER that support the modeling of value and risk in the standard enterprise architecture language Archimate. In Sect. 4, we represent the results of our analysis in a concise OntoUML model. In Sect. 5, we instantiate the model using a Bank Run game example. To demonstrate the contribution of our proposal to the modeling practice, in Sect. 6, we apply these results to represent the emergence of value and risk from game outcomes in enterprise architecture models in Archimate. We conclude with some final remarks in Sect. 7.

## 2 On Game Theory

## 2.1 Strategic Games

'Game Theory studies decisions in which the outcome depends partly on what other people do, and in which this is known to be the case by each decision maker' [27]. Shoam and Leyton-Brown [37] define game theory as 'the mathematical study of interaction among independent, self-interested agents.'

In game theory, a game is intended to refer to any social situation involving two or more agents, named players. A player may be interpreted as an individual or as a group of individuals making a decision. Two basic assumptions about players are that: (i) they are rational [24], meaning that they make decisions consistently in pursuit of their own objectives and aiming at maximizing the expected value of their payoff; and (ii) they take into account their knowledge or expectations of other decision-makers' behavior [37]. According to Shoam and Leyton-Brown [37], each player 'has his own description of which states of the world he likes' and 'acts in an attempt to bring about these states of the world'.

The dominant approach to modeling an agent's interests is Utility Theory, which aims at quantifying an agent's degree of preference across a set of available alternatives [37]. Under a wide range of circumstances, the preference relation of a player in a strategic game can be represented by a utility function (also called a payoff function) [25]. A utility function is a mapping from states of the world to real numbers. These numbers are interpreted as measures of an agent's level of happiness in the given states.

A strategic game is a model of interactive decision-making in which players (agents) simultaneously choose their plan of action to perform in the environment. The combination of each agent action (the action profile , in the gametheoretical jargon) brings about a possible outcome o in a set of outcomes O , that depends on the actions performed by the agents, cf. [42]. We can represent an agent utility function as a function from O to the real numbers R ( u : O → R ) that assigns to each outcome o in O a measure of how good o is for the considered agent. The greater the number, the better o is for that agent.

Based on the above-mentioned definitions, a (strategic) game includes (cf. [42]): a finite set N of n agents, indexed by i ; for each agent i ∈ N , a nonempty set A i of actions (or strategies) available to agent i ; a set of outcomes O ; the preferences or utilities u i of the agents over the combinations of actions (outcomes). In Game Theory, to simplify the model, the set of outcomes is usually identified with the set of all possible combinations of agents' actions; however, we prefer to keep the two sets distinct, as in [42], to facilitate our subsequent ontological analysis.

Let us take as example a set of agents N = { x, y } and a set of actions A = { C,D } available to both agents x and y . Assume that each combination of agents' actions brings about a distinct outcome, i.e. we have the following set O = { o 1 , o 2 , o 3 , o 4 } , where o 1 = ( C,C ) , o 2 = ( C,D ) , o 3 = ( D,C ) and o 4 = ( D,D ) . In addition, for each agent, we can define the preferences or utilities directly on the combinations of actions (or outcomes). For instance:

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

A natural way to represent games is via an n -dimensional matrix, also known as payoff matrix . For example, in a two-dimensional matrix, in general, each row corresponds to a possible action for player x , each column corresponds to a possible action for player y , and each cell is a combination of actions that corresponds to one possible outcome. Each player's utility for an outcome is written in the cell corresponding to that outcome, with player x 's utility listed first. Table 1 illustrates the payoff matrix for the example just mentioned.

Table 1. Payoff matrix example

|          | Player y   | Player y   |
|----------|------------|------------|
|          | C          | D          |
| Player x | C 2,2      | 2,1        |
|          | D 1,3      | 3,2        |

A fundamental concept in game theory is that of Nash equilibrium. A Nash equilibrium is a set of actions (an action profile), one for each player (agent), such that no player could improve their payoff by unilaterally deviating from their assigned action. For example, considering two agents x and y , two actions a 1 and a 2 are in Nash equilibrium if: (i) assuming that agent x plays a 1 , y can do no better than playing a 2 ; and (ii) assuming that agent y plays a 2 , x can do no better than playing a 1 . The game presented in Table 1 has a unique Nash equilibrium, namely ( C,C ) .

## 2.2 Example: Bank Run

The game theoretical literature on bank runs is largely built on the seminal paper by Diamond and Dybvig [5].

A bank holds only a fraction of its deposits as cash reserves. It lends out as much of its deposits as it can (subject to a banking regulator's capital-adequacy requirements), making a profit from the interest it charges. A bank run occurs when a large number of customers of a bank or another financial institution withdraw their deposits simultaneously due to concerns about the bank's solvency, which is common in times of crisis. If the depositors do not withdraw and give bank enough time to tide over crisis, then payoff is highest and they can get their money with interest. However, if there is panic among depositors and all of them rush to withdraw their money, then due to insolvency each will end up getting a lesser amount. Finally, if few withdraws and the others do not, then the one who withdraws gets more than the one who do not withdraw.

To simplify, let us consider the example of a bank with just two depositors. Each depositor makes a deposit of 1000 euros in the bank. The bank invests these deposits in a long term project. If the bank is forced to liquidate its investments before the project matures, a total of 1600 euros can be recovered. However, if the bank allows the investment to reach maturity, the project will pay out a total of 2400 euros. Therefore, if both depositors make withdrawals before the project matures, each agent will receive 800 euros. If only one depositor withdrawal her money before the project matures, she receives 1000 euros and the other one, 600 euros. Finally, if both depositors retain the payment until the project matures, the bank returns 1200 euros for each one. Table 2 presents the payoffmatrix for this example, considering that the depositors may only choose between withdrawing their deposits before the project matures or retaining their deposits until it matures. Note that although in this example the payoffs are related to the value returned to depositors by the bank, payoffs are not necessarily the same as monetary worth. This is because payoffs or utilities identify the players' preferences, which are not necessarily measured in terms of profit or money, cf. [27].

This game has two Nash equilibria: (i) both depositors withdraw; and (ii) both depositors retain. The first of these two outcomes (i) can be interpreted as a run on the bank. If depositor A believes that depositor B will withdraw before the project matures, then her best response is to withdraw as well, even though both depositors would be better off if they waited until the project matures.

Table 2. Bank Run example

|             |          | Depositor B   | Depositor B   |
|-------------|----------|---------------|---------------|
|             |          | Withdraw      | Retain        |
| Depositor A | Withdraw | 800,800       | 1000,600      |
| Depositor A | Retain   | 600,1000      | 1200,1200     |

Recently, some authors have compared the shortage of toilet paper, associated to the spread of coronavirus, to a bank run [26]. They state that 'this panic buying is the result of the fear of missing out and is a phenomenon of consumer behaviour similar to what happens when there is a run on banks' [26]. According to Payolo [26], 'both banking and the toilet-paper market can be thought of as a coordination game with two players (one individual and everyone else) and two strategies (panic buy or act normally). Each strategy has an associated pay-off. If everyone acts normally, we have an equilibrium: there will be toilet paper on the shop shelves, and people can relax and buy it as they need it. But if others panic buy, the optimal strategy for the individual is to do the same, otherwise she'll be left without toilet paper. The result is another equilibrium, which is everyone panic buys'.

## 2.3 Value, Risk and Outcomes

According to Sun and Sun [38], 'game theory is mainly about choosing the most advantageous plan of action given the effect the opponent has on us'. Agents perform actions motivated by intentions, which are related to their goals. In game theory, an outcome corresponds to a combination of actions performed by agents. Payoffs are related to outcomes results, which can contribute to the achievement of agents' goals. Sun and Sun [38] state that payoff 'refers to the reward received after the player has chosen a certain strategy or action'.

As extensively discussed in the literature [21,22,33], value is directly connected to the achievement of goals. Things and experiences have value to people because they allow them to achieve their goals. For example, an object has value to an agent because it has properties (e.g., capacities, 'affordances', i.e., ultimately, dispositions ) that can be leveraged to enact events that, in turn, bring about situations that contribute to satisfy that agent's goals [2,16]. In summary, the more an event makes progress towards achieving an agent's goals (i.e., the more the situation it brings about contributes to satisfying those goals), the more valuable it is to that agent. In other words, the results of outcomes, represented by payoffs, may create value for agents as they can positively impact their goals. But, as value is not an intrinsic property , the same object or experience may have different values to different agents, or even according to different goals adopted by the same agent. Thus, since the players have different goals and under different circumstances, they may feel differently w.r.t. the same reward. For example, a mask has a higher value during the COVID-19 pandemic because by wearing it, one is better protected from getting infected.

Interestingly, at the same time that outcome results can generate value, they also entails some risk, as they can negatively impact an agent's goal. The relation between value and risk is pointed out by several works in the literature. According to Sales et al. [33], 'the notion of risk is irreducibly intertwined with the notion of value' and one of the differences between them rely on 'the expected impact on goals: negative for risks and positive for value'.

Having a clear understanding of the influence of these forces over outcomes is fundamental to the agent's decision making. For example, 'in an uncertain game, a rational agent would not always play the strategy that gives the highest expected payoff if the risk is too high. For a risk-averse agent, the strategy that takes the least risk has the highest dominance. For a risk-seeking agent, the strategy that may give the highest payoff has the highest dominance regardless of the risk and the expected payoff. For a risk-neutral agent, the dominant strategy is the one that gives the highest expected payoff' [8]. Risk analysis, including probabilistic risk assessment of how events may unfold, can be very useful (perhaps even essential) for realistically complex problems, in populating the cells in payoff matrices. Therefore, as stated by Cox [4], 'risk analysis and game theory are also deeply complementary'. Game-theoretic analyses require modeling the probable consequences of each choice of strategies by the players and assessing the expected utilities of these probable consequences. Decision and risk analysis methods are well suited to accomplish these tasks.

## 3 Ontology-Based Foundations

Our aim is to provide a first ontological analysis of the emergence of value and risk from game outcomes. Our analysis is grounded in the Unified Foundational Ontology (UFO) [12], which was created with the specific purpose of providing foundations for conceptual modeling. UFO is formally connected to a set of engineering tools including a modeling language (OntoUML), as well as a number of methodological (e.g., patterns, anti-patterns) and computational tools [15]. Research shows that UFO is among the most used foundational ontologies in conceptual modeling and the one with the fastest adoption rate [40]. In particular, we rely on the concepts and relations defined in the Common Ontology of ValuE and Risk (COVER) [33], a novel well-founded reference ontology grounded on UFO that explains value and risk as dual and intrinsically connected notions. In this section we briefly discuss these ontological foundations.

## 3.1 The Unified Foundational Ontology

The Unified Foundational Ontology (UFO) is an axiomatic, domain independent, formal theory, developed based on a number of theories from Formal Ontology, Philosophical Logics, Philosophy of Language, Linguistics and Cognitive Psychology. UFO is divided into three incrementally layered compliance sets: UFO-A, an ontology of endurants (objects) [12], UFO-B, an ontology of events (perdurants) [16], and UFO-C, an ontology of social entities built on the top of UFO-A and UFO-B, which addresses terms related to the spheres of intentional and social things [13,17]. For an in-depth discussion and formalization, one should refer to, for example, [2,7,12,14].

UFO is the theoretical basis of OntoUML, a language for Ontology-driven Conceptual Modeling that has been successfully employed in a number of academic and industrial projects in several domains, such as services, value, petroleum and gas, media asset management, telecommunications, and government [15]. Models created in OntoUML have a clear formal semantics, and a comprehensive support for model verification, validation and code generation, including versions in languages such as OWL [15]. In the sequel, we briefly explain a selected subset of ontological distinctions put forth by the Unified Foundational Ontology, which are relevant to our discussion.

UFO makes a fundamental distinction between individuals (particulars), and types (or universals), i.e., patterns of features that are repeatable across individuals. Individuals can be endurants (roughly, things or object-like entities) and perdurants (roughly, events, occurrences, processes). Within the category of endurants, UFO distinguishes substantials and aspects (or moments). Substantials are existentially independent objects, such as Mick Jagger, the Moon, the United Nations organization. Moments, in contrast, are existentially dependent individuals, such as (a) Mary's capacity to speak italian (which depends on her) and (b) the marriage between John and Mary (which depends on both John and Mary). Moments of type (a) are termed modes; those of type (b) are termed relators. Relators are individuals with the power of connecting entities. For example, an 'enrollment' relator connects an individual playing the 'student' role with an 'educational institution'. Furthermore, there is a third sort of moments termed qualities. Qualities are individual moments that can be mapped to some quality space, e.g., a flower's color which may change from red to brown while maintaining its identity and a person's weight, which can be mapped to a one-dimensional structure of positive real numbers.

The metamodel of the OntoUML language was designed to reflect the ontological distinctions put forth by UFO. For this reason, the distinctions of the latter are reflected as modeling primitives (mostly stereotyped classes and relations) of the former. In OntoUML, the stereotypes «phase», «role» and «roleMixin» represent the respective ontological types of anti-rigid universals (which contingently instantiate their instances): phases are anti-rigid universals with an associated intrinsic contingent instantiation condition (e.g., being a child is being a person who contingently is in a certain age range); roles are anti-rigid universals with an associated relation contingent instantiation condition (e.g., being a student is being a person who contingently participates in a enrollment relation with an educational institution); rolemixins are anti-rigid and relationally dependent universals that aggregate properties that are common to different roles (e.g., the type customer that aggregates properties of individual customers and corporate customers). Furthermore, the stereotype «mixin» is used to represent semi-rigid universals (which are necessarily instantiated by some of its instances and contingently instantiated by others). Finally, the stereotype «category» is used to represent rigid universals (which necessarily instantiate their instances such as physical object, which aggregates essential properties of tables, cars, books). The reader interested in more details on the modeling primitives of OntoUML is referred to [1,7,14].

## 3.2 The Common Ontology of ValuE and Risk (COVER)

In this section, we briefly present the Common Ontology of ValuE and Risk (COVER) [33], a well-founded ontology that makes the deep connections between the concepts of value and risk explicit. COVER is grounded on several theories from marketing, service science, strategy and risk management. It is specified in OntoUML in [12].

COVER proposes an ontological analysis of notions such as Value, Risk, Risk Event (Threat Event, Loss Event) and Vulnerability, among others. This ontology characterizes and integrates different perspectives of value and risk.

COVER makes the following ontological commitments on the nature of value:

- -Value emerges from impacts on goals. Value emerges from events that affect the degree of satisfaction of one or more goals of an agent.
- -Value is relative. The same object or experience may be valuable to a person and of no value to another.
- -Value is experiential. Even though value can be ascribed to objects, it is ultimately grounded on experiences. For instance, in order to explain the value of a smartphone, one must refer to the experiences enabled by it.
- -Value is contextual. The value of an object can vary depending on the context in which it is used.

As for risk, COVER makes the following ontological commitments:

- -Risk is relative. This means that an event might be simultaneously considered as a risk by one agent and not as a risk by another (it may even be considered as an opportunity by such an agent).
- -A risk is perceived according to its impact on goals, i.e. in order to talk about risk, one needs to account for which goals are 'at stake'.
- -Risk is experiential. This means that we ultimately ascribe risk to events, not objects.
- -Risk is contextual. Thus, the risk an object is exposed to may vary even if all its intrinsic properties (e.g. its vulnerabilities) are the same.
- -Risk is grounded on uncertainty about events and their outcomes.

Given the objectives of this paper, we focus here on the perspective of value and risk as a chain of events that impacts an agent's goals, which the authors named Value Experience and Risk Experience, respectively.

COVER breaks down Value Experiences into 'smaller' events, dubbed Value Events. These are classified into Impact and Trigger Events. The former are those that directly impact a goal or bring about a situation (named Impactful Outcome) that impacts a goal. On contrast, Trigger Events are simply parts of an experience that are identified as causing Impact Events, directly or indirectly. To formalize goals, COVER reuses the concept of Intention from UFO [12], as a type of mental state that describes a class of state-of-affairs that an agent is committed to bring about. Note that, since agents in UFO's view include both physical and social agents, COVER is able to represent value being ascribed from the perspective of a customer and an employee, but also from that of a business unit or even a whole enterprise.

Risk Experiences focus on unwanted events that have the potential of causing losses and are composed by events of two types, namely threat and loss events. A Threat Event is the one with the potential of causing a loss, which might be intentional or unintentional. A Threat Event might be the manifestation of: (i) a Vulnerability (a special type of disposition whose manifestation constitutes a loss or can potentially cause a loss from the perspective of a stakeholder); or (ii) a Threatening Capability (capabilities are usually perceived as beneficial, as they enable the manifestation of events desired by an agent. However, when the manifestation of a capability enables undesired events that threaten agent's abilities to achieve a goal, it can be seen as a threatening capability). The second mandatory component of a Risk Experience is a Loss Event, which necessarily impact intentions in a negative way (captured by a Hurts relation between Loss Event and Intention).

Figures 1 and 2 depicts two COVER diagrams in OntoUML, which captures part of the aforementioned ontological notions.

Fig. 1. A fragment of COVER depicting value experiences [33]

[FIGURE]

## 3.3 Value and Risk Experience Modeling in Archimate

Archimate is a modeling standard that defines a layered structure by means of which the architecture of enterprises can be described [39]. Based on the Common Ontology of Value and Risk, Sales et al. [35] propose a pattern language for value modeling in Archimate that allows the representation of Value Experiences as well as Experience Valuations, among others. Similarly, in [32] Sales et al. conduct an ontological analysis of risk modeling in Archimate in the light of COVER, in which they propose a pattern to represent Risk Experiences. By deriving patterns from COVER, they provide clear real-world semantics for its constituting elements, thus reducing the ambiguity and conceptual complexity found in previous approaches to model value and risk in the literature.

Fig. 2. A fragment of COVER depicting risk experiences [33]

[FIGURE]

In the sequel we briefly describe three patterns that are relevant in the context of our paper, namely the Value Experience Pattern, the Experience Valuation Pattern and the Risk Experience Pattern. For a more detailed discussion on value and risk modeling patterns, one should refer to [35] and [32], respectively.

Value Experience. This pattern allows modelers to detail experiences that creates value for a given stakeholder. As shown in Fig. 3, it consists of a «ValueExperience» Grouping connected to a Stakeholder acting as the value subject (agent from whose perspective the experience creates value), and its decomposition into value events, which can be represented using Business Processes , Business Events and/or Business Interactions .

Fig. 3. The Value Experience Pattern

[FIGURE]

Experience Valuation. This pattern allows modelers to describe value judgments made towards experiences. As shown in Fig. 4, it consists of a «Valuation» Assessment made by a Stakeholder (Value Assessor) that a «ValueExperience» creates Value for another Stakeholder (Value Subject). The Value element corresponds to an entry in a scale chosen by the modeler.

Fig. 4. The Experience Valuation Pattern

[FIGURE]

Risk Experience. According to Sales et al. [32] risk experiences focus on unwanted events that have the potential of causing losses and are composed by events of two types, namely threat and loss events. A threat event is the one with the potential of causing a loss. As described in [32], it might be the manifestation of a vulnerability or a threatening capability. The second mandatory component of a risk experience is a loss event, which necessarily impact intentions in a negative way.

In [32] the authors map risk experience as a Grouping stereotyped as a «RiskExperience», which aggregates the elements and the relations in the experience. They associate the «RiskExperience» Grouping with risks, which are mapped as «Risk» Drivers , as drivers represent 'conditions that motivate an organization to define its goals and implement the changes necessary to achieve them' [39]. For the sake of simplicity, we represent here a simplified version of the Risk Experience pattern (Fig. 5), containing only the experience elements and relations that are relevant to our proposal.

Fig. 5. The Risk Experience Pattern

[FIGURE]

## 4 Modeling the Emergence of Value and Risk from Outcomes in the Unified Foundational Ontology (UFO)

In this section, we use the aforementioned theories to present a preliminary model of the emergence of value and risk from games outcomes. Our analysis relies on the concepts of value and risk defined in COVER, the Common Ontology of ValuE and Risk [33].

Note that, as argued in [34], value can be ascribed to past, actual or envisioned experiences. Risk, however, is only ascribed to envisioned experiences that may (but are not certain to) happen [33]. Also agents' actions (or strategies) in a game may be about envisioned events (which may never occur). For instance, if a depositor decides to withdraw her money instead of retaining it in the bank, then the action of retaining the money will not happen. This means that we need to refer to future or envisioned events - whose expected temporal properties are not completely fixed - in our domain of discourse. Therefore, we shall talk of expected events as regular entities of our domain, not differently from, say, a planned air trip in a flight reservation system. In order to use this nonclassical notion of events in our analysis while maintaining its ontological rigour, we employ the formulation of events as proposed in [10], which was already successfully employed in [33] and [34]. 1

Fig. 6. Modeling the emergence of Value Risk from Outcomes in OntoUML

[FIGURE]

Fig. 7. Value and Risk Events

[FIGURE]

Our model is specified in OntoUML [12] and thus, compliant with the meta -ontological commitments of the Unified Foundational Ontology (UFO) [12]. In the diagram depicted in Figs. 6 and 7, we represent events in yellow, relators in green, objects in pink, qualities and modes in blue, situations in orange and datatypes in white.

1 A different strategy that avoids introducing future or possible events is to rephrase the model using types of actions and events, cf. [29].

We use the notion of agent defined in UFO-C to model a participant of a game as an Agent that plays the role of Game Player in a Game (Fig. 6). In UFO-C, agents are individuals that can perform actions, perceive events and bear mental aspects. A relevant type of mental aspect for our proposal is the intention . Intentions are desired state of affairs for which the agent commits to pursuing (e.g., the intention of going to a beach resort for the next summer break) [3]. For this reason, intentions cause the agent to perform actions . In the ontology, Intentions are represented as modes that inhere in Agent s.

The Actions performed by Game Players are modeled as intentional events, in the sense that they have the specific purpose of satisfying some Intention . As events, actions can be atomic or complex. A complex action is composed of several actions. Action Profiles are complex events composed of Actions performed by the players in a Game .

In the ontology, the Action Profile is modeled as a type of Value Event [33] (as defined in COVER [33]) and can be classified into Impact and Trigger Event (Fig. 7). The former is the one that directly impact an Intention of reaching a goal. By contrast, a Trigger Event is simply the one that causes an Impact Event . Within the category of Impact Events we can further distinguish into Gain Event and Loss Event . The difference between them rely on the nature of the impact caused on goals (positive for Gain Event s and negative for Loss Event s).

A Game involves a set of Outcomes . Outcome s are modeled as a type of Value Experience [33] (as defined in COVER [33]) and thus are composed of Value Events. Among the Value Events that compose an Outcome there is exactly one Action Profile . Figure 7 presents a fragment of COVER depicting the different types of Value Events that can compose a Value Experience.

Outcome s have impact on Game Player s' Intentions , which may affect her goals either positively or negatively. We analyze the emergence of risks from Outcome s, based on COVER [33]. An Action Profile is a complex event that brings about a Resulting Situation (Fig. 7). The Resulting Situation may satisfy the Game Player 's goals (and in this case it is considered a Successful Situation ) or, in the worst case, it may not have the desired result and the Game Player will not be able to achieve her goal. In this case, the Resulting Situation stands for a Threatening Situation that may trigger a Threat Event , which may cause a loss. The Loss Event is a Risk Event that impacts intentions in a negative way, as it hurts the Game Player 's Intention s of reaching a specific goal.

As we have previously discussed, value emerges from achieving goals. Thus, the more an event contributes to the achievement of a goal, the more valuable it is. Outcomes that positively impact Game Player s' Intentions can create value. However, whether or not value is produced in the realization of an Outcome is, in fact, a subjective notion, which depends on how the Game Player s assess their participation, i.e., whether they ascribe to the experience a positive assessment [33,34].

The entity Utility Value Ascription represents this assessment. The Utility Value Ascription is an example of a mode that inheres in the Agent and is externally dependent on the Outcome . As aforementioned, a mode is an existentially dependent entity that, as such, can only exist by inhering in some other individual. In particular, the Utility Value Ascription is a relationally dependent mode (or an externally dependent mode), i.e., a mode that inheres in an individual but which is also externally dependent on a different individual. The Utility Value Ascription mode takes a value in at least one (but possibly several) Utility Value Magnitude Space s, via the quality Utility Value . These spaces have, in OntoUML, the semantics of abstract conceptual spaces, delimiting the possible values an intrinsic property can be projected into, cf. [12].

Finally, the Utility is composed of the Utility Value Ascriptions of the possible Outcomes , under the perspective of a particular Game Player . In the model, Utility is represented as a complex externally dependent mode that inheres in the Game Player and is composed of the mereological sum of Utility Value Ascription modes 2 .

## 5 Use Case Illustration: Bank Run

In this section, we instantiate our model with two outcomes of the Bank Run example, described in Sect. 2.2, which are Nash Equilibria.

Firstly, in Fig. 8, we illustrate the instantiation of the Outcome in which both Depositor A and Depositor B retain the invested amount until the project matures. In this case both Game Player s have the Intention of 'making profit from the investment'. The Action Profile is composed of the Action of Depositor A , who decides to retain her money and the Action of Depositor B , who also decides to retain her deposit. Note that this is a case of Nash Equilibrium as once Depositor A has retained her deposit, Depositor B can do no better than retaining her deposit too. This Action Profile brings about a situation in which 'the bank does not need cash before the project completion', which stands for a Successful Situation . Consequently, the bank sells the project to another bank at price of 2400 euros, which is considered a Trigger Event that triggers two Gain Events , namely 'Bank pays out more than the amount invested by Depositor A' and 'Bank pays out more than the amount invested by Depositor B'. These two Gain Events positively impact the Intention s of Depositor s A and B of 'making profit from their investments', as they will receive 1200 euros, which is more than the invested value (1000 euros).

Secondly, in Fig. 9, we illustrate the instantiation of the Outcome in which both Depositor A and Depositor B withdraw the invested amount before the project matures. Also in this case, both Game Player s have the Intention of 'making profit from the investment'. The Action Profile is composed of the Action of Depositor A , who decides to withdraw her money and the Action of Depositor B , who also decides to withdraw her deposit. Note that here we also have a case of Nash Equilibrium. Although this outcome is not the one with the best payoff for both players, it can be seen as 'a steady state, in which each player holds the correct expectation about the other players' behavior and acts rationally' [25]: if Depositor A believes that Depositor B will withdraw before the project matures, then her best response is to withdraw as well.

2 This is compatible with the modeling of preferences according to UFO in [28].

Fig. 8. The emergence of Value from Outcomes

[FIGURE]

In the sequel, this Action Profile brings about a situation in which 'the bank needs cash to repay the deposits before the project completion' that can be considered a Threatening Situation . This situation may trigger a Threat Event if, for example, 'the bank is forced to liquidate its investments before the project matures, and recovers only 1600 euros'. This Threat Event causes two Loss Event s, which are 'the bank paying out less than the amount invested by Depositor A and Depositor B, respectively'. These Loss Event s, in turn, hurt the Depositor s' Intention s of 'making profit from their investments'.

We focused on the Nash Equilibria of the game; clearly our approach can be used also for modelling non-equilibrium states. It is interesting to notice that our models illustrate why in a Nash equilibrium players have no incentives to deviate from the current course of action. The chosen action (e.g. 'retain' for both players A and B in Fig. 8) is the action that positively impacts the intention of each player more than any other action, given the other players' move (by definition). Thus, assuming that rational players are pursuing actions that better impact their intentions, players have indeed no reason to deviate from that choice in that context. By contrast, in a non-Nash Equilibrium outcome, players would have actions at their disposal that promote their intentions better, thus providing an incentive to deviate to the action that better impact their intention. Therefore, the ontological analysis provides a rich semantic understanding of equilibrium outcomes, associating the stability of the outcome with the satisfaction of the intentions of the players.

Fig. 9. The emergence of Risk from Outcomes

[FIGURE]

## 6 Modeling Game Outcomes in Enterprise Architecture: The Bank Run Example in Archimate

In order to provide enterprise architects with a common ground to apply game theory notions in coherent enterprise architecture descriptions, we apply the results of the analysis conducted in the previous section to represent the emergence of value and risk from game outcomes in Enterprise Architecture.

In particular, we employ the Archimate modeling patterns based on COVER and presented in Sect. 3.3. We use these patterns to represent the emergence of value and risk from outcomes in the context of the Bank Run example (Sect. 2.2), under the perspective of Depositor A .

To illustrate the emergence of value, we represent the situation in which both Depositor A and Depositor B retain their deposits until the project matures. We start with the application of the Value Experience pattern. The value subject identifies the perspective from which the judgment is made and whose goals are considered, which in this case corresponds to Depositor A . We represent Depositor A 's goal of 'Making profit from investment' as the goal the experience realizes. The experience corresponds to the Outcome and is composed of the Action Profile retain-retain (a complex event composed of the actions Depositor A retains and Depositor B retains ) that triggers the event 'Bank sells the project to another bank after it matures', which in turn triggers the gain event 'Bank pays out more than the amount invested'. This gain event positively impacts Depositor A 's goal of 'Making profit from investment'.

In order to represent how Depositor A ascribes value to the experience, we apply the Experience Valuation pattern. We connect a Valuation Assessment to the value experience named 'Outcome Make profit by retaining deposit' (which corresponds to the Outcome ) and to Depositor A , who plays the roles of value assessor and value subject simultaneously. The value ascribed corresponds to Depositor A 's Utility Value for this Outcome . Figure 10 depicts the application of the patterns just described.

Fig. 10. Application of the Value Experience and Experience Valuation Patterns

[FIGURE]

Fig. 11. Application of the Risk Experience Pattern

[FIGURE]

We illustrate the emergence of risk, by representing the situation in which both Depositor A and Depositor B withdraw their deposits before the project matures.

Using the Risk Experience pattern we represent, in Fig. 11, the emergence of the risk of 'Money loss', under the perspective of Depositor A , who is the risk subject. The risk experience of 'Outcome Money loss due to deposit withdraw' represents the Outcome and is composed of the Action Profile withdraw-withdraw (a complex event composed of the actions Depositor A withdraws and Depositor B withdraws ) that brings about a situation in which the 'Bank needs cash to repay the deposits'. As a result, the 'Bank is forced to liquidate investments before project matures', which stands for a threat event that triggers the loss event 'Bank pays out less than the amount invested by Depositor A'. This loss event hurts Depositor A 's goal of 'Making profit from investment'.

## 7 Final Remarks

We presented an ontological analysis characterizing some basic concepts in game theory, which make clear the emergence of value and risks from game outcomes. We formalized it in OntoUML, aiming at providing an accessible and shareable conceptual model, which may be applied across domains to foster the interoperability and the mutual understanding among modelers.

The model proposed here illustrates a process of conceptual clarification that allows for unpacking the relevant domain notions that are frequently hidden in mathematical formulations of domain phenomena. Moreover, it allows for the ontological grounding of the variables constituting these mathematical formulations. These are in line with the requirements for conceptual models as discussed in [11]. In that paper, the authors discuss why a mathematical model (e.g., Newton's Second Law) is not a conceptual model. They argue that in a formula such as F = M * A 'the modeling constructs are operators and variables. The latter do not denote concepts, but rather actual values of physical quantities. Of course we need a mental model to make sense of such relationship, but such mental model is just presupposed, and not made explicit. In contrast, a conceptual model of the phenomenon described by Newton's second law would not represent the values of such physical quantities without representing the physical quantities themselves, which would be considered as qualities...But just having qualities in the conceptual model would not be enough: we cannot have a free-floating quality (say, a mass) without representing its bearer, which is a physical object...This is what we call the grounding requirement' .

The relation between risk management and game theory has been broadly studied and different approaches have been proposed in the literature to explain how game theory approaches can be integrated into classical risk management [4,8,30,31]. Differently from other approaches, our proposal explores the deep connections between the concepts of value and risk to analyse the impact (either positive or negative) of game outcomes on player's welfare.

As future work, we plan to validate our ontology by means of systematic comparisons with other theories and formalizations of risk and value in the context of game theoretical approaches. We also plan to introduce a mechanism to help rational agents weight value and risks against each other to find an equilibrium when deciding whether to engage in a certain strategy.

Acknowledgments. CAPES (PhD grant 88881.173022/2018-01) and NeXON project (UNIBZ).

## References

1. Almeida, J.P.A., Falbo, R.A., Guizzardi, G.: Events as entities in ontology-driven conceptual modeling. In: Laender, A.H.F., Pernici, B., Lim, E.-P., de Oliveira, J.P.M. (eds.) ER 2019. LNCS, vol. 11788, pp. 469-483. Springer, Cham (2019). https://doi.org/10.1007/978-3-030-33223-5\_39
2. Botti Benevides, A., Bourguet, J.R., Guizzardi, G., Peñaloza, R., Almeida, J.P.A.: Representing a reference foundational ontology of events in SROIQ. Appl. Ontol. 14 (3), 293-334 (2019)
3. Castelfranchi, C.: Commitments: from individual intentions to groups and organizations. In: 1st International Conference on Multi-Agent Systems (ICMAS), vol. 95, pp. 41-48 (1995)
4. Cox Jr., L.A.: Game theory and risk analysis. Risk Anal. Int. J. 29 (8), 1062-1068 (2009)
5. Diamond, D.W., Dybvig, P.H.: Bank runs, deposit insurance, and liquidity. J. Polit. Econ. 91 (3), 401-419 (1983)
6. Easley, D., Kleinberg, J., et al.: Networks, crowds, and markets: reasoning about a highly connected world. Significance 9 , 43-44 (2012)
7. Fonseca, C.M., Porello, D., Guizzardi, G., Almeida, J.P.A., Guarino, N.: Relations in ontology-driven conceptual modeling. In: Laender, A.H.F., Pernici, B., Lim, E.P., de Oliveira, J.P.M. (eds.) ER 2019. LNCS, vol. 11788, pp. 28-42. Springer, Cham (2019). https://doi.org/10.1007/978-3-030-33223-5\_4
8. GhavamiFar, F., Taghiyareh, F., Razavi, M.: Game theory as a tool for converting risk to opportunity (2007)
9. Guarino, N.: Formal ontology in information systems. In: Proceedings of the First International Conference (FOIS 1998), Trento, Italy, 6-8 June, vol. 46. IOS Press (1998)
10. Guarino, N.: On the semantics of ongoing and future occurrence identifiers. In: Mayr, H.C., Guizzardi, G., Ma, H., Pastor, O. (eds.) ER 2017. LNCS, vol. 10650, pp. 477-490. Springer, Cham (2017). https://doi.org/10.1007/978-3-319-69904-2\_36
11. Guarino, N., Guizzardi, G., Mylopoulos, J.: On the philosophical foundations of conceptual models. Inf. Model. Knowl. Bases XXXI (321), 1 (2020)
12. Guizzardi, G.: Ontological foundations for structural conceptual models. Telematica Instituut/CTIT (2005)
13. Guizzardi, G., Falbo, R.A., Guizzardi, R.S.S.: Grounding software domain ontologies in the Unified Foundational Ontology (UFO). In: 11th Ibero-American Conference on Software Engineering (CIbSE), pp. 127-140 (2008)
14. Guizzardi, G., Fonseca, C.M., Benevides, A.B., Almeida, J.P.A., Porello, D., Sales, T.P.: Endurant types in ontology-driven conceptual modeling: towards OntoUML 2.0. In: Trujillo, J.C., et al. (eds.) ER 2018. LNCS, vol. 11157, pp. 136-150. Springer, Cham (2018). https://doi.org/10.1007/978-3-030-00847-5\_12
15. Guizzardi, G., Wagner, G., Almeida, J.P.A., Guizzardi, R.S.S.: Towards ontological foundations for conceptual modeling: the Unified Foundational Ontology (UFO) story. Appl. Ontol. 10 (3-4), 259-271 (2015)
16. Guizzardi, G., Wagner, G., de Almeida Falbo, R., Guizzardi, R.S.S., Almeida, J.P.A.: Towards ontological foundations for the conceptual modeling of events. In: Ng, W., Storey, V.C., Trujillo, J.C. (eds.) ER 2013. LNCS, vol. 8217, pp. 327-341. Springer, Heidelberg (2013). https://doi.org/10.1007/978-3-642-41924-9\_27

17. Guizzardi, R.S.S., Guizzardi, G.: Ontology-based transformation framework from TROPOS to AORML. In: Social Modeling for Requirements Engineering, pp. 547570. The MIT Press (2010)
18. ISO: Risk Management - Vocabulary. Standard, International Organization for Standardization (2018)
19. ISO: Risk Management - Guidelines. Standard, International Organization for Standardization (2009)
20. Jarzabkowski, P., Wilson, D.C.: Actionable strategy knowledge: a practice perspective. Eur. Manag. J. 24 (5), 348-367 (2006)
21. Kambil, A., Ginsberg, A., Bloch, M.: Re-inventing value propositions. Information Systems Working Papers Series (1996)
22. Lanning, M.J., Michaels, E.G.: A business is a value delivery system. McKinsey Staff Paper 41 (July) (1988)
23. McKelvey, R.D., McLennan, A.M., Turocy, T.L.: Gambit: software tools for game theory (2006)
24. Myerson, R.: Game Theory: Analysis of Conflict. Press, Cambridge (1991)
25. Osborne, M.J., Rubinstein, A.: A Course in Game Theory. MIT Press, Cambridge (1994)
26. Payolo, A.R.: A toilet paper run is like a bank run. The economic fixes are about the same. The Conversation, March 2020. https://theconversation.com/a-toiletpaper-run-is-like-a-bank-run-the-economic-fixes-are-about-the-same-133065
27. Peterson, M.: An Introduction to Decision Theory. Cambridge University Press, Cambridge (2017)
28. Porello, D., Guizzardi, G.: Towards an ontological modelling of preference relations. In: Ghidini, C., Magnini, B., Passerini, A., Traverso, P. (eds.) AI*IA 2018. LNCS (LNAI), vol. 11298, pp. 152-165. Springer, Cham (2018). https://doi.org/10.1007/ 978-3-030-03840-3\_12
29. Porello, D., Guizzardi, G., Sales, T.P., Amaral, G.: A core ontology for economic exchanges. In: Dobbie, G., Frank, U., Kappel, G., Liddle, S.W., Mayr, H.C. (eds.) ER 2020. LNCS, vol. 12400, pp. 364-374. Springer, Cham (2020). https://doi.org/ 10.1007/978-3-030-62522-1\_27
30. Rajbhandari, L., Snekkenes, E.A.: Mapping between classical risk management and game theoretical approaches. In: De Decker, B., Lapon, J., Naessens, V., Uhl, A. (eds.) CMS 2011. LNCS, vol. 7025, pp. 147-154. Springer, Heidelberg (2011). https://doi.org/10.1007/978-3-642-24712-5\_12
31. Rass, S.: On game-theoretic risk management (part three)-modeling and applications. arXiv preprint arXiv:1711.00708 (2017)
32. Sales, T.P., Almeida, J.P.A., Santini, S., Baião, F., Guizzardi, G.: Ontological analysis and redesign of risk modeling in ArchiMate. In: 2018 IEEE 22nd International Enterprise Distributed Object Computing Conference (EDOC), pp. 154-163. IEEE (2018)
33. Sales, T.P., Baião, F., Guizzardi, G., Almeida, J.P.A., Guarino, N., Mylopoulos, J.: The common ontology of value and risk. In: Trujillo, J.C., et al. (eds.) ER 2018. LNCS, vol. 11157, pp. 121-135. Springer, Cham (2018). https://doi.org/10.1007/ 978-3-030-00847-5\_11
34. Sales, T.P., Guarino, N., Guizzardi, G., Mylopoulos, J.: An ontological analysis of value propositions. In: 21st IEEE International Enterprise Distributed Object Computing Conference (EDOC), pp. 184-193. IEEE (2017)

35. Sales, T.P., Roelens, B., Poels, G., Guizzardi, G., Guarino, N., Mylopoulos, J.: A pattern language for value modeling in ArchiMate. In: Giorgini, P., Weber, B. (eds.) CAiSE 2019. LNCS, vol. 11483, pp. 230-245. Springer, Cham (2019). https://doi. org/10.1007/978-3-030-21290-2\_15
36. Savani, R., von Stengel, B.: Game theory explorer: software for the applied game theorist. Comput. Manag. Sci. 12 (1), 5-33 (2015)
37. Shoham, Y., Leyton-Brown, K.: Multiagent Systems: Algorithmic, GameTheoretic, and Logical Foundations. Cambridge University Press, Cambridge (2008)
38. Sun, S., Sun, N.: The fundamentals of non-cooperative games. In: Sun, S., Sun, N. (eds.) Management Game Theory, pp. 1-21. Springer, Singapore (2018). https:// doi.org/10.1007/978-981-13-1062-1\_1
39. The Open Group: ArchiMate 3.0.1 Specification. Standard C179 (2017)
40. Verdonck, M., Gailly, F.: Insights on the use and application of ontology and conceptual modeling languages in ontology-driven conceptual modeling. In: ComynWattiau, I., Tanaka, K., Song, I.-Y., Yamamoto, S., Saeki, M. (eds.) ER 2016. LNCS, vol. 9974, pp. 83-97. Springer, Cham (2016). https://doi.org/10.1007/9783-319-46397-1\_7
41. Watson, J.: Strategy: an Introduction to Game Theory, vol. 139. WW Norton New York (2002)
42. Wooldridge, M.: An Introduction to Multiagent Systems. Wiley, Hoboken (2009)
