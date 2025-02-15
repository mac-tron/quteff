# quteFF

* Custom userChrome.css that makes Firefox looks as close as possible to Qutebrowser.
* This is meant to be used with the [Vimium-ff](https://github.com/philc/vimium/) add-on.
* Forked from https://github.com/IanLeCorbeau/hawtbrowser/

## Screenshots
<img width="1800" alt="image" src="https://github.com/user-attachments/assets/5f2e8bfc-2db8-41b7-a655-8b087569edde" />

## Usage
* Clone the repo.    

* In Firefox, go to _about:config_, search for _toolkit.legacyUserProfileCustomizations.stylesheets_ and toggle it to __true__.

* Next go to _about:support_, and under "_Application Basics_", go to "_Profile Directory_" to find which profile you're using. You can either open the dir from the browser, of use the path to open yourself in your file manager.

* Copy the _chrome_ directory into your profile's directory.

* Install the Vimium-ff add-on.    

* Restart Firefox.

# quteFF vs hawtbrowser changelog

A comparison of changes between the original [hawtbrowser](https://github.com/IanLeCorbeau/hawtbrowser) and quteFF CSS.

## Navigation Bar Changes

### Toolbar Height and Positioning
- Added explicit max-height for nav-bar:
  ```css
  max-height: var(--uc-bottom-toolbar-height) !important
  ```
- Added padding and margin reset:
  ```css
  padding: 0 !important;
  margin: 0 !important
  ```

### Toolbar Buttons
- Added aspect-ratio constraints to toolbar buttons:
  ```css
  aspect-ratio: 1 !important
  ```
- Added object-fit contain to button icons:
  ```css
  object-fit: contain !important
  ```
- Modified toolbar button height constraints:
  ```css
  max-height: var(--uc-bottom-toolbar-height) !important;
  padding: 0 !important;
  margin: 0 1px !important;
  ```

### Extension Area Styling (New)
Added comprehensive styling for browser extensions:
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

### Overflow Button Changes
```css
/* Before */
margin: 3px 0px 0px !important;
min-height: 25px !important;
padding: 0px 0px 5px 0px !important;

/* After */
margin: 3px 0px 0px !important;
min-height: var(--uc-bottom-toolbar-height) !important;
max-height: var(--uc-bottom-toolbar-height) !important;
padding: 0 !important;
```

## Tab Styling

### Selected Tab Appearance
```css
/* Before */
background-color: #242424 !important;
border: none !important;

/* After */
background-color: #000000 !important;
border: 1px solid #B933E1 !important;
border-bottom: none !important;
```

## URL Bar Modifications

### Layout and Sizing
```css
/* Before */
min-height: var(--uc-bottom-toolbar-height) !important;
margin-left: 0px !important;

/* After */
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
- Selected tabs now have a purple border (`#B933E1`)
- Selected tabs use pure black background (changed from `#242424`)
- Extensions are grayscaled and slightly dimmed
- More consistent icon sizing and spacing

## Notes
- Core functionality remains the same as hawtbrowser
- Focus on improving scaling, consistency, and extension support
- Maintains compatibility with Firefox's dark theme
