# globalize.now plugin

Localization infrastructure for React, Next.js and Vue apps, usable from your editor or agent.

Connect this plugin and you can run your localization without leaving your workflow: list projects and their target languages, add or remove languages, submit locale files for translation and pull the results back, keep glossaries and per-language style guides consistent, and connect a GitHub repository so translations land in your repo as locale files.

Translations live in your repository, not in a runtime widget.

## What you get

A remote MCP server (`https://api.globalize.now/mcp`) exposing 21 tools:

| Area | Tools |
|---|---|
| Projects | `list_projects`, `get_project`, `create_project`, `set_project_context` |
| Languages | `list_languages`, `add_project_language`, `remove_project_language` |
| Translation | `translate_files`, `get_translation` |
| Glossary | `list_glossary`, `add_glossary_entries`, `delete_glossary_entry` |
| Style guides | `list_style_guides`, `set_style_guide`, `delete_style_guide` |
| GitHub | `list_github_installations`, `start_github_install`, `detect_repository`, `list_repository_branches`, `connect_repository`, `set_repository_patterns` |

Supported file formats: JSON (flat, nested, ARB, Chrome `messages.json`), PO, XLIFF 1.2 and 2.0, YAML, `@wxt-dev/i18n` TOML/JSON5/JSONC, Android XML, iOS `xcstrings`, Markdown and HTML.

## Setup

1. Install the plugin.
2. The first tool call opens a browser window to sign in to globalize.now. Approve access and you're connected.
3. No API key, no config file. Authentication is OAuth against your own globalize.now account.

A globalize.now account is required ([sign up free](https://app.globalize.now/sign-up)). Translation jobs consume account credits.

## Example prompts

- "Show my globalize.now projects and their target languages"
- "Add Japanese to my storefront project"
- "Translate these locale files into German and French and show me the result"
- "Add a glossary entry so 'Pro Plan' is never translated"
- "Connect my GitHub repo and use locales/{locale}/{namespace}.json as the path pattern"

## Scope

This plugin manages localization projects and translation. Converting hardcoded strings in your source code into i18n keys is done by the globalize.now app or the setup skills — see the [developer docs](https://globalize.now/en/developers/).

## Links

- Website: https://globalize.now/en/developers/
- Documentation: https://help.globalize.now
- Privacy: https://globalize.now/en/privacy/
- Terms: https://globalize.now/en/terms/
- Support: support@globalize.now

## License

MIT
