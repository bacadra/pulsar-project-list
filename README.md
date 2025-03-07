# project-list

Easy access and switching between projects with options. The project file is located in the Pulsar configuration files under the name `projects.cson`.

![project-list](https://github.com/asiloisad/pulsar-project-list/raw/master/assets/project-list.png)

![recent-list](https://github.com/asiloisad/pulsar-project-list/raw/master/assets/recent-list.png)

## Installation

To install `project-list` search for [project-list](https://web.pulsar-edit.dev/packages/project-list) in the Install pane of the Pulsar settings or run `ppm install project-list`. Alternatively, you can run `ppm install asiloisad/pulsar-project-list` to install a package directly from the GitHub repository.

## `projects.cson`

You can edit a file by command `project-list:edit` or by manually opening `<config-dir>/projects.cson`. The main file structure consists of a array of objects.

Setting | Type | Description | Default
-|-|-|-
`title` | `string` | Project title used in the project list | *mandatory*
`paths` | `array[string]` | The array of paths to project directories | *mandatory*
`tags` | `array[string]` | The tags help's organize and find projects | `[]`
`scan` | `boolean` | scan paths and add subdir as projects | `false`
`icon` | `string` | custom icon of project e.g. `"icon-star"` | `"icon-file-directory"`
`devMode` | `boolean` | project should open in [Dev Mode](https://pulsar-edit.dev/docs/launch-manual/sections/core-hacking/#running-in-development-mode) | `false`
`safeMode` | `boolean` | project should open in [Safe Mode](https://pulsar-edit.dev/docs/launch-manual/sections/core-hacking/#using-safe-mode) | `false`

Here is an example of `projects.cson`:

```cson
[
  {
    title: "py-bacadra",
    paths: [
      "C:/bacadra/"
    ],
    tags: [
      "bacadra"
    ]
  },
  {
    title: "Projects",
    paths: [
      "C:/Projects/",
      "D:/Projects/"
    ],
    tags: [
      "Projects"
    ],
    scan: true
  },
  {
    title: "Samples",
    paths: [
      "C:/Samples/"
    ],
    tags: [
      "Samples"
    ]
    devMode: true
  }
]
```

## Commands

In `atom-workspace` there are available commands:

- `project-list:toggle`: (default `F10`) opens project list
- `project-list:recent`: (default `Alt-F10`) opens recent projects
- `project-list:update`: update projects list
- `project-list:edit`: open configuration file

In `project-list` there are available shortcuts:

- `project-list:open`: (default `Enter`) opens a new window with selected project
- `project-list:swap`: (default `Alt-Enter`) closes active window and opens a new one with the selected project
- `project-list:append`: (default `Shift-Enter`) appends selected project to active window
- `project-list:paste`: (default `Alt-V`) paste paths into active text-editor
- `project-list:update`: (default `F5`) update projects list

## Configuration

The `Preserve last search` config option is used from the `command-palette` package.

# Contributing

Got ideas to make this package better, found a bug, or want to help add new features? Just drop your thoughts on GitHub — any feedback’s welcome!
