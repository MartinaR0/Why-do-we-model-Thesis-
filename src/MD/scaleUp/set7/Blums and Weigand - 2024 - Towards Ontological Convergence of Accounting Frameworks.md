## Towards Ontological Convergence of Accounting Frameworks

Ivars Blums 1,*, †  and Hans Weigand 2,*, †

1 SIA ODO, Riga, Latvia

2 University of Tilburg, The Netherlands

## Abstract

Converging  and  matching  frameworks,  standards,  and  ontologies  is  crucial  for  achieving  semantic interoperability,  integration,  and  alignment  of  information  across  different  systems  and  domains.  The corporate reporting domain, like many others, is governed by a complex array of accounting, financial reporting, and sustainability standards. This paper presents a novel approach to addressing the convergence challenge between the IFRS and US GAAP Conceptual Frameworks for Financial Reporting by grounding them in UFO-based upper ontologies. A converged ontology is developed and modeled in OntoUML, with the resulting converged concepts defined and discussed.

## Keywords

IFRS, US GAAP, Conceptual Framework, UFO, OntoUML, COFRIS, Convergence †

## 1. Introduction

Converging and matching frameworks, standards, and ontologies is an essential process in achieving semantic interoperability, integration, and alignment of information across different systems and domains. When ontologies are created independently, they may differ in structure, terminology, or granularity, making it necessary to converge them for a unified understanding and use. Converging ontologies is a complex but critical process to achieve semantic consistency, reduce redundancy, and facilitate  knowledge  sharing  and  integration.  The  process  includes  matching  and  alignment, merging, conflict resolution, foundational ontology alignment, validation, and documentation [15].

The corporate reporting domain, like many others, is governed by a complex array of accounting, financial reporting, and sustainability standards. These standards are developed by various entities - such as regulatory bodies, professional organizations, and industry groups - at different times and across different jurisdictions, leading to inconsistencies and fragmentation. Most of these standards attempt to ground themselves in some form of Conceptual Framework (CF) to ensure coherence and provide  a  structured  foundation.  However,  harmonization  efforts  have  emerged  to  align  and converge these frameworks, such as International [1] and U.S. [2], reflecting a growing need for consistency  across  different  reporting  systems.  As  the  primary  focus  of  these  frameworks  is  to facilitate standard setting, one of the immediate purposes of a converged framework is to support the joint development and ongoing maintenance of converged standards, such as IFRS 15. It is also important to  help  these  frameworks  adapt  over  time  to  reflect  changes  in  the  market  economy. Notably, the U.S. GAAP's current version is more recent than its IFRS counterpart.

Recent  research  has  introduced  ontological  engineering  methods  to  address  the  formal conceptualization  of  the  International  Accounting  and  Financial  Reporting  Standards  (IFRS) framework [1], conceptualized as the CF Ontology [3, 4]. This approach fosters i nteroperability across various landscapes/domains, addressing ambiguities and enhancing the conceptual consistency  of  the  framework.  As  depicted  in  Figure  1,  such  framework  ontologies  should  be grounded in unified foundational ontologies, in this case in UFO [5] and in an already large set of UFO-grounded core ontologies [6-13]. The next step involves specialization of the CF Ontology for creating IFRS standard ontologies, such as for IFRS 15 Revenue from contracts with customers [14] highlighted in [15]. Furthermore, there is a need for the convergence of different frameworks and standards  and  the  development  of  converged  standards  and  ontologies.  This  paper  explores  the convergence between the CF Ontology for IFRS and the CF Ontology for U.S. Generally Accepted Accounting Principles (US GAAP). Additionally, future research will focus on the connectivity of these  financial  reporting  frameworks  with  sustainability  standards,  addressing  the  increasing demand for integrated reporting that encompasses both financial and non-financial information, and explaining the sustainability-related risks and opportunities arising from an entity's activities and its assets and liabilities [16].

Companion Proceedings of the 17th IFIP WG 8.1 Working Conference on the Practice of Enterprise Modeling Forum, M4S, FACETE, AEM, Tools and Demos co-located with PoEM 2024, Stockholm, Sweden, December 3-5, 2024

*  Corresponding author.

†  These authors contributed equally.

[FIGURE]

[FIGURE]

[FIGURE]

[FIGURE]

The ontological analysis of IFRS and converged standards has uncovered further opportunities for generalization and convergence, extending to the framework level. Upon review and discussion of the proposed ontologies, as well as comparing them with other U FO-based economic and legal ontologies, such as OntoFine [10] and UFO -L [13], it is evident that the conceptualizations introduced vary  or  require  further  meaning  negotiation  and  explication.  Key  concepts  needing  clarification include Economic Resource [11], Control [17, 18], Agency, Transfer [13, 19], Capabilities [12] and Services [13].

Figure 1: Principal diagram of developing Ontologies of Accounting Standards.  Connectivity - a requirement to provide information in a manner that enables users of financial reports to understand the connections between the items to which the information relates and the connections between disclosures provided by the entity [16].

[FIGURE]

The problem of engineering ontology for economics and accounting has been regarded before, e.g. [18], however [3] is the sole documented effort exclusively focused on the (previous iteration of the) IFRS CF itself. Other efforts were devoted to the ontology of Economic Exchange and its use in accounting. Several ontologies for economic exchange were proposed grounded in UFO, and in a recent work, they have been consolidated for standard setting [20].

The research goal of this study is to study the problem of ontology convergence and to create an analysis and core ontology artifact - Converged Conceptual Framework (CCF) Ontology, grounded in the UFO and Core Ontology for Financial Reporting Information Systems (COFRIS) [20], as a formal model for convergence of the frameworks of the International Financial Reporting Standards (IFRS CF) [1] and the United States Generally Accepted Accounting Principles (US GAAP CF) [2].

The overall research frame is Design Science Research where COFRIS [20, 21], as it has been developed along several cycles so far, is the core artifact. The current paper represents a new design cycle; the primary research goal is to validate the usefulness of COFRIS by applying it to the practical purpose of CF convergence and to extend COFRIS if needed.

