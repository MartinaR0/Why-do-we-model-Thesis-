## Knowledge Models for Diagnosing Postharvest Diseases of Apples

Armin NIEDERKOFLER a , Sanja BARIC b , Giancarlo GUIZZARDI a , Gabriele SOTTOCORNOLA a and Markus ZANKER a , 1

a Faculty of Computer Science, Free University of Bozen-Bolzano, Italy b Faculty of Science and Technology, Free University of Bozen-Bolzano, Italy

Abstract. Postharvest diseases are a common problem in the cultivation of apples. Since determining the exact disease is often difficult and time-consuming, an ontology-based decision support system is being developed to support this diagnosis process. In this paper a reference ontology is presented that captures the lifecycle of apples from the orchard to the storage phase. This ontology focuses mainly on postharvest diseases including their symptoms, characteristics, and other important factors. This reference model is represented using the ontology-driven conceptual modeling language OntoUML and it is then encoded as an OWL specification enriched with SWRL rules. The latter will then serve as a basis for supporting automated reasoning in the aforementioned decision support system.

Keywords. Postharvest diseases of Apples, Apple Diseases Ontology, decisionsupport system.

## 1. Introduction

The cultivation and export of apples is a big economic factor for many countries around the world with the US, China, and Italy leading the list. In 2014, such exports amounted to a total value of 7.5 trillion dollars [1]. However, a big economic threat are the various kinds of post-harvest diseases and disorders that can develop and spread during the stages of storage and transportation. Although these processes are constantly improved, such defects can still cause losses of up to 10% in integrated production and up to 30% in organic production [2]. One reason for this is that many diseases expose similar-looking symptoms, which makes them hard to identify. For diseases caused by pathogenic fungi, tests in specialized laboratories are necessary [3]. This makes it difficult to introduce appropriate countermeasures before defects spread and infect larger amounts of fruits.

To address this problem, the decision support system DSSApple [4] is being developed that builds on the results of the research project Frudistor [5] in order to support farmers and storage workers in the identification of diseases. The underlying basis of the system is an ontology containing the relevant apple- and disease-related information. This ontology is employed to support automated reasoning over a set of input data. Lit- erature research revealed that such a model has not yet been developed mapping fruit and disease-related data in such a way that is both extensive and detailed enough for this purpose. To address this gap in the literature, this paper proposes a reference ontology on post-harvest diseases of apples.

1 Corresponding Author: Markus Zanker, Free University of Bozen-Bolzano, Universit¨ atsplatz 1, 39100 Bozen, Italy; E-mail: Markus.Zanker@unibz.it. Copyright c © 2019 for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).

The remainder of this paper is organized as follows: First, section 2 describes the approach employed to develop our reference ontology. In that section, we discuss both the origin of our disease data, as well as adopted approach for engineering the ontology. Section 3 presents the main contribution of this paper, i.e., the DSSApple Ontology. Section 4, presents a preliminary evaluation of our model. Finally, section 5 discusses some final considerations and summarizes the work presented in this paper.

## 2. Methodological Approach

## 2.1. Gathering Disease Data

We started the project by collecting and categorizing the necessary apple disease-related information 2 . Most of the data was provided by the FrudiStor project - a web application that lists more than 40 different post-harvest diseases and physiological disorders of apples [5]. The difference between these two kinds is that diseases are caused by pathogenic fungi, while disorders develop due to nutritional imbalance, weather conditions, senescence, etc. All of these instances are post-harvest defects, which means that they show their first symptoms only during storage or distribution, even if fruits were already infected in the orchard.

The data we used from the Frudistor application mainly consisted of plain text descriptions of the symptoms of diseases and their development progress. Similar to human diseases, the characteristics of a fruit disease at an early stage may be different from those at a later moment, which needs to be taken into account when determining the exact disorder. Typical symptoms are: spots on the surface of the fruit, different types of rots, discolorations, development of spores, etc. Further information includes the life cycle of diseases (the points in time when fruits are infected and when symptoms become visible), susceptible varieties, possible causes, and similar diseases that can be easily confused.

## 2.2. The Ontology Engineering Approach

For the development of the ontology presented in section 3, we have considered the data gathered about the domain (see section 2.1), the expert opinion of domain experts, as well as existing ontologies in the field [6,7] (indluding the IDOPlant Ontology [8]).

