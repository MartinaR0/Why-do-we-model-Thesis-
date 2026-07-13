[FIGURE]

## Handling Crimes of Omission by reconciling a criminal core ontology with UFO

Cleyton Mário de Oliveira Rodrigues a , b , ∗ , Camila Bezerra b , Fred Freitas b and Italo Oliveira c

a University of Pernambuco, Garanhuns-PE, Brazil

E-mail: cleyton.rodrigues@upe.br

b Center of Informatics, Federal University or Pernambuco, Recife-PE, Brazil

E-mails: camila.bezerra.br@gmail.com, fred@cin.ufpe.br

c Center of Legal Sciences, Federal University or Pernambuco, Recife-PE, Brazil

E-mail: italojsoliveira1@gmail.com

Abstract. Whereas ordinary legal documents are deployed as text documents for human consumption, AI &amp; LAW focuses on tackling the challenges surrounding the development of legal ontologies to assign meaning to legal provisions. We have witnessed an explosion of legal domain (and application) ontologies loosely based on sustainable theories, harming reusability. Fortunately, foundational ontologies foster interoperability between these domain ontologies, providing context-independent concepts that are usable and reusable across multiple domains. In particular, legal ontologies require this 'conciliation' with other foundational ontologies, given the inherent heterogeneity of the domain, such as the criminal domain. This paper describes a core legal ontology, built top-down from the UFO foundational ontology, engineered using the positivist legal theory of Hans Kelsen, fostering reusability across a plurality of the criminal field. The UFO proposal makes it possible to evaluate and leverage the conceptual quality of class hierarchies and concept taxonomies through stereotyped modeling primitives and constraints. The latter regulates how the primitives can be combined to support the design of ontologically well-founded conceptual models. This study was conducted to further highlight the depiction of Crimes of Omission, which have not yet been properly explored in the available literature. Although the conceptualization is tied directly to the Brazilian legal domain, it can be applied, with slight adaptations, to other legal systems around the world that follow the Roman-Germanic (or Civil Law) system and Kelsen's legal theory. Through these ontologies, it is possible to perform lawsuit simulation, such as the identification of a crime and imposition of penalties. At the end of this paper, we detail these possibilities for future work.

Keywords: AI &amp; Law, Legal Ontology, Criminal Domain, Foundational Ontology, Crimes of Omission

Accepted by: Chris Partridge

## 1. Introduction

Norms and standards regulating human society are pervasive in everyday life. Fundamental rights, such as life and personal liberty beyond the knowledge of what constitutes unlawful acts ensure that no ordinary citizen may refuse to comply with the law by claiming ignorance (expressed by the Latin maxim Nemo ius ignorare censetur (JURIS, 2018)). Gathering precedents, creating lines of argumentation, harmonizing and comparing regulations are all time and labor-intensive activities performed on a daily basis by legal professionals (lawyers, judges, legislators) around the world.

Demand for conceptual representations that tackle aspects that come into play when facing legal issues has increased. As the missing link between AI &amp; Law (Valente, 1994), (legal) ontologies are likely to be a global solution to handle a plethora of legal services, besides offering cost savings, high availability, flexibility of use, and platform independence. According to the 'level of generality' proposed by Guarino (1998), ontologies can be classified into different types, such as foundational, core, domain and application. In the order listed, the degree of ontological reusability decreases from more abstract concepts that can span a diversity of domains down to very specific application-focused concepts. In particular, a core ontology assures an intermediate view between general purpose foundational and domain ontologies: it restricts categories of a particular universe to an abstraction level that allows them to be reused across the domain. A core ontology is justified for indexing domain ontology libraries and providing a standard knowledge skeleton upon which to instantiate other conceptual models.

* Corresponding author. E-mail: cleyton.rodrigues@upe.br.

Legal systems are created and consolidated around historical, cultural, social and political issues. They accommodate a variety of legal phenomena described substantially through legal theories. Among others, the system proposed by positivist legal scholar Hans Kelsen stands out. Kelsen (1881-1973) proposed a very broad theory of law (Kelsen, 1949), where norms are rules that are either observed, violated, or that force people to perform desirable activities. Regardless of the specific legal system, crime can be defined as an action (or omission) that violates some state-protected good, culminating in a criminal sanction. The legal theory of crime (Greco, 2017) per se limits social reality by defining concepts, social roles, duties and obligations, normative descriptions, legal acts, and so on, inherited directly by the range of crime types. Crime theory is, therefore, the foundation of Criminal Law. Nevertheless, despite the principle of Nemo ius ignorare censetur , the various shortcomings of the legal context (inconsistencies, open-ended concepts, among others described in the semantic anomaly framework proposed by Freitas et al. (2011)) paradoxically prevent the lay citizen from fulfilling its purpose.

UFO (Unified Foundational Ontology) is an ontology (Guizzardi and Wagner, 2005) created from other foundational ontologies, such as the General Ontological Language/General Formal Ontology presented by Herre (2010) and the ontology of universals discussed by Guarino and Welty (2002), to fix the shortcomings and limitations of these earlier conceptual models. In addition, UFO has fostered conceptual model engineering as a theoretically sound discipline, gluing together several micro-theories on notions of conceptual modeling. UFO also provides stereotyped classes (kind, role, phase, among others) and constraints motivated by semantic considerations, which together provide a framework that supports the development of ontologically well-founded models.

The goal of this paper is to engineer a concise core ontology that does not over-constrain reality with unneeded axioms, focusing on tackling the challenges surrounding the Criminal and Positive Legal Theory. The proposed ontology is rooted in the UFO foundational ontology. Considering the general theory of crime as a core ontology, the specific crime types (crimes against life, patrimony or the environment, as well as extortion and corruption) are considered domain ontologies. In addition, the UFO primitive constructors and restrictions are utilized to explore a crime type that is little discussed in the literature: crimes caused by 'acts of omission'. We also provide a formal specification of conceptualizations through Description Logic (Baader et al., 2010) axioms, a family of formalisms (subset of First-Order Logic) for knowledge representation and reasoning, with remarkable expressiveness.

This study is organized as follows. In Section 2, we present UFO. The syntax and semantics of Description Logic is briefly presented in Section 3. Next, the criminal process according to the general theory of crime in Brazil is reviewed, with a special focus on crimes committed through inaction (thereafter referred to as crimes of omission). In Section 5, the criminal core ontology is presented. We further explore patterns (and anti-patterns) for this conceptual modeling. Details on the crimes of omission are presented in Section 6. Finally, some work related to the proposed study is discussed, concluding with some actual case studies extracted from local crime databases.

## 2. UFO: The Unified Foundational Ontology

Foundational (or upper-level) ontologies represent an overview of top-level, domain independent categories, from which tailored conceptual models can be built. From this perspective, foundational ontologies allow for a common shared vocabulary among the application models, permitting interoperability between them.

The UFO (Guizzardi and Wagner, 2004, 2005) emerged as a proposal to unify the General Ontological Language/General Formal Ontology (GOL/GFO, proposed by Herre, 2010) and the foundational ontology of universals underlying the OntoClean methodology discussed by Guarino and Welty (2002), in order to solve their limitations while inheriting their principal features. UFO provides a theory of ontological distinctions that addresses a typology of universals such as rigid sortal (kind, subkind), anti-rigid sortal (role, phase), and non-sortal dispersive types (category, mixin, and role-mixin), along with some constraints (e.g., a rigid type cannot be supertyped by an anti-rigid one) to regulate the conceptual modelling. Some of these universals are described in this paper. Nevertheless, it is not within the scope of this work to fully describe the conceptual modelling universals. For additional references, check the work by Guizzardi (2005). It has been suggested that models rooted in UFO favor ontological adequacy, that is, they have a higher degree of closeness with reality (Bringuente et al., 2011; Guizzardi et al., 2010). Since its inception, UFO continues to be widely used in a variety of domains (Detoni et al., 2017; Griffo et al., 2017; Poletaeva et al., 2017). In order to ensure proper formalization, this foundational ontology is based not only on Formal Ontology, but also on a number of other theories from Philosophical Logic, Language Philosophy, Linguistics, and Cognitive Psychology.

UFO is structured as three complementary parts: UFO-A, UFO-B and UFO-C. UFO-A describes the objects that persist throughout their lifetime, preserving their identity as a person, a book, and son on. These are known as Endurants . UFO-B handles events or Perdurants , i.e., things that 'happen in time', such as a musical concert, a business process, a game of chess, a crime, or a legal action. Finally, UFOC is the part built on top of the other two. It defines social entities, such as agents, goals, actions and commitments. Each UFO fragment is described in the following subsections. They are based mainly on the work of Guizzardi et al. (2008, 2013).

## 2.1. An ontology of endurants

Figure 1 shows a partial view of UFO-A. Moving downward from the top-most category ENTITY, UFO-A is specialized into two branches that tackle the 'Instance v. Type' duality, represented by PARTICULAR and UNIVERSAL categories, respectively. UNIVERSAL sets the patterns of features that are instantiated by PARTICULARS, each with its identifier. ENDURANTS are perennial particulars that exist as time passes. They can be existentially independent (SUBSTANCE) or exist only when associated with another particular (MOMENT). A notoriously complex type of ENDURANT is SITUATION, a portion of reality recognized as a whole, a state of affairs. In practice, situations are fulfilled by other endurants, including other minor situations. Dependent moment instances may be tied to either a single particular - INTRINSIC MOMENT -, or to an assortment of these: RELATOR.

Related to UNIVERSAL types, the subcategories of KIND, ROLE and PHASE also stand out. KIND is a rigid type, which means that it provides the essential property of instantiating imperiously in every situation. ROLE and PHASE are anti-rigid types. ROLE is instantiated only in certain contexts depending on a given relation, whereas PHASE is a type instantiated in a context dependent on an intrinsic property. RELATIONs are UNIVERSAL types that match other entities. This mediation can take place through a RELATOR (MATERIAL RELATION), or directly, without the intervention of any other individual, that is, the FORMAL RELATION.

