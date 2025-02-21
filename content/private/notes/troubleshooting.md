---
title: "Troubleshooting and FAQ"
---

## Common Pitfalls
### Some of my pages have 'January 1, 0001' as the last modified date
This is a problem caused by `git` treating files as case-insensitive by default and some of your posts probably have capitalized file names. You can turn this off in your Quartz by running this command.

```shell
# in the root of your Quartz (same folder as config.toml)
git config core.ignorecase true

# or globally (not recommended)
git config --global core.ignorecase true
```

### Can I publish only a subset of my pages?
Yes! Quartz makes selective publishing really easy. Heres a guide on [excluding pages from being published](private/notes/ignore%20notes.md).

### Can I host this myself and not on GitHub Pages?
Yes! All built files can be found under `/public` in the `master` branch. More details under [hosting](private/notes/hosting.md).

### Do I need a website already?
No! Setting up Quartz means you set up a site too :)

### `command not found: hugo-obsidian`
Make sure you set your `GOPATH` correctly! This will allow your terminal to correctly recognize `hugo-obsidian` as an executable.

```shell
# Add the following 2 lines to your ~/.bash_profile
export GOPATH=/Users/$USER/go
export PATH=$GOPATH/bin:$PATH

# In your current terminal, to reload the session
source ~/.bash_profile
```

### How come my notes aren't being rendered?
You probably forgot to include front matter in your Markdown files. You can either setup [obsidian](private/notes/obsidian.md) to do this for you or you need to manually define it. More details in [the 'how to edit' guide](private/notes/editing.md).

### My custom domain isn't working!
Walk through the steps in [the hosting guide](private/notes/hosting.md) again. Make sure you wait 30 min to 1 hour for changes to take effect.

### How do I setup Google Analytics?
You can edit it in `config.toml` and either use a V3 (UA-) or V4 (G-) tag.

### How do I change the content on the home page?
To edit the main home page, open `/content/_index.md`.

### How do I change the colours?
You can change the theme by editing `assets/custom.scss`. More details on customization and themeing can be found in the [customization guide](private/notes/config.md).

### How do I add images?
You can put images anywhere in the `/content` folder. The only caveat is that you should reference them in your Markdown by prefixing it with a `/`.

```markdown
Example image (source is in content/notes/images/example.png)
![Example Image](/content/notes/images/example.png)
```

### My Interactive Graph and Backlinks aren't up to date
By default, the `linkIndex.yaml` (which Quartz needs to generate the Interactive Graph and Backlinks) are not regenerated locally. To set that up, see the guide on [local editing](private/notes/editing.md)

### Can I use React/Vue/some other framework?
Not out of the box. You could probably make it work by editing `/layouts/_default/single.html` but that's not what Quartz is designed to work with. 99% of things you are trying to do with those frameworks you can accomplish perfectly fine using just vanilla HTML/CSS/JS.

## Still Stuck?
Quartz isn't perfect! If you're still having troubles, file an issue in the GitHub repo with as much information as you can reasonably provide. Alternatively, you can message me on [Twitter](https://twitter.com/_jzhao) and I'll try to get back to you as soon as I can.

🐛 [Submit an Issue](https://github.com/jackyzha0/quartz/issues)