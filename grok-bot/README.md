# Price Agreed plugin for Grok Bot

Lets Grok Bot (and Cursor, which shares the same plugin marketplace) find
tradespeople in any country, send them one job, compare their quotes and accept one for the
user.

## What's inside

- `mcp.json`: the Price Agreed MCP server at `https://mcp.priceagreed.com/mcp/grok`
  (Streamable HTTP, no authentication, no variables to set).
- `skills/hire-a-tradesperson`: how to use the tools in order, when to ask the
  user, and how to treat text written by tradespeople.

## Configuration

None. Price Agreed needs no account or API key. Each job returns its own
access token, which the assistant keeps for that job.

## Usage

Install the plugin, then ask, for example:

- "Find me a plumber near Leeds LS6 who can fix a leaking kitchen tap."
- "I need an electrician in Lyon, France, to replace a fuse box."
  (The assistant asks which country if it isn't clear.)
- "Send my job to the three you found." (Grok Bot reads the details back and asks first.)
- "Check my job for quotes this evening and tell me the cheapest."
- "Accept the £180 quote from Smith Plumbing." (Each job has its own currency, e.g. EUR in France.)

The job reaches tradespeople only after the user confirms it from the email
Price Agreed sends them. Quotes are also emailed to the user.

## Privacy

Personal data (the user's email, country and postcode or town, job title and description, plus name and
phone if given) is sent only when the user asks to send a job. See
https://priceagreed.com/privacy. Operator: ELK CONSULTING LTD, company number
17326346, England and Wales. Support: support@priceagreed.com.
