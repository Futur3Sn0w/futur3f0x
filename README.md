
# futur3f0x
My personal userChrome.css tweaklist and some matching UI adjustments to make Firefox look ~pretty and blurry\~ on macOS  

|Light Theme|Dark Theme|
|---|---|
|![image](https://github.com/Futur3Sn0w/futur3f0x/assets/18166632/25ce25ce-a230-49cc-a131-030c796db69c)|![image](https://github.com/Futur3Sn0w/futur3f0x/assets/18166632/ebbb82a3-cfe5-4bd0-bced-5f7bab827d8e)|

**Note:** This setup looks best on macOS, and although tested on Windows, blur doesn't work, and the layout needs tweaks to look right.

## Tweaks made
- Misc
 	- **BLUR!** Native macOS blur effects around the window. Looks great when focused or inactive!
	- Using Google Chrome icons/symbols around the UI
	- (Optional) Rounded border around the page in windowed mode (Arc-inspired)
	- (Optional) Compact 'unified extensions menu'
	- Added a bit of padding to the context menu(s)
- Automatically adjusts to light/dark theme
	- Recommended to set to **system auto theme**
	- Custom themes *should* work but aren't technically supported.
- Autohide
	- (Optional) Back/forward buttons only show when enabled
	- Tabs toolbar shows only when you have more than 1 tab
	- Tab close button only shows when tab icon (favicon) is hovered
	- Bookmarks toolbar shows when hovering in the navigation area
	- Small indicator dots (⋮) on each side of the urlbar indicate hidden items, shown when hovered
- Tabs
	- Shown below the navbar (Safari-inspired)
	- Stretch to fill available width
	- Close button is combined with favicon; show on hover
	- Newtab button moved next to extensions button
- URL bar
	- Centered text 
	- Items hidden until hovered
	- Color/theme matched to UI

## Setup and Pre-Install
If you've never setup a custom userChrome.css before, I won't go into full detail here, but there's a great writeup from Winaero that will get you where you need to be. Then, come back here to install futur3f0x!  
https://winaero.com/enable-loading-userchrome-css-usercontent-css-firefox/
  
> Before you install futur3f0x's userChrome, I'd **highly** recommend setting up the navbar as some items change when it's installed.  
  
### Customize Toolbar...
1. Remove any spacers from the toolbar
2. Add a spacer to the far-left of the toolbar, before the back, forward, reload buttons
3. Add another spacer to the right of the URL bar, before any buttons
4. Move the newtab button from the tabs bar to the left of the extensions button
> If you experiment with different layouts and/or find something you like more, feel free to screenshot and tag me on socials!

### about:config tweaks
1. Navigate to **about:config** in a new tab
2. Set the **required** keys (see below)
3. Set any **optional** or **futur3f0x specific** keys (see below) as desired
4. Navigate to **about:support**
5. Click **Clear startup cache...** and then **Restart**  

**Required:**
- Allow new icons to be properly colored:
	- Set `svg.context-properties.content.enabled` to `true`
- IF YOU want to enable the context menu tweaks, you'll need to:
	- Set `widget.macos.native-context-menus` to `false`

**Optional/Recommended:**
- Remove the tab manager dropdown from the top-left:
	- Set `browser.tabs.tabmanager.enabled` to `false`
- Enable double-click to close tabs:
	- Set `browser.tabs.closeTabByDblclick` to `true`
- Not all Firefox versions have this, but for tab-hover previews:
	- Set `browser.tabs.cardPreview.enabled` to `true`
 
**Futur3F0x specific:**
- Enable the rounded window border+padding when windowed:
	- Set `userchrome.windowed-screen-border` to `true`
- Hide back/forward buttons when disabled:
	- Set `userchrome.hide-history-nav` to `true`
- Make address bar fully transparent until hovered/clicked:
	- Set `userchrome.transparent-urlbar` to `true`
- Show more items in extensions menu by compacting it
	- Set `userchrome.compact-extensions-menu` to `true`
  
## Download/Install
The setup follows the basic process for setting up a userChrome.css file. The main difference is the addition of icon images for use around the UI.  
1. Follow the above steps ***FIRST!***
2. Open your Firefox's **chrome** folder, and remove any files inside
3. Download this repo, and copy the **userChrome.css, newIcons.css,** and the  **chrome_icons** folder to your **chrome** folder
4. In Firefox, navigate to **about:support**, click **Clear startup cache...**, and then **Restart**
5. When Firefox relaunches, you should be greeted with a pretty new UI!

## Notes and bugs
- Context menu looks a bit strange, the padding adjustments are newer so I'm still tweaking them
- In fullscreen, the background and webpage **don't** shift down when the navbar is hovered
- ~~The windowed border and padding is often broken, leaving sharp edges in place of the rounded ones~~
	- This issue has been fixed with Futur3F0x v1.2
	- Some may not prefer this, but you can enable it in **about:config** (see above)

**I DO NOT** consider this an actively maintained project. I made this largely for personal use, so I'll only update the project when I make changes (rarely); with exception of UI-breaking changes that come through Firefox updates that need to be fixed.  
Of course, those who like tweaking are always welcome to propose changes, file issues/bugs, and even fork the project, but I may not commit changes that I don't want in my own setup, as this will mirror whatever I'm currently using.

Lastly, HUGE thanks @MrOtherGuy for his incredible dedication to FirefoxCSS hacks & tricks; this would *not* be possible without him!
