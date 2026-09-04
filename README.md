# SimuXL

**Monte Carlo simulation inside desktop Excel, for engineers and cost/schedule risk analysts who need an auditable probabilistic tool.**

SimuXL is an Excel add-in (`.xll`). You define uncertain inputs with ordinary worksheet functions - `=SimuXL_Triangular(2,4,9)`, `=SimuXL_YesNo(0.4)` and six more - point it at the cells you care about, and run. Every run is reproducible under a seed you choose, and every number it reports can be traced back to the sample that produced it.

**Download the latest release below** (under *Releases*, on the right). This repository holds the releases, the user guide and the licence text only; the source is not published.

## Install

1. Find out whether your Excel is 32-bit or 64-bit: in Excel, **File ▸ Account ▸ About Excel**; the first line ends *32-bit* or *64-bit*. Most current installations are 64-bit.
2. From the latest release, download **`SimuXL64.xll`** (64-bit Excel) or **`SimuXL32.xll`** (32-bit Excel). Save it somewhere it can stay, for example a `SimuXL` folder under your Documents.
3. Windows marks a downloaded file as coming from the internet and Excel will not load it while that mark is there. Right-click the downloaded `.xll` ▸ **Properties** ▸ tick **Unblock** at the bottom of the General tab ▸ **OK**. This is a one-time step for each downloaded file.
4. In Excel: **File ▸ Options ▸ Add-ins**. At the bottom, next to *Manage*, choose **Excel Add-ins** and press **Go…**, then **Browse…**, pick the `.xll` you saved, and press **OK**. Make sure **SimuXL** is ticked in the list, then **OK**.
5. A **SimuXL** tab appears on the ribbon. **Help ▸ User Guide** opens the guide; it is also here as `user-guide.html`.

If every SimuXL formula shows `#NAME?`, the add-in is not loaded - repeat step 4. The guide's *When something looks wrong* section covers the rest.

## Licensing

SimuXL runs as a **30-day trial** on each machine with nothing to enter. After that, running a simulation needs a licence key issued for that machine: press **Help ▸ License**, copy the machine id it shows, and send it with your order. The key you receive is pasted into the same dialog. A key is verified on your machine and never leaves it. The terms are in `License.txt`.

## Updates

**Help ▸ Check for Updates** reads one small signed file from this repository's latest release and tells you whether a newer release exists and whether your licence covers it. It sends SimuXL's version number and nothing else - no machine id, no licensee, no workbook name - and it downloads nothing. To update, download the new `.xll` from the release page and load it in place of the old one (step 4 above, after closing Excel).

## Support

Email **michael.smith935@gmail.com**. When reporting a problem, include the line **Help ▸ About** prints under *Build* and, if a run is involved, the seed and the trial count.
