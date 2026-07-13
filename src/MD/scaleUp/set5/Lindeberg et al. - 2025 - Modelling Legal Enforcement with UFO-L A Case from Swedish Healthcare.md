## Modelling Legal Enforcement with UFO-L: A Case from Swedish Healthcare

[FIGURE]

[FIGURE]

Jöran Lindeberg 1( B ) , Paul Johannesson 1 , Erik Perjons 1 , Martin Henkel 1 , and Katarina Fast Lappalainen 2

1 Department of Computer and Systems Sciences, Stockholm University, Stockholm, Sweden

joran@dsv.su.se

- 2 Department of Law, Stockholm University, Stockholm, Sweden

Abstract. Organisations are increasingly governed by complex and multilayered systems of rules and regulations. In heavily regulated sectors such as healthcare, compliance with these rules poses significant challenges. Not only can rule compliance conflict with organisational goals, but varying interpretations by enforcement actors can also lead to conflicting or unpredictable outcomes. Decisions by regulatory authorities and courts, equipped with fines and other sanctioning powers, create new institutional realities for organisations. One way to examine and understand these complex systems of rules and actors is through the use of ontologies. This paper aims to investigate how the UFO ontology, and, specifically, the legal core ontology UFO-L, can be used, or extended, for creating patterns for modelling of organisational rule enforcement. To facilitate this investigation, a legal case regarding Swedish healthcare was selected to identify requirements for an ontology for legal enforcement. These requirements were then compared with the representation capabilities of UFO-L. The investigation revealed strengths and weaknesses of UFO-L and provided suggestions for its modification.

Keywords: Enterprise modelling · Compliance · Rule enforcement · UFO-L · Ontology · Healthcare · Legal Design

## 1 Introduction

Organisations are increasingly controlled by vast and multilayered systems of rules and regulations. In particular in heavily regulated sectors, such as healthcare, complying with all rules is challenging. Not only do organisations have to balance compliance against other rules, such as profits or creating value for citizens, but they sometimes will also find that different rules will push them in opposite directions. What is permitted or not in a particular situation has to be determined by institutional actors at different levels.

Within an organisation, these levels can include, for example, an employee, their manager, and a compliance officer. This hierarchical chain then continues outside of the organisation. Typically, a public authority will be in charge

c © The Author(s), under exclusive license to Springer Nature Switzerland AG 2025 M. Saeki et al. (Eds.): ER 2024 Workshops, LNCS 14932, pp. 267-283, 2025.

of enforcing compliance with the existing legislation. Organisations that do not accept this authority's decisions may have the possibility of appealing to a court, perhaps also to a second instance court. In cases of organisational collaborations, there can also exist an intermediate step between the internal rule and the external rules, composed of contracts and agreements.

Organisations, including their internal and external rules, are socio-technical systems that can be understood through the lens of complex adaptive systems (CAS) theory [6,20]. This is particularly strong in healthcare management [9,18, 19,22]. A CAS is composed of two fundamental elements: agents and constraints. Agents interact with each other according to the constraints, but the results of these interactions are far from certain. Agents will also receive feedback loops that allow them to evaluate the results of their actions and adapt accordingly by setting new constraints for themselves and others. As can be seen, organisations and regulations are part of a dynamic and indeterministic system in constant development at different levels. CAS theory recognises that the amount of control that can be exercised from above is limited, and even more so in organisational collaborations with loose constraints between actors.

Rules are key parts of social systems, but they are passive objects and can only achieve effects when they are mediated by actors [7]. Therefore, the enforcement of rules by institutional actors needs to be clearly understood both by the actors required to follow the rules and by those making the rules. Creating such a common understanding can be achieved through enterprise modelling. Although much research has been done on how enterprise modelling can facilitate compliance [16] and the use of ontologies in legal proceedings [21], less attention has been paid to modelling the legal enforcement apparatus that detects and corrects noncompliance.

