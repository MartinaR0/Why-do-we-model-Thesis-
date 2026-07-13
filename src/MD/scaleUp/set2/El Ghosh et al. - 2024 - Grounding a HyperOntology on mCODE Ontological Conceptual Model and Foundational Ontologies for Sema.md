## Grounding a Hyper-Ontology on mCODE Ontological Conceptual Model and Foundational Ontologies for Semantic Interoperability in the Oncology Domain

Mirna El Ghosh 1 , ∗ , † , Christel Daniel 1 , Catherine Duclos 2 , Varvara Kalokyri 3 Jean Charlet 1 , Melanie Sambres 1 , Gianna Tsakou 4 , Manolis Tsiknakis 3 and Ferdinand Dhombres 1

1 Sorbonne Université, Inserm, Université Sorbonne Paris-Nord, LIMICS, Paris, France

2 Université Sorbonne Paris-Nord, Inserm, Sorbonne Université, LIMICS, Paris, France

3 Institute of Computer Science, Foundation of Research and Technology Hellas, Heraklion, Greece

4 MAGGIOLI S.P.A., Research and Development Lab, Marousi, Greece

## Abstract

Grounding biomedical ontologies in core ontological conceptual models considering foundational ontologies is a prominent top-down approach neglected in domain-specific ontologies but is required to support semantic interoperability. This study discusses developing a core ontological model for mCODE (minimal Common Oncology Data Elements), which captures and reflects the main oncology's ontological semantics on which a hyper-ontology for the oncology domain is grounded. To conduct the ontological analysis, Ontology-Driven Conceptual Modeling (ODCM) is applied using OntoUML, an ontologically well-founded language whose meta-model complies with the Unified Foundational Ontology (UFO). The top-down approach has helped overcome conflicting or heterogeneous descriptions of oncology concepts, maintaining coherent ontological content and semantic interoperability.

## Keywords

Ontological Analysis, Conceptual Modeling, OntoUML, Foundational Ontologies, mCODE, Semantic Interoperability, Oncology

## 1. Introduction and Motivation

Tumor (or Neoplasm ), Tumor Morphology , and Cancer (or Malignant Tumor ) are core concepts in the oncology domain used to describe different medical contexts. However, conflicting or heterogeneous representations of these concepts in commonly known biomedical ontologies or terminologies, such as SNOMEDCT 1 and NCIT 2 , make interoperability challenging (see Figure 1). SNOMEDCT is an ontology-based medical terminology standard that has been largely used to develop ontologies in the biomedical domain. NCIT is a reference terminology in the oncology domain developed and maintained by the National Cancer Institute. SNOMEDCT differentiates

FOAM 2024: FAIR principles for Ontologies and Metadata in Knowledge Management Co-located with FOIS 2024 (JOWO Workshops) 15-19 July 2024 (Enschede, Netherlands)

∗ Corresponding author.

[Envelope-Open mirna.el-ghosh@inserm.fr (M. E. Ghosh)](mailto:mirna.el-ghosh@inserm.fr)

[FIGURE]

[FIGURE]

[0000-0002-0877-7063 (M. E. Ghosh)](https://orcid.org/0000-0002-0877-7063)

[FIGURE]

© 2024 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).

1 https://www.snomed.org/, Accessed April 23, 2024

2 https://ncithesaurus.nci.nih.gov, Accessed April 23, 2024

,

Figure 1: An example of a conflicting description of oncology concepts in SNOMEDCT/NCIT (colored shapes are potential mappings between SNOMEDCT and NCIT)

[FIGURE]

between Neoplasm , or Tumor , (108369006) and Malignant neoplastic disease (363346000), having as synonyms Malignant tumor and Cancer , where the former is a 'morphologic abnormality' that belongs to Body structure (123037004) and the latter is a Disease , or Disorder , (64572001). However, in NCIT, Neoplasm (C3262) is a Disease or Disorder (C2991) having Tumor Morphology (or Neoplasm by Morphology ) (C4741) and Malignant neoplasm , or Cancer , (C9305) as specific categories. In this context, mapping Carcinoma of breast (SNOMEDCT:254838004) with Breast Carcinoma (NCIT:C4872) is challenging due to the heterogeneity of their ascendants. Facing this heterogeneity and to clarify these concepts' specifications and medical aspects, we refer to the minimal Common Oncology Data Elements (mCODE) 3 [1] largely adopted within healthcare establishments which are increasingly implementing FHIR 4 . mCODEis a 'Domain of Knowledge' implementation guide intended to show how to represent clinical concepts generally, aiming to increase interoperability in the oncology domain. Among various profiles and extensions, Tumor , Tumor Morphology , Histology/Morphology , and Primary Cancer Condition are defined in mCODE STU4 model. In this context, inspired by [2], there is a need for an ontological analysis that reveals the ontological conceptual model of mCODE, helping to achieve semantic clarity on oncology's main concepts.

