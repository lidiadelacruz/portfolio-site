# Technical PRD: Community Portfolio Page

## Technical Overview

A static, single-page HTML website with embedded CSS and minimal JavaScript, optimized for performance and easy deployment.

## Technology Stack

**Frontend**
- HTML5 (semantic markup)
- CSS3 (embedded in `<style>` tag)
- Vanilla JavaScript (optional, for progressive enhancement)
- No frameworks or dependencies required

**Hosting Options**
- GitHub Pages (recommended for version control)
- Netlify (drag and drop deployment)
- Vercel (auto-deploy from Git)
- Any static file hosting service

## Architecture

### File Structure
```
portfolio/
├── index.html          # Single file containing all code
└── assets/            # Optional: if adding images
    ├── profile.jpg
    ├── project1.jpg
    └── project2.jpg
```

### HTML Structure

```
<!DOCTYPE html>
<html>
  <head>
    - Meta tags (charset, viewport, description, OG tags)
    - Title
    - Embedded CSS
  </head>
  <body>
    <header>
      - Profile image
      - Name and title
      - Tagline
      - Social links (LinkedIn, GitHub, Instagram, X)
    </header>
    
    <main>
      <section class="about">
        - About Me heading
        - Brief bio paragraph
        - Key expertise areas
      </section>
      
      <section class="featured-work">
        - Section heading
        - Work items grid
          - Work item 1 (with LinkedIn link)
          - Work item 2 (with LinkedIn link)
          - Work item 3 (with LinkedIn link)
      </section>
    </main>
    
    <footer>
      - Copyright
      - Additional links
    </footer>
    
    <script>
      - Optional progressive enhancements
    </script>
  </body>
</html>
```

## Design System

### Typography

**Font Stack**
```css
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 
             'Helvetica', 'Arial', sans-serif;
```

**Font Sizes**
- H1 (Name): 2.5rem (40px)
- H2 (Section titles): 1.5rem (24px)
- H3 (Work titles): 1.3rem (20.8px)
- Body text: 1rem (16px)
- Small text (tags, meta): 0.85rem (13.6px)

**Font Weights**
- Headings: 600-700
- Body: 400
- Tags/meta: 500

### Color Palette

**Primary Colors**
- Primary Black: #000000
- Navy Blue: #14213d (headings, important text)
- Text primary: #000000
- Text secondary: #14213d
- Background: #ffffff

**Accent Colors**
- Orange Accent: #fca311 (CTAs, highlights, hover states)
- Border: #e5e5e5
- Border hover: #14213d
- Background subtle: #f5f5f5

**Interactive States**
- Link hover: #fca311
- Button background: #fca311
- Button hover: #14213d

### Spacing System

```css
--spacing-xs: 8px
--spacing-sm: 12px
--spacing-md: 16px
--spacing-lg: 24px
--spacing-xl: 32px
--spacing-2xl: 40px
--spacing-3xl: 60px
```

### Layout

**Container**
- Max-width: 800px
- Centered with margin: 0 auto
- Padding: 40px 20px

**Grid System**
- Work items: CSS Grid
- Gap: 40px between items
- Single column on mobile
- Single column on desktop (maintains focus)

**Breakpoints**
- Mobile: < 640px
- Tablet: 640px - 1024px
- Desktop: > 1024px

## Component Specifications

### Header Component

**Requirements**
- Centered content
- Profile image: 120px circle
- Vertical spacing hierarchy
- Social links in horizontal row
- Border bottom separator

**CSS Classes**
```css
.header
.profile-img
.title
.subtitle
.social-links
```

### Work Item Component

**Requirements**
- Card-based design
- Rounded corners (8px)
- Border with hover effect
- Subtle shadow on hover
- Tags displayed as pills
- Structured content hierarchy

**CSS Classes**
```css
.work-item
.work-content
.work-tags
.tag
.work-title
.work-description
.work-details
.work-outcome
```

**Hover Behavior**
```css
.work-item:hover {
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
  border-color: #d5d5d5;
  transform: translateY(-2px);
  transition: all 0.2s ease;
}
```

### Social Links Component

