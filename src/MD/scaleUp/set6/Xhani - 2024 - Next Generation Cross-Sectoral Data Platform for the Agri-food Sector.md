## Next Generation Cross-Sectoral Data Platform for the Agri-Food Sector

Donika Xhani ∗ , † , Anand Gavai, Gayane Sedrakyan, Renata Guizzardi-Silva Souza and Jos van Hillegersberg

Industrial Engineering &amp; Business Information Systems (IEBIS) group, University of Twente, Enschede, the Netherlands

## Abstract

The food system is a complex network encompassing various stakeholders, including primary producers, manufacturers, retailers, and consumers. Across all the stages of the food supply chain, a significant amount of data is produced, offering valuable insights crucial for ensuring the delivery of safe, highquality, and cost-effective products to meet the needs of a growing global population. Recommender systems are commonly used in the food domain but often lack personalization, leading to generic recommendations. Enhancing user experience through explainability offers transparent reasoning behind recommendations, fostering trust and informed decision-making. Semantic reasoning can be enhanced through ontology-based user profiles. Moreover, the increased data sharing in the food sector has raised privacy and security concerns, prompting the development of privacy-preserving data platforms. This PhD project aims to address these challenges by (1) utilizing ontologies for enhancing semantic interoperability, (2) employing eXplainable Artificial Intelligence (XAI) methods and semantic reasoning for enhancing the transparency of recommender systems, and (3) designing a privacy-preserving data platform that facilitates data sharing while ensuring the protection of sensitive information.

## Keywords

Food supply chain, ontology, recommender system, data platform, explainable AI

## 1. Introduction

The food system comprises a multitude of participants across the supply chain: (1) primary producers such as cultivators, farmers, and aquafarmers, (2) food producers such as breeders, processors, and packers, (3) retailers such as distributors, supermarkets and restaurants, (4) logistics such as transporters, shippers and carriers, and (5) consumers [1]. Throughout every stage of the food supply chain, a substantial volume of data is produced, offering valuable insights to those managing the processing and distribution of food items from production to consumption [1]. Effective management of this food data plays a vital role in ensuring the delivery of safe, high-quality, and cost-effective products to meet the needs of a growing global population [1, 2].

A guidance for achieving appropriate data management is the FAIR principles [3], which ensure Findability, Accessibility, Interoperability, and Reusability of the data [4], and present

FOIS 2024: International Conference on Formal Ontology in Information Systems, Enschede, the Netherlands

Envelope-Open d.xhani@utwente.nl (D. Xhani); a.k.gavai@utwente.nl (A. Gavai); g.sedrakyan@utwente.nl (G. Sedrakyan);

r.guizzardi@utwente.nl (R. G. Souza); j.vanhillegersberg@utwente.nl (J. v. Hillegersberg)

[FIGURE]

© 2024 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).

huge opportunities in the scientific community [5]. However, ensuring interoperability (the 'I' in FAIR) by representing the semantics using ontologies remains a demanding task [5, 6].

In the food domain, recommender systems are commonly used for recommending different food items or recipes in accordance with the user's preferences, nutritional goals, or dietary restrictions. Current food recommendation systems face several limitations such as the lack of personalization by often relying on generic suggestions rather than taking into account user's preferences, dietary constraints, cultural heritages, and health-related needs [7].

Enhancing user experience can be achieved through explainability, which offers transparent and understandable reasoning behind specific recommendations [8, 9]. This empowers users to make informed decisions and builds trust [9, 7, 8]. For instance, explaining that a lactose-free dish is recommended because it aligns with the user's dietary needs of not eating milk-based products. For example, in this case, the recommender system can give this explanation: 'This meal was suggested because it aligns with your lactose-free dietary requirements ' provides clarity and reinforces trust in the system [7]. For this purpose, the recommender system can rely on eXplainable Artificial Intelligence (XAI) models which refers to techniques used for making the Machine Learning (ML) models interpretable and comprehensible by humans [10].

XAI can be implemented by using post-hoc approaches which refer to the application of XAI models on top of the black-box output generated from a ML model [8]. For explaining the decision-making and the output of a food recommender system, it is crucial to comprehend which are the important features i.e., by doing feature extraction by using the SHAP model, and to have textual explanation for creating personalized explanations [8]. Semantic reasoning of the food recommender system can be enhanced by the usage of ontologies by enabling ontologybased user profiles, which can help the algorithms understand user preferences, dietary needs and culinary aspects [7].

The increase of data sharing among the actors and sharing of personal data and health data has led to increased awareness of privacy and security concerns. Privacy-preserving data platforms are systems that facilitate the data sharing while ensuring the protection and security of sensitive information [11, 12]. Such platforms enable users to make well-informed food decisions while safeguarding their sensitive data, thereby enhancing the security and reliability of the user experience [7].

