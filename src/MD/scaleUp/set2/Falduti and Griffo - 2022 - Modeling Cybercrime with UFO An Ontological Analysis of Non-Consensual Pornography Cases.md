[FIGURE]

## Modeling Cybercrime with UFO: An Ontological Analysis of Non-Consensual Pornography Cases

Mattia Falduti ( B ) and Cristine Griffo ( B )

Free University of Bozen-Bolzano Faculty of Computer Science, Piazza Domenicani 3,

39100 Bolzano, Italy @unibz.it

{ mattia.falduti,cristine.griffo }

Abstract. The legal domain has challenging aspects. One is that legislation is written to regulate an unpredictable number of cases and, therefore, the language of the law is made of open texture and ambiguous terms. Another peculiarity is that each country has its own legislation, often using the common legal expressions but with different meanings. This results in difficulty in understanding supranational cases and in the interoperability of knowledge bases as well. For example, cybercrimes, in particular, image-based sexual abuses (also known as 'revenge porn' or non-consensual pornography) are on the rise globally. Several countries are responding to this social issue by adopting dedicated regulations. However, these regulations are still fragmented, do not share a common conceptualization. In this work, we face these challenges by proposing the application of an ontology-based conceptual modeling to represent a set of concepts and legal relations in cybercrime law. To evaluate the model built, we analyzed the subdomain of cybercrimes, in particular, cases of non-consensual pornography on digital platforms. The result is a conceptualization capable of being shared with other models, increasing the interoperability and clarity of the meaning of common terms and relations found in the various laws studied.

Keywords: Cybercrime · Non-consensual pornography · Legal knowledge representation · UFO-L · Legal ontology

## 1 Introduction

Non-consensual pornography is a recent crime 1 . It consists of sharing in digital platforms nude photos or videos without the consent of the individuals depicted or recorded [9]. Colloquially, this phenomenon is known as 'revenge porn', a highly misleading expression, usually used in the news, with many stigmatising implications for the victim. Sharing intimate images without the consent of the person depicted aims at shaming and humiliating someone, while publicly exposing the most intimate and private sphere of life, obtained in several ways, or digitally generated (deepfake).

1 We point out that, even if the terms 'non-consensual pornography' and 'revenge pornography' have been used in the literature, official documents, and news, the term pornography appears not properly used, because it refers to a particular adult content, legitimate and for mass consumption [32]. We encourage the use of the following terms Non-Consensual Intimate Images (NCII) abuse [29] and Imagebased Sexual Abuse [12] notwithstanding the general public's unfamiliarity with these terms. In this paper, we use the cited terms interchangeably in order to make the content of the article as accessible as possible to all readers.

Unfortunately, data confirms the global reach of the phenomenon and the urgency for providing effective solutions. According to the Italian law enforcement agency [24], only last year there were more than 500 complaints with over 1.400 people accused. This represents an increase of almost 80% as compared to the previous year. Northern countries display even more dramatic figures. According to the UK Police data, in the same year there were 1,185 cases of private multimedia content illegally shared online, while in Germany, the crime of violation of the personal realm by pictures counted 9.233 cases only in 2020 [4]. The UK press suggests that, due to the current pandemic, cases of revenge pornography raised by 329% only in London [34].

Although non-consensual pornography phenomenon is a global concern and several countries have regulated this conduct in their legal systems as crime (e.g. Italy, Germany, France, Denmark, Spain, UK, Australia, Canada, Japan), a shared and portable common knowledge has not been formalized yet. In fact, the phenomenon per se is well defined, but semantic differences arise from different legislation.

A possible solution to the semantic problem in different legislations is the ontological analysis of each one of them and its representation using a common well-founded ontological modeling language. A next step would be the application of some approach of ontology matching, alignment, or correspondence [35]. In this paper, we present the beginning of this process by proposing an ontological conceptualization of the crime. We analyzed the main concepts and relations existing in the non-consensual pornography struggled by legislation of different countries. Then, we applied a well-grounded legal core ontology (UFO-L) [15] to build a domain ontology for the phenomenon of non-consensual pornography.

