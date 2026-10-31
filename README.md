# GymHappy for Claude

GymHappy helps gym owners turn happy members into public reviews, track how their reputation is trending, and keep member engagement healthy. This plugin connects Claude to your GymHappy gym account so you can ask questions about your reviews, coaches, members and messaging in plain language, and make supported changes to your GymHappy settings.

> **Who can use it:** GymHappy is available only to [PushPress](https://www.pushpress.com) gym clients with a **Grow Pro** account. You need an eligible Grow Pro account and access to your gym in GymHappy to connect.

## What you can do

- **Review analytics:** review totals, average rating and trends over any date range, grouped by day, week or month
- **Coach performance:** which coaches can receive reviews and how they are performing
- **Review fatigue:** whether members are getting too many review requests, using conversion and repeat-request data
- **Message delivery:** how your review and engagement messages are being delivered
- **Setup status:** what is still missing from your GymHappy setup checklist
- **Monthly highlights:** your current and past monthly highlights
- **Members:** search members and manage their GymHappy preferences
- **Settings:** update supported gym profile, messaging and coach settings

### Example prompts

- "How are my gym reviews performing this month?"
- "Show my review trends from September 1 to September 30, grouped weekly."
- "Which coaches at my gym can receive reviews?"
- "Are members getting tired of review requests? Look at the last 90 days."
- "What is still missing from my GymHappy setup?"
- "Show my monthly highlight history."

GymHappy does not process payments, book classes, or remove reviews from Google or other review sites.

## What's in this plugin

| Component | Purpose |
| --- | --- |
| `.mcp.json` | Connects Claude to the GymHappy MCP server at `https://app.gymhappy.co/mcp/tenant` |
| `skills/gymhappy` | Guidance that helps Claude pick the right GymHappy tool, use correct date ranges, and report results accurately |

The plugin runs no local code, scripts or hooks. All tools run on GymHappy's hosted server.

## Setup

1. Install the GymHappy plugin from the Claude directory.
2. When Claude first uses a GymHappy tool, you'll be asked to sign in. Sign in with the GymHappy account that has access to your gym and approve access.
3. Ask Claude about your gym.

Claude only sees data for the gym your GymHappy account can access. You can disconnect at any time from your Claude connector settings. Read-only tools (analytics, lookups) can run without a prompt; tools that change your settings ask for confirmation first.

## Data and privacy

- **Where data goes:** Claude sends tool requests only to GymHappy's server at `app.gymhappy.co`, operated by PushPress. The plugin sends data nowhere else.
- **Authentication:** OAuth 2.0 with PKCE, scope `mcp:tenant`. Claude never sees your GymHappy password.
- **What is accessed:** your gym's review, coach, member, messaging and setup data in GymHappy, only as needed to answer your request or make a change you asked for.
- **Storage and retention:** governed by the GymHappy privacy policy.

Privacy policy: https://app.gymhappy.co/privacy-policy
Terms of service: https://app.gymhappy.co/terms-of-service

## Support

- Help and setup docs: https://app.gymhappy.co/connect
- Support: https://app.gymhappy.co/support
- Website: https://gymhappy.co/

## License

MIT. See [LICENSE](LICENSE).
