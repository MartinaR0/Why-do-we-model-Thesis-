## An ontological analysis of artifact-centric business processes managed by smart contracts

[FIGURE]

M.E.M. van Wingerde Department of Management Tilburg University Tilburg, The Netherlands m.e.m.vanwingerde@uvt.nl

Abstract -Inter-organizational business processes require extensive information sharing between organizations. To acquire a holistic overview of an inter-organizational process, insight in both its control flow and data model is required. Business artifacts are a well-positioned mechanism to model these two dimensions. However, when business artifacts and their associated lifecycle and information models are shared between organizations, a single source of truth is preferred. To maintain such a single source without centralized administration, blockchain-based smart contracts may be used. We claim that an artifact-centric approach to business processes is well-suited for smart contract implementations. However, the conceptual relationship between business process artifacts and smart contracts has not yet been extensively analyzed. In this paper, we present a novel ontological analysis of artifact-centric processes managed by smart contracts. We adopt the method of enterprise ontology and regard an interorganizational process as a set of causally related transactions in which the state of the lifecycle and associated data objects of business artifacts is transformed by sending messages to smart contracts. Our conceptual models are visualized in OntoUML, a modeling language based on the Unified Foundational Ontology.

Index Terms -inter-organizational business processes, business artifacts, smart contracts, blockchain, enterprise ontology

## I. INTRODUCTION

Widespread adoption of inter-organizational business process management is hampered by the requirement for trust in a central authority to administer the state of the shared business processes [1]. Blockchain technology has been widely acknowledged to have the potential to remove the need for a central authority in the management and operation of interorganizational business processes [2], [3]. Through a distributed ledger and shared business logic in the form of smart contracts, organizations can execute shared business logic and monitor the state of process instances [4]. Our hypothesis is that blockchain technology opens up a new level of crossenterprise integration. Compared to other enterprise integration efforts, such as service oriented architectures, blockchain allows organizations to use a single shared database to manage and operate their shared business processes.

As commonly seen with the introduction of a potentially disruptive information technology, blockchain and its smart

The authors would like to sincerely thank DEITY B.V. for funding this research.

[FIGURE]

H. Weigand Department of Management Tilburg University Tilburg, The Netherlands h.weigand@uvt.nl

contract capability has mostly been researched from a technical perspective [5]. Organizations, and the business networks they operate in, have initiated numerous pilot projects to determine how they may best exploit the technology. While prototyping can provide valuable insight into the technology, the downside is that without a common conceptual knowledge base, each organization may develop a separate understanding of blockchain-based business processes. Therefore, the authors have decided to conduct an ontological analysis of the concepts and their relationships, providing a common understanding of artifact-centric business processes managed by smart contracts.

Inter-organizational business processes are invoked by an event external to the process. For example, the creation of an invoice by an organization may trigger a payment workflow of another organization. Smart contracts contain business logic which is triggered by sending 'transactions' to the contract [6]. Business logic can either be invoked by an external (a wallet) or internal (another smart contract) account. Transactions initiate a state change in the smart contract, e.g. some business logic gets executed and state variables are updated to new values. Both the business logic execution and state changes are publicly visible to the entire network of participants.

This is where a link with established theory can be found. An inter-organizational business process has a public part, visible for all process actors, and multiple private parts which interface with the public part [7]. We draw from the public to private approach of Van Der Aalst [8], which outlines an approach to designing inter-organizational workflows. The approach starts with all process actors designing their shared public workflow, after which each of the actors can autonomously design their internal workflows, as long as they interface with the predefined public workflow. Due to the design principles of blockchain, i.e. transparency and decentralization, we hypothesize that indeed only the public view of an interorganizational business process could be feasibly implemented on a blockchain.

The predominant method of theorizing and modeling business processes emphasizes the control flow of a process, taking an activity-centric approach. While this approach is suited to describe the activities process agents conduct, how they are related to each other, and what the associated conditional logic is, the approach has a significant drawback [9]. That is, the link between the control flow and the data required for it or produced by it, is not clear in an activity-centric business process model. In 2003, IBM recognized this issue and developed a process modeling approach centered around business artifacts [10]. Business artifacts are entities which are transformed by the operational activities a business conducts. Both a lifecycle and information model are associated with the artifact. The artifact-centric approach has been recognized [9], [11] as a potentially superior method to manage interorganizational processes.

Thus, both smart contracts and business artifacts combine control flow and process data. For this reason, we follow the view that artifact-centric approaches to blockchain-based inter-organizational business processes may indeed be superior to activity-centric approaches [12]. However, before we can validate this claim, a formalization of the relationship between business artifacts and smart contracts is required, as it is not present in current literature. The key research questions are (1) how are inter-organizational processes related to business transactions, (2) what is the relationship between business artifacts and smart contracts, and (3) how do smart contracts manage business artifact lifecycles and states. To provide an answer to these questions, we have conducted an ontological analysis. We designed three ontologies grounded in the four axioms of enterprise ontology by Dietz [13]. These ontologies formalize the concepts - and the associations between them -of business artifacts and smart contracts. We model the ontologies on the essential, infological and datalogical level using OntoUML, which is based on the Unified Foundational Ontology [14].

Section II provides background literature on interorganizational processes, modeling paradigms and smart contracts. Hereafter, section III outlines how smart contracts may be used to manage inter-organizational process artifacts. In section IV, the ontologies are presented, after which section V provides a mapping between the ontologies. Lastly, sections VI and VII provide for discussion and conclusions.

