# Privacy policy — Lumi GEO

*Version française : [lire en français](fr.html).*

*Last updated: October 11, 2026*

Lumi GEO is an extension for the Chrome browser that analyses the open web page: what AI crawlers see of it, structured data, AI crawler access, SEO basics, llms.txt file.

## Data collected

**None.** Lumi GEO does not collect, transmit, sell or share any personal data or browsing data.

## How it works

- The analysis only happens **when you click** the extension icon, and only on that tab.
- It runs **entirely in your browser**. No server belonging to the publisher is contacted, and the extension uses no external API.
- To check the `/robots.txt`, `/llms.txt` and `/llms-full.txt` files, and to get the raw HTML of the page ("robot view"), the extension requests them **from the site you are visiting**, exactly as your browser would (the raw HTML is requested without cookies, as a crawler would). No other address is contacted.
- The detailed results are not stored and disappear when the panel is closed. Only the final score is kept (see below).
- The interface language follows the language of Chrome: nothing is stored or sent for it.

## Local storage

The extension stores in your browser (`chrome.storage.local`), and nowhere else:

- your interface preferences (animations on or off, Lumi's introduction already seen);
- the **score history of each analysed page** (address of the page without its parameters, date, overall score and scores of the 4 pillars), to show how it changes. At most 30 analyses per page and 300 pages; the oldest are forgotten first.

This information never leaves your device. You can erase it at any time (Settings › "Clear the score history"), and everything disappears if you uninstall the extension.

## Lumi AI (Chrome's built-in AI)

When you click "Ask Lumi", the text of the analysed page is read by **the AI built into Chrome (Gemini Nano)**, which runs **on your computer**. No text is sent to a server, to the publisher of Lumi GEO or to an online AI service. The first time, Chrome downloads its AI model (only once, from Google): Chrome handles this download, not Lumi GEO. The AI's answers are not stored.

## PDF report

The report is built in your browser. Its data goes through Chrome's session memory (`chrome.storage.session`), emptied when the browser is closed, then is displayed in an extension tab. The PDF is created by Chrome's print feature: no online service is used.

## Analytics and advertising

None. The extension contains no analytics tool, no tracker and no advertising.

## Permissions requested

| Permission  | Use                                                                                                          |
| ----------- | ------------------------------------------------------------------------------------------------------------ |
| `activeTab` | Read the open page, only after you click the icon                                                            |
| `scripting` | Run the analysis script in that page, after that click                                                       |
| `sidePanel` | Show the results in the side panel                                                                           |
| `storage`   | Remember your interface preferences and the score history, only on your device; prepare the PDF report       |

## Contact

For any question: matteo.spring67@gmail.com
