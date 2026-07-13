## Towards Semantic Interoperability among Heterogeneous Cancer Data Models using a Layered Modular Hyper-Ontology

Mirna EL GHOSH a , 1 , Varvara KALOKYRI b , Melanie SAMBRES a , Morgan VATERKOWSKI a , Catherine DUCLOS c , Xavier TANNIER a , Gianna TSAKOU d , Manolis TSIKNAKIS b , Christel DANIEL a and Ferdinand DHOMBRES a

a Sorbonne Universit´ e, Inserm, Universit´ e Sorbonne Paris-Nord, LIMICS, Paris, France b Institute of Computer Science, Foundation of Research and Technology Hellas, Heraklion, Greece

c Universit´ e Sorbonne Paris-Nord, Inserm, Sorbonne Universit´ e, LIMICS, Paris, France d MAGGIOLI S.P.A., Research and Development Lab, Marousi, Greece

Abstract. Semantic interoperability is a growing and challenging subject in the healthcare domain. It aims to ensure a coherent and unambiguous exchange, use, and reuse of health information among different systems and applications. In the context of the EUCAIM (Cancer Image Europe) project, semantic interoperability among various heterogeneous cancer image data models is required to support the communication, integration, and sharing of data in a standardized and structured way. For this purpose, hyper-ontology is developed as a common semantic metamodel that bridges the disparate imaging and clinical knowledge of the various repositories in EUCAIM and supports their integration. EUCAIM's hyper-ontology is also an application-based ontology targeted for federated semantic querying and image annotation. To facilitate the hyper-ontology building process and ensure the extensibility of the ontology model, an iterative hybrid well-founded approach that divides the ontology structure into layers and modules is established.

Keywords. Semantic Interoperability, Biomedical ontologies, Hyper-Ontology, Cancer image data, Heterogeneous data standards, Common Data Models

## 1. Introduction

'Rectal cancer', 'Cancer of rectum', and 'Rectal carcinoma' refer to the cancer type 'Malignant tumor of rectum'. 'Colorectal cancer' and 'CRC' are alternative labels for the disorder 'Malignant neoplasm of colon and/or rectum'. In healthcare, medical terms describing the same cases (e.g., disorders) may have different labels, including synonyms and acronyms. Interoperable health data representations would ideally bridge syntactically different but semantically equivalent expressions in different degrees of structure [2]. Additionally, information models (or Common Data Models) in healthcare are a way to standardize data storage (OHDSI-OMOP 2 ) or data exchange (HL7-FHIR 3 ), but they don't have a shared conceptualization; thus, they create new divergences between identical concepts. For instance, PSA (Prostate Specific Antigen) lab test is viewed as a Measurement in OMOP and an Observation in FHIR. In this context, semantic interoperability supports medical systems in interpreting the shared meaning of medical terms unambiguously to avoid misunderstandings when describing the same cases using disparate terms/standards. Standardized terminologies and ontologies, agreed at the international level (e.g., SNOMED-CT 4 , LOINC 5 ), and aligned basically with the FAIR principles [1], support interoperability in healthcare, where each medical term is linked to a shared and controlled vocabulary. However, applying semantic interoperability is challenging due to the large amount of data and the diversity of terminologies/standards.

1 Corresponding Author: Mirna El Ghosh, mirna.el-ghosh@inserm.fr

This study is part of the EUCAIM project 6 , a joint effort by the AI for Health Imaging (AI4HI) network [10,11] and major European Research Infrastructures to build up a hybrid (distributed and centralized) infrastructure integrating major existing European Real World Data infrastructures on cancer images, including many types of cancer. EUCAIM aims to integrate and federate large volumes of cancer image data by establishing semantic interoperability among the diverse data provided by the AI4HI network and future data providers. In EUCAIM, clinical and biological data/metadata associated with images are standardized and structured using FHIR and OMOP. For imaging knowledge, the DICOM standard 7 is commonly used to represent image segmentation and studies. Facing this diversity, a common semantic meta-model is required for semantic interoperability among the repositories [10].

Although using/developing ontologies is a vital strategy for enhancing the interoperability of heterogeneous datasets [4], their integration becomes significantly more challenging when annotating with various ontological or terminological references [3,4]. In EUCAIM, we develop a hyper-ontology to ensure and maintain semantic interoperability among multiple independently developed systems used for collecting and describing cancer image data. The hyper-ontology will help, on the semantic level, organize and group common data representations under a common meta-model so that disparate and heterogeneous clinical and imaging data models can easily and unambiguously communicate and interoperate. Also, the meaning of essential medical data is preserved and exchanged in a standardized, consistent, and meaningful way. Therefore, the main challenge of hyper-ontology is to facilitate integration and interoperability among data stored and modeled using diverse clinical and imaging data models and associated terminologies. Hyper-ontology is also an application ontology that permits the exploration of data collections, federated querying, and image annotation. A hybrid approach is proposed to facilitate the hyper-ontology development and ensure its extensibility. Section 2 overviews EUCAIM data models. Sections 3 and 4 present the development process and results, respectively. Section 5 outlines the evaluation and validation. Finally, sections 6 and 7 discuss the related work and conclude the paper.

