---
layout: post
date: "2017-11-26 20:57:00"
categories: Jekyll Github Hosting
---

Hosting a Jekyll site on Github pages is pretty easy. Here's what I had to do to host this site.

> Assuming that you have a Gihub account and Jekyll site already set up.

1. Firstly, we need to create a repository in our Github account. I've called mine jekyll-blog, [at this link](https://github.com/geejay81/jekyll-blog).

2. Next, we will edit the _config.yml file. Change the baseurl value to the same name as your Github repository. Here I have changed mine to jekyll-blog as this is the name of my repository.

    ``` yaml
    baseurl: "jekyll-blog"
    ```
3. Now we will initialise our local git repository. When running the command below, make sure that you are in the root directory of you Jekyll site:

    ``` git
    git init
    ```
4. Github uses a special branch name called *gh-pages* for hosting on Gihub Pages. We will create this branch and check it out so that we can work with it (and push up to our remote repository for hosting):

    ``` git
    git checkout -b gh-pages
    ```

5. We will now check the status of our gh-pages branch to see what needs to be commited:

    ``` git
    git status
    ```

    This will give us a result similar to below. As we haven't committed before, it should be all files:

    ```
    On branch gh-pages

    Initial commit

    Untracked files:
       (use "git add <file>..." to include in what will be committed)

            .gitignore
            404.html
            Gemfile
            Gemfile.lock
            _config.yml
            _drafts/
            _posts/
            about.md
            index.md
    ```

6. We can stage all of these files for our next commit by using the _add_ verb and _*_ to select all files:

    ``` git
    git add *
    ```

7. Now we will commit all of these files to our local repository:

    ``` git
    git commit -m "First commit"
    ```

8. To push the files to our remote repository on Github, we will need to tell our local Git db where the remote repository is. We can do this by adding an origin:

    ``` git
    git remote add origin https://github.com/geejay81/jekyll-blog.git
    ```

9. Finally, we can push the files in our local reposity up the gh-pages branch in the remote repository on Github:

    ``` git
    git push origin gh-pages
    ```

10. Now we can go to our Github Pages site followed by the name of the repository and see our new site!

> Credit: The code above has been adapted from the instructions given in a video by the Giraffe Academy. Visit their YouTube channel for plenty of informative videos on a range of subjects including Jekyll [Giraffe Academy](https://www.youtube.com/channel/UCvmINlrza7JHB1zkIOuXEbw)