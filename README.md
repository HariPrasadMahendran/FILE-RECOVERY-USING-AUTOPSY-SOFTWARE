# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1600" height="899" alt="dfd-1" src="https://github.com/user-attachments/assets/1b373933-b411-4052-8db9-75458ce0836a" />
<img width="1600" height="899" alt="dfd-2" src="https://github.com/user-attachments/assets/1e1b9d9d-7fec-414b-b15e-3b865a24dcc5" />
<img width="1600" height="900" alt="dfd-3" src="https://github.com/user-attachments/assets/fd838284-2c6b-440d-bfa2-5042feba9a00" />
<img width="1600" height="899" alt="dfd-4" src="https://github.com/user-attachments/assets/cd9723c6-378b-46fd-9a00-4f88a1b9d4d1" />
<img width="1600" height="892" alt="dfd-5" src="https://github.com/user-attachments/assets/cc0d2b8b-2037-4a7d-8524-13c421097688" />
<img width="1600" height="899" alt="dfd-6" src="https://github.com/user-attachments/assets/cd0b874e-ca00-4fbb-8774-c193ee13c818" />
<img width="1600" height="898" alt="dfd-7" src="https://github.com/user-attachments/assets/03ec465d-bf8b-4973-a2a9-b57c4d941ad1" />
<img width="1600" height="899" alt="dfd-8" src="https://github.com/user-attachments/assets/02f8fc7a-c8ff-4ba7-8eac-23396f19e9f9" />
<img width="1600" height="895" alt="dfd-9" src="https://github.com/user-attachments/assets/b5d3b683-81f3-43ee-8550-8e88a6a02712" />
<img width="1600" height="899" alt="dfd-10" src="https://github.com/user-attachments/assets/fcec2e58-2108-4211-9374-61e0d667504d" />
<img width="1482" height="926" alt="dfd-11" src="https://github.com/user-attachments/assets/cba58877-2136-4275-9979-9d106fb47e4e" />




## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
