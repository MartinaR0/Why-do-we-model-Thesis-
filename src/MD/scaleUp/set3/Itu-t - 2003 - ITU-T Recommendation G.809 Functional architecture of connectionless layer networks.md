[FIGURE]

INTERNATIONAL TELECOMMUNICATION UNION

## ITU-T G.809

TELECOMMUNICATION STANDARDIZATION SECTOR OF ITU (03/2003)

## SERIES G: TRANSMISSION SYSTEMS AND MEDIA,

## DIGITAL SYSTEMS AND NETWORKS Digital networks - General aspects

## Functional architecture of connectionless layer networks

## ITU-T G-SERIES RECOMMENDATIONS

## TRANSMISSION SYSTEMS AND MEDIA, DIGITAL SYSTEMS AND NETWORKS

| INTERNATIONAL TELEPHONE CONNECTIONS AND CIRCUITS                                                                                             | G.100-G.199   |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| GENERAL CHARACTERISTICS COMMONTOALLANALOGUECARRIER- TRANSMISSION SYSTEMS                                                                     | G.200-G.299   |
| INDIVIDUAL CHARACTERISTICS OF INTERNATIONAL CARRIER TELEPHONE SYSTEMS ON METALLIC LINES                                                      | G.300-G.399   |
| GENERAL CHARACTERISTICS OF INTERNATIONAL CARRIER TELEPHONE SYSTEMS ON RADIO-RELAY OR SATELLITE LINKS AND INTERCONNECTION WITH METALLIC LINES | G.400-G.449   |
| COORDINATION OF RADIOTELEPHONY AND LINE TELEPHONY                                                                                            | G.450-G.499   |
| TESTING EQUIPMENTS                                                                                                                           | G.500-G.599   |
| TRANSMISSION MEDIA CHARACTERISTICS                                                                                                           | G.600-G.699   |
| DIGITAL TERMINAL EQUIPMENTS                                                                                                                  | G.700-G.799   |
| DIGITAL NETWORKS                                                                                                                             | G.800-G.899   |
| General aspects                                                                                                                              | G.800-G.809   |
| Design objectives for digital networks                                                                                                       | G.810-G.819   |
| Quality and availability targets                                                                                                             | G.820-G.829   |
| Network capabilities and functions                                                                                                           | G.830-G.839   |
| SDH network characteristics                                                                                                                  | G.840-G.849   |
| Management of transport network                                                                                                              | G.850-G.859   |
| SDH radio and satellite systems integration                                                                                                  | G.860-G.869   |
| Optical transport networks                                                                                                                   | G.870-G.879   |
| DIGITAL SECTIONS AND DIGITAL LINE SYSTEM                                                                                                     | G.900-G.999   |
| QUALITY OF SERVICE AND PERFORMANCE                                                                                                           | G.1000-G.1999 |
| TRANSMISSION MEDIA CHARACTERISTICS                                                                                                           | G.6000-G.6999 |
| DIGITAL TERMINAL EQUIPMENTS                                                                                                                  | G.7000-G.7999 |
| DIGITAL NETWORKS                                                                                                                             | G.8000-G.8999 |

For further details, please refer to the list of ITU-T Recommendations.

## ITU-T Recommendation G.809

## Functional architecture of connectionless layer networks

## Summary

This  Recommendation  describes  the  functional  architecture  of  a  connectionless  transport  network from the viewpoint of its information transfer capability. The functional and structural architecture of these networks is described independently of networking technology. As such, the Recommendation should be taken as the basis for technology-specific descriptions of connectionless transport networks.

## Source

ITU-T Recommendation G.809 was prepared by ITU-T Study Group 13 (2001-2004) and approved under the WTSA Resolution 1 procedure on 22 March 2003.

## FOREWORD

The International Telecommunication Union (ITU) is the United Nations specialized agency in the field of telecommunications. The ITU Telecommunication Standardization Sector (ITU-T) is a permanent organ of ITU. ITU-T is responsible for studying technical, operating and tariff questions and issuing Recommendations on them with a view to standardizing telecommunications on a worldwide basis.

The  World  Telecommunication  Standardization  Assembly  (WTSA),  which  meets  every  four  years, establishes  the  topics  for  study  by  the  ITU-T  study  groups  which,  in  turn,  produce  Recommendations  on these topics.

The approval of ITU-T Recommendations is covered by the procedure laid down in WTSA Resolution 1.

In  some  areas  of  information  technology  which  fall  within  ITU-T's  purview,  the  necessary  standards  are prepared on a collaborative basis with ISO and IEC.

## NOTE

In  this  Recommendation,  the  expression  "Administration"  is  used  for  conciseness  to  indicate  both  a telecommunication administration and a recognized operating agency.

## INTELLECTUAL PROPERTY RIGHTS

ITU  draws  attention  to  the  possibility  that  the  practice  or  implementation  of  this  Recommendation  may involve  the  use  of  a  claimed  Intellectual  Property  Right.  ITU  takes  no  position  concerning  the  evidence, validity or applicability of claimed Intellectual Property Rights, whether asserted by ITU members or others outside of the Recommendation development process.

As of the date of approval of this Recommendation, ITU had not received notice of intellectual property, protected by patents, which may be required to implement this Recommendation. However, implementors are cautioned that this may not represent the latest information and are therefore strongly urged to consult the TSB patent database.

##  ITU 2003

All rights reserved. No part of this publication may be reproduced, by any means whatsoever, without the prior written permission of ITU.

## CONTENTS

