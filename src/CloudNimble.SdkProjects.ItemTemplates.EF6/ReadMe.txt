========================================
VS2017 ItemTemplates for SdkProjects
========================================

By CloudNimble, Inc.
Written By: Robert McLaws
Last Updated: 29 October 2017

========================================
Instructions
========================================

1) Let the wizard complete. It will throw errors. Ignore them, the EF tools have not been updated for VS2017 yet.
   NOTE: Whatever code-generation technique you selected will not execute because of those errors.

2) Close the solution. VS will pop up a dialog saying it has conflicting changes. Click Ignore.

3) Re-open the solution.

4) Right-click the T4 templates and select "Run Custom Tool". If VS pops up a dialog saying it has conflicting changes, select "Discard".
   If it pops up a "Save" dialog, select "No".

5) The project should re-load with the EDMX file excluded, and the resources nested under the T4 templates.