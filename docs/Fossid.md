# Fossid
A new, major, software update is now available for all customers and for evaluation purposes for prospects. The recent “21.2” release brings significant updates to the Software Composition Analysis tool for Enterprise, including improvements in the user interface, automatic component identification, OAuth2.0 authentication with Azure AD, and more.

# UI Improvements
The User Interface has been re-designed with a new, always on top, main menu. The re-design offers a cleaner, more uncluttered view, and a more purposeful grouping of features and functionality. Buttons in the scan interface have been removed if there is a corresponding menu item, and new dialog windows are movable and resizable. Further UI additions include:

 > File tree in scans.
 > Language selection in user profile.
 > Adding/creating components manually in scans.
 > Component information is in one single dialog instead of four.
 > Auto-Approval based on License Policies
 > FossID allows creating automatic approval policies for components depending on component license. Component approval requests will then be approved or rejected based on the policy without involvement of an approver. Auto-approvals not only save time and effort, but are a great help enforcing rules and safeguarding against AGPL.

## Automatic Component Identification
This new scan option allows for pending identifications to be resolved automatically by assigning the top component match to all files with pending identification and marking those files as identified.

## Authentication Through Azure Active Directory
FossID now supports OAuth2.0 authentication of WebApp users with Azure Active Directory. FossID users can thus use the same login mechanism as for any other system on the customer premises that also supports the same authentication method. This is both more secure and more convenient.

## CPE Identifier List
FossID maintains a list of components/versions combinations with known CPEs. This information is used to automatically suggest values when manually adding components.

The list of component/versions and CPEs is continuously updated out-of-the-box or can be manually updated.

Easier Installation and System Maintenance
Several improvements and additions have been made to ease installation and system maintenance.

The installation and update documentation is now provided in a single, structured document with sections per operating system or specific part configuration instead of being distributed across a number of different files.

Background tasks (such as updating vulnerability information for components with CPEs) no longer require the use of crontab. These tasks will be configured and enabled out of the box, and the configuration can now be updated from within the tool.

Scanning will be done in a few different steps (such as scanning, cleanup, dependency analysis). Each step is regarded as a process and a process can have different states: QUEUED, RUNNING, FINISHED, FAILED and Idle. The status and details of all processes can be examined from within the WebApp.