Once the effects of cybercrimes go beyond the jurisdiction of a country, it is appropriate that information systems of different countries can interact and use the same set of concepts and relations to represent the same phenomenon. This work contributes to extending the body of knowledge by proposing a common conceptualization for the mentioned phenomenon. We believe that this is the first step towards enabling the interoperability of information systems in cybercrime cases.

The paper is organized as follows: Sect. 2 presents a brief summary of the main works on legal ontologies found in the literature; Sect. 3 presents the ontological analysis of the selected cybercrime, emphasizing fragments of legislation from five countries. Based on this ontological analysis, it is presented the ontological representation of the scenario of the non-consensual pornography crime, from the content generation phase, passing through the preparatory actions, and culminating with the crime realization. The preliminary results are presented in Sect. 5 with the application of the model to three real cases. In Sect. 6, we discuss the main results and limitations followed by the final considerations and future works.

## 2 Related Work

Legal knowledge is usually modeled using ontologies. As reported in [21], ontologies can be seen as explicit specifications of conceptualisations and as representations of terminological legal knowledge. As any other domain, the legal knowledge can also be represented at different levels of abstraction. For instance, Core legal ontologies are devoted to formalizing the general aspects of the legal domain, with the main aim of reasoning and inference on general legal concepts. As pointed out in [14], over the previous decades, the field of legal ontologies had seen an increase in the number of papers. The literature on legal ontologies now covers a wide variety of topics and research approaches. One of these topics is represented by legal core ontologies, which had received significant attention since the 1990s.s. However, the heterogeneity of the legal domain has led to the construction of content description models of miscellaneous ontological types. Indeed, at a lower level of abstraction, we find several domain legal ontologies. These are devoted at formalizing concepts and relations featuring a single domain such as civil law, commercial law, data protection and copyrights, international law, European law, public law and criminal law. Legal domain ontologies aim mainly at i) understanding the domain [16], ii) organizing and structuring information for applications/system [6], iii) semantic indexing and information search [7]. The criminal domain has been modeled in several ontologies, but usually with only a national-based and domestic point of view [10].

## 2.1 National Criminal Law Ontologies in the Literature

Regarding the criminal domain, several works have been proposed in different countries. Further details about the mentioned works are described in [10].

The Netherlands. In [2], the authors present the use of various ontologies for the information management of documents produced inside the criminal trial hearings. These ontologies are used in the e-COURT project and cover the Dutch criminal law by following the structure of the LRI-Core ontology [3]. The main aim of this work is to support information retrieval by tagging and annotating the hearing documents.

India. A semantic web-based recommendation system is presented in [30]. The proposed OWL ontology helps legal expert users in extracting court decisions from a case law repository with respect to similar cases. The authors report that the ontology is designed exclusively for that purpose. Indeed, the knowledge represented derives from the Indian Penal Code and an application on murder cases is proposed.

Lebanon. In [13] a criminal ontology defining Lebanese criminal law is formalized in Semantic Web Rule Language (SWRL). Authors modeled this ontology for constructing a legal rule-based decision support system for the criminal domain named CORBS. The system supports legal decision-making with the use of a rule-based reasoning approach. The rule-based decision system contains a set of logic rules composed of atoms, which are defined based on the ontology elements and formalized using SWRL. Authors report that SWRL is used because it is better suited to express deductive knowledge by rules composed of atoms.

USA. [11] presents an ontology engineering methodology and a semi-automated approach of legal ontology generation, both derived from a collection of legal documents. Their model represents semantic information about the USA criminal law. The generation approach also includes legal rules to provide reasoning support to an automatic legal question answering system.

Italy. In [1] an Italian criminal law ontology is described. A UML ontology, based on the Italian crime law, used as a support tool for the judges' activity in the criminal field, is here presented. The ontology formalizes the difference between the criminal behaviours with respect to the offences and to the interests protected by the law, presenting the crime structure as follows: an offender , a behaviour , a penalty and optionally, an event and a coercion .