This PhD project aims to dive into these areas: (1) the usage or design of ontologies for enhancing semantic interoperability in the food supply chain, (2) the usage of XAI methods and semantic reasoning for explaining the decision-making of the recommender systems and the generated output, and (3) the design of a privacy-preserving data platform.

## 2. Research Questions

The development of this future food system inspires the following Research Questions (RQ) that will be carried out throughout the PhD.

The main RQ is:

How to design a next-gen cross-sectoral data platform that ensures semantic interoperability, privacy-preserving, and provides Explainable AI solutions?

The sub-research questions are:

Figure 1: Conceptual Model of the proposed solution

[FIGURE]

1. How to enhance semantic interoperability and explainable artificial intelligence (XAI) in food supply chains or food recommender systems?
2. Whatprivacy-preserving techniques are most effective for protecting sensitive agricultural data?
3. What architectural models are best suited for integrating cross-sectoral data while maintaining privacy and interoperability?
4. What are the specific needs and requirements of the various stakeholders in the agricultural sector?
5. What are the potential applications and benefits of the platform in real-world agricultural scenarios?

## 3. Methodology

The methodology used in this PhD project is the Design Science methodology [13]. The Problem Investigation phase is used to identify what is the state-of-the-art regarding existing ontologies and knowledge graphs in the agri-food domain, XAI techniques that are used in food recommenders, and privacy-preserving techniques. The Treatment Design phase is used to identify (1) requirement analysis, (2) adopting existing web technologies frameworks, (3) designing a semantic web technologies-based recommender, and (4) modeling of a reference architecture for next-gen privacy-preserving data platform. The Treatment Validation phase is used for (1) validating the used semantic web technologies, (2) using the single case mechanism method in a case study for validating the prototype, and (3) using the expert opinion method for validating the reference architecture models.

## 4. Conceptual Model

Figure 1 illustrates the primary components of the proposed solution, which addresses our research questions in the following manner. The privacy-preserving data platform ensures that each stakeholder retains ownership of their data and can selectively permit access to it. Each data station is managed by a data owner and is accessible via specific algorithms. The platform leverages ontologies to guarantee semantic interoperability. Additionally, the recommender system generates explainable recommendations, thereby assisting users in obtaining informed and transparent outcomes.

## References

- [1] Zeb A, Soininen JP, Sozer N. Data harmonisation as a key to enable digitalisation of the food sector: A review. Food and Bioproducts Processing. 2021 May 1;127:360-70.
- [2] Ivanov VM, Shevchenko O, Marynin A, Stabnikov V, Stabnikova E, Gubenia O, Shevchenko A, Gavva OM, Salyuk A. Trends and expected benefits of the breaking edge food technologies in 2021-2030.
- [3] Zontal. Fair Data-How data increase the value of Biotechs [Whitepaper].2020.
- [4] Jacobsen A, de Miranda Azevedo R, Juty N, Batista D, Coles S, Cornet R, Courtot M, Crosas M, Dumontier M, Evelo CT, Goble C. FAIR principles: interpretations and implementation considerations. Data intelligence. 2020 Jan 1;2(1-2):10-29.
- [5] Top J, Janssen S, Boogaard H, Knapen R, Şimşek-Şenel G. Cultivating FAIR principles for agri-food data. Computers and Electronics in Agriculture. 2022 May 1;196:106909.
- [6] Pizzuti T, Mirabelli G, Sanz-Bobi MA, Goméz-Gonzaléz F. Food Track Trace ontology for helping the food traceability control. Journal of Food Engineering. 2014 Jan 1;120:17-30.
- [7] Sedrakyan G, Gavai A, van Hillegersberg J. Design Implications Towards Human-Centric Semantic Recommenders for Sustainable Food Consumption. InInternational Conference on Conceptual Modeling 2023 Oct 26 (pp. 312-328). Cham: Springer Nature Switzerland.
- [8] Tessa M, Abchiche S, Ferstler YC, Tchappi I, Benatchba K, Najjar A. Enhancing Explanaibility in AI: Food Recommender System Use Case. InProceedings of the 11th International Conference on Human-Agent Interaction 2023 Dec 4 (pp. 395-397).
- [9] Rostami M, Muhammad U, Forouzandeh S, Berahmand K, Farrahi V, Oussalah M. An effective explainable food recommendation using deep image clustering and community detection. Intelligent Systems with Applications. 2022 Nov 1;16:200157.
- [10] Seeliger A, Pfaff M, Krcmar H. Semantic web technologies for explainable machine learning models: A literature review. PROFILES/SEMEX@ ISWC. 2019 Oct 27;2465:1-6.
- [11] Qadeer B, Shah MA, Ishaq A. Privacy Preservation in Digital Economy Platforms.
- [12] Durrant A, Markovic M, Matthews D, May D, Leontidis G, Enright J. How might technology rise to the challenge of data sharing in agri-food?. Global Food Security. 2021 Mar 1;28:100493.
- [13] Wieringa RJ. Design science methodology for information systems and software engineering. Springer; 2014 Nov 19.