In the EUCAIM project 5 , we employ an ontological approach toward semantic interoperability among heterogeneous cancer image data models and distributed big cancer data repositories

3 https://build.fhir.org/ig/HL7/fhir-mCODE-ig/, Accessed April 11, 2024

4 https://www.hl7.org/fhir/

5 https://cancerimage.eu/

[3]. We propose developing a FAIR-compliant hyper-ontology to integrate and federate large volumes of cancer image and clinical data, including many types of cancer (e.g., Breast cancer, Cancer of prostate, Lung cancer, etc.), aiming to establish semantic interoperability among the diverse data sources. The hyper-ontology goal is to define domain-specific concepts and ground them on core oncology concepts in a coherent semantic context. Additionally, semantic mappings are applied with various controlled vocabularies and ontologies in the biomedical domain (e.g., SNOMEDCT, NCIT, ICDO3, etc.). To tackle the heterogeneity of oncology concepts and ensure a well-founded representation of the oncology domain, we propose grounding the hyper-ontology on validated foundational ontologies (e.g., UFO [4, 5], BFO [6, 7]), which help to improve interoperability by being 'translators of intended meaning' [8]. The grounding process considers developing the mCODE core ontological model that reflects the main ontological semantics of the oncology domain. To conduct the ontological analysis, there is a need for a language that supports making explicit the ontological nature of real-world entities and the relations between them [9]. In this regard, Ontology-Driven Conceptual Modeling (ODCM) is applied using OntoUML 6 [10], an ontologically well-founded language whose meta-model complies with the ontological distinctions and axiomatization of UFO. In the remainder of the paper, section 2 overviews this study's background, section 3 discusses the grounding approach, the formal results are given in section 4, and section 5 concludes the paper.

## 2. Background

## 2.1. EUCAIM's Hyper-Ontology

The main challenge of the hyper-ontology is to facilitate integration and interoperability among data stored and modeled using diverse clinical and imaging data models and associated terminologies. Two main data models are considered in EUCAIM: OHDSI-OMOP 7 and HL7FHIR 8 . In OMOP, domains are defined to which the concepts of the standardized vocabularies can belong, such as Person , Condition , Measurement , Drug , and Procedure . Meanwhile, FHIR is built upon a set of resources, including Patient , Observation , Medication , Procedure , and Condition . In EUCAIM, the data heterogeneity is exposed in two aspects: semantic , such as the example discussed in the introduction (Section 1) and syntactic , such as in OMOP/FHIR. For instance, the PSA lab test is defined in OMOP as a SNOMED concept ( Prostate specific antigen measurement (63476009)) from the Measurement domain and as a LOINC concept ( Prostate specific Ag [Mass/volume] in Serum or Plasma (LP18192-2)) from the Observation resource in FHIR. Also, the Lesion concept (SNOMEDCT:52988006), which is a morphologic abnormality, is defined as Observation in OMOP and Condition in FHIR. To tackle the heterogeneity challenges, maintain semantic interoperability, and simplify the hyper-ontology development, an iterative hybrid approach is proposed, composed of bottom-up and top-down strategies and supported by ontology layering and modularization. The bottom-up strategy relies on the clinical and imaging data, associated terminologies, and their mappings to build the hierarchy and content of the domain and domain-specific layers. The core and upper layers are developed using a top-down strategy, which aims to ground the hyper-ontology in core conceptual models and foundational ontologies, supporting semantic interoperability. The integration of these strategies will maintain the hyper-ontology structure and semantic content. This study focuses on the core and upper layers.

6 https://ontouml.org/

7 https://www.ohdsi.org/data-standardization/

8 https://www.hl7.org/fhir/

## 2.2. OntoUML

