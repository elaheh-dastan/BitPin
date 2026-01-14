# MCP Tools
Instead of:

“Here’s how you could do it…”

You get:

“I actually ran it and here’s the result.”

## Playwright
Playwright is a browser automation framework.

it allows an LLM to:

- Open real web pages
- Click buttons, fill forms
- Take screenshots
- Run end-to-end tests
- Scrape dynamic websites (JS-heavy)

### Use Case Examples
- “Open Amazon, search for ‘iPhone 15’, extract prices”
- “Run this E2E test and tell me which step failed”
- “Log into staging and verify checkout works”

## Chrome DevTools
Chrome DevTools MCP integration lets the model:

- Inspect DOM (Document Object Model) structure
- Read network requests & responses
- Analyze performance metrics
- Check console errors
- View JS execution details

### Use Case Examples
- “Why is this page slow?” → analyze network waterfall
- “Which API powers this search result?”
- “Is this button rendered or dynamically injected?”
- “Find tracking events fired on add-to-cart”
