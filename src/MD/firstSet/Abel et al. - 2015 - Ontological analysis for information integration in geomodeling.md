## RESEARCH ARTICLE

## Ontological analysis for information integration in geomodeling

Mara Abel &amp; Michel Perrin &amp; Joel Luis Carbonera

Received: 31 March 2014 /Accepted: 2 February 2015 /Published online: 3 March 2015 # Springer-Verlag Berlin Heidelberg 2015

Abstract When building earth models, data heterogeneity is a major difficulty. Heterogeneity can be a consequence of different geologists ' views or goals when capturing the data, or can be a result of representing the geological models through distinct modeling languages. We analyze here how each one of these causes affect the way in which the geological information is captured into models and systems. The major claim of this paper is that many problems related to these heterogeneities can be solved or at least simplified by analyzing the models through the view of Ontology. We assume that heterogeneity is originally related to the different choices that a geologist makes, when she/he decides to consider a particular set of qualities among the large number of qualities that are attached to the entities that she/he intends to model. Considering this, for deciding which attributes hold the ontological nature of a given category of geological entity, one can apply the ontological notions of identity, rigidity, essentiality and unity. This allows solving the difficulties due to the heterogeneity of modeling languages by identifying, among the many entities and properties considered by the geologists, those that are eligible for being mapped from one model to another, not considering the name that they bear or the format in which they are represented. This paper also discusses how to build good models for further integration, avoiding some common misuse of hierarchical and partonomy

## Communicated by: H. A. Babaie

Published in the Special Issue of Semantic e-Science with Guest Editors Dr. Xiaogang Ma, Dr. Peter Fox, Dr. Thomas Narock and Dr. Brian Wilson

M. Abel ( * ) : J. L. Carbonera Informatics Institute, Universidade Federal do Rio Grande do Sul (UFRGS), Porto Alegre, Brazil e-mail: marabel@inf.ufrgs.br

J. L. Carbonera e-mail: jlcarbonera@inf.ufrgs.br

M. Perrin GEOSIRIS, Fourqueux, France e-mail: michel.perrin@geosiris.com

relationships, and the limitations of the current available representation languages. Finally, we examine as a case study the ' Petroleum system ' , providing a concrete example for explaining how some issues related to data heterogeneity can be dealt with in practice.

Keywords Information heterogeneity . Geological data integration . Ontology . . Semantic interoperability

## Introduction

At present, many geoscientists need to manipulate and integrate huge volumes of data that belong to many different categories. Geological surveys not only establish geological and structural maps at various scales, but also various kinds of thematic maps (hydrogeology, natural resources, geological risks and so forth), which require the record and synthesis of a large number of geo-located data and their interpretations. They also intend to better coordinate data formats, interpretations and representations in order to harmonize maps related to adjacent regions and produce relevant maps at broader scales both as paper copies and as scalable digital views. In another field, hydrocarbon exploration and production rest on more and more sophisticated 3Dor4Dmodelsfor describing individual reservoirs, as well as large sedimentation basins. As shown in Fig. 1, the process of modeling oil reservoirs involves a complex sequence of activities, each of which rests on different kinds of data interpreted by various groups of experts (geophysicists, structural geologists, sedimentologists, petrographers, engineers), each specialized in a specific field. Considering this diversity, there is a growing need of building software applications not only able to manipulate a large number of data of different kinds and produced by separate vendors, but also the interpretations attached to them (Perrin and Abel 2013).

[FIGURE]

Fig. 1 The reservoir modeling workflow showing the sequence of stages in data acquisition and interpretation (redrawn from (Perrin et al. 2007))

[FIGURE]

Interoperability among the geological applications that are used for building large geological models can be compromised by different kinds of heterogeneity and by the ambiguities that result from this situation. In the field reservoir studies, this difficulty has been pointed out by several authors such as (Cosentino 2001), (Fanchi 2005), (Ludäscher et al. 2006), (Perrin and Abel 2013). The article of Chum (Chum 2007) notably mentions the following issues:

- -dealing with large amount of data generated every day from multiple sources (seismic data, well data, drilling data, transportation data, and marketing data)
- -the need of a new approach to search and access to this flood of information and to cope with the heterogeneous formats of the data,
- -the need of standardizing and integrating information across systems, disciplines and organizational boundaries.

The goal of the present paper is to provide to the Geosciences field some tools for dealing with the issues related to data heterogeneity and notably those related to conceptualization and to representation formalisms. We intend to show that the conceptual tools provided by ontology theories allow operating a sound conceptual analysis of the invariant and consensual part (the ontological part) of the geological knowledge used for geo-modeling. This is likely to facilitate the tasks of modeling and of integrating legacy models. Therefore, the second section ' Ontologies ' provides some philosophical introduction to Ontology by discussing the meaning of some geological entities. It also shortly presents the Unified Foundational Ontology applied in this work. The third section ' Semantic heterogeneity in geological information ' introduces the technical meaning of heterogeneity in terms of Computer Science, discussing how the several types of heterogeneity are perceived and solved in the Geology domain. The ' Petroleum system ' case-study that comes next introduces the description of the geological case that we use for applying our approach, ending with a well-formed example of modeling using ontological analysis. The Conclusion of the paper finally discusses the advantages and limitations of our approach.

[FIGURE]

## Ontologies

This section presents the theories in Ontology adopted as the basis for our studies and introduces the conceptual framework for ontological analysis.

Background concepts in Ontology

## Ontological engineering

Ontology engineering is growing in importance as a conceptual tool for providing interoperability among applications and data in petroleum industry. The contribution for making evident the semantics of information and data is undeniable, but further developments need to be accomplished in order to achieve a homogenous and uniform view over the modeled domain. We deal here with ontological analysis, trying to make apparent and represent the invariant aspects across all the possible situations that occur for a given domain, specifying the types of entities that are supposed to exist in the reality by a community.

Our study refers to what was called by Guarino in (Guarino 1994) the Ontological Level, to differentiate it from the Epistemological Level of knowledge representation. Although well-founded ontologies can be used as a support for developing good knowledge models or knowledge-based systems, for the ontological analysis point of view, questions like reasoning, context or uncertainty treatment are not considered, since they are not ontological issues. In short, knowledge models (in general) deal with problems and how to solve them. Ontologies deal with what are the entities of the world and what is invariant on them and can be used to track these entities through time and space (and obviously, through legacy systems).

## Conceptualization, knowledge models and ontologies