In order to avoid having to reinvent the wheel, reusable meta-models, such as ontologies, have been developed for a multitude of domains. However, to the best of our knowledge, there is no ontology or reusable pattern for rule enforcement. One well-founded legal core ontology that has been used in a number of domains is UFO-L. This core ontology extends the Unified Foundational Ontology (UFO) to the legal domain. However, its capabilities to represent rule enforcement have not yet been investigated. Thus, our research aim in this paper is to clarify how UFO-L can be used to model organisational rule enforcement. Concretely, we propose a number of modelling patterns that can be useful for designers of information systems with aspects of legal enforcement.

Laws and regulation can be seen as externally imposed organisational rules and are often tightly intertwined with internal rules. Legislation is also usually well structured and publicly available. Such patterns can contribute to sensemaking for both lawmakers and regulated entities. Organisations need to understand their environment. In addition, at least large and formally advanced organisations will have their own procedures for monitoring, interpretation, and conflict resolution, resembling those of the legal enforcement system.

The remainder of this paper is as follows. Section 2 first presents a case of legal enforcement that is analysed and abstracted. Section 3 then reviews a number of legal modelling patterns based on UFO, which are used for designing our legal enforcement patterns. Section 4 presents our main contribution in the form of two complementary patterns of legal enforcement by regulatory authorities and courts. Section 5 discusses possible adaptations of UFO-L and presents additional preliminary patterns as illustrations. Section 6 concludes.

## 2 Methodology

## 2.1 Case Selection

The methodology involved testing UFO-L against a real-world case of rule enforcement. The case was selected according to the following criteria. First, the case should be sufficiently complex to provide a challenge for UFO-L. Previous research suggested that the domain of health data, characterised by heavy regulation, intricate care chains, and value conflicts between the right to health and the right to personal integrity, provides an interesting setting [14]. Second, the case should already have undergone a number of interventions by the legal enforcers. Third, for pragmatic reasons, the case should also be well documented. The chosen case was identified in a lawsuit between a private emergency hospital in Sweden, Capio S:t Görans sjukhus (hereafter referred to as the 'Hospital') and the Swedish Authority for Privacy Protection (Integritetsskyddsmyndigheten, IMY) 1 IMY has been designated as the supervisory authority with respect to the General Data Protection Regulation, GDPR, and the Data Protection Act (2018: 218), DPA, as well as the Patient Data Act (2008:355) and other data protection laws in Sweden.

## 2.2 Data Collection and Data Analysis

The dominant source for information about the case is the judgment by the Stockholm Administrative Court of Appeal, which includes the judgment by the County Administrative Court as well as the decision by IMY 2 . When needed, complementary information was searched, including, for example, references in legal articles and case law, and the IMY website. The analysis searched for semantic triples that explain the interaction: how the actors interacted, what was the legal basis for the interaction, and what were the legal implications of the interaction. A semantic triple is a subject-predicate-object statement, e.g. 'Judgment Xcites -Legislation Y', or 'IMYappeals -Judgment X'. The extracted triples were represented as an informal model 3

