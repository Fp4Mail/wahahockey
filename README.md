# WAHA Hockey Website

A modern, volunteer-friendly website for the Westborough Amateur Hockey Association built with Hugo and hosted on Cloudflare Pages.

## 🚀 Quick Start for Volunteers

### Adding Content (No Technical Skills Required!)

1. **Access the Content Management System**
   - Go to: `https://your-domain.com/admin/`
   - Sign in with your GitHub account
   - You'll see a user-friendly editor interface

2. **Adding News Articles**
   - Click "📰 News Articles" → "New News Articles"
   - Fill in the title, date, and content
   - Upload photos if you have them
   - Click "Publish" when ready

3. **Adding Photos/Videos**
   - Click "📸 Media & Videos" → "New Media & Videos"
   - Add YouTube links or Google Photos albums
   - Write a description of the content

4. **Adding Events**
   - Click "📅 Events & Games" → "New Events & Games"
   - Fill in event details, location, and time
   - Mark if registration is required

### Content Management Tips

- **Photos**: Keep images under 5MB for faster loading
- **Videos**: Upload to YouTube first, then link to them
- **Writing**: Use clear, engaging headlines
- **Publishing**: Content appears on the site within a few minutes

## 🔧 Technical Setup (One-Time Only)

### Prerequisites
- GitHub account
- Cloudflare account
- Domain name (wahahockey.org)

### Initial Setup Steps

1. **GitHub Repository**
   ```bash
   # Fork or create repository
   # Upload these files to your repo
   ```

2. **Cloudflare Pages Setup**
   - Connect your GitHub repository
   - Build command: `hugo --minify`
   - Output directory: `public`
   - Environment variable: `HUGO_VERSION = 0.119.0`

3. **Content Management**
   - Update `admin/config.yml` with your GitHub repo name
   - Enable GitHub OAuth for the CMS

4. **Essential Updates Required**
   - **Donation URL**: Update `config.toml` line 10 with your actual donation platform
   - **GitHub Repo**: Update `admin/config.yml` line 3 with your repository name
   - **Contact Info**: Update social media links in `config.toml`
   - **EIN Number**: Add your tax ID to the donation page

## 💡 Key Features

### For Volunteers
- ✅ **Easy Content Management** - No coding required
- ✅ **Photo/Video Management** - Simple media uploads
- ✅ **Mobile-Friendly** - Works on phones and tablets
- ✅ **Automatic Backups** - All changes saved to GitHub
- ✅ **Preview Mode** - See changes before publishing

### For Visitors
- ✅ **Fast Loading** - Optimized for speed
- ✅ **Donation Integration** - Secure, tax-deductible giving
- ✅ **Event Calendar** - Easy to find upcoming events
- ✅ **News & Updates** - Stay informed about WAHA
- ✅ **Mobile Responsive** - Perfect on any device

## 🎨 Customization

### Updating the Logo
1. Replace `/static/images/logo.jpg` with your new logo
2. Keep the same filename for automatic updates
3. Recommended size: 200px wide, PNG or JPG format

### Changing Colors
Edit `/static/css/waha.css`:
- `--burgundy`: Main brand color
- `--navy`: Secondary color
- `--white`: Background color

### Adding New Pages
1. Create new `.md` file in `/content/`
2. Add to navigation menu in `config.toml`
3. Update CMS config to allow editing

## 🔒 Security & Best Practices

### Content Security
- All content changes are tracked in GitHub
- Multiple people can have access without conflicts
- Changes can be reviewed before going live

### Backup Strategy
- Website files: Automatically backed up to GitHub
- Content: Stored in markdown files (easily portable)
- Images: Stored in GitHub repository

### User Management
- Add/remove CMS users through GitHub repository settings
- Different permission levels available
- Volunteer access can be granted easily

## 📊 Analytics & Performance

### Recommended Setup
- **Google Analytics**: Add tracking code to monitor traffic
- **Search Console**: Monitor SEO performance
- **Cloudflare Analytics**: Built-in performance metrics

### Performance Tips
- Images automatically optimized by Cloudflare
- Site loads from global CDN for fast access
- Mobile-first design ensures good mobile experience

## 🛠️ Troubleshooting

### Common Issues

**"Content not updating"**
- Check if changes were saved in the CMS
- Allow 2-3 minutes for changes to appear
- Clear browser cache if needed

**"Can't access admin panel"**
- Ensure GitHub OAuth is properly configured
- Check if user has repository access
- Try incognito/private browsing mode

**"Images not loading"**
- Verify image file size (keep under 5MB)
- Check file path and naming
- Ensure images are in correct folder

## 📞 Support

### For Volunteers
- **Website Issues**: Contact your tech volunteer
- **Content Questions**: Check this README first
- **Emergency**: Use GitHub issues for urgent problems

### For Technical Help
- **Hugo Documentation**: https://gohugo.io/documentation/
- **Netlify CMS Docs**: https://decapcms.org/docs/
- **Cloudflare Support**: https://support.cloudflare.com/

## 🤝 Contributing

### Volunteer Roles
- **Content Managers**: Add news, events, photos
- **Social Media**: Cross-post content to social platforms
- **Tech Support**: Handle technical issues and updates
- **Review Team**: Proofread content before publishing

### Getting Involved
1. Contact WAHA board for access
2. Complete brief orientation on content management
3. Start with simple tasks like news posts
4. Gradually take on more complex content

---

*This website is built with ❤️ by volunteers for the Westborough hockey community.*

## 📋 Setup Checklist

- [ ] GitHub repository created
- [ ] Cloudflare Pages connected
- [ ] Domain configured (wahahockey.org)
- [ ] CMS authentication setup
- [ ] Donation platform configured
- [ ] Contact information updated
- [ ] EIN number added to donation page
- [ ] Volunteer accounts created
- [ ] Google Analytics added (optional)
- [ ] Social media links updated
- [ ] Test content published successfully

**Next Steps After Setup:**
1. Create welcome post announcing new website
2. Train 2-3 volunteers on content management
3. Set up regular content schedule
4. Plan photo/video content strategy
5. Launch announcement to WAHA community