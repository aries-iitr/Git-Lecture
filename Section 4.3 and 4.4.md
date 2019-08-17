## Section 4.3 Git-tagging

### What is Git-tagging and why is it used?
Tags are references that point to specific points in Git history. Tagging is generally used to capture a point in history 
that is used for a marked version release (i.e. v1.0.1).

![](images/Screenshot%20(41).png)

In the image, it is seen that a number of commits are done from a particular branch (say, master). If we feel that it is an important 
point in the history of the repo, then we use tags so as to go back and change anything whenever we need.

Now we discuss various steps in git-tagging:

#### 4.3.1 Create tag when you feel right
##### 4.3.1.1 Normal tags

syntax : git tag (tagname)                                                                                                                   
##### 4.3.1.2 Annotated tags
Annotated tags can contain a message, creator, and date different than the commit they point to. So we could use them to describe a release without making a release commit.

syntax : git tag -a (tagname) -m ('comment')     

![](images/Screenshot%20(43).png)

The image shows how to create tags and how to view all the tags together

#### 4.3.2 Show/display tags
* git tag 
* git show (tagname)

![](images/Screenshot%20(44).png)

If any edit is done to any of the file inside the repo, then all the activities get shown up here.

#### 4.3.3 Delete tags
##### 4.3.3.1 Deleting a single tag
* git tag -d (tagname)
* git tag --delete (tagname)

![](images/Screenshot%20(45).png)

##### 4.3.3.2 deleting multiple tags
git tag -d (tagname) (tagname) (tagname) .....

#### 4.3.4 Working remote
Typically, we work in teams and need to work on a codebase together.  The codebase is on a “central” server and people retrieve files from it and commit to it.

Git refers to the centralized server as a “remote repository”.  The remote repo is usually not on your machine and is the one shared by the team. The team “pushes” commits to it when ready to share with the team.

##### 4.3.4.1 Pushing from local to remote
* git push origin (tagname)

![](images/Screenshot%20(52)%20-%20Copy.png)

![](images/Screenshot%20(47).png)

There was no release earlier. But now there is one on the remote repo.

![](images/Screenshot%20(48).png)

This shows the added tag

* git push origin --tags
* git push --tags

To push all the tags together we use this

![](images/Screenshot%20(52).png)

![](images/Screenshot%20(49).png)

##### 4.3.4.2 Deleting tags from remote
* git push origin -d (tagname)
* git push origin --delete (tagname)
* git push origin : (tagname)

![](images/Screenshot%20(53)%20-%20Copy%20-%20Copy.png)

![](images/Screenshot%20(50).png)

The tag is now deleted

##### 4.3.4.2 Deleting mulitple tags from remote
git push origin -d (tagname) (tagname) .....

![](images/Screenshot%20(53)%20-%20Copy.png)

![](images/Screenshot%20(51).png)

Multiple tags are deleted altogether

#### 4.3.5 Branching in tags

We cannot checkout tags in git. But, we can create a separate branch, create tags from there and checkout that branch.

git checkout -b (branch name) (tagname)

![](images/Screenshot%20(53)%20-%20Copy.png)

#### 4.3.6 Creating a tag from past commits

git tag (tagname) (reference code(only first 7 digits))

![](images/Screenshot%20(54).png)

The new tag created can be seen here