Fig. 1. UFO-A: a sub-ontology of endurants (Guizzardi et al., 2008, 2013).

[FIGURE]

Fig. 2. UFO-B: a sub-ontology of perdurants (Guizzardi et al., 2008, 2013).

[FIGURE]

## 2.2. An ontology of perdurants

UFO-B holds entities that are framed by time intervals. Distinct viewpoints describe the ontology of perdurants (or EVENT), as highlighted by Guizzardi et al. (2008, 2013): the mereological structure of events, events as mappings from situation to situation, the participation of objects in events, the temporal ordering of events, and events as manifestations of objects dispositions (Fig. 2).

The mereological EVENT structure can be classified as either an ATOMIC EVENT or a COMPLEX EVENT. The latter case is an event that is an aggregation of two or more other events, which can be either atomic or complex themselves. Furthermore, events are changes of state of affairs. PARTICIPATION is a special type of EVENT involving the participation of Substantial.

## 2.3. A subontology of social entities

On top of the endurant and perdurant ontological categories, social entities are defined, known as UFO-C. In order to facilitate understanding, UFO-C has been separated into two complementary parts: the subontology for actions, objects, and agents, and the subontology for commitments, delegations, and intentions. In the UFO-C hierarchy displayed in Fig. 3, SUBSTANTIAL can be specialized into two disjoint categories: AGENT and (non-agentive) OBJECT, which are further specialized into physical and social entities. Although both can participate in arbitrary EVENTS (AGENT PARTICIPATION and OBJECT PARTICIPATION), unlike an inanimate OBJECT, an AGENT creates actions (AGENT CONTRIBUTION), usually driven by an intention or belief (or some other INTENTIONAL MOMENT).

SOCIAL AGENTS ensure a set of (SOCIAL OBJECT) rules/norms - a NORMATIVE DESCRIPTION which define SOCIAL ROLES. For example, a politically-organized community lives under the aegis of the State (an INSTITUTIONAL AGENT) which, through a cohesive and coherent system of legal norms, defines social roles, such as those of the plaintiff and defendant.

INTENTIONAL MOMENTS are intrinsic constituents of the AGENT, usually guided by GOALS (Fig. 4). These moments are properly separated into internal commitments (MENTAL MOMENT) or externalized through SOCIAL COMMITMENTS. In addition, actions are created in order to meet these pledges. A SOCIAL COMMITMENT involves at least two AGENTS: the one who signed the commitment, and the one for whom the commitment was secured. The former - the person committed - creates an internal commitment in order to accomplish the task while the claimant creates a SOCIAL CLAIM dependent upon the first. A SOCIAL RELATOR equalizes these moments, through mediation between both agents. In the aforementioned relation, the one who signs the commitment must create actions that seek to satisfy the objective. Another dual commitment/claim relation is made through the DELEGATION relationship. Whenever someone delegates something to a third party, the latter is the one who must make the commitment towards the intended purpose. In the model, this relationship is derived by the special SOCIAL RELATOR, DELEGATUM.

Fig. 3. UFO-C: a sub-ontology of agents, objects and actions (Guizzardi et al., 2008, 2013).

[FIGURE]

Fig. 4. UFO-C: a sub-ontology of commitments and intentions (Guizzardi et al., 2008, 2013).

[FIGURE]

## 3. Description Logic

Description Logics (DLs) are a set of knowledge representation formalisms, with support for reasoning tasks (Baader et al., 2010). DLs sublanguages are a well-behaved fragment of First-Order Logic (FOL) with 2 variables. Each sublanguage establishes a trade-off between expressiveness and reasoning complexity. For simplicity, we explore the language that comprises only the conjunction, disjunction, negation, existential and universal restriction constructors, known as Attributive Language with Complements ( ALC ). The syntax of ALC is arranged in terms of three pairwise disjoint finite sets of symbols: the set of concept names ( NC ), the set of role names ( NR ), and the set of individual names ( NI ). The grammar below defines the structure of ALC concept expressions:

<!-- formula-not-decoded -->

While the first rule defines the set of ALC concept expressions, the second defines the role expressions. We denote L as the set of ALC concepts. Concept constructors can be classified into Boolean constructs and relationship constraints. A DL knowledge base ( KB ) is structured in two components, KB := 〈 A , T 〉 , where:

- ∗ Concept inclusion, C ⊑ C ;
- T is the terminological axioms, in which, we find:
- ∗ Concept equivalence, C ≡ C .
- ∗ Concept assertions, C(NI) ;
- A is the assertional axioms, in which, we find:
- ∗ Role assertions, R(NI × NI) .

In addition, DL semantics assumes the Open-World Assumption (OWA) (Reiter, 1978). According to the OWA premise, given a state-of-affairs, the absence of information is treated as something unknown, unlike the Closed-World assumption (Imieli´ nski and Lipski, 1984; Reiter, 1978), where it is interpreted as negative information. OWA is the most reliable assumption for the representation of knowledge, whenever it is not possible to guarantee that all information has been provided, or have not been made available yet.

Baader et al. (2010) outlines the semantics of Classical DL in terms of first-order interpretations. An Interpretation ( I ) is a tuple 〈 /Delta1 I , · I 〉 , where /Delta1 I represents the non-empty set known as the domain of I , while · I is a function that maps concepts to subsets of /Delta1 I , relations to subsets of /Delta1 I × /Delta1 I and instances to elements of /Delta1 I .

Table 1 highlights the semantics for DL grammar constructors and TBox axioms, which are selfexplanatory. For a short and didactic introduction to DL and its applications, as well as semantics for remaining constructors (ABox), check additional reference (Baader et al., 2010).

From the definition of Interpretation in DL, we can sketch the basic tasks of reasoning over concept expressions:

Table 1 DL ALC Syntax × Semantics (Baader et al., 2010)

≡

=

