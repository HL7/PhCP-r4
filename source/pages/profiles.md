---
title: Profiles defined as part of this Guide
layout: default
active: profiles
---

<!-- { :.no_toc } -->

<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}

<!-- end TOC -->

---
<br />

### Profiles

<table>
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="StructureDefinition-PhCP-CareCoordination.html">PhCPCareCoordination</a></td>
<td>This profile represents communication regarding care coordination for the patient. </td>
</tr>
<tr>
<td><a href="StructureDefinition-PhCP-Coverage.html">PhCPCoverage</a></td>
<td>The Coverage profile groups the policy and authorization acts within a Payers Section to order the payment sources. 
The Coverage.identifier is the ID from the patient's insurance card. 
</td>
</tr>
<tr>
<td><a href="StructureDefinition-PhCP-Encounter.html">PhCPEncounter</a></td>
<td>This is where the main encounter information is recorded. It includes codes for describing the care environment. 
This profile constrains the US Core Encounter profile. It includes value sets intended for use by pharmacy systems. Everywhere it is referenced, an unconstrained US Core Encounter reference is also allowed. </td>
</tr>
<tr>
<td><a href="StructureDefinition-PhCP-Instruction-Procedure.html">PhCPInstructionProcedure</a></td>
<td>The Instruction profile can be used in several ways, such as to record patient medication instructions or to record fill instructions for an order. The code defines the type of instruction. 
This profile constrains the US Core Procedure profile. It includes value sets intended for use by pharmacy systems. Everywhere it is referenced, an unconstrained US Core Procedure reference is also allowed. </td>
</tr>
<tr>
<td><a href="StructureDefinition-PhCP-Intervention-Procedure.html">PhCPInterventionProcedure</a></td>
<td>This profile records the pharmacists observation of new information about the patient obtained from monitoring devices such as blood glucose, blood pressure monitors, weight,scales, and movement trackers.
This profile constrains the US Core Procedure profile. It includes value sets intended for use by pharmacy systems. Everywhere it is referenced, an unconstrained US Core Procedure reference is also allowed. 
</td>
</tr>
<tr>
<td><a href="StructureDefinition-PhCP-MedicationDispense.html">PhCPMedicationDispense</a></td>
<td>This profile records the act of supplying medications (i.e., dispensing).</td>
</tr>
<tr>
<td><a href="StructureDefinition-PhCP-Medication-Therapy-Condition.html">PhCPMedicationTherapyCondition</a></td>
<td>This profile represents a medication therapy problem. A medication therapy problem is any undesirable event experienced by a patient that involves, or is suspected to involve, drug therapy, and that interferes with achieving the desired goals of therapy and requires professional judgment to resolve.
This profile constrains the US Core Condition profile. It includes value sets intended for use by pharmacy systems. Everywhere it is referenced, an unconstrained US Core Condition reference is also allowed. 
</td>
</tr>
<tr>
<td><a href="StructureDefinition-PhCP-Organization.html">PhCPOrganization</a></td>
<td>This profile represents the Organization providing the environment of care. 
This profile constrains the US Core Organization profile. It includes value sets intended for use by pharmacy systems. Everywhere it is referenced, an unconstrained US Core Organization reference is also allowed. 
</td>
</tr>
<tr>
<td><a href="StructureDefinition-PhCP-ServiceRequest.html">PhCPServiceRequest</a></td>
<td>This profile represents any of a number of planned interventions for the patient. For example, an activity such as "elevate head of bed" combined with "provide humidified O2 per nasal cannula" may be the interventions performed for a health concern of "respiratory insufficiency" to achieve a goal of "pulse oximetry greater than 92%". These intervention activities may be newly described or derived from a variety of sources within an EHR. Interventions are actions taken to increase the likelihood of achieving the patient's or providers' goals. </td>
</tr>
<tr>
<td><a href="StructureDefinition-PhCP-Composition.html">PharmacistCarePlanDocument</a></td>
<td>The Pharmacist Care Plan standardizes the information gathered and developed through the process of medication planning and management in community, hospital, and long term post-acute care (LTPAC) settings. It allows exchange of information between providers of care to optimize medication-related decision support and patient adherence to medication regimens both within a healthcare setting and when a patient moves between healthcare settings.
Standardization of information used in this form will promote interoperability; support a comprehensive, multi-discipline longitudinal care plan; and create information suitable for reuse in quality measurement, public health reporting, research, and for reimbursement.
In assessment of and consultation with the patient, the Pharmacist Care Plan focuses on:

* 	Maximizing the effectiveness of medications ordered and currently used
* 	Identifying and addressing barriers to successful implementation of the therapy regimen
* 	Assuring patient understanding of the reasons for and use of the medication and the goals of therapy
* 	Resolving conflicting orders and plans

These activities help the patient achieve the best possible outcomes of treatment and an enhanced sense of wellbeing.
</td>
</tr>
</tbody>
</table>