We start with a concise overview of the IFRS Conceptual Framework, its counterpart within the U.S., and definitions of the used social concepts from UFO-C and COFRIS, in Section 2. In Section 3, we introduce the CCF Ontology in OntoUML and propose motivated suggestions for convergence and generalization of frameworks. Section 4 concludes and outlines further validation work.

## 2. Background

## 2.1. The IFRS Conceptual Framework (IFRS CF)

The International Accounting and Financial Reporting Standards Conceptual Framework (IFRS CF) [1] sets out the fundamental concepts that guide the standard-setters in developing international accounting and financial reporting standards.

The Objective of Financial Reporting is to provide financial information about the reporting entity (aka Enterprise )  that  is  useful  to  existing  and potential investors and creditors in making decisions relating to providing resources to the entity.

Financial  Reports provide  information  about  (a)  the  nature  and  amounts  of  the  entity's Economic Resources and  the Claims against the Entity ;  (b)  the  effects  of Transactions and Other  Events that  change  an  entity's  economic  resources  and  claims;  (c)  the  efficiency  and effectiveness  with  which  the  entity's  management  discharged  their  stewardship  [and  custody] responsibilities.

## 2.2. The US GAAP Conceptual Framework (US GAAP CF)

Numerous other accounting  and financial  reporting  frameworks  exist,  each  tailored  to  different activities and jurisdictions. A significant counterpart to the IFRS CF is the United States Generally Accepted Accounting Principles Conceptual Framework for Financial Reporting (US GAAP CF) [2]. US GAAP CF shares the same purpose and objective as IFRS CF. However, while there is a declared intention to minimize differences across these frameworks and standards, considering variations in legal, regulatory, or social norms [2], there are substantial specificities, and in 2014 the joint work program was discontinued. Generally, the US GAAP CF seemingly contains a broader array of core concepts than in IFRS CF, such as specific Transactions and Other Events, Economic Exchange, and Service Provision [2]. The US GAAP Framework defines ten core elements in contrast with IFRS CF's five elements [1]. The US GAAP CF has dismissed the asset control and custody concepts present in IFRS CF and exhibits differences in core element sets and definitions.

## 2.3. Unified Foundational Ontology (UFO)

Unified Foundational Ontology (UFO) is an axiomatic domain-independent formal Theory. UFO is divided  into  three  layered  compliance  sets:  UFO-A,  an  ontology  of  concrete endurants -  of substantials and aspects [5],  UFO-B,  an  ontology  of events [6],  and  UFO-C,  an  ontology  of intentional and social entities [7]. OntoUML is a language whose meta-model has been designed to comply  with  the  ontological  distinctions  and  axiomatization  put  forth  by  UFO  [8].  OntoUML diagrams (e.g., Figure 2) represent types ‡ .

Social  commitments  and  claims specialize social  aspects [7].  A social  commitment is  the commitment of an agent (a committer ) against another agent (a claimer ). As an externally dependent mode , a social commitment is a characterization of the committer, has externalDependence on the  claimer,  and causes the creation of an internal  commitment in  the  committer  [7].  Also, correlative to this internal commitment, a ( comparative ) social claim of the claimer against the committer is created. Commitments and claims always form a pair that refers to unique propositional content. A social relator, mediated by agents, is an example of a relator composed of correlative commitments/claims. Actions are intentional events ,  i.e.,  events that are performed by agents to satisfy  their  goals.  Actions  are manifestations of  agent  modes  and  action types  are specified  in commitment schedules or through committed resource types [7].

‡  OntoUML diagrams encompass both first order and higher-order types. For our modeling approach, we distinguish entities based on their instantiation status within the model. If an entity exists as an actual instance after the model's instantiation, such as a specific Tesla Model Y with chassis #123 involved in a delivery event #345-essentially, any entity that exists in the past or present-it is represented as a first-order type.

Conversely, if the entity is expected to manifest in the future (e.g., a Tesla Model Y specified within a purchase order), it is represented as a higher-order type. Unfortunately, the OntoUML currently does support modeling of different sorts of higher-order types as discussed in [22].

For similar reasons, we utilize primitive relations, such as creation and termination , to associate not only events with objects but also to associate modes that represent the intention behind the creation or termination of objects specified by higher-order types.

Figure 2: OntoUML diagram of Reciprocity Relator. Inspired by [9]. Enterprise view. In all diagrams, types are represented in purple, objects in pink, modes in blue, events in yellow, and relators in green.

[FIGURE]

Reciprocity Relators [9, 20], see Figure 2, relate Social Commitments to Exchange (or correlative Claims to Exchange ) Economic Benefits of each of the two agents, e.g., the enterprise as a Going Concern and  the  other Market Participant(s) ,  as  in  contracts.  The  services  ontology  UFO-S  [9] regards  reciprocity  relator  as  an  agreement  to  exchange  service  actions.  Initial  phases  of  the reciprocity relator relate enterprise conditional commitments or offerings with expectations. The other market participants involved in a reciprocity relator may be independent or maintain related party  relationships  with  the  enterprise,  characterized  by  varying  degrees  of Relatedness , potentially  positioning  the  enterprise  as  a  principal  to  its  agents. Economic  Events create or terminate reciprocity  relators  or  manifest  their  respective modes through  the  execution  of economic exchanges.

## 2.4. Core Ontology for Financial Reporting Information Systems (COFRIS)

COFRIS [20] adds economic resource flow and affected resource stock concepts to the commitments/ obligations  and  their  fulfillment  conceptualized  in  [9].  Furthermore, Economic  Resources are considered as a set of institutional rights that have the potential to produce economic benefits. The term Economic when used as an adjective, refers to the monetary valuation or financial aspect of a given  concept.  In  some  cases,  this  qualifier  is  implicit  and  may  be  omitted  when  contextually understood.

