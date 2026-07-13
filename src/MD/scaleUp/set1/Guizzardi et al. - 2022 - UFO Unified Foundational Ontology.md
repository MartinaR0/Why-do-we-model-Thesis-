[FIGURE]

## UFO: Unified Foundational Ontology

Giancarlo Guizzardi , Alessander Botti Benevides , Claudenir M. Fonseca

Daniele Porello , João Paulo A. Almeida and Tiago Prince Sales

a , b , ∗ c a , d c a

a Conceptual and Cognitive Modeling Research Group, Free University of Bozen-Bolzano, Italy

E-mails: gguizzardi@unibz.it, cmoraisfonseca@unibz.it, tiago.princesales@unibz.it

b Services &amp; Cybersecurity Group, University of Twente, The Netherlands

c Ontology &amp; Conceptual Modeling Research Group, Federal University of Espírito Santo, Brazil

E-mails: abbenevides@inf.ufes.br, jpalmeida@ieee.org

d University of Genoa, Italy

E-mail: daniele.porello@unige.it

Abstract. The Unified Foundational Ontology (UFO) was developed over the last two decades by consistently putting together theories from areas such as formal ontology in philosophy, cognitive science, linguistics, and philosophical logics. It comprises a number of micro-theories addressing fundamental conceptual modeling notions, including entity types and relationship types. The aim of this paper is to summarize the current state of UFO, presenting a formalization of the ontology, along with the analysis of a number of cases to illustrate the application of UFO and facilitate its comparison with other foundational ontologies in this special issue. (The cases originate from the First FOUST Workshop - the Foundational Stance, an international forum dedicated to Foundational Ontology research.)

Keywords: UFO, OntoUML, foundational ontology, ontological analysis, formal ontology

Accepted by: Stefano Borgo

## 1. Introduction

For almost two decades now, the Unified Foundational Ontology (UFO) has been the focus of a longterm research program on ontological foundations for conceptual modeling. UFO (Guizzardi, 2005; Guizzardi et al., 2015b) was developed by consistently putting together theories from formal ontology in philosophy, cognitive science, linguistics, and philosophical logic. UFO is a four-category ontology that addresses fundamental conceptual modeling notions via a set of micro-theories, including:

- a theory of types and taxonomic structures that is connected to a theory of object identifier s, including a formal semantics in a sortal quantified modal logic (Guizzardi et al., 2021);
- a theory of part-whole relations ;
- a theory of particularized intrinsic properties, attributes and attribute value spaces (Guizzardi and Zamborlini, 2014), which includes a view on datatypes as semantic reference structures (Albuquerque and Guizzardi, 2013);
- a theory of particularized relational properties and relations , (Guarino and Guizzardi, 2015; Fon2019), including a proposal for Weak Truthmaking (Guarino et al., 2019) connecting particularized properties to propositions;

* Corresponding author. E-mail: gguizzardi@unibz.it.

- a theory of roles ;
- a theory of events (Guizzardi et al., 2013a; Almeida et al., 2019; Benevides et al., 2019b; Guizzardi et al., 2016), including aspects such as event mereology, temporal ordering of events, object participation in events, causation, change, and the connection between events and endurants via dispositions;
- a theory for multi-level modeling (Guizzardi et al., 2015a; Fonseca et al., 2021a).

This program was initially inspired by seminal work on ontological foundations for conceptual modeling (Wand and Weber, 1989, 1990; Weber, 1997) that had employed the work of physicist and philosopher of science Mario Bunge (Bunge, 1977) to evaluate a number of conceptual modeling languages, including NIAM (Weber and Zhang, 1991), ER (Wand et al., 1999), UML (Evermann and Wand, 2001), and OWL (Bera and Wand, 2004). Despite the fruitfulness of the application of Bunge's work to conceptual modeling, it soon became clear that there was a mismatch between the purposes for which Bunge's ontology was developed and the requirements of ontological foundations for conceptual modeling. This became manifest in the literature as the predictions made by the Bunge Wand Weber (BWW) approach found themselves in strong contrast with the intuitions and practical knowledge of modelers, as well as with some predictions unanimously shared by alternative approaches (Guizzardi et al., 2015b). For example, BWW disavowed reified relationships, a position that conflicted with modeling predictions made by other foundational theories, such as Jackendoff's semantic structures (Veres and Hitchman, 2002; Veres and Mansson, 2005), and with evidence from practitioners (Hitchman, 2003).

It was clear from the outset that an ontological theory for conceptual modeling would have to countenance both individuals and types, accounting for not only substantials and their types but also accidents and their types (e.g. particularized properties, moments, qualities, modes, tropes, abstract particulars, aspects, ways). In other words, a four-category ontology (Lowe and Lowe, 2006) was required. We needed particularized properties not only because they were of great importance in making sense of language and cognition (Parsons, 1990; Masolo et al., 2003; Davidson, 2001, Ch. 6), but because they would repeatedly appear in the discourse of conceptual modelers. Moreover, particularized relations (relationships) and particularized intrinsic properties (e.g., often represented by the so-called weak entities) are frequently modeled as bearers of other particularized properties in the practice of conceptual modeling. In fact, as demonstrated by Guizzardi and colleagues (see Guizzardi, 2005; Guizzardi et al., 2006; Guarino and Guizzardi, 2015), many conceptual modeling problems can hardly be solved without considering particularized properties.

In initial papers for this project, Guizzardi and Wagner attempted to employ the General Formal Ontology (GFO) and the General Ontology Language (GOL) being developed in Leipzig, Germany, as a reference theory (Heller and Herre, 2004; Herre et al., 2004). More or less at the same time, a strong cooperation was established between them and the Laboratory for Applied Ontology (LOA - Trento, Italy), which was concurrently developing the Descriptive Ontology for Linguistic and Cognitive Engineering (DOLCE; Masolo et al., 2003). In this setting, their first attempt was to unify DOLCE and GFO to produce a reference foundational ontology for conceptual modeling, hence the name Unified Foundational Ontology (Guizzardi and Wagner, 2004b). Both theories were philosophically sound, formally characterized, and based on the so-called Aristotelian Square, i.e., they were 'four-category ontologies' (Lowe and Lowe, 2006).

UFO has since evolved, always focused on the requirements of the conceptual modeling discipline. In particular, ontological foundations for conceptual modeling would demand micro-theories to address its most fundamental constructs, namely, entity types and relationship types. 1 So, any reference theory for conceptual modeling would need a rich theory of entity (object) types and a rich theory of domain (also called material) relations. In the case of the former, we needed something in the spirit of the ontology of universals underlying the OntoClean methodology (Guarino and Welty, 2009) in order to systematize a number of notions that were pervasive in the conceptual modeling literature (e.g., types, roles, phases or states, mixins) but for which there were no precise definitions or consensus (Guizzardi, 2005). In that respect, GFO's theory of universals still does not recognize these notions and DOLCE does not include universal as a category (DOLCE was designed as an ontology of particulars). Regarding the latter, DOLCE still does not include a theory of particularized relational properties (relational qualities) and the GFO theory of relations is subject to the so-called Bradley's Regress (Bradley, 1893) and, hence, it can only be instantiated by infinite (logical) models. This feature renders it ill-suited for most conceptual modeling applications. Finally, there were many additional specific aspects needed for a general ontology for conceptual modeling that were not addressed by the existing approaches (e.g., attributes and datatypes, a rich theory of cognitively/linguistically motivated part-whole relations, higher-order types).

UFO's evolution has also been influenced by its applications over the years. It has been employed as a basis for analyzing, reengineering, and integrating many modeling languages and standards in different domains (e.g., UML, BPMN, ArchiMate), as well as for the development of core and domain ontologies in different areas (Guizzardi et al., 2015b). For instance, it has been successfully used to provide conceptual clarification in complex domains such as risk, services, trust, law, biodiversity, design science research, among many others (a more comprehensive list is provided in Section 5).

Of all UFO's applications, one deserves special attention, namely, the use of UFO in the design of an ontology-driven conceptual modeling language, which later came to be known as OntoUML (Guizzardi, 2005). This is a language that reflects the ontological micro-theories comprising UFO. The observation of the application of OntoUML over the years conducted by several groups in a variety of domains also amounted to a fruitful empirical source of knowledge regarding the language and its foundations. 2 In this paper, we incorporate the latest developments of UFO arising out of these observations (Guizzardi et al., 2021). More specifically, the fine-grained distinctions among types (differentiating types according to meta-types such as Kinds , Phases , Roles and Mixins ) that were before only applied to substantials are now applied to endurants in general (including thus existentially dependent endurants such as: qualities , e.g., the perceived value of the experience, the color of the apple; modes , e.g., Paul's Dengue Fever, Matteo's capacity of programming in Scratch; and relators , e.g., John and Mary's Marriage, Giovanni's Employment at the UN). These were needed to capture subtle aspects of domains such as value, service, economic exchange, and many others (Blums and Weigand, 2017; Carmo et al., 2017; Guarino and Guizzardi, 2015; Zamborlini et al., 2017), and are also employed in some cases presented in this paper.

This paper can be consumed as an introduction to UFO, as we cover its main tenets (Section 2), its formalization (Section 3), its application to relevant illustrative domains (Section 4), and its relevance in the field of applied ontology and conceptual modeling (Section 5). Alternatively, readers interested in comparing UFO's modeling approach with those of other foundational ontologies in this special issue may proceed directly to Section 4. As these examples are mainly represented by means of OntoUML models and all axioms in the paper are preceded by descriptions in natural language, the axioms can be largely skipped, with Section 3 serving as a reference of the axiomatization following the examples for those concerned with a more precise representation of UFO's approach.

1 Hence, the name of the so-called Entity-Relationship approach that gives the name to the most important conference in conceptual modeling!

2 Several dozens of these models are available at http://purl.org/krdb-core/model-repository/.

## 2. Principles and structure of UFO

The objective of UFO was, from the beginning, to provide foundations for domain analysis in conceptual modeling, as well as for designing concrete models and modeling grammars. The idea was to develop a 'Calculus of Content' aimed at supporting the ontological analysis, conceptual clarification, and semantic explicitation of the content embedded in representation artifacts. These, in turn, should support human users in tasks such as domain understanding, problem-solving, and meaning negotiation (Guarino et al., 2020).

As defended by the philosopher Kit Fine, '[...] the fundamental question of ontology is not 'what is there?' but 'what is real?'[...] As a first stab, [...] what is real is what one must make reference to in giving a description of reality. ' . 3 In this spirit, UFO aims at providing instruments for describing what is real, at the mesoscopic level, and as accounted for by human cognition. For this reason, not only rocks and animals are real, but so are enrollments, employments, presidential mandates, symptoms, covalent bonds, birthday parties and football matches, colors and electrical charges, organizations and constitutions, software systems and derivative contracts.

Given these objectives, UFO was constructed as a descriptive (as opposed to a revisionary ) project (Strawson, 1959). This means that it is an ontology that takes into full consideration both cognitive and linguistic aspects informing its constituting categories. However, this is far from saying that reality is purely cognitively constructed. In this sense and, as put by Smith (2019), '[t]his is not to say that ontological items or entities - objects, properties, states of affairs, etc. - are ways of taking the world. Tables, detente, machinists, and love affairs are absolutely not merely epistemic entities... In that sense, [this view] is stubbornly realist: all these entities are things beyond us, things in the world. [They] are not 'ways of taking the world', They are the world taken a certain way. ' . From considering that 'the world can be taken in many ways' (i.e., a pluralism of worldviews), it does not follow that anything goes, i.e., that all worldviews are equally valid or even acceptable. We should still 'carve reality at its joints', 'joints' that are supplied by concrete causal nexus of properties associated with natural and nominal kinds (Keil, 1992). There are, however, multiple ontologically viable and cognitively useful ways of doing that. The ultimate goal of this project is, thus, providing well-founded engineering mechanisms for helping modelers to achieve intra-worldview consistency , i.e., ontological consistency when taking the world a certain way, and inter-worldview interoperability , i.e., making explicit the ontological commitments of a worldview such that different worldviews can safely interoperate.

UFO is organized in three main fragments:

- UFO-A , which is an ontology of endurants;
- UFO-C , which is an ontology of social and intentional entities build on the foundations provided by the other two (de Oliveira Bringuente et al., 2011).
- UFO-B , which is an ontology of perdurants (Benevides et al., 2019b);

In this paper, we focus on the categories around UFO-A and a few categories of UFO-B, which are depicted in Fig. 1. UFO is a 3D ontology having, as a fundamental distinction, the one between endurants (e.g., Mick Jagger, the Moon, John's headache, Mary's marriage to Paul) and perdurants (e.g., the 2020 U.S. presidential election, the World War II, the UEFA Euro 2021 Final), as opposed to a 4D ontology in which all concrete individuals are perdurants. Endurants are individuals that exist in time with all their parts. They have essential and accidental properties and, hence, they can qualitatively change while maintaining their numerical identity (i.e., while remaining the same individual). The sorts of changes an endurant can undergo while maintaining its identity is defined by the unique Kind it instantiates.

[3 https://www.3-16am.co.uk/articles/metaphysical-kit](https://www.3-16am.co.uk/articles/metaphysical-kit)

Fig. 1. The taxonomy of UFO.

[FIGURE]

Perdurants 4 are individuals that unfold in time accumulating temporal parts. They are manifestations of dispositions and only exist in the past. As such, perdurants are modally fragile , i.e., there is no crossworld identity between them and, hence, they cannot be in any way different than what they are (Guizzardi et al., 2016). Changes are perdurants but perdurants cannot be the subject of change. Any apparent change to a perdurant is either a variation (i.e., different temporal parts of an event having incompatible properties), or a change happening to some underlying endurant that is the focus of that event (Guizzardi et al., 2016). An endurant then participates in a perdurant if that perdurant has a part that is a manifestation of a disposition inhering in that endurant (Benevides et al., 2019b).

Regarding the endurant fragment of the ontology, UFO is an ontology based of the so-called Aristotelian Square , thus, accounting for both substantial individuals (or Substantials ), i.e., independent entities (e.g., Mick Jagger, the Free University of Bozen-Bolzano), as well as particularized properties, i.e., existentially dependent entities or moments , these last ones termed aspects, abstract particulars, or variable tropes (Moltmann, 2020). Moments are parasitic entities and can only exist by inhering in other entities.

4 We often refer to perdurants as events, given that the latter is more easily understood by a non-philosophical audience.

Intrinsic moments are existentially dependent on a single individual. These include qualities , i.e., reifications of categorical properties such as color, height, weight, electrical charge. Qualities are entities that can be directly projected into certain value spaces. The latter, termed quality structures , are abstract entities delimiting the space of possible values (qualia, singular quale ) for qualities of a given quality type. Quality structures can be either one-dimensional, in which case they are termed quality dimensions , or composed of multiple co-dependent dimensions (see also integral dimensions, Gärdenfors, 2004), in which case they are termed quality domains . While the former includes height and weight dimensions as examples (structures isomorphic to a subset of the positive half-line of real numbers), the later includes as examples the color spindle and the taste tetrahedron.

Intrinsic moments also include modes . Modes can bear their own moments, including their own qualities, which can vary in independent ways. The category of modes include dispositions (e.g., functions, capabilities, capacities, vulnerabilities, etc.) as well as externally dependent entities (e.g., the love of John for Mary, the commitment of Paul towards Clara to meet for lunch next Friday). Externally dependent modes inhere in an entity while being externally dependent on another entity. 5 A particularly interesting type of externally dependent mode is a qua individual , which is a mode composed of other externally dependent modes that share the same bearer, the same source of external dependence, and the same foundational event (Guizzardi, 2005). For instance, the sum of all commitments and claims of John towards Mary form such a complex mode that we could call John-qua-husband-of-Mary, as they all inhere in John, are externally dependent of Mary, and are founded in that particular wedding event. Likewise, a relator is a moment (i.e., an existentially dependent entity) that is an aggregation of qua individuals (Guizzardi, 2005). For instance, John and Mary's Marriage is composed of John-quahusband-of-Mary and Mary-qua-wife-of-John. A relator is, hence, existentially dependent on multiple individuals, namely, the bearers of its constituting qua individuals. Examples of relators include marriages, enrollments, employments, contracts, and presidential mandates. Externally dependent modes as well as relators serve as truthmarkers of material relations (Guarino and Guizzardi, 2015; Guarino et al., 2019), the first for one-sided relations and the second for double-sided (or multi-sided) ones (Fonseca et al., 2019).

Both substantials and moments are full-fledged endurants, being both able to bear moments, i.e., including cases involving moments of moments (e.g., the intensity of my headache, the hue of the color). All endurants can have essential and accidental properties and can qualitatively change while maintaining their identity, provided they respect the principle of application provided by their respective Kinds. For example, John and Mary's marriage can change from a marriage with full separation of assets to one with partial separation of assets. The way their marriage can change is defined by the Kind it instantiates (marriage). Additionally, all endurants can have parts (e.g., George's employment to the UN is composed of a number of mutual claims and obligations).