[1 For information in English, see https://www.imy.se/en/news/deficiencies-in-howhealthcare-providers-control-staff-access-to-patient-journal-data/.](https://www.imy.se/en/news/deficiencies-in-how-healthcare-providers-control-staff-access-to-patient-journal-data/)

3 The informal model is available as a Kumu.io map at https://kumu.io/joran/legalenforcement-informal-model-jusmod2024.

2 Kammarrätten i Stockholm, judgment 16 May 2022, case n ◦ 4548-21; Förvaltningsrätten i Stockholm, judgment 26 May 2021, case n ◦ 25868-20; Datainspektionen, decision 2 December 2020, ref. n ◦ DI-2019-3846.

## 2.3 Case Description

The case is summarised in the following timeline.

1. In March-April 2019 IMY conducted audits of eight health care providers, of which one was the Hospital regarding its electronic health record (EHR) systems. The legal base for the audit is Art. 58 in GDPR and Chap. 6, Sect. 1 of the DPA.
2. IMY concluded that the Hospital failed to undertake technical and organisational measures according to Art. 32 GDPR due to the lack of documentation in regard to the needs and risks analysis it is obligated to provide according to the regulations of the National Board of Health and Welfare to guide its assessments of the personnel's need to access information in the health records and the risks that this entails. IMY decided on a fine of 30 million SEK (equivalent to 2,6 million EUR). The legal basis for the sanctioning capabilities is Art. 58.2 in GDPR.
3. The Hospital appealed to the County Administrative Court (Förvaltningsrätten), the court of first instance. The court partly rejected the appeal but reduced the fine to a third.
4. Both IMY and the Hospital appealed to the Administrative Court of Appeal. The appeal court rejected the decision of IMY. It held that there was no basis in the GDPR to fine the hospital and that IMY had not proven that the hospital had not carried out its duties according to the rules and regulations applicable to the case.
5. IMY requested a leave to appeal to the Supreme Administrative Court (Högsta Förvaltningsdomstolen), the court of third instance. However, leave was not granted.

## 2.4 Abstracted Case Description

The IMY case was abstracted to the following general description: The case involves a public authority (in this case, IMY) using its legal mandate to audit the compliance of an organisation (in this case, the hospital) with specific regulations. Based on its findings and legal argumentation, the public authority makes an administrative decision which includes imposing sanctions if noncompliance is found. This decision is documented and creates new legal implications for the organisation, such as requirements to implement changes or payment of administrative fines. The organisation affected by the decision has the right to appeal in court. The court then reviews the case, potentially modifying or overturning the authority's decision. The final judgment can uphold, alter, or nullify the initial administrative decision by the public authority, depending on the court's interpretation of the law and the evidence provided.

## 2.5 Delimitations

To reduce the complexity of the model, a number of delimitations were established.

- -The existing legislation was taken as given.
- -The legal reasoning behind the decisions was not represented. We already know that UFO-L can do this. However, it was represented that certain legal provisions were invoked.
- -We were not modelling the internal organisational events that had legal implications, such as how the Hospital managed its information systems, only the legal events that followed, such as investigation and interpretation.
- -As for legal rights and duties that came into play during the process, the only ones represented were those that were made explicit from the final judgment AND involved the inspected organisation.
- -People are not represented, only organisations.
- -Differences in jurisdictions are not represented.

Then, we translated the informal model into a UFO-L compliant model. If needed, we would extend UFO with necessary elements. The modelling language used was OntoUML [1], a UML extension based on UFO [2]. In OntoUML, both classes and associations has stereotypes that correspond to UFO. The tool used was the OntoUML Visual Paradigm Plugin [3].

## 3 Fundamental Legal Modelling Patterns

We reviewed recent studies of legal modelling patterns that could provide a basis for the design of our rule enforcement patterns and found the following specific ontologies within the broader UFO framework:

- -UFO-B, which is part of the foundational level of UFO, and represent events [5].
- -UFO-L, a legal core ontology. It was originally created by Griffo as a doctoral thesis [10] grounded in theory by the legal scholars Wesley Newcomb Hohfeld and Robert Alexy. According to Hohfeld, all legal relations can be broken down into corresponding rights-duties, powers-liabilities, etc. [15]. In contrast, Alexy puts more emphasis on interpreting and balancing colliding principles (see, for example, [4]). UFO-L has been used to model, e.g., judicial decision making [11], and how legal powers can be manifested in legal events that create new rights and duties [12].
- -A core ontology on decision making, which we will refer to as UFO-D [13].

In the following, we will present and depict the identified patterns. The presentation includes rudimentary information about UFO; for a more detailed understanding, we refer to the sources mentioned above.

Figure 1 represents that an actor with a Legal Role takes part in a Legal Event. Griffo et al. state that 'legal events (e.g. signing of contracts, breaking laws, paying taxes, etc.) can create, change, or extinguish legal relations' [12, p. 5]. For practical modelling purposes, this means that a Legal Event creates, modifies, or terminates a Legal Relator between two parties. A party can be represented as an Actor or Role. It follows that the creation of general rules, such as lawmaking, also must be a Legal Event. A Legal Relator can be, for example, that a parent decides over a child, that a school must provide quality education for a child, or that the school must send reports to the ministry of education. Figure 1 also shows that a Legal Relator can be fulfilled, through manifestation, by other Legal Events.

Fig. 1. The Legal Actor-Event-Relator pattern, derived from UFO-L [12, Figure 2] and UFO-B [5, Figure 4]. Note that the OntoUML plugin for Visual Paradigm that was used lacks an association stereotype for &lt; modification &gt; , which is why only the &lt; creation &gt; and &lt; termination &gt; stereotypes are used in the diagrams.

[FIGURE]

Figure 2 expands the workings of the Legal Relator. As mentioned, the Legal Relator is a so-called truthmaker of a relation between a Right Holder and a Duty Bearer. The Right and Duty that are parts of the Legal Relator provide details for each party. Note that Rights and Duties are Modes, which are characteristics of one party, and can also be externally dependent of the other party. Also note that the Right-Duty pair is only one out of several UFO-L patterns of corresponding relations. Another example is Power-Subjection, which is used for expressing that one party can unilaterally create Duties for the other.

Figure 3 shows that a normative legal description, such as a law, a court decision document, or a contract, is prescribed by at least one Agentive Legal Institution, i.e. a formally established organisation. It also shows that the Legal Norms that are expressed in a Legal Normative Description are separate from their description. As can be understood from the multiplicity, some norms do not need a legal document to exist, such as customary law. The figure also shows that from the UFO-L legal hierarchy it can be deduced that Legal Role, Legal Event, and Legal Relator are all subclasses of Legal Thing, which can be defined by a Legal Normative Description [11, Figure 3]. Finally, the figure shows that a Legal Normative Description must somehow be created, namely through a Legal Event. In other words, Legal Events create Legal Relators both directly (Eventcreate -Relator) and indirectly (Eventcreate -Legal Normative Descriptiondefines -Legal Relator).

Figure 4 provides a basic representation of the legislative life cycle. As mentioned, lawmaking is outside the scope of this article, but this pattern is still included since we will adapt it to the life cycle of appealable legal decision documents. The figure shows how a Lawmaker makes a Legislative Enactment, creating a new Piece of Legislation. The legislation is later repealed by the same Lawmaker, which changes its status to a Repealed Piece of Legislation.

Fig. 2. The Legal Relator-Modes pattern, slightly adapted from UFO-L [11, Figure 4].

[FIGURE]

Fig. 3. The Legal Normative Description-Legal Norm-Legal Thing pattern, derived from UFO-L [11, Figure 3].

[FIGURE]

Fig. 4. The Legislation Enactment-Repeal pattern, derived from UFO-B, [5, Figure 2, Fig. 4].

[FIGURE]

The pattern from UFO-D confirms that a decision (e.g. a Legislative Enactment), is a type of Event that is done by an actor (e.g. a Lawmaker), and has a consequence (e.g. a Piece of Legislation). These relations have already been covered in Fig. 4.

## 4 Proposed Legal Enforcement Patterns

Until this point, the discussed patterns have been found in the literature, although presented with some adaptations, mainly to save space and reduce the complexity of the diagrams. In the following, they will be used to design two new patterns, needed to represent the legal enforcement case summarised in Sect. 2.4. The first pattern, presented in Fig. 5 and Fig. 6, covers the legal enforcement by a supervisory authority. The second pattern, presented in Figs. 7, Fig. 8, and Fig. 9, shows what happens if the supervised organisation appeals the decision of the supervisory authority.

## 4.1 Legal Enforcement Pattern

This pattern is divided into two overlapping diagrams. The first shows the legal situation that allows the legal enforcement, and the second depicts how the legal enforcement unfolds.

As can be seen in Fig. 5, the enactment of a law has created Legal Relators which gives a designated Supervisory Authority, for example an Independent Supervisory Authority as defined by GDPR, the right to conduct audits and also the power to impose administrative sanctions against a Supervised Organisation, including warning, reprimand, order (including restrictions and prohibitions), and an administrative fine.

Fig. 5. The Legal Basis diagram of the Legal Enforcement Pattern.

[FIGURE]

Figure 6 expands on Fig. 5, adding the events that are manifestations of the Legal Relators. The two classes Audit and Sanction Decision are both subclasses of Legal Case Decision, which in turn is a subclass of Legal Decision. (The Audit could have been broken down into several events, from the decision to audit, to the actual audit, but to simplify, it is treated as one single event.) An Audit is eventually followed by a decision by the Supervisory Authority, which may include use of a sanctioning capability. When the deadline for appeal has passed and the decision thus come into force, Legal Order Relators From Appealable Decision will be created or terminated.

However, if the decision is appealed, another complementing pattern is needed, which is presented in the next Section.

## 4.2 The Appeals Cycle Pattern

The Appeals Cycle Pattern represents what unfolds if an organisation that has been subject to sanctions by a supervising authority appeals.

Actors and Roles. We will start by unfolding the actors and roles shown in Fig. 7. In the domain of rule enforcement by Supervisory Authorities, the actors are organisations, either Public Authorities or Private Companies. A relevant Public Authority is either a Court or Authority With Mandate To Enforce. A Public Authority has a Legal Level, from a common authority to third (and final) instance in the court system. Any organisation can find itself as a Case Party in a legal case, and more specifically also as an Appealing Party.

Fig. 6. The Decisions Diagram of the Legal Enforcement Pattern.

[FIGURE]

Fig. 7. The Actors and Roles diagram of the Appeals Cycle pattern.

[FIGURE]

Decisions and Legal Relators. As shown in Fig. 8, a Public Authority makes a Legal Case Decision in an individual case, which is also a manifestation of an Applicable Law Legal Relator. (The facts of the case, not shown here, are another input.) The replaces association expresses that an appealable decision can eventually be overruled or otherwise affected by another decision of a higher court. The most common types of legal decision would probably be to Confirm, Reject, or Modify a decision, but its also possible to Vacate (nullify/void a case due to an erroneous decision by a lower instance), or Dismiss it.

As expressed by the Object Constraint Language (OCL) restriction code next to the Legal Decision class, replacement can only be done through decisions by a higher court. An Appealable Legal Case Decision will eventually be either associated with an Appeal Made, or Appeal Deadline Passed Without Appeal will occur, as expressed by the other OCL restriction code in the centre of the figure. The latter alternative will, just as a Non-Appealable Legal Case Decision, lead to the respective subclass of Legal Order Relator entered into force.

Fig. 8. The Decisions and Legal Relators Diagram of the Appeals Cycle Pattern.

[FIGURE]

Each Legal Relator can be broken down to a corresponding Right and Duty, which are Legal Modes. If a court has ruled, for example, that the Hospital would have to pay an administrative fine to the Swedish state, this would entail four relations. Two of those involve the right of the state to enforce and collect the fine. This right is inherent to the state, but it is also externally dependent on the actor that has the duty to pay, which in this case is the Hospital. The other two associations, in a corresponding manner, involve the duty of the Hospital to pay.

Documents and Appeals. A Legal Case Decision is formulated in a Legal Order Document, either appealable or not, as shown in Fig. 9. An Appealable Legal Order Document will first be Pending, and will then either be part of an appeal or not.

An Appeal is made by a Case Party and will also involve the Court that receives the appeal. This event ends the circle, and the new court will make a new decision.

Fig. 9. The Documents and Appeals Diagram of the Appeals Cycle Pattern.

[FIGURE]

## 5 Discussion About Alternative Patterns

In the previous section, we proposed two new patterns for representing legal enforcement by supervisory authorities. Based on this experience, in this section, we will discuss perceived challenges with UFO-L, and explore opportunities for modifications. In so doing, we will also propose additional alternative patterns that extend the ones in this paper.

## 5.1 Legal Norm, Legal Relator, and Legal Decision

The relation between Legal Norm and Legal Relator requires further investigation. We consider these two constructs to be closely related; however, we do not find a relation in the UFO-L models that we have studied. As modelled by UFO-L, Legal Events create Legal Relators, which are manifested as new Legal Events, and so forth [12]. We believe that this makes sense as long as Legal Normative Descriptions and Legal Norms [10] are not included, but when they are, it seems reasonable that at least one of these constructs could affect future legal decisions. After all, when legal experts argue their decisions, they often refer to texts and norms.

As shown in Fig. 3 presented in Sect. 3, a Legal Relator, like any Legal Thing, can be defined by a Legal Normative Description [11]. Moreover, a Legal Norm can, but does not have to, be expressed by a Legal Normative Description. A common example of Legal Norms without association to a Legal Normative Text is customary law. The question then becomes: How can UFO-L represent the association between a customary Legal Norm and a Legal Relator? It appears that it cannot, which we consider a limitation. On the other hand, in many domains, it can probably be expected that all Legal Norms are expressed in Legal Normative Descriptions. Also for pragmatic reasons it could often be best to simply associate Legal Relators to Legal Normative Descriptions, and not represent the separation between text and norm, which could probably sometimes be impractical.

A Legal Relator always defines a legal relation between parties. In contrast, a Legal Norm, in our understanding, is not limited to expressing bilateral relationships. In our understanding, Hohfeld [15] would argue that all legal realities can be expressed as relationships between two parties. However, Alexy [4] would likely consider this an over-simplification, and argue for more focus on the distinction between rules and principles, and in particular how to balance principles in case of conflicts. Certainly, there are also legal scholars who would have other views. From a pragmatic modelling point of view, expressing all norms as relators would probably not be very efficient or comprehensible. Even if we accept Hohfelds claim that all legal realities can be expressed as relationships between two parties, this does not mean that they should be .

Considering the above, we do not think it is possible to make a logically solid association between legal norms and legal relators. However, what could be represented is that a legal norm influences a legal decision. A possible pattern is shown in Fig. 10. Here, we have also included the facts of the case. The facts of the case could probably also be modelled as Legal Relators by representing the legal relations that the evidence leads to. However, that approach would not clearly distinguish between the facts and its interpreted legal implications. The advantage of the proposed pattern is its clear separation between the facts and the norms with which it is analysed. In summary, this pattern offers a new possibility for modelling decisions that constitute a vital part of legal enforcement.

## 5.2 Extending Legal Events

The Legal Events construct in UFO-L can be used for many different things that have legal implications. First, according to Burns and Flam [7], social actors can interact with rules in three ways: creating, interpreting, and implementing. In UFO-L, a Legal Event can be a formally defined institutional action, such as a legislator enacting new laws, or a court decision, as well as any natural act that has legal implications, such as breaking the law [12, p. 5]. In other words, Legal Event can represent all three interaction types. Second, Legal Events can in our understanding be a) legislative acts, which can create legal relators affecting millions of people, b) court orders, that is often only between two particular parties but can also affect whole categories of actors, and c) events that are not institutional but have legal implications, such as following or breaking a law. Third, the implementation of the law can be done by both action and inaction [17]. Figure 11 shows how these dimensions could be modelled.

