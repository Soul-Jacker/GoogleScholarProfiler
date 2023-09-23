# Google Scholar Profiler

![image](https://github.com/Soul-Jacker/GoogleScholarProfiler/assets/88346723/ad16e758-48b3-4f69-bd43-bb15a14ee35f)

## Description

This Python code performs two main tasks:

1. Retrieves the scholarly data of a single author based on the search query.
2. Retrieves the scholarly data of multiple authors listed in a Google Sheet.

The code uses the `scholarly` Python package for fetching information from Google Scholar and pandas for data manipulation. It also uses Google Colab's `auth` and `gspread` to interact with Google Sheets.

## Dependencies

- `scholarly`
- `pandas`
- `google.colab`
- `gspread`
- `oauth2client`

You can install these packages using pip:

```bash
pip install scholarly pandas google-auth-oauthlib gspread oauth2client
```

## How to Run

### Single Author Search

1. Run the block under "Run the single author search".
2. Provide the name of the author you want to search in the `Scholar_Name` variable.
3. Execute the code. The program will output a DataFrame containing various scholarly metrics of the single author.

### Multiple Authors Search

1. Before running the code, ensure you have a Google Sheet named `GoogleScholarProfiler_INPUT` with the list of author names.
2. Run the block under "Run multiple author search".
3. Execute the code. The program will output a DataFrame containing various scholarly metrics of the listed authors.

## Output Columns

- `name`: Name of the scholar.
- `scholar_id`: Unique ID for the scholar.
- `affiliation`: Current affiliated institution.
- `email_domain`: The domain of the affiliated institution.
- `citedby`: Total number of citations.
- `citedby5y`: Total number of citations in the last 5 years.
- `hindex`: H-index of the author.
- `hindex5y`: H-index of the author in the last 5 years.
- `i10index`: i10-Index of the author.
- `i10index5y`: i10-Index of the author in the last 5 years.

## Exceptions Handling

The code handles exceptions for author names not found during the search and will print `COULD NOT FIND: [author_name]`.

## Known Limitations

- The `interests` section has been omitted for the single author search.
- The program assumes the Google Sheet has only one column with the author names.

## Future Work

- Implement rate limiting to adhere to Google Scholar's rate limits.
- Extend the functionality to search by multiple criteria.
  
## Author

Your name or alias here.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