|                                                                                                                                    |                                                                                                                                                                                      |   Page |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| Scope ............................................................................................................................ | Scope ............................................................................................................................                                                   |      1 |
| References.....................................................................................................................    | References.....................................................................................................................                                                      |      1 |
| Definitions ....................................................................................................................   | Definitions ....................................................................................................................                                                     |      2 |
| Abbreviations................................................................................................................      | Abbreviations................................................................................................................                                                        |      4 |
| Conventions..................................................................................................................      | Conventions..................................................................................................................                                                        |      4 |
| Functional Architecture of connectionless layer networks...........................................                                | Functional Architecture of connectionless layer networks...........................................                                                                                  |      4 |
| 6.1                                                                                                                                | Introduction ....................................................................................................                                                                    |      4 |
| 6.2                                                                                                                                | Relationship between connection-oriented and connectionless layer networks ......................................................................................................... |      4 |
| 6.3                                                                                                                                | Architectural components...............................................................................                                                                              |      5 |
| 6.4                                                                                                                                | Partitioning and layering ................................................................................                                                                           |     11 |
| 6.5                                                                                                                                | Decomposition of connectionless layer networks..........................................                                                                                             |     16 |
| 6.6                                                                                                                                | Application of concepts to network topologies and structures.......................                                                                                                  |     16 |
| Annex A - Characteristics of connectionless and connection-oriented layer networks..........                                       | Annex A - Characteristics of connectionless and connection-oriented layer networks..........                                                                                         |     17 |
| A.1                                                                                                                                | Characteristics of a CO-CS network implemented with SDH, OTN or PDH................................................................................................................  |     18 |
| A.2                                                                                                                                | Characteristics of a CO-PS network implemented with ATM.......................                                                                                                       |     18 |
| A.3                                                                                                                                | Characteristics of a CLPS network implemented with IP using best effort, destination-based forwarding .........................................................................      |     19 |
| A.4                                                                                                                                | Characteristics of a network implemented with ethernet ...............................                                                                                               |     19 |
| Annex B - Components of connection-oriented and connectionless layer networks..............                                        | Annex B - Components of connection-oriented and connectionless layer networks..............                                                                                          |     21 |

1

1

2

4

4

4

4

4

5

## ITU-T Recommendation G.809

## Functional architecture of connectionless layer networks

## 1 Scope

This Recommendation describes the functional architecture of connectionless layer networks using the methodology described in ITU-T Rec. G.805. The concept of the connection is central to the functional  architecture  described  in  ITU-T  Rec.  G.805  and  in  order  to  provide  a  common framework between the connection-oriented layer networks and a connectionless layer network, it is necessary  to  introduce  new  concepts  that  describe  connectionless  behaviour.  The  connectionless transport  network  functionality  is  described  from  a  network  level  viewpoint,  taking  into  account layer network structure, networking topology, client characteristic information, client/server layer associations and mapping between connectionless and connection-oriented layer networks.

This Recommendation describes the functional architecture of connectionless transport networks in a  technology  independent  way.  As  such,  it  forms  the  basis  for  a  set  of  Recommendations  for management, performance analysis and equipment specifications related to specific connectionless technologies. The extension of the methodology defined in ITU-T Rec. G.805 for connectionless layer  networks  allows  for  the  description  of  equipment  containing  both  connection-oriented  and connectionless technologies in a common way.

If this Recommendation is used as the basis for developing a technology-specific Recommendation to describe and model networks that use existing protocols (such as IP, Ethernet, Token Ring, etc.) it shall be used in a manner that is fully consistent with existing specifications as approved by the relevant  standards  organizations.  The  use  of  this  Recommendation  is  not  intended  to  provide  a means by which existing protocols and architectures are modified.

## 2 References

The  following  ITU-T  Recommendations  and  other  references  contain  provisions  which,  through reference in this text, constitute provisions of this Recommendation. At the time of publication, the editions indicated were valid. All Recommendations and other references are subject to revision; users of this Recommendation are therefore encouraged to investigate the possibility of applying the most  recent  edition  of  the  Recommendations  and  other  references  listed  below.  A  list  of  the currently valid ITU-T Recommendations is regularly published. The reference to a document within this Recommendation does not give it, as a stand-alone document, the status of a Recommendation.

- -ITU-T Recommendation G.803 (2000), Architecture of transport networks based on the synchronous digital hierarchy (SDH) .
- -ITU-T Recommendation G.805 (2000), Generic functional architecture of transport networks .
- -ITU-T Recommendation G.8080/Y.1304 (2001), Architecture for the automatically switched optical networks (ASON) .
- -ITU-T Recommendation I.326 (2003), Functional architecture of transport networks based on ATM .
- -ITU-T Recommendation X.200 (1994) | ISO/IEC 7498-1:1994, Information technology Open Systems Interconnection - Basic Reference Model: The basic model .

## 3 Definitions

- NOTE 1 - Where a definition contains a term which is itself defined, that term is given in quotation marks.
- NOTE  2 - The  terms  can  be  further  qualified  by  reference  to  a  specific  layer  network  by  adding  the appropriate layer network qualifier.
- NOTE 3 - All architectural components are unidirectional.
- NOTE 4 - The definitions only apply to connectionless layer networks. Definitions for connection-oriented networks are as described in ITU-T Rec. G.805.

This Recommendation defines the following terms:

- 3.1 access group :  A  group of colocated "flow termination" functions that are attached to the same "flow domain" or " flow point pool link".
- 3.2 access point : A "reference point" that represents the binding between the flow termination and adaptation functions.
- 3.3 adaptation :  A  "transport  processing  function".  There  are  two  types  of  adaptation,  an adaptation sink and an adaptation source.
- 3.4 adaptation sink : A "transport processing function" which presents the client layer network characteristic information at its output by processing the information presented at its input by the server layer network trail.
- 3.5 adaptation source :  A  "transport processing function" which accepts client layer network characteristic information at its input and processes it to allow transfer over a trail (in the server layer network).
- 3.6 adapted information :  A signal which is transferred on "trails" or "connectionless trails". The specific formats will be defined in the technology specific recommendations.
- 3.7 architectural component : Any item used in this Recommendation to generically describe transport network functionality.
- 3.8 binding :  A  direct  relationship  between  a  "transport  processing  function"  or  "transport entity"  and  another  "transport  processing  function"  or  "transport  entity"  which  represents  static associations that cannot be directly modified by management action.
- 3.9 characteristic  information :  A  signal  with  a  specific  format,  which  is  transferred  on "flows". The specific formats will be defined in the technology specific Recommendations.
- 3.10 client/server relationship : The association between layer networks that is performed by an "adaptation" function to allow the "flow" in the client layer network to be supported by a trail in the server layer.
- 3.11 connectionless trail :  A "transport entity" responsible for the transfer of information from the input of a flow termination source to the output of a flow termination sink. The integrity of the information transfer may be monitored.
- 3.12 flow : An aggregation of one or more traffic units with an element of common routing.
- 3.13 flow  domain : A topological component used to effect forwarding of a specific characteristic information.
- 3.14 flow domain flow : A "transport entity" that transfers information across a flow domain, it is formed by the association of "ports" on the boundary of the flow domain.
- 3.15 flow point : A "reference point" that represents a point of transfer for traffic units between topological components.
- 3.16 flow point pool : A group of colocated flow points that have a common routing.

