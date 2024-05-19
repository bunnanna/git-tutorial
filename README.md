# git-tutorial

## Agenda

1. Why git
2. clone project
3. branch
4. add + commit
5. secret + .gitignore
6. local vs remote
7. mr
8. stash
9. reset vs revert

## Recommend

Select one of following

1. Git Graph (VSCode Extension)
1. Source Tree (Git Software)

## Why git

To let a little change be one of development version

## Clone

To get folder from remote(Gitlab) to local(PC)

repository = main folder of project

* with git command (```git clone https://foobar.git```)
* with gitlab
   1. click ```Code``` button
   2. select VSCode (HTTPS)
   3. select folder where to place

## Branch

When we want to add new idea or fix something. We must create new branch, so that we can do it without affect main branch. Then we can merge changes to main branch after it works.(A branch should have only one maintainer to avoid conflict)

### VSCode

1. click on bottom left of screen
2. type branch name

if there is existed, branch will be changed to that branch
if not, new branch will be created and checkout to that branch

checkout = switch branch

## add + commit

### Add

Add to stageing area (pending confirm)

A part of changed file can be add, instead of whole file with stage seleted area.

The change that dont want to add to staging area can be discard to be previous version.

### Commit

Confirm changed in staging area And add to development history.

The commit must be send with message

## .gitignore

to prevent secret file to appear in public.

## local vs remote

* local = Our PC
* remote = Gitlab

What we change in local affect only in local.

* To make remote *update* the change in local. we should *push* local to remote
* To make local *know* the change in remote. we should *fetch* remote to local
* To make local *update* the change in remote. we should *pull* remote to local

## MR

The action when we want to apply change in current branch to target branch (main branch)

mr must be applied only when merge to protected branch.

### Step

1. merge target branch to current branch(To make sure that will not have conflict)
2. push current branch to remote
3. open mr from current remote branch to target branch
4. assign to reviewer and wait for review
5. if something need to be fixed, you can commit at local and push again(no need mr again)
6. if passed reviewer will merge the change to target branch

## Stash

when you want to save the change but dont want to commit you can *stash* change from staging area without commit. that change will be saved somewhere, then you can apply that change anytime you want.

## reset vs revert

the following command is used to rollback the commited change

* reset = you didnt do that commit and the following commit before. delete it
  * Hard = completely clear the commit
  * Soft = put all change in the staging area so you can recommit.
* revert = you do it in opposite direction to undo it