Mereologically complex substantials are characterized by the different unity conditions that bind their parts together:

- Quantities are maximally-topologically-self-connected (e.g., pieces) of homeomerous amounts of matter, e.g., that puddle of water, this particular pile of sand;
- Collectives are entities whose parts play the same role with respect to the whole, e.g., the Black Forest (as a collective of trees), a deck of cards, the Dutch-speaking group in the crowd; and
- Objects (aka functional complexes ) are entities whose parts play differentiated functional roles with respect to the whole, e.g., a human body, an organization, a computer, John's car.

5 That is, it is existentially dependent on an entity mereologically disjoint from the entity it inheres in (aka its bearer).

UFO is an ontology of both particulars and universals (or types), i.e., patterns of features that are repeatable across different particulars. In fact, UFO is an ontology that also countenances high-order types, i.e., types whose instances are also types. The hierarchy of types in UFO reflects on the one hand the existing distinctions among sorts of individuals. So, we have perdurant types, substantial types, moment types, etc. On the other hand, UFO employs a number of formal meta-properties to spawn a rich typology of endurant types (Guizzardi et al., 2021).

As previously mentioned, a fundamental sort of endurant type is a kind , which provides uniform principles of individuation, identity, and persistence to its instances. For example, the types person, dog, computer, car, headache, organization and marriage are typically considered to be kinds. Kinds apply to instantiating individuals in all possible situations in which these individuals exist, and hence kinds are rigid types, applying necessarily to their instances. A sortal is either a kind or a specialization of a kind, and every sortal that is not a kind specializes exactly one kind. These specializations can be either themselves rigid, in which case they are termed subkinds (e.g., hatchback car as a subkind of car; financial organization as a subkind of organization) or they can be anti-rigid , i.e., classifying only contingently their instances. Among the latter, we have sortals whose contingent classification conditions are intrinsic, termed Phases (e.g., teenager as a phase of person, hemorrhagic dengue fever as a phase of dengue fever, and tenured employment as a phase of employment), and we have sortals whose contingent classification conditions are relational, termed roles (e.g., employee as a role of a person in the scope of an employment relator, and husband as a role of a person in the scope of a marriage relator).

In contrast with sortals, non-sortals are types that represent common properties of individuals of multiple Kinds. These can be:

- categories : rigid types that define essential properties for their instances, e.g., the category 'physical object' describing the properties of having a mass and a spatial extension, common to things of the kinds car, person, bridge, cow, etc.;
- phase mixins : anti-rigid types that define contingent properties for their instances. Their instantiation is characterized by intrinsic contingent conditions . For example, the phase mixin 'living animal' may apply to instances of the kinds person, dog, and horse; the phase mixin 'functional device' may characterize instances of the kinds computer, watch, and espresso machine;
- role mixins : anti-rigid types that define contingent properties for their instances. Their instantiation is characterized by relational contingent conditions . Examples include 'customer' for the kinds person and organization, but also 'insured legal relator' for the kinds employment and enrollment;
- mixins : semi-rigid types that define properties that are essential to some of their instances but accidental to some other instances (e.g., being a 'music artist' is essential to bands but accidental to people).

## 2.1. Summary

For the sake of comparison with other foundational ontologies within this special issue, we summarize UFO's core positions in the list below:

- I. UFO distinguishes between endurants and perdurants. Endurants are individuals that exist in time with all their parts. Perdurants are individuals that unfold in time accumulating temporal parts. An endurant can change while maintaining its identity, a perdurant cannot.
- II. UFO accounts for the existence of both independent and dependent endurants. Independent endurants are called substantials, while those that existentially depend on other individuals are

dubbed moments. More precisely, a moment is said to inhere in another endurant. Perdurants are always dependent on the substantials that participate in them.

- III. Perdurants are past entities in UFO and cannot genuinely change. Alleged change in a perdurant is thus either a reflection of a perdurant having temporal parts with different properties, or, a change in an endurant (e.g., a mode or relator) of which the event is a manifestation. Thus, instead of admitting those entities that Stout refers to as 'processes' (Stout, 1997), we rather consider those underlying endurants as the subject of change, and track their manifestations in time.
- IV. UFO accounts for (particularized) intrinsic and relational properties, which can serve as truthmakers for different types of relations and attributes. Particularized intrinsic properties that can be projected into a value space are deemed qualities, whilst those that cannot are deemed modes. Particularized relational properties are called relators. The term quantity is reserved for substantials that are maximally-topologically-self-connected of homeomerous amounts of matter.
- V. In UFO, roles are anti-rigid types whose instantiation occur in virtue of relational conditions. Roles that can be instantiated by individuals of a single kinds are simply termed roles, while those that can be instantiated by individuals of different kinds (thus, adhering to different identity principles) are termed roleMixins. There is no explicit definition of function in UFO.

## 3. The formalization of UFO in first-order modal logic

In this section, we present a first-order modal theory of endurant types, in which types and their instances are both in the domain of quantification (i.e., first-order citizens), being connected by the instantiation relation (symbolized as ' : :'). For our purposes, the first-order modal logic QS5 plus the Barcan formula and its converse suffices (Fitting and Mendelsohn, 2012). That means that we assume a fixed domain of entities for every possible world, what is traditionally associated to a possibilistic view of the entities of the domain, i.e., the domain includes all the possibilia . The modal operators of necessity ( □ ) and possibility ( ♦ ) are used with their usual meaning.

We drop both the universal quantifier and the necessity operator in case their scope takes the full formula. Definitions, introduced by ' def = ', 'are to be viewed as extraneous conventions of notational abbreviation' (Quine, 1937, p. 72). Axioms, theorems and definitions are indexed as in '(a n )', '(t n )' and '(d n ),' respectively. In a few cases when it is necessary to refer to the original formalization of UFO, we use '( m.n )' to denote the n th axiom of the m th chapter of Guizzardi (2005). Finally, this section is based on a first-order logic formalization of UFO 6 specified in the TPTP syntax (Sutcliffe, 2017), and submitted to multiple automated provers for consistency and satisfability checks.

## 3.1. Types, individuals and instantiation

Firstly, types are implicitly defined as those entities that are possibly instantiated (a1), while individuals are those necessarily not instantiated (a2). The domain of : : is Type ∪ Individual (a3) and it follows from (a1) that the codomain is Type . We deal here only with first-order and second-order types (a4). Axioms (a1) and (a2) entail that entities are partitioned into individuals and types (t1), (t2).

6 The complete first-order logic formalization of UFO in TPTP is available at https://purl.org/ufo-formalization.

We introduce the specialization relation between types ( ⊑ ) defining it in terms of necessary extensional inclusion (a5), i.e., inclusion of their instances. Proper specialization ( ⊏ ) is defined in the usual way (d1). By means of (a5), it follows that the specialization relation is quasi-reflexive (t3) and transitive (t4). Whenever two types have a common instance, they must share a supertype or a subtype for this instance (a6).

```
a5 x ⊑ y ↔ Type (x) ∧ Type (y) ∧ □ ( ∀ z(z :: x → z :: y)) d1 x ⊏ y def = x ⊑ y ∧¬ (y ⊑ x) t3 x ⊑ y → (x ⊑ x ∧ y ⊑ y) t4 x ⊑ y ∧ y ⊑ z → x ⊑ z a6 ∀ t 1 , t 2 , x((x :: t 1 ∧ x :: t 2 ∧¬ (t 1 ⊑ t 2 ) ∧¬ (t 2 ⊑ t 1 )) → ( ∃ t 3 (t 1 ⊑ t 3 ∧ t 2 ⊑ t 3 ∧ x :: t 3 ) ∨ ∃ t 3 (t 3 ⊑ t 1 ∧ t 3 ⊑ t 2 ∧ x :: t 3 )))
```

Among the individuals, there are concrete individuals (a7) and abstract individuals (a8)-(a10). Concrete individuals are further differentiated into endurants (a11) and perdurants (a12). The classification of individuals into concrete and abstract individuals (a9), as well as the classification of concrete individuals into endurants and perdurants (a13)-(a14), are disjoint and complete.

```
a7 ConcreteIndividual (x) → Individual (x) a8 AbstractIndividual (x) → Individual (x) a9 ConcreteIndividual (x) →¬ AbstractIndividual (x) a10 Individual (x) ↔ ConcreteIndividual (x) ∨ AbstractIndividual (x) a11 Endurant (x) → ConcreteIndividual (x) a12 Perdurant (x) → ConcreteIndividual (x) a13 Endurant (x) →¬ Perdurant (x) a14 ConcreteIndividual (x) ↔ Endurant (x) ∨ Perdurant (x)
```

Moreover, types are classified into types of endurants and types of perdurants (a15)-(a17), which are both disjoint (a17).

```
a15 EndurantType (x) → Type (x) a16 PerdurantType (x) → Type (x) a17 EndurantType (x) →¬ PerdurantType (x)
```

## 3.2. Some relevant type qualifications

UFO includes categories for types of endurants based on their rigidity and sortality. We implicitly define rigidity of endurant types as rigid (a18), anti-rigid (a19) and semi-rigid (a20), concluding that every endurant type is either one of the three (t5)-(t6). Also, rigid and semi-rigid types cannot specialize anti-rigid ones (t7)-(t8).

```
a18 Rigid (t) ↔ EndurantType (t) ∧∀ x( ♦ (x :: t) → □ (x :: t)) a19 AntiRigid (t) ↔ EndurantType (t) ∧∀ x( ♦ (x :: t) → ♦ ( ¬ x :: t)) a20 SemiRigid (t) ↔ EndurantType (t) ∧¬ Rigid (t) ∧¬ AntiRigid (t) t5 EndurantType (t) ↔ Rigid (t) ∨ AntiRigid (t) ∨ SemiRigid (t) t6 ¬∃ x(( Rigid (x) ∧ AntiRigid (x)) ∨ ( Rigid (x) ∧ SemiRigid (x)) ∨ ( SemiRigid (x) ∧ AntiRigid (x))) t7 ¬∃ x, y( Rigid (x) ∧ AntiRigid (y) ∧ x ⊑ y)
```

```
t8 ¬∃ x, y( SemiRigid (x) ∧ AntiRigid (y) ∧ x ⊑ y)
```

On sortality , our basic assumption is that every endurant necessarily instantiates a kind (a21), and everything necessarily instantiates at most one kind (a22). We implicitly define sortals as those endurant types whose instances necessarily instantiate the same kind (a23); while a non-sortal is an endurant type that is necessarily not a sortal (a24). As theorems, we have that: kinds are rigid (t9); kinds are necessarily disjoint (t10); a kind cannot specialize a different kind (t11); kinds are sortals (t12); sortals specialize a kind (t13); sortals cannot specialize different kinds (t14); a non-sortal cannot specialize a sortal (t15); and non-sortals do not have direct instances, their instances are also instances of some sortal that either specializes the non-sortal, or specializes a common non-sortal supertype (t16).

```
a21 Endurant (x) →∃ k( Kind (k) ∧ □ (x :: k)) a22 Kind (k) ∧ x :: k →¬ ♦ ( ∃ z( Kind (z) ∧ x :: z ∧ z ̸= k)) a23 Sortal (t) ↔ EndurantType (t) ∧∃ k( Kind (k) ∧ □ ( ∀ x(x :: t → x :: k))) a24 NonSortal (t) ↔ EndurantType (t) ∧¬ Sortal (t) t9 Kind (k) → Rigid (k) t10 Kind (x) ∧ Kind (y) ∧ x ̸= y → □ ( ¬∃ z(z :: x ∧ z :: y)) t11 Kind (x) ∧ Kind (y) ∧ x ̸= y → ( ¬ (x ⊑ y) ∧¬ (y ⊑ x)) t12 Kind (t) → Sortal (t) t13 Sortal (x) →∃ k( Kind (k) ∧ x ⊑ k) t14 ¬∃ x, y, z( Kind (y) ∧ Kind (z) ∧ y ̸= z ∧ x ⊑ y ∧ x ⊑ z) t15 ¬∃ x, y( NonSortal (x) ∧ Sortal (y) ∧ x ⊑ y) t16 ( NonSortal (t) ∧ x :: t) → ( ∃ s( Sortal (s) ∧ s ⊑ t ∧ x :: s) ∨∃ n, s( NonSortal (n) ∧ Sortal (s) ∧ s ⊑ n ∧ t ⊑ n ∧ x :: s))
```

Regarding the leaves of the taxonomy of endurant types according to their sortality and rigidity, kinds and subkinds are disjoint (a25), and together encompass all rigid sortals (a26). Phases and roles are disjoint (a27), and together encompass all antirigid sortals (a28). Semi-rigid sortals are those that are semi-rigid and sortal (a29). Categories are those types that are rigid and non-sortal (a30). Mixins are those types that are semirigid and non-sortal (a31). Phase-mixins and role-mixins are disjoint (a32), and together encompass all antirigid non-sortals (a33). Let L T be the set of the leaf categories of the aforementioned taxonomy of endurant types { Kind , SubKind , Role , Phase , SemiRigidSortal , RoleMixin , PhaseMixin , Category , Mixin }, it follows that these leaf categories are pairwise disjoint (t17) and complete (t18).

```
a25 ¬∃ t ( Kind (t) ∧ SubKind (t)) a26 Kind (t) ∨ SubKind (t) ↔ Rigid (t) ∧ Sortal (t) a27 ¬∃ t ( Phase (t) ∧ Role (t)) a28 Phase (t) ∨ Role (t) ↔ AntiRigid (t) ∧ Sortal (t) a29 SemiRigidSortal (t) ↔ SemiRigid (t) ∧ Sortal (t) a30 Category (t) ↔ Rigid (t) ∧ NonSortal (t) a31 Mixin (t) ↔ SemiRigid (t) ∧ NonSortal (t) a32 ¬∃ t ( PhaseMixin (t) ∧ RoleMixin (t)) a33 PhaseMixin (t) ∨ RoleMixin (t) ↔ AntiRigid (t) ∧ NonSortal (t)
```

t17 ∧ i,j ∈ L T ,i ̸= j i(t) →¬ j(t) t18 EndurantType (x) ↔ ∨ i ∈ L T i(x)

## 3.3. Endurants

On the UFO taxonomy of endurants, Endurant is partitioned into Substantial and Moment (a34), (a35). Additionally, Substantial is partitioned into Object , Collective and Quantity (a36), (a37), (a38) and (a39). Further, Moment is partitioned into Relator and IntrinsicMoment (a40), (a41). Finally, IntrinsicMoment is partitioned into Mode and Quality (a42), (a43). Let L e be the set of the leaf categories of endurants { Object , Collective , Quantity , Relator , Mode , Quality }, it is a theorem that these leaf categories partition Endurant (t19), (t20).

