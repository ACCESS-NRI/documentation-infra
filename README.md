# Documentation infrastructure
This repo contains the reusable infrastructure for the documentation websites curated and deployed by ACCESS-NRI.

## Templates
The [templates](https://github.com/ACCESS-NRI/documentation-infra/blob/main/templates) folder contains templates used for documentation websites, to be copied into their repositories following the instructions at the beginning of each template file.

They are organised into directories that mirror their intended location in the target repository, so the `templates` directory can be treated as the target repository root.
For example, `templates/.readthedocs.yaml` should be copied to `.readthedocs.yaml` in the target repository, while `templates/.github/workflows/check_links.yml` should be copied to `.github/workflows/check_links.yml`.

## ReadTheDocs Project Management

This section outlines how Read the Docs (RTD) projects are managed across ACCESS-NRI.

### Maintainer Requirements

Every RTD project must have **at least two individual maintainers** in addition to the `access-nri` organisation account.
This ensures continuity of access and avoids single points of failure when team members change roles or leave.

- Maintainers must be listed explicitly on the RTD project's **Maintainers** settings page.
- The `access-nri` account must always be included as a maintainer alongside the individual maintainers.
- It is the maintainers' responsibility to keep the maintainers list up to date whenever team membership changes.

### Personal RTD Accounts

RTD projects must be maintained through **individual personal RTD accounts**, not the `access-nri` one.
This ensures each maintainer has access only to the projects they are responsible for, thus improving security.

Each maintainer should connect their personal RTD account to their GitHub account so that repository integrations run smoothly.
This connection must be made via the **GitHub App** integration (the legacy GitHub OAuth method is no longer supported and should not be used).

### Setting Up a New RTD Project

To set up a new RTD project for an ACCESS-NRI repository:

1. Open an issue in this repository requesting a new RTD project, including:
   - The GitHub repository URL
   - The intended project name/slug on RTD
   - The RTD usernames (or emails) intended maintainers
   - The custom URL for the website (if required)
2. The documentation team will create the RTD project with the proper settings and GitHub integration configured.
3. Once the project is created, the documentation team will grant **Maintainer** permissions to the nominated individuals.
4. Each maintainer should verify their access by logging into their personal RTD account and confirming the project appears in their dashboard.