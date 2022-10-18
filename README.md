# maven
A repository in Maven holds build artifacts and dependencies of varying types.  There are exactly two types of repositories: local and remote:
the local repository is a directory on the computer where Maven runs. It caches remote downloads and contains temporary build artifacts that you have not yet released.
remote repositories refer to any other type of repository, accessed by a variety of protocols such as file:// and https://. These repositories might be a truly remote repository set up by a third party to provide their artifacts for downloading (for example, repo.maven.apache.org). Other "remote" repositories may be internal repositories set up on a file or HTTP server within your company, used to share private artifacts between development teams and for releases.


Local and remote repositories are structured the same way so that scripts can run on either side, or they can be synced for offline use. The layout of the repositories is completely transparent to the Maven user, however.

Using Repositories
In general, you should not need to do anything with the local repository on a regular basis, except clean it out if you are short on disk space (or erase it completely if you are willing to download everything again).

For the remote repositories, they are used for both downloading and uploading (if you have the permission to do so).

Downloading from a Remote Repository
Downloading in Maven is triggered by a project declaring a dependency that is not present in the local repository (or for a SNAPSHOT, when the remote repository contains one that is newer). By default, Maven will download from the central repository.

To override this, you need to specify a mirror as shown in Using Mirrors for Repositories.

You can set this in your settings.xml file to globally use a certain mirror. However, it is common for a project to customise the repository in its pom.xml and that your setting will take precedence. If dependencies are not being found, check that you have not overridden the remote repository.

For more information on dependencies, see Dependency Mechanism.

How to Get Support
Support for Maven is available in a variety of different forms.

To get started, search the documentation, issue management system, the wiki or the mailing list archives to see if the problem has been solved or reported before.

If the problem has not been reported before, the recommended way to get help is to subscribe to the Maven Users Mailing list. Many other users and Maven developers will answer your questions there, and the answer will be archived for others in the future.