## II. BACKGROUND

Related research has been conducted in both business process management and blockchain literature. We will review the current line of thought in both domains.

## A. Inter-organizational business processes

To accomplish the goal of an inter-organizational business process, for example the successful delivery of a customer order, the participating organizational actors of the process must communicate with each other and exchange information. From a coordination perspective, these interactions between actors make sure that both parties commit to the performance of a particular process, before the actual realization of the process [13]. Coordination between actors occurs via message exchange, which can either be structured (XML or JSON files) or ad hoc (a phone call or email). Coordination efforts are essential in inter-organizational business processes, since they express commitments such as requests, promises, approvals, or declines [15], [16]. These messages are often required to initiate an (internal) workflow.

Contrary to intra-organizational processes, interorganizational business processes contain interaction between two or more autonomous organizations. Organizations attempt to integrate their processes, to improve the performance of the overall value chain. To achieve such performance improvements, a certain degree of information sharing between organizations is required [17]. The traditional challenge introduced in this situation -sharing information to increase value chain performance -is striking a balance between transparency and privacy [18]-[21].

Optimizing these processes may lead to multiple benefits, such as higher process transparency, degree of integration and facilitation of communication [22]. However, to achieve those benefits, collaborating organizations have certain requirements:

- the public part of the process requires decentralized governance,
- private processes, which interface with the public part, must be kept private,
- autonomy of the organizations must be preserved.

Due to a different unit of analysis, the approach to interorganizational process models varies from the BPMN approach as commonly seen for intra-organizational processes. This is confirmed by Montali et al [23] and Gattas and Soffer [24], who show that inter-organizational processes must preserve the autonomy, flexibility and compliance of participating organizations.

Various approaches have been put forward [8], [25]-[27] to solve the issue of transparency versus privacy. They all share a similar approach: define a public, shared part of the interorganizational process which all participating organizations can interact with. How each organization interacts with the public process remains private, as long as they conform to the rules defined in the shared process. However, the public process domain has to be, with current technology, managed by a trusted entity or group of entities. Thus, the integrity of the state of a public process at any given time requires trust in the entity who controls the data.

## B. Process modeling paradigms

Multiple high-level business process modeling frameworks exist among the scientific community. Activity-centric modeling is the predominant stream, focusing on the activities conducted by humans or software to advance a process from its start to its end. The data generated or required for the completion of these activities is less emphasized in this paradigm. On the other hand, document-centric process modeling focuses entirely on the data of processes [28]. While the state of business data can be closely monitored, the association with activities responsible for state changes is not sufficiently insightful. The artifact-centric view of a process combines both the activities and data encapsulated in a business process.

While activity-centric modeling is the dominant stream within business process management, the artifact-centric ap- proach provides advantages in the inter-organizational process management domain [29]. The business artifact approach to process management was initiated by IBM in 2003 [10]. In their work, important axioms are defined which we adopt in this paper. First, a business artifact is defined as a mechanism to provide for information localization . An artifact consists of an enterprise-wide unique identity and self-describing content, of which the identity may never change, while the content may arbitrarily change over time. Moreover, a business artifact has a lifecycle, which captures the state changes to the particular artifact, showing how it alters over time. For example, many businesses may represent a Customer Order as a business artifact. When we model the lifecycle of this artifact, it may have a requested, fulfillment, delivery , and settlement phase. Each of these phases will in turn rely upon different content.

Yongchareon et al [9] observe two main approaches to artifact-centric process management in the literature, namely to (1) use artifacts as an interoperation hub to orchestrate inter-organizational workflows [30] and (2) using artifacts in choreographies to model the results of business interactions [31]. In their work, they show that the state of business artifacts may be updated by private processes of business partners and separate between shared and private artifacts. This approach is in line with many previous works on inter-organizational process modeling, such as the Public-to-Private approach. The lifecycles of the shared artifacts may be modeled using a Guard-Stage-Milestone approach [32], which uses declarative rules to determine whether an artifact may advance to the next stage.

## C. Smart contracts

Smart contracts are persistent scripts of which the code is executed by a distributed virtual machine 1 . Smart contracts are deployed by sending a transaction to a blockchain network containing the compiled contract code. Once a smart contract has been successfully deployed it is immutable, similar to any other transaction conducted on a blockchain. Every smart contract instance is uniquely identified by an address, which is deterministic from the sender of the transaction which created the smart contract.

Every smart contract instance has its own storage in the form of a Merkle Patricia tree, which in turn records keyvalue pairs. State changes of a contract storage are initiated by transactions sent to the blockchain network. This may either be a direct transaction of an externally owned account to a smart contract, or indirectly from a smart contract to another via message exchange. An indirect state change - from one smart contract to another - does not require a separate transaction. Instead, it is processed during the execution of the transaction initiated by the externally owned account.

In the artifact-centric business process management approach, artifacts are composed of a unique identifier and content. Similarly, a smart contract is composed of a unique

1 While the architecture of blockchain platforms may differ, we refer to the Ethereum platform and its derivatives throughout this paper.

address and its content. In the case of Ethereum-based smart contracts, the content consists of the following:

- 1) state variable: key/value pairs containing arbitrary data, may also be in the form of a struct or enum
- 2) function: executable code which may be constrained by a modifier
- 3) event: interface to read data generated from function execution

