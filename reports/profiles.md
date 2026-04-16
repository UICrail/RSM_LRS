# OWL Profile Validation Report

**Ontology**: ontology/src/core.ttl
**Date**: 2026-04-16 19:25:52 UTC

---

## OWL2 DL Profile

✅ **Status**: PASSED

```
OWL 2 DL Profile Report: [Ontology and imports closure in profile]
```

## OWL2 RL Profile

⚠️ **Status**: VIOLATIONS DETECTED

```
OWL 2 RL Profile Report: Ontology and imports closure NOT in profile. The following violations are present:
Use of non-superclass expression in position that requires a superclass expression: ObjectOneOf(<https://cdm.ovh/rsm/linearReferencing/rlrs#Absolute> <https://cdm.ovh/rsm/linearReferencing/rlrs#Interpolative> <https://cdm.ovh/rsm/linearReferencing/rlrs#Relative>) [ObjectPropertyRange(<https://cdm.ovh/rsm/linearReferencing/rlrs#linearReferencingMethodType> ObjectOneOf(<https://cdm.ovh/rsm/linearReferencing/rlrs#Absolute> <https://cdm.ovh/rsm/linearReferencing/rlrs#Interpolative> <https://cdm.ovh/rsm/linearReferencing/rlrs#Relative>)) in OntologyID(OntologyIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs>) VersionIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs/0.2/rlrs>))]
Use of non-superclass expression in position that requires a superclass expression: DataSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#icValue> rdfs:Literal) [SubClassOf(<https://cdm.ovh/rsm/linearReferencing/rlrs#IntrinsicPositionExpression> DataSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#icValue> rdfs:Literal)) in OntologyID(OntologyIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs>) VersionIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs/0.2/rlrs>))]
Use of non-superclass expression in position that requires a superclass expression: ObjectSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#distanceExpression> owl:Thing) [SubClassOf(<https://cdm.ovh/rsm/linearReferencing/rlrs#PositionExpression> ObjectSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#distanceExpression> owl:Thing)) in OntologyID(OntologyIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs>) VersionIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs/0.2/rlrs>))]
Use of non-superclass expression in position that requires a superclass expression: ObjectOneOf(<https://cdm.ovh/rsm/linearReferencing/rlrs#Opposite> <https://cdm.ovh/rsm/linearReferencing/rlrs#Same>) [ObjectPropertyRange(<https://cdm.ovh/rsm/linearReferencing/rlrs#positiveDistanceAlongDirection> ObjectOneOf(<https://cdm.ovh/rsm/linearReferencing/rlrs#Opposite> <https://cdm.ovh/rsm/linearReferencing/rlrs#Same>)) in OntologyID(OntologyIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs>) VersionIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs/0.2/rlrs>))]
Use of non-superclass expression in position that requires a superclass expression: ObjectSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#linearElement> owl:Thing) [SubClassOf(<https://cdm.ovh/rsm/linearReferencing/rlrs#LinearPositionExpression> ObjectSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#linearElement> owl:Thing)) in OntologyID(OntologyIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs>) VersionIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs/0.2/rlrs>))]
Use of non-superclass expression in position that requires a superclass expression: ObjectSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#hasLRM> owl:Thing) [SubClassOf(<https://cdm.ovh/rsm/linearReferencing/rlrs#PositionExpression> ObjectSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#hasLRM> owl:Thing)) in OntologyID(OntologyIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs>) VersionIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs/0.2/rlrs>))]
Use of non-superclass expression in position that requires a superclass expression: ObjectSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#offsetUnit> owl:Thing) [SubClassOf(<https://cdm.ovh/rsm/linearReferencing/rlrs#LRMWithOffset> ObjectSomeValuesFrom(<https://cdm.ovh/rsm/linearReferencing/rlrs#offsetUnit> owl:Thing)) in OntologyID(OntologyIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs>) VersionIRI(<https://cdm.ovh/rsm/linearReferencing/rlrs/0.2/rlrs>))]
```
