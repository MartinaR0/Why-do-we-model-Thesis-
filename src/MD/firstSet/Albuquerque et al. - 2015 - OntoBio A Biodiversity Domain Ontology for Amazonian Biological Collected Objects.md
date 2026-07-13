## OntoBio: A Biodiversity Domain Ontology for Amazonian Biological Collected Objects

Andréa C. F. Albuquerque Federal University of Amazonas andreaalb.1993@gmail.com

## Abstract

The use of ontology presents a novel data integration resource, when centred in semantic definitions  and  the  need  for  interoperability.  Results from previews works indicate that ontologies can drive knowledge  acquisition  processes  for  the  purpose  of comprehensive,  transportable  machine  understanding and knowledge management. Applied to the biodiversity  domain,  ontologies  can  be  a  valuable resource  for  strategic  planning  and  its  contribution toward conservation of the Amazon region. This work presents  a  biodiversity  domain  ontology  developed  at the National Institute for Amazonian Research (INPA) using biological data as its object of study.

## 1. Introduction

Nowadays, research in biodiversity involves interdisciplinary  complex  systems,  which  are  part  of the  understanding  of  the  systems  science  domain. Dealing with such complex areas, constitutes opportunities and a way to propitiate the development of  new  foundations that are applicable in a  variety of fields  such  as  scientific  data  modeling,  knowledge representation and management, including formal ontology that can guarantee semantic expressiveness.

The  definition  of  ontology  in  the  Computer  and Information  Science  context  is  not  yet  consolidated, however,  it  has  undergone  improvements  due  to  the heightened interest of a growing number of researchers.  Ontologies  have  already  been  applied  in various fields such as Artificial Intelligence (AI), Software  Engineering  and  Semantic  Web,  within  the perspective  of  the  system  science  methodologies  to address complex problems. These ontologies enable, or try  to  enable,  the  creation  of  straightforward,  concise and unambiguous conceptual models. Ontologies generally refer to a specification of a conceptualization.

'An ontology is a formal and explicit specification of a shared conceptualization'.

José L. Campos dos Santos National Institute for Amazon Research lcampos@inpa.gov.br Alberto N. de Castro Júnior Federal University of Amazonas alberto@icomp.ufam.edu.br

In  this  definition,  "formal"  means  readable  by computers; "explicit  specification"  refers  to  concepts, attributes,  relationships,  constraints,  and  axioms  that are explicitly defined; "shared means consensual knowledge; and "conceptualization" refers to an abstract model of some real-world phenomenon [1].

Even without a consensus of its definition, ontologies share common characteristics and drive the development of several works related to methodologies, tools, languages and applications.

Ontologies have emerged as tools for representing, organizing and sharing knowledge in a given domain, allowing  several  areas  of  application  to  use  them  for managing knowledge.

The  process  of  ontology  development  research involves  collaboration  between  ontology  researchers and  researchers  in  specific  fields  that  use  ontologies, this  is  especially  evident  in  biology  and  its  related areas.  Bio-ontologies,  ontologies  related  to  biology and life sciences, have helped and contributed to major advances in these areas, they allow the association of meaning  to  the  data  generated  in  experiments,  and enable the integration of various sources of knowledge,  new  approaches  for  the  preparation  of experiments  or  searching  for  answers  using  results from different sources [2].

Biodiversity  research  is  an  interdisciplinary  field that  requires  the  cooperation  of  various  researchers. Biologists, medical scientists, chemists, physicists, geographers, geologists, geneticists, meteorologists and researchers involved in biodiversity research perform different types of activities such as collecting samples and or specimens, analysing data, and collecting  geographical  information.  Researchers  also analyse correlations with other living beings, building models  that  describe  these  interactions  in  different scenarios.  The  available  data  have  been  collected  in various  parts  of  the  world  and  published  in  different formats  and  specified  in  many  data  standards.  This scenario is characterized by its intrinsic heterogeneity not just the data and conceptual models used, but also the  needs  and  profiles  of  the  specialists  who  collect and analyse the data.

Many issues in biology have their domain described by consensual ontologies (reflecting consensual knowledge accepted by a group or community),  such  as  Gene  Ontology  in  genetics  [3] and TAMBIS (Transparent Access to Multiple Bioinformatics Information Sources) Ontology in molecular  biology  [4]. In the  biodiversity  domain however, there is still no consensus ontology, although there  are  several  experts  involved  in  multinational initiatives  such  as  Global  Biodiversity  Information Facility  (GBIF),  Cable  News  Network  (CNN)  and Biodiversity Information Standards (TDWG).

[FIGURE]

Due to the wide-ranging characteristics of data and the diverse profiles of experts, there is still much work to  be  done  in  the  specification  of  ontology  for  this domain. This is one of the reasons that the integration of biodiversity data and ecological studies is not considered  trivial.  Solutions  for  interoperability  are needed  for  research  in  this  field.  Even  the  taxonomic classifications of species are debated among researchers. Some taxonomic trees are clearly defined such as mammals within zoology. However, there are still  differences between authors in various fields, and many  species  to  be  classified  or  reclassified  -  like insects, for example.  Similar  problems  also  affect species habitat descriptions, such as differing classifications  of  soil  in  the  world.  In  Brazil,  two systems  of  soil  classification  are  considered  official. Thus, one sample of soil may be represented not only by different names and identifiers, but also as belonging to classes of distinct ontologies.

This paper presents OntoBio, a biodiversity ontology  developed  in  a  research  initiative  involving the Institute of Computing at the Federal University of Amazonas and INPA's Biological Collection Program. It is organized as follows: Section 2 provides information  about  the  methods  used  to  develop  the ontology (a brief description of the biodiversity domain, requirements elicitation, the ontological engineering  approach,  and  the  biodiversity  ontology and  its  sub-ontologies);  and  Section  3  concludes  this work.

## 2. Methods

## 2.1. Requirements Elicitation

The requirements elicitation in the context of biodiversity  data  was  developed  following  some  of INPA's Biological Collection Program protocols steps for collecting objects:

