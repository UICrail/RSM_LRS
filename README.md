# Purpose

Create a small LRS ontology for the purpose of RSM.

# Rationale

A successor to a part of the "Positioning" package in RTM. The former Positioning package covered:

* geographic or geometric referencing systems
* linear referencing systems

Geographic or geometric referencing systems are now managed by using GeoSPARQL, and in the future by using IFC (for local coordinate systems).

Linear referencing systems remain to be addressed. They are also defined in IFC, which adheres with ISO19148 to a large extent. However at this stage (end of MOTIONAL project) we need a simplified, self-standing representation.

Semantic links with IFC are obviously welcome, especially w.r.t. future evolutions.

# Design guidelines

The [RSM GeoSPARQL adapter](https://cdm.ovh/rsm/adapters/geosparql_adapter/geo_ad.ttl) already introduced the concepts of nominal geometry: typically, a 2D geometry (e.g. derived from public data such as OpenStreetMap) from which nominal placement of linear elements on maps and nominal length of such elements can be derived.

> Note: while OpenStreetMap is a rich and useful source of railway network information, the high uncertainty of longitudinal node placement in OSM (where tracks diverge at switches is a tangential point that is hard to observe precisely) makes IM sources preferrable when available.

Since network topology is deemed very stable in time and associated geometries need not be revised frequently, we chose not to use a DUL "Situation" pattern for describing their evolution. Geometry change can be accomodated with simpler means (triple annotations or versionad named graphs). This choice would not apply to IfcAlignment-related data that are much more detailed and serve track geometry specification and monitoring. In the latter case, SOSA/SSN patterns and their generalization to specifications (POP) are essential. These patterns replace simple properties such as "hasGeometry" by reified properties, complete with source, timestamp, and any other relevant information.

In the versions of RSM developed under LinX4Rail, and in absence of a "nominal geometry", intrinsic coordinates along a linear element were downgraded:

* from being a linear referencing system using extremal coordinates 0 and 1 and an interpolation method for intermediate values, to
* a mere support for a total order relation along the element.

It was possible to state in what succession net entities would appear along the linear element, but the way coordinates are derived was left to the user.

In the present case, we follow the current (semantic RSM) topology definition, where each linear element is a geo:Feature and may be associated with a geo:Geometry. We use the 'hasNominalGeometry' property defined by GeoSPARQL to derive a 'NominalLRS' associated with each linear element.

Linear locations refer to linear elements. Their nominal geometry may be obtained by assembling nominal geometries of linear elements (or segments thereof). This derivation was not suggested, let alone enforced, by the geosparql adapter ontology. The adapter only states its existence of a nominal geometry applying to linear elements in a 1-to-1 relationship.

In RSM Linear referencing systems (not defined as such in ISO 19148) are defined by a linear location, one particular associated geometry (nominal or not), and an interpolation method (following ISO 19148). The chosen geometry is equivalent to an ISO19148 referent.
