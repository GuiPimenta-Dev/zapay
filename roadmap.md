
# Lambda Forge Road Map


Lambda Forge is a Framework that outlines a structured approach for organizing, developing, and deploying AWS Lambda functions, emphasizing a consistent directory setup to ensure modularity and maintainability. 

It has a command-line tool called *Forge* designed to simplify Lambda function creation by automating the setup process and generating a standard folder structure with necessary configurations and testing files, streamlining the development workflow and improving efficiency, especially for projects with multiple Lambda functions.

P.S: It automatically generates docs with swagger for all endpoints attached to API Gateway. :)


## Create a new directory:
```
mkdir zapay
cd zapay
````

## Create a new venv:
```
python3 -m venv venv
source venv/bin/activate
```
## Install lambda-forge from TestPYPI:
```
pip install lambda-forge==1.0.63 --extra-index-url https://pypi.org/simple --extra-index-url https://test.pypi.org/simple/
````

## Create a new project:
```
forge project zapay --repo-owner "GuiPimenta-Dev" --repo-name "zapay" --bucket "gui-docs"
````

## Create a new public function:

```
forge function hello_world --method "GET" --description "A simple hello word" --public
```

## Create a repository called zapay on GitHub:

```
git init
git add .
git commit -m "Initial commit"
git branch -M dev
git remote add origin git@github.com:GuiPimenta-Dev/zapay.git
git push -u origin dev
```

## Sync and deploy the dev stack to the cloud:

```
cdk synth
cdk deploy Dev-Zapay-Stack
````

# Go to the Pipeline section on the AWS Console and see the magic happening!