- 3.17 flow  point  pool  link :  A  "topological  component"  which  describes  a  fixed  relationship between a "flow domain" or "access group" and another "flow domain" or "access group".
- 3.18 flow  termination :  A  "transport  processing  function".  There  are  two  types  of  flow termination, a flow termination sink and a flow termination source.
- 3.19 flow termination sink : A "transport processing function" which accepts the "characteristic information" of the layer network at its input, recovers the information related to "connectionless trail" monitoring and presents the remaining information at its output.
- 3.20 flow  termination  source :  A  "transport  processing  function"  which  accepts  adapted "characteristic information" from a client layer network at its input, adds information to allow the "connectionless  trail"  to  be  monitored  and  presents  the  characteristic  information  of  the  layer network at its output(s).
- 3.21 layer  network :  A  "topological  component"  that  represents  the  complete  set  of  access groups of the same type which may be associated for the purpose of transferring information.
- 3.22 link  flow :  A  "transport  entity"  that  transfers  information  between  "ports"  across  a  flow point pool link.
- 3.23 matrix : It represents the limit to the recursive partitioning of a flow domain.
- 3.24 matrix flow : A "transport entity" that transfers information across a matrix, it is formed by the association of ports on the boundary of the matrix.
- 3.25 network :  All  of  the  entities  (such  as  equipment,  plant,  facilities)  which  together  provide communication services.
- 3.26 network  flow :  A  transport  entity  formed  by  a  series  of  contiguous  "flows"  between "termination flow points".
- 3.27 port : It represents the output of a flow termination source or flow domain or the input to a flow termination sink or flow domain.
- 3.28 reference  point :  An  architectural  component,  which  is  formed  by  the  binding  between inputs and outputs of transport processing functions and/or transport entities.
- 3.29 topological  component :  An  architectural  component,  used  to  describe  the  transport network  in  terms  of  the  topological  relationships  between  sets  of  points  within  the  same  layer network.
- 3.30 traffic unit : An instance of characteristic information and a unit of usage.
- 3.31 transport : The functional process of transferring information between different locations.
- 3.32 transport  entity :  An  architectural  component  which  transfers  information  between  its inputs and outputs within a layer network.
- 3.33 transport  network : The  functional resources of the network  which  conveys  user information between locations.
- 3.34 transport  processing  function :  An  architectural  component  defined  by  the  information processing which is performed between its inputs and its outputs. Either the input or the output must be inside a layer network.
- 3.35 termination flow point : A reference point that represents the binding of a flow termination to a flow.

## 4 Abbreviations

This Recommendation uses the following abbreviations:

| AP       | Access Point                         |
|----------|--------------------------------------|
| CLPS     | Connectionless packet switched       |
| CO-CS    | Connection-oriented circuit switched |
| CO-PS    | Connection-oriented packet switched  |
| CP       | Connection Point                     |
| FP       | Flow Point                           |
| FPP      | Flow Point Pool                      |
| FPP link | Flow Point Pool link                 |
| TCP      | Termination Connection Point         |
| TFP      | Termination Flow Point               |

## 5 Conventions

The diagrammatic convention for connection-oriented layer networks described in this Recommendation is that of ITU-T Rec. G.805.

## 6 Functional Architecture of connectionless layer networks

## 6.1 Introduction

The various functions that constitute a telecommunications network can be classified into two broad functional  groups.  One  is  the  transport  functional  group  that  transfers  any  telecommunications information  from  one  point  to  another  point(s).  The  other  is  the  control  functional  group  that realises various ancillary services and operations and maintenance functions.

A connectionless transport network transfers user information from one location to another location in a unidirectional manner. A transport network can also transfer various kinds of network control information such as routing protocols and operations and maintenance information for the control functional group.

Since the transport network is a large, complex network with various components, an appropriate network model with well-defined functional entities is essential for its design and management. The connectionless  transport  can  be  described  by  defining  the  relationships  between  points  in  the network. In order to simplify the description, a transport network model, based on the concepts of layering and partitioning within each layer network is used in a manner that allows a high degree of recursion. It is recommended that this method is used for describing the transport network.

## 6.2 Relationship between connection-oriented and connectionless layer networks

Central to the description of connection-oriented networks is the concept of a connection. However, such a construct is inappropriate for the description of a connectionless network. Consequently, it is necessary  to  replace  the  concepts  of  a  connection  and  a  connection  point  as  defined  in  ITU-T Rec. G.805  with  new  architectural  components  as  defined  in  this  Recommendation.  A  detailed description of the properties and differences between connection-oriented and connectionless layer networks can be found in Annexes A and B.

The  description  of  connection-oriented  layer  networks  in  ITU-T  Rec.  G.805  assumes  that  the default for transmission is bidirectional whereas transfer in a connectionless layer network is always unidirectional. As such many of the definitions in ITU-T Rec. G.805 are not strictly appropriate for connectionless  layer  networks.  This  Recommendation  therefore  defines  all  of  the  architectural components related to the architecture of connectionless layer networks.

## 6.3 Architectural components

The  connectionless  transport  network  has  been  analysed  to  identify  generic  functionality  that  is independent  of  implementation  technology.  This  has  provided  a  means  to  describe  network functionality in an abstract way in terms of a small number of architectural components. These are defined by the function they perform in information processing terms, or by the relationships they describe  between  other  architectural  components.  In  general,  the  functions  described  here  act  on information  presented  at  one  or  more  inputs  and  present  processed  information  at  one  or  more outputs.  They are defined and characterized by the information process between their inputs and outputs.  The  architectural  components  are  associated  together  in  particular  ways  to  form  the network elements from which real networks are constructed. The reference points of the transport network  architecture  are  the  result  of  associations  between  the  inputs  and  outputs  of  processing functions and transport entities.

