## Ontology for Structuring a Digital Databases for Decision Making in Grain Production

Ricardo A. Neves 1,2,3 , Paulo E. Cruvinel 1,2

1 Embrapa Instrumentation, São Carlos, SP, Brazil

2 Post-Graduation Program in Computer Science - Federal University of São Carlos, SP, Brazil

3 Federal Institute of São Paulo, São João da Boa Vista, SP, Brazil

Emails: ricardo.alexandre@ifsp.edu.br, paulo.cruvinel@embrapa.br

Abstract -This paper presents an ontology for the structuring of  digital  databases  with  the  objective  of  acting  in  a  cloud environment  and  meeting big  data sources in  the  agricultural context of grain production. Its conception is structured in three stages: the first stage presents an ontological architecture aimed at public and private cloud environments, the second stage deals with  a semantic  model  at  process  level, and a  pseudocode  for ontological application is elaborated in the third stage, considering  the  technologies  applied  to  the  cloud.  This  work combines  advanced  features  to  support  decision  making  from Data Lake storage  solutions,  semantic  treatment  of big  data , as well as the presentation of strategies  based on machine learning and data quality analysis to obtain data and metadata organized for  application  in  a  decision  model.  The  configuration  of  the ontology presented meets the diversity of big data projects in the grain production context, the characteristics of which are based on  interoperability  in  the  use  of  heterogeneous  data  and  its integration, elasticity of computational resources, and high availability of cloud access.

Index  Terms-Ontology; Agriculture; Digital  Database; Cloud Computing; Big Data; Decision Making.

## I. INTRODUCTION

Computational models based on the use of data to characterize  decision-making processes  in  agriculture  have increasingly occupied space in the productive sector [1]-[5]. In management practices based on information agriculture, which uses  decision support, productivity  gains have  been  found, as well as better use of agricultural inputs [6][7]. In general, databased  decision-making algorithms need  to  consider  structures that make it possible to work with different data or even large amounts of data. In this context, the use of big data has become a common practice [8][9].

Big  data has  significant  potential  to  address  the  issues  of modern societies, including the needs of consumers, financial analysts, marketing agents, producers, and decision makers. To effectively manipulate big data information, organizations need data integration between different data sources. Data integration deals with the heterogeneity of the syntactic, schematic or semantic structure of big data sources [10][11].

In  agriculture  today,  development  of  cloud  infrastructure architectures had  become  essential  to  serve  an  increasingly demanding public  in the area  of information  consumption, through integrated  data  from  big  data sources.  For  decision making in the agricultural context, from the perspective of risk analysis,  which  involves  the  management  of  digital  data  with an explicit  need  to  deal  with  the  integration  of  big  data, requires  a computing  infrastructure  with  characteristics  of robustness, flexibility, elasticity, high availability, interoperability  and  affordable  cost  as  to  the  technologies, to enable  the  storage  and  processing  of  data  in an  efficient  and secure way [10][12].

Algorithms developed to work with big data, either through image and signal processing methods [13] or pattern recognition [14] or  machine learning [15],  are  increasingly dependent  on  platforms  that  operate  in a  distributed  and/or parallel way to be executed.

According  to Tan in  (2016), addresses the  problem  of scarcity  of  decision  support  systems to  minimize  humancentered decisions [12]. The issue also envisages the development  of  a  better  decision-making support  system  for the  special  crops  industry, taking in to account the challenges in the field of information technology. The approach developed by  the  author  is  based  on  the  context  of  precision  agriculture and allows  the  acquisition of  data  from  different sources,  the synthesis  of  application-specific  decisions,  and the  control  of field devices through the use of cloud technology.  The approach has outstanding features such as an extensible architecture  and  a  device-independent  front-end,  capable  of processing input data in a variety of formats and semantics. In this  aspect,  cloud computing has  become a differential in the architecture developed by the author, presenting itself as a key element of the solution developed. By working with heterogeneous  databases,  given  their  complexity  in obtaining results, the  use  of  data integration in  its  different  sources and formats,  which  can  be  of  public  or  private  origin,  of  devices interconnected  by  sensor  networks  with  Internet  of  Things (IoT)  technology  or  obtained  by  satellites, drones, time  series data, among others, has been observed.

