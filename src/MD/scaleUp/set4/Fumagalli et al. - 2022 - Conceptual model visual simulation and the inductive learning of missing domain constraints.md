[FIGURE]

Contents lists available at ScienceDirect

## Data &amp; Knowledge Engineering

[journal homepage: www.elsevier.com/locate/datak](http://www.elsevier.com/locate/datak)

## Conceptual model visual simulation and the inductive learning of missing domain constraints

Mattia Fumagalli a, ∗ , Tiago Prince Sales a , Fernanda Araujo Baião b , Giancarlo Guizzardi a,c

- a Conceptual and Cognitive Modeling Research Group (CORE), Free University of Bozen-Bolzano, Bolzano, Italy
- b Department of Industrial Engineering, Pontifical Catholic University of Rio de Janeiro, Rio de Janeiro, Brazil

c Services &amp; Cybersecurity (SCS), University of Twente, Enschede, The Netherlands

## A R T I C L E I N F O

Keywords: Conceptual modeling Constraints learning Model validation Inductive learning Inductive Logic Programming Model simulation

## 1. Introduction

Conceptual modeling plays a fundamental role in data and knowledge engineering and management. They allow for the embedding of semantics into a data representation, and they directly impact the quality and correctness of the related information systems [1]. Still, conceptual modeling is a highly error-prone activity. This is because, among other factors, modeling is a complex task, which requires a level of expertise that practitioners often lack [2-4]. Therefore, it is not surprising that, in recent years, the difficulty of designing conceptual models has been investigated in several contributions [5-8] within the information systems engineering community.

A great deal of research effort has been devoted to devise conceptual models validation techniques, with the main goal of identifying and avoiding significant faults in conceptual models. More specifically, promising results have been produced in validating conceptual models from a semantic perspective [9-11]. From this perspective, conceptual models should only allow for instantiations (e.g., model interpretations , instance populations ) that correspond to state-of-affairs that are admissible according to the

∗ Corresponding author. E-mail address: mattia.fumagalli@unibz.it (M. Fumagalli).

0169-023X/ © 2022 Elsevier B.V. All rights reserved.

## A B S T R A C T

Conceptual modeling plays a fundamental role in information systems engineering, and in data and systems interoperability. To play their role as instruments for domain modeling, conceptual models must contain the exact set of constraints that represent the worldview of the relevant domain stakeholders. However, as empirical results show, conceptual modelers are subject to cognitive limitations and biases and, hence, in practice, they systematically produce models that fall short in that respect. Moreover, automating the process of formally assessing conceptual models in this sense (i.e., model validation) is notoriously hard, mainly because the intended worldview at hand lies in the mind of these stakeholders. In this paper, we provide a novel approach to model validation and automated constraint learning that combines, on one hand, Model Finding via the visual simulation of that model's valid instances and, on the other hand, Inductive Logic Programming techniques. In our approach, we properly channel the results produced by the application of a visual model finding technique as input to a learning process. We then show how the approach is able to support the modeler in identifying missing constraints from the original model. The approach is validated against a catalog of empiricallyelicited conceptual modeling anti-patterns. As we show here, the approach is able to support the automated learning of constraints that are needed to rectify a number of relevant anti-patterns in this catalog.

[FIGURE]

[FIGURE]

conceptualizations these models are supposed to represent. However, as empirical results show [1,10,12], modelers are subject to cognitive limitations and biases and, hence, in practice, are unable to create conceptual models endowed with this property. In particular, these results show that the produced models often lack the correct set of formal domain constraints 1 thus being either: underconstrained , i.e., they allow for model interpretations that are not intended by the community of modelers and domain experts; overconstrainted , i.e., they forbid interpretations that are intended by that community.

Checking if a conceptual model is overconstrained can be framed as a classical model checking problem, namely as the activity of verifying whether a given state of affairs holds in a given model [14]. This can be done by leveraging on well-established technologies model checking tools and approaches [15,16]. The same techniques offer little support for checking whether a conceptual model is underconstrained , i.e., for checking the existence of unintended interpretations of which the modelers is not aware a priori.

In the past, some of us have employed a validation technique combining model finding with visual simulation [17] to automatically generate a finite set of possible interpretations of a model so that the modeler can be contrasted with what the model is saying on their behalf [18]. Moreover, we managed to find regularities in these simulations that pointed to error-prone structures or anti-patterns [10,12], i.e., structures that whenever present in a conceptual model were prone to cause a deviation between the set of possible and intended interpretations of that model. However, in these past experiences, finding out which set of formal constraints should be included in the model as well as detecting these anti-patterns were tasks performed manually and required a significant modeling experience and expertise.

In this paper, we propose an approach that combines the aforementioned process of validation with a machine learning technique to support the automated learning of formal constraints. In particular, we employ visual model finding to generate a set of possible interpretations of a model. These interpretations are then shown to a modeler one by one, so she can either: mark an interpretation as intended - in which case all its constituent parts are intended; or mark an interpretation as unintended - in which case the modeler is asked to also identify which parts of that interpretation are unintended. By simply validating the model, the modeler is also curating a database of positive and negative examples of possible model interpretations. Moreover, the original model is itself a background theory . These components together form the basis on which formal constraints for model repair can be learned using Inductive Logical Programming (ILP) techniques [19]. As we demonstrate here, this approach allows for the learning of formal constraints without the requirement that the modelers formulate these constraints beforehand, thus bridging the gap between the modeler intended interpretations and the interpretations admitted by the model. The approach presented here is a significant extension and implementation of the ideas originally presented in [20,21].

The remainder of this paper is organized as follows: Section 2 describes the challenge of identifying semantic problems across conceptual models by introducing a running example. In that section, we also formally characterize the problem we are addressing here; in Section 3, we briefly explain the key roles played in our enterprise by techniques for model finding via visual simulation, as well as Inductive Logic Programming (ILP). In this paper, we focus on structural domain models represented as UML class diagrams (annotated with OntoUML stereotypes [22]). For this reason, OntoUML is also briefly introduced in that section; in Section 4, we present our framework, detailing its workflow and components. In doing that, we present the approach we follow to: (i) generate a set of possible interpretations of a model, (ii) curate as a database of negative and positive examples out of the interpretations set, (iii) prepare multiple training sets for distinct portions of the model. Finally, we also show (iv) how we map the input conceptual model into a Prolog-like [23,24] language, thus describing the learning process set-up; in Section 5, we provide experimental validation of the proposed approach. We show that the approach is able to support the learning of constraints that rectify a number of known and relevant conceptual modeling semantic anti-patterns; Section 6 elaborates on the implications of this research and the long-term program of supporting the automated learning of modeling constraints and anti-patterns, and Section 7 discusses related work; finally, Section 8 elaborates on some final considerations.

## 2. Problem statement

Let us consider the following scenario. Mary is a conceptual modeler. She has been working at a new company for just a few weeks. She is finally ready to share with her colleagues the first version of a domain model she designed for an important project. She knows the model is syntactically correct and logically consistent, but before sharing it, Mary wants to make sure it also accurately represents the domain she modeled. To do that, she uses a model finding tool (e.g. [18,25,26]), which allows her to automatically generate valid instances from her model, and thus, concretely uncover the worldview she has formalized with it. Unfortunately, from this assessment, Mary realizes that her model admits some instances it should not. She is now faced with a challenge. She needs to find out which constructs in her model are allowing for unintended instances and come up with a solution to prevent them, while still allowing all intended instances she already checked. What if, besides using a tool to generate valid model instances, Mary could use another tool that recommends amendments to her model based on her judgement of which of those valid instances are also intended?

Suppose that the conceptual model devised by Mary is the one depicted in Fig. 1, which is represented in OntoUML [22,27]. 2 The model mainly describes roles people may play in the context of a Criminal Investigation , namely:

· Detective : a Person who carries out a Criminal Investigation

1 Notice that we take the notion of ''domain constraint'' as from [13], where domain constraints are taken as constraints that are always related to the modeler's conceptualization of a domain of interest.

2 Notice that the point of the paper is not to propose an ontology of criminal investigation. The running example we adopted is designed to collect in one single model issues that, as described by the empirical analysis in [12], have been found in dozens of models (also used for real-world applications). This also allows us to validate how our approach can handle constraints that are needed in practice.

Fig. 1. OntoUML model representing a subset of criminal investigation domain.

[FIGURE]

- Suspect : a Person who is investigated in a Criminal Investigation
- Witness : a Person who contributes to a Criminal Investigation by participating in an Interrogation

Each Criminal Investigation has a Detective who is responsible for it, deemed the Lead Detective . Each Detective is classified according to his/her seniority as a Junior or a Senior Detective . Lastly, a Detective that is a Lead Detective or a Senior Detective is modeled as a Superintendent . The dynamics for this classification, however, is out of the scope of Mary's model. By adopting OntoUML, Mary knows that her model explicitly represents her domain of interest. For instance, she represented that certain types rigidly 3 classify their instances (e.g. Person , Criminal Investigation ), while others do so only accidentally (e.g Detective , Suspect ). She also captured that individuals of a certain type can only exist if related to individuals of other types (e.g. an instance of Interrogation existentially depends on an instance of Criminal Investigation ). She even declares the context in which certain roles are played (e.g. a Person becomes a Suspect if she is involved as the target of a Criminal Investigation ).

By adhering to OntoUML's syntax, Mary knows that her model conforms to the domain-independent principles put forth by the Unified Foundational Ontology (UFO) [22,27], and thus, is ontologically consistent.

OntoUML, however, cannot help Mary decide whether her model is an appropriate representation of the criminal investigation domain. On the one hand, it may be over-constrained, that is, it may forbid instances that correspond to intended states-of-affairs she sought to represent (i.e., forbidden intended instances ); on the other hand, it may be under-constrained, that is, it may allow for instances that correspond to non-intended states-of-affairs (i.e., allowed unintended instances ). Examples of the latter include:

- (1) there is a Lead Detective who is not a Senior Detective ;
- (2) there is an Interrogation in which a Detective interrogates herself ;
- (3) there is a Junior Detective who teams up with himself/herself and does not team up with any other Junior Detective ;
- (4) there is a Detective who is both Senior Detective and Lead Detective , but not Superintendent ;
- (5) there is a Junior Detective who teams up with another Junior Detective who is not managed by the same Senior Detective ;
- (6) there is a Criminal Investigation in which a Detective investigates herself ;
- (7) there is a Criminal Investigation in which a Detective is also a Witness ;
- (8) there is a Criminal Investigation in which a Suspect is also a Witness ;
- (9) there is a Criminal Investigation that is led by a Detective who does not participate in it ;
- (10) there is an Interrogation that questions a Witness who is not involved in the Criminal Investigation the Interrogation contributes to ;
- (11) there is an Interrogation that is conducted by a Detective who is not involved in the Criminal Investigation the Interrogation contributes to .

All these model instances (or model configurations) 4 are the result of an interpretation function satisfying the conceptual model . In other words, if we take the OntoUML diagram of Fig. 1 as a M1-model (in OMG's MDA sense), a configuration is a M0-model that could instantiate that M1-model; if we take the UML diagram as a logical specification, then a configuration is a logical model of that specification. Finding these valid configurations given a (conceptual) model is the classical task performed by a model finder .

3 In OntoUML, if an individual instantiates a rigid type in a certain situation, it instantiate that type in all possible situations [22]. Conversely, if an individual instantiates an anti-rigid type in a given situation, then there is always a possible counterfactual situation in which the individual exists without instantiating that type. In other words, these are types that promote static and dynamic classification conditions, respectively.

4 From now on we use these notions interchangeably.

Fig. 2. Inconsistency example (caused by 𝑥 1 and 𝑥 2 ) that can be stored into a constraint.

[FIGURE]

After discovering that the aforementioned configurations are allowed by her model and deciding whether they are intended (and, hence, should indeed be allowed) or unintended (and, hence, should be forbidden), Mary needs to repair the model in order to avoid the unintended admissible configurations. Helping modelers like Mary to automatically overcome this step is exactly the goal of this paper. More precisely, this paper develops an approach that automatically suggests repairing solutions for an under-constrained (Onto)UML model given a set of model configurations that have been identified by the modeler as intended or unintended.

## 2.1. Problem formalization

By taking inspiration from [28,29], we define the task of identifying repairing solutions for a given input conceptual model as follows:

- given an input model 𝑀 , a target constrained model 𝑀 𝐶 and a set of instances 𝐸 that satisfy 𝑀 and do not satisfy 𝑀 𝐶 ;
- such that 𝑀 ∩ 𝐶 ⊆ 𝑀 𝐶 .
- find a set of constraints 𝐶 ;

To illustrate this definition, let us consider the model devised by Mary in Fig. 1 as 𝑀 . Suppose that we have an instance 𝑒 ∈ 𝐸 that is both a Junior Detective and a Lead Detective . This instance satisfies the source model 𝑀 but it is an non-intended instance (i.e., it does not satisfy the constraints of a target constrained model 𝑀 𝐶 representing the conceptualization Mary has in her mind).

Fig. 2 illustrates this situation, caused by the fact that in 𝑀 Junior Detective is not disjoint with Lead Detective . In this setting, learning a constraint, means finding a formula, e.g., ¬( 𝐽𝑢𝑛𝑖𝑜𝑟𝐷𝑒𝑡𝑒𝑐𝑡𝑖𝑣𝑒 ∧ 𝐿𝑒𝑎𝑑𝐷𝑒𝑡𝑒𝑐𝑡𝑖𝑣𝑒 ) , by which 𝑀 can be amended.

## 3. Research baseline

We build the approach proposed in this work on top of three key research outputs, namely: (i) the OntoUML conceptual modeling language [22]; (ii) the Alloy [17] specification language and its related model validation facilities, and (iii) the ProbFOIL [24] probabilistic rule learner, which combines the relational rule learner FOIL 5 with the probabilistic Prolog , ProbLog [23]. In the sequel, we elaborate on these three background technologies.

(i) OntoUML is an extension of the UML modeling language. Its meta-model is grounded on UFO (Unified Foundational Ontology) [22], namely a formal theory based on contributions from Formal Ontology in Philosophy, Philosophical Logic, Cognitive Psychology, and Linguistics. UFO is considered one of the most used foundational ontologies in conceptual modeling and OntoUML is among the most used languages in ontology-driven conceptual modeling [30]. An example of core ontological distinctions underlying OntoUML is represented by the key categories of object types (e.g., Kind , Subkind , Roles and RoleMixins ), trope types (e.g., Relator , Mode ) and relations ( formal relations , material relations and parthood relations ). 6

One of the main goals of OntoUML is supporting the conceptual modeling activities by making explicit the semantics behind the modelers' design choices, thus enabling key features of the output conceptual models, such as understandability, interoperability, and reusability.

In the context of this work, we adopted OntoUML to pave the way towards a constraint learning approach that can be applied over different OntoUML models. Moreover, the fact that OntoUML is grounded on UFO will support us in the future goal of uncovering recurrent errors and learning-related constraints, not only within single-domain models but also across multiple models.

[5 https://cgi.csc.liv.ac.uk/~frans/KDD/Software/FOIL\_PRM\_CPAR/foil.html.](https://cgi.csc.liv.ac.uk/~frans/KDD/Software/FOIL_PRM_CPAR/foil.html)

6 For an in depth analysis and characterization of the ontological categories underlying OntoUML, the reader is referred to [22,27,31].

Fig. 3. An overview of the constraint learning process.

[FIGURE]

(ii) Alloy [17,26] is a language for specifying and analyzing structures based on relational logic . Its creators combined existential and universal quantifiers from first-order logic with operators from set theory (e.g., union, intersection) and relational calculus (e.g., relational join) to create a fairly expressive language.

One of the key features of Alloy is its powerful model analysis service. This feature can be used to address model finding tasks, 7 namely to generate possible instances for a given model specified through the Alloy language. The generated instances are taken as part of simulations , by which a demonstration of how the input model can be satisfied is provided. The generation of instances is defined by a user-defined scope , which bounds the number of instances that can be generated for each predicate in the model. The rationale underlying the bounded model finding strategy of Alloy is the small scope hypothesis [32,33], which basically claims most design errors can be found in small counterexamples [34]. Experimental results suggest that exhaustive testing within a small finite domain does indeed catch all type system errors in practice [35], and many case studies using the tool Alloy have confirmed the hypothesis by performing an analysis in a variety of scopes and showing, retrospectively, that a small scope would have sufficed to find all the bugs discovered [26].

The Alloy's model finding facility is pivotal for our approach since it is necessary to uncover underconstraining problems within the input model. Thanks to the generated simulations the modeler can indeed check if the model allows for unintended instances and whether the model needs to be constrained. Is worth mentioning that the Alloy analyzer can also be used to run model checking and counterexamples generation, thus addressing over-constraining issues, which are, however, out of the scope of the problem we are addressing in this paper.

(iii) ProbFOIL [24] 8 is the Inductive Logic Programming (ILP) algorithm by which we address the learning task. This package is used to extend the Problog [23] 9 distribution for addressing structure learning tasks , where, for instance, a set of example predicates and target predicates can be defined to learn about n-ary relations. ProbFOIL can be taken as an upgrade of traditional rule learning, which combines the relational rule learner FOIL with the probabilistic Prolog , ProbLog. Besides, learning deterministic rules from deterministic data, this algorithm can also be used, indeed, to learn probabilistic rules, by exploiting logical and probabilistic examples.

We adopted this algorithm because it leverages the main core functionalities of most of the state-of-the-art rule learners [36] and, with simple customization, represents a flexible solution to handle different types of constraint rules. Moreover, the ProbFOIL probabilistic setting is key to what we are planning to do in the immediate future work, namely applying our approach by exploiting different feedback from multiple users (see discussion on Section 8.1), where the ProbFOIL capabilities can be exploited to address model validation as a meaning negotiation task , i.e., where multiple modelers can provide their feedback about possible negative and positive examples admitted by the same conceptual model. In this setting, the final repairing solution can be derived, for instance, by leveraging the annotations that are most relevant within the collected data.

## 4. Conceptual model visual simulation meets inductive learning

In what follows we describe the framework to combine model finding and inductive logic programming to support the learning of constraints that are missing from conceptual models. The framework can be divided into four main phases, which are then divided into related steps (see Fig. 3). The first three phases, namely the (1) Generation , the (2) Assertion and the (3) Induction phases represent the core of this paper proposal. The (4) Repair phase will be addressed in the immediate future work. We discuss it here, nonetheless, for sake of completeness of the framework [37].

7 The Alloy Analyzer can be downloaded at https://alloytools.org/.

[8 https://pypi.org/project/probfoil/.](https://pypi.org/project/probfoil/)

[9 https://problog.readthedocs.io/en/latest/.](https://problog.readthedocs.io/en/latest/)

## 4.1. Generation

The first step in our approach is the generation phase (see (1) in Fig. 3), which automatically generates a set of valid instance models or configurations for a conceptual model under validation. The configurations are generated by converting the OntoUML model at hand into an Alloy specification (activity 1.a in Fig. 3), which is then fed into the Alloy Analyzer to generate possible instances or to look for counter-examples that fail the assumptions we have about our model (activity 1.b in Fig. 3). To be able to analyze models specified in Alloy, the tool performs a bounded analysis, assuming that at most 𝑁 individuals of each type may exist. The rationale underlying this strategy is the aforementioned small scope hypothesis [32,33].

To use Alloy and the Alloy Analyzer for generating admissible instances of our conceptual models, we need a tool that can translate (Onto)UML into Alloy. For OntoUML, such a tool has been proposed by Benevides et al. [18], while for UML, it has been proposed by Shah et al. [38]. In this study, we use a combination of both approaches to accommodate the changes introduced in the new OntoUML version [27] The Alloy code produced by applying this transformation to the criminal investigation model is shown in Listing 1. In other words, this listing represent the logical rendering of that conceptual modeling in this language. 10

```
abstract sig Endurant {} abstract sig Object extends Endurant {} abstract sig Relator extends Endurant { mediates ∶ some Endurant } { all r ∶ Relator | #r.@mediates ≥ 2 } sig Person extends Object {} sig Detective in Person {} { all d ∶ Detective | some InvolvesDetective.d } sig JuniorDetective in Detective { TeamsUp ∶ some JuniorDetective } { all r ∶ JuniorDetective | one Manages.r } sig SeniorDetective in Detective { Manages ∶ some JuniorDetective } { all r ∶ SeniorDetective | #r.@Manages ≥ 2 } sig LeadDetective in Detective {}{ all d ∶ LeadDetective | one IsLedBy.d } sig Superintendent in LeadDetective + SeniorDetective {} sig Suspect in Person {} { all s ∶ Suspect | some InvolvesSuspect.s } sig Witness in Person {} { all w ∶ Witness | some InvolvesWitness.w all w ∶ Witness | some Questions.w } sig CriminalInvestigation extends Relator { InvolvesDetective ∶ some Detective, InvolvesSuspect ∶ some Suspect, InvolvesWitness ∶ set Witness, IsLedBy ∶ one LeadDetective } sig Interrogation extends Relator { ConductedBy ∶ one Detective, ContributesTo ∶ one CriminalInvestigation, Questions ∶ one Witness } fact { Detective = JuniorDetective + SeniorDetective disj [JuniorDetective,SeniorDetective] Questions in mediates ContributesTo in mediates ConductedBy in mediates InvolvesWitness in mediates
```

Listing 1: Alloy code formalizing the criminal investigation model of Fig. 1.

10 Notice that the Alloy analyzer can be adopted with efficacy on models of restricted size. However, our approach scales to bigger models. That is, it requires models to be broken down into pieces. We account for the possibility of cutting complex models into simpler sub-models to facilitate the modeler analysis and the simulation process relying on previous work [39,40].

[FIGURE]

Fig. 4. An example of intended configuration found using Alloy Analyzer.

```
InvolvesDetective in mediates InvolvesSuspect in mediates IsLedBy in mediates ~mediates & mediates in iden no iden & mediates mediates = ConductedBy + ContributesTo + InvolvesDetective + InvolvesSuspect + InvolvesWitness + IsLedBy ↪ + Questions }
```

## 4.2. Assertion

In the assertion phase (see (2) in Fig. 3), each model configuration generated in the previous phase is processed and analyzed by the modeler, who annotates it as either intended or unintended (activity (2.a) in Fig. 3). 11 An example of an intended configuration is shown in Fig. 4, 12 illustrating a CriminalInvestigation that is led by Person2 , who investigates Suspect Person1 and counts on Person0 as a Witness .

Conversely, Fig. 5 depicts an unintended configuration that contains the following errors:

- E1. Person0 and Person1 are a Detective in CriminalInvestigation0 and CriminalInvestigation1 respectively, while also being a Suspect in them;
- E2. Person1 leads CriminalInvestigation0 , while still being ranked as a JuniorDetective ;
- E3. Person1 leads CriminalInvestigation0 without being involved in it;
- E4. Interrogation questions Witness Person0 who is not involved in the CriminalInvestigation the Interrogation contributes to;
- E5. Person2 is a Superintendent without being a SeniorDetective ;
- E6. Person2 teams up with herself.

If only intended configurations are found in the annotation step, no constraints need to be learned and the process terminates. Otherwise, it continues to the elicitation step (activity (2.b) in Fig. 3), which is when the modeler goes through the configurations she identified as unintended to explain her decisions. This is done by identifying in these configurations, exactly which elements there are responsible for making them unintended.

11 Although we describe this as a waterfall process, in which all model configurations are first generated and then classified, that is not how the process necessarily unfolds. A modeler may just as well annotate a configuration as intended or unintended right after it is generated and then go back to generate more configurations.

12 In the figures depicting model configurations generated by Alloy, each box represents an individual, which we paint according to the following coloring scheme: (i). instances of Interrogation are represented by blue boxes; (ii). instances of CriminalInvestigation are represented by green boxes; and instances of Person , regardless of the role they are playing, are represented by yellow boxes. Additionally, the top label in each box is the identifier for the individual it represents (e.g. Interrogation , Person0 ), while the this/xxx labels refer to classes the individual instantiates. So, in Fig. 5, since Person2 's box has the labels this/LeadDetective , this/SeniorDetective and this/Superintendent , it means the individual Person2 instantiates the LeadDetective , this/SeniorDetective and this/Superintendent classes at that configuration. The arcs between boxes refer to relations that hold between the individuals characterized by those boxes.

Fig. 5. Unintended but valid instantiation of the criminal investigation model of Fig. 1 found by the Alloy Analyzer. (For interpretation of the references to color in this figure legend, the reader is referred to the web version of this article.)

[FIGURE]

This is done by highlighting the individuals and relations that characterize each error in a configuration. In Fig. 5: to explain error E1, the modeler highlights InvolvesDetective(CriminalInvestigation1,Person1) and InvolvesDetective(CriminalInvestigation0,Person0) in contrast with InvolvesSuspect(CriminalInvestigation1,Person1) and InvolvesSuspect(CriminalInvestigation0,Person0) ; to explain E2, the modeler highlights LeadDetective(Person1) and LeadDetective(Person2) in contrast with JuniorDetective(Person1) and JuniorDetective(Person2) , respectively. From each generated unintended configuration, the modeler can highlight multiple errors. Along with the errors highlighted in the unintended configurations, positive examples must be provided. These can be easily highlighted in the generated intended configurations or in the unintended configurations as well. The unintended configurations host, indeed, one or multiple errors, but may also host correct modeling examples. For instance, the relation '' Manages '', in the configuration represented by Fig. 5, occurs as a positive modeling example only.

The selection of the elements that characterize an error and the corresponding elicitation of the negative and positive examples should be systematically performed as specified by the algorithm presented in Listing 2.

The process described in Listing 2 can be iterated multiple times, for any given configuration and any given target predicate. Given multiple iterations, the final output is one single file, i.e., what we denote as 𝐸 -∕+ . This file collects multiple negative and positive examples, about the set of selected predicates, out of a list of intended and unintended configurations. In this setting, concerning the annotation process, there are some key observations:

- given an input configuration, the modeler can mark the target predicate as negative according to two main reasons: (i). because it must be associated with one element or more elements that are missing in the configuration; (ii). because it cannot be associated with one element or more elements that are present in the configuration. For instance, in Fig. 5, JuniorDetective(Person2) can be marked as negative because LeadDetective(Person2) is also present. Differently, Superintendent(Person2) can be marked as negative because LeadDetective(Person2) is present and SeniorDetective(Person2) is not;
- each configuration can be used to elicit multiple examples, for multiple predicates. In the example provided by Fig. 6 we have two examples for one target predicate, namely: (1) InvolvesDetective(CriminalInvestigation1,Person1)(-) ,
- highlighting a negative example for a target predicate means providing information about the configuration fragment involving the negative example. Fig. 6, for instances, shows the elements of the configuration represented in Fig. 5 to be highlighted in order to store meaningful negative examples for E1. Here the target negative predicates, which are marked with ''-'' are two occurrences of '' InvolvesDetective ''. To highlight the error, the related conflicting predicates '' InvolvesSuspect '', marked as ''+'', must also be provided;

## Listing 2: Elicitation Process.

```
negative as ''+''; positive as ''+'';
```

```
Result: Negative/Positive examples file 𝐸 -∕+ 1 get the list of configurations ; 2 for configuration 𝐶𝑛 in the list do 3 if 𝐶𝑛 is intended then 4 store 𝐶𝑛 as intended configuration 𝐶 𝑖 𝑛 ; 5 else 6 store 𝐶𝑛 as unintended configuration 𝐶 𝑢 𝑛 ; 7 end 8 end 9 for configuration 𝐶 𝑗 𝑛 do 10 for predicate p in 𝐶 𝑗 𝑛 do 11 if p is negative then 12 mark p as ''-''; 13 mark elements in 𝐶 𝑗 𝑛 making p 14 store information in 𝐸 -∕+ ; 15 end 16 if p is positive then 17 mark p as ''+''; 18 mark elements in 𝐶 𝑗 𝑛 making p 19 store information in 𝐸 -∕+ ; 20 end 21 end 22 end
```

Fig. 6. Eliciting two negative examples for the '' InvolvesDetective '' target predicate.

[FIGURE]

InvolvesSuspect(CriminalInvestigation1,Person1)(+) and (2) InvolvesDetective(CriminalInvestigation0,Person0)(-) , InvolvesSuspect(CriminalInvestigation0,Person0)(+) ;

- given an input configuration, the modeler can highlight a positive example for a target predicate following two main approaches: (i). proactively , namely by providing information about the exact fragment involving the positive example; (ii). passively , namely, by just marking the target predicate as positive and leaving all the connected predicates as positive. In the configuration provided in Fig. 7, for instance, given the target predicate '' InvolvesDetective '', three positive examples are proactively provided, by selecting the element(s) to be associated with (see the occurrence of '' InvolvesSuspect '', which, in this case, is associated to a different person). Differently, adopting the passive approach, the modeler can just mark the '' InvolvesDetective '' occurrences as positive and keep all the other predicates as positive, since there is no conflict

Fig. 7. Eliciting three positive examples for the '' InvolvesDetective '' target predicate.

[FIGURE]

generating errors. In this second scenario, the fragment for eliciting the positive examples will account for all the elements in the configuration depicted in Fig. 7;

- the ways (''proactive'' or ''passive'') of annotating examples depend primarily on what the modeler wants to avoid in the model. These two kinds of annotation affect the output of the learning process. For instance, if the modeler provides positive examples for '' InvolvesDetective '' as from Fig. 7, the output rule will involves the highlighted predicates only (e.g., InvolvesDetective and InvolvesSuspect ). Differently, if the modeler elicits positive examples from all the graph elements represented in Fig. 7, the learned rule may involve other (potentially useless) predicates that are present in the graph (e.g., Manages or IsLedBy ).

The above-introduced annotation (a.2) and elicitation (b.2) steps will be supported by an ad-hoc editor. The plan is to employ the capabilities embedded in the OntoUML editor [41], with some additional features, like, for instance, enabling users to efficiently browse the configurations, annotate them, keeping track of all the elicited examples and generate the required 𝐸 -∕+ file as final output.

## 4.3. Induction

The third step in our approach is the induction phase (see (3) in Fig. 3), which is aimed at addressing the target goal of this paper, namely learning a set of candidate constraint rules, to be used then for repairing the input conceptual model. This phase, similarly to the previous phases (see (1) and (2) in Fig. 3), consists of a transformation task (3.a in Fig. 3) and the application of a learning algorithm (3.b in Fig. 3). The learning process (3.b) is performed by exploiting the ProbFOIL [24] 13 functionalities. The transformation step (3.a) is aimed at generating the files required by ProbFOIL out of the data produced through the previous steps of the framework.

By means of (3.a) the 𝐸 -∕+ file produced through the assertion phase and the predicates of the input conceptual model involved in the annotated configurations are taken as input. The files generated out of this step are: (1) a .settings file encoding key information about the predicates to be learned, and (2) a .data file encoding elicited neg/pos examples. These files are required for the activation of the next phase of the process, which consists of setting up and applying the ProbFOIL ILP algorithm.

<!-- formula-not-decoded -->

[FIGURE]

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

An illustrative example of the .settings file generated by reusing (part of) 14 the predicates of the conceptual model represented by Fig. 1, is showed by (1), (2) and (3) above. The specifications are divided in three main parts, namely type definitions , mode declarations and target predicate .

Type definitions. These play a central role to capture the base model structure and predicates needed for the learning task, where a unary predicate can be defined as base(classname(x)) ; a binary predicate can be defined as base(predicatename(x,y)) and so forth. In (1) types definitions for the predicates Person , Witness , Interrogation , ConductedBy and Questions are provided.

Mode declarations. These are used to define how variables can occur in the learned rules. In the adopted set-up, mode declarations take the form of mode(predicatename(ModeType, ModeType, . . . ) . ''predicatename'' is where the name of the predicate that can be used in the rule is provided. ''ModeType'' is used to specify if: (i). the variable for the given predicate cannot be free in the output rule (in this case the ModeType symbol is '' + ''); (ii). the variable for the given predicate is free in the output rule (in this case the ModeType symbol is '' -''). In (2) examples of mode types for the predicates Interrogation and Questions are provided.

Target predicate. These denote the goal of the learning task and they are specified in the form learn(predicate/arity) . Notice that in our approach the target predicate selection can be automated. That is, we are able to learn every predicate that has a negative example in the input .data file. Moreover, each target predicate, once selected, must be excluded from the mode declarations. In (3) an example of target for the predicates ConductedBy is provided.

<!-- formula-not-decoded -->

Along with the .settings file, a .data file, encoding the 𝐸 -∕+ file produced in the assertion phase, generated. This is in order to capture all the information about the elicited examples. An illustrative example of the .data file generated by reusing part of the conceptual model represented by Fig. 1 is shown by (4). The file contains examples elicited from one intended configuration and examples derived from two unintended configurations. The target predicate that can be selected from here is '' conductedby ''.

Each record represents an assertion (i.e., an ''example'', in the ILP jargon) that is encoded in the configuration produced by Alloy and stored in the 𝐸 -∕+ file. Negative examples are specified by adding zero-probability facts, e.g.: 0.0::conductedby(x1, y1) . This way of highlighting the negative examples depends on the fact that ProbFOIL accounts for probabilistic learning (to each example a probability weight can be added, from 0 to 1).

The main steps involved in the above-described transformation process are represented by Listing 3. Notice that before generating the final .settings file, a version without target predicates is generated out of the input conceptual model. This intermediate version is then tuned according to the information encoded by the related .data file, which is needed to address the target learning task. 15

14

The scripts we used to generate and are available at: https://github.com/unibz-core/ConstraintLearning. Notice that, currently, the only manual step performed was the generation of the final .settings file out of the intermediate .settings and .data files.

Notice that the examples are partial, in a real-world scenario the modes and types cover all the predicates that are present in the input conceptual model. 15 .settings .data

```
Result: .settings and .data files 1 get input conceptual model ; 2 get the 𝐸 -∕+ file ; 3 for input conceptual model 𝑀 do 4 generate types definitions t ; 5 generate mode declarations d ; 6 store .settings file; 7 for negative and positive examples in 𝐸 -∕+ do 8 generate annotated assertions 𝐴 ; 9 store .𝑑𝑎𝑡𝑎 file; 10 for negative assertion 𝑎 - ∈ .𝑑𝑎𝑡𝑎 do 11 create target predicate p ; 12 update .settings file; 13 end 14 end 15 end
```

Listing 3: Transformation Process.

## 4.3.1. Rules learning

Once the .settings and the .data files are produced we set up the ILP pipeline in order to address a constraint learning task (see (3) in Fig. 3). On top of the adaptation of the concept learning problem provided in Section 2.1 we model this task as follows:

<!-- formula-not-decoded -->

with 𝐸 + and 𝐸 -being a set of positive and negative examples, respectively, elicited via model simulation and encoded as .data file assertions; with M being the involved base predicates of the input source conceptual, encoded by the .settings file; and with H being a constraint axiom hypothesis which entails all the positive and none of the negative examples.

In our current setting we map the constraints axiom hypothesis H that can be learned into two main types of clauses [42]:

- horn clauses , namely a disjunction of literals with at most one positive literal, e.g.: 𝑎 ∨¬ 𝑏 ∨¬ 𝑐 ∨¬ 𝑑 ∨ ... ∨¬ ℎ , which can be mapped into ( 𝑏, 𝑐, 𝑑, … , ℎ ) → 𝑎 ;
- goal clauses , namely a a horn clause with no positive literals, e.g.: ¬ 𝑎 ∨¬ 𝑏 ∨¬ 𝑐 ∨¬ 𝑑 ∨ ... ∨¬ ℎ , which can be mapped into ¬( 𝑎, 𝑏, 𝑐, … , 𝑑 ) .

We use these formulas to cover, in practice, different types of constraints, that we categorize as follows: (i). constraints by implication , namely repairing solutions that maps into horn clauses ; (ii). constraints by negation or integrity constraints , namely, repairing solutions that maps into goal clauses , and (iii). meta-constraints , namely repairing solutions that can map into either horn clauses or goal clauses , but that are aimed at constraining n-ary predicates, with 𝑛 &gt; 1 with meta-properties, like reflexivity , symmetricity or transitivity .

To handle constraints by negation and meta constraints, we adopted a customization of ProbFOIL, which, with the standard set-up, has the same limitations as Prolog in handling some types of rules [37] (see, for instance, goal clauses formulas).

Learning goal clauses. In order to learn goal clauses, we adopt the following approach. Suppose that the example .data file in (6) is generated, in order to learn a constraint for the target predicate '' questions/2 '':

<!-- formula-not-decoded -->

By running the learning task, the output rule would be:

<!-- formula-not-decoded -->

meaning by this that: ForAll A and B , Questions(A,B) is true if not ConductedBy(A,B) . Even if the provided examples capture exactly the inconsistency to be forbidden (namely, the fact that Questions and ConductedBy cannot share the same source and target at the same time), the output learned rule does not prevent this situation. Moreover, this rule is a precise example of indefinite clause , namely a clause with at list two positive literals ((7), can be read as '' Questions(A,B) or not(ConductedBy(A,B)) ''.

Thus, whenever we have an indefinite clause as output rule, we rise the negation in the body to the head of the rule. This can be easily generated by leveraging the same annotation provided by the modeler. The only difference is that each negative assertion for a given predicate, will be transformed into a positive assertion for the negation of that predicate, and, uniformly, each positive assertion for the same predicate will be transformed into a negative assertion for the negation of that predicate. 16

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

(8) encodes an example of how (6) can be straightforwardly transformed. (9) shows how (7) is transformed by rising the ''not'' to the head of the clause. Notice that, as anticipated above, this can be easily automated by running a simple command, for instance: '' if the learned output rule is an indefinite clause then raise the ''not'' from body to head ''. Moreover, as anticipated, this does not affect the annotation feedback provided by the modeler.

Learning meta-constraints. In order to learn meta-constraints we adopt the following approach. Suppose that we need to learn the property of being symmetric for the binary predicate TeamsUp , as from Fig. 1. This rule can be written in prolog as:

<!-- formula-not-decoded -->

This rule can be learned by generating a copy for the target predicate in the ProbFOIL set-up, for which we need to learn the meta-constraint. For instance, from teamsup(x,y) we generate teamsup\_(x,y) . This copy will be added in the .setting file, as mode declaration and type definition, and in the .data file as an assertion.

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

(11) is an example of .data file and examples to learn a symmetric property for the predicate TeamsUp . (12) represents the learned rule. Notice that we adopted this customization in order to facilitate the meta-constraints learning task and to handle recursive rules. As reference ILP approach for meta-interpretive learning we followed the work in [45].

Thus, whenever the modeler has to learn a meta-constraint, the task will be enabled by simply generating copies of the target predicate in the .setting and the .data files.

## 4.4. Repair

In the final phase, the rules derived through the learning task, through the induction phase, can be assessed by the modeler that can decide to apply them over the source conceptual model (see (4) in Fig. 3). Notice that a full exploitation of the repair phase is out of the scope of this paper. However, it can be observed that: (i). the application of the rules requires another key transformation step, namely from the Prolog-like language to the input conceptual modeling language; (ii). the repair task can be run automatically, by using ad-hoc ILP theory revision approaches [46,47].

## 5. Validation

## 5.1. An anti-patterns catalog as a litmus test

To validate that our approach can learn relevant constraints that are likely to be needed in practice, we use, as a ''litmus test'', 17 the catalog of empirically-elicited ontological anti-patterns developed for OntoUML [12,49-51]. That is, we verify if we can automatically learn the repair suggestions embedded in some of these anti-patterns.

16 It is worth noticing that the solution we adopted can be partially grounded on the research work about NEG raising and negative inversion , see for instance [43,44]. However, a detailed discussion of the theoretical foundation of these choices is out of the scope of this paper.

17 A litmus test is ''a critical indicator of future success or failure''. To say that A is a litmus test for B means that A can be effectively used to measure some property of B [48].

## 5.1.1. Methods and materials

As the basis of our test 18 we used the input model specified in Fig. 1 and we grouped all the errors that are admitted by that model into a set of ontological anti-patterns,

Ontological anti-patterns are syntactically valid but error-prone patterns recurrently found in conceptual models. They are errorprone in the sense that they are likely to cause a mismatch between the conceptualization one intended to capture and that which is actually formalized in one's model. Such mismatches include, for instance, all the under-constraining issues we discussed in Sections 2 and 4.1, but also issues related to over-constraining.

The anti-pattern catalog works well as a litmus test for our approach because it has been empirically developed by analyzing over 50 OntoUML models, many of which developed in industrial and research projects. This means that it allows us to demonstrate two properties about the constraints our approach can learn. First, that they are relevant, i.e., modelers would actually want to add them to their models. Second, that they are likely to be needed, as many of the anti-patterns occurred in more than 70% of the models analyzed in a study [12].

For each identified anti-pattern, and corresponding error, we added a fact in the alloy specifications of the model in Fig. 1. This was in order to constrain the model and being able to produce intended configurations. For instance, to avoid E4 (see Section 4.1) we added the following fact:

<!-- formula-not-decoded -->

We then generated a set of configurations through the Alloy analyzer either by keeping all the constraints, in order to generate intended configurations or by negating some of the constraints, in order to generate unintended configurations. After this step we generated the 𝐸 -∕+ file following the process described in Section 4.1, as from Listing 2. We then created the .settings and the .data file by running the transformation process described in line 3. As result, we collected 8 configurations, with 2 intended configurations (i.e, containing only correct examples) and 6 unintended configurations hosting multiple errors. The output .data generated out of these configurations was then composed by 75 assertions, where 17 were marked as negative and 58 were marked as positive, for a total amount of 12 predicates (7 of which were used as a target).

Finally, we defined the goal of this validation as learning from the given .settings and .data files the constraints that are needed to avoid the following identified anti-patterns:

Association Cycle (AssCyc) . An anti-pattern characterized by a set of 𝑛 classes (where 𝑛 &gt; 1) connected through 𝑛 links, i.e. associations or generalizations, such that they form a cycle (in the traditional graph-theoretical sense). AssCyc is associated to two refactoring plans:

- (i) require open cycles at the instance-level;
- (ii) require closed cycles at the instance-level;

An occurrence of AssCyc in our running example consists of the classes Interrogation , Witness , and CriminalInvestigation , as well as the associations Questions , InvolvesWitness , and ContributesTo . Another occurrence consists of Interrogation , Detective , CriminalInvestigation , ConductedBy , InvolvesDetective , and ContributesTo . In both cases, we always want closed cycles.

Relator Mediating Overlapping Types (RelOver) . An anti-pattern characterized by a relator (a reified relationship) that connects overlapping classes (i.e. classes that may have common individuals in their extensions). RelOver is associated to two refactoring plans:

- (i) make the overlapping classes exclusive in the context of the relator, i.e. forbid that, for any given instance of the relator, one individual is involved in it different ways;
- (ii) make the overlapping classes disjoint, i.e. make the intersection of the extension of these types an empty set;

There are two RelOver occurrences in our criminal investigation model. One characterized by the relator Interrogation and the overlapping classes Detective and Witness , and another characterized by the relator CriminalInvestigation and the overlapping classes Detective , Witness , and Suspect . Both occurrences would be fixed by adding an exclusivity constraint to the model, thus prohibiting that one interrogates oneself, as well as one investigates and serves as a witness against oneself. A disjointness constraint is not applicable in these cases because we want the model to allow people to play the role of detective in one context and of suspect in another.

Relation Specialization (RelSpec) . An anti-pattern characterized by two associations, 𝑎 and 𝑏 , and classes 𝐴 1 , 𝐴 2 , 𝐵 1 , and 𝐵 2 , such that: (i) 𝑎 connects 𝐴 1 to 𝐴 2 ; (ii) 𝑏 connects 𝐵 1 to 𝐵 2 ; (iii) 𝐴 1 = 𝐵 1 or 𝐵 1 is a subclass of 𝐴 1 ; and (iv) 𝐴 2 = 𝐵 2 or 𝐵 2 is a subclass of 𝐴 2 . RelSpec is associated with three refactoring plans, namely:

- (i) a subsetting constraint requiring that if 𝑏 holds between two individuals, 𝑎 must also hold (but not the other way around);
- (ii) a redefinition constraint requiring that if 𝑏 holds between two individuals, 𝑎 must also hold, and also the other way around (i.e., if 𝑎 then 𝑏 );

18 For sake of reproducibility, all the experiment files we produced and the procedures we followed are available at https://github.com/unibz-core/ ConstraintLearning.

(iii) a disjoint constraint requiring that if 𝑏 holds between two individuals, 𝑎 cannot also hold between them.

A RelSpec occurrence in our running example is characterized by the association InvolvesDetective , which holds between CriminalInvestigation and Detective , and IsLedBy , which holds between CriminalInvestigation and LeadDetective . In this case, the model lacks an association inclusion constraint, so that it would not be possible for a detective to lead an investigation she is not involved in.

Binary Relation Between Overlapping Types (BinOver) . An anti-pattern that occurs when an association connects two classes that constitute an overlapping set. BinOver involves that the same individual instantiates both targets of the relationship and can be associated with two refactoring plans:

- (i) specify binary association properties, like reflexivity, transitivity and symmetry;
- (ii) enforce disjointness, namely, make the related types disjoint by the specification of a disjoint generalization set.

A BinOver occurrence in our running example is characterized by the association TeamsUp , which has JuniorDetective has source and target. In this case, the model allows for a JuniorDetective that teams up with him/herself and lacks meta-constraints to enforce the relationship to be symmetric.

Relation Composition (RelComp) . An anti-pattern that consists of two distinct associations, A and B, which connect A-Source to A-Target and B-Source to B-Target, respectively. RelComp occurs when the following conditions hold: (a). B-Source is equal to or is a subtype of A-Target and B-Target is equal to or is a subtype of A-Target; (b). B-Source is equal to or is a subtype of A-Source and B-Target is equals to or is a subtype of A-Source. This anti-pattern is associated to the following refactoring plans:

- (i) Existential composition. For every distinct individuals x , y , if x is related to y through B, it implies that x and y are related to at least one common individual through relation A;
- (ii) Right Universal Composition. For every distinct individuals x , y , if x is related to y through B, it implies that all z that is connected to x , through A, is also connected to y , through A;
- (iii) Left Universal Composition . For every distinct individuals x , y , if x is related to y through B, it implies that all z that is connected to y , through A, is also connected to z , through A;
- (iv) Forbidden Composition. For every two distinct individuals x , y , if x is related to 𝑦 through B, it implies that x and y are connected to no individual in common through A;
- (v) Custom Existential Composition. For every distinct individuals x , y , if x is related to y through B, it implies that x and y are connected to [less than/more than/exactly] n common individuals through A.

The RelComp occurrence in our criminal investigation model is characterized by the Manages and the TeamsUp relations, where the source of TeamsUp is equal the target of Manages and the target of TeamsUp is equal to the target of Manages .

Deceiving Intersection (DecInt) . This anti-pattern occurs when a type, specializes in two or more concrete types giving to the modeler the false impression that the extension of that type is identical to the intersection of the extension of its multiple supertypes. The refactoring plans for this anti-pattern are as follows:

- (i) deleting and/or inverting one or more generalizations;
- (ii) creating a constraint to specify that the specializing type is derived by the intersection of the two (or more) parent types.

In our criminal investigation model, DecInt occurs with the specialization of the type Superintendent , which is subsumed by LeadDetective and SeniorDetective , thus allowing, for instance, for individuals that are SeniorDetectives ad LeadDetectives but not Superintendents .

## 5.1.2. Results

By running the ProbFOIL algorithm for each predicate marked as negative in the input .data file, we produce a set of candidate repairing solutions, or constraints, as output. In what follows we list the learned constraints and we group them in relation to the corresponding anti-patterns we used as a litmus test, by also discussing when needed, the possibility to learn other refactoring plans (which are not required by the model we used for the test) involved by the given anti-pattern.

## (a.0) AssCyc learned constraint.

<!-- formula-not-decoded -->

where the formula should read as: Forall A, B and C , InvolvesWitness(A,B) is true if both ContributesTo(C,A) and Questions(C,B) are true.

Here the elicited negative examples were three instances of the InvolvesWitness predicate: one being not associated with a ContributesTo predicate, the other two being associated to a Interrogation that Questions a different Witness .

(a.1) AssCyc learned constraint.

<!-- formula-not-decoded -->

where the formula should read as: Forall A, B and C , IsLedBy(A,B) is true if both ContributesTo(C,A) and ConductedBy(C,B) are true.

Here the elicited negative examples were three instances of the is led by predicate: one being not associated with a ContributesTo predicate, the other two being associated to a Interrogation that is ConductedBy a different LeadDetective .

Notice that a.0 and a.1 are two examples of closed cycle refactoring plan . Similarly, the open cycle refactoring plan could also have been learned, by transforming an indefinite clause such as InvolvesWitness(A,B) :- ContributesTo(C,A), not(Questions(C,B)) , which can be derived with an annotation that is the inverse of the one used for the closed cycle refactoring plan . The ProbFOIL output for the open cycle refactoring plan would be transformed into ContributesTo(C,A) :InvolvesWitness(A,B), not(InvolvesWitness(A,B),Questions(C,B)) . 19

## (b.0) RelOver learned constraint.

<!-- formula-not-decoded -->

where the formula should read as: Forall A and B , ConductedBy(A,B) is not true if Questions(A,B) is true. Here the elicited negative example was just one instance of the ConductedBy predicate being associated with a Questions predicate having the same instance as a target. The constraint in (15) is an example of a goal clause that can be learned via the adaptation explained in Section 4.3.

## (b.1) RelOver learned constraint.

<!-- formula-not-decoded -->

where the formula should read as: Forall A and B , InvolvesDetective(A,B) is not true if InvolvesSuspect(A,B) is true. Here the elicited negative example was just one instance of the InvolvesDetective predicate being associated with a InvolvesSuspect predicate having the same instance as target. Again, the constraint in (16) is an example of goal clause that can be learned via the adaptation explained in Section 4.3.

The refactoring plans involving stronger constraints, namely making the two overlapping classes disjoint can be straightforwardly derived by learning, for instance, the following goal clauses: b.0 , not(Detective(A), Witness(A)) or b.1 not(Detective(A), Suspect(A)) .

## (c) RelSpec learned constraint.

<!-- formula-not-decoded -->

where the formula should read as: For all A and B , if IsLedBy(A,B) then InvolvesDetective(A,B) . Here the elicited negative examples were two instances of the InvolvesDetective predicate, both of them being associated with a IsLedBy predicate having the same source instance and different target instance (e.g., a detective leading an investigation of which they are not involved). This allowed us to learn the rule addressing the refactoring plan expressed by (i) in Section 5.1.1. The refactoring plan expressed by (iii) can be addressed by learning rules that are similar to the open cycle plan for the AssCyc anti-pattern.

## (d) BinOver learned constraint.

<!-- formula-not-decoded -->

The rules in (18) are derived by the following output: TeamsUp(A,B) :- TeamsUp\_(B,A) not(TeamsUp\_(A,A)) . This can be converted by applying the steps described in Section 4.3 and in the above AssCyc Open Cycle explanation. Here the formula should read as: For all A and B , if TeamsUp(B,A) is true if TeamsUp(A,B) is true, and TeamsUp(A,A) and TeamsUp(A,B) cannot be both true.

19 This formula is derived by applying the following conversion steps: (a) InvolvesWitness(A,B) :- ContributesTo(C,A), not(Questions(C,B)) ; (b) InvolvesWitness(A,B) :-not(not(ContributesTo(C,A)) or Questions(C,B)) ; (c) not(InvolvesWitness(A,B)) :-(not(ContributesTo(C,A)) or Questions(C,B)) ; (d) (not(InvolvesWitness(A,B)) or ContributesTo(C,A)), (not(InvolvesWitness(A,B)) or not(Questions(C,B))) .

Here the elicited negative examples were two instances of the TeamsUp predicate, one having a junior detective as a target that is not also a source in the same relation; the other having the same junior detective as source and target.

Notice that in this case we learned two meta-constraints, i.e., symmetry and anti-reflexivity, but other meta-constraints can also be learned, see for instance transitivity (e.g., TeamsUp(A,B) :- TeamsUp\_(A,C), TeamsUp\_(C,B) ), or reflexivity (e.g., TeamsUp(A,B) :- TeamsUp\_(A,A) ).

## (e) RelComp learned constraint.

<!-- formula-not-decoded -->

where the formula should read as: Forall A, B and C , Manages(A,B) is true if both TeamsUp(B,C) and Manages(A,C) are true or if both TeamsUp(C,B) and Manages(A,C) are true.

Here the elicited negative examples were two instances of the Manages predicate, one being associated with the source of the corresponding TeamsUp predicate, the other being associated only to the target of the corresponding TeamsUp predicate.

Notice that the above learned rule can account for the refactoring rule expressed by (ii), i.e., the right universal composition and (iii) the left universal composition . The current set-up can also account for (iv), namely the forbidden composition , by applying a transformation of an indefinite clause, like in the example provided for the AssCyc open cycle refactoring plan. 20 Differently, with the current set-up, the refactoring rules for existential composition (i) and custom existential composition (v) cannot be learned, because of some limitations related to the adopted Prolog-like language. In Section 6.2 we will provide more details about this particular issue.

## (f) DecInt learned constraint.

<!-- formula-not-decoded -->

where the formula should read as: Forall A , Superintendant(A) is true if LeadsDetective(A) is true and SeniorDetective(A) is true.

Here the elicited negative examples were two instance of the Superintendent predicate, one being associated to LeadsDetective only, the other one being associated only to SeniorDetective .

## 5.2. Performance test

To check the practical feasibility of our approach we also tested the proposed set-up against different volumes of data. A future application scenario of our approach could, indeed, leverage a much larger amount of (possibly contrasting) annotation feedback from multiple users.

## 5.2.1. Methods and materials

We organized the test in four trials, namely: the baseline trial (0) , where we selected as input the 8 configurations and the 75 assertions (unary and binary predicates stored in the .data file) used to derive the rules as from the previous experiment (see the previous subsection); trial (1) where the input was composed by 15 configurations for a total of 277 assertions; trial (2) where the input is composed by 24 configurations for a total of 563 assertions; trial (3) where the input is composed by 31 configurations for a total of 1044 assertions.

To run the experiment we used a MacBook Pro (Retina, 13-inch, Early 2015) with CPU 2,7 GHz Intel Core i5. 21 We set up ProbFOIL by adopting the default beam size 22 5 and random seeds [53] 10. All the used data sets can be found at https://github.com/unibzcore/ConstraintLearning. We then run the algorithm and we checked its performance in terms of time and accuracy 23 of the derived rules.

## 5.2.2. Results

Table 1 summarizes the data collected by running the four trials, by providing the accuracy of the learned rule, the number of rule evaluations and the number of (neg/pos) examples involved. The results are grouped per type of anti-pattern.

20 In this specific case the output rule would have been '' Manages(A,B) :- not(TeamsUp(C,B)) or Manages(A,B) :- not(Manages\_(A,C)) '', which can be transformed as '' not(Manages(A,B)) :-TeamsUp(C,B) or not(Manages(A,B)) :-Manages\_(A,C) '', which is equivalent to '' not(Manages(A,B), Manages\_(A,C), TeamsUp(C,B) ''.

[21 https://support.apple.com/kb/SP715.](https://support.apple.com/kb/SP715)

22 The ProbFOIL algorithm executes a rule search, starting from the input data and identifying a set of best candidate rules. The beam size parameter is used to determine the number of best rules to be kept as candidates, thus controlling the computational complexity of the rules search. For more info about this measure in the context of ILP the reader is referred to [52].

23 As the sum of all the true positive examples and all the true negative examples divided by all the examples. For more information, we refer the reader to [54].

Table 1

Experiment data overview.

|   Trial |   Accuracy |   Rule evals |   Time (s) |   Examples |   pos |   neg |
|---------|------------|--------------|------------|------------|-------|-------|
|       0 |          1 |           78 |       3.59 |          5 |     1 |     4 |
|       1 |          1 |          112 |       6.06 |         14 |    10 |     4 |
|       2 |          1 |          814 |      42.52 |         17 |    15 |     2 |
|       3 |          1 |          900 |      50.78 |         22 |    15 |     7 |
|       0 |          1 |          170 |       7.80 |          7 |     3 |     4 |
|       1 |       0.93 |          368 |      19.01 |         18 |    14 |     4 |
|       2 |       0.92 |          743 |      45.01 |         26 |    18 |     8 |
|       3 |       0.94 |         2342 |     180.57 |         34 |    26 |     8 |
|       0 |          1 |           50 |       2.29 |          6 |     5 |     1 |
|       1 |          1 |           73 |       4.16 |         23 |    20 |     3 |
|       2 |          1 |           73 |       4.56 |         26 |    23 |     3 |
|       3 |          1 |           73 |       4.81 |         35 |    30 |     5 |
|       0 |          1 |          160 |       7.10 |          4 |     2 |     2 |
|       1 |          1 |          475 |      31.23 |         34 |    26 |     8 |
|       2 |          1 |          896 |      60.50 |         49 |    39 |    10 |
|       3 |          1 |          983 |      89.70 |         67 |    51 |    16 |
|       0 |          1 |          160 |       7.10 |          4 |     2 |     2 |
|       1 |          1 |          475 |      31.23 |         34 |    26 |     8 |
|       2 |          1 |          896 |      60.50 |         49 |    39 |    10 |
|       3 |          1 |          983 |      89.70 |         67 |    51 |    16 |
|       0 |          1 |          155 |       7.39 |          7 |     5 |     2 |
|       1 |       0.85 |          179 |       7.44 |         27 |    21 |     6 |
|       2 |       0.89 |          193 |       8.20 |         37 |    31 |     6 |
|       3 |       0.84 |          203 |       8.83 |         49 |    39 |    10 |
|       0 |          1 |          314 |      13.92 |          4 |     2 |     2 |
|       1 |          1 |          522 |      27.09 |         24 |    22 |     2 |
|       2 |       0.76 |          859 |     115.10 |         34 |    24 |    10 |
|       3 |       0.82 |         1136 |     175.10 |         46 |    36 |    10 |
|       0 |          1 |           62 |       2.80 |          3 |     1 |     2 |
|       1 |          1 |          118 |       6.10 |         14 |     9 |     5 |
|       2 |          1 |          455 |      23.36 |         17 |    12 |     5 |
|       3 |          1 |          455 |      26.77 |         24 |    16 |     8 |

One first observation is that the amount of data needed to identify the target constraints is potentially very small. Trial 0 shows how 8 configurations are enough to derive all the rules with 100% of accuracy, by consuming a trifling amount of time. Still, this is possible if the annotation process is very precise and in our case, this was biased by the fact we knew in advance the rules to be learned. One second observation is that, as expected and showed by trials (1), (2), and (3), by improving the number of examples the algorithm takes more time to learn the rule. However, the consumed time is still reasonable, even with the maximum amount of assertions, for the more complex rules (see, for instance, AssCyc and RelComp ). Similarly, the accuracy of the learned rules can be sometimes affected by the noise introduced with new annotations. Finally, it is worth noticing how the performance trend is similar for each rule to be learned, even if there can be of course variations depending on the number of examples collected for the target predicate and the predicates involved for composing the rule. Fig. 8 provides a focus on the data collected by Table 1, by showing how the amount of input data affects the time performance for each learned rule.

## 5.3. Threats to validity

In what follows, we propose a set of validity threats that may affect the validation of our constraint learning approach.

These threats are mainly concerned with the generalization of the observed results to a real-case scenario and can be described as follows:

- No accounting for random annotation. In this experiment, we only learned rules we knew we wanted beforehand. The errors we found in the configurations were generated by knowing in advance the rules to be learned. In this phase, the focus was on checking whether the given approach is valid in learning the selected repairing solutions. In order to check the types of rules that can be learned, their level of complexity, and their practical utility, when the modeler does not know in advance the required output, an experiment considering a larger population of modelers and, possibly, a larger set of conceptual models should be conducted.
- No accounting for data growing size. This item is partially related to the previous one. Our final goal is to implement this approach and make it usable by teams of engineers that may vary in size and complexity. Therefore, the approach must be evaluated across a breadth of annotation data sets, both varying in size and complexity, to provide a precise assessment of the limits of the new technique.

Fig. 8. Performance trends: x axis provides the number of assertions for each learned rule; y axis provides the time taken by the algorithm, in seconds , to learn the rule.

[FIGURE]

- Lack of algorithm comparison. In the experiment we did not compare the observed results with what could be obtained by using alternative ILP algorithms. Before selecting the ProbFOIL algorithm we went through an analysis of multiple available options in the context of ILP and we based our selection on the comparison of the algorithms run in the related seminal papers. In any case, we recognize that the approach could potentially benefit from assessing different algorithms in terms of what types of rules can be learned (or not) and how efficiently they can be learned. We intend to do this as future work after gathering more data from concrete models in different domains.

## 6. Discussion

We believe that the approach proposed here amounts to a novel strategy for conceptual model (re)design by supporting: (i). the automated visualization of the (model-theoretical) semantics of a conceptual model; (ii). the judgment of intended/unintended cases put forth by modelers; (iii). constraint learning automated techniques. Moreover, regarding (ii) , it is important to highlight that this annotation/judgment task is done in a non-disruptive way as a by-product of performing a model validation task. This is key given that the difficulty in curating the databases of positive/negative examples has been one of the biggest impediments to the use of ILP in practical cases.

In the sequel, we discuss the implications of this novel approach. Moreover, by identifying the limitations of our current setting, we also discuss opportunities for future work.

## 6.1. Implications

The first central implication is that the proposed approach can support the modelers in better exploiting the analysis they run with the model-finding model simulator. Indeed, by collecting and annotating the configurations generated through the application of the model finder, a large data set of intended/unintended model instances can be generated, and then (re-)used to derive possible repair options. This can be taken as a backup facility that allows storing and keeping track of information that may be lost during the run-time analysis.

Secondly, another key point is that, by enabling modelers to generate populated models with a related set of elicited negative/positive examples, the proposed framework paves the way to a large number of case studies, especially on the application of different learning approaches, to identify constraints, or to address other tasks that can support the conceptual modeling activities (like for instance the identification of unintended instances across models, exploiting the annotation of previous activities). In the current setting, we adopted one single algorithm, but the same algorithm can be tuned in multiple ways and can produce different kinds of outputs. A benchmark of the available technologies and the possible configurations is out of the scope of this paper, but it is still a pivotal research issue, especially to check what kind of constraints can be learned and how easily they can be understood and reused to repair the model.

Thirdly, the approach we are proposing is compliant to both distributional and symbolic approaches to relational learning [55]. In the transformation step of the learning phase, indeed, we allow for different embedding approaches (e.g., propositionalization [56]). However, in the setting of this paper, we adopted ILP. This was primarily to show how the constraints learning task can leverage on even a very small amount of data. Similarly, and this is another key implication, relying on ILP allows inducing humanunderstandable logical rules. Still, this does not prevent us to exploit a much larger amount of data. Even just by applying the ProbFOIL ILP algorithm we selected, indeed, we can measure the accuracy of each derived rule, thus leveraging the feedback provided by multiple annotations and/or users.

Fourthly, the application of the automated steps of the framework, see for instance the conversion of the conceptual model into Alloy specifications, or the automatic identification of possible erroneous axioms, along with the suggestion of possible repair solutions, return to be useful allies in the conceptual modeling process. While they cannot be seen as alternatives to most of the modelers' activities, still they can be seen as useful means for improving the efficiency of some key steps. For instance, the modeler does not need to know how to encode her model into Alloy specifications, or she can start from a set of multiple repair suggestions, before deciding how to change the source model, this being particularly helpful in a scenario with very complex models, or involving non-expert (i.e., novice) modelers.

Finally, the overall framework was devised to address the full ontological semantics of the OntoUML (the simulation phase accounts for a full transformation of OntoUML models). In that sense, it makes it possible to leverage the existing OntoUML support for model validation via visual simulation in Alloy [12,18]. This feature is key to enable learning tasks over configurations structures that are recurrent in several OntoUML models as well as reusable cross-model rules that could rectify them.

## 6.2. Limitations

In order to achieve the goal of making the proposed approach usable by a large population of modelers and capable of learning all the repairing solutions that may be needed, with the current set-up, there is still a gap that needs to be bridged.

A first central issue is that for the generation of the constraint rules we are committed to a Prolog-like language and this prevents us from covering a full FOL expressivity. As we showed in Section 4.3 we already adopted a customization of the ProbFOIL set-up in order to extend the set of rules that can be learned, however, there are still some cases of non-horn formulas that we are not able to handle. Most of them involve the application of the existential quantifier in the head, for instance:

<!-- formula-not-decoded -->

∧ 𝐶𝑟𝑖𝑚𝑖𝑛𝑎𝑙𝐼𝑛𝑣𝑒𝑠𝑡𝑖𝑎𝑔𝑎𝑡𝑖𝑜𝑛 ( 𝐵 )

The above formula reads as ''every interrogation contributes to a criminal investigation'' and can be converted to horn form via skolemization [57] as follows:

<!-- formula-not-decoded -->

∧ 𝐶𝑟𝑖𝑚𝑖𝑛𝑎𝑙𝐼𝑛𝑣𝑒𝑠𝑡𝑖𝑎𝑔𝑎𝑡𝑖𝑜𝑛 ( 𝑐 ( 𝐴 ))

𝑐 ( 𝐴 ) is called skolem function and represents an artificial variable meaning, for instance, the ''the criminal investigation related to A'' by which ∃ 𝐵 can be eliminated and horn clause can be created. At the current state we are not able to learn the skolemized rules like the one represented by (23). Similarly, with the current set-up, we are not able to handle formulas with operators that can be useful for constraining cardinalities, like, for instance, equal , i.e., = , less-than-or-equal , i.e., =&lt; , or more-than-or-equal , i.e., &gt;= . These operators could be handled in the future by introducing user-defined predicates like eq/2 leq/2 or meq/2 , as suggested in [37].

Another relevant issue is that a full formalization and simplification of the process by which multiple model configurations are generated and negative/positive examples are elicited must be provided. This step is mandatory to enable the scalability of the approach and its application over conceptual models with a high level of complexity. Notice that the plan is to use an ad-hoc editor to support the whole process with the generation of the output files. In particular, we will employ the capabilities embedded in the OntoUML editor [41], with some additional features, like, for instance, (i). enabling users to efficiently browse the input conceptual models by also decomposing them into multiple sub-graphs; (ii). supporting an easy set-up of the scope of the simulations; (iii). allowing for the annotation of the generated outputs via simulation visualizer.

## 7. Related work

The contribution we present builds upon the research done in recent years on model validation [17] and constraint learning [28,29], with a particular focus on their application in conceptual modeling. These two research areas are very broad and have been addressed in the literature by a series of different approaches and techniques, with a huge amount of relevant results.

However, the scope of our proposal is much more restricted and, more precisely, is characterized by the challenge of leveraging the combination of two well-established technologies in the context of model validation and constraint learning, namely Conceptual Model Visual Simulation and Inductive Logic Programming . Additionally, the main goal is to offer practical support to modelers in the task of avoiding unintended simulations, thus designing more precise [58] conceptual models.

For these reasons, we selected here the works from the literature that share the most our concern, trying to address the same goal through similar approaches and techniques (see Table 2), i.e., by exploiting existing features derived by well-established research in model validation and constraint learning.

Model validation. Among the most relevant works in this direction, [18] proposed a solution to assess conceptual models defined in OntoUML by transforming these models into Alloy specifications. This approach is an essential step towards the application of model finding techniques to validate conceptual models designed through OntoUML. The main focus here is on the formalization of the translation of OntoUML into Alloy specifications and on the application of the Alloy analyzer to generate possible instantiations, and then check possible overconstraining and underconstraining issues.

Similarly, [11] devised a methodology to test the conceptual models semantic quality, in terms of correctness and completeness , which is based on the generation of automated conceptual test cases [59]. The main goal of this approach is to guide the modeler

## Table 2

Comparing our approach to related work: an exemplification. ''Approach'' returns the target reference work; ''Language'' is what is used to express the input models validated by the reference approach; ''Target'' refers to the type of issue addressed by the validation, i.e., underconstraining or overconstraining issues; ''Technology'' refers to the main technologies used by the validation approach; ''Problem'' stands for the method adopted for finding problems into the assessed model, which can be auto , manual or semi-auto ; ''Solution'' stands for the method adopted for finding the repairing solutions, and it has the same values of ''Problem'' ; ''Repair'' refers to the method adopted for repairing the model, and it has the same values of ''Problem'' .

| Approach   | Language       | Target     | Technology          | Problem   | Solution   | Repair    |
|------------|----------------|------------|---------------------|-----------|------------|-----------|
| [18]       | OntoUML        | Under/over | Alloy               | Semi-auto | Manual     | Manual    |
| [11]       | UML/OCL        | Under/over | CSTL [59]           | Semi-auto | Manual     | Manual    |
| [9]        | UML/OCL        | Under/over | USE                 | Semi-auto | Manual     | Manual    |
| [7]        | FOL            | Under/over | null                | Manual    | Manual     | Manual    |
| [60]       | UML            | Under      | Formula a           | Semi-auto | Manual     | Manual    |
| [10,12]    | OntoUML        | Under      | Alloy               | Semi-auto | Manual     | Manual    |
| [62]       | UML/OCL        | Under      | Genetic programming | Manual    | Auto       | Manual    |
| [64]       | UML/OCL        | Under      | UML2CSP [67]        | Manual    | Auto       | Manual    |
| [65]       | ER             | Under      | SAT                 | Semi-auto | Manual     | Manual    |
| [66]       | Temporal Logic | Over       | SAT/ILP             | Auto      | Auto       | Semi-auto |
| Us         | OntoUML/UML    | Under      | Alloy/ILP           | Semi-auto | Auto       | Manual    |

[a https://www.microsoft.com/en-us/research/project/formula-modeling-foundations/.](https://www.microsoft.com/en-us/research/project/formula-modeling-foundations/)

through an iterative UML/OCL models generation, by also exploiting the functionalities of an ad-hoc editing environment. The approach presented in [9] is also related to what we propose. Here the solution is based on the application of a system, namely the USE system, that allows for a model-driven validation of UML models and OCL constraints, by generating multiple instances of the model, or snapshots. These snapshots, like the Alloy simulations, can be then assessed by the modeler to detect overconstraining and underconstraining issues. Moreover, the USE system enables modelers in checking the models' properties, from a meta-level viewpoint, thus facilitating the detection of the flaws within the model structure.

The recent work described in [7], even if from a higher-level perspective, is related to our proposal as well. There, the main goal is to formalize the process by which modelers analyze and modify the model as a sort of ''dialogue'', which must be iterated in order to better identify and capture the final intended worldview. Their process can be taken as a way to improve the awareness of the modeler in designing her/his model in accordance with the final application goal. In that work, no particular tools or automatization methods are described and there is no focus on a specific modeling language. However, the authors provide a comprehensive high-level analysis of the validation process to be run by modelers, in order to address underconstraining and overconstraining issues.

Our approach is also in line with the representative work discussed in [10,12], where the key goal is to efficiently identify recurrent error-prone structures across conceptual models and then manually uncover possible missing constraints.

Constraint Learning. In this respect, of direct relevance to our effort on using the validation process to then infer model constraints is also the work in [60]. This approach aims at identifying and solving possible (UML) model design flaws, by exploiting model finding and adopting constraint logic [61]. Similarly, the work in [62] proposes a genetic programming algorithm [63] in order to generate Object Constraint Language (OCL) invariants from examples. Moreover, the work in [64] proposes an approach to infer OCL invariants from valid/invalid snapshots by checking the relevance of the generated outputs. Another work that is close in spirit to ours is discussed in [65], where a technique for supporting engineers in the definition of constraints for Entity-Relationship (ER) models is provided. From a broader perspective, we consider of direct relevance also the research in [66] by Alrajeh and colleagues, who proposed an approach to automatically diagnose and repair temporal logic software specifications based on the integration of model checking and machine learning .

Compared to these pivotal works, the main differences in our approach are the following: (i) we employ ILP (as opposed to the Constraint Satisfaction Problem (CSP) algorithm, as, e.g., in [64]) to address the constraint learning problem. As discussed in [68], there might be some relevant advantages in addressing constraints induction problems from an ILP perspective; (ii) we support multiple representational languages for the input conceptual model to be assessed and repaired, namely, OWL, UML, and OntoUML (approaches like the ones present in [63,64], for instance, account for UML models only). In fact, our aim is to build an infrastructure for learning: (a) ontological constraints such as the ones expressible in OntoUML [22]; (b) anti-patterns for that language [12]; (iii) we provide a set-up of the model finding facility that can be used to curate a database of positive and negative examples for conceptual models, covering different application domains. In fact, our approach seamlessly leverages and extends on the existing methodological and computational support for model validation via visual simulation (visual model finding) provided by the OntoUML toolset [18,69]. In that sense, it requires less intrusive manual interventions for eliciting and curating examples and counterexamples than, for instance, [64].

## 8. Conclusion

In this paper, we presented a theoretical framework to combine visual model finding (or visual model simulation) and ILP, in order to support automated model validation and repair. We presented a practical solution to generate and exploit multiple configurations for any given (Onto)UML conceptual model, thus allowing its analysis and annotation. Finally, we provided an approach to learn constraints from the annotated configuration outputs. All the adopted data and processes are available at https://github.com/unibz-core/ConstraintLearning respectively.

While our work is inscribed in the general line of recent efforts that aim at improving (ontology-driven) conceptual modeling diagnosis and repair, we also consider it as a starting point for the investigation of the influence of machine learning approaches and model finding techniques on model validation.

Based on the presented results, as future work, we plan to evaluate our constraint learning approach over different OntoUML models, thus uncovering also recurrent errors across models and related constraints. This involves both practical and theoretical research that examines the impact of various algorithms on the learning goal, as well as the generation of a data set of annotated configurations coming from different OntoUML models.

We focus here on OntoUML models because it is a goal of our research program to learn constraints and anti-patterns that reflect the ontological semantics and expressivity of this language. However, most of our results henceforth can also benefit standard UML models. For example, with the exception of the RelOver anti-pattern (which involves relators and explicitly modeled existential dependence relations), all the other anti-patterns discussed here can also be manifested in standard UML class diagrams.

## 8.1. Future perspectives

Applying the presented framework over OntoUML configurations, and implementing it into a usable and scalable application is our long-term objective and it triggers the agenda for immediate future work. In order to achieve this goal, with the current set-up, there are still some gaps that need to be bridged.

Firstly, we intend to evolve of the elicitation and learning processes to learn constraints that can be transported to multiple conceptual models. This will involve the generation of a single .settings files containing mode declaration and type definitions for the OntoUML basic constructs. Moreover, all the domain information encoded in the .data files derived by the configuration annotations of each domain conceptual will need to be mapped to the same basic OntoUML constructs.

Learned meta-constraint example.

<!-- formula-not-decoded -->

As an example in this research path, the formalism in (12) represents the meta-constraint for solving the AssCyc anti-pattern. According to this pattern, mediation relations must form a cycle (i.e., starting from every 𝑇𝑦𝑝𝑒 𝑛 , one can navigate the mediation relations and arrive back to the same type using every relation exactly once). Future work will address efficient derivation of rules of this kind from a large set of conceptual models and by implementing an abstraction procedure that will allow us to map domain information into the OntoUML constructs. It is important to notice that our proposed framework already fully addresses the ontological semantics of OntoUML, since the simulation phase accounts for a full transformation of OntoUML models. This makes it possible to easily leverage the existing OntoUML support for model validation via visual simulation in Alloy [12,18]. This feature is key in enabling learning tasks over recurring structures across several OntoUML models, as well as reusable cross-model rules that could rectify them.

Another central point, which is a key objective in our immediate future plan, is to apply the framework in an open scenario, where several people simulate the same model and provide multiple annotation feedback, possibly diverging on what they assign as intended and unintended configurations. This paves the way to several case studies and would then offer a way to support the modelers with multiple options, suggesting to them how often people chose each of the options. This is about repairing a particular model by learning from a collective judgment (in this case, a type of meaning negotiation activity).

A further objective, which cannot be addressed with the current set-up, is to generate refactoring plans by encoding the output constraint rules into OCL specifications, thus enabling the automatic repair of the input conceptual model. With the current set-up, the learned constraints can be taken as repair suggestions, to be assessed by the modeler and, eventually, manually added to the source model. Although this allows for a more accurate refinement process, the automatic implementation of repair suggestions can be used to increase the efficiency of the engineering process. In this regard, we are already testing Theory Revision and ILP algorithms , see for instance FORTE [46] and ProPPR [47] which will enable us automate the repairing process.

Finally, another goal will be to exploit the amount of data generated through the annotation process in order to enable predictive tasks, where for instance the annotation from the modelers can be used as training data to identify error-prone structures or 'suspicious' instances. This will involve a deeper assessment and understanding of the currently available approaches ( distributional or symbolic ) to relational learning [55].

## Declaration of competing interest

The authors declare that they have no known competing financial interests or personal relationships that could have appeared to influence the work reported in this paper.

## Acknowledgments

This research is partially funded by the Foundations of Next-Generation Ontology-Driven Conceptual Modeling (NeXON) project CUP: I54I19001060005, sponsored by UNIBZ, Italy, and by the Pattern-Based Approach for the Engineering of Large-Scale Knowledge Graphs in the Risk Management Domain (RiskGraph) project, sponsored by Accenture Israel Cybersecurity R&amp;D Lab.

## References

- [1] [G. Guizzardi, Theoretical foundations and engineering tools for building ontologies as reference conceptual models, Semantic Web 1 (1, 2) (2010) 3-10.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb1)
- [2] F. van Harmelen, A. ten Teije, Validation and verification of conceptual models of diagnosis, in: Proceedings of the Fourth European Symposium on the Validation and Verification of Knowledge Based Systems (EUROVAV'97), 1997, pp. 117-128.
- [3] [M. Kayama, S. Ogata, K. Masymoto, M. Hashimoto, M. Otani, A practical conceptual modeling teaching method based on quantitative error analyses for novices learning to create error-free simple class diagrams, in: 2014 IIAI 3rd International Conference on Advanced Applied Informatics, IEEE, 2014, pp. 616-622.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb3)
- [4] [M. Poveda, M.C. Suárez-Figueroa, A. Gómez-Pérez, Common pitfalls in ontology development, in: Conference of the Spanish Association for Artificial Intelligence, Springer, 2009, pp. 91-100.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb4)
- [5] [M.L. Brodie, J. Mylopoulos, J.W. Schmidt, On Conceptual Modelling: Perspectives from Artificial Intelligence, Databases, and Programming Languages, Springer Science &amp; Business Media, 2012.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb5)
- [6] L. Burgueño, A. Vallecillo, M. Gogolla, Teaching UML and OCL models and their validation to software engineering students: an experience report, Comput. Sci. Educ. 28 (1) (2018) 23-41.
- [7] M. Grüninger, Ontology validation as dialogue, in: A. Barton, S. Seppälä, D. Porello (Eds.), Proceedings of the Joint Ontology Workshops 2019, Vol. 2518, CEUR-WS, 2019.
- [8] H. Mumtaz, M. Alshayeb, S. Mahmood, M. Niazi, A survey on UML model smells detection techniques for software refactoring, J. Softw. Evol. Process 31 (3) (2019) e2154.
- [9] M. Gogolla, F. Büttner, M. Richters, USE: A UML-based specification environment for validating UML and OCL, Sci. Comput. Program. 69 (1-3) (2007) 27-34.
- [10] [G. Guizzardi, T.P. Sales, Detection, simulation and elimination of semantic anti-patterns in ontology-driven conceptual models, in: E. Yu, G. Dobbie, M. Jarke, S. Purao (Eds.), Conceptual Modeling. ER 2014, in: Lecture Notes in Computer Science, vol. 8824, Springer, Cham, 2014, pp. 363-376.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb10)
- [11] [A. Tort, A. Olivé, M.-R. Sancho, An approach to test-driven development of conceptual schemas, Data Knowl. Eng. 70 (12) (2011) 1088-1111.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb11)
- [12] T.P. Sales, G. Guizzardi, Ontological anti-patterns: Empirically uncovered error-prone structures in ontology-driven conceptual models, Data Knowl. Eng. 99 (2015) 72-104.
- [13] [J. Guerson, J.P.A. Almeida, G. Guizzardi, Support for domain constraints in the validation of ontologically well-founded conceptual models, in: Enterprise, Business-Process and Information Systems Modeling, Springer, 2014, pp. 302-316.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb13)
- [14] [E.M. Clarke Jr., O. Grumberg, D. Kroening, D. Peled, H. Veith, Model checking, MIT Press, 2018.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb14)
- [15] [S. Abburu, A survey on ontology reasoners and comparison, Int. J. Comput. Appl. 57 (17) (2012).](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb15)
- [16] W.J. Thong, M.A. Ameedeen, A survey of UML tools, in: Proceedings of the International Conference on Data Engineering 2015 (DaEng-2015), Springer, 2019, pp. 61-70.
- [17] [D. Jackson, Software Abstractions: Logic, Language, and Analysis, MIT Press, 2012.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb17)
- [18] [A.B. Benevides, G. Guizzardi, B.F.B. Braga, J.P.A. Almeida, Validating modal aspects of OntoUML conceptual models using automatically generated visual world structures, J. UCS 16 (20) (2010) 2904-2933.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb18)
- [19] [M. Nickel, K. Murphy, V. Tresp, E. Gabrilovich, A review of relational machine learning for knowledge graphs, Proc. IEEE 104 (1) (2015) 11-33.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb19)
- [20] M. Fumagalli, T.P. Sales, G. Guizzardi, Towards automated support for conceptual model diagnosis and repair, in: International Conference on Conceptual Modeling, Springer, 2020, pp. 15-25.
- [21] [M. Fumagalli, T.P. Sales, G. Guizzardi, Mind the gap!: Learning missing constraints from annotated conceptual model simulations, in: IFIP Working Conference on the Practice of Enterprise Modeling, Springer, 2021, pp. 64-79.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb21)
- [22] [G. Guizzardi, Ontological Foundations for Structural Conceptual Models, Telematica Instituut / CTIT, 2005.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb22)
- [23] L. De Raedt, A. Kimmig, H. Toivonen, ProbLog: A probabilistic prolog and its application in link discovery, in: Manuela M. Veloso (Eds.), Proceedings of 20th International Joint Conference on Artificial Intelligence (IJCAI), 2007, pp. 2462-2467.
- [24] L. De Raedt, A. Dries, I. Thon, G. Van Den Broeck, M. Verbeke, Inducing probabilistic relational rules from probabilistic examples, in: Proceedings of the Twenty-Fourth International Joint Conference on Artificial Intelligence, 2015, pp. 1835-1843.
- [25] A.J. Simons, C.A. Fernandez-y Fernandez, Using alloy to model-check visual design notations, in: Sixth Mexican International Conference on Computer Science (ENC'05), 2008, pp. 121-128.
- [26] [D. Jackson, Alloy: a language and tool for exploring software designs, Commun. ACM 62 (9) (2019) 66-76.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb26)
- [27] [G. Guizzardi, C.M. Fonseca, A.B. Benevides, J.P.A. Almeida, D. Porello, T.P. Sales, Endurant types in ontology-driven conceptual modeling: Towards OntoUML 2.0, in: J.C. Trujillo, et al. (Eds.), Conceptual Modeling, Springer, 2018, pp. 136-150.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb27)
- [28] [L. De Raedt, A. Passerini, S. Teso, Learning constraints from examples, in: S.A. McIlraith, K.Q. Weinberger (Eds.), Proceedings of the Thirty-Second AAAI Conference on Artificial Intelligence, AAAI Press, 2018, pp. 7965-7970.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb28)
- [29] [T.M. Mitchell, Machine Learning, McGraw-Hill New York, 1997.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb29)
- [30] [M. Verdonck, F. Gailly, Insights on the use and application of ontology and conceptual modeling languages in ontology-driven conceptual modeling, in: International Conference on Conceptual Modeling, Springer, 2016, pp. 83-97.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb30)
- [31] [N. Guarino, G. Guizzardi, ''We need to discuss the relationship'': Revisiting relationships as modeling constructs, in: International Conference on Advanced Information Systems Engineering, Springer, 2015, pp. 279-294.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb31)
- [32] A. Andoni, D. Daniliuc, S. Khurshid, D. Marinov, Evaluating the ''small scope hypothesis'', Technical Report, Computer Science and Artificial Intelligence Laboratory, MIT, USA, 2003.
- [33] D. Jackson, C.A. Damon, Elements of style: Analyzing a software design feature with a counterexample detector, IEEE Trans. Softw. Eng. 22 (7) (1996) 484-495.
- [34] L. Gammaitoni, P. Kelsen, Q. Ma, Agile validation of model transformations using compound F-alloy specifications, Sci. Comput. Program. 162 (2018) 55-75.
- [35] M. Roberson, M. Harries, P.T. Darga, C. Boyapati, Efficient software model checking of soundness of type systems, ACM Sigplan Notices 43 (10) (2008) 493-504.
- [36] A. Cropper, S. Dumančić, Inductive logic programming at 30: a new introduction, 2020, arXiv preprint arXiv:2008.07912.
- [37] [T. Frühwirth, Theory and practice of constraint handling rules, J. Logic Program. 37 (1-3) (1998) 95-138.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb37)
- [38] [S.M. Shah, K. Anastasakis, B. Bordbar, From UML to alloy and back again, in: S. Ghosh (Ed.), Models in Software Engineering. MODELS 2009, in: Lecture Notes in Computer Science, vol. 6002, Springer, 2009, pp. 158-171.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb38)
- [39] G. Guizzardi, T.P. Sales, J.P.A. Almeida, G. Poels, Automated conceptual model clustering: a relator-centric approach, Software and Systems Modeling (2021) 1-25.
- [40] [G. Figueiredo, A. Duchardt, M.M. Hedblom, G. Guizzardi, Breaking into pieces: an ontological approach to conceptual model complexity management, in: 2018 12th International Conference on Research Challenges in Information Science (RCIS), IEEE, 2018, pp. 1-10.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb40)
- [41] [J. Guerson, T.P. Sales, G. Guizzardi, J.P.A. Almeida, Ontouml lightweight editor: a model-based environment to build, evaluate and implement reference ontologies, in: 2015 IEEE 19th International Enterprise Distributed Object Computing Workshop, 2015, pp. 144-147.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb41)
- [42] [A. Horn, On sentences which are true of direct unions of algebras, J. Symbolic Logic 16 (1) (1951) 14-21.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb42)

- [43] [L. Haegeman, Negative preposing, negative inversion, and the split CP, Negation Polarity (2000) 21-61.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb43)
- [44] [C. Collins, P.M. Postal, Classical NEG Raising: An Essay on the Syntax of Negation, Vol. 67, MIT Press, 2014.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb44)
- [45] A. Cropper, S.H. Muggleton, Metagol system, 2016, https://github.com/metagol/metagol.
- [46] [B.L. Richards, R.J. Mooney, First-order theory revision, in: Machine Learning Proceedings 1991, Elsevier, 1991, pp. 447-451.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb46)
- [47] [V. Guimarães, A. Paes, G. Zaverucha, Online probabilistic theory revision from examples with ProPPR, Mach. Learn. 108 (7) (2019) 1165-1189.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb47)
- [48] [Collins, Litmus test, 2021, https://www.collinsdictionary.com/dictionary/english/litmus-test, Accessed in 2021-04-02.](https://www.collinsdictionary.com/dictionary/english/litmus-test)
- [49] [T.P. Sales, G. Guizzardi, Anti-patterns in ontology-driven conceptual modeling: The case of role modeling in ontouml, in: A. Gangemi, P. Hizler, K. Janowicz, A. Krisnadhi, V. Presutti (Eds.), Ontology Engineering with Ontology Design Patterns: Foundations and Applications, in: Studies on the Semantic Web, IOS Press, 2016, pp. 161-187.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb49)
- [50] [T.P. Sales, G. Guizzardi, ''Is it a fleet or a collection of ships?'': Ontological anti-patterns in the modeling of part-whole relations, in: Advances in Databases and Information Systems. ADBIS 2017, Vol. 10509, Springer, 2017, pp. 28-41.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb50)
- [51] [T.P. Sales, G. Guizzardi, Ontological anti-patterns in taxonomic structures, in: J.P.A. Almeida, M. Bax, R. Berardi, F. Baião (Eds.), XII Seminar on Ontology Research in Brazil. Ontobras 2019, Vol. 2519, CEUR-WS, 2019.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb51)
- [52] [N. Lavrač, S. Džeroski, M. Numao, Inductive logic programming for relational knowledge discovery, New Gener. Comput. 17 (1) (1999) 3-23.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb52)
- [53] [I. de Castro Dutra, D. Page, V.S. Costa, J. Shavlik, An empirical evaluation of bagging in inductive logic programming, in: International Conference on Inductive Logic Programming, Springer, 2002, pp. 48-65.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb53)
- [54] [A. Gunawardana, G. Shani, A survey of accuracy evaluation metrics of recommendation tasks, J. Mach. Learn. Res. 10 (12) (2009).](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb54)
- [55] S. Dumancic, A. Garcia-Duran, M. Niepert, A Comparative study of distributional and symbolic paradigms for relational learning, in: Proceedings of the Twenty-Eighth International Joint Conference on Artificial Intelligence, 2019.
- [56] [N. Lavrač, B. Škrlj, M. Robnik-Šikonja, Propositionalization and embeddings: two sides of the same coin, Mach. Learn. 109 (7) (2020) 1465-1507.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb56)
- [57] [J. Hsiang, M. Srivas, Automatic inductive theorem proving using prolog, Theoret. Comput. Sci. 54 (1) (1987) 3-28.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb57)
- [58] [N. Guarino, D. Oberle, S. Staab, What is an ontology? in: Handbook on Ontologies, Springer, 2009, pp. 1-17.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb58)
- [59] [D. Janzen, H. Saiedian, Test-driven development concepts, taxonomy, and future direction, Computer 38 (9) (2005) 43-50.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb59)
- [60] [B. Pérez, I. Porres, Reasoning about UML/OCL class diagrams using constraint logic programming and formula, Inf. Syst. 81 (2019) 152-177.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb60)
- [61] [J. Jaffar, M.J. Maher, Constraint logic programming: A survey, J. Logic Program. 19 (1994) 503-581.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb61)
- [62] M. Faunes, et al., Automatically searching for metamodel well-formedness rules in examples and counter-examples, in: Proc. MODELS 2013, 2013, pp. 187-202.
- [63] [S. Mirjalili, Genetic algorithm, in: Evolutionary Algorithms and Neural Networks, Springer, 2019, pp. 43-55.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb63)
- [64] [D.-H. Dang, J. Cabot, On automating inference of OC constraints from counterexamples and examples, in: Proc. KSE 2015, Springer, 2015, pp. 219-231.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb64)
- [65] [S. Hartmann, S. Link, T. Trinh, Constraint acquisition for entity-relationship models, Data Knowl. Eng. 68 (10) (2009) 1128-1155.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb65)
- [66] [D. Alrajeh, J. Kramer, A. Russo, S. Uchitel, Automated support for diagnosis and repair, Commun. ACM 58 (2) (2015) 65-72.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb66)
- [67] J. Cabot, R. Clarisó, D. Riera, UMLtoCSP: a tool for the formal verification of UML/OCL models using constraint programming, in: Proceedings of the Twenty-Second IEEE/ACM International Conference on Automated Software Engineering, 2007, pp. 547-548.
- [68] [L. De Raedt, et al., Learning constraint satisfaction problems: An ILP perspective, in: Data Mining and Constraint Programming, Springer, 2016, pp. 96-112.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb68)
- [69] [C.M. Fonseca, T.P. Sales, V. Viola, L.B.R. Fonseca, G. Guizzardi, J.P.A. Almeida, Ontology-driven conceptual modeling as a service, in: 11th International Workshop on Formal Ontologies Meet Industry (FOMI'21), CEUR-WS, 2021.](http://refhub.elsevier.com/S0169-023X(22)00043-X/sb69)

Mattia Fumagalli is a postdoctoral researcher at the CORE: Conceptual and Cognitive Modeling Research Group at the Free University of Bozen-Bolzano, where he is also a teaching assistant for the Information Systems Design and IT Management and Enterprise Modeling courses. He is also working with the Knowdive Group at the Department of Information Engineering and Computer Science of the University of Trento, where he was (from 2015 to 2019) a teaching assistant for the Mathematical Logics and Knowledge-Data Integration courses.

He has a Master's Degree in Philosophy and a Ph.D. in Computer Science. His research concerns primarily Artificial Intelligence, with a particular focus on the combination of Knowledge Representation, Data Mining, and Machine Learning techniques. Other key research interests include Logic and Philosophy of Mind. With an interdisciplinary research approach, on the border between computer science, AI, philosophy and cognitive science, he is currently investigating how we can get closer in developing systems that bridge the gap between today's state-of-the-art in AI and Human-level intelligence.