Tunisia. In [22], the CrimAr ontology for Arabic criminal law is presented. CrimAr is based on the top-levels of LRI-Core ontology [3] and represents all the relevant knowledge in the Arabic legal domain, especially in the criminal matter.

South Korea. [31] presents an ontology for the South Korean criminal law. In particular, this work discusses an ontology-based legal knowledge representation first, and then a logic-based legal rule design methodology, with an application tested on the Korean anti-graft act.

## 3 Ontological Analysis

The ontological analysis started with the study of legislation, followed by the study of real cases. In general, diffusion of personal data is forbidden by data protection regulations. However, these regulations do not always introduce a criminal punishment. Differently, to consider non-consensual pornography as a criminal activity, the introduction of a dedicated criminal law is necessary.

From real-cases, we noticed that media object are usually i) self-taken, i.e. created or shared between partners during a relationship, or ii) stealth-taken, i.e. stolen, obtained without authorization or extorted. The criminal action consists in uploading - and making public - these media on one or more digital platforms, with the intention of diffusing the intimate imagery and abusing the victim.

Analysing the existing criminal legislation we identified three main phases, namely, 1) Content Generation , i.e., the creation of the intimate private media object; 2) Preparatory Action , i.e., the uploading of the intimate private media object; and 3) Crime Realization , i.e., the visualization of these media objects by third parties. This last phase is when the crime is consummated To be more precise, uploading intimate content online, for example, in a chat group, could already be relevant from a criminal perspective. Indeed, this fact can be recognized as an offensive preparation for the crime. On the contrary, uploading an intimate media content on an empty chat group or on a deprecated website, might be realized only a potential offence, maybe irrelevant from a (pure) criminal perspective, but possibly sanctioned with civil law remedies.

According to the European Network of Legal Experts on Gender Equality and Non-discrimination of the European Commission, in 2021 eleven states (Belgium, France, Ireland, Italy, Malta, Netherlands, Poland, Portugal, Spain, Sweden, United Kingdom) have specifically criminalised the non-consensual dissemination/publication/disclosure of intimate/private/sexual images [28]. In the USA, according to a study of the Center for Internet and Society, most of the states have a dedicated legislation. Moreover, Canada, Australia, Israel, New Zealand and Japan have also specifically criminalised the phenomenon. For the sake of space, we mention here some excerpts from the legislation collected 2 .

Belgium. The Article 371/1 of the Belgian Criminal Code, as reported in [25] states that whoever [...] made or caused to be made a visual or audio recording of a person: (i) directly or by technical or other means; (ii) without that person 's authorization or without his or her knowledge; (iii) while the person was nude or engaged in explicit sexual activity ; and (iv) in circumstances in which the person could reasonably be expected not to invade his or her privacy showed, made accessible or disseminated images or the visual or audio recording of a person who is nude or engaged in explicit sexual activity, without his or her consent or without his or her knowledge, even if that person has consented to their production will be punished [...] .

Brazil. 218-C of the Penal Code [26] establishes that it is a crime to offer, exchange, make available, transmit, sell or exhibit for sale, distribute, publish or disseminate , by any means, including through mass communication or computer or telematics system, photography, video or other audiovisual record that contains a scene of rape or rape of a vulnerable person or that makes incitement or induces its practice, or, without the consent of the victim , sex scene, nudity or pornography , setting the penalty of imprisonment from one to five years .

Italy. As pointed out in [5] the Article 612 ter of the Italian Criminal Code states that [...] a person who, after having made or stolen them, sends, delivers, transfers, publishes or disseminates images or videos containing sexually explicit materials , intended to remain private , without the consent of the persons depicted , is liable to be punished [...] .

2 The full content can be accessed at the link https://github.com/mf-thesquare/ NCP legislation.

Malta. Article 208E of the Maltese Criminal Code was introduced in 2016 and it punishes whoever, with an intent to cause distress, emotional harm or harm of any nature, discloses a private sexual photograph or film without the consent of the person or persons displayed or depicted in such photograph or film shall on conviction be liable to imprisonment [...] [8].

## 3.1 Problem Statement

