## Pull Requests

Making pull requests to a GitHub repository is common. You do it when contributing code to your work projects, side projects with friends, and open source projects. When you make a pull request to a GitHub repository, you're asking the repository's administrators to incorporate the code in your pull request into their main repository. 

If you are a member of the main repository to which you make your pull request, you can make a pull request from a branch. Create a new branch, edit the code, and then issue a pull request. If you are not a member of the repository, if you have access, you can fork the repository to your GitHub repo and then create the pull request. This exercise focuses on the first scenario. The second scenario is more advanced and not necessary to know for this course.

For this exercise, you should use the cloned version of the GitHub Exercises repository that you made in the previous exercises. You already have read and write access to it. You need read access to create a pull request. Plus, you need write access to create a branch for your pull request.

Here are the steps you will follow for creating a pull request.

First, in your GitHub Exercises repository, create a new branch called `new-feature`.

Second, in the root folder for your project, add a new file called `newFeature.js`. In the new file, write an array of strings and a `for` loop. Using the array and `for` loop, build a sentence. The fourth word in your sentence must be `four`, but the word `four` cannot appear in your array.

Third, now you should stage, commit, and push your changes to the `new-feature` branch.

Fourth, go to your GitHub repository for the GitHub Exercises project. Find the link toward the top of the page called "Pull requests." Click it to visit the Pull requests page.

Fifth, on the Pull requests page, click the green button that says "New pull request." It takes you to a page for comparing the changes between two branches.

Sixth, you should see two dropdown menus on your compare changes page. One for "base" and the other "compare". For each dropdown, you need to select a branch from your repository. For "base", make sure you've selected "main". For "compare", make sure you've selected "new-feature".

Seventh, you should now see a green button that says "Create pull request." Click it. Fill out the information in the inputs that appear, and then click the green "Create pull request" button again.

In the Github Exercises repository, the "Pull requests" link should now display the number `1` next to it. Click it and look at your pull request.

If you'd like to try creating a pull request using a fork, here are some resources to help guide you:

[GitHub Fork / Pull](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork)  
[Blog about fork-and-branch git flow](https://blog.scottlowe.org/2015/01/27/using-fork-branch-git-workflow/)
