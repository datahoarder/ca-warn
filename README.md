# California WARN data

(Collected on May 12, 2016)

Related story: [Tech layoffs more than double in Bay Area](http://www.mercurynews.com/business/ci_29880696/tech-layoffs-more-than-double-bay-area)

California's Employment Development Department posts WARN notices online at:

[http://www.edd.ca.gov/jobs_and_training/Layoff_Services_WARN.htm](http://www.edd.ca.gov/jobs_and_training/Layoff_Services_WARN.htm)

The files are published as PDFs. This is the shell command to collect them all:


~~~sh
$ wget -r --level 1 --accept pdf --no-directories \
       http://www.edd.ca.gov/jobs_and_training/Layoff_Services_WARN.htm
~~~



## Manifest 

This repo contains:



- [pdfs/](pdfs/) - a mirror of those PDFs (from 2012 May 10, 2016) 
- [pdftotext-layout/](pdftotext-layout/) - the result of running those PDFs through [poppler's](https://poppler.freedesktop.org/) `pdftotext -layout`
- __abbyy/__
  + [all-text-xlsx](abbyy/all-text-xlsx/) - ABBYY FineReader's PDF-to-Excel conversion, including content in- and outside-of what it detects as tables.
  + [just-tables-xlsx](abbyy/just-tables-xlsx) - FineReader's PDF-to-Excel conversion, but only tabular content
  + [just-tables-csv](abbyy/just-tables-csv) - Same as above, just converted to CSV. Probably the most convenient.

The table format changes over the years so there's an output file for each original PDF.






## Table format


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



And here's what [pdfs/WARN-Report-for-7-1-2015-to-05-10-2016.pdf](pdfs/WARN-Report-for-7-1-2015-to-05-10-2016.pdf) looks like as a [CSV](abbyy/just-tables-csv/WARN-Report-for-7-1-2015-to-05-10-2016.csv):


| ﻿Notice Date | Effective Date | Received Date |                 Company                  |      City     | No. Of Employees |        Layoff/Closure       |
|--------------|----------------|---------------|------------------------------------------|---------------|------------------|-----------------------------|
| 06/22/2015   | 03/25/2016     | 07/01/2015    | Maxim Integrated Product                 | San Jose      |              150 | Closure Permanent           |
| 06/30/2015   | 08/29/2015     | 07/01/2015    | McGraw-Hill Education                    | Monterey      |              137 | Layoff Unknown at this time |
| 06/30/2015   | 08/30/2015     | 07/01/2015    | Long Beach Memorial Medical Center       | Long Beach    |               90 | Layoff Permanent            |
| 07/01/2015   | 09/02/2015     | 07/01/2015    | Leidos                                   | El Segundo    |               72 | Layoff Permanent            |
| 07/01/2015   | 09/30/2016     | 07/01/2015    | Bosch Healthcare Systems, Inc.           | Palo Alto     |               55 | Closure Permanent           |
| 06/29/2015   | 09/01/2015     | 07/02/2015    | Encompass Digital Media, Inc.            | Los Angeles   |               41 | Closure Permanent           |
| 07/02/2015   | 07/06/2015     | 07/02/2015    | Alphatec Spine                           | Carlsbad      |               99 | Layoff Permanent            |
| 06/30/2015   | 08/07/2015     | 07/06/2015    | Symantec Corporation                     | Mountain View |               60 | Layoff Permanent            |
| 06/30/2015   | 08/31/2015     | 07/06/2015    | Fusion Contacts Centers, LLC             | Santa Maria   |               50 | Closure Permanent           |
| 06/30/2015   | 09/15/2015     | 07/06/2015    | KLA-T encor Corporation                  | Milpitas      |              213 | Layoff Permanent            |
| 07/01/2015   | 09/04/2015     | 07/06/2015    | Southern California Edison Company       | San Clemente  |              100 | Closure Permanent           |
| 05/06/2016   | 07/08/2016     | 05/06/2016    | Pactiv LLC                               | Vernon        |              108 | Closure Permanent           |
| 04/29/2016   | 06/10/2016     | 05/09/2016    | Symantec Corporation                     | Mountain View |               15 | Layoff Permanent            |
| 04/29/2016   | 06/30/2016     | 05/09/2016    | First Student                            | Yucca Valley  |                5 | Closure Permanent           |
| 04/29/2016   | 06/30/2016     | 05/09/2016    | The Declan Suites San Diego              | San Diego     |               65 | Layoff Permanent            |
| 05/05/2016   | 05/02/2016     | 05/09/2016    | Homemade Real Foods                      | Vernon        |              316 | Layoff Permanent            |
| 05/05/2016   | 07/07/2016     | 05/09/2016    | Roof Diagnostics Solar and Electric, LLC | San Francisco |               48 | Layoff Permanent            |
| 05/06/2016   | 07/06/2016     | 05/09/2016    | Brake Parts Inc.                         | Chowchilla    |                1 | Layoff Permanent            |
| 05/09/2016   | 07/10/2016     | 05/09/2016    | Los Angeles Guild LLC                    | Hawthorne     |               57 | Layoff Permanent            |


## Caveats

There's obvious inconsistencies and errors in the data. The newer formats have a summary table at the end, [which needs to be manually removed](https://github.com/datahoarder/ca-warn/blob/master/abbyy/just-tables-csv/WARN-Report-for-7-1-2015-to-05-10-2016.csv#L631-L650).

Then there are errors of spelling, such as ["Microsift"](https://github.com/datahoarder/ca-warn/search?utf8=%E2%9C%93&q=Microsift)

In the [first 2014 file, a Zynga layoff of 194 jobs each shows up twice](https://github.com/datahoarder/ca-warn/blob/baacea5c6d0edc86bd4b2d72e3184761326f24fa/abbyy/just-tables-csv/eddwarncn14.csv#L413-L414).

I'm don't think [pdfs/eddwarncn14.pdf](pdfs/eddwarncn14.pdf) actually contains all of 2014, i.e. what's included in the [two interim files that overlap with 2015](/pdfs).
