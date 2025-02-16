# quteFF

[Qutebrowser](https://www.qutebrowser.org/) is an open source keyboard driven browser, however it lacks broad plug-in / extension support. This project aims to implement a Qutebrowser-like UX and provide keyboard capabilities via Vimium-ff with a customised Vimium-ff theme.

* Required: Custom userChrome.css to make Firefox look like Qutebrowser [forked](https://github.com/IanLeCorbeau/hawtbrowser/)
* Required: [Vimium-ff](https://github.com/philc/vimium/) plug-in
* Optional: Vimium vomnibox .css code [forked](https://github.com/okaihe/vomnibar-custom-css)
* Optional: [New Tab Override](https://github.com/cadeyrn/newtaboverride) plug-in to enable New Tabs to load a webpage, which maintains Viumum functionality

## Screenshots

* quteFF userChrome.css customisation UX

<img width="1800" alt="image" src="https://github.com/user-attachments/assets/f5be697d-4815-48fa-97c1-9ffed6c3015c" />

* Vimium-ff HUD vomnibar with customised [Vimium-FF Theme](#matching-vimium-ff-css-optional) 

<img width="1800" alt="image" src="https://github.com/user-attachments/assets/2fbc341f-d27e-4722-bc42-7f3351f169ad" />

* Link navigation

<img width="1800" alt="image" src="https://github.com/user-attachments/assets/9d970671-e209-40e5-950e-cb7ff8708ba5" />

* Vimium-ff HUD with customised [Vimium-FF Theme](#matching-vimium-ff-css-optional) 

<img width="1800" alt="image" src="https://github.com/user-attachments/assets/e5f320f7-cbec-4ebe-92a8-e214c59b2532" />


# Installation

Follow these steps to install quteFF:
* [Basic Setup](#basic-setup) - Enable customization and add CSS
* [Firefox URL Bar Customization](#firefox-url-bar-customization) - Optional URL bar tweaks
* [Vimium-FF Theme](#matching-vimium-ff-css-optional) - Optional CSS for Vimium
* [New Tab Override](https://github.com/cadeyrn/newtaboverride) installation and configuration - Optional

### Basic Setup

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
* Install the Vimium-ff plug-in
* Optional: add the vimium customised .css 
* Optional: add and configure [New Tab Override](https://github.com/cadeyrn/newtaboverride) to enable the extension to work on New Tabs

## Firefox URL Bar Customization (Optional)

Firefox uses a popup called "rich results" by default. You may want to disable this URL bar enhancement to simplify the UI. (Optional)
1. Open Firefox and navigate to `about:config`
2. Accept the warning about modifying advanced preferences
3. Search for each preference name
4. Double-click the preference to modify its value
5. Restart Firefox for changes to take full effect

### Disable Firefox Rich Results in URL Bar

```css
browser.urlbar.maxRichResults = 0
```

- Prevents the URL bar from showing rich preview cards and expanded results

### Enable Inline Autocomplete

```css
browser.urlbar.autocomplete.inline = true
```

- Enables inline autocompletion as you type in the URL bar

## Matching Vimium-ff CSS (Optional)

Matching Vimium theme using [vimium-ff.css](https://github.com/mac-tron/quteff/blob/main/vimium-ff.css) can be added to the vimium-ff css options.

## New Tab Override (Optional)

Vimium does not work on protected tabs, such as New Tabs. Whilst this is can be modified it allows all plug-ins to run in protected tabs which is not ideal.
New Tab Override enables a custom web page to be set as a "New Tab", therefore enabling Vimium functionality. Whilst Vimium has the ability to set a blank page as a New Tab, it does not cover the edge case where all tabs are closed and Firefox reloads which creates a New Tab (solved with this method).

![CleanShot 2025-02-17 at 10 23 01@2x](https://github.com/user-attachments/assets/1168b80d-e001-4299-af44-9369e482b4bb)

 
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
