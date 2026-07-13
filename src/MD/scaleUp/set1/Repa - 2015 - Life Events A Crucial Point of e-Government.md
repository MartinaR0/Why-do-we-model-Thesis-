## Life Events: A Crucial Point of e-Government

Vaclav Repa ( B )

Faculty of Informatics and Statistics, University of Economics, Prague, W. Churchill Sqr. 4, 13067 Prague, Czech Republic repa@vse.cz

Abstract. Life events (life situations) are usually understood as a specific view on public administration activities which is close to their clients: citizens. This view usually helps to effectively and client-friendly organize the web platform of the public authority. However, the real meaning of life events is more essential. Such a view allows regarding the public administration activities as consequences of real events in real lives of the public administrations clients. This paper introduces an approach to the analysis of life situations in the context of life cycles of the public administration objects and the use of this approach in a real ongoing project. The relation of life events to the public administration processes as well as their relation to e-government are discussed and illustrated with examples from the project.

Keywords: Life event · Object life cycle · Public administration · Conceptual modeling · Process-driven management

## 1 Introduction

Effectiveness in the field of public administration always has been a hot topic for politicians. It seems that what is called the 'black hole for public finances' is a natural attribute of this area. The advances in technology paradoxically even worsen the situation; so called e-government often leads to large investments without an adequate effect which would justify them. However, these problems are first of all a great challenge for the management theory researchers. It is obvious that the problem is rooted not in the infrastructure (IT) but in the management itself. E-government is defined in [1] as: 'the use of ICTs as a tool to achieve better government'. The impact of e-government at the broadest level is simply better government 'e-government is more about government than about 'e' ' [10]. This idea became widespread as noted in many other sources: [9,11].

Once we accept this idea, we need to answer the consequential question: what are the changes that e-government should offer in order to 'achieve better government' and how to make them? The origin of this question is the same as in case of business process re-engineering in market oriented companies as defined in [3]. It is about how to use technology to make the public authority flexible enough to be able to change its internal behavior to conform to the changes in the environment. Thus, it seems that to achieve the ideal effects of

c © Springer International Publishing Switzerland 2015

e-government as stated in [10], the concept of process-oriented management in the field of public administration should be applied.

Unlike in market-oriented businesses, the application of general management principles in public administration poses considerably harder problems. The cause is in particular the absence of the market. The absence of the market causes the need for using a great amount of abstraction to implement general management principles in this field. Questions as 'who is a customer?' or 'what is the customer's interest?' are typically not easy to answer here. The difficulty of using general management practices in this business is visible best in the context of business processes, especially in their re-engineering. These problems manifest themselves specifically in identifying core processes.

While implementing process-driven style of management, the critical success factors of the public administration are:

- -Primary function of public administration (what are the main 'strategic' goals of public administration activities?) is very abstract. The best illustration of the needed amount of abstraction are the following questions:
- Who is a 'customer' of public administration? Obviously it is not only a citizen. The community itself or enterprise and other 'actors' in the field of the community life are additional specific types of customers.
- What are a 'customer needs' in the area of public administration? There are often more interconnected 'needs' that may be mutually in conflict in this area.
- How do these 'customer needs' manifest themselves? As many needs are not in the form of explicitly expressed 'requirements', it is necessary to systematically analyze different factors of the situation to uncover them. Moreover, the precise knowledge of the general context is often necessary to uncover the needs in this area.
- -The field of public administration is typically tied to the legislation which is neither perfect, nor consistent. At the same time, the legislation is traditionally regarded as an expression of basic values, in other words as a substitution of the primary function. This fact makes the analysis of the roots of the strategic values in this area very complicated and cumbersome especially if there exists some resistance against possible changes ('You are not allowed to revise the legislation!', 'It is against the law!').

The consequence of both aforementioned factors is the fact that the idea of main strategic values of a community is not commonly accepted and that there are strong mental as well as legislative barriers which have to be overcame while uncovering the primary function of public administration. On the other hand, to shift the conception of management activities from the traditional to the process-oriented one we need in the first place to define its primary function 'what should be the main purposes and goals of public administration activities'.

The main purpose of this paper is to introduce the specific approach to overcome the crucial problems of public administration and e-Government as stated above based on the fundamental analysis of life events (situations).

