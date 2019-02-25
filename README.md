# Automatic Workflow Launch

The Automatic Workflow Launch project demonstrates the launching of a workflow from a server event or action.

#### How it works
A method is attached to the ItemType as an OnAfterAdd/OnAfterUpdate server event. When the item is saved with the Launch Workflow property set to 1, the method finds the Workflow Map by name, then instantiates and starts it. The same method is attached to the ItemType as an action, allowing the workflow to be launched using a menu choice.

## History

Release | Notes
--------|--------
[v1.0.1](https://github.com/ArasLabs/auto-workflow-branching/releases/tag/v1.0.1) | Tested 11.0 SP12, SP15. Tested on Edge, Firefox 60 ESR, Chrome.
[v1.0.0](https://github.com/ArasLabs/auto-workflow-branching/releases/tag/v1.0.0) | First release. Tested on Internet Explorer 11, Firefox 38 ESR, Chrome. Though built and tested using Aras 11.0 SP7, this project should function in older releases of Aras 11.0 and Aras 10.0.

#### Supported Aras Versions

Project | Aras
--------|------
[v1.0.1](https://github.com/ArasLabs/auto-workflow-branching/releases/tag/v1.0.1) | 10.0 SPx, 11.0 SP7+, 11.0 SP12+, 11.0 SP15
[v1.0.0](https://github.com/ArasLabs/auto-workflow-branching/releases/tag/v1.0.0) | 10.0 SPx, 11.0 SP7; Old Community Board Migration

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 11.0 SPx preferred)
2. Aras Package Import tool
3. AutoWorkflowBranching import package

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\AutoWorkflowLaunch\Import\imports.mf` file in the Manifest File field.
6. Select **aras.labs.WorkflowAutomationExamples** and **aras.labs.AutoWorkflowLaunch** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.

You are now ready to login to Aras and try out the Automatic Workflow Launch action/event.

## Usage

1. Log in to Aras as admin.
2. Navigate to **Workflow Examples** in the table of contents (TOC).
3. Create a new Workflow Launch Example item.
4. Click **Save/Unlock/Close**.
5. Edit the item and check the **Launch Workflow** checkbox.
6. Navigate to **My Innovator > My Inbasket** in the TOC.
7. Search for the newly created assignment.
8. Repeat steps 2-4.
9. Choose the new item and run the **Workflow Launch Example** action (under the Actions menu)
10. Navigate to **My Innovator > My Inbasket** in the TOC.
11. Search for the newly created assignment.

As an alternative to checking My Inbasket, you can also determine whether an item has a workflow process from the item's worm. On the item form, select **Views > Workflow** from the main menu to view the workflow process. The resulting dialog will show the workflow process, if it exists, or an empty grid if there is no workflow process for the item.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Original Aras community project written by Rob McAveney at Aras Corp.

Project rewritten for Aras 11.0 by Alexander Sklyarskiy. @asklyarskiy

Documented and published by Eli Donahue at Aras Labs. @elijdonahue

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
