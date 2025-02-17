# quteFF

Transform Firefox into a keyboard-driven browser inspired by Qutebrowser's minimal interface. quteFF combines custom CSS theming with Vimium-FF's to create a cohesive keyboard driven browsing experience.

## Features

- Clean, minimal interface styled to match Qutebrowser
- Full keyboard navigation via Vimium-FF
- Customizable HUD and command interface
- Optional New Tab page integration

## Preview

### Qute influenced simple UI
![Minimal Browser Interface](https://github.com/user-attachments/assets/f5be697d-4815-48fa-97c1-9ffed6c3015c)

### Command Mode
![Vimium Command Interface](https://github.com/user-attachments/assets/2fbc341f-d27e-4722-bc42-7f3351f169ad)

### Link Navigation
![Link Hints](https://github.com/user-attachments/assets/9d970671-e209-40e5-950e-cb7ff8708ba5)

### HUD Display
![Heads Up Display](https://github.com/user-attachments/assets/e5f320f7-cbec-4ebe-92a8-e214c59b2532)

## Installation

### Required Components

1. **Enable Custom CSS**
   - Navigate to `about:config`
   - Set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`

2. **Install CSS Theme**
   - Go to `about:profiles`
   - Open your Root Directory
   - Create a `chrome` folder if it doesn't exist
   - Create `userChrome.css` and paste the provided CSS code
   - Restart Firefox

3. **Install Vimium-FF**
   - Install from the [official repository](https://github.com/philc/vimium/)

### Optional Enhancements

1. **Custom Vimium Theme**
   - Apply the [provided CSS theme](https://github.com/mac-tron/quteff/blob/main/vimium-ff.css) in Vimium-FF settings

2. **New Tab Override**
   - Install [New Tab Override](https://github.com/cadeyrn/newtaboverride)
   - Configure the following settings:
     
     **a. Custom URL**
     - Set to: `https://mac-tron.github.io/quteff/`
     - Only `http://` or `https://` URLs are supported
     - For local files, use a local web server (e.g., MAMP, XAMPP)
     
     **b. Focus Behavior**
     - Enable: "Set focus to the web page instead of the address bar"
     - Improves keyboard navigation by focusing on content immediately

## URL Bar Customization

Enhance the URL bar experience with these optional tweaks:

### Simplified Results
```
browser.urlbar.maxRichResults = 0
```
Disables rich preview cards in URL bar results

### Smart Autocomplete
```
browser.urlbar.autocomplete.inline = true
```
Enables inline URL completion as you type

## Technical Details

<details>
<summary>Changes from hawtbrowser</summary>

Key improvements over the original [hawtbrowser](https://github.com/IanLeCorbeau/hawtbrowser) theme:

### Interface Refinements
- Consistent toolbar and button sizing
- Improved extension icon handling
- Enhanced tab highlighting with purple accents
- Standardized spacing and alignment

### Technical Updates
- Added aspect-ratio properties for better scaling
- Improved icon containment and scaling
- Enhanced extension button layout
- Standardized height variable usage

</details>

## References

This project builds upon and is influenced by the following open-source projects:

- [Qutebrowser](https://www.qutebrowser.org/) - Original inspiration for the keyboard-driven interface
- [hawtbrowser](https://github.com/IanLeCorbeau/hawtbrowser) - Base Firefox CSS customization
- [Vimium-FF](https://github.com/philc/vimium/) - Keyboard navigation extension
- [New Tab Override](https://github.com/cadeyrn/newtaboverride) - New tab page customization
- [Vimium Custom CSS](https://github.com/okaihe/vomnibar-custom-css) - Vomnibar styling reference
