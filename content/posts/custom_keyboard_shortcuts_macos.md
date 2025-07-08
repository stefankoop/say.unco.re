---
title: "Custom Keyboard Shortcuts on macOS"
date: 2025-02-17T20:19:44+02:00
draft: false
toc: false
images:
tags:
  - macos
  - shortcuts
  - workflow
---

I changed my workflow a bit depending on keyboard shortcuts and different
desktops and found a nifty tool called [Hammerspoon](https://www.hammerspoon.org/)
that allows you to create custom keyboard shortcuts. It's a Lua scripting
language that allows you to write small scripts that can be triggered by
keyboard shortcuts.

Originally found at [Superuser](https://superuser.com/questions/1340264/keyboard-shortcut-to-switch-to-specific-app-in-os-x)

```lua
-- Constants
MODIFIERS = {"cmd"}    -- Modifiers used for app shortcuts

-- App configuration
APPS = {
  {shortcut = "1", name = "Firefox"},
  {shortcut = "2", name = "Alacritty"},
}

-- Bind application shortcuts
for _, app in ipairs(APPS) do
  hs.hotkey.bind(MODIFIERS, app.shortcut, function()
    hs.application.launchOrFocus(app.name)
  end)
end
```

`CMD + 1` will focus on/open Firefox, and `CMD + 2` will focus on/open Alacritty.
