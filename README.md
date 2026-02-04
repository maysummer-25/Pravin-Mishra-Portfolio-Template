# DMI Portfolio Website (Static HTML/CSS)

This repository contains a clean, professional-looking **static portfolio website** used in **DevOps Micro Internship (DMI)** Week 1 to practice:
- Linux basics
- Nginx hosting
- Deployment proof / ownership
- Production-style checks

✅ Students deploy this website on an Ubuntu VM using Nginx and keep it live for 24 hours.

---

## Who is this for?
- DMI students (beginner → intermediate)
- Anyone learning how to host a static site with Nginx on Linux

---

## What you will build
A portfolio-style website hosted on:
- **Ubuntu VM**
- **Nginx**
- Accessible via: `http://<public-ip>`

---

## Mandatory Ownership Proof (DMI Rule)
Before you deploy, you MUST edit the footer and add your details:

Original:

```html
<p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
```

Add this line (example):

```html
<p><strong>Deployed by:</strong> DMI Cohort 2 | Rahul Sharma | Group 4 | Week 1 | 16-01-2026</p>
```

## Footer Implementation

### Requirement
The portfolio footer displays:
- Version number (v1.0)
- Deploy date (automatically generated)
- Author name

### How the Deploy Date is Generated

The deploy date is dynamically generated using JavaScript when the page loads.

**Implementation:**
- Added a `<span id="deployDate"></span>` element in the footer
- JavaScript automatically populates it with today's date in "DD Mon YYYY" format
- Format example: "05 Feb 2026"

### Code Snippet

**HTML (footer section):**
```html
<footer>
  <p>Pravin Mishra Portfolio v1.0 — Deployed on <span id="deployDate">04-02-2026</span> — By Mmesoma Chukwumezie 
     <span style="color: green;">● Live</span>
  </p>
</footer>
```

**JavaScript:**
```javascript
const months = ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
const now = new Date();
const dateStr = now.getDate().toString().padStart(2,'0') + ' ' + months[now.getMonth()] + ' ' + now.getFullYear();
document.getElementById('deployDate').textContent = dateStr;
```

✅ This proof must be visible in your browser screenshot submission.
