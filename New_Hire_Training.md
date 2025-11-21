# ATC Engineering New Hire Training Reference

---

## Assigning Work & Project Navigation

- Use the hotkey `Ctrl + Alt + J` to assign work. This sends a request to the remote server, which fetches a project (e.g., a monopole) and returns the project and asset numbers, plus a direct link to the project page.
- To access your project, use your work list and click the project number to go directly to the site page in Siterra.
- Alternatively, paste the project number into Siterra’s search bar. If needed, switch between "Jump to Site" and "Project" modes.

---

## Siterra Workflow & Task Management

- Siterra is filtered to show engineering tasks by default.
- The main structural task is Task 3000. The first two subtasks are usually incomplete and should be completed before submitting for checking.
- If an auto SA (Structural Analysis) is converted to manual, treat it as a typical SA.
- If the first two subtasks are already complete, proceed as normal.
- Use the left-hand navigation in Siterra to access external links, including the AES platform for the asset.

---

## Asset Engineering Suite (AES) — Scenario History & Asset Information

- In AES, scenario history displays different models and links.
- Start with Asset Information, which contains all structural analysis parameters and supporting documents.
- You can toggle between different TIA codes; most projects use Rev I.
- Check wind speed, ice, and seismic parameters. Use the site coordinates and TIA code to jump to the hazard tool (hotkey: `Ctrl + Alt + Space`). If Google Earth Pro is open, it will also jump to the site.
- Assess exposure and topography in Google Earth. Most sites are flat (topo category 1) and use method 1 unless a climate study is available.
- Exposure is usually B; use C for open areas like plains or farms. If in an intermediate area, calculate equivalent exposure (BC) as needed.
- If a tower is failing with exposure C, you may calculate and use BC before sending to checking, but using C is acceptable.
- The checker will provide direction, especially for failing towers.

---

## Hazard Tool & Site Parameters

- Wind speed and other parameters come from the hazard tool, using site latitude/longitude and the standard (ASCE 7-22 for Rev I).
- Ice is often not applicable (NA), and seismic parameters (SDS, SD1, TL) are default unless specified in the geotechnical report.
- In seismically active regions, like California, seismic site class may be specified; otherwise, use the default.

---

## Supporting Documents & Foundation Analysis

- Asset Information lists supporting documents. Modifications (e.g., pole extensions) should be noted.
- The software is usually set to ATC Standard, meaning AES is used for analysis.
- Foundation analysis may use "reactions comparison" instead of validating the foundation model in AES. This uses original design reactions for comparison, simplifying the process.
- If needed, switch from "use reactions comparison" to "ATC Standard" if the reactions comparison fails or if we previously included the foundation analysis in the SA.

---

## Saving & Navigating Models

- After reviewing or editing parameters, click Save.
- Use the Home button to return to the main AES page.
- Access File Manager for the site to view documents and drawings.

---

## Working with Drawings & Historical Documents

- Some tower drawings may be grainy or hard to read. Most are legible, but some scans are poor quality.
- If more information is needed, check the archive for older documents.
- Use discretion when referencing old structural analyses or design drawings. Confirm accuracy when possible.
- Previous structural analyses can be used to check against current designs, especially if they align with the timestamp of design drawings.

---

## Best Practices & Troubleshooting

- Always verify exposure and topography; these are the most likely parameters within Asset Information to require changes.
- Use historical documents and previous analyses as reference, but confirm their relevance and accuracy.
- If foundation analysis fails with reactions comparison, switch to ATC Standard and validate the foundation model.
- Consult the checker for guidance on failing towers or ambiguous exposure/topography cases.

---

# End of Training Reference