Despite considering a number of ontological choices put forth by these existing ontologies, reusing their structure directly posed some significant difficulties. Besides not covering all aspects that are needed for supporting our decision-support system, the most salient problem with these existing ontologies is that frequently they conflate multiple (albeit independent) phenomena dealing with plant diseases. This tends to result in an combinatorial proliferation of classes (e.g.,). To avoid this problem, we decided to model the scope defined by some of these existing models but to evolve and organize it as a new full-blown reference ontology addressing specific aspects of the apple pathology domain. In particular, by applying the methodological approach of separation of concerns , we organize our ontology in 5 modules, each one addressing a different type of phenomenon in reality (see section 3).

2 Note that unless specified otherwise, this paper may use the terms disease , disorder , and defect interchangeably for a better reading.

As a second methodological principle, we separated the conceptual modeling phase of the engineering process from the codification (or implementation ) phase [9]. For the former phase, to develop our reference ontology, we have used the support of the foundational ontology UFO (Unified Foundational Ontology) [10]. In particular, this was done by employing the UFO-based conceptual modeling language OntoUML [11,12]. This allows us to directly apply the UFO-based ontology design patterns present in the language, as well as a number of supporting tools for ontology quality assurance (e.g., verification and validation tools, anti-pattern detection and rectification tools, verbalization tools, etc.). In particular, this allows for the systematic code generation of an OWL specification representing our conceptual reference model. So, for the latter phase of this process, we employed the representation language OWL enriched with SWRL rules. In this paper, we focus on the conceptual part of this reference ontology.

## 3. The DSSApple Ontology

In the sequel, we elaborate on the 5 modules constituting our reference ontology: apple characterization , apple handling , apple pathologies , apple dispositional factors , and apple representation .

## 3.1. Apple Characterization

This module addresses the apple itself, its possible types, its parts as well as its qualities and features.

An Apple is composed of a number of (functional) Apple Parts [13]. Apple bears a relation of instantiation to an Apple Cultivar (e.g., Golden Delicious, Gala, HoneyCrisp). This relation is formally defined in [14] and implies that every instance of Apple is an instance of an instance of Apple Cultivar. In other words, the latter is a sort of higher-order type (also termed powertype [15] or classification type [16]) whose instances are types of Apples. Analogously, an apple part can be refined in a number of apple part subtypes (e.g., endocarp, exocarp, mesocarp).

Apples and their parts (here termed Apple Substances ) can be characterized by Apple Aspects , including Apple Qualities or Apple Features . The former includes Taste , Color , but also Texture , Odor (not in the diagram), among others. In UFO and, hence, in OntoUML, qualities are full-fledged endurants [12] and, thus, they can endure in time and change in a qualitative manner whilst maintaining their identity. So, in different time intervals, a quality can manifest a different Apple Quality State . Each of these states can have a different qualitative value that is taken suitable quality structure (by redefining the abstract relation has value - not shown in the model). These quality spaces are geometric value spaces (e.g., the Apple Color Space is a proper part of a tridimensional space composed of the dimensions of hue, saturation and brightness; analogously, the Apple Taste Space is a proper part of a four-dimensional space forming a taste tetrahedron) [11,17]. Apple Features include Apple Stain , Hole in Apple , but also Insect Sting in Apple and Pressure Mark in Apple (not shown in the diagram), among others.

Figure 1. Module 1 describing the characteristics of an apple

[FIGURE]

As with all aspects [11], the common characteristic of apple qualities and apple features is that they are existentially dependent on some bearer, namely, apple and their parts. In OntoUML, this relation of existential dependence is represented by the relation of characterization [11].

There are certain qualities that characterize the fruit as a whole. In particular, the Apple Nutritional Factor . For this reason, for example, a redefined relation of characterization is created between Apple Nutritional Factor and Apple . Finally, since aspects are endurants in UFO, they can bear their own aspects, which, in turn, can change in time. For instance, a hole can have a diameter, which can vary in time.

## 3.2. Apple Handling

This second module addresses the parts of an apple handling activities as the characteristics of these handling processes may have a significant influence on the health of whole apple batches.

Apple Handling activities here include Apple Harvest and Apple Storage activities. Since all apple handling activities are subtypes of Event , they occur in a particular time interval (delimited by time points). As discussed in [18], from these time points, we can infer the derived relations between events. Here, use the a historical dependence relation (see [11]) to represent that Apple Storage must be preceded by Apple Harvest activities. Finally, all events occur in a Spatial Region .

