# MA Trial Court Charges Scrapper

Ruby script to iterate over the data in the MA Trial Court Charges Tableau
dashboard.

The script is a work-in-progress.  Currently it:

* Loads the dashboard
* Selects the target year to scrape
* Iterates through the first page of the charges list and creates a PDF file

To be done:
* Scrolling through the charges list to download county-level information for
  each charge.

Challenges:
* Tableau renders all table data in a `<canvas>` element. This means traditional
  scraping isn't possible.  To interact with the page, clicking at exact
  coordinates of data in the `<canvas>` is required.

## Setup

Setup the `.env` file

```shell
$ cp .env.example .env
```

Set `DASHBOARD_URL` to the `src` attribute of the iframe.

## Running

```shell
$ ./bin/scrape
```