In order to provide a better understanding of the propositions discussed throughout this article, we will at first define a small set of terms that support our explanation. We will use concept to refer to the mental abstraction of some entities of reality, i.e., entities that only exist in human mind. Entity refers to entities that can be whether universals (abstract modeled entities) or particulars (instances). A mental representation of a portion of reality created according to a previous conceptualization will be called a mental model , while a concept in some specific model will be described as a modeled concept . A concept will be materialized in some artifact as one or more representations .

The object of ontology studies is the conceptualization , which is the set of concepts used to articulate the abstractions of the state of affairs in a given domain. A conceptualization captures the invariant aspects of entities that are not dependent of the context or a particular application of the model, such as the consensual meaning of core concepts like geological units or boundaries, faults, folds, channels, sedimentary basins, geological reservoirs and also lithological types, rock porosity and permeability, seismic speeds, rock rheological properties. The goal of ontologies is to characterize the meaning of the basic ontological categories used to describe the domain and to restrict the number of possible interpretations of knowledge models in the epistemological level (Guarino 1995).

Conceptualizations and models are abstract entities that only exist in geologists ' mind. In order to be documented, communicated and analyzed, they need to be externalized in specifications, using a representation language that is acknowledged by the community that will use the model. This process is shortly illustrated in Fig. 2. Although we agree that each human being has his/her particular conceptualization about the world, we also consider that in order to achieve communication among the practitioners of a community, some part of this conceptualization need to have some invariante aspects to be shared. Guarino, in the set of articles cited in this paper, has established the theoretical basis that allows us considering an ontology as the shared portion of a conceptualization and use it for building good geological models.

In general, models are built for supporting some kind of problem solving. We acknowledge that these models need to deal with distinct contexts and uncertainties regarding, for example, recognition of geological entities in the field, or interpretation of the gathered data. These issues arise only when a geologist is articulating knowledge about some specific state of affairs. However, in this paper we are interested in ontological issues, which concern what is invariant in all possible states of affairs of a given domain. Our focus is to use ontologies for making explicit (a) the set of categories of entities that are supposed to exist in a given domain, and (b) the meaning that is assigned to each of these categories. We claim that these issues are fundamental for building accurate models of the geologic reality.

## The dual sense of ontology

The term Ontology was originally defined in philosophy as a particular theory about the nature of being or the kinds of existents (Guizzardi 2005). In the Computer Science context, the term ontology is used with two different meanings: (1) an artifact that represents a portion of reality according to the theory of existence (Gruber 2003); (2) a logical theory accounting for the intended meaning of a formal vocabulary utilized for representation (Guarino 1998). As an artifact (a model specified in a language and stored in a format), an ontology can represent a domain and be used for information integration and for supporting applications. However, ontologies are not simply knowledge models and this artifact should be built to express the common understanding of a community about the existence of beings. The ontology as a theory provides the support to build models that capture this understanding and specifies what types of entities are supposed to exist in the reality according a community.

## Knowledge building: an example

In a simple example, let us consider the modeling of a mineral crystal . Then our domain of investigation can be, for example, the instances to which we have real access out of the pictures represented in Fig. 3.

Some knowledge model would abstract the common characteristics of these particular instances and create an abstract model that can represent them. The knowledge acquisition questions would include questions such as:

[FIGURE]

Fig. 2 Steps in the creation of computer-based models. A geologist studies the domain and creates a mental model of his/her interpretation of the world based in his/her previous conceptualization. This mental model needs to be externalized in some kind of physical representation

[FIGURE]

- -What have these instances in common?
- -What are their variations in properties like color, size, height, weight?
- -What are they used for?

The resulting model would include the attributes listed in the Fig. 4.

Notice that, in general, knowledge models are built with specific uses in mind and some modelers build models trying to meet only the immediate requirements at hand. Our model aims to represent the three above entities that are supposed to be the ones accessible in the universe of discourse of this modeler. The resulting model (such as the model represented in Fig. 4) has a very narrow scope and, it will probably be necessary to make a further modification for accommodating new cases that were not considered at the beginning. Consequently, this model will have a low potential of reuse, and it will be hard to integrate it with other models.

For developing a domain ontology about mineral crystals, having access to the same instances, the questions that would raise are:

- -What makes a mineral being a mineral crystal?
- -What is not a mineral crystal?
- -What will a mineral crystal become when it stops being a mineral crystal?
- -What was the mineral crystal before?
- -Can a mineral crystal have other habits and continue to be a mineral crystal?

Fig. 3 A few instances of mineral crystal in the domain of investigation

[FIGURE]

to be communicated among a group. Several shared representations are used as a base to create formal representations and the applications that manipulate them

- -Where else can a mineral crystal be than a mineral crystal?

and so forth.

The resulting model showed in Fig. 5 would consider capturing the essential of all existent mineral crystals.

As expected, the model seems more similar to a taxonomical definition in Mineralogy, than to a description of the three crystals. External or functional characteristics, like uses or shape were not included in Fig. 5, because they are not intrinsic properties of the mineral and have no relation with its ontological nature, although the same attributes can be requested and modeled to attend several applications based in domain knowledge. In addition, it would make no sense to define a subclass Gem crystal for designating mineral crystal that can be used as jewels, since this subclass would describe a category that includes several kinds of materials that are not natural mineral crystals.

## Key concepts selection

Ontological analysis investigates the invariant conceptualization across all possible situations of a given domain. When building a knowledge or information conceptual model that is intended to be further integrated, the modeler should first

[FIGURE]

Fig. 4 Knowledge model of a mineral crystal

describe the geological entities that preserve identity through all situations in the domain (that we define as rigid entities), hold independent existence, can exist as wholes and preserve their existences in any possible world. Our natural choice should then be to represent a lithological unit rather than a reservoir (that could possibly stop being considered a reservoir but that will remain a lithological unit), a geological structure rather than a trap (a trap would not be a trap in a region where there are no hydrocarbons around), and hydrocarbon rather than fuel (since in a world that would have developed alternative sources of energy, oil might cease to be used as a fuel but will still be a hydrocarbon). These concepts and choices will be the main framework for anchoring raw data and support model integration.

## Unified foundational ontology

Foundational ontologies are domain independent systems of categories and their relations, which can be used to clarify the meaning of the concepts applied to build models of a specific domain. In this paper, we adopt the Unified Foundational Ontology (UFO) proposed by Guizzardi (Guizzardi 2005). This meta-ontology provides a set of categories that account for the ontological distinctions underlying language and cognition. These categories help in building uniform conceptual models by orienting the modeler in the ontological choices of associating the entities to some representational primitives. These ontological choices are shown to have impact in implementation decisions and in the potential interoperability of implemented systems, as we will see later on in this paper.

