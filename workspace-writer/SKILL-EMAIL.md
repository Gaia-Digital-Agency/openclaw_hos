# SKILL-EMAIL.md

Use this skill when handling email requests (send, read, count).

## Available Tools

You have a `gmail` MCP server with these tools:
- `send_email` — Send an email (to, subject, body)
- `read_email` — Read a specific email by ID
- `search_emails` — Search emails (query, maxResults)
- `list_emails` — List emails from inbox

## Common Operations

### Check incoming emails today
1. Use `search_emails` with query: `after:YYYY/MM/DD is:inbox`
2. Report count and brief summary of senders/subjects

### Send an email
1. Use `send_email` with:
   - `to`: recipient email address
   - `subject`: the subject line
   - `body`: the email content (plain text)
2. Confirm to user: "Email sent to [recipient] with subject [subject]."

### Count sent emails today
1. Use `search_emails` with query: `after:YYYY/MM/DD in:sent`
2. Report the count

### Email a letter
1. If a letter was drafted (from a prior task), use its content as the email body
2. Use `send_email` with the recipient, subject, and letter content
3. Confirm sent

## Reply Rules
- Be concise. Confirm actions clearly.
- Never expose message IDs, thread IDs, or API details.
- Never include internal reasoning or thinking in output.
- Use plain text for email bodies unless HTML is specifically requested.
