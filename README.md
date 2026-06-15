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
| About | Company description + Robert Merrill principal bio (links to rahhb.xyz) |
| Services | Talent & Recruiting · Software Innovation · Strategic Partnerships |
| Portfolio | RecruiterBuddy · CareerTilt · Limitless Talent (all live links) |
| Contact | Email · Phone · Business Hours · Address |
| Footer | HZH, LLC tagline · Privacy Policy · Terms of Service · Copyright |

### Contact Info
- **Email:** info@hzhllc.com
- **Phone:** 801-228-0529
- **Hours:** Monday–Friday, 9:00 AM – 5:00 PM MT
- **Address:** 299 S Main St Suite 1300 PMB 95478, Salt Lake City, UT 84111-1919

### Portfolio Links
- **RecruiterBuddy** → https://recruiterbuddy.net
- **CareerTilt** → https://careertilt.com
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
- Named principal (Robert Merrill) with professional bio
- Three live portfolio products with working links
- Business hours, phone, full address in contact section
- Functional Privacy Policy and Terms of Service pages (9 sections each, Utah governing law)
- No placeholder content, no dead links, no "coming soon" text
- Favicon, meta description, clean URL structure

### Remaining checklist before resubmitting

- [ ] **Switch nameservers in Hover** to Netlify DNS (above)
- [ ] **Disable WHOIS privacy** on hzhllc.com in Hover — Apple's automated system checks that the registrant name matches the legal entity. With privacy on, it sees a proxy instead of "HZH, LLC."
- [ ] **Verify D-U-N-S record** at https://dnb.com — name must be exactly `HZH, LLC` (same punctuation), address and Key Principal must match enrollment submission
- [ ] **Wait 2 weeks** from site launch before resubmitting — Apple's systems cache domain checks; immediate resubmission after a prior rejection often fails even with a fixed site
- [ ] **Use info@hzhllc.com** (not a personal email) as the Apple ID for enrollment
- [ ] **Keep phone available** (801-228-0529) — Apple may call to verbally verify enrollment

### Why the site now qualifies
Apple's "minimal content" rejection is a safeguard against shell entities. The site now demonstrates a real operating business through:
- A named principal with verifiable credentials
- Three live proprietary products with working URLs
- Named enterprise partnerships (Vibrant Emotional Health, Huntsman Mental Health Institute)
- A physical Salt Lake City address, business phone, and business hours
- Professional legal pages with Utah governing law

---

## Design Reference

For recreating in Carrd or another platform, key design decisions:

- **Color palette:** Navy `#0d1b2a` (header/hero/footer) · Accent blue `#2d6cdf` · Light gray `#f5f7fa` (alternate sections) · White `#ffffff`
- **Typography:** System font stack (`system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI'`) — zero external dependencies
- **Layout:** Max-width 1100px centered container, 2rem horizontal padding
- **Grid:** CSS Grid, 3-column for services/portfolio, collapses to 2-col at 900px and 1-col at 640px
- **Hero:** Dark navy background, `clamp(2rem, 5vw, 3.2rem)` responsive headline
- **Cards:** White background, `1px solid #e0e4ea` border, `8px` border-radius, `2rem` padding

---

## AI Prompt for Recreation

To recreate or extend this site using an AI tool, use this prompt:

```
Build a professional single-page HTML/CSS website for HZH, LLC (hzhllc.com),
a Utah-based strategic consulting and software firm.

Design: Minimalist, professional. Dark navy (#0d1b2a) header/hero/footer,
white body, light gray (#f5f7fa) alternate sections, accent blue (#2d6cdf).
System font stack. No external CSS frameworks or font CDNs.

Pages needed: index.html, privacy.html, terms.html, plus a favicon.svg.

Sections (in order):
1. Sticky header — "HZH, LLC" wordmark left, nav links right (About, Services, Portfolio, Contact)
2. Hero — H1: "Strategic Consulting & Software Innovation." Subhead: "HZH, LLC bridges the gap between high-level human capital strategy and custom, automated software solutions." CTA button "Get in Touch" linking to #contact
3. About — Company description + principal bio for Robert Merrill (Founder & Principal, link to https://rahhb.xyz/). Bio: Talent Futurist, Senior Director Global Talent Acquisition, 15+ countries, bootstrapped fractional recruiting firm $0–$1.5MM ARR, expertise in ATS/CRM, AI automation, hyper-scale hiring
4. Services (3-column grid cards):
   - Talent & Recruiting: enterprise talent acquisition, RecOps, ATS/CRM optimization, hyper-scale growth hiring
   - Software Innovation: proprietary tools including RecruiterBuddy, AI-driven automation, API integrations
   - Strategic Partnerships: Vibrant Emotional Health, Huntsman Mental Health Institute
5. Portfolio (3-column grid cards with live links):
   - RecruiterBuddy (https://recruiterbuddy.net) — 24/7 AI recruiting partner, automates resume screening, interview questions, candidate comparisons. Integrated with SmartRecruiters and Airtable.
   - CareerTilt (https://careertilt.com) — 5-week Job Search Accelerator, expert coaching, online presence optimization, interview technique
   - Limitless Talent (https://limitlesstalent.xyz) — Substack newsletter on Future of Work, thought leadership for the Exponential Age
6. Contact (3-column):
   - Email: info@hzhllc.com (mailto link) · Phone: 801-228-0529 (tel link)
   - Business Hours: Monday–Friday, 9:00 AM – 5:00 PM MT
   - Address: 299 S Main St Suite 1300 PMB 95478, Salt Lake City, UT 84111-1919
7. Footer — "HZH, LLC" brand + tagline "Strategic consulting & software innovation." · Privacy Policy (/privacy) · Terms of Service (/terms) · © 2026 HZH, LLC. All rights reserved.

Legal pages: Privacy Policy and Terms of Service with 9 sections each,
effective January 1, 2026, governed by Utah law / Salt Lake County courts.
Both pages share the same header/nav/footer as index.html.
Contact block on each legal page: info@hzhllc.com · 801-228-0529 · full address.

Also create netlify.toml with redirects from /privacy → /privacy.html
and /terms → /terms.html (status 200).

No dead links. No placeholder content. No "coming soon" text.
```