```
a34 Substantial (x) ∨ Moment (x) ↔ Endurant (x) a35 ¬∃ x( Substantial (x) ∧ Moment (x)) a36 Object (x) ∨ Collective (x) ∨ Quantity (x) ↔ Substantial (x) a37 ¬∃ x( Object (x) ∧ Collective (x)) a38 ¬∃ x( Object (x) ∧ Quantity (x)) a39 ¬∃ x( Collective (x) ∧ Quantity (x)) a40 Relator (x) ∨ IntrinsicMoment (x) ↔ Moment (x) a41 ¬∃ x( Relator (x) ∧ IntrinsicMoment (x)) a42 Mode (x) ∨ Quality (x) ↔ IntrinsicMoment (x) a43 ¬∃ x( Mode (x) ∧ Quality (x)) t19 ∧ i,j ∈ L e ,i ̸= j i(t) →¬ j(t) t20 Endurant (x) ↔ ∨ i ∈ L e i(x)
```

## 3.4. Endurant types

We define an orthogonal taxonomy of endurant types according to the ontological nature of their instances. Let P E be the set of pairs {( EndurantType , Endurant ); ( PerdurantType , Perdurant ); ( SubstantialType , Substantial ); ( MomentType , Moment )}; and P E ′ be the set of pairs {( ObjectType , Object ); ( CollectiveType , Collective ); ( QuantityType , Quantity ); ( RelatorType , Relator ); ( ModeType , Mode ); ( QualityType , Quality )}. We implicitly define these types in the axiom schema (a44). It follows that the types in P E ′ are pairwise disjoint (t21).

```
a44 ∧ (i,j) ∈ P E ∪ P E ′ i(t) ↔ Type (t) ∧ □ ( ∀ x(x :: t → j(x))) t21 ∧ i,j ∈{ k | (k, _ ) ∈ P E ′ } ,i ̸= j i(x) →¬ j(x)
```

Kinds are also specialized according to the ontological nature of their instances. Let P K be the set of pairs {( ObjectKind , ObjectType ); ( CollectiveKind , CollectiveType ); ( QuantityKind , QuantityType ); ( RelatorKind , RelatorType ); ( ModeKind , ModeType ); ( QualityKind , QualityType )}. We implicitly define these kinds in the axiom schema (a45). It is a theorem that all entities that possibly instantiate an endurant kind are endurants (t22). Moreover, every endurant instantiates one of the specific endurant kinds (a46). It follows that every endurant sortal is a type in L ES = { ObjectKind , CollectiveKind , QuantityKind , RelatorKind , ModeKind , QualityKind , SubKind , Phase , Role , SemiRigidSortal } (t23); and that some sortals specialize specific kinds (t24).

- a45 ∧ (i,j) ∈ P K i(t) ↔ j(t) ∧ Kind (t) t22 ♦ ( ∃ k(( ObjectKind (k) ∨ CollectiveKind (k) ∨ QuantityKind (k) ∨ RelatorKind (k) ∨ ModeKind (k) ∨ QualityKind (k)) ∧ x :: k)) → Endurant (x) a46 Endurant (x) → ♦ ( ∃ k(( ObjectKind (k) ∨ CollectiveKind (k) ∨ QuantityKind (k) ∨ RelatorKind (k) ∨ ModeKind (k) ∨ QualityKind (k)) ∧ x :: k)) t23 EndurantType (x) ∧ Sortal (x) → ∨ i ∈ L ES i(x) ∧ ∨ ∨ ∨ ∨

We have as theorems that the leaves of the taxonomy of endurant types L ET = { ObjectKind , CollectiveKind , QuantityKind , SubKind , RelatorKind , ModeKind , QualityKind , SemiRigidSortal , Category , Phase , Mixin , Role , PhaseMixin , RoleMixin } - are pairwise disjoint (t25); and that every endurant type is a type in L ET (t26).

- t24 ( Sortal (t) ( ObjectType (t) CollectiveType (t) QuantityType (t) RelatorType (t) ModeType (t) ∨ QualityType (t))) ↔∃ k(( ObjectKind (k) ∨ CollectiveKind (k) ∨ QuantityKind (k) ∨ RelatorKind (k) ∨ ModeKind (k) ∨ QualityKind (k)) ∧ t ⊑ k)

<!-- formula-not-decoded -->

## 3.5. Mereology

In the axioms (a47)-(a52) we formalize general extensional mereology (see Hovda, 2009). We present here the main axioms and definitions; for the purposes of the subsequent definitions, that suffices.

```
a47 P (x, x) (reflexivity) a48 P (x, y) ∧ P (y, x) → x = y (anti-symmetry) a49 P (x, y) ∧ P (y, z) → P (x, z) (transitivity) a50 O (x, y) ↔∃ z( P (z, x) ∧ P (z, y)) (Overlap) a51 ¬ P (y, x) →∃ z( P (z, y) ∧¬ O (z, x)) (Strong supplementation) a52 PP (x, y) ↔ P (x, y) ∧¬ P (y, x) (Proper Part)
```

## 3.6. Composition

We summarize below the treatment of functional parts by Guizzardi (2005). We introduce a relation F (x, x ′ ) between an object x and a type x ′ , whose meaning is that ' x functions as x ′ .' The relation of generic functional dependence between types is then defined as follows.

<!-- formula-not-decoded -->

We define the functional dependence between individuals x and y of types x ′ and y ′ (respectively) as follows.

<!-- formula-not-decoded -->

We can now introduce the notion of component of that we are going to use in the subsequent example.

<!-- formula-not-decoded -->

## 3.7. Constitution

We adopt here a very simple and preliminary view of constitution. First, it is a relation that holds between things of the same ontological category (a56).

```
a56 constitutedBy (x, y) → (( Endurant (x) ↔ Endurant (y)) ∧ ( Perdurant (x) ↔ Perdurant (y)))
```

However, following Baker (2007), we have that constitution holds between things of different Kinds (a57). From this, we have the non-reflexivity of constitution as a theorem (t27). Notice that by instantiating different kinds, constituent and constituted obey different principles of identity, and have different modal properties (including different essential parts). 7

```
a57 constitutedBy (x, y) ∧ (x :: x ′ ) ∧ (y :: y ′ ) ∧ Kind (x ′ ) ∧ Kind (y ′ ) → x ′ ̸= y ′ t27 ¬ constitutedBy (x, x)
```

Any complete theory of constitution should explain why material properties of the constituent are systematically related to those of the constituted. Typically, for physical endurants, the spatial location of the former are inherited by the latter; 8 for perdurants, the temporal properties of the former are constrained by the latter. 9 However, these derived relations can apply to many other properties, e.g., the weight, volume, color, chemical structure of the statue are derived from the properties of the constituting clay (Baker, 2007). Now, it would be hard to defend that these derivation relations work the other way around as well (e.g., that the weight, volume, color, chemical structure of the lump of clay are derived from the properties of the constituted statue). In fact, although it is natural to conceptualize The Beatles as being constituted by collective of John, Paul, George, Ringo, it is utterly unnatural to conceptualize the collective as being constituted by The Beatles . Why is that? We believe that this is because constitution relies on a notion of grounding . This seems to also explain requirements such as the one proposed by Baker (2007) that special circumstances must hold for the constituent to constitute the constituted (e.g., for the clay to constitute the statue, an intentional act of the sculptor is required), and that these circumstances are both necessary and sufficient.

This asymmetry is also often framed in terms of asymmetric cases of dependence (again, strongly connected to grounding). For example, every instance of statue of clay must be constituted by a particular lump of clay, but not the other way around, i.e., lumps of clay can exist without constituting statues. In other words, statues of clay are generically dependent on the type Lump of Clay. This can be captured with the notions of Generic Constitutional Dependence (GCD), between types x ′ and y ′ , as well as the type-level relation of Constitution (a59) between x of type x ′ , and y of type y ′ .

```
a58 GCD (x ′ , y ′ ) ↔∀ x(x :: x ′ ) →∃ y(y :: y ′ ) ∧ constitutedBy (x, y) a59 Constitution (x, x ′ , y, y ′ ) ↔ (x :: x ′ ) ∧ (y :: y ′ ) ∧ GCD (x ′ , y ′ ) ∧ constitutedBy (x, y)
```

Now, using another example, we can have a Boxing Match being constituted by one or more punches (again, an asymmetric dependence). In this case, however, a specific Boxing Match is constituted by specific punching events, i.e., a case of specific dependence . This is because we are dealing here with a constitution relation between events and, as previously discussed, events are modally fragile entities and, hence, all their parts and constituents are necessary constituents (a60).

7 Thomson (1998) requires the following condition to hold in constitution: 'there must be at least one essential part of the constituent, and no part of the constituent is essential to the constituted' .

8 We do admit, however, relations of constitution between non-physical endurants. For example, a software program is constituted by software code, not identical to it.

9 For the case of parthood between events (Benevides et al., 2019b), we have that the temporal interval framing the parts are part of the one framing the whole. Mutatis mutandis , for the case of constitution between events, we assume the same here for the relation between the temporal interval framing the constituent and the one framing the constituted.

```
a60 ∀ x, y Perdurant (x) ∧ constitutedBy (x, y) → □ ( ex (x) → constitutedBy (x, y))
```

In light of these notions of dependence, constitution seems to be similar to the relation of functional parthood ( componentOf ). ComponentOf is a material relation that also requires 'special circumstances' in order to hold. Due to the different configurations involving different types of dependence relations holding between functional parts, functional parthood is not irrestrictively transitive. In fact, transitivity only holds in certain scopes defined by these 'special circumstances'. Maybe an analogous case can be made to explain why transitivity does not seem to hold for constitution irrestrictively either. For example, the human tissue that constitutes Paul McCartney does not constitute The Beatles . Perhaps, like parthood (Guizzardi, 2005), constitution is not a single relation but a family of relations, each requiring additional axioms extending a very minimal common core.

Again, we advocate that a complete theory of constitution requires a proper theory of grounding. For this reason, we postpone proposing a complete theory for the former relation in UFO until we can fully advance a complete theory of the latter relation. In any case, to honor this strong intuition based on grounding (which is asymmetric) and asymmetric dependence, we assume here that constitution is an asymmetric relation (a61).

```
a61 constitutedBy (x, y) →¬ constitutedBy (y, x)
```

In summary, in this rather simplified form, the general relation of constitution is taken here as a nonreflexive and asymmetric relation. Moreover, it is a relation that holds between entities of the same ontological categories but between entities of different Kinds. Specific types of constituents and constituted entities can extend this minimal axiomatization, for example, to constraint relations between properties of physical endurants or events. A fuller theory of derivation of properties in this sense, however, waits for a fuller theory of grounding.

## 3.8. Existence and existential dependence

UFO introduces an existence predicate defined on any possible entity. In principle, we can view existence as related to time, ex (x, t) , however, as we are proposing here a single time slice formalization of UFO, we introduce in (a62) existence as a unary predicate ex (x) . By means of the existence predicate, we implicitly define in (a63) the relation of existential dependence between two entities, ed (x, y) . We also implicitly define the notion of existential independence, ind (x, y) , accordingly (a64).

```
a62 ex (x) → Thing (x) a63 ed (x, y) ↔ □ ( ex (x) → ex (y)) a64 ind (x, y) ↔¬ ed (x, y) ∧¬ ed (y, x)
```

## 3.9. Moments and inherence

We summarize a few points of the formalization of substantials and moments of the original UFO, as they shall be required in the subsequent sections. Moments are known as variable tropes , abstract particulars, or particular qualities in the philosophical literature (Guizzardi, 2005). In UFO, moments can be viewed either as individualized properties, such as the color or the weight of an object, for the case of intrinsic moments, or a marriage or an enrollment, for the case of relational moments (relators), cf. (a40), (a41). The relation that connects moments to the object that they are about is the relation of inherence . Inherence is a type of existential dependence relation (a65) holding between a moment and an entity of which it depends, called its bearer (a66).

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

Moreover, a moment cannot inhere in two separate individuals (a67), this is the so-called nonmigration or non-transferability principle (a67).

<!-- formula-not-decoded -->

Moments can also be involved in chains of inherence relations (d2), which are ultimately grounded on a unique entity that does not inhere in anything else. This entity that we will call here the Ultimate Bearer . (d3). Furthermore, the ultimate bearer of a moment is unique (a68).

<!-- formula-not-decoded -->

```
d2 momentOf (m, x) = inheresIn (m, x) ∨∃ y( inheresIn (m, y) ∧ momentOf d3 ultimateBearerOf (b, m) def =¬ Moment (b) ∧ momentOf (m, b) a68 Moment (m) →∃! b ultimateBearerOf (b, m)
```

Finally, in line with what was proposed originally in UFO (Guizzardi, 2005), we have the following theorems (t28)-(t30), i.e., inherence is a non-reflexive, asymmetric and anti-transitive relation.

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

```
¬ →¬ ∧ →¬
```

## 3.10. Relators

We summarize below the presentation of relators by Guizzardi (2005). Recent investigations on relators, relations, and their connections to perdurants (events) have been proposed by Guarino and Guizzardi (2015, 2016). We start by defining externally dependent modes (a70): a mode x that is existentially dependent on an entity that is independent of the bearer of x .

```
a69 externallyDependent (x, y) ↔ ed (x, y) ∧∀ z ( inheresIn (x, z) → ind (y, z)) a70 ExternallyDependentMode (x) ↔ Mode (x) ∧∃ y( externallyDependent (x, y)) ( 6 . 42 )
```

Externally dependent modes indeed capture truly relational qualities. For instance, by being married to Mary, in virtue of this relation, John acquires a number of properties (i.e. modes ) that depend on John's relationship with Mary; John's commitment towards Mary is a mode that depends on an individual that is existentially independent of the bearer of John's commitment. The condition of existential independence excludes that an externally dependent mode may depend on individuals that are ontologically too close to the bearer of the mode. For instance, the courage of John is a mode that depends on John, who is not existentially independent of himself; for this reason, the courage of John is a mode that is not externally dependent.

Externally dependent modes (as well as relators, as we discuss later) are founded by means of a unique event (a71), (a72). E.g., John's conjugal commitments towards Mary are founded on the event of the wedding between John and Mary. Since every externally dependent mode is founded by an unique event, we can define foundationOf (x) by means of a definite description (d4).

```
a71 foundedBy (x, y) → ( ExternallyDependentMode (x) ∨ Relator (x)) ∧ Perdurant (y) a72 ExternallyDependentMode (x) →∃! y( foundedBy (x, y)) d4 foundationOf (x) = y ↔ foundedBy (x, y)
```

We can now explain what it means for an individual x to be a qua individual of another individual y : the relation quaIndividualOf holds between x and y iff x is the sum of all externally dependent modes of y that share the same foundational event (a73). Moreover, an entity is a qua individual iff it is a quaIndividualOf another entity (a74). For instance, in virtue of the marriage with Mary, John is the bearer of a number of externally dependent modes related to conjugal commitments that constitute Johnqua-husband-of-Mary. For this reason, we view a qua individual as a complex externally dependent mode (a75), and so it has a unique foundation, which is the same as the foundation of its parts (a31). Finally, qua individuals are genuine individuals in the sense that they cannot be attached to two distinct particulars (a76). E.g., John qua student is the qua individual of John, not of any other person.

```
a73 quaIndividualOf (x, y) ↔∀ z ( O (z, x) ↔ ( ExternallyDependentMode (z) ∧ inheresIn (z, y) ∧ foundationOf (z) = foundationOf (x))) t31 quaIndividualOf (x, y) ∧ x ′ P x → foundationOf (x) = foundationOf (x ′ ) a74 QuaIndividual (x) ↔∃ y quaIndividualOf (x, y) a75 QuaIndividual (x) → ExternallyDependentMode (x) a76 quaIndividualOf (x, y) ∧ quaIndividualOf (x, y ′ ) → y = y ′
```