In  COFRIS  Economic  exchanges  are  specialized  institutional  actions  in  which  two  economic agents (A and B) establish and fulfill reciprocal performance obligations, typically through a contract. These  obligations  involve  the  transfer  of  control  over  economic  resources  and  the  provision  of services, ultimately impacting both parties' resources and activities. The primary objective of such exchanges is to generate economic benefits for either or both parties involved.

The accounting for economic exchanges begins with the recognition of performance obligations. Fulfillment  of  these  obligations  occurs  through  the  transfer  of  economic  resources,  which  are specified by the resource types outlined in the contract.

The transfer of resources entails the execution of one agent's control or power over the resource, resulting in the termination of that agent's rights and the simultaneous creation of equivalent rights for the other agent. This transfer assumes that the receiving party can generate economic benefits from the acquired resource, either independently or in combination with other transferred resources or those freely available to the other party. A transfer action (1) may involve the actions of conduct - (2) service provision and (3) object delivery. Service provision refers to a simultaneous transfer of service rights and execution of specified action for the benefit of the other party. Notice a difference between  service  rights  transfer,  whereby  a  service  provider  is  hired  to  stand  ready  for  their execution, and service provision which is rights transfer with their simultaneous execution.

Fulfillment of performance obligation causes Accrual of a reciprocal conditional economic claim against  the  other  party,  fulfillment  of  all  performance  obligations  of  a  contract  creates  an unconditional  claim.  Besides  resulting  from  the  fulfillment  or  valuation  of  a  contract,  economic claims can be constructive or created by law.

In  addition  to  economic  resources,  economic  claims  can  be  transferred  and  exchanged.  The transfer of claims entails the execution of one agent's agreed control or power over the claim of the other party, resulting in the termination of that agent's obligation and the simultaneous creation of an equivalent obligation for the third party, usually with the consent of the other party. The opposite operation of the transfer of an economic claim against one party is the assumption of this claim by the other party.

## 3. Converged ontology of conceptual frameworks for financial reporting (CCF Ontology)

This  Section  presents  the  Converged  CF  Ontology  by  (1)  presenting  core  concepts  used  in  both frameworks (IFRS and US GAAP), (2) conducting ontological analysis by visually representing and exploring the nature of these concepts through OntoUML diagrams, (3) suggesting and motivating the core concepts of the converged ontology. Our primary focus in this paper is on the convergence of elements within financial statements. The questions to be answered in a converged way are:

1. What are the economic resources and claims of the enterprise, their control and deployment rights and obligations?
2. What are the core economic events and their dispositions, participants, and effects?

Building  upon  the  foundation  laid  by  COFRIS,  CCF  Ontology  takes  a  broader  perspective  by encompassing  not  only  'pure'  economic  exchanges,  but  also  production  and  transactions  with owners that are 'analytically useful to treat like' exchanges [27, 17], service provision, and other events, roles, and phases of resources and claims additionally required for the frameworks.

We consider the roles and phases of enterprise Economic Resources and Claims in Subsection 3.1, Table 1, and Figure 3, then transactions and other events and their effects on Resources and Claims in Subsection 3.2, Table 2, and Figure 4.

The concepts and terminology have been refined to align closely with those used in established frameworks, with particular attention given to cross-lingual validation using GPT-4 for term testing, including  the  nuanced  selection  of  terminologies,  such  as  differentiating  between Transferred Resource and Resource Transferred . It is assumed that for most concepts, corresponding higherorder types and correlative counterparts of concepts exist.

The UFO foundational concepts will be denoted in camelCase Arial italics, such as roleMixin but CCF Ontology concepts in Arial italics, starting in uppercase Economic Resource .

The  Terms Enterprise and [ Reporting ] Entity are  used  interchangeably . The  existing frameworks and CCF Ontology have the reporting entity perspective as opposed to the independent view [18, 20]. We assume that the Enterprise is a Market Participant in  some Environment and holds Economic Resources and Economic Claims against the Entity from other parties that are affected by Economic Events - transactions and other events with enterprise participation . Within its Business Activities ,  the  enterprise enters into transactions with other market participants to maximize equity for its owners.

An Economic Claim against the Entity from other parties is abbreviated as Claim From Others or simply Claim, while an Economic Claim of the Entity to other parties is a Claim To Others.

We combine the institutional actions of Economic Resource Transfer to the other party and Claim Assumption from the other party as an Outflow .  Conversely, Inflow combines Economic Resource Receipt from the other party and Claim Transfer to the other party .

## 3.1. Economic Resources of the Enterprise and Claims against it

To achieve the ontological convergence, we follow the ontology matching procedure of [23]. We start  with  identifying  similar  or  equivalent  elements  reflecting  financial  position  across  the frameworks. Table 1 shows the definitions of elements by frameworks and our suggestions and preferences  for  the  convergence  in italics .  In  certain  instances,  we  identify  elements,  such  as Revenue , related to one framework in the standards of another (i.e., on a lower level). In such  cases, the element from the second standard can provide additional context or enhancement to the first framework.  Subsequently,  we  establish  semantic  mappings  between  entities  from  different ontologies and consolidate equivalent or aligned entities into unified representations. Any semantic conflicts, such as naming discrepancies, variations in definitions, and inconsistencies in constraints, are resolved by prioritizing the definitions provided by IFRS. All these steps are aligned with the shared Unified Foundational Ontology (UFO) and its sub -ontologies. If a concept does not align with or specialize an existing concept in the upper ontology, it is redefined accordingly. However, in the past, we have experienced a situation when our conceptualization influenced upper ontologies [8]. The outcome is the development and validation of the converged ontology, represented in OntoUML. Having  achieved  an  initial  match  between  the  two  standards,  we  continue  by  describing  the grounding  of  these  elements  in  UFO  depicted  as  the  OntoUML  diagram  in  Figure  3  and  our motivation for resolving semantic conflicts of both frameworks and creating unified representations.