**Requirements**
- Horizontal layout with flexbox
- Bordered buttons
- Hover states
- External link icons (optional)

**Links to Include**
- LinkedIn: https://linkedin.com/in/lidiadelacruz
- GitHub: https://github.com/[username]
- Instagram: https://instagram.com/[username]
- X (Twitter): https://x.com/[username]

## Content Data Structure

### Work Example Schema

```javascript
{
  title: "Project Title",
  organization: "Organization Name",
  tags: ["Tag1", "Tag2", "Tag3"],
  description: "2-3 sentence description of the project",
  role: "Your specific role and contributions",
  outcome: "Key results or impact",
  link: "Optional external link" // if applicable
}
```

### Actual Content

**Example 1: AI for Business Workshop**
```
title: "Co-Facilitator – AI for Business Workshop"
organization: "Entrepreneurs & Builders"
tags: ["Workshop Facilitation", "AI Education", "Practical Implementation"]
description: "Led a hands-on workshop demonstrating how entrepreneurs can leverage AI agents and productivity tools using Sintra AI, Notion AI, and real-world workflows. The session focused on practical adoption, not hype—showing attendees how to operationalize AI for day-to-day decision-making and execution."
role: "Co-facilitated workshop, developed curriculum focused on practical AI adoption, and guided entrepreneurs through real-world implementation."
link: "https://www.linkedin.com/posts/lidiadelacruz_aiforbusiness-latinaentrepreneurs-aistrategy-activity-7386440779113734144-GAs8"
```

**Example 2: Community-Centered Tech Talk**
```
title: "Talk Lead – Community-Centered Tech & Advocacy"
organization: "Industry Conference"
tags: ["Public Speaking", "Developer Relations", "Community Strategy"]
description: "Delivered a talk on community as a strategic layer in technology adoption, highlighting how developer trust, education, and shared learning accelerate product adoption and long-term engagement."
role: "Presented strategic insights on building developer communities and leveraging trust as a growth mechanism in tech adoption."
link: "https://www.linkedin.com/posts/lidiadelacruz_pasaporte-hispanicheritagemonth-speaker-activity-7256764168798638080-r8Su"
```

**Example 3: Google DevFest Panel**
```
title: "Panelist – Google DevFest"
organization: "Women Techmakers / GDG"
tags: ["Panel Discussion", "Diversity & Inclusion", "Developer Community"]
description: "Participated in a panel discussion focused on representation, developer growth, and building inclusive technical communities within the Google Developer ecosystem."
role: "Shared insights on building inclusive tech communities and supporting underrepresented developers in the Google ecosystem."
link: "https://www.linkedin.com/posts/lidiadelacruz_womentechmakers-google-gdg-activity-7265038749720317952-0Psf"
```

## Performance Requirements

### Load Time Targets
- First Contentful Paint: < 1.0s
- Largest Contentful Paint: < 1.5s
- Time to Interactive: < 2.0s

### Optimization Strategies
- Inline CSS (no external stylesheets)
- Optimize images (WebP format, max 800px width)
- Use system fonts (no web font loading)
- Minimize DOM depth
- Lazy load images below fold (optional)

### File Size Targets
- HTML + CSS: < 20KB
- Images: < 200KB each
- Total page weight: < 500KB

## Accessibility Requirements

**WCAG 2.1 Level AA Compliance**

**Semantic HTML**
- Proper heading hierarchy (h1 → h2 → h3)
- Semantic tags (header, main, section, footer)
- Alt text for all images
- Descriptive link text

**Keyboard Navigation**
- All interactive elements focusable
- Visible focus indicators
- Logical tab order

**Screen Reader Support**
- ARIA labels where needed
- Skip navigation link
- Descriptive page title

**Color Contrast**
- Text: minimum 4.5:1 ratio
- Interactive elements: minimum 3:1 ratio

## Browser Support