## Particulars and universals

We will introduce here the main categories applied by UFO in ontological analysis. UFO is an ontology of particulars and universals. Roughly speaking, the distinction between universal and particular (or individual) is analogous to the distinction

Fig. 5 Ontological model of a mineral crystal

between types (classes) and their instances, in conceptual modeling. A particular is a single existent entity, while a Universal is an abstraction that generalizes this particular and others of the same type. Thus, UFO provides a set of categories of particulars and a set of categories of universals. The categories of universals can be viewed as meta-types, since they are ' types of types ' . These meta-types are used for classifying concepts in domain models according to their ontological properties.

## Endurants and perdurants

Initially, regarding the universals, UFO distinguishes between Endurant Universal and Perdurant Universal (or Event Universal). This distinction is based on the temporal behavior of the entities. Endurant universals are those whose individuals are wholly present whenever they are present, i.e., they are in time . For example, person, company, rock, reservoir and petroleum are examples of endurant universals. On the other hand, perdurant universals correspond to individuals composed of temporal parts; they happen in time , in the sense that they extend in time accumulating temporal parts. Events like earthquakes, volcano eruption, and deposition are examples of perdurants. Endurants have a relation of participation in perdurant occurrences, and these are commonly responsible for the creation, modification or destruction of those. For example, plates and faults are, among others, the endurant participants of an earthquake.

Besides that, foundational ontologies deal with ontological properties drawn from Philosophy (e.g., identity, dependence, unity), i.e., with formal aspects of universal and individuals irrespective of their particular nature. The properties applied in this work are essence, identity, and unity (Guarino and Welty 2004).

## Essence

Aproperty of an entity is essential to that entity if it must hold for it. It is a definitional property that explains what makes some individual to be an instance of a particular universal. Some essential properties are rigid, meaning that they are essential to all their possible instances. For example, it is essential for a mineral having a crystalline structure since a mineral that would not have this property would stop being a mineral. 1 Having a crystalline structure is a rigid property for a mineral that helps in identifying and defining it. Some properties are anti-rigid. For example, a prospect is defined as a region with economic interest. Being a prospect is an anti-rigid property, since the region can become not interesting if the petroleum price goes down in market. Even if the prospect stops being so, the concrete entity that was before the prospect (the region) is still there. The classical example for anti-rigidity describes the property of being a student . A student is an anti-rigid property that is held by some person when a relation between that person and an educational institution is effective. When the relation stops being effective (when the student is graduated, for example), the student stops to exist as a student, but the person, who provides the identity to that student, is still there. Rigid properties are important because they identify the entities that are present in all geological models and can be mapped from one model to another.

1 Minerals without a crystalline structure, such as opal, are no longer considered as minerals but are put in the category mineraloids .

[FIGURE]

## Identity

Identity refers to the issue of being able to recognize individual entities in the world as being the same (or different) regarding some characteristic properties. This ontological property is crucial for geological interpretation and is used by geologists to interpret stratigraphic and structural correlations. Identity criteria allow us to recognize that a person that was a classmate in our school many years ago is the same person that we met today, even if the superficial aspects (hair color, voice, way of dressing, etc.) are completely different now. Identity refers to the essence of entities and involves, for instance, the genetic causes that were responsible by the formation of a given rock stratum. Thus, if two rock strata, which were described in two different exploration wells, are found to have been generated by the same geologic event, they are actually considered as being the same rock stratum. In practical terms, deciding whether an entity carries an identity criterion or not is often hard, especially for natural kinds and artifacts. Even so, trying to clarify what are the essential properties of entities appear to be a useful support for building accurate conceptual models.

## Unity

The ontological and epistemological issues on defining identity and unity are properly discussed in (Guarino and Welty 2001). Unity refers to the problem of describing the parts and boundaries of an individual, so that we can decide what is part of the entity, what is not, and under what conditions the entity is a whole. For example, water is a concept whose instances are not wholes, except if they are limited by an instance of some other entity, such as a cup, a bottle or a lake. In the same sense, rocks have no unity, since a rock can only be individualized by a core, a sample or a geological unit.

## Dependence

Another important notion is the existential dependence . A given entity x is said to be existentially dependent on another entity y , if y must exist whenever x exists. For example, we can say that a given porous rock portion can be considered as existentially dependent on the rock of which it is a part. Finally, in our approach, we also use the notion of relational dependence . Wesay that a concept x is relationally dependent on a concept y via relation r , if every particular object that is an instance of x is related to a particular object that is instance of the concept y via relation r . For example, the concept of source rock is considered as relationally dependent on the concept of Hydrocarbon, via the relation generates. This means that a rock is considered a source rock when it generates hydrocarbon.

[FIGURE]

## Kinds and Subkinds

UFOprovides a set of categories for endurants, called UFO-A. Among the endurants, the Sortal Universals provide principle of identity and unity to their instances. This means that any concept in the model that can be categorized as a Sortal Universal will have instances in reality, which, in Geology, corresponds to instances with spatial presence (they will be concrete). Kind is a Sortal Universal that supplies identity and whose instances are existentially independent and can be made of parts (such as a rock made of minerals or a person made of organs). Subkinds are Sortals whose identities are supplied by another Sortal (their superclass). In general, we can classify the concepts Man and Woman as Subkinds, since they carry the identity supplied by the concept Person, which can be classified as a Sortal.

## Quantity universals

Some Sortal Universals are amount of matters that have concrete existence and identity but they do not represent countable instances (they do not hold unity). This definition differs from the original quantity category defined in UFO, which considers all its parts essential (if we change a part, it becomes a new instance), while, in our notion, amount of matter does not hold unity and its instances don ' t compose wholes or parts. Typical examples are the substances that form the matter of the Kinds, such as water, rock, ceramic, wood, etc. In order to allow one to represent individualized instances of quantities, a portion of matter needs to be individualized by a container. Then a sample of rock, a rock unit, a core, or a thin-section act as containers for some amount of rock, in the same way that a bottle delimits some amount of water. In such case, portions of rock have their own identities as portions, they are kinds in UFO sense, but the amount of matter that constitute them preserves a unique identity as a rock. We consider that the identity of a rock is provided by its composition and origin; then disconnected pieces of a rock are different instances of a rock portion but constitute a single instance of a rock. This assumption guarantees that we can consider that a rock will be the same rock in its spatial continuity and also if it is broken in pieces, since all the pieces were generated in the same geological process. This definition of the rock concept embodies the geological notion of a rock and it is required for geological reasoning, when a geologist takes several instances of portions of rock in order to understand the unique rock that constitutes all the portions.

