## Contributing to a Project code

### Create new branch

From the Git Command prompt use

```
git checkout -b TestBranch
```

the output should be something like

```
amit@amit-desktop:~/dev/code/courtres$ git checkout -b TestBranch
M	views/layout.ejs
Switched to a new branch 'TestBranch'
```

### Do the code change
Use an editor to make the code changes.

### Commit and push your changes
Add the changed file to index

```
git add README.md
```

Commit the code

```
git commit -m "Test Change"
```

sample output

```
amit@amit-desktop:~/dev/code/courtres$ git commit -m "Test Change"
[TestBranch d7201f3] Test Change
 1 file changed, 2 insertions(+)
```

Push your local branch to remote

```
git push -u github TestBranch
```

### Creating a pull request

https://help.github.com/articles/using-pull-requests/
