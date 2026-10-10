# Portfolio editing guide

This repository contains Chelsea Kezber's current static portfolio source in dist/. No build or dependency installation is required.

Edit dist/content.js for project text and interests, dist/style.css for appearance, dist/index.html for structure, and dist/app.js for behavior.

Add images under dist/assets/. To add a CV, put its PDF there and set cvUrl in content.js to assets/your-file.pdf.

Preview locally: python3 -m http.server 8000 --directory dist
Then open http://localhost:8000.

Checks: node --check dist/content.js && node --check dist/app.js

Select Kezber99/Website in Codex to work on this code. Review and commit changes through your normal GitHub workflow.

GitHub pushes do not currently deploy to the existing ChatGPT Sites website. Deployment synchronization has not been configured. The original hosted Site remains private at https://chelsea-kezber-portfolio.steadytern4.chatgpt.site. Its identity and credentials are not included here.

The current version uses project dialogs. Dedicated image-based project pages and an experience timeline have been discussed but are not implemented yet. No admin editing dashboard is included.