In all Apple Handling Activities , we have the participation of an Apple Batch , which is a collective whose members are individual Apples (see the member of relation in [19]). In Apple Storage , we also have the participation of a Storage Facility , which is a role played by a Building .

Figure 2. Description of the handling processes during harvest and storage

[FIGURE]

Storage facilities and spatial regions are Spatial Entities . All spatial entities can be characterized by Physical Qualities , such as Humidity , Gas Concentration and Temperature . Since we are interested in how these qualities change their values through time, we, once more, employ here one of the truthmaking patterns proposed in [20]. In this way, we explicitly represent the Physical Quality States of Physical Qualities . Each of these states (which are events and, hence, occur in a particular time interval) can be mapped to a value in a suitable quality space. Moreover, we define a particular type of Physical Quality State called a Physical Quality State of Spatial Entity During Apple Handing . As explicit in its name, this is a quality state of either a store facility involved in an Apple Storage activity or the quality state of a spatial region on which an Apple Handing Activity occurs. As such, the relation of occurs during represented in this model implies the Allen relation of temporal mereological overlapping between the two events it relates [18].

By doing this, we can capture in different times points, for example, the temperature, humidity and gas concentration of particular facilities or regions during storage and harvest, respectively. Moreover, since both Physical Quality States as well as Apple Handling Activities are events, which occupy a certain spatial region, we can infer, for example, the origin of the fruits in a batch, the age of the fruits at the moment they enter the storage facility, storage duration, etc. Different storage conditions can favour the spread of a disease, but in some cases they may also heal certain symptoms. We address these aspects in the next module of this ontology.

Characteristics of these handling processes may have a significant influence on the health of whole apple batches. Handling processes include the actions during harvest as well as the storage characteristics. Main parameters here are the storage temperature, humidity, gas concentration, the storage duration, and the age of the fruits at the moment they enter the storage facility. Different storage conditions can favour the spread of a disease, but in some cases they may also heal certain symptoms. These concepts are represented in the second module. Additional classes connected to the harvest allow to draw conclusions about the origin of the fruits.

## 3.3. Apple Pathology

This third module addresses the core of this ontology, dealing with Apple Pathologies and their manifestations ( Apple Pathology Manifestation ). In this model, an Apple Substance can eventually be in a Pathological Apple Substance phase (see semantics of phase in [11]). This happens when it bears an Apple Pathology . An apple pathology is a type of disposition of a given type ( Apple Pathology Type ). As it is usually the case with dispositions [21], an Apple Disposition is grounded in a number of Apple Aspects . These, in turn, can be either intrinsic aspects (qualities, features or other dispositions) or relational aspects ( Pathogen Signs ). In the former case, this Apple Pathology instantiates an Apple Disorder Type ; in the latter case, it instantiates a Apple Disease Type . A Pathogen Sign is a relator [22], i.e., a relation aspect binding an Infected Apple Substance (a role played by Pathological Apple Substance ) w.r.t. a given Pathogen Collective , which aggregates Pathogens of a given Pathogen Type , which, in turn, can be associated with particular Apple Disease Types .

Again, as it is always the case with dispositions [21], when manifested, an Apple Pathology is manifested through the occurrence of an event, which in this case it is instances of Apple Pathology Manifestation . This even, in turn, is composed of a number of sub-events termed Apple Symptom Manifestation . A symptom manifestation is considered here to be an aggregation of states of particular relevant qualities ( Apple Quality State ) of the Apple Substance (the apple itself and its parts). Symptom manifestations are instances of Apple Symptom Type , which are correlated with particular types of Apple Pathologies ( Apple Pathology Type ).

## 3.4. Apple Dispositional Factors

The fourth Module represents pathology enabling factors Apple Pathology Enabling Factor (sometimes called dispositional factors ). These are factors that are associated with Apple Pathology Types in the sense that they can enable the onset of apple pathologies 3 , but also in the sense that they can activate the manifestation of these pathologies (see discussion on mutual activation partners for dispositions in [21]). Apple Pathology Enabling Factor is a cross-categorical types since its instances can be features ( Apple Features such as Insect Sting in Apple or Pressure Mark in Apple ), Apple Qualities (e.g., Apple Low Nutritional Factor - a contingent phase of a particular Apple Nutritional Factor quality), or even events such as Inadequate Physical Quality State of Spatial Entity During Apple Handling (e.g., a storage activity having a storage facility with an inadequate temperature, humidity or gas concentration).

