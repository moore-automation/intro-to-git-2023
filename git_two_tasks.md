# Git Branching & Issue Resolution

## Branches

In this task we'll experiment with branches!

> :computer:
>
> 1. Check the names of current branches.
> 2. Create a new branch called new_feature.
> 3. Move to the new branch and add a file detailing your amazing idea.
> 4. Investigate the diff between new_feature and main
> 5. Merge the changes made in new_feature to the main branch.
> 6. Remove the branch you've created.
>

<details>
  <summary>Click here to show solution</summary>
  
  ```console
1.

  git branch

2.

  git branch new_feature

3.

  move branches: git checkout new_feature
  add a file: touch feature.txt
  # add some content to file, an example used below
  echo "This project removes posts around ChatGPT from LinkedIn!"
  git add .
  git commit -am "My amazing feature"

4.

  move branches: git checkout main
  check diff: git diff new_feature

5.
  git checkout main
  git merge new_feature

6.
  git branch -d new_feature

  ```

</details>
<br>

## Issue Resolution #1

In this task we'll experiment with commits and checking difference between files in our working directory and repository.

> :computer:
>
> 1. Create a two keys (public/private) and add both to index
> 2. Reset change, create .gitignore file which ignores files starting with private
> 3. Re-add all files within directory
> 4. Check status and if only public.key is tracked commit the changes.

>
>> Optional: Make a second update then check the diff using difftool: <br>
>>
>> ```console
>> git config --global difftool.vscode.cmd 'code --wait --diff $LOCAL $REMOTE'
>> git difftool
>> ```

<details>
  <summary>Click here to show solution</summary>
  
  ```console
1.

  touch public.key private.key
  git add .
2.

  git reset HEAD
  echo ’private.key’ >> .gitignore

3. 
  git add .

4.

  git status
  git commit –m “Adding the public key”

  ```

</details>

## Issue Resolution #2

In this task we've accidently deleted the public key from the previous task and need to reset the working directory to reflect the HEAD.

> :computer:
>
> 1. Delete the public key.
> 2. Reset the state of the working directory
> 3. Check the status and any implications on the commit history.
>

<details>
  <summary>Click here to show solution</summary>
  
  ```console
1.

  rm public.key

2.

  git reset --hard HEAD
  ```

</details>

## Issue Resolution #3

In this task we've made a mess of our directory and need to clean it up.

> :computer:
>
> 1. Add a few untracked files/folders (1 of each is fine)
> 2. Dry run a removal of files only and then both files/folders
> 3. Remove just the files and check status
>

<details>
  <summary>Click here to show solution</summary>
  
  ```console
1.

  touch 1.txt 2.txt
  mkdir 1f

2.

  git clean -n
  git clean -dn

3. 
  git clean -f
  git status

  ```

</details>

## Closure

Congrats on reaching the end of this short workshop, if you're done before the time is up grab a coffee, download VS Code or play around with creating your own github repository. Once you've done all of that complete the following:

* Raise your left hand
* Move it over your right shoulder
* Give yourself a nice pat on the back
* Have a great day.


<div align="right">

   [Prev](git_one_tasks.md) - Next
</div>
