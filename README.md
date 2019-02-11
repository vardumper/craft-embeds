# Embeds plugin for Craft CMS 3.x

Allow using Embeds within Redactor. Embeds are referenced Matrix Blocks within the Redactor body.

![Screenshot](resources/img/plugin-logo.png)

## Requirements

This plugin requires Craft CMS 3.0.0-beta.23 or later and the Craft Redactor plugin.

## Installation

To install the plugin, follow these instructions.

1. Open your terminal and go to your Craft project:
    ```
    cd /path/to/project
    ```
2. (As long as this is unreleased) Add the repository to your composer.json:
    ```
    {
        "repositories": [
            {
                "type": "vcs",
                "url":  "git@github.com:fork/embeds.git"
            }
        ]
    }
    ```
3. Then tell Composer to load the plugin:
    ```
    composer require fork/embeds
    ```
4. In the Control Panel, go to Settings → Plugins and click the “Install” button for Embeds. This will also install
Redactor if it wasn't already installed before.

## Embeds Overview

This plugin adds a Redactor plugin which enables editors to set markers between paragraphs in a redactor field. These
markers then work as placeholders for blocks from a matrix field (_embeds_). In the current development phase, this
plugin only supports one redactor field and one matrix field whit the names _embedsCopy_ and _embeds_. The install
migration of the plugin creates these fields automatically and also adds a Redactor configuration file for the copy
field. **Warning**: Renaming the handles of these fields breaks the plugin! The matrix field will be empty. Redactor
will be installed automatically by the install migration of this plugin.

## Configuring Embeds

Currently there are no configuration options.

## Using Embeds

Add the two fields to any of your EntryTypes' FieldLayout and don't forget to add some MatrixBlocks to the embeds field.
When you add an embed marker to the copy text and add blocks to the matrix field, the plugin will show you which embed
will appear at which placeholder.

## Embeds Roadmap

Some things to do, and ideas for potential features:

* Fix the merging of copy and embeds
* Enable using multiple fields via plugin settings
* 

Brought to you by [Fork Unstable Media GmbH](https://fork.de)