We assume that every relator is founded on a unique event (a77), which is also the foundation of the parts of the relator. Relators are then implicitly defined by (a79): they are sums of qua individuals that share the same foundation and are existentially dependent on each other.

```
a77 Relator (x) →∃! y( foundedBy (x, y)) a78 Relator (x) ∧ y P x → foundationOf (x) = foundationOf (y) a79 Relator (x) ↔∃ y( PP (y, x)) ∧∀ y, z(( PP (y, x) ∧ PP (z, x)) → ( QuaIndividual (y) ∧ QuaIndividual (z) ∧ ( foundationOf (y) = foundationOf (z)) ∧ ed (y, z) ∧ ed (z, y))) ∧ ∀ y, z(( PP (y, x) ∧ QuaIndividual (z) ∧ ( foundationOf (y) = foundationOf (z)) ∧ ed (y, z) ∧ ed (z, y)) → PP (z, x))
```

For example, John and Mary's wedding is the foundation of a number of externally dependent modes of John that depend on Mary and of Mary that depend on John, the sum of which constitutes the marriage relator.

According to this view, relators bring about qua individuals. By (a79), there must exist at least two qua individuals, x ′ and x ′′ , that are part of the relator, given by the existence of a proper part in (a79)

and by strong supplementation (a51). By (t32), those qua individuals are qua individuals of some other individual, y ′ and y ′′ . Thus, we establish (t32).

```
t32 Relator (x) →∃ x ′ , x ′′ , y ′ , y ′′ ( quaIndividualOf (x ′ , y ′ ) ∧ quaIndividualOf (x ′′ , y ′′ ))
```

We introduce the relation of mediation , mediates (x, y) , between a relator x and an individual y that the relator connects in a relational statement (a80).

```
a80 mediates (x, y) ↔ Relator (x) ∧ Endurant (y) ∧∃ z.( quaIndividualOf (z, y) ∧ P zx) t33 Relator (x) →∃ y, z(y ̸= z ∧ mediates (x, y) ∧ mediates (x, z))
```

By axiom (a79), any relator has at least two distinct qua individuals as parts. Those qua individuals are associated to distinct individuals by (a74) and (a76), which are mediated by the relator by (a80). Thus, we infer (t33). 10

Since a relator is a particular type of moment, it has to have a unique bearer, we define the bearer of the relator as the mereological sum of the individuals that the relator mediates. Moreover, a relator type is a type that applies to relators. For instance, marriage is a relator type of which the marriage between John and Mary is an instance. Relator types are defined according to schema (a44).

## 3.11. Characterization

Guizzardi (2005) states that a type is characterized by moment types that inhere in its instances.

```
a81 characterization (t, m) → EndurantType (t) ∧ MomentType (m) ∧ ∀ x.(x :: t →∃ y.(y :: m ∧ inheresIn (y, x))) ∧∀ z.(z :: m →∃! w.(w :: t ∧ inheresIn (z, w))) In particular, for quality kinds, we have that: a82 characterization (t, q) ∧ QualityType (q) → ( ∀ x :: q →∃! y :: t ∧ inheresIn (x, y))
```

## 3.12. Qualities and quality structures

In the following axioms, we use the standard notation from set-theory and arithmetic, i.e., membership ∈ , set inclusion ⊆ , proper set inclusion ⊂ , Cartesian product × , the empty set ∅ , addition + , the greater or equal relation ⩾ , and the natural number zero 0, by appealing to their intuitive meaning. However, we will not commit to a specific theory. 11

UFO grounds quality structures in its taxonomy of abstract individuals, which in classified into sets and quales (a83)-(a85).

```
a83 Quale (x) → AbstractIndividual (x) a84 Set (x) → AbstractIndividual (x) a85 ¬∃ x( Quale (x) ∧ Set (x))
```

10 Our theorem (t33) corresponds to axiom (6.45) in Guizzardi's book (Guizzardi, 2005, §6.45). It is now a theorem, since we introduced a stronger definition of relators.

11 A suitable set theory should be enough for expressing these notions. For instance, New Foundations with Urelements (NFU) + Infinity + Choice can represent first-order Peano arithmetic (PA) and Cartesian product. One problem here is that theories of arithmetic, like Robinson arithmetic (Q) and PA, have no finite models.

A quality structure is defined as an entity associated with a unique quality type (d5). Moreover, quality structures are non-empty sets (a86). The members of quality structures are quale s, where an entity is a quale iff it is a member of a unique quality structure (a87). A quality structure is partitioned into quality dimension and quality domain (a88), (a89). Finally, given two quality types such that one properly specializes the other, the sub-quality-type imposes constraints on the quality structure associated with the super-quality-type. Since quality structures are sets, the quality structure associated with the subquality-type must be a proper subset of the quality structure associated with the super-quality-type. For instance, given that Color is associated with ColorSpace , then SkinColor (a subkind of Color ) is associated with a proper subset of ColorSpace . More formally, for any quality structures s and s ′ and quality types t and t ′ such that s is associated with t , s ′ is associated with t ′ , and t ′ is a proper specialization of t , then s ′ is a proper subset of s (a90).

<!-- formula-not-decoded -->

```
d5 QualityStructure (x) =∃! t ( QualityType (t) ∧ associatedWith (x, t)) (6.26) a86 QualityStructure (x) → Set (x) ∧ x ̸= ∅ (6.27) a87 Quale (x) ↔∃! y( QualityStructure (y) ∧ x ∈ y) (6.40) a88 QualityStructure (x) ↔ QualityDomain (x) ∨ QualityDimension (x) (6.23) a89 QualityDomain (x) →¬ QualityDimension (x) a90 associatedWith (s, t) ∧ associatedWith (s ′ , t ′ ) ∧ t ′ ⊏ t → s ′ ⊂ s
```

An intrinsic moment type is a quality type iff it is associated with a unique quality structure (a91). A quality is defined as an entity that instantiates a unique quality kind (d6).

```
a91 QualityType (t) ↔ IntrinsicMomentType (t) ∧∃! x( QualityStructure (x) ∧ associatedWith (x, t)) (6.24)
```

<!-- formula-not-decoded -->

The hasValue relation holds from qualities to quales (a92), where hasValue is functional (a93). From (d6), we have that a quality instantiates a unique quality kind , which from (a91) is associated to at least one quality structure. The axiom (a94) enforces each quale of a quality to be member of such quality structure s.

<!-- formula-not-decoded -->

UFO-A also defines what is for a quality (type) to be simple or complex . A simple quality is a quality that bears nothing (d7). A complex quality is a quality but not a simple quality (d8). A simple quality type is a quality type that have only simple qualities as instances (d9). Similarly, a complex quality type is a quality type that have only complex qualities as instances (d10). Moreover, quality dimensions can only be associatedWith simple quality types, and vice versa (a95), while quality domains can only be associatedWith complex quality types, and vice versa (a96).

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

Since the qualities of a complex quality x :: X correspond to the quality dimensions of the quality domain associated with X , then no two distinct qualities inhering a complex quality can be of the same type (a97). Moreover, since quality dimensions are unidimensional, and quality domains can only be defined by quality dimensions, then complex qualities can only bear simple qualities (a98).

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

Concerning quality domains, each quality domain d associatedWith a complex quality type t can be defined in terms of the Cartesian product of the quality dimensions associatedWith the quality types characterizing t (a99).

<!-- formula-not-decoded -->

A metric space s is obtained from a quality domain s by associating a distance function d (called the metric of s ) such that for every two quality values x , y in s , d(x, y) represents the distance between x and y in s (see Guizzardi, 2005, §6.11). Here, we define d as a left-total functional ternary relation d(x, y, r) such that r is the distance between the quales x and y , see (a100), (a101).

```
a100 d(x, y, r) → ( Quale (x) ∧ Quale (y) ∧∃ z( memberOf (x, z) ∧ memberOf (y, z))) a101 ( Quale (x) ∧ Quale (y)) →∃! r(d(x, y, r))
```

Moreover, the distance relation d must also obey the following constraints:

```
a) x = y ∧ d(x, y, r) → (r = 0 ) ; b) d(x, y, r) → d(y, x, r) ; c) d(x, y, r 0 ) ∧ d(y, z, r 1 ) ∧ d(x, z, r 2 ) ∧+ (r 0 , r 1 , s) → s ⩾ r 2 (triangle inequality) 12
```

The notion of region is also informally defined by Guizzardi (2005, §6.2.6). A region is a kind of division of a quality structure with respect to a specific quale and according to the structure of the quality structure. Definition 6.12 (see quality region, Guizzardi, 2005, p.228) states that a quality region is a convex region c of a quality domain; while c is convex iff for all two points x , y in c , all points between x and y are also in c . We think that a suitable set theory would be able to represent the required topological notions.

## 3.13. Endurants and perdurants

Any endurant is connected to a perdurant by the manifestation relation (a102). The life of an endurant is then specified by a functional relation that associates the endurant with the mereological sum of all the events that manifest it (a103). The life of an endurant is unique due to the unicity of mereological sums. Moreover, the case where two perdurants are consecutive in time is here abstractly modeled by means of the meet relation (a104). We refer to Guizzardi et al. (2016) for the detailed presentation of this approach, and to Benevides et al. (2019b) for a complete formalization of the UFO-B ontology.

12 + (r 0 , r 1 , s) denotes the relationship that holds when the arithmetic equation s = r 0 + r 1 is true.

```
a102 manifests (x, y) → Endurant (x) ∧ Perdurant (y) a103 lifeOf (x, y) ↔ Perdurant (x) ∧ Endurant (y) ∧∀ z ( O (z, x) ↔ Perdurant (z) ∧ manifests (z, y)) a104 meet (x, y) → Perdurant (x) ∧ Perdurant (y)
```

So, there is a special perdurant (which we may call a process, in a very particular sense) that is the life of an endurant, i.e., the sum of everything that is a manifestation of the dispositions inhering in) that perdurant (Guizzardi et al., 2016). As previously discussed, perdurants have all their parts and constituents necessarily. So, every single manifestation of that endurant literally changes its life (a change of life, not a change in the life!). In other words, this particular perdurant represents the current life of an endurant at each point in time (Guizzardi et al., 2016).

## 4. Analysis and formalization in UFO: Examples

This section presents an analysis and formalization of various cases that originate from the First FOUST Workshop - the Foundational Stance, an international forum dedicated to Foundational Ontology research. They cover a number of topics (composition/constitution, roles, property change, event change, and conceptual evolution) and are also addressed by other papers in this special issue to facilitate the comparison of the various approaches. Each of the following sub-sections begins with a quote of the text supplied as the case description, which is followed by our analysis. We employ OntoUML diagrams and provide some formalization to accompany them.

## 4.1. Composition/constitution

- 1) 'There is a four-legged table made of wood. Some time later, a leg of the table is replaced. Even later, the table is demolished so it ceases to exist although the wood is still there after the demolition. '

Figure 2 depicts an OntoUML model 13 representing this situation. In this model, a Wood Portion is a quantity (in the technical sense discussed by Guizzardi (2005), i.e., a maximally topologically selfconnected portion of matter). It is contingent for a Wood Portion to constitute a Wooden Table Component . In this model, Wooden Table Component s are artifacts that are manufactured to necessarily serve the role of Wooden Table Component (i.e., Wooden Table Component is a nominal kind/artifact kind). Two particular subkinds considered are a Table Leg Component (e.g., that has necessarily a shape and necessarily a certain structure capable of supporting a certain weight range, etc.) and a Table Top Component . A Wooden Table is structured in a number of functional roles associated via componentOf relations, i.e., parthood relations in which the parts play a functional role with respect to the whole (see Guizzardi, 2005), that can contingently be played by Wooden Table Component s. Since the relation between the table and its parts is one of generic dependence , parts can be replaced without any impact on the identity of the table. Moreover, since the relation between a Wood Portion and each Wooden Table Component (that it contingently constitutes) is one of constitution and not one of identity, the lifecycles of the former and the latter are completely independent. Therefore, a Wood Portion can survive the destruction of these wood components and the destruction of the table as a functional complex. Finally, as represented by the black diamond in the figure (exclusive parthood), each Table Leg Component can only be part of one single Wooden Table at a certain point in time.

13 In OntoUML, the stereotypes «kind» and «quantity» stand for ObjectKind and QuantityKind, respectively.

Fig. 2. The wooden table case in OntoUML.

[FIGURE]

In the sequel, we show a partial formalization of this case.

QuantityKind ( WoodPortion )

Being a Wooden Component Constituent is a role played by a Wood Portion in the scope of a (contingent) constitution relation with a Wooden Table Component :

Role ( WoodenComponentConstituent ) WoodenComponentConstituent ⊑ WoodPortion ∀ :: →∃! :: ∧

x.(x WoodenComponentConstituent y.(y WoodenTableComponent constitutedBy (y, x)))

This constitution relation is also contingent from the point of view of the Wooden Table Component , i.e., the Wooden Table Component can be constituted by different Wood Portion s in different situations (worlds): 14

14 One should notice that these formulae here are a special case of (a58) in which there is a single constituent involved. In other words, a case of what is called wholly constituting . Moreover, since WoodenTableComponent is a kind, its instances are always generically dependent on WoodenComponentConstituent . In contrast, since WoodenComponentConstituent is a role, WoodPortion is only dependent on WoodenTableComponent insofar as it instantiates the WoodenComponentConstituent role.

```
∀ x.(x :: WoodenTableComponent →∃! y.(y :: WoodenComponentConstituent ∧ constitutedBy (x, y))) ObjectKind ( WoodenTable ) ObjectKind ( WoodenTableComponent ) SubKind ( TableLegComponent ) SubKind ( TableTopComponent ) TableTopComponent ⊑ WoodenTableComponent TableLegComponent ⊑ WoodenTableComponent
```

To allow the representation of Table Leg Component and Table Top Component as disjoint types, we introduce (a105):

```
a105 isDisjointWith (t, t ′ ) ↔ Type (t) ∧ Type (t ′ ) ∧¬∃ x(x :: t 1 ∧ x :: t 2 ) isDisjointWith ( TableLegComponent , TableTopComponent )
```

Right Rear Leg , Right Front Leg , Left Front Leg , Left Rear Leg and Top Component are roles played by a Table Leg Component (the first four) and Table Top Component (the latter) in the scope of a component of relation with a Table :

```
Role ( RightRearLeg ) Role ( RightFrontLeg ) Role ( LeftRearLeg ) Role ( LeftFrontLeg ) Role ( TopComponent ) RightRearLeg ⊑ TableLegComponent RightFrontLeg ⊑ TableLegComponent LeftRearLeg ⊑ TableLegComponent LeftFrontLeg ⊑ TableLegComponent TopComponent ⊑ TableTopComponent
```

For example, Right Front Leg is a role played by a Table Leg Component when being a functional part of a Wooden Table . Guizzardi (2005) defines the relation of component of between a functional part and a functional complex, and it conflates a mereological relation plus a relation of functional dependence. Here, in order for a Table Component to function as a Table Component , it must be part of a Table functioning as a Table ( Mutatis mutandis , the same for the roles of Right Rear Leg , Left Front Leg , Left Rear Leg and Top Component ):

```
∀ x.(x :: RightFrontLeg →∃! y.(y :: WoodenTable ∧ componentOf (x, RightFrontLeg , y, WoodenTable ))
```

In the converse direction, in order for a Wooden Table to function as such it must be composed of four distinct Table Leg Component s and a Top Component (which here are all assumed to be Wooden Table Component s), each of these functioning in a particular role:

```
∀ x.(x :: WoodenTable →∃ y 1 , y 2 , y 3 , y 4 , y 5 .(y 1 :: RightRearLeg ∧ y 2 :: RightFrontLeg ∧ y 3 :: LeftFrontLeg ∧ y 4 :: LeftRearLeg ∧ y 5 :: TopComponent ∧ componentOf (y 1 , RightRearLeg , x, WoodenTable ) ∧ componentOf (y 2 , RightFrontLeg , x, WoodenTable ) ∧ componentOf (y 3 , LeftFrontLeg , x, WoodenTable ) ∧ componentOf (y 4 , LeftRearLeg , x, WoodenTable ) ∧ componentOf (y 5 , TopComponent , x, WoodenTable ) ∧ (y 1 ̸= y 2 ) ∧ (y 1 ̸= y 3 ) ∧ (y 1 ̸= y 4 ) ∧ (y 2 ̸= y 3 ) ∧ (y 2 ̸= y 4 ) ∧ (y 3 ̸= y 4 ))
```

The relation of component of is a relation of generic dependence from the whole to the part and from the part to the whole. So, not only the Wooden Table can have different Wooden Table Component s playing these functional part roles in different situations, but these components can play these roles in different tables in different situations.

From an OntoUML model and using its supporting tools, we can automatically generate models that satisfy the logical theory corresponding to the OntoUML model (Benevides et al., 2010). In conceptual modeling terms, this means that we can generate instances that are admissible by an OntoUML model. In the sequel, we show a number of examples (Figs 3 to 5) of these visual models automatically generated for the OntoUML diagram of Fig. 2.

Fig. 3. A Wood Portion exists in world w 1 without constituting any object ( Object0 :: WoodPortion ) and in w 2 it goes on to constitute a Wooden Table Component , namely, a Table Top Component ( Object1 :: WoodenTableComponent , Object1 :: TableTopComponent ).

[FIGURE]

Fig. 4. A Table Leg Component ( Object3 :: TableLegComponent , Object3 :: WoodenTableComponent ) exists in w 1 being constituted by a Wood Portion ( Object7 :: WoodPortion ) and, in w 2, it still exists but now constituted by a different Wood Portion ( Object4 :: WoodPortion ).

[FIGURE]

Fig. 5. A Wooden Table ( Object10 :: WoodenTable ) exists in world w 1 being composed by a Table Leg Component that plays in it a functional role of Right Rear Leg ( Object5 :: WoodenTableComponent , Object5 :: TableLegComponent , Object5 :: RightRearLeg , componentOf ( Object5 , RightRearLeg , Object10 , WoodenTable ) ) and which, in that world, is constituted by a particular Wood Portion ( Object1 :: WoodPortion , Object1 :: WoodenComponentConstituent , constitutedBy ( Object5 , Object1 ) ). In a different world w 2, the table still exists but now having that same Table Leg Component Object5 playing a different role, namely, that of a Left Front Leg ( Object5 :: LeftFrontLeg , componentOf ( Object5 , LeftFrontLeg , Object10 , WoodenTable ) ). In that world, this Table Leg Component is also constituted by a different Wood Portion ( constitutedBy ( Object5 , Object0 )).

[FIGURE]

## 4.2. Roles

- 2) 'Mr. Potter is the teacher of class 2C at Shapism School and resigns at the beginning of the spring break. After the spring break, Mrs. Bumblebee replaces Mr. Potter as the teacher of 2C. Also, student Mary left the class at the beginning of the break and a new student, John, joins in when the break ends. '

In this example, captured in the OntoUML of Fig. 6, Teacher is a role played by a person when mediated by an Employment relator (Guarino and Guizzardi, 2015) connecting her to a School . Analogously, Student is a role played by a Person when connected via a School Enrollment relator to a School . A School makes Course Offering s (a relator) to a given Class (a collective forming the target community to which that course is addressed). Students can enroll to a Course Offering via a Course Enrollment relator, connecting the former to a particular enrollment of a Student in that School . In other words, the enrollment of a Student to a Course Offering existentially depends both on the offering and on a particular School Enrollment of that Student . Notice that the relation from Course Enrollment to Course Offering is one of existential dependence ( mediation , Guizzardi, 2005; Guarino and Guizzardi, 2015) and, hence, immutable. However, the relation from Course Offering to Course Enrollment is an optional relation of generic dependence and, thus, contingent, mutable. For this reason, the set of students actually enrolled in a given Course Offering can change from situation to situation. Analogously, a Teacher is assigned to a Course Offering by having a Course Teacher Assignment relator that connects a Course Offering to an Employment of a Teacher . In other words, a teacher's assignment to a course offering existentially depends on both on the Course Offering and on the Employment of a Teacher in that School . Again, since the relation from Course Offering to Teacher Assignment is one of generic dependence, different teachers can be assigned to a course offering in different points in time.

Fig. 6. The school case in OntoUML.

[FIGURE]

In the sequel, we show a partial formalization of this case.

```
ObjectKind ( School ) ObjectKind ( Course ) ObjectKind ( Person ) CollectiveKind ( Class )
```

Teacher is a role (contingently) played by a Person in the scope of an Employment relation to a School .

```
Role ( Teacher )
```

```
Teacher ⊑ Person RelatorKind ( Employment ) ∀ x(x :: Teacher →∃ y(y :: Employment ∧ mediates (y, x)) ∀ x(x :: Employment →∃! y, ! z(y :: Teacher ∧ z :: School ∧ mediates (x, y) ∧ mediates
```

(x, z)))

Student is a role (contingently) played by a Person in the scope of an Enrollment relation to a School .

```
x(x y(y mediates (y, x))
```

```
Role ( Student ) Student ⊑ Person RelatorKind ( SchoolEnrollment ) ∀ :: Student →∃ :: SchoolEnrollment ∧
```

```
∀ x(x :: SchoolEnrollment →∃! y, ! z(y :: Student ∧ z :: School ∧ mediates (x, y) ∧ mediates (x, z)))
```

A School can make several Course Offering s to Class es. Student s can be members of Class es. A Class must have at least two Student s as members. Notice that a Course Offering in this model is a particular instantiation of the UFO-S Service Offering pattern (Nardi et al., 2015), having the Class here as the Target Community .

```
RelatorKind ( CourseOffering ) ∀ x(x :: CourseOffering →∃! y, ! z, w(y :: School ∧ z :: Course ∧ w :: Class ∧ mediates (x, y) ∧ mediates (x, z) ∧ mediates (x, w))) ∀ x(x :: Student →∃ y(y :: Class ∧ memberOf (x, y)) ∀ x(x :: Class → ∃ y, z(y :: Student ∧ z :: Student ∧ (y ̸= z) ∧ memberOf (y, x) ∧ memberOf (z, x)))
```

Student s that are enrolled in a School can enroll in Course Offering s of that School . Notice that a Course Enrollment here is an instantiation of the UFO-S pattern of Service Agreement s (Nardi et al., 2015). 15

```
RelatorKind ( CourseEnrollment ) ∀ x(x :: CourseEnrollment →∃! y, ! z(y :: SchoolEnrollment ∧ z CourseOffering mediates (x, y) mediates (x, z)))
```

```
:: ∧ ∧
```

Teacher s can be assigned to Course Offering s. There is exactly one Teacher assigned to a Course Offering in a given situation. However, since the relation between Course Offering and Course Teacher Assignment is one of generic dependence, different Teacher s can be assigned to the same Course Offering in different situations. 16

```
RelatorKind ( CourseTeacherAssignment ) ∀ x(x :: CourseTeacherAssignment →∃! y, ! z(y :: Employment ∧ z :: CourseOffering ∧ mediates (x, y) ∧ mediates (x, z))) ∀ x, y, z(x :: CourseOffering ∧ y :: CourseTeacherAssignment ∧ z :: CourseTeacherAssignment ∧ mediates (y, x) ∧ mediates (z, x) → (y = z))
```

Figure 7 shows visual models automatically generated for the OntoUML diagram of Fig. 6 illustrating the dynamics of change in this domain.

## 4.3. Property change

3.a) 'A flower is red in the summer. As time passes, the color changes. In autumn the flower is brown. '

15 The complete specification of this case includes a constraint that guarantees that a Student can only enroll in Course Offering s of the School s in which he has a School Enrollment . This constraint is automatically detected and included in the specification by the anti-pattern detection and rectification support of the OntoUML tool (Guerson et al., 2015). We omit it here, nonetheless, for the sake of brevity.

16 The complete specification of this case includes a constraint that guarantees that a Teacher can only be assigned to Course Offering s of the School s in which she has an Employment relationship. Once more, this constraint is automatically detected and included in the specification by the anti-pattern detection and rectification support of the OntoUML tool. Once more, we omit it here, nonetheless, for the sake of brevity.

[FIGURE]

Fig. 7. In world w 1, we have a School Object0 ( Object0 :: School ) and a student Object3 ( Object3 :: Student ) enrolled in that School (by Property 3 ( Property 3 :: SchoolEnrollment )) and who is part of Class Object4 ( Object4 :: Class ). Moreover, we have a Teacher Object1 ( Object1 :: Teacher ) that works for that School (by Employment Property 0 ( Property 0 :: Employment )). There is also a Course Offering ( Property 2 :: CourseOffering ) of Course Object5 ( Object5 :: Course , e.g., CS 101 ) made by that School to Class Object4 . Finally, Student Object3 enrolls in Course Offering Property 2 (by Course Enrollment Property 6 ( Property 6 :: CourseEnrollment )) and Teacher Object1 is assigned to teach that Course Offering (by Course Teacher Assignment Property 1 ( Property 1 :: CourseTeacherAssignment )). In world w 2, a different Teacher Object2 ( Object2 :: School ), who is also employed in that same school (by Employment Property 4 ( Property 4 :: Employment )), is now assigned to that Course Offering Property 2 .

Fig. 8. The flower case in OntoUML.

[FIGURE]

In Fig. 8, we present an OntoUML model 17 representing this situation. In this model, a Rose is modeled as a subkind of Flower . All flowers are bearers of a Color quality. 18 As for any quality, a Flower Color 19 quality inheres in its bearer (the characterization relation). A perceivable quality takes its value in a color domain (here modeled as a simple ordinal space of colors).

17 In OntoUML, the simplest way to represent quality structures is as datatypes (Guizzardi, 2005). Classes stereotyped as «enumeration»are particular types of datatypes. For a more sophisticated representation of these structures in the language, one should refer to Albuquerque and Guizzardi (2013). We take here the simplest approach.

18 To be precise, Color is a particular type of quality termed as Perceivable Quality by Albuquerque and Guizzardi (2013). We omit this discussion here.

19 Flower Color is a genuine subtype of Color given that it is associated with a particular subspace of possible values, which is a proper part of the entire color spindle.

In the sequel, we show a partial formalization of this case.

```
ObjectKind ( Flower ) SubKind ( Rose ) Rose ⊑ Flower SubKind ( Color ) SubKind ( FlowerColor ) FlowerColor ⊑ Color QualityStructure ( FlowerColorValues ) Now, the quality type Flower Color characterizes the object type Flower : characterization ( Flower , FlowerColor ) Following (a81) and (a82), this implies: ∀ x.(x :: Flower →∃! y.(y :: FlowerColor ∧ inheresIn (y, x))) ∀ z.(z :: FlowerColor →∃! w.(w :: Flower ∧ inheresIn (z, w))) Since Flower Color is a Quality Type , it is associated with a Quality Structure (a91): associatedWith ( FlowerColor , FlowerColorValues ) As Quality Structure s are non-empty sets of possible values that qualities can take (a86): Red ∈ FlowerColorValues ∧ Yellow ∈ FlowerColorValues ∧ Brown ∈ FlowerColorValues ∧ White ∈ FlowerColorValues
```

Given (a93) and (a94), each quality instance of Flower Color takes, in a given situation, a value in the Flower Color Value s space:

```
∀ x.(x :: FlowerColor →∃! y.(y ∈ FlowerColorValues ∧ hasValue (x, y)))
```

Now, notice that inherence is an existential dependence relation and, hence, the connection between a particular quality and its bearer is immutable. However, the relation of hasValue between a quality and its value (qualia) in a quality structure is one of generic dependence. Therefore, the value of a given Flower Color can change from situation to situation. In the sequel, we show examples (Fig. 9) of the visual models automatically generated for the OntoUML diagram of Fig. 8.

3.b) 'A man is walking when suddenly he starts walking faster and then breaks into a run. '

In Fig. 10, we present an OntoUML model representing this case. In UFO, we follow a classical view of events in which events are modally fragile entities. So, events cannot bear modal properties, they cannot genuinely change, and they cannot be different from what they are (Guizzardi et al., 2016). Events are also polygenic manifestations of (possibly bundles of) dispositions (Guizzardi et al., 2013a). These (bundles of) dispositions are said to be the focuses of these events, so that events are carved out of scenes by having those underlying endurants as their focus (Guarino and Guizzardi, 2016). For example, the marriage of John and Mary as a perdurant is the manifestation of the marriage (as a relator) that binds John and Mary, i.e., the sum of all manifestations of the moments inhering in John-qua-Husbandof-Mary and Mary-qua-Wife-of-John (Guizzardi et al., 2016, 2013a). Following up on this example, there are two kinds of 'changes' referring to 'John and Mary's marriage': (1) a change in the marriage relator - for example, when we say that the marriage between John and Mary (as a whole) changed from passionate in situation s 1 to cold and distant in situation s 2, we are referring to this endurant (a bundle of moments), which can qualitatively change while remaining numerically the same; (2) a change of (or, more precisely, a variation of) temporal parts of a perdurant that are qualitatively different. Figure 10 illustrates a case of the latter; Fig. 12 illustrates a case of the former.