Fig. 10. Alternative Pattern 1: Facts and Legal Norms in Legal Decisions.

[FIGURE]

## 5.3 Who Accepts a Legal Relator?

According to UFO-L, a Legal Relator is created by a Legal Event. An example is when someone clicks 'I agree' on a user agreement on the Web [12]. From that moment on, most if not all legal experts would agree that there are a number of legal relators between the two parties: the user and the company. But there would likely be some legal relator that the company believes exists, that the client or a privacy watchdog would claim does not exist. Other stakeholders could have different views. Perhaps the dispute would be settled by a court, whose decision may eventually be overruled by another court. In other words: 1) not all legal relators are recognised by all actors, 2) some actors have a legal mandate to establish the legal truth, and 3) even these truths are only preliminary until no further appeals can be made.

In our patterns in Sect. 4, we delimited the model to only show legal relators from final court judgments. However, it could be useful to also represent the different views that are constructed through the legal process, or even the conflicting legal analysis by actors without a particular mandate. In Fig. 12, we show how conflicting opinions can be modelled. We find inspiration from another part of UFO-L, which states that a Legal Normative Description must be recognised by at least two agents [10]. We propose representing that an actor can accept or contest a Legal Relator (neutral actors would have no association). If an actor is the first to accept a legal relator, this event would also include establishing it. If a legal relator is no longer accepted by anyone, it is effectively nullified.