An Economic Resource, such as homeownership, is a subkind of Reciprocity Relator mediating the enterprise with the Market Society relating an Enabling Right to Exchange, e.g., a right to sell a house, and reciprocal Economic Benefit Potential, e.g., receiving a payment. The rights to exchange may either arise from ownership over a particular physical or social Object , e.g., a house, rights to receive Services or  other  resources of  a  certain type, e.g.  housekeeping  services,  or Rights  to Transfer a Claim of the other party, e.g. transfer of a mortgage to the buyer of a house. The latter right  is  overlooked  in  accounting  framework  definitions  but  is  implicitly  recognized  in  actions described by standards such as IFRS 13 [24]. Therefore, it has been incorporated into the converged definition.

The US GAAP Conceptual Framework does not differentiate economic resources as a separate element, considering them synonymous with assets. The earlier UFO conceptualization in [11] is less detailed  but  also  follows  the  synonymous  approach.  Our  preference  for  the  IFRS  treatment  of economic resources, as noted in [3], stems from its broader, more generic definition. This perspective recognizes economic resources not only as part of an entity's financial position (a situation ) but also as  participants  in  transactions,  such  as Resource  Transferred .  Additionally,  an  entity's  own capabilities-such as control over the resource, as well as the recognition criteria and measurement principles, it applies-can differ from those in a more generic (i.e., market or transactional) context.

Table 1 Definitions of the core elements of financial position [1, 2] with our suggestions in italics.

| Element           | Framework Definition or Description in IFRS and US GAAP Conceptual Frameworks   | Framework Definition or Description in IFRS and US GAAP Conceptual Frameworks                                                                                 |
|-------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Economic Resource | IFRS                                                                            | An [ enabling or entitling ] right that has the potential to produce economic benefits, including the right to transfer an economic claim against the entity. |

| Economic Claim                | IFRS                     | An entitling right that corresponds to an obligation of another party                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Economic Benefit              |                          | Future Increases in economic resources or decreases in economic claims against entity                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Asset                         | IFRS : US GAAP:          | A present economic resource controlled by the entity as a result of past events. A present right of an entity to an economic benefit.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Control                       | IFRS                     | An entity controls an economic resource if it has the present ability to direct the use of the economic resource and obtain the economic benefits that may flow from it, either directly or through an agent acting on behalf of the controlling entity. Control includes the present ability to prevent other parties from directing the use of the economic resource and from obtaining the economic benefits that may flow from it. An agent may facilitate the obtaining of economic benefits or the prevention of others from obtaining such benefits, but the principal retains ultimate control. It follows that, if one party controls an economic resource, no other party controls that resource. |
| Right to Deploy               | IFRS                     | An entity has the present ability to direct the use of an economic resource if it has the right to deploy that economic resource in its activities, or to allow another party , such as an agent, to deploy the economic resource in that other party's activities.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Momentarily Asset             | Both                     | Goods or services received and immediately consumed. See Services in Subsection 3.2.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Executory Contract            | IFRS and US GAAP ASC 606 | A combined right and obligation to exchange economic resources. The right and obligation are interdependent and cannot be separated. Hence, the combined right and obligation constitute a single asset or liability.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Economic Claim Against Entity | Both                     | Liability or Equity Claim. An obligation that has the potential to sacrifice economic benefits, including the obligation to assume a new economic claim against the entity.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Liability                     | IFRS : US GAAP:          | A present obligation of the entity to transfer an economic resource to provide services or to assume a new claim against the entity as a result of past events. A present obligation of an entity to transfer economic benefits - either to transfer cash or convey assets or to provide services or stand ready to do so.                                                                                                                                                                                                                                                                                                                                                                                  |
| Equity Claim                  | Both                     | The residual interest in the assets of the entity after deducting all its liabilities.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Obligation to Deploy          | IFRS                     | A present obligation of an agent to transfer to a third party an economic resource controlled by the principal.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Unit of account               | IFRS                     | The right to inflow or the group of rights, the obligation to outflow or the group of obligations, or the group of rights and obligations, to which recognition criteria and measurement concepts are applied.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

Figure 3: CCF Ontology. OntoUML diagram of Economic Resources and Claims. Enterprise View. Sections: 1. Reciprocity Relator, 2. Resources and Claims, 3. Assets, Liabilities, and Equity Claims.

[FIGURE]

This highlights the added dimension that an entity brings to its economic resources beyond what is reflected in generic market definitions. For example, intangible economic resources like software, control features as an asset include not only the software itself but also the rights to access, update, or use it, which may be specific to the enterprise holding the asset. Similarly, a house that has been acquired by an enterprise is classified as being used for production purposes, but not for sale.

US  GAAP  CF  does  not  differentiate  between  enabling  rights  and  entitling  rights § ,  thereby omitting the "potential to produce" characteristic found in the IFRS definition of economic resource. US GAAP suggests a more stringent recognition criterion. We prefer to emphasize enabling rights and  the  inherent  uncertainty,  as  this  distinction  aligns  with  the  asset-resource  differentiation, allowing  for  a  more  nuanced  and  comprehensive  characterization  of  economic  resources.  By focusing on enabling rights and uncertainty, a broader perspective is introduced, accommodating the  various  aspects  of  economic  potential  and  resource  utility  beyond  the  more  rigid  asset recognition criteria.

§  Sometimes also referred as in rem and in personam rights respectively.

Economic claims against other parties when enabling rights have been Extinguished for the benefit of the other party, the Entitling Rights over economic benefits, such as receivables, are raised and the economic resource enters into the Claim to Others phase .

Economic  Benefits are  understood  as  a  result  of  the creation of  economic  resources  or termination of  claims,  thereby  enhancing  the  entity's  economic  position.  These  benefits  are  the foundation of financial value and serve as the outcome of economic exchanges. This is our suggestion instead of rather long definitions in the frameworks, that as one standard-setter answered, 'economic benefit is difficult to define'.

