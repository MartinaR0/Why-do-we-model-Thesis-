## Programming the Nationality Identity in the Federal Constitution of Brazil

```
Rhuan Paulo Lopes Barros 1[0000 -0001 -6349 -9249] , Jos Palazzo Moreira de Oliveira 1[0000 -0002 -9166 -8801] , and Lucian Rocha 2 1 Instituto de Informtica - PPGCC - Federal University of Rio Grande do Sul (UFRGS) PO Box 15.064 - 91.501-970 - Porto Alegre - RS - Brazil { rplbarros, palazzo } @inf.ufrgs.br 2 Universidade do Vale do Rio dos Sinos (UNISINOS) - So Leopoldo - RS - Brazil lucian@slap.law
```

Abstract. Brazil received more than 1 million immigrants and refugees in the last years. With that, doubts naturally arise as to the rights of nationality of these persons and their children in Brazilian territory. So, an ontology was developed that models the Nationality section of Federal Constitution of Brazil in order to provide the realisation of inferences regarding the possibility of a person being Brazilian or not, also infer if the nationality would be Brazilian born or naturalised, besides informing the article and item that support the inference.

Keywords:

Legal Ontology · Constitution · Nationality

## 1 Introduction

It would not be interesting if it were possible to enter a legal question, such as a question concerning the Brazilian nationality, in a search site and, in addition to returning a list of related sites, also a logical answer based on the articles of the laws governing this matter. To present a solution to this problem, we sought to develop a computational legal ontology that would allow the reasoning, to present a logical result and an explanation of the reason for the answer, as well as the legislation that supports the assertion with the use of semantic web technologies [2].

According to Ribeiro, 2019 [7], in recent years Brazil has received more than 1 million immigrants and refugees from countries such as Venezuela and Haiti. Once entering Brazil, foreigners are screened and elucidated about their rights and duties. In the meantime, immigrants may have new questions during their stay as regarding the nationality of a child born in Brazilian territory. In addition, it is possible to spot, by a brief search on search engines for the terms Brazilian nationality, several questions related to the subject in legal forums and blogs.

Copyright c © 2020 for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0). This volume is published and copyrighted by its editors. COUrT - CAiSE for Legal Documents , June 9, 2020, Virtual Workshop.

Thus, it would be highly relevant if it were possible for the citizen to obtain legal information easily and quickly automatically by computational systems. Thus, in the core of applications that answer questions in natural language, there are computational ontologies. This technology allows the development of inferences through computer-modelled knowledge and intelligent information processing [1].

Therefore, this research sought to explore the advantages and limitations of conceptual framework of the legal knowledge contained in the Federal Constitution of Brazil in its article 12 through ontology and semantic web technologies. We developed an ontology that allows us to infer the nationalisation of a hypothetical user as Brazilian born or naturalised person in accordance with the rules of the Brazilian Constitution.

The present study is organised as follows. First is presented concepts related to the Law about the people nationality, after the methodology. Following are shown the development steps and inherent difficulties found. Finally, the conclusion and future works are presented.

## 2 Legal aspects of Brazilian nationality

In the Science of Law, nationality can be understood as the juridical-political bond that binds an individual to a State, making that individual a component of the people of that State, that is, this concept brings us to the idea of belonging of an individual to a particular nation. According to Article 5 of the Universal Declaration of Human Rights 'Everyone has the right to have a nationality'. Therefore, no one will be deprived of the right to be identified as belonging to a particular State.

It is the duty of each State to define the elements that identify its respective nationality, according to its current legal order. As previously explained, such elements can be territorial (eg. individual born in Brazil, will be Brazilian) Jus Solis -, or blood meaning hereditary (individual born from Italian parents will be Italian) Jus Sanguinis . It is possible for a State to adopt both, like Brazil. There are also cases of plurinationality, that is, when the individual, due to the incidence of multiple legal norms that recognise him as a national of some States, has more than one nationality. In a situation of conflict of nationalities, it will, as a rule, be up to Public International Law (international conventions, treaties and agreements) to define which nationality should prevail (eg. place of birth, place of issuing identity, others).

Still, it is important to highlight that nationality' and citizenship' are not synonymous concepts, which is why they should not be confused. Although they are often conditions of possibility, legally speaking, citizenship is linked to the set of political rights and duties of an individual within a territory, e.g. the right to vote and be voted. Therefore, it is possible to be a national without being a citizen and vice versa.

