# SuppCo for Claude

SuppCo helps you research dietary supplements and keep track of the ones you take. This plugin connects Claude to SuppCo's MCP server and adds skills that show Claude how to use it well.

## What you can do

Without signing in:

- Search SuppCo's supplement catalog and compare a product with alternatives in its category.
- See product and brand TrustScores, SuppCo's quality rating based on manufacturing, certifications and testing.
- Read SuppCo's summaries of published research for a supplement, with evidence grades.
- Look up a nutrient's forms, typical intake ranges and upper limits, and find supplement protocols for goals like sleep or energy.

After you connect your SuppCo account:

- View and update your supplement stack and schedule.
- See your nutrient totals, your personalized nutrient plan and your StackScore.
- Save preferences for future SuppCo conversations.
- Add SuppCo Buying Club products to your cart and get a checkout link. Purchases are only completed on SuppCo's own checkout page; no tool takes payment.

SuppCo provides general supplement information, not medical advice, and does not diagnose or treat any condition.

## What's included

- `.mcp.json`: the SuppCo remote MCP server at `https://api.supp.co/mcp` (streamable HTTP).
- `skills/choose-a-supplement`: finding and comparing products and brands.
- `skills/review-my-stack`: reviewing and updating your stack, StackScore and nutrients.
- `skills/supplement-research`: research summaries, nutrient reference values and protocols.
- `skills/buying-club-cart`: Buying Club search, cart and checkout link.

The plugin contains only Markdown and JSON. It runs no local code, hooks or scripts, and installs no packages.

## Connecting your account

On claude.ai and in Cowork, open the plugin's Connectors tab and connect SuppCo. Claude signs you in through SuppCo's OAuth page at `login.supp.co` and asks you to approve access. Catalog and research tools work without signing in.

## Data and privacy

Claude sends your requests only to SuppCo's MCP server at `api.supp.co`. When you connect your account, SuppCo's tools read and, when you ask, update your SuppCo stack, schedule, profile, saved preferences and Buying Club cart. The plugin sends data nowhere else. See SuppCo's [privacy policy](https://supp.co/about/privacy-policy) and [terms of use](https://supp.co/about/terms-of-use).

## Support

Email support@supp.co or visit https://supp.co/contact.
