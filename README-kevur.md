# Custom Notes

## Why?

* AWS Lambda Runtimes don't have imagemagick included. [The upstream project at Github](https://github.com/serverlesspub/imagemagick-aws-lambda-2) provides an imagemagick layer for Lambda.
* Problem: it does not support freetype / font support (e.g. to add text to your image via imagemagick)
* We can customize the layer here for ourselves

## Custom Features:

* freetype / font support

## Usage:

* Deploy custom layer to AWS lambda
* In SAM, you can use the layer version ARN to make your function use that layer.

## Dev / extend:

* to add more stuff, edit Makefile_ImageMagick
* to test: `make libs` to run build, `make bash` to inspect the build directory
* to deploy new version: `export AWS_REGION="eu-central-1"; make deploy DEPLOYMENT_BUCKET="my-bucket"`
