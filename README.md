# AWS Layers
A collection of helpful layers for AWS lambda

Each directory will have it's own README.

In general though...
Lambda will unzip the file under the `opt/` directory and lambda is expecting
the code to be in a folder supported by the runtime. Using python as an example,
AWS Lambda would unzip this file from `s3`  `example.zip` into the `opt/`directory and would expect the following
file structure

```bash
python/
     lib/
       python3.7/
          site-packages/
             some_python_script.py
  ```

After creating the layer for your lamda function you would then import the file
as normal
```py
import some_python_script

def some_function():
  print("Hello World")
```


### Reference:
[Intro to lambda layers](https://towardsdatascience.com/introduction-to-amazon-lambda-layers-and-boto3-using-python3-39bd390add17)

[Configuration](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html)
