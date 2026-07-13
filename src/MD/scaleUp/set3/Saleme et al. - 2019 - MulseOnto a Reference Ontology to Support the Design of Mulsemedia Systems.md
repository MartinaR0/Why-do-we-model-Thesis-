Journal of Universal Computer Science, vol. 25, no. 13 (2019), 1761-1786 submitted: 1/5/19, accepted: 28/10/19, appeared: 28/12/19  J.UCS

## MulseOnto: a Reference Ontology to Support the Design of Mulsemedia Systems

## Estˆ ev˜ ao B. Saleme

(Federal University of Esp´ ırito Santo, Brazil estevao.saleme@ieee.org)

## Celso A. S. Santos

(Federal University of Esp´ ırito Santo, Brazil saibel@inf.ufes.br)

## Ricardo A. Falbo

(Federal University of Esp´ ırito Santo, Brazil falbo@inf.ufes.br)

## Gheorghita Ghinea

(Brunel University London, UK george.ghinea@brunel.ac.uk)

## Frederic Andres

(National Institute of Informatics, Japan andres@nii.ac.jp)

Abstract: Designing a mulsemedia-multiple sensorial media-system entails first and foremost comprehending what it is beyond the ordinary understanding that it engages users in digital multisensory experiences that stimulate other senses in addition to sight and hearing, such as smell, touch, and taste. A myriad of programs that comprise a software system, several output devices to deliver sensory effects, computer media, among others, dwell deep in the realm of mulsemedia systems, making it a complex task for newcomers to get acquainted with their concepts and terms. Although there have been many technological advances in this field, especially for multisensory devices, there is a shortage of work that tries to establish common ground in terms of formal and explicit representation of what mulsemedia systems encompass. This might be useful to avoid the design of feeble mulsemedia systems that can be barely reused owing to misconception. In this paper, we extend our previous work by proposing to establish a common conceptualization about mulsemedia systems through a domain reference ontology named MulseOnto to aid the design of them. We applied ontology verification and validation techniques to evaluate it, including assessment by humans and a data-driven approach whereby the outcome is three successful instantiations of MulseOnto for distinct cases, making evident its ability to accommodate heterogeneous mulsemedia scenarios.

Key Words: mulsemedia systems, reference ontology, multimedia Category: H.5.1, L.1.3

## 1 Introduction

Continuous advances in technology have enabled the use of mulsemedia to build more immersive experiences for users. Not only do they engage the senses of sight and hearing in this kind of experience, they can also have involvement with artificially produced sensory effects such as scent, vibration, and flavor [Ghinea et al., 2011, Ghinea et al., 2014]. However, building a mulsemedia system entails weaving multiple technologies to connect different entities, distribute the sensory signals, and render sensory effects appropriately, as described in [Waltl et al., 2013, Kim et al., 2013, Luque et al., 2014, Saleme and Santos, 2015, Jalal et al., 2018, Wanick et al., 2018, Saleme et al., 2019b].

The concept of mulsemedia along with the interactions and inter-relationships between applications, types of sensory effects, and devices in this domain are indeed complex to understand and frequently not so clear-cut because of its heterogeneous digital ecosystem [Covaci et al., 2018, Saleme et al., 2019a, Saleme et al., 2019c]. Despite existing standards, tools, and recent research devoted to mulsemedia, there is still a lack of formal and explicit representation for mulsemedia, which may cause a failure to understand it adequately. Misconception might eventually lead to a weak arrangement of how to manage and integrate a plethora of entities. As a result, stakeholders may overlook relevant design aspects such as standardization [Yoon et al., 2015], reuse, and compatibility, to name but a few design features.

In light of this, capturing the common conceptualization underlying this type of systems is rather important to understand and improve the mulsemedia digital ecosystem by integrating information from varied sources, reducing ambiguity and inaccuracy when interpreting shared information. One way to represent a shared conceptualization is through the use of ontologies. They bring together a shared understanding of a domain that can be communicated between humans and also computers [Guarino, 1995]. Ideally, first, the structure of the domain conceptualization must be made available to humans through an explicit and formal description of the corresponding portion of reality in terms of a domain reference ontology . A reference ontology should be constructed with the sole objective of making the best possible description of the domain in reality, for the purposes of communication, learning and problem-solving. Once a reference ontology is built, an operational version of it (said an operational ontology ) can be designed and implemented to be processed by machines.

It is noteworthy that there is a subtle difference between the concept of mulsemedia and digital multisensory experiences. Whilst the latter involves more than one human sense in a digital experience, the former requires sight and hearing added to at least another human sense such as smell, taste, and touch. Therefore, when users are experiencing mulsemedia, there is a clue-multimedia plays a role in it-in contrast with other digital multisensory experiences that eventually might not be linked necessarily to multimedia and thus have different challenges.

In this paper, we refreshed a domain reference ontology on Mulsemedia Systems presented by [Saleme et al., 2018], named MulseOnto. It chiefly encompasses the understanding of what mulsemedia systems and their small parts are, which entities they interact with, where the sensory effects come from, and what physical realizations different kinds of media do in this context, therefore providing a big picture of mulsemedia systems. By building this ontology, we propose to establish a common conceptualization about mulsemedia systems to address purposes such as understanding the interrelationship between their entities, describing a common vocabulary for knowledge workers in this domain, certifying that stakeholders are talking over the same concepts when making mulsemedia solutions, and fostering this 'novel' field.

