HASHING
   |
Tree Data Structure / Graph

1. git is like key value structure 
        key - hash of the data
        value - data

2. git uses a cryptographic hash function -> SHA1

3. for a given data, it outputs 40 digit hexadecimal number.

4. The hash value is always same for the same data.

5. git compresses the data in a blob and store some meta data about data

6. .git -> objects -> '<hash key>'

7. objects folder

8. cat hashname -> "Blob / Binary data"

9. we are missing file names, directory, etc

10. git are using trees for it.

11. tree -> It contains pointers (using the hashes)
            1. to store blobs
            2. to store trees and meta data
            3. type of pointer (tree, blob)
            4. directory name or file name 
            5. mode

12. `git cat-file -p 0dec2239efc0bbfabe4078f5357705ca93b5475e`

13. commit -> snapshot
      1. author
      2. msg
      3. date

14. pack file compression

15. create same Hash for same file 

16. git gc --> Garbage Collector

17. git verify-pack -v .git/objects/pack.pack_______.pack

`echo 'Hello git' | git hash-object --stdin` -> 0dec2239efc0bbfabe4078f5357705ca93b5475e

`echo 'Hello git' | git hash-object -w --stdin` ->
0dec2239efc0bbfabe4078f5357705ca93b5475e

`0d % cat ec2239efc0bbfabe4078f5357705ca93b5475e` -> xK??OR04`?H???WH?,?5?%   

`git cat-file -p 645fc4ecbd796bc0e61b00e318e1ab50ae425531` -> HASHING
   |
Tree Data Structure / Graph

1. git is like key value structure 
        key - hash of the data
        value - data

2. git uses a cryptographic hash function -> SHA1
3. for a given data, it outputs 40 digit hexadecimal number.
4. The hash value is always same for the same data.
5. git compresses the data in a blob and store some meta data about data%  


`git cat-file -p 645fc4ecbd796bc0e61b00e318e1ab50ae425531` -> 
100644 blob 645fc4ecbd796bc0e61b00e318e1ab50ae425531	README.md


`git verify-pack -v .git/objects/pack/pack-7848ea9825fe28bb60c938bdf3f2294b87880b20.pack` -> 
be634c51f540bb02c6968d5c14829e5928c575e2 commit 215 135 12
a8bdf587ebde8ff968ba767ee77de8e21efb121d blob   1481 605 147
a382805cb9262424ced3bbd0236f20e68579b8c6 blob   21 31 752
57d2a94ffb1c5a7d17a0c0924f869dbd576e5e33 blob   20 30 783
36ee24a03dabf5ef06f7425cf395603573f3a892 tree   37 48 813
645fc4ecbd796bc0e61b00e318e1ab50ae425531 blob   10 21 861 1 a8bdf587ebde8ff968ba767ee77de8e21efb121d
non delta: 5 objects
chain length = 1: 1 object
.git/objects/pack/pack-7848ea9825fe28bb60c938bdf3f2294b87880b20.pack: ok