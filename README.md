# California WARN data

(Collected on May 12, 2016)

Related story: [Tech layoffs more than double in Bay Area](http://www.mercurynews.com/business/ci_29880696/tech-layoffs-more-than-double-bay-area

California's Employment Development Department posts WARN notices online at:

[http://www.edd.ca.gov/jobs_and_training/Layoff_Services_WARN.htm](http://www.edd.ca.gov/jobs_and_training/Layoff_Services_WARN.htm)

The files are published as PDFs; this repo contains:


- [pdfs/][pdfs/] - a mirror of those PDFs (from 2012 May 10, 2016) 
- [pdftotext-layout/](pdftotext-layout/) - the result of running those PDFs through [poppler's](https://poppler.freedesktop.org/) `pdftotext -layout`
- __abbyy/__
  + [all-text-xlsx](abbyy/all-text-xlsx/) - ABBYY FineReader's PDF-to-Excel conversion, including content in- and outside-of what it detects as tables.
  + [just-tables-xlsx](abbyy/just-tables-xlsx) - FineReader's PDF-to-Excel conversion, but only tabular content
  + [just-tables-csv](abbyy/just-tables-csv) - Same as above, just converted to CSV. Probably the most convenient.

The table format changes over the years so there's an output file for each original PDF.


Here's what [pdfs/eddwarncn12.pdf](pdfs/eddwarncn12.pdf) looks like as a [CSV](abbyy/just-tables-csv/eddwarncn12.csv):

|         Company Name        |     Location    | Employees Affected | Layoff Date |
|-----------------------------|-----------------|--------------------|-------------|
| AAR MOBILITY SYSTEMS        | MCCLELLAN AFB   |                 48 | 6/15/12     |
| ABBOTT VASCULAR             | MURRIETA        |                 45 | 1/25/12     |
| ABBOTT VASCULAR             | MURRIETA        |                 38 | 10/17/12    |
| ABBOTT VASCULAR             | TEMECULA        |                247 | 1/25/12     |
| ABBOTT VASCULAR             | TEMECULA        |                  7 | 1/25/12     |
| ABBOTT VASCULAR             | TEMECULA        |                139 | 10/17/12    |
| ABBOTT VASCULAR             | TEMECULA        |                 16 | 10/17/12    |
| ABEO MANAGEMENT CORPORATION | LOS ANGELES     |                 42 | 11/28/12    |
| ABERCROMBIE & FITCH         | ANAHEIM         |                 51 | 1/14/12     |
| ABERCROMBIE & FITCH         | CAPITOLA        |                 51 | 1/21/12     |
| ABERCROMBIE & FITCH         | RIVERSIDE       |                 64 | 1/14/12     |
| XEROX STATE HEALTHCARE, LLC | LOS ANGELES     |                 18 | 10/20/12    |
| XEROX STATE HEALTHCARE, LLC | SACRAMENTO      |                  4 | 10/20/12    |
| XEROX STATE HEALTHCARE, LLC | STOCKTON        |                 24 | 10/20/12    |
| XOMA (US) LLC               | BERKELEY        |                 78 | 3/6/12      |
| XPAL POWER INC.             | MODESTO         |                  6 | 1/3/12      |
| XYRATEX INTERNATIONAL, INC. | WEST SACRAMENTO |                 27 | 5/17/12     |
| XYRATEX INTERNATIONAL, INC. | WEST SACRAMENTO |                 78 | 11/29/12    |
| YAHOO! INC.                 | BURBANK         |                 65 | 6/8/12      |
| YAHOO! INC.                 | SAN DIEGO       |                 35 | 6/8/12      |
| YAHOO! INC.                 | SANTA CLARA     |                130 | 6/8/12      |
| YAHOO! INC.                 | SANTA MONICA    |                 70 | 6/8/12      |
| YAHOO! INC.                 | SUNNYVALE       |                720 | 6/8/12      |
| ZODIAC POOL SYSTEMS, INC.   | MOORPARK        |                125 | 3/30/12     |



And here's what [pdfs/WARN-Report-for-7-1-2015-to-05-10-2016.pdf](pdfs/WARN-Report-for-7-1-2015-to-05-10-2016.pdf) looks like as a [CSV](abbyy/WARN-Report-for-7-1-2015-to-05-10-2016.csv):


| ﻿Notice Date | Effective Date | Received Date |             Company              |      City     | No. Of Employees |        Layoff/Closure        |
|--------------|----------------|---------------|----------------------------------|---------------|------------------|-----------------------------|
| 06/30/2014   | 06/18/2014     | 07/01/2014    | Symantec Corporation             | Mountain View |               51 | Layoff Permanent            |
| 06/30/2014   | 09/12/2014     | 07/07/2014    | Post Foods, LLC                  | Modesto       |               52 | Closure Permanent           |
| 06/30/2014   | 09/26/2014     | 07/07/2014    | Post Foods, LLC                  | Modesto       |                6 | Closure Permanent           |
| 07/01/2014   | 09/15/2014     | 07/07/2014    | Crissair, Inc                    | Palmdale      |              170 | Closure Permanent           |
| 07/02/2014   | 10/01/2014     | 07/07/2014    | Brooks Automation Inc.           | Petaluma      |               89 | Closure Permanent           |
| 07/08/2014   | 09/07/2014     | 07/08/2014    | Bimbo Bakeries USA, Inc.         | Fresno        |               73 | Layoff Permanent            |
| 07/09/2014   | 09/07/2014     | 07/10/2014    | Buca Restaurants 2, Inc./Buca di | Irvine        |               87 | Closure Permanent           |
| 07/15/2014   | 09/15/2014     | 07/17/2014    | Xerox Business Services          | Bakersfield   |               38 | Layoff Permanent            |
| 07/17/2014   | 09/15/2014     | 07/17/2014    | Microsift and Nokia Inc          | San Diego     |              378 | Layoff Permanent            |
| 06/24/2015   | 08/19/2015     | 06/30/2015    | SureFire, LLC                    | Santa Ana     |                2 | Layoff Permanent            |
| 06/24/2015   | 08/19/2015     | 06/30/2015    | SureFire, LLC                    | Santa Ana     |               10 | Layoff Permanent            |
| 06/25/2015   | 08/24/2015     | 06/30/2015    | Intuit, Inc.                     | Menlo Park    |               27 | Layoff Permanent            |
| 06/25/2015   | 08/24/2015     | 06/30/2015    | Intuit, Inc.                     | Mountain View |               13 | Layoff Permanent            |
| 06/25/2015   | 08/24/2015     | 06/30/2015    | Intuit, Inc.                     | San Diego     |               11 | Layoff Permanent            |
| 06/25/2015   | 08/24/2015     | 06/30/2015    | Intuit, Inc.                     | San Francisco |               86 | Layoff Permanent            |
| 06/25/2015   | 08/24/2015     | 06/30/2015    | Intuit, Inc.                     | Santa Monica  |               49 | Closure Permanent           |
| 06/25/2015   | 08/24/2015     | 06/30/2015    | Intuit, Inc.                     | Venice        |               11 | Closure Permanent           |
| 06/29/2015   | 08/28/2015     | 06/30/2015    | Safeway, Inc.                    | Pleasanton    |               18 | Layoff Unknown at this time |
| 06/30/2015   | 07/22/2015     | 06/30/2015    | Medtronic Ablation Frontiers LLC | Carlsbad      |               50 | Closure Permanent           |
