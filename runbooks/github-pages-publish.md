# Publish a static site with GitHub Pages
1. Keep the site static (index.html at repo root or /docs). Use relative paths for data/assets.
2. Repo Settings > Pages > Source: Deploy from branch, main, / (root) or /docs. Save.
3. Push. Site appears at https://<user>.github.io/<repo>/ in 1-5 min (check Actions tab).
4. Private repos need a paid plan for Pages; otherwise make the entry repo public before publishing.
5. Smoke test on phone, iPad and laptop; check console for 404s (case-sensitive paths).
6. Keep total asset size small (practice: ~2 MB assets, <2 MB per JSON).