Life events of the public administration objects are analyzed in the context of their life cycles. Life cycle describes the universal context of the group of life events that characterizes the given object in terms of their causal and time dependencies. It brings the essential information about what may (and may not) happen in the life of the given object in the given context. We use this information as a basis for the analysis of the essence of the needed public administration actions. The result of this analysis is intended to be used for the conception of essential public administration processes, i.e. processes which are undoubtedly necessary for objective reasons. The approach introduced in this paper has been used in the real analysis project managed by the Czech Ministry of Interior. We use the experience from this project for the discussion of the crucial features of the concept of application of the process-driven management in the field of public administration as well as its consequences. We argue that life events should be regarded as a crucial point of the analysis in the field of public administration for the purpose of the application of e-government.

The paper is organized into the five sections. In the second section, immediately after this introduction, we explain the methodology background. We briefly characterize the MMABP methodology as the basic source of the main principles and techniques for information organizational modeling as well as the PARMA project as a source of the approach to the application of the process-driven ideas in public administration. Finally, the concept of life events and its relationships to other basic public administration aspects are explained. It the third section we describe the project, its context, and the way in which this methodology approach has been used there. Fourth section contains the main discussion of the experience from the project and some generalization of this experience. In the conclusion section we summarize the main ideas of this paper and point out the needed future work.

## 2 Methodology Background

In the project described in the following section we use two main methodology resources:

- -MMABP (Methodology for Modeling and Analysis of Business Processes)
- -PARMA (Public Administration Reference Model and Architecture)

MMABP is a methodology for information modeling of organizations. Its goal is to create a precise model of the 'Real World' as the basis for any consequent infrastructure (such as the information or organization system). The methodology has been originally developed for the purpose of the application of the ideas of processes -driven management (see [3]). Nevertheless, it covers all important dimensions of the information model of an organization (see Fig. 1).

MMABP uses four basic types of models derived from the combination of two basic organizational viewpoints:

- -Ontological view focused on the description of the causality in the Real World. Models in this view express the main objects which the Real World consists of, their relationships and rules for their dynamics.

Fig. 1. Types of particular models in the MMABP

[FIGURE]

- -Behavioral view focused on the description of the intentionality in the Real World. Models in this view express the main processes of the Real World and their relationships.

Each view is represented by two types of models:

- -Global (system) view that look at the system as a whole. This type of models is oriented on the static aspects of the system its parts and their relationships.
- -Detailed view looking at just one essential part of the system in the proper detail. This type of models is oriented on dynamic aspects of the system. Such aspects can sufficiently describe just one part of the system.

Only the ontological models are relevant for the purpose of this paper. Therefore, the methodology uses two essential UML diagrams for the two basic types of models:

- -Class Diagram for the description of the global contextual view on objects in the given area.
- -State Chart for the description of how one particular object can change during its life cycle.

MMABP applies these two models is based mainly on the following theoretical resources: the conceptual modeling with the UML [7] and the work of M. Jackson [5,6]. More detailed information about the MMABP methodology can be found in [12].

PARMA (Public Administration Reference Model and Architecture) [13] is a long-term project aimed at the application of the process-driven management concepts in the field of public administration. This project resulted in a set of essential principles where the central point are life events as described in the following sub-section.

## 2.1 Life Events

The concept of Life Events is often used in the context of the process-oriented view of public administration. This concept represents the view of public administration activities in their natural relations. These 'natural consequences' are always given by the situation in the life of the public authoritys 'customer' a citizen. Life situations of a citizen are in fact very close to the main goal of the public administration activities and objective reason for its existance. It is obvious that such view has very much to do with the main principle of business process re-engineering ordering activities according to the main goals, which have to be directly connected with the natural strategic goals of the organization consequently always follow from the customer needs.

