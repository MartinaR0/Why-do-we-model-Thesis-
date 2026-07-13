## A Hazard Modeling Language for Safety-Critical Systems Based on the Hazard Ontology

Jiale Zhou, Kaj Hänninen, Kristina Lundqvist Mälardalen University, Västerås, Sweden

zhou.jiale@mdh.se

Abstract -Preliminary  hazard  analysis  (PHA)  is  a  key  safetyconcerned activity  to  identify  potential  hazards.  However,  since various stakeholders will be involved in the identification process, a  common  understanding  of  the  nature  of  hazards  among stakeholders, such as what a hazard consists of and how to describe it without ambiguities, is of crucial importance to achieve the goal of  PHA.  In  this  work,  we  propose  a  hazard  modeling  language (HML) based on a domain ontology to facilitate the specification of identified hazards. In addition, we present an approach to guide the  transformation  from  natural  language  hazard  descriptions into the HML specification. Finally, an industrial PHA example is used to illustrate the usefulness of our work.

Keywords-preliminary hazard analysis; hazard ontology; hazard modeling language;

## I. INTRODUCTION

This  Preliminary  hazard  analysis  (PHA)  is  a  key  safetyconcerned  activity  to  provide  stakeholders  (e.g.,  developers, organizations and authorities) with a general understanding of the systems' potential hazards in terms of their causes, consequences,  risks,  etc.  Typically,  the  identified  hazards  are described  using  natural  languages  (NL)  in  the  form  of  PHA worksheet. The main drawbacks of using such tabular hazard descriptions to serve as a communication basis, lie in that: 1) it suffers from a lack of hazard conceptualization that underpins the negotiation of hazards for various stakeholders [2] and, 2) NL hazard descriptions (NLHD) cannot efficiently highlight the information  that  are  of  paramount  importance  for  subsequent risk  reduction  activities  and,  3)  the  NLHD  hinder  to  a  large extent  the  possibility  of  performing  automatic  definition  of hazard mitigation mechanisms. However, there are little pieces of work, aiming to make up for the deficiencies in the current practice.

In  our  earlier  work  [2],  we  have  presented  an  ontological interpretation of the concept of hazard, i.e., the Hazard Ontology (HO).  The  HO  consists  of  a  set  of  hazard-related  concepts, relations, and axioms. In order to interpret hazard in the realworld semantics, the HO is explicitly grounded in the Unified Foundational Ontology (UFO) [6]. The HO aims to achieve a better understanding of the concept of hazard from modelers and model users point of view. A core benefit of understanding the ontological foundation of hazards is that it provides a basis for designing hazard modeling languages [11]. These considerations motivate us to formulate the following research questions: Can we utilize the ontological interpretation of hazard to support the specification of potential hazards identified in the PHA?

In  this  paper,  we  propose  a  hazard  modeling  language (HML) based on the Hazard Ontology. Especially, the contribution of this work is two-fold:

- We propose a hazard modeling language to specify the potential hazards identified in a PHA, and
- We propose  an  approach  to  guide  the  transformation from NLHDs into HML specifications, and

The remainder of this paper is organized as follows: Section II briefly elaborates the Hazard Ontology. Section III presents the  HML  in  detail.  Section  IV  proposes  the  transformation approach, and a running example is given to further illustrate the approach.  Section V  introduces related work,  and  finally concluding remarks and future work are outlined in Section VI.

## II. THE HAZARD ONTOLOGY

The Hazard Ontology (HO) [2] is an ontological interpretation of the hazard concept, which is explicitly grounded in a theoretically well-founded foundation ontology, i.e.,  the  Unified  Foundational  Ontology  (UFO)  [6].  Figure  1 depicts the Hazard Ontology (HO) using a UML class diagram.

