Download Link: https://assignmentchef.com/product/solved-cis336-lab-2-the-expanded-entity-relationship-diagram
<br>
<header class="entry-header">

 <p class="entry-title">This lab introduces the next step in creating a data model, the Entity Relationship Diagram (ERD). You will be given a business scenario for a University Medical Center, which is a small community hospital. The business specifications will outline a number of things about the business, some of which will apply directly to the database you are being asked to model. There is a table that lists the entities (tables) that will be needed for the database and related attributes (columns) for each entity. There is also a column that lists specific information about the entity that will be helpful in determining its relationship to other entities within the model.

</header>

5/5 - (4 votes)

Be sure to include the minimum and maximum occurrences of each relationship (cardinality) and to supply a name to the relationship that will work in both directions. Make sure to use Crow’s Feet notation in your ERD.

<strong>Narrative/Case Study</strong>The University Medical Center is a small, community hospital. A new hospital administrator has recently been hired by the Board of Directors, and directed to right-size patient care and pharmacy services and improve profitability. The hospital operates three clinical facilities: the main hospital, a mid-town clinic, and an Urgent Care location. The hospital also offers selected in-home care services. Many of the patients are repeat or regular patients who receive regular treatment for various conditions, and many utilize the hospital’s pharmacy services for prescription medications.

The pharmacy dispenses about 3,000 different prescription medications of various kinds. Every prescription is associated with one patient, and is logged by the dispensing clinic. The new administrator wants to know which drugs are most prescribed, and also which are the most profitable.The following is some general information about the organization and its current processes.

<ul>

 <li>The hospital operates three clinical facilities.</li>

 <li>A healthcare worker logs in at a facility at the start of a shift and logs out at the end.</li>

 <li>The name, address, Social Security number and other information is recorded for every healthcare worker.</li>

 <li>All healthcare workers have one billing rate, which is determined by their job description.</li>

 <li>Each medication dispensed by prescription is linked to both the prescription number and the medication ID number, recording the item price and the quantity dispensed.</li>

</ul>

As a convenient and affordable means of providing hospice care, palliative care, and convalescent care to patients that need occasional/intermittent skilled nursing, but do not require hospitalization, the hospital offers limited in-home care. Recording of in-home care includes the healthcare worker ID, their departure time and return time, and also the prescription ID for any prescriptions administered by the healthcare worker in the home setting.

The hospital administrator would like to know what home-care visits have been made to whom, by whom, when, and how long they took. There is concern at this point that the cost of providing limited home healthcare is not providing adequate return on investment, and the program should be revised or discontinued.

<strong>Requirements</strong>You have been asked to develop a logical data model for University Medical Center based on the information given to you by the new hospital administrator and their staff. Through analysis of the nouns and verbs in the case study above, you have accumulated the following entity, attribute, and relationship information shown in the table below. The attribute list may not be complete. If you determine that additional attributes are needed to better define an entity, then you should add them.Entities Attributes and Relationships for University Medical Center (Parallel Lab Exercise):

Entity Attributes Relationships:HealthcareWorker HealthcareWorkerID, LastName, FirstName, SSN, Address, City, State, Zip, Phone Number, HealthcareWorkerTypeID A healthcare worker can belong to any one of the three job categories, but can belong to one and only one of the three. healthcare worker has names and other contact information.HealthcareWorkerType HealthcareWorkerTypeID, HealthcareWorkerTypeDesc, HourlyBillingRate A healthcare worker can be either a physician (diagnoses, prescribes medication), nurse (provides physician-ordered treatments, administers medications), or a pharmacist (dispenses, delivers medication).ClinicLog ClinicLogID, ClinicID, Login, Logout, HealthcareWorkerID Patients may be treated by a healthcare worker at a clinic and can be tracked by the clinic log number. A healthcare worker must sign into the clinic before he or she can serve patients, and must sign out when finished treating patients at that clinic. A healthcare worker may serve portions of a shift at more than one clinic.Clinic ClinicID, ClinicLocationDesc, AMAAccredNum The hospital operates three clinical facilities: General Hospital, Midtown Clinic, and Urgent Care.

InHomeCare InHomeCareID, HealthcareWorkerID, PrescriptionID, DepartTime, ReturnTime. Relates to both the healthcare worker and the prescription entities. This entity will help track provision of home healthcare. A healthcare worker can provide many home visits but a prescription is administered on a home visit by one and only one healthcare worker.

Method MethodID, Method Description Relates to medication and identifies the method of administration, for example, oral, injection, and so on.

Medication MedicationID, MedicationName, Dosage, Cost, QuantityOnHand, LastPurchasedDate, ReorderMinimum Identifies the medication the hospital pharmacy dispenses. One or more medications can be dispensed per prescription. The quantity on hand allows Pharmacists to determine the inventory levels. The reorder minimum can be used to determine when the inventory level has reached a reorder point.Prescription PrescriptionID, MedicationID, BillingAmount, TransactionDateTime, ClinicLogID, PatientID A prescription is identified by a single prescription order. Prescriptions are

<ul>

 <li>made to one or more patients but only one patient at a time;</li>

 <li>made by one or more pharmacists but only one pharmacist per prescription;</li>

 <li>recorded on one or more clinics but only one clinic per prescription; and</li>

 <li>administered by one or more nurses but no one prescription can be administered by more than one nurse.</li>

</ul>

PrescribedMedication PrescriptionID, MedicationID, ItemPrice, QuantityDispensed Prescribed medication is part of a prescription and records medication dispensed per prescription. Prescribed medication must be able to associate multiple medications sold on a single prescription number.

Patient Patient Number, First Name, Last Name, Address, City, State, Zip, Phone Number A patient can be associated with multiple prescriptions, but any one prescription is to one and only one patient. A prescription can occur without a patient registering in the system (e.g., an unconscious patent arrives by ambulance in the emergency room and receives life-saving emergency treatment).

Using an appropriate drawing/data modelling tool, develop an ERD that meets the following guidelines.

<ul>

 <li>Draw the entities with their attributes.</li>

 <li>Indicate the relationships between the entities using Crow’s Foot notation. You will need to determine the cardinality and optionality for each direction of the relationships. Some of the Foreign Key relationships are identified in the graph above but not all. Be sure you identify and account for all Foreign Key relationships.</li>

 <li>Add a name (in both directions) to the relationships. Remember, if you can verbalize the relationship in both directions, then you probably have a valid relationship.</li>

</ul>

<strong>Deliverables</strong>The deliverable for this lab will be your completed ERD as a single MS Word document using copy/paste or imported as an image from your drawing/modelling application, cropped and sized appropriately (it should fit on a single page), and named lab2_solutions_yourname.

<strong>iLAB STEPS</strong><strong>STEP 1:</strong> Drawing Entities and AttributesBe sure to include all of the entities that have been defined. You need to include at least the primary and foreign key attributes where applicable in your diagram.

<strong>STEP 2: </strong>Add RelationshipsBe sure that you link all entities based on PK to FK relationships. There may be a case where you need to identify a combination PK and if so make sure that all of the relationships involved are defined. Be sure that you have set your drawing/modelling tool set to show Crow’s Foot notation. Also, be sure that you are defining the correct cardinality for the relationships.