The construction of an effective approach, in terms of the semantic  structuring  of  digital  databases,  has  been  presented previously int  the  literature [5][16]. Such  publications  have presented solutions  in  the  area  of  big  data , which  seek  to integrate  heterogeneous  databases  to  meet  the  demands  of precision agriculture and digital agriculture, to support decision-making in agricultural risks.  The structured  database can  be  used in  robust  and/or  intelligent  systems to  provide semi-automated  or  automated  solutions so  that  agricultural producers can anticipate, avoid and/or react to shocks resulting from negative externalities that may occur in crop areas [16].

Sheu and  collaborators have  defined that  the connection between content and the user can be made through five aspects [17].  The  first  aspect is  semantic  analysis,  responsible  for analyzing the content to convert it into a semantic description. The  second  aspect is  semantic  integration,  which  aims to integrate  content  and  semantics  from  multiple  sources.  The third aspect was considered as semantic services to use content and  semantics  to  solve  problems.  The  fourth  aspect  is the integration  of  services to  integrate  different  types of  services for the purpose of enhancing services. Finally, the fifth aspect addresses  the  semantic  interface, aimed  at  permeating  the interpretation of user intentions in a natural way.

According to Alqahtani and Rilling in (2019), the semantic web and its technology stack are introduced to address knowledge sharing from heterogeneous data resources [18]. In addition, Hull  and  King in  (1987) have  presented  a semantic modeling, which provides  rich  data  structuring  resources to complement  the  work  of  representation, interrelationship,  in situations involving  complex structures and knowledge, under different aspects, such as artificial intelligence and the generation  of  database models and  also the  semantic  web depends on a unified ontological representation that is capable of standardizing, sharing and performing data analysis, beyond the frontier of knowledge [19].

The literature presented approaches to addressing the issue of  data  integration  under  the  big  data context.  Fathy  and collaborators presented an overview of different approaches for integrating big data sources through a unified semantic model [20]. The first approach consists of using the ExtractTransform-Load (ETL) process to integrate data from various sources in three phases: (a)  extraction,  (b)  transformation and (c) load, where in phase ' c ' the Data Mart or Data Warehouse structure  is  considered  for  data  storage to  serve  as  big  data infrastructure.  The second  approach  deals  with the  semantic reduction focusing on the industrial automation domain, which works with structural heterogeneity because data are extracted from sources in Extensible Markup Language (XML) formats, text files and databases. The third approach is the semantic big data approach.  Its  aim is  to  aggregate  and integrate  different geospatial  data resources  from  the  web,  followed  by  their transformation into Comma-Separated Values (CSV) data files, and with the next step, an algorithm is applied to generate the Resource Description Framework (RDF) model, using generic spatial  ontology  and  an Application Programming  Interface (API)  to  convert CSV  data  into  RDF.  The  fourth  approach focuses on the modular ontology construction approach for the integration of big data integration presented in three steps. The first steps groups the source data into a non-relational document-based database, MongoDB,  as an intermediate representation between big data and ontology. The second step includes  the  generation  of  ontology modules  for  each  data source,  using the  Ontology  Web  Language (OWL)  and the MongoDB  database from the  transformation  rules.  The  third and final step  consists  of combining the  ontology modules to obtain a global ontology, following a  compositional approach.

The  fifth  approach  presents  the  query  translation,  known  as Ontology-Based Data  Access (OBDA) to  provide  a  global scheme on data sources in ontology. Thus, mappings between the global schema and the data sources are defined. The sixth approach  proposes an  OBDA  application  for  non-relational databases (NoSQL) by the authors. This is extended as a new functionality  for the Ontop  system, used to  work  with OBDA for relational databases. In this context, the MongoDB database was  used  to  test  the  new  architecture.  Finally,  the  seventh approach also proposes to extend functionalities of the Sparklmap tool (SPARKL-to-SQL), with the aim of accessing non-relational data, from a relational view of document storage.

Besides, Ostrowski and Kim [21], Chittayasothorn [22], as well  as Ramadhan and  collaborators [23] have all presented different  approaches  for  using big data integration, using semantic  models  based  on  ontology.  Further, Ostrowski and Kim  have also presented an efficient solution for data integration  by  extracting  and  combining  data  from  various heterogeneous sources. However, such a solution considers the use of a multilayered application system that acts on heterogeneous distributed data sources, i.e., dealing with semantic heterogeneity through visualizations and RDF services with the domain ontology [24].

