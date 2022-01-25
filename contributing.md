# Contributing to this repository

## Getting started

Before you begin:

- Setup the environment.
- Check out the [existing issues](https://github.com/Anything-Minecraft-Team/anything-minecraft/issues) and [pull requests](https://github.com/Anything-Minecraft-Team/anything-minecraft/pulls).

### Environment setup

The final page is built using [MkDocs](https://www.mkdocs.org/), a static site generator written in Python. You need to have Python and its package manager Pip installed.

If you're ready, install the dependencies by using this command in the root of this repo:

```bash
pip install -r requirements.txt
```

In addition to MkDocs, we use [Markdownlint](https://github.com/DavidAnson/markdownlint) and [Prettier](https://prettier.io/) to keep our Markdown structured and well formatted. You have to have Node.JS installed in order to use it. VS Code extensions are available for both of these. If you use another editor, you may need to change the formatting options, in order for it to use our configurations.

```bash
# Install dependencies from package.json
npm i
# Run the linting
npm run lint
```

The linting is automatically run before each commit to ensure your Markdown is formatted correctly. Committing will be stopped, if it fails. To temporarily bypass this, use the `--no-verify` argument while committing.

### Using MkDocs

Once you have MkDocs and our dependencies installed, you can start the development server with the following command:

```bash
mkdocs serve
```

You can then open the page by navigating to [http://localhost:8000](http://localhost:8000). The page will automatically reload if you change something. We recommend **not** to use the integrated Markdown preview in your editor, as MkDocs offers a lot of features that are not available in "vanilla" Markdown.

### Getting changes into the repository

#### If you don't have write access

- Fork the repository
- (optional: Make a new branch in the fork)
- Commit changes to the Fork
- Lint your markdown (`npm run lint`)
- Create a pull request (PR)

#### If you have write access (but not on main)

- Create a new branch from main
- Commit changes to the fork
- Lint your markdown (`npm run lint`)
- Create a pull request (PR)

### Submit your PR & get it reviewed

- Once you submit your PR, others from the community will review it with you.
- Your code will also be automatically linted using a GitHub Workflow.
- After that, we may have questions, check back on your PR to keep up with the conversation.

### Folder Conventions

- The [guides folder](docs/server/guides) is for any _guide_ on how to do anything, such as, start a community, setup a server jar or using certain functions of a plugin.
- The [info folder](docs/server/info) is used for listing all commands, permissions, config options of plugins etc and explaining what they do. Not for examples of how to use them.
- The [images folder](docs/images) is for images in guides and other files.

### Tips and other conventions

- Don't use absolute paths for images. MkDocs has problems with them. **Always** use a relative path.
- Check out the [Material MkDocs documentation](https://squidfunk.github.io/mkdocs-material/reference/abbreviations/). Try to use some of the advanced features of it, which are not available in "vanilla" Markdown. Most of the extensions should be enabled.
- Don't use Unicode emojis. Material MkDocs comes bundled with an extensions for emojis and icons. For more information, take a look [here](https://squidfunk.github.io/mkdocs-material/reference/icons-emojis/).

### Your PR is merged

Congratulations! The whole community thanks you. :sparkles:
