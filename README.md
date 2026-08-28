# aki

**AI agent orchestrator for multi-repo workspaces.**

`aki` lets you dispatch AI coding agents against one or more git repositories,
drive them from the terminal or the web UI, and manage the resulting work as
tasks with isolated git worktrees.

This repository hosts the **public** distribution of the `aki` CLI — released
binaries, installation instructions, and command reference.

## Install

Download the latest binary from the [Releases](https://github.com/sfast/aki-cli/releases) page,
or install via cargo:

```bash
cargo install aki
```

## Getting started

```bash
aki init      # scan the current workspace for git repos, create .aki/
aki login     # sign in (device flow)
aki ui        # open the web UI, authenticated with your login
```

## Commands

| Command   | Description                                                          |
|-----------|---------------------------------------------------------------------|
| `init`    | Initialize aki in the current directory — scan repos, create `.aki/`  |
| `analyze` | Analyze the workspace — detect stacks, routes, generate `workspace.md` |
| `project` | Manage projects (alias: `p`)                                        |
| `task`    | Manage tasks (alias: `t`)                                           |
| `add`     | Add a repo to the current project                                   |
| `remove`  | Remove a repo from the current project                              |
| `select`  | Select a project as current (alias: `sel`)                          |
| `start`   | Start a task — launch an agent session                             |
| `go`      | Attach to a running task in the terminal                           |
| `web`     | Attach a task to the web UI                                        |
| `stop`    | Stop a running task                                                 |
| `ls`      | List tasks                                                          |
| `pls`     | List projects                                                       |
| `diff`    | Show the diff across all repos for a task                          |
| `merge`   | Merge a task's branches into a target branch                       |
| `done`    | Merge a task's branches and mark it done                           |
| `sync`    | Reconcile local tasks with the backend                             |
| `ui`      | Open the aki web UI in your browser                                |
| `status`  | Quick overview of current state                                    |

Run `aki <command> --help` for details on any command.

## License

See [LICENSE](./LICENSE).
