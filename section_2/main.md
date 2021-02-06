# gitFlow Workflow
The gitFlow Workflow is a branching model for development focused on collaboration and scaling.

## Branches
A standard gitFlow model will have 5 branch types:
1. main - The production branch. There can only be one. It is eternal (or at least lives as long as your project). Whenever changes are merged into the main branch this is by definition a new production release.
2. hotfixes - One or more branches focused on fixing critical bugs in the main branch that cannot wait for the next version. These branches are short-lived, existing only as long as needed to develop a bug fix. When completed, changes are merged into both the main and develop branches.
3. release branches - The release branch is a staging area to test new features and the next version of a project. Bug fixes discovered during testing are made directly on the release branch. Once you are satisfied with the code in the release branch, it is merged into the main branch as the next production release.
4. develop - This is where the next version of your project begins. Develop branches start from a fork of the main branch, and are merged with hotfixes prior to being merged into a release branch.
5. feature branches - This is where all the new features are created and what enables parallel development. Feature branches are forked from the develop branch, and merged back in once they're ready for release. Feature branches live for as long as needed, until the feature is merged into a develop branch or it is abandoned. Work on one specific feature branch can continue while others are completed and merged into develop, release, and eventually the main branch.

![gitFlowBranchDiagram](/images/gitflow_diagram.png)
