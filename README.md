# Fake News Ad Trackers Analysis — before Nov. 2016 vs. March 2017

This repository contains data, analytic code, and findings based on a collaboration between BuzzFeed News and [Liliana Bounegru](https://github.com/lilianabounegru), an author of the forthcoming [A Field Guide to Fake News](http://fakenews.publicdatalab.org/).

The findings support portions of the BuzzFeed News article, "[Fake News, Real Ads](https://www.buzzfeed.com/craigsilverman/fake-news-real-ads)," published April 4, 2017. Please read that article, which contains important context and details, before proceeding.

## Data

This repository contains the following five CSV files:

- [`data/observed-trackers.csv`](data/observed-trackers.csv): The data BuzzFeed News received from the researchers behind A Field Guide to Fake News, slightly restructured.

- [`output/tracker-matrix.csv`](output/tracker-matrix.csv): For each website-and-tracker combination, whether the website had that tracker (a) before Nov. 2016, and/or (b) in March 2017. (Includes only "comparable" sites. See below for details.)

- [`output/tracker-counts.csv`](output/tracker-counts.csv): Using the data in `output/tracker-matrix.csv`, counts the number of comparable sites containing each tracker during the two timeframes, and the net change.

- [`output/tracker-statuses.csv`](output/tracker-statuses.csv): Using the data in `output/tracker-matrix.csv`, classifies each website-and-tracker combination into one of four categories: kept, removed, added or never had the tracker.

- [`output/tracker-statuses-pivot.csv`](output/tracker-statuses-pivot.csv): Using the data in `output/tracker-statuses.csv`, counts the number of sites that kept, removed, added, or never had each tracker.

### A note on "comparable" sites

To make the two time frames — before Nov. 2016 and in March 2017 — comparable, we removed two types of sites:

- Sites with no observed trackers in the "before" period

- Sites that had disappeared by the "after" period

After doing so, we were left with 51 websites.

## Code

The Python code that processes the data can be [found here](notebooks/analysis.ipynb).

## Feedback / Questions?

Contact Jeremy Singer-Vine at jeremy.singer-vine@buzzfeed.com.

Looking for more from BuzzFeed News? [Click here for a list of our open-sourced projects, data, and code](https://github.com/BuzzFeedNews/everything).
