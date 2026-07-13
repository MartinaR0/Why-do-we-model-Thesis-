## An Ontology Reference Model for Normative Acts

Pedro Paulo F. Barcelos 1 , Renata S. S. Guizzardi 2 , Anilton S. Garcia 1

1 Electrical Engineering Department - PPGEE 2 Department of Computer Science - PPGI

Federal University of Espírito Santo - UFES Vitória - ES - Brazil

pedropaulofb@gmail.com, rguizzardi@inf.ufes.br, anilton@inf.br

Abstract. Normative Acts are important legislative and regulatory documents made  by  different  governmental  organs.  Every  year,  a  huge  amount  of information  is  provided  in  Normative  Acts  by  these  organs  without  control, i.e.,  there  is  no  effective  way  to  verify  redundancies,  inconsistencies,  crossimpact  and  ambiguities.  In  this  paper,  we  propose  a  domain  ontology  for Normative  Acts  based  on  official  documents  (the  Brazilian  Constitution  and the Redaction Manual of the Presidency of the Republic) as a reference model that can be used to improve communication, interoperation and automation of Normative  Acts.  The  reference  model  is  built  with  a  highly  expressive  wellfounded language within a methodology that ensures its quality.

## 1. Introduction

Among  the  various  duties  of  the  Brazilian  powers,  one  of  its  main  activities  is  the publication of Normative Acts (NAs) to establish standards and to inform decisions and other information to society. The main types of Brazilian NAs can be found in Article 59  of  the  1988  Constitution  of  the  Federative  Republic  of  Brazil.  NAs  are  central  to legislative power, where these acts are daily created in the form of laws. They are also important to the executive power, where they are mainly created in form of executive decrees. In addition, they are essential to the national regulatory agencies, where they are created in the form of resolutions.

The  activities  done  by  these  organs  to  elaborate,  edit,  and  publish  NAs  are complex  and  involve  several  organizational  units  and  a  large  number  of  human resources.  Different  people,  with  different  cultural  and  technical  knowledge  and  with different interests are involved with the creation of NAs. Thus, these people must share a  common  comprehension  about  the  terms  and  concepts  related  to  NAs,  in  order  to improve  the  resultant  document.  Due  to  the  legislative  and  regulatory  importance  of NAs, miscomprehension of concepts during the planning and elaboration of NAs can range from a simple structure error (resulting in a difficulty to automatically read the generated  document  with  an  computational  application)  to  a  huge  interpretation problem, generating social and financial losses to society and companies. Moreover, to be published, the NAs text must be clear and unambiguous, as society and other public and  private  organs  have  to  comprehend  and  share  (textually  or  computationally)  its contents.

In  order  to  produce  the  desired  impact  to  society,  the  NAs  must  be  carefully planned in their elaboration stage, involving studies and researches of previous related NAs.  Today,  these  studies  and  researches  are  done  manually,  without  intelligence provided by computational applications - to research a NA, an editor must use a nonspecialized  research  tool,  just  like  any  layman  would.  Moreover,  once  published,  its content must be easily accessible and researchable by society and other stakeholders. In fact, in Brazil, a federal law ensures that every public organ or entity must publish, in detail, the formats used to structure their information. It is widely known that, although a reference document exists for the NAs writing, this document is not always used by the  legislative  houses  and  regulatory  agencies,  thus  resulting  in  the  above  cited problems.

The  official  reference  document  which  deals  with  the  NAs'  writing  is  the Presidency  Writing  Manual  (in  Portuguese, Manual  de  Redação  da  Presidência  da República -  available  at  http://www.planalto.gov.br/ccivil\_03/manual/).  The  Writing Manual  is  divided  into  two  parts:  the  first,  among  other  topics,  presents  the  official communications and standardizes the layout of expedients. The second part deals with the elaboration and wording of NAs and presents examples of the Normative Acts and the legislative procedure.