To evaluate MulseOnto, we have applied an approach for verifying the concepts and relations, including assessment by humans and a data-driven approach. Aside from the work of [Saleme et al., 2018] who described a hypothetical scenario as MulseOnto's instance, we selected three varied mulsemedia systems to be instances of the ontology to find out whether it is able to describe real-world situations. The results showed that this ontology can be used as a consensual conceptual model for exploring the knowledge about the whole chain of mulsemedia systems.

This work is organized as follows. Section 2 brings the main concepts on mulsemedia used to support the ontology and presents related work. Section 3 presents MulseOnto, including the questions it aims to answer and the relationship between its entities. Section 4 discusses how the ontology was evaluated and depicts instances of the ontology through real-world situations. Finally, Section 5 concludes the paper and leads to future works.

## 2 Background and Related Work

[Ghinea et al., 2014] stated that multimedia applications are usually composed of more than two different digital media and almost exclusively bisensorial (sight and hearing) by nature, whereas mulsemedia refers to applications that also engages at least other three primary senses (smell, taste, and touch). Hence, multimedia and also mulsemedia refer to the use of multiple media, but it is necessary to take into account what the meaning of media is. The problem with terminology in mulsemedia starts with the misunderstanding of the concept of media due to the use of this term with different meanings in different contexts.

## 2.1 Meaning of Media

[Heller and Martin, 1995] proposed a media taxonomy consisting of two dimensions. The first one is related to the well-known existing media types (text, graphics, sound, and motion) and the second one, to the continuum between concrete and abstract expression of each medium. The authors consider that media types can only provide information in aural or visual forms.

[Roy and Zeng, 2015] are particularly interested in multimedia content shared within a social network. They acknowledged that the term media is often used in a broad sense and usually related to the nature of information perceived by humans. Indeed, the authors consider that, in multimedia communication, media are delivered through presentation spaces (e.g. screen, speakers, projector) with presentation attributes (e.g. color, intensity, font) to address the primary human senses. A presentation space includes specialized output devices and can have one or more dimensions (e.g. a computer monitor has two space dimensions, while holography has three ones).

Regarding the time dimension of its presentation space, a medium is classified as discrete or continuous [Steinmetz and Nahrstedt, 1995]. The first one is composed of time-independent information units, whereas the second one requires a continuous play-out of its information units in time. The time-dependency between the information units of a continuous medium establishes the semantics of this kind of content.

## 2.2 Multimedia Concepts

Starting from a conventional view, [Roy and Zeng, 2015] initially defined multimedia as 'the use of a variety of communicative media (i.e., information intended for human consumption), including text, audio, visual, and haptic data.' Authors also stated that multimedia integrates signals from our primary senses in an attempt to generate a coherent perceptual experience for the users. Afterward and agreeing with [Chang, 2013], the authors claim that the definition of multimedia has been extended to be much broader and more inclusive, covering a wide spectrum of multimedia applications, going far beyond the conventional audiovisual contents to, for instance, mulsemedia applications.

In an attempt to address the issue of creating a unified terminology for the multimedia domain, [Bordegoni et al., 1997] brought not only one but also two definitions of the medium term. The first definition considers a medium as being a certain physical space in which perceptible entities are realized, concentrating on human sensory receptors and derived sensations. As there are different types of perceptible entities (visual, auditory, haptic, gustatory, and olfactory), one may use these terms for making a distinction between media too. In the second definition, medium designates a certain type of information and/or the representation format in which information is stored.

## 2.3 Demystifying Mulsemedia

Using the two definitions of medium proposed by [Bordegoni et al., 1997], mulsemedia could be characterized as: (i) a common physical space in which different perceptible entities can be realized, being two of them, at least, visual and audible entities and the others, haptic, gustative or olfactive ones; or (ii) a composition of basic media types with one or more haptic, gustative or olfactive sensory effects. This composition is characterized by additional properties, such as temporal relationships between the involved media and sensory effect, the expected presentation's behavior, user preferences, etc.

Media content can be directly created by humans (e.g. this paper, pictures, songs), acquired through various sensors (e.g. camera, microphone, motion capture) that capture real-world information, or synthesized using computers (e.g. a virtual 3D space in a game). The sensory effects are usually synthesized. Though haptic effects can be captured, recording taste and smell from the real world remains a great challenge [Danieau et al., 2013].

After media content and sensory effects data have been created, they are usually coded for transmission or storage generally using a standard (e.g. MPEG-4 and AV1 for videos, and MPEG-V [Yoon et al., 2015] or recently NCL [Josu´ e et al., 2018] for sensory effects). Although the mulsemedia ecosystem should take into consideration issues involving all of these phases, in this paper, we are concentrated only on authoring and presentation phases.

During the so-called authoring phase (Figure 1), media, sensory effects, and additional presentation properties are linked together in a mulsemedia composition [de Amorim et al., 2019]. In this phase, if the author is a human, something abstract that exists only in the author's mind must be transformed into a mulsemedia content; if the author is a computer system, an explicit representation of the information content (e.g. video from surveillance cameras, automatic caption from automatic speech recognition, etc.) must be provided.

