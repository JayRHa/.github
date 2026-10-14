# Repository naming conventions

Repository names use lowercase kebab-case: words separated by hyphens, without spaces or underscores.

## Pattern

Use `<domain-or-product>-<purpose>[-<type>]`. Include only the pieces that help distinguish the project.

| Kind | Pattern | Examples |
| --- | --- | --- |
| CLI | `<domain>-<purpose>-cli` | `intune-evidence-cli`, `azure-ops-cli`, `microsoft-graph-cli` |
| Script collection | `<domain>-<purpose>-scripts` | `intune-remediation-scripts`, `intune-custom-compliance-scripts` |
| Tool or application | `<domain-or-product>-<purpose>` | `intune-device-troubleshooter`, `document-manager` |
| Examples and labs | `<platform>-examples` or `<platform>-labs` | `foundry-examples`, `foundry-labs` |
| Book companion | `<subject>-book-code` | `foundry-book-code`, `ai-search-foundry-iq-book-code` |
| Website | `<brand>-website` | Use the brand followed by `-website` |
| Infrastructure | `<scope>-infrastructure` | Use the platform or project followed by `-infrastructure` |

Established product names can stand alone. Avoid generic names such as `Demo` or `Terraform`, and avoid redundant `Tool-` or `Web-` prefixes. Archive and visibility are repository settings, not name prefixes.

## GitHub exceptions

- `JayRHa` is the profile repository and must match the account name.
- `.github` provides shared community files and must keep its special name.
- Forks can keep an already compliant upstream name, such as `azure-ai-docs` and `iq-series`.

## Migration rules

Update README links, clone commands and repository references in workflows and configuration. Keep package names, commands, application IDs and deployed resource names unless a separate migration requires changing them. Check deployment integrations, OIDC subjects, webhooks, hosted actions and local remotes before a rename.

GitHub redirects ordinary repository and Git URLs, but this does not replace checking integrations or updating references. Do not reuse an old repository name for a different project, because doing so removes the redirect.
