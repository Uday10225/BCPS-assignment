# BCPS Computer Practical Labs 1–10 — Udaypartap Singh

**Roll no.: 2610997576**

Portfolio based on the supplied lab plan. Replace any remaining course/date placeholders as your instructor requires. Use your own screenshots and observations; the sample data is fictional.

## What is included
- Labs 1–2: CLI practice with PowerShell and Bash commands, plus a record sheet.
- Lab 3: safe system/network commands and a record sheet. Add only your own results; redact private network details before publishing.
- Lab 4: formatted Writer-compatible document `lab04-writer/Digital-Literacy.docx`.
- Lab 5: mail-merge template and personalized example letters, plus invitee CSV.
- Labs 6–8: Calc-compatible workbook with marksheet, attendance, salary, and inventory tabs; sample CSV datasets are also included.
- Labs 9–10: editable Impress-compatible presentation `lab09-10-impress/Digital-Literacy-Presentation.pptx`.

## Lab 1–2: CLI file management
Windows PowerShell:
```powershell
New-Item -ItemType Directory -Path BCPS-Lab-Work\Lab01\notes -Force
Set-Location BCPS-Lab-Work\Lab01\notes
Set-Content readme.txt 'My first CLI practical.'
Get-Content readme.txt
Get-ChildItem -Force
Copy-Item readme.txt readme-copy.txt
Rename-Item readme-copy.txt summary.txt
New-Item -ItemType Directory ..\backup -Force
Move-Item summary.txt ..\backup\summary.txt
Remove-Item ..\backup\summary.txt
```
Linux/macOS equivalent: `mkdir -p BCPS-Lab-Work/Lab01/notes`, `cd` into it, `printf 'My first CLI practical.\n' > readme.txt`, `cat readme.txt`, `ls -la`, `cp readme.txt readme-copy.txt`, `mv readme-copy.txt summary.txt`, then remove only the temporary file you created. Capture your own terminal evidence and complete `lab01-02-cli/record.md`.

## Lab 3: system configuration and networking
PowerShell: `Get-ComputerInfo`, `Get-Date`, `Get-NetIPConfiguration`, `ipconfig /all`, `ping -n 4 127.0.0.1`, `nslookup example.com`, `tracert -h 8 example.com`.
Linux/macOS alternatives: `uname -a`, `date`, `ip address` (Linux) or `ifconfig` (macOS), `ip route` or `netstat -rn`, `ping -c 4 127.0.0.1`, `nslookup example.com`, `traceroute -m 8 example.com`. Record actual results in `lab03-system-network/record.md`; DNS/traceroute may be blocked on some networks. Do not publish MAC/public IP or other private network details.

## Lab 4: Writer document
Open `Digital-Literacy.docx` in LibreOffice Writer. It has title, headings, body text, a table, header/footer, and your name/roll number. Review it, save a native ODT copy if required, then export PDF.

## Lab 5: mail merge
Open `Invitation-Mail-Merge-Template.docx` in Writer and connect `datasets/invitees.csv` through Tools → Mail Merge Wizard. Preview recipients, finish to a new document, and save. `Merged-Invitation-Letters.docx` contains example personalized letters based on the fictional CSV. Do not send these invitations.

## Lab 6: marksheet
In the workbook's Marksheet tab, subject marks are B:F; formulas are Total `=SUM(B2:F2)`, Average `=AVERAGE(B2:F2)`, Result `=IF(MIN(B2:F2)>=40,"Pass","Needs Improvement")`. Copy down. Summary values: highest total 455, lowest total 283. Format averages to 2 decimals.

## Lab 7: attendance
Attendance tab uses P for present, A for absent. Formulas: present days `=COUNTIF(B2:F2,"P")`, working days `=COUNTA(B$1:F$1)`, attendance percent `=G2/H2*100`, status `=IF(I2>=75,"Eligible","Below 75%")`. Copy down and format percentage.

## Lab 8: salary and inventory
Salary tab assumes allowance = 10% of basic pay and deduction = 5%; gross = basic + allowance; net = gross − deduction. This is a classroom example, not actual payroll policy. Inventory tab calculates stock value = quantity × unit price and flags reorder when quantity is at/below reorder level.

## Labs 9–10: Impress presentation
Open the included 8-slide deck in LibreOffice Impress. Add a theme, relevant image/icon with attribution, restrained transitions, and simple animations as required by your instructor. Check slideshow, save an ODP copy, and export PDF.

## Upload to GitHub
Extract this ZIP. On GitHub create a new repository, then either upload these files using **Add file → Upload files**, or use Git in this folder:
```bash
git init
git add .
git commit -m "Add BCPS computer practicals 1-10"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```
Do not upload private screenshots/network details or credentials. Only include evidence you produced yourself.