In fact, the semantic integration is a process that consists of linking data based on conceptual  representation  and  data relationships, with a goal  of  generating a  global  scheme  with the purpose of integrating several different schemes. The use of ontologies is one of the most relevant methods of correspondence for the integration  of  semantic-based schemas to support semantic heterogeneity. The main difference between traditional data integration and ontological integration is the provision of information in an integrated view about the domain, taking into  account the relationship between  the concepts [20][24].

According  to Guizzardi and collaborators, the Unified Fundamental  Ontology  (UFO) is  defined  as  a  fundamental ontology that provides a solid ontological approach for evaluating and providing semantics  of  the real  world used in the  construction  of  semantic  models  from languages  such  as Unified Modeling Language (UML) [25]. To meet the purpose of representing the ontological approach UFO,  the class diagram of UML 2.0 has been adapted, taking into account the concepts  of UFO, resulting  in  a  version  capable  of  providing subsidies for the development of ontology-based diagrams. The new representation has been named OntoUML. To support the development  of  OntoUML metamodels,  an  OpenSource tool called OntoUML Lightweight  Editor was  developed with a plugin  for  use  in  the  commercial  visual  paradigm  tool. From the development of the OntoUML diagram, the tool enables the generation of code in OWL and Semantic Web Rule Language (SWRL). SWRL is a language used to express logical rules for the OWL specifications. However, with the use of plugin, it is possible to use the gUFO language (Lightweight Implementation  of Unified  Fundamental  Ontology) and  also the JSON (JavaScript Object Notation) format for exporting the OntoUML diagram [26].

This  work  presents  a  model  to  predict  an  ontology  for structuring digital databases for decision-making in grain production. The paper  is  structured  as  follows: Section  II presents  the  materials  and  methods;  Section  III  refers  to the results  and  discussions  and,  finally,  Section  IV  presents  the conclusions.

## II. MATERIALS AND METHODS

The  databases  used  for  the  elaboration  of  the  ontology originate from  public  data  sources  available  on  the  Internet. Therefore, data from satellite images, soil, plants, geolocation, weather stations, and other agricultural management variables are  obtained  from  these  databases. In  addition, data  from private  sources are considered and made possible through the rural property sensor networks and their field truth devices.

With  the  infrastructure adopted,  the use of the  cloud environment and its technologies are considered in two aspects: (1) Private cloud environment; and (2) Public cloud environment.  The private cloud environment presents the structures  responsible  for  receiving  big  data and  other  steps envisaged for the storage, management, processing, treatment, analysis  and  availability  of  results.  However, in the  public cloud environment, access via connection to the Internet network is envisaged to obtain the public data.

## A. Methodological design

The methodological process  used to  develop  the  ontology for structuring of digital databases has been divided into three stages: in the first stage an architecture has been developed for understanding of the domain from the perspective of semantic infrastructure, at the macro level of detail; in the second stage a refinement  diagram  of  the  architecture  has  been developed, with  greater  detail  of the  processes  and, finally,  in  the third stage, the diagram is unfolded into pseudocode.

The architecture has be designed to work in cloud environment  due  to  the  demands  established  by  processes  of precision agriculture [26], digital agriculture [27], and agriculture 4.0 [28], justified by the need to receive, transform, process and analyze large volumes of big data, considering its diversity  and heterogeneous  characteristics. These needs meet the  requirement  to  use a modern  computational infrastructure that is  flexible,  integrated, elastic from  the  perspective of increasing  or  decreasing  processing  power  and  access, on demand, without losing sight of performance, high availability of access to parallel and distributed processing resources.

Figure 1 presents, in a block diagram, the ontology for the semantic  structuring of  agricultural  environment  databases, which  is  implemented  in  the  context  of a cloud  computing structure.

Cloud  infrastructure  can  be  either  public  or  private.  The public  cloud is  maintained by  third  parties  and  the  data  of different users  is  stored  or  shared in the  infrastructure  servers located in data centers on the Internet  network  domain. However,  the  private  cloud, also called  internal  cloud or corporate  cloud, has a  proprietary  computing  architecture that provides services to authorized users [29].

