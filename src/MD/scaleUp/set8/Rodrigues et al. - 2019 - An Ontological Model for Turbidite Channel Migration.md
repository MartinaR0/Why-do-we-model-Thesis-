## An Ontological Model for Turbidite Channel Migration

## Fabrício Henrique Rodrigues, Luan Fonseca Garcia, Renata dos Santos Alvarenga, Mara Abel

Instituto de Informática - Universidade Federal do Rio Grande do Sul (UFRGS)

{fabricio.rodrigues, luan.garcia, rsakuchle, marabel}@inf.ufrgs.br

Abstract . Geology  interpretation  applies  abductive  reasoning  to  determine, from the actual existent rock units, the processes that create these occurrences. In particular, modelling the sedimentary processes of erosion and deposition, are of crucial importance for understanding the spatial distribution of the rock bodies  that  configure  actual  petroleum  reservoir.  This  paper  proposes  an ontological model for turbidite channel migration, which is an important event in the formation of turbidite systems, a common type of reservoir. The proposed model is based on the Unified Foundational Ontology and presents both a high level  description  of  the  event  as  well  as  details  its  main  composing  events, namely erosion, transportation and deposition of sediments.

## 1. Introduction

Ontologies  can  be  regarded  as  explicit  specifications  of  conceptualizations  (Gruber, 1993). In a practical sense, an ontology formally describes the concepts of a given domain and the relationships among them. Such concepts may represent both things that exist (usually called objects ) as well as things that happen (usually called events ). In spite of that, there is a somewhat widespread view that objects are ontologically prior to events 1 , according to which objects are all that exists and events exist just as the distribution of matter  and  objects  in  space  and  time  (Galton,  Mizoguchi,  2009).  Nevertheless,  from chemical  reactions  to  business  transactions,  it  seems  that  great  part  of  our  reality  is fundamentally  dependent  on  events  (Casati,  Varzi,  2015).  Therefore,  a  thorough ontological treatment of this dynamic aspect of reality would surely enhance our means of representing the world. An example of domain that would take advantage of good ontological analysis of perdurants is Geology.

Geology is the domain that studies the Earth and the rocks that compose it. Since geologists  cannot  observe  their  whole  subject  of  study,  they  heavily  rely  on  the understanding  of  the  geological  processes  that  form  rocks,  since  it  can  support  the interpretation of the environment which is under analysis. With that, they can analyze samples of rock and other indirect measures from some geological target of investigation and infer the processes that led it to its current state. Then, considering that the other geological objects which are present in the same environment may have been affected by the same processes, this approach can provide a glimpse of the conditions of these other objects.

The  understanding  of  geological  processes  is  particularly  important  for  the comprehension of sedimentary deposits, such as turbidites - a frequent type of clastic deposit on the continental slope (McHargue et al., 2011) associated to the occurence of hydrocarbon reservoirs in several parts of the world. These deposits are formed as a result of  turbidity  currents,  which  are  dense  sediment  gravity  flows  that  happen  when  the accumulation  of  sediments  in  the  border  of  the  continental  platform  achieves  its equilibrium limit and suddenly fall down. Due to their strength, such currents dig deep channels in the border of the slope, transporting and depositing large volume of coarsegrained clastic sediments from continental slope into deep ocean. Besides creating new turbidite channels, subsequent flows can also reshape previously formed channels and deposits, by means of the deposition of new sediment as well the erosion and reallocation of  already  deposited  sediment.  Fig.  1  shows  a  schematic  representation  of  a  turbidity current.

1 We use here the terms process, event, occurrent and perdurant interchangeably along the text keeping the same meaning.

According to (McHargue et al., 2011), despite the abundance of turbidites and the many years of study of such deposit type, their characterization and predictability is still a big challenge for industry, due to the three-dimensional complexity and diversity of channel systems.

Figure 1. A turbidity current carrying the sediments towards the distal part of the area.  (source National Ocean Service, USA).

[FIGURE]

