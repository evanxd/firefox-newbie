# Mercurial

## Useful Commands
* `git add new-file`: `hg add new-file`
* Commit: `hg commit -m 'Commit message'`
* Create a new branch: `hg branch branch-name`
* List branches: `hg branches`
* Checkout to the branch/version: `hg co branch-name-or-rev`
* `git reset --hard`: `hg revert -a`
* `git reset --hard HEAD~1`: `hg strip -r .`

## Mercurial Queues

Please refer to [Mercurial Queues][mdn-mercurial-queues] on MDN.

### Commands
* New a patch file: `hg patch-name.patch`
* Export patch file: `hg export > ~/path/to/patch-name.patch`
* Import patch file: `hg qimport ~/path/to/patch-name.patch`
* Check the queues: `hg qseries -s -v`

[mdn-mercurial-queues]: https://developer.mozilla.org/en-US/docs/Mozilla/Mercurial/Queues