The  HO  includes  a  set  of  foundational  concepts  inherited from the UFO. An event is an entity where its constituent parts cannot be present simultaneously. There are two categories of objects, i.e., Kind (e.g., ' a person ') and Role (e.g., ' a driver '). A kind object can play different roles. A relator is a relational property connecting multiple objects. A disposition denotes a property that can characterize an object.  A situation is considered as state of affairs. The constituent parts of a situation can be kind / role objects, relators, and dispositions. For example, in the situation 'a train is approaching a person who is crossing the track', there exist three kind objects (i.e., a train, a person, a track ), two relators (i.e., being-approaching and beingcrossing ), and two kinetic energy dispositions that characterize a  person and a  train ,  respectively.  Two  foundational causal relations are defined between events and situations. A situation can trigger an event and the event will then bring about another situation. The  idea  behind  the  causal  relations  is: 1) the occurrence of an event is the manifestation of a collection of dispositions in a situation and, 2) an event may change reality by changing the state of affairs from one situation to another.

[FIGURE]

Figure1.  The  UML  class  diagram  of  the  Hazard  Ontology.  Concepts  are represented as rectangles. The hazard-related concepts are colored in gray, and the foundational concepts are white. Typed relations are represented by lines with a reading direction pointed by ' ► ',  from open end to aggregated end. Cardinality constraints are labeled on each end of typed relations. Subsumption constraints are represented by open-headed arrows lines with ' ' connecting a sub-concept to its subsuming super-concept. InstanceOf axiom, labeled as insOf , specifies that one concept is an instance of the other concept.

[FIGURE]

The HO provides analysts with a real-world perspective to explain the hazard-related concepts and relations. The main idea behind  the  HO  is  in  line  with  widely  accepted  definitions  of hazards in the context of SCSs [1] [10]. On one hand, the nature of a hazard is a set of states, which motivates the interpretation that a hazard is a type of situation. On the other hand, the states are likely to lead to severe consequences, which is interpreted into the modeling decision that a hazard can trigger mishaps. A mishap is  an  accidental  event  that  will  consequently  cause injuries, damages or significant financial losses. Inspired by the first  idea  behind  the  causal  relations,  the  essential  constituent parts  existing  in  a  hazard  consist  of  mishap  victims,  harm truthmakers, hazard elements, and exposures. A harm truthmaker represents  the  harmful  or  critical  dispositions. When such harm truthmakers are manifested, mishaps are likely to occur. A hazard element denotes the role objects that bear the  harm  truthmakers.  A mishap victim denotes  a  hazard element  that  is  not  supposed  to  but  have  the  potential  to encounter  damages  or  injuries.  An exposure represents  the relations  through  which  mishap  victim(s)  will  be  exposed  to harms posed by hazard elements.

The HO defines that a hazard can be brought about by at least one initiating event. An initiating event denotes an undesirable or unexpected event that can bring about a hazard. An initiating condition represents  a  situation  that  comprises  the  necessary constituent  parts  to  trigger  the  initiating  event.  Furthermore, Initiator Factor and Initiating Role represent the dispositions and roles, respectively, which are necessary constituent parts of an initiating condition to trigger the initiating event.  An environment object is a kind object that can play different roles in  a  hazard  or  initiating  condition.  The cause relation  implies that a pre-initiating event can bring about an initiating condition which will trigger another post-initiating event to bring about a hazard.

## III. THE HAZARD MODELING LANGUAGE

We give the syntax of the hazard modeling language (HML) in  Figure  2  using  Extended-BNF  [12].  We  use  '()'  to  group characters, '?' to represent optional character, '*' to represent empty or repetitive characters, and '|' to represent alternatives. Non-terminals are in italics, and terminals are quoted or derived from '... Name ' non-terminals.

Hazard (line  1)  consists  of  a  mandatory  part  and  three optional parts. HazardName assigns the hazard with a unique name or number. The first optional part defines that there could be more than one initiating event that bring about the hazard. The bring about relation  is  represented  by  '-&gt;'.  The  second optional  part  indicates  that  each  hazard  can  be  expanded  by defining its HazardBody (line 8). The terminal '=&gt;' in the last optional part represents the trigger relation. In particular, each hazard can trigger more than one Mishap (line 2), which consists of MishapName and MishapVictim (line  12).  Note  that  the motivation behind the optional and mandatory definition is twofold: 1) the modeling language is able to provide constructs to fully support the hazard conceptualization defined in the Hazard Ontology  and,  2)  it  supports  partial  specification  in  practice, which  enables  the  HML  specification  being  developed  in  an iterative way.

