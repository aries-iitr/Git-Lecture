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
e.g., git tag v1.0
  
##### 4.3.1.2 Annotated tags
git tag -a (tagname)
e.g., git tag -a v1.1

#### 4.3.2 Show/display tags
* git tag 
* git show (tagname)