i.  Collected  Sample/Specimen  Data  (CSD)  consist of collected records and or documents from fieldwork. Data  were  collected  from  projects,  organizations  and institutes, available on the Web, and at INPA, resulting in electronic documents (mostly text files) and information  about  the  conceptual  schema  database based on CLOSi (Clustered Object Schema for INPA)

- [5]. The research at INPA permitted an in-depth study of  biodiversity  domain  data.  It  would  not  have  been possible  to  build  this  ontology  without  personal,  onsite  experience,  and  the  expertise  of  collaborators  at INPA, since this domain requires specialized knowledge of the context;

ii.  Requirements  Elicitation,  based  on  CSD.  The common  aspects  of  most  documents  acquired  for modelling the ontology were highlighted. At this stage, a generic document was defined for recording fieldwork data.

These  two  steps  demonstrated  that  the  domain application is complex and large with regard to taxonomy, morphological and morphometric analysis.

There was a wide variety of nomenclatures/classifications of a given species. Interestingly,  botanists  and  zoologists  have  different ways  of  recording  species.  It  should  be  noted  that thousands  of  species  can  now  be  found  in  museum records  and  research  institutes,  and  new  species  are discovered daily.

## · INPA's Biological Collection Program Protocol

Below is a brief description of INPA's Biological Collection Program Protocol, defining the requirements  of  an  application  in the biodiversity domain. It guides the ontology development.

Biodiversity studies use samples as material evidence for identification, collections and future studies.  They  allow  for  the  manipulation  of  data  that can  be  used  for  other  analysis  such  as  geographical distribution;  biogeography;  distribution  patterns  and potential  ecological  niches;  and  descriptions  of  new species, among others. Obtained from collected samples,  this  information  can  be  applied  across  the breadth of the domain area, allowing access to all its biological diversity.

Field  collection  aims  to  acquire  and  record  any biological material sampled. During  collection, in addition to the biological material of interest, geographic  information  on  the  specimen  or  sample's collection site, the physical characteristics of the location, as well as, information regarding the material collected  is  essential.  The  data  to  be  collected  will generally include body size (e.g. height, weight, width, length), morphometry or dimensions of the body (e.g. head-body, head, tail, legs, wings, beak, scales, antennae), and developmental stage (e.g. puppy, young,  adult, larva, nymph,  button,  flower,  fruit). Popular and scientific names can also be recorded, and specifically  for  flora,  the  popular  uses  of  the  plant  in question. In addition, time of collection, moon phase, temperature,  weather  quality,  environment  (e.g.  land, air,  water),  salinity,  environment  conductivity,  light, substrate and vegetation type, are important for guiding future analysis and comparisons made  with other studies.

In the field,  collected  plants  are  properly  preidentified.  After  harvesting,  the  pre-sorted  material  is then identified. The same procedure applies for animals. In many cases, it is necessary to remove a part of the animal, for example, the skull, or the claws of a paw, and to use a magnifying glass for proper identification.

## · Analysis and Data Treatment

Ontology modelling for biodiversity data can make use of the domain of a database application as the basis for the graphical representation and the rules of zoological and botanical nomenclature to compose part of the vocabulary.

Ontologies  based  on  conceptual  data  schemas  are more  easily  defined,  especially  when  the  application domain tends to be large and complex (the data schema tends  to  play  the  role  of  the  domain  expert).  It  is possible to add  descriptions of the constants  and contexts,  as  well  as  members  of  a  class,  making  it possible to cover a large number of objects.

The  application  used  in  this  research  consists  of procedures  for  fieldwork  collection  of biodiversity data.

The  design  of  a  database  for  managing  fieldwork collection  data,  biological  collections  or  biodiversity data requires the understanding of each of these activities.  It  also  requires  knowledge  of  the  data  and their characteristics. To do so, users should be involved in the process of identifying data requirements and the system, especially during requirements analysis of data.

At  INPA,  this  phase  was  guided  by  documents, interviews  with researchers, and researcher evaluation of specimen, and or, sample descriptions. Each participant in the process was an expert in a taxonomic group or in a biological aspect of a taxonomic group. The  interviews  had  an  open  format  and  the  same general questions were asked to each researcher. Information was also acquired from literature and web searches.

Conceptually,  it  can  be  said  that  institutions  have biological  collections  and  these  in  turn  are  composed of  objects  collected  in  a  given  location  with  their specific  taxonomy;  the  classification  of  each  object, when determined, is referenced in scientific papers.

The  data collected during fieldwork to record species, are divided into two types: general, information  that  is  normally  collected  in  all  studies (e.g.  day,  hour,  description  of  location),  and  specific, that correspond to the scientific interest of a study (for example, altitude of a location or the moon phase may be  of interest to  one  study  but  not  for  another). Interviewing scientists working in different studies, in different areas, helps to differentiate between information  that  is  common  to  all  and  information used  only  by  a  few  scientists.  The  results  of  the interviews along with other collected data were separated by functions and grouped as type of objects [5].

In 2003, Campos dos Santos presented a conceptual framework for representing INPA's biological  collections  called  CLOSi,  constituting  a basis for an integrated view  of these data collections. CLOSi is the result of studies in scientific institutions of the Amazon:  INPA,  the  Brazilian Agricultural Research  Corporation  (EMBRAPA),  the  Institute  for Scientific and Technological Research of the State of Amapá (IEPA), the Goeldi Museum (MPEG) and the Laboratory of Silviculture (Silvolab) in French Guiana. This ontology is based on CLOSi and INPA's CSD.

The  use  of  data  schemas  helps  the  process  of ontology development. Ontology development uses an already conceived conceptualization of domain application  to  design  a  new  conceptualization  with different levels of detail.

## 2.2. The Ontological Engineering Approach

Despite  various  attempts  to  create  methodologies for  developing  ontologies,  practice  shows  that  most research groups create their own method of development, depending on the application characteristics that must be developed using the ontology.

