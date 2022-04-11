---
author: Dominic Buehler
title: Custom window title text in VS Code
date: 2022-04-11
series: ["60 second gists"]
tags: 
    - "vs-code"
---

## VS Code - Custom window title

You know for sure the window title in VS Code, i.e. the text at the very top of your VS Code window.  
But did you know that (like most in VS Code) you can modify it such that it suits your working style best?

Just go to the .json settings (MacOS Shortcut: `Cmd + ;`) and add the key-value-pair `"window.title": "<your prefered title>"`

This is my setting: 
```json
"window.title": "${activeEditorLong}"

<-- Original -->
"window.title":"${activeEditorShort}${separator}${rootName}"
```
With this setting, I see the whole absolute filepath. This helps me to distinguish more easily in which project I am in comparison to the original value.  
For a complete list of variables, please see [here](https://code.visualstudio.com/updates/v1_10#_configurable-window-title).

{{% notice tip "Tip" %}}
If you like emojis as much as I do: you can also add emojis to the window title 🤯
{{% /notice %}}



