# Mercurial Queues

Please refer to [Mercurial Queues][mdn-mercurial-queues] on MDN.

## Commands
* New a patch file: `hg patch-name.patch`
* Export patch file: `hg export > ~/path/to/patch-name.patch`
* Import patch file: `hg qimport ~/path/to/patch-name.patch`
* Check the queues: `hg qseries -s -v`

[mdn-mercurial-queues]: https://developer.mozilla.org/en-US/docs/Mozilla/Mercurial/Queues
