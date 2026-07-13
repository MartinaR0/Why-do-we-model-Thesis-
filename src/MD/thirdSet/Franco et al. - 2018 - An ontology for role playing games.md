## An Ontology for Role Playing Games

Artur O. R. Franco, T´ ulio V. Rolim, Alexandre M. M. Santos, Jos´ e W. F. Silva, Vˆ ania M. P. Vidal, Fernando A. C. Gomes, Miguel F. Castro, Jos´ e G. R. Maia Universidade Federal do Cear´ a Fortaleza, Cear´ a, Brazil

Email: { artur.fhtagn,tulio.xcrtf,magnomont12 } @gmail.com, wellington@crateus.ufc.br, { vvidal,fernando,miguel } @lia.ufc.br

Abstract -In this paper, we introduce a new, comprehensive ontology specially designed for modeling Role-Playing Games semantics. We build on top of a foundational ontology approach, namely Unified Foundational Ontology, to cover elements from Interactive Storytelling and aspects from a game's narrative. Experimental results using two well-known, representative titles from the electronic and the analog supports, respectively, shows promising flexibility and effectiveness in terms of competency questions.

Keywords -games; rpg; ontologies; semantic web;

## I. INTRODUCTION

According to Tim Bernets Lee [1], endowing web data with significance will make it possible for computers and people to interact more seamlessly. This is a core goal of the Semantic Web, but electronic games stand out as research opportunities for exploring other medias [2]. Doran and Parberry [3] analyzed adventures from four Massive Multiplayer Online Role Playing Games (MMORPG) titles in order to realize which elements of this genre that could be recommended for automatic quest generation models. Their study is limited to the MMORPG genre, thus excluding other rich models such as text adventures, tabletop Role Playing Game (RPG), and electronic RPG played online.

This work aims to provide an improved semantic model, which is necessary to consult and discuss a given material in common for these RPG platforms. Models, methods, and techniques already applied in the context of semantic web are reused and adapted for tackling the challenges regarding 'semantic games' [2]. Within the context of RPGs, we already can find ontologies such as the one proposed by Djuric and Konecki [4], which fits well to a part of RPGs, but cannot extract other simple information about adventures, quests, and other concepts which are central for typical applications of RPG game semantics [3]. We propose a comprehensive ontology specially designed for modeling RPG games for semantic applications, which is built on top of Unified Foundational Ontology (UFO) [5] and covers elements from Interactive Storytelling (IS).

## II. RELATED WORK

In the vast field of philosophy, ontologies are applied in the study of the nature and existence of elements, while in computing this term became widely known due to its use for the representation of knowledge [6]. There are different definition of ontologies, as can be observed from the following definitions found in literature [7] [8] [9] [10].

## A. Brief Literature Survey

The Video Game Ontology (VGO) [10] aimed at the interoperability between games and providing the exchange of information. This model covers characters, items, and events happening between the games, by extending an approach initially proposed in [11]. A similar, previous approach [12] named Digital Game Ontology was shown to be sufficiently capable of processing a wide variety of concepts and events from digital games as pieces of media. These authors sought to produce an ontology suitable for applications related to game production, activities, and players' experience. Other works [13] propose to facilitate the identification of technical requirements in game design through an Ontology in support of Games Development.

Existing game concepts were exposed to model a new ontology that represents general aspects of serious games [14] resorting to a formalized model and language capable of supporting the creation of new game-specific content. Sacco et al. [15] present a vocabulary for describing character information in digital games, and also an ontology that can be used to define information extracted from several different data sources of game characters. Kritz et ak. [16] developed an ontology that represents Game Mechanics based on the categories presented on BoardGameGeek.com through the formal concepts of the well-known MDA Mechanics, Dynamics, and Aesthetics framework [17]. The general purpose of these studies was to represent generic aspects of games and their components, hence there a lack of comprehensive models developed specifically to handle the RPG domain.

