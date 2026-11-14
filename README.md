# Super Baldi Maker status

The game reads `status.json` from this repository every time it starts, and every 5 minutes while it's open.

## Announce an update

Change `latestVersion` to the new version number (the same number as **Project Settings → Player → Version** in Unity).
Anyone running an older version sees an "Update available!" message with a button to `updateUrl`.

## Broadcast a message

Add an entry to `broadcasts`:

```json
{
  "latestVersion": "1.0",
  "updateUrl": "https://gamebanana.com/mods/740285",
  "broadcasts": [
    {
      "id": "2026-11-14-welcome",
      "title": "Heads up!",
      "message": "Thanks for playing Super Baldi Maker!",
      "sent": "2026-11-14T02:30:00Z",
      "expires": "2026-12-01T00:00:00Z"
    }
  ]
}
```

- `id` must be different for every message. Each player sees each `id` only once.
- `sent` is optional. It's shown under the title as "Sent November 14, 2026 at 9:30 PM", converted to each player's own time zone. Write it in UTC (the `Z` at the end).
- `expires` is optional. After that date (UTC) the message is no longer shown.
- Messages are plain text.
- GitHub can take up to 5 minutes to serve a changed file.
