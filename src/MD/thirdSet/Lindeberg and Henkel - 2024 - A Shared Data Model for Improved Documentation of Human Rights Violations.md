[FIGURE]

## A Shared Data Model for Improved Documentation of Human Rights Violations

[FIGURE]

[FIGURE]

Jöran Lindeberg,

*

,

and Martin Henkel **

,

## Abstract

Human rights groups of all sizes and specializations gather evidence of human rights violations. Those with sufficient resources commonly use dedicated databases to manage the intricate web of sources, events, and analyses that build a strong case. However, developing databases for the needs of each organization remains a challenge. Effective database design requires a data model, which functions as a blueprint for how the data is structured and related. A most basic example of what a data model can specify is that a human rights violation is committed by at least one perpetrator, and that the perpetrator's attributes, such as name or date of birth, should be recorded. A data model that is shared and generic reduces the need to reinvent the wheel since its design can be reused for several databases. In the information systems field, such shared models are called ontologies. Despite the critical nature of the matter, no ontology for human rights violations documentation exists. The present note, therefore, will present the design of the first ontology of this kind. It was developed in association with the human rights group HURIDOCS, which specializes in information management. The requirements elicitation included unstructured interviews with HURIDOCS, document analysis of human rights manuals, and a survey with practitioners. The resulting ontology, named OntoRights, is freely available online with an open license. The evaluation of OntoRights suggests that OntoRights could be highly useful for case databases.

## Practitioner Points

- Human Rights Groups documenting human rights violations need well-designed data models for managing their information.
- There is a need for shared and reusable data models, reducing the need to reinvent the wheel. The shared models must be both generic and adaptable, which is a challenge.
- A reusable data model called OntoRights is available online with an open license. Human rights groups can use it as a base for their own data models.

Keywords: complex adaptive system; data modelling; human rights technology; information system; ontology

* PhD student, Department of Computer and Systems Sciences, Stockholm University, Stockholm, Sweden.
- ** Associate Professor, Department of Computer and Systems Sciences, Stockholm University, Stockholm, Sweden.

© The Author(s) 2024. Published by Oxford University Press.