Economic rights and obligations are modes inhering in the enterprise and other parties and are manifested by actions. These  rights and  obligations  govern future transfers and  receipts (assumptions and transfers) of economic resources (resp. claims). Consequently, specified economic resources and claims are modeled as higher-order types. Modes progress through different phases, raising phases of economic resources and claims.

Assets, such as crude oil (economic resource) as a raw material (role) or homeownership as an investment property, specialize economic resources that are held and controlled by an enterprise. These assets serve specific purposes aligned with the enterprise's objectives and are subject to unique restrictions, controls, and accounting treatments, including recognition, measurement, and valuation based on their intended use and the economic benefits they are expected to generate.

Control encompasses both the ability to direct the  use of a resource and to obtain economic benefits from it, as well as the right to manage outflows and facilitate inflows.

Control to Exchange and Control to Inflow refer to the ability of the enterprise to realize the potential of the resource within some business activity type. Unlike IFRS, US GAAP CF does not explicitly recognize the concept of control, which we find particularly important, especially when considering transfer and agency issues. Control involves the Ability to Direct and Ability to Obtain Economic Benefits and the Ability to Deploy Outflow and Ability  to  Facilitate  Inflow . For the latter  two  an Exchange  Engagement with  an Agent is  possible,  potentially  separated  for deployment and facilitation of obtaining and prevention. It also brings up the question about the transferability of control, assets, and liabilities, as regarded in Subsection 3.2.

An Exchange Contract, another subkind of Reciprocity Relator , mediates the enterprise with the Other  Party that  specializes Market  Participant .  Contracts  have  inseparable Rights and Obligations to Exchange economic resources or claims, mutually agreed upon between two parties. Executory  Contract is  a phase of an equally unfulfilled contract with the net cash flow value typically equal to zero. Contracts, resources, and claims are not static; they are subject to fulfillment, extinguishment,  and  fluctuating  valuations.  Therefore,  we  conceptualize  them  as  distinct  but interconnected phases within their lifecycle.

A Claim  to  Others , such as [account] receivable,  arises  from  a  contract  when Rights  to Exchange are predisposed to yield economic benefits-specifically, eventual inflows that are either greater than outflows of the related Obligation to Exchange or no such obligations exist.

A Claim from Others , such as payable , arises from a contract if the outflows are greater, or no rights exist and stems from the fulfillment of the Obligation to Exchange or the valuation of the contract. It can also be a participant in transactions as Claim Transferred .

A Liability specializes Claim from Others that the enterprise has no practical ability to avoid . In its definition in Table 1 we emphasize the transfer of services because in this case, the transfer of rights takes place simultaneously with service provision.

An Equity  Claim specializes  residual Claim  from  Others -  from  the entity's Owners and represents the owners' interest in the Equity - the assets of the entity after deducting all its liabilities.

The Outflow Engagement with the Agent Obligation to Deploy specifies a present obligation of an agent to transfer to a third party an economic resource controlled by the principal.

The US GAAP does not include  control and agency-related concepts in CF, which is the reason for choosing more comprehensive IFRS CF definitions, elaborated in IFRS 15.

The Unit of Account , a collective of Reciprocity Relators , is the right or the group of rights, the obligation or the group of obligations, or the group of rights and obligations, to which recognition criteria and measurement concepts are applied [1]. The rationale for grouping or separating rights and obligations into particular Unit of Account is a matter of particular standards.

## 3.2. Transactions and other events

Per  [25]  much  of  financial  reporting  is  currently  transaction-based  and  will  continue  to  be  so. Transactions  and  other  events  result  in  [ gross ]  increases  in  equity  (such  as  income)  and  [ gross ] decreases in equity (such as expenses), typically accompanied by corresponding changes in assets and liabilities, ensuring that the fundamental equation, Assets = Liabilities + Equity Claim, remains balanced and intact. In Table 2 we have accumulated definitions of changes in equity from both frameworks and standards grouped by Transaction or Other Event type as a main criterion for naming these changes, allowing us to combine the differences in naming.

Table 2 Transactions and Other Events Represented as Changes in Equity

| Change in Equity        | Framework       | Definition or Description in IFRS and US GAAP Conceptual Frameworks 1. Changes in economic resources and claims reflecting financial performance .                                                                                                                       |
|-------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Income                  | IFRS            | Increases in assets, or decreases in liabilities, or goods or services received and immediately consumed, that result in increases in equity, other than those relating to contributions from holders of equity claims.                                                  |
| Expenses                | IFRS            | Decreases in assets, or increases in liabilities, or goods or services received and immediately consumed, that result in decreases in equity, other than those relating to distributions to holders of equity claims.                                                    |
|                         |                 | 1.1 Changes from ordinary activities                                                                                                                                                                                                                                     |
| Revenues                | US GAAP IFRS 15 | Inflows or other enhancements of assets of an entity or settlements of its liabilities from delivering or producing goods, rendering services, or carrying out other activities. Income arising in the course of an entity's ordinary activities when transferring goods |
| [ Operating ] Expenses  | US GAAP         | Outflows or other using up of assets of an entity or incurrences of its liabilities from delivering or producing goods, rendering services, or carrying out other activities.                                                                                            |
|                         |                 | 1.2 Changes from not ordinary activities                                                                                                                                                                                                                                 |
| Gains                   | US GAAP         | Increases in equity from transactions and other events and circumstances affecting an entity except those that result from revenues or investments by owners.                                                                                                            |
| Losses                  | US GAAP         | Decreases in equity from transactions and other events and circumstances affecting an entity except those that result from expenses or distributions to owners.                                                                                                          |
|                         |                 | 2. Changes in economic resources and claims not reflecting financial performance                                                                                                                                                                                         |
|                         |                 | 2.1. Transactions with Owners                                                                                                                                                                                                                                            |
| Investments from Owners | US GAAP         | Increases in equity of an entity resulting from transfers to the entity from other entities of something valuable to obtain or increase interests (or equity) in the entity.                                                                                             |
| Distributions to Owners | US GAAP         | Decreases in equity of an entity resulting from transferring assets, rendering services, or incurring liabilities by the entity to owners. Distributions to owners decrease ownership interest (or equity) in an entity.                                                 |
|                         |                 | 2.2. Other changes                                                                                                                                                                                                                                                       |
| None                    | Both            | Exchanges of assets or liabilities that do not result in increases or decreases in equity.                                                                                                                                                                               |

