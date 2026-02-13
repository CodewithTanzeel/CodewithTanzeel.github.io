# CodewithTanzeel.github.io

Personal website hosted at [www.tanzeelahmad.me](https://www.tanzeelahmad.me)

## Deployment

This site can be deployed on either GitHub Pages or Vercel.

### Option 1: Deploy on Vercel (Recommended)

1. Import this repository to Vercel
2. In your Vercel project settings, go to **Domains**
3. Add the custom domain: `www.tanzeelahmad.me`
4. Vercel will provide DNS records to configure
5. Update your domain's DNS settings with the provided records:
   - Add a CNAME record for `www` pointing to your Vercel deployment (e.g., `cname.vercel-dns.com`)
   - Or follow Vercel's specific DNS instructions
6. Wait for DNS propagation (can take up to 48 hours, but usually minutes)
7. Vercel will automatically provision an SSL certificate for your domain

### Option 2: Deploy on GitHub Pages

1. Go to repository Settings → Pages
2. Set Source to the main branch
3. GitHub will automatically read the CNAME file and configure the custom domain
4. Update your domain's DNS settings:
   - Add a CNAME record for `www` pointing to `CodewithTanzeel.github.io`
5. Wait for DNS propagation
6. GitHub will automatically provision an SSL certificate

## Fixing SSL Certificate Errors

If you see `ERR_CERT_COMMON_NAME_INVALID`, it means:
- The domain DNS is pointing to the hosting provider (Vercel or GitHub)
- But the custom domain hasn't been added to the project settings
- The SSL certificate doesn't include your domain name

**Solution:**
1. Make sure you've added `www.tanzeelahmad.me` to your Vercel project domains (or enabled it in GitHub Pages settings)
2. Wait for the SSL certificate to be provisioned (usually takes a few minutes)
3. Clear your browser cache and try again