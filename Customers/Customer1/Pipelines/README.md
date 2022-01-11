<h1>CI/CD Pipelines</h1>

This folder contains all the different Azure DevOps pipelines in YAML format so they can be directly used in you DevOps project.

These pipelines are written using the Pipeline artifacts feature (see: https://docs.microsoft.com/es-es/azure/devops/pipelines/artifacts/pipeline-artifacts?view=azure-devops&tabs=yaml) and they contain build and deploy stages in a single pipeline.

In order for these pipelines to work, you need to install in the Files Validator extension from https://marketplace.visualstudio.com/items?itemName=roshkovski.Files-Validator in your Azure DevOps organization.


<h2>buildScripts.yml</h2>
Build pipeline that gets all the powershell scripts in the Scripts folder and publishes as a pipeline artifact to be used in other pipelines. It also validates powershell syntax.

<h2>analyticsRules.yml</h2>
Publishes Analytics Rules json file under AnalyticsRules folder as a pipeline artifact and executes CreateAnalyticsRules.ps1 script to deploy the rules defined in the json file. It also validates proper JSON syntax for the rules file.

<h2>alertRulesCICD.yml</h2>
Publishes Analytics Rules json file under AnalyticsRules folder as a pipeline artifact and executes CreateAnalyticsRulesAPI.ps1 script to deploy the rules defined in the json file.
deprecated - to figure out replacing solution

<h2>ARmultistage.yml</h2>
This pipeline has two different release stages that point to two different Azure workspaces. These can be in the same or different tenants, just need to modify the service connection and variable group.

<h2>huntingRulesCICD.yml</h2>
Publishes Hunting queries json file under HuntingRules folder as a pipeline artifact and executes CreateHuntingRulesAPI.ps1 script to deploy the hunting queries defined in the json file.

<h2>onboardingCICD.yml</h2>
Publishes Onboarding json file under Onboard folder as a pipeline artifact and executes InstallSentinel.ps1 script to install the Sentinel solution where needed.

<h2>playbooksCICD.yml</h2>
Publishes all json files under Playbooks folder as pipeline artifacts and executes CreatePlaybooks.ps1 script to create all the playbooks.

<h2>workbooksCICD.yml</h2>
Publishes all json files under Workbooks folder as pipeline artifacts and executes CreateWorkbooks.ps1 script to create all the workbooks.
