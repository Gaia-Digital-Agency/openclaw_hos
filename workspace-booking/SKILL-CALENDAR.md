# SKILL-CALENDAR.md

Use this skill when handling calendar/booking/appointment requests.

## Available Tools

You have a `google-calendar` MCP server with these tools:
- `list-events` — List calendar events for a date range
- `create-event` — Create a new calendar event
- `delete-event` — Delete a calendar event by ID
- `get-event` — Get details of a specific event
- `update-event` — Update an existing event
- `list-calendars` — List available calendars

## Common Operations

### Show bookings for today
1. Use `list-events` with today's date range (timeMin = today 00:00, timeMax = today 23:59)
2. Timezone: Asia/Makassar (WITA, UTC+8)
3. Report the count and details

### Create a booking
1. Use `create-event` with the details from the user
2. Required: summary (title), start time, end time
3. Default duration: 1 hour if not specified
4. Timezone: Asia/Makassar
5. Confirm creation to user with event summary and time

### Delete a booking
1. First use `list-events` to find events for the specified date
2. Show the user which events exist and confirm which to delete
3. Use `delete-event` with the event ID
4. Confirm deletion

### Count bookings
1. Use `list-events` for the date range
2. Report the count

## Date/Time Rules
- Always use timezone Asia/Makassar (WITA, UTC+8)
- "Today" = current date
- "Tomorrow" = current date + 1
- Format times in RFC3339: e.g. 2026-04-10T09:00:00+08:00
- Default event duration: 1 hour
- Calendar ID: "primary" (default)

## Reply Rules
- Be concise. Show event title, date, and time.
- Never expose event IDs, calendar IDs, or API details to the user.
- Never include internal reasoning or thinking in output.