Based  on  the  various  methods  used  for  building ontologies, Falbo et al . propose a systematic approach for building domain ontologies called Systematic Approach  for  Building  Ontologies  (SABIO);  it  is adopted within this research [6].

SABIO  prescribes  an  iterative  process  comprised of the following activities: (i) the identification of the ontology purpose by means of competence questions; (ii)  the  capture  of  concepts  existing  in  the  domain  as well as its relations and its properties; (iii) the ontology  formalization, which  is the definition of formal axioms by using First-Order Logic (FOL); (iv) the search for existing  ontologies with  reuse  and integration in mind; (v) the evaluation of the ontology to  identify  inconsistencies  as  well  as  to  verify  the truthfulness  with  the  ontology  purpose;  (vi)  ontology documentation.  The  competence  questions  are  the questions  the  ontology  is  supposed  to  answer.  It  is important to highlight that competence questions play a prominent role in this methodology by: (1) defining the scope and purpose of the domain conceptualization being developed; (2) serving as a testbed for ontology evaluation.

Ontology  engineering  should  include  phases  of conceptual modelling, design and  codification [7]. These phases, in turn, shall produce different artefacts with  different  objectives  and,  consequently,  require different  types  of  modelling  languages  and  methods with specific characteristics. In the conceptual modelling phase, the ontology should strive for expressivity, clarity and truthfulness in representing the subject  domain  at  hand.  The  same  conceptual  model can then give rise to different ontology codifications in different  languages  in  order  to  satisfy  different  nonfunctional requirements (e.g. computational tractability,  decidability).  Guizzardi  demonstrates  that semantic  web  languages  such  as  OWL  and  RDF  are codification  languages  and  fall  short  in  serving  as  a language for the phase of ontology conceptual modelling [7].

The steps in the process of developing an ontology and their interdependencies are illustrated in Figure 1. Dashed lines indicate the existence of a constant (but weak) interaction, between associated steps. Solid lines indicate  the  main  flow  of  work  in  the  process  of building ontology. The bold line surrounding the steps of  ontology  capture  and  formalization  enhances  the strong interaction and thus iteration that occurs between these steps.

Figure 1. Ontology development steps and their interdependencies (adapted from [6]).

[FIGURE]

Once  a  formal  ontology  is  obtained  it  needs  to become  operational.  To  do  so,  two  other  activities should be undertaken: design and coding. In the project,  the  concepts,  relations  and  axioms  of  the formal  ontology  should  be  placed  in  a  compatible format with the implementation language. During codification,  the  ontology  is  encoded  in  the  chosen language.

In  order  to  represent  the  biodiversity  ontology  we have  used  Onto  UML,  an  ontologically  well-founded UML modelling profile [7]. This profile is comprised of a number  of  stereotyped classes and relations creating  a  metamodel  that  reflects  the  structure  and axiomatization of a foundational (domain independent) ontology named UFO (Unified Foundation Ontology) [7].  Based on this approach, OntoBio is comprised of: i)  structural  conceptual  models,  (ii)  FOL  axioms  and (iii)  a  dictionary  of  terms.  The  sections  2.4  and  2.5 present  (i)  and  (ii);  for  brevity,  however,  we  do  not present (iii) in this paper.

## 2.3. Tools for Development

For the implementation of the biodiversity ontology, Protégé ontology editor was used.

Protégé is an open source, free editor and framework for acquiring knowledge. One of the main features of this tool is to support two  forms  of implementation and modelling of ontologies: one based on frames and the other, which was used in this work, based on Ontology Web Language (OWL).

To extend the functionality of Protégé two plugins were used: Racer Pro e o Jess .

The inference engine Racer Pro ,  version 1.9.0 for Linux 32 bit, is a plugin that checks the consistency of the  ontology,  it  checks  for  any  contradictions  in  the logical  conditions  declared  for  the  classes,  and  an inference sub junction checks if a class is contained in another. It also carries out a classification of individuals, to establish which class or classes individuals belong to, given the conditions and known information about them. The inferences in the ontology are performed using this plugin.

Jess ,  version  7.0  for  Linux  32  bit  is  a  plugin  that allows  inferences  to  be  made  about  Semantic  Web Rule Language  (SWRL)  for  rules to answer the competence questions.