2 https://www.ohdsi.org/data-standardization/

3 https://www.hl7.org/fhir/

4 https://www.snomed.org/

5 https://loinc.org/

6 https://cancerimage.eu/

7 https://www.dicomstandard.org/

## 2. Cancer Image Data Models in EUCAIM

In EUCAIM, clinical and imaging data types are considered. All AI4HI projects (CHAIMELEON, ProCAncer-I, EuCanImage, INCISIVE, and PRIMAGE) adopt a common data model (CDM) (e.g., OMOP, FHIR) for the clinical data where standardized vocabularies (e.g., SNOMED-CT, LOINC) are used for harmonizing the data to be stored in the CDM [11]. Using CDM facilitates standardization, ensuring all data nodes adhere to the same structure and represent their information using standardized terminologies. In EUCAIM, OMOP and FHIR are used based on the AI4HI network [10]. For the OMOPapproach, oncology extension [13] and imaging extension [14,15,16] are applied in CHAIMELEON and ProCAncer-I. Additionally, the DICOM standard for medical imaging is adopted to represent disparate types of imaging data, including information about imaging studies or image annotations/segmentations. Despite the commonalities, data models/standards and data minimization suffer from diversity [11].

1. Data models and standards: in the AI4HI network, data models and standards are diverse for representing clinical and imaging knowledge.
- Clinical data: suffers from significant disparity where various data models and ontologies coexist, and the projects combine, among many others, SNOMEDCT with OMOP or FHIR CDMs. Also, multiple terminologies and ontologies are used to standardize and homogenize various fields. For instance, ProCAncer-I and CHAIMELEON both provide clinical data for prostate cancer and adopt OMOP as CDM. However, they differ in choosing terminologies or concepts to standardize the same fields (see Table 1).
- Imaging data: the DICOM standard is commonly used, but in the ProCAncer-I project, RadLex [12], is also used to standardize and homogenize some imaging metadata (e.g., Modality , Laterality , Anatomic Region ).
2. Data minimization: also suffers from variability as each project defines its required clinical/imaging variables differently. There is no standard or consensus on the amount and granularity of data required [11].
- Clinical data: there is a diversity in specifying clinical variables among projects addressing the same cancer type. For instance, INCISIVE and EuCanImage both have clinical data for breast cancer and adopt FHIR as CDM. However, they differ regarding the amount/type of required data (see Table 1).
- Imaging data: although the projects commonly adopt the DICOM standard and rely on its representation for imaging knowledge, imaging metadata deemed useful for extracting and being used differs. For instance, CHAIMELEON focuses on extracting imaging metadata from imaging studies (e.g., image modality , body part examined ). In contrast, ProCAncer-I and INCISIVE, apart from the imaging studies, also focus on metadata of image segmentations (e.g., segment label , annotated region ).

The variability and diversity in data models/standards and data minimization on the clinical and imaging levels show that a common semantic meta-model is required to maintain semantic interoperability and enable seamless integration and communication among disparate data models.

Table 1. Examples of diversity of terminologies/standards and required data

| Field             | Project     | Terminology     | Standard terms                              |
|-------------------|-------------|-----------------|---------------------------------------------|
| Therapy           | ProCAncer-I | SNOMED-CT       | Intensity modulated radiation therapy       |
| Therapy           | CHAIMELEON  | ICD10PCS        | Beam Radiation of Prostate                  |
| Cancer Staging    | ProCAncer-I | Cancer Modifier | AJCC/UICC 7th pathological M1a Category     |
| Cancer Staging    | CHAIMELEON  | NAACCR          | pM1a                                        |
| Diagnosis         | INCISIVE    | SNOMED-CT       | Malignant neoplasm of breast                |
| Diagnosis         | EuCanImage  | SNOMED-CT       | Primary malignant neoplasm of female breast |
| Medical procedure | INCISIVE    | SNOMED-CT       | Chemotherapy                                |
| Medical procedure | EuCanImage  | SNOMED-CT       | Chemotherapy cycle                          |
| Medication        | INCISIVE    | -               | -                                           |
| Medication        | EuCanImage  | RxNorm          | Capecitabine                                |
| Follow- up        | INCISIVE    | SNOMED-CT       | Treatment changed                           |
| Follow- up        | EuCanImage  | -               | -                                           |

## 3. Hyper-Ontology Development Process

EUCAIM's hyper-ontology is a semantic meta-model that aims to integrate heterogeneous and complex imaging and clinical/biological knowledge represented using various standards. Inspired by the Neon methodology [5], and SABiO [7], we propose a hybrid systematic formally and semantically well-founded approach (Figure 1) to develop the hyper-ontology.

Figure 1. An illustration of the hyper-ontology development process

[FIGURE]

- 1Requirements Analysis and Specifications states why the ontology is being built, its intended uses, who the end users are, and which requirements the ontology should fulfill [6]. After a set of meetings with users and experts from the EUCAIM community, we define the following:
- Purpose : EUCAIM's hyper-ontology aims to maintain and support semantic interoperability among diverse cancer image data models by providing the ontology-