Mulsemedia contents are represented in a format that is not directly presentable to humans. Hence, for each medium and sensory effects, it must always exist a dedicated physical device that is able to produce perceptible entities. In other words, devices have a function of rendering each mulsemedia content to the human senses. Moreover, the authored content establishes an expected behavior of the presentation through a set of presentation commands and/or constraints, which usually include references to mulsemedia data together with the purposes of engagement, immersion, flow assessment, and so on. Both constraints and commands are assumed to be defined outside the presentation system.

Devices for delivering visual, auditory, and haptic experiences have reached a fairly advanced stage of maturity, whereas olfactory and gustatory, are relatively newcomers. In this fashion, it is worth highlighting the work of [Hariri et al., 2016], who aimed at stimulating the sense of smell by using electric to improve the processes of multimedia annotation and retrieval from databases. Although it is not a mulsemedia ontology, it is related to this work in the sense that it can be referred to how emotion can be captured. It could be combined with MulseOnto in future works to help to explain the emotions from mulsemedia experiences.

[FIGURE]

[FIGURE]

The ontology of [Naravane and Lange, 2017] refers to organoleptic properties to the consumption of food. They argue that organoleptic, as well as biological, chemical, and physical, is a class of phenotypic properties resulting from the intersection of them. Thereby, the authors focus on the details of all possible organoleptic traits of an edible substance. The ontology has several classes of stimuli related to the sensory reaction like appearance, touch, smell, taste, and sound, whereas the sensory ontology presented in this work focus on the knowledge about the detection of the stimulus and subsequent recognition and characterization of it. As the work of [Horvat et al., 2014], it could be a complementary work towards the perception of the senses produced by mulsemedia systems. However, this is out of the scope of our work in this paper. Furthermore, the perception of the senses might not be the same when combining different sensory effects and is very dependent on the user's Quality of Experience (QoE) [Mesfin et al., 2019].

Following the same way of the aforementioned work, [Albert et al., 2017] present an ontological representation of sensory perception knowledge. However, they go deeper in detail on specifications for haptic perceptions with the proposition of generic elementary haptic sensations. This focus also does not allow stakeholders to perceive the mulsemedia environment as a whole because of its particular addressing. Moreover, as well as the work of [Naravane and Lange, 2017], the sense of QoE seems to be out of its scope.

As far as mulsemedia systems ontology, this research did not find studies dealing with it so far-to the best of our knowledge.

## 3 Mulsemedia Systems Reference Ontology

Our reference ontology on Mulsemedia Systems, called MulseOnto, predominantly incorporates the comprehension of what mulsemedia systems and their small parts are, which entities they interact with, where the sensory effects come from, and what physical realizations different kinds of media do in this context, thus providing a big picture of mulsemedia systems. It does not intend to answer how they affect the QoE of users, how stimuli are perceived by users, how devices produce each sensory effect, how media are loaded, composed and presented in mulsemedia systems, how mulsemedia systems manage timing aspects, or how users set up systems and devices within an interactive environment. Moreover, attribute details such as computer media extensions, encoding methods for computer medium, kinds of flavors or scent, the intensity of effects, temporality constraints, colors, and/or in-depth particulars do not take place in this ontology.

To develop MulseOnto, we adopted SABiO, a Systematic Approach for Building Ontologies [Falbo, 2014]. We chose SABiO because it has been successfully used to develop domain ontologies, in particular, Software Engineering reference domain ontologies. SABiO's development process comprises five main phases, namely: (i) Purpose Identification and Requirements Elicitation; (ii) Ontology Capture and Formalization; (iii) Design; (iv) Implementation; and (v) Test. These phases are accompanied by supporting processes, such as knowledge acquisition, reuse, documentation, and evaluation. SABiO aims at developing both reference ontologies (phases i and ii) and operational ontologies (phases iii, iv and v). In this work, we are interested in building only a domain reference ontology; thus we performed only the first two phases, namely the main results produced, followed by how we have evaluated MulseOnto, both of which are discussed next.

## 3.1 MulseOnto Requirements

Analogously to requirements in Requirements Engineering, ontology requirements can be functional and non-functional. Functional requirements refer to the ontology content and can be specified as Competency Questions (CQs). CQs are questions that the ontology should be able to answer [Gruninger and Fox, 1995]. They help to refine the scope of the ontology and are used in the ontology verification process to check whether the ontology elements (concepts, relations, and properties) are able and sufficient to answer the CQs [Falbo, 2014]. MulseOnto should be able to answer the following CQs:

- CQ01 . What is a mulsemedia computer system?
- CQ02 . What is a mulsemedia software system?
- CQ03 . What do mulsemedia programs handle?
- CQ04 . What is a user interface in a mulsemedia computer system?
- CQ05 . What are the most common classes of output devices in mulsemedia computer systems?
- CQ06 . What is a medium?
- CQ07 . Which creation works does a medium realize?
- CQ08 . What are the types of media typically present in mulsemedia computer systems?
- CQ09 . What is a sensory effect description?

- CQ10 . What are the most common classes of sensory effect descriptions in mulsemedia computer systems?

Ontology non-functional requirements, in turn, refer to the characteristics, qualities, and general aspects not related to the ontology content [Suarez-Figueroa et al., 2012]. The following non-functional requirements were defined for MulseOnto:

- NFR01 . MulseOnto should be integrated into the Software Engineering Ontology Network (SEON) [Ruy et al., 2016], reusing its parts that cover aspects related to the mulsemedia domain.
- NFR02 . MulseOnto should be developed in a modular way, allowing addressing this complex domain in an iterative fashion, focusing on different concerns.

Concerning NFR01 , SEON is an ontology network for the Software Engineering domain, which is organized in layers [Ruy et al., 2016]. At its uppermost layer, there is the Unified Foundational Ontology (UFO). UFO is a foundational ontology that is based on a number of theories from Formal Ontology, Philosophical Logics, Philosophy of Language, Linguistics and Cognitive Psychology [Guizzardi et al., 2015]. At the core layer, there are core ontologies on software (Software Ontology-SwO [Duarte et al., 2018]) and software process (Software Process Ontology-SPO [Bringuente et al., 2011]). MulseOnto is a domain ontology included in SEON's domain layer, by extending both SwO and SPO.

For addressing NFR02 , the current version of MulseOnto is divided into four sub-ontologies, namely: (i) Mulsemedia System sub-ontology, which focuses on what a mulsemedia system is, addressing competency questions CQ01 to CQ04; (ii) Output device sub-ontology, which relates to the classification of mulsemedia output devices (CQ05); (iii) Medium sub-ontology, which refers to types of media used in mulsemedia systems (CQ06 to CQ08); and (iv) Sensory Effect Description sub-ontology, which regards the types of sensory effects descriptions used in mulsemedia systems (CQ09 and CQ10). Figure 3 presents a UML package diagram, showing the sub-ontologies that comprise MulseOnto and the relationships between them. The dependencies between the sub-ontologies indicate that concepts and relations from a sub-ontology are used by the dependent sub-ontology.

In the following subsections, MulseOnto sub-ontologies are presented. Concepts reused from SPO are shown in blue, preceded by its acronym (SPO::); concepts from SwO are shown in green, preceded by its acronym (SwO::); concepts from UFO are shown in gray, preceded by its acronym (UFO::).

[FIGURE]

[FIGURE]

[FIGURE]

[FIGURE]

[FIGURE]

## 4.1 Competency Questions Verification

For verifying MulseOnto, we analyzed if its concepts and relations are able to answer the competency questions. Furthermore, by performing this step, it is also possible to identify whether there are elements besides the point, particularly those that do not play a part in answering the questions. The following frames show which elements of the ontology account for each competency question in terms of concepts, relations, and properties.

Competency Question CQ01 . What is a mulsemedia computer system?

```
Mulsemedia Computer System subtype of Computer System ; Mulsemedia Computer System composed of Medium ; Mulsemedia Computer System composed of Sensory Effect Description ; Mulsemedia Computer System composed of Behavior Presentation Specification ; Mulsemedia Computer System composed of User Interface ; Mulsemedia Computer System has Loaded Mulsemedia Software System Copy ; Loaded Mulsemedia Software System Copy materialization of Mulsemedia Software System .
```

Competency Question CQ02 . What is a mulsemedia software system?

```
Mulsemedia Software System subtype of Software System ; Mulsemedia Software System constituted of Mulsemedia Program .
```

Competency Question CQ03 . What do mulsemedia programs handle?

```
Mulsemedia Program handles Computer Medium ; Mulsemedia Program handles Sensory Effect Description ; Mulsemedia Program handles Behavior Presentation Specification .
```

Competency Question CQ04 . What is a user interface in a mulsemedia computer system?

```
User Interface composed of Input Device ; User Interface composed of Output Device ; User Interface related to Loaded Mulsemedia Program Copy ; Loaded Mulsemedia Program Copy materialization of Mulsemedia Program ; Loaded Mulsemedia Software System Copy includes Loaded Mulsemedia Program Copy .
```

Competency Question CQ05 . What are the most common classes of output devices in mulsemedia computer systems?

```
Visual Output Device subtype of Output Device ; Auditory Output Device subtype of Output Device ; Haptic Output Device subtype of Output Device ; Olfactory Output Device subtype of Output Device ; Gustatory Output Device subtype of Output Device ; Screen Output Device subtype of Visual Output Device ; LED Lighting Output Device subtype of Visual Output Device ; Lightbulb Output Device subtype of Visual Output Device ; Projector Output Device subtype of Visual Output Device ; Holographic Output Device subtype of Visual Output Device ; Head-Mounted Display Output Device subtype of Visual Output Device ; Box Speaker Output Device subtype of Auditory Output Device ; Headphone Output Device subtype of Auditory Output Device ; Earbud Output Device subtype of Auditory Output Device ; Rumble Output Device subtype of Auditory Output Device ; Motion Chair Output Device subtype of Haptic Output Device ; Temperature Output Device subtype of Haptic Output Device ; Spraying Output Device subtype of Haptic Output Device ; Wind Turbine Output Device subtype of Haptic Output Device ; Vibration Output Device subtype of Haptic Output Device ; Scent Diffuser Output Device subtype of Olfactory Output Device ; Electric Smell Interface Output Device subtype of Olfactory Output Device ; Lollipop Output Device subtype of Gustatory Output Device ; Beverage Output Device subtype of Gustatory Output Device .
```

Competency Question CQ06 . What is a medium?

```
Medium subtype of Object ; Medium realizes Creation Work .
```