Finally, nationality is divided into two species, namely, original (or primary) and acquired (or secondary). In the first, nationality is legally imposed by the State or by the context of the individual's birth, regardless of his will - the born; the second, in turn, is voluntary and can be acquired through the naturalisation process when the requirements demanded by the State that one wants to belong to are met - the naturalised.

In Brazil, according to article 12, item I, of the Federal Constitution, the original nationals (born Brazilians or Brazilians by birth) are those born in Brazilian territory, even if from foreign parents, as long as they are not in the service of their country Jus Solis ; those born abroad, of a Brazilian father or mother, provided that any one of them is in the service of Brazil Jus Sanguinis ; those born abroad, of a Brazilian father or mother, provided that they are registered with a competent Brazilian office or come to reside in Brazil and choose, at any time, after reaching the age of civilian age - eighteen years -, by Brazilian nationality Jus Sanguinis .

Secondary nationals (naturalised Brazilians), also provided for in Article 12 of the Federal Constitution, in item II, are those who, under the terms of Brazilian law, acquire Brazilian nationality, required of those originating in Portuguesespeaking countries only residing for an uninterrupted year and with a certification of moral integrity; foreigners of any nationality, residing in Brazil for more than fifteen years without interruption and without criminal conviction, as long as they require Brazilian nationality.

In the infra-constitutional order, the Migration Law (Federal Law No. 13,445, of May 24, 2017), in its article 64, brings other modalities for foreigners to become naturalised Brazilian, namely: ordinary naturalisation; extraordinary naturalisation; special naturalisation; or provisional naturalisation. Each hypothesis has its own and distinct requirements of the Federal Constitution for secondary acquisition of Brazilian nationality, which, however, will not be deepened, since they are outside the scope of this work, which is limited to a constitutional analysis of the problem.

## 3 Methodology

We developed the research in such a way that it can be reproduced or expanded by law students, i.e. researchers who do not hold prior technical knowledge in the area of Information Technology, as formal logic, programming techniques or computational modelling. Thus, we used a simplified methodology based on Chungoora, D.T., 2006 [3]. This methodology is intended to be accessible to beginners, which is composed of the following phases: Definition of objective and scope; Knowledge capture and elucidation; Initial Structure; Formalisation; Deployment; Evaluation.

In addition, we tracked the management of ontology requirements, as well as the terms discovered through spreadsheets. Various mind maps were also used to assist in the elucidation of knowledge. This material used proved to be of great Rhuan P. L. Barros. et al.

value because mind maps present knowledge modelled using the most important terms and related items by means of arrows.

## 4 Development

The development of ontology started by Requirements Management, trying to understand what is the need for future users. Thus, the user's need was established Know if a person is Brazilian or not according to the rules of the Constitution and receive information about the articles that support the answer. From this, the following requirement was defined: Verify if a person fulfils Brazilian nationality requirements using informed data. Then this requirement was divided into two atomic units:

- -Inform if the person meets the Brazilian born nationality requirements using reported data.
- -Verify if the person meets the naturalised Brazilian nationality requirements using informed data.

## 4.1 Class modeling

In the Knowledge Capture and Elucidation phase, it was firstly worked the pure text of the Federal Constitution for the marking of important terms, according to part of speech. In general, nouns can be identified as individuals or classes if we abstract, verbs already indicate relationships. In fact, the suggestion of the chosen methodology was to facilitate the identification of relationships by directly observing verbs and nouns. However, if there was been followed to the letter, we would have had some modelling problems. So it was needed to expand the relationship markings for all words that express they did action, like some participles and nouns. In addition, they were also marked numerals for expressing important information for this modelling, although not be included as guidance in the chosen methodology.

Therefore, the diagram of the final ontology created directly expresses the existing types of Brazilian nationality. Also, some classes that are not found directly in the text of the law, however, they are known by the doctrine and found in [6]. For example, Jus Solis, which represents the concept of nationality law allusive to the birth of the individual according to where he was physically born, in this case, the Brazilian territory. Also included was the class Jus Sanguinis which says respect for the principle of law granting nationality according to nationality of the citizen's parents, as a subclass of the class Brazilian Nationalised. Thus, the Federal Constitution describes eight ways of obtaining nationality a class was created for each one of them, which are at the tip of the branches in Figure 1.

