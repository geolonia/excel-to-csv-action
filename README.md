# Excel to CSV Action

This action converts an Excel file to a CSV file.

## Inputs

### `input_dir`

**Required** The directory containing the Excel files to convert. Default `"./"`.

## Example usage

```yaml
name: Build and Deploy
on: [push]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    name: Convert Excel to CSV
    steps:
      - name: checkout
        uses: actions/checkout@v3

      # Generate tiles 🚀
      - name: 'Convert Excel to CSV'
        uses: geolonia/excel-to-csv-action@vmain
        with:
          input_dir: './data' # [Required] The directory containing the Excel files to convert.
```
