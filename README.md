![Rubberduck AI Chat](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/asset/rubberduck-header-2.gif)

# Rubberduck: ChatGPT for Visual Studio Code

> &nbsp;
>
> #### AI chat in the Visual Studio Code side bar. Rubberduck can [generate code](#generate-code), [edit code](#edit-code), [explain code](#explain-code), [generate tests](#generate-tests), [find bugs](#find-bugs), [diagnose errors](#diagnose-errors), and more. You can even add [your own conversation templates](#custom-conversations).
>
> &nbsp;

<!-- prettier-ignore-start -->
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Twitter](https://img.shields.io/twitter/url/https/twitter.com/rubberduckai.svg?style=social&label=%20%40rubberduckai)](https://twitter.com/rubberduckai)
[![Discord](https://discordapp.com/api/guilds/1061938502327091271/widget.png?style=shield)](https://discord.gg/8KN2HmyZmn)<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-19-orange.svg?style=flat-square)](#contributors)
<!-- ALL-CONTRIBUTORS-BADGE:END --> 

<!-- prettier-ignore-end -->

## Quick Install

You can install Rubberduck from the

- [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=Rubberduck.rubberduck-vscode)
- [Open VSX Registry](https://open-vsx.org/extension/Rubberduck/rubberduck-vscode)

Rubberduck requires an OpenAI API key. You can get an OpenAI API key from [platform.openai.com/account/api-keys](https://platform.openai.com/account/api-keys) (you'll need to sign up for an account).

## Features

[AI Chat](#ai-chat) | [Generate Code](#generate-code) | [Edit Code](#edit-code) | [Explain Code](#explain-code) | [Generate Tests](#generate-tests) | [Find Bugs](#find-bugs) | [Diagnose Errors](#diagnose-errors) | [Custom Conversations](#custom-conversations)

### AI Chat

Chat with Rubberduck about your code and software development topics. Rubberduck knows the editor selection at the time of conversation start.

![Chat](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-start-chat.png)

# Generate Code

Instruct Rubberduck to generate code for you.

![Generate Code](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-generate-code.gif)

## Edit Code

Change the selected code by instructing Rubberduck to create an edit.

![Edit Code](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-edit-code.gif)

### Explain Code

Ask Rubberduck to explain the selected code.

![Explain Code](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-code-explanation.png)

### Generate Tests

Generate test cases for the selected code.

![Generate Tests](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-generate-test.gif)

## Find Bugs

Find potential defects in your code.

![Find Bugs](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-find-bugs.png)

### Diagnose Errors

Let Rubberduck identify error causes and suggest fixes to fix compiler and linter errors faster.

![Diagnose Errors](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-diagnose-errors.gif)

### Custom Conversations

You can define your own conversation templates. See the [Rubberduck Template docs](https://github.com/rubberduck-ai/rubberduck-vscode/blob/main/doc/rubberduck-templates.md) for more information.

Here is an example of a [drunken pirate describing your code](https://github.com/rubberduck-ai/rubberduck-vscode/blob/main/template/fun/drunken-pirate.rdt.md):

![Describe code as a drunken pirate](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/drunken-pirate.gif)

## Configuration Options

- **rubberduck.syntaxHighlighting.useVisualStudioCodeColors**: Use the Visual Studio Code Theme colors for syntax highlighting in the diff viewer. Might not work with all themes. Default is `false`.

## Built With

- [ModelFusion](https://modelfusion/dev) - AI library
- [Prism.js](https://prismjs.com/) - Syntax highlighting
- [React](https://reactjs.org/) - UI rendering

<!-- ALL-CONTRIBUTORS-LIST:END -->

## Running it locally & Contributing
