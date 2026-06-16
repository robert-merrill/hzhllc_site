
# HZH, LLC: About Page Implementation Guide

## Overview
This document provides the finalized copy and technical specifications for the HZH, LLC "About" page redesign. The goal is to move from a disjointed layout to a cohesive narrative that emphasizes the synergy between our firm's core pillars: **Human-First Systems** (Mental Health/Philanthropy) and **Technical Execution** (Talent/AI).

---

## 1. Primary Page Copy

### Tagline
**We Build for the Future of Work**

### Firm Narrative
HZH, LLC is a multidisciplinary consultancy built to solve the modern paradox of growth: how to scale organizations while humanizing their systems. We combine elite mental health strategy with the technical rigor of autonomous recruitment and data-driven talent architecture. We don’t just advise; we build the tools and frameworks that allow mission-driven organizations to scale without losing their humanity.

---

## 2. Core Leadership Section
*Each entry features a concise professional summary, actionable call-to-actions, and an accordion-style "View Full Background" toggle for legacy biographical details.*

### Celeste Merrill, Founder & Principal
Anchors our work in human-first strategy and cross-sector collaboration, ensuring that every organizational solution is built on a foundation of clarity and impact.
**[Connect with Celeste on LinkedIn]**

**[+] View Full Background**
*Mental Health Strategy & Systems Leader with a career spanning philanthropy, clinical care, and cross-sector partnership. Celeste serves as Strategic Initiatives Lead at Vibrant Emotional Health and previously as Managing Director at the Huntsman Family Foundation, where she led initiatives transforming mental health and substance use systems locally and nationally. Her approach is human-first — bringing clarity, compassion, and bold coordination to complex problems.*

### Robert Merrill, Co-Founder & Managing Member
Architects our technical capabilities, utilizing AI-driven workflows and advanced analytics to ensure your talent systems are built for velocity and scale.
**[View Robert’s Portfolio (rahhb.xyz)]** | **[Connect with Robert on LinkedIn]**

**[+] View Full Background**
*Talent Futurist and Strategic People Leader with experience spanning Fortune 100 enterprises to seed-stage startups across 15+ countries. Robert bootstrapped a fractional recruiting firm from $0 to $1.5MM ARR and brings deep expertise in recruiting operations, AI-driven automation, and enterprise systems integration to every HZH, LLC engagement. Specialties include ATS/CRM platforms, advanced data analytics, technical recruiting, and hyper-scale growth hiring.*

---

## 3. Web Developer Implementation Specifications

### Structural Layout
1.  **Firm Narrative Block:** Position the primary narrative directly under the main page H1/H2 header. 
2.  **Core Leadership Grid:** Use a 2-column flexbox or CSS grid to display the leadership blurbs side-by-side. 
3.  **Accordion Interaction:** * The "Full Background" content should be hidden by default.
    * Clicking "[+] View Full Background" should toggle visibility for that specific bio.
    * The link/CTA section should remain permanently visible below the condensed bio.

### Link & CTA Requirements
* **Celeste Links:**
    * "Connect with Celeste on LinkedIn": Link to her LinkedIn profile.
* **Robert Links:**
    * "View Robert’s Portfolio (rahhb.xyz)": Link to https://rahhb.xyz.
    * "Connect with Robert on LinkedIn": Link to his LinkedIn profile.
* *Note:* Ensure clear visual separation (using a pipe `|` or line break) between Robert’s two links for mobile usability.
