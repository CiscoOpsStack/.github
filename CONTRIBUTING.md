# Contributing to Ops Stack

First off, thank you for considering contributing to Ops Stack! Your help is greatly appreciated.

## How to Contribute

### Reporting Bugs

If you find a bug, please report it by opening an issue in the [issue tracker](https://github.com/CiscoOpsStack/[repo-name]/issues). Please include:

- A clear and descriptive title.
- A detailed description of the problem.
- Steps to reproduce the issue.
- Any relevant logs or screenshots.

### Suggesting Enhancements

If you have an idea for an enhancement, please open an issue in the [issue tracker](https://github.com/CiscoOpsStack/[repo-name]/issues) and include:

- A clear and descriptive title.
- A detailed description of the enhancement.
- Any relevant examples or mockups.

### Best Practices for Naming GitHub Branches in Ops Stack

1. **Include the Jira Ticket ID:**

   - Always include the Jira ticket ID in the branch name. This makes it easy to trace the branch back to the corresponding Jira issue.
   - Example: `feature/PROJ-1234-add-login-page`

2. **Use Descriptive Names:**

   - Include a brief, descriptive summary of the work being done. This helps others understand the purpose of the branch at a glance.
   - Example: `bugfix/PROJ-5678-fix-login-error`

3. **Use Consistent Prefixes:**
   - Use consistent prefixes to indicate the type of work being done. Common prefixes include `feature/`, `bugfix/`, `hotfix/`, and `chore/`.
   - Example: `chore/PROJ-9101-update-dependencies`
   - **Feature:** Adds new functionality or enhancements.
   - **Bugfix:** Resolves identified issues or bugs.
   - **Hotfix:** Applies urgent fixes to critical issues in production.
   - **Chore:** Performs maintenance tasks, code cleanup, or updates.
   -
4. **Use Hyphens to Separate Words:**

   - Use hyphens (`-`) to separate words in the branch name for better readability.
   - Example: `feature/PROJ-1234-add-login-page`

5. **Keep It Short and Simple:**

   - While it's important to be descriptive, try to keep the branch name as short as possible while still conveying the necessary information.
   - Example: `feature/PROJ-1234-login-page`

6. **Avoid Special Characters:**
   - Avoid using special characters or spaces in branch names. Stick to alphanumeric characters and hyphens.
   - Example: `feature/PROJ-1234-add-login-page` (instead of `feature/PROJ-1234_add_login_page`)

### Examples of Branch Naming Conventions

Here are some examples of branch names following these best practices:

- **Feature Branch:**

  - `feature/PROJ-1234-add-login-page`
  - `feature/PROJ-5678-implement-search-functionality`

- **Bugfix Branch:**

  - `bugfix/PROJ-9101-fix-login-error`
  - `bugfix/PROJ-1122-resolve-crash-on-startup`

- **Hotfix Branch:**

  - `hotfix/PROJ-3344-patch-security-vulnerability`
  - `hotfix/PROJ-5566-fix-critical-bug`

- **Chore Branch:**
  - `chore/PROJ-7788-update-dependencies`
  - `chore/PROJ-9900-refactor-codebase`

### Example Workflow

1. **Create a New Branch:**

   - When starting work on a Jira ticket, create a new branch using the ticket ID and a descriptive name.

   ```sh
   git checkout -b feature/PROJ-1234-add-login-page
   ```

2. **Make Changes and Commit:**

   - Make the necessary changes and commit them to the branch.

   ```sh
   git add .
   git commit -m "Add login page functionality (PROJ-1234)"
   ```

3. **Push the Branch:**

   - Push the branch to the remote repository.

   ```sh
   git push origin feature/PROJ-1234-add-login-page
   ```

4. **Open a Pull Request:**
   - Open a pull request from the new branch to the main branch, referencing the Jira ticket in the pull request description.

By following these best practices, you can create clear, consistent, and informative branch names that make it easier to manage and track your work in both GitHub and Jira.

Certainly! Here are detailed instructions for adding a pull request (PR) using the branch naming pattern that includes Jira ticket names. This guide assumes you have the necessary permissions to create branches and submit pull requests in the repository.

### Instructions for Adding a Pull Request

#### 1. **Create a New Branch**

First, ensure you are on the main branch and that your local repository is up to date.

```sh
# Navigate to the main branch
git checkout main

# Pull the latest changes
git pull origin main
```

Next, create a new branch using the Jira ticket ID and a descriptive name.

```sh
# Create a new branch
git checkout -b feature/PROJ-1234-add-login-page
```

#### 2. **Make Your Changes**

Make the necessary changes in your local repository. This could involve editing files, adding new files, or deleting files.

#### 3. **Commit Your Changes**

Once you have made your changes, stage them and commit with a descriptive message that includes the Jira ticket ID.

```sh
# Stage your changes
git add .

# Commit your changes
git commit -m "Add login page functionality (PROJ-1234)"
```

#### 4. **Push the Branch to the Remote Repository**

Push your new branch to the remote repository.

```sh
# Push the new branch
git push origin feature/PROJ-1234-add-login-page
```

#### 5. **Open a Pull Request**

1. **Navigate to the Repository on GitHub:**

   - Go to your repository on GitHub.

2. **Open the Pull Request:**

   - You should see a prompt to open a pull request for the branch you just pushed. If not, click on the "Pull requests" tab and then the "New pull request" button.

3. **Select the Branch:**

   - Ensure that the base branch is set to `main` (or the appropriate branch you are merging into) and the compare branch is set to `feature/PROJ-1234-add-login-page`.

4. **Fill Out the Pull Request Template:**

   - Provide a clear and detailed description of the changes you made. Reference the Jira ticket in the description.
   - Example:

     ```markdown
     ## Description

     This pull request adds the login page functionality as described in Jira ticket PROJ-1234. The changes include:

     - A new login form component
     - Validation for user input
     - Integration with the authentication API

     ## Jira Ticket

     [PROJ-1234](https://your-jira-instance.atlassian.net/browse/PROJ-1234)

     ## Type of Change

     - [x] New feature (non-breaking change which adds functionality)

     ## How Has This Been Tested?

     - Manual testing of the login form
     - Unit tests for the login component

     ## Checklist:

     - [x] My code follows the style guidelines of this project
     - [x] I have performed a self-review of my own code
     - [x] I have commented my code, particularly in hard-to-understand areas
     - [x] I have made corresponding changes to the documentation
     - [x] My changes generate no new warnings
     - [x] I have added tests that prove my fix is effective or that my feature works
     - [x] New and existing unit tests pass locally with my changes
     ```

5. **Submit the Pull Request:**
   - Click the "Create pull request" button to submit your PR.

#### 6. **Address Feedback**

Be prepared to address any feedback or requested changes from code reviewers. Make the necessary changes in your branch, commit them, and push the updates.

```sh
# Make changes based on feedback
# (edit files as needed)

# Stage and commit the changes
git add .
git commit -m "Address feedback for PROJ-1234"

# Push the updates
git push origin feature/PROJ-1234-add-login-page
```

#### 7. **Merge the Pull Request**

Once the pull request has been reviewed and approved, you can merge it into the main branch. This can be done by clicking the "Merge pull request" button on GitHub.

### Code Style

Please ensure your code adheres to the project's coding standards. This includes:

- Consistent indentation and spacing.
- Descriptive variable and function names.
- Comments where necessary to explain complex logic.

### Running Tests

Before submitting your pull request, make sure all tests pass. You can run the tests using:

```sh
# Example command, terratest example
go test -v -timeout 30m
```
