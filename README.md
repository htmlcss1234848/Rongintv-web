# LiveTV MPEGTS Project

## Structure

- `index.html` — responsive LiveTV interface
- `tv_channels.json` — channel configuration

## Run

Do not open `index.html` directly with `file://`.

Use a local HTTP server, for example:

```bash
python -m http.server 8000
```

Then open:

http://localhost:8000

## Channel JSON

Replace the demo URLs in `tv_channels.json` with your MPEG-TS stream URLs.

Supported format:

```json
{
  "name": "Channel Name",
  "category": "Bangla",
  "logo": "https://example.com/logo.png",
  "url": "https://example.com/live/channel.ts"
}
```

To hide a channel:

```json
{
  "name": "Hidden Channel",
  "category": "Other",
  "logo": "...",
  "url": "...",
  "status": "hidden"
}
```

## Important

The browser must be able to access the stream with CORS enabled. HTTPS pages cannot normally play an HTTP stream because of mixed-content restrictions.

This project uses MPEGTS.js 1.7.3 from jsDelivr.