Thus, smart contracts can be regarded as isolated software containing data, which has a state in a certain point in time, and business logic to transition that state. Two relevant differences between smart contracts and other replicated state machine implementations is that they are both available to the public and not governed by any subset of entities. Any actor interacting with a smart contract is interacting with the same data and business logic. Given an identical input, the contract will always produce an identical output.

## III. USING SMART CONTRACTS TO MANAGE INTER-ORGANIZATIONAL PROCESS ARTIFACTS

With smart contracts, we can model the fundamental elements of an inter-organizational process, namely business logic and data. The main difference between a smart contract and any other software implementation of process engines, however, is that smart contracts may be shared among multiple process participants. Due to the technical characteristics of blockchain platforms, which smart contracts are natively implemented on, the process logic and the data generated by it is distributed among all nodes. Note however, that the smart contract is readable to any node, but not necessarily interpretive. Using standard cryptographic techniques such as hashing or encrypting data, it may be obfuscated to other participants. Other more advanced techniques such as zeroknowledge proofs do not even require the actual data to be known to process participants. They merely require a cryptographic proof that the outcome of an operation is correct, augmenting the privacy of autonomous business entities.

Although they take an activity instead of an artifact-centric approach, Weber et al [4] have designed a process architecture -based on Ethereum -to monitor or implement inter-organizational processes. They use an API interface as triggers between public Ethereum smart contracts and private BPMN engines. Communication between the smart contract and internal processes is done via message exchange. They show that a supply chain, incident management and insurance claim process can be executed with 100% correctness.

As defined in the literature, business artifacts are a mechanism to provide for information localization. However, the localization scope is limited to the scope of the business artifact itself. Thus, if a single business artifact is not shared between multiple organizations, it will only provide information localization to the organizational domain in which it resides. If multiple autonomous organizations were to share business artifacts, they would require a business artifact management system which satisfies the requirements of interorganizational processes, i.e. organizational autonomy, privacy and flexibility. Blockchain-based smart contracts may satisfy these requirements, as they provide for a trustworthy history of state changes and offer independent process execution and monitoring [1], [33].

We illustrate the use of smart contracts to manage interorganizational business artifacts by introducing a running example. Consider the inter-organizational process of dropshipments, which is a specific pattern of fulfilling e-commerce orders used by retailers. Instead of buying inventory in bulk, the retailer contracts multiple suppliers who commit to fulfill consumer orders without logistics capabilities of the retailer. A visualization of the relevant shared artifact lifecycles is presented in figure 1 below.

Fig. 1. Artifact-centric drop-shipping process model

[FIGURE]

In common drop-shipment scenarios, the retailer is responsible for order and invoice processing, while the supplier is responsible for the order fulfillment and supply chain operations. The inter-organizational drop-shipping process has multiple interdependent business artifacts, each with its own lifecycle. Note that while business artifacts may be shared, they are generally owned by a single organization. In this case, a single holistic view of a business artifact and its state is absent. The information localization mechanism is limited to the internal domain of the retailer, supplier or carrier.

Similar to the information and lifecycle model of a business artifact, a smart contract has a business logic and state variable model. A relational mapping between these concepts appears to be present, which is visualized in figure 2.

Although this figure suggests the existence of a mapping between the concepts of business artifacts and smart contracts, it is by no means conclusive. A formal description of the relationship lacks in literature, a gap we aim to fill by presenting an ontological analysis in the following section.

## IV. ONTOLOGY

There are many approaches to construct an ontology. In the field of (accounting) information systems, often-used methods are Enterprise Ontology, e3value and Resources Events Agents (REA). As part of Enterprise Engineering [13], an enterprise ontology is useful to create a formal and explicit specification of a shared conceptualization among a group of people. e3value [34] emphasizes the exchange of value objects between actors, mapping the economic exchanges between autonomous actors and determining whether a value network is sustainable. REA is an ontology stemming from the accounting information systems domain [35], describing the economic value increases and decreases within an enterprise through resources, events and agents.

Fig. 2. Conceptual mapping between business artifacts and smart contracts

[FIGURE]

Our object of interest is the organization of activities within and between enterprises, as opposed to the (network) business model. We therefore choose to adopt the Enterprise Engineering approach. The enterprise ontology creates a common understanding of the activities performed within the enterprise. Related work [36] has used REA in combination with Enterprise Ontology to present a three-layered ontological analysis of commitment-based smart contracts. We adopt a very similar methodology, but choose to not incorporate REA. As an accounting ontology, REA is particularly well-suited to represent the duality of economic exchanges. Projected on commitments, De Kruijff &amp; Weigand show that every commitment by an actor is matched by a commitment of the counterparty. Our work differs from this commitment-based view, in that we analyze the use of business artifacts in interorganizational processes. State changes of business artifacts are not by definition dual. To represent inter-organizational business processes, we use the transaction model of enterprise ontology without the transaction duality of REA.

In enterprise ontology, four distinction axioms are presented: the operation, transaction, composition and distinction axioms. The operation axiom states that an enterprise is composed of subjects who may perform two kinds of acts, production and coordination acts, which result in production and coordination facts. Whereas the performance of an act is a direct or indirect contribution to the bringing about of a product of service, the creation of facts are state transitions which cannot be undone. A state transition generates an event in a certain point in time. In a business process, organizational agents perform coordination acts which result in coordination facts in the form of commitments, such as the delivery of a product for a certain price. The executor will typically perform a production act, resulting in the fact that a product has been created.

