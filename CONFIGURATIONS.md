# Configurations

| Config file | Model class | The agent gets |
|---|---|---|
| `bash.yaml` | `BashModel` | bash, default mini-swe-agent prompt (baseline) |
| `tools.yaml` | `ToolsModel` | bash + search, default prompt |
| `minimal.yaml` | either | bash (+ search), short prompt that names no tool |
| `minimal-directive.yaml` | `ToolsModel` | as minimal, the search description says to use it instead of grep |
| `minimal-reason.yaml` | either | as minimal, every call states why this tool and why not the others |
| `minimal-reason-nogrep.yaml` | `ToolsModel` | as reason, grep and rg refused in bash |
| `minimal-reason-read.yaml` | `ToolsModel` | bash + read, with reasons |
| `minimal-reason-read-nocat.yaml` | `ToolsModel` | as reason-read, cat, head, nl and sed -n refused in bash |
| `minimal-search-read.yaml` | `ToolsModel` | bash + search + read, short prompt |

Each yaml says what it changes and why in its header comment. `thesis_tools/model.py` documents the reason fields, the blocking and the rate-limit keys.
