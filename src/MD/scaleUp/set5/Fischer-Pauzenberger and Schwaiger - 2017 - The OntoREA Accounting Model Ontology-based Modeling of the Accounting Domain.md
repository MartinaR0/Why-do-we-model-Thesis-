[FIGURE]

## The OntoREA Accounting Model: Ontology-based Modeling of the Accounting Domain

Christian Fischer-Pauzenberger 1* and Walter S.A. Schwaiger 1*

1 Institute of Management Science, Technische Universität Wien, Theresianumg. 27, 1040 Wien, Austria

christian.fischer-pauzenberger@tuwien.ac.at , walter.schwaiger@tuwien.ac.at

Abstract. McCarthy  developed  a  framework  for  modeling  the  economic rationale  of  different  business  transactions  along  the  enterprise  value  chain described in his seminal article 'The REA Accounting Model - A Generalized Framework for Accounting Systems in a Shared Data Environment' Originally, the  REA  accounting  model  was  specified  in  the  entity-relationship  (ER) language. Later on other languages - especially in form of generic data models and UML class models (UML language) - were used. Recently, the OntoUML language was  developed  by  Guizzardi  and  used by Gailly et al. for a metaphysical reengineering of the REA enterprise ontology. Although the REA accounting model originally addressed the accounting domain, it most successfuly is applied as a reference framework for the conceptual modeling of enterprise  systems.  The  primary  research  objective  of  this  article  is  to  anchor the  REA-based  models  more  deeply  in  the  accounting  domain.  In  order  to achieve this objective, essential primitives of the REA model are identified and conceptualized  in  the  OntoUML  language  within  the  Asset  Liability  Equity (ALE) context of the traditional ALE accounting domain.

Keywords: REA  accounting model, ALE  accounting  model,  OntoUML, OntoREA accounting model.

## 1 Introduction

McCarthy  [1]  introduced  the  REA  accounting  model  to  conceptualize  the  economic  logic  of accounting  in  terms  of  economic  resources  (R)  that  are  exchanged  in  economic  events  (E) between economic agents (A). In contrast to conventional accounting literature he looked at the accounting theory from a stock and flow perspective with the REA accounting framework. This framework, called the REA accounting model, was developed using data modeling techniques, and  its  underlying  structure  is  found  to  consist  of  sets  representing  economic  resources, economic  events,  and  economic  agents  plus  relationships  among  those  sets.  [1,  p.  554].  The economic core of the REA accounting  model  is  the duality principle. The duality relationship expresses the economic rationale that scarce resources have a positive price that has to be paid in

* Corresponding author