Even if many states have attempted to use existing statutes or created new ones to combat non-consensual pornography, there is no consistent approach, which has led to variable results among states [27]. The legal literature confirms that, for protecting victims efficiently and response with efficacy to this vicious phenomenon, 'the need for a consistent approach is obvious, especially given the borderless nature of the crime '. To move direction consistency, we noticed that legislators are using different terms to express very similar or identical concepts. Examples are the terms photography, video, audiovisual, image, visual, audio, film, recordings for expressing a media content, or nude, explicit sexual activity, pornographic, sexually explicit material, private sexual, sex scene to express the concept of intimate media content. With our knowledge model, we try to systematize the criminal knowledge.

## 4 Model

Analysing the legislation and real-case applications emerging in the literature and in the news, we identified concepts, roles, events and relations. Some concepts were named following the legal literature or the text of the studied laws (e.g. Depicted Person, Perpetrator, Private Intimate Media Object ). Others, however, we harmonize to converge the different terms found in the analyzed laws (e.g. Depicter Person, Publisher, Content Consumer ). Finally, following the UFO-L patterns, we elaborated four main relations, namely i) Right to Privacy of an Intimate Media and ii) Uploading of the Private Media Object, iii) Accessing of the Private Intimate Media and iv) Violation of the Right to Privacy of an Intimate Media. To model these relations, we applied UFO/OntoUML [17] and UFO-L P1-RD-LR legal relator pattern [15]. As we used the OntoUML plugin for Visual Paradigm, colours are set by default according to the stereotypes. For instance, the colour rose for role ; green for relator ; blue for mode .

## 4.1 Legal Roles

We identified several legal roles modeling non-consensual pornography phenomenon. Usually, in sex offenses, the involved subjects are natural persons (see Fig. 1).

Depicted Person in Intimacy: is a person depicted in an intimate media (e.g. photo, video), recognizable from the face or other unique characteristics.

Fig. 1. Legal Roles Taxonomy

[FIGURE]

Depicted Person with Privacy Violated: is a natural person who has his/her privacy violated by means of the uploading or publishing of the media in which s/he is in intimacy.

Constraint 1:Depicted Person with Privacy Violated may not play the role of Depicter Person in the same relation because, in this case, it would be a self-action and, hence, no crime would have occurred.

Depicter Person: is a person able to upload and publish an intimate media. Depicter Person has the duty to keep the privacy of the Depicted Person's intimate media.

Constraint 2: Depicter Person may not play the role of Depicted Person with Privacy Violated in the same relation.

Publisher: the Depicter Person , being in possession of intimate media, becomes a Publisher after uploading it to an Accessible Digital Platform .

Perpetrator: Publisher becomes a Perpetrator with the access to private media by the Content Consumer and the violation of the depicted person's right to privacy.

Constraint 3: In a same relation of Right-Duty to Keep the Intimate Media Object Privately, Perpetrator may not be Depicted Person in Intimacy .

Content Consumer: is one or more third-parties accessing and consuming the private, intimate media content uploaded. If one or more Content Consumer(s) re-upload the private intimate media content, they may become publisher(s) and potentially perpetrator(s).

Constraint 4: in a same relation, Content Consumer may not be Depicted Person with Privacy Violated .

## 4.2 Right to Privacy of an Intimate Media

The legal position right to privacy is represented by applying the legal relator pattern right-duty to an action between Depicted Person in Intimacy and Depicter Person after the publication and entry into force of the criminal law . In the model, Depicted Person in Intimacy is entitled with the right to privacy after the effective publication of the criminal law as well as Depicter Person has the duty to keep Intimate Media Object Privately (see Fig. 2).

Fig. 2. Right-Duty to Privacy

[FIGURE]

Effective Publication of the Criminal Law: is the event, (usually the date) when the legislation that criminalizes the conducts of non-consensual diffusion of intimate imagery is officially published and entries into force. We precise that before the introduction of the criminal law, in some countries, the non-consensual publication of intimate imagery could be forbidden or sanctioned by non-criminal legislation or case law.

