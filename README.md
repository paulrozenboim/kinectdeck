# KinectDeck project website

Static project page for `https://kinect.unapaulogetic.art/`. Its public files are in `public/`. The Windows app lives separately and the site serves selected stills, studio branding and page files.

## Preview

Open `public/index.html` in a browser for a file preview, or run the following from this folder for an HTTP preview:

```powershell
py -3.12 -m http.server 4322 --bind 127.0.0.1 --directory public
```

Open [the local project page](http://127.0.0.1:4322/). The Lab and support links point to their production addresses.

## Cloudflare

This is a static-assets Worker called `kinectdeck`, with no build step. The custom domain binding in `wrangler.jsonc` points at `kinect.unapaulogetic.art`. Cloudflare manages the DNS record and certificate for the custom domain. Before the first deploy, check the zone for a pre-existing record at that exact hostname. [Cloudflare custom domains](https://developers.cloudflare.com/workers/configuration/routing/custom-domains/)

With Wrangler logged into the studio Cloudflare account, run these from this folder:

```powershell
npx wrangler deploy --dry-run
npx wrangler deploy
```

Once the Worker serves HTTPS at the custom domain, publish the reviewed homepage changes through its existing `unapaulogetic-website` deployment. Check the production Lab card and the link back to `/support/`. If managing future deployments through Cloudflare's GitHub integration, connect a dedicated website repository to the `kinectdeck` Worker and use `npx wrangler deploy` as its deploy command.

## Images

Stills are from the studio's KinectDeck reel sources and the 9 November 2026 explainer pickups. The hardware frame is cropped to the Kinect and monitor. The desktop app screenshots omit the local capture-library path. The TouchDesigner crop shows the signal path from the NDI receiver into a Transform TOP. Keep only approved derivatives in `public/assets/stills/`.