Okrea and Schatten [9] present a mixture between an ontology of organizational concepts, adequate for the development of Large-scale Multi-Agent Systems (LSMAS) , in conjunction with an ontology composed of the elements found in the MMORPG title The Mana World 2 [18]. By proposing this combination, these authors emphasizes especially the identification of elements and organizational aspects they argue are appropriate to the development of LS- MAS in the context of MMORPGs. Roman [19] detailed a general method comprised by the use of both W3C Resource Description Framework (RDF) and W3C Web Ontology Language (OWL) standards as a way to represent knowledge in RPG games. According to the author, his method covers elements like characters, history, and resources. In order to integrate these elements, the work used Jena framework in a fictitious Java-based game which was written by the authors as a study case. Similarly, in [4], an ontology was proposed for RPG games in the style of [18] contemplating aspects of: NPCs ( Non-Player Characters ), characters, items, maps, abilities, (skills) , and properties. Table I presents the main related works found in the literature regarding the adoption or development of ontologies for RPG games. Columns in this table provide a comparison on what important aspects can be found in published works and this paper.

TABLE I. COMPARISON OF RELATED WORK

|            | Ontoloy Reuse   | Approaches Storytelling   | UFO   |
|------------|-----------------|---------------------------|-------|
| [19]       | X               | -                         | -     |
| [4]        | X               | -                         | -     |
| [9]        | X               | -                         | -     |
| This paper | X               | X                         | X     |

## B. Unified Foundational Ontology (UFO)

UFO [5] is an ontology of foundation that provides a system of categories and relationships, which are based on a set of theories derived from Philosophy, Logic, Language, and Cognitive Psychology. These are formally characterized by means of logical axioms, thus endowing models with a possibility of deriving inferences.

Based on UFO-A and UFO-B, OntoUML provides benefits when modeling knowledge both based on the use of a foundational ontology and ontology engineering. OntoUML presents wide availability of related tools ( e.g. , Menthor ) useful for the verification and validation of the models. Moreover, OntoUML also allows to export of the ontology in the W3C's standard OWL format.

UFO is comprised by three main modules: UFO-A, an ontology related to objects (endurants) ; UFO-B, an ontolgy related to events (perdurants) ; and UFO-C, a social entity ontology which is built on top of UFO-A and UFO-B. UFO is more representative, for example, in relation to binary relations, since it allows a more precise specification, distracting the relations in formal and material [20]. UFO was used as the basis for OntoUML [5], a modeling language whose metamodel is based on ontological properties and possesses a great number of classes, stereotyped relations, and axioms.

## III. OUR APPROACH

RPGs are proven to have a strong potential as a medium for telling interactive stories [21], so we take into account the models proposed in the modeling of RPGs and video games. In addition, the practices from IS and their criteria regarding planning are also considered in this first attempt to incorporate IS planning models [3] [21] to understand the actions and controls. This allows for diversity and depth when players affect histories with their actions. The game world is described by a set of states, which serve as a guideline for the objectives of the entities in the game. Actions, in their turn, trigger state changes and require previous states, so it is possible that, in order to achieve certain state as desired by a character, that character must perform a sequence of actions, i.e., execute a plan [22] [21]. Therefore, our model is expected to be able to cover the adventures and missions found in both tabletop and digital RPG titles.

## A. Methodology

We adopted the following steps of the NeOn Methodology [23]: i) Specification of Ontology Requirements; ii) Reuse and Fusion of Ontological Resources; and iii) Ontology evaluation. Our ontology considers the structure of digital and tabletop RPGs, the supplements and accessories that can be seen as books, magazines, and data that can be computed or represented. This is important so that the ontology allows to extract both information and the relationship of these data in the future. We adopted Competency Questions (CQ) based on the work by Gr¨ uninger and Fox [24], which should be answered, thus providing an initial assessment of the completeness of the ontology: (QC1) What items are being carried by the player? (QC2) What entities are present in a game? (QC3) What actions are necessary to achieve a goal?. The modeling was performed in OntoUML aiming to provide answers to the questions of competence aforementioned reusing ontologies [10] [15].

