# notebook-share
A template for turning Jupyter notebooks and markdown files into a website.

Steps to use this template:

- Click the **Use this template** green button on this GitHub repo and fill in the details to create a repo under your account.
- Clone the newly created repo to your computer and open it using a Text Editor (e.g., Visual Studio Code).
- Use the Text Editor to search `notebook-share` and replace it with your repo name.
- Add/remove dependencies in `requirements.txt` if need.
- Add folders (e.g., `chapter_01`) and files (e.g., `intro.ipynb`, `index.md`) to the `docs` folder.
- Open `mkdocs.yml` and make several changes, including `site_name`, `site_url`, `repo_url`, and `nav`. If you don't want the notebooks to be executed when building the website, set `execute: False` under `plugins`.
- Customize the issue template (`.github/ISSUE_TEMPLATE/config.yml`) if needed.
- Commit the changes using Git and push changes to GitHub.
- Enable GitHub Pages through GitHub Settings - Pages.
- Check out the website at https://username.github.io/repo-name.


## Build docs locally

https://www.mkdocs.org/getting-started/

We still need requirements.txt for the Github Actions pip installation, but locally we can use with conda+pip

    conda env create -n notebook-share --file requirements.yml
    conda activate notebook-share
    mkdocs serve
    mkdocs gh-deploy

How to update conda env with more packages?

    conda env update --file requirements.yml --prune