Building upon the operation axiom, the transaction axiom defines standardized patterns in which production and coordination acts and facts occur. These patterns are called transactions. A transaction consists of three phases, namely the order, execution and result phase. A transaction may be cancelled at certain points in time. Cancellation occurs due to two reasons, dispute or discourse. When a dispute occurs, the actors have a different claim to truth, which must be proved by facts. Discourse cancellations are more problematic since they are not solvable with facts, but are about the social values and norms of the actors. The transaction axiom is highly relevant for inter-organizational business processes, as every process may be mapped to a set of transactions.

The third axiom states that every transaction is either a part of another transaction, is initiated by a customer of the organization, or that is self-activated. This axiom is called the composition axiom . According to this axiom, a business process is a collection of causally related transactions. Such a process may then either be externally activated by a customer, or self-activated by an internal actor.

The distinction axiom states that humans have three distinct abilities with regards to coordination and production acts. They are the performa, informa and forma abilities. Transactions typically occur on one or more of these levels. On the performa level, ontological transactions establish new things, such as the creation of a product or making a decision. On the informa level, infological transactions serve to realize the ontological transaction, in which information or knowledge is exchanged between actors. On the forma level, datalogical transactions take place to realize infological exchange by storing or transmitting data.

A useful tool to depict the various concepts and their relationships in a graphical manner is OntoUML. OntoUML is a language for ontology-driven conceptual modeling, based on the well-known Unified modeling Language (UML). OntoUML is founded on the Unified Foundational Ontology (UFO) [14], consisting of a world view and multiple categories -UFO-A, UFO-B, UFO-C and UFO-S. They, respectively, provide an ontological description of conceptual constructs, events, social aspects, and commitment-based services. Contrary to other ontological modeling languages, such as OWL and RDF, OntoUML is suited to model the essence of an enterprise.

## A. Essential Ontology

At the essential level, process participants interact with each other in an inter-organizational process. The interaction patterns between participants are called transactions. Each transaction consists of multiple phases, the order, execution and result phase. The actions of participants result in facts, which contribute to the realization of the transaction's goal. Acts and facts may either be of the coordination or production type. Production acts and facts are the material or immaterial realization of the bringing about of goods and services. Coordination acts and facts, on the other hand, are communicative by nature whereby process participants engage into commitments regarding the performance of a process.

An inter-organizational business process consists of a number of causally related transactions, as depicted by the composition axiom of Enterprise Ontology. Each of these transactions has one initiator and one executor, which are roles played by process participants. Every transaction has a single goal. Process participants perform acts during the various transaction phases. Whenever an act is carried out, it results in a fact. Whereas an act typically consists of a desirable future state, such as the 'request of an order', a fact states something that actually is true in the social world at a point in time, such as 'an order has been placed'. In the context of business processes, a fact is always related to a business object. Business objects may either be physical or artificial. Facts contribute to the realization of a transaction goal, a single fact or set of facts may be required.

Fig. 3. Essential Ontology

[FIGURE]

Consider our previous example of a drop-shipment. In this inter-organizational process, three process participants are transacting with each other; the retailer, supplier and carrier. We highlight the transaction initiated by the retailer and executed by the supplier, which may be named T1: order placement transaction . During every transaction instance, the retailer and supplier perform acts, which result in facts. For example, the retailer would perform act A1: request to place order #1 , which results in the fact F1: placement of order #1

TABLE I ESSENTIAL CLASS DEFINITION

| Class                          | Definition                                                                           |
|--------------------------------|--------------------------------------------------------------------------------------|
| inter-organizatio- nal process | a business process consisting of at least two autonomous organizational participants |
| transaction                    | a standard socio-economic pattern bringing about a production result                 |
| transaction phase              | phase within a transaction where acts and facts occur                                |
| process participant            | role of the organization in the inter- organizational process                        |
| initiator                      | process participant who initiates a particular transaction                           |
| executor                       | process participant who executes a particular transaction                            |
| goal                           | the goal of a particular transaction, consisting of a set of facts                   |
| act                            | a communicative or material activity performed by a participant                      |
| fact                           | a state transition leading to a change in the social world                           |
| business object                | entities which are transformed during transac- tions                                 |
| physical object                | a tangible business object, such as a package or truck                               |
| artificial object              | an intangible business object, such as an order or invoice                           |

has been requested . Both A1 and F1 are of the coordination type and occur during the order transaction phase. In the execute phase of the T1, we notice a decomposition of the transaction. The supplier acts by initiating the transaction T2: shipment transaction , which is executed by the carrier. The completion of T2 results in the fact F2: order has been shipped . In the final transaction phase of T1, the supplier acts by stating F2 to the retailer, who in turn communicates his acceptance, resulting in the fact F3: order placement has been accepted . The set of all facts generated in transaction T1 contribute to the transaction goal, which may be the successful placement of the drop-shipment order.

## B. Infological Ontology

At the infological level, the lifecycle of an artifact and its associated data objects are transformed by services performed by agents. The purpose of process contracts, in the infological sense, is twofold. They serve as an information localization interface, containing the lifecycle and information model. Moreover, they guard the invocation of business services upon artifacts by procedural or declarative business rules. A business rule may contain both pre- and post-conditions.

