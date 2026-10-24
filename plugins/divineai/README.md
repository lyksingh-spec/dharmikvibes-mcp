# DivineAI

![DivineAI icon](assets/icon.png)

DivineAI by DharmikVibes is a Hindu spiritual companion. With this plugin Claude answers three everyday questions: the panchang for your city (sunrise, sunset, and the tithi, nakshatra, yoga and karana at sunrise with end times, for more than fifty Indian and overseas cities), upcoming festival dates from a verified calendar where a date is kept only when the panchang and an independent official, temple or sampradaya source agree, and the coming vrat days (Ekadashi, Pradosh, Purnima and festival fasts) with their deity.

## Use it

Ask in Hindi, Hinglish or English, for example for today's tithi in Varanasi or when the next Ekadashi is. Every panchang answer says the city, time zone and date it is for, and festivals still being checked are shown as date to be confirmed, never guessed.

Example prompts:

- Aaj Varanasi mein tithi aur nakshatra kya hai?
- When is Diwali this year, and what festivals are coming in the next two months?
- When is the next Ekadashi, and how is it kept?

## Install

In Claude Code, add the DharmikVibes marketplace and install the plugin:

```
/plugin marketplace add lyksingh-spec/dharmikvibes-mcp
/plugin install divineai --marketplace lyksingh-spec/dharmikvibes-mcp
```

On claude.ai and in Cowork, add it from the directory once it is listed.

## What is in this plugin

- A connector, `divineai`, that points at the public, read-only DivineAI MCP server at https://divineai-mcp.dharmikvibes.com/claude/divineai. On claude.ai and in Cowork, add it from the plugin's Connectors tab. No sign-in is needed.
- Skills that tell Claude when to use the connector and how to answer:

- `festival-dates`
- `panchang-today`
- `plan-vrat`

The connector's tools are all read-only (`readOnlyHint` true, `destructiveHint` false):

| Tool | What it returns |
|---|---|
| `get_panchang` | Panchang for a city and day |
| `get_festival_dates` | Verified festival and observance dates in a window |
| `get_vrat_guide` | Vrat days with dates, deity and basis |

## What it does not do

The plugin is read-only. It has no prices, does not book pujas or yatras, set reminders, sign you in or see any personal data, and gives no astrology predictions or medical advice. Anyone unwell, pregnant, diabetic or on medicine should check with their doctor before fasting.

## Data

The plugin runs no code on your computer and has no hooks or scripts. When a skill uses the connector, Claude sends your search words, city, dates or the id of a page to divineai-mcp.dharmikvibes.com, which DharmikVibes operates, and shows you what comes back. The server needs no account, asks for no personal data and returns only public content. Requests are logged for security and reliability as described in the privacy policy. Nothing is sent anywhere else.

- Privacy policy: https://divineai.dharmikvibes.com/en/privacy/
- Terms: https://divineai.dharmikvibes.com/en/terms/
- Support: https://divineai.dharmikvibes.com/en/support/

## Publisher

DIVVIB LIFESTYLE PRIVATE LIMITED (DharmikVibes), Plot No 4, 2nd Floor, Minarch Tower, Sector 44, Gurugram 122003, Haryana, India. Contact: hi@dharmikvibes.com.

## License

MIT. See [LICENSE](LICENSE).
