## Steps of the Pipeline
* Orbs: The following Orbs are declared and are called before running any steps on the backend or front end: Node, Elastic BeanStalk and AWS CLI. These need to be loaded first in order to do any of the steps for installing prereqs, building the apps and deploying the app to AWS. You will also need to supply the appropriate ENV variables in CircleCI for AWS. These steps, once called, will install the components and it is necessary for these to be called first.
* Checkout Code: obtains the necessary files needed to run the tasks needed
* Front End/Back End Dependency Install: npm install is ran on the front end project and will install all necessary packages required for both apps to work.
* Lint: ESLint is called to make sure that our freontend code is formatted in accordance to code style.
* Front End/Back End Build: This step will build the app for production 
* Deployment: Assuming that all credentials are loaded in the env, the code will be deployed to EB (for the backend) and S3 (for the front end)