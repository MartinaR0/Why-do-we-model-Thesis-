## Towards a Collaboration Ontology

Felipe F. Oliveira 1,2 , Julio C. P. Antunes, 1,2 , Renata S. S. Guizzardi 2.

1 zAgile Inc., San Francisco, California, USA

2 Informatics Depart., Federal University of Espírito Santo (UFES), Vitória (ES), Brazil

```
{felipefo, jcpantunes)@zagile.com , rguizzardi@inf.ufes.br
```

Abstract. Collaboration is a complex and essential process for organizations. Ontologies can provide a way to promote software tool integration, by serving as  a  common  conceptualization  among  these  tools.  This  integration  may ultimately  lead to  lower  costs and  improved  flexibility  and  revenue  in business. This paper presents a collaboration ontology based on the structure defined by the 3C Model and shows how it can be used to promote integration among collaborative software tools.

## 1. Introduction

Organizations use collaboration as a method to exchange information inside and across their boundaries. It is believed that organizations that collaborate efficiently have greater revenue  than  their  competitor  [The  Global  Ceo  Study  2006].  In  fact,  collaboration reduces transaction costs  between  organizations.  With  this in mind, organizations can create  business  models  extremely  specialized  that  can  combine  a  set  of  services provided by collaboration among organizations.

Given the importance of the topic, it is crucial to conceptualize and formalize a common vocabulary to represent collaboration.  Therefore, in this paper, we present a collaboration ontology based on the structure defined by the 3C Model (communication, coordination and cooperation) [Ellis et al. 1991]. This ontology is being developed to formalize  knowledge  about  the  domain  in  order  to  provide  a  common  vocabulary, promoting integration within the collaboration domain . We propose this ontology as the means  to  integrate  several  collaborative  software  applications  aiming  at  effectively collaboration support within organizations.

An  overview  of  the  proposed  method  to  support  collaborative  software  tools integration is  illustrated  in  Figure  1.  The  Figure  shows  that  the  conceptual  models  of each tool are mapped into the collaboration ontology model, meaning that ideally, each concept in the tool can be mapped directly to one concept in the ontology, in order to promote semantic meaning integration. The figure also highlights that non-collaborative tools  (e.g.,  the  project  management  tool  in  Figure  1)  may  also  be  integrated.  In  other words, in this case, we can find points of integration between the collaborative tools and the  project  management  tool,  such  as  activities  that  are  assigned  to  one  user  in  the project  management  tool  and  participation in  a  forum  that are  performed  in  the  same period of time.

Figure 1. An Overview of the mapping between the collaborative tools' conceptual models and the collaboration ontology

[FIGURE]

In  the  next  section,  we  present  a  brief  description  about  the collaboration domain .  Section  3  shows  the  methodology  used  here  to  build  the  Collaboration Ontology  and  the  method  used  to  give  semantics  for  collaboration  tools.  Section  4 presents  the  ontology,  including  the  competence  questions,  concepts,  properties  and relations  between  these  concepts.  Section  5  employs  an  application  for  this  ontology, mapping the conceptual model of a tool in order to exemplify how the ontology can be mapped to it. Moreover, this section presents a mapping to a Framework called LEICA 1 that provides integration among collaborative and non-collaborative applications. This is done in  order  to  show  the  behavior  of  the  Ontology  when  mapped  for  a  generic tool integration  framework.  Section  6  discusses  some  future  works  and  presents  the conclusion of this paper.

## 2. Collaboration Domain

In the business world, one of the most critical processes is collaboration. Be it e-mail, instant  messaging,  virtual  workspaces,  videoconferencing,  collaborative  text  edition, shared  white  boards  or  case  tools,  technology  dramatically  shortens  distances  among people  and  frees  up  the  flow  of  intellectual  capital,  enabling  employees  to  work,  to capture  and  to  share  knowledge  more  quickly.  The  most  important  gain  of  the information  exchanged  among  workers  is  achieving  greater  gains  in  revenue  growth, operating margins and productivity [IBM Global Services 2006].

A collaboration session (CS) is a kind of event that represents (loosely speaking) a period of time in which some agents collaborate with each other for a given purpose. There  are  some  important  concepts  related  to  a CS ,  such  as:  participants,  objectives, artifacts, coordination and communication.