Some diagrammatic conventions have been developed to support the descriptions that follow and these are illustrated in Figures 1 and 2 and summarized in Table 1.

Figure 1/G.809 - Diagrammatic conventions for processing functions (start)

[FIGURE]

[FIGURE]

Figure 1/G.809 - Diagrammatic conventions for processing functions (end)

[FIGURE]

## 6.3.1 Topological components

The  topological  components  provide  the  most  abstract  description  of  a  network  in  terms  of  the topological relationships between sets of like reference points. Four topological components have been distinguished; these are the layer network, the flow domain, the flow point pool link and the access group. Using these components it is possible to completely describe the logical topology of a connectionless layer network.

## 6.3.1.1 Layer network

A layer  network  is  defined  by  the  complete  set  of  access  groups  of  the  same  type  that  may  be associated for the purpose of transferring information. The information transferred is characteristic of  the  layer  network  and  is  termed  characteristic  information.  The  associations  of  the  flow terminations (that form a connectionless trail) in a layer network are defined on a per traffic unit basis, which, in a connectionless layer network, is a datagram. A separate, logically distinct layer network  exists  for  each  flow  termination  type.  The  topology  of  a  layer  network  is  described  by access groups, flow domains and the flow point pool links between them. The structures within and between layer networks are described by the components below.

## 6.3.1.2 Flow domain

A flow domain exists within a single layer network. It is defined by the set of flow points that are available  for  the  purpose  of  transferring  information.  Datagram  transfers  across  the  flow  domain that  correspond  to  a  particular  association  between  ingress  and  egress  flow  points  need  not  be present  at  all  times.  In  general,  flow  domains  may  be  partitioned  into  smaller  flow  domains interconnected by flow point pool links. The matrix is a special case of a flow domain that cannot be further partitioned.

## 6.3.1.3 Flow point pool link

A flow point pool link consists of a subset of the flow points at the edge of one flow domain or a subset of the access points of an access group that are associated with a corresponding subset of flow points or access points at the edge of another flow domain or access group for the purpose of transferring characteristic information. The  flow  point  pool  link (FPP  link) represents the topological relationship and available capacity between a pair of flow domains, or a flow domain and an access group, or a pair of access groups.

Multiple flow point pool links may exist between any given flow domain and access group or pair of  flow  domains  or  access  groups.  Flow  point  pool  links  are  established  at  the  timescale  of  the server layer network.

## 6.3.1.4 Access group

An access group is a group of colocated flow termination functions that are connected to the same flow domain or flow point pool link.

## 6.3.2 Transport entities

The  transport  entities  provide  transparent  information  transfer  between  layer  network  reference points.  There  is  no  information  change  between  input  and  output  other  than  that  resulting  from degradation in the transfer process. Two basic entities are distinguished according to whether the information transferred is monitored for integrity. These are termed flows and trails. Flows may be decomposed in a number of ways including topologically, into network flows, flow domain flows and link flows.

## 6.3.2.1 Flow

A flow is an aggregation of one or more traffic units with an element of common routing. A flow has the following properties:

- -it is a unidirectional entity;
- -a flow can contain another flow. This is recursive until, for example, the limit of a single traffic unit is reached;
- -flows can be multiplexed together in the same layer network;
- -flows can be multiplexed together as part of adaptation to a server layer network;
- -a flow can be associated with one or more topological entities;
- -a  flow  can  be  defined  in  terms  of  a  parameter  such  as  its  characteristic  information,  the address to which traffic units are directed or the address the traffic units have come from;
- -the aggregation of traffic units may be spatial or temporal.

## 6.3.2.2 Link flow

A link flow is capable of transferring information (traffic units) transparently across an FPP link. It is  delimited by flow points and represents the fixed relation between the ends of the link. A link flow represents a pair of adaptation functions and a trail in the server layer network.

The flow point at the input to the unidirectional link flow also represents the input to an adaptation source; the flow point at the output of the unidirectional link flow also represents the output of an adaptation sink.

## 6.3.2.3 Flow domain flow

A flow domain flow is a grouping of traffic units that are transferred transparently across a flow domain. It is delimited by the ports associated with flow points at the boundary of the flow domain and represents an association between these ports. In general, flow domain flows are constructed from a concatenation of flow domain flows and link flows. The matrix flow is a special case of the flow domain flow.

## 6.3.2.4 Network flow

A  network  flow  is  a  grouping  of  traffic  units  that  are  transferred  transparently  across  a  layer network.  It  is  delimited  by  the  termination  flow  points  (TFPs).  In  general,  network  flows  are constructed  from  a  concatenation  of  flow  domain  flows  and  link  flows.  The  TFP  is  formed  by binding the port of a flow termination to either a flow domain port or a port on an FPP link.

## 6.3.2.5 Connectionless trail

A connectionless trail represents the transfer of monitored adapted characteristic information of the client layer network between access points. It is delimited by two access points, one at each end of the  connectionless  trail.  It  represents  the  association  between  a  source  and  destination  on  a  per traffic unit or datagram basis. A connectionless trail is formed by associating flow terminations with a traffic unit or datagram.

## 6.3.3 Transport processing functions

Two generic processing functions of adaptation and flow termination are distinguished in describing the architecture of connectionless layer networks.

## 6.3.3.1 Adaptation function

Adaptation  source :  A  transport  processing  function  which  adapts  the  client  layer  network characteristic  information  into  a  form  suitable  for  transport  over  a  trail  (in  a  connection-oriented server layer network) or connectionless trail (in a connectionless server layer network) in the server layer network.

Adaptation  sink :  A  transport  processing  function  which  converts  the  server  layer  network  trail (in a  connection-oriented server layer network) or connectionless trail (in a connectionless server layer network) information into the characteristic information of the client layer network.

The following are examples of processes that may occur singly or in combination in an adaptation function:

Labelling, scheduling, buffering, queuing, multiplexing, traffic dropping, segmentation and reassembly.