Private Intimate Media Object: is any image, videos, or audio with intimate content, both self-created by or stealth-obtained, representing sexual activities, genital regions or female breast. This subkind specializes Media object in terms of content.

Right to Privacy of Intimate Media Object: is the right that Depicted Person in Intimacy may exercise against Depicter Person . Even if there exists a general right to privacy, recognized by various data protection legislation, proper criminal protection against illicit publication comes to light with the Publication of the Criminal Law .

Duty to Keep the Intimate Media Object Privately: is the duty of Depicter Person to keep an intimate media private. This duty comes to light with the Publication of the Criminal Law .

Right-duty to Keep the Intimate Media Object Privately: is the legal relation between Depicted Person in Intimacy and Depicter Person . It is composed by the legal positions Right to Privacy of Intimate Media Object and Duty to Keep the Intimate Media Object Privately , each one inherent in the respective legal roles.

## 4.3 Uploading a Protected Private Media Online

The uploading of the protected private media on a digital platform is the preliminary action before the violation of the right to keep the intimate media private. In our model, Depicter Person is in possession of an intimate private media (e.g. messaging app, an image or a video) and uploads it on an accessible digital platform (e.g. hosting website, or a social media) as shown in Fig. 3. We decided apply the stereotype role to Uploaded Private Intimate Media Object without Consent instead of phase because the UFO-L pattern is built using roles, but we understand that in this case Private Intimate Media Object can have phases (e.g. uploaded media, accessed media, with consent or without consent). In the moment of media uploading, Depicter Person becomes Publisher .

