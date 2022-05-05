# mk-aws-lambda-zip
A python script to make a zip file with libraries for your python code. 

Builds an AWS lambda deployment package. As explained here: 
https://docs.aws.amazon.com/lambda/latest/dg/python-package.html

## Requires python to run
```sh
python3 mk_aws_lambda_zip.py
``` 

## Configuring the script

```sh
# 1 Open the file
vim mk_aws_lambda_zip.py

# 2 Edit these lines

pipLibraries = ['requests']
outputFilename = "lambda.zip"
pythonCodeLocation = "python"
pipTempLocation = "tmp"


```

## PUT THE SCRIPT 1 Directory ABOVE your lambda code
ie. source code location:  C:/Code/python/my_lambda.py ( containing lambda_handler(event, context))
then Put this script here: C:/Code 

### Example file structure

```text
> tree
.
├── mk_aws_lambda_zip.py <--- Put the script here
├── python  <--- Your code
│   └── utils
│       └── api  <--- any nested file structure will be preserved!
├── tmp  <--- The libraries are installed here before they are baked into the root of the zip file
│   ├── bin
│   └── (etc etc ...)
│
└── lambda.zip   <--- Resulting zip for aws lambda

```