In order to help in achieving a better understanding of turbidite deposits, this paper proposes an ontological model for the process of lateral migration of turbidite channels (i.e.,  the  erosion  of  sediments  from  the  lateral  bank  of  the  channel  followed  by  the transport and deposit of the sediment further ahead on the channel). The model is based on  the  Unified  Foundational  Ontology  (UFO)  (Guizzardi,  2005)  and  may  help  in developing  a  geological  model  of  the  sedimentation-erosion  process  of  the  lateral migration process, which can further feed the flow model of reservoirs.

Thus, the model makes explicit (a) the pre-conditions and the results of the lateral migration  process,  (b)  the  stages  of  this  process,  (c)  the  required  conditions  to  the occurrence of each of the stages, (d) the objects that participate in them, and (e) which role they play in the process.

The remaining of the paper is organized as follows: section 2 presents an overview of UFO, section 3 provides a summary of the turbidite domain, section 4 presents and discusses the proposed model, and section 5 brings our final remarks.

## 2. The Unified Foundational Ontology (UFO)

UFO is a philosophically and cognitively well-founded foundational ontology (Guizzardi et al., 2013), which provides a set of meta-types described in terms of well-defined meta- properties (such as rigidity, provision of identity criterion, relational dependence). One of its major benefits is that, by offering such meta-properties, it gives us a systematic and rigorous way to analyze the universals (i.e. a notion roughly equivalent to that of concept or class) of a domain. It can be done by identifying which combination of meta-properties the  universal  presents  and  then  selecting  the  corresponding  meta-type  into  which  the universal  should  be  classified.  UFO  divides  universals  into  two  broad  categories: endurant universals and perdurant universals.

Endurant universals gather individuals that are in time (i.e. they are wholly present whenever  they  are  present).  A  person,  a  rock,  and  a  pen  are  examples  of  endurant individuals.  Endurant  universals  are  further  divided  into objects (i.e.  existentially independent  endurants,  e.g.,  book,  water)  and moments (i.e.  that  only  exist  in  other individuals, e.g., weight, color) (Guizzardi, 2005).

Perdurant universals (hereafter referred to as event universals ) comprise individuals that happen in time (i.e. they extend in time accumulating temporal parts) and that are existentially  dependent  on  the  objects  that  participate  in  them.  Instances  of  such universals are regarded as transformations of the state of affairs from one situation to another (Guizzardi et al., 2013). Examples of event individuals include the fall of an apple from  a  tree  (that  would  be  existentially  dependent  on  the  apple)  or  a  game  of  chess (dependent on the players and the chess set).

Situation universals comprise particular configurations of a part of reality that can be understood as a whole. A traffic jam and a weather station deployed on a given area are examples of situations. A situation instance may be related to an event instance either being its pre-state (i.e. situation that triggers the occurrence of an event, e.g. some water exposed to below freezing temperature triggers a freezing event) or its post-state (i.e. situation that is brought about as a result of the occurrence of the event, e.g. a wet soil after  a  rain).  There  is  a  unique  particular  situation  that  triggers  a  particular  event occurrence, as well as there is a unique maximal situation that is brought about by such occurrence.

Events  may  be  composed  by  other  events.  A  particular  way  of  partitioning  a complex event is separating each part of it that is existentially dependent on each of its participants.  Each  of  such  parts  would  be  a participation (i.e.  an  event  exclusively dependent on a single object). Each participation induces one or more processual roles over its participant object, representing the role the object plays in the event it participates in (i.e. the way its participation influences the event) (Guizzardi et al., 2013).

## 3. Turbidite Channel Lateral Migration

Turbidite  channels  are  conduits  on  the  underwater  surface  that  are  dug  by  turbidity currents. These channels are formed by delineated by sediment volumes that act as border walls of the channel confining the currents that flow on it. Such sediment volumes are called banks and may be of two types: inner banks or outer banks. Inner banks are convexshaped banks that form the inner side of the curves of some channel whereas outer banks are concave-shaped banks that form the outer side of the curves of some channel. The shape  of  a  turbidite  channel  is  given  by  the  shapes  of  its  composing  banks  and  both turbidite  channels  and  banks  are  characterized  by  their  sinuosity,  which  roughly corresponds to how curved the channel/bank is.