As shown  in  Figure  1,  the  infrastructure  represented  as public cloud is responsible for making big data available to the private cloud infrastructure. In this case, this may occur in the context of a central server, when field truth data are obtained from sensor networks operating with IoT technology [30], in different farms  or  institutions. Alternatively, data  can  be obtained from a server, which operates on an Internet network, via a data  communication  link, which  is  customized  to  the application and  operates at high  speed  and low  latency.  This type  of  link  can  be  contracted  by a  telecommunications operator. The second  way  is  to  obtain  the  data  through  a connection to  public  institutions  providing access  to  climate, image, soil, plant data and other variables directly through the Internet network.

Figure 1. Ontology architecture for semantic structuring of digital databases

[FIGURE]

The private network structure comprises of the following: (1) data  lake: acts  in  receiving  data prepared  to  work  with heterogeneous  big  data; (2) semantic analyzer;  (3)  semantic repository with the use of class-based ontology; (4) block data preparation;  (5)  block  analysis  of  data  quality  requirements; (6) block data vector; and, finally, (7) block organized data for use in decision model.

The processes used includes detailing of the architecture of the  model  for  semantic  and  ontological  structuring  of  the digital database to support decision making in agricultural risk can be evaluated, as shown in Figure 2.

The processes were mapped in UML 2.0 language using the activity  diagram.  The  diagram  maps,  in  its  first  phase,  the activities related to the private cloud context, separated in five blocks, whose details are described below: Block 1 connects to the  big  data databases to  read and  browse  the  data in the databases,  being  able  to  be  structured,  semi-structured  and unstructured; Block 2 deals with the preparation of the data in its initial phase, that is, the receipt of ' raw ' data via Data Lake. The  data  are stored in  internal  data  lake structures  called buckets. You can create a bucket to store each database context so  that  it  is  organized;  Block  3  works  with  two  algorithms designed to be developed as REST services. These algorithms have the function of distributing data which are stored on the Data  Lake to the semantic database structure. The first algorithm called distribute data accesses the Data Lake buckets,  retrieves  the  data,  and  according  to  the  metadata information recorded by the bucket, of each data retrieved, the algorithm inserts this data into the semantic database structure. Such  semantic  structure  information  is  provided  to  distribute data by the second algorithm called check agricultural ontology .

The two functionalities together, referring to the two algorithms represent step ' 2 ' called semantic analyzer; Block 4 applies machine learning algorithms for the mining and preparation of data, through the application of  filters; Block 5 applies  algorithms  to  do  the  data  fusion  step,  taking  into account  that  the  data  may  have  different  granularities  and magnitudes. After the fusion, the data will be made available in a data  vector,  organized  so  that  it  can  be  used  in  decision making processes for grain production.

Figure 2. UML diagram for the semantic structuring model of digital databases

[FIGURE]

To  make the  semantic  architecture  possible, as  shown  in Figure 1, as well as its details, according to the UML diagram in  Figure  2, a pseudocode  has  been developed, according  to Figure 3, so that it can represent the ontology developed, in a way that allows the use of different technologies, aiming at its practical application, from the point of view of cloud technologies.

With  the  pseudocode structure  presented,  it  is  possible  to observe  the  establishment  of  an  excellent  operational  merit figure (Benefit/Cost),  considering  the  efficient  use  of  cloud computing resources, the improvement of energy consumption and  the  allocation  of  physical  space in data  centers.  In  this approach  model,  the  rural  producers,  when  configured  as  a market product, will employ financial courses only for the time of use of the architectures hired by operators operating in this market, such as Oracle, Amazon  Web  Services  (AWS), Google , among others.

## II. RESULTS AND DISCUSSIONS

To  configure  a  case  study  scenario  applied  to  agricultural risk analysis,  an  OntoUML diagram characterizing grain production is presented in Figure 4.

Figure 3. Pseudocode -Semantic structuring of digital databases

[FIGURE]

Figura 4. OntoUML diagram -Grain production case study based on support decision computational model

[FIGURE]

As part of the results obtained for this work, the OntoUML diagram in Figure 4 represents the ontology constructed from an  agricultural  context, which  considers  the  main  aspects  for grain  production:  weather  station  data  (relative  air  humidity, accumulated precipitation, minimum and maximum temperatures, foliar wet duration); digital imaging data (satellite  images  and  NDVI index);  and  states  of  production evolution.