Adaptation  function  cardinality :  The  adaptation  source  function  input  to  output  relation  is  a many-to-one relationship or a one-to-many. In the first case, one or more client layer network inputs are  adapted  into  a  single  adapted  information  stream  suitable  for  transport  over  a  trail  (or connectionless  trail)  in  the  connection-oriented  (or  connectionless)  server  layer  network  and  this relationship is commonly used to represent the multiplexing of several clients into a single server. In the second case, one composite stream is split over several outputs, and this is used to describe the common processing involved in inverse multiplexing. The converse relationships hold for the adaptation sink function between its single input and one or more outputs.

## 6.3.3.2 Flow termination function

Flow  termination  source :  A  transport  processing  function  which  accepts  adapted  characteristic information from a client layer network at its input, adds information to allow the connectionless trail  to  be  monitored,  and  presents  the  characteristic  information  of  the  layer  network  at  its output(s). The flow termination source can operate without an input from a client layer network.

NOTE - Whilst the general case is one where a flow termination function adds or extracts information to monitor a connectionless trail, it is also possible that no overhead is provided to monitor the connectionless trail.

Flow  termination sink : A  transport processing function which accepts the characteristic information of the layer network at its input, removes the information related to connectionless trail monitoring and presents the remaining information at its output.

Flow  termination  function  cardinality :  The  flow  termination  source  function  input  to  output relation  is  a  one-to-many  relationship.  The  single  adapted  information  input  stream  is  distributed over one or more (connectionless) trails in the server layer. The flow termination source function is associated with a number of termination flow points. The termination flow point that is selected for a particular datagram is dependent on the destination address.

Note that, in a connection-oriented network, the default cardinality is such that a trail termination source has a single termination connection point associated with it.

The flow termination sink function input to output relation is a one-to-one relationship. The flow termination sink is bound to a single termination flow point.

## 6.3.4 Reference points

Reference  points  are  formed  by  the  binding  between  inputs  and  outputs  of  transport  processing functions  or  represent  the  role  of  an  unbound  input  or  output  of  a  transport  processing  function when  associated  with  a  topological  component.  The  resultant  bindings  and  specific  types  of reference point are shown in Table 1.

A dynamic binding exists between a flow point or a termination flow point and a connectionless datagram. This binding exists for the time period over which the datagram transits the flow point or termination flow point.

Table 1/G.809 - Allowable bindings and resulting reference points

| Architectural components   | Architectural components   | Architectural components   | Architectural components   | Reference point   | Reference point   |
|----------------------------|----------------------------|----------------------------|----------------------------|-------------------|-------------------|
| Adaptation                 | Source output              | Flow Termination           | Source input               | AP                | unidirectional    |
|                            | Sink input                 | Flow Termination           | Sink output                |                   | unidirectional    |
| Flow domain                | Input port                 | Flow termination           | Source output              | TFP               | unidirectional    |
|                            | Output port                | Flow termination           | Sink input                 |                   | unidirectional    |
| Flow domain                | Output port                | Adaptation                 | Source input               | FP                | unidirectional    |
|                            | Input port                 | Adaptation                 | Sink output                |                   | unidirectional    |
| Flow domain                | Output port                | Flow domain                | Input port                 | FP                | unidirectional    |
|                            | Input port                 | Flow domain                | Output port                |                   | unidirectional    |
| Flow                       | Egress                     | Flow                       | Ingress                    | FP                | unidirectional    |
|                            | Ingress                    | Flow                       | Egress                     |                   |                   |
| AP                         | Access Point               |                            |                            |                   |                   |
| FP                         | Flow Point                 |                            |                            |                   |                   |
| TFP                        | Termination Flow Point     |                            |                            |                   |                   |

Figure 2/G.809 - Bindings and types of reference points

[FIGURE]

## 6.4 Partitioning and layering

## 6.4.1 Introduction

A transport network can be decomposed into a number of independent transport layer networks with a client/server association between adjacent layer networks. Each layer network can be separately partitioned in a way that reflects the internal structure of that layer network or the way that it will be managed. Thus the concepts of partitioning and layering are orthogonal as shown in Figure 3.

Figure 3/G.809 - Orthogonal views of layering and partitioning

[FIGURE]

## 6.4.1.1 Application of the partitioning concept

The partitioning concept is important as a framework for defining:

- -the network structure within a layer network;
- -administrative boundaries between network operators within a single layer network;
- -routing domain boundaries within the layer network of a single operator;
- -the part of a layer network or routing domain that is under the control of a third party for routing purposes (e.g., customer network management).

## 6.4.1.2 Application of the layering concept

The layering concept of the transport network allows:

- -each layer network to be described using similar functions;
- -the independent design and operation of each layer network;
- -each layer network to have its own operations, diagnostic and automatic failure recovery capability;
- -the  possibility  of  adding  or  modifying  a  layer  network  without  affecting  other  layer networks from the architectural viewpoint;
- -simple modelling of networks that contain multiple transport technologies.

## 6.4.2 Partitioning concept

## 6.4.2.1 Flow domain partitioning

In general a flow domain is constructed by representing the physical implementation as FPP links and flow domains, starting from the matrix that is the smallest (indivisible) flow domain. A set of flow domains and FPP links may be abstracted as a higher (containing) flow domain. The way in which the contained flow domains are interconnected by FPP links describes the topology of the containing  flow  domain.  The  ports  at  the  boundary  of  the  containing  flow  domain  and  the interconnection capability must fully represent, but not extend, the connectivity supported by the contained flow domains and FPP links. Therefore, a higher level flow domain may be partitioned to show the level of detail required.

Thus, in general, any flow domain may be partitioned into a number of smaller (contained) flow domains interconnected by FPP links. The partitioning of a flow domain cannot extend or restrict its connectivity i.e.:

- -The ports on the boundary of the containing flow domain and the interconnection capability must be represented by the contained flow domains and FPP links.
- -The contained flow domains and FPP links cannot provide connectivity that is not available in the containing flow domain.

Examples of flow domains are the international portion and the national portions of a layer network which  can  be  further  divided  into  transit  portions  and  access  portions  and  so  on,  as  shown  in Figure 4. Another example of partitioning is the creation of virtual private network topologies.

A network flow or flow domain flow may be decomposed into a concatenation of other transport entities (link flow or flow domain flow) which reflects the partitioning of a flow domain.

Figure 4/G.809 - Partitioning of layer networks and flow domains

[FIGURE]

