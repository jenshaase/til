# Wrap Markdown lines after 80 chars

For me it is easier to edit markdown documents if the lines warp after around 80 characters. This can be configured in VS Code with the following settings.

```json
{
    // ... other settings
    "[markdown]":{
        "editor.wordWrap": "wordWrapColumn",
        "editor.wordWrapColumn": 80,
    },
}
```