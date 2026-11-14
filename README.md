# Super Baldi Maker status

The game reads `status.json` every time it starts, and every 5 minutes while it's open.

```json
{
  "version": "1.0",
  "message": ""
}
```

## Send a message to everyone

Type your message between the quotes of `message` and commit:

```json
{
  "version": "1.0",
  "message": "Thanks for playing Super Baldi Maker!"
}
```

- Everyone sees it once. The popup shows the date and time you committed it, in each player's own time zone.
- Change the text to send a new message. Set it back to `""` to send nothing.
- Optional: add `"title": "Heads up!"` to change the popup title (default is "Message").

## Announce an update

Change `version` to the new version number. Anyone whose game is on a different version sees
"Update available!" with a button to the GameBanana page.

Use the same number as **Project Settings → Player → Version** in Unity when you build the update.

GitHub can take up to 5 minutes to show a change to everyone.