Figure 2. The syntax of the proposed hazard modeling language.

Each InitiatingEvent (line 3) possesses an InitiatingEventName . It includes two optional parts, one of which defines the initiating condition triggering this event and the other defines event  participants. EventParticipant (line  4),  wrapped  with  a pair of '(' and ')', denotes the role object participating in the initiating event and the EnvObj playing the role. InitiatingCondition (line 5) defines an Initiating -ConditionName to specify the initiating condition that triggers the initiating event. An initiating condition can be expanded by defining initiating roles. An InitiatingRole (line 6) is wrapped with  a  pair  of  '&lt;&lt;'  and  '&gt;&gt;'.  ' InitiatorFactor '  (line  7)  is wrapped with a pair of '&lt;' and '&gt;'. As a disposition, an initiator factor  can  have  an  optional  value,  for  example,  '&lt;Toxicity: High&gt;' means the level of toxicity of a certain material is high.

HazardBody (line  8)  consists  of  two  parts.  The Expo -sureRelName denotes  the  exposure  relation  between  related roles. An ExposureRelRole (line 09) can be a hazard element, a mishap victim, or other roles existing in a hazard. HazardElement (line 10) is comprised of three parts, wrapped with  a  pair  of  '('  and  ')'. HazardElementName assigns  the hazard element with a name. The hazard element can be played by  an EnvObj ,  and  can  be  characterized  by  more  than  one harmtruthmaker. HarmTruthMaker (line 11) has a name and is wrapped with a pair of '&lt;' and '&gt;'. A harmtruthmaker can have an optional value. MishapVictim (line 12) has a mishap victim name and is wrapped with a pair of '(' and ')'. Meanwhile, a mishap victim role can be played by an EnvObj .  An EnvObj (line  13)  can  be  the  name  of  a kind object,  a  ' DEFAULT ' terminal, the negation of an EnvObj, the conjunction or union of EnvObjs.  Especially,  ' DEFAULT '  implies  there  are  certain kind objects that can play the corresponding roles, but not known for  sure  during  the  hazard  modeling  stages,  e.g.,  '(HotParts:

DEFAULT)' means there are certain environment objects are hot parts. The terminals 'NOT', ' ∨ ', and ' ∧ ' applied to EnvObj are standard set operations.

## IV. AN APPROACH TO TRANSFORM FROM NL HAZARD DESCRIPTIONS INTO THE HML SPECIFICATIONS

In  this  section,  we  introduce  the  approach  to  the  transformation from a natural language hazard description (NLHD) into the hazard modeling language (HML) specification. In general, our approach is conducted in three steps as follows:

- Step  1: Hazard  Description  Analysis disambiguates and breaks a NLHD down into different parts, according to the Hazard Ontology;
- Step 3: Hazard Specification Population analyzes the formalized hazard description and captures other important information for the NLHD.
- Step 2: Hazard Description Formalization formalizes the separated parts of the NLHD based on the HML.

We will go into details about each step, and illustrate our approach using a list of identified hazards of a passenger train in the railway industrial, as shown in Figure 3.

Figure 3. The example of NLHD for a passenger train.

## A. Hazard Description Analysis

In practice, a typical hazard description may  merely explicitly describe a part of the knowledge defined in the Hazard Ontology. Therefore, the Hazard Description Analysis step aims to analyze the NLHD in the light of the Hazard Ontology, and accordingly  breaks  the  NLHD  down  into  different  parts.  To perform this step, a set of heuristic questions can be answered, which are listed as follows:

