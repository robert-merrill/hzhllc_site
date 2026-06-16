# HZH, LLC — Website

**Live URL:** https://hzhllc.com  
**Netlify project:** hzhllc (`ab66dee9-de7b-458f-89c1-9d9e3dae63af`)  
**GitHub repo:** https://github.com/robert-merrill/hzhllc_site  
**Purpose:** Establish verified digital presence for Apple Developer Program enrollment (Enrollment ID: `VTQMCY3QR8`)

---

## File Structure

```
hzhllc_site/
├── index.html       # Main single-scroll page
├── styles.css       # All styles — no framework, no external dependencies
├── privacy.html     # Privacy Policy
├── terms.html       # Terms of Service
├── favicon.svg      # Navy "H" SVG favicon
└── netlify.toml     # Clean URL redirects (/privacy → /privacy.html, /terms → /terms.html)
```

---

## Site Sections

| Section | Content |
|---|---|
| Header (sticky) | HZH, LLC wordmark + nav (About, Services, Portfolio, Contact) |
| Hero | Headline, subheadline, "Get in Touch" CTA → #contact |
| About | Firm narrative + two principal bios (Celeste Merrill, Robert Merrill) with accordion full backgrounds |
| Services | Strategic Partnerships · Talent & Recruiting · Software Innovation |
| Portfolio | Enterprise Mental Health Strategy · RecruiterBuddy · Mental Health Clinic Advisory · TextDrop Buddy · Limitless Talent |
| Contact | Email · Phone · Business Hours · Address |
| Footer | HZH, LLC tagline · Privacy Policy · Terms of Service · Copyright |

### Principals

**Celeste Merrill** — Founder & Principal  
Strategic Initiatives Lead at Vibrant Emotional Health. Former Managing Director, Huntsman Family Foundation. Mental health strategy, philanthropy, cross-sector partnership.  
LinkedIn: https://www.linkedin.com/in/celeste-merrill

**Robert Merrill** — Co-Founder & Managing Member  
Talent Futurist. Fortune 100 to seed-stage startups, 15+ countries. Bootstrapped fractional recruiting firm $0–$1.5MM ARR. Expertise in ATS/CRM, AI automation, hyper-scale hiring.  
LinkedIn: https://www.linkedin.com/in/robertmerrill/

### Contact Info
- **Email:** info@hzhllc.com
- **Phone:** 801-228-0529
- **Hours:** Monday–Friday, 9:00 AM – 5:00 PM MT
- **Address:** 299 S Main St Suite 1300 PMB 95478, Salt Lake City, UT 84111-1919

### Portfolio Links
- **RecruiterBuddy** → https://recruiterbuddy.net
- **Limitless Talent** → https://limitlesstalent.xyz

---

## Deployment

Hosted on **Netlify** with continuous deploy. To redeploy manually:

```bash
cd hzhllc_site
netlify deploy --dir=. --prod
```

Netlify CLI must be installed and authenticated:

```bash
npm install -g netlify-cli
netlify login
netlify link --id ab66dee9-de7b-458f-89c1-9d9e3dae63af
```

---

## DNS Configuration

Domain registered at **Hover**. DNS managed by **Netlify DNS**.

### Nameservers (set in Hover)
```
dns1.p01.nsone.net
dns2.p01.nsone.net
dns3.p01.nsone.net
dns4.p01.nsone.net
```

### DNS Records (managed in Netlify DNS zone `6a2f9fa8ac46f0259b72322d`)

| Type | Host | Value | Priority | TTL |
|---|---|---|---|---|
| NETLIFY | hzhllc.com | hzhllc.netlify.app | — | 3600 |
| NETLIFY | www.hzhllc.com | hzhllc.netlify.app | — | 3600 |
| MX | hzhllc.com | aspmx.l.google.com | 1 | 900 |
| MX | hzhllc.com | alt1.aspmx.l.google.com | 5 | 900 |
| MX | hzhllc.com | alt2.aspmx.l.google.com | 5 | 900 |
| MX | hzhllc.com | alt3.aspmx.l.google.com | 10 | 900 |
| MX | hzhllc.com | alt4.aspmx.l.google.com | 10 | 900 |
| TXT | hzhllc.com | google-site-verification=LUI_05RGiLOwpffEWdDL-0_4BlSdp-KRI8ZXC-mvz-k | — | 86400 |

MX records preserve Google Workspace email (info@hzhllc.com) through the DNS migration.

---

## Apple Developer Program Verification

Apple rejected enrollment citing "minimal content" and "domain registrar messages."  
Enrollment ID: **VTQMCY3QR8**

### What was built to address this
- Full single-page site with substantive content in every section
- Two named principals (Celeste Merrill, Robert Merrill) with professional bios and LinkedIn links
- Live portfolio products with working links (RecruiterBuddy, Limitless Talent)
- Named enterprise partnerships (Vibrant Emotional Health, Huntsman Mental Health Institute, Huntsman Family Foundation)
- Business hours, phone, full address in contact section
- Functional Privacy Policy and Terms of Service pages (9 sections each, Utah governing law)
- No placeholder content, no dead links, no "coming soon" text
- Favicon, meta description, clean URL structure

### Remaining checklist before resubmitting

- [x] **Switch nameservers in Hover** to Netlify DNS
- [ ] **Disable WHOIS privacy** on hzhllc.com in Hover — Apple's automated system checks that the registrant name matches the legal entity. With privacy on, it sees a proxy instead of "HZH, LLC."
- [ ] **Verify D-U-N-S record** at https://dnb.com — name must be exactly `HZH, LLC` (same punctuation), address and Key Principal must match enrollment submission
- [ ] **Wait ~2 weeks** from site launch before resubmitting — Apple's systems cache domain checks; immediate resubmission after a prior rejection often fails even with a fixed site
- [ ] **Use info@hzhllc.com** (not a personal email) as the Apple ID for enrollment
- [ ] **Keep phone available** (801-228-0529) — Apple may call to verbally verify enrollment

### Why the site now qualifies
Apple's "minimal content" rejection is a safeguard against shell entities. The site now demonstrates a real operating business through:
- Two named principals with verifiable credentials and LinkedIn profiles
- Live proprietary products with working URLs
- Named enterprise partnerships with real organizations
- A physical Salt Lake City address, business phone, and business hours
- Professional legal pages with Utah governing law

---

## Design Reference

- **Color palette:** Navy `#0d1b2a` (header/hero/footer) · Accent blue `#2d6cdf` · Light gray `#f5f7fa` (alternate sections) · White `#ffffff`
- **Typography:** System font stack (`system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI'`) — zero external dependencies
- **Layout:** Max-width 1100px centered container, 2rem horizontal padding
- **Grid:** CSS Grid, 3-column for services, collapses to 2-col at 900px and 1-col at 640px
- **About section:** 2-column CSS subgrid (`grid-template-rows: subgrid`) so name, title, bio, and links align across both principals
- **Accordion:** `hidden` attribute toggled by JS, `aria-expanded` for accessibility. Default view shows condensed blurb; "[+] View Full Background" expands full bio.
- **Portfolio:** Horizontal scroll carousel with arrow buttons, 3 cards visible at once (2 at 900px, 1 at 640px)
- **Hero:** Dark navy background, `clamp(2rem, 5vw, 3.2rem)` responsive headline
- **Cards:** White background, `1px solid #e0e4ea` border, `8px` border-radius, `2rem` padding
