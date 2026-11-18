# Data

## Sources and access terms

- Structured data: Wharton Research Data Services (WRDS), a subscription service. The study used CRSP
  (market data), Compustat (financial ratios and ratings), and Mergent FISD and TRACE (bond data). Access
  needs a WRDS subscription. The data are proprietary, so they are not in this repository.
- Text data: earnings call transcripts from Seeking Alpha (<https://seekingalpha.com>), collected by web
  scraping. The repository and the paper do not state access terms for these texts, and they are not in
  this repository.
- Synthetic sample: `Artificial_Data.xlsx`, made by the authors. The paper describes it as a sample "synthetically altered by large language models (Gemini)". No separate licence is stated for it.

`Data Source & Collection.md` describes each source and how the data were collected.

## Files in this folder

| File | Content |
|---|---|
| `Artificial_Data.xlsx` | Synthetic sample, 100 rows and 154 columns: `RATING_TYPE` (S&P, Moody's or Fitch), `Rating` (letter grade), 151 numerical features, and `string_values` (a short text). |
| `Data characteristics and features.xlsx` | One row per variable (154 rows): its source, name and description. |
| `Data Source & Collection.md` | Data sources and collection method. |

## Where the code expects the data

Each notebook in `code/` reads one file with `pd.read_csv("data.csv")`, a path relative to the notebook's
working directory. Jupyter starts the kernel in the notebook's folder, so by default the file goes to
`code/data.csv`. Do not commit it to this repository.

The notebooks use these columns of `data.csv`:

- `RATING`: an integer rating code. The notebooks merge codes 1 to 5, 10 to 12, 13 to 15 and 16 to 22
  into one class each, then number the classes from 0.
- `RATING_TYPE` and `pastrating`: covariates, one-hot encoded in `code/Group1.ipynb` and
  `code/Group2.ipynb`.
- `cleantext`: the transcript text that the tokenizers use. The notebooks also clean a `text` column.
- Numerical features selected by position, as commented in the notebooks: `iloc[:, 4:101]` market data,
  `iloc[:, 102:110]` bond data and `iloc[:, 111:157]` financial ratios. `code/Group1.ipynb` and
  `code/Group2.ipynb` drop a `dater` column from these.

`Artificial_Data.xlsx` has a different layout: it has `Rating` (letter grades) instead of `RATING`, and it
has no `pastrating`, `cleantext`, `text` or `dater` column. The repository has no script that converts it
to `data.csv`.

## Data Access and Reproducibility

Due to the proprietary nature of the data sources from Wharton Research Data Services (WRDS), direct access to the raw datasets used in our study is restricted. We acknowledge the importance of transparency and reproducibility in research, and as such, have taken several steps to enable others to validate and build upon our work:

### Documentation

- **Comprehensive Data Documentation:** We have prepared a detailed document that provides an exhaustive description of each data source utilized in our study. This document includes:
  - **Data Source and Collection:** Detailed profiles of each dataset, including the types of data contained, the data provider, and the data structure.  Also it outlines how data was collected, processed, and analyzed, ensuring that researchers can understand and replicate our methodology.
  - **Dataset Features and Characteristics:** Detailed explanations of the features and characteristics of each dataset, including any preprocessing or transformations applied.

This documentation is designed to provide researchers with sufficient information to understand the context and constraints of our data without accessing the actual datasets.

### Synthetic Dataset

- **Synthetic Data Generation:** To further support the reproducibility of our analyses, we have created a synthetic dataset. This synthetic dataset is constructed to:
  - **Reflect the Original Data's Structure:** Ensuring that the synthetic data maintains the same format and type distributions as the original data.

- **Purpose and Usage:** The synthetic dataset is provided to enable external parties to run and validate our analytical code. This dataset allows users to:
  - **Test and Execute Analytical Code:** Users can run our provided code against the synthetic dataset to observe how it performs and to modify or extend the analysis. The notebooks do not read `Artificial_Data.xlsx` as it is; see "Where the code expects the data" above.
  - **Validate Methodologies:** By providing a dataset with known properties and outcomes, researchers can validate the efficacy and accuracy of our methods.

