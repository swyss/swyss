# Git Submodules Cheat-Sheet

Git Submodules allow you to keep a Git repository as a subdirectory of another Git repository. This is useful for including libraries, frameworks, or other external projects that your project depends on.

## Quick and Dirty

1. **clone a repository**
```console
git clone <repository-url>
```
2. **check status**
```console
git status
```
> check if everything is ok

3. **add a submodule**
> create a folder in repo then:

```console
cd <submodule-folder-path>
git submodule add <repository-url> 
```
> repository-url is needed -> create a git-repo first

4. **check status**
```console
git status
```

5. **update and commit**
```console
git git add .
git commit -m "Add GitHub submodule"
```

## Adding a Submodule

1. **Add the submodule:** Navigate to your main project directory and use the command:

```console
git submodule add <repository-url> <path/to/submodule>
```

Replace `<repository-url>` with the URL of the repository you want to add as a submodule and `<path/to/submodule>` with the path within your main project where the submodule should be placed.

2. **Initialize the submodule:** After adding a submodule, you need to initialize it:

```console
git submodule init
```


3. **Clone submodule content:** To clone the content of the submodule and check out the appropriate commit, use:

```console
git submodule update
```


## Cloning a Project with Submodules

When you clone a repository that contains submodules, the submodule directories are initialized, but they will be empty. To initialize and clone the submodules, use:

```console
git clone --recurse-submodules <repository-url>
```

Alternatively, if you've already cloned the repository, you can initialize and update the submodules with:

```console
git submodule update --init --recursive
```


## Pulling Changes in Submodules

To pull changes from the upstream in all submodules, use:

```console
git submodule update --remote
```

This command fetches new changes from the upstream of all submodules and updates the working directory to the commit specified in the superproject.

## Pushing Changes to Submodules

If you make changes within a submodule and want to push them back to the submodule's repository, you need to:


1. **Navigate to the submodule directory:**

```console
cd <path/to/submodule>
```


2. **Commit and push as usual:**

```console
git commit -am "Your commit message"
git push
```


## Removing a Submodule

To remove a submodule, you need to:
1. **Delete the relevant section from the `.gitmodules` file.**
2. **Stage the `.gitmodules` changes:**

```console
git add .gitmodules
```

3. **Delete the relevant section from `.git/config`.**
4. **Remove the submodule files from the working tree:**

```console
git rm --cached <path/to/submodule>
```

5. **Commit your changes:**

```console
git commit -m "Removed submodule"
```

6. **Delete the now untracked submodule files:**

```console
rm -rf <path/to/submodule>
```


Remember, when working with submodules, it's important to communicate with your team about changes to submodules to ensure everyone's repository stays in sync.