|                             | Syntax   | Semantics                                            |
|-----------------------------|----------|------------------------------------------------------|
| Individuals Individual Name | a        | a I                                                  |
| Roles                       | R        | I                                                    |
| Atomic Role                 |          | R                                                    |
| Concepts                    |          |                                                      |
| Atomic Concept              | A        | A I                                                  |
| Intersection                | C ⊓ D    | C I ∩ D I                                            |
| Union                       | C ⊔ D    | C I ∪ D I                                            |
| Complement                  | ¬ C      | /Delta1 I \ C I                                      |
| Top Concept                 | ⊤        | /Delta1 I                                            |
| Bottom Concept              | ⊥        | ∅                                                    |
| Existential Restriction     | ∃ R.C    | { x ∈ /Delta1 I &#124; ∃ y, (x, y) ∈ R I , y ∈ C I } |
| Universal Restriction       | ∀ R.C    | { x ∈ /Delta1 I &#124; ∀ y, (x, y) ∈ R I ⇒ y ∈ C I } |
| TBox                        |          |                                                      |
| Subsumption                 | C ⊑ D    | C I ⊆ D I                                            |
| Equivalence                 | C D      | C I D I                                              |

- Concept Satisfiability : Given a concept C , C is satisfiable iff it admits a model. An interpretation I is a model of a concept C if C I ̸= ∅ ;
- Concept Subsumption : An interpretation I is a model of a general concept subsumption ( C ⊑ D ) if C I ⊆ D I .

## 4. Criminal process and Crimes of Omission

The ideas addressed in this manuscript are heavily compliant with the Civil Law, the legal system derived from the influence of late Roman law, Germanic culture, and the Napoleonic code, among others. As such, the primary source of the legal order is the laws (statutes), created by federal or regional legislative chambers. From the criminal law perspective, each law is made up of two well-defined parts: the behavior (the primary precept) and the sanction (or penalty, the secondary precept). Unlike the AngloSaxon system (in which Common Law prevails), a system governed by Civil Law is recognized as being organized into a state-affirmed hierarchy of regulations, which are applied mainly to concrete cases (and not inferred from them).

Law emerges as a social phenomenon. Living in society therefore requires the harmonious organization of a group of individuals, each with their own behavior. Through behavior, values such as respect, dignity, and citizenship are sought. As such, law becomes an instrument of social control, carried out by means of legal norms.

## 4.1. Criminal law

Criminal law refers to as the set of legal norms that define criminal offenses and establish penalties and security measures. Criminal law regulates State intervention, shifting power towards the application of sanctions or benefits in response to specific behaviors. It is legally arranged by the sovereign Federal Constitution (1988) and the Penal Code (Decree-Law 2848 dated 1940), having been renewed by Law 7209/1984.

Generally speaking, a crime is an (intentional) action or omission, prohibited by a law, potentially culminating in a sanction for the offender. In a more detailed view, provided by the analytical theory (Greco, 2017), a crime is a typical, unlawful, and culpable behavior. Typicality comes from the perfect match between the behavior and a well-defined type of crime. A behavior is unlawful if the violation does not occur under any condition that might overcome illegality (such as self-defense, compliance with legal duty, state of necessity, or regular exercise of rights). Finally, culpability is ensured by the criminal imputability of the offender.

The offender (active agent) must be a physical person and must meet certain conditions that guarantee rights and obligations under Criminal Law. Following the same line of thought, a person is said to be incapable when he or she either has not reached the age of majority or when he or she has certain mental disorders. Additionally, inanimate objects and irrational animals are criminally incapable entities. A victim (passive agent) is the one whose legal good (the object of the law, that is, goods of material or immaterial value, such as life, honor, patrimony, physical integrity, public peace, as well as the material objects themselves) was either injured or threatened.

## 4.2. Positivist Legal Theory of Hans Kelsen

ALegal Theory needs to accurately describe a legal framework, seeking a clear description for a set of legal phenomena arranged in a juridical system. Hans Kelsen (1881-1973) proposed a very broad theory of law that has been applied to many legal systems and is well-suited to the approach used in this paper. In particular, the legal ontology presented here can be seen in part as a formalization of some of the ideas introduced by Kelsen. These ideas will be reviewed, and their relation to this study will be described.

Kelsen's legal theory is positivist in the sense that it concerns positive law, in opposition to natural law: the characterization of a legal system depends on the presence of certain governance structures, not on the extent to which it satisfies ideals of justice or morality. The existence of law is one thing; its merit or demerit another. In other words, there is a clear distinction between what law is and what law should be, as highlighted by Green (2009). Legal positivism is considered almost common sense in the western legal community, despite the importance of the evaluation of law beyond itself. Therefore, the ontology presented here represents nothing about the merits of law, justice, or morality, making it legally positivist, as well.

As stated by Kelsen (1949) legal theory, law is understood to be a set of rules with a defined structure, forming a system. In a legal system, through the power of authority, legal norms validate other legal norms, creating a hierarchy of legal regulations. The validity of all norms is founded on another higher-level norm, and a norm should be compliant based on the authority of another. This creates a chain linking every norm to a hierarchically superior regulation (i.e., ordinary laws with respect to the Constitution) until reaching the top 'basic norm' ( Grundnorm ). This norm is considered to be above even the Constitution, but has only a hypothetical value and is not a legal norm per se , only being necessary to avoid what Kelsen regards as a conceptual error: logically inferring ought from is . The basic norm means something along the lines of 'the original constitution is to be obeyed'.

Kelsen also defends the idea that a legal norm has a hypothetical structure that can be described by the propositions of legal science. A legal norm is in essence a conditional rule where the antecedent is an infraction and the consequent is a sanction; in both cases, not necessarily limited to one. A sanction, in Kelsen's words (1949, p. 50), is provided by the legal order to regulate specific human behavior which the legislator considers to be desirable. A sanction is, therefore, a type of coercive act. The oldest type of sanction is that of punishment under criminal law. Nevertheless, there are other kinds, according to different domains of law such as specific civil sanction, civil execution, or forcible deprivation of property to provide reparation. An infraction, in Kelsen's definition (1949, pp. 54-55), is the behavior of the individual against whom the sanction has been applied. Therefore, as mentioned earlier, an infraction can be an action, but can also be an omission. In this view, a legal norm would have the following logical structure: (i 1 ∧··· ∧ in) → (s 1 ∨··· ∨ sn) . However, s must be understood deontically: if i , then should be s .

Typically, a norm prescribing a sanction aims to prohibit a behavior. However, there are also norms of obligation. Kelsen claims that an obligation can be defined as a prohibition, and vice versa. To obligate a behavior is the same as to prohibit the omission of the behavior. To prohibit a behavior is the same as obligating the omission of the behavior. In other words, if a law obligates a behavior P , the law is in fact sanctioning the omission of P . Whatever is not prohibited, is permitted. This is why sanction is a central feature of the concept of norm. Because it may sound strange to regard all norms as having a sanction, Kelsen explains that norms that do not themselves contain a sanction depend on others that have some type of explicitly declared punishment. These are called 'secondary norms' because they are not autonomous.

## 4.3. Crimes of Omission

Underlying theories of foundational ontologies focus almost exclusively on the conceptualization of actions performed intentionally to check whether an agent is ' ipso facto ' blameworthy. The representa- tion of omissions, or non-comissive behaviors, is usually not considered. Part of this lack stems from the difficulty in theorizing a shared conceptual foundation regarding what an omission is, and to what extent a non-action can be configured. This paper does not dwell deeply on philosophical issues, for example, whether not doing something should be considered properly an ordinary action or an absence of action (Clarke, 2012); nor on other subsidiary questions regarding the act of merely failing to do something (Bach, 2010). Conversely, a favorable, though non-unique, definition is presented for non-comissive criminal behaviors, using UFO as the foundation.

At any given moment, countless singular activities are not being performed. Some are not done because of lack of opportunity, others for lack of skills. The vast majority are cognitively unconscious until they are remembered (such as scratching your head). There are still more that are actively omitted. Defining the domain is challenging and still full of conceptual disagreements. It is important to consider where an omission is directly intertwined with an internal commitment on the part of the agent, such as a desire or an intention.

Facing this variety of interpretations, the conceptualization of the non-performance of an act must be narrowly tied to that referenced in legal theory. In order to ascribe responsibility, a predefined legal duty to act must be defined. Ability and opportunity are both essential parts of this conceptual framework.

Definition 4.1 (Omission) . Suppose an agent AG, and an action AC. AG omitted to perform AC iff (Kleinig, 1986):

- (i) AG did not do AC;
- (ii) AG had the opportunity to do AC;
- (iii) AG had the ability to do AC;
- (iv) AG had good reason to believe that he had the opportunity and ability to do AC; and
- (v) AC was reasonably expected of AG, because:
- AG, or those in AG's position, ordinarily do AC; or
- AG was obliged to do AC; or
- AG had a responsibility to do AC; or
- AC was in some other way morally required of AG.

The Brazilian Penal Code (Brasil, 1940) address offenses described by a negative behavior in two criminal categories (Greco, 2017, p. 227): when an agent has deliberately omitted a legal obligation (pure omission, such as in the omission of aid or in the abandonment of public employment), or when there is a transgression of a specific legal duty to prevent a certain result (felony omission, such as when a mother stops breastfeeding her child, causing its death). It has been suggested that the second type is more complete than the first, and that the roles established between the parties transcend the shallow regular civic duty of protection in a deeper relationship between the guarantor and the protected legal good. This duty of protection is not shared by everyone, but only by those who have the function of ensuring that the result does not occur. Furthermore, from a more subjective perspective, an internal commitment on the part of the active agent towards the outcome is equally expected. In this type, the presence of a result is mandatory.

Another point that deserves attention is that for pure crimes of omission there is an explicitly defined crime type in legal texts, that is, a typical prediction of behavior that must be imposed upon the agent. Among these crimes are omission of relief (article 135), material abandonment (article 244), intellectual abandonment (article 246), failure to notify illness (article 269), and prevarication (article 319). All of them are regularly described within the Penal Code (Brasil, 1940). On the other hand, felony crimes of omission are considered to be an open type, as there is no typical predicted behavior. The guarantor who fails in his duty to avoid the result, can be charged with carrying out a crime that is described as a commissive offense. For example, a mother who kills her own child at an early age and one who denies him food causing his death (omission) are involved in the same type of crime.

## 5. The Criminal Ontology

Before presenting the Criminal Core Ontology, some Competency Questions (CQs) that guided the engineering of the ontology are listed.

## 5.1. Competency questions

Given a list of scenarios related to a discourse domain, developers should be able to describe a set of competency questions (CQs) that can represent user demands and scope limits. These questions are usually written in controlled natural language and support the development process in two ways:

- By enabling the identification of CQs core elements (classes and instances) in advance and the relationships between them, in order to create the ontology vocabulary, and;
- By providing a simple means of verifying the satisfiability of requirements, either by knowledge retrieval or by entailment through axioms.

Several ontology development methodologies (Fernández-López et al., 1997; Hasse et al., 2008) propose the use of CQs as ontology requirements. Nevertheless, traditional methodologies do not describe how to use them. For instance, the process of checking fulfillment by the developed ontology via reasoning is neither well-documented, nor automated. CQs could play a crucial role in this scenario, because they consist of a set of questions stated and replied to in natural language, that the ontology must be able to correctly answer (Noy and Hafner, 1997). They play an important role both in the specification of requirements as well as in the evaluation phase of most ontology engineering methodologies.

A competency question can be shown as 〈 Q,σ 〉 such that Q is a query expressed in a formal language and σ is an answer to this query expressed as a variable substitution (Bezerra et al., 2013). In addition, a competency question 〈 Q,σ 〉 is satisfied by an ontology O if O ∪ Q | = σ . According to Ren et al. (2014), the answers to these questions range from the short and direct ones (such as classes or instances) to formal axioms. In dealing with semantically complex ontologies, for example, separating CQs as such assures a more appropriate understanding of the suitability of the engineered model. Thus, we have: (i) CQs which work on classes and their relations; (ii) decision problems expressed as CQs, which should be answered with a boolean value; (iii) CQs expressed in an interrogative form which works only on instances; and, (iv) CQs expressed in an interrogative form that works only on a set of axioms.

## 5.2. Competency questions for the Criminal Domain

Some competency questions for the criminal domain were created, to help in the specification of requirements as well during the validation phase. Some CQs, specified according to the types considered, appear below.

## · CQs over classes:

- ∗ CQ1 : Which types of objects are present in an infraction? The answer to this question, according to the criminal ontology is 'Material Object, Abstract Object'. In this case, the answer corresponds to a set of entities;
- ∗ CQ2 : How many parties have a criminal norm? Two: behavior (the actual fact) and sanction. This competency question is related to a cardinality restriction in the ontology;
- ∗ CQ3 : In which cases can an agent not be penalized criminally? Answer: Mental Illness and Underage;
- ∗ CQ4 : What are the types of Norms? Answer: Incriminating and Non-Incriminating (or Justifying Norm);
- ∗ CQ5 : What types of qualified situations exist? Answer: Forbidden, Permitted and Mandatory;
- ∗ CQ6 : How many main types of sanction are there in the criminal area? Answer: Three: Fine, Restriction of rights and Deprivation of liberty;
- ∗ CQ7 : What are the principal doctrines for breaking up potential conflicts between criminal rules? Answer: Lex Specialis, Lex Posterior and Lex Superior ;
- ∗ CQ8 : What identifies a Felony crime of omission? Answer: Agent has power to act and is responsible for the victim (Guarantor), Mandatory situation, Specific Duty to Act (unfulfilled) and a Result;

## · Decision Problems:

- ∗ CQ9 : Can an agent be an offender and a victim of the same crime? The answer is 'No'. Here, the answer is dichotomous (yes or no);
- ∗ CQ10 : Does any legal act have an Intention as a cause? Answer: Yes;
- ∗ CQ11 : What is a Legal Norm? The answer is 'A Norm that defines the Deontic Qualification of a Situation'. This is a interesting answer to a competency question, because it is equivalent to a definition, which is represented by a set of axioms.
- CQ over axioms:

## 5.3. Axiomatizing the Criminal Domain

The axiomatization of the criminal domain is illustrated through UML notation, and formalized through DL axioms. Concepts are reified as UML classes, subsumption relations take the form of inheritance between classes, binary relations assume the role of UML associations, and instances are described through object diagrams. Figures 5 and 6 show the module with regard to the agents and the objects related to a legal scenario. We show stereotyped classes because we argue throughout this work on the use of patterns and anti-patterns grounded on UFO types (Guizzardi, 2005). Throughout this study, we present only a portion of the developed models/axioms. The full ontology (OntoCrime) can be found at https://github.com/cleytonrodrigues/Tese . Additional information on UFO concepts and stereotypes can be found at https://ontology.com.br/ .

LEGAL AGENT and LEGAL OBJECT are specialized (super) classes for the Law domain (based on the AGENT and OBJECT UFO-C concepts), which in turn are customized in criminal universe classes, namely CRIME AGENT and CRIME OBJECT, respectively. For any infraction, two roles are clearly delineated, the offender (ACTIVE AGENT) and the victim (PASSIVE AGENT). These roles do not overlap, but do not completely cover all possible entities. NATURAL PERSON represents a physical entity, achieved by specializing the PHYSICAL AGENT concept, and which has a kind of 'id register', known as CPF. The CPF is an individual 11-digit numbering, generated to identify federal taxpayers. Two partitions are built from NATURAL PERSON, one to divide the individuals among UNDERAGE and ADULT, and a second to separate people who have some type of mental illness (MENTALLY SICK), of those MENTALLY HEALTHY. A person is said to be criminally responsible (CRIMINALLY LIABLE) whether he or she is of legal age and has no mental disorder. In this case, it does not make sense to speak of roles, but rather of phases, since this classification depends exclusively on an agent's intrinsic properties. An active agent will only be the perpetrator (CRIME AUTHOR), if he/she can be held responsible for a crime.

Fig. 5. Criminal agents.

[FIGURE]

Fig. 6. Criminal objects.

[FIGURE]

In addition to ordinary people, other categories might also assume the role of victim, such as a juridical person (PASSIVE JURIDICAL PERSON) or the society (PASSIVE SOCIETY). Crimes against the environment, for example, have society as their principal victim. A juridical person owns an unique national registry as well (CNPJ), in addition they are commonly represented by a civil person. The CNPJ is the identifier of legal entities for the Internal Revenue Service. It is a digit of 14 numbers, necessary before beginning any commercial activity. Although outside the scope of this study, penal law defines further the role of an 'Impaired Agent', for example, those dependent upon a murdered victim.

Figure 6 shows legal objects configured as objects of crime (CRIME OBJECT). A MATERIAL OBJECT is a concrete asset protected by criminal law, such as a wallet or a cell phone. The ABSTRACT OBJECT satisfies a human need, even of purely moral value. These values include things such as life, honor, public peace, and physical integrity. The legal objects are usually associated with a PASSIVE AGENT, that is, those agents affected by the offending behavior, such as the person (honor, life) or society (public peace). POSITIVE LAW is a special type of NORMATIVE DESCRIPTION: a legislatively produced norm that defines the aforementioned roles, recognized by a politically organized community (STATE). The State, as a political society, has three primary roles: the Legislative role to draft laws; the Executive role to administer the State aiming at its concrete objectives; and the Jurisdictional role (JURISDICTION AGENT) to interpret and apply the law in the legal disputes. Therefore, under the assumption that the STATE plays judicial power over society, it is specialized in a legal agent as well (JURISDICTIONAL STATE). Description Logic axioms T ag describe agents and objects in the criminal universe. In order not to overload the axioms, some subsumption relations are not explicit.



























































[FIGURE]





⊑∃





Fig. 7. Conceptualization of Crime of Commission.

[FIGURE]

In order to model the concept of CRIME (Fig. 7), we define a LEGAL EVENT as an AGENT PARTICIPATION event, accomplished through the participation of a LEGAL AGENT. Three legal events are built by specialization, one to represent a TYPICAL EVENT, another for an UNLAWFUL EVENT, and, finally, a CULPABLE EVENT, to match the aforementioned definition of an ordinary crime. TYPICAL EVENT has a post-situation prohibited by some norm. The unlawfulness arises from the violation of some legal good protected by the State, so UNLAWFUL EVENT violates a CRIME OBJECT. CULPABLE EVENT requires the participation of a criminally imputable agent. Therefore, CRIME is logically defined as a conjunction of these minor events.

T com lists the principal axioms related to the definition of crime.

[FIGURE]





⊑∃



















































































































A CRIME is specialized in a set of subtypes. Some of these subtypes refer to the gravity of the fact, others to the form of execution, to the result, or to the type of agents participating. The most widely encompassing is COMMISSIVE CRIME: one which necessarily involves a voluntary action (CRIMINAL ACT), performed by an ACTIVE AGENT (such as killing, stealing, taking something, inducing someone to commit suicide, among others). CRIMINAL ACT specializes LEGAL ACT, a broader entity bringing together actions of the legal scope, carried out by some LEGAL AGENT. A crime is said to be commissive if, in addition to unlawfulness and culpability, the agent does not act by chance, but is directed by an internal commitment (INTENTION) to achieve a purpose. This action causes a change from a pre-existing situation to another, the DISALLOWED SITUATION, which perfectly matches at least one prohibited regulation. A special type of SOCIAL RELATOR (CRIME RELATOR) mediates the participating agents. Other legal mediators are built under the more general entity LEGAL RELATOR.

Figure 8 depicts the match between the description enclosed within the norm and the concrete fact (the situation), known as 'Legal Tipicity', as stated by Greco (2017). A LEGAL RELATOR was created for this: QUALIFICATION. A LEGAL NORM is a kind of a regulation like any other, with the addition of being part of the law created by the State. A norm specializes in legal PRINCIPLES (generic norms on which legal systems are built), and written LEGAL RULES, which define qualified situations and punitive measures. Furthermore, a partition is set apart from the legal rules to regulate INCRIMINATING and NON-INCRIMINATING rules.

Based on the work by Hoekstra et al. (2009), QUALIFICATION describes the deontic notions of the acceptability of the situation. Roughly, typicity encompasses three types, that is, abstract descriptions for prohibited, mandatory, and permissive situations, subsumed by QUALIFIED SITUATION. It is worth noting that situations do not create a disjointed partition. Incidentally, it is possible for behaviors to be mutually qualified by norms with distinct deontic notions, creating a conflict between them (CONFLICT SITUATION). Legal systems around the world, therefore, contain various set of legal doctrines to resolve such conflicts (addressed later).

PERMISSION mediates a non-incriminating rule with a situation which the rule allows. In addition, PROHIBITION mediates an incriminating rule with a disallowed situation which the rule forbids, or with a mandatory situation which the rule requires to happen. A mandatory situation regulates SOCIAL COMMITMENTS; which, when not observed, lead to infractions. In order to not overload the model, some relations are not represented. These deontic qualifications are formally defined in T qua .

Fig. 8. Norms and situations.

[FIGURE]













































[FIGURE]





≡























A legal norm presupposes two set of precepts: the primary, which deontically regulates the situation and, optionally, a secondary precept that decrees the PUNISHMENT ACT, that is, the punishment to be imputed to the offending agent, as a consequence of his illicit act (Fig. 9). A punishment act is a sanction imposed by the JURISDICTIONAL STATE, through its representatives. Punishments are partitioned into three disjoint groups: DEPRIVING LIBERTY, RESTRICTING RIGHT and FINE.

CIRCUMSTANCES are special factors (state-of-affairs) that come into play to increase or decrease the severity of a criminal act, without modifying its essence. For example, the crime of infanticide - i.e. when during the postpartum period, the mother kills her own child - is a more serious type of murder, culminating in more severe penalties.

Fig. 9. Punishments and conflicts.

[FIGURE]

Whenever two or more norms may be applied to the same fact, an apparent conflict takes place (Pauwelyn, 2003). It is not possible, however, to allow two rules to relate to a single natural fact, which would violate the principle known as Non bis in idem (Buckland and Stein, 2007, p. 457), according to which an agent cannot be punished twice for the same act. The legal doctrine has some fixed principles to solve these conflicts, considering specialty, superiority or temporal criteria. In Fig. 9, these principles are linked by a NORM RELATOR, mediating the norms, that assume different roles, depending on the criteria listed. Some axioms related to the handling of conflicts between rules are defined in T lex .



















































[FIGURE]





## 5.4. Handling Crimes of Omission

Rather than forcibly assuming omission to be a type of action, the strategy adopted in this study to represent crimes of omission was to avoid using the ACTION CONTRIBUTION entity. Consequently, there is an agent involved in the situation, but one who is not intentionally executing any action. This agent also needs to possess some abilities (SKILLED PERSON), without which he would be incapable of accomplishing a certain act. This therefore characterizes a LEGAL OMISSION (Fig. 10), a typical event carried out through the participation of a skillful agent (SKILLED AGENT PARTICIPATION) in a situation where, obligatorily, he has a legal DUTY TO ACT. This is a SOCIAL COMMITMENT regularly established among ordinary citizens. Moreover, this social duty represents an UNFULFILLED COMMITMENT. ABILITY is an INTRINSIC MOMENT whose existence is tied to the person possessing it. In this way, PURE OMISSIVE CRIME brings together the three necessary and sufficient events to classify a behavior as a crime, plus the extra conditions to identify the perpetrator's omission.

Additional circumstances are necessary in order to classify an event as a FELONY OMISSION crime (Fig. 11). Unlike an immediate duty, which obliges everyone indiscriminately, there is a SPECIFIC DUTY TO ACT. Through this commitment, a new legal relator (LEGAL CARE RELATOR) is required to mediate the relationship between the parties, that is, the one who protects (GUARANTOR), and the protected (GUARANTEED). Therefore, the offender in a crime of this type must be an instance of GUARANTOR, and there must be a specific result described. This condition satisfies a state-of-affairs with an objective, considered to be the desire of the GUARANTOR when omitting to perform the required action. It is worth noting that it makes no sense to speak of an agent's intention, because the agent does not commit himself to act in order to achieve the result. Conversely, there is a DESIRE that a state-of-affairs be reached. This type of crime is often renamed as 'Commission through omission'. This is because the agent who is obliged to avoid the result is punished with the criminal type corresponding to the result. Therefore, the

⊑∃

Fig. 10. Pure omissive crime.

[FIGURE]

Fig. 11. Felony omissive crime.

[FIGURE]

lifeguard who assists, through inaction, in the drowning of a bather is considered to have practiced the crime of homicide. A bidirectional UML association, MATCH, materializes this relationship between the crime of omission and that of commission. Terminological axioms T omp and T omi represent the related crimes of omission in Description Logic.

[FIGURE]





⊑∃

5.5. Addressing semantic deficiencies with patterns and anti-patterns

UFO promotes a sort of profile, improving the discovery and correction of erroneous assumptions due to semantic conceptualization mistakes with regard to a particular domain. In general terms, UFO establishes a set of ontological constraints over the categories it supports. These constraints are built on meta-properties drawn from classical theories, such as those that accommodate the principle of identity, rigidity, and external dependence, as discussed by Guizzardi (2005). In this work, some postulates rooted in the well-founded theory of substantial universals are presented. In short, the postulates state that: (i) each object must be an instance (directly or indirectly) of a Kind, (ii) and not more than one; (iii) a ridig type can not be super-typed by an anti-rigid one; (iv) universal dispersive types (mixin, category, rolemixin) can not specialize sortal.

## 5.5.1. UFO patterns

In order to design high-quality and ontologically consistent conceptual models, the engineer should make use of tools and methodologies for ontology-driven conceptual modeling, such as modeling patterns and anti-patterns. Patterns (Guizzardi, 2014) are well-established design fragments to comply with the theories underlying UFO. Figure 12 pictures the principal patterns adopted, namely Role Pattern, Phase Pattern, and RoleMixin Pattern.























































Fig. 13. Models representing the patterns used.

[FIGURE]

With respect to the Role Pattern (Fig. 12(a)), role stereotyped types (e.g., X ) must necessarily relate to some other type with which the former maintains a dependency (hence the minimum cardinality at the opposite end must be 1), such as the relation R . The Phase pattern (Fig. 12(b)) defines complete and disjoint phase partitions (such as types, P 1 , . . . , P n ). RoleMixin Pattern (Fig. 12(c)) is used to handle cases where a dependent anti-rigid type (such as RM ) specializes in subtypes ( R 1 , . . . , Rn ) that instantiate distinct kinds. In these situations, the super-type must be stereotyped with rolemixin, in addition to requiring an external dependence (relation R ), as any role type does.

These modeling patterns may be observed in the UML models discussed so far. In particular, we highlight in Fig. 13 excerpts from the class diagrams consistent with such patterns. Taking into account the conceptualization of crime of commission (Fig. 7), the perpetrator, for example, can only exist whether there is a crime (Fig. 13(a)). Similar concerns were considered in the definition of other agents and objects, such as ActiveAgent , PassiveAgent , SpecificRule , Guarantor , among others. Figure 13(b) shows the partition defined from the sortal NaturalPerson , to conceptualize types as to be of legal age or not, extracted from the hierarchy of agents (Fig. 5). Finally, in order to achieve ontological engagement regarding the different types of agents present in a crime scene, it was necessary to resort to rolemixin pattern, as can be seen in the construction of possible victims of a criminal act (Fig. 13(c)). Some additional patterns were further introduced as the models have evolved, such as Relator and Material Relations Pattern (Guizzardi, 2014), which we do not explore here for the sake of legibility.

## 5.5.2. UFO anti-patterns

Given the factual legal knowledge, largely based on semantic pitfalls, patterns do not guarantee that unwanted models instances are created. Therefore, it is imperative to make additional use of antipatterns, that is, additional configurations to discover error-prone assumptions, which may lead to unintended state-of-affairs. Throughout ontological engineering, we adopted four modeling patterns, namely:

Fig. 14. RS (a) and RWOR (b, c) anti-patterns.

[FIGURE]

Role Pattern, Phase Partition Pattern, RoleMixin Pattern, and Relator and Material Relations Pattern. Figure 13 depicts some of them.

From the catalogue of available semantic anti-patterns (Guizzardi and Sales, 2014), we show some DL axioms used to restrain the possibility of instances of unintended models. In particular, we focus on the following anti-patterns: Relation Specialization (RS), Relator with Overlapping Roles (RWOR), and Imprecise Abstraction (IA) (Guizzardi and Sales, 2014). Figure 14 shows some parts from the criminal ontology which can derive unintended instance models.

The RS anti-pattern requires the analysis of whether relations between types and their super-types are not related to each other. We observe this occurrence in the relations between agents and legal events (Fig. 14(a)), and in those between legal events and post-prohibited situations. To eliminate any source of problems, one must establish how these associations relate. In both cases, one specializes the other. Therefore: performanceOf ⊑ participationOf and hasDisallowedSituation ⊑ hasPosSituation .

Even unusual, it is likely that in addition to natural person, a juridical person may be classified as a perpetrator, particularly with regard to environmental crimes. Such cases have society as the single victim. Although we narrowed the scope, some considerations are necessary if we adopt this role extension for the active agent. According to Guizzardi and Sales (2014), when two types are related through an association with an upper cardinality in both ends greater than one, and at least one of the related types specializes into subtypes, an Imprecise Abstraction anti-pattern emerges. This is what occurs with the injures relation between the agents of a criminal event. The practical solution is to define concrete associations between subtypes, rather than maintaining an abstract and vague relationship between their types. We highlight the relation that needs to be removed, as well as those between subtypes that must be explicitly added in Fig. 15.

When two (potentially) overlapping roles (rooted in the same kind) are related by a material relation, we have a RWOR anti-pattern. Analyzing, therefore, if the same individual can play both roles, we can unveil models semantically non-compliant with reality. We have had two cases, with different solutions. In a single model of the world, a perpetrator of crime and its victim, cannot be the same individual. Even for the crimes of suicide, other agents are investigated, such as the one who induced or facilitated the act. Therefore, for Fig. 14(b), it is necessary and sufficient to make the roles disjoint ( ActiveAgent ⊑ ¬ PassiveAgent ). The case in Fig. 14(c) is more complex: a rule can play both roles (specific and general), but not related to the same individual. In other words, an arbitrary norm X may be more specific than a norm Y , and more general than a norm Z , however, Y and Z must be distinct. In this case, it is necessary to add DL axioms to make the relation asymmetric (that is, disjoint from its own inverse), and irreflexive (that is, it is never locally reflexive). Thus, we have: Disjoint ( specializes , specializes -) and ⊥ ⊑ ¬∃ specializes . Self .

Fig. 15. Imprecise Abstraction representation. Anti-patterns advise against the first relation.

[FIGURE]

## 6. Related work

Automated case research, legal analysis systems, and other sophisticated legal applications have become a current concern, given the tangled and complex network of regulations presented in legal documents. The formalization of legal documents in a machine-readable unambiguous manner is not solely an academic interest, despite the difficulty of dealing with open-textured concepts and other semantic anomalies (Freitas et al., 2011). Researches supported by governmental initiatives (Costilla et al., 2005; Agnoloni and Tiscornia, 2010; Jinhyung et al., 2012; Lu et al., 2012; Gostojic et al., 2013) seek the same goal, attempting to create free access to legislation online. Nevertheless, the online availability of legal documents does not solve the practical problems of citizens and businesses: the need for an approach that models the knowledge and interpretations from legal documents, queries and laws. Over the last two decades, an exponential explosion of conceptual models addressing entities from a social reality perspective and proposing practical applications has occurred, even though few have met these requirements. The discussion that follows is restricted to some studies that attempted to map legal (and specifically, criminal) nuances, such as those by Griffo et al. (2016), Rodrigues et al. (2015), Hoekstra et al. (2009), Gangemi et al. (2005) and Asaro et al. (2003).

Griffo et al. (2016) produced a legal core ontology, grounded on UFO: the UFO-L. The purpose of this was to provide conceptual models of the legal domain, following a so-called relational perspective (different from the positivist-normative perspective adopted in this present work). Other legal theories can be used in conjunction with ontologies to overcome the existing semantic gap in legal systems. UFO-L therefore considers modeling a more contemporary theory than the positivist: the theory of fundamental rights represented by legal positions and legal relations, also known as Alexy's Theory (Alexy and Pulido, 2007). UFO-L attempts to map right-duty relations, besides those of liberties and powers. A typical example is the relationship between the right to life and the state's duty to guarantee this right. This work, in fact, is much more a theoretical complement to what is presented here, than a repeated study.

Inspiration for this ongoing work did not come about by chance, but through long-term research of a set of ontologies developed to simulate lawsuit rooted in the Brazilian Penal Code, as reported in Rodrigues et al. (2015). Domain and application ontologies were designed to model the principal criminal types found in the local legal order, such as crimes against life (Rodrigues et al., 2017), against property (Rodrigues et al., 2016), and infractions related to the drinking-and-driving law (Rodrigues et al., 2015). Specifically, an ontological representation through which the normative code can be formalized in a machine-readable fashion to support decision making in the legal domain was proposed: OntoCrime. Although these conceptualizations were lightly-based on LKIF theories and validated through methodologies proposing meta-properties of rigidity, dependence, unity, and identity (OntoClean meta- properties defined by Guarino and Welty (2002)), there was also a need to direct them through a foundational ontology that already defined social entities concepts and incorporated these types of restrictions.

LKIF, the Legal Knowledge Interchange Framework (Hoekstra et al., 2009), is a generic architecture developed using some of the emerging Semantic Web standards such as RDF (Resource Description Framework described by Baader et al. (2010)) and OWL (Web Ontology Language described by Antoniou and Harmelen (2009)). This core ontology was developed to support two main proposals: to serve as a common basis for translation between disparate legal knowledge bases, and to provide an axiomatization of legal categories (clusters) to facilitate the construction of autonomous legal systems for legal assessment and argumentation. LKIF is structured as a library of 15 modules, encompassing notions such as actions, processes, situations, and time/space occurrences. At the time of its development, however, LKIF did not relate to any Foundational/Core Ontology (except for a partial view of the LRI-Core structure (Breuker and Hoekstra, 2004)) given the lack of these models for representing legal knowledge based on empirical evidence, besides the incipient commonsense view. Furthermore, the clusters were organized based on a joint view of three user profiles: laypersons, area professionals, and law students. It is suggested that the notions of legal theory, though not explicitly addressed, fall heavily on conceptual notions arising from the interaction between these groups. LKIF is undoubtedly an inspiration for this work, however, the domain has been limited to the singularities of the criminal universe and the decisions have been rooted in assumptions made in the UFO top ontology.

The Core Legal Ontology (CLO, defined by Gangemi et al. (2005)) is a general typology of legal entities, addressing mental, social, and legal categories. CLO can be considered a constructive framework that provides reusable components across multiple legal domain ontologies. Conformity checking and norm comparison are the main attributions of this core ontology, whose basic precepts lie in the foundational theories of DOLCE + : a DOLCE extension with dedicated support for the representation of time, space, plans, and context (Masolo et al., 2002). CLO preferred to base its representations on Hohfeld's theory of basic conception (Hohfeld, 1913). This proposes 'normative positions', that is, relations of opposition/correlation between parties involved in a legal context, such as: Duty (and its correlative, Claim), Privilege (and its correlative, Non-Right), and Immunity (and its correlative, Disability).

The Italian Crime Ontology proposed by Asaro et al. (2003) presents a conceptual formalization for crime definition, featuring criminal behavior, additional circumstances that could increase punishment, sanctions, and security measures, beyond the identification of those responsible for violating the laws. This project, however, offers no means of resolving conflicts when different (and potentially, conflicting) norms match a particular situation. The study traced the first steps in the search for a homogeneous domain ontology that could be shared by several Italian projects to develop systems for judicial decision support. However, its concepts are presented superficially, without being properly anchored in legal theory.

According to our literature review, to the best of our knowledge, the core ontology proposed in this work is the first that brings together a criminal (positivist) legal theory with the underlying philosophical theories of a foundational ontology, in an approach that transcends purely conceptual notion towards the construction of practical applications. In other words, by raising criminal concepts to a foundational ontology, the range of extension possibilities from the core ontology is decreased, while at the same time allowing users to reduce difficulties and errors in the construction of domain and application ontologies for real practical systems.

## 7. Running examples

Some examples of crimes extracted from the Brazilian legal code are discussed in this section. Object diagrams are also highlighted to instantiate elements of entities defined in criminal ontology, in order to demonstrate the suitability of the model for commissive and omissive crimes. When necessary, reference is made to the laws from the Penal Code, the Brazilian constitution, or some other more specific norm.

Example 7.1. Peter and Bill used to be friends and often visited each other's house with their wives. However, after learning about the extra-marital affair of Peter's wife, Bill began to make jokes about Peter in a group of friends. After numerous taunts, while both were at a bar, Peter, compelled by strong and uncontrolled anger, hits Bill with a broken glass bottle, killing him.

Laws that prevent crimes against life (articles 121 to 128 of Penal Code (Brasil, 1940)), as stated in the example, can have a number of doubts as the understanding of the type of crime and consequently, the corresponding punishment. Concerning the range of crimes under the umbrella of infractions against life, a series of disparate circumstances emerges which may transform the crime in another of a more or less severe type, directly increasing or decreasing the final sentence. The norms that address the situation at hand are transcribed in the original Portuguese as well as in English:

## · In Portuguese:

Art. 121 - Matar Alguém:

- ∗ Homicídio Simples :

Pena - reclusão, de seis a vinte anos

Caso de redução da pena

§1. Se o agente comete o crime impelido por motivo de relevante valor social ou moral, ou sob o domínio de violenta emoção, logo em seguida a injusta provocação da vítima, o juiz pode reduzir a pena de um sexto a um terço;

- ∗ Homicídio Qualificado :

Art. 121

§2. Se o homicídio é cometido:

II - Por motivo futil;

Pena - reclusão, de doze a trinta anos .

- In English:

Art. 121 - killing someone:

- ∗ Simple Homicide :

Punishment - imprisonment, from six to twenty years

## Case of reduction of punishment

§1. If the perpetrator commits the crime motivated by reason of social or moral value, or under the control of violent emotion, immediately after the unfair provocation by the victim, the judge can reduce the penalty from one-sixth to one-third;

- ∗ Felony Homicide :

Art. 121

§2. If the murder is committed:

II - For trivial reasons;

Punishment - imprisonment, from twelve to thirty years .

Fig. 16. Example of a Comissive Crime.

[FIGURE]

The description of this troubled relationship between Bill and Peter is represented in Fig. 16, falling under the MURDERWITHDECREASE criminal type (a specialization of Comissive Crime). The leftmost part of Fig. 16 covers the offending agent and his intention. The upper right portion defines the initial and final situations, highlighting whether Bill is living or not. Finally, the lower portion highlights the norms covering the mentioned case and the punishment to be fixed at a certain amount, respecting the legal limits. This activity follows a process of dosimetry, in which a minimum and maximum limit are defined. In this case, the presence of special circumstances (HEALOFPASSION) is observed, beyond those ordinarily present in the crime of killing. Two moments in the dosimetry of the punishment can be pointed out: first, ARTICLE 121 defines the basic penalty; and second, the first paragraph reduces the base value, given the condition of acting in a moment of extreme emotion. Although Bill plays roles and assumes disjoint phases, he is an instance of a single ultimate Kind (NATURAL PERSON), respecting the postulates by Guizzardi (2005).

The following example still refers to Bill and Peter, with some subtle yet significant modifications to the description of the crime, and in the calculation of the appropriate punishment.

Example 7.2. Bob and Bill, passionate fans of the two biggest rival soccer teams in town, were friends who were watching the final match. After the victory of Bill's team, he begins to make jokes towards Peter, who attacks him with a broken bottle, leading to Bill's death (although this was not Peter's intention).

These are similar cases, but with slightly different circumstances: the second crime occurred for trivial (futile) reasons. This last example is illustrated in Fig. 17. There are some similarities with the previous case, differing in the presence of an aggravating circumstance (FUTILEREASONX: the silly discussion about the soccer teams). The second internal paragraph of ARTICLE 121 is considered, which defines more severe prison limits for the accused. It is not possible to apply both sanctions against the offender, in order to not violate the principle of Non bis in idem . Typically, homicide results in prison time of 6 to

Fig. 17. Example of a Comissive Crime with aggravating circumstance.

[FIGURE]

20 years. However, killing for trivial reasons is a more severe crime, meaning that the punishment at the bottom of the image is an exception to the more typical case. The principle of Lex Specialis , therefore, mediates the relationship between the norms, giving them a specificity relation. The relator resolves the tiebreaker by choosing the more specific norm, that is, ARTICLE 121 PAR 2 DECREE 2848.

Now, some crimes of omission will be explored.

Example 7.3. A certain doctor (doctorX) of a family health clinic, located in an arbitrary city (VillageX), attends to the case of a child with suspected bacterial meningitis. After the necessary procedures and due care of the child, doctorX does not inform the case to the necessary authorities, i.e. the public health agency of the city or state. Meningitis is a mandatory notification disease according to the Brazilian Department of Health Regulation/1923 (which addresses other diseases such as plague, cholera, smallpox, and puerperal infection), because it involves danger that can result from the spread of the contagious disease. The object of legal protection is public safety.

This example is illustrated in Fig. 18.

The situation aforementioned matches the crime described in article 269 (Brasil, 1940), which states that:

## · In Portuguese:

∗ Omissão por Notificação de Doença Art. 269 - Deixar o médico de denunciar à autoridade pública doença cuja notificação é compulsória: Pena - detenção, de seis meses a dois anos, e multa.

Fig. 18. Example of pure omissive crime.

[FIGURE]

## ∗ Omission of Disease Notification

## · In English:

Art. 269 - Doctor fails to notify the public authority regarding a disease whose notification is compulsory:

Punishment - imprisonment, from six months to two years, and fine.

The conduct mentioned in article 269 is, in fact, a crime of pure omission. The active agent can only be a doctor, because only he would have the necessary ability to verify the presence of the disease, be aware of its seriousness, and the responsibility to notify the competent authorities. In this case, the ethical commitment to notify was not fulfilled. The passive agent in this occasion is not the child, who received the proper care. Society itself is the victim. In the Fig. 18, it is emphasized that the city would be the victim, as it would suffer the first lethal effects of the spread of the disease. Moreover, the situation portrayed is qualified by Article 269, which dictates two types of punishment: a fine (whose value is not explicitly specified in the incriminating rule) and imprisonment from 6 to 24 months.

Let us check a new example that involves the omission of participants.

Example 7.4. Isadora, the mother of 12-year-old Larissa, left early from work and, when arriving home, sees her partner, Frederick, from the living room window, having sex with her daughter on the couch. Shocked by the scene, she had no reaction. Not having been seen by either, Isadora decided, from then on, to arrive at her residence at that same time and verified that the act was repeated over a period of weeks. Isadora had an effective knowledge of the abuses perpetrated by Frederick, but, very much in love with him, she did nothing. Isadora remained inactive, while knowing of the abuses committed by her companion against her daughter.

In felony crimes of omission, as detailed earlier, the agent does not respond for the omission itself, but for its effects and the consequences resulting from it. This mother described in the scenario is the guar- antor of the sexual integrity of her daughter. In addition, there is no information indicating an inability to act to avoid the result of rape on the part of the mother. In choosing to let her daughter be sexually assaulted in order not to lose her partner, she has committed felony omission. Because of this, she must respond for the same crime imputed to her husband, that is, both will be judge for rape of a minor. It should also be noted that sexual offenses against children under the age of 14 are considered a heinous crime. The Brazilian Federal Constitution of 1988 (Brasil, 1988), in Article 5, says that heinous crimes will be answered by the executors, and by anyone who might be able to prevent them, but who fails to act. These norms are transcribed below.

## · In Portuguese:

XLIII - a lei considerará crimes inafiançáveis e insuscetíveis de graça ou anistia a prática da tortura , o tráfico ilícito de entorpecentes e drogas afins, o terrorismo e os definidos como crimes hediondos, por eles respondendo os mandantes, os executores e os que, podendo evitá-los, se omitirem;

- ∗ (Constituição Federal) Art 5. - [. . . ]
- ∗ Dos Crimes Sexuais contra Vulneráveis (Lei 12.015/2009) Art. 218 - Induzir alguém menor de 14 (catorze) anos a satisfazer a lascívia de outrem: Pena - reclusão, de 2 (dois) a 5 (cinco) anos.
- In English:

XLIII - the law shall consider crimes to be non-bailable and not susceptible to grace or amnesty: the practice of torture, illicit trafficking in narcotics and related drugs, terrorism, and what are defined as heinous crimes, to which must respond the principals, the executors and those who

- ∗ (Federal Constitution) Art. 5 - [. . . ] could have prevented the crime but omitted to act.
- ∗ Sexual Crimes Against the Vulnerable (Law 12,015/2009) - Induce someone under the age of 14 (fourteen) years to satisfy the lust of another:

Art. 218 Punishment - imprisonment, from 2 (two) to 5 (five) years.

Figure 19 is divided into two distinct sections. The section on the left models Isadora's behavior, while that on the right conceptualizes Frederick's behavior. Without any doubt, the behavior of the husband is criminal, and subject to penal sanction. There is a willful intent in Frederick's action. Greater attention is focused on the behavior of Larissa's mother in the same way. Isadora was fully aware of the sexual abuse, and had the ability to act, either by preventing or informing someone else who could act against the rape. However, by deciding to do nothing, it becomes guilty omission. In addition, the MATCH association between the criminal types attests that Isadora will also be punished for a sexual offense against the vulnerable. According to the same constraint that regulates the instances of active and passive agents, Guarantor and Guaranteed objects must be disjoint.

## 8. Conclusion

In this paper, the assumptions and commitments surrounding the criminal law system are made explicit, through the use of ontological models, due two reasons little explored over the years. First, this paper was conceived in order to overcome some limitations of past experiences in constructing legal systems for practical use, insofar as the relations between AI &amp; Law and Hans Kelsen's positivist legal philosophy can be approximated. As UFO provides a well-defined profile for conceptual modeling along with some methodological guidelines to avoid modelling confusions, a criminal core ontology grounded on a typology of universals was engineered. Therefore, UFO played an irreplaceable function for the conceptual modeling.

Fig. 19. Example of felony omissive crime.

[FIGURE]

Secondly, the inaction of an agent when there is a legal obligation to prevent an undesirable result against a legal right protected by the state is an event that until has not heretofore been properly conceptualized given the difficulties and lack of consensus among the underlying philosophical theories. The scope of the study was restricted to the types of crimes of omission found in the Brazilian Penal Code. Although related to a specific legal system, the suitability of the model for other localities that also follow the Civil Law system is emphasized.

The rich refined axiomatization of UFO made it possible to externalize the rationales without worrying about specific axioms, that might cross a plurality of sub-domains within the criminal field. Additionally, UFO categories enabled the axiomatization of crimes of omission, without directly representing the underlying philosophical concept of omission (negative action), and their relation (if any) to a positive action. The universe of crime is vast and variable. Concepts change over the years. Likewise, criminal law is also in continuous movement as it seeks to adapt to social realities. With this in mind, the ontology proposed is flexible enough to be expandable whenever possible. For example, while some crimes are removed from the penal code (such as seduction), others are included (such as cyber-crimes). These models should intuitively follow the evolution of the penal code, a difficult task to perform cognitively without technological support.

Some future work has already been outlined based on the results achieved. We propose to adapt domain ontologies available in literature (Rodrigues et al., 2016, 2017) and developed under this same project, to meet the assumptions of the Criminal Ontology. The goal is to build a framework of criminal ontologies, that are accessible through web-based autonomous services capable of performing legal simulations that aid in decision-making. This framework can be expanded with criminal subtypes still scantly explored, such as crimes against the environment and crimes of terrorism. Numerous applicationspecific ontologies can be built along these lines. Finally, an ongoing project is the development of a pro- totype, in which an ordinary user can simulate lawsuits for real or fictitious cases through a user-friendly interface, without needing to deal with the low-level modeling formalisms. LEGIS (LEGal analysIS) is a web-based front-end system through which one can make functional and affordable checks against the mapped criminal ontologies. The results obtained thus far should improve the juridical understanding of layperson and aid in the labor-intensive task of lawsuits performed by professional jurists.

## Acknowledgements

This research is part of the project APQ-0550-1.03/16 ( Reconciling Description logic and nonmonotonic reasoning in the legal domain ), supported by the Fundação de Amparo à Ciência e Tecnologia do Estado de Pernambuco (FACEPE), by the Institut National de Recherche en Informatique et Automatique (INRIA) and by the Centre National de la Recherche Scientifique (CNRS).

## References

- Agnoloni, T. &amp; Tiscornia, D. (2010). Semantic web standards and ontologies for legislative drafting support. In E. Tambouris, A. Macintosh and O. Glassey (Eds.), Electronic Participation (pp. 184-196). Berlin, Germany: Springer. doi:10.1007/9783-642-15158-3\_16.
- Alexy, R. &amp; Pulido, C.B. (2007). Teoría de los derechos fundamentales . Colección El derecho y la justicia. Centro de Estudios Politicos y Constitucionales.
- Antoniou, G. &amp; Harmelen, F.V. (2009). Web ontology language: OWL. In S. Staab and R. Studer (Eds.), Handbook on Ontologies (pp. 91-110). Berlin, Germany: Springer. doi:10.1007/978-3-540-92673-3\_4.
- Asaro, C., Biasiotti, M.A., Guidotti, P., Papini, M., Sagri, M.T., Tiscornia, D. &amp; Court, M.A.L. (2003). Domain ontology: Italian crime ontology. In Workshop on Legal Ontologies &amp; Web Based Legal Information Management (ICAIL 2003) . New York, NY, USA: ACM Press.
- Baader, F., Calvanese, D., McGuinness, D.L., Nardi, D. &amp; Patel-Schneider, P.F. (2010). The Description Logic Handbook: Theory, Implementation and Applications (2nd ed.). New York, NY, USA: Cambridge University Press.
- Bach, K. (2010). Refraining, omitting and negative acts. In T. O'Connor and C. Sandis (Eds.), A Companion to the Philosophy of Action (pp. 50-57). Chichester, UK: Wiley-Blackwell. doi:10.1002/9781444323528.ch7.
- Bezerra, C., Freitas, F. &amp; Santana, F. (2013). Evaluating ontologies with competency questions. In Proceedings of the 2013 IEEE/WIC/ACM International Joint Conferences on Web Intelligence (WI) and Intelligent Agent Technologies (IAT), WIIAT '13 (Vol. 3, pp. 284-285). Washington, DC, USA: IEEE Computer Society. doi:10.1109/WI-IAT.2013.199.
- Brasil (1940). Decreto n 2848, de 1940. Código Penal. Brasília - DF. Retrieved on March 17, 2018 from http://www.planalto. gov.br/ccivil\_03/decreto-lei/Del2848compilado.htm.
- Brasil (1988). Constituição Federal de 1988. Brasília - DF. Retrieved on March 18, 2018 from http://www.planalto.gov.br/ ccivil\_03/constituicao/constituicao.htm.
- Breuker, J. &amp; Hoekstra, R. (2004). Core concepts of law: Taking common-sense seriously. In Proceedings of Formal Ontologies in Information Systems, FOIS'04 (pp. 210-221). Amsterdam, The Netherlands: IOS Press.
- Bringuente, A.C.O., de Almeida Falbo, R. &amp; Guizzardi, G. (2011). Using a foundational ontology for reengineering a software process ontology. JIDM , 2 (3), 511-526.
- Buckland, W.W. &amp; Stein, P. (2007). A Text-Book of Roman Law: From Augustus to Justinian (3rd ed.). Cambridge, UK: Cambridge University Press. Available at: https://books.google.com.br/books?id=l5U8xwaGxb0C.
- Clarke, R. (2012). What is an omission? Philosophical Issues , 22 (1), 127-143. doi:10.1111/j.1533-6077.2012.00221.x.
- Costilla, C., Palacios, J.P., Cremades, J. &amp; Vila, J. (2005). e-Government: A legislative ontology for the 'SIAP' parliamentary management system. In M. Böhlen, J. Gamper, W. Polasek and M.A. Wimmer (Eds.), E-Government: Towards Electronic Democracy (pp. 134-146). Berlin, Germany: Springer. doi:10.1007/978-3-540-32257-3\_13.
- Detoni, A.A., Miranda, G.M., Renault, L.D.C., de Almeida Falbo, R., Almeida, J.P.A., Guizzardi, G. &amp; Barcellos, M.P. (2017). Exploring the role of enterprise architecture models in the modularization of an ontology network: A case in the public security domain. In EDOC Workshops (pp. 117-126). IEEE Computer Society.
- Fernández-López, M., Gómez-Pérez, A. &amp; Juristo, N. (1997). Methontology: From ontological art towards ontological engineering. In Proceedings of the AAAI97 Spring Symposium (pp. 33-40).

- Freitas, F.L.G., Candeias, Z. &amp; Stuckenschmidt, H. (2011). Towards checking laws' consistency through ontology design: The case of Brazilian vehicles' laws. Theoretical and Applied Electronic Commerce Research , 6 , 112-126. doi:10.4067/S071818762011000100008.
- Gangemi, A., Sagri, M.T. &amp; Tiscornia, D. (2005). A constructive framework for legal ontologies. In V.R. Benjamins, P. Casanovas, J. Breuker and A. Gangemi (Eds.), Law and the Semantic Web: Legal Ontologies, Methodologies, Legal Information Retrieval, and Applications (pp. 97-124). Berlin, Germany: Springer. doi:10.1007/978-3-540-32253-5\_7.
- Gostojic, S., Milosavljevic, B. &amp; Konjovic, Z. (2013). Ontological model of legal norms for creating and using legislation. Comput. Sci. Inf. Syst. , 10 (1), 151-171. doi:10.2298/CSIS110804035G.
- Greco, R. (2017). Curso de Direito Penal - Parte Geral . Coleção Rogério Greco (18th ed., Vol. 1). Niterói, RJ, Brazil: Editora Impetus. Available at: https://books.google.com.br/books?id=54L2DQAAQBAJ.
- Green, L. (2009). Legal positivism. In E.N. Zalta (Ed.), The Stanford Encyclopedia of Philosophy (Fall 2009 ed.). Stanford, CA, USA: Metaphysics Research Lab, Stanford University.
- Griffo, C., Almeida, J.P.A. &amp; Guizzardi, G. (2016). A pattern for the representation of legal relations in a legal core ontology. In Legal Knowledge and Information Systems - JURIX 2016: The Twenty-Ninth Annual Conference (pp. 191-194). doi:10. 3233/978-1-61499-726-9-191.
- Griffo, C., Almeida, J.P.A., Guizzardi, G. &amp; Nardi, J.C. (2017). From an ontology of service contracts to contract modeling in enterprise architecture. In EDOC (pp. 40-49). IEEE Computer Society.
- Guarino, N. (1998). Formal Ontology in Information Systems: Proceedings of the 1st International Conference , June 6-8, 1998, Trento, Italy (1st ed.). Amsterdam, The Netherlands: IOS Press.
- Guarino, N. &amp; Welty, C. (2002). Evaluating ontological decisions with OntoClean. Commun. ACM , 45 (2), 61-65. doi:10.1145/ 503124.503150.
- Guizzardi, G. (2005). Ontological foundations for structural conceptual models. PhD thesis, University of Twente.
- Guizzardi, G. (2014). Ontological patterns, anti-patterns and pattern languages for next-generation conceptual modeling. In E. Yu, G. Dobbie, M. Jarke and S. Purao (Eds.), Conceptual Modeling (pp. 13-27). Cham, Switzerland: Springer International Publishing. doi:10.1007/978-3-319-12206-9\_2.
- Guizzardi, G., Baião, F.A., Lopes, M. &amp; de Almeida Falbo, R. (2010). The role of foundational ontologies for domain ontology engineering: An industrial case study in the domain of oil and gas exploration and production. IJISMD , 1 (2), 1-22.
- Guizzardi, G., de Almeida Falbo, R. &amp; Guizzardi, R.S.S. (2008). Grounding software domain ontologies in the unified foundational ontology (UFO): the case of the ODE software process ontology. In Memorias de la XI Conferencia Iberoamericana de Software Engineering (CIbSE 2008) , Recife, Pernambuco, Brasil, February 13-17, 2008 (pp. 127-140).
- Guizzardi, G. &amp; Sales, T.P. (2014). Detection, simulation and elimination of semantic anti-patterns in ontology-driven conceptual models. In E. Yu, G. Dobbie, M. Jarke and S. Purao (Eds.), Conceptual Modeling (pp. 363-376). Cham, Switzerland: Springer International Publishing. doi:10.1007/978-3-319-12206-9\_30.
- Guizzardi, G. &amp; Wagner, G. (2004). A unified foundational ontology and some applications of it in business modeling. In J. Grundspenkis and M. Kirikova (Eds.), CAiSE Workshops (Vol. 3, pp. 129-143). Riga, Latvia: Faculty of Computer Science and Information Technology, Riga Technical University. Available at: http://dblp.uni-trier.de/db/conf/caise/caisews2004-3. html#GuizzardiW04a.
- Guizzardi, G. &amp; Wagner, G. (2005). Towards ontological foundations for agent modelling concepts using the unified fundational ontology (UFO). In P. Bresciani, P. Giorgini, B. Henderson-Sellers, G. Low and M. Winikoff (Eds.), Agent-Oriented Information Systems II: 6th International Bi-Conference Workshop, AOIS 2004, Riga, Latvia, June 8, 2004, and New York, NY, USA, July 20, 2004, Revised Selected Papers (pp. 110-124). Berlin, Germany: Springer. doi:10.1007/11426714\_8.
- Guizzardi, G., Wagner, G., de Almeida Falbo, R., Guizzardi, R.S.S. &amp; Almeida, J.P.A. (2013). Towards ontological foundations for the conceptual modeling of events. In Conceptual Modeling - 32th International Conference, ER 2013, Hong-Kong, China, November 11-13, 2013. Proceedings (pp. 327-341). doi:10.1007/978-3-642-41924-9\_27.
- Hasse, P., Lewen, H., Studer, R. &amp; Erdmann, M. (2008). The NeOn ontology engineering toolkit.
- Herre, H. (2010). General formal ontology (GFO): A foundational ontology for conceptual modelling. In R. Poli, M. Healy and A. Kameas (Eds.), Theory and Applications of Ontology: Computer Applications (pp. 297-345). Dordrecht, The Netherlands: Springer. doi:10.1007/978-90-481-8847-5\_14.
- Hoekstra, R., Breuker, J., Bello, M.D. &amp; Boer, A. (2009). LKIF core: Principled ontology development for the legal domain. In Proceedings of the 2009 Conference on Law, Ontologies and the Semantic Web: Channelling the Legal Information Flood (pp. 21-52). Amsterdam, The Netherlands: IOS Press. Available at: http://dl.acm.org/citation.cfm?id=1563987.1563992.
- Hohfeld, W.N. (1913). Some fundamental legal conceptions as applied in judicial reasoning. The Yale Law Journal , 23 (1), 16-59. doi:10.2307/785533.
- Imieli´ nski, T. &amp; Lipski, W. Jr. (1984). Incomplete information in relational databases. J. ACM , 31 (4), 761-791. doi:10.1145/ 1634.1886.
- Jinhyung, Hwang, M., Jung, H. &amp; Sung, W. (2012). iLaw: Semantic web technology Based intelligent legislation supporting system. International Journal of Information Processing and Management , 3 , 45-49.

- JURIS (2018). Nemo jus ignorare censetur - JURIS, A Enciclopédia Jurídica. Retrieved on March 2, 2018 from http://juris. wiki.br/index.php?title=Nemo\_jus\_ignorare\_censetur&amp;oldid=46078.
- Kelsen, H. (1949). General Theory of Law and State (1st ed., V ol. 1). Cambridge, UK: Harvard University Press.
- Kleinig, J. (1986). Criminal liability for failures to act. Law and Contemporary Problems , 49 , 161-180. doi:10.2307/1191631.
- Lu, W., Xiong, N. &amp; Park, D.-S. (2012). An ontological approach to support legal information modeling. The Journal of Supercomputing , 62 (1), 53-67. doi:10.1007/s11227-011-0647-8.
- Masolo, C., Borgo, S., Gangemi, A., Guarino, N., Oltramari, A. &amp; Schneider, L. (2002). The WonderWeb library of foundational ontologies and the DOLCE ontology. Technical report. Available at: http://www.loa.istc.cnr.it/old/DOLCE.html.
- Noy, N.F. &amp; Hafner, C.D. (1997). The state of the art in ontology design: A survey and comparative review. AI Magazine , 18 (3), 53-74. Available at: http://www.idi.ntnu.no/~agnar/tdt55/AIMag18-03-006.pdf.
- Pauwelyn, J. (2003). Resolving conflict in the applicable law. In Conflict of Norms in Public International Law: How WTO Law Relates to Other Rules of International Law (pp. 327-439). Cambridge, UK: Cambridge University Press. doi:10.1017/ CBO9780511494550.009.
- Poletaeva, T., Guizzardi, G., Almeida, J.P.A. &amp; Abdulrab, H. (2017). Revisiting the DEMO transaction pattern with the unified foundational ontology (UFO). In EEWC . Lecture Notes in Business Information Processing (Vol. 284, pp. 181-195).
- Reiter, R. (1978). On closed world data bases. In H. Gallaire and J. Minker (Eds.), Logic and Data Bases (pp. 55-76). Boston, MA, USA: Springer. doi:10.1007/978-1-4684-3384-5\_3.
- Ren, Y., Parvizi, A., Mellish, C., Pan, J.Z., van Deemter, K. &amp; Stevens, R. (2014). Towards competency question-driven ontology authoring. In V. Presutti, C. d'Amato, F. Gandon, M. d'Aquin, S. Staab and A. Tordai (Eds.), The Semantic Web: Trends and Challenges (pp. 752-767). Cham, Switzerland: Springer International Publishing. doi:10.1007/978-3-319-07443-6\_50.
- Rodrigues, C.M.O., Azevedo, R.R., Freitas, F.L.G., Palmeira, E. &amp; Barros, P.V.S. (2015). An ontological approach for simulating legal action in the Brazilian Penal Code. In Proceedings of the 30th Annual ACM Symposium on Applied Computing, SAC '15 (pp. 376-381). New York, NY, USA: ACM. doi:10.1145/2695664.2695740.
- Rodrigues, C.M.O., Freitas, F.L.G. &amp; Azevedo, R.R. (2016). An ontology for property crime based on events from UFO-B foundational ontology. In 5th Brazilian Conference on Intelligent Systems (BRACIS) (Vol. 5, pp. 331-336). New York, NY, USA: IEEE. doi:10.1109/BRACIS.2016.067.
- Rodrigues, C.M.O., Freitas, F.L.G. &amp; Oliveira, I.J.S. (2017). An ontological approach to the three-phase method of imposing penalties in the Brazilian criminal code. In 6th Brazilian Conference on Intelligent Systems (BRACIS) . New York, NY, USA: IEEE.
- Valente, A. (1994). Ontologies, the missing link between legal theory and AI and law. In Proceedings of Legal Knowledge Based Systems and Legal Theory (pp. 65-75). Lelystad, The Netherlands: Koninklijke Vermande.
