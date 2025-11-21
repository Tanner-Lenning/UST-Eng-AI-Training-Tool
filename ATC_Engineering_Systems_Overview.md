# Engineering Department Systems & Applications Reference

---

## Engineering Worklist

The Engineering Worklist is hosted on BI and powered by Oracle Analytics. It is the main source for individuals to track their assigned engineering tasks. Engineers can filter the dashboard by entering their name, which displays active tasks assigned to them. Each project number links directly to the workflow in Siterra. Bookmarking your personalized worklist allows quick access to your filtered tasks. This worklist is the primary way engineers view assigned work and navigate to Siterra project workflows.

---

## Siterra

Accessed via embedded links in the Engineering Worklist. Siterra is the internal application for tracking project milestones and tasks from start to finish. Each project page contains site and asset information, scope, contacts, and customer details. The project schedule, found near the bottom of the page, can be filtered for engineering tasks. Tasks can be revised to allow multiple versions within a project. The Responsibilities tab assigns workflow roles to specific users. The left-hand navigation contains useful links, including access to the Asset Engineering Suite (AES) and project resources.

---

## On Air Access (OAA)

On Air Access (OAA) includes Customer Equipment (CE), which is essential for engineering workflows. It is a database of all equipment and lines on an asset, including proposed changes and non-contracted equipment. Data from Salesforce applications flows into CE and is used to populate loads in the Scenario Analysis Tool (SAT) for structural analysis. OAA also includes:

- **Antenna Central:** Database of antenna models and parameters.
- **Line Central:** Database of line/coax models and parameters.
- **Mount Central:** Database of mount types and manufacturers.

These databases define engineering parameters for antennas, lines, and mounts in the structural analysis.

---

## AES - Home

Accessible via left hand nav of Siterra project.  The Asset Engineering Suite (AES) is a critical application for engineering. The homepage displays a list of engineering models and the structural scenario history. One model is marked as active and is selected by default for structural analysis. Model actions available include viewing, cloning, validating, archiving, and toggling active status. The Scenario History section logs all analyses run on the asset, with options to create new scenarios (standard or mock), clone, tag, analyze, report, lock, and archive.

---

## AES - Analysis/Report

Accessible via scenario actions dropdown or by finalizing a scenario.  The Scenario Analysis page in AES is where engineers select the engineering model, generate load cases, and set parameters before running the structural analysis. After analysis, results are summarized. The Scenario Reports page allows users to download the SA Letter and compile deliverables. The Report Links tab provides direct access to analysis reports from the corresponding scenario analysis.

---

## AES - Asset Information

Accessible via link from AES home page.  The Asset Information page stores all structural analysis parameters for an asset, including TIA Code, risk category, exposure, topography, seismic coefficients, wind speed, and ice thickness. Supporting documents used for analysis are listed here and pulled into the final deliverable. It is crucial that engineering parameters are accurate as this is the data source for parameters used in structural analysis.

---

## ASCE 7 Hazard Tool

Accessible via a link in AES Asset Information, the ASCE 7 Hazard Tool is used to enter site latitude/longitude, select code, risk category, and soil class. It provides wind speed, seismic spectral acceleration, ice thickness, and companion ice wind speed for the site.

---

## File Manager

Accessible via link in AES.  File Manager contains all relevant engineering documents for an asset, including documents, photos, and drawings. By default, it shows tower files and active files, but filters can be adjusted to view site or archived documents. The photos viewer allows access to site and tower photos. The "Drone 3D Model" link provides access to Precision Analytics drone models for the asset.

---

## Scenario Analysis Tool (SAT)

SAT is accessed through AES in the Scenario History section, either by cloning an existing scenario or creating a new one. SAT displays asset-level information and analysis parameters from AES. The Load List includes carrier equipment and lines from Customer Equipment and engineering loads from previous scenarios. Engineers can add, remove, or adjust loads and appurtenances. The preview scenario button shows the final loading configuration before finalizing.  Finalizing the scenario directs the user to the AES Scenario Analysis page.

---

## Network Drives

Key network drives used in engineering:

- **S Drive:** Contains engineering documentation, building codes, jurisdictional standards, manufacturer databases, analysis tools, and approved spreadsheets.
- **T Drive:** Contains folders for each asset, with the history of compiled structural deliverables.
- **X Drive:** Contains folders for each asset with structural engineering documentation, notes, spreadsheets, and supporting documents.

---

## Vanguard Tool

The ATC Engineering Internal Vanguard Tool is built with AutoHotkey and used for efficiency and internal review. Engineers use Vanguard to submit structural analyses for review, receive feedback, and push completed projects to the stamping engineer.

---
