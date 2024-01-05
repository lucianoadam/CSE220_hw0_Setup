# Homework 0: Test GitHub Classroom Workflow
We will use this homework assignment to test the Github Classroom workflow that we will use to submit assignments in this course. This homework will not be graded. Use this opportunity to make sure that you have everything setup before working with the homework assignments. Do not hesitate to contact the teaching staff if you are stuck.

## Required Software
- [Git](https://git-scm.com/downloads)\
Mac OSX and Linux systems have git pre-installed. Check by running the command `git --version` in a terminal. On Windows, you will use git bash to run git commands.

## Compilation
- You can use any framework that can compile C programs. However, I would recomend that you do it with online VM [Codespaces](https://github.com/features/codespaces). It gives you free 60 hrs of machine time each month. This will be enough for the programming assignments for this course.
- [Codespaces documentation](https://docs.github.com/en/codespaces/overview).

## Setting up SSH

You will need to use the SSH protocol to securely connect to the assignment repository hosted on GitHub. Follow the listed steps below to setup ssh with GitHub:

- If you already have an account, add the Stonybrook email to your existing GitHub account. See [here](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-user-account/managing-email-preferences/adding-an-email-address-to-your-github-account) for reference. If you created a new GitHub account with your Stonybrook email and SBU Net ID as your username, then skip this step.

- Once you have a GitHub account, you will need to setup SSH public and private keys. These keys will be used by GitHub to authenticate your system. If you already have an existing public/private key pair in your system, you can simply use those keys. How do you know your system has these keys? See [here](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/checking-for-existing-ssh-keys). Skip next step, if the keys exist in your system.

- If your system does not have any public/private key pairs, do not panic. We can easily generate a new key pair. See [here](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) on how to generate new keys.

- The next step is add the public/private key pair in your system to your GitHub account. This is how GitHub knows which keys to use for authenticating your system. See [here](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) for how to add keys to GitHub.

- The final step is to test the SSH connection. See [here](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/testing-your-ssh-connection) for testing your setup.

## Downloading The Repository

Once you have setup SSH to work with GitHub, we can now seamlessly download the assignment repository from GitHub and push or upload code to the repository. You should be able to see a **Code** button in the repository. Click on the button and select the **SSH** option. Copy the corresponding link under this option and run the following command in your local terminal or git bash:

`git clone <paste-ssh-link>`

You will see a directory or folder named *./assignment-name-yourID* created in your current directory or folder. Inside this folder, you will find the following files:
- *hello.c* with a function that returns a message. This is the file in which you will write your code. For this assignment all you have to do is fill in your name, NetID, and SBU ID.

- *test.sh* This file contains test code to verify the behavior of *hello.c*. In this assignment it contains code to verify if the expected message is being returned from the function in *hello.c*. In future assignments, this file will have numerous test cases which you will need to pass. You will get credit for every test case you pass. You must not change this file. If you do then you won't receive any credit for the homework.

## Submitting to GitHub
As described in the previous section, you will write all your code in the *hello.c* file. For this assignment, fill in your full name, NetID, and SBU ID in the parts marked for you in *hello.c*. Submit your code using the following commands:

- Add your file to git:\
`git add hello.c`

- Save your file with a comment:\
`git commit -m "first draft"`

- Submit file:\
`git push`

### Run test
`make test`

## After submission/pushing
After you submit or push code to your repository, open the assignment repository on GitHub in a browser. Look for a **green tick** or a **red cross**. A green tick indicates that all tests have passed. A red cross indicates some or all tests may have failed. When you click on the red cross and then *details*, you will see a report indicating which test methods in *hello.c* passed and which methods failed. In this assignment, there is only one test method. Since you won't be changing any code, the test will pass. Hence, you will see a green tick indicating that the test has passed. For future assignments, you can click on the report to view the test report. You can keep changing your code till all tests pass or you see the green tick. However, submissions/pushes will only be allowed till a deadline, after which you will not be allowed to submit/push. This homework assignment has no deadline.

#### Possible Issues
If you see a red cross for this homework assignment, it is most likely because there is something wrong in your local system's configuration. All your assignments will be tested with CodeSpace. Therefore, **it is highly recomended to check it using Codespaces VM first before submitting it.**

## Testing Your code locally

You can also verify if the test cases pass locally in your system before pushing to the remote repository. Use the following command in a terminal to run the tests:

`make test`

After the running the command you should see a test report with the tests that passed/failed. Expect to see a green tick in GitHub after you push code that passed all tests locally, in which case you are done!

