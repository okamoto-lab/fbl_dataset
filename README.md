# Function-based Label Dataset for Complementary Recommendation

This repository provides the FBL2023.tsv and FBL2024.tsv datasets along with their specification documents. The datasets are formatted as TSV files using UTF-8 encoding with tab-delimited values.

## File Format

- **File Format:** TSV
- **Encoding:** UTF-8
- **Delimiter:** Tab (`\t`)

## Column Structure

Each file includes the following columns:

| Column Name        | Data Type | Description                   |
| ------------------ | --------- | ----------------------------- |
| `ITEM_URL_1`       | URL       | URL for Item 1                |
| `ITEM_NAME_1`      | String    | Name of Item 1                |
| `ITEM_URL_2`       | URL       | URL for Item 2                |
| `ITEM_NAME_2`      | String    | Name of Item 2                |
| `ANNOTATOR1_ID`    | Integer   | Identifier for Annotator 1    |
| `ANNOTATOR1_LABEL` | Integer   | Label assigned by Annotator 1 |
| `ANNOTATOR2_ID`    | Integer   | Identifier for Annotator 2    |
| `ANNOTATOR2_LABEL` | Integer   | Label assigned by Annotator 2 |
| `ANNOTATOR3_ID`    | Integer   | Identifier for Annotator 3    |
| `ANNOTATOR3_LABEL` | Integer   | Label assigned by Annotator 3 |

## Label Definitions

### FBL2023

| Mapping Number | Label |
| :--------------: | ----- |
| 1  | Items 1 and 2 have the same function and usage. |
| 2  | Item 1 can be replenished with item 2. |
| 3  | Item 2 can be replenished with item 1. |
| 4  | Item 1 and 2 must be combined to be usable. |
| 5  | When combined with item 2, item 1 becomes more useful. |
| 6  | When combined with item 1, item 2 becomes more useful. |
| 7  | Combining 1 and 2 makes them more useful. |
| 8  | Items 1 and 2 have no relationship. |
| 9  | Items 1 and 2 seem to have a relationship, but it is difficult to verbalize. |

*Note: Any response that does not match one of the specified labels will be treated as a missing value.*


### FBL2024

| Mapping Number  | Label |
| :-------------: | ----- |
| 1 | Substitute relationship  |
| 2 | Complementary relationship |
| 3 | Other relationship         |

## Reference Papers

For further details and the underlying methodology, please refer to the following paper:

- **Reference Paper 1:**
  - *Title:* [Is It Really Complementary? Revisiting Behavior-based Labels for Complementary Recommendation](https://doi.org/10.1145/3640457.3691705)
  - *Authors:* Kai Sugahara, Chihiro Yamasaki, Kazushi Okamoto
  - *Conference:* Proceedings of the 18th ACM Conference on Recommender Systems (RecSys2024), pp.1091-1095, 2024.10

## Acknowledgements

We would like to thank all contributors and annotators who participated in creating this dataset. Special thanks are also extended to our collaborative research partner, [**ASKUL Corporation**](https://www.askul.co.jp/corp/english/), for their invaluable support and cooperation.

## Update History

- **2025-04-01**: Initial version created
