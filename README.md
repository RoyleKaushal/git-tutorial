1. git stash -> for stash 

2. git stash list -> 
        stash@{0}: WIP on Day3: 2ac0a4d First commit

3. git stash apply -> It is used for revert last stash and persist that stash in stash stack.

4. git stash show stash@{0} -> It shows particular stash which is mentioned.

5. git stash apply stash@{1} -> It revert particular stash from stash list which is mentioned.

6. git stash --include-untracked -> It stash untracked file also 

7. git stash --all -> It stash all files.

8. git stash pop -> It pop and revert the last stash.

9. git stash drop -> It deletes the last stash

10. git stash drop stash@{0} -> It deletes the particular stash 

11. git stash clear -> It delete complete stack of stash.