## Role, categories and Mixins

Some sortals carry Unity and have concrete existence, but they are defined by some anti-rigid criteria of identity: such are the Roles . A source rock is a role of rock unit when it is possibly producing oil. There also exist endurants that are not Sortals. This is the case, for example, of Category, which represents essential properties of instances of many different kinds. Gemstone is a typical example of category, since it can classify material as diverse as tourmaline crystal and amber (organic material). Mixin is another non-sortal. It abstracts universals that are anti-rigid (such as roles) and universals that are rigid (such as kinds).

## Quality universals, quality structures

Quality Universals are Endurant Universals whose instances are existentially dependent individuals, which inhere in other individuals. Quality Universals represent the properties in conceptual models. The set of values that a property can assume are represented by Quality Structures. Each value that belongs to a quality structure is called quale. This approach allows us to share properties of entities and to compare attributes that inhere to other entities. Figure 6 illustrates the relation between a Sortal Universal and its quality universal and quality structures. The value of granularity is an instance of a value in a dimension of grain size. This dimension allows performing comparisons like stating that ' the granularity of this rock is the same as the one of that other rock ' , ' the brown color of this sample is the same brown as the one of that piece of wood ' . This means that both values refer to the same instance in a quality dimension.

Fig. 6 Structure of properties of endurants in ontology (modified from (Guizzardi 2005))

## Parthood relations

UFO-A also proposes four types of parthood relations and clarifies their semantics: memberOf, componentOf, subCollectionOf and subQuantityOf. Each type of parthood relation has its own ontological restrictions. The metacategories proposed by UFO are a great contribution to the problem of modeling the semantics of the part of relations, which are usually treated as having the same semantics in knowledge models.

Parthood relations are extremely important in geological modeling, since the comprehension that a geological entity is part or not of another entity is the basic support for correlation and structural interpretation. Figure 7, provides a general view of UFO-A categories, including some that were not discussed in this paper. For a detailed description of UFO-A, see (Guizzardi 2005).

## Perdurants

The Unified Foundational Ontology defines categories of perdurants in UFO-B for modeling the dynamic aspects of a domain. UFO-B considers that an event can be atomic or complex (made of temporal parts) and that some sortal universal participate in the event occurrence. UFO-B also models time relations between these entities (before, meets, overlaps, starts, ends, during, equals).

We will apply these ontological categories to develop our analysis of earth models.

## Semantic heterogeneity in geological information

Wewill discuss in this section the aspects of information heterogeneity that can be ameliorated with the use of an ontology approach.

## Background considerations

A set of data is considered heterogeneous when the data are diverse in origin, format, and content and, as a consequence, are not directly comparable. Interpretation heterogeneity is inherent in geologists ' tasks. Geologists perform their interpretations using the expert knowledge that they possess. The fields of interest of stratigraphers, sedimentologists, petrologists, structural geologists are different and, consequently the mental models used by each of these categories of geologists also vary. Even geologists who share the same field of interest may provide different interpretations of one same set of data since they may belong to different schools of thought or since they may be either experts or novices. Finally, interpretations provided by two geologists may also vary just because one may have observed more data than the other.

[FIGURE]

[FIGURE]

Fig. 7 System of categories of UFO-A (Guizzardi 2005)

[FIGURE]

What is necessary in terms of knowledge management, is considering that the assertions provided by a geoscientist at all scales (i.e. from the elementary geological entity up to a full earth model) and at all the stages of a modeling process are always tentative interpretations that may be contradicted by some other interpretations. Most of the knowledge models that are currently used for recording and managing geological data such as GeoSciML 2 or RESQML, 3 carefully take this point of view into account by allowing the characterization of each interpretation by means of a set of metadata (who produced it? when was it produced? etc.).

[FIGURE]

In this paper, we will mostly focus our attention on other heterogeneities related to conceptualization formalisms, for which conceptual methodologies can help in developing automatic or semi-automatic information integration. Our reflection will be illustrated by a particular example, that of the study of a hydrocarbon reservoir, which will be developed in the next session dedicated to ' The Petroleum system case-study ' .

