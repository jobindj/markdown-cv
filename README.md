# markdown-cv

A curriculum vitae maintained in plain text and rendered to HTML and PDF using CSS. 

See the `index.md` file build as resume page [here](https://jobindj.github.io/markdown-cv/)

> This is a fork of the markdown-cv repo with additional automation with github actions to deploy your CV using github pages. For more details, see the [original project page](http://elipapa.github.io/markdown-cv), or the blog post on [switching to markdown for CV](http://elipapa.github.io/blog/why-i-switched-to-markdown-for-my-cv.html).

## Step 1: Clone this Repo using [Template](https://github.com/jobindj/markdown-cv/generate)


## Step 2: Setup Repo Permissions (for Github Actions)

[Source: [GitHub Actions | Jekyll](https://jekyllrb.com/docs/continuous-integration/github-actions/#providing-permissions)]

The action needs permissions to push to your `gh-pages` branch. So you need to create a GitHub **authentication token** on your GitHub profile, then set it as an environment variable in your build using _Secrets_:

1.  On your GitHub profile, under **Developer Settings**, go to the [Personal Access Tokens](https://github.com/settings/tokens) section.
2.  **Create** a token. Give it a name like “GitHub Actions” and ensure it has permissions to `public_repos` (or the entire `repo` scope for private repository) — necessary for the action to commit to the `gh-pages` branch.
3.  **Copy** the token value.
4.  Go to your repository’s **Settings** and then the **Secrets** tab.
5.  **Create** a token named `ACTIONS_TOKEN` (_important_). Give it a value using the value copied above.




***

## Step 3: Make it your CV

Edit the `index.md` file 

- Either [directly in Github](https://help.github.com/articles/editing-files-in-your-repository/)

![](https://help.github.com/assets/images/help/repository/edit-file-edit-button.png)

adding your skills, jobs and education.

![](https://help.github.com/assets/images/help/repository/edit-readme-light.png)

- Or clone the repo!

## Distribution

To transform your plain text CV into a beautiful and shareable HTML page, you have two options:

### I. Use Github Pages to publish it online

1. Delete the existing `gh-pages` branch from your fork. It will only contain this webpage. You can either use git or [the Github web interface](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/#deleting-a-branch).
2. Create a new branch called `gh-pages`.
3. Head to *yourusername*.github.io/markdown-cv to see your CV live.

Any change you want to make to your CV from then on would have to be done on the `gh-pages` branch and will be immediately rendered by Github Pages.

### II. Build it locally and print a PDF

1. To [install jekyll](https://jekyllrb.com/docs/installation/), run `gem install bundler jekyll` from the command line.
3. [Clone](https://help.github.com/en/articles/cloning-a-repository) your fork of markdown-cv to your local machine.
3. Type `jekyll serve` to render your CV at http://localhost:4000.
4. You can edit the `index.md` file and see the changes live in your browser.
5. To print a PDF, press <kbd>⌘</kbd> + <kbd>p</kbd>. Print and web CSS media queries should take care of the styling.

## Styling

The included CSS will render your CV in two styles:
s
1. `kjhealy` the original default, inspired by [kjhealy's vita
template](https://github.com/kjhealy/kjh-vita).
2. `davewhipp` is a tweaked version of `kjhealy`, with bigger fonts and dates
  right aligned.

To change the default style, simply change the variable in the
`_config.yml` file.

Any other styling is possible. More CSS style contributions and forks are welcome!

### Repo Authors

- Eliseo Papa ([Twitter](http://twitter.com/elipapa)/[Github](http://github.com/elipapa)/[Website](https://elipapa.github.io)).

![Eliseo Papa](https://s.gravatar.com/avatar/eae1f0c01afda2bed9ce9cb88f6873f6?s=100)

- Jobin John (added Github Actions)

### License

[MIT License](https://github.com/elipapa/markdown-cv/blob/master/LICENSE)