Notwithstanding the crime being consummated with third-party access to uploaded media, the attempt event is also punishable (e.g. to upload the photos, but due to an event beyond the publisher's control, they are not accessible).

Fig. 3. Uploading of a private intimate media online

[FIGURE]

Accessible Digital Platform: is the Digital Platform where the media content can be uploaded or posted and accessed, such as messaging apps, social media, image or video hosting websites and forums.

Private Media Object's Uploading: is the ternary relation between Publisher, Accessible Digital Platform, and the intimate media uploaded without the consent of the Depicted Person. The event Upload Private Media Object to the Digital Platform is run by Publisher and grounds the described relation.

Uploaded Private Intimate Media Object without Consent: is the Private Intimate Media Object without Consent after the end of the uploading event made by Publisher on a Accessible Digital Platform .

## 4.4 Violation of Depicted Person's Right to Privacy

After the uploading, the private intimate media is potentially accessible and visualized by one or more content consumers. This is the first moment when the realization of the crime of non-consensual pornography is complete and, consequently, the right to privacy of the depicted person is violated according to criminal law (Fig. 4). At this moment, Publisher becomes Perpetrator .

Private Intimate Media Accessing: is the intimate media accessed by thirdparties on an Accessible Digital Platform .

Violation of the Depicted Person's Right to Privacy: when an intimate media has been uploaded and accessed/visualized, the privacy of Depicted Person is violated. Therefore, there is a relation between a person, who had the duty to keep private the intimate media and violated it; and the person, who had the right to privacy violated. Both Violated Right to Privacy of an Intimate Media and Violated Duty to Keep Private an Intimate Media , are aspects inherent in Depicted Person with Privacy Violated and Perpetrator respectively.

Accessed Private Intimate Media Object: is the Uploaded Private Intimate Media Object without Consent accessed and visualized by one or more Content Consumer on an Accessible Digital Platform .

## 5 Preliminary Evaluation

We evaluate our model with real cases reported in the news and literature. More in particular, involving two criminal law experts, we ask them to analyse cases and classify the facts. We tested the instantiation of these cases in our model, and we compare the facts' classification performed by the expert and by the model.

Fig. 4. Violation of Depicted Person Right to Privacy

[FIGURE]

## 5.1 Real Cases

Tiziana Cantone. This case was extensively reported in the Italian news [33] and in the criminal literature [5]. The 31-year-old woman caught the public attention due to the viral dissemination of videos of her performing sexual acts, found online from April 2015 on several porn websites, and circulated on the messaging application like WhatsApp. There were also dedicated Facebook pages and groups, and a phrase recorded in the video became a so-called 'meme'. Nonconsensual pornography became a specific criminal offence in Italy in August 2019.

Chrissy Chambers. This case has also been largely reported in the UK news [20] and in the literature [36]. Chrissy Chambers, a famous YouTuber and activist, discovered that people around her received a message saying literally 'Did you know that Chrissy has a porn video on RedTube? [...]' Chambers googled herself and discovered that her ex-boyfriend uploaded between December 2009 and January 2012 seven videos of them having sex to dozens of porn sites, and people had left comments underneath the video. Non-consensual pornography became a specific criminal offence in England in Wales in April 2015.

John Duffin. This case has also been reported in several UK news [18] and discussed in the literature [19]. As described and reported, the John Duffin in 2015 saved an intimate picture of his ex-girlfriend and set it as his WhatsApp profile picture, which allowed all his contacts to view it. Non-consensual pornography became a specific criminal offence in England in Wales in April 2015.

## 5.2 Experts Analysis

The criminal law experts analysed the narratives of the facts. They report that the cases have many facts in common, namely, a female victim, a broken relationship, a perpetrator, an intimate video of the victim, the publication of this video committed by the ex-boyfriend, and the access of these videos by an undefined set of people. However, the first two cases are not relevant from a pure criminal perspective because they occurred before the introduction of criminal legislation. In contrast, the last case occurred after the publication of the legislation criminalizing non-consensual pornography in the UK and therefore, it is recognizable as a crime. Having this expert-based facts classification, we aim at making legal interpretation machine-readable by instantiating roles, concepts and relations, performing a preliminary model classification and comparing it with the expert-based classification.

## 5.3 Model Instantiation and Facts Classification

We instantiated our model with the information extracted (see a fragment in Fig. 5). Considering that the crime of non-consensual pornography is consummated if all events and the roles modeled occur, we first instantiate the events and roles, and then we compared the model and the expert classification of the facts. More in particular, as presented in Fig. 1, the crime phases present different roles of the Natural Person . For example, if the crime is consumed and the ex-partner 1) has taken the picture (is the Depicter Person ), 2) has published the picture online (is the Publisher ) and 3) has made it available for the public (is the Perpetrator ), following the path of the crime, it is possible to instantiate each role with the ex-partner. Differently, if the crime does not reach its last phase or the three action described above are committed by different agents, it is possible to instantiate the model accordingly. Similarly, Private Intimate Media Object assumes the last role of Accessed Private Intimate Media Object (see Fig. 4) when the crime is consumed. With this approach, it is possible to formalize the different phases of the crime and identify each legal roles during the crime evolution, which is mapped through the events.

## 6 Final Considerations

In this paper, we presented a preliminary ontological analysis of non-consensual pornography cases. With this work, we aim at presenting the first step for the process of interoperability of information systems on cybercrimes, in particular, on non-consensual pornography crime. With the proposed conceptualization, we aim also at encouraging effective multinational solutions and cooperation.

Fig. 5. Model Instantiation and Facts Classification (fragment)

[FIGURE]

The benefits of our approach range from the possibility of representing the dynamics of roles and their respective interactions over time. Also, it is possible with this approach to clearly identify the intrinsic aspects of each role in each relation, making it possible to identify the legal positions of each person in each role during the path of crime. This is relevant in the criminal law, as the penalty dosimetry depends on the role each agent played in the crime.

At the same time, we recognize the limits of our approach. Our model does not represent the geographical and temporal evolution of the law. We decided to leave the model temporal and national-agnostic, but we also plan to model the dynamic aspects of the criminal evolution in future works. Furthermore, non-consensual pornography evolves with different and new conducts, such as sextortion , i.e. the threat to distribute intimate materials unless a victim complies with specific demands [23] and cyberflashing , i.e. the act of sending nonrequested obscene images or videos [12]. These conducts present peculiarities that have not been modeled in this preliminary formalization and will also be part of our future work. Moreover, we plan to add to this first representation the knowledge concerning the initial steps of the access to justice, such as victims reports, police investigations, and formal allegations.