Fig. 9. In world w 1, we have two roses Object0 ( Object0 :: Rose , Object0 :: Flower ) and Object1 ( Object1 :: Rose , Object1 :: Flower ). These roses bear each a Flower Color quality ( Property 0 :: FlowerColor , inheresIn ( Property 0 , Object1 ) , Property 2 :: FlowerColor , inheresIn ( Property 2 , Object0 ) . In that situation, qualities Property 0 and Property 2 have the color values Red and Brown , respectively. In world w 2, Rose Object1 turns from Red to Brown (by having its quality Property 0 assuming the new value), and Rose Object0 turns from Brown to White (again, by having its quality Property 2 taking the new value).

[FIGURE]

Fig. 10. The changing speed case in OntoUML.

[FIGURE]

In the sequel, we show a partial formalization of this case.

```
ObjectKind ( Person )
```

Jogger is a role played by a Person when bearing a Jog mode (an endurant comprising an intention as well as the capacities of the person as a Jogger ).

```
Role ( Jogger ) Jogger ⊑ Person ModeKind ( Jog ) characterization ( Jogger , Jog ) ∀ x.(x :: Jog →∃! y.(y :: JoggingTrack ∧ externallyDependent (x, y)))
```

As explained in details by Guizzardi et al. (2016), associated to a Jog (an endurant), we have Jogging perdurants that are manifestations of that endurant. In particular, we have Jogging Event s, which are direct manifestations of the dispositions constituting a Jog , and Jogging Process es, which are constituted by Jogging Event s.

```
EventType ( JoggingProcess ) EventType ( JoggingEvent ) ∀ x.(x :: JoggingEvent →∃! y.(y :: Jog ∧ □ ( ex (x) → manifestedBy (y, x))))
```

At each situation, we have a particular type of maximal Jogging Process (termed the life of a Jog ) that is constituted by (exactly) the sum of Jogging Event s that are manifestations of that Jog . Moreover, since perdurants have all their parts, properties and constituents necessarily, every time a new Jogging Event takes place, there is a new Jogging Process that arises as a cumulative aggregation of manifestations of that Jog , i.e., a new life of that Jog .

```
∀ x.(x :: Jog →∃! y.(y :: JoggingProcess ∧ lifeOf (y, x)) ∀ x.(x :: JoggingProcess →∃ y.(y :: JoggingEvent ∧ constitutedBy (x, y)) ∀ x, y.(x :: Jog ∧ y :: JoggingProcess ∧ lifeOf (y, x) →∀ z.(z :: JoggingEvent → ( constitutedBy (y, z) ↔ manifestedBy (x, z))))
```

Since perdurants unfold in time accumulating parts, if we have two Jogging Process es that are manifestations of the same Jog and that immediately follow each other, meeting in the Allen sense (Guizzardi et al., 2013a), then we have that all constituents of the preceding process also constitute the succeeding process. 20

20 We use the term process here in this very specific sense to denote the current life of an endurant constituted by all and exactly the manifestations of (the dispositions inhering in) that endurant (see Section 3.13) (Guizzardi et al., 2016). These formulae here capture the continuous changes of life of an endurant as dispositions continue to manifest. Each current life of an endurant is monotonically constituted by all constituents of its immediate preceding life.

```
∀ x, y, z.(x :: Jog ∧ y :: JoggingProcess ∧ z :: JoggingProcess ∧ manifestedBy (x, y) ∧ manifestedBy (x, z) ∧ meet (y, z) →∀ w.(w :: JoggingEvent ∧ constitutedBy (y, w) → constitutedBy (z, w)))
```

Jogging Event s can be stative/homeomerous and some are dynamic/sequences of changes. In the former's case, we have Jog State , while in the latter we have Jogging Locomotion . Moreover, Jogging Locomotion s can be such that they have the quality of being a Walk While Jogging event (an event characterized by a 'walking' moving speed), or they can be such that they have the quality of being a Run While Jogging (an event characterized by a 'running' moving speed). Since events are immutable, they are characterized by tropes, in the classical sense, not qualities as variable tropes (Guarino and Guizzardi, 2015, 2016). Unlike qualities, tropes cannot change their values.

```
EventType ( JogState ) EventType ( JoggingLocomotion ) EventType ( WalkWhileJogging ) EventType ( RunWhileJogging ) ∀ x.(x :: JoggingLocomotion →∃! y.(y ∈ JoggingSpeedValues ∧ □ hasValue (x, y)))
```

In the specialization of Jogging Event into Jogging Locomotion and Jog State , and the specialization Jogging Locomotion into Walk While Jogging and Run While Jogging , partition the instances of the specialized types, which can be represented with support of (a105)-(a107).

```
a106 isCompletelyCoveredBy (t, t ′ , t ′′ ) ↔∀ x(x :: t → x :: t ′ ∨ x :: t ′′ ) a107 isPartitionedInto (t, t ′ , t ′′ ) ↔ isCompletelyCoveredBy (t, t ′ , t ′′ ) ∧ isDisjointWith (t ′ , t ′′ ) isPartitionedInto ( JoggingEvent , JogState , JoggingLocomotion ) isPartitionedInto ( JoggingLocomotion , WalkWhileJogging , RunWhileJogging )
```

Figure 11 depicts instances automatically generated for the OntoUML diagram of Fig. 10.

## 4.4. Event change

## 4) 'A man is walking to the station, but before he gets there, he turns around and goes home. '

As discussed in the previous sections, in UFO, we take the classical approach towards events, thus, treating them as modally fragile entities. For this reason, events cannot genuinely change, i.e., they cannot qualitatively change as a whole while maintaining their numerical identity. Alleged events change are either: (a) event variation - different temporal parts of the event in question have different properties as a whole. An example of this is exercised in the previous section; (b) the subject of change is the focus of the event, i.e., the underlying endurant of which the event is a manifestation. The case addressed in this section is not really a case of the former but one of the latter. To put it baldly, what genuinely changes is this case is the complex mode (including an intentional component) inhering in the Walker. Due to a change in the intention of the walker, a different walking perdurant will be manifested. In other words, what genuinely changes is a property of Walk (the complex mode). These changes make that Walk be manifested as a (numerically) different walking perdurant. Given that the focus of change here is the endurant, we will refrain from representing the perdurant part of this example, which would otherwise follow the design pattern proposed by Guizzardi et al. (2016) and instantiated in the previous section.

Fig. 11. From world w 1 to w 3, we have a jogger Object2 ( Object2 :: Jogger ) who is an increasing speed jog ( Property :: Jog , inheresIn ( Property , Object2 ) ). In w 1, the jog is manifested by a walking speed jog Object5 ( Object5 :: WalkingWhileJogging ), which is then manifested by a fast walking Object4 ( Object4 :: WalkingWhileJogging ) in w 2, and finally, breaks into a run Object3 ( Object3 :: RunningWhileJogging ) in w 3. These events meet as they succeed one another being constituents of the same jogging process Object1 ( Object1 :: JoggingProcess , meet ( Object5 , Object4 ) , meet ( Object4 , Object3 ) , constitutedBy ( Object1 , Object5 ) , constitutedBy ( Object1 , Object4 ) , constitutedBy ( Object1 , Object3 ) ).

[FIGURE]

Fig. 12. The redirected walk case in OntoUML.

[FIGURE]

In Fig. 12, we present an OntoUML model representing this situation. 21 In this model, a Walk is modeled as an externally dependent mode that inheres in the Walker and that is externally dependent on Place (that plays the role of an originally intended destination).

```
ObjectKind ( Person ) Role ( Walker ) Walker ⊑ Person ModeKind ( Walk ) characterization ( Walk , Walker ) ∀ x.(x :: Walk →∃! y.(y :: OriginallyIntendedDestination ∧ externalDependence (x, y)))
```

A (originally intended) destination is a role played by a Place when involved in a relationship with a Walk (i.e., when it is the target of an intention present in a Walk ).

```
ObjectKind ( Place ) Role ( Destination ) Role ( OriginallyIntendedDestination ) Destination ⊑ Place
```

21 It would, of course, be trivial to model the class Man here as a subkind of Person and as a supertype of Walker . We omit it, however, for the sake of simplicity and given that it does not have any impact on the focus of the analysis conducted here.

```
OriginallyIntendedDestination ⊑ Destination ∀ x.(x :: OriginallyIntendedDestination →∃ y.(y :: Walk ∧ externalDependence (y, x)))
```

As previously discussed, a Walk here is an endurant that is the focus of a walking perdurant, in the technical sense discussed by Guarino and Guizzardi (2016). In this sense, the Walk aggregates both the intention of the walker and his capabilities qua-walker. As such, i.e., as an endurant, the Walk can change in time undergoing the phases of Ongoing Walk and Finalized Walk (Guarino and Guizzardi, 2016).

```
isPartitionedInto ( Walk , OngoingWalk , FinalizedWalk ) ∀ x.(x :: FinalizedWalk →∃! y.(y :: Destination ∧ arrivedAt (x, y) 22 ))
```

A Finalized Walk is only contingently a Successful Walk (i.e., a walk that arrives at the originally intended destination) as well as it can be contingently (i.e., in a counterfactual situation) a Redirected Walk .

```
isPartitionedInto ( FinalizedWalk , SucessfulWalk , RedirectedWalk ) ∀ x.(x :: SuccessfulWalk ↔ (x :: FinalizedWalk ∧ ∀ y, z.((y :: OriginallyIntendedDestination ∧ externallyDependent (x, y) ∧ z :: Destination ∧ arrivedAt (x, z)) → (y = z)))) 23
```

In the case of a Redirected Walk , there is a new intention, which is aggregated to the original walk and which is directed (again, externally dependent on) a new destination. Associated to the Walk (i.e., the endurant), there are many possible unfoldings (in different histories of the world) representing how the dispositions aggregated in the walk mode are manifested by different walking perdurants (Guizzardi et al., 2016).

```
Role ( RedirectedDestination ) RedirectedDestination ⊑ Destination ModeKind ( RedirectedDestinationIntention ) ∀ x.(x :: RedirectedDestinationIntention →∃! y.(y :: RedirectedWalk ∧ inheresIn (x, y))) ∀ x.(x :: RedirectedWalk →∃! y.(y :: RedirectedDestinationIntention ∧ inheresIn (y, x))) ∀ x.(x :: RedirectedDestinationIntention →∃! y.(y :: RedirectedDestination ∧ externallyDependent (x, y))) ∀ x.(x :: RedirectedDestination →∃ y.(y :: RedirectedDestinationIntention ∧ externallyDependent (x, y))
```

22 The relation of 'arrived at' is a material relation, which is a derived from the following rule: a walk x , qua-endurant, is related via this relation to a place y iff y is the location of the Walker in the post-situation immediately brought about by the occurrence of the walking process that is the manifestation of x (Guizzardi et al., 2016).

23 A successful walk must 'arrive at' a place that is identical to the originally intended destination. This constraint is automatically generated by the OntoUML tool after an automated process of anti-pattern detection and rectification (Sales and Guizzardi, 2015).

[FIGURE]

Fig. 13. In this model, we have a Person Object1 that plays the role of a Walker by being the bearer of three distinct Walk modes ( Object1 :: Person , Object1 :: Walker , Property 0 :: Walk , Property 1 :: Walk , Property 2 :: Walk , inheresIn ( Property 0 , Object1 ) , inheresIn ( Property 1 , Object1 ) , inheresIn ( Property 3 , Object1 ) ). Property 1 is an ongoing walk that has Object0 as its originally intended destination ( Property 1 :: OngoingWalk , Object0 :: Place , Object0 :: Destination , externallyDependent ( Property 1 , Object0 ) , Object0 :: OriginallyIntendedDestination ); Property 0 is a finalized walk that also had Object1 as its originally dependent and also final destination ( externallyDependent ( Property 0 , Object0 ) , arrivedAt ( Property 0 , Object0 ) ); finally, Property 3 is a finalized walk that had Object0 as its originally dependent but it was redirected and arrived at a different destination ( externallyDependent ( Property 3 , Object0 ) , arrivedAt ( Property 3 , Object2 ) ).

```
∀ x.(x :: RedirectedWalk →∀ y, z.((y :: OriginallyIntendedDestination ∧ externallyDependent (x, y) ∧ z :: RedirectedDestination ∧ arrivedAt (x, z)) → (y ̸= z))) 24 ∀ x, y, z.((x :: RedirectedWalk ∧ y :: RedirectedDestinationIntention ∧ inheresIn (y, x) ∧ z :: RedirectedDestination ∧ externallyDependent (y, z)) → arrivedAt (x, z))
```

In the sequel, we show an example of visual model (Fig. 13) automatically generated for the OntoUML diagram of Fig. 12.

## 4.5. Concept evolution

- 5) 'A marriage is a contract that is regulated by civil and social constraints. These constraints can change but the meaning of marriage continues over time. '

In order to address matters of 'concept evolution,' it is key to understand what the subject of 'evolution' is, and what aspects of this subject remain stable. According to the 'marriage' concept evolution case, 'a marriage is a contract that is regulated by civil and social constraints', and 'these constraints can change but the meaning of marriage continues over time.' We observe that what remains stable here is a general kind of relator we call Conjugal Relationship between Spouse s, as represented in Figure 14. Varying constraints established in the social process in time lead to specific types of conjugal relationships, e.g., 'monogamous marriage,' 'polygamous marriage,' 'heterosexual marriage,' and 'same-sex marriage.' What is invariant across all foreseen types of conjugal relationships is that they specialize the more general Conjugal Relationship relator kind. However, the number and sex of spouses may vary according to the specific type of conjugal relationship.

24 A redirected walk must 'arrive at' a place that is different from the originally intended destination. Again, this constraint is automatically generated by the OntoUML tool after an automated process of anti-pattern detection and rectification.

Fig. 14. The concept evolution case in OntoUML.

[FIGURE]

UFO captures this scenario by accounting not only for the individuals in the domain of inquiry but types as well. This leads to higher-order types, i.e., types whose instances are themselves types 25 . The theory provides a formal characterization of the relations between higher-order types, first-order types, and individuals, along with a characterization of the so-called powertype pattern in the conceptual modeling literature). In this case, we have that specializations of the more general (and stable) notion of Conjugal Relationship are instances of a second-order type Conjugal Relationship Type . These instances establish more specific constraints that are not required in every Conjugal Relationship . The type Conjugal Relationship serves as the so-called base type in its relation with the higher-order type (Carvalho and Almeida, 2018). Identifying the second-order type allows us to specify invariants that apply to any first-order type instantiating the second-order type: First, all its instances specialize Conjugal Relationship (this is what remains the same or is said to continue over time). Further, by identifying the second-order type, we can impose conditions on the first-order types that instantiate it, such as, e.g., that any instance of Conjugal Relationship Type determines one or more specific Spouse Type s. For a Monogamous Heterosexual Marriage , for example, these are Husband and Wife . The formal relation between these higher-order types and their base types is captured with (a108), as defined by Carvalho and Almeida (2018) for MLT.

<!-- formula-not-decoded -->

In the sequel, we show a partial formalization of this case. We start with the structure that is invariant with respect to the possible types of conjugal relationships:

categorizes ( ConjugalRelationshipType , ConjugalRelationship )

25 We refer the reader to Carvalho et al. (2017) which shows the combination of UFO with the Multi-Level Theory (MLT). 26 In OntoUML, the «instantiation» stereotype represents both MLT relations of categorizes and powertypeOf , the later being outside the scope of this example.

```
RelatorKind ( ConjugalRelationship ) categorizes ( SpouseType , Spouse ) ObjectKind ( Person ) Role ( Spouse ) Spouse ⊏ Person ∀ x(x :: Spouse →∃ y(y :: ConjugalRelationship ∧ mediates (y, x)) ∀ x(x :: ConjugalRelationship →∃ y, z(y :: Spouse ∧ z :: Spouse ∧ y ̸= z ∧ mediates (x, y) ∧ mediates (x, z)))
```

We also need to ensure that Conjugal Relationship s (at the individual level) respect the invariants specified for Conjugal Relationship Type s and Spouse Type s. Thus, we add a constraint that all Conjugal Relationship s (instances of instances of Conjugal Relationship Type ) mediate relata that instantiate Spouse Type that are compatible with their specific Conjugal Relationship Type s: 27

```
∀ x, y((x :: y ∧ y :: ConjugalRelationshipType ) →∀ z( mediates (y, z) →∃ t (t :: SpouseType ∧ compatibleWith (t, y) ∧ z :: t)))
```

And then introduce two types of Conjugal Relationship s, in conformance with the formalization so far. First, we introduce Monogamous Heterosexual Marriage :

And, second,

```
MonogamousHeterosexualMarriage :: ConjugalRelationshipType SubKind ( MonogamousHeterosexualMarriage ) MonogamousHeterosexualMarriage ⊏ ConjugalRelationship Husband :: SpouseType Role ( Husband ) Husband ⊏ Spouse ∀ x(x :: Husband →∃! y(y :: MonogamousHeterosexualMarriage ∧ mediates (y, x)) Wife :: SpouseType Role ( Wife ) Wife ⊏ Spouse ∀ x(x :: Wife →∃! y(y :: MonogamousHeterosexualMarriage ∧ mediates (y, x)) ∀ x(x :: MonogamousHeterosexualMarriage →∃! y, ! z(y :: Husband ∧ z :: Wife ∧ mediates (x, y) ∧ mediates (x, z))) MonogamousSamesexMarriage : MonogamousSamesexMarriage :: ConjugalRelationshipType SubKind ( MonogamousSamesexMarriage ) MonogamousSamesexMarriage ⊏ ConjugalRelationship
```

27 This constraint spans more than two levels of classification and corresponds to what can be obtained with a 'regularity attribute' of types (Guizzardi et al., 2015a).