Agents interact with process contracts. An agent may either be human or artificial (software). In most business processes, both human and artificial agents invoke particular services within a single process instance. In the infological sense, we regard the service as an event, as the invocation of it is of relevance. When an agent invokes a service, it will be processed by the process contract logic to determine whether it is recorded on the blockchain. Note that every agent, no matter which organization it represents, interacts with the same process contracts. A process contract represents at least one business artifact type. Instances of these business artifacts may or may not already exist during the creation of the process contract. Any artifact may be associated with zero to many other artifacts. For example, a shipping notice may be dependent on an invoice. Business artifacts contain two types of information [29], a lifecycle and data model. In most cases, the data model starts out relatively empty and expands over time. The lifecycle model changes from one state to the next in a mostly linear fashion. The set of all possible lifecycle stages form the entire lifecycle of the artifact.

Fig. 4. Infological Ontology

[FIGURE]

Both the lifecycle and all data objects associated with an artifact are stateful. Agents may consult the artifact state from its process contract, which maintains the state through state variables, to possibly influence their future behavior.

TABLE II INFOLOGICAL CLASS DEFINITION

| Class                  | Definition                                                                      |
|------------------------|---------------------------------------------------------------------------------|
| agent                  | human or software acting on behalf of a process participant                     |
| artificial agent       | a single artificial process participant, e.g. a soft- ware module               |
| human agent            | a single human process participant                                              |
| service                | a unit of work meaningfull to the business process                              |
| process contract       | process participant who executes a particular transaction                       |
| business rule          | pre- and post-conditions guarding whether a service can be successfully invoked |
| business artifact type | category of artifacts of which each has similar characteristics                 |
| business artifact      | business entity with a lifecycle and information model                          |
| lifecycle              | set of business-relevant stages in the evolution of the artifact                |
| data object            | information chunk associated with an artifact                                   |
| state                  | lifecycle and data object values at a fixed point in time                       |

The essential ontology depicted how process participants engage into transactions with each other in which they perform acts resulting in facts. We now present an analysis of the dropshipment process example on the infological level. When an essential transaction is initiated, the participants must arrive at a common understanding of the information associated with the transaction. Business artifacts are the mechanism which provide this understanding. In figure 1, three business artifact types are presented and instantiated once: the 'purchase order', 'shipping order' and 'invoice'. Let us consider the purchase order artifact. An artificial agent controlled by the retailer invokes an order placement service, which in turn invokes the process contract. The service invocations must conform to business rules contained in a process contract. In this case, the order must be placed 14 days prior to the proposed delivery date and the supplier must have a stock level above threshold. If the process contract successfully validates the service invocation, the contract creates a business artifact of the type 'purchase order'. The purchase order is in its first lifecycle stage, and has various data attributes associated with it, such as its identifier and the date it was created. These data are represented as the state of the artifact lifecycle and data objects, respectively. This artifact state is controlled by the process contract, which an agent may refer at any time to localize artifact information.

## C. Datalogical Ontology

On the datalogical level, an inter-organizational process is composed of transactions to smart contracts made by account wallets, which are owned by externally owned accounts. These wallets are software programs which are able to send messages to the pool of blockchain nodes. Messages originating from various wallets are independently validated. If validated, these messages are recorded as a transaction in a particular block -grouped with other transactions -and contain metadata and a payload. In the metadata, various data are found, such as the transaction hash which uniquely identifies the transaction. Moreover, the cryptographic signature output is attached to every transaction, allowing anyone with access to the blockchain to verify any transaction.

The payload of a transaction invokes a function of a smart contract with optional input parameters. The contract function acts upon a state variable, stored in the contract storage. New key/value pairs may be created, or existing values of a key updated. The execution of the function may emit an event, which is stored in the transaction trie of the block the transaction is contained in. Any node may listen to these events through a publish subscribe mechanism.

Fig. 5. Datalogical Ontology

[FIGURE]

While state variables may refer to arbitrary data, in the context of artifact centric processes, they may refer to lifecycle data or data objects. Due to the sensitive nature of the business artifact data, these are often stored in an 'off-chain' location. The state variable of the smart contract then merely contains a reference to the data, so that one may verify the integrity of that data by comparing the hash of the off-chain data with the one found in the smart contract.

TABLE III DATALOGICAL CLASS DEFINITION

| Class             | Definition                                                                                             |
|-------------------|--------------------------------------------------------------------------------------------------------|
| external actor    | an account owned by an agent, created by the generation of a cryptographic key pair                    |
| account wallet    | software package from which transactions may be initiated                                              |
| transaction       | a validated message sent to an account on a blockchain                                                 |
| smart contract    | internal account containing a shared artifact of an inter-organizational process                       |
| function          | specification of a procedural operation of a pro- cess transformation                                  |
| payload           | bytecode containing instructions to one or more functions of a process contract                        |
| event             | data emitted by a smart contract function to which nodes may subscribe                                 |
| transaction trie  | storage of a block containing event logs                                                               |
| block             | grouped data structure containing a set of trans- actions which are immutably stored on the blockchain |
| blockchain        | aggregation of all blocks of a specific blockchain platform                                            |
| contract storage  | dedicated storage of a process contract contained in the distributed ledger                            |
| state variable    | values of variables managed by a process con- tract which may change over time                         |
| key               | static identifier of a state variable                                                                  |
| value             | dynamic value associated with a key                                                                    |
| data object       | attributes and documents associated with an ar- tifact                                                 |
| off-chain storage | storage location which is not on a distributed ledger                                                  |

Consider our running example of a drop-shipment process again. On the datalogical level, an organizational actor external to the blockchain would generate transactions via specific 'wallet' software associated with the blockchain. Thus, placing a purchase order triggers a transaction to a smart contract. The transaction has a data payload containing instructions to invoke a particular smart contract function with specific input parameters. See the following code example:

