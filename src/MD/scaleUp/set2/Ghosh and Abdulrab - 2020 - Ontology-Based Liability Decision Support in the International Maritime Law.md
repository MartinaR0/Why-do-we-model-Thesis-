- © 2020 The Authors, Faculty of Law, Masaryk University and IOS Press.

This article is published online with Open Access by IOS Press and distributed under the terms of the Creative Commons Attribution Non-Commercial License 4.0 (CC BY-NC 4.0). doi:10.3233/FAIA200882

## Ontology-Based Liability Decision Support in the International Maritime Law

## Mirna EL GHOSH a , 1 , Habib ABDULRAB a

a Normandie Universit´ e, INSA Rouen, 76000, Rouen, France

Abstract. In this paper, we present an ontology-based liability decision support task in the international maritime law, specifically the domain of carriage of goods by sea. We analyze the liabilities of the involved legal agents (carriers and shippers) in case of loss or damage of goods. Thus, a well-founded legal domain ontology, named CargO-S, is used. CargO-S has been developed using an ontology-driven conceptual modeling process, supported by reusing foundational and legal core ontologies. In this work, we demonstrate the usability of CargO-S to design and implement a set of chained rules describing the procedural aspect of the liabilities legal rules. Finally, we employ these rules in a liability rule-based decision support task using a real case study.

Keywords. well-founded legal domain ontologies, legal decision support, ontologybased decision support, maritime law

## 1. Introduction

Legal decision support aims to help solving problems in the juridical domain. The most commonly known approaches focus on employing rules to describe judges' strategies and procedures to analyze legal issues [1]. However, the particular characteristics of the legal domain cause specific difficulties in establishing such tasks [1]. In this study, we propose a decision support task that helps making decisions in the legal domain using ontological models. The implementation of such tasks implies creating an appropriate legal domain ontology that reflects as much as possible the real application domain [2]. Ontology models that are faithful to realities are called well-founded domain ontologies [3]. These ontologies are grounded in validated foundational ontologies where concepts and relations are previously analyzed in the light of a foundational ontology. The domain application of this work is international maritime law. Specifically, the domain of carriage of goods by sea represented by the Hague-Visby Rules 2 is designated. The main goal is to define the liabilities of the involved legal agents (carriers and shippers) in case of loss or damage of goods. Thus, a well-founded legal domain ontology, named CargOS, is used. In this work, we do not expose the building process of CargO-S. However, we demonstrate the ontology's usability to design a set of chained rules describing the procedural aspect of liabilities legal rules. Furthermore, we employ these rules in a rule- based decision support task. The remainder of this paper is organized as follows: Section 2 introduces CargO-S. Section 3 discusses the modeling and formalizing of legal rules. In section 4, we employ the formalized rules in a decision support task. Finally, section 5 concludes the paper.

1 Corresponding Author:

2 Hague-Visby Rules is a set of international rules for the international carriage of goods by sea, Wikipedia, last visited September, 04 2020

## 2. CargO-S: A Well-Founded Legal Domain Ontology for the Domain of Carriage of Goods by Sea

In this section, we briefly introduce CargO-S, a pattern-based well-founded legal domain ontology for the domain of carriage of goods by sea. CargO-S has been developed using an ontology-driven conceptual modeling process [4] and grounded in the unified foundational ontology UFO by applying the ontology-driven conceptual modeling language OntoUML [5]. Besides, the development of CargO-S has been supported by reusing conceptual ontology patterns from UFO[3] and the legal core ontology UFO-L [6]. The structure of CargO-S is composed of three different layers located at different granularity levels: upper , core and domain . The upper and core layers are composed of different types of ontology patterns, which are applied either by extension or analogy for building the domain layer. In this study, we focus on the domain layer where different legal categories are defined: (1) legal roles such as, Carrier and Shipper ; (2) legal relators such as, Contract of Carriage of Goods by Sea , Right Duty to Indemnity , and Disability Immunity to Liabilities ; (3) legal moments such as, Right to Indemnity , and Disability to Indemnity ; (4) legal events, such as Carriage of Goods by Sea , Loss or Damage of Goods ; (5) situations, such as Inaccuracies and Unseaworthiness .

## 3. Modeling and Formalizing the Procedural Aspect of Liabilities Legal Rules using CargO-S

In this section, we describe the modeling and formalizing of legal liability rules using CargO-S. Rule 1 is an example of a simple legal rule where a situation of inaccuracies triggers the loss or damage of goods.

Rule 1. (Article 3. Section 5) The shipper shall indemnify the carrier against all loss, damages and expenses arising or resulting from inaccuracies.