based standard and structured vocabulary that integrates and combines these data models in a common meta-model. The hyper-ontology will permit applications to exchange queries and provide the semantic labels required for annotating cancer images. Besides, the integration with the OMOP and FHIR CDMs of the AI4HI network should be ensured, permitting consistent mapping with local nodes to seamlessly explore data collections through the Public Catalogue 8 .

- Scope : the hyper-ontology covers the oncology domain, mainly cancer imaging data provided by the AI4HI network, including, among many others, the following cancer types: prostate, breast, rectum, lung, colon, colorectal, and liver.
- Intended uses and users : the hyper-ontology will support exploring the data collections through the Public Catalogue, Federated Querying (federated search of aggregated data in the collections), and semantic annotation of cancer images. Data users or researchers can use the hyper-ontology to explore or use data in research. We give an example of a simple query that uses terms from the hyper-ontology and will return information from the diverse data collections: 'age at diagnosis' ≥ 50 &amp; 'diagnosis' = 'prostate cancer' &amp; 'modality' = 'MR' .
- Requirements : non-functional (NFRs) and functional (FRs) are defined.
1. NFRs : such as NFR1- to support English; NFR2- the terminology to be used must be taken from validated biomedical ontologies and standardized terminologies; NFR3- the ontology model should be extensible to include future ontological aspects and new cancer types; NFR4- to support the FAIR principles; NFR5- to comply with the GDPR 9 .
2. FRs : defined as quality requirements that describe the goals for modeling [8] and are stated as Competency Questions (CQs). Examples of FRs that the hyper-ontology should fulfill:
* FR1- to define the different cancer types (e.g., Breast cancer , Prostate cancer ), subtypes (e.g., Primary malignant neoplasm of breast with axillary lymph node invasion , Hormone sensitive prostate cancer ), and their associated morphology (e.g., Malignant neoplasm , Neoplasm, metastatic );
* FR2- to define the different body parts related to the identified cancer type/subtypes (e.g., Breast , Axillary lymph node structure , Prostate );
* FR3- to define the diagnostic and therapeutic procedures, medication, and treatments used throughout and after the diagnosis or treatment of the different cancer types/subtypes (e.g., Chemotherapy , Combined chemotherapy and radiation therapy , Androgen deprivation therapy , Surgical procedure );
* FR4- to define the imaging modalities, procedures, and results (e.g., MRI , MRI of breast for screening for malignant neoplasm , MRI scan abnormal );
* FR5- to include the semantic labels and qualifier values required for image annotation and segmentation (e.g., Malignant , Benign , Automatic , Manual ).
* FR6- to define the semantic relations among the different entities, such as medication treats disorder, patient has undergone surgical procedure, etc.
* FR7- to ensure the correspondence of the concepts to their domains/resources in OMOP and FHIR CDMs. For instance, Primary malignant neoplasm

8 https://catalogue.eucaim.cancerimage.eu/

9 https://commission.europa.eu/law/law-topic/data-protection/data-protection-eu en

of breast and Chemotherapy have Condition and Procedure as FHIR resourceType and OMOP domain , respectively.

* FR8- to represent specific concepts by combining atomic-related concepts, which aims to solve the disparity problem of provided data. For instance, the cancer staging metastasis value of M1 from TNM (Tumor-node-metastasis) category could be represented in two different ways: 1) AJCC/UICC 7th pathological M1a Category (Table 1, Cancer Staging /ProCAncer-I), which is a concept of the Measurement OMOP domain; 2) TNM Path M , a concept of the Measurement domain with value pM1a (Table 1, Cancer Staging /CHAIMELEON) of the Meas Value domain.

Following [5,6], the specifications and requirements are documented in the Ontology Requirements and Specifications Document (ORSD). Examples of knowledgebased CQs classified by cancer types are identified in the ORSD [30]. ORSD will have a key role during the hyper-ontology development process because it facilitates (1) the search and reuse of existing data resources, (2) the search and reuse of terminological/ontological resources, and (3) the verification and evaluation of the hyper-ontology.

2Knowledge Acquisition aims to collect and organize the knowledge the different projects provide.

1. Collecting mandatory/required clinical and imaging knowledge : provided as use cases defined per cancer type. Facing the diversity of knowledge discussed in Section 2, all the acquired knowledge is presented and organized in the ORSD using a set of Competency Questions. For clinical knowledge (following OMOP/FHIR), the standardized terms, their source terminologies/ontologies, and codes are collected. For imaging knowledge, we collect the values associated with DICOM tags and the standardized terms, if available.
2. Reusing and merging ontological resources : (scenario defined in Neon methodology [5]) includes establishing semantic and syntactic alignments and mappings to the acquired terms and their ontological resources. Two main mapping strategies are followed (see Figure 2):
- Label-based : aligns the collected OMOP and FHIR standard concepts and DICOMimaging values/labels to existent validated terminological/ontological resources (e.g., SNOMED-CT, LOINC, NCIT, RadLex, ICDO-3) by applying an exact match similarity approach. This strategy will enrich the hyper-ontology with synonyms, codes, and definitions.
- Hierarchical-based : extracts the taxonomies ( is-a ) of the OMOP and FHIR standard concepts and DICOM imaging values/labels from the standard terminologies/ontologies and aligns and merges them to construct the hierarchical structure of the hyper-ontology.

