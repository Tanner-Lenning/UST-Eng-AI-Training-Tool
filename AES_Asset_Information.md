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
- **Description:** Indicates if structural deliveravles require Outsource stamping.
- **Data Type:** Dropdown
- **Required Field:** 
- **Editable:** Yes
- **Engineer Action:** ATC engineers typically should not complete SAs on assets where Outsource stamping is required (Outsource = "Yes").  Confirm with manager vefore proceeding.
- **Data Source:** Jurisdiction/Permitting Entity
- **Notes:** LOV: Yes, No, Undetermined.  Certain states require special licensing requirements for stamping.  Rather than cokplete the SA internally and send to Outsource stamping, the SA tasks are typically outsourced in their entirety.

### **Ignore HMSL**
- **Description:** Toggle to omit wind pressure reductions based on altitude in the structural analysis.
- **Data Type:** Dropdown
- **Required Field:** 
- **Editable:** Yes
- **Data Source:** Jurisdiction/Permitting Entity
- **Notes:** LOV: Yes, No, Undetermined. Some jurisdictions do not permit wind pressure reductions based on altitude as prescribed in TIA-222.  When value = "Yes" the Ground Elevation Factor, K<sub>e</sub>, equals 1.0 for wind pressure, Q<sub>z</sub>, calculations.

### **Allowable Capacity**
- **Description:** Threshold for passing structural result expressed as a percentage.  
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Typically none required.  If Allowable Capacity <> 105% further investigation required to confirm reason and legitimacy.
- **Data Source:** Jurisdiction/Permitting Entity
- **Notes:** Typically 105% as prescribed in TIA code.  Some jurisdictions mandate 100%.  May be reduced to 1% by engineering management to flag critical structural defect pending resolution such as corrosion.  Passing SA Result <= Allowable Capacity < Failing SA Result

### **Automation Candidate**
- **Description:** Flag indicating asset eligibility for structural analysis automation.  
- **Data Type:** Dropdown
- **Required Field:** 
- **Editable:** Yes
- **Engineer Action:** Typically none required.  Engineer can set value to "No" to prevent automated deliverables from running on the asset.  This would be appropriate if an external calculation or analysis is required (ie Excel) or manual changes to the report will be needed.  Always document reason for disabling automation in AES - Notes page for the asset.
- **Notes:** LOV: Yes, No, Undetermined.  If toggled to "No", all projects on the asset will fail **Instant Determination** and will require manual completion of triage and structural deliverable tasks.

### **Analysis Engine**
- **Description:** Indicates the active/preferred software used to perform structural analysis
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** If Non-Standard value (ie <> "SAPS" or "Robot") special training in alternate software required to complete structural analysis.
- **Data Source:** TOW, previous SA
- **Notes:** LOV: SAPS, Robot, Concrete, PLS, Risa, TNX, Wood.  AES platform supports the SAPS and Robot analysis engines.  Ither analysis engines require special training with analysis in external application.  Non-Standard analysis softwares are typically reserved for non-standard tower geometries that are not supported by the AES Model interface.

### **Foundation Analysis Software**
- **Description:** Indicates the method of analyzing the foundation / structure base reactions
- **Data Type:** Dropdown
- **Required Field:** 
- **Editable:** Yes
- **Engineer Action:** Confirm active foundation analysis method is appropriate, update as needed.
- **Data Source:** TFD, MOD, previous structural
- **Notes:** LOV: ATC Standard, Used Reaction Compariosn, Excel.  ATC Standard is the preferred analysis method and analyzes the foundation within the AES platform. Used Reactions Comparison, also referred to as ODRs (Original Design Reactions) is only appropriate under the following conditions: structural analysis must be passing, no propsed tower extension, previous ATC structural analysis on file that used reaction comparison, reaction comparison result < 100% (regardless of **Allowable Capacity**). Many assets with asset number like 4##### (part of Verizon Sequoia Acquisition) will be set to use ODRs, but should be changed to ATC Standard and the foundation modelled and analyzed in AES since the foundation was analyzed by ATC at the time of acquisition. Excel foundation analysis typically reserved for non-standard or modified foundations that are not supported in AES  