As stated by Guizzardi [9], 'Semantic interoperability cannot be achieved without the support of ontologies and ontology '. While ontologies aim to capture domain conceptualization (e.g., domain ontologies), ontology represents the discipline through formal methods and theories clarifying conceptualizations (e.g., foundational ontologies). Lightweight ontology languages, such as OWL 9 , are insufficient to explicitly represent the ontological nature of a given domain, i.e., conceptualization. There is a need for a ' language truly ontological by nature ', such as OntoUML [9]. OntoUML is an Ontology-Driven Conceptual Modeling (ODCM) language whose metamodel complies with UFO, where the modeling primitives of OntoUML reflect the ontological distinctions and axiomatization of UFO [11, 5]. Two main entities are defined in UFO: endurants , which are the most dominant, and perdurants (or occurrents) . Objects are endurants that have specific properties and are classified by «kind» in UFO. Examples of objects kinds are Person , Medication , and Body structure . Subkinds are subtypes of kinds , such as Breast and Prostate . Other types of entities are defined in UFO, such as roles and phases , which represent 'contingent or accidental properties of objects' [2]. For instance, Cancer Patient is classified as «role» and Alive Person is classified as «phase». Objects can also be classified as modes , such as Disease/Disorder , which are existentially dependent on their bearers (e.g., Patient ). Besides, Qualities (e.g., size ) are objects that existentially depend on the entities they characterize (e.g., tumor ). Finally, Events , perdurants that exist only in the past [2], can be represented using the stereotype «event». Relationships between Endurants and perdurants are reciprocal, where kinds , subkinds , phases , and roles can participate in events . Also, events can create endurants . In this section, we briefly introduced selected modeling primitives from OntoUML; for more details, refer to [10, 11].

## 3. Ontology-Oriented Grounding Approach

The hyper-ontology grounding approach aims to build the core and upper layers, considering the mCODEontological conceptual model and foundational ontologies. Using OntoUML, we develop the mCODE ontological model as a reference model [12], independent from any computational language, which captures and reflects the basics of the oncology domain. Ontological unpacking process, which refers to a process of ontological analysis that reveals the ontological conceptual model , is applied as a prominent top-down approach that can effectively ensure semantic interoperability according to FAIR principles [2]. The intended model aims to capture and explicitly and unambiguously represent the basic concepts of the oncology domain and their connections. For this purpose, we refer to the mCODE guide that consists of various profiles and extensions organized into different thematic groups, including:

9 https://www.w3.org/OWL/

- Disease Characterization : includes data elements specific to the diagnosis (e.g., date, location), cancer staging, and tumor characteristics (histological classification, grade, morphology, and behavior of the tumor cell);
- Health Assessment : contains information about the patient's general health before and during treatment, such as comorbidities, performance assessment, laboratory tests, and history of metastatic cancer;
- Cancer Treatments : includes reporting of procedures (surgery and radiotherapy) and medications used to treat a cancer patient or relevant to that treatment;
- Outcomes : includes disease status, tumor, and tumor size.

Based on the hyper-ontology requirements (stated as Competency Questions (CQs) in the Ontology Requirements and Specifications Document (ORSD) [13]), we selected basic elements from different thematics to build the mCODE core conceptual model, such as Cancer Patient , Histology/Morphology , Tumor Morphology , Cancer-Related Surgical Procedure , Cancer-Related Medication Administration , Primary Cancer Condition , and Cancer Stage . These elements will be analyzed and represented using the stereotypes of OntoUML to build the core layer, and their anchoring with generic concepts will be conducted in the upper layer.

## 3.1. Core Layer

The core layer comprises different modules according to the mCODE thematic groups: Disease Characterization , Health Assessment , Cancer Treatment , and Outcomes . The modeling of each module is guided by a set of competency questions (CQs), which fulfill the main requirements of modeling the general aspects of oncology. Cancer Patient is a concept from Patient Information group 10 used in the different modules and defined as a patient diagnosed with or receiving medical treatment for a malignant growth or tumor .

Disease Characterization The main CQs for the disease characterization module are: CQ1) Howarecancer conditions classified? CQ2) Who has been diagnosed with primary cancer? CQ3) In what body location is the cancer condition identified? CQ4) Is there any histology/morphology associated with the cancer condition? CQ5) How is the cancer stage/grade specified? CQ6) Is the cancer condition classified by a certain stage/grade? CQ7) Are there any tumor marker tests for the cancer condition? CQ8) Are there any results generated by lab tests? In this module, the following elements are considered from mCODE:

