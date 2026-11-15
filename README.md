# shellbent

Coding agents using open-weight LLMs seem to be (s)hellbent on using shell commands for searching and reading code instead of named tools. This is the repo we use for the experiments in my master's thesis at TU Wien.

It adds named tools and model classes to [mini-swe-agent](https://github.com/SWE-agent/mini-swe-agent) 2.4.6, without forking it. Each configuration is a config file plus a model class, listed in [CONFIGURATIONS.md](CONFIGURATIONS.md).

## Usage

With Pier, pinned to a commit:

```
--ak 'extra_python_packages=["git+https://github.com/alexander-posztos/shellbent.git@<sha>"]'
--ak config_file=tools.yaml --ak model_class=thesis_tools.model.ToolsModel
```

## Tools

`search` and `read` are Python ports of [pi](https://github.com/earendil-works/pi)'s grep and read tools. They run in the task container as shell commands, so trajectories look the same as in stock mini-swe-agent.

## License

MIT
