# How to Contribute

We'd love to accept your patches and contributions to this project. There are
just a few small guidelines you need to follow.

## Code reviews

All submissions, including submissions by project members, require review.  
We use GitHub pull requests for this purpose.  
Consult [GitHub Help](https://help.github.com/articles/about-pull-requests/) for more information on using pull requests.

## Steps to send a Pull Request
1. Fork this repository to your GitHub account.
2. Clone your fork to your local system using git.
```shell
git clone URLofYourRepository
```
3. Add your changes.
4. Push local changes to your GitHub repository.
```shell
git add --all
git commit -m "Short description of changes in this commit"
git push origin master
```
5. Go to your GitHub repository. You'll see it has your changes and is some commits ahead of the original repository.
6. If it is some commits behind, update your fork:
```shell
git fetch upstream
git checkout master
git merge upstream/master
```
    Push the updated changes to your GitHub repository:
```shell
git push origin master
```
7. Go to your GitHub fork, which is some commits aheads of the original. Press `Compare` to review the changes.
8. Describe the changes you want to push and send a `Pull Request`.
9. Your changes will be added to the original repository once your Pull Request is reviewed and accepted.