Life events became one of the most important subjects of the e-government activities. Several standard classifications of life events emerged as a reaction to the fact that standardization is very natural in the area of public administration. These standards are of different quality from simple description of routine activities of clerks to the lists of life events carefully analyzed as core representations of the public administration activities. One of the most interesting classifications stems from the LEAP project. LEAP (Life Events Access Project) [8] is a partnership project among British Councils. According to its mission statement, 'LEAP aims to utilize knowledge management in order to improve service provision to customers. The LEAP consortium will use new information and communication technologies to develop services to best meet the needs of customers and clients.' In this project, life events are derived from the conception of the standard life cycle of a citizen. Despite the fact that 'citizen' is not the only crucial type of public administration objects it is obvious that such an approach is a good basis for constituting the interface between the authority and its customers as it is very closely aligned with the real life and, consequently, with the essence of public administration itself.

Figure 2 shows the general context of the concept of life situations (life events) consisting of other important public administration concepts. Public administration object (such as 'citizen') always exists in some external environment that is a source of basic rules, necessities, possibilities, obligations and other limitations which the object has to respect because they are objective from its point of view. The objective factors are always commonly valid for all public administration objects.

At the same time, the object is limited even by its internal factors dependent on the overall context of its life: its current life situation, its past history as well as its possible future. This context of internal factors is called the 'life cycle' of the object. These factors can be called subjective as they are specific, private for every object. These factors are subjective and valid specifically for the given object nevertheless the object has to respect them in its behavior as well.

In its life the object is experiencing different life situations that follow from the external, objective situation as well as from the internal state of the object's life. The objective, environmental factors are driven by objective logic of the external world. There are three basic sources of crucial life events (see Fig. 2):

Fig. 2. General context of life situations

[FIGURE]

- -Physical environment which represents the natural and other physical values of the given territory. It consists of the natural and physical attributes of the territory such as raw materials, nature and its values for recreation and tourism, and also infrastructure and other values of physical environment important for people as well as for business.
- -Social Environment which consists of people and their personal, cultural, and social values. It includes not only the individual personal characteristics of people but also global attributes of the society itself often called the culture' of the society.
- -Business environment including organizational and cultural values necessary for realization of opportunities. This area includes all business entities: enterprises, entrepreneurs and their quality, employees and their qualification, as well as legislation and quality of public administration services supporting the business.

Similarly, even the internal life cycle factors are driven by the general logic of the life cycle. This general logic of the object's life is objective in the same way as the logic of the external world. This fact is the reason for describing life cycles on the same level of preciseness and regarding them as being as important as the logic of the external world.

## 3 The Project

The aforementioned methodology has been used in the analysis project managed by the Czech Ministry of Interior. This project is focused on the revision of the current official view of life events (life situations) in order to make it consistent with the Czech e-Government Architecture and its intended future development [4]. According to the Chief e-Government Architect Office this architecture should consist of:

- -Countrywide catalog of Public Services supported by Information Systems Services catalog.
- -Key Agenda Information Systems redesign, re-engineering and consolidation.
- -National Architecture Standards.
- -EU interoperability standards and gateways.
- -Compliance with Cyber Security standards.
- -Data orchestration via common service bus called 'eGon Service Bus'.
- -and other important features and tasks.

From the point of view of the project, the most important feature of the architecture is the interface between the public administration processes and 'public administration services' which is called the 'service bus'. At the current state of the architecture, which is mostly technically oriented, this service bus is viewed just as an issue of data, and its meaning is interpreted as 'data orchestration'. However, the meaning of the orchestration should be conceived in a much wider scope. The concept of orchestration is often used in the context of process-driven management and its IT support. Not just data but even the actions in information systems should be orchestrated the same way as the events in the real world are naturally synchronized. From this point of view the service bus has the crucial meaning for the contents and the quality of e-government as it is a direct interface between what is happening in the real life and between the public administration processes. Therefore, it has to take into the account all the essential rules and restrictions of the real life and cover them within its functionality. We posit that the analysis based on the description of life events is the best way to fulfilling these requirements.

The methodology used in the project is based on the conceptual analysis in the area of public administration that includes even the analysis of life cycles of crucial objects, i.e. those objects whose life events are critically important for the public administration activities.

The methodology uses two essential UML diagrams for two basic types of models:

- -Class Diagram for description of the global contextual view on objects in the given area.
- -State Chart for description of the life cycle of one particular object.

Both types of models are used in close mutual dependency.

