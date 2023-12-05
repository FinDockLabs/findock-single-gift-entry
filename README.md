<a href="https://githubsfdeploy.herokuapp.com?owner=FinDockLabs&repo=findock-single-gift-entry&ref=main">
  <img alt="Deploy to Salesforce"
       src="https://raw.githubusercontent.com/afawcett/githubsfdeploy/master/deploy.png"></a>

```text
NOTE: to be able to deploy this project to your Salesforce production environment your overall test code coverage needs to meet Salesforce thresholds.
Although this project has 100% coverage, existing custom code in your environment might push the overall coverage below the threshold. 
```

# FinDock for Fundraising: Single Gift Entry

The components in this repository can be used to integrate the FinDock MOTO component into the Salesforce Fundraising Single Gift Entry feature.
To make easy entry of multiple Gift Entries easy and fast, the Flow loops after every entry.

The Salesforce Batch Gift Entry is not supported.

## Requirements

The prerequisites to deploy this repository are:
- Fundraising enabled and configured in your Salesforce environment
- The FinDock for Fundraising package is installed

## Full list of components

A quick description for what this repo contains:
- FinDock version of Salesforce Manage Gift Entries flow (cloned & customised)
- Visualforce Page to override the 'New Gift Entry' button
- LWC Component and Aura app to run the flow in a Visualfroce page

Supporting permissions are included.

```text
**Aura app**
aura/GiftEntry

**flows**
flows/Manage_Gift_Entries_Findock.flow

**LWC**
lwc/giftEntryLWC

**permissionsets**
permissionsets/FinDock_Single_Gift_Entry.permissionset

**pages**
pages/NewGiftEntry.page
```

## Installation

First make sure your user has permissions to all objects referenced by the components in this repository. This includes FinDock permissions and Fundraising permissions, then use one of the below options to deploy the code.
- use `sfdx` to deploy a selection of or all components.
- press the "Deploy to Salesforce" button at the top of this README and then press "Login to Salesforce" in the top right of your screen. Please note, the GitHub Salesforce Deploy Tool is provided open source by [andyinthecloud](http://andyinthecloud.com/category/githubsfdeploy/). No FinDock support is provided.
- any other deployment method you prefer.

## Configuration
- Override the 'New' button on the object 'Gift Entry' and point it to the Visualforce page `NewGiftEntry`
- Update the flow `Manage Gift Entries FinDock` to use the correct target in the `Take Payment` screen.
- Assign the permission set `FinDock Single Gift Entry` to the right users


## Contributing

When contributing to this repository, please first discuss the change you wish to make via an issue or any other method with FinDock before making a change.

## Support

FinDock Labs is a non-supported group in FinDock that releases applications. Despite the name, assistance for any of these applications is not provided by FinDock Support because they are not officially supported features. For a list of these apps, visit the FinDock Labs account on Github.

## License

This project is licensed under the MIT License - see the [LICENSE](/LICENSE) file for details