Competency Question CQ07 . Which creation works does a medium realize?

```
Medium realizes Creation Work ; Graphic Medium realizes Text ; Graphic Medium realizes Picture ; Motion Medium realizes Text ; Motion Medium realizes Picture ; Motion Medium realizes Sound ; Motion Medium realizes Motion Picture ; Audio Medium realizes Sound ; Text subtype of Creation Work ; Picture subtype of Creation Work ; Sound subtype of Creation Work ; Motion Picture subtype of Creation Work .
```

Competency Question CQ08 . What are the types of media typically present in mulsemedia computer systems?

```
Computer Medium subtype of Medium ; Computer Medium stored in Hardware Equipment ; Directly Transmitted Medium subtype of Medium ; Directly Transmitted Medium captured by Hardware Equipment ; Discrete Medium subtype of Computer Medium ; Continuous Medium subtype of Computer Medium ; Text Medium subtype of Discrete Medium ; Graphic Medium subtype of Discrete Medium ; Motion Medium subtype of Continuous Medium ; Audio Medium subtype of Continuous Medium .
```

Competency Question CQ09 . What is a sensory effect description?

Mulsemedia Program handles Sensory Effect Description ; Sensory Effect Description subtype of Data File .

Competency Question CQ10 . What are the most common classes of sensory effect descriptions in mulsemedia computer systems?

Prompt Sensory Effect Description subtype of Sensory Effect Description ; Lingering Sensory Effect Description subtype of Sensory Effect Description ; Light Sensory Effect Description subtype of Prompt Sensory Effect Description ; Vibration Sensory Effect Description subtype of Prompt Sensory Effect Description ; Spraying Sensory Effect Description subtype of Prompt Sensory Effect Description ; Kinesthetic Sensory Effect Description subtype of Prompt Sensory Effect Description ; Tactile Sensory Effect Description subtype of Prompt Sensory Effect Description ; Wind Sensory Effect Description subtype of Lingering Sensory Effect Description ; Scent Sensory Effect Description subtype of Lingering Sensory Effect Description ; Taste Sensory Effect Description subtype of Lingering Sensory Effect Description ; Temperature Sensory Effect Description subtype of Lingering Sensory Effect Description ; Fog Sensory Effect Description subtype of Lingering Sensory Effect Description .

## 4.2 MulseOnto Instantiation

In accordance with SABiO [Falbo, 2014], we validated whether MulseOnto is capable of representing real-world cases besides the hypothetical mulsemedia scenario presented in [Saleme et al., 2018]. Therefore, we instantiated three distinct cases:

1. an off-the-shelf mulsemedia system [Saleme and Santos, 2015]; 2. a mulsemedia system for vehicles [Kim et al., 2013];
3. a wearable VR-based mulsemedia system [Ranasinghe et al., 2018].

In order to portray these instantiations, a brief description of each mulsemedia environment is presented next, along with object diagrams to refer to the classes of MulseOnto. Then, the diagrams are further explained. The relations in the diagrams are named, however, we suppressed them for part-whole ones in order to have neater models.

## 4.2.1 Off-the-shelf Mulsemedia System

Created by [Saleme and Santos, 2015], this work presents a platform that comprises a video player (SE Video Player) and a mulsemedia renderer (SE Renderer) for delivering sensory effects in a desktop setting. This mulsemedia system is comprised of a mini PC where the mulsemedia renderer runs, another computer to reproduce audiovisual content along with a computer screen, a LED strip light, to present lighting effects, a vibration motor, to deliver vibration, and two wind fans, to blow air towards the user. Moreover, an Arduino microcontroller runs a module for controlling devices. Despite supporting audiovisual content Mulsemedia Vehicle is a Mulsemedia Computer System composed of Wind Metadata , Vibration Metadata , a Ski Jump Video , a Ski Jump Audio , a Cavalry Charges Video , a Cavalry Charges Audio , a User's Computer , a Command Transmitter Device , and a Mulsemedia Vehicle User Interface . The latter is composed of a User's Computer Screen , A Wind Fan , A Heating Fan , A Vibrator , and A LED Light . The media previously mentioned realize creation work (motion picture and sound) and are handled by SMCS which is a mulsemedia program that also handles sensory effects descriptions such as Wind Metadata and Vibration Metadata . Furthermore, both descriptions are handled by SMURF , another mulsemedia program. Their loaded counterparts Loaded SMCS and Loaded SMURF , along with Loaded Blazed DS , Loaded Command Transmitter Module , and Loaded Sensible Media Simulator that are materializations of Blazed DS , Command Transmitter Module , and Sensible Media Simulator respectively, are included in Loaded Sensible Media Software . The latter is a materialization of Sensible Media Software , constituted of the aforementioned mulsemedia programs. The loaded mulsemedia programs inhere (reside) in a User's Computer , except for the Loaded Command Transmitter Module that inheres (resides) in the Command Transmitter Device .

[FIGURE]

[FIGURE]

## 4.2.3 Wearable VR-based Mulsemedia System