RPG Metadata covers Planning, System and Scenario. Planning is closely related to Interactive Storytelling (IS) and the narrative, while the system is involved with the mechanics and rules of the game. RPG Systems covers mechanics and rules, including calculations for performing combat maneuvers and character prowess. RPG Planning comprises all elements necessary to represent actions, objectives, and goals, which, in its turn, allows for analyzing and reconstructing narrative elements [21]. Entities are represented within a system as concrete elements of the game universe. In this case, entities are divided into objects, characters, and places. All entities have the characteristic of being able to perform actions and even have plans [25]. In addition, we must observe that Entities inherit the Friend of a friend (FOAF) character relationship model, and there is also the distinction between Player Character (PC) and Non-Player Character (NPC). Moreover, for each entity, there is also a relationship to other entities as place and items. Materials an important addendum to the proposed model. These could be game books, magazines, websites, and forums. These materials have records representing a myriad of elements from both RPG and MMORPG, including systems, scenarios, and even game matches. Match represents the game itself, setting a time to start and end each game. The RPG already have a structure linked to the narrative categorized in: adventure with a central objective that requires a series of actions; a campaign , which can be seen as a large set of adventures that leads to a major outcome or the end of the story/arc for the protagonists. This structure allows to categorize and separate which elements are actually used in a given match.

## IV. EXPERIMENTAL EVALUATION

Two titles were used for experimental evaluation: Ragnar¨ ok Online (RO) 1 is a MMORPG which was already been reviewed in other works [26]. In contrast, Tagmar 2 was chosen because it adopts the tabletop as the supporting technology and its contents are open for a quite active community. In both study cases an initial portion of individuals within the model was used. RO's data were annotated directly from the gameplay and also extracted from the BROWiki website. Similarly, for Tagmar, annotations from gameplay of the two adventures from 'The Temple and the Marriage' were mapped into our ontology. After exporting data from our model simulating individuals found in both games to the OWL format, a total of 2,233 triplets was generated resorting to the Triple-Store Apache Jena Fuseki [27] persistent triple store. This allowed us to both syntactically and semantically validate our ontology using OWL tools. Moreover, SPARQL queries were executed to respond to the previously enumerated competence questions.

## V. CONCLUDING REMARKS

The ontology proposed in this work was built on top of the UFO approach and NeOn methodology, so our model incorporates elements from Interactive Storytelling. As a result, our model is more comprehensive than similar works found in the literature. Finally, practical evaluation using two game titles from the digital and tabletop supports demonstrate how flexible our resulting model is.

Future investigation lines include: adapting our comprehensive semantic model for producing more succinct ontologies directed to specific applications; evaluation within the context of integrating heterogeneous databases of RPG games; and also develop efforts regarding the application our ontology to extract concepts and relations from RPGs played using the play-by-forum electronic support.

## REFERENCES

- [1] T. Berners-Lee, J. Hendler, O. Lassila et al. , 'The semantic web,' Scientific american , vol. 284, no. 5, pp. 28-37, 2001.
- [2] A.-V. Pietarinen, 'Semantic games in logic and epistemology,' in Logic, epistemology, and the unity of science . Springer, 2009, pp. 57-103.

1 http://browiki.org/

2 http://www.tagmar.com.br/