## 6.4.2.2 Flow point pool link partitioning

In general, a flow point pool link is constructed by bundling a set of link flows (and assigning the associated flow points into flow point pools), that are equivalent for the purposes of routing. Flow point pool links may also be further bundled to provide for any desired capacity visibility.

## 6.4.3 Layering concept

The  transport  network  can  be  decomposed  into  a  number  of  independent  layer  networks  with  a client/server relationship between adjacent layer networks. A  layer network describes the generation, transport and termination of a particular characteristic information.

The layer networks that have been identified in the transport network functional model should not be confused with the layers of the OSI Model (ITU-T Rec. X.200). An OSI layer offers a specific service using one protocol among different protocols. On the contrary, each layer network (in this Recommendation) offers the same service using a specific protocol (the characteristic information).

## 6.4.3.1 Client/server relationships between layer networks

Four forms of client/server relationships exist between connection-oriented and connectionless layer networks:

- -A connection-oriented client layer supported by a connection-oriented server layer network. This relationship is described in ITU-T Rec. G.805.

- -A  connection-oriented  client  layer  network  supported  by  a  connectionless  server  layer network. This relationship is illustrated in Figure 5. In this relationship, a client layer link connection (or a network connection containing no subnetwork connections) is supported by  a  server  layer  connectionless  trail.  The  server  layer  source  adaptation  adapts  the connection-oriented  characteristic  information  of  the  client  layer  into  connectionless adapted information in the server layer.  The  server  layer  sink  adaptation  function  adapts server layer connectionless adapted information to client layer connection-oriented characteristic information.
- -A  connectionless  client  layer  network  supported  by  a  connection-oriented  server  layer network. This relationship is illustrated in Figure 6. In this relationship, a client layer flow is  supported  by  a  server  layer  trail.  The  server  layer  source  adaptation  adapts  the connectionless  characteristic  information  of  the  client  layer  into  connection-oriented adapted information in the server layer.  The  server  layer  sink  adaptation  function  adapts server layer connection-oriented adapted information to client layer connectionless characteristic information.
- -A connectionless client layer network supported by a connectionless server layer network. This  relationship  is  illustrated  in  Figure  7.  In  this  relationship,  a  client  layer  flow  is supported by a server layer connectionless trail. The server layer source adaptation adapts the connectionless characteristic information of the client layer into connectionless adapted information in the server layer. The server layer sink adaptation function adapts server layer connectionless adapted information to client layer connectionless characteristic information.

The  concept  of  adaptation  is  introduced  to  describe  how  the  client  layer  network  characteristic information is modified so that it can be transported over a trail, or connectionless trail, in the server layer  network.  From  a  transport  network  functional  viewpoint,  therefore,  the  adaptation  function falls between the layer networks. All the reference points belonging to a single layer network can be visualized as lying on a single plane as illustrated in Figure 1. This is the reason why there is not the same concept of contiguous layer boundaries in the transport network model as in the OSI protocol reference model.

Figure 5/G.809 - Example client server/relationship between a connection-oriented client layer network and a connectionless server layer network

[FIGURE]

Figure 6/G.809 - Example client server/relationship between a connectionless client layer network and a connection-oriented server layer network

[FIGURE]

Figure 7/G.809 - Example client server/relationship between a connectionless client layer network and a connectionless server layer network

[FIGURE]

## 6.5 Decomposition of connectionless layer networks

It  is  possible  to  decompose  a  connectionless  layer  network  by  expanding  either  the  flow terminations, or (termination) flow points of the layer network.

## 6.6 Application of concepts to network topologies and structures

NOTE 1 - The naming schemes used in the examples may not correspond with the naming schemes used in any related equipment specifications.

NOTE 2 - The examples show only the basic network topologies and structures. Additional functionality, where appropriate, will be provided in the related equipment specifications.

## 6.6.1 Ethernet supported on SDH layer networks

Figure 8 shows an example of the case where Ethernet signals (ETH) are supported on SDH. Four layer networks are shown:

- -Ethernet Media Access Control (ETH) layer network;
- -SDH higher-order path (e.g., VC-4) layer network;
- -SDH multiplex section layer network;
- -SDH regenerator section layer network.

Figure 8/G.809 - Application of functional architecture to the case of Ethernet supported on SDH

[FIGURE]

## Annex A

## Characteristics of connectionless and connection-oriented layer networks

This annex compares and contrasts the properties of connection-oriented and connectionless layer networks.

Many  existing  transport  networks  provide  a  Connection-oriented  circuit  switched  (CO-CS) infrastructure  (e.g.,  SDH).  The  architecture  of  transport  networks  based  on  SDH  is  described  in ITU-T Rec. G.803. A Connection-oriented packet switched (CO-PS) infrastructure (e.g., ATM) that uses  the  CO-CS  infrastructure  may  also  be  provided.  ITU-T  Rec.  I.326  describes  the  functional architecture for ATM networks. A Connectionless Packet Switched (CLPS) infrastructure may be provided directly over a CO-CS infrastructure, CO-PS infrastructure, another CLPS infrastructure or over none of the above (e.g., directly connected). Note that the CO-CS infrastructure supporting a CO-PS or CLPS infrastructure may have limited capability (e.g., flexibility).

These  infrastructures  have  certain  inherent  characteristics  that  are  used  in  the  Operation  and Administration of the network and the services that the network supports. A simplified description of, and an attempt to characterise, some of these networks is provided below:

## A.1 Characteristics of a CO-CS network implemented with SDH, OTN or PDH