©  2017  Christian  Fischer-Pauzenberger  and  Walter  S.A.  Schwaiger.  This  is  an  open  access  article licensed under the Creative Commons Attribution License (http://creativecommons.org/licenses/by/4.0).

Reference:  Ch.  Fischer-Pauzenberger  and  W.S.A.  Schwaiger,  'The  OntoREA  Accounting  Model: Ontology-based Modeling  of the  Accounting,'  Complex  Systems  Informatics  and  Modeling  Quarterly, CSIMQ, Issue no. 11, pp. 20-37, 2017. Available: https://doi.org/10.7250/csimq.2017-11.02

an  exchange  transaction  from  the  buyer  to  the  seller.  McCarthy  relates  economic  resources closely  to  tangible  assets.  He  explicitly  distinguishes  economic  claims  from  the  economic resources to emphasize the temporal imbalance between the flows of the economic resources in business transactions like, e.g. credit card sales and sales on account.

The  REA  accounting  model  was  extended  by  Geerts  and  McCarthy  [2],  [3]  to  the  REA business ontology by including a policy infrastructure next to the accounting infrastructure. This conceptualization extends the economic logic by a forward looking and a typification perspective so that  business  policies  can  be  considered  for the  acquisition,  conversion,  revenue  as  well  as financing and investment transactions. The term ontology refers to Gruber's definition [4] of an ontology  as  a  specification  of  a  conceptualization.  This  definition  is  mainly  used  in  the knowledge representation and management domain. It clearly distinguishes from the metaphysical  understanding  of  ontology.  Such  an  understanding  is  applied,  e.g.  by  Wand  and Weber  [5]  in  information  systems  research  where  they  use  Bunge's  metaphysical  ontology concept in order to ground information systems upon an ontological foundation.

A more recent development is Guizzardi's Unified Foundational Ontology (UFO) [6]. UFO is built  on the  metaphysical  foundation  of  the  four-category  ontology  by  Lowe  [7]  and therefore distinguishes at the highest level between Universals and Individuals. Universals are space-time independent  classifiers  that  define  patterns  of  features.  Individuals,  on  the  other  hand,  are particular things that instantiate specific Universals in space and time. Furthermore, UFO relies on a hierarchical object type structure [8] which gets further specialized by incorporating metaproperties along the way from the origin to the leaves. Meta-properties are ontological notions drawn from philosophy like the principle of essence and rigidity, identity, unity and dependency. These principles have their origins in Formal Ontology which is incorporated in OntoClean [9] as a further ontological source of UFO. Finally, the part of UFO (UFO-A) which deals with the meta-properties of the types of entity and relationship is supported with the OntoUML language [6], [10]. OntoUML is an UML extension that incorporates the ontological meta-properties and makes them accessible in ULM class diagrams via stereotypes. OntoUML can be considered as a modernized entity-relationship (ER) language by  covering ontologically differentiated types of entities and types of relationships.

Gailly  et  al.  [11]  are  the  first  ones  who  use the  OntoUML  language  in  order to  classify  the primitives in the REA enterprise domain ontology (REA-EO) in terms of the metaphysical UFO upper-level  ontology.  They  model  the  REA  primitives  represented  in  the  form  of  economic resource, economic event and economic agent in UFO terms as Role, Relator and Role Mixin, and duality is considered as Formal relation. This classification of the REA primitives has shown to be beneficial for their research focus related to REA's enterprise domain ontology. But for the applicability  of  this  classification  in  the  accounting  domain  the  question  arises:  Does  this classification also adequately cover all essential elements of the accounting domain?

In the article question will be answered in a negative way because of two reasons: Firstly, in the ALE accounting context it is important to identify the provider of the identity principle and not just the carriers of an identity principle. The identity providers have to be rigid so that they can always be traced back unanimously over time. This holds for economic resources, economic events  and  economic  agents  as  well.  Consequently,  e.g.  the  typification  of  an  REA-EO Economic  Resource  as  an  UFO  Anti-rigid  Sortal  Universal  is  not  adequate.  Secondly,  in  the Asset Liability Equity (ALE) accounting domain the duality relationship constitutes a material and not just a formal relationship. The materiality comes from the contracting that underlies each business  transaction.  This  contracting  mediates  between  the  economic  agents  in  an  economic event.  Furthermore  the  contracting  contains  a  value  constraint  between  the  opposite  flows  of economic resources in the dual economic events. The incorporation of the value constraint will be called Balanced Duality Relationship.

The  argumentation  for  the  deeper  anchoring  of  the  REA  models  into  the  ALE  accounting domain will be provided in two steps.

In the first step a refined representation of the REA-based accounting domain is constructed. This representation is a refined version of Schwaiger's [12] REA-based ALE accounting model. The refinement relates to the inclusion of the balanced duality relationship which integrates the value  constraint  into  the  duality  relationship.  Furthermore  the  claims  are  explicitly  delineated from  receivables  and  payables,  from  contractual  financial  instruments  and  from  the  owner's equity. By following this distinction, claims are only related to imbalances in the debit and credit events  arising  from  misaligned  event  realizations  (e.g.  sending  or  receiving  resources  before invoicing or without transfer of control).

In the second step the refined REA-based ALE accounting model is translated from the UML language  into  the  OntoUML  language.  In  this  translation  the  additional  vocabulary  of  the OntoUML language provides the ontological meaning in form of existence, identity, temporality and  modality  to  the  different  classes.  Equipped  with  this  additional  information  the  derived OntoREA  accounting  model  conceptualizes  a  framework  designed  to  be  used  for  different purposes. One possibility is its usage in the accounting (AIS - see Romney et al. [13]) as well as enterprise  information systems (EIS - see Dunn et al. [14]) research by establishing ontologybased  accounting  and  enterprise  information  systems.  Such  systems  could  be  designed  and implemented, e.g. within a model-driven software development approach (see, e.g. Brambilla et al. [15], Stahl and Völter [16] or Pergl et al. [17]) by establishing the OntoREA-based conceptual model first and subsequently transforming it into a software application.

The article is organized along the reification of different variants of the duality relationship. In the  subsequent  section  the  duality  relationship  is  reified  as  a  separate  UML  class  model.  The reason for this reification  lies  in an enhanced understandability of this essential  concept in the REA accounting model. This is helpful for capturing the extensions in the next section where the REA-based  ALE  accounting  model  is  based  upon  the  balanced  duality  relationship  which  is defined  and  reified  again  as  a  separate  UML  class  model.  Afterwards  the  refined  REA-based ALE  accounting  model  is  translated  into  the  OntoUML  language  by  directly  integrating  the balanced duality relationship and by specifying all cardinalities as well as OntoUML stereotypes. In the final section the conclusions of the article are provided.

## 2 REA Accounting Model: Reification of the Duality Relationship

The  REA  accounting  model  (Figure  1)  conceptualizes  a  generalized  accounting  framework designed to be used in a shared data environment where both accountants and non-accountants are interested in  maintaining  information about the same set of phenomena. This framework is developed using data modeling techniques, and its underlying structure is found to consist of sets representing  economic  resources,  economic  events,  and  economic  agents  plus  relationships among those sets. Correspondence of REA elements with the accounting theories is discussed in [1]. The practical  use  of  the  model  in  the  database  design  phases  of  view  modeling  and  view integration is presented, and some REA representations of accounting objects are reconciled with those representations found in conventional double-entry systems. [1, p. 554].

McCarthy  [1,  pp.  562-563]  uses  the  following  definitions  of  economic  resource,  economic event, economic agent and duality as well as claims [1, p. 568]:

-  Economic resources are defined ... to be objects that (1) are scarce and have utility and (2) are under the control of an enterprise. In practice, the definition of this entity set  can be considered equivalent to ... the term "asset" ... with one exception: economic resources in the schema do not automatically include claims such as accounts-receivable.
-  Economic  events  are  ...  "a  class  of  phenomena  which  reflect  changes  in  scarce  means [economic resources] resulting from production, exchange, consumption, and distribution."
-  Duality  relationships  link  each  increment  in  the  resource  set  of  the  enterprise  with  a corresponding decrement .... Increments and decrements must be members of two different

- event entity sets: one characterized by transferring in (purchase and cash receipts) and the other characterized by transferring out (sales and cash disbursements).
-  Economic agents include persons and agencies who participate in the economic events of the enterprise or who are responsible for subordinates' participation. Agents in this sense can  be  considered  equivalent  to  ...  "entities."  That  is,  they  are  identifiable  parties  with discretionary power to use or dispose economic resources.
-  Claims,  or  future  assets  ...  derive  from  imbalances  in  duality  relationships  where  an enterprise has either: (1) gained control of a resource and is now accountable for a future decrement  (future  negative  asset)  or  (2)  relinquished  control  of  a  resource  and  is  now entitled to a future increment (future positive asset).

Figure 1. REA Accounting model [1, p. 564] - ER language

[FIGURE]

Figure 2 shows the REA accounting model in the UML language which is used in the ISO/IEC 15944-4:2007  standard  related  to  the  Accounting  and  Economic  Ontology  (AEO)  to  model business transactions [18, p. 16] and by Schwaiger and Abmayer [12], [19], [20] for the REAbased  accounting  domain  modeling.  The  REA  accounting  model  is  focusing  on  the  resource flows that occur in economic transactions between the involved agents. The duality relationship expresses the economic principle that scarce resources have a positive price that has to be paid in an  exchange  transaction.  The  inclusion  of  the  business  location  information  in  the  REA accounting model is due to its intention that both accountants and non-accountants are interested in maintaining information. As the focus in this article is the accounting domain, this information will not be addressed any further.

Figure 2. REA Accounting model [12] - UML language

[FIGURE]

The figure contains the duality relationship named Duality . The capitalized naming intends to indicate a reification of that relationship, which  is introduced  in order  to  enhance  the understandability  of  this  important  concept.  To  keep  the  REA  accounting  model  close  to  its original version the reification is shown outside the model within a separate diagram.

For illustration purposes the duality relationship  is demonstrated within a simple example in Figure 3. In the cash purchase transaction the enterprise buys from the supplier a commodity and pays for it in cash. In this case the duality relationship connects one increment event (on the left hand side) with one decrement event (on the right hand side). The arrows indicate the resource flow  from  one  agent  (from  agent)  to  another  agent  (to  agent).  Concerning  the  agents  the  two involved  resources  flow  into  the  opposite  directions.  At  the  top  of  Figure  3  the  Duality relationship  is  shown  as  a  rectangle.  It  connects  the  increment  event  on  the  left  with  the decrement event on the right hand side.

Figure 3 . Duality relationship - cash purchase transaction

[FIGURE]

The reification model for the generic duality relationship in the UML language can be seen in Figure  4.  The  duality  relationship  is  reified  via  the  Duality  relationship  class  located  in  the middle  of  the  diagram.  The  Duality  class  is  linked  to  the  Increment  Event  class  and  to  the Decrement  Event  class.  According  to  the  cardinalities,  one  increment  (decrement)  event  is connected to one business transaction. On the other hand, one business transaction is connected to  one  or  many  increment  (decrement)  events.  Furthermore,  one  or  many  resource  flows  are connected to one increment (decrement) event; and one resource flow is linked to one increment (decrement) event. Finally two agents are involved in the business transaction, i.e. the from agent who delivers and the to agent who receives. Depending on the nature of the business transaction different internal  and/or external agents are involved. In the cash purchase transaction, e.g. the enterprise is an internal agent that receives the commodity from the supplier who is an external agent.

Figure 4. Reified Duality relationship - UML language

[FIGURE]

## 3 REA-based ALE Accounting Model: Reification of the Balanced Duality Relationship

Although  the  original  REA  accounting  model  is  intended  to  specify  the  accounting  domain  it does  not cover several important  accounting requirements.  The  following  are  the  main deficiencies of the REA accounting model with respect to the traditional Asset Liability Equity/ALE-accounting logic [21]:

1. The narrow focus on (tangible) assets is not compatible with the more comprehensive asset, liability and equity view of ALE accounting.
2. The duality relationship establishes matches between increment and decrement events but it does not cover the value constraint associated with the business transactions' debit and credit events, i.e. the balanced duality relationship.
3. The focus on resource flows is not sufficient to cover the recording requirements of changes in the resource values (e.g. depreciations).
4. The  broad  definition  of  claims  neglects  the  delineation  to  the  claims  related  assets  and liabilities (e.g. receivables, payables and financial instruments) as well as equity resources.

In order to eliminate these shortcomings the REA-based ALE accounting model developed by Schwaiger  [12]  is  considered.  To  promote  understandability,  in  this  article,  the  argumentation underlying this model is summarized as follows: The conventional reasoning in accounting starts with the accounting equation, which specifies the resources of the enterprise as assets and the claims to those resources as liabilities  and  equity.  The  assets  are owned  and  the  liabilities  are owed by the enterprise. The equity is the owner's claim to the net value of the enterprise which is defined as the difference of the assets and the liabilities. The account category (asset, liability, equity) governs how we record increases and decreases. For any given account, increases are recorded  on  one  side,  and  decreases  are  recorded  on  the  opposite  side.  The  following  Taccounts provide a summary :

```
Assets                         ||        Liabilities and Owner's Equity       . Increase = Debit | Decrease = Credit ||   Decrease = Debit | Increase = Credit
```

These are the rules of debit and credit. Whether an account is increased or decreased by a debit or a credit depends on the type of account. Debits are not 'good' or 'bad'. Neither are credits. Debits are not always increases or always decreases -neither are credits. [21, p. 92].

In  conventional  accounting stocks and flows of assets (A),  liabilities  (L)  and  equity  (E)  are considered. Consequently the ALE-based accounting includes more resource types than the REA accounting  model.  Next  to  the  tangible  resources  it  also  contains  financial  resources  and categorizes these into financial asset, liabilities and equity.

Once assets, liabilities and equity are considered, the increment and decrement events have to be aligned with the double-entry recording by using the debit and credit notations. The increment and  decrement  notations  used  in  the  REA  accounting  model  are  not  sufficient  to  cover  all business  transactions.  E.g.  a  balance  sheet  extension  transaction  in  form  of  a  debit  financing increases the cash resource and the liability resource at the same time. The double increase is not possible  in  the  REA  accounting  model  but  it  is  possible  according  to  the  ALE  category properties. By using the debit and credit concepts this problem gets solved. The increment of the cash is credited and the increment of the liability is debited.

The problem with the broad definition of economic claims is solved by narrowing the claim definition. In the ALE context, different types of claims can be categorized as follows:

-  Claims from the enterprise vis-à-vis its debtors - as assets (e.g. receivables).
-  Claims from the creditors vis-à-vis the enterprise - as liabilities (e.g. payables and loans).

-  Claims from the owner vis-à-vis the enterprise - as owner's equity.

The narrowed claim definition relates to those temporal imbalances in the duality relationship, which are not any of the three aforementioned claim types. Examples of such claims would be a delivery  of  goods  without  invoicing  or  transferring  control  rights.  Such  claims  are  not  yet recorded  in  the  double-entry  bookkeeping  system  although  resource  flows  already  occurred. Their inclusion into the REA-based ALE accounting model provides a good example why such a model  conceptualizes a generalized accounting framework. As in  the  REA-based  ALE accounting model all accounting requirements are fulfilled, the model actually conceptualizes a generalized full-accounting framework, which clearly distinguishes from the generalized (partial-) accounting framework related to the REA accounting model.

The  REA-based  ALE  accounting  model,  which  remedies  all  four  deficiencies,  is  shown  in Figure 5. Its distinguishing features are as follows:

-  It covers all resources related to the assets, liabilities and equity instead of the primary focus on physical assets and cash in the REA accounting model.
-  It  includes  the  business  transaction  class,  which  is  missing  in  the  REA  accounting  model. This element is the conceptual starting point of accounting professionals and academics. Its inclusion  anchors  the  ontology  in  the  accounting  domain.  Furthermore  the  business transaction class contains the value constraint requirement related to debit events and credit events, which is also missing in the REA accounting model.
-  It uses the value flow relationship related to debit and credit events instead of the stock flow relationship related to increment and decrement events in the REA accounting model. The reason for this modification lies in the fact that not only resource flows have to be accounted for  in  the  ALE  accounting  model.  In  actual  accounting  the  periodic  income  also  includes profits and losses that result, e.g. from changing resource prices. Such value changes occur without resource flows. On the other hand, all resource flows are related to value flows so that in the value flow relationship all accounting relevant events are captured.
-  It has a correctly specified claims class, which only contains the temporal imbalances in the duality  relationship  that  are  not  claims  that  underlie  certain  asset,  liability  and  equity positions from the balance sheet.

Figure 5. REA-based ALE Accounting model [12] - UML language

[FIGURE]

The  REA-based  ALE  accounting  model  can  conceptually  be  refined  by  integrating  the business transaction concept that contains the value constraint into the duality relationship. The combined  concept  is  termed balanced  duality  relationship .  This  relationship  is  capitalized  in Figure 6 to indicate its reification in a separate diagram.

Figure 6. REA-based ALE Accounting model (refined) - UML language

[FIGURE]

For illustration purposes also the balanced duality relationship is demonstrated first within a simple  example  (Figure  7).  In  an  acquisition  transaction  the  resource  that  flows  into  the enterprise  is  the  commodity.  The  outflowing  resource  is  cash.  The  inflowing  resource  is connected  to  the  debit  event Commodity  Inflow ,  which  increases  the  stock  of  the  commodity resource  in  the  enterprise.  The  outflowing  cash  resource  is  linked  to  the  debit  event Cash Disbursement , which decreases the enterprise's stock of the cash resource.

Figure 7. Balanced Duality relationship - cash purchase transaction

[FIGURE]

Furthermore, the  tax  consideration  is  incorporated  in  the  example.  This  can  be  seen  by  the second debit event, which is related to the value added tax (VAT). The VAT is included in the invoice amount and it is therefore paid in cash by the enterprise. It is a receivable against the tax authority  that  can  be  deducted  by  the  enterprise  from  the  VAT  payables  stemming  from  the enterprise's revenue businesses with its customers.

At the top of Figure 7 the Balanced Duality relationship is shown as a rectangle. It connects two debit events on the left with one credit event on the right hand side. The value constraint within  the  balanced  duality  relationship  can  be  seen  by  the  variables x and y in  the  diagram. These currency unit amounts ( x, y ) indicated on the three resource flows show that the absolute value of the two debit events is equal to the absolute amount of the credit event. This is the value constraint requirement, which has to hold in each business transaction. The '+' sign indicates an inflow  and  the  '-'  sign  signals  an  outflow.  Next  to  the  mathematical  expression  the  value constraint can be seen in iconic form by the position of the arrow in the middle of the figure. It is positioned straight down so that both sides of the scale have the same (monetary) weights. The reification model for the generic balanced duality relationship in the UML language can be seen in  Figure  8.  The  balanced  duality  relationship  is  reified  via  the  Balanced  Duality  relationship class located in the middle of the diagram. The Balanced Duality class links to the Debit Event class  and  to the  Credit  Event  class.  All  the  cardinalities  are  the  same  as  in  the  reified  duality relationship  model. The major distinction to this model is, firstly, the usage of the debit/credit event typification instead of the increment/decrement typification and, secondly, the inclusion of the value constraint that requires that the value of all debit events in the business transaction is the same as the value of all of its credit events.

Figure 8. Reified Balanced Duality relationship - UML language

[FIGURE]

The Balanced Duality relationship not only holds in acquisition, conversion and revenue, but also in financing and investment transactions. To illustrate this point a debt financing transaction is considered. In debt financing financial instruments are involved. These instruments distinguish from  physical  resources  and  cash  by  having  contractually  defined  future  commitments.  The inclusion of this future related information connected to financial resources is not required by the accounting  standards  and  consequently  it  is  not  modeled  in  the  REA-based  ALE  accounting model.

Figure 9 . Balanced Duality relationship - debt financing transaction

[FIGURE]

In  Figure  9 the  Balanced  Duality  relationship  is  shown  as  a  rectangle.  It  connects one  debit event (cash inflow) on the left with one credit event (debt issue) on the right hand side. The value constraint  within  the  balanced  duality  relationship  can  be  seen  again  by  the  balancing  of  the variables x , which takes the sign + x for the debit event and x for the credit event.

## 4 The OntoREA Accounting Model: Modeling the REA-based ALE Accounting Model in OntoUML

Guizzardi  [6],  [10]  developed  the  OntoUML  language  as  an  UML  extension  that  inherits  its expressiveness  from  the  Unified  Foundational  Ontology  (UFO)  and  makes  them  accessible  in UML class diagrams via stereotypes. All elements in OntoUML class diagrams, i.e. classes and associations,  are universals with  specific  meta-properties.  The  universals  are  distinct  from individuals as  their  instances.  This distinction corresponds to the difference  between class and instance in  object  oriented  programming.  The  universals  are  distinguished  into endurants ,  i.e. time existing entities  with  identity,  vs. perdurants ,  i.e.  temporal  occurrences.  For the  endurant universals  there  is  a  hierarchical  typification  which  results  in  a  bushy  tree  [10].  Along  the different paths of the tree subsequently more meta-properties are added. The leaves at the end of each path are the elements that can be used in the OntoUML language. They are the grey shaded elements in the last row of Figure 10.

Figure 10. Relation types and (monadic) entity types - UFO excerpt

[FIGURE]

The hierarchical arrangement in the typification tree is based upon generalization (specialization) relationships. Furthermore, universals of the same order can be related to one another  through  generalizations  (or  specialization)  relations.  This  particular  type  of  binary relation defines a universal as the parent (or the super-type) of another universal, the child (or the subtype). By specializing a universal, one defines a subset of individuals that instantiate the parent universal and share some characteristics [22, p. 26] .

After the aforementioned distinction of Individuals and Universals ,  Figure 10 shows that the latter are specialized into Relation Universals and Monadic Universals .

Relation  Universals are  defined  as  meta-concepts,  that  apply  to  groups  of  two  or  more Individuals . They get further differentiated into Formal Relations and Material Relations . While Formal  Relations can hold between  two Individuals , without the support of additional Individuals , Material Relations require an additional, external Universal called Relator Universal .

Monadic  Universals conversely  are  meta-classes,  whose  instances  can  be  instantiated  by singular Individuals . They get specialized by Endurant Universals , which ensures the Individual's persistence throughout time, in contrast to Perdurant Universals (not shown here), that do not persist over time.

Substantial  Universals and Moment  Universals both  generalize  to Endurant  Universals . Substantial Universal's instances are highly independent Individuals , they can exist alone where Moment Universals exist in other Individuals and depend on them. One specialization of Moment Universal is the Relator Universal . As mentioned above, it requires an external Universal for the Material Relation to hold.

The following distinction introduces the identity principle: While NonSortal Universals do not provide the identity principles for their instances, Sortal Universals do. Therefore, their instances are  able  to  carry  the  identity  principle. Identity  principle  is  a  key  feature  of  the  UFO,  which enables  individuals  to  be  distinguished  from  each  other.  Various  universals  define  different identity principles and thus different ways how to distinguish their individuals [23, p.4] .

The specialization of Sortal Universals to Rigid Sortals and AntiRigidSortals define the metaproperty of rigidity in a modal sense. The UFO distinguishes between rigidity and anti-rigidity as follows [6, p. 124]: A rigid universal is one that applies to its instances necessarily, i.e., in every possible  world. In contrast to the rigid universal, an anti-rigid universal applies to its instances contingently. Illustrating examples for different modal meta-properties are given in [6, p. 289]: Modal meta-properties play a fundamental role in conceptual modeling and ontology engineering. … there are a number of (meta)categories of types which are differentiated in terms of their modal meta-properties. For instance, while a kind such as person applies to its instances necessarily,  a phase such  as  teenager  or  a role such  as  student  apply  to  its  instances  only contingently.  In  other  words,  an  instance  of  a  person  cannot  cease  to  instantiate  that  type without  ceasing  to  exist.  In  contrast,  instances  of  a phase (teenager,  living  person)  or role (student, husband, employee) can move in an out of the extension of these classes without any impact of their identity.

A similar definition is as follows [23, p.5]: Rigid universal's instances cannot cease to exist to be their instances without ceasing to exist by themselves . On the contrary, anti-rigidity describes universals that contain an instance in their extension in one world which is not included in the extension in another world . Rigid Sortals are further specialized to Substance Sortals , which not only carry the identity principle, but also provide its own identity.

In  conceptual  modeling  entity  types and  relationship  types  are  the  most  fundamental constructs [24]. For the OntoREA accounting model to be developed the following entity types are of importance:

-  Kinds are rigid substance sortals and provide their own identity principle (rather than just carrying it). Kinds are also considered as an OntoUML model's backbone [23].

-  SubKinds are rigid sortals and do not provide their own identity principle, they are merely inheriting the principle from another Substance Sortal .
-  Roles  are anti-rigid  sortals and  therefore  can  change  their  instantiation  in  a  modal  sense according  to  an  extrinsic  generalization  condition.  Furthermore,  Roles  are  relationaldependent, they have to rely on at least one other universal. Roles get their identity principle through the generalization relation from the instance of its parent universal.
-  Phases  are anti-rigid  sortals as  well  with  a  significant  distinction  to  Roles.  Phases  are relational-independent  and  so  do  not  depend  on  another  universal  to  function.  Due  to  the predetermined disjoint and complete generalization sets, Phases, in contrast to Roles, change to other Phases according to their intrinsic generalization condition. As with Roles, Phases also get their identity principle through the generalization relation.

Next to the above-mentioned entity types the following relationship types will be important for the OntoREA accounting model to be developed:

-  Relator Universals, are moment universals which represent the objectification of a relational property. Relator Universals are existentially dependent on a multitude of individuals, thus, mediating them. Relators are the foundation of the so-called Material Relations and act as truth-makers of the relation.
-  Formal Relations hold directly between entities without requiring any intervening individual.

The remaining Entity and Relationship Types of the UFO are out of the scope, since they are not  used  in  the  discussed  OntoUML  models.  The  current  and  complete  version  of  the  UFO  is specified in the UFO reference [25].

Now all needed UFO and OntoUML ingredients are given, so that the REA accounting model can  be  constructed  in  the  OntoUML  language.  The  traditional  starting  point  of  an  OntoUML model is the identity providing Kind universal (substance sortal universal), which is represented in the OntoUML language as an accordingly stereotyped class ( Kind class). In Figure 11 the Kind class is used for the Economic Resource, Economic Event and Economic Agent.

Figure 11. REA Accounting model - OntoUML language

[FIGURE]

The Kind class possesses the meta-properties so that they are independently existent and that they  inherit  their  identity  to  their  subclasses  within  a  generalization  relation.  If  the  relation  is rigid, a single individual is an instance of the super-class and the subclass in all possible worlds (constellations). If the relation is not rigid, a single individual may be an instance of both classes in one world, but not in another. These flexibilities, i.e. non-rigidities within the inheritance and the  generalization  already  show  the  more  flexible  modeling  possibilities  in  the  OntoUML language compared to the rigid, i.e. non-modal UML language.

In  the  simplest  case,  all  OntoUML  elements  are  rigid  in  Figure  11.  In  this  case  the  REA accounting  model  does  not  have  any  modality  so  that  it  corresponds  to  a  model  in  the  UML language. The temporal and modal changes of OntoUML elements are not needed in the REA accounting  model  as  only  REA-related  snapshots  of  the  business  transactions  are  taken  over time. But the situation changes - as will be seen later on - in the REA-based ALE accounting model.

In Figure 11 the REA accounting model includes several special modeling constructs:

-  There  is  a  typification  of  the Kind class  Economic  Event  into  the  two SubKind classes Increment Event and Decrement Event via a disjoint and complete generalization set. In the mathematical sense such a set is a partition, so that an event can only be either an increment or a decrement event, i.e. there are only two possible states for the economic events to be in.
-  The two disjoint subsets of the two SubKind classes are related by the Relator class  REA Duality. This means that the duality relationship is reified via the Relator class that mediates between  the  increment  and  decrement  events.  This  intermediation  specifies  the Material relationship  called duality ,  which  is  shown  in  the  form  of  an  association  between  the  two SubKind classes.
-  The relationship between the Increment/Decrement Event and the Economic Resource is a Formal association named inflow / outflow . The distinction of Formal and Material relates to the reification of the relationship. Material relationships are reified and Formal relationships are not.
-  The relationship between the Economic Event and Economic Agent called participation is a Formal association  as  well.  The  cardinalities  in  the  figure  indicate  that  two  agents  are involved  in  the  relationship.  The  two  additional  lines  say  that one  agent  provides  and  the other receives.
-  Finally it can be seen that all the cardinalities are specified in the REA accounting model.

Now the final step is taken, i.e. the translation of the REA-based ALE accounting model into the OntoUML language is performed. This translation is shown in Figure 12 and the resulting model is called the OntoREA accounting model due to its modeling in the OntoUML language.

Figure 12. OntoREA Accounting Model - REA-based ALE Accounting in OntoUML

[FIGURE]

There  are  four  remarks  related  to  the  difference  between  the  REA  accounting  and  the OntoREA accounting model:

1. The Relator class Balanced Duality is used instead of the REA Duality class. The difference lies in the value constraint, which is included in the Balanced Duality class.
2. Debit  and  Credit  Event  classes  are  used  instead  of  the  Increment  and  Decrement  Event classes. The necessity for the change comes from the different resource types in the REAbased  ALE  accounting  model,  i.e.  asset,  liability  and  equity.  An  increase  in  liabilities  and equity  is  related  to  a  credit  event,  whereas  an  increase  of  assets  relates  to  a  debit  event. Consequently increases of the different resource types are not associated with only one event type. The same holds true for decreases of different resource types.
3. The Formal relationships  between  the  Economic  Resource and the Debit Event as well as Credit  Event  are  not  any  longer  an  inflow  as  well  as  outflow  association.  Instead  in-  and outflows can occur with debit as well as credit events. What really occurs depends on the type of the resource, i.e. asset, liability or equity.
4. An important additional OntoUML element is used for modeling of the resource types: the Phase element. The Phase class is an anti-rigid and a non-identity providing universal. Due to  its  anti-rigidity  it  possess  a  modal  meta-property  and  it  receives  its  identity  from  the superclass in the inheritance. The Phase class  is needed to model the resource types with a modal meta-property. This property allows the change of resource phases over time. Due to the disjoint and complete generalization set the assignment of the resources to the different phases  is  modeled  as  a  partition.  This  means  that  each  individual  resource  instance  is assigned to one phase. Over time the assignment can change. At first glance this might be confusing as normally the assignment stays the same over time. Such a rigid, i.e. non-modal behavior is typical  for  most assets, liabilities and equity. But a clear exemption are claims. According  to  the  definition  in  the  refined  REA-based  ALE  accounting  model,  claims  are negatively defined by imbalances in the balanced duality relationship that are neither assets, nor  liabilities,  nor  equity.  When  claims  materialize  they  convert  to  their  corresponding resource type. It has to be noted that this is only one example of a modal behavior of resource types  over  time.  There  are  more  such  resources  out  there  especially  in  the  context  of derivative financial instruments.

For technical validation purposes the OntoREA accounting model presented in Figure 12 was modeled  in  the Sparx  Enterprise  Architect software  application  equipped  with  the  OntoUML plugin as well. As the modeling did not show any problems, it can be concluded that the model fulfills all UFO axioms [11, p. 8]. Furthermore it is also possible to validate the substance of the OntoREA accounting model by comparing its underlying modeling decisions with the modeling constructs chosen in the reengineered REA enterprise ontology by Gailly et al. [11].

The  middle  column  in  Table  1  shows  the  UFO  universals  selected  by  Gailly  et  al.  in  their OntoUML model. Their modeling decisions with respect to the REA primitives relevant for the comparison are as follows:

-  An Economic  Resource is  modeled  as  an  UFO Role class,  an anti-rigid  sortal universal, carrying  but  not  providing  a  criterion  of  identity  for  its  instances.  Gailly  et  al.  justify  the anti-rigidity  that  an  economic  resource  is  not  of  the  type Economic  Resource in  every possible world. It is mentioned that if the economic resource perishes it no longer has value. Furthermore,  if  an  economic  resource  is  no  longer  under  control  of  an  economic  agent, Gailly et al. argue, it no longer is an economic resource. The properties, that legitimate the anti-rigidity are therefore being under control of an economic agent and having economic value .  Moreover, these  properties  are  considered  as  extrinsic  properties,  that  have  their origin in some kind of event or relationship [11, p. 8].
-  The Economic  Event is  modeled  as  an  UFO Relator class,  a  non-sortal  anti-rigid  mixin universal.  Justified  by that  according  to  its  definition,  the  Economic  Event  is  not  a

- standalone  kind  but  represents  a  mediating  entity  for  the  relation  between  an  economic resource and two economic agents (inside and outside), i.e. glues them together [11, p. 9].
-  The Economic Agent is  modeled as an UFO Role Mixin class. It is not supposed to carry a criterion of identity for its instances but instead represents an abstraction of the roles played, namely accountability of the inside agent and participation of the outside agent.
-  The  concept  of Duality is  modeled  as Formal  relation with  the  reasoning  that  they  have some similar characteristics of the entities they connect.

Table 1. Mapping of REA Primitives onto OntoUML constructs

| REA primitives                 | Mapping in Gailly et al. [11]   | Mapping in OntoREA Accounting Model   |
|--------------------------------|---------------------------------|---------------------------------------|
| Economic Resource              | Role                            | Kind                                  |
|  Asset/Liability/Equity/Claim | -                               |  Phase                               |
| Economic Event                 | Relator Universal               | Kind                                  |
|  Increment Event              |  -                             |  SubKind                             |
|  Decrement Event              |  -                             |  SubKind                             |
| Economic Agent                 | RoleMixin                       | Kind                                  |
|  Inside Agent                 |  Role                          | -                                     |
|  Outside Agent                |  Role                          | -                                     |
| Duality                        | Formal relation                 | -                                     |
| Balanced Duality               | -                               | Material relation                     |

The last column in Table 1 shows the UFO universals used in the OntoREA accounting model (Figure 12). There are some remarkable differences which are explained as follows:

-  The legal requirement in the ALE accounting domain to record the accounting information of  business  transactions  necessitates  (rigid)  substantial  sortal  universals  that  provide  the identity principle for their instances. In the REA-based ALE accounting context this relates to  the Economic  Resource ,  the Economic  Event as  well  as  the Economic  Agent which consequently are modeled in OntoUML in form of Kind classes. These three classical REA primitives  consequently  constitute  the  ontological  backbone  of  the  OntoREA  accounting model.
-  The Economic  Resource is  typified  into Phase classes  according  to  the  economic  value specialization  condition  for  distinguishing  between  Asset,  Liability,  Equity  and  Claim whereas this condition is considered as an intrinsic property of the resources. The argument for  this  lies  in  the  determination  of  the  resource's  economic  value  according  to  the resource's  intrinsic  quality  property.  Furthermore  the  modal  property  of  anti-rigidity  with respect to the Claim is not of a deterministic but of a probabilistic nature. This means that Claim  instances  do  not  have  to  switch  into  another  phase  in  a  temporal  deterministic sequence (like, e.g. transition from childhood to adulthood), but can change randomly (e.g. between accounts receivable and product liability in both directions).
-  The Economic Event is typified into rigid SubKind classes for the Debit Event and the Credit Event. Due to the rigidity the Debit Event and the Credit Event do not change over time. They inherit the identity principle of the Economic Event and they are mediated ('married') via the Relator class Balanced Duality. Furthermore it is important to note that the Economic Event and its typification are not modeling activities within perduring business transactions, but  instead,  they  are  important  for  recording  the  occurence  of  such  transactions.  The recording  of  the Economic  Event has  to  be  rigid  in  order  to  assure  trackability  of  the transactions over time.
-  The Balanced  Duality is  a material  relationship due  to  the  contracting  that  underlies business transactions and mediates between debit and credit events.

-  The Economic Agent is  -  as  already  mentioned - of an UFO Kind class so that it provides the identity principle and can be recorded. Its typification is left unspecified. Depending on the identity principle, the (anti-)rigidity and  the intrinsic or extrinsic nature  of the specialization properties, different UFO constructs can be adequate.

## 5 Conclusions

The primary research objective addressed in this article relates to a deeper anchoring of REAbased  accounting  models  into  the  ALE  accounting  domain.  For  this  purpose  the  OntoREA accounting model was developed by translating the REA-based ALE accounting model into an adequate  model  formulated  in  the  OntoUML  language.  The  adequacy  of  the  OntoREA accounting  model  stems  from  the  inclusion  of  the  balanced  duality  relationship  which  is  an essential primitive of the ALE accounting domain. Next to that, it contains a sharper definition of claims which is compliant within the ALE accounting context. Finally the OntoREA accounting model  is  expressed  in  the  OntoUML  language.  By  this,  the  rigidity  of  the  UML  language  is extended  to  allow  anti-rigid  typifications,  e.g.  in  form  of  temporal  and  modal  changes  of  the economic resources over time.

The  actual  benefits  of  a  conceptual  modeling  in  the  OntoUML  language  can  be  directly observed by comparing the REA-based ALE accounting model in Figure 6 with the OntoREA accounting model in Figure 12. The OntoREA accounting model is not only quantitatively more expressive but also qualitatively. Here are the following quantitative enhancements:

-  The complete specification of all relationship cardinalities.
-  The integrated reification of the balanced duality relationship.
-  The integrated typification that was demonstrated for the event and resource types.

The  qualitative  enhancement  relates  to  the  additionally  included  ontological  information  in form  of Kind , SubKind , Phase , Relator , Material , Formal , disjoint and complete .  This  added ontological information characterizes the very nature of all the elements (universals) in the REAbased accounting domain with respect to dependent and independent existence, possession and providing  of  identity,  rigidity  and  anti-rigidity  of  instantiations  as  well  as  temporality  and modality of the universals. In this light, new ways of thinking are available, for instance: in the resulting OntoREA accounting model the resources, events and agents are the identity providing universals. The event universals are rigid over time whereas the resource universals are non-rigid so that a modal behavior can be specified like, e.g. in the case of claims.

Summing up, the proposed model provides the following benefits:

-  The identification of the balanced duality relationship and its integration as a Relator class mediating between credit and debit events.
-  The  rigid  and  identity  principle  providing  economic  resources,  economic  events  and economic agents as Kind classes.
-  The rigid typification of economic events into the SubKind classes Debit Event and Credit Event.
-  The  anti-rigid  typification  of  economic  resources  into  the Phase classes  Asset,  Liability, Equity and Claim.
-  Enhancement of the OntoREA accounting model's ALE accounting compliance.

Accordingly,  the  inclusion  of  the  ontological  meta-properties  in  the  OntoREA  accounting model assures compliance and gives an improved expressiveness, which can be achieved neither in  the  UML  nor  in  the  ER  languages.  This  advantage  also  prevails  vis-à-vis  domain  specific languages as the DSL languages are normally constructed in Gruber's ontology understanding so that the ontological meta-properties are missing.

It is interesting to note that the REA-based ALE accounting model is just the first step where the benefits of the OntoUML language are prevailing. It can be expected that the full benefits of the  OntoUML  languages  will  be  seen  in  more  advanced  models  within  the  REA-based accounting  domain  like,  e.g.  the  REAC-based  accounting  model  [12]  that  includes  finance requirements and the REA business management model [19] that includes managerial planning and control systems. In these advanced models the temporal and modal changes are especially important due to the uncertainty that lies ahead of the conventional accounting focus, but that has to be captured in the business management context.

Finally, an  interesting  idea  for future research related to the REA enterprise ontology comes from an anonymous referee. Instead of only using enduring entities from the UFO-A for all REA primitives, it seems worthwhile to model economic events via perduring entities from the UFOB  and  economic  agents  via  agents  as  described  in  the  UFO-C  [6],  [24],  [25].  By  doing  this, enterprise models can be developed that cover a much broader range of aspects compared to the more narrow compliance requirements within the ALE accounting domain.

## References

- [1] W.E.  McCarthy,  'The  REA  Accounting  Model  -  A  Generalized  Framework  for  Accounting  Systems  in  a Shared Data Environment,' The Accounting Review , vol. LVII, no. 3, pp. 554-578, 1982.
- [2] G.L. Geerts and W.E. McCarthy, 'An ontological analysis of the economic primitives of the extended-REA enterprise  information  architecture,  ' Int.  J.  Account.  Inf.  Syst., vol.  3,  no.  1,  pp.  1-16,  2002.  [Online] Available: https://doi.org/10.1016/S1467-0895(01)00021-5
- [3] G.L. Geerts and W.E. McCarthy, 'Policy Level Specifications in REA Enterprise Information Systems,' J. Inf. Syst. , vol. 20, no. 2, pp. 37-63, 2006. [Online] Available: https://doi.org/10.2308/jis.2006.20.2.37
- [4] T.R. Gruber, 'A translation approach to portable ontology specifications,' Knowl. Acquis .,  vol.  5, no.  2,  pp. 199-220, 1993. [Online] Available: https://doi.org/10.1006/knac.1993.1008.
- [5] Y. Wand and R. Weber, 'An Ontological Model of an Information System,' IEEE Trans. Softw. Eng. , vol. 16, no. 11, pp. 1282-1292, 1990. [Online] Available: https://doi.org/10.1109/32.60316
- [6] G. Guizzardi, 'Ontological Foundations for Structural Conceptual Model,' 2005.
- [7] E.J. Lowe, 'The Four-Category Ontology: A Metaphysical Foundation for Natural Science,' Dialectica ,  vol. 60, no. 4, pp. 513-518, 2006. [Online] Available: https://doi.org/10.1111/j.1746-8361.2006.01078.x
- [8] G.  Guizzardi  and  G.  Wagner,  'Towards  Ontological  Foundations  for  Agent  Modelling Concepts  Using  the Unified  Fundational  Ontology  (UFO),' Agent-Oriented  Inf.  Syst.  II. ,  3508,  pp.  110-124,  2005.  [Online] Available: https://doi.org/10.1007/11426714\_8
- [9] N. Guarino and C.A. Welty, 'An overview of OntoClean,' in: Handbook on Ontologies , pp. 201-220 Springer International Publishing, 2009. [Online] Available: https://doi.org/10.1007/978-3-540-92673-3\_9
- [10] OntoUML: Specification 1.0. [Online] Available: http://ontology.com.br/ontouml/spec/.
- [11] F. Gailly, G. Geerts and G. Poels, 'Ontological Reengineering of the REA-EO Using UFO,' OOPSLA Work. Ontol. Softw. Eng ., October, 2009.
- [12] W.S.A.  Schwaiger,  'The  REA  Accounting  Model:  Enhancing  Understandability  and  Applicability,'  in: Conceptual  Modeling:  34th  International  Conference,  ER 2015,  Stockholm,  Sweden,  October  19-22, 2015, Proceedings. pp. 566-573 Springer International Publishing, 2015. [Online] Available: https://doi.org/10.1007/978-3-319-25264-3\_43
- [13] M. Romney and P.J. Steinbart, 'Accounting Information Systems,' Pearson Higher Education AU, 2012.
- [14] C.L. Dunn, J.O. Cherrington and A.S. Hollander, 'Enterprise information systems: A pattern-based approach,' McGraw-Hill/Irwin, 2005.
- [15] M. Brambilla, J. Cabot and M. Wimmer, 'Model-Driven Software Engineering in Practice,' 2012. [Online] Available: https://doi.org/10.2200/s00441ed1v01y201208swe001
- [16] M. Völter, T. Stahl, 'Model-driven software development: technology, engineering, management,' John Wiley &amp; Sons, 2013.

- [17] R. Pergl, T.P. Sales and Z. Rybola, 'Towards ontoUML for software engineering: From domain ontology to implementation model,' in: Lecture Notes in Computer Science (including subseries Lecture Notes in Artificial Intelligence and Lecture Notes in Bioinformatics). pp. 249-263, 2013. [Online] Available: https://doi.org/10.1007/978-3-642-41366-7\_21
- [18] Standardization/International, E.C.I.O. for:  'Information Technology-Business Operational,' View-Part 4: 'Business  Transactions  Scenarios-Accounting  and  Economic  Ontology,'  ISO/IEC  FDIS.  15944,  2007. [Online] Available: https://www.iso.org/obp/ui/#iso:std:67199:en
- [19] W.S.A. Schwaiger, 'REA Business Management Ontology: Conceptual Modeling of Accounting, Finance and Management  Control,'  in:  S.  España,  et  al.  (eds.)  Proceedings  of  the  CAiSE'16  Forum,  at  the  28th International  Conference  on  Advanced  Information  Systems  Engineering  (CAiSE  2016),  2016.  [Online] Available: http://ceur-ws.org/Vol-1612/paper6.pdf
- [20] W.S.A.  Schwaiger and  M.  Abmayer,  'Accounting and  Management  Information  Systems,'  Proc.  Int.  Conf. Inf. Integr. Web-based Appl. Serv. - IIWAS '13, pp. 346-352, 2013.
- [21] C. Horngren, et al., 'Accounting,' Pearson Higher Education AU, 2012.
- [22] T.P. Sales, 'Ontology Validation for Managers,' 2014, [Online] Available: https://www.researchgate.net/publication/268220197\_Ontology\_Validation\_for\_Managers
- [23] Rybola, Z. and Pergl, R.: Towards OntoUML for Software Engineering : Introduction to the Transformation of OntoUML into Relational Databases.
- [24] G.  Guizzardi,  G.  Wagner,  J.P.A  Almeida  and  R.S.S.  Guizzardi,  'Towards  ontological  foundations  for conceptual modeling: The unified foundational ontology (UFO) story,' Appl. Ontol ., vol. 10, no. 3-4, pp. 259271, 2015. [Online] Available: https://doi.org/10.3233/ao-150157
- [25] T.  Sales,  P.P.F.  Barcelos  and  G.  Guizzardi,  'Identification  of  semantic  anti-patterns  in  ontology-driven conceptual  modeling  via  visual  simulation,'  4th  Int.  Work.  Ontol.  Inf.  Syst.  (ODISE  2012),  Graz,  Austria. January 2012. [Online] Available: https://www.researchgate.net/publication/260545296\_Identification\_of\_Semantic\_Anti-Patterns\_in\_Ontology-Driven\_Conceptual\_Modeling\_via\_Visual\_Simulation
- [26] Ontology Project: UFO-A Specification. [Online] Available: http://ontology.com.br/ufo-a/spec/

## Additional information about the article:

| Author ORCID iD   | Christian Fischer-Pauzenberger - www.orcid.org/0000-0002-9071-9523 Walter S.A. Schwaiger - www.orcid.org/0000-0003-1868-7018   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Article history   | Received 16 September 2016 Last revision received 16 February 2017 Accepted 31 May 2017 Available online 31 July 2017          |
| Article PII       | S225599221700063X                                                                                                              |