The diagram presented in Figure 3 was developed using the UML 2.0 concept, through the class diagram, using stereotypes from UFO Ontology. This technique is known as OntoUML.

To implement the OntoUML structure foreseen in this case study,  the  OntoUML diagram  was  developed based  on  the gUFO language  (light  implementation  of the  fundamental unified ontology) and can be seen in Figure 5. With this code it is  necessary  to  implement  it in  a  server  with  support  for semantic  database  resources.  Next, two  servers  are  suggested that  can  be  used  in  a  free and  OpenSource  way  for  the implementation of the code: OpenLink Virtuoso and Blazegraph [31][32].

The code generated for the developed ontology is written in N-Triples format  which,  according  to  the  World  Wide  Web Consortium  (W3C), is an  online  syntax to  encode  a graph  in RDF. N-Triples are a reference of RDF terms that represent the triple:  the  subject,  the  predicate  and  the  object.  They can  be separated  by  whitespaces  or  tabs  and  are  terminated  by  a  dot [33]. The semantic database with the use of ontology allows the use  of  SPARQL language  searches, and is also  supported by most conventional databases, such as Mysql and Oracle.

Figure 4. Code generated: OntoUML -Risk analysis-based grain production case study

[FIGURE]

The results of  this  work  address  a  set  of  four  aspects that translate the  ontology  for  grain production. The  first aspect is an ontology architecture for the semantic structuring of digital databases.  The  second  aspect  is  represented  by  the  semantic model, detailed at the  process level. The third aspect  presents an algorithm of the process model.

In fact, the fourth aspect shows  the ontology in the OntoUML diagram configuration, as well as the configuration expressed in code in N-Triples format, to detail its sequence of terms in the  triple  subject,  predicate and  object,  according  to the data provided in the case study.

The results clearly presented that ontology demonstrates, in a clear and complete way, the specification of concepts in the agricultural field of grain production, as well as their relationships. Ontology has brought  the  understanding  of  the domain  in a  complete  cycle, including the  infrastructure,  the process  model,  the  pseudocode  consolidation , the  OntoUML representation, as well as the implementation code.

In addition, it was considered plausible that, the difficulties with  data  integration presented in  the  context of agricultural ontology, were minimized from the use of cloud technologies due  to the flexibility of access to public and/or private databases,  and  also  due  to the  use  of  the  data lake storage structure.  Other gains have  been made from the infrastructure used, such as the elasticity of the computational infrastructure size, the  high  availability  that  guarantees  access  to  databases and interoperability because it works with heterogeneous data.

The use  of data  mining  algorithms in  the  context of machine learning has effectively subsidized the analysis of big data datasets  in  an  agricultural  environment.  In  addition  to contributing  directly  to the data  preparation  stage  by  bringing direct benefits  to  knowledge  discovery,  it  also  supported  the data quality analysis stage.

Finally, the use of REST services in the semantic analysis infrastructure block has made it possible to automate processes both  for  searching for data  in  big  data and for  loading  and distributing  this  data  in  the  semantic  database,  to  make  the semantic  model  for  structuring  databases  dynamic  from  the functional point of view of their processes.

## III. CONCLUSION

An ontology was presented for the semantic structuring of a digital database to aid decision making in grain production. Its structuring  enables a  better  understanding  of data  for  use  in agriculture.  Further,  it provides  opportunities  for intelligent searches, considering the semantic infrastructure, from the use of data in  big  data arrangements.  In  the  method  developed, strategies to  support  data  processing  and  analysis  of  quality requirements have been  adopted.  To  meet  this  context,  the results presented considered the use of data mining algorithm based on machine learning for the discovery of expert knowledge  attributes  of  the agricultural  sector.  In  addition, REST-based  algorithm services  were  employed  for  semantic analysis,  enabling  the automation  and  effectiveness  of  these processes. Therefore, to establish the developed method, it was necessary  to  use  advanced  computing  resources to  adopt private  cloud  services,  such as the  data lake  storage  structure, semantic  repository, and  communication  interface  between public and private clouds. As future work, the evolution of the ontology is suggested so that the performance, in the decisionmaking scenario in grain production, is carried out in real time.

