---
title: Development
nav_order: 9
has_children: false
---

# Sticky Selectron Development
## Prerequisites
- [VS Code](https://code.visualstudio.com/)
- [Salesforce DX CLI (SF/SFDX)](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_install_cli.htm)
- CumulusCI
-- Here's a Trailhead about CCI that includes the above: https://trailhead.salesforce.com/content/learn/modules/cumulusci-setup and https://cumulusci.readthedocs.io/en/latest/tutorial.html for more info
- Also our code is stored in Github, so you'll need Git too: https://docs.github.com/en/get-started/getting-started-with-git/set-up-git

- You'll need to configure your SFDX to work with a DevHub first before you can create scratch orgs. Here's a couple few that talk about doing that:
-- https://trailhead.salesforce.com/content/learn/projects/quick-start-salesforce-dx
-- https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_setup_enable_devhub.htm
-- https://www.salesforceben.com/salesforce-scratch-orgs/

- So once you've got all the tools installed and a DevHub connected to your sfdx you can download the code and get started



  
## Working with our code
- If you navigate on your computer to where you want the files to be, you can download the code (using either ssh or http). This example is http:
`git clone https://github.com/SFDO-Community/sticky-selectron.git`
- That will make a sticky-selectron folder, so go into it with `cd sticky-selectron`
- then `cci flow run dev_org --org dev` will create a new scratch org with our code (note that scratch orgs only last 7 days by default)
- and `cci task run deploy_example_flows --org dev` will install the example flow (note that we can/should probably combine this task with the dev_org flow definition next time we change the cci config metadata)
- If you want to create a large number of example Accounts to work with in your scratch org you can use Snowfakery like this `cci task run snowfakery --recipe datasets/Snowfakery-Account-Example.recipe.yml --run-until-recipe-repeated 5 --org dev` (this example command will make 15 records because the recipe has 3 records inside)
- and finally `cci org browser dev` will open the new scratch org in a browser

After that you can go into Salesforce setup and navigate to flows. You'll see an example flow from our code called Sticky Selectron Example Accounts Flow. And running that flow will let you see the LWC config and sample run




  
