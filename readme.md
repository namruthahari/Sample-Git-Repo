# Tutorial for contributing to a project with Git and GitHub: Beginners

Let's learn **GitHub**! Feel free to use the issues in this **git** sample **Project** to learn **Git** and **Github**. Add commands you learned that are useful to make this like documentation. Hopefully it will be fun and teach you so you can contribute to bigger projects in the future.

### Mini tutorial for beginners

To contribute to a project the first thing you have to do is:

1. **Create a Fork of the repository:** we will have a button that specifically says **Fork** which will generate us an exact copy of the project we want to contribute to.
2. Then we clone the repository from our terminal.

**Commands**:

``` bash
git clone [url] myproject
```

**Explanation**:

* `git clone` allows us to specify that we will clone the repository. 
* `url` refers to the project where we want to contribute in this case `https://github.com/namruthahari/Sample-Git-Repo.git`.
* `myproject` refers to the name we want to give to the project in our local files, in case we don't give it a name it will use the repository name.

**Example:**

``` bash
git clone https://github.com/namruthahari/Sample-Git-Repo.git myproject
```

After cloning the repository you can start contributing to any file in the project. In our case we will create an `index.html` file.

We have created the `index.html` file now we want to keep track of that file.

The first thing we will do is:

3. Add our file to the scenario with the command:

``` bash
git add .
```

**Explanation:**

1. `git add .` adds the changes that have been made to our repository, in this way we will send the changes to wait on the stage.

4. Check the status of our files with the command:

``` bash
git status -s
```

**Explanation:**

1. with `git status` we are telling git that we want to check the status of the files we have added.
2. `-s` is a shorthand for output information indicating what change has been made to the file and the file name.

**output**:

```
M index.html
```

Now let's say we have added some information in the `index.html` file.

``` html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tutorial</title>
</head>

<body>
    <h1>Git and GitHub</h1>
</body>

</html>
```

After adding the information, we will do the same process:

We check the status with `git status -s`

**Output:**

``` 
M index.html 
```

2. We then use the `git add -A` command to add the changes made to the scenario.

**Explanation:**

1. `-A` adds the files that have been modified. This command is mostly used to avoid adding files that have been created on the fly.

We have already added our changes to the scenario, now we want to save those changes in a **commit**. 

5. We will do this through the command:

```bash
git commit -m "Add index.html"
```

**Explanation**:

1. `git commit` creates an instant snapshot of all the code we have written and files we have added.
2. `git commit -m " "` is used as a quick way to add a message.
3. `"Add index.html"` inside the quotes has to be a short message explaining what we have done.



From there, we can see all the **commits** we have done with the command:

```bash
git log --pretty=oneline
```

**Explanation**:

1. `git log` shows us the history of **commits** we have performed.
2. `git log --pretty=oneline` is a shorthand for displaying the **commits** in a reduced form on a single line.



After that we can upload our contribution to our repository. To do this the first thing we have to do is:

1. rename the branch

```bash
git branch -M main
```

**note**: the name we specify in this example is main, but you can give any name to your branch, e.g. **dev** or **example**.

**explanation**:

`git branch -M` helps us to change the branch name to a new name, so when using the command we have to specify the branch name, example: `git branch -M dev`.

2. Add the remote branch

```bash
git remote add origin [url]
```

**Explanation**:

1. With this command what we will do is send the commits from our **local branch** to our **remote branch**, once synchronized all the changes will be sent to the repository.

**Example**:

```bash
git remote add origin https://github.com/namruthahari/Sample-Git-Repo.git
```

3. After synchronizing our branch we do a **push** to upload everything to our repository.

```bash
git push origin main
```

**Explanation**:

1. What this command does is to send all the **commit** containing all the changes we have made from there, everything we have done will be reflected in our remote branch.
2. So we specify it to do a **push** to our remote **main** branch.
3. From there we can update the page and we will see all the uploaded files in our repository.



When everything is **ready** to commit to the **official** repository we will get a **message** that will say the following:

**This branch is 1 commit ahead of namruthahari:main.** right there it asks us to make a **Pull request** or a **compare**.

What we will do is the following:

1. We will give **click** where it says **Pull request**: it will compare if we don't have any error when joining the two branches, in case we don't have error we will see in green that we can merge the branches automatically.
2. We will give **click** in the green button that says **Create pull request**.
3. We write a **title** and a **description**.
4. We **click** again where it says **Create pull request**.
5. **Done**: now we have sent a request to merge our branch with the main project branch.

## Extra:

**Want to learn how to contribute?**

You can take this repository as an example to take your first steps. Follow the knowledge you have already acquired for yourself or this small tutorial.

**Do you want to learn more about Git and GitHub?

Documentation, books and videos about Git:
[Click here](https://git-scm.com/doc)

GitHub documentation:
[Click here](https://docs.github.com/en/github)