- Primary Cancer Condition : captures the cancer diagnosis (original or first neoplasm in the body) and is associated with Malignant neoplastic disease (SNOMEDCT:363346000);
- Secondary Cancer Condition : captures secondary malignant neoplasms related to primary condition and is associated with Secondary malignant neoplastic disease (SNOMEDCT:128462008);
- Histology/Morphology : describes the morphologic and behavioral characteristics of cancer and conforms with, among others, Malignant neoplasm (morphologic abnormality) (SNOMEDCT:1240414004);

10 https://build.fhir.org/ig/HL7/fhir-mCODE-ig/group-patient.html, Accessed May 2, 2023

- Tumor Morphology : represents ICD-O-3 morphology determined from examination of tumor sample and is associated with Tumor morphology panel Cancer (LOINC:77753-2);
- Cancer Stage : is a parent profile for observations regarding cancer stage, grade, or classification. The stage is an assessment of the extent of cancer in the body, according to a given cancer staging classification system (e.g., TNM stage group);
- TNM Stage Group : is a specialization of Cancer Stage dedicated to AJCC TNM staging;
- Tumor Marker Test : is an observation that relates to the result of a tumor marker test (e.g., Prostate specific Ag [Mass/volume] in Serum or Plasma (LOINC:2857-1)). We differentiate between the lab tests and the values generated by these tests (e.g., Negative , Positive , or numeric values). Figure 2 depicts an example of using this profile.

Figure 2: An example of using Tumor Marker Test profile from mCODE.

[FIGURE]

Considering the definitions given in mCODE and their associations with standard ontological/terminological resources, we propose the reference model of the Disease Characterization module depicted in Figure 3. Primary Cancer Condition and Secondary Cancer Condition are cancer disease phases (original/secondary) generalized by Neoplastic Disease , an intrinsic mode inherent in the Patient and located in a certain Body Location . Cancer Patient , which is diagnosed by a Primary Cancer Condition , is a specialization of Patient . Cancer Stage , a category that classifies/characterizes a Malignant Neoplastic Disease , is specialized as TNM Stage Group and Cancer Grade categories. Histology/Morphology (e.g., Malignant neoplasm ), that 'characterizes' cancer regarding the morphologic and behavioral aspects is an intrinsic mode dependent on its bearer(s) (e.g., Malignant tumor of breast , Tumor (see Outcomes )). Thus, the morphology specification deviates from SNOMEDCT but aligns with HPO 11 and ICDO3. While neoplasms are considered as Phenotypic abnormality (HP:0000118) in HPO and Morphology in ICDO3, they are classified as Body Structure in SNOMEDCT (see Figure 1), which is a material independent entity (see Figure 8) contradicting the dependent nature of morphology. Finally, Tumor Marker Test is a lab test (e.g., PSA) that generates a Lab Test Result . Thus, we align with SNOMEDCT, which classifies lab tests as Procedure .

11 Human Phenotype Ontology, https://hpo.jax.org/app/

Figure 3: Disease Characterization module represented using OntoUML.

[FIGURE]

Health Assessment The main CQs for the health assessment module are as follows: CQ1) Are there any comorbidities the cancer patient suffers from? CQ2) Are there any related cancer conditions for these comorbidities? CQ3) How is the cancer patient's functional status assessed? CQ4) Is the history of metastatic cancer recorded? In this module, the following elements are considered from mCODE:

- Comorbidities : means co-occurring disorders that are typically treated as high-level categories (e.g., Adenoma of liver is a disease associated with Liver cell carcinoma );
- History of Metastatic Cancer : defined as the patient history of metastatic cancer;
- ECOG Performance Status : represents the patient's functional status and is used to determine their ability to tolerate therapies in serious illness, specifically for chemotherapy;

Figure 4 depicts the modeling of Health Assessment using OntoUML. Comorbidities are disorders inhering in a Cancer Patient and associated with some cancer conditions. History of Metastatic Cancer is defined as a situation aligning with SNOMEDCT that classified Family history of neoplasm (266883004) in the situation hierarchy and not the disease/disorder hierarchy (as suggested in mCODE). ECOG Performance Status is a quality describing the functional status of the Cancer Patient .

Cancer Treatment The main CQs for the cancer treatment module are: CQ1) Has the cancer patient undergone any surgical procedure? CQ2) What cancer condition does the surgical procedure treat? CQ3) What body location is affected by the surgical procedure? CQ4) Is any medication prescribed to treat the cancer condition? CQ5) How is the medication prescribed? The following elements are considered from mCODE:

