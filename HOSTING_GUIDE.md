# Domain & Hosting Guide - Subscription Compass

**Quick guide to hosting your privacy policy and website**

---

## 🎯 What You Need

1. **Domain Name**: `subscriptioncompass.com` (or similar)
2. **Hosting**: Place to put your `privacy.html` file
3. **SSL Certificate**: HTTPS (required by Chrome Web Store)

**Total Cost**: $0-15/year (can be completely free!)

---

## 🚀 Option 1: GitHub Pages (FREE - Recommended for MVP)

**Best for**: Quick setup, free hosting, perfect for privacy policy

### Step 1: Create GitHub Repository

```bash
# 1. Go to: https://github.com/new
# 2. Repository name: subscription-compass-website
# 3. Set to Public
# 4. Click "Create repository"
```

### Step 2: Upload Your Files

```bash
# Option A: Via GitHub Web Interface
1. Click "Add file" → "Upload files"
2. Drag privacy.html
3. Commit changes

# Option B: Via Git (if you have it installed)
cd /Users/williampalasti/Desktop/CancelKey
git init
git add privacy.html
git commit -m "Add privacy policy"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/subscription-compass-website.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

```bash
1. Go to repository Settings
2. Scroll to "Pages" section (left sidebar)
3. Source: Deploy from branch
4. Branch: main, folder: / (root)
5. Click Save
```

### Step 4: Access Your Page

```
Your privacy policy will be at:
https://YOUR-USERNAME.github.io/subscription-compass-website/privacy.html

Example:
https://williampalasti.github.io/subscription-compass-website/privacy.html
```

### Step 5: Update manifest.json

```json
{
  "privacy_policy": "https://YOUR-USERNAME.github.io/subscription-compass-website/privacy.html"
}
```

**Pros:**
- ✅ Completely FREE
- ✅ HTTPS included
- ✅ Fast setup (5 minutes)
- ✅ Easy updates (just push to GitHub)
- ✅ Reliable (99.9% uptime)

**Cons:**
- ⚠️ URL includes github.io (not custom domain yet)
- ⚠️ Can add custom domain later for $12/year

---

## 🌐 Option 2: Custom Domain + GitHub Pages ($12/year)

**Best for**: Professional look with custom domain

### Step 1: Buy Domain

**Recommended Registrars:**

#### Namecheap (Cheapest)
```
1. Go to: https://www.namecheap.com
2. Search: subscriptioncompass.com
3. Price: ~$9-13/year for .com
4. Add to cart and checkout
```

#### Google Domains / Squarespace Domains
```
1. Go to: https://domains.google.com (now Squarespace)
2. Search: subscriptioncompass.com
3. Price: ~$12/year
4. Purchase
```

#### Cloudflare (Best Value)
```
1. Go to: https://www.cloudflare.com/products/registrar/
2. Search: subscriptioncompass.com
3. Price: ~$9/year (at-cost pricing)
4. Requires Cloudflare account (free)
```

### Step 2: Set Up GitHub Pages (Same as Option 1)

Follow Option 1 steps 1-3 above.

### Step 3: Configure Custom Domain

**In GitHub:**
```bash
1. Repository Settings → Pages
2. Custom domain: subscriptioncompass.com
3. Click Save
4. Wait for DNS check
```

**In Your Domain Registrar:**
```bash
# Add these DNS records:

Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153

Type: CNAME
Name: www
Value: YOUR-USERNAME.github.io
```

### Step 4: Enable HTTPS

```bash
1. In GitHub Pages settings
2. Check "Enforce HTTPS"
3. Wait 24 hours for certificate
```

### Step 5: Update manifest.json

```json
{
  "homepage_url": "https://subscriptioncompass.com",
  "privacy_policy": "https://subscriptioncompass.com/privacy.html"
}
```

**Total Cost**: $9-13/year
**Setup Time**: 30 minutes + 24 hours for DNS

---

## 💰 Option 3: Netlify (FREE with Custom Domain)

**Best for**: More features, easy deployment

### Step 1: Create Netlify Account

```bash
1. Go to: https://www.netlify.com
2. Sign up (free)
3. Connect GitHub account
```

### Step 2: Deploy Site

```bash
1. Click "Add new site" → "Import an existing project"
2. Choose GitHub
3. Select your repository
4. Build settings:
   - Build command: (leave empty)
   - Publish directory: /
