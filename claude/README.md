# Price Agreed plugin for Claude

Lets Claude (chat, Cowork and Claude Code) find UK
tradespeople, send them one job, compare their quotes and accept one for the
user.

## What's inside

- `.mcp.json`: the Price Agreed MCP server at `https://mcp.priceagreed.com/mcp/claude`
  (Streamable HTTP, no authentication, no variables to set).
- `skills/hire-a-tradesperson`: how to use the tools in order, when to ask the
  user, and how to treat text written by tradespeople.

## Configuration

None. Price Agreed needs no account or API key. Each job returns its own
access token, which the assistant keeps for that job.

## Usage

Install the plugin, then ask, for example:

- "Find me a plumber near Leeds LS6 who can fix a leaking kitchen tap."
- "Send my job to the three you found." (Claude reads the details back and asks first.)
- "Check my job for quotes this evening and tell me the cheapest."
- "Accept the £180 quote from Smith Plumbing."

The job reaches tradespeople only after the user confirms it from the email
Price Agreed sends them. Quotes are also emailed to the user.

## Privacy

Personal data (the user's name, email, phone, postcode and job description) is
sent only when the user asks to send a job. See
https://priceagreed.com/privacy. Operator: ELK CONSULTING LTD, company number
17326346, England and Wales. Support: support@priceagreed.com.
