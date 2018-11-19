# OONI Translations

This repository contains all the translations for OONI software.

You are expected to have installed the [transifex
CLI](https://docs.transifex.com/client/installing-the-client) (please don't run
`pip` or `easy_install` as root to install it!)

You should also have setup transifex with you credentials via a
`~/.transifexrc` file (see: [client-configuration
docs](https://docs.transifex.com/client/client-configuration#~/-transifexrc)).

## Updating translations

This is the process by which you pull the latest translations and generate the
OS specific localization strings.

Usually you will run this as part of the app workflow, but you can also do it
in here via:

```
./update-translations.sh
```

## Uploading new strings

Strings are generated from a csv master file. To upload new strings you should
copy the strings csv file to `probe-mobile/en/strings.csv` and then run:

```
./sync-csv-source.sh
```

This will generate `probe-mobile/en/strings.json` and push it to transifex for
you.
