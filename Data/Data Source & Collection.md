## Data Sources Overview

In our study, we utilized two main categories of data: structured and unstructured. Our structured data sources were primarily obtained from Wharton Research Data Services (WRDS), a highly regarded private, subscription-based data repository known for its extensive collection of financial, marketing, and economic information. More information about WRDS can be found at [WRDS](https://wrds-www.wharton.upenn.edu/).

### Structured Data Sources

We sourced data from the following databases within WRDS:

#### 1. CRSP (Center for Research in Security Prices)
- **Purpose:** Provides comprehensive security price, return, and volume data.
- **Markets Covered:** NYSE, AMEX, and NASDAQ.
- **Additional Data:** Stock indices, beta and cap-based portfolios, treasury bond rates, mutual funds, and real estate data.
- **Usage in Study:** Utilized for market data.

#### 2. Compustat
- **Purpose:** Offers detailed corporate financial ratios and ratings.
- **Coverage:** Data for U.S. and Canadian companies.
- **Data Range:** Over 300 annual and 100 quarterly financial data items.
- **Historical Data Availability:** Annual data back to 1950 and quarterly and monthly market data back to 1962.
- **Usage in Study:** Employed for financial ratio and rating data.

#### 3. Mergent and TRACE (Trade Reporting and Compliance Engine)
- **Purpose:** Provides in-depth information on bond transactions and performance.
- **Data Includes:** Corporate bonds, U.S. government agency bonds, and securitized products, detailed by types like asset-backed securities and mortgage-backed securities.
- **Usage in Study:** Utilized for bond data.

### Unstructured Data Sources

Our study also incorporated significant amounts of unstructured data, primarily sourced from the following platform:

#### 1. Seeking Alpha
- **Website:** [Seeking Alpha](https://seekingalpha.com)
- **Purpose:** Utilized for textual data extraction.
- **Specialization:** Specializes in financial news and analysis covering a broad range of publicly traded companies and investments, focusing on North American markets.
- **Usage in Study:** Employed for gathering insights and sentiments from financial analysts and investor commentary.

### Data Collection Methodology

Data collection from WRDS involved utilizing Structured Query Language (SQL) on the WRDS platform to access and extract specific datasets:

- **Market-Related Data:** Sourced from the Center for Research in Security Prices (CRSP) to obtain comprehensive information on stock prices, returns, and market indices.
- **Corporate Financial Data:** Extracted from Compustat, focusing on extensive historical financial data for U.S. and Canadian companies.
- **Bond-Related Information:** Collected from both Mergent for detailed bond deal structures and the Trade Reporting and Compliance Engine (TRACE) for transactional bond data, including corporate and government agency bonds.

Unstructured data from Seeking Alpha was harvested using web scraping techniques to capture relevant financial news articles, analyst reports, and investor comments. This method allowed for the extraction of rich textual content which was then processed using natural language processing (NLP) tools to analyze sentiments and extract meaningful insights related to financial markets and specific companies.

This approach ensured precise and consistent retrieval of data aligned with our research objectives, leveraging robust data management tools to handle, integrate, and process the data efficiently while adhering to strict data security and compliance standards.
