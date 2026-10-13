# Privacy policy — Lumi GEO

*Version française : [lire en français](fr.html).*

*Last updated: October 12, 2026*

Lumi GEO is an extension for the Chrome browser that analyses the open web page: what AI crawlers see of it, structured data, AI crawler access, SEO basics, llms.txt file.

## Data collected

**None for the analysis.** Lumi GEO does not collect, transmit, sell or share any browsing data: the pages you analyse and their results never leave your device.

The only exception is the optional **Pro subscription** (see below): it is handled by Lemon Squeezy, which receives the information needed for the payment.

## How it works

- The analysis only happens **when you click** the extension icon, and only on that tab.
- It runs **entirely in your browser**. No server belonging to the publisher is contacted, and the analysis uses no external API.
- To check the `/robots.txt`, `/llms.txt` and `/llms-full.txt` files, and to get the raw HTML of the page ("robot view"), the extension requests them **from the site you are visiting**, exactly as your browser would (the raw HTML is requested without cookies, as a crawler would). No other address is contacted.
- The detailed results are not stored and disappear when the panel is closed. Only the final score is kept (see below).
- The interface language follows the language of Chrome: nothing is stored or sent for it.

## Local storage

The extension stores in your browser (`chrome.storage.local`), and nowhere else:

- your interface preferences (animations on or off, Lumi's introduction already seen);
- if you subscribed: your **license key** and the identifier of its activation in this browser, and your **last known plan** (Free or Pro, status of the key, email of the purchase), so that a subscriber keeps Pro for a few days without a connection;
- the **score history of each analysed page** (address of the page without its parameters, date, overall score and scores of the 4 pillars), to show how it changes. At most 30 analyses per page and 300 pages; the oldest are forgotten first;
- for the free plan, the **daily count of analyses** (5 different pages a day): today's date and a short code computed from each page analysed today. The code does not contain the address of the page and it cannot be read back from it. This count starts again every day.

This information never leaves your device. You can erase the score history at any time (Settings › "Clear the score history"); the daily count replaces itself every day; everything disappears if you uninstall the extension.

## Lumi AI (Chrome's built-in AI)

When you click "Ask Lumi", the text of the analysed page is read by **the AI built into Chrome (Gemini Nano)**, which runs **on your computer**. No text is sent to a server, to the publisher of Lumi GEO or to an online AI service. The first time, Chrome downloads its AI model (only once, from Google): Chrome handles this download, not Lumi GEO. The AI's answers are not stored.

## PDF report

The report is built in your browser. Its data goes through Chrome's session memory (`chrome.storage.session`), emptied when the browser is closed, then is displayed in an extension tab. The PDF is created by Chrome's print feature: no online service is used.

## Pro subscription (optional)

Lumi GEO Pro is a paid subscription. Payments are handled by **Lemon Squeezy** (lemonsqueezy.com), the official seller (merchant of record): the payment page is theirs, and Lumi GEO never sees your card number.

- After the payment, Lemon Squeezy sends you a **license key** by email. You paste it in Lumi GEO (Plans).
- Nothing is sent to Lemon Squeezy as long as you have not entered a key.
- With a key, the extension sends to Lemon Squeezy's License API (api.lemonsqueezy.com) **only the key, the identifier of its activation and the label "Lumi GEO (Chrome)"**: when you activate it, each time the panel opens (to check that the subscription is still active), and when you remove it from the browser.
- Lemon Squeezy receives what you enter on its payment page (email address, payment details, billing address) and processes it under its own privacy policy: [Lemon Squeezy](https://www.lemonsqueezy.com/privacy).
- No browsing data and no analysis result is ever sent to it.

## Analytics and advertising

None. The extension contains no analytics tool, no tracker and no advertising.

## Permissions requested

| Permission  | Use                                                                                                          |
| ----------- | ------------------------------------------------------------------------------------------------------------ |
| `activeTab` | Read the open page, only after you click the icon                                                            |
| `scripting` | Run the analysis script in that page, after that click                                                       |
| `sidePanel` | Show the results in the side panel                                                                           |
| `storage`   | Remember your interface preferences, the score history, your plan and the daily count of free analyses; prepare the PDF report |

## Contact

For any question: matteo.spring67@gmail.com