The  lateral  migration  of  the  turbidite  channel  is  an  event  that  reshapes  the architecture of a channel and increases its sinuosity by transferring sediment among its banks. Thus, this event can be decomposed in three other events: erosion, transportation, and deposition of sediments.

Figure 2:  A) Schematic illustration of sediment flow through a turbidite channel. The cross-sectional view (x-y) illustrates the vertical view of turbidite channel that  is  presented  in  (B),  (Modified  from  Posamentier  &amp;  Walker,  2006).  B) Depositional model of the turbite channel migration that results from systematic erosion of the outer banks and deposition along inner banks. (Modified from Abreu et al., 2003).

[FIGURE]

First, in the event of erosion , unconsolidated material that is located in some outer bank of the channel is eroded by the flowing water, due to its high energy in that point of the channel. The transportation process drags the eroded sediment downstream until the water loses the necessary energy to transport it, which happens when reaching some inner bank of the channel. At this moment, we have the deposition of the heavier sediments on the reached inner bank, while the lighter portion may remain in suspension, being carried by  the  water  to  some  place  ahead  on  the  channel.  Fig.  2A  shows  a  sinuous  channel, indicating both inner and outer banks. Fig. 2B shows the lateral profile of the channel depicted in Fig. 2A, depicting the inner and outer banks from another perspective and presenting the temporal evolution of the sediments deposits on the inner bank.

## 4. An Ontological Model for Turbidite Channel Lateral Migration

This section presents the proposed ontological model for the event of turbidite channel lateral migration. It first presents a high-level model of the event, describing it in terms of its pre-state and post-state situations, its continuant participants, and the processual roles they play. Then it enumerates the stages that compose the migration event, which are further detailed one at a time.

There  are  basically  four  types  of  continuants  involved  in  a  turbidite  channel migration event: the turbidite channel, its composing banks, water, and sediment, which are shown in Fig. 3. Turbidite channel is a channel on the underwater surface that are formed by turbidity currents and whose shape is delineated by that of its composing banks (i.e.,  the  sediment  mass  that  forms  the  border  walls  of  the  channel).  Both  turbidity channels  and  banks  are  characterized  by  their sinuosity (i.e.,  how  curved  they  are). Depending on their shape, banks are further divided into inner banks (i.e., convex-shaped banks that  form  the  inner  side  of  the  curves  of  some  channel)  and outer  banks (i.e., concave-shaped banks that form the outer side of the curves os some channel).

The  concept  of water refers  to  specific,  maximally  connected  portions  of  the homonymous chemical  substance.  For  the  purposes  of  this  work,  we  highlighted  the kinetic energy attribute of water as a way to statically represent its 'moving state' (as a disposition that leads to some moving event). Regarding this attribute, we subdivided the concept of water into moving water (i.e., water with some kinetic energy) and still water (i.e.,  water  with  no  kinetic  energy).  On  top  of  that,  we  further  divided  the  concept  of moving water into high energy water and low energy water , according to the amount of kinetic energy it has, which would lead to faster or slower water flow. Finally, sediment represents specific, maximally connected portions of material that typically composes the underwater surface (including structures such as channels and banks), that may be of various types (e.g. sands constituted by diverse chemical substances).

Figure 3 - Continuants that participate in lateral migration events.

[FIGURE]

## 4.1. Turbidite Channel Lateral Migration: High-Level Model