```
Partner :: SpouseType Role ( Partner ) Partner ⊏ Spouse ∀ x(x :: Partner →∃! y(y :: MonogamousSamesexMarriage ∧ mediates (y, x)) ∀ x(x :: MonogamousSamesexMarriage →∃! y, ! z(y :: Partner ∧ z :: Partner ∧ y ̸= z ∧ mediates (x, y) ∧ mediates (x, z) ∧ ((y :: Man ∧ z :: Man ) ∨ (y :: Woman ∧ z :: Woman ))))
```

In the sequence, we present a simulation of such a scenario where in the past world the only instance of Conjugal Relationship Type present is the Monogamic Heterosexual Marriage , which is also foreseen in the model. In the subsequent world another Conjugal Relationship Type is also present, one that has only one compatible Spouse Type (which can be interpreted as a sort of Partner type), and whose instances relate two instances of Spouse of the same sex. This simulation shows that Monogamic Samesex Marriage is also a possible instance for the model in Fig. 15.

We should observe that we are dealing here with a case of anticipated evolution (Bennett and Rajlich, 2000), i.e., when it is possible at specification time to foresee that types are likely to change and hence introduce invariant structures that can accommodate the envisioned space of change. Unanticipated evolution would effectively require changing the model, which could be obtained by application of model refactoring operations (Sunyé et al., 2001). For example, in the case of the 'marriage' scenario, if we had an initial model consisting of a 'marriage' relator between a 'man' and a 'woman,' we could rename it to 'heterosexual marriage', add 'same-sex marriage' and introduce 'conjugal relationship' as a super type of both of them along with declaring 'monogamous heterosexual marriage' and 'monogamous same-sex marriage' as instances of 'conjugal relationship type' (to foresee other possible changes).

