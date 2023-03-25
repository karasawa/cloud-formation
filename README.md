# cloud-formation
cloud-formation用のテンプレート置き場

aws s3 mb s3://nested-demo

aws cloudformation package --template-file main.yaml --s3-bucket nested-demo --output-template-file artifact.yaml

aws cloudformation deploy --template-file artifact.yaml --stack-name nested-demo

aws s3 rm s3://nested-demo --recursive