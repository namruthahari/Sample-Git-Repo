# Learning to use Git and GitHub: beginners

Let's learn **GitHub**! Feel free to use the issues in this **git** sample **Project** to learn **Git** and **Github**. Add commands you learned that are useful to make this like documentation. Hopefully it will be fun and teach you so you can contribute to bigger projects in the future.

### Mini course for beginners

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

