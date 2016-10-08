# RetroTxt Changes

## 1.5

### September 2016

- Detects and converts many [ANSI Control Sequence Introduces](https://en.wikipedia.org/wiki/ANSI.SYS) used by MS-DOS's ANSI.SYS to display ANSI art.
- Detects and converts legacy BBS colour codes for [PCBoard and Wildcat!](http://wiki.synchro.net/custom:colors#pcboard_wildcat_format).
- **_Apply RetroTxt to any text files hosted on these websites_** will only run on a user supplied whitelist of website domains. This will stop it from conflicting with secured login sessions used by some websites.
- Options has been reworked with a refresh to its look including the use of Google's [Material Icons](https://design.google.com/icons/).
- Introduced a new, charcoal coloured icon that should class less with most browser themes.
- **_Automatic detect & run RetroTxt on text files feature_** has been renamed to **_Apply RetroTxt to any text files hosted on these websites_**.
- Options, font samples now reset when the user's mouse leaves the font selection form.
- **_Display formatting control codes as DOS CP-437 glyphs_** has been renamed to **_DOS control glyphs_**.
- When checked **_DOS control glyphs_** will show a few ASCII control characters in the sample text.
- Refactored much of the JavaScript source to use [ECMAScript 6](http://es6-features.org) specific features.
- Improved handling of [file:///](file:///) domains.
- Uses asynchronous `XMLHttpRequest.open()` functionality as browser support of synchronous requests may end.
- Context menus now use checkmarks for active options.
- Context menus code in `eventpages.js` has been redesigned so it is now easier to add new themes and Display options.

  ###### Firefox specific fixes
- Requires Firefox 49+.
- Options dialogue is better themed to Firefox's style guides. <small>(Unfortunately Firefox on Linux still has some strange <code>input</code> style quirks)</small>
- Fixed Options not supporting UK locales.
- Fixed first time run bugs that required RetroTxt to reload for it to work correctly.
- Fixed RetroTxt trying to run on about: URIs.
- RetroTxt should be slightly less resource intensive as previously there were some event filters that Firefox was ignoring.

## 1.25

### 2 July 2016

- **_Automatic detect & run RetroTxt on text files feature_** **is now more reliable and intuitive**. It's (experimental) tag has been dropped and can now be considered stable.
- _Automatic detect & run RetroTxt..._ also has a hardcoded blacklist of domains to ignore which previously this feature conflicted with.
- Added [QUnit](https://qunitjs.com/) testing. A _Tests_ link to the results page will show up with Chrome in Options when using a _development_ install.
- Fixed vertical lines artefacts issue with block fonts with most colour combinations.
- Firefox specific bugs fixed including incorrect `normal` line height and weird toolbar button behaviour.
- Refactored a number of function names to be more descriptive of their purpose.
- Started the transition of replacing `var` with `let` and `const`.
- Some functions now return more meaningful errors when missing required parameters.

## 1.2

### 22 June 2016

- **Now works in Firefox** but requires at least Firefox (Gecko) 48.
- Tested in Opera (Blink) and works great.

#### Differences between using Firefox and Chrome?

- Chrome uses event pages while Firefox uses the less desirable persistent background pages. Event pages only load when needed so in theory they should be less resource intensive.
- Firefox and the Gecko engine renders multiple block characters better than the Blink engine used in Chrome. The Blink engine adds light but distracting vertical lines.
- Firefox's Options UI does not support the unified `chrome_style`.
- The toolbar button in Firefox does not support right-click context menus.
- Context menus in Firefox are not filtered by URL types as it doesn't support the `documentUrlPatterns` property.
- When loading RetroTxt both Chrome and Firefox will throw warnings about unrecognised items in the manifest.

## 1.1

### 21 June 2016

- **Added ability to increase the whitespace between rows of text (line space)**.
- **Rearranged the Options menu to be more compact**.
- Changed the sample text found in the Options menu.
- Removed the Options, font selection mouseout event to make the font samples more stable.
- Added IBM BIOS font (only 2y and 2x were previously included).
- Created this file.