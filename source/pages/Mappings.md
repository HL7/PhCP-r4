---
title: Mappings
layout: default
active: Mappings
---

[Previous Page](Use_Cases.html)

The following table contains mappings between the CDA and FHIR versions of the Pharmacist Care Plan document type. 

<table class="table table-bordered table-hover table-condensed">
<thead><tr><th title="Field #1">Data Element</th>
<th title="Field #2">FHIR Contained by</th>
<th title="Field #3">FHIR Resource</th>
<th title="Field #4">FHIR Element Path</th>
<th title="Field #5">CDA Section</th>
<th title="Field #6">CDA Mapping</th>
</tr></thead>
<tbody><tr>
<td>Date of the Report</td>
<td> </td>
<td>Composition [PhCP-Composition]</td>
<td>date</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/effectiveTime</td>
</tr>
<tr>
<td>ID of the PhCP Document</td>
<td> </td>
<td>Composition [PhCP-Composition]</td>
<td>id</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/id</td>
</tr>
<tr>
<td>Provider ID</td>
<td>PhCP-Encounter.particpant</td>
<td>Practitioner</td>
<td>identifier</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/responsibleParty/assignedEntity/id</td>
</tr>
<tr>
<td>Provider Name</td>
<td>PhCP-Encounter.participant</td>
<td>Practitioner</td>
<td>name</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/responsibleParty/assignedEntity/assignedPerson/name</td>
</tr>
<tr>
<td>Provider Phone</td>
<td>PhCP-Encounter.participant</td>
<td>Practitioner</td>
<td>telecom[system=&quot;phone&quot;]</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/responsibleParty/assignedEntity/telecom</td>
</tr>
<tr>
<td>Provider Fax</td>
<td>PhCP-Encounter.participant</td>
<td>Practitioner</td>
<td>telecom[system=&quot;fax&quot;]</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/responsibleParty/assignedEntity/telecom</td>
</tr>
<tr>
<td>Provider Email</td>
<td>PhCP-Encounter.participant</td>
<td>Practitioner</td>
<td>telecom[system=&quot;email&quot;]</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/responsibleParty/assignedEntity/telecom</td>
</tr>
<tr>
<td>Provider Facility/Office Name</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>name</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/location</td>
</tr>
<tr>
<td>Provider Address</td>
<td>PhCP-Encounter.participant</td>
<td>Practitioner</td>
<td>address</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/responsibleParty/assignedEntity/addr</td>
</tr>
<tr>
<td>Facility ID Number</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>identifier</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/location/healthCareFacility/id</td>
</tr>
<tr>
<td>Facility Name</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>name</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/location/healthCareFacility/serviceProviderOrganization/name</td>
</tr>
<tr>
<td>Facility Type</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>type</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/location/healthCareFacility/serviceProviderOrganization/code</td>
</tr>
<tr>
<td>Facility Phone</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>telecom[system=&quot;phone&quot;]</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/location/healthCareFacility/serviceProviderOrganization/telecom[@use=&quot;phone&quot;]</td>
</tr>
<tr>
<td>Facility FAX</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>telecom[system=&quot;fax&quot;]</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/location/healthCareFacility/serviceProviderOrganization/telecom</td>
</tr>
<tr>
<td>Facility Address</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>address</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/location/healthCareFacility/location/addr</td>
</tr>
<tr>
<td>Patient ID Number</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>identifier</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/id</td>
</tr>
<tr>
<td>Patient Name</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>name</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/name</td>
</tr>
<tr>
<td>Patient Phone</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>telecom[system=&quot;phone&quot;]</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/telecom</td>
</tr>
<tr>
<td>Patient Email</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>telecom[system=&quot;email&quot;]</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/telecom</td>
</tr>
<tr>
<td>Parent/ Guardian Name</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>contact</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/guardian/guardianPerson/name</td>
</tr>
<tr>
<td>Parent/ Guardian Phone</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>contact.telecom[system=&quot;phone&quot;]</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/guardian/telecom</td>
</tr>
<tr>
<td>Parent/ Guardian Email</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>contact.telecom[system=&quot;email&quot;]</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/guardian/telecom</td>
</tr>
<tr>
<td>Patient Street Address</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>address</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/addr</td>
</tr>
<tr>
<td>Patient Birth Date</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>birthDate</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/birthTime</td>
</tr>
<tr>
<td>Patient Sex</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>gender</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/administrativeGenderCode</td>
</tr>
<tr>
<td>Patient Race</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>extension</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/raceCode</td>
</tr>
<tr>
<td>Patient Ethnicity</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>extension</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/ethnicGroupCode</td>
</tr>
<tr>
<td>Preferred Language</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>communication.language</td>
<td>US Realm Header (V3)</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/languageCommunication</td>
</tr>
<tr>
<td>Occupation</td>
<td>Composition.section</td>
<td>Observation</td>
<td>value</td>
<td>Social History Section (V3)</td>
<td>Social History Observation (V3)/code</td>
</tr>
<tr>
<td>Pregnant</td>
<td>Composition.section</td>
<td>Observation</td>
<td>value</td>
<td>Social History Section (V3)</td>
<td>Pregnancy Observation/code</td>
</tr>
<tr>
<td>Hospital Unit</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>type</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/location/healthCareFacility/code</td>
</tr>
<tr>
<td>Visit Date/Time</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>period.start</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/effectiveTime/low</td>
</tr>
<tr>
<td>Admission Date/Time</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>period.start</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/effectiveTime/low</td>
</tr>
<tr>
<td>Discharge Date/Time</td>
<td>PhCP-Encounter.location</td>
<td>Location</td>
<td>period.end</td>
<td>Pharmacist Care Plan Document</td>
<td>ClinicalDocument/componentOf/encompassingEncounter/effectiveTime/high</td>
</tr>
<tr>
<td>History of Present Illness</td>
<td> </td>
<td>Composition.section</td>
<td>text</td>
<td>History of Present Illness Section</td>
<td>text</td>
</tr>
<tr>
<td>Reason for Visit</td>
<td> </td>
<td>Composition.section</td>
<td>text</td>
<td>Reason for Visit Section</td>
<td>text</td>
</tr>
<tr>
<td>Date of Onset</td>
<td>Composition.section</td>
<td>Condition</td>
<td>onset</td>
<td>Problem Section (entries required) (V3)</td>
<td>Problem Concern Act (V3)/Problem Observation (V3)/effectiveTime + Problem Concern Act (V3)/Initial Case Report Trigger Code Problem Observation/effectiveTime</td>
</tr>
<tr>
<td>Symptoms (list)</td>
<td>Compostion.section</td>
<td>Observation</td>
<td>code</td>
<td>Problem Section (entries required) (V3)</td>
<td>Problem Concern Act (V3)/Problem Observation (V3)/value</td>
</tr>
<tr>
<td>Lab Order Code</td>
<td>Composition.section</td>
<td>ServiceRequest</td>
<td>code</td>
<td>Plan of Treatment Section (V2)</td>
<td>Planned Observation (V2)/code</td>
</tr>
<tr>
<td>Lab Order Code (Trigger)</td>
<td>Composition.section</td>
<td>ServiceRequest</td>
<td> </td>
<td>Plan of Treatment</td>
<td> </td>
</tr>
<tr>
<td>Laboratory Results</td>
<td>Composition.section</td>
<td>Observation</td>
<td>code OR value</td>
<td>Results Section (V3)</td>
<td>Result Observation (V3)/code OR Result Observation (V3)/value</td>
</tr>
<tr>
<td>Laboratory Result (Trigger)</td>
<td>Composition.section</td>
<td>Observation</td>
<td> </td>
<td>Results Section (V3)</td>
<td> </td>
</tr>
<tr>
<td>Filler Order Number</td>
<td>Composition.section</td>
<td>Observation</td>
<td>identifier</td>
<td>Results Section (V3)</td>
<td>Result Organizer (V3)/id</td>
</tr>
<tr>
<td>Diagnoses</td>
<td>Composition.section</td>
<td>Observation</td>
<td>code</td>
<td>Problem Section (entries required) (V3)</td>
<td>Problem Observation (V3)/code</td>
</tr>
<tr>
<td>Diagnosis (Trigger)</td>
<td>Composition.section</td>
<td>Observation</td>
<td> </td>
<td>Problem Section (entries required) (V3)</td>
<td> </td>
</tr>
<tr>
<td>Date of Diagnosis</td>
<td>Composition.section</td>
<td>Observation</td>
<td>effective[x]</td>
<td>Problem Section (entries required) (V3)</td>
<td>Problem Observation (V3)/effectiveTime</td>
</tr>
<tr>
<td>Medications Administered (list)</td>
<td>Composition.section</td>
<td>MedicationStatement</td>
<td>medication[x]</td>
<td>Medications Administered Section (V2)</td>
<td>Medication Information (V2)/manufacturedMaterial/code</td>
</tr>
<tr>
<td>Death Date</td>
<td>Composition.subject</td>
<td>Patient</td>
<td>deceased[x]</td>
<td>Pharamacist Care Plan Document</td>
<td>ClinicalDocument/recordTarget/patientRole/patient/sdtc:deceasedInd</td>
</tr>
<tr>
<td>Immunization Status</td>
<td>Composition.section</td>
<td>Immunization</td>
<td>status</td>
<td>Immunizations Section (entries required) (V3)</td>
<td>Immunization Activity (V3)/statusCode</td>
</tr>
<tr>
<td>Travel History Dates</td>
<td>Composition.section</td>
<td>Observation</td>
<td>effective[x]</td>
<td>Social History Section (V3)</td>
<td> </td>
</tr>
<tr>
<td>Travel History Location - Free Text</td>
<td>Composition.section</td>
<td>Observation</td>
<td>valueCodeableConcept.text</td>
<td>Social History Section (V3)</td>
<td> </td>
</tr>
<tr>
<td>Travel History Location - Coded</td>
<td>Composition.section</td>
<td>Observation</td>
<td>valueCodeableConcept.coding</td>
<td>Social History Section (V3)</td>
<td> </td>
</tr>
<tr>
<td>Travel History Location - Address</td>
<td>Composition.section</td>
<td>Observation</td>
<td> </td>
<td>Social History Section (V3)</td>
<td> </td>
</tr>
</tbody></table>

null