Figure 4: Health Assessment module represented using OntoUML.

[FIGURE]

- Cancer-Related Surgical Procedure : designates a surgical action addressing a cancer condition and is associated with Surgical Procedure (SNOMEDCT:387713003).
- Cancer-Related Medication Administration : is an episode of medication administration for a patient diagnosed with a primary or secondary cancer condition.

Figure 5 depicts the modeling of Cancer Treatment using OntoUML. We note that radiotherapy treatment is out of this study's scope. A Cancer Patient diagnosed with Primary Cancer Condition has undergone some Cancer-Related Surgical Procedure , which surgically treats the condition located in a specific body site. Cancer-Related Medication Administration is a procedure that prescribes a Medication (substance) to treat the cancer.

Figure 5: Cancer Treatment module represented using OntoUML.

[FIGURE]

Outcomes The main CQs for the cancer treatment module are: CQ1) Who suffers from the tumor? CQ2) In which body location is the tumor identified? CQ3) Is there any cancer condition related to this tumor? CQ4) Is there any morphology associated with the tumor? CQ5) How is the size of an identified tumor recorded? In this module, three main elements are considered from mCODE:

- Tumor : identifies a tumor (body structure) that has not been removed from the body (see Figure 6 for an example);
- Tumor morphology : defines the morphology (normal and abnormal) associated with the tumor;
- Tumor size : records the dimensions of a tumor.

Figure 6: An example of using Tumor profile from mCODE.

[FIGURE]

Figure 7 depicts the modeling of Outcomes module using OntoUML. Tumor , identified in a specific body location and characterized by a Tumor Morphology , has a related condition by which a Cancer Patient is diagnosed. A Tumor is characterized by a Tumor Size , which is recorded using a specific Laboratory Procedure .

Figure 7: Outcomes module represented using OntoUML.

[FIGURE]

## 3.2. Upper Layer

The upper layer aims to define generic categories, such as Disease , Morphology , Treatment , Procedure , Body Structure , etc.), which generalize the core layer content. Anchoring the core concepts with upper-level categories is performed using OntoUML, which considers the ontological distinctions of UFO [11, 5]. For instance, Comorbidities and Neoplastic Disease are specifications

( subkinds ) of Disease , which is an intrinsic mode existentially dependent on its bearer ( Cancer Patient ); Tumor Morphology is a specific type of Histology/Morphology , which is an intrinsic mode inherent in cancer conditions; Surgical Procedure and Administration of Medication are specific types of Treatment procedure (perdurant); Body Location and Tumor are specific types ( subkinds ) of Body Structure (rigid type of endurants). Compared to BFO [6, 7], the intrinsic modes ( Histology/Morphology and Disease ) could be specified as Generically dependent continuant (BFO:0000031) and the endurants ( Patient and Body Structure ) as Independent continuant (BFO:0000004). However, using UFO and the modeling primitives of OntoUML has permitted us to ontologically analyze, clarify, and unambiguously represent concepts such as Morphology and Disease and connect them with appropriate semantic relations.

Figure 8: Excerpt of the Upper Layer represented using OntoUML.

[FIGURE]

## 4. Results

The operational version of the mCODE ontological model is generated as an OWL file [13]. The semantic integration experiment with the bottom-up version of the hyper-ontology [13] is conducted as follows. The elements defined in the mCODE ontological model are analyzed to find/match a correspondent concept/entity (i.e., addressing a similar semantic/medical context) defined in the hyper-ontology. Also, we consider the associated standard concepts recommended in mCODE (e.g., Primary Cancer Condition is associated with Malignant neoplastic disease (SNOMEDCT:363346000)). Figure 9 depicts an Excerpt of the integration results in the core layer around Disease and Morphology , which are defined as separate categories but semantically connected using Has associated morphology semantic relation. Maintaining the core layer has positively affected the domain layer (Figure 10), where cancer conditions (e.g., Carcinoma of breast ) and morphology types (e.g., Malignant epithelial neoplasm ) are classified in a coherent semantic content in contrast to SNOMEDCT and NCIT (see Figure 1).

Figure 9: An excerpt of the hyper-ontology Core Layer around Disease / Morphology (Protégé).

[FIGURE]

Figure 10: An excerpt of the hyper-ontology Domain Layer around Disease / Morphology (Protégé).

[FIGURE]

## 5. Conclusion

