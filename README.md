# Calgary Emergency Garage Door Repair Website

## Project Overview

This is a conversion-optimized emergency garage door repair lead generation website for Calgary, Alberta. The site is designed to capture high-intent emergency calls and form submissions, then route them to a vetted local technician network.

## Business Model

**B2B2C Emergency Dispatch Service**
- Captures emergency garage door repair requests in Calgary
- Routes leads to pre-vetted local technicians
- Revenue: Lead generation fees or referral commissions from technicians
- Market: Calgary and surrounding communities (Airdrie, Chestermere, Okotoks, Cochrane)

## Key Features

### Conversion-Focused Design
- **Sticky phone CTA** on mobile for instant calls
- **Multiple conversion points** throughout every page
- **Emergency urgency** messaging that reassures stressed homeowners
- **Trust signals** prominently displayed (licensed, insured, same-day service)
- **No-obligation assessment** to reduce friction

### SEO Optimization
- Location-specific content targeting Calgary neighborhoods
- Keyword-optimized pages for:
  - "emergency garage door repair calgary"
  - "broken garage door spring calgary"
  - "24/7 garage door repair calgary"
- Schema markup ready for local business implementation
- Fast-loading, clean HTML structure

### User Experience
- Clean, professional design (not salesy or gimmicky)
- Calm, authoritative tone for stressed homeowners
- Mobile-first responsive design
- Clear navigation and information hierarchy
- Safety warnings for DIY attempts

## Site Structure

```
/
├── index.html                  # Homepage - Main conversion page
├── broken-springs.html         # Broken Springs service page
├── styles.css                  # Master stylesheet
└── README.md                   # This file
```

### Planned Additional Pages
- `emergency-repair.html` - General emergency repair information
- `cable-track.html` - Cable and track issues
- `service-areas.html` - Comprehensive service area coverage
- `contact.html` - Contact page with large form

## Target Keywords & Traffic Strategy

### Primary Keywords
- emergency garage door repair calgary (High intent, low volume)
- 24/7 garage door repair calgary
- broken garage door spring calgary
- garage door won't open calgary

### Long-Tail Keywords
- door stuck halfway calgary
- garage door spring snapped
- vehicle trapped garage calgary
- emergency garage door service near me

### Local SEO Strategy
1. Google Business Profile optimization
2. Local citations (Yelp, HomeStars, Yellow Pages)
3. Neighborhood-specific landing pages
4. Schema markup for LocalBusiness and EmergencyService
5. Reviews and testimonials from satisfied customers

## Deployment Options

### Option 1: Static Hosting (Recommended for MVP)
**Best for:** Quick deployment, low cost, fast loading

**Providers:**
- **Netlify** - Free tier, automatic SSL, form handling
- **Vercel** - Free tier, excellent performance
- **GitHub Pages** - Free, simple deployment

**Steps (Netlify):**
```bash
# 1. Push to GitHub repository
git init
git add .
git commit -m "Initial commit"
git remote add origin YOUR_REPO_URL
git push -u origin main

# 2. Connect to Netlify
# - Sign up at netlify.com
# - Click "New site from Git"
# - Select your repository
# - Deploy settings: Build command: (leave blank), Publish directory: /
# - Deploy!

# 3. Add custom domain (optional)
# - Buy domain (e.g., yycemergencygaragedoor.ca)
# - Add DNS records in Netlify
```

### Option 2: Traditional Web Hosting
**Best for:** More control, existing hosting account

**Providers:**
- **SiteGround** - Great support, good for local businesses
- **Bluehost** - Affordable, WordPress option available
- **HostPapa** - Canadian hosting

**Steps:**
1. Purchase hosting and domain
2. Upload files via FTP or cPanel file manager
3. Configure SSL certificate
4. Set up contact form handling (FormSpree, Google Forms, or server-side)

### Option 3: WordPress Conversion
**Best for:** Easier client management, form handling, blog capability

**Why WordPress?**
- Easy for non-technical operators to update
- Better form handling with plugins (Contact Form 7, Gravity Forms)
- Call tracking integration easier
- Blog capability for content marketing

**Conversion steps:**
1. Convert HTML to WordPress theme or use page builder (Elementor)
2. Implement WPForms for contact forms
3. Add CallRail or similar for call tracking
4. Install Yoast SEO for optimization

## Critical Next Steps

### 1. Form Handling Implementation
Current forms don't have backend. Choose one:
- **FormSpree** - Simple, free tier available
- **Netlify Forms** - If hosting on Netlify
- **Email forwarding** - Simple solution for low volume
- **Custom backend** - For more control (Node.js, PHP)

### 2. Phone Number Setup
Replace `(403) 555-1234` with:
- **Call tracking number** - CallRail, CallTrackingMetrics
- **Local Calgary number** - Essential for trust
- **Toll-free option** - Consider for surrounding areas

### 3. Lead Routing System
How will leads get to technicians?
- **Manual dispatch** - You handle routing initially
- **Round-robin** - Rotate between technicians
- **Zone-based** - Assign by Calgary quadrant
- **Bid system** - Technicians bid on leads

### 4. Analytics Setup
```html
<!-- Add to <head> of all pages -->

<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>

<!-- Event tracking for calls -->
<script>
  document.querySelectorAll('a[href^="tel:"]').forEach(function(link) {
    link.addEventListener('click', function() {
      gtag('event', 'phone_call_clicked', {
        'phone_number': this.href
      });
    });
  });
</script>
```

### 5. Conversion Rate Optimization

