# DharmikVibes Wellness

![DharmikVibes Wellness icon](assets/icon.png)

DharmikVibes Wellness brings yoga and sadhana, darshan and aarti, Ayurveda and Jyotish together in spiritual wellness journeys across India: integrated journeys in Haridwar and Rishikesh, Kashi, Ujjain, Ayodhya and Kerala, residential retreats in Rishikesh, a forest retreat in Jim Corbett, experiences such as Antar Yatra in Lucknow, and group wellness sessions for families, societies and companies.

## Use it

Tell Claude your place, length, who is coming and your focus. Claude finds offerings that fit, opens the day-by-day plan with what is and is not included, explains care for seniors, NRIs, foreign guests and families, and lists recent wellness reading. Prices are shown only as the published labels: from-prices, indicative prices marked as indicative, and priced on enquiry where no price is published.

Example prompts:

- A 5-day Ayurveda retreat in Kerala for two. What is included?
- Yoga and Ganga aarti near Rishikesh for my parents, who are in their seventies.
- Any wellness events coming up, and something to read about a sattvic routine?

## Install

In Claude Code, add the DharmikVibes marketplace and install the plugin:

```
/plugin marketplace add lyksingh-spec/dharmikvibes-mcp
/plugin install dharmikvibes-wellness --marketplace lyksingh-spec/dharmikvibes-mcp
```

On claude.ai and in Cowork, add it from the directory once it is listed.

## What is in this plugin

- A connector, `dharmikvibes-wellness`, that points at the public, read-only DharmikVibes Wellness MCP server at https://wellness.dharmikvibes.com/mcp. On claude.ai and in Cowork, add it from the plugin's Connectors tab. No sign-in is needed.
- Skills that tell Claude when to use the connector and how to answer:

- `plan-wellness-journey`
- `wellness-events-and-reading`
- `wellness-whats-included`

The connector's tools are all read-only (`readOnlyHint` true, `destructiveHint` false):

| Tool | What it returns |
|---|---|
| `search` | Search offerings and pages |
| `fetch` | One wellness page, such as what is included or care for seniors |
| `list_offerings` | Journeys, retreats, experiences and sessions |
| `get_offering` | Day-by-day plan, inclusions, exclusions and published price label |
| `contact_and_booking` | The wellness desk contact details |
| `list_blog_posts` | Recent wellness reading |

## What it does not do

The plugin is read-only. It does not book, hold a place, take payment, send an enquiry or see any personal data, and gives no medical advice. To plan dates or book, it points you to the DharmikVibes wellness desk on WhatsApp (+91 92203 52244) or spiritualwellness@dharmikvibes.com.

## Data

The plugin runs no code on your computer and has no hooks or scripts. When a skill uses the connector, Claude sends your search words, an offering type, or the id of an offering, page or blog post to wellness.dharmikvibes.com, which DharmikVibes operates, and shows you what comes back. The server needs no account, asks for no personal data and returns only public content. Requests are logged for security and reliability as described in the privacy policy. Nothing is sent anywhere else.

- Privacy policy: https://dharmikvibes.com/privacy-policy
- Terms: https://dharmikvibes.com/terms-conditions
- Support: https://wellness.dharmikvibes.com/about

## Publisher

DIVVIB LIFESTYLE PRIVATE LIMITED (DharmikVibes), Plot No 4, 2nd Floor, Minarch Tower, Sector 44, Gurugram 122003, Haryana, India. Contact: hi@dharmikvibes.com.

## License

MIT. See [LICENSE](LICENSE).
