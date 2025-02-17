# quteFF

A Firefox customization that implements keyboard-focused navigation, drawing inspiration from Qutebrowser's minimalist design.
quteFF integrates custom CSS styling with Vimium-FF to enable efficient keyboard-driven browsing.

## Features

- Clean, minimal interface styled to match Qutebrowser
- Full keyboard navigation via Vimium-FF
- Themed Vimium config

## Screenshots

![quteff-screenshots](https://github.com/user-attachments/assets/46e689ef-b973-4f9d-bbc6-c48925ca2c99)

## Installation

### Required Components

1. **Enable Custom CSS**
   - Open `about:config`
   - Set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`

2. **Install CSS Theme**
   - Open `about:profiles`
   - Find Root Directory
   - Create `chrome` folder
   - Create `userChrome.css` and paste theme code
   - Restart Firefox

3. **Install Vimium-FF**
   - Install from [Firefox Add-ons](https://addons.mozilla.org/firefox/addon/vimium-ff/)

### Optional Components

1. **Vimium Theme**
   - Apply [this CSS theme](https://github.com/mac-tron/quteff/blob/main/vimium-ff.css) in Vimium settings

2. **New Tab Page**
   - Install [New Tab Override](https://addons.mozilla.org/firefox/addon/new-tab-override/)
   - Set URL: `https://mac-tron.github.io/quteff/`
   - Enable "Set focus to web page"

3. **URL Bar Tweaks**
   - Open `about:config`
   <br>

   ```
   browser.urlbar.maxRichResults = 0
   browser.urlbar.autocomplete.inline = true
   ```

## Changes from hawtbrowser

<details>
<summary>Expand for summary</summary>

Key improvements over the original [hawtbrowser](https://github.com/IanLeCorbeau/hawtbrowser) theme:

### Interface Refinements
- Consistent toolbar and button sizing
- Improved extension icon handling
- Enhanced tab highlighting with purple accents
- Standardized spacing and alignment

</details>

## Related projects

This project builds upon and is influenced by the following open-source projects:

- [Qutebrowser](https://www.qutebrowser.org/) - Original inspiration for the keyboard-driven interface
- [hawtbrowser](https://github.com/IanLeCorbeau/hawtbrowser) - Base Firefox CSS customization
- [Vimium-FF](https://github.com/philc/vimium/) - Keyboard navigation extension
- [New Tab Override](https://github.com/cadeyrn/newtaboverride) - New tab page customization
- [Vimium Custom CSS](https://github.com/okaihe/vomnibar-custom-css) - Vomnibar styling reference
