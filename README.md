# SimuXL

**Monte Carlo simulation inside desktop Excel, for engineers and cost/schedule risk analysts who need an auditable probabilistic tool.**

SimuXL is an Excel add-in (`.xll`). You define uncertain inputs with ordinary worksheet functions - `=SimuXL_Triangular(2,4,9)`, `=SimuXL_YesNo(0.4)` and six more - point it at the cells you care about, and run. Every run is reproducible under a seed you choose, and every number it reports can be traced back to the sample that produced it.

**Download the latest release below** (under *Releases*, on the right). This repository holds the releases, the user guide and the licence text only; the source is not published.

## Install

1. Find out whether your Excel is 32-bit or 64-bit: in Excel, **File ▸ Account ▸ About Excel**; the first line ends *32-bit* or *64-bit*. Most current installations are 64-bit.
2. From the latest release, download **`SimuXL64.xll`** (64-bit Excel) or **`SimuXL32.xll`** (32-bit Excel), and beside it **`SimuXL-Publisher.cer`** and **`SimuXL-Trust.bat`**. Save all three in a folder where they can stay, for example a `SimuXL` folder under your Documents.
3. Both add-in files are digitally signed by **Michael Ray Smith**, the licensor named in `License.txt`, with SimuXL's own certificate rather than one bought from a certificate authority - so your machine does not trust the signature until you tell it to. **Double-click `SimuXL-Trust.bat` once.** It adds `SimuXL-Publisher.cer` to your own Trusted Root Certification Authorities and Trusted Publishers stores - no administrator is needed, nothing else on the machine changes, and every SimuXL file signed with that certificate is trusted from then on, including a copy Windows marked as downloaded from the internet. Windows asks once whether to install a certificate claiming to represent Michael Ray Smith; answer **Yes**. The window then reads the signature on each SimuXL file beside it and prints **Valid** for each - that is the pass. If Excel still refuses to load the add-in afterwards, right-click the downloaded `.xll` ▸ **Properties** ▸ tick **Unblock** ▸ **OK**, and tell us (see *Support*): that is a machine whose policy blocks add-ins for a reason other than the signature.
4. In Excel: **File ▸ Options ▸ Add-ins**. At the bottom, next to *Manage*, choose **Excel Add-ins** and press **Go…**, then **Browse…**, pick the `.xll` you saved, and press **OK**. Make sure **SimuXL** is ticked in the list, then **OK**.
5. A **SimuXL** tab appears on the ribbon. **Help ▸ User Guide** opens the guide; it is also here as `user-guide.html`. **Help ▸ About** prints a *Signature* line reading `signed by Michael Ray Smith, trusted on this machine.` once step 3 has been run.

If every SimuXL formula shows `#NAME?`, the add-in is not loaded - repeat step 4. The guide's *When something looks wrong* section covers the rest.

## Licensing

SimuXL runs as a **30-day trial** on each machine with nothing to enter. After that, running a simulation needs a licence key issued for that machine: press **Help ▸ License**, copy the machine id it shows, and send it with your order. The key you receive is pasted into the same dialog. A key is verified on your machine and never leaves it. The terms are in `License.txt`.

## Updates

**Help ▸ Check for Updates** reads one small signed file from this repository's latest release and tells you whether a newer release exists and whether your licence covers it. SimuXL also makes the same check on its own once a week, about thirty seconds after Excel starts, showing nothing; the result is on the *Updates* line of **Help ▸ About**, and unticking **Check for updates once a week when Excel starts** under **Preferences ▸ Simulation** turns the weekly check off. Either way it sends SimuXL's version number and nothing else - no machine id, no licensee, no workbook name - and it downloads nothing. To update, download the new `.xll` from the release page and load it in place of the old one (step 4 above, after closing Excel); the trust step is not repeated, because every release is signed with the same certificate.

## Support

Email **michael.smith935@gmail.com**. When reporting a problem, include the line **Help ▸ About** prints under *Build* and, if a run is involved, the seed and the trial count.