Fig. 11. Alternative Pattern 2: Extending Legal Events.

[FIGURE]

Fig. 12. Alternative Pattern 3: Legal Case Decision Accepting Legal Relator.

[FIGURE]

## 6 Conclusion

In this paper, UFO-L, a well-founded legal core ontology, was used to model the legal enforcement by supervisory authorities. The domain description was created through the analysis of a legal case from Swedish healthcare, in which an authority acting as independent supervisory authority, as defined by GDPR, supervised the management of a private hospital employees' access rights to electronic health records. The authority decided on a substantial administrative fine for the hospital, but the case was appealed, and eventually a second-instance court rejected the decision. The modelling began with identifying and analysing existing patterns from UFO-L and other relevant UFO contributions.

Two new patterns were designed: one for the legal process between the supervisory authority and the supervised organisation, and another, as a continuation, of the appeals processes that followed in courts. Based on this design experience, some possibilities for further development of UFO-L were discussed and corresponding preliminary patterns were proposed.

As mentioned in Sect. 1, the legal system is also interesting to study to understand organisational rules in general. The patterns for legal enforcement in this paper can also be useful for representing and understanding the internal dynamics of an organisation, or a collaboration of organisations. As also explained in Sect. 1, organisations can be viewed as complex adaptive systems (CAS). In these systems, one cannot fully foresee how rules will be interpreted and enforced, constantly recreating institutional realities. This complex and dynamic environment will be more manageable if represented in information systems. One possible future research direction could be to explore how organisational rules and their enforcement can be included in digital twins of organisations [8]. Another direction could be to design systems aimed at providing feedback for rule makers, including law makers, on how the consequences of their decisions unfold throughout an organisational system.

