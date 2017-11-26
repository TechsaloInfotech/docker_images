Usage

This repository automatically builds containers for using the python3.6.3 and terraform v0.10.7 command line program. 


Example
Steps:
1. To initialize provider plugins
    docker run -v $(pwd):/app/ -w /app/ test terraform init
2. To plan/Apply
    docker run -v $(pwd):/app/ -w /app/ test terraform plan -target=your_terraform_file.tf
    