This second part of the document, in particular, describes the textual elements that a NA may have and their inter-relationships, making it a valuable reference and a natural candidate for the development of an Ontology Reference Model for this domain. Even though the description  contained  in  the  Presidency  Writing  Manual  is  available only in natural language (Portuguese), which does not guarantee absence of ambiguities, the  use  of  an  ontologically  well-founded  language  can  identify  and  correct  these possible  deficiencies.  Such  type  of  language  differs  from  other  commonly  used languages  to  represent  data  or  knowledge  in  information  systems  (like  databases schemas) as they are built accordingly to a foundational ontology, i.e., a meta-ontology that  describes  a  set  of  real-world  categories  that  can  be  used  to  talk  about  reality [Guizzardi  2007].  A  framework  for  ontological  evaluation  is  presented  in  [Guizzardi 2005],  and  an  example  of  an  application  of  this  kind  of  evaluation  in  a  network language, also described in natural language, can be seen in [Barcelos et al. 2011].

Our objective in this paper is to present a domain ontology developed to be a reference model for NAs.   Reference  Models  are  essential  artifacts  when  dealing  with information of a given domain, as they formalize concepts and their relations in a clear and  unambiguous  way,  improving  communication  and  information  exchange  and interoperation.  In fact,  the  main objective of a  reference model is to assist humans in tasks  such  as  meaning  negotiation  and  consensus  establishment.  This  goal  can  be achieved  by  using  highly  expressive  languages,  within  a  formal  ontology  engineering methodology,  to  create  a  strongly  axiomatized  ontology  that  approximates  as  well  as possible to the domain  conceptualization. The  focus on these languages  is on representation adequacy, instead of computational representation [Guizzardi 2007]. The Normative Acts ontology reference model is formalized with OntoUML, an ontologically  well-founded  profile  of  the  Unified  Modeling  Language  (UML).  The ontology engineering methodology used guarantees the validity and correctness of the modeled information through syntactical and semantic validations.