[Ranasinghe et al., 2018] introduce a VR (Virtual Reality) game where users enjoy the four seasons of the year (spring, summer, autumn, and winter) as though they were traveling on a virtual hot air balloon with multisensory sensations. To this end, the users wear a Samsung Gear VR, connected to a Samsung Note 5 smartphone, whereby the game runs. Furthermore, a wind device, a thermal neckband, and an olfactory pump are attached to the VR gear to deliver wind, thermal and scent effects respectively. The game connects to a control module on a DFRobot Bluno Nano microcontroller that handles the devices. An instantiation of MulseOnto for the wearable VR-based mulsemedia system described in [Ranasinghe et al., 2018] is presented in an object diagram in Figure 10.

Season Traveller is a Mulsemedia Computer System that is composed of many media such as Summer Graphic , Spring Graphic , Autumn Graphic , Winter Graphic , Summer Audio , Spring Audio , Autumn Audio , and Winter Audio , and sensory effects descriptions like Thermal Metadata , Wind Effects Metadata , and Olfactory Metadata . Season Traveller User Interface , A DF Robot Bluno Nano , and A Samsung Note 5 are also parts of Season Traveller . Another constituent is Loaded Season Traveller Software , a Loaded Mulsemedia Software System Copy that is a materialization of Season Traveller Software and includes loaded mulsemedia programs such as a Loaded VR Game , which is a materialization of VR Game that inheres (reside) in A Samsung Note 5 , and a Loaded Control Module , a materialization of

[FIGURE]

- -Alignment and comparison of a new mulsemedia system with other systems using MulseOnto might help to avoid neglecting small parts of this complex ecosystem. It might also be useful to speed up this development once it is known what is necessary for a complete system.

## 5 Conclusion and Future Directions

The concept of mulsemedia is not easy to understand at a glance due to its complex digital ecosystem. By underlining sensory effects, types of different media, responsibilities to present/produce them, and their physical realizations through a formal and explicit representation, we try to convey the message of what is entailed in mulsemedia systems through MulseOnto, a reference domain ontology on Mulsemedia Systems.

This effort aimed at establishing a common conceptualization about mulsemedia including the interrelationship between its entities, describing a common vocabulary for knowledge workers in this domain, certifying the stakeholders are uniform and consistent when discussing mulsemedia solutions, and promoting the development of mulsemedia ecosystems as a whole.

We evaluated the reference ontology against the competency questions and also created different instances of the concepts from three real-world scenarios to verify whether they conform to it in addition to a hypothetical scenario described in [Saleme et al., 2018]. As a result, this strengthened the accuracy of our ontology from the assumption that MulseOnto is capable of reflecting concepts based on real-world environments, and therefore, it encompasses true abstractions of mulsemedia systems elements sometimes neglected when reading a plain English text about it.

MulseOnto can be regarded as a tool to discuss the mulsemedia ecosystem that involves capturing, distributing, rendering and perceiving sensory effects. As future work, we intend to take it a step further by creating a mulsemedia ontology network to cope with those processes in detail. A network of ontologies is an assortment of ontologies connected through a variety of relationships. Therefore, each descendant-ontology can share their relationships with a conceivably large number of other well-established ontologies promoting reuse [Suarez-Figueroa et al., 2012]. Another concern that can be taken into account in the future is the materialization of this conceptual model to an operational ontology to exchange, for instance, sensory effects metadata as an alternative to the current standards such as MPEG-V. Moreover, it can be useful for integrating different mulsemedia standards that might eventually arise enabling interoperability between different solutions by mapping them to this reference ontology.

## Acknowledgments

This study was financed in part by the Coordena¸ c˜ ao de Aperfei¸ coamento de Pessoal de N´ ıvel Superior-Brasil (CAPES)-Finance Codes 88881.187844/2018-01 and 88882.317673/2019-01. It was also funded by the European Union's Horizon 2020 Research and Innovation programme under Grant Agreement no. 688503. E. B. Saleme acknowledges support from the Federal Institute of Esp´ ırito Santo (IFES). C. A. S. Santos additionally acknowledges the Instituto de Ciˆ encias Matem´ aticas e de Computa¸ c˜ ao (ICMC) of the University of S˜ ao Paulo (USP), where he is currently in a sabbatical year.

## References

