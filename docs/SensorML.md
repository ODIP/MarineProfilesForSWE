---
title: 1. SensorML
layout: page
---
# Common SensorML profiles

“In order to achieve interoperability within and between various sensor
communities, implementation of SensorML will require the definition of
community specific semantics (within online dictionaries or ontologies)
that can be utilized within the framework” \[1\].

Task 3.21 deals with the implementation of these profiles, by dealing
with the following issues in SensorML:

-   The coding standard itself

-   The list of terms each section includes

-   The list of values each term can accept

-   The controlled vocabularies for the terms and values.

The current report is in sync with the SWE Marine profiles group, which
is formulating the common SensorML profiles across the world. The
following profiles will form the basis for the SWE Marine group work as
they include the decisions taken from the group’s meetings as well.

SWE Marine Profiles Group
-------------------------

To avoid interoperability issues in OGC SWE implementations by different
organizations and users, an agreement was needed on how to apply SWE
concepts and how to use vocabularies in a common way that would be
shared by different projects, implementations, and users.

SWE Marine Profiles group, was created as a solution to the above
mentioned need, by partners from several projects and initiatives (AODN,
BRIDGES, ENVRI+, EUROFLEETS /EUROFLEETS2, FixO3, FRAM, IOOS,
Jerico/Jerico-Next, NeXOS, ODIP/ODIP II, RITMARE, SeaDataNet,
SenseOcean, X-DOMES) who joined forces to develop common marine profiles
of OGC SWE standards that can be used in multiple projects and
organizations. \[2\]