- Q1: ' Does the NLHD describe a situation (state of affairs) or event ?'. Q1 can be asked to determine if the NLHD  describes  a  hazard/initiating  condition  (if  the answer is 'situation') or mishap/initiating event (if the answer is 'event').
- Q2:  ' If  the  NLHD  describes  a  situation,  can  the situation  trigger  mishaps  when  dispositions  in  the situation are manifested ?'. Q2 can be asked to determine if the NLHD describes a hazard (if the answer is yes) or initiating condition (if the answer is no).
- Q3:  ' If the  NLHD  describes  a  situation,  what kind/role objects and properties can be identified in the situation ?'. Q3  can  be asked to inspire the environment objects, hazard element/initiating roles and harmtruthmakers/initiator factors of the NLHD.
- Q4: ' If the NLHD describes an event, can the event bring about losses, injuries or damages ?'. Q5 can be asked to determine if the NLHD describes a mishap (if the answer is yes) or initiating event (if the answer is no).
- Q5: ' If the NLHD describes a hazard situation or a mishap event, who or what will be damaged in the NLHD ?'.  Q6  can  be  asked  to  determine  the  mishap victims of the NLHD.

Figure  4  lists  the  separated  parts  of  the  NLHDs  in  the example hazard list. Note that with the increasing of experience, the list of questions can be further expanded.

## B. Hazard Description Formalization

This  step  is  to  formalize  different  separated  parts  of  the NLHD using the hazard modeling language. The main tasks in

Figure 4. The separated parts of the NLHDs.

## this step are to:

- 1) If the separated part is an event type,  such as initi -ating event or mishap , then the event participants are to be  identified  in  the  form  of  '(EventParticipantName: KindObject)' and a name is given to this part.
- 2)  If  the  separated  part  is  a disposition type,  such  as harmtruthmaker or initiator factor , then the disposition name and its value are to be identified in the form of '&lt;DispositionName: Value&gt;'. The value of the disposition is optional.
- 3) If the separated part is a role type, such as a hazard element , a mishap victim or an initiating role , then the role name and the corresponding kind object are to be identified in the form of '(RoleName: KindObject)'.
- 5)  If  the  separated  part  is  an exposure type,  then  a exposurename is given to the part.
- 4) If the separated part is a situation type, such as hazard or initiating condition , then the part is to be refined into different  roles,  and  the  relation  between  these  roles should be identified as well.

Figure  5  lists  the  formalized  hazards  with  respect  to  the example hazard list. The hazard elements in the Hazard Element column are connected by the exposure.

Figure 5. The formalized parts of the NLHDs.

## C. Hazard Specification Population

The  population  step  will  highly  depends  on  the  results obtained from the Hazard Description Analysis step. We provide some operational guidelines as follows:

- 1) For each NLHD, the corresponding mishap should be defined at first.
- 2) If the NLHD describes a hazard that can directly lead to  mishaps,  then  the hazard should  be  refined  into hazard element s,  and  the  relation  between  the  roles should be identified.
- 3)  If  the  NLHD  describes initiating event s,  then  the subsequent hazards should be defined and further formalized.
- 5) If hazard eleiments are identified in the NLHD, the harmtruthmakers that  characterize  the hazard element should be identified.
- 4)  If  the  NLHD  describes  an initiating condition ,  the initiating  condition  should  be  refined  into initiating roles and initiator factors . Then the subsequent hazards should be defined and then refined.
- 6) If the NLHD describes harmtruthmakers , the hazard elements bear the harmtruthmakers should be defined.
- 7) For each role entity, the corresponding kind object(s) should be defined.

Figure  6  lists  the  populated  hazards  with  respect  to  the example hazard list.

Figure 6. The populated parts of the NLHDs.

## V. RELATED WORK

Winther et al. [13] propose an ontological conceptualization of hazard to address the confusion concerning what are called hazards. Different from ours, they regard a hazard as an event or state at the boundary of a system that can lead to an accident. In our ontology, a hazard is regarded as a situation.

Lawrynowicz et al. [14] describe an ontology design pattern for modeling hazardous situations. They take some foundational concepts (such as object, event) into account as well, but their work is  not  grounded  in  well-founded  foundational  ontology. Therefore,  some  concepts  suffer  from  a  lack  of  real-world semantics.

Daramola et al. [15] presents a framework and tool prototype that facilitates the early identification of  potential  system hazards. A HAZOP ontology is defined in the framework, which consists of types of study node, description,  guidewords, deviations,  causes,  consequences,  risk  level,  safeguards,  and recommendation. Their main objective is, different from ours, to discover potential hazards.

## VI. CONCLUSION AND FUTURE WORK

