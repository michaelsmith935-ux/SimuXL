# SimuXL

**Monte Carlo simulation inside desktop Excel, for engineers and cost/schedule risk analysts who need an auditable probabilistic tool.**

SimuXL is an Excel add-in (`.xll`). You define uncertain inputs with ordinary worksheet functions - `=SimuXL_Triangular(2,4,9)`, `=SimuXL_YesNo(0.4)` and six more - point it at the cells you care about, and run. Every run is reproducible under a seed you choose, and every number it reports can be traced back to the sample that produced it.

**Download the latest release below** (under *Releases*, on the right). This repository holds the releases, the user guide and the licence text only; the source is not published.

## Install

From the latest release, download **`SimuXL-Setup-1.9.3.exe`**, close Excel, and run it. That is the only file you need.

The installer reads whether your Excel is 64-bit or 32-bit (and shows you the answer, which you can change), installs the matching add-in into your own Programs folder with no administrator, registers it with Excel so there is no Browse step, adds that one folder to Excel's Trusted Locations so Excel loads the add-in even if your Trust Center blocks add-in files, and - ticked by default - runs a one-time trust step. Windows asks once whether to install a certificate claiming to represent **Michael Ray Smith**; answer **Yes**.

Then start Excel: a **SimuXL** tab appears on the ribbon, and **Help ▸ About** prints a *Signature* line reading `signed by Michael Ray Smith, trusted on this machine.`

Windows SmartScreen may say it *protected your PC* from an app it does not recognise - it judges a file by how many machines have already run it, not by its certificate. Press **More info**, read the publisher's name (**Michael Ray Smith**) and press **Run anyway**.

**To check the download before running it**, compare its SHA-256 against the line below. In PowerShell:

```
Get-FileHash "$HOME\Downloads\SimuXL-Setup-1.9.3.exe" -Algorithm SHA256
```

```
69903bdb1541befa4e285cb3c387a0cb2e368f74053a72cafa3627118bb80767
```

The other file on this page, `simuxl-latest.txt`, is **not a download**. It is the small signed file **Help ▸ Check for Updates** reads to tell you whether a newer release exists; it has to sit here under that exact name.

If every SimuXL formula shows `#NAME?`, the add-in is not loaded - run the installer again. The guide's *When something looks wrong* section covers the rest, and **Help ▸ User Guide** opens it.

## Uninstall

Close Excel first, then remove **SimuXL** from Windows' **Installed apps**. If Excel still has the add-in open - even with no window on screen - Uninstall says so and changes nothing, so nothing is half-removed; close Excel (or end `EXCEL.EXE` in Task Manager) and run it again.

**Uninstall removes SimuXL completely.** It removes the files it installed, the one trusted location it added, and **every** SimuXL add-in entry in Excel - not only its own - so Excel is left with no SimuXL at all. If any of those entries points at a SimuXL `.xll` elsewhere on your computer - a copy registered by hand, or an older version - Uninstall lists those files and asks whether to delete them too; answer **No** to keep the files, and the entries are removed either way. Nothing that is not a SimuXL `.xll` named by one of those entries is ever touched.

**What Uninstall never removes:** your settings, your licence file, your evaluation record, your log and the trusted certificate. They stay where they are, so reinstalling later finds your licence still in place.

## Licensing

SimuXL runs as a **30-day trial** on each machine with nothing to enter. After that, running a simulation needs a licence key issued for that machine: press **Help ▸ License**, copy the machine id it shows, and send it with your order. The key you receive is pasted into the same dialog. A key is verified on your machine and never leaves it. The terms are in `License.txt`.

## Updates

**Help ▸ Check for Updates** reads one small signed file from this repository's latest release and tells you whether a newer release exists and whether your licence covers it. SimuXL also makes the same check on its own once a week, about thirty seconds after Excel starts, showing nothing; the result is on the *Updates* line of **Help ▸ About**, and unticking **Check for updates once a week when Excel starts** under **Preferences ▸ Simulation** turns the weekly check off. Either way it sends SimuXL's version number and nothing else - no machine id, no licensee, no workbook name - and it downloads nothing.

To update, close Excel and run the new release's installer; it installs over the old one, and the trust step is not repeated, because every release is signed with the same certificate.

## Support

Email **michael.smith935@gmail.com**. When reporting a problem, include the line **Help ▸ About** prints under *Build* and, if a run is involved, the seed and the trial count.
