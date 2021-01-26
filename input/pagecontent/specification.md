[Previous Page - Background](background.html)

### FHIR Documents

The Pharmacist Care Plan document relies on the FHIR Documents paradigm. Implementers need to be aware of and follow all the rules required for FHIR Documents. Please refer to that section of the core FHIR spec.

[http://hl7.org/fhir/documents.html](http://hl7.org/fhir/documents.html)


### Actors

This specification defines no new actors beyond those in the C-CDA on FHIR specification. 

### Profiles and Extensions

To claim conformance to a Pharmacist e-Care Plan Profile, servers SHALL:

* Be able to populate all profile data elements that have a minimum cardinality >= 1 and/or flagged as Must Support as defined by that profile’s StructureDefinition.
* Conform to this IG's Server Capability Statement expectations for that profile’s type. 

The following profiles and extensions are present in the specification. Details on these profiles and extensions are available on the [Artifact Index page](artifacts.html). 

#### Resource Profiles

* [PhCP-CareCoordination](StructureDefinition-PhCP-CareCoordination.html)
* [PhCP-Coverage](StructureDefinition-PhCP-Coverage.html)
* [PhCP-MedicationDispense](StructureDefinition-PhCP-MedicationDispense.html)
* [PhCP-Composition](StructureDefinition-PhCP-Composition.html)
* [PhCP-ServiceRequest](StructureDefinition-PhCP-ServiceRequest.html)
* [PhCP-Instruction-Procedure](StructureDefinition-PhCP-Instruction-Procedure.html)
* [PhCP-Encounter](StructureDefinition-PhCP-Encounter.html)
* [PhCP-Organization](StructureDefinition-PhCP-Organization.html)
* [PhCP-Intervention-Procedure](StructureDefinition-PhCP-Intervention-Procedure.html)
* [PhCP-Medication-Therapy-Condition](StructureDefinition-PhCP-Medication-Therapy-Condition.html)

#### Extensions

This implementation guide defines no new extensions beyond those defined in C-CDA on FHIR. 

### Document Bundles

Per the FHIR Document's paradigm, the Composition resource and all references resources must be packaged in a FHIR Bundle resource where Bundle.type = document in order for the content in the Composition resource to be considered a "document". Un-bundled Composition resources are useful while a document is being edited, but until it has been bundled it does not meet the key characteristics of a clinical document (persistence, potential for authentication, etc.). The FHIR specification includes a $document operation on the Composition resource, and FHIR servers that support that operation can handle the task of bundling Composition and other resources. 

See the documentation on the [FHIR Bundle resource](http://hl7.org/fhir/bundle.html) and the [FHIR $document operation](http://hl7.org/fhir/composition-operation-document.html) for more information. 


### US Core and C-CDA on FHIR

The Pharmacist Care Plan specification depends on the C-CDA on FHIR and US Core specifications. 

More information on C-CDA on FHIR can be found [here](https://www.hl7.org/fhir/us/ccda). 
More information on US Core can be found [here](https://www.hl7.org/fhir/us/core). 

### Must Support

This specification uses the same must-support rules as the C-CDA on FHIR specification. 



[Next Page - Acknowledgments](acknowledgments.html)