In Figure 4 we depict the converged ontology of transactions and other events grounding it in UFO. Economic  Outflow  and  Inflow  events  are  fundamental  components  of  Transactions  and  Other Events. These events may occur independently as environmental or market phenomena, such as impairments or value changes, or as manifestations of Obligations and Rights arising constructively, by law, or through exchange contracts. In the latter scenario, the fulfillment of non-terminal phases of Obligations or Rights to Exchange also triggers accrual ** or reciprocal events.

Outflows involve the Resource Transfers to other parties and the Assumptions of Claims from other parties . These actions result from the Decreases in Assets, Increases in Liabilities , and the consumption of Services Provided, leading to Decreases in Equity.

The Fulfillment of Obligations to  Exchange or Entitlement Obligations results in Extinguished Obligations. Furthermore, outflows advance unfulfilled Rights to Exchange into Entitling Rights which trigger the Accrual of Claims to Others leading to Increases in Equity.

Figure  4: CCF  Ontology.  OntoUML  diagram  of  transactions  and  other  events.  Enterprise view †† , ‡‡ Sections:  1.  Transfers,  2.  Accounting  effects,  and  3.  Changes  in  equity  specialized  by economic event type.

[FIGURE]

**  Accrual accounting depicts the effects of transactions and other events and circumstances on a reporting entity's economic resources and claims in the periods in which those effects occur, even if the resulting cash receipts and payments occur in a different period. [1, 2]

††  One reviewer questioned the validity of the &lt;&lt;characterization&gt;&gt; relation between &lt;&lt;kind&gt;&gt; and &lt;&lt;subkind&gt;&gt; in Figure 4. However, we, along with the OntoUML verifier, have confirmed its validity. The &lt;&lt;characterization&gt;&gt; relation in question is appropriately established between the Enterprise and the Obligation, which is a &lt;&lt;subkind&gt;&gt; of the Social Commitment &lt;&lt;mode&gt;&gt; depicted in Figure 3.

‡‡  Aggregation relations between events are used instead of &lt;&lt;historicalDependence&gt;&gt; relations.

Inflows involve the Resource Receipts from other parties or the Claim Transfers to other parties . These actions result in Increases in Assets, Decreases in Liabilities ,  and  the  consumption of Services Provided, leading to Increases in Equity.

The Fulfillment of Rights to Exchange or Entitling  Rights results  in Extinguished Rights. Furthermore, inflows advance unfulfilled Obligations to Exchange into Entitlement Obligations which trigger the Accrual of Claims from Others leading to Decreases in Equity .

The  progression  of  both  obligations  and  rights  into  their  extinguished  phases  results  in  the exchange contract transitioning into its Extinguished Contract phase.

All changes in equity are categorized based on the type of Economic Event , the Nature and Roles ( Functions ) of the agentive and non-agentive participants in the entity's business activities, and the methods used to measure these changes.

In  addition  to the  general  pattern  described  above,  changes  in  equity  are  recognized specifically  depending  on  the  type  of  event.  First,  the  transaction  or  event  is  categorized  as whether it is within the scope of the Financial Performance of the enterprise. In this case, the Expense specializes Decrease in Equity and the Income specializes Increase in Equity .

Second, within the first, the transaction or event is categorized as whether it is within the scope of Ordinary Activities of the enterprise. In this case, the Operating Expense specializes Expense and Revenue specializes Income . This follows from the US GAAP CF and IFRS 15.

Otherwise, if not within ordinary activities, Loss specializes Expense and Gain specializes Income .

For changes in economic resources and claims that do not reflect financial performance, we have Operations with Owners and Other Changes . For operations with owners, Distribution specializes Decrease in Equity and Investment specializes Increase in Equity. The US GAAP CF in contrast with IFRS has special elements for owner transactions [2] that indicate some construct deficit in [1].

The remaining are 'Exchanges of assets or liabilities that do not result in increases or decreases in [net] equity' [1] and do not reflect financial performance. Changes in equity typically are not recognized for these inflow and outflow events, e.g., for purchase transactions.

However,  under  US  GAAP,  transactions  with  owners  are  included  as  separate  elements  of financial  statements-specifically,  'Investments  by  Owners'  and  'Distributions  to  Owners.'  This inclusion, along with discussions on defining elements in terms of cash inflows and outflows (as elaborated in paragraph C4.97 of the Basis of Conclusions on the IFRS Conceptual Framework [25]), supports the perspective that categorizing changes in equity at the transaction level for each inflow and  outflow  provides  ontologically  meaningful  insights  into  the  economic  events  of  an  entity. Whether this categorization is significant for presentation or disclosure purposes depends on the specific requirements of the applicable accounting standards.

Important components of transactions and other events are transfers of economic resources and claims, and service provision - services received that are immediately consumed.

Using legal concepts regarded in [13] we define Transfer of Rights as institutional action in which a holder of an economic resource, leveraging its legal power to create or modify legal relations, terminates  the  holder's  rights  to  the  resource  and  simultaneously  creates  equivalent  rights  for another party who is initially under a legal disability.

IFRS 15 [14] and the converged ASC 606 [26] introduce the concept of Transfer of Control as a criterion for revenue recognition. Additionally, they treat assets (and liabilities in other standards) as the objects of transfer. We question this approach, as control encompasses certain capabilities of an enterprise, as understood in the [12], which are inherently complex to identify and transfer. This distinction directs us back to the fundamental difference between economic resources and assets. Economic resources encompass transferable rights and are understood not only in terms of their legal status but also either by the market society's (or shared by the agreement with the other party) understanding of the resource's capabilities and the availability of other components necessary to realize those capabilities.