## References

1. Asaro, C., Biasiotti, M., Guidotti, P., Papini, M., Sagri, M.T., Tiscornia, D.: A domain ontology: Italian crime ontology. In: Proceedings of the Workshop on Legal Ontologies and Web Based Legal Information Management (LegOnt 2003), pp. 1-7. Edinburgh, UK (2003)
2. Breuker, J.: The construction and use of ontologies of criminal law in the e-Court European project. In: Proceedings of Means of Electronic Communication in Court Administration, pp. 15-40 (2003)
3. Breuker, J., Hoekstra, R.: Core concepts of law: Taking common-sense seriously. In: Proceedings of the 3rd International Conference on Formal Ontologies in Information Systems (FOIS 2004), pp. 210-221. Torino, Italy (2004)
4. Bundeskriminalamt: BKA - Police Crime Statistics. https://www.bka.de/EN/ CurrentInformation/PoliceCrimeStatistics (2022)

5. Caletti, G.M.: Can affirmative consent save 'Revenge Porn' Laws? Lessons from the Italian criminalization of non-consensual pornography. Virginia J. Law Technol. 25 (3), 112-174 (2021)
6. Castano, S., Falduti, M., Ferrara, A., Montanelli, S.: Crime knowledge extraction: an ontology-driven approach for detecting abstract terms in case law decisions. In: Proceedings of the 17th International Conference on Artificial Intelligence and Law (ICAIL19), pp. 179-183. Montreal, Canada (2019)
7. Castano, S., Falduti, M., Ferrara, A., Montanelli, S.: A knowledge-centered framework for exploration and retrieval of legal documents. Inf. Syst. 106 , 101842 (2021). https://doi.org/10.1016/j.is.2021.101842
8. Degiorgio, E.: Criminalising Revenge Porn. Ph.D. thesis, University of Malta (2016)
9. European Institute for Gender Equality: Cyber Violence against Women and Girls. Vilnius, European Institute for Gender Equality (EIGE) (2017)
10. Falduti, M.: Law and Data Science: Knowledge Modeling and Extraction from Court Decisions. Ph.D. thesis, Universit` a degli Studi di Milano (2021)
11. Fawei, B., Pan, J.Z., Kollingbaum, M.J., Wyner, A.Z.: A semi-automated ontology construction for legal question answering. N. Gener. Comput. 37 (4), 453-478 (2019)
12. Fido, D., Harper, C.A.: An introduction to image-based sexual abuse. In: Nonconsensual Image-based Sexual Offending. PSC, pp. 1-26. Springer, Cham (2020). https://doi.org/10.1007/978-3-030-59284-4 1
13. Ghosh, M.E., Naja, H., Abdulrab, H., Khalil, M.: Towards a legal rule-based system grounded on the integration of criminal domain ontology and rules. Proc. Comput. Sci. 112 , 632-642 (2017)
14. Griffo, C., Almeida, J.P.A., Guizzardi, G.: A systematic mapping of the literature on legal core ontologies. In: Proceedings of the 7th Brazilian Symposium on Ontology Research (ONTOBRAS 2015), pp. 79-90, Sao Paolo, Brazil (2015)
15. Griffo, C., Almeida, J.P.A., Guizzardi, G.: Conceptual modeling of legal relations. In: Trujillo, J.C., Davis, K.C., Du, X., Li, Z., Ling, T.W., Li, G., Lee, M.L. (eds.) Conceptual Modeling. LNCS, vol. 11157, pp. 169-183. Springe, Cham (2018). https://doi.org/10.1007/978-3-030-00847-5-14
16. Griffo, C., Almeida, J.P.A., Guizzardi, G., Nardi, J.C.: Service contract modeling in enterprise architecture: an ontology-based approach. Inf. Syst. 101 , 101454 (2021). https://doi.org/10.1016/j.is.2019.101454
17. Guizzardi, G.: Ontological foundations for structural conceptual models. Ph.D. thesis, University of Twente, October 2005
18. Harriet Thurley: Bristol man found guilty of revenge porn against his ex - via WhatsApp. Cosmopolitan (2015)
19. Haynes, J.: Legislative approaches to combating 'revenge porn': a multijurisdictional perspective. Statut. Law Rev. 3 (39), 319-336 (2018)
20. Kleeman, J.: The YouTube star who fought back against revenge porn - and won. The Guardian (2018)
21. Benjamins, V.R., Casanovas, P., Breuker, J., Gangemi, A.: Law and the Semantic Web. Legal Ontologies, Methodologies, Legal Information Retrieval, and Applications. LNCS (LNAI), vol. 3369. Springer, Heidelberg (2005). https://doi.org/10. 1007/b106624
22. Mezghanni, I., Gargouri, F.: CrimAr: A criminal Arabic ontology for a benchmark based evaluation. In: Proceedings of the 21st International Conference on Knowledge-Based and Intelligent Information &amp; Engineering Systems (KES 2017), pp. 653-662. Procedia Computer Science, Marseille, France (2017). https://doi. org/10.1016/j.procs.2017.08.113

23. O'Malley, R.L., Holt, K.M.: Cyber sextortion: an exploratory analysis of different perpetrators engaging in a similar crime. J. Interpers. Violence. 37, 258-283 (2020). https://doi.org/10.1177/0886260520909186
24. Postale, P.: I dati 2021 della Polizia postale. https://www.poliziadistato.it/ articolo/23393
25. Resourcehub: Fighting Domestic Violence - Belgium. Technical report, Bakermckenzie (2021)
26. Rocha, R.L.M., Pedrinha, R.D., de Oliveira, M.H.B.: O tratamento da pornografia de vingan¸ ca pelo ordenamento jur´ ıdico brasileiro. Sa´ ude em Debate 43(spe4), 178189 (2019). https://doi.org/10.1590/0103-11042019s415
27. Roffer, J.: Nonconsensual pornography: an old crime updates its software. Fordham Intellect. Prop. Media Entertain. Law J. 27 (4), 935 (2017)
28. Sara De Vido, Sosa, L.: Criminalisation of gender-based violence against women in European States, including ICT-facilitated violence. Technical report, European network of legal experts in gender equality and non-discrimination, European Commission (2021)
29. Semenzin, S., Bainotti, L.: The use of telegram for non-consensual dissemination of intimate images: gendered affordances and the construction of Masculinities. Soc. Media + Soc. 6 (4), 205630512098445 (2020). https://doi.org/10.1177/ 2056305120984453
30. Shankhdhar, G.K., Singh, V.K., Darbari, M.: Legal semantic web - a recommendation system. Int. J. Appl. Inf. Syst. 7 (3), 21-27 (2014)
31. Pagallo, U., Palmirani, M., Casanovas, P., Sartor, G., Villata, S.: AI Approaches to the Complexity of Legal Systems. AICOL 2015-2017. LNCS (LNAI), vol. 10791. Springer, Cham (2018). https://doi.org/10.1007/978-3-030-00178-0
32. Maddocks, S.: 'Revenge Porn': 5 Important Reasons Why We Should Not Call It By That Name. GenderIt.org (2019)
33. Stephanie Kirchgaessner: Tiziana Cantone: Seeking justice for woman who killed herself over sex tape. The Guardian (2016)
34. Terry, K.: Pandemic fuels 329% rise in revenge porn offences in London: Met Police records 1,185 cases of private snaps and videos illegally shared online in last year - with victims as young as TEN. https://www.dailymail.co.uk/news/ article-10303961/Pandemic-fuels-329-rise-revenge-porn-offences-London-victimsyoung-TEN.html (2021)
35. Trojahn, C., Vieira, R., Schmidt, D., Pease, A., Guizzardi, G.: Foundational ontologies meet ontology matching: a survey. Semant. Web. 1-20 (2021). https://doi.org/ 10.3233/SW-210447
36. V´ eliz, C.: The internet and privacy. In: Edmonds, D. (ed.) Ethics and the Contemporary World, pp. 149-159. Abingdon, UK (2019)
