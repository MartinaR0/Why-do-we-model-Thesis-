## OntoUML Conceptual Model for Egyptian E-Government: Student and Traveler Case Studies

Shaimaa Haridy Faculty of Computer and Information Sciences Ain Shams University Cairo, Egypt shaimaaharidy@cis.asu.edu.eg Rasha M. Ismail Faculty of Computer and Information Sciences Ain Shams University Cairo, Egypt rashaismail@cis.asu.edu.eg Mohamed Hashem Faculty of Computer and Information Sciences Ain Shams University Cairo, Egypt mhashem100@yahoo.com

Abstract -Nowadays,  digital  transformation  has  gained  a great attention in Egypt. The Ministry of Communications and Information Technology (MCIT) seeks to promote the development of the information and communication technologies (ICT) infrastructure and improve digital services in  government  agencies.  E-government  is  one  of  strategic orientation  of  digital  transformation  in  Egypt.  It  improves citizens' quality of life by providing several electronic services that work efficiently and effectively. However rare studies are available on this area in Egypt. So, a new conceptual model will be developed for Egyptian e-Government. OntoUML conceptual modeling language has been adopted. The model has the potential to improve knowledge of crucial issues, particularly in Egypt's e-government development process. It is also  expected  to  be  used  to  assess  the  adoption  of  ICT  in government institutions. This paper presents the case studies of both Student and Traveler consumers.

Keywords -Conceptual Modelling, Ontology, OntoUML, Digital Transformation, E-Government

## I. INTRODUCTION

Information and communication technologies (ICT) plays a  crucial  part  to  create,  access,  process,  and  analyze  the information.  It  facilitates  access  to  government  information and services by making it accessible, accountable, effective and  transparent.  Nowadays  the  governments  are  serving  to different  stakeholders  through  the  internet  instead  of  using traditional  services.  In  the  1990s,  the  term  "e-government" was coined to define the use of information and communication technology (ICT) to improve the activities of government agencies. [1]. Ministry of Communications and Information Technology with Ministry of State for Administrative Development in Egypt have launched the egovernment program. It was divided into two phases, the first phase from 2001 to 2007, and the second one from 2007 to 2012 [2]. COVID-19 has pressed the government to expedite its  goal  of  digital  transformation,  according  to  a  recent analysis on digitization in Egypt by Decode, an economic and financial consultancy firm. For that reason, Egypt increased its ICT investment allocations by 300 percent in FY 2021/22 [3]. [1] explains that many initiatives of the e-government in the developing countries have not been completed successfully.  Therefore,  to  improve  citizen  satisfaction,  egovernment authorities must establish e-government portals with  strong  capabilities.  Figure  1  displays  the  Egyptian  egovernment  portal.  United  Nations  [4]  rank  the  countries according  to  their  e-government  development  index.  The latest rank for Egypt has been reported in figure 2. In 2020 Egypt has been ranked as 111 out of 193 countries.

Conceptual models were developed to help stakeholders better understand and communicate about a system or domain. Ontologies can help improve the quality of conceptual models significantly. [5]. When it comes to the analysis, design, and re-engineering of huge and complicated information systems, they're  believed  to  be  the  most  important.  Many  system engineering gains, like better reliability and reusability , might be achieved if ontologies were used.

Fig. 1. Egyptian E-Government Portal

[FIGURE]

Fig. 2. Egyptian E-Government Development Index [4]

[FIGURE]

For that reason, OntoUML modeling language has been selected to design the proposed model. As it is the only one that has established real-world (ontological) semantics

Nagwa Badr Faculty of Computer and Information Sciences Ain Shams University Cairo, Egypt nagwabadr@cis.asu.edu.eg directly. Furthermore, there is an increasing number of users who  use  this  language  in  a  variety  of  crucial  fields  and complicated models [6].

Therefore,  the  goal  of  this  paper  is  to  design  a  new conceptual  model  using  OntoUML  for  the  Egyptian  egovernment.  The  remainder  of  the  paper  is  structured as follows. Section 2 presents a brief introduction about UFO (Unified Foundational Ontology) and OntoUML. In section 3 the related work has been addressed. Section 4 explains the analysis of the Egyptian portal. A description about proposed model is presented in section 5. Finally, the conclusion will be in section 6.

## II. UFO AND ONTOUML OVERVIEW

