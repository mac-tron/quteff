# quteFF

* Custom userChrome.css that makes Firefox looks as close as possible to Qutebrowser
* This is meant to be used with the [Vimium-ff](https://github.com/philc/vimium/) add-on
* Forked from https://github.com/IanLeCorbeau/hawtbrowser/

## Screenshots

<img width="1800" alt="image" src="https://github.com/user-attachments/assets/5f2e8bfc-2db8-41b7-a655-8b087569edde" />

## Usage

* Clone the repo
* Enable userChrome.css customization:
  * Go to about:config
  * Set toolkit.legacyUserProfileCustomizations.stylesheets to true
* Add the CSS file:
  * Go to about:profiles
  * Open your Root Directory folder
  * Create a folder named "chrome" if it doesn't exist
  * Create userChrome.css inside and paste the code from above
  * Restart Firefox
* Install the Vimium-ff add-on

<details>
<summary># quteFF vs hawtbrowser changelog</summary>

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
```
