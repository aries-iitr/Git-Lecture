## Section 4.3 Git-tagging

### What is Git-tagging and why is it used?
Tags are references that point to specific points in Git history. Tagging is generally used to capture a point in history 
that is used for a marked version release (i.e. v1.0.1).
![](Screenshot%20(41).png)
In the image, it is seen that a number of commits are done from a particular branch (say, master). If we feel that it is an important 
point in the history of the repo, then we use tags so as to go back and change anything whenever we need.

Now we discuss various steps in git-tagging:

#### 4.3.1 Create tag when you feel right
##### 4.3.1.1 Normal tags
git tag (tagname)                                                                                                                 
  
##### 4.3.1.2 Annotated tags
git tag -a (tagname) -m ('comment')                                                                                  

#### 4.3.2 Show/display tags
* git tag 
* git show (tagname)

#### 4.3.3 Delete tags
##### 4.3.3.1 Deleting a single tag
* git tag -d (tagname)
* git tag --delete (tagname)

##### 4.3.3.2 deleting multiple tags
git tag -d (tagname) (tagname) (tagname) .....

#### 4.3.4 Working remote
##### 4.3.4.1 Pushing from local to remote
* git push origin (tagname)
* git push origin --tags
* git push --tags

##### 4.3.4.2 Deleting tags from remote
* git push origin -d (tagname)
* git push origin --delete (tagname)
* git push origin : (tagname)

##### 4.3.4.2 Deleting mulitple tags from remote
git push origin -d (tagname) (tagname) .....

#### 4.3.5 Branching in tags
We cannot checkout tags in git. But, we can create a separate branch, create tags from there and checkout that branch.

git checkout -b (branch name) (tagname)

#### 4.3.6 Creating a tag from past commits

git tag (tagname) (reference code(only first 7 digits))
