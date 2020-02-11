# DA Section Hands-On Meeting
January 31, 2020


## Git Use for ProdGSI
Guoqing Ge


- Use submodules to manage fix/ and libsrc/. These are both separate Git repos.
  - Need to use --recursive flag with git clone to get the contents of the submodules.
  - May not want to grab the fix submodule, you don’t have to use the --recursive flag.
- Our code in GSD is in a branch gsd/develop
- Safer to use git fetch than git pull.
  - A  `git pull` is the same as `fetch + merge`.
- Submodules will not be updated automatically with a fetch/pull, or with change of branch. 
  - Use git submodule update [fix | update].
- We may need more information about how to contribute back to the submodule repositories.
- gsd/develop is synced with master a few times a year. This is mainly for RAP/HRRR development.  We will need an ongoing discussion about doing development of GSI for FV3.
- In general, it’s good to use `git status` often to ensure that you are committing only the files you intend to. Don’t commit large files.
- Work in a branch! Push your branch to the remote as a safe way to back up the code.
- To save off changes, use `git stash` to save, then to put them back `git stash pop`
- Use `--soft` with `git reset` to keep the changes that you committed by accident, but uncommit them.
- See diffs between branches: `git diff <branch> --- <path/to/file>`
- In rapid-refresh, the copy of GSI is not used.


## Future topics:
- Forking
- Pull Requests
- FV3 Repos
- JEDI 

