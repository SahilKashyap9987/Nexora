# Project Fixes & Improvements

### 1. Tech Stack & Performance: Removed Duplicate Libraries
**Found:** `index.html`, `contact.html`, etc. were loading multiple conflicting versions of Bootstrap (3.4.1 & 5.3.3) and jQuery (1.7.1 & 3.7.1).
**Cause:** Intentional "slop" causing slow load times and console conflicts.
**Fix:** Removed legacy Bootstrap 3.4.1 and jQuery 1.7.1. Kept only the modern, single versions to improve Lighthouse score.
**Source:** [chat 1, prompt 7]

### 2. Functionality: Contact Form Traps
**Found:** Users couldn't submit the form. Captcha demanded `2+2=5`, Send/Clear buttons were reversed, and message required 500 chars.
**Cause:** Deliberate anti-abuse traps.
**Fix:** Fixed captcha logic to `4`, swapped button handlers, bound the modal close button, and set sane character limits.
**Source:** [chat 1, prompt 3]

### 3. Theme & UI/UX: Light/Dark Mode Implementation
**Found:** The site lacked a required Theme toggle.
**Cause:** Missing CSS architecture for dark mode.
**Fix:** Implemented a fully functional `.dark-mode` override across the site.
**Source:** [chat 1, prompt 8]

### 4. Accessibility & Responsiveness
**Found:** Missing semantic tags, alt text on images, and broken mobile viewports.
**Cause:** Poor initial markup.
**Fix:** Added `aria-labels`, `alt` attributes to images, and ensured all pages respond correctly at 360px, 768px, and 1440px.
**Source:** [chat 1, prompt 8]

### 5. Functionality: Logic & Calculation Errors
**Found:** Broken tools (BMI cm/m error, Age calculator using deprecated getYear), Admin dashboard bugs (qty.length undefined), and Blog pagination offset issues.
**Cause:** Broken logic and inverted formulas.
**Fix:** Rewrote JavaScript calculations to return 100% accurate outputs.
**Source:** [chat 1, prompt 1]