In this section a brief description  about  UFO  and OntoUML will be provided. UFO is one of the foundational ontologies that was created by Guizzardi. It is 'an axiomatic formal theory based on contributions from Formal Ontology in Philosophy, Philosophical Logics, Cognitive Psychology, and Linguistics' [7]. According to [8] UFO is the second most utilized foundational ontology in conceptual modelling. OntoUML is a language having a meta-model that conforms to the ontological distinctions and axiomatization of UFO, a theoretically  well-grounded  foundational  ontology  (Unified Foundational Ontology) [9]. It is successfully used in various industrial projects in several domains. In the sequel, a brief explanation about OntoUML class and relationship stereotypes will be presented. For more details refer to [10].

Table 1 summarizes OntoUML Class stereotypes. Sortals provide identity to their instances, however non-sortals do not supply any clear identification principles.  Rigid means  it is necessarily applied to all its instances in all possible scenarios, anti-rigid means is not necessarily applied to all its instances, while semi-rigid represents  shared properties  which  are required  to  some  of  its  instances  but  accidental  to  others. Finally,  Moment  represents  classes  of  elements  that  are existentially dependent on other individuals.

Also,  OntoUML  offers  several  relationship  stereotypes (Formal,  Material,  Mediation,  Characterization,  Derivation, Structuration, Part-Whole, Component  Of, Containment, Member Of, Sub Collection Of, Sub Quantity Of).

TABLE I. ONTOUML CLASS STEREOTYPES

| Class Stereotype   | Sortal   | Non Sortal   | Rigid   | Semi- Rigid   | Anti- Rigid   | Moment   |
|--------------------|----------|--------------|---------|---------------|---------------|----------|
| Kind               | √        |              | √       |               |               |          |
| Subkind            | √        |              | √       |               |               |          |
| Phase              | √        |              |         |               | √             |          |
| Role               | √        |              |         |               | √             |          |
| Collective         | √        |              | √       |               |               |          |
| Quantity           | √        |              | √       |               |               |          |
| Relator            |          |              |         |               |               | √        |
| Category           |          | √            | √       |               |               |          |
| PhaseMixin         |          | √            |         |               | √             |          |
| RoleMixin          |          | √            |         |               | √             |          |
| Mixin              |          | √            |         | √             |               |          |
| Mode               |          |              |         |               |               | √        |
| Quality            |          |              |         |               |               | √        |

## III. LITRETURE REVIEW

The usage of conceptual models in the e-Government area has been explored in some publications. In this section some of  these  works  will  be  discussed.  They  are  organized  into three main groups: The first group contains papers that study the e-government  features  and  measurements  and  how conceptual models can contribute in their enhancement, such as ([11], [12], [13], [14] and [15]). The second group presents conceptual  models  in  case  of  specific  countries  like  ([16] Malaysia, [17] and [18] Indonesia, [19] Egypt, [1] Developing  Countries  in  general).  The  last  group  contains papers that applied OntoUML conceptual modeling in the egovernment domain, such as ([20], [21], and [22]). And this is the most similar group to the proposed research.

[11]  Developed  a  model  for  evaluating  democratic  egovernance  websites.  It's  an  all-encompassing  approach  to assessing a government website. They extended the area of egovernment website analysis by the issue of citizens' engagement, not by their acceptance only. This model aids in the  investigation  of  multidimensional  aspects  that  enable government  websites  to  deliver  the  expected  results  and produce better public results. The goal of study [12] was to look  at  the  aspects  that  influence  user  behaviour  when  it comes  to  e-government  acceptability.  They  found  that  the most  used  model  to  check  e-government  acceptance  is  the TAM model.

The technology acceptance model (TAM) was proposed to  measure  behaviour  of  people  in  acceptance  of  new technologies. So, a conceptual model was suggested based on technology  acceptance  model.  Paper  [13]  concluded  that while  developing  and  testing  conceptual  models,  there  is minimal  agreement  on  the  best  way  to model  citizen satisfaction  and  trust.  They  put  two  popular  e-government satisfaction-trust models to the test: the "expectancydisconfirmation" and "service quality" models. They looked at data collected on citizens' perceptions and experiences of three  essential  federal  e-government  programmes  in  the United States. [14] proposes a generic process model in the agricultural  sector.  End  users  can  participate  in  effective service  delivery  through  a  new  conceptual  approach  to  egovernment development. This programme allows citizens to actively  participate  in  the  design  of  their  services  from relevant  agencies,  as  opposed  to  the  typical  information portal procedure. Authors of [15] are interested in the flip side of the e-government coin: citizen oversight of all governmental entities.  This  occurs  during  the  course  of  all official business and operations. As a result, they developed a new conceptual model that allows citizens to keep track of their government's  activities  by  archiving  governmental transactions and  activities in a publicly available data warehouse. This data warehouse is linked to the portal and available to the public.