Fig. 15. Simulation of evolving notion of Conjugal Relationship . In w 1, the only Conjugal Relationship Type present is the one whose instances include Monogamic Heterosexual Marriage , e.g., Property 0 ( Object5 :: ConjugalRelationshipType , Property 0 :: Monogamic HeterosexualMarriage , instantiation ( Property 0 , Object5 ). In a subsequent world, it is present a different instance of Conjugal Relationship Type -Object8 -whose instances include same sex conjugal relationships, such as Property 1 ( Object8 :: ConjugalRelationshipType , Property 1 :: ConjugalRelationship , instantiation ( Property 1 , Object8 ). The compatible Spouse Type to Object8 -Object0 - is also different from the ones classifying instances of Husband and x Object0 -Object2 and Object1 -, what shows that the model also accommodates types such as Partner as instances ( Object0 :: SpouseType , Object1 :: SpouseType , Object2 :: SpouseType , Object7 :: Spouse , Object3 :: Spouse , Object4 :: Husband , Object6 :: Wife , instantiation ( Object7 , Object0 ), instantiation ( Object3 , Object0 ), instantiation ( Object4 , Object2 ), instantiation ( Object6 , Object1 ).

[FIGURE]

## 5. Ontology usage and community impact

Over the years, UFO has been used for the development of core and domain ontologies on a wide range of domains, in academic, governmental and industrial contexts Guizzardi et al. (2015b). For instance, it has been used to provide conceptual clarification in domains ranging from natural sciences (e.g., agriculture, bioinformatics, geology) to 'purely informational' domains (e.g., telecommunications, mulsemedia, game design, programming languages), from methodological domains (e.g., design science research) to addressing practical environmental management problems (e.g., simulation for land covering and use, waste management, emergency and disaster management). Moreover, UFO and ontologies built with it have been used to analyze, reengineer, or integrate many modeling languages and standards in different domains (e.g., ArchiMate, ARIS, DEMO, ISO/IEC 24744, ITU-T G.805, BPMN, TOGAF, Tropos and i * , and UML). In particular, we call attention to a recent industry standard in the tourism area that is entirely based on UFO-B (AlpineBits Alliance, 2021).

Clearly one of the most influential applications of UFO has been on the design of the conceptual modeling language OntoUML and its ecosystem of methodological and computational tools. A recent study shows that UFO is the second-most used foundational ontology in conceptual modeling and the one with the fastest adoption rate (Verdonck and Gailly, 2016). That study also shows that OntoUML is among the most used languages in ontology-driven conceptual modeling (together with UML, (E)ER, OWL, and BPMN). Moreover, empirical evidence shows that OntoUML significantly contributes to improving the quality of conceptual models without requiring an additional effort to producing them. For instance, Verdonck et al. (2019) report on a modeling experiment conducted with 100 participants in two countries showing the advantages (in these respects) of OntoUML when compared to a classical conceptual modeling language (EER - Extended ER).

Currently, the development of UFO-based models through OntoUML is supported by a microservicebased infrastructure. The OntoUML as a Service infrastructure (Fonseca et al., 2021b), or OaaS, is designed to decouple model services developed by OntoUML researchers (e.g., transformations, verifications, simulations, verbalizations) and the modeling tools they support. As a result, these model intelligence services can be developed independently, making use of programming languages and libraries that best fit the researcher's needs and preferences, and later integrated into modeling tools, such as UML CASE tools. This is enabled by OaaS's low requirements on services and tool developers that consists of support to HTTP and JSON used for service request and model serialization respectively. The current implementation of OaaS consists of a JSON Schema specification to govern the JSON serialization of OntoUML models 28 , a TypeScript library to support the manipulation and serialization of OntoUML models 29 , an HTTP server that provides multiple model intelligence services 30 , and a plugin for the UML CASE Visual Paradigm 31 that extends it with OntoUML modeling capabilities 32 .

Besides OntoUML, UFO has been successfully used in the design of a number of ontologies in a multitude of sub-domains in Software Engineering (Duarte et al., 2018; Henderson-Sellers, 2012; HendersonSellers et al., 2014; Kirk and MacDonell, 2016; Maretto and Barcellos, 2014; Morales-Ramirez et al., 2015; Ruy et al., 2016; Shekhovtsov and Mayr, 2014; Sydorov et al., 2019; Bernabé et al., 2019; Duarte et al., 2018, 2021; Guizzardi et al., 2014; Negri et al., 2017). In fact, a number of these ontologies forming SEON (Software Engineering Ontology Network) 33 has been used to address problems such as application integration, semantic annotation of requirements, software quality assurance, code interoperability, among others.

28 The ontouml-schema project is available at https://purl.org/krdb-core/ontouml-schema.

29 The ontouml-js project is available at https://purl.org/krdb-core/ontouml-js.

[30 The ontouml-server is available at https://purl.org/krdb-core/ontouml-server.](https://purl.org/krdb-core/ontouml-server)

[31 https://www.visual-paradigm.com/](https://www.visual-paradigm.com/)

[32 The ontouml-vp-plugin is available at https://purl.org/krdb-core/ontouml-plugin.](https://purl.org/krdb-core/ontouml-plugin)

Finally, another area in which UFO had a noticeable impact is domains dealing with legal, social and economic aspects. These include financial accounting (Blums and Weigand, 2021; Fischer-Pauzenberger and Schwaiger, 2017; Fraller, 2019; Laurier et al., 2018) as well as domains dealing with legal relations and contracts (Sharifi et al., 2020; El Ghosh and Abdulrab, 2020, 2021; Griffo et al., 2015; Mário de Oliveira Rodrigues et al., 2020), as well as microeconomic subdomains such as resources and capabilities (Azevedo et al., 2015), competition (Sales et al., 2018c), economic exchanges (Porello et al., 2020), services (Nardi et al., 2015), money (Amaral et al., 2020b), trust (Amaral et al., 2019), risk and value (Guarino et al., 2016; Sales et al., 2018b), among others. The perceived usefulness of the ontology in these domains is unsurprising given that most of these domains require a sophisticated modeling of relational aspects. The proper modeling of all the aforementioned phenomena real requires the support of fuller theory of relations, which is one of the distinctive theoretical aspects of UFO.

## Acknowledgements

We are grateful to Gerd Wagner, Nicola Guarino, and the members of the Ontology &amp; Conceptual Modeling Research Group (NEMO) - especially, Renata Guizzardi and Ricardo Falbo ( in memoriam ) -for all the years of collaboration in the scope of UFO.

Claudenir M. Fonseca and Giancarlo Guizzardi are supported by the NeXON Project (Free University of Bozen-Bolzano). João Paulo A. Almeida is funded by the Brazilian Research Funding Agencies CNPq (grants number 313687/2020-0 and 407235/2017-5), CAPES (23038.028816/2016-41) Finance Code 001 and FAPES (281/2021). Daniele Porello thanks the European project OntoCommons (GA 958371) for co-funding the writing of this paper.

## References

- Albuquerque, A. &amp; Guizzardi, G. (2013). An ontological foundation for conceptual modeling datatypes based on semantic reference spaces. In IEEE 7th International Conference on Research Challenges in Information Science (RCIS) (pp. 1-12).
- Almeida, J.P.A., Falbo, R.A. &amp; Guizzardi, G. (2019). Events as entities in ontology-driven conceptual modeling. In International Conference on Conceptual Modeling (pp. 469-483). Springer. doi:10.1007/978-3-030-33223-5\_39.
- AlpineBits Alliance (2021). AlpineBits DestinationData 2021-04. https://www.alpinebits.org/destinationdata/.
- Amaral, G., Sales, T.P., Guizzardi, G. &amp; Porello, D. (2020b). A reference ontology of money and virtual currencies. In IFIP Working Conference on the Practice of Enterprise Modeling (pp. 228-243). Springer. doi:10.1007/978-3-030-63479-7\_16.
- Amaral, G., Sales, T.P., Guizzardi, G. &amp; Porello, D. (2019). Towards a reference ontology of trust. In H. Panetto et al. (Eds.), 27th International Conference on Cooperative Information Systems (CoopIS) . Lecture Notes in Computer Science (Vol. 11877, pp. 3-21). Cham: Springer.
- Azevedo, C.L.B., Iacob, M., Almeida, J.P.A., van Sinderen, M., Pires, L.F. &amp; Guizzardi, G. (2015). Modeling resources and capabilities in enterprise architecture: A well-founded ontology-based proposal for ArchiMate. Information Systems , 54 , 235-262. doi:10.1016/j.is.2015.04.008.
- Baker, L.R. (2007). The Metaphysics of Everyday Life . Cambridge: Cambridge University Press.
- Benevides, A.B., Bourguet, J.-R., Guizzardi, G., Penaloza, R. &amp; Almeida, J.P.A. (2019b). Representing a reference foundational ontology of events in SROIQ. Applied Ontology , 14 (3), 293-334. doi:10.3233/AO-190214.
- Benevides, A.B., Guizzardi, G., Braga, B.F.B. &amp; Almeida, J.P.A. (2010). Validating modal aspects of OntoUML conceptual models using automatically generated visual world structures. Journal of Universal Computer Science , 16 (20), 2904-2933.

[33 https://dev.nemo.inf.ufes.br/seon/](https://dev.nemo.inf.ufes.br/seon/)

- Bennett, K.H. &amp; Rajlich, V.T. (2000). Software maintenance and evolution: A roadmap. In Proceedings of the Conference on the Future of Software Engineering, ICSE'00 (pp. 73-87). ACM. doi:10.1145/336512.336534.
- Bera, P. &amp; Wand, Y. (2004). Analyzing OWL using a philosophy-based ontology. In A. Varzi and L. Vieu (Eds.), 3rd International Conference on Formal Ontology in Information Systems (FOIS) (pp. 353-62). IOS Press.
- Bernabé, C.H., Silva Souza, V.E., Almeida Falbo, R.D., Guizzardi, R.S.S. &amp; Silva, C. (2019). GORO 2.0: Evolving an ontology for goal-oriented requirements engineering. In G. Guizzardi, F. Gailly and R. Suzana Pitangueira Maciel (Eds.), Advances in Conceptual Modeling. ER 2019 . Lecture Notes in Computer Science (Vol. 11787, pp. 169-179). Springer. doi:10.1007/ 978-3-030-34146-6\_15.
- Blums, I. &amp; Weigand, H. (2017). Financial reporting by a shared ledger. In 8th International Workshop on Formal Ontologies Meet Industry (FOMI) .
- Blums, I. &amp; Weigand, H. (2021). Conceptualizing social relators and economic exchange contracts for reporting purposes. In International Workshop on Value Modelling and Business Ontologies (VMBO (Vol. 2835).
- Bradley, F. (1893). Appearance and reality: A metaphysical essay . Swan Sonnenschein &amp; Co.
- Bunge, M. (1977). Treatise on Basic Philosophy. Ontology I: The Furniture of the World. (Vol. 3). Reidel Publishing Company.
- Carmo, A.P., Zamperini, T., Mello, M.R.S., Leal, A.L.C. &amp; Garcia, A.S. (2017). Ontologia das coisas para espaços inteligentes baseados em visão computacional. In 9th Seminar of Ontology Research in Brazil (ONTOBRAS) .
- Carvalho, V.A. &amp; Almeida, J.P.A. (2018). Toward a well-founded theory for multi-level conceptual modeling. Software &amp; Systems Modeling , 17 (1), 205-231. doi:10.1007/s10270-016-0538-9.
- Carvalho, V.A., Almeida, J.P.A., Fonseca, C.M. &amp; Guizzardi, G. (2017). Multi-level ontology-based conceptual modeling. Data &amp;Knowledge Engineering , 109 , 3-24. doi:10.1016/j.datak.2017.03.002.
- Davidson, D. (2001). Essays on Actions and Events: Philosophical Essays (Vol. 1). Oxford University Press on Demand.
- de Oliveira Bringuente, A.C., de Almeida Falbo, R. &amp; Guizzardi, G. (2011). Using a foundational ontology for reengineering a software process ontology. Journal of Information and Data Management , 2 (3), 511-511.
- Duarte, B.B., de Almeida Falbo, R., Guizzardi, G., Guizzardi, R. &amp; Souza, V.E.S. (2021). An ontological analysis of software system anomalies and their associated risks. Data &amp; Knowledge Engineering , 134 , 101892. doi:10.1016/j.datak.2021. 101892.
- Duarte, B.B., Leal, A.L.C., Falbo, R.A., Guizzardi, G., Guizzardi, R.S.S. &amp; Souza, V.E.S. (2018). Ontological foundations for software requirements with a focus on requirements at runtime. Applied Ontology , 13 (2), 73-105. doi:10.3233/AO-180197.

El Ghosh, M. &amp; Abdulrab, H. (2020). Ontology-based liability decision support in the international maritime law. In

Knowledge and Information Systems

(pp. 273-276). IOS Press.

- El Ghosh, M. &amp; Abdulrab, H. (2021). Cargo-s: A pattern-based well-founded legal domain ontology for the traceability of goods in logistic sea corridors. Applied Ontology , 1-40.
- Evermann, J. &amp; Wand, Y. (2001). Towards ontologically based semantics for UML constructs. In H.S. Kunii, S. Jajodia and A. Sølvberg (Eds.), Conceptual Modeling. ER 2001 . Lecture Notes in Computer Science (Vol. 2224, pp. 354-367). Springer. doi:10.1007/3-540-45581-7\_27.
- Fischer-Pauzenberger, C. &amp; Schwaiger, W.S. (2017). The ontorea accounting model: Ontology-based modeling of the accounting domain. Complex Systems Informatics and Modeling Quarterly , 11 , 20-37. doi:10.7250/csimq.2017-11.02.
- Fitting, M. &amp; Mendelsohn, R.L. (2012). First-Order Modal Logic (Vol. 277). Springer.
- Fonseca, C.M., Almeida, J.P.A., Guizzardi, G. &amp; Carvalho, V.A. (2021a). Multi-level conceptual modeling: Theory, language and application. Data &amp; Knowledge Engineering , 134 , 101894. doi:10.1016/j.datak.2021.101894.
- Fonseca, C.M., Porello, D., Guizzardi, G., Almeida, J.P.A. &amp; Guarino, N. (2019). Relations in ontology-driven conceptual modeling. In International Conference on Conceptual Modeling (pp. 28-42). Springer. doi:10.1007/978-3-030-33223-5\_4.
- Fonseca, C.M., Sales, T.P., Viola, V., Fonseca, L.B.R., Guizzardi, G. &amp; Almeida, J.P.A. (2021b). Ontology-driven conceptual modeling as a service. In 11th International Workshop on Formal Ontologies Meet Industry (FOMI 2021) .
- Fraller, C. (2019). Flexible budgeting in an activity-based costing framework: From conceptual modeling to prototypical implementation . PhD thesis, Wien.
- Gärdenfors, P. (2004). Conceptual Spaces: The Geometry of Thought . MIT Press.
- Griffo, C., Almeida, J.P.A. &amp; Guizzardi, G. (2015). Towards a legal core ontology based on Alexy's theory of fundamental rights. In Multilingual Workshop on Artificial Intelligence and Law .
- Guarino, N., Andersson, B., Johannesson, P. &amp; Livieri, B. (2016). Towards an ontology of value ascription. In 9th International Conference on Formal Ontology in Information Systems (FOIS) (Vol. 283, p. 331). IOS Press.
- Guarino, N. &amp; Guizzardi, G. (2015). 'We need to discuss the relationship': Revisiting relationships as modeling constructs. In Advanced Information Systems Engineering. CAiSE 2015 . Lecture Notes in Computer Science (Vol. 9097, pp. 279-294).
- Guarino, N. &amp; Guizzardi, G. (2016). Relationships and events: Towards a general theory of reification and truthmaking. In G. Adorni, S. Cagnoni, M. Gori and M. Maratea (Eds.), Advances in Artificial Intelligence. AI*IA 2016 . Lecture Notes in Computer Science (Vol. 10037, pp. 237-249). doi:10.1007/978-3-319-49130-1\_18.
- Guarino, N., Guizzardi, G. &amp; Mylopoulos, J. (2020). On the philosophical foundations of conceptual models. Information Modelling and Knowledge Bases , 31 (321), 1.

Legal

- Guarino, N., Porello, D. &amp; Guizzardi, G. (2019). On weak truthmaking. In A. Barton, S. Seppälä and D. Porello (Eds.), Proceedings of the Joint Ontology Workshops 2019 Episode V: The Styrian Autumn of Ontology , Graz, Austria, September 23-25, 2019, CEUR Workshop Proceedings (Vol. 2518). CEUR-WS.org.
- Guarino, N. &amp; Welty, C.A. (2009). An overview of OntoClean. In Handbook on Ontologies, International Handbooks on Information Systems (pp. 201-220). Springer.
- Guerson, J., Sales, T.P., Guizzardi, G. &amp; Almeida, J.P.A. (2015). OntoUML lightweight editor: A model-based environment to build, evaluate and implement reference ontologies. In 19th IEEE International Enterprise Distributed Object Computing Workshops (pp. 144-147). IEEE. doi:10.1109/EDOCW.2015.17.
- Guizzardi, G. (2005). Ontological Foundations for Structural Conceptual Models . Enschede: CTIT, Centre for Telematics and Information Technology.
- Guizzardi, G., Almeida, J.P.A., Guarino, N. &amp; Carvalho, V.A. (2015a). Towards an ontological analysis of powertypes. In O. Papini et al. (Eds.), Joint Ontology Workshops (JOWO) (Vol. 1517). CEUR-WS.org.
- Guizzardi, G., Fonseca, C.M., Almeida, J.P.A., Sales, T.P., Benevides, A.B. &amp; Porello, D. (2021). Types and taxonomic structures in conceptual modeling: A novel ontological theory and engineering support. Data &amp; Knowledge Engineering , 134 .
- Guizzardi, G., Guarino, N. &amp; Almeida, J.P.A. (2016). Ontological considerations about the representation of events and endurants in business models. In M.L. Rosa, P. Loos and O. Pastor (Eds.), Business Process Management. BPM 2016 . Lecture Notes in Computer Science (Vol. 9850, pp. 20-36). Springer.
- Guizzardi, G., Masolo, C. &amp; Borgo, S. (2006). In defense of a trope-based ontology for conceptual modeling: An example with the foundations of attributes, weak entities and datatypes. In A. Persson and J. Stirna (Eds.), Conceptual Modeling. ER 2006 . Lecture Notes in Computer Science (Vol. 3084, pp. 112-125). Springer. doi:10.1007/11901181\_10.
- Guizzardi, G. &amp; Wagner, G. (2004b). A unified foundational ontology and some applications of it in business modeling. In M. Missikoff (Ed.), Enterprise Modelling and Ontologies for Interoperability. EMOI - INTEROP 2004 (Vol. 125). CEURWS.org.
- Guizzardi, G., Wagner, G., Almeida, J.P.A. &amp; Guizzardi, R.S.S. (2015b). Towards ontological foundations for conceptual modeling: The unified foundational ontology (UFO) story. Applied Ontology , 10 (3-4), 259-271. doi:10.3233/AO-150157.
- Guizzardi, G., Wagner, G., Falbo, R.A., Guizzardi, R.S.S. &amp; Almeida, J.P.A. (2013a). Towards ontological foundations for the conceptual modeling of events. In W. Ng, V.C. Storey and J.C. Trujillo (Eds.), Conceptual Modeling. ER 2013 . Lecture Notes in Computer Science (Vol. 8217, pp. 327-341). Springer.
- Guizzardi, G. &amp; Zamborlini, V. (2014). Using a trope-based foundational ontology for bridging different areas of concern in ontology-driven conceptual modeling. Science of Computer Programming , 96 , 417-443. doi:10.1016/j.scico.2014.02.022.
- Guizzardi, R.S.S., Li, F., Borgida, A., Guizzardi, G., Horkoff, J. &amp; Mylopoulos, J. (2014). An ontological interpretation of nonfunctional requirements. In 8th International Conference on Formal Ontology in Information Systems (FOIS) (pp. 344-357).
- Heller, B. &amp; Herre, H. (2004). Ontological categories in gol. Axiomathes , 14 (1), 57-76. doi:10.1023/B:AXIO.0000006788. 44025.49.
- Henderson-Sellers, B. (2012). On the Mathematics of Modelling, Metamodelling, Ontologies and Modelling Languages. Springer Briefs in Computer Science . Springer.
- Henderson-Sellers, B., Gonzalez-Perez, C., McBride, T. &amp; Low, G. (2014). An ontology for ISO software engineering standards: 1 creating the infrastructure. Computer Standards &amp; Interfaces , 36 (3), 563-576. doi:10.1016/j.csi.2013.11.001.
- Herre, H., Heller, B., Burek, P., Loebe, F. &amp; Michalek, H. (2004). General ontological language: A formal framework for building and representing ontologies (version 1.0). Onto-Med Report 7, Reseach Group Ontologies in Medicine.
- Hitchman, S. (2003). An interpretive study of how practitioners use entity-relationship modelling in a ternary relationship situation. Communications of the Association for Information Systems , 11 , 26. doi:10.17705/1CAIS.01126.
- Hovda, P. (2009). What is classical mereology? Journal of Philosophical Logic , 38 (1), 55-82. doi:10.1007/s10992-008-9092-4. Keil, F.C. (1992). Concepts, Kinds, and Cognitive Development . MIT Press.
- Kirk, D. &amp; MacDonell, S. (2016). An ontological analysis of a proposed theory for software development. In P. Lorenz, J. Cardoso, L.A. Maciaszek and M. van Sinderen (Eds.), Software Technologies. ICSOFT 2015 . Communications in Computer and Information Science (Vol. 586, pp. 155-171). Cham: Springer.
- Laurier, W., Kiehn, J. &amp; Polovina, S. (2018). Rea 2: A unified formalisation of the resource-event-agent ontology. Applied Ontology , 13 (3), 201-224. doi:10.3233/AO-180198.
- Lowe, E.J. &amp; Lowe, E.J. (2006). The Four-Category Ontology: A Metaphysical Foundation for Natural Science . Oxford University Press.
- Maretto, C.X. &amp; Barcellos, M.P. (2014). A levels-based approach for defining software measurement architectures. CLEI Electronic Journal , 17 (3). doi:10.19153/cleiej.17.3.4.
- Mário de Oliveira Rodrigues, C., Bezerra, C., Freitas, F. &amp; Oliveira, I. (2020). Handling crimes of omission by reconciling a criminal core ontology with UFO. Applied Ontology , 15 (1), 7-39. doi:10.3233/AO-200223.
- Masolo, C., Borgo, S., Gangemi, A., Guarino, N. &amp; Oltramari, A. (2003). WonderWeb Deliverable D18 . Technical report, CNR. Moltmann, F. (2020). Variable objects and truthmaking. In Metaphysics, Meaning, and Modality (pp. 368-394). Oxford University Press. doi:10.1093/oso/9780199652624.003.0020.

- Morales-Ramirez, I., Perini, A. &amp; Guizzardi, R.S. (2015). An ontology of online user feedback in software engineering. Applied Ontology , 10 (3-4), 297-330. doi:10.3233/AO-150150.
- Nardi, J.C., Falbo, R.A., Almeida, J.P.A., Guizzardi, G., Pires, L.F., van Sinderen, M., Guarino, N. &amp; Fonseca, C.M. (2015). A commitment-based reference ontology for services. Information Systems , 54 , 263-288. doi:10.1016/j.is.2015.01.012.
- Negri, P.P., Souza, V.E.S., Leal, A.L.C., Falbo, R.A. &amp; Guizzardi, G. (2017). Towards an ontology of goal-oriented requirements. In 20th Iberoamerican Conference on Software Engineering (CIBSE) , Buenos Aires, Argentina, May 22-23, 2017 (pp. 469-482).
- Parsons, T. (1990). Events in the Semantics of English (Vol. 5). Cambridge, MA: MIT Press.
- Porello, D., Guizzardi, G., Sales, T.P. &amp; Amaral, G. (2020). A core ontology for economic exchanges. In G. Dobbie, U. Frank, G. Kappel, S.W. Liddle and H.C. Mayr (Eds.), Conceptual Modeling . Lecture Notes in Computer Science (Vol. 12400, pp. 364-374). Springer. doi:10.1007/978-3-030-62522-1\_27.
- Quine, W.V.O. (1937). New foundations for mathematical logic. The American mathematical monthly , 44 (2), 70-80. doi:10. 1080/00029890.1937.11987928.
- Ruy, F.B., Falbo, R.A., Barcellos, M.P., Costa, S.D. &amp; Guizzardi, G. (2016). SEON: A software engineering ontology network. In 20th International Conference on Knowledge Engineering and Knowledge Management (EKAW) (pp. 527-542).
- Sales, T.P., Baião, F., Guizzardi, G., Guarino, N. &amp; Mylopoulos, J. (2018b). The common ontology of value and risk. In J.C. Trujillo et al. (Eds.), Conceptual Modeling. ER 2018 . Lecture Notes in Computer Science (Vol. 11157, pp. 121-135). Cham: Springer.
- Sales, T.P. &amp; Guizzardi, G. (2015). Ontological anti-patterns: Empirically uncovered error-prone structures in ontology-driven conceptual models. Data &amp; Knowledge Engineering , 99 , 72-104. doi:10.1016/j.datak.2015.06.004.
- Sales, T.P., Porello, D., Guarino, N., Guizzardi, G. &amp; Mylopoulos, J. (2018c). Ontological foundations of competition. In S. Borgo, P. Hitzler and O. Kutz (Eds.), 10th International Conference on Formal Ontology in Information Systems (FOIS) . Frontiers in Artificial Intelligence and Applications (Vol. 306, pp. 96-109). IOS Press.
- Sharifi, S., Parvizimosaed, A., Amyot, D., Logrippo, L. &amp; Mylopoulos, J. (2020). Symboleo: Towards a specification language for legal contracts. In 2020 IEEE 28th International Requirements Engineering Conference (RE) (pp. 364-369). IEEE. doi:10.1109/RE48521.2020.00049.
- Shekhovtsov, V.A. &amp; Mayr, H.C. (2014). Managing quality related information in software development processes. In CAiSE Forum and Doctoral Consortium 2014 (Vol. 1164, pp. 73-80). CEUR-WS.org.
- Smith, B.C. (2019). The Promise of Artificial Intelligence: Reckoning and Judgment . Mit Press.
- Stout, R. (1997). Processes. Philosophy , 72 (279), 19-27. doi:10.1017/S0031819100056631.
- Strawson, P.F. (1959). An essay in descriptive metaphysics. Chapter individuals.
- Sunyé, G., Pollet, D., Le Traon, Y. &amp; Jézéquel, J.-M. (2001). Refactoring UML models. In M. Gogolla and C. Kobryn (Eds.), UML 2001 - The Unified Modeling Language. Modeling Languages, Concepts, and Tools . Lecture Notes in Computer Science (Vol. 2185, pp. 134-148). Springer. doi:10.1007/3-540-45441-1\_11.
- Sutcliffe, G. (2017). The TPTP problem library and associated infrastructure. From CNF to TH0, TPTP v6.4.0. Journal of Automated Reasoning , 59 (4), 483-502. doi:10.1007/s10817-017-9407-7.
- Sydorov, N., Sydorova, N., Sydorov, E., Cholyshkina, O. &amp; Batsurovska, I. (2019). Development of an approach to using a style in software engineering. Eastern-European Journal of Enterprise Technologies , 4 (2), 41-51. doi:10.15587/1729-4061. 2019.175665.
- Thomson, J.J. (1998). The statue and the clay. Noûs , 32 (2), 149-173.
- Verdonck, M. &amp; Gailly, F. (2016). Insights on the use and application of ontology and conceptual modeling languages in ontology-driven conceptual modeling. In I. Comyn-Wattiau et al. (Eds.), Conceptual Modeling. ER 2016 . Lecture Notes in Computer Science. (Vol. 9974). Springer.
- Verdonck, M., Gailly, F., Pergl, R., Guizzardi, G., Martins, B. &amp; Pastor, O. (2019). Comparing traditional conceptual modeling with ontology-driven conceptual modeling: An empirical study. Information Systems , 81 , 92-103. doi:10.1016/j.is.2018.11. 009.
- Veres, C. &amp; Hitchman, S. (2002). Using psychology to understand conceptual modelling. In ECIS (pp. 473-481).
- Veres, C. &amp; Mansson, G. (2005). Cognition and modeling: Foundations for research and practice. Journal of Information Technology Theory and Application , 7 (1), 9.
- Wand, Y., Storey, V.C. &amp; Weber, R. (1999). An ontological analysis of the relationship construct in conceptual modeling. ACM Transactions on Database Systems , 24 (4), 494-528. doi:10.1145/331983.331989.
- Wand, Y. &amp; Weber, R. (1989). An ontological evaluation of systems analysis and design methods. In E. Falkenberg and P. Lindgreen (Eds.), Informution Systems Concepts - An In-Depth Analysis (pp. 79-108). North-Holland.
- Wand, Y. &amp; Weber, R. (1990). An ontological model of an information system. IEEE Transactions on Software Engineering , 16 (11), 1282-1292. doi:10.1109/32.60316.
- Weber, R. (1997). Ontological Foundations of Information Systems . Coopers &amp; Lybrand and the Accounting Association of Australia and New Zealand Melbourne.

Weber, R. &amp; Zhang, Y. (1991). An ontological evaluation of niam's grammar for conceptual schema diagrams. In ICIS (pp. 75-82). Association for Information Systems.

Zamborlini, V., Betti, A. &amp; van den Heuvel, C. (2017). Toward a core conceptual model for (im)material cultural heritage in the golden agents project. In 1st International Workshop on Understanding Events Semantics in Cultural Heritage .
