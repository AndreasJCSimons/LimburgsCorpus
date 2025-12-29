
# Limburgish Dialect Corpus

This repository contains a corpus of Limburgish text and audio under "corpus".  The metadata can be found under "files.json". This corpus was collected through fieldwork and crowdsourcing contributions from various authors across Limburg. For more information: https://www.limburgscorpus.com.

## About the Corpus

This corpus represents a diverse collection of written and spoken materials in various Limburgish dialects, including literary works, educational materials, postcards, poetry, and other genres. The materials span multiple decades and represent different communities within the Limburg region of the Netherlands and Belgium. This corpus was explicitly collected through informed consent and is fully GDPR-compliant.

## License Information

### Creative Commons Licenses

All files in this corpus are shared under Creative Commons licenses, which allow for sharing and reuse under specific conditions. The metadata file "files.json" specifies the license under "license" and who requires attribution under "attribution_name". Attribution to the author is mandatory under Creative Commons licenses (except CC0). The corpus uses three different licenses:

#### CC BY-NC 4.0 (Attribution-NonCommercial 4.0 International)

 https://creativecommons.org/licenses/by-nc/4.0/

#### CC BY 4.0 (Attribution 4.0 International)

 https://creativecommons.org/licenses/by/4.0/

#### CC0 (Public Domain Dedication)

https://creativecommons.org/publicdomain/zero/1.0/

## Metadata Structure

The corpus metadata is stored in JSON format (`files.json`), with each entry containing various fields. The metadata is a mix of Dutch, English, and Limburgish, and normalization may be required for analysis. Placename normalization is explicitly required for geographical data.

### Important Notes on Data Handling

- **Missing data**: If data is missing, the key is absent from the JSON object (not present as null or empty string)
- **Mandatory fields**: Only `file_name` is 100% mandatory across all entries
- **Language mixing**: Metadata uses Dutch, English, and Limburgish; normalization is required for analysis
- **Placename normalization**: Geographic locations require normalization for consistency


### Metadata Schema

#### File Metadata

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| `name` | string | Filename | `"1.txt"` |
| `path` | string | Relative file path | `"corpus\\1.txt"` |
| `size` | integer | File size in bytes | `202` |
| `modified` | string | Last modification timestamp (ISO 8601) | `"2025-12-29T17:50:19"` |

#### Content Description

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| `title` | string | Title of the work | `"Vallekebergs leesplenkske"` |
| `description` | string | Brief description of content | `"2025, postkaarten, Fieldwork..."` |
| `genre` | string | Type/genre of content | `"postkaarten"`, `"poëzie"`, `"artikel"` |
| `year_of_publication` | int/string | Year published (int, or string if estimated) | `2025`, `"ca. 1995"` |
| `file_extra_information` | string | Additional contextual information | `"Fieldwork met LTL..."` |

#### Linguistic Information

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| `dialect` | string | Specific dialect/location (requires normalization) | `"Schimmert"`, `"Weert, Nederland"` |
| `specific_spelling` | string | Spelling system used |  `"Veldekespelling"`, `"Specifieke dialect- of woordenboekspelling"`, `"Eigen spelling van auteur"`, `"Andere"` |

#### Author Information

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| `author_year_of_birth` | int/string | Birth year (int, or string if estimated) | `1969`, `"voor 1955"` |
| `author_outside_community` | string | Whether author lived outside dialect community or dialect changed | `"Nee"`, `"Ja"` |
| `author_changes_description` | string | Description of dialect changes if applicable | `"Moved to Amsterdam for 10 years..."` |
| `author_dialect_community` | string/list | Who author speaks/spoke dialect with | `"Grandparents, Parents, Siblings, Their children, Friends, At work, On the street"` |

#### Rights and Licensing

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| `license` | string | License type | `"CC BY-NC 4.0"`, `"CC BY 4.0"`, `"CC0 (publiek domein)"`|
| `attribution_name` | string | Name to use for attribution | `"Andreas Simons"` |


## Data Structure

The corpus metadata is structured as a JSON array, where each object represents a single file with its associated metadata. This structure allows for easy parsing, filtering, and analysis of the corpus contents.


## Acknowledgments

This corpus was made possible through the generous contributions of numerous authors, associations, and the fieldwork conducted with dialect communities throughout Limburg. Special thanks to all contributors who have shared their work under Creative Commons licenses. For more information see: https://www.limburgscorpus.com/dank.html


## Citation

 Simons, A. & Cornips, L. (2025). *The Limburgish Corpus: database of Limburgish dialects*. Available online at https://www.limburgscorpus.com/corpus.html.

_Last updated: December 29, 2025_
