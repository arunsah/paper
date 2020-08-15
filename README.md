# paper
Experimental Rich Text Editor

[2020-08-15]

---


## Project setup

```shell
npm install
```

### Compiles and hot-reloads for development

```shell
npm run serve

```

### Compiles and minifies for production

```shell
npm run build
```

### Run your unit tests

```shell
npm run test:unit

```

### Lints and fixes files

```shell
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

### Deployment Guidelines

See [Deployment Guidelines](https://cli.vuejs.org/guide/deployment.html)

### Previewing Locally

The `dist` directory is meant to be served by an HTTP server (unless you've configured `publicPath` to be a relative value), so it will not work if you open `dist/index.html` directly over `file://` protocol. The easiest way to preview your production build locally is using a Node.js static file server, for example serve:

```shell
npm install -g serve
# -s flag means serve it in Single-Page Application mode
# which deals with the routing problem below
serve -s dist
```

## Git Branch

https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches

```shell

# check current branch
$ git branch

# If you want create a new branch:
$ git branch <name_of_your_new_branch>

# Before creating a new branch, pull the changes from upstream. Your master needs to be up to date.
$ git pull

# Create the branch on your local machine and switch in this branch
$ git checkout -b [name_of_your_new_branch]

# Push the branch on github
$ git push origin [name_of_your_new_branch]

# Fork branch from another branch
$ git checkout -b <new_sub_branch> <source_branch>

# Set upstream for new branch
$ git push --set-upstream origin [name_of_your_new_branch]

# see all branch
$ git branch -a

# switch branch
$ git checkout master
$ git checkout [name_of_your_branch]

# Add a new remote for your branch
$ git remote add [name_of_your_remote] [name_of_your_new_branch]

## Deletion

# Delete a branch on your local filesystem
$ git branch -d [name_of_your_new_branch]
# To force the deletion of local branch on your filesystem
$ git branch -D [name_of_your_new_branch]
# Delete the branch on github
$ git push origin :[name_of_your_new_branch]

## Merging

# (on branch development)
$ git merge master

# resolve any merge conflicts if there are any)
$ git checkout master
# (there won't be any conflicts now)
# If you want to keep track of who did the merge and when, you can use --no-ff flag while merging to do so.
$ git merge  --no-ff development
```

#### Squahing

```shell

$ git rebase -i head~[no_of_commits_to_squash_from_head_commit]

## Select [pick] base commit and [s] for commits to squash

## Select the comments to keep and remove extra comment.

$ git push origin [name_of_your_branch] -f

# In Vim, Press `Esc :wq` to save and quit
# Press `i` for insert mode
# In Vim, Press `Esc` key and type `:w` to save a file in vim.
# One can press `Esc` and type `:wq` to save changes to a file and exit from vim.

# Resolve all conflicts manually, mark them as resolved with
# `git add/rm <conflicted_files>` , then run `git rebase --continue` .
# You can instead skip this commit: run `git rebase --skip` .
# To abort and get back to the state before “git rebase”, run `git rebase --abort` .
```

### new repo

##### create a new repository on the command line

```shell
echo "# apollo-ms-filemanager-service" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/arunsah/apollo-ms-filemanager-service.git
git push -u origin master
```

##### push an existing repository from the command line

```shell
git remote add origin https://github.com/arunsah/apollo-ms-filemanager-service.git
git push -u origin master
```
