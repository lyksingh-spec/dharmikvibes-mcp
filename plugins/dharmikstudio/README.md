# DharmikStudio

![DharmikStudio icon](assets/icon.png)

DharmikStudio is the public catalogue of DharmikVibes: Indian spiritual audio, video and reading in Hindi and English. It covers gently told audio series of the epics (Ramayana, Devi Mahatmya, Shivaji Maharaj), the Gita for everyday life, aartis and mantras with their meaning, katha and pravachan, temple and tirtha stories (the Jyotirlingas, Rameswaram, Vrindavan), festival and vrat guides (Navratri, Diwali, Karwa Chauth, Ekadashi, Chhath), children's bedtime stories, courses and articles.

## Use it

Ask in Hindi, Hinglish or English. Claude searches the catalogue, opens a work to show its episodes or lessons, lists categories and new releases, and always gives you the studio.dharmikvibes.com link so you can listen, watch or read there.

Example prompts:

- Find a Hindi audio series on the Ramayana I can listen to tonight.
- एकादशी व्रत कैसे रखें? DharmikStudio से बताइए।
- Aartis and mantras for Lord Ganesha, with their meaning.
- Tell me the story of Rameswaram and give me something to listen to.

## Install

In Claude Code, add the DharmikVibes marketplace and install the plugin:

```
/plugin marketplace add lyksingh-spec/dharmikvibes-mcp
/plugin install dharmikstudio --marketplace lyksingh-spec/dharmikvibes-mcp
```

On claude.ai and in Cowork, add it from the directory once it is listed.

## What is in this plugin

- A connector, `dharmikstudio`, that points at the public, read-only DharmikStudio MCP server at https://studio.dharmikvibes.com/mcp. On claude.ai and in Cowork, add it from the plugin's Connectors tab. No sign-in is needed.
- Skills that tell Claude when to use the connector and how to answer:

- `deity-bhajans-aartis`
- `explain-festival-vrat`
- `find-devotional-series`
- `temple-tirtha-stories`

The connector's tools are all read-only (`readOnlyHint` true, `destructiveHint` false):

| Tool | What it returns |
|---|---|
| `search` | Search the catalogue in Hindi, Hinglish or English |
| `fetch` | Full public record of one work or place |
| `search_catalogue` | Ranked search with language, type and category filters |
| `get_item` | Episodes or lessons, length, access and other-language versions of one work |
| `list_categories` | Categories with counts and browse pages |
| `new_releases` | Works published or updated in the last 1 to 30 days |

## What it does not do

The plugin is read-only. It does not sign you in, see any account or listening history, take payments, book pujas or yatras, or give astrology, medical or financial advice. It returns only content that is publicly listed on studio.dharmikvibes.com.

## Data

The plugin runs no code on your computer and has no hooks or scripts. When a skill uses the connector, Claude sends your search words, city, dates or the id of a page to studio.dharmikvibes.com, which DharmikVibes operates, and shows you what comes back. The server needs no account, asks for no personal data and returns only public content. Requests are logged for security and reliability as described in the privacy policy. Nothing is sent anywhere else.

- Privacy policy: https://studio.dharmikvibes.com/privacy
- Terms: https://studio.dharmikvibes.com/terms
- Support: https://studio.dharmikvibes.com/support

## Publisher

DIVVIB LIFESTYLE PRIVATE LIMITED (DharmikVibes), Plot No 4, 2nd Floor, Minarch Tower, Sector 44, Gurugram 122003, Haryana, India. Contact: hi@dharmikvibes.com.

## License

MIT. See [LICENSE](LICENSE).
