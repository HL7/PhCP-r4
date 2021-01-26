[Previous Page - Home Page](index.html)

### Purpose

This document describes constraints on the C-CDA on FHIR header and body elements for the Pharmacist Care Plan, which are derived from requirements set forth by the Pharmacy Health Information Technology (HIT) Collaborative  and the National Council for Prescription Drug Programs (NCPDP) WG10 Professional Pharmacy Services,  vendors, and Health Level Seven (HL7) stakeholder workgroups. Templates in this US Realm implementation guide are specific to pharmacy management treatment and interventions that will promote interoperability and will create information suitable for reuse in quality measurement, public health reporting, research, and reimbursement.

This guide contains a library of FHIR profiles and is compliant with FHIR Release 4.  

### Audience

The audience for this document includes pharmacy vendors, software developers, and implementers with reporting capabilities within their electronic health record (EHR) systems; developers and analysts in receiving institutions; and local, regional, and national health information exchange networks who wish to create or process pharmacy clinical documents according to this specification.

Business analysts and policy managers can also benefit from a basic understanding of the use of FHIR profiles across multiple implementation use cases.

### General Background

Pharmacists work in multiple environments (community, hospital, long term care, clinics, etc.) and increasingly participate in patient-centered care teams providing essential clinically-oriented patient care services such as medication therapy management, clinical reconciliation (medication, allergies and problems), patient immunization management, disease state monitoring, and therapy adherence programs. These services reduce adverse drug events, improve patient safety, and optimize medication use and health outcomes. Pharmacists are integral members of the health care team and have unique and frequent access to patients, routinely working with patients to facilitate understanding and compliance with drug regimens, reconcile medications from multiple prescribers, and monitor effectiveness of the treatment. These activities affect the treatment plans of other caregivers. Having a medication-related plan of care shared with those providers and incorporated with care plans developed by other care team members is critical to the overall success of patients reaching their proposed care goals of care. 

Today, pharmacists document within proprietary systems that do not export and cannot receive standards-based data. Where care plan information is shared from pharmacy management systems, it is done using proprietary interfaces and free text; there is no standard covering pharmacist care plans. Thus, sharing data requires time consuming redundant data entry which is a major factor limiting care planning. Furthermore, care plan documentation that is free text is inconsistent and incapable of supporting electronic quality measurement and reporting. 


### Current Project

The current project specifies the Pharmacist Care Plan, an electronic care plan document with enhanced medication management content based on the profiles in the C-CDA on FHIR specification. The Pharmacist Care Plan is a standardized, interoperable document containing information on medication-related activities, as well as patient-provider shared goals and plans for care. The Pharmacist Care Plan identifies resources for and obstacles to patient compliance with the recommended treatment. This type of data is not often captured in a structured and standard format that can be used for research, quality measurement, or public health reporting. The Pharmacist Care Plan supports the strategy of interoperability and information exchange promoting coordination of care among a variety of settings, thus improving the quality of care for the patient. 

The Pharmacist Care Plan serves two needs. It supports the CMS Medicare Part D Enhanced Medicare Therapy Management (MTM) program that started on January 1, 2017. The program launched a pilot in five Medicare Part D regions. Program participants in these regions have the opportunity coordinate care with pharmacy providers on issues related to medication management and adverse outcomes through the MTM model of enhanced care, which includes an individuals goals for therapy and outcomes. 

Secondly, the movement towards value-based payment (VBP) models has recognized pharmacists as an important part of the well-connected care team that addresses the needs of the patient.  In a VBP model, a patients care is coordinated, managed, and supported through documentation of goals and outcomes. The Pharmacist Care Plan provides that documentation for medications and medication-related issues.

The current project builds on the work started in the NCPDP Pharmacist eCare Plan, which provides guidance for pharmacist and vendors as they implement the standard CDA R2.1 Care Plan document. The Pharmacist Care Plan electronic document standardizes exchange of information on medications dispensed and medication therapy problems which are not specified in the current Care Plan document type. This version contains reconciled ballot comment changes and includes pharmacy HIT value sets that are published in the Value Set Authority Center (VSAC). 

