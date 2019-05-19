# Chrome Dev Tools

## Important Takeaways
- Understand the Elements tab, with focus on DOM (HTML), Styles, and Computed panels
- Modify styles dynamically so you can see the effect of small changes to the CSS without having to reload the page

## Notes
- Docs talk about **DOM Nodes** or **nodes**.  For time being, assume that nodes are another way to refer to HTML elements.  Learn more later.
- Get comfortable using Inspect for debugging and experimentation tool.
  - If having issues with Box Model, Inspector is where you will find the info you need to diagnose the issue

# Inspect and Edit Pages and Styles/Overview
https://developers.google.com/web/tools/chrome-devtools/inspect-styles/

## TL;DR
- Inspect and edit on the fly any element in the DOM tree in the **Elements panel**
- View and change the CSS rules applied to any selected element in the Styles pane
- View and edit a selected element's box model in the Computed panel
- View any changes made to your page locally in the Sources panel

### Live-edit a DOM node
- To live-edit a DOM node, double click the selected element and make changes

## Live-edit a Style
- Live-edit property names and values in the **Styles pane**
  - To edit, click on it, make changes, then press Tab or Enter to save change
- All styles are editable except those that are greyed out
- By default, CSS mods are not permanent and changes are lost on reload but you can set up persistent authoring if you want to persist changes between page loads
  - Persistent authoring: https://developers.google.com/web/tools/setup/setup-workflow

## Examine and Edit Box Model Parameters
- Examine and edit box model params using the **Computed pane**



# Inspect and Edit Pages and Styles/Edit the DOM
https://developers.google.com/web/tools/chrome-devtools/inspect-styles/edit-dom

