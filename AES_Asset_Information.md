# AES - Asset Information Guide

## Page Layout

Describes the layout and position of links and data fields within the AES - Asset Information user interface.  Sections are defined sequentially from top to bottom and controls defined sequentially within each section.  Controls are described in the following standard format:
- Control/Field Name exactly as it appears within the application ; comma delimited list of psuedonyms if applicable
Descriptions and definitions for the listed controls are included in the subsequent section

### Top Actions Bar
- **Reset**
- **Save**
- Prequalify

### **STANDARD AND ANALYSIS DATA**
- Engineering Class
- **TIA Standard** ; TIA Code, TIA Rev
- Permitting Entity
- IBC Override Code
- IBC Override Reason
- **Jurisdictional Review** ; CMS Jurisdiction
- Jurisdiction Requires SA
- Twist/Sway Limitation
- Outsource
- Ignore HMSL
- Allowable Capacity
- **Automation Candidate**
- **Analysis Engine** ; Analysis Software, Software Type
- **Foundation Analysis Software**
- **Fatigue Check**
- **Galloping Check**
- Site Specific Climatic Study Date
- **Long-Period Transition Period** ; TL, T<sub>L</sub>
- Redundancy Factor
- **Load Case Azimuth**
- Correction Factor
- Unused Reserve Automation

### **JURISDICTIONAL NOTES**
- State
- County
- City

### **TIA STANDARD DETAILS**
- **TIA Standard Details** ; TIA Code, TIA Rev
- **Risk Category** ; Structure Class
- **Exposure**  ; Exposure Category, Exposure Cat
- **Equivalent Z<sub>0</sub>** ; Equivalent Z0, Z0
- **Topo Factor Procedure** ; Topo Procedure, Topographic Factor Procedure, Topo Method, Topgraphy Method
- **Feature** ; Topo Feature, Topographic Feature
- **Crest Height**
- **Crest Length**
- **Distance from Apex** ; Distance from crest
- **Upwind/Downwind**
- Seismic Site Class ; Soil Site Class, Site Class, Site Soil Class
- **Seismic S<sub>DS</sub> Coefficient** ; SDS
- **Seismic S<sub>D1</sub> Coefficient** ; SD1
- **Annex S**
- **V** ; Windspeed, Basic Windspeed, Design Windspeed
- **Ice Windspeed** ; Basic Windspeed with Ice
- **Ice Thickness**
- VT
- Damping Ratio

### **SUPPORTING DOCUMENTS**
- **Tower Drawing** ; TOW, Mapping
- **Foundation Drawing** ; TFD, FDN, Foundation Mapping
- **Geotechnical Report** ; GEO, Geotech
- **Modifications** ; MOD, Mod Drawing
- **Inspection** ; INS
- **Site Specific Study** ; SSCS, Wind Study, Climate Study, ICE Study

## Control Definitions
All buttons and data fields in AES - Asset Information are described in their own sections using the following standard format:

Section Break **Field Name** The label as shown in AES - Asset Information.
- **Description:** What the field represents and its purpose.
- **Data Type:** Expected input type (e.g., Text, Numeric, Dropdown, Boolean).
- **Required Field:** Yes/No – whether the field must be populated for analysis.
- **Editable:** Yes/No – whether the engineer can modify the field in AES.
- **Engineer Action:** Expected action or responsibility for engineer performing structural analysis. 
- **Data Source:** Suggested data source or sources for validating the information shown.
- **Notes:** Additional notes if applicable.

### **Reset**
- **Description:** Reverts/discards all of the user's unsaved changes to the asset information page.
- **Data Type:** Button

### **Save**
- **Description:** Saves/publishes all of the user's changes to the asset information page.
- **Data Type:** Button

### **Prequalify**
- **Description:** Depricated, do not use.
- **Data Type:** Button

### **Engineering Class**
- **Description:** Indicates class of asset (ie lattice tower or pole)
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Typically no action needed unless value is NULL/empty
- **Data Source:** TOW
- **Notes:** LOV: Pole, Tower

### **TIA Standard**
- **Description:** Indicates the active TIA code for structural analysis
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Typically none needed. If TIA Standard is not ANSI/TIA-222-I investigate the reason for using an older code and confirm its legitimacy
- **Data Source:** Check X Drive / Structural Info folder for saved notes or emails.  Check Notes in AES.
- **Notes:** Default TIA Standard is ANSI/TIA-222-I (also known as Rev I).  TIA codes F through I supported

### **Permitting Entity**
- **Description:** Indicates the relevant permitting jurisdictional entity 
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Notes:** LOV: County, City, Override.  Permitting entity may have special requirements for Structural Analyses and can reject the SA if not met.

### **IBC Override Code**
- **Description:** Overrides the jurisdiction default IBC code with the code specified
- **Data Type:** Dropdown
- **Required Field:** No
- **Editable:** Yes, only if **Permitting Entity** = "Override"
- **Notes:** Changes the IBC code listed in the structural analysis deliverable

### **IBC Override Reason**
- **Description:** Freeform textbox to give context on reasoning for using **IBC Code Override**
- **Data Type:** Text
- **Required Field:** No
- **Editable:** Yes, only if **Permitting Entity** = "Override"

### **Jurisdictional Review**
- **Description:** Indicates if structural analyses for the asset are subject to jurisdictional review.
- **Data Type:** Dropdown
- **Required Field:** No
- **Editable:** Yes
- **Engineer Action:** If **Jurisdictional Review** = "Yes", Structural Analysis must include all supporting documentation appended to the report.  Additional requirements may apply depending on the jurisdiction.
- **Data Source:** County/City, Jurisdictional Notes, previous ATC SA.
- **Notes:** LOV: Yes, No, Undetermined.  Certain Counties or Cities always require jurisdictional review.  Additional emphasis on accuracy of structural analysis to avoid jurisdictional rejection.

### **Jurisdictional Requires SA**
- **Description:** Indicates if full structural analysis is required by the jurisdiction or if PE Letters/Opinions are acceptable.
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Notes:** LOV: Yes, No, Undetermined.  Data field supports service determination logic at the triage stage.

### **Twist/Sway Limitation**
- **Description:** Honestly, I'm not sure what this is for just don't mess with it.
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Notes:** LOV: Yes, No, Undetermined.  

### **Outsource**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Ignore HMSL**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Allowable Capacity**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Automation Candidate**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Analysis Engine**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Foundation Analysis Software**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Fatigue Check**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Galloping Check**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Site Specific Climatic Study Date**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Long-Period Transition Period**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Redundancy Factor**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Load Case Azimuth**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Correction Factor**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **Unused Reserve Automation**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **State**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **County**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 

### **City**
- **Description:** 
- **Data Type:** 
- **Required Field:** 
- **Editable:** 
- **Engineer Action:** 
- **Data Source:** 
- **Notes:** 




