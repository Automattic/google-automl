# Google AutoML investigation

Notes, scripts and codes related to Google's AutoML

https://cloud.google.com/automl/

### Training data

Google accepts training data in `.tsv` and `.tmx` formats. `.tmx` is better at
handling the tabs and newlines in some of our strings, but is less convenient
to work with, so we've got some tools to manipulate it:

- `apply-blacklist-to-tsv`: Remove entries and trim leading/trailing whitespace `./apply-blacklist-to-tsv ./blacklist.txt data/fr.tmx > data/fr-clean.tmx`