The mappings are performed automatically using the following resources that combine many health and biomedical vocabularies and standards to enable interoperability between computer systems:

- OHDSI ATHENA 10 : permits harvesting diverse mappings ( exact search and is-a ) from various standardized vocabularies.

10 https://github.com/OHDSI/Athena

## March 2024

Figure 2. An illustration of label-based and hierarchical-based mappings

[FIGURE]

- UMLS (Unified Medical Language System) REST API 11 [18]: provides various endpoints to search and retrieve UMLS content (e.g., atoms, CUIs (Concept Unique Identifiers), definitions, semantic types, parents, children, etc.).
- BioPortal RESTful API 12 : comprises different resources (Ontologies, Classes) and related endpoints to access and browse biomedical contents. BioPortal helps enrich the hyper-ontology with synonyms, codes, and definitions and access the resources not considered in UMLS/ATHENA (e.g., RadLex, NCIT).
3. Intervention of experts : to specify application-related knowledge required in the hyper-ontology (e.g., query criteria), preferences in terminologies/ontologies (e.g., RadLex[12] for imaging), and to supervise mappings curation.
- 3Design and Conceptualization aims to design and structure the domain knowledge in a conceptual model that describes the problem and its solution regarding the domain vocabulary and mappings identified and harvested in the previous phases. To simplify this activity, we apply ontology layering and modularization as support processes:
- Layering : divides the ontology structure into four layers located at different granularity levels, from bottom to top:
* Domain-Specific Layer ( DSL ): includes the domain-specific concepts defined/used in the cancer imaging domain such as Prostate cancer , Prostate gland , pM1a , Malignant , and MRI guided biopsy of prostate . These concepts

11 https://documentation.uts.nlm.nih.gov/rest/home.html

12 https://data.bioportal.lirmm.fr/documentation

are specified based on the clinical and imaging provided knowledge and their mappings. DSL reflects the granularity level of the hyper-ontology.

* Domain Layer ( DL ): defines the domain concepts of the application domain such as Neoplasm of trunk , MRI of prostate . These concepts are specified and connected to DSL using a bottom-up approach considering the is-a mappings obtained in the knowledge acquisition phase.
* Core Layer ( CL ): includes the core concepts of the oncology domain reused from conceptual or ontological resources (e.g., Minimal Common Oncology Data Elements (mCODE) 13 [19]), aiming to ground the hyper-ontology in oncology. For instance, Cancer Patient , Primary Cancer Condition , Histology/Morphology , Cancer-Related Surgical Procedure , Tumor Marker Test , and Cancer Stage are generic entities defined in the conceptual model of mCODE. They must be represented in a core ontological conceptual model that reflects the main ontological semantics of the oncology domain. In this regard, applying an ontological unpacking process, which refers to a process of ontological analysis that reveals the ontological conceptual model , is a prominent top-down approach that can effectively ensure the semantic interoperability according to FAIR principles [20].
* Upper Layer ( UL ): anchors CL concepts to generic concepts (e.g., Person , Disease , Procedure , Assessment , Treatment , Situation , etc.). The grounding (CL) and anchoring (UL) processes require using foundational ontologies (e.g., UFO [23,24], BFO [22]) as semantic bridges between domain/core concepts, improving the semantic understanding of terms and supporting the mappings of concepts and interoperability [9].
- Modularization splits the ontology content into generic modules, facilitating the building process and supporting the hyper-ontology extensibility. Three main ontology modules are considered:
* Clinical OM : includes the clinical and biological knowledge such as cancer types and subtypes, their associated morphology/histology, body parts, family history, medical treatment, surgical/therapeutic procedures, staging/grading systems/methods, specimen, tumor markers, and other laboratory tests/results.
* Imaging OM : defines the imaging knowledge such as modalities, procedures, assessment, and findings, which are also provided as clinical knowledge supporting cancer imaging (see section 2).
* Common OM : includes age at diagnosis , sex assigned at birth , gender , and qualifier values required for image annotation/segmentation (e.g., benign , malignant , automatic , manual ), tumor staging/grading (e.g., pT0 , pM1 , cM2 ), or lab test results, such as absence/presence findings (e.g., positive , negative ).

Figure 3 depicts an example of the hyper-ontology structure with examples of concepts selected from the different layers and modules. An additional ontology module, Correspondence OM , is envisaged to permit a syntactic integration with OMOP/FHIR by explicitly specifying the correspondences of concepts with OMOP domain and FHIR resourceType .

13 https://build.fhir.org/ig/HL7/fhir-mCODE-ig/

March 2024

