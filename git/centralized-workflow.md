# Git: Centralized workflow
This workflow uses a central repository as the single point-of-entry for all changes

## Step by step guide
1. Save all work
2. Open source tree
3. Review unstaged files
    * Review diffs and discard errant changes
    * You may be tempted to skip this, but by doing this you'll have smaller commits and less complicated merge conflicts
4. Stage files
    * Only stage files you want Git to track (do no commit temporary files)
5. Local commit
    * Add a commit message describing your changes and commit
    * Now Git "knows" about your changes
6. Pull remote changes
    * This will download remote commits
    * If the same line of code is touched in both your local commit and in the downloaded commits a merge conflict will occur
    * Sometimes the merge conflict will seem nonsensical, remember white characters exist even if you don't see them
7. (*skip if no merge conflict*) Resolve merge conflicts
    * If you have merge conflicts there will be unstaged files again
    * These files will have markers added by Git (see *Example merge conflict*)
    * You must decide whether your code, their code, or a combination of both are correct
    * To do this open the file in a text editor and make the necessary changes
        * This includes deleting "<<<<<<<", "=======", and ">>>>>>>" markers
    * If you get confused (you will), and want to start over click discard > reset all
8. (*skip if no merge conflict*) Staging the merged files will signal to Git you've resolved the merge conflicts
9. (*skip if no merge conflict*) Make a local commit of your merged files
10. Push local changes
    * This will write your changes to the remote server
    * Relax your changes are safe and if anything goes horribly wrong you can fall back to them

## Example merge conflict
    <<<<<<< HEAD
    // This is your local change
    =======
    // This is the downloaded change
    >>>>>>> 4e2b407f501b68f8588aa645acafffa0224b9b78

