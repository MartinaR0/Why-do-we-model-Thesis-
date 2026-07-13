[FIGURE]

## Towards A Domain Specific Modeling Language For Agent-Based Models In Land Use Science

## Cédric Grueau

Departamento de Sistemas e Informática

Escola Superior de Tecnologia

Campus do IPS, Estefanilha

2910-761 Setúbal, Portugal

cedric.grueau@estsetubal.ips.pt

## ABSTRACT

While Multi-Agent Systems are widely used in Land Use Science, it still remains challenging for scientists to specify their models in a manner that they can be understood and used by others. Domain users require a higher-level language to agents. To overcome this issue, we propose the development of a domain specific modeling language (DSML) for agentbased models in Land Use Science. In this paper, we present the first step towards the development of the DSML, which consists of a domain analysis model for agent-based in Land Use Science.

## Categories and Subject Descriptors

D.2.13 [ Software Engineering ]: Reusable SoftwareDomain engineering ; I.2.11 [ Artificial Intelligence ]: Distributed Artificial IntelligenceMultiagent systems

; I.6.4 [ Simulation and Modeling ]: Model Validation and Analysis

## General Terms

Design, Verification.

## Keywords

Software Product Lines, Multi-Agents Systems, Modeling Language, Land-Use Science.

## 1. INTRODUCTION

Computer-based simulations have become an important asset to understand the complex interactions between human societies and the land resources on which they depend on. Over the last decade, agent-based modeling has been widely used in the field of spatial planning and natural resource management to perform such simulations (see [1] for examples). When building Multi-Agent Systems in Land Use Science (MASLUS), scientists often use graphic languages such

Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. To copy otherwise, to republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee.

SAC'13 March 18-22, 2013, Coimbra, Portugal.

João Araujo Faculdade de Ciências e Tecnologia Universidade Nova de Lisboa Quinta da Torre 2829-516 Caparica , Portugal ja@di.fct.unl.pt

as the Unified Modeling Language to specify and communicate about their models before implementing them using specific frameworks 1 . But the differences between models' objectives, models' specifications and models' implementations hamper the validation, reuse or replication of models. We, thus, propose to develop an approach that follows the paradigm of model driven development [2], a recent field in the software engineering community, to create a domainspecific modeling language (DMSL). Our objective is to provide a framework that would enhance the conception and reuse of models in MASLUS.

## 2. DSML DEVELOPMENT

In this paper we will only focus on the first phase of the DSML development: the domain analysis. The objective of this phase is to produce a domain model that will support the implementation of the DSML.

To identify which features are important for MASLUS, we first proceeded to the analysis of technical literature and identified MASLUS requirements. The results are synthesized in figure 1 which represents the feature diagram (FD) resulting from the application of the Feature-Oriented Domain Analysis, known as FODA context analysis [3]. Below we describe some of the features relevant to MASLUS.

ModelDescription This first feature is expressed as a set of metadata, which describes objectives, authors and versions of the model. In fact, it is important to specify what the goal of the model is. It must be clear if the model has been built for validation, understanding, visualization, training, control, decision-aid, prevision or gaming purpose.

Agent When building MAS, modelers represent explicit entities of the system modeled as agents (e.g. institutions, individuals). The choice of entities depends on the level of abstraction of the reference system under study and on the question to be answered by the model. Agents might be spatially distributed (location feature) and use decision models to choose what decision to make and which action to perform. This feature is related to subfeatures such as the atomic location feature and the DecisonModel feature that encapsulates the rationale necessary for the agent to make a decision. Other parameters are required to define agents' behavior. Those parameters are control, communication, perception, actions or organization. Collectivities are important feature in MASLUS. The NetworkModel fea- ture represents the network model that an agent might need to know to construct the social relations.

1 such as RePast (repast.sourceforge.net)

Figure 1: a partial view of the feature diagram for MASLUS

[FIGURE]

SpatialContext Another essential feature is the environment in which agents interact. Environment in MAS provide services (perception, movements, localization, etc.) and topological structures to agents. The spatial context defines the spatial area that is covered by the model. The agents' environment can be described, using spatial layers that depict institutional, socio-economic, and biophysical data and constraints. Spatial layers are represented spatially using different formats that might be based on tesselation, vector, or graph format.

BiophysicalProcessModel It may also be important to represent spatial dynamics in MASLUS. Modelers may require interfacing the MAS model with other temporally and spatially dynamic models, such as hydrology, transport cost, and erosion models. Modelers working with land use issues often use cellular automata (CA) to model dynamic phenomena that occur over space and relates directly to agents' activity. CAs are adequate to model for example forest fires, flood, or vegetation growth.

SimulationParameters For each model, we need to describe what parameters are used for the simulation. We need to specify what are the rules governing the sequencing and information flows. The representation of time in the model (discrete, continuous or both), the scheduling information (synchronous, asynchronous or events), time step and duration are parameters that might require parametrization. Additional features regarding the number of agents of each type and other socio-economic and biophysical values may need to be defined before initiating a simulation.

## 3. RELATED WORK

To address the ABM limitations, some researchers have focused on building model repositories, such as the Open ABM (www.openabm.org), to provide a locus for authors and modelers to share their models. But the simple access to the model library does not allow for the rigorous and executable comparison between models that we propose in our work. In [4], authors have suggested the use of a Pattern-Oriented approach to composing Agent-Based Models. The approach, implemented as the ODD (Overview, Design concepts, De- tails) protocol, does not integrate a description of the environment, necessary in MASLUS problems, and cannot be directly compiled to computer code.

## 4. CONCLUSIONSANDFURTHERWORK

We have introduced the recurrent challenges that MASLUS are facing to become a mature field of research. We proposed an approach based on the definition of a Domain Specific Modeling Language to respond to these challenges. We performed a domain analysis and contributed to MASLUS field by presenting a feature model that illustrates vocabulary and key concepts of the problem domain. Next step of our work will consist of designing and implementing the DSML.

## 5. REFERENCES

- [1] D. C. Parker, S. M. Manson, M. A. Janssen, M. J. Hoffmann, and P. Deadman. Multi-agent systems for the simulation of land-use and land-cover change: A review. Annals of the Association of American Geographers , 93(2):314-337, 2003. http://dx.doi.org/10.1111/1467-8306.9302004.
- [2] A. van Deursen, P. Klint, and J. Visser. Domain-specific languages: An annotated bibliography. ACM SIGPLAN Notices , 35(6):26-36, June 2000.
- [3] K. Kang, S. Cohen, J. Hess, W. Nowak, and S. Peterson. Feature-oriented domain analysis (foda). Feasibility Study (Report). CMU/SEI-90-TR-21., Software Engineering Institute, Carnegie Mellon University., 1990.
- [4] Volker Grimm, Uta Berger, Finn Bastiansen, Sigrunn Eliassen, Vincent Ginot, Jarl Giske, John Goss-Custard, Tamara Grand, Simone K. Heinz, Geir Huse, Andreas Huth, Jane U. Jepsen, Christian Jørgensen, Wolf M. Mooij, Birgit M¨ uller, Guy Pe'er, Cyril Piou, Steven F. Railsback, Andrew M. Robbins, Martha M. Robbins, Eva Rossmanith, Nadja R¨ uger, Espen Strand, Sami Souissi, Richard A. Stillman, Rune Vabø, Ute Visser, and Donald L. DeAngelis. A standard protocol for describing individual-based and agent-based models. Ecological Modelling , 198(1-2):115 - 126, 2006.
