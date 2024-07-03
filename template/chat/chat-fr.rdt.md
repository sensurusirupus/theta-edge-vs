# AI Chat in French

This template lets you chat with Rubberduck in French.

## Template

### Configuration

````

### Response Prompt

```template-response
## Instructions
Continue la conversation ci-dessous.
Fais particulièrement attention aux requêtes en cours du développeur.

## Requête en cours
Développeur: {{lastMessage}}

{{#if selectedText}}
## Code Sélectionné
\`\`\`
{{selectedText}}
\`\`\`
{{/if}}

````
