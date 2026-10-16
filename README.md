# hyperlab Claude Code plugins

The plugin marketplace for [hyperlab-sh](https://github.com/hyperlab-sh). This repository is only an index: every plugin lives in, and is versioned with, its own repository.

## Install

```
/plugin marketplace add hyperlab-sh/claude-plugins
/plugin install <plugin>@hyperlab
```

## Adding a plugin

Add an entry to `.claude-plugin/marketplace.json` that points at the plugin's repository, which must carry its own `.claude-plugin/plugin.json` at the root:

```json
{
  "name": "<plugin>",
  "source": { "source": "github", "repo": "hyperlab-sh/<plugin>" },
  "description": "<one line>"
}
```

Entries track the plugin repository's default branch. Add `"ref": "<tag>"` to the source to pin a release.