## ACKNOWLEDGMENTS

This scientific research is being supported by the São Paulo Research Fondation (Process 17/19350-2, FAPESP/IBM/ Embrapa), the Federal University of São Carlos (UFSCar/PostGraduation  Program in Computer  Science), and the  Federal Institute of  Education, Science and Technology  of  São  Paulo (IFSP/ São João da Boa Vista).

## REFERENCES

- [1] C. de  F Fernandes, ' Diseases of bananiculture: sigatoca-negra, ' Embrapa Rondônia-Circular Técnica (INFOTECA-E), 2005.
- [2] Cruvinel et al., ' Evaluation  of  models  to  establish  a risk  figure  for Sigatoka-Negra occurrence in banana plantations, ' Embrapa Instrumentation-Documents (INFOTECA-E), 2011.
- [3] Erol et  al., Data  Mining  models  for  selection  of  the  best  spectral reflectance  indices  in  estimation  of  crop  yields  and  classification  of maize hybrid  types using  spectroradiometer  data, ' in 2017 Eur. Conf. Elec. Engineer. Comp. Sci. (EECS). IEEE, 2017. pp. 180 -187.
- [4] F. Silva, R. L. Manzione,  and A. H. De  Castro  Teixeira, ' Spatial modeling of evapotranspiration and water productivity in the São Paulo portion of the Guarani aquifer outcrop between 2013 and 2015, ' Holos Environ., vol. 18, n. 2, pp. 126 -140, 2018.
- [5] R. A. Neves and P. E. Cruvinel, ' Model for semantic base structuring of digital data to support agricultural management, ' in 2020 IEEE 14th Int. Conf. Semantic Comp. (ICSC). IEEE, 2020. pp. 337 -340.
- [6] M. T. Stefanello et  al., ' Effect of  the  interaction  between  fungicide application  time  and  rainfall  simulation  interval  on Asian  Soybean Rust  control  effectiveness, ' Semina: Ciências  Agrárias,  vol.  37,  n.  6, pp. 3881 -3892, 2016.
- [7] A. M. Balasha, ' Drivers  of  adoption  of  integrated  pest  management

