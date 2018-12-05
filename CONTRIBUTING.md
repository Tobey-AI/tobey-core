# Contributing

If you want to help making the next level of the Smart Assistants this is the right place.
To become a contributor for **Tobey AI** you can follow the steps described below:

## Getting started

1. You need a Github account.
2. Create a [new issue](https://github.com/Tobey-AI/tobey-core/issues), making sure that it doesn't exist already:

- If you found a **bug**: Make sure to describe the bug properly and provide the steps to reproduce it.

- If it is a **new feature**: Make sure to provide a detailed description of the new feature, including how it should work. 

- If you want to fix/implement the issue by yourself, you can [fork the Github project](https://help.github.com/articles/fork-a-repo/).

## Development

### Tools

Tobey Core is being implemented as a UWP app running on Windows IOT. 
Please find the list of adopted tools below:
- Visual Studio 2017 Community edition.
- Github extention for Visual Studio. https://visualstudio.github.com

### Branching and PRs strategy

1. Create a [new issue](https://github.com/Tobey-AI/tobey-core/issues).

2. [Fork the project](https://help.github.com/articles/fork-a-repo/).

3. Create a new branch from 'master'. Each branch name should end with the Github issue ID. For example, if your Github issue name is: *issue-001* , your branch should be named as follows:

    - If the issue is related to a bug, **bug-001**.
    
    - If the issue is related to a new feature, **feat-001**.

4. Please follow the object oriented design and patterns already present in the solution as much as possible.

5. Please make sure your code will be properly documented. You can find the .Net documentation guidelines at this link: https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments 

6. Make sure that each commit comment will contain the issue ID which is related to, together with a proper description of what is contained.

7. Make sure there are no warnings or errors in your commits.

8. Sync your fork with the original (*upstream*) project. This step is needed to guarantee that your fork is in sync with the latest status of the original repository.

**From your Fork**:

   - Pull from the master branch to make sure your local master is synced.

   - Merge the master branch into your branch.

   - Resolve any conflicts

   - You can finally [raise a PR on Github](https://help.github.com/articles/about-pull-requests/) to be reviewed and merged. 

The entire process is clearly explained on this web article:<br/>
http://doc.fireflymigration.com/working-with-github-fork-in-visual-studio.html

If accepted, your fork will be pulled into the original repository. 

**Make sure you never push or merge your Pull Requests**. Let another reviewer review your request.

**Important**:
Even if you have write permission to the master branch of your fork, make sure you never work on the master branch.
