Problem Statement: 


Nonprofit organizations play a critical role in providing essential healthcare services to underserved communities. Many of these organizations rely heavily on donations and grants to fund their programs, yet they face a persistent challenge: linking donor contributions to actual healthcare outcomes. While patient health data is often maintained in medical systems and donations are tracked in separate financial systems, there is little to no integration between the two. This disconnect creates a lack of transparency and accountability.

For donors, this issue is particularly concerning. Donors want to see the real-world impact of their contributions—how many patients were treated, what services were provided, and how community health has improved as a result of their support. Without clear visibility, donors may feel uncertain about the effectiveness of their giving, leading to reduced trust, lower donor retention, and decreased funding over time. Nonprofits then struggle not only with sustaining financial support but also with building long-term donor relationships.

On the other side, healthcare workers and program managers face operational difficulties. Generating reports that combine patient outcomes with donor contributions is time-consuming and error-prone. Staff often resort to manual spreadsheets, which are prone to inaccuracies and require significant effort to maintain. This inefficiency slows down decision-making, reduces the ability to measure program effectiveness, and limits opportunities for scaling healthcare initiatives.

The lack of a unified system impacts all stakeholders—patients, who depend on timely healthcare; donors, who expect transparency and accountability; and nonprofits, which need efficiency and sustainability to continue their work.

Therefore, there is a strong need for a centralized solution that integrates patient care data with donation tracking. Such a system should allow healthcare workers to record patient visits and treatments, enable nonprofits to map contributions to specific programs or outcomes, and provide donors with transparent, real-time reports on the impact of their funding. By bridging this gap, nonprofits can strengthen donor relationships, increase funding sustainability, and ultimately improve community healthcare delivery.

🔹 Step-by-Step Execution

Step 1: Create & Configure Org*

* Sign up for *Salesforce Developer Edition*.
* Set *Company Profile* (org name, currency, timezone).
* Enable *My Domain* (needed for Lightning apps).

---

Step 2: Define the Data Model*

* Use *Contacts* for Donors (add field Total_Donations__c).
* Use *Campaigns* for Programs (Health Camp, Vaccination Drive).
* Create *Donation__c* object → fields: Donor, Amount, Date, Campaign.
* Create *Patient__c* object → fields: Name, Age, Gender, Condition, Campaign.
* Create *Treatment__c* object → fields: Patient, Type, Date, Funded_By (Donation).

---

Step 3: Page Layouts & Apps*

* Create a custom *Healthcare App* in App Manager.
* Customize layouts: show related Donations on Donor; Treatments on Patient.
* Add quick actions (e.g., New Donation, New Patient).

---

### *Step 4: Security & Access*

* Define *Roles* (Admin → Program Manager → Volunteer).
* Create *Profiles* (Admin, Healthcare Staff, Donor Manager).
* Set *OWD* = Private for Patients & Donations.
* Use *Sharing Rules* to give managers broader access.

---

Step 5: Automation (Flows)*

* *Flow 1 (Donation Update):* When Donation__c is created, recalc Total_Donations__c on Contact.
* *Flow 2 (Acknowledgment):* Send thank-you email to donor when Donation__c is created.
* *Flow 3 (Optional):* Scheduled monthly impact summary emails.

---

Step 6: Optional Apex Enhancement*

* Add Apex Trigger to auto-update donor totals (instead of Flow).
* Write a Test Class for trigger (ensures deployability).

---

*Step 7: Reports & Dashboards*

* Reports:

  * Total Donations by Campaign.
  * Patients served per Campaign.
  * Donations by Donor.
* Dashboard: Community Impact Overview → donations raised, patients treated, treatments delivered.

---

Step 8: Sample Data Import*

* Use *Data Import Wizard*.
* Upload Donors (Contacts), Patients, Donations, Treatments.
* Link Donations to Campaigns and Donors, Treatments to Patients.

---

Step 9: Testing & Validation*

* Add donation → check donor total updates.
* Add patient & treatment → verify links to campaign & donation.
* Run reports → confirm totals.

---

Step 10: Final Demo Prep*

* Show live flow: Donor → Donation → Auto Email → Linked Campaign → Patients treated → Dashboard.
* Package artifacts: ERD diagram, flow screenshots, Apex code, and reports.

---



Linkedin profile : www.linkedin.com/in/tavishi-baranwal-aba65627a
Project Video link : https://drive.google.com/file/d/16q-RKj8mCgQxtA5Ivq1vIhhcIMFB3Afa/view?usp=sharing
Trailmix Profile : https://www.salesforce.com/trailblazer/nfo667k5lok54uaisl
