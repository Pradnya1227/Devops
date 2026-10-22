# Jenkins and GitHub Integration

## Aim
To integrate Jenkins with a GitHub repository and configure Jenkins to pull source code from GitHub.

## Objectives
- Understand Jenkins integration with GitHub.
- Configure a Jenkins Freestyle project.
- Connect Jenkins to a Git repository.
- Retrieve source code from GitHub.
- Verify the integration through the Jenkins console output.

## Tools Required
- Jenkins
- GitHub account
- Git
- Java JDK

## Procedure

1. Create a repository on GitHub.
2. Add a `README.md` file to the repository.
3. Open Jenkins at `http://localhost:8080`.
4. Click **New Item** and create a Freestyle project named `GitHub-Integration`.
5. Under **Source Code Management**, select **Git**.
6. Enter the GitHub repository URL.
7. Select the appropriate credentials. For a public repository, credentials can usually be left as `- none -`.
8. Specify the branch as `*/main`, if the repository uses the `main` branch.
9. Under **Build Steps**, select **Execute Windows batch command**.
10. Enter the following commands:

   ```bat
   echo Code successfully pulled from GitHub!
   dir
   ```

11. Save the configuration and click **Build Now**.
12. Open the latest build and select **Console Output** to verify the result.

## Expected Output

The Jenkins console should display:

```text
Code successfully pulled from GitHub!
```

The console should also list the files checked out from the repository and show:

```text
Finished: SUCCESS
```

## Result

Jenkins was configured to connect to a GitHub repository and retrieve its source code. The integration was verified through the build console output.