Participants are the agents that can contribute in a meaningful way to achieve the objectives of the session. The objectives are the states of affairs the participants aim at achieving in the end of this particular CS .  Cooperation and interaction depend on the commitments  of  each  of  the  participants.  In  addition  to  that,  collaboration  involves sharing of specific information among members of a group that cooperate to create or consume information.

1 Loosely-coupled Environment for Integrating Collaborative Applications

According to Nguyen et al. (2005), the purpose of the concept of collaboration artifact is  to  serve  as  a  bridge  that  connects  agents  and  software.  This  means  that  a collaboration artifact provides a shared workspace for the participants. Participants can exchange data with peers as well as with agents that did not participate in the CS . This creates a kind of record that can help to re-construct the experiences of the CS , which most of times is only 'recorded' in the agent's mind.

In collaborative work, cooperation is a joint effort in a shared space to achieve some  goal.  To  avoid  implicit  rules  and  uncontrolled  behaviors  in  a CS ,  participants should  know  the  rules  and  procedures  defined  for  the CS. Hence,  these  rules  and procedures  must  be  very  explicit,  defined  in  a  way  that  makes  each  participant comfortable to use and contribute to the CS in  a  meaningful  way.  This  motivates  the need for a formal protocol, commonly known as coordination, defined by the Webster dictionary [Merriam 2007] as the harmonious functioning of parts for effective results. In other words,    coordination can be described as a layer that mediates the communication and the cooperation, to enforce the success of collaboration.

Coordination services support management and enforcement of group activities [Fuks et al. 2005]. After all, how can people collaborate without coordination? Without coordination, people will usually engage in conflicts or repetitive actions. Due to that, coordination is essential to solve problems that share common objectives, resources and activities  [Ellis  et  al.  1991].  In  fact, we  here  generalize  this by stating that one of the most important  prerequisite  to  accomplish  collaboration  goals  is  coordination.  For  an organization, the main objective of coordination is to execute the project scope without exceeding limits of time and cost, while maintaining quality.

Another point  worth  mentioning  is  the  relationship  between  collaboration  and communication  [Fuks  et  al.  2003].  Communication  is  the  basis  to  any  collaborative system.   The objective of communication is to exchange knowledge among individuals. To transmit content, the sender expresses his intentions or goals, defined by symbols in a language that must be understood by all receivers. Moreover, information transmission needs to be accomplished by a communication media [Fuks et al. 2005].