Before  a  user  information  flow  is  initiated  across  the  network,  the  user  source,  user  destination (applications)  and  the  network  must  agree  on  the  characteristics  of  the  connection  (e.g.,  bit  rate, availability).  In  terms  of  the  Automatic  Switched  Transport  Network  architecture  described  in ITU-T  Rec.  G.8080/Y.1304,  a  call  represents  the  negotiation  between  the  customer  and  the network,  whilst  the  connection  supports  the  information  flow.  Based  on  this  agreement  to communicate (the call), the end customer payload is explicitly assigned to network resources by a connection  management  process,  e.g.,  an  explicit  time-slot  is  identified  in  each  of  a  series  of concatenated (server layer) trails to interconnect the end user terminals at the addresses identified in the  call  request.  These  trails  may  be  shared  by  multiple  end  customer  payloads.  Contention  for resources  is  resolved  at  the  time  the  connection  is  requested,  if  resources  are  not  available  the connection request is rejected (and the call attempt fails). In this case, the timeslot represents both a networking identifier (for the purposes of cross-connection or switching) and an explicit resource reservation. In terms of the ITU-T Rec. G.805 model, it is the adaptation function at the input of a server layer trail that "stores" the client signal until the assigned timeslot arrives. The customer does not constrain the choice of timeslot within the network i.e., the network "owns" the multiplexing and switching identifier space. This networking identifier (timeslot) has only local significance; it is only valid in the context of a specific trail. Separation of customer signals is provided inherently by the timeslot assignment performed by the network. Since the network has performed the assignment process, it can also arrange to intercept and monitor the client signal (or the trail supporting it) at any convenient point in the network. Network failures invoke a specific process, either a protection switch or restoration. A protection switch process is not visible to a connection management system (i.e., the end points of the trail are unchanged) whilst restoration invokes a new connection setup. Monitoring of the client signal can be coordinated across these processes. In general, both the client signal and the trails used to carry it are monitored using network overhead.

## A.2 Characteristics of a CO-PS network implemented with ATM

Before  a  user  information  flow  is  initiated  across  the  network,  the  user  source,  user  destination (applications) and the network must agree on the characteristics of the signal (e.g., peak and average bit  rate).  Based  on  this  agreement,  the  end  customer  payload  is  explicitly  assigned  to  network resources by a connection management system i.e., an explicit VPI/VCI is identified in each of a series of concatenated (server layer) trails to interconnect the end user terminals at the addresses identified in the call request. These trails may be shared by multiple end customer payloads. In this case,  contention  for  the  trail  resources  is  not  always  fully  resolved  at  the  time  the  connection  is requested,  however,  the  network  can  assign  (or  not)  customer  connections  to  trails  based  on  the traffic parameters of the connection request and the connections already assigned to the trail. In this case, the VCI/VPI represent networking identifiers for switching. In terms of the I.326 model, it is the  adaptation  function  on  the  input  to  the  server  layer  trail  that  buffers  the  ATM cell  until  a timeslot is available on the outgoing (CO-CS) trail. The customer does not constrain the choice of VPI/VCI  within  the  network  i.e.,  the  network  "owns"  the  multiplexing  and  switching  identifier space. The VPI/VCI identifiers only have local significance; they are only valid in the context of a specific  trail.  Separation  of  customer  signals  is  provided  inherently  by  the  VPI/VCI  assignment performed by the  network.  Since  the  network  has  performed  the  assignment  process,  it  can  also arrange to intercept and monitor the client signal (or the trail supporting it) at any convenient point in the network. Note that, while network failures can cause the rearrangement of connections, this does  not  prevent  monitoring  as  described  above.  In  general,  the  integrity  of  the  client  signal  is monitored using OAM cells. The trails in the network are monitored using network overhead.

## A.3 Characteristics of a CLPS network implemented with IP using best effort, destinationbased forwarding

An IP packet can be initiated  by  a  user  without  prior  negotiation  with  either  the  network  or  the destination  user  terminal:  there  is  no  reservation  of  end-to-end  resources.  The  source  and destination addresses (networking identifiers) are included in the IP header appended to each packet by the source terminal. Both addresses have global significance, and the destination address is used by each router to forward the packet towards the intended destination based on the routing table at each router. A new packet invokes the same process used for any previous packet i.e., the network does not maintain state. The transport network resources (e.g., the CO-CS trails between routers) are shared by arbitrary end customer packets based on the content of the routing tables (e.g., current network topology and congestion). Changes in network topology (e.g., failures) and traffic loading are accommodated by updating the routing tables (e.g., removal of a failed link from the topology). The IP network uses a routing protocol to keep the routing tables current. Since the network has no explicit knowledge of the existence or location of a specific packet between customer terminals, the network  cannot  monitor  these  packets  for  service  assurance.  In  such  a  network,  each  packet  is treated independently and each packet can be considered as being equivalent to a flow using the model  described  in  this  Recommendation.  Higher  granularity  flows  based  upon  aggregation  of packets can also be defined.

## A.4 Characteristics of a network implemented with ethernet

Similar to IP, as described above, a Media Access Control (MAC) frame can be initiated by a user, without prior negotiation, with either the network or the destination user terminal. The source and destination addresses (networking identifiers) are added to the header of each MAC frame by the source terminal. The addresses have global significance and the destination address is used by each switch to forward the information flow towards the intended destination based on the forwarding table at each switch.

When  a  switch  receives  a  frame  with  a  MAC  address  that  is  not  in  the  forwarding  table,  it  is broadcast and, based on the frames received in the reverse direction, a new entry is made in the forwarding table. The information in the forwarding table "ages" and after some period of inactivity (i.e.,  no  frames)  it  is  discarded.  The  transport  network  resources  (e.g.,  the  CO-CS  trails  between routers)  are  shared  by  arbitrary  end  customer  information  flows  based  on  the  content  of  the forwarding  table.  Network  topology  changes  are  accommodated  by  invoking  the  broadcast mechanism and spanning tree algorithm to refresh the forwarding table. Since the network has no explicit knowledge of the existence or location of a specific flow between customer terminals, the network cannot monitor these flows for service assurance. In common with IP used in best effort, destination-based forwarding mode, each MAC frame can be considered as a flow, where the flow is equivalent to a single frame. Higher granularity flows based on aggregation of frames can also be defined.

The characteristics of the networks identified above are summarized in Table A.1.

Table A.1/G.809 - Network characteristics of connection-oriented and connectionless layer networks