```
f u n c t i o n placeOrder ( uint256 i d , uint256 amount , uint256 deliveryDate ) { r e q u i r e ( amount > = s t o c k && deliveryDate > = dateTime + 1209600); order . l i f e c y c l e . s t a g e = ' r e q u e s t e d ' ; emit OrderPlaced ( i d ) ; }
```

The retailer would call this function with the appropriate parameters, which emits an event 'OrderPlaced' with an attached order identifier to the transaction trie of the block the transaction was included in. The supplier may listen to these events by subscribing to them. Calling the placeOrder function modifies the 'order.lifecycle.stage' key, setting its value to 'requested'.

## V. MAPPING BETWEEN THE ONTOLOGICAL LAYERS

Now that we have presented an analysis of each ontological layer independently, we can construct a mapping between them. We will describe what the implications of an interorganizational process on the essential level are on the infological level, and in turn what the implications of infological state transitions are on the datalogical level.

## A. Essential to infological mapping

On the essential level, process participants conduct acts during standard interaction patterns called transactions. These acts result in facts, which are related to physical or artificial business objects. On the infological level, we see that agents invoke services in a process contracts, which maintains the state of artifact lifecycles and data objects.

Whereas the essential level depicts how new things are brought about through acts and facts, the infological layer provides for intellectual understanding of those acts and facts. An act on the essential level, such as the placement of a dropshipment order, maps to one or more service invocations on the infological level. In turn, the resulting essential fact maps to a state change on the infological level. Note that the business rules that apply to the process are represented at the infological level, in logical form. Enterprise ontology does not represent rules at the essential level.

## B. Infological to datalogical mapping

On the infological level, agents invoke services which transform the state of business artifacts. State transitions are bound by business rules contained in the process contract. On the datalogical level, we see that smart contracts contain programmable functions and state variables. Smart contracts are deployed on a particular blockchain.

The infological layer depicts how agents localize and transform information about business artifacts. A service invocation on the infological level - such as invoking an order placement service -maps to a transaction initiation on the datalogical level. Infological service invocations are bound by business rules contained in the process contract, and are represented by datalogical functions. Function execution is validated before the successful addition of a transaction in a block. Therefore, as long as business rules are programmable by logical functions, infological service invocations - and thus business artifacts states - by definition adhere to the associated business rules. Note that the state of a business artifact at any given point in time may be localized by reading the values of smart contract state variables.

## VI. DISCUSSION

This paper presents an ontological analysis of interorganizational business process artifacts managed by blockchain-based smart contracts. One of the main challenges facing inter-organizational processes, is that business networks must generally rely upon a trusted (third) party to maintain the state of process instances. Smart contracts offer an alternative since the blockchain they are deployed on are decentralized.

We have used a drop-shipment process as a running example throughout this paper. Drop-shipments are a common interorganizational process in the e-commerce industry, where a retailer handles the customer-facing process, but outsources the fulfillment of the order to an external supplier. Instead of the retailer buying products in bulk and keeping them in stock, the supplier now has full control over the logistical process. Traditionally, each organization would only have insight in their own processes and to a limited extent the process of their direct trading partner. Our ontology presents a novel way of managing business artifacts, where the data is shared among all process participants in one place. The integrity of the data is safeguarded by the blockchain network, thus creating a single source of truth. We have provided a mapping between the three ontological layers, which is expected to be of value to business architects and software engineers.

Interestingly, our research confirms an apparent synergy between artifact-centric process modeling and smart contracts. Smart contracts essentially consist of two elements, programmable logic and data storage. With these two elements, organizations may model business logic and data models of their shared processes. Based on our analyses, we encourage further research in the domain of inter-organizational processes managed by smart contracts to take on an artifact-centric approach, as opposed to an activity-centric or documentcentric approach. Specific research should be conducted in the tokenization of business artifacts, and the ontological implications of that.

Our findings are limited by a lack of empirical evaluation. However, to enhance formal correctness, our ontological analysis is grounded in DEMO and OntoUML, which are widely used ontological methodologies. Moreover, by using a running example we test whether the ontologies apply to a typical inter-organizational process model. Further research should be conducted to strengthen the ontological soundness. A technical proof of concept may be built to reveal potential missing concepts or associations within each of the three ontological layers. Furthermore, the datalogical ontology is now based on the Ethereum blockchain platform. Further research may be conducted to determine to what extent the datalogical ontology is dependent on the platform being used.

## VII. CONCLUSION

Managing inter-organizational business process artifacts with smart contracts introduces multiple research questions. The research questions of this study are (1) how are interorganizational processes related to business transactions, (2) what is the relationship between business artifacts and smart contracts, and (3) how do smart contracts manage business artifact lifecycles and states. In our paper, we have presented an ontological analysis of business artifacts managed by smart contracts. We have used the DEMO approach and modeled our ontologies in OntoUML. Each of ontological levels, the essential, infological and datalogical, respectively provide an answer to the research questions.

In the essential ontology, we see that an inter-organizational process is a collection of causally related business transactions. Each transaction consists of phases, in which process participants perform acts. The performance of such acts, either coordination or production acts, results in facts. A set of facts realizes the goal of a transaction. We conclude that essential acts are on the business level of an inter-organizational process, they initiate new processes and advance their phases.