5. Click "Deploy site"
```

### Step 3: Your Site is Live!

```
Netlify gives you a URL like:
https://random-name-12345.netlify.app/privacy.html

You can customize the subdomain:
https://subscriptioncompass.netlify.app/privacy.html
```

### Step 4: Add Custom Domain (Optional)

```bash
1. Buy domain (see Option 2)
2. In Netlify: Site settings → Domain management
3. Add custom domain: subscriptioncompass.com
4. Follow DNS instructions
5. HTTPS automatic!
```

**Pros:**
- ✅ FREE hosting
- ✅ Automatic HTTPS
- ✅ Automatic deployments from GitHub
- ✅ Custom domain support
- ✅ Fast CDN

**Cons:**
- ⚠️ Still need to buy domain for custom URL

---

## ⚡ Option 4: Vercel (FREE - Similar to Netlify)

**Best for**: Developer-friendly, great performance

### Quick Setup:

```bash
1. Go to: https://vercel.com
2. Sign up with GitHub
3. Import repository
4. Deploy (automatic)
5. Get URL: https://subscription-compass.vercel.app
```

**Same features as Netlify, slightly different interface**

---

## 🎯 Recommended Path for You

### For Immediate Testing (Today):

**Use GitHub Pages (Free)**
```bash
1. Create GitHub repo (5 min)
2. Upload privacy.html (2 min)
3. Enable Pages (2 min)
4. Update manifest.json with github.io URL
5. Submit to Chrome Web Store

Total time: 10 minutes
Total cost: $0
```

### For Production Launch (Next Week):

**Buy Domain + GitHub Pages**
```bash
1. Buy subscriptioncompass.com on Namecheap ($12)
2. Configure DNS to point to GitHub Pages
3. Update manifest.json with custom domain
4. Update Chrome Web Store listing

Total time: 30 min + 24hr DNS
Total cost: $12/year
```

---

## 📋 Step-by-Step: GitHub Pages Setup (Detailed)

### 1. Create GitHub Account (if needed)

```bash
Go to: https://github.com/signup
Enter email, create password
Verify email
```

### 2. Create Repository

```bash
1. Click "+" in top right → "New repository"
2. Name: subscription-compass-website
3. Description: "Privacy policy and website for Subscription Compass"
4. Public (must be public for free GitHub Pages)
5. Click "Create repository"
```

### 3. Upload Privacy Policy

```bash
# Method 1: Web Interface (Easiest)
1. Click "uploading an existing file"
2. Drag privacy.html from your Desktop/CancelKey folder
3. Commit message: "Add privacy policy"
4. Click "Commit changes"

# Method 2: GitHub Desktop App
1. Download GitHub Desktop
2. Clone repository
3. Copy privacy.html to folder
4. Commit and push
```

### 4. Enable GitHub Pages

```bash
1. Click "Settings" tab (top of repository)
2. Click "Pages" in left sidebar
3. Under "Source":
   - Branch: main
   - Folder: / (root)
4. Click "Save"
5. Wait 1-2 minutes
```

### 5. Test Your Page

```bash
GitHub will show: "Your site is live at https://..."
Click the URL
Add /privacy.html to the end
Example: https://williampalasti.github.io/subscription-compass-website/privacy.html

Should see your privacy policy!
```

### 6. Update Extension

```bash
# In manifest.json, change:
"privacy_policy": "https://YOUR-USERNAME.github.io/subscription-compass-website/privacy.html"

