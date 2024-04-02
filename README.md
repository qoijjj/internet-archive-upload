## Inputs

* `access-key`: Your archive.org access key
* `secret-key`:  Your archive.org secret key
* `identifier`: The unique identifier of the archive.org item where the file will be stored
* `files`: The file or folder path inside the action's filesystem to upload

## Usage

Upload a single file.

```yaml
name: Example action
jobs:
  job:
    name: Upload
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Upload file to archive.org
        uses: qoijjj/internet-archive-upload@v7
        with:
          access-key: ${{ secrets.IA_ACCESS_KEY }}
          secret-key: ${{ secrets.IA_SECRET_KEY }}
          identifier: your-item
          files: your-file.jpg
```

Upload a directory of files.

```yaml
name: Example action
jobs:
  job:
    name: Upload
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Upload file to archive.org
        uses: qoijjj/internet-archive-upload@v7
        with:
          access-key: ${{ secrets.IA_ACCESS_KEY }}
          secret-key: ${{ secrets.IA_SECRET_KEY }}
          identifier: your-item
          files: your-files/
```