On the infological level, services are invoked by agents who interact with process contracts. Process contracts represent business artifacts, of which each has a lifecycle and data objects. The state of both the lifecycle and data objects is directly managed by the process contract. Changes to the artifact state are triggered by service invocations, which are bound by business rules contained in the process contract. Thus, infological service invocations - as opposed to essential level acts - deal with the information perspective of processes by transforming artifact states.

Finally, on the datalogical level the infological state changes are realized. Agents send transactions to a blockchain via specific 'wallet' software. The transaction contains a data payload, containing instructions to invoke smart contract functions with specific input parameters. The function may update state variables, which are stored in the contract's internal storage. Each function call may emit events, to which any agent can subscribe.

## REFERENCES

- [1] J. Mendling, I. Weber, W. van der Aalst, J. v. Brocke, C. Cabanillas, F. Daniel, S. Debois, C. Di Ciccio, M. Dumas, S. Dustdar, A. Gal, L. Garcia-Banuelos, G. Governatori, R. Hull, M. La Rosa, H. Leopold, F. Leymann, J. Recker, M. Reichert, H. A. Reijers, S. Rinderle-Ma, A. Rogge-Solti, M. Rosemann, S. Schulte, M. P. Singh, T. Slaats, M. Staples, B. Weber, M. Weidlich, M. Weske, X. Xu, and L. Zhu, 'Blockchains for Business Process Management - Challenges and Opportunities,' ACM Transactions on Management Information Systems , vol. 9, no. 1, Apr. 2017, arXiv: 1704.03610. [Online]. Available: http://arxiv.org/abs/1704.03610
- [2] K. Korpela, J. Hallikas, and T. Dahlberg, 'Digital Supply Chain Transformation toward Blockchain Integration,' in Proceedings of the 50th Hawaii international conference on system sciences , 2017, p. 10.
- [3] S. Saberi, M. Kouhizadeh, J. Sarkis, and L. Shen, 'Blockchain technology and its relationships to sustainable supply chain management,' International Journal of Production Research , vol. 57, no. 7, pp. 21172135, 2019.
- [4] I. Weber, X. Xu, R. Riveret, G. Governatori, A. Ponomarev, and J. Mendling, 'Untrusted Business Process Monitoring and Execution Using Blockchain,' in Business Process Management , vol. 9850. Cham: Springer International Publishing, 2016, pp. 329-347. [Online]. Available: http://link.springer.com/10.1007/978-3-319-45348-4-19
- [5] O. Labazova, T. Dehling, and A. Sunyaev, 'From hype to reality: A taxonomy of blockchain applications,' in Proceedings of the 52nd Hawaii International Conference on System Sciences (HICSS 2019) , 2019.
- [6] V. Buterin, 'A next generation smart contract &amp; decentralized application platform,' 2014. [Online]. Available: https://cryptorating.eu/ whitepapers/Ethereum/Ethereum-white-paper.pdf
- [7] Jae-yoon Jung, Wonchang Hur, Suk-Ho Kang, and Hoontae Kim, 'Business process choreography for b2b collaboration,' IEEE Internet Comput. , vol. 8, no. 1, pp. 37-45, Jan. 2004. [Online]. Available: http://ieeexplore.ieee.org/document/1260702/
- [8] W. M. van der Aalst and M. Weske, 'The p2p approach to interorganizational workflows,' in International conference on advanced information systems engineering . Springer, 2001, pp. 140-156.
- [9] S. Yongchareon, C. liu, J. Yu, and X. Zhao, 'A view framework for modeling and change validation of artifact-centric inter-organizational business processes,' Information Systems , vol. 47, pp. 51-81, Jan. 2015. [Online]. Available: https://linkinghub.elsevier.com/retrieve/pii/ S0306437914001264

