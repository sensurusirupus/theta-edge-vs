![Rubberduck AI Chat](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/asset/rubberduck-header-2.gif)

> #### AI chat in the Visual Studio Code side bar. Rubberduck can [generate code](#generate-code), [edit code](#edit-code), [explain code](#explain-code), [generate tests](#generate-tests), [find bugs](#find-bugs), [diagnose errors](#diagnose-errors), and more. You can even add [your own conversation templates](https://github.com/rubberduck-ai/rubberduck-vscode/blob/main/doc/rubberduck-templates.md).

# Setup

## OpenAI

1. Get an OpenAI API key from [platform.openai.com/account/api-keys](https://platform.openai.com/account/api-keys) (you'll need to sign up for an account)
2. Enter the API key with the `Rubberduck: Enter OpenAI API key` command

## Llama.cpp (experimental)

You can use Rubberduck with local models, e.g. [CodeLlama-7B-Instruct](https://huggingface.co/TheBloke/CodeLlama-7B-Instruct-GGUF) running in [Llama.cpp](https://github.com/ggerganov/llama.cpp) (see [ModelFusion Llama.cpp setup](https://modelfusion.dev/integration/model-provider/llamacpp#setup)). To enable llama.cpp in Rubberduck, set the `Rubberduck: Model` setting to `llama.cpp`.

## Configuration Options

- **rubberduck.syntaxHighlighting.useVisualStudioCodeColors**: Use the Visual Studio Code Theme colors for syntax highlighting in the diff viewer. Might not work with all themes. Default is `false`.

# Features

[AI Chat](#ai-chat) | [Generate Code](#generate-code) | [Edit Code](#edit-code) | [Explain Code](#explain-code) | [Generate Tests](#generate-tests) | [Find Bugs](#find-bugs) | [Diagnose Errors](#diagnose-errors) | [Custom Conversations](#custom-conversations)

## AI Chat

Chat with Rubberduck about your code and software development topics. Rubberduck knows the editor selection at the time of conversation start.

1. You can start a chat using one of the following options:
   1. Run the `Rubberduck: Start Chat 💬` command from the command palette.
   1. Select the `Start Chat 💬` entry in the editor context menu (right-click, requires selection).
   1. Use the "Start new chat" button in the side panel.
   1. Use the keyboard shortcut: `Ctrl + Cmd + C` (Mac) or `Ctrl + Alt + C` (Windows / Linux).
   1. Press 💬 on the MacOS touch bar (if available).
1. Ask a question in the new conversation thread in the Rubberduck sidebar panel.

![AI Chat](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-start-chat.png)

# Generate Code

Instruct Rubberduck to generate code for you.

1. You can start generating code using one of the following options:
   1. Run the `Rubberduck: Generate Code 💬` command from the command palette.
   1. Use the "Generate Code" toolbar button in the side panel.
   1. Use the keyboard shortcut: `Ctrl + Cmd + G` (Mac) or `Ctrl + Alt + G` (Windows / Linux).
2. Describe what you want to generate in the new conversation thread in the Rubberduck sidebar panel. Rubberduck will generate code for you based on your description. Further messages can be used to refine the generated code.

![Generate Code](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-generate-code.gif)

## Edit Code

Change the selected code by instructing Rubberduck to create an edit.

1. Select the code that you want to change in the editor.
1. Invoke the "Edit Code" command using one of the following options:

   1. Run the `Rubberduck: Edit Code 💬` command from the command palette.
   1. Select the `Edit Code 💬` entry in the editor context menu (right-click).
   1. Use the keyboard shortcut: `Ctrl + Cmd + E` (Mac) or `Ctrl + Alt + E` (Windows / Linux).

1. Rubberduck will generate a diff view.
1. Provide additional instructions to Rubberduck in the chat thread.
1. When you are happy with the changes, apply them using the "Apply" button in the diff view.

![Edit Code](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-edit-code.gif)

## Explain Code

Ask Rubberduck to explain the selected code.

1. Select the code that you want to have explained in the editor.
1. Invoke the "Explain Code" command using one of the following options:
   1. Run the `Rubberduck: Explain Code 💬` command from the command palette.
   1. Select the `Explain Code 💬` entry in the editor context menu (right-click).
1. The explanations shows up in the Rubberduck sidebar panel.

![Explain Code](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-code-explanation.png)

## Generate Unit Test

Generate a unit test for the selected code.

1. Select a piece of code in the editor for which you want to generate a test case.
2. Invoke the "Generate Unit Test" command using one of the following options:
   1. Run the `Rubberduck: Generate Unit Test 💬` command from the command palette.
   1. Select the `Generate Unit Test 💬` entry in the editor context menu (right-click).
3. The test case shows up in a new editor tab. You can refine it in the conversation panel.

![Generate Test](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-generate-test.gif)

## Find Bugs

Identify potential defects in your code.

1. Select a piece of code that you want to check for bugs.
2. Invoke the "Find Bugs" command using one of the following options:
   1. Run the `Rubberduck: Find Bugs 💬` command from the command palette.
   1. Select the `Find Bugs 💬` entry in the editor context menu (right-click).
3. Rubberduck will show you a list of potential bugs in the chat window. You can refine it in the conversation panel.

![Find Bugs](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-find-bugs.png)

## Diagnose Errors

Let Rubberduck identify error causes and suggest fixes to fix compiler and linter errors faster.

1. Select a piece of code in the editor that contains errors.
2. Invoke the "Diagnose Errors" command using one of the following options:
   1. Run the `Rubberduck: Diagnose Errors 💬` command from the command palette.
   1. Select the `Diagnose Errors 💬` entry in the editor context menu (right-click).
3. A potential solution will be shown in the chat window. You can refine it in the conversation panel.

![Diagnose Errors](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/screenshot-diagnose-errors.gif)

# Custom Conversations

What if you want to craft an AI Chat that knows _specifically_ about your conventions?
How cool would it be to have the answers in your own language?

You can craft your own conversation templates by adding `.rdt.md` files to the `.rubberduck/template` folder in your workspace. See the [Rubberduck Template docs](https://github.com/rubberduck-ai/rubberduck-vscode/blob/main/doc/rubberduck-templates.md) for more information.

To use custom conversations, run the "Rubberduck: Start Custom Chat… 💬" command.

Here is an example of a [drunken pirate describing your code](https://github.com/rubberduck-ai/rubberduck-vscode/blob/main/template/fun/drunken-pirate.rdt.md):

![Describe code as a drunken pirate](https://raw.githubusercontent.com/rubberduck-ai/rubberduck-vscode/main/app/vscode/asset/media/drunken-pirate.gif)

[Learn how to craft your own Rubberduck template](https://github.com/rubberduck-ai/rubberduck-vscode/blob/main/doc/rubberduck-templates.md)!

# Tips and Tricks

Understanding these concepts will help you get the most out of Rubberduck.

- **Be specific**.
  When you ask for, e.g., code changes, include concrete names and describe the desired outcome. Avoid vague references.
- **Provide context**.
  You can include the programming language ("in Rust") or other relevant contexts for basic questions.
  You can select a meaningful code snippet for code explanations and error diagnosis.
- **Do not trust answers blindly**.
  It's a big step for a rubber duck to be able to respond to your questions.
  It might respond with inaccurate answers, especially when talking about
  less well-known topics or when the conversation gets too detailed.
- **Use different chat threads for different topics**.
  Shorter threads with specific topics will help Rubberduck respond more accurately.

# Built With

- [ModelFusion](https://modelfusion/dev) - AI library
- [Prism.js](https://prismjs.com/) - Syntax highlighting
- [React](https://reactjs.org/) - UI rendering
