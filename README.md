# subtree-test-parent
Testing git subtrees (parent)

### How it's done

Reference links:
- http://rogerdudler.github.io/git-guide/
- https://medium.com/@v/git-subtrees-a-tutorial-6ff568381844

1. Open parent repo in GitHub Desktop and go to Repository->Open in Terminal
2. Add subtree:

  git remote add my-subtree git@github.com:microbit-rosslowe/my-subproject.git
  git subtree add —-prefix=(DIR)/ my-subtree master

Replace 'master' with a branch and '(DIR)' with directory in which subtree content will go.

3. When changes are made in the subtree you need to periodically pull these:

   git subtree pull -—prefix=(DIR) my-subtree master
 
You'll enter [Vi](https://stackoverflow.blog/2017/05/23/stack-overflow-helping-one-million-developers-exit-vim/) and be asked to write a commit message. Write a message then press ctrl-c, type :, then in the field at the bottom type x to exit.

Use GitHub Desktop again to push.