**A/B Testing Ideas:**
- Button colors (orange vs. red for urgency)
- Phone number position
- Form length (3 fields vs. 4 fields)
- "Call Now" vs. "Get Help Now" vs. "Emergency Service"

**Heat Mapping:**
- Install Hotjar or Microsoft Clarity
- Track where users click, scroll, drop off
- Optimize based on behavior

## Marketing & Launch Strategy

### Phase 1: Soft Launch (Week 1-2)
- [ ] Deploy website
- [ ] Set up Google Business Profile
- [ ] Configure call tracking
- [ ] Test form submissions
- [ ] Create 5-10 local citations

### Phase 2: Local SEO (Week 3-4)
- [ ] Submit to HomeStars, Yelp, Yellow Pages
- [ ] Create Google My Maps with service areas
- [ ] Add schema markup
- [ ] Set up Google Search Console
- [ ] Submit sitemap

### Phase 3: Paid Advertising (Month 2)
- [ ] Google Local Services Ads (if available for your area)
- [ ] Google Search Ads (emergency keywords)
- [ ] Facebook local awareness ads
- [ ] Retargeting campaigns

### Phase 4: Content Marketing (Ongoing)
- [ ] Blog posts on garage door maintenance
- [ ] Calgary neighborhood guides
- [ ] Safety warning videos
- [ ] Customer testimonials (with permission)

## Technician Network Development

### Vetting Process
1. **License verification** - Alberta licensing requirements
2. **Insurance confirmation** - Liability and workers comp
3. **Background checks** - For peace of mind
4. **Test call** - Mystery shop their service
5. **Rate negotiation** - Lead fee or commission structure

### Partnership Structure
**Option A: Lead Fee**
- Charge $25-75 per qualified lead
- No guarantee of conversion
- Higher volume potential

**Option B: Commission**
- Charge 10-20% of job value
- Only pay on completed jobs
- Better alignment of interests
- Requires more tracking

### Finding Technicians
- Kijiji job postings
- Indeed contractor ads
- Reach out to existing independent techs
- Partner with small garage door companies
- Trade shows and industry associations

## Legal Considerations

### Required Disclaimers
✅ Already included on site:
- "We dispatch local independent garage door technicians"
- "Availability subject to technician availability"

### Additional Legal Needs
- [ ] Terms of Service page
- [ ] Privacy Policy (especially for form data)
- [ ] Service Area limitations clearly stated
- [ ] Pricing disclaimer ("Pricing set by independent contractors")
- [ ] Business license in Calgary (if required)

### Insurance Considerations
- **General Liability** - Protect against claims
- **E&O Insurance** - Professional liability
- Consider whether matching service needs insurance

## Financial Projections

### Startup Costs
- Domain: $15-50/year
- Hosting: $0-20/month (Netlify free tier)
- Call tracking: $30-100/month
- Google Ads: $500-2000/month (optional initially)
- **Total**: ~$50-150/month minimum

### Revenue Potential
**Conservative Scenario:**
- 30 leads/month @ $40/lead = $1,200/month
- Or: 15 jobs/month @ 15% commission on $400 avg job = $900/month

**Growth Scenario (Month 6+):**
- 100 leads/month @ $50/lead = $5,000/month
- Or: 50 jobs/month @ 15% commission = $3,000/month

### Break-Even Analysis
- Need approximately 5-10 paid leads per month to break even
- With 2-5% conversion rate on emergency traffic
- Need roughly 250-500 visitors/month

## Competitive Advantages

### Why This Site Will Work
1. **Pure emergency focus** - Not competing with full-service companies
2. **24/7 positioning** - Captures off-hours traffic others miss
3. **Local trust signals** - Calgary-specific, community-focused
4. **Safety-first messaging** - Builds authority and trust
5. **Mobile-optimized** - Most emergency searches are mobile
6. **No DIY nonsense** - Serious, professional tone

### Market Opportunity
- Calgary population: 1.3M+ (2023)
- High home ownership rate
- Harsh winters = more garage door issues
- Underserved emergency niche vs. general contractors

## Success Metrics

### Track Weekly
- Unique visitors
- Phone calls (tracked numbers)
- Form submissions
- Conversion rate (visitors → leads)

### Track Monthly
- Lead cost (if running ads)
- Lead quality (technician feedback)
- Customer satisfaction
- Revenue per lead/job

### Goals
- **Month 1**: 10 quality leads
- **Month 3**: 30 quality leads
- **Month 6**: 75-100 quality leads
- **Month 12**: Self-sustaining with positive ROI

## Technical Specifications

### Performance
- Target load time: < 2 seconds
- Lighthouse score: 90+ on mobile
- No external dependencies (except fonts if added)
- Optimized images (when added)

### Browser Support
- Chrome, Firefox, Safari, Edge (latest 2 versions)
- Mobile: iOS Safari, Chrome Android
- Graceful degradation for older browsers

### Accessibility
- Semantic HTML structure
- Proper heading hierarchy (h1 → h6)
- Alt text for images (when added)
- Color contrast WCAG AA compliant
- Keyboard navigation support

## Contact & Support

For questions about this project:
- **Email**: [Your contact email]
- **Phone**: [Your phone number]

---

## Quick Start Commands

```bash
# Clone or download the project
git clone [your-repo-url]
cd calgary-emergency-garage-door

# Open in browser
open index.html

# Or start a local server
python -m http.server 8000
# Then visit: http://localhost:8000
```

## License

© 2026 Calgary Emergency Garage Door Repair. All rights reserved.

---

**Built with:** Pure HTML, CSS, JavaScript (no frameworks)
**Last Updated:** January 2026
**Version:** 1.0