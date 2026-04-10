# Purpose

Create a small LRS ontology for the purpose of RSM.

# Rationale

A successor to a part of the "Positioning" package in RTM. The former Positioning package covered:

* geographic or geometric referencing systems
* linear referencing systems

Geographic or geometric referencing systems are now managed by using GeoSPARQL, and in the future by linking with IFC (for local coordinate systems or track alignment data).

Linear referencing systems remain to be addressed. They are also defined in IFC, which adheres with ISO19148:2021 to a large extent. However at this stage (end of MOTIONAL project) we need a self-standing representation.

# Design guidelines

## ISO 19148:2021 conformance

The ontology is designed in conformance with ISO 19148:2021, with the following adaptations:

* ISO Terminology was re-used:
  * Terms adhere to ISO, except in rare cases where similar terms are used in RSM. For instance, "Linear element" occurs both in RSM topology and in ISO 19148. We disambiguated the ISO term into "Linear element for linear referencing".
  * Definitions do not extensively quote ISO definitions (owing to copyright issues).
* RSM_LRS OWL ontology is derived from the ISO UML class diagrams, with all adaptations required when changing modelling framework.
* RSM_LRS does not transpose the entire ISO, although this would be possible of course. Most concepts were transposed, but many attributes (annotations) and some multiplicities were not transposed.

Conformance verification remains to be performed.

## Evolution since RTM 1.0

The notions of geometric or geographic referencing systems (in 2D or 3D space), linear referencing systems, and intrinsic coordinates were contained in the positioning UML package of RTM 1.1 and 1.2.

Now these three coordinate systems are separated, and the earlier Positioning package was removed.

* The [RSM GeoSPARQL adapter](https://cdm.ovh/rsm/adapters/geosparql_adapter/geo_ad.ttl) takes care of geographic referencing systems.

* Linear referencing is the topic of the present RSM_LRS.

* Other geometric referencing systems (typically, local or project coordinate systems) shall be addressed by IFC.

## Intrinsic coordinates

The notion of "intrinsic coordinate" was part of the RTM positioning package and used is the topology package. It is a normalized distance along a linear element (in the sense of RSM topology), starting from port (extremity) 0 with value 0.0 and ending at port (extremity) 1 with value 1.0. At present:

* intrinsic coordinates are no longer necessary for describing topology (linear element extremities being embodied by "ports");
* intrinsic coordinates remain instrumental in the localisation package, to define linear locations that include segments of linear elements (e.g. the location of a speed reduction or the location of a tunnel)
* intrinsic coordinates are defined (ISO-compliant) as a linear referencing system using a nominal geometry (as ISO Linear element) over a linear net element (in the sense of RSM topology) and using Linear Referencing Method "Interpolating". To implement that definition, the ISO-compliant part of the ontology suffices and does not need adaptations.
* in addition, intrinsic coordinates can be represented using using a dedicated "shorthand" close to earlier RTM/RSM version.