Figure 3 shows a fragment of the contextual model of public administration objects and their life cycles. The model describes concepts and their relationships which characterize the context of the crucial object types in public administration. In this project we primarily need to identify the crucial objects in the field and all relevant roles which these objects have. Each role represents the specific life cycle. Life cycle is an algorithmic structure of actions driven by events. We primarily need to identify all important algorithmic dependencies connected with each given object. In other words we need to find all possible roles of this object where each of the roles represent a specific life cycle a set of algorithmic dependencies. As the object can have a number of different roles in one moment, it has typically different life cycles (i.e. algorithmic structures of relevant actions) valid at the same time. From the methodological point of view we need to solve the problem of parallel dynamic structures tied to the same object. This theoretical problem is outlined in [2] and its general solution in the form of special pattern is described in [14]. This pattern is used as the main technique in our model. Concepts are classified according to their meaning as follows:

Fig. 3. Contextual model of public administration objects and their life cycles a fragment

[FIGURE]

1. Stereotype kind is used for the concepts which define the basic physical objects and their types.
2. Stereotype phase is used for the concepts which express the states (phases) in the life cycle of given basic physical object that is a super-type of this set of life phases.
3. Stereotype viewpoint is used for the concepts which express the element of the aggregation structure that represents the set of different points of view from which the given physical object can be seen.

This way we can describe any physical object as a set of parallel lives, each one from a specific point of view. All objects in the model are sub-types of the object Public Administration Client. This generic object is an abstract concept existing in two possible forms (sub-types) Physical Person and Company. Both Physical Person and Company are generalizations of the sub-types that represent their life phases. At the same time, each of these objects is an aggregate of the possible viewpoints (roles of person, respectively forms of company), and each of them represents a possible specific life cycle.

Fig. 4. Physical person life cycle

[FIGURE]

Figures 4 and 5 describe the life cycles of object classes Physical Person and Company. Each model represents the specific set of states and possible transitions among them. Every transition is described by its reason (alias some Real World event) and the action taken as a reaction to the reason (the relevant reaction of the public administration). From the contents of both models it is obvious that the same object instance cannot have both life cycles at the same time as it can be either Physical Person or Company, but not both. Their mutual exclusivity follows from the fact that they both are different sup-types of the same abstract type PA Client. Nevertheless, at the same time each of them can have a number of parallel lives in different roles (of Physical Person) or forms (of Company) since both are the aggregate of a number of possible viewpoints that represent different sub-types, each of them living its specific life. 1

## 4 Discussion of the Lessons Learned

During the project we have uncovered many important aspects, specific features, and problems to overcome which originated form the objective of applying the process-driven management in the field of public administration by means of life events. The most important aspects can be structured into two main groups of actual needs:

1 This is visible in the contextual model (class diagram) of the role Offspring of Physical Person which has several life phases (see Fig. 3). Similarly, any other sub-type of viewpoint can have its own life cycle (which are not described by the model in this figure).

Fig. 5. Company life cycle

[FIGURE]

1. Need for distinguishing between essential life events and those events which are forced by public administration:
2. -Essential life events are those regarded as objective, natural factors. Events of this type represent the happenings in the real life no matter whether they are influenced by the public administration actions or not. Examples of essential life events are such natural events as 'birth', 'marriage', 'material poverty', and even personal intention events like 'starting a business' or 'building a house'.
3. -On the other hand, 'forced' life events are those which can (and should) be potentially overcome or eliminated by the means of future technology development in terms of M.Hammer's argumentation for process-driven management [3]. The main reason for such forced events is the need to support the public administration activities. 'Obtaining the ID' or 'filing tax return statement' are examples of such forced events. In public administration, the 'forced' life events are represented exclusively by the legislation. The legislation sets the rules which force all actors to respect them - whether they are essential for the support of public administration activities, or whether they are arguably irrelevant. Thus, we cannot fully accept the idea, widespread especially in the field of public administration, that the legislation is the highest authority expressing the essence of the real life, and therefore it has to be respected without a doubt. If we were respecting such an understanding of the legislation we would never be able to eliminate even a single 'forced' life event. This means in turn that we would never be able to make any positive change in the public administration practice, in terms of the idea of process-driven management, using the possibilities provided by the new technology. On the other hand, we cannot ignore the forced events as they are a regular part of the current