### **Fatigue Check**
- **Description:** Toggles fatigue check for monopole structural analysis.
- **Data Type:** Dropdown
- **Required Field:** 
- **Editable:** Yes
- **Engineer Action:** If enabled, engineer MUST perform external fatigue analysis using approved excel tool.  Can be enabled by engineer to reduce structural usage on monopoles.
- **Notes:** LOV: Disabled, Enabled.  Not applicable to lattice towers (Self Support, Guyed).  When enabled the fatigue loadcase is included in the AES analysis and reduces the **Gust Effect Factor**, G<sub>h<\sub>, as prescribed in TIA-222-I. 

### **Galloping Check**
- **Description:** Toggles galloping check for lattice (Self Support, Guyed) tower structural analysis.
- **Data Type:** Dropdown
- **Required Field:** 
- **Editable:** Yes
- **Engineer Action:** If enabled, engineer MUST perform external galloping analysis.
- **Notes:** LOV: Disabled, Enabled.  Galloping check is not currently functional in AES and will be added in a future update.  This field currently has no inpact on the structural analysis and should be ignored until functionality is implemented.

### **Site Specific Climatic Study Date**
- **Description:** Lists date of most recent Site Specific Climatic Study (if applicable)
- **Data Type:** Date
- **Required Field:** No
- **Editable:** No
- **Engineer Action:** If value is not NULL/Empty, engineer ahould expect to use **Topo Method** 2 and verify exposure/topo parametets using SSCS with ATC **Site Parameters** excel spreadsheet.
- **Data Source:** SSCS file (found in file manager site documents)
- **Notes:** Typically there is no SSCS on file and field is NULL/Empty.  In rare cases, there may be an SSCS on file that is not considered in the structural analysis due to the site being located in a hurrican region (**Windspeed**, V, > 115 mph) and ineligible per TIA code.

### **Long-Period Transition Period**
- **Description:** Site Specific transition point on seismic design response spectrum.  Determines what equation is used for calculating spectral reaponse acceleration based on calculated period of the structure.
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify accuracy of value
- **Data Source:** ASCE 7 Hazard Tool
- **Notes:** 

### **Redundancy Factor**
- **Description:** Factor describing redundancy of seismic force resisting system.
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** None typically required
- **Data Source:** Tower type
- **Notes:** Equals 1.0 for pole structures and 1.3 for lattice structures.  Factor modifies horizontal seismic forces.

### **Load Case Azimuth**
- **Description:** Sets wind direction/pole orientation for monpole loadcases with wind.
- **Data Type:** Number
- **Required Field:** 
- **Editable:** Yes
- **Engineer Action:** Verify value/update as needed.
- **Data Source:** Coax Mapping, photos, drone model, Monopole Azimuth Calculator excel spreadsheet
- **Notes:** Not applicable to lattice towers. Only impactful when linear appurtenances with **Exposed To Wind** = "Y" included in analysis.  Load case azimuth should be set to the worst case direction (that which results in the largest applied forces).  Can be thought of as a counterclockwise rotation of applied wind direction (with 0 degrees corresponding to wind from the "top of page" or North to South) or a clockwise rotation of the pole and external linear appurtenances with the wind direction coming from "top of page" or north to south.  Generally acceptable to set load case azimuth orthogonal to coax azimuth if possible (eg if coax located at 90 and/or 270 degrees, load case azimuth of 0 appropriate).  For failing or near-failing analyses with external coax, azimuth should be calculated using excel spreadsheet to determine worst case. Example: coax exposed to wind with azimuth of 60 degrees, a load case azimuth of 30 degrees would orient the coax perpendicular to the applied wind (common mistake is to use 150 degrees thinking that is perpendicular to the coax azimuth of 60 degrees). 

### **Correction Factor**
- **Description:** Used to calculate amount of loading reserved on asset.
- **Data Type:** Number
- **Required Field:** 
- **Editable:** Yes
- **Data Source:** Operations/Acquisition Structural Analysis
- **Notes:** Reserved loading applies to specific carriers only; primarily to Verizon Wireless/Alltel and occasionally to Cellular South Real Estate.  A correction factor (CF) of 1.0 corresponds to a total of 30000 square inches and 2400 lbs of equipment.  Values below or above 1.0 are applied as factors to reduce or increase the carrier's entitled reserve. To calculate the unused reserve, the size/weight of all carrier contracted equipment is summed and subtracted frim the calculated reserved loading entitlement; if this difference is positive then a dummy load is included in the scenario to preeserve the carrier's reserved loading/capacity on the tower.