- [Albert et al., 2017] Albert, B., Zanni-Merk, C., de Beuvron, F. B., Pillet, M., Maire, J.-L., Knecht, C., and Charrier, J. (2017). A smart system to standardize the specifications of haptic quality control. Procedia Comput. Sci. , 112(C):723-730.
- [Bordegoni et al., 1997] Bordegoni, M., Faconti, G., Feiner, S., Maybury, M. T., Rist, T., Ruggieri, S., Trahanias, P., and Wilson, M. (1997). A standard reference model for intelligent multimedia presentation systems. Computer Standards &amp; Interfaces , 18(6-7):477-496.
- [Bringuente et al., 2011] Bringuente, A. C. O., Falbo, R. A., and Guizzardi, G. (2011). Using a foundational ontology for reengineering a software process ontology. JIDM , 2(3):511-526.
- [Chang, 2013] Chang, S.-F. (2013). ACM SIGMM Chair's Message. http://www. sigmm.org/news/chairs\_msg\_2013 . [Online; accessed 04-April-2019].
- [Covaci et al., 2018] Covaci, A., Zou, L., Tal, I., Muntean, G.-M., and Ghinea, G. (2018). Is multimedia multisensorial? - a review of mulsemedia systems. ACM Computing Surveys , 51(5):91:1-91:35.
- [Danieau et al., 2013] Danieau, F., Bernon, J., Fleureau, J., Guillotel, P., Mollet, N., Christie, M., and L´ ecuyer, A. (2013). H-studio: An authoring tool for adding haptic and motion effects to audiovisual content. In Proc. of the Adjunct Publication of the 26th Annual ACM Symposium on User Interface Software and Technology , UIST '13 Adjunct, pages 83-84, New York, NY, USA. ACM.
- [de Amorim et al., 2019] de Amorim, M. N., Saleme, E. B., de Assis Neto, F. R., Santos, C. A. S., and Ghinea, G. (2019). Crowdsourcing authoring of sensory effects on videos. Multimedia Tools and Applications , 78(14):19201-19227.
- [Duarte et al., 2018] Duarte, B. B., Leal, A. L. C., Falbo, R. A., Guizzardi, G., Guizzardi, R. S. S., and Souza, V. E. S. (2018). Ontological foundations for software requirements with a focus on requirements at runtime. Applied Ontology , 13(2):73105.
- [Falbo, 2014] Falbo, R. A. (2014). Sabio: Systematic approach for building ontologies. In 1st Joint Workshop Onto.Com/ODISE on Ontologies in Conceptual Modeling and Information Systems Engineering .
- [Ghinea et al., 2011] Ghinea, G., Andres, F., and Gulliver, S. R. (2011). Multiple Sensorial Media Advances and Applications: New Developments in MulSeMedia: New Developments in MulSeMedia . Premier reference source. Information Science Reference.
- [Ghinea et al., 2014] Ghinea, G., Timmerer, C., and Lin, W. (2014). Mulsemedia: State of the Art, Perspectives, and Challenges. ACM Trans. Multimedia Comput. Commun. Appl. , 11(1s):17:1-17:23.

- [Gruninger and Fox, 1995] Gruninger, M. and Fox, M. S. (1995). Methodology for the design and evaluation of ontologies. In Workshop on Basic Ontological Issues in Knowledge Sharing .
- [Guarino, 1995] Guarino, N. (1995). Formal ontology, conceptual analysis and knowledge representation. Int. J. Hum.-Comput. Stud. , 43(5-6):625-640.
- [Guizzardi et al., 2015] Guizzardi, G., Wagner, G., Almeida, J. P. A., and Guizzardi, R. S. S. (2015). Towards ontological foundations for conceptual modeling: The unified foundational ontology (UFO) story. Applied Ontology , 10(3-4):259-271.
- [Hariri et al., 2016] Hariri, S., Mustafa, N. A., Karunanayaka, K., and Cheok, A. D. (2016). Electrical stimulation of olfactory receptors for digitizing smell. In Proceedings of the 2016 Workshop on Multimodal Virtual and Augmented Reality , MVAR '16, pages 4:1-4:4, New York, NY, USA. ACM.
- [Heller and Martin, 1995] Heller, R. S. and Martin, C. D. (1995). A media taxonomy. IEEE MultiMedia , 2(4):36-45.
- [Horvat et al., 2014] Horvat, M., Bogunovi´ c, N., and ´ Cosi´ c, K. (2014). Stimont: a core ontology for multimedia stimuli description. Multimedia Tools and Applications , 73(3):1103-1127.
- [Jalal et al., 2018] Jalal, L., Anedda, M., Popescu, V., and Murroni, M. (2018). Qoe assessment for iot-based multi sensorial media broadcasting. IEEE Transactions on Broadcasting , 64(2):552-560.
- [Josu´ e et al., 2018] Josu´ e, M., Abreu, R., Barreto, F., Mattos, D., Amorim, G., dos Santos, J., and Muchaluat-Saade, D. (2018). Modeling sensory effects as first-class entities in multimedia applications. In Proc. 9th ACM Multimedia Systems Conf. , MMSys '18, pages 225-236, New York, NY, USA. ACM.
- [Kim et al., 2013] Kim, S.-K., Joo, Y.-S., and Lee, Y. (2013). Sensible media simulation in an automobile application and human responses to sensory effects. ETRI Journal , 35(6):1001-1010.
- [Luque et al., 2014] Luque, F. P., Galloso, I., Feijoo, C., Mart´ ın, C. A., and Cisneros, G. (2014). Integration of multisensorial stimuli and multimodal interaction in a hybrid 3dtv system. ACM Trans. Multimedia Comp. Comm. Appl. , 11(1s):16:116:22.
- [Mesfin et al., 2019] Mesfin, G., Hussain, N., Covaci, A., and Ghinea, G. (2019). Using eye tracking and heart-rate activity to examine crossmodal correspondences qoe in mulsemedia. ACM Trans. Multimedia Comput. Commun. Appl. , 15(2):34:1-34:22.
- [Murray et al., 2017] Murray, N., Ademoye, O. A., Ghinea, G., and Muntean, G.-M. (2017). A tutorial for olfaction-based multisensorial media application design and evaluation. ACM Comp. Surveys , 50(5):67:1-67:30.
- [Naravane and Lange, 2017] Naravane, T. and Lange, M. (2017). Organoleptic and sensory ontology. In Proceedings of the Joint Ontology Workshops 2017 Episode 3: The Tyrolean Autumn of Ontology, Bozen-Bolzano, Italy, September 21-23, 2017.
- [Oh and Hahn, 2009] Oh, S. and Hahn, M. (2009). The ontology for a multi-sensory media service. In 2009 11th Int. Conf. on Advanced Communication Technology , volume 02, pages 1025-1030.
- [Presutti et al., 2012] Presutti, V., Blomqvist, E., Daga, E., and Gangemi, A. (2012). Pattern-Based Ontology Design , pages 35-64. Springer Berlin Heidelberg, Berlin, Heidelberg.
- [Ranasinghe and Do, 2016] Ranasinghe, N. and Do, E. Y.-L. (2016). Digital lollipop: Studying electrical stimulation on the human tongue to simulate taste sensations. ACM Trans. Multimedia Comput. Commun. Appl. , 13(1):5:1-5:22.
- [Ranasinghe et al., 2017] Ranasinghe, N., Nguyen, T. N. T., Liangkun, Y., Lin, L.-Y., Tolley, D., and Do, E. Y.-L. (2017). Vocktail: A virtual cocktail for pairing digital taste, smell, and color sensations. In Proceedings of the 2017 ACM on Multimedia Conference , MM '17, pages 1139-1147, New York, NY, USA. ACM.
- [Ranasinghe et al., 2018] Ranasinghe, N., Jain, P., Thi Ngoc Tram, N., Tolley, D., Liangkun, Y., Eason Wai Tung, C., Yen, C. C., Do, E. Y.-L., Koh, K. C. R., and

