# Dev Tools

## Refactor with React
Please refer to [Dev Tools Study Group][dev-tools-study-group].

### Refactor Inspector Panel
We can append our new React panel in the below [code][addexistingtab-function]
```
// For XUL panel.
addExistingTab: function (id, title, selected) {
  this._tabbar.addTab(id, title, selected, this.InspectorTabPanel);
  this.emit("new-tab-registered", id);
},

// For React panel.
addTab: function (id, title, selected, panel) {
  this._tabbar.addTab(id, title, selected, panel);
  this.emit("new-tab-registered", id);
},
```

## about:config
* `devtools.webconsole.new-frontend-enabled` for enabling REP on web console panel.

[dev-tools-study-group]: https://public.etherpad-mozilla.org/p/dev-tools-study-group
[addexistingtab-function]: https://github.com/mozilla/gecko-dev/blob/a61e84c9f3c99cfa98c05f3460dc1fe01fa7213c/devtools/client/inspector/toolsidebar.js#L92-L96