### **Unused Reserve Automation**
- **Description:** Toggles automated unused reserve calculation within SAT
- **Data Type:** Dropdown
- **Required Field:** 
- **Editable:** Yes
- **Engineer Action:** Typically not required.  If Disabled, reserve must be manually calculated and updated in SAT.
- **Notes:** Hotkey for manual reserve calculation is Alt+U

### **State**
- **Description:** State jurisdictional notes
- **Data Type:** Text
- **Required Field:** No
- **Editable:** No
- **Engineer Action:** Review jurisdictional notes and incorporate into structural analysis as applicable.

### **County**
- **Description:** County jurisdictional notes
- **Data Type:** Text
- **Required Field:** No
- **Editable:** No
- **Engineer Action:** Review jurisdictional notes and incorporate into structural analysis as applicable
- **Notes:** May only apply if **Permitting Entity** is County

### **City**
- **Description:** City jurisdictional notes
- **Data Type:** Text
- **Required Field:** No
- **Editable:** No
- **Engineer Action:** Review jurisdictional notes and incorporate into structural analysis as applicable
- **Notes:** May only apply if **Permitting Entity** is City

### **TIA Standard Details**
- **Description:** Sets TIA code under consideration for all parameters in the **TIA Standard Details** section of Asset Information.
- **Data Type:** Dropdown
- **Engineer Action:** Verify that selected code matches the active **TIA Standard** for the asset.
- **Notes:** LOV: TIA-222-F, TIA-222-G, TIA-222-H, TIA-222-I. Many parameters in the **TIA Standard Details** portion of Asset Information are unique to the selected code while others are shared accross all or multiple standards.  This is denoted in Asset Information by a symbol on the parameter name with a corresponding footnote.

### **Risk Category**
- **Description:** Designated asset risk category based on function and potential hazard to human life in the event of a failure
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Typically none required. If risk category <> II investigate reason and legitimacy.
- **Data Source:** Jurisdictional notes, check X Drive for saved notes/emails
- **Notes:** LOV: II, III, IV.  Default risk category is II.  Some jurisdictions require higher risk category if asset is near high occupancy or essential facilities like a school or hospital, or if the asset supports equipment essential for emergency response.  Analysis parameters from the ASCE 7 Hazard Tool should be retrieved using the relevant risk category input.

### **Exposure**
- **Description:** Asset exposure category used in calculation of K<sub>z<\sub> and K<sub>zt<\sub> wind pressure factors.
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify accuracy of site exposure category and update as needed.
- **Data Source:** Google Earth, Jurisdictional Notes, SSCS, Site Parameters excel spreadsheet
- **Notes:** LOV: B, BC, C, D.  Some jurisdictions may require exposure C or only accept exposure B with a stamped engineering letter providing justification.  Exposure BC is available for intermediate terrain between the discrete cargories  B and C OR C and D.  If exposure BC is used, equivalent Z<sub>0</sub> MUST be calculated using the site parameters excel spreadsheet.

### **Equivalent Z<sub>0</sub>**
- **Description:** Calculated surface roughness for use with exposure caregory BC.
- **Data Type:** Number
- **Required Field:** Yes, iff Exposure = "BC"
- **Editable:** Yes
- **Engineer Action:** Verify calculated value or add value if changing exposure category to BC using site parameters excel spreadsheet.
- **Data Source:** Google Earth, Site Parameters excel spreadsheet
- **Data Source:** Site Parameters Spreadsheet, Google Earth, KML file of worst case exposure path used for calculation should be saved in X Drive structural info folder

### **Topo Factor Procedure**
- **Description:** Specified the procedure/method used to determine site topography
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify that appropriate method is selected.
- **Data Source:** SSCS
- **Notes:** LOV: Method 1, Method 2.  Method 2 corresponds to topography determination using a Site Specific Climatic Study.  Method 1 corresponds to all other cases/sites where a site specific study was not referenced in determining topography.

### **Feature**
- **Description:** Type of topographic feature considered for structural analysis, used in calculating K<sub>zt</sub>.
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify that appropriate feature is selected.
- **Data Source:** Google Earth (Method 1), SSCS and Site Parameters excel spreadsheet (Method 2)
- **Notes:** LOV: Flat, Flat Topped Hill, Flat Topped Ridge, Hill, Ridge, Rolling Hill, Rolling Ridge, Escarpment. If using topo method 2 with a wind study, the calculated/considered topographic feature may not and need not visually match the topography of the site viewed in Google Earth.

