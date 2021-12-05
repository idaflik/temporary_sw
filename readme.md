README

current state of things: (8.10.2021)
- this repo is not online
- this repo is a filtered and more up-to-date version from `/deportation union visualisations/`
- files from "output" folder are at online but in idaflik/data/sw
- html files from / are online but in idaflik/sw-temporary

plan: to make a github account from volunteer@statewatch

input/frontex_docs_converted/
are input/frontex_docs_pdf/
files converted with an online converter.

`clean_data.R` takes:
input/deportation-union-data.xlsx (years 2006 - 2018) (link to statewatch site)
(OBS! Some small mistakes are manually corrected in the repo file, don't replace with original!)
and
input/frontex_docs_converted/ files
and makes them into:

OPERATIONS.csv -> aggregated by ID. FX_STAFF added here

"ID": internally used ID, until 2018 "Number" from Spreadsheet, 2019 + 2020 ROID.
"OPTYPE"
"N_RETURNEES" : total across MS and DESTs
"N_ESC_OBS_MED" : total of escort (leader)s, oberserver, medical staff aggregated (before 2018, only in this aggregate mostly) across MS
"N_ESC": total across MS and DESTs
"N_ESC_LEAD": total across MS and DESTs
"N_FX_STAFF" : frontex staff on operation
"N_MEDS" : total across MS
"N_OBS" : total across MS
"N_MONITORS" : total across MS
"FX_CONTRIB" : total across MS
--
"DATE" : operations span across dates. to find dates of the operation, check OPERATIONS_BY_MS
"ROID": before 2017 instead of RO-IDs there are different codes for each member state. therefore impossible to match one ROID to each operation; check OPERATIONS_BY_MS for Codes and ROIDs involved in each Operation (ID)

OPERATIONS_BY_MS.csv -> aggregated by ID and MS. N_ESC_OBS_MED, N_MEDS, N_OBS, N_MONITORS, FX_CONTRIB added here.
"DATE"
"ROID": "Code" from Spreadsheet. some older "Code" formats have differing formats.
"MSNAME"
"MSISO"
"N_RETURNEES": total across destinations
"N_ESC_OBS_MED" : escort (leader)s, oberserver, medical staff aggregated (before 2018, only in this aggregate mostly)
"N_ESC": total across destinations
"N_ESC_LEAD": total across destinations
"N_MEDS": medical staff from member state
"N_OBS": observers from member state
"N_MONITORS": monitors from member state
"FX_CONTRIB": to member state
"OPTYPE"
"Notes/comments"
"ID": internally used ID, until 2018 "Number" from Spreadsheet, 2019 + 2020 ROID.
"ROWID": year and rownumber (from spreadsheet)

OPERATIONS_BY_DEST_MS.csv

"ROID"
"MSNAME"
"MSISO"
"DEST"
"N_RETURNEES"
"N_ESC": careful, incomplete! (for many years and operations, only aggregated by MS and ESC/ESC_LEAD/MED/OBS is available)
"N_ESC_LEAD" : careful, incomplete! (for some years and operations, only aggregated by MS is available)
"ROWID": year and rownumber (from spreadsheet)
"ID"
