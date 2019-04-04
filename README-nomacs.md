# OpenCV for nomacs

## Update upstream
Checkout master & update
```console
$ git checkout master
$ git fetch upstream
$ git merge upstream/master
```
### Merge conflicts
If you run into merge conflicts, fix them and:
```console
$ git commit -a
```

## Create a local branch with the last stable
List all tags
```console
$ git tag
3.4.4
3.4.5
4.0.0
4.0.0-alpha
4.0.0-beta
4.0.0-openvino
4.0.0-rc
4.0.1
4.0.1-openvino
carma_release.0.0.1
perf4au
```
choose the lates stable (i.e. `4.0.1`):
```console
git checkout -b 4.0.1 4.0.1
```

## Push branch
Since your branch name exists as tag, you might get this error message:
```console
$ git push --set-upstream origin 4.0.1
error: src refspec 4.0.1 matches more than one.
error: failed to push some refs to 'git@github.com:TUWien/opencv.git'
```