# Fish Auto-commit for Bitbucket

This is a FISH function that is commited to in parallel to wherever I actually want to commit to.

Here is the function

```
function gitcommit -a param1 param2
    set --local path $PWD
    cd /Users/danielhebdon/Dev/personal/github-commit-dummy
    echo '.' >> commit.txt
    git add .
    git commit -m "commit made"
    git push
    cd $path
    git add $param1
    git commit -m $param2
end
```