Turbidity channel migration is the event in which some portion of moving water that fills a channel reshapes it by reallocating the sediment that composes its banks, increasing the sinuosity of the channel. Thus, it is an event that is triggered by a pre-state situation of water flowing through channel and brings about a situation of channel with increased sinuosity,  in  which  the  same  initial  turbidite  channel  has  a  more  sinuous  shape.  We represented the pre-state situation by means of the dynamic fill material relation (i.e., UFO's Relator), which relates some turbidite channel (that plays the role of confining channel) to the moving water that is running through it (that assumes the role of water stream).  The  water  participates  as  the  channel  sculptor  and  the  channel  participates, during most of the process, as the shape-changing channel, and as the resulting reshaped channel at the end of the event. Channel sinuosity increases during the process. This is the high-level description of the lateral migration event that is presented in Fig. 4.

Since  it  is  not  an  instantaneous,  atomic  event,  we  can  go  on  in  our  analysis, breaking it into its main stages, which can give us a better understanding of the way the process occurs. We are considering that any transference of sediment between any two banks of a turbidity channel changes its shape, by increasing the sinuosity of the involved banks. Thus, any such transference can be regarded as an event of lateral migration of the channel. Based on that, we can analyze how this transference takes place.

Within the pre-state situation of a turbidite channel migration event (i.e., the water flowing through channel situation), we can focalize a partial, local strong flow over outer bank situation, encompassing a portion of the water stream that is abrading an outer bank of the channel. This situation triggers the first stage of the channel migration: the event of erosion of outer bank , which represents the extraction of sediment from an outer bank and  its  transference  to  the  water  stream.  Such  event  brings  about  an erosion  result situation, which is composed by two smaller situations: the outer bank in new shape , that composes the post-situation of the whole turbidite channel migration event and comprises an eroded and more sinuous outer bank, and the loaded flow situation, which includes some moving water containing the eroded sediments.

The  loaded  flow situation  leads  to  the  second  stage:  the  event  of sediment transportation to inner bank , that represents the movement of the sediment-loaded water until it reaches an inner bank. This transportation event brings about a loaded weak flow on inner bank situation, which triggers the last stage of the migration event: the sediment deposition onto inner bank . This depositional event results in an inner bank with new sediment situation,  that  comprises  an  inner  bank  with  newly  deposited  sediment  and, consequently, with an altered, more sinuous shape. Given such shape modification, this situation is also a part of the post-state of the turbidite channel migration event as a whole.

It  is  important  to  note  that  events  of  migration  of  turbidite  channel  are  not restricted to a single sequences of erosion-transportation-deposition events. Considering the whole extension of the channel and the whole body of water flowing through it, there may be several outer banks suffering the erosive pressure of the water flow, which will lead to several independent chains of erosion-transportation-deposition events that will compose an overall turbidite channel migration event. This possibility is represented by the 1..* cardinalities on the composition relations between the pre/post-state situations and their component situations and on the composition relations between the turbidite channel migration event and its component stages. In the following, we detail such stages.

Figure 4 - Turbidity Channel Migration Ontological Model.

[FIGURE]

## 4.2. First Stage: Erosion of Outer Bank

Erosion of outer bank (Fig. 5) represents the process of dragging sediment out of the bank. This event is the result of the manifestation of two complementary dispositions: the disposition of pulling sediment out from a bank that inheres in high energy water , and the disposition of deposited sediment of being carried out when touched by some high energy water. Thus, the event is triggered by a strong flow over an outer bank situation, which gathers all the required conditions for the referred disposition manifestation, and brings about an erosion result situation.

A strong flow over an outer bank situation involves a frictional contact relation between some high energy water (which plays the role of frictioning water ), the outer bank that is in contact with the water (which plays the role of frictionally pressed outer bank ), and the portion of deposited sediment over which the water is exerting pressure (which plays the role of unstable sediment ). With that, the outer bank participates as the erosion patient of the event, the water participates as the erosive agent , and the sediment participates as the frictioned sediment .

The erosion result situation is composed by an outer bank in new shape situation and a loaded flow situation. The first one corresponds to the state of the outer bank after losing part of its sediment and, consequently, becoming more sinuous. With that, the outer bank also participates in the event as eroded bank .

The  other  (i.e., loaded  flow )  refers  to  the  state  of  the  remaining  participants, including the same portion of moving water that was present in the pre-state of the event, but now loaded with the eroded sediment. To represent that, we included the traction relator  (i.e.,  the  relation  between  flowing  water  and  some  heavy  sediment  that  it  is transporting), which relates some tractive water (i.e., the water that carries the sediment) to its drawn sediment (i.e., the sediment that is being carried by the water). Due to that, besides being the erosive agent of the event, the water also participates in the event as sediment receiver , and the sediment also participates as removed sediment .

Figure 5 - Outer Bank Erosion Event.

[FIGURE]

## 4.3. Second Stage: Sediment Transport to Inner Bank

The  movement  of  the  eroded  sediment  towards  an  inner  bank  is  represented  by  the sediment transportation to inner bank (Fig. 6) event. It is triggered by some loaded flow situation  and  happens  as  a  series  of  successive  manifestations  of  two  complementary dispositions: the disposition that a moving water has of carrying a mass load proportional to its kinetic energy, and the corresponding disposition of the sediment of being carried by some fluid with enough kinetic energy. The event ends when the loaded water reaches an inner bank.

For  the  dynamics  of  fluids  that  run  through  channels,  the  flowing  water  loses energy and gets slower when reaching an inner bank. As a result, the post-state of this event is a loaded weak flow over inner bank situation. This situation includes an obstacle contact relator, representing the relationship between the inner bank (that plays the role of obstacle inner bank ), the loaded water that is being slowed down by the inner bank (that plays the role of obstacled loaded water ), and the sediment that is in traction (that plays the role of obstacled sediment ).

Given this description, the water participates as the vehicle for the sediment, the sediment participates as the transported load during most of the event and as the blocked load at the end of the event, and the inner bank participates as the arriving point of the transportation.

Figure 6 - Sediment Transport to Inner Bank Event.

[FIGURE]

## 4.4. Third Stage: Sediment Deposition onto Inner Bank

The event of sediment transport to inner bank ends in a situation with some slow moving, loaded water that is being obstacled by an inner bank - which is exactly the situation that triggers the event of sediment deposition onto inner bank (Fig. 7). However, it raises the question of why such a situation leads to an event of deposition and not to a different event of transportation (e.g., deviating from the inner bank).

As  mentioned  before,  the  event  of  transportation  is  composed  by  successive activations of the disposition that a moving water has of carrying a load proportional to its  kinetic  energy  and  the  complementary  disposition  that  the  sediment  has  of  being carried by a sufficiently strong water flow. Therefore, although the end mark of such directed transport event is the arrival of the loaded water at some inner bank, it coincides with  the  instant  in  which  the  conditions  that  cause  the  activation  of  the  referred dispositions cease to exist. In other words, given their shape and inner bank position, inner banks have the disposition of hinder the water flow. With that, when the loaded water reaches an inner bank, there is a decrease in the kinetic energy of the water that prevents it from pushing the sediment forward to the next position. Moreover, the presence of some obstacle also prevents the sediment from occupying the next position ahead. It is this presence of such diverse conditions that changes the behavior of the involved continuants and triggers the event of sediment deposition onto inner bank .

Thus, whereas the obstacle inner bank simply participated as the arriving point in the transportation event, in the deposition event it participates as the obstacle that causes the ceasing of the conditions of activation of the dispositions of the moving water and the drawn sediment. First it slows water down, reducing its kinetic so that it is no longer sufficient to keep sediment in traction. Along with that, it blocks the sediment, making it even  harder  to  be  carried  by  the  water.  Then,  water  loses  its  load  (participating  as unloading vehicle ) and the drawn sediment is deposited on the inner bank (participating as captured sediment ), and, with that, the inner bank also participates as depositing place .

The event of sediment deposition onto inner bank brings about an inner bank with new sediment ,  which  gathers  an  inner  bank  with  some  deposited  sediment  (which  is represented by the deposition relator, and its relata deposited sediment and deposition bank ). This completes the reallocation of sediment of the banks of the channel. Moreover, the sum of modifications on the outer and inner banks involved in the three presented represent a modification on the overall shape of the channel as a whole. This combination of sediment reallocation and channel reshaping qualifies the sequence of such stages as a turbidite channel lateral migration event.

Figure 7 - Sediment Deposition onto Inner Bank Event.

[FIGURE]

## 5. Concluding Remarks

This paper presented an ontological model for turbidite lateral channel migration, which was developed based on the Unified Foundational Ontology. It provides a general, high level  description  of  the  event  as  well  as  details  its  three  main  stages  -  i.e.  erosion  of sediment from an outer bank, sediment transportation, and sediment deposition onto an inner bank. The model makes explicit the pre and post conditions of the lateral migration event, as well as the pre and post conditions of each of its stages. It also exposes the specific contributions of the participants to the overall event and its stages, as well as their arrangement in the situations that precede and follow each of the events.

With the conceptual formalization of this important process in the formation of turbidite systems we aim to contribute to a better comprehension of its effects over the final configuration of turbidite deposits, enhancing its predictability. Aligned with that, our  model  may  provide  a  conceptual  framework  to  guide  simulation  efforts  and  to contextualize their findings, since it indicates which are the main objects involved in the development  of  the  event,  makes  explicit  which  are  their  noteworthy  attributes  and interactions, and establishes how these elements must be arranged to trigger each of the described events and how they are left after the each event happens. This can provide basis for further definition of the physical quantities involved (e.g. the model indicates the  general  disposition  of  high  energy  water  of  eroding  sediments  from  outer  banks, which may be further quantified to establish the energy level required to erode different types of sediment).

As future work, we intend to model the other events that occur inside turbidite channels  (e.g.  aggradation,  flow  stripping)  and  those  events  that  comprise  the  whole turbidite channel system. We believe that fully modeling the events related to turbidite systems can greatly improve the understanding of such a complex systems and support the building of more accurate 3D models of this type of sedimentary deposit.

## Acknowledgements

We carry on this project in collaboration with Petrobras. We acknowledge the support of Brazilian sponsor agencies CAPES and CNPq.

## References

- Abreu,  V.,  Sullivan,  M.,  Pirmez,  C.,  Mohrig,  D.,  2003.  Lateral  accretion  packages (LAPs): an important reservoir element in deep water sinuous channels. Marine and Petroleum Geology 20, 631- 648.
- Casati, Roberto and Varzi, Achille, "Events", The Stanford Encyclopedia of Philosophy (Winter 2015 Edition), Edward N. Zalta (ed.), URL = &lt;https://plato.stanford.edu/archives/win2015/entries/events/&gt;.
- Galton, Antony, and Riichiro Mizoguchi. "The water falls but the waterfall does not fall: New perspectives on objects, processes and events." Applied Ontology 4.2 (2009): 71107.
- Gruber,  Thomas  R.  "A  translation  approach  to  portable  ontology  specifications." Knowledge acquisition 5.2 (1993): 199-220.
- Guizzardi,  Giancarlo.  "Ontological  foundations  for  structural  conceptual  models." (Doctoral Thesis), Centre for Telematics and Information Technology   (CTIT): Enschede, 2005.
- Guizzardi,  Giancarlo,  et  al.  "Towards  ontological  foundations  for  the  conceptual modeling  of  events." International  Conference  on  Conceptual  Modeling .  Springer, Berlin, Heidelberg, 2013.
- McHargue, Tim, et al. "Architecture of turbidite channel systems on the continental slope: patterns and predictions." Marine and Petroleum Geology 28.3 (2011): 728-743.
- Posamentier, H.W. &amp; Walker, R.G. 2006. Deepwater turbidites and submarine fans. In : Posamentier,  H.W.  &amp;  Walker  R.G.  (Eds.), Facies  Models  Revisited .  Society  for Sedimentary Geology (SEPM), Special Publication, 84, 397-520.
