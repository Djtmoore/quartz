---
title: "Obsidian Vault Integration"
tags:
- setup
---

## Setup
Obsidian is the preferred way to use Quartz. You can either create a new Obsidian Vault or link one that your already have.

### New Vault
If you don't have an existing Vault, [download Obsidian](https://obsidian.md/) and create a new Vault in the `/content` folder that you created and cloned during the [setup](private/notes/setup.md).

### Linking an existing Vault
The easiest way to use an existing Vault is to copy all of our files (directory and hierarchies intact) into the `/content` folder.

## Settings
Great, now that you have your Obsidian linked to your Quartz, let's fix some settings so that they play well.

Under Options > Files and Links, set the New link format to always be Absolute Path in Vault and disabled WikiLinks so Obsidian generates regular Markdown links.

![Obsidian Settings](private/notes/images/obsidian-settings.png)*Obsidian Settings*

## Templates
Inserting front matter everytime you want to create a new Note gets annoying really quickly. Luckily, Obsidian supports templates which makes inserting new content really easily.

**If you decide to overwrite the `/content` folder completely, don't remove the `/content/templates` folder!**

Head over to Options > Core Plugins and enable the Templates plugin. Then go to Options > Hotkeys and set a hotkey for 'Insert Template'. That way, when you create a new note, you can just press the hotkey for a new template and be ready to go!