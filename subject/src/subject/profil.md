# Profile page

This page is designed to allow a user to view their information, modify it, and also delete or log out of their account.

## Features

-   A text field (email)
-   Input verification based on the criteria provided in the subject
-   A profile picture
-   An account deletion button
-   A logout button

## Input Verification Criteria

-   An email containing at least one '@'

## Behavior

Since this page is a mock-up, you are not required to implement a real account modification system.

When clicking the "Modify my information" button, and after input validation, the new email should be saved and the data updated locally.

When clicking the logout button, delete the local data and redirect to the login page.

When clicking the account deletion button, perform the same actions as logging out, in our case since we do not have a database.

**⚠️ Make sure to save the email locally so that it can be used later.**

## To Go Further

To extend beyond the subject, at the end of the project you can try to integrate a real account modification system by updating the data in a SQL or NoSQL database such as MySQL or MongoDB, whether local or remote.
