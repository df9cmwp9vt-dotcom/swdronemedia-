# SW Drone Media Website

This is a free static website for GitHub Pages.

## Files
- `index.html` — website content
- `styles.css` — design and layout
- `assets/` — logo/flyer images

## Publish free on GitHub Pages
1. Create a free GitHub account.
2. Create a new repository called `swdronemedia`.
3. Upload `index.html`, `styles.css`, and the `assets` folder.
4. Go to Settings → Pages.
5. Under Build and deployment, choose:
   - Source: Deploy from a branch
   - Branch: main
   - Folder: /root
6. Save.
7. GitHub gives you a temporary URL like `https://yourname.github.io/swdronemedia/`.

## Connect swdronemedia.co.uk via Cloudflare
After GitHub Pages is live:
1. In the GitHub repo, create a file named `CNAME` containing only:
   swdronemedia.co.uk
2. In Cloudflare DNS, add these records:
   - Type: A, Name: @, Value: 185.199.108.153, Proxy: DNS only
   - Type: A, Name: @, Value: 185.199.109.153, Proxy: DNS only
   - Type: A, Name: @, Value: 185.199.110.153, Proxy: DNS only
   - Type: A, Name: @, Value: 185.199.111.153, Proxy: DNS only
   - Type: CNAME, Name: www, Value: yourgithubusername.github.io, Proxy: DNS only
3. In GitHub Pages, add custom domain: `swdronemedia.co.uk`.
4. Tick Enforce HTTPS once available.

## Email routing
Once DNS records exist, go back to Cloudflare Email Routing and re-check `hello@swdronemedia.co.uk` forwarding to your iCloud address.
