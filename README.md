# Updating Okta Directory Users in Bulk using Workato

This document provides step-by-step instructions on how to use the Workato recipe for bulk updating users in the Okta directory. The recipe leverages the Okta REST API to update user profiles and group memberships based on data in a CSV file.

## Prerequisites

- A Workato account with sufficient privileges to create and run recipes.
- Access to an Okta account with the necessary permissions to manage user profiles and group memberships.
- A CSV file containing the user data to be updated. The CSV file should have headers for FirstName, LastName, Email, Groups, and CustomAttribute (optional).

## Steps

1. Open the Workato recipe `bulk-update-okta-users.json` in your browser.

2. Download the recipe file by clicking the "Raw" button, right-clicking anywhere on the page, and selecting "Save as". Save the file with a `.json` extension.

3. Log in to your Workato account and navigate to the "Recipes" tab.

4. Click the "Import" button and select the recipe file you downloaded in step 2.

5. Once the recipe is imported, click on the "Configure" button to open the configuration page.

6. In the "CSV Import" section, select the file you want to use for updating the user data. You can either choose a file that is already in your Workato account or upload a new file from your computer. If you choose to upload a new file, you will need to specify the file name and worksheet name.

7. In the "Okta Connection" section, enter the following information:
    - Subdomain: Enter the subdomain of your Okta account. For example, if your Okta URL is `https://example.okta.com`, enter "example" as the subdomain.
    - API Token: Enter an Okta API token that has the necessary permissions to update user profiles and group memberships.

8. In the "User Profile Mapping" section, map the fields from your CSV file to the corresponding fields in the Okta user profile. You can leave fields unmapped if they are not needed for your use case.

9. In the "Group Mapping" section, map the Groups field from your CSV file to the corresponding field in the Okta user profile. If your CSV file does not contain group data, you can leave this field unmapped.

10. In the "Custom Attribute Mapping" section, map the CustomAttribute field from your CSV file to a custom attribute in the Okta user profile. If your CSV file does not contain custom attribute data, you can leave this field unmapped.

11. Click the "Save & Test" button to save your configuration and test the recipe. Workato will import the user data from your CSV file and attempt to update the corresponding user profiles and group memberships in Okta. If any errors occur, you will be able to view the error messages and make adjustments to your configuration as needed.

12. Once you have successfully tested the recipe, you can click the "Activate" button to run the recipe on a schedule or trigger.

This technical documentation should provide users with clear instructions on how to use the Workato recipe we have created to update user data in the Okta directory. Users can refer to this documentation as needed to ensure they are following the correct steps and avoiding common errors or pitfalls.