This is an Open Access article distributed under the terms of the Creative Commons Attribution License (https://creativecommons.org/licenses/by/4.0/), which permits unrestricted reuse, distribution, and reproduction in any medium, provided the original work is properly cited.

## 1.  Introduction

In their quest for truth and justice, human rights groups of all sizes and specializations gather evidence of human rights violations. The collected information is stored in repositories of varying types: from paper notebooks to advanced databases. This practice is referred to as human rights violations documentation . According to Dueck et al. (2001: 4), 'documentation  is  the  process  of  systematically  recording  the  results  of  an  investigation  or fact-finding in relation to an event or number of events'. While some cases of human rights violations contain just a single piece of information, others constitute a complex puzzle of people, timelines, legal analysis, connections with other cases, and sources.

Managing this information is a challenging task, in particular since many human rights groups work on a shoestring budget (Land and Aronson 2018) in high-pressure environments (Pirac é s 2018). Fortunately, the costs associated with the necessary technologies are falling (Land and Aronson 2018) so more human rights groups can make the leap from text documents and spreadsheets to a structured database, or improve an existing database.

The need for structure is increased by today's abundance of data sources. Social media, smartphones, and sensors produce much useful data (Pirac é s 2018), but also contribute to information overload. Hence, in the words of Guberek and Silva (2014: 13), 'the quantity of data available requires careful organization and preservation to enable its use in long-term struggles for truth and justice'. However, the reviewed literature (Pirac é s 2018; Land and Aronson 2018; Poblet and Kolieb 2018) conveys the impression that the human rights technology field have had more focus on extracting information than structuring it. Structure is also needed for improved inter-organizational information exchange, which is hampered by the heterogeneous character of both the cases and the involved actors (Harrison et al. 2020). As Alston and Gillespie (2012) have shown, the current human rights system suffers from dispersed information, a term established by Sunstein (2006).

Database design requires a data model , which functions as a blueprint stating how different concepts relate to each other. Developing effective data models, however, remains a challenge for human rights groups. Therefore, the Geneva-based civil society organization Human Rights Information and Documentation Systems (HURIDOCS) recently published a community resource for database design, written for and with human rights groups who are  documenting  human rights  violations  in  their  communities. 1   Such  capacity-building efforts can be mutually reinforced by other kinds of support. One possibility is to use what in the information systems field is called ontologies .

An ontology can be described as a data model that is shared, generic, and represents consensus about a domain (Nguyen 2011). In other words, it is above the implementation of a concrete data system (Gruber et al. 2016). An ontology can specify, for example, that:

- A Human Rights Violation is committed by at least one P erpetrator ,  with attributes such as name or date of birth .
- A Perpetrator can have a Role in an Organization .

There are several benefits to using ontologies in information systems. Ontologies can contribute to reducing the problem of semantic heterogeneity , that is the problem that different systems (or people) do not use the same, well-defined, concepts (Uschold and Gruninger 2004). In other words, ontologies help not only machines but also people to acquire a shared understanding of a domain (Uschold and Gruninger 2004). For the purpose of database  design,  it  is  easier  to  adapt  an  existing  domain  ontology  than  reinvent  the  wheel. Beyond the creation of individual databases, ontologies are also powerful tools for system integration and the automatic processing of information dispersed across web sites. This approach could reduce the tedious human labour of searching for already published information and then repackaging it for new purposes.

1 HURIDOCS' Community Recourse can be accessed at https://huridocs.org/community-resources/ (accessed 24 July 2024).

In spite of these advantages, no ontology for human rights violations documentation appears to have been designed before. The closest work in this direction that could be found is:

- A data model designed by HURIDOCS two decades ago, the so-called event model (Dueck et al. 2001: 223/Appendix C).
- An ontology called UFO-L, documenting legislation (Griffo 2018).

The data model by HURIDOCS can represent the core questions of human rights violations documentation: who did what to whom? and what was done in response? Moreover, it comes with exhaustive lists of domain relevant reference data, such as rights, ethnicities, and body parts. This model is still being used to some extent, even though its uptake among practitioners appears to have been moderate. One possible reason for this is an apparent lack of customizability. Another weakness is that it is rather limited to physical events-for example a police officer hitting someone-and is inadequate for expressing an event's legal implications. For example, if the violence by the police officer was not proportional, this act would constitute a human rights violation. In contrast, the second model, UFO-L, can express advanced legal problems but is too abstract for effective representation of many other aspects of human rights violations.

To close this gap, the research goal was to design the first ontology for human rights violations documentation, in collaboration with HURIDOCS. Named OntoRights, its primary purpose is to be used by human rights groups for developing case databases.

In order to provide the reader with an idea of what an ontology can concretely look like, a part of a module of OntoRights is available in Figure 1. As can be seen, the module shows concepts needed to describe a human rights violation, and how these concepts are associated with each other. The module that is displayed is one of ten; the remaining modules can be seen in the figure as links on the left.

Figure 1. A screenshot of the Human Rights Violation module of Easy OntoRights, accessed as a website on GitHub.

[FIGURE]

A human rights group can reuse complete modules or just parts, according to its needs. For instance, as part of the evaluation of OntoRights, an adapted instantiation was developed  for  Committee  for  Justice,  an  Egyptian  human  rights  group  focused  on  arbitrary detentions. In their data model, only some modules were included, and additional concepts and associations had to be added to reflect their work and the Egyptian justice system. A more detailed explanation of OntoRights is presented in section 3.

The remainder of this note is organized as follows: section 2 explains the research process, from problem explication to evaluation. The subsequent section presents OntoRights and the results from its evaluation. The final sections include discussion and conclusions.

## 2.  Methodology: design science research

The overall methodological framework for this note is Design Science Research (DSR), as described by Johannesson and Perjons (2014). The aim of DSR is to create an artefact that solves a practical problem. DSR consists of five logically connected phases: (1) Explicate Problem, (2) Define Requirements, (3) Design and Development, (4) Demonstration, and (5) Evaluation. Note that the connections between phases are logical, but not necessarily chronological. Each phase can have its own research strategies and methods. In the following, it is described how each of the phases was applied in order to create OntoRights.

## 2.1  Explicate problem and define requirements

The problem was explicated through unstructured interviews with HURIDOCS. At the time, HURCIDOCS was developing a community resource with the purpose of supporting human rights groups in developing data models for human rights violations documentation. We concluded that this resource could be complemented by an ontology in the same domain.

Much effort was devoted to defining the requirements of the ontology. Requirements can be divided into non-functional and functional (Johannesson and Perjons 2014). While the non-functional requirements concern the generic qualities of OntoRights, the functional requirements are about competency questions , that is what kind of statements the ontology should be able to express. An example of such a statement could be 'to which organization(s) does a certain person belong?'.

Preliminary  non-functional  requirements  were  also  elicited  through  the  unstructured interviews  with  HURIDOCS. A  main  concern  was  how  to  handle  the  fact  that  human rights  organizations  have  very  varying  needs,  depending  on  differences  in,  for  example, thematic focus, geographic location, and legal expertise. Another challenge, identified in the literature (Guberek and Silva 2014) is that prior experience has shown that tool-centric approaches, that is building a specific tool and proposing that human rights practitioners use it, have often led to low uptake. Instead, more long-term support based on a systemic view is needed.

The preliminary non-functional requirements were further analysed through the lens of a design theory about information infrastructures by Hanseth and Lyytinen (2010). The authors argue that conventional design theory in general wrongfully assumes a static environment and a designer in control of the design space. This might often be true for less complex types of IT artefacts such as single IT capabilities, applications and even platforms, but not for an information infrastructure, which can be described as a shared, heterogeneous and evolving sociotechnical system, consisting of both its IT capabilities and user community.

Hanseth and Lyytinen (2010) identify two inherent and conflicting problems of information infrastructure (II) design: the bootstrap problem (how to attract a critical mass of users) and the adaptability problem (how to prepare the system to grow and thrive). As a solution, the authors propose five design principles, shown in Table 1, which are further broken down into 19 design rules.

Table 1. Information infrastructures (IIs): problems and design principles. (Adapted from Hanseth and Lyytinen (2010, Table 2)

| Problem                  | Design Principle                                                                                                                                                  |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| The bootstrap problem    | 1. Design initially for usefulness 2. Draw upon existing infrastructures and communities 3. Expand existing infrastructures and communities by persuasive tactics |
| The adaptability problem | 4. Make each IT capability simple 5. Modularize the II                                                                                                            |

An ontology, together with its users and related IT solutions, form an information infrastructure, and the identified tension between the two problems above is thereby relevant for OntoRights. The implication of the II bootstrap problem is that OntoRights must be useful for, and used by, small human rights groups for developing case databases. Moreover, the II adaptability problem requires additionally designing OntoRights so that it can evolve and survive in the long run, and consequently in the future be used also for system integration, artificial intelligence, and semantic web applications.

Based on the IIs design principles, seven generic qualities for the design of OntoRights were initially defined:

Requirement 1: the ontology should have high usefulness for human rights groups doing conceptual modelling.

Requirement 2: the ontology should have high ease of use for human rights groups doing conceptual modelling.

Requirement 3: the ontology should have high customizability.

Requirement 4: the ontology should have high modularity.

Requirement 5: the ontology should have high completeness.

Requirement 6: the ontology should be made available with the most widely used relevant standards.

Requirement 7: the ontology should be published with tools that are collaborative and open source.

The functional requirements, that is competency questions, were defined in two phases: a  qualitative  document survey of human rights monitoring manuals, and a quantitative survey with human rights practitioners. The aim of the document survey was to acquire a  complete  picture  of  the  human  rights  violations  documentation  domain.  The  sample started with the several-hundred-page-long Manual on Human Rights Monitoring (2011) by the UN Human Rights agency. After relevant parts had been reviewed, the sample was extended to the 261-page-long HURIDOCS' Events Standard format (Dueck et al. 2001). The documents were subject to thematic analysis, drawing from Braun and Clarke (2006), which includes marking relevant text extracts, coding them, grouping codes into themes, and finally also grouping the themes. The resulting themes, or sub-domains, were:

1.  Roles and People.
2.  Relations Between Events.
3.  Interventions (Remedy by the State).
4.  Human Rights Protection System.
5.  Monitoring Process.
6.  Information Management.
7.  Organizational Structures, Influence and Risk.

While the aim of the document survey was to acquire a complete picture of the domain, the purpose of the practitioner survey was to understand what to prioritize within that domain. Concretely, the document survey grounded the questionnaire that was used in the practitioner survey. The purpose of said questionnaire was to understand which of the seven subdomains identified in the document survey should be given priority during the design and develop artefact activity. A questionnaire was written in English and translated into Spanish. It contained 25 questions grouped according to the seven subdomains identified in the previous section. It also included background questions about the participants, such as years of experience and geographic focus. It asked the participants to: (1) imagine that their organization was developing a new database for managing their documented cases of human rights violations; (2) according to perceived importance, do an ordinal categorization of the identified themes, with questions starting with 'How important is it that your database can express …'; and (3) perform a ranking of the subdomains.

Links to the questionnaire were distributed by HURIDOCS to human rights groups in its network. In total, 13 participants submitted the form, three of them were in Spanish. Everyone had experience of working with human rights violations documentation (at least two years' worth in all but one case), in particular from managing information from fieldwork in a database. Their aggregated experience covered all seven parts of the world that could be selected in the form, with some extra weight on Northern Africa and Middle East , and Latin America and the Caribbean . Common focus areas of the participants included, for example, protection of human rights defenders, persons deprived of liberty, and migrants.

Two calculation methods were used to triangulate the relative importance of each subdomain, with rather concurring results (Lindeberg 2023). The result is shown in Table 2.

## 2.2  Design and development

Ontology  design  requires  choices  regarding  foundational  and  core  ontology,  ontology language and an ontology tool. A foundational (top-level) ontology defines essential concepts about reality and their relations. A core ontology does the same for a broad domain, such as law. An ontology language represents the ontology, either with computer code or a visual model of, for example, boxes and arrows. An ontology tool is the computer application used. For OntoRights, the chosen foundational ontology was Unified Foundational Ontology (UFO), and the core ontology of the legal domain was UFO-L. One advantage of  UFO-L is that it builds on Alexy's Theory of Constitutional Rights, which is a legal theory suited for expressing conflicting principles, which is common in human rights problems. Finally, OntoUML was chosen for the ontology language, and the OntoUML Visual Paradigm Plugin was selected as a tool.

OntoRights was then designed in modules, starting with the subdomain that had been identified  as  the  most  important  in  the  practitioner  survey,  proceeding  with  the  second most important subdomain, and so forth. For increased ease of use, the full version of OntoRights (Full OntoRights) was converted into another version (Easy OntoRights) that is less true to ontological rules but closer to a conceptual model of a case database. At a later point, yet another version, Basic OntoRights, was added for users who found Easy OntoRights hard to grasp. All versions are available at OntoRight's website on Github. 2

Table 2. Subdomains ranked according to perceived importance in the practitioner survey

| Subdomain                                     |   Importance |
|-----------------------------------------------|--------------|
| Roles and People                              |            2 |
| Relations Between Events                      |            6 |
| Interventions (Remedy by the State)           |            5 |
| Human Rights Protection System                |            3 |
| Monitoring Process                            |            4 |
| Information Management                        |            1 |
| Organizational Structures, Influence and Risk |            7 |

## 2.3  Demonstration and evaluation

Easy OntoRights was demonstrated as instantiations for both a real case and a fictitious case. In both cases, the actual instantiation of the ontology was done by the authors of this note. The real case was the Committee for Justice, a human rights group that monitors cases of arbitrary detention and maltreatment during detention in Egypt. It aims to track how criminal investigations involve different people, who in turn are sent to different detention centres. The Committee for Justice preferred to be public about its participation and was therefore not anonymized. The fictitious case was Harassment Stop, a human rights group in need of a conceptual data model for its monitoring of incidents of harassment against a minority group.

Additionally,  an  evaluation  was  conducted  through  semi-structured  interviews  with three staff members from HURIDOCS and the Committee for Justice. The questions were designed to capture to what extent the non-functional requirements had been fulfilled. The result of the evaluation is described in the next section.

## 3.  Result: the OntoRights ontology

This section gives an overview of Easy OntoRights and how it can be used, and also reports results from its demonstration and evaluation. Full OntoRights and Basic OntoRights will not be presented further; we prioritize Easy OntoRights since this is the version we consider of most practical use for database design, and is also the version that was demonstrated and evaluated. However, readers interested in more details can access all three versions, including documentation, user manual, and project files, on GitHub. 3

## 3.1  Overview of Easy OntoRights

As mentioned, Easy OntoRights is designed in a language called OntoUML, which in turn builds on Unified Modelling Language (UML) class diagrams. A class diagram shows how classes (that is, concepts, such as 'Person') are associated to (for example 'works for') other classes (such as 'Organization'), and the attributes (for example 'year born') of each class. In other words, a database designed according to the examples in the previous sentence can contain the information that, for example, a person called Sara was born in the year of 1988 , and works for the organization Amnesty International . Another important feature of class diagrams is defining the multiplicity of each association, that is, how many instances of the other class an instance of the first class can be associated to. For instance, an organization would likely have several people working there.

The above features could be considered the core of a UML class diagram. The added value of OntoUML is that it embeds syntactical rules that help the designer to make a data model according to the logic of the top-level Unified Foundational Ontology (UFO) mentioned earlier. As also mentioned earlier, extending an existing foundational or core ontology allows for the reuse of high-quality design patterns, and can also facilitate interoperability between different systems.

Easy OntoRights includes nine ordinary modules, and an annexe module with data types (that is, if an attribute is, for example, a text string or a decimal number) and enumerations

[2 https://joranl.github.io/human-rights-ontology/ontorights-access.html (accessed 24 July 2024).](https://joranl.github.io/human-rights-ontology/ontorights-access.html)

[3 https://joranl.github.io/human-rights-ontology (accessed 24 July 2024).](https://joranl.github.io/human-rights-ontology)

(that is, lists of permitted values). One of these modules, the Human Rights Violation module,  is  shown  in  Figure  2. This  can  be  considered  the  core  module,  including  the  basic components of a human rights violation: a perpetrator did something to a victim, and this action (or inaction) violates a human rights standard. Note that this diagram is not immediately understandable for people without previous experience in data modelling.

Another noteworthy module, for which the corresponding subdomain scored high in importance in the practitioner survey, was information management. This module shows how an event of interest is associated with a Monitoring Process (that is, a case file) that contains Monitoring Events (that is, investigative measure) conducted by the human rights group.  Each  Monitoring  Event  has  as  an  attribute  regarding  how  informed  consent  (if relevant) was obtained from, for example, victims and witnesses. A Monitoring Event can optionally contain sub-events, which allows for a more granular representation of reality. This solution may seem complex at first, but it should be noted that a particular human rights group or investigator may choose to use this pattern or forsake granularity for the sake of simplicity, which can also be a valid choice. After all, all models are only approximations to what information systems researchers refer to as the 'messy reality'. A final remark about this module is that a Monitoring Event generates Pieces of Information. One possible reason for dividing the information from one Monitoring Event into several pieces is that they may have different types of confidentiality.

Figure 2. The Human Rights Violation module of Easy OntoRights. This OntoUML diagram shows, among other things, that a Human Rights Violations requires at least one Perpetrator and at least one Victim . It also shows that both Perpetrator and Victim are sub-classes (i.e. a kind of) Agent .

[FIGURE]

Together these modules form a comprehensive model of a case database. For a complete look  at  Easy  OntoRights,  please  access  its  diagrams  (published  as  a  webpage) 4 and  its accompanying documentation. 5

However, as recognized during the requirements elicitation, human rights groups have varying needs. A particular human rights group will probably not need the complete model, but only certain modules, or even just parts of modules. It is also unlikely that the suggested attributes in Easy OntoRights are exactly what each group needs.

To do these adaptations in practice, the suggested approach would be that the human rights group: (1) download the free community version of Visual Paradigm, (2) add the OntoUML plugin, (3) download and open the Easy OntoRights project files, (4) remove unnecessary modules and classes, and (5) do any other additional changes of associations and attributes. An alternative approach would be to start from scratch with any tool while looking at the website version of Easy OntoRights for inspiration.

## 3.2  Results from demonstration and evaluation of OntoRights

As mentioned above, the demonstration of Easy OntoRights included two cases: the fictitious Harassment Stop and the real Committee for Justice. Harassment Stop was described as an expanding organization with increasingly advanced needs, that implements new modules in phases. For this case, OntoRights worked perfectly.

As for the Committee of Justice, OntoRights was used to propose a redesign of the organization's public database Justice Watch Archive. The proposed instantiation could represent a  complete  cycle  of  detention  of  a  person,  and  the  legal  human  rights  implications.  Its most important elements will be presented in the following. (For clarity, classes will be in bold, and attributes and associations will be in italics.) A Court participates in an Event , which creates a Legal Process , which creates a role for a Person as a Detained Person , with a start time and eventually an end time . The Legal Process also includes the responsible Persons , in their respective capacity of president of the court , fi rst advisor , and second advisor . The Detained Persons is detained in a Detention Centre , which is a type of Place with a latitude and longitude . Some Events can be ground for legal implications, more specifically a Human Rights Violation . If so, this must be argued through a legal analysis , and be associated with a Victim , which is another possible role for a Person . As mentioned, only the relevant elements of Easy OntoRights were used for this instantiation. For example, Easy OntoRights can in a structured manner express the particular Human Rights Standards that a Human Rights Violation concerns , or that this Human Rights Standard is content of a certain Human Rights Instrument . However, these aspects were not deemed important enough for the work of the Committee for Justice to include in the model.

[4 https://joranl.github.io/human-rights-ontology/vp-projects/Easy\_OntoRights\_v1\_1/ (accessed 24 July 2024).](https://joranl.github.io/human-rights-ontology/vp-projects/Easy_OntoRights_v1_1/)

5 https://joranl.github.io/human-rights-ontology/easy-ontorights-documentation-v1\_1.html (accessed July 2024).

When dealing with a real organization, it became apparent that there is a myriad of potential associations in the human rights violations documentation domain that are unfeasible to include in a domain ontology, which per definition is generic. For example, since Committee for Justice  tracks  several  different  categories  of  people  involved  in  criminal investigations, additional associations had to be added (president of the court, first advisor, and second advisor, as mentioned above). However, this adaptation could be done quickly without negative effects on the model as a whole. The Committee for Justice reviewed the proposed instantiation and considered that it would be useful as a starting point if the organization in the future was to make major changes to its database.

While the least positive evaluation participant thought that OntoRights perhaps could be useful, the others were more convinced. A Committee for Justice Participant commented that 'It is extremely efficient, everything is there'. Participant 1 stated that overall, the ontology would be 'very, very useful'. All participants stated they would use OntoRights in varying degrees next time they do conceptual modelling of a case database: 'It is very likely. I definitely would use it' (Participant 3).

The participants were also asked if they would recommend its use to other groups. Two said yes, but one participant said it depended on the technological competence of the group. The participants saw a risk that a human rights group could be overwhelmed by the many classes, associations, and technically sounding attributes:

The great challenge is to understand all this without being an engineer … Many organizations do not have a technological team. For the great majority of people [these diagrams] are very frightening (Participant 2).

One suggestion was to present key fragments of Easy OntoRights in a simpler language than OntoUML and without attributes. Short introduction videos and translations to other natural languages than English were also suggested. In conclusion, non-functional requirement number 2 (ease of use) was only partly fulfilled.

The participants thought Easy OntoRights appeared to be flexible with regard to the many different types of issues that human rights groups can monitor:

It is quite adaptable; it can be used for different reasons and different needs. It is perhaps 90-95 per cent adaptable (Participant 3).

Regarding non-functional requirement 7, about tools that are collaborative and open source, there were mixed outcomes. On the one hand, the ontology is published with an open license on GitHub, which is collaborative and open source. On the other hand, Visual  Paradigm  is  neither  free  nor  open  source.  The  community  edition  of  Visual Paradigm is free for non-commercial use but does not include the feature that published the ontology as a local website, which is a limitation. In summary, this requirement was only partly fulfilled.

From the above findings from the three evaluation interviews, we assessed that OntoRights fully fulfilled five out of seven of the elicited non-functional requirements. Two, however, were only partly fulfilled: Requirement 2 (ease of use) and Requirement 7 (tools that are collaborative and open source).

In response to the raised doubts regarding ease of use, OntoRights was recently updated to release 1.1. This update includes a third version of the ontology: Basic OntoRights. Its purpose is mainly pedagogical, to bridge the gap between the Easy OntoRights and human rights practitioners that are new to conceptual modelling. Its simple notation is borrowed from HURIDOCS' previously mentioned Community Resource. Moreover, this new release includes some minor adaptions of Full and Easy OntoRights based on feedback from other modelling scholars.

## 4.  Discussion

The research goal was to design a domain ontology for human rights documentation with the primary purpose of facilitating conceptual modelling of case databases for human rights groups. The evaluation suggests that OntoRights could be highly useful for this purpose, either as a blueprint or as mere inspiration. However, the requirement of ease of use was only partly fulfilled, at least initially. Using release 1.0 of OntoRights was likely to be too demanding for the human rights groups with the scarcest resources, at least not without assistance. Therefore update 1.1 included an additional simplified version of OntoRights. Moreover, human rights groups at the mid-range level are perhaps anyway those who do have the resources to develop a database beyond spreadsheets and off-the-shelf content management systems.

The discussion  above  highlights  the  challenge  of  designing  shared  data  models  for  a user community with such diversity as human rights practitioners. Adaptation is crucial to achieve usefulness. Moreover, as emphasized by information infrastructure design theory, a shared data model must also be able to adapt over time. Here, we consider OntoRight a substantial step in the right direction but hope to see future contributions by other authors.

As  discussed  in  the  Introduction,  no  formal  ontology  appears  to  have  been  designed previously for the specific domain of human rights violations documentation. From a more general point of view, however, OntoRights can be compared with, on the one hand, existing legal ontologies, and, on the other hand, existing available data models. Legal ontologies such as UFO-L can express the legal aspects of human rights problems. In particular, UFO-L allows for expressing advanced combinations of duties, rights,  powers,  liberties commissions, and omissions (Griffo et al. 2020), which can be valuable for a more complex legal  analysis  of  human  rights  problems.  Since  OntoRights  extends  UFO-L,  these  more advanced features are inherited. However, the domain of human rights violations documentation comprehends more aspects than law. UFO-L does not cover, for example, organizational structures, places, or information management, while OntoRights has dedicated modules for these aspects. Another major advantage of OntoRights is that it also includes Easy OntoRights. In comparison, UFO-L is considerably more difficult to instantiate for case databases.

Regarding  available  data  models,  the  foremost  contender  is  the  model  designed  by HURIDOCS two decades ago,  the  so-called  Events  Standard  (Dueck  et  al.  2001:  223/ Appendix C). Compared to the Event Standard, Easy OntoRights has a number of advantages. First, while the Events Standard is closer to a physical model of a relational database, Easy OntoRights is closer to a conceptual model, which increases its compatibility with other technologies. Second, Easy OntoRights is presented as modules, which makes it easier to understand and customize. Third, while the Events Standard mainly can express 'what happened?', Easy OntoRights can better represent 'what are the human rights implications' and 'how do we know this?'.

## 5.  Conclusion

In this note, we addressed the lack of shared data models, also known as ontologies, for human  rights  violation  documentation.  Both  qualitative  and  quantitative  inputs  from human rights practitioners were analysed through the lens of an information infrastructure  design  theory,  leading  to  a  set  of  functional  and  non-functional  requirements. The proposed ontology, called OntoRights, was designed as an extension of an existing legal core ontology, UFO-L. OntoRights was demonstrated and evaluated by human rights practitioners, who found it useful and complete but expressed doubts about its ease of use. In response, another version of OntoRights was developed, that prioritized ease of use over completeness.

Looking ahead, OntoRights, just like any formal ontology, has the potential to be used for system integration, artificial intelligence, and semantic web applications. This could be an entry point towards a human rights system that suffers less from the dispersed information problem identified by Alston and Gillespie (2012), and where the individual cases gathered by local human rights groups can be better recognized, aggregated and finally funnelled to the halls of power, as envisioned by Harrison et al. (2020).

## Acknowledgements

For their time, knowledge, and trust, we want to express our gratitude to the members of HURIDOCS, the Committee for Justice, and the other human rights groups who participated in this research project.

## Conflict of Interest

The authors did not have any prior affiliations with the involved organisations.

## Funding

This work was supported by Stockholm University (with no external funding).

## References

- Alston, P., and C. Gillespie. 2012. Global Human Rights Monitoring, New Technologies, and the Politics of Information. European Journal of International Law 23(4): 1089-123. https://doi.org/10.1093/ ejil/chs073.
- Braun, V., and V. Clarke. 2006. Using Thematic Analysis in Psychology. Qualitative Research in Psychology 3(2): 77-101. https://doi.org/10.1191/1478088706qp063oa.
- Dueck,  J.,  M.  Guzman,  B.  Verstappen,  J.  Dueck,  and  HURIDOCS  (Network).  2001. HURIDOCS Events Standard Formats: A Tool for Documenting Human Rights Violations . Versoix, Switzerland: HURIDOCS.
- Griffo, C. 2018. UFO-L: A Core Ontology of Legal Aspects Built on Legal Relations Perspective . Vitória, Espírito Santo: Federal University of Espírito Santo State.
- [Griffo, C., J. P. A. Almeida, and G. Guizzardi. 2020. Legal Theories and Judicial Decision-Making: An Ontological Analysis. Formal Ontology in Information Systems. Vol. 330. pp. 63-76. https://ebooks. iospress.nl/volume/formal-ontology-in-information-systems-proceedings-of-the-11th-international-conference-fois-2020?\_gl=1*1imoqcs*\_up*MQ..*\_ga*MTI0MjQwMjYxNC4xNzIxODAxNjY0*\_ga\_6N3Q0141SM*MTcyMTgwMTY2My4xLjAuMTcyMTgwMTY2My4wLjAuMA.](https://ebooks.iospress.nl/volume/formal-ontology-in-information-systems-proceedings-of-the-11th-international-conference-fois-2020?_gl=1*1imoqcs*_up*MQ..*_ga*MTI0MjQwMjYxNC4xNzIxODAxNjY0*_ga_6N3Q0141SM*MTcyMTgwMTY2My4xLjAuMTcyMTgwMTY2My4wLjAuMA)
- Gruber, T. 2016. Ontology. In L. Liu and M. T. Özsu (eds), Encyclopedia of Database Systems, 1-3. New York, NY: Springer. https://doi.org/10.1007/978-1-4899-7993-3\_1318-2.
- Guberek, T., and R. Silva. 2014. Human Rights and Technology: Mapping the Landscape to Support Grantmaking . Ford Foundation. Partners  for  Human  Rights  Information,  Methodology  &amp; Analysis (PRIMA). https://www.fordfoundation.org/work/learning/research-reports/human-rights-andtechnology/
- Hanseth,  O.,  and  K.  Lyytinen.  2010.  Design  Theory  for  Dynamic  Complexity  in  Information Infrastructures: The Case of Building Internet. Journal of Information Technology (Sage Publications Inc.) 25(1): 1-19. https://doi.org/10.1057/jit.2009.19.
- Harrison,  J.,  D.  Maynard,  and  S.  Torsner.  2020.  Strengthening  the  Monitoring  of  Violations  against Journalists through an Events-Based Methodology. Media and Communication 8(1): 89-100. https:// doi.org/10.17645/mac.v8i1.2543.
- Johannesson, P., and E. Perjons. 2014. An Introduction to Design Science (2014, 1st ed.). Cham, Heidelberg, New York, Dordrecht, London: Springer. https://link.springer.com/book/10.1007/978-3-030-78132-3
- Land, M. K., and J. D. Aronson. 2018. The Promise and Peril of Human Rights Technology (Introduction). In New Technologies for Human Rights Law and Practice , 1-20. Cambridge: Cambridge University Press. https://doi.org/10.1017/9781316838952.

- Lindeberg,  J.  2023.  Practitioner  Survey  from  Human  Rights  Ontology  (OntoRights)  Study  (dataset).  Harvard  Dataverse.  https://doi.org/10.7910/DVN/IITKTQ. Version no. 1. Date of deposit 18 September 2023. Date accessed 22 July 2024.
- Manual  on  Human  Rights  Monitoring.  2011.  OHCHR.  https://searchlibrary.ohchr.org/record/4835 (accessed 1 March 2022).
- Nguyen,  V.  2011. Ontologies  and  Information  Systems:  A  Literature  Survey .  Defence  Science  and Technology Organisation Edinburgh (Australia). https://apps.dtic.mil/sti/citations/ADA546186
- Pirac é s, E. 2018. The Future of Human Rights Technology: A Practitioner's View. In M. K. Land and J. D. Aronson (eds), New Technologies for Human Rights Law and Practice ,  289-308.  Cambridge: Cambridge University Press. https://doi.org/10.1017/9781316838952.
- Poblet, M., and J. Kolieb. 2018. Responding to Human Rights Abuses in the Digital Era: New Tools, Old Challenges. Stanford Journal of International Law 54(2): 259-84.
- Sunstein, C. R. 2006. Infotopia: How Many Minds Produce Knowledge . Oxford: Oxford University Press. Uschold,  M.,  and  M.  Gruninger.  2004.  Ontologies  and  Semantics  for  Seamless  Connectivity. ACM SIGMOD Record 33(4): 58-64. https://doi.org/10.1145/1041410.1041420.
