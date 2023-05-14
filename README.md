# Okta Bulk User Update Workato Recipe

This Workato recipe allows you to bulk update user profiles and group memberships in the Okta directory using a CSV file. The recipe leverages the Okta REST API to automate the process of updating user data, and can be configured to run on a schedule or trigger.

## Prerequisites

- An Okta account with the necessary permissions to manage user profiles and group memberships.
- A CSV file containing the user data to be updated. The CSV file should have headers for `FirstName`, `LastName`, `Email`, `Groups`, and `CustomAttribute` (optional).
- A Workato account with the necessary permissions to create and run recipes.

## Steps

1. Log in to your Workato account and create a new recipe.
2. Select "Trigger" as the first step of the recipe and choose the appropriate trigger for your use case. For example, you may choose "Scheduled" to run the recipe on a daily or weekly basis, or "New file in folder" to trigger the recipe when a new CSV file is uploaded to a specific folder.
3. Add the "CSV Parser" action as the next step of the recipe. Configure the action to parse the CSV file and map the appropriate fields to the corresponding variables. For example, you may map the `FirstName` field to the `First Name` variable and the `Email` field to the `Email Address` variable.
4. Add the "Loop" action as the next step of the recipe. Configure the action to loop through each row of the parsed CSV file.
5. Add the "Okta Update User" action as the next step of the recipe. Configure the action to update the corresponding user profile and group memberships in Okta using the variables from the current row of the loop. For example, you may use the `First Name`, `Last Name`, and `Email Address` variables to update the user's profile, and the `Groups` variable to add the user to the appropriate groups.
6. (Optional) Add the "Delay" action as the next step of the recipe to insert a delay between API calls to avoid hitting rate limits.
7. (Optional) Add additional actions as needed for error handling, logging, or other requirements.
8. Save and run the recipe to update the user profiles and group memberships in the Okta directory based on the data in the CSV file.

## CSV File Format

The CSV file should have headers for the following fields:

- `FirstName`: The first name of the user.
- `LastName`: The last name of the user.
- `Email`: The email address of the user. This field is required and must be unique.
- `Groups`: A comma-separated list of group names that the user should be a member of.
- `CustomAttribute`: A custom attribute that should be updated for the user.

Note: Ensure that the variables in the Okta Update User action match the headers in your CSV file. If necessary, modify the variable names to match the column headers in your CSV file.