Consequently, the transfer of control should include rights and capabilities of economic resources underlying  assets  but  not  the  rights  and  capabilities  specialized  by  the  assets  inhering  in  the enterprise.

Both frameworks introduce a Momentarily Asset concept for goods or services received and immediately consumed. That makes the definitions of the elements shorter. However, in UFO [9], service delivery is a complex event (not an endurant) characterized by its temporal nature and the immediate co-consumption by the service recipient. Also, SNA [27] finds that service production is an activity that  cannot  be  conceived  without  its  simultaneous  consumption.  The  CCF  Ontology models momentarily assets as Services Provided and adjusts the changes in equity definitions in Table 2. This is also reflected in Figure 4 whereby changes  in  equity can  be  created  by  Service provision event. An example of recognizing service production and consumption as pure changes in equity is the recognition of revenue in a barter transaction. In such a transaction, the value of the goods  transferred  is  measured  by  the  fair  value  of  the  services  received  and  consumed  as consideration.

An example of a sales transaction scenario is represented in Table 3, formatted as an event table [32]. In transaction #1, the enterprise-a car dealership-transfers a car to a customer as part of its ordinary activities for $29,500, plus $1,000 worth of cleaning services provided by the customer. The cleaning services  are  immediately  received  and  consumed . The cost of the car to the dealership is $20,000.

In  transaction #2, the dealership assumes a  $500  registration  fee  payable  to  a third  party  (the DMV), which is reimbursable by the customer (as part of the other events of the enterprise).

The third transaction is the fulfillment (F) of the registration fee payable to the DMV assumed in transaction #2. In the table, '+' indicates an increase, while '-' indicates a decrease.

Table 3 Example of a Sales Transaction

|    |     |                |             |     |              |                   |              |        | Stock   | Stock         | Stock       | Stock   |
|----|-----|----------------|-------------|-----|--------------|-------------------|--------------|--------|---------|---------------|-------------|---------|
| #  | F # | Economic Event | Other Party | + - | Flow Element | Resource or Claim | Third- Party | Amt $  | + -     | Stock Element | Other Party | Amt $   |
| 1  |     | Transfer       | Customer    | -   | COGS         | Car               |              | 20,000 | -       | Inventory     |             | 20,000  |
|    |     | Accrual        |             | +   | Revenue      | Receivable        |              | 29,500 | +       | Receivable    | Customer    | 29,500  |
|    |     | Receipt        | Customer    | +   | Barter       | Services          |              | 1,000  |         |               |             |         |
|    |     | Consumption    |             | -   | Expense      | Services          |              | 1,000  |         |               |             |         |
| 2  |     | Assumption     | Customer    | -   | Loss         | Fee to            | DMV          | 500    | +       | Fee to        | DMV         | 500     |
|    |     | Accrual        |             | +   | Gain         | Receivable        |              | 500    | +       | Receivable    | Customer    | 500     |
| 3  | 2   | Transfer       | DMV         | -   | Cash Outflow | Cash              |              | 500    | -       | Cash in Bank  | Bank        | 500     |
|    |     | Fulfillment    |             | +   | Fulfillment  | Fee to            | DMV          | 500    | -       | Fee to        | DMV         | 500     |

## 4. Conclusion and future work

Grounding in UFO and COFRIS social and economic endurants, events, and their primitive relations we have developed a Converged Ontology of the IFRS and US GAAP Conceptual Frameworks for Financial Reporting. This ontology is a novel attempt to describe the core transactions and other events, the elements for financial reporting. It charts the path for setting standard ontologies through framework  specialization,  framework  improvement  via  convergence,  theory  and  technology adaptation, and standard generalization.

In our development process, we have refined the distinctions between economic resources and assets, clarified the dual nature of economic claims against an entity, and identified the participants involved in inflows and outflows. Additionally, we have addr essed issues surrounding the transfer of economic resources, differentiated between services and 'momentarily assets', and developed a converged taxonomy of economic transactions and other events.

The  need  to  converge  concepts  necessitates  their  unification  while  excluding  contradictions, ensuring  that  the  converged  concept  is  grounded  in  an  upper-level  ontology  and  effectively specialized at the lower levels. Convergence can significantly enhance or refine a concept; however, care must be taken to prevent it from becoming overly broad or abstract. Achieving convergence between  frameworks  requires  an  in-depth  analysis  of  standards  to  identify  a  shared  conceptual foundation.  Success  in  this  process  is  marked  by  identifying  higher-level  concepts  rooted  in established theories or the Unified Foundational Ontology (UFO).

The bias toward IFRS in a converged framework arises from the desire for global applicability, principles-based  flexibility,  alignment  with  economic  substance,  and  regulatory  preferences  for simpler, more uniform standards. This makes IFRS a more appealing foundation for a unified set of global accounting standards compared to the more detailed and rules-heavy US GAAP.

The observed need to delve into the IFRS 15 and converged US GAAP ASC 606 is because this standard reflects the core concepts of economic exchange, and in some sense is more fundamental than the frameworks.

UFO Ontology matching and convergence remains mostly a costly manual process. However, the attempts to automate it open a new perspective by using the means of LLM [28, 29] and exporting to OWL of OntoUML diagrams [30].

The resulting converged framework serves as a validation of COFRIS. Furthermore, the validation of the CCF Ontology itself should involve the modeling of converged standards, such as IFRS 13 [24], and  addressing  emerging  challenges,  like  climate-related  and  other  uncertainties  in  financial statements [31], which are pertinent to both frameworks. This approach not only verifies ontology's robustness but also ensures its relevance to contemporary financial reporting issues.