Figure 3. An excerpt of the hyper-ontology structure

[FIGURE]

Finally, semantic patterns are captured within the collected data to enrich the ontology model semantically. For instance, body locations are linked to cancers (e.g., Prostate cancer SNOMED:Has finding site some Prostate ) and imaging procedures (e.g., MRI of breast SNOMED:Has direct procedure site some Breast ).

- 4Formalization This activity generates a machine-readable and reusable formal version of the hyper-ontology supporting the FAIR principles.
- 5Evaluation and Validation The hyper-ontology needs to be evaluated with the help of clinical experts regarding the specified requirements. Also, assessing the integrity and performance of the hyper-ontology in achieving pertinent results in specific tasks of querying and segmentation is required. Besides, automatic methods are used to evaluate the hyper-ontology semantic content (see Section 5).
- 6Maintenance Based on the feedback from the evaluation and validation phases, the hyper-ontology will be revised to correct or enhance the ontological semantic/syntactic content.

## 4. Results

This study takes into consideration 9 use cases of cancer of the prostate, breast, colon, liver, and rectum, provided by four different projects (ProCAncer-I, CHAIMELEON, INCISIVE, and EuCanImage). The clinical/biological and imaging knowledge provided by the projects is organized in the ORSD per cancer type using a set of competency questions ( N = 170). OMOP standard concepts ( N = 305) for prostate cancer are collected from ProCAncer-I and CHAIMELEON and distributed to the following domains: Condition, Measurement, Unit, Procedure, Regimen, Drug, Observation, Spec Anatomic Site, and Meas Value. FHIR standard concepts ( N = 380) for breast, liver, and rectum cancers are collected from EuCanImage and INCISIVE (breast can- cer) and distributed to the following resource types: Observation, Medication, Condition, and Diagnostic Report. The standard vocabularies/ontologies commonly adopted in these projects are SNOMEDCT, Cancer Modifier, LOINC, ICDO3, RxNorm, GENDER, CPT4, NAACCR, ATC, ICD10PCS, HemOnc, and UCUM. The first beta version of the hyper-ontology (V0.1 beta - March 2024) [30] defines: 1504 concepts (including 1076 SNOMEDCT, 158 Cancer Modifier, 80 LOINC, 59 NAACCR, 31 ICDO3, 18 RadLex), 2701 is-a mappings, 875 exactMatch mappings (262 UMLS, 124 RadLex, 321 NCIT, 135 SNOMEDCT, and 27 NAACCR), 2025 synonyms, 210 definitions, and 645/194 syntactic alignments to OMOP/FHIR. We discuss some results of the bottom-up approach in what follows.

- Clinical module: defines a hierarchy of cancer types, histology/morphology, body part, cancer stage/grade, tumor marker test, medication, diagnostic and therapeutic procedures, specimen, and clinical findings, fulfilling FR1, FR2, and FR3;
- Imaging module: includes provided clinical knowledge supporting the imaging (e.g., procedures, modalities, and findings) and imaging metadata collected from imaging studies (e.g., imaging modality , laterality ), fulfilling FR4;
- Common module: includes gender, age at diagnosis, and qualifier values, such as disease qualifiers, units of measure, time patterns, absence/presence findings, and segmentation/annotation values, fulfilling FR5.

Different semantic relations are specified in this version to fulfill FR6, such as Treats that links medication to cancers, Has Answer that relates staging categories to staging values (a TNM staging example in Figure 5), and Unit for that defines the unit measures for measurements (a PSA example in Figure 4). FR7 is fulfilled by establishing syntactic alignment to OMOP (e.g., domain id) and FHIR (e.g., resourceType) using semantic annotations and Has correspondence relation (see Figure 4). For FR8, Figure 5 shows an example of representing the specific concept AJCC/UICC 7th pathological M1a Category (Cancer Modifier) in the form of atomic concepts, TNM Path M (NAACCR:900) and pM1a (NAACCR:900@p1A) using the owl:equivalentClass property. Finally, the integration of standard OMOP and FHIR concepts is ensured in the hyper-ontology by using common categories to maintain semantic interoperability. We give examples of abstracting standard concepts from OMOP and FHIR CDMs:

- Medication standard concepts (e.g., Capecitabine (RxNorm:194000)) having Drug as OMOP domain and Medication as FHIR resourceType are commonly specified as Medication (NCIT:C459). Cancer-Related Medication Administration mCODE core concept is envisaged to ground the medication in oncology.
- Laboratory test concepts (e.g., PSA (SNOMEDCT:63476009)) having Measurement OMOP domain and Observation FHIR resource are specified as Measurement (SNOMEDCT:122869004, NCIT:C25209). Tumor Marker Test core concept will be reused from mCODE to ground lab tests in oncology.
- Cancer staging values (e.g., pM1a (NAACCR:900@p1A)), which are Meas value in OMOP and Observation in FHIR, are specified as qualifier finding values (SNOMEDCT:260245000). Cancer Stage and TNM Stage Group mCODE core concepts will be potentially reused to classify the staging categories and values for a semantically coherent oncology context.