For the modeling process, a core ontology pattern ( Right duty to an Action ) is applied by analogy with the legal rule for representing its procedural aspect. Following the isomorphism principle stated by Bench-Capon [7] the conceptual model is transformed into formal rule. In this paper, we use SWRL 3 as a formal rule language. By representing legal rules using SWRL, we assume that they are conflict-free and will be complied with. In Figure 1, we depict the ontological model of Rule 1 represented in OntoUML [5].

3 https://www.w3.org/Submission/SWRL/

Figure 1. Modeling the procedural aspect of Rule 1 represented in OntoUML.

[FIGURE]

Based on the ontological model, two chained formal rules are generated where the latter's condition is the former's consequence. These rules are represented by an obligation rule in the following form: IF condition (operative facts) THEN conclusion (legal effect) .

```
Carrier(?c) ∧ Shipper(?s) ∧ Legal_Relator(?r) ∧ mediates(?r, ?c) ∧ mediates(?r, ?s) ∧ Loss_or_Damage_of_Goods(?d) ∧ grounds(?d,?r) ∧ Inaccuracies(?i) ∧ has_part(?i, ?c) ∧ triggers(?i, ?d) = ⇒ Right_Duty_to_Indemnity(?r) ∧ mediates(?r, ?s) ∧ mediates(?r, ?c) ∧ defines(Article3, ?r) Right_Duty_to_Indemnity(?r) ∧ Carrier(?c) ∧ Shipper(?s) ∧ mediates(?r, ?c) ∧ mediates(?r, ?s) = ⇒ has_a_right_to_indemnity_against(?s, ?c)
```

## 4. Rule-Based Liability Decision Support

This section outlines the formal rules' employment in a lightweight decision support task. Given an event of carriage of lychees operated by the carrier Service Capricorne and the shipper Lacour Exotics . At the destination port, a prolonged parking for seven days has occurred. Such a situation of inaccuracies have triggered the damage of fruits. Thereby, based on the given facts, different legal effects are computed and generated following the execution of rules (Figure 2). As a legal decision, we obtained that the shipper has a right to indemnity against the carrier.

Figure 2. The legal effects as inferences following the execution of SWRL rules in Prot´ eg´ e 4

[FIGURE]

## 5. Conclusion

In this paper, we presented an ontology-based liability decision support task in international maritime law. We demonstrated that decision support could solve basic legal problems using well-founded legal domain ontologies. A well-founded legal domain ontology, named CargO-S, has been used for this purpose. In CargO-S, various legal categories have been defined by reusing conceptual ontology patterns from foundational and core ontologies. Core patterns have been applied by analogy to describe the procedural aspect of legal rules. Furthermore, the legal rules' ontological model has been transformed into chained formal rules embedded in a lightweight decision support task. This work was a preliminary study. In further works, we will examine more complex rules taking into consideration different formal rule languages. Acknowledgment : This work has been supported by the European Regional Development Fund (ERDF) under Grant Agreement n HN0002134 in the project CLASSE2.

## References

- [1] Zeleznikow J (2004) Building Intelligent Legal Decision Support Systems: Past Practice and Future Challenges. In: Fulcher J, Jain L C (eds) Applied Intelligent Systems. Studies in Fuzziness and Soft Computing, vol 153. Springer, Berlin, Heidelberg
- [2] Daduna J, Hunke K and Prause G (2012) Logistics Corridors and Short Sea Shipping in the Baltic Sea Area. In Proceedings of the International Research Conference on Short Sea Shipping, Estoril, Portugal
- [3] Guizzardi G (2005) PhD Thesis. Ontological Foundations for Structural Conceptual Models. TelematicaInstitut / CTIT
- [4] El Ghosh M, Abdulrab H (2019) The application of ODCM for Building Well-founded Legal Domain Ontologies: A Case Study in the Domain of Carriage of Goods by Sea Conventions. In: International Conference on Artificial Intelligence and Law, ICAIL, Montreal
- [5] Guerson J, Sales T P, Guizzardi G and Almeida J (2015) OntoUML Lightweight Editor: A ModelBased Environment to Build, Evaluate and Implement Reference Ontologies. In: 19th IEEE Enterprise Computing Conference.
- [6] Griffo C (2018) UFO-L, A Core Ontology of Legal Aspects Building Under the Perspective of Legal Relations, PhD Thesis, Federal University of Espirito Santo
- [7] Bench-Capon T and Coenen F (1992) Isomorphism and Legal Knowledge Based Systems. In: Artificial Intelligence and Law 1.1, pp. 65-86
