# python-zip-script-lambda-ready
A python script to make a zip file with libraries for your python code. 
Builds it AWS lambda compatible.

## Requires python to run
```sh
python3 make_aws_lambda_zip_with_libs.py
``` 

## Example file structure

```text
tree
.
├── make-python-zip.py <--- Put the script here
├── python  <--- Your code
│   └── utils
│       └── api  <--- any nested file structure will be preserved!
├── tmp  <--- The libraries are installed here before they are baked into the root of the zip file
│   ├── bin
│   └── (etc etc ...)
│
└── lambda.zip   <--- Resulting zip for aws lambda

```