The  biodiversity  ontology  was  developed  using ontology engineering. As in software engineering, we present  an  initial  overview  analysis  (ontology  as  a conceptual  model  -  OntoUML  [7]  and  subsequently adopt the ontology as implementation languages (OWL/OWL2).

OntoUML  is  a  model-based  graphical  editor  for supporting  the  creation  of  conceptual  models  and domain ontologies in a philosophically and cognitively well-founded  modelling  language  named  OntoUML. The Editor is designed in a way that it shields the user from  the complexity  of  the ontological principles underlying this language. At the same time, it reinforces these principles in the produced models by providing a mechanism for automatic formal constraint verification [8].

## 2.4. Competence Questions (CQs)

The main purpose of this ontology is to provide a clear and precise conceptualization of the issues raised in  CSD,  independent  of  a  specific  application.  The CQs tend to reflect this purpose and the expected uses for it, that is, the ontology competence. The competence  of  a  representation  is  about  the  coverage of  issues  that  this  representation  can  answer  or  tasks that it can support; it delimits the scope of the ontology developed.  When  establishing  competence,  what  is relevant to the ontology and what is not are defined. It is also helpful  to identify potential  users  and  the scenarios that motivated the development of the ontology in question. CQs are answered using FOL and SWRL 1 , which validate the design of the ontology. The implementation is open to use and reusable on a global scale.  It  is  available  with  sub-ontology  schemas  at http://lis.inpa.gov.br/biodiversityontology/.

- CQs defined for this ontology are listed below:
- CQ1. Which  institution is responsible for the collected specimen?
- CQ2.  What  is  the  type  of  collection:  manual  or instrumented?
- CQ3. What are the species of the collected objects?
- CQ4. Who is responsible for the collected sample/specimen?
- CQ5. Who classifies the collected object?
- CQ6. Who participates in collecting the object?
- CQ7. Who assists in collecting the object?
- CQ8.  What  is  the  taxonomic  classification  of  the collected object?
- CQ9.  What  is  the  popular  name  of  the  collected object?
- CQ10.  What  is  the  life  stage  of  the  collected object?
- CQ11. What is the average weight of the collected objects in a given region to a certain taxon?
- CQ12. What is the vegetation found in the collected sample/specimen site?
- CQ13. What is the biome of the collection site?
- CQ14. What is the geographic region of the collection site?
- CQ15. What is the phitophisiognomy of the collection site?
- CQ16.  What  is  the  social-political  area  of  the collection site?
- CQ17 What are the geographic coordinates  of  the location where the object was collected?
- CQ18. What is the micro environment that characterizes the place where the object was collected?
- CQ19. What is the macro environment that characterizes the collection site?

1 Due to space restrictions of this article, CQ answers are presented in FOL, rather than SWRL.

## 2.5. Biodiversity Ontology

To answer these questions, the biodiversity ontology is divided into five sub-ontologies, connected by  relationships  between  the  concepts  and  axioms. They  are:  Collect 2 ;  Material  Entity,  sub-divided  into Abiotic  Entity  and  Biotic  Entity;  Spatial  Location; Ecosystem;  and  Environment.  The  OntoBio  macro schema is detailed in [2].

These ontologies are complementary to each other and once related to each other constitute the biodiversity ontology. They are connected by relations between their concepts, as well as by formal axioms. These axioms respond to competence questions presented above, in order to allow: (i) a rich semantic expressiveness  that  cannot  be  reached  by  only  using the  graphical  model,  (ii)  the  inferences  (for  encoding the  ontology),  (iii)  an  evaluation  of  the  reliability  of the proposed  ontology  with  its purpose, and  (iv) identification of inconsistencies.

## · Sub-Ontology Collect

This sub-ontology captures the structure of a protocol for collecting objects in fieldwork, in a high level of abstraction.

A Collect must  necessarily  be  associated  to  a CollectLocal (Sub-Ontology  Spatial  Location),  to  a CollectResponsibleInstitution ,  to  a CollectParticipant (Sub-Ontology Biotic Entity), to a CollectResponsible (Sub-Ontology Biotic Entity) and to a CollectedObject (Sub-Ontology Biotic Entity), characterizing a formal relation of  all roles mentioned  above.  The Collect is stereotyped as a relator (representing a type of property  that  mediates  two  or  more  sortals,  and  is existentially dependent on them, e.g. Wedding mediates  the  roles Husband and Wife )  that  mediates the formal  relation between  the roles played by CollectLocal , CollectResponsibleInstitution , CollectParticipant , CollectResponsible , and CollectObject . Similarly, InstitutionalLink , as a relator ,  mediates  the material  relation ( isLinkedTo ) between ResearchInstitution and Researcher (SubOntology  Biotic  Entity). Collect can  be  specialized according to the area, or to the instruments used.

Collect also establishes a formal relation (isClassifiedAs)  with the powertype CollectType .  The classes  of  the  supertype  Collect  are  instances  of  the powertype CollectType .

The kind Tool plays the role of CollectTool .  This, in turn, maintains a formal relation of mediation with the relator InstrumentedCollect .

2 The  term Collect is  used  to  represent  fieldwork  collection  of specimens, samples or records of occurrence.

Axiom 1 indicates that all collected objects will be associated with an institution responsible for collecting and a researcher responsible for collecting.

Axiom 1 -∀ x,y,z [ CollectResponsible (x) ∧ Collect (y) ∧ media(y,x) → ∃ z [ CollectResponsibleInstitution (z) ∧ media(y,z)]]

The  Competence  Questions  are  answered  by  the axioms  An  (FOL).  A1,  A2  and  A3  are  presented below.

- (A2) ∀ x [ Collect (x) → ∃ y [ TypeCollect (y) ∧ instanceOf (x,y)]]
- (A1) ∀ x [ Collect (x) → ∃ y [ CollectResponsibleInstitution (y) ∧ media(y,x)]]
- (A3) ∀ x,y,z  [ Collect (x) ∧ CollectedObject (y) ∧ media(x,y) ∧ ClassifiedObject (y) ∧ Classification (z) ∧ media(z,y) → ∃ w [ Specie (w) ∧ media(z,w)]]

## · Sub-Ontology Material Entity

## · Sub-Ontology Abiotic Entity

This  sub-ontology  conceptualizes  material  entities that are part of a Collect . MaterialEntity is  a  category that generalizes two sub-ontologies: Abiotic Entity and Biotic  Entity. MaterialEntity establishes  two formal relations with sub-ontology Spatial Location: locatedAt and localization with SpatialLocation and GeographicCoordinate respectively.

AbioticEntity is a categorization from MaterialEntity that  represents  all  non-living  physical factors and is specialized in the quantities Water , Soil and Air . Water and Soil establish  a formal  relation ( isClassifiedAs )  with  the powertypes TypeWater and TypeSoil respectively. Water and Soil classes will instantiate the powertypes TypeWater and TypeSoil .

## · Sub-Ontology Biotic Entity

BioticEntity is a categorization from MaterialEntity that encompasses all physical and living organisms and is  represented  by  the categories Plant , Animal and MicroOrganism .  They  establish  a  whole-part  relation ( memberOf ) shareable with the Flora , Fauna and Microbiota collectives since the categories can instantiate them more than once.

The kind Vegetation establishes  a formal  relation ( isConstitutedBy )  with  the collective Flora .  This kind is  specialized  in subkinds and  establishes  a formal relation ( isClassifiedAs ) with the powertype TypeVegetation . The subkinds of kind Vegetation will instantiate  the powertype TypeVegetation . Vegetation also  establishes  a formal  relation ( localizedAt )  with the category GeographicSpace .

Kind Person is  a  specialization  of  the  category Animal . Person may play the roles Researcher , CollectParticipant and Classifier in  an  overlapped way since Classifier can optionally be both a Researcher and a CollectParticipant or not. CollectParticipant can play the roles ParticipantResearcher and CollectAssistant . Researcher also specializes into the role ParticipantResearcher ,  which  in  turn  specializes  into CollectResponsible . In summary, every CollectParticipant is either a ParticipantResearcher or a CollectAssistant ; the CollectAssistant will always be a ParticipantResearcher .

The BioticEntity also  establishes formal  relations with the category Sex and the mixin StageOfLife that also  specializes  and  enriches  the  vocabulary  of  this ontology  schema. Sex and StageOfLife establish a formal  relation (isClassifiedAs)  with  the powertypes TypeSex and TypeStageOfLife respectively. The classes Sex and StageOfLife and  their  subclasses  will instantiate the powertypes TypeSex and TypeStageOfLife .

StageOfLife cannot be a category because it is not rigid, the stereotype used is mixin which is specialized by, phases ,  e.g. a single BioticEntity can be sorted by different life stages during its life.

The BioticEntity plays  the  role ObjectUnderStudy that is specialized in ClassfiedObject and CollectedObject in  an  overlapping  and  incomplete way . Classification is  stereotyped  as  a relator ,  that mediates the formal relation between the roles played by the powertype Specie , ClassifiedObject , and Classifier .

Axiom 2 demonstrates that if a classified object is associated  to  a  ranked  taxonomic  classification  and  a species is also associated with the same classification, then the classified object is an instance of the species. ∀ ∧ (y)

Axiom 2 -x,  y,  z  [ ClassifiedObject (x) Specie Classification(z) ∧ media  (z,  x) ∧ media  (z,  y) → instanceOf (x, y)]

The  following  observation  should  be  considered: Historical dependence relations cannot be represented in  OntoUML  because  it  is  based  in  foundational ontology, an ontology focused on structural aspects of endurant  individuals  and  endurant  universals,  which does  not  consider  dynamic  aspects  of  extension  over time  [7].  Thus,  for  the role ObjectUnderStudy ,  we should consider: An object under study can be specialized in collection object, collected object, classified  object,  discarded  object,  stored  object  and individuated  object  (which  receives  an  identification even if  provisional).  For  each time  period ,  the  object under  study  can  play  one  of  these  roles.  A  dropped, stored  or  individuated  object,  must  necessarily  be  a collected object. An individuated object can become a disposed object, collection object or become again an object  in  collect  (in  another  timeline).  Similar  to  the example "Mary is John's wife", which is real only for a given space in time.

The category BioticEntity establishes a formal relation ( instanceOf )  with powertype Specie ,  that  is, the  subclasses  of BioticEntity will  instantiate Specie . At first it may be said that every BioticEntity instantiates a single Specie . However, in some situations (peculiar to the domain under consideration), a BioticEntity can be classified in more than one way, that  is,  a BioticEntity can  instantiate  more  than  one Specie (typical  problem  of  taxonomic  classification, sometimes associated with the location or belief system of individual performing the ranking), which leads to a reflexive formal relation (identityOfSpecie).

Axiom 3 tells us that if a BioticEntity is ( instanceOf ) two differently classified Specie , then the two Specie are equal.

Axiom 4 ,  in  turn,  shows  us  that  if  two  SPECIES maintains  a formal  relation ( identityOfSpecie ),  both are instances of the same BioticEntity .

Axiom  4 -∀ x,  y,  z  [BioticEntity(x) ∧ Specie(y) ∧ instanceOf(x,  y) ∧ Specie(z) ∧ identityOfSpecie(y,  z) → instanceOf(x, z)]

Axiom  3 -∀ x,  y,  z  [BioticEntity(x) ∧ Specie(y) ∧ Specie(z) ∧ instanceOf(x,  y) ∧ instanceOf(x,  z) → identityOfSpecie(y, z)]

The powertype Specie establishes a formal relation (subtypeOf)  with powertype Genus,  which  establishes a formal relation ( subtypeOf )  with powertype Family . These formal  relations ,  semantically,  represent  the taxonomic hierarchy between family, genus and species  in  a  classification  system. Family , Genus and Specie specialize powertype the Taxon .  The category BioticEntity establishes  a formal relation (instanceOf) with powertype Taxon ,  the  subclasses  of BioticEntity instantiate Taxon .

The  Competence  Questions  are  answered  by  the axioms A4 to A12, presented below.

- (A4) ∀ x [ Collect (x) → ∃ y [ CollectResponsible (y) ∧ media(x,y)]]
- (A5) ∀ x  [ CollectedObject (x) ∧ ClassifiedObject (x) → ∃ y,z [ Classification (y) ∧ Classifier (z) ∧ media(y,x) ∧ media(y,z)]] (A6) ∀ x [ Collect (x) → ∃ y [ CollectParticipant (y) ∧ media(x,y)]]
- (A7) ∀ x [ Collect (x) → ∃ y [ CollectAssistant (y) ∧ media(x,y)]]
- (A8) ∀ x [ CollectedObject (x) ∧ ClassifiedObject (x) → ∃ y,z,w,v [ Classification (y) ∧ media(y,x) ∧ Specie (z) ∧ media(y,z) ∧ Genus (w) ∧ subtypeOf (z,w) ∧ Family (v) ∧ subtypeOf (w,v)]]
- (A9) ∀ x [ CollectedObject (x) ∧ ClassifiedObject (x) → ∃ y,z,w [ Classification (y) ∧ media(y,x) ∧ Specie (z) ∧ media(y,z) ∧ z.commonname(w) ]]
- (A10) ∀ x [ CollectedObject (x) → ∃ y x. StageOfLife (y)]
- (A11) ∀ x,y,z [ Taxon (x) ∧ GeographicSpace (y) ∧ CollectedObject (z) ∧ instanceOf (z,x) ∧ locatedAt (z,Y) → ∃ p z.peso(p)] /g1512 avg(p)
- (A12) ∀ x [ Collect (x) → ∃ y,z,w,v [ CollectLocal (y) ∧ media(x,y) ∧ Vegetation (z) ∧ GeographicSpace (v) ∧ locatedAt (z,v) ∧ spatiallyContainedAt (y,v) ∧ TypeVegetation (w) ∧ instanceOf (z,w)]]

## · Sub-Ontology Ecosystem

This  sub-ontology  conceptualizes  the  relations  of the  ecosystem  within  the  scope  of  a  collect  protocol for biodiversity data.

An  ecosystem  is  a  natural  unit  consisting  of  all plants, animals and microorganisms (biotic factors) in an  area  functioning  together  with  the  entire  physical non-living (abiotic) environment. Basically, an integrated and self-functioning system that consists of interactions of biotic  and abiotic  elements  whose dimensions can vary considerably.

The relationship  between  the  biotic  ("living")  and abiotic ("inanimate") elements in an ecosystem depends,  mainly,  on  the  energy  flow.  What  can  be considered an ecosystem varies in scale from a small lake, a puddle,  a forest, a city and  a well.  The importance is the relationship that is in this environment, which may contain common elements in different ecosystems.

Any  unit  that  includes  all  of  the  organisms  (i.e.: the" community") in a given area interacting with the physical environment so that a flow of energy leads to clearly  defined  trophic  structure,  biotic  diversity,  and material  cycles  (i.e.:  exchange  of  materials  between living and nonliving parts) within the system is considered an ecosystem.

The kind Ecosystem establishes whole-part relation ( componentOf )  shareable  with  Sub-Ontology Material  Entity  through categories BioticEntity and AbioticEntity .  Another  option  would  be  to  model  the whole-part relation ( componentOf )  shareable  directly with category MaterialEntity.

Ecosystem establishes a formal relation (isClassifiedAs) with powertype TypeEcosystem . Classes MacroEcosystem, MesoEcosystem and MicroEcosystem will instantiate the powertype TypeEcosystem . Another formal relation ( containedAt ) is established with category SpatialLocation .

Ecosystem establishes a self-relationship through a whole-part  relation ( componentOf )  shareable,  since Ecosystem is  not  applied  to  a  particular  geographic area,  i.e.  it  is  associated  with  various  dimensions  (it explains the specialization MacroEcosystem , MesoEcosyatem and MicroEcosystem ) and each Ecosystem can  be  composed of several Ecosystem .  In this context, we observe a whole-part relation ( componentOf ) between MicroEcosystem and MesoEcosystem ,  in  which  a MesoEcosystem may  be composed of two or more MicroEcosystem .  Likewise there is the whole-part relation ( componentOf ) between MesoEcosystem and MacroEcosystem .

Biome is a set of life (plant and animal) defined by the grouping of contiguous vegetation types identifiable  on  a  regional  scale,  with  similar  geo- climatic  conditions  and  shared  history  of  changes, resulting in its biological diversity (Source: IBGE).

In  a  biome,  the  profiles  of  the  size  and  dimension are  extremely important.  A biome can be analysed as an ecosystem, if it is understood as the flow of energy and the relationship between biotic and abiotic elements, but a single ecosystem will only be considered a biome if its dimensions are regional ,  i.e. on a large scale and consider abiotic aspects.

The subkind Biome establishes  a formal  relation (isClassifiedAs) with powertype TypeBioma . Subclasses  that  specialize Biome will  instantiate  the powertype TypeBioma .

The  Competence  Question  is  answered  by  the axiom A13, presented below.

(A13) ∀ x [ Collect (x) → ∃ y,z,w,v [ CollectLocal (y) ∧ media(x,y) ∧ Biome (z) ∧ GeographicSpace (v) ∧ locatedAt (z,v) ∧ spatiallyContainedAt (y,v) ∧ TypeBiome (w) ∧ instanceOf(z,w)]]

## · Sub-Ontology Spatial Location

A category SpatialLocation (as  reported by a GPS system) is specialized in GeographicSpace and GeographicPoint (latitude, longitude and altitude). GeographicSpace may be associated with geographical coordinates of various locations, but different GeographicSpace may also be associated with a particular set of coordinates in different circumstances. Thus, the formal relation ( spatialyContainedAt ) indicates that a GeographicSpace may contain spatially another GeographicSpace (adapted from [7]).

GeographicCoordinate is  a datatype that  provides an array of three elements representing altitude, latitude and longitude. GeographicCoordinate maintains formal relations ( localization ) with categories SpatialLocation , GeographicSpace and GeographicPoint .

GeographicSpace is specialized according to social-political, climatic and phytophysiognomic aspects. The categories ClimaticRegion and PhitophisiognomicRegion maintain  a formal  relation ( isClassifiedAs )  associated  with  a powertype .  These powertypes are  instantiated  by  the  specialization  of subclasses ClimaticRegion and PhitophisiognomicRegion . GeographicSpace also plays the role CollectLocal .

The  kind Locality establishes  a formal  relation ( spatialyContainedAt )  with the kind County ,  which in turn establishes a formal relation ( spatialyContainedAt ) with kind State , which establishes a formal  relation ( spatialyContainedAt ) with the kind Country . These formal relation , semantically  represent  the  hierarchy  and  relationships between localities  and  the  federal  units  recognized  in the political and social context of a country. Locality is specialized  according  to  the  property  and  the  type  of locality. The kind Locality establishes a formal relation ( isClassifiedAs ) with powertype TypeLocality , i.e. instances of Locality will instantiate TypeLocality .

The  Competence  Questions  are  answered  by  the axioms A14 to A17, presented below. (A14) ∀ x,u [ Collect (x) ∧ CollectedObject (u) ∧ media(x,u) → ∃ y,z,w,v [ GeographicCoordinate (y) ∧ localization (y,u) ∧ y.latitude(z) ∧ y.longitude(w) ∧ y.altitude(v)]] (A15) ∀ x [ Collect (x) → ∃ y,z,w [ CollectLocal (y) ∧ media(x,y) ∧ PhitophisiognomicRegion (z) ∧ spatiallyContainedAt (y,z) ∧ TypePhitophisiognomicRegion (w) ∧ instanceOf (z,w)]] (A16) ∀ x,y [ Collect (x) ∧ CollectLocal (y) ∧ media(x,y) → ∃ z,w,v,u [ Locality (z) ∧ spatiallyContainedAt (y,z) ∧ County (w) ∧ spatiallyContainedAt (z,w) ∧ State (v) ∧ spatiallyContainedAt (w,v) ∧ Country (u) ∧ spatiallyContainedAt (v,u)]] (A17) ∀ x [ CollectedObject (x) → ∃ y,z,w,v [ GeographicCoordinate (y) ∧ localization (y,x) ∧ y.latitude(z) ∧ y.longitude(w) ∧ y.altitude(v)]]

## · Sub-Ontology Environment

Environment is the set of substances, circumstances or conditions where there is a particular object  or  that  particular  action  occurs.  This  term  has specialized meanings in different contexts. In biology, it includes everything that directly affects the metabolism  or  behaviour  of  living  beings  or  species, including  light,  climate,  water,  moon  phases,  soil  or other living beings that cohabit with it.

Environment was  stereotyped  as mode which  can be  described  as  an  intrinsic  individual  moment.  By definition (OntoUML), must be connected in combination with at least one relationship type characterization .

Environment is specialized in modes MacroEnvironment and MicroEnvironment . Both MacroEnvironment and MicroEnvironment establish a formal relation ( isClassifiedAs ) with powertypes TypeMacroEnvironment and TypeMicroEnvironment . Subclasses of MacroEnvironment and MicroEnvironment will instantiate the powertypes TypeMacroEnvironment and TypeMicroEnvironment respectively.

Environment maintains relations of characterization with modes of the type ClimaticCondition , Luminosity , MoonPhase and is specialized in MacroEnvironment and MicroEnvironment . Environment , MacroEnvironment and MicroEnvironment maintain relations of characterization with categories SpatialLocation , GeographicSpace and GeographicPoint respectively from Sub- Ontology Spatial Location.

The  Competence  Questions  are  answered  by  the axioms A18 to A19, presented below. (A18) ∀ x [ CollectedObject (x) → ∃ y,z,w [ GeographicPoint (y) ∧ locatedAt(x,y) ∧ MicroEnvironment (z) ∧ isOf (z,y) ∧ TypeMicroEnvironment (w) ∧ instanceOf (z,w)]] (A19) ∀ x [ Collect (x) → ∃ y,z,w [ CollectLocal (y) ∧ media(x,y) ∧ MacroEnvironment (z) ∧ isOf(z,y) ∧ TypeMacroEnvironment(w) ∧ instanceOf(z,w)]]

## 2.6. Development Details

The following aspects should be considered regarding the development phase.

Initially, the ontology was modelled and implemented without ontology engineering. We chose a conceptual model; the domain problem was modelled and  then  implemented  using  the Protégé .  The  final result  was  unsatisfactory  since  the  conceptual  model used for modelling data was semantically meaningless and the ontology editor itself was just a coding language. The editor did not have sufficient resources to implement a complex domain, such as biodiversity.

At  this  point,  ontology  engineering  was  used  to develop the ontology. The loss of semantic expressiveness of the language used in the implementation phase (OWL) compared to the language  used  in  the  process  of  modelling/analysis (OntoUML) is notorious.

Some aspects should be highlighted:

- Historical dependence relations cannot be represented  in  OntoUML  because  it  is  focuses  on endurants  rather  than  dynamic  aspects  of  extension over time [7].
-  Biological  collections  reference  work  was  not modelled. Items in biological collections are associated to a taxonomic classification in general and not to the specific collected item.
- When a generalization is not disjoint and complete, it is considered incomplete and overlapping.
-  Biome  and  ecosystem  classes  both  specialize biological  systems  and  are  comprised  of  biological systems.
-  Ecosystem  is  not  considered  a  stereotype &lt;&lt; collective &gt;&gt; ,  it  is  a  whole  whose  parts  play  different roles  in  the  whole.  An  instance  of  Ecosystem  is  a functional complex.
-  When  using  languages  for  reference  ontologies (or  languages  for  conceptual  model  ontologies)  at  the analysis  level,  the  completeness  of  a  specialization  is semantically relevant. In contrast, when using languages for lightweight ontologies (or ontologies as implementation languages) at the implementation level, the completeness of a specialization is irrelevant.
- It is extremely complex to measure the Size of an organism. This difficulty is inherent to the biodiversity domain.
- GeographicSpace / GeographicCoordinate was adapted from Guizzardi [7].

The clearest examples of the loss of expressiveness of language, during ontology development occur in the implementation of the stereotypes powertype and datatype , which are expressed in the modelling language,  but  do  not  have  an  equivalent  primitive  in the implementation language.

OntoUML, modal logic intentional quantified, uses 1 st order  logic. Powertype uses  2 nd. order logic, based on  UML,  but  not  formalized  in  OntoUML.  Since OntoUML is an extension of UML standard, it can be represented by the use of powertype .

## 3. Conclusions

Within  the  perspective  of  systems  science,  the ontological  approach  contributes  to  the  advancement of formal ontology theory, providing excellent practical resources for knowledge acquisition, representation and integration of different data sources. Ontology contains an additional classification dimension that allows knowledge recovery and establishes  a  common  vocabulary,  fundamental  for knowledge sharing. However, the difficulty in developing ontologies is defining the set of knowledge that  it  must  contain,  and  fulfilling  the  objective  of developing  generic  ontologies  and  rich  and  complex domains that require investigation of a large number of services,  documents  and  different  understandings  of the various communities of a single domain.

The computing community for biodiversity is concerned  with  the  description  of,  and  access  to,  a variety of additional information that may be associated  with  a  specific  sample  of  a  specimen  or record of occurrence. This additional information enlarges the scope  of  potentially relevant data to include  a  wide  range  of  measurements  observed  in biotic  and  abiotic  aspects  of  the  environment.  For example,  to  analyse  patterns  in  global  abundance  of certain taxon, information on the status of coprecipitation,  frost,  soil  type,  land  use,  among  others, could be important parameters for analysis. Thus, the need  for  integration  of  the  biodiversity  informatics community finally converges with environmental science fields, and therefore relies on multi and interdisciplinary data for integrated or holistic understanding.  Biodiversity  domain  ontology  has  a wide-ranging domain and its demands are exacerbated.

Tools to assist the development of ontologies are a challenge.  Many  tools  do  not  provide  the  necessary resources  for  the  demands  of  the  domain,  especially complex  domains  such  as  biodiversity.  The  use  of graphical tools to visualize ontologies is important for capturing the ontology concepts and for training professionals  for  ontology  development.  It  is  difficult to  interact  with  domain  experts  without  the  use  of graphical resources.

The need to use ontologically well-founded languages for ontology conceptual modelling has been recognized in the literature. This is usually the result of concerns about interoperability and the inadequacy of lightweight  ontology  language  representation  to  solve these  issues.  Nevertheless,  these  languages  have  not yet been widely adopted. A main reason they have not been adopted is the need for high-level expertise in the treatment  of  underlying  philosophical  concepts  (e.g. sortais, perdurants, etc.).

When using ontology engineering: the completeness of a specialization is semantically relevant at the analysis level  and  irrelevant  when dealing with ontology as implementation; various structures/stereotypes found in languages at the analysis  level  cannot  be  mapped  to  a  language  at  the implementation level. Ontologies have been well modelled conceptually, but at the time of implementation, equivalent resources are not found to represent that particular situation.

Many  ontologies  are  hierarchies  of  classes  and subclasses, thus inferences or manipulation of controlled  vocabulary  cannot  be  done,  therefore  the scope of the resource is limited.

Another  ontology  development  difficulty  is  the issue of reuse and  integration of ontologies.  The question  considered  is  the  methodology  used  for  the development  of  each  ontology. Since there is no standardization  in  the  development  methodology,  in the considered conceptual models, or in the implementation  languages,  reuse  and  integration  can become unviable tasks because there will be differences  in  the  semantic  expressiveness  of  each resource  used  and  consequently  in  the  quality  and richness of each ontology developed.

This  research  was  developed  in  the  scope  of  the Intelligent  Systems  Group-GSI/UFAM,  in  partnership with the Semantic Interoperability Lab - LIS INPA.

OntoBio  has  already  been  validated  by  NEMO (Nucleus  for  Studies  on  Conceptual  Modelling  and Ontologies). NEMO, housed at the Federal University of Espírito Santo, is a reference in research  and development of ontologies in Brazil. However, several issues  still  need  to  be  addressed,  such  as  reuse  and integration of ontologies and semantic differences associated with expressiveness. OntoBio has contributed  to  knowledge  organization  and  has  been used in real world situations such as INPA's Biological Collection  Program  serving  as  a  central  object  of investigation for the previously mentioned issues.

The  development  of  OntoBio  showed  that  even when dealing with a complex domain, it is possible to model structured/semistructured knowledge from preexisting  databases.  The  modelling  of  tacit  knowledge remains an area that requires investigation. To represent and use knowledge stored from expertise in a structured way remains a challenge. We are currently exploring different approaches for knowledge organization and elicitation using OntoBio.

## 4. Acknowledgements

This  work  was  partially  supported  by  CNPQ,  grant number 486333/2011-6 and FAPEAM Universal Amazonas,  grant  number  021/2011062.03101/2012D.O. number 01.01.2008.

## 5. References

- [1] Borst, W.N. (1997) Construction of Engineering Ontologies  for  Knowledge  Sharing  and  Reuse.  PhD  thesis, Univ. of Twente. CTIT Ph.D.-thesis series No. 97-14. ISBN 90-365-0988-2.
- [2]  Albuquerque,  A.C.F.  (2011)  Desenvolvimento  de  uma Ontologia de Domínio para Modelagem de Biodiversidade. Dissertação de Mestrado, UFAM, 2011.
- [3]  Ashburner, M. et al (2000) Gene ontology: tool for the uni/g191cation of biology. The gene ontology consortium. Nature Genetics, 25(1):25-29.
- [4] Baker, P.G. et al (1998) TAMBIS-Transparent Access to Multiple Bioinformatics Information Sources. In International Conference on Intelligent Systems for Molecular Biology, volume 6, pages 25-34, Montreal, Canada.
- [5] Campos dos Santos, J.L. (2003) A Biodiversity Information System in an Open Data/Metadatabase Architecture' Ph. D. Thesis. International Institute For GeoInformation Science and Earth Observation. Enschede, The Netherlands. ISBN 90-6164-214-0.
- [6] Falbo et al. (1998) A Systematic Approach for Building Ontologies. In Progress in Artificial Intelligence -IBERAMIA'98  (Proceedings  of  the  6th Ibero-American Conference on AI), Coelho, H. (Ed.): LNCS 1484 (Lecture Notes  in  Artificial  Intelligence),  pp.  349-360,  SpringerVerlag Berlin Heidelberg, Lisbon, Portugal.
- [7] Guizzardi,G. (2005) Ontological Foundations for Structural Conceptual Models. PhD Thesis (CUM LAUDE), University  of  Twente,  The  Netherlands.  Published  as  the same name book in Telematica Institut Fundamental Research. Series  No.  15,  ISBN 90-75176-81-3 ISSN 13881795; No. 015; CTIT PhD-thesis, ISSN 1381-3617; No. 0574.
- [8]  Benevides,  A.B.  and  Guizzardi,G.  (2009)  A  ModelBased Tool for Conceptual Modeling and Domain Ontology Engineering  in  OntoUML,11th  Intl.  Conf.  on  Enterprise Information Systems (ICEIS), Milan, LNBIP.