SWE Marine Profile members interact and communicate through the use of a
mailing list and a wiki website. The wiki helps to collect and discuss
different approaches to how OGC Sensor Web Enablement (SWE) standards
(Sensor Observation Service (SOS), Observations and Measurements (O&M)
and SensorML are used in different projects and systems. It is currently
structured in the following subsections, which can be edited by its
members after logging in:

• SweExamples: Examples of SensorML, O&M and SOS usage

• SweVocabularies: Vocabularies for the Marine SWE Profiles

• SweProfile: Structure and proposed content of the Marine SWE Profiles

• SosInventory: Inventory of SOS Servers

A while ago the group published several vocabularies that cover six
SensorML sections, namely the History, Capabilities, Characteristics,
Classification, Identification and Contacts \[3\].

Overview
--------

This document describes platforms and sensors and distinguished them in
models and instances. A model is an intangible entity that specifies
some characteristics of a group of similar, usually mass-produced
products, in the sense of a prototype. An instance is a particular
serial number of a model. Through extension and inheritance, we need to
only provide minimal instance-specific information about a particular
deployed sensor/platform, while retaining a link back to a much more
robust manufacturer's description. The information that is common to all
sensors of this model is found by following the link in the typeOf
element.

PLATFORM MODELS
---------------

### <span id="_iyyj709ib2wn" class="anchor"><span id="_Toc485492827" class="anchor"></span></span>IDENTIFIERS

#### Code style

> &lt;sml:identification&gt;
>
> &lt; sml:IdentifierList&gt;
>
> &lt; sml:identifier&gt;
>
> &lt; sml:Term
> definition="http://vocab.nerc.ac.uk/collection/W07/current/IDEN0012/"&gt;
>
> &lt; sml:label&gt;Manufacturer&lt;/label&gt;
>
> &lt;
> sml:value&gt;http://vocab.nerc.ac.uk/collection/L35/current/MAN0007/&lt;/
> sml:value&gt;
>
> &lt;/Term&gt;
>
> &lt;/ sml:identifier&gt;
>
> &lt; /sml:IdentifierList&gt;
>
> &lt; /sml:identification&gt;

### Vocabularies
| List of terms:  | Minimum terms: | Status:   |
|-----------------|----------------|-----------|
| W07             | [Model name ](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0003/)     | Mandatory |
|                 | [Model number](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0004/)   |           |
|                 | [Manufacturer ](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0012/)   |           |
|                 | [UUID](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0007/)           |           |
|                 | [Unique ID](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0008/)|           |

### <span id="_l0e829l8f9yg" class="anchor"><span id="_Toc485492831" class="anchor"></span></span>CLASSIFICATION

#### Code style

> &lt;sml:classification&gt;
>
> &lt;sml:ClassifierList&gt;
>
> &lt;sml:classifier&gt;
>
> &lt;sml:Term
> definition="http://vocab.nerc.ac.uk/collection/W06/current/CLSS0002/"&gt;
>
> &lt;sml:label&gt;Instrument Type&lt;/ sml:label&gt;
> &lt;sml:value&gt;http://vocab.nerc.ac.uk/collection/L05/current/351/&lt;/sml:value&gt;
>
> &lt;/sml:Term&gt;
>
> &lt;/sml:classifier&gt;
>
> &lt;/sml:ClassifierList&gt;
>
> &lt;/sml:classification&gt;

#### Vocabularies
| List of terms:  | Minimum terms: | Status:   |
|-----------------|----------------|-----------|
| [W06](http://vocab.nerc.ac.uk/collection/W06/current/)| [Platform type](http://vocab.nerc.ac.uk/collection/W06/current/CLSS0001/)      | Mandatory |
|                 | Application Domain    |           |




### <span id="_qepzmqbra3l7" class="anchor"><span id="_Toc485492835" class="anchor"></span></span>CAPABILITIES

#### Code style

> &lt;?xml version="1.0"?&gt;
>
> &lt;sml:capabilities name="MeasurementCapapbilities"&gt;
>
> &lt;sml:CapabilityList&gt;
>
> &lt;sml:capability name="Operating depth"&gt;
>
> &lt;sml:QuantityRange definition="
> http://vocab.nerc.ac.uk/collection/W04/current/CAPB0012/"&gt;
>
> &lt;sml:label&gt; Operating depth&lt;/label&gt;
>
> &lt;sml:uom href="
> http://vocab.nerc.ac.uk/collection/P06/current/ULAA/"/&gt;
>
> &lt;sml:value&gt;10 1000&lt;/value&gt;
>
> &lt;/sml:QuantityRange&gt;
>
> &lt;/sml:capability&gt;
>
> &lt;sml:capability name="SurvivalDepth"&gt;
>
> &lt;sml:Quantity definition="
> http://vocab.nerc.ac.uk/collection/W04/current/CAPB0013/"&gt;
>
> &lt;sml:label&gt;Survival Depth&lt;/label&gt;
>
> &lt;sml:uom href="
> http://vocab.nerc.ac.uk/collection/P06/current/ULAA/"/&gt;
>
> &lt;sml:value&gt;1000&lt;/value&gt;
>
> &lt;/sml:Quantity&gt;
>
> &lt;/sml:capability&gt;
>
> &lt;/sml:CapabilityList&gt;
>
> &lt;/sml:capabilities&gt;

#### Vocabularies
| List of terms:  | Minimum terms: | Status:   |
|-----------------|----------------|-----------|
| [W04](http://vocab.nerc.ac.uk/collection/W04/current/)|[*Operating Depth*](http://vocab.nerc.ac.uk/collection/W04/current/CAPB0012/)|
|                 | [*Survival Depth*](http://vocab.nerc.ac.uk/collection/W04/current/CAPB0013/)     |           |
|                 | [*Resolution*](http://vocab.nerc.ac.uk/collection/W04/current/CAPB0007/)     |           |
|                 |Sampling Rate     |           |



### <span id="_llx5qbdflb00" class="anchor"><span id="_Toc485492839" class="anchor"></span></span>CHARACTERISTICS

#### Code style

> &lt;sml:characteristics name="PhysicalCharacteristics"&gt;
>
> &lt;sml:CharacteristicList&gt;
>
> &lt;sml:characteristic name="Weight"&gt;
>
> &lt;sml:Quantity
> definition="http://vocab.nerc.ac.uk/collection/W05/current/CHAR0001/"&gt;
>
> &lt;sml:label&gt;Weight&lt;/ sml:label&gt;
>
> &lt;sml:uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UGKG/"/&gt;
>
> &lt;sml:value&gt;160&lt;/value&gt;
>
> &lt;/sml:Quantity&gt;
>
> &lt;/sml:characteristic&gt;
>
> &lt;sml:characteristic name="Length"&gt;
>
> &lt;sml:QuantityRange
> definition="http://vocab.nerc.ac.uk/collection/W05/current/CHAR0002/"&gt;
>
> &lt;sml:label&gt;Length&lt;/ sml:label&gt;
>
> &lt;sml:uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UXMM/"/&gt;
>
> &lt;sml:value&gt;193 273&lt;/value&gt;
>
> &lt;/sml:QuantityRange&gt;
>
> &lt;/sml:characteristic&gt;
>
> &lt;/sml:CharacteristicList&gt;
>
> &lt;/sml:characteristics&gt;

#### Vocabularies

| List of terms:  | Minimum terms: | Status:   |
|-----------------|----------------|-----------|
| [W05](http://vocab.nerc.ac.uk/collection/W05/current/)|[Width](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0004/)|Optional|
|                 | [Height](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0003/)    |           |
|                 | [Weight](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0001/)     |           |
|                 |[Length](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0002/)      |           |
|                  |Material      |           |
|        |[*Data Storage*](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0006/)     |           |











### <span id="_xok52toc9kae" class="anchor"><span id="_Toc485492843" class="anchor"></span></span>Contacts

#### Code style

> &lt;sml:contacts&gt;
>
> &lt;sml:ContactList&gt;
>
> &lt; sml:contact
> arcrole="http://vocab.nerc.ac.uk/collection/G04/current/001/"&gt;
>
> &lt;gmd:CI\_ResponsibleParty&gt;
>
> &lt; gmd:contactInfo&gt;
>
> &lt; gmd::CI\_Contact&gt;
>
> &lt; gmd:phone&gt;
>
> &lt; gmd:CI\_Telephone&gt;
>
> &lt; gmd:voice&gt;
>
> &lt;gco:CharacterString&gt;+449898989&lt;/gco:CharacterString&gt;
>
> &lt;/ gmd:voice&gt;
>
> &lt;/ gmd:CI\_Telephone&gt;
>
> &lt;/ gmd:phone&gt;
>
> &lt; gmd:address&gt;
>
> &lt; gmd:CI\_Address&gt;
>
> &lt; gmd:deliveryPoint&gt;
>
> &lt;gco:CharacterString&gt;xx YYYYYY
> street&lt;/gco:CharacterString&gt;
>
> &lt;/gmd:deliveryPoint&gt;
>
> &lt;gmd:city&gt;
>
> &lt;gmd:CharacterString&gt;UKPT0811&lt;/gmd:CharacterString&gt;
>
> &lt;/gmd:city&gt;
>
> &lt;gmd:postalCode&gt;
>
> &lt;gco:CharacterString&gt;L3 2BD&lt;/gco:CharacterString&gt;
>
> &lt;/gmd:postalCode&gt;
>
> &lt;/gmd:CI\_Address&gt;
>
> &lt;/gmd:address&gt;
>
> &lt;/gmd:CI\_Contact&gt;
>
> &lt;/gmd:contactInfo&gt;
>
> &lt;gmd:role gco:nilReason="inapplicable"/&gt;
>
> &lt;/CI\_ResponsibleParty&gt;
>
> &lt;/contact&gt;
>
> &lt;sml:contact
>
> xlink:arcrole=" http://vocab.nerc.ac.uk/collection/G04/current/010/"
>
> xlink:href="http://www.myCompany.com/contact/company.xml"/&gt;
>
> &lt;/sml:ContactList&gt;
>
> &lt;/sml:contacts&gt;

<span id="_myf4facr4mp3" class="anchor"></span>

#### Vocabularies

| List of terms for roles from [*G04*](http://vocab.nerc.ac.uk/collection/G04/current/): | Status:  |
|----------------------------------------------------------------------------------------|----------|
| [G04](http://vocab.nerc.ac.uk/collection/G04/current/)                                    | Optional |

### <span id="_iapljiq8q5mb" class="anchor"><span id="_Toc485492844" class="anchor"></span></span>Documentation

#### Code style

&lt;?xml version="1.0"?&gt;

&lt;documentation&gt;

&lt;DocumentList&gt;

&lt;document
arcrole="http://sensorml.com/ont/swe/property/OperationsManual"&gt;

&lt;CI\_OnlineResource&gt;

&lt;linkage&gt;

&lt;URL&gt;http://www.aanderaa.com/media/pdfs/oxygen-optode-4531.pdf&lt;/URL&gt;

&lt;/linkage&gt;

&lt;name&gt; &lt;CharacterString&gt;Aanderaa 4531 oxygen optode
OperationsManual&lt;/CharacterString&gt;&lt;/name&gt;

&lt;description&gt;&lt;CharacterString&gt;Aanderaa 4531 oxygen optode
OperationsManual&lt;/CharacterString&gt;&lt;/description&gt;

&lt;/CI\_OnlineResource&gt;

&lt;/document&gt;

&lt;/DocumentList&gt;

&lt;/documentation&gt;

<span id="_w4vwhjxssk42" class="anchor"></span>

| Status:  |
|----------|
| Optional |

<span id="_8trqckcy9l00" class="anchor"><span id="_Toc485492845" class="anchor"></span></span>PLATFORM INSTANCES
----------------------------------------------------------------------------------------------------------------

### <span id="_bpcr1v982n8w" class="anchor"><span id="_Toc485492846" class="anchor"></span></span>IDENTIFIERS

#### Code style

> &lt;identification&gt;
>
> &lt;IdentifierList&gt;
>
> &lt;identifier&gt;
>
> &lt;Term
> definition="http://vocab.nerc.ac.uk/collection/current/IDEN0009/"&gt;
>
> &lt;label&gt;WMO platform number&lt;/label&gt;
>
> &lt;value&gt;XXXXXXX&lt;/value&gt;
>
> &lt;/Term&gt;
>
> &lt;/identifier&gt;
>
> &lt;IdentifierList&gt;
>
> &lt;identification&gt;

#### Vocabularies

| List of terms:  | Minimum terms: | Status:   |
|-----------------|----------------|-----------|
|[W07](http://vocab.nerc.ac.uk/collection/W07/current/)|[ICES CODE ](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0001/)| Mandatory|
|                 | [CALLSIGN](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0010/)|                                      |       
|                 | [WMO](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0009/)|           |
|                 | [UniqueID](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0008/)|         |
|                 | [Serialnumber](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0005/)|                             |           |                   | [LongName](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0002/) |         |                                   |                 | [ShortName](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0006/)|         |  
|                 | [UUID](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0007/)|         |  

### <span id="_kfyje2tdxpda" class="anchor"><span id="_Toc485492850" class="anchor"></span></span>KEYWORDS

#### Code style

> &lt;keywords&gt;
>
> &lt;KeywordList&gt;
>
> &lt;keyword&gt;SenseOcean&lt;/keyword&gt;
>
> &lt;keyword&gt;BODC&lt;/keyword&gt;
>
> &lt;keyword&gt;NOC&lt;/keyword&gt;
>
> &lt;/KeywordList&gt;
>
> &lt;/keywords&gt;

### <span id="_lkaneg1ftppi" class="anchor"><span id="_Toc485492851" class="anchor"></span></span>CAPABILITIES (if additional from the model add here. if different add them in the output)

#### Code style

> &lt;?xml version="1.0"?&gt;
>
> &lt;capabilities name="MeasurementCapapbilityTEMPPR01"&gt;
>
> &lt;CapabilityList&gt;
>
> &lt;capability name="Latency"&gt;
>
> &lt;QuantityRange
> definition="http://vocab.nerc.ac.uk/collection/W04/current/CAPB0004/"&gt;
>
> &lt;label&gt;Latency&lt;/label&gt;
>
> &lt;uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UTBB/"/&gt;
>
> &lt;value&gt;0 1&lt;/value&gt;
>
> &lt;/QuantityRange&gt;
>
> &lt;/capability&gt;
>
> &lt;capability name="Frequency"&gt;
>
> &lt;Quantity
> definition="http://vocab.nerc.ac.uk/collection/W04/current/CAPB0003/"&gt;
>
> &lt;label&gt;Frequency&lt;/label&gt;
>
> &lt;uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UTHZ/"/&gt;
>
> &lt;value&gt;1&lt;/value&gt;
>
> &lt;/Quantity&gt;
>
> &lt;/capability&gt;
>
> &lt;/CapabilityList&gt;
>
> &lt;/capabilities&gt;

| List of terms:                                         | Status:  |
|--------------------------------------------------------|----------|
| [W04](http://vocab.nerc.ac.uk/collection/W04/current/) | Optional |

### <span id="_a8qjwu9hjv4y" class="anchor"><span id="_Toc485492852" class="anchor"></span></span>CHARACTERISTICS (Additional characteristics diff from model)

#### Code style

> &lt;characteristics name="PhysicalCharacteristics"&gt;
>
> &lt;CharacteristicList&gt;
>
> &lt;characteristic name="Weight"&gt;
>
> &lt;Quantity
> definition="http://vocab.nerc.ac.uk/collection/W05/current/CHAR0001/"&gt;
>
> &lt;label&gt;Weight&lt;/label&gt;
>
> &lt;uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UGKG/"/&gt;
>
> &lt;value&gt;160&lt;/value&gt;
>
> &lt;/Quantity&gt;
>
> &lt;/characteristic&gt;
>
> &lt;characteristic name="Length"&gt;
>
> &lt;QuantityRange
> definition="http://vocab.nerc.ac.uk/collection/W05/current/CHAR0002/"&gt;
>
> &lt;label&gt;Length&lt;/label&gt;
>
> &lt;uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UXMM/"/&gt;
>
> &lt;value&gt;193 273&lt;/value&gt;
>
> &lt;/QuantityRange&gt;
>
> &lt;/characteristic&gt;
>
> &lt;/CharacteristicList&gt;
>
> &lt;/characteristics&gt;

#### Vocabularies

| List of terms: | Status: |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [W05](http://vocab.nerc.ac.uk/collection/W05/current/)        | Optional                                                                                                                                             |

<span id="_9uqu1nzfuc47" class="anchor"><span id="_ijx5mp9l9t4k"
class="anchor"></span></span>

### CONTACTS (Contacts specific to the instance)

#### Code style

> &lt;sml:contacts&gt;
>
> &lt;sml:ContactList&gt;
>
> &lt; sml:contact
> arcrole="http://vocab.nerc.ac.uk/collection/G04/current/CONT0001/"&gt;
>
> &lt;gmd:CI\_ResponsibleParty&gt;
>
> &lt; gmd:contactInfo&gt;
>
> &lt; gmd::CI\_Contact&gt;
>
> &lt; gmd:phone&gt;
>
> &lt; gmd:CI\_Telephone&gt;
>
> &lt; gmd:voice&gt;
>
> &lt;gco:CharacterString&gt;+449898989&lt;/gco:CharacterString&gt;
>
> &lt;/ gmd:voice&gt;
>
> &lt;/ gmd:CI\_Telephone&gt;
>
> &lt;/ gmd:phone&gt;
>
> &lt; gmd:address&gt;
>
> &lt; gmd:CI\_Address&gt;
>
> &lt; gmd:deliveryPoint&gt;
>
> &lt;gco:CharacterString&gt;17 STANDISH
> STREET&lt;/gco:CharacterString&gt;
>
> &lt;/gmd:deliveryPoint&gt;
>
> &lt;gmd:city&gt;
>
> &lt;gmd:CharacterString&gt;UKPT0811&lt;/gmd:CharacterString&gt;
>
> &lt;/gmd:city&gt;
>
> &lt;gmd:postalCode&gt;
>
> &lt;gco:CharacterString&gt;L3 2BD&lt;/gco:CharacterString&gt;
>
> &lt;/gmd:postalCode&gt;
>
> &lt;/gmd:CI\_Address&gt;
>
> &lt;/gmd:address&gt;
>
> &lt;/gmd:CI\_Contact&gt;
>
> &lt;/gmd:contactInfo&gt;
>
> &lt;gmd:role gco:nilReason="inapplicable"/&gt;
>
> &lt;/CI\_ResponsibleParty&gt;
>
> &lt;/contact&gt;
>
> &lt;sml:contact
>
> xlink:arcrole="
> http://vocab.nerc.ac.uk/collection/W08/current/CONT0001/"
>
> xlink:href="http://www.myCompany.com/contact/company.xml"/&gt;
>
> &lt;/sml:ContactList&gt;
>
> &lt;/sml:contacts&gt;

####  Vocabularies

| List of terms   | Status:   |
|-----------------|-----------|
| *G04*           | Mandatory |

###  COMPONENTS (These are the attached sensors)

#### Code style

&lt;?xml version="1.0"?&gt;

&lt;components&gt;

&lt;ComponentList&gt;

&lt;component
href="http://linkedsystems.uk/system/instance/TOOL0969_1234/"/&gt;

&lt;component
href="http://linkedsystems.uk/system/instance/TOOLYSI_89325698/"/&gt;

&lt;component
href="http://linkedsystems.uk/system/instance/TOOLYSI_1234/"/&gt;

&lt;component
href="http://linkedsystems.uk/system/instance/TOOL0969_55555/"/&gt;

&lt;component
href="http://linkedsystems.uk/system/instance/TOOL0969_9898989/"/&gt;

&lt;component
href="http://linkedsystems.uk/system/instance/TOOLYSI_789-654-123/"/&gt;

&lt;/ComponentList&gt;

&lt;/components&gt;

#### Status: Optional

### <span id="_f7i4mzd8d3vn" class="anchor"><span id="_Toc485492857" class="anchor"></span></span>POSITION

#### Code style

##### By location:

A static location can also be provided using a swe:Vector

&lt;position&gt;

&lt;Vector referenceFrame="http://www.opengis.net/def/crs/EPSG/6.7/4326"

&lt;coordinate name="latitude"&gt;

&lt;Quantity
definition="http://vocab.nerc.ac.uk/collection/P07/current/CFSN0600/"
axisID="latitude"&gt;

&lt;uom href="http://vocab.nerc.ac.uk/collection/P06/current/UAAA/"/&gt;

&lt;value&gt;2.3&lt;/value&gt;

&lt;/Quantity&gt;

&lt;/coordinate&gt;

&lt;coordinate name="longitude"&gt;

&lt;Quantity
definition="http://vocab.nerc.ac.uk/collection/P07/current/CFSN0554/"
axisID="longitude"&gt;

&lt;uom href="http://vocab.nerc.ac.uk/collection/P06/current/UAAA/"/&gt;

&lt;value&gt;47.8&lt;/value&gt;

&lt;/Quantity&gt;

&lt;/coordinate&gt;

&lt;/Vector&gt;

&lt;/position&gt;

##### By point:

Position by point supports a static location using the gml:Point
element. It is not appropriate if the orientation of the component is
relevant or the component is has a dynamic location.

&lt;sml:position&gt;

&lt;!-- EPSG 4326 is for latitude-longitude, in that order --&gt;

&lt;gml:Point gml:id="stationLocation"
srsName="http://www.opengis.net/def/crs/EPSG/0/4326"&gt;

&lt;gml:coordinates&gt;47.8 88.56&lt;/gml:coordinates&gt;

&lt;/gml:Point&gt;

&lt;/sml:position&gt;

##### Trajectory

Status: Mandatory (but depends if you model position or outputs)

-   Suggestions are: to refer to the data to get the position

-   To add a bounding box (To be added soon)

-   To list the values of the trajectory vs time (for fast moving ones,
    this can get very long)

&lt;sml:position&gt;

&lt;swe:DataArray definition="Suggestion to create a new vocabulary for
geographical spatial co-ordinate category"&gt;

&lt;swe:elementCount&gt;

&lt;swe:Count&gt;

&lt;swe:value&gt;10&lt;/swe:value&gt;

&lt;/swe:Count&gt;

&lt;/swe:elementCount&gt;

&lt;swe:elementType name="trajectory"&gt;

&lt;swe:DataRecord definition="Suggestion to create a new vocabulary for
geographical spatial co-ordinate category"&gt;

&lt;swe:field name="samplingTime"&gt;

&lt;swe:Time definition="To be added in the "&gt;

&lt;swe:label&gt;Sampling Time&lt;/swe:label&gt;

&lt;swe:uom
xlink:href="[*http://www.opengis.net/def/uom/ISO-8601/0/Gregorian*](http://www.opengis.net/def/uom/ISO-8601/0/Gregorian)"/&gt;

&lt;/swe:Time&gt;

&lt;/swe:field&gt;

&lt;swe:field name="location"&gt;

&lt;swe:Vector
definition="[*http://sensorml.com/ont/swe/property/location*](http://sensorml.com/ont/swe/property/location)"
referenceFrame="[*http://www.opengis.net/def/crs/EPSG/6.7/4326*](http://www.opengis.net/def/crs/EPSG/6.7/4326)"

localFrame="\#SENSOR\_CRS"&gt;

&lt;swe:label&gt;Platform Location&lt;/swe:label&gt;

&lt;swe:coordinate name="Lat"&gt;

&lt;swe:Quantity
definition="[*http://vocab.nerc.ac.uk/collection/P01/current/ALATZZ01*](http://vocab.nerc.ac.uk/collection/P01/current/ALONZZ01/)/"

axisID="Lat"&gt;

&lt;swe:uom code="deg"/&gt;

&lt;/swe:Quantity&gt;

&lt;/swe:coordinate&gt;

&lt;swe:coordinate name="Lon"&gt;

&lt;swe:Quantity
definition="[*http://vocab.nerc.ac.uk/collection/P01/current/ALONZZ01/*](http://vocab.nerc.ac.uk/collection/P01/current/ALONZZ01/)"

axisID="Long"&gt;

&lt;swe:uom code="deg"/&gt;

&lt;/swe:Quantity&gt;

&lt;/swe:coordinate&gt;

&lt;/swe:Vector&gt;

&lt;/swe:field&gt;

&lt;/swe:DataRecord&gt;

&lt;/swe:elementType&gt;

&lt;swe:encoding&gt;

&lt;swe:TextEncoding blockSeparator=" " tokenSeparator=","/&gt;

&lt;/swe:encoding&gt;

&lt;swe:values&gt;

2011-03-01T04:20:00Z,25.72,-61.75

2011-03-14T13:10:00Z,25.49,-61.70

2011-03-21T18:43:00Z,25.35,-61.63

2011-03-30T05:13:00Z,24.87,-61.43

2011-04-08T01:45:00Z,24.86,-61.42

2011-04-12T08:34:00Z,24.32,-61.67

2011-04-15T09:12:00Z,24.54,-61.53

2011-04-21T03:21:00Z,24.53,-61.68

2011-04-27T04:34:00Z,24.32,-61.76

2011-05-01T12:01:00Z,24.28,-61.56

&lt;/swe:values&gt;

&lt;/swe:DataArray&gt;

&lt;/sml:position&gt;

### <span id="_7xe2zqvitw16" class="anchor"><span id="_Toc485492858" class="anchor"></span></span>TYPEOF

#### Code style

&lt;sml:typeOf
xlink:title="National\_Oceanography\_Centre\_waveglider\_General\_platform\_category"
xlink:href="http://linkedsystems.uk/system/prototype/PL898/"/&gt;

### <span id="_jbg8hi4jewog" class="anchor"><span id="_Toc485492859" class="anchor"></span></span>HISTORY

#### Code style

&lt;sml:history&gt;

&lt;sml:EventList&gt;

&lt;sml:event
href="http://vocab.nerc.ac.uk/collection/W03/current/W030002/"&gt;

&lt;sml:Event&gt;

&lt;swe:label&gt;Deployment&lt;/swe:label&gt;

&lt;swe:description&gt;A deployment &lt;/swe:description&gt;

&lt;sml:time&gt;

&lt;gml:TimeInstant id="D07072016"&gt;

&lt;gml :timePosition&gt;2016-07-07T00:00:00Z&lt;/gml :timePosition&gt;

&lt;/gml :TimeInstant&gt;

&lt;/sml:time&gt;

&lt;/sml:Event&gt;

&lt;/sml:event&gt;

&lt;sml:event
href="http://vocab.nerc.ac.uk/collection/W03/current/W030012/"&gt;

&lt;sml :Event&gt;

&lt;swe:label&gt;Decommissioning&lt;/swe :label&gt;

&lt;swe:description&gt;A decommissioning &lt;/swe:description&gt;

&lt;sml:documentation&gt;

&lt;sml:DocumentList&gt;

&lt;sml:document&gt;

&lt;gmd:CI\_OnlineResource&gt;

&lt;gmd:linkage&gt;

&lt;gmd:URL&gt;http://document819path&lt;/gmd:URL&gt;

&lt;/gmd:linkage&gt;

&lt;/gmd:CI\_OnlineResource&gt;

&lt;/ sml:document&gt;

&lt;/ sml:DocumentList&gt;

&lt;/sml:documentation&gt;

&lt;sml:time&gt;

&lt; gml:TimeInstant id="D02082016"&gt;

&lt; gml:timePosition&gt;2016-08-02T00:00:00Z&lt;/ gml:timePosition&gt;

&lt;/gml:TimeInstant&gt;

&lt;/sml:time&gt;

&lt;/sml:Event&gt;

&lt;/ sml:event&gt;

&lt; /sml:EventList&gt;

&lt;/sml:history&gt;

| List of terms:                                                                                         | Status:     |
|--------------------------------------------------------------------------------------------------------|-------------|
| [*http://vocab.nerc.ac.uk/collection/W03/current/*](http://vocab.nerc.ac.uk/collection/G04/current/)   | Mandatory   |

SENSOR MODELS
-------------

### IDENTIFIERS

#### Code style

> &lt;sml:identification&gt;
>
> &lt; sml:IdentifierList&gt;
>
> &lt; sml:identifier&gt;
>
> &lt; sml:Term
> definition="http://vocab.nerc.ac.uk/collection/W07/current/IDEN0012/"&gt;
>
> &lt; sml:label&gt;Manufacturer&lt;/label&gt;
>
> &lt;
> sml:value&gt;http://vocab.nerc.ac.uk/collection/L35/current/MAN0007/&lt;/
> sml:value&gt;
>
> &lt;/Term&gt;
>
> &lt;/ sml:identifier&gt;
>
> &lt; /sml:IdentifierList&gt;
>
> &lt; /sml:identification&gt;

#### Vocabularies

### Vocabularies
| List of terms:  | Minimum terms: | Status:   |
|-----------------|----------------|-----------|
| W07             | [Model name ](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0003/)     | Mandatory |
|                 | [Model number](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0004/)   |           |
|                 | [Manufacturer ](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0012/)   |           |
|                 | [UUID](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0007/)           |           |
|                 | [Unique ID](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0008/)|           |

### CLASSIFICATION

#### Code style

> &lt;sml:classification&gt;
>
> &lt;sml:ClassifierList&gt;
>
> &lt;sml:classifier&gt;
>
> &lt;sml:Term
> definition="http://vocab.nerc.ac.uk/collection/W06/current/CLSS0002/"&gt;
>
> &lt;sml:label&gt;Instrument Type&lt;/ sml:label&gt;
>
> &lt;sml:value&gt;http://vocab.nerc.ac.uk/collection/L05/current/351/&lt;/sml:value&gt;
>
> &lt;/sml:Term&gt;
>
> &lt;/sml:classifier&gt;
>
> &lt;/sml:ClassifierList&gt;
>
> &lt;/sml:classification&gt;

#### Vocabularies

#### Vocabularies
| List of terms:  | Minimum terms: | Status:   |
|-----------------|----------------|-----------|
| [W06](http://vocab.nerc.ac.uk/collection/W06/current/)|[Instrument type](http://vocab.nerc.ac.uk/collection/W06/current/CLSS0002/)|
|                 |Application Domain     |           |


### CAPABILITIES

#### Code style

> &lt;?xml version="1.0"?&gt;
>
> &lt;sml:capabilities name="MeasurementCapapbilities"&gt;
>
> &lt;sml:CapabilityList&gt;
>
> &lt;sml:capability name="Operating depth"&gt;
>
> &lt;sml:QuantityRange definition="
> http://vocab.nerc.ac.uk/collection/W04/current/CAPB0012/"&gt;
>
> &lt;sml:label&gt; Operating depth&lt;/label&gt;
>
> &lt;sml:uom href="
> http://vocab.nerc.ac.uk/collection/P06/current/ULAA/"/&gt;
>
> &lt;sml:value&gt;10 1000&lt;/value&gt;
>
> &lt;/sml:QuantityRange&gt;
>
> &lt;/sml:capability&gt;
>
> &lt;sml:capability name="SurvivalDepth"&gt;
>
> &lt;sml:Quantity definition="
> http://vocab.nerc.ac.uk/collection/W04/current/CAPB0013/"&gt;
>
> &lt;sml:label&gt;Survival Depth&lt;/label&gt;
>
> &lt;sml:uom href="
> http://vocab.nerc.ac.uk/collection/P06/current/ULAA/"/&gt;
>
> &lt;sml:value&gt;1000&lt;/value&gt;
>
> &lt;/sml:Quantity&gt;
>
> &lt;/sml:capability&gt;
>
> &lt;/sml:CapabilityList&gt;
>
> &lt;/sml:capabilities&gt;

#### Vocabularies

| List of terms:  | Minimum terms: | Status:   |
|-----------------|----------------|-----------|
| [W04](http://vocab.nerc.ac.uk/collection/W04/current/)|[*Resolution*](http://vocab.nerc.ac.uk/collection/W04/current/CAPB0007/)|
|                 | [Selectivity](http://vocab.nerc.ac.uk/collection/W04/current/CAPB0010/)         |           |
|                 | [Sensitivity](http://vocab.nerc.ac.uk/collection/W04/current/CAPB0009/)         |           |
|                 | [Accuracy](http://vocab.nerc.ac.uk/collection/W04/current/CAPB0001/)     |           |
|                 | [Frequency](http://vocab.nerc.ac.uk/collection/W04/current/CAPB0003)|     |
|                 | [*Latency*](http://vocab.nerc.ac.uk/collection/W04/current/CAPB0004/)|    |
|                 |*Sampling Rate*    |           |


### CHARACTERISTICS

#### Code style

> &lt;sml:characteristics name="PhysicalCharacteristics"&gt;
>
> &lt;sml:CharacteristicList&gt;
>
> &lt;sml:characteristic name="Weight"&gt;
>
> &lt;sml:Quantity
> definition="http://vocab.nerc.ac.uk/collection/W05/current/CHAR0001/"&gt;
>
> &lt;sml:label&gt;Weight&lt;/ sml:label&gt;
>
> &lt;sml:uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UGKG/"/&gt;
>
> &lt;sml:value&gt;160&lt;/value&gt;
>
> &lt;/sml:Quantity&gt;
>
> &lt;/sml:characteristic&gt;
>
> &lt;sml:characteristic name="Length"&gt;
>
> &lt;sml:QuantityRange
> definition="http://vocab.nerc.ac.uk/collection/W05/current/CHAR0002/"&gt;
>
> &lt;sml:label&gt;Length&lt;/ sml:label&gt;
>
> &lt;sml:uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UXMM/"/&gt;
>
> &lt;sml:value&gt;193 273&lt;/value&gt;
>
> &lt;/sml:QuantityRange&gt;
>
> &lt;/sml:characteristic&gt;
>
> &lt;/sml:CharacteristicList&gt;
>
> &lt;/sml:characteristics&gt;

#### <span id="_tiue72x5hzxx" class="anchor"><span id="_q679h3g3kdrl" class="anchor"><span id="_qkas6iw9it9k" class="anchor"></span></span></span>Vocabularies

| List of terms: | Possible terms:           | <span id="_Toc485492876" class="anchor"></span>Status: |
|----------------|---------------------------|--------------------------------------------------------|
| |[W05](http://vocab.nerc.ac.uk/collection/W05/current/)|     |Optional |
|                |[Width](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0004/)|                  |    
|                |[Height](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0003/)|                  |    
|                |[Weight](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0001/)|                  |    
|                |[Lenght](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0002/)|                  |    
|                |[Data Storage](http://vocab.nerc.ac.uk/collection/W05/current/CHAR0006/)|            |    
|                |Material                                                          |                  |    

### Contacts

#### Code style

> &lt;sml:contacts&gt;
>
> &lt;sml:ContactList&gt;
>
> &lt; sml:contact
> arcrole="http://vocab.nerc.ac.uk/collection/G04/current/001/"&gt;
>
> &lt;gmd:CI\_ResponsibleParty&gt;
>
> &lt; gmd:contactInfo&gt;
>
> &lt; gmd::CI\_Contact&gt;
>
> &lt; gmd:phone&gt;
>
> &lt; gmd:CI\_Telephone&gt;
>
> &lt; gmd:voice&gt;
>
> &lt;gco:CharacterString&gt;+449898989&lt;/gco:CharacterString&gt;
>
> &lt;/ gmd:voice&gt;
>
> &lt;/ gmd:CI\_Telephone&gt;
>
> &lt;/ gmd:phone&gt;
>
> &lt; gmd:address&gt;
>
> &lt; gmd:CI\_Address&gt;
>
> &lt; gmd:deliveryPoint&gt;
>
> &lt;gco:CharacterString&gt;17 STANDISH
> STREET&lt;/gco:CharacterString&gt;
>
> &lt;/gmd:deliveryPoint&gt;
>
> &lt;gmd:city&gt;
>
> &lt;gmd:CharacterString&gt;UKPT0811&lt;/gmd:CharacterString&gt;
>
> &lt;/gmd:city&gt;
>
> &lt;gmd:postalCode&gt;
>
> &lt;gco:CharacterString&gt;L3 2BD&lt;/gco:CharacterString&gt;
>
> &lt;/gmd:postalCode&gt;
>
> &lt;/gmd:CI\_Address&gt;
>
> &lt;/gmd:address&gt;
>
> &lt;/gmd:CI\_Contact&gt;
>
> &lt;/gmd:contactInfo&gt;
>
> &lt;gmd:role gco:nilReason="inapplicable"/&gt;
>
> &lt;/CI\_ResponsibleParty&gt;
>
> &lt;/contact&gt;
>
> &lt;sml:contact
>
> xlink:arcrole=" http://vocab.nerc.ac.uk/collection/G04/current/010/"
>
> xlink:href="http://www.myCompany.com/contact/company.xml"/&gt;
>
> &lt;/sml:ContactList&gt;
>
> &lt;/sml:contacts&gt;

#### Vocabularies

| List of terms from G04 for roles:                                                                    | Status:  |
|------------------------------------------------------------------------------------------------------|----------|
| [G04](http://vocab.nerc.ac.uk/collection/G04/current/) | Optional |

### Documentation

#### Code style

&lt;?xml version="1.0"?&gt;

&lt;documentation&gt;

&lt;DocumentList&gt;

&lt;document
arcrole="http://sensorml.com/ont/swe/property/OperationsManual"&gt;

&lt;CI\_OnlineResource&gt;

&lt;linkage&gt;

&lt;URL&gt;http://www.aanderaa.com/media/pdfs/oxygen-optode-4531.pdf&lt;/URL&gt;

&lt;/linkage&gt;

&lt;name&gt; &lt;CharacterString&gt;Aanderaa 4531 oxygen optode
OperationsManual&lt;/CharacterString&gt;&lt;/name&gt;

&lt;description&gt;&lt;CharacterString&gt;Aanderaa 4531 oxygen optode
OperationsManual&lt;/CharacterString&gt;&lt;/description&gt;

&lt;/CI\_OnlineResource&gt;

&lt;/document&gt;

&lt;/DocumentList&gt;

&lt;/documentation&gt;

| Status:  |
|----------|
| Optional |

### OUTPUTS (Outputs in the model, are inherited to the instance)

#### Code style

&lt;sml:outputs&gt;

&lt;sml:OutputList&gt;

&lt;sml:output name="O2Sat\_2"&gt;

&lt;swe:Quantity
definition="http://vocab.nerc.ac.uk/collection/P01/current/OXYSZZ02/"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/UPCT"/&gt;

&lt;/swe:Quantity&gt;

&lt;/sml:output&gt;

&lt;sml:output name="Latency"&gt;

&lt;swe:Quantity
definition="http://vocab.nerc.ac.uk/collection/W04/current/CAPB0004/"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/UTBB"/&gt;

&lt;swe:value&gt;1&lt;/swe:value&gt;

&lt;/swe:Quantity&gt;

&lt;/sml:output&gt;

&lt;sml:output name="Sample volume"&gt;

&lt;swe:QuantityRange definition="N/A"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/"/&gt;

&lt;/swe:QuantityRange&gt;

&lt;/sml:output&gt;

&lt;sml:output name="Temp"&gt;

&lt;swe:Quantity
definition="http://vocab.nerc.ac.uk/collection/P01/current/TEMPPR01/"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/UPAA"/&gt;

&lt;/swe:Quantity&gt;

&lt;/sml:output&gt;

&lt;sml:output name="WC\_dissO2\_uncalib\_2"&gt;

&lt;swe:Quantity
definition="http://vocab.nerc.ac.uk/collection/P01/current/DOXYUZ02/"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/UPOX"/&gt;

&lt;/swe:Quantity&gt;

&lt;/sml:output&gt;

&lt;/sml:OutputList&gt;

&lt;/sml:outputs&gt;

SENSOR INSTANCES
----------------

### IDENTIFIERS

#### Code style

> &lt;identification&gt;
>
> &lt;IdentifierList&gt;
>
> &lt;identifier&gt;
>
> &lt;Term
> definition="http://vocab.nerc.ac.uk/collection/W07/current/IDEN0009/"&gt;
>
> &lt;label&gt;UUID&lt;/label&gt;
>
> &lt;value&gt;XXXXXXX&lt;/value&gt;
>
> &lt;/Term&gt;
>
> &lt;/identifier&gt;
>
> &lt;IdentifierList&gt;
>
> &lt;identification&gt;

#### Vocabularies

| List of terms:  | Minimum terms: | Status:   |
|-----------------|----------------|-----------|
|[W07](http://vocab.nerc.ac.uk/collection/W07/current/)|[ICES CODE ](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0001/)| Mandatory|
|                 | [UniqueID](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0008/)|         |
|                 | [Serialnumber](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0005/)|                             |           |                   | [LongName](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0002/) |         |                                   |                 | [ShortName](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0006/)|         |  
|                 | [UUID](http://vocab.nerc.ac.uk/collection/W07/current/IDEN0007/)|         |  
                                                                                          |

### KEYWORDS (Keywords can include the sensor outputs from P01)

#### Code style

> &lt;keywords&gt;
>
> &lt;KeywordList&gt;
>
> &lt;keyword&gt;
> http://vocab.nerc.ac.uk/collection/P01/current/TEMPPR01/"&gt;&lt;/keyword&gt;
>
> &lt;keyword&gt;
> http://vocab.nerc.ac.uk/collection/P01/current/OXYSZZ02/"&gt;"&gt;&lt;/keyword&gt;
>
> &lt;keyword&gt;
> http://vocab.nerc.ac.uk/collection/P01/current/TEMPPR01/"&gt;&lt;/keyword&gt;
>
> &lt;/KeywordList&gt;
>
> &lt;/keywords&gt;

### CAPABILITIES (if additional from the model add here. if different add them in the output)

#### Code style

> &lt;?xml version="1.0"?&gt;
>
> &lt;capabilities name="MeasurementCapapbilityTEMPPR01"&gt;
>
> &lt;CapabilityList&gt;
>
> &lt;capability name="Latency"&gt;
>
> &lt;QuantityRange
> definition="http://vocab.nerc.ac.uk/collection/W04/current/CAPB0004/"&gt;
>
> &lt;label&gt;Latency&lt;/label&gt;
>
> &lt;uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UTBB/"/&gt;
>
> &lt;value&gt;0 1&lt;/value&gt;
>
> &lt;/QuantityRange&gt;
>
> &lt;/capability&gt;
>
> &lt;capability name="Frequency"&gt;
>
> &lt;Quantity
> definition="http://vocab.nerc.ac.uk/collection/W04/current/CAPB0003/"&gt;
>
> &lt;label&gt;Frequency&lt;/label&gt;
>
> &lt;uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UTHZ/"/&gt;
>
> &lt;value&gt;1&lt;/value&gt;
>
> &lt;/Quantity&gt;
>
> &lt;/capability&gt;
>
> &lt;/CapabilityList&gt;
>
> &lt;/capabilities&gt;

####  Vocabularies

| List of terms: | Status:  |
|----------------|----------|
| [W06](http://vocab.nerc.ac.uk/collection/W06/current/)          | Optional |

### CHARACTERISTICS (Additional characteristics diff from model)

#### Code style

> &lt;characteristics name="PhysicalCharacteristics"&gt;
>
> &lt;CharacteristicList&gt;
>
> &lt;characteristic name="Weight"&gt;
>
> &lt;Quantity
> definition="http://vocab.nerc.ac.uk/collection/W05/current/CHAR0001/"&gt;
>
> &lt;label&gt;Weight&lt;/label&gt;
>
> &lt;uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UGKG/"/&gt;
>
> &lt;value&gt;160&lt;/value&gt;
>
> &lt;/Quantity&gt;
>
> &lt;/characteristic&gt;
>
> &lt;characteristic name="Length"&gt;
>
> &lt;QuantityRange
> definition="http://vocab.nerc.ac.uk/collection/W05/current/CHAR0002/"&gt;
>
> &lt;label&gt;Length&lt;/label&gt;
>
> &lt;uom
> href="http://vocab.nerc.ac.uk/collection/P06/current/UXMM/"/&gt;
>
> &lt;value&gt;193 273&lt;/value&gt;
>
> &lt;/QuantityRange&gt;
>
> &lt;/characteristic&gt;
>
> &lt;/CharacteristicList&gt;
>
> &lt;/characteristics&gt;

| List of terms: | Status: |
|----------------|---------|
| [W05](http://vocab.nerc.ac.uk/collection/W05/current/)           | Optional|

### CONTACTS (Additional contacts specific to the instance)

#### Code style

> &lt;sml:contacts&gt;
>
> &lt;sml:ContactList&gt;
>
> &lt; sml:contact
> arcrole="http://vocab.nerc.ac.uk/collection/G04/current/CONT0001/"&gt;
>
> &lt;gmd:CI\_ResponsibleParty&gt;
>
> &lt; gmd:contactInfo&gt;
>
> &lt; gmd::CI\_Contact&gt;
>
> &lt; gmd:phone&gt;
>
> &lt; gmd:CI\_Telephone&gt;
>
> &lt; gmd:voice&gt;
>
> &lt;gco:CharacterString&gt;+449898989&lt;/gco:CharacterString&gt;
>
> &lt;/ gmd:voice&gt;
>
> &lt;/ gmd:CI\_Telephone&gt;
>
> &lt;/ gmd:phone&gt;
>
> &lt; gmd:address&gt;
>
> &lt; gmd:CI\_Address&gt;
>
> &lt; gmd:deliveryPoint&gt;
>
> &lt;gco:CharacterString&gt;17 BlUMERG
> STREET&lt;/gco:CharacterString&gt;
>
> &lt;/gmd:deliveryPoint&gt;
>
> &lt;gmd:city&gt;
>
> &lt;gmd:CharacterString&gt;UKPT0811&lt;/gmd:CharacterString&gt;
>
> &lt;/gmd:city&gt;
>
> &lt;gmd:postalCode&gt;
>
> &lt;gco:CharacterString&gt;XXXXX&lt;/gco:CharacterString&gt;
>
> &lt;/gmd:postalCode&gt;
>
> &lt;/gmd:CI\_Address&gt;
>
> &lt;/gmd:address&gt;
>
> &lt;/gmd:CI\_Contact&gt;
>
> &lt;/gmd:contactInfo&gt;
>
> &lt;gmd:role gco:nilReason="inapplicable"/&gt;
>
> &lt;/CI\_ResponsibleParty&gt;
>
> &lt;/contact&gt;
>
> &lt;sml:contact
>
> xlink:arcrole="
> http://vocab.nerc.ac.uk/collection/W08/current/CONT0001/"
>
> xlink:href="http://www.myCompany.com/contact/company.xml"/&gt;
>
> &lt;/sml:ContactList&gt;
>
> &lt;/sml:contacts&gt;

| List of terms for the role:   | Status:     |
|-------------------------------|-------------|
| [G08](http://vocab.nerc.ac.uk/collection/G08/current/)                         | Mandatory   |

###  POSITION (only relative position to the platform)

#### Code style

&lt;sml:position&gt;

> &lt;swe:Vector referenceFrame="EPSG::4326"&gt;
>
> &lt;swe:coordinate name="easting"&gt;
>
> &lt;swe:Quantity axisID="x"&gt;
>
> &lt;swe:uom code="degree"/&gt;
>
> &lt;swe:value&gt;00.0000000&lt;/swe:value&gt;
>
> &lt;/swe:Quantity&gt;
>
> &lt;/swe:coordinate&gt;
>
> &lt;swe:coordinate name="northing"&gt;
>
> &lt;swe:Quantity axisID="y"&gt;
>
> &lt;swe:uom code="degree"/&gt;
>
> &lt;swe:value&gt;00.00000&lt;/swe:value&gt;
>
> &lt;/swe:Quantity&gt;
>
> &lt;/swe:coordinate&gt;
>
> &lt;swe:coordinate name="altitude"&gt;
>
> &lt;swe:Quantity axisID="z"&gt;
>
> &lt;swe:uom code="m"/&gt;
>
> &lt;swe:value&gt;0&lt;/swe:value&gt;
>
> &lt;/swe:Quantity&gt;
>
> &lt;/swe:coordinate&gt;
>
> &lt;/swe:Vector&gt;

&lt;/sml:position&gt;

Vocabularies

| List of terms for the position:   | Status:    |
|-----------------------------------|------------|
| *New vocabulary*                  | Optional   |

### TYPEOF

#### Code style

&lt;sml:typeOf xlink:title="AanderaaOxygenOptode"
xlink:href="<http://linkedsystems.uk/system/prototype/TOOL0969/%22/>&gt;

### <span id="_gjw2lk178rkt" class="anchor"><span id="_Toc485492893" class="anchor"></span></span>ATTACHEDTO

#### Code style

&lt;sml:attachedTo xlink:title="platform name" xlink:href="URI of the
platform"/&gt;

### HISTORY

#### Code style

&lt;sml:outputs&gt;

&lt;sml:OutputList&gt;

&lt;sml:output name="O2Sat\_2"&gt;

&lt;swe:Quantity
definition="http://vocab.nerc.ac.uk/collection/P01/current/OXYSZZ02/"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/UPCT"/&gt;

&lt;/swe:Quantity&gt;

&lt;/sml:output&gt;

&lt;sml:output name="Latency"&gt;

&lt;swe:Quantity
definition="http://vocab.nerc.ac.uk/collection/W04/current/CAPB0004/"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/UTBB"/&gt;

&lt;swe:value&gt;1&lt;/swe:value&gt;

&lt;/swe:Quantity&gt;

&lt;/sml:output&gt;

&lt;sml:output name="Sample volume"&gt;

&lt;swe:QuantityRange definition="N/A"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/"/&gt;

&lt;/swe:QuantityRange&gt;

&lt;/sml:output&gt;

&lt;sml:output name="Temp"&gt;

&lt;swe:Quantity
definition="http://vocab.nerc.ac.uk/collection/P01/current/TEMPPR01/"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/UPAA"/&gt;

&lt;/swe:Quantity&gt;

&lt;/sml:output&gt;

&lt;sml:output name="WC\_dissO2\_uncalib\_2"&gt;

&lt;swe:Quantity
definition="http://vocab.nerc.ac.uk/collection/P01/current/DOXYUZ02/"&gt;

&lt;swe:uom code="UCUMCODE"
xlink:href="http://vocab.nerc.ac.uk/collection/P06/current/UPOX"/&gt;

&lt;/swe:Quantity&gt;

&lt;/sml:output&gt;

&lt;/sml:OutputList&gt;

&lt;/sml:outputs&gt;

| List of terms:   | Status:     |
|------------------|-------------|
| [W03](http://vocab.nerc.ac.uk/collection/W03/current/)            | Mandatory   |

REFERENCES
----------

1.  Portal.opengeospatial.org, 2016.
    \[Online\]. Available:http://portal.opengeospatial.org/files/?artifact_id=21273.
    \[Accessed: 31-Jul- 2016\]

2.  S. Jirka, "Marine Profiles for OGC Sensor Web Enablement Standard",
    in EGU General Assembly, Vienna, 2016, p. 14690

3.  Kokkinaki, Alexandra et al. [“Semantically enhancing SensorML with
    Controlled Vocabularies in the Marine Domain.” (2016).](http://ceur-ws.org/Vol-1762/Kokkinaki.pdf)
