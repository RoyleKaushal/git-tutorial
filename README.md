1. git stash -> for stash 

2. git stash list -> 
        stash@{0}: WIP on Day3: 2ac0a4d First commit

3. git stash apply -> It is used for revert last stash and persist that stash in stash stack.

4. git stash show stash@{0} -> It shows particular stash which is mentioned.

5. git stash apply stash@{1} -> It revert particular stash from stash list which is mentioned.

6. git stash --include-untracked -> It stash untracked file also 

7. git stash --all -> It stash all files.
