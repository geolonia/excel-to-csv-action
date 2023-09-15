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

      - name: 'Convert Excel to CSV'
        uses: geolonia/excel-to-csv-action@main
        with:
          input_dir: './data' # [Required] The directory containing the Excel files to convert.
```

## Note
* Values output as CSV will be the values specified in the Excel cell format.
* For dates (cell format: date, user-defined), the values are output to CSV in `m/d/yy` format. 

## Development

```
$ git clone git@github.com:geolonia/excel-to-csv-action.git
$ cd excel-to-csv-action
$ npm install
```

### Build

```
$ npm run build
```


