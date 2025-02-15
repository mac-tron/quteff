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

# quteFF vs hawtbrowser changelog

A comparison of changes between the original [hawtbrowser](https://github.com/IanLeCorbeau/hawtbrowser) and quteFF CSS.

## Navigation Bar Changes

### Toolbar Height and Positioning
```css
max-height: var(--uc-bottom-toolbar-height) !important;
padding: 0 !important;
margin: 0 !important;