state of the real life. For most people the legislation is the basic view that determines their understanding the public administration activities and their conceptual meaning. However, from the practical point of view, the respect for the legislation rules is mandatory including even the rules which represent the forced events.

Based on from the above argument it seems necessary to distinguish not only between essential and forced life events but also between the similar two kinds of models. This finding led us to maintain two types of public administration ontology models:

- Full current state ontology models that contain all life events: the essential as well as the 'forced' ones. These models allow us to communicate with people from the public administration in the manner that is very close to their understanding of their business. This mutual understanding is very important for our need to make all models complete, i.e. to incorporate in them all the important, and necessary events as well as the consequent public administration actions. Only such complete models create a sufficient basis for understanding all necessary e-government services which is the ultimate original goal of the project.
- Essential ontology models that contain only the essential life events. The main value of these models lies in the fact that they express the essential reasons for the public administration acts which have to be respected anyway. In other words, these models express the extent to which the processes of the public administration can be reduced without simultaneously reducing their essential meaning the borderline between what can and what cannot be actually eliminated by means of technology.
2. Need for shifting the understanding of life events and their role in public administration.

Figure 6 shows the fragment of the public administration ontology that emphasizes the difference between the public administration and the citizen points of view on life situations. It also shows in which direction the traditional understanding of life events should be shifted. In the traditional understanding (represented by the bold association between the concepts 'PA Agenda' and 'Life situation'), life situations are regarded as a specific view of the public administration official processes (so-called 'PA agendas'). Agendas are defined by legislative documents and fixed in the organizational structure of PA authorities. Thus, the meaning of a particular life situation is defined by the PA agenda(s) connected to this situation. From this point of view the life situation is nothing more than just a specific view of the agenda, the view which is close to the client's perception of such agendas. Even though it represents a significant difference in the presentation of PA agendas, this point of view is still far away from the natural meaning of life situations and from the real value of this approach to the PA development.

The needed new understanding of the concepts (represented by the bold association between the concepts 'Employee' and 'Life situation') is substantially different. For the PA authority employee, as a provider of PA agendas, the life situation represents the trigger of the particular agenda. Agendas are regarded as tools for solutions of life situations. Given the fact that life situations are naturally dynamic (as the environment is changing, the new life situations emerge and the meaning of current situations mutates as well, etc.), even the agendas acquire different meaning from this viewpoint. Therefore the agendas should be regarded as something dynamic, continuously changing. This understanding of the meaning of the agenda contrasts with the original meaning of this concept and consequently leads to a dramatically different view on the public administration processes which is close to the process-driven management ideas as expressed in [3]. Further consequences can be deducted from the aforementioned literature: the need for changing of the public administrations organizational structure as well as redefining the role of legislation, etc.

Fig. 6. Public administration versus person's views on life situations

[FIGURE]

Although, at the first look, this view does not seem to be much different from the traditional one, the proposed enhancement of the life situation concept naturally leads to a substantially different perception of the meaning of PA agendas. Consequently, it also naturally leads to a substantially different perception of the traditional roles in public administration it starts fulfilling the original purpose of e-government: a client-oriented public administration.

## 5 Conclusions and Future Work

As follows from the previous section, the use of the life events concept as the root of the public administrations activities naturally invokes many related essential changes and uncovers many important problems to be solved in the field of public administration and e-government. The experience gained from the project mentioned in this paper led us to the following main conclusions:

- -Looking at the public administration in terms of life events and their needed solutions allows a comprehensive analysis of the requirements for so-called e-government based on the essential nature of the public administration: the situations in lives of the crucial objects and their natural consequences. This point of view is an analogy of the idea of the process-driven management. In fact, it expresses exactly the same idea.
- -At the same time, this point of view naturally leads to an essential change of the approach to the understanding of the public administration role. Public administration actions have to be understood not as the purpose but as the consequence of the life of society and its elements (called in our project 'public administration clients').
- -Moreover, this point of view is closely connected to the essence of the so-called e-Government, i.e., as the application of the information technologies in public administration. Semi-formal models of life cycles completed with the ontology model of their mutual context can serve as a precise definition of the contents of the central common part of the public administration IT applications' logic. It expresses the essence of the real world logic together with the basic contents of the legislation. In the Enterprise Architecture and connected terminologies, this central common part of the applications' logic is usually called 'enterprise service bus' or 'common request broker', etc.
- The main actual problems connected with above described paradigmatic change, as uncovered in the project, are:
- The need for distinguishing between essential life events and those events which are forced by the public administration.
- The need for shifting the understanding of life events and their role in public administration.