**Target Browsers**
- Chrome/Edge (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Mobile Safari (iOS 14+)
- Chrome Mobile (latest)

**Fallbacks**
- CSS Grid with flexbox fallback
- Modern CSS features with prefixes where needed

## SEO Optimization

**Meta Tags**
```html
<meta name="description" content="Community Manager & Creator Relations portfolio showcasing partnership development, content strategy, and technical education.">
<meta name="keywords" content="community manager, creator relations, developer relations, content strategy">
<meta name="author" content="Lidia">
```

**Open Graph Tags**
```html
<meta property="og:title" content="Lidia - Community & Creator Portfolio">
<meta property="og:description" content="Showcasing community management and creator collaboration work">
<meta property="og:type" content="website">
<meta property="og:url" content="[deployed URL]">
```

**Structured Data**
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Lidia",
  "jobTitle": "Community Marketing Manager",
  "url": "[portfolio URL]"
}
</script>
```

## Security Considerations

**Content Security**
- No inline JavaScript event handlers
- External links open in new tab with rel="noopener noreferrer"
- No form submissions (static page)

**Privacy**
- No tracking scripts
- No cookies
- No personal data collection

## Deployment Process

### GitHub Pages Deployment
1. Create repository: `portfolio`
2. Push `index.html` to main branch
3. Enable GitHub Pages in settings
4. Custom domain (optional): configure DNS

### Netlify Deployment
1. Drag and drop `index.html` to Netlify
2. Auto-generates URL
3. Custom domain (optional): configure in Netlify

### Vercel Deployment
1. Import repository or upload file
2. Auto-deploy on commit
3. Custom domain (optional): configure in Vercel

## Testing Checklist

**Functional Testing**
- [ ] All links work correctly
- [ ] Images load properly
- [ ] Page renders correctly in all target browsers
- [ ] Mobile responsive layout works
- [ ] No console errors

**Performance Testing**
- [ ] Lighthouse score > 90
- [ ] Page loads in < 2s on 3G
- [ ] Images optimized
- [ ] No render-blocking resources

**Accessibility Testing**
- [ ] Lighthouse accessibility score > 90
- [ ] Screen reader compatible
- [ ] Keyboard navigation works
- [ ] Color contrast passes WCAG AA

**Cross-Browser Testing**
- [ ] Chrome (desktop & mobile)
- [ ] Firefox
- [ ] Safari (desktop & mobile)
- [ ] Edge

## Maintenance Plan

**Content Updates**
- Add new work examples as completed
- Update social links as needed
- Refresh metrics quarterly

**Technical Updates**
- Review browser compatibility annually
- Update meta descriptions for SEO
- Optimize images as needed

## Rollout Plan

**Phase 1: Development (Day 1)**
- Create HTML structure
- Implement CSS styling
- Add content for 3 work examples
- Test locally

**Phase 2: Review (Day 1)**
- Review with stakeholder (Lidia)
- Make content adjustments
- Test on multiple devices

**Phase 3: Deploy (Day 1)**
- Choose hosting platform
- Deploy to production
- Test live URL
- Share link

**Phase 4: Iterate (Ongoing)**
- Gather feedback
- Make improvements
- Add new work examples

## Success Metrics

**Technical Metrics**
- Lighthouse performance score > 90
- Zero accessibility violations
- < 2s load time
- 100% uptime

**Business Metrics**
- Positive feedback from hiring managers
- Link shares increase profile views
- Clear communication of work examples

## Risk Management

**Potential Risks**
1. Images too large (slow load times)
   - Mitigation: Compress all images, use WebP format
   
2. Content too long (page feels overwhelming)
   - Mitigation: Keep descriptions concise, use scannable format
   
3. Mobile layout breaks
   - Mitigation: Test on real devices, use responsive design patterns
   
4. Link rot (external links break)
   - Mitigation: Quarterly link checking, use permalinks where possible

## Documentation

**Code Comments**
- Comment each major section
- Explain any non-obvious CSS
- Document color and spacing variables

**README**
- How to update content
- How to deploy
- How to test locally

## Appendix

### Useful Resources
- CSS Grid Guide: https://css-tricks.com/snippets/css/complete-guide-grid/
- Accessibility Checklist: https://www.a11yproject.com/checklist/
- Lighthouse Testing: Chrome DevTools

### Design Inspiration
- nnennahacks.com (reference design)
- Minimalist portfolio examples
- Card-based layouts