# Mercurial

## Useful Commands
* Pull and update to latest version: `hg pull -u`
* Show log tree: `hg log -G`
* Check the status: `hg status`
* Add new files in a commit: `hg add new-file`
* Commit: `hg commit -m 'Commit message'`
* Create a new branch: `hg branch branch-name`
* List branches: `hg branches`
* Checkout to the branch/version: `hg co branch-name-or-rev`
* Reset to current version: `hg revert -a`
* Go to previous version: `hg strip -r .`
* Apply a commit: `hg graft rev`
* Export patch to a file: `hg export > ~/path/to/patch-name.patch`
* Clean the untracked files: `hg purge`
* Make a (`rev-a`) commit as the parent of b(`rev-b`) commit: `hg rebase -s rev-b -d rev-a`

## Mercurial Queues

Please refer to [Mercurial Queues][mdn-mercurial-queues] on MDN.

### Commands
* New a patch file: `hg patch-name.patch`
* Import patch file: `hg qimport ~/path/to/patch-name.patch`
* Check the queues: `hg qseries -s -v`
* Delete a queue item: `hg qdelete item-name`

[mdn-mercurial-queues]: https://developer.mozilla.org/en-US/docs/Mozilla/Mercurial/Queues