## References

1. [OntoUML specification. https://ontouml.readthedocs.io/](https://ontouml.readthedocs.io/)
2. Unified Foundational Ontology (UFO) specification. https://dev.nemo.inf.ufes.br/ seon/UFO.html
3. OntoUML visual paradigm plugin, May 2024. https://github.com/OntoUML/ ontouml-vp-plugin, original-date: 2019-11-25T14:21:32Z
4. Alexy, R.: A Theory of Constitutional Rights. Oxford University Press, Oxford (2010)
5. Almeida, J.P.A., Falbo, R.A., Guizzardi, G.: Events as entities in ontology-driven conceptual modeling. In: Laender, A.H.F., Pernici, B., Lim, E.-P., de Oliveira, J.P.M. (eds.) ER 2019. LNCS, vol. 11788, pp. 469-483. Springer, Cham (2019). https://doi.org/10.1007/978-3-030-33223-5\_39
6. Anderson, P.: Perspective: complexity theory and organization science. Organ. Sci. 10 (3), 216-232 (1999). https://doi.org/10.1287/orsc.10.3.216
7. Burns, T.R., Flam, H.: The Shaping of Social Organization. Swedish Collegium for Advanced Study in the Social Sciences. SAGE Publications, London, England, May 1987
8. Caporuscio, M., Edrisi, F., Hallberg, M., Johannesson, A., Kopf, C., Perez-Palacin, D.: Architectural concerns for digital twin of the organization. In: Jansen, A., Malavolta, I., Muccini, H., Ozkaya, I., Zimmermann, O. (eds.) ECSA 2020. LNCS, vol. 12292, pp. 265-280. Springer, Cham (2020). https://doi.org/10.1007/978-3030-58923-3\_18

9. Ellis, B.: 29. An overview of complexity theory: understanding primary care as a complex adaptive system. In: Sturmberg, J., Martin, C. (eds.) Handbook of Systems and Complexity in Health. Springer, New York (2013). http://dx.doi.org/ 10.1007/978-1-4614-4998-0
10. Griffo, C.: UFO-L: a core ontology of legal aspects built on legal relations perspective. Ph.D. thesis, Technological Center, Computer Science Department, Federal University of Espírito Santo State (2018)
11. Griffo, C., Almeida, J.P.A., Guizzardi, G.: Legal theories and judicial decisionmaking: an ontological analysis. In: Proceedings of the 11th International Conference (FOIS 2020). Frontiers in Artificial Intelligence and Applications, vol. 330, pp. 63-76 (2020), publication Title: Frontiers in Artificial Intelligence and Applications
12. Griffo, C., Almeida, J.P.A., Lima, J.A.O., Prince Sales, T., Guizzardi, G.: Legal powers, subjections, disabilities, and immunities: ontological analysis and modeling patterns. Data Knowl. Eng. 148 , 102219 (2023). https://doi.org/ 10.1016/j.datak.2023.102219, https://www.sciencedirect.com/science/article/pii/ S0169023X23000794
13. Guizzardi, R., Carneiro, B.G., Porello, D., Guizzardi, G.: A core ontology on decision making. In: Proceedings of the XIII Seminar on Ontology Research in Brazil and IV Doctoral and Masters Consortium on Ontologies (ONTOBRAS 2020), vol. 2728, pp. 9-21. CEUR-WS (2020)
14. Henkel, M., Perjons, E., Lappalainen, K.F., Fors, U., Sjöberg, C.M.: Digitalization of health and social care collaboration: identification of problems and solutions. In: Joint Proceedings of RCIS 2024 Workshops and Research Projects Track. CEUR Workshop Proceedings, Guimarães, Portugal (2024). https://ceur-ws.org/ Vol-3674/RP-paper8.pdf
15. Hohfeld, W.N.: Fundamental legal conceptions as applied in judicial reasoning. Yale Law J. 26 (8), 710-770 (1917), publisher: JSTOR
16. Kim, H., Fox, M., Sengupta, A.: how to build enterprise data models to achieve compliance to standards or regulatory requirements (and share data). J. Assoc. Inf. Syst. 8 (2) (2007). https://doi.org/10.17705/1jais.00115, https://aisel.aisnet. org/jais/vol8/iss2/5
17. Mário de Oliveira Rodrigues, C., Bezerra, C., Freitas, F., Oliveira, I.: Handling crimes of omission by reconciling a criminal core ontology with UFO. Appl. Ontol. 15 (1), 7-39 (2020). https://doi.org/10.3233/AO-200223, https://content.iospress. com/articles/applied-ontology/ao200223, publisher: IOS Press
18. Plsek, P.E., Greenhalgh, T.: Complexity science: the challenge of complexity in health care. BMJ: Br. Med. J. 323 (7313), 625-628 (2001). https://doi.org/10.1136/ bmj.323.7313.625
19. Rouse, W.B.: Health care as a complex adaptive system: implications for design and management. Bridge-Washington-Natl. Acad. Eng. 38 (1), 17 (2008)
20. Turner, J.R., Baker, R.M.: Complexity theory: an overview with potential applications for the social sciences. Systems 7 (1), 4 (2019). https://doi.org/10.3390/ systems7010004
21. Vafaie, M., Bruns, O., Pilz, N., Waitelonis, J., Sack, H.: CourtDocs ontology: towards a data model for representation of historical court proceedings. In: Proceedings of the 12th Knowledge Capture Conference 2023, K-CAP 2023, pp. 175-179. Association for Computing Machinery, New York, NY, USA, December 2023. https://doi.org/10.1145/3587259.3627562, https://dl.acm.org/doi/10.1145/ 3587259.3627562
22. Zimmerman, B.: How complexity science is transforming healthcare. In: The SAGE handbook of complexity and management, pp. 617-635. SAGE Publications Ltd (2011). https://doi.org/10.4135/9781446201084