Considering foundational ontologies for biomedical ontologies development is a growing interest in biomedical research [8]. Various domain and domain-specific ontologies have been developed and shared in the biomedical domain to support interoperability, complying with the FAIR principles. However, conflicting/heterogeneous definitions of biomedical concepts (e.g., morphology/disease in SNOMEDCT/NCIT) make semantic interoperability challenging. Achieving semantic interoperability requires the use of ontologies as domain conceptualization (e.g., domain ontologies) and ontology as a discipline (e.g., foundational ontologies) [9]. In this study, we relied on the Unified Foundational Ontology (UFO) [11, 5] and the OntologicallyDriven Conceptual Modeling language OntoUML, which is based on the ontological distinctions of UFO, to build a core ontological model for the oncology domain considering the mCODE model [1]. The ontological distinctions of UFO have permitted, using OntoUML, to uncover and clarify the nature of real-world entities from the oncology domain (e.g., morphology/disease) and explicitly represent the ontological nature of these entities. Besides, the nature of relations between entities in the oncology domain has been identified and characterized using a variety of semantic associations. Also, we compared UFO's ontological choices at the core level regarding BFO upper-level categories. Although UFO and BFO align with the main distinctions of independent and dependent entities, UFO is richer in axiomatization, and the ontological distinctions, represented using OntoUML, permit the explicit and consistent representation of ontological choices. In further work, the main categories of hyper-ontology's upper layer will be maintained with the help of medical experts. This project is co-funded by the European Union under Grant Agreement №101100633.

## References

- [1] T. J. Osterman, M. Terry, R. S. Miller, Improving cancer data interoperability: The promise of the minimal common oncology data elements (mcode) initiative, JCO Clin Cancer Inform 4 (2020). doi: 10.1200/CCI.20.00059 .
- [2] A. Bernasconi, G. Guizzardi, O. Pastor, V. C. Storey, Semantic interoperability: ontological unpacking of a viral conceptual model, BMC Bioinformatics 23(Suppl 11) (2022). doi: 10. 1186/s12859-022-05022-0 .
- [3] H. Kondylakis, et al., Data infrastructures for ai in medical imaging: a report on the experiences of five eu projects, European Radiology Experimental 7 (2023). doi: 10.1186/ s41747-023-00336-x .
- [4] G. Guizzardi, G. Wagner, J. P. A. Almeida, R. Guizzardi, Towards ontological foundations for conceptual modeling: The unified foundational ontology (ufo) story, Appl. Ontology 10 (2015) 259-271. doi: 10.3233/AO-150157 .
- [5] G. Guizzardi, A. B. Benevides, C. M. Fonseca, J. ao Paulo A. Almeida, T. P. Sales, D. Porello, Ufo: Unified foundational ontology, Appl. Ontology 17 (2022) 167-210. doi: 10.3233/ ao-210256 .
- [6] B. Smith, A. Kumar, T. Bittner, Basic Formal Ontology for Bioinformatics, IFOMIS Reports, 2005.
- [7] R. Arp, B. Smith, A. D. Spear, Building ontologies with Basic Formal Ontology, Cambridge, MA:MIT Press, 2015.
- [8] C. H. Bernabé, N. Queralt-Rosinach, V. E. S. Souza, L. O. B. da Silva Santos, B. Mons, A. Jacobsen, M. Roos, The use of foundational ontologies in biomedical research, J Biomed Semant 14 (2023). doi: 10.1186/s13326-023-00300-z .
- [9] G. Guizzardi, Ontology, ontologies and the 'i'' of fair, Data Intelligence 2 (2020) 181-191. doi: 10.1162/dint\_a\_00040 .
- [10] G. Guizzardi, T. P. Sales, C. M. Fonseca, D. Porello, J. P. Almeida, N. Guarino, Endurant types in ontology-driven conceptual modeling: Towards ontouml 2, in: Conceptual Modeling - 37th International Conference, {ER} 2018, Xi'an, China, October 22-25, Proceedings, Springer, 2018, pp. 136-150.
- [11] G. Guizzardi, Ontological Foundations for Structural Conceptual Models, CTIT, Centre for Telematics and Information Technology, Twente, Netherlands, 2005.
- [12] R. de Almeida Falbo, Sabio: Systematic approach for building ontologies, in: ONTO.COM/ODISE@FOIS 2014, 2014.
- [13] LIMICS, Eucaim's hyperontology v0.2beta, 2024. Https://doi.org/10.5281/zenodo.11109765.
