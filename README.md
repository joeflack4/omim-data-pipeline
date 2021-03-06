# OMIM Data Pipeline
Tools for ingesting data from [omim.org](https://omim.org).

Currently, the only feature is `get_codes_by_yyyy_mm`, which returns a list of 
OMIM codes and their prefixes from https://omim.org/statistics/update.

## Usage: Command Line Interface
### Syntax
1. `python -m omim_data_pipeline YYYY/MM`
2. `python -m omim_data_pipeline YYYY/MM --outpath my/output/path`
2. `python -m omim_data_pipeline YYYY/MM --outpath my/output/path/my_file.txt`

### Instantiated
1. `python -m omim_data_pipeline 2021/05`
2. `python -m omim_data_pipeline 2021/05 --outpath ~/Desktop`
2. `python -m omim_data_pipeline 2021/05 --outpath ~/Desktop/omim.txt`

### Examples
Command:  
`python -m omim_data_pipeline 2021/05`

Response:
```py
[('#', '619340'),
 ('#', '619355'),
 ('*', '619357'),
 ('*', '619358'),
 ('*', '619359'),
 ('#', '619325'),
 ('#', '619328'),
 ('*', '100850'),
 ...
 ('#', '613102')]
 ```

## Usage: Python API
Using `get_codes_by_yyyy_mm()` will return a list of tuples.

```py
from omim_data_pipeline import get_codes_by_yyyy_mm

code_tuples = get_codes_by_yyyy_mm('2021/05')
```