### **Crest Height**
- **Description:** Topographic feature measured (Method 1) or calculated (Method 2) crest height used in calculation of K<sub>zt</sub>.
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify that **Crest Height** matches calculated crest height (Method 2) or measured crest height for worst case direction in Google Earth (Method 1).  Update value as needed and save screenshot of measurement in Google Earth and topo path kml file (Method 1) or Site Parameters excel spreadsheet (Method 2) in structural info folder.
- **Data Source:** Google Earth (Method 1), SSCS and Site Parameters excel spreadsheet (Method 2)
- **Notes:** Crest Height must = 0 if **Feature** = "Flat".  Crest Height must be greater than 0 if **Feature** <> "Flat".  Calculated slope, **Crest Height** / **Crest Length**, MUST be greater than 0.1 or AES analysis will not consider wind speed up from topography (K<sub>zt</sub> will be calculated as 1.0) with no warning or indication to the user.

### **Crest Length**
- **Description:** Topographic feature measured (Method 1) or calculated (Method 2) crest length used in calculation of K<sub>zt</sub>.
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify that **Crest Length** matches calculated crest length (Method 2) or measured crest length for worst case direction in Google Earth (Method 1).  Update value as needed and save screenshot of measurement in Google Earth and topo path kml file (Method 1) or Site Parameters excel spreadsheet (Method 2) in structural info folder.
- **Data Source:** Google Earth (Method 1), SSCS and Site Parameters excel spreadsheet (Method 2)
- **Notes:** **Crest Length** is calculated as 2*L<sub>h</sub> where L<sub>h</sub> is the horizontal distance from top of feature to the vertical midpoint of the feature.  A common mistake is for engineers to measure crest length as the horizontal distance from the base to top of the feature.  Calculated slope, Crest Height / Crest Length, MUST be greater than 0.1 or AES analysis will not consider wind speed up from topography (Kzt will be calculated as 1.0) with no warning or indication to the user.

### **Distance from Apex**
- **Description:** Horizontal distance from the apex of the topographic feature considered to the tower site used in calculation of K<sub>zt</sub>.
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify that **Distance from Apex** matches measured value in Google Earth (Method 1) or the distance from crest value considered in the Site Parameters spreadsheet (Method 2).  Update value as needed and save screenshot of measurement in Google Earth and topo path kml file (Method 1) or Site Parameters excel spreadsheet (Method 2) in structural info folder.
- **Data Source:** Google Earth
- **Notes:** Tower sites are often constructed at the top of a topographic feature, so **Distance from Apex** is often 0.  Larger values of **Distance from Apex** decrease the horizontal distance factor K3 which reduces the calculate value of K<sub>zt</sub>. If **Distance from Apex** is relatively large in relation to the **Crest Height** and **Crest Length**, the calculated horizontal distance factor K3 will be 0 and the AES analysis will not consider wind speed up from topography (Kzt will be calculated as 1.0) with no warning or indication to the user.  The horizontal distance factor K3 is a constant and does not change with elevation, so there is no need or reason to use a **Distance from Apex** value other than 0 when calculating topography using Method 2.

### **Upwind/Downwind**
- **Description:** Indicates if the asset is located beyond (Downwind) or before (Upwind) of the topographic feature considered.  Used in calculating K<sub>zt</sub>.
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify that appropriate option is selected based on the site location relative to the crest height for the worst case wind direction considered for topography.
- **Data Source:** Google Earth
- **Notes:** If **Distance from Apex** = 0, the horizontal distance factor K3 will equal 1.0 regardless of **Upwind/Downwind** selection.  For symmetrical topographic features (hills/ridges and their variants), the equation used for calculating K3 is identical for the Upwind and Downwind condition.  Only the K3 and Kzt values for the Escarpment togopgraphic feature are impacted by the **Upwind/Downwind** parameter and only when **Distance from Apex** > 0.

