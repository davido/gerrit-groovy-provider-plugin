Outdated, latest version is:
============================

https://gerrit-review.googlesource.com/#/admin/projects/plugins/scripting/groovy-provider

Gerrit Groovy Provider Plugin
=============================

This plugin provides Groovy runtime environment for Gerrit plugins in Groovy.

To test this series must be applied on top of Gerrit master [1].

To build link this directory under Gerrit's tree plugins directory and run:

```
  buck build plugins/groovy-provider
```

The result artifact can be found under:

```
 buck-out/gen/plugins/groovy-provider/groovy-provider.jar 
```

To test deploy the review plugin [2] and copy this Groovy Provider plugin
under `$gerrit_site/plugins` directory.

Review plugin in Groovy can be used: 

```
  ssh gerrit review approve I59302cbb
  Approve change: I59302cbb
```

* [1] https://gerrit-review.googlesource.com/#/q/status:open+project:gerrit+branch:master+topic:plugin-dependencies
* [2] https://github.com/davido/gerrit-groovy-plugin
