# Experiment – 10
## Title
Creation, Storage, and Loading of Datasets using Pandas

## Aim
To study the process of manual dataset creation in Python and understand the methodologies for loading, exporting, and performing initial structural analysis on external data files.

## Objectives
* To learn how to construct a DataFrame from raw Python dictionaries
* To explore various file export formats including CSV and Excel
* To understand the mechanisms for loading external datasets from local and cloud directories
* To perform basic structural inspection using shape, size, and metadata attributes
* To implement data selection and filtering techniques (loc, iloc, and column-based access)
* To apply basic descriptive statistical functions and schema modification methods

---

## Theory on Dataset Management
In the lifecycle of Exploratory Data Analysis (EDA), data management begins with either manual creation for testing purposes or, more commonly, loading large-scale datasets from external sources. Pandas provides a robust framework for handling these transitions through its specialized input/output (I/O) API.

### 1. Manual Dataset Construction
Data can be structured in Python using dictionaries where keys represent column headers and values (lists) represent the data rows. By passing these structures into a **DataFrame constructor**, Pandas creates a tabular representation that supports relational operations. This is vital for creating dummy data or small-scale look-up tables.

### 2. Data Persistence (Exporting)
Once a dataset is created or modified in the memory (RAM), it must be saved to permanent storage to be shared or used later. 
* **CSV (Comma Separated Values)**: A lightweight, plain-text format that is universally accepted across data platforms.
* **Excel (.xlsx)**: A binary format that supports multiple sheets and complex formatting, often used in business environments.



---

## Structural Inspection Theory
Before analyzing data, a researcher must understand its "topology" or physical structure. Pandas provides several attributes for this:
* **Shape**: Returns a tuple representing the dimensionality (Rows, Columns). Knowing the number of observations is critical for statistical validity.
* **Size**: Represents the total number of elements (cells) in the dataset (Rows × Columns).
* **Info()**: A comprehensive method that displays the DataFrame's schema, including column names, non-null counts (to identify missing data), and memory usage.
* **Dtypes**: Every column in a DataFrame is assigned a specific data type (int64, float64, object/string). Understanding these types prevents logic errors during mathematical operations.



---

## Data Retrieval and Modification
### 1. Accessing Observations
Data can be retrieved through two primary methods:
* **Label-based Selection**: Using column names to extract specific features or using `.loc` to find rows based on their index labels.
* **Position-based Selection**: Using `.iloc` to access data based on its numerical integer position.

### 2. Slicing the Dataset
To avoid overwhelming the system when dealing with thousands of rows, researchers use the **Head** and **Tail** functions. `head()` allows a preview of the initial records to verify successful loading, while `tail()` helps in checking the end of the file for potential corruption or trailing empty rows.

### 3. Dynamic Schema Modification
A dataset is rarely perfect upon loading. Pandas allows for dynamic updates:
* **Column Addition**: New features can be derived or added to an existing DataFrame.
* **Column Dropping**: Irrelevant features can be removed from the view to reduce memory overhead and focus the analysis.
* **Aggregate Functions**: Simple operations like `min()` and `max()` can be applied to numerical columns to find the range of specific variables.

---

## Applications in Engineering
* **Sensor Data Logging**: In Electronics & Telecommunication, Pandas is used to collect and structure real-time signals from sensors into timestamped datasets.
* **Network Analysis**: Loading log files from servers to analyze traffic patterns and peak usage times.
* **Market Analysis**: Comparing prices and specifications of hardware components to optimize procurement.

---

## Conclusion
The ability to create, save, and reload datasets is the foundation of any data-driven project. By mastering the I/O operations and structural attributes of Pandas, researchers can efficiently transition from raw data collection to deep analytical processing. Understanding how to inspect the shape and info of a dataset ensures that the subsequent analysis is performed on a clean and well-understood schema.