The  CF  Ontology  diagrams  were  syntactically  verified  using  OntoUML  tools.  The  successful development of the CCF Ontology demonstrates the conceptual richness of the UFO and COFRIS ontologies and their suitability as ontological analysis means.

The CCF Ontology is submitted for publishing in OntoUML/UFO Catalog.

## References

- [1] IFRS Foundation. Conceptual framework for financial reporting, Retrieved from https://www.ifrs.org, 2018.
- [2] Financial Accounting Standards Board. US GAAP conceptual framework for financial reporting. Norwalk, CT: FASB, 2023.
- [3] Gerber,  MC.,  Gerber  AJ.,  and  Van  der  Merwe  A.,  The  conceptual  framework  for  financial reporting as a domain ontology, AMCIS 2015.
- [4] Blums, I., H. Weigand, Ontological grounding of accounting frameworks. 42nd International Conference on Conceptual Modeling: ER Forum, 7th SCME, Project Exhibitions, Posters and Demos, and Doctoral Consortium, 2023.
- [5] Guizzardi,  G.:  Ontological  foundations  for  structural  conceptual  models.  Ph.D.  thesis,  CTIT, Centre for Telematics and Information Technology, Enschede (2005).
- [6] Almeida,  J.P.A.,  R.  A.  Falbo,  G.  Guizzardi,  Events  as  entities  in  ontology-driven  conceptual modeling.  Conceptual  Modeling:  38th  International  Conference,  ER  2019,  Salvador,  Brazil, November 4-7, 2019, Proceedings: 469-483.
- [7] Guizzardi  RSS,  Guizzardi  G.  Ontology-based  transformation  framework  from  TROPOS  to AORML. Social modeling for requirements engineering. The MIT Press; 2010. 547-70.
- [8] Guizzardi, G., et al, Endurant types in ontology -driven conceptual modeling: Towards OntoUML 2.0, ER 2018, Xi'an, China.
- [9] Nardi, J.C., et al., A commitment-based reference ontology for services. Inf. Syst. 54, 263-288 (2015).
- [10] Amaral, G.C.M., An ontology network in finance and economics: money, trust, value, risk and economic exchanges. Doctoral Thesis, Faculty of Computer Science Free University of BozenBolzano 2022.
- [11] Azevedo, C.L.B., et al.: an ontology-based well-founded proposal for modeling resources and capabilities in ArchiMate. In: 17th IEEE International EDOC Conference (EDOC 2013). pp. 3948. IEEE Computer Society Press (2013)
- [12] Calhau,  R.F.,  JPA.  Almeida,  S.  Kokkula,  G.  Guizzardi,  Modeling  competences  in  enterprise architecture: from knowledge, skills, and attitudes to organizational capabilities. Software and Systems Modeling, 1-40
- [13] Griffo,  C.,  JPA.  Almeida,  JAO.  Lima,  TP.  Sales,  G.  Guizzardi  Legal  powers,  subjections, disabilities,  and  immunities:  Ontological  analysis  and  modeling  patterns  Data  &amp;  Knowledge Engineering 148, 102219
- [14] IFRS Foundation. IFRS 15: Revenue from contracts with customers. 2014.
- [15] Blums, I., H. Weigand, Toward ontology-guided IFRS standard-setting. CAiSE Forum 2024: 7381.
- [16] IFRS Foundation. IFRS S1 general requirements for disclosure of sustainability-related financial information. Retrieved from https://www.ifrs.org, 2023.
- [17] Ijiri, Y.: Theory of accounting measurement. American Accounting Association (1975).
- [18] ISO/IEC  FDIS  15944-4:  2015.  Information  technology  -  business  operational  view  -  part  4: business transactions scenarios - accounting and economic ontology. ISO 2015.
- [19] Massin, O, E. Tieffenbach, The metaphysics of economic exchanges. Journal of Social Ontology 3(2), 167-205
- [20] Blums,  I.,  H.  Weigand,  Consolidating  economic  exchange  ontologies  for  financial  reporting standard setting, Data &amp; Knowledge Engineering, Volume 145, 2023, 102148.
- [21] Blums,  I.,  H.  Weigand:  Towards  a  core  ontology  of  economic  exchanges  for  multilateral accounting information systems, EDOC 2020: 227-232.
- [22] Fonseca, C.M., G. Guizzardi, JPA. Almeida, TP. Sales, D. Porello, Incorporating types of types in ontology-driven conceptual modeling. International Conference on Conceptual Modeling, 1834, 2022.
- [23] Euzenat, J. &amp; Shvaiko, P. (2013). Ontology matching (2nd ed.). Springer Berlin Heidelberg.
- [24] IFRS Foundation. IFRS 13 Fair Value Measurement. Retrieved from https://www.ifrs.org, 2011.
- [25] IFRS Foundation. Basis for conclusions on conceptual framework for financial reporting. (2018)
- [26] Financial  Accounting  Standards  Board  (FASB).  ASC  606:  revenue  from  contracts  with customers. Norwalk, CT: FASB, 2014.
- [27] System of National Accounts, EC, IMF, OECD, UN, World Bank, 2009.
- [28] Amini, R., S.S., Norouzi, Pascal Hitzler, and Reza Amini, Towards complex ontology alignment using large language models, ArXiv, 2024.
- [29] [https://oaei.ontologymatching.org/](https://oaei.ontologymatching.org/)
- [30] Guizzardi, G., Almeida, J.P.A., &amp; Guizzardi, R.S.S. (2021). gUFO: A lightweight implementation of  the  unified  foundational  ontology  (UFO)  in  OWL2.  Applied  Ontology,  16(2),  109-143. https://doi.org/10.3233/AO-200240
- [31] IFRS Foundation. climate-related and other uncertainties in the financial statements. Exposure draft, 2024.
- [32] Weigand, H., I. Blums and J.d. Kruijff, Shared ledger accounting - implementing the economic exchange pattern, information systems (2019) 101437, https://doi.org/10.1016/j.is.2019.101437