A  communication  action  involves  interaction  among  individuals,  (agents  that can be messages' senders and receivers), a dialog event (an event characterized by the exchange information through messages), a context (a situation in which the communication occur) and a protocol (a set of rules that coordinate the communication). Moreover, a communication action generates commitments that create new objectives [Winograd and Flores 1987]. To achieve these goals, through a set of individual tasks, it is necessary to coordinate the activities necessary to carry through the commitments. It supports the group to manage their information.

## 3. The Ontology Development Methodology

Domain ontology captures the common sense of a particular domain in a generic and formal way to improve reuse and sharing through applications and groups [GómezPérez et al.  2004]. In other  words, it  defines  a  specific vocabulary used to describe a portion  of  reality.  A  domain  ontology  should  have  a  representation  that  captures concepts, relations and their properties in a domain, and a set of axioms that constraint their interpretation [Guarino 1998].

In  this  article,  we  have  adopted  the  following  Ontology  development  strategy. Firstly,  the  SABIO  ( Systematic  Approach  for  Building  Ontologies) methodology  has been employed [Falbo 2004]. SABIO proposes a method of ontology development and coordination process whose  life cycle has the following  steps: (i) purpose  and requirements specification: identifying the ontology's objective (or purpose), application area and competence (through competence questions); (ii) ontology capture: capturing of the concepts of the domain, along with  their relations and properties; (iii) ontology formalization: representing the formalization of the conceptualization captured in the previous step; (iv) reuse and integration with existing ontologies: integrating with ontologies  already  available; (v) Evaluation:    verifying  if  the  developed  ontology accomplishes  its  purpose; (vi) Ontology  documentation:  recording  all  knowledge gathered in the process of ontology development.   These steps are organized in an interactive life-cycle [Falbo 2004].

For  the  purpose  of  representation,  the  SABIO  methodology  suggests  the application  of  a  graphical  language  named  LINGO  which  in  [Falbo  2004]  has  been implemented as a UML profile. However,  in  [Guizzardi  2005]  proposes  a  much  more expressive extension to UML. The latter represents (among other things) a number of distinctions betweens different types of classifiers (depicted in figure 2). Thus, to create the conceptual representation of our collaboration ontology, we have used the language proposed by [Guizzardi 2005].

Figure 2. Part of a typology of classifiers [Guizzardi 2005]

[FIGURE]

In this model, 'Type' represents the most abstract sort of classifier. An object type is a type whose instances are entities that exist in time while maintaining their identity (e.g., a car, a person). In contrast, an event type is a type whose instances happen in time by unfolding its temporal phases (e.g., a football game, a business process, a conversation). A sortal is an,object type which carries a proper identity criterion for its instances. An identity criterion can be defined as some property necessary and sufficient to define the identity of that individual. An object type which is not a sortal is named a mixin .

Sortal types are divided into rigidSortal and antiRigidSortal that are defined by the rigidity property.  In simple terms, a type T is said to be rigid if every instance x of T is necessarily (in the modal sense) an instance of T. Conversely, a type T is anti-rigid if every instance x of T is possibly (in the modal sense) not an instance of T, i.e., if x can cease  to  instantiate  T  without  ceasing  to  exist  [Guizzardi  2005].  A  typical  example highlighting this distinction is given by the types person and employee, both instantiated by the individual Lisa in a given circumstance. While Lisa can cease to be an employee of Xerox (and there were periods of time in which Lisa was not one), she cannot cease to  be  a  person.  Thus  person  is  a rigidSortal while  employee is  an antiRigidSortal .  A rigidSortal that supplies a principal of identify for its instances is named here a kind . A rigidSortal that inherit the identity criterion supplied by a kind is named here subKind . The figure still defines role and phase as subtypes of antiRigidSortal .  A role type is a type  that  instances  of  a  kind  instantiate  in  a  given  context  (e.g.  the  employee  type mentioned  above).  Another  example  is  the  role  type  student:  student  is  a  type contingently  instantiated  by  people  when  registered  in  an  educational  institution.  A phase , in contrast, is a type instantiated contingently by instances of a kind when these instances have specific values for a set of its intrinsic properties. Examples include alive and decease as two possible phase types of the kind person.

In  an  analogous  way,  a mixin object  type  is  classified  as rigidMixin and nonRigidMixin . A rigidMixin which is instantiated by individuals of different kinds that share a common essential property (i.e., a property that they must not lack) are named category .  For  example,  an  agent  is  classified  as  a category ,  since  different  kinds  of individuals like person or organization are instances of the type agent. An antiRigidMixin describes accidental properties shared by individuals of different kinds. A roleMixin is an antiRigidMixin that describes common properties of different types of roles  (instantiated  by  instances  of  different  kinds).  Examples  of roleMixins include formal roles as whole and part but also examples such as Customer (which has instances persons and organizations).

Many other concepts are defined in [Guizzardi 2005], however in the scope of this paper we just use the ones presented above.

## 4. The Collaboration Ontology

Following the structure of the 3C Model, we divide the Collaboration Ontology in three sub-ontologies:  Cooperation,  Communication  and  Coordination  Ontology.  Figure  3 describes the relation among Ontologies within the Collaboration Domain, according to the  discussion  presented  in  section  2.  This  paper  presents  only  the  Cooperation  and Communication Ontologies, while the Coordination Ontology is left as future work.

Figure 3. The Ontologies that comprise the Collaboration Ontology

[FIGURE]

To collaborate, the individuals have to exchange information (communication) and  to  organize  themselves  (coordination)  to  work  together  in  a  same  workspace (cooperation) [Fucks et al. 2005].

As previously  mentioned,  the ontologies  proposed  are developed based on the SABIO  approach.  We  begin  with  the  first  SABIO  step,  developing  the  competency questions, i.e. questions that the ontology should be able to answer. These competency questions  identify  the  purpose  of  our  Collaboration  Ontology,  thus  summarizing  the discussions proposed in section 2. Here they follow:

- CQ  1 - What are the artifacts of a CS ?
- CQ  2 - Who are the participants of a CS ?
- CQ  3 - What are the objectives of a CS ?
- CQ  4 - When and where a CS happens?
- CQ  5 - What are the rules of a CS ?
- CQ  6 - What kind of artifact a CS generates?
- CQ  7 - What kind of participants a CS has?
- CQ  8 - How the collaborations artifacts are generated?
- CQ  9 - Who are the participants of a communication action?
- CQ 10 - What is the protocol of a communication action?
- CQ 11 - What is the language used to exchange messages among agents?
- CQ 12 - What is the context of a communication action?
- CQ 13 - What is the media used on a communication action?

Figure 4 shows the Cooperation Ontology.

Figure 4. The Cooperation Ontology

[FIGURE]

A collaboration session ( CS )  is  an  event that is composed of the actions of its participants . These actions are instantaneous events ( atomic event ) and they are named here participations (e.g., the action of sending or receiving a message). A participation is performed by a participant and a participant can have one or more participations . A CS has  one  or  more objectives ,  defining  its  main  purpose  or  goal.  An objective can depend  on  other objectives and  each  one  have  a  priority  level  according  to  its importance for that CS . Besides, the CS can consume or generate artifacts, defined here as collaboration artifact . Finally, the CS happens in a place, defined in the model above as a site .   The  actions of a CS need some kind of coordination. In the presented model, this is represented by the concept of protocol . However, as aforementioned, we hope to develop, in the future, a coordination ontology to treat this matter in more detail.

Following the SABIO approach, a term dictionary was elaborated, with one entry for each concept. Table 1 presents a short dictionary of the Cooperation Ontology.

Table 1. Part of the terms dictionary for the Cooperation Ontology

| Collaboration Artifact   | Designates the object that can be either generated or consumed by the collaboration session.                  |
|--------------------------|---------------------------------------------------------------------------------------------------------------|
| Collaboration Session    | Denotes in an event in which participants interact for the purpose of collaboration                           |
| Objective                | Denotes the motivation of the collaboration session, in others words, a reason that motivates its occurrence. |
| Participant              | An agent that can contribute in a meaningful way to achieve the objectives of the Collaboration Session.      |
| Participation            | Denotes an atomic event that one participant executes in a collaboration session.                             |
| Protocol                 | Designates a set of rules which establish coordination for the harmony of the collaboration session.          |
| Site                     | Denotes a place that hosts the Collaboration Session                                                          |
| VirtualSite              | Denotes an electronic environment which mediates the Collaboration Session.                                   |
| RealSite                 | Denotes a place in the real world in which the Collaboration Session is held.                                 |
| Collaborative Action     | Denotes a participation in a collaboration session without the exchange of a message                          |

During  a CS ,  the participants exchanges  information.  This  is  carried  out  by performing send  and  receive participations ,  which  in  turn,  are  essential  parts  of communication  actions .  These  concepts  are  defined  in Communication  Ontology depicted in Figure 5.

Figure 5. The Communication Ontology

[FIGURE]

A communication action is composed of two participations executed by agents . Each participation event has one message that represents the exchanged information. A m essage is expressed through a language . It also uses one communication media that is the instrument used to carry out communication.

Table  2  presents  the  dictionary  of  the  communication  ontology,  describing  its main concepts:

Table 2. Part of the terms dictionary for the Communication Ontology

| Communication Action   | Denotes an act of communication between two or more agents.   |
|------------------------|---------------------------------------------------------------|
| Message                | Denotes the content of a participation of an agent.           |
| Send                   | Denotes the event of sending a message.                       |
| Receive                | Denotes the event of receiving a message.                     |
| Agent                  | performing some (potentially) useful function [Guizzardi      |
| Language               | Designates the language in which the message is expressed     |

Besides the models presented in Figures 4 and 5, some axioms must be defined for these ontologies. These axioms are classified in consolidation and derivation axioms. Consolidation axioms describe the restrictions of the relations  among  concepts structured in the models. Derivation axioms are developed to answer to the competence questions. In this paper, for illustration purposes, we present two axioms, one of each of these  types.  In  order  to  answer  to  the  competence  question  (CQ2)  we  present  the following derivation axiom:

∀ x,y collaborationSession(x) ∧ agent(y)

→

( participant\_of(y,x) ↔ ∃ z participation(z) ∧ partOf(z,x) ∧ executes(y,z) )

In  the  Communication  Ontology,  to  execute  one  communication  action,  the  receiver must receive the one message previously sent by the sender. Here is the consolidation axiom showing this constraint:

∀ x,y,z communicationAction(x) ∧ send(y) ∧ receive(z) ∧ partOf(y,x) ∧ partOf(z,x) → (precedes (y,z) ∧ ∀ m1,m2 message\_of(m1,y) ∧ message\_of(m2,z) → m1 = m2)

## 5. Some Applications of the Collaboration Ontology

Traditional systems have in the information source layer different understanding about the  domain  knowledge.  Each  system  uses  its  own  language  or  syntax  to  represent knowledge which forms their respective local semantic schema [Gu 2004]. In face of that, the collaboration ontology becomes useful to provide a common language (both in terms of syntax and semantics) in order to promote interoperability. To illustrate that, we define mappings from concrete tools to the ontology developed. First, we present a mapping  the  forum  module  of  Drupal 2 to  this  ontology.  Then,  a  mapping  of  a framework that promotes integration among collaborative and non-collaborative tools.

## 5.1 Mapping the Forum Module of Drupal

Figure 6. Mapping Drupal's Forum Module to the Collaboration Ontology

[FIGURE]

Drupal is a content management system that provides modules useful for collaboration such as: forum, blog, book and so on. Figure 6 shows a mapping from the forum module of Drupal to our Collaboration ontology. In this figure, concepts from Drupal's Forum Module are depicted in grey. This mapping defines the semantics of Drupal's concepts in terms of the notions defined in the ontology.   There  are,  however,  concepts  that  are not directly mapped to the ontology because most of tools have their own specializations, i.e., concepts which are tool specific.

2 Drupal: http://drupal.org

## 5.2 Mapping the Collaboration Ontology in LEICA

LEICA is a framework that supports the integration of collaborative tools. It is based on loosely-coupled  integration,  which  means  that  the  integrated  tools  do  not  loose  their own autonomy. Two collaborative  tools  are here  used to explain how  LEICA  works. The  first  cooperative  tool,  CoLab  is  a  co-browsing  application.  The  second  tool, Babylon  is  a  multi-chat  tool.  In  this  example,  these  tools  are  integrated  by  LEICA. Figure  7  shows  one super-session in  LEICA,  in  which  user  'D'  joins  the  same subsession of user 'F' inside CoLab, transforming it in only one sub-session inside CoLab. After  this,  a  collaboration  rule  defined  in  LEICA  is  fired  and  moves  all  users  that belongs to this sub-session of 'D' in CoLab to the same sub-session in Babylon chat of 'F' automatically [Gomes et. al. 2006].

Figure 7- When user 'D' joins the CoLab sub-session of 'F' he is automatically moved to the same chat-room of 'F' in Babylon

[FIGURE]

Figure 8 shows how we map the conceptual model of the LEICA framework into the  collaboration  ontology.  Once  more,  the  gray  concepts  correspond  to  concepts  in LEICA.

Figure 8- Mapping between the LEICA framework to the Collaboration Ontology

[FIGURE]

## 6. Conclusion and Future Works

Collaboration processes have a significant impact in the context of business organizations and are crucial processes to improve revenue and competition. Due to that a  Collaboration  Ontology  is  presented  here  using  the  method  SABIO.  The  modeling language proposed by [Guizzardi 2005] is used to represent the Ontology.

In order to exemplify the usefulness of the collaboration ontology proposed here, a mapping has been demonstrated describing how a conceptual model of a collaboration tool can be integrated with the Ontology proposed. In the same way, other conceptual models  could  be  integrated  by  the  Collaboration  Ontology.  The  LEICA  conceptual model was mapped in the Ontology, in order to demonstrate how the Ontology covers a generic collaborative framework.

The  ontology  proposed  here  should  be  seem  as  an  initial  attempt  to  define  a model in this domain. In particular, it still lacks concepts related to coordination subdomain,  which  is  deemed  here  as  a  fundamental  part  of  a  Cooperation  Ontology. Concepts like group, protocol and roles will be provided by this ontology, which is the next step in our research agenda.   Another  point  to  focus  is  the  integration  with  upper level Ontologies in other to improve both its expressiveness and generality.

In  many  practical  situations,  a  collaboration  artifact  is  controlled  by  access control mechanisms since some organizations have strict restrictions imposed to the use of  particular  some  artifacts  (e.g.,  confidential  documents  and  information).  As  future work, we intend to integrate this collaboration ontology with a Software Configuration Management Ontology. This will provide means for among other things constraining the access of each participant to a given collaboration artifact.

## Acknowledgements

The work of the first two authors in this article has been supported by zAgile Inc. As consequence,  the Collaboration  Ontology published  here  is  intellection  property  of zAgile  Inc.  zAgile  grants  permission  for  this  ontology  to  be  used  for  all  Academic Purposes.  We  would  like  to  thank  Giancarlo  Guizzardi,  Roberta  Lima  Gomes  and Sanjiva Nath for fruitful discussions and for providing valuable input to the issues of this article.

## References

- Ellis,  C.  A.,  Gibbs,  S.  J.,  and  Rein,  G.  (1991).  'Groupware:  some  issues  and experiences'. Commun. ACM 34, 1 (Jan. 1991), 39-58.
- Falbo, R. A, (2004). 'Experiences in Using a Method for Building Domain Ontologies'. Proc.   of International Workshop on Ontology In Action, Banff, Alberta, Canada.
- Fuks, H., Raposo, A. B. and Gerosa, M. A. (2003). 'Do Modelo de Colaboração 3C à Engenharia  de  Groupware'  -  Pontifícia  Universidade  Católica  do  Rio  de  Janeiro (PUC-Rio).
- Fuks,  H.,  Raposo,  A.B.,  Gerosa,  M.A.  and  Lucena,  C.J.P.  (2005).  'Applying  the  3C Model to Groupware Development'.
- Gomes, R.L., Hoyos-Rivera, G.J., Courtiat, J.P (2006). "Um Ambiente para Integração de  Aplicações  Colaborativas".  Simpósio  Brasileiro  em  Sistemas  Colaborativos, (SBSC'06). Natal, Brasil, 2006.
- Gómez-Pérez, A., Fernández -  López,  M.  and  Corcho-Garcia,  O.,  (2003).  'Ontological Engineering - with examples from the áreas of knowledge management, e-  commerce and the semantic web'. Ed. Springer, p.107-153
- Gu, Jinguang, et al. (2004) 'OBSA: Ontology-based Semantic Information Processing Architecture', Proceedings of the 2004 IEEE/WIC/ACM International Conference on Web Intelligence, IEEE Computer Society   Washington, DC, Pages: 607 - 610
- Guarino, N. (1998). 'Formal Ontology in Information System'. In: Proceedings of the First Int. Conference on Formal Ontology in Information Systems, Trento, Italy, June. p.3-15.
- Guizzardi, G. (2005). 'Ontological Foundations for Structural   Conceptual Models'       , Telamatica Instituut Fundamental  Research Series,  ISBN  90-75176-81-3, The Netherlands.
- Guizzardi, G  (2007). 'On  Ontology, ontologies, Conceptualizations, Modeling Language and (Meta)Models', Federal University of Espirito Santo, Vitoria, Brasil Laboratory for Applied Ontology, Trento, Italy.
- Guizzardi,  R.  S.  S.  (2006).  'Agent-oriented  Constructivist  Knowledge  Management'. PhD thesis, University of Twente, The Netherlands.
- IBM  Global  Services  (2006).  'Using  collaboration  to  enable  the  innovators  in  your organization'. [online:www.ibm.com], captured in 2007
- Merrian-Webster Dictionary, [online:www.webster.com], captured in 2007
- Nguyen, A. V., Rekik, Y., Gillet, D., (2005) 'A framework for sustaining the continuity of  integration  in  Web-based  learning  environment  for  engineering  education'.  In Proceedings of the World Conference on Educational Multimedia, Hypermedia and Telecommunications  (ED-MEDIA  2005),  (C)  AACE,  Montreal,  Canada,  June  27July 02, 2005
- The Global CEO study (2006). 'Expanding Innovation Horizon'. [online: www.ibm.com], captured in 2007
- Winograd, T., Flores, F., (1987). 'Understanding Computers and Cognition', AddisonWesley, USA.