[2 http://www.geosciml.org/](http://www.geosciml.org/)

[3 www.energistics.org/reservoir/resqml-sig](http://www.energistics.org/reservoir/resqml-sig)

## Adopted modeling options

Obtaining a uniform view of reality is a difficult task. Any modeling activity is based on a pre-defined set of types of entities that are acknowledge by the modeler, who accordingly controls the mental abstractions that her/his mind operates when examining the various entities of the world that she/he considers. However, we will assume here that, in any specific case, the various conceptualizations and the various models that are deduced from these conceptualizations all refer to the same existing world. In other words, we adopt the referential approach philosophy that states that there exists some entity in the real world, which materializes the meaning of any modeled concept (Gärdenfors 2000). For the same reason, we adopt a endurantist philosophical view of modeling that considers that an entity in reality exists through time, which means that it is wholly present at more than one time without losing its identity (Zimmerman 1996). The combination of these two philosophical views allows us to consider that there is only one reality to be modeled and that entities and notably geological entities keep their identity through time, even when they are modified by some geological phenomena, until they stop existing. Complementing these views, we adopt the notion of logical modality (Fitting and Mendelsohn 1998) that extends classical logics to represent concepts regarding possibility, necessity and temporality, among others. This allows us to represent events (such as generation or migration of oil) that induce entity transformations (for example the events that allow a rock unit to become a reservoir). According to these two philosophical views, the conceptual model is considered as a snapshot of entities that have spatial temporal existence in the world. This means that we anchor the concepts of our model in concrete geological entities of the world that will provide meaning to them.

When we adopt the referential and endurantism conceptual framework, the differences between the views of a structural geologist, of a stratigrapher and of a petrologist are just related to the differences of ontological choices, i.e., to the choices that each of them makes in considering a particular set of qualities among the large (but finite) number of qualities that are attached to the entities that they intend to model.

## Identity issues

At this point, we need to consider how we can decide that two entities that exist in the real world are the same, in the case when two modelers select two disjoint set of attributes to represent each of them. The simplest assumption would be to assume that two individuals are the same if they have the same name. However, in geologic models, we often find examples where one name is applied to ontologically distinct entities.

Considering geological models, we can find several examples when one same name is applied to ontologically distinct entities ( polysemy ). The most common polysemic name in geology is rock, which can refer to a petrological class of rock, to a rock sample, to a rock unit and so forth. Another example can be found in the names of geological ages. The term « Oxfordian » designates a geological period in the Jurassic , but may also designate, in a local context, any geological formation, whose age is Oxfordian . Consequently, we may read in some paper that « a calcareous Oxfordian lies over a Callovian essentially consisting in marls », i.e., a phrase that just makes no sense if you think of Oxfordian and Callovian as geological ages. More generally, several terminologies apply to the same geological entities as the result of translation problems, regional schools of thought, scientific evolution and many other causes. The identification of rigid properties of concepts can help in defining if two modeled concepts are the same, independent of the given names. When names are ambiguous for determining entity identities, instead of comparing the whole, one can decompose the entity in parts and try to find similarities between the entity parts (Fiorini and Abel 2014). In this approach, two entities are considered as being the same if they are described by the same set of attributes, if each of these attributes is instantiated to the same values and if the two entities each have the same relations with the same entities. For instance, a geologist who maps a definite region and observes in two different places two portions of geological unit, will look for the following conditions: (1) both portions are made of the same type of rock; (2) have similar fossil contents; (3) both overlay formations that look the same; and (4) they are both overlaid by formations that look the same. In these conditions, she/he will assume that she/ he has observed the same geological unit in the two places. However, two geologists who have different experiences such as a petrologist and a paleontologist for instance, may not pay attention or describe the same attributes. Decomposing entities into the proper attributes can be achieved when geologists know which attributes hold the identity of the geological unit and should consequently be examined.

In conclusion, we should consider that deciding that two entities are fully identical is not a trivial problem both when studying a geological terrain and in legacy models. In some cases, even if two models refer to the same entity, it may just not be possible to determine that it is so. Better ontological tools, however, can help the modeler in getting a better understanding of the community view and provide an approximation in creating integrable models. Referring to the UFO methodology exposed in section 2.3, we will show further in this paper that potentially more integrable models can be produced by applying to ontological notions of identity , rigidity , essentiality and unity (Guarino and Welty 2004; Guizzardi 2005).

Modeling directives to deal with view heterogeneity

We applied the concepts of foundational ontology to increase the semantic content of our representations. The multiplicity of the meta-types provided by UFO (Guarino and Welty 2004; Guizzardi et al. 2010) allows one to make explicit differences between types of classes that representational languages usually consider as being of same type. The UFO meta-types thus provide a conceptual tool for deciding which entities exist in the world reality. All geologists assume that rocks, reservoirs, traps and source rocks all are existing entities that have recognizable instances. However, under ontological analysis, this is not always true.

[FIGURE]

## Kinds and quantities

Let us consider the example of rocks . Although they have an objective existence, rocks have hardly individual instances, since the identity of a rock is defined by its internal petrological properties: chemical and mineral composition, texture, etc. We can assert that two arkoses deposited in different basins are the same if they have the same mineral compositions, textures and structures but we would certainly not assert that two instances of these arkoses are the same. A rock, in geological sense, does not represent a topologic whole. It needs to be individuated by a second entity that delimits its extent. A rock sample , a rock core or a rock unit have instances, but these are instances of the sample , core and unit concepts and not instances of the rock concept. Instances of rock are petrological concepts (uncountable entities) like grainstone , dolomite or shale . These instances correspond to a list of terms, like a rock-type catalog that can be accessed by the system. This brings a problem in conceptual modeling, since the metatype quantity , as defined in UFO, considers that instances of a rock are portions of rocks. However, in Geology, these portions have proper names: thin-section, core, sample, outcrop, etc., and these are ontological kinds . In our view, this approach does not capture the important ontological nature of a rock, which is defined by its intrinsic characteristics that transcend its portions. The modeling of this behavior is still an open issue in ontological analysis. In this work, we keep using the metatype quantity to classify the universals rock, petroleum and other concepts referring to substances, but this means that we are making flexible the definition of the UFO ' s author regarding the unity property.

## Rigid sortals and roles

In addition to the distinction that is made in UFO between kinds and quantities, an even more important distinction is introduced between rigid sortals (kinds and quantities) and roles . We can understand the distinction between a rigid sortal and a role through a common example in petroleum exploration illustrated by Fig. 8. Shales can be source rocks for hydrocarbons if they are delimited as a lithological unit, if they contain a significant amount of organic matter and if this organic matter was submitted to thermodynamic conditions

[FIGURE]

(pressure and temperature) that transformed it into kerogene and then into oil or gas. Later on, when the hydrocarbons have migrated upward, the considered shale unit is no longer a source rock but the rock is still there.

Any instance of a source rock is necessarily an instance of a lithological unit. However the UFO meta-types allow us to explicit the difference that exist between a rock unit , which is an entity that exists as a whole in the world, and a source rock unit, a reservoir or a seal , which are roles that an instance of a rock unit plays under some conditions. Another example related to mining geology concerns the term ore . A rock delimited by some geological body can play the role of an ore if its volume is large enough and if its grade in some valuable metallic minerals (lead, copper, zinc, tungsten or whatever) is high enough for justifying its mining with financial profit. In this case, the considered rock will play or not the role of an ore depending on the situation of the market. In UFO, roles are not represented as classes that can have instances that are not instances of a rigid sortal. The multiplicity of roles that rock units can play in geology (source rock, porous rock, reservoir, seal) are represented in our conceptual model as additional attributes for the actual entities that have a concrete existence, i.e., the rigid sortals (kinds and quantities). This directive is critical to guarantee model integration since rigid sortals are those that are effectively found in all geological models even under different representations.

## Subsumption relationships

Another important ontological notion is the subsumption relationship ( subclass or is-a relationships), which formally means that all instances of a subclass are necessarily instances of the superclass. Subsumption is an important relation used to structure the invariant aspects of the domain in the backbone taxonomy of an ontology. Each subclass in a taxonomy must hold the same identity criteria as its superclass. Each instance in the domain should instantiate one and only one concept in the taxonomy that supplies the identity criteria to the instance.

In many models, the subsumption relationships are often misused, when one simply transfers to the model some language usages. Although it sounds correct saying that a seal is a rock , the ontological meaning is that a seal is a rock unit made of rock . The made-of relationship between a rock unit and a rock must be defined as a part-of relation not as a subclass.

A typical example of possible consequence of the misuse of the subsumption relationship would be to answer yes to the question: « Is a cross stratification a sedimentary facies? ». Sedimentary facies is ontologically defined by Lorenzatti (Lorenzatti et al. 2011) as a complex entity that includes the depositional and post depositional structures, the lithology, and the fossil content. According to the definition of (Carbonera et al. 2015), sedimentary structure is an inseparable part of a facies. However the identity of a sedimentary structure such as a cross stratification is only related to the spatial arrangement of the grains, while the facies is defined by depositional, post depositional structures, lithology and fossil content. Consequently, the concept facies cannot subsume the concept sedimentary structure . A sedimentary structure indeed, is a component (part) of a sedimentary facies.

Fig. 8 The schematic illustration of the elements of petroleum system (Feijó 2010)

[FIGURE]

The misuse of subclass and part-of relations are mostly a consequence of the lack of understanding of the ontological properties of the entities. Consequently, models currently operate some approximation by using the subclass relationship. Acommonexample of this misuse of subsumption consists in representing a disjunction of classes for introducing a type restriction (Guarino and Welty 2002). Let us consider for instance the Petroleum system , which will be object of the use case exposed in the next section of this paper and which is pictured in Fig. 8. To define the conditions in which all the components of a petroleum system are present, we could create an artificial entity PetroleumSystemPart (meaning that it is a concept that cannot be associated to some instance or raw data). This entity would subsume and relate to the Petroleum System all the entities that are required to be part of this system. However, when doing so, we would state that the identity of an entity that is a PetroleumSystemPart , is given by the fact that this entity is part of a petroleum system . However, this is not the case. The identity of a seal is given by a unit of rock and the identity of a rock structure is the result of a rock transformation. In order for these entities to exist, it is not essential for them being part of a petroleum system. Therefore, they cannot inherit the identity of the super class PetroleumSystemPart.

Another example of misuse of a subsumption relationship is using the is-a relation as a substitute for the is-constituted-of relationship. Is it right stating for instance that an ocean is a sub-class of water or that a stromatolit is a subclass of rock ? The answer is no in both examples, since the identity criteria of ocean (size, location) are different from those of water (chemical composition), and since the identity criterion of stromatolite is being an accretionary structure of grains, while the identity criteria of rock are a definite mineral composition and a definite texture. These notions can be extended through the study of the work of Guarino and colleagues in the cited references and many others not mentioned here.

## The Petroleum system case study

As a case study, we will introduce here the conceptual model of the petroleum system defined in (Magoon and Dow 1994). The model is an abstraction, which specifies the main conditions requested for a prospect to become a hydrocarbon reservoir. Our intention has not been to provide a complete and detailed version of the model, but rather to emphasize important aspects of the modeling process. We have been specially attached to identifying the concepts that represent real instances in the raw data and that can be mapped from one model to another. This special case study is interesting in the context of information integration because the concepts on which it rests, must match with different geological models in reference and with the variety of data captured in the prospected geological region. This case study involves sequences of events and spatial relationships that are not trivially modeled by the geo-modelers currently used by geoscientists.

## Description of the petroleum system

For characterizing the petroleum system case study, we can start from the textual description provided by (Magoon and Dow 1994) and shown in Fig. 9. This description is complemented by the schematic diagram of the petroleum system that we already presented in Fig. 8.

## Ontological analysis of the case study

The main keywords of the case are those described in Fig. 8 and listed in Table 1, in the order in which they appear in the text. We will analyze each of the terms identified in the text considering its ontological nature characterized by the metaproperties of existential dependence, identity, unity, rigidity, inseparable part and relational dependence.

[FIGURE]

Fig. 9 Textual description of the Petroleum System, according with (Magoon and Dow 1994), considered for ontological analysis

In Table 1, these meta-properties are signaled in the following way:

- -ED+/ ED-: existentially dependent / independent,
- -I+ / I-: carrying / not carrying an identity criterion,
- -O+/ O-: property providing / not providing its own identity criterion
- -U+/ U-: carrying / not carrying a common unity criterion,
- -P+ / P-: being / not being an inseparable part of another entity,

Table 1 Ontological analysis of the terms, according to foundational ontology, describing the recognizable concepts to be modeled for the ' Petroleum System '

| Concept                  | Identity   | Unity   | Rigidity   | Existential dependence   | Relational dependence   | Inseparable part   | Ontological category   |
|--------------------------|------------|---------|------------|--------------------------|-------------------------|--------------------|------------------------|
| Petroleum                | O+ I+      | U -     | R+         | ED -                     | RD -                    | P -                | Quantity               |
| Transformation           | O+ I+      | U -     | R+         | ED+                      | RD -                    | P -                | Event                  |
| Organic matter           | O+ I+      | U -     | R+         | ED -                     | RD -                    | P -                | Quantity               |
| Rock                     | O+ I+      | U -     | R+         | ED -                     | RD -                    | P -                | Quantity               |
| Argillaceous substrate   | O - I -    | U -     | R+         | ED -                     | RD -                    | P -                | Category               |
| Shale                    | O+ I+      | U -     | R+         | ED -                     | RD -                    | P -                | Quantity               |
| Pressure                 | O+ I+      | U -     | R+         | ED+                      | RD -                    | P -                | Quality                |
| Temperature              | O+ I+      | U -     | R+         | ED+                      | RD -                    | P -                | Quality                |
| Oil                      | O+ I+      | U -     | R+         | ED -                     | RD -                    | P -                | Quantity               |
| Gas                      | O+ I+      | U-      | R+         | ED -                     | RD -                    | P -                | Quantity               |
| Source Rock              | O - I+     | U -     | R~         | ED -                     | RD+                     | P -                | Role                   |
| Migration                | O+I+       | U -     | R+         | ED+                      | RD -                    | P -                | Event                  |
| Transport                | O+I+       | U -     | R+         | ED+                      | RD -                    | P -                | Event                  |
| Hydrocarbon              | O+ I+      | U -     | R+         | ED -                     | RD -                    | P -                | Quantity               |
| Reservoir rock           | O - I+     | U -     | R~         | ED -                     | RD+                     | P -                | Role                   |
| Millions of years        | O+ I+      | U -     | R+         | ED -                     | RD -                    | P -                | Quale                  |
| Volume                   | O+ I+      | U -     | R+         | ED+                      | RD -                    | P -                | Quality                |
| Pore                     | O+ I+      | U+      | R+         | ED+                      | RD -                    | P+                 | Kind                   |
| Porous rock              | O - I -    | U-      | R-         | ED -                     | RD-                     | P -                | Mixin                  |
| Permeable rock           | O - I -    | U -     | R-         | ED -                     | RD -                    | P -                | Mixin                  |
| Water                    | O+ I+      | U -     | R+         | ED -                     | RD -                    | P -                | Quantity               |
| Impermeable rock         | O - I -    | U -     | R-         | ED -                     | RD -                    | P -                | Mixin                  |
| Seal                     | O - I+     | U -     | R~         | ED -                     | RD+                     | P -                | Role                   |
| Trap                     | O - I -    | U+      | R-         | ED -                     | RD -                    | P -                | Mixin                  |
| Upward vertical movement | O+I+       | U -     | R+         | ED+                      | RD -                    | P -                | Event                  |
| Rise                     | O+I+       | U -     | R+         | ED+                      | RD -                    | P -                | Event                  |
| Primary migration        | O+I+       | U -     | R+         | ED+                      | RD -                    | P -                | Event                  |
| Secondary migration      | O+I+       | U -     | R+         | ED+                      | RD -                    | P -                | Event                  |

[FIGURE]

[FIGURE]

Fig. 10 The conceptual model of the petroleum system according to the ontological analysis

[FIGURE]

- -R+/ R- / R~: being rigid / non rigid /anti-rigid
- -RD+/ RD-: relationally dependent / independent,
- -Petroleum has its own identity but no unity. We can individuate its instances by stating, for example, that one petroleum is different from another, because of its composition, but we cannot count its instances if they are not individuated by a container. Consequently, the concept has its own identity, but has no unity. Other entities must be present in order for an instance of petroleum to exist. The same analysis and characterization can be applied for Hydrocarbon , Organic matter and Water . In this context, the terms Petroleum and Hydrocarbon terms seem to be synonyms. We consider that the use of different names is an indication of different concepts, but this difference was not defined at the time when this model was built. Consequently, we will only adopt the term Hydrocarbon in the model until new properties may allow us differentiating Petroleum from Hydrocarbon .
- -Transformation is an event, then a perdurant. Each perdurant has existential dependence with respect to an instance that preserves its identity but has no proper ontological identity. In order to define a transformation, which is the entity that it transforms. The same classification applies to Migration , Transport and Upward vertical movement . Events can hold their own properties, such as the qualities Primary and Secondary applied to Migration in our case study.
- -Rock has identity but no unity, since it needs to be framed by another entity in order to be counted, as it was discussed in section 2.
- -Argillaceous substrate gets its identity from the material that contains clay since there are no instances of argillaceous substrate that are not instances of a rock or of some other material in the subsurface. Regarding this property, some instances of a rock play the role of being argillaceous, but differently of being a source rock, since these instances cannot stop being argillaceous. This defines the ontological type of a Category in UFO-A, which can hold or not unity, according to the ontological properties of the instances being categorized. The decision of including categories in a conceptual model depends on the intended use of the model. Categories can help considering as a group, a set of entities of different kinds, i.e., in including, for instance, a specific attribute of value to gemstone materials. Otherwise, properties can be modeled as qualities and treated by the applications. We will include here the class Siliciclastic rock to associate all the properties that apply to this kind of rock, but not to other classes of compositional rocks.

[FIGURE]

-

- In such case, the quantity Siliciclastic Rock could hold a property amount of argilaceous material . Shale inherits its ontological identity from Rock, which subsumes all the types of rocks, building thus a taxonomical relationship. This means that this concept also has not unity. We will include here the disjoint class Sandstone (while omitting other disjoint subclasses not needed for this model) as a subtype of Siliciclastic rock .
- -Pressure is a property of some physical entity and it is thus existentially dependent on that entity. It is not possible to count or individuate instances of pressure. The same analysis is applied to Temperature and Volume .
- -Oil and Gas are subtypes of Hydrocarbon and inherit its ontological properties, such as being uncountable.
- -Source rock requires a careful analysis. On the contrary, to what the language suggests, it is not a subtype of Rock , since it is possible to individuate a source rock and to count it. When we state that there are two source rocks in a prospect, we mean that there are two rock units that produce oil and not two different rocks, to which a source rock has existential dependence. Being a source rock is a role played by some rock units under specific conditions. In order to have this concept in our model, it is necessary to include a rigid type -Lithological unit - that guarantees the identity of the instances of source rock. The same classification is applied to Reservoir rock and Seal .
- -Pore is a rigid sortal of an inseparable part of a rock. It has ontological identity, holds unity and owns properties, even if it is not constituted by matter.
- -Porous rock is a rock that has part of its volume constituted by empty spaces, or pores. Since it is not a rigid concept and is dependent of a rock, we suggest modeling Porosity as a quality of Rock and omit the sortal Porous rock in the model. The same analysis applies to the terms Permeable rock and Impermeable rock , which respectively designate the quality of a rock which have a high or a low permeability, i.e., through which fluid can or cannot percolate.
- -Upward vertical movement has no ontological identity; it applies to the entity that suffers the movement. It is a perdurant and it can be categorized as an event. In this case, it is a synonym of Rise , and only one term should be kept in the model.
- -Trap is a complex entity that is built by the aggregation of a Seal and a Reservoir rock , which are both anti-rigid concepts that define different roles for lithological units. It defines semi-rigid properties for some instances of Lithological units when they play the roles of Reservoir and Seal .

For simplicity, we have not discussed here several other conceptualizations expressed in the Petroleum System case, such as the formal relation between the volume of petroleum and the empty volume of the rock, expressed by the term bigger volume in the text. We have omitted also discussing the several types of parthood relations, such has a pore being part of a rock or a seal being part of a trap.

## Modeling of the petroleum system

The result of our analysis produced the model expressed in the ONTOUML 4 notation in the diagram of Fig. 10. The model applies the meta-types of UFO-A and UFO-B that hold to the examined properties.

Our approach suggests that the essential concepts to be modeled are the rigid concepts that instantiate to Kinds and Quantities (depicted in the model by thick boxes). These entities can be requested by applications to play specific roles and this can be expressed in the model. However, the model clearly expresses that only Kinds and Quantities will have instances and can be associated to the raw data in order to be further mapped to other applications.

Regarding the framework of relations among the concepts, the main relations are subsumptions - represented by arcs ended by triangles in the side of the superclasses -. They organize the concepts, guarantee the intention of the modeler and fully support attribute inheritance to subclasses and instances.

The second more important relation is the parthood relationship, represented in the diagram as arcs with diamonds in the end. In this diagram, we did not specialize the several kinds of part of relations, as it was supported by UFO-A. Parthood relations are of extreme importance for modeling organization and geological reasoning.

Wehave also provided a high-level model for the perdurants in this domain, represented by events, framed in time and dependent on the participation of kinds and quantities. We express the situations that need to be found in order for some event to occur. Our model expresses, for instance, that in order for the event Generation to happen, it is requested that there exists a situation, called Pre-generation in the model, in which pressure increases while temperature stays between 25 and 125° Celsius and in which an instance of a source rock having a high content of organic matter is present. Moreover, the model expresses that it is necessary that some lithological units participate in each of the identified situation, so that the successive event can occur.

For a question of space and simplicity, we have omitted here the detailed description of relations, qualities and quality structures, although we assume that they are necessary to fully express the semantics of the model. Instead, we focused our attention in emphasizing how to select entities in the domain in order to build interoperable models. The resulting model intends to illustrate these choices.

4 code.google.com/p/ontouml/

## Discussion and Conclusion

We have presented in this paper a study that discusses how to deal with information heterogeneity and interoperability among systems to be applied to process geological information. We analyzed the semantic heterogeneity that can affect the interoperability of geological software applications, showing that, out of interpretation heterogeneity, most of data integration is limited by modeling practices that produce poor models.

Our claim is that interoperability among earth models built and manipulated by different professionals and systems, can be achieved by making apparent the intended meaning of the geological entities represented in the models. We showed that few ontological properties inhered to concepts - identity, rigidity, essentiality and unity -are enough to clarify the meaning of the modeled entities and to define the similarities and identities between models and data. These properties elucidate which are the concepts that are essential to the modeled reality and can be used for providing a unified view over this reality. In addition, the understanding of the modeling principles can lead to clean the future models of the entities that have no proper existence in reality (i.e., that have no instances). This allows modelers to develop naturally integrable models based on a common framework of essential rigid concepts.

In order to help the understanding of our approach, we have performed an ontological analysis and developed a conceptual model for a petroleum system, based on the original description of Magoon and Wallace. We did not discuss here some important primitives of modeling, such as, the representation of domains of attributes and their possible values, and their dimensionality. We also omitted the modeling of formal and material relations in our case study, avoiding extending a complex discussion in a single paper. In addition, we need to expand our understanding of the role of parthood relationship in supporting geological knowledge, in order to provide a proper contribution in geological modeling. These topics will the focus of future studies in the geological domain.

New technologies based on semantic issues are presently being developed by the Energistic Consortium, 5 a global community devoted to the development and promotion of data exchange standards for the petroleum industry. Energistics has proposed and still enhances standards for drilling (WITSML), production (PRODML) and reservoir (RESQML), which tend to become largely accepted by the petroleum community. A review about the semantics of these standards is available in (Werlang et al. 2013).

[5 www.energistics.org](http://www.energistics.org/)

[FIGURE]

Acknowledgments We gratefully thank GEOSIRIS; Brazilian Research Council, CNPq; PRH PB-17 program (supported by PETROBRAS); and ENDEEPER Co. for the support to this work.

## References

- Carbonera JL, Abel M, Scherer CMS (2015) Visual interpretation of events in petroleum exploration: an approach supported by wellfounded ontologies. Expert Systems with applications 42:2749 -2763
- Chum F (2007) Use case: ontology-driven information integration and delivery - a survey of semantic web technology in the oil and gas industry
- Cosentino L (2001) Integrated reservoir studies. Technip, Paris
- Fanchi JR (2005) Principles of applied reservoir simulation. Elsevier
- Feijó FJ (2010) Basics of petroleum geology (In portugues: Noções Básicas de Geologia de Petróleo). Petrobras University, Rio de Janeiro
- Fiorini SR, Abel M, Carbonera JL (2015) Representation of part-whole similarity in Geology. Earth Science Informatics (Print), Springer
- Fitting M, Mendelsohn RL (1998) First-order modal logic. Studies in epistemology logic, methodology, and philosophy of science, vol 277. Kluwer Academic Publishers
- Gärdenfors P (2000) Conceptual spaces: the geometry of thought. MIT Press, Cambridge
- Gruber TR (2003) Ontology progress -what is an ontology. Softw World 34:6
- Guarino N (1994) In: Casati R, Smith B, White G (eds) The ontological level. Philosophy and the Cognitive Science Hölder-PichlerTempsky, Vienna, pp 443 -456
- Guarino N (1995) Formal ontology, conceptual analysis and knowledge representation. Int J Hum Comput Stud 43:625 -640
- Guarino N (1998) Formal ontology in information systems paper presented at the formal ontology in information systems. FOIS ' 98, Trento
- Guarino N, Welty C (2002) Evaluating ontological Decisions with Ontoclean. Commun ACM 45:61 -65
- Guarino N, Welty C (2001) Identity and Subsumption. In: Green R, Bean CA, Myaeng SH (eds) The semantics of relationships. An interdisciplinary perspective. Information science and knowledge management, vol 3. Springer, Netherlands, pp 111 -126. doi:10.1007/97894-017-0073-3\_7
- Guarino N, Welty CA (2004) An overview of OntoClean. In: Staab S, Studer R (eds) Handbook of Ontologies. International handbook on information systems. Springer, Berlin, pp p 151 -171
- Guizzardi G (2005) Ontological foundations for structural conceptual models vol 05 -74. CTIT PhD Thesis Series. Universal Press, Enschede, The Netherlands
- Guizzardi G, Baiao F, Lopes M, Falbo RA (2010) The role of foundational ontologies for domain ontology engineering. Int J Inf Syst Model Des 1:22
- Lorenzatti A, Abel M, Fiorini SR, Bernardes A, Scherer CMS (2011) Ontological primitives for visual knowledge. In: Costa ACR, Vicari R, Tonidandel F (eds) Lecture notes in artificial intelligence, vol 6404. São Bernardo do Campo: Springer Berlin / Heidelberg, pp 1 -10
- Ludäscher B, Lin K, Bowers S, Jaeger-Frank E, Brodaric B, Baru C (2006) Managing scientific data: from data integration to scientific workflows. Geological survey of America special paper 397
- Magoon LB, Dow WG (1994) The petroleum system. In: Magoon LB, Dow WG (eds) The petroleum system: from source to trap, vol 60. AAPG Memoir. AAPG, Tulsa, pp 3 -24
- Perrin M, Rainaud J-F, Mastella LS, Abel M (2007) Knowledge related challenges for efficient Data fusion. Paper presented at the Data fusion: combining geological, geophysical and engineering data, SEG/AAPG/SPE Joint Workshop, Vancouver, October 14 -18
- Perrin M, Abel M (2013) Earth models as subsurface representations. In: Perrin M, Rainaud J-F (eds) Knowledge driven earth modelling. Editions Technip, Paris, pp 3 -24
- Werlang R, Abel M, Perrin M, Carbonera JL, Fiorini SR (2013) Ontological foundations for petroleum application modeling. Paper presented at the The Petroleum Network Education Conference, Houston
- Zimmerman D (1996) Persistence and Presentism Philosophical Papers 25 115 -126

[FIGURE]
