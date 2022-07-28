# Data Preparation Basics
## 1. Filtering and selecting
* Introducing the pandas Library
    * Why pandas - fast data cleaning, preparaion and analysis; easy to use for data visualization and machine learning.
    * What is pandas - built on top of NumPy, makes it easy to work with arrays and matrices.
    * Indexing in pandas
        * An index is a list of integers or labels you use to uniquely identify rows or columns.
        * This course uses: 
            * A set of square-brackets `[...]`
            * the `.loc[]` indexer.
    * `DataFrame` object - acts like a spreadsheet in Excel, made of a set of `Series` objects, and are indexables.
    * `Series` object - a row or column that is indexed.
    ![pandas DataFrame](./resources/images/pandas%20DataFrame.jpg)
* Comparison Operators in Python

    Operator | Arithmetic Operaion
    ---------|--------------------
    == | True if values of two operands are equal
    != | True if values of two operands are unequal
    <> | True if values of two operands are unequal
    \> | True if the left operand has a value that's greater than the right operand
    < | True if the left operand has a value that's less than the right operand
    \>= | True if the left operand has a value that's greater than or equal the right operand
    <= | True if the left operand has a value that's less than or equal the right operand
* [Code Demonstration](./code/02-01.ipynb)
    * Plain indexing
    * Data slicing 
    * Arithmetic comparison

## 2. Treating missing values
* By Default, missing values are represented with `Nan`: _Not a Number_
    * **Note**: If your dataset has 0s, 99s, or 999s, be sure to either drop or approximate them as you would with missing values.

* Assume the below data from customer satisfaction survey:
    * _Sally_ and _Jim_ didn't provide _Quality of Work_ information.
    * At the same time, both responded to 75% of their request for information. So we can't drop them from the dataset.
    * The other 3 participants provided resonses to _Quality of Work_ so we can't drop this column.

        Respondant Name | Speed of Service (1-10) | Friendliness of Staff (1-10) | Quality of Wor (1-10) | Price (1-10)
        ----------------|-------------------------|------------------------------|-----------------------|-------------
        Sally | 10 | 10 | **missing** | 8
        Jim | 10 | 9 | **missing** | 10
        Rod | 9 | 8 | 9 | 9
        Sam | 8 | 10 | 8 | 10
        Jane | 10 | 4 | 10 | 6

* As a solution we can take the **Average** of the available values of _Quality of Work_ and replace the missing values with this **Average**.
    * This will be an **Approximation**. Many times, using an **Approximation** would be better than dropping the missing values.

        Respondant Name | Speed of Service (1-10) | Friendliness of Staff (1-10) | Quality of Wor (1-10) | Price (1-10)
        ----------------|-------------------------|------------------------------|-----------------------|-------------
        Sally | 10 | 10 | **8** | 8
        Jim | 10 | 9 | **8** | 10
        Rod | 9 | 8 | 9 | 9
        Sam | 8 | 10 | 8 | 10
        Jane | 10 | 4 | 10 | 6

* [Code Demonstration](./code/02-02.ipynb)
    * Discovering what's missing.
    * Filling in for missing values.
    * Counting missing values.
    * Filtering oyt missing values.
## 3. Removing duplicates
* Why remove duplicates?
    * To maintain accurate, consistent datasets.
    * To avoid producing erronous or misleading statistics.
    * For example, imagine a customer made 3 purchase with 3 different credit cards but with the same ZIP code.
        * Based on the Credit Card Number, Sally will look like 3 different customers, all  from the same ZIP code.
        * If we fail to examine the other attributes of the customer so we identify and remove duplicates, Sally transactions would the skew the results of a customer demographic analysis because Sally will be counted as 3 different people rather than 1.

            Name | Zip | Credit Card Number
            -----|-----|-------------------
            Sally | 32803 | 123456789123
            Sally | 32803 | 234567891234
            Sally | 32803 | 345678912345

* [Code Demonstration](./code/02-03.ipynb)

## 4. Concatenating and Transforming
* **Concatenating**: Combining data from seperate sources.
* **Transforming**: conferting and reformatting data to teh format that's necessary for your purposes.
* [Code Demonstration](./code/02-04.ipynb)

## 5. Grouping and aggregation
* Grouping and Aggregation are useful for exploring and describing your dataset in its subgroups.
* Reasons for Grouping Data:
    * To compare subsets.
    * To deduce reasons why subgroups differ.
    * To subset your data for your analysis.
* [Code Demonstration](./code/02-05.ipynb)

[<<Previous](../unit01-Introduction%20to%20the%20data%20professions/README.md) | [Next>>]()