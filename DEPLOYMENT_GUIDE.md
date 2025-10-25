# Deploying WAHA Website to Cloudflare Pages

This guide will help you deploy your enhanced WAHA hockey website to Cloudflare Pages for fast, reliable hosting.

## Prerequisites

- GitHub account with your website repository
- Cloudflare account (free tier is sufficient)
- Domain name (wahahockey.org) managed through Cloudflare

## Step 1: Prepare Your Repository

1. **Upload all website files to GitHub**
   - Create a new repository named `wahahockey` (or similar)
   - Upload all the enhanced website files
   - Make sure the repository is public or upgrade to allow private repos

2. **Update Configuration**
   - Edit `admin/config.yml` line 3: Update with your GitHub username/repo
   - Edit `config.toml` line 10: Add your actual donation platform URL
   - Commit these changes to GitHub

## Step 2: Connect to Cloudflare Pages

1. **Log into Cloudflare Dashboard**
   - Go to https://dash.cloudflare.com/
   - Navigate to "Pages" in the sidebar

2. **Create New Project**
   - Click "Create a project"
   - Choose "Connect to Git"
   - Select "GitHub" and authorize the connection

3. **Select Your Repository**
   - Choose your `wahahockey` repository
   - Click "Begin setup"

## Step 3: Configure Build Settings

Use these exact settings:

**Project name**: `waha-hockey` (or your preference)  
**Production branch**: `main`  
**Build command**: `hugo --minify`  
**Build output directory**: `public`  

**Environment Variables**:
- Variable name: `HUGO_VERSION`
- Value: `0.120.0`

Click "Save and Deploy"

## Step 4: Configure Custom Domain

1. **Add Custom Domain**
   - In your Cloudflare Pages project, go to "Custom domains"
   - Click "Set up a custom domain"
   - Enter: `wahahockey.org`
   - Also add: `www.wahahockey.org`

2. **DNS Configuration**
   - Cloudflare will automatically configure DNS
   - Verify both domains show "Active" status

## Step 5: SSL/Security Setup

1. **SSL Settings** (in Cloudflare DNS dashboard)
   - Set SSL/TLS encryption mode to "Full (strict)"
   - Enable "Always Use HTTPS"
   - Enable "Automatic HTTPS Rewrites"

2. **Security Features**
   - Enable "Brotli compression" for faster loading
   - Consider enabling "Minification" for CSS/JS/HTML

## Step 6: Content Management Setup

### GitHub OAuth for CMS

1. **Create GitHub OAuth App**
   - Go to GitHub Settings → Developer settings → OAuth Apps
   - Click "New OAuth App"
   - **Application name**: "WAHA Hockey CMS"
   - **Homepage URL**: `https://wahahockey.org`
   - **Authorization callback URL**: `https://wahahockey.org/admin/`

2. **Configure Netlify Identity** (Alternative)
   - Or use Netlify Identity for simpler setup
   - Add environment variable: `NETLIFY_SITE_ID`

### Test Content Management

1. **Access CMS**
   - Go to `https://wahahockey.org/admin/`
   - Test login and content creation
   - Verify changes appear on the site

## Step 7: Performance Optimization

### Cloudflare Settings

1. **Speed Tab**
   - Enable "Auto Minify" for CSS, JS, HTML
   - Enable "Brotli" compression
   - Set "Browser Cache TTL" to 4 hours

2. **Caching**
   - Enable "Development Mode" temporarily for testing
   - Disable when site is ready for production

## Step 8: Analytics Setup (Optional)

1. **Cloudflare Web Analytics**
   - Enable in Cloudflare dashboard
   - Automatic setup, no code changes needed

2. **Google Analytics** (if preferred)
   - Add tracking code to `layouts/_default/baseof.html`
   - Insert before closing `</head>` tag

## Testing Your Deployment

### Functionality Checklist

- [ ] Website loads at wahahockey.org
- [ ] All pages accessible (About, Programs, Donate, etc.)
- [ ] Logo displays correctly in header
- [ ] Favicon appears in browser tab
- [ ] Mobile responsiveness works
- [ ] Donation button links to correct platform
- [ ] Admin panel accessible at /admin/
- [ ] Content management works
- [ ] Images and media load properly

### Performance Testing

Use these tools to verify performance:
- **PageSpeed Insights**: https://pagespeed.web.dev/
- **Cloudflare Analytics**: Built into dashboard
- **GTmetrix**: https://gtmetrix.com/

Target metrics:
- Page load time: Under 3 seconds
- Mobile score: 90+ 
- Desktop score: 95+

## Troubleshooting

### Common Issues

**Build fails:**
- Check Hugo version in environment variables
- Verify all files are committed to GitHub
- Check for syntax errors in config files

**Content not updating:**
- Clear Cloudflare cache in dashboard
- Check if CMS is properly configured
- Verify GitHub OAuth settings

**Images not loading:**
- Check file paths in markdown content
- Verify images are in correct folders
- Test image URLs directly

**Domain not working:**
- Verify DNS settings in Cloudflare
- Check custom domain configuration
- Allow up to 48 hours for DNS propagation

## Maintenance

### Regular Tasks

- **Weekly**: Check for broken links and images
- **Monthly**: Review site performance metrics
- **Quarterly**: Update Hugo version if needed
- **Annually**: Renew domain registration

### Backup Strategy

- **Code**: Automatically backed up in GitHub
- **Content**: Stored in markdown files in repository  
- **Images**: Uploaded files stored in GitHub
- **Database**: Not applicable (static site)

## Security

### Best Practices

- Keep Hugo version updated
- Regularly review CMS user access
- Monitor Cloudflare security events
- Use strong passwords for all accounts

### Content Security

- All content changes tracked in GitHub
- Review process available for sensitive updates
- Rollback capability through Git history

---

## Quick Reference

**Website URL**: https://wahahockey.org  
**Admin Panel**: https://wahahockey.org/admin/  
**GitHub Repo**: https://github.com/[username]/wahahockey  
**Cloudflare Dashboard**: https://dash.cloudflare.com/  

**Support Contacts**:
- Technical issues: [Insert tech volunteer email]
- Content questions: [Insert communications lead email]
- Emergency: [Insert board member email]

---

*Your WAHA website is now live and ready for the community!*