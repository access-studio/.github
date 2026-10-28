# Access Studio

Web accessibility audits.

## AccessStudioBot

If you saw `AccessStudioBot` in your logs, it was us:
`AccessStudioBot/1.0 (+https://github.com/access-studio)`

- It respects `robots.txt` and crawls slowly.
- It stops at any bot protection and never tries to get round it.
- It never sends forms, buys or creates accounts.

To block it, add to your `robots.txt`:

    User-agent: AccessStudioBot
    Disallow: /

Questions or requests: open an issue in this repository.