In this paper, we have proposed a hazard modeling language (HML)  based  on  the  Hazard  Ontology,  to  formalize  nature language hazard descriptions (NLHDs). In this way, we aim to provide  a  structured  and  unambiguous  hazard  specification which can facilitate the communication and negotiation between various stakeholders in the PHA. Furthermore, we propose an approach to transformation from  the  NLHDs  into  HML specification,  in  terms  of  hazard  description  analysis,  hazard description  formalization,  and  hazard  description  population. Meanwhile, the approach is illustrated  using  a  list  of  hazards identified in the PHA for a passenger train.

This work is an extension to our previous work [2]. Our next plan  is  to  conduct  an  industrial  case  study  to  evaluate  the expressiveness of the proposed modeling language and improve it. In addition, it will be of great interest to explore the possibility of  using  a  formal  hazard  specification  as  a  starting  point  to facilitate the process of defining hazard mitigation mechanisms. Finally,  tooling  support  is  considered  as  an  essential  part  of future work as well.

## ACKNOWLEDGMENT

Our research is supported by the Dependable Platforms for Autonomous systems and Control (DPAC) project through the Knowledge Foundation (KKS).

- [1] N. G. Leveson, Engineering a Safer World: Systems Thinking Applied to Safety . The MIT Press, 2011.
- [2] J.  Zhou,  K.  Hänninen,  Y.  Lu,  K.  Lundqvist,  and  L.  Provenzano,  'An Ontological Interpretation of Hazard for Safety-Critical Systems,' Proceedings of ESREL'17 , 2017.
- [3] F. Crawley, M. Preston, and B. Tyler, HAZOP: Guide to Best Practice: Guidelines to Best Practice for the Process and Chemical Industries , 2000.
- [4] R.  Mader,  G.  Griessnig,  A.  Leitner,  C.  Kreiner,  Q.  Bourrouilh,  E. Armengaud, C. Steger, and R. Weiss, 'A Computer-Aided Approach to Preliminary  Hazard  Analysis  for  Automotive  Embedded  Systems,'  in Proceedings of ECBS'11 , 2011, pp. 169-178.
- [5] C.  Fleming, Safety-driven  Early  Concept  Analysis  and  Development , 2015.
- [6] G. Guizzardi, Ontological Foundations for Structural Conceptual Model, 2005.
- [7] H. Herre, B. Heller, P. Burek, R. Hoehndorf, F. Loebe, and H. Michalek, 'General Formal Ontology (GFO): A Foundational Ontology Integrating Objects and Processes. Part I: Basic Principles (Version 1.0),' Tech. Rep., 2006.
- [8] R. Arp, B. Smith, and A. Spear, Building Ontologies with Basic Formal Ontology . MIT Press, 2015.
- [9] C.  Masolo,  S.  Borgo,  A.  Gangemi,  N.  Guarino,  and  A.  Oltramari, 'Ontology Library,' in WonderWeb Deliv . D18, 2003.
- [10] MIL-STD-882, 'DoD Standard Practice for System Safety, version D,' 2000.
- [11] R. S. S. Guizzardi, F. Li, A. Borgida, G. Guizzardi, J. Horkoff, and J. Mylopoulos, 'An Ontological Interpretation of NonFunctional Requirements,' in Proceedings of FOIS'14 , 2014, pp. 344-357.
- [12] ISO/IEC14977:1996(E), 'Information technology-Syntactic metalanguage - Extended BNF,' 1996.
- [13] R.  Winther  and  W.  Marsh,  'Hazards,  accidents  and  events-a  land  of confusing  terms,'  in Safety,  Reliability  and  Risk  Analysis  Beyond  the Horizon , 2013, pp. 2545-2553.
- [14] A. Lawrynowicz and I. Lawniczak, 'The Hazardous Situation Ontology Design Pattern,' in Proceedings of WOP'15 , 2015.

̊

- [15] O.  Daramola,  T.  Sta lhane,  G.  Sindre,  and  I.  Omoronyia,  'Enabling Hazard  Identification  from  Requirements  and  Reuse-Oriented  HAZOP Analysis,' in Proceedings of MARK'11 , 2011, pp. 3-11.
