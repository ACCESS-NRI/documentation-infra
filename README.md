# Documentation infrastructure
This repo contains the reusable infrastructure and templates for the documentation websites curated and deployed by ACCESS-NRI.

The instructions below will help you set up a documentation repository and webite built using [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/reference/) and hosted through [ReadTheDocs](https://docs.readthedocs.com/platform/stable/) (RTD).

## Set up a documentation repository
The [templates](https://github.com/ACCESS-NRI/documentation-infra/blob/main/templates) folder contains files needed to set up a documentation repository for ACCESS-NRI. 
They are organised into directories that mirror their intended location in the target repository.

To set up a documentation repository:

1. Clone this repository<br>
    ```
    git clone git@github.com:ACCESS-NRI/documentation-infra.git
    ```

2. Copy the `templates` filetree into your documentation repository root<br>
    ```
    cp -r templates/. <your-repository-path>
    ```
    This will copy all files/folders within `templates` (including dot files and folders) into your documentation repository, with the correct structure.

3. Modify the files<br>
    The copied files have commented lines starting with `# MODIFY`. This indicates that those lines might need to be edited based on the specifics of your documentation repository/website.

## Set up a ReadTheDocs Project

To set up a new RTD project for an ACCESS-NRI repository:

1. Open an issue in this repository requesting a new RTD project, including:
   - The GitHub repository URL
   - The intended project name/slug on RTD
   - The RTD usernames (or emails) for the intended maintainers
   - The custom URL for the website (if required)
2. The documentation team will create the RTD project with the proper settings and GitHub integration configured.
3. Once the project is created, the documentation team will grant **Maintainer** permissions to the nominated individuals along with `access-nri`.
4. Each maintainer should verify their access by logging into their personal RTD account and confirming the project appears in their dashboard.

### RTD Projects Management

- Every RTD project must have **at least two individual maintainers** in addition to the `access-nri` organisation account.
This ensures continuity of access and avoids single points of failure when team members change roles or leave.

- RTD projects must be maintained through **individual personal RTD accounts**, not the `access-nri` one.
This ensures each maintainer has access only to the projects they are responsible for. 

- Each maintainer should [log in](https://app.readthedocs.org/accounts/login/) to their personal RTD account using GitHub via the **GitHub App** integration (the legacy GitHub OAuth method is no longer supported and should not be used).

- The `access-nri` account must always be included as a maintainer alongside the individual maintainers.

- It is the maintainers' responsibility to keep the maintainers list up to date whenever team membership changes.


## Need help?
Feel free to ask any questions in the hive-docs-team Zulip channel. For bigger or more complex questions/suggestions, open a new issue in this repository.