In [16] Malaysia has created and validated a conceptual model for digital government service usability. This aids in identifying  the  important  aspects  that  influence  observed usability, which promotes the use and acceptance of digital government services. In [17] Indonesia, a specific egovernment change management model was designed. This model is made up of seven major parts. An action research study  on  governmental entities  can  be  used  to  test  the suggested model. The goal of this research [18] is to find out what factors impact Indonesians' acceptance of eGovernment. As a result, they created a technology adoption model for e-Government. This study was not only concerned with technological aspects, but also with the behaviour and attitudes of its participants. [19] investigates the elements and causes that are necessary for citizens to adopt e-government services in Egypt. They devised a novel model for determining  the  elements  that  influence  the  uptake  of  egovernment services. The model adds a set of political, social,  and  design  constructs  to  the  Technology Acceptance  Model  (TAM)  that  were  culled  from  several research papers. While [1] proposed a study about developing countries in general. They developed a conceptual model for e-government performance in order to determine the aspects that contribute to success from  a business standpoint. perceived  ease  of  use,  quality  of  information, trust,  and personalisation were the four factors they discussed.

Authors of paper [20] built CargO-S, a well-founded legal domain  ontology,  using  OntoUML  conceptual  modeling. This ontology will be used to track products along logistical maritime corridors. They used ontology layering to streamline the process of development by separating CargOS into three levels of different granularity: domain, core, and upper.  A  dual  assessment  approach  is  used  to  assess  the performance  and  accuracy  of suggested ontology. [21] adopted  OntoUML  to  develop  the  Violent  Crime  Process Ontology Network (VCPON). This will be considered as a semantic Enterprise Application Integration (EAI) initiative in the Public Security domain. The ontology supports EAI by capturing the conceptualization underlying different applications to be integrated and providing an 'interlingua'. While [22] proposed a reference ontology for the domain of Brazilian Government Budget using the OntoUML language. The  authors  used  the  ontology  in  Enterprise  Application Integration (EAI) initiative involving two applications (SIOP and SIAF). Those applications are used by Brazilian public agencies.  Finally,  to  consume  and  connect  data  from  the applications, SPARQL queries are applied.

## IV. PROPOSED ANALYSIS

In this section the Egyptian e-government portal [23] is analyzed  and  use  case  diagram  has  been  designed  using Rational Rose tool [24]. In the Egyptian portal, there is 30 different providers offer services to 15 different consumers. The use case diagram helps to represent and summarize the system functionalities without redundancy. Also, it shows the different types of relations between actors and functions.