### **Seismic Site Class**
- **Description:** Asset seismic site class designation based on the expected spectral response of the soil.
- **Data Type:** Dropdown
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify that appropriate option is selected. Spectral response parameters from the ASCE 7 Hazard Tool should be taken using the appropriate Site Class input.
- **Data Source:** GEO
- **Notes:** Unless specified in the Geotechnical report, **Seismic Site Class** should be Default.  Site class will not be specified in the GEO for the majority of assets.  Assets in seismically active areas such as CA may have **Seismic Site Class** given in the GEO.

### **Seismic S<sub>DS</sub> Coefficient**
- **Description:** Seismic spectral acceleration at short periods
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify that accuracy of value using ASCE 7 Hazard Tool
- **Data Source:** ASCE 7 Hazard Tool
- **Notes:** Values given in ASCE 7 Hazard Tool depend on **Seismic Site Class**.  Make sure to select the corresponding site class input in the Hazard Tool.  If analysis is failing in Seismic load case, check GEO to see if **Seismic Site Class** is specified and update values if applicable.

### **Seismic S<sub>D1</sub> Coefficient**

- **Description:** Seismic spectral acceleration at 1 second period
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify that accuracy of value using ASCE 7 Hazard Tool
- **Data Source:** ASCE 7 Hazard Tool
- **Notes:** Values given in ASCE 7 Hazard Tool depend on Seismic Site Class. Make sure to select the corresponding site class input in the Hazard Tool. If analysis is failing in Seismic load case, check GEO to see if **Seismic Site Class** is specified and update values if applicable.

### **Annex S**
- **Description:** Toggle to apply load reductions per TIA-222 Annex S.  Offers 5% reduction in wind force and 15% reduction in ice thickness.
- **Data Type:** Dropdown
- **Required Field:** No
- **Editable:** Yes
- **Engineer Action:** Toggle to Yes and rerun analysis if structural analysis is failing
- **Notes:** LOV: Yes, No. If previous ATC analysis used Annex S, it should continue to be used for consistency even if not required to pass.  5% wind load reduction is achieved by reducing the **windspeed** by a factor of (0.95)^0.5 since **wind pressure** is a function of **windspeed** squared.  Not applicable to **Risk Category** III or IV structures.

### **V**
- **Description:** Basic/design windspeed considered in structural analysis.
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify accuracy of value.
- **Data Source:** ASCE 7 Hazard Tool, Jurisdictional Notes, State and Local Codes folder, SSCS (rarely)
- **Notes:** Asset Information also contains override field for manual override of default (ASCE 7 Hazard Tool) value.  Manual override would be appropriate for calculated **Windspeed** from SSCS or as a **Jurisdictional Requirement**. Some jurisdictions require higher windspeeds than those reported by the Hazard Tool.  Design wind speed is dependent on **Risk Category**, make sure to use the correct **Risk Category** input in the Hazard Tool.

### **Ice Windspeed**
- **Description:** Basic/design windspeed for ice loadcase.
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify accuracy of value.
- **Data Source:** ASCE 7 Hazard Tool, SSCS
- **Notes:** Asset Information also contains override field for manual override of default (ASCE 7 Hazard Tool) value.  Manual override would be appropriate for calculated **Ice Windspeed** from SSCS.

### **Ice Thickness**
- **Description:** Design ice thickness for ice loadcase.
- **Data Type:** Number
- **Required Field:** Yes
- **Editable:** Yes
- **Engineer Action:** Verify accuracy of value.
- **Data Source:** ASCE 7 Hazard Tool, SSCS
- **Notes:** Asset Information also contains override field for manual override of default (ASCE 7 Hazard Tool) value.  Manual override would be appropriate for calculated **Ice Thickness** from SSCS. **Ice Thickness** affects the calculated ice dead load and increase in structure and appurtenance effective area for applied wind forces in the ice loadcase.

### **V<sub>T</sub>**
- **Description:** Tornado windspeed
- **Data Type:** Number
- **Required Field:** Yes, iff **Risk Category** III or IV
- **Editable:** Yes
- **Engineer Action:** Consult manager or stamper on how to proceed if value is required.
- **Notes:** Only applicable to **Risk Category** III and IV. AES does not currently support tornado loading.

### **Damping Ratio**
- **Description:** Honestly, I'm not quite sure what this is for, maybe the fatigue check or seismic loads?  Just don't mess with it.
- **Data Type:** Number
- **Required Field:** No
- **Editable:** Yes
- **Notes:** Always seems to be 0.3%. 


