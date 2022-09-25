### Using Git
This is a cheatsheet created for future developers. The team should use this to document Git commands and the methodologies used while developing these projects.

---
#### Organizations
A GitHub Organization was created to store the team projects as remote repositories. The new team can be added to this organization and it allows for everyone to have access to previous projects.

#### Cloning a Remote Repository
Cloning a remote repository that is stored on GitHub is the easiest way to create a tracked repository on your personal machine. Doing so allows you to make changes to the existing code and documents stored in the remote repository or to develop new material, then to commit your changes and additions to the remote repository. This allows other users to then pull those changes to their machine for further development. 

To clone a remote repository, use the following procedure:
1. At the [CU-Boeing-Projects](https://github.com/CU-Boeing-Projects) organization homepage, click one of the links to the repository you want to clone.
2. Click the GREEN button that says, "Code".
3. From the drop down menu, copy the URL of the remote repository.
4. Open a terminal on your machine.
5. Navigate to the location there you want the remote repository to be cloned using the "cd" commands.
6. Use the command ```git clone https://github.com/CU-Boeing-Projects/Fall-2022```
7. Open that repository however you would like (VsCode will do)

#### Setting Global Username
In order for Git to track commits by users, a global username must be set. This should only need to be done one time and might require a login. If a login is required, use the directions below to get a token from GitHub that allows you to verify your identity.

[resource](https://support.atlassian.com/bitbucket-cloud/docs/configure-your-dvcs-username-for-commits/)