- [10] A. Nigam and N. S. Caswell, 'Business artifacts: An approach to operational specification,' IBM Syst. J. , vol. 42, no. 3, pp. 428-445, 2003. [Online]. Available: http://ieeexplore.ieee.org/document/5386806/
- [11] R. Hull, 'Artifact-Centric Business Process Models: Brief Survey of Research Results and Challenges,' in On the Move to Meaningful Internet Systems: OTM 2008 , R. Meersman and Z. Tari, Eds. Berlin, Heidelberg: Springer Berlin Heidelberg, 2008, vol. 5332, pp. 1152-1163. [Online]. Available: http://link.springer.com/10.1007/ 978-3-540-88873-4-17
- [12] R. Hull, V. S. Batra, Y.-M. Chen, A. Deutsch, F. F. T. Heath III, and V. Vianu, 'Towards a shared ledger business collaboration language based on data-aware processes,' in International Conference on ServiceOriented Computing . Springer, 2016, pp. 18-36.
- [13] J. L. G. Dietz, Enterprise Ontology . Berlin, Heidelberg: Springer Berlin Heidelberg, 2006. [Online]. Available: http://link.springer.com/ 10.1007/3-540-33149-2
- [14] G. Guizzardi, 'Ontological foundations for structural conceptual models,' Doctoral Thesis, University of Twente, Enschede, 2005.
- [15] J. L. G. Dietz and J. A. P. Hoogervorst, 'Enterprise ontology in enterprise engineering,' in Proceedings of the 2008 ACM symposium on Applied computing -SAC '08 . Fortaleza, Ceara, Brazil: ACM Press, 2008, p. 572. [Online]. Available: http: //portal.acm.org/citation.cfm?doid=1363686.1363824
- [16] G. Goldkuhl and M. Lind, 'The generics of business interactionemphasizing dynamic features through the bat model,' in Proceedings of the 9th International Working Conference on the Language-Action Perspective on Communication Modelling LAP , 2004, pp. 1-26.
- [17] S. Barrett and B. Konsynski, 'Inter-Organization Information Sharing Systems,' MIS Quarterly , vol. 6, p. 93, Dec. 1982. [Online]. Available: https://www.jstor.org/stable/248993?origin=crossref
- [18] H. L. Lee, K. C. So, and C. S. Tang, 'The Value of Information Sharing in a Two-Level Supply Chain,' Management Science , vol. 46, no. 5, pp. 626-643, May 2000. [Online]. Available: http://pubsonline.informs.org/doi/abs/10.1287/mnsc.46.5.626.12047
- [19] H. Zhou and W. Benton, 'Supply chain practice and information sharing,' Journal of Operations Management , vol. 25, no. 6, pp. 1348-1365, Nov. 2007. [Online]. Available: http://doi.wiley.com/10. 1016/j.jom.2007.01.009
- [20] S. Whang, 'Information sharing in a supply chain,' International Journal of Technology Management , vol. 20, no. 3/4, pp. 373-387, 2000.
- [21] C. Legner and K. Weber, 'THE CHALLENGES OF INTERORGANIZATIONAL BUSINESS PROCESS DESIGN -A RESEARCH AGENDA,' in Proceedings of the 15th European Conference on Information Systems , St. Gallen, Switzerland, 2007.
- [22] L. Xu, H. Liu, S. Wang, and K. Wang, 'Modelling and analysis techniques for cross-organizational workflow systems,' Systems Research and Behavioral Science: The Official Journal of the International Federation for Systems Research , vol. 26, no. 3, pp. 367-389, 2009.
- [23] M. Montali, M. Pesic, W. M. v. d. Aalst, F. Chesani, P. Mello, and S. Storari, 'Declarative specification and verification of service choreographiess,' ACM Transactions on the Web (TWEB) , vol. 4, no. 1, pp. 1-62, 2010.
- [24] J. Ghattas and P. Soffer, 'Evaluation of inter-organizational business process solutions: A conceptual model-based approach,' Inf Syst Front , vol. 11, no. 3, pp. 273-291, Jul. 2009. [Online]. Available: http://link.springer.com/10.1007/s10796-008-9090-7
- [25] W. M. van der Aalst, N. Lohmann, P. Massuthe, C. Stahl, and K. Wolf, 'Multiparty Contracts: Agreeing and Implementing Interorganizational Processes,' The Computer Journal , vol. 53, no. 1, pp. 90-106, Jan. 2010. [Online]. Available: https://academic.oup.com/ comjnl/article-lookup/doi/10.1093/comjnl/bxn064
- [26] K. Bouchbout and Z. Alimazighi, 'Inter-organizational business processes modelling framework,' in ADBIS (2) . Citeseer, 2011, pp. 45-54.
- [27] A. Norta, P. Grefen, and N. C. Narendra, 'A reference architecture for managing dynamic inter-organizational business processes,' Data &amp; Knowledge Engineering , vol. 91, pp. 52-89, May 2014. [Online]. Available: https://linkinghub.elsevier.com/retrieve/pii/S0169023X14000421
- [28] R. J. Glushko and T. McGrath, Document engineering . Mit Press Cambridge, 2005.
- [29] D. Cohn and R. Hull, 'Business artifacts: A data-centric approach to modeling business operations and processes.' IEEE Data Eng. Bull. , vol. 32, no. 3, pp. 3-9, 2009.
- [30] R. Hull, N. C. Narendra, and A. Nigam, 'Facilitating workflow interoperation using artifact-centric hubs,' in Service-Oriented Computing . Springer, 2009, pp. 1-18.
- [31] N. Lohmann and K. Wolf, 'Artifact-Centric Choreographies,' in Service-Oriented Computing , P. P. Maglio, M. Weske, J. Yang, and M. Fantinato, Eds. Berlin, Heidelberg: Springer Berlin Heidelberg, 2010, vol. 6470, pp. 32-46. [Online]. Available: http://link.springer. com/10.1007/978-3-642-17358-5-3
- [32] R. Hull, E. Damaggio, R. D. Masellis, F. Fournier, M. Gupta, H. Iii, S. Hobson, M. Linehan, S. Maradugu, A. Nigam, and R. Vacul´ ın, 'Business Artifacts with Guard-Stage-Milestone Lifecycles: Managing Artifact Interactions with Conditions and Events,' in Proceedings of the 5th ACM international conference on Distributed event-based system , 2011, pp. 51-62.
- [33] G. Meroni, L. Baresi, M. Montali, and P. Plebani, 'Multi-party business process compliance monitoring through IoT-enabled artifacts,' Information Systems , vol. 73, pp. 61-78, Mar. 2018. [Online]. Available: https://linkinghub.elsevier.com/retrieve/pii/S0306437917301242
- [34] J. Gordijn, 'E-business value modelling using the e3-value ontology.' in Value creation from e-business models . Butterworth-Heinemann., 2004, pp. 98-127.
- [35] W. E. McCarthy, 'The REA accounting model: A generalized framework for accounting systems in a shared data environment.' Accounting Review , pp. 554-578, 1982.
- [36] J. de Kruijff and H. Weigand, 'Understanding the blockchain using enterprise ontology.' in International Conference on Advanced Information Systems Engineering . Cham: Springer, 2017, pp. 29-43.