## March 2024

Figure 4. An excerpt of the hyper-ontology around PSA fulfilling FR6 and FR7

[FIGURE]

Figure 5. An example of representing specific concepts (TNM staging) fulfilling FR8

[FIGURE]

## 5. Evaluation and Validation

The hyper-ontology is validated as an RDF/OWL formal ontology [30], and its consistency is verified using Hermit 14 , an OWL2 inference engine. Medical and ontological experts from EUCAIM's community will assess the hyper-ontology semantic content regarding the specified requirements. Moreover, the hyper-ontology will be evaluated according to its performance in data collection exploration through the Public Catalog 15 , federated querying and processing, and cancer image segmentation/annotation tasks. Automatically, we tested two methods:

1. generic competency questions (CQs) are translated to SPARQL queries to interrogate the hyper-ontology content regarding the answers given in the ORSD. For instance, (CQ1) What are the main types and subtypes of breast cancer (CLIN1000060)? (CQ2) What body sites are affected by breast cancer ?
2. similarity computation is performed among randomly selected concepts from the hyper-ontology (see Table 2) to verify the correctness of the semantic content. We assessed the similarity degree ([0..1]) by computing the specificity

```
PREFIX ho: <https://cancerimage.eu/ontology/EUCAIM#> Q1: SELECT ?p WHERE { ?p rdfs:subClassOf* ho:CLIN1000060. Q2: SELECT ?p WHERE { ho:CLIN1000060 rdfs:subClassOf [ a owl:Restriction ; owl:onProperty ho:HasFindingSite ; owl:someValuesFrom ?p ].
```

14 http://www.hermit-reasoner.com/

15 https://catalogue.eucaim.cancerimage.eu

Table 2. Similarity values among selected terms from the hyper-ontology

| Concept#1     | Concept#2          |   Sim | Concept#1          | Concept#2          |   Sim |
|---------------|--------------------|-------|--------------------|--------------------|-------|
| Chemotherapy  | Drug therapy       |  0.83 | Chemotherapy       | Abdomen excision   |  0.49 |
| Chemotherapy  | Hormone therapy    |  0.92 | PSA                | Hormone therapy    |  0.49 |
| Prostatectomy | Surgical procedure |  0.52 | Prostatectomy      | Breast cancer      |   0.2 |
| PSA           | Measurement        |   0.7 | Surgical procedure | Breast cancer      |  0.21 |
| Breast cancer | Neoplasm of breast |  0.68 | Measurement        | Neoplasm of breast |  0.22 |
| Prostatectomy | Abdomen excision   |  0.95 | Drug therapy       | Abdomen excision   |  0.51 |

of concepts in the ontology graph, such as the number of leaves and subsumers [25]. We noticed that similarity results positively correlate with the semantic content of the hyper-ontology, reflecting its applicability. For instance, the concepts having elevated similarity scores (e.g., 0 . 83, 0 . 92) share a semantic context, such as subClassOf (e.g., Chemotherapy / Drug therapy )), ascendants/descendants (e.g., PSA / Measurement ), or siblings (e.g., Chemotherapy / Hormone therapy ), in contrast to concepts having low degrees (e.g., Prostatectomy / Breast cancer ), which are specified in completely different semantic context (Surgical procedure/Disease).

## 6. Related Work

Various ontologies have been proposed to support semantic interoperability in healthcare, such as, among others, Operational Ontology for Oncology (O3) [26,27] (previously OORO) and AIDAVA 16 Reference Ontology (RO) [28,29]. While O3 is an expertcentered ontology relying on medical experts' and stakeholders' intervention and expertise, RO and hyper-ontology consider health records extracted from heterogeneous data sources in a knowledge-centered approach. Nevertheless, expert intervention is considered in RO and hyper-ontology not only to evaluate the ontology model from the medical and semantic aspects but also to collaborate on some significant decisions regarding the requirements, the selection of terminologies/ontologies, and the curation of mappings. Table 3 presents the main specifications and strategies for building O3 and RO compared to the hyper-ontology.

## 7. Conclusion

This study discussed the development process of EUCAIM's hyper-ontology to semantically bridge multiple independently developed systems used for collecting and describing cancer image data. Facing the diversity of healthcare standards (OMOP/FHIR) and the complexity and disparity of imaging and clinical/biological knowledge and associated terminologies, a hybrid systematic and well-founded approach, supported by ontology grounding, layering, and modularization processes, is proposed to simplify the building process. We demonstrated that the hyper-ontology supports semantic interoperability by providing a common terminology and set of concepts that can represent and integrate data from OMOP and FHIR, allowing users to formulate queries without needing to know the specifics of each underlying model. EUCAIM's hyper-ontology has also fulfilled specific requirements to resolve knowledge complexity. Semantic mappings with standardized vocabularies/ontologies and healthcare standards have ensured the reusability and compliance of hyper-ontology with FAIR principles. In further work, we will revise the ontology content based on the experts' feedback and organize meetings with oncology/radiology experts to enrich the hyper-ontology with additional semantic patterns to resolve the disparity of knowledge. Furthermore, we will extend the ontology model iteratively with new use cases provided by the AI4HI projects, for which related CQs will be specified in the ORSD. The top-down approach will also be finalized to support the mapping of concepts and semantic interoperability. Finally, we will address significant challenges, such as extending the hyper-ontology with new cancer types and the evolution and sustainability of the hyper-ontology, mainly after the project completion. This project is co-funded by the European Union under Grant Agreement № 101100633.