The project has implemented both the CDA and the FHIR (Fast Healthcare Interoperability Resources) Pharmacist Care Plan specifications in a pilot at Community Care of North Carolina (CCNC) and ongoing use at Community Pharmacy Enhanced Service Network (CPESN) USA.. Please note, this FHIR Pharmacist Care Plan is balloted separately from the CDA standard. The burden of redundant data entry is a major factor limiting care planning to less than 15% of the CCNC population, which includes many at risk and care-intensive patients. Reducing redundant data entry and providing standard, structured data will enhance the ability of pharmacists to engage with patients and will improve the patient experience of care through comprehensive medication review with the pharmacists and care managers. Facilities received Pharmacist Care Plan files in both CDA and FHIR formats from implementing EHRs. In addition, participating systems convert CDA-based Pharmacist Care Plans to the FHIR format using transformation files.

### Use Cases

This implementation guide meets the need of four use cases unique to the pharmacy environment.  Though the scope of the pilot testing focused on Use Case 4, the standard was designed to meet the needs for clinical data exchange in each of the cases described in this section.

#### Use Case 1: New condition for a patient at risk for a pulmonary embolism

<table><tr><td><img src="phcp_use_case_1.png" alt="phcp-use-case-1" /></td></tr></table>

The community pharmacist meets with the patient and the caregiver after a recent discharge from a hospital for a pulmonary embolism. The patient is diagnosed with hypertension and diabetes. The patient has been enrolled in a diabetes outpatient clinic and has now been referred to an anticoagulation outpatient clinic. 
The community pharmacist coordinates medication therapy management services (including reconciliation of medications, allergies and indications for medication use) with the primary care provider (PCP) and the diabetes and anticoagulation clinics and documents the patients medication-related goals. The pharmacy generates the Pharmacist Care Plan to share medication related goals and electronically delivers the Care Plan to the patient, the PCP, and the outpatient clinics for chronic care management and care coordination.

#### Use Case 2: Patient scheduled for a hip replacement

<table><tr><td><img src="phcp_use_case_2.png" alt="phcp-use-case-2" /></td></tr></table>

The pharmacist, under a collaborative practice agreement with the orthopedic surgeon, counsels the patient prior to the procedure to ensure there are no medication-related problems. After the surgery, the pharmacist coordinates medication-related goals with the patient pertaining to deep vein thrombosis risk and pain management. 

The community pharmacist uses a health IT system to document patient care. The health IT system generates the Pharmacist Care Plan to share the medication related goals electronically with the patient, orthopedic surgeon, PCP, home health care agency, and the rehabilitation center for care coordination.

#### Use Case 3: Patient with behavioral health issues and multiple chronic diseases meets with a consultant pharmacist for the yearly comprehensive medication review to meet Medicare Part D MTM requirement

<table><tr><td><img src="phcp_use_case_3.png" alt="phcp-use-case-3" /></td></tr></table>

The pharmacist documents conflicting treatment strategies and medications. The pharmacist recommends strategies/alterations to existing treatment, development of a manageable medication schedule, patient education, and outcome follow-up.

The community pharmacist uses a health IT system to document patient care. The health IT system generates the Pharmacist Care Plan to share the medication related goals and strategies electronically with the patient, the psychiatrist, the outpatient psychiatric clinic, and the PCP or chronic care management and care coordination.

#### Use Case 4: Patient comes to the community pharmacy to pick up hydrocodone, which has been e-prescribed and complaints of constipation

<table><tr><td><img src="phcp_use_case_4.png" alt="phcp-use-case-4" /></td></tr></table>

The pharmacist reviews the state Prescription Drug Monitoring Program (PDMP) database and discovers that multiple physicians have treated the patient for pain. The pharmacist suspects the patient may have an opioid abuse condition. Through patient assessment using a validated nutrition screening tool, the pharmacist discovers the patient shows signs of potential malnutrition, has three chronic care conditions, complains of constipation, and has no PCP. The pharmacist performs comprehensive medication review and helps the patient identify a PCP.

The community pharmacist documents conflicting treatment strategies and medications including the need for naloxone. The pharmacist recommends strategies/alterations to existing treatment, pain management, development of a manageable medication schedule, nutritional counseling, patient education, and outcome follow-up.

### Mappings

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





[Next Page - Specification](specification.html)