In brief, the main contribution of this paper is to provide an ontology reference model for the NAs domain, formalized with OntoUML within an ontology engineering methodology. A secondary contribution is the presentation of this ontology`s capabilities to be used as basis for computational implementation.

The  work  described  here  is  placed  in  the  context  of  the  Information  and Knowledge  Management  Model  Project  ('Modelo  de  Gestão  da  Informação  e  do Conhecimento',  MGIC,  in  Portuguese),  a  cooperation  project  between  the  Federal Fluminense University and the National Agency of Terrestrial Transportation (ANTT). The  MGIC  aims  to  improve  efficiency  in  ANTT's  decision-making.  To  achieve  this goal, the information modeling work is performed on four different fronts. The ontology modeling, one of these fronts, aims to create conceptual reference model ontologies for structuring the agency's information.

This  paper  is  structured  as  follows:  in  section  2,  we  compare  this  work  with others that are related to NAs; section 3 presents the ontology engineering methodology used to create and guarantee the quality of the proposed NAs ontology; in section 4, we describe the ontology reference model for NAs in details; section 5 presents possibilities of  practical  use  of  the  NAs  ontology  as  a  conceptual  model  and  as  basis  for computational implementation; section 6 presents the main conclusions as well as future works.

## 2. Related Works

As the legislative  process  involves  several  public  entities in various spheres and as it generates  a  large  amount  of  information,  a  huge  number  of  works  are  published involving  the  creation  of  ontologies  used  for  communication  and  automation  in  this domain. In fact, some of these works are the results of large projects, like the LexML Project [Lima 2010], and the International Ontojuris Project [Clara et al. 2010].

Legal ontology projects differentiate from each other in scope, objective and in which  kind  of  ontology  they  are  based.  As  an  example,  the  Brazilian  LexML  project uses  as  basis  an  ontology  called  FRBROO,  an  ontology  in  the  domain  of  cultural heritage; while the Ontojuris Project uses a lightweight ontology (almost a dictionary), similarly to other initiatives, such as the LTS (Legal Taxonomy Syllabus) [Ajani et al. 2009], in Europe.

The  Power  project,  in  its  turn,  uses  shared  conceptual  models  to  facilitate  the legislation  process  [Engers  and  Glassée  2001].  [Visser  and  Bench-Capon  1996]  also proposed a Legal Ontology specification, while [Boer et al. 2003] proposed an ontology for comparing and harmonizing legislation.   Other works aim to provide foundations for concepts  of  law,  like  [Breuker  and  Hoekstra  2004].  These  works  and  the  ontology proposed in this paper, however, do not share the same scope, as the foundations are provided to models representing legislative process concepts, not the internal elements and relations of Normative Acts.

Even though there is a vast number of works about ontologies in the legislative area, it appears, however, that no work involves the creation of a well-founded ontology reference model for the representation of the Normative Acts' internal structure.

## 3. Ontology Engineering Methodology

In  order  to  create  an  ontology  reference  model  that  correctly  reflects  the  intended domain and that is  able  to  be  used  by  different  agents  (people,  groups  of  people  and other,  like  machines)  to  interoperate,  an  ontology  engineering  methodology  must  be used.  This  section  presents  our  methodology,  partially  based  on  the  Ontological Approach to Domain Engineering presented in [Falbo et al. 2002]. In our methodology, shown  in  Figure  1,  we  use  the  steps  of  the  Ontological  Approach  to  Domain Engineering with different level of rigor, abstracting non-essential elements to our case.

Figure 1 - The used Ontology Engineering Methodology

[FIGURE]

Scope definition is the first step of the iterative methodology. Our ontology uses a  reference  document,  the  Presidency  Writing  Manual,  written  in  natural  language (Portuguese in our case), as the modeling scope.

The  second  step  of  the  methodology  is  the ontology  capture ,  were  the  sub activities  of  Information  Acquisition  and  Conceptualization  are  realized.  In  order  to acquire  information,  a  domain  study  is  necessary  for  the  modeler  to  learn  about  the subject  to  be  modeled.  We  used  the  Presidency  Writing  Manual  and  the  Brazilian Constitution as main source of information. Conceptualizations are immaterial entities that only exist in the mind of the user or a community of users of a language. In order to be documented, they must be captured in terms of some concrete artifact. This implies that a language  is necessary  for  representing  them  in  a  concise,  complete  and unambiguous way [Guizzardi 2007].

The ontology formalization step consists in the formalization, through diagrams, of the domain model. In order to correctly represent a domain, an expressive language must  be  used.  This  language  should  be  able  to  represent  information  despite  of implementation  technologies  or  limitations.  In  this  work,  we  use  OntoUML,  an ontologically well-founded UML profile [Guizzardi 2005]. As graphical languages are not  always  capable  of  correctly  representing  the  domain,  some  Object  Constraint Language (OCL) rules are also necessary for restrictions and derivations rules.

As  we  intend  to  create  a  reference  model  for  Normative  Acts  (NAs),  it  is important to ensure that the diagrams allow only instantiation as desired, that is, that the user can only create instances that are possible in the real world. To do this, we focus on the validation of information modeled at the diagrams.   In this stage, we have two main types of validation: (1) the syntactic one, which guarantees that the OntoUML models created  are  syntactically  correct,  that  is,  that  the  entities  created  are  according  to  the languages  meta-model;  and  (2)  the  semantic  validation,  where  we  want  to  avoid syntactically  correct  diagrams  that  can  be  instantiated  to  generate  undesired  world  of affairs.

The OntoUML Lightweight Editor (OLED) (https://code.google.com/p/ontoumllightweight-editor/)  provides  the syntactical  validation .  The  Semantic Validation does not ensure that there is no impossible state of affairs allowed by the ontology, it does, in fact,  ensure  that  its  occurrences  are  reduced.  The  semantic  validation  is  done  in  two steps, within  an  OLED's  module,  called  MOVE  (OntoUML  Model  Validation Environment):  the  first  step  is  an anti-patterns  identification and  treatment  and  the second step is a simulation using Alloy.

As  stated  in  [Sales  et  al.  2012],  an  anti-pattern  is  a  recurrent  decision  for  a specific scenario that usually results in more negative consequences than positives ones. The  MOVE tool  provides  a  model  verification  to  check  occurrences  of  anti-patterns. Simulation can help the modeler to find inconsistencies and unwanted worlds of affairs allowed by the model. The MOVE tool can translate the model to Alloy [Jackson 2002]. Alloy is a model-checking language that can be used to simulate possible worlds based on  the  formalization  provided.  This  kind  of  validation  guarantees  the  validity  of modeled  information  inside  an  specific  context,  thus  its  usage  significantly  improves model quality as the user can make assertions and check if these are valid or not.

## 3.1. The use of OntoUML

OntoUML provides a well-founded UML profile. The classes in OntoUML are  based on  some  important  ontological  meta-properties  that  allow  the  creation  of  consistent ontologies [Guizzardi 2005].

Examples of meta-properties are identity principle and rigidity . Identity principle is related to the nature of an object. For example, a Student is a Person, as they have the same  identity  principle,  but  they  can  never  be  a  Car,  as  they  have  different  identity principle.  The rigidity principle  is  the  capacity  of  an  entity  to  be  part  of  a  class maintaining its existence. For example: John is an individual of the class Student but, in a given world, it can cease to be a Student and still exists as a Person. However, in any world John cannot cease to be a Person without ceasing to exist. Thus, Student is an example of an anti-rigid class while Person is an example of a rigid class.

Table 1 - OntoUML Class Stereotypes present in the Normative Acts Ontology

| Stereotype   | Main Characteristics                                                                                           | Example                     |
|--------------|----------------------------------------------------------------------------------------------------------------|-----------------------------|
| Kind         | Rigid types which provide an identity principle                                                                | Person, TV                  |
| Subkind      | Relationally independent rigid specializations of kinds, collectives, or other subkinds                        | Man, LED TV                 |
| Category     | Aggregate rigid elements with different identity principles                                                    | Animal, Electronic          |
| Collective   | Elements whose instances are collectives, i.e., they are collections of elements that have a uniform structure | A forest, a group of people |

The OntoUML  stereotypes  present in the Normative  Acts Ontology are summarized in Table 1 above.   For an in depth presentation, formal characterization and empirical evidence for a number of the ontological categories underlying OntoUML, the reader is referred to [Guizzardi 2005].

## 4. The Domain Ontology for Brazilian Normative Acts

The  domain  ontology  presented  here  is  based  on  official  documents:  the  Presidency Writing  Manual  (hereafter,  for  short,  called  PWM)  and  on  the  Brazilian  Federal Constitution.  Although  the  Normative  Acts  (NAs)  Ontology  created  to  the  National Agency of Terrestrial Transportation involves three aspects of the Normative Process Structural Elements, Management Issues and Regulatory Marks - the Reference Model presented  here  considers  just  the  Structural  Elements  of  NAs,  considering  NAs compositions, aggregations, its internal elements, and all relations between these.

The  ontology  reference  model  presented  in  detail  in  this  section  is  divided  in three  subdomains  and  modeled  using  OntoUML  diagrams.  For  highlight,  the  first occurrences  of  an  ontology  terms  are  presented  with  the  Courier  New  font.  It  is important to mention that the ontology reference model is fully available for download at: http://www.nemo.inf.ufes.br/en/courses/ontologyengineering.

## 4.1. Normative Acts and Articles Subdomain

The model related to this subdomain states the different existing types of Normative Acts in Brazil and their internal structure.

Due to space limitations, the diagram that differentiates the NAs is not presented in  image.  This  diagram's  information  was  extracted  from  the  59th  Brazilian  Federal Constitution article, where it states that the legislative process involves the creation of: Constitution Amendments , Complementary Laws , Ordinary Laws , Delegated Laws , Provisional Measures , Legislative Decrees and Resolutions . Decree , Ordinance and Handout were extracted from the PWM. All of these NAs are disjoint from each other, i.e., no NA can be of two different types at the same time. NAs are defined by its composition by different subkinds of Articles and by its preliminary elements.

At the adopted conceptualization, the Article performs the most important function in NAs as it contains the statements defining the rules and information that the NA is about. In the ontology reference model every concept has a (direct or indirect) relation  with  Articles.  It  can  be  seen  in  Figure  2  that  every  article  has  an  identifier number.  An  OCL  rule  formalizes  that  Articles  in  the  same  NA  have  unique  natural numbers.

Figure 2 also represents the different types of Articles. Articles can  be Ordinary Articles (regular  Articles,  the  ones  that  states  new  communication), Revocation  Clauses (Articles that revokes other Articles) or Duration Clauses (Articles that asserts a validation time). Every NA must be composed of at least one Ordinary Article, but it is not necessary for it to be composed of Revocation Clauses or Duration Clauses.

Figure 2. Compositions of Normative Acts

[FIGURE]

Preamble , Epigraph and Brief  ( in  Portuguese: Preâmbulo , Epígrafe , and Ementa ,  respectively)  are  obligatory  preliminary  elements  in  every  NA.  These preliminary elements cannot be modified (vetoed, revoked or altered) - these properties are  stated  in  the  Ontology  Reference  Model  by  the  composition  meta-properties  of essential and inseparable [Guizzardi 2005].

## 4.2. Discrimination of Normative Acts' Elements Subdomain

Grouping and Discrimination  Elements  are  important  part  of  NAs  as  they  provide  to their  author the desired abstraction granularity. The Discrimination Elements are used to describe in more detail the information being normalized in a NA.

The  different  types  of  Discrimination  Elements  are: Paragraph , Item , Letter (in  Portuguese: Parágrafo , Inciso ,  and Alínea ,  respectively)  and Letter Discriminator . Every Discrimination Element is a part of a Normative Act because the Articles that are discriminated by these elements are part of the Normative Act.

Articles can be of two types: Simple Article or Composed Article . While  the  former  consists  only  of  a  text,  the  latter  consists  of  its  introductory  text, named Caput, and  of  at  least  one  Item  or  Paragraph.  Both  types  are  represented  in Figure 3.

Figure 3. Compositions of Articles

[FIGURE]

If there is just one Paragraph composing an Article, its identification string must be Unique Paragraph . OCL rules ensure these restrictions.

Articles and Paragraphs can be decomposed in Items (see Figure 3), identified by  roman  numbers.  Items,  represented  in  Figure  4,  can  be Simple Items (when undivided) or composed by Letters. Letters can also be undivided ( Simple Letters ) or they can be divided in Letter Discriminators. The PWM states at its section 10.2.2.3 that ' Letters can be discriminated with cardinal numbers, followed by periods '. As no name is given to these discrimination elements, we named them Letter Discriminators.

Figure 4 - Items, Letters and Letter Discriminators

[FIGURE]

## 4.3 Grouping of Normative Acts' Elements Subdomain

The Grouping Elements are used to easily aggregate related information in a NA. They are the Parts , Books , Charters , Chapters and Sections  ( in Portuguese: Parte , Livro , Título , Capítulo ,  and Seção ,  respectively ) .  Every  Grouping Element is part of the NA that is composed of the Articles that are grouped by these Grouping Elements.

As  represented  in  Figure  5,  related  Articles  can  be  grouped  in  Sections  or Chapters. Sections can be of two types: Simple Sections , i.e., Sections that are not composed by other Sections, and Composed Sections, that are Sections composed by  other  Sections  or Subsections :  a  specific  type  of  Section  that  just  occurs composing a Composed Section.

Figure 5. Grouping of Articles in Sections and Chapters

[FIGURE]

The grouping of Chapters by Charters, of Charters by Books, and of Books by Parts can be seen in Figure 6.

Figure 6 - Chapters, Charters, Books and Parts

[FIGURE]

Parts  can  be  of  types Double Part or Multiple Part .  OCL  rules  were created to state that every NA that is composed by a Multiple Part always have at least three  of  these  and  to  state  that  if  the  NA  is  composed  of  a  Double  Part  it  must  have exactly only one instance of a General Part and a Special Part .

## 5. Practical Applications

As  stated  by  [Guizzardi  2007],  there  is  a  clear  distinction  between  (a)  Conceptual Modeling, (b) Design and (c) Implementation. The ontology reference model presented here is a result of the Conceptual Modeling stage, as it aims to make a clear and precise description of the Normative  Acts  (NA)  domain  elements  for  the  purposes  of communication, learning and problem solving, independent of implementation platform or technology. Considering a Model Driven Architecture approach [Miller and Mukerji 2003],  the  Reference  Model  can  be  seen  as  the Computational  Independent  Model (CIM), its design products as Platform Independent Models (PIMs) and its implementation  products  as Platform  Specific  Models (PSMs).  In  the  Design  and Implementation  phase,  this  conceptual  specification  is  transformed  by  taking  into consideration  a  number  of  issues  ranging  from  architectural  styles,  non-functional quality  criteria  to  be  maximized,  target  implementation  environment,  etc.  The  same conceptual  specification  can  potentially  be  used  to  produce  a  number  of  different artifacts  in  different  implementation  languages  -  ranging  from  relational  databases  to semantic web languages, like the Web Ontology Language (OWL).

In  Brazil,  according  to  the  Federal  Information Access Law (Brazilian Federal Law  number  12,527,  from  November  18th  2011.  Available  just  in  Portuguese  at http://www.planalto.gov.br/ccivil\_03/\_ato2011-2014/2011/lei/l12527.htm), every public organ or entity must use the Internet to publish, in detail, the formats used to structure their  information.  The  ontology  presented  here,  as  a  well-founded  formalization  of  a domain conceptualization, is the best option to accomplish this requirement. This same law also states that the public organ or entity must enable automated access by external systems to the information in open, structured and machine-readable formats. Thus, an ontology implementation in the Resource Description Framework (RDF) or OWL can entirely  satisfy  the  law.  In  fact,  the  federal  government  with  the  World  Wide  Web Consortium (W3C), cite OWL as a desirable practice for Open Data [Comitê Gestor da Internet no Brasil 2011].

A computational implementation of the proposed ontology reference model can also  be  used  in  applications  to  assist  different  stages  of  the  regulatory  and  legislative process,  like  the  NA  edition.  The  usage  of  automation  software  can  significantly improve the time spent with the huge amount of NAs that are created daily in a public entity.  This  automation  can  make  processes  more  effective  as  it  reduces  the  domain specialists' writing and research time and it gives them more time to think and reason about the subject of the documents.

In the edition phase, ontology-based software can eliminate from the writer the need to know each concepts from the PWM, as the software can automatically create these concepts  for  him.  Another  great improvement  is  the  restriction to create documents that are not in accordance with the PWM. As an example, every time a writer creates an Article, if he wants to create a subtopic of this Article, he can just press the TAB key and two options appears to him: an Item or a Paragraph. So, it is not possible to  create,  for  example,  a  Letter  discriminating  directly  an  Article.  Another  possible usage of this software would be to evaluate Normative Acts already created.

The ontology-based software for the NA process can be significantly improved by  using  other  Ontology  Models.  The  usage  of  an  ontology  model  about  NAs' revocation  or  modifications  can  add  the  ability  to  control  the  impact  of  a  newly published NA in others already published. That is, there will be no need to manually state that an NA is repealed; it can be done automatically by software - thus, eliminating human errors.

Also, adding ontology reference models to the domain that the NAs are about, we can create  a  semantic  annotation  feature  [Oren  et  al.  2006],  where  the  writer  can mark (tag)  the  concepts  improving  their  semantics  in  accordance  with  the  conceptual model.  Please  consider  a  reference  model  about  highways,  where  a  highway  is composed  by  lanes  and  where  it  has  a  relation  with  other  highways  (for  example 'crosses').  If  the  NA  editor  is  writing,  for  example,  about  BR-101  (a  Brazilian highway), it can mark it as an instance of highway so, even if it is not explicit in the text that the BR-101 has lanes and that it can cross other highways, this information can be inferred. Semantic annotation is widely studied and used, even for large-scale scenarios [Dill et al. 2003].

With the usage of semantic annotation, the search on documents is improved, as there is no need to lexically match all search terms. A search using the word 'highway' can return documents that use the term highway, and documents that deal with highways but do no explicitly use this concept, for example, a document that contains information about  the  BR-101.  An  improved  search  is  vital  to  guarantee  that  new  NAs  do  not conflicts with older NAs.

Already existent ontology-based tools for the legislative process can be found in [Valente  and  Breuker  1995]  and  [Gangemi  et  al.  2003].  The  base  ontologies  used  in these works, however, do not share the same scope of the ontology here presented and some  of  them  are  not  formalized  using  a  well-founded  ontology  language  such  as OntoUML.

## 6. Conclusions

This work presented an Ontology Reference Model for the domain of Normative Acts, built  over  information  extracted  from  the  Brazilian  Constitution  and  the  Presidency Writing  Manual.  The  proposed  ontology  is  formalized  using  an  ontologically  wellfounded  highly  expressive  language  and  it  was  developed  following  the  ontology engineering  methodology  presented  here.  This  ontology  can  be  used  as  basis  for automation and interoperation of information about this domain.

The Ontology Reference Model is presented considering three subdomains:

(a) Normative Acts and Articles, where different existing types of Brazilian Normative Acts are presented as well as their internal structure, representing their composition by articles and preliminary elements;

(b)  Discrimination  of  Normative  Acts'  Elements,  related  to  elements  that  are  used  to describe in detail the information being normalized in a Normative Act;

(c)  Grouping  of  Normative  Acts'  Elements,  that  formalizes  elements  that  are  used  to easily aggregate related information.

As a reference model, this ontology aims to make a clear and precise description of  the  domain  elements  for  the  purposes  of  communication,  learning  and  problem solving.  As  an  implementation,  the  model  is  able  to  solve  problems  related  to  the redaction  and  edition  of  Normative  Acts,  like  reference  finding,  and  cross-impact analysis. The ontology, in its conceptual or computational form, can be used to adequate public organs to the Federal Information Access Law, as every public organ or entity must  use  the  Internet to publish, in detail, the formats  used  to  structure  their information.

Future work involves the expansion of the ontology to represent other aspects of Normative Acts, like temporal ones (e.g. an NA is valid from a beginning date and can have an end date). Another important future work is the creation of the computational ontology in semantic web languages, like OWL.

Acknowledgements. This research has been funded by the MGIC Project. We thank the  ANTT employees and all project members who have somehow contributed to the development  of  this  work.  This  research  has  also  been  funded  by  FAPES/CNPq (PRONEX 52272362/11).

## References

- Ajani, G., Boella, G., Lesmo, L., et al. (2009). Legal Taxonomy Syllabus version 2.0. In IDT.
- Barcelos,  P.  P.  F.,  Guizzardi,  G.,  Garcia,  A.  S.  and  Monteiro,  M.  E.  (may  2011). Ontological Evaluation of  the  ITU-T  Recommendation  G.805.  In  2011  18th International Conference on Telecommunications. IEEE.
- Boer, A., Van Engers, T. and Winkels, R. (2003). Using ontologies for comparing and harmonizing  legislation.  In  Proceedings  of  the  9th  international  conference  on Artificial intelligence and law - ICAIL '03. ACM Press.

- Breuker,  J.  and  Hoekstra,  R.  (2004).  Core  concepts  of  law:  taking  common  sense seriously.  In  Proceedings  of  the  Third  International  Conference  (FOIS-2004).  IOS Press.
- Clara, B. L., Di Iorio, A. H. and Lerena, R. G. (2010). Ontologies , ICTs and Law The International  Ontojuris  Project.  In  Proceedings  of  LOAIT  2010  IV  Workshop  on Legal Ontologies and Artificial Intelligence Techniques.
- Comitê Gestor da Internet no Brasil (2011). Manual dos Dados Abertos: Desenvolvedores.http://www.w3c.br/pub/Materiais/PublicacoesW3C/manual\_dados\_ abertos\_desenvolvedores\_web.pdf.
- Dill,  S.,  Eiron,  N.,  Gibson,  D.,  et  al.  (2003).  A  Case  for  Automated  Large  Scale Semantic Annotation. Web Semantics: Science, Services and Agents on the World Wide Web 1.1, v. 1, n. 1, p. 115-132.
- Engers, T. M. Van and Glassée, E. (2001). Facilitating the Legislation Process Using a Shared Conceptual Model. IEEE Intelligent Systems, v. 16, n. 1, p. 50-58.
- Falbo, R. de A., Guizzardi, G. and Duarte, K. C. (2002). An Ontological Approach to Domain Engineering. Proceedings of the 14th international conference on Software engineering and knowledge engineering - SEKE  '02, p. 351-358.
- Gangemi,  A.,  Prisco,  A.,  Sagri,  M.-T.,  Steve,  G.  and  Tiscornia,  D.  (2003).  Some ontological tools to support legal regulatory compliance, with a case study. In On The Move to Meaningful Internet Systems 2003: OTM 2003 Workshops.
- Guizzardi,  G.  (2005).  Ontological  Foundations  for  Structural  Conceptual  Models. Enschede: Centre for Telematics and Information Technology University of Twente.
- Guizzardi, G. (2007). On Ontology, ontologies, Conceptualizations, Modeling Languages, and (Meta)Models. Proceedings of the 2007 conference on Databases and Information Systems IV: 7th International Baltic Conference, p. 18-39.
- Jackson, D. (2002). Alloy: a lightweight object modelling notation. ACM Transactions on Software Engineering and Methodology (TOSEM), v. 11, n. 2, p. 256-290.
- Lima,  J.  A.  de  O.  (2010).  Interoperabilidade  Semântica  no  LexML.  Panorama  da Interoperabilidade no Brasil. Brasília: p. 74-79.
- Miller,  J.  and  Mukerji,  J.  (2003).  MDA  Guide  Version  1.0.1.  Object  Management Group.
- Oren,  E.,  Möller,  K.  H.,  Scerri,  S.,  Handschuh,  S.  and  Sintek,  M.  (2006).  What  are Semantic Annotations?.
- Sales,  T.  P.,  Barcelos,  P.  P.  F.  and  Guizzardi,  G.  (2012).  Identification  of  Semantic Anti-Patterns  in  Ontology-Driven  Conceptual  Modeling  via  Visual  Simulation.  4th International Workshop on Ontology-Driven Information Systems (ODISE 2012).
- Valente,  A.  and  Breuker,  J.  (1995).  ON-LINE:  An  architecture  for  modelling  legal information. In Proceedings of the 5th international conference on Artificial intelligence and law. ACM.
- Visser, P. and Bench-Capon, T. (1996). The Formal Specification of a Legal Ontology. In Proceedings of JURIX.