Service consumers are (citizens, companies, companies' founders, dawns -locals, Egyptians abroad, family, intellectuals,  job  seekers,  lawyers,  neighborhoods,  cities, people  with  disabilities  services,  physicians,  students,  and travelers). On the other side, the 30 service providers in the suggested analysis are classified as follows: (8 ministries, 5 companies, 6 authorities, 2 offices and 9 organizations)

Figures 3 and 4 display use case diagrams of student and traveler  actors  respectively.  As  illustrated  in  figure  3  the student actor is generalized into 5 types of students (secondary azhar, secondary general, technical, nile schools, stem schools). Below are the services offered by the portal to student consumers.

1. Coordinate Arabic equivalent certificates
2. Coordinate Foreign equivalent certificates
3. Register Wishes
4. Ask about wish results
5. Introduce for the equivalence of degrees
6. Inquiry about request for equivalence of degrees

As in figure 4, the functionalities can be done by travelers as follow:

1. Reserve flight
2. Inquire about flight status
3. Check flight schedule
4. Apply for visa
5. Check travel guide
6. Check railway schedule
7. Reserve train ticket

## V. PROPOSED CONCEPTUAL MODEL

In  this  section  Student  and  Traveler  portions  of  the conceptual model has been described. This model has been implemented using OLED  [25]. It is a model-based environment that supports the task of formalization, implementation,  verification  and  validation  of  OntoUML models.

Figure 5 illustrates a portion a bout 'student' class. The 'student' class can enroll in secondary certificate, coordinate his  wishes,  or  make  equivalent  to  his  scientific  degree. Secondary certificate  has  7  certificate  subtypes  (secondary azhar, secondary general, technical, nile school, arab country, and foreign country). The secondary certificate class characterized  by  his  results.  The  scientific  degree  may  be bachelor, masters or PhD.

Figure  6  displays  the  'Traveler'  class.  Traveler  may reserve ticket, check schedule, or apply for visa. Airline and train  tickets  are  available  for  reservation.  The  traveler  can check  flight  schedule,  flight  status,  or  railway  schedule. Finally, Traveler can review the travel guide. The development process of the rest of the conceptual model is ongoing.

## VI. CONCLUSION

This study presents a novel conceptual model for Egyptian e-government. E-government is one of strategic orientation of digital  transformation  in  Egypt.  This  transformation  has gained  a  great  attention  from  Egyptian  administration  and institutions. Although, E-government is one of the large and complex  information  systems.  These  systems  face  many challenges  that  require  high  quality  solutions  to  be  tackled. Conceptual models are critical in such systems for a variety of purposes.  OntoUML  is  one  of  the  conceptual  modeling languages with a rapidly rising user base who utilize it in a variety of key domains. So, The purpose of this work is to design models for two different case studies from the Egyptian e-government  portal  using  the  OntoUML  language.  This model enhances the understanding of important issues in eGovernment development process in Egypt. Moreover, it is expected to be used as an evaluation in government institutions.

In the future work, it is planned to complete the proposed model. Also, an experimental evaluation will be conducted.

Fig. 3. Use Case -Student Actor

[FIGURE]

Fig. 4. Use Case -Traveler Actor

[FIGURE]

Fig. 5. A fragment of proposed conceptual model -Student Role

[FIGURE]

Fig. 6. A fragment of proposed conceptual model -Traveler Role

[FIGURE]

## REFERENCES

- [1] Anas Ghassan Kanaan, Shahizan Bin Hassan, and Arfan Shahzad, 'A  Conceptual  Model  for  E -Government  Success  Factors  in Developing  Countries,'  International  Journal  of  Scientific  and Research  Publications,  vol.  6,  no.  12,  2016,  [Online].  Available: www.ijsrp.org
- [2] Tarek Roshdy Gebba and Mohamed Ramzy Zakaria, 'E -Government in Egypt: An Analysis of Practices and Challenges,'
3. International Journal of Business Research and Development, vol. 4, no. 2, pp. 11 -25, 2015.
- [3] Ahram Online, 'Digital transformation: Egypt's means to build back better,' 2021. https://english.ahram.org.eg/NewsContent/3/12/418543/Business/E conomy/Digital-transformation-Egypt%E2%80%99s-means-tobuild-back.aspx (accessed Sep. 10, 2021).

- [4] United Nations,  'UN  E -Government Knowledgebase,' 2020. https://publicadministration.un.org/egovkb/en-us/Data/CountryInformation/id/53-Egypt/dataYear/2020 (accessed Sep. 10, 2021).
- [5] Michaël  Verdonck,  Frederik  Gailly,  Sergio  De  Cesare,  and  Geert Poels, ' Ontology-driven conceptual modeling: A systematic literature mapping and review,' Applied Ontology, vol. 10, no. 34, pp. 197 -227, Dec. 2015, doi: 10.3233/AO-150154.
- [6] Guylerme  Figueiredo,  Amelie  Duchardt,  Maria  M  Hedblom,  and Giancarlo Guizzardi, 'Break ing into Pieces: An Ontological Approach to Conceptual Model Complexity Management,' 2018.
- [7] Giancarlo Guizzardi, Gerd Wagner, João Paulo, Andrade Almeida, and  Renata  SS  Guizzardi,  'Towards  Ontological  Foundations  for Conceptual Modeling: The Unified Foundational Ontology (UFO) Story,' Applied ontology, vol. 10, no. 34, pp. 259 -271, 2015.
- [8] Michael  Verdonck  and  Frederik  Gailly,  'Insights  on  the  use  and application  of  ontology  and  conceptual  modeling  languages  in ontologydriven conceptual modeling,' in International Conference on Conceptual Modeling, 2016, vol. 9974 LNCS, pp. 83 -97.
- [9] Giancarlo Guizzardi, Ontological foundations for structural conceptual models. Centre for Telematics and Information Technology, 2005.
- [10] Marek Suchánek, 'OntoUML specification Documentation,' 2020.
- [11]  Seulki  LeeGeiller  and  Taejun  David  Lee,  'Using  government websites to enhance democratic E-governance: A conceptual model for evaluation,' Government Information Quarterly, vol. 36, no. 2, pp. 208 -225, Apr. 2019, doi: 10.1016/j.giq.2019.01.003.
- [12] Outstanding Ozen, Hadi Pourmousa, and Neda Alıpour, 'Investigation  of  The  Critical  Factors  Affecting  E -Government Acceptance: A Systematic Review and A Conceptual Model,' 2018. [Online]. Available: http://www.innovativejournal.in/index.php/ijbm
- [13]  Pratyush  Nidhi  Sharma,  Forrest  V.  Morgeson,  Sunil  Mithas,  and Salman  Aljazzaf,  'An  empirical  and  comparative  analysis  of  E -government performance measurement models: Model selection via explanation, prediction, and parsimony, ' Government Information Quarterly, vol. 35, no. 4, pp. 515 -535, Oct. 2018, doi: 10.1016/j.giq.2018.07.003.
- [14] Shah Jahan Miah, 'The role of end user in e -government application development:  A  conceptual  model  in  the  agricultural  context,' Journal of Organizational and End User Computing, vol. 24, no. 3, pp. 69 -85, Jul. 2012, doi: 10.4018/joeuc.2012070104.
- [15] Ahmed Elmorshidy, 'The Other Side of the E -Government Coin: Monitor  from  the  People:  Building  a  New  Double-Sided  EGovernment Conceptual Model,' 2 012. [Online]. Available: http://en.wikipedia.org/wiki/E-Government
- [16]  Rini Yudesia Naswir, Nurazean Maarop, Mahmudul Hasan, Salwani Daud, Ganthan Narayana Samy, and Pritheega Magalingam, 'Towards  a  Conceptual  Model  to  Evaluate  Usability  of  Digital Gover nment  Services  in  Malaysia,'  2019.  [Online].  Available: www.ijacsa.thesai.org
- [17] Darmawan  Napitupulu,  'A  Conceptual  Model  of  E -Government Adoption in Indonesia,' vol. 7, no. 4, 2017.
- [18] Endang Sulistiyani and Tony Dwi Susanto, 'A Conceptual Model of Change Management for E-Government Project in Indonesia,' 2018. [Online].Available:

https://www.prosci.com/resources/articles/change-

- [19] Sara  Elkheshin  and  Noha  Saleeb,  'A  conceptual  model  for  E -government  adoption  in  Egypt,'  in  Proceedings  of  2016  11th International  Conference  on  Computer  Engineering  and  Systems, ICCES 2016, Jan. 2017, pp. 254 -259. doi: 10.1109/ICCES.2016.7822010.
- [20] Mirna El Ghosh and Habib Abdulrab, 'CargO -S:  A  pattern-based well-founded legal domain ontology for the traceability of goods in logistic sea corridors,' Applied Ontology, vol. 16, no. 3, Jul. 2021, doi: 10.3233/AO-210250.
- [21] Lucas  A  Santos  et  al.,  'Using  an  Ontology  Network  for  Data Integration: A Case in the Public Security Domain,' 2018.
- [22]  Archimedes Alves Detoni, Lucas Bassetti Rodrigues Fonseca, João Paulo Andrade Almeida, and Ricardo Almeida Falbo, 'A Reference Ontology  for  Budgetary  Authorization  and  Execution  of  Public Expenditure,' iSys - Brazilian Journal of Information Systems, vol. 11, no. 3, Dec. 2018, doi: 10.5753/isys.2018.369.
- [23] 'Egyptian EGovernment Portal.' http://www.egypt.gov.eg/english/home.aspx (accessed Feb. 15, 2021).
- [24]  Wendy Boggs and Michael Boggs, Mastering UML with Rational Rose 2002, vol. 1. Alameda: Sybex, 2002.
- [25]  John Guerson, Tiago Prince Sales, Giancarlo Guizzardi, and Paulo A Almeida, 'OntoUML  Lightweight Editor A model -based environment to build, evaluate and implement reference ontologies,' in  2015  IEEE  19th  International  Enterprise  Distributed  Object Computing Workshop, 2015, pp. 144 -147.
