# Basic Git Commands

## Initialisation

> :computer:
>
> 1. Create a new directory.
> 2. Intialise a local git repository and check the status.
>>* Optional: Inspect the .git subdirectory
> 3. Verify username and email is set correctly.


<details>
  <summary>Click here to show solution</summary>
  
  ```console
1.

  Create new Folder: mkdir demo_project
  Validate Status: Git status
2.

Initialise git repository: git init 
check status: git status

3.

Verify user/email is set: git config –list
  ```

</details>

## Adding/Removing Files


> :computer:
>
> 1. Create a new file.
> 2. Add the file to the index and check the summary status ( --short)
> 3. Update file contents and check difference.
> 4. Commit file to main branch.
> 5. Check the log and explore the options to print commits as a single line
> 6. Check the diff after the commit
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

  Create new Folder: touch example.txt
  Validate Status: git status
2.

  Add file: git add example.txt
  Check status: git status --short
3.

  Update file contents: echo “sample text”” >> example.txt
  Check difference: git diff
4.

  Commit file to main: git commit -am "Example Commit"
5.
  git log
  git log --help
  git log --oneline
  ```

   [Prev](README.md) - [Next](git_two_tasks.md)
</div>