## 3.5. Apple Prototype Representation

This final module addresses the image processing part of the decision support system. To support the operation the system is working, our model needs to be able to relate prototypical pictures associated with symptom types ( Prototypical Apple Symptoms Photograph ), as well as prototypical pictures associated with types of ( Prototypical Apple Pathogen Sign Photograph ). The model also recognizes the existence of photographs of particular symptom manifestations ( Apple Symptoms Photograph ) of particular apples, as well as of pathogen signs ( Apple Pathogen Infection Photograph ). Photographs of these two latter kinds can deliberately chosen to play the role of prototypes, i.e., Prototypical Apple Symptoms Photograph and Prototypical Apple Pathogen Sign Photograph are roles played by photographs of individual apples

3 For a discussion on how enabling factors can activate the manifestation of vulnerabilities, the reader can refer to [23].

Figure 3. The pathology view representing the disease state of an apple consisting of the states of its single parts

[FIGURE]

Figure 4. Dispositional factors that either occur before or during harvest and favour the development of defects

[FIGURE]

Figure 5. Representation of the image data of the system with the dinstinction between images of symptoms and images of signs

[FIGURE]

## 3.6. Ontology Encoding in SWRL

In order to support reasoning with actual disease instances according to the descriptions in the specialist literature, we implemented parts of the model in section 3 as an ontology in the OWL language enriched with SWRL rules [24].

This approach not only gave us the required flexibility to represent the myriad of possible combinations of aspects and aspect values that can be used to characterize specific pathologies. So, the disease data in our model would not just include information like 'there are spots on the skin of the apple', but rather provide detailed descriptions like 'the spots on the apple are brown with irregular shapes and diffuse margins', which may increase the reasoning power of a decision support system. As a concrete example, a description of Alternaria Rot in FrudiStor amounts to 'Early infestation usually occurs in the calyx area of the fruit. Typically, there are small (up to 0.5 mm large) dark brown or black lenticel spots, which are often surrounded by a brown ring. ' . A description like this can be described as a conjunctive SWRL rule using the predicates of our proposed ontology, which, in this case, refers to pathogen signs, apple parts, features, and qualities of features having specific values.

## 4. Preliminary Evaluation

## 4.1. A Simple Diagnostic System

In order to get a first experience on how the decision support system would work, we developed a simple diagnostic system for a subset of 5 diseases ( Alternaria Rot, Bitter Rot, Botrytis, Penicillium Rot, and Mucor Rot ). Through an online survey [24], a nonexpert user was given 15 images of bad apples, from which each one was infected by one of the five diseases. The user had to specify which kinds of symptoms occurred (rots, spots, lesions, etc.), on which parts of the fruit they appeared, and finally describe the characteristics of the symptoms in more detail (including color, shape, texture, etc.). In order to evaluate the prediction accuracy, we split each rule into multiple simpler SWRL rules, where - for simplicity sake - a single rule only contained a single symptom of a disease, which resulted in 8-19 one-symptom rules per disease. This approach follows the recommendation for preference-based reasoning with soft rules or constraints as outlined in [25]. Requiring the conjunction of all symptoms as a precondition for deriving a disease would actually lead to empty result sets in all cases. However, when ranking the diseases for each of the 15 test cases based on the share of identified symptoms by the total number of symptoms of the respective disorder, i.e. assuming equal weights for each rule and ranking items like described in [25], the experiment revealed the results presented in next section.

## 4.2. Evaluation of the Results

In most cases and for a given disease the user identified about 50% of the symptoms as described in the literature. Although this number may appear rather small at first, it has to be taken into account that tests have been conducted only with images of apples and not with real infected fruits. Since it is very unlikely that all possible symptoms of a disease will be present on a single image, identifying 100% of all symptoms is extremely unlikely.

In addition, several symptoms have been wrongly identified (false positives). Furthermore, several diseases have some symptoms in common, which also leads to high scores for multiple diseases.

As a measure for the predictive accuracy of our results, we report Precision at 1, which means that based on the identified symptoms the correct disease was most highly ranked. Top-1 Precision: actually reached 0.533% (8 out of 15). In contrast, in an earlier user study in which randomly selected images of diseased apples were presented to users, who clicked on these images based on the perceived similarity with their target image [4]. There a random image selection algorithm lead to an overall success rate of 28%, i.e. in less than a third of all cases users were able to correctly identify the disease of the target apple. Thus, in future work we will explore how to fuse the explicit user feedback and knowledge-based reasoning on symptoms with a picture-based navigation approach.