# Replace YOUR-USERNAME with your actual GitHub username
```

---

## 🔧 Troubleshooting

### Issue: GitHub Pages not working

**Solution:**
```bash
1. Check repository is Public (not Private)
2. Wait 5 minutes after enabling Pages
3. Check Settings → Pages shows green checkmark
4. Try accessing: https://USERNAME.github.io/REPO-NAME/
```

### Issue: 404 Not Found

**Solution:**
```bash
1. Make sure file is named exactly: privacy.html (lowercase)
2. Check file is in root directory (not in a folder)
3. Clear browser cache
4. Try incognito/private window
```

### Issue: DNS not working (custom domain)

**Solution:**
```bash
1. DNS takes 24-48 hours to propagate
2. Check DNS with: https://dnschecker.org
3. Make sure you added ALL 4 A records
4. CNAME should point to username.github.io (not the full URL)
```

---

## 💡 Pro Tips

### Tip 1: Create a Simple Homepage

```html
<!-- index.html -->
<!DOCTYPE html>
<html>
<head>
    <title>Subscription Compass</title>
</head>
<body>
    <h1>🧭 Subscription Compass</h1>
    <p>Find subscription cancellation buttons instantly.</p>
    <a href="privacy.html">Privacy Policy</a>
</body>
</html>
```

Upload this as `index.html` to have a homepage at your domain.

### Tip 2: Add Terms of Service

```bash
# Create terms.html (similar to privacy.html)
# Upload to same repository
# Access at: https://your-domain.com/terms.html
```

### Tip 3: Use Cloudflare (Free CDN)

```bash
1. Sign up at cloudflare.com
2. Add your domain
3. Update nameservers at registrar
4. Get free SSL, CDN, and DDoS protection
```

---

## 📊 Cost Comparison

| Option | Setup Time | Cost/Year | Custom Domain | HTTPS |
|--------|------------|-----------|---------------|-------|
| GitHub Pages | 10 min | $0 | ❌ | ✅ |
| GitHub + Domain | 30 min | $12 | ✅ | ✅ |
| Netlify Free | 15 min | $0 | ❌ | ✅ |
| Netlify + Domain | 30 min | $12 | ✅ | ✅ |
| Vercel Free | 15 min | $0 | ❌ | ✅ |
| Vercel + Domain | 30 min | $12 | ✅ | ✅ |

**Recommendation**: Start with GitHub Pages (free), buy domain later when you're ready to launch.

---

## 🎯 Action Plan

### Today (10 minutes):
1. ✅ Create GitHub account
2. ✅ Create repository
3. ✅ Upload privacy.html
4. ✅ Enable GitHub Pages
5. ✅ Update manifest.json with GitHub Pages URL

### This Week (when ready to launch):
1. Buy domain on Namecheap ($12)
2. Configure DNS
3. Wait 24 hours
4. Update manifest.json with custom domain

### Future (optional):
1. Add homepage (index.html)
2. Add terms of service
3. Add Chrome Web Store badges
4. Add contact form

---

## 📞 Need Help?

### GitHub Pages Documentation:
- https://pages.github.com/
- https://docs.github.com/en/pages

### Domain Registrars:
- Namecheap: https://www.namecheap.com
- Cloudflare: https://www.cloudflare.com/products/registrar/
- Google Domains: https://domains.google.com

### Hosting Platforms:
- Netlify: https://www.netlify.com
- Vercel: https://vercel.com
- GitHub Pages: https://pages.github.com

---

## ✅ Quick Checklist

Before submitting to Chrome Web Store:

- [ ] Privacy policy hosted and accessible
- [ ] HTTPS enabled (automatic with GitHub Pages)
- [ ] URL updated in manifest.json
- [ ] Privacy policy loads correctly
- [ ] No broken links
- [ ] Mobile-friendly (privacy.html already is)
- [ ] Contact email works

---

**You're ready to host! Start with GitHub Pages (free) and upgrade to custom domain later.** 🚀

*Estimated time to go live: 10 minutes*
