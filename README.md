# quteFF

* Custom userChrome.css that makes Firefox looks as close as possible to Qutebrowser
* This is meant to be used with the [Vimium-ff](https://github.com/philc/vimium/) add-on
* Forked from https://github.com/IanLeCorbeau/hawtbrowser/

## Screenshots

<img width="1800" alt="image" src="https://github.com/user-attachments/assets/5f2e8bfc-2db8-41b7-a655-8b087569edde" />

## Installation

* Clone the repo
* Enable userChrome.css customization:
  * Go to `about:config`
  * Set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`
* Add the CSS file:
  * Go to `about:profiles`
  * Open your Root Directory folder
  * Create a folder named "chrome" if it doesn't exist
  * Create userChrome.css inside and paste the code from above
  * Restart Firefox
* Install the Vimium-ff add-on
* Update the Vimium-ff CSS (optional)
* Apply the urlbar `about:config` changes (optional)

# Firefox URL Bar Customization

You may want to disable Firefox's URL bar enhancements to simplify the UI and prevent rich results appearing. (Optional)

## How to Apply

1. Open Firefox and navigate to `about:config`
2. Accept the warning about modifying advanced preferences
3. Search for each preference name
4. Double-click the preference to modify its value
5. Restart Firefox for changes to take full effect

## Firefox URL bar tweaks

### Disable Rich Results in URL Bar

```css
browser.urlbar.maxRichResults = 0
```

- Prevents the URL bar from showing rich preview cards and expanded results

### Enable Inline Autocomplete

```css
browser.urlbar.autocomplete.inline = true
```

- Enables inline autocompletion as you type in the URL bar


### Matching Vimium-ff CSS

This can be optionally installed to match the theme by adding the .css to within the vimium-ff css options.

```css
/* Link hints */
div > .vimiumHintMarker {
    background: #000000;
    border: 1px solid #B933E1;
    padding: 2px 4px;
    font-size: 12px;
}

div > .vimiumHintMarker span {
    color: #eeeeee;
    font-size: 12px;
    font-family: monospace;
}

div > .vimiumHintMarker > .matchingCharacter {
    color: #B933E1;
}

/* Vomnibar */
#vomnibar {
    background-color: #000000;
    border: 1px solid #B933E1;
    box-shadow: none;
}

#vomnibar input {
    color: #eeeeee;
    font-size: 12px;
    background-color: #000000;
    border: none;
    padding: 4px;
}

#vomnibar ul {
    background-color: #000000;
}

#vomnibar li {
    border-bottom: 1px solid #323232;
    padding: 4px;
}

#vomnibar li .vomnibarTitle {
    color: #eeeeee;
}

#vomnibar li .vomnibarUrl {
    color: #B933E1;
}

#vomnibar li.vomnibarSelected {
    background-color: #323232;
}

/* HUD (Heads-up-display) */
div.vimiumHUD {
    background-color: #000000 !important;
    border: 1px solid #B933E1 !important;
    box-shadow: none !important;
}

div.vimiumHUD .hud-find {
    background: #000000 !important;
    border: 1px solid #B933E1 !important;
}

div.vimiumHUD .vimiumHUDSearchAreaInner {
    color: #eeeeee !important;
    font-family: monospace !important;
    font-size: 12px !important;
    background-color: #000000 !important;
    border: none !important;
}

div.vimiumHUD .vimiumHUDSearchArea {
    background-color: #000000 !important;
    color: #eeeeee !important;
}

div.vimiumHUD input {
    color: #eeeeee !important;
    background-color: #000000 !important;
}

div.vimiumHUD #hud-find-input {
    color: #eeeeee !important;
    background-color: #000000 !important;
}

/* Find Input Box */
.vimiumFindBar {
    background-color: #000000 !important;
    border: 1px solid #B933E1 !important;
    box-shadow: none !important;
}

.vimiumFindBar input {
    background-color: #000000 !important;
    color: #eeeeee !important;
    border: none !important;
    font-size: 12px !important;
}

.vimiumFindBar .no-matches {
    color: #666666 !important;
}

/* Help Dialog */
div#vimiumHelpDialogContainer {
    opacity: 1.0 !important;
    background-color: #000000 !important;
    border: 1px solid #B933E1 !important;
    border-radius: 0 !important;
    width: 840px !important;
    max-width: calc(100% - 100px) !important;
    max-height: calc(100% - 100px) !important;
    margin: 50px auto !important;
    color: #eeeeee !important;
}

div#vimiumHelpDialog {
    background-color: #000000 !important;
    color: #eeeeee !important;
}

div#vimiumHelpDialog a {
    color: #B933E1 !important;
}

div#vimiumHelpDialog td {
    color: #eeeeee !important;
}

div#vimiumHelpDialog th {
    color: #B933E1 !important;
}

/* Generic input styling */
.vimiumReset input {
    background-color: #000000 !important;
    color: #eeeeee !important;
    border: 1px solid #B933E1 !important;
    box-shadow: none !important;
}

.vimiumReset input[type="text"] {
    color: #eeeeee !important;
    background-color: #000000 !important;
    border: none !important;
    font-size: 12px !important;
}

.vimiumReset .no-matches {
    color: #666666 !important;
}
```

  
# quteFF vs hawtbrowser changelog

<details>
<summary>Expand for full changelog</summary>
<br>
A comparison of changes between the original [hawtbrowser](https://github.com/IanLeCorbeau/hawtbrowser) and quteFF CSS.

## Navigation Bar Changes

### Toolbar Height and Positioning
```css
max-height: var(--uc-bottom-toolbar-height) !important;
padding: 0 !important;
margin: 0 !important;
```

### Toolbar Buttons
```css
aspect-ratio: 1 !important;
object-fit: contain !important;
max-height: var(--uc-bottom-toolbar-height) !important;
padding: 0 !important;
margin: 0 1px !important;
```

### Extension Area Styling
```css
.webextension-browser-action {
    filter: grayscale(100%) brightness(0.8) !important;
    padding: 0 !important;
    margin: 0 !important;
    width: 16px !important;
    height: 16px !important;
    aspect-ratio: 1 !important;
}

.webextension-browser-action .toolbarbutton-icon {
    width: 12px !important;
    height: 12px !important;
    padding: 0 !important;
    margin: 0 2px !important;
    aspect-ratio: 1 !important;
    object-fit: contain !important;
}

#unified-extensions-area {
    display: flex !important;
    align-items: center !important;
    height: var(--uc-bottom-toolbar-height) !important;
    gap: 2px !important;
}

#unified-extensions-button .toolbarbutton-icon {
    filter: grayscale(100%) brightness(0.8) !important;
}
```

### Selected Tab Appearance
```css
background-color: #000000 !important;
border: 1px solid #B933E1 !important;
border-bottom: none !important;
```

### URL Bar Modifications
```css
min-height: var(--uc-bottom-toolbar-height) !important;
max-height: var(--uc-bottom-toolbar-height) !important;
margin: 0 !important;
padding: 0 !important;
```

## Technical Improvements

1. Added aspect-ratio properties throughout for better scaling behavior
2. Added object-fit constraints for icons to prevent distortion
3. Improved extension button layout and appearance
4. More consistent use of height variables

## Visual Changes

* Selected tabs now have a purple border (`#B933E1`)
* Selected tabs use pure black background (changed from `#242424`)
* Extensions are grayscaled and slightly dimmed
* More consistent icon sizing and spacing

## Notes

* Core functionality remains the same as hawtbrowser
* Focus on improving scaling, consistency, and extension support
* Maintains compatibility with Firefox's dark theme

</details>
