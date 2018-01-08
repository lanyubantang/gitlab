#### On this page:

* [Open a shell](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#open-a-shell)
* [Check if Git has already been installed](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#check-if-git-has-already-been-installed)
* [Add your Git username and set your email](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#add-your-git-username-and-set-your-email)
* [Check your information](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#check-your-information)
* [Basic Git commands](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#basic-git-commands)
  * [Go to the master branch to pull the latest changes from there](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#go-to-the-master-branch-to-pull-the-latest-changes-from-there)
  * [Download the latest changes in the project](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#download-the-latest-changes-in-the-project)
  * [Create a branch](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#create-a-branch)
  * [Work on a branch that has already been created](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#work-on-a-branch-that-has-already-been-created)
  * [View the changes you've made](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#view-the-changes-you-ve-made)
  * [Add changes to commit](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#add-changes-to-commit)
  * [Send changes to gitlab.com](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#send-changes-to-gitlab-com)
  * [Delete all changes in the Git repository, but leave unstaged things](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#delete-all-changes-in-the-git-repository-but-leave-unstaged-things)
  * [Delete all changes in the Git repository, including untracked files](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#delete-all-changes-in-the-git-repository-including-untracked-files)
  * [Merge created branch with master branch](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#merge-created-branch-with-master-branch)
  * [Merge master branch with created branch](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#merge-master-branch-with-created-branch)

* [GitLab Documentation](https://docs.gitlab.com/ee/README.html)
* [GitLab basics](https://docs.gitlab.com/ee/gitlab-basics/README.html)
* Start using Git on the command line

# Start using Git on the command line {#start-using-git-on-the-command-line}

If you want to start using Git and GitLab, make sure that you have created and/or signed into an account on GitLab.

## Open a shell {#open-a-shell}

Depending on your operating system, you will need to use a shell of your preference. Here are some suggestions:

* [Terminal](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line)on Mac OSX

* [GitBash](https://msysgit.github.io/)on Windows

* [Linux Terminal](http://www.howtogeek.com/140679/beginner-geek-how-to-start-using-the-linux-terminal/)on Linux

## Check if Git has already been installed {#check-if-git-has-already-been-installed}

Git is usually preinstalled on Mac and Linux.

Type the following command and then press enter:

```
git --version

```

You should receive a message that will tell you which Git version you have on your computer. If you don’t receive a "Git version" message, it means that you need to[download Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

If Git doesn't automatically download, there's an option on the website to[download manually](https://git-scm.com/downloads). Then follow the steps on the installation window.

After you are finished installing, open a new shell and type "git --version" again to verify that it was correctly installed.

## Add your Git username and set your email {#add-your-git-username-and-set-your-email}

It is important to configure your Git username and email address as every Git commit will use this information to identify you as the author.

On your shell, type the following command to add your username:

```
git config --global user.name "YOUR_USERNAME"

```

Then verify that you have the correct username:

```
git config --global user.name

```

To set your email address, type the following command:

```
git config --global user.email "your_email_address@example.com"

```

To verify that you entered your email correctly, type:

```
git config --global user.email

```

You'll need to do this only once as you are using the`--global`option. It tells Git to always use this information for anything you do on that system. If you want to override this with a different username or email address for specific projects, you can run the command without the`--global`option when you’re in that project.

## Check your information {#check-your-information}

To view the information that you entered, type:

```
git config --global --list

```

## Basic Git commands {#basic-git-commands}

### Go to the master branch to pull the latest changes from there {#go-to-the-master-branch-to-pull-the-latest-changes-from-there}

```
git checkout master

```

### Download the latest changes in the project {#download-the-latest-changes-in-the-project}

This is for you to work on an up-to-date copy \(it is important to do every time you work on a project\), while you setup tracking branches.

```
git pull REMOTE NAME-OF-BRANCH -u

```

\(REMOTE: origin\) \(NAME-OF-BRANCH: could be "master" or an existing branch\)

### Create a branch {#create-a-branch}

Spaces won't be recognized, so you will need to use a hyphen or underscore.

```
git checkout -b NAME-OF-BRANCH

```

### Work on a branch that has already been created {#work-on-a-branch-that-has-already-been-created}

```
git checkout NAME-OF-BRANCH

```

### View the changes you've made {#view-the-changes-you-39-ve-made}

It's important to be aware of what's happening and what's the status of your changes.

```
git status

```

### Add changes to commit {#add-changes-to-commit}

You'll see your changes in red when you type "git status".

```
git add CHANGES IN RED
git commit -m "DESCRIBE THE INTENTION OF THE COMMIT"

```

### Send changes to gitlab.com {#send-changes-to-gitlab-com}

```
git push REMOTE NAME-OF-BRANCH

```

### Delete all changes in the Git repository, but leave unstaged things {#delete-all-changes-in-the-git-repository-but-leave-unstaged-things}

```
git checkout .

```

### Delete all changes in the Git repository, including untracked files {#delete-all-changes-in-the-git-repository-including-untracked-files}

```
git clean -f

```

### Merge created branch with master branch {#merge-created-branch-with-master-branch}

You need to be in the created branch.

```
git checkout NAME-OF-BRANCH
git merge master

```

### Merge master branch with created branch {#merge-master-branch-with-created-branch}

You need to be in the master branch.

```
git checkout master
git merge NAME-OF-BRANCH
```



