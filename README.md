# Positive Case Tracker for the Castro Valley Unified School Disctrict

School's starting, and our district has a [Positive Case Dashboard](https://www.cv.k12.ca.us/apps/pages/index.jsp?uREC_ID=1728675&type=d&pREC_ID=2165165) that reports confirmed COVID-19 cases within students and staff present at schools. This repository attempts to use the [Git scraping technique](https://simonwillison.net/2020/Oct/9/git-scraping/) to track case numbers over time.

Raw HTML dumps from the embedded Google Spreadsheet are in the `data/html/` folder, and parsed CSV versions (using [pandas](https://pandas.pydata.org/)) are available in `data/csv/`. The most recent CSV can be found in `data/daily.csv` for git diffing.

This GitHub Action runs every 4 hours from 5:06 AM PDT (4 AM PST) to 9:06 PM PDT (8 PM PST) Mon-Fri. I'm not sure how often the data updates, but the numbers changed while I was working on it, so I assume they will update throughout the day.

School started on August 10th, but the first entry was from Aug. 15 (with data last updated from Aug. 11), so basically right from the beginning. It appears that I missed some updates on the day of Aug. 16 (as I was working on this), but we should have data from then on.
