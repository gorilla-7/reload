# Imported static site

## Preview

Use the **Preview site** workflow. It runs:

```sh
python3 -m http.server 5000 --bind 0.0.0.0
```

## Publishing

Static publishing copies only `index.html` into `dist/` and publishes that directory. No dependencies or secrets are required. Use Replit's Publish action to make the site public.

## Preserved behavior

The user requested that `index.html` remain unchanged. It contains no visible page content and attempts to redirect to a relative `www.google.com` path with the URL fragment appended. That path does not lead to Google and may return a missing-page response. Publishing does not correct this behavior.