16 https://aidava.eu/

Table 3. A comparison of specifications and strategies for developing O3 and RO, and the hyper-ontology

| Ontology        | Scope                                                              | Approach                                                                                                               | Strategy                               | Content                                                                                                                                                                                                                                        | Alignment/Integration                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O3              | Prostate, breast, and head and neck cancers                        | Iterative- deliberations approach                                                                                      | Top-down                               | Common concepts for all cancer types, including imaging, pathol- ogy, medical oncology, surgery, and radiation treatment                                                                                                                       | SNOMEDCT, NCIT, mCODE, CodeX 17                                                                                                                                                                                  |
| RO              | Breast cancer registry and Cardiovascular Diseases score           | Minimum set of requirements                                                                                            | Bottom-up                              | covers Observation, Condition, Procedure, Medication, Diagnos- tic Report (based on HL7 FHIR IPS profiles)                                                                                                                                     | SNOMEDCT, LOINC, and HL7 FHIR ontological compo- nents                                                                                                                                                           |
| Hyper- Ontology | Cancer of prostate, breast, rectum, lung, colon, liver, colorectal | Hybrid iterative formally and semantically well-founded approach sup- ported by ontol- ogy layering and modularization | Integration of bottom-up and top- down | Common concepts for all cancer types, including his- tology/morphology, stag- ing/Grading, surgical, diagnostic and therapeutic procedures, tumor marker test, medication, imaging procedures, body parts, time patterns, and units of measure | SNOMEDCT, NCIT, RadLex, ICDO3, ICD10, LOINC, NAACCR, etc. ( exactMatch and is-a mappings), mCODE (grounding in oncology), BFO/UFO (grounding in foundational ontologies), and syntactic alignment with OMOP/FHIR |

## References

- [1] Wilkinson MD, Dumontier M, Aalbersberg I, et al.. The FAIR Guiding Principles for scientific data management and stewardship. Sci Data 2016;3:160018
- [2] Schulz, S et al. Towards Principles of Ontology-Based Annotation of Clinical Narratives. International Conference on Biomedical Ontology (2023).
- [3] Oliveira D, Pesquita C. Improving the interoperability of biomedical ontologies with compound alignments. J Biomed Semant 9, 1 (2018). doi: 10.1186/s13326-017-0171-8
- [4] Smith B, Arabandi S, Brochhausen M, Calhoun M, Ciccarese P, Doyle S, Gibaud B, Goldberg I, Kahn CE, Overton J, Tomaszewski J, Gurcan M. Biomedical imaging ontologies: A survey and proposal for future work, Journal of Pathology Informatics, Volume 6, Issue 1, 2015, 37, ISSN 2153-3539. doi: 10.4103/2153-3539.159214.
- [5] Su´ arez-Figueroa MC, G´ omez-P´ erez A, Fern´ andez-L´ opez M. The NeOn Methodology for Ontology Engineering. In: Su´ arez-Figueroa M, G´ omez-P´ erez A, Motta E, Gangemi A, editors. Ontology Engineering in a Networked World. 2012. Springer, Berlin, Heidelberg. doi: 10.1007/978-3-642-24794-1 2
- [6] Su´ arez-Figueroa MC, G´ omez-P´ erez A. Ontology Requirements Specification. In: Su´ arez-Figueroa M, G´ omez-P´ erez A, Motta E, Gangemi A, editors. Ontology Engineering in a Networked World. 2012. Springer, Berlin, Heidelberg. p. 93-106, doi: 10.1007/978-3-642-24794-1 5
- [7] Falbo R. SABiO: Systematic Approach for Building Ontologies. ONTO.COM/ODISE@FOIS. 2014.
- [8] Guizzardi G, Proper HA. On Understanding the Value of Domain Modeling. Proceedings of 15th International Workshop on Value Modelling and Business Ontologies (VMBO 2021); 2021.