Shamaiah, K. (2018). A demonstration of season traveller: Multisensory narration for enhancing the virtual reality experience. In Extended Abstracts of the 2018 CHI Conference on Human Factors in Computing Systems , CHI EA '18, pages D114:1D114:4, New York, NY, USA. ACM.

- [Roy and Zeng, 2015] Roy, S. D. and Zeng, W. (2015). Media on the web. In Social Multimedia Signals , pages 9-18. Springer.
- [Ruy et al., 2016] Ruy, F. B., Falbo, R. A., Perini, M. B., Costa, S. D., and Guizzardi, G. (2016). Seon: A software engineering ontology network. In Knowledge Engineering and Knowledge Management , pages 527-542, Cham. Springer International Publishing.
- [Saleme and Santos, 2015] Saleme, E. B. and Santos, C. A. S. (2015). PlaySEM: A Platform for Rendering MulSeMedia Compatible with MPEG-V. In Proceedings of the 21st Brazilian Symposium on Multimedia and the Web , WebMedia '15, pages 145-148, New York, NY, USA. ACM.
- [Saleme et al., 2018] Saleme, E. B., Santos, C. A. S., Falbo, R. A., Ghinea, G., and Andres, F. (2018). Towards a reference ontology on mulsemedia systems. In Proceedings of the 10th International Conference on Management of Digital EcoSystems , MEDES '18, pages 23-30, New York, NY, USA. ACM.
- [Saleme et al., 2019a] Saleme, E. B., Covaci, A., Mesfin, G., Santos, C. A. S., and Ghinea, G. (2019a). Mulsemedia DIY: A survey of devices and a tutorial for building your own mulsemedia environment. ACM Computing Surveys , 52(3):58:1-58:29.
- [Saleme et al., 2019b] Saleme, E. B., Santos, C. A. S., and Ghinea, G. (2019b). Coping with the challenges of delivering multiple sensorial media. IEEE MultiMedia , 26(2):66-75.
- [Saleme et al., 2019c] Saleme, E. B., Santos, C. A. S., and Ghinea, G. (2019c). A mulsemedia framework for delivering sensory effects to heterogeneous systems. Multimedia Systems , 25(4):421-447.
- [Steinmetz and Nahrstedt, 1995] Steinmetz, R. and Nahrstedt, K. (1995). Multimedia: Computing, Communications and Applications . Prentice-Hall, Inc., Upper Saddle River, NJ, USA.
- [Suarez-Figueroa et al., 2012] Suarez-Figueroa, M. C., Gomez-Perez, A., Motta, E., and Gangemi, A. (2012). Ontology Engineering in a Networked World . Springer Publishing Company, Inc.
- [Vi et al., 2017] Vi, C. T., Marzo, A., Ablart, D., Memoli, G., Subramanian, S., Drinkwater, B., and Obrist, M. (2017). Tastyfloats: A contactless food delivery system. In Proceedings of the 2017 ACM International Conference on Interactive Surfaces and Spaces , ISS '17, pages 161-170, New York, NY, USA. ACM.
- [Waltl et al., 2013] Waltl, M., Rainer, B., Timmerer, C., and Hellwagner, H. (2013). An End-to-end Tool Chain for Sensory Experience Based on MPEG-V. Image Commun. , 28(2):136-150.
- [Wanick et al., 2018] Wanick, V., Xavier, G., and Ekmekcioglu, E. (2018). Virtual transcendence experiences: Exploring technical and design challenges in multi-sensory environments. In Proceedings of the 10th International Workshop on Immersive Mixed and Virtual Environment Systems , MMVE '18, pages 7-12, New York, NY, USA. ACM.
- [Yoon et al., 2015] Yoon, K., Kim, S.-K., Han, J. J., Han, S., and Preda, M. (2015). MPEG-V: Bridging the Virtual and Real World . Academic Press, 1st edition.
