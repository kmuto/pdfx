# pdfx

Make your PDFs compliant with PDF/X-1a.

## Pre-requisite

- Docker

## Quick Usage

Pull `vibranthq/pdfx` image from [Docker Hub](https://hub.docker.com/r/vibranthq/pdfx/).

```bash
docker pull vibranthq/pdfx
docker run --rm -it -v $PWD:/workdir vibranthq/pdfx ./input.pdf ./output.pdf
docker run --rm -it vibranthq/pdfx s3://bucket/input.pdf s3://bucket/output.pdf
```

for fetching and uploading AWS S3 resources, you need to set env var for `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`.

## Development Build

### Docker

```bash
docker build -t vibranthq/pdfx .
docker run --rm -it -v $PWD/workdir vibranthq/pdfx ./input.pdf ./output.pdf
docker run --rm -it vibranthq/pdfx s3://bucket/input.pdf s3://bucket/output.pdf
```

### Docker Compose

```bash
docker-compose build
docker-compose run pdfx ./input.pdf ./output.pdf
```

## Configuration

### Color Profile

There is a support only for **Japan 2001 Coated**. If you have any suggestions, please consider submitting an issue.

### Color Mode

Currently supports **CMYK** and planned to support **Grayscale** color mode.