| Network Characteristic                                                                  | CO-CS (e.g., SDH, OTN)                            | CO-PS (e.g., ATM)                                 | CLPS (IP) With best effort, destination- based forwarding                           | CLPS (Ethernet)                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| UNI demarcation                                                                         | Yes                                               | Yes                                               | No                                                                                  | No                                                                              |
| NNI demarcation                                                                         | Yes                                               | Yes                                               | No                                                                                  | No                                                                              |
| Control Plane/Bearer Plane separation                                                   | Yes                                               | Yes                                               | No                                                                                  | No                                                                              |
| Networking identifier assigned by                                                       | Network                                           | Network                                           | Client                                                                              | Client                                                                          |
| Network identifier used for naming or addressing                                        | No                                                | No                                                | Yes                                                                                 | Yes                                                                             |
| Networking identifier                                                                   | Local                                             | Local                                             | Global                                                                              | Global                                                                          |
| Networking identifier forwarding                                                        | Crossconnect                                      | ATM Switch                                        | router                                                                              | switch                                                                          |
| Source/destination address appended by                                                  | -                                                 | -                                                 | Client                                                                              | Client                                                                          |
| Source/destination address independent of networking identifier                         | Yes                                               | Yes                                               | No                                                                                  | No                                                                              |
| Network visibility from client                                                          | No                                                | No                                                | Yes (e.g., Ping, Trace Route)                                                       | Yes (e.g., Ping)                                                                |
| Explicit connection request before flow initiation (Call/connection model)              | Yes                                               | Yes                                               | No                                                                                  | No                                                                              |
| Per flow (call) service assurance                                                       | Yes                                               | Yes                                               | No                                                                                  | No                                                                              |
| Per flow (call) billing                                                                 | Yes                                               | Yes                                               | No                                                                                  | No                                                                              |
| Per flow (call) end-to-end resource allocation                                          | Yes/Implicit                                      | Yes                                               | No                                                                                  | No                                                                              |
| Flow (call) duration                                                                    | Until explicitly terminated                       | Until explicitly terminated                       | Length of current packet                                                            | Length of current packet                                                        |
| Possibility of miss-sequencing of information between delivered to end user application | No - assuming communication is over a single flow | No - assuming communication is over a single flow | Yes - communication is segmented into packets each of which is routed independently | Yes - but not if packet flow is frequent enough to refresh the forwarding table |

## Annex B

## Components of connection-oriented and connectionless layer networks

This  annex  compares  the  components  of  a  connection-oriented  architecture  based  on  ITU-T Rec. G.805 with that of the connectionless architecture described in this Recommendation. This is described in Table B.1. Note that, whilst the terms "access group" and "access point" appear to be the same in both architectures their definitions are different depending upon the context of the layer network. In a connection-oriented layer network, the access point is the reference point between the adaptation and trail termination whilst, in a connectionless layer network, it is the reference point between  the  adaptation  and  flow  termination.  Furthermore,  the  access  point  of  a  connectionless layer network is associated with a connectionless trail, whilst the connection-oriented access point is associated with a trail. Similarly, the access group in a connectionless layer network is defined in terms of flow terminations, flow domains and flow point pool links whilst, in a connection-oriented layer  network,  it  is  defined  in  terms  of  terminations,  links  and  subnetworks.  This  allows  for  a common description of a layer network for both connection-oriented and connectionless cases.

Note that bidirectional constructs described in ITU-T Rec. G.805 do not have a counterpart in a connectionless layer network.

Entities that are specific to a connectionless network are indicated in bold type.

Table B.1/G.809 - Components of connection-oriented and connectionless architectures

| Connection-oriented component               | Connectionless component      |
|---------------------------------------------|-------------------------------|
| Access group                                | Access group                  |
| Access point                                | Access point                  |
| Adaptation                                  | Adaptation                    |
| Adaptation sink                             | Adaptation sink               |
| Adaptation source                           | Adaptation source             |
| Adapted information                         | Adapted information           |
| Architectural component                     | Architectural component       |
| Characteristic information                  | Characteristic information    |
| Client/server relationship                  | Client/server relationship    |
| Unidirectional connection                   | Flow                          |
| Unidirectional connection point             | Flow point                    |
| Layer network                               | Layer network                 |
| Link                                        | Flow point pool link          |
| Link connection                             | Link flow                     |
| Network connection                          | Network flow                  |
| Subnetwork                                  | Flow domain                   |
| Subnetwork connection                       | Flow domain flow              |
| Unidirectional termination connection point | Termination flow point        |
| Topological component                       | Topological component         |
| Trail                                       | Connectionless trail          |
| Trail termination                           | Flow termination              |
| Trail termination sink                      | Flow termination sink         |
| Trail termination source                    | Flow termination source       |
| Transport                                   | Transport                     |
| Transport entity                            | Transport entity              |
| Transport network                           | Transport network             |
| Transport processing function               | Transport processing function |

## SERIES OF ITU-T RECOMMENDATIONS

| Series A   | Organization of the work of ITU-T                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| Series B   | Means of expression: definitions, symbols, classification                                                                      |
| Series C   | General telecommunication statistics                                                                                           |
| Series D   | General tariff principles                                                                                                      |
| Series E   | Overall network operation, telephone service, service operation and human factors                                              |
| Series F   | Non-telephone telecommunication services                                                                                       |
| Series G   | Transmission systems and media, digital systems and networks                                                                   |
| Series H   | Audiovisual and multimedia systems                                                                                             |
| Series I   | Integrated services digital network                                                                                            |
| Series J   | Cable networks and transmission of television, sound programme and other multimedia signals                                    |
| Series K   | Protection against interference                                                                                                |
| Series L   | Construction, installation and protection of cables and other elements of outside plant                                        |
| SeriesM    | TMN and network maintenance: international transmission systems, telephone circuits, telegraphy, facsimile and leased circuits |
| Series N   | Maintenance: international sound programme and television transmission circuits                                                |
| Series O   | Specifications of measuring equipment                                                                                          |
| Series P   | Telephone transmission quality, telephone installations, local line networks                                                   |
| Series Q   | Switching and signalling                                                                                                       |
| Series R   | Telegraph transmission                                                                                                         |
| Series S   | Telegraph services terminal equipment                                                                                          |
| Series T   | Terminals for telematic services                                                                                               |
| Series U   | Telegraph switching                                                                                                            |
| Series V   | Data communication over the telephone network                                                                                  |
| Series X   | Data networks and open system communications                                                                                   |
| Series Y   | Global information infrastructure and Internet protocol aspects                                                                |
| Series Z   | Languages and general software aspects for telecommunication systems                                                           |