- [3] J. Doran and I. Parberry, 'A prototype quest generator based on a structural analysis of quests from four mmorpgs,' in Proceedings of the 2nd international workshop on procedural content generation in games . ACM, 2011, p. 1.
- [4] B. O. Djuric and M. Konecki, 'Specific owl-based rpg ontology,' in Central European Conference on Information and Intelligent Systems 26th International Conference , 2015.
- [5] G. Guizzardi, 'Ontological foundations for structural conceptual models,' 2005.
- [6] S. Rautenberg, J. L. Todesco, A. V. Steil, and F. A. Gauthier, 'Uma metodologia para o desenvolvimento de ontologias,' RECEN-Revista Ciˆ encias Exatas e Naturais , vol. 10, no. 2, pp. 237-262, 2008.
- [7] R. Studer, V. R. Benjamins, D. Fensel et al. , 'Knowledge engineering: principles and methods,' Data and knowledge engineering , vol. 25, no. 1, pp. 161-198, 1998.
- [8] A. Maedche and S. Staab, 'Ontology learning for the semantic web,' IEEE Intelligent systems , vol. 16, no. 2, pp. 72-79, 2001.
- [9] D. B. Okrea and M. Schatten, 'Defining ontology combining concepts of massive multi-player online role playing games and organization of large-scale multi-agent systems,' in Information and Communication Technology, Electronics and Microelectronics (MIPRO), 2016 39th International Convention on . IEEE, 2016, pp. 1330-1335.
- [10] J. Parkkila, F. Radulovic, D. Garijo, M. Poveda-Villal´ on, J. Ikonen, J. Porras, and A. G´ omez-P´ erez, 'An ontology for videogame interoperability,' Multimedia Tools and Applications , vol. 76, no. 4, pp. 4981-5000, 2016.
- [11] J. Parkkila, T. Hynninen, J. Ikonen, J. Porras, and F. Radulovic, 'Towards interoperability in video games,' in Proceedings of the 11th Biannual Conference on Italian SIGCHI Chapter . ACM, 2015, pp. 26-29.
- [12] J. T. Chan and W. Y. Yuen, 'Digital game ontology: Semantic web approach on enhancing game studies,' in ComputerAided Industrial Design and Conceptual Design, 2008. CAID/CD 2008. 9th International Conference on . IEEE, 2008, pp. 425-429.
- [13] G. O. Trindade, 'Video game development ontology,' Ph.D. dissertation, Universidade Federal do Rio de Janeiro, 2015.
- [14] S. Tang and M. Hanneghan, 'Game content model: an ontology for documenting serious game design,' in Developments in E-systems Engineering (DeSE), 2011 . IEEE, 2011, pp. 431-436.
- [15] O. Sacco, A. Liapis, and G. N. Yannakakis, 'Game character ontology (gco) a vocabulary for extracting and describing game character information from web content,' in Proceedings of the 13th International Conference on Semantic Systems . ACM, 2017, pp. 9-16.
- [16] J. Kritz, E. Mangeli, and G. Xex´ eo, 'Building an ontology of boardgame mechanics based on the boardgamegeek database and the mda framework,' 2017.
- [17] R. Hunicke, M. LeBlanc, and R. Zubek, 'Mda: A formal approach to game design and game research,' in Proceedings of the AAAI Workshop on Challenges in Game AI , vol. 4, no. 1, 2004, p. 1722.
- [18] TMW2, 'The mana world 2 game.' https://tmw2.org/, 2018, acessado em: 2018-07-26.
- [19] M. Roman, I. Sandu, and S. C. Buraga, 'Owl-based modeling of rpg games,' Studia Universitatis Babes-Bolyai , vol. 56, no. 3, p. 83, 2011.
- [20] J. C. Nardi, R. de Almeida Falbo, J. P. A. Almeida, G. Guizzardi, L. F. Pires, M. J. van Sinderen, N. Guarino, and

Figure 1. Overview of the proposed ontology. Some aspects are not shown due to the lack of space.

[FIGURE]

- C. M. Fonseca, 'A commitment-based reference ontology for services,' Information systems , vol. 54, pp. 263-288, 2015.
- [22] E. S. de Lima, B. Feij´ o, and A. L. Furtado, 'Player behavior modeling for interactive storytelling in games,' in Proceedings of SBGames 2016 , 2016, pp. 1-10.
- [21] A. d. O. da Rocha Franco, J. G. R. Maia, and F. A. de Carvalho Gomes, 'A programming framework for autonomous npcs,' Game Engine Gems 3 , 2016.
- [23] M. C. Su´ arez-Figueroa, A. G´ omez-P´ erez, and M. Fern´ andezL´ opez, 'The neon methodology for ontology engineering,' in Ontology engineering in a networked world . Springer, 2012, pp. 9-34.
- [25] A. d. O. da Rocha Franco, J. G. R. Maia, Joaquim Alvino de Mesquita Neto, and F. A. de Carvalho Gomes, 'An interactive storytelling model for non-player characters on electronic rpgs,' in Proceedings of SBGames 2015 , 2015, pp. 33-41.
- [24] M. Gr¨ uninger and M. S. Fox, 'The role of competency questions in enterprise engineering,' in Proceedings of the IFIP WG5.7 Workshop on Benchmarking - Theory and Practice , 1994.
- [26] A. M. M. Santos, A. d. O. da Rocha Franco, J. G. R. Maia, F. A. de Carvalho Gomes, and M. F. de Castro, 'A methodology proposal for mmorpg content expansion analysis.'
- [27] Fuseki, 'Apache jena fuseki,' https://jena.apache.org/documentation/fuseki2/, 2011, acessado em: 2018-07-30.