Overcoming these two kinds of actual problems is an essential condition for successful application of the process-driven management concepts in the field of public administration. At the same time, given how substantial is the connection between information technology and process-driven management, it is as well an indispensable condition for successful application of e-government per se.

Future work should have two main directions:

- The completion the model of life events to achieve the state in which it will express all substantial events that require some reactions from the public administration bodies . This model then will be used as a basis for the definition of the need for essential public administration processes. Further analysis of these processes will lead to their standardization and to the specification of the basic central public administration agendas. This way the border between the mandatory standard activities and the space for individual creativity in managing public administration processes in various public administration bodies will be exactly defined.
- -The use of the definitions of life cycles (state charts) together with the contextual information from the connected global ontology models (class diagrams) as a basis for the development of the central public administration service

bus - a crucial part of the e-government architecture framework. This element of the framework represents the essence of the interface between the public administration activities and their central support by the information systems in several dimensions:

- From the technical point of view, the bus is a central broker ensuring the interchange between the process requests (representing real events) for the information support and suitable information systems that offer the corresponding IS services. It also contains the mechanism assuring general correctness of the reactions as well as of the requests based on the knowledge of the context of every event in the life cycle models.
- At the same time, this meeting point represents the standard interface for all possible information systems for their connection with the corresponding information requests from the public administration processes. In other words, this standard represents the market place that allows the integration of public administration processes with the information services market supply in terms of opening as wide as possible public-private cooperation. Public-private cooperation in terms of the open market for information services is the only warranted way to decreasing the public expenses for IT support towards their optimal value.

Acknowledgments. The paper was processed with contribution of long term institutional support of research activities by Faculty of Informatics and Statistics, University of Economics, Prague.

## References

1. eGovernment, Information Society Commission, Dublin, Ireland. http://www. isc.ie
2. Guizzardi, G.: Ontological Foundations for Structural Conceptual Models, Telematica Instituut, Fundamental Research Series No. 15 (2005). ISBN 90-75176-81-3 ISSN 1388-1795
3. Hammer, M., Champy, J.: Reengineering the Corporation: A Manifesto for Business Revolution. Nicholas Brealey Publishing, London (1993)
4. Hrabe, P.: The proposal of czech government enterprise architecture implementation. In: CONFENIS-2013, 7th International Conference on Research and Practical Issues of Enterprise Information Systems, Prague, Trauner Verlag, Linz (2013)
5. Jackson, M.A.: Principles of Program Design. Academic Press, London (1975)
6. Jackson, M.A.: System Development. Prentice-Hall Inc., Englewood Cliffs (1982)
7. Kobryn, C.: Introduction to UML: Structural Modeling and Use Cases, Object Modeling with OMG - UML Tutorial Series (2000). www.omg.org
8. [LEAP Project. http://www.leap.gov.uk/](http://www.leap.gov.uk/)
9. [McKendrick, J: Making e-government more than a glorified service-delivery platform, SmartPlanet (2009). http://www.smartplanet.com/blog/business-brains/ making-e-government-more-than-a-glorified-service-delivery-platform/2964](http://www.smartplanet.com/blog/business-brains/making-e-government-more-than-a-glorified-service-delivery-platform/2964)
10. The e-government imperative: main findings, OECD Observer, March 2003
11. The Obama Administrations Commitment to Open Government, status report (2012)

12. [OpenSoul, 2000-2015. http://opensoul.panrepa.org](http://opensoul.panrepa.org/)
13. PARMA: Public Administration Reference Model and Architecture Project. http://parma.vse.cz
14. Repa, V.: Modeling life cycles of generic object classes. In: Linger, H., Fisher, J., Barnden, A., Barry, C., Lang, M., Schneider, C., et al. (eds.) Building Sustainable Information Systems, pp. 443-454. Springer, New York (2013). ISBN 978-1-46147539-2
