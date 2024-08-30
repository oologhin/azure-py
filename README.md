# azure-py
A simple python micro-service on Azure

# Steps

## Step1 : Env Prerequisites
    Make sure you environment is ready
    Update you VS Studio
    Install Extensions: **Azure Tools**, **Docker**, **Python**, **Azure Resource Manager (ARM) Tools**
    Verify you github project

## Step 2 : Code
    ### Flask app.py file
    ### Dockerfile to dockerise my app

## Step 3 : Set Gihub do build the container and deploy it
    ### 3.1. create the asible-deploy.yml play book
    ### 3.2. Set up the azure secrets in github
        ```yml
        env:
        AZURE_CLIENT_ID: ${{ secrets.AZURE_CLIENT_ID }}
        AZURE_SECRET: ${{ secrets.AZURE_SECRET }}
        AZURE_SUBSCRIPTION_ID: ${{ secrets.AZURE_SUBSCRIPTION_ID }}
        AZURE_TENANT: ${{ secrets.AZURE_TENANT }}
        ```
        To securely pass sensitive information to your GitHub Actions workflow, you should use GitHub Secrets:

            Go to your GitHub repository.
            Click on the Settings tab.
            Click on Secrets in the left sidebar.
            Click on New repository secret to add each of your sensitive values (like AZURE_CLIENT_ID, AZURE_SECRET, etc.).
    ### 3.3. Set up the azure service principal in github
