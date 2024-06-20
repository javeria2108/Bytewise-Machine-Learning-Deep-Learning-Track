# Git and GitHub

GitHub is a version control system used for managing your code and keeping track of updates and collaborations on your code. We use different branches to maintain and work on different versions of a project. We can see the full history of our project and also restore an earlier version of our project.

To check the installation of git, we can use the command:
```sh
git --version
```

To make a GitHub repository for our project, we use this command in the project directory:
```sh
git init
```

Here are other commands for working with git:

To check if a file is a part of our GitHub repository:
```sh
git status
```

To add a file to the staging environment, we use this command:
```sh
git add [filename]
```

For adding all files, we can use:
```sh
git add --all
```
or
```sh
git add -A
```

Now we can commit our changes. A commit is a kind of a checkpoint where we can roll back if we face a bug. We also add a commit message with the commit. The command is:
```sh
git commit -m "commit message"
```

We can directly commit and skip the staging step using:
```sh
git commit -a -m "message"
```

To view the history of commits, we use:
```sh
git log
```

## Branching in Git

Branching allows us to work on different parts of the project without modifying the code in the main branch. After the work on a new branch is completed, we can merge it with the main branch to keep it up to date. For example, to create a new branch for fixing a bug, we can use this command:
```sh
git branch bug-fix
```

To check the branch we are currently on:
```sh
git branch
```
The branch name with an asterisk `*` on the left shows our current branch.

To change our current branch:
```sh
git checkout bug-fix
```

To create an emergency branch, we use:
```sh
git checkout -b emergency-branch
```

To merge our current branch with another branch, we use:
```sh
git merge another-branch-name
```

After merging, we can delete the other temporary branch:
```sh
git branch -d another-branch-name
```
# GitHub

To connect our local git repository to our new repository on GitHub:
```sh
git remote add origin URL
```

Now to push our master branch to the remote repository:
```sh
git push --set-upstream origin master
```

`git pull` is used to fetch all changes from the tracked branch to your local repository.

When we create a new branch using the GUI on GitHub, we can pull it to our local repository using:
```sh
git pull
```

If we create a new branch locally and want to push it to GitHub, we can use:
```sh
git push origin new-branch
```
## For Contributing: 
We fork the repository we want to contribute to. Then we clone the code to our device and open it in our code editor. We check the existing remote origins and add the URL of our forked repo as another remote origin. After we are finished with the changes we can commit the changes to our origin. This will make our branch ahead of the original repo branch. So we can raise a pull request and add a suitable description for our changes to be reviewed by others who have access to the default branch. If they approve the changes they merge our branch with theirs. 

## Data Science, AI, Machine Learning, and Deep Learning

For understanding the difference between these terms, I read the following article: [Data Science vs Artificial Intelligence vs Machine Learning vs Deep Learning](https://towardsdatascience.com/data-science-vs-artificial-intelligence-vs-machine-learning-vs-deep-learning-9fadd8bda583).

To summarize the article in simple words:

- **Data Science**: In data science, we deal with data to make business decisions, gain insights, and understand user trends. This field involves prescriptive analysis. Data science uses machine learning algorithms to make predictions and discover patterns in data.

- **Artificial Intelligence (AI)**: AI is the comprehensive term that refers to making our computer systems intelligent enough to understand data, learn from data, and make decisions. It encompasses a wide range of techniques and technologies aimed at creating intelligent behavior in machines.

- **Machine Learning (ML)**: ML is an implementation of AI that includes various algorithms used to train a machine. In machine learning, we make our machine "learn" based on training data and test it using test data. It involves the creation of models that can make predictions or decisions without being explicitly programmed to perform the task.

- **Deep Learning (DL)**: When we have a huge amount of data and cannot compromise on accuracy, we use deep learning. Deep learning is an advanced subset of machine learning, utilizing neural networks with many layers. It is used in applications like recommendation systems on entertainment platforms (e.g., Netflix), self-driving cars, and more. Deep learning algorithms require substantial computational power and large datasets.

In essence, AI evolved to machine learning, and ML evolved to deep learning. These algorithms are fundamental to data science. Ultimately, it all revolves around data.