Programming the Nationality Identity in the Federal Constitution of Brazil

Fig. 1. Final version of visual modelling with OntoUML in the Menthor app

[FIGURE]

## 4.2 Individual modeling

The ontology was structured aiming at the creation of individuals who represent the data entered by the user in their question. These individuals inserted in ontology would be automatically classified by the Reasoner as belonging to one of the classes representing nationality if the reported properties are enough to be classified as such. If the properties are not sufficient, the Reasoner would not classify it in any class. Each of these subclasses created, contains rules written using Protg's Class expression editor. Thus, it was necessary to extract from the text of the law all possible variables to be used in cases of inference of nationality.

Therefore, we modelled some individuals who represent questions from users of the ontology with the corresponding property values. Also included were the properties of Brazilian mother, Brazilian father, Mother service, and Father service because they provide important information to infer the only case of exception to the Jus Solis principle in the Federal Constitution, namely the the case of a person born in Brazilian territory to a foreign father and mother (both) and father and mother (both) in the service of their country, for example, an ambassador.

In this case, the first attempt was to model the general rule and the exception by from the Class expression editor. However, Reasoner could not work with the exception because of the Open World Assumption (OWA) [4]. OWA is a Semantic Web principle that assumes that what is not modelled in ontology is simply unknown. Thus, it is not possible for Reasoner make inferences about exceptions, because exceptions can be many things if each one is not modelled.

Finally, to facilitate the creation of the logical expression, it was created a truth table that includes all the variables involved and their possibilities of values, true or false. In this way, 5 variables are analyzed, being the variable 'Born' necessarily true in case of Jus Solis were true, there is 2 4 possibilities, i.e. 16 logic described, minus the case of the exception.

## 5 Conclusion

An ontology has been developed that models the Nationality section of the Federal Constitution of Brazil in order to provide the realisation of inferences of individuals representing a case of a person in relation to the possibility of this person is Brazilian or not, as well as inferring whether nationality would be Brazilian or naturalised, in addition to informing the article and item supporting the inference. In this way, this ontology can be used to solve doubts related to the Brazilian nationality of an individual. To evaluate the quality and effectiveness of the created ontology, specific cases were created simply for testing purposes. Thus, previously saved questions were modelled in the format of an individual and inferences were made.

On the other hand, the main advantage of developing a system that infers a person has Brazilian nationality through a ontology is to expand it in the future to answer other questions. If this were not the case, it would be easier and faster to program all possibilities directly in some software with its own programming language.

However, the use of ontologies for the development of software that answer questions is promising because as search systems become more complete in relation to the use of semantic web standards, in the future they will be able to explore these ontologies automatically in their result pages. It would be possible for survey site users to receive answers to questions in the own results pages based on ontologies made available on websites. As future work, it would be interesting to integrate ontology in a semantic search engine that provides access to ontology through web services to the implementation of ontology in a web page so that it can be accessed by the public on the internet. In addition, the expansion of ontology through the use of cool modelling with LKIF [5] would allow its expansion and reuse by other systems on the web.

## References

1. Benjamins, V.R., Casanovas, P., Breuker, J., Gangemi, A.: Law and the semantic web: legal ontologies, methodologies, legal information retrieval, and applications, vol. 3369. Springer (2005)
2. Berners-Lee, T., Hendler, J., Lassila, O., et al.: The semantic web . Scientific american 284 (5), 28-37 (2001)
3. Chungoora, D.T.: Practical knowledge modelling, https://www.udemy.com/practical-knowledge-modelling/learn/lecture/2803056
4. Drummond, N., Shearer, R.: The open world assumption. In: eSI Workshop: The Closed World of Databases meets the Open World of the Semantic Web. vol. 15 (2006)
5. Hoekstra, R., Breuker, J., Di Bello, M., Boer, A., et al.: The lkif core ontology of basic legal concepts. LOAIT 321 , 43-63 (2007)
6. Rego, T.: Mapas e questes para concursos. Direito Constitucional. Mapasequestoes.com.br (2011)
7. Ribeiro, V.: Brasil j recebeu 1,1 milho de imigrantes e 7 mil refugiados (2019), http://agenciabrasil.ebc.com.br/direitos-humanos/noticia/2019-01/brasilja-recebeu-11-milhao-de-imigrantes-e-7-mil-refugiados