- [9] Bernab´ e CH, Queralt-Rosinach N, Silva Souza VE et al. The use of foundational ontologies in biomedical research. J Biomed Semant 14, 21 (2023). doi: 10.1186/s13326-023-00300-z
- [10] Kondylakis H, Kalokyri V, Sfakianakis S, Marias K, Tsiknakis M, Jimenez-Pastor A, et al.Data infrastructures for AI in medical imaging: a report on the experiences of five EU projects. Eur Radiol Exp. 2023 May 8;7(1):20. doi: 10.1186/s41747-023-00336-x. PMID: 37150779; PMCID: PMC10164664.
- [11] Kondylakis, H., Ciarrocchi, E., Cerda-Alberich, L. et al. Position of the AI for Health Imaging (AI4HI) network on metadata models for imaging biobanks. Eur Radiol Exp 6, 29 (2022). doi: 10.1186/s41747022-00281-1
- [12] Chepelev LL, Kwan D, Kahn CE, Filice RW, Wang KC. Ontologies in the New Computational Age of Radiology: RadLex for Semantics and Interoperability in Imaging Workflows. Radiographics. 2023 Mar;43(3):e220098. doi: 10.1148/rg.220098. PMID: 36757882.
- [13] Belenkaya R, Gurley MJ, Golozar A, et al.: Extending the OMOP common data model and standardized vocabularies to support observational cancer research. JCO Clin Cancer Inform 5:12-20, 2021. doi:10.1200/CCI.20.00079
- [14] Kalokyri V, et al. MI-Common Data Model: Extending Observational Medical Outcomes PartnershipCommon Data Model (OMOP-CDM) for Registering Medical Imaging Metadata and Subsequent Curation Processes. JCO Clin Cancer Inform. 2023 Sep;7:e2300101. doi: 10.1200/CCI.23.00101. PMID: 38061012; PMCID: PMC10715775.
- [15] Park C, et al. Development and Validation of the Radiology Common Data Model (R-CDM) for the International Standardization of Medical Imaging Data. Yonsei Med J 63, S74 (2022).
- [16] Park WY, Jeon K, Schmidt TS et al. Development of Medical Imaging Data Standardization for ImagingBased Observational Research: OMOP Common Data Model Extension. J Digit Imaging. Inform. med. (2024). doi:10.1007/s10278-024-00982-6
- [17] Osterman TJ, Terry M, and Miller RS. Improving cancer data interoperability: the promise of the Minimal Common Oncology Data Elements (mCODE) initiative. JCO Clinical Cancer Informatics 4 (2020): 993-1001.
- [18] Bodenreider O. The Unified Medical Language System (UMLS): integrating biomedical terminology. Nucleic Acids Res. 2004 Jan 1;32(Database issue):D267-70. doi: 10.1093/nar/gkh061. PubMed PMID: 14681409; PubMed Central PMCID: PMC308795.
- [19] Osterman TJ, Terry M, Miller RS. Improving Cancer Data Interoperability: The Promise of the Minimal Common Oncology Data Elements (mCODE) Initiative. JCO Clinical Cancer Informatics. 2020; Vol 4:4. doi: 10.1200/CCI.20.0005.
- [20] Bernasconi A, Guizzardi G, Pastor O, Storey VC. Semantic interoperability: ontological unpacking of a viral conceptual model. BMC Bioinformatics 2022, 23(Suppl 11):491.doi:10.1186/s12859-022-05022-0
- [21] Smith B, Kumar A, Bittner T. Basic Formal Ontology for Bioinformatics; 2005
- [22] Arp R, Smith B, and Spear A. Building ontologies with Basic Formal Ontology. 2015. Cambridge, MA: MIT Press
- [23] Guizzardi G, Wagner G, Almeida JPA, Guizzardi RS. Towards ontological foundations for conceptual modeling: The unified foundational ontology (UFO) story. Appl Ontol. 2015;10(3-4):259-71.
- [24] Guizzardi G, Botti Benevides A, Fonseca CM, Porello D, Almeida JPA, Prince Sales T. UFO: Unified Foundational Ontology. Appl Ontol. 2022;17(1):167-210. doi:10.3233/ao-210256.
- [25] Lin, D. An Information-Theoretic Definition of Similarity. In: Jude W. Shavlik (eds.) Proceedings of the Fifteenth International Conference on Machine Learning, ICML'98, pp. 296-304. Morgan Kaufmann Publishers Inc. (1998). doi:10.5555/645527.657297.
- [26] Mayo CS et al. Operational Ontology for Oncology (O3): A Professional Society-Based, Multistakeholder, Consensus-Driven Informatics Standard Supporting Clinical and Research Use of Real-World Data From Patients Treated for Cancer. Int J Radiat Oncol Biol Phys. 2023 Nov 1;117(3):533-550. doi: 10.1016/j.ijrobp.2023.05.033. Epub 2023 May 26. PMID: 37244628; PMCID: PMC10741247.
- [27] Hong et al. Operational Ontology for Oncology: A Framework for Improved Communication and Understanding in Cancer Care. int J Radiat Oncol Biol Phys. 2023 Nov 1;117(3):551-553. doi:10.1016/j.ijrobp.2023.02.058
- [28] De Zegher I, C ¸ eleb, R, Powell L, Bihari B, Dallos D. D2.3 Solution Design Document for G1. 2023. Zenodo. doi: 10.5281/zenodo.10245773
- [29] Primov T, Boytcheva S, Celebi R. D2.1 Global Data Sharing Standard. 2023. Zenodo. doi: 10.5281/zenodo.10117718
- [30] LIMICS. (2024). EUCAIM's hyper-ontology v0.1beta. Zenodo. doi:10.5281/zenodo.10817687
