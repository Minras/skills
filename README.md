# Agent Skills

This repository contains reusable AI agent skills for software development and agentic workflows. Skills follow the Agent Skills convention and are organized in individual directories, each containing a `SKILL.md` file.

## Available skills

| Skill | Description | Instructions |
| --- | --- | --- |
| `implement-user-story` | Implement repository user stories from clear acceptance criteria, with clarification and independent review when needed. | [SKILL.md](skills/implement-user-story/SKILL.md) |

## Install as a plugin

These instructions use the public GitHub repository `minras/skills`. The plugin is named `minras-skills`; its skill is named `implement-user-story`.

### OpenAI Codex

Add the marketplace:

```sh
codex plugin marketplace add minras/skills
```

In Codex, open `/plugins`, choose the `Minras Skills` marketplace, and install `minras-skills`. Invoke the `implement-user-story` skill when working on a user story. See the [Codex plugin documentation](https://developers.openai.com/plugins/build/plugins).

### Claude Code

Add the marketplace and install the plugin:

```sh
claude plugin marketplace add minras/skills
claude plugin install minras-skills@minras
```

Invoke the skill as `/minras-skills:implement-user-story`. See the [Claude Code marketplace documentation](https://code.claude.com/docs/en/plugin-marketplaces).

### GitHub Copilot CLI

Add the marketplace and install the plugin:

```sh
copilot plugin marketplace add minras/skills
copilot plugin install minras-skills@minras
```

See the [Copilot CLI plugin reference](https://docs.github.com/en/copilot/reference/copilot-cli-reference/cli-plugin-reference).

### Cursor

For local installation, clone the repository into Cursor's local plugin directory:

```sh
git clone https://github.com/minras/skills ~/.cursor/plugins/local/minras-skills
```

Restart Cursor or run **Developer: Reload Window**, then open **Customize** to find the plugin. Local plugin imports may need to be enabled by a team administrator. Teams and Enterprise administrators can instead import the repository from **Dashboard → Plugins & MCPs → Add Marketplace → Import from Repo**. Public Cursor Marketplace listings require submission and review. See the [Cursor plugin documentation](https://cursor.com/docs/plugins).

## Remove the plugin

Uninstall `minras-skills` from the platform where you installed it. Remove the marketplace registration separately if you no longer want it listed there.

### OpenAI Codex

In `/plugins`, open the installed `minras-skills` plugin and choose **Uninstall**. To remove the marketplace source as well, run:

```sh
codex plugin marketplace remove minras
```

See the [Codex plugin documentation](https://developers.openai.com/plugins/build/plugins).

### Claude Code

Uninstall the plugin, then remove the marketplace if you no longer need it:

```sh
claude plugin uninstall minras-skills@minras
claude plugin marketplace remove minras
```

See the [Claude Code plugin commands](https://code.claude.com/docs/en/plugins/cli-reference).

### GitHub Copilot CLI

Uninstall the plugin, then remove the marketplace if you no longer need it:

```sh
copilot plugin uninstall minras-skills
copilot plugin marketplace remove minras
```

See the [Copilot CLI plugin reference](https://docs.github.com/en/copilot/reference/copilot-cli-reference/cli-plugin-reference).

### Cursor

For a local installation, delete `~/.cursor/plugins/local/minras-skills` and reload Cursor. For a marketplace installation, uninstall the plugin from **Customize** if the marketplace's installation policy allows it. See the [Cursor plugin documentation](https://cursor.com/docs/plugins).

## Version

`0.0.1`

## License

This repository is distributed under the MIT License. See [LICENSE](LICENSE).
