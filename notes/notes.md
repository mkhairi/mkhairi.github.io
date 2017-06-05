# Rails

Quick note

Reset primary key sequence!
```ruby ActiveRecord::Base.connection.tables.each { |t| ActiveRecord::Base.connection.reset_pk_sequence!(t) }```



# Git

## checkout specific tags

```$ git clone will give you the whole repository.```

After the clone, you can list the tags with $ git tag -l and then checkout a specific tag:

```$ git checkout tags/<tag_name>```

Even better, checkout and create a branch (other you will be on a branch named after the revision number of tag):

```$ git checkout tags/<tag_name> -b <tag_name>```

## author

```git commit --author "New Author Name <New Author Email>" -m "commit message "```

Interactive rebase off of a point earlier in the history than the commit you need to modify ```(git rebase -i <earliercommit>)```. In the list of commits being rebased, change the text from pick to edit next to the hash of the one you want to modify. Then when git prompts you to change the commit, use this:

```git commit --amend --author="Author Name <email@address.com>"```
For example, if your commit history is ```A-B-C-D-E-F``` with ```F``` as ```HEAD```, and you want to change the author of ```C``` and ```D```, then you would...

Specify ```git rebase -i B```
change the lines for both C and D to edit
Once the rebase started, it would first pause at C
You would ```git commit --amend --author="Author Name <email@address.com>"```
Then ```git rebase --continue```
It would pause again at D
Then you would ```git commit --amend --author="Author Name <email@address.com>"``` again
```git rebase --continue```
The rebase would complete.

##reset
Setting your branch to exactly match the remote branch can be done in two steps:

git fetch origin
git reset --hard origin/master
If you want to save your current branch's state before doing this (just in case), you can do:

git commit -a -m "Saving my work, just in case"
git branch my-saved-work

checkout deleted file only
git ls-files -d | xargs git checkout --