## 5. Conclusion

In this paper we propose a reference ontology to model the life cycle of apples, so that it can be used in a decision support system to support the diagnosis of postharvest defects. Reusing existing ontologies as base models showed limited results, as they provided a useful base structure, but were lacking the expressivity to represent more complex relations. To handle this complexity, we designed our new model in OntoUML and divided it into 5 modules, where each describes a specific aspect of an apple's life cycle, while focusing on the disease-related aspects. To be able to include all information from the specialist literature in our ontology, we added SWRL rules that allowed us to model the symptom descriptions very precisely. Finally, first tests of these rules in a simple diagnostic system already showed some promising results for decision support of users.

## References

- [1] T. Haqqi, '10 countries that export the most apples in the world,' May 2016. [Online]. Available: https://www.insidermonkey.com/blog/10-countries-that-export-the-most-apples-in-the-world-446514/
- [2] P. Maxin, M. Williams, and R. Weber, 'Control of fungal storage rots of apples by hot-water treatments: A northern european perspective,' Erwerbs - Obstbau , vol. 56, no. 1, pp. 25-34, 3 2014.
- [3] F. Martinelli, R. Scalenghe, S. Davino, S. Panno, G. Scuderi, P. Ruisi, P. Villa, D. Stroppiana, M. Boschetti, L. R. Goulart, C. E. Davis, and A. M. Dandekar, 'Advanced methods of plant disease detection. A review,' Agronomy for Sustainable Development , vol. 35, no. 1, pp. 1-25, 2015. [Online]. Available: https://hal.archives-ouvertes.fr/hal-01284270
- [4] M. Nocker, G. Sottocornola, M. Zanker, S. Baric, G. A. Carneiro, and F. Stella, 'Picture-based navigation for diagnosing post-harvest diseases of apple,' in Proceedings of the 12th ACM Conference on Recommender Systems . ACM, 2018, pp. 506-507.
- [5] S. K. Obstbau-Bodensee, 'Frudistor - die app zur bestimmung von lagersch¨ aden,' http://www.frudistor. de/, accessed on 15.06.2019.
- [6] O. Foundry, 'Plant ontology,' http://www.obofoundry.org/ontology/po.html, https://github.com/ Planteome/plant-ontology, accessed on 12.09.2017.
- [7] L. G. Cowell and B. Smith, Infectious Disease Ontology . New York, NY: Springer New York, 2010. [Online]. Available: https://doi.org/10.1007/978-1-4419-1327-2 19
- [8] R. L. Walls, B. Smith, J. Elser, A. Goldfain, D. W. Stevenson, and P. Jaiswal, 'A plant disease extension of the infectious disease ontology,' in International Conference on Biomedical Ontology (ICBO-2012) , 2012.
- [9] G. Guizzardi, 'Theoretical foundations and engineering tools for building ontologies as reference conceptual models,' Semantic Web , vol. 1, no. 1-2, pp. 3-10, 2010. [Online]. Available: https://doi.org/10.3233/SW-2010-0015
- [10] G. Guizzardi, G. Wagner, J. P. A. Almeida, and R. S. S. Guizzardi, 'Towards ontological foundations for conceptual modeling: The unified foundational ontology (UFO) story,' Applied Ontology , vol. 10, no. 3-4, pp. 259-271, 2015. [Online]. Available: https://doi.org/10.3233/AO-150157
- [11] G. Guizzardi, 'Ontological foundations for structural conceptual models,' Ph.D. dissertation, University of Twente, Enschede, 2005. [Online]. Available: http://doc.utwente.nl/50826/
- [12] G. Guizzardi, C. M. Fonseca, A. B. Benevides, J. P. A. Almeida, D. Porello, and T. P. Sales, 'Endurant types in ontology-driven conceptual modeling: Towards ontouml 2.0,' in Conceptual Modeling -37th International Conference, ER 2018, Xi'an, China, October 22-25, 2018, Proceedings , 2018, pp. 136-150. [Online]. Available: https://doi.org/10.1007/978-3-030-00847-5 \ 12
- [13] G. Guizzardi, 'The problem of transitivity of part-whole relations in conceptual modeling revisited,' in Advanced Information Systems Engineering, 21st International Conference, CAiSE 2009, Amsterdam, The Netherlands, June 8-12, 2009. Proceedings , ser. Lecture Notes in Computer Science, P. van Eck, J. Gordijn, and R. Wieringa, Eds., vol. 5565. Springer, 2009, pp. 94-109. [Online]. Available: https://doi.org/10.1007/978-3-642-02144-2 \ 12
- [14] V. A. de Carvalho, J. P. A. Almeida, and G. Guizzardi, 'Using a well-founded multi-level theory to support the analysis and representation of the powertype pattern in conceptual modeling,' in 28th International Conference on Advanced Information Systems Engineering (CAiSE 2016), Ljubljana, Slovenia, June 13-17, 2016 , ser. LNCS, S. Nurcan, P. Soffer, M. Bajec, and J. Eder, Eds., vol. 9694. Springer, 2016, pp. 309-324. [Online]. Available: https://doi.org/10.1007/978-3-319-39696-5 \ 19
- [15] G. Guizzardi, J. P. A. Almeida, N. Guarino, and V. A. de Carvalho, 'Towards an ontological analysis of powertypes.' in JOWO@ IJCAI , 2015.
- [16] G. Guizzardi and G. Wagner, 'Some applications of a unified foundational ontology in business modeling,' in Business Systems Analysis with Ontologies . IGI Global, 2005, pp. 345-367.
- [17] P. G¨ ardenfors, Conceptual spaces: The geometry of thought . MIT press, 2004.
- [18] G. Guizzardi, G. Wagner, R. de Almeida Falbo, R. S. S. Guizzardi, and J. P. A. Almeida, 'Towards ontological foundations for the conceptual modeling of events,' in Conceptual Modeling -32th International Conference, ER 2013, Hong-Kong, China, November 11-13, 2013. Proceedings , ser. Lecture Notes in Computer Science, W. Ng, V. C. Storey, and J. Trujillo, Eds., vol. 8217. Springer, 2013, pp. 327-341. [Online]. Available: https://doi.org/10.1007/978-3-642-41924-9 \ 27
- [19] G. Guizzardi, 'Ontological foundations for conceptual part-whole relations: The case of collectives and their parts,' in Advanced Information Systems Engineering -23rd International Conference, CAiSE 2011, London, UK, June 20-24, 2011. Proceedings , ser. Lecture Notes in Computer Science, H. Mouratidis and C. Rolland, Eds., vol. 6741. Springer, 2011, pp. 138-153. [Online]. Available: https://doi.org/10.1007/978-3-642-21640-4 \ 12
- [20] N. Guarino, T. P. Sales, and G. Guizzardi, 'Reification and truthmaking patterns,' in Conceptual Modeling - 37th International Conference, ER 2018, Xi'an, China, October 22-25, 2018, Proceedings , 2018, pp. 151-165. [Online]. Available: https://doi.org/10.1007/978-3-030-00847-5 \ 13
- [21] S. Mumford, Dispositions . Clarendon Press, 2003.
- [22] N. Guarino and G. Guizzardi, 'We need to discuss the relationship: Revisiting relationships as modeling constructs,' in 27th Intl. Conf. on Advanced Information Systems Engineering (CAiSE 2015), Stockholm, Sweden, June 8-12, 2015, Proceedings , ser. LNCS, J. Zdravkovic, M. Kirikova, and P. Johannesson, Eds., vol. 9097. Springer, 2015, pp. 279-294. [Online]. Available: https://doi.org/10.1007/978-3-319-19069-3 \ 18
- [23] T. P. Sales, F. Bai˜ ao, G. Guizzardi, J. P. A. Almeida, N. Guarino, and J. Mylopoulos, 'The common ontology of value and risk,' in International Conference on Conceptual Modeling . Springer, 2018, pp. 121-135.
- [24] A. Niederkofler, 'Creation of an ontology and reasoning mechanism for post-harvest diseases of apple cultivars,' Ph.D. dissertation, Master Thesis, Free University of Bozen-Bolzano, Italy, 2019.
- [25] M. Zanker, M. Jessenitschnig, and W. Schmid, 'Preference reasoning with soft constraints in constraintbased recommender systems,' Constraints , vol. 15, no. 4, pp. 574-595, 2010.