- among  small-scale  vegetable farmers  in  Lubumbashi,  DR  Congo, ' American J. Rural Dev., vol. 7, n. 2, pp. 53 -59, 2019.
- [8] N. Tantalaki, S. Souravlas, and M. Roumeliotis, ' Data-driven decision making  in  precision  agriculture:  The  rise  of  big  data  in  agricultural systems, ' J. Agri. Food Inform., vol. 20, n. 4, pp. 344 -380, 2019.
- [9] G. Pal, K. Atkinson, and G. Li, ' Managing heterogeneous data on a big data platform: A  multi-criteria decision making  model  for dataintensive science, ' in 2020 IEEE Int. Conf. Big Data and Smart Comp. (BigComp). IEEE, 2020. pp. 229 -239.
- [10] Coble et al., ' Big data in agriculture: A challenge for the future, ' Appl. Econ. Persp. Policy, vol. 40, n. 1, pp. 79 -96, 2018.
- [11] A. O. Alkhamisi and M. Saleh, ' Ontology opportunities and challenges:  Discussions  from  semantic  data integration  perspectives, ' in 2020 6th Conf. Data Sci. Mach. Learn. App. (CDMA). IEEE, 2020. pp. 134 -140.
- [12] TAN, Li. Cloud-based decision  support  and  automation  for  precision agriculture in orchards. IFAC-PapersOnLine, v. 49, n. 16, p. 330-335, 2016.
- [13] ALVES, Gabriel M.; CRUVINEL, Paulo E. Big data infrastructure for agricultural  tomographic  images  reconstruction.  In:  2018  IEEE  12th International Conference on Semantic Computing (ICSC). IEEE, 2018. p. 346-351.
- [14] R. Varatharajan, G. Manogaran, and  M.  K. Priyan, ' A  big  data classification approach using LDA with an enhanced SVM method for ECG signals in cloud computing, ' Multimedia Tools and Applications, vol. 77, n. 8, pp. 10195 -10215, 2018.
- [15] Y. Mekonnen et al., ' Machine learning techniques in  wireless  sensor network based  precision  agriculture, ' J. Electrochem. Society,  vol. 167, n. 3, p. 037522, 2019.
- [16] S. Rajeswari, K. Suthendran, and K. Rajakumar, ' A smart agricultural model by integrating IoT, mobile and cloud-based big data analytics, ' in 2017 Int. Conf. Intell. Comp. Control (I2C2). IEEE, 2017. pp. 1 -5.
- [17] P. C.-Y. Sheu et al. (Ed.).  Semantic Computing. John Wiley  &amp; Sons, 2011.
- [18] S.S. Alqahtani and J. Rilling, ' Semantic  modeling  approach for software vulnerabilities data sources, ' in 2019 17th Int. Conf. Privacy, Security and Trust (PST). IEEE, 2019. pp. 1 -7.
- [19] Ri. Hull and R. King, ' Semantic database modeling: Survey, applications, and research issues, ' ACM Computing Surveys (CSUR), vol. 19, n. 3, pp. 201 -260, 1987.
- [20] N. Fathy, W. Gad, and N. Badr, ' Aunified access to heterogeneous big data  through  ontology-based  semantic  integration, ' in 2019 9 th Int. Conf. Intell. Comp. Inf. Sys. (ICICIS). IEEE, 2019. pp. 387 -392.
- [21] D. Ostrowski and Mira Kim, ' A semantic  based  framework  for  the purpose of big data integration, ' in 2017  IEEE  11th  Int. Conf. Semantic Comp. (ICSC). IEEE, 2017. pp. 305 -309.
- [22] S. Chittayasothorn, ' Some key issues in information systems, databases and big  data integration, ' in 2019 5th Int. Conf. Engineer., Applied Sci. Tech. (ICEAST). IEEE, 2019. pp. 1 -4.
- [23] H. Ramadhan et al., ' MusQ: A Multi-store query system for iot data
- using a datalog-like language, ' IEEE Access, vol. 8, pp. 58032 -58056, 2020.
- [24] Y. P. E. Hounguè, K. A. R. Sagbo, and  K. Yetongnon, ' RDF-based web information integration system: A travel system use case, ' in 2018 14th Int. Conf. Signal-Image  Technology  &amp;  Internet-Based  Sys. (SITIS). IEEE, 2018. pp. 500 -507.
- [25] G. Guizzardi et  al., ' Towards  ontological  foundations  for  conceptual modeling:  The  unified  foundational  ontology  (UFO) story, ' Appl. Ontol., vol. 10, n. 3 -4, p. 259 -271, 2015.
- [26] Bernardi et  al., ' Precision  farming:  results  of  a  new  look, ' Embrapa Instrumentation-Technical book (INFOTECA-E), 2014.
- [27] MASSRUHÁ, S. M. F. S.;  LEITE, M.  A.  de  A. Agricultura  Digital. RECoDAF -Revista Eletrônica Competências Digitais para Agricultura  Familiar,  Tupã,  v.2,  n.1,  p.72-88,  jan.2016.  ISSN:24480452.
- [28] R. Hartanto et al., ' Intelligent unmanned aerial vehicle for agriculture and  agroindustry, ' in IOP  Conf. Series:  Earth  and Environ. Sci.  IOP Publishing, 2019. p. 012001.
- [29] S. Singh and T. Jangwal, ' Cost breakdown of public cloud computing and private cloud computing and security issues, ' International Journal of Computer Science &amp; Information Technology, vol. 4, n. 2, pp. 17, 2012.
- [30] F.-H. Tseng, H.-H.  Cho,  and H.-T.  Wu, ' Applying  big  data  for intelligent  agriculture-based  crop  selection  analysis, ' IEEE  Access, vol. 7, pp. 116965 -116974, 2019.
- [31] BLAZEGRAPH, Semantic Web Standards. Available at: &lt;https://www.w3.org/2001/sw/wiki/Bigdata&gt;. Access in: 05/10/2020.
- [32] Server,  OpenLink Virtuoso Universal. Documentation.  OpenLink Software Documentation. Available at: &lt;http://docs.openlinksw.com/&gt;. Access at: 05/10/2020.
- [33] W3C,  Rdf  1.1  N-Triples.  W3c  recommendation,  W3C,  2014.  2014. Available at:&lt;https://www.w3.org/TR/n-triples/&gt;. Access on: 05/10/2020.
